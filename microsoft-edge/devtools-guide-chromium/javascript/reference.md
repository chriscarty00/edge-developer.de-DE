---
description: Entdecken Sie neue Debuggingworkflows in diesem umfassenden Verweis auf Die Debugfeatures von Microsoft Edge DevTools.
title: JavaScript-Debugging-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398476"
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

# <a name="javascript-debugging-reference"></a>JavaScript-Debugging-Referenz  

Entdecken Sie neue Debugworkflows mit dem folgenden umfassenden Verweis auf Die Debugfeatures von Microsoft Edge DevTools.  

Um die Grundlagen des Debuggens zu erlernen, navigieren Sie zu Erste Schritte mit dem Debuggen von [JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted].  

## <a name="pause-code-with-breakpoints"></a>Anhalten von Code mit Haltepunkten  

Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.  

Informationen zum Festlegen von Haltepunkten finden Sie unter [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].  

## <a name="step-through-code"></a>Schritt durch Code  

Sobald Der Code angehalten wurde, durchschritten Sie ihn, eine Zeile nach der anderen, und untersuchen Sie dabei den Steuerungsfluss und die Eigenschaftswerte.  

### <a name="step-over-line-of-code"></a>Schritt über Codezeile  

Wenn sie in einer Codezeile angehalten wird, die eine Funktion enthält, die für das Problem, das Sie debuggen, nicht relevant ist, wählen Sie die Schaltfläche **Schritt** über \( Schritt über ![ \) aus, um die Funktion auszuführen, ohne sie ][ImageStepOverIcon] auszuführen.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Wählen Sie Schritt über" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Wählen Sie **Schritt über**  
:::image-end:::  

Angenommen, Sie debuggen den folgenden Codeausschnitt.  

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

Sie werden auf `A` angehalten.  Nachdem Sie **Schritt über**auswählen, führt DevTools den ganzen Code in der Funktion aus, über die Sie schrittweise gehen, d. h. und `B` `C` .  DevTools hält dann auf `D` an.  

### <a name="step-into-line-of-code"></a>Schritt in Codezeile  

Wenn sie in einer Codezeile angehalten wird, die einen Funktionsaufruf enthält, der mit dem Problem im Zusammenhang steht, das Sie debuggen, wählen Sie die Schaltfläche **Schritt** in \( Schritt in ![ \) aus, um diese Funktion weiter ][ImageStepIntoIcon] zu untersuchen.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Wählen Sie Schritt in aus." lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Wählen Sie **Schritt in aus.**  
:::image-end:::  

Angenommen, Sie debuggen den folgenden Codeausschnitt.  

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

Sie werden auf `A` angehalten.  Nachdem Sie **Schritt in auswählen,** führt DevTools diese Codezeile aus und hält dann auf `B` an.  

### <a name="step-out-of-line-of-code"></a>Schritt aus der Codezeile  

Wenn Sie innerhalb einer Funktion angehalten werden, die nicht mit dem Debugproblem im Zusammenhang steht, wählen Sie die Schaltfläche Step **out** \( ![ Step out \) aus, um den Rest des Codes der Funktion ][ImageStepOutIcon] auszuführen.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Auswählen von Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Auswählen **von Step out**  
:::image-end:::  

Angenommen, Sie debuggen den folgenden Codeausschnitt.  

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

Sie werden auf `A` angehalten.  Nachdem Sie **Step out**auswählen, führt DevTools den Rest des Codes in aus, der sich nur in diesem Beispiel befindet, und hält dann auf `getName()` `B` `C` an.  

### <a name="run-all-code-up-to-a-specific-line"></a>Ausführen des codes bis zu einer bestimmten Zeile  

Beim Debuggen einer langen Funktion gibt es möglicherweise eine Menge Code, der nicht mit dem Problem im Zusammenhang steht, das Sie debuggen.  

Sie können alle Zeilen durchschritten, aber das ist mühsam.  Sie können einen Codepunkt in der Zeile festlegen, an der Sie interessiert sind, und dann die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) auswählen, aber es gibt eine schnellere ![ ][ImageResumeScriptExecutionIcon] Möglichkeit.  

Zeigen Sie auf die Codezeile, an der Sie interessiert sind, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Weiter zu hier aus.**  DevTools führt bis zu diesem Punkt den ganzen Code aus und hält dann in dieser Zeile an.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Wählen Sie Weiter zu hier aus." lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Wählen **Sie Weiter zu hier aus.**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Starten Sie die oberste Funktion der Aufrufliste neu.  

Wenn Sie in der ersten Zeile der obersten Funktion in Ihrer Aufrufliste anhalten und **** in einer Codezeile angehalten werden, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie Frame neu **starten**aus.  Die top-Funktion ist die letzte ausgeführte Funktion.  

