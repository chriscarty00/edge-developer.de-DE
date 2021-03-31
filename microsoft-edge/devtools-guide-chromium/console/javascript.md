---
description: Erfahren Sie, wie Sie JavaScript in der Konsole ausführen.
title: Erste Schritte mit der Ausführung von JavaScript in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398819"
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

# <a name="get-started-with-running-javascript-in-the-console"></a><span data-ttu-id="96444-104">Erste Schritte mit der Ausführung von JavaScript in der Konsole</span><span class="sxs-lookup"><span data-stu-id="96444-104">Get started with running JavaScript in the Console</span></span>  

<span data-ttu-id="96444-105">In diesem interaktiven Lernprogramm wird gezeigt, wie Sie JavaScript in der Microsoft Edge DevTools-Konsole **ausführen.**</span><span class="sxs-lookup"><span data-stu-id="96444-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="96444-106">Weitere Informationen zum Protokollieren von Nachrichten an der **Konsole**finden Sie unter Erste Schritte [mit protokollieren von Nachrichten.][DevToolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="96444-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="96444-107">Weitere Informationen zum Anhalten von JavaScript-Code und zum Schrittweisen Durchfahren des Codes in einer Zeile finden Sie unter Erste Schritte mit [Debuggen von JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="96444-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Die Konsole" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="96444-109">Die **Konsole**</span><span class="sxs-lookup"><span data-stu-id="96444-109">The **Console**</span></span>  
:::image-end:::  

## <a name="overview"></a><span data-ttu-id="96444-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="96444-110">Overview</span></span>  

<span data-ttu-id="96444-111">Die **Konsole** ist eine [REPL][WikiReadEvalPrintLoop], die für Read, Evaluate, Print und Loop steht.</span><span class="sxs-lookup"><span data-stu-id="96444-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="96444-112">Es liest das JavaScript, das Sie eingeben, wertet Den Code aus, druckt das Ergebnis Ihres Ausdrucks aus [und][2alityExpressionsVersusStatements]führt dann eine Schleife zurück zum ersten Schritt.</span><span class="sxs-lookup"><span data-stu-id="96444-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <a name="set-up-devtools"></a><span data-ttu-id="96444-113">Einrichten von DevTools</span><span class="sxs-lookup"><span data-stu-id="96444-113">Set up DevTools</span></span>  

<span data-ttu-id="96444-114">Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.</span><span class="sxs-lookup"><span data-stu-id="96444-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="96444-115">Wenn Sie physisch folgen, werden Sie sich die Workflows wahrscheinlich später merken.</span><span class="sxs-lookup"><span data-stu-id="96444-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="96444-116">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um die Konsole **zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="96444-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="96444-117">Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **Javascript-Beispiel** für Konsole aus, um in einem neuen Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="96444-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="96444-118">Beispiel für JavaScript für konsolen</span><span class="sxs-lookup"><span data-stu-id="96444-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Die Seite Konsolen-JavaScript-Beispiel links und DevTools auf der rechten Seite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="96444-120">Die Seite "Konsolen-JavaScript-Beispiel" links und DevTools auf der rechten Seite</span><span class="sxs-lookup"><span data-stu-id="96444-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a><span data-ttu-id="96444-121">Anzeigen und Ändern des JavaScript oder DOM der Seite</span><span class="sxs-lookup"><span data-stu-id="96444-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="96444-122">Beim Erstellen oder Debuggen einer Seite ist es  häufig hilfreich, Anweisungen in der Konsole auszuführen, um das Aussehen oder die Ausführung der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96444-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="96444-123">Beachten Sie den Text auf der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="96444-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="96444-124">Geben `document.getElementById('hello').textContent = 'Hello, Console!'` Sie in die **Konsole** ein, und wählen Sie dann `Enter` aus, um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="96444-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="96444-125">Beachten Sie, wie sich der Text innerhalb der Schaltfläche ändert.</span><span class="sxs-lookup"><span data-stu-id="96444-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aussehen der Konsole nach der Auswertung des Ausdrucks" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="96444-127">Aussehen der **Konsole** nach der Auswertung des Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="96444-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    `"Hello, Console!"`<span data-ttu-id="96444-128">, wird unterhalb des von Ihnen ausgewerteten Codes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96444-128">, is displayed below the code that you evaluated.</span></span>  <span data-ttu-id="96444-129">Denken Sie an die 4 Schritte von REPL: Lesen, Auswerten, Drucken, Schleifen.</span><span class="sxs-lookup"><span data-stu-id="96444-129">Remember the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="96444-130">Nach der Auswertung des Codes druckt eine REPL das Ergebnis des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="96444-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="96444-131">Dies `"Hello, Console!"` muss das Ergebnis der Auswertung `document.getElementById('hello').textContent = 'Hello, Console!'` sein.</span><span class="sxs-lookup"><span data-stu-id="96444-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a><span data-ttu-id="96444-132">Ausführen von beliebigem JavaScript, das nicht mit der Seite in Zusammenhang steht</span><span class="sxs-lookup"><span data-stu-id="96444-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="96444-133">Manchmal möchten Sie nur einen Codespielplatz, in dem Sie Code testen oder neue JavaScript-Features ausprobieren können, mit denen Sie nicht vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="96444-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="96444-134">Die **Konsole** ist ein perfekter Ort für diese Art von Experimenten.</span><span class="sxs-lookup"><span data-stu-id="96444-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="96444-135">Geben `5 + 15` Sie in die Konsole ein, und wählen Sie `Enter` aus, um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="96444-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="96444-136">Die Konsole druckt das Ergebnis des Ausdrucks unter Ihrem Code aus.</span><span class="sxs-lookup"><span data-stu-id="96444-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="96444-137">In der folgenden Abbildung sollte ihre **Konsole** das Ergebnis nach der Auswertung des Ausdrucks anzeigen.</span><span class="sxs-lookup"><span data-stu-id="96444-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="96444-138">Geben Sie den folgenden Code in die **Konsole ein.**</span><span class="sxs-lookup"><span data-stu-id="96444-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="96444-139">Versuchen Sie, sie zeichen-für-zeichen- und nicht kopierend eintippen.</span><span class="sxs-lookup"><span data-stu-id="96444-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="96444-140">Wenn Sie mit der Syntax nicht vertraut sind, navigieren Sie, um Standardwerte `b=20` [für Funktionsargumente zu definieren.][Esma6DefaultParameterValues]</span><span class="sxs-lookup"><span data-stu-id="96444-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="96444-141">Führen Sie nun die Funktion aus, die Sie gerade definiert haben.</span><span class="sxs-lookup"><span data-stu-id="96444-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Die Konsole wird angezeigt, nachdem die Ausdrücke im Codeausschnitt ausgewertet wurden." lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="96444-143">Die **Konsole** wird angezeigt, nachdem die Ausdrücke im Codeausschnitt ausgewertet wurden.</span><span class="sxs-lookup"><span data-stu-id="96444-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="96444-144">wird ausgewertet, da, wenn die Funktion ohne ein zweites Argument aufgerufen `45` `add` wird, `b` standardmäßig auf `20` .</span><span class="sxs-lookup"><span data-stu-id="96444-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="96444-145">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="96444-145">Next steps</span></span>  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="96444-146">Mit DevTools können Sie ein Skript mitten in der Ausführung anhalten.</span><span class="sxs-lookup"><span data-stu-id="96444-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="96444-147">Während Sie angehalten sind, können  Sie die Konsole verwenden, um den Oder der Seite zu diesem Zeitpunkt ein- und `window` zu `DOM` ändern.</span><span class="sxs-lookup"><span data-stu-id="96444-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="96444-148">Der Workflow sorgt für einen leistungsstarken Debugworkflow.</span><span class="sxs-lookup"><span data-stu-id="96444-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="96444-149">Ein interaktives Lernprogramm finden Sie unter [Erste Schritte mit debuggen von JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="96444-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="96444-150">Die **Konsole** verfügt außerdem über eine Reihe von Komfortfunktionen, die die Interaktion mit einer Seite vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="96444-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="96444-151">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="96444-151">For example:</span></span>  

*   <span data-ttu-id="96444-152">Anstatt ein Element auszuwählen, geben `document.querySelector()` Sie `$()` ein .</span><span class="sxs-lookup"><span data-stu-id="96444-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="96444-153">Diese Syntax wird von jQuery inspiriert, ist aber nicht wirklich jQuery.</span><span class="sxs-lookup"><span data-stu-id="96444-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="96444-154">Es handelt sich lediglich um einen Alias für `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="96444-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="96444-155">legt effektiv einen Haltepunkt in der ersten Zeile dieser Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="96444-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="96444-156">gibt ein Array zurück, das die Schlüssel des angegebenen Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="96444-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="96444-157">Weitere Informationen zu den Komfortfunktionen finden Sie unter [Console Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="96444-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="96444-158">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="96444-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Konsolenreferenz | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Ausdrücke und Anweisungen in JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Standardparameterwerte - Erweiterte Parameterbehandlung - ECMAScript 6 – Neue Features: Übersicht & Vergleich"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Javascript-Beispiel für | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lese-eval-print-Schleife – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="96444-167">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96444-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96444-168">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/javascript) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="96444-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="96444-170">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96444-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
