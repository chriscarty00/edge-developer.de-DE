---
description: Ein Lernprogramm zu den am häufigsten verwendeten netzwerkbezogenen Features in Microsoft Edge devtools
title: Überprüfen der Netzwerkaktivität in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125426"
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

# <span data-ttu-id="98c53-104">Überprüfen der Netzwerkaktivität in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="98c53-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="98c53-105">Hierbei handelt es sich um ein praktisches Lernprogramm einiger der am häufigsten verwendeten devtools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.</span><span class="sxs-lookup"><span data-stu-id="98c53-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="98c53-106">Weitere Informationen finden Sie unter [Netzwerk Referenz][DevtoolsNetworkReference] , wenn Sie stattdessen Features durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="98c53-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="98c53-107">Verwendung des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="98c53-107">When to use the Network panel</span></span>  

<span data-ttu-id="98c53-108">Verwenden Sie im Allgemeinen das Netzwerk Panel, wenn Sie sicherstellen möchten, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="98c53-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="98c53-109">Die häufigsten Anwendungsfälle für das Netzwerk Panel sind:</span><span class="sxs-lookup"><span data-stu-id="98c53-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="98c53-110">Sicherstellen, dass Ressourcen tatsächlich hochgeladen oder überhaupt heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="98c53-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="98c53-111">Überprüfen der Eigenschaften einer einzelnen Ressource, wie HTTP-Header, Inhalt, Größe usw.</span><span class="sxs-lookup"><span data-stu-id="98c53-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="98c53-112">Wenn Sie nach Möglichkeiten suchen, die Seiten Ladeleistung zu verbessern, beginnen Sie **nicht** mit dem Netzwerk Panel.</span><span class="sxs-lookup"><span data-stu-id="98c53-112">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="98c53-113">Es gibt viele Arten von Problemen mit der Auslastungs Leistung, die nicht mit der Netzwerkaktivität zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="98c53-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="98c53-114">Beginnen Sie mit dem Überwachungs Panel, da Sie gezielte Vorschläge zum Verbessern Ihrer Seite erhalten.</span><span class="sxs-lookup"><span data-stu-id="98c53-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="98c53-115">Weitere Informationen finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="98c53-115">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="98c53-116">Öffnen des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="98c53-116">Open the Network panel</span></span>  

