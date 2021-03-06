---
description: DevTools Protocol Version 0.2 (EdgeHTML)-Referenz für die Schemadomäne. Stellt Informationen zum Protokollschema zur Verfügung.
title: Schemadomäne – DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398147"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a>Schemadomäne – DevTools Protocol Version 0.2 (EdgeHTML)  

Stellt Informationen zum Protokollschema zur Verfügung.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [Methoden](#methods) | [getDomains](#getdomains) |  
| [Typen](#types) | [Domänenobjekt](#domain) |  

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
