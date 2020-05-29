---
title: Spezielle Fehlereigenschaften von asynchronen Windows-Runtime-Methoden
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 5cf2604e26c84e769cf44e0879ee137cbfbe8b90
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568714"
---
# Spezielle Fehlereigenschaften von asynchronen Windows-Runtime-Methoden  

Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem Tiefpunkt in der Aufrufliste ausgelöst wird. Das JavaScript `Error` -Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die APP im Debugmodus ausgeführt wird.  
  
## Spezielle Fehlereigenschaften  

Ein Fehlerobjekt, das aus einem fehlerhaften Windows-Runtime-asynchronen Vorgang im Debugmodus resultiert, weist die folgenden speziellen Eigenschaften auf:  

*   `asyncOpSource` \ (Object \) Ruft Informationen über die ursprüngliche Position ab, an der der Aufruf, der einen Fehler erzeugt hat, erfolgte. Die Eigenschaft `asyncOpSource.originatingCall` \ (Zeichenfolge \) zeigt die Position im Code des Benutzers an, der den asynchronen Vorgang initiiert hat.  
*   asyncOpType \ (Zeichenfolge \) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.  
    
Weitere Informationen zu Fehlern mit asynchronen Vorgängen finden Sie unter:  
  
*   [Behandeln von Fehlern mit Zusagen][PreviousVersionsWindowsAppsHh700337]  
*   [Problembehandlung für Windows-Runtime-Fehler][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Versprechungen (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Behandeln von Problemen mit Windows-Runtime-Fehlern (HTML)"  
