---
description: Öffnen Sie das Befehl-Menü, und führen Sie den Befehl "JavaScript deaktivieren" aus.
title: Deaktivieren von JavaScript mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992799"
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

# <span data-ttu-id="7560f-104">Deaktivieren von JavaScript mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="7560f-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7560f-105">Führen Sie die folgenden Aktionen aus, um zu sehen, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7560f-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="7560f-106">[Öffnen Sie Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="7560f-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="7560f-107">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7560f-107">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="7560f-109">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="7560f-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7560f-110">Beginnen `javascript` Sie mit der Eingabe, wählen Sie **JavaScript deaktivieren**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7560f-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="7560f-111">JavaScript ist jetzt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7560f-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="7560f-113">Wählen Sie im **Befehlsmenü** **JavaScript deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7560f-113">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7560f-114">Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7560f-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol nebenquellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="7560f-116">Das Warnungssymbol neben **Quellen**</span><span class="sxs-lookup"><span data-stu-id="7560f-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7560f-117">JavaScript bleibt auf der Registerkarte so lange deaktiviert, wie Sie devtools geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="7560f-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="7560f-118">Möglicherweise möchten Sie die Seite neu laden, um festzustellen, ob und wie die Seite beim Laden von JavaScript abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="7560f-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="7560f-119">Führen Sie die folgenden Aktionen aus, um JavaScript wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7560f-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="7560f-120">Öffnen Sie das **Befehl-Menü** erneut, und führen Sie den Befehl aus `Enable JavaScript` .</span><span class="sxs-lookup"><span data-stu-id="7560f-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="7560f-121">Schließen Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="7560f-121">Close DevTools.</span></span>  

## <span data-ttu-id="7560f-122">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="7560f-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="7560f-124">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7560f-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7560f-125">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="7560f-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="7560f-127">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7560f-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
