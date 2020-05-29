---
description: Stellt Ereignisinformationen zur aktuellen Berechtigungsanforderung bereit
title: PermissionRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/04/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 07fccebc9e061d4ee7a85e48271aaf9c0574e1ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568593"
---
# <span data-ttu-id="ff5f0-104">PermissionRequestedEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="ff5f0-104">PermissionRequestedEvent object</span></span>

<span data-ttu-id="ff5f0-105">Stellt Ereignisinformationen zur aktuellen Berechtigungsanforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="ff5f0-105">Provides event information about the current permission request.</span></span>

```js
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

## <span data-ttu-id="ff5f0-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff5f0-106">Properties</span></span>

### <span data-ttu-id="ff5f0-107">permissionRequest</span><span class="sxs-lookup"><span data-stu-id="ff5f0-107">permissionRequest</span></span>

<span data-ttu-id="ff5f0-108">Gibt ein **[PermissionRequest](permissionrequest.md)** -Objekt zurück, das die Berechtigungsanforderung des Endbenutzers darstellt, die durch den Inhalt der [WebView](../webview.md)-Datei erfolgt.</span><span class="sxs-lookup"><span data-stu-id="ff5f0-108">Returns a **[PermissionRequest](permissionrequest.md)** object that represents the end-user permission request made by content of the [webview](../webview.md).</span></span>

<span data-ttu-id="ff5f0-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ff5f0-109">This property is read-only.</span></span>
