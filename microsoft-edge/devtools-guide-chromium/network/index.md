---
title: Überprüfen der Netzwerkaktivität in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: cca9a45dae5ee845a219ef3f29c54a99e1ee904a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985617"
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





# <span data-ttu-id="c32d2-103">Überprüfen der Netzwerkaktivität in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="c32d2-103">Inspect network activity in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c32d2-104">Hierbei handelt es sich um ein praktisches Lernprogramm einiger der am häufigsten verwendeten devtools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.</span><span class="sxs-lookup"><span data-stu-id="c32d2-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="c32d2-105">Weitere Informationen finden Sie unter [Netzwerk Referenz][DevtoolsNetworkReference] , wenn Sie stattdessen Features durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="c32d2-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="c32d2-106">Verwendung des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="c32d2-106">When to use the Network panel</span></span>   

<span data-ttu-id="c32d2-107">Verwenden Sie im Allgemeinen das Netzwerk Panel, wenn Sie sicherstellen möchten, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="c32d2-108">Die häufigsten Anwendungsfälle für das Netzwerk Panel sind:</span><span class="sxs-lookup"><span data-stu-id="c32d2-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="c32d2-109">Sicherstellen, dass Ressourcen tatsächlich hochgeladen oder überhaupt heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="c32d2-110">Überprüfen der Eigenschaften einer einzelnen Ressource, wie HTTP-Header, Inhalt, Größe usw.</span><span class="sxs-lookup"><span data-stu-id="c32d2-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="c32d2-111">Wenn Sie nach Möglichkeiten suchen, die Seiten Ladeleistung zu verbessern, beginnen Sie **nicht** mit dem Netzwerk Panel.</span><span class="sxs-lookup"><span data-stu-id="c32d2-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="c32d2-112">Es gibt viele Arten von Problemen mit der Auslastungs Leistung, die nicht mit der Netzwerkaktivität zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="c32d2-113">Beginnen Sie mit dem Überwachungs Panel, da Sie gezielte Vorschläge zum Verbessern Ihrer Seite erhalten.</span><span class="sxs-lookup"><span data-stu-id="c32d2-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="c32d2-114">Weitere Informationen finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c32d2-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="c32d2-115">Öffnen des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="c32d2-115">Open the Network panel</span></span>   

<span data-ttu-id="c32d2-116">Um dieses Lernprogramm optimal zu nutzen, öffnen Sie die Demo und testen Sie die Features auf der Demo-Seite.</span><span class="sxs-lookup"><span data-stu-id="c32d2-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="c32d2-117">Öffnen [Sie die Demo für erste Schritte][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c32d2-117">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="c32d2-119">Die Demo</span><span class="sxs-lookup"><span data-stu-id="c32d2-119">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="c32d2-120">[Öffnen Sie devtools][DevToolsOpen] , indem Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="c32d2-120">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="c32d2-121">Das **Konsolen** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-121">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Der Konsole" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="c32d2-123">Der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="c32d2-123">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c32d2-124">Sie können [devtools am unteren Rand des Fensters andocken][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="c32d2-124">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools an den unteren Rand des Fensters angedockt" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="c32d2-126">DevTools an den unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="c32d2-126">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-127">Wählen Sie die Registerkarte **Netzwerk** aus.  Das Netzwerkfenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-127">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="DevTools an den unteren Rand des Fensters angedockt" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="c32d2-129">DevTools an den unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="c32d2-129">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c32d2-130">Im Moment ist das Netzwerk Panel leer.</span><span class="sxs-lookup"><span data-stu-id="c32d2-130">Right now the Network panel is empty.</span></span>  <span data-ttu-id="c32d2-131">DevTools protokolliert nur Netzwerkaktivitäten, nachdem Sie Sie geöffnet haben und seit dem Öffnen von devtools keine Netzwerkaktivität stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="c32d2-131">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="c32d2-132">Protokollieren von Netzwerkaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c32d2-132">Log network activity</span></span>   

