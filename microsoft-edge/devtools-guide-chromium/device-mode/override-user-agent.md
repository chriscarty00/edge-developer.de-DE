---
title: Überschreiben der Benutzer-Agent-Zeichenfolge von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0dedfcd8d00035ed1c4c02ef8a2ec0f1643d0687
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991163"
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

# <span data-ttu-id="923c6-103">Überschreiben der Benutzer-Agent-Zeichenfolge von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="923c6-103">Override the user agent string from Microsoft Edge DevTools</span></span>  

<span data-ttu-id="923c6-104">So überschreiben Sie die Zeichenfolge des [Benutzer-Agents][MDNUserAgent] von Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="923c6-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="923c6-105">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="923c6-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="923c6-107">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="923c6-107">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="923c6-108">Geben `network conditions` Sie **Netzwerkbedingungen anzeigen**ein, und drücken Sie, `Enter` um die Registerkarte **Netzwerkbedingungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="923c6-108">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="923c6-109">Deaktivieren Sie im Abschnitt **Benutzer-Agent** das Kontrollkästchen **automatisch auswählen** .</span><span class="sxs-lookup"><span data-stu-id="923c6-109">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Automatisches auswählen deaktivieren" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="923c6-111">**Automatisches auswählen** deaktivieren</span><span class="sxs-lookup"><span data-stu-id="923c6-111">Disable **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="923c6-112">Wählen Sie eine Benutzer-Agent-Zeichenfolge aus der Liste aus, oder geben Sie eine eigene benutzerdefinierte Zeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="923c6-112">Select a user agent string from the list, or enter your own custom string.</span></span>  

## <span data-ttu-id="923c6-113">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="923c6-113">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  

> [!NOTE]
> <span data-ttu-id="923c6-115">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="923c6-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="923c6-116">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="923c6-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="923c6-118">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="923c6-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
