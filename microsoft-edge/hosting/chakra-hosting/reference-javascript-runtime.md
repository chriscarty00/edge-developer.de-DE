---
description: JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.
title: Reference (JavaScript Runtime)
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
# Reference (JavaScript runtime)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.  

If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.  

## In this section  

Typedefs, constants, and enumerations that support JsRT hosting are described here:  
  
*   [JavaScript Runtime Typedefs, Constants, and Enumerations](./javascript-runtime-typedefs-constants-and-enumerations.md)  

The following functions enable JsRT hosting:  

*   [JsAddRef Function](./jsaddref-function.md)  
*   [JsBooleanToBool Funktion](./jsbooleantobool-function.md)  
*   [JsBoolToBoolean Funktion](./jsbooltoboolean-function.md)  
*   [JsCallFunction Funktion](./jscallfunction-function.md)  
*   [JsCollectGarbage Funktion](./jscollectgarbage-function.md)  
*   [JsConstructObject Funktion](./jsconstructobject-function.md)  
*   [JsConvertValueToBoolean Funktion](./jsconvertvaluetoboolean-function.md)  
*   [JsConvertValueToNumber Funktion](./jsconvertvaluetonumber-function.md)  
*   [JsConvertValueToObject Funktion](./jsconvertvaluetoobject-function.md)  
*   [JsConvertValueToString Funktion](./jsconvertvaluetostring-function.md)  
*   [JsCreateArray Funktion](./jscreatearray-function.md)  
*   [JsCreateArrayBuffer Funktion](./jscreatearraybuffer-function.md)  
*   [JsCreateContext Funktion](./jscreatecontext-function.md)  
*   [JsCreateDataView Funktion](./jscreatedataview-function.md)  
*   [JsCreateError Funktion](./jscreateerror-function.md)  
*   [JsCreateExternalArrayBuffer Funktion](./jscreateexternalarraybuffer-function.md)  
*   [JsCreateExternalObject Funktion](./jscreateexternalobject-function.md)  
*   [JsCreateFunction Funktion](./jscreatefunction-function.md)  
*   [JsCreateNamedFunction Funktion](./jscreatenamedfunction-function.md)  
*   [JsCreateObject Funktion](./jscreateobject-function.md)  
*   [JsCreateRangeError Funktion](./jscreaterangeerror-function.md)  
*   [JsCreateReferenceError Funktion](./jscreatereferenceerror-function.md)  
*   [JsCreateRuntime Funktion](./jscreateruntime-function.md)  
*   [JsCreateSymbol Funktion](./jscreatesymbol-function.md)  
*   [JsCreateSyntaxError Funktion](./jscreatesyntaxerror-function.md)  
*   [JsCreateTypeError Funktion](./jscreatetypeerror-function.md)  
*   [JsCreateTypedArray Funktion](./jscreatetypedarray-function.md)  
*   [JsCreateURIError Funktion](./jscreateurierror-function.md)  
*   [JsDefineProperty Funktion](./jsdefineproperty-function.md)  
*   [JsDeleteIndexedProperty Funktion](./jsdeleteindexedproperty-function.md)  
*   [JsDeleteProperty Funktion](./jsdeleteproperty-function.md)  
*   [JsDisableRuntimeExecution Funktion](./jsdisableruntimeexecution-function.md)  
*   [JsDisposeRuntime Funktion](./jsdisposeruntime-function.md)  
*   [JsDoubleToNumber Funktion](./jsdoubletonumber-function.md)  
*   [JsEnableRuntimeExecution Funktion](./jsenableruntimeexecution-function.md)  
*   [JsEnumerateHeap Funktion](./jsenumerateheap-function.md)  
*   [JsEquals Funktion](./jsequals-function.md)  
*   [JsGetAndClearException Funktion](./jsgetandclearexception-function.md)  
*   [JsGetArrayBufferStorage Funktion](./jsgetarraybufferstorage-function.md)  
*   [JsGetContextData Funktion](./jsgetcontextdata-function.md)  
*   [JsGetContextOfObject Funktion](./jsgetcontextofobject-function.md)  
*   [JsGetCurrentContext Funktion](./jsgetcurrentcontext-function.md)  
*   [JsGetDataViewStorage Funktion](./jsgetdataviewstorage-function.md)  
*   [JsGetExtensionAllowed Funktion](./jsgetextensionallowed-function.md)  
*   [JsGetExternalData Funktion](./jsgetexternaldata-function.md)  
*   [JsGetFalseValue Funktion](./jsgetfalsevalue-function.md)  
*   [JsGetGlobalObject Funktion](./jsgetglobalobject-function.md)  
*   [JsGetIndexedPropertiesExternalData Funktion](./jsgetindexedpropertiesexternaldata-function.md)  
*   [JsGetIndexedProperty Funktion](./jsgetindexedproperty-function.md)  
*   [JsGetNullValue Funktion](./jsgetnullvalue-function.md)  
*   [JsGetOwnPropertyDescriptor Funktion](./jsgetownpropertydescriptor-function.md)  
*   [JsGetOwnPropertyNames Funktion](./jsgetownpropertynames-function.md)  
*   [JsGetOwnPropertySymbols Funktion](./jsgetownpropertysymbols-function.md)  
*   [JsGetProperty Funktion](./jsgetproperty-function.md)  
*   [JsGetPropertyIdFromName Funktion](./jsgetpropertyidfromname-function.md)  
*   [JsGetPropertyIdFromSymbol Funktion](./jsgetpropertyidfromsymbol-function.md)  
*   [JsGetPropertyIdType Funktion](./jsgetpropertyidtype-function.md)  
*   [JsGetPropertyNameFromId Funktion](./jsgetpropertynamefromid-function.md)  
*   [JsGetPrototype Funktion](./jsgetprototype-function.md)  
*   [JsGetRuntime Funktion](./jsgetruntime-function.md)  
*   [JsGetRuntimeMemoryLimit Funktion](./jsgetruntimememorylimit-function.md)  
*   [JsGetRuntimeMemoryUsage Funktion](./jsgetruntimememoryusage-function.md)  
*   [JsGetStringLength Funktion](./jsgetstringlength-function.md)  
*   [JsGetSymbolFromPropertyId Funktion](./jsgetsymbolfrompropertyid-function.md)  
*   [JsGetTrueValue Funktion](./jsgettruevalue-function.md)  
*   [JsGetTypedArrayInfo Funktion](./jsgettypedarrayinfo-function.md)  
*   [JsGetTypedArrayStorage Funktion](./jsgettypedarraystorage-function.md)  
*   [JsGetUndefinedValue Funktion](./jsgetundefinedvalue-function.md)  
*   [JsGetValueType Funktion](./jsgetvaluetype-function.md)  
*   [JsHasException Funktion](./jshasexception-function.md)  
*   [JsHasExternalData Funktion](./jshasexternaldata-function.md)  
*   [JsHasIndexedPropertiesExternalData Funktion](./jshasindexedpropertiesexternaldata-function.md)  
*   [JsHasIndexedProperty Funktion](./jshasindexedproperty-function.md)  
*   [JsHasProperty Funktion](./jshasproperty-function.md)  
*   [JsIdle Funktion](./jsidle-function.md)  
*   [JsInspectableToObject Funktion](./jsinspectabletoobject-function.md)  
*   [JsInstanceOf Funktion](./jsinstanceof-function.md)  
*   [JsIntToNumber Funktion](./jsinttonumber-function.md)  
*   [JsIsEnumeratingHeap Funktion](./jsisenumeratingheap-function.md)  
*   [JsIsRuntimeExecutionDisabled Funktion](./jsisruntimeexecutiondisabled-function.md)  
*   [JsNumberToDouble Funktion](./jsnumbertodouble-function.md)  
*   [JsNumberToInt Funktion](./jsnumbertoint-function.md)  
*   [JsObjectToInspectable Funktion](./jsobjecttoinspectable-function.md)  
*   [JsParseScript Funktion](./jsparsescript-function.md)  
*   [JsParseSerializedScript Funktion](./jsparseserializedscript-function.md)  
*   [JsParseSerializedScriptWithCallback Funktion](./jsparseserializedscriptwithcallback-function.md)  
*   [JsPointerToString Funktion](./jspointertostring-function.md)  
*   [JsPreventExtension Funktion](./jspreventextension-function.md)  
*   [JsProjectWinRTNamespace Funktion](./jsprojectwinrtnamespace-function.md)  
*   [JsRelease Funktion](./jsrelease-function.md)  
*   [JsRunScript Funktion](./jsrunscript-function.md)  
*   [JsRunSerializedScript Funktion](./jsrunserializedscript-function.md)  
*   [JsRunSerializedScriptWithCallback Funktion](./jsrunserializedscriptwithcallback-function.md)  
*   [JsSerializeScript Funktion](./jsserializescript-function.md)  
*   [JsSetContextData Funktion](./jssetcontextdata-function.md)  
*   [JsSetCurrentContext Funktion](./jssetcurrentcontext-function.md)  
*   [JsSetException Funktion](./jssetexception-function.md)  
*   [JsSetExternalData Funktion](./jssetexternaldata-function.md)  
*   [JsSetIndexedPropertiesToExternalData Funktion](./jssetindexedpropertiestoexternaldata-function.md)  
*   [JsSetIndexedProperty Funktion](./jssetindexedproperty-function.md)  
*   [JsSetObjectBeforeCollectCallback Funktion](./jssetobjectbeforecollectcallback-function.md)  
*   [JsSetProjectionEnqueueCallback Funktion](./jssetprojectionenqueuecallback-function.md)  
*   [JsSetPromiseContinuationCallback Funktion](./jssetpromisecontinuationcallback-function.md)  
*   [JsSetProperty Funktion](./jssetproperty-function.md)  
*   [JsSetPrototype Funktion](./jssetprototype-function.md)  
*   [JsSetRuntimeBeforeCollectCallback Funktion](./jssetruntimebeforecollectcallback-function.md)  
*   [JsSetRuntimeMemoryAllocationCallback Funktion](./jssetruntimememoryallocationcallback-function.md)  
*   [JsSetRuntimeMemoryLimit Funktion](./jssetruntimememorylimit-function.md)  
*   [JsStartDebugging Funktion](./jsstartdebugging-function.md)  
*   [JsStartProfiling Funktion](./jsstartprofiling-function.md)  
*   [JsStopProfiling Funktion](./jsstopprofiling-function.md)  
*   [JsStrictEquals Funktion](./jsstrictequals-function.md)  
*   [JsStringToPointer Funktion](./jsstringtopointer-function.md)  
*   [JsValueToVariant Funktion](./jsvaluetovariant-function.md)  
*   [JsVariantToValue Function](./jsvarianttovalue-function.md)  

## See also  

*   [Hosting the JavaScript Runtime](./hosting-the-javascript-runtime.md)  
*   [JavaScript Runtime Hosting](../javascript-runtime-hosting.md)  
