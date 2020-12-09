---
description: Erfahren Sie, wie Sie die Laufzeitleistung in Microsoft Edge devtools.
title: Erste Schritte mit der Analyse der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7cb1d8f073cdb8a43093514dd7dea86d72102011
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124985"
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

# <span data-ttu-id="d5b7c-104">Erste Schritte mit der Analyse der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="d5b7c-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="d5b7c-105">Wenn Sie wissen möchten, wie Sie Ihre Seiten schneller laden können, navigieren Sie zur [Optimierung der Website Geschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="d5b7c-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="d5b7c-106">Die Laufzeitleistung ist die Art und Weise, wie Ihre Seite ausführt, wenn Sie ausgeführt wird, im Gegensatz zum Laden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="d5b7c-107">Im folgenden Lernprogramm Artikel erfahren Sie, wie Sie das Microsoft Edge devtools-Leistungs Panel verwenden, um die Runtime-Leistung zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="d5b7c-108">Im Hinblick auf das **Schienen** Modell sind die in diesem Lernprogramm gelernten Kenntnisse hilfreich, um die Reaktions-, Animations-und Leerlaufphasen Ihrer Seite zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="d5b7c-109">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d5b7c-109">Get started</span></span>  

<span data-ttu-id="d5b7c-110">Im folgenden Lernprogramm öffnen Sie devtools auf einer Live Seite und verwenden den **Leistungs** Panel, um einen Leistungsengpass auf der Seite zu finden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="d5b7c-111">Öffnen Sie Microsoft Edge im **InPrivate-Modus**.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="d5b7c-112">Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="d5b7c-113">Wenn Sie beispielsweise viele Erweiterungen installiert haben, können die Erweiterungen zu Lärm in ihren Leistungsmessungen führen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="d5b7c-114">Laden Sie die folgende Seite in Ihrem InPrivate-Fenster.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="d5b7c-115">Bei der Seite handelt es sich um die Demo, die Sie profilieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="d5b7c-116">Auf der Seite werden einige kleine Symbole angezeigt, die sich nach oben und unten bewegen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="d5b7c-117">Wählen Sie `Control` + `Shift` + `I` \ (Windows, Linux \) oder `Command` + `Option` + `I` \ (macOS \) aus, um devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Die Demo auf der linken Seite und DevTools auf der rechten Seite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="d5b7c-119">Die Demo auf der linken Seite und DevTools auf der rechten Seite</span><span class="sxs-lookup"><span data-stu-id="d5b7c-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-120">Für die restlichen Zahlen wird devtools [an einem separaten Fenster Abdocken][DevtoolsCustomizePlacement] , um sich besser auf den Inhalt zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="d5b7c-121">Simulieren einer mobilen CPU</span><span class="sxs-lookup"><span data-stu-id="d5b7c-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="d5b7c-122">Mobile Geräte haben viel weniger Prozessorleistung als Desktops und Laptops.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="d5b7c-123">Wenn Sie eine Seite profilieren, simulieren Sie mithilfe der CPU-Drosselung, wie Ihre Seite auf mobilen Geräten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="d5b7c-124">Wählen Sie in devtools die Registerkarte **Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-124">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="d5b7c-125">Stellen Sie sicher, dass das Kontrollkästchen **Screenshots** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="d5b7c-126">Wählen Sie **aufnahmeeinstellungen** \ (! [ Aufnahmeeinstellungen] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d5b7c-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="d5b7c-127">DevTools zeigt Einstellungen in Bezug auf die Erfassung von Leistungs Metriken an.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="d5b7c-128">Wählen Sie für **CPU**die Option **4X Verlangsamung**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="d5b7c-129">DevTools drosselt Ihre CPU so, dass Sie viermal langsamer als üblich ist.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="CPU-Drosselung" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="d5b7c-131">CPU-Drosselung</span><span class="sxs-lookup"><span data-stu-id="d5b7c-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-132">Beim Testen anderer Seiten; Wenn Sie sicherstellen möchten, dass jede Seite auf Low-End-mobilen Geräten gut funktioniert, legen Sie die CPU-Drosselung auf **6x Verlangsamung**fest.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="d5b7c-133">Die Demo funktioniert nicht gut mit einer 6x Verlangsamung, sodass Sie nur eine vierfache Verlangsamung für Unterrichtszwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="d5b7c-134">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="d5b7c-134">Set up the demo</span></span>  

<span data-ttu-id="d5b7c-135">Es ist schwierig, eine Demo zur Laufzeit-Performance zu erstellen, die für alle Leser der Website konsistent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="d5b7c-136">Im folgenden Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung mit den Screenshots und Beschreibungen relativ konsistent ist, unabhängig von der jeweiligen Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="d5b7c-137">Wählen Sie die Schaltfläche " **10 hinzufügen** " aus, bis sich die blauen Symbole merklich langsamer bewegen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="d5b7c-138">Auf einem Highend-Computer können Sie die Datei etwa 20 Mal auswählen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="d5b7c-139">Wählen Sie **optimieren**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-139">Choose **Optimize**.</span></span>  <span data-ttu-id="d5b7c-140">Die blauen Symbole sollten sich schneller und reibungsloser bewegen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-141">Um einen Unterschied zwischen den optimierten und nicht optimierten Versionen besser anzuzeigen, wählen Sie die Schaltfläche **10 subtrahieren** einige Male aus, und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="d5b7c-142">Wenn Sie zu viele blaue Symbole hinzufügen, ist es möglich, dass Sie die CPU maximal auszahlen, und es ist möglich, dass Sie keinen großen Unterschied in den Ergebnissen für die beiden Versionen beobachten.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="d5b7c-143">Wählen Sie **UN-Optimize**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="d5b7c-144">Die blauen Symbole bewegen sich langsamer und mit mehr Trägheit wieder.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="d5b7c-145">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="d5b7c-145">Record runtime performance</span></span>  

<span data-ttu-id="d5b7c-146">Wenn Sie die optimierte Version der Seite ausgeführt haben, werden die blauen Symbole schneller verschoben.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="d5b7c-147">Weshalb?</span><span class="sxs-lookup"><span data-stu-id="d5b7c-147">Why is that?</span></span>  <span data-ttu-id="d5b7c-148">Beide Versionen sollen die Symbole in derselben Zeitdauer auf die gleiche Menge an Speicherplatz verschieben.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="d5b7c-149">Nehmen Sie im Leistungs Panel eine Aufzeichnung auf, um zu erfahren, wie Sie den Leistungsengpass in der nicht optimierten Version erkennen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="d5b7c-150">Wählen Sie in devtools die Option **Record** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d5b7c-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="d5b7c-151">DevTools erfasst Leistungs Metriken während der Ausführung der Seite.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profil der Seite" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="d5b7c-153">Profil der Seite</span><span class="sxs-lookup"><span data-stu-id="d5b7c-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-154">Warten Sie ein paar Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="d5b7c-155">Wählen Sie **Beenden**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-155">Choose **Stop**.</span></span>  <span data-ttu-id="d5b7c-156">DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Leistungs Panel an.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Die Ergebnisse des Profils" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="d5b7c-158">Die Ergebnisse des Profils</span><span class="sxs-lookup"><span data-stu-id="d5b7c-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5b7c-159">Wow, das ist eine überwältigende Menge an Daten.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="d5b7c-160">machen Sie sich keine Sorgen, schon bald macht der Prozess Sinn.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-160">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="d5b7c-161">Analysieren der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="d5b7c-161">Analyze the results</span></span>  

<span data-ttu-id="d5b7c-162">Nachdem Sie die Leistung der Seite aufgezeichnet haben, Messen Sie die Qualität der Leistung der Seite, und ermitteln Sie die Ursachen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="d5b7c-163">Analysieren von Frames pro Sekunde</span><span class="sxs-lookup"><span data-stu-id="d5b7c-163">Analyze frames per second</span></span>  

<span data-ttu-id="d5b7c-164">Die wichtigste Metrik zum Messen der Leistung einer Animation ist Frames pro Sekunde \ (fps \).</span><span class="sxs-lookup"><span data-stu-id="d5b7c-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="d5b7c-165">Benutzer sind zufrieden, wenn Animationen mit 60 fps ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="d5b7c-166">Schauen Sie sich das **fps** -Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-166">Look at the **FPS** chart.</span></span>  <span data-ttu-id="d5b7c-167">Wenn Sie eine rote Leiste oberhalb von **fps**sehen, bedeutet dies, dass die Framerate so gering ist, dass Sie die Benutzerfreundlichkeit wahrscheinlich beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-167">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="d5b7c-168">Je höher die grüne Leiste, desto höher der FPS-Wert.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Das fps-Diagramm" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="d5b7c-170">Das **fps** -Diagramm</span><span class="sxs-lookup"><span data-stu-id="d5b7c-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-171">Unterhalb des **fps** -Diagramms wird das **CPU** -Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-171">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="d5b7c-172">Die Farben im **CPU** -Diagramm entsprechen den Farben auf der Registerkarte " **Zusammenfassung** " unten im Leistungsbereich.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-172">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="d5b7c-173">Die Tatsache, dass das **CPU** -Diagramm Farb voll ist, bedeutet, dass die CPU während der Aufzeichnung ausgereizt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="d5b7c-174">Wenn Sie sehen, dass die CPU über einen längeren Zeitraum ausgeschöpft ist, ist es ein Anhaltspunkt, wie Sie Möglichkeiten für eine geringere Arbeit finden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-174">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Das CPU-Diagramm und die Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="d5b7c-176">Das **CPU** -Diagramm und die Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="d5b7c-176">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-177">Zeigen Sie auf die **fps**-, **CPU**-oder **net** -Diagramme.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="d5b7c-178">DevTools zeigt zu diesem Zeitpunkt einen Screenshot der Seite an.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="d5b7c-179">Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="d5b7c-180">Die Aktion wird als Scrubbing referenziert, und Sie ist nützlich, um den Fortschritt von Animationen manuell zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="d5b7c-182">Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="d5b7c-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-183">Zeigen Sie im Abschnitt **Frames** auf eines der grünen Quadrate.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="d5b7c-184">DevTools zeigt Ihnen die fps für diesen bestimmten Frame.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="d5b7c-185">Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 fps.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Bewegen des Mauszeigers auf einem Frame" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="d5b7c-187">Bewegen des Mauszeigers auf einem Frame</span><span class="sxs-lookup"><span data-stu-id="d5b7c-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5b7c-188">Natürlich sollten Sie sehen, dass die Seite nicht gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-188">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="d5b7c-189">In realen Szenarien ist es aber möglicherweise nicht so klar, dass alle Tools für die Messung praktisch sind.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="d5b7c-190">Bonus: Öffnen des FPS-meters</span><span class="sxs-lookup"><span data-stu-id="d5b7c-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="d5b7c-191">Ein weiteres praktisches Tool ist das FPS-Messgerät, das in Echtzeit Schätzungen für FPS bereitstellt, während die Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="d5b7c-192">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="d5b7c-193">Beginnen `Rendering` Sie mit der Eingabe im **Befehlsmenü** , und wählen Sie **Rendering anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="d5b7c-194">Aktivieren Sie auf der Registerkarte **Rendern** die Option **FPS-Meter**.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-194">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="d5b7c-195">In der oberen rechten Ecke des Viewports wird eine neue Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Das fps-Messgerät" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="d5b7c-197">Das **fps-Messgerät**</span><span class="sxs-lookup"><span data-stu-id="d5b7c-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-198">Deaktivieren Sie das **fps-Messgerät** , und wählen Sie aus `Escape` , um die Registerkarte **Rendering** zu schließen.  In diesem Lernprogramm verwenden Sie nicht **FPS-Meter** .</span><span class="sxs-lookup"><span data-stu-id="d5b7c-198">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="d5b7c-199">Ermitteln des Engpasses</span><span class="sxs-lookup"><span data-stu-id="d5b7c-199">Find the bottleneck</span></span>  

<span data-ttu-id="d5b7c-200">Nachdem Sie gemessen und überprüft haben, dass die Animation nicht gut funktioniert, besteht der nächste Schritt darin, die Frage "Warum?" zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-200">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="d5b7c-201">Wenn keine Ereignisse ausgewählt sind, wird auf der Registerkarte **Zusammenfassung** eine Aufschlüsselung der Aktivitäten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-201">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="d5b7c-202">Die Seite verbrachte die meiste Zeit beim Rendern.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-202">The page spent most of the time rendering.</span></span>  <span data-ttu-id="d5b7c-203">Da Leistung die Kunst ist, weniger Arbeit zu erledigen, besteht das Ziel darin, die Zeit zu verringern, die für das Rendern von Arbeit aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-203">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="d5b7c-205">Registerkarte " **Zusammenfassung** "</span><span class="sxs-lookup"><span data-stu-id="d5b7c-205">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-206">Erweitern des **Haupt** Abschnitts</span><span class="sxs-lookup"><span data-stu-id="d5b7c-206">Expand the **Main** section.</span></span>  <span data-ttu-id="d5b7c-207">DevTools zeigt Ihnen im Laufe der Zeit ein Flammen Diagramm mit Aktivitäten auf dem Hauptthread.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-207">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="d5b7c-208">Die x-Achse steht für die Aufzeichnung im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-208">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="d5b7c-209">Jeder Balken steht für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-209">Each bar represents an event.</span></span>  <span data-ttu-id="d5b7c-210">Eine breitere Leiste bedeutet, dass das Ereignis länger dauerte.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-210">A wider bar means that event took longer.</span></span>  <span data-ttu-id="d5b7c-211">Die y-Achse steht für die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-211">The y-axis represents the call stack.</span></span>  <span data-ttu-id="d5b7c-212">Wenn Ereignisse übereinander gestapelt angezeigt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-212">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Der Hauptabschnitt" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="d5b7c-214">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d5b7c-214">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5b7c-215">Die Aufzeichnung enthält viele Daten.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-215">There is a lot of data in the recording.</span></span>  <span data-ttu-id="d5b7c-216">So zoomen Sie in ein einzelnes Ereignis Wählen Sie den Mauszeiger über der **Übersicht**aus, halten Sie ihn gedrückt, und ziehen Sie ihn in den Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-216">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="d5b7c-217">Der **Haupt** Abschnitt und die Registerkarte " **Zusammenfassung** " zeigen nur Informationen für den ausgewählten Teil der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-217">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Vergrößern eines Ereignisses" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="d5b7c-219">Vergrößern eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d5b7c-219">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-220">Eine weitere Möglichkeit zum Zoomen, zum Fokussieren des **Haupt** Abschnitts, zum Auswählen des Hintergrunds oder eines Ereignisses und zum auswählen `W` ,, `A` `S` oder `D` .</span><span class="sxs-lookup"><span data-stu-id="d5b7c-220">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="d5b7c-221">Konzentrieren Sie sich auf das rote Dreieck in der oberen rechten Ecke des Ereignisses **Animations Frame ausgelöst** .</span><span class="sxs-lookup"><span data-stu-id="d5b7c-221">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d5b7c-222">Wenn Sie ein rotes Dreieck sehen, wird eine Warnung angezeigt, dass ein Problem im Zusammenhang mit dem Ereignis auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-222">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-223">Das **ausgelöste Animations Frame** -Ereignis tritt auf, wenn ein [ `requestAnimationFrame()` Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-223">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="d5b7c-224">Wählen Sie das **ausgelöste Animations Frame** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-224">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d5b7c-225">Auf der Registerkarte " **Zusammenfassung** " werden nun Informationen zu diesem Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-225">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="d5b7c-226">Beachten Sie den Link **Reveal** .</span><span class="sxs-lookup"><span data-stu-id="d5b7c-226">Note the **Reveal** link.</span></span>  <span data-ttu-id="d5b7c-227">Nachdem Sie Sie ausgewählt haben, hebt devtools das Ereignis hervor, das das ausgelöste **Animations Frame** -Ereignis initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-227">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="d5b7c-228">Konzentrieren Sie sich auch auf den Link **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="d5b7c-228">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="d5b7c-229">Nachdem Sie Sie ausgewählt haben, wird die entsprechende Zeile im Quellcode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-229">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Weitere Informationen zum ausgelösten Animations Frame-Ereignis" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="d5b7c-231">Weitere Informationen zum **ausgelösten Animations Frame** -Ereignis</span><span class="sxs-lookup"><span data-stu-id="d5b7c-231">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-232">Verwenden Sie nach dem Auswählen eines Ereignisses die Pfeiltasten, um die Ereignisse daneben auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-232">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="d5b7c-233">Unter dem **app. Update** -Ereignis gibt es eine Reihe von lila Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-233">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="d5b7c-234">Wenn jedes violette Ereignis breiter war, sieht es so aus, als ob jeder ein rotes Dreieck darauf haben kann.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-234">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="d5b7c-235">Wählen Sie eines der lila **Layout** -Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-235">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="d5b7c-236">DevTools enthält weitere Informationen zu dem Ereignis auf der Registerkarte " **Zusammenfassung** ".  In der Tat gibt es eine Warnung zu erzwungenen Umläufen \ (ein weiteres Wort für das Layout \).</span><span class="sxs-lookup"><span data-stu-id="d5b7c-236">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="d5b7c-237">Wählen Sie auf der Registerkarte **Zusammenfassung** den Link **app.js:71** unter **Layout erzwungen**aus.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-237">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="d5b7c-238">DevTools führt Sie zu der Codezeile, die das Layout erzwungen hat.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-238">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Die Codezeile, die das erzwungene Layout verursacht hat" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="d5b7c-240">Die Codezeile, die das erzwungene Layout verursacht hat</span><span class="sxs-lookup"><span data-stu-id="d5b7c-240">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5b7c-241">Das Problem mit dem Code besteht darin, dass in jedem Animationsframe die Formatvorlage für jedes Symbol geändert und dann die Position der einzelnen Symbole auf der Seite abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-241">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="d5b7c-242">Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob jede Symbolposition geändert wurde, sodass das Symbol neu angeordnet werden muss, um die neue Position zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-242">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="d5b7c-243">Das war viel zu lernen.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-243">That was a lot to learn.</span></span>  <span data-ttu-id="d5b7c-244">Sie verfügen jetzt über eine solide Grundlage im grundlegenden Workflow zum Analysieren der Laufzeitleistung.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-244">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="d5b7c-245">Gut Gemacht.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-245">Good job.</span></span>  

### <span data-ttu-id="d5b7c-246">Bonus: Analysieren der optimierten Version</span><span class="sxs-lookup"><span data-stu-id="d5b7c-246">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="d5b7c-247">Wählen Sie mithilfe der soeben gelernten Workflows und Tools in der Demo **optimieren** aus, um den optimierten Code zu aktivieren, eine andere Leistungsaufnahme durchführen und dann die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-247">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="d5b7c-248">Von der verbesserten Framerate bis zur Reduzierung von Ereignissen im Flammen Diagramm im **Haupt** Abschnitt können Sie feststellen, dass die optimierte Version der APP viel weniger Arbeit leistet, was zu einer besseren Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-248">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5b7c-249">Auch die optimierte Version ist nicht optimal, da Sie die `top` Eigenschaft jedes Symbols manipuliert.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-249">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="d5b7c-250">Ein besserer Ansatz ist das Beibehalten von Eigenschaften, die sich nur auf die Compositing-Methode auswirken.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-250">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="d5b7c-251">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d5b7c-251">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="d5b7c-252">Um mit dem Leistungsumfang noch komfortabler zu werden, ist die Praxis perfekt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-252">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="d5b7c-253">Versuchen Sie, Ihre Seiten zu profilieren und die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-253">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="d5b7c-254">Wenn Sie Fragen zu ihren Ergebnissen haben, verwenden Sie das Symbol **Feedback senden** , wählen Sie `Alt` + `Shift` + `I` \ (Windows, Linux \) aus, wählen Sie `Option` + `Shift` + `I` \ (macOS \) aus, oder [tweeten Sie das devtools-Team][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="d5b7c-254">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="d5b7c-255">Fügen Sie Screenshots oder Links zu reproduzierbaren Seiten hinzu, falls möglich.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-255">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Das \* \* Feedback \* \*-Symbol in der Microsoft Edge-devtools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="d5b7c-257">Das Symbol " **Feedback senden** " im Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="d5b7c-257">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="d5b7c-258">Schließlich gibt es viele Möglichkeiten, die Laufzeitleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-258">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="d5b7c-259">Dieser Artikel befasst sich mit einem bestimmten Animations Engpass, der Ihnen eine gezielte Tour durch das Leistungs Panel ermöglicht, aber nur eine von vielen Engpässen, die Ihnen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-259">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <span data-ttu-id="d5b7c-260">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d5b7c-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools"  

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
> <span data-ttu-id="d5b7c-265">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-265">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d5b7c-266">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-266">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d5b7c-268">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d5b7c-268">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
