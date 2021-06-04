---
description: Verbesserungen bei der Barrierefreiheit mithilfe der DevTools in anderen Sprachen und mehr.
title: Neues in DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 58e5bf43720c7ba94a721804eb44d82ba657b599
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564994"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a>Neues in DevTools (Microsoft Edge 80)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Ankündigungen des Microsoft Edge DevTools-Teams  

Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom DevTools-Microsoft Edge verpasst haben.  Sehen Sie sich die Ankündigungen an, um neue Features in den DevTools zu testen, Microsoft Visual Studio Codeerweiterungen und vieles mehr zu testen.  Laden Sie die Microsoft Edge-Vorschaukanäle herunter und folgen Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount] [um auf][MicrosoftEdgePreviewChannels] dem neuesten stand zu bleiben.  

### <a name="accessibility-improvements-to-the-devtools"></a>Verbesserungen bei der Barrierefreiheit der DevTools  

Das DevTools-Team hat 170 Änderungen an Chromium, um probleme mit hohem Farbkontrast, Tastatur und Bildschirmleseprogramm in den DevTools zu beheben.  Jeder Entwickler, der das Web aufbaut, sollte die DevTools verwenden können.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Das Leistungstool in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   Das **Leistungstool** in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe  
:::image-end:::  

Möchten Sie erfahren, wie Sie ihre Webseite für alle Benutzer zugänglich machen?  Laden Sie [die Barrierefreiheits-Einblicke][AccessibilityInsights] und [Webhint-Erweiterungen][WebhintBrowserExtension] für Microsoft Edge, um zu beginnen.  

Wenn Sie Bildschirmlesegeräte oder die Tastatur verwenden, um [][PostTweetEdgeDevTools] die DevTools zu navigieren, senden Sie Ihr Feedback, indem Sie an uns twittern oder das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) drücken!  

