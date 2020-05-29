---
description: Enthält Informationen zur abgeschlossenen WebView-Navigation
title: NavigationCompletedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567166"
---
# <span data-ttu-id="0dd49-104">NavigationCompletedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="0dd49-104">NavigationCompletedEvent object</span></span>

<span data-ttu-id="0dd49-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die [WebView](../webview.md) das Laden des aktuellen Inhalts durchgeführt hat oder die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0dd49-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>

## <span data-ttu-id="0dd49-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dd49-106">Properties</span></span>
    
### <span data-ttu-id="0dd49-107">Uri</span><span class="sxs-lookup"><span data-stu-id="0dd49-107">uri</span></span>

<span data-ttu-id="0dd49-108">Der Uniform Resource Identifier (URI) der Navigation.</span><span class="sxs-lookup"><span data-stu-id="0dd49-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>

<span data-ttu-id="0dd49-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0dd49-109">This property is read-only.</span></span>

```js
var uri = NavigationCompletedEvent.uri;
```

#### <span data-ttu-id="0dd49-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="0dd49-110">Property value</span></span>
<span data-ttu-id="0dd49-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="0dd49-111">Type: **DOMString**</span></span>

### <span data-ttu-id="0dd49-112">issuccess</span><span class="sxs-lookup"><span data-stu-id="0dd49-112">isSuccess</span></span>

<span data-ttu-id="0dd49-113">Ruft einen Wert ab, der angibt, ob die Navigation erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0dd49-113">Gets a value that indicates whether the navigation completed successfully.</span></span>

<span data-ttu-id="0dd49-114">Diese Eigenschaft ist schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dd49-114">This property is read-only</span></span>

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### <span data-ttu-id="0dd49-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="0dd49-115">Property value</span></span>
<span data-ttu-id="0dd49-116">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="0dd49-116">Type: **Boolean**</span></span>

### <span data-ttu-id="0dd49-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="0dd49-117">webErrorStatus</span></span>

<span data-ttu-id="0dd49-118">Wenn die Navigation nicht erfolgreich war, Ruft einen Wert ab, der angibt, warum.</span><span class="sxs-lookup"><span data-stu-id="0dd49-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>

<span data-ttu-id="0dd49-119">Diese Eigenschaft ist schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dd49-119">This property is read-only</span></span>

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### <span data-ttu-id="0dd49-120">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="0dd49-120">Property value</span></span>
<span data-ttu-id="0dd49-121">Typ: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="0dd49-121">Type: **unsigned long**</span></span>
