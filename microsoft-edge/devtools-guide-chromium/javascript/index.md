---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um JavaScript-Fehler zu finden und zu beheben.
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398441"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a>Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools  

In diesem Artikel wird der grundlegende Workflow zum Debuggen von JavaScript-Problem in DevTools erläutert.  

## <a name="step-1-reproduce-the-bug"></a>Schritt 1: Reproduzieren des Fehlers  

Das Suchen einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt zum Debuggen.  

1.  Wählen **Sie Demo öffnen aus.**  Halten `Control` Sie \(Windows, Linux\) oder `Command` \(macOS\) fest, und öffnen Sie die Demo auf einer neuen Browserregisterkarte.  
    
    [Demo öffnen][OpenDebugJSDemo]  
    
1.  Geben `5` Sie in das Textfeld Zahl **1** ein.  
1.  Geben `1` Sie in das Textfeld Nummer **2** ein.  
1.  Wählen **Sie Nummer 1 und Nummer 2 hinzufügen aus.**  Die Bezeichnung unterhalb der Schaltfläche sagt `5 + 1 = 51` .  Das Ergebnis sollte `6` sein.  Beheben Sie als Nächstes den Additionsfehler, bei dem es sich um den Fehler handelt.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 führt zu 51, sollte aber 6 sein" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` führt zu `51` , sollte aber `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a>Schritt 2: Machen Sie sich mit der Benutzeroberfläche des Quellentools vertraut  

DevTools bietet viele verschiedene Tools für verschiedene Aufgaben.  Zu den verschiedenen Aufgaben gehören das Ändern von CSS, die Profilerstellung der Seitenladeleistung und die Überwachung von Netzwerkanforderungen.  Das **Tool Sources** ist der Ort, an dem Sie JavaScript debuggen.  

1.  Um das **Konsolentool** in DevTools zu öffnen, wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Das Konsolentool" lightbox="../media/javascript-console-empty.msft.png":::
       Das **Konsolentool**  
    :::image-end:::  
    
1.  Wählen Sie das **Tool Quellen** aus.  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Das Tool "Quellen"" lightbox="../media/javascript-sources-sections.msft.png":::
       Das **Tool "Quellen"**  
    :::image-end:::  
    
Die **Benutzeroberfläche** des Quellentools hat drei Teile.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Die 3 Teile der Benutzeroberfläche des Quellentools" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Die 3 Teile der **Benutzeroberfläche des Quellentools**  
:::image-end:::  

1.  Der **Bereich Dateinavigator** \(Abschnitt 1 in der vorherigen Abbildung\).  Jede Datei, die die Webseite anfordert, wird hier aufgelistet.  
1.  Der **Code-Editor-Bereich** \(Abschnitt 2 in der vorherigen Abbildung\).  Nachdem Sie eine Datei im Bereich **Dateinavigator** ausgewählt haben, wird der Inhalt dieser Datei hier angezeigt.  
1.  Der **JavaScript-Debugbereich** \(Abschnitt 3 in der vorherigen Abbildung\).  Verschiedene Tools zum Überprüfen des JavaScript für die Webseite.  Wenn Ihr DevTools-Fenster breit ist, wird dieser Bereich rechts neben dem **Code-Editor-Bereich** angezeigt.  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a>Schritt 3: Anhalten des Codes mit einem Haltepunkt  

Eine gängige Methode zum Debuggen dieser Art von Problem ist das Einfügen mehrerer Anweisungen in den Code und anschließend das Überprüfen von Werten während der Ausführung `console.log()` des Skripts.  Zum Beispiel:  

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

Die `console.log()` -Methode kann den Auftrag erledigen, aber **haltepunkte machen** es schneller.  Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.  Haltepunkte haben die folgenden Vorteile gegenüber der `console.log()` Methode.  

*   Mit müssen Sie den Quellcode manuell öffnen, den relevanten Code suchen, die Anweisungen einfügen und dann die Webseite aktualisieren, um die Nachrichten in der Konsole `console.log()` `console.log()` **anzuzeigen.**  Mit Haltepunkten können Sie den relevanten Code anhalten, ohne zu wissen, wie der Code strukturiert ist.  
*   In Ihren `console.log()` Anweisungen müssen Sie jeden Wert explizit angeben, den Sie überprüfen möchten.  Mit Haltepunkten zeigt DevTools die Werte aller Variablen zu diesem Zeitpunkt an.  Manchmal werden Variablen, die sich auf Ihren Code auswirken, ausgeblendet und verschleiert.  
    
