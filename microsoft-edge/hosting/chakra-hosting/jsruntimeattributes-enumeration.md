---
description: 'Attribute einer Laufzeit. '
title: JsRuntimeAttributes-Enumeration | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568325"
---
# <span data-ttu-id="2837d-103">JsRuntimeAttributes-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2837d-103">JsRuntimeAttributes Enumeration</span></span>
<span data-ttu-id="2837d-104">Attribute einer Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="2837d-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="2837d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2837d-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="2837d-106">Member</span><span class="sxs-lookup"><span data-stu-id="2837d-106">Members</span></span>  
  
### <span data-ttu-id="2837d-107">Werte</span><span class="sxs-lookup"><span data-stu-id="2837d-107">Values</span></span>  
  
|<span data-ttu-id="2837d-108">Name</span><span class="sxs-lookup"><span data-stu-id="2837d-108">Name</span></span>|<span data-ttu-id="2837d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2837d-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="2837d-110">Die Laufzeit sollte eine zuverlässige Skript Unterbrechung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2837d-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="2837d-111">Dies erhöht die Anzahl der stellen, an denen die Laufzeit auf eine Skript Unterbrechungsanforderung überprüft, und zwar zu Lasten einer geringen Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="2837d-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="2837d-112">Die Laufzeit führt keine Arbeit (wie Garbage Collection) für Hintergrund-Threads aus.</span><span class="sxs-lookup"><span data-stu-id="2837d-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="2837d-113">Mit `eval` oder `function` -Konstruktor wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2837d-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="2837d-114">Die Laufzeit generiert keinen systemeigenen Code.</span><span class="sxs-lookup"><span data-stu-id="2837d-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="2837d-115">Die Laufzeit ermöglicht alle experimentellen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2837d-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="2837d-116">Host ruft an `JsIdle` , also aktivieren Sie die Leerlaufverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="2837d-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="2837d-117">Andernfalls verwaltet die Laufzeit den Arbeitsspeicher etwas aggressiver.</span><span class="sxs-lookup"><span data-stu-id="2837d-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="2837d-118">Durch das Aufrufen `JsSetException` wird auch die Ausnahme an den Skriptdebugger gesendet (sofern vorhanden), der dem Debugger die Möglichkeit gibt, die Ausnahme zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="2837d-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="2837d-119">Keine besonderen Attribute.</span><span class="sxs-lookup"><span data-stu-id="2837d-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="2837d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2837d-120">Requirements</span></span>  
 <span data-ttu-id="2837d-121">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2837d-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2837d-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2837d-122">See Also</span></span>  
 [<span data-ttu-id="2837d-123">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2837d-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)