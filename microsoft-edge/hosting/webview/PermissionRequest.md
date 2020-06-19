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
# PermissionRequest-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Enthält Informationen zu einer Berechtigungsanforderung. Dieses Objekt ist über die permissionRequest-Eigenschaft der Ereignisargumente aus dem [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) -WebView-Ereignis verfügbar.  

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

## Methoden  

### ermöglichen  

Ermöglicht die Genehmigungsanforderung.  

#### Parameter  

Diese Methode hat keine Parameter.  

#### Rückgabewert  

Diese Methode gibt keinen Wert zurück.  

### zurückstellen  

Wenn Sie eine PermissionRequest nicht synchron zulassen oder ablehnen möchten, benötigen Sie Zeit für die Interaktion mit dem Benutzer oder das Ausführen einer anderen asynchronen Aktion, indem Sie auf der PermissionRequest den Wert zurücksetzen () aufrufen.  Das PermissionRequest wird nun als DeferredPermissionRequest von getDeferredPermissionRequests und getDeferredPermissionRequestById zur Verfügung stehen.  Sie können den aktuellen PermissionRequest mit dem entsprechenden DeferredPermissionRequest über die entsprechende ID-Eigenschaft korrelieren.  

#### Parameter  

Diese Methode hat keine Parameter.  

#### Rückgabewert  

Diese Methode gibt keinen Wert zurück.  

### verweigern  

Verweigert die Genehmigungsanforderung.  

#### Parameter  

Diese Methode hat keine Parameter.  

#### Rückgabewert  

Diese Methode gibt keinen Wert zurück.  

## Eigenschaften  

### id  

Eine eindeutige ID, die verwendet werden kann, um die aktuelle PermissionRequest mit einem entsprechenden DeferredPermissionRequest zu korrelieren, wenn die Verzögerungsmethode verwendet wird.  Weitere Informationen finden Sie unter verzögerte Methode.  

Diese Eigenschaft ist schreibgeschützt.  

##### Eigenschaftenwert  

Typ: **unsigned long**  

### Zustand  

Gibt "unknown", "verzögern", "zulassen" oder "verweigern" zurück, um den aktuellen Status der Berechtigungsanforderung anzugeben.  Die Zustands Zeichenfolge entspricht der Methode allow, Deny oder reverzögerung wurde als "zuletzt" oder "unbekannt" bezeichnet, wenn keine der Methoden aufgerufen wurde.  

Diese Eigenschaft ist schreibgeschützt.  

#### Eigenschaftenwert  

Typ: **Zeichenfolge**  

### Typ  

Der Typ der anzufordernden Berechtigung. Hierbei kann es sich um einen der folgenden Zeichenfolgenwerte handeln:  

*   **Geolocation**: Zugriff auf Standortdaten über Navigator. Geolocation.  
*   **unlimitedIndexedDBQuota**: zulassen, dass IndexedDB-APIs die übliche Größenbeschränkung für gespeicherte Daten ignorieren.  
*   **Medien**: Zugriff auf Mikrofon und Kamera über Navigator. getUserMedia.  
*   **pointerlock**: Möglichkeit zum Sperren und Steuern des Mauszeigers über Element. requestPointerLock.  
*   **webbenachrichtigungen**: Möglichkeit zum Anzeigen von Desktopbenachrichtigungen über Fenster. Benachrichtigung.  
*   **Bildschirm**: Möglichkeit zum Aufnehmen von Screenshots über die Media Capture-API.  
*   **immersiveview**: Möglichkeit zum Steuern einer VR-Anzeige.  

Diese Eigenschaft ist schreibgeschützt.  

#### Eigenschaftenwert  

Typ: **Zeichenfolge**  

### Uri  

Der Uniform Resource Identifier (URI) des Dokuments, das die Berechtigung anfordert.  

Diese Eigenschaft ist schreibgeschützt.  

#### Eigenschaftenwert  

Typ: **Zeichenfolge**  
