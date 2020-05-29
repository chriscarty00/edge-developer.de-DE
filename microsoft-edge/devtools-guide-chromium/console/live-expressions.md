---
title: Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: c388e44ca5507dd88ad9ad7b7ee985e658dfc569
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601740"
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





# <span data-ttu-id="726cd-103">Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an</span><span class="sxs-lookup"><span data-stu-id="726cd-103">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="726cd-104">Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="726cd-104">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="726cd-105">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.</span><span class="sxs-lookup"><span data-stu-id="726cd-105">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="726cd-106">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="726cd-106">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="726cd-107">Erstellen eines Live Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="726cd-107">Create a Live Expression</span></span>   

1.  <span data-ttu-id="726cd-108">[Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="726cd-108">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="726cd-109">Klicken Sie auf **Live** Ausdruck erstellen ![ , um Live Ausdruck erstellen ][ImageCreateLiveExpressionIcon] .</span><span class="sxs-lookup"><span data-stu-id="726cd-109">Click **Create Live Expression** ![Create Live Expression][ImageCreateLiveExpressionIcon].</span></span>  <span data-ttu-id="726cd-110">Das Textfeld " **Live Ausdruck** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="726cd-110">The **Live Expression** text box appears.</span></span>  
    
    > ##### <span data-ttu-id="726cd-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="726cd-111">Figure 1</span></span>  
    > <span data-ttu-id="726cd-112">Eingeben `document.activeElement` in das Textfeld " **Live Ausdruck** "</span><span class="sxs-lookup"><span data-stu-id="726cd-112">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    > ![Eingeben von Document. activeElement in das Textfeld "Live Ausdruck"][ImageLiveExpressionTextbox]  
    
1.  <span data-ttu-id="726cd-114">Geben `Control` + `Enter` Sie \ (Windows \) oder `Command` + `Enter` \ (macOS \) ein, um den Ausdruck zu speichern, oder klicken Sie außerhalb des Textfeldes **Live Ausdruck** .</span><span class="sxs-lookup"><span data-stu-id="726cd-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpressionTextbox]: /microsoft-edge/devtools-guide-chromium/media/console-create-live-expression.msft.png "Abbildung 1: eingeben von Document. activeElement in das Textfeld "Live Ausdruck""  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console "Öffnen der Console-Console-Referenz"  

> [!NOTE]
> <span data-ttu-id="726cd-117">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="726cd-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="726cd-118">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="726cd-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="726cd-120">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="726cd-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
