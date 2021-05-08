---
description: Öffnen Sie die Konsole, erstellen Sie einen Liveausdruck, und legen Sie den Ausdruck auf document.activeElement.
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2c2040c690441fb33c802cf454dc7a1e3f33c494
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439170"
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

# <a name="track-which-element-has-focus"></a><span data-ttu-id="45e1b-104">Nachverfolgen, welches Element den Fokus hat</span><span class="sxs-lookup"><span data-stu-id="45e1b-104">Track which element has focus</span></span>  

<span data-ttu-id="45e1b-105">Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation einer Seite.</span><span class="sxs-lookup"><span data-stu-id="45e1b-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="45e1b-106">Beim Navigieren auf der Seite mit der Taste wird der Fokusring manchmal ausgeblendet, da das Element mit dem Fokus `Tab` ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="45e1b-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="45e1b-107">Führen Sie die folgenden Aktionen aus, um das fokussierte Element in DevTools nachverfolgt zu haben.</span><span class="sxs-lookup"><span data-stu-id="45e1b-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="45e1b-108">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="45e1b-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="45e1b-109">Wählen **Sie Liveausdruck** erstellen \( ![ Liveausdruck ](../media/create-live-expression-icon.msft.png) erstellen \).</span><span class="sxs-lookup"><span data-stu-id="45e1b-109">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Liveausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="45e1b-111">Erstellen eines Liveausdrucks</span><span class="sxs-lookup"><span data-stu-id="45e1b-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45e1b-112">Geben Sie `document.activeElement` ein.</span><span class="sxs-lookup"><span data-stu-id="45e1b-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="45e1b-113">Wählen Sie außerhalb der **zu speichernde Live** Expression-Benutzeroberfläche aus.</span><span class="sxs-lookup"><span data-stu-id="45e1b-113">Choose outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="45e1b-114">Der unten angezeigte `document.activeElement` Wert ist das Ergebnis des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="45e1b-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="45e1b-115">Da dieser Ausdruck immer das fokussierte Element darstellt, haben Sie nun eine Möglichkeit, immer nachverfolgt zu werden, welches Element den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="45e1b-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="45e1b-116">Zeigen Sie auf das Ergebnis, um das fokussierte Element im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="45e1b-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="45e1b-117">Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \*\*\*\* \(klicken Sie mit der rechten Maustaste\), und wählen Sie im Bereich Elemente anzeigen aus, um das Element im DOM-Struktur im **Elementtool anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="45e1b-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="45e1b-118">Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Store als globale** Variable aus, um einen Variablenverweis auf den Knoten zu erstellen, den Sie in der Konsole verwenden **können.**</span><span class="sxs-lookup"><span data-stu-id="45e1b-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="45e1b-119">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="45e1b-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="45e1b-120">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45e1b-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="45e1b-121">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="45e1b-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="45e1b-123">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45e1b-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
