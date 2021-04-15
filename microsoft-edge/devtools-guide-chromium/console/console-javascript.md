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
# <a name="the-console-as-a-javascript-environment"></a><span data-ttu-id="42517-104">Die Konsole als JavaScript-Umgebung</span><span class="sxs-lookup"><span data-stu-id="42517-104">The Console as a JavaScript environment</span></span>  

<span data-ttu-id="42517-105">Das **Konsolentool** im Browser DevTools ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="42517-105">The **Console** tool inside the browser DevTools is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="42517-106">Das bedeutet, dass Sie ein beliebiges JavaScript in der **Konsole schreiben können, das** sofort ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42517-106">It means that you may write any JavaScript in the **Console** that runs immediately.</span></span>

<span data-ttu-id="42517-107">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="42517-107">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="42517-108">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="42517-108">Open the **Console**.</span></span>  
    *   <span data-ttu-id="42517-109">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="42517-109">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="42517-110">Geben Sie `2 + 2` ein.</span><span class="sxs-lookup"><span data-stu-id="42517-110">Type `2 + 2`.</span></span>  <span data-ttu-id="42517-111">Die **Konsole** zeigt das Ergebnis bereits `4` in der nächsten Zeile an, während Sie es eingeben.</span><span class="sxs-lookup"><span data-stu-id="42517-111">The **Console** already displays the result `4` on the next line while you type it.</span></span>  <span data-ttu-id="42517-112">Mit `Eager evaluation` dem Feature können Sie gültiges JavaScript schreiben.</span><span class="sxs-lookup"><span data-stu-id="42517-112">The `Eager evaluation` feature helps you write valid JavaScript.</span></span>  <span data-ttu-id="42517-113">Es zeigt das Ergebnis an, während Sie eingeben, ob es falsch ist oder ob ein gültiges Ergebnis vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="42517-113">It displays the result while you type whether it's wrong or if a valid result exists.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Konsole zeigt das Ergebnis von 2 + 2 live an, während Sie es eingeben" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="42517-115">**Konsole** zeigt das Ergebnis von `2 + 2` live an, während Sie es eingeben</span><span class="sxs-lookup"><span data-stu-id="42517-115">**Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="42517-116">Wenn Sie `Enter` auswählen, führt **die Konsole** den Befehl JavaScript aus, gibt Ihnen das Ergebnis und ermöglicht Ihnen das Schreiben des nächsten Befehls.</span><span class="sxs-lookup"><span data-stu-id="42517-116">If you select `Enter`, the **Console** runs the JavaScript command, gives you the result, and allows you to write the next command.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ausführen mehrerer JavaScript-Ausdrücke nacheinander" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="42517-118">Ausführen mehrerer JavaScript-Ausdrücke nacheinander</span><span class="sxs-lookup"><span data-stu-id="42517-118">Run several JavaScript expressions in succession</span></span>  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a><span data-ttu-id="42517-119">AutoCompletion zum Schreiben komplexer Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42517-119">Autocompletion to write complex expressions</span></span>

<span data-ttu-id="42517-120">Das letzte Beispiel mag beängstigend wirken, aber die **Konsole** hilft Ihnen, komplexes JavaScript mithilfe einer hervorragenden AutoCompletion-Funktion zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="42517-120">The last example may seem scary, but the **Console** helps you write complex JavaScript using an excellent autocompletion feature.</span></span>  <span data-ttu-id="42517-121">Dieses Feature ist eine hervorragende Möglichkeit, um mehr über Methoden zu erfahren, die Sie vorher nicht kannten.</span><span class="sxs-lookup"><span data-stu-id="42517-121">This feature is a great way to learn about methods you didn't know before.</span></span>  

<span data-ttu-id="42517-122">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="42517-122">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="42517-123">Geben Sie `doc` ein.</span><span class="sxs-lookup"><span data-stu-id="42517-123">Type `doc`.</span></span>  
1.  <span data-ttu-id="42517-124">Wählen `document` Sie aus dem Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="42517-124">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="42517-125">Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="42517-125">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="42517-126">Geben Sie `.bo` ein.</span><span class="sxs-lookup"><span data-stu-id="42517-126">Type `.bo`.</span></span>  
1.  <span data-ttu-id="42517-127">Wählen `tab` Sie aus, um `document.body` zu erhalten .</span><span class="sxs-lookup"><span data-stu-id="42517-127">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="42517-128">Geben Sie einen anderen ein, um eine große Liste möglicher Eigenschaften und Methoden zu erhalten, die im `.` Textkörper der aktuellen Webseite verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="42517-128">Type another `.` to get a large list of possible properties and methods available on the body of the current webpage.</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Konsolenautocompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="42517-130">\*\*\*\* Konsolenautocompletion von JavaScript-Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="42517-130">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="console-history"></a><span data-ttu-id="42517-131">Konsolenverlauf</span><span class="sxs-lookup"><span data-stu-id="42517-131">Console history</span></span>

