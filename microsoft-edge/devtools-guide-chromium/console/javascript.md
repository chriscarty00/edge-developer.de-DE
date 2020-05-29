---
title: Erste Schritte mit der Ausführung von JavaScript in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601726"
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







# <span data-ttu-id="9135f-103">Erste Schritte mit der Ausführung von JavaScript in der Konsole</span><span class="sxs-lookup"><span data-stu-id="9135f-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="9135f-104">In diesem interaktiven Lernprogramm erfahren Sie, wie Sie JavaScript in der Microsoft Edge devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="9135f-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="9135f-105">Informationen zum Protokollieren von Nachrichten in der Konsole finden Sie unter [Erste Schritte mit der Protokollierung von Nachrichten][DevToolsConsoleLoggingMessages] .</span><span class="sxs-lookup"><span data-stu-id="9135f-105">See [Get Started With Logging Messages][DevToolsConsoleLoggingMessages] to learn how to log messages to the Console.</span></span>  <span data-ttu-id="9135f-106">Weitere Informationen finden Sie unter [Erste Schritte mit dem Debuggen von JavaScript][DevToolsJavascriptIndex] , um zu erfahren, wie Sie JavaScript-Code pausieren und eine Zeile gleichzeitig durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9135f-106">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] to learn how to pause JavaScript code and step through it one line at a time.</span></span>  

> ##### <span data-ttu-id="9135f-107">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="9135f-107">Figure 1</span></span>  
> <span data-ttu-id="9135f-108">Der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="9135f-108">The **Console**</span></span>  
> ![Der Konsole][ImageConsole]  

## <span data-ttu-id="9135f-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9135f-110">Overview</span></span>   

<span data-ttu-id="9135f-111">Die **Konsole** ist ein [repl][WikiReadEvalPrintLoop], das für Read, Evaluate, Print und Loop steht.</span><span class="sxs-lookup"><span data-stu-id="9135f-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="9135f-112">Sie liest das JavaScript ein, das Sie eingeben, wertet den Code aus, druckt das Ergebnis des [Ausdrucks][2alityExpressionsVersusStatements]aus und führt dann eine Schleife zurück zum ersten Schritt aus.</span><span class="sxs-lookup"><span data-stu-id="9135f-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="9135f-113">Einrichten von devtools</span><span class="sxs-lookup"><span data-stu-id="9135f-113">Set up DevTools</span></span>   