Kurz gesagt, haltepunkte können Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.  

Wenn Sie zurück treten und überlegen, wie die App funktioniert, können Sie eine gebildete Vermutung treffen, dass die falsche Summe \( \) im Ereignislistener berechnet wird, der der Schaltfläche Nummer 1 und Nummer 2 hinzufügen zugeordnet `5 + 1 = 51` `click` ist. ****  Daher möchten Sie den Code wahrscheinlich zu dem Zeitpunkt anhalten, zu dem der `click` Listener ausgeführt wird.  **Mit Ereignislistener-Haltepunkten** können Sie genau dies tun:  

1.  Wählen Sie **im Bereich JavaScript-Debugging** die **Option Ereignislistener-Haltepunkte** aus, um den Abschnitt zu erweitern.  DevTools zeigt eine Liste erweiterbarer Ereigniskategorien an, z. B. **Animation** und **Zwischenablage.**  
1.  Wählen Sie neben **der Kategorie Mouse-Ereignis** **die Option Erweitern** \( Symbol erweitern ![ ][ImageExpandIcon] \).  DevTools zeigt eine Liste von Mausereignissen an, z. B. **Klicken** **und Mousedown**.  Jedes Ereignis hat ein Kontrollkästchen daneben.  
1.  Aktivieren Sie das Kontrollkästchen neben , um **auf zu klicken.**  DevTools ist jetzt so eingerichtet, dass es automatisch angehalten wird, wenn ein `click` Ereignislistener ausgeführt wird.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Aktivieren Sie das Kontrollkästchen neben dem Klicken." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Aktivieren Sie das Kontrollkästchen neben **dem Klicken.**  
    :::image-end:::  
    
1.  Wählen Sie wieder auf der Demo **die Option Nummer 1 und Nummer 2** hinzufügen aus.  DevTools hält die Demo an und hebt eine Codezeile im **Tool Quellen** hervor.  DevTools sollte in Zeile 16 in `get-started.js` anhalten.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Wenn Sie in einer anderen Codezeile anhalten, wählen Sie **Skriptausführung** fortsetzen \( Skriptausführung fortsetzen \) aus, bis Sie in der richtigen ![ ][ImageResumeIcon] Zeile anhalten.  
    
    > [!NOTE]
    > Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browsererweiterung, die einen Ereignislistener auf jeder besuchten `click` Webseite registriert.  Sie werden im Listener der `click` Erweiterung angehalten.  Wenn Sie den InPrivate-Modus verwenden, um **im**privaten Modus zu navigieren, wodurch alle Erweiterungen deaktiviert werden, wird möglicherweise jedes Mal angezeigt, dass Sie in der gewünschten Codezeile anhalten.  

<!--todo: add inprivate section when available -->  

**Ereignislistener-Haltepunkte** sind nur einer von vielen Arten von Haltepunkten, die in DevTools verfügbar sind.  Merken Sie sich alle verschiedenen Typen, um unterschiedliche Szenarien so schnell wie möglich zu debuggen.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a>Schritt 4: Schritt durch den Code  

Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.  Wenn Sie den Code schrittweise durchschritten haben, können Sie die Laufzeit Ihres Codes durchfingen.  Sie gehen eine Zeile gleichzeitig durch, um herauszufinden, wo Ihr Code in einer anderen Reihenfolge ausgeführt wird als erwartet.  Probieren Sie es jetzt aus:  

1.  Wählen **Sie Schritt über nächsten Funktionsaufruf** \( Schritt über nächsten ![ Funktionsaufruf ][ImageOverIcon] \).  DevTools führt den folgenden Code aus, ohne ihn zu verwenden.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools überspringt einige Codezeilen.  Dies liegt `inputsAreEmpty()` daran, dass false ausgewertet wird, sodass der Codeblock für die Anweisung `if` nicht ausgeführt wird.  
    
