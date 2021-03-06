---
description: Dynamisches Einfügen eines NASA-Bilds unter dem Seitentexttag mithilfe von Inhaltsskripts
title: Erstellen eines Erweiterungslernprogramms Teil 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions
ms.openlocfilehash: 48af14c33a368a3449acb88b4dfb875ad5398e7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397916"
---
# <a name="create-an-extension-tutorial-part-2"></a><span data-ttu-id="f7992-104">Erstellen eines Erweiterungslernprogramms Teil 2</span><span class="sxs-lookup"><span data-stu-id="f7992-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="f7992-105">Quelle des abgeschlossenen Erweiterungspakets für diesen Teil</span><span class="sxs-lookup"><span data-stu-id="f7992-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a><span data-ttu-id="f7992-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f7992-106">Overview</span></span>  

<span data-ttu-id="f7992-107">Dieses Lernprogramm behandelt die folgenden Erweiterungstechnologien.</span><span class="sxs-lookup"><span data-stu-id="f7992-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="f7992-108">Injizieren von JavaScript-Bibliotheken in erweiterung</span><span class="sxs-lookup"><span data-stu-id="f7992-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="f7992-109">Verfügbar machen von Erweiterungsressourcen für Browserregisterkarten</span><span class="sxs-lookup"><span data-stu-id="f7992-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="f7992-110">Hinzufügen von Inhaltsseiten in vorhandene Browserregisterkarten</span><span class="sxs-lookup"><span data-stu-id="f7992-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="f7992-111">So können Inhaltsseiten auf Nachrichten von Popups lauschen und antworten</span><span class="sxs-lookup"><span data-stu-id="f7992-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="f7992-112">Sie erfahren, wie Sie Ihr Popupmenü aktualisieren, um Ihr statisches Startbild durch einen Titel und eine standardmäßige HTML-Schaltfläche zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f7992-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="f7992-113">Diese Schaltfläche übergibt bei Auswahl dieses Sternbilds, das in die Erweiterung eingebettet ist, an die Inhaltsseite.</span><span class="sxs-lookup"><span data-stu-id="f7992-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="f7992-114">Dieses Bild wird in die Aktive Browserregisterkarte eingefügt. Führen Sie die folgenden Schritte aus, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7992-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="f7992-115">Entfernen sie das Bild aus dem Popup, und ersetzen Sie es durch eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="f7992-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="f7992-116">Aktualisieren Sie zunächst Ihre Datei mit einem geraden Markup, `popup.html` das einen Titel und eine Schaltfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f7992-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="f7992-117">Sie werden diese Schaltfläche in Kürze programmieren, aber vorerst nur einen Verweis auf eine leere JavaScript-Datei `popup.js` hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7992-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="f7992-118">Hier ist Update-HTML.</span><span class="sxs-lookup"><span data-stu-id="f7992-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="f7992-119">Nach dem Aktualisieren und Öffnen der Erweiterung wird ein Popup mit einer Anzeigeschaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f7992-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach Auswahl des Erweiterungssymbols":::
   <span data-ttu-id="f7992-121">popup.html-Anzeige nach Auswahl des Erweiterungssymbols</span><span class="sxs-lookup"><span data-stu-id="f7992-121">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="f7992-122">Updatestrategie zum Anzeigen des Bilds am oberen Rand der Browserregisterkarte</span><span class="sxs-lookup"><span data-stu-id="f7992-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="f7992-123">Nach dem Hinzufügen der Schaltfläche besteht die nächste Aufgabe darin, die Bilddatei oben auf der aktiven `images/stars.jpeg` Registerkartenseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7992-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="f7992-124">Denken Sie daran, dass jede Registerkartenseite in einem eigenen Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="f7992-125">Außerdem verwendet die Erweiterung einen anderen Thread.</span><span class="sxs-lookup"><span data-stu-id="f7992-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="f7992-126">Erstellen Sie zunächst ein Inhaltsskript, das in die Registerkartenseite eingejiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="f7992-127">Senden Sie dann eine Nachricht von Ihrem Popup an das Inhaltsskript, das auf der Registerkartenseite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="f7992-128">Das Inhaltsskript empfängt die Nachricht, die beschreibt, welches Bild angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7992-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="f7992-129">Erstellen des Popup-JavaScript zum Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="f7992-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="f7992-130">Erstellen und fügen Sie zunächst Code hinzu, um eine Nachricht an Ihr noch nicht erstelltes Inhaltsskript zu senden, das Sie in der Zeit erstellen und in Ihre Browserregisterkarte ein- und `popup/popup.js` einwerfen müssen.  Dazu fügt der folgende Code der Popupanzeigeschaltfläche ein `onclick` Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7992-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="f7992-131">Suchen Sie `onclick` in diesem Fall nach der aktuellen Browserregisterkarte.  Verwenden Sie dann die `chrome.tabs.sendmessage` Erweiterungs-API, um eine Nachricht an diese Registerkarte zu senden.</span><span class="sxs-lookup"><span data-stu-id="f7992-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="f7992-132">In dieser Nachricht müssen Sie die URL zu dem Bild hinzufügen, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f7992-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="f7992-133">Senden Sie außerdem eine eindeutige ID, die dem eingefügten Bild zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7992-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="f7992-134">Sie können dies durch den Inhaltseinfügungs-JavaScript generieren lassen, aber aus später ersichtlichen Gründen generieren Sie diese eindeutige ID hier in und übergeben sie an das noch nicht erstellte `popup.js` Inhaltsskript.</span><span class="sxs-lookup"><span data-stu-id="f7992-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="f7992-135">Der folgende Codeausschnitt umreißt den aktualisierten Code in `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="f7992-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="f7992-136">Übergeben Sie außerdem die aktuelle Registerkarten-ID, die weiter später in diesem Artikel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="f7992-137">Machen Sie "stars.jpeg" auf einer beliebigen Browserregisterkarte verfügbar</span><span class="sxs-lookup"><span data-stu-id="f7992-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="f7992-138">Sie fragen sich wahrscheinlich, warum Sie, wenn Sie das Muss übergeben, die Chromerweiterungs-API verwenden, anstatt einfach die relative URL ohne das zusätzliche Präfix wie im vorherigen Abschnitt `images/stars.jpeg` `chrome.extension.getURL` zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f7992-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="f7992-139">Dieses zusätzliche Präfix, das mit dem angefügten Bild zurückgegeben wird, sieht im Vergleich dazu `getUrl` wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="f7992-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="f7992-140">Der Grund dafür ist, dass Sie das Bild mithilfe des Attributs des Elements in die `src` `img` Inhaltsseite einjizieren.</span><span class="sxs-lookup"><span data-stu-id="f7992-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="f7992-141">Die Inhaltsseite wird in einem eindeutigen Thread ausgeführt, der nicht mit dem Thread identisch ist, in dem die Erweiterung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="f7992-142">Sie müssen die statische Bilddatei als Web-Ressource verfügbar machen, damit sie ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f7992-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="f7992-143">Fügen Sie einen weiteren Eintrag in der Datei hinzu, um zu deklarieren, dass das Bild `manifest.json` für alle Browserregisterkarten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f7992-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="f7992-144">Dieser Eintrag lautet wie folgt \(Sie sollten ihn in der vollständigen Datei unten sehen, wenn Sie die Deklaration des Inhaltsskripts hinzufügen, die `manifest.json` angezeigt wird\).</span><span class="sxs-lookup"><span data-stu-id="f7992-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="f7992-145">Sie haben nun den Code in Ihre Datei geschrieben, um eine Nachricht an die Inhaltsseite zu senden, die auf der aktuellen aktiven Registerkartenseite eingebettet ist, aber Sie haben diese Inhaltsseite nicht erstellt und `popup.js` injiziert.</span><span class="sxs-lookup"><span data-stu-id="f7992-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="f7992-146">Machen Sie dies jetzt.</span><span class="sxs-lookup"><span data-stu-id="f7992-146">Do that now.</span></span>  

