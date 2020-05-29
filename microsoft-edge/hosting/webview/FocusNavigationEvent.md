---
description: Das gesendete Objekt aus einem fokusereignis, das den Grund und die Position der Navigation enthält
title: FocusNavigationEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567177"
---
# <span data-ttu-id="1826a-104">FocusNavigationEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="1826a-104">FocusNavigationEvent object</span></span>

<span data-ttu-id="1826a-105">Das gesendete Objekt aus [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) mit dem [**NavigationReason**](#navigationreason) und dem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1826a-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span> 

## <span data-ttu-id="1826a-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="1826a-106">Methods</span></span>

### <span data-ttu-id="1826a-107">requestFocus "</span><span class="sxs-lookup"><span data-stu-id="1826a-107">requestFocus</span></span>

<span data-ttu-id="1826a-108">Wird aufgerufen, um den Fokus von der APP auf die WebView zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="1826a-108">Called to move focus from the app to the webview.</span></span>

### <span data-ttu-id="1826a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1826a-109">Parameters</span></span>

<span data-ttu-id="1826a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1826a-110">This method does not have parameters.</span></span>

### <span data-ttu-id="1826a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1826a-111">Return value</span></span>

<span data-ttu-id="1826a-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1826a-112">This method does not return a value.</span></span>

## <span data-ttu-id="1826a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1826a-113">Properties</span></span>
    
### <span data-ttu-id="1826a-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="1826a-114">navigationReason</span></span>

<span data-ttu-id="1826a-115">Aufgezählter Typ **NavigationReason**, entweder "Links", "oben", "rechts" oder "unten".</span><span class="sxs-lookup"><span data-stu-id="1826a-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span> 

<span data-ttu-id="1826a-116">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1826a-116">This property is read-only.</span></span>

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### <span data-ttu-id="1826a-117">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="1826a-117">Property value</span></span>
<span data-ttu-id="1826a-118">Geben Sie Folgendes ein: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="1826a-118">Type: **NavigationReason**</span></span>

### <span data-ttu-id="1826a-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="1826a-119">originHeight</span></span>

<span data-ttu-id="1826a-120">Die Position der Ursprungs Höhe des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1826a-120">The origin height location of the element to be given focus.</span></span>

<span data-ttu-id="1826a-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1826a-121">This property is read-only.</span></span>

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### <span data-ttu-id="1826a-122">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="1826a-122">Property value</span></span>
<span data-ttu-id="1826a-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1826a-123">Type: **float**</span></span>

### <span data-ttu-id="1826a-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="1826a-124">originLeft</span></span>

<span data-ttu-id="1826a-125">Die Position des Ausgangs Links des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1826a-125">The origin left location of the element to be given focus.</span></span>

<span data-ttu-id="1826a-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1826a-126">This property is read-only.</span></span>

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### <span data-ttu-id="1826a-127">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="1826a-127">Property value</span></span>
<span data-ttu-id="1826a-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1826a-128">Type: **float**</span></span>

### <span data-ttu-id="1826a-129">originTop</span><span class="sxs-lookup"><span data-stu-id="1826a-129">originTop</span></span>

<span data-ttu-id="1826a-130">Die ursprüngliche oberste Position des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1826a-130">The origin top location of the element to be given focus.</span></span>

<span data-ttu-id="1826a-131">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1826a-131">This property is read-only.</span></span>

```js
var originTop = FocusNavigationEvent.originTop;
```

#### <span data-ttu-id="1826a-132">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="1826a-132">Property value</span></span>
<span data-ttu-id="1826a-133">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1826a-133">Type: **float**</span></span>

### <span data-ttu-id="1826a-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="1826a-134">originWidth</span></span>

<span data-ttu-id="1826a-135">Die Position der Ursprungs Breite des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1826a-135">The origin width location of the element to be given focus.</span></span>

<span data-ttu-id="1826a-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1826a-136">This property is read-only.</span></span>

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### <span data-ttu-id="1826a-137">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="1826a-137">Property value</span></span>
<span data-ttu-id="1826a-138">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1826a-138">Type: **float**</span></span>

