---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um JavaScript-Fehler zu finden und zu beheben.
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325948"
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
# Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools  

In diesem Artikel lernen Sie den grundlegenden Workflow zum Debuggen von JavaScript-Problem in DevTools.  

## Schritt 1: Reproduzieren des Fehlers  

Das Suchen einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt beim Debuggen.  

1.  Wählen Sie **"Demo öffnen"** aus.  Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und öffnen Sie die Demo `Command` auf einer neuen Browserregisterkarte.  
    
    [Demo öffnen][OpenDebugJSDemo]  
    
1.  Geben `5` Sie in das Textfeld Zahl **1** ein.  
1.  Geben `1` Sie in das Textfeld Zahl **2** ein.  
1.  Wählen **Sie "Nummer 1 hinzufügen" und "Zahl 2" aus.**  Die Bezeichnung unterhalb der Schaltfläche steht `5 + 1 = 51` für .  Das Ergebnis sollte `6` .  Beheben Sie als Nächstes den Fehler beim Hinzuf?en, der der Fehler ist.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 ergibt 51, sollte aber 6 sein" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` führt zu `51` , sollte aber `6`  
    :::image-end:::  
    
## Schritt 2: Machen Sie sich mit der Benutzeroberfläche des Quellenbereichs vertraut  

DevTools bietet viele verschiedene Tools für verschiedene Aufgaben.  Zu den verschiedenen Aufgaben gehören das Ändern von CSS, das Laden von Profilingseiten und das Überwachen von Netzwerkanforderungen.  Im **Bereich** "Quellen" debuggen Sie JavaScript.  

