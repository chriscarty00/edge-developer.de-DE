---
description: Microsoft Edge devtools Protocol, Version 0,2, unterstützt die folgenden HTTP-Endpunkte.
title: Microsoft Edge devtools Protocol, Version 0,2, HTTP-Endpunkte (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: eb5b29e4d8149f511d8a7cbca3da72391a13e449
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882858"
---
# <span data-ttu-id="589d0-103">Microsoft Edge devtools Protocol, Version 0,2, HTTP-Endpunkte (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="589d0-103">Microsoft Edge DevTools Protocol Version 0.2 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="589d0-104">Version 0,2 des Microsoft Edge devtools-Protokolls funktioniert nur auf dem [Windows 10 October 2018-Update]() und später in [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.</span><span class="sxs-lookup"><span data-stu-id="589d0-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update]() and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="589d0-105">Das **devtools-Protokoll 0,2** unterstützt die folgenden HTTP-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="589d0-105">**DevTools Protocol 0.2** supports the following HTTP endpoints.</span></span> <span data-ttu-id="589d0-106">Weitere Informationen zum Herstellen einer Verbindung mit einem Browser Inhalts Prozess und zur [Domänen](domains/index.md) Dokumentation für die vollständige Web Sockets-basierte devtools-Protokoll-API finden Sie unter [Verwenden des Protokolls](../index.md#using-the-protocol) .</span><span class="sxs-lookup"><span data-stu-id="589d0-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="589d0-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="589d0-107">/json/version</span></span>
<span data-ttu-id="589d0-108">Enthält Informationen über den Browser des Hostcomputers und die Version des devtools-Protokolls, das er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="589d0-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="589d0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="589d0-109">Parameters</span></span>**

*<span data-ttu-id="589d0-110">Keine</span><span class="sxs-lookup"><span data-stu-id="589d0-110">None</span></span>*

**<span data-ttu-id="589d0-111">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="589d0-111">Return object</span></span>**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## <span data-ttu-id="589d0-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="589d0-112">/json/protocol</span></span>

<span data-ttu-id="589d0-113">Stellt die gesamte als JSON serialisierte Protokoll-API-Oberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="589d0-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="589d0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="589d0-114">Parameters</span></span>**

*<span data-ttu-id="589d0-115">Keine</span><span class="sxs-lookup"><span data-stu-id="589d0-115">None</span></span>*

**<span data-ttu-id="589d0-116">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="589d0-116">Return object</span></span>**

<span data-ttu-id="589d0-117">JSON-Objekt, das die verfügbare API-Oberfläche für die aktuelle Version des Protokolls darstellt.</span><span class="sxs-lookup"><span data-stu-id="589d0-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="589d0-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="589d0-118">/json/list</span></span>

<span data-ttu-id="589d0-119">Stellt eine Kandidatenliste mit Seiten Zielen für das Debuggen bereit.</span><span class="sxs-lookup"><span data-stu-id="589d0-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="589d0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="589d0-120">Parameters</span></span>**

*<span data-ttu-id="589d0-121">Keine</span><span class="sxs-lookup"><span data-stu-id="589d0-121">None</span></span>*

**<span data-ttu-id="589d0-122">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="589d0-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="589d0-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="589d0-123">/json/close</span></span>

<span data-ttu-id="589d0-124">Schließt den Zielprozess ab (beispielsweise wird in Microsoft Edge die Registerkarte Seite geschlossen.)</span><span class="sxs-lookup"><span data-stu-id="589d0-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="589d0-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="589d0-125">Parameters</span></span>**

<span data-ttu-id="589d0-126">Ziel-ID</span><span class="sxs-lookup"><span data-stu-id="589d0-126">Target ID</span></span> 

**<span data-ttu-id="589d0-127">Rückgabeobjekt</span><span class="sxs-lookup"><span data-stu-id="589d0-127">Return object</span></span>**

```
String("Target is closing")
```
