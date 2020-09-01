---
title: Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6bf9605fc8dc4e43db88668ac1f0af35bf9aba66
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982306"
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





# <span data-ttu-id="17f04-103">Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp)</span><span class="sxs-lookup"><span data-stu-id="17f04-103">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>   



<span data-ttu-id="17f04-104">Die [Druckmedien Abfrage][MDNUsingMediaQueries] steuert, wie Ihre Seite gedruckt aussieht.</span><span class="sxs-lookup"><span data-stu-id="17f04-104">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="17f04-105">So erzwingen Sie eine Seite in den Druckvorschau Modus:</span><span class="sxs-lookup"><span data-stu-id="17f04-105">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="17f04-106">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17f04-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="17f04-108">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="17f04-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="17f04-109">Geben `rendering` Sie, wählen Sie **Rendering anzeigen**aus, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="17f04-109">Type `rendering`, select **Show Rendering**, and then press `Enter`.</span></span>  
1.  <span data-ttu-id="17f04-110">Wählen Sie unter **emulieren von CSS-Medien** die Option **Drucken**aus.</span><span class="sxs-lookup"><span data-stu-id="17f04-110">Under **Emulate CSS media** select **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Seitenansicht-Modus" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="17f04-112">Seitenansicht-Modus</span><span class="sxs-lookup"><span data-stu-id="17f04-112">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="17f04-113">Von hier aus können Sie Ihre CSS wie jede andere Webseite anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="17f04-113">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="17f04-114">Weitere Informationen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="17f04-114">See [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevToolsCSSGetStarted]: ./index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von medienabfragen | MDN"  

> [!NOTE]
> <span data-ttu-id="17f04-118">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17f04-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="17f04-119">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="17f04-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="17f04-121">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17f04-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