1.  Wählen Sie **im Tool** Quellen von DevTools Schritt **in** nächsten Funktionsaufruf \( Schritt in nächsten Funktionsaufruf \) aus, um die Laufzeit der Funktion zu durchschritten, eine Zeile ![ ][ImageIntoIcon] nach der `updateLabel()` anderen.  
    
Das Überprüfen einer Zeile nach dem anderen ist die grundlegende Idee des Schrittweisen Durcharbeitens von Code.  Wenn Sie den Code in `get-started.js` überprüfen, befindet sich der Fehler wahrscheinlich irgendwo in der `updateLabel()` Funktion.  Anstatt jede Codezeile zu durchbrechen, können Sie eine andere Art von Haltepunkt verwenden, um den Code näher am wahrscheinlichen Speicherort des Fehlers anzuhalten.  

## <a name="step-5-set-a-line-of-code-breakpoint"></a>Schritt 5: Festlegen eines Codezeile-Haltepunkts  

Codelinien-Haltepunkte sind die am häufigsten verwendeten Haltepunkte.  Wenn Sie zu der bestimmten Codezeile kommen, die Sie anhalten möchten, verwenden Sie einen Codezeile-Haltepunkt.  

1.  Sehen Sie sich die letzte Codezeile in `updateLabel()` an:  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  Auf der linken Seite wird die Nummer dieser bestimmten Codezeile als **34 angezeigt.**  Wählen Sie Zeile **34 aus.**  DevTools zeigt links von **34**ein rotes Symbol an.  Das rote Symbol gibt an, dass sich ein Codepunkt in dieser Zeile befindet.  DevTools hält immer an, bevor diese Codezeile ausgeführt wird.  
1.  Wählen **Sie Skriptausführung fortsetzen** \( ![ Skriptausführung fortsetzen ][ImageResumeIcon] \).  Das Skript wird weiterhin ausgeführt, bis Zeile 33 erreicht ist.  In den Zeilen 31, 32 und 33 druckt DevTools die Werte von , und rechts neben dem `addend1` `addend2` `sum` Semikolon in jeder Zeile.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools hält am Zeilen-of-Code-Haltepunkt in Zeile 34 an" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools hält am Zeilen-of-Code-Haltepunkt in Zeile 34 an  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a>Schritt 6: Überprüfen von Variablenwerten  

Die Werte `addend1` von , und sehen `addend2` `sum` verdächtig aus.  Die Werte werden in Anführungszeichen eingeschlossen.  Die Anführungszeichen bedeuten, dass der Wert eine Zeichenfolge ist. Dies ist eine gute Hypothese, um die Ursache des Fehlers zu erläutern.  Sammeln Sie weitere Informationen zur Situation.  DevTools bietet viele Tools zum Untersuchen von Variablenwerten.  

### <a name="method-1-the-scope-panel"></a>Methode 1: Bereich  

Wenn Sie in einer Codezeile **** anhalten, werden im Bereich Bereich die lokalen und globalen Variablen angezeigt, die derzeit definiert sind, zusammen mit dem Wert der einzelnen Variablen.  Außerdem werden ggf. Schließvariablen angezeigt.  Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.  Wenn Sie in einer Codezeile nicht anhalten, ist der **Bereich** Bereich leer.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Der Bereich Bereich" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Der **Bereich Bereich**  
:::image-end:::  

### <a name="method-2-watch-expressions"></a>Methode 2: Watch Expressions  

Im **Bereich Überwachungsausdrücke** können Sie die Werte von Variablen im Laufe der Zeit überwachen.  Wie der Name schon sagt, **sind Watch Expressions** nicht auf Variablen beschränkt.  Sie können einen beliebigen gültigen JavaScript-Ausdruck in einem **Watch Expression speichern.**  Versuchen Sie es jetzt.  

1.  Wählen Sie den **Bereich "Beobachten"** aus.  
1.  Wählen **Sie Ausdruck hinzufügen** \( Ausdruck hinzufügen ![ ][ImageAddIcon] \).  
1.  Geben Sie `typeof sum` ein.  
1.  Wählen Sie `Enter` aus.  DevTools zeigt `typeof sum: "string"` .  Der Wert rechts neben dem Doppelpunkt ist das Ergebnis Ihres Watch Expression.  
    
