---
description: Verbesserungen der Barrierefreiheit, Verwendung des devtools in anderen Sprachen und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8f82f46cd683433a37614bcf15745e1de9f31ffb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015468"
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

# Neuerungen in devtools (Microsoft Edge 80)  

## Ankündigungen des Microsoft Edge devtools-Teams  

In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben. Schauen Sie sich diese an, um neue Features in den devtools, Visual Studio-Code Erweiterungen und vieles mehr zu testen.  Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].  

### Verbesserungen der Barrierefreiheit für devtools  

Das devtools-Team hat 170-Änderungen zu chromium beigetragen, um Probleme mit der Farbkontrast-, Tastatur-und Bildschirmsprachausgabe in devtools zu beheben.  Jeder Entwickler, der das Web erstellt, sollte in der Lage sein, das devtools zu verwenden.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   Das Tool " **Leistung** " im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe  
:::image-end:::  

Möchten Sie erfahren, wie Sie Ihre Webseite für alle Benutzer barrierefrei gestalten können?  Laden Sie die [Barrierefreiheits Einblicke][AccessibilityInsights] und [webhint][WebhintBrowserExtension] -Erweiterungen für Microsoft Edge herunter, um zu beginnen.  

Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie Ihr Feedback, indem Sie uns über [tweeten][PostTweetEdgeDevTools] oder auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) klicken.  

