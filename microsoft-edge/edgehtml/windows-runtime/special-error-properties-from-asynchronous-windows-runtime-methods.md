---
description: Spezielle Fehlereigenschaften von asynchronen Windows-Runtime-Methoden.
title: Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3557d0097d632f4058e46acbff748f7177d24ab1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233869"
---
# Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem Tiefpunkt in der Aufrufliste ausgelöst wird.  Das JavaScript `Error` -Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die APP im Debugmodus ausgeführt wird.  
  
## Spezielle Fehlereigenschaften  

Ein Fehlerobjekt, das aus einem fehlerhaften Windows-Runtime-asynchronen Vorgang im Debugmodus resultiert, weist die folgenden speziellen Eigenschaften auf:  

*   `asyncOpSource` \ (Object \) Ruft Informationen über die ursprüngliche Position ab, an der der Aufruf, der einen Fehler erzeugt hat, erfolgte.  Die Eigenschaft `asyncOpSource.originatingCall` \ (Zeichenfolge \) zeigt die Position im Code des Benutzers an, der den asynchronen Vorgang initiiert hat.  
*   asyncOpType \ (Zeichenfolge \) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.  
    
Weitere Informationen zu Fehlern mit asynchronen Vorgängen finden Sie unter:  
  
*   [Behandeln von Fehlern mit Zusagen][PreviousVersionsWindowsAppsHh700337]  
*   [Problembehandlung für Windows-Runtime-Fehler][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Versprechungen (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Behandeln von Problemen mit Windows-Runtime-Fehlern (HTML) | Microsoft docs"  
