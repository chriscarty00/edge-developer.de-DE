---
description: Erfahren Sie, wie Sie die Laufzeitleistung in Microsoft Edge devtools.
title: Erste Schritte mit der Analyse der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 65351f3846ed76ef8a27dbff2cfb08c497282d15
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992946"
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
> Informationen dazu, wie Sie Ihre Seiten schneller laden können, finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted].  

Die Laufzeitleistung ist die Art und Weise, wie Ihre Seite ausführt, wenn Sie ausgeführt wird, im Gegensatz zum Laden.  Im folgenden Lernprogramm Artikel erfahren Sie, wie Sie das Microsoft Edge devtools-Leistungs Panel verwenden, um die Runtime-Leistung zu analysieren.  Im Hinblick auf das **Schienen** Modell sind die in diesem Lernprogramm gelernten Kenntnisse hilfreich, um die Reaktions-, Animations-und Leerlaufphasen Ihrer Seite zu analysieren.  

<!--todo: add rail link when section is ready -->  

## Erste Schritte  

Im folgenden Lernprogramm öffnen Sie devtools auf einer Live Seite und verwenden den **Leistungs** Panel, um einen Leistungsengpass auf der Seite zu finden.  

1.  Öffnen Sie Microsoft Edge im **InPrivate-Modus**.  Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.  Wenn Sie beispielsweise viele Erweiterungen installiert haben, können die Erweiterungen zu Lärm in ihren Leistungsmessungen führen.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Laden Sie die folgende Seite in Ihrem InPrivate-Fenster.  Bei der Seite handelt es sich um die Demo, die Sie profilieren möchten.  Auf der Seite werden einige kleine Symbole angezeigt, die sich nach oben und unten bewegen.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Wählen Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \) aus, um devtools zu öffnen.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Die Demo auf der linken Seite und DevTools auf der rechten Seite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       Die Demo auf der linken Seite und DevTools auf der rechten Seite  
    :::image-end:::  
    
    > [!NOTE]
    > Für die restlichen Zahlen wird devtools [an einem separaten Fenster Abdocken][DevtoolsCustomizePlacement] , um sich besser auf den Inhalt zu konzentrieren.  
    
### Simulieren einer mobilen CPU  

Mobile Geräte haben viel weniger Prozessorleistung als Desktops und Laptops.  Wenn Sie eine Seite profilieren, simulieren Sie mithilfe der CPU-Drosselung, wie Ihre Seite auf mobilen Geräten ausgeführt wird.  

1.  Wählen Sie in devtools die Registerkarte **Leistung** aus.  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Screenshots** aktiviert ist.  
1.  Wählen Sie **aufnahmeeinstellungen** \ (! [ Aufnahmeeinstellungen] [ImageCaptureSettingsIcon] \).  DevTools zeigt Einstellungen in Bezug auf die Erfassung von Leistungs Metriken an.  
1.  Wählen Sie für **CPU**die Option **4X Verlangsamung**aus.  DevTools drosselt Ihre CPU so, dass Sie viermal langsamer als üblich ist.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="CPU-Drosselung" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       CPU-Drosselung  
    :::image-end:::  
    
    > [!NOTE]
    > Beim Testen anderer Seiten; Wenn Sie sicherstellen möchten, dass jede Seite auf Low-End-mobilen Geräten gut funktioniert, legen Sie die CPU-Drosselung auf **6x Verlangsamung**fest.  Die Demo funktioniert nicht gut mit einer 6x Verlangsamung, sodass Sie nur eine vierfache Verlangsamung für Unterrichtszwecke verwendet.  
    
### Einrichten der Demo  

Es ist schwierig, eine Demo zur Laufzeit-Performance zu erstellen, die für alle Leser der Website konsistent funktioniert.  Im folgenden Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung mit den Screenshots und Beschreibungen relativ konsistent ist, unabhängig von der jeweiligen Einrichtung.

