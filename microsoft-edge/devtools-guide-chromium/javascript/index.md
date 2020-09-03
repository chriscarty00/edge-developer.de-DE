---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um JavaScript-Fehler zu finden und zu beheben.
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: f8846388f92ba330940b4b6842964d96d9bbce4d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993394"
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







# Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools   



In diesem Lernprogramm lernen Sie den grundlegenden Workflow zum Debuggen von JavaScript-Problemen in devtools.  

## Schritt 1: reproduzieren des Fehlers   

Das Suchen nach einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt zum Debuggen.  

1.  Klicken Sie auf **Demo öffnen**.  Halten Sie `Control` \ (Windows \) oder `Command` \ (macOS \) gedrückt, und öffnen Sie die Demo auf einer neuen Registerkarte.  
    
    [Demo öffnen][OpenDebugJSDemo]  
    
1.  Geben Sie `5` den Text in das Textfeld **Zahl 1** ein.  
1.  Geben Sie `1` den Text in das Textfeld **Zahl 2** ein.  
1.  Klicken Sie auf **Add Number 1 und Number 2**.  Die Beschriftung unter der Schaltfläche steht `5 + 1 = 51` .  Das Ergebnis sollte sein `6` .  Dies ist der Fehler, den Sie beheben werden.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="Das Ergebnis von 5 + 1 ist 51, sollte aber 6 sein." lightbox="../media/javascript-js-demo-bad.msft.png":::
       Das Ergebnis `5 + 1` ist `51` `6`  
    :::image-end:::  
    
## Schritt 2: Kennenlernen der Benutzeroberfläche des Quellbereichs   

DevTools bietet eine Vielzahl unterschiedlicher Tools für verschiedene Aufgaben, wie beispielsweise das Ändern von CSS, die Leistung der Profilerstellung für Seiten und das Überwachen von Netzwerkanforderungen.  Im **Quellen** Bereich können Sie JavaScript Debuggen.  

1.  Öffnen Sie devtools, indem Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) drücken.  Mit dieser Tastenkombination wird die **Konsolen** Leiste geöffnet.  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/javascript-console-empty.msft.png":::
       Die **Konsolen** Leiste  
    :::image-end:::  
    
1.  Klicken Sie auf die Registerkarte **Quellen** .  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Das Quellen Panel" lightbox="../media/javascript-sources-sections.msft.png":::
       Das **Quellen** Panel  
    :::image-end:::  
    
Die Benutzeroberfläche des **Quellen** Panels besteht aus drei Teilen.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Die drei Teile der Benutzeroberfläche des Quellen Panels" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Die drei Teile der Benutzeroberfläche des **Quellen** Panels  
:::image-end:::  

1.  Der Bereich " **Datei-Navigator** " \ (Abschnitt 1 in der vorhergehenden Abbildung \).  Jede Datei, die die Seite anfordert, wird hier aufgelistet.  
1.  Der Bereich " **Code-Editor** " \ (Abschnitt 2 in der vorhergehenden Abbildung \).  Nachdem Sie eine Datei im Bereich " **Datei-Navigator** " ausgewählt haben, wird hier der Inhalt der Datei angezeigt.  
1.  Der **JavaScript-Debugbereich** \ (in der vorherigen Abbildung Abschnitt 3).  Verschiedene Tools zum Überprüfen des Javascripts für die Seite.  Wenn Ihr devtools-Fenster breit ist, wird dieser Bereich rechts neben dem **Code-Editor-** Bereich angezeigt.  
    
## Schritt 3: Anhalten des Codes mit einem Haltepunkt   

Eine gängige Methode zum Debuggen eines Problems wie dieses besteht darin, viele `console.log()` Anweisungen in den Code einzufügen, um Werte während der Ausführung des Skripts zu überprüfen.  Zum Beispiel:  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

Die `console.log()` Methode erhält möglicherweise die Aufgabe erledigt, aber **Haltepunkte** können Sie schneller erledigen.  Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.  Haltepunkte weisen gegenüber der Methode einige Vorteile auf `console.log()` :  

