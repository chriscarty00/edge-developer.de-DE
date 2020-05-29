---
title: JavaScript-Debug-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581740"
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







# JavaScript-Debug-Referenz   



Entdecken Sie neue Debugging-Workflows mit dieser umfassenden Referenz zu den Microsoft Edge DevTools-Debugging-Features.  

Informationen zu den Grundlagen des Debuggens finden Sie unter [Erste Schritte beim Debuggen von JavaScript in Microsoft Edge devtools][DevToolsJavascriptGetStarted] .  

## Anhalten von Code mit Haltepunkten   

Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.  

Informationen zum Festlegen von Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints] .  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  

## Schritt-für-Schritt-Code   

Nachdem der Code angehalten wurde, führen Sie ihn schrittweise durch, und untersuchen Sie die Fluss-und Eigenschaftswerte auf dem Weg.  

### Schritt über Codezeile   

Wenn Sie in einer Codezeile mit einer Funktion angehalten wurden, die für das Problem, das Sie Debuggen, nicht relevant ist, klicken Sie auf das Symbol **Schritt** überschritt, ![ ][ImageStepOverIcon] um die Funktion auszuführen, ohne Sie zu betreten.  

> ##### Abbildung1  
> Auswählen des **Schritts**  
> ![Auswählen des Schritts][ImageSelectingStepOver]  

Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Sie sind angehalten `A` .  Wenn Sie den **Schritt über**drücken, führt devtools den gesamten Code in der Funktion aus, die Sie überschreiten, also `B` und `C` .  DevTools wird dann angehalten `D` .  

### Schritt in Codezeile   

Wenn Sie in einer Codezeile mit einem Funktionsaufruf angehalten haben, der sich auf das Problem bezieht, das Sie Debuggen, klicken Sie auf das Symbol **Schritt** in ![ Schritt, ][ImageStepIntoIcon] um diese Funktion weiter zu untersuchen.  

> ##### Abbildung2  
> Auswählen von **Schritt in**  
> ![Auswählen von Schritt in][ImageSelectingStepInto]  

Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Sie sind angehalten `A` .  Durch Drücken von **Schritt in**führt devtools diese Codezeile aus und hält dann an `B` .  

### Schritt außerhalb der Codezeile   

Wenn Sie innerhalb einer Funktion angehalten haben, die nicht mit dem Problem in Verbindung steht, das Sie Debuggen, klicken Sie auf das Symbol " **Schritt** aus", ![ ][ImageStepOutIcon] um den restlichen Code der Funktion auszuführen.  

> ##### Abbildung 3  
> Auswählen **von "Schritt aus** "  
> ![Auswählen von "Schritt aus"][ImageSelectingStepOut]  

Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Sie sind angehalten `A` .  Durch Drücken von **Step out**führt devtools den restlichen Code in aus `getName()` , der sich nur `B` in diesem Beispiel befindet, und hält dann an `C` .  

### Ausführen des gesamten Codes bis zu einer bestimmten Zeile   

Wenn Sie eine Long-Funktion Debuggen, gibt es möglicherweise viel Code, der sich nicht auf das zu debuggende Problem bezieht.  

Sie können alle Zeilen durchlaufen, aber das ist mühsam.  Sie können festlegen, dass in der Zeile, in der Sie interessiert sind, ein Haltepunkt für die Codezeile gesetzt wird, und klicken Sie dann auf das Symbol zum Fortsetzen der Skript **Ausführung** ![ fortsetzen ][ImageResumeScriptExecutionIcon] , aber es gibt einen schnelleren Weg.  

Klicken Sie mit der rechten Maustaste auf die Codezeile, für die Sie sich interessieren, und wählen Sie **hier weiter**.  DevTools führt den gesamten Code bis zu diesem Punkt aus und hält dann in dieser Zeile an.  

> ##### Abbildung4  
> Auswählen **von weiter hier**  
> ![Auswählen von weiter hier][ImageSelectingContinueToHere]  

### Starten der obersten Funktion der Aufrufliste   

Wenn Sie in einer Codezeile angehalten sind, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Frame neu starten** aus, um in der ersten Zeile der obersten Funktion in der Aufrufliste zu pausieren.  Die oberste Funktion ist die letzte aufgerufene Funktion.  

Nehmen wir beispielsweise an, dass Sie den folgenden Code durchlaufen:  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Sie sind angehalten `A` .  Nachdem Sie auf **Frame neu starten**geklickt haben, sollten Sie angehalten werden `B` , ohne einen Haltepunkt festzulegen oder die **Ausführung von Skript Fortsetzung**zu drücken.  

> ##### Abbildung5  
> Auswählen von " **Frame neu starten** "  
> ![Auswählen von "Frame neu starten"][ImageSelectingRestartFrame]  

### Fortsetzen der Skriptlaufzeit   

Wenn Sie die Laufzeit nach einer Pause Ihres Skripts fortsetzen möchten, klicken Sie auf das Symbol Ausführungsskript **Ausführung fortsetzen** ![ ][ImageResumeScriptExecutionIcon] .  DevTools führt das Skript bis zum nächsten Haltepunkt aus, sofern vorhanden.  

