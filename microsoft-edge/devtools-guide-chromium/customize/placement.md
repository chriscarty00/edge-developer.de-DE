---
title: Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601346"
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





# <span data-ttu-id="6afcb-103">Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)</span><span class="sxs-lookup"><span data-stu-id="6afcb-103">Change Microsoft Edge DevTools Placement (Undock, Dock To Bottom, Dock To Left)</span></span>   



<span data-ttu-id="6afcb-104">Standardmäßig ist devtools an der rechten Seite des Viewports verankert.</span><span class="sxs-lookup"><span data-stu-id="6afcb-104">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="6afcb-105">Sie können auch an der Unterseite andocken, an der linken Seite andocken oder das devtools in einem separaten Fenster Abdocken.</span><span class="sxs-lookup"><span data-stu-id="6afcb-105">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

> ##### <span data-ttu-id="6afcb-106">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="6afcb-106">Figure 1</span></span>  
> <span data-ttu-id="6afcb-107">An Links Andocken</span><span class="sxs-lookup"><span data-stu-id="6afcb-107">Dock To Left</span></span>  
> ![An Links Andocken][ImageDockLeft]  

> ##### <span data-ttu-id="6afcb-109">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="6afcb-109">Figure 2</span></span>  
> <span data-ttu-id="6afcb-110">An den unteren Rand Andocken</span><span class="sxs-lookup"><span data-stu-id="6afcb-110">Dock To Bottom</span></span>  
> ![An den unteren Rand Andocken][ImageDockBottom]  

> ##### <span data-ttu-id="6afcb-112">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="6afcb-112">Figure 3</span></span>  
> <span data-ttu-id="6afcb-113">Browser in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="6afcb-113">Browser in separate window</span></span>  
> ![Browser in einem separaten Fenster][ImageUndockBrowser]  

> ##### <span data-ttu-id="6afcb-115">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="6afcb-115">Figure 4</span></span>  
> <span data-ttu-id="6afcb-116">Abdocken von devtools in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="6afcb-116">Undocked DevTools in separate window</span></span>  
> ![Abdocken von devtools in einem separaten Fenster][ImageUndockDevTools]  

## <span data-ttu-id="6afcb-118">Ändern der Platzierung aus dem Hauptmenü</span><span class="sxs-lookup"><span data-stu-id="6afcb-118">Change placement from the main menu</span></span>   

1.  <span data-ttu-id="6afcb-119">Klicken Sie auf **anpassen und Steuern von devtools** , `...` und wählen Sie **Abdocken in separates Fenster** ![ Abdocken aus ][ImageUndockIcon] , **docken** Sie an die untere ![ Docking-Station an den unteren Rand an ][ImageBottomIcon] , oder **docken** ![ ][ImageLeftIcon] Sie nach links</span><span class="sxs-lookup"><span data-stu-id="6afcb-119">Click **Customize And Control DevTools** `...` and select **Undock Into Separate Window** ![Undock][ImageUndockIcon], **Dock To Bottom** ![Dock To Bottom][ImageBottomIcon], or **Dock To Left** ![Dock To Left][ImageLeftIcon].</span></span>  
    
    > ##### <span data-ttu-id="6afcb-120">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="6afcb-120">Figure 5</span></span>  
    > <span data-ttu-id="6afcb-121">Auswählen der Option **"Abdocken" in separates Fenster**</span><span class="sxs-lookup"><span data-stu-id="6afcb-121">Selecting **Undock Into Separate Window**</span></span>  
    > ![Auswählen der Option "Abdocken" in separates Fenster][ImageUndockSettings]  
    
## <span data-ttu-id="6afcb-123">Ändern der Platzierung über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="6afcb-123">Change placement from the Command Menu</span></span>   

1.  <span data-ttu-id="6afcb-124">[Öffnen des Befehlsmenüs][DevtoolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="6afcb-124">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="6afcb-125">Führen Sie einen der folgenden Befehle aus: `Dock To Bottom` , `Undock Into Separate Window` .</span><span class="sxs-lookup"><span data-stu-id="6afcb-125">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="6afcb-126">Derzeit gibt es keinen Befehl zum Andocken an Left, aber Sie können über das [Hauptmenü](#change-placement-from-the-main-menu)darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6afcb-126">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    > ##### <span data-ttu-id="6afcb-127">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="6afcb-127">Figure 6</span></span>  
    > <span data-ttu-id="6afcb-128">Befehl "Abdocken"</span><span class="sxs-lookup"><span data-stu-id="6afcb-128">The undock command</span></span>  
    > ![Befehl "Abdocken"][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Abbildung 1: Andocken nach links"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Abbildung 2: Andocken an den unteren Rand"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Abbildung 3: Browser in einem separaten Fenster"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Abbildung 4: Abdocken von devtools in einem separaten Fenster"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Abbildung 5: Auswählen der Option "Abdocken" in separates Fenster"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Abbildung 6: Befehl "Abdocken""  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  

> [!NOTE]
> <span data-ttu-id="6afcb-137">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6afcb-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6afcb-138">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/customize/placement) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6afcb-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6afcb-140">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6afcb-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
