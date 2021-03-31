---
description: Wenn Sie die gleichen JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie es stattdessen mit Live-Ausdrücken.
title: Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Liveausdrücken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: af920de1c395489dc09b83f3cc0f24814c4f5cbe
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439226"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a><span data-ttu-id="78a06-104">Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Liveausdrücken</span><span class="sxs-lookup"><span data-stu-id="78a06-104">Watch JavaScript expression values in real-time with Live Expressions</span></span>  

<span data-ttu-id="78a06-105">Wenn Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="78a06-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="78a06-106">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein undheften ihn dann an den oberen Rand der Konsole.</span><span class="sxs-lookup"><span data-stu-id="78a06-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="78a06-107">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="78a06-107">The value of the expression updates in near real-time.</span></span>  

## <a name="create-a-live-expression"></a><span data-ttu-id="78a06-108">Erstellen eines Liveausdrucks</span><span class="sxs-lookup"><span data-stu-id="78a06-108">Create a Live Expression</span></span>  

1.  <span data-ttu-id="78a06-109">[Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="78a06-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="78a06-110">Wählen **Sie Liveausdruck** erstellen \( ![ Liveausdruck ](../media/create-live-expression-icon.msft.png) erstellen \).</span><span class="sxs-lookup"><span data-stu-id="78a06-110">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  <span data-ttu-id="78a06-111">Das **Textfeld Live-Ausdruck** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="78a06-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von document.activeElement in das Textfeld Live Expression" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="78a06-113">Eingeben `document.activeElement` in das Textfeld **Live Expression**</span><span class="sxs-lookup"><span data-stu-id="78a06-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="78a06-114">Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus,  um den Ausdruck zu speichern, oder wählen Sie außerhalb des Textfelds Live expression aus.</span><span class="sxs-lookup"><span data-stu-id="78a06-114">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save the expression, or choose outside of the **Live Expression** textbox.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="78a06-115">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="78a06-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Öffnen Sie die Konsole – Konsolenreferenz | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="78a06-117">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78a06-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="78a06-118">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="78a06-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="78a06-120">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="78a06-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
