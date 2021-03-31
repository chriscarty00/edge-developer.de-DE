---
description: Erfahren Sie, wie Sie die Laufzeitleistung in Microsoft Edge DevTools bewerten.
title: Erste Schritte mit der Analyse der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 439d6d4331550b7fc92bfc5fef4c3fc88df38872
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439612"
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

# <a name="get-started-with-analyzing-runtime-performance"></a><span data-ttu-id="6829b-104">Erste Schritte mit der Analyse der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="6829b-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="6829b-105">Um zu erfahren, wie Sie Ihre Seiten schneller laden können, navigieren Sie zu [Optimieren der Websitegeschwindigkeit][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="6829b-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="6829b-106">Die Laufzeitleistung ist die Leistung Ihrer Seite, wenn sie ausgeführt wird, statt zu laden.</span><span class="sxs-lookup"><span data-stu-id="6829b-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="6829b-107">Im folgenden Lernprogrammartikel erfahren Sie, wie Sie die Laufzeitleistung mithilfe des Microsoft Edge DevTools-Leistungsbereichs analysieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="6829b-108">Im Hinblick auf das **RAIL-Modell** sind die in diesem Lernprogramm gelernten Kenntnisse nützlich, um die Reaktions-, Animations- und Leerlaufphasen Ihrer Seite zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a><span data-ttu-id="6829b-109">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="6829b-109">Get started</span></span>  

<span data-ttu-id="6829b-110">Im folgenden Lernprogramm öffnen Sie DevTools auf  einer Liveseite und verwenden den Bereich Leistung, um einen Leistungsengpässe auf der Seite zu finden.</span><span class="sxs-lookup"><span data-stu-id="6829b-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="6829b-111">Öffnen Sie Microsoft Edge im **InPrivate-Modus.**</span><span class="sxs-lookup"><span data-stu-id="6829b-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="6829b-112">Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6829b-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="6829b-113">Wenn Sie z. B. viele Erweiterungen installiert haben, können die Erweiterungen zu Rauschen in Ihren Leistungsmessungen führen.</span><span class="sxs-lookup"><span data-stu-id="6829b-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="6829b-114">Laden Sie die folgende Seite in Ihr InPrivate-Fenster.</span><span class="sxs-lookup"><span data-stu-id="6829b-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="6829b-115">Die Seite ist die Demo, die Sie profilieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6829b-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="6829b-116">Die Seite zeigt eine Reihe kleiner Symbole, die nach oben und unten bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="6829b-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="6829b-117">Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6829b-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Die Demo auf der linken Seite und DevTools auf der rechten Seite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="6829b-119">Die Demo auf der linken Seite und DevTools auf der rechten Seite</span><span class="sxs-lookup"><span data-stu-id="6829b-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-120">Für die restlichen Abbildungen wird DevTools an ein [separates][DevtoolsCustomizePlacement] Fenster gedockt, um sich besser auf den Inhalt zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <a name="simulate-a-mobile-cpu"></a><span data-ttu-id="6829b-121">Simulieren einer mobilen CPU</span><span class="sxs-lookup"><span data-stu-id="6829b-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="6829b-122">Mobile Geräte haben viel weniger CPU-Leistung als Desktops und Laptops.</span><span class="sxs-lookup"><span data-stu-id="6829b-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="6829b-123">Verwenden Sie bei jedem Profil einer Seite die CPU-Einschränkung, um die Leistung Ihrer Seite auf mobilen Geräten zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="6829b-124">Wählen Sie in DevTools das **Tool Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-124">In DevTools, choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="6829b-125">Stellen Sie sicher, dass Sie das Kontrollkästchen neben **Screenshots auswählen.**</span><span class="sxs-lookup"><span data-stu-id="6829b-125">Ensure the you choose the checkbox next to **Screenshots**.</span></span>  
1.  <span data-ttu-id="6829b-126">Wählen **Sie Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="6829b-126">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>  <span data-ttu-id="6829b-127">DevTools zeigt Einstellungen im Zusammenhang mit der Erfassung von Leistungsmetriken an.</span><span class="sxs-lookup"><span data-stu-id="6829b-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="6829b-128">Wählen **Sie für CPU**die Option **4x Verlangsamung aus.**</span><span class="sxs-lookup"><span data-stu-id="6829b-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="6829b-129">DevTools drosselt die CPU, sodass sie viermal langsamer ist als gewöhnlich.</span><span class="sxs-lookup"><span data-stu-id="6829b-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="CPU-Drosselung" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="6829b-131">CPU-Drosselung</span><span class="sxs-lookup"><span data-stu-id="6829b-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-132">Beim Testen anderer Seiten; Wenn Sie sicherstellen möchten, dass jede Seite auf mobilen Low-End-Geräten gut funktioniert, legen Sie die CPU-Einschränkung auf **die 6-fache Verlangsamung fest.**</span><span class="sxs-lookup"><span data-stu-id="6829b-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="6829b-133">Die Demo funktioniert nicht gut mit der 6x-Verlangsamung, daher verwendet sie nur die 4-fache Verlangsamung für Anweisungszwecke.</span><span class="sxs-lookup"><span data-stu-id="6829b-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <a name="set-up-the-demo"></a><span data-ttu-id="6829b-134">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="6829b-134">Set up the demo</span></span>  

