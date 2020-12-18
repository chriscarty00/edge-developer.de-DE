---
description: Öffnen Sie das Befehl-Menü, und führen Sie den Befehl "JavaScript deaktivieren" aus.
title: Deaktivieren von JavaScript mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: f7aafee4b05f843319a4a744e6cba148d4642667
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230670"
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

# <span data-ttu-id="f214d-104">Deaktivieren von JavaScript mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="f214d-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f214d-105">Führen Sie die folgenden Aktionen aus, um zu sehen, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f214d-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="f214d-106">[Öffnen Sie Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="f214d-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="f214d-107">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f214d-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="f214d-109">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="f214d-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f214d-110">Beginnen `javascript` Sie mit der Eingabe, wählen Sie **JavaScript deaktivieren**aus, und wählen Sie dann aus `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f214d-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="f214d-111">JavaScript ist jetzt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f214d-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="f214d-113">Wählen Sie im **Befehlsmenü** **JavaScript deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f214d-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f214d-114">Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f214d-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol nebenquellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="f214d-116">Das Warnungssymbol neben **Quellen**</span><span class="sxs-lookup"><span data-stu-id="f214d-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f214d-117">JavaScript bleibt auf der Registerkarte so lange deaktiviert, wie Sie devtools geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="f214d-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="f214d-118">Möglicherweise möchten Sie die Seite neu laden, um festzustellen, ob und wie die Seite beim Laden von JavaScript abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="f214d-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="f214d-119">Führen Sie die folgenden Aktionen aus, um JavaScript wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f214d-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="f214d-120">Öffnen Sie das **Befehl-Menü** erneut, und führen Sie den Befehl aus `Enable JavaScript` .</span><span class="sxs-lookup"><span data-stu-id="f214d-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="f214d-121">Schließen Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="f214d-121">Close DevTools.</span></span>  

## <span data-ttu-id="f214d-122">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f214d-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="f214d-124">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f214d-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f214d-125">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f214d-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f214d-127">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f214d-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
