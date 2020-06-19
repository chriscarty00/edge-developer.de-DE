---
description: Enthält verweisende Informationen zur Navigation
title: NavigationEventWithReferrer-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752127"
---
# <span data-ttu-id="84b8b-104">NavigationEventWithReferrer-Objekt</span><span class="sxs-lookup"><span data-stu-id="84b8b-104">NavigationEventWithReferrer object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="84b8b-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die Navigation initiiert wird und die Navigation einen Referer enthält.</span><span class="sxs-lookup"><span data-stu-id="84b8b-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>  

## <span data-ttu-id="84b8b-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84b8b-106">Properties</span></span>  

### <span data-ttu-id="84b8b-107">Referer</span><span class="sxs-lookup"><span data-stu-id="84b8b-107">referer</span></span>

<span data-ttu-id="84b8b-108">Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.</span><span class="sxs-lookup"><span data-stu-id="84b8b-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="84b8b-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84b8b-109">This property is read-only.</span></span>  

#### <span data-ttu-id="84b8b-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="84b8b-110">Property value</span></span>  

<span data-ttu-id="84b8b-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="84b8b-111">Type: **DOMString**</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### <span data-ttu-id="84b8b-112">Uri</span><span class="sxs-lookup"><span data-stu-id="84b8b-112">uri</span></span>  

<span data-ttu-id="84b8b-113">Der URI (Uniform Resource Identifier) des Ziels der Navigation.</span><span class="sxs-lookup"><span data-stu-id="84b8b-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="84b8b-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84b8b-114">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="84b8b-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="84b8b-115">Property value</span></span>  

<span data-ttu-id="84b8b-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="84b8b-116">Type: **DOMString**</span></span>  
