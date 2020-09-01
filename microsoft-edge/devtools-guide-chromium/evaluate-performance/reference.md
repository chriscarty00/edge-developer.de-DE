---
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 59e2f67d773102554b96749690fae51da09428a8
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984092"
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







# <span data-ttu-id="6ac00-103">Referenz zur Leistungsanalyse</span><span class="sxs-lookup"><span data-stu-id="6ac00-103">Performance analysis reference</span></span>   



<span data-ttu-id="6ac00-104">Diese Seite ist eine umfassende Referenz zu den Microsoft Edge devtools-Features, die sich auf die Leistungsanalyse beziehen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="6ac00-105">Eine Anleitung zum Analysieren der Leistung einer Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]finden Sie unter [Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] .</span><span class="sxs-lookup"><span data-stu-id="6ac00-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="6ac00-106">Aufzeichnen der Leistung</span><span class="sxs-lookup"><span data-stu-id="6ac00-106">Record performance</span></span>   

### <span data-ttu-id="6ac00-107">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="6ac00-107">Record runtime performance</span></span>   

<span data-ttu-id="6ac00-108">Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, anstatt Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="6ac00-109">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6ac00-110">Klicken Sie in devtools auf die Registerkarte **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="6ac00-111">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6ac00-111">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="6ac00-113">Record</span><span class="sxs-lookup"><span data-stu-id="6ac00-113">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="6ac00-114">Interagieren Sie mit der Seite.</span><span class="sxs-lookup"><span data-stu-id="6ac00-114">Interact with the page.</span></span>  <span data-ttu-id="6ac00-115">DevTools zeichnet alle Seiten Aktivitäten auf, die durch ihre Interaktionen entstehen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-115">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="6ac00-116">Klicken Sie erneut auf **aufzeichnen** , oder klicken Sie auf **Beenden** , um die Aufzeichnung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-116">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="6ac00-117">Aufzeichnen der Ladeleistung</span><span class="sxs-lookup"><span data-stu-id="6ac00-117">Record load performance</span></span>   

<span data-ttu-id="6ac00-118">Zeichnen Sie die Ladeleistung auf, wenn Sie die Leistung einer Seite während des Ladens analysieren möchten, anstatt Sie zu starten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-118">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="6ac00-119">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-119">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6ac00-120">Öffnen Sie das **Leistungs** Panel von devtools.</span><span class="sxs-lookup"><span data-stu-id="6ac00-120">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="6ac00-121">Klicken Sie auf **Seite aktualisieren** \ ( ![ Seite aktualisieren ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6ac00-121">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="6ac00-122">DevTools zeichnet Leistungs Metriken auf, während die Seite aktualisiert wird, und stoppt dann die Aufzeichnung ein paar Sekunden nach Abschluss der Auslastung automatisch.</span><span class="sxs-lookup"><span data-stu-id="6ac00-122">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Seite aktualisieren" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="6ac00-124">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6ac00-124">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6ac00-125">DevTools zoomt automatisch auf den Teil der Aufzeichnung, in dem die meisten Aktivitäten aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-125">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Laden einer Seite" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="6ac00-127">Laden einer Seite</span><span class="sxs-lookup"><span data-stu-id="6ac00-127">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-128">Aufzeichnen von Screenshots während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-128">Capture screenshots while recording</span></span>   

<span data-ttu-id="6ac00-129">Aktivieren Sie das Kontrollkästchen **Screenshots** , um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-129">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Das Kontrollkästchen "Screenshots"" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="6ac00-131">Das Kontrollkästchen " **Screenshots** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-131">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-132">Informationen zum interagieren mit Screenshots finden Sie unter [Anzeigen eines](#view-a-screenshot) Screenshots.</span><span class="sxs-lookup"><span data-stu-id="6ac00-132">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="6ac00-133">Erzwingen der Garbage Collection während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-133">Force garbage collection while recording</span></span>   

<span data-ttu-id="6ac00-134">Klicken Sie, während Sie eine Seite aufzeichnen, auf **Garbage Collection sammeln** \ ( ![ Garbage ][ImageCollectGarbageIcon] Collection), um die Garbage Collection zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-134">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Garbage Collection" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="6ac00-136">Garbage Collection</span><span class="sxs-lookup"><span data-stu-id="6ac00-136">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-137">Aufzeichnungseinstellungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac00-137">Show recording settings</span></span>   

<span data-ttu-id="6ac00-138">Klicken Sie auf **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureSettingsIcon] \), um weitere Einstellungen anzuzeigen, die sich auf die Darstellung von Leistungs Aufzeichnungen in devtools beziehen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-138">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Abschnitt "Aufnahmeeinstellungen"" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="6ac00-140">Abschnitt " **aufnahmeeinstellungen** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-140">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-141">Deaktivieren von JavaScript-Beispielen</span><span class="sxs-lookup"><span data-stu-id="6ac00-141">Disable JavaScript samples</span></span>   

<span data-ttu-id="6ac00-142">Standardmäßig werden im **Haupt** Abschnitt einer Aufzeichnung detaillierte Aufruflisten von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-142">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="6ac00-143">So deaktivieren Sie diese Anruflisten:</span><span class="sxs-lookup"><span data-stu-id="6ac00-143">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="6ac00-144">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-144">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ac00-145">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ac00-145">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ac00-146">Aktivieren Sie das Kontrollkästchen **JavaScript-Beispiele deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-146">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="6ac00-147">Nehmen Sie eine Aufzeichnung der Seite auf.</span><span class="sxs-lookup"><span data-stu-id="6ac00-147">Take a recording of the page.</span></span>  
    