<span data-ttu-id="c32d2-133">So zeigen Sie die Netzwerkaktivität an, die eine Seite verursacht:</span><span class="sxs-lookup"><span data-stu-id="c32d2-133">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="c32d2-134">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c32d2-134">Reload the page.</span></span>  <span data-ttu-id="c32d2-135">Das Netzwerk Panel protokolliert alle Netzwerkaktivitäten im **Netzwerkprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="c32d2-135">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Das Netzwerkprotokoll" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="c32d2-137">Das **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="c32d2-137">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c32d2-138">Jede Zeile des **Netzwerkprotokolls** stellt eine Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="c32d2-138">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="c32d2-139">Standardmäßig werden die Ressourcen in chronologischer Reihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-139">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="c32d2-140">Die oberste Ressource ist in der Regel das wichtigste HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="c32d2-140">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="c32d2-141">Die untere Ressource ist, was zuletzt angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="c32d2-141">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="c32d2-142">Jede Spalte stellt Informationen zu einer Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="c32d2-142">Each column represents information about a resource.</span></span>  <span data-ttu-id="c32d2-143">In der vorhergehenden Abbildung werden die Standardspalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-143">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="c32d2-144">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-144">**Status**.</span></span>  <span data-ttu-id="c32d2-145">Der HTTP-Statuscode für die Antwort.</span><span class="sxs-lookup"><span data-stu-id="c32d2-145">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="c32d2-146">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="c32d2-146">**Type**.</span></span>  <span data-ttu-id="c32d2-147">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="c32d2-147">The resource type.</span></span>  
    *   <span data-ttu-id="c32d2-148">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="c32d2-148">**Initiator**.</span></span>  <span data-ttu-id="c32d2-149">Die Ursache der Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="c32d2-149">The cause of the resource request.</span></span>  <span data-ttu-id="c32d2-150">Wenn Sie einen Link in der Spalte Initiator auswählen, gelangen Sie zu dem Quellcode, der die Anforderung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c32d2-150">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="c32d2-151">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="c32d2-151">**Time**.</span></span>  <span data-ttu-id="c32d2-152">Die Dauer der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c32d2-152">The duration of the request.</span></span>  
    *   <span data-ttu-id="c32d2-153">**Wasserfall**.</span><span class="sxs-lookup"><span data-stu-id="c32d2-153">**Waterfall**.</span></span>  <span data-ttu-id="c32d2-154">Eine grafische Darstellung der verschiedenen Phasen der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c32d2-154">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="c32d2-155">Zeigen Sie mit der Maus auf einen Wasserfall, um eine Unterbrechung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-155">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c32d2-156">Das Diagramm oberhalb des Netzwerkprotokolls wird als Übersicht bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-156">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="c32d2-157">Sie werden das Übersichtsdiagramm in diesem Lernprogramm nicht verwenden, sodass Sie es möglicherweise ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="c32d2-157">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="c32d2-158">Weitere Informationen finden Sie unter [Ausblenden des][DevtoolsReferenceHideOverview]Übersichtsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c32d2-158">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="c32d2-159">Nachdem Sie devtools geöffnet haben, werden die Netzwerkaktivitäten im Netzwerkprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-159">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="c32d2-160">Um dies zu veranschaulichen, schauen Sie sich zuerst den unteren Rand des **Netzwerkprotokolls** an und machen Sie sich mit der letzten Aktivität auf den Kopf.</span><span class="sxs-lookup"><span data-stu-id="c32d2-160">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="c32d2-161">Wählen Sie nun in der Demo die Schaltfläche **Daten abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-161">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="c32d2-162">Sehen Sie sich die untere Seite des **Netzwerkprotokolls** erneut an.</span><span class="sxs-lookup"><span data-stu-id="c32d2-162">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="c32d2-163">Es sollte eine neue Ressource mit dem Namen angezeigt werden `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-163">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="c32d2-164">Durch Auswählen der Schaltfläche " **Daten abrufen** " wurde die Datei von der Seite angefordert.</span><span class="sxs-lookup"><span data-stu-id="c32d2-164">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Eine neue Ressource im Netzwerkprotokoll" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="c32d2-166">Eine neue Ressource im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="c32d2-166">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c32d2-167">Weitere Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="c32d2-167">Show more information</span></span>   

