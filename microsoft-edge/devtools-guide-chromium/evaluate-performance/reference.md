---
description: Ein Verweis auf alle Möglichkeiten zum Aufzeichnen und Analysieren der Leistung in Microsoft Edge DevTools.
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 181bc05fffbaef6a06bebcc5cb9ccfcc8e7de498
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398805"
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

# <a name="performance-analysis-reference"></a><span data-ttu-id="361e9-104">Referenz zur Leistungsanalyse</span><span class="sxs-lookup"><span data-stu-id="361e9-104">Performance analysis reference</span></span>  

<span data-ttu-id="361e9-105">Diese Seite ist eine umfassende Referenz zu Microsoft Edge DevTools-Features im Zusammenhang mit der Leistungsanalyse.</span><span class="sxs-lookup"><span data-stu-id="361e9-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="361e9-106">Navigieren Sie [zu Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] für ein geführtes Lernprogramm zum Analysieren der Leistung einer Seite mithilfe von Microsoft Edge [DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="361e9-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="record-performance"></a><span data-ttu-id="361e9-107">Aufzeichnen der Leistung</span><span class="sxs-lookup"><span data-stu-id="361e9-107">Record performance</span></span>  

### <a name="record-runtime-performance"></a><span data-ttu-id="361e9-108">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="361e9-108">Record runtime performance</span></span>  

