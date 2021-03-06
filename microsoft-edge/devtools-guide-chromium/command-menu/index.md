---
description: Eine Anleitung zum Öffnen des Befehlsmenüs, Ausführen von Befehlen, Überprüfen anderer Aktionen und vieles mehr.
title: Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: a9e67815f69a44d3bd2a741738b04c7170f6ac15
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398028"
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

# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a><span data-ttu-id="13275-104">Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü</span><span class="sxs-lookup"><span data-stu-id="13275-104">Run commands with the Microsoft Edge DevTools Command menu</span></span>  

<span data-ttu-id="13275-105">Das Befehlsmenü bietet eine schnelle Möglichkeit, die Microsoft Edge DevTools-Benutzeroberfläche zu navigieren und allgemeine Aufgaben auszuführen, z. B. das Deaktivieren [von JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="13275-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="13275-106">Möglicherweise kennen Sie ein ähnliches Feature in Microsoft Visual Studio Code, die [Befehlspalette][VisualStudioCodeUICommandPalette], die die ursprüngliche Inspiration für das Befehlsmenü war.</span><span class="sxs-lookup"><span data-stu-id="13275-106">You may be familiar with a similar feature in Microsoft Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="13275-108">Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript</span><span class="sxs-lookup"><span data-stu-id="13275-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <a name="open-the-command-menu"></a><span data-ttu-id="13275-109">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="13275-109">Open the Command Menu</span></span>  

<span data-ttu-id="13275-110">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="13275-110">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="13275-111">Oder wählen **Sie Customize and Control DevTools** \( `...` \) > Run Command **aus.**</span><span class="sxs-lookup"><span data-stu-id="13275-111">Or choose **Customize And Control DevTools** \(`...`\) > **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Befehl ausführen" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="13275-113">Befehl ausführen</span><span class="sxs-lookup"><span data-stu-id="13275-113">Run Command</span></span>  
:::image-end:::  

## <a name="display-other-available-actions"></a><span data-ttu-id="13275-114">Anzeigen anderer verfügbarer Aktionen</span><span class="sxs-lookup"><span data-stu-id="13275-114">Display other available actions</span></span>  

<span data-ttu-id="13275-115">Wenn Sie den unter [Öffnen](#open-the-command-menu)des Befehlsmenüs beschriebenen Workflow verwenden, wird das Befehlsmenü mit einem Zeichen geöffnet, das im Textfeld Befehlsmenü `>` vorkonfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="13275-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Das Befehlszeichen" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="13275-117">Das Befehlszeichen</span><span class="sxs-lookup"><span data-stu-id="13275-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="13275-118">Löschen Sie `>` das Zeichen und den `?` Typ, um andere Aktionen anzuzeigen, die im Befehlsmenü verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="13275-118">Delete the `>` character and type `?` to display other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Andere verfügbare Aktionen" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="13275-120">Andere verfügbare Aktionen</span><span class="sxs-lookup"><span data-stu-id="13275-120">Other available actions</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="13275-121">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="13275-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deaktivieren von JavaScript mit Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio Codebenutzeroberfläche"  

> [!NOTE]
> <span data-ttu-id="13275-124">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13275-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="13275-125">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="13275-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="13275-127">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="13275-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