*   Mit `console.log()` müssen Sie den Quellcode manuell öffnen, den relevanten Code suchen, die Anweisungen einfügen und die `console.log()` Seite dann erneut laden, um die Nachrichten in der Konsole anzuzeigen.  Mit Haltepunkten können Sie den relevanten Code anhalten, ohne zu wissen, wie der Code strukturiert ist.  
*   In Ihren `console.log()` Anweisungen müssen Sie jeden Wert, den Sie überprüfen möchten, explizit angeben.  Mit Haltepunkten zeigt devtools die Werte aller Variablen zu diesem Zeitpunkt an.  Manchmal gibt es Variablen, die Ihren Code beeinflussen, den Sie nicht einmal kennen.  

Kurz gesagt: Haltepunkte können Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.  

Wenn Sie einen Schritt zurückgehen und darüber nachdenken, wie die APP funktioniert, können Sie eine fundierte Vermutung anstellen, dass die falsche Summe ( `5 + 1 = 51` ) im `click` Ereignislistener berechnet wird, der der Schaltfläche " **Zahl 1" und "Zahl 2** " zugeordnet ist.  Daher möchten Sie den Code wahrscheinlich um die Zeit anhalten, zu der der `click` Listener ausgeführt wird.  Mit **Ereignis-Listener-Haltepunkten** können Sie genau das ausführen:  

1.  Klicken Sie im Bereich **JavaScript-Debuggen** auf **Ereignislistener-Haltepunkte** , um den Abschnitt zu erweitern.  DevTools zeigt eine Liste erweiterbarer Ereigniskategorien wie **Animation** und **Zwischenablage**an.  
1.  Klicken Sie neben der **Maus** Ereigniskategorie auf **erweitern** \ ( ![ Symbol erweitern ][ImageExpandIcon] \).  DevTools zeigt eine Liste von Mausereignissen wie **Click** und **MouseDown**an.  Neben jedem Ereignis ist ein Kontrollkästchen markiert.  
1.  Aktivieren Sie das Kontrollkästchen **Klicken** .  DevTools ist jetzt so eingerichtet, dass automatisch angehalten wird, wenn *ein* `click` Ereignis-Listener ausgeführt wird.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Das Kontrollkästchen "klicken" ist aktiviert." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Das Kontrollkästchen **"klicken"** ist aktiviert.  
    :::image-end:::  
    
1.  Klicken Sie wieder auf die Demo und dann erneut auf **Nummer 1 und 2** .  DevTools hält die Demo an und hebt eine Codezeile im **Quellen** Panel hervor.  DevTools sollte auf Zeile 16 anhalten `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Wenn Sie in einer anderen Codezeile pausieren, drücken Sie die Fortsetzung der **Skriptausführung** \ ( ![ Fortsetzen der Skriptausführung ][ImageResumeIcon] \), bis Sie die richtige Zeile anhalten.  
    
    > [!NOTE]
    > Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browser Erweiterung, die einen `click` Ereignis-Listener auf jeder besuchten Seite registriert.  Sie wurden im `click` Listener der Erweiterung angehalten.  Wenn Sie den InPrivate-Modus verwenden, um **private zu durchsuchen**, wodurch alle Erweiterungen deaktiviert werden, sehen Sie möglicherweise, dass Sie jedes Mal in der gewünschten Codezeile anhalten.  

<!--todo: add inprivate section when available -->  

**Ereignis-Listener-Haltepunkte** sind nur eine von vielen Arten von Haltepunkten, die in devtools verfügbar sind.  Es lohnt sich, alle unterschiedlichen Typen zu merken, denn jeder Typ hilft Ihnen letztendlich dabei, verschiedene Szenarien so schnell wie möglich zu debuggen.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Schritt 4: Durchlaufen des Codes   

Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.  Wenn Sie den Code schrittweise durchlaufen, können Sie die Laufzeit des Codes, jeweils eine Zeile, durchlaufen und genau ermitteln, wo er in einer anderen Reihenfolge als erwartet ausgeführt wird.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf **Schritt über den nächsten Funktionsaufruf** \ ( ![ Schritt zum nächsten Funktionsaufruf ][ImageOverIcon] \).  DevTools führt den folgenden Code aus, ohne ihn zu betreten.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools überspringt einige Codezeilen.  Dies liegt daran `inputsAreEmpty()` , dass die Auswertung als falsch ausgewertet wird, damit der Codeblock für die `if` Anweisung nicht ausgeführt wird.  
    
1.  Klicken Sie im **Quellen** Panel von devtools auf **Schritt in nächster Funktionsaufruf** \ ( ![ Schritt in nächster Funktionsaufruf ][ImageIntoIcon] \), um die Laufzeit der Funktion um `updateLabel()` jeweils eine Zeile zu durchlaufen.  
    
Das ist die grundlegende Idee, Code zu durchlaufen.  Wenn Sie sich den Code in ansehen `get-started.js` , sehen Sie, dass der Fehler wahrscheinlich irgendwo in der `updateLabel()` Funktion enthalten ist.  Anstatt jede Codezeile zu durchlaufen, können Sie eine andere Art von Haltepunkt verwenden, um den Code näher an der wahrscheinlichen Position des Fehlers anzuhalten.  

## Schritt 5: Festlegen eines Haltepunkts für die Code Zeile   

Die am häufigsten verwendeten Haltepunkte sind die Code Haltepunkte.  Wenn Sie die spezifische Codezeile erhalten, die Sie anhalten möchten, verwenden Sie einen Haltepunkt für die Code Zeile:  

1.  Sehen Sie sich die letzte Codezeile in an `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  Auf der linken Seite des Codes sehen Sie die Nummer der Zeile dieser bestimmten Codezeile, die **33**ist.  Klicken Sie auf **33**.  DevTools platziert ein rotes Symbol links von **33**.  Dies bedeutet, dass in dieser Zeile ein Haltepunkt für eine Codezeile vorhanden ist.  DevTools wird nun immer angehalten, bevor diese Codezeile ausgeführt wird.  
1.  Klicken Sie auf **Skriptausführung fortsetzen** \ ( ![ Skriptausführung fortsetzen ][ImageResumeIcon] \).  Das Skript wird weiterhin ausgeführt, bis es die Zeile 33 erreicht hat.  In den Zeilen 30, 31 und 32 druckt devtools die Werte von `addend1` , `addend2` und `sum` rechts neben dem Semikolon auf jeder Zeile aus.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools hält auf dem Zeile-zu-Code-Haltepunkt in Zeile 32" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools hält auf dem Zeile-zu-Code-Haltepunkt in Zeile 32  
    :::image-end:::  
    
