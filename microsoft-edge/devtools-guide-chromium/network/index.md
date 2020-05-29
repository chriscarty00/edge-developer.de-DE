---
title: Überprüfen der Netzwerkaktivität in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611812"
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





# <span data-ttu-id="c6bd7-103">Überprüfen der Netzwerkaktivität in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="c6bd7-103">Inspect Network Activity In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c6bd7-104">Hierbei handelt es sich um ein praktisches Lernprogramm einiger der am häufigsten verwendeten devtools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="c6bd7-105">Weitere Informationen finden Sie unter [Netzwerk Referenz][DevtoolsNetworkReference] , wenn Sie stattdessen Features durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="c6bd7-106">Verwendung des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="c6bd7-106">When to use the Network panel</span></span>   

<span data-ttu-id="c6bd7-107">Verwenden Sie im Allgemeinen das Netzwerk Panel, wenn Sie sicherstellen möchten, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="c6bd7-108">Die häufigsten Anwendungsfälle für das Netzwerk Panel sind:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="c6bd7-109">Sicherstellen, dass Ressourcen tatsächlich hochgeladen oder überhaupt heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="c6bd7-110">Überprüfen der Eigenschaften einer einzelnen Ressource, wie HTTP-Header, Inhalt, Größe usw.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  

<span data-ttu-id="c6bd7-111">Wenn Sie nach Möglichkeiten suchen, die Seiten Ladeleistung zu verbessern, beginnen Sie **nicht** mit dem Netzwerk Panel.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="c6bd7-112">Es gibt viele Arten von Problemen mit der Auslastungs Leistung, die nicht mit der Netzwerkaktivität zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="c6bd7-113">Beginnen Sie mit dem Überwachungs Panel, da Sie gezielte Vorschläge zum Verbessern Ihrer Seite erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="c6bd7-114">Weitere Informationen finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c6bd7-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="c6bd7-115">Öffnen des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="c6bd7-115">Open the Network panel</span></span>   

