---
description: Definiert Eigenschaften, die WebView-Features aktivieren oder deaktivieren.
title: MSWebViewSettings-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752178"
---
# <span data-ttu-id="fdd96-104">MSWebViewSettings-Objekt</span><span class="sxs-lookup"><span data-stu-id="fdd96-104">MSWebViewSettings object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="fdd96-105">Definiert Eigenschaften, die [WebView](../webview.md) -Features aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fdd96-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>  

## <span data-ttu-id="fdd96-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fdd96-106">Properties</span></span>  

### <span data-ttu-id="fdd96-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="fdd96-107">isIndexedDBEnabled</span></span>  

<span data-ttu-id="fdd96-108">Ruft einen Wert ab, der angibt, ob die Verwendung von IndexedDB in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fdd96-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### <span data-ttu-id="fdd96-109">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="fdd96-109">Property value</span></span>  

<span data-ttu-id="fdd96-110">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fdd96-110">Type: **boolean**</span></span>  

<span data-ttu-id="fdd96-111">**True** , wenn IndexedDB in der **WebView**zulässig ist, andernfalls false. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fdd96-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span>  

### <span data-ttu-id="fdd96-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="fdd96-112">isJavaScriptEnabled</span></span>  

<span data-ttu-id="fdd96-113">Ruft einen Wert ab, der angibt, ob die Verwendung von JavaScript in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fdd96-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### <span data-ttu-id="fdd96-114">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="fdd96-114">Property value</span></span>  

<span data-ttu-id="fdd96-115">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fdd96-115">Type: **boolean**</span></span>  

<span data-ttu-id="fdd96-116">**True** JavaScript ist in der [WebView](../webview.md)zulässig; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fdd96-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

### <span data-ttu-id="fdd96-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="fdd96-117">isScriptNotifyAllowed</span></span>  

<span data-ttu-id="fdd96-118">Ruft einen Wert ab, der angibt, ob die Verwendung von [ScriptNotifyEvent](ScriptNotifyEvent.md) in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fdd96-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### <span data-ttu-id="fdd96-119">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="fdd96-119">Property value</span></span>  

<span data-ttu-id="fdd96-120">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fdd96-120">Type: **boolean**</span></span>  

<span data-ttu-id="fdd96-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) ist in der [WebView](../webview.md)zulässig; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fdd96-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  
