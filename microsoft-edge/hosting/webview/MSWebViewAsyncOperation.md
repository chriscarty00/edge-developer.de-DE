---
description: Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist
title: MSWebViewAsyncOperation-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567170"
---
# <span data-ttu-id="5f1a2-104">MSWebViewAsyncOperation-Objekt</span><span class="sxs-lookup"><span data-stu-id="5f1a2-104">MSWebViewAsyncOperation object</span></span>

<span data-ttu-id="5f1a2-105">Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-105">Exposes whether the operation completed successfully or failed.</span></span> 

## <span data-ttu-id="5f1a2-106">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5f1a2-106">Events</span></span>

### <span data-ttu-id="5f1a2-107">Ausführen</span><span class="sxs-lookup"><span data-stu-id="5f1a2-107">complete</span></span>

<span data-ttu-id="5f1a2-108">Gibt an, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-108">Indicates that the operation completed.</span></span> 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### <span data-ttu-id="5f1a2-109">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="5f1a2-109">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="5f1a2-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5f1a2-110">Interface</span></span>** | **<span data-ttu-id="5f1a2-111">Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f1a2-111">Event</span></span>**
|**<span data-ttu-id="5f1a2-112">Synchron</span><span class="sxs-lookup"><span data-stu-id="5f1a2-112">Synchronous</span></span>** |<span data-ttu-id="5f1a2-113">Ja</span><span class="sxs-lookup"><span data-stu-id="5f1a2-113">Yes</span></span> |    
|**<span data-ttu-id="5f1a2-114">Blasen</span><span class="sxs-lookup"><span data-stu-id="5f1a2-114">Bubbles</span></span>**     |<span data-ttu-id="5f1a2-115">Nein</span><span class="sxs-lookup"><span data-stu-id="5f1a2-115">No</span></span> |   
|**<span data-ttu-id="5f1a2-116">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="5f1a2-116">Cancelable</span></span>**  |<span data-ttu-id="5f1a2-117">Nein</span><span class="sxs-lookup"><span data-stu-id="5f1a2-117">No</span></span> |        


### <span data-ttu-id="5f1a2-118">Fehler</span><span class="sxs-lookup"><span data-stu-id="5f1a2-118">error</span></span>

<span data-ttu-id="5f1a2-119">Gibt an, dass ein Fehler mit dem Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-119">Indicates that there was an error with the operation.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### <span data-ttu-id="5f1a2-120">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="5f1a2-120">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="5f1a2-121">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5f1a2-121">Interface</span></span>** | **<span data-ttu-id="5f1a2-122">Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f1a2-122">Event</span></span>**
|**<span data-ttu-id="5f1a2-123">Synchron</span><span class="sxs-lookup"><span data-stu-id="5f1a2-123">Synchronous</span></span>** |<span data-ttu-id="5f1a2-124">Ja</span><span class="sxs-lookup"><span data-stu-id="5f1a2-124">Yes</span></span> |    
|**<span data-ttu-id="5f1a2-125">Blasen</span><span class="sxs-lookup"><span data-stu-id="5f1a2-125">Bubbles</span></span>**     |<span data-ttu-id="5f1a2-126">Nein</span><span class="sxs-lookup"><span data-stu-id="5f1a2-126">No</span></span> |   
|**<span data-ttu-id="5f1a2-127">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="5f1a2-127">Cancelable</span></span>**  |<span data-ttu-id="5f1a2-128">Nein</span><span class="sxs-lookup"><span data-stu-id="5f1a2-128">No</span></span> |            


## <span data-ttu-id="5f1a2-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="5f1a2-129">Methods</span></span>

### <span data-ttu-id="5f1a2-130">start</span><span class="sxs-lookup"><span data-stu-id="5f1a2-130">start</span></span>

<span data-ttu-id="5f1a2-131">Wird aufgerufen, um die asynchrone Aufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-131">Called to start the async task.</span></span> 

```js
MSWebViewAsyncOperation.start();
```

### <span data-ttu-id="5f1a2-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f1a2-132">Parameters</span></span>

<span data-ttu-id="5f1a2-133">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-133">This method does not have parameters.</span></span>

