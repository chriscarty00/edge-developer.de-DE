---
description: Dynamisches Einfügen eines NASA-Bilds unter dem Body-Tag der Seite mithilfe von Inhalts Skripts
title: Erstellen eines Erweiterungs Lernprogramms, Teil 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: 755b70635c93d7331ef3ac985625ba7ac5689679
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104714"
---
# <span data-ttu-id="bfdbe-104">Erstellen eines Erweiterungs Lernprogramms, Teil 2</span><span class="sxs-lookup"><span data-stu-id="bfdbe-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="bfdbe-105">Abgeschlossene Erweiterungspaket Quelle für diesen Teil</span><span class="sxs-lookup"><span data-stu-id="bfdbe-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <span data-ttu-id="bfdbe-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bfdbe-106">Overview</span></span>  

<span data-ttu-id="bfdbe-107">Dieses Lernprogramm umfasst die folgenden Erweiterungstechnologien.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="bfdbe-108">Einfügen von JavaScript-Bibliotheken in die Erweiterung</span><span class="sxs-lookup"><span data-stu-id="bfdbe-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="bfdbe-109">Verfügbar machen von Erweiterungs Ressourcen für browserregisterkarten</span><span class="sxs-lookup"><span data-stu-id="bfdbe-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="bfdbe-110">Einschließen von Inhaltsseiten in vorhandene browserregisterkarten</span><span class="sxs-lookup"><span data-stu-id="bfdbe-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="bfdbe-111">Wenn Inhaltsseiten auf Nachrichten von Popups abhören und Antworten</span><span class="sxs-lookup"><span data-stu-id="bfdbe-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="bfdbe-112">Sie erfahren, wie Sie das Popupmenü aktualisieren können, um Ihr statisches Start Bild durch einen Titel und eine standardmäßige HTML-Schaltfläche zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="bfdbe-113">Wenn diese Schaltfläche ausgewählt ist, wird das in der Erweiterung eingebettete Sternchen-Bild an die Inhaltsseite weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="bfdbe-114">Das Bild wird in die Registerkarte aktiver Browser eingefügt. Führen Sie die folgenden Schritte aus, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="bfdbe-115">Entfernen des Bilds aus dem Popup und ersetzen durch eine Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="bfdbe-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="bfdbe-116">Aktualisieren Sie zunächst die `popup.html` Datei mit einem geraden Markup, in dem ein Titel und eine Schaltfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="bfdbe-117">Sie programmieren die Schaltfläche in Kürze, aber im Moment fügen Sie einfach einen Verweis auf eine leere JavaScript-Datei hinzu `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="bfdbe-118">Hier ist Update HTML.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-118">Here is update HTML.</span></span>  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="bfdbe-119">Nach dem Aktualisieren und Öffnen der Erweiterung wird ein Popup mit einer Anzeige Schaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols":::
   <span data-ttu-id="bfdbe-121">popup.html-Anzeige nach dem Drücken des Erweiterungssymbols</span><span class="sxs-lookup"><span data-stu-id="bfdbe-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="bfdbe-122">Update Strategie zum Anzeigen des Bilds oben auf der Registerkarte "Browser"</span><span class="sxs-lookup"><span data-stu-id="bfdbe-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="bfdbe-123">Nachdem Sie die Schaltfläche hinzugefügt haben, besteht die nächste Aufgabe darin, die Bilddatei oben auf der `images/stars.jpeg` aktiven Registerkarte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="bfdbe-124">Beachten Sie, dass jede Registerkarte in einem eigenen Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="bfdbe-125">Außerdem verwendet die Erweiterung einen anderen Thread.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="bfdbe-126">Erstellen Sie zunächst ein Inhalts Skript, das in die Registerkartenseite eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="bfdbe-127">Senden Sie dann eine Nachricht vom Popup an das Inhalts Skript, das auf der Registerkartenseite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="bfdbe-128">Das Inhalts Skript empfängt die Nachricht, die beschreibt, welches Bild angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="bfdbe-129">Erstellen des Popup-Javascripts zum Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="bfdbe-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="bfdbe-130">Erstellen Sie zunächst `popup/popup.js` Code, um eine Nachricht an ihr noch nicht erstelltes Inhalts Skript zu senden, das Sie im Moment erstellen und in Ihre Browserregister Karte einfügen müssen.  Dazu fügt der folgende Code der `onclick` Popup Anzeige Schaltfläche ein Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="bfdbe-131">`onclick`Suchen Sie im Ereignis die aktuelle Browserregister Karte.  Verwenden Sie dann die `chrome.tabs.sendmessage` Erweiterungs-API, um eine Nachricht an diesen Reiter zu senden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="bfdbe-132">In dieser Nachricht müssen Sie die URL zu dem Bild hinzufügen, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="bfdbe-133">Senden Sie außerdem eine eindeutige ID, die dem eingefügten Bild zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="bfdbe-134">Sie können festlegen, dass die Inhalts Einfügung JavaScript generieren soll, aber aus Gründen, die später deutlich werden, generieren Sie diese eindeutige ID hier in `popup.js` und übergeben Sie an das noch nicht erstellte Inhalts Skript.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="bfdbe-135">Der folgende Codeausschnitt beschreibt den aktualisierten Code in `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="bfdbe-136">Übergeben Sie auch die aktuelle Tab-ID, die später in diesem Artikel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

