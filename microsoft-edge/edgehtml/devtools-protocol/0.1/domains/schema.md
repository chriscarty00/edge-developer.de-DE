---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Schemadomäne. Stellt Informationen zum Protokollschema zur Verfügung.
title: Schemadomäne – DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398861"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a>Schemadomäne – DevTools Protocol Version 0.1 (EdgeHTML)  

Stellt Informationen zum Protokollschema zur Verfügung.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [Methoden](#methods) | [getDomains](#getdomains) |  
| [Typen](#types) | [Domäne](#domain) |  

## <a name="methods"></a>Methoden  

### <a name="getdomains"></a>getDomains  

Gibt unterstützte Domänen zurück.  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| domänen | [Domain[]](#domain) | Liste der unterstützten Domänen. |  

---  

## <a name="types"></a>Typen  

### <a name="domain-object"></a>Domänenobjekt  

<a name="domain"></a>  

Beschreibung der Protokolldomäne.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| name | `string` | Domänenname. |  
| version | `string` | Domänenversion. |  

---  