1.  Wählen Sie die Schaltfläche " **10 hinzufügen** " aus, bis sich die blauen Symbole merklich langsamer bewegen.  Auf einem Highend-Computer können Sie die Datei etwa 20 Mal auswählen.  
1.  Wählen Sie **optimieren**aus.  Die blauen Symbole sollten sich schneller und reibungsloser bewegen.  
    
    > [!NOTE]
    > Um einen Unterschied zwischen den optimierten und nicht optimierten Versionen besser anzuzeigen, wählen Sie die Schaltfläche **10 subtrahieren** einige Male aus, und versuchen Sie es erneut.  
    > Wenn Sie zu viele blaue Symbole hinzufügen, ist es möglich, dass Sie die CPU maximal auszahlen, und es ist möglich, dass Sie keinen großen Unterschied in den Ergebnissen für die beiden Versionen beobachten.  
    
1.  Wählen Sie **UN-Optimize**aus.  Die blauen Symbole bewegen sich langsamer und mit mehr Trägheit wieder.  
    
### Aufzeichnen der Laufzeitleistung  

Wenn Sie die optimierte Version der Seite ausgeführt haben, werden die blauen Symbole schneller verschoben.  Weshalb?  Beide Versionen sollen die Symbole in derselben Zeitdauer auf die gleiche Menge an Speicherplatz verschieben.  Nehmen Sie im Leistungs Panel eine Aufzeichnung auf, um zu erfahren, wie Sie den Leistungsengpass in der nicht optimierten Version erkennen.  

1.  Wählen Sie in devtools die Option **Record** \ (! [ Record] [ImageRecordIcon] \).  DevTools erfasst Leistungs Metriken während der Ausführung der Seite.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profil der Seite" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Profil der Seite  
    :::image-end:::  
    
1.  Warten Sie ein paar Sekunden.  
1.  Wählen Sie **Beenden**aus.  DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Leistungs Panel an.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Die Ergebnisse des Profils" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Die Ergebnisse des Profils  
    :::image-end:::  
    
Wow, das ist eine überwältigende Menge an Daten.  machen Sie sich keine Sorgen, schon bald macht der Prozess Sinn.  

## Analysieren der Ergebnisse  

Nachdem Sie die Leistung der Seite aufgezeichnet haben, Messen Sie die Qualität der Leistung der Seite, und ermitteln Sie die Ursachen.  

### Analysieren von Frames pro Sekunde  

Die wichtigste Metrik zum Messen der Leistung einer Animation ist Frames pro Sekunde \ (fps \).  Benutzer sind zufrieden, wenn Animationen mit 60 fps ausgeführt werden.  

1.  Schauen Sie sich das **fps** -Diagramm an.  Wenn Sie eine rote Leiste oberhalb von **fps**sehen, bedeutet dies, dass die Framerate so gering ist, dass Sie die Benutzerfreundlichkeit wahrscheinlich beeinträchtigt.  Je höher die grüne Leiste, desto höher der FPS-Wert.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Das fps-Diagramm" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Das **fps** -Diagramm  
    :::image-end:::  
    
1.  Unterhalb des **fps** -Diagramms wird das **CPU** -Diagramm angezeigt.  Die Farben im **CPU** -Diagramm entsprechen den Farben auf der Registerkarte " **Zusammenfassung** " unten im Leistungsbereich.  Die Tatsache, dass das **CPU** -Diagramm Farb voll ist, bedeutet, dass die CPU während der Aufzeichnung ausgereizt wurde.  Wenn Sie sehen, dass die CPU über einen längeren Zeitraum ausgeschöpft ist, ist es ein Anhaltspunkt, wie Sie Möglichkeiten für eine geringere Arbeit finden.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Das CPU-Diagramm und die Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Das **CPU** -Diagramm und die Registerkarte " **Zusammenfassung** "  
    :::image-end:::  
    
1.  Zeigen Sie auf die **fps**-, **CPU**-oder **net** -Diagramme.  DevTools zeigt zu diesem Zeitpunkt einen Screenshot der Seite an.  Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wiederzugeben.  Die Aktion wird als Scrubbing referenziert, und Sie ist nützlich, um den Fortschritt von Animationen manuell zu analysieren.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Anzeigen eines Screenshot der Seite um das 2500ms-Zeichen der Aufzeichnung  
    :::image-end:::  
    
1.  Zeigen Sie im Abschnitt **Frames** auf eines der grünen Quadrate.  DevTools zeigt Ihnen die fps für diesen bestimmten Frame.  Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 fps.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Bewegen des Mauszeigers auf einem Frame" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Bewegen des Mauszeigers auf einem Frame  
    :::image-end:::  
    
