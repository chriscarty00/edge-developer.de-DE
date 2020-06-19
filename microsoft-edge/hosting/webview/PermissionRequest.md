---
description: Enthält Informationen zu einer Berechtigungsanforderung
title: PermissionRequest-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752116"
---
# <span data-ttu-id="c372d-104">PermissionRequest-Objekt</span><span class="sxs-lookup"><span data-stu-id="c372d-104">PermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="c372d-105">Enthält Informationen zu einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="c372d-105">Provides information about a permission request.</span></span> <span data-ttu-id="c372d-106">Dieses Objekt ist über die permissionRequest-Eigenschaft der Ereignisargumente aus dem [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) -WebView-Ereignis verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c372d-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## <span data-ttu-id="c372d-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="c372d-107">Methods</span></span>  

### <span data-ttu-id="c372d-108">ermöglichen</span><span class="sxs-lookup"><span data-stu-id="c372d-108">allow</span></span>  

<span data-ttu-id="c372d-109">Ermöglicht die Genehmigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="c372d-109">Allows the request for permission.</span></span>  

#### <span data-ttu-id="c372d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c372d-110">Parameters</span></span>  

<span data-ttu-id="c372d-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c372d-111">This method has no parameters.</span></span>  

#### <span data-ttu-id="c372d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c372d-112">Return value</span></span>  

<span data-ttu-id="c372d-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c372d-113">This method does not return a value.</span></span>  

### <span data-ttu-id="c372d-114">zurückstellen</span><span class="sxs-lookup"><span data-stu-id="c372d-114">defer</span></span>  

<span data-ttu-id="c372d-115">Wenn Sie eine PermissionRequest nicht synchron zulassen oder ablehnen möchten, benötigen Sie Zeit für die Interaktion mit dem Benutzer oder das Ausführen einer anderen asynchronen Aktion, indem Sie auf der PermissionRequest den Wert zurücksetzen () aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c372d-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span>  <span data-ttu-id="c372d-116">Das PermissionRequest wird nun als DeferredPermissionRequest von getDeferredPermissionRequests und getDeferredPermissionRequestById zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="c372d-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span>  <span data-ttu-id="c372d-117">Sie können den aktuellen PermissionRequest mit dem entsprechenden DeferredPermissionRequest über die entsprechende ID-Eigenschaft korrelieren.</span><span class="sxs-lookup"><span data-stu-id="c372d-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>  

#### <span data-ttu-id="c372d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c372d-118">Parameters</span></span>  

<span data-ttu-id="c372d-119">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c372d-119">This method has no parameters.</span></span>  

#### <span data-ttu-id="c372d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c372d-120">Return value</span></span>  

<span data-ttu-id="c372d-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c372d-121">This method does not return a value.</span></span>  

### <span data-ttu-id="c372d-122">verweigern</span><span class="sxs-lookup"><span data-stu-id="c372d-122">deny</span></span>  

<span data-ttu-id="c372d-123">Verweigert die Genehmigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="c372d-123">Denies the request for permission.</span></span>  

#### <span data-ttu-id="c372d-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="c372d-124">Parameters</span></span>  

<span data-ttu-id="c372d-125">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c372d-125">This method has no parameters.</span></span>  

#### <span data-ttu-id="c372d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c372d-126">Return value</span></span>  

<span data-ttu-id="c372d-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c372d-127">This method does not return a value.</span></span>  

## <span data-ttu-id="c372d-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c372d-128">Properties</span></span>  

### <span data-ttu-id="c372d-129">id</span><span class="sxs-lookup"><span data-stu-id="c372d-129">id</span></span>  

<span data-ttu-id="c372d-130">Eine eindeutige ID, die verwendet werden kann, um die aktuelle PermissionRequest mit einem entsprechenden DeferredPermissionRequest zu korrelieren, wenn die Verzögerungsmethode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c372d-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span>  <span data-ttu-id="c372d-131">Weitere Informationen finden Sie unter verzögerte Methode.</span><span class="sxs-lookup"><span data-stu-id="c372d-131">See the defer method.</span></span>  

<span data-ttu-id="c372d-132">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c372d-132">This property is read-only.</span></span>  

##### <span data-ttu-id="c372d-133">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="c372d-133">Property value</span></span>  

<span data-ttu-id="c372d-134">Typ: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="c372d-134">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="c372d-135">Zustand</span><span class="sxs-lookup"><span data-stu-id="c372d-135">state</span></span>  

<span data-ttu-id="c372d-136">Gibt "unknown", "verzögern", "zulassen" oder "verweigern" zurück, um den aktuellen Status der Berechtigungsanforderung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c372d-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span>  <span data-ttu-id="c372d-137">Die Zustands Zeichenfolge entspricht der Methode allow, Deny oder reverzögerung wurde als "zuletzt" oder "unbekannt" bezeichnet, wenn keine der Methoden aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c372d-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>  

<span data-ttu-id="c372d-138">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c372d-138">This property is read-only.</span></span>  

#### <span data-ttu-id="c372d-139">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="c372d-139">Property value</span></span>  

<span data-ttu-id="c372d-140">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c372d-140">Type: **String**</span></span>  

### <span data-ttu-id="c372d-141">Typ</span><span class="sxs-lookup"><span data-stu-id="c372d-141">type</span></span>  

<span data-ttu-id="c372d-142">Der Typ der anzufordernden Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="c372d-142">The type of permission being requested.</span></span> <span data-ttu-id="c372d-143">Hierbei kann es sich um einen der folgenden Zeichenfolgenwerte handeln:</span><span class="sxs-lookup"><span data-stu-id="c372d-143">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="c372d-144">**Geolocation**: Zugriff auf Standortdaten über Navigator. Geolocation.</span><span class="sxs-lookup"><span data-stu-id="c372d-144">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="c372d-145">**unlimitedIndexedDBQuota**: zulassen, dass IndexedDB-APIs die übliche Größenbeschränkung für gespeicherte Daten ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c372d-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="c372d-146">**Medien**: Zugriff auf Mikrofon und Kamera über Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="c372d-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="c372d-147">**pointerlock**: Möglichkeit zum Sperren und Steuern des Mauszeigers über Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="c372d-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="c372d-148">**webbenachrichtigungen**: Möglichkeit zum Anzeigen von Desktopbenachrichtigungen über Fenster. Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c372d-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="c372d-149">**Bildschirm**: Möglichkeit zum Aufnehmen von Screenshots über die Media Capture-API.</span><span class="sxs-lookup"><span data-stu-id="c372d-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="c372d-150">**immersiveview**: Möglichkeit zum Steuern einer VR-Anzeige.</span><span class="sxs-lookup"><span data-stu-id="c372d-150">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="c372d-151">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c372d-151">This property is read-only.</span></span>  

#### <span data-ttu-id="c372d-152">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="c372d-152">Property value</span></span>  

<span data-ttu-id="c372d-153">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c372d-153">Type: **String**</span></span>  

### <span data-ttu-id="c372d-154">Uri</span><span class="sxs-lookup"><span data-stu-id="c372d-154">uri</span></span>  

<span data-ttu-id="c372d-155">Der Uniform Resource Identifier (URI) des Dokuments, das die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c372d-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="c372d-156">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c372d-156">This property is read-only.</span></span>  

#### <span data-ttu-id="c372d-157">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="c372d-157">Property value</span></span>  

<span data-ttu-id="c372d-158">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c372d-158">Type: **String**</span></span>  