<span data-ttu-id="6829b-135">Es ist schwierig, eine Laufzeitleistungsdemo zu erstellen, die für alle Leser der Website konsistent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6829b-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="6829b-136">Im folgenden Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung relativ konsistent mit den Screenshots und Beschreibungen ist, unabhängig von Ihrer speziellen Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="6829b-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="6829b-137">Wählen Sie **die Schaltfläche 10** hinzufügen aus, bis die blauen Symbole merklich langsamer als zuvor bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="6829b-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="6829b-138">Auf einem High-End-Computer können Sie ihn etwa 20-mal auswählen.</span><span class="sxs-lookup"><span data-stu-id="6829b-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="6829b-139">Wählen Sie **Optimieren**aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-139">Choose **Optimize**.</span></span>  <span data-ttu-id="6829b-140">Die blauen Symbole sollten sich schneller und reibungsloser bewegen.</span><span class="sxs-lookup"><span data-stu-id="6829b-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-141">Um einen Unterschied zwischen den optimierten und nicht optimierten Versionen besser anzeigen zu können, wählen Sie einige Male die Schaltfläche Subtrahieren **10** aus, und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="6829b-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="6829b-142">Wenn Sie zu viele blaue Symbole hinzufügen, können Sie die CPU maximal verwenden, und dann sehen Sie möglicherweise keinen wesentlichen Unterschied in den Ergebnissen für die beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="6829b-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="6829b-143">Wählen **Sie Un-Optimize**aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="6829b-144">Die blauen Symbole werden langsamer und mit mehr Trägheit wieder bewegt.</span><span class="sxs-lookup"><span data-stu-id="6829b-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <a name="record-runtime-performance"></a><span data-ttu-id="6829b-145">Aufzeichnen der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="6829b-145">Record runtime performance</span></span>  

<span data-ttu-id="6829b-146">Wenn Sie die optimierte Version der Seite ausgeführt haben, bewegen sich die blauen Symbole schneller.</span><span class="sxs-lookup"><span data-stu-id="6829b-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="6829b-147">Weshalb?</span><span class="sxs-lookup"><span data-stu-id="6829b-147">Why is that?</span></span>  <span data-ttu-id="6829b-148">Beide Versionen sollen die Symbole in der gleichen Zeit verschieben.</span><span class="sxs-lookup"><span data-stu-id="6829b-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="6829b-149">Nehmen Sie eine Aufzeichnung im Bereich Leistung vor, um zu erfahren, wie Sie den Leistungsengpässe in der nicht optimierten Version erkennen.</span><span class="sxs-lookup"><span data-stu-id="6829b-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="6829b-150">Wählen Sie in DevTools **die Option Record** \( Record ![ ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="6829b-150">In DevTools, choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  <span data-ttu-id="6829b-151">DevTools erfasst Leistungsmetriken, während die Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6829b-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profilieren der Seite" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="6829b-153">Profilieren der Seite</span><span class="sxs-lookup"><span data-stu-id="6829b-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-154">Warten Sie einige Sekunden.</span><span class="sxs-lookup"><span data-stu-id="6829b-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="6829b-155">Wählen Sie **Beenden**aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-155">Choose **Stop**.</span></span>  <span data-ttu-id="6829b-156">DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Bereich Leistung an.</span><span class="sxs-lookup"><span data-stu-id="6829b-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Die Ergebnisse des Profils" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="6829b-158">Die Ergebnisse des Profils</span><span class="sxs-lookup"><span data-stu-id="6829b-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6829b-159">Wow, das ist eine übergroße Datenmenge.</span><span class="sxs-lookup"><span data-stu-id="6829b-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="6829b-160">machen Sie sich keine Sorgen, bald ist der Prozess sinnvoller.</span><span class="sxs-lookup"><span data-stu-id="6829b-160">do not worry, soon the process makes more sense.</span></span>  

