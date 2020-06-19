---
description: ''
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752151"
---
# <span data-ttu-id="39e34-103">LongRunningScriptDetectedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="39e34-103">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="39e34-104">Enthält Informationen zu [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="39e34-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>  

## <span data-ttu-id="39e34-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39e34-105">Properties</span></span>  

### <span data-ttu-id="39e34-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="39e34-106">executionTime</span></span>  

<span data-ttu-id="39e34-107">Ruft die Anzahl der Millisekunden ab, die das [WebView](../webview.md) -Element ein Skript mit langer Ausführungsdauer ausführt.</span><span class="sxs-lookup"><span data-stu-id="39e34-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <span data-ttu-id="39e34-108">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="39e34-108">Property value</span></span>  

<span data-ttu-id="39e34-109">Typ: **Long**</span><span class="sxs-lookup"><span data-stu-id="39e34-109">Type: **long**</span></span>  

### <span data-ttu-id="39e34-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="39e34-110">stopPageScriptExecution</span></span>  

<span data-ttu-id="39e34-111">Beendet ein Skript mit langer Ausführungszeit, das im [WebView](../webview.md) -Element ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39e34-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <span data-ttu-id="39e34-112">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="39e34-112">Property value</span></span>  

<span data-ttu-id="39e34-113">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="39e34-113">Type: **Boolean**</span></span>  
