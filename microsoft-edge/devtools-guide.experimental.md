---
description: Kennenlernen der Microsoft Edge-Entwickler Tools
title: Microsoft Edge-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 47b7a3f4f523170f4dfb6f3ef674cecfdc0e157c
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645329"
---
# Microsoft Edge-Entwickler Tools  

> [!NOTE]
> Die Microsoft Edge-devtools helfen Webentwicklern beim Erstellen und Testen von Websites.  Wenn Sie das devtools versehentlich geöffnet haben, drücken Sie einfach `F12` zum Schließen.  

Die Microsoft Edge-devtools [sind mit einer](https://www.typescriptlang.org/)von [Open Source](https://github.com/Microsoft/ChakraCore)unterstützten, für moderne Front-End-Workflows optimierten und jetzt als [eigenständige Windows 10-App](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) im Microsoft Store verfügbaren Version erstellt.

Weitere Informationen zu den neuesten Features finden Sie unter [*devtools im neuesten Update von Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Kern Tools

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

Die Microsoft Edge-devtools umfassen Folgendes:

 - Ein [**Element**](./devtools-guide/elements.md) Panel zum Bearbeiten von HTML und CSS, untersuchen von Barrierefreiheitseigenschaften, Anzeigen von ereignislistern und Festlegen von Haltepunkten für DOM-Mutationen
 - Eine [**Konsole**](./devtools-guide/console.md) zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens
 - Ein [**Debugger**](./devtools-guide/debugger.md) zum Durchlaufen von Code, Festlegen von Überwachungen und Haltepunkten, Live Bearbeiten des Codes und untersuchen der Webspeicher-und Cookie-Caches
 - [**Netzwerk**](./devtools-guide/network.md) Fenster zum Überwachen und prüfen von Anforderungen und Antworten aus dem Netzwerk-und Browsercache 
 - Ein [**Leistungs**](./devtools-guide/performance.md) Panel, in dem die von Ihrer Website benötigten Zeit-und Systemressourcen angezeigt werden
 - Ein [**Speicher**](./devtools-guide/memory.md) Panel, mit dem Sie die Verwendung von Speicherressourcen Messen und Heap-Schnappschüsse in verschiedenen Zuständen der Codeausführung vergleichen können
 - Ein [**Emulations**](./devtools-guide/emulation.md) Panel zum Testen Ihrer Website mit unterschiedlichen Browser Profilen, Bildschirmauflösungen und GPS-Positionskoordinaten

Bitte senden Sie Ihr [Feedback und ihre Funktionswünsche](#feedback)weiter!

> [!TIP]
> **[Testen Sie Microsoft Edge kostenlos in einem beliebigen Browser](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: Wir haben eine Partnerschaft mit [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) , um ﻿kostenlose Live-und automatisierte Tests für Microsoft Edge bereitzustellen.

## Microsoft Store-App

Die **Microsoft Edge-devtools** sind nun zusätzlich zur in-Browser ()-Tooling-Funktion [für die Vorschau](./devtools-guide/whats-new.md) als eigenständige [Windows 10-App aus dem Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab)verfügbar `F12` . Bei der Store-Version wird ein *Auswahl* Bereich für das Anfügen zum Öffnen von lokalen und Remote Seiten Zielen sowie ein Layout mit Registerkarten zum einfachen Umschalten zwischen devtools-Instanzen geliefert.

### Lokales Debuggen

Wenn Sie eine Seite lokal debuggen möchten, starten Sie einfach die *Microsoft Edge devtools* -app. Im **lokalen** Fenster des Auswahlfelds werden alle aktiven EdgeHTML-Inhalts Prozesse angezeigt, einschließlich der geöffneten Edge-Browser-Registerkarten, Ausführen von [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost. exe* -Prozesse) und [WebView](./webview.md) -Steuerelementen. Klicken Sie auf das gewünschte Ziel, um eine neue Registerkarten Instanz des devtools anzufügen und zu öffnen.

![Lokales Panel der devtools-App](./devtools-guide/media/chooser_local.png)

### Remote Debuggen

Die *Microsoft Edge devtools* -App bietet grundlegende Unterstützung für das Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [**devtools-Protokoll**](./devtools-protocol/index.md). Mit dieser Version wird der Remotezugriff auf Core Funktionalität im [**Debuggerfenster**](./devtools-guide/debugger.md) , abzüglich der Cache Überprüfung (für Web Storage, Service Worker, Cache-API und IndexedDB), bereit stehen. Das Remote Debuggen ist auf *Microsoft Edge* mit *Desktop* Hosts und Unterstützung für andere EdgeHTML-Hosts und Windows 10-Geräte in zukünftigen Versionen limitiert.

Um zu beginnen, lesen Sie den Abschnitt [*Microsoft Edge devtools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) der [devtools-Protokoll](./devtools-protocol/index.md) Dokumentation.

![DevTools-App-Remote Panel](./devtools-guide/media/chooser_remote.png)

## Feedback senden

Bitte senden Sie uns Ihr Feedback, damit wir die Microsoft Edge-devtools für Sie weiter verbessern können. Öffnen Sie einfach die Tools ( `F12` ) und klicken Sie auf die Schaltfläche [**Feedback senden**](#microsoft-edge-developer-tools) .

Sie können auch Tooling-Anfragen zu unserem [UserVoice-Forum](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) hinzufügen und upvoten und zu einem [Windows-Insider](https://insider.windows.com/) werden, der die [neuesten Funktionen in der devtools](./devtools-guide/whats-new.md)-Ansicht zeigt. Verwenden Sie die Windows- **Feedback-Hub** -APP, um für allgemeine Windows-Vorschläge und-Probleme Beiträge zu senden, zu überwachen und Support zu erhalten.

## Allgemeine Tastenkombinationen

Diese Tastenkombinationen steuern das Hauptfenster von devtools und/oder Arbeiten über alle Tools hinweg.

Aktion | Tastenkombination
:------------ | :-------------
Einblenden/Ausblenden von devtools (wird zum zuletzt angezeigten Fenster geöffnet) | F12, STRG + UMSCHALT + I
Umschalten der Docking-Station (Abdocken/unten/rechts) | STRG + UMSCHALT + D 
Anzeigen des nicht bearbeitbaren HTML-Quellcodes im Debugger | STRG + U
Konsole am unteren Rand eines beliebigen anderen Tools einblenden/ausblenden  | STRG +**`**
Wechseln zu Elementen (DOM-Explorer) | STRG + 1
Zur Konsole wechseln |  STRG + 2
Wechseln zu Debugger | STRG + 3
Zum Netzwerk wechseln | STRG + 4
Wechseln zur Leistung | STRG + 5
Wechseln zum Arbeitsspeicher | STRG + 6
Wechseln zur Emulation | Strg + 7
Hilfedokument | F1
Nächstes Tool | STRG + F6
Vorheriges Tool | STRG + UMSCHALT + F6
Vorheriges Tool (aus Verlauf) | STRG + UMSCHALT + [
Nächstes Tool (aus Verlauf) | STRG + UMSCHALT +]
Nächster teilframe    | F6
Vorheriger teilframe | UMSCHALT + F6
Nächste Übereinstimmung im Suchfeld | F3
Vorherige Übereinstimmung im Suchfeld | UMSCHALTTASTE+F3
Suchen im Suchfeld | STRG+F
Konzentrieren Sie sich am unteren Rand auf die Konsole. | ALT + UMSCHALT + I
Andocken/Abdocken von Tools (Umschalten) | STRG+P  
Starten von devtools to Console | STRG + UMSCHALT + J
Aktualisieren Sie die Seite. **Hinweis:** Wenn Sie Debuggen und an einem Haltepunkt angehalten haben, wird die Ausführung zuerst fortgesetzt. | STRG + UMSCHALT + F5 oder STRG + R
