---
description: Das gesendete Objekt aus einem fokusereignis, das den Grund und die Position der Navigation enthält
title: FocusNavigationEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752164"
---
# FocusNavigationEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Das gesendete Objekt aus [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) mit dem [**NavigationReason**](#navigationreason) und dem Speicherort.  

## Methoden  

### requestFocus "  

Wird aufgerufen, um den Fokus von der APP auf die WebView zu verschieben.  

### Parameter  

Diese Methode hat keine Parameter.  

### Rückgabewert  

Diese Methode gibt keinen Wert zurück.  

## Eigenschaften  

### navigationReason  

Aufgezählter Typ **NavigationReason**, entweder "Links", "oben", "rechts" oder "unten".  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **NavigationReason**  

### originHeight  

Die Position der Ursprungs Höhe des Elements, dem der Fokus zugewiesen werden soll.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### Eigenschaftenwert  

Typ: **float**  

### originLeft  

Die Position des Ausgangs Links des Elements, dem der Fokus zugewiesen werden soll.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### Eigenschaftenwert  

Typ: **float**  

### originTop  

Die ursprüngliche oberste Position des Elements, dem der Fokus zugewiesen werden soll.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### Eigenschaftenwert  

Typ: **float**  

### originWidth  

Die Position der Ursprungs Breite des Elements, dem der Fokus zugewiesen werden soll.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### Eigenschaftenwert  

Typ: **float**  