<span data-ttu-id="9135f-114">Dieses Lernprogramm wurde entwickelt, um die Demo zu öffnen und alle Workflows selbst zu testen.</span><span class="sxs-lookup"><span data-stu-id="9135f-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="9135f-115">Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.</span><span class="sxs-lookup"><span data-stu-id="9135f-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="9135f-116">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um die **Konsole**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9135f-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="9135f-117">Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **Konsolen-JavaScript-Beispiel** , um es in einem neuen Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9135f-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    [<span data-ttu-id="9135f-118">Beispiel für eine Konsolen-JavaScript</span><span class="sxs-lookup"><span data-stu-id="9135f-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    > ##### <span data-ttu-id="9135f-119">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="9135f-119">Figure 2</span></span>  
    > <span data-ttu-id="9135f-120">Die JavaScript-Beispielseite der Konsole Links und DevTools auf der rechten Seite</span><span class="sxs-lookup"><span data-stu-id="9135f-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    > ![Die JavaScript-Beispielseite der Konsole Links und DevTools auf der rechten Seite][ImageTutorialDevToolsJs]  

## <span data-ttu-id="9135f-122">Anzeigen und Ändern des JavaScript-oder Dom der Seite</span><span class="sxs-lookup"><span data-stu-id="9135f-122">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="9135f-123">Beim Erstellen oder Debuggen einer Seite ist es häufig hilfreich, Anweisungen in der **Konsole** auszuführen, um zu ändern, wie die Seite aussehen oder ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9135f-123">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="9135f-124">Beachten Sie den Text in der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9135f-124">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="9135f-125">Geben `document.getElementById('hello').textContent = 'Hello, Console!'` Sie die **Konsole** ein, und drücken Sie dann `Enter` , um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="9135f-125">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="9135f-126">Beachten Sie, wie sich der Text in der Schaltfläche ändert.</span><span class="sxs-lookup"><span data-stu-id="9135f-126">Notice how the text inside the button changes.</span></span>  
    
    > ##### <span data-ttu-id="9135f-127">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="9135f-127">Figure 3</span></span>  
    > <span data-ttu-id="9135f-128">So sieht die Konsole nach der Auswertung des Ausdrucks aus</span><span class="sxs-lookup"><span data-stu-id="9135f-128">How the Console looks after evaluating the expression</span></span>  
    > ![So sieht die Konsole nach der Auswertung des Ausdrucks aus][ImageConsoleAfterEvaluating]  
    
    <span data-ttu-id="9135f-130">Unter dem Code, den Sie ausgewertet haben, wird angezeigt `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="9135f-130">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="9135f-131">Rufen Sie die vier Schritte von repl: lesen, auswerten, drucken, Schleife zurück.</span><span class="sxs-lookup"><span data-stu-id="9135f-131">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="9135f-132">Nach dem Auswerten des Codes wird von einem repl das Ergebnis des Ausdrucks gedruckt.</span><span class="sxs-lookup"><span data-stu-id="9135f-132">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="9135f-133">Daher `"Hello, Console!"` muss das Ergebnis der Auswertung sein `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="9135f-133">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="9135f-134">Ausführen von beliebigem JavaScript, das nicht mit der Seite verbunden ist</span><span class="sxs-lookup"><span data-stu-id="9135f-134">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="9135f-135">Manchmal möchten Sie einfach nur einen Code-Spielplatz, in dem Sie einige Codes testen oder neue JavaScript-Funktionen testen können, mit denen Sie nicht vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="9135f-135">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="9135f-136">Die Konsole eignet sich hervorragend für Experimente dieser Art.</span><span class="sxs-lookup"><span data-stu-id="9135f-136">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="9135f-137">Geben `5 + 15` Sie die Konsole ein, und drücken Sie `Enter` , um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="9135f-137">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="9135f-138">Die Konsole druckt das Ergebnis des Ausdrucks unter dem Code aus.</span><span class="sxs-lookup"><span data-stu-id="9135f-138">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="9135f-139">**Abbildung 4** zeigt, wie Ihre Konsole nach der Auswertung dieses Ausdrucks aussehen soll.</span><span class="sxs-lookup"><span data-stu-id="9135f-139">**Figure 4** below shows how your Console should look after evaluating this expression.</span></span>  

1.  <span data-ttu-id="9135f-140">Geben Sie den folgenden Code in die **Konsole**ein.</span><span class="sxs-lookup"><span data-stu-id="9135f-140">Type the following code into the **Console**.</span></span>  <span data-ttu-id="9135f-141">Versuchen Sie, das Zeichen-für-Zeichen-Zeichen zu schreiben, anstatt es zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9135f-141">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    <span data-ttu-id="9135f-142">Weitere Informationen finden Sie unter [Definieren von Standardwerten für Funktionsargumente][Esma6DefaultParameterValues] , wenn Sie mit der Syntax nicht vertraut sind `b=20` .</span><span class="sxs-lookup"><span data-stu-id="9135f-142">See [define default values for function arguments][Esma6DefaultParameterValues] if you are unfamiliar with the `b=20` syntax.</span></span>  
    
1.  <span data-ttu-id="9135f-143">Rufen Sie nun die soeben definierte Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9135f-143">Now, call the function that you just defined.</span></span>  
    
    ```javascript
    add(25);
    ```  
    
    > ##### <span data-ttu-id="9135f-144">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="9135f-144">Figure 4</span></span>  
    > <span data-ttu-id="9135f-145">So sieht die Konsole aus, nachdem die Ausdrücke oben ausgewertet wurden</span><span class="sxs-lookup"><span data-stu-id="9135f-145">How the Console looks after evaluating the expressions above</span></span>  
    > ![So sieht die Konsole aus, nachdem die Ausdrücke oben ausgewertet wurden][ImagePlayground]  
    
    `add(25)` <span data-ttu-id="9135f-147">wird als Standardwert ausgewertet, `45` Wenn die `add` Funktion ohne ein zweites Argument aufgerufen wird `b` `20` .</span><span class="sxs-lookup"><span data-stu-id="9135f-147">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="9135f-148">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9135f-148">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="9135f-149">Mit devtools können Sie ein Skript mitten in der Ausführung anhalten.</span><span class="sxs-lookup"><span data-stu-id="9135f-149">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="9135f-150">Während Sie angehalten werden, können Sie die **Konsole** verwenden, um die `window` oder `DOM` der Seite zu diesem Zeitpunkt anzuzeigen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9135f-150">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="9135f-151">Dies sorgt für einen leistungsfähigen Debugging-Workflow.</span><span class="sxs-lookup"><span data-stu-id="9135f-151">This makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="9135f-152">Weitere Informationen finden Sie unter [Erste Schritte beim Debuggen von JavaScript][DevToolsJavascriptIndex] für ein interaktives Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="9135f-152">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] for an interactive tutorial.</span></span>  

<span data-ttu-id="9135f-153">Die **Konsole** verfügt auch über eine Reihe von Funktionen, mit denen Sie die Interaktion mit einer Seite vereinfachen können.</span><span class="sxs-lookup"><span data-stu-id="9135f-153">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="9135f-154">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9135f-154">For example:</span></span>  

*   <span data-ttu-id="9135f-155">Anstatt `document.querySelector()` ein Element zu markieren, geben Sie Folgendes ein: `$()`</span><span class="sxs-lookup"><span data-stu-id="9135f-155">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="9135f-156">Diese Syntax wurde von jQuery inspiriert, ist aber nicht wirklich jQuery.</span><span class="sxs-lookup"><span data-stu-id="9135f-156">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="9135f-157">Es ist nur ein Alias für `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="9135f-157">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="9135f-158">legt einen Haltepunkt in der ersten Zeile dieser Funktion effektiv fest.</span><span class="sxs-lookup"><span data-stu-id="9135f-158">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="9135f-159">Gibt ein Array zurück, das die Schlüssel des angegebenen Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="9135f-159">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Abbildung 1: die Konsole"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Abbildung 2: die Konsole JavaScript-Beispielseite auf der linken Seite und DevTools auf der rechten Seite"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Abbildung 3: Aussehen der Konsole nach dem Auswerten des Ausdrucks"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Abbildung 4: so sieht die Konsole aus, nachdem die Ausdrücke oben ausgewertet wurden"  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Konsolen Referenz"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "API-Referenz für Konsolen Dienstprogramme"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Ausdrücke im Vergleich zu Anweisungen in JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Standardparameterwerte – erweiterte Parameterbehandlung – ECMAScript 6 – neue Features: Übersicht & Vergleich"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Beispiel für eine Konsolen-JavaScript | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lesen – eval – Print Loop – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="9135f-172">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9135f-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9135f-173">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/javascript) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9135f-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9135f-175">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9135f-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
