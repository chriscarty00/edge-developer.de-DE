---
description: Wavy unterstreicht Codeprobleme im Elementtool, in der Zeitachse für Dienstarbeitsaktualisierungen und vieles mehr.
title: Neues in DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583459"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Neues in DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Wavy unterstreicht Codeprobleme und Verbesserungen im Elementtool  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.   In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen unter HTML in der **DOM-Ansicht** des **Elements-Tools** angezeigt.  Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung und so weiter hin.  Weitere Informationen zum Überprüfen und Bearbeiten von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

Führen Sie **eine** der folgenden Aktionen aus, um das Problem zu öffnen und mehr über das Problem und die Behebung zu erfahren.  

*   Wählen Sie `Shift` aus, halten Sie , und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.  
*   Führen Sie die folgenden Aktionen aus.  
    1.  Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.  
    1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
    1.  Wählen **Sie In Problemen anzeigen aus.**  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Wählen Sie den unterstrichenen Fehler im Elementtool aus." lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Wählen Sie den unterstrichenen Fehler im **Elementtool** aus.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Problemtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Anzeigen von Fehlerdetails im **Problemtool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Mehr über DevTools mit informativen QuickInfos erfahren  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche in DevTools zu erfahren.  Wählen Sie aus, um QuickInfos zu `Esc` deaktivieren.  Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.  

