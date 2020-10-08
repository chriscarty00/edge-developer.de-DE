---
description: Ein Verweis auf alle Möglichkeiten zum Aufzeichnen und Analysieren der Leistung in Microsoft Edge devtools
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0e81cb89f0e690533bdd9c8fdbfce272610be783
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992904"
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







# <span data-ttu-id="c42a4-104">Referenz zur Leistungsanalyse</span><span class="sxs-lookup"><span data-stu-id="c42a4-104">Performance analysis reference</span></span>   



<span data-ttu-id="c42a4-105">Diese Seite ist eine umfassende Referenz zu den Microsoft Edge devtools-Features, die sich auf die Leistungsanalyse beziehen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="c42a4-106">Eine Anleitung zum Analysieren der Leistung einer Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]finden Sie unter [Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] .</span><span class="sxs-lookup"><span data-stu-id="c42a4-106">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="c42a4-107">Aufzeichnen der Leistung</span><span class="sxs-lookup"><span data-stu-id="c42a4-107">Record performance</span></span>   

### <span data-ttu-id="c42a4-108">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="c42a4-108">Record runtime performance</span></span>   

<span data-ttu-id="c42a4-109">Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, anstatt Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="c42a4-110">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c42a4-111">Klicken Sie in devtools auf die Registerkarte **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-111">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="c42a4-112">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c42a4-112">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="c42a4-114">Record</span><span class="sxs-lookup"><span data-stu-id="c42a4-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="c42a4-115">Interagieren Sie mit der Seite.</span><span class="sxs-lookup"><span data-stu-id="c42a4-115">Interact with the page.</span></span>  <span data-ttu-id="c42a4-116">DevTools zeichnet alle Seiten Aktivitäten auf, die durch ihre Interaktionen entstehen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="c42a4-117">Klicken Sie erneut auf **aufzeichnen** , oder klicken Sie auf **Beenden** , um die Aufzeichnung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-117">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="c42a4-118">Aufzeichnen der Ladeleistung</span><span class="sxs-lookup"><span data-stu-id="c42a4-118">Record load performance</span></span>   

<span data-ttu-id="c42a4-119">Zeichnen Sie die Ladeleistung auf, wenn Sie die Leistung einer Seite während des Ladens analysieren möchten, anstatt Sie zu starten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="c42a4-120">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c42a4-121">Öffnen Sie das **Leistungs** Panel von devtools.</span><span class="sxs-lookup"><span data-stu-id="c42a4-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="c42a4-122">Klicken Sie auf **Seite aktualisieren** \ ( ![ Seite aktualisieren ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c42a4-122">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="c42a4-123">DevTools zeichnet Leistungs Metriken auf, während die Seite aktualisiert wird, und stoppt dann die Aufzeichnung ein paar Sekunden nach Abschluss der Auslastung automatisch.</span><span class="sxs-lookup"><span data-stu-id="c42a4-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="c42a4-125">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c42a4-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="c42a4-126">DevTools zoomt automatisch auf den Teil der Aufzeichnung, in dem die meisten Aktivitäten aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="c42a4-128">Laden einer Seite</span><span class="sxs-lookup"><span data-stu-id="c42a4-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-129">Aufzeichnen von Screenshots während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-129">Capture screenshots while recording</span></span>   

<span data-ttu-id="c42a4-130">Aktivieren Sie das Kontrollkästchen **Screenshots** , um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-130">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="c42a4-132">Das Kontrollkästchen " **Screenshots** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-133">Informationen zum interagieren mit Screenshots finden Sie unter [Anzeigen eines](#view-a-screenshot) Screenshots.</span><span class="sxs-lookup"><span data-stu-id="c42a4-133">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="c42a4-134">Erzwingen der Garbage Collection während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-134">Force garbage collection while recording</span></span>   

<span data-ttu-id="c42a4-135">Klicken Sie, während Sie eine Seite aufzeichnen, auf **Garbage Collection sammeln** \ ( ![ Garbage ][ImageCollectGarbageIcon] Collection), um die Garbage Collection zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-135">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="c42a4-137">Garbage Collection</span><span class="sxs-lookup"><span data-stu-id="c42a4-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-138">Aufzeichnungseinstellungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="c42a4-138">Show recording settings</span></span>   

<span data-ttu-id="c42a4-139">Klicken Sie auf **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureSettingsIcon] \), um weitere Einstellungen anzuzeigen, die sich auf die Darstellung von Leistungs Aufzeichnungen in devtools beziehen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-139">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="c42a4-141">Abschnitt " **aufnahmeeinstellungen** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-142">Deaktivieren von JavaScript-Beispielen</span><span class="sxs-lookup"><span data-stu-id="c42a4-142">Disable JavaScript samples</span></span>   

