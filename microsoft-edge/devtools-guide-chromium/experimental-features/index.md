---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, DevTools, Experimentieren
ms.openlocfilehash: 018364d4debc1791685a028c337f61f85865ef6b
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313055"
---
# Experimentelle Funktionen  

Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.  

Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal.  

## Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um experimentelle Features in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
    *   Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Weitere Informationen finden Sie unter ["Microsoft Edge DevTools"-Tastenkombinationen.][DevToolsShortcuts]  
1.  Öffnen Sie den [Bereich "Einstellungen".][DevToolsCustomizeIndexSettings]  
    *   Wählen Sie `Shift` + `?` .  Weitere Informationen finden Sie unter ["Microsoft Edge DevTools"-Tastenkombinationen.][DevToolsShortcuts]  
1.  Wählen Sie auf der linken Seite **des** Einstellungsbereichs den Abschnitt **"Experimente"** aus.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Seite "Experimente" in den Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       Seite **"Experimente"** in den **Einstellungen**  
    :::image-end:::  
    
1.  Scrollen Sie **auf** der Seite "Experimente" durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.  
1.  Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.  
    
> [!NOTE]
> Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.  Um ein experimentelles Feature **** zu deaktivieren, öffnen Sie die Seite "Experimente", und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.  

## Hervorgehobene experimentelle Features  

In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.  

