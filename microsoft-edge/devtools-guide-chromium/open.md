---
title: Öffnen von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601887"
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
   limitations under the License. -->





# <span data-ttu-id="900f9-103">Öffnen von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="900f9-103">Open Microsoft Edge DevTools</span></span>   



<span data-ttu-id="900f9-104">Es gibt viele Möglichkeiten, Microsoft Edge devtools zu öffnen, da unterschiedliche Benutzer schnellen Zugriff auf verschiedene Teile der devtools-Benutzeroberfläche wünschen.</span><span class="sxs-lookup"><span data-stu-id="900f9-104">There are many ways to open Microsoft Edge DevTools, because different users want fast access to different parts of the DevTools UI.</span></span>  

## <span data-ttu-id="900f9-105">Öffnen des Elements Panels zum Überprüfen des DOM oder CSS</span><span class="sxs-lookup"><span data-stu-id="900f9-105">Open the Elements panel to inspect the DOM or CSS</span></span>   

<span data-ttu-id="900f9-106">Wenn Sie die Formatvorlagen oder Attribute eines DOM-Knotens überprüfen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="900f9-106">When you want to inspect the styles or attributes of a DOM node, right-click the element and select **Inspect**.</span></span>  

> ##### <span data-ttu-id="900f9-107">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="900f9-107">Figure 1</span></span>  
> <span data-ttu-id="900f9-108">Die Option "über **prüfen** "</span><span class="sxs-lookup"><span data-stu-id="900f9-108">The **Inspect** option</span></span>  
> ![Die Option "überprüfen"][ImageInspectOption]  

<span data-ttu-id="900f9-110">Oder drücken Sie `Control` + `Shift` + `C` \ (Windows \) oder `Command` + `Option` + `C` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="900f9-110">Or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Option`+`C` \(macOS\).</span></span>  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <span data-ttu-id="900f9-111">Öffnen des Konsolen Panels zum Anzeigen von protokollierten Nachrichten oder Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="900f9-111">Open the Console panel to view logged messages or run JavaScript</span></span>   

<span data-ttu-id="900f9-112">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um direkt in den **Konsolen** Fenster zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="900f9-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to jump straight into the **Console** panel.</span></span>  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## <span data-ttu-id="900f9-113">Öffnen des letzten geöffneten Panels</span><span class="sxs-lookup"><span data-stu-id="900f9-113">Open the last panel you had open</span></span>   

<span data-ttu-id="900f9-114">Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="900f9-114">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  

## <span data-ttu-id="900f9-115">Öffnen von devtools über das Haupt Menü von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="900f9-115">Open DevTools from the Microsoft Edge main menu</span></span>  

<span data-ttu-id="900f9-116">Klicken Sie auf **Einstellungen und mehr \ (Alt + F \)** `...` , und wählen Sie dann **Weitere Tools**-  >  **Entwicklertools**aus.</span><span class="sxs-lookup"><span data-stu-id="900f9-116">Click **Settings and more \(Alt+F\)** `...` and then select **More Tools** > **Developer Tools**.</span></span>  

> ##### <span data-ttu-id="900f9-117">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="900f9-117">Figure 2</span></span>  
> <span data-ttu-id="900f9-118">Öffnen von devtools über das Microsoft Edge-Hauptmenü</span><span class="sxs-lookup"><span data-stu-id="900f9-118">Opening DevTools from the Microsoft Edge main menu</span></span>  
> ![Öffnen von devtools über das Microsoft Edge-Hauptmenü][ImageOpenFromMain]  

## <span data-ttu-id="900f9-120">Automatisches Öffnen von devtools auf jeder neuen Registerkarte</span><span class="sxs-lookup"><span data-stu-id="900f9-120">Auto-open DevTools on every new tab</span></span>   

<span data-ttu-id="900f9-121">Öffnen Sie Microsoft Edge über die Befehlszeile, und übergeben Sie die `--auto-open-devtools-for-tabs` Kennzeichnung.</span><span class="sxs-lookup"><span data-stu-id="900f9-121">Open Microsoft Edge from the command line and pass the `--auto-open-devtools-for-tabs` flag.</span></span>  

<span data-ttu-id="900f9-122">Windows \ (cmd \):</span><span class="sxs-lookup"><span data-stu-id="900f9-122">Windows \(CMD\):</span></span>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

<span data-ttu-id="900f9-123">Windows \ (PowerShell \):</span><span class="sxs-lookup"><span data-stu-id="900f9-123">Windows \(PowerShell\):</span></span>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

<span data-ttu-id="900f9-124">macOS</span><span class="sxs-lookup"><span data-stu-id="900f9-124">macOS:</span></span>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Abbildung 1: die Option "überprüfen""  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Abbildung 2: Öffnen von devtools aus dem Microsoft Edge-Hauptmenü"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> <span data-ttu-id="900f9-127">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="900f9-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="900f9-128">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/open) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="900f9-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/open) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="900f9-130">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="900f9-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
