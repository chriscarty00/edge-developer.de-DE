---
description: So finden und analysieren Sie nicht verwendeten JavaScript- und CSS-Code in Microsoft Edge DevTools.
title: Suchen nicht verwendeten JavaScript- und CSS-Codes im Bereich "Abdeckung" in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398763"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a><span data-ttu-id="37061-104">Suchen von nicht verwendetem JavaScript- und CSS-Code im Bereich "Abdeckung" in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="37061-104">Find unused JavaScript and CSS code with the Coverage panel in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="37061-105">Der **Bereich Abdeckung** in Microsoft Edge DevTools hilft Ihnen, nicht verwendeten JavaScript- und CSS-Code zu finden.</span><span class="sxs-lookup"><span data-stu-id="37061-105">The **Coverage** panel in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="37061-106">Das Entfernen nicht verwendeten Codes kann das Laden der Seite beschleunigen und Mobilfunkdaten ihrer mobilen Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="37061-106">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analysieren der Codeabdeckung" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="37061-108">Analysieren der Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="37061-108">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="37061-109">Die Suche nach nicht verwendetem Code ist relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="37061-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="37061-110">Es kann jedoch schwierig sein, eine Codebasis so umgestalten, dass jede Seite nur javaScript und CSS enthält, die sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="37061-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="37061-111">In diesem Handbuch wird nicht beschrieben, wie Eine Codebasis umgestaltet wird, um nicht verwendeten Code zu vermeiden, da diese Umgestaltungen stark von Ihrem Technologiestapel abhängen.</span><span class="sxs-lookup"><span data-stu-id="37061-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <a name="overview"></a><span data-ttu-id="37061-112">Übersicht</span><span class="sxs-lookup"><span data-stu-id="37061-112">Overview</span></span>  

<span data-ttu-id="37061-113">Der Versand nicht verwendeter JavaScript- oder CSS-Dateien ist ein häufiges Problem bei der Webentwicklung.</span><span class="sxs-lookup"><span data-stu-id="37061-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="37061-114">Angenommen, Sie möchten die [Bootstrap-Schaltflächenkomponente auf][BootstrapButtons] Ihrer Seite verwenden.</span><span class="sxs-lookup"><span data-stu-id="37061-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="37061-115">Um die Schaltflächenkomponente zu verwenden, müssen Sie einen Link zum Bootstrap-Stylesheet in Ihrem HTML wie den folgenden hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="37061-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="37061-116">Dieses Stylesheet enthält nicht nur den Code für die Schaltflächenkomponente.</span><span class="sxs-lookup"><span data-stu-id="37061-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="37061-117">Es enthält die CSS für **alle** Bootstrap-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="37061-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="37061-118">Sie verwenden jedoch keine der anderen Bootstrap-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="37061-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="37061-119">Ihre Seite heruntergeladen also eine Reihe von CSS, die sie nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="37061-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="37061-120">Diese zusätzliche CSS ist aus den folgenden Gründen ein Problem.</span><span class="sxs-lookup"><span data-stu-id="37061-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="37061-121">Der zusätzliche Code verlangsamt die Seitenlast.</span><span class="sxs-lookup"><span data-stu-id="37061-121">The extra code slows down your page load.</span></span>  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="37061-122">Wenn ein Benutzer auf die Seite auf einem mobilen Gerät zugreift, verwendet der zusätzliche Code seine Mobilfunkdaten.</span><span class="sxs-lookup"><span data-stu-id="37061-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a><span data-ttu-id="37061-123">Öffnen des Abdeckungsbereichs</span><span class="sxs-lookup"><span data-stu-id="37061-123">Open the Coverage panel</span></span>  

