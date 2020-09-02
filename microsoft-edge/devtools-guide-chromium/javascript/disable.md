---
title: Deaktivieren von JavaScript mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 829902ddd76800bb8d36268cb07a61361aa1a159
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986115"
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

# <span data-ttu-id="42f81-103">Deaktivieren von JavaScript mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="42f81-103">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="42f81-104">Führen Sie die folgenden Aktionen aus, um zu sehen, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-104">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="42f81-105">[Öffnen Sie Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="42f81-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="42f81-106">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="42f81-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="42f81-108">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="42f81-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="42f81-109">Beginnen `javascript` Sie mit der Eingabe, wählen Sie **JavaScript deaktivieren**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="42f81-109">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="42f81-110">JavaScript ist jetzt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="42f81-110">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="42f81-112">Wählen Sie im **Befehlsmenü** **JavaScript deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-112">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="42f81-113">Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-113">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol nebenquellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="42f81-115">Das Warnungssymbol neben **Quellen**</span><span class="sxs-lookup"><span data-stu-id="42f81-115">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="42f81-116">JavaScript bleibt auf der Registerkarte so lange deaktiviert, wie Sie devtools geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="42f81-116">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="42f81-117">Möglicherweise möchten Sie die Seite neu laden, um festzustellen, ob und wie die Seite beim Laden von JavaScript abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-117">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="42f81-118">Führen Sie die folgenden Aktionen aus, um JavaScript wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="42f81-118">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="42f81-119">Öffnen Sie das **Befehl-Menü** erneut, und führen Sie den Befehl aus `Enable JavaScript` .</span><span class="sxs-lookup"><span data-stu-id="42f81-119">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="42f81-120">Schließen Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="42f81-120">Close DevTools.</span></span>  

## <span data-ttu-id="42f81-121">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="42f81-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="42f81-123">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42f81-123">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42f81-124">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="42f81-124">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="42f81-126">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42f81-126">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
