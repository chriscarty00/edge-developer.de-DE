---
description: Öffnen Sie das Befehlsmenü, und führen Sie den Befehl "JavaScript deaktivieren" aus.
title: Deaktivieren von JavaScript mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 665181b14e6fa5e86950a27822d52395f49f5b92
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519352"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a><span data-ttu-id="b1cac-104">Deaktivieren von JavaScript mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b1cac-104">Disable JavaScript with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b1cac-105">Um zu überprüfen, wie Ihre Webseite gerendert wird, wenn ein Browser keine JavaScript-Unterstützung hat, deaktivieren Sie javaScript vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="b1cac-105">To review how your webpage renders when a browser doesn't have JavaScript support, temporarily turn off JavaScript.</span></span>

<span data-ttu-id="b1cac-106">Führen Sie die folgenden Aktionen aus, um zu untersuchen, wie eine Webseite angezeigt wird und wie sie sich verhält, wenn Sie JavaScript deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b1cac-106">Complete the following actions to examine how a webpage displays and behaves when you turn off JavaScript.</span></span>  

1.  <span data-ttu-id="b1cac-107">[Öffnen Sie Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="b1cac-107">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="b1cac-108">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="b1cac-108">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="b1cac-110">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="b1cac-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b1cac-111">Beginnen Sie mit der `javascript` Eingabe, wählen **Sie JavaScript deaktivieren**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b1cac-111">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="b1cac-112">JavaScript ist jetzt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1cac-112">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="b1cac-114">Wählen **Sie im Befehlsmenü JavaScript** deaktivieren **aus.**</span><span class="sxs-lookup"><span data-stu-id="b1cac-114">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b1cac-115">Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b1cac-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol neben Quellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="b1cac-117">Das Warnungssymbol neben **Quellen**</span><span class="sxs-lookup"><span data-stu-id="b1cac-117">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b1cac-118">JavaScript bleibt auf der Registerkarte deaktiviert, solange DevTools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b1cac-118">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="b1cac-119">Möglicherweise möchten Sie die Seite aktualisieren, um zu überprüfen, ob und wie die Webseite beim Laden von JavaScript abhängt.</span><span class="sxs-lookup"><span data-stu-id="b1cac-119">You may want to refresh the page to review if and how the webpage depends on JavaScript while loading.</span></span>  

<span data-ttu-id="b1cac-120">Führen Sie die folgenden Aktionen aus, um JavaScript erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b1cac-120">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="b1cac-121">Öffnen Sie **das Befehlsmenü** erneut, und führen Sie den Befehl `Enable JavaScript` aus.</span><span class="sxs-lookup"><span data-stu-id="b1cac-121">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="b1cac-122">Schließen Sie DevTools.</span><span class="sxs-lookup"><span data-stu-id="b1cac-122">Close DevTools.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b1cac-123">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="b1cac-123">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="b1cac-125">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1cac-125">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b1cac-126">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="b1cac-126">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b1cac-128">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b1cac-128">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
