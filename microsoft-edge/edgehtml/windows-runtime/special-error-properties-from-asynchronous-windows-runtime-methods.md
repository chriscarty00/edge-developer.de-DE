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
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a><span data-ttu-id="62433-103">Eigenschaften spezieller Fehler von asynchronen Methoden von Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="62433-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="62433-104">Es kann schwierig sein, asynchrone Windows-Runtime-Methoden in JavaScript zu debuggen, da der Fehler möglicherweise von einem orts tief in der Aufrufliste ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="62433-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="62433-105">Das JavaScript-Objekt verfügt über zusätzliche Eigenschaften, die nur angezeigt werden, wenn der Fehler von einer asynchronen Windows-Runtime-Methode ausgelöst wird, wenn die App `Error` im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62433-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <a name="special-error-properties"></a><span data-ttu-id="62433-106">Spezielle Fehlereigenschaften</span><span class="sxs-lookup"><span data-stu-id="62433-106">Special error properties</span></span>  

<span data-ttu-id="62433-107">Ein Fehlerobjekt, das aus einem fehlgeschlagenen asynchronen Windows-Runtime-Vorgang im Debugmodus resultiert, hat die folgenden speziellen Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62433-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="62433-108">\(Object\) Ruft Informationen zum ursprünglichen Speicherort ab, an dem der Aufruf erfolgt ist, der einen Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="62433-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="62433-109">Die Eigenschaft \(String\) zeigt den Speicherort im Code des Benutzers an, der `asyncOpSource.originatingCall` den asynchronen Vorgang ursprünglich war.</span><span class="sxs-lookup"><span data-stu-id="62433-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="62433-110">asyncOpType \(String\) Ruft den Namen des asynchronen Vorgangstyps ab, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="62433-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="62433-111">Weitere Informationen zu Fehlern bei asynchronen Vorgängen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="62433-111">For more information about errors with asynchronous operations, see:</span></span>  

*   [<span data-ttu-id="62433-112">Behandeln von Fehlern mit Zusagen</span><span class="sxs-lookup"><span data-stu-id="62433-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="62433-113">Problembehandlung für Windows-Runtime-Fehler</span><span class="sxs-lookup"><span data-stu-id="62433-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Behandeln von Fehlern mit Zusagen (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Problembehandlung bei Windows-Runtime-Fehlern (HTML) | Microsoft Docs"  
