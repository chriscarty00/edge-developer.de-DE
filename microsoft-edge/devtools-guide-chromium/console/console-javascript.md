---
description: Eine Einführung in die Verwendung des Konsolentools innerhalb der Microsoft Edge Developer Tools als JavaScript-Umgebung.
title: Die Konsole als JavaScript-Umgebung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, Web development, f12 tools, devtools
ms.openlocfilehash: f75ac6d728c9a69542b2f58df85248759267f76d
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483474"
---
# <a name="the-console-as-a-javascript-environment"></a>Die Konsole als JavaScript-Umgebung  

Das **Konsolentool** im Browser DevTools ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]  Das bedeutet, dass Sie ein beliebiges JavaScript in der **Konsole schreiben können, das** sofort ausgeführt wird.

Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Öffnen Sie die **Konsole**.  
    *   Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  
1.  Geben Sie `2 + 2` ein.  Die **Konsole** zeigt das Ergebnis bereits `4` in der nächsten Zeile an, während Sie es eingeben.  Mit `Eager evaluation` dem Feature können Sie gültiges JavaScript schreiben.  Es zeigt das Ergebnis an, während Sie eingeben, ob es falsch ist oder ob ein gültiges Ergebnis vorhanden ist.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Konsole zeigt das Ergebnis von 2 + 2 live an, während Sie es eingeben" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   **Konsole** zeigt das Ergebnis von `2 + 2` live an, während Sie es eingeben  
:::image-end:::  

Wenn Sie `Enter` auswählen, führt **die Konsole** den Befehl JavaScript aus, gibt Ihnen das Ergebnis und ermöglicht Ihnen das Schreiben des nächsten Befehls.  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ausführen mehrerer JavaScript-Ausdrücke nacheinander" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Ausführen mehrerer JavaScript-Ausdrücke nacheinander  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a>AutoCompletion zum Schreiben komplexer Ausdrücke

Das letzte Beispiel mag beängstigend wirken, aber die **Konsole** hilft Ihnen, komplexes JavaScript mithilfe einer hervorragenden AutoCompletion-Funktion zu schreiben.  Dieses Feature ist eine hervorragende Möglichkeit, um mehr über Methoden zu erfahren, die Sie vorher nicht kannten.  

Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Geben Sie `doc` ein.  
1.  Wählen `document` Sie aus dem Dropdownmenü aus.  
1.  Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.  
1.  Geben Sie `.bo` ein.  
1.  Wählen `tab` Sie aus, um `document.body` zu erhalten .  
1.  Geben Sie einen anderen ein, um eine große Liste möglicher Eigenschaften und Methoden zu erhalten, die im `.` Textkörper der aktuellen Webseite verfügbar sind.  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Konsolenautocompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **** Konsolenautocompletion von JavaScript-Ausdrücken  
:::image-end:::  

## <a name="console-history"></a>Konsolenverlauf

Wie bei vielen anderen Befehlszeilenerfahrungen verfügen Sie auch über einen Verlauf von Befehlen.  Wählen `Arrow Up` Sie diese Option aus, um die zuvor eingegebenen Befehle anzuzeigen.  Die AutoCompletion behält auch einen Verlauf der Befehle bei, die Sie zuvor eingeben.  Sie können die ersten Buchstaben früherer Befehle eingeben, und Ihre vorherigen Auswahlmöglichkeiten werden in einem Textfeld angezeigt.  

Darüber hinaus bietet **die Konsole** auch zahlreiche [Hilfsmethoden,][DevtoolsConsoleUtilities] die Ihnen das Leben erleichtern.  Enthält z. `$_` B. immer das Ergebnis des letzten Ausdrucks, den Sie in der Konsole **verwendet haben.**

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="Der $_-Ausdruck in der Konsole enthält immer das letzte Ergebnis." lightbox="../media/console-javascript-console-history.msft.png":::
    Der `$_` Ausdruck in der **Konsole** enthält immer das letzte Ergebnis.  
