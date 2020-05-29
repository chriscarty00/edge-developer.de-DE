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







# Erste Schritte mit der Analyse der Laufzeitleistung   



> [!NOTE]
> Informationen dazu, wie Sie Ihre Seiten schneller laden können, finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted] .  

Die Laufzeitleistung ist die Art und Weise, wie Ihre Seite ausführt, wenn Sie ausgeführt wird, im Gegensatz zum Laden.  In diesem Lernprogramm erfahren Sie, wie Sie das Microsoft Edge devtools-Leistungs Panel verwenden, um die Runtime-Leistung zu analysieren.  Im Hinblick auf das **Schienen** Modell sind die in diesem Lernprogramm gelernten Kenntnisse hilfreich, um die Reaktions-, Animations-und Leerlaufphasen Ihrer Seite zu analysieren.  

<!--todo: add rail link when section is ready -->  

## Erste Schritte   

In diesem Lernprogramm öffnen Sie devtools auf einer Live Seite und verwenden den Leistungs Panel, um einen Leistungsengpass auf der Seite zu finden.  

1.  Öffnen Sie Microsoft Edge im **InPrivate-Modus**.  Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.  Wenn Sie beispielsweise viele Erweiterungen installiert haben, können diese Erweiterungen zu Lärm in ihren Leistungsmessungen führen.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Laden Sie die folgende Seite in Ihrem InPrivate-Fenster.  Dies ist die Demo, die Sie profilieren werden.  Auf der Seite werden einige kleine Symbole angezeigt, die sich nach oben und unten bewegen.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \), um devtools zu öffnen.  
    
    > ###### Abbildung1  
    > Die Demo auf der linken Seite und DevTools auf der rechten Seite  
    > ![Die Demo auf der linken Seite und DevTools auf der rechten Seite][ImageGetStarted]  
    
    > [!NOTE]
    > Für die restlichen Screenshots wird devtools [in einem separaten Fenster Abdocken][DevtoolsCustomizePlacement] , damit Sie den Inhalt besser sehen können.  
    
### Simulieren einer mobilen CPU  

Mobile Geräte haben viel weniger Prozessorleistung als Desktops und Laptops.  Wenn Sie eine Seite profilieren, simulieren Sie mithilfe der CPU-Drosselung, wie Ihre Seite auf mobilen Geräten ausgeführt wird.  

1.  Klicken Sie in devtools auf die Registerkarte **Leistung** .  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Screenshots** aktiviert ist.  
1.  Klicken Sie auf Aufnahmeeinstellungen für **aufnahmeeinstellungen** ![ ][ImageCaptureSettingsIcon] .  DevTools zeigt Einstellungen in Bezug auf die Erfassung von Leistungs Metriken an.  
1.  Wählen Sie für **CPU**die Option **4X Verlangsamung**aus.  DevTools drosselt Ihre CPU so, dass Sie viermal langsamer als üblich ist.  
    
    > ###### Abbildung2  
    > CPU-Drosselung  
    > ![CPU-Drosselung][ImageCPUThrottling]  
    
    > [!NOTE]
    > Wenn Sie beim Testen anderer Seiten sicherstellen möchten, dass Sie auf Low-End-mobilen Geräten gut funktionieren, legen Sie die CPU-Drosselung auf **6x Abschwächung**fest.  Diese Demo funktioniert nicht gut mit einer 6x Verlangsamung, sodass Sie nur eine vierfache Verlangsamung für Unterrichtszwecke verwendet.  
    
### Einrichten der Demo  

Es ist schwierig, eine Runtime Performance-Demo zu erstellen, die für alle Leser dieser Website konsistent funktioniert.  In diesem Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung mit den Screenshots und Beschreibungen, die Sie in diesem Lernprogramm sehen, relativ konsistent ist, und zwar unabhängig von ihrem jeweiligen Setup.

1.  Klicken **Sie auf Hinzufügen 10** , bis die blauen Symbole merklich langsamer als zuvor verschoben sind.  Auf einem Highend-Computer kann es etwa 20 Klicks dauern.  
1.  Klicken Sie auf **optimieren**.  Die blauen Symbole sollten sich schneller und reibungsloser bewegen.  

    > [!NOTE]
    > Wenn Sie zwischen den optimierten und nicht optimierten Versionen keinen nennenswerten Unterschied sehen, klicken Sie mehrmals auf **subtrahieren** , und versuchen Sie es erneut.  
    > Wenn Sie zu viele blaue Symbole hinzufügen, werden Sie einfach die CPU ausweiten, und Sie werden keinen großen Unterschied in den Ergebnissen für die beiden Versionen sehen.  

