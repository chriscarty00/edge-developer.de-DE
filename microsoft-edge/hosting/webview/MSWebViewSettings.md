---
description: Definiert Eigenschaften, die WebView-Features aktivieren oder deaktivieren.
title: MSWebViewSettings-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567167"
---
# <span data-ttu-id="3277a-104">MSWebViewSettings-Objekt</span><span class="sxs-lookup"><span data-stu-id="3277a-104">MSWebViewSettings object</span></span>

<span data-ttu-id="3277a-105">Definiert Eigenschaften, die [WebView](../webview.md) -Features aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3277a-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>

## <span data-ttu-id="3277a-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3277a-106">Properties</span></span>

### <span data-ttu-id="3277a-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="3277a-107">isIndexedDBEnabled</span></span>

<span data-ttu-id="3277a-108">Ruft einen Wert ab, der angibt, ob die Verwendung von IndexedDB in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3277a-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### <span data-ttu-id="3277a-109">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="3277a-109">Property value</span></span>
<span data-ttu-id="3277a-110">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3277a-110">Type: **boolean**</span></span>

<span data-ttu-id="3277a-111">**True** , wenn IndexedDB in der **WebView**zulässig ist, andernfalls false. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3277a-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span> 

### <span data-ttu-id="3277a-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="3277a-112">isJavaScriptEnabled</span></span>

<span data-ttu-id="3277a-113">Ruft einen Wert ab, der angibt, ob die Verwendung von JavaScript in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3277a-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### <span data-ttu-id="3277a-114">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="3277a-114">Property value</span></span>
<span data-ttu-id="3277a-115">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3277a-115">Type: **boolean**</span></span>

<span data-ttu-id="3277a-116">**True** JavaScript ist in der [WebView](../webview.md)zulässig; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3277a-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

### <span data-ttu-id="3277a-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="3277a-117">isScriptNotifyAllowed</span></span>

<span data-ttu-id="3277a-118">Ruft einen Wert ab, der angibt, ob die Verwendung von [ScriptNotifyEvent](ScriptNotifyEvent.md) in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="3277a-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### <span data-ttu-id="3277a-119">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="3277a-119">Property value</span></span>
<span data-ttu-id="3277a-120">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3277a-120">Type: **boolean**</span></span>

<span data-ttu-id="3277a-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) ist in der [WebView](../webview.md)zulässig; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3277a-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 