## Schritt 6: Überprüfen von Variablenwerten   

Die Werte von `addend1` , `addend2` und `sum` verdächtig aussehen.  Sie werden in Anführungszeichen eingeschlossen, was bedeutet, dass es sich um Zeichenfolgen handelt.  Dies ist eine gute Hypothese, in der die Ursache des Fehlers erläutert wird.  Jetzt ist es an der Zeit, weitere Informationen zu sammeln.  DevTools bietet eine Vielzahl von Tools für die Untersuchung von Variablenwerten.  

### Methode 1: Bereichs Bereich   

Wenn Sie in einer Codezeile anhalten, zeigt der **Bereich** Bereich an, welche lokalen und globalen Variablen aktuell definiert sind, zusammen mit dem Wert der einzelnen Variablen.  Darüber hinaus werden ggf. Schließ Variablen angezeigt.  Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.  Wenn Sie nicht in einer Codezeile angehalten werden, ist der **Bereich** Bereich leer.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Bereichs Bereich" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   **Bereichs** Bereich  
:::image-end:::  

### Methode 2: Überwachen von Ausdrücken   

Auf der Registerkarte " **Überwachungsausdrücke** " können Sie die Werte von Variablen über einen Zeitraum überwachen.  Wie der Name schon sagt, sind Watch-Ausdrücke nicht nur auf Variablen limitiert.  Sie können jeden gültigen JavaScript-Ausdruck in einem Überwachungsausdruck speichern.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf die Registerkarte über **Wachen** .  
1.  Klicken Sie auf **Ausdruck hinzufügen** \ ( ![ Ausdruck hinzufügen ][ImageAddIcon] \).  
1.  Geben Sie `typeof sum` ein.  
1.  Drücken Sie `Enter` .  DevTools wird angezeigt `typeof sum: "string"` .  Der Wert rechts neben dem Doppelpunkt ist das Ergebnis des Überwachungsausdrucks.  
    
> [!NOTE]
> Im Bereich "Überwachungsausdruck" \ (unten rechts) in der folgenden Abbildung `typeof sum` wird der Überwachungsausdruck angezeigt.  Wenn Ihr devtools-Fenster groß ist, befindet sich der Bereich "Überwachungsausdruck" auf der rechten Seite oberhalb des Bereichs " **Ereignis-Listener-Haltepunkte** ".  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Der Bereich "Überwachungsausdruck"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Der Bereich " **Überwachungsausdruck** "  
:::image-end:::  

