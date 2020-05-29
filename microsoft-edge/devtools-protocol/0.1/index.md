---
description: Anmerkungen zu dieser Version von Microsoft Edge devtools Protocol, Version 0,1
title: Versionshinweise zu devtools-Protokoll Version 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 29dc8f1b0ba67cb2b3155cb2135d488609e9bff9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567549"
---
# Versionshinweise zu devtools-Protokoll Version 0,1

> [!NOTE]
> Das Microsoft Edge devtools-Protokoll funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und später [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.

Version 0,1 des Microsoft **Edge devtools-Protokolls** bietet eine frühe Vorschau zum Testen der EdgeHTML-Instrumentation und des einfachen Remotedebuggens in der neuen eigenständigen [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -app. Daher ist es erforderlich, dass Sie [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) oder einen späteren [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Build ausführen.

Die Ziele hinter dem devtools-Protokoll sind drei Fach:

 - Bereitstelleneiner öffentlichen API für unsere devtools-App zum Anfügen an Microsoft Edge
 - Erweitern des Zugriffs auf die devtools-Funktionalität auf externe Tooling-Clients
 - Aktivieren des Remotedebuggens im gesamten Bereich von Windows 10-Geräten mit Micrsoft Edge 

Diese vorläufige Version bietet Kernfunktionen zum Debuggen, wie das Festlegen von Haltepunkten, das Durchlaufen von Code und das Untersuchen von Stapelablaufverfolgungen. In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die im [**Debuggerfenster**](../../devtools-guide/debugger.md) zur Verfügung steht, minus Cache Überprüfung (für Web Storage, Service Worker, Cache-API und IndexedDB). 

Weitere Debuggerfunktionen werden in bevorstehenden Versionen hinzugefügt, gefolgt von der Instrumentation, die andere [devtools](../../devtools-guide.md) -Panels anbietet.
