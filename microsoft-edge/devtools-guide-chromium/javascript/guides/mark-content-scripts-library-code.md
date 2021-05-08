---
description: Aktivieren Sie "Markieren von Inhaltsskripts als Bibliothekscode" Einstellungen > Framework Library Code.
title: Markieren von Inhaltsskripts als Bibliothekscode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c1571ab909aac09e4593413e96f7d4b7723c7759
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519345"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="42b34-104">Markieren von Inhaltsskripts als Bibliothekscode</span><span class="sxs-lookup"><span data-stu-id="42b34-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="42b34-105">Wenn Sie das Tool **Quellen** verwenden, um Code zu [durchschritten,][DevToolsJavascriptStepThroughCode]unterbrechen Sie manchmal code, den Sie nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="42b34-105">When you use the **Sources** tool to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you don't recognize.</span></span>  <span data-ttu-id="42b34-106">Wahrscheinlich haben Sie den Code für eine der installierten Microsoft Edge angehalten.</span><span class="sxs-lookup"><span data-stu-id="42b34-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="42b34-107">Führen Sie die folgenden Aktionen aus, um den Erweiterungscode nicht anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="42b34-107">To not pause on extension code, complete the following actions.</span></span>  

1.  <span data-ttu-id="42b34-108">Wählen Sie in DevTools oben rechts das Zahnradsymbol (**Einstellungen**).</span><span class="sxs-lookup"><span data-stu-id="42b34-108">In DevTools, in the upper right, choose the gear icon (**Settings**).</span></span>  <span data-ttu-id="42b34-109">Die Seite **Einstellungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42b34-109">The **Settings** page appears.</span></span>  
1.  <span data-ttu-id="42b34-110">Wählen **Einstellungen**Sie Liste **ignorieren aus.**</span><span class="sxs-lookup"><span data-stu-id="42b34-110">Below **Settings**, choose **Ignore List**.</span></span>  <span data-ttu-id="42b34-111">Der **Abschnitt Framework Library Code** von **Einstellungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42b34-111">The **Framework Library Code** section of **Settings** appears.</span></span>  
1.  <span data-ttu-id="42b34-112">Aktivieren Sie das **Kontrollkästchen Inhaltsskripts als Bibliothekscode** markieren.</span><span class="sxs-lookup"><span data-stu-id="42b34-112">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Aktivieren des Kontrollkästchens Inhaltsskripts als Bibliothekscode markieren" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="42b34-114">Aktivieren des **Kontrollkästchens Inhaltsskripts als Bibliothekscode** markieren</span><span class="sxs-lookup"><span data-stu-id="42b34-114">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="42b34-115">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="42b34-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: Schritt durch den Code – Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="42b34-117">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42b34-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42b34-118">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="42b34-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="42b34-120">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42b34-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
