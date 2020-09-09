---
description: Passen Sie Tastenkombinationen mit Visual Studio-Code an, emulieren Sie Surface Duo und Samsung Galaxy Fold, Verbesserungen der CSS-Raster Überlagerung und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 943eca7e73385513b264feb74ec37c450d5c5a2f
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004164"
---
# Neuerungen in devtools (Microsoft Edge 86)  

## Ankündigungen des Microsoft Edge devtools-Teams  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### Zuordnen von Tastenkombinationen in devtools zu Visual Studio-Code  

In Microsoft Edge 86 können Sie die Tastenkombinationen im devtools mit ihren Tastenkombinationen in [Visual Studio-Code][VisualStudioCode]vergleichen. 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code  
:::image-end:::  

Um dieses Feature zu aktivieren, navigieren Sie zum [Anpassen von Tastenkombinationen im Microsoft Edge-devtools][DevtoolsCustomizeShortcuts].  

Die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in [Visual Studio-Code][VisualStudioCodeShortcutsKeyboardWindows] lautet beispielsweise `F5` .  Mit der **devtools (Standardeinstellung)** ist dieselbe Verknüpfung in der devtools `F8` , aber wenn Sie die **Visual Studio-Code** Vorgabe auswählen, ist diese Verknüpfung nun auch `F5` .  