## <a name="analyze-the-results"></a><span data-ttu-id="6829b-161">Analysieren der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="6829b-161">Analyze the results</span></span>  

<span data-ttu-id="6829b-162">Nachdem Sie die Leistung der Seite aufgezeichnet haben, messen Sie die Qualität der Leistung der Seite, und suchen Sie nach den ursachen.</span><span class="sxs-lookup"><span data-stu-id="6829b-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <a name="analyze-frames-per-second"></a><span data-ttu-id="6829b-163">Analysieren von Frames pro Sekunde</span><span class="sxs-lookup"><span data-stu-id="6829b-163">Analyze frames per second</span></span>  

<span data-ttu-id="6829b-164">Die Hauptmetrik zum Messen der Leistung einer Animation sind Frames pro Sekunde \(FPS\).</span><span class="sxs-lookup"><span data-stu-id="6829b-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="6829b-165">Benutzer freuen sich, wenn Animationen mit 60 FPS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6829b-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="6829b-166">Überprüfen Sie **das FPS-Diagramm.**</span><span class="sxs-lookup"><span data-stu-id="6829b-166">Review the **FPS** chart.</span></span>  <span data-ttu-id="6829b-167">Wenn ein roter Balken über **FPS**angezeigt wird, bedeutet dies, dass die Framerate so niedrig ist, dass sie wahrscheinlich die Benutzerfreundlichkeit geschädigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-167">Whenever a red bar is displayed above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="6829b-168">Im Allgemeinen gilt: Je höher der grüne Balken, desto höher der FPS.</span><span class="sxs-lookup"><span data-stu-id="6829b-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="6829b-170">Das **#A0**</span><span class="sxs-lookup"><span data-stu-id="6829b-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-171">Unterhalb **des #A0** wird das **#A1** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-171">Below the **FPS** chart, the **CPU** chart is displayed.</span></span>  <span data-ttu-id="6829b-172">Die Farben im **CPU-Diagramm** entsprechen  den Farben im Zusammenfassungsfenster am unteren Rand des Leistungsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6829b-172">The colors in the **CPU** chart correspond to the colors in the **Summary** panel, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="6829b-173">Die Tatsache, dass das **CPU-Diagramm** farblich voll ist, bedeutet, dass die CPU während der Aufzeichnung maximal ausgesenert wurde.</span><span class="sxs-lookup"><span data-stu-id="6829b-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="6829b-174">Immer wenn die CPU über einen längeren Zeitraum ausgesenkte, ist dies ein Indikator dafür, dass Sie Möglichkeiten finden sollten, weniger Arbeit zu machen.</span><span class="sxs-lookup"><span data-stu-id="6829b-174">Whenever the CPU maxed out for long periods, it is an indicator that you should find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Das CPU-Diagramm und der Zusammenfassungsbereich" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="6829b-176">Das **CPU-Diagramm** und **der Zusammenfassungsbereich**</span><span class="sxs-lookup"><span data-stu-id="6829b-176">The **CPU** chart and **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-177">Zeigen Sie auf **die FPS-,** **CPU-** oder **NET-Diagramme.**</span><span class="sxs-lookup"><span data-stu-id="6829b-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="6829b-178">DevTools zeigt einen Screenshot der Seite zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="6829b-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="6829b-179">Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wieder zu wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="6829b-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="6829b-180">Die Aktion wird als Scrubbing bezeichnet und ist nützlich für die manuelle Analyse des Verlaufs von Animationen.</span><span class="sxs-lookup"><span data-stu-id="6829b-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Anzeigen eines Screenshot der Seite um die 2500-ms-Marke der Aufzeichnung" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="6829b-182">Anzeigen eines Screenshot der Seite um die 2500-ms-Marke der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6829b-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-183">Zeigen Sie **im Abschnitt Frames** auf eines der grünen Quadrate.</span><span class="sxs-lookup"><span data-stu-id="6829b-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="6829b-184">DevTools zeigt ihnen den FPS für den jeweiligen Frame an.</span><span class="sxs-lookup"><span data-stu-id="6829b-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="6829b-185">Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="6829b-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Zeigen auf einen Frame" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="6829b-187">Zeigen auf einen Frame</span><span class="sxs-lookup"><span data-stu-id="6829b-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6829b-188">Die Anzeige zeigt natürlich an, dass die Webseite nicht gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6829b-188">Of course, the display indicates that the webpage is not performing well.</span></span>  <span data-ttu-id="6829b-189">In realen Szenarien ist dies jedoch möglicherweise nicht so klar, sodass alle Tools zum Durchführen von Messungen nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="6829b-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <a name="bonus-open-the-fps-meter"></a><span data-ttu-id="6829b-190">Bonus: Öffnen des FPS-Zählers</span><span class="sxs-lookup"><span data-stu-id="6829b-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="6829b-191">Ein weiteres praktisches Tool ist das FPS-Zähler, das Echtzeitschätzungen für FPS während der Seitenläufe bietet.</span><span class="sxs-lookup"><span data-stu-id="6829b-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="6829b-192">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="6829b-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="6829b-193">Beginnen Sie mit der `Rendering` Eingabe im **Befehlsmenü,** und wählen Sie **Rendern anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="6829b-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="6829b-194">Aktivieren Sie **im Renderingtool** **FPS Meter**.</span><span class="sxs-lookup"><span data-stu-id="6829b-194">In the **Rendering** tool, turn on **FPS Meter**.</span></span>  <span data-ttu-id="6829b-195">Oben rechts im Viewport wird eine neue Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="6829b-197">Das **#A0**</span><span class="sxs-lookup"><span data-stu-id="6829b-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="6829b-198">Deaktivieren Sie das **FPS Meter,** und wählen `Escape` Sie aus, um das **Renderingtool zu** schließen.</span><span class="sxs-lookup"><span data-stu-id="6829b-198">Turn off the **FPS Meter** and select `Escape` to close the **Rendering** tool.</span></span>  <span data-ttu-id="6829b-199">Sie verwenden **fps Meter** in diesem Lernprogramm nicht.</span><span class="sxs-lookup"><span data-stu-id="6829b-199">You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <a name="find-the-bottleneck"></a><span data-ttu-id="6829b-200">Suchen des Engpasss</span><span class="sxs-lookup"><span data-stu-id="6829b-200">Find the bottleneck</span></span>  