<span data-ttu-id="c42a4-143">Standardmäßig werden im **Haupt** Abschnitt einer Aufzeichnung detaillierte Aufruflisten von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="c42a4-144">So deaktivieren Sie diese Anruflisten:</span><span class="sxs-lookup"><span data-stu-id="c42a4-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="c42a4-145">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c42a4-146">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c42a4-146">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c42a4-147">Aktivieren Sie das Kontrollkästchen **JavaScript-Beispiele deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-147">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="c42a4-148">Nehmen Sie eine Aufzeichnung der Seite auf.</span><span class="sxs-lookup"><span data-stu-id="c42a4-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="c42a4-149">Die folgenden zwei Abbildungen zeigen den Unterschied zwischen dem deaktivieren und Aktivieren von JavaScript-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="c42a4-150">Der **Haupt** Abschnitt der Aufzeichnung ist viel kürzer, wenn Sampling deaktiviert ist, da alle JavaScript-Aufruflisten ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="c42a4-152">Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="c42a4-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="c42a4-154">Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="c42a4-154">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="c42a4-155">Drosseln des Netzwerks während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-155">Throttle the network while recording</span></span>   

<span data-ttu-id="c42a4-156">So Drosseln Sie das Netzwerk während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="c42a4-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="c42a4-157">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c42a4-158">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c42a4-158">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c42a4-159">Stellen Sie **Network** auf die gewünschte drosselungsebene ein.</span><span class="sxs-lookup"><span data-stu-id="c42a4-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="c42a4-160">Drosseln der CPU während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-160">Throttle the CPU while recording</span></span>   

<span data-ttu-id="c42a4-161">So Drosseln Sie die CPU während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="c42a4-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="c42a4-162">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c42a4-163">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c42a4-163">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c42a4-164">Setzen Sie die **CPU** auf das gewünschte Drosselungs Niveau.</span><span class="sxs-lookup"><span data-stu-id="c42a4-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="c42a4-165">Die Drosselung ist relativ zu den Funktionen Ihres Computers.</span><span class="sxs-lookup"><span data-stu-id="c42a4-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="c42a4-166">Mit der Option " **2X verlangsamen** " wird beispielsweise die CPU zwei Mal langsamer als normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="c42a4-167">DevTools simulieren die CPUs von mobilen Geräten nicht wirklich, da sich die Architektur von mobilen Geräten stark von der von Desktops und Laptops unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="c42a4-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="c42a4-168">Erweiterte Paint-Instrumentation aktivieren</span><span class="sxs-lookup"><span data-stu-id="c42a4-168">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="c42a4-169">So zeigen Sie die detaillierte Farb Instrumentation an:</span><span class="sxs-lookup"><span data-stu-id="c42a4-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="c42a4-170">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c42a4-171">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c42a4-171">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c42a4-172">Aktivieren Sie das Kontrollkästchen **Erweiterte Farb Instrumentation (langsam) aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="c42a4-173">Informationen zur Interaktion mit den Malfarbe-Informationen finden Sie unter [Anzeigen von Ebenen](#view-layers-information) und [Anzeigen von Paint Profiler](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="c42a4-173">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="c42a4-174">Speichern einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-174">Save a recording</span></span>   

<span data-ttu-id="c42a4-175">Wenn Sie eine Aufzeichnung speichern möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-175">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="c42a4-177">Profil speichern</span><span class="sxs-lookup"><span data-stu-id="c42a4-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="c42a4-178">Laden einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-178">Load a recording</span></span>   

<span data-ttu-id="c42a4-179">Wenn Sie eine Aufzeichnung laden möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil laden**aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-179">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="c42a4-181">Profil laden</span><span class="sxs-lookup"><span data-stu-id="c42a4-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="c42a4-182">Löschen der vorherigen Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-182">Clear the previous recording</span></span>   

<span data-ttu-id="c42a4-183">Nachdem Sie eine Aufzeichnung gemacht haben, drücken Sie die **Aufzeichnung löschen** \ ( ![ Aufzeichnung löschen ][ImageClearRecordingIcon] \), um die Aufzeichnung aus dem **Leistungs** Panel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-183">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="c42a4-185">Aufzeichnen löschen</span><span class="sxs-lookup"><span data-stu-id="c42a4-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="c42a4-186">Analysieren einer Leistungsaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-186">Analyze a performance recording</span></span>   

