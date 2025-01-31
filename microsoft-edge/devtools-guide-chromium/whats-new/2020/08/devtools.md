---
description: Anpassen von Tastenkombinationen Visual Studio Code, Emulieren von Surface Duo und Samsung -Galaxis-Fold, Verbesserungen der CSS-Rasterüberlagerung und vieles mehr.
title: Neues in DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564945"
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
# <a name="whats-new-in-devtools-microsoft-edge-86"></a>Neues in DevTools (Microsoft Edge 86)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Ankündigungen des Microsoft Edge DevTools-Teams  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a>Übereinstimmung von Tastenkombinationen in DevTools mit Visual Studio Code  

In Microsoft Edge 86 können Sie Tastenkombinationen in den DevTools mit Ihren Verknüpfungen in Microsoft Visual Studio [Code übereinstimmen.][VisualStudioCodeMain]  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code  
:::image-end:::  

Navigieren Sie zum Aktivieren dieses Features zu [Tastenkombinationen anpassen im Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Beispielsweise ist die Tastenkombination zum Anhalten oder Fortsetzen des Ausführens eines Skripts in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] `F5` .  Mit der **Voreinstellung DevTools (Default)** ist dieselbe Verknüpfung in devTools , aber wenn Sie die voreingestellte Visual Studio Code auswählen, ist diese Verknüpfung `F8` jetzt auch **** `F5` .  