<span data-ttu-id="6829b-201">Nachdem Sie gemessen und überprüft haben, ob die Animation nicht gut funktioniert, besteht der nächste Schritt in der Beantwortung der Frage "Warum?".</span><span class="sxs-lookup"><span data-stu-id="6829b-201">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="6829b-202">Wenn keine Ereignisse ausgewählt werden, wird im **Zusammenfassungsbereich** eine Aufschlüsselung der Aktivität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-202">When no events are chosen, the **Summary** panel shows you a breakdown of activity.</span></span>  <span data-ttu-id="6829b-203">Die Seite hat die meiste Zeit mit dem Rendern verbracht.</span><span class="sxs-lookup"><span data-stu-id="6829b-203">The page spent most of the time rendering.</span></span>  <span data-ttu-id="6829b-204">Da leistung die Kunst ist, weniger Arbeit zu tun, besteht Ihr Ziel in der Reduzierung des Zeitaufwands für Renderingarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6829b-204">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Der Zusammenfassungsbereich" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="6829b-206">Der **Zusammenfassungsbereich**</span><span class="sxs-lookup"><span data-stu-id="6829b-206">The **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-207">Erweitern Sie den **Abschnitt Main.**</span><span class="sxs-lookup"><span data-stu-id="6829b-207">Expand the **Main** section.</span></span>  <span data-ttu-id="6829b-208">DevTools zeigt Ein Flammendiagramm der Aktivität im Hauptthread im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="6829b-208">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="6829b-209">Die x-Achse stellt die Aufzeichnung im Laufe der Zeit dar.</span><span class="sxs-lookup"><span data-stu-id="6829b-209">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="6829b-210">Jede Leiste stellt ein Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="6829b-210">Each bar represents an event.</span></span>  <span data-ttu-id="6829b-211">Ein breiterer Balken bedeutet, dass das Ereignis länger dauerte.</span><span class="sxs-lookup"><span data-stu-id="6829b-211">A wider bar means that event took longer.</span></span>  <span data-ttu-id="6829b-212">Die y-Achse stellt die Aufrufliste dar.</span><span class="sxs-lookup"><span data-stu-id="6829b-212">The y-axis represents the call stack.</span></span>  <span data-ttu-id="6829b-213">Wenn Ereignisse übereinander gestapelt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="6829b-213">When events are stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Der Abschnitt Main" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="6829b-215">Der **Abschnitt "Main"**</span><span class="sxs-lookup"><span data-stu-id="6829b-215">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6829b-216">Die Aufzeichnung enthält viele Daten.</span><span class="sxs-lookup"><span data-stu-id="6829b-216">There is a lot of data in the recording.</span></span>  <span data-ttu-id="6829b-217">So zoomen Sie in ein einzelnes Ereignis; Wählen, halten und ziehen Sie den Cursor über die **Übersicht**, die den Abschnitt enthält, der die **FPS-,** **CPU-** und **NET-Diagramme** enthält.</span><span class="sxs-lookup"><span data-stu-id="6829b-217">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="6829b-218">Im **Hauptabschnitt** **und im Zusammenfassungsbereich** werden nur Informationen für den ausgewählten Teil der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-218">The **Main** section and **Summary** panel only display information for the chosen portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Zoomen in ein Ereignis" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="6829b-220">Zoomen in ein Ereignis</span><span class="sxs-lookup"><span data-stu-id="6829b-220">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-221">Eine weitere Möglichkeit zum Zoomen, **Fokussieren** des Hauptabschnitts, Auswählen des Hintergrunds oder eines Ereignisses und Auswählen `W` von , , oder `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="6829b-221">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="6829b-222">Konzentrieren Sie sich auf das rote Dreieck oben rechts des **Ereignisses Animation Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="6829b-222">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="6829b-223">Jedes Mal, wenn ein rotes Dreieck angezeigt wird, wird gewarnt, dass es zu einem Problem im Zusammenhang mit dem Ereignis kommt.</span><span class="sxs-lookup"><span data-stu-id="6829b-223">Whenever a red triangle is displayed, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-224">Das **Ereignis Animation Frame Fired** tritt auf, wenn ein [requestAnimationFrame()-Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6829b-224">The **Animation Frame Fired** event occurs whenever a [requestAnimationFrame() callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="6829b-225">Wählen Sie das **Ereignis Animation Frame Fired** aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-225">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="6829b-226">Im **Zusammenfassungsbereich** werden nun Informationen zu diesem Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-226">The **Summary** panel now shows you information about that event.</span></span>  <span data-ttu-id="6829b-227">Notieren Sie sich **den Link Reveal.**</span><span class="sxs-lookup"><span data-stu-id="6829b-227">Note the **Reveal** link.</span></span>  <span data-ttu-id="6829b-228">Nachdem Sie es markiert haben, hebt DevTools das Ereignis hervor, das das **Ereignis Animation Frame Fired initiiert** hat.</span><span class="sxs-lookup"><span data-stu-id="6829b-228">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="6829b-229">Konzentrieren Sie sich außerdem auf **den linkapp.js:95.**</span><span class="sxs-lookup"><span data-stu-id="6829b-229">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="6829b-230">Nachdem Sie sie auswählen, wird die entsprechende Zeile im Quellcode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6829b-230">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Weitere Informationen zum Ereignis Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="6829b-232">Weitere Informationen zum **Ereignis Animation Frame Fired**</span><span class="sxs-lookup"><span data-stu-id="6829b-232">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-233">Nachdem Sie ein Ereignis ausgewählt haben, wählen Sie mit den Pfeiltasten die Ereignisse daneben aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-233">After choosing an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="6829b-234">Unter dem **app.update-Ereignis** gibt es eine Reihe von violetten Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6829b-234">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="6829b-235">Wenn jedes violette Ereignis breiter war, sieht es so aus, als ob jedes einzelne ein rotes Dreieck hat.</span><span class="sxs-lookup"><span data-stu-id="6829b-235">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="6829b-236">Wählen Sie eines der lila **Layout-Ereignisse** aus.</span><span class="sxs-lookup"><span data-stu-id="6829b-236">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="6829b-237">DevTools bietet weitere Informationen zum Ereignis im **Zusammenfassungsbereich.**</span><span class="sxs-lookup"><span data-stu-id="6829b-237">DevTools provides more information about the event in the **Summary** panel.</span></span>  <span data-ttu-id="6829b-238">Tatsächlich gibt es eine Warnung über erzwungene Umflüsse \(ein anderes Wort für Layout\).</span><span class="sxs-lookup"><span data-stu-id="6829b-238">Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="6829b-239">Wählen Sie **im Bereich** Zusammenfassung den Link **app.js:71** unter **Layout Erzwungen aus.**</span><span class="sxs-lookup"><span data-stu-id="6829b-239">In the **Summary** panel, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="6829b-240">DevTools führt Sie zur Codezeile, die das Layout erzwungen hat.</span><span class="sxs-lookup"><span data-stu-id="6829b-240">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Die Codezeile, die das erzwungene Layout verursacht hat" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="6829b-242">Die Codezeile, die das erzwungene Layout verursacht hat</span><span class="sxs-lookup"><span data-stu-id="6829b-242">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6829b-243">Das Problem mit dem Code ist, dass er in jedem Animationsframe die Formatvorlage für jedes Symbol ändert und dann die Position der einzelnen Symbole auf der Seite abfragt.</span><span class="sxs-lookup"><span data-stu-id="6829b-243">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="6829b-244">Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob sich jede Symbolposition geändert hat. Daher muss das Symbol neu layoutt werden, um die neue Position zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6829b-244">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="6829b-245">Das war viel zu lernen.</span><span class="sxs-lookup"><span data-stu-id="6829b-245">That was a lot to learn.</span></span>  <span data-ttu-id="6829b-246">Sie verfügen nun über eine solide Grundlage im grundlegenden Workflow für die Analyse der Laufzeitleistung.</span><span class="sxs-lookup"><span data-stu-id="6829b-246">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="6829b-247">Gut Gemacht.</span><span class="sxs-lookup"><span data-stu-id="6829b-247">Good job.</span></span>  

### <a name="bonus-analyze-the-optimized-version"></a><span data-ttu-id="6829b-248">Bonus: Analysieren der optimierten Version</span><span class="sxs-lookup"><span data-stu-id="6829b-248">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="6829b-249">Wählen Sie mithilfe der Workflows und Tools, die Sie gerade gelernt haben, **optimieren** in der Demo aus, um den optimierten Code zu aktivieren, eine weitere Leistungsaufzeichnung zu erstellen und die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-249">Using the workflows and tools that you just learned, choose **Optimize** on the demo to turn on the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="6829b-250">Von der verbesserten Framerate bis zur Reduzierung der Ereignisse im Flammendiagramm im **Abschnitt Main** führt die optimierte Version der App wesentlich weniger Arbeit, was zu einer besseren Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6829b-250">From the improved framerate to the reduction in events in the flame chart in the **Main** section, the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="6829b-251">Auch die optimierte Version ist nicht großartig, da sie die `top` Eigenschaft jedes Symbols bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="6829b-251">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="6829b-252">Ein besserer Ansatz ist, sich an Eigenschaften zu halten, die sich nur auf das Compositing auswirken.</span><span class="sxs-lookup"><span data-stu-id="6829b-252">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a><span data-ttu-id="6829b-253">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="6829b-253">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

<span data-ttu-id="6829b-254">Damit Sie sich mit dem **Tool "Leistung"** bequemer machen können, ist die Übung perfekt.</span><span class="sxs-lookup"><span data-stu-id="6829b-254">To get more comfortable with the **Performance** tool, practice makes perfect.</span></span>  <span data-ttu-id="6829b-255">Versuchen Sie, Ihre Seiten zu profilieren und die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6829b-255">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="6829b-256">Wenn Sie Fragen zu Ihren Ergebnissen  haben, verwenden Sie das Symbol Feedback senden, wählen `Alt` + `Shift` + `I` Sie \(Windows, Linux\), wählen `Option` + `Shift` + `I` Sie \(macOS\) aus, [][TwitterEdgeDevtools]oder twittern Sie das DevTools-Team .</span><span class="sxs-lookup"><span data-stu-id="6829b-256">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="6829b-257">Fügen Sie nach Möglichkeit Screenshots oder Links zu reproduzierbaren Seiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="6829b-257">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Das Symbol **Feedback** in den Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="6829b-259">Das Symbol **Feedback senden** in den Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6829b-259">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="6829b-260">Last, there are many ways to improve runtime performance.</span><span class="sxs-lookup"><span data-stu-id="6829b-260">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="6829b-261">Dieser Artikel konzentrierte sich auf einen bestimmten Animationsengpässe, um Ihnen eine konzentrierte Tour durch den Bereich Leistung zu bieten, aber es ist nur einer von vielen Engpässen, die Sie möglicherweise haben.</span><span class="sxs-lookup"><span data-stu-id="6829b-261">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6829b-262">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="6829b-262">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Ändern der Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools – Post a Tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

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
> <span data-ttu-id="6829b-267">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6829b-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6829b-268">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="6829b-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6829b-270">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6829b-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
