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
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a><span data-ttu-id="70774-103">Microsoft Edge (Chromium) DevTools-Protokoll</span><span class="sxs-lookup"><span data-stu-id="70774-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="70774-104">Mit der Umstellung der zugrunde liegenden Webplattform von Microsoft Edge auf Chromium erhält das [Microsoft Edge (EdgeHTML)-DevTools-Protokoll](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) keine weiteren Updates.</span><span class="sxs-lookup"><span data-stu-id="70774-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) will not be receiving any further updates.</span></span>  <span data-ttu-id="70774-105">Das Microsoft Edge \(Chromium\) DevTools-Protokoll wird den APIs des Chrome DevTools-Protokolls entsprechen.</span><span class="sxs-lookup"><span data-stu-id="70774-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="70774-106">Die Dokumentation zu diesen Domänen und Methoden finden Sie unter [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).</span><span class="sxs-lookup"><span data-stu-id="70774-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).</span></span>  

> [!NOTE]
> <span data-ttu-id="70774-107">Alle Methoden, mit deren Präfix im `ms` [Microsoft Edge (EdgeHTML)-DevTools-Protokoll](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) das Präfix enthalten ist, werden im Microsoft Edge \(Chromium\) DevTools-Protokoll nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70774-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <a name="using-the-devtools-protocol"></a><span data-ttu-id="70774-108">Verwenden des DevTools-Protokolls</span><span class="sxs-lookup"><span data-stu-id="70774-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="70774-109">Hier erfahren Sie, wie Sie einen benutzerdefinierten Toolclient an den DevTools Server in Microsoft Edge \(Chromium\) anfügen.</span><span class="sxs-lookup"><span data-stu-id="70774-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="70774-110">Stellen Sie sicher, dass Microsoft Edge \(Chromium\) geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="70774-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="70774-111">Starten Microsoft Edge \(Chromium\) mit dem Remotedebugport:.</span><span class="sxs-lookup"><span data-stu-id="70774-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="70774-112">Optional können Sie bei Bedarf eine separate Instanz von Edge mit einem anderen Benutzerprofil starten.</span><span class="sxs-lookup"><span data-stu-id="70774-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="70774-113">Verwenden Sie als Nächstes den `list` HTTP-Endpunkt, um eine Liste der anfügenbaren Seitenziele zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="70774-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="70774-114">Verbinden Sie sich schließlich mit dem gewünschten Ziel, und geben Sie Befehle aus/abonnieren Sie Ereignismeldungen über den `webSocketDebuggerUrl` DevTools-Webserver.</span><span class="sxs-lookup"><span data-stu-id="70774-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <a name="devtools-protocol-http-endpoints"></a><span data-ttu-id="70774-115">DevTools-Protokoll-HTTP-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="70774-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="70774-116">Das Microsoft Edge \(Chromium\) DevTools-Protokoll unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="70774-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <a name="jsonversion"></a><span data-ttu-id="70774-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="70774-117">/json/version</span></span>  

<span data-ttu-id="70774-118">Stellt Informationen zum Browser des Hostcomputers und zur Unterstützten Version des DevTools-Protokolls zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="70774-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="70774-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-119">Parameters</span></span>**  

**<span data-ttu-id="70774-120">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-120">None</span></span>**  

**<span data-ttu-id="70774-121">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-121">Return object</span></span>**  

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

## <a name="jsonprotocol"></a><span data-ttu-id="70774-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="70774-122">/json/protocol</span></span>  

<span data-ttu-id="70774-123">Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="70774-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="70774-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-124">Parameters</span></span>**  

**<span data-ttu-id="70774-125">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-125">None</span></span>**  

**<span data-ttu-id="70774-126">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-126">Return object</span></span>**  

<span data-ttu-id="70774-127">JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.</span><span class="sxs-lookup"><span data-stu-id="70774-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <a name="jsonlist"></a><span data-ttu-id="70774-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="70774-128">/json/list</span></span>  

<span data-ttu-id="70774-129">Stellt eine Kandidatenliste mit Seitenzielen für das Debuggen zur Wahl.</span><span class="sxs-lookup"><span data-stu-id="70774-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="70774-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-130">Parameters</span></span>**  

**<span data-ttu-id="70774-131">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-131">None</span></span>**  

**<span data-ttu-id="70774-132">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-132">Return object</span></span>**  

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

## <a name="jsonclose"></a><span data-ttu-id="70774-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="70774-133">/json/close</span></span>  

<span data-ttu-id="70774-134">Schließt den Zielprozess \(z. B. in Microsoft Edge \(Chromium\), schließt die Seitenregisterkarte\).</span><span class="sxs-lookup"><span data-stu-id="70774-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="70774-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-135">Parameters</span></span>**  

