---
description: Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.
title: JsCreateExternalArrayBuffer-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567300"
---
# <span data-ttu-id="13aa4-103">JsCreateExternalArrayBuffer Funktion</span><span class="sxs-lookup"><span data-stu-id="13aa4-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="13aa4-104">Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="13aa4-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="13aa4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13aa4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="13aa4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13aa4-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="13aa4-107">Ein Zeiger auf den externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="13aa4-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="13aa4-108">Die Anzahl der Bytes im externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="13aa4-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="13aa4-109">Ein Rückruf für den Zeitpunkt, zu dem das Objekt finalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="13aa4-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="13aa4-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="13aa4-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="13aa4-111">Der Benutzer hat den Zustand bereitgestellt, der an finalizeCallback zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13aa4-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="13aa4-112">Das neue `ArrayBuffer` Objekt.</span><span class="sxs-lookup"><span data-stu-id="13aa4-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="13aa4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13aa4-113">Return Value</span></span>  
 <span data-ttu-id="13aa4-114">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="13aa4-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="13aa4-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13aa4-115">Remarks</span></span>  
 <span data-ttu-id="13aa4-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="13aa4-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="13aa4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13aa4-117">Requirements</span></span>  
 <span data-ttu-id="13aa4-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="13aa4-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="13aa4-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13aa4-119">See Also</span></span>  
 [<span data-ttu-id="13aa4-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="13aa4-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)