1.  <span data-ttu-id="37061-124">[Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="37061-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="37061-125">Beginnen Sie mit der `coverage` Eingabe, wählen Sie den **Befehl Abdeckung** anzeigen aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="37061-125">Start typing `coverage`, select the **Show Coverage** command, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="37061-126">Der **Bereich** Abdeckung wird in der **Schublade geöffnet.**</span><span class="sxs-lookup"><span data-stu-id="37061-126">The **Coverage** panel opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Der Bereich "Abdeckung"" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="37061-128">Der **Bereich "Abdeckung"**</span><span class="sxs-lookup"><span data-stu-id="37061-128">The **Coverage** panel</span></span>  
    :::image-end:::  
    
## <a name="record-code-coverage"></a><span data-ttu-id="37061-129">Aufzeichnen der Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="37061-129">Record code coverage</span></span>  

1.  <span data-ttu-id="37061-130">Wählen Sie eine der folgenden Schaltflächen im **Bereich Abdeckung** aus.</span><span class="sxs-lookup"><span data-stu-id="37061-130">Choose one of the following buttons in the **Coverage** panel.</span></span>  
    *   <span data-ttu-id="37061-131">Wählen **Sie Start Instrumenting Coverage and Reload Page** \( Start Instrumenting Coverage and Reload Page \) aus, wenn Sie überprüfen möchten, welcher Code zum Laden der ![ Seite erforderlich ][ImageReloadIcon] ist.</span><span class="sxs-lookup"><span data-stu-id="37061-131">Choose **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page][ImageReloadIcon]\) if you want to review what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="37061-132">Wählen **Sie Instrument Coverage** \( Instrument Coverage ![ \) aus, wenn Sie überprüfen möchten, welcher Code nach der Interaktion mit der ][ImageRecordIcon] Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37061-132">Choose **Instrument Coverage** \(![Instrument Coverage][ImageRecordIcon]\) if you want to review what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="37061-133">Wählen **Sie Abdeckung beenden und Ergebnisse** anzeigen \( Die Instrumentierungsabdeckung beenden und Ergebnisse anzeigen \) aus, wenn Sie die Aufzeichnung der Codeabdeckung ![ beenden ][ImageStopIcon] möchten.</span><span class="sxs-lookup"><span data-stu-id="37061-133">Choose **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results][ImageStopIcon]\) when you want to stop recording code coverage.</span></span>  
    
## <a name="analyze-code-coverage"></a><span data-ttu-id="37061-134">Analysieren der Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="37061-134">Analyze code coverage</span></span>  

<span data-ttu-id="37061-135">In der Tabelle im **Bereich** "Abdeckung" werden die analysierten Ressourcen und der Code in den einzelnen Ressourcen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37061-135">The table in the **Coverage** panel displays the resources that were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="37061-136">Wählen Sie eine Zeile aus, um diese Ressource im Bereich Quellen zu **öffnen,** und überprüfen Sie eine Zeilenaufschlüsselung des verwendeten Codes und des nicht verwendeten Codes.</span><span class="sxs-lookup"><span data-stu-id="37061-136">Choose a row to open that resource in the **Sources** panel and review a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Ein Codeabdeckungsbericht" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="37061-138">Ein Codeabdeckungsbericht</span><span class="sxs-lookup"><span data-stu-id="37061-138">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="37061-139">Die **SPALTE URL** ist die URL der Ressource, die analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="37061-139">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="37061-140">Die **Spalte Type** gibt an, ob die Ressource CSS, JavaScript oder beides enthält.</span><span class="sxs-lookup"><span data-stu-id="37061-140">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="37061-141">Die **Spalte Bytes insgesamt** ist die Gesamtgröße der Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="37061-141">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="37061-142">Die **Spalte Nicht verwendete Bytes** gibt die Anzahl der Bytes an, die nicht verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="37061-142">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="37061-143">Die letzte, nicht benannte Spalte ist eine Visualisierung der Spalten **Total Bytes** und **Unused Bytes.**</span><span class="sxs-lookup"><span data-stu-id="37061-143">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="37061-144">Der rote Abschnitt der Leiste ist nicht verwendete Bytes.</span><span class="sxs-lookup"><span data-stu-id="37061-144">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="37061-145">Der grüne Abschnitt wird byte verwendet.</span><span class="sxs-lookup"><span data-stu-id="37061-145">The green section is used bytes.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="37061-146">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="37061-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Schaltflächen – Bootstrap"  

> [!NOTE]
> <span data-ttu-id="37061-149">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37061-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="37061-150">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/coverage/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="37061-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="37061-152">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="37061-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
