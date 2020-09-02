---
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 5261824b725384240453f216071255494e88e98d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991175"
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

# <span data-ttu-id="6a37f-103">Nachverfolgen, welches Element den Fokus hat</span><span class="sxs-lookup"><span data-stu-id="6a37f-103">Track Which Element Has Focus</span></span>  

<span data-ttu-id="6a37f-104">Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation auf einer Seite.</span><span class="sxs-lookup"><span data-stu-id="6a37f-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="6a37f-105">Beim Navigieren auf der Seite mit dem `Tab` Schlüssel verschwindet der Fokus Ring manchmal, da das Element mit dem Fokus ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="6a37f-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="6a37f-106">Führen Sie die folgenden Aktionen aus, um das fokussierte Element in devtools zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6a37f-106">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="6a37f-107">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="6a37f-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="6a37f-108">Klicken Sie auf **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6a37f-108">Click **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Live Ausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="6a37f-110">Erstellen eines Live Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="6a37f-110">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6a37f-111">Geben Sie `document.activeElement` ein.</span><span class="sxs-lookup"><span data-stu-id="6a37f-111">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="6a37f-112">Klicken Sie auf eine Stelle außerhalb der **Live Ausdruck** -Benutzeroberfläche, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6a37f-112">Click outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="6a37f-113">Der unten angezeigte Wert `document.activeElement` ist das Ergebnis des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="6a37f-113">The value that you see below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="6a37f-114">Da dieser Ausdruck immer das Focused-Element darstellt, haben Sie jetzt die Möglichkeit, immer nachzuverfolgen, welches Element den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="6a37f-114">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="6a37f-115">Zeigen Sie mit der Maus auf das Ergebnis, um das fokussierte Element im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="6a37f-115">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="6a37f-116">Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **im Element Fenster** anzeigen aus, um das Element in der DOM- **Struktur im Element Panel anzuzeigen** .</span><span class="sxs-lookup"><span data-stu-id="6a37f-116">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="6a37f-117">Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **als globale Variable speichern** aus, um einen Variablen Bezug auf den Knoten zu erstellen, den Sie in der **Konsole**verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6a37f-117">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <span data-ttu-id="6a37f-118">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="6a37f-118">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="6a37f-119">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a37f-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6a37f-120">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a37f-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6a37f-122">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6a37f-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
