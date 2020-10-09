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
# Erstellen eines Erweiterungs Lernprogramms, Teil 2  
  
[Abgeschlossene Erweiterungspaket Quelle für diesen Teil][ArchiveExtensionGettingStartedPart2]    

## Übersicht  

Dieses Lernprogramm umfasst die folgenden Erweiterungstechnologien.
*   Einfügen von JavaScript-Bibliotheken in die Erweiterung  
*   Verfügbar machen von Erweiterungs Ressourcen für browserregisterkarten  
*   Einschließen von Inhaltsseiten in vorhandene browserregisterkarten  
*   Wenn Inhaltsseiten auf Nachrichten von Popups abhören und Antworten  

Sie erfahren, wie Sie das Popupmenü aktualisieren können, um Ihr statisches Start Bild durch einen Titel und eine standardmäßige HTML-Schaltfläche zu ersetzen.  Wenn diese Schaltfläche ausgewählt ist, wird das in der Erweiterung eingebettete Sternchen-Bild an die Inhaltsseite weitergeleitet.  Das Bild wird in die Registerkarte aktiver Browser eingefügt. Führen Sie die folgenden Schritte aus, um weitere Informationen zu erhalten.

1.  Entfernen des Bilds aus dem Popup und ersetzen durch eine Schaltfläche  

Aktualisieren Sie zunächst die `popup.html` Datei mit einem geraden Markup, in dem ein Titel und eine Schaltfläche angezeigt werden.  Sie programmieren die Schaltfläche in Kürze, aber im Moment fügen Sie einfach einen Verweis auf eine leere JavaScript-Datei hinzu `popup.js` .  Hier ist Update HTML.  

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

Nach dem Aktualisieren und Öffnen der Erweiterung wird ein Popup mit einer Anzeige Schaltfläche geöffnet.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols&quot;:::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  Update Strategie zum Anzeigen des Bilds oben auf der Registerkarte &quot;Browser"  

Nachdem Sie die Schaltfläche hinzugefügt haben, besteht die nächste Aufgabe darin, die Bilddatei oben auf der `images/stars.jpeg` aktiven Registerkarte anzuzeigen.  

Beachten Sie, dass jede Registerkarte in einem eigenen Thread ausgeführt wird. Außerdem verwendet die Erweiterung einen anderen Thread.  Erstellen Sie zunächst ein Inhalts Skript, das in die Registerkartenseite eingefügt wird.  Senden Sie dann eine Nachricht vom Popup an das Inhalts Skript, das auf der Registerkartenseite ausgeführt wird. Das Inhalts Skript empfängt die Nachricht, die beschreibt, welches Bild angezeigt werden soll.  

3. Erstellen des Popup-Javascripts zum Senden einer Nachricht  

Erstellen Sie zunächst `popup/popup.js` Code, um eine Nachricht an ihr noch nicht erstelltes Inhalts Skript zu senden, das Sie im Moment erstellen und in Ihre Browserregister Karte einfügen müssen.  Dazu fügt der folgende Code der `onclick` Popup Anzeige Schaltfläche ein Ereignis hinzu.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

`onclick`Suchen Sie im Ereignis die aktuelle Browserregister Karte.  Verwenden Sie dann die `chrome.tabs.sendmessage` Erweiterungs-API, um eine Nachricht an diesen Reiter zu senden.  

In dieser Nachricht müssen Sie die URL zu dem Bild hinzufügen, das Sie anzeigen möchten. Senden Sie außerdem eine eindeutige ID, die dem eingefügten Bild zugewiesen werden soll.  Sie können festlegen, dass die Inhalts Einfügung JavaScript generieren soll, aber aus Gründen, die später deutlich werden, generieren Sie diese eindeutige ID hier in `popup.js` und übergeben Sie an das noch nicht erstellte Inhalts Skript.  

Der folgende Codeausschnitt beschreibt den aktualisierten Code in `popup/popup.js` .  Übergeben Sie auch die aktuelle Tab-ID, die später in diesem Artikel verwendet wird.  

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

4. Stellen Sie Ihre Stars. JPEG über eine beliebige Browser-Registerkarte zur Verfügung.  

Sie Fragen sich wahrscheinlich, warum Sie die `images/stars.jpeg` `chrome.extension.getURL` Chrome-Erweiterungs-API verwenden müssen, anstatt einfach nur die relative URL ohne das zusätzliche Präfix zu übergeben, wie im vorherigen Abschnitt.  Übrigens sieht das zusätzliche Präfix, das `getUrl` mit dem angefügten Bild zurückgegeben wird, ungefähr wie folgt aus.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

