---
title: Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 39a7967a7dd1d0b34eb802d2879e04a64afd0dd0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982236"
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





# <span data-ttu-id="5c286-103">Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an</span><span class="sxs-lookup"><span data-stu-id="5c286-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="5c286-104">Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c286-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="5c286-105">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.</span><span class="sxs-lookup"><span data-stu-id="5c286-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="5c286-106">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5c286-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="5c286-107">Erstellen eines Live Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="5c286-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="5c286-108">[Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="5c286-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="5c286-109">Klicken Sie auf **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="5c286-109">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="5c286-110">Das Textfeld " **Live Ausdruck** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c286-110">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von Document. activeElement in das Textfeld "Live Ausdruck"" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="5c286-112">Eingeben `document.activeElement` in das Textfeld " **Live Ausdruck** "</span><span class="sxs-lookup"><span data-stu-id="5c286-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5c286-113">Geben `Control` + `Enter` Sie \ (Windows \) oder `Command` + `Enter` \ (macOS \) ein, um den Ausdruck zu speichern, oder klicken Sie außerhalb des Textfeldes **Live Ausdruck** .</span><span class="sxs-lookup"><span data-stu-id="5c286-113">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Console-Console-Referenz öffnen | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="5c286-115">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c286-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5c286-116">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c286-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="5c286-118">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c286-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
