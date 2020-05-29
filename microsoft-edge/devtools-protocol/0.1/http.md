---
description: Microsoft Edge devtools Protocol, Version 0,1, unterstützt die folgenden HTTP-Endpunkte.
title: DevTools-Protokoll Version 0,1 HTTP-Endpunkte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 5b1cf0d347fec5bfe20b2574afcd635ee569c92d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567550"
---
# HTTP-Endpunkte des devtools-Protokolls

> [!NOTE]
> Das Microsoft Edge devtools-Protokoll funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und später [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.

Das **devtools-Protokoll 0,1** unterstützt die folgenden HTTP-Endpunkte. Weitere Informationen zum Herstellen einer Verbindung mit einem Browser Inhalts Prozess und zur [Domänen](domains/index.md) Dokumentation für die vollständige Web Sockets-basierte devtools-Protokoll-API finden Sie unter [Verwenden des Protokolls](../index.md#using-the-protocol) .

## /json/version
Enthält Informationen über den Browser des Hostcomputers und die Version des devtools-Protokolls, das er unterstützt.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## /json/protocol

Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.

**Parameter**

*Keine*

**Rückgabeobjekt**

JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.

## /json/list

Stellt eine Kandidatenliste mit Seiten Zielen für das Debuggen bereit.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Schließt den Zielprozess ab (beispielsweise wird in Microsoft Edge die Registerkarte Seite geschlossen.)

**Parameter**

Ziel-ID 

**Rückgabeobjekt**

```
String("Target is closing")
```