<span data-ttu-id="361e9-109">Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, statt zu laden.</span><span class="sxs-lookup"><span data-stu-id="361e9-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="361e9-110">Navigieren Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="361e9-110">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="361e9-111">Öffnen Sie **das Tool Leistung** in DevTools.</span><span class="sxs-lookup"><span data-stu-id="361e9-111">Open the **Performance** tool in DevTools.</span></span>  
1.  <span data-ttu-id="361e9-112">Wählen **Sie Datensatz** \( ![ Datensatzsymbol ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="361e9-112">Choose **Record** \(![Record icon][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="361e9-114">Record</span><span class="sxs-lookup"><span data-stu-id="361e9-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="361e9-115">Interagieren mit der Seite.</span><span class="sxs-lookup"><span data-stu-id="361e9-115">Interact with the page.</span></span>  <span data-ttu-id="361e9-116">DevTools zeichnet alle Seitenaktivitäten auf, die als Ergebnis Ihrer Interaktionen auftreten.</span><span class="sxs-lookup"><span data-stu-id="361e9-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="361e9-117">Wählen **Sie erneut Aufzeichnen** aus, oder wählen Sie Beenden **aus,** um die Aufzeichnung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="361e9-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <a name="record-load-performance"></a><span data-ttu-id="361e9-118">Aufzeichnen der Lastleistung</span><span class="sxs-lookup"><span data-stu-id="361e9-118">Record load performance</span></span>  

<span data-ttu-id="361e9-119">Zeichnen Sie die Lastleistung auf, wenn Sie die Leistung einer Seite beim Laden analysieren möchten, statt sie zu ausführen.</span><span class="sxs-lookup"><span data-stu-id="361e9-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="361e9-120">Navigieren Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="361e9-120">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="361e9-121">Öffnen Sie **den Bereich** Leistung von DevTools.</span><span class="sxs-lookup"><span data-stu-id="361e9-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="361e9-122">Wählen **Sie Seite aktualisieren** \( Seite aktualisieren ![ ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="361e9-122">Choose **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="361e9-123">DevTools zeichnet Leistungsmetriken auf, während die Seite aktualisiert wird, und beendet dann die Aufzeichnung ein paar Sekunden nach Abschluss der Last automatisch.</span><span class="sxs-lookup"><span data-stu-id="361e9-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Seite aktualisieren" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="361e9-125">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="361e9-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="361e9-126">DevTools vergrößert automatisch den Teil der Aufzeichnung, in dem der Großteil der Aktivität aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="361e9-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Eine Aufzeichnung zum Laden von Seiten" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="361e9-128">Eine Aufzeichnung zum Laden von Seiten</span><span class="sxs-lookup"><span data-stu-id="361e9-128">A page-load recording</span></span>  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a><span data-ttu-id="361e9-129">Aufnehmen von Screenshots während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="361e9-130">Aktivieren Sie das **Kontrollkästchen Screenshots,** um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="361e9-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Das Kontrollkästchen Screenshots" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="361e9-132">Das **Kontrollkästchen Screenshots**</span><span class="sxs-lookup"><span data-stu-id="361e9-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-133">Navigieren Sie zu [Screenshot anzeigen,](#view-a-screenshot) um zu erfahren, wie Sie mit Screenshots interagieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <a name="force-garbage-collection-while-recording"></a><span data-ttu-id="361e9-134">Erzwingen der Garbage Collection während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="361e9-135">Wählen Sie beim Aufzeichnen einer Seite die Option Garbage **sammeln** \( Garbage Icon sammeln \) aus, ![ um die Garbage Collection zu ][ImageCollectGarbageIcon] erzwingen.</span><span class="sxs-lookup"><span data-stu-id="361e9-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Sammeln von Garbage" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="361e9-137">Sammeln von Garbage</span><span class="sxs-lookup"><span data-stu-id="361e9-137">Collect garbage</span></span>  
:::image-end:::  

### <a name="show-recording-settings"></a><span data-ttu-id="361e9-138">Anzeigen von Aufzeichnungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="361e9-138">Show recording settings</span></span>  

<span data-ttu-id="361e9-139">Wählen **Sie Aufnahmeeinstellungen** \( Aufnahmeeinstellungen \) aus, um weitere Einstellungen im Zusammenhang mit der Erfassung von Leistungsaufzeichnungen durch ![ ][ImageCaptureSettingsIcon] DevTools verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="361e9-139">Choose **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Abschnitt "Aufnahmeeinstellungen"" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="361e9-141">Abschnitt **"Aufnahmeeinstellungen"**</span><span class="sxs-lookup"><span data-stu-id="361e9-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <a name="disable-javascript-samples"></a><span data-ttu-id="361e9-142">Deaktivieren von JavaScript-Beispielen</span><span class="sxs-lookup"><span data-stu-id="361e9-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="361e9-143">Standardmäßig werden im **Hauptabschnitt** einer Aufzeichnung detaillierte Aufrufstapel von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="361e9-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="361e9-144">So deaktivieren Sie diese Aufrufstapel:</span><span class="sxs-lookup"><span data-stu-id="361e9-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="361e9-145">Öffnen Sie **das Menü Einstellungen erfassen.**</span><span class="sxs-lookup"><span data-stu-id="361e9-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="361e9-146">Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="361e9-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="361e9-147">Aktivieren Sie das **Kontrollkästchen JavaScript-Beispiele** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="361e9-148">Nehmen Sie eine Aufzeichnung der Seite vor.</span><span class="sxs-lookup"><span data-stu-id="361e9-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="361e9-149">Die folgenden beiden Abbildungen zeigen den Unterschied zwischen dem Deaktivieren und Aktivieren von JavaScript-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="361e9-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="361e9-150">Der **Abschnitt "Main"** der Aufzeichnung ist wesentlich kürzer, wenn das Sampling deaktiviert ist, da alle JavaScript-Aufrufstapel nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="361e9-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="361e9-152">Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="361e9-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="361e9-154">Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="361e9-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a><span data-ttu-id="361e9-155">Drosseln des Netzwerks während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-155">Throttle the network while recording</span></span>  

<span data-ttu-id="361e9-156">So drosseln Sie das Netzwerk während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="361e9-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="361e9-157">Öffnen Sie **das Menü Einstellungen erfassen.**</span><span class="sxs-lookup"><span data-stu-id="361e9-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="361e9-158">Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="361e9-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="361e9-159">Legen **Sie Netzwerk** auf die gewünschte Drosselungsstufe.</span><span class="sxs-lookup"><span data-stu-id="361e9-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <a name="throttle-the-cpu-while-recording"></a><span data-ttu-id="361e9-160">Drosseln der CPU während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="361e9-161">So drosseln Sie die CPU während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="361e9-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="361e9-162">Öffnen Sie **das Menü Einstellungen erfassen.**</span><span class="sxs-lookup"><span data-stu-id="361e9-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="361e9-163">Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="361e9-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="361e9-164">Legen **Sie die CPU** auf die gewünschte Drosselungsstufe.</span><span class="sxs-lookup"><span data-stu-id="361e9-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="361e9-165">Die Einschränkung ist relativ zu den Funktionen Ihres Computers.</span><span class="sxs-lookup"><span data-stu-id="361e9-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="361e9-166">Die **2x-Verlangsamungsoption** z. B. macht ihre CPU zwei Mal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="361e9-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="361e9-167">DevTools simulieren nicht wirklich die CPUs mobiler Geräte, da sich die Architektur mobiler Geräte stark von der architektur von Desktops und Laptops unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="361e9-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <a name="turn-on-advanced-paint-instrumentation"></a><span data-ttu-id="361e9-168">Aktivieren der erweiterten Farbinstrumentierung</span><span class="sxs-lookup"><span data-stu-id="361e9-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="361e9-169">So zeigen Sie die detaillierte Farbinstrumentierung an:</span><span class="sxs-lookup"><span data-stu-id="361e9-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="361e9-170">Öffnen Sie **das Menü Einstellungen erfassen.**</span><span class="sxs-lookup"><span data-stu-id="361e9-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="361e9-171">Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="361e9-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="361e9-172">Aktivieren Sie **das Kontrollkästchen Erweiterte Farbinstrumentierung aktivieren (langsam).**</span><span class="sxs-lookup"><span data-stu-id="361e9-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="361e9-173">Um zu erfahren, wie Sie mit den Farbinformationen interagieren, navigieren Sie zu [Ebenen anzeigen](#view-layers-information) und [Lackprofiler anzeigen.](#view-paint-profiler)</span><span class="sxs-lookup"><span data-stu-id="361e9-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <a name="save-a-recording"></a><span data-ttu-id="361e9-174">Speichern einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-174">Save a recording</span></span>  

<span data-ttu-id="361e9-175">Öffnen Sie zum Speichern einer Aufzeichnung das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie **Profil speichern aus.**</span><span class="sxs-lookup"><span data-stu-id="361e9-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Profil speichern" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="361e9-177">Profil speichern</span><span class="sxs-lookup"><span data-stu-id="361e9-177">Save Profile</span></span>**  
:::image-end:::  

## <a name="load-a-recording"></a><span data-ttu-id="361e9-178">Laden einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-178">Load a recording</span></span>  

<span data-ttu-id="361e9-179">Öffnen Sie zum Laden einer Aufzeichnung das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Profil laden aus.**</span><span class="sxs-lookup"><span data-stu-id="361e9-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Lastenprofil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="361e9-181">Lastenprofil</span><span class="sxs-lookup"><span data-stu-id="361e9-181">Load Profile</span></span>**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a><span data-ttu-id="361e9-182">Löschen der vorherigen Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-182">Clear the previous recording</span></span>  

<span data-ttu-id="361e9-183">Nachdem Sie eine Aufzeichnung gemacht haben, **wählen** Sie Aufzeichnung löschen \( Aufzeichnungssymbol löschen \) aus, um diese Aufzeichnung im ![ ][ImageClearRecordingIcon] Leistungsbereich **zu** löschen.</span><span class="sxs-lookup"><span data-stu-id="361e9-183">After making a recording, choose **Clear recording** \(![Clear recording icon][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Löschen der Aufzeichnung" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="361e9-185">Löschen der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-185">Clear recording</span></span>**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a><span data-ttu-id="361e9-186">Analysieren einer Leistungsaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-186">Analyze a performance recording</span></span>  

<span data-ttu-id="361e9-187">Nachdem Sie [die Laufzeitleistung oder](#record-runtime-performance) \*\*\*\* die Ladeleistung aufgezeichnet [haben,](#record-load-performance)stellt der Bereich Leistung eine Menge Daten für die Analyse der Leistung der gerade geschehenen Daten zur Wahl.</span><span class="sxs-lookup"><span data-stu-id="361e9-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <a name="select-a-portion-of-a-recording"></a><span data-ttu-id="361e9-188">Auswählen eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-188">Select a portion of a recording</span></span>  

<span data-ttu-id="361e9-189">Ziehen Sie die Maus nach links oder rechts über die **Übersicht,** um einen Teil einer Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="361e9-190">Der **Abschnitt Übersicht** enthält die Diagramme **FPS,** **CPU**und **NET.**</span><span class="sxs-lookup"><span data-stu-id="361e9-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Ziehen Sie die Maus über die Übersicht, um zu zoomen" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="361e9-192">Ziehen Sie die Maus über die **Übersicht,** um zu zoomen</span><span class="sxs-lookup"><span data-stu-id="361e9-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-193">So wählen Sie einen Teil mithilfe der Tastatur aus:</span><span class="sxs-lookup"><span data-stu-id="361e9-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="361e9-194">Wählen Sie den Hintergrund des **Abschnitts Main** oder einen der abschnitte daneben aus, z. B. **Interaktionen,** **Netzwerk**oder **GPU**.</span><span class="sxs-lookup"><span data-stu-id="361e9-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="361e9-195">Dieser Tastaturworkflow funktioniert nur, wenn sich einer dieser Abschnitte im Fokus befindet.</span><span class="sxs-lookup"><span data-stu-id="361e9-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="361e9-196">Verwenden Sie die Tasten , , , um `W` `A` zu `S` zoomen, nach links zu verschieben, zu verkleinern und nach rechts `D` zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="361e9-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="361e9-197">Führen Sie die folgenden Aktionen aus, um einen Teil mithilfe eines Trackpads auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="361e9-198">Zeigen Sie mit der Maus auf den **Abschnitt Übersicht** oder den **Abschnitt Details.**</span><span class="sxs-lookup"><span data-stu-id="361e9-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="361e9-199">Der **Abschnitt Übersicht** ist der Bereich, der die **FPS-,** **CPU-** und **#A0** enthält.</span><span class="sxs-lookup"><span data-stu-id="361e9-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="361e9-200">Der **Abschnitt Details** ist der Bereich, der den Abschnitt **Main,** den Abschnitt **Interaktionen** und so weiter enthält.</span><span class="sxs-lookup"><span data-stu-id="361e9-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="361e9-201">Wischen Sie mit zwei Fingern nach oben, um sie zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="361e9-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="361e9-202">Wenn Sie ein langes Flammendiagramm im **Abschnitt "Main"** oder einen der Benachbarten scrollen möchten, wählen Sie beim Ziehen nach oben und unten die Option und halten sie gedrückt.</span><span class="sxs-lookup"><span data-stu-id="361e9-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="361e9-203">Ziehen Sie nach links und rechts, um den ausgewählten Teil der Aufzeichnung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="361e9-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <a name="search-activities"></a><span data-ttu-id="361e9-204">Suchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="361e9-204">Search activities</span></span>  

<span data-ttu-id="361e9-205">Wählen `Control` + `F` Sie \(Windows, Linux\) oder `Command` + `F` \(macOS\) \*\*\*\* aus, um das Suchfeld am unteren Rand des Leistungsbereichs zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="361e9-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Suchfeld" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="361e9-207">Suchfeld</span><span class="sxs-lookup"><span data-stu-id="361e9-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-208">So navigieren Sie zu Aktivitäten, die mit Ihrer Abfrage übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="361e9-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="361e9-209">Verwenden Sie **die Schaltflächen** Previous \( ![ Previous ][ImagePreviousIcon] \) und **Next** \( ![ Next ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="361e9-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="361e9-210">Wählen `Shift` + `Enter` Sie diese Option aus, um den `Enter` vorherigen oder den nächsten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="361e9-211">So ändern Sie Abfrageeinstellungen:</span><span class="sxs-lookup"><span data-stu-id="361e9-211">To modify query settings:</span></span>  

*   <span data-ttu-id="361e9-212">Wählen **Sie Zwischen- und** ![ Kleinschreibung \( Zwischenfall ][ImageSearchCaseIcon] und \) aus, um die Abfragefalle vertraulich zu machen.</span><span class="sxs-lookup"><span data-stu-id="361e9-212">Choose **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="361e9-213">Wählen **Sie Regex** \( ![ Regex ][ImageSearchRegexIcon] \) aus, um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="361e9-213">Choose **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="361e9-214">Wählen Sie Abbrechen aus, um das Suchfeld **auszublenden.**</span><span class="sxs-lookup"><span data-stu-id="361e9-214">To hide the search box, choose **Cancel**.</span></span>  

### <a name="view-main-thread-activity"></a><span data-ttu-id="361e9-215">Anzeigen der Hauptthreadaktivität</span><span class="sxs-lookup"><span data-stu-id="361e9-215">View main thread activity</span></span>  

<span data-ttu-id="361e9-216">Verwenden Sie **den Abschnitt Main,** um Aktivitäten im Hauptthread der Seite zu anzeigen.</span><span class="sxs-lookup"><span data-stu-id="361e9-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Der Abschnitt "Main"" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="361e9-218">Der **Abschnitt "Main"**</span><span class="sxs-lookup"><span data-stu-id="361e9-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-219">Wählen Sie ein Ereignis aus, um weitere Informationen zu diesem Ereignis im **Zusammenfassungsfenster anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="361e9-219">Choose an event to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="361e9-220">DevTools umreißt das ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="361e9-220">DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Weitere Informationen zur anonymen Funktion im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="361e9-222">Weitere Informationen zur `anonymous` Funktion im **Zusammenfassungsfenster**</span><span class="sxs-lookup"><span data-stu-id="361e9-222">More information about the `anonymous` function in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-223">DevTools stellt die Hauptthreadaktivität mit einem Flammendiagramm dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-223">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="361e9-224">Die x-Achse stellt die Aufzeichnung im Laufe der Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-224">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="361e9-225">Die y-Achse stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-225">The y-axis represents the call stack.</span></span>  <span data-ttu-id="361e9-226">Die Ereignisse oben verursachen die Ereignisse darunter.</span><span class="sxs-lookup"><span data-stu-id="361e9-226">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Ein Flammendiagramm" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="361e9-228">Ein Flammendiagramm</span><span class="sxs-lookup"><span data-stu-id="361e9-228">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-229">In der vorherigen Abbildung hat ein `click` Ereignis ein In in zeile `Function Call` `activitytabs.js` 53 verursacht.</span><span class="sxs-lookup"><span data-stu-id="361e9-229">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="361e9-230">Überprüfen `Function Call` Sie unten, ob eine anonyme Funktion ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="361e9-230">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="361e9-231">Die anonyme Funktion angefordert `a` , die angefordert hat , die angefordert `wait` `Minor GC` hat.</span><span class="sxs-lookup"><span data-stu-id="361e9-231">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="361e9-232">DevTools weist Skripts zufällige Farben zu.</span><span class="sxs-lookup"><span data-stu-id="361e9-232">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="361e9-233">In der vorherigen Abbildung sind Funktionsanforderungen von einem Skript hellgrün gefärbt.</span><span class="sxs-lookup"><span data-stu-id="361e9-233">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="361e9-234">Anforderungen von einem anderen Skript sind gefärbtes Grau.</span><span class="sxs-lookup"><span data-stu-id="361e9-234">Requests from another script are colored beige.</span></span>  <span data-ttu-id="361e9-235">Das dunklere Gelb stellt die Skriptaktivität dar, und das violette Ereignis stellt die Renderingaktivität dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-235">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="361e9-236">Diese dunkleren gelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="361e9-236">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="361e9-237">Navigieren Sie [zu Deaktivieren von JavaScript-Beispielen,](#disable-javascript-samples) wenn Sie das detaillierte Flammendiagramm von JavaScript-Anforderungen ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="361e9-237">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="361e9-238">Wenn JS-Beispiele deaktiviert sind, werden nur Ereignisse auf hoher Ebene wie und aus der `Event: choose` `Function Call` vorherigen Abbildung `str` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-238">When JS samples are disabled, only high-level events such as `Event: choose` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <a name="view-activities-in-a-table"></a><span data-ttu-id="361e9-239">Anzeigen von Aktivitäten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="361e9-239">View activities in a table</span></span>  

<span data-ttu-id="361e9-240">Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Abschnitt "Main"** verlassen, um Aktivitäten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-240">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="361e9-241">DevTools bietet außerdem drei Tabellenansichten für die Analyse von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="361e9-241">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="361e9-242">Jede Ansicht bietet Ihnen eine andere Perspektive für die Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="361e9-242">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="361e9-243">Wenn Sie die Stammaktivitäten anzeigen möchten, die am meisten Arbeit verursachen, verwenden Sie den [Anrufstrukturbereich.](#the-call-tree-panel)</span><span class="sxs-lookup"><span data-stu-id="361e9-243">When you want to view the root activities that cause the most work, use the [Call Tree](#the-call-tree-panel) panel.</span></span>  
*   <span data-ttu-id="361e9-244">Wenn Sie die Aktivitäten anzeigen möchten, in denen die meiste Zeit direkt verbracht wurde, verwenden Sie den [Bottom-Up-Bereich.](#the-bottom-up-panel)</span><span class="sxs-lookup"><span data-stu-id="361e9-244">When you want to view the activities where the most time was directly spent, use the [Bottom-Up](#the-bottom-up-panel) panel.</span></span>  
*   <span data-ttu-id="361e9-245">Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der sie während der Aufzeichnung aufgetreten sind, verwenden Sie den [Ereignisprotokollbereich.](#the-event-log-panel)</span><span class="sxs-lookup"><span data-stu-id="361e9-245">When you want to view the activities in the order in which they occurred during the recording, use the [Event Log](#the-event-log-panel) panel.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="361e9-246">Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.</span><span class="sxs-lookup"><span data-stu-id="361e9-246">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="361e9-247">Führen Sie die Demo selbst unter [Activity Tabs Demo aus.][ActivityTabsDemo]</span><span class="sxs-lookup"><span data-stu-id="361e9-247">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <a name="root-activities"></a><span data-ttu-id="361e9-248">Stammaktivitäten</span><span class="sxs-lookup"><span data-stu-id="361e9-248">Root activities</span></span>  

<span data-ttu-id="361e9-249">Hier finden Sie \*\*\*\* eine Erläuterung des Konzepts \*\*\*\* der Stammaktivitäten, das im Bereich Anrufstruktur, **Bottom-Up-Bereich** und **Ereignisprotokoll erwähnt** wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-249">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** panel, **Bottom-Up** panel, and **Event Log** panel.</span></span>  

<span data-ttu-id="361e9-250">Stammaktivitäten sind diejenigen, die dazu führen, dass der Browser einige Arbeit macht.</span><span class="sxs-lookup"><span data-stu-id="361e9-250">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="361e9-251">Wenn Sie beispielsweise eine Webseite auswählen, führt der Browser eine `Event` Aktivität als Stammaktivität aus.</span><span class="sxs-lookup"><span data-stu-id="361e9-251">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="361e9-252">Dies `Event` kann dazu führen, dass ein Handler ausgeführt wird, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="361e9-252">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="361e9-253">Im Flammendiagramm des **Abschnitts Main** befinden sich die Stammaktivitäten am oberen Rand des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="361e9-253">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="361e9-254">In den **Feldern Anrufstruktur** **und Ereignisprotokoll** sind Stammaktivitäten die Elemente auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="361e9-254">In the **Call Tree** and **Event Log** panels, root activities are the top-level items.</span></span>  

<span data-ttu-id="361e9-255">Navigieren Sie zum [Bereich Anrufstruktur,](#the-call-tree-panel) um ein Beispiel für Stammaktivitäten zu finden.</span><span class="sxs-lookup"><span data-stu-id="361e9-255">Navigate to the [Call Tree](#the-call-tree-panel) panel for an example of root activities.</span></span>  

#### <a name="the-call-tree-panel"></a><span data-ttu-id="361e9-256">Der Bereich "Anrufstruktur"</span><span class="sxs-lookup"><span data-stu-id="361e9-256">The Call Tree panel</span></span>  

<span data-ttu-id="361e9-257">Verwenden Sie **den Anrufstrukturbereich,** um zu sehen, [welche Stammaktivitäten](#root-activities) am meisten Arbeit verursachen.</span><span class="sxs-lookup"><span data-stu-id="361e9-257">Use the **Call Tree** panel to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="361e9-258">Im **Bereich Anrufstruktur** werden nur Aktivitäten während des ausgewählten Abschnitts der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-258">The **Call Tree** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="361e9-259">Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-259">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Der Bereich "Anrufstruktur"" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="361e9-261">Der **Bereich "Anrufstruktur"**</span><span class="sxs-lookup"><span data-stu-id="361e9-261">The **Call Tree** panel</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-262">In der vorherigen Abbildung ist die oberste Ebene der Elemente in der Spalte **Aktivität,** z. B. Und `Evaluate Script` sind `Parse HTML` Stammaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="361e9-262">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="361e9-263">Die Verschachtelung stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-263">The nesting represents the call stack.</span></span>  <span data-ttu-id="361e9-264">Beispiel: in der vorherigen Abbildung, `Parse HTML` die verursacht hat, `Evaluate Script` und `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="361e9-264">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="361e9-265">**Self Time stellt** die Zeit dar, die direkt in dieser Aktivität verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-265">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="361e9-266">**Die Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der kinder verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-266">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="361e9-267">Wählen **Sie Self Time**, Total **Time**oder **Activity** aus, um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-267">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="361e9-268">Verwenden Sie das **Textfeld Filter,** um Ereignisse nach Aktivitätsnamen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="361e9-268">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="361e9-269">Standardmäßig ist **das Menü Gruppierung** auf Keine Gruppierung **festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="361e9-269">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="361e9-270">Verwenden Sie **das Menü** Gruppierung, um die Aktivitätstabelle nach verschiedenen Kriterien zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-270">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="361e9-271">Wählen **Sie Schwerer Stapel** anzeigen \( Schwerer Stapel anzeigen \) aus, um eine weitere Tabelle rechts neben der ![ ][ImageShowHeaviestStackIcon] **Aktivitätstabelle zu** zeigen.</span><span class="sxs-lookup"><span data-stu-id="361e9-271">Choose **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="361e9-272">Wählen Sie eine Aktivität aus, um die **Tabelle "Schwerster Stapel" auffüllen** zu können.</span><span class="sxs-lookup"><span data-stu-id="361e9-272">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="361e9-273">In **der Tabelle "Schwerster Stapel"** wird angezeigt, welche Kinder der ausgewählten Aktivität am längsten ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="361e9-273">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <a name="the-bottom-up-panel"></a><span data-ttu-id="361e9-274">The Bottom-Up panel</span><span class="sxs-lookup"><span data-stu-id="361e9-274">The Bottom-Up panel</span></span>  

<span data-ttu-id="361e9-275">Verwenden Sie **den Bottom-Up-Bereich,** um zu sehen, welche Aktivitäten am häufigsten zusammengefasst verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="361e9-275">Use the **Bottom-Up** panel to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="361e9-276">Im **Bottom-Up-Bereich** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-276">The **Bottom-Up** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="361e9-277">Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-277">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="The Bottom-Up panel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="361e9-279">The **Bottom-Up** panel</span><span class="sxs-lookup"><span data-stu-id="361e9-279">The **Bottom-Up** panel</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-280">Navigieren Sie **im Diagramm Hauptabschnitt** Flammen der vorherigen Abbildung zu dem fast die ganze Zeit, die für die Ausführung auf sich `Parse HTML` hatte.</span><span class="sxs-lookup"><span data-stu-id="361e9-280">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="361e9-281">Die oberste Aktivität im **Bottom-Up-Bereich** der vorherigen Abbildung ist `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="361e9-281">The top activity in the **Bottom-Up** panel of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="361e9-282">Navigieren Sie zum **Bottom-Up-Bereich,** die nächste teuerste Aktivität ist `Layout` .</span><span class="sxs-lookup"><span data-stu-id="361e9-282">Navigate to the **Bottom-Up** panel, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="361e9-283">Die **Spalte Self Time** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität über alle Vorkommen hinweg verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-283">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="361e9-284">Die **Spalte Gesamtzeit** stellt die aggregierte Zeit dar, die in dieser Aktivität oder in einem der unterg nen Aktivitäten verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-284">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <a name="the-event-log-panel"></a><span data-ttu-id="361e9-285">Ereignisprotokollbereich</span><span class="sxs-lookup"><span data-stu-id="361e9-285">The Event Log panel</span></span>  

<span data-ttu-id="361e9-286">Verwenden Sie **den Ereignisprotokollbereich,** um Aktivitäten in der Reihenfolge zu anzeigen, in der sie während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="361e9-286">Use the **Event Log** panel to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="361e9-287">Im **Ereignisprotokollbereich** werden nur Aktivitäten während des ausgewählten Abschnitts der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-287">The **Event Log** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="361e9-288">Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-288">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Ereignisprotokollbereich" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="361e9-290">**Ereignisprotokollbereich**</span><span class="sxs-lookup"><span data-stu-id="361e9-290">The **Event Log** panel</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-291">Die **Spalte Startzeit** stellt den Zeitpunkt dar, an dem diese Aktivität gestartet wurde, relativ zum Beginn der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="361e9-291">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="361e9-292">Beispielsweise bedeutet die Startzeit für das ausgewählte Element in der vorherigen Abbildung, dass die Aktivität `175.7 ms` 175,7 ms nach Beginn der Aufzeichnung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="361e9-292">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="361e9-293">Die **Spalte Self Time** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-293">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="361e9-294">Die **Spalten Gesamtzeit** stellen die Zeit dar, die direkt in dieser Aktivität oder in einem der unterg nen Aktivitäten verbracht wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-294">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="361e9-295">Wählen **Sie Startzeit,** **Selbstzeit**oder **Gesamtzeit aus,** um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-295">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="361e9-296">Verwenden Sie das **Textfeld Filter,** um Aktivitäten nach Namen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="361e9-296">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="361e9-297">Verwenden Sie **das Menü Dauer,** um aktivitäten herausfiltern, die weniger als 1 ms oder 15 ms dauerten.</span><span class="sxs-lookup"><span data-stu-id="361e9-297">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="361e9-298">Standardmäßig ist das **Menü Dauer** auf **Alle festgelegt,** d. h. alle Aktivitäten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-298">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="361e9-299">Deaktivieren Sie **die Kontrollkästchen Laden,** \*\*\*\* **Skripten,** **Rendern**oder Malen, um alle Aktivitäten aus diesen Kategorien heraus zu filtern.</span><span class="sxs-lookup"><span data-stu-id="361e9-299">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <a name="view-gpu-activity"></a><span data-ttu-id="361e9-300">Anzeigen der GPU-Aktivität</span><span class="sxs-lookup"><span data-stu-id="361e9-300">View GPU activity</span></span>  

<span data-ttu-id="361e9-301">Anzeigen der GPU-Aktivität im **Abschnitt GPU.**</span><span class="sxs-lookup"><span data-stu-id="361e9-301">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Der Abschnitt "GPU"" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="361e9-303">Der **Abschnitt "GPU"**</span><span class="sxs-lookup"><span data-stu-id="361e9-303">The **GPU** section</span></span>  
:::image-end:::  

### <a name="view-raster-activity"></a><span data-ttu-id="361e9-304">Anzeigen der Rasteraktivität</span><span class="sxs-lookup"><span data-stu-id="361e9-304">View raster activity</span></span>  

<span data-ttu-id="361e9-305">Anzeigen der Rasteraktivität im **Abschnitt Raster.**</span><span class="sxs-lookup"><span data-stu-id="361e9-305">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Der Abschnitt Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="361e9-307">Der **Abschnitt Raster**</span><span class="sxs-lookup"><span data-stu-id="361e9-307">The **Raster** section</span></span>  
:::image-end:::  

### <a name="view-interactions"></a><span data-ttu-id="361e9-308">Anzeigen von Interaktionen</span><span class="sxs-lookup"><span data-stu-id="361e9-308">View interactions</span></span>  

<span data-ttu-id="361e9-309">Verwenden Sie **den Abschnitt Interaktionen,** um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung passiert sind.</span><span class="sxs-lookup"><span data-stu-id="361e9-309">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Der Abschnitt Interaktionen" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="361e9-311">Der **Abschnitt Interaktionen**</span><span class="sxs-lookup"><span data-stu-id="361e9-311">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-312">Eine rote Linie am unteren Rand einer Interaktion stellt die Wartezeit auf den Hauptthread dar.</span><span class="sxs-lookup"><span data-stu-id="361e9-312">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="361e9-313">Wählen Sie eine Interaktion aus, um weitere Informationen dazu im **Zusammenfassungsfenster einblenden** zu können.</span><span class="sxs-lookup"><span data-stu-id="361e9-313">Choose an interaction to view more information about it in the **Summary** panel.</span></span>  

### <a name="analyze-frames-per-second-fps"></a><span data-ttu-id="361e9-314">Analysieren von Frames pro Sekunde (FPS)</span><span class="sxs-lookup"><span data-stu-id="361e9-314">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="361e9-315">DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:</span><span class="sxs-lookup"><span data-stu-id="361e9-315">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="361e9-316">Verwenden [Sie das FPS-Diagramm,](#the-fps-chart) um eine Übersicht über FPS über die Dauer der Aufzeichnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="361e9-316">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="361e9-317">Verwenden [Sie den Abschnitt Frames,](#the-frames-section) um die Dauer eines bestimmten Frames zu sehen.</span><span class="sxs-lookup"><span data-stu-id="361e9-317">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="361e9-318">Verwenden Sie **das #A0** für eine Echtzeitschätzung von FPS, während die Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-318">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="361e9-319">Navigieren Sie [mit dem FPS-Meter zu](#view-frames-per-second-in-realtime-with-the-fps-meter)Frames pro Sekunde in Echtzeit anzeigen.</span><span class="sxs-lookup"><span data-stu-id="361e9-319">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <a name="the-fps-chart"></a><span data-ttu-id="361e9-320">Das #A0</span><span class="sxs-lookup"><span data-stu-id="361e9-320">The FPS chart</span></span>  

<span data-ttu-id="361e9-321">Das **#A0** bietet eine Übersicht über die Framerate während der Dauer einer Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="361e9-321">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="361e9-322">Im Allgemeinen gilt: Je höher der grüne Balken, desto besser ist die Framerate.</span><span class="sxs-lookup"><span data-stu-id="361e9-322">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="361e9-323">Ein roter Balken über dem **#A0** ist eine Warnung, dass die Framerate so niedrig gefallen ist, dass sie wahrscheinlich die Benutzererfahrung geschädigt hat.</span><span class="sxs-lookup"><span data-stu-id="361e9-323">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="361e9-325">Das **#A0**</span><span class="sxs-lookup"><span data-stu-id="361e9-325">The **FPS** chart</span></span>  
:::image-end:::  

#### <a name="the-frames-section"></a><span data-ttu-id="361e9-326">Der Abschnitt Frames</span><span class="sxs-lookup"><span data-stu-id="361e9-326">The Frames section</span></span>  

<span data-ttu-id="361e9-327">Im **Abschnitt Frames** erfahren Sie genau, wie lange ein bestimmter Frame ge dauern hat.</span><span class="sxs-lookup"><span data-stu-id="361e9-327">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="361e9-328">Zeigen Sie auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu zu sehen.</span><span class="sxs-lookup"><span data-stu-id="361e9-328">Hover on a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Zeigen auf einen Frame" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="361e9-330">Zeigen auf einen Frame</span><span class="sxs-lookup"><span data-stu-id="361e9-330">Hover on a frame</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-331">Wählen Sie einen Frame aus, um weitere Informationen zum Frame im **Zusammenfassungsbereich anzeigen zu** können.</span><span class="sxs-lookup"><span data-stu-id="361e9-331">Choose a frame to view more information about the frame in the **Summary** panel.</span></span>  <span data-ttu-id="361e9-332">DevTools umreißt den ausgewählten Frame in Blau.</span><span class="sxs-lookup"><span data-stu-id="361e9-332">DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Anzeigen eines Frames im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="361e9-334">Anzeigen eines Frames im **Zusammenfassungsfenster**</span><span class="sxs-lookup"><span data-stu-id="361e9-334">View a frame in the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-network-requests"></a><span data-ttu-id="361e9-335">Anzeigen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="361e9-335">View network requests</span></span>  

<span data-ttu-id="361e9-336">Erweitern Sie den **Abschnitt Netzwerk,** um einen Wasserfall mit Netzwerkanforderungen zu sehen, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="361e9-336">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Der Abschnitt "Netzwerk"" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="361e9-338">Der **Abschnitt "Netzwerk"**</span><span class="sxs-lookup"><span data-stu-id="361e9-338">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-339">Anforderungen sind wie folgt farblich codiert:</span><span class="sxs-lookup"><span data-stu-id="361e9-339">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="361e9-340">HTML: Blau</span><span class="sxs-lookup"><span data-stu-id="361e9-340">HTML: Blue</span></span>  
*   <span data-ttu-id="361e9-341">CSS: Lila</span><span class="sxs-lookup"><span data-stu-id="361e9-341">CSS: Purple</span></span>  
*   <span data-ttu-id="361e9-342">JS: Gelb</span><span class="sxs-lookup"><span data-stu-id="361e9-342">JS: Yellow</span></span>  
*   <span data-ttu-id="361e9-343">Bilder: Grün</span><span class="sxs-lookup"><span data-stu-id="361e9-343">Images: Green</span></span>  
    
<span data-ttu-id="361e9-344">Wählen Sie eine Anforderung aus, um weitere Informationen dazu im **Zusammenfassungsfenster anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="361e9-344">Choose a request to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="361e9-345">In der vorherigen Abbildung \*\*\*\* zeigt der Zusammenfassungsbereich beispielsweise weitere Informationen zur blauen Anforderung an, die im Abschnitt **Netzwerk ausgewählt** ist.</span><span class="sxs-lookup"><span data-stu-id="361e9-345">For example, in the previous figure, the **Summary** panel is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="361e9-346">Ein dunkelblaues Quadrat oben links einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.</span><span class="sxs-lookup"><span data-stu-id="361e9-346">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="361e9-347">Ein heller-blaues Quadrat bedeutet niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="361e9-347">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="361e9-348">In der vorherigen Abbildung hat die blaue, ausgewählte Anforderung beispielsweise eine höhere Priorität, und die grüne Anforderung darunter hat eine niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="361e9-348">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="361e9-349">In der 1. der folgenden Abbildungen wird die Anforderung durch eine Linie auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Und einem hellen Teil und einer Linie auf der rechten Seite `www.bing.com` dargestellt.</span><span class="sxs-lookup"><span data-stu-id="361e9-349">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="361e9-350">Im 2. der folgenden Abbildungen ist die entsprechende Darstellung derselben Anforderung im **Zeitfenster** des **Netzwerktools** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-350">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** panel of the **Network** tool.</span></span>  <span data-ttu-id="361e9-351">So ordnen sich diese beiden Darstellungen zu:</span><span class="sxs-lookup"><span data-stu-id="361e9-351">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="361e9-352">Die linke Linie ist alles bis zur `Connection Start` Gruppe von Ereignissen, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="361e9-352">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="361e9-353">Mit anderen Worten, es ist alles vor `Request Sent` , exklusiv.</span><span class="sxs-lookup"><span data-stu-id="361e9-353">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="361e9-354">Der helle Teil der Leiste ist `Request Sent` und `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="361e9-354">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="361e9-355">Der dunkle Teil der Leiste ist `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="361e9-355">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="361e9-356">Die rechte Linie ist im Wesentlichen eine Zeit, die auf das Warten auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="361e9-356">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="361e9-357">Dies wird im **Zeitsteuerungsfenster nicht** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="361e9-357">This is not represented in the **Timing** panel.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Die Zeilenleistendarstellung der www.bing.com Anforderung" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="361e9-359">Die Zeilenleistendarstellung der `www.bing.com` Anforderung</span><span class="sxs-lookup"><span data-stu-id="361e9-359">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Das Netzwerktool" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="361e9-361">Das **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="361e9-361">The **Network** tool</span></span>  
<span data-ttu-id="361e9-362">: ::image-end:::</span><span class="sxs-lookup"><span data-stu-id="361e9-362">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a><span data-ttu-id="361e9-363">Anzeigen von Speichermetriken</span><span class="sxs-lookup"><span data-stu-id="361e9-363">View memory metrics</span></span>  

<span data-ttu-id="361e9-364">Aktivieren Sie das **Kontrollkästchen Speicher,** um Speichermetriken aus der letzten Aufzeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="361e9-364">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Das Kontrollkästchen Speicher" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="361e9-366">Das **Kontrollkästchen Speicher**</span><span class="sxs-lookup"><span data-stu-id="361e9-366">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-367">DevTools zeigt ein neues **Arbeitsspeicherdiagramm** über dem **Zusammenfassungsfenster** an.</span><span class="sxs-lookup"><span data-stu-id="361e9-367">DevTools displays a new **Memory** chart, above the **Summary** panel.</span></span>  <span data-ttu-id="361e9-368">Es gibt auch ein neues Diagramm unterhalb des **NET-Diagramms** mit dem Namen **HEAP**.</span><span class="sxs-lookup"><span data-stu-id="361e9-368">There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="361e9-369">Das **HEAP-Diagramm** enthält die gleichen Informationen wie die **JS-Heap-Zeile** im **Arbeitsspeicherdiagramm.**</span><span class="sxs-lookup"><span data-stu-id="361e9-369">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Speichermetriken" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="361e9-371">Speichermetriken</span><span class="sxs-lookup"><span data-stu-id="361e9-371">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-372">Die farbigen Linien im Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="361e9-372">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="361e9-373">Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie im Diagramm auszublenden.</span><span class="sxs-lookup"><span data-stu-id="361e9-373">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="361e9-374">Das Diagramm zeigt nur den Bereich der aktuell ausgewählten Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="361e9-374">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="361e9-375">In der vorherigen Abbildung \*\*\*\* zeigt das Diagramm Arbeitsspeicher beispielsweise nur die Speicherauslastung zwischen 400 ms und 1750 ms an.</span><span class="sxs-lookup"><span data-stu-id="361e9-375">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a><span data-ttu-id="361e9-376">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-376">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="361e9-377">Bei der Analyse eines Abschnitts wie **"Netzwerk"** oder **"Main"** benötigen Sie manchmal eine genauere Schätzung der Dauer bestimmter Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="361e9-377">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="361e9-378">Halten, auswählen und halten Sie, und ziehen Sie nach links oder rechts, um `Shift` einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-378">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="361e9-379">Am unteren Rand Ihrer Auswahl zeigt DevTools, wie lange dieser Teil ge dauern hat.</span><span class="sxs-lookup"><span data-stu-id="361e9-379">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Anzeigen der Dauer eines Teils einer Aufzeichnung" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="361e9-381">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="361e9-381">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <a name="view-a-screenshot"></a><span data-ttu-id="361e9-382">Screenshot anzeigen</span><span class="sxs-lookup"><span data-stu-id="361e9-382">View a screenshot</span></span>  

<span data-ttu-id="361e9-383">Navigieren Sie während der Aufzeichnung zu Screenshots [aufnehmen,](#capture-screenshots-while-recording) um zu erfahren, wie Sie Screenshots aktivieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-383">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="361e9-384">Zeigen Sie auf **die Übersicht,** um einen Screenshot zu sehen, wie die Seite in diesem Moment der Aufzeichnung aussah.</span><span class="sxs-lookup"><span data-stu-id="361e9-384">Hover on the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="361e9-385">Der **Abschnitt Übersicht** enthält die Diagramme **CPU,** **FPS**und **NET.**</span><span class="sxs-lookup"><span data-stu-id="361e9-385">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Screenshot anzeigen" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="361e9-387">Screenshot anzeigen</span><span class="sxs-lookup"><span data-stu-id="361e9-387">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-388">Sie können auch Screenshots anzeigen, indem Sie im Abschnitt Frames einen **Frame** auswählen.</span><span class="sxs-lookup"><span data-stu-id="361e9-388">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="361e9-389">DevTools zeigt eine kleine Version des Screenshots im **Zusammenfassungsbereich** an.</span><span class="sxs-lookup"><span data-stu-id="361e9-389">DevTools displays a small version of the screenshot in the **Summary** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Anzeigen eines Screenshots im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="361e9-391">Anzeigen eines Screenshots im **Zusammenfassungsfenster**</span><span class="sxs-lookup"><span data-stu-id="361e9-391">View a screenshot in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-392">Wählen Sie die Miniaturansicht im **Zusammenfassungsfenster aus,** um den Screenshot zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="361e9-392">Choose the thumbnail in the **Summary** panel to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Vergrößern eines Screenshots aus dem Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="361e9-394">Vergrößern eines Screenshots aus dem **Zusammenfassungsfenster**</span><span class="sxs-lookup"><span data-stu-id="361e9-394">Zoom into a screenshot from the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-layers-information"></a><span data-ttu-id="361e9-395">Anzeigen von Layerinformationen</span><span class="sxs-lookup"><span data-stu-id="361e9-395">View layers information</span></span>  

<span data-ttu-id="361e9-396">So zeigen Sie erweiterte Layerinformationen zu einem Frame an:</span><span class="sxs-lookup"><span data-stu-id="361e9-396">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="361e9-397">[Aktivieren Sie die erweiterte Malinstrumentierung.](#turn-on-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="361e9-397">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="361e9-398">Wählen Sie im Abschnitt **Frames einen Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="361e9-398">Choose a frame in the **Frames** section.</span></span>  <span data-ttu-id="361e9-399">DevTools zeigt Informationen zu den Ebenen im neuen **Ebenenbereich** neben dem **Ereignisprotokollbereich** an.</span><span class="sxs-lookup"><span data-stu-id="361e9-399">DevTools displays information about the layers in the new **Layers** panel, next to the **Event Log** panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Der Bereich Ebenen" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="361e9-401">Der **Bereich Ebenen**</span><span class="sxs-lookup"><span data-stu-id="361e9-401">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="361e9-402">Zeigen Sie auf eine Ebene, um sie im Diagramm zu markieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-402">Hover on a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Hervorheben einer Ebene" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="361e9-404">Hervorheben einer Ebene</span><span class="sxs-lookup"><span data-stu-id="361e9-404">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="361e9-405">So verschieben Sie das Diagramm:</span><span class="sxs-lookup"><span data-stu-id="361e9-405">To move the diagram:</span></span>  

*   <span data-ttu-id="361e9-406">Wählen **Sie Schwenkmodus** \( ![ Schwenkmodus ][ImagePanModeIcon] \), um sich entlang der X- und Y-Achsen zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="361e9-406">Choose **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="361e9-407">Wählen **Sie Drehmodus** \( ![ Drehmodus ][ImageRotateModeIcon] \) aus, um sich entlang der Z-Achse zu drehen.</span><span class="sxs-lookup"><span data-stu-id="361e9-407">Choose **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="361e9-408">Wählen **Sie Transform zurücksetzen** \( Transform zurücksetzen ![ ][ImageResetTransformIcon] \), um das Diagramm an die ursprüngliche Position zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="361e9-408">Choose **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <a name="view-paint-profiler"></a><span data-ttu-id="361e9-409">Anzeigen von Farbprofiler</span><span class="sxs-lookup"><span data-stu-id="361e9-409">View paint profiler</span></span>  

<span data-ttu-id="361e9-410">So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:</span><span class="sxs-lookup"><span data-stu-id="361e9-410">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="361e9-411">[Aktivieren Sie](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="361e9-411">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="361e9-412">Wählen Sie im **Abschnitt** Main ein **Paint-Ereignis** aus.</span><span class="sxs-lookup"><span data-stu-id="361e9-412">Choose a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Der Bereich "Paint Profiler"" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="361e9-414">Der **Bereich "Paint Profiler"**</span><span class="sxs-lookup"><span data-stu-id="361e9-414">The **Paint Profiler** panel</span></span>  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a><span data-ttu-id="361e9-415">Analysieren der Renderingleistung mit dem Renderingtool</span><span class="sxs-lookup"><span data-stu-id="361e9-415">Analyze rendering performance with the Rendering tool</span></span>  

<span data-ttu-id="361e9-416">Verwenden Sie die \*\*\*\* Features des Renderingbereichs, um die Renderingleistung Ihrer Seite zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-416">Use the features of the **Rendering** panel to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="361e9-417">So öffnen Sie das **Renderingtool:**</span><span class="sxs-lookup"><span data-stu-id="361e9-417">To open the **Rendering** tool:</span></span>  

1.  <span data-ttu-id="361e9-418">[Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="361e9-418">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="361e9-419">Beginnen Sie mit der `Rendering` Eingabe und wählen Sie `Show Rendering` aus.</span><span class="sxs-lookup"><span data-stu-id="361e9-419">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="361e9-420">DevTools zeigt das **Renderingtool** am unteren Rand des DevTools-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="361e9-420">DevTools displays the **Rendering** tool at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Das Renderingtool" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="361e9-422">Das **Renderingtool**</span><span class="sxs-lookup"><span data-stu-id="361e9-422">The **Rendering** tool</span></span>  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a><span data-ttu-id="361e9-423">Anzeigen von Frames pro Sekunde in Echtzeit mit dem #A0</span><span class="sxs-lookup"><span data-stu-id="361e9-423">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="361e9-424">Die **#A0 ist** eine Überlagerung, die in der oberen rechten Ecke Des Viewports angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-424">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="361e9-425">Es bietet eine Echtzeitschätzung von FPS, während die Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="361e9-425">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="361e9-426">So öffnen Sie das **FPS-Zähler:**</span><span class="sxs-lookup"><span data-stu-id="361e9-426">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="361e9-427">Öffnen Sie das **Renderingtool.**</span><span class="sxs-lookup"><span data-stu-id="361e9-427">Open the **Rendering** tool.</span></span>  <span data-ttu-id="361e9-428">[Analysieren Sie die Renderingleistung mit dem Renderingtool](#analyze-rendering-performance-with-the-rendering-tool).</span><span class="sxs-lookup"><span data-stu-id="361e9-428">[Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="361e9-429">Aktivieren Sie das **Kontrollkästchen FPS Meter.**</span><span class="sxs-lookup"><span data-stu-id="361e9-429">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="361e9-431">Das **#A0**</span><span class="sxs-lookup"><span data-stu-id="361e9-431">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a><span data-ttu-id="361e9-432">Anzeigen von Malereignissen in Echtzeit mit Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="361e9-432">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="361e9-433">Verwenden Sie Paint Flashing, um eine Echtzeitansicht aller Malereignisse auf der Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="361e9-433">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="361e9-434">Jedes Mal, wenn ein Teil der Seite neu angestrichen wird, umreißt DevTools diesen Abschnitt grün.</span><span class="sxs-lookup"><span data-stu-id="361e9-434">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="361e9-435">Führen Sie die folgenden Aktionen aus, um das Blinken von Farben zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="361e9-435">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="361e9-436">Öffnen Sie das **Renderingtool.**</span><span class="sxs-lookup"><span data-stu-id="361e9-436">Open the **Rendering** tool.</span></span>  <span data-ttu-id="361e9-437">Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="361e9-437">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="361e9-438">Aktivieren Sie das **Kontrollkästchen Farbenblitzen.**</span><span class="sxs-lookup"><span data-stu-id="361e9-438">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Blinken von Farben" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="361e9-440">Blinken von Farben</span><span class="sxs-lookup"><span data-stu-id="361e9-440">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a><span data-ttu-id="361e9-441">Anzeigen einer Überlagerung von Ebenen mit Ebenenrändern</span><span class="sxs-lookup"><span data-stu-id="361e9-441">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="361e9-442">Verwenden **Sie Ebenenränder,** um eine Überlagerung von Ebenenrändern und Kacheln oben auf der Seite zu sehen.</span><span class="sxs-lookup"><span data-stu-id="361e9-442">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="361e9-443">Führen Sie zum Aktivieren von Ebenenrändern die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="361e9-443">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="361e9-444">Öffnen Sie das **Renderingtool.**</span><span class="sxs-lookup"><span data-stu-id="361e9-444">Open the **Rendering** tool.</span></span>  <span data-ttu-id="361e9-445">Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="361e9-445">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="361e9-446">Aktivieren Sie das **Kontrollkästchen Ebenenränder.**</span><span class="sxs-lookup"><span data-stu-id="361e9-446">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Ebenenränder" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="361e9-448">Ebenenränder</span><span class="sxs-lookup"><span data-stu-id="361e9-448">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="361e9-449">Navigieren Sie zu den Kommentaren in [debug_colors.cc,][ChromiumDebugColors] um eine Erläuterung der Farbcodierungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="361e9-449">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <a name="find-scroll-performance-issues-in-realtime"></a><span data-ttu-id="361e9-450">Suchen von Problemen mit der Bildlaufleistung in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="361e9-450">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="361e9-451">Verwenden Sie Bildlaufleistungsprobleme, um Elemente der Seite zu identifizieren, die Ereignislistener im Zusammenhang mit einem Bildlauf haben, die die Leistung der Seite beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="361e9-451">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="361e9-452">DevTools skizziert die potenziell problematischen Elemente in Teal.</span><span class="sxs-lookup"><span data-stu-id="361e9-452">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="361e9-453">Führen Sie die folgenden Aktionen aus, um Probleme mit der Bildlaufleistung zu sehen.</span><span class="sxs-lookup"><span data-stu-id="361e9-453">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="361e9-454">Öffnen Sie das **Renderingtool.**</span><span class="sxs-lookup"><span data-stu-id="361e9-454">Open the **Rendering** tool.</span></span>  <span data-ttu-id="361e9-455">Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="361e9-455">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="361e9-456">Aktivieren Sie das **Kontrollkästchen Leistungsprobleme** beim Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="361e9-456">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Scrolling Performance Issues gibt an, dass objekte, die nicht mit viewport eingeschränkt sind, die Bildlaufleistung beeinträchtigen können." lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="361e9-458">**Scrolling Performance Issues** gibt an, dass objekte, die nicht mit viewport eingeschränkt sind, die Bildlaufleistung beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="361e9-458">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="361e9-459">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="361e9-459">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Öffnen Sie das Befehlsmenü - Befehle ausführen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Erste Schritte mit der Analyse der Laufzeitleistung | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Aktivitätsregisterkarten Demo | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc – Codesuche"  

> [!NOTE]
> <span data-ttu-id="361e9-465">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="361e9-465">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="361e9-466">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="361e9-466">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="361e9-468">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="361e9-468">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
