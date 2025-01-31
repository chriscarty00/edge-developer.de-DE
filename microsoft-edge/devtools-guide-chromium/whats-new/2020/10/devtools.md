---
description: Neue CSS Grid-Debuggingtools, Webauthn-Tool, verschiebbare Tools und berechnete Seitenleisten.
title: Neues in DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564896"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-87"></a>Neues in DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a>Verbessern der DevTools-Lokalisierung  

Um Ihre Übersetzungsanforderungen zu erfüllen, konzentriert sich Microsoft Edge DevTools-Team auf die Verbesserung der Übersetzungsqualität.  Ab Microsoft Edge Version 87 sind mehrere Zeichenfolgen und Begriffe gesperrt und ändern sich nicht, auch wenn die restlichen DevTools in anderen Sprachen angezeigt werden.  Die Liste der betroffenen Zeichenfolgen und Begriffe umfasst Folgendes.  

*   Die Zeichenfolgen im **Tool "Leuchttürme".**  
*   Der Begriff `service worker` .  
*   Einige der **Netzwerktoolfilter** wie `URL` , , und `XHR` `JS` `CSS` .  
*   Die [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] Console Utilities-API.  
    
[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] ist jetzt in der [Konsole][DevtoolsConsoleIndex] für Benutzer in lokalisierten Versionen der DevTools verfügbar.   Vielen Dank an die globale Entwickler-Community für die Verbesserung der Lokalisierung der Microsoft Edge DevTools.  Senden Sie [weiterhin Feedback zur Lokalisierungsqualität,](#getting-in-touch-with-microsoft-edge-devtools-team) um die Unterstützung für DevTools in allen Locales zu verbessern.  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1136655][CR1136655].  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Netzwerktool mit nicht lokalisierten Filtern" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Netzwerkbereich** mit nicht lokalisierten Filtern  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Verschieben von Tools zwischen oberen und unteren Panels  

DevTools unterstützt jetzt das Verschieben von Tools zwischen dem oberen und unteren Bereich.  Passen Sie Ihre DevTools an, und verbessern Sie Ihre Produktivität, indem Sie eine beliebige Kombination von zwei Tools gleichzeitig anzeigen.  Zeigen Sie z. B. die **Elemente** und die **Sources-Tools** gleichzeitig an \(durch Verschieben des **Tools Sources** nach unten\).  Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium Open Source-Projekt zu Problem [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Um ein beliebiges oberstes Tool nach unten zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Nach unten verschieben aus.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Nach unten verschieben" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Nach unten verschieben  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Um ein beliebiges unteres Tool nach oben zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Nach oben verschieben aus.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Nach oben verschieben" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Nach oben verschieben  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a>Speichern und Exportieren mithilfe der Netzwerkkonsole  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Das **Tool für die** Netzwerkkonsole hat nun die Kompatibilität mit den [Schemas Postman v2.1][PostmanSchemaJsonCollectionv210Index] und [OpenAPI v2][SwaggerSpecificationV2] verbessert.  Navigieren Sie zum Aktivieren des Experiments zu [Aktivieren von Experimentellen Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Netzwerkkonsole aktivieren.**  Weitere Informationen zur **** Netzwerkkonsole finden Sie unter [Feature NetzwerkkonsolenexperimentalFeaturesEnableNetworkConsole aktivieren][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Dieses Experiment unterstützt nun die folgenden Aktionen.  

*   Speichern und exportieren Sie Sammlungen und Umgebungen.  
*   Bearbeiten und exportieren Sie Sätze von Umgebungsvariablen im **Netzwerkkonsolentool.**  
    
Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Geben Sie den Namen für die neue Umgebung ein." lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Geben Sie den Namen für die neue Umgebung ein.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Auswählen des Formats für die neue Umgebung" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Auswählen des Formats für die neue Umgebung  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a>Verbessertes CSS-Raster-Tool  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Die Microsoft Edge DevTools unterstützen nun die folgenden Features zum Überprüfen, Anzeigen und Debuggen Ihrer CSS-Raster.  

*   Zeigen Sie eine vereinfachte Rasterüberlagerung mit dem **Tool Inspect** an, oder erhalten Sie detailliertere Informationen mit beständigen Überlagerungen.  
*   Wenn Sie dauerhafte Rasterüberlagerungen aktivieren möchten, wählen Sie das Rastersymbol neben einem Rastercontainerelement im **Tool Elemente** aus, oder wählen Sie das Raster im **Layouttool** aus.  
*   Sie können dauerhafte Überlagerungen für mehrere Raster aktivieren.  
*   Mit dem **neuen Layout-Tool** können Sie Gitternetzüberlagerungen einfach umschalten und die Darstellung und den Inhalt für die einzelnen Einstellungen konfigurieren.  
    
Die Features sind standardmäßig aktiviert.  Weitere Informationen zu den Features finden Sie unter [CSS-Raster][DevtoolsCssGrid].  Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium Open Source-Projekt zu Problem [#1047356][CR1047356].  Darüber hinaus arbeitet Microsoft Edge DevTools-Team mit dem Chrome DevTools-Team und der Chromium zusammen, um DevTools neue Flexbox-Toolfunktionen hinzuzufügen.  Informationen zu Updates für die flexbox-Tools im Chromium-Open-Source-Projekt finden Sie unter Issue [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Layouttool mit Rastern" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Layouttool** mit Rastern  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Anpassen von Tastaturkürzeln in den Einstellungen  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Sie können nun die Tastenkombination für alle Aktionen in devTools anpassen.  Seit Microsoft Edge Version 84 können Sie zwischen **** Visual Studio Code und **DevTools (Standard)-Voreinstellungen** für Tastenkombinationen [wählen.][DevtoolsCustomizeShortcuts]  Ab Microsoft Edge Version 87 können Sie das **** Experiment Tastenkombinationen-Editor aktivieren, um Tastenkombinationen [weiter anzupassen.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]  

Navigieren Sie zum Aktivieren des Experiments zu [Aktivieren von Experimentellen Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben Tastenkombinationen-Editor **aktivieren.**  Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter Bearbeiten von Tastenkombinationen für alle Aktionen [in devTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open [Source-Projekt][CR174309]zu Problem #174309 .  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Einführung in Microsoft Edge Tools for Visual Studio Code Extension  

Die **Elemente für Visual Studio Code** und Network for **Visual Studio Code** werden nun mit den neuen Microsoft Edge Developer Tools [for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] zusammengeführt.  Verwenden Sie Microsoft Edge DevTools für die folgenden Aktivitäten, ohne Microsoft Visual Studio zu lassen.  

*   Debuggen des DOM  
*   Bearbeiten von CSS  
*   Überprüfen des Netzwerkdatenverkehrs  

Starten Sie mit der Erweiterung Microsoft Edge, stellen Sie eine Verbindung mit einer vorhandenen Instanz des Browsers oder verwenden Sie einen headless-Browser direkt von Ihrem Editor aus.  Um Mitwirken und Ablegen von Problemen mit Ihrem Feedback zu dieser Erweiterung zu beginnen, navigieren Sie zum [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repository on GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Screenshot mit der Erweiterung im vollständigen Browsermodus" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Screenshot mit der Erweiterung im vollständigen Browsermodus  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Verwenden der Erweiterung im Kopflosenmodus screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Verwenden der Erweiterung im Kopflosenmodus screenshot  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a>Neues WebAuthn-Tool  

In früheren Versionen von Microsoft Edge gab es keine systemeigene WebAuthn-Debuggingunterstützung.  Sie benötigten physische Authentisierungsgeräte, um Ihre Webanwendung mit der [Webauthentifizierungs-API zu testen.][GithubW3cWebauthn]  Mit dem neuen **WebAuthn-Tool** können Sie die folgenden Aktionen ausführen, ohne physische Authentisierungen zu verwenden.

*   Emulieren von Authentatoren
*   Anpassen von Attributen von Authentatoren
*   Überprüfen der Zustände von Authentatoren
    
Weitere Informationen zum **WebAuthn-Feature** finden Sie unter [Emulieren von Authentifizierungsautoren und Debuggen von WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Sie können Authentisierungsgeräte emulieren und die [Webauthentifizierungs-API][GithubW3cWebauthn] mit dem neuen [WebAuthn][DevtoolsWebauthnIndex]-Tool debuggen.  Wählen Sie zum Öffnen des **WebAuthn-Tools** das Symbol **DevTools** anpassen \( \) > `...` Weitere **Tools**  >  **WebAuthn aus.**  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Öffnen des WebAuthn-Tools" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Öffnen des **WebAuthn-Tools**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="WebAuthn-Tool" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **WebAuthn-Tool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a>Aktualisierungen des Tools „Elemente“  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Anzeigen des Seitenleistenbereichs "Berechnet" im Bereich Formatvorlagen  

Schaltet den **Bereich Berechnet** im Bereich **Formatvorlagen** um.  Der **Bereich Berechnet** im Bereich **Formatvorlagen** ist standardmäßig reduziert.  Um ihn umschalten zu können, wählen Sie die Schaltfläche aus.  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Öffnen des Seitenleistenbereichs Berechnet" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Öffnen des **Seitenleistenbereichs "Berechnet"**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Berechneter Seitenleistenbereich" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Berechneter Seitenleistenbereich**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a>Gruppieren von CSS-Eigenschaften im Berechneten Bereich  

Um die angewendete CSS mit weniger Bildlauf anzuzeigen, gruppieren Sie die CSS-Eigenschaften nach Kategorien im **Bereich Berechnet.**  Sie können sich auch selektiv auf eine Reihe verwandter Eigenschaften konzentrieren, während Sie Ihre CSS überprüfen.  Wählen Sie **im Elementtool** ein Element aus.  Um die CSS-Eigenschaften \(oder ungroup\) zu gruppieren, aktivieren Sie das **Kontrollkästchen Gruppe.**  Navigieren Sie zu Probleme [#1096230][CR1096230], [#1084673][CR1084673]und #1106251 , um Echtzeitupdates für dieses Feature im open-source-Projekt Chromium zu [überprüfen.][CR1106251]  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Gruppieren von CSS-Eigenschaften" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Gruppieren von CSS-Eigenschaften  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool&quot;></a>Leuchttürme 6.4 im Tool &quot;Leuchttürme"  

Das **Tool "Leuchtturm"** wird jetzt mit "6.4" ausgeführt.  Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Veröffentlichung von "Leuchttürme".][GithubGoogleChromeLighthouseReleasesV641]  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>performance.mark()-Ereignisse im Abschnitt Timings  

Der **Abschnitt Timings einer** Aufzeichnung im Tool ["Leistung"][DevtoolsEvaluatePerformanceReference] markiert nun `performance.mark()` Ereignisse.  Um dieses Feature auszuprobieren und die Leistung Ihres JavaScript-Codes zu messen, fügen Sie `performance.mark()` Dem Code Ereignisse hinzu.  Der folgende Codeausschnitt fügt z. B. Markierungen vor und nach einer Schleife hinzu, die mithilfe von Schritten von 7 von 0 auf `for` 1000 iteriert wird.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Öffnen Sie dann das [Tool Leistung,][DevtoolsEvaluatePerformanceReference] und navigieren Sie zum **Abschnitt Timings,** um Ihren JavaScript-Code zu aufzeichnen.  Die `performance.mark()` hinzugefügten Ereignisse werden nun in der Aufzeichnung angezeigt.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance.mark-Ereignisse" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` Ereignisse  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Neue Ressourcentyp- und URL-Filter im Netzwerktool  

Verwenden Sie das neue `resource-type` und `url` Schlüsselwörter im **Netzwerktool,** um Netzwerkanforderungen zu filtern.  Verwenden Sie beispielsweise, `resource-type:image` um sich auf die Netzwerkanforderungen zu konzentrieren, die Bilder sind.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ressourcentypfilter" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   Ressourcentypfilter  
:::image-end:::  

Navigieren Sie zu `resource-type` `url` [Filteranforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties].  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Probleme [#1121141][CR1121141] und [#1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Updates der Frame-Detailansicht  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Anzeigen der COEP- und COOP-Berichterstellung an den Endpunkt  

Zeigen Sie die Endpunkte Cross-Origin Embedder Policy \(COEP\) und Cross-Origin Opener Policy \(COOP\) unter dem Abschnitt Sicherheit `reporting to` **& Isolation** an.  Die [Berichts-API][MdnReportingApi] definiert `Report-To` einen neuen HTTP-Header, mit dem Sie die Serverendpunkte für den Browser zum Senden von Warnungen und Fehlern angeben können.  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Die Berichterstellung an den Endpunkt" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   Der `reporting to` Endpunkt  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Anzeigen des NS-Berichtsmodus für COEP und COOP  

DevTools zeigt jetzt die `report-only` Bezeichnung für COEP und COOP an, die auf den Modus `report-only` festgelegt sind.  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Bezeichnung für den Nur-Bericht-Modus" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Die `report-only` Bezeichnung für den Modus  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Anzeigen und Beheben von Farbkontrastproblemen im CSS-Übersichtstool  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Das **Tool CSS Overview** zeigt nun eine Liste der Elemente auf Ihrer Seite an, die Probleme mit dem Farbkontrast haben.  Die folgende Demoseite enthält ein Beispiel für ein Farbkontrastproblem.  

[DEMO zu barrierefreien Farben (CSS Overview Accessible Colors)][GlitchCssOverviewAccessibleColorsDemo]  

Aktivieren Sie zum Aktivieren dieses **Experiments Einstellungen**  >  **Experimenten**das **Kontrollkästchen CSS-Übersicht.**  Wenn Sie eine Liste der Elemente anzeigen möchten, bei der ein Farbkontrastproblem besteht, wählen Sie unter **Kontrastprobleme** **Text aus.**  Um das Element im **Elementtool zu** öffnen, wählen Sie ein Element in der Liste aus.  Um Kontrastprobleme zu beheben, stellt Microsoft Edge DevTools [automatisch Farbvorschläge zur Verfügung.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Chromium Open Source-Projekt zu Problem [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Probleme mit geringem Farbkontrast" lightbox="../../media/2020/10/css-overview.msft.png":::
   Probleme mit geringem Farbkontrast  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie sich auf Windows oder macOS befinden, sollten Sie die Microsoft Edge Vorschaukanäle [als][MicrosoftEdgePreviewChannels] Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Veralteter Eigenschaftenbereich im Elementtool – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features zum Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Barrierefreier Farbvorschlag im Bereich Formatvorlagen – Neues in DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Verwenden der Konsolenanwendung | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Kürzlich ausgewähltes Element- oder JavaScript-Objekt – Apireferenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Bearbeiten von Tastenkombinationen für alle Aktionen im DevTools-| Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Unterstützung des dualen Bildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Aktivieren experimenteller APIs – Experimentelle | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console "Enable Network Console - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Microsoft Docs&quot; [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices &quot;Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table "table - Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md "Suchen sie nicht verwendeten JavaScript- und CSS-Code mit der Registerkarte Abdeckung in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md "Überprüfen der CSS Grid-| Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer "Drawer - Customize Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings "Einstellungen - Customize Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte Rendering – Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md "Emulieren von Authentifizierungsautoren und Debuggen von WebAuthn in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium Fehler"
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von &quot;| Chromium Fehler"  
[CR1034663]: https://crbug.com/1034663 "Erstellen eines Front-Ends für die WebAuthn Testing-API | Chromium Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützung des COOP/COEP-Debuggings in DevTools | Chromium Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte &quot;Berechnete Formatvorlage&quot; wird im reaktionsschnellen Modus | Chromium Fehler"  
[CR1075732]: https://crbug.com/1075732 "DevTools-Personalisierung – Wechselregisterkarten | Chromium Fehler"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Verbessern Sie die Art und Weise, wie wir benutzerdefinierte CSS-Eigenschaften ((auch bekannt) präsentieren. CSS-Variablen) und deren Werte | Chromium Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellen eines Tools zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium Fehler"  
[CR1096230]: https://crbug.com/1096230 "Gruppieren von CSS-Eigenschaften nach Kategorien im Bereich &quot;Computed Styles&quot; | Chromium Fehler"  
[CR1104188]: https://crbug.com/1104188 "Bei der Suche nach vollständigen URL-Adressen findet die Netzwerktoolsuche keine | Chromium Fehler"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: Verbessern der Registerkarten für berechnete Formatvorlagen | Chromium Fehler"  
[CR1120316]: https://crbug.com/1120316 "Hervorheben eines schlechten Kontrasts unter CSS Overview > Colors | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Filtern nach Ressourcentyp in Netzwerkprotokollen | Chromium Fehler"  
[CR1121312]: https://crbug.com/1121312 "Einstellungen sollten aus dem Menü &quot;Weitere Tools&quot; entfernt | Chromium Fehler"  
[CR1136394]: https://crbug.com/1136394 "Flexbox-| Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Lokalisierung V2 | Chromium Fehler"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Berichterstellungs-API-| MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 – GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierungs-| GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hello! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI-Spezifikations-| Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-87) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