5.  <span data-ttu-id="f7992-147">Aktualisieren der manifest.jsfür Inhalt und Webzugriff</span><span class="sxs-lookup"><span data-stu-id="f7992-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="f7992-148">Die `manifest.json` aktualisierte, die das `content-scripts` und `web_accessible_resources` enthält, lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="f7992-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="f7992-149">Der hinzugefügte Abschnitt ist `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="f7992-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="f7992-150">Das Attribut ist auf festgelegt, was bedeutet, dass alle Dateien in alle Browserregisterkartenseiten injiziert werden, wenn jede Registerkarte `matches` `<all_urls>` geladen `content_scripts` wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="f7992-151">Die zulässigen Dateitypen, die injiziert werden können, sind JavaScript und CSS.</span><span class="sxs-lookup"><span data-stu-id="f7992-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="f7992-152">Sie haben auch `libjquery.min.js` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7992-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="f7992-153">Sie können dies aus dem oben im Abschnitt erwähnten Download enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7992-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="f7992-154">Hinzufügen von jQuery und Verstehen des zugeordneten Threads</span><span class="sxs-lookup"><span data-stu-id="f7992-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="f7992-155">Planen Sie in den Inhaltsskripts, die Sie injizieren, die Verwendung von jQuery \( `$` \).</span><span class="sxs-lookup"><span data-stu-id="f7992-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="f7992-156">Sie haben eine minifizierte Version von jQuery hinzugefügt und in Das Erweiterungspaket als `lib\jquery.min.js` eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f7992-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="f7992-157">Diese Inhaltsskripts werden in einzelnen Sandkasten ausgeführt, was bedeutet, dass die in die Seite eingejizierte jQuery nicht für `popup.js` den Inhalt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="f7992-158">Denken Sie daran, dass selbst wenn auf der Browserregisterkarte JavaScript auf der geladenen Webseite ausgeführt wird, alle injizierten Inhalte keinen Zugriff darauf haben.</span><span class="sxs-lookup"><span data-stu-id="f7992-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="f7992-159">Dieses injizierte JavaScript hat nur Zugriff auf das tatsächlich in dieser Browserregisterkarte geladene DOM.</span><span class="sxs-lookup"><span data-stu-id="f7992-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="f7992-160">Hinzufügen des Inhaltsskriptnachrichtenlisteners</span><span class="sxs-lookup"><span data-stu-id="f7992-160">Add the content script message listener</span></span>  

<span data-ttu-id="f7992-161">Hier ist diese Datei, die basierend auf Ihrem Abschnitt in jede `content-scripts\content.js` Browserregisterkartenseite eingejiziert `manifest.json` `content-scripts` wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="f7992-162">Beachten Sie, dass alle oben genannten JavaScript-Funktionen die Registrierung einer mit `listener` der `chrome.runtime.onMessage.addListener` Extension-API-Methode sind.</span><span class="sxs-lookup"><span data-stu-id="f7992-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="f7992-163">Dieser Listener wartet auf Nachrichten wie die, die Sie von der zuvor mit der `popup.js` `chrome.tabs.sendMessage` Extension-API-Methode gesendet haben.</span><span class="sxs-lookup"><span data-stu-id="f7992-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="f7992-164">Der erste Parameter der Methode ist eine Funktion, deren erster Parameter, request, die Details der Nachricht `addListener` ist, die übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="f7992-165">Denken Sie daran, dass diese Attribute des ersten Parameters aus und sind, wenn Sie die -Methode `popup.js` `sendMessage` verwendet `url` `imageDivId` haben.</span><span class="sxs-lookup"><span data-stu-id="f7992-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="f7992-166">Wenn ein Ereignis vom Listener verarbeitet wird, wird die Funktion ausgeführt, die der erste Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="f7992-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="f7992-167">Der erste Parameter dieser Funktion ist ein Objekt, das Attribute wie von zugewiesen `sendMessage` hat.</span><span class="sxs-lookup"><span data-stu-id="f7992-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="f7992-168">Diese Funktion verarbeitet einfach die drei jQuery-Skriptzeilen.</span><span class="sxs-lookup"><span data-stu-id="f7992-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="f7992-169">Die erste Skriptzeile fügt dynamisch in den DOM-Header einen Abschnitt ein, den Sie Ihrem Element als Klasse **\<style\>** `slide-image` zuweisen `img` müssen.</span><span class="sxs-lookup"><span data-stu-id="f7992-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="f7992-170">Die zweite Skriptzeile fügt ein Element direkt unterhalb der Browserregisterkarte an, der die Klasse zugewiesen ist, sowie die `img` `body` ID dieses `slide-image` `imageDivId` Bildelements.</span><span class="sxs-lookup"><span data-stu-id="f7992-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="f7992-171">In der dritten Skriptzeile wird ein Ereignis hinzugefügt, das das gesamte Bild umfasst, sodass der Benutzer eine beliebige Stelle im Bild auswählen kann und dieses Bild von der Seite \(zusammen mit dem Ereignislistener\) entfernt `click` wird.</span><span class="sxs-lookup"><span data-stu-id="f7992-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="f7992-172">Hinzufügen von Funktionen zum Entfernen des angezeigten Bilds bei Auswahl</span><span class="sxs-lookup"><span data-stu-id="f7992-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="f7992-173">Wenn Sie nun zu einer beliebigen Seite navigieren und ihr Erweiterungssymbol **auswählen,** wird das Popupmenü wie folgt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7992-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach Auswahl des Erweiterungssymbols":::
   <span data-ttu-id="f7992-175">popup.html-Anzeige nach Auswahl des Erweiterungssymbols</span><span class="sxs-lookup"><span data-stu-id="f7992-175">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="f7992-176">Wenn Sie die Schaltfläche `Display` auswählen, erhalten Sie die unten aufgeführten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f7992-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="f7992-177">Wenn Sie eine beliebige Stelle im Bild auswählen, wird dieses Bildelement entfernt, und Registerkartenseiten werden wieder auf das reduziert, `stars.jpeg` was ursprünglich angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="f7992-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Das im Browser angezeigte Bild":::
   <span data-ttu-id="f7992-179">Das im Browser angezeigte Bild</span><span class="sxs-lookup"><span data-stu-id="f7992-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="f7992-180">Sie haben eine Erweiterung erstellt, die erfolgreich eine Nachricht aus dem Popup des Erweiterungssymbols sendet und dynamisch JavaScript eingefügt hat, das als Inhalt auf der Registerkarte Browser ausgeführt wird.  Der injizierte Inhalt legt das Bildelement fest, um Ihre statischen Sterne jpeg anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f7992-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Abgeschlossene Erweiterungspaketquelle | Microsoft Docs"  
