---
title: Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601747"
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





# <span data-ttu-id="1cdc8-103">Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="1cdc8-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="1cdc8-104">Das Befehlsmenü bietet eine schnelle Möglichkeit, auf der Benutzeroberfläche von Microsoft Edge devtools zu navigieren und häufige Aufgaben wie das [Deaktivieren von JavaScript][JavascriptDisable]durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="1cdc8-105">Möglicherweise sind Sie mit einem ähnlichen Feature in Visual Studio-Code vertraut, der als [Befehls Palette][VisualStudioCodeUICommandPalette]bezeichnet wird, was die ursprüngliche Inspiration für das Befehlsmenü war.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

> ##### <span data-ttu-id="1cdc8-106">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="1cdc8-106">Figure 1</span></span>  
> <span data-ttu-id="1cdc8-107">Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript</span><span class="sxs-lookup"><span data-stu-id="1cdc8-107">Using the Command Menu to disable JavaScript</span></span>  
> ![Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript][ImageDisableJS]  

## <span data-ttu-id="1cdc8-109">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="1cdc8-109">Open the Command Menu</span></span>   

<span data-ttu-id="1cdc8-110">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="1cdc8-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="1cdc8-111">Oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Befehl ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

> ##### <span data-ttu-id="1cdc8-112">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="1cdc8-112">Figure 2</span></span>  
> <span data-ttu-id="1cdc8-113">Befehl "ausführen"</span><span class="sxs-lookup"><span data-stu-id="1cdc8-113">Run Command</span></span>  
> ![Befehl "ausführen"][ImageRunCommand]  

## <span data-ttu-id="1cdc8-115">Anzeigen der anderen verfügbaren Aktionen</span><span class="sxs-lookup"><span data-stu-id="1cdc8-115">See other available actions</span></span>   

<span data-ttu-id="1cdc8-116">Wenn Sie den Workflow verwenden, der unter [Öffnen des Befehls](#open-the-command-menu)Menüs erläutert wird, wird das Befehl-Menü mit einem `>` Zeichen, das dem Befehlsmenü-Textfeld vorangestellt wird, geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-116">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character prepended to the Command Menu text box.</span></span>  

> ##### <span data-ttu-id="1cdc8-117">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="1cdc8-117">Figure 3</span></span>  
> <span data-ttu-id="1cdc8-118">Das Befehlszeichen</span><span class="sxs-lookup"><span data-stu-id="1cdc8-118">The command character</span></span>  
> ![Das Befehlszeichen][ImageCommandCharacter]  

<span data-ttu-id="1cdc8-120">Löschen `>` Sie das Zeichen und den Typ `?` , um andere Aktionen anzuzeigen, die über das Befehlsmenü verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-120">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

> ##### <span data-ttu-id="1cdc8-121">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="1cdc8-121">Figure 4</span></span>  
> <span data-ttu-id="1cdc8-122">Andere verfügbare Aktionen</span><span class="sxs-lookup"><span data-stu-id="1cdc8-122">Other available actions</span></span>  
> ![Andere verfügbare Aktionen][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Abbildung 1: Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Abbildung 2: Befehl "ausführen""  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Abbildung 3: das Befehlszeichen"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Abbildung 4: Weitere verfügbare Aktionen"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Deaktivieren von JavaScript mit Microsoft Edge devtools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio-Code-UI"  

> [!NOTE]
> <span data-ttu-id="1cdc8-130">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-130">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1cdc8-131">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="1cdc8-131">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="1cdc8-133">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1cdc8-133">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