1.  Klicken Sie auf **UN-Optimize**.  Die blauen Symbole werden langsamer und mit mehr Jank wieder verschoben.  

### Aufzeichnen der Laufzeitleistung   

Wenn Sie die optimierte Version der Seite ausgeführt haben, werden die blauen Symbole schneller verschoben.  
Weshalb?  Beide Versionen sollen die Symbole in derselben Zeitdauer auf die gleiche Menge an Speicherplatz verschieben.  Nehmen Sie im Leistungs Panel eine Aufzeichnung auf, um zu erfahren, wie Sie den Leistungsengpass in der nicht optimierten Version erkennen.  

1.  Klicken Sie in devtools auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
    DevTools erfasst Leistungs Metriken während der Ausführung der Seite.  
    
    > ###### Abbildung 3 
    > Profilerstellung der Seite  
    > ![Profilerstellung der Seite][ImagePageProfiling]  
    
1.  Warten Sie ein paar Sekunden.  
1.  Klicken Sie auf **Beenden**.  DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Leistungs Panel an.  
    
    > ###### Abbildung4  
    > Die Ergebnisse des Profils  
    > ![Die Ergebnisse des Profils][ImageProfileResults]  

Wow, das ist eine überwältigende Menge an Daten.  Machen Sie sich keine Sorgen, es wird in Kürze sinnvoller sein.  

## Analysieren der Ergebnisse   

Nachdem Sie die Leistung der Seite aufgezeichnet haben, können Sie messen, wie schlecht die Leistung der Seite ist, und die Ursachen ermitteln.  

### Analysieren von Frames pro Sekunde  

Die wichtigste Metrik zum Messen der Leistung einer Animation ist Frames pro Sekunde \ (fps \).  Benutzer sind zufrieden, wenn Animationen mit 60 fps ausgeführt werden.  

1.  Schauen Sie sich das **fps** -Diagramm an.  Wenn Sie eine rote Leiste oberhalb von **fps**sehen, bedeutet dies, dass die Framerate so gering ist, dass Sie die Benutzerfreundlichkeit wahrscheinlich beeinträchtigt.  Je höher die grüne Leiste, desto höher der FPS-Wert.  
    
    > ###### Abbildung5  
    > Das fps-Diagramm  
    > ![Das fps-Diagramm][ImageFPSChart]  

1.  Unterhalb des **fps** -Diagramms wird das **CPU** -Diagramm angezeigt.  Die Farben im **CPU** -Diagramm entsprechen den Farben auf der Registerkarte " **Zusammenfassung** " unten im Leistungsbereich.  Die Tatsache, dass das **CPU** -Diagramm Farb voll ist, bedeutet, dass die CPU während der Aufzeichnung ausgereizt wurde.  Wenn Sie sehen, dass die CPU über einen längeren Zeitraum ausgeschöpft ist, ist es ein Anhaltspunkt, wie Sie Möglichkeiten für eine geringere Arbeit finden.  
    
    > ###### Abbildung6  
    > Das CPU-Diagramm und die Registerkarte "Zusammenfassung"  
    > ![Das CPU-Diagramm und die Registerkarte "Zusammenfassung"][ImageCPUSummary]  

1.  Zeigen Sie mit der Maus auf die **fps**-, **CPU**-oder **net** -Diagramme.  DevTools zeigt zu diesem Zeitpunkt einen Screenshot der Seite an.  Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wiederzugeben.  Dies wird als Scrubbing bezeichnet und ist hilfreich, um den Fortschritt von Animationen manuell zu analysieren.  
    
    > ###### Abbildung7  
    > Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung  
    > ![Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung][ImageViewingScreenshot]  

1.  Zeigen Sie im Abschnitt **Frames** mit der Maus auf eines der grünen Quadrate.  DevTools zeigt Ihnen die fps für diesen bestimmten Frame.  Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 fps.  
    
    > ###### Abbildung8  
    > Bewegen des Mauszeigers über einen Frame  
    > ![Bewegen des Mauszeigers über einen Frame][ImageFrameHover]  

