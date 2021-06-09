---
description: Überprüfen Sie den Kontrast der Textfarbe im Standardzustand, indem Sie die Informationsüberlagerung des Tools "Inspect" auf der Seite verwenden, die über einen Abschnitt "Barrierefreiheit" verfügt, der Kontrastinformationen enthält.
title: Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597413"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a>Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Überprüfen Sie den Kontrast der Textfarbe im Standardzustand, indem Sie das Tool **Inspect** verwenden.  Die Informationsüberlagerung des **Tools "Inspect"** auf der Webseite verfügt über einen Abschnitt **"Barrierefreiheit",** der **Kontrastinformationen** enthält.

Führen Sie die folgenden Schritte aus, um den Textfarbkontrast im Standardzustand mithilfe der Informationsüberlagerung des Tools Inspect zu überprüfen.

<!-- Inspect tool -->
Für Elemente mit Text zeigt die Informationsüberlagerung des **Inspect-Tools** Folgendes an:
*  Das Kontrastverhältnis zwischen Text und Hintergrundfarben.
*  Ein grünes Häkchensymbol für Elemente mit genügend Kontrast.
*  Ein gelbes Warnsymbol für Elemente, die nicht über genügend Kontrast verfügen.

In einigen Fällen wird der Kontrast beeinflusst, indem der Browser auf helles oder dunkles Design festgelegt wird.

Auf der Demoseite haben beispielsweise die blauen Links des Navigationsmenüs auf der Seitenleiste genügend Kontrast, aber der grüne Link **"Hunde"** im Abschnitt **"Schenkungsstatus"** hat nicht genügend Kontrast.  Überprüfen Sie diese **** Elemente wie folgt mithilfe des Inspect-Tools:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Schaltfläche ](../media/inspect-icon.msft.png) überprüfen\) aus, damit das Symbol hervorgehoben wird (blau).

1.  Zeigen Sie auf der gerenderten Webseite über den blauen **Katzenlink** des Navigationsmenüs in der Seitenleiste.  Die Informationsüberlagerung des **Tools "Überprüfen"** wird angezeigt.  Im Abschnitt **"Barrierefreiheit"** der Informationsüberlagerung wird in der Zeile ** Contrast ** ein grünes Häkchen angezeigt, das angibt, dass dieses Element über genügend Kontrast zwischen Textfarbe und Hintergrundfarbe verfügt.

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Die Menüelemente weisen genügend Kontrast auf, wie im Inspect-Tool dargestellt." lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        Die Menüelemente weisen genügend Kontrast auf, wie im Inspect-Tool dargestellt.
    :::image-end:::

1.  Zeigen Sie auf der gerenderten Webseite im Abschnitt **"Schenkungsstatus"** auf den Link **"Hunde".**  Die Informationsüberlagerung des **Inspect-Tools** zeigt ein orangefarbenes Ausrufezeichen in der **Zeile "Kontrast",** das angibt, dass dieses Element nicht über genügend Kontrast zwischen Text und Hintergrundfarben verfügt.

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Ein Element, das nicht über genügend Kontrast verfügt, wie die Warnung im Inspect-Tool zeigt" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        Ein Element, das nicht über genügend Kontrast verfügt, wie die Warnung im Inspect-Tool zeigt
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a>Verschiedene Optionen zum Überprüfen des Kontrasts von Textfarben in DevTools

Verwenden Sie die folgenden DevTools-Features, um den Kontrast von Textfarben zu überprüfen.

*  Verwenden Sie das **Tool Inspect** (als Informationsüberlagerung auf der Webseite), um zu überprüfen, ob ein einzelnes Seitenelement über genügend Textfarbkontrast verfügt.  Die Informationsüberlagerung des **Tools "Inspect"** enthält einen Abschnitt **"Barrierefreiheit",** der über eine Zeile mit **Kontrastinformationen** verfügt.  Das **Tool Inspect** zeigt nur Informationen zum Textkontrast für den aktuellen Zustand an.  Dieser Ansatz wird im aktuellen Artikel beschrieben.

*  Das Tool **"Probleme"** meldet automatisch alle Farbkontrastprobleme für die gesamte Webseite, wenn Text- und Hintergrundfarbe nicht ausreichend kontrastreich sind.  Dieser Ansatz wird unter [Überprüfen beschrieben, ob Textfarben genügend Kontrast aufweisen.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)

*  Emulieren Eines nicht standardmäßigen Zustands, z. B. des `hover` Zustands, mithilfe von **Toggle Element State** im Bereich **Formatvorlagen,** beschrieben unter [Überprüfen der Barrierefreiheit aller Zustände von Elementen.](test-inspect-states.md)


## <a name="see-also"></a>Weitere Informationen:

*  [Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen][DevtoolsAccessibilityTestInspectStates]
*  [Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen](test-inspect-tool.md)
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Überprüfen der Barrierefreiheit aller Zustände von Elementen | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
