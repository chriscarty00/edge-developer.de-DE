---
description: Erfahren Sie mehr über alle Möglichkeiten, wie Sie Ihren Code in Microsoft Edge DevTools anhalten können.
title: So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 84077503d6c786244fc2ca4d54c349ae9f6d20d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398595"
---
<!-- Copyright Kayce Basques

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a>So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools an  

Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.  In diesem Handbuch werden die einzelnen Typen von Haltepunkten erläutert, die in DevTools verfügbar sind, sowie die Verwendung und das Festlegen der einzelnen Typen.  Ein praktisches Lernprogramm des Debugprozesses finden Sie unter Erste Schritte mit dem Debuggen von [JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].  

## <a name="overview-of-when-to-use-each-breakpoint-type"></a>Übersicht über die Verwendung der einzelnen Haltepunkttypen  

Der bekannteste Haltepunkttyp ist die Codezeile.  Aber codebasierte Haltepunkte können ineffizient festgelegt werden, insbesondere wenn Sie nicht genau wissen, wo sie aussehen sollen, oder wenn Sie mit einer großen Codebasis arbeiten.  Sie können sich beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.  

| Haltepunkttyp | Verwenden Sie dies, wenn Sie anhalten möchten...  |  
|:--- |:--- |  
| [Codezeile](#line-of-code-breakpoints) | Für einen genauen Codebereich.  |  
| [Bedingte Codezeile](#conditional-line-of-code-breakpoints) | Für einen genauen Codebereich, jedoch nur, wenn eine andere Bedingung true ist.  |  
| [DOM](#dom-change-breakpoints) | Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die unteren Knoten.  |  
| [XHR](#xhrfetch-breakpoints) | Wenn eine XHR-URL ein Zeichenfolgenmuster enthält.  |  
| [Ereignislistener](#event-listener-breakpoints) | Auf dem Code, der nach einem Ereignis ausgeführt wird, z. B. `click` , wird ausgeführt.  |  
| [Ausnahme](#exception-breakpoints) | In der Codezeile, die eine Ausnahme beim Abfangen oder Nichtfangen auslöst.  |  
| [Funktion](#function-breakpoints) | Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder methode ausgeführt wird.  |  

## <a name="line-of-code-breakpoints"></a>Zeilen-von-Code-Haltepunkte  

Verwenden Sie einen Codezeile-Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.  DevTools hält immer an, bevor diese Codezeile ausgeführt wird.  

So legen Sie einen Codezeile-Haltepunkt in DevTools ein:  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Öffnen Sie die Datei, die die Codezeile enthält, in der Sie die Datei umbrechen möchten.  
1.  Wechseln Sie zur Codezeile.  
1.  Links von der Codezeile befindet sich die Zeilennummerspalte.  Wählen Sie sie aus.  Neben der Zeilennummerspalte wird ein rotes Symbol angezeigt.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Codezeile-Haltepunkt" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Ein Codezeile-Haltepunkt  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a>Zeilen-von-Code-Haltepunkte in Ihrem Code  

Führen Sie `debugger` die -Methode aus Ihrem Code aus, um diese Zeile anzuhalten.  Dies entspricht einem [Zeilen-von-Code-Haltepunkt,](#line-of-code-breakpoints)mit der Ausnahme, dass der Haltepunkt in Ihrem Code festgelegt ist, nicht in der DevTools-Benutzeroberfläche.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a>Bedingte Zeilen-von-Code-Haltepunkte  

Verwenden Sie einen bedingten Zeilen-von-Code-Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber Sie möchten nur anhalten, wenn eine andere Bedingung wahr ist.  

So legen Sie einen bedingten Codelinien-Haltepunkt ein:  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Öffnen Sie die Datei, die die Codezeile enthält, in der Sie die Datei umbrechen möchten.  
1.  Wechseln Sie zur Codezeile.  
1.  Links von der Codezeile befindet sich die Zeilennummerspalte.  Zeigen Sie auf die Zeilennummer, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  
1.  Wählen **Sie Bedingten Haltepunkt hinzufügen aus.**  Unterhalb der Codezeile wird ein Dialogfeld angezeigt.  
1.  Geben Sie Ihre Bedingung in das Dialogfeld ein.  
1.  Wählen `Enter` Sie diese Option aus, um den Haltepunkt zu aktivieren.  Ein Symbol neben der Zeilennummerspalte.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Ein bedingter Zeilen-von-Code-Haltepunkt" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Ein bedingter Zeilen-von-Code-Haltepunkt  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a>Verwalten von Zeilen-von-Code-Haltepunkten  

Verwenden Sie **den Bereich Haltepunkte,** um Codelinien-Haltepunkte an einem einzigen Speicherort zu deaktivieren oder zu entfernen.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="The Breakpoints panel" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   The **Breakpoints** panel  
:::image-end:::  

*   Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.  
*   Zeigen Sie auf einen Eintrag, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), um diesen Haltepunkt zu entfernen.  
*   Zeigen Sie **** auf eine beliebige Stelle im Bereich Haltepunkte, und öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.  Das Deaktivieren aller Haltepunkte entspricht dem Deaktivieren der einzelnen Haltepunkte.  Durch das Deaktivieren aller Haltepunkte wird DevTools angewiesen, alle Zeilen-von-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand so zu verwalten, dass sich alle im gleichen Zustand befinden wie zuvor, wenn Sie die einzelnen Haltepunkte reaktivieren.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Deaktivierte Haltepunkte im Bereich Haltepunkte" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Deaktivierte Haltepunkte im **Bereich Haltepunkte**  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a>DOM-Änderungs-Haltepunkte  

Verwenden Sie einen DOM-Änderungsbruchpunkt, wenn Sie den Code anhalten möchten, der einen DOM-Knoten oder die unteren Knoten ändert.  

So legen Sie einen DOM-Änderungs-Haltepunkt ein:  

1.  Wählen Sie das **Elementtool** aus.  
1.  Wechseln Sie zum Element, für das Sie den Haltepunkt festlegen möchten.  
1.  Zeigen Sie auf das Element, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  
1.  Zeigen Sie **auf Unterbrechung auf**, und wählen Sie dann **Subtree-Änderungen,** **Attributänderungen**oder **Knotenentfernung aus.**  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Das Kontextmenü zum Erstellen eines DOM-Änderungs-Haltepunkts" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Das Kontextmenü zum Erstellen eines DOM-Änderungs-Haltepunkts  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a>Typen von DOM-Änderungs-Haltepunkten  

*   **Änderungen an der Unterstruktur**.  Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt wird oder der Inhalt eines untergeordneten Knotens geändert wird.  Wird nicht bei Änderungen des untergeordneten Knotenattributs oder bei Änderungen am aktuell ausgewählten Knoten ausgelöst.  
*   **Attributeänderungen:** Wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.  
*   **Knotenentfernung**: Wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.  
    
## <a name="xhrfetch-breakpoints"></a>XHR/Fetch-Haltepunkte  

Verwenden Sie einen XHR-Haltepunkt, wenn Sie den Wert ändern möchten, wenn die Anforderungs-URL einer XHR eine angegebene Zeichenfolge enthält.  DevTools hält in der Codezeile an, in der die XHR die Methode `send()` ausgeführt wird.  

> [!NOTE]
> Dieses Feature funktioniert auch mit [Fetch-API-Anforderungen.][MDNFetchApi]  

Ein Beispiel dafür, wann dies hilfreich ist, ist, wenn Ihre Webseite eine falsche URL anfordert und Sie schnell den AJAX- oder Fetch-Quellcode finden möchten, der die falsche Anforderung verursacht.  

So legen Sie einen XHR-Haltepunkt ein:  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Erweitern Sie **den XHR-Haltepunktbereich.**  
1.  Wählen **Sie Haltepunkt hinzufügen aus.**  
1.  Geben Sie die Zeichenfolge ein, die Sie umbrechen möchten.  DevTools hält an, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XHR-Anforderungs-URL vorhanden ist.  
1.  Wählen `Enter` Sie aus, um dies zu bestätigen.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Erstellen eines XHR-Haltepunkts" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Erstellen eines XHR-Haltepunkts  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a>Haltepunkte für Ereignislistener  

Verwenden Sie Ereignislistener-Haltepunkte, wenn Sie den Ereignislistenercode anhalten möchten, der nach dem Ausgelöst eines Ereignisses ausgeführt wird.  Sie können bestimmte Ereignisse auswählen, z. B. , oder Kategorien von Ereignissen, z. B. `click` alle Mausereignisse.  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Erweitern Sie **den Bereich Ereignislistener-Haltepunkte.**  DevTools zeigt eine Liste der Ereigniskategorien an, z. B. **Animation**.  
1.  Überprüfen Sie eine dieser Kategorien, um zu unterbrechen, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Erstellen eines Haltepunkts für Ereignislistener" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Erstellen eines Haltepunkts für Ereignislistener  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a>Ausnahme-Haltepunkte  

Verwenden Sie Ausnahme-Haltepunkte, wenn Sie die Codezeile anhalten möchten, die eine Ausnahme beim Abfangen oder Nichtfangen auslöst.  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Wählen **Sie Pause für Ausnahmen** \( Pause für Ausnahmen ![ ][ImagePauseOnExceptionsIcon] \).  Das Symbol wird blau, wenn es aktiviert ist.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Die Schaltfläche Für Ausnahmen anhalten" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Die **Schaltfläche Für Ausnahmen anhalten**  
    :::image-end:::  
    
1.  **Optional**.  Aktivieren Sie das Kontrollkästchen Bei **erwischten Ausnahmen** anhalten, wenn Sie zusätzlich zu nicht abgefangenen Ausnahmen auch bei abgefangenen Ausnahmen anhalten möchten.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Angehalten für eine nicht abgefangene Ausnahme" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Angehalten für eine nicht abgefangene Ausnahme  
    :::image-end:::  
    
## <a name="function-breakpoints"></a>Haltepunkte für Funktionen  

Führen Sie die -Methode aus, wobei der Befehl, die Funktion oder die Methode ist, die Sie debuggen möchten, wenn Sie anhalten möchten, wenn eine bestimmte `debug(method)` `method` Funktion ausgeführt wird.  Sie können in Ihren Code (wie eine Anweisung) einfügen oder die Methode über die `debug()` `console.log()` DevTools-Konsole ausführen.  `debug()` entspricht dem Festlegen eines [Codepunkts](#line-of-code-breakpoints) in der ersten Zeile der Funktion.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a>Sicherstellen, dass sich die Zielfunktion im Bereich befindet  

DevTools gibt eine `ReferenceError` aus, wenn sich die funktion, die Sie debuggen möchten, nicht im Bereich befindet.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Wenn Sie die Methode über die DevTools-Konsole ausführen, ist es schwierig sicherzustellen, dass sich die Zielfunktion im Bereich `debug()` befindet.  Hier ist eine Strategie:  

1.  Legen Sie [einen Codezeile-Haltepunkt](#line-of-code-breakpoints) an einer Stelle an, an der sich die Funktion im Bereich befindet.
1.  Lösen Sie den Haltepunkt aus.  
1.  Führen Sie die Methode in der DevTools-Konsole aus, während der Code weiterhin an Ihrem `debug()` Codezeile-Haltepunkt angehalten wird.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Abrufen von API-| MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