Natürlich sollten Sie sehen, dass die Seite nicht gut funktioniert.  In realen Szenarien ist es aber möglicherweise nicht so klar, dass alle Tools für die Messung praktisch sind.  

#### Bonus: Öffnen des FPS-meters  

Ein weiteres praktisches Tool ist das FPS-Messgerät, das in Echtzeit Schätzungen für FPS bereitstellt, während die Seite ausgeführt wird.  

1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.  
1.  Beginnen `Rendering` Sie mit der Eingabe im **Befehlsmenü** , und wählen Sie **Rendering anzeigen**aus.  
1.  Aktivieren Sie auf der Registerkarte **Rendern** die Option **FPS-Meter**.  In der oberen rechten Ecke des Viewports wird eine neue Überlagerung angezeigt.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Das fps-Messgerät" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       Das **fps-Messgerät**  
        :::image-end:::  
    
1.  Deaktivieren Sie das **fps-Messgerät** , und wählen Sie aus `Escape` , um die Registerkarte **Rendering** zu schließen.  In diesem Lernprogramm verwenden Sie nicht **FPS-Meter** .  
    
### Ermitteln des Engpasses  

Nachdem Sie gemessen und überprüft haben, dass die Animation nicht gut funktioniert, besteht der nächste Schritt darin, die Frage "Warum?" zu beantworten.  

1.  Wenn keine Ereignisse ausgewählt sind, wird auf der Registerkarte **Zusammenfassung** eine Aufschlüsselung der Aktivitäten angezeigt.  Die Seite verbrachte die meiste Zeit beim Rendern.  Da Leistung die Kunst ist, weniger Arbeit zu erledigen, besteht das Ziel darin, die Zeit zu verringern, die für das Rendern von Arbeit aufgewendet wurde.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Registerkarte "Zusammenfassung"" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Registerkarte " **Zusammenfassung** "  
    :::image-end:::  
    
1.  Erweitern des **Haupt** Abschnitts  DevTools zeigt Ihnen im Laufe der Zeit ein Flammen Diagramm mit Aktivitäten auf dem Hauptthread.  Die x-Achse steht für die Aufzeichnung im Laufe der Zeit.  Jeder Balken steht für ein Ereignis.  Eine breitere Leiste bedeutet, dass das Ereignis länger dauerte.  Die y-Achse steht für die Aufrufliste.  Wenn Ereignisse übereinander gestapelt angezeigt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Der Hauptabschnitt" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Der **Haupt** Abschnitt  
    :::image-end:::  
    
