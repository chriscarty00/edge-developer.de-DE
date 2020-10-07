---
description: Einführung in die Microsoft Edge-Entwicklertools (EdgeHTML)
title: Microsoft Edge-Entwicklertools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
experimental: true
experiment_id: 51fe4b97-3e55-41
ms.localizationpriority: high
ms.openlocfilehash: 0c01b761d1aa1fb645b15b0be5d5d6e4265e646e
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10985968"
---
# Microsoft Edge-Entwicklertools (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Die Microsoft Edge\(EdgeHTML\) DevTools basieren auf [TypeScript][|::ref1::|Index], werden von [Open-Source][GithubMicrosoftChakracore] unterstützt, sind für moderne Front-End-Workflows optimiert und jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbar.  

Wenn Sie mehr über die neuesten Funktionen erfahren möchten, lesen Sie [DevTools in der neuesten Version von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Grundlegende Tools  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
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

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Microsoft Edge (EdgeHTML) DevTools"
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Remotedebugging  

Die Microsoft Edge DevTools-App bietet grundlegende Unterstützung beim Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].  Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionen der Bereiche [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elemente][DevtoolsGuideEdgehtml|::ref11::|] \(für schreibgeschützte Vorgänge\) und [Konsole][DevtoolsGuideEdgehtml|::ref12::|] bereitgestellt.  Das Remote-Debugging ist auf Microsoft Edge \(EdgeHTML\), auf dem Desktop-Hosts ausgeführt werden, begrenzt und unterstützt andere EdgeHTML-Hosts und Windows 10-Geräte, die mit zukünftigen Versionen verfügbar sind.  

Lesen Sie zu Beginn den Abschnitt [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der Dokumente [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Microsoft Edge (EdgeHTML) DevTools"  
