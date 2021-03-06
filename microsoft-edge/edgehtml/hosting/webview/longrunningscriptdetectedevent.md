---
description: LongRunningScriptDetectedEvent-Objekt
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: Webview, Windows 10-Apps, UWP, Edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397941"
---
# <a name="longrunningscriptdetectedevent-object"></a><span data-ttu-id="83e17-104">LongRunningScriptDetectedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="83e17-104">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="83e17-105">Enthält Informationen für [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="83e17-105">Provides information for [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span></span>  

## <a name="properties"></a><span data-ttu-id="83e17-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83e17-106">Properties</span></span>  

### <a name="executiontime"></a><span data-ttu-id="83e17-107">executionTime</span><span class="sxs-lookup"><span data-stu-id="83e17-107">executionTime</span></span>  

<span data-ttu-id="83e17-108">Ruft die Anzahl von Millisekunden ab, mit der das [Webview-Element](../webview/index.md) ein lange ausgeführtes Skript ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="83e17-108">Gets the number of milliseconds that the [webview](../webview/index.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a><span data-ttu-id="83e17-109">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="83e17-109">Property value</span></span>  

<span data-ttu-id="83e17-110">Typ: **long**</span><span class="sxs-lookup"><span data-stu-id="83e17-110">Type: **long**</span></span>  

### <a name="stoppagescriptexecution"></a><span data-ttu-id="83e17-111">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="83e17-111">stopPageScriptExecution</span></span>  

<span data-ttu-id="83e17-112">Stoppt ein lange ausgeführtes Skript, das im [webview-Element ausgeführt](../webview/index.md) wird.</span><span class="sxs-lookup"><span data-stu-id="83e17-112">Stops a long-running script executing in the [webview](../webview/index.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a><span data-ttu-id="83e17-113">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="83e17-113">Property value</span></span>  

<span data-ttu-id="83e17-114">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83e17-114">Type: **Boolean**</span></span>  
