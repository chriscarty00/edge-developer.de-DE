---
description: Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen, z. B. den Textkontrast während des Hoverzustands, im Bereich "Formatvorlagen" mithilfe des Toggle-Elementstatus.
title: Überprüfen der Barrierefreiheit aller Zustände von Elementen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597443"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a>Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen

<!-- 5. STYLES: TOGGLE STATE -->

Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen, z. B. den Kontrast der Textfarbe während des `hover` Zustands.  Das **Tool Inspect** meldet Barrierefreiheitsprobleme für jeweils einen Status.  Um die Barrierefreiheit der verschiedenen Zustände von Elementen zu überprüfen, wählen Sie auf der Registerkarte **Formatvorlagen** **\:hov** (**Toggle Element State**), wie in diesem Artikel beschrieben. Wir zeigen zunächst, warum die Zustandssimulation mit dem **Inspect-Tool** erforderlich ist, und dann zeigen wir, wie Zustandssimulationen verwendet werden.


## <a name="checking-text-color-contrast-in-the-default-state"></a>Überprüfen des Textfarbkontrasts im Standardzustand

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Zusätzlich zu den automatischen Farbkontrasttests im Tool **"Probleme"** können Sie auch das **Tool Inspect** verwenden, um zu überprüfen, ob einzelne Seitenelemente über genügend Kontrast verfügen.  Wenn Kontrastinformationen verfügbar **** sind, zeigt die Inspect-Überlagerung das Kontrastverhältnis und ein Kontrollkästchenelement an.  Ein grünes Häkchensymbol zeigt an, dass genügend Kontrast vorhanden ist, und ein gelbes Warnsymbol zeigt an, dass nicht genügend Kontrast vorhanden ist.

Beispielsweise weisen die Links im Navigationsmenü der Seitenleiste ausreichend Kontrast auf.  Das grüne **Listenelement "Hunde"** im Abschnitt **"Schenkungsstatus"** hat jedoch nicht genügend Kontrast und wird daher durch eine Warnung in der **Inspect-Überlagerung** gekennzeichnet.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Die Links im Navigationsmenü der Seitenleiste weisen ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt." lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Die Links im Navigationsmenü der Seitenleiste weisen **** ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt. :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Ein Element, das nicht über genügend Kontrast verfügt, wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet." lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Ein Element, das nicht über genügend Kontrast verfügt, **** wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet. :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a>Beim Bewegen des Mauszeigers, wenn das Tool Inspect aktiv ist, wird der Textfarbkontrast für den Hoverzustand nicht angezeigt.

Die Informationsüberlagerung des **Tools Inspect** stellt nur einen einzelnen Zustand dar.  Elemente auf der Seite können unterschiedliche Zustände aufweisen, die alle getestet werden müssen.  Wenn Sie beispielsweise mit dem Mauszeiger über das Menü der Demoseite für Barrierefreiheitstests zeigen, erhalten Sie eine Animation, die die Farben ändert. Führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.

1.  Zeigen Sie auf die blauen Menüelemente im Seitenleisten-Navigationsmenü.  Beachten Sie, dass jedes Element über eine Animation verfügt.

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet" lightbox="../media/a11y-testing-hover.msft.png":::
        Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet
    :::image-end:::
    
Verwenden Sie nun das Tool Inspect. Wenn das Tool Inspect verwendet wird, werden Animationen für die Menüelemente nicht ausgeführt, wenn Sie mit dem Mauszeiger darauf zeigen.  Wenn Sie das Tool Inspect verwenden, können Sie den Status für Menüelemente nicht `hover` erreichen, um das Kontrastverhältnis zu testen, da der `hover` Status in Ihren Formatvorlagen nicht ausgelöst wird.  
    
Führen Sie die folgenden Schritte aus, um zu bestätigen, dass die Animationen nicht ausgeführt werden.
    
