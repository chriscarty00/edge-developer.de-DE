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
# DeferredPermissionRequest-Objekt

Stellt eine verzögerte Anforderung vom Inhalt der [WebView](../webview.md) für die Endbenutzer Berechtigung für den Zugriff auf spezielle Gerätefunktionen (wie Geolocation oder Zeiger Sperre) dar.

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

## Methoden

### ermöglichen

Ermöglicht die Genehmigungsanforderung.

```js
deferredPermissionRequest.allow();
```

#### Parameter

Diese Methode hat keine Parameter.

#### Rückgabewert

Diese Methode gibt keinen Wert zurück.

### verweigern

Verweigert die Genehmigungsanforderung.

```js
deferredPermissionRequest.deny();
```

#### Parameter

Diese Methode hat keine Parameter.

#### Rückgabewert

Diese Methode gibt keinen Wert zurück.

## Eigenschaften

### id

Eine eindeutige ID, die verwendet werden kann, um die aktuelle DeferredPermissionRequest mit einem PermissionRequest-Objekt aus einem vorherigen MSWebViewPermissionRequested-Ereignis zu korrelieren. Weitere Informationen finden Sie unter der **PermissionRequested. verzögert** -Methode.

Diese Eigenschaft ist schreibgeschützt.

```js
var id = deferredPermissionRequest.id;
```

##### Eigenschaftenwert

Typ: **unsigned long**

### Typ

Der Typ der anzufordernden Berechtigung. Hierbei kann es sich um einen der folgenden Zeichenfolgenwerte handeln:

- **Geolocation**: Zugriff auf Standortdaten über Navigator. Geolocation.
- **unlimitedIndexedDBQuota**: zulassen, dass IndexedDB-APIs die übliche Größenbeschränkung für gespeicherte Daten ignorieren.
- **Medien**: Zugriff auf Mikrofon und Kamera über Navigator. getUserMedia.
- **pointerlock**: Möglichkeit zum Sperren und Steuern des Mauszeigers über Element. requestPointerLock.
- **webbenachrichtigungen**: Möglichkeit zum Anzeigen von Desktopbenachrichtigungen über Fenster. Benachrichtigung.
- **Bildschirm**: Möglichkeit zum Aufnehmen von Screenshots über die Media Capture-API.
- **immersiveview**: Möglichkeit zum Steuern einer VR-Anzeige.

Diese Eigenschaft ist schreibgeschützt.

```js
var type = deferredPermissionRequest.type;
```

#### Eigenschaftenwert

Typ: **Zeichenfolge**

### Uri

Der Uniform Resource Identifier (URI) des Dokuments, das die Berechtigung anfordert.

Diese Eigenschaft ist schreibgeschützt.

```js
var uri = deferredPermissionRequest.uri;
```

##### Eigenschaftenwert

Typ: **Zeichenfolge**

## Anforderungen

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong>Unterstützte Mindestversion (Client)</strong> | Windows 10 [nur Windows Store-Apps] |
| <strong>Unterstützte Mindestversion (Server)</strong> |            Nicht unterstützt.             |
| <strong>Unterstützte Mindestversion (Telefon)</strong>  |            Nicht unterstützt.             |
