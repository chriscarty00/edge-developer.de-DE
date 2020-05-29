---
description: Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.
title: WebResourceRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566689"
---
# <span data-ttu-id="66180-104">WebResourceRequestedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="66180-104">WebResourceRequestedEvent object</span></span>

<span data-ttu-id="66180-105">Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66180-105">An event that is fired when an HTTP request is made.</span></span>

## <span data-ttu-id="66180-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66180-106">Properties</span></span>

### <span data-ttu-id="66180-107">args</span><span class="sxs-lookup"><span data-stu-id="66180-107">args</span></span>

<span data-ttu-id="66180-108">Informationen zur Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="66180-108">Information about the resource request.</span></span> <span data-ttu-id="66180-109">Dies ist ein [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="66180-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>

<span data-ttu-id="66180-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="66180-110">This property is read-only.</span></span>

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### <span data-ttu-id="66180-111">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="66180-111">Property value</span></span>
<span data-ttu-id="66180-112">Geben Sie Folgendes **ein** :</span><span class="sxs-lookup"><span data-stu-id="66180-112">Type: **any**</span></span>

