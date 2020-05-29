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
# <span data-ttu-id="f124e-103">Microsoft Edge (Chrom)-devtools-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f124e-103">Microsoft Edge (Chromium) DevTools Protocol</span></span>

<span data-ttu-id="f124e-104">Mit der Verlagerung der zugrunde liegenden Webplattform von Microsoft Edge auf Chrom erhält das [Microsoft Edge-Protokoll (EdgeHTML) devtools](./devtools-protocol/index.md) keine weiteren Updates.</span><span class="sxs-lookup"><span data-stu-id="f124e-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) will not be receiving any further updates.</span></span> <span data-ttu-id="f124e-105">Das devtools-Protokoll von Microsoft Edge (Chrom) entspricht den APIs des Chrome-devtools-Protokolls, das weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f124e-105">The Microsoft Edge (Chromium) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span> 

<span data-ttu-id="f124e-106">Sie finden die Dokumentation zu diesen Domänen und Methoden, indem Sie auf den [Chrome devtools-Protokoll-Viewer](https://chromedevtools.github.io/devtools-protocol/tot/)verweisen.</span><span class="sxs-lookup"><span data-stu-id="f124e-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>

> [!NOTE]
> <span data-ttu-id="f124e-107">Alle Methoden, die `ms` im [Microsoft Edge (EdgeHTML)-devtools-Protokoll](./devtools-protocol/index.md) vorangestellt wurden, werden im Microsoft Edge (Chrom) devtools-Protokoll nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f124e-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) are no longer supported in the Microsoft Edge (Chromium) DevTools Protocol.</span></span>

## <span data-ttu-id="f124e-108">Verwenden des devtools-Protokolls</span><span class="sxs-lookup"><span data-stu-id="f124e-108">Using the DevTools Protocol</span></span>

<span data-ttu-id="f124e-109">Hier erfahren Sie, wie Sie einen benutzerdefinierten Tooling-Client an den devtools-Server in Microsoft Edge (Chrom) anfügen.</span><span class="sxs-lookup"><span data-stu-id="f124e-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge (Chromium).</span></span>

1. <span data-ttu-id="f124e-110">Stellen Sie sicher, dass alle Instanzen von Microsoft Edge (Chrom) geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="f124e-110">Ensure all instances of Microsoft Edge (Chromium) are closed.</span></span>

2. <span data-ttu-id="f124e-111">Starten Sie Microsoft Edge (Chrom) mit dem Remote Debugging-Port:</span><span class="sxs-lookup"><span data-stu-id="f124e-111">Launch Microsoft Edge (Chromium) with the remote debugging port:</span></span>

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. <span data-ttu-id="f124e-112">Optional können Sie bei Bedarf eine separate Instanz von Edge mit einem eindeutigen Benutzerprofil starten:</span><span class="sxs-lookup"><span data-stu-id="f124e-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired:</span></span>

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. <span data-ttu-id="f124e-113">Verwenden Sie als nächstes den HTTP- `list` Endpunkt, um eine Liste von anfügbaren Seiten Zielen abzurufen:</span><span class="sxs-lookup"><span data-stu-id="f124e-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets:</span></span>

    ```
    http://localhost:9222/json/list
    ```

5. <span data-ttu-id="f124e-114">Stellen Sie schließlich eine Verbindung mit den `webSocketDebuggerUrl` gewünschten Ziel-und Ausgabe Befehlen her/abonnieren Sie Ereignismeldungen über den devtools Web Socket-Server.</span><span class="sxs-lookup"><span data-stu-id="f124e-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>

## <span data-ttu-id="f124e-115">HTTP-Endpunkte des devtools-Protokolls</span><span class="sxs-lookup"><span data-stu-id="f124e-115">DevTools Protocol HTTP Endpoints</span></span>

<span data-ttu-id="f124e-116">Das devtools-Protokoll für Microsoft Edge (Chrom) unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="f124e-116">The Microsoft Edge (Chromium) DevTools Protocol supports the following HTTP endpoints.</span></span>

## <span data-ttu-id="f124e-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="f124e-117">/json/version</span></span>
<span data-ttu-id="f124e-118">Enthält Informationen über den Browser des Hostcomputers und die Version des devtools-Protokolls, das er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f124e-118">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="f124e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-119">Parameters</span></span>**

*<span data-ttu-id="f124e-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-120">None</span></span>*

**<span data-ttu-id="f124e-121">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-121">Return object</span></span>**

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

## <span data-ttu-id="f124e-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="f124e-122">/json/protocol</span></span>

<span data-ttu-id="f124e-123">Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="f124e-123">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="f124e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-124">Parameters</span></span>**

*<span data-ttu-id="f124e-125">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-125">None</span></span>*

**<span data-ttu-id="f124e-126">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-126">Return object</span></span>**

<span data-ttu-id="f124e-127">JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.</span><span class="sxs-lookup"><span data-stu-id="f124e-127">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="f124e-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="f124e-128">/json/list</span></span>

<span data-ttu-id="f124e-129">Stellt eine Kandidatenliste mit Seiten Zielen für das Debuggen bereit.</span><span class="sxs-lookup"><span data-stu-id="f124e-129">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="f124e-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-130">Parameters</span></span>**

*<span data-ttu-id="f124e-131">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-131">None</span></span>*

**<span data-ttu-id="f124e-132">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-132">Return object</span></span>**

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

## <span data-ttu-id="f124e-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="f124e-133">/json/close</span></span>

<span data-ttu-id="f124e-134">Schließt den Zielprozess ab (z. b. in Microsoft Edge (Chrom), schließt das Seitenregister.)</span><span class="sxs-lookup"><span data-stu-id="f124e-134">Closes down the target process (e.g., in Microsoft Edge (Chromium), closes the page tab.)</span></span>

