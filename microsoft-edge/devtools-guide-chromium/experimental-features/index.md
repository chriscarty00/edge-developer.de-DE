---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, experiment
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398679"
---
# <a name="experimental-features"></a>Experimentelle Funktionen  

Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.  

Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, können Sie die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal erhalten.  

## <a name="turn-on-experimental-features"></a>Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um \(oder off\) experimentelle Features in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
    *   Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevToolsShortcuts]  
1.  Öffnen Sie den [Bereich][DevToolsCustomizeIndexSettings] Einstellungen.  
    *   Wählen Sie `Shift` + `?` aus.  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevToolsShortcuts]  
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
| [Aktivieren von Webhint](#enable-webhint) | 85 oder höher |  
| [Aktivieren der Netzwerkkonsole](#enable-network-console) | 85 oder höher |  
| [Source Order Viewer](#source-order-viewer) | 86 oder höher |  
| [Aktivieren des Tastenkombinationen-Editors](#enable-keyboard-shortcut-editor) | 87 oder höher |  
| [Aktivieren zusammengesetzter Layer in der 3D-Ansicht](#enable-composited-layers-in-3d-view) | 87 oder höher |  
| [Aktivieren des neuen Schriftart-Editor-Tools im Bereich Formatvorlagen](#enable-new-font-editor-tool-within-the-styles-pane) | 89 oder höher |  
| [Aktivieren neuer CSS Flexbox-Debuggingfeatures](#enable-new-css-flexbox-debugging-features) | 89 oder höher |  
| [Aktivieren und Aktivieren von Registerkartenmenüs für Schaltflächen zum Öffnen von weiteren Tools](#enable--button-tab-menus-to-open-more-tools) | 89 oder höher |  
| [Registerkarte Willkommen aktivieren](#enable-welcome-tool) | 89 oder höher |  

### <a name="enable-new-css-grid-debugging-features"></a>Aktivieren neuer FEATURES für das CSS-Rasterdebuding  

Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, mit deren Hilfe Sie CSS-Rasterlayouts debuggen können.  Aktivieren Sie dieses [Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu, um eine Vorschau der neuesten experimentellen Features anzuzeigen.  Dieses Experiment ist standardmäßig in Microsoft Edge, Version 87 oder höher, aktiviert.  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a>Anzeigen von On-Hover-Rasterüberlagerungen mit dem Inspect-Tool  

Das **Tool Inspect** bietet eine schnelle Möglichkeit, CSS Grid Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.  Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.  Zeigen Sie dann auf ein `Grid` Element auf der Webseite, die Sie debuggen.  Gliederungen werden um das Raster herum angezeigt, und die Schraffur gibt die Position von Gitterlücken an, falls vorhanden.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Anzeigen von Rastern mit dem Inspect-Tool" lightbox="../media/grid-inspect.msft.png":::
   Anzeigen von Rastern mit dem **Inspect-Tool**  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a>Anzeigen von beständigen Rasterüberlagerungen  

In Microsoft Edge, Version 86 oder höher, bietet das experimentelle CSS-Rasterfeature auch die Möglichkeit, dauerhafte Grid-Überlagerungen zu aktivieren.  Die beständigen Überlagerungen bieten verschiedene Vorteile.  

*   Die beständigen Überlagerungen bleiben auf der Seite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features der DevTools verwenden.  
*   Mehrere dauerhafte Überlagerungen können gleichzeitig aktiviert werden, sodass Sie mehrere Rasterlayouts gleichzeitig überprüfen können.  
*   Dauerhafte Überlagerungen bieten viele Konfigurationsoptionen, z. B. Ausblenden oder Anzeigen von Namen im Rasterbereich, Rasterlücken, Titelgrößen und so weiter.  
    
Die beiden Möglichkeiten zum Umschalten einer beständigen Rasterüberlagerung.  

*   Wählen Sie **das Ovalsymbol Raster** neben einem Grid-Element aus, das in der DOM-Struktur des **Elements-Tools angezeigt** wird.  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Gitternetz-Ovalsymbol im Elementtool" lightbox="../media/grid-adorner.msft.png":::
       Gitternetz-Ovalsymbol im **Elementtool**  
    :::image-end:::  
    
*   Öffnen Sie das **neue Layoutpanel** im Elementtool, und aktivieren Sie das Kontrollkästchen neben jedem Grid-Element, das Hervorgehoben werden soll.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Layoutbereich in DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Layoutbereich** in DevTools  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a>Konfigurieren von beständigen Überlagerungen  

In Microsoft Edge, Version 86 oder höher, befindet sich das neue **Layoutpanel** im **Elementtool** neben den **Formatvorlagen** und **berechneten** Panels.  Im **Layoutbereich** werden Konfigurationsoptionen für dauerhafte Überlagerungen angezeigt.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Feature zum Debuggen von CSS-Rastern" lightbox="../media/experiments-grid.msft.png":::
   Feature zum Debuggen von CSS-Rastern  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a>Aktivieren der Unterstützung zum Verschieben von Registerkarten zwischen Panels  

Normalerweise können Tools wie **Elemente** und **Netzwerk** nur im Hauptbereich geöffnet werden, der sich am oberen Rand der DevTools befindet.  Tools wie **3D-Ansicht** und **Probleme,** die normalerweise nur im **Drawer-Bereich** geöffnet werden, der sich am unteren Rand der DevTools befindet.  Nachdem Sie das Experiment auswählen, können Sie Tools zwischen dem oberen und unteren Bereich verschieben.  Um ein Tool zu verschieben, zeigen Sie auf die Registerkarte, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Nach** oben oder **Nach unten verschieben aus.**   Mit diesem Experiment können Sie Ihr DevTools-Layout anpassen.  Wählen Sie aus, um den **Bereich "Drawer" ein- oder** auszublenden. `Escape`  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Verschieben von Tools zwischen Panels" lightbox="../media/experiments-move-panels.msft.png":::
   Verschieben von Tools zwischen Panels  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a>Aktivieren von Webhint  

[webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten liefert.  Die Art des Feedbacks, das [von webhint bereitgestellt wird.][WebhintMain]  

*   Bedienungshilfen  
*   Browserübergreifende Kompatibilität  
*   Sicherheit  
*   Leistung  
*   Progressive Web Apps (PWAs)  
*   Andere häufige Probleme bei der Webentwicklung  
    
Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im Bereich [Probleme][DevtoolsIssues] an.  Wählen Sie ein Problem zum Anzeigen der Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website aus.  Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich Netzwerk,** **Quellen**oder **Elemente** in DevTools zu öffnen.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhintfeedback im Problembereich" lightbox="../media/experiments-webhint.msft.png":::
   Webhintfeedback im **Problembereich**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a>Aktivieren der Netzwerkkonsole  

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

### <a name="source-order-viewer"></a>Source Order Viewer  

**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, wodurch Bildschirmlese- und Tastaturbenutzer verwechselt werden.  Verwenden Sie **das Experiment Source Order Viewer,** um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um die **Quellauftragsanzeige**zu verwenden.  

1.  Öffnen Sie das **Elementtool.**  
1.  Öffnen Sie **den Bereich** Barrierefreiheit im Bereich "Drawer\(bottom\)".  
1.  Aktivieren Sie **im Abschnitt Quellauftragsanzeige** das Kontrollkästchen **Quellreihenfolge** anzeigen.  
1.  Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die die Reihenfolge in der Webseitenquelle enthält.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Quellauftragsanzeige im Bereich Barrierefreiheit" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Quellauftragsanzeige** im Bereich **Barrierefreiheit**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a>Aktivieren des Tastenkombinationen-Editors

Wenn das **Experiment Tastenkombinationen-Editor** aktivieren aktiviert ist, können Sie Tastenkombinationen für alle Aktionen in devTools anpassen.  Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
1.  Öffnen [Sie Einstellungen][DevToolsCustomizeIndexSettings].  
    *   Wählen Sie `Shift` + `?` aus.  
1.  Navigieren Sie zur **Seite Verknüpfungen.**  
1.  Wählen Sie die Aktion aus, die Sie anpassen möchten.  
1.  Wählen Sie **das Symbol** Bearbeiten \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \) aus.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Wählen Sie auf der Seite Verknüpfungen unter Einstellungen die anzupassende Aktion aus." lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Wählen Sie auf der Seite Verknüpfungen unter Einstellungen die anzupassende **Aktion** [aus.][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  Wählen Sie auf der Tastatur die Tasten aus, die an die Aktion gebunden werden soll.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Auswählen der Schlüssel, die Sie der Aktion zuweisen möchten" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Auswählen der Schlüssel, die Sie der Aktion zuweisen möchten  
    :::image-end:::  
    
1.  Zum Speichern der neuen Tastenkombination wählen Sie das Häkchen \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) symbol.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Wählen Sie das Häkchensymbol aus, um die neue Tastenkombination zu speichern." lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Wählen Sie das Häkchensymbol aus, um die neue Tastenkombination zu speichern.  
    :::image-end:::  
    
1.  Wählen Sie die neue Tastenkombination aus, um die Aktion in den DevTools auszulösen.  
    
Auf der **Seite Verknüpfungen** zeigt **das** Symbol Benutzerdefinierte Tastenkombination \( ![ CustomKeyboardShortcut \) die von Ihnen ](../media/custom-keyboard-shortcut-icon.msft.png) angepassten Tastenkombinationen an.  Um alle Verknüpfungen zurückzusetzen, wählen Sie **Standardverknüpfungen wiederherstellen aus.**  

Wenn Sie Ihre Änderungen beim Bearbeiten der Tastenkombinationen für eine Aktion verwerfen möchten, wählen Sie das Symbol X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \) aus.  Zum Entfernen von Verknüpfungen für eine bestimmte Aktion wählen Sie **das** Symbol Verknüpfung löschen \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \) aus.  Wenn Sie mehrere Verknüpfungen für eine Aktion hinzufügen möchten, wählen **Sie Verknüpfung hinzufügen aus.**  

> [!NOTE]
> Wenn eine Tastenkombination derzeit einer anderen Aktion zugewiesen ist, können Sie sie nicht für eine neue Aktion speichern.  Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a>Aktivieren zusammengesetzter Layer in der 3D-Ansicht  

Sie können layer jetzt zusammen mit z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.  Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.  Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.  Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.  Für ein umfassendes visuelles Debugging werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden **Schritte aus,** um zusammengesetzte Layer zu verwenden.  

1.  Wählen Sie in der Schublade das **3D-Ansichtstool** aus.  
1.  Öffnen Sie den **Bereich Zusammengesetzte Ebenen.**  
1.  Alle dargestellten Ebenen der App werden angezeigt.  Testen Sie dieses Feature mit Ihren eigenen Web-Apps.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a>Aktivieren des neuen Schriftart-Editor-Tools im Bereich Formatvorlagen  

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

### <a name="enable-new-css-flexbox-debugging-features"></a>Aktivieren neuer CSS Flexbox-Debuggingfeatures  

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

### <a name="enable--button-tab-menus-to-open-more-tools"></a>Aktivieren und Aktivieren von Registerkartenmenüs für Schaltflächen zum Öffnen von weiteren Tools  

Sie können nun weitere Tools mit dem neuen **Symbol Weitere Tools** \( `+` \) öffnen.  Nachdem Sie die **** Registerkartenmenüs +aktivieren aktiviert haben, um weitere Tools zu öffnen und DevTools neu zu laden, wird rechts neben der Registerkartengruppe am oberen Rand der DevTools ein Pluszeichen \( `+` \) angezeigt.  Wenn Sie eine Liste anderer Tools anzeigen möchten, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol Weitere **Tools** \( `+` \) aus.  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Weitere Tools** im oberen Bereich
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a>Aktivieren des Willkommenstools

Dieses Experiment ersetzt das **Neue** Tool durch das neue **Willkommenstool.**  Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.  

*   Links zu Entwickler-Dokumenten  
*   die neuesten Features  
*   Versionshinweise  
*   Option zum Kontaktieren des Microsoft Edge DevTools-Teams  
    
Das **Willkommenstool** wird nach jedem Update auf Microsoft Edge automatisch geöffnet.  Um die Anzeige **** des Willkommenstools nach jedem Update zu verhindern, aktivieren Sie das Kontrollkästchen neben Registerkarte Öffnen nach jedem Update **unter** dem **Titel Willkommenstool.**  

Wenn Sie das ursprüngliche **Tool What's New** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente,** und entfernen Sie das Kontrollkästchen neben **Registerkarte Willkommen aktivieren**.  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommenstool" lightbox="../media/experiments-welcome.msft.png":::
   **Willkommenstool**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Frühere experimentelle Features  

*   [Die 3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.  
*   [Aktivieren Der Support zum Verschieben von Registerkarten][DevtoolsMoveTabs] zwischen Panels ist jetzt verfügbar und in Microsoft Edge, Version 85 oder höher, standardmäßig aktiviert.  
*   [Tastenkombinationen anpassen ist][DevtoolsCustomKeyboardShortcuts] jetzt verfügbar und in Microsoft Edge, Version 86 oder höher, standardmäßig aktiviert.  
*   [Emulation: Der duale][DevtoolsDeviceModeDualScreenAndFoldables] Bildschirmmodus ist jetzt verfügbar und in Microsoft Edge, Version 89 oder höher, standardmäßig aktiviert.  
*   [In Microsoft Edge,][DevtoolsCssGrid] Version 89 oder höher, sind neue FEATURES für das CSS-Rasterdebuding jetzt verfügbar und standardmäßig aktiviert.  
    
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
[DevtoolsMoveTabs]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen in DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Dualscreen-Weberfahrungen | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Laden Sie den Surface Duo-Emulator | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Css-Medienbildschirm-Spannfunktion für die Erkennung von | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-| Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxis fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
