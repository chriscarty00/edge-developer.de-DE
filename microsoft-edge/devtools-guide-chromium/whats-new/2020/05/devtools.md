---
description: Verwenden Sie die DevTools im Windows-Modus mit hohem Kontrast, passen Sie Tastenkombinationen in den DevTools an, Visual Studio Code zu ändern, und vieles mehr.
title: Neues in DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3264292721d5e4385b0e6d256d042c76182c21c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408325"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Neues in DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Ankündigungen des Microsoft Edge DevTools-Teams  

Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.  Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.  Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount]um über die neuesten und besten Features in Ihren Entwicklertools auf dem neuesten Stand zu bleiben.  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Verwenden der DevTools im Windows-Modus mit hohem Kontrast

Die Microsoft Edge DevTools werden jetzt im Modus mit hohem Kontrast angezeigt, wenn sich Windows im Modus mit hohem Kontrast befindet.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools im Modus mit hohem Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

[Befolgen Sie die Anweisungen, um den Modus mit hohem Kontrast in Windows zu aktivieren.][MicrosoftSupportWindows10HighContrastMode]  Wählen Sie oder aus, um die DevTools in Microsoft Edge `F12` zu `Ctrl` + `Shift` + `I` öffnen.  Die DevTools werden im Modus mit hohem Kontrast angezeigt.  

> [!NOTE]
> Die Microsoft Edge DevTools unterstützen derzeit den Modus mit hohem Kontrast unter Windows, jedoch nicht unter macOS.  

