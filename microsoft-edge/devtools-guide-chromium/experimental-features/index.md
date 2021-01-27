---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, DevTools, Experimentieren
ms.openlocfilehash: fbdeeb08599285a9cfa6edd467282cfbabbadd74
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233929"
---
# Experimentelle Funktionen  

Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.  

Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal.  

## Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um experimentelle Features in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
    *   Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Weitere Informationen finden Sie unter ["Microsoft Edge DevTools"-Tastenkombinationen.][DevToolsShortcuts]  
1.  Öffnen Sie den [Bereich "Einstellungen".][DevToolsCustomizeSettings]  
    *   Wählen Sie `Shift` + `?` .  Weitere Informationen finden Sie unter ["Microsoft Edge DevTools"-Tastenkombinationen.][DevToolsShortcuts]  
1.  Wählen Sie auf der linken Seite **des** Einstellungsbereichs den Abschnitt **"Experimente"** aus.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Liste der Experimente in den DevTools-Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       Liste der Experimente **** in den DevTools-Einstellungen  
    :::image-end:::  
    
1.  Scrollen Sie **auf** der Seite "Experimente" durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.  
1.  Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.  
    
> [!NOTE]
> Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.  Um ein experimentelles Feature **** zu deaktivieren, öffnen Sie die Seite "Experimente", und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.  

## Hervorgehobene experimentelle Features  

In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.  

