---
description: Microsoft Edge devtools Protocol, Version 0,1, unterstützt die folgenden HTTP-Endpunkte.
title: DevTools-Protokoll Version 0,1 HTTP-Endpunkte (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5fe50122728304de137efdfb25ebed7274c55cee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233646"
---
# <span data-ttu-id="1a204-103">DevTools-Protokoll Version 0,1 HTTP-Endpunkte (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="1a204-103">DevTools Protocol Version 0.1 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="1a204-104">Das Microsoft Edge devtools-Protokoll funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und später [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.</span><span class="sxs-lookup"><span data-stu-id="1a204-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="1a204-105">Das **devtools-Protokoll 0,1** unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="1a204-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="1a204-106">Weitere Informationen zum Herstellen einer Verbindung mit einem Browser Inhalts Prozess und zur [Domänen](domains/index.md) Dokumentation für die vollständige Web Sockets-basierte devtools-Protokoll-API finden Sie unter [Verwenden des Protokolls](../index.md#using-the-protocol) .</span><span class="sxs-lookup"><span data-stu-id="1a204-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="1a204-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="1a204-107">/json/version</span></span>
<span data-ttu-id="1a204-108">Enthält Informationen über den Browser des Hostcomputers und die Version des devtools-Protokolls, das er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a204-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="1a204-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a204-109">Parameters</span></span>**

*<span data-ttu-id="1a204-110">Keine</span><span class="sxs-lookup"><span data-stu-id="1a204-110">None</span></span>*

**<span data-ttu-id="1a204-111">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1a204-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="1a204-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="1a204-112">/json/protocol</span></span>

<span data-ttu-id="1a204-113">Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="1a204-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="1a204-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a204-114">Parameters</span></span>**

*<span data-ttu-id="1a204-115">Keine</span><span class="sxs-lookup"><span data-stu-id="1a204-115">None</span></span>*

**<span data-ttu-id="1a204-116">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1a204-116">Return object</span></span>**

<span data-ttu-id="1a204-117">JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a204-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="1a204-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="1a204-118">/json/list</span></span>

<span data-ttu-id="1a204-119">Stellt eine Kandidatenliste mit Seiten Zielen für das Debuggen bereit.</span><span class="sxs-lookup"><span data-stu-id="1a204-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="1a204-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a204-120">Parameters</span></span>**

*<span data-ttu-id="1a204-121">Keine</span><span class="sxs-lookup"><span data-stu-id="1a204-121">None</span></span>*

**<span data-ttu-id="1a204-122">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1a204-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="1a204-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="1a204-123">/json/close</span></span>

<span data-ttu-id="1a204-124">Schließt den Zielprozess ab (beispielsweise wird in Microsoft Edge die Registerkarte Seite geschlossen.)</span><span class="sxs-lookup"><span data-stu-id="1a204-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="1a204-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a204-125">Parameters</span></span>**

<span data-ttu-id="1a204-126">Ziel-ID</span><span class="sxs-lookup"><span data-stu-id="1a204-126">Target ID</span></span> 

**<span data-ttu-id="1a204-127">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1a204-127">Return object</span></span>**

```
String("Target is closing")
```
