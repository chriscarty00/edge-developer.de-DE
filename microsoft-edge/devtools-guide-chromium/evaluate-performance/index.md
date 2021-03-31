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

# <a name="get-started-with-analyzing-runtime-performance"></a>Erste Schritte mit der Analyse der Laufzeitleistung  

> [!NOTE]
> Um zu erfahren, wie Sie Ihre Seiten schneller laden können, navigieren Sie zu [Optimieren der Websitegeschwindigkeit][DevtoolsSpeedGetStarted].  

Die Laufzeitleistung ist die Leistung Ihrer Seite, wenn sie ausgeführt wird, statt zu laden.  Im folgenden Lernprogrammartikel erfahren Sie, wie Sie die Laufzeitleistung mithilfe des Microsoft Edge DevTools-Leistungsbereichs analysieren.  Im Hinblick auf das **RAIL-Modell** sind die in diesem Lernprogramm gelernten Kenntnisse nützlich, um die Reaktions-, Animations- und Leerlaufphasen Ihrer Seite zu analysieren.  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a>Erste Schritte  

Im folgenden Lernprogramm öffnen Sie DevTools auf **** einer Liveseite und verwenden den Bereich Leistung, um einen Leistungsengpässe auf der Seite zu finden.  

1.  Öffnen Sie Microsoft Edge im **InPrivate-Modus.**  Der InPrivate-Modus stellt sicher, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.  Wenn Sie z. B. viele Erweiterungen installiert haben, können die Erweiterungen zu Rauschen in Ihren Leistungsmessungen führen.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Laden Sie die folgende Seite in Ihr InPrivate-Fenster.  Die Seite ist die Demo, die Sie profilieren möchten.  Die Seite zeigt eine Reihe kleiner Symbole, die nach oben und unten bewegt werden.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus, um DevTools zu öffnen.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Die Demo auf der linken Seite und DevTools auf der rechten Seite" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       Die Demo auf der linken Seite und DevTools auf der rechten Seite  
    :::image-end:::  
    
    > [!NOTE]
    > Für die restlichen Abbildungen wird DevTools an ein [separates][DevtoolsCustomizePlacement] Fenster gedockt, um sich besser auf den Inhalt zu konzentrieren.  
    
### <a name="simulate-a-mobile-cpu"></a>Simulieren einer mobilen CPU  

Mobile Geräte haben viel weniger CPU-Leistung als Desktops und Laptops.  Verwenden Sie bei jedem Profil einer Seite die CPU-Einschränkung, um die Leistung Ihrer Seite auf mobilen Geräten zu simulieren.  

1.  Wählen Sie in DevTools das **Tool Leistung** aus.  
1.  Stellen Sie sicher, dass Sie das Kontrollkästchen neben **Screenshots auswählen.**  
1.  Wählen **Sie Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ](../media/capture-settings-icon.msft.png) \).  DevTools zeigt Einstellungen im Zusammenhang mit der Erfassung von Leistungsmetriken an.  
1.  Wählen **Sie für CPU**die Option **4x Verlangsamung aus.**  DevTools drosselt die CPU, sodass sie viermal langsamer ist als gewöhnlich.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="CPU-Drosselung" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       CPU-Drosselung  
    :::image-end:::  
    
    > [!NOTE]
    > Beim Testen anderer Seiten; Wenn Sie sicherstellen möchten, dass jede Seite auf mobilen Low-End-Geräten gut funktioniert, legen Sie die CPU-Einschränkung auf **die 6-fache Verlangsamung fest.**  Die Demo funktioniert nicht gut mit der 6x-Verlangsamung, daher verwendet sie nur die 4-fache Verlangsamung für Anweisungszwecke.  
    
### <a name="set-up-the-demo"></a>Einrichten der Demo  

Es ist schwierig, eine Laufzeitleistungsdemo zu erstellen, die für alle Leser der Website konsistent funktioniert.  Im folgenden Abschnitt können Sie die Demo anpassen, um sicherzustellen, dass Ihre Erfahrung relativ konsistent mit den Screenshots und Beschreibungen ist, unabhängig von Ihrer speziellen Einrichtung.

