---
description: Debugunterstützung für CSS Flexbox, Leistungskopfanzeige auf der Webseite, Probleme mit Toolupdates und mehr
title: Neues in DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408509"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Neues in DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Gruppieren von Tools im Fokusmodus  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

Der Fokusmodus ist eine experimentelle Schnittstelle, mit der Sie verschiedene Tools basierend auf Ihren eigenen Debuggingszenarien gruppieren können.  Die neue **Aktivitätsleiste,** die auf der linken Seite angezeigt wird, enthält vordefinierte Toolgruppen wie **Layout** und **Debugging.**  Schließen Sie zum Anpassen jeder Toolgruppe Tools mit dem Symbol Schließen **\(** \) oder fügen Sie mit dem Symbol Weitere Tools \( \) neue Tools `X` **** `+` hinzu.  

Navigieren Sie zum Aktivieren [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] des Experiments zu Aktivieren experimenteller Features, und wählen Sie die Kontrollkästchen neben Fokusmodus und **DevTools-Toolinfos** und Registerkartenmenüs Aktivieren + aus, um weitere Tools **zu öffnen.**  Weitere Informationen zu diesem Feature oder zum Kommentieren mit Fragen und Ideen finden Sie unter [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Anzeigen der Aktivitätsleiste" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Anzeigen der **Aktivitätsleiste**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Informationen zu DevTools mit informativen QuickInfos  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche zu erfahren.  Wählen Sie das Symbol Hilfe \( \) am unteren Rand der Aktivitätsleiste aus, um `?` quickInfos **** in den DevTools umschalten zu können.  Wenn QuickInfos verfügbar sind, zeigen Sie auf jeden umrissenen Bereich von DevTools, um mehr über die Verwendung des Tools zu erfahren.  Navigieren Sie zum Aktivieren [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] des Experiments zu Aktivieren experimenteller Features, und wählen Sie die Kontrollkästchen neben Fokusmodus und **DevTools-Toolinfos** und Registerkartenmenüs Aktivieren + aus, um weitere Tools **zu öffnen.**  Weitere Informationen zu diesem Feature oder zum Kommentieren mit Fragen und Ideen finden Sie unter [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Auswählen des Hilfesymbols (?) in der Aktivitätsleiste zum Anzeigen von QuickInfos" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Wählen Sie das Symbol Hilfe \( `?` \) in der **Aktivitätsleiste aus,** um QuickInfos anzeigen zu können.  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Anpassen von Tastenkombinationen in den Einstellungen  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Sie können jetzt die Tastenkombination für jede Aktion in den DevTools anpassen.  Führen Sie die folgenden Aktionen aus, um eine Tastenkombination zu bearbeiten.  

1.  Öffnen Sie die DevTools, und wählen Sie dann **Einstellungen**  >  **Verknüpfungen aus.**  
1.  Wählen Sie die Aktion aus, die Sie anpassen möchten.  
1.  Wählen Sie bearbeiten \(![Bearbeiten des Tastenkombinationssymbols](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) symbol.  
1.  Wählen Sie die Schlüssel aus, die Sie an die Aktion binden möchten.  
1.  Aktivieren Sie das Häkchen \(![Symbol für die Tastenkombination "Häkchen".](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) symbol.  
    
Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter Anpassen von Tastenkombinationen [in den Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Anpassen von Tastenkombinationen in den DevTools-Einstellungen für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Anpassen von Tastenkombinationen in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools für Visual Studio Codeerweiterungsupdate 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

Die [Microsoft Edge Developer Tools für Visual Studio Codeerweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Version 1.1.4 für Microsoft Visual Studio Code zeigt jetzt neben jeder DevTools-Instanz einen Favicon an.  Konsolennachrichten von Microsoft Edge werden jetzt in der **DevTools-Konsole** unter **Ausgabe** von Microsoft Visual Studio angezeigt.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.4 zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Sie können Probleme datein und zur Erweiterung im [vscode-edge-devtools-GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] beitragen.  

:::row:::
   :::column span="":::
      In der folgenden Abbildung werden Nachrichten von einer Beispielwebseite angezeigt, die im **Konsolentool** in Microsoft Edge protokolliert wurde.  
   :::column-end:::
   :::column span="":::
      In der folgenden Abbildung werden die gleichen Nachrichten von der Beispielwebseite angezeigt, die in der **DevTools-Konsole** unter **Ausgabe** von Microsoft Visual Studio ist.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Anzeigen derselben Meldung in der DevTools-Konsole unter Ausgabe von Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Anzeigen derselben Meldung in der DevTools-Konsole unter Ausgabe von Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Verbesserte CSS-Flexboxbearbeitung mit visuellem Flexbox-Editor und mehreren Überlagerungen  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools verfügt jetzt über dedizierte CSS-Flexbox-Debuggingtools.  Wenn die `display: flex` Oder `display: inline-flex` -CSS-Formatvorlage auf ein HTML-Element angewendet wird, wird neben diesem Element im Tool Elemente ein `flex` **Symbol** angezeigt.  Zum Anzeigen \(oder Ausblenden\) einer Flexüberlagerung auf der Webseite wählen Sie das `flex` Symbol aus.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1166710][CR1166710] und [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Navigieren Sie zum Öffnen des **** **Flexbox-Editors** zum Bereich `display: flex` Formatvorlagen, und wählen Sie das neue Symbol neben dem Format oder `display: inline-flex` aus.  Der **Flexbox-Editor** bietet eine schnelle Möglichkeit zum Bearbeiten der flexbox-Eigenschaften.  
   :::column-end:::
   :::column span="":::
      Darüber hinaus werden im **Abschnitt Flexbox** im **Layoutbereich** alle flexbox-Elemente auf der Webseite angezeigt.  Sie können die Überlagerung der einzelnen Elemente umschalten.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="CSS-Flexbox-Debuggingtools" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         CSS-Flexbox-Debuggingtools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Abschnitt "Flexbox" im Layoutbereich" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Abschnitt "Flexbox"** im **Layoutbereich**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Verbesserungen bei der Tastaturnavigation für Netzwerkanforderungen  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Zuvor waren Sie nicht in der Lage, die Kette von Anforderungen mithilfe der Pfeiltasten auf der Tastatur im **Bereich Initiator** zu erweitern oder zu reduzieren, im Gegensatz zum DOM im **Elementtool.**  Wenn eine Netzwerkanforderung im **** Netzwerktool ausgewählt ist, zeigt der **Bereich Initiator** die Kette der Anforderungen an, die die aktuell ausgewählte Anforderung initiiert haben.  

In Microsoft Edge, Version 90, können Sie die Kette von Anforderungen mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** erweitern oder reduzieren.  Die fokussierte Netzwerkanforderung in der Kette wird nun ebenfalls hervorgehoben.  Weitere Informationen zu Initiatoren im **Netzwerktool** finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1158276][CR1158276] und [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Wählen Sie eine Netzwerkanforderung aus, und wählen Sie den Bereich Initiator aus." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Wählen Sie eine Netzwerkanforderung aus, und wählen Sie den **Bereich Initiator** aus.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Erweitern oder Reduzieren der Anforderungsinitiatorkette und Folgen der hervorgehobenen Zeile" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Erweitern oder Reduzieren der Anforderungsinitiatorkette und Folgen der hervorgehobenen Zeile  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>Filtern in der Konsole ist konsistenter  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Während Sie mit der [Konsolenseite filtern,][DevtoolsConsoleReferenceOpenConsoleSidebar]sind die Filter im Dropdownmenü [Protokollebenen][DevtoolsConsoleReferenceFilterByLogLevel] nicht verfügbar.  Zuvor wurde das **Dropdown "Protokollebenen"** hervorgehoben, wenn Sie mit dem Mauszeiger auf sie zeigen, auch wenn ein Filter aus der **Konsolen-Seitenleiste** ausgewählt wurde.  In Microsoft Edge, Version 90, wird das Dropdown **"Protokollebenen"** nicht mehr hervorgehoben, wenn Sie den Mauszeiger auf sie zeigen, während ein Filter aus der **Konsolenseite ausgewählt** wird.  Weitere Informationen zum Filtern in der **Konsole finden**Sie unter Filtern [von Nachrichten][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Wenn Sie zuvor die Konsolen-Seitenleiste öffnen und auf Standardebenen zeigen, wurde sie hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Wenn Sie zuvor die Konsolen-Seitenleiste öffnen und auf Standardebenen zeigen, **wurde** sie hervorgehoben. ****  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Wenn Sie ab Microsoft Edge 90 die Konsolen-Seitenleiste auswählen und auf Standardebenen zeigen, wird dies nicht hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         Wenn Sie ab Microsoft Edge 90 die Konsolen-Seitenleiste auswählen und auf Standardebenen **zeigen,** wird dies nicht hervorgehoben. ****  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>Die Konsole entweicht jetzt doppelten Anführungszeichen  

Zuvor hat die **Konsole** keine gültigen doppelten Anführungszeichen \( `"` \) in JavaScript-Zeichenfolgen ausgegeben.  Ab Microsoft Edge, Version 90, gibt die **Konsole** JavaScript-Zeichenfolgen unter Verwendung von Escape-Doppelanführungszeichen \( `"` \) aus.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Die Konsole gibt JavaScript-Zeichenfolgen mithilfe von Escapezeichen für doppelte Anführungszeichen (&#0022;) aus." lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   Die **Konsole gibt** JavaScript-Zeichenfolgen unter Verwendung von Escape-Doppelanführungszeichen \( `"` \) aus.  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emulieren des CSS-Farbskala-Medienfeatures  

Die [Farbskala-Medienabfrage][ChromestatusFeature5354410980933632] emuliert den ungefähren Farbbereich, der vom Browser und dem getesteten Gerät unterstützt wird.  Das Dropdown unter **Emulieren der Farbskala** des CSS-Medienfeatures enthält Farbräume, die DevTools emulieren kann.  Um beispielsweise eine Medienabfrage auszulösen, wählen Sie im `color-gamut: p3` **Dropdownmenü Farbskala: p3** aus.  

Führen Sie die folgenden Aktionen aus, um das CSS-Farb gamut-Medienfeature zu emulieren.  

1.  Öffnen Sie das [Befehlsmenü][DevtoolsCommandMenuIndex].  
1.  Geben Sie `Rendering` ein.  
1.  Führen Sie den **Befehl Rendering anzeigen** aus.  
1.  Navigieren Sie **zu Css-Medienfeature-Farbskala emulieren,** und wählen Sie eine Option aus.  

Um mehr über das Feature zu `color-gamut` erfahren, navigieren Sie zu [Farbanzeigequalität: das Feature "Farbskala".][CsswgDraftsMediaqueries4ColorGamut]  Navigieren Sie zu Issue [1073887,][CR1073887]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emulieren des CSS-Farbskala-Medienfeatures" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emulieren des CSS-Farbskala-Medienfeatures  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Verbesserte Progressive Web Apps-Tools  

#### <a name="pwa-installability-warning-in-the-console"></a>Warnung zur Installation von PWA in der Konsole  

Die **Konsole** zeigt nun eine ausführlichere Warnung zur Installation von [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] mit einem Link zur Verbesserung der [Progressive Web App-Offlineunterstützungserkennung an.][ChromeDeveloperBlogImprovedPwaOfflineDetection]  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Warnung zur Installation von PWA im Konsolentool" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Warnung zur Installation von PWA im **Konsolentool**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Warnung zur Länge der PWA-Beschreibung im Manifestbereich

Im **Manifestbereich** wird nun eine Warnmeldung angezeigt, wenn die Manifestbeschreibung 324 Zeichen überschreitet.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Warnung zum Kürzen der PWA-Beschreibung" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Warnung zum Kürzen der PWA-Beschreibung  
:::image-end:::  

Navigieren Sie zu Probleme [965802,][CR965802] [1146450][CR1146450]und [1169689,][CR1169689]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Neue Spalte "Remote address space" im Netzwerktool  

<!-- does not work in canary 90.0.813.0 -->  
In der neuen **Spalte Remoteadressenraum** wird der Netzwerk-IP-Adressraum jeder Netzwerkressource angezeigt.  Führen Sie die folgenden Aktionen aus, um die neue Spalte Remoteadressenraum anzeigen zu können.  

1.  Navigieren Sie zum **Netzwerktool.**  
1.  Zeigen Sie in der Tabelle Anforderungen auf die Kopfzeile, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  Informationen zum Hinzufügen oder Entfernen von Spalten aus der Tabelle Anforderungen finden Sie unter [Hinzufügen oder Entfernen von Spalten.][DevtoolsNetworkReferenceAddRemoveColumns]  
1.  Wählen **Sie Remoteadressenbereich aus.**  
    
In der Tabelle Anforderungen wird nun eine neue Spalte mit der Kopfzeile **"Remote address Space" angezeigt.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Wählen Sie im Kontextmenü Remoteadressenbereich aus." lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         Wählen Sie im Kontextmenü den **Remoteadressenbereich aus.**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="In der Tabelle Anforderungen wird nun die Spalte Remoteadressenbereich angezeigt." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         In der Tabelle Anforderungen wird nun die **Spalte Remoteadressenbereich** angezeigt. :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Anzeigen zulässiger und nicht zulässiger Features in der Frame-Detailansicht  

Die Frame-Detailansicht zeigt nun eine Liste der zulässigen und nicht zulässigen Browserfeatures an, die durch die [Berechtigungsrichtlinie gesteuert werden.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]  Die Berechtigungsrichtlinie ist eine Webplattform-API, mit der eine Webseite die Verwendung von Browserfeatures in einem einzelnen Frame oder in iframes ermöglicht wird, die sie einbettet.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Zugelassene und nicht zulässige Features basierend auf der Berechtigungsrichtlinie" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Zugelassene und nicht zulässige Features basierend auf der Berechtigungsrichtlinie  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Neue Spalte SameParty im Bereich Cookies  

Im **Bereich Cookies** im **Anwendungstool** wird nun das `SameParty` Attribut für jedes Cookie angezeigt.  Das Attribut ist ein neues boolesches Attribut, das angibt, ob ein Cookie in Anforderungen an Ursprünge derselben `SameParty` [First-Party-Sets enthalten ist.][GithubPrivacycgFirstPartySets]  Navigieren Sie zu Issue [1161427,][CR1161427]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Spalte SameParty im Bereich Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Spalte SameParty** im **Bereich Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>Die fn.displayName-Eigenschaft im Konsolentool ist nun veraltet.  

Zuvor konnten Sie mit der Eigenschaft Debugnamen für Funktionen steuern, die in und `fn.displayName` `error.stack` in DevTools-Stapelverfolgungen angezeigt werden können.  Ab Microsoft Edge, Version 90, ist die Eigenschaft veraltet `fn.displayName` und wird durch die Eigenschaft `fn.name` ersetzt.  Verwenden Sie die `Object.defineProperty` Standardmethode, um die Eigenschaft `fn.name` zu definieren.  Um mehr über zu `fn.name` erfahren, navigieren Sie [zu Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Navigieren Sie zu Issue [1177685,][CR1177685]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Ein Beispiel für die fn.name-Eigenschaft zum Steuern von Debugnamen für Funktionen" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Ein Beispiel für die `fn.name` Eigenschaft zum Steuern von Debugnamen für Funktionen  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Vollständige Barrierefreiheitsstrukturansicht im Elementtool  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Dieses Experiment bietet eine **vollständige Barrierefreiheitsstrukturansicht** im **Elementtool.**  Der [Bereich Barrierefreiheit][DevtoolsAccessibilityReferenceTheAccessibilityPane] bietet eine teilweise Barrierefreiheitsstrukturansicht, in der die direkte Vorgängerkette vom Stammknoten zum überprüften Knoten angezeigt wird.  
Nachdem Sie dieses Experiment aktivieren und die DevTools neu laden, wählen Sie eine der folgenden Schaltflächen aus, um die Anzeige im Elementtool für alle Elemente auf der Webseite zu wechseln.  

*   Wählen Sie zum Anzeigen der vollständigen Barrierefreiheitsstrukturansicht die **Ansicht Barrierefreiheitsstruktur wechseln aus.**  
*   Wählen Sie zum Anzeigen der DOM-Strukturansicht die **Ansicht Wechseln zu DOM-Struktur aus.**  
    
Um das Experiment zu aktivieren, navigieren Sie zu Experimentelle Features [aktivieren,][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben Vollständige Barrierefreiheitsstrukturansicht aktivieren **im Bereich Elemente.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Anzeigen der DOM-Strukturansicht" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Anzeigen der **DOM-Ansicht**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Anzeigen der vollständigen Barrierefreiheitsstrukturansicht" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Anzeigen der **Vollständigen Barrierefreiheitsstrukturansicht**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Der Bereich Barrierefreiheit – Barrierefreiheitsreferenz | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtern von Nachrichten – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Öffnen Sie die Konsolenseite – Konsolenreferenz | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Aktivieren sie + Schaltflächenmenüs, um weitere Tools zu öffnen – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Hinzufügen oder Entfernen von Spalten – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Übersicht über progressive Web Apps unter Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterung Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Verbessern der Erkennung von Progressive Web App-Offlineunterstützung | Chrome Developers"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Farbskala-Medienabfragen | Status der Chrome-Plattform"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR887173]: https://crbug.com/887173 "Issue 887173: DevTools: Full Accessibility Tree Inspection | Chromium-Fehler"  
[CR965802]: https://crbug.com/965802 "Problem 965802: Implementieren einer genaueren Erkennung von Offlinefunktionen | Chromium-Fehler"  
[CR1073887]: https://crbug.com/1073887 "Issue 1073887: DevTools: @media (color-gamut: ...) colorspace emulation | Chromium-Fehler"  
[CR1128885]: https://crbug.com/1128885 "Problem 1128885: DevTools-Unterstützung für CORS-RFC1918 | Chromium-Fehler"  
[CR1146450]: https://crbug.com/1146450 "Issue 1146450: [Android] Implement bottom sheet installs | Chromium-Fehler"  
[CR1158276]: https://crbug.com/1158276 "Problem 1158276: Bereich "Initiatorkette anfordern" kann nicht mithilfe von Pfeiltasten im Abschnitt "Netzwerk" von DevTools erweitert/| Chromium-Fehler"  
[CR1158827]: https://crbug.com/1158827 "Issue 1158827: [Permissions Policy] Implement devtool support for permissions policy | Chromium-Fehler"  
[CR1160637]: https://crbug.com/1160637 "Problem 1160637: Der Fokus auf "Anforderungsinitiatorkette" wird im Abschnitt "Netzwerk" des Fensters "Dev Tools" als unvollständig | Chromium-Bugs"  
[CR1161427]: https://crbug.com/1161427 "Problem 1161427: &#9730; Support SameParty cookie attribute debugging in DevTools | Chromium-Fehler"  
[CR1166710]: https://crbug.com/1166710 "Problem 1166710: Aktivieren des Flexboxtool-Experiments standardmäßig | Chromium-Fehler"  
[CR1169689]: https://crbug.com/1169689 "Problem 1169689: Das untere Blatt für die PWA-Installation sollte keine Kategorien | Chromium-Fehler"  
[CR1175699]: https://crbug.com/1175699 "Problem 1175699: Flexbox-Editor | Chromium-Fehler"  
[CR1177685]: https://crbug.com/1177685 "Problem 1177685: Entfernen von nicht standardmäßigen fn.displayName-| Chromium-Fehler"  
[CR1178530]: https://crbug.com/1178530 "Problem 1178530: Die Konsole entweicht keine Doppelquote beim Drucken von Zeichenfolgen | Chromium-Fehler"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Farbanzeigequalität: Das Feature "Farbskala" | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Fokusmodus-UI – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "First-Party Sets | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2021/02/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