> ##### Abbildung6  
> Auswählen der **Skriptausführung fortsetzen**  
> ![Auswählen der Skriptausführung fortsetzen][ImageSelectingResumeScriptExecution]  

#### Erzwingen der Skriptlaufzeit   

Wenn Sie alle Haltepunkte ignorieren und die Ausführung des Skripts erzwingen möchten, klicken Sie auf **das** Symbol Ausführungsskript Ausführung fortsetzen, und halten Sie es gedrückt, ![ ][ImageResumeScriptExecutionIcon] und wählen Sie dann Skript Ausführungs **Force script execution** ![ Erzwingung erzwingen aus ][ImageForceScriptExecutionIcon] .  

> ##### Abbildung7  
> Auswählen der **Erzwingung der Skriptausführung**  
> ![Auswählen der Erzwingung der Skriptausführung][ImageSelectingForceScriptExecution]  

### Ändern des Thread Kontexts   

Wenn Sie mit webarbeitern oder Dienst Mitarbeitern arbeiten, klicken Sie auf einen im Bereich **Threads** aufgelisteten Kontext, um zu diesem Kontext zu wechseln.  Das blaue Pfeilsymbol steht für den aktuell ausgewählten Kontext.  

> ##### Abbildung8  
> Der Bereich " **Threads** "  
> ![Der Bereich "Threads"][ImageThreadsPane]  

Nehmen wir beispielsweise an, dass Sie sowohl in Ihrem Hauptskript als auch in Ihrem Dienstmitarbeiter Skript an einem Haltepunkt angehalten werden.  Sie möchten die lokalen und globalen Eigenschaften für den Service Worker-Kontext anzeigen, aber der Bereich " **Quellen** " zeigt den Hauptskript Kontext an.  Durch Klicken auf den Eintrag Service Worker im Bereich **Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.  

## Anzeigen und Bearbeiten von lokalen, Closure-und globalen Eigenschaften   

Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie **den Bereich Bereich,** um die Werte von Eigenschaften und Variablen in den Bereichen lokal, Closure und Global anzuzeigen und zu bearbeiten.  

*   Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.  
*   Nicht aufzählbare Eigenschaften werden abgeblendet dargestellt.  

> ##### Abbildung 9  
> **Bereichs** Bereich  
> ![Bereichs Bereich][ImageScopePane]  

## Anzeigen der aktuellen Anrufliste   

Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie den Bereich **Anrufliste** , um die Anrufliste anzuzeigen, die Sie zu diesem Punkt erhalten hat.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Klicken Sie auf einen Eintrag, um zu der Codezeile zu springen, in der die Funktion aufgerufen wurde.  Das blaue Pfeilsymbol stellt dar, welche Funktion devtools derzeit markiert.  

> ##### Abbildung 10  
> Der Bereich " **Anrufliste** "  
> ![Der Bereich "Anrufliste"][ImageCallStackPane]  

> [!NOTE]
> Wenn Sie nicht in einer Codezeile angehalten wurden, ist der Bereich **Aufrufliste** leer.  

### Kopieren einer Stapelüberwachung   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Stapelüberwachung kopieren** aus, um die aktuelle Aufrufliste in die Zwischenablage zu kopieren.  

> ##### Abbildung 11  
> Auswählen der **Stapelüberwachung kopieren**  
> ![Auswählen der Stapelüberwachung kopieren][ImageSelectingCopyStackTrace]  

Nachfolgend finden Sie ein Beispiel für die Ausgabe:  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorieren eines Skripts oder Musters von Skripts  

Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.  Wenn es sich um einen Bibliothekscode handelt, wird ein Skript im Bereich " **Aufrufliste** " verdeckt, und Sie gehen nie in die Funktionen des Skripts ein, wenn Sie den Code schrittweise durchlaufen.  