Der folgende Codeausschnitt ist ein Beispiel für einen schrittweisen Schritt.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Sie werden auf `A` angehalten.  Nachdem Sie **Frame neu starten**auswählen, sollten Sie auf angehalten werden, ohne jemals einen Haltepunkt festlegen oder `B` **skriptausführung fortsetzen auswählen zu müssen.**  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Wählen Sie Frame neu starten aus" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Wählen **Sie Frame neu starten aus**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Fortsetzen der Skriptlaufzeit  

Wenn Sie die Laufzeit nach einer Pause ihres Skripts fortsetzen möchten, wählen Sie **die** Schaltfläche Skriptausführung fortsetzen \( ![ Skriptausführung fortsetzen ][ImageResumeScriptExecutionIcon] \) aus.  DevTools führt das Skript bis zum nächsten Haltepunkt aus, falls dies der Fall ist.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Wählen Sie Skriptausführung fortsetzen aus" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Wählen Sie **Skriptausführung fortsetzen aus**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Erzwingen der Skriptlaufzeit  

Um alle Haltepunkte zu ignorieren und die Fortsetzung der Ausführung des Skripts zu erzwingen, wählen Sie die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) aus, und wählen Sie dann die Schaltfläche Skriptausführung erzwingen \( Skriptausführung erzwingen ![ ][ImageResumeScriptExecutionIcon] **** ![ ][ImageForceScriptExecutionIcon] \) aus.  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Auswählen der Skriptausführung erzwingen" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Auswählen **der Skriptausführung erzwingen**  
:::image-end:::  

### <a name="change-thread-context"></a>Ändern des Threadkontexts  

Wählen Sie bei der Arbeit mit Webmitarbeitern oder Servicemitarbeitern einen Kontext aus, der im **Bereich Threads** aufgeführt ist, um zu diesem Kontext zu wechseln.  Das blaue Pfeilsymbol gibt an, welcher Kontext aktuell ausgewählt ist.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Der Bereich Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Der **Bereich Threads**  
:::image-end:::  

Angenommen, Sie werden sowohl im Hauptskript als auch im Dienstarbeitsskript an einem Haltepunkt angehalten.  Sie möchten die lokalen und globalen Eigenschaften für den Dienstarbeitskontext anzeigen, aber im **Bereich Quellen** wird der Hauptskriptkontext angezeigt.  Durch Auswählen des Dienstarbeitseintrags im **Bereich Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.  

## <a name="view-and-edit-local-closure-and-global-properties"></a>Anzeigen und Bearbeiten lokaler, geschlossener und globaler Eigenschaften  

Verwenden Sie den Bereich Bereich, **** um die Werte von Eigenschaften und Variablen in den lokalen, Schließ- und globalen Bereich anzuzeigen und zu bearbeiten, während sie in einer Codezeile angehalten werden.  

*   Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.  
*   Nicht aufzählbare Eigenschaften sind ausgegraut.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Der Bereich Bereich" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Der **Bereich Bereich**  
:::image-end:::  

## <a name="view-the-current-call-stack"></a>Anzeigen der aktuellen Aufrufliste  

Während Sie in einer Codezeile **** angehalten werden, verwenden Sie den Bereich Anrufliste, um die Aufrufliste anzuzeigen, die Sie zu diesem Punkt enstanden hat.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Wählen Sie einen Eintrag aus, um zur Codezeile zu springen, in der diese Funktion aufgerufen wurde.  Das blaue Pfeilsymbol stellt dar, welche Funktion DevTools derzeit hervorhebt.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Der Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Der **Bereich "Anrufliste"**  
:::image-end:::  

> [!NOTE]
> Wenn sie in einer Codezeile nicht angehalten wird, ist der Bereich **Anrufliste** leer.  

### <a name="copy-stack-trace"></a>Kopieren der Stapelverfolgung  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Um die aktuelle Aufrufliste in die Zwischenablage zu kopieren, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Stapelverfolgung kopieren **aus.** ****  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Wählen Sie Stapelverfolgung kopieren aus" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Wählen **Sie Stapelverfolgung kopieren aus**  
:::image-end:::  

Der folgende Codeausschnitt ist ein Beispiel für die Ausgabe.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a>Ignorieren eines Skripts oder Skriptmusters  

Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.  Wenn sie als Bibliothekscode markiert sind, **** wird ein Skript im Bereich Aufrufliste verdeckt, und Sie treten niemals in die Funktionen des Skripts ein, wenn Sie den Code durchschritten.  

