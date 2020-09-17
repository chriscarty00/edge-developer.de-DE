---
description: Erweiterungen erste Schritte Teil 2
title: Dynamisches Einfügen eines NASA-Bilds unter dem Body-Tag der Seite mithilfe von Inhalts Skripts
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterungen
ms.openlocfilehash: fd2276c069116a7f69f06ae50f201e284b60f3ea
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016729"
---
# Dynamisches Einfügen eines NASA-Bilds unter dem Body-Tag der Seite mithilfe von Inhalts Skripts  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## Übersicht  

In Teil 2 erfahren Sie, wie Sie das Popup-Menü aktualisieren können, damit das Bild, das Sie vorher hatten, nicht angezeigt wird, aber dieses Bild durch einen Titel und eine standardmäßige HTML-Schaltfläche ersetzt.  Wenn diese Schaltfläche ausgewählt ist, wird das in der Erweiterung eingebettete Sternchen-Bild an die Inhaltsseite weitergeleitet.  Das Bild wird in die Registerkarte aktiver Browser eingefügt.  

*   In diesem Leitfaden behandelte Erweiterungstechnologien  
    *   Einfügen von JavaScript-Bibliotheken in die Erweiterung  
    *   Verfügbar machen von Erweiterungs Ressourcen für browserregisterkarten  
    *   Einschließen von Inhaltsseiten in vorhandene browserregisterkarten  
    *   Wenn Inhaltsseiten auf Nachrichten von Popups abhören und Antworten  

## Entfernen des Bilds aus dem Popup und ersetzen durch eine Schaltfläche  

Aktualisieren Sie zunächst die `popup.html` Datei mit einem geraden Markup, in dem ein Titel und eine Schaltfläche angezeigt werden.  Sie werden die Schaltfläche in Kürze programmieren, aber im Moment fügen Sie einfach einen Verweis auf eine leere JavaScript-Datei hinzu `popup.js` .  Hier ist Update HTML.  

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
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Nachdem Sie Ihre Erweiterung aktualisiert und das Symbol für die Erweiterungs Einführung ausgewählt haben, enthält das Popupfenster die Schaltfläche Anzeige.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols":::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## Aktualisierte Strategie zum Anzeigen des Bilds oben auf der Registerkarte "Browser"  

Nachdem Sie die Schaltfläche hinzugefügt haben, besteht die nächste Aufgabe darin, die Bilddatei oben auf der `images/stars.jpeg` aktiven Registerkarte anzuzeigen.  

Beachten Sie, dass jede Registerkarte einen eigenen Thread hat und die Erweiterung einen separaten Thread aufweist.  Daher müssen Sie zuerst ein Inhalts Skript erstellen und dieses Inhalts Skript auf der Registerkartenseite einfügen.  Wenn Sie dies tun, müssen Sie eine Nachricht von Ihrem Popup an das Inhalts Skript senden, das auf der Registerkartenseite ausgeführt wird und dem Inhalts Skript mitteilt, welches Bild angezeigt werden soll und wie es angezeigt werden soll.  

## Erstellen des Popup-Javascripts zum Senden einer Nachricht  

Erstellen Sie zunächst `popup/popup.js` Code, um eine Nachricht an ihr noch nicht erstelltes Inhalts Skript zu senden, das Sie im Moment erstellen und in Ihre Browserregister Karte einfügen müssen.  Dazu fügt der folgende Code der `onclick` Popup Anzeige Schaltfläche ein Ereignis hinzu.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

Im `onclick` Fall, was Sie tun müssen, ist die aktuelle Browser-Registerkarte zu finden \ (wenn nur eine geöffnet ist, ist das eine \).  Nachdem Sie diese Registerkarte gefunden haben, verwenden Sie die `chrome.tabs.sendmessage` Erweiterungs-API, um eine Nachricht an diesen Reiter zu senden.  

In dieser Nachricht müssen Sie die URL zu dem Bild hinzufügen, das Sie anzeigen möchten, und Sie möchten eine eindeutige ID senden, die dem eingefügten Bild zugewiesen werden soll.  Sie können festlegen, dass die Inhalts Einfügung JavaScript generieren soll, aber aus Gründen, die später deutlich werden, generieren Sie diese eindeutige ID hier in `popup.js` und übergeben Sie an das noch nicht erstellte Inhalts Skript.  

Hier ist Ihre aktualisierte `popup/popup.js` Datei.  Übergeben Sie auch die aktuelle Tab-ID, die Sie in einem späteren Abschnitt benötigen, aber für jetzt, wird nicht verwendet.  

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

## So können Sie Ihre Stars. JPEG auf jeder Registerkarte des Browsers zur Verfügung stellen  

Sie Fragen sich wahrscheinlich, warum Sie die `images/stars.jpeg` `chrome.extension.getURL` Chrome-Erweiterungs-API verwenden müssen, anstatt einfach nur die relative URL ohne das zusätzliche Präfix zu übergeben, wie im vorherigen Abschnitt.  Übrigens sieht das zusätzliche Präfix, das `getUrl` mit dem angefügten Bild zurückgegeben wird, ungefähr wie folgt aus.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

Der Grund dafür ist, dass Sie das Bild mit dem `src` Attribut des `img` Elements in die Inhaltsseite einfügen.  Die Inhaltsseite wird in einem eindeutigen Thread ausgeführt, der nicht mit dem Thread identisch ist, auf dem die Erweiterung ausgeführt wird.  Sie müssen die statische Bilddatei als Web-Ressource verfügbar machen, damit Sie ordnungsgemäß funktioniert.  