Chrom Problem [#174309][CR174309]  

### Emulieren von Surface Duo und Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   Experimentelle Funktion  
:::image-end:::  

Sie können jetzt das Aussehen und Verhalten Ihrer Website oder App auf zwei neuen Geräten testen:  [Surface Duo][MicrosoftSurfaceDevicesDuo] und [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.  

Verwenden Sie beim [emulieren des Geräts][DevtoolsDeviceModeIndex]die folgenden Features, um Ihre Website oder App für Dual-Screen-und faltbare Geräte zu verbessern.  

*   Über [greifend][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], das heißt, wenn auf beiden Bildschirmen die Website \ (oder App \) angezeigt wird.
*   [Rendern der Naht][DualScreenIntroductionHowWorkSeam], also des Leerraums zwischen den beiden Bildschirmen
*   [Aktivieren von experimentellen Web-Platform-APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] für den Zugriff auf das neue [CSS mediascreen-Feature][DualScreenWebCssMediaSpanning] und die [JavaScript-getWindowSegments-API][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Geräteemulation für Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Geräteemulation für Surface Duo  
:::image-end:::  

Um dieses experimentelle Feature zu aktivieren, navigieren Sie zu [experimentelle Features aktivieren][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , und aktivieren Sie das Kontrollkästchen neben **Emulation: Dual-Screen-Modus unterstützen**.  

Wenn Sie weitere Informationen zu diesem Experiment erhalten möchten, navigieren Sie zu [Emulation: Unterstützung des dualen Bildschirms][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].  

Chromium-Problem: [#1054281][CR1054281]  

### Verbesserungen der CSS-Raster Überlagerung und neue experimentelle Raster Features  

Vielen Dank für ihr positives Feedback zu den verbesserten CSS-Raster Überlagerungen.  Die CSS-Raster Überlagerungen sind nun standardmäßig aktiviert, und es ist nicht erforderlich, dass Sie ein Experiment aktivieren.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="CSS-Raster Überlagerung für Artikel Element" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   CSS-Raster Überlagerung für `article` Element  
:::image-end:::  

> [!NOTE]
> Weitere Informationen zu Raster Überlagerungen finden Sie unter [Debuggen von CSS-Raster Features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

Das Microsoft Edge devtools-Team und das Chrome devtools-Team arbeiten an zusätzlichen Features zusammen.  Zu den neuen Features gehören mehrere Overlays, die in einem neuen **Layoutbereich** im Bereich **Elemente** persistent und konfigurierbar sind.  

Um dieses experimentelle Feature zu aktivieren, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **neue CSS-Raster Debuggen Features aktivieren (Konfigurationsoptionen, die im Bereich "Layout-Seitenleiste" in Elementen nach dem Neustart verfügbar sind)**.  

Weitere Informationen zu diesem Experiment finden Sie unter [Aktivieren neuer Features für das Debuggen von CSS-Rastern][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].  

Chromium-Problem: [#1047356][CR1047356]  

### Von der Konsole kopierte Tabelle erhält die Formatierung  

In Microsoft Edge 85 oder früher ging die Formatierung einer Kopie `console.table` verloren.  Wenn Sie die Ausgabe aus der [Tabellen][DevtoolsConsoleApiTable] Konsolen-API kopiert und eingefügt haben, wurde nur der Text der Tabelle beibehalten.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Ausgabe der Tabellen Konsolen-API in Microsoft Edge 85 oder früher" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Ausgabe der Konsolen-API in Microsoft Edge 85 oder früher  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Tabellen Konsolen-API-Ausgabe von Microsoft Edge 85 oder früher in Visual Studio-Code eingefügt" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Konsolen-API-Ausgabe von Microsoft Edge 85 oder früher in Visual Studio-Code eingefügt  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Wenn Sie in Microsoft Edge 86 oder höher eine Tabelle aus der **Konsole**kopieren, ist die Formatierung nun erhalten.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Ausgabe der Tabellen Konsolen-API in Microsoft Edge 86 oder höher" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Ausgabe der Konsolen-API in Microsoft Edge 86 oder höher  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Tabellen Konsolen-API-Ausgabe von Microsoft Edge 86 oder später eingefügt in Visual Studio-Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Konsolen-API-Ausgabe von Microsoft Edge 86 oder später eingefügt in Visual Studio-Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chrom Problem: [#1115011] [CR1115011]  

### Viewer für Quellreihenfolge für einfachere Tests zur Barrierefreiheit  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   Experimentelle Funktion  
:::image-end:::  

Die neue Barrierefreiheits Hilfe zeigt die Reihenfolge der Elemente in der Quelle an.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Aktivieren der Quellreihenfolge anzeigen" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Aktivieren der **Quellreihenfolge anzeigen**  
:::image-end:::  

Dieses Feature macht es einfacher, die Art und Weise zu testen, wie Sprachausgabe und Tastatur Benutzer Ihre Website oder App erleben.  Bildschirmsprachausgaben und Tastaturnavigation hängen davon ab, ob Inhalte in einer bestimmten Reihenfolge im Quellcode Ihrer Website oder App gespeichert werden, damit Sie der gerenderten Seite entsprechen.  In der Quellauftrags Anzeige werden potenzielle Unterschiede in der Reihenfolge zwischen der gerenderten Seite und dem Quellcode angezeigt.  

Wenn Sie dieses experimentelle Feature aktivieren möchten, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **Quellauftrags Anzeige aktivieren**.  

Weitere Informationen zu diesem Experiment finden Sie unter [Aktivieren der Quellauftrags Anzeige][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Chromium-Problem: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### Markieren aller Suchergebnisse im elementtool  

In Microsoft Edge 84 und 85 wurde das erste Suchergebnis im **Element** Panel nicht markiert.  Die restlichen Suchergebnisse wurden richtig hervorgehoben.  

Vielen Dank für Ihr Feedback und die Verbesserung von Chrom.  Ihr Feedback hat ein Problem [#1103316][CR1103316] im Open-Source-Projekt Chromium aufgedeckt.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Hervorgehobenes erstes Suchergebnis im Element Panel in Microsoft Edge 84 oder höher" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Hervorgehobenes erstes Suchergebnis im **Element** Panel in Microsoft Edge 84 oder höher  
:::image-end:::  

Das Problem ist jetzt in allen Versionen von Microsoft Edge behoben.  

Chromium-Problem: [#1103316][CR1103316]  

## Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Neues Medien Panel  

DevTools zeigt nun Informationen zu Medienplayern im [Medien][DevtoolsMediaIndex] Panel an.  

Führen Sie den folgenden Schritt aus, um den neuen **Medien** Panel zu öffnen.  

1.  Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **Medien**aus.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Neues Medien Panel" lightbox="../../media/2020/08/media-panel.msft.png":::
       Neues **Medien** Panel  
    :::image-end:::  

Vor dem neuen **Medien** Panel in devtools befanden sich die Protokollierungs-und Debuginformationen zu Videoplayern unter der Einstellung " **zuletzt verwendete Spieler** ".  Wenn Sie die Einstellung für **zuletzt verwendete Spieler** öffnen möchten, wechseln Sie zu `edge://media-internals` und wählen Sie den Reiter **Spieler** aus.  

Zeigen Sie Liveinhalte an, und prüfen Sie potenzielle Probleme schneller, einschließlich der folgenden Beispiele.  

*   Warum werden Frames verworfen?  
*   Warum wird JavaScript in einer unerwarteten Weise mit dem Spieler interagieren?  

### Aufzeichnen von Knoten Screenshots über das Kontextmenü des Elements Panels  

Sie können nun Knoten Screenshots über das Kontextmenü im Bereich " **Elemente** " erfassen.  

Wenn Sie beispielsweise einen Screenshot des Inhaltsverzeichnisses erstellen möchten, zeigen Sie auf das Element, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Screenshot des Knotens aufzeichnen**aus.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Screenshots des Knotens aufzeichnen" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Screenshots des Knotens aufzeichnen  
:::image-end:::  

Chromium-Problem: [#1100253][CR1100253]  

### Probleme mit Tool Updates  

Die warnungsleiste "Probleme" im **Konsolen** Bereich wird nun durch eine normale Nachricht ersetzt.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Probleme in der Konsolen Nachricht" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Probleme in der Konsolen Nachricht  
:::image-end:::  

Probleme mit Cookies von Drittanbietern sind jetzt standardmäßig im **Problem** Tool ausgeblendet.  Aktivieren Sie das Kontrollkästchen neues **einbeziehen von Cookies von Drittanbietern** , um die Probleme anzuzeigen.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Kontrollkästchen für Cookies von Drittanbietern" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   Kontrollkästchen für Cookies von Drittanbietern  
:::image-end:::  

Chrom Probleme: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### Emulieren fehlender lokaler Schriftarten  

Öffnen Sie das [Rendering-Tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] , und verwenden Sie das neue Feature **lokale Schriftarten deaktivieren** , um fehlende `local()` Quellen in Regeln zu emulieren `@font-face` .  

Wenn die Schriftart beispielsweise `Rubik` auf Ihrem Gerät installiert ist und von der `@font-face src` Regel als Schriftart verwendet wird `local()` , verwendet Microsoft Edge die lokale Schriftartdatei auf Ihrem Gerät.  

Wenn **lokale Schriftarten deaktivieren** aktiviert ist, ignoriert devtools die `local()` Schriftarten und ruft alle aus dem Netzwerk ab.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emulieren fehlender lokaler Schriftarten" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emulieren fehlender lokaler Schriftarten  
:::image-end:::  

Wenn Sie während der Entwicklung zwei unterschiedliche Kopien derselben Schriftart verwenden, wie beispielsweise die folgenden Beispiele.  

*   Eine lokale Schriftart für Ihre Entwurfstools.  
*   Eine Web-Schriftart für Ihren Code.  

Verwenden Sie **lokale Schriftarten deaktivieren** , damit Sie die folgenden Aufgaben einfacher ausführen können.  

*   Debuggen und Messen der Ladeleistung und Optimierung von Webschriftarten  
*   Überprüfen Sie die Genauigkeit Ihrer CSS `@font-face` -Regeln.  
*   Entdecken Sie Unterschiede zwischen lokalen Versionen, die auf Ihrem Gerät installiert sind, und einer Web-Schriftart.  

Chromium-Problem: [#384968][CR384968]  

### Emulieren inaktiver Benutzer  

Die [API für die Leerlauferkennung][WebDevIdleDetection] ermöglicht es Entwicklern, inaktive Benutzer zu erkennen und auf Leerlauf Zustandsänderungen zu reagieren.  Sie können jetzt devtools verwenden, um die Änderungen im Leerlaufzustand im **Sensor** Tool sowohl für den Benutzerzustand als auch für den Bildschirm Zustand zu emulieren, anstatt zu warten, bis der Zustand des tatsächlichen Ruhezustands geändert wird.  Sie können das Tool **Sensoren** aus der [Schublade][DevtoolsCustomizeIndexDrawer]öffnen.  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emulieren inaktiver Benutzer" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emulieren inaktiver Benutzer  
:::image-end:::  

Chromium-Problem: [#1090802][CR1090802]  

### Emulieren bevorzugt-reduzierte Daten  

> [!NOTE]
> Wenn Sie dieses Feature in Microsoft Edge 86 aktivieren möchten, wechseln Sie zu, `edge://flags#enable-experimental-web-platform-features` und aktivieren Sie das Kennzeichen **experimentelle webplattforms-Features** .  Die Emulations Option wird nur angezeigt, wenn das Flag aktiviert ist.  

Die Abfrage " [bevorzugt reduzierte Daten][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] Medien" erkennt Benutzerinhalts Einstellungen für reduzierte Daten.  Wenn diese Option ausgewählt ist, erhält der Benutzer Alternativen Seiteninhalt, in dem geringere Daten verwendet werden.  

Sie können jetzt devtools verwenden, um die medienabfrage zu emulieren `prefers-reduced-data` .  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emulieren bevorzugt-reduzierte Daten" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emulieren bevorzugt-reduzierte Daten  
:::image-end:::  

Chromium-Problem: [#1096068][CR1096068]  

### Unterstützung für neue JavaScript-Features  

DevTools haben nun die folgenden JavaScript-Sprachfeatures besser unterstützt.  

| JavaScript-Sprachfeature | Details |  
|:--- |:--- |  
| [Logische Zuordnungs Operatoren][V8FeaturesLogicalAssignment] | DevTools unterstützt jetzt die logische Zuordnung mit dem neuen `&&=` `||=` und den `??=` Operatoren in den Panels **Console** und **Sources** .  |  
| Pretty-Print- [numerische Trenn][V8FeaturesNumericSeparators] Zeichen | DevTools nun richtig hübsch – druckt die numerischen Trennzeichen im **Quellen** Panel.  |  

Probleme mit Chrom: [1086817][CR1086817], [1080569][CR1080569]  

### Leuchtturm 6,2 im Leuchtturm-Panel  

Auf dem **Leuchtturm** -Panel läuft nun Lighthouse 6,2.  Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Lighthouse-Version][GithubGooglechromeLighthouseV620].  

Chromium-Problem: [#772558][CR772558]  

### Deprecated of other Origins-Eintrag im Bereich "Dienstmitarbeiter"  

DevTools bietet nun einen Link im Bereich " **Dienstmitarbeiter** " \ (**Anwendungs** Bereich > Bereich " **Dienstmitarbeiter** \"), um die vollständige Liste der Servicemitarbeiter anderer Herkunft anzuzeigen.  Wechseln Sie zu, um auf die Liste zuzugreifen, ohne das devtools zu öffnen `edge://service-worker-internals/?devtools` .  

Zuvor devtools eine Liste angezeigt, die unter dem **Anwendungs** Bereich > Bereich " **Dienstmitarbeiter** " geschachtelt ist.  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Link zu anderen Ursprüngen" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Link zu anderen Ursprüngen  
:::image-end:::  

Chromium-Problem: [#807440][CR807440]  

### Anzeigen der Deckungs Zusammenfassung für gefilterte Elemente  

DevTools wird nun dynamisch neu berechnet und eine Zusammenfassung der Deckungs Informationen angezeigt.  Die dynamische Anzeige wird ausgelöst, wenn Filter im [Coverage][DevtoolsCoverageIndex] -Tool angewendet werden.  Vor dem **Coverage** -Tool wird immer eine Zusammenfassung aller Deckungs Informationen angezeigt.  

In der ersten der folgenden Zahlen wird die Zusammenfassung zunächst angezeigt, `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` und in der zweiten der folgenden Zahlen wird die Zusammenfassung angezeigt, `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` nachdem die CSS-Filterung angewendet wurde.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Deckungs Zusammenfassung" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Deckungs Zusammenfassung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Deckungs Zusammenfassung für gefilterte Elemente" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Deckungs Zusammenfassung für gefilterte Elemente  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Chromium-Problem: [#1061385][CR1090802]  

### Neue Frame Detailansicht im Anwendungsbereich  

DevTools zeigen nun eine detaillierte Ansicht für jeden Frame an.  Um darauf zuzugreifen, wählen Sie im **Anwendungs** Bereich unter dem Menü **Frames** einen Frame aus.  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Neue Detailansicht für einen Frame im Anwendungsbereich" lightbox="../../media/2020/08/frame-details.msft.png":::
   Neue Detailansicht für einen Frame im **Anwendungs** Bereich  
:::image-end:::  

Chromium-Problem: [#1093247][CR1093247]  

#### Frame Details für geöffnete Fenster  

Geöffnete Fenster und Popupfenster werden nun auch unter der Frame Struktur angezeigt.  Die Detailansicht der geöffneten Fenster enthält zusätzliche Sicherheitsinformationen.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Neue Frame-Detailansicht für geöffnete Fenster" lightbox="../../media/2020/08/window-opener.msft.png":::
   Neue Frame-Detailansicht für geöffnete Fenster  
:::image-end:::  

Chrom Problem: [#1107766] [CR1107766]  

#### Sicherheits-und Isolierungsinformationen  

Sicherer Kontext, [Cross-Origin-embeder-Policy (COEP)][WebDevCoopCoep]und [Cross-Origin-Opener-Policy (Coop)][WebDevCoopCoep] werden jetzt in den Frame Details angezeigt.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Sicherheits-und Isolierungsinformationen" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Sicherheits-und Isolierungsinformationen  
:::image-end:::  

In Zukunft planen das Microsoft Edge devtools-Team und das Chrome devtools-Team, weitere Sicherheitsinformationen zu den Frame Details hinzuzufügen.  

Chromium-Problem: [#1051466][CR1051466]  

### Elemente und Aktualisierungen des Netzwerk Panels  

#### Vorschlag für barrierefreie Farben im Bereich "Formatvorlagen"  

DevTools bietet jetzt Farbvorschläge für Text mit niedriger Farbkontrast.  

Im folgenden Beispiel `h1` ist Text mit geringem Kontrast.  Um das Problem zu beheben, öffnen Sie die Farbauswahl der `color` Eigenschaft im Bereich **Formatvorlagen** .  Nachdem Sie den Abschnitt **Kontrastverhältnis** erweitert haben, bietet devtools AA-und AAA-Farbvorschläge.  Wählen Sie die vorgeschlagene Farbe aus, um die Farbe anzuwenden.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Farbauswahl schlägt Vorschläge für AA-und AAA-Farben vor" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Farbauswahl schlägt Vorschläge für AA-und AAA-Farben vor  
:::image-end:::  

Chromium-Problem: [#1093227][CR1093227]  

#### Bereich ' Eigenschaften wiederherstellen ' im Bereich ' Elemente '  

Der Bereich " **Eigenschaften** " ist "zurück".  Es war [in Microsoft Edge 84 veraltet][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  Das Microsoft Edge devtools-Team und das Chrome devtools-Team planen Verbesserungen bei der Überprüfung von Eigenschaften von Elementen.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Bereich ' Eigenschaften ' im Bereich ' Elemente '" lightbox="../../media/2020/08/properties-pane.msft.png":::
   Bereich ' **Eigenschaften** ' im Bereich ' **Elemente** '  
:::image-end:::  

Chromium-Problem:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### AutoVervollständigen von benutzerdefinierten Schriftarten im Bereich "Formatvorlagen"  

Importierte Schrift Flächen werden jetzt der Liste der CSS-Autovervollständigung hinzugefügt, wenn die `font-family` Eigenschaft im Bereich " **Formatvorlagen** " bearbeitet wird.  

Wenn beispielsweise `monospace` eine benutzerdefinierte Schriftart auf dem lokalen Computer installiert ist, wird Sie in der Liste CSS-Vervollständigung angezeigt. In früheren Versionen von Microsoft Edge wurde die Schriftart nicht angezeigt.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Benutzerdefinierte AutoVervollständigen-Schriftarten" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Benutzerdefinierte AutoVervollständigen-Schriftarten  
:::image-end:::  

Chrom Problem: [#1106221] [CR1106221]  

#### Konsistente Anzeige des Ressourcentyps in der Netzwerksteuerung  

DevTools zeigt jetzt konsistent denselben Ressourcentyp wie die ursprüngliche Netzwerkanforderung an und fügt `/ Redirect` beim Umleiten \ (HTTP-Statuscode 302 \) den Wert der Spalte **Typ** an.  

Zuvor hat devtools den Typ in `Other` Sometimes geändert.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Anzeigen des Umleitungs Ressourcentyps" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Anzeigen des Umleitungs Ressourcentyps  
:::image-end:::  

Chromium-Problem: [#997694][CR997694]  

#### Löschen von Schaltflächen in den Elementen und Netzwerk Fenstern  

Die folgenden Textfelder verfügen nun über **klare** Schaltflächen.  

*   Die Felder ' Text filtern ' im Bereich ' **Formatvorlagen** ' und ' **Netzwerk** Bereich '  
*   Das Textfeld "Dom-Suche" im Dialogfeld " **Elemente** ".  

Wählen Sie die Schaltfläche **Löschen** aus, um den eingegebenen Text zu entfernen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Löschen von Schaltflächen in den Elementen-Panels" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Löschen von Schaltflächen in den **Elementen** -Panels  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Löschen von Schaltflächen in den Netzwerk Panels" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Löschen von Schaltflächen in den  **Netzwerk** Panels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium-Problem: [#1067184][CR1067184]  

## Herunterladen der Microsoft Edge Preview-Kanäle  

Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.  Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Symbol für devtools-Einstellungen"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Missbilligung des Bereichs "Eigenschaften" im Bereich "Elemente" – Neuerungen in devtools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features des CSS-Raster Debuggens – Neuerungen in devtools (Microsoft Edge 85) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellauftrags Anzeige – experimentelle Features | Microsoft docs"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf faltbaren und Dual-Screen-Geräten – experimentelle Funktionen | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von experimentellen Features – experimentelle Features | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle-Console-API-Referenz | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie ungenutzten JavaScript-und CSS-Code mit der Registerkarte Coverage in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendering" – Referenz zur Leistungsanalyse | Microsoft docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Anzeigen und Debuggen von Medienplayer-Informationen | Microsoft docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Dual-Screen-Geräte | Microsoft docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "CSS mediascreen-Spanning-Funktion für Dual-Screen-Erkennung | Microsoft docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-Geräte | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview-Kanäle"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio-Code "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio-Code Tastenkombinationen für Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter-Konto"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: zulassen der Anpassung von Tastenkombinationen/Tastenkombinationen | Chrom Fehler"
[CR384968]: https://crbug.com/384968 "Option zum ignorieren lokaler () Schriftarten | Chrom Fehler"  
[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von Lighthouse | Chrom Fehler"  
[CR807440]: https://crbug.com/807440 "Chrome sperrt mit einer hohen Anzahl von SWs | Chrom Fehler"  
[CR997694]: https://crbug.com/997694 "XMLHttpRequest-Anforderungen mit 302-Status werden nicht unter dem Filter \ "XMLHttpRequest \" im Netzwerk Panel angezeigt | Chrom Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Tabellentools"  
[CR1051466]: https://crbug.com/1051466 "Unterstützen des Coop/COEP-Debuggens in devtools | Chrom Fehler"  
[CR1054281]: https://crbug.com/1054281 "Feature Request: devtools sollte faltbare und Dual-Screen-Geräte emulieren | Chrom Fehler"  
[CR1067184]: https://crbug.com/1067184 "Feature Request: Schaltfläche "Filter löschen" im Netzwerk &-Elemente-> Formatfilter Eingaben | Chrom Fehler"  
[CR1068116]: https://crbug.com/1068116 "☂ Bereich "Schiffs Probleme" | Chrom Fehler"  
[CR1080569]: https://crbug.com/1080569 "Acorn unterstützt keine logischen Zuweisungsoperatoren | Chrom Fehler"  
[CR1080589]: https://crbug.com/1080589 "Klassifizieren von Problemen durch Drittanbieter/First-Party | Chrom Fehler"  
[CR1086817]: https://crbug.com/1086817 "Acorn unterstützt keine numerischen Trennzeichen | Chrom Fehler"  
[CR1090802]: https://crbug.com/1090802 "Simulieren von Änderungen im Leerlaufzustand aus der Leerlauf Erkennungs-API | Chrom Fehler"  
[CR1093227]: https://crbug.com/1093227 "DevTools: empfehlen Sie die nächste barrierefreie Farbe | Chrom Fehler"  
[CR1093247]: https://crbug.com/1093247 "Anzeigen von Informationen zu Frames im Anwendungs Panel | Chrom Fehler"  
[CR1094406]: https://crbug.com/1094406 "Entwickler möchten eine Quellauftrags Anzeige für at https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: Unterstützung emuliert das Feature "bevorzugt-reduzierte Datenmedien" | Chrom Fehler"  
[CR1096481]: https://crbug.com/1096481 "Issues Banner Placement | Chrom Fehler"  
[CR1100253]: https://crbug.com/1100253 "Verknüpfung zum Hinzufügen eines Screenshot-Knotens im Kontextmenü des Elements | Chrom Fehler"  
[CR1103316]: https://crbug.com/1103316 "Beim ersten Suchergebnis wird die Element Suche nicht resolveNode (Text markieren usw.) | Chrom Fehler"  
[CR1103854]: https://crbug.com/1103854 "De-verschleiern von X-Client-Datenwerten in Developer Tools | Chrom Fehler"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Hinzufügen von importierten Schriftarten zur Autovervollständigung der Schriftartfamilie im Formatvorlagen-Panel | Chromium-Fehler "  
[CR1107766]: https://crbug.com/1107766 "zeigt Informationen zu Frames an, die von" Window. Open () "in der Frame Struktur generiert wurden | Chromium-Fehler "  
[CR1115011]: https://crbug.com/1115011 "beim Kopieren einer Tabelle aus der Konsole wird die Struktur der Tabelle nicht beibehalten | Chromium-Fehler "  
[CR1116085]: https://crbug.com/1116085 "Bitte bringen Sie den devtools-Eigenschafteninspektor zurück | Chromium-Fehler "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "bevorzugt-reduzierte Datenmedien Abfragen Ebene 5 | W3C CSS-Arbeitsgruppen-Editor-Entwürfe"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Protokollpuffer | Google-Entwickler"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung USA"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Logische Zuordnung | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Numerische Trennzeichen | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Erstellen Ihrer Website \ "Cross-Origin isolated \" mit Coop und COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Erkennen von inaktiven Benutzern mit der Leerlauf Erkennungs-API | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Vermeiden Sie nicht zusammengesetzte Animationen | Web. dev"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/08/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