Der folgende Codeausschnitt ist ein Beispiel für einen schrittweisen Schritt.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` ist eine Bibliothek eines Drittanbieters, der Sie vertrauen.  Wenn Sie sicher sind, dass das Problem, das Sie debuggen, nicht mit der Bibliothek eines Drittanbieters in Zusammenhang steht, ist es sinnvoll, das Skript als **Bibliothekscode zu kennzeichnen.**  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Markieren eines Skripts als Bibliothekscode aus dem Editorbereich  

Führen Sie die folgenden Aktionen aus, um ein Skript **im** Editorbereich als **Bibliothekscode zu** markieren.  

1.  Öffnen Sie die Datei.  
1.  Zeigen Sie auf eine beliebige Stelle, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  
1.  Wählen **Sie Als Bibliothekscode markieren aus.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Editorbereich" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Markieren eines Skripts **als Bibliothekscode** aus dem **Editorbereich**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"  

Führen Sie die folgenden Aktionen aus, um ein Skript **im** Bereich Aufrufliste als **Bibliothekscode zu** markieren.  

1.  Zeigen Sie auf eine Funktion aus dem Skript, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  
1.  Wählen **Sie Als Bibliothekscode markieren aus.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Markieren eines Skripts **als Bibliothekscode** aus dem **Bereich "Aufrufliste"**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Markieren eines Skripts als Bibliothekscode in den Einstellungen  

Führen Sie die folgenden Aktionen aus, um ein einzelnes Skript oder Muster von Skripts aus Einstellungen **zu markieren.**  

1.  Öffnen [Sie Einstellungen][DevToolsCustomize].  
1.  Navigieren Sie zur **Codeeinstellung Bibliothek.**  
1.  Wählen **Sie Muster hinzufügen aus.**  
1.  Geben Sie den Skriptnamen oder ein Regexmuster von Skriptnamen ein, die als **Bibliothekscode zu markieren sind.**  
1.  Wählen Sie **Hinzufügen**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode in den Einstellungen" lightbox="../media/javascript-framework-library-code.msft.png":::
       Markieren eines Skripts **als Bibliothekscode in** **den Einstellungen**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Ausführen von Codeausschnitten für debuggen von einer beliebigen Seite  

Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Codeausschnitte in Betracht ziehen.  Codeausschnitte sind Laufzeitskripts, die Sie in DevTools erstellen, speichern und ausführen.  

Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten von beliebigen Seiten][DevToolsJavascriptSnippets].  

## <a name="watch-the-values-of-custom-javascript-expressions"></a>Beobachten der Werte benutzerdefinierter JavaScript-Ausdrücke  

Verwenden Sie den **Bereich "Watch",** um die Werte benutzerdefinierter Ausdrücke zu beobachten.  Sie können einen beliebigen gültigen JavaScript-Ausdruck ansehen.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Der Bereich "Watch"" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Der **Bereich "Watch"**  
:::image-end:::  

*   Wählen Sie **die Schaltfläche Ausdruck** hinzufügen \( Ausdruck hinzufügen ![ ][ImageAddExpressionIcon] \) aus, um einen neuen Watchausdruck zu erstellen.  
*   Wählen Sie die **Schaltfläche Aktualisieren** \( ![ Aktualisieren ][ImageRefreshIcon] \) aus, um die Werte aller vorhandenen Ausdrücke zu aktualisieren.  Werte werden automatisch aktualisiert, während Code schrittweise durchschritten wird.  
*   Zeigen Sie auf einen Ausdruck, und wählen Sie die Schaltfläche **Ausdruck** löschen \( ![ Ausdruck löschen ][ImageDeleteExpressionIcon] \) aus, um ihn zu löschen.  

## <a name="make-a-minified-file-readable"></a>Lesen einer verminten Datei  

Wählen Sie **die Schaltfläche Format** \( Format ![ \) aus, um eine verminte Datei lesbar ][ImageFormatIcon] zu machen.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Die Schaltfläche Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Die **Schaltfläche Format**  
:::image-end:::  

## <a name="edit-a-script"></a>Bearbeiten eines Skripts  

Beim Beheben eines Fehlers möchten Sie häufig einige Änderungen an Ihrem #A0 testen.  Sie müssen die Änderungen nicht in einem externen Editor oder einer IDE vornehmen und dann die Seite aktualisieren.  Sie können Ihr Skript in DevTools bearbeiten.  

Führen Sie die folgenden Aktionen aus, um ein Skript zu bearbeiten.  

1.  Öffnen Sie die Datei im **Editorbereich** des **Bereichs Quellen.**  
1.  Nehmen Sie Ihre Änderungen im **Editorbereich** vor.  
1.  Wählen `Ctrl` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.  DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Der Editorbereich" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Der **Editorbereich**  
    :::image-end:::  
     
## <a name="disable-javascript"></a>JavaScript deaktivieren  

Navigieren Sie [zu Deaktivieren von JavaScript mit Microsoft Edge DevTools][DevToolsJavascriptDisable].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

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

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deaktivieren von JavaScript mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
