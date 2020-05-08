---
description: Kennenlernen der Microsoft Edge-Entwickler Tools (EdgeHTML)
title: Microsoft Edge (EdgeHTML)-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629504"
---
# Microsoft Edge (EdgeHTML)-Entwickler Tools  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Die Microsoft Edge \ (EdgeHTML \) devtools [sind mit einer][|::ref1::|Index]von [Open Source][GithubMicrosoftChakracore]unterstützten, für moderne Front-End-Workflows optimierten und jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbaren Version erstellt.  

Weitere Informationen zu den neuesten Features finden Sie unter [devtools im neuesten Update von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Kern Tools  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) devtools":::
   Microsoft Edge (EdgeHTML) devtools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Zu den Microsoft Edge \ (EdgeHTML \) devtools gehören:  

*   Ein [Element][DevtoolsGuideEdgehtml|::ref2::|] Panel zum Bearbeiten von HTML und CSS, untersuchen von Barrierefreiheitseigenschaften, Anzeigen von ereignislistern und Festlegen von Haltepunkten für DOM-Mutationen  
*   Eine [Konsole][DevtoolsGuideEdgehtml|::ref3::|] zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens  
*   Ein [Debugger][DevtoolsGuideEdgehtml|::ref4::|] zum Durchlaufen von Code, Festlegen von Überwachungen und Haltepunkten, Live Bearbeiten des Codes und untersuchen der Webspeicher-und Cookie-Caches  
*   [Netzwerk][DevtoolsGuideEdgehtml|::ref5::|] Fenster zum Überwachen und prüfen von Anforderungen und Antworten aus dem Netzwerk-und Browsercache  
*   Ein [Leistungs][DevtoolsGuideEdgehtml|::ref6::|] Panel, in dem die von Ihrer Website benötigten Zeit-und Systemressourcen angezeigt werden  
*   Ein [Speicher][DevtoolsGuideEdgehtml|::ref7::|] Panel zum Messen der Verwendung von Speicherressourcen und zum Vergleichen von Heap-Snapshots in verschiedenen Zuständen der Code Laufzeit  
*   Ein [Speicher][DevtoolsGuideEdgehtml|::ref8::|] Panel zum Überprüfen und Verwalten Ihres Webspeichers, IndexedDB, Cookies und Cache-Daten  
*   Ein [Dienstmitarbeiter][DevtoolsGuideEdgehtmlServiceworkers] -Panel zum Verwalten und Debuggen von Servicemitarbeitern  
*   Ein [Emulations][DevtoolsGuideEdgehtml|::ref9::|] Panel zum Testen Ihrer Website mit unterschiedlichen Browser Profilen, Bildschirmauflösungen und GPS-Positionskoordinaten  

