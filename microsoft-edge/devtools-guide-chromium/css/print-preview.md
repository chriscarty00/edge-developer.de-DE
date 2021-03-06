---
description: Öffnen Sie das Tool "Rendering", und wählen Sie Emulieren von CSS-Medien > aus.
title: Erzwingen des Druckvorschaumodus von Microsoft Edge DevTools (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 0123b7abf475212304f654c04bc232e3e96f0bda
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399078"
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

# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a><span data-ttu-id="367a6-104">Erzwingen des Druckvorschaumodus von Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="367a6-104">Force Microsoft Edge DevTools into Print Preview mode</span></span>  

<span data-ttu-id="367a6-105">Die [Druckmedienabfrage steuert,][MDNUsingMediaQueries] wie Ihre Seite beim Drucken aussieht.</span><span class="sxs-lookup"><span data-stu-id="367a6-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="367a6-106">So erzwingen Sie, dass Ihre Seite in den Druckvorschaumodus wechselt:</span><span class="sxs-lookup"><span data-stu-id="367a6-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="367a6-107">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="367a6-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="367a6-109">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="367a6-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="367a6-110">Geben `rendering` Sie ein, wählen **Sie Rendering anzeigen**aus, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="367a6-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="367a6-111">Wählen **Sie unter Emulieren von CSS-Medien**die Option **Drucken aus.**</span><span class="sxs-lookup"><span data-stu-id="367a6-111">Under **Emulate CSS media**, choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Druckvorschaumodus" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="367a6-113">Druckvorschaumodus</span><span class="sxs-lookup"><span data-stu-id="367a6-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="367a6-114">Von hier aus können Sie Ihre CSS wie jede andere Webseite anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="367a6-114">From here, you may display and change your CSS, like any other web page.</span></span>  <span data-ttu-id="367a6-115">Navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="367a6-115">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="367a6-116">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="367a6-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsCSSGetStarted]: ./index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von Medienabfragen | MDN"  

> [!NOTE]
> <span data-ttu-id="367a6-120">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="367a6-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="367a6-121">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="367a6-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="367a6-123">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="367a6-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