Chromium Problem [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emulieren von Surface Duo und Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Sie können nun das Aussehen ihrer Website oder App auf zwei neuen Geräten testen: [Surface Duo][MicrosoftSurfaceDevicesDuo] und Samsung [Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.  

Um Ihre Website oder App für die Geräte mit dualem Bildschirm oder für die faltbare Geräte zu verbessern, verwenden Sie die folgenden Features bei der [Emulation des Geräts][DevtoolsDeviceModeIndex].  

*   [Aufteilung][DevtoolsDeviceModeDualScreenAndFoldables], das ist, wenn Ihre Website \(oder App\) auf beiden Bildschirmen angezeigt wird.
*   [Rendering der Naht][DualScreenIntroductionHowWorkSeam], das ist der Abstand zwischen den beiden Bildschirmen.
*   Aktivieren experimenteller Webplattform-APIs für den Zugriff auf das neue Feature für die [Medienbildschirmübergreifende][DualScreenWebCssMediaSpanning] CSS und [die JavaScript getWindowSegments-API][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Geräteemulation für Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Geräteemulation für Surface Duo  
:::image-end:::  

Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren experimenteller Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Emulation: Support dual screen mode**.  

Weitere Informationen zu diesem Feature finden Sie unter [Emulieren von Dualscreen-][DevtoolsDeviceModeDualScreenAndFoldables]und faltbaren Geräten in Microsoft Edge DevTools .  

Chromium Problem: [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Verbesserungen der CSS-Rasterüberlagerung und neue experimentelle Rasterfeatures  

Vielen Dank für das positive Feedback zu den verbesserten CSS-Rasterüberlagerungen.  Die CSS-Rasterüberlagerungen sind jetzt standardmäßig aktiviert und erfordern nicht, dass Sie ein Experiment aktivieren.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="CSS-Rasterüberlagerung für artikelelement" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   CSS-Rasterüberlagerung für `article` Element  
:::image-end:::  

> [!NOTE]
> Weitere Informationen zu Rasterüberlagerungen finden Sie unter [CSS-Rasterdebugfunktionen][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

Das Microsoft Edge DevTools-Team und das Chrome DevTools-Team arbeiten an weiteren Features zusammen.  Die neuen Features umfassen mehrere Überlagerungen, die dauerhaft und aus einem neuen **Layoutbereich** im Elementtool **konfigurierbar** sind.  

Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren von experimentellen Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben Neue CSS-Raster-Debuggingfeatures aktivieren (Konfigurationsoptionen sind im Seitenleistenbereich Layout in Elementen nach dem Neustart **verfügbar)**.  

Weitere Informationen zu diesem Feature finden Sie unter [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].  

Chromium Problem: [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>Aus der Konsole kopierte Tabelle behält die Formatierung bei  

In Microsoft Edge 85 oder früheren Versionen ist die Formatierung eines kopierten `console.table` Textes verloren gegangen.  Wenn Sie die Ausgabe aus der [Konsolen-API der Tabelle][DevtoolsConsoleApiTable] kopiert und eingeschrieben haben, wurde nur der Text der Tabelle beibehalten.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Table Console API output in Microsoft Edge 85 or earlier" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Konsolen-API-Ausgabe in Microsoft Edge 85 oder früher  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Konsolen-API-Ausgabe von Microsoft Edge 85 oder früher in Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

In Microsoft Edge 86 oder höher wird die Formatierung **** beibehalten, wenn Sie eine Tabelle aus der Konsole kopieren.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Table Console API Output in Microsoft Edge 86 oder höher" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Konsolen-API-Ausgabe in Microsoft Edge 86 oder höher  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Konsolen-API-Ausgabe aus Microsoft Edge 86 oder höher, die in Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium Problem: [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Source Order Viewer für einfachere Barrierefreiheitstests  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Die neue Barrierefreiheitshilfe zeigt die Reihenfolge der Elemente in der Quelle an.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Aktivieren der Quellreihenfolge anzeigen" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Aktivieren **der Quellreihenfolge anzeigen**  
:::image-end:::  

Mit diesem Feature können Sie leichter testen, wie Bildschirmlese- und Tastaturbenutzer Ihre Website oder App nutzen.  Bildschirmlesegeräte und Tastaturnavigation hängen davon ab, dass Inhalte im Quellcode Ihrer Website oder App in einer bestimmten Reihenfolge platziert werden, sodass sie der gerenderten Seite entspricht.  Der Quellauftragsanzeige zeigt potenzielle Unterschiede in der Reihenfolge zwischen der gerenderten Seite und dem Quellcode an.  

Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren experimenteller Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Source Order Viewer**aktivieren.  

Weitere Informationen zu diesem Experiment finden Sie unter [Source Order Viewer][DevtoolsExperimentalFeaturesSourceOrderViewer].  

Chromium Problem: [#1094406][CR1094406]  

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

### <a name="highlight-all-search-results-in-elements-tool"></a>Hervorheben aller Suchergebnisse im Elementtool  

In Microsoft Edge 84 und 85 wurde das erste Suchergebnis im **Elementtool** nicht hervorgehoben.  Die restlichen Suchergebnisse wurden korrekt hervorgehoben.  

Vielen Dank für Das Senden Ihres Feedbacks und die Verbesserung Chromium.  Ihr Feedback deckte Problem [#1103316][CR1103316] im Open-Source-Chromium auf.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Hervorgehobenes erstes Suchergebnis im Elementbereich in Microsoft Edge 84 oder höher" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Hervorgehobenes erstes Suchergebnis im **Elementtool** in Microsoft Edge 84 oder höher  
:::image-end:::  

Das Problem wurde jetzt in allen Versionen von Microsoft Edge.  

Chromium Problem: [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Tool für neue Medien  

DevTools zeigt jetzt Media Player-Informationen im Tool [Media][DevtoolsMediaPanelIndex] an.  

Führen Sie den folgenden Schritt aus, um das neue **Medientool** zu öffnen.  

1.  Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere **Tools**  >  **Media aus.**  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Tool für neue Medien" lightbox="../../media/2020/08/media-panel.msft.png":::
       Tool **für neue Medien**  
    :::image-end:::  

Vor dem neuen **Medientool** in DevTools befanden sich die Protokollierungs- und Debuginformationen zu Video playern unter der **Einstellung Zuletzt verwendeter Player.**  Navigieren Sie zum Öffnen der Einstellung Zuletzt **verwendeter Spieler,** `edge://media-internals` und wählen Sie das Tool **Spieler** aus.  

Zeigen Sie Liveinhalte an, und untersuchen Sie potenzielle Probleme schneller, einschließlich der folgenden Beispiele.  

*   Warum werden Frames verworfen?  
*   Warum interagiert JavaScript unerwartet mit dem Spieler?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Erfassen von Knoten-Screenshots mithilfe des Kontextmenüs des Elements-Tools  

Sie können jetzt Knoten-Screenshots mithilfe des Kontextmenüs im **Elementtool** erfassen.  

Um beispielsweise einen Screenshot des Inhaltsverzeichnisses zu erstellen, zeigen Sie auf das Element, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Screenshot des Knotens **erfassen aus.**  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Screenshots des Aufnahmeknotens" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Screenshots des Aufnahmeknotens  
:::image-end:::  

Chromium Problem: [#1100253][CR1100253]  

### <a name="issues-tool-updates"></a>Probleme mit Toolupdates  

Die Warnmeldungsleiste Probleme im **Konsolentool** wird jetzt durch eine reguläre Meldung ersetzt.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Probleme in Konsolennachrichten" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Probleme in Konsolennachrichten  
:::image-end:::  

Cookieprobleme von Drittanbietern werden jetzt standardmäßig im **Problemtool** ausgeblendet.  Aktivieren Sie das neue **Kontrollkästchen Cookieprobleme von** Drittanbietern enthalten, um die Probleme anzeigen zu können.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Kontrollkästchen für Cookieprobleme von Drittanbietern" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   Kontrollkästchen für Cookieprobleme von Drittanbietern  
:::image-end:::  

Chromium Probleme: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### <a name="emulate-missing-local-fonts"></a>Emulieren fehlender lokaler Schriftarten  

Öffnen Sie [das Renderingtool,][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] und verwenden Sie das neue Feature Lokale **Schriftarten** deaktivieren, um fehlende `local()` Quellen in Regeln zu `@font-face` emulieren.  

Wenn die Schriftart beispielsweise auf Ihrem Gerät installiert ist und von der Regel als Schriftart verwendet wird, verwendet Microsoft Edge die lokale Schriftartdatei `Rubik` `@font-face src` von Ihrem `local()` Gerät.  

Wenn **Lokale Schriftarten deaktivieren** aktiviert ist, ignoriert DevTools die Schriftarten und ruft jede Schriftart aus dem Netzwerk `local()` ab.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emulieren fehlender lokaler Schriftarten" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emulieren fehlender lokaler Schriftarten  
:::image-end:::  

Wenn Sie während der Entwicklung zwei unterschiedliche Kopien derselben Schriftart verwenden, z. B. die folgenden Beispiele.  

*   Eine lokale Schriftart für Ihre Designtools.  
*   Eine Webschriftart für Ihren Code.  

Verwenden **Sie Lokale Schriftarten deaktivieren,** um ihnen das Ausführen der folgenden Aufgaben zu erleichtern.  

*   Debuggen und Messen der Ladeleistung und Optimierung von Webschriftarten.  
*   Überprüfen Sie die Genauigkeit Ihrer `@font-face` CSS-Regeln.  
*   Ermitteln Sie Unterschiede zwischen lokalen Versionen, die auf Ihrem Gerät installiert sind, und einer Webschriftart.  

Chromium Problem: [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Emulieren inaktiver Benutzer  

Die [Idle Detection-API][WebDevIdleDetection] ermöglicht Es Entwicklern, inaktive Benutzer zu erkennen und auf Änderungen des Leerlaufzustands zu reagieren.  Sie können devTools nun verwenden, um Änderungen des Leerlaufzustands im Tool **Sensoren** sowohl für den Benutzerstatus als auch für den Bildschirmzustand zu emulieren, anstatt auf die Änderung des tatsächlichen Leerlaufzustands zu warten.  Sie können das Tool **"Sensors"** in der [Drawer öffnen.][DevtoolsCustomizeIndexDrawer]  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emulieren inaktiver Benutzer" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emulieren inaktiver Benutzer  
:::image-end:::  

Chromium Problem: [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Emulieren von prefers-reduced-data  

> [!NOTE]
> Navigieren Microsoft Edge 86, um dieses Feature zu aktivieren, zu und aktivieren Sie das Flag für Features der `edge://flags#enable-experimental-web-platform-features` **Experimentellen** Webplattform.  Die Emulationsoption wird nur angezeigt, wenn das Flag aktiviert ist.  

Die [Prefers-reduced-Data Media-Abfrage][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] erkennt Benutzerinhaltseinstellungen für reduzierte Daten.  Wenn diese Option ausgewählt ist, erhält der Benutzer alternative Seiteninhalte, die weniger Daten verwenden.  

Sie können jetzt DevTools verwenden, um die `prefers-reduced-data` Medienabfrage zu emulieren.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emulieren von prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emulieren von prefers-reduced-data  
:::image-end:::  

Chromium Problem: [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Unterstützung für neue JavaScript-Features  

DevTools haben jetzt die folgenden JavaScript-Sprachfeatures besser unterstützt.  

| JavaScript-Sprachfeature | Details |  
|:--- |:--- |  
| [Logische Zuweisungsoperatoren][V8FeaturesLogicalAssignment] | DevTools unterstützt jetzt die logische Zuordnung mit den neuen `&&=` Operatoren `||=` , und in `??=` den **Konsolen-** und **Quellentools.**  |  
| Ziemlich gedruckte [numerische Trennzeichen][V8FeaturesNumericSeparators] | DevTools druckt nun die numerischen Trennzeichen im Tool **Sources ordnungsgemäß.**  |  

Chromium: [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel&quot;></a>Leuchttürme 6.2 im Bereich &quot;Leuchttürme"  

Das **Tool "Leuchtturm"** wird jetzt mit "6.2" ausgeführt.  Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Veröffentlichung von "Leuchttürme".][GithubGooglechromeLighthouseV620]  

Chromium Problem: [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane&quot;></a>Veraltetes Auflisten anderer Ursprünge im Bereich &quot;Service Workers"  

DevTools stellt nun einen Link aus dem Bereich Service **workers** **\(** Anwendungstool > Dienstmitarbeiterbereich\) zur Verfügung, um die vollständige Liste der Servicemitarbeiter anderer Ursprünge anzuzeigen. ****  Navigieren Sie zu, um auf die Liste zu zugreifen, ohne die DevTools zu `edge://service-worker-internals/?devtools` öffnen.  

Zuvor hat DevTools eine Liste angezeigt, die unter dem Anwendungstool **>** **Dienstmitarbeiterbereich geschachtelt** ist.  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Link zu anderen Ursprüngen" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Link zu anderen Ursprüngen  
:::image-end:::  

Chromium Problem: [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Anzeigen der Abdeckungszusammenfassung für gefilterte Elemente  

DevTools berechnet nun neu und zeigt dynamisch eine Zusammenfassung der Abdeckungsinformationen an.  Die dynamische Anzeige wird ausgelöst, wenn Filter im [Coverage-Tool angewendet][DevtoolsCoverageIndex] werden.  Bevor das **Coverage-Tool** immer eine Zusammenfassung aller Abdeckungsinformationen angezeigt hat.  

In der ersten der folgenden Abbildungen wird zunächst die Zusammenfassung angezeigt, und in der zweiten der folgenden Abbildungen wird die Zusammenfassung angezeigt, nachdem die `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS-Filterung angewendet wurde.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Zusammenfassung der Abdeckung" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Zusammenfassung der Abdeckung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Abdeckungszusammenfassung für gefilterte Elemente" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Abdeckungszusammenfassung für gefilterte Elemente  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Chromium Problem: [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Neue Framedetailseansicht im Anwendungsbereich  

DevTools zeigt jetzt eine detaillierte Ansicht für jeden Frame an.  Um darauf zu zugreifen, wählen Sie im Anwendungstool unter dem Menü **Frames** einen **Frame** aus.  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Neue Detailansicht für einen Frame im Anwendungsbereich" lightbox="../../media/2020/08/frame-details.msft.png":::
   Neue Detailansicht für einen Frame im **Anwendungstool**  
:::image-end:::  

Chromium Problem: [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Framedetails für geöffnete Fenster  

Geöffnete Fenster und Popupfenster werden nun auch unter der Framestruktur angezeigt.  Die detaillierte Ansicht der geöffneten Fenster enthält zusätzliche Sicherheitsinformationen.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Neue Frame-Detailansicht für geöffnete Fenster" lightbox="../../media/2020/08/window-opener.msft.png":::
   Neue Frame-Detailansicht für geöffnete Fenster  
:::image-end:::  

Chromium Problem: [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Sicherheits- und Isolationsinformationen  

Sicherer Kontext, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]und [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] werden nun in den Framedetails angezeigt.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Sicherheits- und Isolationsinformationen" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Sicherheits- und Isolationsinformationen  
:::image-end:::  

In Zukunft planen das Microsoft Edge DevTools-Team und das Chrome DevTools-Team, den Framedetails weitere Sicherheitsinformationen hinzuzufügen.  

Chromium Problem: [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Updates für Elemente und Netzwerkpanels  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Barrierefreier Farbvorschlag im Bereich Formatvorlagen  

DevTools bietet nun Farbvorschläge für Text mit geringem Farbkontrast.  

Im folgenden Beispiel hat `h1` Text mit geringem Kontrast.  Um dies zu beheben, öffnen Sie die Farbauswahl der `color` Eigenschaft im **Bereich Formatvorlagen.**  Nachdem Sie den Abschnitt **Kontrastverhältnis** erweitert haben, stellt DevTools AA- und AAA-Farbvorschläge zur Verfügung.  Wählen Sie die vorgeschlagene Farbe aus, um die Farbe anzuwenden.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Farbauswahl schlägt AA- und AAA-Farbvorschläge vor" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Farbauswahl schlägt AA- und AAA-Farbvorschläge vor  
:::image-end:::  

Chromium Problem: [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Bereich Eigenschaften im Elementbereich neu festlegen  

Der **Bereich** Eigenschaften ist zurück.  In [84 wurde Microsoft Edge veraltet.][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]  Das Microsoft Edge DevTools-Team und das Chrome DevTools-Team planen Verbesserungen für die Überprüfung der Eigenschaften von Elementen.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Eigenschaftenbereich im Elementbereich" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Eigenschaftenbereich** im **Elementtool**  
:::image-end:::  

Chromium Problem:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a>Automatisches Kompletieren benutzerdefinierter Schriftarten im Bereich Formatvorlagen  

Importierte Schriftartengesichter werden nun der Liste der automatischen CSS-Vervollständigung hinzugefügt, wenn die Eigenschaft im `font-family` Bereich **Formatvorlagen bearbeitet** wird.  

Wenn beispielsweise eine benutzerdefinierte Schriftart auf dem lokalen Computer installiert ist, wird `monospace` sie in der Css-Abschlussliste angezeigt.  In früheren Versionen von Microsoft Edge wurde die Schriftart nicht angezeigt.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Automatisches Kompletieren benutzerdefinierter Schriftarten" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Automatisches Kompletieren benutzerdefinierter Schriftarten  
:::image-end:::  

Chromium Problem: [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Konsistenter Ressourcentyp im Netzwerkbereich anzeigen  

DevTools zeigen jetzt konsistent denselben Ressourcentyp wie die ursprüngliche Netzwerkanforderung an und fügen den Wert der Spalte Type an, wenn die Umleitung `/ Redirect` \(HTTP-Statuscode 302\) erfolgt. ****  

Zuvor hat DevTools den Typ in manchmal `Other` geändert.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Umleitungsressourcentyp anzeigen" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Umleitungsressourcentyp anzeigen  
:::image-end:::  

Chromium Problem: [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Löschen von Schaltflächen in den Elementen und Netzwerktools  

Die folgenden Textfelder verfügen jetzt über **Schaltflächen löschen.**  

*   Die Filtertextfelder im **Bereich Formatvorlagen** und **im Netzwerktool.**  
*   Das Textfeld DOM-Suche im **Elementtool.**  

Wählen Sie die **Schaltfläche Löschen** aus, um eingegebenen Text zu entfernen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Löschen von Schaltflächen in den Elementen-Panels" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Löschen von Schaltflächen in den **Elements-Tools**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Löschen von Schaltflächen in den Netzwerkpanels" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Löschen von Schaltflächen in den **Netzwerktools**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium Problem: [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie sich auf Windows oder macOS befinden, sollten Sie die Microsoft Edge Vorschaukanäle [als][MicrosoftEdgePreviewChannels] Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Veralteter Eigenschaftenbereich im Elementbereich – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features zum Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "Tabelle – Konsolen-API-| Microsoft Docs"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Suchen Sie nicht verwendeten JavaScript- und CSS-Code auf der Registerkarte Abdeckung in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Drawer – Anpassen Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analysieren der Renderingleistung mit dem Renderingtool – Leistungsanalysereferenz | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer "Source Order Viewer - Experimental features | Microsoft Docs"
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Geräten mit dualem Bildschirm | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Feature „CSS-Medienbildschirmaufteilung“ für die Erkennung von dualem Bildschirm | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die API „getWindowSegments JavaScript“ für Geräte mit dualem Bildschirm | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Tastenkombinationen für Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools, Twitter-Konto"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium Fehler"
[CR384968]: https://crbug.com/384968 "Option zum Ignorieren von lokalen()Schriftarten | Chromium Fehler"  
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von &quot;| Chromium Fehler"  
[CR807440]: https://crbug.com/807440 "Chrome wird mit einer großen Anzahl von SWs | Chromium Fehler"  
[CR997694]: https://crbug.com/997694 "XHR-Anforderungen mit dem Status 302 werden im Netzwerkbereich nicht unter dem Filter \"xhr\" | Chromium Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützung des COOP/COEP-Debuggings in DevTools | Chromium Fehler"  
[CR1054281]: https://crbug.com/1054281 "Featureanforderung: DevTools sollte zusammenklappbare und duale Bildschirmgeräte emulieren, die | Chromium Fehler"  
[CR1067184]: https://crbug.com/1067184 "Featureanforderung: Filterschaltfläche löschen im Netzwerk & Elemente -> Formatfiltereingaben | Chromium Fehler"  
[CR1068116]: https://crbug.com/1068116 "☂ Problembereich | Chromium Fehler"  
[CR1080569]: https://crbug.com/1080569 "acorn unterstützt keine logischen Zuweisungsoperatoren | Chromium Fehler"  
[CR1080589]: https://crbug.com/1080589 "Klassifizieren von Problemen nach Drittanbieter-/erst-| Chromium Fehler"  
[CR1086817]: https://crbug.com/1086817 "acorn unterstützt keine numerischen Trennzeichen | Chromium Fehler"  
[CR1090802]: https://crbug.com/1090802 "Simulieren von Änderungen des Leerlaufzustands aus der Leerlauferkennungs-API | Chromium Fehler"  
[CR1093227]: https://crbug.com/1093227 "DevTools: Schlagen Sie die am nächsten barrierefreien | Chromium Fehler"  
[CR1093247]: https://crbug.com/1093247 "Anzeigen von Informationen zu Frames im Anwendungsbereich | Chromium Fehler"  
[CR1094406]: https://crbug.com/1094406 "Entwickler möchten eine Quellauftragsanzeige für AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: Unterstützt die Emulierung der Features &quot;prefers-reduced-data media&quot; | Chromium Fehler"  
[CR1096481]: https://crbug.com/1096481 "Probleme bei der Bannerplatzierung | Chromium Fehler"  
[CR1100253]: https://crbug.com/1100253 "Hinzufügen einer Verknüpfung mit einem Screenshotknoten im Elementkontextmenü | Chromium Fehler"  
[CR1103316]: https://crbug.com/1103316 "Elementesuche wird nicht aufgelöstNode (Hervorhebungstext usw.) im ersten Suchergebnis | Chromium Fehler"  
[CR1103854]: https://crbug.com/1103854 "Entverschleieren von X-Client-Data-Werten in Entwicklertools | Chromium Fehler"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Hinzufügen importierter Schriftarten zur automatischen Schriftfamilienvervollständigung https://crbug.com/1106221 im Formatvorlagenbereich | Chromium Fehler"  
[CR1107766]: "Anzeigen von Informationen zu Frames, die von https://crbug.com/1107766 'window.open()' in der Framestruktur generiert | Chromium Fehler"  
[CR1115011]: "Beim Kopieren einer Tabelle aus der Konsole wird die Struktur der Tabelle nicht | https://crbug.com/1115011 Chromium Fehler"  
[CR1116085]: "Rufen Sie den https://crbug.com/1116085 Inspektor für DevTools-Eigenschaften | Chromium Fehler"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data – Media Queries Level 5 | W3C CSS Working Group Editor Drafts"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 – GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Protokollpuffer | Google Developers"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Logische Zuweisung | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Numerische Trennzeichen | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "So wird Ihre Website mithilfe von COOP und COEP isoliert\"Cross-Origin\" | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Erkennen von inaktiven Benutzern mit dem Leerlauferkennungs-API-| web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Vermeiden sie nicht zusammengesetzte Animationen | web.dev"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-86) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
