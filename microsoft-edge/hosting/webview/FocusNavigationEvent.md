---
description: Das gesendete Objekt aus einem fokusereignis, das den Grund und die Position der Navigation enthält
title: FocusNavigationEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752164"
---
# <span data-ttu-id="d627c-104">FocusNavigationEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="d627c-104">FocusNavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="d627c-105">Das gesendete Objekt aus [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) mit dem [**NavigationReason**](#navigationreason) und dem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d627c-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span>  

## <span data-ttu-id="d627c-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="d627c-106">Methods</span></span>  

### <span data-ttu-id="d627c-107">requestFocus "</span><span class="sxs-lookup"><span data-stu-id="d627c-107">requestFocus</span></span>  

<span data-ttu-id="d627c-108">Wird aufgerufen, um den Fokus von der APP auf die WebView zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d627c-108">Called to move focus from the app to the webview.</span></span>  

### <span data-ttu-id="d627c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d627c-109">Parameters</span></span>  

<span data-ttu-id="d627c-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d627c-110">This method does not have parameters.</span></span>  

### <span data-ttu-id="d627c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d627c-111">Return value</span></span>  

<span data-ttu-id="d627c-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d627c-112">This method does not return a value.</span></span>  

## <span data-ttu-id="d627c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d627c-113">Properties</span></span>  

### <span data-ttu-id="d627c-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="d627c-114">navigationReason</span></span>  

<span data-ttu-id="d627c-115">Aufgezählter Typ **NavigationReason**, entweder "Links", "oben", "rechts" oder "unten".</span><span class="sxs-lookup"><span data-stu-id="d627c-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span>  

<span data-ttu-id="d627c-116">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d627c-116">This property is read-only.</span></span>  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### <span data-ttu-id="d627c-117">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="d627c-117">Property value</span></span>  

<span data-ttu-id="d627c-118">Geben Sie Folgendes ein: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="d627c-118">Type: **NavigationReason**</span></span>  

### <span data-ttu-id="d627c-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="d627c-119">originHeight</span></span>  

<span data-ttu-id="d627c-120">Die Position der Ursprungs Höhe des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d627c-120">The origin height location of the element to be given focus.</span></span>  

<span data-ttu-id="d627c-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d627c-121">This property is read-only.</span></span>  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### <span data-ttu-id="d627c-122">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="d627c-122">Property value</span></span>  

<span data-ttu-id="d627c-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d627c-123">Type: **float**</span></span>  

### <span data-ttu-id="d627c-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="d627c-124">originLeft</span></span>  

<span data-ttu-id="d627c-125">Die Position des Ausgangs Links des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d627c-125">The origin left location of the element to be given focus.</span></span>  

<span data-ttu-id="d627c-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d627c-126">This property is read-only.</span></span>  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### <span data-ttu-id="d627c-127">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="d627c-127">Property value</span></span>  

<span data-ttu-id="d627c-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d627c-128">Type: **float**</span></span>  

### <span data-ttu-id="d627c-129">originTop</span><span class="sxs-lookup"><span data-stu-id="d627c-129">originTop</span></span>  

<span data-ttu-id="d627c-130">Die ursprüngliche oberste Position des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d627c-130">The origin top location of the element to be given focus.</span></span>  

<span data-ttu-id="d627c-131">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d627c-131">This property is read-only.</span></span>  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### <span data-ttu-id="d627c-132">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="d627c-132">Property value</span></span>  

<span data-ttu-id="d627c-133">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d627c-133">Type: **float**</span></span>  

### <span data-ttu-id="d627c-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="d627c-134">originWidth</span></span>  

<span data-ttu-id="d627c-135">Die Position der Ursprungs Breite des Elements, dem der Fokus zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d627c-135">The origin width location of the element to be given focus.</span></span>  

<span data-ttu-id="d627c-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d627c-136">This property is read-only.</span></span>  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### <span data-ttu-id="d627c-137">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="d627c-137">Property value</span></span>  

<span data-ttu-id="d627c-138">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d627c-138">Type: **float**</span></span>  