<span data-ttu-id="98c53-117">Um dieses Lernprogramm optimal zu nutzen, öffnen Sie die Demo und testen Sie die Features auf der Demo-Seite.</span><span class="sxs-lookup"><span data-stu-id="98c53-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="98c53-118">Öffnen [Sie die Demo für erste Schritte][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="98c53-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="98c53-120">Die Demo</span><span class="sxs-lookup"><span data-stu-id="98c53-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="Die Demo" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="98c53-121">[Öffnen Sie devtools][DevToolsOpen] , indem Sie `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="98c53-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="98c53-122">Das **Konsolen** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-122">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="98c53-124">Der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="98c53-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="98c53-125">Sie können [devtools am unteren Rand des Fensters andocken][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="98c53-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="98c53-127">DevTools an den unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="98c53-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-128">Wählen Sie die Registerkarte **Netzwerk** aus.  Das **Netzwerk** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-128">Select the **Network** tab.  The **Network** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="98c53-130">**Konsolen** Tool im devtools, das am unteren Rand des Fensters angedockt ist</span><span class="sxs-lookup"><span data-stu-id="98c53-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="98c53-131">Im Moment ist das Netzwerk Panel leer.</span><span class="sxs-lookup"><span data-stu-id="98c53-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="98c53-132">DevTools protokolliert nur Netzwerkaktivitäten, nachdem Sie Sie geöffnet haben und seit dem Öffnen von devtools keine Netzwerkaktivität stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="98c53-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="98c53-133">Protokollieren von Netzwerkaktivitäten</span><span class="sxs-lookup"><span data-stu-id="98c53-133">Log network activity</span></span>  

<span data-ttu-id="98c53-134">So zeigen Sie die Netzwerkaktivität an, die eine Seite verursacht:</span><span class="sxs-lookup"><span data-stu-id="98c53-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="98c53-135">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="98c53-135">Reload the page.</span></span>  <span data-ttu-id="98c53-136">Das Netzwerk Panel protokolliert alle Netzwerkaktivitäten im **Netzwerkprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="98c53-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="98c53-138">Das **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="98c53-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="98c53-139">Jede Zeile des **Netzwerkprotokolls** stellt eine Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="98c53-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="98c53-140">Standardmäßig werden die Ressourcen in chronologischer Reihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="98c53-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="98c53-141">Die oberste Ressource ist in der Regel das wichtigste HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="98c53-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="98c53-142">Die untere Ressource ist, was zuletzt angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="98c53-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="98c53-143">Jede Spalte stellt Informationen zu einer Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="98c53-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="98c53-144">In der vorhergehenden Abbildung werden die Standardspalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="98c53-145">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-145">**Status**.</span></span>  <span data-ttu-id="98c53-146">Der HTTP-Statuscode für die Antwort.</span><span class="sxs-lookup"><span data-stu-id="98c53-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="98c53-147">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="98c53-147">**Type**.</span></span>  <span data-ttu-id="98c53-148">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="98c53-148">The resource type.</span></span>  
    *   <span data-ttu-id="98c53-149">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="98c53-149">**Initiator**.</span></span>  <span data-ttu-id="98c53-150">Die Ursache der Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="98c53-150">The cause of the resource request.</span></span>  <span data-ttu-id="98c53-151">Wenn Sie einen Link in der Spalte Initiator auswählen, gelangen Sie zu dem Quellcode, der die Anforderung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="98c53-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="98c53-152">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="98c53-152">**Time**.</span></span>  <span data-ttu-id="98c53-153">Die Dauer der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="98c53-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="98c53-154">**Wasserfall**.</span><span class="sxs-lookup"><span data-stu-id="98c53-154">**Waterfall**.</span></span>  <span data-ttu-id="98c53-155">Eine grafische Darstellung der verschiedenen Phasen der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="98c53-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="98c53-156">Zeigen Sie mit der Maus auf einen Wasserfall, um eine Unterbrechung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98c53-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="98c53-157">Das Diagramm oberhalb des Netzwerkprotokolls wird als Übersicht bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="98c53-158">Sie werden das Übersichtsdiagramm in diesem Lernprogramm nicht verwenden, sodass Sie es möglicherweise ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="98c53-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="98c53-159">Weitere Informationen finden Sie unter [Ausblenden des][DevtoolsReferenceHideOverview]Übersichtsbereichs.</span><span class="sxs-lookup"><span data-stu-id="98c53-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="98c53-160">Nachdem Sie devtools geöffnet haben, werden die Netzwerkaktivitäten im Netzwerkprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="98c53-161">Um dies zu veranschaulichen, schauen Sie sich zuerst den unteren Rand des **Netzwerkprotokolls** an und machen Sie sich mit der letzten Aktivität auf den Kopf.</span><span class="sxs-lookup"><span data-stu-id="98c53-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="98c53-162">Wählen Sie nun in der Demo die Schaltfläche **Daten abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="98c53-163">Sehen Sie sich die untere Seite des **Netzwerkprotokolls** erneut an.</span><span class="sxs-lookup"><span data-stu-id="98c53-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="98c53-164">Es sollte eine neue Ressource mit dem Namen angezeigt werden `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="98c53-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="98c53-165">Durch Auswählen der Schaltfläche " **Daten abrufen** " wurde die Datei von der Seite angefordert.</span><span class="sxs-lookup"><span data-stu-id="98c53-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="98c53-167">Eine neue Ressource im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="98c53-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="98c53-168">Weitere Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="98c53-168">Show more information</span></span>  

<span data-ttu-id="98c53-169">Die Spalten des Netzwerkprotokolls können konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="98c53-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="98c53-170">Sie können Spalten, die Sie nicht verwenden, ausblenden.</span><span class="sxs-lookup"><span data-stu-id="98c53-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="98c53-171">Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind, die Sie möglicherweise als nützlich empfinden.</span><span class="sxs-lookup"><span data-stu-id="98c53-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="98c53-172">Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Netzwerkprotokoll Tabelle, und wählen Sie **Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-172">Right-click the header of the Network Log table and choose **Domain**.</span></span>  <span data-ttu-id="98c53-173">Die Domäne jeder Ressource wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="98c53-175">Aktivieren der Spalte "Domäne"</span><span class="sxs-lookup"><span data-stu-id="98c53-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="98c53-176">Zeigen Sie die vollständige URL einer Ressource an, indem Sie in der Spalte **Name** auf die Zelle zeigen.</span><span class="sxs-lookup"><span data-stu-id="98c53-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="98c53-177">Simulieren einer langsameren Netzwerkverbindung</span><span class="sxs-lookup"><span data-stu-id="98c53-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="98c53-178">Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Websites verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte ihrer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="98c53-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="98c53-179">Durch Drosselung der Seite erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät dauert.</span><span class="sxs-lookup"><span data-stu-id="98c53-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="98c53-180">Wählen Sie die Dropdownliste **Drosselung** aus, die standardmäßig auf **Online** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="98c53-180">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="98c53-182">Aktivieren der Drosselung</span><span class="sxs-lookup"><span data-stu-id="98c53-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-183">Wählen Sie **Slow 3G**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="98c53-185">Wählen Sie Slow 3G aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-186">Lange drücken Sie **Reload** (Reload ![ ][ImageRefreshIcon] \), und wählen Sie dann **Cache leeren und Hard Reload**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="98c53-188">Leerer Cache und schweres erneutes Laden</span><span class="sxs-lookup"><span data-stu-id="98c53-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="98c53-189">Bei wiederholten Besuchen dient der Browser in der Regel einigen Dateien aus dem [Cache][MDNHTTPCache], wodurch die Seitenauslastung beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="98c53-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="98c53-190">**Leerer Cache und harter Reload** erzwingt den Browser, das Netzwerk für alle Ressourcen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="98c53-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="98c53-191">Dies ist hilfreich, wenn Sie sehen möchten, wie ein Erstbesucher eine Seitenbelastung erlebt.</span><span class="sxs-lookup"><span data-stu-id="98c53-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="98c53-192">Der Workflow " **leerer Cache" und "harter Reload** " steht nur zur Verfügung, wenn devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="98c53-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="98c53-193">Screenshots aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="98c53-193">Capture screenshots</span></span>  

<span data-ttu-id="98c53-194">Mit Screenshots können Sie sehen, wie eine Seite im Laufe der Zeit aussah, während Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="98c53-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="98c53-195">Wählen Sie \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und aktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="98c53-195">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="98c53-196">Laden Sie die Seite erneut über den **leeren Cache und** den Arbeitsablauf für das erneute Laden.</span><span class="sxs-lookup"><span data-stu-id="98c53-196">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="98c53-197">Weitere Informationen hierzu finden Sie unter [Simulieren einer langsameren Verbindung](#simulate-a-slower-network-connection) .</span><span class="sxs-lookup"><span data-stu-id="98c53-197">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="98c53-198">Der Bereich "Screenshots" bietet Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten aussah.</span><span class="sxs-lookup"><span data-stu-id="98c53-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="98c53-200">Screenshots des Ladens der Seite</span><span class="sxs-lookup"><span data-stu-id="98c53-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-201">Wählen Sie die erste Miniaturansicht aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-201">Select the first thumbnail.</span></span>  <span data-ttu-id="98c53-202">DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="98c53-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="98c53-204">Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat</span><span class="sxs-lookup"><span data-stu-id="98c53-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-205">Wählen Sie erneut \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und deaktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** , um den Bereich Screenshots zu schließen.</span><span class="sxs-lookup"><span data-stu-id="98c53-205">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="98c53-206">Laden Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="98c53-206">Reload the page again.</span></span>  
    
## <span data-ttu-id="98c53-207">Überprüfen der Details der Ressource</span><span class="sxs-lookup"><span data-stu-id="98c53-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="98c53-208">Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98c53-208">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="98c53-209">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="98c53-209">Try it now:</span></span>  

1.  <span data-ttu-id="98c53-210">Wählen Sie aus `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="98c53-210">Select `getstarted.html`.</span></span>  <span data-ttu-id="98c53-211">Die Registerkarte über **Schriften** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="98c53-212">Verwenden Sie diese Registerkarte, um HTTP-Header zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="98c53-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="98c53-214">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="98c53-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-215">Wählen Sie die Registerkarte **Vorschau** aus.  Eine grundlegende Darstellung des HTML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-215">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="98c53-217">Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="98c53-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="98c53-218">Diese Registerkarte ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="98c53-218">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="98c53-219">Möglicherweise ist es einfacher, den gerenderten HTML-Code zu lesen als den HTML-Quellcode, oder wenn Sie Bilder untersuchen.</span><span class="sxs-lookup"><span data-stu-id="98c53-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="98c53-220">Wählen Sie die Registerkarte **Antwort** aus.  Der HTML-Quellcode wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-220">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="98c53-222">Die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="98c53-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="98c53-223">Wenn eine Datei minimierte ist, wird durch Auswählen der Schaltfläche **Format** \ ( ![ Format ][ImageFormatIcon] \) am unteren Rand der Registerkarte **Antwort** der Inhalt der Datei zur Lesbarkeit neu formatiert.</span><span class="sxs-lookup"><span data-stu-id="98c53-223">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="98c53-224">Wählen Sie die Registerkarte **Anzeige** Dauer aus.  Eine Aufschlüsselung der Netzwerkaktivität für diese Ressource wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-224">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="98c53-226">Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="98c53-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-227">Wählen Sie **Schließen** \ ( ![ Schließen ][ImageCloseIcon] \) aus, um das Netzwerkprotokoll erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98c53-227">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="98c53-229">Schaltfläche " **Schließen** "</span><span class="sxs-lookup"><span data-stu-id="98c53-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="98c53-230">Durchsuchen von Netzwerk Kopfzeilen und-Antworten</span><span class="sxs-lookup"><span data-stu-id="98c53-230">Search network headers and responses</span></span>  

<span data-ttu-id="98c53-231">Verwenden Sie den **Such** Bereich, wenn Sie die HTTP-Header und Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="98c53-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="98c53-232">Angenommen, Sie möchten beispielsweise überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien**verwenden.</span><span class="sxs-lookup"><span data-stu-id="98c53-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="98c53-233">Wählen Sie **Suchen** \ ( ![ Suchen ][ImageSearchIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-233">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="98c53-234">Der Suchbereich wird links neben dem Netzwerkprotokoll geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="98c53-236">Der **Such** Bereich</span><span class="sxs-lookup"><span data-stu-id="98c53-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-237">Geben `Cache-Control` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="98c53-237">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="98c53-238">Der Suchbereich listet alle Instanzen auf `Cache-Control` , die in Ressourcen Kopfzeilen oder-Inhalten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="98c53-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="98c53-240">Suchergebnisse‎‏ für: </span><span class="sxs-lookup"><span data-stu-id="98c53-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-241">Wählen Sie ein Ergebnis aus, um die Ressource anzuzeigen, in der das Ergebnis gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="98c53-241">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="98c53-242">Wenn Sie die Details der Ressource sehen möchten, wählen Sie ein Ergebnis aus, um direkt dorthin zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="98c53-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="98c53-243">Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird die Registerkarte Überschriften geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="98c53-244">Wenn die Abfrage im Inhalt gefunden wurde, wird die Registerkarte " **Antwort** " geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98c53-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="98c53-246">Auf der Registerkarte "über **Schriften** " hervorgehobenes Suchergebnis</span><span class="sxs-lookup"><span data-stu-id="98c53-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-247">Schließen Sie den Suchbereich und die Registerkarte Überschriften.</span><span class="sxs-lookup"><span data-stu-id="98c53-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="98c53-249">Die Schaltflächen " **Schließen** "</span><span class="sxs-lookup"><span data-stu-id="98c53-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="98c53-250">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98c53-250">Filter resources</span></span>  

<span data-ttu-id="98c53-251">DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="98c53-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="98c53-253">Die Symbolleiste " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="98c53-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="98c53-254">Die **Filter** Symbolleiste sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="98c53-254">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="98c53-255">Wenn nicht,:</span><span class="sxs-lookup"><span data-stu-id="98c53-255">If not:</span></span>  

1.  <span data-ttu-id="98c53-256">Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98c53-256">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="98c53-257">Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98c53-257">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="98c53-258">Das Textfeld " **Filter** " unterstützt viele verschiedene Filterarten.</span><span class="sxs-lookup"><span data-stu-id="98c53-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="98c53-259">Geben Sie `png` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="98c53-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="98c53-260">Nur die Dateien, die den Text enthalten, `png` werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98c53-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="98c53-261">In diesem Fall sind die einzigen Dateien, die dem Filter entsprechen, die PNG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="98c53-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="98c53-263">Ein Zeichenfolgenfilter</span><span class="sxs-lookup"><span data-stu-id="98c53-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-264">Geben Sie `/.*\.[cj]s+$/` ein.</span><span class="sxs-lookup"><span data-stu-id="98c53-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="98c53-265">DevTools filtert jede Ressource mit einem Dateinamen, der nicht mit a `j` oder a, `c` gefolgt von 1 oder mehr Zeichen, endet `s` .</span><span class="sxs-lookup"><span data-stu-id="98c53-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="98c53-267">Ein Filter für reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="98c53-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-268">Geben Sie `-main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="98c53-268">Type `-main.css`.</span></span>  <span data-ttu-id="98c53-269">DevTools filtert aus `main.css` .</span><span class="sxs-lookup"><span data-stu-id="98c53-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="98c53-270">Wenn eine andere Datei mit dem Muster übereinstimmt, würden Sie ebenfalls herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="98c53-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="98c53-272">Ein negativer Filter</span><span class="sxs-lookup"><span data-stu-id="98c53-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-273">Geben Sie `domain:cdn.glitch.com` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="98c53-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="98c53-274">DevTools filtert jede Ressource mit einer URL ab, die dieser Domäne nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="98c53-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="98c53-276">Ein Eigenschaften Filter</span><span class="sxs-lookup"><span data-stu-id="98c53-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="98c53-277">Die vollständige Liste der filterbaren Eigenschaften finden Sie unter [Filtern von Anforderungen nach Eigenschaften][DevtoolsReferenceProperty] .</span><span class="sxs-lookup"><span data-stu-id="98c53-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="98c53-278">Deaktivieren Sie das Textfeld " **Filter** " eines beliebigen Texts.</span><span class="sxs-lookup"><span data-stu-id="98c53-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="98c53-279">Nach Ressourcentyp Filtern</span><span class="sxs-lookup"><span data-stu-id="98c53-279">Filter by resource type</span></span>  

<span data-ttu-id="98c53-280">So konzentrieren Sie sich auf eine bestimmte Art von Datei, beispielsweise Stylesheets:</span><span class="sxs-lookup"><span data-stu-id="98c53-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="98c53-281">Wählen Sie **CSS**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-281">Choose **CSS**.</span></span>  <span data-ttu-id="98c53-282">Alle anderen Dateitypen werden herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="98c53-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="98c53-284">Nur CSS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="98c53-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-285">Wenn Sie auch Skripts anzeigen möchten, halten Sie `Control` \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann **js**aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-285">To also see scripts, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="98c53-287">Nur CSS-und JS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="98c53-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-288">Wählen Sie **alle** aus, um die Filter zu entfernen und alle Ressourcen erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98c53-288">Choose **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="98c53-289">Weitere Informationen finden Sie unter [Filteranforderungen][DevtoolsNetworkReferenceFilter] für andere Filter Workflows.</span><span class="sxs-lookup"><span data-stu-id="98c53-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="98c53-290">Anfragen blockieren</span><span class="sxs-lookup"><span data-stu-id="98c53-290">Block requests</span></span>  

<span data-ttu-id="98c53-291">Wie wird eine Seite aussehen und sich Verhalten, wenn einige Seitenressourcen nicht verfügbar sind?</span><span class="sxs-lookup"><span data-stu-id="98c53-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="98c53-292">Funktioniert es nicht vollständig, oder ist es immer noch etwas funktionell?</span><span class="sxs-lookup"><span data-stu-id="98c53-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="98c53-293">Anfragen blockieren, um Folgendes zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="98c53-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="98c53-294">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="98c53-294">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="98c53-296">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="98c53-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-297">Geben `block` Sie die Option **Blockierungs Anforderung anzeigen**ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="98c53-297">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="98c53-299">Anforderungs Blockierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="98c53-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-300">Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="98c53-300">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="98c53-301">Geben Sie `main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="98c53-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="98c53-303">Blockieren</span><span class="sxs-lookup"><span data-stu-id="98c53-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-304">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="98c53-304">Choose **Add**.</span></span>  
1.  <span data-ttu-id="98c53-305">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="98c53-305">Reload the page.</span></span>  <span data-ttu-id="98c53-306">Wie erwartet, wird das Design der Seite etwas durcheinander gebracht, da das Haupt-Stylesheet blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="98c53-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="98c53-307">Die `main.css` Zeile im Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="98c53-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="98c53-308">Der rote Text bedeutet, dass die Ressource blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="98c53-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="98c53-310">wurde blockiert</span><span class="sxs-lookup"><span data-stu-id="98c53-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="98c53-311">Deaktivieren Sie das Kontrollkästchen **Anforderungs Blockierung aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="98c53-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="98c53-312">Fazit</span><span class="sxs-lookup"><span data-stu-id="98c53-312">Conclusion</span></span>  

<span data-ttu-id="98c53-313">Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="98c53-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="98c53-314">Sie wissen jetzt, wie Sie das **Netzwerk** Panel im Microsoft Edge-devtools verwenden!</span><span class="sxs-lookup"><span data-stu-id="98c53-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="98c53-315">Navigieren Sie zu der [Netzwerk Referenz][DevtoolsNetworkReference] , um weitere devtools-Features im Zusammenhang mit der Überprüfung von Netzwerkaktivitäten zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="98c53-315">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <span data-ttu-id="98c53-316">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="98c53-316">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> <span data-ttu-id="98c53-326">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98c53-326">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="98c53-327">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="98c53-327">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="98c53-329">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98c53-329">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
