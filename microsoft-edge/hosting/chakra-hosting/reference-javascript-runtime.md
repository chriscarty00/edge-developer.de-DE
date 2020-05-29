---
description: JavaScript Runtime (JsRT)-APIs ermöglichen das Hinzufügen von Skriptfunktionen zu Desktop-und serverseitigen Anwendungen, die unter Windows ausgeführt werden.
title: Referenz (JavaScript-Laufzeit) | Microsoft docs
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d1215d84daa31f2338b8c7e237625d0129026bea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567189"
---
# <span data-ttu-id="fd753-103">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="fd753-103">Reference (JavaScript Runtime)</span></span>
<span data-ttu-id="fd753-104">JavaScript Runtime (JsRT)-APIs ermöglichen das Hinzufügen von Skriptfunktionen zu Desktop-und serverseitigen Anwendungen, die unter Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd753-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  
  
 <span data-ttu-id="fd753-105">Wenn Sie beabsichtigen, [ChakraCore](https://github.com/Microsoft/ChakraCore) in Ihre Anwendung einzubetten, lesen Sie stattdessen [ChakraCore-wiki](https://aka.ms/corejsrtref) für JSRT-Verweise.</span><span class="sxs-lookup"><span data-stu-id="fd753-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  
  
## <span data-ttu-id="fd753-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="fd753-106">In This Section</span></span>  
 <span data-ttu-id="fd753-107">Typedefs, Konstanten und Enumerationen, die JsRT-Hosting unterstützen, werden hier beschrieben:</span><span class="sxs-lookup"><span data-stu-id="fd753-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
-   [<span data-ttu-id="fd753-108">JavaScript-Runtime-Typedefs,-Konstanten und-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="fd753-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](../chakra-hosting/javascript-runtime-typedefs-constants-and-enumerations.md)  
  
 <span data-ttu-id="fd753-109">Die folgenden Funktionen ermöglichen JsRT-Hosting:</span><span class="sxs-lookup"><span data-stu-id="fd753-109">The following functions enable JsRT hosting:</span></span>  
  
-   [<span data-ttu-id="fd753-110">JsAddRef-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-110">JsAddRef Function</span></span>](../chakra-hosting/jsaddref-function.md)  
  
-   [<span data-ttu-id="fd753-111">JsBooleanToBool-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-111">JsBooleanToBool Function</span></span>](../chakra-hosting/jsbooleantobool-function.md)  
  
-   [<span data-ttu-id="fd753-112">JsBoolToBoolean-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-112">JsBoolToBoolean Function</span></span>](../chakra-hosting/jsbooltoboolean-function.md)  
  
-   [<span data-ttu-id="fd753-113">JsCallFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-113">JsCallFunction Function</span></span>](../chakra-hosting/jscallfunction-function.md)  
  
-   [<span data-ttu-id="fd753-114">JsCollectGarbage-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-114">JsCollectGarbage Function</span></span>](../chakra-hosting/jscollectgarbage-function.md)  
  
-   [<span data-ttu-id="fd753-115">JsConstructObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-115">JsConstructObject Function</span></span>](../chakra-hosting/jsconstructobject-function.md)  
  
-   [<span data-ttu-id="fd753-116">JsConvertValueToBoolean-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-116">JsConvertValueToBoolean Function</span></span>](../chakra-hosting/jsconvertvaluetoboolean-function.md)  
  
-   [<span data-ttu-id="fd753-117">JsConvertValueToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-117">JsConvertValueToNumber Function</span></span>](../chakra-hosting/jsconvertvaluetonumber-function.md)  
  
-   [<span data-ttu-id="fd753-118">JsConvertValueToObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-118">JsConvertValueToObject Function</span></span>](../chakra-hosting/jsconvertvaluetoobject-function.md)  
  
-   [<span data-ttu-id="fd753-119">JsConvertValueToString-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-119">JsConvertValueToString Function</span></span>](../chakra-hosting/jsconvertvaluetostring-function.md)  
  
-   [<span data-ttu-id="fd753-120">JsCreateArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-120">JsCreateArray Function</span></span>](../chakra-hosting/jscreatearray-function.md)  
  
-   [<span data-ttu-id="fd753-121">JsCreateArrayBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-121">JsCreateArrayBuffer Function</span></span>](../chakra-hosting/jscreatearraybuffer-function.md)  
  
-   [<span data-ttu-id="fd753-122">JsCreateContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-122">JsCreateContext Function</span></span>](../chakra-hosting/jscreatecontext-function.md)  
  
-   [<span data-ttu-id="fd753-123">JsCreateDataView-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-123">JsCreateDataView Function</span></span>](../chakra-hosting/jscreatedataview-function.md)  
  
-   [<span data-ttu-id="fd753-124">JsCreateError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-124">JsCreateError Function</span></span>](../chakra-hosting/jscreateerror-function.md)  
  
-   [<span data-ttu-id="fd753-125">JsCreateExternalArrayBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-125">JsCreateExternalArrayBuffer Function</span></span>](../chakra-hosting/jscreateexternalarraybuffer-function.md)  
  
-   [<span data-ttu-id="fd753-126">JsCreateExternalObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-126">JsCreateExternalObject Function</span></span>](../chakra-hosting/jscreateexternalobject-function.md)  
  
-   [<span data-ttu-id="fd753-127">JsCreateFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-127">JsCreateFunction Function</span></span>](../chakra-hosting/jscreatefunction-function.md)  
  
-   [<span data-ttu-id="fd753-128">JsCreateNamedFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-128">JsCreateNamedFunction Function</span></span>](../chakra-hosting/jscreatenamedfunction-function.md)  
  
-   [<span data-ttu-id="fd753-129">JsCreateObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-129">JsCreateObject Function</span></span>](../chakra-hosting/jscreateobject-function.md)  
  
-   [<span data-ttu-id="fd753-130">JsCreateRangeError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-130">JsCreateRangeError Function</span></span>](../chakra-hosting/jscreaterangeerror-function.md)  
  
-   [<span data-ttu-id="fd753-131">JsCreateReferenceError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-131">JsCreateReferenceError Function</span></span>](../chakra-hosting/jscreatereferenceerror-function.md)  
  
-   [<span data-ttu-id="fd753-132">JsCreateRuntime-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-132">JsCreateRuntime Function</span></span>](../chakra-hosting/jscreateruntime-function.md)  
  
-   [<span data-ttu-id="fd753-133">JsCreateSymbol-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-133">JsCreateSymbol Function</span></span>](../chakra-hosting/jscreatesymbol-function.md)  
  
-   [<span data-ttu-id="fd753-134">JsCreateSyntaxError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-134">JsCreateSyntaxError Function</span></span>](../chakra-hosting/jscreatesyntaxerror-function.md)  
  
-   [<span data-ttu-id="fd753-135">JsCreateTypeError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-135">JsCreateTypeError Function</span></span>](../chakra-hosting/jscreatetypeerror-function.md)  
  
-   [<span data-ttu-id="fd753-136">JsCreateTypedArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-136">JsCreateTypedArray Function</span></span>](../chakra-hosting/jscreatetypedarray-function.md)  
  
-   [<span data-ttu-id="fd753-137">JsCreateURIError-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-137">JsCreateURIError Function</span></span>](../chakra-hosting/jscreateurierror-function.md)  
  
-   [<span data-ttu-id="fd753-138">JsDefineProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-138">JsDefineProperty Function</span></span>](../chakra-hosting/jsdefineproperty-function.md)  
  
-   [<span data-ttu-id="fd753-139">JsDeleteIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-139">JsDeleteIndexedProperty Function</span></span>](../chakra-hosting/jsdeleteindexedproperty-function.md)  
  
-   [<span data-ttu-id="fd753-140">JsDeleteProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-140">JsDeleteProperty Function</span></span>](../chakra-hosting/jsdeleteproperty-function.md)  
  
-   [<span data-ttu-id="fd753-141">JsDisableRuntimeExecution-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-141">JsDisableRuntimeExecution Function</span></span>](../chakra-hosting/jsdisableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="fd753-142">JsDisposeRuntime-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-142">JsDisposeRuntime Function</span></span>](../chakra-hosting/jsdisposeruntime-function.md)  
  
-   [<span data-ttu-id="fd753-143">JsDoubleToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-143">JsDoubleToNumber Function</span></span>](../chakra-hosting/jsdoubletonumber-function.md)  
  
-   [<span data-ttu-id="fd753-144">JsEnableRuntimeExecution-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-144">JsEnableRuntimeExecution Function</span></span>](../chakra-hosting/jsenableruntimeexecution-function.md)  
  
-   [<span data-ttu-id="fd753-145">JsEnumerateHeap-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-145">JsEnumerateHeap Function</span></span>](../chakra-hosting/jsenumerateheap-function.md)  
  
-   [<span data-ttu-id="fd753-146">JsEquals-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-146">JsEquals Function</span></span>](../chakra-hosting/jsequals-function.md)  
  
-   [<span data-ttu-id="fd753-147">JsGetAndClearException-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-147">JsGetAndClearException Function</span></span>](../chakra-hosting/jsgetandclearexception-function.md)  
  
-   [<span data-ttu-id="fd753-148">JsGetArrayBufferStorage-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-148">JsGetArrayBufferStorage Function</span></span>](../chakra-hosting/jsgetarraybufferstorage-function.md)  
  
-   [<span data-ttu-id="fd753-149">JsGetContextData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-149">JsGetContextData Function</span></span>](../chakra-hosting/jsgetcontextdata-function.md)  
  
-   [<span data-ttu-id="fd753-150">JsGetContextOfObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-150">JsGetContextOfObject Function</span></span>](../chakra-hosting/jsgetcontextofobject-function.md)  
  
-   [<span data-ttu-id="fd753-151">JsGetCurrentContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-151">JsGetCurrentContext Function</span></span>](../chakra-hosting/jsgetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="fd753-152">JsGetDataViewStorage-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-152">JsGetDataViewStorage Function</span></span>](../chakra-hosting/jsgetdataviewstorage-function.md)  
  
-   [<span data-ttu-id="fd753-153">JsGetExtensionAllowed-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-153">JsGetExtensionAllowed Function</span></span>](../chakra-hosting/jsgetextensionallowed-function.md)  
  
-   [<span data-ttu-id="fd753-154">JsGetExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-154">JsGetExternalData Function</span></span>](../chakra-hosting/jsgetexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-155">JsGetFalseValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-155">JsGetFalseValue Function</span></span>](../chakra-hosting/jsgetfalsevalue-function.md)  
  
-   [<span data-ttu-id="fd753-156">JsGetGlobalObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-156">JsGetGlobalObject Function</span></span>](../chakra-hosting/jsgetglobalobject-function.md)  
  
-   [<span data-ttu-id="fd753-157">JsGetIndexedPropertiesExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-157">JsGetIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jsgetindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-158">JsGetIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-158">JsGetIndexedProperty Function</span></span>](../chakra-hosting/jsgetindexedproperty-function.md)  
  
-   [<span data-ttu-id="fd753-159">JsGetNullValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-159">JsGetNullValue Function</span></span>](../chakra-hosting/jsgetnullvalue-function.md)  
  
-   [<span data-ttu-id="fd753-160">JsGetOwnPropertyDescriptor-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-160">JsGetOwnPropertyDescriptor Function</span></span>](../chakra-hosting/jsgetownpropertydescriptor-function.md)  
  
-   [<span data-ttu-id="fd753-161">JsGetOwnPropertyNames-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-161">JsGetOwnPropertyNames Function</span></span>](../chakra-hosting/jsgetownpropertynames-function.md)  
  
-   [<span data-ttu-id="fd753-162">JsGetOwnPropertySymbols-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-162">JsGetOwnPropertySymbols Function</span></span>](../chakra-hosting/jsgetownpropertysymbols-function.md)  
  
-   [<span data-ttu-id="fd753-163">JsGetProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-163">JsGetProperty Function</span></span>](../chakra-hosting/jsgetproperty-function.md)  
  
-   [<span data-ttu-id="fd753-164">JsGetPropertyIdFromName-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-164">JsGetPropertyIdFromName Function</span></span>](../chakra-hosting/jsgetpropertyidfromname-function.md)  
  
-   [<span data-ttu-id="fd753-165">JsGetPropertyIdFromSymbol-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-165">JsGetPropertyIdFromSymbol Function</span></span>](../chakra-hosting/jsgetpropertyidfromsymbol-function.md)  
  
-   [<span data-ttu-id="fd753-166">JsGetPropertyIdType-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-166">JsGetPropertyIdType Function</span></span>](../chakra-hosting/jsgetpropertyidtype-function.md)  
  
-   [<span data-ttu-id="fd753-167">JsGetPropertyNameFromId-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-167">JsGetPropertyNameFromId Function</span></span>](../chakra-hosting/jsgetpropertynamefromid-function.md)  
  
-   [<span data-ttu-id="fd753-168">JsGetPrototype-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-168">JsGetPrototype Function</span></span>](../chakra-hosting/jsgetprototype-function.md)  
  
-   [<span data-ttu-id="fd753-169">JsGetRuntime-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-169">JsGetRuntime Function</span></span>](../chakra-hosting/jsgetruntime-function.md)  
  
-   [<span data-ttu-id="fd753-170">JsGetRuntimeMemoryLimit-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-170">JsGetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jsgetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="fd753-171">JsGetRuntimeMemoryUsage-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-171">JsGetRuntimeMemoryUsage Function</span></span>](../chakra-hosting/jsgetruntimememoryusage-function.md)  
  
-   [<span data-ttu-id="fd753-172">JsGetStringLength-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-172">JsGetStringLength Function</span></span>](../chakra-hosting/jsgetstringlength-function.md)  
  
-   [<span data-ttu-id="fd753-173">JsGetSymbolFromPropertyId-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-173">JsGetSymbolFromPropertyId Function</span></span>](../chakra-hosting/jsgetsymbolfrompropertyid-function.md)  
  
-   [<span data-ttu-id="fd753-174">JsGetTrueValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-174">JsGetTrueValue Function</span></span>](../chakra-hosting/jsgettruevalue-function.md)  
  
-   [<span data-ttu-id="fd753-175">JsGetTypedArrayInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-175">JsGetTypedArrayInfo Function</span></span>](../chakra-hosting/jsgettypedarrayinfo-function.md)  
  
-   [<span data-ttu-id="fd753-176">JsGetTypedArrayStorage-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-176">JsGetTypedArrayStorage Function</span></span>](../chakra-hosting/jsgettypedarraystorage-function.md)  
  
-   [<span data-ttu-id="fd753-177">JsGetUndefinedValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-177">JsGetUndefinedValue Function</span></span>](../chakra-hosting/jsgetundefinedvalue-function.md)  
  
-   [<span data-ttu-id="fd753-178">JsGetValueType-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-178">JsGetValueType Function</span></span>](../chakra-hosting/jsgetvaluetype-function.md)  
  
-   [<span data-ttu-id="fd753-179">JsHasException-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-179">JsHasException Function</span></span>](../chakra-hosting/jshasexception-function.md)  
  
-   [<span data-ttu-id="fd753-180">JsHasExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-180">JsHasExternalData Function</span></span>](../chakra-hosting/jshasexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-181">JsHasIndexedPropertiesExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-181">JsHasIndexedPropertiesExternalData Function</span></span>](../chakra-hosting/jshasindexedpropertiesexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-182">JsHasIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-182">JsHasIndexedProperty Function</span></span>](../chakra-hosting/jshasindexedproperty-function.md)  
  
-   [<span data-ttu-id="fd753-183">JsHasProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-183">JsHasProperty Function</span></span>](../chakra-hosting/jshasproperty-function.md)  
  
-   [<span data-ttu-id="fd753-184">JsIdle-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-184">JsIdle Function</span></span>](../chakra-hosting/jsidle-function.md)  
  
-   [<span data-ttu-id="fd753-185">JsInspectableToObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-185">JsInspectableToObject Function</span></span>](../chakra-hosting/jsinspectabletoobject-function.md)  
  
-   [<span data-ttu-id="fd753-186">JsInstanceOf-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-186">JsInstanceOf Function</span></span>](../chakra-hosting/jsinstanceof-function.md)  
  
-   [<span data-ttu-id="fd753-187">JsIntToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-187">JsIntToNumber Function</span></span>](../chakra-hosting/jsinttonumber-function.md)  
  
-   [<span data-ttu-id="fd753-188">JsIsEnumeratingHeap-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-188">JsIsEnumeratingHeap Function</span></span>](../chakra-hosting/jsisenumeratingheap-function.md)  
  
-   [<span data-ttu-id="fd753-189">JsIsRuntimeExecutionDisabled-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-189">JsIsRuntimeExecutionDisabled Function</span></span>](../chakra-hosting/jsisruntimeexecutiondisabled-function.md)  
  
-   [<span data-ttu-id="fd753-190">JsNumberToDouble-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-190">JsNumberToDouble Function</span></span>](../chakra-hosting/jsnumbertodouble-function.md)  
  
-   [<span data-ttu-id="fd753-191">JsNumberToInt-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-191">JsNumberToInt Function</span></span>](../chakra-hosting/jsnumbertoint-function.md)  
  
-   [<span data-ttu-id="fd753-192">JsObjectToInspectable-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-192">JsObjectToInspectable Function</span></span>](../chakra-hosting/jsobjecttoinspectable-function.md)  
  
-   [<span data-ttu-id="fd753-193">JsParseScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-193">JsParseScript Function</span></span>](../chakra-hosting/jsparsescript-function.md)  
  
-   [<span data-ttu-id="fd753-194">JsParseSerializedScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-194">JsParseSerializedScript Function</span></span>](../chakra-hosting/jsparseserializedscript-function.md)  
  
-   [<span data-ttu-id="fd753-195">JsParseSerializedScriptWithCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-195">JsParseSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsparseserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="fd753-196">JsPointerToString-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-196">JsPointerToString Function</span></span>](../chakra-hosting/jspointertostring-function.md)  
  
-   [<span data-ttu-id="fd753-197">JsPreventExtension-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-197">JsPreventExtension Function</span></span>](../chakra-hosting/jspreventextension-function.md)  
  
-   [<span data-ttu-id="fd753-198">JsProjectWinRTNamespace-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-198">JsProjectWinRTNamespace Function</span></span>](../chakra-hosting/jsprojectwinrtnamespace-function.md)  
  
-   [<span data-ttu-id="fd753-199">JsRelease-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-199">JsRelease Function</span></span>](../chakra-hosting/jsrelease-function.md)  
  
-   [<span data-ttu-id="fd753-200">JsRunScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-200">JsRunScript Function</span></span>](../chakra-hosting/jsrunscript-function.md)  
  
-   [<span data-ttu-id="fd753-201">JsRunSerializedScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-201">JsRunSerializedScript Function</span></span>](../chakra-hosting/jsrunserializedscript-function.md)  
  
-   [<span data-ttu-id="fd753-202">JsRunSerializedScriptWithCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-202">JsRunSerializedScriptWithCallback Function</span></span>](../chakra-hosting/jsrunserializedscriptwithcallback-function.md)  
  
-   [<span data-ttu-id="fd753-203">JsSerializeScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-203">JsSerializeScript Function</span></span>](../chakra-hosting/jsserializescript-function.md)  
  
-   [<span data-ttu-id="fd753-204">JsSetContextData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-204">JsSetContextData Function</span></span>](../chakra-hosting/jssetcontextdata-function.md)  
  
-   [<span data-ttu-id="fd753-205">JsSetCurrentContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-205">JsSetCurrentContext Function</span></span>](../chakra-hosting/jssetcurrentcontext-function.md)  
  
-   [<span data-ttu-id="fd753-206">JsSetException-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-206">JsSetException Function</span></span>](../chakra-hosting/jssetexception-function.md)  
  
-   [<span data-ttu-id="fd753-207">JsSetExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-207">JsSetExternalData Function</span></span>](../chakra-hosting/jssetexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-208">JsSetIndexedPropertiesToExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-208">JsSetIndexedPropertiesToExternalData Function</span></span>](../chakra-hosting/jssetindexedpropertiestoexternaldata-function.md)  
  
-   [<span data-ttu-id="fd753-209">JsSetIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-209">JsSetIndexedProperty Function</span></span>](../chakra-hosting/jssetindexedproperty-function.md)  
  
-   [<span data-ttu-id="fd753-210">JsSetObjectBeforeCollectCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-210">JsSetObjectBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetobjectbeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="fd753-211">JsSetProjectionEnqueueCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-211">JsSetProjectionEnqueueCallback Function</span></span>](../chakra-hosting/jssetprojectionenqueuecallback-function.md)  
  
-   [<span data-ttu-id="fd753-212">JsSetPromiseContinuationCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-212">JsSetPromiseContinuationCallback Function</span></span>](../chakra-hosting/jssetpromisecontinuationcallback-function.md)  
  
-   [<span data-ttu-id="fd753-213">JsSetProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-213">JsSetProperty Function</span></span>](../chakra-hosting/jssetproperty-function.md)  
  
-   [<span data-ttu-id="fd753-214">JsSetPrototype-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-214">JsSetPrototype Function</span></span>](../chakra-hosting/jssetprototype-function.md)  
  
-   [<span data-ttu-id="fd753-215">JsSetRuntimeBeforeCollectCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](../chakra-hosting/jssetruntimebeforecollectcallback-function.md)  
  
-   [<span data-ttu-id="fd753-216">JsSetRuntimeMemoryAllocationCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](../chakra-hosting/jssetruntimememoryallocationcallback-function.md)  
  
-   [<span data-ttu-id="fd753-217">JsSetRuntimeMemoryLimit-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-217">JsSetRuntimeMemoryLimit Function</span></span>](../chakra-hosting/jssetruntimememorylimit-function.md)  
  
-   [<span data-ttu-id="fd753-218">JsStartDebugging-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-218">JsStartDebugging Function</span></span>](../chakra-hosting/jsstartdebugging-function.md)  
  
-   [<span data-ttu-id="fd753-219">JsStartProfiling-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-219">JsStartProfiling Function</span></span>](../chakra-hosting/jsstartprofiling-function.md)  
  
-   [<span data-ttu-id="fd753-220">JsStopProfiling-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-220">JsStopProfiling Function</span></span>](../chakra-hosting/jsstopprofiling-function.md)  
  
-   [<span data-ttu-id="fd753-221">JsStrictEquals-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-221">JsStrictEquals Function</span></span>](../chakra-hosting/jsstrictequals-function.md)  
  
-   [<span data-ttu-id="fd753-222">JsStringToPointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-222">JsStringToPointer Function</span></span>](../chakra-hosting/jsstringtopointer-function.md)  
  
-   [<span data-ttu-id="fd753-223">JsValueToVariant-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-223">JsValueToVariant Function</span></span>](../chakra-hosting/jsvaluetovariant-function.md)  
  
-   [<span data-ttu-id="fd753-224">JsVariantToValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd753-224">JsVariantToValue Function</span></span>](../chakra-hosting/jsvarianttovalue-function.md)  
  
## <span data-ttu-id="fd753-225">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd753-225">See Also</span></span>  
 [<span data-ttu-id="fd753-226">Hosten der JavaScript-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="fd753-226">Hosting the JavaScript Runtime</span></span>](../chakra-hosting/hosting-the-javascript-runtime.md)   
 [<span data-ttu-id="fd753-227">JavaScript-Runtime-Hosting</span><span class="sxs-lookup"><span data-stu-id="fd753-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)