---
title: Markieren von Inhalts Skripts als Bibliotheks Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581789"
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





# <span data-ttu-id="086d9-103">Markieren von Inhalts Skripts als Bibliotheks Code</span><span class="sxs-lookup"><span data-stu-id="086d9-103">Mark Content Scripts as Library Code</span></span>   



<span data-ttu-id="086d9-104">Wenn Sie den Quellcode **-Panel von** Microsoft Edge devtools verwenden, um Code zu [durchlaufen][DevToolsJavascriptStepThroughCode], können Sie manchmal auf Code pausieren, den Sie nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="086d9-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="086d9-105">Wahrscheinlich haben Sie den Code für eine der installierten Microsoft-Edge-Erweiterungen angehalten.</span><span class="sxs-lookup"><span data-stu-id="086d9-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="086d9-106">Führen Sie die folgenden Schritte aus, um den Erweiterungscode nicht zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="086d9-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="086d9-107">Öffnen Sie devtools, wählen Sie anpassen aus, **und Steuern Sie devtools** , `...` und klicken Sie auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="086d9-107">Open DevTools, select **Customize and control DevTools** `...` and click **Settings**.</span></span>  <span data-ttu-id="086d9-108">Sie können die **Einstellungen** auch öffnen, indem Sie auf klicken `F1` .</span><span class="sxs-lookup"><span data-stu-id="086d9-108">You may also open **Settings** by pressing `F1`.</span></span>  

1.  <span data-ttu-id="086d9-109">Wählen Sie die Registerkarte " **Bibliothekscode** " aus, um den Abschnitt " **Framework Library Code** " von **Settings**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="086d9-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="086d9-110">Aktivieren Sie das Kontrollkästchen **Inhalts Skripts als Bibliothekscode markieren** .</span><span class="sxs-lookup"><span data-stu-id="086d9-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="086d9-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="086d9-111">Figure 1</span></span>  
    > <span data-ttu-id="086d9-112">Aktivieren des Kontrollkästchens " **Inhalts Skripts als Bibliothekscode markieren** "</span><span class="sxs-lookup"><span data-stu-id="086d9-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    > ![Aktivieren des Kontrollkästchens "Inhalts Skripts als Bibliothekscode markieren"][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Abbildung 1: Aktivieren des Kontrollkästchens "Inhalts Skripts als Bibliothekscode markieren""  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: Durchlaufen des Codes – erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  

> [!NOTE]
> <span data-ttu-id="086d9-116">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="086d9-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="086d9-117">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse) erstellt.</span><span class="sxs-lookup"><span data-stu-id="086d9-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="086d9-119">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="086d9-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
