---
description: Ein Fehlercode, der von einer Chakra-Hosting-API zurückgegeben wird.
title: JsErrorCode-Enumeration | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b0a4aa7b47070bd5c8c7fe48cdbecf0dbefa9aa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233888"
---
# <span data-ttu-id="16e6e-103">JsErrorCode Enumeration</span><span class="sxs-lookup"><span data-stu-id="16e6e-103">JsErrorCode Enumeration</span></span>

<span data-ttu-id="16e6e-104">Ein Fehlercode, der von einer Chakra-Hosting-API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="16e6e-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="16e6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e6e-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="16e6e-106">Member</span><span class="sxs-lookup"><span data-stu-id="16e6e-106">Members</span></span>  
  
### <span data-ttu-id="16e6e-107">Werte</span><span class="sxs-lookup"><span data-stu-id="16e6e-107">Values</span></span>  
  
|<span data-ttu-id="16e6e-108">Name</span><span class="sxs-lookup"><span data-stu-id="16e6e-108">Name</span></span>|<span data-ttu-id="16e6e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16e6e-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="16e6e-110">Der Kontext kann nicht in einen Debug-Zustand versetzt werden, da er sich bereits in einem Debugstatus befindet.</span><span class="sxs-lookup"><span data-stu-id="16e6e-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="16e6e-111">Der Kontext kann die Profilerstellung nicht starten, da er bereits Profilerstellung ist.</span><span class="sxs-lookup"><span data-stu-id="16e6e-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="16e6e-112">Eine Hosting-API, die für Objektwerte verwendet wird, wurde mit einem nicht-Objekt-Wert aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="16e6e-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="16e6e-113">Es wurde ein fehlerhaftes serialisiertes Skript verwendet, oder das serialisierte Skript wurde von einer anderen Version des Chakra-Moduls serialisiert.</span><span class="sxs-lookup"><span data-stu-id="16e6e-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="16e6e-114">Runtime unterstützt keine zuverlässige Skript Unterbrechung.</span><span class="sxs-lookup"><span data-stu-id="16e6e-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="16e6e-115">Skripts können nicht in Debug-Kontexten serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="16e6e-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="16e6e-116">Fehlerkategorie, die sich auf Fehler im Modul selbst bezieht.</span><span class="sxs-lookup"><span data-stu-id="16e6e-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="16e6e-117">Kategorie der Fehler, die fatal sind und einen Fehler des Moduls signalisieren.</span><span class="sxs-lookup"><span data-stu-id="16e6e-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="16e6e-118">Fehlerkategorie, die sich auf Fehler in einem Skript bezieht.</span><span class="sxs-lookup"><span data-stu-id="16e6e-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="16e6e-119">Fehlerkategorie, die sich auf eine falsche Verwendung der API selbst bezieht.</span><span class="sxs-lookup"><span data-stu-id="16e6e-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="16e6e-120">Ein schwerwiegender Fehler im Modul ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="16e6e-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="16e6e-121">Im Skriptkontext läuft derzeit eine Heap-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="16e6e-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="16e6e-122">Leerlauf Benachrichtigung, wenn der Host die Leerlaufverarbeitung nicht aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="16e6e-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="16e6e-123">Die Laufzeit befindet sich in einem deaktivierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="16e6e-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="16e6e-124">Das Modul befindet sich in einem Ausnahmezustand, und es können keine APIs aufgerufen werden, bis die Ausnahme gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="16e6e-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="16e6e-125">Der Vorgang wird in einem Objekt vor dem Collect-Rückruf nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="16e6e-126">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="16e6e-127">Ein Skriptkontext befindet sich in der Mitte eines Profil Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="16e6e-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="16e6e-128">Ein Thread Dienst Rückruf ist derzeit im Gange.</span><span class="sxs-lookup"><span data-stu-id="16e6e-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="16e6e-129">Ein Argument für eine Hosting-API war ungültig.</span><span class="sxs-lookup"><span data-stu-id="16e6e-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="16e6e-130">Die Hosting-API setzt voraus, dass ein Kontext aktuell ist, aber es gibt keinen aktuellen Kontext.</span><span class="sxs-lookup"><span data-stu-id="16e6e-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="16e6e-131">Eine Hosting-API ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="16e6e-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="16e6e-132">Ein Argument für eine Hosting-API war NULL in einem Kontext, in dem NULL nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="16e6e-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="16e6e-133">Das Objekt kann nicht in den Zeiger umgebrochen werden `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="16e6e-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="16e6e-134">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="16e6e-135">Das Chakra-Modul hat keinen Arbeitsspeicher mehr.</span><span class="sxs-lookup"><span data-stu-id="16e6e-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="16e6e-136">Eine Hosting-API, die für Symbol Eigenschafts-IDs verwendet wird, aber mit einer nicht-Symbol-Eigenschafts-ID aufgerufen wurde. Der Fehlercode wird von zurückgegeben, `JsGetSymbolFromPropertyId` Wenn die Funktion mit einer nicht-Symbol-Eigenschafts-ID aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16e6e-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="16e6e-137">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="16e6e-138">Eine Hosting-API, die für Zeichenfolgeneigenschaften-IDs verwendet wird, aber mit einer Eigenschafts-ID ohne Zeichenfolge aufgerufen wurde. Der Fehlercode wird von vorhanden zurückgegeben, `JsGetPropertyNamefromId` Wenn die Funktion mit einer nicht-Zeichenfolgen-Eigenschafts-ID aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16e6e-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="16e6e-139">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="16e6e-140">Eine noch verwendete Laufzeit kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16e6e-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="16e6e-141">JavaScript konnte nicht kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="16e6e-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="16e6e-142">Ein Skript wurde beendet, weil es versucht hat, zu verwenden, `eval` oder `function` und eval wurde deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="16e6e-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="16e6e-143">Beim Ausführen eines Skripts ist eine JavaScript-Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="16e6e-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="16e6e-144">Ein Skript wurde aufgrund einer Anforderung zum Anhalten einer Laufzeit beendet.</span><span class="sxs-lookup"><span data-stu-id="16e6e-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="16e6e-145">Eine Hosting-API wurde mit einem Objekt aufgerufen, das unter einer anderen JavaScript-Laufzeit erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="16e6e-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="16e6e-146">Eine Hosting-API wurde im falschen Thread aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="16e6e-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="16e6e-147">Erfolgs Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="16e6e-147">Success error code.</span></span>|  
  
## <span data-ttu-id="16e6e-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16e6e-148">Requirements</span></span>  
 <span data-ttu-id="16e6e-149">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="16e6e-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="16e6e-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16e6e-150">See Also</span></span>  
 [<span data-ttu-id="16e6e-151">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="16e6e-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
