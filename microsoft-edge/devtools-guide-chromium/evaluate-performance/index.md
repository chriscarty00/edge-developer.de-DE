---
title: Erste Schritte mit der Analyse der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611741"
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







# <span data-ttu-id="9fae6-103">Erste Schritte mit der Analyse der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="9fae6-103">Get Started With Analyzing Runtime Performance</span></span>   



> [!NOTE]
> <span data-ttu-id="9fae6-104">Informationen dazu, wie Sie Ihre Seiten schneller laden können, finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="9fae6-104">See [Optimize Website Speed][DevtoolsSpeedGetStarted] to learn how to make your pages load faster.</span></span>  

<span data-ttu-id="9fae6-105">Die Laufzeitleistung ist die Art und Weise, wie Ihre Seite ausführt, wenn Sie ausgeführt wird, im Gegensatz zum Laden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="9fae6-106">In diesem Lernprogramm erfahren Sie, wie Sie das Microsoft Edge devtools-Leistungs Panel verwenden, um die Runtime-Leistung zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9fae6-106">This tutorial teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="9fae6-107">Im Hinblick auf das **Schienen** Modell sind die in diesem Lernprogramm gelernten Kenntnisse hilfreich, um die Reaktions-, Animations-und Leerlaufphasen Ihrer Seite zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9fae6-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="9fae6-108">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="9fae6-108">Get started</span></span>   

<span data-ttu-id="9fae6-109">In diesem Lernprogramm öffnen Sie devtools auf einer Live Seite und verwenden den Leistungs Panel, um einen Leistungsengpass auf der Seite zu finden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-109">In this tutorial, you open DevTools on a live page and use the Performance panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="9fae6-110">Öffnen Sie Microsoft Edge im **InPrivate-Modus**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="9fae6-111">Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae6-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="9fae6-112">Wenn Sie beispielsweise viele Erweiterungen installiert haben, können diese Erweiterungen zu Lärm in ihren Leistungsmessungen führen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-112">For example, if you have a lot of extensions installed, those extensions might create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="9fae6-113">Laden Sie die folgende Seite in Ihrem InPrivate-Fenster.</span><span class="sxs-lookup"><span data-stu-id="9fae6-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="9fae6-114">Dies ist die Demo, die Sie profilieren werden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-114">This is the demo that you're going to profile.</span></span>  <span data-ttu-id="9fae6-115">Auf der Seite werden einige kleine Symbole angezeigt, die sich nach oben und unten bewegen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  <span data-ttu-id="9fae6-116">Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \), um devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-116">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-117">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="9fae6-117">Figure 1</span></span>  
    > <span data-ttu-id="9fae6-118">Die Demo auf der linken Seite und DevTools auf der rechten Seite</span><span class="sxs-lookup"><span data-stu-id="9fae6-118">The demo on the left, and DevTools on the right</span></span>  
    > ![Die Demo auf der linken Seite und DevTools auf der rechten Seite][ImageGetStarted]  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-120">Für die restlichen Screenshots wird devtools [in einem separaten Fenster Abdocken][DevtoolsCustomizePlacement] , damit Sie den Inhalt besser sehen können.</span><span class="sxs-lookup"><span data-stu-id="9fae6-120">For the rest of the screenshots, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] so that you can see the contents better.</span></span>  
    
