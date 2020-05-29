---
description: Gibt an, dass die WebView versucht, eine nicht unterstützte Datei herunterzuladen.
title: UnviewableContentIdentifiedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566692"
---
# <span data-ttu-id="4b682-104">UnviewableContentIdentifiedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="4b682-104">UnviewableContentIdentifiedEvent object</span></span>

<span data-ttu-id="4b682-105">Gibt an, dass die [WebView](../webview.md) versucht, zu einer Datei mit einem nicht unterstützten Inhaltstyp zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="4b682-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span> 

## <span data-ttu-id="4b682-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b682-106">Properties</span></span>

### <span data-ttu-id="4b682-107">MediaType</span><span class="sxs-lookup"><span data-stu-id="4b682-107">mediaType</span></span>

<span data-ttu-id="4b682-108">Ruft den Inhaltstyp des nicht sichtbar-Inhalts ab.</span><span class="sxs-lookup"><span data-stu-id="4b682-108">Gets the content type of the unviewable content.</span></span>

<span data-ttu-id="4b682-109">Diese Eigenschaft ist schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4b682-109">This property is read-only</span></span>

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### <span data-ttu-id="4b682-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="4b682-110">Property value</span></span>
<span data-ttu-id="4b682-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="4b682-111">Type: **DOMString**</span></span>

### <span data-ttu-id="4b682-112">Referer</span><span class="sxs-lookup"><span data-stu-id="4b682-112">referer</span></span>

<span data-ttu-id="4b682-113">Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.</span><span class="sxs-lookup"><span data-stu-id="4b682-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="4b682-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b682-114">This property is read-only.</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

#### <span data-ttu-id="4b682-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="4b682-115">Property value</span></span>
<span data-ttu-id="4b682-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="4b682-116">Type: **DOMString**</span></span>

### <span data-ttu-id="4b682-117">Uri</span><span class="sxs-lookup"><span data-stu-id="4b682-117">uri</span></span>

<span data-ttu-id="4b682-118">Der URI (Uniform Resource Identifier) des Ziels der Navigation.</span><span class="sxs-lookup"><span data-stu-id="4b682-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="4b682-119">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b682-119">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="4b682-120">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="4b682-120">Property value</span></span>
<span data-ttu-id="4b682-121">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="4b682-121">Type: **DOMString**</span></span>
