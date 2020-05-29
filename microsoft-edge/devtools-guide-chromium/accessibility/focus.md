---
title: Nachvollziehen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: a1bcb7e97357d1348b363ecd4842d1b6a78feb45
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581531"
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





# <span data-ttu-id="f24cd-103">Nachvollziehen, welches Element den Fokus hat</span><span class="sxs-lookup"><span data-stu-id="f24cd-103">Track Which Element Has Focus</span></span>   



<span data-ttu-id="f24cd-104">Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation auf einer Seite.</span><span class="sxs-lookup"><span data-stu-id="f24cd-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="f24cd-105">Beim Navigieren auf der Seite mit dem `Tab` Schlüssel verschwindet der Fokus Ring manchmal, da das Element mit dem Fokus ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="f24cd-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  <span data-ttu-id="f24cd-106">So überwachen Sie das Focused-Element in devtools:</span><span class="sxs-lookup"><span data-stu-id="f24cd-106">To track the focused element in DevTools:</span></span>  

1.  <span data-ttu-id="f24cd-107">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f24cd-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="f24cd-108">Klicken Sie auf **Live** Ausdruck erstellen ![ , um Live Ausdruck erstellen ][ImageCreateIcon] .</span><span class="sxs-lookup"><span data-stu-id="f24cd-108">Click **Create Live Expression** ![Create Live Expression][ImageCreateIcon].</span></span>  

    > ##### <span data-ttu-id="f24cd-109">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="f24cd-109">Figure 1</span></span>  
    > <span data-ttu-id="f24cd-110">Erstellen eines **Live Ausdrucks**</span><span class="sxs-lookup"><span data-stu-id="f24cd-110">Creating a **Live Expression**</span></span>  
    > ![Erstellen eines Live Ausdrucks][ImageLiveExpression]  
    
1.  <span data-ttu-id="f24cd-112">Geben Sie `document.activeElement` ein.</span><span class="sxs-lookup"><span data-stu-id="f24cd-112">Type `document.activeElement`.</span></span>
1.  <span data-ttu-id="f24cd-113">Klicken Sie auf eine Stelle außerhalb der **Live Ausdruck** -Benutzeroberfläche, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f24cd-113">Click outside of the **Live Expression** UI to save.</span></span>

<span data-ttu-id="f24cd-114">Der unten angezeigte Wert `document.activeElement` ist das Ergebnis des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="f24cd-114">The value that you see below `document.activeElement` is the result of the expression.</span></span>  
<span data-ttu-id="f24cd-115">Da dieser Ausdruck immer das Focused-Element darstellt, haben Sie jetzt die Möglichkeit, immer nachzuverfolgen, welches Element den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="f24cd-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="f24cd-116">Zeigen Sie mit der Maus auf das Ergebnis, um das fokussierte Element im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="f24cd-116">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="f24cd-117">Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **im Element Fenster** anzeigen aus, um das Element in der DOM- **Struktur im Element Panel anzuzeigen** .</span><span class="sxs-lookup"><span data-stu-id="f24cd-117">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="f24cd-118">Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **als globale Variable speichern** aus, um einen Variablen Bezug auf den Knoten zu erstellen, den Sie in der **Konsole**verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f24cd-118">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCreateIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpression]: /microsoft-edge/devtools-guide-chromium/media/accessibility-console-create-live-expression-empty.msft.png "Abbildung 1: Erstellen eines Live Ausdrucks"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="f24cd-120">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f24cd-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f24cd-121">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f24cd-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f24cd-123">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f24cd-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