<span data-ttu-id="c32d2-168">Die Spalten des Netzwerkprotokolls können konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-168">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="c32d2-169">Sie können Spalten, die Sie nicht verwenden, ausblenden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-169">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="c32d2-170">Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind, die Sie möglicherweise als nützlich empfinden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-170">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="c32d2-171">Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Netzwerkprotokoll Tabelle, und wählen Sie **Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-171">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="c32d2-172">Die Domäne jeder Ressource wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-172">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Aktivieren der Spalte "Domäne"" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="c32d2-174">Aktivieren der Spalte "Domäne"</span><span class="sxs-lookup"><span data-stu-id="c32d2-174">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="c32d2-175">Zeigen Sie die vollständige URL einer Ressource an, indem Sie in der Spalte **Name** auf die Zelle zeigen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-175">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="c32d2-176">Simulieren einer langsameren Netzwerkverbindung</span><span class="sxs-lookup"><span data-stu-id="c32d2-176">Simulate a slower network connection</span></span>   

<span data-ttu-id="c32d2-177">Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Websites verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte ihrer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c32d2-177">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="c32d2-178">Durch Drosselung der Seite erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät dauert.</span><span class="sxs-lookup"><span data-stu-id="c32d2-178">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="c32d2-179">Wählen Sie die Dropdownliste **Drosselung** aus, die standardmäßig auf **Online** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c32d2-179">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Aktivieren der Drosselung" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="c32d2-181">Aktivieren der Drosselung</span><span class="sxs-lookup"><span data-stu-id="c32d2-181">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-182">Wählen Sie **Slow 3G**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-182">Select **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Wählen Sie Slow 3G aus." lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="c32d2-184">Wählen Sie Slow 3G aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-184">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-185">Lange drücken Sie **Reload** (Reload ![ ][ImageRefreshIcon] \), und wählen Sie dann **Cache leeren und Hard Reload**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-185">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then select **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Leerer Cache und schweres erneutes Laden" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="c32d2-187">Leerer Cache und schweres erneutes Laden</span><span class="sxs-lookup"><span data-stu-id="c32d2-187">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="c32d2-188">Bei wiederholten Besuchen dient der Browser in der Regel einigen Dateien aus dem [Cache][MDNHTTPCache], wodurch die Seitenauslastung beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="c32d2-188">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="c32d2-189">**Leerer Cache und harter Reload** erzwingt den Browser, das Netzwerk für alle Ressourcen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c32d2-189">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="c32d2-190">Dies ist hilfreich, wenn Sie sehen möchten, wie ein Erstbesucher eine Seitenbelastung erlebt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-190">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c32d2-191">Der Workflow " **leerer Cache" und "harter Reload** " steht nur zur Verfügung, wenn devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="c32d2-191">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="c32d2-192">Screenshots aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="c32d2-192">Capture screenshots</span></span>   

