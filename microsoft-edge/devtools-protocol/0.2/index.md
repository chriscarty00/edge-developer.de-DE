---
description: Anmerkungen zu dieser Version von Microsoft Edge devtools Protocol, Version 0,2
title: Versionshinweise zu Microsoft Edge devtools Protocol Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4c54273d123c605181ee4b53aa441768a8711bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567524"
---
# Versionshinweise zu devtools-Protokoll Version 0,2

> [!NOTE]
> Version 0,2 des Microsoft Edge devtools-Protokolls funktioniert nur auf dem [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) und später in [Windows Insider Preview](https://insider.windows.com/getting-started/) -Builds.

Version 0,2 des Microsoft **Edge devtools-Protokolls** bietet eine Vorschau zum Testen der EdgeHTML-Instrumentation und des einfachen Remotedebuggens in der neuen eigenständigen [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -app. Daher müssen Sie das [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) oder einen späteren [Windows Insider Preview](https://insider.windows.com/getting-started/) -Build ausführen.

Die Ziele hinter dem devtools-Protokoll sind drei Fach:

 - Bereitstelleneiner öffentlichen API für unsere devtools-App zum Anfügen an Microsoft Edge
 - Erweitern des Zugriffs auf die devtools-Funktionalität auf externe Tooling-Clients
 - Aktivieren des Remotedebuggens im gesamten Bereich von Windows 10-Geräten mit Micrsoft Edge 

Version 0,2 des devtools-Protokolls enthält neue Domänen für Format-und Layoutfunktionen (schreibgeschützt) sowie Debug-und Konsolen-APIs, zusätzlich zu den Kernskript Debugging-Funktionen, die in Version 0,1 eingeführt wurden. In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den Panels [**Elemente**](../../devtools-guide/elements.md), [**Konsole**](../../devtools-guide/console.md) und [**Debugger**](../../devtools-guide/debugger.md) zur Verfügung steht.
