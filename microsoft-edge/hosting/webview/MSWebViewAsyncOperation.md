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
# MSWebViewAsyncOperation-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Gibt an, ob der Vorgang erfolgreich abgeschlossen wurde oder fehlgeschlagen ist.  

## Veranstaltungen  

### Ausführen  

Gibt an, dass der Vorgang abgeschlossen wurde.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### Ereignisinformationen  

|  |  |  
|:--- |:--- |  
| **Schnittstelle** | **Ereignis** |  
| **Synchron** |Ja |  
| **Blasen** |Nein |   
| **Abbrechbar** |Nein |  

### Fehler  

Gibt an, dass ein Fehler mit dem Vorgang aufgetreten ist.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### Ereignisinformationen  

|  |  |  
|:--- |:--- |  
| **Schnittstelle** | **Ereignis** |  
| **Synchron** | Ja |  
| **Blasen** | Nein |  
| **Abbrechbar** | Nein |  

## Methoden  

### start  

Wird aufgerufen, um die asynchrone Aufgabe zu starten.  

```javascript
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

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOMError**  

### OnComplete  

Der **Complete** -Ereignishandler.  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### Eigenschaftenwert  

Typ: **EventHandler**  

### OnError  

Der **Fehler** Ereignishandler.  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### Eigenschaftenwert  

Typ: **EventHandler**  

### ReadyState  

Beschreibt den Ready-Zustand des Objekts.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### Eigenschaftenwert  

Typ: **unsigned Short**  

### Ergebnis  

Das Ergebnis des Vorgangs.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein:  

### target  

Das Ziel des Vorgangs.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: [ **MSHTMLWebViewElement**](../webview.md)  

### Typ  

Der Typ des Vorgangs.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### Eigenschaftenwert  

Typ: **unsigned Short**  
