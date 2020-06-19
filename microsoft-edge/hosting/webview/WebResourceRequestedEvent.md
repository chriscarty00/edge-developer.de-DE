---
description: Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.
title: WebResourceRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751982"
---
# <span data-ttu-id="51fd1-104">WebResourceRequestedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="51fd1-104">WebResourceRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="51fd1-105">Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51fd1-105">An event that is fired when an HTTP request is made.</span></span>  

## <span data-ttu-id="51fd1-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51fd1-106">Properties</span></span>  

### <span data-ttu-id="51fd1-107">args</span><span class="sxs-lookup"><span data-stu-id="51fd1-107">args</span></span>  

<span data-ttu-id="51fd1-108">Informationen zur Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="51fd1-108">Information about the resource request.</span></span>  <span data-ttu-id="51fd1-109">Dies ist ein [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="51fd1-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>  

<span data-ttu-id="51fd1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="51fd1-110">This property is read-only.</span></span>  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### <span data-ttu-id="51fd1-111">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="51fd1-111">Property value</span></span>  

<span data-ttu-id="51fd1-112">Geben Sie Folgendes **ein** :</span><span class="sxs-lookup"><span data-stu-id="51fd1-112">Type: **any**</span></span>  
