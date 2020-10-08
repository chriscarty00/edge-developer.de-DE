---
description: Kennenlernen der Microsoft Edge-Entwickler Tools
title: Microsoft Edge-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986220"
---
# Microsoft Edge-Entwickler Tools  

> [!NOTE]
> Die Microsoft Edge-devtools helfen Webentwicklern beim Erstellen und Testen von Websites.  Wenn Sie das devtools versehentlich geöffnet haben, drücken Sie einfach `F12` zum Schließen.  

Die Microsoft Edge-devtools [sind mit einer](https://www.typescriptlang.org/)von [Open Source](https://github.com/Microsoft/ChakraCore)unterstützten, für moderne Front-End-Workflows optimierten und jetzt als [eigenständige Windows 10-App](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) im Microsoft Store verfügbaren Version erstellt.

Weitere Informationen zu den neuesten Features finden Sie unter [*devtools im neuesten Update von Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Grundlegende Tools

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

Die Microsoft Edge-devtools umfassen Folgendes:

 - Ein [**Element**](./devtools-guide/elements.md) Panel zum Bearbeiten von HTML und CSS, untersuchen von Barrierefreiheitseigenschaften, Anzeigen von ereignislistern und Festlegen von Haltepunkten für DOM-Mutationen
 - Eine [**Konsole**](./devtools-guide/console.md) zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens
 - Ein [**Debugger**](./devtools-guide/debugger.md) zum Durchlaufen von Code, Festlegen von Überwachungen und Haltepunkten, Live Bearbeiten des Codes und untersuchen der Webspeicher-und Cookie-Caches
 - [**Netzwerk**](./devtools-guide/network.md) Fenster zum Überwachen und prüfen von Anforderungen und Antworten aus dem Netzwerk-und Browsercache 
 - Ein [**Leistungs**](./devtools-guide/performance.md) Panel, in dem die von Ihrer Website benötigten Zeit-und Systemressourcen angezeigt werden
 - Ein [**Speicher**](./devtools-guide/memory.md) Panel, mit dem Sie die Verwendung von Speicherressourcen Messen und Heap-Schnappschüsse in verschiedenen Zuständen der Codeausführung vergleichen können
 - Ein [**Emulations**](./devtools-guide/emulation.md) Panel zum Testen Ihrer Website mit unterschiedlichen Browser Profilen, Bildschirmauflösungen und GPS-Positionskoordinaten

Bitte senden Sie Ihre [Feedback-und Funktionswünsche](#getting-in-touch-with-the-microsoft-edge-devtools-team)weiter.

> [!TIP]
> **[Testen Sie Microsoft Edge kostenlos in einem beliebigen Browser](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: Wir haben eine Partnerschaft mit [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) , um ﻿kostenlose Live-und automatisierte Tests für Microsoft Edge bereitzustellen.

## Microsoft Store-App

Die **Microsoft Edge-devtools** sind nun zusätzlich zur in-Browser ()-Tooling-Funktion [für die Vorschau](./devtools-guide/whats-new.md) als eigenständige [Windows 10-App aus dem Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab)verfügbar `F12` . Die Store-Version enthält einen Bereich *Auswahl* zum Anfügen an geöffnete lokale und remote Seitenziele und ein Layout im Registerkartenformat für den einfachen Wechsel zwischen DevTools-Instanzen.

### Lokales Debugging

Wenn Sie eine Seite lokal debuggen möchten, starten Sie einfach die *Microsoft Edge devtools* -app. Im **lokalen** Fenster des Auswahlfelds werden alle aktiven EdgeHTML-Inhalts Prozesse angezeigt, einschließlich der geöffneten Edge-Browser-Registerkarten, Ausführen von [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* Prozesse) und [WebView](./webview.md) -Steuerelementen. Klicken Sie auf das gewünschte Ziel, um eine neue Registerkarten Instanz des devtools anzufügen und zu öffnen.

![DevTools-App, Bereich "Lokal"](./devtools-guide/media/chooser_local.png)

### Remotedebugging

Die *Microsoft Edge devtools* -App bietet grundlegende Unterstützung für das Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [**devtools-Protokoll**](./devtools-protocol/index.md). Mit dieser Version wird der Remotezugriff auf Core Funktionalität im [**Debuggerfenster**](./devtools-guide/debugger.md) , abzüglich der Cache Überprüfung (für Web Storage, Service Worker, Cache-API und IndexedDB), bereit stehen. Das Remote Debuggen ist auf *Microsoft Edge* mit *Desktop* Hosts und Unterstützung für andere EdgeHTML-Hosts und Windows 10-Geräte in zukünftigen Versionen limitiert.

Lesen Sie zu Beginn den Abschnitt [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) der Dokumente [DevTools-Protokoll](./devtools-protocol/index.md).

![DevTools-App, Bereich "Remote"](./devtools-guide/media/chooser_remote.png)

## Allgemeine Tastenkombinationen

Diese Tastenkombinationen steuern das Hauptfenster von devtools und/oder Arbeiten über alle Tools hinweg.

Aktion | Tastenkombination
:------------ | :-------------
Einblenden/Ausblenden von devtools (wird zum zuletzt angezeigten Fenster geöffnet) | F12, STRG + UMSCHALT + I
Umschalten der Docking-Station (Abdocken/unten/rechts) | STRG + UMSCHALT + D 
Nicht bearbeitbaren HTML-Quellcode im Debugger anzeigen | STRG + U
Konsole am unteren Rand eines beliebigen anderen Tools ein-/ausblenden  | STRG +**`**
Wechseln zu Elementen (DOM-Explorer) | STRG + 1
Zu Konsole wechseln |  STRG + 2
Zu Debugger wechseln | STRG + 3
Zu Netzwerk wechseln | STRG + 4
Zu Leistung wechseln | STRG + 5
Zu Arbeitsspeicher wechseln | STRG + 6
Zu Emulation wechseln | Strg + 7
Hilfedokument | F1
Nächstes Tool | STRG + F6
Vorheriges Tool | STRG + UMSCHALT + F6
Vorheriges Tool (aus Verlauf) | STRG + UMSCHALT + [
Nächstes Tool (aus Verlauf) | STRG + UMSCHALT +]
Nächster Hilfsrahmen    | F6
Vorheriger Hilfsrahmen | UMSCHALT + F6
Nächste Übereinstimmung im Suchfeld | F3
Vorherige Übereinstimmung im Suchfeld | UMSCHALTTASTE+F3
Über Suchfeld suchen | STRG+F
Fokus auf Konsole unten richten | ALT + UMSCHALT + I
Andocken/Abdocken von Tools (Umschalten) | STRG+P  
DevTools in Konsole starten | STRG + UMSCHALT + J
Aktualisieren Sie die Seite. **Hinweis:** Wenn Sie Debuggen und an einem Haltepunkt angehalten haben, wird die Ausführung zuerst fortgesetzt. | STRG + UMSCHALT + F5 oder STRG + R

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