1.  Öffnen Sie DevTools, indem `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) drücken.  Mit dieser Verknüpfung wird der **Konsolenbereich** geöffnet.  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Konsolenbereich" lightbox="../media/javascript-console-empty.msft.png":::
       Das **Konsolentool**  
    :::image-end:::  
    
1.  Wählen Sie das **Quellentool** aus.  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Bereich "Quellen"" lightbox="../media/javascript-sources-sections.msft.png":::
       Bereich **"Quellen"**  
    :::image-end:::  
    
Die **Benutzeroberfläche** des Quellenbereichs hat drei Teile.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Die drei Teile der Benutzeroberfläche des Quellenbereichs" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Die drei Teile der **Benutzeroberfläche** des Quellenbereichs  
:::image-end:::  

1.  Der **Dateinavigatorbereich** \(Abschnitt 1 in der vorherigen Abbildung\).  Jede Datei, die die Webseite anfordert, wird hier aufgelistet.  
1.  Der **Code-Editor-Bereich** \(Abschnitt 2 in der vorherigen Abbildung\).  Nachdem Sie eine Datei im **Bereich "Dateinavigator"** ausgewählt haben, wird der Inhalt dieser Datei hier angezeigt.  
1.  Der **JavaScript-Debugbereich** \(Abschnitt 3 in der vorherigen Abbildung\).  Verschiedene Tools zum Überprüfen des JavaScript für die Webseite.  Wenn ihr DevTools-Fenster breit ist, wird dieser Bereich rechts vom **Code-Editor-Bereich** angezeigt.  
    
## Schritt 3: Anhalten des Codes mit einem Haltepunkt  

Eine gängige Methode zum Debuggen dieser Art von Problem ist das Einfügen mehrerer Anweisungen in den Code und das anschließende Überprüfen von Werten während der Ausführung `console.log()` des Skripts.  Zum Beispiel:  

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

Die `console.log()` Methode kann die Aufgabe erledigen, **haltepunkte können** sie jedoch schneller erledigen.  Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.  Haltepunkte haben gegenüber der Methode einige `console.log()` Vorteile:  

*   With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.  Bei Haltepunkten können Sie den relevanten Code unterbrechen, ohne zu wissen, wie der Code strukturiert ist.  
*   In Ihren Anweisungen müssen Sie explizit jeden `console.log()` Wert angeben, den Sie überprüfen möchten.  Mit Haltepunkten zeigt DevTools die Werte aller Variablen zu diesem Zeitpunkt an.  Manchmal werden Variablen, die sich auf Ihren Code auswirken, ausgeblendet und verschleiert.  
    
Kurz gesagt, können Haltepunkte Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.  

Wenn Sie einen Schritt zurück gehen und sich Gedanken über die Funktionsweise der App machen, können Sie eine gebildete Ermutung treffen, dass die falsche Summe \( \) im Ereignislistener berechnet wird, der der Schaltfläche "Nummer 1 hinzufügen" und "Nummer `5 + 1 = 51` `click` **2"** zugeordnet ist.  Daher möchten Sie den Code wahrscheinlich zu dem Zeitpunkt anhalten, zu dem der `click` Listener ausgeführt wird.  **Mit Ereignislistener-Haltepunkten** können Sie genau dies tun:  

1.  Wählen Sie **im Bereich "JavaScript-Debuggen"** die **Option "Ereignislistener-Haltepunkte"** aus, um den Abschnitt zu erweitern.  DevTools zeigt eine Liste erweiterbarer Ereigniskategorien an, z. B. **Animation** und **Zwischenablage.**  
1.  Wählen Sie neben der **Kategorie "Mausereignis"** **"Erweitern** \( ![ Symbol "Erweitern" ][ImageExpandIcon] \) aus.  DevTools zeigt eine Liste von Mausereignissen an, z. B. **Klicken** **und Mousedown.**  Jedes Ereignis verfügt über ein Kontrollkästchen daneben.  
1.  Aktivieren Sie das Kontrollkästchen neben dem **Klicken.**  DevTools ist jetzt so eingerichtet, dass es automatisch angehalten wird, wenn ein `click` Ereignislistener ausgeführt wird.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Aktivieren Sie das Kontrollkästchen neben dem Klicken." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Aktivieren Sie das Kontrollkästchen neben dem **Klicken.**  
    :::image-end:::  
    
1.  Wählen Sie wieder auf der Demo **"Nummer 1" und "Nummer 2"** aus.  DevTools hält die Demo an und hebt eine Codezeile im **Quellenbereich** hervor.  DevTools sollten in Zeile 16 in angehalten `get-started.js` werden.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Wenn Sie in einer anderen Codezeile anhalten, drücken Sie **"Skriptausführung** fortsetzen\( Skriptausführung fortsetzen \) bis Sie in der richtigen ![ ][ImageResumeIcon] Zeile anhalten.  
    
    > [!NOTE]
    > Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browsererweiterung, die einen Ereignislistener auf jeder besuchten `click` Webseite registriert.  Sie wurden im Listener der Erweiterung `click` angehalten.  Wenn Sie den InPrivate-Modus verwenden, um **im privaten**Modus zu navigieren, wodurch alle Erweiterungen deaktiviert werden, sehen Sie möglicherweise, dass Sie jedes Mal in der gewünschten Codezeile anhalten.  

<!--todo: add inprivate section when available -->  

**Ereignislistener-Haltepunkte** sind nur einer von vielen Arten von Haltepunkten, die in DevTools verfügbar sind.  Merken Sie sich alle verschiedenen Typen, damit Sie unterschiedliche Szenarien so schnell wie möglich debuggen können.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Schritt 4: Schrittweises Durchschritten des Codes  

Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.  Schrittweises Durchschritten des Codes ermöglicht Es Ihnen, die Laufzeit ihres Codes zu durchschritten.  Sie werden durch eine Zeile nach der anderen gehen, um herauszufinden, wo Ihr Code in einer anderen Reihenfolge als erwartet ausgeführt wird.  Probieren Sie es jetzt aus:  

1.  Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  DevTools führt den folgenden Code aus, ohne ihn schrittweise zu verwenden.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools überspringt einige Codezeilen.  Dies liegt daran, dass der Codeblock für die Anweisung nicht als `inputsAreEmpty()` falsch `if` ausgewertet wird.  
    
1.  On the **Sources** panel of DevTools, choose **Step into next function call** \( Step into next function call ![ ][ImageIntoIcon] \) to step through the runtime of the `updateLabel()` function, one line at a time.  
    
Das Überprüfen einer Zeile nach der anderen ist die grundidee Idee, codeschritten zu werden.  Wenn Sie den Code in betrachten, sehen Sie, dass sich der Fehler wahrscheinlich an `get-started.js` einer anderen Stelle in der Funktion `updateLabel()` befindet.  Anstatt jede Codezeile zu durchschritten, können Sie einen anderen Haltepunkttyp verwenden, um den Code näher an der voraussichtlichen Stelle des Fehlers anzuhalten.  

## Schritt 5: Festlegen eines Codezeile-Haltepunkts  

Codelinien-Haltepunkte sind der am häufigsten verwendeten Haltepunkttyp.  Wenn Sie zu der bestimmten Codezeile kommen, die Sie anhalten möchten, verwenden Sie einen Codezeile-Haltepunkt.  

1.  Sehen Sie sich die letzte Codezeile `updateLabel()` in:  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  Auf der linken Seite wird die Nummer dieser bestimmten Codezeile als **34 angezeigt.**  Wählen Sie Zeile **34 aus.**  DevTools setzt links von **34**ein rotes Symbol.  Das rote Symbol gibt an, dass sich in dieser Zeile ein Codezeile-Haltepunkt befindet.  DevTools hält immer an, bevor diese Codezeile ausgeführt wird.  
1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  Das Skript wird weiterhin ausgeführt, bis es Die Zeile 33 erreicht.  In den Zeilen 31, 32 und 33 druckt DevTools die Werte von , und rechts neben dem `addend1` `addend2` `sum` Semikolon in jeder Zeile.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools hält am Codelinien-Haltepunkt in Zeile 34 an." lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools hält am Codelinien-Haltepunkt in Zeile 34 an.  
    :::image-end:::  
    
## Schritt 6: Überprüfen von Variablenwerten  

Die Werte von `addend1` , `addend2` und sehen `sum` verdächtig aus.  Die Werte sind in Anführungszeichen eingeschlossen.  Die Anführungszeichen bedeuten, dass der Wert eine Zeichenfolge ist. Dies ist eine gute Hypothese, um die Ursache des Fehlers zu erläutern.  Sammeln Sie weitere Informationen zur Situation.  DevTools bietet viele Tools zum Untersuchen von Variablenwerten.  

### Methode 1: Bereichsbereich  

Wenn Sie in einer Codezeile **** anhalten, werden im Bereichsbereich die lokalen und globalen Variablen angezeigt, die derzeit definiert sind, zusammen mit dem Wert jeder Variablen.  Außerdem werden ggf. Schließvariablen angezeigt.  Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.  Wenn Sie in einer Codezeile nicht anhalten, **ist** der Bereich leer.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Bereichsbereich" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   **Bereichsbereich**  
:::image-end:::  

### Methode 2: Ausdrücke ansehen  

Im **Bereich "Überwachungsausdrücke"** können Sie die Werte von Variablen im Laufe der Zeit überwachen.  Wie der Name schon sagt, sind **Watch Expressions** nicht auf Variablen beschränkt.  Sie können jeden gültigen JavaScript-Ausdruck in einem **Watch-Ausdruck speichern.**  Versuchen Sie es jetzt.  

1.  Wählen Sie den **Bereich "Watch"** aus.  
1.  Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).  
1.  Geben Sie `typeof sum` ein.  
1.  Wählen Sie `Enter` .  DevTools zeigt `typeof sum: "string"` .  Der Wert rechts neben dem Doppelpunkt ist das Ergebnis des Watch-Ausdrucks.  
    
> [!NOTE]
> Im Bereich **"Watch Expression"** (unten rechts\) in der folgenden Abbildung wird der Watch `typeof sum` Expression angezeigt.  Wenn ihr DevTools-Fenster groß ist, befindet sich der Bereich "Watch **Expression"** auf der rechten Seite über dem Bereich "Haltepunkte des Ereignislisteners". ****  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Der Bereich "Watch Expression"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Der **Bereich "Watch Expression"**  
:::image-end:::  

Wie verdächtig, `sum` wird sie als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.  Sie haben nun bestätigt, dass der Werttyp die Ursache des Fehlers ist.  

### Methode 3: Die Konsole  

Mit **der Konsole** können Sie Nachrichten anzeigen und sie auch zum `console.log()` Auswerten beliebiger JavaScript-Anweisungen verwenden.  Zum Debuggen können Sie die **Konsole** verwenden, um potenzielle Fehlerbehebungen zu testen.  Versuchen Sie es jetzt.  

1.  Wenn die **Konsolenschubschubte** geschlossen ist, wählen Sie `Escape` sie aus, um sie zu öffnen.  Die **** Konsolenschubschubleiste wird im unteren Bereich des Fensters DevTools geöffnet.  
1.  Geben Sie in **der Konsole**den Text `parseInt(addend1) + parseInt(addend2)` ein.  Die Anweisung, mit der das Tool in einer Codezeile angehalten wird, in der sich der Bereich `addend1` `addend2` befindet.  
1.  Wählen Sie `Enter` .  DevTools wertet die Anweisung aus und druckt , was das Ergebnis ist, das Sie von `6` der Demo erwarten.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Die Konsolenschubschubte nach der Auswertung von parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       Die **Konsolenschubschubte** nach der Auswertung `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Schritt 7: Anwenden eines Fixs  

