---
description: ''
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567176"
---
# <span data-ttu-id="e306b-103">LongRunningScriptDetectedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="e306b-103">LongRunningScriptDetectedEvent object</span></span>

<span data-ttu-id="e306b-104">Enthält Informationen zu [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="e306b-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>

## <span data-ttu-id="e306b-105">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e306b-105">Properties</span></span>

### <span data-ttu-id="e306b-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="e306b-106">executionTime</span></span>

<span data-ttu-id="e306b-107">Ruft die Anzahl der Millisekunden ab, die das [WebView](../webview.md) -Element ein Skript mit langer Ausführungsdauer ausführt.</span><span class="sxs-lookup"><span data-stu-id="e306b-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### <span data-ttu-id="e306b-108">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="e306b-108">Property value</span></span>
<span data-ttu-id="e306b-109">Typ: **Long**</span><span class="sxs-lookup"><span data-stu-id="e306b-109">Type: **long**</span></span>

### <span data-ttu-id="e306b-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="e306b-110">stopPageScriptExecution</span></span>
<span data-ttu-id="e306b-111">Beendet ein Skript mit langer Ausführungszeit, das im [WebView](../webview.md) -Element ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e306b-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### <span data-ttu-id="e306b-112">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="e306b-112">Property value</span></span>
<span data-ttu-id="e306b-113">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="e306b-113">Type: **Boolean**</span></span>