Natürlich ist es bei dieser Demo ziemlich offensichtlich, dass die Seite nicht gut funktioniert.  In realen Szenarien ist es aber möglicherweise nicht so klar, dass alle diese Tools für Messungen praktisch sind.  

#### Bonus: Öffnen des FPS-meters  

Ein weiteres praktisches Tool ist das FPS-Messgerät, das in Echtzeit Schätzungen für FPS bereitstellt, während die Seite ausgeführt wird.  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.  
1.  Beginnen `Rendering` Sie mit der Eingabe im Befehlsmenü, und wählen Sie **Rendering anzeigen**aus.  
1.  Aktivieren Sie auf der Registerkarte **Rendern** die Option **FPS-Meter**.  In der oberen rechten Ecke des Viewports wird eine neue Überlagerung angezeigt.  
    
    > ###### Abbildung 9  
    > Das fps-Messgerät  
    > ![Das fps-Messgerät][ImageFPSMeter]  

1.  Deaktivieren Sie das **fps-Messgerät** , und drücken Sie `Escape` , um die Registerkarte **Rendern** zu schließen.  In diesem Lernprogramm verwenden Sie Sie nicht.  

### Ermitteln des Engpasses  

Nachdem Sie nun gemessen und überprüft haben, dass die Animation nicht gut funktioniert, müssen Sie die nächste Frage beantworten: Warum?  

1.  Beachten Sie die Registerkarte Zusammenfassung.  Wenn keine Ereignisse ausgewählt sind, wird auf dieser Registerkarte eine Aufschlüsselung der Aktivitäten angezeigt.  Die Seite hat die meiste Zeit gerendert.  Da Leistung die Kunst ist, weniger Arbeit zu erledigen, besteht das Ziel darin, die Zeit zu verringern, die für das Rendern von Arbeit aufgewendet wurde.  
    
    > ###### Abbildung 10  
    > Registerkarte "Zusammenfassung"  
    > ![Registerkarte "Zusammenfassung"][ImageSummaryTab]  

1.  Erweitern des **Haupt** Abschnitts  DevTools zeigt Ihnen im Laufe der Zeit ein Flammen Diagramm mit Aktivitäten auf dem Hauptthread.  Die x-Achse steht für die Aufzeichnung im Laufe der Zeit.  Jeder Balken steht für ein Ereignis.  Eine breitere Leiste bedeutet, dass das Ereignis länger dauerte.  Die y-Achse steht für die Aufrufliste.  Wenn Ereignisse übereinander gestapelt angezeigt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.  
    
    > ##### Abbildung 11  
    > Der Hauptabschnitt  
    > ![Der Hauptabschnitt][ImageMainSection]  

