---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Features
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, experiment
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: c76830cb8bbcc597aa026f58e1926cd2f9bc2d62
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439584"
---
# <a name="experimental-features"></a>Experimentelle Features  

Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.  

Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, können Sie die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal erhalten.  

## <a name="turn-on-experimental-features"></a>Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um \(oder off\) experimentelle Features in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie DevTools][DevtoolsOpenIndex].  
    *   Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  
1.  Öffnen Sie den [Bereich][DevToolsCustomizeIndexSettings] Einstellungen.  
    *   Wählen Sie `Shift` + `?` aus.  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  
1.  Klicken Sie auf der linken Seite des **Einstellungsbereichs** auf den Abschnitt **Experimente.**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Die Seite Experimente unter Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       Die **Seite Experimente** unter **Einstellungen**  
    :::image-end:::  
    
1.  Scrollen Sie **auf** der Seite Experimente durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.  
1.  Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.  
    
> [!NOTE]
> Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.  Um ein experimentelles Feature zu deaktivieren, öffnen Sie die Seite **Experimente,** und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.  

## <a name="highlighted-experimental-features"></a>Hervorgehobene experimentelle Features  

In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.  

| Experimentelles Feature | Microsoft Edge-Version |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | 85 oder höher |  
| [Enable Network Console](#enable-network-console) | 85 oder höher |  
| [Source Order Viewer](#source-order-viewer) | 86 oder höher |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | 87 oder höher |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | 89 oder höher |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | 89 oder höher |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | 89 oder höher |  
| [Enable Welcome tab](#enable-welcome-tab) | 89 oder höher |  

### Enable webhint  

[webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten liefert.  Die Art des Feedbacks, das [von webhint bereitgestellt wird.][WebhintMain]  

*   Bedienungshilfen  
*   Browserübergreifende Kompatibilität  
*   Sicherheit  
*   Leistung  
*   Progressive Web Apps (PWAs)  
*   Andere häufige Probleme bei der Webentwicklung  
    
Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im Bereich [Probleme][DevtoolsIssuesIndex] an.  Wählen Sie ein Problem zum Anzeigen der Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website aus.  Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich Netzwerk,** **Quellen**oder **Elemente** in DevTools zu öffnen.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhintfeedback im Problembereich" lightbox="../media/experiments-webhint.msft.png":::
   Webhintfeedback im **Problembereich**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments zum Erstellen synthetischer Netzwerkanforderungen über HTTP.  Sie können das **Netzwerkkonsolenexperiment** verwenden, um Web-API-Anforderungen zu senden.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um die **Netzwerkkonsole**zu verwenden.  

1.  Öffnen Sie den **Netzwerkbereich.**  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.  
1.  Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen **Sie Bearbeiten und Wiedergabe aus.**  
1.  Wenn die **Netzwerkkonsole geöffnet** wird, bearbeiten Sie die Netzwerkanforderungsinformationen.  
1.  Wählen Sie **Senden**aus.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschubschubschube" lightbox="../media/network-network-console.msft.png":::
   **Netzwerkkonsole** in der **Konsolenschubschubschube**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, wodurch Bildschirmlese- und Tastaturbenutzer verwechselt werden.  Verwenden Sie das Experiment, um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und **Source Order Viewer** der Reihenfolge der Quelle zu finden.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie **Source Order Viewer** zur Verwendung die folgenden Schritte aus.  

1.  Öffnen Sie das **Elementtool.**  
1.  Öffnen Sie **den Bereich** Barrierefreiheit im Bereich "Drawer\(bottom\)".  
1.  Aktivieren Sie **Source Order Viewer** im Abschnitt das Kontrollkästchen **Quellreihenfolge** anzeigen.  
1.  Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die die Reihenfolge in der Webseitenquelle enthält.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer im Bereich Barrierefreiheit" lightbox=".. /media/experiments-source-order-viewer.msft.png"::: im **Source Order Viewer** Bereich **Barrierefreiheit**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

Sie können layer jetzt zusammen mit z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.  Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.  Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.  Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.  Für ein umfassendes visuelles Debuggen werden nun 3D View die und zusammengesetzte Ebenen kombiniert.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden **Schritte aus,** um zusammengesetzte Layer zu verwenden.  

1.  Wählen Sie in der Schublade das **3D View** Tool aus.  
1.  Öffnen Sie den **Bereich Zusammengesetzte Ebenen.**  
1.  Alle dargestellten Ebenen der App werden angezeigt.  Testen Sie dieses Feature mit Ihren eigenen Web-Apps.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

Sie können nun den neuen visuellen [Schriftarten-Editor verwenden,][DevtoolsInspectStylesEditFonts] um Schriftarten zu bearbeiten.  Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.  Der visuelle **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.  

*   Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften  
*   Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften  
*   Einheiten konvertieren  
*   Generieren von genauem CSS-Code  
    
Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um den neuen **visuellen Schriftart-Editor**zu verwenden.  

1.  Öffnen Sie das **Elementtool.**  
1.  Öffnen Sie den **Bereich Formatvorlagen.**  
1.  Wählen Sie das **Symbol Schriftart-Editor** aus.  
    
Weitere Informationen zum neuen visuellen Schriftarten-Editor **finden**Sie unter Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich [Formatvorlagen in DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der visuelle Schriftarten-Editor-Bereich wird hervorgehoben" lightbox="../media/font-editor-open.msft.png":::
   Der visuelle **Schriftarten-Editor-Bereich** wird hervorgehoben  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

Dieses experimentelle Feature bietet viele neue Visualisierungen, mit deren Hilfe Sie CSS-Flexbox-Layouts debuggen können.  Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Anzeigen von beständigen Überlagerungen in Flexbox-Layouts mit dem Inspect-Tool  

Das **Inspect-Tool** bietet eine schnelle Möglichkeit, CSS-Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.  Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.  Zeigen Sie dann beim Debuggen der Website auf einen Flexcontainer, um Gliederungen um den flex-Container zu zeigen.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von Flexbox-Containern mit dem Inspect-Tool" lightbox="../media/flexbox-hover.msft.png":::
   Anzeigen von Flexbox-Containern mit dem **Inspect-Tool**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Anzeigen von beständigen Überlagerungen in Flexboxlayouts  

In Microsoft Edge, Version 89 oder höher, bietet das experimentelle FEATURE CSS Flexbox auch die Möglichkeit, dauerhafte Überlagerungen für Flexbox-Layouts zu aktivieren.  Dauerhafte Überlagerungen bieten die folgenden Vorteile.  

*   Dauerhafte Überlagerungen bleiben auf der Webseite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features der DevTools verwenden.
*   Mehrere dauerhafte Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexbox-Layouts gleichzeitig überprüfen können.  
*   Dauerhafte Überlagerungen bieten Farbkonfigurationsoptionen.  
    
Verwenden Sie eine der folgenden Aktionen, um dauerhafte Überlagerungen im Flexbox-Layout umschalten zu können.  

*   Wählen Sie **das Ovalsymbol Flexbox** neben einem beliebigen Flexbox-Container aus, der in der DOM-Struktur des **Elements-Tools angezeigt** wird.  
*   Öffnen Sie das **neue Layoutpanel** im **Elementtool,** und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flexsymbole und Layoutbereich in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Flexsymbole **und Layoutbereich** in DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Konfigurieren von beständigen Überlagerungen  

Verwenden Sie den **Layoutbereich,** um Optionen für dauerhafte Überlagerungen für CSS-Raster oder Flexbox-Layouts zu konfigurieren.  Der **Layoutbereich** befindet sich im **Elementtool** neben den **Formatvorlagen-** und **Berechneten** Fensterausschnitten.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutbereich" lightbox="../media/flexbox-layout.msft.png":::
   Layoutbereich  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

Sie können nun weitere Tools mit dem neuen **Symbol Weitere Tools** \( `+` \) öffnen.  Nachdem Sie das Experiment aktivieren und DevTools neu laden, wird rechts neben der Registerkartengruppe am oberen Rand der DevTools ein Pluszeichen **Enable + button tab menus to open more tools** \( `+` \) angezeigt.  Wenn Sie eine Liste anderer Tools anzeigen möchten, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol Weitere **Tools** \( `+` \) aus.  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Weitere Tools** im oberen Bereich
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

Dieses Experiment ersetzt das **Neue** Tool durch das neue **Willkommenstool.**  Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.  

*   Links zu Entwickler-Dokumenten  
*   die neuesten Features  
*   Versionshinweise  
*   Option zum Kontaktieren des Microsoft Edge DevTools-Teams  
    
Das **Willkommenstool** wird nach jedem Update auf Microsoft Edge automatisch geöffnet.  Um die Anzeige **** des Willkommenstools nach jedem Update zu verhindern, aktivieren Sie das Kontrollkästchen neben Registerkarte Öffnen nach jedem Update **unter** dem **Titel Willkommenstool.**  

Wenn Sie das ursprüngliche **Tool What's New** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente,** und entfernen Sie das Kontrollkästchen neben **Enable Welcome tab** .  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommenstool" lightbox="../media/experiments-welcome.msft.png":::
   **Willkommenstool**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Frühere experimentelle Features  

*   [3D View][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Turn on support to move tabs between panels][DevtoolsCustomizeIndex] ist jetzt in Microsoft Edge, Version 85 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] ist jetzt in Microsoft Edge, Version 86 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] ist jetzt in Microsoft Edge, Version 89 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Turn on new CSS grid debugging features][DevtoolsCssGrid] ist jetzt in Microsoft Edge, Version 89 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] ist jetzt in Microsoft Edge, Version 90 oder höher, verfügbar und standardmäßig aktiviert.  

## <a name="providing-feedback-on-experimental-features"></a>Bereitstellen von Feedback zu experimentellen Features  

So geben Sie Feedback zu Microsoft Edge DevTools-Experimenten oder zu anderen DevTools-Bezogenen.  

*   Senden Sie Ihr Feedback mit dem **Symbol** Feedback senden in den DevTools  
*   Tweet bei [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   Das Symbol **Feedback senden** in den Microsoft Edge-Entwicklungstools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Tastenkombinationen für alle Aktionen in devTools bearbeiten | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Tastenkombinationen in devTools mit Microsoft Visual Studio Code übereinstimmen | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen in DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