Wenn Sie einen Fix für den Fehler finden, probieren Sie Ihre Korrektur aus, indem Sie den Code bearbeiten und die Demo erneut ausführen.  Sie können JavaScript-Code direkt in der DevTools-Benutzeroberfläche bearbeiten und den Fix anwenden.  Versuchen Sie es jetzt.  

1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  
1.  Ersetzen Sie **im Code-Editor**Zeile 32 `var sum = addend1 + addend2` durch `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um Ihre Änderung zu speichern.  
1.  Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).  Es ändert sich blau, um anzugeben, dass die Option aktiv ist.  Während **Haltepunkte deaktiviert sind,** ignoriert DevTools alle von Ihnen festgelegten Haltepunkte.  
1.  Testen Sie die Demo mit unterschiedlichen Werten.  Die Demo wird nun korrekt berechnet.  
    
> [!CAUTION]
> Dieser Workflow wendet nur eine Korrektur auf den Code an, der in Ihrem Browser ausgeführt wird.  Der Code für alle Benutzer, die Ihre Webseite besuchen, wird nicht korrigiert.  Dazu müssen Sie den Code auf den Servern korrigieren.  

## Nächste Schritte  

Herzlichen Glückwunsch!  Sie wissen nun, wie Sie Microsoft Edge DevTools beim Debuggen von JavaScript nutzen.  Die Tools und Methoden, die Sie in diesem Artikel gelernt haben, können Stunden sparen.  

In diesem Artikel wurden ihnen nur zwei Methoden zum Festlegen von Haltepunkten erläutert.  DevTools bietet viele weitere Möglichkeiten, einschließlich der folgenden Einstellungen.  

*   Bedingte Haltepunkte, die nur ausgelöst werden, wenn die bedingung, die Sie bereitstellen, wahr ist.  
*   Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen.  
*   XHR-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen angegebenen Teilzeichenfolge entspricht.  
    
Weitere Informationen dazu, wann und wie Sie die einzelnen Typen verwenden, finden Sie unter ["Ihren Code mit Haltepunkten anhalten".][DevtoolsJavscriptBreakpoints]  

Einige Steuerelemente für die Codeschritte werden in diesem Artikel nicht erläutert.  Weitere Informationen finden Sie unter ["Schritt über Codezeile".][DevtoolsJavascriptReferenceStepThroughCode]  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Schritt-für-Schritt-Code – JavaScript-Debugreferenz-| Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Öffnen der Demo-| Glitch"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Baskisch][KayceBasques] \(Technical Writer, Chrome DevTools \& Vorsteller\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