<span data-ttu-id="6ac00-148">Die folgenden zwei Abbildungen zeigen den Unterschied zwischen dem deaktivieren und Aktivieren von JavaScript-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-148">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="6ac00-149">Der **Haupt** Abschnitt der Aufzeichnung ist viel kürzer, wenn Sampling deaktiviert ist, da alle JavaScript-Aufruflisten ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-149">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="6ac00-151">Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="6ac00-151">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="6ac00-153">Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="6ac00-153">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6ac00-154">Drosseln des Netzwerks während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-154">Throttle the network while recording</span></span>   

<span data-ttu-id="6ac00-155">So Drosseln Sie das Netzwerk während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="6ac00-155">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="6ac00-156">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-156">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ac00-157">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ac00-157">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ac00-158">Stellen Sie **Network** auf die gewünschte drosselungsebene ein.</span><span class="sxs-lookup"><span data-stu-id="6ac00-158">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="6ac00-159">Drosseln der CPU während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-159">Throttle the CPU while recording</span></span>   

<span data-ttu-id="6ac00-160">So Drosseln Sie die CPU während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="6ac00-160">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="6ac00-161">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-161">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ac00-162">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ac00-162">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ac00-163">Setzen Sie die **CPU** auf das gewünschte Drosselungs Niveau.</span><span class="sxs-lookup"><span data-stu-id="6ac00-163">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="6ac00-164">Die Drosselung ist relativ zu den Funktionen Ihres Computers.</span><span class="sxs-lookup"><span data-stu-id="6ac00-164">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="6ac00-165">Mit der Option " **2X verlangsamen** " wird beispielsweise die CPU zwei Mal langsamer als normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-165">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="6ac00-166">DevTools simulieren die CPUs von mobilen Geräten nicht wirklich, da sich die Architektur von mobilen Geräten stark von der von Desktops und Laptops unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="6ac00-166">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="6ac00-167">Erweiterte Paint-Instrumentation aktivieren</span><span class="sxs-lookup"><span data-stu-id="6ac00-167">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="6ac00-168">So zeigen Sie die detaillierte Farb Instrumentation an:</span><span class="sxs-lookup"><span data-stu-id="6ac00-168">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="6ac00-169">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ac00-170">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ac00-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ac00-171">Aktivieren Sie das Kontrollkästchen **Erweiterte Farb Instrumentation (langsam) aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-171">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="6ac00-172">Informationen zur Interaktion mit den Malfarbe-Informationen finden Sie unter [Anzeigen von Ebenen](#view-layers-information) und [Anzeigen von Paint Profiler](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="6ac00-172">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="6ac00-173">Speichern einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-173">Save a recording</span></span>   

<span data-ttu-id="6ac00-174">Wenn Sie eine Aufzeichnung speichern möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-174">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Profil speichern" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="6ac00-176">Profil speichern</span><span class="sxs-lookup"><span data-stu-id="6ac00-176">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ac00-177">Laden einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-177">Load a recording</span></span>   

<span data-ttu-id="6ac00-178">Wenn Sie eine Aufzeichnung laden möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil laden**aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-178">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Profil laden" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="6ac00-180">Profil laden</span><span class="sxs-lookup"><span data-stu-id="6ac00-180">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ac00-181">Löschen der vorherigen Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-181">Clear the previous recording</span></span>   

<span data-ttu-id="6ac00-182">Nachdem Sie eine Aufzeichnung gemacht haben, drücken Sie die **Aufzeichnung löschen** \ ( ![ Aufzeichnung löschen ][ImageClearRecordingIcon] \), um die Aufzeichnung aus dem **Leistungs** Panel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-182">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Aufzeichnen löschen" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="6ac00-184">Aufzeichnen löschen</span><span class="sxs-lookup"><span data-stu-id="6ac00-184">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ac00-185">Analysieren einer Leistungsaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-185">Analyze a performance recording</span></span>   

<span data-ttu-id="6ac00-186">Nachdem Sie die Leistung der [Lauf Zeitaufzeichnung](#record-runtime-performance) oder die [Daten Satz Auslastung](#record-load-performance)aufgezeichnet haben, bietet der **Leistungs** Bereich viele Daten für die Analyse der Leistung von dem, was gerade geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="6ac00-186">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="6ac00-187">Auswählen eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-187">Select a portion of a recording</span></span>   

<span data-ttu-id="6ac00-188">Ziehen Sie den Mauszeiger über die **Übersicht** nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-188">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="6ac00-189">Die **Übersicht** ist der Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-189">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Ziehen Sie den Mauszeiger über die Übersicht, um die Ansicht zu vergrößern" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="6ac00-191">Ziehen Sie den Mauszeiger über die **Übersicht** , um die Ansicht zu vergrößern</span><span class="sxs-lookup"><span data-stu-id="6ac00-191">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-192">So wählen Sie einen Teil über die Tastatur aus:</span><span class="sxs-lookup"><span data-stu-id="6ac00-192">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="6ac00-193">Klicken Sie auf den Hintergrund des **Haupt** Abschnitts oder eines der Abschnitte daneben, wie **Interaktionen**, **Netzwerk**oder **GPU**.</span><span class="sxs-lookup"><span data-stu-id="6ac00-193">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="6ac00-194">Dieser Tastatur Workflow funktioniert nur, wenn einer dieser Abschnitte den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="6ac00-194">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="6ac00-195">Verwenden Sie `W` die `A` Tasten,, `S` , `D` um Sie zu vergrößern, nach Links zu verschieben, zu verkleinern und nach rechts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6ac00-195">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="6ac00-196">So wählen Sie einen Teil mithilfe eines Trackpads aus:</span><span class="sxs-lookup"><span data-stu-id="6ac00-196">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="6ac00-197">Zeigen Sie mit der Maus auf den Abschnitt " **Übersicht** " oder den Abschnitt " **Details** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-197">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="6ac00-198">Der Abschnitt " **Übersicht** " ist der Bereich, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-198">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="6ac00-199">Der Abschnitt **Details** ist der Bereich, der den **Haupt** Abschnitt, den Abschnitt **Interaktionen** und so weiter enthält.</span><span class="sxs-lookup"><span data-stu-id="6ac00-199">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="6ac00-200">Wischen Sie mit zwei Fingern nach oben, um es zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um die Ansicht zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln</span><span class="sxs-lookup"><span data-stu-id="6ac00-200">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="6ac00-201">Wenn Sie im **Haupt** Abschnitt oder in einem der Nachbarn in einem langen Flammen Diagramm Scrollen möchten, klicken und halten Sie beim Ziehen nach oben und unten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-201">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="6ac00-202">Ziehen Sie nach links und rechts, um zu verschieben, welcher Teil der Aufzeichnung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ac00-202">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="6ac00-203">Suchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="6ac00-203">Search activities</span></span>   

<span data-ttu-id="6ac00-204">Drücken Sie `Control` + `F` \ (Windows \) oder `Command` + `F` \ (macOS \), um das Suchfeld unten im **Leistungs** Bereich zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-204">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Suchfeld" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="6ac00-206">Suchfeld</span><span class="sxs-lookup"><span data-stu-id="6ac00-206">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-207">So navigieren Sie in Aktivitäten, die Ihrer Abfrage entsprechen:</span><span class="sxs-lookup"><span data-stu-id="6ac00-207">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="6ac00-208">Verwenden Sie die Schaltflächen **vorherige** \ ( ![ vorherige ][ImagePreviousIcon] \) und **nächste** \ ( ![ weiter \ ][ImageNextIcon] ).</span><span class="sxs-lookup"><span data-stu-id="6ac00-208">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="6ac00-209">Drücken Sie `Shift` + `Enter` , um die vorherige oder `Enter` die nächste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-209">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="6ac00-210">So ändern Sie die Abfrageeinstellungen:</span><span class="sxs-lookup"><span data-stu-id="6ac00-210">To modify query settings:</span></span>  

*   <span data-ttu-id="6ac00-211">Drücken Sie **groß** -/Kleinschreibung ![ beachten \ (Groß-/Kleinschreibung ][ImageSearchCaseIcon] beachten \), damit die Abfrage Groß-/Kleinschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-211">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="6ac00-212">Drücken Sie **Regex** \ ( ![ Regex ][ImageSearchRegexIcon] \), um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-212">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="6ac00-213">Wenn Sie das Suchfeld ausblenden möchten, drücken Sie **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="6ac00-213">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="6ac00-214">Hauptthread Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac00-214">View main thread activity</span></span>   

<span data-ttu-id="6ac00-215">Verwenden Sie den **Haupt** Abschnitt, um die Aktivitäten anzuzeigen, die im Hauptthread der Seite aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-215">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Der Hauptabschnitt" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="6ac00-217">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6ac00-217">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-218">Klicken Sie auf ein Ereignis, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  DevTools skizziert das ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6ac00-218">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Weitere Informationen zur anonymen Funktion auf der Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="6ac00-220">Weitere Informationen zur `anonymous` Funktion auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-220">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-221">DevTools stellt die Hauptthread Aktivität mit einem Flammen Diagramm dar.</span><span class="sxs-lookup"><span data-stu-id="6ac00-221">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="6ac00-222">Die x-Achse stellt die Aufzeichnung über einen Zeitraum dar.</span><span class="sxs-lookup"><span data-stu-id="6ac00-222">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="6ac00-223">Die y-Achse steht für die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="6ac00-223">The y-axis represents the call stack.</span></span>  <span data-ttu-id="6ac00-224">Die Ereignisse im Vordergrund führen zu den darunter liegenden Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-224">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Ein Flammen Diagramm" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="6ac00-226">Ein Flammen Diagramm</span><span class="sxs-lookup"><span data-stu-id="6ac00-226">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-227">In der vorherigen Abbildung hat ein `click` Ereignis eine `Function Call` in `activitytabs.js` on Zeile 53 verursacht.</span><span class="sxs-lookup"><span data-stu-id="6ac00-227">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="6ac00-228">Unten `Function Call` sehen Sie, dass eine anonyme Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-228">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="6ac00-229">Die anonyme Funktion mit dem Namen, die aufgerufen `a` `wait` wird `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-229">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="6ac00-230">DevTools weist Skripten zufällige Farben zu.</span><span class="sxs-lookup"><span data-stu-id="6ac00-230">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="6ac00-231">In der vorhergehenden Abbildung sind Funktionsaufrufe eines Skripts farbig hellgrün.</span><span class="sxs-lookup"><span data-stu-id="6ac00-231">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="6ac00-232">Anrufe von einem anderen Skript sind farbig beige.</span><span class="sxs-lookup"><span data-stu-id="6ac00-232">Calls from another script are colored beige.</span></span>  <span data-ttu-id="6ac00-233">Das dunklere Gelb steht für Skriptaktivitäten, und das Purple-Ereignis stellt die Rendering-Aktivität dar.</span><span class="sxs-lookup"><span data-stu-id="6ac00-233">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="6ac00-234">Diese dunkelgelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="6ac00-234">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="6ac00-235">Weitere Informationen finden Sie unter [Deaktivieren von JavaScript-Beispielen](#disable-javascript-samples) , wenn Sie den detaillierten Flammen Diagramm von JavaScript-anrufen ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-235">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="6ac00-236">Wenn js-Beispiele deaktiviert sind, sehen Sie nur Ereignisse auf höherer Ebene, wie `Event: click` und `Function Call` aus der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="6ac00-236">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="6ac00-237">Anzeigen von Aktivitäten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="6ac00-237">View activities in a table</span></span>   

<span data-ttu-id="6ac00-238">Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Haupt** Abschnitt verlassen, um Aktivitäten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-238">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="6ac00-239">DevTools stellt auch drei tabellarische Ansichten zum Analysieren von Aktivitäten bereit.</span><span class="sxs-lookup"><span data-stu-id="6ac00-239">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="6ac00-240">Jede Ansicht gibt Ihnen eine andere Perspektive auf die Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="6ac00-240">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="6ac00-241">Wenn Sie die Stammaktivitäten anzeigen möchten, die die meiste Arbeit verursachen, verwenden Sie [die Registerkarte anrufstruktur](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-241">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="6ac00-242">Wenn Sie die Aktivitäten anzeigen möchten, bei denen die meiste Zeit direkt ausgegeben wurde, verwenden Sie [die Registerkarte unten nach oben](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-242">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="6ac00-243">Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der Sie während der Aufzeichnung aufgetreten sind, verwenden Sie [die Registerkarte Ereignisprotokoll](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-243">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6ac00-244">Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.</span><span class="sxs-lookup"><span data-stu-id="6ac00-244">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="6ac00-245">Führen Sie die Demo selbst auf der [Registerkarte Activity Tabs][ActivityTabsDemo]aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-245">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="6ac00-246">Stammaktivitäten</span><span class="sxs-lookup"><span data-stu-id="6ac00-246">Root activities</span></span>   

<span data-ttu-id="6ac00-247">Im folgenden finden Sie eine Erläuterung des Konzepts der **Stammaktivitäten** , das auf der Registerkarte " **anrufstruktur** ", " **Bottom-up-** Registerkarte" und " **Ereignisprotokoll** Abschnitte" erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="6ac00-247">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="6ac00-248">Stammaktivitäten sind solche, die dazu führen, dass der Browser einige Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="6ac00-248">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="6ac00-249">Wenn Sie beispielsweise auf eine Seite klicken, löst der Browser eine `Event` Aktivität als Stammaktivität aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-249">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="6ac00-250">, Die `Event` dazu führen können, dass ein Handler ausgeführt wird usw.</span><span class="sxs-lookup"><span data-stu-id="6ac00-250">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="6ac00-251">Im Flammen Diagramm des **Haupt** Abschnitts befinden sich die Stammaktivitäten am oberen Rand des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="6ac00-251">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="6ac00-252">In den Registerkarten " **anrufstruktur** " und " **Ereignisprotokoll** " sind Stammaktivitäten die Elemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ac00-252">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="6ac00-253">Ein Beispiel für Stammaktivitäten finden Sie auf [der Registerkarte anrufstruktur](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="6ac00-253">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="6ac00-254">Die Registerkarte "anrufstruktur"</span><span class="sxs-lookup"><span data-stu-id="6ac00-254">The Call Tree tab</span></span>   

<span data-ttu-id="6ac00-255">Verwenden Sie die Registerkarte **anrufstruktur** , um anzuzeigen, welche [Stammaktivitäten](#root-activities) die meiste Arbeit verursachen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-255">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="6ac00-256">Die Registerkarte " **anrufstruktur** " zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-256">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ac00-257">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="6ac00-257">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Die Registerkarte "anrufstruktur"" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="6ac00-259">Die Registerkarte " **anrufstruktur** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-259">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-260">In der vorhergehenden Abbildung sind die Elemente der obersten Ebene in der Spalte **Aktivität** , beispielsweise `Evaluate Script` und Stammaktivitäten, zu finden `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-260">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="6ac00-261">Die Schachtelung stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="6ac00-261">The nesting represents the call stack.</span></span>  <span data-ttu-id="6ac00-262">Beispielsweise in der vorherigen Abbildung, die `Parse HTML` verursacht hat, `Evaluate Script` `Compile Script` und `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-262">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="6ac00-263">**Self time** steht für die in dieser Aktivität direkt verbrachte Zeit.</span><span class="sxs-lookup"><span data-stu-id="6ac00-263">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="6ac00-264">**Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-264">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="6ac00-265">Klicken Sie auf **selbst Zeit**, **Gesamtzeit**oder **Aktivität** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-265">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="6ac00-266">Verwenden Sie das Textfeld **Filtern** , um Ereignisse nach Aktivitätsname zu filtern.</span><span class="sxs-lookup"><span data-stu-id="6ac00-266">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="6ac00-267">Standardmäßig ist das Menü **Gruppierung** auf **keine Gruppierung**eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-267">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="6ac00-268">Verwenden Sie das Menü **Gruppierung** , um die aktivitätstabelle auf der Grundlage verschiedener Kriterien zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-268">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="6ac00-269">Klicken Sie auf **schwersten Stapel anzeigen** \ ( ![ schwersten Stapel anzeigen ][ImageShowHeaviestStackIcon] \), um eine andere Tabelle rechts neben der **Aktivitäts** Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-269">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="6ac00-270">Klicken Sie auf eine Aktivität, um die **schwerste Stapel** Tabelle aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-270">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="6ac00-271">Die **schwerste Stapel** Tabelle zeigt, welche untergeordneten Elemente der ausgewählten Aktivität am längsten ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-271">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="6ac00-272">Die Registerkarte "Bottom-up"</span><span class="sxs-lookup"><span data-stu-id="6ac00-272">The Bottom-Up tab</span></span>   

<span data-ttu-id="6ac00-273">Verwenden Sie die Registerkarte " **Bottom-up** ", um anzuzeigen, welche Aktivitäten die meiste Zeit im Aggregat Direktaufnahmen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-273">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="6ac00-274">Auf der Registerkarte **Bottom-up** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-274">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ac00-275">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="6ac00-275">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Die Registerkarte "Bottom-up"" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="6ac00-277">Die Registerkarte " **Bottom-up** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-277">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-278">Im **Haupt** Abschnitt Flammen Diagramm der vorhergehenden Abbildung ist zu sehen, dass fast die ganze Zeit ausgeführt wurde `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-278">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="6ac00-279">Die oberste Aktivität auf der Registerkarte " **Bottom-up** " der vorherigen Abbildung ist `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-279">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="6ac00-280">Informationen dazu finden Sie auf der Registerkarte " **Bottom-up** " `Layout` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-280">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="6ac00-281">Die Spalte **selbst Zeit** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität für alle Vorkommen aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-281">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="6ac00-282">Die Spalte " **Gesamtzeit** " stellt die aggregierte Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-282">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="6ac00-283">Die Registerkarte "Ereignisprotokoll"</span><span class="sxs-lookup"><span data-stu-id="6ac00-283">The Event Log tab</span></span>   

<span data-ttu-id="6ac00-284">Verwenden Sie die Registerkarte **Ereignisprotokoll** , um Aktivitäten in der Reihenfolge anzuzeigen, in der Sie während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-284">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="6ac00-285">Die Registerkarte **Ereignisprotokoll** zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-285">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ac00-286">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="6ac00-286">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Die Registerkarte "Ereignisprotokoll"" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="6ac00-288">Die Registerkarte " **Ereignisprotokoll** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-288">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-289">Die Spalte **Anfangszeit** steht für den Punkt, an dem die Aktivität gestartet wurde, relativ zum Anfang der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="6ac00-289">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="6ac00-290">Beispielsweise bedeutet die Startzeit `175.7 ms` für das ausgewählte Element in der vorherigen Abbildung, dass die Aktivität nach Beginn der Aufzeichnung 175,7 ms gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="6ac00-290">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="6ac00-291">Die Spalte **selbst Zeit** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-291">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="6ac00-292">Die Spalten **Gesamtzeit** stellt die Zeit dar, die direkt in dieser Aktivität oder in einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-292">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="6ac00-293">Klicken Sie auf **Startzeit**, **selbst Zeit**oder **Gesamtzeit** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-293">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="6ac00-294">Verwenden Sie das Textfeld **Filtern** , um Aktivitäten nach Namen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="6ac00-294">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="6ac00-295">Verwenden Sie das Menü " **Dauer** ", um alle Aktivitäten zu filtern, die weniger als 1 MS oder 15 MS dauerte.</span><span class="sxs-lookup"><span data-stu-id="6ac00-295">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="6ac00-296">Standardmäßig ist das Menü **Dauer** auf **alle**eingestellt, was bedeutet, dass alle Aktivitäten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-296">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="6ac00-297">Deaktivieren Sie die Kontrollkästchen **Lade**-, **Skripting**-, **Rendering**-oder **Painting** , um alle Aktivitäten aus diesen Kategorien zu filtern.</span><span class="sxs-lookup"><span data-stu-id="6ac00-297">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="6ac00-298">Anzeigen der GPU-Aktivität</span><span class="sxs-lookup"><span data-stu-id="6ac00-298">View GPU activity</span></span>   

<span data-ttu-id="6ac00-299">Zeigen Sie die GPU-Aktivität im Abschnitt **GPU** an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-299">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Der GPU-Abschnitt" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="6ac00-301">Der **GPU** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6ac00-301">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-302">Raster Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac00-302">View raster activity</span></span>   

<span data-ttu-id="6ac00-303">Raster Aktivitäten im **Raster** Abschnitt anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac00-303">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Der Raster Abschnitt" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="6ac00-305">Der **Raster** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6ac00-305">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-306">Anzeigen von Interaktionen</span><span class="sxs-lookup"><span data-stu-id="6ac00-306">View interactions</span></span>   

<span data-ttu-id="6ac00-307">Verwenden Sie den Abschnitt **Interaktionen** , um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-307">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Abschnitt "Interaktionen"" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="6ac00-309">Abschnitt " **Interaktionen** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-309">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-310">Eine rote Zeile am unteren Rand einer Interaktion stellt die Zeit dar, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="6ac00-310">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="6ac00-311">Klicken Sie auf eine Interaktion, um weitere Informationen dazu auf der Registerkarte **Zusammenfassung** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-311">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="6ac00-312">Analysieren von Frames pro Sekunde (fps)</span><span class="sxs-lookup"><span data-stu-id="6ac00-312">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="6ac00-313">DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:</span><span class="sxs-lookup"><span data-stu-id="6ac00-313">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="6ac00-314">Verwenden Sie [das FPS-Diagramm](#the-fps-chart) , um einen Überblick über fps über die Dauer der Aufzeichnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-314">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="6ac00-315">Verwenden Sie [den Abschnitt Frames](#the-frames-section) , um anzuzeigen, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-315">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="6ac00-316">Verwenden Sie das **fps-Messgerät** für eine echt Zeitschätzung von fps während der Ausführung der Seite.</span><span class="sxs-lookup"><span data-stu-id="6ac00-316">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6ac00-317">Informationen dazu finden Sie unter [Anzeigen von Frames pro Sekunde in Echtzeit mit dem FPS-Meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="6ac00-317">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="6ac00-318">Das fps-Diagramm</span><span class="sxs-lookup"><span data-stu-id="6ac00-318">The FPS chart</span></span>   

<span data-ttu-id="6ac00-319">Das **fps** -Diagramm bietet eine Übersicht über die Framerate für die Dauer einer Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="6ac00-319">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="6ac00-320">Je höher die grüne Leiste, desto besser die Framerate.</span><span class="sxs-lookup"><span data-stu-id="6ac00-320">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="6ac00-321">Eine rote Leiste oberhalb des **fps** -Diagramms ist eine Warnung, dass die Framerate so gering war, dass Sie möglicherweise die Benutzererfahrung beeinträchtigte.</span><span class="sxs-lookup"><span data-stu-id="6ac00-321">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Das fps-Diagramm" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="6ac00-323">Das **fps** -Diagramm</span><span class="sxs-lookup"><span data-stu-id="6ac00-323">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="6ac00-324">Der Abschnitt "Frames"</span><span class="sxs-lookup"><span data-stu-id="6ac00-324">The Frames section</span></span>   

<span data-ttu-id="6ac00-325">Im Abschnitt **Frames** erfahren Sie genau, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac00-325">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="6ac00-326">Zeigen Sie mit der Maus auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-326">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Zeigen Sie mit der Maus auf einen Frame" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="6ac00-328">Zeigen Sie mit der Maus auf einen Frame</span><span class="sxs-lookup"><span data-stu-id="6ac00-328">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-329">Klicken Sie auf einen Frame, um auf der Registerkarte **Zusammenfassung** noch weitere Informationen zu dem Frame anzuzeigen.  DevTools konturiert den markierten Frame in blau.</span><span class="sxs-lookup"><span data-stu-id="6ac00-329">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Anzeigen eines Frames auf der Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="6ac00-331">Anzeigen eines Frames auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-331">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-332">Anzeigen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="6ac00-332">View network requests</span></span>   

<span data-ttu-id="6ac00-333">Erweitern Sie den Abschnitt **Netzwerk** , um einen Wasserfall von Netzwerkanforderungen anzuzeigen, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ac00-333">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Der Abschnitt "Netzwerk"" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="6ac00-335">Der Abschnitt " **Netzwerk** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-335">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-336">Anforderungen werden wie folgt farblich gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="6ac00-336">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="6ac00-337">HTML: blau</span><span class="sxs-lookup"><span data-stu-id="6ac00-337">HTML: Blue</span></span>  
*   <span data-ttu-id="6ac00-338">CSS: lila</span><span class="sxs-lookup"><span data-stu-id="6ac00-338">CSS: Purple</span></span>  
*   <span data-ttu-id="6ac00-339">JS: gelb</span><span class="sxs-lookup"><span data-stu-id="6ac00-339">JS: Yellow</span></span>  
*   <span data-ttu-id="6ac00-340">Bilder: grün</span><span class="sxs-lookup"><span data-stu-id="6ac00-340">Images: Green</span></span>  
    
<span data-ttu-id="6ac00-341">Klicken Sie auf eine Anfrage, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  In der vorhergehenden Abbildung werden beispielsweise auf der Registerkarte **Zusammenfassung** Weitere Informationen zu der im Abschnitt **Netzwerk** ausgewählten blauen Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-341">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="6ac00-342">Ein dunkelblaues Quadrat in der oberen linken Ecke einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-342">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="6ac00-343">Ein helleres blaues Quadrat bedeutet niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="6ac00-343">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="6ac00-344">In der vorhergehenden Abbildung ist beispielsweise die blaue, ausgewählte Anforderung eine höhere Priorität, und die grüne darunter hat eine niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="6ac00-344">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="6ac00-345">In der ersten der folgenden Zahlen wird die Anforderung für `www.bing.com` durch eine Zeile auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Teil und einem hellen Teil sowie eine Zeile auf der rechten Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-345">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="6ac00-346">In der zweiten der folgenden Abbildungen wird die entsprechende Darstellung der gleichen Anforderung auf der Registerkarte **Anzeige** Dauer im **Netzwerk** Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-346">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="6ac00-347">Hier sehen Sie, wie diese beiden Darstellungen einander zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="6ac00-347">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="6ac00-348">Die linke Zeile ist alles bis zur `Connection Start` Gruppe von Ereignissen inklusive.</span><span class="sxs-lookup"><span data-stu-id="6ac00-348">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="6ac00-349">Mit anderen Worten: Es ist alles vor `Request Sent` , exklusiv.</span><span class="sxs-lookup"><span data-stu-id="6ac00-349">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="6ac00-350">Der helle Bereich der Leiste ist `Request Sent` und `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-350">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="6ac00-351">Der dunkle Teil der Leiste ist `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-351">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="6ac00-352">Die richtige Zeile ist im Wesentlichen die Zeit, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="6ac00-352">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="6ac00-353">Diese wird auf der Registerkarte **Anzeige** Dauer nicht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-353">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Die Zeile-Balken-Darstellung der www.Bing.com-Anforderung" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="6ac00-355">Die Zeile-Balken-Darstellung der `www.bing.com` Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ac00-355">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Der Abschnitt "Netzwerk"" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="6ac00-357">Der Abschnitt " **Netzwerk** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-357">The **Network** section</span></span>  
<span data-ttu-id="6ac00-358">::: Image-End:::</span><span class="sxs-lookup"><span data-stu-id="6ac00-358">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6ac00-359">Anzeigen von Speicher Metriken</span><span class="sxs-lookup"><span data-stu-id="6ac00-359">View memory metrics</span></span>   

<span data-ttu-id="6ac00-360">Aktivieren Sie das Kontrollkästchen **Speicher** , um Speicher Metriken aus der letzten Aufzeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-360">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Das Kontrollkästchen "Speicher"" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="6ac00-362">Das Kontrollkästchen " **Speicher** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-362">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-363">DevTools zeigt ein neues **Speicher** Diagramm über der Registerkarte " **Zusammenfassung** " an.  Es gibt auch ein neues Diagramm unter dem **Netz** Diagramm, das als **Heap**bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6ac00-363">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="6ac00-364">Das **Heap** Diagramm bietet dieselben Informationen wie die **js-heaplinie** im **Speicher** Diagramm.</span><span class="sxs-lookup"><span data-stu-id="6ac00-364">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Speicher Metriken" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="6ac00-366">Speicher Metriken</span><span class="sxs-lookup"><span data-stu-id="6ac00-366">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-367">Die farbigen Linien auf dem Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ac00-367">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="6ac00-368">Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie aus dem Diagramm auszublenden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-368">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="6ac00-369">Das Diagramm zeigt nur den Bereich der Aufzeichnung an, der aktuell markiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ac00-369">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="6ac00-370">In der vorhergehenden Abbildung zeigt das **Speicher** Diagramm beispielsweise nur die Speicherauslastung von der 400 MS-Marke bis zum 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="6ac00-370">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="6ac00-371">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-371">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="6ac00-372">Wenn Sie einen Abschnitt wie " **Netzwerk** " oder " **Main**" analysieren, benötigen Sie manchmal eine genauere Einschätzung, wie lange bestimmte Ereignisse dauerte.</span><span class="sxs-lookup"><span data-stu-id="6ac00-372">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="6ac00-373">Halten `Shift` , klicken und halten Sie, und ziehen Sie nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-373">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="6ac00-374">Am unteren Rand Ihrer Auswahl zeigt devtools an, wie lange dieser Teil dauerte.</span><span class="sxs-lookup"><span data-stu-id="6ac00-374">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Anzeigen der Dauer eines Teils einer Aufzeichnung" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="6ac00-376">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6ac00-376">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-377">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="6ac00-377">View a screenshot</span></span>   

<span data-ttu-id="6ac00-378">Informationen zum Aktivieren von Screenshots finden Sie unter [Aufzeichnen von Screenshots während der Aufzeichnung](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="6ac00-378">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="6ac00-379">Zeigen Sie mit der Maus auf die **Übersicht** , um einen Screenshot zu sehen, wie die Seite während dieses Moments der Aufzeichnung aussah.</span><span class="sxs-lookup"><span data-stu-id="6ac00-379">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="6ac00-380">Die **Übersicht** ist der Abschnitt mit den Diagrammen **CPU**, **fps**und **net** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-380">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Anzeigen eines Screenshots" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="6ac00-382">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="6ac00-382">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-383">Sie können Screenshots auch anzeigen, indem Sie im Abschnitt **Frames** auf einen Frame klicken.</span><span class="sxs-lookup"><span data-stu-id="6ac00-383">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="6ac00-384">DevTools zeigt eine kleine Version des Screenshots auf der Registerkarte " **Zusammenfassung** " an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-384">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Anzeigen eines Screenshots auf der Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="6ac00-386">Anzeigen eines Screenshots auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-386">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-387">Klicken Sie auf der Registerkarte **Zusammenfassung** auf die Miniaturansicht, um den Screenshot zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="6ac00-387">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Vergrößern eines Screenshots über die Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="6ac00-389">Vergrößern eines Screenshots über die Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-389">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6ac00-390">Informationen zu Layern anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac00-390">View layers information</span></span>   

<span data-ttu-id="6ac00-391">So zeigen Sie erweiterte Folieninformationen zu einem Frame an:</span><span class="sxs-lookup"><span data-stu-id="6ac00-391">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="6ac00-392">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="6ac00-392">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6ac00-393">Wählen Sie im Abschnitt **Frames** einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-393">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="6ac00-394">DevTools zeigt Informationen zu den Ebenen auf der Registerkarte "neue **Ebenen** " neben der Registerkarte " **Ereignisprotokoll** " an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-394">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Der Bereich "Ebenen"" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="6ac00-396">Der Bereich " **Ebenen** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-396">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6ac00-397">Zeigen Sie mit der Maus auf eine Ebene, um Sie im Diagramm hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="6ac00-397">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Markieren eines Layers" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="6ac00-399">Markieren eines Layers</span><span class="sxs-lookup"><span data-stu-id="6ac00-399">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="6ac00-400">So verschieben Sie das Diagramm:</span><span class="sxs-lookup"><span data-stu-id="6ac00-400">To move the diagram:</span></span>  

*   <span data-ttu-id="6ac00-401">Klicken Sie auf **Schwenkmodus** \ ( ![ Schwenkmodus ][ImagePanModeIcon] \), um entlang der X-und Y-Achse zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-401">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="6ac00-402">Klicken Sie auf **Drehungsmodus** \ ( ![ Rotationsmodus ][ImageRotateModeIcon] \), um sich entlang der Z-Achse zu drehen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-402">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="6ac00-403">Klicken Sie auf **Transform zurücksetzen** \ ( ![ Transform zurücksetzen ][ImageResetTransformIcon] \), um das Diagramm auf die ursprüngliche Position zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-403">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="6ac00-404">Anzeigen des Paint-Profilers</span><span class="sxs-lookup"><span data-stu-id="6ac00-404">View paint profiler</span></span>   

<span data-ttu-id="6ac00-405">So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:</span><span class="sxs-lookup"><span data-stu-id="6ac00-405">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="6ac00-406">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="6ac00-406">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6ac00-407">Wählen Sie im **Haupt** Abschnitt ein **Paint** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="6ac00-407">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Die Registerkarte "Paint-Profiler"" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="6ac00-409">Die Registerkarte " **Paint-Profiler** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-409">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6ac00-410">Analysieren der Renderingleistung mit der Registerkarte "Rendern"</span><span class="sxs-lookup"><span data-stu-id="6ac00-410">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="6ac00-411">Verwenden Sie die Features der Registerkarte " **Rendern** ", um die Renderingleistung Ihrer Seite zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="6ac00-411">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="6ac00-412">So öffnen Sie die Registerkarte " **Rendering** ":</span><span class="sxs-lookup"><span data-stu-id="6ac00-412">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="6ac00-413">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="6ac00-413">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="6ac00-414">Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="6ac00-414">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="6ac00-415">DevTools zeigt die Registerkarte " **Rendering** " am unteren Rand des devtools-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="6ac00-415">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Die Registerkarte "Rendern"" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="6ac00-417">Die Registerkarte " **Rendern** "</span><span class="sxs-lookup"><span data-stu-id="6ac00-417">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6ac00-418">Anzeigen von Frames pro Sekunde in Echtzeit mit dem fps-Messgerät</span><span class="sxs-lookup"><span data-stu-id="6ac00-418">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="6ac00-419">Das **fps-Messgerät** ist ein Overlay, das in der oberen rechten Ecke des Viewports angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ac00-419">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="6ac00-420">Bei der Ausführung der Seite wird eine Echtzeit-Schätzung von fps bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-420">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6ac00-421">So öffnen Sie das **fps-Messgerät**:</span><span class="sxs-lookup"><span data-stu-id="6ac00-421">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="6ac00-422">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-422">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ac00-423">Aktivieren Sie das Kontrollkästchen **FPS-Meter** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-423">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Das fps-Messgerät" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="6ac00-425">Das **fps-Messgerät**</span><span class="sxs-lookup"><span data-stu-id="6ac00-425">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6ac00-426">Anzeigen von Zeichnungs Ereignissen in Echtzeit mit Farb blinken</span><span class="sxs-lookup"><span data-stu-id="6ac00-426">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="6ac00-427">Verwenden Sie das Farb blinken, um eine Echtzeitansicht aller Paint-Ereignisse auf der Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ac00-427">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="6ac00-428">Jedes Mal, wenn ein Teil der Seite neu gestrichen wird, wird der Abschnitt in devtools in grün umrissen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-428">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="6ac00-429">So aktivieren Sie die Farb Blinkfunktion:</span><span class="sxs-lookup"><span data-stu-id="6ac00-429">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="6ac00-430">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-430">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ac00-431">Aktivieren Sie das Kontrollkästchen " **Farbe blinkt** ".</span><span class="sxs-lookup"><span data-stu-id="6ac00-431">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Malen blinkt" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="6ac00-433">Malen blinkt</span><span class="sxs-lookup"><span data-stu-id="6ac00-433">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="6ac00-434">Anzeigen einer Überlagerung von Ebenen mit Ebenen Rändern</span><span class="sxs-lookup"><span data-stu-id="6ac00-434">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="6ac00-435">Verwenden Sie **Layer-Rahmen** , um eine Überlagerung von Layer-Rändern und Kacheln oben auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ac00-435">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="6ac00-436">So aktivieren Sie Layer-Rahmen:</span><span class="sxs-lookup"><span data-stu-id="6ac00-436">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="6ac00-437">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-437">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ac00-438">Aktivieren Sie das Kontrollkästchen **Layer-Rahmen** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-438">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Folienrahmen" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="6ac00-440">Folienrahmen</span><span class="sxs-lookup"><span data-stu-id="6ac00-440">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6ac00-441">[`debug_colors.cc`][ChromiumDebugColors]Eine Erläuterung der Farbcodierungen finden Sie in den Kommentaren in.</span><span class="sxs-lookup"><span data-stu-id="6ac00-441">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="6ac00-442">Suchen von Scroll-Leistungsproblemen in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="6ac00-442">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="6ac00-443">Verwenden Sie Leistungsprobleme beim Scrollen, um Elemente der Seite zu identifizieren, die Ereignislistener in Bezug auf den Bildlauf aufweisen, die die Leistung der Seite beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="6ac00-443">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="6ac00-444">DevTools beschreibt die potenziell problematischen Elemente in Teal.</span><span class="sxs-lookup"><span data-stu-id="6ac00-444">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="6ac00-445">So zeigen Sie Bild Lauf Leistungsprobleme an:</span><span class="sxs-lookup"><span data-stu-id="6ac00-445">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="6ac00-446">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ac00-446">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ac00-447">Aktivieren Sie das Kontrollkästchen **Scrolling Performance Issues** .</span><span class="sxs-lookup"><span data-stu-id="6ac00-447">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Probleme mit der Bildlaufleistung deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können." lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="6ac00-449">**Probleme mit der Bildlaufleistung** deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="6ac00-449">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
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
> <span data-ttu-id="6ac00-455">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ac00-455">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6ac00-456">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6ac00-456">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6ac00-458">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ac00-458">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