<span data-ttu-id="70774-136">Ziel-ID</span><span class="sxs-lookup"><span data-stu-id="70774-136">Target ID</span></span>  

**<span data-ttu-id="70774-137">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a><span data-ttu-id="70774-138">Remotetools für Microsoft Edge (Beta)</span><span class="sxs-lookup"><span data-stu-id="70774-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="70774-139">Sie können nun die Remotetools für [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) aus dem [Microsoft Store.](https://www.microsoft.com/store/apps/windows)</span><span class="sxs-lookup"><span data-stu-id="70774-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="70774-140">Mit dieser App können Sie Remotedebugger Microsoft Edge (Chromium), die auf einem Windows 10 von Ihrem Entwicklungscomputer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70774-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="70774-141">Um zu erfahren, wie Sie Ihr Windows 10 einrichten und von Ihrem Entwicklungscomputer aus eine Verbindung mit dem Gerät herstellen, navigieren Sie zu [Erste Schritte Remote debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="70774-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="70774-142">Die [Remotetools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) verwenden dasselbe Microsoft Edge (Chromium) DevTools-Protokoll wie [die DevTools,](../devtools-guide-chromium/index.md) um mit Microsoft Edge zu kommunizieren, die auf dem zu debuggenden Windows 10-Gerät ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70774-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="70774-143">Diese App prepends `/msedge/` und eine Prozess-ID ( `pid` ) vor jedem Aufruf des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="70774-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="70774-144">Es unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="70774-144">It supports the following HTTP endpoints.</span></span>  

### <a name="msedgejsonlist"></a><span data-ttu-id="70774-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="70774-145">/msedge/json/list</span></span>  

<span data-ttu-id="70774-146">Stellt eine Kandidatenliste aller Prozesse `msedge.exe` \(einschließlich [PWAs](../progressive-web-apps-chromium/index.md) und aller Registerkarten in allen Instanzen von Microsoft Edge\) auf dem Windows 10 debuggen.</span><span class="sxs-lookup"><span data-stu-id="70774-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="70774-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-147">Parameters</span></span>**  

**<span data-ttu-id="70774-148">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-148">None</span></span>**  

**<span data-ttu-id="70774-149">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-149">Return object</span></span>**  

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

### <a name="msedge"></a><span data-ttu-id="70774-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="70774-150">/msedge/</span></span>  

<span data-ttu-id="70774-151">Funktionell äquivalent zu [/msedge/json/list](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="70774-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <a name="msedgepidjsonlist"></a><span data-ttu-id="70774-152">/msedge/[pid]/json/list</span><span class="sxs-lookup"><span data-stu-id="70774-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="70774-153">Stellt eine Kandidatenliste mit Seitenzielen für die Microsoft Edge bereit, die mit dem für das `[pid]` Debuggen bereitgestellten entspricht.</span><span class="sxs-lookup"><span data-stu-id="70774-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="70774-154">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-154">Parameters</span></span>**  

**<span data-ttu-id="70774-155">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-155">None</span></span>**  

**<span data-ttu-id="70774-156">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-156">Return object</span></span>**  

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

### <a name="msedgepidjsonversion"></a><span data-ttu-id="70774-157">/msedge/[pid]/json/version</span><span class="sxs-lookup"><span data-stu-id="70774-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="70774-158">Enthält Informationen zur Microsoft Edge Instanz, die mit der bereitgestellten und der version `[pid]` des devTools-Protokolls, das sie unterstützt, entspricht.</span><span class="sxs-lookup"><span data-stu-id="70774-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="70774-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-159">Parameters</span></span>**  

**<span data-ttu-id="70774-160">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-160">None</span></span>**  

**<span data-ttu-id="70774-161">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-161">Return object</span></span>**  

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

### <a name="msedgepidjsonprotocol"></a><span data-ttu-id="70774-162">/msedge/[pid]/json/protocol/</span><span class="sxs-lookup"><span data-stu-id="70774-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="70774-163">Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche für die Microsoft Edge bereit, die dem bereitgestellten `[pid]` entspricht.</span><span class="sxs-lookup"><span data-stu-id="70774-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="70774-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="70774-164">Parameters</span></span>**  

**<span data-ttu-id="70774-165">Keine</span><span class="sxs-lookup"><span data-stu-id="70774-165">None</span></span>**  

**<span data-ttu-id="70774-166">Return-Objekt</span><span class="sxs-lookup"><span data-stu-id="70774-166">Return object</span></span>**  

<span data-ttu-id="70774-167">JSON-Objekt, das die verfügbare API-Oberfläche für die Version des Protokolls darstellt, die von der Microsoft Edge verwendet wird, die der bereitgestellten `[pid]` entspricht.</span><span class="sxs-lookup"><span data-stu-id="70774-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