Nehmen wir beispielsweise an, dass Sie diesen Code durchlaufen:  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` ist eine drittanbieterbibliothek, der Sie vertrauen.  Wenn Sie sicher sind, dass das Problem, das Sie Debuggen, nicht mit der Bibliothek von Drittanbietern verknüpft ist, ist es sinnvoll, das Skript als **Bibliothekscode**zu kennzeichnen.  

### Markieren eines Skripts als Bibliothekscode im Bereich "Editor"  

So markieren Sie ein Skript im **Editor** Bereich als **Bibliothekscode** :  

1.  Öffnen Sie die Datei.  
1.  Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle.  
1.  Wählen Sie **als Bibliothekscode markieren**aus.  

> ##### Abbildung 12  
> Markieren eines Skripts als **Bibliothekscode** über den Bereich " **Editor** "  
> ![Markieren eines Skripts als Bibliothekscode über den Bereich "Editor"][ImageMarkEditorPane]  

### Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"  

So markieren Sie ein Skript aus dem Bereich " **Anrufliste** " als **Bibliothekscode** :  

1.  Klicken Sie mit der rechten Maustaste auf eine Funktion aus dem Skript.  
1.  Wählen Sie **als Bibliothekscode markieren**aus.  

> ##### Abbildung 13  
> Markieren eines Skripts als **Bibliothekscode** aus dem Bereich " **Anrufliste** "  
> ![Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"][ImageMarkCallStackPane]  

### Markieren eines Skripts als Bibliothekscode aus Einstellungen  

So markieren Sie ein einzelnes Skript oder Skript Muster aus den Einstellungen:  

1.  Öffnen Sie [Einstellungen][DevToolsCustomize].  
1.  Wechseln Sie zur Registerkarte **Bibliothekscode** .  
1.  Klicken Sie auf **Muster hinzufügen**.  
1.  Geben Sie den Skriptnamen oder ein Regex-Muster von Skriptnamen ein, das als **Bibliothekscode**markiert werden soll.  
1.  Klicken Sie auf **Hinzufügen**.  

> ##### Abbildung 14  
> Markieren eines Skripts als **Bibliothekscode** aus Einstellungen  
> ![Markieren eines Skripts als Bibliothekscode aus Einstellungen][ImageMarkScriptSettings]  

## Ausführen von Codeausschnitten von Debugcode auf jeder Seite   

Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Snippets in Betracht gezogen sehen.  Ausschnitte sind Lauf Zeit Skripte, die Sie in devtools erstellen, speichern und ausführen.  

Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevToolsJavascriptSnippets] .  

## Sehen Sie sich die Werte benutzerdefinierter JavaScript-Ausdrücke an   

Verwenden Sie den **Überwachungs** Bereich, um die Werte benutzerdefinierter Ausdrücke zu überwachen.  Sie können jeden gültigen JavaScript-Ausdruck sehen.  

> ##### Abbildung 15  
> Der **Überwachungs** Bereich  
> ![Der Überwachungsbereich][ImageWatchPane]  

*   Klicken Sie auf **Add Expression** das ![ Symbol zum Hinzufügen eines Ausdrucks hinzufügen ][ImageAddExpressionIcon] , um einen neuen Überwachungsausdruck zu erstellen.  
*   Klicken Sie auf **das Aktualisierungs** ![ Symbol Aktualisieren ][ImageRefreshIcon] , um die Werte aller vorhandenen Ausdrücke zu aktualisieren.  Werte werden beim Durchlaufen des Codes automatisch aktualisiert.  
*   Zeigen Sie mit der Maus auf einen Ausdruck, und klicken Sie **auf das** Symbol Ausdrucks löschen Ausdruck löschen ![ ][ImageDeleteExpressionIcon] , um es zu löschen.  

## Erstellen einer lesbaren minimierte-Datei   

Klicken Sie auf das Symbol **Format** formatieren ![ ][ImageFormatIcon] , um eine minimierte-Datei menschlich lesbar zu machen.  

> ##### Abbildung 16  
> Schaltfläche " **Format** "  
> ![Schaltfläche "Format"][ImageFormat]  

## Bearbeiten eines Skripts   

Wenn Sie einen Fehler beheben, möchten Sie häufig einige Änderungen an Ihrem JavaScript-Code testen.  Sie müssen die Änderungen nicht in einem externen Editor oder in einer IDE vornehmen und die Seite dann erneut laden.  Sie können Ihr Skript in devtools bearbeiten.  

So bearbeiten Sie ein Skript:  

1.  Öffnen Sie die Datei im Bereich " **Editor** " des Bereichs " **Quellen** ".  
1.  Nehmen Sie die gewünschten Änderungen im Bereich " **Editor** " vor.  
1.  Drücken Sie `Ctrl` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.  DevTools-Patches die gesamte JS-Datei in das JavaScript-Modul von Microsoft Edge.  

> ##### Abbildung 17  
> Der Bereich " **Editor** "  
> ![Der Bereich "Editor"][ImageEditorPane]  

## JavaScript deaktivieren   

Weitere Informationen finden Sie unter [Deaktivieren von JavaScript mit Microsoft Edge devtools][DevToolsJavascriptDisable].  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Abbildung 1: Auswählen des Schritts"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Abbildung 2: Auswählen von "Schritt in""  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Abbildung 3: Auswählen von "Schritt aus""  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Abbildung 4: Auswählen von "weiter hier""  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Abbildung 5: Auswählen von "Frame neu starten""  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Abbildung 6: Auswählen der Skriptausführung fortsetzen"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Abbildung 7: Auswählen der Erzwingung der Skriptausführung"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Abbildung 8: der Bereich "Threads""  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Abbildung 9: Bereichs Bereich"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Abbildung 10: der Bereich "Anrufliste""  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Abbildung 11: Auswählen der Stapelüberwachung kopieren"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Abbildung 12: Kennzeichnen eines Skripts als Bibliothekscode im Bereich "Editor""  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Abbildung 13: Kennzeichnen eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste""  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Abbildung 14: Kennzeichnen eines Skripts als Bibliothekscode aus Einstellungen"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Abbildung 15: Überwachungsbereich"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Abbildung 16: die Schaltfläche "Format""  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Abbildung 17: der Bereich "Editor""  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools"  
[DevToolsJavascriptGetStarted]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  
[DevToolsJavascriptSnippets]: snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  

[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge devtools"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
