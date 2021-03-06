---
description: Die Hauptanwendung der Microsoft Edge DevTools-Konsole sind die Protokollierung von Nachrichten und das Ausführen von JavaScript.
title: Konsole – Übersicht
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399120"
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

# <a name="console-overview"></a><span data-ttu-id="34f03-104">Konsole – Übersicht</span><span class="sxs-lookup"><span data-stu-id="34f03-104">Console overview</span></span>  

  

<span data-ttu-id="34f03-105">Auf dieser Seite wird erläutert, wie die Microsoft Edge DevTools-Konsole die Entwicklung von Webseiten vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="34f03-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="34f03-106">Die **Konsole** hat zwei Hauptverwendungszwecke: [Anzeigen protokollierter Nachrichten und](#viewing-logged-messages) Ausführen von [JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="34f03-106">The **Console** has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <a name="viewing-logged-messages"></a><span data-ttu-id="34f03-107">Anzeigen protokollierter Nachrichten</span><span class="sxs-lookup"><span data-stu-id="34f03-107">Viewing logged messages</span></span>  

<span data-ttu-id="34f03-108">Webentwickler protokollieren häufig Nachrichten an der Konsole, um sicherzustellen, dass ihr JavaScript wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="34f03-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="34f03-109">Um eine Nachricht zu protokollieren, fügen Sie einen Ausdruck wie `console.log('Hello, Console!')` in Ihr JavaScript ein.</span><span class="sxs-lookup"><span data-stu-id="34f03-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="34f03-110">Wenn der Browser Ihr JavaScript ausgeführt und einen Ausdruck wie ihn verarbeitet, protokolliert der Browser die Nachricht an der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="34f03-110">When the browser runs your JavaScript and processes an expression like it, the browser logs the message to the **Console**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="34f03-111">Html und JavaScript für die Seite.</span><span class="sxs-lookup"><span data-stu-id="34f03-111">The HTML and JavaScript for the page.</span></span>  
      
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
      <span data-ttu-id="34f03-112">In der folgenden Abbildung zeigt die **Konsole** die Ergebnisse des Ladens der Seite an und wartet 3 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="34f03-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Konsolenbereich" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="34f03-114">Das **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="34f03-114">The **Console** tool</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="34f03-115">Versuchen Sie zu bestimmen, welche Codezeilen den Browser dazu führte, dass die Nachrichten protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="34f03-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="34f03-116">Webentwickler protokollieren Nachrichten aus den folgenden 2 allgemeinen Gründen.</span><span class="sxs-lookup"><span data-stu-id="34f03-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="34f03-117">Stellen Sie sicher, dass Code in der richtigen Reihenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34f03-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="34f03-118">Überprüfen der Werte von Variablen zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="34f03-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="34f03-119">Um praktische Erfahrungen mit der Protokollierung zu erhalten, navigieren Sie zu [Erste Schritte mit Protokollierungsmeldungen][DevtoolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="34f03-119">To get hands-on experience with logging, navigate to [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="34f03-120">Navigieren Sie zur Konsolen-API-Referenz, um die vollständige Liste der Methoden `console` [zu durchsuchen.][DevToolsConsoleAPI]</span><span class="sxs-lookup"><span data-stu-id="34f03-120">To browse the full list of `console` methods, navigate to the [Console API Reference][DevToolsConsoleAPI].</span></span>  <span data-ttu-id="34f03-121">Der Hauptunterschied zwischen den Methoden besteht in der Anzeige der protokollierten Daten.</span><span class="sxs-lookup"><span data-stu-id="34f03-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <a name="running-javascript"></a><span data-ttu-id="34f03-122">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="34f03-122">Running JavaScript</span></span>  

<span data-ttu-id="34f03-123">Die **Konsole** ist auch eine [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="34f03-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="34f03-124">Sie können JavaScript in der Konsole **ausführen,** um mit der überprüften Seite zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="34f03-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="34f03-125">In der folgenden Abbildung wird **die Konsole** neben der DevTools-Homepage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34f03-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Das Konsolentool neben der DevTools-Homepage" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="34f03-127">Das **Konsolentool** neben der DevTools-Homepage</span><span class="sxs-lookup"><span data-stu-id="34f03-127">The **Console** tool next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="34f03-128">In der folgenden Abbildung wird dieselbe Seite nach der Verwendung der **Konsole** angezeigt, um die obere Überschrift der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="34f03-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Ändern der oberen Überschrift der Seite mithilfe der Konsole" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="34f03-130">Ändern **der** oberen Überschrift der Seite mithilfe der Konsole</span><span class="sxs-lookup"><span data-stu-id="34f03-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="34f03-131">Das Ändern der Seite über die **Konsole** ist möglich, da die **Konsole** Vollzugriff auf das [Fenster][MDNWindow] der Seite hat.</span><span class="sxs-lookup"><span data-stu-id="34f03-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="34f03-132">DevTools verfügt über einige Komfortfunktionen, die das Überprüfen einer Seite vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="34f03-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="34f03-133">Angenommen, Ihr JavaScript enthält eine Funktion namens `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="34f03-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="34f03-134">Beim `debug(hideModal)` Ausführen wird der Code in der ersten Zeile des nächsten `hideModal` Ausführungslaufs angehalten.</span><span class="sxs-lookup"><span data-stu-id="34f03-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="34f03-135">Weitere Informationen zur vollständigen Liste der Hilfsfunktionen finden Sie unter [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="34f03-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="34f03-136">Wenn Sie JavaScript ausführen, müssen Sie nicht mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="34f03-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="34f03-137">Sie können die Konsole **verwenden,** um neuen Code zu testen, der nichts mit der Seite zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="34f03-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="34f03-138">Angenommen, Sie haben gerade etwas über die integrierte JavaScript Array [map()-Methode][MDNMap] erfahren, und Sie möchten damit experimentieren.</span><span class="sxs-lookup"><span data-stu-id="34f03-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="34f03-139">Die **Konsole** ist ein guter Ort, um die Funktion auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="34f03-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="34f03-140">Weitere praktische Erfahrungen mit der Ausführung von JavaScript in der **Konsole finden**Sie unter Erste Schritte mit der Ausführung [von JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="34f03-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="34f03-141">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="34f03-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsolenkonsole | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "debug – Apireferenz für Konsolenprogramme | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-Schleife – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="34f03-149">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34f03-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="34f03-150">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="34f03-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="34f03-152">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="34f03-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
