---
description: Schauen Sie sich die Neuerungen in der Microsoft Edge-devtools im Windows 10 Oktober 2018-Update an
title: Neuerungen im Microsoft Edge-devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.openlocfilehash: 604419f4c77ccaaf2dfd3179273be803cde86fc8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567574"
---
# DevTools im neuesten Windows 10-Update (EdgeHTML 18)

Das neueste Update für Microsoft Edge devtools bietet eine Reihe von Vorteilen sowohl für die Benutzeroberfläche als auch unter der Haube, einschließlich neuer dedizierter Panels für [*Dienstmitarbeiter*](#service-workers-panel) und [*Speicher*](#storage-panel), Quell [Datei-Such](#source-file-search-tools) Tools im Debugger und neuen Edge- [devtools-Protokoll Domänen](#edge-devtools-protocol-updates) für das Debuggen von Stilen und Layouts sowie für Konsolen-APIs.

Hier sind die neuesten Microsoft Edge devtools-Funktionen, die jetzt im [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)) zur Verfügung stehen. Darüber hinaus haben wir auch eine Reihe von Fehlern bei der Barrierefreiheit, Zuverlässigkeit und Leistung behoben, um die Grundlagen zu verbessern!

## DevTools-App

Wir haben die eigenständige [Microsoft Edge devtools Preview-App](../devtools-guide.md#microsoft-store-app)aktualisiert. Die neueste Version umfasst den Remotedebuggen Zugriff auf Kernfunktionalität im [**Debugger**](./debugger.md), [**Elemente**](./elements.md) (für schreibgeschützte Vorgänge) und [**Konsolen**](./console.md) Panels.

## Dienstmitarbeiter-Panel

Es gibt jetzt ein dediziertes [**Service Worker**](./service-workers.md) -Panel zum Überprüfen, verwalten und Debuggen der Servicemitarbeiter Ihrer Website. Dies bietet die gleiche Funktionalität wie zuvor im *Debugger* -Panel (jetzt mit einer nicht überfüllten UI!).

![Dienstmitarbeiter-Panel](./media/service_worker.png)

## Speicher Panel

Darüber hinaus haben wir alle lokalen Speicher Inspektoren (*lokaler Speicher, IndexedDB, Cookies, Cache*), die sich zuvor im *Debugger* befanden, in Ihre eigene dedizierte [**Speicher**](./storage.md) Konsole verschoben.

![Speicher Panel](./media/storage_cache.png)

## Such Tools für Quelldateien

Der [**Debugger**](./debugger.md) verfügt nun über einen Bereich für die [Quelldatei Suche](./debugger.md#file-search) . Öffnen Sie die Datei mit dem Befehl *in Dateien suchen* ( `Ctrl` + `Shift` + `F` ), wenn Sie über eine bestimmte Zeichenfolge verfügen, die Sie in der Quelle finden möchten. Die Symbolleiste bietet verschiedene Suchoptionen, einschließlich regulärer Ausdrücke. 

![Debugger-Dateisuche](./media/debugger_file_search.png)

Sie können auch eine beliebige geladene Quelldatei mit dem Befehl *Open File* () schnell öffnen `Ctrl` + `P` .

![Debugger-Datei öffnen](./media/debugger_open_file.png)

## Edge-devtools-Protokoll Updates

[Version 0,2](../devtools-protocol/0.2/index.md) des devtools-Protokolls bietet neue Domänen für Stil-und Layoutfunktionen (schreibgeschützt) sowie Debug-und Konsolen-APIs sowie die Kernskript Debugging-Funktionen, die in [Version 0,1](../devtools-protocol/0.1/index.md)eingeführt wurden. In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den [**Elementen**](../devtools-guide/elements.md) (für schreibgeschützte Vorgänge), [**Konsolen**](../devtools-guide/console.md) -und [**Debuggerfenster**](../devtools-guide/debugger.md) zur Verfügung steht.
