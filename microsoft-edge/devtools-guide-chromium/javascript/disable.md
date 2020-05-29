---
title: Deaktivieren von JavaScript mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581810"
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





# <span data-ttu-id="a61ee-103">Deaktivieren von JavaScript mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="a61ee-103">Disable JavaScript With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="a61ee-104">So sehen Sie, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="a61ee-104">To see how a web page looks and behaves when JavaScript is disabled:</span></span>  

1.  <span data-ttu-id="a61ee-105">[Öffnen Sie Microsoft Edge devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="a61ee-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="a61ee-106">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a61ee-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="a61ee-107">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="a61ee-107">Figure 1</span></span>  
    > <span data-ttu-id="a61ee-108">Das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="a61ee-108">The Command Menu</span></span>  
    > ![Das Befehlsmenü][ImageCommandMenu]  
    
1.  <span data-ttu-id="a61ee-110">Beginnen `javascript` Sie mit der Eingabe, wählen Sie **JavaScript deaktivieren**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a61ee-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="a61ee-111">JavaScript ist jetzt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a61ee-111">JavaScript is now disabled.</span></span>  
    
    > ##### <span data-ttu-id="a61ee-112">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="a61ee-112">Figure 2</span></span>  
    > <span data-ttu-id="a61ee-113">Auswählen von " **JavaScript deaktivieren** " im Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="a61ee-113">Selecting **Disable JavaScript** in the Command Menu</span></span>  
    > ![Auswählen von "JavaScript deaktivieren" im Befehlsmenü][ImageDisableJS]  
    
    <span data-ttu-id="a61ee-115">Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a61ee-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    > ##### <span data-ttu-id="a61ee-116">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="a61ee-116">Figure 3</span></span>  
    > <span data-ttu-id="a61ee-117">Das Warnungssymbol neben **Quellen**</span><span class="sxs-lookup"><span data-stu-id="a61ee-117">The warning icon next to **Sources**</span></span>  
    > ![Das Warnungssymbol nebenquellen][ImageDisableJSWarning]  

<span data-ttu-id="a61ee-119">JavaScript bleibt auf dieser Registerkarte so lange deaktiviert, wie Sie devtools geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="a61ee-119">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="a61ee-120">Möglicherweise möchten Sie die Seite neu laden, um festzustellen, ob und wie die Seite beim Laden von JavaScript abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="a61ee-120">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="a61ee-121">So aktivieren Sie JavaScript erneut:</span><span class="sxs-lookup"><span data-stu-id="a61ee-121">To re-enable JavaScript:</span></span>  

*   <span data-ttu-id="a61ee-122">Öffnen Sie das **Befehl-Menü** erneut, und führen Sie den Befehl aus `Enable JavaScript` .</span><span class="sxs-lookup"><span data-stu-id="a61ee-122">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="a61ee-123">Schließen Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="a61ee-123">Close DevTools.</span></span>  

## <span data-ttu-id="a61ee-124">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="a61ee-124">Feedback</span></span>   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Abbildung 1: das Befehlsmenü"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Abbildung 2: Auswählen von "JavaScript deaktivieren" im Befehlsmenü"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Abbildung 3: das Warnungssymbol nebenquellen"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Öffnen von Microsoft Edge devtools"  

> [!NOTE]
> <span data-ttu-id="a61ee-129">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a61ee-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a61ee-130">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a61ee-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="a61ee-132">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a61ee-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
