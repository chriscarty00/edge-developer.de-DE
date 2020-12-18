---
description: Einführung in die Microsoft Edge-Entwicklertools (EdgeHTML)
title: Microsoft Edge-Entwicklertools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233809"
---
# Microsoft Edge-Entwicklertools (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

Die Microsoft Edge\(EdgeHTML\) DevTools basieren auf [TypeScript][|::ref1::|Index], werden von [Open-Source][GithubMicrosoftChakracore] unterstützt, sind für moderne Front-End-Workflows optimiert und jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbar.  

Wenn Sie mehr über die neuesten Funktionen erfahren möchten, lesen Sie [DevTools in der neuesten Version von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Grundlegende Tools  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Die Microsoft Edge \(EdgeHTML\) DevTools umfassen:  

*   Einen Bereich [Elemente][DevtoolsGuideEdgehtml|::ref2::|] zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignis-Listenern und Festlegen von Haltepunkten für DOM-Mutationen  
*   Eine [Konsole][DevtoolsGuideEdgehtml|::ref3::|] zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens  
*   Einen [Debugger][DevtoolsGuideEdgehtml|::ref4::|] zum Durchlaufen von Code, Einstellen von Uhren und Haltepunkten, Livebearbeiten von Code und Überprüfen Ihrer Webspeicher- und Cookie-Caches  
*   Einen Bereich [Netzwerk][DevtoolsGuideEdgehtml|::ref5::|] zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache  
*   Einen Bereich [Leistung][DevtoolsGuideEdgehtml|::ref6::|], um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind  
*   Einen Bereich [Arbeitsspeicher][DevtoolsGuideEdgehtml|::ref7::|] zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Zuständen der Code-Runtime  
*   Einen Bereich [Speicher][DevtoolsGuideEdgehtml|::ref8::|] zum Überprüfen und Verwalten Ihres Webspeichers, Ihrer IndexedDB, Ihrer Cookies und Ihrer Cachedaten  
*   Einen Bereich [Dienstmitarbeiter][DevtoolsGuideEdgehtmlServiceworkers] zum Verwalten und Debuggen Ihrer Servicemitarbeiter  
*   Einen Bereich [Emulation][DevtoolsGuideEdgehtml|::ref9::|] zum Testen Ihrer Website mit unterschiedlichen Browserprofilen, Bildschirmauflösungen und GPS-Positionskoordinaten  

Bitte senden Sie weiterhin [Feedback und Feature-Anfragen](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [!TIP]
> [Testen Sie auf Microsoft Edge \(EdgeHTML\) kostenlos mit jedem Browser][BrowserstackEdgehtml].  
> Das Microsoft Edge-Team hat sich mit [BrowserStack][BrowserstackEdgehtml] zusammengetan, um ﻿kostenlose Live- und automatisierte Tests auf Microsoft Edge bereitzustellen. \(EdgeHTML \).  

## Microsoft Store-App  

Die **Microsoft Edge \(EdgeHTML\) DevTools** sind [jetzt][DevtoolsGuideEdgehtmlWhatsnew] als eigenständige [Windows 10-App im Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview] erhältlich, und zwar zusätzlich zur browserabhängigen \(`F12`\) Tooling-Oberfläche.  Die Store-Version enthält einen Bereich **Auswahl** zum Anfügen an geöffnete lokale und remote Seitenziele und ein Layout im Registerkartenformat für den einfachen Wechsel zwischen DevTools-Instanzen.  

### Lokales Debugging  

Um eine Seite lokal zu debuggen, starten Sie einfach die Microsoft Edge DevTools-App.  Im Bereich **Lokal** der Auswahl werden alle aktiven EdgeHTML-Inhaltsprozesse angezeigt, einschließlich der geöffneten Edge-Browser-Registerkarten, in denen [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe`-Prozesse\) und [WebView][HostingWebview]-Steuerelemente ausgeführt werden.  Wählen Sie das Ziel, das angehängt werden soll, und öffnen Sie eine neue Registerkarten-Instanz der DevTools.  

:::image type="complex" source=".//media/chooser_local.png" alt-text="DevTools-App, Bereich "Lokal"":::
   DevTools-App, Bereich "Lokal"
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Remotedebugging  

Die Microsoft Edge DevTools-App bietet grundlegende Unterstützung beim Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].  Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionen der Bereiche [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elemente][DevtoolsGuideEdgehtml|::ref11::|] \(für schreibgeschützte Vorgänge\) und [Konsole][DevtoolsGuideEdgehtml|::ref12::|] bereitgestellt.  Das Remote-Debugging ist auf Microsoft Edge \(EdgeHTML\), auf dem Desktop-Hosts ausgeführt werden, begrenzt und unterstützt andere EdgeHTML-Hosts und Windows 10-Geräte, die mit zukünftigen Versionen verfügbar sind.  

Lesen Sie zu Beginn den Abschnitt [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der Dokumente [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./media/chooser_remote.png" alt-text="DevTools-App, Bereich "Remote"":::
   DevTools-App, Bereich "Remote"
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Allgemeine Tastenkombinationen  

> [!IMPORTANT]
> Alle Tastenkombinationen wurden in der aktuellen Windows-Version überprüft.  
> Wenn Sie eine Tastenkombination nicht verwenden können, aktualisieren Sie Ihre Windows-Version.  

Mit diesen Tastenkombinationen wird das DevTools-Hauptfenster gesteuert, und sie sollten bei allen Tools funktionieren.  

| Aktion | Tastenkombination |  
|:--- |:--- |  
| DevTools ein-/ausblenden\(zuletzt angezeigter Bereich wird geöffnet\) | `F12`, `Ctrl`+`Shift`+`I` |  
| Docking umschalten \(Ausdocken/Unten/Rechts\) | `Ctrl`+`Shift`+`D` |  
| Datei öffnen | `Ctrl`+`P`, `Ctrl`+`O` |  
| Nicht bearbeitbaren HTML-Quellcode im Debugger anzeigen | `Ctrl`+`U` |  
| Konsole am unteren Rand eines beliebigen anderen Tools ein-/ausblenden  | `Ctrl`+`` ` `` |  
| Zu Elementen wechseln \(DOM-Explorer\) | `Ctrl`+`1` |  
| Zu Konsole wechseln |  `Ctrl`+`2` |  
| Zu Debugger wechseln | `Ctrl`+`3` |  
| Zu Netzwerk wechseln | `Ctrl`+`4` |  
| Zu Leistung wechseln | `Ctrl`+`5` |  
| Zu Arbeitsspeicher wechseln | `Ctrl`+`6` |  
| Zu Emulation wechseln | `Ctrl`+`7` |  
| Hilfedokument | `F1` |  
| Nächstes Tool | `Ctrl`+`F6` |  
| Vorheriges Tool | `Ctrl`+`Shift`+`F6` |  
| Vorheriges Tool \(aus Verlauf\) | `Ctrl`+`Shift`+`[` |  
| Nächstes Tool \(aus Verlauf\) | `Ctrl`+`Shift`+`]` |  
| Nächster Hilfsrahmen | `F6` |  
| Vorheriger Hilfsrahmen | `Shift`+`F6` |  
| Nächste Übereinstimmung im Suchfeld | `F3` |  
| Vorherige Übereinstimmung im Suchfeld | `Shift`+`F3` |  
| Über Suchfeld suchen | `Ctrl`+`F` |  
| Fokus auf Konsole unten richten | `Alt`+`Shift`+`I` |  
| DevTools in Konsole starten | `Ctrl`+`Shift`+`J` |  
| Seite aktualisieren | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Wenn Sie Debuggen und an einem Haltepunkt angehalten werden, setzen Sie zuerst mit der Aktion **Seite aktualisieren** die Laufzeit fort.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Bitte senden Sie uns Ihr Feedback, damit wir die Microsoft Edge \(EdgeHTML \) DevTools für Sie verbessern können!  Öffnen Sie einfach die Tools \(`F12`\), und wählen Sie die Schaltfläche [Feedback senden](#microsoft-edge-edgehtml-developer-tools) aus.  

Werden Sie [Windows-Insider][WindowsInsiderProgram], um die [neuesten Funktionen der DevTools][DevtoolsGuideEdgehtmlWhatsnew] in der Vorschau anzuzeigen.  Verwenden Sie die Windows Feedback-Hub-App, um allgemeine Vorschläge und Probleme in Bezug auf Windows zu posten, zu empfehlen zu verfolgen oder Hilfe zu erhalten.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Konsole"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Debugger"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elemente"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Arbeitsspeicher"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Netzwerk"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Leistung"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Dienstmitarbeiter"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Speicher"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools im neuesten Windows 10-Update (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Microsoft Edge (EdgeHTML) DevTools Protocol"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools-Vorschau – DevTools-Protokoll-Clients"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) für Windows 10-Apps"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Progressive Web Apps (EdgeHTML) unter Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools-Vorschau"  

[WindowsInsiderProgram]: https://insider.windows.com "Windows-Insider-Programm"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Kostenlose Microsoft Edge-Browser-Tests | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