1.  Wählen Sie **die Schaltfläche 10** hinzufügen aus, bis die blauen Symbole merklich langsamer als zuvor bewegt werden.  Auf einem High-End-Computer können Sie ihn etwa 20-mal auswählen.  
1.  Wählen Sie **Optimieren**aus.  Die blauen Symbole sollten sich schneller und reibungsloser bewegen.  
    
    > [!NOTE]
    > Um einen Unterschied zwischen den optimierten und nicht optimierten Versionen besser anzeigen zu können, wählen Sie einige Male die Schaltfläche Subtrahieren **10** aus, und versuchen Sie es erneut.  
    > Wenn Sie zu viele blaue Symbole hinzufügen, können Sie die CPU maximal verwenden, und dann sehen Sie möglicherweise keinen wesentlichen Unterschied in den Ergebnissen für die beiden Versionen.  
    
1.  Wählen **Sie Un-Optimize**aus.  Die blauen Symbole werden langsamer und mit mehr Trägheit wieder bewegt.  
    
### <a name="record-runtime-performance"></a>Aufzeichnen der Laufzeitleistung  

Wenn Sie die optimierte Version der Seite ausgeführt haben, bewegen sich die blauen Symbole schneller.  Weshalb?  Beide Versionen sollen die Symbole in der gleichen Zeit verschieben.  Nehmen Sie eine Aufzeichnung im Bereich Leistung vor, um zu erfahren, wie Sie den Leistungsengpässe in der nicht optimierten Version erkennen.  

1.  Wählen Sie in DevTools **die Option Record** \( Record ![ ](../media/record-icon.msft.png) \).  DevTools erfasst Leistungsmetriken, während die Seite ausgeführt wird.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Profilieren der Seite" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Profilieren der Seite  
    :::image-end:::  
    
1.  Warten Sie einige Sekunden.  
1.  Wählen Sie **Beenden**aus.  DevTools beendet die Aufzeichnung, verarbeitet die Daten und zeigt dann die Ergebnisse im Bereich Leistung an.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Die Ergebnisse des Profils" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Die Ergebnisse des Profils  
    :::image-end:::  
    
Wow, das ist eine übergroße Datenmenge.  machen Sie sich keine Sorgen, bald ist der Prozess sinnvoller.  

## <a name="analyze-the-results"></a>Analysieren der Ergebnisse  

Nachdem Sie die Leistung der Seite aufgezeichnet haben, messen Sie die Qualität der Leistung der Seite, und suchen Sie nach den ursachen.  

### <a name="analyze-frames-per-second"></a>Analysieren von Frames pro Sekunde  

Die Hauptmetrik zum Messen der Leistung einer Animation sind Frames pro Sekunde \(FPS\).  Benutzer freuen sich, wenn Animationen mit 60 FPS ausgeführt werden.  

1.  Überprüfen Sie **das FPS-Diagramm.**  Wenn ein roter Balken über **FPS**angezeigt wird, bedeutet dies, dass die Framerate so niedrig ist, dass sie wahrscheinlich die Benutzerfreundlichkeit geschädigt.  Im Allgemeinen gilt: Je höher der grüne Balken, desto höher der FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Das **#A0**  
    :::image-end:::  
    
1.  Unterhalb **des #A0** wird das **#A1** angezeigt.  Die Farben im **CPU-Diagramm** entsprechen **** den Farben im Zusammenfassungsfenster am unteren Rand des Leistungsbereichs.  Die Tatsache, dass das **CPU-Diagramm** farblich voll ist, bedeutet, dass die CPU während der Aufzeichnung maximal ausgesenert wurde.  Immer wenn die CPU über einen längeren Zeitraum ausgesenkte, ist dies ein Indikator dafür, dass Sie Möglichkeiten finden sollten, weniger Arbeit zu machen.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Das CPU-Diagramm und der Zusammenfassungsbereich" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Das **CPU-Diagramm** und **der Zusammenfassungsbereich**  
    :::image-end:::  
    
1.  Zeigen Sie auf **die FPS-,** **CPU-** oder **NET-Diagramme.**  DevTools zeigt einen Screenshot der Seite zu diesem Zeitpunkt.  Bewegen Sie die Maus nach links und rechts, um die Aufzeichnung wieder zu wiedergeben.  Die Aktion wird als Scrubbing bezeichnet und ist nützlich für die manuelle Analyse des Verlaufs von Animationen.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Anzeigen eines Screenshot der Seite um die 2500-ms-Marke der Aufzeichnung" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Anzeigen eines Screenshot der Seite um die 2500-ms-Marke der Aufzeichnung  
    :::image-end:::  
    
