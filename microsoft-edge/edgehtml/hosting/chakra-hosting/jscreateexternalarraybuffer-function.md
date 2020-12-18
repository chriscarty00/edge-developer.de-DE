---
description: Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.
title: JsCreateExternalArrayBuffer-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234141"
---
# <span data-ttu-id="7f0db-103">JsCreateExternalArrayBuffer Funktion</span><span class="sxs-lookup"><span data-stu-id="7f0db-103">JsCreateExternalArrayBuffer Function</span></span>

<span data-ttu-id="7f0db-104">Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="7f0db-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="7f0db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f0db-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="7f0db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f0db-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="7f0db-107">Ein Zeiger auf den externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="7f0db-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="7f0db-108">Die Anzahl der Bytes im externen Speicher.</span><span class="sxs-lookup"><span data-stu-id="7f0db-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="7f0db-109">Ein Rückruf für den Zeitpunkt, zu dem das Objekt finalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7f0db-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="7f0db-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7f0db-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="7f0db-111">Der Benutzer hat den Zustand bereitgestellt, der an finalizeCallback zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f0db-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="7f0db-112">Das neue `ArrayBuffer` Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f0db-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="7f0db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f0db-113">Return Value</span></span>  
 <span data-ttu-id="7f0db-114">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7f0db-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7f0db-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f0db-115">Remarks</span></span>  
 <span data-ttu-id="7f0db-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="7f0db-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7f0db-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f0db-117">Requirements</span></span>  
 <span data-ttu-id="7f0db-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7f0db-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7f0db-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f0db-119">See Also</span></span>  
 [<span data-ttu-id="7f0db-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="7f0db-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