<span data-ttu-id="c6bd7-116">Um dieses Lernprogramm optimal zu nutzen, öffnen Sie die Demo und testen Sie die Features auf der Demo-Seite.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="c6bd7-117">Öffnen [Sie die Demo für erste Schritte][GlitchNetworkGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-117">Open the [Get Started Demo][GlitchNetworkGetStarted] .</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-118">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="c6bd7-118">Figure 1</span></span>  
    > <span data-ttu-id="c6bd7-119">Die Demo</span><span class="sxs-lookup"><span data-stu-id="c6bd7-119">The demo</span></span>  
    > ![Die Demo][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  <span data-ttu-id="c6bd7-121">[Öffnen Sie devtools][DevToolsOpen] , indem Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="c6bd7-122">Das **Konsolen** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-122">The **Console** panel opens.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-123">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="c6bd7-123">Figure 2</span></span>  
    > <span data-ttu-id="c6bd7-124">Der Konsole</span><span class="sxs-lookup"><span data-stu-id="c6bd7-124">The Console</span></span>  
    > <span data-ttu-id="c6bd7-125">! [Konsole] [ImagesTutorialConsole]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-125">![The Console][ImagesTutorialConsole]</span></span>  
    
    <span data-ttu-id="c6bd7-126">Sie können [devtools am unteren Rand des Fensters andocken][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="c6bd7-126">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-127">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="c6bd7-127">Figure 3</span></span>  
    > <span data-ttu-id="c6bd7-128">DevTools an den unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="c6bd7-128">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="c6bd7-129">! [Devtools angedockt am unteren Rand des Fensters] [ImagesTutorialDocked]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-129">![DevTools docked to the bottom of the window][ImagesTutorialDocked]</span></span>  

1.  <span data-ttu-id="c6bd7-130">Wählen Sie die Registerkarte **Netzwerk** aus.  Das Netzwerkfenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-130">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-131">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="c6bd7-131">Figure 4</span></span>  
    > <span data-ttu-id="c6bd7-132">DevTools an den unteren Rand des Fensters angedockt</span><span class="sxs-lookup"><span data-stu-id="c6bd7-132">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="c6bd7-133">! [Devtools angedockt am unteren Rand des Fensters] [ImagesTutorialNetwork]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-133">![DevTools docked to the bottom of the window][ImagesTutorialNetwork]</span></span>  

<span data-ttu-id="c6bd7-134">Im Moment ist das Netzwerk Panel leer.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-134">Right now the Network panel is empty.</span></span>  <span data-ttu-id="c6bd7-135">DevTools protokolliert nur Netzwerkaktivitäten, nachdem Sie Sie geöffnet haben und seit dem Öffnen von devtools keine Netzwerkaktivität stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-135">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="c6bd7-136">Protokollieren von Netzwerkaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c6bd7-136">Log network activity</span></span>   

<span data-ttu-id="c6bd7-137">So zeigen Sie die Netzwerkaktivität an, die eine Seite verursacht:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-137">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="c6bd7-138">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-138">Reload the page.</span></span>  <span data-ttu-id="c6bd7-139">Das Netzwerk Panel protokolliert alle Netzwerkaktivitäten im **Netzwerkprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-139">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-140">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="c6bd7-140">Figure 5</span></span>  
    > <span data-ttu-id="c6bd7-141">Das Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="c6bd7-141">The Network Log</span></span>  
    > <span data-ttu-id="c6bd7-142">! [Netzwerkprotokoll] [ImagesTutorialLog]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-142">![The Network Log][ImagesTutorialLog]</span></span>  
    
    <span data-ttu-id="c6bd7-143">Jede Zeile des **Netzwerkprotokolls** stellt eine Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-143">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="c6bd7-144">Standardmäßig werden die Ressourcen in chronologischer Reihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-144">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="c6bd7-145">Die oberste Ressource ist in der Regel das wichtigste HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-145">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="c6bd7-146">Die untere Ressource ist, was zuletzt angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-146">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="c6bd7-147">Jede Spalte stellt Informationen zu einer Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-147">Each column represents information about a resource.</span></span>  <span data-ttu-id="c6bd7-148">[**Abbildung 6**](#figure-6) zeigt die Standardspalten:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-148">[**Figure 6**](#figure-6) shows the default columns:</span></span>  

    *   <span data-ttu-id="c6bd7-149">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-149">**Status**.</span></span>  <span data-ttu-id="c6bd7-150">Der HTTP-Statuscode für die Antwort.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-150">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="c6bd7-151">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-151">**Type**.</span></span>  <span data-ttu-id="c6bd7-152">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-152">The resource type.</span></span>  
    *   <span data-ttu-id="c6bd7-153">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-153">**Initiator**.</span></span>  <span data-ttu-id="c6bd7-154">Die Ursache der Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-154">The cause of the resource request.</span></span>  <span data-ttu-id="c6bd7-155">Wenn Sie einen Link in der Spalte Initiator auswählen, gelangen Sie zu dem Quellcode, der die Anforderung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-155">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="c6bd7-156">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-156">**Time**.</span></span>  <span data-ttu-id="c6bd7-157">Die Dauer der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-157">The duration of the request.</span></span>  
    *   <span data-ttu-id="c6bd7-158">**Wasserfall**.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-158">**Waterfall**.</span></span>  <span data-ttu-id="c6bd7-159">Eine grafische Darstellung der verschiedenen Phasen der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-159">A graphical representation of the different stages of the request.</span></span>  
        <span data-ttu-id="c6bd7-160">Zeigen Sie mit der Maus auf einen Wasserfall, um eine Unterbrechung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-160">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c6bd7-161">Das Diagramm oberhalb des Netzwerkprotokolls wird als Übersicht bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-161">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="c6bd7-162">Sie werden das Übersichtsdiagramm in diesem Lernprogramm nicht verwenden, sodass Sie es möglicherweise ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-162">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="c6bd7-163">Weitere Informationen finden Sie unter [Ausblenden des][DevtoolsReferenceHideOverview]Übersichtsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-163">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
        
1.  <span data-ttu-id="c6bd7-164">Nachdem Sie devtools geöffnet haben, werden die Netzwerkaktivitäten im Netzwerkprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-164">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="c6bd7-165">Um dies zu veranschaulichen, schauen Sie sich zuerst den unteren Rand des **Netzwerkprotokolls** an und machen Sie sich mit der letzten Aktivität auf den Kopf.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-165">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="c6bd7-166">Wählen Sie nun in der Demo die Schaltfläche **Daten abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-166">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="c6bd7-167">Sehen Sie sich die untere Seite des **Netzwerkprotokolls** erneut an.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-167">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="c6bd7-168">Es sollte eine neue Ressource mit dem Namen angezeigt werden `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-168">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="c6bd7-169">Durch Auswählen der Schaltfläche " **Daten abrufen** " wurde die Datei von der Seite angefordert.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-169">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-170">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="c6bd7-170">Figure 6</span></span>  
    > <span data-ttu-id="c6bd7-171">Eine neue Ressource im Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="c6bd7-171">A new resource in the Network Log</span></span>  
    > <span data-ttu-id="c6bd7-172">! [Eine neue Ressource im Netzwerkprotokoll] [ImagesTutorialRuntime]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-172">![A new resource in the Network Log][ImagesTutorialRuntime]</span></span>  

## <span data-ttu-id="c6bd7-173">Weitere Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-173">Show more information</span></span>   

<span data-ttu-id="c6bd7-174">Die Spalten des Netzwerkprotokolls können konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-174">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="c6bd7-175">Sie können Spalten, die Sie nicht verwenden, ausblenden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-175">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="c6bd7-176">Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind, die Sie möglicherweise als nützlich empfinden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-176">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="c6bd7-177">Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Netzwerkprotokoll Tabelle, und wählen Sie **Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-177">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="c6bd7-178">Die Domäne jeder Ressource wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-178">The domain of each resource is now shown.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-179">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="c6bd7-179">Figure 7</span></span>  
    > <span data-ttu-id="c6bd7-180">Aktivieren der Spalte "Domäne"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-180">Enabling the Domain column</span></span>  
    > <span data-ttu-id="c6bd7-181">! [Aktivieren der Domänen Spalte] [ImagesTutorialDomain]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-181">![Enabling the Domain column][ImagesTutorialDomain]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="c6bd7-182">Zeigen Sie die vollständige URL einer Ressource an, indem Sie in der Spalte **Name** auf die Zelle zeigen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-182">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  

## <span data-ttu-id="c6bd7-183">Simulieren einer langsameren Netzwerkverbindung</span><span class="sxs-lookup"><span data-stu-id="c6bd7-183">Simulate a slower network connection</span></span>   

<span data-ttu-id="c6bd7-184">Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Websites verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte ihrer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-184">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="c6bd7-185">Durch Drosselung der Seite erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät dauert.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-185">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="c6bd7-186">Wählen Sie die Dropdownliste **Drosselung** aus, die standardmäßig auf **Online** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-186">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-187">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="c6bd7-187">Figure 8</span></span>  
    > <span data-ttu-id="c6bd7-188">Aktivieren der Drosselung</span><span class="sxs-lookup"><span data-stu-id="c6bd7-188">Enabling throttling</span></span>  
    > <span data-ttu-id="c6bd7-189">! [Aktivieren der Drosselung] [ImagesTutorialThrottling]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-189">![Enabling throttling][ImagesTutorialThrottling]</span></span>  
    
1.  <span data-ttu-id="c6bd7-190">Wählen Sie **Slow 3G**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-190">Select **Slow 3G**.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-191">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="c6bd7-191">Figure 9</span></span>  
    > <span data-ttu-id="c6bd7-192">Auswählen von Slow 3G</span><span class="sxs-lookup"><span data-stu-id="c6bd7-192">Selecting Slow 3G</span></span>  
    > <span data-ttu-id="c6bd7-193">! [Auswahl von Slow 3G] [ImagesTutorialSlow3G]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-193">![Selecting Slow 3G][ImagesTutorialSlow3G]</span></span>  
    
1.  <span data-ttu-id="c6bd7-194">Lange drücken Sie **Reload** Reload ![ ][ImageRefreshIcon] , und wählen Sie dann **Cache leeren und Hard Reload**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-194">Long-press **Reload** ![Reload][ImageRefreshIcon] and then select **Empty Cache And Hard Reload**.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-195">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="c6bd7-195">Figure 10</span></span>  
    > <span data-ttu-id="c6bd7-196">Leerer Cache und schweres erneutes Laden</span><span class="sxs-lookup"><span data-stu-id="c6bd7-196">Empty Cache And Hard Reload</span></span>  
    > <span data-ttu-id="c6bd7-197">! [Cache leeren und Hard Reload] [ImagesTutorialHardReload]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-197">![Empty Cache And Hard Reload][ImagesTutorialHardReload]</span></span>  
    
    <span data-ttu-id="c6bd7-198">Bei wiederholten Besuchen dient der Browser in der Regel einigen Dateien aus dem [Cache][MDNHTTPCache] , wodurch die Seitenauslastung beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-198">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache] , which speeds up the page load.</span></span>  <span data-ttu-id="c6bd7-199">**Leerer Cache und harter Reload** erzwingt den Browser, das Netzwerk für alle Ressourcen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-199">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="c6bd7-200">Dies ist hilfreich, wenn Sie sehen möchten, wie ein Erstbesucher eine Seitenbelastung erlebt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-200">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c6bd7-201">Der Workflow " **leerer Cache" und "harter Reload** " steht nur zur Verfügung, wenn devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-201">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  

## <span data-ttu-id="c6bd7-202">Screenshots aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-202">Capture screenshots</span></span>   

<span data-ttu-id="c6bd7-203">Mit Screenshots können Sie sehen, wie eine Seite im Laufe der Zeit aussah, während Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-203">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="c6bd7-204">Wählen Sie ![ Netzwerkeinstellungen aus ][ImageSettingsIcon] , und aktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-204">Select ![Network settings][ImageSettingsIcon] and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="c6bd7-205">Laden Sie die Seite erneut über den **leeren Cache und** den Arbeitsablauf für das erneute Laden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-205">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="c6bd7-206">Weitere Informationen hierzu finden Sie unter [Simulieren einer langsameren Verbindung](#simulate-a-slower-network-connection) .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-206">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="c6bd7-207">Der Bereich "Screenshots" bietet Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten aussah.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-207">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-208">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="c6bd7-208">Figure 11</span></span>  
    > <span data-ttu-id="c6bd7-209">Screenshots des Ladens der Seite</span><span class="sxs-lookup"><span data-stu-id="c6bd7-209">Screenshots of the page load</span></span>  
    > <span data-ttu-id="c6bd7-210">! [Screenshots der Seite laden] [ImagesTutorialAllScreenshots]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-210">![Screenshots of the page load][ImagesTutorialAllScreenshots]</span></span>  

1.  <span data-ttu-id="c6bd7-211">Wählen Sie die erste Miniaturansicht aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-211">Select the first thumbnail.</span></span>  <span data-ttu-id="c6bd7-212">DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-212">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-213">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="c6bd7-213">Figure 12</span></span>  
    > <span data-ttu-id="c6bd7-214">Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat</span><span class="sxs-lookup"><span data-stu-id="c6bd7-214">The network activity that was happening during the first screenshot</span></span>  
    > <span data-ttu-id="c6bd7-215">! [Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat] [ImagesTutorialFirstScreenshot]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-215">![The network activity that was happening during the first screenshot][ImagesTutorialFirstScreenshot]</span></span>  

1.  <span data-ttu-id="c6bd7-216">Wählen Sie ![ erneut Netzwerkeinstellungen aus, ][ImageSettingsIcon] und deaktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** , um den Bereich Screenshots zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-216">Select ![Network settings][ImageSettingsIcon] again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="c6bd7-217">Laden Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-217">Reload the page again.</span></span>  

## <span data-ttu-id="c6bd7-218">Überprüfen der Details der Ressource</span><span class="sxs-lookup"><span data-stu-id="c6bd7-218">Inspect the details of the resource</span></span>   

<span data-ttu-id="c6bd7-219">Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-219">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="c6bd7-220">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-220">Try it now:</span></span>  

1.  <span data-ttu-id="c6bd7-221">Wählen Sie aus `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-221">Select `getstarted.html`.</span></span>  <span data-ttu-id="c6bd7-222">Die Registerkarte über **Schriften** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-222">The **Headers** tab is shown.</span></span>  <span data-ttu-id="c6bd7-223">Verwenden Sie diese Registerkarte, um HTTP-Header zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-223">Use this tab to inspect HTTP headers.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-224">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="c6bd7-224">Figure 13</span></span>  
    > <span data-ttu-id="c6bd7-225">Die Registerkarte "Überschriften"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-225">The Headers tab</span></span>  
    > <span data-ttu-id="c6bd7-226">! [Die Registerkarte ' Überschriften '] [ImagesTutorialHeaders]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-226">![The Headers tab][ImagesTutorialHeaders]</span></span>  
    
1.  <span data-ttu-id="c6bd7-227">Wählen Sie die Registerkarte **Vorschau** aus.  Eine grundlegende Darstellung des HTML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-227">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-228">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="c6bd7-228">Figure 14</span></span>  
    > <span data-ttu-id="c6bd7-229">Registerkarte "Vorschau"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-229">The Preview tab</span></span>  
    > <span data-ttu-id="c6bd7-230">! [Vorschau-Reiter] [ImagesTutorialPreview]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-230">![The Preview tab][ImagesTutorialPreview]</span></span>  

     <span data-ttu-id="c6bd7-231">Diese Registerkarte ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-231">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="c6bd7-232">Möglicherweise ist es einfacher, den gerenderten HTML-Code zu lesen als den HTML-Quellcode, oder wenn Sie Bilder untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-232">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="c6bd7-233">Wählen Sie die Registerkarte **Antwort** aus.  Der HTML-Quellcode wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-233">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-234">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="c6bd7-234">Figure 15</span></span>  
    > <span data-ttu-id="c6bd7-235">Die Registerkarte "Antwort"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-235">The Response tab</span></span>  
    > <span data-ttu-id="c6bd7-236">! [Die Registerkarte ' Antwort '] [ImagesTutorialResponse]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-236">![The Response tab][ImagesTutorialResponse]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="c6bd7-237">Wenn eine Datei minimierte ist, wird durch **Format** auswählen der ![ ][ImageFormatIcon] Schaltfläche Format Format unten auf der Registerkarte **Antwort** der Inhalt der Datei zur Lesbarkeit neu formatiert.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-237">When a file is minified, selecting the **Format** ![Format][ImageFormatIcon] button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  

1.  <span data-ttu-id="c6bd7-238">Wählen Sie die Registerkarte **Anzeige** Dauer aus.  Eine Aufschlüsselung der Netzwerkaktivität für diese Ressource wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-238">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-239">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="c6bd7-239">Figure 16</span></span>  
    > <span data-ttu-id="c6bd7-240">Registerkarte "Anzeigedauer"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-240">The Timing tab</span></span>  
    > <span data-ttu-id="c6bd7-241">! [Die Registerkarte Anzeigedauer] [ImagesTutorialTiming]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-241">![The Timing tab][ImagesTutorialTiming]</span></span>  

1.  <span data-ttu-id="c6bd7-242">Wählen **Sie schließen aus** ![ ][ImageCloseIcon] , um das Netzwerkprotokoll erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-242">Select **Close** ![Close][ImageCloseIcon] to view the Network Log again.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-243">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="c6bd7-243">Figure 17</span></span>  
    > <span data-ttu-id="c6bd7-244">Schaltfläche "Schließen"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-244">The Close button</span></span>  
    > <span data-ttu-id="c6bd7-245">! [Die Schaltfläche ' Schließen '] [ImagesTutorialCloseTiming]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-245">![The Close button][ImagesTutorialCloseTiming]</span></span>  

## <span data-ttu-id="c6bd7-246">Durchsuchen von Netzwerk Kopfzeilen und-Antworten</span><span class="sxs-lookup"><span data-stu-id="c6bd7-246">Search network headers and responses</span></span>   

<span data-ttu-id="c6bd7-247">Verwenden Sie den **Such** Bereich, wenn Sie die HTTP-Header und Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-247">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="c6bd7-248">Angenommen, Sie möchten beispielsweise überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien**verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-248">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="c6bd7-249">Wählen **Sie Suche suchen** aus ![ ][ImageSearchIcon] .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-249">Select **Search** ![Search][ImageSearchIcon].</span></span>  <span data-ttu-id="c6bd7-250">Der Suchbereich wird links neben dem Netzwerkprotokoll geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-250">The Search pane opens to the left of the Network log.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-251">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="c6bd7-251">Figure 18</span></span>  
    > <span data-ttu-id="c6bd7-252">Der Suchbereich</span><span class="sxs-lookup"><span data-stu-id="c6bd7-252">The Search pane</span></span>  
    > <span data-ttu-id="c6bd7-253">! [Der Suchbereich] [ImagesTutorialSearch]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-253">![The Search pane][ImagesTutorialSearch]</span></span>  

1.  <span data-ttu-id="c6bd7-254">Geben `Cache-Control` Sie ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-254">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="c6bd7-255">Der Suchbereich listet alle Instanzen auf `Cache-Control` , die in Ressourcen Kopfzeilen oder-Inhalten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-255">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-256">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="c6bd7-256">Figure 19</span></span>  
    > <span data-ttu-id="c6bd7-257">Suchergebnisse‎‏ für: </span><span class="sxs-lookup"><span data-stu-id="c6bd7-257">Search results for</span></span> `Cache-Control`  
    > <span data-ttu-id="c6bd7-258">! [Suchergebnisse für Cache-Control] [ImagesTutorialResults]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-258">![Search results for Cache-Control][ImagesTutorialResults]</span></span>  

1.  <span data-ttu-id="c6bd7-259">Wählen Sie ein Ergebnis aus, um die Ressource anzuzeigen, in der das Ergebnis gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-259">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="c6bd7-260">Wenn Sie die Details der Ressource sehen möchten, wählen Sie ein Ergebnis aus, um direkt dorthin zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-260">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="c6bd7-261">Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird die Registerkarte Überschriften geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-261">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="c6bd7-262">Wenn die Abfrage im Inhalt gefunden wurde, wird die Registerkarte " **Antwort** " geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-262">If the query was found in content, the **Response** tab opens.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-263">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="c6bd7-263">Figure 20</span></span>  
    > <span data-ttu-id="c6bd7-264">Auf der Registerkarte "Überschriften" hervorgehobenes Suchergebnis</span><span class="sxs-lookup"><span data-stu-id="c6bd7-264">A search result highlighted in the Headers tab</span></span>  
    > <span data-ttu-id="c6bd7-265">! [Ein Suchergebnis ist auf der Registerkarte ' Überschriften ' hervorgehoben] [ImagesTutorialCache]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-265">![A search result highlighted in the Headers tab][ImagesTutorialCache]</span></span>  
    
1.  <span data-ttu-id="c6bd7-266">Schließen Sie den Suchbereich und die Registerkarte Überschriften.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-266">Close the Search pane and the Headers tab.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-267">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="c6bd7-267">Figure 21</span></span>  
    > <span data-ttu-id="c6bd7-268">Die Schaltflächen "Schließen"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-268">The Close buttons</span></span>  
    > <span data-ttu-id="c6bd7-269">! [Die Schaltflächen zum Schließen] [ImagesTutorialCloseButtons]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-269">![The Close buttons][ImagesTutorialCloseButtons]</span></span>  
    
## <span data-ttu-id="c6bd7-270">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-270">Filter resources</span></span>   

<span data-ttu-id="c6bd7-271">DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-271">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

> ##### <span data-ttu-id="c6bd7-272">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="c6bd7-272">Figure 22</span></span>  
> <span data-ttu-id="c6bd7-273">Die Symbolleiste "Filter"</span><span class="sxs-lookup"><span data-stu-id="c6bd7-273">The Filters toolbar</span></span>  
> <span data-ttu-id="c6bd7-274">! [Die Filtersymbolleiste] [ImagesTutorialFilters]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-274">![The Filters toolbar][ImagesTutorialFilters]</span></span>  

<span data-ttu-id="c6bd7-275">Die **Filter** Symbolleiste sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-275">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="c6bd7-276">Wenn nicht,:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-276">If not:</span></span>  

1.  <span data-ttu-id="c6bd7-277">Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um ihn anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-277">Select **Filter** ![Filter][ImageFilterIcon] to show it.</span></span>  

### <span data-ttu-id="c6bd7-278">Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c6bd7-278">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="c6bd7-279">Das Textfeld " **Filter** " unterstützt viele verschiedene Filterarten.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-279">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="c6bd7-280">Geben Sie `png` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-280">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="c6bd7-281">Nur die Dateien, die den Text enthalten, `png` werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-281">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="c6bd7-282">In diesem Fall sind die einzigen Dateien, die dem Filter entsprechen, die PNG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-282">In this case the only files that match the filter are the PNG images.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-283">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="c6bd7-283">Figure 23</span></span>  
    > <span data-ttu-id="c6bd7-284">Ein Zeichenfolgenfilter</span><span class="sxs-lookup"><span data-stu-id="c6bd7-284">A string filter</span></span>  
    > <span data-ttu-id="c6bd7-285">! [Ein Zeichenfolgenfilter] [ImagesTutorialPNG]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-285">![A string filter][ImagesTutorialPNG]</span></span>  

1.  <span data-ttu-id="c6bd7-286">Geben Sie `/.*\.[cj]s+$/` ein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-286">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="c6bd7-287">DevTools filtert jede Ressource mit einem Dateinamen, der nicht mit a `j` oder a, `c` gefolgt von 1 oder mehr Zeichen, endet `s` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-287">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-288">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="c6bd7-288">Figure 24</span></span>  
    > <span data-ttu-id="c6bd7-289">Ein Filter für reguläre Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="c6bd7-289">A regular expression filter</span></span>  
    > <span data-ttu-id="c6bd7-290">! [Ein Filter für reguläre Ausdrücke] [ImagesTutorialRegEx]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-290">![A regular expression filter][ImagesTutorialRegEx]</span></span>  
    
1.  <span data-ttu-id="c6bd7-291">Geben Sie `-main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-291">Type `-main.css`.</span></span>  <span data-ttu-id="c6bd7-292">DevTools filtert aus `main.css` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-292">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="c6bd7-293">Wenn eine andere Datei mit dem Muster übereinstimmt, würden Sie ebenfalls herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-293">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-294">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="c6bd7-294">Figure 25</span></span>  
    > <span data-ttu-id="c6bd7-295">Ein negativer Filter</span><span class="sxs-lookup"><span data-stu-id="c6bd7-295">A negative filter</span></span>  
    > <span data-ttu-id="c6bd7-296">! [Ein negativer Filter] [ImagesTutorialNegative]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-296">![A negative filter][ImagesTutorialNegative]</span></span>  
    
1.  <span data-ttu-id="c6bd7-297">Geben Sie `domain:cdn.glitch.com` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-297">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="c6bd7-298">DevTools filtert jede Ressource mit einer URL ab, die dieser Domäne nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-298">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-299">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="c6bd7-299">Figure 26</span></span>  
    > <span data-ttu-id="c6bd7-300">Ein Eigenschaften Filter</span><span class="sxs-lookup"><span data-stu-id="c6bd7-300">A property filter</span></span>  
    > <span data-ttu-id="c6bd7-301">! [Ein Eigenschaften Filter] [ImagesTutorialProperty]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-301">![A property filter][ImagesTutorialProperty]</span></span>  

    <span data-ttu-id="c6bd7-302">Die vollständige Liste der filterbaren Eigenschaften finden Sie unter [Filtern von Anforderungen nach Eigenschaften][DevtoolsReferenceProperty] .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-302">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
    
1.  <span data-ttu-id="c6bd7-303">Deaktivieren Sie das Textfeld " **Filter** " eines beliebigen Texts.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-303">Clear the **Filter** text box of any text.</span></span>  

### <span data-ttu-id="c6bd7-304">Nach Ressourcentyp Filtern</span><span class="sxs-lookup"><span data-stu-id="c6bd7-304">Filter by resource type</span></span>   

<span data-ttu-id="c6bd7-305">So konzentrieren Sie sich auf eine bestimmte Art von Datei, beispielsweise Stylesheets:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-305">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="c6bd7-306">Wählen Sie **CSS**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-306">Select **CSS**.</span></span>  <span data-ttu-id="c6bd7-307">Alle anderen Dateitypen werden herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-307">All other file types are filtered out.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-308">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="c6bd7-308">Figure 27</span></span>  
    > <span data-ttu-id="c6bd7-309">Nur CSS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-309">Showing CSS files only</span></span>  
    > <span data-ttu-id="c6bd7-310">! [Nur CSS-Dateien anzeigen] [ImagesTutorialCSS]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-310">![Showing CSS files only][ImagesTutorialCSS]</span></span>  
    
1.  <span data-ttu-id="c6bd7-311">Wenn Sie auch Skripts anzeigen möchten, halten Sie `Control` \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann **js**aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-311">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-312">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="c6bd7-312">Figure 28</span></span>  
    > <span data-ttu-id="c6bd7-313">Nur CSS-und JS-Dateien anzeigen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-313">Showing CSS and JS files only</span></span>  
    > <span data-ttu-id="c6bd7-314">! [Nur CSS-und JS-Dateien anzeigen] [ImagesTutorialCSSJS]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-314">![Showing CSS and JS files only][ImagesTutorialCSSJS]</span></span>  
    
1.  <span data-ttu-id="c6bd7-315">Wählen Sie **alle** aus, um die Filter zu entfernen und alle Ressourcen erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-315">Select **All** to remove the filters and see all resources again.</span></span>  

<span data-ttu-id="c6bd7-316">Weitere Informationen finden Sie unter [Filteranforderungen][DevtoolsNetworkReferenceFilter] für andere Filter Workflows.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-316">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="c6bd7-317">Anfragen blockieren</span><span class="sxs-lookup"><span data-stu-id="c6bd7-317">Block requests</span></span>   

<span data-ttu-id="c6bd7-318">Wie wird eine Seite aussehen und sich Verhalten, wenn einige Seitenressourcen nicht verfügbar sind?</span><span class="sxs-lookup"><span data-stu-id="c6bd7-318">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="c6bd7-319">Funktioniert es nicht vollständig, oder ist es immer noch etwas funktionell?</span><span class="sxs-lookup"><span data-stu-id="c6bd7-319">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="c6bd7-320">Anfragen blockieren, um Folgendes zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="c6bd7-320">Block requests to find out:</span></span>  

1.  <span data-ttu-id="c6bd7-321">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-321">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-322">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="c6bd7-322">Figure 29</span></span>  
    > <span data-ttu-id="c6bd7-323">Das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="c6bd7-323">The Command Menu</span></span>  
    > <span data-ttu-id="c6bd7-324">! [Befehlsmenü] [ImagesTutorialCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-324">![The Command Menu][ImagesTutorialCommandMenu]</span></span>  
    
1.  <span data-ttu-id="c6bd7-325">Geben `block` Sie die Option **Blockierungs Anforderung anzeigen**ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-325">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-326">Abbildung 30</span><span class="sxs-lookup"><span data-stu-id="c6bd7-326">Figure 30</span></span>  
    > <span data-ttu-id="c6bd7-327">Anforderungs Blockierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="c6bd7-327">Show Request Blocking</span></span>  
    > <span data-ttu-id="c6bd7-328">! [Anzeige der Anforderungs Blockierung] [ImagesTutorialBlock]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-328">![Show Request Blocking][ImagesTutorialBlock]</span></span>  

1.  <span data-ttu-id="c6bd7-329">Wählen Sie **Muster** ![ hinzufügen aus ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-329">Select **Add Pattern** ![Add Pattern][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="c6bd7-330">Geben Sie `main.css` ein.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-330">Type `main.css`.</span></span>  
    
    > ##### <span data-ttu-id="c6bd7-331">Abbildung 31</span><span class="sxs-lookup"><span data-stu-id="c6bd7-331">Figure 31</span></span>  
    > <span data-ttu-id="c6bd7-332">Blockieren</span><span class="sxs-lookup"><span data-stu-id="c6bd7-332">Blocking</span></span> `main.css`  
    > <span data-ttu-id="c6bd7-333">! [Blockieren von Main. CSS] [ImagesTutorialAddBlock]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-333">![Blocking main.css][ImagesTutorialAddBlock]</span></span>  
    
1.  <span data-ttu-id="c6bd7-334">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-334">Select **Add**.</span></span>  
1.  <span data-ttu-id="c6bd7-335">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-335">Reload the page.</span></span>  <span data-ttu-id="c6bd7-336">Wie erwartet, wird das Design der Seite etwas durcheinander gebracht, da das Haupt-Stylesheet blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-336">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c6bd7-337">Die `main.css` Zeile im Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-337">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="c6bd7-338">Der rote Text bedeutet, dass die Ressource blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-338">The red text means that the resource was blocked.</span></span>
    
    > ##### <span data-ttu-id="c6bd7-339">Abbildung 32</span><span class="sxs-lookup"><span data-stu-id="c6bd7-339">Figure 32</span></span>  
    > `main.css` <span data-ttu-id="c6bd7-340">wurde blockiert</span><span class="sxs-lookup"><span data-stu-id="c6bd7-340">has been blocked</span></span>  
    > <span data-ttu-id="c6bd7-341">! [Main. CSS wurde blockiert] [ImagesTutorialBlockedStyles]</span><span class="sxs-lookup"><span data-stu-id="c6bd7-341">![main.css has been blocked][ImagesTutorialBlockedStyles]</span></span>  

1.  <span data-ttu-id="c6bd7-342">Deaktivieren Sie das Kontrollkästchen **Anforderungs Blockierung aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-342">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="c6bd7-343">Fazit</span><span class="sxs-lookup"><span data-stu-id="c6bd7-343">Conclusion</span></span>  

<span data-ttu-id="c6bd7-344">Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-344">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="c6bd7-345">Sie wissen jetzt, wie Sie das Netzwerk Panel im Microsoft Edge-devtools verwenden!</span><span class="sxs-lookup"><span data-stu-id="c6bd7-345">You now know how to use the Network panel in the Microsoft Edge DevTools!</span></span>






<span data-ttu-id="c6bd7-346">Schauen Sie sich die [Netzwerk Referenz][DevtoolsNetworkReference] an, um weitere devtools-Features im Zusammenhang mit der Überprüfung von Netzwerkaktivitäten zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-346">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Abbildung 1: die Demo"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Console.msft.png "Abbildung 2: die Konsole"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Console-Bottom.msft.png "Abbildung 3: devtools an den unteren Rand des Fensters angedockt"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Bottom.msft.png "Abbildung 4: devtools an den unteren Rand des Fensters angedockt"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network.msft.png "Abbildung 5: das Netzwerkprotokoll"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-New-Resource.msft.png "Abbildung 6: eine neue Ressource im Netzwerkprotokoll"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Edit-column.msft.png "Abbildung 7: Aktivieren der Spalte" Domäne "  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Throttling.msft.png "Abbildung 8: Aktivieren der Drosselung"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Throttling-Slow-3G.msft.png "Abbildung 9: Auswählen von" Slow 3G "  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Empty-Cache-and-Hard-Reset.msft.png "Abbildung 10: leerer Cache und Hard Reload"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Screenshots.msft.png "Abbildung 11: Screenshots der Seite laden"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Screenshots-First.msft.png "Abbildung 12: die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Headers.msft.png "Abbildung 13: die Registerkarte" Überschriften "  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Preview.msft.png "Abbildung 14: die Registerkarte" Vorschau "  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Response.msft.png "Abbildung 15: die Registerkarte" Antwort "  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Timing.msft.png "Abbildung 16: die Registerkarte" Anzeigedauer "  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Close-Tabs.msft.png "Abbildung 17: die Schaltfläche" Schließen "  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Empty.msft.png "Abbildung 18: der Suchbereich"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control.msft.png "Abbildung 19: Suchergebnisse für Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control-Headers-Response-Headers.msft.png "Abbildung 20: hervorgehobenes Suchergebnis auf der Registerkarte" Überschriften "  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-close.msft.png "Abbildung 21: die Schaltflächen" Schließen "  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Empty.msft.png "Abbildung 22: die Symbolleiste" Filter "  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-PNG.msft.png "Abbildung 23: ein Zeichenfolgenfilter"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Regex.msft.png "Abbildung 24: ein Filter für reguläre Ausdrücke"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-negative-Statement.msft.png "Abbildung 25: ein negativer Filter"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Property-Value.msft.png "Abbildung 26: ein Eigenschaften Filter"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-File-Type-CSS.msft.png "Abbildung 27: nur CSS-Dateien anzeigen"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-File-Type-CSS-js.msft.png "Abbildung 28: nur CSS-und JS-Dateien anzeigen"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Empty.msft.png "Abbildung 29: das Befehlsmenü"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block.msft.png "Abbildung 30: Anzeigen der Anforderungs Blockierung"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Add-Pattern.msft.png "Abbildung 31: Blockieren von Main. CSS"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Main-CSS.msft.png "Abbildung 32: Main. CSS wurde blockiert"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Netzwerkanalyse Referenz"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Filter Anforderungen – Netzwerkanalyse Referenz"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ausblenden des Übersichtsbereichs – Netzwerkanalyse Referenz"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Überprüfen der Netzwerk Aktivitäts Demo"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> <span data-ttu-id="c6bd7-388">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c6bd7-389">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c6bd7-391">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c6bd7-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