4. <span data-ttu-id="bfdbe-137">Stellen Sie Ihre Stars. JPEG über eine beliebige Browser-Registerkarte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="bfdbe-138">Sie Fragen sich wahrscheinlich, warum Sie die `images/stars.jpeg` `chrome.extension.getURL` Chrome-Erweiterungs-API verwenden müssen, anstatt einfach nur die relative URL ohne das zusätzliche Präfix zu übergeben, wie im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="bfdbe-139">Übrigens sieht das zusätzliche Präfix, das `getUrl` mit dem angefügten Bild zurückgegeben wird, ungefähr wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="bfdbe-140">Der Grund dafür ist, dass Sie das Bild mit dem `src` Attribut des `img` Elements in die Inhaltsseite einfügen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="bfdbe-141">Die Inhaltsseite wird in einem eindeutigen Thread ausgeführt, der nicht mit dem Thread identisch ist, auf dem die Erweiterung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="bfdbe-142">Sie müssen die statische Bilddatei als Web-Ressource verfügbar machen, damit Sie ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="bfdbe-143">Fügen Sie einen weiteren Eintrag in der `manifest.json` Datei hinzu, um zu deklarieren, dass das Bild für alle browserregisterkarten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="bfdbe-144">Dieser Eintrag sieht folgendermaßen aus: \ (Sie sollten ihn in der vollständigen `manifest.json` Datei unten sehen, wenn Sie die Inhalts Skript Deklaration hinzufügen).</span><span class="sxs-lookup"><span data-stu-id="bfdbe-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="bfdbe-145">Sie haben jetzt den Code in Ihre Datei geschrieben, `popup.js` um eine Nachricht an die Inhaltsseite zu senden, die auf der aktuellen aktiven Registerkarte eingebettet ist, aber Sie haben diese Inhaltsseite nicht erstellt und injiziert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="bfdbe-146">Tun Sie das jetzt.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-146">Do that now.</span></span>  

5.  <span data-ttu-id="bfdbe-147">Aktualisieren Ihrer manifest.jsfür Inhalte und Web Access</span><span class="sxs-lookup"><span data-stu-id="bfdbe-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="bfdbe-148">Das aktualisierte `manifest.json` , das das `content-scripts` und enthält, `web_accessible_resources` ist wie folgt.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

