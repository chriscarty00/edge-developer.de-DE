---
description: JavaScript Runtime (JsRT)-APIs ermöglichen das Hinzufügen von Skriptfunktionen zu Desktop-und serverseitigen Anwendungen, die unter Windows ausgeführt werden.
title: Referenz (JavaScript-Laufzeit)
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 7166e6cd5d64060c2939d8404e1415dc34fce17b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752213"
---
# <span data-ttu-id="00a65-103">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="00a65-103">Reference (JavaScript runtime)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="00a65-104">JavaScript Runtime (JsRT)-APIs ermöglichen das Hinzufügen von Skriptfunktionen zu Desktop-und serverseitigen Anwendungen, die unter Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="00a65-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

<span data-ttu-id="00a65-105">Wenn Sie beabsichtigen, [ChakraCore](https://github.com/Microsoft/ChakraCore) in Ihre Anwendung einzubetten, lesen Sie stattdessen [ChakraCore-wiki](https://aka.ms/corejsrtref) für JSRT-Verweise.</span><span class="sxs-lookup"><span data-stu-id="00a65-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  

## <span data-ttu-id="00a65-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="00a65-106">In this section</span></span>  

<span data-ttu-id="00a65-107">Typedefs, Konstanten und Enumerationen, die JsRT-Hosting unterstützen, werden hier beschrieben:</span><span class="sxs-lookup"><span data-stu-id="00a65-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
*   [<span data-ttu-id="00a65-108">JavaScript-Laufzeit-Typedefs, Konstanten und Enumerationen</span><span class="sxs-lookup"><span data-stu-id="00a65-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](./javascript-runtime-typedefs-constants-and-enumerations.md)  

<span data-ttu-id="00a65-109">Die folgenden Funktionen ermöglichen JsRT-Hosting:</span><span class="sxs-lookup"><span data-stu-id="00a65-109">The following functions enable JsRT hosting:</span></span>  

*   [<span data-ttu-id="00a65-110">JsAddRef Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-110">JsAddRef Function</span></span>](./jsaddref-function.md)  
*   [<span data-ttu-id="00a65-111">JsBooleanToBool Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-111">JsBooleanToBool Function</span></span>](./jsbooleantobool-function.md)  
*   [<span data-ttu-id="00a65-112">JsBoolToBoolean Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-112">JsBoolToBoolean Function</span></span>](./jsbooltoboolean-function.md)  
*   [<span data-ttu-id="00a65-113">JsCallFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-113">JsCallFunction Function</span></span>](./jscallfunction-function.md)  
*   [<span data-ttu-id="00a65-114">JsCollectGarbage Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-114">JsCollectGarbage Function</span></span>](./jscollectgarbage-function.md)  
*   [<span data-ttu-id="00a65-115">JsConstructObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-115">JsConstructObject Function</span></span>](./jsconstructobject-function.md)  
*   [<span data-ttu-id="00a65-116">JsConvertValueToBoolean Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-116">JsConvertValueToBoolean Function</span></span>](./jsconvertvaluetoboolean-function.md)  
*   [<span data-ttu-id="00a65-117">JsConvertValueToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-117">JsConvertValueToNumber Function</span></span>](./jsconvertvaluetonumber-function.md)  
*   [<span data-ttu-id="00a65-118">JsConvertValueToObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-118">JsConvertValueToObject Function</span></span>](./jsconvertvaluetoobject-function.md)  
*   [<span data-ttu-id="00a65-119">JsConvertValueToString Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-119">JsConvertValueToString Function</span></span>](./jsconvertvaluetostring-function.md)  
*   [<span data-ttu-id="00a65-120">JsCreateArray Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-120">JsCreateArray Function</span></span>](./jscreatearray-function.md)  
*   [<span data-ttu-id="00a65-121">JsCreateArrayBuffer Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-121">JsCreateArrayBuffer Function</span></span>](./jscreatearraybuffer-function.md)  
*   [<span data-ttu-id="00a65-122">JsCreateContext Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-122">JsCreateContext Function</span></span>](./jscreatecontext-function.md)  
*   [<span data-ttu-id="00a65-123">JsCreateDataView Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-123">JsCreateDataView Function</span></span>](./jscreatedataview-function.md)  
*   [<span data-ttu-id="00a65-124">JsCreateError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-124">JsCreateError Function</span></span>](./jscreateerror-function.md)  
*   [<span data-ttu-id="00a65-125">JsCreateExternalArrayBuffer Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-125">JsCreateExternalArrayBuffer Function</span></span>](./jscreateexternalarraybuffer-function.md)  
*   [<span data-ttu-id="00a65-126">JsCreateExternalObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-126">JsCreateExternalObject Function</span></span>](./jscreateexternalobject-function.md)  
*   [<span data-ttu-id="00a65-127">JsCreateFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-127">JsCreateFunction Function</span></span>](./jscreatefunction-function.md)  
*   [<span data-ttu-id="00a65-128">JsCreateNamedFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-128">JsCreateNamedFunction Function</span></span>](./jscreatenamedfunction-function.md)  
*   [<span data-ttu-id="00a65-129">JsCreateObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-129">JsCreateObject Function</span></span>](./jscreateobject-function.md)  
*   [<span data-ttu-id="00a65-130">JsCreateRangeError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-130">JsCreateRangeError Function</span></span>](./jscreaterangeerror-function.md)  
*   [<span data-ttu-id="00a65-131">JsCreateReferenceError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-131">JsCreateReferenceError Function</span></span>](./jscreatereferenceerror-function.md)  
*   [<span data-ttu-id="00a65-132">JsCreateRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-132">JsCreateRuntime Function</span></span>](./jscreateruntime-function.md)  
*   [<span data-ttu-id="00a65-133">JsCreateSymbol Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-133">JsCreateSymbol Function</span></span>](./jscreatesymbol-function.md)  
*   [<span data-ttu-id="00a65-134">JsCreateSyntaxError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-134">JsCreateSyntaxError Function</span></span>](./jscreatesyntaxerror-function.md)  
*   [<span data-ttu-id="00a65-135">JsCreateTypeError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-135">JsCreateTypeError Function</span></span>](./jscreatetypeerror-function.md)  
*   [<span data-ttu-id="00a65-136">JsCreateTypedArray Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-136">JsCreateTypedArray Function</span></span>](./jscreatetypedarray-function.md)  
*   [<span data-ttu-id="00a65-137">JsCreateURIError Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-137">JsCreateURIError Function</span></span>](./jscreateurierror-function.md)  
*   [<span data-ttu-id="00a65-138">JsDefineProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-138">JsDefineProperty Function</span></span>](./jsdefineproperty-function.md)  
*   [<span data-ttu-id="00a65-139">JsDeleteIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-139">JsDeleteIndexedProperty Function</span></span>](./jsdeleteindexedproperty-function.md)  
*   [<span data-ttu-id="00a65-140">JsDeleteProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-140">JsDeleteProperty Function</span></span>](./jsdeleteproperty-function.md)  
*   [<span data-ttu-id="00a65-141">JsDisableRuntimeExecution Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-141">JsDisableRuntimeExecution Function</span></span>](./jsdisableruntimeexecution-function.md)  
*   [<span data-ttu-id="00a65-142">JsDisposeRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-142">JsDisposeRuntime Function</span></span>](./jsdisposeruntime-function.md)  
*   [<span data-ttu-id="00a65-143">JsDoubleToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-143">JsDoubleToNumber Function</span></span>](./jsdoubletonumber-function.md)  
*   [<span data-ttu-id="00a65-144">JsEnableRuntimeExecution Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-144">JsEnableRuntimeExecution Function</span></span>](./jsenableruntimeexecution-function.md)  
*   [<span data-ttu-id="00a65-145">JsEnumerateHeap Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-145">JsEnumerateHeap Function</span></span>](./jsenumerateheap-function.md)  
*   [<span data-ttu-id="00a65-146">JsEquals Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-146">JsEquals Function</span></span>](./jsequals-function.md)  
*   [<span data-ttu-id="00a65-147">JsGetAndClearException Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-147">JsGetAndClearException Function</span></span>](./jsgetandclearexception-function.md)  
*   [<span data-ttu-id="00a65-148">JsGetArrayBufferStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-148">JsGetArrayBufferStorage Function</span></span>](./jsgetarraybufferstorage-function.md)  
*   [<span data-ttu-id="00a65-149">JsGetContextData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-149">JsGetContextData Function</span></span>](./jsgetcontextdata-function.md)  
*   [<span data-ttu-id="00a65-150">JsGetContextOfObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-150">JsGetContextOfObject Function</span></span>](./jsgetcontextofobject-function.md)  
*   [<span data-ttu-id="00a65-151">JsGetCurrentContext Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-151">JsGetCurrentContext Function</span></span>](./jsgetcurrentcontext-function.md)  
*   [<span data-ttu-id="00a65-152">JsGetDataViewStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-152">JsGetDataViewStorage Function</span></span>](./jsgetdataviewstorage-function.md)  
*   [<span data-ttu-id="00a65-153">JsGetExtensionAllowed Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-153">JsGetExtensionAllowed Function</span></span>](./jsgetextensionallowed-function.md)  
*   [<span data-ttu-id="00a65-154">JsGetExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-154">JsGetExternalData Function</span></span>](./jsgetexternaldata-function.md)  
*   [<span data-ttu-id="00a65-155">JsGetFalseValue Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-155">JsGetFalseValue Function</span></span>](./jsgetfalsevalue-function.md)  
*   [<span data-ttu-id="00a65-156">JsGetGlobalObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-156">JsGetGlobalObject Function</span></span>](./jsgetglobalobject-function.md)  
*   [<span data-ttu-id="00a65-157">JsGetIndexedPropertiesExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-157">JsGetIndexedPropertiesExternalData Function</span></span>](./jsgetindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="00a65-158">JsGetIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-158">JsGetIndexedProperty Function</span></span>](./jsgetindexedproperty-function.md)  
*   [<span data-ttu-id="00a65-159">JsGetNullValue Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-159">JsGetNullValue Function</span></span>](./jsgetnullvalue-function.md)  
*   [<span data-ttu-id="00a65-160">JsGetOwnPropertyDescriptor Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-160">JsGetOwnPropertyDescriptor Function</span></span>](./jsgetownpropertydescriptor-function.md)  
*   [<span data-ttu-id="00a65-161">JsGetOwnPropertyNames Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-161">JsGetOwnPropertyNames Function</span></span>](./jsgetownpropertynames-function.md)  
*   [<span data-ttu-id="00a65-162">JsGetOwnPropertySymbols Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-162">JsGetOwnPropertySymbols Function</span></span>](./jsgetownpropertysymbols-function.md)  
*   [<span data-ttu-id="00a65-163">JsGetProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-163">JsGetProperty Function</span></span>](./jsgetproperty-function.md)  
*   [<span data-ttu-id="00a65-164">JsGetPropertyIdFromName Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-164">JsGetPropertyIdFromName Function</span></span>](./jsgetpropertyidfromname-function.md)  
*   [<span data-ttu-id="00a65-165">JsGetPropertyIdFromSymbol Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-165">JsGetPropertyIdFromSymbol Function</span></span>](./jsgetpropertyidfromsymbol-function.md)  
*   [<span data-ttu-id="00a65-166">JsGetPropertyIdType Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-166">JsGetPropertyIdType Function</span></span>](./jsgetpropertyidtype-function.md)  
*   [<span data-ttu-id="00a65-167">JsGetPropertyNameFromId Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-167">JsGetPropertyNameFromId Function</span></span>](./jsgetpropertynamefromid-function.md)  
*   [<span data-ttu-id="00a65-168">JsGetPrototype Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-168">JsGetPrototype Function</span></span>](./jsgetprototype-function.md)  
*   [<span data-ttu-id="00a65-169">JsGetRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-169">JsGetRuntime Function</span></span>](./jsgetruntime-function.md)  
*   [<span data-ttu-id="00a65-170">JsGetRuntimeMemoryLimit Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-170">JsGetRuntimeMemoryLimit Function</span></span>](./jsgetruntimememorylimit-function.md)  
*   [<span data-ttu-id="00a65-171">JsGetRuntimeMemoryUsage Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-171">JsGetRuntimeMemoryUsage Function</span></span>](./jsgetruntimememoryusage-function.md)  
*   [<span data-ttu-id="00a65-172">JsGetStringLength Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-172">JsGetStringLength Function</span></span>](./jsgetstringlength-function.md)  
*   [<span data-ttu-id="00a65-173">JsGetSymbolFromPropertyId Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-173">JsGetSymbolFromPropertyId Function</span></span>](./jsgetsymbolfrompropertyid-function.md)  
*   [<span data-ttu-id="00a65-174">JsGetTrueValue Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-174">JsGetTrueValue Function</span></span>](./jsgettruevalue-function.md)  
*   [<span data-ttu-id="00a65-175">JsGetTypedArrayInfo Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-175">JsGetTypedArrayInfo Function</span></span>](./jsgettypedarrayinfo-function.md)  
*   [<span data-ttu-id="00a65-176">JsGetTypedArrayStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-176">JsGetTypedArrayStorage Function</span></span>](./jsgettypedarraystorage-function.md)  
*   [<span data-ttu-id="00a65-177">JsGetUndefinedValue Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-177">JsGetUndefinedValue Function</span></span>](./jsgetundefinedvalue-function.md)  
*   [<span data-ttu-id="00a65-178">JsGetValueType Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-178">JsGetValueType Function</span></span>](./jsgetvaluetype-function.md)  
*   [<span data-ttu-id="00a65-179">JsHasException Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-179">JsHasException Function</span></span>](./jshasexception-function.md)  
*   [<span data-ttu-id="00a65-180">JsHasExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-180">JsHasExternalData Function</span></span>](./jshasexternaldata-function.md)  
*   [<span data-ttu-id="00a65-181">JsHasIndexedPropertiesExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-181">JsHasIndexedPropertiesExternalData Function</span></span>](./jshasindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="00a65-182">JsHasIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-182">JsHasIndexedProperty Function</span></span>](./jshasindexedproperty-function.md)  
*   [<span data-ttu-id="00a65-183">JsHasProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-183">JsHasProperty Function</span></span>](./jshasproperty-function.md)  
*   [<span data-ttu-id="00a65-184">JsIdle Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-184">JsIdle Function</span></span>](./jsidle-function.md)  
*   [<span data-ttu-id="00a65-185">JsInspectableToObject Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-185">JsInspectableToObject Function</span></span>](./jsinspectabletoobject-function.md)  
*   [<span data-ttu-id="00a65-186">JsInstanceOf Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-186">JsInstanceOf Function</span></span>](./jsinstanceof-function.md)  
*   [<span data-ttu-id="00a65-187">JsIntToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-187">JsIntToNumber Function</span></span>](./jsinttonumber-function.md)  
*   [<span data-ttu-id="00a65-188">JsIsEnumeratingHeap Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-188">JsIsEnumeratingHeap Function</span></span>](./jsisenumeratingheap-function.md)  
*   [<span data-ttu-id="00a65-189">JsIsRuntimeExecutionDisabled Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-189">JsIsRuntimeExecutionDisabled Function</span></span>](./jsisruntimeexecutiondisabled-function.md)  
*   [<span data-ttu-id="00a65-190">JsNumberToDouble Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-190">JsNumberToDouble Function</span></span>](./jsnumbertodouble-function.md)  
*   [<span data-ttu-id="00a65-191">JsNumberToInt Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-191">JsNumberToInt Function</span></span>](./jsnumbertoint-function.md)  
*   [<span data-ttu-id="00a65-192">JsObjectToInspectable Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-192">JsObjectToInspectable Function</span></span>](./jsobjecttoinspectable-function.md)  
*   [<span data-ttu-id="00a65-193">JsParseScript Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-193">JsParseScript Function</span></span>](./jsparsescript-function.md)  
*   [<span data-ttu-id="00a65-194">JsParseSerializedScript Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-194">JsParseSerializedScript Function</span></span>](./jsparseserializedscript-function.md)  
*   [<span data-ttu-id="00a65-195">JsParseSerializedScriptWithCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-195">JsParseSerializedScriptWithCallback Function</span></span>](./jsparseserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="00a65-196">JsPointerToString Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-196">JsPointerToString Function</span></span>](./jspointertostring-function.md)  
*   [<span data-ttu-id="00a65-197">JsPreventExtension Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-197">JsPreventExtension Function</span></span>](./jspreventextension-function.md)  
*   [<span data-ttu-id="00a65-198">JsProjectWinRTNamespace Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-198">JsProjectWinRTNamespace Function</span></span>](./jsprojectwinrtnamespace-function.md)  
*   [<span data-ttu-id="00a65-199">JsRelease Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-199">JsRelease Function</span></span>](./jsrelease-function.md)  
*   [<span data-ttu-id="00a65-200">JsRunScript Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-200">JsRunScript Function</span></span>](./jsrunscript-function.md)  
*   [<span data-ttu-id="00a65-201">JsRunSerializedScript Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-201">JsRunSerializedScript Function</span></span>](./jsrunserializedscript-function.md)  
*   [<span data-ttu-id="00a65-202">JsRunSerializedScriptWithCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-202">JsRunSerializedScriptWithCallback Function</span></span>](./jsrunserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="00a65-203">JsSerializeScript Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-203">JsSerializeScript Function</span></span>](./jsserializescript-function.md)  
*   [<span data-ttu-id="00a65-204">JsSetContextData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-204">JsSetContextData Function</span></span>](./jssetcontextdata-function.md)  
*   [<span data-ttu-id="00a65-205">JsSetCurrentContext Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-205">JsSetCurrentContext Function</span></span>](./jssetcurrentcontext-function.md)  
*   [<span data-ttu-id="00a65-206">JsSetException Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-206">JsSetException Function</span></span>](./jssetexception-function.md)  
*   [<span data-ttu-id="00a65-207">JsSetExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-207">JsSetExternalData Function</span></span>](./jssetexternaldata-function.md)  
*   [<span data-ttu-id="00a65-208">JsSetIndexedPropertiesToExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-208">JsSetIndexedPropertiesToExternalData Function</span></span>](./jssetindexedpropertiestoexternaldata-function.md)  
*   [<span data-ttu-id="00a65-209">JsSetIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-209">JsSetIndexedProperty Function</span></span>](./jssetindexedproperty-function.md)  
*   [<span data-ttu-id="00a65-210">JsSetObjectBeforeCollectCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-210">JsSetObjectBeforeCollectCallback Function</span></span>](./jssetobjectbeforecollectcallback-function.md)  
*   [<span data-ttu-id="00a65-211">JsSetProjectionEnqueueCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-211">JsSetProjectionEnqueueCallback Function</span></span>](./jssetprojectionenqueuecallback-function.md)  
*   [<span data-ttu-id="00a65-212">JsSetPromiseContinuationCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-212">JsSetPromiseContinuationCallback Function</span></span>](./jssetpromisecontinuationcallback-function.md)  
*   [<span data-ttu-id="00a65-213">JsSetProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-213">JsSetProperty Function</span></span>](./jssetproperty-function.md)  
*   [<span data-ttu-id="00a65-214">JsSetPrototype Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-214">JsSetPrototype Function</span></span>](./jssetprototype-function.md)  
*   [<span data-ttu-id="00a65-215">JsSetRuntimeBeforeCollectCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](./jssetruntimebeforecollectcallback-function.md)  
*   [<span data-ttu-id="00a65-216">JsSetRuntimeMemoryAllocationCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](./jssetruntimememoryallocationcallback-function.md)  
*   [<span data-ttu-id="00a65-217">JsSetRuntimeMemoryLimit Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-217">JsSetRuntimeMemoryLimit Function</span></span>](./jssetruntimememorylimit-function.md)  
*   [<span data-ttu-id="00a65-218">JsStartDebugging Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-218">JsStartDebugging Function</span></span>](./jsstartdebugging-function.md)  
*   [<span data-ttu-id="00a65-219">JsStartProfiling Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-219">JsStartProfiling Function</span></span>](./jsstartprofiling-function.md)  
*   [<span data-ttu-id="00a65-220">JsStopProfiling Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-220">JsStopProfiling Function</span></span>](./jsstopprofiling-function.md)  
*   [<span data-ttu-id="00a65-221">JsStrictEquals Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-221">JsStrictEquals Function</span></span>](./jsstrictequals-function.md)  
*   [<span data-ttu-id="00a65-222">JsStringToPointer Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-222">JsStringToPointer Function</span></span>](./jsstringtopointer-function.md)  
*   [<span data-ttu-id="00a65-223">JsValueToVariant Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-223">JsValueToVariant Function</span></span>](./jsvaluetovariant-function.md)  
*   [<span data-ttu-id="00a65-224">JsVariantToValue Funktion</span><span class="sxs-lookup"><span data-stu-id="00a65-224">JsVariantToValue Function</span></span>](./jsvarianttovalue-function.md)  

## <span data-ttu-id="00a65-225">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00a65-225">See also</span></span>  

*   [<span data-ttu-id="00a65-226">Hosten der JavaScript-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="00a65-226">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="00a65-227">JavaScript-Laufzeit-Hosten</span><span class="sxs-lookup"><span data-stu-id="00a65-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  
