---
title: Übersicht über die Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601786"
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





# <span data-ttu-id="454ef-103">Übersicht über die Konsole</span><span class="sxs-lookup"><span data-stu-id="454ef-103">Console Overview</span></span>   

  

<span data-ttu-id="454ef-104">Auf dieser Seite wird erläutert, wie die Microsoft Edge devtools-Konsole das Entwickeln von Webseiten vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="454ef-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="454ef-105">Die Konsole hat zwei hauptsächliche Verwendungsmöglichkeiten: [Anzeigen von protokollierten Nachrichten](#viewing-logged-messages) und [Ausführen von JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="454ef-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="454ef-106">Anzeigen von angemeldeten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="454ef-106">Viewing logged messages</span></span>   

<span data-ttu-id="454ef-107">Web-Entwickler protokollieren häufig Nachrichten an die Konsole, um sicherzustellen, dass Ihr JavaScript wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="454ef-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="454ef-108">Wenn Sie eine Nachricht protokollieren möchten, fügen Sie einen Ausdruck wie `console.log('Hello, Console!')` in Ihr JavaScript ein.</span><span class="sxs-lookup"><span data-stu-id="454ef-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="454ef-109">Wenn der Browser Ihr JavaScript ausführt und einen Ausdruck wie diesen sieht, wird die Nachricht in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="454ef-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  <span data-ttu-id="454ef-110">Nehmen wir beispielsweise an, dass Sie das HTML und JavaScript für eine Seite schreiben:</span><span class="sxs-lookup"><span data-stu-id="454ef-110">For example, suppose that you are writing the HTML and JavaScript for a page:</span></span>  

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
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
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

