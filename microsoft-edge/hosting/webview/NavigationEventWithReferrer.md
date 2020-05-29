---
description: Enthält verweisende Informationen zur Navigation
title: NavigationEventWithReferrer-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567160"
---
# <span data-ttu-id="5a1c2-104">NavigationEventWithReferrer-Objekt</span><span class="sxs-lookup"><span data-stu-id="5a1c2-104">NavigationEventWithReferrer object</span></span>

<span data-ttu-id="5a1c2-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die Navigation initiiert wird und die Navigation einen Referer enthält.</span><span class="sxs-lookup"><span data-stu-id="5a1c2-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>

## <span data-ttu-id="5a1c2-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a1c2-106">Properties</span></span>

### <span data-ttu-id="5a1c2-107">Referer</span><span class="sxs-lookup"><span data-stu-id="5a1c2-107">referer</span></span>

<span data-ttu-id="5a1c2-108">Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.</span><span class="sxs-lookup"><span data-stu-id="5a1c2-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="5a1c2-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5a1c2-109">This property is read-only.</span></span>

#### <span data-ttu-id="5a1c2-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5a1c2-110">Property value</span></span>
<span data-ttu-id="5a1c2-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="5a1c2-111">Type: **DOMString**</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

### <span data-ttu-id="5a1c2-112">Uri</span><span class="sxs-lookup"><span data-stu-id="5a1c2-112">uri</span></span>

<span data-ttu-id="5a1c2-113">Der URI (Uniform Resource Identifier) des Ziels der Navigation.</span><span class="sxs-lookup"><span data-stu-id="5a1c2-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="5a1c2-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5a1c2-114">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="5a1c2-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5a1c2-115">Property value</span></span>
<span data-ttu-id="5a1c2-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="5a1c2-116">Type: **DOMString**</span></span>
