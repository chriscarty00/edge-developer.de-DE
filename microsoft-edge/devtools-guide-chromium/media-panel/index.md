---
description: Verwenden Sie das Medienfenster, um Informationen anzuzeigen und die Media Player pro Browser-Registerkarte zu debuggen.
title: Anzeigen und Debuggen von Medienplayer-Informationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e6259cf573b76df7e281527ad30360b8f473a165
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230950"
---
# <span data-ttu-id="9b3d2-104">Anzeigen und Debuggen von Medienplayer-Informationen</span><span class="sxs-lookup"><span data-stu-id="9b3d2-104">View and debug media players information</span></span>  

<span data-ttu-id="9b3d2-105">Verwenden Sie das **Medien** Fenster in Microsoft Edge devtools, um Informationen anzuzeigen und die Media Player pro Browser-Registerkarte zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="9b3d2-106">Öffnen des Medien Panels</span><span class="sxs-lookup"><span data-stu-id="9b3d2-106">Open the Media panel</span></span>  

<span data-ttu-id="9b3d2-107">Der **Medien** Bereich ist der wichtigste Ort in devtools, um den Media Player einer Webseite zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="9b3d2-108">[Öffnen Sie devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="9b3d2-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="9b3d2-109">Um das **Medien** Panel zu öffnen, wählen Sie **anpassen und Steuern devtools** `...`  >  **Weitere Tools**  >  **Medien**aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="9b3d2-111">**Medien** Panel</span><span class="sxs-lookup"><span data-stu-id="9b3d2-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9b3d2-112">Anzeigen von Informationen zu Medien Teilnehmern</span><span class="sxs-lookup"><span data-stu-id="9b3d2-112">View media players information</span></span>  

1.  <span data-ttu-id="9b3d2-113">Navigieren Sie zu einer Webseite mit einem Media Player, beispielsweise der folgenden Website.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="9b3d2-114">Maximieren der Produktivität mit den Edge-Entwickler Tools</span><span class="sxs-lookup"><span data-stu-id="9b3d2-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="9b3d2-115">Unter dem **Player** -Menü wird ein Media-Player angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="9b3d2-116">Wählen Sie den Player aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-116">Select the player.</span></span>  <span data-ttu-id="9b3d2-117">Auf der Registerkarte " **Eigenschaften** " werden die Eigenschaften des Media Players angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Medieneigenschaften" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="9b3d2-119">Medieneigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b3d2-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b3d2-120">Wenn Sie alle Media Player-Ereignisse anzeigen möchten, wählen Sie die Registerkarte **Ereignisse** aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Medienereignisse" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="9b3d2-122">Medienereignisse</span><span class="sxs-lookup"><span data-stu-id="9b3d2-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b3d2-123">Um die Media Player-Nachrichtenprotokolle anzuzeigen, wählen Sie die Registerkarte **Nachrichten** aus.  Sie können die Nachrichten nach Protokollebene oder Zeichenfolge filtern.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Medien Nachrichten" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="9b3d2-125">Medien Nachrichten</span><span class="sxs-lookup"><span data-stu-id="9b3d2-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b3d2-126">Auf der Registerkarte **Zeitachse** werden die Medienwiedergabe und der Pufferstatus Live angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Medienzeitachse" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="9b3d2-128">Medienzeitachse</span><span class="sxs-lookup"><span data-stu-id="9b3d2-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9b3d2-129">Remotedebugging</span><span class="sxs-lookup"><span data-stu-id="9b3d2-129">Remote debugging</span></span>  

<span data-ttu-id="9b3d2-130">Zeigen Sie die Medienwiedergabe Informationen auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus an.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="9b3d2-131">Wenn Sie das Remotedebuggen einrichten möchten, navigieren Sie zu den [ersten Schritten mit dem Remotedebuggen von Android-Geräten][DevtoolsGuideChromiumRemoteDebuggingIndex].</span><span class="sxs-lookup"><span data-stu-id="9b3d2-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="9b3d2-132">Anzeigen der Medienplayer-Informationen per Remotezugriff</span><span class="sxs-lookup"><span data-stu-id="9b3d2-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="9b3d2-133">Ausblenden und Anzeigen von Media Playern</span><span class="sxs-lookup"><span data-stu-id="9b3d2-133">Hide and show media players</span></span>  

<span data-ttu-id="9b3d2-134">Manchmal führen Sie mehr als einen Media Player auf einer Webseite aus, oder Sie verwenden dieselbe Browserregister Karte, um verschiedene Webseiten zu durchsuchen, die jeweils mit Media Playern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="9b3d2-135">Sie können festlegen, dass die einzelnen Media Player ausgeblendet werden, um das Debugging zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="9b3d2-136">Navigieren Sie mit der gleichen Browserregister Karte zu verschiedenen Video Webseiten.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="9b3d2-137">Wenn Sie Medienplayer ausblenden möchten, führen Sie eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="9b3d2-138">Wenn Sie einen Media Player ausblenden möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Player ausblenden**aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="9b3d2-139">Wenn Sie alle anderen Media Player ausblenden möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **alle anderen ausblenden**aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ausblenden von Media Playern" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="9b3d2-141">Ausblenden von Media Playern</span><span class="sxs-lookup"><span data-stu-id="9b3d2-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9b3d2-142">Exportieren von Media Player-Informationen</span><span class="sxs-lookup"><span data-stu-id="9b3d2-142">Export media player information</span></span>  

1.  <span data-ttu-id="9b3d2-143">Wenn Sie die Media Player-Informationen als JSON-Datei herunterladen möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Player-Informationen speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportieren von Medieninformationen" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="9b3d2-145">Exportieren von Medieninformationen</span><span class="sxs-lookup"><span data-stu-id="9b3d2-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9b3d2-146">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="9b3d2-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge (Chrom) devtools | Microsoft docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximieren der Produktivität mit den Edge-Entwickler Tools | Bing-Video"  

> [!NOTE]
> <span data-ttu-id="9b3d2-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9b3d2-151">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b3d2-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="9b3d2-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b3d2-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

