---
description: Das gesendete Objekt aus einem fokusereignis, das den Grund und die Position der Navigation enthält
title: FocusNavigationEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567177"
---
# FocusNavigationEvent-Objekt

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

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **NavigationReason**

### originHeight

Die Position der Ursprungs Höhe des Elements, dem der Fokus zugewiesen werden soll.

Diese Eigenschaft ist schreibgeschützt.

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### Eigenschaftenwert
Typ: **float**

### originLeft

Die Position des Ausgangs Links des Elements, dem der Fokus zugewiesen werden soll.

Diese Eigenschaft ist schreibgeschützt.

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### Eigenschaftenwert
Typ: **float**

### originTop

Die ursprüngliche oberste Position des Elements, dem der Fokus zugewiesen werden soll.

Diese Eigenschaft ist schreibgeschützt.

```js
var originTop = FocusNavigationEvent.originTop;
```

#### Eigenschaftenwert
Typ: **float**

### originWidth

Die Position der Ursprungs Breite des Elements, dem der Fokus zugewiesen werden soll.

Diese Eigenschaft ist schreibgeschützt.

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### Eigenschaftenwert
Typ: **float**