<span data-ttu-id="42517-132">Wie bei vielen anderen Befehlszeilenerfahrungen verfügen Sie auch über einen Verlauf von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="42517-132">As with many other command-line experiences, you also have a history of commands.</span></span>  <span data-ttu-id="42517-133">Wählen `Arrow Up` Sie diese Option aus, um die zuvor eingegebenen Befehle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="42517-133">Select `Arrow Up` to display the commands you entered before.</span></span>  <span data-ttu-id="42517-134">Die AutoCompletion behält auch einen Verlauf der Befehle bei, die Sie zuvor eingeben.</span><span class="sxs-lookup"><span data-stu-id="42517-134">Autocompletion also keeps a history of the commands you previously typed.</span></span>  <span data-ttu-id="42517-135">Sie können die ersten Buchstaben früherer Befehle eingeben, und Ihre vorherigen Auswahlmöglichkeiten werden in einem Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42517-135">You may type the first few letters of earlier commands and your previous choices display in a textbox.</span></span>  

<span data-ttu-id="42517-136">Darüber hinaus bietet **die Konsole** auch zahlreiche [Hilfsmethoden,][DevtoolsConsoleUtilities] die Ihnen das Leben erleichtern.</span><span class="sxs-lookup"><span data-stu-id="42517-136">Also, the **Console** also offers quite a few [utility methods][DevtoolsConsoleUtilities] that make your life easier.</span></span>  <span data-ttu-id="42517-137">Enthält z. `$_` B. immer das Ergebnis des letzten Ausdrucks, den Sie in der Konsole **verwendet haben.**</span><span class="sxs-lookup"><span data-stu-id="42517-137">For example, `$_` always contains the result of the last expression you ran in the **Console**.</span></span>

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="Der $_-Ausdruck in der Konsole enthält immer das letzte Ergebnis." lightbox="../media/console-javascript-console-history.msft.png":::
    <span data-ttu-id="42517-139">Der `$_` Ausdruck in der **Konsole** enthält immer das letzte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="42517-139">The `$_` expression in the **Console** always contains the last result</span></span>  
:::image-end:::  

## <a name="multiline-edits"></a><span data-ttu-id="42517-140">Mehrstufige Bearbeitungen</span><span class="sxs-lookup"><span data-stu-id="42517-140">Multiline edits</span></span>

<span data-ttu-id="42517-141">Standardmäßig gibt ihnen **die Konsole** nur eine Zeile, um Ihren JavaScript-Ausdruck zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="42517-141">By default, the **Console** only gives you one line to write your JavaScript expression.</span></span>  <span data-ttu-id="42517-142">Sie code wird ausgeführt, wenn Sie auswählen `Enter` .</span><span class="sxs-lookup"><span data-stu-id="42517-142">You code runs when you select `Enter`.</span></span> <span data-ttu-id="42517-143">Die Einschränkung einer Zeile kann Sie frustrieren.</span><span class="sxs-lookup"><span data-stu-id="42517-143">The one line limitation may frustrate you.</span></span>  <span data-ttu-id="42517-144">Wählen Sie anstelle von aus, um die Einschränkung einer Zeile `Shift` + `Enter` zu `Enter` umgehen.</span><span class="sxs-lookup"><span data-stu-id="42517-144">To work around the one line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="42517-145">Im folgenden Beispiel ist der angezeigte Wert das Ergebnis aller Zeilen, die in der Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42517-145">In the following example, the value displayed is the result of all the lines run in order.</span></span>  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Wählen Sie Umschalt+Eingabe aus, um mehrere Zeilen JavaScript zu schreiben, und der resultierende Wert wird in der Reihenfolge ausgeführt." lightbox="../media/console-javascript-multiline.msft.png":::
   <span data-ttu-id="42517-147">Wählen `Shift` + `Enter` Sie diese Option aus, um mehrere Zeilen JavaScript zu schreiben, und der resultierende Wert wird in der Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42517-147">Select `Shift`+`Enter` to write several lines of JavaScript and the resulting value is run in order</span></span>  
:::image-end:::  

<span data-ttu-id="42517-148">Wenn Sie eine mehrstufige Anweisung in der **Konsole starten,** wird sie automatisch erkannt und eingezogen.</span><span class="sxs-lookup"><span data-stu-id="42517-148">If you start a multiline statement in the **Console**, it gets automatically recognized and indented.</span></span>  <span data-ttu-id="42517-149">Wenn Sie z. B. eine Block-Anweisung mit einer geschweiften Klammer starten.</span><span class="sxs-lookup"><span data-stu-id="42517-149">For example, if you start a block statement with a curly brace.</span></span>  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="Konsole erkennt bereits mehrere Ausdrücke mit geschweiften Geschweiften und Einzugslinien für Sie" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    <span data-ttu-id="42517-151">**Konsole** erkennt bereits mehrere Ausdrücke mit geschweiften Geschweiften und Einzugslinien für Sie</span><span class="sxs-lookup"><span data-stu-id="42517-151">**Console** already recognizes multiline expressions using curly braces and indents each for you</span></span>  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a><span data-ttu-id="42517-152">Netzwerkanforderungen mit await() auf oberster Ebene</span><span class="sxs-lookup"><span data-stu-id="42517-152">Network requests using top-level await()</span></span>  

