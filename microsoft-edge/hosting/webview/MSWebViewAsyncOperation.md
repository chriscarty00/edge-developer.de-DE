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
# MSWebViewAsyncOperation-Objekt

Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist. 

## Ereignisse

### Ausführen

Gibt an, dass der Vorgang abgeschlossen wurde. 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | **Ereignis**
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |        


### Fehler

Gibt an, dass ein Fehler mit dem Vorgang aufgetreten ist.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | **Ereignis**
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |            


## Methoden

### start

Wird aufgerufen, um die asynchrone Aufgabe zu starten. 

```js
MSWebViewAsyncOperation.start();
```

### Parameter

Diese Methode hat keine Parameter.

### Rückgabewert

Diese Methode gibt keinen Wert zurück.

## Eigenschaften

### Fehler

Der Fehler, der aufgetreten ist.

Diese Eigenschaft ist schreibgeschützt.

```js
var error = MSWebViewAsyncOperation.error;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOMError**

### OnComplete

Der **Complete** -Ereignishandler. 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### Eigenschaftenwert
Typ: **EventHandler**

### OnError

Der **Fehler** Ereignishandler. 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### Eigenschaftenwert
Typ: **EventHandler**

### ReadyState

Beschreibt den Ready-Zustand des Objekts.

Diese Eigenschaft ist schreibgeschützt.

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### Eigenschaftenwert
Typ: **unsigned Short**

### Ergebnis

Das Ergebnis des Vorgangs.

Diese Eigenschaft ist schreibgeschützt.

```js
var result = MSWebViewAsyncOperation.result;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein:

### target

Das Ziel des Vorgangs. 

Diese Eigenschaft ist schreibgeschützt.

```js
var target = MSWebViewAsyncOperation.target;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: [ **MSHTMLWebViewElement**](../webview.md)

### Typ

Der Typ des Vorgangs.

Diese Eigenschaft ist schreibgeschützt.

```js
var type = MSWebViewAsyncOperation.type;
```

#### Eigenschaftenwert
Typ: **unsigned Short**
