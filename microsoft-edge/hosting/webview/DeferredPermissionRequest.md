---
description: Stellt eine verzögerte Anforderung für die Benutzerberechtigung für den Zugriff auf die Gerätefunktionalität dar
title: DeferredPermissionRequest-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567179"
---
# <span data-ttu-id="2b94e-104">DeferredPermissionRequest-Objekt</span><span class="sxs-lookup"><span data-stu-id="2b94e-104">DeferredPermissionRequest object</span></span>

<span data-ttu-id="2b94e-105">Stellt eine verzögerte Anforderung vom Inhalt der [WebView](../webview.md) für die Endbenutzer Berechtigung für den Zugriff auf spezielle Gerätefunktionen (wie Geolocation oder Zeiger Sperre) dar.</span><span class="sxs-lookup"><span data-stu-id="2b94e-105">Represents a deferred request by the content of the [webview](../webview.md) for end-user permission to access specialized device functionality (such as geolocation, or pointer lock).</span></span>

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## <span data-ttu-id="2b94e-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="2b94e-106">Methods</span></span>

### <span data-ttu-id="2b94e-107">ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2b94e-107">allow</span></span>

<span data-ttu-id="2b94e-108">Ermöglicht die Genehmigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="2b94e-108">Allows the request for permission.</span></span>

```js
deferredPermissionRequest.allow();
```

#### <span data-ttu-id="2b94e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b94e-109">Parameters</span></span>

<span data-ttu-id="2b94e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2b94e-110">This method has no parameters.</span></span>

#### <span data-ttu-id="2b94e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b94e-111">Return value</span></span>

<span data-ttu-id="2b94e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2b94e-112">This method does not return a value.</span></span>

### <span data-ttu-id="2b94e-113">verweigern</span><span class="sxs-lookup"><span data-stu-id="2b94e-113">deny</span></span>

<span data-ttu-id="2b94e-114">Verweigert die Genehmigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="2b94e-114">Denies the request for permission.</span></span>

```js
deferredPermissionRequest.deny();
```

#### <span data-ttu-id="2b94e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b94e-115">Parameters</span></span>

<span data-ttu-id="2b94e-116">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2b94e-116">This method has no parameters.</span></span>

#### <span data-ttu-id="2b94e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b94e-117">Return value</span></span>

<span data-ttu-id="2b94e-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2b94e-118">This method does not return a value.</span></span>

## <span data-ttu-id="2b94e-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b94e-119">Properties</span></span>

### <span data-ttu-id="2b94e-120">id</span><span class="sxs-lookup"><span data-stu-id="2b94e-120">id</span></span>

<span data-ttu-id="2b94e-121">Eine eindeutige ID, die verwendet werden kann, um die aktuelle DeferredPermissionRequest mit einem PermissionRequest-Objekt aus einem vorherigen MSWebViewPermissionRequested-Ereignis zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="2b94e-121">A unique ID that can be used to correlate the current DeferredPermissionRequest with a PermissionRequest object from a previous MSWebViewPermissionRequested event.</span></span> <span data-ttu-id="2b94e-122">Weitere Informationen finden Sie unter der **PermissionRequested. verzögert** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2b94e-122">See the **PermissionRequested.defer** method.</span></span>

<span data-ttu-id="2b94e-123">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b94e-123">This property is read-only.</span></span>

```js
var id = deferredPermissionRequest.id;
```

##### <span data-ttu-id="2b94e-124">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="2b94e-124">Property value</span></span>

<span data-ttu-id="2b94e-125">Typ: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="2b94e-125">Type: **Unsigned long**</span></span>

### <span data-ttu-id="2b94e-126">Typ</span><span class="sxs-lookup"><span data-stu-id="2b94e-126">type</span></span>

<span data-ttu-id="2b94e-127">Der Typ der anzufordernden Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="2b94e-127">The type of permission being requested.</span></span> <span data-ttu-id="2b94e-128">Hierbei kann es sich um einen der folgenden Zeichenfolgenwerte handeln:</span><span class="sxs-lookup"><span data-stu-id="2b94e-128">This may be one of the following string values:</span></span>

- <span data-ttu-id="2b94e-129">**Geolocation**: Zugriff auf Standortdaten über Navigator. Geolocation.</span><span class="sxs-lookup"><span data-stu-id="2b94e-129">**geolocation**: access to location data via navigator.geolocation.</span></span>
- <span data-ttu-id="2b94e-130">**unlimitedIndexedDBQuota**: zulassen, dass IndexedDB-APIs die übliche Größenbeschränkung für gespeicherte Daten ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2b94e-130">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>
- <span data-ttu-id="2b94e-131">**Medien**: Zugriff auf Mikrofon und Kamera über Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="2b94e-131">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>
- <span data-ttu-id="2b94e-132">**pointerlock**: Möglichkeit zum Sperren und Steuern des Mauszeigers über Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="2b94e-132">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>
- <span data-ttu-id="2b94e-133">**webbenachrichtigungen**: Möglichkeit zum Anzeigen von Desktopbenachrichtigungen über Fenster. Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2b94e-133">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>
- <span data-ttu-id="2b94e-134">**Bildschirm**: Möglichkeit zum Aufnehmen von Screenshots über die Media Capture-API.</span><span class="sxs-lookup"><span data-stu-id="2b94e-134">**screen**: ability to take screen shots via the Media Capture API.</span></span>
- <span data-ttu-id="2b94e-135">**immersiveview**: Möglichkeit zum Steuern einer VR-Anzeige.</span><span class="sxs-lookup"><span data-stu-id="2b94e-135">**immersiveview**: ability to control a VR display.</span></span>

<span data-ttu-id="2b94e-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b94e-136">This property is read-only.</span></span>

```js
var type = deferredPermissionRequest.type;
```

#### <span data-ttu-id="2b94e-137">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="2b94e-137">Property value</span></span>

<span data-ttu-id="2b94e-138">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b94e-138">Type: **String**</span></span>

### <span data-ttu-id="2b94e-139">Uri</span><span class="sxs-lookup"><span data-stu-id="2b94e-139">uri</span></span>

<span data-ttu-id="2b94e-140">Der Uniform Resource Identifier (URI) des Dokuments, das die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="2b94e-140">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>

<span data-ttu-id="2b94e-141">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b94e-141">This property is read-only.</span></span>

```js
var uri = deferredPermissionRequest.uri;
```

##### <span data-ttu-id="2b94e-142">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="2b94e-142">Property value</span></span>

<span data-ttu-id="2b94e-143">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2b94e-143">Type: **String**</span></span>

## <span data-ttu-id="2b94e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b94e-144">Requirements</span></span>

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong><span data-ttu-id="2b94e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b94e-145">Minimum supported client</span></span></strong> | <span data-ttu-id="2b94e-146">Windows 10 [nur Windows Store-Apps]</span><span class="sxs-lookup"><span data-stu-id="2b94e-146">Windows 10 [Windows Store apps only]</span></span> |
| <strong><span data-ttu-id="2b94e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b94e-147">Minimum supported server</span></span></strong> |            <span data-ttu-id="2b94e-148">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b94e-148">Not supported</span></span>             |
| <strong><span data-ttu-id="2b94e-149">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="2b94e-149">Minimum supported phone</span></span></strong>  |            <span data-ttu-id="2b94e-150">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b94e-150">Not supported</span></span>             |
