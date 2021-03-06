---
description: Verwenden Sie das Medientool, um Informationen anzuzeigen und die Media Player pro Browserregisterkarte zu debuggen.
title: Anzeigen und Debuggen von Informationen zu Media Playern
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 7680faa13f65a2ea6f0a8b085316b5ed67bfdaba
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398406"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="view-and-debug-media-players-information"></a><span data-ttu-id="ed40e-104">Anzeigen und Debuggen von Informationen zu Media Playern</span><span class="sxs-lookup"><span data-stu-id="ed40e-104">View and debug media players information</span></span>  

<span data-ttu-id="ed40e-105">Verwenden Sie **das Medientool** in Microsoft Edge DevTools, um Informationen anzuzeigen und die Media Player pro Browserregisterkarte zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="ed40e-105">Use the **Media** tool in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <a name="open-the-media-tool"></a><span data-ttu-id="ed40e-106">Öffnen des Medientools</span><span class="sxs-lookup"><span data-stu-id="ed40e-106">Open the Media tool</span></span>  

<span data-ttu-id="ed40e-107">Das **Medientool** ist der wichtigste Ort in DevTools zum Überprüfen des Media Players einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="ed40e-107">The **Media** tool is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="ed40e-108">[Öffnen Sie DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="ed40e-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="ed40e-109">Zum Öffnen des **Medienbereichs** wählen **Sie Anpassen und Steuern devTools** `...`  >  **Weitere Tools**  >  **Medien aus.**</span><span class="sxs-lookup"><span data-stu-id="ed40e-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Medienbereich" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="ed40e-111">**Medienbereich**</span><span class="sxs-lookup"><span data-stu-id="ed40e-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <a name="view-media-players-information"></a><span data-ttu-id="ed40e-112">Anzeigen von Informationen zu Media Playern</span><span class="sxs-lookup"><span data-stu-id="ed40e-112">View media players information</span></span>  

1.  <span data-ttu-id="ed40e-113">Navigieren Sie zu einer Webseite mit einem Media Player, z. B. der folgenden Webseite.</span><span class="sxs-lookup"><span data-stu-id="ed40e-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="ed40e-114">Maximieren der Produktivität mit den Edge-Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="ed40e-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="ed40e-115">Im Menü **Player** wird ein Media Player angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed40e-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="ed40e-116">Wählen Sie den Spieler aus.</span><span class="sxs-lookup"><span data-stu-id="ed40e-116">Choose the player.</span></span>  <span data-ttu-id="ed40e-117">Im **Bereich** Eigenschaften werden die Eigenschaften des Media Players angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed40e-117">The **Properties** panel displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Medieneigenschaften" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="ed40e-119">Medieneigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed40e-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ed40e-120">Um alle Media Player-Ereignisse anzeigen zu können, wählen Sie den **Bereich Ereignisse** aus.</span><span class="sxs-lookup"><span data-stu-id="ed40e-120">To view all the media player events, choose the **Events** panel.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Medienereignisse" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="ed40e-122">Medienereignisse</span><span class="sxs-lookup"><span data-stu-id="ed40e-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ed40e-123">Wählen Sie zum Anzeigen der Media Player-Nachrichtenprotokolle den **Bereich Nachrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="ed40e-123">To view the media player message logs, choose the **Messages** panel.</span></span>  <span data-ttu-id="ed40e-124">Sie können die Nachrichten nach Protokollebene oder Zeichenfolge filtern.</span><span class="sxs-lookup"><span data-stu-id="ed40e-124">You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mediennachrichten" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="ed40e-126">Mediennachrichten</span><span class="sxs-lookup"><span data-stu-id="ed40e-126">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ed40e-127">Im **Zeitachsenbereich** werden die Medienwiedergabe und der Pufferstatus live angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed40e-127">On the **Timeline** panel, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Medienzeitachse" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="ed40e-129">Medienzeitachse</span><span class="sxs-lookup"><span data-stu-id="ed40e-129">Media timeline</span></span>  
    :::image-end:::  
    
### <a name="remote-debugging"></a><span data-ttu-id="ed40e-130">Remotedebugging</span><span class="sxs-lookup"><span data-stu-id="ed40e-130">Remote debugging</span></span>  

<span data-ttu-id="ed40e-131">Zeigen Sie die Media Player-Informationen auf einem Android-Gerät von Ihrem Windows- oder macOS-Computer an.</span><span class="sxs-lookup"><span data-stu-id="ed40e-131">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="ed40e-132">Navigieren Sie zum Einrichten des Remotedebu debuggings zu [Erste Schritte mit Remotedebugen von Android-Geräten.][DevtoolsGuideChromiumRemoteDebuggingIndex]</span><span class="sxs-lookup"><span data-stu-id="ed40e-132">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="ed40e-133">Zeigen Sie die Media Player-Informationen remote an.</span><span class="sxs-lookup"><span data-stu-id="ed40e-133">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a><span data-ttu-id="ed40e-134">Ausblenden und Anzeigen von Media Playern</span><span class="sxs-lookup"><span data-stu-id="ed40e-134">Hide and show media players</span></span>  

<span data-ttu-id="ed40e-135">Manchmal führen Sie mehrere Media Player auf einer Webseite aus, oder verwenden Sie die gleiche Browserregisterkarte, um verschiedene Webseiten zu durchsuchen, jeweils mit Media Playern.</span><span class="sxs-lookup"><span data-stu-id="ed40e-135">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="ed40e-136">Sie können festlegen, dass \(oder show\) jeder Media Player ausgeblendet werden soll, um ein einfacheres Debuggen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ed40e-136">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="ed40e-137">Navigieren Sie mit derselben Browserregisterkarte zu mehreren verschiedenen Videoweb webseiten.</span><span class="sxs-lookup"><span data-stu-id="ed40e-137">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="ed40e-138">Führen Sie eine der folgenden Aktionen aus, um Media Player auszublenden.</span><span class="sxs-lookup"><span data-stu-id="ed40e-138">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="ed40e-139">Um einen Media Player auszublenden, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Player ausblenden aus.**</span><span class="sxs-lookup"><span data-stu-id="ed40e-139">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="ed40e-140">Um alle anderen Media Player auszublenden, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Alle anderen **ausblenden aus.**</span><span class="sxs-lookup"><span data-stu-id="ed40e-140">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ausblenden von Media Playern" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="ed40e-142">Ausblenden von Media Playern</span><span class="sxs-lookup"><span data-stu-id="ed40e-142">Hide media players</span></span>  
    :::image-end:::  
    
## <a name="export-media-player-information"></a><span data-ttu-id="ed40e-143">Exportieren von Media Player-Informationen</span><span class="sxs-lookup"><span data-stu-id="ed40e-143">Export media player information</span></span>  

1.  <span data-ttu-id="ed40e-144">Wenn Sie die Media Player-Informationen als JSON-Datei herunterladen möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Playerinformationen speichern aus.**</span><span class="sxs-lookup"><span data-stu-id="ed40e-144">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportieren von Medieninformationen" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="ed40e-146">Exportieren von Medieninformationen</span><span class="sxs-lookup"><span data-stu-id="ed40e-146">Export media information</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ed40e-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ed40e-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximieren der Produktivität mit den Edge-Entwicklertools | Bing Video"  

> [!NOTE]
> <span data-ttu-id="ed40e-151">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed40e-151">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ed40e-152">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed40e-152">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ed40e-154">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ed40e-154">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