### <span data-ttu-id="9fae6-121">Simulieren einer mobilen CPU</span><span class="sxs-lookup"><span data-stu-id="9fae6-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="9fae6-122">Mobile Geräte haben viel weniger Prozessorleistung als Desktops und Laptops.</span><span class="sxs-lookup"><span data-stu-id="9fae6-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="9fae6-123">Wenn Sie eine Seite profilieren, simulieren Sie mithilfe der CPU-Drosselung, wie Ihre Seite auf mobilen Geräten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae6-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="9fae6-124">Klicken Sie in devtools auf die Registerkarte **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="9fae6-124">In DevTools, click the **Performance** tab.</span></span>  
1.  <span data-ttu-id="9fae6-125">Stellen Sie sicher, dass das Kontrollkästchen **Screenshots** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9fae6-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="9fae6-126">Klicken Sie auf Aufnahmeeinstellungen für **aufnahmeeinstellungen** ![ ][ImageCaptureSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="9fae6-126">Click **Capture Settings** ![Capture Settings][ImageCaptureSettingsIcon].</span></span>  <span data-ttu-id="9fae6-127">DevTools zeigt Einstellungen in Bezug auf die Erfassung von Leistungs Metriken an.</span><span class="sxs-lookup"><span data-stu-id="9fae6-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="9fae6-128">Wählen Sie für **CPU**die Option **4X Verlangsamung**aus.</span><span class="sxs-lookup"><span data-stu-id="9fae6-128">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="9fae6-129">DevTools drosselt Ihre CPU so, dass Sie viermal langsamer als üblich ist.</span><span class="sxs-lookup"><span data-stu-id="9fae6-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-130">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="9fae6-130">Figure 2</span></span>  
    > <span data-ttu-id="9fae6-131">CPU-Drosselung</span><span class="sxs-lookup"><span data-stu-id="9fae6-131">CPU throttling</span></span>  
    > ![CPU-Drosselung][ImageCPUThrottling]  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-133">Wenn Sie beim Testen anderer Seiten sicherstellen möchten, dass Sie auf Low-End-mobilen Geräten gut funktionieren, legen Sie die CPU-Drosselung auf **6x Abschwächung**fest.</span><span class="sxs-lookup"><span data-stu-id="9fae6-133">When testing other pages, if you want to ensure that they work well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="9fae6-134">Diese Demo funktioniert nicht gut mit einer 6x Verlangsamung, sodass Sie nur eine vierfache Verlangsamung für Unterrichtszwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fae6-134">This demo doesn't work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="9fae6-135">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="9fae6-135">Set up the demo</span></span>  

<span data-ttu-id="9fae6-136">Es ist schwierig, eine Runtime Performance-Demo zu erstellen, die für alle Leser dieser Website konsistent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9fae6-136">It is hard to create a runtime performance demo that works consistently for all readers of this website.</span></span>  <span data-ttu-id="9fae6-137">In diesem Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung mit den Screenshots und Beschreibungen, die Sie in diesem Lernprogramm sehen, relativ konsistent ist, und zwar unabhängig von ihrem jeweiligen Setup.</span><span class="sxs-lookup"><span data-stu-id="9fae6-137">This section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions you see in this tutorial, regardless of your particular setup.</span></span>

1.  <span data-ttu-id="9fae6-138">Klicken **Sie auf Hinzufügen 10** , bis die blauen Symbole merklich langsamer als zuvor verschoben sind.</span><span class="sxs-lookup"><span data-stu-id="9fae6-138">Keep clicking **Add 10** until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="9fae6-139">Auf einem Highend-Computer kann es etwa 20 Klicks dauern.</span><span class="sxs-lookup"><span data-stu-id="9fae6-139">On a high-end machine, it may take about 20 clicks.</span></span>  
1.  <span data-ttu-id="9fae6-140">Klicken Sie auf **optimieren**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-140">Click **Optimize**.</span></span>  <span data-ttu-id="9fae6-141">Die blauen Symbole sollten sich schneller und reibungsloser bewegen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-141">The blue icons should move faster and more smoothly.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="9fae6-142">Wenn Sie zwischen den optimierten und nicht optimierten Versionen keinen nennenswerten Unterschied sehen, klicken Sie mehrmals auf **subtrahieren** , und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="9fae6-142">If you don't see a noticeable difference between the optimized and un-optimized versions, try clicking **Subtract 10** a few times and trying again.</span></span>  
    > <span data-ttu-id="9fae6-143">Wenn Sie zu viele blaue Symbole hinzufügen, werden Sie einfach die CPU ausweiten, und Sie werden keinen großen Unterschied in den Ergebnissen für die beiden Versionen sehen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-143">If you add too many blue icons, you're just going to max out the CPU and you're not going to see a major difference in the results for the two versions.</span></span>  

1.  <span data-ttu-id="9fae6-144">Klicken Sie auf **UN-Optimize**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-144">Click **Un-Optimize**.</span></span>  <span data-ttu-id="9fae6-145">Die blauen Symbole werden langsamer und mit mehr Jank wieder verschoben.</span><span class="sxs-lookup"><span data-stu-id="9fae6-145">The blue icons move slower and with more jank again.</span></span>  

### <span data-ttu-id="9fae6-146">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="9fae6-146">Record runtime performance</span></span>   

<span data-ttu-id="9fae6-147">Wenn Sie die optimierte Version der Seite ausgeführt haben, werden die blauen Symbole schneller verschoben.</span><span class="sxs-lookup"><span data-stu-id="9fae6-147">When you ran the optimized version of the page, the blue icons move faster.</span></span>  
<span data-ttu-id="9fae6-148">Weshalb?</span><span class="sxs-lookup"><span data-stu-id="9fae6-148">Why is that?</span></span>  <span data-ttu-id="9fae6-149">Beide Versionen sollen die Symbole in derselben Zeitdauer auf die gleiche Menge an Speicherplatz verschieben.</span><span class="sxs-lookup"><span data-stu-id="9fae6-149">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="9fae6-150">Nehmen Sie im Leistungs Panel eine Aufzeichnung auf, um zu erfahren, wie Sie den Leistungsengpass in der nicht optimierten Version erkennen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-150">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="9fae6-151">Klicken Sie in devtools auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="9fae6-151">In DevTools, click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="9fae6-152">DevTools erfasst Leistungs Metriken während der Ausführung der Seite.</span><span class="sxs-lookup"><span data-stu-id="9fae6-152">DevTools captures performance metrics as the page runs.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-153">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="9fae6-153">Figure 3</span></span> 
    > <span data-ttu-id="9fae6-154">Profilerstellung der Seite</span><span class="sxs-lookup"><span data-stu-id="9fae6-154">Profiling the page</span></span>  
    > ![Profilerstellung der Seite][ImagePageProfiling]  
    
1.  <span data-ttu-id="9fae6-156">Warten Sie ein paar Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-156">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="9fae6-157">Klicken Sie auf **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-157">Click **Stop**.</span></span>  <span data-ttu-id="9fae6-158">DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Leistungs Panel an.</span><span class="sxs-lookup"><span data-stu-id="9fae6-158">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-159">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="9fae6-159">Figure 4</span></span>  
    > <span data-ttu-id="9fae6-160">Die Ergebnisse des Profils</span><span class="sxs-lookup"><span data-stu-id="9fae6-160">The results of the profile</span></span>  
    > ![Die Ergebnisse des Profils][ImageProfileResults]  

<span data-ttu-id="9fae6-162">Wow, das ist eine überwältigende Menge an Daten.</span><span class="sxs-lookup"><span data-stu-id="9fae6-162">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="9fae6-163">Machen Sie sich keine Sorgen, es wird in Kürze sinnvoller sein.</span><span class="sxs-lookup"><span data-stu-id="9fae6-163">Don't worry, it'll all make more sense shortly.</span></span>  

## <span data-ttu-id="9fae6-164">Analysieren der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9fae6-164">Analyze the results</span></span>   

<span data-ttu-id="9fae6-165">Nachdem Sie die Leistung der Seite aufgezeichnet haben, können Sie messen, wie schlecht die Leistung der Seite ist, und die Ursachen ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9fae6-165">Once you've got a recording the performance of the page, you can measure how poor the performance of the page is, and find the any causes.</span></span>  

### <span data-ttu-id="9fae6-166">Analysieren von Frames pro Sekunde</span><span class="sxs-lookup"><span data-stu-id="9fae6-166">Analyze frames per second</span></span>  

<span data-ttu-id="9fae6-167">Die wichtigste Metrik zum Messen der Leistung einer Animation ist Frames pro Sekunde \ (fps \).</span><span class="sxs-lookup"><span data-stu-id="9fae6-167">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="9fae6-168">Benutzer sind zufrieden, wenn Animationen mit 60 fps ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-168">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="9fae6-169">Schauen Sie sich das **fps** -Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="9fae6-169">Look at the **FPS** chart.</span></span>  <span data-ttu-id="9fae6-170">Wenn Sie eine rote Leiste oberhalb von **fps**sehen, bedeutet dies, dass die Framerate so gering ist, dass Sie die Benutzerfreundlichkeit wahrscheinlich beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-170">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="9fae6-171">Je höher die grüne Leiste, desto höher der FPS-Wert.</span><span class="sxs-lookup"><span data-stu-id="9fae6-171">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-172">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="9fae6-172">Figure 5</span></span>  
    > <span data-ttu-id="9fae6-173">Das fps-Diagramm</span><span class="sxs-lookup"><span data-stu-id="9fae6-173">The FPS chart</span></span>  
    > ![Das fps-Diagramm][ImageFPSChart]  

1.  <span data-ttu-id="9fae6-175">Unterhalb des **fps** -Diagramms wird das **CPU** -Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-175">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="9fae6-176">Die Farben im **CPU** -Diagramm entsprechen den Farben auf der Registerkarte " **Zusammenfassung** " unten im Leistungsbereich.</span><span class="sxs-lookup"><span data-stu-id="9fae6-176">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="9fae6-177">Die Tatsache, dass das **CPU** -Diagramm Farb voll ist, bedeutet, dass die CPU während der Aufzeichnung ausgereizt wurde.</span><span class="sxs-lookup"><span data-stu-id="9fae6-177">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="9fae6-178">Wenn Sie sehen, dass die CPU über einen längeren Zeitraum ausgeschöpft ist, ist es ein Anhaltspunkt, wie Sie Möglichkeiten für eine geringere Arbeit finden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-178">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-179">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="9fae6-179">Figure 6</span></span>  
    > <span data-ttu-id="9fae6-180">Das CPU-Diagramm und die Registerkarte "Zusammenfassung"</span><span class="sxs-lookup"><span data-stu-id="9fae6-180">The CPU chart and Summary tab</span></span>  
    > ![Das CPU-Diagramm und die Registerkarte "Zusammenfassung"][ImageCPUSummary]  

1.  <span data-ttu-id="9fae6-182">Zeigen Sie mit der Maus auf die **fps**-, **CPU**-oder **net** -Diagramme.</span><span class="sxs-lookup"><span data-stu-id="9fae6-182">Hover your mouse over the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="9fae6-183">DevTools zeigt zu diesem Zeitpunkt einen Screenshot der Seite an.</span><span class="sxs-lookup"><span data-stu-id="9fae6-183">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="9fae6-184">Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="9fae6-184">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="9fae6-185">Dies wird als Scrubbing bezeichnet und ist hilfreich, um den Fortschritt von Animationen manuell zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9fae6-185">This is called scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-186">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="9fae6-186">Figure 7</span></span>  
    > <span data-ttu-id="9fae6-187">Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="9fae6-187">Viewing a screenshot of the page around the 2500ms mark of the recording</span></span>  
    > ![Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung][ImageViewingScreenshot]  

1.  <span data-ttu-id="9fae6-189">Zeigen Sie im Abschnitt **Frames** mit der Maus auf eines der grünen Quadrate.</span><span class="sxs-lookup"><span data-stu-id="9fae6-189">In the **Frames** section, hover your mouse over one of the green squares.</span></span>  <span data-ttu-id="9fae6-190">DevTools zeigt Ihnen die fps für diesen bestimmten Frame.</span><span class="sxs-lookup"><span data-stu-id="9fae6-190">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="9fae6-191">Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 fps.</span><span class="sxs-lookup"><span data-stu-id="9fae6-191">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-192">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="9fae6-192">Figure 8</span></span>  
    > <span data-ttu-id="9fae6-193">Bewegen des Mauszeigers über einen Frame</span><span class="sxs-lookup"><span data-stu-id="9fae6-193">Hovering over a frame</span></span>  
    > ![Bewegen des Mauszeigers über einen Frame][ImageFrameHover]  

<span data-ttu-id="9fae6-195">Natürlich ist es bei dieser Demo ziemlich offensichtlich, dass die Seite nicht gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9fae6-195">Of course, with this demo, it is pretty obvious that the page is not performing well.</span></span>  <span data-ttu-id="9fae6-196">In realen Szenarien ist es aber möglicherweise nicht so klar, dass alle diese Tools für Messungen praktisch sind.</span><span class="sxs-lookup"><span data-stu-id="9fae6-196">But in real scenarios, it may not be so clear, so having all of these tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="9fae6-197">Bonus: Öffnen des FPS-meters</span><span class="sxs-lookup"><span data-stu-id="9fae6-197">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="9fae6-198">Ein weiteres praktisches Tool ist das FPS-Messgerät, das in Echtzeit Schätzungen für FPS bereitstellt, während die Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae6-198">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="9fae6-199">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-199">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="9fae6-200">Beginnen `Rendering` Sie mit der Eingabe im Befehlsmenü, und wählen Sie **Rendering anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="9fae6-200">Start typing `Rendering` in the Command Menu and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="9fae6-201">Aktivieren Sie auf der Registerkarte **Rendern** die Option **FPS-Meter**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-201">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="9fae6-202">In der oberen rechten Ecke des Viewports wird eine neue Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-202">A new overlay appears in the top-right of your viewport.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-203">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="9fae6-203">Figure 9</span></span>  
    > <span data-ttu-id="9fae6-204">Das fps-Messgerät</span><span class="sxs-lookup"><span data-stu-id="9fae6-204">The FPS meter</span></span>  
    > ![Das fps-Messgerät][ImageFPSMeter]  

1.  <span data-ttu-id="9fae6-206">Deaktivieren Sie das **fps-Messgerät** , und drücken Sie `Escape` , um die Registerkarte **Rendern** zu schließen.  In diesem Lernprogramm verwenden Sie Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="9fae6-206">Disable the **FPS Meter** and press `Escape` to close the **Rendering** tab.  You won't be using it in this tutorial.</span></span>  

### <span data-ttu-id="9fae6-207">Ermitteln des Engpasses</span><span class="sxs-lookup"><span data-stu-id="9fae6-207">Find the bottleneck</span></span>  

<span data-ttu-id="9fae6-208">Nachdem Sie nun gemessen und überprüft haben, dass die Animation nicht gut funktioniert, müssen Sie die nächste Frage beantworten: Warum?</span><span class="sxs-lookup"><span data-stu-id="9fae6-208">Now that you've measured and verified that the animation is not performing well, the next question to answer is:  why?</span></span>  

1.  <span data-ttu-id="9fae6-209">Beachten Sie die Registerkarte Zusammenfassung.  Wenn keine Ereignisse ausgewählt sind, wird auf dieser Registerkarte eine Aufschlüsselung der Aktivitäten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-209">Note the summary tab.  When no events are selected, this tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="9fae6-210">Die Seite hat die meiste Zeit gerendert.</span><span class="sxs-lookup"><span data-stu-id="9fae6-210">The page spent most of its time rendering.</span></span>  <span data-ttu-id="9fae6-211">Da Leistung die Kunst ist, weniger Arbeit zu erledigen, besteht das Ziel darin, die Zeit zu verringern, die für das Rendern von Arbeit aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9fae6-211">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-212">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="9fae6-212">Figure 10</span></span>  
    > <span data-ttu-id="9fae6-213">Registerkarte "Zusammenfassung"</span><span class="sxs-lookup"><span data-stu-id="9fae6-213">The Summary tab</span></span>  
    > ![Registerkarte "Zusammenfassung"][ImageSummaryTab]  

1.  <span data-ttu-id="9fae6-215">Erweitern des **Haupt** Abschnitts</span><span class="sxs-lookup"><span data-stu-id="9fae6-215">Expand the **Main** section.</span></span>  <span data-ttu-id="9fae6-216">DevTools zeigt Ihnen im Laufe der Zeit ein Flammen Diagramm mit Aktivitäten auf dem Hauptthread.</span><span class="sxs-lookup"><span data-stu-id="9fae6-216">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="9fae6-217">Die x-Achse steht für die Aufzeichnung im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="9fae6-217">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="9fae6-218">Jeder Balken steht für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9fae6-218">Each bar represents an event.</span></span>  <span data-ttu-id="9fae6-219">Eine breitere Leiste bedeutet, dass das Ereignis länger dauerte.</span><span class="sxs-lookup"><span data-stu-id="9fae6-219">A wider bar means that event took longer.</span></span>  <span data-ttu-id="9fae6-220">Die y-Achse steht für die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="9fae6-220">The y-axis represents the call stack.</span></span>  <span data-ttu-id="9fae6-221">Wenn Ereignisse übereinander gestapelt angezeigt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="9fae6-221">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    > ##### <span data-ttu-id="9fae6-222">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="9fae6-222">Figure 11</span></span>  
    > <span data-ttu-id="9fae6-223">Der Hauptabschnitt</span><span class="sxs-lookup"><span data-stu-id="9fae6-223">The Main section</span></span>  
    > ![Der Hauptabschnitt][ImageMainSection]  

1.  <span data-ttu-id="9fae6-225">Die Aufzeichnung enthält viele Daten.</span><span class="sxs-lookup"><span data-stu-id="9fae6-225">There is a lot of data in the recording.</span></span>  <span data-ttu-id="9fae6-226">Vergrößern Sie ein einzelnes Ereignis, indem Sie mit der Maus auf die **Übersicht**klicken, halten und ziehen, wobei es sich um den Abschnitt mit den **fps**-, **CPU**-und **net** -Diagrammen handelt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-226">Zoom in on a single event by clicking, holding, and dragging your mouse over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="9fae6-227">Der **Haupt** Abschnitt und die Registerkarte " **Zusammenfassung** " zeigen nur Informationen für den ausgewählten Teil der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="9fae6-227">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    > ###### <span data-ttu-id="9fae6-228">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="9fae6-228">Figure 12</span></span>  
    > <span data-ttu-id="9fae6-229">Vergrößert auf ein einzelnes Ereignis</span><span class="sxs-lookup"><span data-stu-id="9fae6-229">Zoomed in on a single event</span></span>  
    > ![Vergrößert eines Ereignisses][ImageZoomedAnimation]  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-231">Eine weitere Möglichkeit zum Zoomen ist das Fokussieren des **Haupt** Abschnitts durch Klicken auf den Hintergrund oder Auswählen eines Ereignisses, und drücken Sie dann die `W` Tasten, und `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="9fae6-231">Another way to zoom is to focus the **Main** section by clicking its background or selecting an event, and then press the `W`, `A`, `S`, and `D` keys.</span></span>  
    
    1.  <span data-ttu-id="9fae6-232">Beachten Sie das rote Dreieck in der oberen rechten Ecke des Ereignisses **Animations Frame ausgelöst** .</span><span class="sxs-lookup"><span data-stu-id="9fae6-232">Note the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9fae6-233">Wenn Sie ein rotes Dreieck sehen, ist es eine Warnung, dass möglicherweise ein Problem im Zusammenhang mit diesem Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9fae6-233">Whenever you see a red triangle, it is a warning that there may be an issue related to this event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-234">Das **ausgelöste Animations Frame** -Ereignis tritt auf, wenn ein [ `requestAnimationFrame()` Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae6-234">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="9fae6-235">Klicken Sie auf das Ereignis **Animations Frame ausgelöst** .</span><span class="sxs-lookup"><span data-stu-id="9fae6-235">Click the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9fae6-236">Auf der Registerkarte " **Zusammenfassung** " werden nun Informationen zu diesem Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-236">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="9fae6-237">Beachten Sie den Link **Reveal** .</span><span class="sxs-lookup"><span data-stu-id="9fae6-237">Note the **Reveal** link.</span></span>  <span data-ttu-id="9fae6-238">Wenn Sie darauf klicken, wird devtools zum Hervorheben des Ereignisses veranlasst, das das ausgelöste **Animations Frame** initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="9fae6-238">Clicking that causes DevTools to highlight the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="9fae6-239">Beachten Sie auch den Link **app. js: 95** .</span><span class="sxs-lookup"><span data-stu-id="9fae6-239">Also note the **app.js:95** link.</span></span>  <span data-ttu-id="9fae6-240">Durch Klicken auf diese Schaltfläche springen Sie zur entsprechenden Zeile im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="9fae6-240">Clicking that jumps you to the relevant line in the source code.</span></span>
    
    > ##### <span data-ttu-id="9fae6-241">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="9fae6-241">Figure 13</span></span>  
    > <span data-ttu-id="9fae6-242">Weitere Informationen zum ausgelösten Animations Frame-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9fae6-242">More information about the Animation Frame Fired event</span></span>  
    > ![Weitere Informationen zum ausgelösten Animations Frame-Ereignis][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-244">Verwenden Sie nach dem Auswählen eines Ereignisses die Pfeiltasten, um die Ereignisse daneben auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-244">After selecting an event, use the arrow keys to select the events next to it.</span></span>  

1.  <span data-ttu-id="9fae6-245">Unter dem **app. Update** -Ereignis gibt es eine Reihe von lila Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-245">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="9fae6-246">Wenn Sie breiter waren, sieht es so aus, als ob jedes eine rote Dreiecks Farbe aufweist.</span><span class="sxs-lookup"><span data-stu-id="9fae6-246">If they were wider, it looks as though each one might have a red triangle on it.</span></span>  <span data-ttu-id="9fae6-247">Klicken Sie jetzt auf eines der lila **Layout** -Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9fae6-247">Click one of the purple **Layout** events now.</span></span>  <span data-ttu-id="9fae6-248">DevTools enthält weitere Informationen zu dem Ereignis auf der Registerkarte " **Zusammenfassung** ".  In der Tat gibt es eine Warnung zu erzwungenen Umläufen \ (ein weiteres Wort für das Layout \).</span><span class="sxs-lookup"><span data-stu-id="9fae6-248">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  

1.  <span data-ttu-id="9fae6-249">Klicken Sie auf der Registerkarte **Zusammenfassung** auf den Link **app. js: 71** unter **Layout erzwungen**.</span><span class="sxs-lookup"><span data-stu-id="9fae6-249">In the **Summary** tab, click the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="9fae6-250">DevTools führt Sie zu der Codezeile, die das Layout erzwungen hat.</span><span class="sxs-lookup"><span data-stu-id="9fae6-250">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    > ##### <span data-ttu-id="9fae6-251">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="9fae6-251">Figure 14</span></span>  
    > <span data-ttu-id="9fae6-252">Die Codezeile, die das erzwungene Layout verursacht hat</span><span class="sxs-lookup"><span data-stu-id="9fae6-252">The line of code that caused the forced layout</span></span>  
    > ![Die Codezeile, die das erzwungene Layout verursacht hat][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > <span data-ttu-id="9fae6-254">Das Problem mit diesem Code besteht darin, dass in jedem Animationsframe die Formatvorlage für jedes Symbol geändert und dann die Position der einzelnen Symbole auf der Seite abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae6-254">The problem with this code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="9fae6-255">Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob sich die einzelnen Symbolpositionen geändert haben, sodass das Symbol neu angeordnet werden muss, um seine Position zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-255">Because the styles changed, the browser doesn't know if each icon position changed, so it has to re-layout the icon in order to compute its position.</span></span>  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

<span data-ttu-id="9fae6-256">Da kommt doch einiges zusammen.</span><span class="sxs-lookup"><span data-stu-id="9fae6-256">Phew!</span></span>  <span data-ttu-id="9fae6-257">Das war viel zu erledigen, aber Sie haben jetzt eine solide Grundlage im grundlegenden Workflow zum Analysieren der Laufzeitleistung.</span><span class="sxs-lookup"><span data-stu-id="9fae6-257">That was a lot to take in, but you now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="9fae6-258">Gut Gemacht.</span><span class="sxs-lookup"><span data-stu-id="9fae6-258">Good job.</span></span>  

### <span data-ttu-id="9fae6-259">Bonus: Analysieren der optimierten Version</span><span class="sxs-lookup"><span data-stu-id="9fae6-259">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="9fae6-260">Klicken Sie unter Verwendung der soeben gelernten Workflows und Tools in der Demo auf **optimieren** , um den optimierten Code zu aktivieren, eine andere Leistungsaufnahme durchführen und dann die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9fae6-260">Using the workflows and tools that you just learned, click **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="9fae6-261">Von der verbesserten Framerate bis zur Reduzierung von Ereignissen im Flammen Diagramm im **Haupt** Abschnitt können Sie sehen, dass die optimierte Version der APP viel weniger Arbeit leistet, was zu einer besseren Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-261">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you can see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="9fae6-262">Auch diese "optimierte" Version ist nicht so toll, weil Sie immer noch die `top` Eigenschaft der einzelnen Symbole manipuliert.</span><span class="sxs-lookup"><span data-stu-id="9fae6-262">Even this "optimized" version isn't that great, because it still manipulates the `top` property of each icon.</span></span>  <span data-ttu-id="9fae6-263">Ein besserer Ansatz ist das Beibehalten von Eigenschaften, die sich nur auf die Compositing-Methode auswirken.</span><span class="sxs-lookup"><span data-stu-id="9fae6-263">A better approach is to stick to properties that only affect compositing.</span></span>  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="9fae6-264">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9fae6-264">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="9fae6-265">Um mit dem Leistungsumfang noch komfortabler zu werden, ist die Praxis perfekt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-265">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="9fae6-266">Versuchen Sie, ihre eigenen Seiten zu profilieren und die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9fae6-266">Try profiling your own pages and analyzing the results.</span></span>  <span data-ttu-id="9fae6-267">Wenn Sie Fragen zu ihren Ergebnissen haben, verwenden Sie das **Feedback** -Symbol, drücken Sie `Alt`  +  `Shift`  +  `I` auf Windows ( `Option`  +  `Shift`  +  `I` unter macOS) oder [tweeten Sie uns][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="9fae6-267">If you have any questions about your results, use the **Feedback** icon, press `Alt` + `Shift` + `I` on Windows (`Option` + `Shift` + `I` on macOS), or [tweet at us][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="9fae6-268">Fügen Sie Screenshots oder Links zu reproduzierbaren Seiten hinzu, falls möglich.</span><span class="sxs-lookup"><span data-stu-id="9fae6-268">Include screenshots or links to reproducible pages, if possible.</span></span>

> ##### <span data-ttu-id="9fae6-269">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="9fae6-269">Figure 15</span></span>
> <span data-ttu-id="9fae6-270">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="9fae6-270">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Das \* \* Feedback \* \*-Symbol in der Microsoft Edge-devtools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="9fae6-272">Schließlich gibt es viele Möglichkeiten, die Laufzeitleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9fae6-272">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="9fae6-273">In diesem Lernprogramm wurde auf einen bestimmten Animations Engpass eingegangen, der Ihnen eine gezielte Tour durch das Leistungs Panel ermöglicht, aber nur eine von vielen Engpässen, die Ihnen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="9fae6-273">This tutorial focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Abbildung 1: die Demo auf der linken Seite und DevTools auf der rechten Seite"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Abbildung 2: CPU-Drosselung"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Abbildung 3: Profilerstellung der Seite"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Abbildung 4: die Ergebnisse des Profils"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Abbildung 5: das FPS-Diagramm"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Abbildung 6: das CPU-Diagramm und die Registerkarte "Zusammenfassung", blau dargestellt"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Abbildung 7: Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Abbildung 8: Bewegen des Mauszeigers über einen Frame"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Abbildung 9: FPS-Messgerät"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Abbildung 10: Registerkarte "Zusammenfassung""  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Abbildung 11: der Hauptabschnitt"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Abbildung 12: vergrößert eines einzelnen Animations Frame-Ereignisses"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Abbildung 13: Weitere Informationen zum ausgelösten Animations Frame-Ereignis"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Abbildung 14: die Codezeile, die das erzwungene Layout verursacht hat"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Abbildung 15: das * * Feedback * *-Symbol in der Microsoft Edge-devtools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-Post a tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="9fae6-293">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fae6-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9fae6-294">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fae6-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9fae6-296">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9fae6-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