<span data-ttu-id="454ef-111">[Abbildung 1](#figure-1) zeigt, wie die Konsole aussieht, nachdem Sie die Seite geladen und 3 Sekunden gewartet hat.</span><span class="sxs-lookup"><span data-stu-id="454ef-111">[Figure 1](#figure-1) shows what the Console looks like after loading the page and waiting 3 seconds.</span></span>  <span data-ttu-id="454ef-112">Versuchen Sie herauszufinden, welche Codezeilen der Browser veranlasst hat, die Nachrichten zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="454ef-112">Try to figure out which lines of code caused the browser to log the messages.</span></span>  

> ##### <span data-ttu-id="454ef-113">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="454ef-113">Figure 1</span></span>  
> <span data-ttu-id="454ef-114">Die Konsolen Leiste</span><span class="sxs-lookup"><span data-stu-id="454ef-114">The Console panel</span></span>  
> ![Die Konsolen Leiste][ImageConsole]  

<span data-ttu-id="454ef-116">Web-Entwickler protokollieren Nachrichten aus zwei allgemeinen Gründen:</span><span class="sxs-lookup"><span data-stu-id="454ef-116">Web developers log messages for 2 general reasons:</span></span>  

*   <span data-ttu-id="454ef-117">Sicherstellen, dass der Code in der richtigen Reihenfolge ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="454ef-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="454ef-118">Überprüfen der Werte von Variablen zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="454ef-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="454ef-119">Lesen Sie [Erste Schritte mit der Protokollierung von Nachrichten][DevtoolsConsoleLoggingMessages] , um praktische Erfahrungen mit der Protokollierung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="454ef-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="454ef-120">Die vollständige Liste der Methoden finden Sie in der [API-Referenz][DevToolsConsoleAPI] für die Konsole `console` .</span><span class="sxs-lookup"><span data-stu-id="454ef-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="454ef-121">Der Hauptunterschied zwischen den Methoden besteht darin, wie die Daten, die protokolliert werden, angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="454ef-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="454ef-122">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="454ef-122">Running JavaScript</span></span>   

<span data-ttu-id="454ef-123">Die Konsole ist auch ein [repl][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="454ef-123">The Console is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="454ef-124">Sie können JavaScript in der Konsole ausführen, um mit der geprüften Seite zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="454ef-124">You may run JavaScript in the Console to interact with the page being inspected.</span></span>  <span data-ttu-id="454ef-125">[Abbildung 2](#figure-2) zeigt beispielsweise die Konsole neben der devtools-Startseite, und [Abbildung 3](#figure-3) zeigt dieselbe Seite nach der Verwendung der Konsole, um die obere Überschrift der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="454ef-125">For example, [Figure 2](#figure-2) shows the Console next to the DevTools homepage, and [Figure 3](#figure-3) shows that same page after using the Console to change the top heading of the page.</span></span>  

> ##### <span data-ttu-id="454ef-126">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="454ef-126">Figure 2</span></span>  
> <span data-ttu-id="454ef-127">Das Konsolenfeld neben der devtools-Startseite</span><span class="sxs-lookup"><span data-stu-id="454ef-127">The Console panel next to the DevTools homepage</span></span>  
> ![Das Konsolenfeld neben der devtools-Startseite][ImageConsoleOverview]  

> ##### <span data-ttu-id="454ef-129">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="454ef-129">Figure 3</span></span>  
> <span data-ttu-id="454ef-130">Verwenden der Konsole zum Ändern der obersten Überschrift der Seite</span><span class="sxs-lookup"><span data-stu-id="454ef-130">Using the Console to change the top heading of the page</span></span>  
> ![Verwenden der Konsole zum Ändern der obersten Überschrift der Seite][ImageConsoleChangeTitle]  

<span data-ttu-id="454ef-132">Das Ändern der Seite über die Konsole ist möglich, da die Konsole Vollzugriff auf das [Fenster][MDNWindow] der Seite hat.</span><span class="sxs-lookup"><span data-stu-id="454ef-132">Modifying the page from the Console is possible because the Console has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="454ef-133">DevTools verfügt über einige komfortable Funktionen, mit denen Sie eine Seite leichter überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="454ef-133">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="454ef-134">Nehmen wir beispielsweise an, dass Ihr JavaScript eine Funktion mit dem Namen `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="454ef-134">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="454ef-135">Durch Ausführen wird der `debug(hideModal)` Code in der ersten Zeile des `hideModal` nächsten Ausführungszeitraums angehalten.</span><span class="sxs-lookup"><span data-stu-id="454ef-135">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="454ef-136">Die vollständige Liste der Dienstprogrammfunktionen finden Sie unter [API-Referenz][DevtoolsConsoleUtilitiesDebug] für die Konsolen Dienstprogramme.</span><span class="sxs-lookup"><span data-stu-id="454ef-136">See [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug] to see the full list of utility functions.</span></span>  

<span data-ttu-id="454ef-137">Wenn Sie JavaScript ausführen, müssen Sie nicht mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="454ef-137">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="454ef-138">Sie können die Konsole verwenden, um neuen Code auszuprobieren, der sich nicht auf die Seite bezieht.</span><span class="sxs-lookup"><span data-stu-id="454ef-138">You may use the Console to try out new code unrelated to the page.</span></span>  <span data-ttu-id="454ef-139">Angenommen, Sie haben soeben die integrierte JavaScript-Array [Zuordnungsmethode ()][MDNMap] kennengelernt, und Sie möchten damit experimentieren.</span><span class="sxs-lookup"><span data-stu-id="454ef-139">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="454ef-140">Die **Konsole** ist ein guter Ort, um die Funktion auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="454ef-140">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="454ef-141">Lesen Sie [Erste Schritte mit der Ausführung von JavaScript][ImageConsoleChangeTitle] , um praktische Erfahrungen mit der Ausführung von JavaScript in der Konsole zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="454ef-141">See [Get Started With Running JavaScript][ImageConsoleChangeTitle] to get hands-on experience with running JavaScript in the Console.</span></span>  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Abbildung 1: die Konsolen Leiste"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Abbildung 3: Verwenden der Konsole zum Ändern der obersten Überschrift der Seite"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Abbildung 2: die Konsolen Leiste neben der devtools-Startseite"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Erste Schritte mit der Ausführung von JavaScript in der Konsole"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Debug-API-Referenz für Console Utilities"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. Prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lesen – eval – Print Loop – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="454ef-152">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="454ef-152">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="454ef-153">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="454ef-153">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="454ef-155">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="454ef-155">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