Wie vermutet, `sum` wird als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.  Sie haben nun bestätigt, dass dies die Ursache des Fehlers ist.  

### Methode 3: die Konsole   

Neben der Anzeige von `console.log()` Nachrichten können Sie auch die Konsole verwenden, um willkürliche JavaScript-Anweisungen auszuwerten.  Im Hinblick auf das Debuggen können Sie die Konsole verwenden, um mögliche Fehlerkorrekturen zu testen.  Probieren Sie es jetzt aus:  

1.  Wenn das Konsolen Fach nicht geöffnet ist, drücken Sie, `Escape` um es zu öffnen.  Sie wird unten im devtools-Fenster geöffnet.  
1.  Geben Sie in der Konsole `parseInt(addend1) + parseInt(addend2)` .  Diese Anweisung funktioniert, weil Sie in einer Codezeile angehalten werden `addend1` und `addend2` sich im Bereich befinden.  
1.  Drücken Sie `Enter` .  DevTools wertet die Anweisung aus und gibt das `6` Ergebnis aus, das Sie erwarten, dass die Demo erstellt wird.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Der Konsolen Einzug nach der Auswertung von parseInt (addend1) + parseInt (addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       Der **Konsolen** Einzug nach der Auswertung `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Schritt 7: Anwenden einer Korrektur   

Wenn Sie eine Lösung für den Fehler gefunden haben, versuchen Sie, Ihr Problem zu beheben, indem Sie den Code bearbeiten und die Demo erneut ausführen.  Sie müssen devtools nicht mehr belassen, um den Fix anzuwenden.  Sie können JavaScript-Code direkt in der devtools-Benutzeroberfläche bearbeiten.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf **Skriptausführung fortsetzen** \ ( ![ Skriptausführung fortsetzen ][ImageResumeIcon] \).  
1.  Ersetzen Sie im **Code-Editor**Zeile 32, `var sum = addend1 + addend2` mit `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.  
1.  Klicken Sie auf **Haltepunkte deaktivieren** \ ( ![ Haltepunkte deaktivieren ][ImageDeactivateIcon] \).  Es wechselt blau, um anzuzeigen, dass es aktiv ist.  Während dies eingestellt ist, ignoriert devtools alle von Ihnen gesetzten Haltepunkte.  
1.  Probieren Sie die Demo mit unterschiedlichen Werten aus.  Die Demo wird nun korrekt berechnet.  
    
> [!CAUTION]
> Dieser Workflow wendet nur einen Fix auf den Code an, der im Browser ausgeführt wird.  Der Code für alle Benutzer, die Ihre Seite besuchen, wird dadurch nicht behoben.  Dazu müssen Sie den Code korrigieren, der sich auf Ihren Servern befindet.  

## Nächste Schritte   

Herzlichen Glückwunsch!  Sie wissen jetzt, wie Sie Microsoft Edge devtools beim Debuggen von JavaScript optimal nutzen können.  Die Tools und Methoden, die Sie in diesem Lernprogramm gelernt haben, können Ihnen unzählige Stunden sparen.  

In diesem Lernprogramm wurden nur zwei Möglichkeiten zum Festlegen von Haltepunkten gezeigt.  DevTools bietet viele weitere Möglichkeiten, einschließlich der folgenden Einstellungen.  

*   Bedingte Haltepunkte, die nur ausgelöst werden, wenn die von Ihnen bereitgestellte Bedingung wahr ist.  
*   Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen  
*   XMLHttpRequest-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen bereitgestellten Teilzeichenfolge entspricht.  
    
Weitere Informationen dazu, wann und wie Sie die einzelnen Typen verwenden, finden Sie unter [Anhalten des Codes mit Haltepunkten][DevtoolsJavscriptBreakpoints].  

Es gibt ein paar Code-Stepping-Steuerelemente, die in diesem Lernprogramm nicht erläutert wurden.  Weitere Informationen finden Sie unter Schritt-für- [Zeile-Code][DevtoolsJavascriptReferenceStepThroughCode].  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools | Microsoft docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Schritt-für-Schritt-Code – JavaScript-Debug-Referenz | Microsoft docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demo öffnen | Glitch"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