1.  Zeigen Sie **im Abschnitt Frames** auf eines der grünen Quadrate.  DevTools zeigt ihnen den FPS für den jeweiligen Frame an.  Jeder Frame liegt wahrscheinlich deutlich unter dem Ziel von 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Zeigen auf einen Frame" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Zeigen auf einen Frame  
    :::image-end:::  
    
Die Anzeige zeigt natürlich an, dass die Webseite nicht gut funktioniert.  In realen Szenarien ist dies jedoch möglicherweise nicht so klar, sodass alle Tools zum Durchführen von Messungen nützlich sind.  

#### <a name="bonus-open-the-fps-meter"></a>Bonus: Öffnen des FPS-Zählers  

Ein weiteres praktisches Tool ist das FPS-Zähler, das Echtzeitschätzungen für FPS während der Seitenläufe bietet.  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
1.  Beginnen Sie mit der `Rendering` Eingabe im **Befehlsmenü,** und wählen Sie **Rendern anzeigen aus.**  
1.  Aktivieren Sie **im Renderingtool** **FPS Meter**.  Oben rechts im Viewport wird eine neue Überlagerung angezeigt.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       Das **#A0**  
        :::image-end:::  
    
1.  Deaktivieren Sie das **FPS Meter,** und wählen `Escape` Sie aus, um das **Renderingtool zu** schließen.  Sie verwenden **fps Meter** in diesem Lernprogramm nicht.  
    
### <a name="find-the-bottleneck"></a>Suchen des Engpasss  

Nachdem Sie gemessen und überprüft haben, ob die Animation nicht gut funktioniert, besteht der nächste Schritt in der Beantwortung der Frage "Warum?".  

1.  Wenn keine Ereignisse ausgewählt werden, wird im **Zusammenfassungsbereich** eine Aufschlüsselung der Aktivität angezeigt.  Die Seite hat die meiste Zeit mit dem Rendern verbracht.  Da leistung die Kunst ist, weniger Arbeit zu tun, besteht Ihr Ziel in der Reduzierung des Zeitaufwands für Renderingarbeiten.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Der Zusammenfassungsbereich" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Der **Zusammenfassungsbereich**  
    :::image-end:::  
    
1.  Erweitern Sie den **Abschnitt Main.**  DevTools zeigt Ein Flammendiagramm der Aktivität im Hauptthread im Laufe der Zeit.  Die x-Achse stellt die Aufzeichnung im Laufe der Zeit dar.  Jede Leiste stellt ein Ereignis dar.  Ein breiterer Balken bedeutet, dass das Ereignis länger dauerte.  Die y-Achse stellt die Aufrufliste dar.  Wenn Ereignisse übereinander gestapelt werden, bedeutet dies, dass die oberen Ereignisse die niedrigeren Ereignisse verursacht haben.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Der Abschnitt Main" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Der **Abschnitt "Main"**  
    :::image-end:::  
    
1.  Die Aufzeichnung enthält viele Daten.  So zoomen Sie in ein einzelnes Ereignis; Wählen, halten und ziehen Sie den Cursor über die **Übersicht**, die den Abschnitt enthält, der die **FPS-,** **CPU-** und **NET-Diagramme** enthält.  Im **Hauptabschnitt** **und im Zusammenfassungsbereich** werden nur Informationen für den ausgewählten Teil der Aufzeichnung angezeigt.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Zoomen in ein Ereignis" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Zoomen in ein Ereignis  
    :::image-end:::  
    
    > [!NOTE]
    > Eine weitere Möglichkeit zum Zoomen, **Fokussieren** des Hauptabschnitts, Auswählen des Hintergrunds oder eines Ereignisses und Auswählen `W` von , , oder `A` `S` `D` .  
    
    1.  Konzentrieren Sie sich auf das rote Dreieck oben rechts des **Ereignisses Animation Frame Fired.**  Jedes Mal, wenn ein rotes Dreieck angezeigt wird, wird gewarnt, dass es zu einem Problem im Zusammenhang mit dem Ereignis kommt.  
    
    > [!NOTE]
    > Das **Ereignis Animation Frame Fired** tritt auf, wenn ein [requestAnimationFrame()-Rückruf][MDNWebRequestAnimationFrame] ausgeführt wird.  
    
