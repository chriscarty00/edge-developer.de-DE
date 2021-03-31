---
description: Neue CSS Grid-Debuggingtools, Webauthn-Tool, verschiebbare Tools und berechnete Seitenleisten.
title: Neues in DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 53aa8f20ba400c7ff95432b1e752f1f008dac919
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408332"
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

Um Ihre Übersetzungsanforderungen zu erfüllen, konzentriert sich das Microsoft Edge DevTools-Team auf die Verbesserung der Übersetzungsqualität.  Ab Microsoft Edge, Version 87, sind mehrere Zeichenfolgen und Begriffe gesperrt und ändern sich nicht, auch wenn die restlichen DevTools in anderen Sprachen angezeigt werden.  Die Liste der betroffenen Zeichenfolgen und Begriffe umfasst Folgendes.  

*   Die Zeichenfolgen im **Tool "Leuchttürme".**  
*   Der Begriff `service worker` .  
*   Einige der **Netzwerktoolfilter** wie `URL` , , und `XHR` `JS` `CSS` .  
*   Die [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities-API.  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] ist jetzt in der [Konsole](/microsoft-edge/devtools-guide-chromium/console/index.md) für Benutzer in lokalisierten Versionen der DevTools verfügbar.   Vielen Dank an die globale Entwickler-Community, dass Sie die Lokalisierung von Microsoft Edge DevTools verbessert haben.  Senden Sie [weiterhin Feedback zur Lokalisierungsqualität,](#getting-in-touch-with-microsoft-edge-devtools-team) um die Unterstützung für DevTools in allen Locales zu verbessern.  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Netzwerktool mit nicht lokalisierten Filtern" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Netzwerkbereich** mit nicht lokalisierten Filtern  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Verschieben von Tools zwischen oberen und unteren Panels  

DevTools unterstützt jetzt das Verschieben von Tools zwischen dem oberen und unteren Bereich.  Passen Sie Ihre DevTools an, und verbessern Sie Ihre Produktivität, indem Sie eine beliebige Kombination von zwei Tools gleichzeitig anzeigen.  Zeigen Sie z. B. die **Elemente** und die **Sources-Tools** gleichzeitig an \(durch Verschieben des **Tools Sources** nach unten\).  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [#1075732][CR1075732].  

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

Das **Tool für die** Netzwerkkonsole hat nun die Kompatibilität mit den [Schemas Postman v2.1][PostmanSchemaJsonCollectionv210Index] und [OpenAPI v2][SwaggerSpecificationV2] verbessert.  Navigieren Sie zum Aktivieren des Experiments zu Aktivieren von [Experimentellen Features,][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Netzwerkkonsole aktivieren.**  Weitere Informationen zur Netzwerkkonsole **finden**Sie unter [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Dieses Experiment unterstützt nun die folgenden Aktionen.  

*   Speichern und exportieren Sie Sammlungen und Umgebungen.  
*   Bearbeiten und exportieren Sie Sätze von Umgebungsvariablen im **Netzwerkkonsolentool.**  
    
Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1093687][CR1093687].  

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
    
Die Features sind standardmäßig aktiviert.  Weitere Informationen zu den Features finden Sie unter [CSS-Raster][DevtoolsCssGrid].  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1047356][CR1047356].  Darüber hinaus arbeitet das Microsoft Edge DevTools-Team mit dem Chrome DevTools-Team und der Chromium-Community zusammen, um DevTools neue Features für flexbox-Tools hinzuzufügen.  Informationen zu Updates für flexbox-Tools im Open-Source-Projekt Chromium finden Sie unter Issue [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Layouttool mit Rastern" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Layouttool** mit Rastern  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Anpassen von Tastenkombinationen in den Einstellungen  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Sie können nun die Tastenkombination für alle Aktionen in devTools anpassen.  Seit Microsoft Edge, Version 84, können Sie zwischen Visual Studio **Code** und **DevTools (Standard)-Voreinstellungen** für Tastenkombinationen [wählen.][DevtoolsCustomizeShortcuts]  Ab Microsoft Edge, Version 87, **** können Sie das Experiment Tastenkombinationen-Editor aktivieren, um Tastenkombinationen [weiter anzupassen.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Navigieren Sie zum Aktivieren des Experiments zu Experimentelle Features [aktivieren,][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Tastenkombinationen-Editor aktivieren.**  Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter [Experimentelles Feature „Tastenkombinations-Editor aktivieren“][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Einführung in die Microsoft Edge Tools for Visual Studio Code extension  

Die **Elemente für Visual Studio Code** und Netzwerk für Visual Studio **Codeerweiterungen** werden nun mit den neuen Microsoft Edge Developer Tools for Visual Studio [Code-Erweiterung][VisualStudioCodeMarketplaceMsEdgedevtools] zusammengeführt.  Verwenden Sie die Microsoft Edge DevTools für die folgenden Aktivitäten, ohne Microsoft Visual Studio verlassen.  

*   Debuggen des DOM  
*   Bearbeiten von CSS  
*   Überprüfen des Netzwerkdatenverkehrs  

Starten Sie mit der Erweiterung Microsoft Edge, stellen Sie eine Verbindung mit einer vorhandenen Instanz des Browsers oder verwenden Sie einen kopflosen Browser direkt von Ihrem Editor aus.  Navigieren Sie zum Microsoft Edge Developer Tools for [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repository auf GitHub, um Mitwirken und Ablegen von Problemen mit Ihrem Feedback zu dieser Erweiterung zu beginnen.  

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
    
Weitere Informationen zum **WebAuthn-Feature** finden Sie unter Emulieren von Authentatoren und Debuggen [von WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Sie können Authentatoren emulieren und die [Webauthentifizierungs-API][GithubW3cWebauthn] mit dem neuen [WebAuthn-Tool][DevtoolsWebauthnIndex] debuggen.  Wählen Sie zum Öffnen des **WebAuthn-Tools** das Symbol **DevTools** anpassen \( \) > `...` Weitere **Tools**  >  **WebAuthn aus.**  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1034663][CR1034663].  

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

### <a name="elements-tool-updates"></a>Aktualisierungen des Elements-Tools  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Anzeigen des Seitenleistenbereichs "Berechnet" im Bereich Formatvorlagen  

Schaltet den **Bereich Berechnet** im Bereich **Formatvorlagen** um.  Der **Bereich Berechnet** im Bereich **Formatvorlagen** ist standardmäßig reduziert.  Um ihn umschalten zu können, wählen Sie die Schaltfläche aus.  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1073899][CR1073899].  

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

Um die angewendete CSS mit weniger Bildlauf anzuzeigen, gruppieren Sie die CSS-Eigenschaften nach Kategorien im **Bereich Berechnet.**  Sie können sich auch selektiv auf eine Reihe verwandter Eigenschaften konzentrieren, während Sie Ihre CSS überprüfen.  Wählen Sie **im Elementtool** ein Element aus.  Um die CSS-Eigenschaften \(oder ungroup\) zu gruppieren, aktivieren Sie das **Kontrollkästchen Gruppe.**  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1096230][CR1096230], [#1084673][CR1084673]und [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Gruppieren von CSS-Eigenschaften" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Gruppieren von CSS-Eigenschaften  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a>Leuchttürme 6.4 im Tool "Leuchttürme"  

Das **Tool "Leuchtturm"** wird jetzt mit "6.4" ausgeführt.  Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Veröffentlichung von "Leuchttürme".][GithubGoogleChromeLighthouseReleasesV641]  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>performance.mark()-Ereignisse im Abschnitt Timings  

Der **Abschnitt Timings einer** Aufzeichnung im Tool ["Leistung"][DevtoolsGuideChromiumEvaluatePerformanceReference] markiert nun `performance.mark()` Ereignisse.  Um dieses Feature auszuprobieren und die Leistung Ihres JavaScript-Codes zu messen, fügen Sie `performance.mark()` Dem Code Ereignisse hinzu.  Der folgende Codeausschnitt fügt z. B. Markierungen vor und nach einer Schleife hinzu, die mithilfe von Schritten von 7 von 0 auf `for` 1000 iteriert wird.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Öffnen Sie dann das [Tool Leistung,][DevtoolsGuideChromiumEvaluatePerformanceReference] und navigieren Sie zum **Abschnitt Timings,** um Ihren JavaScript-Code zu aufzeichnen.  Die `performance.mark()` hinzugefügten Ereignisse werden nun in der Aufzeichnung angezeigt.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance.mark-Ereignisse" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` Ereignisse  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Neue Ressourcentyp- und URL-Filter im Netzwerktool  

Verwenden Sie das neue `resource-type` und `url` Schlüsselwörter im **Netzwerktool,** um Netzwerkanforderungen zu filtern.  Verwenden Sie beispielsweise, `resource-type:image` um sich auf die Netzwerkanforderungen zu konzentrieren, die Bilder sind.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ressourcentypfilter" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   Ressourcentypfilter  
:::image-end:::  

Um speziellere Schlüsselwörter wie und zu `resource-type` `url` ermitteln, navigieren Sie zu [Filtern von Anforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties].  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1121141][CR1121141] und [#1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Updates der Frame-Detailansicht  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Anzeigen der COEP- und COOP-Berichterstellung an den Endpunkt  

Zeigen Sie die Endpunkte Cross-Origin Embedder Policy \(COEP\) und Cross-Origin Opener Policy \(COOP\) unter dem Abschnitt Sicherheit `reporting to` **& Isolation** an.  Die [Berichts-API][MdnReportingApi] definiert `Report-To` einen neuen HTTP-Header, mit dem Sie die Serverendpunkte für den Browser zum Senden von Warnungen und Fehlern angeben können.  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Die Berichterstellung an den Endpunkt" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   Der `reporting to` Endpunkt  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Anzeigen des NS-Berichtsmodus für COEP und COOP  

DevTools zeigt jetzt die `report-only` Bezeichnung für COEP und COOP an, die auf den Modus `report-only` festgelegt sind.  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Bezeichnung für den Nur-Bericht-Modus" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Die `report-only` Bezeichnung für den Modus  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Anzeigen und Beheben von Farbkontrastproblemen im CSS-Übersichtstool  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Das **Tool CSS Overview** zeigt nun eine Liste der Elemente auf Ihrer Seite an, die Probleme mit dem Farbkontrast haben.  Die folgende Demoseite enthält ein Beispiel für ein Farbkontrastproblem.  

[DEMO zu barrierefreien Farben (CSS Overview Accessible Colors)][GlitchCssOverviewAccessibleColorsDemo]  

Aktivieren Sie zum Aktivieren dieses Experiments unter **Einstellungen**Experimente das Kontrollkästchen  >  **** **CSS-Übersicht.**  Wenn Sie eine Liste der Elemente anzeigen möchten, bei der ein Farbkontrastproblem besteht, wählen Sie unter **Kontrastprobleme** **Text aus.**  Um das Element im **Elementtool zu** öffnen, wählen Sie ein Element in der Liste aus.  Zur Behebung von Kontrastproblemen stellen die Microsoft Edge DevTools [automatisch Farbvorschläge zur Verfügung.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu Problem [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Probleme mit geringem Farbkontrast" lightbox="../../media/2020/10/css-overview.msft.png":::
   Probleme mit geringem Farbkontrast  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Veralteter Eigenschaftenbereich im Elementtool – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features zum Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Barrierefreier Farbvorschlag im Bereich Formatvorlagen – Neues in DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulation: Unterstützung des dualen Bildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Tastenkombinationen-Editors – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des dualen Bildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Aktivieren der Netzwerkkonsole – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellauftragsanzeige – Experimentelle | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf zusammenklappbaren geräten und dualen Bildschirmen – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von Experimentellen Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle – Konsolen-API-| Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie nicht verwendeten JavaScript- und CSS-Code auf der Registerkarte Abdeckung in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Überprüfen der CSS Grid-| Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte Rendering – Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtern von Anforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emulieren von Authentifizierungsautoren und Debuggen von WebAuthn in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium-Fehler"
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von "| Chromium-Fehler"  
[CR1034663]: https://crbug.com/1034663 "Erstellen eines Front-Ends für die WebAuthn Testing-API | Chromium-Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium-Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützung des COOP/COEP-Debuggings in DevTools | Chromium-Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte "Berechnete Formatvorlage" wird im reaktionsschnellen Modus | Chromium-Fehler"  
[CR1075732]: https://crbug.com/1075732 "DevTools-Personalisierung – Wechselregisterkarten | Chromium-Fehler"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Verbessern Sie die Art und Weise, wie wir benutzerdefinierte CSS-Eigenschaften ((auch bekannt) präsentieren. CSS-Variablen) und deren Werte | Chromium-Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellen eines Tools zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium-Fehler"  
[CR1096230]: https://crbug.com/1096230 "Gruppieren von CSS-Eigenschaften nach Kategorien im Bereich "Computed Styles" | Chromium-Fehler"  
[CR1104188]: https://crbug.com/1104188 "Bei der Suche nach vollständigen URL-Adressen findet die Netzwerktoolsuche keine | Chromium-Fehler"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: Verbessern der Registerkarten für berechnete Formatvorlagen | Chromium-Fehler"  
[CR1120316]: https://crbug.com/1120316 "Hervorheben eines schlechten Kontrasts unter CSS Overview > Colors | Chromium-Bugs"  
[CR1121141]: https://crbug.com/1121141 "Filtern nach Ressourcentyp in Netzwerkprotokollen | Chromium-Fehler"  
[CR1121312]: https://crbug.com/1121312 "Einstellungen sollten aus dem Menü "Weitere Tools" entfernt | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Flexbox-| Chromium-Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Lokalisierung V2 | Chromium-Fehler"  

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
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2020/10/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
