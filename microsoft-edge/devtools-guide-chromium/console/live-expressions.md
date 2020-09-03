---
description: Wenn Sie feststellen, dass Sie dieselben JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie stattdessen, Live Ausdrücke zu verwenden.
title: Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
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





# <span data-ttu-id="90ac9-104">Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an</span><span class="sxs-lookup"><span data-stu-id="90ac9-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="90ac9-105">Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="90ac9-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="90ac9-106">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.</span><span class="sxs-lookup"><span data-stu-id="90ac9-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="90ac9-107">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="90ac9-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="90ac9-108">Erstellen eines Live Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="90ac9-108">Create a Live Expression</span></span>   

1.  <span data-ttu-id="90ac9-109">[Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="90ac9-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="90ac9-110">Klicken Sie auf **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="90ac9-110">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="90ac9-111">Das Textfeld " **Live Ausdruck** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90ac9-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von Document. activeElement in das Textfeld "Live Ausdruck"" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="90ac9-113">Eingeben `document.activeElement` in das Textfeld " **Live Ausdruck** "</span><span class="sxs-lookup"><span data-stu-id="90ac9-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="90ac9-114">Geben `Control` + `Enter` Sie \ (Windows \) oder `Command` + `Enter` \ (macOS \) ein, um den Ausdruck zu speichern, oder klicken Sie außerhalb des Textfeldes **Live Ausdruck** .</span><span class="sxs-lookup"><span data-stu-id="90ac9-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Console-Console-Referenz öffnen | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="90ac9-116">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90ac9-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="90ac9-117">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="90ac9-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="90ac9-119">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90ac9-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
