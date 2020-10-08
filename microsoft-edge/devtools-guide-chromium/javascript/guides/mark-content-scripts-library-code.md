---
description: Aktivieren Sie "Inhalts Skripts als Bibliothekscode markieren" aus Einstellungen > Framework-Bibliothekscode.
title: Markieren von Inhaltsskripts als Bibliothekscode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 517e0a4e944f32d41451a0a5d9d7baa91ff97212
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992792"
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

# <span data-ttu-id="ba4a0-104">Markieren von Inhalts Skripts als Bibliothekscode</span><span class="sxs-lookup"><span data-stu-id="ba4a0-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="ba4a0-105">Wenn Sie den Quellcode **-Panel von** Microsoft Edge devtools verwenden, um Code zu [durchlaufen][DevToolsJavascriptStepThroughCode], können Sie manchmal auf Code pausieren, den Sie nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-105">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="ba4a0-106">Wahrscheinlich haben Sie den Code für eine der installierten Microsoft-Edge-Erweiterungen angehalten.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="ba4a0-107">Führen Sie die folgenden Schritte aus, um den Erweiterungscode nicht zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-107">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="ba4a0-108">Öffnen Sie devtools, wählen Sie **anpassen und Steuern von devtools** \ ( `...` \) aus, und wählen Sie **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-108">Open DevTools, select **Customize and control DevTools** \(`...`\) and choose **Settings**.</span></span>  <span data-ttu-id="ba4a0-109">Sie können die **Einstellungen** auch öffnen, indem Sie auswählen `F1` .</span><span class="sxs-lookup"><span data-stu-id="ba4a0-109">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="ba4a0-110">Wählen Sie die Registerkarte " **Bibliothekscode** " aus, um den Abschnitt " **Framework Library Code** " von **Settings**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-110">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="ba4a0-111">Aktivieren Sie das Kontrollkästchen **Inhalts Skripts als Bibliothekscode markieren** .</span><span class="sxs-lookup"><span data-stu-id="ba4a0-111">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Aktivieren des Kontrollkästchens &quot;Inhalts Skripts als Bibliothekscode markieren&quot;" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="ba4a0-113">Aktivieren des Kontrollkästchens " **Inhalts Skripts als Bibliothekscode markieren** "</span><span class="sxs-lookup"><span data-stu-id="ba4a0-113">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ba4a0-114">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ba4a0-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: schrittweise durch den Code – erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="ba4a0-116">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba4a0-117">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba4a0-119">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba4a0-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
