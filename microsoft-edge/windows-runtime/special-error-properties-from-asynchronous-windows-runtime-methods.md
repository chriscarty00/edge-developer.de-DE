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
# <span data-ttu-id="080f3-102">Spezielle Fehlereigenschaften von asynchronen Windows-Runtime-Methoden</span><span class="sxs-lookup"><span data-stu-id="080f3-102">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="080f3-103">Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem Tiefpunkt in der Aufrufliste ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="080f3-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="080f3-104">Das JavaScript `Error` -Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die APP im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="080f3-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="080f3-105">Spezielle Fehlereigenschaften</span><span class="sxs-lookup"><span data-stu-id="080f3-105">Special error properties</span></span>  

<span data-ttu-id="080f3-106">Ein Fehlerobjekt, das aus einem fehlerhaften Windows-Runtime-asynchronen Vorgang im Debugmodus resultiert, weist die folgenden speziellen Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="080f3-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="080f3-107">\ (Object \) Ruft Informationen über die ursprüngliche Position ab, an der der Aufruf, der einen Fehler erzeugt hat, erfolgte.</span><span class="sxs-lookup"><span data-stu-id="080f3-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="080f3-108">Die Eigenschaft `asyncOpSource.originatingCall` \ (Zeichenfolge \) zeigt die Position im Code des Benutzers an, der den asynchronen Vorgang initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="080f3-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="080f3-109">asyncOpType \ (Zeichenfolge \) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="080f3-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="080f3-110">Weitere Informationen zu Fehlern mit asynchronen Vorgängen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="080f3-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="080f3-111">Behandeln von Fehlern mit Zusagen</span><span class="sxs-lookup"><span data-stu-id="080f3-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="080f3-112">Problembehandlung für Windows-Runtime-Fehler</span><span class="sxs-lookup"><span data-stu-id="080f3-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Versprechungen (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Behandeln von Problemen mit Windows-Runtime-Fehlern (HTML) | Microsoft docs"  
