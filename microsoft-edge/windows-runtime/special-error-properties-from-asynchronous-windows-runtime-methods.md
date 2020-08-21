---
title: Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a1fccf1cec811501b94e7da4aa20b69d93754f62
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942068"
---
# Spezielle Fehlereigenschaften von asynchronen Windows-Runtime-Methoden  

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
