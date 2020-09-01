---
title: Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 09adaadd6f62710b219911f69fbe39ba8edfb61a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982549"
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





# <span data-ttu-id="4763d-103">Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4763d-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="4763d-104">Das Befehlsmenü bietet eine schnelle Möglichkeit, auf der Benutzeroberfläche von Microsoft Edge devtools zu navigieren und häufige Aufgaben wie das [Deaktivieren von JavaScript][JavascriptDisable]durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4763d-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="4763d-105">Möglicherweise sind Sie mit einem ähnlichen Feature in Visual Studio-Code vertraut, der als [Befehls Palette][VisualStudioCodeUICommandPalette]bezeichnet wird, was die ursprüngliche Inspiration für das Befehlsmenü war.</span><span class="sxs-lookup"><span data-stu-id="4763d-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="4763d-107">Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript</span><span class="sxs-lookup"><span data-stu-id="4763d-107">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="4763d-108">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="4763d-108">Open the Command Menu</span></span>   

<span data-ttu-id="4763d-109">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="4763d-109">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="4763d-110">Oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Befehl ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="4763d-110">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Befehl "ausführen"" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="4763d-112">Befehl "ausführen"</span><span class="sxs-lookup"><span data-stu-id="4763d-112">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="4763d-113">Anzeigen der anderen verfügbaren Aktionen</span><span class="sxs-lookup"><span data-stu-id="4763d-113">See other available actions</span></span>   

<span data-ttu-id="4763d-114">Wenn Sie den Workflow verwenden, der unter [Öffnen des Befehls](#open-the-command-menu)Menüs erläutert wird, wird das Befehl-Menü mit einem `>` Zeichen vor der vorangestellt des Befehlsmenü-Textfelds geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4763d-114">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Das Befehlszeichen" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="4763d-116">Das Befehlszeichen</span><span class="sxs-lookup"><span data-stu-id="4763d-116">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="4763d-117">Löschen `>` Sie das Zeichen und den Typ `?` , um andere Aktionen anzuzeigen, die über das Befehlsmenü verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4763d-117">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Andere verfügbare Aktionen" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="4763d-119">Andere verfügbare Aktionen</span><span class="sxs-lookup"><span data-stu-id="4763d-119">Other available actions</span></span>  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools | Microsoft docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio-Code-UI"  

> [!NOTE]
> <span data-ttu-id="4763d-122">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4763d-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4763d-123">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4763d-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4763d-125">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4763d-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