*   Wählen `Ctrl` + `Shift` + `H` Sie \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\).  
*   [Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` ein.  
*   Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > **Hilfe**Umschalten der  >  **DevTools-QuickInfos**.  

Wenn Sie außerdem das Experiment Fokusmodus und [DevTools-Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **DevTools Tooltips** \( \) am unteren Rand der Aktivitätsleiste umschalten. `?` ****  

Wenn Sie weitere Informationen zur Verwendung der DevTools anzeigen möchten, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Problemtools, um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Problemtools,** um weitere Details anzuzeigen.  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Zeitachse der Dienstarbeitsmitarbeiteraktualisierung  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

In Microsoft Edge Version 91 oder höher, wenn Sie Entwickler von Progressive Web App oder Service Worker sind, zeigen Sie den Updatelebenszyklus Ihrer Service Workers als Zeitachse im Anwendungstool **an.**  Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Dienstmitarbeiter in den folgenden Phasen verbringt.  

*   **Installieren**  
*   **Warte**  
*   **Aktivieren**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Aktualisierungszyklus für Ihren Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Überprüfen der **Zeitachse** im **Aktualisierungszyklus für** Ihren Service Worker  
:::image-end:::  

Weitere Informationen zum Lebenszyklus Ihrer Service Workers finden Sie unter [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].  Weitere Informationen zu Debuggingtools für Progressive Web Apps and Service Workers in den DevTools finden Sie unter [Service Worker improvements][DevtoolsServiceWorkerIndex].  Navigieren Sie zu Issue [1066604,][CR1066604]um die Echtzeitupdates für dieses Feature Chromium open-source-Projekt zu überprüfen.  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Wenn [Microsoft Edge Version 90][DevtoolsWhatsNew202102Devtools] oder früher ein nicht quadratisches Symbol enthält, wurde im Abschnitt Fehler und Warnungen für jedes nicht quadratische Symbol eine Warnung angezeigt, wenn das Web-App-Manifest Ihres PWA ein nicht quadratisches Symbol enthielt. ****  In Microsoft Edge Version 91 oder höher werden **** im **Abschnitt Manifest** im Anwendungstool keine Warnungen angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen.  Wenn Sie keine quadratischen Symbole bereitstellen, wird die folgende Meldung in einer Warnung angezeigt.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Um Fehler und Warnungen in Ihrem Web App-Manifest zu überprüfen, navigieren Sie zum **Anwendungstool,** und wählen Sie den **Abschnitt Manifest** aus.  Fehler und Warnungen werden unter der Überschrift **Fehler und Warnungen** aufgeführt.  Weitere Informationen zum Web App-Manifest finden Sie unter Verwenden des [Web-App-Manifests,][ProgressiveWebAppsWebappmanifests]um Ihre Progressive Web App in das Betriebssystem zu integrieren.  Navigieren Sie zum [PWABuilder][PwabuilderImagegenerator]Image Generator, um Symbole zu erstellen, die in Ihr Web-App-Manifest enthalten sind.  Navigieren Sie Chromium zu Problem [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>Lokalisierte DevTools werden jetzt in Chromium Browsern unterstützt  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

Ab Microsoft Edge [Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.  Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer eigenen Sprache, nicht nur in Englisch.  Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google -Leuchtturm-Team haben zusammengearbeitet, um die gleiche Erfahrung in allen Chromium Browsern zu bieten.  Weitere Informationen zur Verwendung von DevTools in Ihrer Sprache finden Sie unter [Ändern der DevTools-Spracheinstellungen.][DevtoolsCustomizeLocalization]  Weitere Informationen zur Zusammenarbeit an diesem Feature Chromium Open Source-Projekt finden Sie unter [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge Browser und DevTools auf Japanisch festgelegt  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Navigieren zu CSS-Variablen mithilfe der Tastatur  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

Ab Microsoft Edge [Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt **** der Bereich Formatvorlagen CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen zur Seite.  In Microsoft Edge Version 91 oder höher können Sie die Pfeiltasten verwenden, um problemlos zu CSS-Variablen zu navigieren.  Um die Definition im Bereich **Formatvorlagen** zu öffnen, zeigen Sie auf eine Variable, und wählen Sie dann `Enter` aus.  Weitere Informationen zu CSS-Variablen finden Sie unter [Verwenden benutzerdefinierter CSS-Eigenschaften (Variablen).][MdnDocsWebCssUsingCssCustomProperties]  Navigieren Sie Chromium zu Issue [1187735][CR1187735].  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable --theme-body-background, die im Bereich Formatvorlagen hervorgehoben ist" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Die `--theme-body-background` im Bereich Formatvorlagen hervorgehobene **CSS-Variable**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Probleme werden automatisch nach Schweregrad sortiert  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

Das **Tool Probleme** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit und so weiter. Basierend auf Ihrem Feedback werden Probleme jetzt automatisch nach Schweregrad sortiert.  In jeder Feedbackkategorie wird jedes **** als Fehler markierte Problem zuerst angezeigt, gefolgt von jedem Als Warnung gekennzeichneten Problem **und**anschließend jedem Problem, das als Tipp **gekennzeichnet ist.**  Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.  Weitere Informationen zum Überprüfen von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool Probleme zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   Das **Tool Probleme** zeigt sortierte Probleme nach Schweregrad an.  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

Die [Microsoft Edge Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterung, Version 1.1.7, stellt die DevTools aus Microsoft Edge Version [88 bereit.][DevtoolsWhatsNew202011Devtools]  Diese Erweiterung unterstützt jetzt ARM Geräte und hängt nicht mehr vom [Debugger][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] für Microsoft Edge ab.  Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.  

*   Die Zuverlässigkeit der Zielschließung wurde aktualisiert.  
*   Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie ziele debuggen, die erstellt oder zerstört werden.  
*   Es wurde ein neues kontextbezogenes Menü hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.  
*   Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.  
    
Um manuell auf Version 1.1.7 zu aktualisieren, navigieren Sie zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a>Visualisieren des CSS-Bildlauf-Snaps  

Sie können jetzt das Signal im Elementtool umschalten, `scroll-snap` um die CSS-Scroll-Snap-Ausrichtung zu überprüfen. ****  Wenn ein HTML-Element auf Ihrer Webseite darauf angewendet wurde, wird im Tool Elemente ein Signal `scroll-snap-type` `scroll-snap` **daneben** angezeigt.  Wählen Sie das Signal aus, um \(oder aus\) die Anzeige einer Bildlaufrastüberlagerung auf der Webseite zu aktivieren.  Navigieren Sie zum Überprüfen einer Beispielwebseite zu [Scroll Andocken Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].  Im Beispiel werden Punkte an Einrastkanten angezeigt.  Der Bildlaufport hat eine durchgehende Gliederung, während die Einrastelemente Bindestriche enthalten.  Der Bildlaufabstand wird grün gefüllt, während der Bildlaufrand in Orange gefüllt ist.  Navigieren Sie zu Issue [862450,][CR862450]um den Verlauf dieses Features im Chromium-Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS-Bildlauf-Snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   CSS-Bildlauf-Snap  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a>Neues Tool für den Speicherprüfungstool  

Verwenden Sie das neue **Tool Memory Inspector,** um einen `ArrayBuffer` In-JavaScript- und Wasm-Speicher zu überprüfen.  Öffnen Sie [die Demowebseite Memory in JS.][GlitchMemoryInspectorDemoJsHtml]  Öffnen Sie **im Tool** Quellen die `memory-write-wasm` Datei, und legen Sie einen Haltepunkt an der Zeile `0x03c` ein.  Aktualisieren Sie die Webseite.  Erweitern Sie **den Abschnitt Bereich** im Debuggerbereich.  Das neue Symbol wird neben dem **Pufferwert** angezeigt.  Wählen Sie es aus, um das neue **Speicherprüfungstool zu** öffnen.  

Weitere Informationen zum Debuggen im **Tool Sources** finden Sie unter Verwenden des [Debuggerbereichs zum Debuggen von JavaScript-Code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].  Navigieren Sie Chromium zu Issue [1166577][CR1166577].  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Tool "Memory Inspector"" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   **Speicherprüfungstool**  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a>Bereich "Neue Signaleinstellungen" im Tool Elemente  

Verwenden Sie jetzt die **Badge-Einstellungen** im **Elementtool,** um einzelne Signale \(oder aus\) zu aktivieren.  Verwenden Sie dieses Feature, um wichtige Badges anzupassen und sich auf wichtige Badges zu konzentrieren, während Sie Webseiten überprüfen.  Führen Sie die folgenden Aktionen aus, um den Bereich "Signaleinstellungen" am oberen Rand des **Elements-Tools** anzuzeigen.  

1.  Zeigen Sie auf ein beliebiges Element.  
1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Wählen **Sie Signaleinstellungen... aus.**  
    
Zum Anzeigen \(oder Ausblenden\) der Signalen wählen Sie \(oder entfernen\) das Kontrollkästchen neben dem Signalnamen aus.  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Bereich "Signaleinstellungen" im Elementtool" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   **Bereich "Signaleinstellungen"** im **Elementtool**  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a>Erweiterte Bildvorschau mit Seitenverhältnisinformationen  

Die Bildvorschau in den DevTools wurde erweitert, um weitere Informationen anzuzeigen, einschließlich der folgenden Details.  

*   Gerenderte Größe  
*   Gerenderte Seitenverhältnisse  
*   Systeminterne Größe  
*   Systeminternes Seitenverhältnis  
*   Dateigröße  
    
Die Informationen helfen Ihnen, Ihre Bilder besser zu verstehen und die Optimierung anzuwenden.  Die Informationen zum Bildaspektverhältnis sind auch im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.  

:::row:::
   :::column span="":::
      Im **Elementtool** zeigt die Bildvorschau nun weitere Informationen zum Bild an.  
   :::column-end:::
   :::column span="":::
      Darüber hinaus sind die Informationen zum Bildaspektverhältnis im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Bildvorschau mit Seitenverhältnisinformationen im Elementtool" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         Bildvorschau mit Seitenverhältnisinformationen im **Elementtool**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informationen zum Bild seitenverhältnis im Netzwerktool" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         Informationen zum Bild seitenverhältnis im **Netzwerktool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Sie zu Probleme [1149832][CR1149832] und [1170656][CR1149832] und [1170656][CR1170656]. Chromium  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a>Neue Optionen zum Konfigurieren von Inhaltscodierungen im Tool für Netzwerkbedingungen 

Wählen Sie im **Tool** Netzwerk die neue Schaltfläche **** Weitere **Netzwerkbedingungen...** neben dem Dropdownmenü Einschränkung aus, um das Tool **Netzwerkbedingungen zu** öffnen.  Führen Sie die folgenden Aktionen aus, um zu testen, ob Serverantworten für Browser korrekt codiert sind, die [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]oder eine andere Zukunft `Content-Encoding` nicht unterstützen.  

1.  Öffnen des **Tools für Netzwerkbedingungen**
1.  Navigieren Sie zu **Akzeptierte Inhaltscodierungen**. 
1.  Entfernen Sie das Kontrollkästchen neben `Content-Encoding` dem, das Sie testen möchten.  
    
Navigieren Sie Chromium zu Issue [1162042][CR1162042].  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Neue Weitere Netzwerkbedingungen... -Schaltfläche öffnet das Tool "Netzwerkbedingungen", um die Inhaltscodierung zu konfigurieren." lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   Neue **Schaltfläche Weitere Netzwerkbedingungen...** öffnet das **Tool "Netzwerkbedingungen"** zum Konfigurieren `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a>Verbesserungen des Formatbereichs  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a>Neue Verknüpfung zum Anzeigen des berechneten Werts im Bereich Formatvorlagen  

Führen Sie nun die folgenden Aktionen aus, um den berechneten CSS-Wert im Bereich **Formatvorlagen** anzuzeigen.  

1.  Zeigen Sie auf eine CSS-Eigenschaft.  
1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Wählen **Sie Berechneten Wert anzeigen aus.**  
    
Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium Open Source-Projekt zu Issue [1076198][CR1076198].  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Neue Verknüpfung zum Anzeigen des berechneten Werts" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   Neue Verknüpfung zum Anzeigen des berechneten Werts  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a>Unterstützung für das Schlüsselwort akzentuiert  

Die benutzeroberfläche für die **** automatische Vervollständigung des Bereichs Formatvorlagen erkennt nun das SCHLÜSSELWORT CSS, mit dem Sie die Akzentfarbe für vom Element generierte Benutzeroberflächensteuerelemente `accent-color` angeben können.  Beispiele für benutzeroberflächensteuerelemente, die von einem Element generiert werden, sind Kontrollkästchen oder Optionsfelder. Weitere Informationen zum Status der Chromium finden Sie unter [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].  Um dieses Feature zu aktivieren, navigieren Sie `edge://flags#enable-experimental-web-platform-features` zu, und legen Sie das Kontrollkästchen auf **Aktiviert .**  Navigieren Sie Chromium zu Issue [1092093][CR1092093].  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="schlüsselwort accent-color CSS" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` CSS-Schlüsselwort
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a>Anzeigen von Details zu blockierten Features in der Frame-Detailansicht  

Die Berechtigungsrichtlinie ist eine Webplattform-API, mit der eine Website die Verwendung von Browserfeatures in einem einzelnen Frame oder in einem eingebetteten Frame zulassen oder `iframe` blockieren kann. Weitere Informationen finden Sie unter [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].  Führen Sie die folgenden Aktionen aus, um die Details anzuzeigen, warum ein Feature blockiert ist.  

1.  Navigieren Sie zu [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].  
1.  Navigieren Sie zum **Anwendungstool.**  
1.  Wählen Sie einen Frame aus.  
1.  Navigieren Sie zum **Abschnitt Berechtigungsrichtlinie.**  
1.  Navigieren Sie zur **Disabled Features-Eigenschaft.**  
1.  Wählen Sie **Details anzeigen aus.**  
1.  Wählen Sie das Symbol neben jeder Richtlinie aus, um zu der Netzwerkanforderung zu navigieren, `iframe` die das Feature blockiert hat.  
    
Navigieren Sie Chromium zu Issue [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Blockierte Features in der Frame-Detailansicht" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   Blockierte Features in der Frame-Detailansicht  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a>Filtern von Experimenten in der Einstellung Experimente  

Suchen Sie mit dem neuen Experimentfilter schneller nach Experimenten.  Führen Sie beispielsweise die folgenden Aktionen aus, um neue Experimente für Codeprobleme zu aktivieren.
``

1.  Navigieren Sie zu **Einstellungen**  >  **Experiments**.  
1.  Navigieren Sie zum **Textfeld Filter.**  
1.  Geben Sie `issues` ein.  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtern von Experimenten in der Einstellung Experimente" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   Filtern von Experimenten in der **Einstellung Experimente**  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a>Spalte "New Vary Header" im Speicherbereich "Cache"  

Verwenden Sie die neue Spalte im Bereich `Vary Header` **Cache Storage,** um die [Werte der Http-Antwortheader][HttpwgSpecsRfc7231HtmlHeaderVary] variieren anzuzeigen.  Navigieren Sie Chromium zu Issue [1186049][CR1186049].  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Spalte "Kopfzeile variieren"" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   Spalte "Kopfzeile variieren"  
:::image-end:::  

### <a name="sources-tool-improvements"></a>Verbesserungen des Quellentools  

#### <a name="support-for-new-javascript-features"></a>Unterstützung für neue JavaScript-Features  

DevTools unterstützt jetzt die neue [Private-Markenprüfungen a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript-Sprachfeatures.  Das Feature für private Markenüberprüfungen erweitert den [In-Operator,][MdnDocsWebJavascriptReferenceOperatorsIn] um [Private Klassenfelder für][V8DevFeaturesClassFieldsPrivateClassFields] ein bestimmtes Objekt zu unterstützen.  Versuchen Sie es in den **Konsolen-** und **Quellentools.**  Führen Sie außerdem die folgenden Aktionen aus, um die privaten Felder zu überprüfen.  

1.  Navigieren Sie **zum Debuggerbereich.**  
1.  Navigieren Sie zum **Abschnitt Bereich.**  
    
Navigieren Sie zu Problem [11374,][CR11374]um den Verlauf dieses Features Chromium Open Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="JavaScript-Überprüfungen privater Marken" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   JavaScript-Überprüfungen privater Marken  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a>Erweiterte Unterstützung für das Debuggen von Haltepunkten  

Moderne JavaScript-Bundleer wie [Webpack][WebpackJsMain]und [Rollup unterstützen][RollupjsMain] die Codeteilung.  Weitere Informationen zum Teilen von Code finden Sie unter [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].  In Microsoft Edge Version 90 oder früher legen DevTools nur Haltepunkte in einem einzigen Bündel an.  In Microsoft Edge Version 91 oder höher legt DevTools haltepunkte in mehreren Bündeln richtig fest, wenn Sie eine freigegebene Komponente debuggen.  Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium-Open-Source-Projekt zu Probleme [1142705][CR1142705], [979000][CR979000]und [1180794][CR1180794].  

#### <a name="support-hover-preview-with-bracket-notation"></a>Unterstützen der Hovervorschau mit Klammern-Notation  

DevTools unterstützt jetzt die Hovervorschau für JavaScript-Memberausdrücke, die die `[]` Notation im **Tool Quellen** verwenden.  Navigieren Sie Chromium zu Issue [1178305][CR1178305].  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Unterstützen der Hovervorschau mit [] Notation" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   Unterstützen der Hovervorschau mit `[]` Notation  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a>Verbesserte Gliederung von HTML-Dateien  

DevTools bietet jetzt eine bessere Gliederungsunterstützung für `.html` Dateien.  Öffnen Sie **im Tool** Quellen die `.html` Datei.  Um \(oder aus\) die Codegliederung zu aktivieren, wählen Sie `Ctrl` + `Shift` + `O` unter Windows/Linux oder `Cmd` + `Shift` + `O` unter macOS aus.  In der folgenden Abbildung listet DevTools nun ordnungsgemäß alle Funktionen in der Gliederung auf.  Zuvor hat DevTools nur einige der Funktionen angezeigt.  Navigieren Sie zu Issues [761019][CR761019] und [1191465][CR1191465]. Chromium  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Verbesserte Gliederung von HTML-Dateien" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   Verbesserte Gliederung von HTML-Dateien  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a>Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging  

In Microsoft Edge Version 90 oder früher hat DevTools nur generische Wasm-Verweise in Fehlerstapelverfolgungen angezeigt.  In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt den Quellspeicherort unter Fehlerstapelverfolgungen für das Wasm-Debuggen an.  Um mehr über Fehlerstapelverfolgungen in der Konsole zu **erfahren,** navigieren Sie zu [Error][DevtoolsConsoleApiError].  

In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging an.  

:::row:::
   :::column span="":::
      In Microsoft Edge Version 90 und früher wird der Quellspeicherort nicht in den Fehlerstapelverfolgungen angezeigt.  Quellstandorte sind `dsquare` .  
   :::column-end:::
   :::column span="":::
      In Microsoft Edge Version 91 und höher wird der Quellspeicherort in der Fehlerstapelverfolgung angezeigt.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Frühere Fehlerstapelverfolgungen für das Wasm-Debuggen" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Sie Chromium zu Issue [1189161][CR1189161].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Verwenden der DevTools in anderen Sprachen – Neues in DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "CSS-Variablendefinitionen im Formatvorlagenbereich – Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Gruppentools im Fokusmodus – Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Öffnen Sie das Befehlsmenü - Befehle ausführen mit Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error – Konsolen-API-| Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Service Worker-Verbesserungen | Microsoft Docs"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code – Übersicht über das | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Service Worker-Lebenszyklus – Verwenden von Service Workers zum Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Verwenden Sie das Web-App-Manifest, um Ihre Progressive Web App in das Betriebssystem zu | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Feature: accent-color CSS property | Status der Chrome-Plattform"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget Accent Colors: die Accent-color-Eigenschaft – CSS Basic User Interface Module Level 4 | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR11374]: https://crbug.com/v8/11374 "Problem 11374: Implementieren der ergonomischen Markenüberprüfung für private Felder"  
[CR761019]: https://crbug.com/761019 "Problem 761019: &quot;Zum Symbol wechseln&quot; verpasst die erste Funktion und bevorzugt eine schlechtere Übereinstimmung, wenn sie alle typisiert zeichen enthält"  
[CR862450]: https://crbug.com/862450 "Problem 862450: [css-scroll-snap] Erwägen Sie das Hinzufügen der Devtools-Funktion für css-Bildlauf-Snap"  
[CR979000]: https://crbug.com/979000 "Problem 979000: Quellzuordnungen mit kollidierenden Quellenpfaden funktionieren nicht."  
[CR1066604]: https://crbug.com/1066604 "Problem 1066604: DevTools: Weitere Informationen zur Installation und Aktivierung von Ereignissen durch ServiceWorker | Chromium Fehler"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Issue 1076198: [Feature Request] Jump to computed property from `styles` tab"  
[CR1092093]: https://crbug.com/1092093 "Issue 1092093: Make form controls more color stylable by supporting the 'accent-color' CSS property"  
[CR1136655]: https://crbug.com/1136655 "Issue 1136655: Devtools: Localization V2 | Chromium Fehler"  
[CR1142705]: https://crbug.com/1142705 "Issue 1142705: Breakpoints stop working when 2 sourcemaps point to the same virtual file when using webpack"  
[CR1149832]: https://crbug.com/1149832 "Issue 1149832: Feature request: image preview should also show file size"  
[CR1158827]: https://crbug.com/1158827 "Issue 1158827: [Permissions Policy] Implement devtool support for permissions policy"  
[CR1162042]: https://crbug.com/1162042 "Issue 1162042: DevTools: support disabling gzip/brotli/jxl content-encoding"  
[CR1166577]: https://crbug.com/1166577 "Issue 1166577: ☂️ Linear Memory Inspector 1.0"  
[CR1170656]: https://crbug.com/1170656 "Issue 1170656: Show intrinsic aspect-ratio"  
[CR1178305]: "Problem 1178305: Debugger zeigt den Eigenschaftswert eines indizierten Elements nicht an, wenn es mit dem Mauszeiger bewegt https://crbug.com/1178305 wird"  
[CR1180794]: https://crbug.com/1180794 "Issue 1180794: Breakpoints don't work with Closure Compiler inlining optimization"  
[CR1185945]: https://crbug.com/1185945 "Issue 1185945: Manifest warning implies all icons must be square | Chromium Fehler"  
[CR1186049]: https://crbug.com/1186049 "Issue 1186049: Column for Vary: header in Cache Storage viewer"  
[CR1187735]: https://crbug.com/1187735 "Issue 1187735: Accessibility: MAS2.1.1: Keyboard: Unable to invoke the 'Var(..)' function using keyboard | Chromium Fehler"  
[CR1189161]: https://crbug.com/1189161 "Issue 1189161: `new Error` stacktraces are not transformed via DWARF"  
[CR1191465]: https://crbug.com/1191465 "Problem 1191465: STRG+Umschalt+O in HTML unterbrochen"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Arbeitsspeicher in JS | Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Arbeitsspeicher in Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scrollen Andocken demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "OOPIF Permissions Policy | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: Das Datenkomprimierungsprogramm | BETRIEBSSYSTEM &quot;GNU&quot;"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary - Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content | IETF HTTP Working Group"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Es stehen drei allgemeine Ansätze für die Codeteilung zur Verfügung: Einstiegspunkte: Manuell geteilter Code mithilfe der Eingabekonfiguration.  Duplizierung verhindern: Verwenden Sie Eintragsabhängigkeiten oder SplitChunksPlugin zum Deduplizieren und Teilen von Blöcken.  Dynamische Importe: Geteilter Code über Inlinefunktionsaufrufe innerhalb von Modulen. - Codeteilungs-| webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "in operator | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Private Marke überprüft a.k.a. #foo in obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-91) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
