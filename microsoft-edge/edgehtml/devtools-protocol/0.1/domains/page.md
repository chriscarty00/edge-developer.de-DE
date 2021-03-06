---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Seitendomäne. Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.
title: Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399148"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a>Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)  

Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [**Methoden**](#methods) | [aktivieren](#enable), [deaktivieren](#disable), [navigieren](#navigate) |  
| [**Typen**](#types) | [FrameId](#frameid) |  

## <a name="methods"></a>Methoden  

### <a name="enable"></a>Aktivieren  

Aktiviert Seitendomänenbenachrichtigungen.  

&nbsp;  

---  

### <a name="disable"></a>Deaktivieren   

Deaktiviert Seitendomänenbenachrichtigungen.  

&nbsp;  

---  

### <a name="navigate"></a>Navigieren  

Navigiert die aktuelle Seite zur angegebenen URL.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| URL | `string` | URL, zu der die Seite navigiert werden soll. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | **Experimental**.  Frame-ID, die navigiert wird. |  

---  

## <a name="types"></a>Typen  

### <a name="frameid-string"></a>FrameId-Zeichenfolge  

<a name="frameid"></a>  

Eindeutige Frame-ID.  

&nbsp;  

---  
