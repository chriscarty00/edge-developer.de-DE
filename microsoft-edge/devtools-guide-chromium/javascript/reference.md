---
title: JavaScript-Debugging-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a6ec2438457c81ed527154af30c9642d5c287d3c
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991216"
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

# JavaScript-febugging-Referenz  

Entdecken Sie neue Debugging-Workflows mit der folgenden umfassenden Referenz zu den Microsoft Edge DevTools-Debugging-Features.  

Informationen zu den Grundlagen des Debuggens finden Sie unter [Erste Schritte beim Debuggen von JavaScript in Microsoft Edge devtools][DevToolsJavascriptGetStarted] .  

## Anhalten von Code mit Haltepunkten  

Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.  

Informationen zum Festlegen von Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints] .  

## Schritt-für-Schritt-Code  

Nachdem der Code angehalten wurde, führen Sie ihn schrittweise durch, und untersuchen Sie die Fluss-und Eigenschaftswerte auf dem Weg.  

### Schritt über Codezeile  

Wenn Sie in einer Codezeile mit einer Funktion angehalten wurden, die für das zu debuggende Problem nicht relevant ist, klicken Sie auf die Schaltfläche **Schritt über** \ ( ![ Schritt über ][ImageStepOverIcon] \), um die Funktion auszuführen, ohne Sie zu betreten.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Wählen Sie Schritt über" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Wählen Sie **Schritt über**  
:::image-end:::  

Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt Debuggen.  

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

Wenn **Sie in einer** Codezeile mit einem Funktionsaufruf, der sich auf das zu debuggende Problem bezieht, angehalten haben, klicken Sie auf die Schaltfläche \ ( ![ Schritt in ][ImageStepIntoIcon] \), um diese Funktion weiter zu untersuchen.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Schritt in auswählen" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   **Schritt in** auswählen  
:::image-end:::  

Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt Debuggen.  

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

Wenn Sie innerhalb einer Funktion angehalten haben, die nicht mit dem Problem in Verbindung steht, das Sie Debuggen, klicken Sie **auf die** ![ ][ImageStepOutIcon] Schaltfläche zum Ausführen des restlichen Codes der Funktion.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Auswählen von "Schritt aus"" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Auswählen **von "Schritt aus** "  
:::image-end:::  

Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt Debuggen.  

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

Sie können alle Zeilen durchlaufen, aber das ist mühsam.  Sie können festlegen, dass in der Zeile, in der Sie interessiert sind, ein Haltepunkt für den Code in der Zeile gesetzt wird, und dann auf die Schaltfläche **Skriptausführung** \ ( ![ Skriptausführung fortsetzen ][ImageResumeScriptExecutionIcon] \) klicken, aber es gibt eine schnellere Möglichkeit.  

Klicken Sie mit der rechten Maustaste auf die Codezeile, für die Sie sich interessieren, und wählen Sie **hier weiter**.  DevTools führt den gesamten Code bis zu diesem Punkt aus und hält dann in dieser Zeile an.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Wählen Sie hier weiter" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Wählen Sie **hier weiter**  
:::image-end:::  

### Starten der obersten Funktion der Aufrufliste  

Wenn Sie in einer Codezeile angehalten sind, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Frame neu starten** aus, um in der ersten Zeile der obersten Funktion in der Aufrufliste zu pausieren.  Die oberste Funktion ist die letzte Funktion, die ausgeführt wurde.  

Der folgende Codeausschnitt ist ein Beispiel für eine schrittweise Anleitung.  

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

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Wählen Sie Frame neu starten aus." lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Wählen Sie **Frame neu starten** aus.  
:::image-end:::  

### Fortsetzen der Skriptlaufzeit  

