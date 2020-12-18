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
# <span data-ttu-id="a13a7-103">Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="a13a7-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="a13a7-104">Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem Tiefpunkt in der Aufrufliste ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="a13a7-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="a13a7-105">Das JavaScript `Error` -Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die APP im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a13a7-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="a13a7-106">Spezielle Fehlereigenschaften</span><span class="sxs-lookup"><span data-stu-id="a13a7-106">Special error properties</span></span>  

<span data-ttu-id="a13a7-107">Ein Fehlerobjekt, das aus einem fehlerhaften Windows-Runtime-asynchronen Vorgang im Debugmodus resultiert, weist die folgenden speziellen Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="a13a7-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="a13a7-108">\ (Object \) Ruft Informationen über die ursprüngliche Position ab, an der der Aufruf, der einen Fehler erzeugt hat, erfolgte.</span><span class="sxs-lookup"><span data-stu-id="a13a7-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="a13a7-109">Die Eigenschaft `asyncOpSource.originatingCall` \ (Zeichenfolge \) zeigt die Position im Code des Benutzers an, der den asynchronen Vorgang initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="a13a7-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="a13a7-110">asyncOpType \ (Zeichenfolge \) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="a13a7-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="a13a7-111">Weitere Informationen zu Fehlern mit asynchronen Vorgängen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a13a7-111">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="a13a7-112">Behandeln von Fehlern mit Zusagen</span><span class="sxs-lookup"><span data-stu-id="a13a7-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="a13a7-113">Problembehandlung für Windows-Runtime-Fehler</span><span class="sxs-lookup"><span data-stu-id="a13a7-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Versprechungen (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Behandeln von Problemen mit Windows-Runtime-Fehlern (HTML) | Microsoft docs"  
