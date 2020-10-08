---
description: Leitfaden zum Öffnen des Befehlsmenüs, Ausführen von Befehlen, Anzeigen anderer Aktionen und vieles mehr.
title: Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 54dead492e7d58053efab77c82a10e7e3c912460
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993198"
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





# <span data-ttu-id="e2cba-104">Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="e2cba-104">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="e2cba-105">Das Befehlsmenü bietet eine schnelle Möglichkeit, auf der Benutzeroberfläche von Microsoft Edge devtools zu navigieren und häufige Aufgaben wie das [Deaktivieren von JavaScript][JavascriptDisable]durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e2cba-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="e2cba-106">Möglicherweise sind Sie mit einem ähnlichen Feature in Visual Studio-Code vertraut, der als [Befehls Palette][VisualStudioCodeUICommandPalette]bezeichnet wird, was die ursprüngliche Inspiration für das Befehlsmenü war.</span><span class="sxs-lookup"><span data-stu-id="e2cba-106">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="e2cba-108">Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript</span><span class="sxs-lookup"><span data-stu-id="e2cba-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="e2cba-109">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="e2cba-109">Open the Command Menu</span></span>   

<span data-ttu-id="e2cba-110">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="e2cba-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="e2cba-111">Oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Befehl ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="e2cba-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="e2cba-113">Befehl "ausführen"</span><span class="sxs-lookup"><span data-stu-id="e2cba-113">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="e2cba-114">Anzeigen der anderen verfügbaren Aktionen</span><span class="sxs-lookup"><span data-stu-id="e2cba-114">See other available actions</span></span>   

<span data-ttu-id="e2cba-115">Wenn Sie den Workflow verwenden, der unter [Öffnen des Befehls](#open-the-command-menu)Menüs erläutert wird, wird das Befehl-Menü mit einem `>` Zeichen vor der vorangestellt des Befehlsmenü-Textfelds geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e2cba-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="e2cba-117">Das Befehlszeichen</span><span class="sxs-lookup"><span data-stu-id="e2cba-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="e2cba-118">Löschen `>` Sie das Zeichen und den Typ `?` , um andere Aktionen anzuzeigen, die über das Befehlsmenü verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e2cba-118">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="e2cba-120">Andere verfügbare Aktionen</span><span class="sxs-lookup"><span data-stu-id="e2cba-120">Other available actions</span></span>  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools | Microsoft docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio-Code-UI"  

> [!NOTE]
> <span data-ttu-id="e2cba-123">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2cba-123">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e2cba-124">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2cba-124">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2cba-126">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2cba-126">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