1.  Die Aufzeichnung enthält viele Daten.  So zoomen Sie in ein einzelnes Ereignis Wählen Sie den Mauszeiger über der **Übersicht**aus, halten Sie ihn gedrückt, und ziehen Sie ihn in den Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.  Der **Haupt** Abschnitt und die Registerkarte " **Zusammenfassung** " zeigen nur Informationen für den ausgewählten Teil der Aufzeichnung an.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Vergrößern eines Ereignisses" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Vergrößern eines Ereignisses  
    :::image-end:::  
    
    > [!NOTE]
    > Eine weitere Möglichkeit zum Zoomen, zum Fokussieren des **Haupt** Abschnitts, zum Auswählen des Hintergrunds oder eines Ereignisses und zum auswählen `W` ,, `A` `S` oder `D` .  
    
    1.  Konzentrieren Sie sich auf das rote Dreieck in der oberen rechten Ecke des Ereignisses **Animations Frame ausgelöst** .  Wenn Sie ein rotes Dreieck sehen, wird eine Warnung angezeigt, dass ein Problem im Zusammenhang mit dem Ereignis auftreten kann.  
    
    > [!NOTE]
    > Das **ausgelöste Animations Frame** -Ereignis tritt auf, wenn ein [ `requestAnimationFrame()` Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.  
    
1.  Wählen Sie das **ausgelöste Animations Frame** -Ereignis aus.  Auf der Registerkarte " **Zusammenfassung** " werden nun Informationen zu diesem Ereignis angezeigt.  Beachten Sie den Link **Reveal** .  Nachdem Sie Sie ausgewählt haben, hebt devtools das Ereignis hervor, das das ausgelöste **Animations Frame** -Ereignis initiiert hat.  Konzentrieren Sie sich auch auf den Link **app.js:95** .  Nachdem Sie Sie ausgewählt haben, wird die entsprechende Zeile im Quellcode angezeigt.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Weitere Informationen zum ausgelösten Animations Frame-Ereignis" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Weitere Informationen zum **ausgelösten Animations Frame** -Ereignis  
    :::image-end:::  
    
    > [!NOTE]
    > Verwenden Sie nach dem Auswählen eines Ereignisses die Pfeiltasten, um die Ereignisse daneben auszuwählen.  
    
1.  Unter dem **app. Update** -Ereignis gibt es eine Reihe von lila Ereignissen.  Wenn jedes violette Ereignis breiter war, sieht es so aus, als ob jeder ein rotes Dreieck darauf haben kann.  
1.  Wählen Sie eines der lila **Layout** -Ereignisse aus.  DevTools enthält weitere Informationen zu dem Ereignis auf der Registerkarte " **Zusammenfassung** ".  In der Tat gibt es eine Warnung zu erzwungenen Umläufen \ (ein weiteres Wort für das Layout \).  
    
1.  Wählen Sie auf der Registerkarte **Zusammenfassung** den Link **app.js:71** unter **Layout erzwungen**aus.  DevTools führt Sie zu der Codezeile, die das Layout erzwungen hat.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Die Codezeile, die das erzwungene Layout verursacht hat" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Die Codezeile, die das erzwungene Layout verursacht hat  
    :::image-end:::  
    
    > [!NOTE]
    > Das Problem mit dem Code besteht darin, dass in jedem Animationsframe die Formatvorlage für jedes Symbol geändert und dann die Position der einzelnen Symbole auf der Seite abgefragt wird.  Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob jede Symbolposition geändert wurde, sodass das Symbol neu angeordnet werden muss, um die neue Position zu berechnen.  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

Das war viel zu lernen.  Sie verfügen jetzt über eine solide Grundlage im grundlegenden Workflow zum Analysieren der Laufzeitleistung.  Gut Gemacht.  

### Bonus: Analysieren der optimierten Version  

Wählen Sie mithilfe der soeben gelernten Workflows und Tools in der Demo **optimieren** aus, um den optimierten Code zu aktivieren, eine andere Leistungsaufnahme durchführen und dann die Ergebnisse zu analysieren.  Von der verbesserten Framerate bis zur Reduzierung von Ereignissen im Flammen Diagramm im **Haupt** Abschnitt können Sie feststellen, dass die optimierte Version der APP viel weniger Arbeit leistet, was zu einer besseren Leistung führt.  

> [!NOTE]
> Auch die optimierte Version ist nicht optimal, da Sie die `top` Eigenschaft jedes Symbols manipuliert.  Ein besserer Ansatz ist das Beibehalten von Eigenschaften, die sich nur auf die Compositing-Methode auswirken.  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Nächste Schritte

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Um mit dem Leistungsumfang noch komfortabler zu werden, ist die Praxis perfekt.  Versuchen Sie, Ihre Seiten zu profilieren und die Ergebnisse zu analysieren.  Wenn Sie Fragen zu ihren Ergebnissen haben, verwenden Sie das Symbol **Feedback senden** , wählen Sie `Alt` + `Shift` + `I` \ (Windows \) aus, wählen Sie `Option` + `Shift` + `I` \ (macOS \) aus, oder [tweeten Sie das devtools-Team][TwitterEdgeDevtools].  Fügen Sie Screenshots oder Links zu reproduzierbaren Seiten hinzu, falls möglich.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Das * * Feedback * *-Symbol in der Microsoft Edge-devtools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Das Symbol " **Feedback senden** " im Microsoft Edge-devtools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Schließlich gibt es viele Möglichkeiten, die Laufzeitleistung zu verbessern.  Dieser Artikel befasst sich mit einem bestimmten Animations Engpass, der Ihnen eine gezielte Tour durch das Leistungs Panel ermöglicht, aber nur eine von vielen Engpässen, die Ihnen auftreten können.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
