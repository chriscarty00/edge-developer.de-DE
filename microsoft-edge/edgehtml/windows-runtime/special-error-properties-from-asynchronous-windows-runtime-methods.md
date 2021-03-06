---
description: Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime
title: Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398840"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a>Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem orts tief in der Aufrufliste ausgelöst wird.  Das JavaScript-Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die App `Error` im Debugmodus ausgeführt wird.  
  
## <a name="special-error-properties"></a>Spezielle Fehlereigenschaften  

Ein Fehlerobjekt, das aus einem fehlgeschlagenen asynchronen Windows-Runtime-Vorgang im Debugmodus resultiert, hat die folgenden speziellen Eigenschaften:  

*   `asyncOpSource` \(Object\) Ruft Informationen zum ursprünglichen Speicherort ab, an dem der Aufruf erfolgt ist, der einen Fehler verursacht hat.  Die Eigenschaft \(String\) zeigt den Speicherort im Code des Benutzers an, der `asyncOpSource.originatingCall` den asynchronen Vorgang ursprünglich war.  
*   asyncOpType \(String\) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.  
    
Weitere Informationen zu Fehlern bei asynchronen Vorgängen finden Sie unter:  

*   [Behandeln von Fehlern mit Zusagen][PreviousVersionsWindowsAppsHh700337]  
*   [Problembehandlung für Windows-Runtime-Fehler][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Zusagen (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Problembehandlung bei Windows-Runtime-Fehlern (HTML) | Microsoft Docs"  
