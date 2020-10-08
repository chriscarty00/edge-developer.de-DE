---
description: Die hauptsächliche Verwendung der Microsoft Edge devtools-Konsole sind das Protokollieren von Nachrichten und das Ausführen von JavaScript.
title: Übersicht über die Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0cdce953b22d22f9a2bf8048a6eff89388aa6e2e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993156"
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





# <span data-ttu-id="8d0d9-104">Übersicht über die Konsole</span><span class="sxs-lookup"><span data-stu-id="8d0d9-104">Console Overview</span></span>   

  

<span data-ttu-id="8d0d9-105">Auf dieser Seite wird erläutert, wie die Microsoft Edge devtools-Konsole das Entwickeln von Webseiten vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="8d0d9-106">Die Konsole hat zwei hauptsächliche Verwendungsmöglichkeiten: [Anzeigen von protokollierten Nachrichten](#viewing-logged-messages) und [Ausführen von JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="8d0d9-106">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="8d0d9-107">Anzeigen von angemeldeten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8d0d9-107">Viewing logged messages</span></span>   

<span data-ttu-id="8d0d9-108">Web-Entwickler protokollieren häufig Nachrichten an die Konsole, um sicherzustellen, dass Ihr JavaScript wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="8d0d9-109">Wenn Sie eine Nachricht protokollieren möchten, fügen Sie einen Ausdruck wie `console.log('Hello, Console!')` in Ihr JavaScript ein.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="8d0d9-110">Wenn der Browser Ihr JavaScript ausführt und einen Ausdruck wie diesen sieht, wird die Nachricht in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-110">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8d0d9-111">Das HTML und JavaScript für die Seite.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-111">The HTML and JavaScript for the page.</span></span>  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                      { first: 'Henri', last: 'Matisse' }
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8d0d9-112">In der folgenden Abbildung zeigt die **Konsole** die Ergebnisse des Ladens der Seite an und wartet 3 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="8d0d9-114">Die **Konsolen** Leiste</span><span class="sxs-lookup"><span data-stu-id="8d0d9-114">The **Console** panel</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="8d0d9-115">Ermitteln Sie, welche Codezeilen der Browser veranlasst hat, die Nachrichten zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8d0d9-116">Web-Entwickler protokollieren Nachrichten für die folgenden 2 allgemeinen Gründe.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="8d0d9-117">Sicherstellen, dass der Code in der richtigen Reihenfolge ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="8d0d9-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="8d0d9-118">Überprüfen der Werte von Variablen zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="8d0d9-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="8d0d9-119">Lesen Sie [Erste Schritte mit der Protokollierung von Nachrichten][DevtoolsConsoleLoggingMessages] , um praktische Erfahrungen mit der Protokollierung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="8d0d9-120">Die vollständige Liste der Methoden finden Sie in der [API-Referenz][DevToolsConsoleAPI] für die Konsole `console` .</span><span class="sxs-lookup"><span data-stu-id="8d0d9-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="8d0d9-121">Der Hauptunterschied zwischen den Methoden besteht darin, wie die Daten, die protokolliert werden, angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="8d0d9-122">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="8d0d9-122">Running JavaScript</span></span>   

<span data-ttu-id="8d0d9-123">Die **Konsole** ist auch ein [repl][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="8d0d9-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="8d0d9-124">Sie können JavaScript in der **Konsole** ausführen, um mit der geprüften Seite zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="8d0d9-125">In der folgenden Abbildung wird die **Konsole** neben der devtools-Startseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="8d0d9-127">Das **Konsolen** Feld neben der devtools-Startseite</span><span class="sxs-lookup"><span data-stu-id="8d0d9-127">The **Console** panel next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8d0d9-128">In der folgenden Abbildung wird dieselbe Seite nach der Verwendung der **Konsole** angezeigt, um die obere Überschrift der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="8d0d9-130">Verwenden der **Konsole** zum Ändern der obersten Überschrift der Seite</span><span class="sxs-lookup"><span data-stu-id="8d0d9-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="8d0d9-131">Das Ändern der Seite über die **Konsole** ist möglich, da die **Konsole** Vollzugriff auf das [Fenster][MDNWindow] der Seite hat.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="8d0d9-132">DevTools verfügt über einige komfortable Funktionen, mit denen Sie eine Seite leichter überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="8d0d9-133">Nehmen wir beispielsweise an, dass Ihr JavaScript eine Funktion mit dem Namen `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="8d0d9-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="8d0d9-134">Durch Ausführen wird der `debug(hideModal)` Code in der ersten Zeile des `hideModal` nächsten Ausführungszeitraums angehalten.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="8d0d9-135">Weitere Informationen zur vollständigen Liste der Dienstprogrammfunktionen finden Sie unter [API-Referenz für Konsolen Dienstprogramme][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="8d0d9-135">For more information about the full list of utility functions, see [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="8d0d9-136">Wenn Sie JavaScript ausführen, müssen Sie nicht mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="8d0d9-137">Sie können die **Konsole** verwenden, um neuen Code auszuprobieren, der sich nicht auf die Seite bezieht.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="8d0d9-138">Angenommen, Sie haben soeben die integrierte JavaScript-Array [Zuordnungsmethode ()][MDNMap] kennengelernt, und Sie möchten damit experimentieren.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="8d0d9-139">Die **Konsole** ist ein guter Ort, um die Funktion auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="8d0d9-140">Weitere praktische Erfahrungen mit der Ausführung von JavaScript in der **Konsole**finden Sie unter [Erste Schritte mit der Ausführung von JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="8d0d9-140">For more hands-on experience with running JavaScript in the **Console**, see [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

   

  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole | Microsoft docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsole | Microsoft docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "Debug-Console Utilities API Reference | Microsoft docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. Prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lesen – eval – Print Loop – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="8d0d9-148">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8d0d9-149">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d0d9-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="8d0d9-151">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d0d9-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