1.  Wählen Sie das **Ereignis Animation Frame Fired** aus.  Im **Zusammenfassungsbereich** werden nun Informationen zu diesem Ereignis angezeigt.  Notieren Sie sich **den Link Reveal.**  Nachdem Sie es markiert haben, hebt DevTools das Ereignis hervor, das das **Ereignis Animation Frame Fired initiiert** hat.  Konzentrieren Sie sich außerdem auf **den linkapp.js:95.**  Nachdem Sie sie auswählen, wird die entsprechende Zeile im Quellcode angezeigt.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Weitere Informationen zum Ereignis Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Weitere Informationen zum **Ereignis Animation Frame Fired**  
    :::image-end:::  
    
    > [!NOTE]
    > Nachdem Sie ein Ereignis ausgewählt haben, wählen Sie mit den Pfeiltasten die Ereignisse daneben aus.  
    
1.  Unter dem **app.update-Ereignis** gibt es eine Reihe von violetten Ereignissen.  Wenn jedes violette Ereignis breiter war, sieht es so aus, als ob jedes einzelne ein rotes Dreieck hat.  
1.  Wählen Sie eines der lila **Layout-Ereignisse** aus.  DevTools bietet weitere Informationen zum Ereignis im **Zusammenfassungsbereich.**  Tatsächlich gibt es eine Warnung über erzwungene Umflüsse \(ein anderes Wort für Layout\).  
    
1.  Wählen Sie **im Bereich** Zusammenfassung den Link **app.js:71** unter **Layout Erzwungen aus.**  DevTools führt Sie zur Codezeile, die das Layout erzwungen hat.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Die Codezeile, die das erzwungene Layout verursacht hat" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Die Codezeile, die das erzwungene Layout verursacht hat  
    :::image-end:::  
    
    > [!NOTE]
    > Das Problem mit dem Code ist, dass er in jedem Animationsframe die Formatvorlage für jedes Symbol ändert und dann die Position der einzelnen Symbole auf der Seite abfragt.  Da die Formatvorlagen geändert wurden, weiß der Browser nicht, ob sich jede Symbolposition geändert hat. Daher muss das Symbol neu layoutt werden, um die neue Position zu berechnen.  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

Das war viel zu lernen.  Sie verfügen nun über eine solide Grundlage im grundlegenden Workflow für die Analyse der Laufzeitleistung.  Gut Gemacht.  

### <a name="bonus-analyze-the-optimized-version"></a>Bonus: Analysieren der optimierten Version  

Wählen Sie mithilfe der Workflows und Tools, die Sie gerade gelernt haben, **optimieren** in der Demo aus, um den optimierten Code zu aktivieren, eine weitere Leistungsaufzeichnung zu erstellen und die Ergebnisse zu analysieren.  Von der verbesserten Framerate bis zur Reduzierung der Ereignisse im Flammendiagramm im **Abschnitt Main** führt die optimierte Version der App wesentlich weniger Arbeit, was zu einer besseren Leistung führt.  

> [!NOTE]
> Auch die optimierte Version ist nicht großartig, da sie die `top` Eigenschaft jedes Symbols bearbeitet.  Ein besserer Ansatz ist, sich an Eigenschaften zu halten, die sich nur auf das Compositing auswirken.  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a>Nächste Schritte

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

Damit Sie sich mit dem **Tool "Leistung"** bequemer machen können, ist die Übung perfekt.  Versuchen Sie, Ihre Seiten zu profilieren und die Ergebnisse zu analysieren.  Wenn Sie Fragen zu Ihren Ergebnissen **** haben, verwenden Sie das Symbol Feedback senden, wählen `Alt` + `Shift` + `I` Sie \(Windows, Linux\), wählen `Option` + `Shift` + `I` Sie \(macOS\) aus, [][TwitterEdgeDevtools]oder twittern Sie das DevTools-Team .  Fügen Sie nach Möglichkeit Screenshots oder Links zu reproduzierbaren Seiten hinzu.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Das Symbol **Feedback** in den Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Das Symbol **Feedback senden** in den Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Last, there are many ways to improve runtime performance.  Dieser Artikel konzentrierte sich auf einen bestimmten Animationsengpässe, um Ihnen eine konzentrierte Tour durch den Bereich Leistung zu bieten, aber es ist nur einer von vielen Engpässen, die Sie möglicherweise haben.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

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
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
