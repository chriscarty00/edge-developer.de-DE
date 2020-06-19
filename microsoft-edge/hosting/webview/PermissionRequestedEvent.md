---
description: Stellt Ereignisinformationen zur aktuellen Berechtigungsanforderung bereit
title: PermissionRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 9bb6cfdbe3cc430f109ea3a258b6c1a176b05da3
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752020"
---
# PermissionRequestedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Stellt Ereignisinformationen zur aktuellen Berechtigungsanforderung bereit.  

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

## Eigenschaften  

### permissionRequest  

Gibt ein **[PermissionRequest](permissionrequest.md)** -Objekt zurück, das die Berechtigungsanforderung des Endbenutzers darstellt, die durch den Inhalt der [WebView](../webview.md)-Datei erfolgt.  

Diese Eigenschaft ist schreibgeschützt.  