1.  Wählen **** Sie in der oberen linken Ecke von DevTools die Schaltfläche Überprüfen ![ \( Schaltfläche Überprüfen ](../media/inspect-icon.msft.png) aus, damit das Symbol hervorgehoben wird (blau).

1.  Zeigen Sie auf die blauen Links im Navigationsmenü der Seitenleiste.  Die Animationen für die Menüelemente werden nicht ausgeführt. Stattdessen werden die Menüelemente mit Farben und Hervorhebungen für die Flexbox-Überlagerung angezeigt.

Die Überprüfung auf einen ausreichenden Textkontrast auf diese Weise reicht nicht aus, da die Elemente auf der Seite unterschiedliche Zustände aufweisen können.


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a>Verwenden der Zustandssimulation zum Simulieren des Hoverzustands eines animierten Menüelements 

<!-- Elements tool: Styles pane: Toggle Element State -->

Wenn das **Inspect-Tool** aktiv ist, müssen Sie den Status des Menüelements simulieren, anstatt mit dem Mauszeiger auf ein animiertes Element zu zeigen.  Um den Status eines Menüelements zu simulieren, verwenden Sie die Zustandssimulation im Bereich **"Formatvorlagen".**  Der Bereich **Formatvorlagen** verfügt über die Schaltfläche **\:hov** (**Toggle Element State**), die eine Gruppe von Kontrollkästchen mit der Bezeichnung **"Force"-Elementstatus**anzeigt.

So aktivieren Sie den Hoverzustand während der Verwendung des Inspect-Tools:

1.  Wenn es noch nicht geöffnet ist, öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie die Schaltfläche **"Inspect** \( ![ Inspect tool button ](../media/inspect-icon.msft.png) \) " in der oberen linken Ecke von DevTools aus, sodass das Symbol hervorgehoben ist (blau).

1.  Wählen Sie auf der gerenderten Webseite den blauen **Katzenlink** im Seitenleisten-Navigationsmenü aus.  Das **** Elementtool wird geöffnet, wobei das Element `<a href="#cats">Cats</a>` ausgewählt ist.

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Überprüfen des Elements mit einem Hoverstatus im Elementtool" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        Überprüfen des Elements mit einem Hoverstatus im Elementtool
    :::image-end:::

1.  Wählen Sie die Registerkarte **"Formatvorlagen" aus.**  Das ausgewählte `a` Element weist einen Zustand im CSS `hover` auf, der darauf angewendet wird, aber im Bereich **"Formatvorlagen"** nicht sichtbar ist. 

1.  Wählen Sie im Bereich **"Formatvorlagen"** rechts neben der Formatvorlagenregel `#sidebar nav li a` den Link `styles.css` aus.  Das **Tool "Quellen"** wird geöffnet.  Suchen Sie dann die CSS-Pseudoklassenregel. `#sidebar nav li a:hover`  Diese Regel wird nicht ausgeführt, wenn das **Tool Inspect** aktiv ist.  In den nächsten Schritten wird die Ausführung dieser Zustandsregel simuliert.

1.  Wählen Sie das Elementtool **aus.**  Wählen Sie dann im Bereich **"Formatvorlagen"** die Schaltfläche **:hov** (**Toggle Element State**) aus.  Die **Force-Elementstatusgruppe** der Kontrollkästchen wird angezeigt.

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Das Zustandssimulationstool mit allen Optionen" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        Das Zustandssimulationstool mit allen Optionen
    :::image-end:::

1.  Aktivieren Sie das **Kontrollkästchen :hover.**  Im DOM wird links neben dem Element `<a href="#cats">Cats</a>` ein gelber Punkt angezeigt, der angibt, dass das Element einen simulierten Zustand aufweist.  Das **Menüelement "Katzen"** wird nun auf der Webseite angezeigt, als würde der Zeiger darauf zeigen.  Die Animation für das Menüelement kann ausgeführt werden.

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulieren einen Hoverzustand" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        DevTools simulieren einen Hoverzustand
    :::image-end:::

    Nachdem der simulierte Zustand angewendet wurde, können Sie das **Inspect-Tool** erneut verwenden, um den Kontrast des Elements zu überprüfen, wenn der Benutzer mit dem Mauszeiger darauf zeigt, wie folgt.

1.  Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Inspektorsymbol \) " ](../media/inspect-icon.msft.png) aus, damit das Symbol hervorgehoben ist (blau).

1.  Zeigen Sie im Navigationsmenü der Seitenleiste auf den blauen **Katzenlink.**  Der Link ist nun hellblau, aufgrund der simulierten Hoveranimation.  Die Informationsüberlagerung des **Inspect-Tools** wird mit einem orangefarbenen Ausrufezeichen in der **Zeile "Kontrast"** angezeigt, das angibt, dass der Kontrast nicht hoch genug ist.

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testen des Kontrasts eines Elements in einem simulierten Hoverzustand" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        Testen des Kontrasts eines Elements in einem simulierten Hoverzustand
    :::image-end:::

Die Zustandssimulation ist auch eine gute Möglichkeit, um zu überprüfen, ob Sie unterschiedliche Benutzeranforderungen berücksichtigt haben, z. B. die Anforderungen von Tastaturbenutzern.  Mithilfe der Kontrollkästchen für den **Force-Elementstatus** können Sie den Zustand simulieren, `:focus` um festzustellen, dass die Benutzeroberfläche unverändert bleibt, wenn sie den Fokus hat. Dieses Fehlen eines Indikators, wenn ein Element den Fokus hat, ist ein Problem.


## <a name="see-also"></a>Weitere Informationen:

*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