[Chromium-Problem #1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Übereinstimmung von Tastenkombinationen in devTools mit Visual Studio Code  

Aus Ihrem [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) und dem [Chromium-Problemverfolgungstool][CRIssuesList]für öffentliche Fragen hat das Microsoft Edge DevTools-Team erfahren, dass Sie die Möglichkeit haben wollten, Tastenkombinationen in den DevTools anzupassen.  In Microsoft Edge 84 können Sie nun Tastenkombinationen in den DevTools mit [Visual Studio Code][VisualStudioCode]übereinstimmen. Dies ist nur eines der Features, an denen das Team für die Anpassung von Verknüpfungen arbeitet.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Übereinstimmung von Tastenkombinationen in devTools mit Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

Um das Experiment zu testen, öffnen Sie devTools-Einstellungen, indem Sie in der oberen rechten Ecke der DevTools das Symbol `?` ![ DevTools-Einstellungen auswählen oder ][ImageSettingsIcon] auswählen.  Navigieren Sie zum Abschnitt **Experimente,** und aktivieren Sie die Registerkarte Einstellungen für benutzerdefinierte Tastenkombinationen **aktivieren (erfordert neu laden).**  Laden Sie jetzt die DevTools neu, öffnen Sie die Einstellungen erneut, und navigieren Sie zum **Abschnitt Verknüpfungen.**  

Wählen **Sie DevTools (Standard)** in der Dropdownliste **Verknüpfungen** abwählen aus, und wählen Sie **Visual Studio Code aus.**  Die Tastenkombinationen in den DevTools entsprechen jetzt den Verknüpfungen für entsprechende Aktionen in Visual Studio Code.  

Beispielsweise ist die Tastenkombination zum Anhalten oder Fortsetzen des Ausführens eines Skripts in [Visual Studio Code][VisualStudioCodeShortcuts] `F5` .  Mit der **Voreinstellung DevTools (Default)** ist dieselbe Verknüpfung in devTools, aber mit der voreingestellten `F8` Visual Studio **Code,** ist diese Verknüpfung jetzt auch `F5` .  

Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar, teilen Sie ihr Feedback daher bitte [mit](#getting-in-touch-with-microsoft-edge-devtools-team) dem Team!  

[Chromium-#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Remotedebugger von Surface Duo-Emulatoren  

Sie können nun Remotedebuggern Ihrer Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, mithilfe der vollen Leistung von [Microsoft Edge DevTools][DevToolsChromiumGuide].  

Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von zusammenklappbaren Und Dual-Screen-Geräten gerendert werden.  Der Emulator führt das Betriebssystem Android aus und stellt die [Microsoft Edge Android-App bereit.][AndroidEdge]  Laden Sie Ihre Webinhalte in der [Microsoft Edge-App, und][AndroidEdge] debuggen Sie sie mit [den Microsoft Edge DevTools][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge-App, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Die Microsoft Edge-App auf dem Surface Duo-Emulator  
:::image-end:::  

Die Seite in einer Desktopinstanz von Microsoft Edge zeigt `edge://inspect` **surfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs,][PwaIndex] die auf dem [Surface Duo-Emulator ausgeführt werden.][DualScreensAndroidEmulator] [][DesktopEdge]  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf edge://inspect wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   Auf `edge://inspect` der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.
:::image-end:::  

Wählen **Sie Überprüfen** nach der Registerkarte oder dem PWA aus, die Sie debuggen möchten, um die Microsoft Edge [DevTools zu öffnen.][DevToolsChromiumGuide]  [Befolgen Sie die schrittweise Anleitung zum Remotedebuggern Ihrer Webinhalte im Surface Duo-Emulator.][DevToolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Ändern der Größe der DevTools-Schublade einfacher  

In Microsoft Edge 83 oder früher konnten Sie die Größe der [DevTools-Drawer][DevToolsDrawer] nur ändern, indem Sie auf die Symbolleiste der Drawer zeigen.  Die Drawer hat sich anders verhalten als die anderen Größenänderungssteuerelemente für Bereiche in den DevTools, in denen Sie auf den Rahmen des Bereichs zeigen, um die Größe zu ändern.  Wählen Sie die folgende Abbildung aus, um die Größe der Drawer in Version 83 oder früher von Microsoft Edge zu ändern.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Ab Microsoft Edge 84 können Sie nun die Größe der Drawer ändern, indem Sie auf den Rahmen der Drawer zeigen.  Diese Änderung richtet das Verhalten der Größenänderung der DevTools-Drawer an der Art und Weise aus, wie Sie die Größe anderer Bereiche in devTools ändern.  Wählen Sie das folgende Bild aus, um die Größe in Aktion in Microsoft Edge 84 zu ändern.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

[Chromium-#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Bildschirmcastnavigationsschaltflächen zeigen den Fokus an  

Beim Remotedebugieren eines [Android-Geräts,][DevToolsRemoteDebugAndroid]eines Windows [10-Geräts][DevToolsRemoteDebugWindows]oder eines Surface [Duo-Emulators][DevToolsRemoteDebugDuoEmulator]können Sie screencasting mit dem Symbol Umschaltbildschirm in der oberen linken Ecke der ![ ][ImageScreencastingIcon] DevTools umschalten.  Wenn die Screencasting aktiviert ist, können Sie über das DevTools-Fenster auf der Registerkarte in Microsoft Edge auf dem Remotegerät navigieren.  In Microsoft Edge 84 sind diese Navigationsschaltflächen jetzt auch über die Tastatur zugänglich.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Wählen Sie Umschalt+Tab aus der bildschirmcastierten URL-Leiste zeigt den Fokus auf der Schaltfläche Aktualisieren an." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Select `Shift` + `Tab` from the screencasted URL bar shows focus on the **Refresh** button
:::image-end:::  

[Chromium-#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Zugriff auf den Detailbereich des Netzwerkbereichs  

In Microsoft Edge 84 steht **** der [Detailbereich][DevToolsNetworkDetails] im Netzwerktool jetzt im Fokus, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll öffnen.][DevToolsNetworkLog]  Mit dieser Änderung können Bildschirmlesegeräte den Inhalt des Detailbereichs **vorlesen und mit ihnen** interagieren.  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Detailbereich im Netzwerkbereich hat beim Öffnen den Fokus" lightbox="../../media/2020/05/network-details.msft.png":::
   Der **Detailbereich** im **Netzwerktool** hat beim Öffnen den Fokus
:::image-end:::  

[Chromium-#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 84 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Beheben von Websiteproblemen mit dem neuen Problemtool in der DevTools-Schublade

Das neue **Problemtool** in der DevTools-Schublade wurde erstellt, um die Benachrichtigungsmüdigkeit und unübersichtlich der Konsole **zu reduzieren.**  Derzeit ist **die Konsole** der zentrale Ort für Websiteentwickler, Bibliotheken, Frameworks und Microsoft Edge zum Protokollieren von Nachrichten, Warnungen und Fehlern.  Das **Problemtool** aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und aktionsfähige Weise, links zu betroffenen Ressourcen in Microsoft Edge DevTools und bietet Anleitungen zum Beheben der Probleme.  Im Laufe der Zeit werden immer mehr Warnungen in Microsoft Edge im Tool Probleme und nicht in der Konsole **angezeigt,** was dazu beitragen sollte, die Unübersichtlichkeit in der Konsole **zu reduzieren.** ****  

Navigieren Sie zu Suchen und Beheben von Problemen mit dem [Microsoft Edge DevTools-Tool,][DevtoolsIssuesIndex]um zu beginnen.  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool Probleme in der DevTools-Schublade" lightbox="../../media/2020/05/issues.msft.png":::
   Das **Tool Probleme** in der DevTools-Schublade  
:::image-end:::  

[Chromium-Problem #1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Anzeigen von Barrierefreiheitsinformationen in der QuickInfo zum Überprüfungsmodus  

Die **QuickInfo zum Überprüfen des** Modus gibt [][WebhintHintsAxeNameRoleValue] jetzt an, ob das Element über einen barrierefreien Namen und eine Rolle verfügt und [tastaturfokussierbar ist.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Die QuickInfo zum Überprüfen des Modus mit Barrierefreiheitsinformationen" lightbox="../../media/2020/05/a11y.msft.png":::
  Die **QuickInfo zum Überprüfen des Modus** mit Barrierefreiheitsinformationen  
:::image-end:::  

[Chromium-#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Aktualisierungen des Leistungsbereichs  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Anzeigen von Informationen zur Sperrzeit insgesamt in der Fußzeile  

Nach der Aufzeichnung der Ladeleistung zeigt der Bereich **Leistung** nun Informationen zur Gesamtblockierungszeit \(TBT\) in der Fußzeile an.  TBT ist eine Lastleistungsmetrik, die quantifiziert, wie lange eine Seite benötigt, um verwendbar zu werden.  Es misst im Wesentlichen, wie lange eine Seite verwendbar zu sein scheint \(da der Inhalt auf dem Bildschirm gerendert wird\); ist jedoch nicht wirklich verwendbar, da JavaScript den Hauptthread blockiert und die Seite daher nicht auf Benutzereingaben reagiert.  TBT ist die Hauptmetrik für die 1. Eingabeverzögerung.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Verwenden Sie nicht den Seitenaktualisierungssymbolworkflow aktualisieren, um Informationen zur Gesamtsperrungszeit zu erhalten, um die Leistung der **** ![ Seite zu ][ImageRefreshPageIcon] erfassen.  

Wählen Sie stattdessen **Datensatzsymbol** aus, laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden ![ Sie dann die ][ImageRecordIcon] Aufzeichnung.  

Wenn angezeigt wird, hat Microsoft Edge DevTools nicht die erforderlichen Informationen aus den internen `Total Blocking Time: Unavailable` Profilerstellungsdaten in Microsoft Edge erhalten.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Informationen zur Blockierungszeit insgesamt in der Fußzeile einer Aufzeichnung des Leistungsbereichs" lightbox="../../media/2020/05/tbt.msft.png":::
   Informationen zur Blockierungszeit insgesamt in der Fußzeile einer **Aufzeichnung des Leistungsbereichs**  
:::image-end:::  

[Chromium-#1054381][CR1054381]  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>Layout Shift-Ereignisse im Abschnitt neue Besen  

Der neue **Abschnitt "Erfahrung"** **des** Leistungsbereichs hilft Ihnen, Layoutverschiebungen zu erkennen.  Kumulative Layoutverschiebung \(CLS\) ist eine Metrik, mit der Sie unerwünschte visuelle Instabilitäten quantifizieren können.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Wählen Sie **das Layout shift-Ereignis** aus, um die Details der Layoutverschiebung im **Zusammenfassungsbereich anzuzeigen.**  Zeigen Sie auf die **Felder Verschoben von** und Zu **Feldern,** um zu visualisieren, wo die Layoutverschiebung aufgetreten ist.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Die Details einer Layoutverschiebung" lightbox="../../media/2020/05/cls.msft.png":::
   Die Details einer Layoutverschiebung  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Präzisere Zusageterminologie in der Konsole  

Bei der Protokollierung eines `Promise` hat **die Konsole** fälschlicherweise den Wert `PromiseStatus` auf `resolved` festgelegt.  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Ein Beispiel für die Konsole mit der alten aufgelösten Terminologie" lightbox="../../media/2020/05/resolved.msft.png":::
   Ein Beispiel für die **Konsole** mit der alten `resolved` Terminologie  
:::image-end:::  

Die **Konsole** verwendet nun den Begriff `fulfilled` , der an der Spezifikation ausgerichtet `Promise` ist.  Weitere Informationen zur Spezifikation `Promise` finden Sie unter States and [Fates auf GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Ein Beispiel für die Konsole mit der neuen erfüllten Terminologie" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Ein Beispiel für die **Konsole** mit der neuen `fulfilled` Terminologie  
:::image-end:::  

V8-Problem [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Aktualisierungen des Formatbereichs  

#### <a name="support-for-the-revert-keyword"></a>Unterstützung für das Revert-Schlüsselwort  

Die Benutzeroberfläche für die **** automatische Vervollständigung des Bereichs Formatvorlagen erkennt nun das Schlüsselwort [CSS][MDNRevert] wiederherstellen, das den kaskadierten Wert einer Eigenschaft auf den vorherigen Wert zurück setzt, der auf die Formatierung des Elements angewendet wurde.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Festlegen des Werts einer eigenschaft, die zurückgesetzt werden soll" lightbox="../../media/2020/05/revert.msft.png":::
  Festlegen des Werts einer eigenschaft, die zurückgesetzt werden soll  
:::image-end:::  

[Chromium-#1075437][CR1075437]  

#### <a name="image-previews"></a>Bildvorschau  

Zeigen Sie auf einen Wert im Bereich Formatvorlagen, um eine Vorschau des `background-image` Bilds in einer QuickInfo anzuzeigen. ****  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Zeigen auf einen Hintergrundbildwert" lightbox="../../media/2020/05/image-preview.msft.png":::
  Zeigen auf einen `background-image` Wert  
:::image-end:::  

[Chromium-#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>Die Farbauswahl verwendet jetzt eine durch Leerzeichen getrennte funktionale Farbtonation.  

[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] gibt an, dass Farbfunktionen, z. B. , leerzeichen `rgb()` getrennte Argumente unterstützen sollen.  So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.  

Wenn Sie Farben [][DevtoolsCssReferenceColorPicker] mit der Farbauswahl auswählen oder **** zwischen Farbdarstellungen im Formatvorlagenbereich wechseln, indem Sie den Wert halten und auswählen, wird die Syntax des durch Leerzeichen getrennten Arguments `Shift` `background-color` angezeigt.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Formatvorlagenbereich" lightbox="../../media/2020/05/color.msft.png":::
  Verwenden von durch Leerzeichen getrennten Argumenten im **Formatvorlagenbereich**  
:::image-end:::  

Sie sollten auch die Syntax im **Bereich "Berechnet"** und in der **QuickInfo "Inspect Mode"** anzeigen.  

Microsoft Edge DevTools verwendet die neue Syntax, da bevorstehende #A0 wie [color()][CSSWGDraftsColor4Property] die veraltete Argumentsyntax durch Kommas nicht unterstützen.  

Die Syntax des durch Leerzeichen getrennten Arguments wird in den meisten Browsern seit einer Weile unterstützt.  Weitere Informationen finden Sie unter [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

[Chromium-#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Veraltetes Anzeigen des Eigenschaftenbereichs im Elementbereich  

Der **Eigenschaftenbereich** im **Elementtool** ist veraltet.  Führen `console.dir($0)` Sie stattdessen in der **Konsole** aus.  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Veralteter Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   Veralteter **Eigenschaftenbereich**  
:::image-end:::  

#### <a name="references"></a>Verweise  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Unterstützung von App-Verknüpfungen im Manifestbereich  

Mithilfe von App-Verknüpfungen können Benutzer häufige oder empfohlene Aufgaben in einer Web-App schnell starten.  Das Menü "App-Verknüpfungen" wird nur für [Progressive Web Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Manifestbereich" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  App-Verknüpfungen im **Manifestbereich**  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Kontakt zum Microsoft Edge Devtools-Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir – Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Referenz | Microsoft Docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Customize Overview | Microsoft Docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Suchen und Beheben von Problemen mit der Registerkarte Microsoft Edge DevTools-Probleme | Microsoft Docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Erste Schritte mit Remotedebugieren von Surface Duo-Emulatoren | Microsoft Docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit remote debugging Windows 10 Devices | Microsoft Docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Überprüfen Sie die Details der | Microsoft Docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollieren von Netzwerkaktivitäts| Microsoft Docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web Apps unter Windows | Microsoft Docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Durch Leerzeichen getrennte funktionale Farb notationen – MDN-| Kann ich verwenden"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium-Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium-Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Formatvorlagenbereich | Chromium-Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Zeigen Sie grundlegende a11y-Informationen in Elementpopover-| Chromium-Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools UI-Unterstützung für den Modus "Hoher Kontrast" | Chromium-Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium-Fehler"  
[CR1068116]: https://crbug.com/1068116 "Problembereich für | Chromium-Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: Die Farbauswahl sollte eine moderne CSS-Farbsyntax | Chromium-Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Fügen Sie Unterstützung für das Schlüsselwort/den Wert der CSS-| Chromium-Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung – Größenanpassung der Schublade"  
[CR1081486]: https://crbug.com/1081486 "Der Tastaturfokus ist für Navigationsschaltflächen im Screencastmodus nicht | Chromium-Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte "erfüllt" und nicht "aufgelöst" | V8-Fehler"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen von Farben 3 – CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die "Farbe" - CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in das neue Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "States and Fates – domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "Wiederherstellen | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browserkompatibilität | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: Tastatur | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus mit hohem Kontrast in Windows | Windows-Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview Channels"  
[TheWebWeWant]: https://aka.ms/webwewant "The Web We Want"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/05/devtools/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
