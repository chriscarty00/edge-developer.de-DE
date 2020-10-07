---
description: If you find yourself typing the same JavaScript expressions into the Console repeatedly, try Live Expressions instead.
title: Watch JavaScript Expression Values In Real-Time With Live Expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 6b66c44b77cd50bc0c1575e5eceb7c8d1a01b709
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993114"
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





# <span data-ttu-id="8a1c8-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span><span class="sxs-lookup"><span data-stu-id="8a1c8-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="8a1c8-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span><span class="sxs-lookup"><span data-stu-id="8a1c8-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="8a1c8-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span><span class="sxs-lookup"><span data-stu-id="8a1c8-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="8a1c8-107">The value of the expression updates in near real-time.</span><span class="sxs-lookup"><span data-stu-id="8a1c8-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="8a1c8-108">Create a Live Expression</span><span class="sxs-lookup"><span data-stu-id="8a1c8-108">Create a Live Expression</span></span>   

1.  <span data-ttu-id="8a1c8-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="8a1c8-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="8a1c8-110">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span><span class="sxs-lookup"><span data-stu-id="8a1c8-110">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="8a1c8-111">The **Live Expression** text box appears.</span><span class="sxs-lookup"><span data-stu-id="8a1c8-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Typing document.activeElement into the Live Expression text box" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="8a1c8-113">Typing `document.activeElement` into the **Live Expression** text box</span><span class="sxs-lookup"><span data-stu-id="8a1c8-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8a1c8-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span><span class="sxs-lookup"><span data-stu-id="8a1c8-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Open the Console - Console Reference | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="8a1c8-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a1c8-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8a1c8-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8a1c8-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8a1c8-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a1c8-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
