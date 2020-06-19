---
description: Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist
title: MSWebViewAsyncOperation-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752124"
---
# <span data-ttu-id="f6a15-104">MSWebViewAsyncOperation-Objekt</span><span class="sxs-lookup"><span data-stu-id="f6a15-104">MSWebViewAsyncOperation object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="f6a15-105">Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f6a15-105">Exposes whether the operation completed successfully or failed.</span></span>  

## <span data-ttu-id="f6a15-106">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="f6a15-106">Events</span></span>  

### <span data-ttu-id="f6a15-107">Ausführen</span><span class="sxs-lookup"><span data-stu-id="f6a15-107">complete</span></span>  

<span data-ttu-id="f6a15-108">Gibt an, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f6a15-108">Indicates that the operation completed.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### <span data-ttu-id="f6a15-109">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="f6a15-109">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="f6a15-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6a15-110">Interface</span></span>** | **<span data-ttu-id="f6a15-111">Ereignis</span><span class="sxs-lookup"><span data-stu-id="f6a15-111">Event</span></span>** |  
| **<span data-ttu-id="f6a15-112">Synchron</span><span class="sxs-lookup"><span data-stu-id="f6a15-112">Synchronous</span></span>** |<span data-ttu-id="f6a15-113">Ja</span><span class="sxs-lookup"><span data-stu-id="f6a15-113">Yes</span></span> |  
| **<span data-ttu-id="f6a15-114">Blasen</span><span class="sxs-lookup"><span data-stu-id="f6a15-114">Bubbles</span></span>** |<span data-ttu-id="f6a15-115">Nein</span><span class="sxs-lookup"><span data-stu-id="f6a15-115">No</span></span> |   
| **<span data-ttu-id="f6a15-116">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="f6a15-116">Cancelable</span></span>** |<span data-ttu-id="f6a15-117">Nein</span><span class="sxs-lookup"><span data-stu-id="f6a15-117">No</span></span> |  

### <span data-ttu-id="f6a15-118">Fehler</span><span class="sxs-lookup"><span data-stu-id="f6a15-118">error</span></span>  

<span data-ttu-id="f6a15-119">Gibt an, dass ein Fehler mit dem Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f6a15-119">Indicates that there was an error with the operation.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### <span data-ttu-id="f6a15-120">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="f6a15-120">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="f6a15-121">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6a15-121">Interface</span></span>** | **<span data-ttu-id="f6a15-122">Ereignis</span><span class="sxs-lookup"><span data-stu-id="f6a15-122">Event</span></span>** |  
| **<span data-ttu-id="f6a15-123">Synchron</span><span class="sxs-lookup"><span data-stu-id="f6a15-123">Synchronous</span></span>** | <span data-ttu-id="f6a15-124">Ja</span><span class="sxs-lookup"><span data-stu-id="f6a15-124">Yes</span></span> |  
| **<span data-ttu-id="f6a15-125">Blasen</span><span class="sxs-lookup"><span data-stu-id="f6a15-125">Bubbles</span></span>** | <span data-ttu-id="f6a15-126">Nein</span><span class="sxs-lookup"><span data-stu-id="f6a15-126">No</span></span> |  
| **<span data-ttu-id="f6a15-127">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="f6a15-127">Cancelable</span></span>** | <span data-ttu-id="f6a15-128">Nein</span><span class="sxs-lookup"><span data-stu-id="f6a15-128">No</span></span> |  

## <span data-ttu-id="f6a15-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6a15-129">Methods</span></span>  

### <span data-ttu-id="f6a15-130">start</span><span class="sxs-lookup"><span data-stu-id="f6a15-130">start</span></span>  

<span data-ttu-id="f6a15-131">Wird aufgerufen, um die asynchrone Aufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="f6a15-131">Called to start the async task.</span></span>  

```javascript
MSWebViewAsyncOperation.start();
```  

### <span data-ttu-id="f6a15-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6a15-132">Parameters</span></span>  

<span data-ttu-id="f6a15-133">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f6a15-133">This method does not have parameters.</span></span>  

