---
description: Dynamisches Einfügen eines NASA-Bilds unter dem Seitentexttag mithilfe von Inhaltsskripts
title: Erstellen eines Erweiterungslernprogramms Teil 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge Chromium, Webentwicklung, html, css, javascript, Entwickler, Erweiterungen
ms.openlocfilehash: c5a17cbc55c6ccb42e06369474cd274d70742494
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579729"
---
# <a name="create-an-extension-tutorial-part-2"></a>Erstellen eines Erweiterungslernprogramms Teil 2  
  
[Quelle des abgeschlossenen Erweiterungspakets für diesen Teil][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a>Übersicht  

Dieses Lernprogramm behandelt die folgenden Erweiterungstechnologien.
*   Injizieren von JavaScript-Bibliotheken in erweiterung  
*   Verfügbar machen von Erweiterungsressourcen für Browserregisterkarten  
*   Hinzufügen von Inhaltsseiten in vorhandene Browserregisterkarten  
*   So können Inhaltsseiten auf Nachrichten von Popups lauschen und antworten  

Sie lernen, Ihr Popupmenü zu aktualisieren, um Ihr statisches Sternbild durch einen Titel und eine Standard-HTML-Schaltfläche zu ersetzen.  Diese Schaltfläche übergibt bei Auswahl dieses Sternbilds, das in die Erweiterung eingebettet ist, an die Inhaltsseite.  Dieses Bild wird in die Aktive Browserregisterkarte eingefügt. Führen Sie die folgenden Schritte aus, um weitere Informationen zu erhalten.

1.  Entfernen sie das Bild aus dem Popup, und ersetzen Sie es durch eine Schaltfläche.  

Aktualisieren Sie zunächst Ihre Datei mit einem geraden Markup, `popup.html` das einen Titel und eine Schaltfläche anzeigt.  Sie werden diese Schaltfläche in Kürze programmieren, aber vorerst nur einen Verweis auf eine leere JavaScript-Datei `popup.js` hinzufügen.  Hier ist Update-HTML.  

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

Nach dem Aktualisieren und Öffnen der Erweiterung wird ein Popup mit einer Anzeigeschaltfläche geöffnet.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach Auswahl des Erweiterungssymbols":::
   popup.html-Anzeige nach Auswahl des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  Updatestrategie zum Anzeigen des Bilds am oberen Rand der Browserregisterkarte  

Nach dem Hinzufügen der Schaltfläche besteht die nächste Aufgabe darin, die Bilddatei oben auf der aktiven `images/stars.jpeg` Registerkartenseite zu öffnen.  

Denken Sie daran, dass jede Registerkartenseite in einem eigenen Thread ausgeführt wird. Außerdem verwendet die Erweiterung einen anderen Thread.  Erstellen Sie zunächst ein Inhaltsskript, das in die Registerkartenseite eingejiziert wird.  Senden Sie dann eine Nachricht von Ihrem Popup an das Inhaltsskript, das auf der Registerkartenseite ausgeführt wird. Das Inhaltsskript empfängt die Nachricht, die beschreibt, welches Bild angezeigt werden soll.  

3. Erstellen des Popup-JavaScript zum Senden einer Nachricht  

Erstellen und fügen Sie zunächst Code hinzu, um eine Nachricht an Ihr noch nicht erstelltes Inhaltsskript zu senden, das Sie in der Zeit erstellen und in Ihre Browserregisterkarte ein- und `popup/popup.js` einwerfen müssen.  Dazu fügt der folgende Code der Popupanzeigeschaltfläche ein `onclick` Ereignis hinzu.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

Suchen Sie `onclick` in diesem Fall nach der aktuellen Browserregisterkarte.  Verwenden Sie dann die `chrome.tabs.sendmessage` Erweiterungs-API, um eine Nachricht an diese Registerkarte zu senden.  

In dieser Nachricht müssen Sie die URL zu dem Bild hinzufügen, das Sie anzeigen möchten. Senden Sie außerdem eine eindeutige ID, die dem eingefügten Bild zugewiesen werden soll.  Sie können dies durch den Inhaltseinfügungs-JavaScript generieren lassen, aber aus später ersichtlichen Gründen generieren Sie diese eindeutige ID hier in und übergeben sie an das noch nicht erstellte `popup.js` Inhaltsskript.  

Der folgende Codeausschnitt umreißt den aktualisierten Code in `popup/popup.js` .  Übergeben Sie außerdem die aktuelle Registerkarten-ID, die weiter später in diesem Artikel verwendet wird.  

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

4. Machen Sie "stars.jpeg" auf einer beliebigen Browserregisterkarte verfügbar  

Sie fragen sich wahrscheinlich, warum Sie, wenn Sie das Muss übergeben, die Chromerweiterungs-API verwenden, anstatt einfach die relative URL ohne das zusätzliche Präfix wie im vorherigen Abschnitt `images/stars.jpeg` `chrome.extension.getURL` zu übergeben.  Dieses zusätzliche Präfix, das mit dem angefügten Bild zurückgegeben wird, sieht im Vergleich dazu `getUrl` wie folgt aus.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

Der Grund dafür ist, dass Sie das Bild mithilfe des Attributs des Elements in die `src` `img` Inhaltsseite einjizieren.  Die Inhaltsseite wird in einem eindeutigen Thread ausgeführt, der nicht mit dem Thread identisch ist, in dem die Erweiterung ausgeführt wird.  Sie müssen die statische Bilddatei als Web-Ressource verfügbar machen, damit sie ordnungsgemäß funktioniert.  

Fügen Sie einen weiteren Eintrag in der Datei hinzu, um zu deklarieren, dass das Bild `manifest.json` für alle Browserregisterkarten verfügbar ist.  Dieser Eintrag lautet wie folgt \(Sie sollten ihn in der vollständigen Datei unten sehen, wenn Sie die Deklaration des Inhaltsskripts hinzufügen, die `manifest.json` angezeigt wird\).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Sie haben nun den Code in Ihre Datei geschrieben, um eine Nachricht an die Inhaltsseite zu senden, die auf der aktuellen aktiven Registerkartenseite eingebettet ist, aber Sie haben diese Inhaltsseite nicht erstellt und `popup.js` injiziert.  Machen Sie dies jetzt.  

5.  Aktualisieren der manifest.jsfür Inhalt und Webzugriff  

Die `manifest.json` aktualisierte, die das `content-scripts` und `web_accessible_resources` enthält, lautet wie folgt.  

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

Der hinzugefügte Abschnitt ist `content_scripts` .  Das Attribut ist auf festgelegt, was bedeutet, dass alle Dateien in alle Browserregisterkartenseiten injiziert werden, wenn jede Registerkarte `matches` `<all_urls>` geladen `content_scripts` wird.  Die zulässigen Dateitypen, die injiziert werden können, sind JavaScript und CSS.  Sie haben auch `libjquery.min.js` hinzugefügt.  Sie können dies aus dem oben im Abschnitt erwähnten Download enthalten.  

6. Hinzufügen von jQuery und Verstehen des zugeordneten Threads  

Planen Sie in den Inhaltsskripts, die Sie injizieren, die Verwendung von jQuery \( `$` \).  Sie haben eine minifizierte Version von jQuery hinzugefügt und in Das Erweiterungspaket als `lib\jquery.min.js` eingefügt.  Diese Inhaltsskripts werden in einzelnen Sandkasten ausgeführt, was bedeutet, dass die in die Seite eingejizierte jQuery nicht für `popup.js` den Inhalt freigegeben wird.  

Denken Sie daran, dass selbst wenn auf der Browserregisterkarte JavaScript auf der geladenen Webseite ausgeführt wird, alle injizierten Inhalte keinen Zugriff darauf haben.  Dieses injizierte JavaScript hat nur Zugriff auf das tatsächlich in dieser Browserregisterkarte geladene DOM.  

7. Hinzufügen des Inhaltsskriptnachrichtenlisteners  

Hier ist diese Datei, die basierend auf Ihrem Abschnitt in jede `content-scripts\content.js` Browserregisterkartenseite eingejiziert `manifest.json` `content-scripts` wird.  

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

Beachten Sie, dass alle oben genannten JavaScript-Funktionen die Registrierung einer mit `listener` der `chrome.runtime.onMessage.addListener` Extension-API-Methode sind.  Dieser Listener wartet auf Nachrichten wie die, die Sie von der zuvor mit der `popup.js` `chrome.tabs.sendMessage` Extension-API-Methode gesendet haben.  

Der erste Parameter der Methode ist eine Funktion, deren erster Parameter, request, die Details der Nachricht `addListener` ist, die übergeben wird.  Denken Sie daran, dass diese Attribute des ersten Parameters aus und sind, wenn Sie die -Methode `popup.js` `sendMessage` verwendet `url` `imageDivId` haben.  

Wenn ein Ereignis vom Listener verarbeitet wird, wird die Funktion ausgeführt, die der erste Parameter ist.  Der erste Parameter dieser Funktion ist ein Objekt, das Attribute wie von zugewiesen `sendMessage` hat.  Diese Funktion verarbeitet einfach die drei jQuery-Skriptzeilen.  

*   Die erste Skriptzeile fügt dynamisch in den DOM-Header einen Abschnitt ein, den Sie Ihrem Element als Klasse **\<style\>** `slide-image` zuweisen `img` müssen.  
*   Die zweite Skriptzeile fügt ein Element direkt unterhalb der Browserregisterkarte an, der die Klasse zugewiesen ist, sowie die `img` `body` ID dieses `slide-image` `imageDivId` Bildelements.  
*   In der dritten Skriptzeile wird ein Ereignis hinzugefügt, das das gesamte Bild umfasst, sodass der Benutzer eine beliebige Stelle im Bild auswählen kann und dieses Bild von der Seite \(zusammen mit dem Ereignislistener\) entfernt `click` wird.  

8. Hinzufügen von Funktionen zum Entfernen des angezeigten Bilds bei Auswahl  

Wenn Sie nun zu einer beliebigen Seite navigieren und ihr Erweiterungssymbol **auswählen,** wird das Popupmenü wie folgt angezeigt.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach Auswahl des Erweiterungssymbols":::
   popup.html-Anzeige nach Auswahl des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

Wenn Sie die Schaltfläche `Display` auswählen, erhalten Sie die unten aufgeführten Informationen.  Wenn Sie eine beliebige Stelle im Bild auswählen, wird dieses Bildelement entfernt, und Registerkartenseiten werden wieder auf das reduziert, `stars.jpeg` was ursprünglich angezeigt wurde.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Das im Browser angezeigte Bild":::
   Das im Browser angezeigte Bild
:::image-end:::

Sie haben eine Erweiterung erstellt, die erfolgreich eine Nachricht aus dem Popup des Erweiterungssymbols sendet und dynamisch JavaScript eingefügt hat, das als Inhalt auf der Registerkarte Browser ausgeführt wird.  Der injizierte Inhalt legt das Bildelement fest, um Ihre statischen Sterne jpeg anzuzeigen.  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Abgeschlossene Erweiterungspaketquelle | Microsoft Docs"  
