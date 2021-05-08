---
description: Aktualisieren auf das Microsoft Edge DevTools-Protokoll
title: Microsoft Edge DevTools-Protokollupdate
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: de7d6c39c09ba321f21b34e6e461ec030f09f6ad
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480160"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a>Microsoft Edge (Chromium) DevTools-Protokoll  

Mit der Umstellung der zugrunde liegenden Webplattform von Microsoft Edge auf Chromium erhält das [Microsoft Edge (EdgeHTML)-DevTools-Protokoll](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) keine weiteren Updates.  Das Microsoft Edge \(Chromium\) DevTools-Protokoll wird den APIs des Chrome DevTools-Protokolls entsprechen.  

Die Dokumentation zu diesen Domänen und Methoden finden Sie unter [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).  

> [!NOTE]
> Alle Methoden, mit deren Präfix im `ms` [Microsoft Edge (EdgeHTML)-DevTools-Protokoll](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) das Präfix enthalten ist, werden im Microsoft Edge \(Chromium\) DevTools-Protokoll nicht mehr unterstützt.  

## <a name="using-the-devtools-protocol"></a>Verwenden des DevTools-Protokolls  

Hier erfahren Sie, wie Sie einen benutzerdefinierten Toolclient an den DevTools Server in Microsoft Edge \(Chromium\) anfügen.  

1.  Stellen Sie sicher, dass Microsoft Edge \(Chromium\) geschlossen sind.  
1.  Starten Microsoft Edge \(Chromium\) mit dem Remotedebugport:. 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  Optional können Sie bei Bedarf eine separate Instanz von Edge mit einem anderen Benutzerprofil starten.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  Verwenden Sie als Nächstes den `list` HTTP-Endpunkt, um eine Liste der anfügenbaren Seitenziele zu erhalten.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Verbinden Sie sich schließlich mit dem gewünschten Ziel, und geben Sie Befehle aus/abonnieren Sie Ereignismeldungen über den `webSocketDebuggerUrl` DevTools-Webserver.  

## <a name="devtools-protocol-http-endpoints"></a>DevTools-Protokoll-HTTP-Endpunkte  

Das Microsoft Edge \(Chromium\) DevTools-Protokoll unterstützt die folgenden HTTP-Endpunkte.  

## <a name="jsonversion"></a>/json/version  

Stellt Informationen zum Browser des Hostcomputers und zur Unterstützten Version des DevTools-Protokolls zur Verfügung.  

**Parameter**  

**Keine**  

**Return-Objekt**  

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

## <a name="jsonprotocol"></a>/json/protocol  

Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.  

**Parameter**  

**Keine**  

**Return-Objekt**  

JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.  

## <a name="jsonlist"></a>/json/list  

Stellt eine Kandidatenliste mit Seitenzielen für das Debuggen zur Wahl.  

**Parameter**  

**Keine**  

**Return-Objekt**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <a name="jsonclose"></a>/json/close  

Schließt den Zielprozess \(z. B. in Microsoft Edge \(Chromium\), schließt die Seitenregisterkarte\).  

**Parameter**  

Ziel-ID  

**Return-Objekt**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a>Remotetools für Microsoft Edge (Beta)  

Sie können nun die Remotetools für [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) aus dem [Microsoft Store.](https://www.microsoft.com/store/apps/windows)  Mit dieser App können Sie Remotedebugger Microsoft Edge (Chromium), die auf einem Windows 10 von Ihrem Entwicklungscomputer ausgeführt werden.  

Um zu erfahren, wie Sie Ihr Windows 10 einrichten und von Ihrem Entwicklungscomputer aus eine Verbindung mit dem Gerät herstellen, navigieren Sie zu [Erste Schritte Remote debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).  

Die [Remotetools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) verwenden dasselbe Microsoft Edge (Chromium) DevTools-Protokoll wie [die DevTools,](../devtools-guide-chromium/index.md) um mit Microsoft Edge zu kommunizieren, die auf dem zu debuggenden Windows 10-Gerät ausgeführt werden.  Diese App prepends `/msedge/` und eine Prozess-ID ( `pid` ) vor jedem Aufruf des Protokolls.  Es unterstützt die folgenden HTTP-Endpunkte.  

### <a name="msedgejsonlist"></a>/msedge/json/list  

Stellt eine Kandidatenliste aller Prozesse `msedge.exe` \(einschließlich [PWAs](../progressive-web-apps-chromium/index.md) und aller Registerkarten in allen Instanzen von Microsoft Edge\) auf dem Windows 10 debuggen.  

**Parameter**  

**Keine**  

**Return-Objekt**  

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
}, ...  ]
```  

### <a name="msedge"></a>/msedge/  

Funktionell äquivalent zu [/msedge/json/list](#msedgejsonlist).  

### <a name="msedgepidjsonlist"></a>/msedge/[pid]/json/list  

Stellt eine Kandidatenliste mit Seitenzielen für die Microsoft Edge bereit, die mit dem für das `[pid]` Debuggen bereitgestellten entspricht.  

**Parameter**  

**Keine**  

**Return-Objekt**  

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
}, ...  ]
```  

### <a name="msedgepidjsonversion"></a>/msedge/[pid]/json/version  

Enthält Informationen zur Microsoft Edge Instanz, die mit der bereitgestellten und der version `[pid]` des devTools-Protokolls, das sie unterstützt, entspricht.  

**Parameter**  

**Keine**  

**Return-Objekt**  

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

### <a name="msedgepidjsonprotocol"></a>/msedge/[pid]/json/protocol/  

Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche für die Microsoft Edge bereit, die dem bereitgestellten `[pid]` entspricht.  

**Parameter**  

**Keine**  

**Return-Objekt**  

JSON-Objekt, das die verfügbare API-Oberfläche für die Version des Protokolls darstellt, die von der Microsoft Edge verwendet wird, die der bereitgestellten `[pid]` entspricht.  