<span data-ttu-id="c42a4-187">Nachdem Sie die Leistung der [Lauf Zeitaufzeichnung](#record-runtime-performance) oder die [Daten Satz Auslastung](#record-load-performance)aufgezeichnet haben, bietet der **Leistungs** Bereich viele Daten für die Analyse der Leistung von dem, was gerade geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="c42a4-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="c42a4-188">Auswählen eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-188">Select a portion of a recording</span></span>   

<span data-ttu-id="c42a4-189">Ziehen Sie den Mauszeiger über die **Übersicht** nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="c42a4-190">Die **Übersicht** ist der Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="c42a4-192">Ziehen Sie den Mauszeiger über die **Übersicht** , um die Ansicht zu vergrößern</span><span class="sxs-lookup"><span data-stu-id="c42a4-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-193">So wählen Sie einen Teil über die Tastatur aus:</span><span class="sxs-lookup"><span data-stu-id="c42a4-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="c42a4-194">Klicken Sie auf den Hintergrund des **Haupt** Abschnitts oder eines der Abschnitte daneben, wie **Interaktionen**, **Netzwerk**oder **GPU**.</span><span class="sxs-lookup"><span data-stu-id="c42a4-194">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="c42a4-195">Dieser Tastatur Workflow funktioniert nur, wenn einer dieser Abschnitte den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="c42a4-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="c42a4-196">Verwenden Sie `W` die `A` Tasten,, `S` , `D` um Sie zu vergrößern, nach Links zu verschieben, zu verkleinern und nach rechts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c42a4-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="c42a4-197">So wählen Sie einen Teil mithilfe eines Trackpads aus:</span><span class="sxs-lookup"><span data-stu-id="c42a4-197">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="c42a4-198">Zeigen Sie mit der Maus auf den Abschnitt " **Übersicht** " oder den Abschnitt " **Details** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="c42a4-199">Der Abschnitt " **Übersicht** " ist der Bereich, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="c42a4-200">Der Abschnitt **Details** ist der Bereich, der den **Haupt** Abschnitt, den Abschnitt **Interaktionen** und so weiter enthält.</span><span class="sxs-lookup"><span data-stu-id="c42a4-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="c42a4-201">Wischen Sie mit zwei Fingern nach oben, um es zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um die Ansicht zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln</span><span class="sxs-lookup"><span data-stu-id="c42a4-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="c42a4-202">Wenn Sie im **Haupt** Abschnitt oder in einem der Nachbarn in einem langen Flammen Diagramm Scrollen möchten, klicken und halten Sie beim Ziehen nach oben und unten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-202">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="c42a4-203">Ziehen Sie nach links und rechts, um zu verschieben, welcher Teil der Aufzeichnung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c42a4-203">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="c42a4-204">Suchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c42a4-204">Search activities</span></span>   

<span data-ttu-id="c42a4-205">Drücken Sie `Control` + `F` \ (Windows \) oder `Command` + `F` \ (macOS \), um das Suchfeld unten im **Leistungs** Bereich zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-205">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="c42a4-207">Suchfeld</span><span class="sxs-lookup"><span data-stu-id="c42a4-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-208">So navigieren Sie in Aktivitäten, die Ihrer Abfrage entsprechen:</span><span class="sxs-lookup"><span data-stu-id="c42a4-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="c42a4-209">Verwenden Sie die Schaltflächen **vorherige** \ ( ![ vorherige ][ImagePreviousIcon] \) und **nächste** \ ( ![ weiter \ ][ImageNextIcon] ).</span><span class="sxs-lookup"><span data-stu-id="c42a4-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="c42a4-210">Drücken Sie `Shift` + `Enter` , um die vorherige oder `Enter` die nächste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-210">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="c42a4-211">So ändern Sie die Abfrageeinstellungen:</span><span class="sxs-lookup"><span data-stu-id="c42a4-211">To modify query settings:</span></span>  

*   <span data-ttu-id="c42a4-212">Drücken Sie **groß** -/Kleinschreibung ![ beachten \ (Groß-/Kleinschreibung ][ImageSearchCaseIcon] beachten \), damit die Abfrage Groß-/Kleinschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="c42a4-213">Drücken Sie **Regex** \ ( ![ Regex ][ImageSearchRegexIcon] \), um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="c42a4-214">Wenn Sie das Suchfeld ausblenden möchten, drücken Sie **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="c42a4-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="c42a4-215">Hauptthread Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="c42a4-215">View main thread activity</span></span>   

<span data-ttu-id="c42a4-216">Verwenden Sie den **Haupt** Abschnitt, um die Aktivitäten anzuzeigen, die im Hauptthread der Seite aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="c42a4-218">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c42a4-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-219">Klicken Sie auf ein Ereignis, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  DevTools skizziert das ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c42a4-219">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="c42a4-221">Weitere Informationen zur `anonymous` Funktion auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-222">DevTools stellt die Hauptthread Aktivität mit einem Flammen Diagramm dar.</span><span class="sxs-lookup"><span data-stu-id="c42a4-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="c42a4-223">Die x-Achse stellt die Aufzeichnung über einen Zeitraum dar.</span><span class="sxs-lookup"><span data-stu-id="c42a4-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="c42a4-224">Die y-Achse steht für die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="c42a4-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="c42a4-225">Die Ereignisse im Vordergrund führen zu den darunter liegenden Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="c42a4-227">Ein Flammen Diagramm</span><span class="sxs-lookup"><span data-stu-id="c42a4-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-228">In der vorherigen Abbildung hat ein `click` Ereignis eine `Function Call` in `activitytabs.js` on Zeile 53 verursacht.</span><span class="sxs-lookup"><span data-stu-id="c42a4-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="c42a4-229">Unten `Function Call` sehen Sie, dass eine anonyme Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-229">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="c42a4-230">Die anonyme Funktion mit dem Namen, die aufgerufen `a` `wait` wird `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-230">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="c42a4-231">DevTools weist Skripten zufällige Farben zu.</span><span class="sxs-lookup"><span data-stu-id="c42a4-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="c42a4-232">In der vorhergehenden Abbildung sind Funktionsaufrufe eines Skripts farbig hellgrün.</span><span class="sxs-lookup"><span data-stu-id="c42a4-232">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="c42a4-233">Anrufe von einem anderen Skript sind farbig beige.</span><span class="sxs-lookup"><span data-stu-id="c42a4-233">Calls from another script are colored beige.</span></span>  <span data-ttu-id="c42a4-234">Das dunklere Gelb steht für Skriptaktivitäten, und das Purple-Ereignis stellt die Rendering-Aktivität dar.</span><span class="sxs-lookup"><span data-stu-id="c42a4-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="c42a4-235">Diese dunkelgelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="c42a4-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="c42a4-236">Weitere Informationen finden Sie unter [Deaktivieren von JavaScript-Beispielen](#disable-javascript-samples) , wenn Sie den detaillierten Flammen Diagramm von JavaScript-anrufen ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-236">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="c42a4-237">Wenn js-Beispiele deaktiviert sind, sehen Sie nur Ereignisse auf höherer Ebene, wie `Event: click` und `Function Call` aus der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="c42a4-237">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="c42a4-238">Anzeigen von Aktivitäten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="c42a4-238">View activities in a table</span></span>   

<span data-ttu-id="c42a4-239">Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Haupt** Abschnitt verlassen, um Aktivitäten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="c42a4-240">DevTools stellt auch drei tabellarische Ansichten zum Analysieren von Aktivitäten bereit.</span><span class="sxs-lookup"><span data-stu-id="c42a4-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="c42a4-241">Jede Ansicht gibt Ihnen eine andere Perspektive auf die Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="c42a4-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="c42a4-242">Wenn Sie die Stammaktivitäten anzeigen möchten, die die meiste Arbeit verursachen, verwenden Sie [die Registerkarte anrufstruktur](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="c42a4-243">Wenn Sie die Aktivitäten anzeigen möchten, bei denen die meiste Zeit direkt ausgegeben wurde, verwenden Sie [die Registerkarte unten nach oben](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="c42a4-244">Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der Sie während der Aufzeichnung aufgetreten sind, verwenden Sie [die Registerkarte Ereignisprotokoll](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c42a4-245">Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.</span><span class="sxs-lookup"><span data-stu-id="c42a4-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="c42a4-246">Führen Sie die Demo selbst auf der [Registerkarte Activity Tabs][ActivityTabsDemo]aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="c42a4-247">Stammaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c42a4-247">Root activities</span></span>   

<span data-ttu-id="c42a4-248">Im folgenden finden Sie eine Erläuterung des Konzepts der **Stammaktivitäten** , das auf der Registerkarte " **anrufstruktur** ", " **Bottom-up-** Registerkarte" und " **Ereignisprotokoll** Abschnitte" erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="c42a4-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="c42a4-249">Stammaktivitäten sind solche, die dazu führen, dass der Browser einige Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c42a4-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="c42a4-250">Wenn Sie beispielsweise auf eine Seite klicken, löst der Browser eine `Event` Aktivität als Stammaktivität aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-250">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="c42a4-251">, Die `Event` dazu führen können, dass ein Handler ausgeführt wird usw.</span><span class="sxs-lookup"><span data-stu-id="c42a4-251">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="c42a4-252">Im Flammen Diagramm des **Haupt** Abschnitts befinden sich die Stammaktivitäten am oberen Rand des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="c42a4-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="c42a4-253">In den Registerkarten " **anrufstruktur** " und " **Ereignisprotokoll** " sind Stammaktivitäten die Elemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="c42a4-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="c42a4-254">Ein Beispiel für Stammaktivitäten finden Sie auf [der Registerkarte anrufstruktur](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="c42a4-254">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="c42a4-255">Die Registerkarte "anrufstruktur"</span><span class="sxs-lookup"><span data-stu-id="c42a4-255">The Call Tree tab</span></span>   

<span data-ttu-id="c42a4-256">Verwenden Sie die Registerkarte **anrufstruktur** , um anzuzeigen, welche [Stammaktivitäten](#root-activities) die meiste Arbeit verursachen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="c42a4-257">Die Registerkarte " **anrufstruktur** " zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c42a4-258">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c42a4-258">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="c42a4-260">Die Registerkarte " **anrufstruktur** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-261">In der vorhergehenden Abbildung sind die Elemente der obersten Ebene in der Spalte **Aktivität** , beispielsweise `Evaluate Script` und Stammaktivitäten, zu finden `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="c42a4-262">Die Schachtelung stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="c42a4-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="c42a4-263">Beispielsweise in der vorherigen Abbildung, die `Parse HTML` verursacht hat, `Evaluate Script` `Compile Script` und `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="c42a4-264">**Self time** steht für die in dieser Aktivität direkt verbrachte Zeit.</span><span class="sxs-lookup"><span data-stu-id="c42a4-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="c42a4-265">**Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="c42a4-266">Klicken Sie auf **selbst Zeit**, **Gesamtzeit**oder **Aktivität** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-266">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="c42a4-267">Verwenden Sie das Textfeld **Filtern** , um Ereignisse nach Aktivitätsname zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c42a4-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="c42a4-268">Standardmäßig ist das Menü **Gruppierung** auf **keine Gruppierung**eingestellt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="c42a4-269">Verwenden Sie das Menü **Gruppierung** , um die aktivitätstabelle auf der Grundlage verschiedener Kriterien zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="c42a4-270">Klicken Sie auf **schwersten Stapel anzeigen** \ ( ![ schwersten Stapel anzeigen ][ImageShowHeaviestStackIcon] \), um eine andere Tabelle rechts neben der **Aktivitäts** Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-270">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="c42a4-271">Klicken Sie auf eine Aktivität, um die **schwerste Stapel** Tabelle aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-271">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="c42a4-272">Die **schwerste Stapel** Tabelle zeigt, welche untergeordneten Elemente der ausgewählten Aktivität am längsten ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-272">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="c42a4-273">Die Registerkarte "Bottom-up"</span><span class="sxs-lookup"><span data-stu-id="c42a4-273">The Bottom-Up tab</span></span>   

<span data-ttu-id="c42a4-274">Verwenden Sie die Registerkarte " **Bottom-up** ", um anzuzeigen, welche Aktivitäten die meiste Zeit im Aggregat Direktaufnahmen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="c42a4-275">Auf der Registerkarte **Bottom-up** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c42a4-276">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c42a4-276">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="c42a4-278">Die Registerkarte " **Bottom-up** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-279">Im **Haupt** Abschnitt Flammen Diagramm der vorhergehenden Abbildung ist zu sehen, dass fast die ganze Zeit ausgeführt wurde `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-279">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="c42a4-280">Die oberste Aktivität auf der Registerkarte " **Bottom-up** " der vorherigen Abbildung ist `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="c42a4-281">Informationen dazu finden Sie auf der Registerkarte " **Bottom-up** " `Layout` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-281">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="c42a4-282">Die Spalte **selbst Zeit** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität für alle Vorkommen aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="c42a4-283">Die Spalte " **Gesamtzeit** " stellt die aggregierte Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="c42a4-284">Die Registerkarte "Ereignisprotokoll"</span><span class="sxs-lookup"><span data-stu-id="c42a4-284">The Event Log tab</span></span>   

<span data-ttu-id="c42a4-285">Verwenden Sie die Registerkarte **Ereignisprotokoll** , um Aktivitäten in der Reihenfolge anzuzeigen, in der Sie während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="c42a4-286">Die Registerkarte **Ereignisprotokoll** zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c42a4-287">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c42a4-287">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="c42a4-289">Die Registerkarte " **Ereignisprotokoll** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-290">Die Spalte **Anfangszeit** steht für den Punkt, an dem die Aktivität gestartet wurde, relativ zum Anfang der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c42a4-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="c42a4-291">Beispielsweise bedeutet die Startzeit `175.7 ms` für das ausgewählte Element in der vorherigen Abbildung, dass die Aktivität nach Beginn der Aufzeichnung 175,7 ms gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="c42a4-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="c42a4-292">Die Spalte **selbst Zeit** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="c42a4-293">Die Spalten **Gesamtzeit** stellt die Zeit dar, die direkt in dieser Aktivität oder in einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="c42a4-294">Klicken Sie auf **Startzeit**, **selbst Zeit**oder **Gesamtzeit** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-294">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="c42a4-295">Verwenden Sie das Textfeld **Filtern** , um Aktivitäten nach Namen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c42a4-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="c42a4-296">Verwenden Sie das Menü " **Dauer** ", um alle Aktivitäten zu filtern, die weniger als 1 MS oder 15 MS dauerte.</span><span class="sxs-lookup"><span data-stu-id="c42a4-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="c42a4-297">Standardmäßig ist das Menü **Dauer** auf **alle**eingestellt, was bedeutet, dass alle Aktivitäten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="c42a4-298">Deaktivieren Sie die Kontrollkästchen **Lade**-, **Skripting**-, **Rendering**-oder **Painting** , um alle Aktivitäten aus diesen Kategorien zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c42a4-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="c42a4-299">Anzeigen der GPU-Aktivität</span><span class="sxs-lookup"><span data-stu-id="c42a4-299">View GPU activity</span></span>   

<span data-ttu-id="c42a4-300">Zeigen Sie die GPU-Aktivität im Abschnitt **GPU** an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="c42a4-302">Der **GPU** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c42a4-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-303">Raster Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="c42a4-303">View raster activity</span></span>   

<span data-ttu-id="c42a4-304">Raster Aktivitäten im **Raster** Abschnitt anzeigen</span><span class="sxs-lookup"><span data-stu-id="c42a4-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="c42a4-306">Der **Raster** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c42a4-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-307">Anzeigen von Interaktionen</span><span class="sxs-lookup"><span data-stu-id="c42a4-307">View interactions</span></span>   

<span data-ttu-id="c42a4-308">Verwenden Sie den Abschnitt **Interaktionen** , um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="c42a4-310">Abschnitt " **Interaktionen** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-311">Eine rote Zeile am unteren Rand einer Interaktion stellt die Zeit dar, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="c42a4-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="c42a4-312">Klicken Sie auf eine Interaktion, um weitere Informationen dazu auf der Registerkarte **Zusammenfassung** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-312">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="c42a4-313">Analysieren von Frames pro Sekunde (fps)</span><span class="sxs-lookup"><span data-stu-id="c42a4-313">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="c42a4-314">DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:</span><span class="sxs-lookup"><span data-stu-id="c42a4-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="c42a4-315">Verwenden Sie [das FPS-Diagramm](#the-fps-chart) , um einen Überblick über fps über die Dauer der Aufzeichnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="c42a4-316">Verwenden Sie [den Abschnitt Frames](#the-frames-section) , um anzuzeigen, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="c42a4-317">Verwenden Sie das **fps-Messgerät** für eine echt Zeitschätzung von fps während der Ausführung der Seite.</span><span class="sxs-lookup"><span data-stu-id="c42a4-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c42a4-318">Informationen dazu finden Sie unter [Anzeigen von Frames pro Sekunde in Echtzeit mit dem FPS-Meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="c42a4-318">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="c42a4-319">Das fps-Diagramm</span><span class="sxs-lookup"><span data-stu-id="c42a4-319">The FPS chart</span></span>   

<span data-ttu-id="c42a4-320">Das **fps** -Diagramm bietet eine Übersicht über die Framerate für die Dauer einer Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c42a4-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="c42a4-321">Je höher die grüne Leiste, desto besser die Framerate.</span><span class="sxs-lookup"><span data-stu-id="c42a4-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="c42a4-322">Eine rote Leiste oberhalb des **fps** -Diagramms ist eine Warnung, dass die Framerate so gering war, dass Sie möglicherweise die Benutzererfahrung beeinträchtigte.</span><span class="sxs-lookup"><span data-stu-id="c42a4-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="c42a4-324">Das **fps** -Diagramm</span><span class="sxs-lookup"><span data-stu-id="c42a4-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="c42a4-325">Der Abschnitt "Frames"</span><span class="sxs-lookup"><span data-stu-id="c42a4-325">The Frames section</span></span>   

<span data-ttu-id="c42a4-326">Im Abschnitt **Frames** erfahren Sie genau, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="c42a4-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="c42a4-327">Zeigen Sie mit der Maus auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="c42a4-329">Zeigen Sie mit der Maus auf einen Frame</span><span class="sxs-lookup"><span data-stu-id="c42a4-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-330">Klicken Sie auf einen Frame, um auf der Registerkarte **Zusammenfassung** noch weitere Informationen zu dem Frame anzuzeigen.  DevTools konturiert den markierten Frame in blau.</span><span class="sxs-lookup"><span data-stu-id="c42a4-330">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="c42a4-332">Anzeigen eines Frames auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-333">Anzeigen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="c42a4-333">View network requests</span></span>   

<span data-ttu-id="c42a4-334">Erweitern Sie den Abschnitt **Netzwerk** , um einen Wasserfall von Netzwerkanforderungen anzuzeigen, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c42a4-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="c42a4-336">Der Abschnitt " **Netzwerk** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-337">Anforderungen werden wie folgt farblich gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="c42a4-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="c42a4-338">HTML: blau</span><span class="sxs-lookup"><span data-stu-id="c42a4-338">HTML: Blue</span></span>  
*   <span data-ttu-id="c42a4-339">CSS: lila</span><span class="sxs-lookup"><span data-stu-id="c42a4-339">CSS: Purple</span></span>  
*   <span data-ttu-id="c42a4-340">JS: gelb</span><span class="sxs-lookup"><span data-stu-id="c42a4-340">JS: Yellow</span></span>  
*   <span data-ttu-id="c42a4-341">Bilder: grün</span><span class="sxs-lookup"><span data-stu-id="c42a4-341">Images: Green</span></span>  
    
<span data-ttu-id="c42a4-342">Klicken Sie auf eine Anfrage, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  In der vorhergehenden Abbildung werden beispielsweise auf der Registerkarte **Zusammenfassung** Weitere Informationen zu der im Abschnitt **Netzwerk** ausgewählten blauen Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-342">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="c42a4-343">Ein dunkelblaues Quadrat in der oberen linken Ecke einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="c42a4-344">Ein helleres blaues Quadrat bedeutet niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="c42a4-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="c42a4-345">In der vorhergehenden Abbildung ist beispielsweise die blaue, ausgewählte Anforderung eine höhere Priorität, und die grüne darunter hat eine niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="c42a4-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="c42a4-346">In der ersten der folgenden Zahlen wird die Anforderung für `www.bing.com` durch eine Zeile auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Teil und einem hellen Teil sowie eine Zeile auf der rechten Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="c42a4-347">In der zweiten der folgenden Abbildungen wird die entsprechende Darstellung der gleichen Anforderung auf der Registerkarte **Anzeige** Dauer im **Netzwerk** Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="c42a4-348">Hier sehen Sie, wie diese beiden Darstellungen einander zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="c42a4-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="c42a4-349">Die linke Zeile ist alles bis zur `Connection Start` Gruppe von Ereignissen inklusive.</span><span class="sxs-lookup"><span data-stu-id="c42a4-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="c42a4-350">Mit anderen Worten: Es ist alles vor `Request Sent` , exklusiv.</span><span class="sxs-lookup"><span data-stu-id="c42a4-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="c42a4-351">Der helle Bereich der Leiste ist `Request Sent` und `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="c42a4-352">Der dunkle Teil der Leiste ist `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="c42a4-353">Die richtige Zeile ist im Wesentlichen die Zeit, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="c42a4-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="c42a4-354">Diese wird auf der Registerkarte **Anzeige** Dauer nicht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="c42a4-356">Die Zeile-Balken-Darstellung der `www.bing.com` Anforderung</span><span class="sxs-lookup"><span data-stu-id="c42a4-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="c42a4-358">Der Abschnitt " **Netzwerk** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-358">The **Network** section</span></span>  
<span data-ttu-id="c42a4-359">::: Image-End:::</span><span class="sxs-lookup"><span data-stu-id="c42a4-359">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="c42a4-360">Anzeigen von Speicher Metriken</span><span class="sxs-lookup"><span data-stu-id="c42a4-360">View memory metrics</span></span>   

<span data-ttu-id="c42a4-361">Aktivieren Sie das Kontrollkästchen **Speicher** , um Speicher Metriken aus der letzten Aufzeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-361">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="c42a4-363">Das Kontrollkästchen " **Speicher** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-364">DevTools zeigt ein neues **Speicher** Diagramm über der Registerkarte " **Zusammenfassung** " an.  Es gibt auch ein neues Diagramm unter dem **Netz** Diagramm, das als **Heap**bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c42a4-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="c42a4-365">Das **Heap** Diagramm bietet dieselben Informationen wie die **js-heaplinie** im **Speicher** Diagramm.</span><span class="sxs-lookup"><span data-stu-id="c42a4-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="c42a4-367">Speicher Metriken</span><span class="sxs-lookup"><span data-stu-id="c42a4-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-368">Die farbigen Linien auf dem Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c42a4-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="c42a4-369">Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie aus dem Diagramm auszublenden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="c42a4-370">Das Diagramm zeigt nur den Bereich der Aufzeichnung an, der aktuell markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c42a4-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="c42a4-371">In der vorhergehenden Abbildung zeigt das **Speicher** Diagramm beispielsweise nur die Speicherauslastung von der 400 MS-Marke bis zum 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="c42a4-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="c42a4-372">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-372">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="c42a4-373">Wenn Sie einen Abschnitt wie " **Netzwerk** " oder " **Main**" analysieren, benötigen Sie manchmal eine genauere Einschätzung, wie lange bestimmte Ereignisse dauerte.</span><span class="sxs-lookup"><span data-stu-id="c42a4-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="c42a4-374">Halten `Shift` , klicken und halten Sie, und ziehen Sie nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-374">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="c42a4-375">Am unteren Rand Ihrer Auswahl zeigt devtools an, wie lange dieser Teil dauerte.</span><span class="sxs-lookup"><span data-stu-id="c42a4-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="c42a4-377">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c42a4-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-378">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="c42a4-378">View a screenshot</span></span>   

<span data-ttu-id="c42a4-379">Informationen zum Aktivieren von Screenshots finden Sie unter [Aufzeichnen von Screenshots während der Aufzeichnung](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="c42a4-379">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="c42a4-380">Zeigen Sie mit der Maus auf die **Übersicht** , um einen Screenshot zu sehen, wie die Seite während dieses Moments der Aufzeichnung aussah.</span><span class="sxs-lookup"><span data-stu-id="c42a4-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="c42a4-381">Die **Übersicht** ist der Abschnitt mit den Diagrammen **CPU**, **fps**und **net** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="c42a4-383">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="c42a4-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-384">Sie können Screenshots auch anzeigen, indem Sie im Abschnitt **Frames** auf einen Frame klicken.</span><span class="sxs-lookup"><span data-stu-id="c42a4-384">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="c42a4-385">DevTools zeigt eine kleine Version des Screenshots auf der Registerkarte " **Zusammenfassung** " an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="c42a4-387">Anzeigen eines Screenshots auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-388">Klicken Sie auf der Registerkarte **Zusammenfassung** auf die Miniaturansicht, um den Screenshot zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="c42a4-388">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="c42a4-390">Vergrößern eines Screenshots über die Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c42a4-391">Informationen zu Layern anzeigen</span><span class="sxs-lookup"><span data-stu-id="c42a4-391">View layers information</span></span>   

<span data-ttu-id="c42a4-392">So zeigen Sie erweiterte Folieninformationen zu einem Frame an:</span><span class="sxs-lookup"><span data-stu-id="c42a4-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="c42a4-393">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="c42a4-393">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c42a4-394">Wählen Sie im Abschnitt **Frames** einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="c42a4-395">DevTools zeigt Informationen zu den Ebenen auf der Registerkarte "neue **Ebenen** " neben der Registerkarte " **Ereignisprotokoll** " an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="c42a4-397">Der Bereich " **Ebenen** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c42a4-398">Zeigen Sie mit der Maus auf eine Ebene, um Sie im Diagramm hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="c42a4-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="c42a4-400">Markieren eines Layers</span><span class="sxs-lookup"><span data-stu-id="c42a4-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="c42a4-401">So verschieben Sie das Diagramm:</span><span class="sxs-lookup"><span data-stu-id="c42a4-401">To move the diagram:</span></span>  

*   <span data-ttu-id="c42a4-402">Klicken Sie auf **Schwenkmodus** \ ( ![ Schwenkmodus ][ImagePanModeIcon] \), um entlang der X-und Y-Achse zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-402">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="c42a4-403">Klicken Sie auf **Drehungsmodus** \ ( ![ Rotationsmodus ][ImageRotateModeIcon] \), um sich entlang der Z-Achse zu drehen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-403">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="c42a4-404">Klicken Sie auf **Transform zurücksetzen** \ ( ![ Transform zurücksetzen ][ImageResetTransformIcon] \), um das Diagramm auf die ursprüngliche Position zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-404">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="c42a4-405">Anzeigen des Paint-Profilers</span><span class="sxs-lookup"><span data-stu-id="c42a4-405">View paint profiler</span></span>   

<span data-ttu-id="c42a4-406">So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:</span><span class="sxs-lookup"><span data-stu-id="c42a4-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="c42a4-407">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="c42a4-407">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c42a4-408">Wählen Sie im **Haupt** Abschnitt ein **Paint** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="c42a4-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="c42a4-410">Die Registerkarte " **Paint-Profiler** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c42a4-411">Analysieren der Renderingleistung mit der Registerkarte "Rendern"</span><span class="sxs-lookup"><span data-stu-id="c42a4-411">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="c42a4-412">Verwenden Sie die Features der Registerkarte " **Rendern** ", um die Renderingleistung Ihrer Seite zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c42a4-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="c42a4-413">So öffnen Sie die Registerkarte " **Rendering** ":</span><span class="sxs-lookup"><span data-stu-id="c42a4-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="c42a4-414">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="c42a4-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="c42a4-415">Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="c42a4-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="c42a4-416">DevTools zeigt die Registerkarte " **Rendering** " am unteren Rand des devtools-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="c42a4-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="c42a4-418">Die Registerkarte " **Rendern** "</span><span class="sxs-lookup"><span data-stu-id="c42a4-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c42a4-419">Anzeigen von Frames pro Sekunde in Echtzeit mit dem fps-Messgerät</span><span class="sxs-lookup"><span data-stu-id="c42a4-419">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="c42a4-420">Das **fps-Messgerät** ist ein Overlay, das in der oberen rechten Ecke des Viewports angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c42a4-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="c42a4-421">Bei der Ausführung der Seite wird eine Echtzeit-Schätzung von fps bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c42a4-422">So öffnen Sie das **fps-Messgerät**:</span><span class="sxs-lookup"><span data-stu-id="c42a4-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="c42a4-423">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-423">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c42a4-424">Aktivieren Sie das Kontrollkästchen **FPS-Meter** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-424">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="c42a4-426">Das **fps-Messgerät**</span><span class="sxs-lookup"><span data-stu-id="c42a4-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c42a4-427">Anzeigen von Zeichnungs Ereignissen in Echtzeit mit Farb blinken</span><span class="sxs-lookup"><span data-stu-id="c42a4-427">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="c42a4-428">Verwenden Sie das Farb blinken, um eine Echtzeitansicht aller Paint-Ereignisse auf der Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c42a4-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="c42a4-429">Jedes Mal, wenn ein Teil der Seite neu gestrichen wird, wird der Abschnitt in devtools in grün umrissen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="c42a4-430">So aktivieren Sie die Farb Blinkfunktion:</span><span class="sxs-lookup"><span data-stu-id="c42a4-430">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="c42a4-431">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-431">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c42a4-432">Aktivieren Sie das Kontrollkästchen " **Farbe blinkt** ".</span><span class="sxs-lookup"><span data-stu-id="c42a4-432">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="c42a4-434">Malen blinkt</span><span class="sxs-lookup"><span data-stu-id="c42a4-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="c42a4-435">Anzeigen einer Überlagerung von Ebenen mit Ebenen Rändern</span><span class="sxs-lookup"><span data-stu-id="c42a4-435">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="c42a4-436">Verwenden Sie **Layer-Rahmen** , um eine Überlagerung von Layer-Rändern und Kacheln oben auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c42a4-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="c42a4-437">So aktivieren Sie Layer-Rahmen:</span><span class="sxs-lookup"><span data-stu-id="c42a4-437">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="c42a4-438">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-438">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c42a4-439">Aktivieren Sie das Kontrollkästchen **Layer-Rahmen** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-439">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="c42a4-441">Folienrahmen</span><span class="sxs-lookup"><span data-stu-id="c42a4-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="c42a4-442">[`debug_colors.cc`][ChromiumDebugColors]Eine Erläuterung der Farbcodierungen finden Sie in den Kommentaren in.</span><span class="sxs-lookup"><span data-stu-id="c42a4-442">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="c42a4-443">Suchen von Scroll-Leistungsproblemen in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="c42a4-443">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="c42a4-444">Verwenden Sie Leistungsprobleme beim Scrollen, um Elemente der Seite zu identifizieren, die Ereignislistener in Bezug auf den Bildlauf aufweisen, die die Leistung der Seite beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="c42a4-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="c42a4-445">DevTools beschreibt die potenziell problematischen Elemente in Teal.</span><span class="sxs-lookup"><span data-stu-id="c42a4-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="c42a4-446">So zeigen Sie Bild Lauf Leistungsprobleme an:</span><span class="sxs-lookup"><span data-stu-id="c42a4-446">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="c42a4-447">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c42a4-447">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c42a4-448">Aktivieren Sie das Kontrollkästchen **Scrolling Performance Issues** .</span><span class="sxs-lookup"><span data-stu-id="c42a4-448">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="c42a4-450">**Probleme mit der Bildlaufleistung** deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="c42a4-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
<!--  
<!--    


-->  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Erste Schritte mit der Analyse der Laufzeitleistung | Microsoft docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demo für Aktivitäts Registerkarten | Glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-Code Suche"  

> [!NOTE]
> <span data-ttu-id="c42a4-456">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c42a4-456">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c42a4-457">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c42a4-457">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c42a4-459">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c42a4-459">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