| Experimentelles Feature | Microsoft Edge Version |  
|:--- |:--- |  
| [Emulation: Unterstützung des Dualbildschirmmodus](#emulation-support-dual-screen-mode) | 84 oder höher |  
| [Aktivieren neuer Features für das Debuggen von CSS-Rastern](#enable-new-css-grid-debugging-features) | 85 oder höher |  
| [Aktivieren der Unterstützung für das Verschieben von Registerkarten zwischen Panels](#enable-support-to-move-tabs-between-panels) | 85 oder höher |  
| [Aktivieren von Webhint](#enable-webhint) | 85 oder höher |  
| [Aktivieren der Netzwerkkonsole](#enable-network-console) | 85 oder höher |  
| [Quellauftragsanzeige](#source-order-viewer) | 86 oder höher |  
| [Aktivieren des Editors für Tastenkombinationen](#enable-keyboard-shortcut-editor) | 87 oder höher |  
| [Aktivieren zusammengesetzter Layer in der 3D-Ansicht](#turn-on-composited-layers-in-3d-view) | 87 oder höher |  

### Emulation: Unterstützung des Dualbildschirmmodus  

Bietet zusätzliche Features zum Emulieren von zwei neuen Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Verknappung][SamsungMobileGalaxyFold]  
    
Emulieren Sie die Geräte, und schalten Sie zwischen den folgenden Haltungen um.  

*   Einzelbildschirm oder geklappte Haltung  
*   Dualbildschirm oder aufgefunktioniertes Bild  
    
Aktivieren Sie [experimentelle Webplattform-APIs,](#enable-experimental-apis) und verwenden Sie die [CSS-Medienbildschirm-übergreifende][DualScreenDocsCssMedia] Funktion und [javaScript getWindowSegments-API,][DualScreenDocsJSAPI] um Ihre Website \(oder App\) für Dualbildschirme und ausklappbare Geräte zu verbessern.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emulieren von Surface Duo in Microsoft Edge  
:::image-end:::  

#### Aktivieren experimenteller APIs  

Aktivieren Sie das Flag in Microsoft Edge, um das Feature für den Bildschirmbereich von [CSS-Medien][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] `Experimental Web Platform features` zu verwenden.  Führen Sie die folgenden Schritte aus.  

1.  Navigieren Sie zu `edge://flags` .  
1.  Geben Sie **im Textfeld "Suchkennzeichen"** die Option `Experimental Web Platform features` **"Experimentelle Webplattform-Features"** ein, und ändern Sie **"Deaktiviert"** in **"Aktiviert".**  
1.  Starten Sie Microsoft Edge neu.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren der Kennzeichnung für experimentelle Webplattformfeatures" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Aktivieren der Kennzeichnung für experimentelle Webplattformfeatures  
:::image-end:::  

> [!NOTE]
> Wenn Sie CSS-Medienabfragen oder die [JavaScript-Windows-Segment-Enumerations-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Flag **"Experimentelle WebPlattform-Features"** in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo-Gerät][SurfaceDevicesDuo] aktivieren. [][DualScreenDocsCssMedia]  
> 
> Wenn das Flag für experimentelle Webplattformfeatures im Microsoft [Edge][MicrosoftEdge] Desktop aktiviert und in der [Android Microsoft][GooglePlayMicrosoftEdge]Edge-App deaktiviert ist, ist das Verhalten Ihrer Website oder App im Surface Duo-Emulator im Desktop von Microsoft Edge nicht mit der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf [Surface Duo kompatibel.][SurfaceDevicesDuo] ****  Stellen Sie sicher, dass die Flags in Android- und Desktop-Microsoft Edge übereinstimmen, um den Surface Duo-Emulator im Microsoft Edge [Desktop erfolgreich zu verwenden.][MicrosoftEdge]  

#### Testen auf ausklappbaren und Dualbildschirmgeräten  

Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einem dualen Bildschirm in Microsoft Edge emulieren, wird die Naht \(der Abstand zwischen den beiden Bildschirmen\) über Ihrer Website oder App gezeichnet.  

Die emulierte Anzeige entspricht der Darstellung Ihrer Website \(oder App\) in der [Microsoft Edge Android-App,][GooglePlayMicrosoftEdge] die auf [Surface Duo ausgeführt wird.][SurfaceDevicesDuo]  Möglicherweise müssen Sie Ihre Website \(oder App\) aktualisieren, damit sie am Nahtstrich besser angezeigt wird.  Weitere Informationen zum Anpassen Ihrer Website \(oder app\) an die Naht finden Sie unter "Arbeiten mit [der Naht".][DualScreenIntroductionHowWorkSeam]  

Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] bietet zusätzliche Features, mit deren Hilfe Sie Ihre Website oder App in mehreren Haltungen und Ausrichtungen testen können.  Choose **Rotate** \( ![ Rotate ][ImageRotateIcon] \) to rotate the viewport to landscape orientation. Kombinieren Sie das Feature mit **Span** \( Span \), um zwischen einem einzelnen Bildschirm oder gefalteten und dualen Bildschirmen oder aufgeklappten ![ ][ImageSpanIcon] Postures umschalten zu können.  Zusammen ermöglichen die Features das Testen Ihrer Website oder App in allen vier möglichen Stellen und Ausrichtungen.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte  
:::image-end:::  

Das **Symbol für experimentelle Webplattformfeatures** \( ExperimentalApis \) zeigt den Status des Features der ![ ][ImageExperimentalApisIcon] **experimentellen Webplattform** an.  Wenn das Flag aktiviert ist, wird das Symbol hervorgehoben.  Wenn das Flag deaktiviert ist, wird das Symbol nicht hervorgehoben.  Um das Flag zu aktivieren (oder zu deaktivieren), navigieren Sie zu dem Flag, und schalten `edge://flags` Sie es um.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Hier finden Sie weitere Ressourcen, die Sie bei der Verbesserung Ihrer Website \(oder App\) für Dual-Screen-Geräte unterstützen können.  

*   Weitere Informationen zur Webentwicklung auf Dual-Screen-Geräten finden Sie unter ["Dual-screen web experiences".][DualScreenWebIndex]  
*   Installieren Sie den [Surface Duo-Emulator.][DualScreenAndroidUseEmulator]  Sie unterscheiden sich vom Emulator in Microsoft Edge, emulieren das Surface Duo unter Android und werden in [Android Studio integriert.][AndroidDeveloperStudio]  Weitere Informationen finden Sie unter ["Surface Duo SDK erhalten".][DualScreenAndroidGetDuoSdk]  
    
> [!NOTE]
> Im Folgenden finden Sie eine Liste der aktuellen bekannten Probleme.  
> 
> *   Wenn Sie einen [Microsoft Remote Desktop Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das Surface [Duo][SurfaceDevicesDuo] oder Samsung [Während Fold][SamsungMobileGalaxyFold]zu emulieren, kann der Zeiger wackeln oder zittern.  Wenn das Problem vor sich geht, senden [Sie Feedback.](#providing-feedback-on-experimental-features)  

### Aktivieren neuer Features für das Debuggen von CSS-Rastern  

Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, die Sie beim Debuggen von CSS-Rasterlayouts unterstützen.  Aktivieren Sie dieses Experiment, und laden Sie DevTools neu, um eine Vorschau der neuesten [experimentellen](#turn-on-experimental-features) Features anzuzeigen.  Dieses Experiment ist in Microsoft Edge, Version 87 oder höher, standardmäßig aktiviert.  

#### Anzeigen von Rasterüberlagerungen beim Zeigen mit dem Tool "Inspect"  

Das **Tool "Inspect"** bietet eine schnelle Möglichkeit, CSS-Rasterlayouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.  Klicken Sie **in der** oberen linken Ecke von DevTools auf das Symbol Überprüfen\( Überprüfen ![ ][ImageInspectIcon] \) .  Zeigen Sie dann auf der Website, die Sie debuggen, auf ein Grid-Element.  Um das Raster herum werden Gliederungen angezeigt, und die Schattierung gibt die Position von Rasterlücken an, falls vorhanden.  

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

Normalerweise können Tools wie **Elemente** und **Netzwerk** nur im Hauptbereich geöffnet werden, der sich oben in devTools befindet.  Tools wie **die 3D-Ansicht** und Probleme, die normalerweise nur im Bereich "Drawer" am unteren Rand der DevTools geöffnet werden. **** ****  Nachdem Sie das Experiment auswählen, können Sie Tools zwischen dem oberen und unteren Bereich verschieben.  Um ein Tool zu verschieben, zeigen Sie auf die Registerkarte, öffnen **** Sie das Kontextmenü \(rechtsklick\), und wählen Sie "Nach oben" oder **"Nach unten" aus.**   Mit diesem Experiment können Sie Ihr DevTools-Layout anpassen.  Wählen Sie zum Ein- oder Ausblenden **des Drawerpanels** die Option `Escape` aus.  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Verschieben von Registerkarten zwischen Panels" lightbox="../media/experiments-move-panels.msft.png":::
   Verschieben von Registerkarten zwischen Panels  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren von Webhint  

[Webhint][WebhintMain] ist ein Open Source-Tool, das Echtzeitfeedback für Websites und lokale Webseiten bietet.  Die Art des Feedbacks, das von [Webhint bereitgestellt wird.][WebhintMain]  

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

Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden **Schritte aus, um**die Netzwerkkonsole zu verwenden.  

1.  Öffnen Sie den **Netzwerkbereich.**  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.  
1.  Öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **"Bearbeiten" und "Wiedergabe" aus.**  
1.  Bearbeiten Sie **beim Öffnen der** Netzwerkkonsole die Netzwerkanforderungsinformationen.  
1.  Wählen Sie **"Senden"** aus.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschubte" lightbox="../media/network-network-console.msft.png":::
   **Netzwerkkonsole** in der **Konsolenschubte**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Quellauftragsanzeige  

**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Seitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, was die Benutzer von Bildschirmleseprogramm und Tastatur verwechselt.  Verwenden Sie **das Experiment "Quellreihenfolgeanzeige",** um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.  

Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die **folgenden Schritte aus,** um die Quellauftragsanzeige zu verwenden.  

1.  Öffnen Sie den **Bereich "Elemente".**  
1.  Öffnen Sie den **Barrierefreiheitsbereich** im Bereich "Drawer \(bottom\)".  
1.  Aktivieren Sie **im Abschnitt "Quellauftragsanzeige"** das Kontrollkästchen "Quellbestellung anzeigen". ****  
1.  Markieren Sie alle HTML-Elemente, um eine Überlagerung in der Reihenfolge in der Seitenquelle anzeigen.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Quellreihenfolgeanzeige im Bereich "Barrierefreiheit"" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Quellreihenfolgeanzeige** im Bereich **"Barrierefreiheit"**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Aktivieren des Editors für Tastenkombinationen

Wenn das **Experiment "Tastenkombination-Editor** aktivieren" aktiviert ist, können Sie nun Tastenkombinationen für jede Aktion in devTools anpassen.  Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.  

1.  [Öffnen Sie DevTools][DevtoolsOpenMain].  
1.  Öffnen Sie [Einstellungen][DevToolsCustomizeSettings].
    *   Wählen Sie `Shift` + `?` .  
1.  Navigieren Sie zur **Verknüpfungsseite.**  
1.  Wählen Sie die Aktion aus, die Sie anpassen möchten.  
1.  Wählen Sie **das Symbol "Bearbeiten** \( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \)" aus.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Auswählen der anzupassenden Aktion auf der Seite "Verknüpfungen" in den Einstellungen" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Auswählen der anzupassenden Aktion auf der Seite **"Verknüpfungen"** in den [Einstellungen][DevToolsCustomizeSettings]
    :::image-end:::  
    
1.  Wählen Sie auf der Tastatur die Tasten aus, die Sie an die Aktion binden möchten.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Wählen Sie die Schlüssel aus, die Sie der Aktion zuweisen möchten." lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Wählen Sie die Schlüssel aus, die Sie der Aktion zuweisen möchten.
    :::image-end:::  
    
1.  Um die neue Tastenkombination zu speichern, aktivieren Sie das Kontrollkästchen \(![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]\) symbol.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Klicken Sie auf das Häkchensymbol, um die neue Tastenkombination zu speichern." lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Klicken Sie auf das Häkchensymbol, um die neue Tastenkombination zu speichern.
    :::image-end:::  
    
1.  Wählen Sie die neue Tastenkombination aus, um die Aktion in devTools auszulösen.  
    
Auf der **Seite Verknüpfungen ** zeigt das Symbol Benutzerdefinierte Tastenkombination\( **** ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \) die von Ihnen angepassten Tastenkombinationen an.  Um alle Verknüpfungen zurückzusetzen, wählen Sie **"Standardverknüpfungen wiederherstellen" aus.**  

Wenn Sie die Tastenkombinationen für eine Aktion bearbeiten, wählen Sie zum Verwerfen der Änderungen das X \( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \)-Symbol aus.  Um Verknüpfungen für eine bestimmte Aktion zu entfernen, wählen Sie **das** Symbol "Verknüpfung löschen" ![ (DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \) aus.  Wenn Sie mehrere Verknüpfungen für eine Aktion hinzufügen möchten, wählen **Sie "Verknüpfung hinzufügen" aus.**

> [!NOTE]
> Wenn derzeit eine Tastenkombination einer anderen Aktion zugewiesen ist, können Sie sie nicht für eine neue Aktion speichern.  Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.  

<!--Available in Microsoft Edge version 87 and later.  -->

### Aktivieren zusammengesetzter Layer in der 3D-Ansicht

Sie können layer nun zusammen mit Z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.  Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.  Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.  Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web App auswirkt.  Für ein umfassendes visuelles Debugging werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert.  Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie die DevTools neu starten.  Führen Sie die **folgenden Schritte aus,** um zusammengesetzte Layer zu verwenden.  

1.  Wählen Sie in der Drawer das **3D-Ansichtstool** aus.  
1.  Öffnen Sie den **Bereich zusammengesetzte Layer.**  
1.  Alle dargestellten Ebenen der App werden angezeigt.  Testen Sie dieses Feature mit Ihren eigenen Web-Apps.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## Frühere experimentelle Features  

*   [Die 3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, verfügbar und standardmäßig aktiviert.  
*   [Tastenkombinationen anpassen ist][DevtoolsCustomKeyboardShortcuts] jetzt in Microsoft Edge, Version 86 oder höher, verfügbar und standardmäßig aktiviert.  

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

<!-- image links -->  

[ImageCheckmarkKeyboardShortcutIcon]: ../media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ../media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ../media/delete-keyboard-shortcut-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ../media/edit-keyboard-shortcut-icon.msft.png  
[ImageExperimentalApisIcon]: ../media/experimental-apis-dark-icon.msft.png  
[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ../media/span-dark-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ../media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevToolsCustomizeSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
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

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