### <span data-ttu-id="f6a15-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6a15-134">Return value</span></span>  

<span data-ttu-id="f6a15-135">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6a15-135">This method does not return a value.</span></span>  

## <span data-ttu-id="f6a15-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6a15-136">Properties</span></span>  

### <span data-ttu-id="f6a15-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="f6a15-137">error</span></span>  

<span data-ttu-id="f6a15-138">Der Fehler, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f6a15-138">The error that occurred.</span></span>  

<span data-ttu-id="f6a15-139">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f6a15-139">This property is read-only.</span></span>  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### <span data-ttu-id="f6a15-140">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-140">Property value</span></span>  

<span data-ttu-id="f6a15-141">Geben Sie Folgendes ein: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="f6a15-141">Type: **DOMError**</span></span>  

### <span data-ttu-id="f6a15-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="f6a15-142">oncomplete</span></span>  

<span data-ttu-id="f6a15-143">Der **Complete** -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="f6a15-143">The **complete** event handler.</span></span>  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### <span data-ttu-id="f6a15-144">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-144">Property value</span></span>  

<span data-ttu-id="f6a15-145">Typ: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="f6a15-145">Type: **EventHandler**</span></span>  

### <span data-ttu-id="f6a15-146">OnError</span><span class="sxs-lookup"><span data-stu-id="f6a15-146">onerror</span></span>  

<span data-ttu-id="f6a15-147">Der **Fehler** Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="f6a15-147">The **error** event handler.</span></span>  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### <span data-ttu-id="f6a15-148">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-148">Property value</span></span>  

<span data-ttu-id="f6a15-149">Typ: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="f6a15-149">Type: **EventHandler**</span></span>  

### <span data-ttu-id="f6a15-150">ReadyState</span><span class="sxs-lookup"><span data-stu-id="f6a15-150">readyState</span></span>  

<span data-ttu-id="f6a15-151">Beschreibt den Ready-Zustand des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6a15-151">Describes the ready state of the object.</span></span>  

<span data-ttu-id="f6a15-152">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f6a15-152">This property is read-only.</span></span>  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### <span data-ttu-id="f6a15-153">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-153">Property value</span></span>  

<span data-ttu-id="f6a15-154">Typ: **unsigned Short**</span><span class="sxs-lookup"><span data-stu-id="f6a15-154">Type: **unsigned short**</span></span>  

### <span data-ttu-id="f6a15-155">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f6a15-155">result</span></span>  

<span data-ttu-id="f6a15-156">Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f6a15-156">The result of the operation.</span></span>  

<span data-ttu-id="f6a15-157">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f6a15-157">This property is read-only.</span></span>  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### <span data-ttu-id="f6a15-158">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-158">Property value</span></span>  

<span data-ttu-id="f6a15-159">Geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="f6a15-159">Type: any</span></span>  

### <span data-ttu-id="f6a15-160">target</span><span class="sxs-lookup"><span data-stu-id="f6a15-160">target</span></span>  

<span data-ttu-id="f6a15-161">Das Ziel des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f6a15-161">The target of the operation.</span></span>  

<span data-ttu-id="f6a15-162">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f6a15-162">This property is read-only.</span></span>  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### <span data-ttu-id="f6a15-163">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-163">Property value</span></span>  

<span data-ttu-id="f6a15-164">Geben Sie Folgendes ein: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="f6a15-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>  

### <span data-ttu-id="f6a15-165">Typ</span><span class="sxs-lookup"><span data-stu-id="f6a15-165">type</span></span>  

<span data-ttu-id="f6a15-166">Der Typ des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f6a15-166">The type of the operation.</span></span>  

<span data-ttu-id="f6a15-167">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f6a15-167">This property is read-only.</span></span>  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### <span data-ttu-id="f6a15-168">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="f6a15-168">Property value</span></span>  

<span data-ttu-id="f6a15-169">Typ: **unsigned Short**</span><span class="sxs-lookup"><span data-stu-id="f6a15-169">Type: **unsigned short**</span></span>  