Bitte senden Sie Ihr [Feedback und ihre Funktionswünsche](#feedback)weiter!  

> [!TIP]
> [Testen Sie Microsoft Edge \ (EdgeHTML \) kostenlos in einem beliebigen Browser][BrowserstackEdgehtml].  
> Das Microsoft Edge-Team hat sich mit [BrowserStack][BrowserstackEdgehtml] zusammengetan, um ﻿kostenlose Live-und automatisierte Tests für Microsoft Edge (EdgeHTML \) bereitzustellen.  

## Microsoft Store-App  

Die **Microsoft Edge \ (EdgeHTML \)-devtools** sind nun als eigenständige [Windows 10-App aus dem Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview]sowie über die in-Browser`F12`-Tooling-Umgebung [verfügbar][DevtoolsGuideEdgehtmlWhatsnew] .  Bei der Store-Version wird ein **Auswahl** Bereich für das Anfügen zum Öffnen von lokalen und Remote Seiten Zielen sowie ein Layout mit Registerkarten zum einfachen Umschalten zwischen devtools-Instanzen geliefert.  

### Lokales Debuggen  

Wenn Sie eine Seite lokal debuggen möchten, starten Sie einfach die Microsoft Edge devtools-app.  Der **lokale** Teil des Auswahlfelds zeigt alle aktiven EdgeHTML-Inhalts Prozesse an, einschließlich der geöffneten Edge-Browser-Register [PWAs][PwasEdgehtmlIndex] Karten, mit`WWAHost.exe` PWAs \ (Prozesse \) und [WebView][HostingWebview] -Steuerelementen.  Wählen Sie das gewünschte Ziel aus, um eine neue Registerkarten Instanz des devtools anzufügen und zu öffnen.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Lokales Panel der devtools-App":::
   Lokales Panel der devtools-App
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Remote Debuggen  

Die Microsoft Edge devtools-App bietet grundlegende Unterstützung für das Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [devtools-Protokoll][DevtoolsProtocolEdgehtmlIndex].  Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionalität des [Debuggers][DevtoolsGuideEdgehtml|::ref10::|], [Elemente][DevtoolsGuideEdgehtml|::ref11::|] \ (für schreibgeschützte Vorgänge \) und [Konsolen][DevtoolsGuideEdgehtml|::ref12::|] Panels ausgeführt.  Das Remote Debuggen ist auf Microsoft Edge \ (EdgeHTML \), auf dem Desktop Hosts ausgeführt werden, mit Unterstützung für andere EdgeHTML-Hosts und Windows 10-Geräte in zukünftigen Versionen limitiert.  

Um zu beginnen, lesen Sie den Abschnitt [*Microsoft Edge devtools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der [devtools-Protokoll][DevtoolsProtocolEdgehtmlIndex] Dokumentation.  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="DevTools-App-Remote Panel":::
   DevTools-App-Remote Panel
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Allgemeine Tastenkombinationen  

> [!IMPORTANT]
> Alle Tastenkombinationen wurden in der neuesten Version von Windows überprüft.  
> Wenn Sie eine Verknüpfung nicht verwenden können, aktualisieren Sie Ihre Kopie von Windows.  

Diese Tastenkombinationen steuern das Hauptfenster von devtools und sollten über alle Tools hinweg funktionieren.  

| Aktion | Tastenkombination |  
|:--- |:--- |  
| DevTools anzeigen/ausblenden \ (wird zum zuletzt angezeigten Fenster geöffnet) | `F12`, `Ctrl`+`Shift`+`I` |  
| Umschalten der Docking-Taste \ (Abdocken/unten/rechts \) | `Ctrl`+`Shift`+`D` |  
| Datei öffnen | `Ctrl`+`P`, `Ctrl`+`O` |  
| Anzeigen des nicht bearbeitbaren HTML-Quellcodes im Debugger | `Ctrl`+`U` |  
| Konsole am unteren Rand eines beliebigen anderen Tools einblenden/ausblenden  | `Ctrl`+`` ` `` |  
| Wechseln zu Elementen \ (DOM-Explorer \) | `Ctrl`+`1` |  
| Zur Konsole wechseln |  `Ctrl`+`2` |  
| Wechseln zu Debugger | `Ctrl`+`3` |  
| Zum Netzwerk wechseln | `Ctrl`+`4` |  
| Wechseln zur Leistung | `Ctrl`+`5` |  
| Wechseln zum Arbeitsspeicher | `Ctrl`+`6` |  
| Wechseln zur Emulation | `Ctrl`+`7` |  
| Hilfedokument | `F1` |  
| Nächstes Tool | `Ctrl`+`F6` |  
| Vorheriges Tool | `Ctrl`+`Shift`+`F6` |  
| Vorheriges Tool \ (aus Verlauf \) | `Ctrl`+`Shift`+`[` |  
| Nächstes Tool \ (aus Verlauf \) | `Ctrl`+`Shift`+`]` |  
| Nächster teilframe | `F6` |  
| Vorheriger teilframe | `Shift`+`F6` |  
| Nächste Übereinstimmung im Suchfeld | `F3` |  
| Vorherige Übereinstimmung im Suchfeld | `Shift`+`F3` |  
| Suchen im Suchfeld | `Ctrl`+`F` |  
| Konzentrieren Sie sich am unteren Rand auf die Konsole. | `Alt`+`Shift`+`I` |  
| Starten von devtools to Console | `Ctrl`+`Shift`+`J` |  
| Seite aktualisieren | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Wenn Sie das Debuggen durchgeführt und an einem Haltepunkt angehalten haben, setzt die Aktion **Seite aktualisieren** die Laufzeit zuerst fort.  

## Feedback senden  

Bitte senden Sie Ihr Feedback, damit Sie die Microsoft Edge \ (EdgeHTML \) devtools für Sie verbessern können.  Öffnen Sie einfach die Tools \`F12`(\), und wählen Sie die Schaltfläche [Feedback senden](#microsoft-edge-edgehtml-developer-tools) aus.  

Werden Sie [Windows-Insider][WindowsInsiderProgram] , um eine Vorschau der [neuesten Features in devtools][DevtoolsGuideEdgehtmlWhatsnew]anzuzeigen.  Verwenden Sie die Windows-Feedback-Hub-App zum Posten, nach oben abstimmen, Nachverfolgung und Support für allgemeine Windows-Vorschläge und-Probleme.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Konsole"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Debugger"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elemente"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Speicher"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Netzwerk"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Leistung"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Dienstmitarbeiter"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Speicher"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools im neuesten Windows 10-Update (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Microsoft Edge (EdgeHTML) devtools-Protokoll"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) für Windows 10-apps"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Progressive Web-Apps (EdgeHTML) unter Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge devtools Preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Windows-Insider-Programm"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Testen des Microsoft Edge-Browsers kostenlos | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