1.  Die Aufzeichnung enthält viele Daten.  Vergrößern Sie ein einzelnes Ereignis, indem Sie mit der Maus auf die **Übersicht**klicken, halten und ziehen, wobei es sich um den Abschnitt mit den **fps**-, **CPU**-und **net** -Diagrammen handelt.  Der **Haupt** Abschnitt und die Registerkarte " **Zusammenfassung** " zeigen nur Informationen für den ausgewählten Teil der Aufzeichnung an.  
    
    > ###### Abbildung 12  
    > Vergrößert auf ein einzelnes Ereignis  
    > ![Vergrößert eines Ereignisses][ImageZoomedAnimation]  
    
    > [!NOTE]
    > Eine weitere Möglichkeit zum Zoomen ist das Fokussieren des **Haupt** Abschnitts durch Klicken auf den Hintergrund oder Auswählen eines Ereignisses, und drücken Sie dann die `W` Tasten, und `A` `S` `D` .  
    
    1.  Beachten Sie das rote Dreieck in der oberen rechten Ecke des Ereignisses **Animations Frame ausgelöst** .  Wenn Sie ein rotes Dreieck sehen, ist es eine Warnung, dass möglicherweise ein Problem im Zusammenhang mit diesem Ereignis aufgetreten ist.  
    
    > [!NOTE]
    > Das **ausgelöste Animations Frame** -Ereignis tritt auf, wenn ein [ `requestAnimationFrame()` Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.  
    
1.  Klicken Sie auf das Ereignis **Animations Frame ausgelöst** .  Auf der Registerkarte " **Zusammenfassung** " werden nun Informationen zu diesem Ereignis angezeigt.  Beachten Sie den Link **Reveal** .  Wenn Sie darauf klicken, wird devtools zum Hervorheben des Ereignisses veranlasst, das das ausgelöste **Animations Frame** initiiert hat.  Beachten Sie auch den Link **app. js: 95** .  Durch Klicken auf diese Schaltfläche springen Sie zur entsprechenden Zeile im Quellcode.
    
    > ##### Abbildung 13  
    > Weitere Informationen zum ausgelösten Animations Frame-Ereignis  
    > ![Weitere Informationen zum ausgelösten Animations Frame-Ereignis][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > Verwenden Sie nach dem Auswählen eines Ereignisses die Pfeiltasten, um die Ereignisse daneben auszuwählen.  

1.  Unter dem **app. Update** -Ereignis gibt es eine Reihe von lila Ereignissen.  Wenn Sie breiter waren, sieht es so aus, als ob jedes eine rote Dreiecks Farbe aufweist.  Klicken Sie jetzt auf eines der lila **Layout** -Ereignisse.  DevTools enthält weitere Informationen zu dem Ereignis auf der Registerkarte " **Zusammenfassung** ".  In der Tat gibt es eine Warnung zu erzwungenen Umläufen \ (ein weiteres Wort für das Layout \).  

1.  Klicken Sie auf der Registerkarte **Zusammenfassung** auf den Link **app. js: 71** unter **Layout erzwungen**.  DevTools führt Sie zu der Codezeile, die das Layout erzwungen hat.  
    
    > ##### Abbildung 14  
    > Die Codezeile, die das erzwungene Layout verursacht hat  
    > ![Die Codezeile, die das erzwungene Layout verursacht hat][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > Das Problem mit diesem Code besteht darin, dass in jedem Animationsframe die Formatvorlage für jedes Symbol geändert und dann die Position der einzelnen Symbole auf der Seite abgefragt wird.  Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob sich die einzelnen Symbolpositionen geändert haben, sodass das Symbol neu angeordnet werden muss, um seine Position zu berechnen.  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

Da kommt doch einiges zusammen.  Das war viel zu erledigen, aber Sie haben jetzt eine solide Grundlage im grundlegenden Workflow zum Analysieren der Laufzeitleistung.  Gut Gemacht.  

### Bonus: Analysieren der optimierten Version  

Klicken Sie unter Verwendung der soeben gelernten Workflows und Tools in der Demo auf **optimieren** , um den optimierten Code zu aktivieren, eine andere Leistungsaufnahme durchführen und dann die Ergebnisse zu analysieren.  Von der verbesserten Framerate bis zur Reduzierung von Ereignissen im Flammen Diagramm im **Haupt** Abschnitt können Sie sehen, dass die optimierte Version der APP viel weniger Arbeit leistet, was zu einer besseren Leistung führt.  

> [!NOTE]
> Auch diese "optimierte" Version ist nicht so toll, weil Sie immer noch die `top` Eigenschaft der einzelnen Symbole manipuliert.  Ein besserer Ansatz ist das Beibehalten von Eigenschaften, die sich nur auf die Compositing-Methode auswirken.  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Nächste Schritte

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Um mit dem Leistungsumfang noch komfortabler zu werden, ist die Praxis perfekt.  Versuchen Sie, ihre eigenen Seiten zu profilieren und die Ergebnisse zu analysieren.  Wenn Sie Fragen zu ihren Ergebnissen haben, verwenden Sie das **Feedback** -Symbol, drücken Sie `Alt`  +  `Shift`  +  `I` auf Windows ( `Option`  +  `Shift`  +  `I` unter macOS) oder [tweeten Sie uns][TwitterEdgeDevtools].  Fügen Sie Screenshots oder Links zu reproduzierbaren Seiten hinzu, falls möglich.

> ##### Abbildung 15
> Das **Feedback** Symbol in der Microsoft Edge-devtools  
> ![Das * * Feedback * *-Symbol in der Microsoft Edge-devtools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Schließlich gibt es viele Möglichkeiten, die Laufzeitleistung zu verbessern.  In diesem Lernprogramm wurde auf einen bestimmten Animations Engpass eingegangen, der Ihnen eine gezielte Tour durch das Leistungs Panel ermöglicht, aber nur eine von vielen Engpässen, die Ihnen auftreten können.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
