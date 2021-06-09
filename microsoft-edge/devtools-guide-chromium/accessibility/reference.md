---
description: Eine Liste der Features zum Testen der Barrierefreiheit in Microsoft Edge DevTools.
title: Features für Barrierefreiheitstests in DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a906d60bb74d927fd86c21af1535a8f62eb93cad
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597037"
---
# <a name="accessibility-testing-features-in-devtools"></a>Features für Barrierefreiheitstests in DevTools

Um Ihre Webseiten auf Barrierefreiheit zu testen, erstellen Sie zunächst eine Prüfliste mit zu testigen Aspekten der Barrierefreiheit, und verwenden Sie dann die relevanten DevTools-Features, um jeden Aspekt zu überprüfen.

| Zu überprüfende Barrierefreiheitsaspekt | Feature von DevTools | Artikel oder Unterüberschrift |
|---|---|---|
| Stellen Sie sicher, dass Bilder über alt-Text verfügen | **Problemtool** > Abschnitt **"Barrierefreiheit"** des Berichts | [Stellen Sie sicher, dass Bilder über alt-Text verfügen](test-issues-tool.md#verify-that-images-have-alt-text) |
| Überprüfen der Tastaturunterstützung | **Überprüfen** des Tools > **Barrierefreiheitsbereichs** der Überlagerung | [Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen](test-inspect-tool.md) |
| Überprüfen der Tastaturunterstützung | `Tab``Shift+Tab`, und `Enter` Schlüsseln | [Überprüfen Sie die Tastaturunterstützung mithilfe der Tab- und Eingabetasten](test-tab-enter-keys.md) |
| Überprüfen der Tastaturunterstützung: Überprüfen, ob der Fokus angegeben ist | **Tool,** Registerkarte **"Formatvorlagen"** und **"Quellen"** überprüfen | [Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü](test-analyze-no-focus-indicator.md) |
| Überprüfen der Tastaturunterstützung: Überprüfen, ob Formularschaltflächen mit der Tastatur verwendet werden können | **Überprüfungstool,** **DOM-Struktur** im **Elementtool** und **Registerkarte "Ereignislistener"** | [Analysieren Sie die fehlende Tastaturunterstützung in einem Formular](test-analyze-no-keyboard-support.md) |
| Überprüfen der Tastaturunterstützung: Überprüfen der `Tab` Tastenreihenfolge | **Elementtool** > Registerkarte **"Barrierefreiheit"** > **Source Order Viewer** | [Testen Sie die Tastaturunterstützung mithilfe des Source Order Viewers](test-tab-key-source-order-viewer.md) |
| Stellen Sie sicher, dass Text über ausreichend Kontrast verfügt (automatisch für die gesamte Seite). | **Problemtool** > Abschnitt **"Barrierefreiheit"** des Berichts | [Sicherstellen, dass Textfarben über genügend Kontrast verfügen](test-issues-tool.md#verify-that-text-colors-have-enough-contrast) |
| Sicherstellen, dass Text über genügend Kontrast verfügt | **Elementtool** > Registerkarte **"Formatvorlagen"** > **Farbauswahl** | [Testen Sie den Kontrast von Text und Farbe mithilfe des Farbwählers](color-picker.md) |
| Sicherstellen, dass Text über genügend Kontrast verfügt | **Überprüfen** des Tools > Abschnitt **"Barrierefreiheit"** der Überlagerung > **Zeile "Kontrast"** | [Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen](test-inspect-tool.md) |
| Stellen Sie sicher, dass Text genügend Kontrast aufweist: im Hoverzustand | **Elementtool** > Registerkarte **"Formatvorlagen"** > **"Elementstatus umschalten"** | [Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen](test-inspect-states.md) |
| Stellen Sie sicher, dass Text genügend Kontrast aufweist: mit dunklem Design (dunklem Modus) und hellem Design | **Renderingtool** > **Emulieren des CSS-Medienfeatures "Prefers-Color"-Schema** | [Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design](test-dark-mode.md) |
| Überprüfen der Sprachausgabeunterstützung: Überprüfen, ob Eingabefelder Bezeichnungen aufweisen | **Problemtool** > Abschnitt **"Barrierefreiheit"** des Berichts | [Überprüfen, ob Eingabefelder Bezeichnungen aufweisen](test-issues-tool.md#verify-that-input-fields-have-labels) |
| Überprüfen der Sprachausgabeunterstützung | **Überprüfen des** Tools > Abschnitt **"Barrierefreiheit"** der Überlagerung > **Name** und **Rolle** | [Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen](test-inspect-tool.md) |
| Überprüfen der Sprachausgabeunterstützung | **Elementtool** > Registerkarte **"Barrierefreiheit"** > **Barrierefreiheitsstruktur** | [Überprüfen Sie die Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung,](test-accessibility-tree.md)und [testen Sie die Barrierefreiheit auf der Registerkarte "Barrierefreiheit".](accessibility-tab.md) |
| Stellen Sie sicher, dass die Webseite von Personen mit Farbenblindheit verwendet werden kann. | **Renderingtool** > Emulieren der Dropdownliste **"Sehschwächen"** | [Stellen Sie sicher, dass die Seite von Personen mit Farbblindheit verwendet werden kann](test-color-blindness.md) |
| Überprüfen, ob die Webseite mit verschwommener Sehkraft verwendet werden kann | **Renderingtool** > Emulieren der Dropdownliste **"Sehschwächen"** | [Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann](test-blurred-vision.md) |
| Stellen Sie sicher, dass die Webseite mit deaktivierter UI-Animation verwendet werden kann (reduzierte Bewegung) | **Renderingtool** > **Emulieren von CSS-Medienfeatures bevorzugt reduzierte Bewegung** | [Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann](test-reduced-ui-motion.md) |
| Stellen Sie sicher, dass das Webseitenlayout verwendet werden kann, wenn es schmal ist. | **Geräteemulationstool** | [Stellen Sie sicher, dass das Webseitenlayout verwendet werden kann, wenn es eingrenzt,](accessibility-testing-in-devtools.md#verify-that-the-webpage-layout-is-usable-when-narrow)und [emulieren Sie mobile Geräte in Microsoft Edge DevTools.](../device-mode/index.md) |


## <a name="see-also"></a>Weitere Informationen:

*   [Übersicht über Barrierefreiheitstests mit DevTools][DevtoolsAccessibilityAccessibilitytestingindevtools]
*   [Navigieren Microsoft Edge DevTools mit Hilfstechnologie][DevtoolsAccessibilityNavigation]
*   [Barrierefreiheitstests][DevtoolsAccessibilityTest]
*   [Barrierefreiheitsprinzipien und bewährte Methoden][MDNAccessibility]
*   [Sprachausgabe][MDNScreenReader]


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
[DevtoolsAccessibilityTest]: ../../accessibility/test.md "Barrierefreiheitstests | Microsoft-Dokumente"
[DevtoolsAccessibilityAccessibilitytestingindevtools]: accessibility-testing-in-devtools.md "Übersicht über Barrierefreiheitstests mit DevTools | Microsoft-Dokumente"
[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigieren Microsoft Edge DevTools mit hilfstechnologie | Microsoft-Dokumente"  
<!-- external -->
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | Mdn"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Sprachausgabe | Mdn"  