| Experimentelles Feature | Microsoft Edge Version |  
|:--- |:--- |  
| [Aktivieren von Webhint](#enable-webhint) | 85 oder höher |  
| [Aktivieren der Netzwerkkonsole](#enable-network-console) | 85 oder höher |  
| [Quellauftragsanzeige](#source-order-viewer) | 86 oder höher |  
| [Aktivieren des Editors für Tastenkombinationen](#enable-keyboard-shortcut-editor) | 87 oder höher |  
| [Aktivieren zusammengesetzter Layer in der 3D-Ansicht](#enable-composited-layers-in-3d-view) | 87 oder höher |  
| [Aktivieren des neuen Schriftarten-Editor-Tools im Formatvorlagenbereich](#) | 89 oder höher |  
| [Aktivieren neuer CSS -Flexbox-Debugfeatures](#enable-new-css-flexbox-debugging-features) | 89 oder höher |  
| [Aktivieren + Schaltflächenmenüs zum Öffnen von weiteren Tools](#enable--button-tab-menus-to-open-more-tools) | 89 oder höher |  
| [Registerkarte "Willkommen" aktivieren](#enable-welcome-tool) | 89 oder höher |  

### Aktivieren neuer Features für das Debuggen von CSS-Rastern  

Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, die Sie beim Debuggen von CSS-Rasterlayouts unterstützen.  Aktivieren Sie dieses Experiment, und laden Sie DevTools neu, um eine Vorschau der neuesten [experimentellen](#turn-on-experimental-features) Features anzuzeigen.  Dieses Experiment ist in Microsoft Edge, Version 87 oder höher, standardmäßig aktiviert.  

#### Anzeigen von Rasterüberlagerungen beim Zeigen mit dem Tool "Inspect"  

Das **Tool "Inspect"** bietet eine schnelle Möglichkeit, CSS-Rasterlayouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.  Klicken Sie **in der** oberen linken Ecke von DevTools auf das Symbol Überprüfen\( Überprüfen ![ ](../media/inspect-icon.msft.png) \) .  Zeigen Sie dann auf der Website, die Sie debuggen, auf ein Grid-Element.  Um das Raster herum werden Gliederungen angezeigt, und die Schattierung gibt die Position von Rasterlücken an, falls vorhanden.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Anzeigen von Rastern mit dem Tool "Überprüfen"" lightbox="../media/grid-inspect.msft.png":::
   Anzeigen von Rastern mit dem **Tool "Überprüfen"**  
:::image-end:::  

#### Anzeigen persistenter Rasterüberlagerungen  

In Microsoft Edge, Version 86 oder höher, bietet das experimentelle Feature für das CSS-Raster auch die Option, dauerhafte Rasterüberlagerungen zu aktivieren.  Die persistenten Überlagerungen bieten mehrere Vorteile.  

*   Die persistenten Überlagerungen bleiben auf der Seite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features von DevTools verwenden.  
*   Mehrere persistente Überlagerungen können gleichzeitig aktiviert werden, sodass Sie mehrere Rasterlayouts gleichzeitig überprüfen können.  
*   Dauerhafte Überlagerungen bieten viele Konfigurationsoptionen, z. B. das Ausblenden oder Anzeigen von Namen im Rasterbereich, Rasterlücken, Nachverfolggrößen und so weiter.  
    
Die beiden Möglichkeiten zum Umschalten einer persistenten Rasterüberlagerung.  

*   Wählen Sie das **Symbol "Raster-Oval"** neben einem beliebigen Rasterelement aus, das in der STRUKTUR des Elements **angezeigt** wird.  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Symbol "Raster oval" im Tool "Elemente"" lightbox="../media/grid-adorner.msft.png":::
       Symbol "Raster oval" im **Tool "Elemente"**  
    :::image-end:::  
    
*   Öffnen Sie das neue **Layoutpanel** im Elementtool, und aktivieren Sie das Kontrollkästchen neben jedem Grid-Element, das Sie hervorheben möchten.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Layoutpanel in DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Layoutpanel** in DevTools  
    :::image-end:::  
    
#### Konfigurieren von beständigen Überlagerungen  

In Microsoft Edge, Version 86 oder höher, befindet sich das neue **Layoutpanel** im Tool **"Elemente"** neben den Registerkarten **"Formatvorlagen"** und **"Berechnet".**  Im **Layoutpanel** werden Konfigurationsoptionen für beständige Überlagerungen angezeigt.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Feature für das Debuggen von CSS-Rastern" lightbox="../media/experiments-grid.msft.png":::
   Feature für das Debuggen von CSS-Rastern  
:::image-end:::  

### Aktivieren der Unterstützung für das Verschieben von Registerkarten zwischen Panels  

Normalerweise können Tools wie **Elemente** und **Netzwerk** nur im Hauptbereich geöffnet werden, der sich oben in devTools befindet.  Tools wie **die 3D-Ansicht** und Probleme, die normalerweise nur im Bereich "Drawer" am unteren Rand der DevTools geöffnet werden. **** ****  Nachdem Sie das Experiment auswählen, können Sie Tools zwischen dem oberen und unteren Bereich verschieben.  Um ein Tool zu verschieben, zeigen Sie auf die Registerkarte, öffnen **** Sie das Kontextmenü \(rechtsklick\), und wählen Sie "Nach oben" oder **"Nach unten" aus.**   Mit diesem Experiment können Sie Ihr DevTools-Layout anpassen.  Wählen Sie zum Anzeigen oder Ausblenden **des Drawerpanels** die Option `Escape` aus.  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Verschieben von Registerkarten zwischen Panels" lightbox="../media/experiments-move-panels.msft.png":::
   Verschieben von Registerkarten zwischen Panels  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren von Webhint  

[Webhint][WebhintMain] ist ein Open-Source-Tool, das Echtzeitfeedback für Websites und lokale Webseiten liefert.  Die Art des Feedbacks, das von [Webhint bereitgestellt wird.][WebhintMain]  

*   Bedienungshilfen  
*   Browserübergreifende Kompatibilität  
*   Sicherheit  
*   Leistung  
*   Progressive Web Apps (PWAs)  
*   Andere häufige Probleme bei der Webentwicklung  
    
Das [Webhint-Experiment][WebhintMain] zeigt das Webhintfeedback im Bereich ["Probleme"][DevtoolsIssues] an.  Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzeigen zu können.  Wählen Sie einen Ressourcenlink aus, um den relevanten Bereich **"Netzwerk",** **"Quellen"** oder **"Elemente"** in DevTools zu öffnen.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   Webhint feedback in the **Issues** panel  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Netzwerkkonsole  

**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments zum Erstellen synthetischer Netzwerkanforderungen über HTTP.  Sie können das Experiment **"Netzwerkkonsole"** verwenden, um Web-API-Anforderungen zu senden.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden **Schritte aus, um**die Netzwerkkonsole zu verwenden.  

1.  Öffnen Sie den **Netzwerkbereich.**  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.  
1.  Öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **"Bearbeiten" und "Wiedergabe" aus.**  
1.  Bearbeiten Sie **beim Öffnen der** Netzwerkkonsole die Netzwerkanforderungsinformationen.  
1.  Wählen Sie **"Senden"** aus.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschubschubschubte" lightbox="../media/network-network-console.msft.png":::
   **Netzwerkkonsole** in der **Konsolenschubschubschubte**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Quellauftragsanzeige  

**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, was die Benutzer von Bildschirmleseprogramm und Tastatur verwechselt.  Verwenden Sie **das Experiment "Quellreihenfolgeanzeige",** um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die **folgenden Schritte aus,** um die Quellauftragsanzeige zu verwenden.  

1.  Öffnen Sie das **Elementtool.**  
1.  Öffnen Sie den **Barrierefreiheitsbereich** im Bereich "Drawer \(bottom\)".  
1.  Aktivieren Sie **im Abschnitt "Quellauftragsanzeige"** das Kontrollkästchen "Quellbestellung anzeigen". ****  
1.  Markieren Sie alle HTML-Elemente, um eine Überlagerung anzuzeigen, die in der Reihenfolge in der Webseitenquelle angezeigt wird.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Quellreihenfolgeanzeige im Bereich "Barrierefreiheit"" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Quellreihenfolgeanzeige** im Bereich **"Barrierefreiheit"**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Aktivieren des Editors für Tastenkombinationen

Wenn das **Experiment "Tastenkombination-Editor** aktivieren" aktiviert ist, können Sie Tastenkombinationen für jede Aktion in devTools anpassen.  Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
1.  Öffnen Sie [Einstellungen][DevToolsCustomizeIndexSettings].  
    *   Wählen Sie `Shift` + `?` .  
1.  Navigieren Sie zur **Verknüpfungsseite.**  
1.  Wählen Sie die Aktion aus, die Sie anpassen möchten.  
1.  Wählen Sie **das Symbol "Bearbeiten** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \)" aus.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Auswählen der anzupassenden Aktion auf der Seite "Verknüpfungen" in den Einstellungen" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Auswählen der anzupassenden Aktion auf der Seite **"Verknüpfungen"** in den [Einstellungen][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  Wählen Sie auf der Tastatur die Tasten aus, die an die Aktion gebunden werden soll.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Auswählen der Schlüssel, die der Aktion zugewiesen werden" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Auswählen der Schlüssel, die der Aktion zugewiesen werden  
    :::image-end:::  
    
1.  Um die neue Tastenkombination zu speichern, aktivieren Sie das Kontrollkästchen \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) symbol.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Klicken Sie auf das Häkchensymbol, um die neue Tastenkombination zu speichern." lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Klicken Sie auf das Häkchensymbol, um die neue Tastenkombination zu speichern.  
    :::image-end:::  
    
1.  Wählen Sie die neue Tastenkombination aus, um die Aktion in devTools auszulösen.  
    
Auf der **Seite Verknüpfungen ** zeigt das Symbol Benutzerdefinierte Tastenkombination\( **** ![ CustomKeyboardShortcut ](../media/custom-keyboard-shortcut-icon.msft.png) \) die von Ihnen angepassten Tastenkombinationen an.  Um alle Verknüpfungen zurückzusetzen, wählen Sie **"Standardverknüpfungen wiederherstellen" aus.**  

Wenn Sie Ihre Änderungen beim Bearbeiten der Tastenkombinationen für eine Aktion verwerfen möchten, wählen Sie das X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \)-Symbol aus.  Um Verknüpfungen für eine bestimmte Aktion zu entfernen, wählen Sie **das** Symbol "Verknüpfung löschen" ![ (DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \) aus.  Wenn Sie mehrere Verknüpfungen für eine Aktion hinzufügen möchten, wählen **Sie "Verknüpfung hinzufügen" aus.**  

> [!NOTE]
> Wenn derzeit eine Tastenkombination einer anderen Aktion zugewiesen ist, können Sie sie nicht für eine neue Aktion speichern.  Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Aktivieren zusammengesetzter Layer in der 3D-Ansicht  

Sie können layer nun zusammen mit Z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.  Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.  Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.  Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web App auswirkt.  Für ein umfassendes visuelles Debugging werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert.  

Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die **folgenden Schritte aus,** um zusammengesetzte Layer zu verwenden.  

1.  Wählen Sie in der Drawer das **3D-Ansichtstool** aus.  
1.  Öffnen Sie den **Bereich zusammengesetzte Layer.**  
1.  Alle dargestellten Ebenen der App werden angezeigt.  Testen Sie dieses Feature mit Ihren eigenen Web-Apps.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Aktivieren des neuen Schriftarten-Editor-Tools im Formatvorlagenbereich  

Sie können jetzt den neuen visuellen [Schriftarten-Editor zum][DevtoolsInspectStylesEditFonts] Bearbeiten von Schriftarten verwenden.  Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.  Der visuelle **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.  

*   Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften  
*   Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften  
*   Einheiten konvertieren  
*   Generieren von genauem CSS-Code  
    
Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um den neuen visuellen **Schriftarten-Editor**zu verwenden.  

1.  Öffnen Sie das **Elementtool.**  
1.  Öffnen Sie den **Formatvorlagenbereich.**  
1.  Wählen Sie das **Symbol "Schriftart-Editor"** aus.  
    
For more information about the new visual **Font Editor,** navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der visuelle Schriftarten-Editor-Bereich ist hervorgehoben." lightbox="../media/font-editor-open.msft.png":::
   Der visuelle **Schriftarten-Editor-Bereich** ist hervorgehoben.  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Aktivieren neuer CSS -Flexbox-Debugfeatures  

Dieses experimentelle Feature bietet viele neue Visualisierungen, mit deren Hilfe Sie CSS-Flexbox-Layouts debuggen können.  Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.  

#### Anzeigen beständiger Überlagerungen in Flexboxlayouts mit dem Tool "Inspect"  

Das **Tool "Inspect"** bietet eine schnelle Möglichkeit, CSS-Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.  Klicken Sie **in der** oberen linken Ecke von DevTools auf das Symbol Überprüfen\( Überprüfen ![ ](../media/inspect-icon.msft.png) \) .  Zeigen Sie dann beim Debuggen der Website auf einen Flexcontainer, um Gliederungen um den Flexcontainer zu zeigen.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von "Flexbox"-Containern mit dem Tool "Inspect"" lightbox="../media/flexbox-hover.msft.png":::
   Anzeigen von "Flexbox"-Containern mit dem **Tool "Inspect"**  
:::image-end:::  

#### Anzeigen beständiger Überlagerungen in Flexboxlayouts  

In Microsoft Edge, Version 89 oder höher, bietet das experimentelle CSS-Flexbox-Feature auch die Möglichkeit, dauerhafte Überlagerungen für Flexboxlayouts zu aktivieren.  Dauerhafte Überlagerungen bieten die folgenden Vorteile.  

*   Dauerhafte Überlagerungen bleiben auf der Webseite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features von DevTools verwenden.
*   Mehrere persistente Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexboxlayouts gleichzeitig überprüfen können.  
*   Dauerhafte Überlagerungen bieten Farbkonfigurationsoptionen.  
    
Verwenden Sie eine der folgenden Aktionen, um beständige Überlagerungen im Layout von Flexbox umschalten.  

*   Wählen Sie **das Ovalsymbol "Flexbox"** neben einem beliebigen Flexbox-Container aus, der in der STRUKTUR DES Elements **angezeigt** wird.  
*   Öffnen Sie das neue **** **Layoutpanel** im Elementtool, und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flexsymbole und Layoutpanel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Flexsymbole **und Layoutpanel** in DevTools  
:::image-end:::  

#### Konfigurieren beständiger Überlagerungen  

Verwenden Sie zum Konfigurieren von Optionen für beständige Überlagerungen für CSS-Raster oder Flexbox-Layouts den **Layoutbereich.**  Der **Layoutbereich** befindet sich im Tool **"Elemente"** neben den **Formatvorlagen-** und **berechneten** Fensterausschnitten.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutpanel" lightbox="../media/flexbox-layout.msft.png":::
   Layoutpanel  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Aktivieren + Schaltflächenmenüs zum Öffnen von weiteren Tools  

Sie können nun weitere Tools öffnen, indem Sie das neue Symbol "Weitere **Tools\(** `+` \) " verwenden.  Nachdem Sie die **** Registerkartenmenüs Aktivieren + aktiviert haben, um weitere Tools zu experimentieren und DevTools neu zu laden, wird rechts neben der Registerkartengruppe oben in DevTools ein Pluszeichen \( `+` \) angezeigt.  Wenn Sie eine Liste anderer Tools anzeigen möchten, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol "Weitere **Tools\** `+` (\)" aus.  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Weitere Tools** im oberen Bereich
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Willkommenstool aktivieren

Dieses Experiment ersetzt das Tool **"Neues"** durch das neue **Willkommenstool.**  Es wird ein aktualisiertes Design für die folgenden Inhalte angezeigt.  

*   Links zu Entwickler-Dokumenten  
*   Die neuesten Features  
*   Anmerkungen zur Version  
*   Option zum Kontaktieren des Microsoft Edge DevTools-Teams  
    
Das **Willkommenstool** wird nach jedem Update auf Microsoft Edge automatisch geöffnet.  Um zu verhindern, **** dass das Willkommenstool nach jeder **** Aktualisierung angezeigt wird, müssen Sie nach jeder Aktualisierung unter dem Titel des Willkommenstools das Kontrollkästchen neben der Registerkarte "Öffnen" **** aktivieren.  

Wenn Sie das ursprüngliche Tool **"Was ist neu"** bevorzugen, navigieren Sie zu Einstellungsexperimente, und entfernen Sie das Kontrollkästchen neben der Registerkarte [][DevtoolsCustomizeIndexSettings]  >  **** **"Willkommen aktivieren".**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommenstool" lightbox="../media/experiments-welcome.msft.png":::
   **Willkommenstool**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## Frühere experimentelle Features  

*   [Die 3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Die Unterstützung zum Verschieben von Registerkarten][DevtoolsMoveTabs] zwischen Panels ist jetzt verfügbar und in Microsoft Edge, Version 85 oder höher, standardmäßig aktiviert.  
*   [Tastenkombinationen anpassen ist][DevtoolsCustomKeyboardShortcuts] jetzt in Microsoft Edge, Version 86 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Emulation: Der Dualbildschirmmodus ist][DevtoolsDeviceModeDualScreenAndFoldables] jetzt verfügbar und in Microsoft Edge, Version 89 oder höher, standardmäßig aktiviert.  
*   In Microsoft [Edge,][DevtoolsCssGrid] Version 89 oder höher, sind neue Features zum Debuggen des CSS-Rasters jetzt verfügbar und standardmäßig aktiviert.  
    
## Bereitstellen von Feedback zu experimentellen Features  

Um Feedback zu Microsoft Edge -DevTools-Experimenten oder anderen im Zusammenhang mit DevTools zu geben.  

*   Senden Sie Ihr Feedback über das Symbol **"Feedback** senden" in den DevTools.  
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
[DevtoolsCssGrid]: ../css/grid.md "Überprüfen sie das CSS-Raster in Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von Css-Schriftartenformaten und -einstellungen im Formatvorlagenbereich in DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools – Tastenkombinationen | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Öffnen von Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Weberfahrungen auf zwei | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "So arbeiten Sie mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden der Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Feature für bildschirmübergreifende CSS-Medien für die Erkennung von | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dualbildschirmgeräte | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "1-1-| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
