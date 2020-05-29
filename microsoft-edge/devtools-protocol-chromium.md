---
description: Update auf das Microsoft Edge devtools-Protokoll
title: Microsoft Edge devtools-Protokoll Update
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567567"
---
# Microsoft Edge (Chrom)-devtools-Protokoll

Mit der Verlagerung der zugrunde liegenden Webplattform von Microsoft Edge auf Chrom erhält das [Microsoft Edge-Protokoll (EdgeHTML) devtools](./devtools-protocol/index.md) keine weiteren Updates. Das devtools-Protokoll von Microsoft Edge (Chrom) entspricht den APIs des Chrome-devtools-Protokolls, das weitergeleitet wird. 

Sie finden die Dokumentation zu diesen Domänen und Methoden, indem Sie auf den [Chrome devtools-Protokoll-Viewer](https://chromedevtools.github.io/devtools-protocol/tot/)verweisen.

> [!NOTE]
> Alle Methoden, die `ms` im [Microsoft Edge (EdgeHTML)-devtools-Protokoll](./devtools-protocol/index.md) vorangestellt wurden, werden im Microsoft Edge (Chrom) devtools-Protokoll nicht mehr unterstützt.

## Verwenden des devtools-Protokolls

Hier erfahren Sie, wie Sie einen benutzerdefinierten Tooling-Client an den devtools-Server in Microsoft Edge (Chrom) anfügen.

1. Stellen Sie sicher, dass alle Instanzen von Microsoft Edge (Chrom) geschlossen sind.

2. Starten Sie Microsoft Edge (Chrom) mit dem Remote Debugging-Port:

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. Optional können Sie bei Bedarf eine separate Instanz von Edge mit einem eindeutigen Benutzerprofil starten:

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. Verwenden Sie als nächstes den HTTP- `list` Endpunkt, um eine Liste von anfügbaren Seiten Zielen abzurufen:

    ```
    http://localhost:9222/json/list
    ```

5. Stellen Sie schließlich eine Verbindung mit den `webSocketDebuggerUrl` gewünschten Ziel-und Ausgabe Befehlen her/abonnieren Sie Ereignismeldungen über den devtools Web Socket-Server.

## HTTP-Endpunkte des devtools-Protokolls

Das devtools-Protokoll für Microsoft Edge (Chrom) unterstützt die folgenden HTTP-Endpunkte.

## /json/version
Enthält Informationen über den Browser des Hostcomputers und die Version des devtools-Protokolls, das er unterstützt.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
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
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## /json/close

Schließt den Zielprozess ab (z. b. in Microsoft Edge (Chrom), schließt das Seitenregister.)

**Parameter**

Ziel-ID 

**Rückgabeobjekt**

```
String(“Target is closing”)
```

## Remote Tools für Microsoft Edge (Beta)

Sie können jetzt die [Remote Tools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) aus dem [Microsoft Store](https://www.microsoft.com/store/apps/windows)installieren. Mit dieser APP können Sie Microsoft Edge (Chrom), das auf einem Windows 10-Gerät ausgeführt wird, von Ihrem Entwicklungscomputer aus Remotedebuggen.

In [diesem Lernprogramm](./devtools-guide-chromium/remote-debugging/windows.md)erfahren Sie, wie Sie Ihr Windows 10-Gerät einrichten und von Ihrem Entwicklungscomputer aus eine Verbindung herstellen.

Die [Remote Tools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) verwenden das gleiche Microsoft Edge (Chrom)-devtools-Protokoll als [devtools](./devtools-guide-chromium.md) für die Kommunikation mit Microsoft Edge, das auf dem Windows 10-Gerät ausgeführt wird, das Sie debuggen möchten. Diese APP stellt nur `/msedge/` eine Prozess-ID ( `pid` ) vor jedem Aufruf des Protokolls vor. Sie unterstützt die folgenden HTTP-Endpunkte.

### /msedge/json/list

Stellt eine Kandidatenliste aller `msedge.exe` Prozesse (einschließlich [PWAs](./progressive-web-apps-chromium/index.md) und alle Registerkarten in allen Instanzen von Microsoft Edge) auf dem Windows 10-Gerät zum Debuggen bereit.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, … ]
```

### /msedge/

Entspricht der Funktion von [/msedge/JSON/List](#msedgejsonlist). 

### /msedge/[PID]/JSON/List

Stellt eine Kandidatenliste mit Seiten Zielen für die Microsoft Edge-Instanz bereit, die dem bereitgestellten `[pid]` für das Debuggen entspricht.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, … ]
```

### /msedge/[PID]/JSON/Version

Stellt Informationen zur Microsoft Edge-Instanz bereit, die der bereitgestellten `[pid]` und der unterstützten Version des devtools-Protokolls entspricht.

**Parameter**

*Keine*

**Rückgabeobjekt**

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```

### /msedge/[PID]/JSON/Protocol/

Stellt die gesamte Protokoll-API-Oberfläche als JSON für die Microsoft Edge-Instanz serialisiert dar, die dem bereitgestellten entspricht `[pid]` .

**Parameter**

*Keine*

**Rückgabeobjekt**

JSON-Objekt, das die verfügbare API-Oberfläche für die Version des Protokolls darstellt, die von der Microsoft Edge-Instanz verwendet wird, die der bereitgestellten entspricht `[pid]` .
