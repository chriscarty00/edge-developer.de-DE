---
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611748"
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







# <span data-ttu-id="c765b-103">Referenz zur Leistungsanalyse</span><span class="sxs-lookup"><span data-stu-id="c765b-103">Performance Analysis Reference</span></span>   



<span data-ttu-id="c765b-104">Diese Seite ist eine umfassende Referenz zu den Microsoft Edge devtools-Features, die sich auf die Leistungsanalyse beziehen.</span><span class="sxs-lookup"><span data-stu-id="c765b-104">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="c765b-105">Eine Anleitung zum Analysieren der Leistung einer Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]finden Sie unter [Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] .</span><span class="sxs-lookup"><span data-stu-id="c765b-105">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="c765b-106">Aufzeichnen der Leistung</span><span class="sxs-lookup"><span data-stu-id="c765b-106">Record performance</span></span>   

### <span data-ttu-id="c765b-107">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="c765b-107">Record runtime performance</span></span>   

<span data-ttu-id="c765b-108">Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, anstatt Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="c765b-108">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="c765b-109">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c765b-109">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c765b-110">Klicken Sie in devtools auf die Registerkarte **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="c765b-110">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="c765b-111">Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="c765b-111">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    
    > ##### <span data-ttu-id="c765b-112">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="c765b-112">Figure 1</span></span>  
    > **<span data-ttu-id="c765b-113">Record</span><span class="sxs-lookup"><span data-stu-id="c765b-113">Record</span></span>**  
    > ![Record][ImageRecord]  

1.  <span data-ttu-id="c765b-115">Interagieren Sie mit der Seite.</span><span class="sxs-lookup"><span data-stu-id="c765b-115">Interact with the page.</span></span>  <span data-ttu-id="c765b-116">DevTools zeichnet alle Seiten Aktivitäten auf, die durch ihre Interaktionen entstehen.</span><span class="sxs-lookup"><span data-stu-id="c765b-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="c765b-117">Klicken Sie erneut auf **aufzeichnen** , oder klicken Sie auf **Beenden** , um die Aufzeichnung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c765b-117">Click **Record** again or click **Stop** to stop recording.</span></span>  

### <span data-ttu-id="c765b-118">Aufzeichnen der Ladeleistung</span><span class="sxs-lookup"><span data-stu-id="c765b-118">Record load performance</span></span>   

<span data-ttu-id="c765b-119">Zeichnen Sie die Ladeleistung auf, wenn Sie die Leistung einer Seite während des Ladens analysieren möchten, anstatt Sie zu starten.</span><span class="sxs-lookup"><span data-stu-id="c765b-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="c765b-120">Wechseln Sie zu der Seite, die Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c765b-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="c765b-121">Öffnen Sie das **Leistungs** Panel von devtools.</span><span class="sxs-lookup"><span data-stu-id="c765b-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="c765b-122">Klicken **Sie auf Seite aktualisieren** ![ ][ImageRefreshPageIcon] .</span><span class="sxs-lookup"><span data-stu-id="c765b-122">Click **Refresh page** ![Refresh Page][ImageRefreshPageIcon].</span></span>  <span data-ttu-id="c765b-123">DevTools zeichnet Leistungs Metriken auf, während die Seite aktualisiert wird, und stoppt dann die Aufzeichnung ein paar Sekunden nach Abschluss der Auslastung automatisch.</span><span class="sxs-lookup"><span data-stu-id="c765b-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    > ##### <span data-ttu-id="c765b-124">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="c765b-124">Figure 2</span></span>  
    > **<span data-ttu-id="c765b-125">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c765b-125">Refresh page</span></span>**  
    > ![Seite aktualisieren][ImageRefreshPage]  

<span data-ttu-id="c765b-127">DevTools zoomt automatisch auf den Teil der Aufzeichnung, in dem die meisten Aktivitäten aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-127">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

> ##### <span data-ttu-id="c765b-128">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="c765b-128">Figure 3</span></span>  
> <span data-ttu-id="c765b-129">Laden einer Seite</span><span class="sxs-lookup"><span data-stu-id="c765b-129">A page-load recording</span></span>  
> ![Laden einer Seite][ImageLoadRecording]  

### <span data-ttu-id="c765b-131">Aufzeichnen von Screenshots während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-131">Capture screenshots while recording</span></span>   

<span data-ttu-id="c765b-132">Aktivieren Sie das Kontrollkästchen **Screenshots** , um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c765b-132">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

> ##### <span data-ttu-id="c765b-133">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="c765b-133">Figure 4</span></span>  
> <span data-ttu-id="c765b-134">Das Kontrollkästchen " **Screenshots** "</span><span class="sxs-lookup"><span data-stu-id="c765b-134">The **Screenshots** checkbox</span></span>  
> ![Das Kontrollkästchen "Screenshots"][ImageScreenshots]  

