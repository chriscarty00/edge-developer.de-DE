---
description: Enthält Informationen zur abgeschlossenen WebView-Navigation
title: NavigationCompletedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752138"
---
# <span data-ttu-id="404b0-104">NavigationCompletedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="404b0-104">NavigationCompletedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="404b0-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die [WebView](../webview.md) das Laden des aktuellen Inhalts durchgeführt hat oder die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="404b0-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>  

## <span data-ttu-id="404b0-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="404b0-106">Properties</span></span>  

### <span data-ttu-id="404b0-107">Uri</span><span class="sxs-lookup"><span data-stu-id="404b0-107">uri</span></span>  

<span data-ttu-id="404b0-108">Der Uniform Resource Identifier (URI) der Navigation.</span><span class="sxs-lookup"><span data-stu-id="404b0-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>  

<span data-ttu-id="404b0-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="404b0-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### <span data-ttu-id="404b0-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="404b0-110">Property value</span></span>  

<span data-ttu-id="404b0-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="404b0-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="404b0-112">issuccess</span><span class="sxs-lookup"><span data-stu-id="404b0-112">isSuccess</span></span>  

<span data-ttu-id="404b0-113">Ruft einen Wert ab, der angibt, ob die Navigation erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="404b0-113">Gets a value that indicates whether the navigation completed successfully.</span></span>  

<span data-ttu-id="404b0-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="404b0-114">This property is read-only.</span></span>  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### <span data-ttu-id="404b0-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="404b0-115">Property value</span></span>  

<span data-ttu-id="404b0-116">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="404b0-116">Type: **Boolean**</span></span>  

### <span data-ttu-id="404b0-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="404b0-117">webErrorStatus</span></span>  

<span data-ttu-id="404b0-118">Wenn die Navigation nicht erfolgreich war, Ruft einen Wert ab, der angibt, warum.</span><span class="sxs-lookup"><span data-stu-id="404b0-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>  

<span data-ttu-id="404b0-119">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="404b0-119">This property is read-only.</span></span>  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### <span data-ttu-id="404b0-120">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="404b0-120">Property value</span></span>  

<span data-ttu-id="404b0-121">Typ: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="404b0-121">Type: **unsigned long**</span></span>  
