---
description: Wenn Sie feststellen, dass Sie dieselben JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie stattdessen, Live Ausdrücke zu verwenden.
title: Sehen Sie sich die Werte für JavaScript-Ausdrücke in Real-Time mit Live Ausdrücken an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: f6787455863f738d0fa4e014ca8fc318ad83a9cb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125230"
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

# <span data-ttu-id="0ff5b-104">Sehen Sie sich die Werte für JavaScript-Ausdrücke in Real-Time mit Live Ausdrücken an</span><span class="sxs-lookup"><span data-stu-id="0ff5b-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>  

<span data-ttu-id="0ff5b-105">Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="0ff5b-106">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="0ff5b-107">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="0ff5b-108">Erstellen eines Live Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="0ff5b-108">Create a Live Expression</span></span>  

1.  <span data-ttu-id="0ff5b-109">[Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="0ff5b-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="0ff5b-110">Wählen Sie **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateLiveExpressionIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-110">Choose **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="0ff5b-111">Das Textfeld " **Live Ausdruck** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von Document. activeElement in das Textfeld &quot;Live Ausdruck&quot;" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="0ff5b-113">Eingeben `document.activeElement` in das Textfeld " **Live Ausdruck** "</span><span class="sxs-lookup"><span data-stu-id="0ff5b-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ff5b-114">Wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus, um den Ausdruck zu speichern, oder wählen Sie außerhalb des **Live Ausdrucks** -TextBox aus.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-114">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save the expression, or choose outside of the **Live Expression** textbox.</span></span>  

## <span data-ttu-id="0ff5b-115">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="0ff5b-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Console-Console-Referenz öffnen | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="0ff5b-117">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0ff5b-118">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ff5b-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="0ff5b-120">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0ff5b-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