Dazu müssen Sie einen weiteren Eintrag in der Datei hinzufügen `manifest.json` .  Sie müssen das Bild deklarieren, damit es über jede Registerkarte des Browsers zugänglich ist.  Dieser Eintrag sieht folgendermaßen aus: \ (Sie sollten ihn in der vollständigen `manifest.json` Datei unten sehen, wenn Sie die Inhalts Skript Deklaration hinzufügen).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Sie haben nun den Code in Ihre Datei geschrieben, `popup.js` um eine Nachricht an die Inhaltsseite zu senden, die auf der aktuellen aktiven Registerkarte eingebettet ist, aber Sie haben diese Inhaltsseite nicht erstellt und eingefügt.  Tun Sie das jetzt.  

## Aktualisieren Ihrer manifest.jsfür Inhalte und Web Access  

Das aktualisierte `manifest.json` , das das `content-scripts` und enthält, `web_accessible_resources` ist wie folgt.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
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

Der von Ihnen hinzugefügte Abschnitt ist `content_scripts` .  Das Attribut `matches` auf `<all_urls>` bedeutet, dass alle Dateien, die im Abschnitt " **content_scripts** " erwähnt werden, bei jedem Laden in alle Registerkarten des Browsers eingefügt werden.  Die zulässigen Dateitypen, die hier injiziert werden können, sind JavaScript und CSS.  Sie haben auch hinzugefügt `libjquery.min.js` .  Sie können diese aus dem oben im Abschnitt angegebenen Download aufnehmen.  

## Hinzufügen von jQuery und Grundlegendes zum zugehörigen Thread  

Planen Sie in den Inhalts Skripts, die Sie injizieren, die Verwendung von jQuery \ ( `$` \).  Sie haben eine minimierte-Version von jQuery hinzugefügt und in Ihr Erweiterungspaket als eingefügt `lib\jquery.min.js` .  Diese Inhalts Skripts werden in einer einzelnen Sandbox von Sortierungen ausgeführt, was bedeutet, dass die in die Seite eingefügte jQuery-Datei `popup.js` nicht für den Inhalt freigegeben wird.  

Beachten Sie, dass, selbst wenn auf der Registerkarte Browser auf der geladenen Webseite JavaScript ausgeführt wird, jeder eingefügte Inhalt keinen Zugriff darauf hat.  Das eingefügte JavaScript hat nur Zugriff auf das eigentliche Dom, das auf dieser Registerkarte des Browsers geladen wurde.  

## Hinzufügen des Inhalts Skript-Nachrichten Listeners  

Hier sehen `content-scripts\content.js` Sie die Datei, die auf jeder Registerkarte des Browsers basierend auf Ihrem Abschnitt eingefügt wird `manifest.json` `content-scripts` .  

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

Beachten Sie, dass das obige JavaScript die `listener` Verwendung der `chrome.runtime.onMessage.addListener` Erweiterungs-API-Methode registriert.  Dieser Listener wartet auf Nachrichten wie diejenige, die Sie von der `popup.js` zuvor beschriebenen mit der `chrome.tabs.sendMessage` Erweiterungs-API-Methode gesendet haben.  

Der erste Parameter der `addListener` Methode ist eine Funktion, deren erster Parameter Request die Details der übergebenen Nachricht ist.  Beachten Sie, `popup.js` dass die `sendMessage` Attribute des ersten Parameters, wenn Sie die Methode verwendet haben, `url` und sind `imageDivId` .  

Wenn ein Ereignis vom Listener verarbeitet wird, wird die Funktion, die der erste Parameter ist, ausgeführt.  Der erste Parameter dieser Funktion ist ein Objekt, das Attribute wie zugewiesen von besitzt `sendMessage` .  Diese Funktion verarbeitet einfach die drei jQuery-Skriptzeilen.  

*   Der erste fügt dynamisch in die DOM-Kopfzeile einen **\<style\>** Abschnitt ein, den Sie `slide-image` dem Element als Klasse zuweisen müssen `img` .  
*   Mit der zweiten wird ein `img` Element direkt unter der `body` Registerkarte Ihres Browsers angefügt, auf der die `slide-image` Klasse sowie die `imageDivId` ID des Bildelements zugewiesen ist.  
*   Das dritte fügt ein `click` Ereignis ein, das das gesamte Bild abdeckt, sodass der Benutzer eine beliebige Stelle im Bild auswählen kann, und dieses Bild wird von der Seite entfernt \ (zusammen mit dem Ereignis-Listener \).  

## Hinzufügen von Funktionen zum Entfernen des angezeigten Bilds bei Auswahl  

Wenn Sie nun zu einer beliebigen Seite navigieren und das Symbol für die **Erweiterung** auswählen, wird das Popupmenü wie folgt angezeigt:  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols":::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Wenn Sie die `Display` Schaltfläche auswählen, erhalten Sie die folgenden Elemente.  Wenn Sie eine beliebige Stelle im `stars.jpeg` Bild auswählen, wird das Bildelement entfernt, und die Registerkarten werden wieder auf die ursprüngliche Anzeige reduziert.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Das im Browser angezeigte Bild":::
   Das im Browser angezeigte Bild
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

Sie haben jetzt eine Erweiterung erstellt, mit der eine Nachricht vom Popup Symbol für das Erweiterungssymbol erfolgreich an das dynamisch eingefügte JavaScript gesendet wird, das als Inhalt auf der Registerkarte Browser ausgeführt wird.  Durch diesen eingefügten Inhalt wird das Image-Element so festgesetzt, dass die statischen Sterne JPEG angezeigt werden.  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Abgeschlossene Erweiterungspaket Quelle für diesen Teil | Microsoft docs"  