<span data-ttu-id="c32d2-193">Mit Screenshots können Sie sehen, wie eine Seite im Laufe der Zeit aussah, während Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c32d2-193">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="c32d2-194">Wählen Sie \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und aktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="c32d2-194">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="c32d2-195">Laden Sie die Seite erneut über den **leeren Cache und** den Arbeitsablauf für das erneute Laden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-195">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="c32d2-196">Weitere Informationen hierzu finden Sie unter [Simulieren einer langsameren Verbindung](#simulate-a-slower-network-connection) .</span><span class="sxs-lookup"><span data-stu-id="c32d2-196">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="c32d2-197">Der Bereich "Screenshots" bietet Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten aussah.</span><span class="sxs-lookup"><span data-stu-id="c32d2-197">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Screenshots des Ladens der Seite" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="c32d2-199">Screenshots des Ladens der Seite</span><span class="sxs-lookup"><span data-stu-id="c32d2-199">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-200">Wählen Sie die erste Miniaturansicht aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-200">Select the first thumbnail.</span></span>  <span data-ttu-id="c32d2-201">DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="c32d2-201">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="c32d2-203">Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat</span><span class="sxs-lookup"><span data-stu-id="c32d2-203">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-204">Wählen Sie erneut \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und deaktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** , um den Bereich Screenshots zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-204">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="c32d2-205">Laden Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="c32d2-205">Reload the page again.</span></span>  
    
## <span data-ttu-id="c32d2-206">Überprüfen der Details der Ressource</span><span class="sxs-lookup"><span data-stu-id="c32d2-206">Inspect the details of the resource</span></span>   

<span data-ttu-id="c32d2-207">Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c32d2-207">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="c32d2-208">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="c32d2-208">Try it now:</span></span>  

1.  <span data-ttu-id="c32d2-209">Wählen Sie aus `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-209">Select `getstarted.html`.</span></span>  <span data-ttu-id="c32d2-210">Die Registerkarte über **Schriften** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-210">The **Headers** tab is shown.</span></span>  <span data-ttu-id="c32d2-211">Verwenden Sie diese Registerkarte, um HTTP-Header zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-211">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="c32d2-213">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-213">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-214">Wählen Sie die Registerkarte **Vorschau** aus.  Eine grundlegende Darstellung des HTML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-214">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Registerkarte "Vorschau"" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="c32d2-216">Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-216">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c32d2-217">Diese Registerkarte ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-217">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="c32d2-218">Möglicherweise ist es einfacher, den gerenderten HTML-Code zu lesen als den HTML-Quellcode, oder wenn Sie Bilder untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-218">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="c32d2-219">Wählen Sie die Registerkarte **Antwort** aus.  Der HTML-Quellcode wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-219">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Die Registerkarte "Antwort"" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="c32d2-221">Die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-221">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="c32d2-222">Wenn eine Datei minimierte ist, wird durch Auswählen der Schaltfläche **Format** \ ( ![ Format ][ImageFormatIcon] \) am unteren Rand der Registerkarte **Antwort** der Inhalt der Datei zur Lesbarkeit neu formatiert.</span><span class="sxs-lookup"><span data-stu-id="c32d2-222">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="c32d2-223">Wählen Sie die Registerkarte **Anzeige** Dauer aus.  Eine Aufschlüsselung der Netzwerkaktivität für diese Ressource wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-223">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Registerkarte "Anzeigedauer"" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="c32d2-225">Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="c32d2-225">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-226">Wählen Sie **Schließen** \ ( ![ Schließen ][ImageCloseIcon] \) aus, um das Netzwerkprotokoll erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-226">Select **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Schaltfläche "Schließen"" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="c32d2-228">Schaltfläche " **Schließen** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-228">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c32d2-229">Durchsuchen von Netzwerk Kopfzeilen und-Antworten</span><span class="sxs-lookup"><span data-stu-id="c32d2-229">Search network headers and responses</span></span>   

<span data-ttu-id="c32d2-230">Verwenden Sie den **Such** Bereich, wenn Sie die HTTP-Header und Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-230">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="c32d2-231">Angenommen, Sie möchten beispielsweise überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien**verwenden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-231">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="c32d2-232">Wählen Sie **Suchen** \ ( ![ Suchen ][ImageSearchIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-232">Select **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="c32d2-233">Der Suchbereich wird links neben dem Netzwerkprotokoll geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-233">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Der Suchbereich" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="c32d2-235">Der **Such** Bereich</span><span class="sxs-lookup"><span data-stu-id="c32d2-235">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-236">Geben `Cache-Control` Sie ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-236">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="c32d2-237">Der Suchbereich listet alle Instanzen auf `Cache-Control` , die in Ressourcen Kopfzeilen oder-Inhalten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-237">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Suchergebnisse für Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="c32d2-239">Suchergebnisse‎‏ für: </span><span class="sxs-lookup"><span data-stu-id="c32d2-239">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-240">Wählen Sie ein Ergebnis aus, um die Ressource anzuzeigen, in der das Ergebnis gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c32d2-240">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="c32d2-241">Wenn Sie die Details der Ressource sehen möchten, wählen Sie ein Ergebnis aus, um direkt dorthin zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c32d2-241">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="c32d2-242">Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird die Registerkarte Überschriften geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-242">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="c32d2-243">Wenn die Abfrage im Inhalt gefunden wurde, wird die Registerkarte " **Antwort** " geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c32d2-243">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Auf der Registerkarte "Überschriften" hervorgehobenes Suchergebnis" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="c32d2-245">Auf der Registerkarte "über **Schriften** " hervorgehobenes Suchergebnis</span><span class="sxs-lookup"><span data-stu-id="c32d2-245">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-246">Schließen Sie den Suchbereich und die Registerkarte Überschriften.</span><span class="sxs-lookup"><span data-stu-id="c32d2-246">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Die Schaltflächen "Schließen"" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="c32d2-248">Die Schaltflächen " **Schließen** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-248">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c32d2-249">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c32d2-249">Filter resources</span></span>   

<span data-ttu-id="c32d2-250">DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="c32d2-250">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Die Symbolleiste "Filter"" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="c32d2-252">Die Symbolleiste " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="c32d2-252">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="c32d2-253">Die **Filter** Symbolleiste sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-253">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="c32d2-254">Wenn nicht,:</span><span class="sxs-lookup"><span data-stu-id="c32d2-254">If not:</span></span>  

1.  <span data-ttu-id="c32d2-255">Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-255">Select **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="c32d2-256">Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c32d2-256">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="c32d2-257">Das Textfeld " **Filter** " unterstützt viele verschiedene Filterarten.</span><span class="sxs-lookup"><span data-stu-id="c32d2-257">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="c32d2-258">Geben Sie `png` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-258">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="c32d2-259">Nur die Dateien, die den Text enthalten, `png` werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-259">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="c32d2-260">In diesem Fall sind die einzigen Dateien, die dem Filter entsprechen, die PNG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="c32d2-260">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Ein Zeichenfolgenfilter" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="c32d2-262">Ein Zeichenfolgenfilter</span><span class="sxs-lookup"><span data-stu-id="c32d2-262">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-263">Geben Sie `/.*\.[cj]s+$/` ein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-263">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="c32d2-264">DevTools filtert jede Ressource mit einem Dateinamen, der nicht mit a `j` oder a, `c` gefolgt von 1 oder mehr Zeichen, endet `s` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-264">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Ein Filter für reguläre Ausdrücke" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="c32d2-266">Ein Filter für reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="c32d2-266">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-267">Geben Sie `-main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-267">Type `-main.css`.</span></span>  <span data-ttu-id="c32d2-268">DevTools filtert aus `main.css` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-268">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="c32d2-269">Wenn eine andere Datei mit dem Muster übereinstimmt, würden Sie ebenfalls herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="c32d2-269">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Ein negativer Filter" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="c32d2-271">Ein negativer Filter</span><span class="sxs-lookup"><span data-stu-id="c32d2-271">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-272">Geben Sie `domain:cdn.glitch.com` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-272">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="c32d2-273">DevTools filtert jede Ressource mit einer URL ab, die dieser Domäne nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="c32d2-273">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Ein Eigenschaften Filter" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="c32d2-275">Ein Eigenschaften Filter</span><span class="sxs-lookup"><span data-stu-id="c32d2-275">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c32d2-276">Die vollständige Liste der filterbaren Eigenschaften finden Sie unter [Filtern von Anforderungen nach Eigenschaften][DevtoolsReferenceProperty] .</span><span class="sxs-lookup"><span data-stu-id="c32d2-276">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="c32d2-277">Deaktivieren Sie das Textfeld " **Filter** " eines beliebigen Texts.</span><span class="sxs-lookup"><span data-stu-id="c32d2-277">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="c32d2-278">Nach Ressourcentyp Filtern</span><span class="sxs-lookup"><span data-stu-id="c32d2-278">Filter by resource type</span></span>   

<span data-ttu-id="c32d2-279">So konzentrieren Sie sich auf eine bestimmte Art von Datei, beispielsweise Stylesheets:</span><span class="sxs-lookup"><span data-stu-id="c32d2-279">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="c32d2-280">Wählen Sie **CSS**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-280">Select **CSS**.</span></span>  <span data-ttu-id="c32d2-281">Alle anderen Dateitypen werden herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="c32d2-281">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Nur CSS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="c32d2-283">Nur CSS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="c32d2-283">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-284">Wenn Sie auch Skripts anzeigen möchten, halten Sie `Control` \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann **js**aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-284">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Nur CSS-und JS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="c32d2-286">Nur CSS-und JS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="c32d2-286">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-287">Wählen Sie **alle** aus, um die Filter zu entfernen und alle Ressourcen erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-287">Select **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="c32d2-288">Weitere Informationen finden Sie unter [Filteranforderungen][DevtoolsNetworkReferenceFilter] für andere Filter Workflows.</span><span class="sxs-lookup"><span data-stu-id="c32d2-288">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="c32d2-289">Anfragen blockieren</span><span class="sxs-lookup"><span data-stu-id="c32d2-289">Block requests</span></span>   

<span data-ttu-id="c32d2-290">Wie wird eine Seite aussehen und sich Verhalten, wenn einige Seitenressourcen nicht verfügbar sind?</span><span class="sxs-lookup"><span data-stu-id="c32d2-290">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="c32d2-291">Funktioniert es nicht vollständig, oder ist es immer noch etwas funktionell?</span><span class="sxs-lookup"><span data-stu-id="c32d2-291">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="c32d2-292">Anfragen blockieren, um Folgendes zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="c32d2-292">Block requests to find out:</span></span>  

1.  <span data-ttu-id="c32d2-293">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-293">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="c32d2-295">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="c32d2-295">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-296">Geben `block` Sie die Option **Blockierungs Anforderung anzeigen**ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c32d2-296">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Anforderungs Blockierung anzeigen" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="c32d2-298">Anforderungs Blockierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="c32d2-298">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-299">Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-299">Select **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="c32d2-300">Geben Sie `main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="c32d2-300">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blockieren von Main. CSS" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="c32d2-302">Blockieren</span><span class="sxs-lookup"><span data-stu-id="c32d2-302">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-303">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c32d2-303">Select **Add**.</span></span>  
1.  <span data-ttu-id="c32d2-304">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c32d2-304">Reload the page.</span></span>  <span data-ttu-id="c32d2-305">Wie erwartet, wird das Design der Seite etwas durcheinander gebracht, da das Haupt-Stylesheet blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c32d2-305">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c32d2-306">Die `main.css` Zeile im Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c32d2-306">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="c32d2-307">Der rote Text bedeutet, dass die Ressource blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c32d2-307">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Main. CSS wurde blockiert" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="c32d2-309">wurde blockiert</span><span class="sxs-lookup"><span data-stu-id="c32d2-309">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c32d2-310">Deaktivieren Sie das Kontrollkästchen **Anforderungs Blockierung aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c32d2-310">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="c32d2-311">Fazit</span><span class="sxs-lookup"><span data-stu-id="c32d2-311">Conclusion</span></span>  

<span data-ttu-id="c32d2-312">Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c32d2-312">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="c32d2-313">Sie wissen jetzt, wie Sie das **Netzwerk** Panel im Microsoft Edge-devtools verwenden!</span><span class="sxs-lookup"><span data-stu-id="c32d2-313">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<!--




-->  

<span data-ttu-id="c32d2-314">Schauen Sie sich die [Netzwerk Referenz][DevtoolsNetworkReference] an, um weitere devtools-Features im Zusammenhang mit der Überprüfung von Netzwerkaktivitäten zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="c32d2-314">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Position von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkReference]: ./reference.md "Netzwerkanalyse Referenz | Microsoft docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filter Anforderungen – Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ausblenden des Übersichtsbereichs-Netzwerkanalyse Referenz | Microsoft docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz | Microsoft docs"
[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools | Microsoft docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Überprüfen der Netzwerk Aktivitäts Demo | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> <span data-ttu-id="c32d2-324">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c32d2-324">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c32d2-325">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c32d2-325">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c32d2-327">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c32d2-327">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
