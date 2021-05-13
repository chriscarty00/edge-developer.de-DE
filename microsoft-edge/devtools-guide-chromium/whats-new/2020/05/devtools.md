---
description: Verwenden Sie die DevTools Windows modus mit hohem Kontrast, und passen Sie Tastenkombinationen in den DevTools an Visual Studio Code und vieles mehr.
title: Neues in DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2537495ad14462aac70bfb1b5873aaa0b6e21cdf
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564672"
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

Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom DevTools-Microsoft Edge verpasst haben.  Sehen Sie sich die Ankündigungen an, um neue Features in den DevTools zu testen, Microsoft Visual Studio Codeerweiterungen und vieles mehr zu testen.  Laden Sie die Microsoft Edge-Vorschaukanäle herunter und folgen Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount] [um auf][MicrosoftEdgePreviewChannels] dem neuesten stand zu bleiben.  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Verwenden der DevTools im Windows modus mit hohem Kontrast

Die Microsoft Edge DevTools werden jetzt im Modus mit hohem Kontrast angezeigt, Windows sich im Modus mit hohem Kontrast befindet.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Die Microsoft Edge DevTools im Modus mit hohem Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Die Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

[Befolgen Sie die Anweisungen, um den Modus mit hohem Kontrast in Windows.][MicrosoftSupportWindows10HighContrastMode]  Wählen Sie zum Öffnen der DevTools in Microsoft Edge oder `F12` `Ctrl` + `Shift` + `I` aus.  Die DevTools werden im Modus mit hohem Kontrast angezeigt.  

> [!NOTE]
> Die Microsoft Edge DevTools unterstützen derzeit den Modus mit hohem Kontrast Windows macOS jedoch nicht.  