**<span data-ttu-id="f124e-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-135">Parameters</span></span>**

<span data-ttu-id="f124e-136">Ziel-ID</span><span class="sxs-lookup"><span data-stu-id="f124e-136">Target ID</span></span> 

**<span data-ttu-id="f124e-137">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-137">Return object</span></span>**

```
String(“Target is closing”)
```

## <span data-ttu-id="f124e-138">Remote Tools für Microsoft Edge (Beta)</span><span class="sxs-lookup"><span data-stu-id="f124e-138">Remote Tools for Microsoft Edge (Beta)</span></span>

<span data-ttu-id="f124e-139">Sie können jetzt die [Remote Tools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) aus dem [Microsoft Store](https://www.microsoft.com/store/apps/windows)installieren.</span><span class="sxs-lookup"><span data-stu-id="f124e-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span> <span data-ttu-id="f124e-140">Mit dieser APP können Sie Microsoft Edge (Chrom), das auf einem Windows 10-Gerät ausgeführt wird, von Ihrem Entwicklungscomputer aus Remotedebuggen.</span><span class="sxs-lookup"><span data-stu-id="f124e-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>

<span data-ttu-id="f124e-141">In [diesem Lernprogramm](./devtools-guide-chromium/remote-debugging/windows.md)erfahren Sie, wie Sie Ihr Windows 10-Gerät einrichten und von Ihrem Entwicklungscomputer aus eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="f124e-141">To learn how to set up your Windows 10 device and connect to it from your development machine, check out [this tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span></span>

<span data-ttu-id="f124e-142">Die [Remote Tools für Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) verwenden das gleiche Microsoft Edge (Chrom)-devtools-Protokoll als [devtools](./devtools-guide-chromium.md) für die Kommunikation mit Microsoft Edge, das auf dem Windows 10-Gerät ausgeführt wird, das Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="f124e-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](./devtools-guide-chromium.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span> <span data-ttu-id="f124e-143">Diese APP stellt nur `/msedge/` eine Prozess-ID ( `pid` ) vor jedem Aufruf des Protokolls vor.</span><span class="sxs-lookup"><span data-stu-id="f124e-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span> <span data-ttu-id="f124e-144">Sie unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="f124e-144">It supports the following HTTP endpoints.</span></span>

### <span data-ttu-id="f124e-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="f124e-145">/msedge/json/list</span></span>

<span data-ttu-id="f124e-146">Stellt eine Kandidatenliste aller `msedge.exe` Prozesse (einschließlich [PWAs](./progressive-web-apps-chromium/index.md) und alle Registerkarten in allen Instanzen von Microsoft Edge) auf dem Windows 10-Gerät zum Debuggen bereit.</span><span class="sxs-lookup"><span data-stu-id="f124e-146">Provides a candidate list of all `msedge.exe` processes (including [PWAs](./progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge) on the Windows 10 device for debugging.</span></span>

**<span data-ttu-id="f124e-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-147">Parameters</span></span>**

*<span data-ttu-id="f124e-148">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-148">None</span></span>*

**<span data-ttu-id="f124e-149">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-149">Return object</span></span>**

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

### <span data-ttu-id="f124e-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="f124e-150">/msedge/</span></span>

<span data-ttu-id="f124e-151">Entspricht der Funktion von [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="f124e-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span> 

### <span data-ttu-id="f124e-152">/msedge/[PID]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="f124e-152">/msedge/[pid]/json/list</span></span>

<span data-ttu-id="f124e-153">Stellt eine Kandidatenliste mit Seiten Zielen für die Microsoft Edge-Instanz bereit, die dem bereitgestellten `[pid]` für das Debuggen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f124e-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>

**<span data-ttu-id="f124e-154">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-154">Parameters</span></span>**

*<span data-ttu-id="f124e-155">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-155">None</span></span>*

**<span data-ttu-id="f124e-156">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-156">Return object</span></span>**

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

### <span data-ttu-id="f124e-157">/msedge/[PID]/JSON/Version</span><span class="sxs-lookup"><span data-stu-id="f124e-157">/msedge/[pid]/json/version</span></span>

<span data-ttu-id="f124e-158">Stellt Informationen zur Microsoft Edge-Instanz bereit, die der bereitgestellten `[pid]` und der unterstützten Version des devtools-Protokolls entspricht.</span><span class="sxs-lookup"><span data-stu-id="f124e-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="f124e-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-159">Parameters</span></span>**

*<span data-ttu-id="f124e-160">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-160">None</span></span>*

**<span data-ttu-id="f124e-161">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-161">Return object</span></span>**

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

### <span data-ttu-id="f124e-162">/msedge/[PID]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="f124e-162">/msedge/[pid]/json/protocol/</span></span>

<span data-ttu-id="f124e-163">Stellt die gesamte Protokoll-API-Oberfläche als JSON für die Microsoft Edge-Instanz serialisiert dar, die dem bereitgestellten entspricht `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="f124e-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>

**<span data-ttu-id="f124e-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="f124e-164">Parameters</span></span>**

*<span data-ttu-id="f124e-165">Keine</span><span class="sxs-lookup"><span data-stu-id="f124e-165">None</span></span>*

**<span data-ttu-id="f124e-166">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f124e-166">Return object</span></span>**

<span data-ttu-id="f124e-167">JSON-Objekt, das die verfügbare API-Oberfläche für die Version des Protokolls darstellt, die von der Microsoft Edge-Instanz verwendet wird, die der bereitgestellten entspricht `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="f124e-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>