:::image-end:::  

## <a name="multiline-edits"></a>Mehrstufige Bearbeitungen

Standardmäßig gibt ihnen **die Konsole** nur eine Zeile, um Ihren JavaScript-Ausdruck zu schreiben.  Sie code wird ausgeführt, wenn Sie auswählen `Enter` . Die Einschränkung einer Zeile kann Sie frustrieren.  Wählen Sie anstelle von aus, um die Einschränkung einer Zeile `Shift` + `Enter` zu `Enter` umgehen.  Im folgenden Beispiel ist der angezeigte Wert das Ergebnis aller Zeilen, die in der Reihenfolge ausgeführt werden.  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Wählen Sie Umschalt+Eingabe aus, um mehrere Zeilen JavaScript zu schreiben, und der resultierende Wert wird in der Reihenfolge ausgeführt." lightbox="../media/console-javascript-multiline.msft.png":::
   Wählen `Shift` + `Enter` Sie diese Option aus, um mehrere Zeilen JavaScript zu schreiben, und der resultierende Wert wird in der Reihenfolge ausgeführt.  
:::image-end:::  

Wenn Sie eine mehrstufige Anweisung in der **Konsole starten,** wird sie automatisch erkannt und eingezogen.  Wenn Sie z. B. eine Block-Anweisung mit einer geschweiften Klammer starten.  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="Konsole erkennt bereits mehrere Ausdrücke mit geschweiften Geschweiften und Einzugslinien für Sie" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    **Konsole** erkennt bereits mehrere Ausdrücke mit geschweiften Geschweiften und Einzugslinien für Sie  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a>Netzwerkanforderungen mit await() auf oberster Ebene  

Anders als in Ihren eigenen Skripts unterstützt **Konsole** die oberste Ebene [await,][GithubTc39ProposalTopLevelAwait] um beliebige asynchrones JavaScript auszuführen.  Verwenden Sie beispielsweise die `fetch` API, ohne die `await` Anweisung mit einer asynchronen Funktion umbrechen zu müssen.  

Führen Sie die folgenden Aktionen aus, um die letzten 50 Probleme zu erhalten, die im [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub-Repository eingereicht wurden.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein, um ein Objekt mit 10 Einträgen zu erhalten.  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="Konsole zeigt das Ergebnis einer asynchronen Abrufanforderung auf oberster Ebene an" lightbox="../media/console-javascript-top-level-await.msft.png":::
    **Konsole** zeigt das Ergebnis einer asynchronen Anforderung auf oberster `fetch` Ebene an  
:::image-end:::  

Die 10 Einträge sind schwer zu erkennen, da viele Informationen angezeigt werden.  Zum Glück können Sie die Protokollmethode verwenden, um nur die Informationen zu erhalten, an denen `console.table()` Sie interessiert sind.  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Anzeigen des letzten Ergebnisses in einem lesbaren Format für den Menschen mithilfe von console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    Anzeigen des letzten Ergebnisses in einem lesbaren Format mit `console.table`  
:::image-end:::  

Um die von einem Ausdruck zurückgegebenen Daten wiederzuverwenden, können Sie die `copy()` Hilfsmethode der **Konsole verwenden.**  Der folgende Codeausschnitt sendet die Anforderung und kopiert die Daten aus der Antwort an die Zwischenablage.  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

Verwenden Sie **die Konsole** als hervorragende Möglichkeit, die JavaScript-Funktionalität zu verwenden und einige schnelle Berechnungen durchzuführen.  Die eigentliche Leistung liegt in der Tatsache, dass Sie Zugriff auf das [Fensterobjekt][MdnDocsWebApiWindow] haben.  Sie können [mit dem DOM in der Konsole interagieren.][DevtoolsConsoleConsoleDomInteraction]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Verwenden der Konsole für die Interaktion mit der DOM-| Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "ECMAScript-Vorschlag: Warten auf oberster Ebene – tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-| Wikipedia"  