Chromium Problem [#963183][CR963183]  

### <a name="using-the-devtools-in-other-languages"></a>Verwenden der DevTools in anderen Sprachen  

Viele Entwickler verwenden andere Entwicklertools, wie StackOverflow und Visual Studio Code, in ihrer eigenen Sprache, nicht nur in Englisch.  Wir freuen uns, die Lokalisierung für die DevTools ankündigen zu können, die Sie jetzt in einer von 10 Sprachen neben Englisch verwenden können:  

:::row:::
   :::column span="":::
      Chinesisch \(Vereinfacht\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinesisch \(Traditionell\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Französisch – fran&#231;ais
   :::column-end:::
   :::column span="":::
      Deutsch – deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italienisch - italiano
   :::column-end:::
   :::column span="":::
      Japanisch - &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Koreanisch - &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugiesisch – portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russisch – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Spanisch – espa&#241;ol
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

Navigieren Sie `edge://flags` zu, und legen Sie das **Flag Lokalisierte Entwicklertools aktivieren auf** Aktiviert **.**  Legen Sie außerdem das **Experiment-Flag Für Entwicklertools** auf **Aktiviert festgelegt.**  Starten Microsoft Edge, und öffnen Sie die DevTools.  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  Die DevTools entsprechen der Sprache, die Sie für Microsoft Edge in `edge://settings/languages` verwenden.  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="Die DevTools auf Deutsch" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   Die DevTools auf Deutsch  
:::image-end:::  

Wenn Sie devTools in einer anderen Sprache als die verfügbaren verwenden [möchten,][PostTweetEdgeDevTools] twittern Sie bei uns, oder wählen Sie das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) aus.  

Chromium Problem [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>webhint Microsoft Edge Erweiterung  

Mit der erweiterung webhint Microsoft Edge Können Sie Ihre Webseite ganz einfach überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und mehr innerhalb der DevTools erhalten.  Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Das Hints-Tool in devTools, wenn die Webhint-Browsererweiterung installiert ist" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   Das **Hints-Tool** in devTools, wenn die Webhint-Browsererweiterung installiert ist  
:::image-end:::  

[Testen Sie die Webhint-Browsererweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].  Öffnen Sie nach der Installation der Erweiterung die DevTools, und wählen Sie das **Hints-Tool** aus.  Führen Sie von hier aus eine anpassbare Websitescan aus.  Weitere Informationen finden [Webhint.io][WebhintBrowserExtension] sie.

### <a name="3d-view"></a>3D View  

Verwenden Sie **die 3D-Ansicht,** um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \(DOM\)][MDNDocumentObjectModel] oder den [Z-Index-Stapelkontext][MDNZIndex] navigieren.  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Die 3D-Ansicht in den DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   Die **3D-Ansicht** in den DevTools  
:::image-end:::  

Um auf die 3D-Ansicht zu zugreifen, navigieren Sie zu und stellen Sie sicher, dass das Experiment-Flag `edge://flags` **entwicklertools** auf **Aktiviert festgelegt ist.**  Starten Microsoft Edge, und öffnen Sie die DevTools.  Wählen Sie im Abschnitt DevTools aus, oder öffnen Sie den Abschnitt Einstellungen Experiments, und aktivieren Sie das `F1` ****  >  **** **Kontrollkästchen 3D-Ansicht** aktivieren.  Wählen Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht ein,** und wählen **Sie 3D-Ansicht anzeigen aus.**  

Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht weitere Funktionen hinzu, senden Sie uns ihr [Feedback.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium Problem [#987787][CR987787]

### <a name="visual-studio-code-extensions"></a>Visual Studio Code-Erweiterungen  

Das DevTools-Team hat auch [][VisualStudioCode] einige Erweiterungen für Visual Studio Code veröffentlicht, mit derEnt nen Sie die Leistung der DevTools direkt aus Ihrem Text-Editor nutzen können. Sehen Sie sich die folgenden Erweiterungen an.  

#### <a name="elements-for-microsoft-edge"></a>Elemente für Microsoft Edge  

Verwenden Sie das Elementtool aus Visual Studio Code, indem Sie die Erweiterung Elemente für Microsoft Edge [(Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code hinzufügen.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Das Elementtool in Visual Studio Code unter Verwendung der Erweiterung Elemente Microsoft Edge Erweiterung" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   Das **Elementtool** in Visual Studio Code die Erweiterung Elemente für Microsoft Edge verwenden  
:::image-end:::  

Weitere Informationen finden Sie unter [Elemente für Microsoft Edge Visual Studio Code Erweiterung][VisualStudioCodeElementEdgeExtension].  

#### <a name="debugger-for-microsoft-edge"></a>Debugger für Microsoft Edge  

Mit dem [Debugger für Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code Sie JavaScript debuggen, das in Microsoft Edge direkt von Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Der Debugger für Microsoft Edge Erweiterung in Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   Der Debugger für Microsoft Edge Erweiterung in Visual Studio Code  
:::image-end:::  

Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge von Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].  

#### <a name="webhint"></a>Webhint  

Die [Webhint Visual Studio Code-Erweiterung][VisualStudioMarketplaceWebhintExtension] verwendet, um Ihre Webseite zu verbessern, während Sie sie `webhint` schreiben! Diese Erweiterung wird ausgeführt und meldet Diagnosen für Ihre Arbeitsbereichsdateien basierend auf `webhint` der Analyse.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Das webhint-Visual Studio Code erweiterung, die eine TSX-Datei in einem Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   Das Webhint Visual Studio Code Erweiterung, die eine `.tsx` Datei in einem Visual Studio Code  
:::image-end:::  

[Erfahren Sie mehr über die Visual Studio Code Webhint-Erweiterung][WebhintVisualStudioCodeExtension].  

### <a name="visual-studio-integration"></a>Visual Studio Integration  

Verwenden Visual Studio 2019, Version 16.2 oder höher, den Visual Studio-Debugger, um JavaScript zu debuggen, das in Microsoft Edge.  [Laden Visual Studio 2019 herunter,][MicrosoftVisualStudioDownloads] um dieses Feature auszuprobieren.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta  
:::image-end:::  

[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge von Visual Studio.][MicrosoftVisualStudioBlogDebugJavascript]  

### <a name="tracking-prevention-console-messages"></a>Nachverfolgen von Nachrichten der Verhinderungskonsole  

Die Nachverfolgungsverhütung ist ein Microsoft Edge, das verhindert, dass Sie von einer Website nachverfolgt werden, bevor Sie sie besucht haben.  Die Standardeinstellung für die Nachverfolgungsverhütung ist der Balanced-Modus, der Drittanbieter-Tracker und bekannte bösartige Tracker blockiert, um datenschutz- und webkompatibilität zu gewährleisten.  Damit Sie mehr Einblick in die Kompatibilität Ihrer Webseite erhalten, wenn bestimmte Tracker blockiert werden, hat das Microsoft Edge-Team Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert wird. ****  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Nachrichten in der Konsole beim Nachverfolgen der Verhinderung blockiert den Zugriff auf speicher für einen Tracker" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Nachrichten in der **Konsole beim Nachverfolgen** der Verhinderung blockiert den Zugriff auf speicher für einen Tracker  
:::image-end:::  

[Lesen Sie mehr über die Nachverfolgung der Verhinderung und das Gleichgewicht zwischen Datenschutz und Webkompatibilität.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden zusätzliche features angekündigt, die in Microsoft Edge 80 verfügbar sind, die zum Open Source-Chromium wurden.  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a>Unterstützung von Let- und Klassen-Neudeklarationen in der Konsole  

Die **Konsole** unterstützt jetzt Neudeklarationen von `let` und `class` Anweisungen.  Die Unfähigkeit, eine erneute Deklaration zu erstellen, war für Webentwickler, die die Konsole verwenden, um mit neuem JavaScript-Code zu experimentieren, ein häufiges Unmut.  

> [!WARNING]
> Das erneute Deklarieren einer oder einer Anweisung in einem Skript außerhalb der Konsole oder innerhalb einer einzelnen Konsoleneingabe führt `let` `class` weiterhin zu einer `SyntaxError` .  

Beim erneuten Deklarieren einer lokalen Variablen mit hat die Konsole beispielsweise `let` zuvor einen Fehler ausgegeben:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Die Konsole in Microsoft Edge 79 zeigt an, dass die erneute Deklarierung fehlschlägt" lightbox="../../images/2019/12/letbefore.msft.png":::
   Die **Konsole** in Microsoft Edge 79 zeigt an, dass die erneute Deklaration fehlschlägt  
:::image-end:::  

Nun ermöglicht die Konsole die erneute Deklarierung:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Die Konsole in Microsoft Edge 80 zeigt an, dass die erneute Deklarierung erfolgreich ist." lightbox="../../images/2019/12/letafter.msft.png":::
   Die **Konsole** in Microsoft Edge 80 zeigt an, dass die erneute Deklaration erfolgreich ist  
:::image-end:::  

Chromium Problem [#1004193][CR1004193]  

### <a name="improved-webassembly-debugging"></a>Verbessertes WebAssembly-Debuggen  

DevTools hat damit begonnen, den STANDARD FÜR DAS DEBUGGEN ZU UNTERSTÜTZEN, was bedeutet, dass die Unterstützung für das Schrittweise Festlegen von Code, das Festlegen von Haltepunkten und das Auflösen von Stapelverfolgungen in Ihren Quellsprachen in DevTools erhöht wird.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a>Netzwerkbereichsupdates  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a>Anfordern von Initiatorketten im Initiatorbereich  

Sie können jetzt die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.  Dies hilft Ihnen möglicherweise zu verstehen, warum eine Ressource angefordert wurde oder welche Netzwerkaktivität eine bestimmte Ressource \(z. B. ein Skript\) verursacht hat.  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Eine Anforderungsinitiatorkette im Initiatorbereich" lightbox="../../images/2019/12/initiators.msft.png":::
   Eine Anforderungsinitiatorkette im **Initiatorbereich**  
:::image-end:::  

Wählen [Sie nach der][DevToolsNetworkIndex]Protokollierung der Netzwerkaktivität im Netzwerkbereich eine Ressource aus, und navigieren Sie dann zum Bereich **Initiator,** um die Anforderungsinitiatorkette **zu sehen:**  

*   Die **überprüfte Ressource ist** fett formatiert.  Im obigen Screenshot `ai.2.min.js` ist die überprüfte Ressource.  
*   Die Ressourcen über der überprüften Ressource sind die **Initiatoren.**  Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .  Mit anderen Worten, `https://www.microsoftedgeinsider.com` hat die Netzwerkanforderung für `ai.2.min.js` verursacht.  
*   Die Ressourcen unterhalb der überprüften Ressource sind **die Abhängigkeiten**.  Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .  Mit anderen Worten, `ai.2.min.js` hat die Netzwerkanforderung für `https://dc.services.visualstudio.com/v2/track` verursacht.  

> [!NOTE]
> Der Zugriff auf Initiator- und Abhängigkeitsinformationen kann auch durch Halten und anschließendes Zeigen `Shift` auf Netzwerkressourcen möglich sein.  Navigieren Sie zu [Initiatoren und Abhängigkeiten anzeigen.][DevToolsNetworkReferenceDisplayInitiatorsDependencies]  

Chromium Problem [#842488][CR842488]  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a>Hervorheben der ausgewählten Netzwerkanforderung in der Übersicht  

Nachdem Sie eine Netzwerkressource zum Überprüfen der Ressource auswählen, wird im Bereich Netzwerk nun ein blauer Rahmen um diese Ressource in der **Übersicht angezeigt.**  Dadurch können Sie erkennen, ob die Netzwerkanforderung früher oder später als erwartet vor sich geht.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Der Bereich Übersicht, in dem die überprüfte Ressource hervorgehoben wird" lightbox="../../images/2019/12/overview.msft.png":::
   Der **Bereich Übersicht,** in dem die überprüfte Ressource hervorgehoben wird  
:::image-end:::  

Chromium Problem [#988253][CR988253]  

#### <a name="url-and-path-columns-in-the-network-panel"></a>URL- und Pfadspalten im Netzwerkbereich  

Verwenden Sie die neuen **Pfad-** und **URL-Spalten** im **Netzwerktool,** um den absoluten Pfad oder die vollständige URL jeder Netzwerkressource anzuzeigen.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Die neuen Pfad- und URL-Spalten im Netzwerkbereich" lightbox="../../images/2019/12/columns.msft.png":::
   Die neuen Pfad- und URL-Spalten im **Netzwerktool**  
:::image-end:::  

Um die neuen Spalten anzuzeigen, zeigen Sie auf die **Kopfzeile der Wasserfalltabelle,** öffnen Sie das Kontextmenü \(righ-click\), und wählen Sie **Pfad** oder **URL aus.**  

Chromium Problem [#993366][CR993366]  

#### <a name="updated-user-agent-strings"></a>Aktualisierte User-Agent Zeichenfolgen  

DevTools unterstützt das Festlegen einer benutzerdefinierten User-Agent über den Bereich **Netzwerkbedingungen.**  Die User-Agent wirkt sich auf den an Netzwerkressourcen angefügten HTTP-Header und `User-Agent` auch auf den Wert von `navigator.userAgent` aus.  

Die vordefinierten User-Agent Zeichenfolgen wurden aktualisiert, um moderne Browserversionen wider zuspiegeln.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Das Menü Benutzer-Agent im Bereich Netzwerkbedingungen" lightbox="../../images/2019/12/useragent.msft.png":::
   Das Menü Benutzer-Agent im Bereich **Netzwerkbedingungen**  
:::image-end:::  

Öffnen Sie **zum Zugreifen auf**Netzwerkbedingungen das [Befehlsmenü,][DevToolsCommandMenuIndex] und führen Sie den Befehl `Show Network Conditions` aus.  

> [!NOTE]
> Sie können auch [User-Agent zeichenfolgen im Gerätemodus festlegen.][DevToolsDeviceModeIndex]  

Chromium Problem [#1029031][CR1029031]  

### <a name="audits-panel-updates"></a>Überwachung von Panelupdates  

#### <a name="new-configuration-ui"></a>Neue Konfigurationsbenutzeroberfläche  

Die Konfigurationsbenutzeroberfläche verfügt über ein neues, reaktionsfähiges Design, und die Konfigurationsoptionen für die Einschränkung wurden vereinfacht.  Weitere Informationen zu Den Änderungen der Einschränkungsbenutzeroberfläche finden Sie unter [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Die neue Konfigurationsbenutzeroberfläche" lightbox="../../images/2019/12/start.msft.png":::
   Die neue Konfigurationsbenutzeroberfläche  
:::image-end:::  

### <a name="coverage-tool-updates"></a>Updates des Abdeckungstools  

#### <a name="per-function-or-per-block-coverage-modes"></a>Funktions- oder Blockabdeckungsmodi  

Das [Coverage-Tool][DevToolsCoverageIndex] verfügt über ein neues Dropdownmenü, mit **** dem Sie angeben können, ob Codeabdeckungsdaten pro Funktion oder pro Block **erfasst werden sollen.**  **Die Abdeckung pro** Block ist detaillierter, aber auch viel teurer zu erfassen.  DevTools verwendet **jetzt standardmäßig die** Abdeckung pro Funktion.  

> [!CAUTION]
> Je nachdem, ob Sie pro Funktion oder **** pro Blockmodus verwenden, können Sie große Unterschiede bei der Codeabdeckung in **HTML-Dateien** feststellen.  Bei Verwendung **pro Funktionsmodus** werden Inlineskripts in HTML-Dateien als Funktionen behandelt.  Wenn das Skript überhaupt ausgeführt wird, markiert DevTools das gesamte Skript als verwendeten Code.  Nur wenn das Skript überhaupt nicht ausgeführt wird, markieren DevTools das Skript als nicht verwendeten Code.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Dropdownmenü Abdeckungsmodus" lightbox="../../images/2019/12/modes.msft.png":::
   Dropdownmenü "Abdeckungsmodus"  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a>Die Abdeckung muss jetzt durch eine Seitenaktualisierung initiiert werden.  

Die Toggling-Codeabdeckung ohne Seitenaktualisierung wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.  Beispielsweise kann eine Funktion als nicht verwendet gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector sie bereinigt hat.  

Chromium Problem [#1004203][CR1004203]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie sich auf Windows oder macOS befinden, sollten Sie die Microsoft Edge Vorschaukanäle [als][MicrosoftEdgePreviewChannels] Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Suchen Sie nicht verwendeten JavaScript- und CSS-Code mit dem Coverage-Tool in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: ../../../network/index.md "Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Debugger für Microsoft Edge Visual Studio Code Erweiterung | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elemente für Microsoft Edge Visual Studio Code Erweiterungserweiterungen | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Fügen Sie das Feld Initiator der Registerkarte Kopfzeilen | Chromium Bugs"  
[CR988253]: https://crbug.com/988253 "Bug DevTools – Keine Zuordnung zwischen Netzwerkanforderung und Zeitachsen-Graph | Chromium Bugs"  
[CR993366]: https://crbug.com/993366 "Bitte zeigen Sie den Pfadteil der URL in der Liste der Netzwerkpanelanforderungen | Chromium Bugs"  
[CR1004193]: https://crbug.com/1004193 "REPL-Modus für V8-| Chromium Bugs"  
[CR1004203]: https://crbug.com/1004203 "Machen Sie die Codeabdeckung | Chromium Bugs"  
[CR1029031]: https://crbug.com/1029031 "UA-Zeichenfolgen werden veraltet | Chromium Bugs" 
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium Bugs"
[CR941561]: https://crbug.com/941561 "Lokalisierbarkeit der DevTools-| Chromium Bugs"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Einblicke in die Barrierefreiheit"  

[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools' Audits Panel Throttling – GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Vorschaukanäle"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider-Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Debuggen von JavaScript in Microsoft Edge von Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Download Visual Studio 2019 für Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools, Twitter-Konto"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Debugger für Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elemente für Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint – Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | Webhintdokumentation"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code Extension | Webhintdokumentation"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der Nachverfolgungsverhütung in Microsoft Edge Blogbeitrag"
[TheWebWeWant]: https://aka.ms/webwewant "The Web We Want"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developer.chrome.com/blog/new-in-devtools-80) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