<span data-ttu-id="c765b-136">Informationen zum interagieren mit Screenshots finden Sie unter [Anzeigen eines](#view-a-screenshot) Screenshots.</span><span class="sxs-lookup"><span data-stu-id="c765b-136">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="c765b-137">Erzwingen der Garbage Collection während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-137">Force garbage collection while recording</span></span>   

<span data-ttu-id="c765b-138">Klicken Sie während der Aufzeichnung einer Seite auf Garbage Collect Garbage Collection **sammeln** , ![ ][ImageCollectGarbageIcon] um die Garbage Collection zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c765b-138">While you are recording a page, click **Collect garbage** ![Collect garbage][ImageCollectGarbageIcon] to force garbage collection.</span></span>  

> ##### <span data-ttu-id="c765b-139">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="c765b-139">Figure 5</span></span>  
> <span data-ttu-id="c765b-140">Garbage Collection</span><span class="sxs-lookup"><span data-stu-id="c765b-140">Collect garbage</span></span>  
> ![Garbage Collection][ImageCollectGarbage]  

### <span data-ttu-id="c765b-142">Aufzeichnungseinstellungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="c765b-142">Show recording settings</span></span>   

<span data-ttu-id="c765b-143">Klicken Sie auf Einstellungen für Aufnahme **Einstellungen** ![ ][ImageCaptureSettingsIcon] , um weitere Einstellungen anzuzeigen, die sich auf die Darstellung von Leistungs Aufzeichnungen in devtools beziehen.</span><span class="sxs-lookup"><span data-stu-id="c765b-143">Click **Capture settings** ![Capture settings][ImageCaptureSettingsIcon] to expose more settings related to how DevTools captures performance recordings.</span></span>  

> ##### <span data-ttu-id="c765b-144">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="c765b-144">Figure 6</span></span>  
> <span data-ttu-id="c765b-145">Abschnitt " **aufnahmeeinstellungen** "</span><span class="sxs-lookup"><span data-stu-id="c765b-145">The **Capture settings** section</span></span>  
> ![Abschnitt "Aufnahmeeinstellungen"][ImageCaptureSettings]  

### <span data-ttu-id="c765b-147">Deaktivieren von JavaScript-Beispielen</span><span class="sxs-lookup"><span data-stu-id="c765b-147">Disable JavaScript samples</span></span>   

<span data-ttu-id="c765b-148">Standardmäßig werden im **Haupt** Abschnitt einer Aufzeichnung detaillierte Aufruflisten von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c765b-148">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="c765b-149">So deaktivieren Sie diese Anruflisten:</span><span class="sxs-lookup"><span data-stu-id="c765b-149">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="c765b-150">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-150">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c765b-151">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c765b-151">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c765b-152">Aktivieren Sie das Kontrollkästchen **JavaScript-Beispiele deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c765b-152">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="c765b-153">Nehmen Sie eine Aufzeichnung der Seite auf.</span><span class="sxs-lookup"><span data-stu-id="c765b-153">Take a recording of the page.</span></span>  

<span data-ttu-id="c765b-154">[Abbildung 7](#figure-7) und [Abbildung 8](#figure-8) zeigen den Unterschied zwischen dem deaktivieren und Aktivieren von JavaScript-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="c765b-154">[Figure 7](#figure-7) and [Figure 8](#figure-8) show the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="c765b-155">Der **Haupt** Abschnitt der Aufzeichnung ist viel kürzer, wenn Sampling deaktiviert ist, da alle JavaScript-Aufruflisten ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c765b-155">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

> ##### <span data-ttu-id="c765b-156">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="c765b-156">Figure 7</span></span>  
> <span data-ttu-id="c765b-157">Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind</span><span class="sxs-lookup"><span data-stu-id="c765b-157">An example of a recording when JS samples are disabled</span></span>  
> ![Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind][ImageJSSamplesDisabled]  

> ##### <span data-ttu-id="c765b-159">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="c765b-159">Figure 8</span></span>  
> <span data-ttu-id="c765b-160">Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="c765b-160">An example of a recording when JS samples are enabled</span></span>  
> ![Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind][ImageJSSamplesEnabled]  

### <span data-ttu-id="c765b-162">Drosseln des Netzwerks während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-162">Throttle the network while recording</span></span>   

<span data-ttu-id="c765b-163">So Drosseln Sie das Netzwerk während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="c765b-163">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="c765b-164">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-164">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c765b-165">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c765b-165">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c765b-166">Stellen Sie **Network** auf die gewünschte drosselungsebene ein.</span><span class="sxs-lookup"><span data-stu-id="c765b-166">Set **Network** to the desired level of throttling.</span></span>  

### <span data-ttu-id="c765b-167">Drosseln der CPU während der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-167">Throttle the CPU while recording</span></span>   

<span data-ttu-id="c765b-168">So Drosseln Sie die CPU während der Aufzeichnung:</span><span class="sxs-lookup"><span data-stu-id="c765b-168">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="c765b-169">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-169">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c765b-170">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c765b-170">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c765b-171">Setzen Sie die **CPU** auf das gewünschte Drosselungs Niveau.</span><span class="sxs-lookup"><span data-stu-id="c765b-171">Set **CPU** to the desired level of throttling.</span></span>  

<span data-ttu-id="c765b-172">Die Drosselung ist relativ zu den Funktionen Ihres Computers.</span><span class="sxs-lookup"><span data-stu-id="c765b-172">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="c765b-173">Mit der Option " **2X verlangsamen** " wird beispielsweise die CPU zwei Mal langsamer als normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c765b-173">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="c765b-174">DevTools simulieren die CPUs von mobilen Geräten nicht wirklich, da sich die Architektur von mobilen Geräten stark von der von Desktops und Laptops unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="c765b-174">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="c765b-175">Erweiterte Paint-Instrumentation aktivieren</span><span class="sxs-lookup"><span data-stu-id="c765b-175">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="c765b-176">So zeigen Sie die detaillierte Farb Instrumentation an:</span><span class="sxs-lookup"><span data-stu-id="c765b-176">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="c765b-177">Öffnen Sie das Menü " **aufnahmeeinstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-177">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="c765b-178">Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="c765b-178">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="c765b-179">Aktivieren Sie das Kontrollkästchen **Erweiterte Farb Instrumentation (langsam) aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="c765b-179">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="c765b-180">Informationen zur Interaktion mit den Malfarbe-Informationen finden Sie unter [Anzeigen von Ebenen](#view-layers-information) und [Anzeigen von Paint Profiler](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="c765b-180">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="c765b-181">Speichern einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-181">Save a recording</span></span>   

<span data-ttu-id="c765b-182">Wenn Sie eine Aufzeichnung speichern möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-182">To save a recording, right-click and select **Save Profile**.</span></span>  

> ##### <span data-ttu-id="c765b-183">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="c765b-183">Figure 9</span></span>  
> **<span data-ttu-id="c765b-184">Profil speichern</span><span class="sxs-lookup"><span data-stu-id="c765b-184">Save Profile</span></span>**  
> ![Profil speichern][ImageSaveProfile]  

## <span data-ttu-id="c765b-186">Laden einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-186">Load a recording</span></span>   

<span data-ttu-id="c765b-187">Wenn Sie eine Aufzeichnung laden möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil laden**aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-187">To load a recording, right-click and select **Load Profile**.</span></span>  

> ##### <span data-ttu-id="c765b-188">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="c765b-188">Figure 10</span></span>  
> **<span data-ttu-id="c765b-189">Profil laden</span><span class="sxs-lookup"><span data-stu-id="c765b-189">Load Profile</span></span>**  
> ![Profil laden][ImageLoadProfile]  

## <span data-ttu-id="c765b-191">Löschen der vorherigen Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-191">Clear the previous recording</span></span>   

<span data-ttu-id="c765b-192">Nachdem **Sie eine** Aufzeichnung gemacht haben, drücken Sie die Aufzeichnung löschen, um die Aufzeichnung ![ ][ImageClearRecordingIcon] aus dem **Leistungs** Panel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c765b-192">After making a recording, press **Clear recording** ![Clear recording][ImageClearRecordingIcon] to clear that recording from the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="c765b-193">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="c765b-193">Figure 11</span></span>  
> <span data-ttu-id="c765b-194">Aufzeichnen löschen</span><span class="sxs-lookup"><span data-stu-id="c765b-194">Clear recording</span></span>  
> ![Aufzeichnen löschen][ImageClearRecording]  

## <span data-ttu-id="c765b-196">Analysieren einer Leistungsaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-196">Analyze a performance recording</span></span>   

<span data-ttu-id="c765b-197">Nachdem Sie die Leistung der [Lauf Zeitaufzeichnung](#record-runtime-performance) oder die [Daten Satz Auslastung](#record-load-performance)aufgezeichnet haben, bietet der **Leistungs** Bereich viele Daten für die Analyse der Leistung von dem, was gerade geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="c765b-197">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="c765b-198">Auswählen eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-198">Select a portion of a recording</span></span>   

<span data-ttu-id="c765b-199">Ziehen Sie den Mauszeiger über die **Übersicht** nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c765b-199">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="c765b-200">Die **Übersicht** ist der Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-200">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="c765b-201">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="c765b-201">Figure 12</span></span>  
> <span data-ttu-id="c765b-202">Ziehen der Maus über die Übersicht zum Zoomen</span><span class="sxs-lookup"><span data-stu-id="c765b-202">Dragging the mouse across the Overview to zoom</span></span>  
> ![Ziehen der Maus über die Übersicht zum Zoomen][ImageZoom]  

<span data-ttu-id="c765b-204">So wählen Sie einen Teil über die Tastatur aus:</span><span class="sxs-lookup"><span data-stu-id="c765b-204">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="c765b-205">Klicken Sie auf den Hintergrund des **Haupt** Abschnitts oder eines der Abschnitte daneben, wie **Interaktionen**, **Netzwerk**oder **GPU**.</span><span class="sxs-lookup"><span data-stu-id="c765b-205">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="c765b-206">Dieser Tastatur Workflow funktioniert nur, wenn einer dieser Abschnitte den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="c765b-206">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="c765b-207">Verwenden Sie `W` die `A` Tasten,, `S` , `D` um Sie zu vergrößern, nach Links zu verschieben, zu verkleinern und nach rechts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c765b-207">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="c765b-208">So wählen Sie einen Teil mithilfe eines Trackpads aus:</span><span class="sxs-lookup"><span data-stu-id="c765b-208">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="c765b-209">Zeigen Sie mit der Maus auf den Abschnitt " **Übersicht** " oder den Abschnitt " **Details** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-209">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="c765b-210">Der Abschnitt " **Übersicht** " ist der Bereich, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-210">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="c765b-211">Der Abschnitt **Details** ist der Bereich, der den **Haupt** Abschnitt, den Abschnitt **Interaktionen** und so weiter enthält.</span><span class="sxs-lookup"><span data-stu-id="c765b-211">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="c765b-212">Wischen Sie mit zwei Fingern nach oben, um es zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um die Ansicht zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln</span><span class="sxs-lookup"><span data-stu-id="c765b-212">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="c765b-213">Wenn Sie im **Haupt** Abschnitt oder in einem der Nachbarn in einem langen Flammen Diagramm Scrollen möchten, klicken und halten Sie beim Ziehen nach oben und unten.</span><span class="sxs-lookup"><span data-stu-id="c765b-213">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="c765b-214">Ziehen Sie nach links und rechts, um zu verschieben, welcher Teil der Aufzeichnung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c765b-214">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="c765b-215">Suchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c765b-215">Search activities</span></span>   

<span data-ttu-id="c765b-216">Drücken Sie `Control` + `F` \ (Windows \) oder `Command` + `F` \ (macOS \), um das Suchfeld unten im **Leistungs** Bereich zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c765b-216">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

> ##### <span data-ttu-id="c765b-217">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="c765b-217">Figure 13</span></span>  
> <span data-ttu-id="c765b-218">Verwenden von Regex im Suchfeld am unteren Rand des Fensters, um alle Aktivitäten zu finden, die mit beginnen</span><span class="sxs-lookup"><span data-stu-id="c765b-218">Using regex in the search box at the bottom of the window to find any activity that begins with</span></span> `E`  
> ![Suchfeld][ImageSearch]  

<span data-ttu-id="c765b-220">So navigieren Sie in Aktivitäten, die Ihrer Abfrage entsprechen:</span><span class="sxs-lookup"><span data-stu-id="c765b-220">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="c765b-221">Verwenden Sie die Schaltflächen **vorheriger** ![ ][ImagePreviousIcon] und **Nächster** ![ Nächster Schritt ][ImageNextIcon] .</span><span class="sxs-lookup"><span data-stu-id="c765b-221">Use the **Previous** ![Previous][ImagePreviousIcon] and **Next** ![Next][ImageNextIcon] buttons.</span></span>  
*   <span data-ttu-id="c765b-222">Drücken Sie `Shift` + `Enter` , um die vorherige oder `Enter` die nächste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c765b-222">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="c765b-223">So ändern Sie die Abfrageeinstellungen:</span><span class="sxs-lookup"><span data-stu-id="c765b-223">To modify query settings:</span></span>  

*   <span data-ttu-id="c765b-224">Drücken **Sie** ![ die Groß-/Kleinschreibung von Groß-/Kleinschreibung ][ImageSearchCaseIcon] , damit die Abfrage Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="c765b-224">Press **Case sensitive** ![Case sensitive][ImageSearchCaseIcon] to make the query case sensitive.</span></span>  
*   <span data-ttu-id="c765b-225">Drücken Sie **Regex** ![ Regex ][ImageSearchRegexIcon] , um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c765b-225">Press **Regex** ![Regex][ImageSearchRegexIcon] to use a regular expression in your query.</span></span>  

<span data-ttu-id="c765b-226">Wenn Sie das Suchfeld ausblenden möchten, drücken Sie **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="c765b-226">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="c765b-227">Hauptthread Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="c765b-227">View main thread activity</span></span>   

<span data-ttu-id="c765b-228">Verwenden Sie den **Haupt** Abschnitt, um die Aktivitäten anzuzeigen, die im Hauptthread der Seite aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-228">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

> ##### <span data-ttu-id="c765b-229">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="c765b-229">Figure 14</span></span>  
> <span data-ttu-id="c765b-230">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c765b-230">The **Main** section</span></span>  
> ![Der Hauptabschnitt][ImageMain]  

<span data-ttu-id="c765b-232">Klicken Sie auf ein Ereignis, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  DevTools skizziert das ausgewählte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c765b-232">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

> ##### <span data-ttu-id="c765b-233">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="c765b-233">Figure 15</span></span>  
> <span data-ttu-id="c765b-234">Weitere Informationen zur `anonymous` Funktion auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c765b-234">More information about the `anonymous` function in the **Summary** tab</span></span>  
> ![Weitere Informationen zur anonymen Funktion auf der Registerkarte "Zusammenfassung"][ImageMainEventSummary]  

<span data-ttu-id="c765b-236">DevTools stellt die Hauptthread Aktivität mit einem Flammen Diagramm dar.</span><span class="sxs-lookup"><span data-stu-id="c765b-236">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="c765b-237">Die x-Achse stellt die Aufzeichnung über einen Zeitraum dar.</span><span class="sxs-lookup"><span data-stu-id="c765b-237">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="c765b-238">Die y-Achse steht für die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="c765b-238">The y-axis represents the call stack.</span></span>  <span data-ttu-id="c765b-239">Die Ereignisse im Vordergrund führen zu den darunter liegenden Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c765b-239">The events on top cause the events below it.</span></span>  

> ##### <span data-ttu-id="c765b-240">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="c765b-240">Figure 16</span></span>  
> <span data-ttu-id="c765b-241">Ein Flammen Diagramm im **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c765b-241">A flame chart in the **Main** section</span></span>  
> ![Ein Flammen Diagramm][ImageFlameChart]  

<span data-ttu-id="c765b-243">In [Abbildung 16](#figure-16)hat ein `click` Ereignis eine `Function Call` in `activitytabs.js` on Zeile 53 verursacht.</span><span class="sxs-lookup"><span data-stu-id="c765b-243">In [Figure 16](#figure-16), a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="c765b-244">Unten `Function Call` sehen Sie, dass eine anonyme Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-244">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="c765b-245">Die anonyme Funktion mit dem Namen, die aufgerufen `a` `wait` wird `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="c765b-245">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="c765b-246">DevTools weist Skripten zufällige Farben zu.</span><span class="sxs-lookup"><span data-stu-id="c765b-246">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="c765b-247">In [Abbildung 16](#figure-16)sind Funktionsaufrufe eines Skripts farbig hellgrün.</span><span class="sxs-lookup"><span data-stu-id="c765b-247">In [Figure 16](#figure-16), function calls from one script are colored light green.</span></span>  <span data-ttu-id="c765b-248">Anrufe von einem anderen Skript sind farbig beige.</span><span class="sxs-lookup"><span data-stu-id="c765b-248">Calls from another script are colored beige.</span></span>  <span data-ttu-id="c765b-249">Das dunklere Gelb steht für Skriptaktivitäten, und das Purple-Ereignis stellt die Rendering-Aktivität dar.</span><span class="sxs-lookup"><span data-stu-id="c765b-249">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="c765b-250">Diese dunkelgelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="c765b-250">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="c765b-251">Weitere Informationen finden Sie unter [Deaktivieren von JavaScript-Beispielen](#disable-javascript-samples) , wenn Sie den detaillierten Flammen Diagramm von JavaScript-anrufen ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c765b-251">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="c765b-252">Wenn js-Beispiele deaktiviert sind, werden nur Ereignisse auf höherer Ebene angezeigt, `Event: click` wie `Function Call` in [Abbildung 16](#figure-16).</span><span class="sxs-lookup"><span data-stu-id="c765b-252">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from [Figure 16](#figure-16).</span></span>  

### <span data-ttu-id="c765b-253">Anzeigen von Aktivitäten in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="c765b-253">View activities in a table</span></span>   

<span data-ttu-id="c765b-254">Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Haupt** Abschnitt verlassen, um Aktivitäten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-254">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="c765b-255">DevTools stellt auch drei tabellarische Ansichten zum Analysieren von Aktivitäten bereit.</span><span class="sxs-lookup"><span data-stu-id="c765b-255">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="c765b-256">Jede Ansicht gibt Ihnen eine andere Perspektive auf die Aktivitäten:</span><span class="sxs-lookup"><span data-stu-id="c765b-256">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="c765b-257">Wenn Sie die Stammaktivitäten anzeigen möchten, die die meiste Arbeit verursachen, verwenden Sie [die Registerkarte **anrufstruktur** ](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-257">When you want to view the root activities that cause the most work, use [the **Call Tree** tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="c765b-258">Wenn Sie die Aktivitäten anzeigen möchten, bei denen die meiste Zeit direkt ausgegeben wurde, verwenden Sie [die Registerkarte **unten nach oben** ](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-258">When you want to view the activities where the most time was directly spent, use [the **Bottom-Up** tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="c765b-259">Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der Sie während der Aufzeichnung aufgetreten sind, verwenden Sie [die Registerkarte **Ereignisprotokoll** ](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-259">When you want to view the activities in the order in which they occurred during the recording, use [the **Event Log** tab](#the-event-log-tab).</span></span>  

> [!NOTE]
> <span data-ttu-id="c765b-260">Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.</span><span class="sxs-lookup"><span data-stu-id="c765b-260">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="c765b-261">Führen Sie die Demo selbst auf der [Registerkarte Activity Tabs][ActivityTabsDemo]aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-261">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="c765b-262">Stammaktivitäten</span><span class="sxs-lookup"><span data-stu-id="c765b-262">Root activities</span></span>   

<span data-ttu-id="c765b-263">Im folgenden finden Sie eine Erläuterung des Konzepts der **Stammaktivitäten** , das auf der Registerkarte " **anrufstruktur** ", " **Bottom-up-** Registerkarte" und " **Ereignisprotokoll** Abschnitte" erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="c765b-263">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="c765b-264">Stammaktivitäten sind solche, die dazu führen, dass der Browser einige Aufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c765b-264">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="c765b-265">Wenn Sie beispielsweise auf eine Seite klicken, löst der Browser eine `Event` Aktivität als Stammaktivität aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-265">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="c765b-266">, Die `Event` dazu führen können, dass ein Handler ausgeführt wird usw.</span><span class="sxs-lookup"><span data-stu-id="c765b-266">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="c765b-267">Im Flammen Diagramm des **Haupt** Abschnitts befinden sich die Stammaktivitäten am oberen Rand des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="c765b-267">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="c765b-268">In den Registerkarten " **anrufstruktur** " und " **Ereignisprotokoll** " sind Stammaktivitäten die Elemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="c765b-268">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="c765b-269">Ein Beispiel für Stammaktivitäten finden Sie auf [der Registerkarte anrufstruktur](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="c765b-269">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="c765b-270">Die Registerkarte "anrufstruktur"</span><span class="sxs-lookup"><span data-stu-id="c765b-270">The Call Tree tab</span></span>   

<span data-ttu-id="c765b-271">Verwenden Sie die Registerkarte **anrufstruktur** , um anzuzeigen, welche [Stammaktivitäten](#root-activities) die meiste Arbeit verursachen.</span><span class="sxs-lookup"><span data-stu-id="c765b-271">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="c765b-272">Die Registerkarte " **anrufstruktur** " zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c765b-272">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c765b-273">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c765b-273">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="c765b-274">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="c765b-274">Figure 17</span></span>  
> <span data-ttu-id="c765b-275">Die Registerkarte " **anrufstruktur** "</span><span class="sxs-lookup"><span data-stu-id="c765b-275">The **Call Tree** tab</span></span>  
> ![Die Registerkarte "anrufstruktur"][ImageCallTree]  

<span data-ttu-id="c765b-277">In [Abbildung 17](#figure-17)ist die oberste Ebene der Elemente in der Spalte **Aktivität** , wie `Evaluate Script` und `Parse HTML` sind Stammaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c765b-277">In [Figure 17](#figure-17), the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="c765b-278">Die Schachtelung stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="c765b-278">The nesting represents the call stack.</span></span>  <span data-ttu-id="c765b-279">Beispielsweise in [Abbildung 17](#figure-17), `Parse HTML` die verursacht hat, `Evaluate Script` `Compile Script` und `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="c765b-279">For example, in [Figure 17](#figure-17), `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="c765b-280">**Self time** steht für die in dieser Aktivität direkt verbrachte Zeit.</span><span class="sxs-lookup"><span data-stu-id="c765b-280">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="c765b-281">**Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-281">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="c765b-282">Klicken Sie auf **selbst Zeit**, **Gesamtzeit**oder **Aktivität** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-282">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="c765b-283">Verwenden Sie das Textfeld **Filtern** , um Ereignisse nach Aktivitätsname zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c765b-283">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="c765b-284">Standardmäßig ist das Menü **Gruppierung** auf **keine Gruppierung**eingestellt.</span><span class="sxs-lookup"><span data-stu-id="c765b-284">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="c765b-285">Verwenden Sie das Menü **Gruppierung** , um die aktivitätstabelle auf der Grundlage verschiedener Kriterien zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-285">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="c765b-286">Klicken Sie auf **schwerste** Stapel ![ anzeigen ][ImageShowHeaviestStackIcon] , um eine andere Tabelle rechts neben der **Aktivitäts** Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c765b-286">Click **Show Heaviest Stack** ![Show Heaviest Stack][ImageShowHeaviestStackIcon] to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="c765b-287">Klicken Sie auf eine Aktivität, um die **schwerste Stapel** Tabelle aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="c765b-287">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="c765b-288">Die **schwerste Stapel** Tabelle zeigt, welche untergeordneten Elemente der ausgewählten Aktivität am längsten ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="c765b-288">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="c765b-289">Die Registerkarte "Bottom-up"</span><span class="sxs-lookup"><span data-stu-id="c765b-289">The Bottom-Up tab</span></span>   

<span data-ttu-id="c765b-290">Verwenden Sie die Registerkarte " **Bottom-up** ", um anzuzeigen, welche Aktivitäten die meiste Zeit im Aggregat Direktaufnahmen.</span><span class="sxs-lookup"><span data-stu-id="c765b-290">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="c765b-291">Auf der Registerkarte **Bottom-up** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c765b-291">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c765b-292">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c765b-292">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="c765b-293">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="c765b-293">Figure 18</span></span>  
> <span data-ttu-id="c765b-294">Die Registerkarte " **Bottom-up** "</span><span class="sxs-lookup"><span data-stu-id="c765b-294">The **Bottom-Up** tab</span></span>  
> ![Die Registerkarte "Bottom-up"][ImageBottomUp]  

<span data-ttu-id="c765b-296">Sehen Sie im **Haupt** Abschnitt Flammen Diagramm in [Abbildung 18](#figure-18), dass fast die ganze Zeit ausgeführt wurde `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c765b-296">In the **Main** section flame chart of [Figure 18](#figure-18), see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="c765b-297">Die oberste Aktivität auf der Registerkarte " **Bottom-up** " in [Abbildung 18](#figure-18) ist `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="c765b-297">The top activity in the **Bottom-Up** tab of [Figure 18](#figure-18) is `Parse HTML`.</span></span>  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="c765b-298">Informationen dazu finden Sie auf der Registerkarte " **Bottom-up** " `Layout` .</span><span class="sxs-lookup"><span data-stu-id="c765b-298">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="c765b-299">Die Spalte **selbst Zeit** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität für alle Vorkommen aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-299">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="c765b-300">Die Spalte " **Gesamtzeit** " stellt die aggregierte Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-300">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="c765b-301">Die Registerkarte "Ereignisprotokoll"</span><span class="sxs-lookup"><span data-stu-id="c765b-301">The Event Log tab</span></span>   

<span data-ttu-id="c765b-302">Verwenden Sie die Registerkarte **Ereignisprotokoll** , um Aktivitäten in der Reihenfolge anzuzeigen, in der Sie während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-302">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="c765b-303">Die Registerkarte **Ereignisprotokoll** zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c765b-303">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="c765b-304">Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .</span><span class="sxs-lookup"><span data-stu-id="c765b-304">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

> ##### <span data-ttu-id="c765b-305">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="c765b-305">Figure 19</span></span>  
> <span data-ttu-id="c765b-306">Die Registerkarte " **Ereignisprotokoll** "</span><span class="sxs-lookup"><span data-stu-id="c765b-306">The **Event Log** tab</span></span>  
> ![Die Registerkarte "Ereignisprotokoll"][ImageEventLog]  

<span data-ttu-id="c765b-308">Die Spalte **Anfangszeit** steht für den Punkt, an dem die Aktivität gestartet wurde, relativ zum Anfang der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c765b-308">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="c765b-309">Beispielsweise bedeutet die Startzeit `175.7 ms` für das ausgewählte Element in [Abbildung 19](#figure-19) , dass die Aktivität nach Beginn der Aufzeichnung 175,7 ms gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="c765b-309">For example, the start time of `175.7 ms` for the selected item in [Figure 19](#figure-19) means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="c765b-310">Die Spalte **selbst Zeit** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-310">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="c765b-311">Die Spalten **Gesamtzeit** stellt die Zeit dar, die direkt in dieser Aktivität oder in einem der untergeordneten Elemente aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-311">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="c765b-312">Klicken Sie auf **Startzeit**, **selbst Zeit**oder **Gesamtzeit** , um die Tabelle nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-312">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="c765b-313">Verwenden Sie das Textfeld **Filtern** , um Aktivitäten nach Namen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c765b-313">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="c765b-314">Verwenden Sie das Menü " **Dauer** ", um alle Aktivitäten zu filtern, die weniger als 1 MS oder 15 MS dauerte.</span><span class="sxs-lookup"><span data-stu-id="c765b-314">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="c765b-315">Standardmäßig ist das Menü **Dauer** auf **alle**eingestellt, was bedeutet, dass alle Aktivitäten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c765b-315">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="c765b-316">Deaktivieren Sie die Kontrollkästchen **Lade**-, **Skripting**-, **Rendering**-oder **Painting** , um alle Aktivitäten aus diesen Kategorien zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c765b-316">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="c765b-317">Anzeigen der GPU-Aktivität</span><span class="sxs-lookup"><span data-stu-id="c765b-317">View GPU activity</span></span>   

<span data-ttu-id="c765b-318">Zeigen Sie die GPU-Aktivität im Abschnitt **GPU** an.</span><span class="sxs-lookup"><span data-stu-id="c765b-318">View GPU activity in the **GPU** section.</span></span>  

> ##### <span data-ttu-id="c765b-319">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="c765b-319">Figure 20</span></span>  
> <span data-ttu-id="c765b-320">Der **GPU** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c765b-320">The **GPU** section</span></span>  
> ![Der GPU-Abschnitt][ImageGpu]  

### <span data-ttu-id="c765b-322">Raster Aktivität anzeigen</span><span class="sxs-lookup"><span data-stu-id="c765b-322">View raster activity</span></span>   

<span data-ttu-id="c765b-323">Raster Aktivitäten im **Raster** Abschnitt anzeigen</span><span class="sxs-lookup"><span data-stu-id="c765b-323">View raster activity in the **Raster** section.</span></span>  

> ##### <span data-ttu-id="c765b-324">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="c765b-324">Figure 21</span></span>  
> <span data-ttu-id="c765b-325">Der **Raster** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c765b-325">The **Raster** section</span></span>  
> ![Der Raster Abschnitt][ImageRaster]  

### <span data-ttu-id="c765b-327">Anzeigen von Interaktionen</span><span class="sxs-lookup"><span data-stu-id="c765b-327">View interactions</span></span>   

<span data-ttu-id="c765b-328">Verwenden Sie den Abschnitt **Interaktionen** , um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-328">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

> ##### <span data-ttu-id="c765b-329">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="c765b-329">Figure 22</span></span>  
> <span data-ttu-id="c765b-330">Abschnitt " **Interaktionen** "</span><span class="sxs-lookup"><span data-stu-id="c765b-330">The **Interactions** section</span></span>  
> ![Abschnitt "Interaktionen"][ImageInteractions]  

<span data-ttu-id="c765b-332">Eine rote Zeile am unteren Rand einer Interaktion stellt die Zeit dar, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="c765b-332">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="c765b-333">Klicken Sie auf eine Interaktion, um weitere Informationen dazu auf der Registerkarte **Zusammenfassung** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c765b-333">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="c765b-334">Analysieren von Frames pro Sekunde (fps)</span><span class="sxs-lookup"><span data-stu-id="c765b-334">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="c765b-335">DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:</span><span class="sxs-lookup"><span data-stu-id="c765b-335">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="c765b-336">Verwenden Sie [das **fps** -Diagramm](#the-fps-chart) , um einen Überblick über fps über die Dauer der Aufzeichnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c765b-336">Use [the **FPS** chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="c765b-337">Verwenden Sie [den Abschnitt **Frames** ](#the-frames-section) , um anzuzeigen, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-337">Use [the **Frames** section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="c765b-338">Verwenden Sie das **fps-Messgerät** für eine echt Zeitschätzung von fps während der Ausführung der Seite.</span><span class="sxs-lookup"><span data-stu-id="c765b-338">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c765b-339">Informationen dazu finden Sie unter [Anzeigen von Frames pro Sekunde in Echtzeit mit dem FPS-Meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="c765b-339">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  

#### <span data-ttu-id="c765b-340">Das fps-Diagramm</span><span class="sxs-lookup"><span data-stu-id="c765b-340">The FPS chart</span></span>   

<span data-ttu-id="c765b-341">Das **fps** -Diagramm bietet eine Übersicht über die Framerate für die Dauer einer Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c765b-341">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="c765b-342">Je höher die grüne Leiste, desto besser die Framerate.</span><span class="sxs-lookup"><span data-stu-id="c765b-342">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="c765b-343">Eine rote Leiste oberhalb des **fps** -Diagramms ist eine Warnung, dass die Framerate so gering war, dass Sie möglicherweise die Benutzererfahrung beeinträchtigte.</span><span class="sxs-lookup"><span data-stu-id="c765b-343">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

> ##### <span data-ttu-id="c765b-344">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="c765b-344">Figure 23</span></span>  
> <span data-ttu-id="c765b-345">Das fps-Diagramm</span><span class="sxs-lookup"><span data-stu-id="c765b-345">The FPS chart</span></span>  
> ![Das fps-Diagramm][ImageFpsChart]  

#### <span data-ttu-id="c765b-347">Der Abschnitt "Frames"</span><span class="sxs-lookup"><span data-stu-id="c765b-347">The Frames section</span></span>   

<span data-ttu-id="c765b-348">Im Abschnitt **Frames** erfahren Sie genau, wie lange ein bestimmter Frame aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="c765b-348">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="c765b-349">Zeigen Sie mit der Maus auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c765b-349">Hover over a frame to view a tooltip with more information about it.</span></span>  

> ##### <span data-ttu-id="c765b-350">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="c765b-350">Figure 24</span></span>  
> <span data-ttu-id="c765b-351">Bewegen des Mauszeigers über einen Frame</span><span class="sxs-lookup"><span data-stu-id="c765b-351">Hovering over a frame</span></span>  
> ![Bewegen des Mauszeigers über einen Frame][ImageFramesSection]  

<span data-ttu-id="c765b-353">Klicken Sie auf einen Frame, um auf der Registerkarte **Zusammenfassung** noch weitere Informationen zu dem Frame anzuzeigen.  DevTools konturiert den markierten Frame in blau.</span><span class="sxs-lookup"><span data-stu-id="c765b-353">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

> ##### <span data-ttu-id="c765b-354">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="c765b-354">Figure 25</span></span>  
> <span data-ttu-id="c765b-355">Anzeigen eines Frames auf der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c765b-355">Viewing a frame in the **Summary** tab</span></span>  
> ![Anzeigen eines Frames auf der Registerkarte "Zusammenfassung"][ImageFrameSummary]  

### <span data-ttu-id="c765b-357">Anzeigen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="c765b-357">View network requests</span></span>   

<span data-ttu-id="c765b-358">Erweitern Sie den Abschnitt **Netzwerk** , um einen Wasserfall von Netzwerkanforderungen anzuzeigen, die während der Aufzeichnung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c765b-358">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

> ##### <span data-ttu-id="c765b-359">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="c765b-359">Figure 26</span></span>  
> <span data-ttu-id="c765b-360">Der Abschnitt " **Netzwerk** "</span><span class="sxs-lookup"><span data-stu-id="c765b-360">The **Network** section</span></span>  
> ![Der Abschnitt "Netzwerk"][ImageNetworkRequest]  

<span data-ttu-id="c765b-362">Anforderungen werden wie folgt farblich gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="c765b-362">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="c765b-363">HTML: blau</span><span class="sxs-lookup"><span data-stu-id="c765b-363">HTML: Blue</span></span>  
*   <span data-ttu-id="c765b-364">CSS: lila</span><span class="sxs-lookup"><span data-stu-id="c765b-364">CSS: Purple</span></span>  
*   <span data-ttu-id="c765b-365">JS: gelb</span><span class="sxs-lookup"><span data-stu-id="c765b-365">JS: Yellow</span></span>  
*   <span data-ttu-id="c765b-366">Bilder: grün</span><span class="sxs-lookup"><span data-stu-id="c765b-366">Images: Green</span></span>  

<span data-ttu-id="c765b-367">Klicken Sie auf eine Anfrage, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  So zeigt beispielsweise in [Abbildung 26](#figure-26) auf der Registerkarte " **Zusammenfassung** " Weitere Informationen zur blauen Anforderung an, die im Abschnitt " **Netzwerk** " ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c765b-367">Click on a request to view more information about it in the **Summary** tab.  For example, in [Figure 26](#figure-26) the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="c765b-368">Ein dunkelblaues Quadrat in der oberen linken Ecke einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.</span><span class="sxs-lookup"><span data-stu-id="c765b-368">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="c765b-369">Ein helleres blaues Quadrat bedeutet niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="c765b-369">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="c765b-370">In [Abbildung 26](#figure-26) ist beispielsweise die blaue, ausgewählte Anforderung mit höherer Priorität markiert, und die grüne darunter hat eine niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="c765b-370">For example, in [Figure 26](#figure-26) the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="c765b-371">In [Abbildung 27](#figure-27)wird die Anforderung `www.bing.com` durch eine Zeile auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Teil und einem hellen Teil sowie eine Zeile auf der rechten Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c765b-371">In [Figure 27](#figure-27), the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="c765b-372">[Abbildung 28](#figure-28) zeigt die entsprechende Darstellung der gleichen Anforderung auf der Registerkarte **Anzeige** Dauer des **Netzwerk** Panels.</span><span class="sxs-lookup"><span data-stu-id="c765b-372">[Figure 28](#figure-28) shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="c765b-373">Hier sehen Sie, wie diese beiden Darstellungen einander zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="c765b-373">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="c765b-374">Die linke Zeile ist alles bis zur `Connection Start` Gruppe von Ereignissen inklusive.</span><span class="sxs-lookup"><span data-stu-id="c765b-374">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="c765b-375">Mit anderen Worten: Es ist alles vor `Request Sent` , exklusiv.</span><span class="sxs-lookup"><span data-stu-id="c765b-375">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="c765b-376">Der helle Bereich der Leiste ist `Request Sent` und `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="c765b-376">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="c765b-377">Der dunkle Teil der Leiste ist `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="c765b-377">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="c765b-378">Die richtige Zeile ist im Wesentlichen die Zeit, die auf den Hauptthread wartet.</span><span class="sxs-lookup"><span data-stu-id="c765b-378">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="c765b-379">Diese wird auf der Registerkarte **Anzeige** Dauer nicht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c765b-379">This is not represented in the **Timing** tab.</span></span>  

> ##### <span data-ttu-id="c765b-380">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="c765b-380">Figure 27</span></span>  
> <span data-ttu-id="c765b-381">Die Zeile-Balken-Darstellung der `www.bing.com` Anforderung</span><span class="sxs-lookup"><span data-stu-id="c765b-381">The line-bar representation of the `www.bing.com` request</span></span>  
> ![Die Zeile-Balken-Darstellung der www.Bing.com-Anforderung][ImageLineBar]  

> ##### <span data-ttu-id="c765b-383">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="c765b-383">Figure 28</span></span>  
> <span data-ttu-id="c765b-384">Die Darstellung der Anforderung auf der Registerkarte " **Anzeige** Dauer" `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="c765b-384">The **Timing** tab representation of the `www.bing.com` request</span></span>  
> ![Der Abschnitt "Netzwerk"][ImageTiming]  

### <span data-ttu-id="c765b-386">Anzeigen von Speicher Metriken</span><span class="sxs-lookup"><span data-stu-id="c765b-386">View memory metrics</span></span>   

<span data-ttu-id="c765b-387">Aktivieren Sie das Kontrollkästchen **Speicher** , um Speicher Metriken aus der letzten Aufzeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c765b-387">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

> ##### <span data-ttu-id="c765b-388">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="c765b-388">Figure 29</span></span>  
> <span data-ttu-id="c765b-389">Das Kontrollkästchen " **Speicher** "</span><span class="sxs-lookup"><span data-stu-id="c765b-389">The **Memory** checkbox</span></span>  
> ![Das Kontrollkästchen "Speicher"][ImageMemory]  

<span data-ttu-id="c765b-391">DevTools zeigt ein neues **Speicher** Diagramm über der Registerkarte " **Zusammenfassung** " an.  Es gibt auch ein neues Diagramm unter dem **Netz** Diagramm, das als **Heap**bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c765b-391">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="c765b-392">Das **Heap** Diagramm bietet dieselben Informationen wie die **js-heaplinie** im **Speicher** Diagramm.</span><span class="sxs-lookup"><span data-stu-id="c765b-392">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

> ##### <span data-ttu-id="c765b-393">Abbildung 30</span><span class="sxs-lookup"><span data-stu-id="c765b-393">Figure 30</span></span>  
> <span data-ttu-id="c765b-394">Speicher Metriken oberhalb der Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="c765b-394">Memory metrics, above the **Summary** tab</span></span>  
> ![Speicher Metriken][ImageMemoryMetrics]  

<span data-ttu-id="c765b-396">Die farbigen Linien auf dem Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c765b-396">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="c765b-397">Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie aus dem Diagramm auszublenden.</span><span class="sxs-lookup"><span data-stu-id="c765b-397">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="c765b-398">Das Diagramm zeigt nur den Bereich der Aufzeichnung an, der aktuell markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c765b-398">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="c765b-399">In [Abbildung 30](#figure-30)zeigt das **Speicher** Diagramm beispielsweise nur die Speicherauslastung von der 400 MS-Marke bis zum 1750 MS Mark.</span><span class="sxs-lookup"><span data-stu-id="c765b-399">For example, in [Figure 30](#figure-30), the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="c765b-400">Anzeigen der Dauer eines Teils einer Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="c765b-400">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="c765b-401">Wenn Sie einen Abschnitt wie " **Netzwerk** " oder " **Main**" analysieren, benötigen Sie manchmal eine genauere Einschätzung, wie lange bestimmte Ereignisse dauerte.</span><span class="sxs-lookup"><span data-stu-id="c765b-401">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="c765b-402">Halten `Shift` , klicken und halten Sie, und ziehen Sie nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c765b-402">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="c765b-403">Am unteren Rand Ihrer Auswahl zeigt devtools an, wie lange dieser Teil dauerte.</span><span class="sxs-lookup"><span data-stu-id="c765b-403">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

> ##### <span data-ttu-id="c765b-404">Abbildung 31</span><span class="sxs-lookup"><span data-stu-id="c765b-404">Figure 31</span></span>  
> <span data-ttu-id="c765b-405">Der `9.47ms` Zeitstempel am unteren Rand des markierten Abschnitts gibt an, wie lange dieser Teil dauerte</span><span class="sxs-lookup"><span data-stu-id="c765b-405">The `9.47ms` timestamp at the bottom of the selected portion indicates how long that portion took</span></span>  
> ![Anzeigen der Dauer eines Teils einer Aufzeichnung][ImageDuration]  

### <span data-ttu-id="c765b-407">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="c765b-407">View a screenshot</span></span>   

<span data-ttu-id="c765b-408">Informationen zum Aktivieren von Screenshots finden Sie unter [Aufzeichnen von Screenshots während der Aufzeichnung](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="c765b-408">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="c765b-409">Zeigen Sie mit der Maus auf die **Übersicht** , um einen Screenshot zu sehen, wie die Seite während dieses Moments der Aufzeichnung aussah.</span><span class="sxs-lookup"><span data-stu-id="c765b-409">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="c765b-410">Die **Übersicht** ist der Abschnitt mit den Diagrammen **CPU**, **fps**und **net** .</span><span class="sxs-lookup"><span data-stu-id="c765b-410">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

> ##### <span data-ttu-id="c765b-411">Abbildung 32</span><span class="sxs-lookup"><span data-stu-id="c765b-411">Figure 32</span></span>  
> <span data-ttu-id="c765b-412">Anzeigen eines Screenshots</span><span class="sxs-lookup"><span data-stu-id="c765b-412">Viewing a screenshot</span></span>  
> ![Anzeigen eines Screenshots][ImageViewScreenshot]  

<span data-ttu-id="c765b-414">Sie können Screenshots auch anzeigen, indem Sie im Abschnitt **Frames** auf einen Frame klicken.</span><span class="sxs-lookup"><span data-stu-id="c765b-414">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="c765b-415">DevTools zeigt eine kleine Version des Screenshots auf der Registerkarte " **Zusammenfassung** " an.</span><span class="sxs-lookup"><span data-stu-id="c765b-415">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

> ##### <span data-ttu-id="c765b-416">Abbildung 33</span><span class="sxs-lookup"><span data-stu-id="c765b-416">Figure 33</span></span>  
> <span data-ttu-id="c765b-417">Nachdem Sie auf den `233.9ms` Frame im Abschnitt **Frames** geklickt haben, wird der Screenshot für diesen Frame auf der Registerkarte **Zusammenfassung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c765b-417">After clicking the `233.9ms` frame in the **Frames** section, the screenshot for that frame is displayed in the **Summary** tab</span></span>  
> ![Anzeigen eines Screenshots auf der Registerkarte "Zusammenfassung"][ImageFrameScreenshotSummary]  

<span data-ttu-id="c765b-419">Klicken Sie auf der Registerkarte **Zusammenfassung** auf die Miniaturansicht, um den Screenshot zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="c765b-419">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

> ##### <span data-ttu-id="c765b-420">Abbildung 34</span><span class="sxs-lookup"><span data-stu-id="c765b-420">Figure 34</span></span>  
> <span data-ttu-id="c765b-421">Nachdem Sie auf der Registerkarte " **Zusammenfassung** " auf die Miniaturansicht geklickt haben, vergrößert devtools den Screenshot.</span><span class="sxs-lookup"><span data-stu-id="c765b-421">After clicking the thumbnail in the **Summary** tab, DevTools zooms in on the screenshot</span></span>  
> ![Vergrößern eines Screenshots über die Registerkarte "Zusammenfassung"][ImageFrameScreenshotZoom]  

### <span data-ttu-id="c765b-423">Informationen zu Layern anzeigen</span><span class="sxs-lookup"><span data-stu-id="c765b-423">View layers information</span></span>   

<span data-ttu-id="c765b-424">So zeigen Sie erweiterte Folieninformationen zu einem Frame an:</span><span class="sxs-lookup"><span data-stu-id="c765b-424">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="c765b-425">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="c765b-425">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c765b-426">Wählen Sie im Abschnitt **Frames** einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-426">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="c765b-427">DevTools zeigt Informationen zu den Ebenen auf der Registerkarte "neue **Ebenen** " neben der Registerkarte " **Ereignisprotokoll** " an.</span><span class="sxs-lookup"><span data-stu-id="c765b-427">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    > ##### <span data-ttu-id="c765b-428">Abbildung 35</span><span class="sxs-lookup"><span data-stu-id="c765b-428">Figure 35</span></span>  
    > <span data-ttu-id="c765b-429">Der Bereich " **Ebenen** "</span><span class="sxs-lookup"><span data-stu-id="c765b-429">The **Layers** pane</span></span>  
    > ![Der Bereich "Ebenen"][ImageLayers]  
    
<span data-ttu-id="c765b-431">Zeigen Sie mit der Maus auf eine Ebene, um Sie im Diagramm hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="c765b-431">Hover over a layer to highlight it in the diagram.</span></span>  

> ##### <span data-ttu-id="c765b-432">Abbildung 36</span><span class="sxs-lookup"><span data-stu-id="c765b-432">Figure 36</span></span>  
> <span data-ttu-id="c765b-433">Highlighting Layer **#39**</span><span class="sxs-lookup"><span data-stu-id="c765b-433">Highlighting layer **#39**</span></span>  
> ![Markieren eines Layers][ImageLayerHover]  

<span data-ttu-id="c765b-435">So verschieben Sie das Diagramm:</span><span class="sxs-lookup"><span data-stu-id="c765b-435">To move the diagram:</span></span>  

*   <span data-ttu-id="c765b-436">Klicken **Sie auf Schwenkmodus** ![ ][ImagePanModeIcon] , um entlang der X-und Y-Achse zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-436">Click **Pan Mode** ![Pan Mode][ImagePanModeIcon] to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="c765b-437">Klicken **Sie auf** Rotationsmodus drehen ![ ][ImageRotateModeIcon] , um entlang der Z-Achse zu drehen.</span><span class="sxs-lookup"><span data-stu-id="c765b-437">Click **Rotate Mode** ![Rotate Mode][ImageRotateModeIcon] to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="c765b-438">Klicken Sie auf **Transform** ![ -Transformation zurücksetzen ][ImageResetTransformIcon] , um das Diagramm auf die ursprüngliche Position zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c765b-438">Click **Reset Transform** ![Reset Transform][ImageResetTransformIcon] to reset the diagram to the original position.</span></span>  

### <span data-ttu-id="c765b-439">Anzeigen des Paint-Profilers</span><span class="sxs-lookup"><span data-stu-id="c765b-439">View paint profiler</span></span>   

<span data-ttu-id="c765b-440">So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:</span><span class="sxs-lookup"><span data-stu-id="c765b-440">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="c765b-441">[Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="c765b-441">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="c765b-442">Wählen Sie im **Haupt** Abschnitt ein **Paint** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="c765b-442">Select a **Paint** event in the **Main** section.</span></span>  
    
    > ##### <span data-ttu-id="c765b-443">Abbildung 37</span><span class="sxs-lookup"><span data-stu-id="c765b-443">Figure 37</span></span>  
    > <span data-ttu-id="c765b-444">Die Registerkarte " **Paint-Profiler** "</span><span class="sxs-lookup"><span data-stu-id="c765b-444">The **Paint Profiler** tab</span></span>  
    > ![Die Registerkarte "Paint-Profiler"][ImagePaintProfiler]  
    
## <span data-ttu-id="c765b-446">Analysieren der Renderingleistung mit der Registerkarte "Rendern"</span><span class="sxs-lookup"><span data-stu-id="c765b-446">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="c765b-447">Verwenden Sie die Features der Registerkarte " **Rendern** ", um die Renderingleistung Ihrer Seite zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c765b-447">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="c765b-448">So öffnen Sie die Registerkarte " **Rendering** ":</span><span class="sxs-lookup"><span data-stu-id="c765b-448">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="c765b-449">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="c765b-449">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="c765b-450">Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="c765b-450">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="c765b-451">DevTools zeigt die Registerkarte " **Rendering** " am unteren Rand des devtools-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="c765b-451">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    > ##### <span data-ttu-id="c765b-452">Abbildung 38</span><span class="sxs-lookup"><span data-stu-id="c765b-452">Figure 38</span></span>  
    > <span data-ttu-id="c765b-453">Die Registerkarte " **Rendern** "</span><span class="sxs-lookup"><span data-stu-id="c765b-453">The **Rendering** tab</span></span>  
    > ![Die Registerkarte "Rendern"][ImageRenderingTab]  
    
### <span data-ttu-id="c765b-455">Anzeigen von Frames pro Sekunde in Echtzeit mit dem fps-Messgerät</span><span class="sxs-lookup"><span data-stu-id="c765b-455">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="c765b-456">Das **fps-Messgerät** ist ein Overlay, das in der oberen rechten Ecke des Viewports angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c765b-456">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="c765b-457">Bei der Ausführung der Seite wird eine Echtzeit-Schätzung von fps bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c765b-457">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="c765b-458">So öffnen Sie das **fps-Messgerät**:</span><span class="sxs-lookup"><span data-stu-id="c765b-458">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="c765b-459">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-459">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c765b-460">Aktivieren Sie das Kontrollkästchen **FPS-Meter** .</span><span class="sxs-lookup"><span data-stu-id="c765b-460">Enable the **FPS Meter** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="c765b-461">Abbildung 39</span><span class="sxs-lookup"><span data-stu-id="c765b-461">Figure 39</span></span>  
    > <span data-ttu-id="c765b-462">Das fps-Messgerät</span><span class="sxs-lookup"><span data-stu-id="c765b-462">The FPS meter</span></span>  
    > ![Das fps-Messgerät][ImageFpsMeter]  
    
### <span data-ttu-id="c765b-464">Anzeigen von Zeichnungs Ereignissen in Echtzeit mit Farb blinken</span><span class="sxs-lookup"><span data-stu-id="c765b-464">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="c765b-465">Verwenden Sie das Farb blinken, um eine Echtzeitansicht aller Paint-Ereignisse auf der Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c765b-465">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="c765b-466">Jedes Mal, wenn ein Teil der Seite neu gestrichen wird, wird der Abschnitt in devtools in grün umrissen.</span><span class="sxs-lookup"><span data-stu-id="c765b-466">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="c765b-467">So aktivieren Sie die Farb Blinkfunktion:</span><span class="sxs-lookup"><span data-stu-id="c765b-467">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="c765b-468">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-468">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c765b-469">Aktivieren Sie das Kontrollkästchen " **Farbe blinkt** ".</span><span class="sxs-lookup"><span data-stu-id="c765b-469">Enable the **Paint Flashing** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="c765b-470">Abbildung 40</span><span class="sxs-lookup"><span data-stu-id="c765b-470">Figure 40</span></span>  
    > **<span data-ttu-id="c765b-471">Malen blinkt</span><span class="sxs-lookup"><span data-stu-id="c765b-471">Paint Flashing</span></span>**  
    > ![Malen blinkt][ImagePaintFlashing]  
    
### <span data-ttu-id="c765b-473">Anzeigen einer Überlagerung von Ebenen mit Ebenen Rändern</span><span class="sxs-lookup"><span data-stu-id="c765b-473">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="c765b-474">Verwenden Sie **Layer-Rahmen** , um eine Überlagerung von Layer-Rändern und Kacheln oben auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c765b-474">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="c765b-475">So aktivieren Sie Layer-Rahmen:</span><span class="sxs-lookup"><span data-stu-id="c765b-475">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="c765b-476">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-476">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c765b-477">Aktivieren Sie das Kontrollkästchen **Layer-Rahmen** .</span><span class="sxs-lookup"><span data-stu-id="c765b-477">Enable the **Layer Borders** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="c765b-478">Abbildung 41</span><span class="sxs-lookup"><span data-stu-id="c765b-478">Figure 41</span></span>  
    > **<span data-ttu-id="c765b-479">Folienrahmen</span><span class="sxs-lookup"><span data-stu-id="c765b-479">Layer Borders</span></span>**  
    > ![Folienrahmen][ImageLayerBorders]  
    
<span data-ttu-id="c765b-481">[`debug_colors.cc`][ChromiumDebugColors]Eine Erläuterung der Farbcodierungen finden Sie in den Kommentaren in.</span><span class="sxs-lookup"><span data-stu-id="c765b-481">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="c765b-482">Suchen von Scroll-Leistungsproblemen in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="c765b-482">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="c765b-483">Verwenden Sie Leistungsprobleme beim Scrollen, um Elemente der Seite zu identifizieren, die Ereignislistener in Bezug auf den Bildlauf aufweisen, die die Leistung der Seite beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="c765b-483">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="c765b-484">DevTools beschreibt die potenziell problematischen Elemente in Teal.</span><span class="sxs-lookup"><span data-stu-id="c765b-484">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="c765b-485">So zeigen Sie Bild Lauf Leistungsprobleme an:</span><span class="sxs-lookup"><span data-stu-id="c765b-485">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="c765b-486">Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="c765b-486">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="c765b-487">Aktivieren Sie das Kontrollkästchen **Scrolling Performance Issues** .</span><span class="sxs-lookup"><span data-stu-id="c765b-487">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
 
    > ##### <span data-ttu-id="c765b-488">Abbildung 42</span><span class="sxs-lookup"><span data-stu-id="c765b-488">Figure 42</span></span>  
    > <span data-ttu-id="c765b-489">**Probleme mit der Bildlaufleistung** deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="c765b-489">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    > ![Probleme mit der Bildlaufleistung deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Abbildung 1: aufzeichnen"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Abbildung 2: Seite "Aktualisieren""  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Abbildung 3: Laden einer Seiten Aufzeichnung"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Abbildung 4: das Kontrollkästchen "Screenshots""  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Abbildung 5: Sammeln von Garbage"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Abbildung 6: Abschnitt "Aufnahmeeinstellungen""  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Abbildung 7: ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Abbildung 8: ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Abbildung 9: Speichern des Profils"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Abbildung 10: Laden eines Profils"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Abbildung 11: Löschen der Aufzeichnung"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Abbildung 12: Ziehen des Mauszeigers über die Übersicht zum Zoomen"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Abbildung 13: Suchfeld"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Abbildung 14: der Hauptabschnitt"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Abbildung 15: Weitere Informationen zur anonymen Funktion auf der Registerkarte "Zusammenfassung""  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Abbildung 16: ein Flammen Diagramm"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Abbildung 17: die Registerkarte "anrufstruktur""  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Abbildung 18: die Registerkarte "Bottom-up""  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Abbildung 19: Registerkarte "Ereignisprotokoll""  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Abbildung 20: der GPU-Abschnitt"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Abbildung 21: der Raster Abschnitt"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Abbildung 22: Abschnitt "Interaktionen""  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Abbildung 23: das FPS-Diagramm"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Abbildung 24: Bewegen des Mauszeigers über einen Frame"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Abbildung 25: Anzeigen eines Frames auf der Registerkarte "Zusammenfassung""  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Abbildung 26: der Abschnitt "Netzwerk""  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Abbildung 27: die Linien leisten Darstellung der www.Bing.com-Anforderung"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Abbildung 28: der Abschnitt "Netzwerk""  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Abbildung 29: das Kontrollkästchen "Speicher""  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Abbildung 30: Speicher Metriken"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Abbildung 31: Anzeigen der Dauer eines Teils einer Aufzeichnung"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Abbildung 32: Anzeigen eines Screenshots"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Abbildung 33: Anzeigen eines Screenshots auf der Registerkarte "Zusammenfassung""  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Abbildung 34: Vergrößern eines Screenshots über die Registerkarte "Zusammenfassung""  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Abbildung 35: der Bereich "Ebenen""  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Abbildung 36: Markieren eines Layers"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Abbildung 37: die Registerkarte "Paint-Profiler""  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Abbildung 38: die Registerkarte "Rendern""  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Abbildung 39: das FPS-Messgerät"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Abbildung 40: Farbe blinkt"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Abbildung 41: Ebenen Ränder"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Abbildung 42: Leistungsprobleme beim Scrollen deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können."  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Erste Schritte mit der Analyse der Laufzeitleistung"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demo zu Aktivitäts Registerkarten"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-Code Suche"  

> [!NOTE]
> <span data-ttu-id="c765b-538">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c765b-538">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c765b-539">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c765b-539">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c765b-541">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c765b-541">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