Chrom Problem [#963183][CR963183]  

### Verwenden des devtools in anderen Sprachen  

Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio-Code in ihrer Muttersprache, nicht nur in Englisch.  Wir freuen uns, die Lokalisierung für das devtools bekannt zu geben, das Sie nun in einer von 10 Sprachen außer Englisch verwenden können:  

:::row:::
   :::column span="":::
      Chinesisch (vereinfacht \) –  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinesisch (traditionell \) –  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Französisch – Fran&#231;AIS
   :::column-end:::
   :::column span="":::
      Deutsch-Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italienisch-Italiano
   :::column-end:::
   :::column span="":::
      Japanisch –  &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Koreanisch –  &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugiesisch-Portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russisch –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Spanisch-ESPA&#241;OL
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Navigieren Sie zu `edge://flags` und setzen Sie das Kennzeichen **lokalisierte Entwickler Tools aktivieren** auf **aktiviert**.  Setzen Sie auch das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**.  Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  Die devtools entsprechen der Sprache, in der Sie Microsoft Edge verwenden `edge://settings/languages` .  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="Das devtools in Deutsch" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   Das devtools in Deutsch  
:::image-end:::  

Wenn Sie das devtools in einer anderen Sprache als den verfügbaren verwenden möchten, senden Sie uns eine [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) .  

Chrom Problem [#941561][CR941561]  

### webhint Microsoft Edge-Erweiterung  

Mit der webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite auf einfache Weise überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und vielem mehr in der devtools erhalten.  Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   Die Registerkarte " **Hinweise** " im devtools, wenn die webhint-Browser Erweiterung installiert ist  
:::image-end:::  

[Testen Sie die webhint-Browser Erweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].  Nachdem Sie die Erweiterung installiert haben, öffnen Sie das devtools, und wählen Sie die Registerkarte Hinweise aus.  Führen Sie von hier aus eine anpassbare Website Überprüfung aus.  Besuchen Sie [webhint.IO][WebhintBrowserExtension] , um weitere Informationen zu erhalten.

### 3D View  

Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \ (DOM \)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Die 3D-Ansicht im devtools" lightbox="../../images/2019/12/3dview.msft.png":::
   Die **3D-Ansicht** im devtools  
:::image-end:::  

Wenn Sie auf die 3D-Ansicht zugreifen möchten, navigieren Sie zu `edge://flags` und stellen Sie sicher, dass das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**festgesetzt ist.  Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.  Drücken Sie `F1` im devtools oder wechseln Sie zu **Einstellungen**, navigieren Sie zu **Experimenten** , und aktivieren Sie das Kontrollkästchen **3D-Ansicht aktivieren** .  Drücken Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht** ein, und wählen Sie **3D-Ansicht**anzeigen aus.  

Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht Weitere Funktionen hinzu, damit Sie uns Ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team)senden können.  

Chrom Problem [#987787][CR987787]

### Visual Studio-Code Erweiterungen  

Das devtools-Team hat auch einige Erweiterungen für [Visual Studio-Code][VisualStudioCode] veröffentlicht, mit denen Sie die Leistung des devtools direkt aus Ihrem Text-Editor verwenden können. Schauen Sie sich die folgenden Erweiterungen an.  

#### Elemente für Microsoft Edge  

Verwenden Sie das elementtool in Visual Studio-Code, indem Sie die Visual Studio-Code Erweiterung " [Elemente für Microsoft Edge (Chrom)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] " hinzufügen.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Das Tool ' Elemente ' in Visual Studio-Code mit den Elementen für Microsoft Edge Extension" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   Das Tool ' **Elemente** ' in Visual Studio-Code mit den Elementen für Microsoft Edge Extension  
:::image-end:::  

Weitere Informationen finden Sie unter [Elemente für die Microsoft Edge Visual Studio-Code Erweiterung][VisualStudioCodeElementEdgeExtension].  

#### Debugger für Microsoft Edge  

Debuggen Sie JavaScript in Microsoft Edge direkt aus Visual Studio-Code, wenn Sie den [Debugger für Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio-Code Erweiterung ausführen.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Der Debugger für Microsoft Edge Extension in Visual Studio-Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   Der Debugger für Microsoft Edge Extension in Visual Studio-Code  
:::image-end:::  

Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus Visual Studio-Code][VisualStudioCodeDebuggerEdgeExtension].  

#### Webhint  

Die [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio-Code Erweiterung verwendet `webhint` , um Ihre Webseite zu verbessern, während Sie Sie schreiben! Mit dieser Erweiterung wird die Diagnose für Ihre Arbeitsbereichsdateien basierend auf der Analyse ausgeführt und gemeldet `webhint` .  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Die webhint Visual Studio-Code Erweiterung, die eine TSX-Datei in Visual Studio-Code analysiert" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   Die webhint Visual Studio-Code Erweiterung, die eine `.tsx` Datei in Visual Studio-Code analysiert  
:::image-end:::  

[Erfahren Sie mehr über die Visual Studio-Code webhint-Erweiterung][WebhintVisualStudioCodeExtension].  

### Integration von Visual Studio
Verwenden Sie in Visual Studio 2019, Version 16,2 oder höher, den Visual Studio-Debugger zum Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird.  [Laden Sie Visual Studio 2019 herunter][MicrosoftVisualStudioDownloads] , um dieses Feature auszuprobieren!  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta  
:::image-end:::  

[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge in Visual Studio debuggen][MicrosoftVisualStudioBlogDebugJavascript]können.  

### Nachrichten zur Präventions Konsole  

Die nach Verfolgungs Verhinderung ist ein einzigartiges Feature in Microsoft Edge, das Sie davor schützt, von Websites, die Sie noch nicht besucht haben, nachverfolgt  Die Standardeinstellung für die nach Verfolgungs Verhinderung ist der Modus "ausgeglichen", der Drittanbieter-Tracker und bekannte bösartige Tracker für eine Erfahrung blockiert, die Datenschutz und Web-Kompatibilität abgleicht.  Damit Sie mehr über die Kompatibilität Ihrer Webseite erfahren, wenn bestimmte Tracker blockiert sind, haben wir auch Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert ist.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Nachrichten in der **Konsole** , wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert  
:::image-end:::  

[Weitere Informationen finden Sie unter Verhinderung von Nachverfolgung und dem Gleichgewichtzwischen Datenschutz und Web-Kompatibilität][TrackingPrevention].  

## Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden weitere in Microsoft Edge 80 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.  

### Unterstützung für Let-und Class-Deklarationen in der Konsole  

Die **Konsole** unterstützt jetzt erneute Deklarationen von `let` und- `class` Anweisungen.  Die Unfähigkeit, erneut zu deklarieren, war ein häufiges Ärgernis für Webentwickler, die die Konsole zum Experimentieren mit neuem JavaScript-Code verwenden.  

> [!WARNING]
> Das erneute Deklarieren einer `let` oder `class` -Anweisung in einem Skript außerhalb der Konsole oder in einer einzelnen Konsoleneingabe führt weiterhin zu einer `SyntaxError` .  

Bei der erneuten Deklaration einer lokalen Variablen mit `let` hat die Konsole beispielsweise einen Fehler ausgelöst:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt" lightbox="../../images/2019/12/letbefore.msft.png":::
   Die **Konsole** in Microsoft Edge 79, die zeigt, dass die Let-erneute Deklaration fehlschlägt  
:::image-end:::  

Die Konsole ermöglicht nun die erneute Deklaration:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist" lightbox="../../images/2019/12/letafter.msft.png":::
   Die **Konsole** in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist  
:::image-end:::  

Chrom Problem [#1004193][CR1004193]  

### Verbessertes Webassembly-Debugging  

DevTools hat mit der Unterstützung des [Dwarf-Debugging-Standards][DwarfHome]begonnen, was mehr Unterstützung für die schrittweise Codierung, das Festlegen von Haltepunkten und das Auflösen von Stapelablaufverfolgungen in ihren Quellsprachen in devtools bedeutet.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### Netzwerk Panel-Updates  

#### Anfordern von Initiator-Chains auf der Registerkarte "Initiator"  

Sie können nun die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.  Dies kann Ihnen helfen zu verstehen, warum eine Ressource angefordert wurde, oder welche Netzwerkaktivität eine bestimmte Ressource (wie ein Skript \) verursacht hat.  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"" lightbox="../../images/2019/12/initiators.msft.png":::
   Eine Anforderungs Initiator-Kette auf der Registerkarte " **Initiator** "  
:::image-end:::  

Klicken Sie nach dem [Protokollieren der Netzwerkaktivität in der Netzwerksteuerung][DevToolsNetworkIndex]auf eine Ressource, und wechseln Sie dann zur Registerkarte **Initiator** , um die **Anforderungs initiatorkette**anzuzeigen:  

*   Die **geprüfte Ressource** ist fett formatiert.  Im obigen Screenshot `ai.2.min.js` befindet sich die geprüfte Ressource.  
*   Die Ressourcen oberhalb der geprüften Ressource sind die **Initiatoren**.  Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .  Mit anderen Worten: `https://www.microsoftedgeinsider.com` Ursache für die Netzwerkanforderung `ai.2.min.js` .  
*   Die Ressourcen unterhalb der geprüften Ressource sind die **Abhängigkeiten**.  Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .  Mit anderen Worten: `ai.2.min.js` Ursache für die Netzwerkanforderung `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> Auf Initiator-und Abhängigkeitsinformationen kann auch zugegriffen werden, indem Sie `Shift` auf Netzwerkressourcen halten und dann darauf zeigen.  Weitere Informationen finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevToolsNetworkReferenceViewInitiatorsDependencies].  

Chrom Problem [#842488][CR842488]  

#### Markieren der ausgewählten Netzwerkanforderung in der Übersicht  

Nachdem Sie auf eine Netzwerkressource klicken, um Sie zu überprüfen, fügt das Netzwerk Panel nun einen blauen Rahmen um die Ressource in der **Übersicht**ein.  Dies kann Ihnen helfen zu erkennen, ob die Netzwerkanforderung früher oder später als erwartet ausgeführt wird.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Der Übersichtsbereich, der die überprüfte Ressource markiert" lightbox="../../images/2019/12/overview.msft.png":::
   Der Übersichtsbereich, der die **über** prüfte Ressource markiert  
:::image-end:::  

Chrom Problem [#988253][CR988253]  

#### URL-und Pfad Spalten im Netzwerk Panel  

Verwenden Sie die Spalten neuer **Pfad** und **URL** im **Netzwerk** Panel, um den absoluten Pfad oder die vollständige URL der einzelnen Netzwerkressourcen anzuzeigen.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel" lightbox="../../images/2019/12/columns.msft.png":::
   Die Spalten ' neuer Pfad ' und ' URL ' im **Netzwerk** Panel  
:::image-end:::  

Klicken Sie mit der rechten Maustaste auf die Tabelle Überschrift **Wasserfall** , und wählen Sie **Pfad** oder **URL** aus, um die neuen Spalten anzuzeigen.  

Chrom Problem [#993366][CR993366]  

#### Aktualisierte Benutzer-Agent-Zeichenfolgen  

DevTools unterstützt das Festlegen einer benutzerdefinierten Benutzer-Agent-Zeichenfolge über die Registerkarte **Netzwerkbedingungen** .  Die Benutzer-Agent-Zeichenfolge wirkt `User-Agent` sich auf den an Netzwerkressourcen angefügten HTTP-Header und auch auf den Wert von aus `navigator.userAgent` .  

Die vordefinierten Benutzer-Agent-Zeichenfolgen wurden so aktualisiert, dass Sie den modernen Browserversionen entsprechen.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"" lightbox="../../images/2019/12/useragent.msft.png":::
   Das Menü "Benutzer-Agent" auf der Registerkarte " **Netzwerkbedingungen** "  
:::image-end:::  

Um auf **Netzwerkbedingungen**zuzugreifen, [Öffnen Sie das Befehlsmenü][DevToolsCommandMenuIndex] , und führen Sie den `Show Network Conditions` Befehl aus.  

> [!NOTE]
> Sie können auch [Benutzer-Agent-Zeichenfolgen im Gerätemodus einrichten][DevToolsDeviceModeIndex].  

Chrom Problem [#1029031][CR1029031]  

### Audits-Panel-Updates  

#### Neue Konfigurations-UI  

Die Benutzeroberfläche der Konfiguration verfügt über ein neues, reaktionsfähiges Design, und die Optionen für die Einschränkungs Konfiguration wurden vereinfacht.  Weitere Informationen zu den Änderungen beim Einschränken der Benutzeroberfläche finden Sie unter [Drosselung des Überwachungs Panels][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Die neue Benutzeroberfläche für die Konfiguration" lightbox="../../images/2019/12/start.msft.png":::
   Die neue Benutzeroberfläche für die Konfiguration  
:::image-end:::  

### Updates für Coverage-Registerkarten  

#### Pro-Funktion-oder pro-Block-Abdeckungs Modi  

Die [Registerkarte Coverage][DevToolsCoverageIndex] enthält ein neues Dropdownmenü, in dem Sie angeben können, ob Codeabdeckungsdaten **pro Funktion** oder **pro Block**erfasst werden sollen.  **Pro-Block** -Abdeckung ist detaillierter, aber auch weitaus teurer zu sammeln.  DevTools verwendet jetzt standardmäßig **pro Funktion** Coverage.  

> [!CAUTION]
> Je nachdem, ob Sie **pro Funktion** oder **pro Block** Modus verwenden, werden möglicherweise große Unterschiede bei der Codeabdeckung in HTML-Dateien angezeigt.  Bei Verwendung des **pro-Funktions** Modus werden Inlineskripts in HTML-Dateien als Funktionen behandelt.  Wenn das Skript überhaupt ausgeführt wird, markiert devtools das gesamte Skript als verwendeten Code.  Nur wenn das Skript überhaupt nicht ausgeführt wird, kennzeichnet devtools das Skript als unbenutzten Code.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Dropdownmenü "Coverage-Modus"" lightbox="../../images/2019/12/modes.msft.png":::
   Dropdownmenü "Coverage-Modus"  
:::image-end:::  

#### Coverage muss nun durch ein Seiten-Reload initiiert werden  

Das Umschalten der Codeabdeckung ohne das erneute Laden einer Seite wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.  Beispielsweise kann eine Funktion als unbenutzt gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector Sie bereinigt hat.  

Chrom Problem [#1004203][CR1004203]  

## Herunterladen der Microsoft Edge Preview-Kanäle  

Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.  Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie ungenutzten JavaScript-und CSS-Code mit der Registerkarte Coverage in Microsoft Edge devtools | Microsoft docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools | Microsoft docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalyse Referenz | Microsoft docs"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Neuerungen in EdgeHTML | Microsoft docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Debugger für Microsoft Edge Visual Studio-Code Erweiterung | Microsoft docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elemente für Microsoft Edge Visual Studio-Code Erweiterung | Microsoft docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Hinzufügen des Felds "Initiator" zur Registerkarte "Überschriften" | Chrom Fehler"  
[CR988253]: https://crbug.com/988253 "Fehler devtools-keine Zuordnung zwischen Netzwerkanforderung und Zeitachsendiagramm | Chrom Fehler"  
[CR993366]: https://crbug.com/993366 "Bitte zeigen Sie den Pfad Teil der URL in der Liste der Netzwerk Panel-Anfragen an | Chrom Fehler"  
[CR1004193]: https://crbug.com/1004193 "REPL-Modus für V8 | Chrom Fehler"  
[CR1004203]: https://crbug.com/1004203 "Erstellen von Code Coverage awesome | Chrom Fehler"  
[CR1029031]: https://crbug.com/1029031 "UA-Zeichenfolgen werden veraltet | Chrom Fehler" 
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatibel | Chrom Fehler"
[CR941561]: https://crbug.com/941561 "Lokalisierbarkeit der devtools | Chrom Fehler"
[CR987787]: https://crbug.com/987787 "Dom 3D-Ansicht | Chrom Fehler"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Einblicke in die Barrierefreiheit"  

[DwarfHome]: https://dwarfstd.org "Zwerge-Startseite"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools ' Audits Panel Drosselung-GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge – Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview-Kanäle"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider-Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Debuggen von JavaScript in Microsoft Edge in Visual Studio | Visual Studio-Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Herunterladen von Visual Studio 2019 für Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Dokumentobjektmodell (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio-Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Debugger für Microsoft Edge – Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elemente für Microsoft Edge \ (Chrom \) – Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint – Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint-Browser Erweiterung | webhint-Dokumentation"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio-Code Erweiterung | webhint-Dokumentation"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der nach Verfolgungs Vorbeugung in Microsoft Edge-Blogbeitrag"
[TheWebWeWant]: https://aka.ms/webwewant "Das gewünschte Web"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2019/12/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
