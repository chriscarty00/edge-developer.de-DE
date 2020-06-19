---
description: Gibt an, dass die WebView versucht, eine nicht unterstützte Datei herunterzuladen.
title: UnviewableContentIdentifiedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752013"
---
# <span data-ttu-id="e5618-104">UnviewableContentIdentifiedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="e5618-104">UnviewableContentIdentifiedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="e5618-105">Gibt an, dass die [WebView](../webview.md) versucht, zu einer Datei mit einem nicht unterstützten Inhaltstyp zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="e5618-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span>  

## <span data-ttu-id="e5618-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5618-106">Properties</span></span>  

### <span data-ttu-id="e5618-107">MediaType</span><span class="sxs-lookup"><span data-stu-id="e5618-107">mediaType</span></span>  

<span data-ttu-id="e5618-108">Ruft den Inhaltstyp des nicht sichtbar-Inhalts ab.</span><span class="sxs-lookup"><span data-stu-id="e5618-108">Gets the content type of the unviewable content.</span></span>  

<span data-ttu-id="e5618-109">Diese Eigenschaft ist schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5618-109">This property is read-only</span></span>  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### <span data-ttu-id="e5618-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="e5618-110">Property value</span></span>  

<span data-ttu-id="e5618-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="e5618-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="e5618-112">Referer</span><span class="sxs-lookup"><span data-stu-id="e5618-112">referer</span></span>  

<span data-ttu-id="e5618-113">Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.</span><span class="sxs-lookup"><span data-stu-id="e5618-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="e5618-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e5618-114">This property is read-only.</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### <span data-ttu-id="e5618-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="e5618-115">Property value</span></span>  

<span data-ttu-id="e5618-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="e5618-116">Type: **DOMString**</span></span>  

### <span data-ttu-id="e5618-117">Uri</span><span class="sxs-lookup"><span data-stu-id="e5618-117">uri</span></span>  

<span data-ttu-id="e5618-118">Der URI (Uniform Resource Identifier) des Ziels der Navigation.</span><span class="sxs-lookup"><span data-stu-id="e5618-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="e5618-119">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e5618-119">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="e5618-120">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="e5618-120">Property value</span></span>  

<span data-ttu-id="e5618-121">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="e5618-121">Type: **DOMString**</span></span>  
