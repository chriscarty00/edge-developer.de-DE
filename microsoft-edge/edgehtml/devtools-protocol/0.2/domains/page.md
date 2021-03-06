---
description: DevTools Protocol Version 0.2 (EdgeHTML)-Referenz für die Seitendomäne. Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.
title: Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398847"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a>Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)  

Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [Methoden](#methods) | [aktivieren](#enable), [deaktivieren](#disable), [navigieren](#navigate), [getFrameTree](#getframetree) |  
| [Veranstaltungen](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |  
| [Typen](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |  

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
| frameId \(optional\) | [FrameId](#frameid) | Frame-ID zum Navigieren.  Wenn dieser Wert nicht angegeben ist, navigiert er auf der oberen Seite. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Frame-ID, die navigiert wird. |  

---  

### <a name="getframetree"></a>getFrameTree  

Gibt die aktuelle Struktur der Framestruktur zurück.  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| frameTree | [FrameTree](#frametree) | Präsentieren der Struktur der Framestruktur. |  

---  

## <a name="events"></a>Veranstaltungen  

### <a name="frameattached"></a>frameAttached  

Wird ausgelöst, wenn frame an das übergeordnete Element angefügt wurde.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID des angefügten Frames. |  
| parentFrameId | [FrameId](#frameid) | Übergeordneter Framebezeichner. |  
| stack \(optional\) | [Runtime.StackTrace](./runtime.md#stacktrace) | JavaScript stack trace of when frame was attached, only set if frame initiated from script. |  

---  

### <a name="framedetached"></a>frameDetached  

Wird ausgelöst, wenn der Frame vom übergeordneten Element getrennt wurde.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID des getrennten Frames. |  

---  

### <a name="framenavigated"></a>frameNavigated  

Wird ausgelöst, nachdem die Navigation des Frames abgeschlossen wurde.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| frame | [Frame](#frame) | Frame-Objekt. |  

---  

### <a name="loadeventfired"></a>loadEventFired  

Entspricht dem `window.onload` Ereignis.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| zeitstempel | `number` | Anzahl der Millisekunden seit der Epoche. |  

---  

### <a name="domcontenteventfired"></a>domContentEventFired  

Entspricht dem `document.onDOMContentLoaded` Ereignis.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| zeitstempel | `number` | Anzahl der Millisekunden seit der Epoche. |  

---  

## <a name="types"></a>Typen  

### <a name="frameid-string"></a>FrameId-Zeichenfolge  

<a name="frameid"></a>  

Eindeutige Frame-ID.  

&nbsp;  

---  

### <a name="frame-object"></a>Frame-Objekt  

<a name="frame"></a>  

Informationen zum Frame auf der Seite.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| id | [FrameId](#frameid) | Frame eindeutiger Bezeichner. |  
| parentId \(optional\) | [FrameId](#frameid) | Eindeutiger Bezeichner des übergeordneten Frames. |  
| Name \(optional\) | `string` | Framename, wie im Tag angegeben. |  
| URL | `string` | Die URL des Framedokuments. |  
| securityOrigin | `string` | Der Sicherheitsherkunft des Framedokuments. |  
| mimeType | `string` | Der mimeType des Framedokuments, wie vom Browser bestimmt. |  

---  

### <a name="frametree-object"></a>FrameTree-Objekt  

<a name="frametree"></a>  

Informationen zur Framehierarchie.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| frame | [Frame](#frame) | Frameinformationen für dieses Strukturelement. |  
| childFrames \(optional\) | [FrameTree[]](#frametree) | Untergeordnete Frames. |  

---  
