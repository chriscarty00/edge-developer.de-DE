---
description: Aktivieren Sie "Markieren von Inhaltsskripts als Bibliothekscode" unter Einstellungen > Framework Library Code.
title: Markieren von Inhaltsskripts als Bibliothekscode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: ffc27cdd04ce28df888507fb2e1dc460d5bb4f21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398952"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="191ca-104">Markieren von Inhaltsskripts als Bibliothekscode</span><span class="sxs-lookup"><span data-stu-id="191ca-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="191ca-105">Wenn Sie den **Bereich Quellen** von Microsoft Edge DevTools [verwenden,][DevToolsJavascriptStepThroughCode]um Code zu durchschritten, unterbrechen Sie manchmal Code, den Sie nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="191ca-105">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="191ca-106">Wahrscheinlich haben Sie den Code für eine der installierten Microsoft Edge-Erweiterungen angehalten.</span><span class="sxs-lookup"><span data-stu-id="191ca-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="191ca-107">Führen Sie die folgenden Schritte aus, um den Erweiterungscode nicht anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="191ca-107">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="191ca-108">Öffnen Sie DevTools, wählen **Sie Anpassen und Steuern von DevTools** \( `...` \) > Einstellungen **aus.**</span><span class="sxs-lookup"><span data-stu-id="191ca-108">Open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="191ca-109">Sie können einstellungen auch **öffnen,** indem Sie `F1` auswählen.</span><span class="sxs-lookup"><span data-stu-id="191ca-109">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="191ca-110">Wählen Sie **den Codebereich Bibliothek** aus, der den **Abschnitt Frameworkbibliothekscode** unter **Einstellungen öffnet.**</span><span class="sxs-lookup"><span data-stu-id="191ca-110">Choose the **Library code** panel which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="191ca-111">Aktivieren Sie das **Kontrollkästchen Inhaltsskripts als Bibliothekscode** markieren.</span><span class="sxs-lookup"><span data-stu-id="191ca-111">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Aktivieren des Kontrollkästchens Inhaltsskripts als Bibliothekscode markieren" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="191ca-113">Aktivieren des **Kontrollkästchens Inhaltsskripts als Bibliothekscode** markieren</span><span class="sxs-lookup"><span data-stu-id="191ca-113">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="191ca-114">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="191ca-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: Schritt durch den Code – Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="191ca-116">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="191ca-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="191ca-117">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="191ca-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="191ca-119">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="191ca-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