### <span data-ttu-id="5f1a2-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-134">Return value</span></span>

<span data-ttu-id="5f1a2-135">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-135">This method does not return a value.</span></span>

## <span data-ttu-id="5f1a2-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f1a2-136">Properties</span></span>

### <span data-ttu-id="5f1a2-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="5f1a2-137">error</span></span>

<span data-ttu-id="5f1a2-138">Der Fehler, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-138">The error that occured.</span></span>

<span data-ttu-id="5f1a2-139">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-139">This property is read-only.</span></span>

```js
var error = MSWebViewAsyncOperation.error;
```

#### <span data-ttu-id="5f1a2-140">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-140">Property value</span></span>
<span data-ttu-id="5f1a2-141">Geben Sie Folgendes ein: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="5f1a2-141">Type: **DOMError**</span></span>

### <span data-ttu-id="5f1a2-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="5f1a2-142">oncomplete</span></span>

<span data-ttu-id="5f1a2-143">Der **Complete** -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-143">The **complete** event handler.</span></span> 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### <span data-ttu-id="5f1a2-144">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-144">Property value</span></span>
<span data-ttu-id="5f1a2-145">Typ: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="5f1a2-145">Type: **EventHandler**</span></span>

### <span data-ttu-id="5f1a2-146">OnError</span><span class="sxs-lookup"><span data-stu-id="5f1a2-146">onerror</span></span>

<span data-ttu-id="5f1a2-147">Der **Fehler** Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-147">The **error** event handler.</span></span> 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### <span data-ttu-id="5f1a2-148">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-148">Property value</span></span>
<span data-ttu-id="5f1a2-149">Typ: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="5f1a2-149">Type: **EventHandler**</span></span>

### <span data-ttu-id="5f1a2-150">ReadyState</span><span class="sxs-lookup"><span data-stu-id="5f1a2-150">readyState</span></span>

<span data-ttu-id="5f1a2-151">Beschreibt den Ready-Zustand des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-151">Describes the ready state of the object.</span></span>

<span data-ttu-id="5f1a2-152">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-152">This property is read-only.</span></span>

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### <span data-ttu-id="5f1a2-153">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-153">Property value</span></span>
<span data-ttu-id="5f1a2-154">Typ: **unsigned Short**</span><span class="sxs-lookup"><span data-stu-id="5f1a2-154">Type: **unsigned short**</span></span>

### <span data-ttu-id="5f1a2-155">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="5f1a2-155">result</span></span>

<span data-ttu-id="5f1a2-156">Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-156">The result of the operation.</span></span>

<span data-ttu-id="5f1a2-157">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-157">This property is read-only.</span></span>

```js
var result = MSWebViewAsyncOperation.result;
```

#### <span data-ttu-id="5f1a2-158">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-158">Property value</span></span>
<span data-ttu-id="5f1a2-159">Geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="5f1a2-159">Type: any</span></span>

### <span data-ttu-id="5f1a2-160">target</span><span class="sxs-lookup"><span data-stu-id="5f1a2-160">target</span></span>

<span data-ttu-id="5f1a2-161">Das Ziel des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-161">The target of the operation.</span></span> 

<span data-ttu-id="5f1a2-162">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-162">This property is read-only.</span></span>

```js
var target = MSWebViewAsyncOperation.target;
```

#### <span data-ttu-id="5f1a2-163">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-163">Property value</span></span>
<span data-ttu-id="5f1a2-164">Geben Sie Folgendes ein: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="5f1a2-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>

### <span data-ttu-id="5f1a2-165">Typ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-165">type</span></span>

<span data-ttu-id="5f1a2-166">Der Typ des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-166">The type of the operation.</span></span>

<span data-ttu-id="5f1a2-167">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-167">This property is read-only.</span></span>

```js
var type = MSWebViewAsyncOperation.type;
```

#### <span data-ttu-id="5f1a2-168">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="5f1a2-168">Property value</span></span>
<span data-ttu-id="5f1a2-169">Typ: **unsigned Short**</span><span class="sxs-lookup"><span data-stu-id="5f1a2-169">Type: **unsigned short**</span></span>