> [!NOTE]
> Im Bereich **"Uhrausdruck"** \(unten rechts\) in der folgenden Abbildung wird der `typeof sum` Watch Expression angezeigt.  Wenn Ihr DevTools-Fenster groß ist, befindet sich der Bereich **"Watch Expression"** rechts über dem **Bereich Ereignislistener-Haltepunkte.**  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Der Bereich "Watch Expression"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Der **Bereich "Watch Expression"**  
:::image-end:::  

Wie verdächtig, `sum` wird als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.  Sie haben nun bestätigt, dass der Werttyp die Ursache des Fehlers ist.  

### <a name="method-3-the-console"></a>Methode 3: Die Konsole  

Mit **der Konsole** können Sie Nachrichten anzeigen und sie auch verwenden, um beliebige `console.log()` JavaScript-Anweisungen auszuwerten.  Zum Debuggen können Sie die **Konsole** verwenden, um potenzielle Fehlerbehebungen auf Fehler zu testen.  Versuchen Sie es jetzt.  

1.  Wenn das **Konsolentool** geschlossen ist, wählen Sie `Escape` es aus, um es zu öffnen.  Das **Konsolentool** wird im unteren Bereich des DevTools-Fensters geöffnet.  
1.  Geben Sie **in der Konsole** `parseInt(addend1) + parseInt(addend2)` ein.  Die Anweisung, mit der das Tool in einer Codezeile angehalten wird, in `addend1` der sich der Bereich `addend2` befindet.  
1.  Wählen Sie `Enter` aus.  DevTools wertet die Anweisung aus und druckt , was das Ergebnis ist, das Sie von `6` der Demo erwarten.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Das Konsolentool nach der Auswertung von parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       Das **Konsolentool** nach der Auswertung `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a>Schritt 7: Anwenden einer Korrektur  

Wenn Sie eine Fehlerbehebung für den Fehler finden, versuchen Sie es, indem Sie den Code bearbeiten und die Demo erneut ausführen.  Sie können JavaScript-Code direkt in der DevTools-Benutzeroberfläche bearbeiten und die Korrektur anwenden.  Versuchen Sie es jetzt.  

1.  Wählen **Sie Skriptausführung fortsetzen** \( ![ Skriptausführung fortsetzen ][ImageResumeIcon] \).  
1.  Ersetzen Sie **im Code-Editor**Zeile 32 durch `var sum = addend1 + addend2` `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um Ihre Änderung zu speichern.  
1.  Wählen **Sie Haltepunkte deaktivieren** \( ![ Haltepunkte deaktivieren ][ImageDeactivateIcon] \).  Es ändert sich blau, um anzugeben, dass die Option aktiv ist.  Während **Die Haltepunkte deaktivieren** festgelegt ist, ignoriert DevTools alle von Ihnen festgelegten Haltepunkte.  
1.  Testen Sie die Demo mit unterschiedlichen Werten.  Die Demo wird nun korrekt berechnet.  
    
> [!CAUTION]
> Dieser Workflow wendet nur eine Korrektur auf den Code an, der in Ihrem Browser ausgeführt wird.  Der Code für alle Benutzer, die Ihre Webseite besuchen, wird nicht behoben.  Dazu müssen Sie den Code auf Ihren Servern beheben.  

## <a name="next-steps"></a>Nächste Schritte  

Herzlichen Glückwunsch!  Sie wissen nun, wie Sie Microsoft Edge DevTools beim Debuggen von JavaScript nutzen können.  Die Tools und Methoden, die Sie in diesem Artikel gelernt haben, können Ihnen unzählige Stunden sparen.  

In diesem Artikel wurden Ihnen nur zwei Methoden zum Festlegen von Haltepunkten erläutert.  DevTools bietet viele andere Möglichkeiten, einschließlich der folgenden Einstellungen.  

*   Bedingte Haltepunkte, die nur ausgelöst werden, wenn die bedingung, die Sie bereitstellen, true ist.  
*   Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen.  
*   XHR-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen angegebenen Teilzeichenfolge entspricht.  
    
Weitere Informationen zur Verwendung der einzelnen Typen finden Sie unter [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].  

Einige Codeschrittsteuerelemente werden in diesem Artikel nicht erläutert.  Weitere Informationen finden Sie unter [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Schritt durch Code – JavaScript-Debugreferenz | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Öffnen sie demo | Glitch"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
