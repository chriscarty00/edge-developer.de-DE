---
title: Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8eefea3fad894af6b66a6d7f595c5b663c03a0dc
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991190"
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







# Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools   



Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.  In diesem Leitfaden werden die einzelnen Typen von Haltepunkten erläutert, die in devtools zur Verfügung stehen, sowie Informationen dazu, wann und wie die einzelnen Typen festzulegen sind.  Eine praktische Einführung in den Debuggingprozess finden Sie unter [Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools][DevtoolsJavascriptIndex].  

## Übersicht über die Verwendung der einzelnen Haltepunkttypen   

Der bekannteste Breakpoint-Typ ist "Codezeile".  Es ist jedoch möglich, dass die festgelegten Code Haltepunkte nicht besonders effizient sind, wenn Sie nicht genau wissen, wo Sie suchen müssen, oder wenn Sie mit einer umfangreichen CodeBase arbeiten.  Sie können beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.  

| Breakpoint-Typ | Verwenden Sie diese Taste, wenn Sie anhalten möchten...  |  
|:--- |:--- |  
| [Codezeile](#line-of-code-breakpoints) | In einem exakten Codebereich.  |  
| [Bedingte Codezeile](#conditional-line-of-code-breakpoints) | In einem exakten Codebereich, aber nur, wenn eine andere Bedingung wahr ist.  |  
| [DOM](#dom-change-breakpoints) | Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die untergeordneten Elemente.  |  
| [XMLHttpRequest](#xhrfetch-breakpoints) | Wenn eine XMLHttpRequest-URL ein Zeichenfolgenmuster enthält.  |  
| [Ereignis-Listener](#event-listener-breakpoints) | Auf dem Code, der nach einem Ereignis ausgeführt wird, beispielsweise `click` , wird ausgeführt.  |  
| [Ausnahme](#exception-breakpoints) | In der Codezeile, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.  |  
| [Funktion](#function-breakpoints) | Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder Methode ausgeführt wird.  |  

## Haltepunkte für die Code Zeile   

Verwenden Sie einen Haltepunkt für die Codezeile, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.  DevTools wird immer angehalten, bevor diese Codezeile ausgeführt wird.  

So setzen Sie einen Code Haltepunkt in devtools:  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.  
1.  Wechseln Sie zur Codezeile.  
1.  Links neben der Codezeile befindet sich die Spalte "Zeile".  Klicken Sie darauf.  Neben der Spalte "Zeile Nummer" wird ein rotes Symbol angezeigt.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Ein Haltepunkt für eine Codezeile  
    :::image-end:::  
    
### Haltepunkte für die Code Zeile im Code   

Führen `debugger` Sie die Methode aus dem Code aus, um in dieser Zeile anzuhalten.  Dies entspricht einem [Zeile-zu-Code-Haltepunkt](#line-of-code-breakpoints), mit der Ausnahme, dass der Haltepunkt im Code festgesetzt wird, nicht auf der devtools-Benutzeroberfläche.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### Bedingte Zeile-für-Code-Haltepunkte   

Verwenden Sie einen bedingten Code Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber nur anhalten möchten, wenn eine andere Bedingung wahr ist.  

So setzen Sie einen bedingten Haltepunkt für eine bedingte Codezeile:  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.  
1.  Wechseln Sie zur Codezeile.  
1.  Links neben der Codezeile befindet sich die Spalte "Zeile".  Klicken Sie mit der rechten Maustaste auf die Leitungsnummer.  
1.  Wählen Sie **bedingter Haltepunkt hinzufügen**aus.  Unterhalb der Codezeile wird ein Dialogfeld angezeigt.  
1.  Geben Sie Ihre Bedingung in das Dialogfeld ein.  
1.  Drücken Sie `Enter` , um den Haltepunkt zu aktivieren.  Ein Symbol neben der Spalte "Zeile"  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Ein bedingter Zeile-Code-Haltepunkt" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Ein bedingter Zeile-Code-Haltepunkt  
    :::image-end:::  
    
### Verwalten von Code Haltepunkten   

Verwenden Sie den Bereich **Haltepunkte** , um Code Haltepunkte an einer einzelnen Position zu deaktivieren oder zu entfernen.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Der Haltepunkt-Panel" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Der **Haltepunkt** -Panel  
:::image-end:::  

*   Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.  
*   Klicken Sie mit der rechten Maustaste auf einen Eintrag, um diesen Haltepunkt zu entfernen.  
*   Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Haltepunkte** , um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.  Das Deaktivieren aller Haltepunkte entspricht der Deaktivierung der einzelnen Haltepunkte.  Durch die Deaktivierung aller Haltepunkte wird devtools angewiesen, alle Zeile-zu-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand beizubehalten, damit sich jeder in demselben Zustand wie zuvor befindet, wenn Sie ihn wieder aktivieren.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Deaktivierte Haltepunkte im Bereich "Haltepunkte"" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Deaktivierte Haltepunkte im Bereich " **Haltepunkte** "  
    :::image-end:::  
    
## Dom-Änderungs Haltepunkte   

Verwenden Sie einen Dom-Änderungs Haltepunkt, wenn Sie den Code anhalten möchten, durch den ein DOM-Knoten oder die untergeordneten Elemente geändert werden.  

So setzen Sie einen Dom-Änderungs Haltepunkt:  

1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Wechseln Sie zu dem Element, für das Sie den Haltepunkt festlegen möchten.  
1.  Klicken Sie mit der rechten Maustaste auf das Element.  
1.  Zeigen Sie **mit der Maus auf Umbruch**, und wählen Sie dann **Strukturänderungen**, **Attributänderungen**oder **Knoten Entfernung**aus.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts  
    :::image-end:::  
    
### Typen von Dom-Änderungs Haltepunkten   

*   Teil **Strukturänderungen**.  Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt oder der Inhalt eines untergeordneten Elements geändert wird.  Wird nicht für Änderungen an einem Attribut des untergeordneten Knotens oder für Änderungen am aktuell ausgewählten Knoten ausgelöst.  
*   Attribut **Änderungen**: wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.  
*   **Knoten Entfernung**: wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.  
    
## XMLHttpRequest/FETCH-Haltepunkte   

Verwenden Sie einen XMLHttpRequest-Haltepunkt, wenn Sie unterbrechen möchten, wenn die Anforderungs-URL eines XMLHttpRequest eine angegebene Zeichenfolge enthält.  DevTools wird in der Codezeile angehalten, in der die XMLHttpRequest die `send()` Methode ausführt.  

> [!NOTE]
> Dieses Feature funktioniert auch mit [Fetch-API-][MDNFetchApi] Anforderungen.  

Wenn dies hilfreich ist, können Sie beispielsweise feststellen, dass die Seite eine falsche URL anfordert, und Sie möchten schnell den AJAX-oder Fetch-Quellcode finden, der die falsche Anforderung verursacht.  

So setzen Sie einen XMLHttpRequest-Haltepunkt:  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Erweitern Sie den Bereich **XMLHttpRequest-Haltepunkte** .  
1.  Klicken Sie auf **Haltepunkt hinzufügen**.  
1.  Geben Sie die Zeichenfolge ein, die Sie aufheben möchten.  DevTools wird angehalten, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XMLHttpRequest-Anforderungs-URL vorhanden ist.  
1.  Drücken Sie `Enter` , um zu bestätigen.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Erstellen eines XMLHttpRequest-Haltepunkts" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Erstellen eines XMLHttpRequest-Haltepunkts  
    :::image-end:::  
    
## Ereignis-Listener-Haltepunkte 

Verwenden Sie Ereignis-Listener-Haltepunkte, wenn Sie den Ereignislistener-Code anhalten möchten, der nach dem Auslösen eines Ereignisses ausgeführt wird.  Sie können bestimmte Ereignisse, beispielsweise `click` oder Kategorien von Ereignissen, wie alle Mausereignisse auswählen.  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Erweitern Sie den Bereich **Ereignislistener-Haltepunkte** .  DevTools zeigt eine Liste der Ereigniskategorien, wie etwa **Animationen**, an.  
1.  Überprüfen Sie eine dieser Kategorien, um zu pausieren, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Erstellen eines Ereignis-Listener-Haltepunkts" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Erstellen eines Ereignis-Listener-Haltepunkts  
    :::image-end:::  
    
## Ausnahme Haltepunkte   

Verwenden Sie Ausnahme Haltepunkte, wenn Sie in der Codezeile anhalten möchten, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Klicken Sie auf **Ausnahmen anhalten** \ ( ![ bei Ausnahmen anhalten ][ImagePauseOnExceptionsIcon] \).  Das Symbol wird blau, wenn es aktiviert ist.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Schaltfläche "auf Ausnahmen pausieren"" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Schaltfläche " **auf Ausnahmen pausieren** "  
    :::image-end:::  
    
1.  **Optional**.  Aktivieren Sie das Kontrollkästchen **auf abgefangene Ausnahmen anhalten** , wenn Sie zusätzlich zu den nicht abgefangenen Ausnahmen auch auf abgefangene Ausnahmen anhalten möchten.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Bei einer nicht abgefangenen Ausnahme angehalten" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Bei einer nicht abgefangenen Ausnahme angehalten  
    :::image-end:::  
    
## Funktionshaltepunkte   

Führen Sie die Methode aus, `debug(method)` wobei `method` der Befehl, die Funktion oder die Methode, die Sie debuggen möchten, ist, wenn Sie anhalten möchten, wenn eine bestimmte Funktion ausgeführt wird.  Sie können `debug()` in Ihren Code einfügen (wie eine `console.log()` Anweisung) oder die Methode über die devtools-Konsole ausführen.  `debug()` entspricht dem Festlegen eines [Haltepunkts für die Code Zeile](#line-of-code-breakpoints) in der ersten Zeile der Funktion.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### Sicherstellen, dass sich die Zielfunktion im Bereich befindet   

DevTools löst a `ReferenceError` aus, wenn sich die zu debuggende Funktion nicht im Bereich befindet.  

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

Die Sicherstellung, dass die Zielfunktion im Bereich liegt, ist schwierig, wenn Sie die `debug()` Methode über die devtools-Konsole ausführen.  Hier ist eine Strategie:  

1.  Setzen Sie einen [Haltepunkt für die Codezeile](#line-of-code-breakpoints) an einer beliebigen Stelle, an der sich die Funktion im Bereich befindet.
1.  Auslösen des Haltepunkts  
1.  Führen `debug()` Sie die Methode in der devtools-Konsole aus, während der Code weiterhin auf dem Haltepunkt für die Code Zeile angehalten wird.  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "FETCH-API | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