Chromium Problem [#1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code  

Aus Ihrem [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) und Chromium öffentlichen Problemverfolgung hat das Microsoft Edge DevTools-Team [erfahren,][CRIssuesList]dass Sie die Möglichkeit haben möchten, Tastenkombinationen in den DevTools anzupassen.  In Microsoft Edge 84 können Sie jetzt Tastenkombinationen in den DevTools mit [Visual Studio Code][VisualStudioCodeMain]übereinstimmen. Dies ist nur eines der Features, an denen das Team für die Anpassung von Verknüpfungen arbeitet.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Die Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

Um das Experiment zu testen, öffnen Sie DevTools Einstellungen, indem Sie das Symbol Devtools Einstellungen in der oberen rechten Ecke der DevTools auswählen oder `?` ![ ](../../../media/settings-icon.msft.png) auswählen.  Navigieren Sie zum Abschnitt **Experimente,** und aktivieren Sie die Registerkarte Einstellungen für benutzerdefinierte Tastenkombinationen **aktivieren (erfordert neu laden).**  Laden Sie jetzt die DevTools neu, öffnen Einstellungen erneut, und navigieren Sie zum **Abschnitt Verknüpfungen.**  

Wählen **Sie devTools (Standard)** in der Dropdownliste **Verknüpfungen** abwählen aus, und wählen Sie **Visual Studio Code**.  Die Tastenkombinationen in devTools entsprechen jetzt den Verknüpfungen für entsprechende Aktionen in Visual Studio Code.  

Beispielsweise ist die Tastenkombination zum Anhalten oder Fortsetzen des Ausführens eines Skripts in [Visual Studio Code][VisualStudioCodeShortcuts] `F5` .  Bei der **Voreinstellung DevTools (Default)** ist dieselbe Verknüpfung in devTools, aber mit der Visual Studio Code ist diese Verknüpfung `F8` jetzt auch **** `F5` .  

Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar, teilen Sie ihr Feedback daher bitte [mit](#getting-in-touch-with-microsoft-edge-devtools-team) dem Team!  

Chromium Problem [#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Remotedebugger von Surface Duo-Emulatoren  

Sie können nun Remotedebuggern Ihrer Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, mithilfe der vollen Leistung der [Microsoft Edge DevTools][DevtoolsIndex].  

Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von zusammenklappbaren Und Dual-Screen-Geräten gerendert werden.  Der Emulator führt das Betriebssystem Android aus und stellt die Microsoft Edge [Android-App bereit.][AndroidEdge]  Laden Sie Ihre Webinhalte in [Microsoft Edge App,][AndroidEdge] und debuggen Sie sie [mit dem Microsoft Edge DevTools][DevtoolsIndex].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge App, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Die Microsoft Edge-App im Surface Duo-Emulator  
:::image-end:::  

Die Seite in einer Desktopinstanz von Microsoft Edge zeigt `edge://inspect` **surfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaIndex] an, die im [Surface Duo-Emulator ausgeführt werden.][DualScreensAndroidEmulator] [][DesktopEdge]  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf edge://inspect seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge app angezeigt, die auf dem Emulator ausgeführt wird" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   Auf der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge `edge://inspect` angezeigt, die auf dem Emulator ausgeführt wird.
:::image-end:::  

Wählen **Sie überprüfen** nach der Registerkarte oder PWA, die Sie debuggen möchten, um die Microsoft Edge [DevTools zu öffnen.][DevtoolsIndex]  [Befolgen Sie die schrittweise Anleitung zum Remotedebuggern Ihrer Webinhalte im Surface Duo-Emulator.][DevtoolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Ändern der Größe der DevTools-Schublade einfacher  

In Microsoft Edge 83 oder früheren Versionen konnten Sie die Größe der [Devtools-Drawer][DevtoolsDrawer] nur ändern, indem Sie auf die Symbolleiste der Drawer zeigen.  Die Drawer hat sich anders verhalten als die anderen Größenänderungssteuerelemente für Bereiche in den DevTools, in denen Sie auf den Rahmen des Bereichs zeigen, um die Größe zu ändern.  Wählen Sie die folgende Abbildung aus, um zu zeigen, wie die Größe der Drawer in Version 83 oder früher als Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Ab Microsoft Edge 84 können Sie nun die Größe der Drawer ändern, indem Sie auf den Rahmen der Drawer zeigen.  Diese Änderung richtet das Verhalten der Größenänderung der DevTools-Drawer an der Art und Weise aus, wie Sie die Größe anderer Bereiche in devTools ändern.  Wählen Sie das folgende Bild aus, um die Größenänderung in Aktion in Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Chromium Problem [#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Bildschirmcastnavigationsschaltflächen zeigen den Fokus an  

Beim Remotedebugieren eines [Android-Geräts,][DevtoolsRemoteDebugAndroid]eines [Windows 10-Geräts][DevtoolsRemoteDebugWindows]oder eines Surface [Duo-Emulators][DevtoolsRemoteDebugDuoEmulator]können Sie screencasting mit dem Symbol Umschaltbildschirm in der oberen linken Ecke der DevTools umschalten. ![ ](../../../media/toggle-screencast-icon.msft.png)  Wenn die Screencasting aktiviert ist, können Sie über das DevTools-Fenster Microsoft Edge Registerkarte auf dem Remotegerät navigieren.  In Microsoft Edge 84 sind diese Navigationsschaltflächen jetzt auch über die Tastatur zugänglich.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Wählen Sie Umschalt+Tab aus der bildschirmcastierten URL-Leiste zeigt den Fokus auf der Schaltfläche Aktualisieren an." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Select `Shift` + `Tab` from the screencasted URL bar shows focus on the **Refresh** button
:::image-end:::  

Chromium Problem [#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Zugriff auf den Detailbereich des Netzwerkbereichs  

In Microsoft Edge 84 wird [][DevtoolsNetworkDetails] nun der **** Fokus auf den Detailbereich im Netzwerktool fokussieren, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll öffnen.][DevtoolsNetworkLog]  Mit dieser Änderung können Bildschirmlesegeräte den Inhalt des Detailbereichs **vorlesen und mit ihnen** interagieren.  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Detailbereich im Netzwerkbereich hat beim Öffnen den Fokus" lightbox="../../media/2020/05/network-details.msft.png":::
   Der **Detailbereich** im **Netzwerktool** hat beim Öffnen den Fokus
:::image-end:::  

Chromium Problem [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden zusätzliche features angekündigt, die in Microsoft Edge 84 verfügbar sind, die zum Open Source-Chromium wurden.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Beheben von Websiteproblemen mit dem neuen Problemtool in der DevTools-Schublade

Das neue **Problemtool** in der DevTools-Schublade wurde erstellt, um die Benachrichtigungsmüdigkeit und unübersichtlich der Konsole **zu reduzieren.**  Derzeit ist **die Konsole** der zentrale Ort für Websiteentwickler, Bibliotheken, Frameworks und Microsoft Edge zum Protokollieren von Nachrichten, Warnungen und Fehlern.  Das **Problemtool** aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und aktionsfähige Weise, Links zu betroffenen Ressourcen innerhalb von Microsoft Edge DevTools und bietet Anleitungen zum Beheben der Probleme.  Im Laufe der Zeit werden immer mehr Warnungen **** in Microsoft Edge im Problemtool und nicht in der Konsole **angezeigt,** was dazu beitragen sollte, die Unübersichtlichkeit in der Konsole **zu reduzieren.**  

Navigieren Sie zu Suchen und Beheben von Problemen mit dem Tool [Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool Probleme in der DevTools-Schublade" lightbox="../../media/2020/05/issues.msft.png":::
   Das **Tool Probleme** in der DevTools-Schublade  
:::image-end:::  

Chromium Problem [#1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Anzeigen von Barrierefreiheitsinformationen in der QuickInfo zum Überprüfungsmodus  

Die **QuickInfo zum Überprüfen des** Modus gibt [][WebhintHintsAxeNameRoleValue] jetzt an, ob das Element über einen barrierefreien Namen und eine Rolle verfügt und [tastaturfokussierbar ist.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Die QuickInfo zum Überprüfen des Modus mit Barrierefreiheitsinformationen" lightbox="../../media/2020/05/a11y.msft.png":::
  Die **QuickInfo zum Überprüfen des Modus** mit Barrierefreiheitsinformationen  
:::image-end:::  

Chromium Problem [#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Aktualisierungen des Leistungsbereichs  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Anzeigen von Informationen zur Sperrzeit insgesamt in der Fußzeile  

Nach der Aufzeichnung der Ladeleistung zeigt der Bereich **Leistung** nun Informationen zur Gesamtblockierungszeit \(TBT\) in der Fußzeile an.  TBT ist eine Lastleistungsmetrik, die quantifiziert, wie lange eine Seite benötigt, um verwendbar zu werden.  Es misst im Wesentlichen, wie lange eine Seite verwendbar zu sein scheint \(da der Inhalt auf dem Bildschirm gerendert wird\); ist jedoch nicht wirklich verwendbar, da JavaScript den Hauptthread blockiert und die Seite daher nicht auf Benutzereingaben reagiert.  TBT ist die Hauptmetrik für die 1. Eingabeverzögerung.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Verwenden Sie nicht den Seitenaktualisierungssymbolworkflow aktualisieren, um Informationen zur Gesamtsperrungszeit zu erhalten, um die Leistung der **** ![ Seite zu ](../../../media/refresh-page-icon.msft.png) erfassen.  

Wählen Sie stattdessen **Datensatzsymbol** aus, laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden ![ Sie dann die ](../../../media/record-icon.msft.png) Aufzeichnung.  

Wenn angezeigt wird, Microsoft Edge DevTools nicht die erforderlichen Informationen aus den internen `Total Blocking Time: Unavailable` Profilerstellungsdaten in Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Informationen zur Blockierungszeit insgesamt in der Fußzeile einer Aufzeichnung des Leistungsbereichs" lightbox="../../media/2020/05/tbt.msft.png":::
   Informationen zur Blockierungszeit insgesamt in der Fußzeile einer **Aufzeichnung des Leistungsbereichs**  
:::image-end:::  

Chromium Problem [#1054381][CR1054381]  

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

Die **Konsole** verwendet nun den Begriff `fulfilled` , der an der Spezifikation ausgerichtet `Promise` ist.  Weitere Informationen zur Spezifikation `Promise` finden Sie unter States and [Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

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

Chromium Problem [#1075437][CR1075437]  

#### <a name="image-previews"></a>Bildvorschau  

Zeigen Sie auf einen Wert im Bereich Formatvorlagen, um eine Vorschau des `background-image` Bilds in einer QuickInfo anzuzeigen. ****  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Zeigen auf einen Hintergrundbildwert" lightbox="../../media/2020/05/image-preview.msft.png":::
  Zeigen auf einen `background-image` Wert  
:::image-end:::  

Chromium Problem [#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>Die Farbauswahl verwendet jetzt eine durch Leerzeichen getrennte funktionale Farbtonation.  

[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] gibt an, dass Farbfunktionen, z. B. , leerzeichen `rgb()` getrennte Argumente unterstützen sollen.  So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.  

Wenn Sie Farben [][DevtoolsCssReferenceColorPicker] mit der Farbauswahl auswählen oder **** zwischen Farbdarstellungen im Formatvorlagenbereich wechseln, indem Sie den Wert halten und auswählen, wird die Syntax des durch Leerzeichen getrennten Arguments `Shift` `background-color` angezeigt.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Formatvorlagenbereich" lightbox="../../media/2020/05/color.msft.png":::
  Verwenden von durch Leerzeichen getrennten Argumenten im **Formatvorlagenbereich**  
:::image-end:::  

Sie sollten auch die Syntax im **Bereich "Berechnet"** und in der **QuickInfo "Inspect Mode"** anzeigen.  

Microsoft Edge DevTools verwendet die neue Syntax, da bevorstehende #A0 wie [color()][CSSWGDraftsColor4Property] die veraltete Argumentsyntax durch Kommas nicht unterstützen.  

Die Syntax des durch Leerzeichen getrennten Arguments wird in den meisten Browsern seit einer Weile unterstützt.  Weitere Informationen finden Sie unter [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Chromium Problem [#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Veraltetes Anzeigen des Eigenschaftenbereichs im Elementbereich  

Der **Eigenschaftenbereich** im **Elementtool** ist veraltet.  Führen `console.dir($0)` Sie stattdessen in der **Konsole** aus.  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Veralteter Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   Veralteter **Eigenschaftenbereich**  
:::image-end:::  

#### <a name="references"></a>Verweise  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Unterstützung von App-Verknüpfungen im Manifestbereich  

Mithilfe von App-Verknüpfungen können Benutzer häufige oder empfohlene Aufgaben in einer Web-App schnell starten.  Das Menü "App-Verknüpfungen" wird nur für [Progressive Web Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Manifestbereich" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  App-Verknüpfungen im **Manifestbereich**  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie sich auf Windows oder macOS befinden, sollten Sie die Microsoft Edge Vorschaukanäle [als][MicrosoftEdgePreviewChannels] Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Kontakt mit Microsoft Edge Devtools-Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

<!--[DevtoolsWhatsNew201901Inspect]: ../../../whats-new/2019/01/devtools.md#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[DevtoolsConsoleApiDir]: ../../../console/api.md#dir "dir – Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]: ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Kürzlich ausgewähltes Element oder JavaScript-Objekt – Console Utilities API Reference | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Referenz | Microsoft Docs"  
[DevtoolsDrawer]: ../../../customize/index.md#drawer "Drawer – Customize Overview | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mit Microsoft Edge Der Registerkarte &quot;DevTools-Probleme&quot; | Microsoft Docs"  
[DevtoolsNetworkDetails]: ../../../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der | Microsoft Docs"  
[DevtoolsNetworkLog]: ../../../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäts| Microsoft Docs"  
[DevtoolsRemoteDebugAndroid]: ../../../remote-debugging/index.md "Erste Schritte remote debugging android devices | Microsoft Docs"  
[DevtoolsRemoteDebugDuoEmulator]: ../../../remote-debugging/surface-duo-emulator.md "Erste Schritte remote Debuggen von Surface Duo-Emulatoren | Microsoft Docs"  
[DevtoolsRemoteDebugWindows]: ../../../remote-debugging/windows.md "Erste Schritte remote debugging Windows 10 Devices | Microsoft Docs"  

[PwaIndex]: ../../../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft Docs"  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android-App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Durch Leerzeichen getrennte funktionale Farb notationen – MDN-| Kann ich verwenden"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Formatvorlagenbereich | Chromium Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Zeigen Sie grundlegende a11y-Informationen in Elementpopover-| Chromium Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools UI-Unterstützung für den Modus &quot;Hoher Kontrast&quot; | Chromium Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium Fehler"  
[CR1068116]: https://crbug.com/1068116 "Problembereich für | Chromium Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: Die Farbauswahl sollte eine moderne CSS-Farbsyntax | Chromium Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Fügen Sie Unterstützung für das Schlüsselwort/den Wert der CSS-| Chromium Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung – Größenanpassung der Schublade"  
[CR1081486]: https://crbug.com/1081486 "Der Tastaturfokus ist für Navigationsschaltflächen im Screencastmodus nicht | Chromium Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte &quot;erfüllt&quot; und nicht &quot;aufgelöst&quot; | V8-Fehler"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen von Farben 3 – CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die &quot;Farbe&quot; - CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in die Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "States and Fates – domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "Wiederherstellen | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browserkompatibilität | MDN"  

[VisualStudioCodeMain]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: Tastatur | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus mit hohem Kontrast in Windows | Windows-Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Vorschaukanäle"  
[TheWebWeWantMain]: https://aka.ms/webwewant "The Web We Want"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developer.chrome.com/blog/new-in-devtools-84) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