Wenn Sie die Laufzeit nach einer Pause Ihres Skripts fortsetzen möchten, **Resume Script Execution** klicken Sie auf die ![ Schaltfläche "Skriptausführung fortsetzen ][ImageResumeScriptExecutionIcon] \".  DevTools führt das Skript bis zum nächsten Haltepunkt aus, sofern vorhanden.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Auswählen der Skriptausführung fortsetzen" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Auswählen der **Skriptausführung fortsetzen**  
:::image-end:::  

#### Erzwingen der Skriptlaufzeit  

Wenn Sie alle Haltepunkte ignorieren und das Fortsetzen des Skripts erzwingen möchten, klicken Sie auf die Schaltfläche Skriptausführung **fort** setzen \ ( ![ Fortsetzen der Skriptausführung ][ImageResumeScriptExecutionIcon] \), und wählen Sie dann die Schaltfläche Skriptausführung **erzwingen** \ ( ![ Skriptausführung erzwingen ][ImageForceScriptExecutionIcon] \) aus.  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Auswählen der Erzwingung der Skriptausführung" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Auswählen der **Erzwingung der Skriptausführung**  
:::image-end:::  

### Ändern des Thread Kontexts  

Wenn Sie mit webarbeitern oder Dienst Mitarbeitern arbeiten, klicken Sie auf einen im Bereich **Threads** aufgelisteten Kontext, um zu diesem Kontext zu wechseln.  Das blaue Pfeilsymbol steht für den aktuell ausgewählten Kontext.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Der Bereich "Threads"" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Der Bereich " **Threads** "  
:::image-end:::  

Nehmen wir beispielsweise an, dass Sie sowohl in Ihrem Hauptskript als auch in Ihrem Dienstmitarbeiter Skript an einem Haltepunkt angehalten werden.  Sie möchten die lokalen und globalen Eigenschaften für den Service Worker-Kontext anzeigen, aber der Bereich " **Quellen** " zeigt den Hauptskript Kontext an.  Durch Klicken auf den Eintrag Service Worker im Bereich **Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.  

## Anzeigen und Bearbeiten von lokalen, Closure-und globalen Eigenschaften  

Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie **den Bereich Bereich,** um die Werte von Eigenschaften und Variablen in den Bereichen lokal, Closure und Global anzuzeigen und zu bearbeiten.  

*   Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.  
*   Nicht aufzählbare Eigenschaften werden abgeblendet dargestellt.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Bereichs Bereich" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   **Bereichs** Bereich  
:::image-end:::  

## Anzeigen der aktuellen Anrufliste  

Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie den Bereich **Anrufliste** , um die Anrufliste anzuzeigen, die Sie zu diesem Punkt erhalten hat.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Klicken Sie auf einen Eintrag, um zu der Codezeile zu springen, in der die Funktion aufgerufen wurde.  Das blaue Pfeilsymbol stellt dar, welche Funktion devtools derzeit markiert.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Der Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Der Bereich " **Anrufliste** "  
:::image-end:::  

> [!NOTE]
> Wenn Sie nicht in einer Codezeile angehalten wurden, ist der Bereich **Aufrufliste** leer.  

### Kopieren einer Stapelüberwachung  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Stapelüberwachung kopieren** aus, um die aktuelle Aufrufliste in die Zwischenablage zu kopieren.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Wählen Sie Stapelüberwachung kopieren aus." lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Wählen Sie **Stapelüberwachung kopieren** aus.  
:::image-end:::  

Der folgende Codeausschnitt ist ein Beispiel für die Ausgabe.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorieren eines Skripts oder Musters von Skripts  

Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.  Wenn es sich um einen Bibliothekscode handelt, wird ein Skript im Bereich " **Aufrufliste** " verdeckt, und Sie gehen nie in die Funktionen des Skripts ein, wenn Sie den Code schrittweise durchlaufen.  

Der folgende Codeausschnitt ist ein Beispiel für eine schrittweise Anleitung.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` ist eine drittanbieterbibliothek, der Sie vertrauen.  Wenn Sie sicher sind, dass das Problem, das Sie Debuggen, nicht mit der Bibliothek von Drittanbietern verknüpft ist, ist es sinnvoll, das Skript als **Bibliothekscode**zu kennzeichnen.  

### Markieren eines Skripts als Bibliothekscode im Bereich "Editor"  

Führen Sie die folgenden Aktionen aus, um ein Skript im **Editor** Bereich als **Bibliothekscode** zu kennzeichnen.  

1.  Öffnen Sie die Datei.  
1.  Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle.  
1.  Wählen Sie **als Bibliothekscode markieren**aus.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode im Bereich "Editor"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Markieren eines Skripts als **Bibliothekscode** im Bereich " **Editor** "  
    :::image-end:::  
    
### Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"  

Compelte Sie die folliwng-Aktionen aus, um ein Skript aus dem Bereich " **Aufrufliste** " als **Bibliothekscode** zu kennzeichnen.  

1.  Klicken Sie mit der rechten Maustaste auf eine Funktion aus dem Skript.  
1.  Wählen Sie **als Bibliothekscode markieren**aus.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Markieren eines Skripts als **Bibliothekscode** aus dem Bereich " **Anrufliste** "  
    :::image-end:::  
    
### Markieren eines Skripts als Bibliothekscode aus Einstellungen  

Führen Sie die folgenden Aktionen aus, um ein einzelnes Skript oder Muster von Skripts aus **Einstellungen**zu kennzeichnen.  

1.  Öffnen Sie [Einstellungen][DevToolsCustomize].  
1.  Wechseln Sie zur Registerkarte **Bibliothekscode** .  
1.  Klicken Sie auf **Muster hinzufügen**.  
1.  Geben Sie den Skriptnamen oder ein Regex-Muster von Skriptnamen ein, das als **Bibliothekscode**markiert werden soll.  
1.  Klicken Sie auf **Hinzufügen**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus Einstellungen" lightbox="../media/javascript-framework-library-code.msft.png":::
       Markieren eines Skripts als **Bibliothekscode** aus **Einstellungen**  
    :::image-end:::  
    
## Ausführen von Codeausschnitten von Debugcode auf jeder Seite   

Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Snippets in Betracht gezogen sehen.  Ausschnitte sind Lauf Zeit Skripte, die Sie in devtools erstellen, speichern und ausführen.  

Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevToolsJavascriptSnippets] .  

## Sehen Sie sich die Werte benutzerdefinierter JavaScript-Ausdrücke an  

Verwenden Sie den **Überwachungs** Bereich, um die Werte benutzerdefinierter Ausdrücke zu überwachen.  Sie können jeden gültigen JavaScript-Ausdruck sehen.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Der Überwachungsbereich" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Der **Überwachungs** Bereich  
:::image-end:::  

*   Klicken Sie auf die Schaltfläche **Ausdruck hinzufügen** \ ( ![ Ausdruck hinzufügen ][ImageAddExpressionIcon] \), um einen neuen Überwachungsausdruck zu erstellen.  
*   Klicken Sie auf die Schaltfläche **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \), um die Werte aller vorhandenen Ausdrücke zu aktualisieren.  Werte werden beim Durchlaufen des Codes automatisch aktualisiert.  
*   Zeigen Sie mit der Maus auf einen Ausdruck, und klicken Sie auf die Schaltfläche zum **Löschen** des Ausdrucks \ ( ![ Ausdruck löschen ][ImageDeleteExpressionIcon] ), um Sie zu löschen.  

## Erstellen einer lesbaren minimierte-Datei  

Klicken Sie auf die Schaltfläche **Format** \ ( ![ Format ][ImageFormatIcon] \), um eine minimierte-Datei menschlich lesbar zu machen.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Schaltfläche "Format"" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Schaltfläche " **Format** "  
:::image-end:::  

## Bearbeiten eines Skripts   

Wenn Sie einen Fehler beheben, möchten Sie häufig einige Änderungen an Ihrem JavaScript-Code testen.  Sie müssen die Änderungen nicht in einem externen Editor oder in einer IDE vornehmen und die Seite dann erneut laden.  Sie können Ihr Skript in devtools bearbeiten.  

Führen Sie die folgenden Aktionen aus, um ein Skript zu bearbeiten.  

1.  Öffnen Sie die Datei im Bereich " **Editor** " des Bereichs " **Quellen** ".  
1.  Nehmen Sie die gewünschten Änderungen im Bereich " **Editor** " vor.  
1.  Drücken Sie `Ctrl` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.  DevTools-Patches die gesamte JS-Datei in das JavaScript-Modul von Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Der Bereich "Editor"" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Der Bereich " **Editor** "  
    :::image-end:::  
     
## JavaScript deaktivieren   

Weitere Informationen finden Sie unter [Deaktivieren von JavaScript mit Microsoft Edge devtools][DevToolsJavascriptDisable].  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools | Microsoft docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools | Microsoft docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  
[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