Der Grund dafür ist, dass Sie das Bild mit dem `src` Attribut des `img` Elements in die Inhaltsseite einfügen.  Die Inhaltsseite wird in einem eindeutigen Thread ausgeführt, der nicht mit dem Thread identisch ist, auf dem die Erweiterung ausgeführt wird.  Sie müssen die statische Bilddatei als Web-Ressource verfügbar machen, damit Sie ordnungsgemäß funktioniert.  

Fügen Sie einen weiteren Eintrag in der `manifest.json` Datei hinzu, um zu deklarieren, dass das Bild für alle browserregisterkarten verfügbar ist.  Dieser Eintrag sieht folgendermaßen aus: \ (Sie sollten ihn in der vollständigen `manifest.json` Datei unten sehen, wenn Sie die Inhalts Skript Deklaration hinzufügen).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Sie haben jetzt den Code in Ihre Datei geschrieben, `popup.js` um eine Nachricht an die Inhaltsseite zu senden, die auf der aktuellen aktiven Registerkarte eingebettet ist, aber Sie haben diese Inhaltsseite nicht erstellt und injiziert.  Tun Sie das jetzt.  

5.  Aktualisieren Ihrer manifest.jsfür Inhalte und Web Access  

Das aktualisierte `manifest.json` , das das `content-scripts` und enthält, `web_accessible_resources` ist wie folgt.  

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

Der von Ihnen hinzugefügte Abschnitt ist `content_scripts` .  Das `matches` Attribut ist auf festzulegen `<all_urls>` , was bedeutet, dass alle Dateien in `content_scripts` alle Registerkarten des Browsers eingefügt werden, wenn die einzelnen Registerkarten geladen werden.  Die zulässigen Dateitypen, die injiziert werden können, sind JavaScript und CSS.  Sie haben auch hinzugefügt `libjquery.min.js` .  Sie können dies aus dem oben im Abschnitt genannten Download aufnehmen.  

6. Hinzufügen von jQuery und Grundlegendes zum zugehörigen Thread  

Planen Sie in den Inhalts Skripts, die Sie injizieren, die Verwendung von jQuery \ ( `$` \).  Sie haben eine minimierte-Version von jQuery hinzugefügt und in Ihr Erweiterungspaket als eingefügt `lib\jquery.min.js` .  Diese Inhalts Skripts werden in einzelnen Sandboxes ausgeführt, was bedeutet, dass die in die Seite eingefügten jQuery-Dateien `popup.js` nicht für den Inhalt freigegeben werden.  

Beachten Sie, dass, selbst wenn auf der Registerkarte Browser auf der geladenen Webseite JavaScript ausgeführt wird, jeder eingefügte Inhalt keinen Zugriff darauf hat.  Das eingefügte JavaScript hat nur Zugriff auf das eigentliche Dom, das auf dieser Registerkarte des Browsers geladen wurde.  

7. Hinzufügen des Inhalts Skript-Nachrichten Listeners  

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

*   Die erste Skript Zeile fügt dynamisch in die DOM-Kopfzeile einen **\<style\>** Abschnitt ein, den Sie `slide-image` dem Element als Klasse zuweisen müssen `img` .  
*   Die zweite Skript Zeile fügt ein `img` Element direkt unter der `body` Registerkarte Ihres Browsers an, auf der die `slide-image` Klasse sowie die `imageDivId` ID des Bildelements zugewiesen ist.  
*   In der dritten Skript Zeile wird ein `click` Ereignis mit dem gesamten Bild hinzugefügt, das es dem Benutzer ermöglicht, eine beliebige Stelle im Bild auszuwählen, und dieses Bild wird von der Seite entfernt \ (zusammen mit dem Ereignis-Listener \).  

8. Hinzufügen von Funktionen zum Entfernen des angezeigten Bilds bei Auswahl  

Wenn Sie nun zu einer beliebigen Seite navigieren und das Symbol für die **Erweiterung** auswählen, wird das Popupmenü wie folgt angezeigt:  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols&quot;:::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  Update Strategie zum Anzeigen des Bilds oben auf der Registerkarte &quot;Browser":::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Wenn Sie die `Display` Schaltfläche auswählen, erhalten Sie die folgenden Elemente.  Wenn Sie eine beliebige Stelle im `stars.jpeg` Bild auswählen, wird das Bildelement entfernt, und die Registerkarten werden wieder auf die ursprüngliche Anzeige reduziert.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="popup.html-Anzeige nach dem Drücken des Erweiterungssymbols&quot;:::
   popup.html-Anzeige nach dem Drücken des Erweiterungssymbols
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  Update Strategie zum Anzeigen des Bilds oben auf der Registerkarte &quot;Browser"  
