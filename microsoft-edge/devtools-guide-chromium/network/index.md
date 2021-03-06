---
description: Ein Lernprogramm zu den beliebtesten netzwerkbezogenen Features in Microsoft Edge DevTools.
title: Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 16b60716c91d2f4ce778f1fac37afc0e73e30ab6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398658"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a><span data-ttu-id="a3b8c-104">Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a3b8c-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="a3b8c-105">Dies ist ein praktisches Lernprogramm zu einigen der am häufigsten verwendeten DevTools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="a3b8c-106">Wenn Sie Features durchsuchen möchten, navigieren Sie zu [Netzwerkreferenz][DevtoolsNetworkReference].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-106">If you want to browse features, navigate to [Network Reference][DevtoolsNetworkReference].</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a><span data-ttu-id="a3b8c-107">Verwendung des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="a3b8c-107">When to use the Network panel</span></span>  

<span data-ttu-id="a3b8c-108">Verwenden Sie im Allgemeinen den Netzwerkbereich, wenn Sie sicherstellen müssen, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="a3b8c-109">Die häufigsten Verwendungsfälle für den Netzwerkbereich sind:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="a3b8c-110">Stellen Sie sicher, dass Ressourcen tatsächlich hochgeladen oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="a3b8c-111">Überprüfen der Eigenschaften einer einzelnen Ressource, z. B. http-Header, Inhalt, Größe und so weiter.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="a3b8c-112">Wenn Sie nach Möglichkeiten zur Verbesserung der Seitenladeleistung suchen, **beginnen Sie nicht** mit dem **Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="a3b8c-113">Es gibt viele Arten von Lastenleistungsproblemen, die nicht mit der Netzwerkaktivität in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="a3b8c-114">Beginnen Sie mit dem Prüfungspanel, da es Ihnen gezielte Vorschläge zur Verbesserung Ihrer Seite gibt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="a3b8c-115">Navigieren Sie zu [Optimieren der Websitegeschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <a name="open-the-network-panel"></a><span data-ttu-id="a3b8c-116">Öffnen des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="a3b8c-116">Open the Network panel</span></span>  

<span data-ttu-id="a3b8c-117">Um dieses Lernprogramm zu nutzen, öffnen Sie die Demo, und testen Sie die Features auf der Demoseite.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="a3b8c-118">Öffnen Sie [die Erste Schritte Demo][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="a3b8c-120">Die Demo</span><span class="sxs-lookup"><span data-stu-id="a3b8c-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="a3b8c-121">Wählen [Sie zum Öffnen von DevTools][DevToolsOpen] `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-121">To [Open DevTools][DevToolsOpen], select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="a3b8c-122">Das **Konsolentool** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Die Konsole" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="a3b8c-124">Die **Konsole**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="a3b8c-125">Möglicherweise docken Sie [DevTools am unteren Rand Des Fensters an.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="a3b8c-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools am unteren Rand des Fensters angedockt" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="a3b8c-127">DevTools am unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="a3b8c-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-128">Öffnen Sie das **Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-128">Open the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Konsolentool in den DevTools, die am unteren Rand des Fensters angedockt sind" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="a3b8c-130">**Konsolentool** in den DevTools, die am unteren Rand des Fensters angedockt sind</span><span class="sxs-lookup"><span data-stu-id="a3b8c-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="a3b8c-131">Derzeit ist das **Netzwerktool** leer.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-131">Right now the **Network** tool is empty.</span></span>  <span data-ttu-id="a3b8c-132">DevTools protokolliert die Netzwerkaktivität nur, nachdem Sie sie geöffnet haben, und es sind seit dem Öffnen von DevTools keine Netzwerkaktivitäten aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <a name="log-network-activity"></a><span data-ttu-id="a3b8c-133">Protokollnetzwerkaktivität</span><span class="sxs-lookup"><span data-stu-id="a3b8c-133">Log network activity</span></span>  

<span data-ttu-id="a3b8c-134">So zeigen Sie die Netzwerkaktivität an, die von einer Seite verursacht wird:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="a3b8c-135">Aktualisieren Sie die Webseite.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-135">Refresh the webpage.</span></span>  <span data-ttu-id="a3b8c-136">Im Netzwerkbereich werden alle Netzwerkaktivitäten im **Netzwerkprotokoll protokolliert.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Das Netzwerkprotokoll" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="a3b8c-138">Das **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="a3b8c-139">Jede Zeile des **Netzwerkprotokolls stellt** eine Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="a3b8c-140">Standardmäßig werden die Ressourcen chronologisch aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="a3b8c-141">Die wichtigste Ressource ist in der Regel das Haupt-HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="a3b8c-142">Die untere Ressource ist das, was zuletzt angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="a3b8c-143">Jede Spalte stellt Informationen zu einer Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="a3b8c-144">In der vorherigen Abbildung werden die Standardspalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="a3b8c-145">**Status**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-145">**Status**.</span></span>  <span data-ttu-id="a3b8c-146">Der HTTP-Statuscode für die Antwort.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="a3b8c-147">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-147">**Type**.</span></span>  <span data-ttu-id="a3b8c-148">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-148">The resource type.</span></span>  
    *   <span data-ttu-id="a3b8c-149">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-149">**Initiator**.</span></span>  <span data-ttu-id="a3b8c-150">Die Ursache der Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-150">The cause of the resource request.</span></span>  <span data-ttu-id="a3b8c-151">Wenn Sie einen Link in der Spalte Initiator verwenden, erhalten Sie den Quellcode, der die Anforderung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="a3b8c-152">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-152">**Time**.</span></span>  <span data-ttu-id="a3b8c-153">Die Dauer der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="a3b8c-154">**Wasserfall**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-154">**Waterfall**.</span></span>  <span data-ttu-id="a3b8c-155">Eine grafische Darstellung der verschiedenen Phasen der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="a3b8c-156">Zeigen Sie zum Anzeigen einer Aufschlüsselung auf einen Wasserfall.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-156">To display a breakdown, hover on a Waterfall.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a3b8c-157">Das Diagramm über dem Netzwerkprotokoll wird als Übersicht bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="a3b8c-158">Sie verwenden das Diagramm Übersicht in diesem Lernprogramm nicht, daher können Sie es ausblenden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="a3b8c-159">Navigieren Sie zu [Ausblenden des Übersichtsbereichs][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-159">Navigate to [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="a3b8c-160">Nachdem Sie DevTools geöffnet haben, wird die Netzwerkaktivität im Netzwerkprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="a3b8c-161">Um dies zu veranschaulichen, \*\*\*\* sehen Sie sich zunächst den unteren Rand des Netzwerkprotokolls an, und notieren Sie sich die letzte Aktivität.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="a3b8c-162">Wählen Sie nun in der **Demo** die Schaltfläche Daten herunterladen aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="a3b8c-163">Sehen Sie sich das Netzwerkprotokoll unten **erneut** an.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="a3b8c-164">Eine neue Ressource namens `getstarted.json` wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-164">A new resource named `getstarted.json` is displayed.</span></span>  <span data-ttu-id="a3b8c-165">Um zu verursachen, dass die Webseite die Datei angibt, wählen Sie die Schaltfläche **Daten** anfordern aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-165">To cause the webpage to request the file, choose the **Get Data** button.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Eine neue Ressource im Netzwerkprotokoll" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="a3b8c-167">Eine neue Ressource im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <a name="show-more-information"></a><span data-ttu-id="a3b8c-168">Weitere Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-168">Show more information</span></span>  

<span data-ttu-id="a3b8c-169">Die Spalten des Netzwerkprotokolls können konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="a3b8c-170">Sie können Spalten ausblenden, die Sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="a3b8c-171">Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind und möglicherweise hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="a3b8c-172">Zeigen Sie auf die Kopfzeile der Tabelle Netzwerkprotokoll, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Domäne aus.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="a3b8c-173">Die Domäne der einzelnen Ressourcen wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Aktivieren der Spalte "Domäne"" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="a3b8c-175">Aktivieren der Spalte "Domäne"</span><span class="sxs-lookup"><span data-stu-id="a3b8c-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="a3b8c-176">Um die vollständige URL einer Ressource zu überprüfen, zeigen Sie auf die Zelle in der **Spalte Name.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-176">To review the full URL of a resource, hover on the cell in the **Name** column.</span></span>  
    
## <a name="simulate-a-slower-network-connection"></a><span data-ttu-id="a3b8c-177">Simulieren einer langsameren Netzwerkverbindung</span><span class="sxs-lookup"><span data-stu-id="a3b8c-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="a3b8c-178">Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Standorten verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte Ihrer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="a3b8c-179">Wenn Sie die Seite drosseln, erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät benötigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="a3b8c-180">Wählen Sie **das Dropdownmenü Einschränkung** aus, das standardmäßig **auf Online** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Aktivieren der Einschränkung" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="a3b8c-182">Aktivieren der Einschränkung</span><span class="sxs-lookup"><span data-stu-id="a3b8c-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-183">Wählen **Sie Langsam 3G**aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Wählen Sie Langsame 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="a3b8c-185">Wählen Sie Langsame 3G</span><span class="sxs-lookup"><span data-stu-id="a3b8c-185">Choose Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-186">Lang drücken **Sie Reload** \( Reload ![ ][ImageRefreshIcon] \) und wählen Sie dann Leeren Cache und **Hard Reload aus.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Leerer Cache und Hard Reload" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="a3b8c-188">Leerer Cache und Hard Reload</span><span class="sxs-lookup"><span data-stu-id="a3b8c-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="a3b8c-189">Bei wiederholten Besuchen werden im Browser in der Regel einige Dateien aus dem [Cache verwendet,][MDNHTTPCache]wodurch die Seitenlast beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="a3b8c-190">**Leerer Cache und hard reload** erzwingt, dass der Browser für alle Ressourcen in das Netzwerk wechseln muss.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="a3b8c-191">Verwenden Sie diese, um zu zeigen, wie ein Besucher beim ersten Mal eine Seite laden kann.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-191">Use it to display how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a3b8c-192">Der **Workflow Leerer Cache und Hard Reload** ist nur verfügbar, wenn DevTools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <a name="capture-screenshots"></a><span data-ttu-id="a3b8c-193">Screenshots erfassen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-193">Capture screenshots</span></span>  

<span data-ttu-id="a3b8c-194">Screenshots zeigen, wie eine Webseite im Laufe der Zeit aussieht, während sie geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-194">Screenshots display how a webpage looks over time while it loads.</span></span>  

1.  <span data-ttu-id="a3b8c-195">Wählen Sie \( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und aktivieren Sie das Kontrollkästchen Screenshots **erfassen.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-195">Choose \(![Network settings][ImageSettingsIcon]\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="a3b8c-196">Aktualisieren Sie die Seite erneut mithilfe des **Workflows Leerer Cache und Hard Reload.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="a3b8c-197">Navigieren Sie [zu Simulieren einer langsameren Verbindung,](#simulate-a-slower-network-connection) wenn Sie eine Erinnerung dazu benötigen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="a3b8c-198">Der Bildschirmfotobereich enthält Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten betrachtet wurde.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-198">The Screenshots panel provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Screenshots der Seitenlast" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="a3b8c-200">Screenshots der Seitenlast</span><span class="sxs-lookup"><span data-stu-id="a3b8c-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-201">Wählen Sie die erste Miniaturansicht aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="a3b8c-202">DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Die Netzwerkaktivität, die während des ersten Screenshots passierte" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="a3b8c-204">Die Netzwerkaktivität, die während des ersten Screenshots passierte</span><span class="sxs-lookup"><span data-stu-id="a3b8c-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-205">Wählen Sie \( Netzwerkeinstellungen \) erneut aus, und deaktivieren Sie das Kontrollkästchen Screenshots ![ ][ImageSettingsIcon] erfassen, um den Bildschirmfotobereich zu schließen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a3b8c-205">Choose \(![Network settings][ImageSettingsIcon]\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="a3b8c-206">Aktualisieren Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-206">Refresh the page again.</span></span>  
    
## <a name="inspect-the-details-of-the-resource"></a><span data-ttu-id="a3b8c-207">Überprüfen der Details der Ressource</span><span class="sxs-lookup"><span data-stu-id="a3b8c-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="a3b8c-208">Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="a3b8c-209">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-209">Try it now:</span></span>  

1.  <span data-ttu-id="a3b8c-210">Wählen Sie `getstarted.html` aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="a3b8c-211">Der **Bereich Kopfzeilen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-211">The **Headers** panel is shown.</span></span>  <span data-ttu-id="a3b8c-212">Verwenden Sie diesen Bereich, um HTTP-Header zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-212">Use this panel to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="a3b8c-214">Der **Kopfzeilenbereich**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-214">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-215">Wählen Sie den **Bereich Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-215">Choose the **Preview** panel.</span></span>  <span data-ttu-id="a3b8c-216">Es wird ein einfaches Rendern des HTML angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-216">A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Der Vorschaubereich" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="a3b8c-218">Der **Vorschaubereich**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-218">The **Preview** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="a3b8c-219">Der Bereich ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-219">The panel is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="a3b8c-220">Möglicherweise ist es einfacher, den gerenderten HTML-Code als den HTML-Quellcode zu lesen, oder wenn Sie Bilder überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-220">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="a3b8c-221">Wählen Sie den **Antwortbereich** aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-221">Choose the **Response** panel.</span></span>  <span data-ttu-id="a3b8c-222">Der HTML-Quellcode wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-222">The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Der Antwortbereich" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="a3b8c-224">Der **Antwortbereich**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-224">The **Response** panel</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="a3b8c-225">Wenn eine Datei vermint wird, wählen Sie die Schaltfläche **Format** \( Format \) am unteren Rand des Antwortbereichs aus, um den Inhalt der Datei zur Lesbarkeit neu zu ![ ][ImageFormatIcon] \*\*\*\* formatieren.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-225">When a file is minified, choose the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** panel to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="a3b8c-226">Wählen Sie den **Zeitsteuerungsbereich** aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-226">Choose the **Timing** panel.</span></span>  <span data-ttu-id="a3b8c-227">Eine Aufschlüsselung der Netzwerkaktivität für die Ressource wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-227">A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Der Zeitsteuerungsbereich" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="a3b8c-229">Der **Zeitsteuerungsbereich**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-229">The **Timing** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-230">Wählen **Sie Schließen** \( Schließen ![ ][ImageCloseIcon] \) aus, um das Netzwerkprotokoll erneut anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-230">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Die Schaltfläche Schließen" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="a3b8c-232">Die **Schaltfläche** Schließen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-232">The **Close** button</span></span>  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a><span data-ttu-id="a3b8c-233">Durchsuchen von Netzwerkkopfzeilen und -antworten</span><span class="sxs-lookup"><span data-stu-id="a3b8c-233">Search network headers and responses</span></span>  

<span data-ttu-id="a3b8c-234">Verwenden Sie **den Suchbereich,** wenn Sie die HTTP-Header und -Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-234">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="a3b8c-235">Angenommen, Sie möchten überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien verwenden.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-235">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="a3b8c-236">Wählen **Sie Suchen** \( Suche ![ ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a3b8c-236">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="a3b8c-237">Der Suchbereich wird links vom Netzwerkprotokoll geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-237">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Der Suchbereich" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="a3b8c-239">Der **Suchbereich**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-239">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-240">Geben `Cache-Control` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-240">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="a3b8c-241">Der Suchbereich listet alle Instanzen `Cache-Control` auf, die in Ressourcenkopfzeilen oder Inhalten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-241">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Suchergebnisse für Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="a3b8c-243">Suchergebnisse‎‏ für: </span><span class="sxs-lookup"><span data-stu-id="a3b8c-243">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-244">Wählen Sie ein Ergebnis aus, um die Ressource, in der das Ergebnis gefunden wurde, anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-244">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="a3b8c-245">Wenn Sie sich die Details der Ressource anschauen, wählen Sie ein Ergebnis aus, um direkt zu ihr zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-245">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="a3b8c-246">Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird der **Bereich Kopfzeilen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-246">For example, if the query was found in a header, the **Headers** panel opens.</span></span>   <span data-ttu-id="a3b8c-247">Wenn die Abfrage im Inhalt gefunden wurde, wird der **Antwortbereich** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-247">If the query was found in content, the **Response** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Ein im Kopfzeilenbereich hervorgehobenes Suchergebnis" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="a3b8c-249">Ein im Kopfzeilenbereich **hervorgehobenes Suchergebnis**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-249">A search result highlighted in the **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-250">Schließen Sie den Suchbereich und **den Kopfzeilenbereich.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-250">Close the Search pane and the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Die Schaltflächen Schließen" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="a3b8c-252">Die **Schaltflächen** Schließen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-252">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <a name="filter-resources"></a><span data-ttu-id="a3b8c-253">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-253">Filter resources</span></span>  

<span data-ttu-id="a3b8c-254">DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für den jeweiligen Vorgang nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-254">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Die Symbolleiste Filter" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="a3b8c-256">Die **Symbolleiste Filter**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-256">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="a3b8c-257">Die **Symbolleiste** Filter sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-257">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="a3b8c-258">Wenn nicht,:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-258">If not:</span></span>  

1.  <span data-ttu-id="a3b8c-259">Wählen **Sie Filter** \( Filter ![ ][ImageFilterIcon] \) aus, um es zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-259">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <a name="filter-by-string-regular-expression-or-property"></a><span data-ttu-id="a3b8c-260">Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a3b8c-260">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="a3b8c-261">Das **Textfeld Filter** unterstützt viele verschiedene Filtertypen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-261">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="a3b8c-262">Geben `png` Sie in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-262">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="a3b8c-263">Es werden nur die Dateien angezeigt, die `png` den Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-263">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="a3b8c-264">In diesem Fall sind die einzigen Dateien, die mit dem Filter übereinstimmen, die PNG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-264">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Ein Zeichenfolgenfilter" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="a3b8c-266">Ein Zeichenfolgenfilter</span><span class="sxs-lookup"><span data-stu-id="a3b8c-266">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-267">Geben Sie `/.*\.[cj]s+$/` ein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-267">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="a3b8c-268">DevTools filtert jede Ressource mit einem Dateinamen heraus, der nicht mit einem oder mehreren Zeichen `j` `c` `s` endet.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-268">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filter für reguläre Ausdrücke" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="a3b8c-270">Filter für reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="a3b8c-270">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-271">Geben Sie `-main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-271">Type `-main.css`.</span></span>  <span data-ttu-id="a3b8c-272">DevTools filtert heraus `main.css` .</span><span class="sxs-lookup"><span data-stu-id="a3b8c-272">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="a3b8c-273">Wenn eine Datei dem Muster entspricht, wird auch der Titt herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-273">If any file matches the pattern, tit is also filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Ein negativer Filter" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="a3b8c-275">Ein negativer Filter</span><span class="sxs-lookup"><span data-stu-id="a3b8c-275">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-276">Geben `domain:cdn.glitch.com` Sie in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-276">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="a3b8c-277">DevTools filtert jede Ressource mit einer URL heraus, die nicht mit dieser Domäne übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-277">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Ein Eigenschaftenfilter" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="a3b8c-279">Ein Eigenschaftenfilter</span><span class="sxs-lookup"><span data-stu-id="a3b8c-279">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="a3b8c-280">Navigieren Sie zur vollständigen Liste der filterbaren Eigenschaften zu [Filter requests by properties][DevtoolsReferenceProperty].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-280">For the full list of filterable properties, navigate to [Filter requests by properties][DevtoolsReferenceProperty].</span></span>  
    
1.  <span data-ttu-id="a3b8c-281">Löschen Sie **das Textfeld Filter** eines beliebigen Texts.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-281">Clear the **Filter** text box of any text.</span></span>  
    
### <a name="filter-by-resource-type"></a><span data-ttu-id="a3b8c-282">Filtern nach Ressourcentyp</span><span class="sxs-lookup"><span data-stu-id="a3b8c-282">Filter by resource type</span></span>  

<span data-ttu-id="a3b8c-283">So konzentrieren Sie sich auf einen bestimmten Dateityp, z. B. Stylesheets:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-283">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="a3b8c-284">Wählen Sie **CSS**aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-284">Choose **CSS**.</span></span>  <span data-ttu-id="a3b8c-285">Alle anderen Dateitypen werden herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-285">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Nur CSS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="a3b8c-287">Nur CSS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-287">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-288">Um auch Skripts anzeigen zu können, wählen Sie `Control` \(Windows, Linux\) oder \(macOS\) aus, und wählen `Command` Sie **dann JS aus.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-288">To also display scripts, select and hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Nur CSS- und JS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="a3b8c-290">Nur CSS- und JS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-290">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-291">Wenn Sie die Filter entfernen und alle Ressourcen erneut anzeigen möchten, wählen Sie **Alle aus.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-291">To remove the filters and display all resources again, choose **All**.</span></span>  
    
<span data-ttu-id="a3b8c-292">Navigieren Sie für andere Filterworkflows zu [Filteranforderungen][DevtoolsNetworkReferenceFilter].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-292">For other filtering workflows, navigate to [Filter requests][DevtoolsNetworkReferenceFilter].</span></span>  

## <a name="block-requests"></a><span data-ttu-id="a3b8c-293">Blockieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-293">Block requests</span></span>  

<span data-ttu-id="a3b8c-294">Wie sieht eine Seite aus und verhält sich, wenn einige der Seitenressourcen nicht verfügbar sind?</span><span class="sxs-lookup"><span data-stu-id="a3b8c-294">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="a3b8c-295">Ist der Fehler vollständig, oder ist er noch ein wenig funktionsfähig?</span><span class="sxs-lookup"><span data-stu-id="a3b8c-295">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="a3b8c-296">Blockieren von Anforderungen zum Herausfinden:</span><span class="sxs-lookup"><span data-stu-id="a3b8c-296">Block requests to find out:</span></span>  

1.  <span data-ttu-id="a3b8c-297">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-297">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="a3b8c-299">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="a3b8c-299">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-300">Geben `block` Sie ein, wählen **Sie Anforderungsblockierung anzeigen**aus, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-300">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Anzeigen der Anforderungsblockierung" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="a3b8c-302">Anzeigen der Anforderungsblockierung</span><span class="sxs-lookup"><span data-stu-id="a3b8c-302">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-303">Wählen **Sie Muster hinzufügen** \( Muster hinzufügen ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a3b8c-303">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="a3b8c-304">Geben Sie `main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-304">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blockieren von main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="a3b8c-306">Blockieren</span><span class="sxs-lookup"><span data-stu-id="a3b8c-306">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-307">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-307">Choose **Add**.</span></span>  
1.  <span data-ttu-id="a3b8c-308">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-308">Refresh the page.</span></span>  <span data-ttu-id="a3b8c-309">Wie erwartet ist das Format der Seite etwas verfedert, da das Hauptformatblatt blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-309">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a3b8c-310">Die `main.css` Zeile im Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-310">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="a3b8c-311">Der rote Text bedeutet, dass die Ressource blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-311">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css wurde blockiert" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="a3b8c-313">wurde blockiert</span><span class="sxs-lookup"><span data-stu-id="a3b8c-313">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a3b8c-314">Deaktivieren Sie das **Kontrollkästchen Anforderungsblockierung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-314">Deselect the **Enable request blocking** checkbox.</span></span>  

## <a name="conclusion"></a><span data-ttu-id="a3b8c-315">Fazit</span><span class="sxs-lookup"><span data-stu-id="a3b8c-315">Conclusion</span></span>  

<span data-ttu-id="a3b8c-316">Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-316">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="a3b8c-317">Sie wissen nun, wie Sie das **Netzwerktool** in den Microsoft Edge DevTools verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-317">You now know how to use the **Network** tool in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="a3b8c-318">Navigieren Sie zum [Netzwerkverweis,][DevtoolsNetworkReference] um weitere DevTools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-318">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a3b8c-319">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a3b8c-319">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Platzierung von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Netzwerkanalysereferenz | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filteranforderungen – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ausblenden des Bereichs Übersicht – Netzwerkanalysereferenz | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filteranforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspect Network Activity Demo | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Zwischenspeicherung | MDN"  

> [!NOTE]
> <span data-ttu-id="a3b8c-329">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-329">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a3b8c-330">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a3b8c-330">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a3b8c-332">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a3b8c-332">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