<span data-ttu-id="bfdbe-149">Der von Ihnen hinzugefügte Abschnitt ist `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="bfdbe-150">Das `matches` Attribut ist auf festzulegen `<all_urls>` , was bedeutet, dass alle Dateien in `content_scripts` alle Registerkarten des Browsers eingefügt werden, wenn die einzelnen Registerkarten geladen werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="bfdbe-151">Die zulässigen Dateitypen, die injiziert werden können, sind JavaScript und CSS.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="bfdbe-152">Sie haben auch hinzugefügt `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="bfdbe-153">Sie können dies aus dem oben im Abschnitt genannten Download aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="bfdbe-154">Hinzufügen von jQuery und Grundlegendes zum zugehörigen Thread</span><span class="sxs-lookup"><span data-stu-id="bfdbe-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="bfdbe-155">Planen Sie in den Inhalts Skripts, die Sie injizieren, die Verwendung von jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="bfdbe-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="bfdbe-156">Sie haben eine minimierte-Version von jQuery hinzugefügt und in Ihr Erweiterungspaket als eingefügt `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="bfdbe-157">Diese Inhalts Skripts werden in einzelnen Sandboxes ausgeführt, was bedeutet, dass die in die Seite eingefügten jQuery-Dateien `popup.js` nicht für den Inhalt freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="bfdbe-158">Beachten Sie, dass, selbst wenn auf der Registerkarte Browser auf der geladenen Webseite JavaScript ausgeführt wird, jeder eingefügte Inhalt keinen Zugriff darauf hat.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="bfdbe-159">Das eingefügte JavaScript hat nur Zugriff auf das eigentliche Dom, das auf dieser Registerkarte des Browsers geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="bfdbe-160">Hinzufügen des Inhalts Skript-Nachrichten Listeners</span><span class="sxs-lookup"><span data-stu-id="bfdbe-160">Add the content script message listener</span></span>  

<span data-ttu-id="bfdbe-161">Hier sehen `content-scripts\content.js` Sie die Datei, die auf jeder Registerkarte des Browsers basierend auf Ihrem Abschnitt eingefügt wird `manifest.json` `content-scripts` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

<span data-ttu-id="bfdbe-162">Beachten Sie, dass das obige JavaScript die `listener` Verwendung der `chrome.runtime.onMessage.addListener` Erweiterungs-API-Methode registriert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="bfdbe-163">Dieser Listener wartet auf Nachrichten wie diejenige, die Sie von der `popup.js` zuvor beschriebenen mit der `chrome.tabs.sendMessage` Erweiterungs-API-Methode gesendet haben.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="bfdbe-164">Der erste Parameter der `addListener` Methode ist eine Funktion, deren erster Parameter Request die Details der übergebenen Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="bfdbe-165">Beachten Sie, `popup.js` dass die `sendMessage` Attribute des ersten Parameters, wenn Sie die Methode verwendet haben, `url` und sind `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="bfdbe-166">Wenn ein Ereignis vom Listener verarbeitet wird, wird die Funktion, die der erste Parameter ist, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="bfdbe-167">Der erste Parameter dieser Funktion ist ein Objekt, das Attribute wie zugewiesen von besitzt `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="bfdbe-168">Diese Funktion verarbeitet einfach die drei jQuery-Skriptzeilen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="bfdbe-169">Die erste Skript Zeile fügt dynamisch in die DOM-Kopfzeile einen **\<style\>** Abschnitt ein, den Sie `slide-image` dem Element als Klasse zuweisen müssen `img` .</span><span class="sxs-lookup"><span data-stu-id="bfdbe-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="bfdbe-170">Die zweite Skript Zeile fügt ein `img` Element direkt unter der `body` Registerkarte Ihres Browsers an, auf der die `slide-image` Klasse sowie die `imageDivId` ID des Bildelements zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="bfdbe-171">In der dritten Skript Zeile wird ein `click` Ereignis mit dem gesamten Bild hinzugefügt, das es dem Benutzer ermöglicht, eine beliebige Stelle im Bild auszuwählen, und dieses Bild wird von der Seite entfernt \ (zusammen mit dem Ereignis-Listener \).</span><span class="sxs-lookup"><span data-stu-id="bfdbe-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="bfdbe-172">Hinzufügen von Funktionen zum Entfernen des angezeigten Bilds bei Auswahl</span><span class="sxs-lookup"><span data-stu-id="bfdbe-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="bfdbe-173">Wenn Sie nun zu einer beliebigen Seite navigieren und das Symbol für die **Erweiterung** auswählen, wird das Popupmenü wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bfdbe-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols":::
   <span data-ttu-id="bfdbe-175">popup.html-Anzeige nach dem Drücken des Erweiterungssymbols</span><span class="sxs-lookup"><span data-stu-id="bfdbe-175">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="bfdbe-176">Wenn Sie die `Display` Schaltfläche auswählen, erhalten Sie die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="bfdbe-177">Wenn Sie eine beliebige Stelle im `stars.jpeg` Bild auswählen, wird das Bildelement entfernt, und die Registerkarten werden wieder auf die ursprüngliche Anzeige reduziert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols":::
   <span data-ttu-id="bfdbe-179">Das im Browser angezeigte Bild</span><span class="sxs-lookup"><span data-stu-id="bfdbe-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="bfdbe-180">Sie haben eine Erweiterung erstellt, mit der eine Nachricht vom Popup Symbol für die Erweiterung erfolgreich gesendet und auf der Registerkarte Browser als Inhalt dynamisch eingefügt wird.  Der eingefügte Inhalt legt das Image-Element so fest, dass die statischen Sterne JPEG angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Abgeschlossene Erweiterungspaket Quelle | Microsoft docs"  