<span data-ttu-id="42517-153">Anders als in Ihren eigenen Skripts unterstützt **Konsole** die oberste Ebene [await,][GithubTc39ProposalTopLevelAwait] um beliebige asynchrones JavaScript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="42517-153">Other than in your own scripts, **Console** supports [top level await][GithubTc39ProposalTopLevelAwait] to run arbitrary asynchronous JavaScript in it.</span></span>  <span data-ttu-id="42517-154">Verwenden Sie beispielsweise die `fetch` API, ohne die `await` Anweisung mit einer asynchronen Funktion umbrechen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="42517-154">For example, use the `fetch` API without wrapping the `await` statement with an async function.</span></span>  

<span data-ttu-id="42517-155">Führen Sie die folgenden Aktionen aus, um die letzten 50 Probleme zu erhalten, die im [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub-Repository eingereicht wurden.</span><span class="sxs-lookup"><span data-stu-id="42517-155">To get the last 50 issues filed on the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub repo, complete the following actions.</span></span>  

1.  <span data-ttu-id="42517-156">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="42517-156">Open the **Console**.</span></span>  
1.  <span data-ttu-id="42517-157">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein, um ein Objekt mit 10 Einträgen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="42517-157">Copy and paste the following code snippet to get an object that contains 10 entries.</span></span>  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="Konsole zeigt das Ergebnis einer asynchronen Abrufanforderung auf oberster Ebene an" lightbox="../media/console-javascript-top-level-await.msft.png":::
    <span data-ttu-id="42517-159">**Konsole** zeigt das Ergebnis einer asynchronen Anforderung auf oberster `fetch` Ebene an</span><span class="sxs-lookup"><span data-stu-id="42517-159">**Console** displays the result of a top-level async `fetch` request</span></span>  
:::image-end:::  

<span data-ttu-id="42517-160">Die 10 Einträge sind schwer zu erkennen, da viele Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42517-160">The 10 entries are hard to recognize, since a lot of information is displayed.</span></span>  <span data-ttu-id="42517-161">Zum Glück können Sie die Protokollmethode verwenden, um nur die Informationen zu erhalten, an denen `console.table()` Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="42517-161">Luckily enough, you may use the `console.table()` log method to only receive the information in which you're interested.</span></span>  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Anzeigen des letzten Ergebnisses in einem lesbaren Format für den Menschen mithilfe von console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    <span data-ttu-id="42517-163">Anzeigen des letzten Ergebnisses in einem lesbaren Format mit</span><span class="sxs-lookup"><span data-stu-id="42517-163">Display the last result in a human readable format using</span></span> `console.table`  
:::image-end:::  

<span data-ttu-id="42517-164">Um die von einem Ausdruck zurückgegebenen Daten wiederzuverwenden, können Sie die `copy()` Hilfsmethode der **Konsole verwenden.**</span><span class="sxs-lookup"><span data-stu-id="42517-164">To reuse the data returned from an expression, you may use the `copy()` utility method of the **Console**.</span></span>  <span data-ttu-id="42517-165">Der folgende Codeausschnitt sendet die Anforderung und kopiert die Daten aus der Antwort an die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="42517-165">The following code snippet sends the request and copies the data from the response to the clipboard.</span></span>  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

<span data-ttu-id="42517-166">Verwenden Sie **die Konsole** als hervorragende Möglichkeit, die JavaScript-Funktionalität zu verwenden und einige schnelle Berechnungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="42517-166">Use the **Console** as a great way to practice JavaScript functionality and to do some quick calculations.</span></span>  <span data-ttu-id="42517-167">Die eigentliche Leistung liegt in der Tatsache, dass Sie Zugriff auf das [Fensterobjekt][MdnDocsWebApiWindow] haben.</span><span class="sxs-lookup"><span data-stu-id="42517-167">The real power is the fact that you have access to the [window][MdnDocsWebApiWindow] object.</span></span>  <span data-ttu-id="42517-168">Sie können [mit dem DOM in der Konsole interagieren.][DevtoolsConsoleConsoleDomInteraction]</span><span class="sxs-lookup"><span data-stu-id="42517-168">You may [interact with the DOM in Console][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="42517-169">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="42517-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Verwenden der Konsole für die Interaktion mit der DOM-| Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "ECMAScript-Vorschlag: Warten auf oberster Ebene – tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-| Wikipedia"  
