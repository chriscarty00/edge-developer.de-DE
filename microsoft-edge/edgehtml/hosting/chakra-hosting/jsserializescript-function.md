---
description: Serialisiert ein analysiertes Skript in einen Puffer, als wieder verwendet werden kann.
title: JsSerializeScript-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234260"
---
# <span data-ttu-id="d6fd8-103">JsSerializeScript Funktion</span><span class="sxs-lookup"><span data-stu-id="d6fd8-103">JsSerializeScript Function</span></span>

<span data-ttu-id="d6fd8-104">Serialisiert ein analysiertes Skript in einen Puffer, als wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="d6fd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6fd8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="d6fd8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6fd8-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="d6fd8-107">Das zu serialisierende Skript.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="d6fd8-108">Der Puffer, in den das serialisierte Skript eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="d6fd8-109">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="d6fd8-110">Beim Eintrag die Größe des Puffers in Bytes; beim Beenden muss die Größe des Puffers in Byte für das serialisierte Skript angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="d6fd8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6fd8-111">Return Value</span></span>  
 <span data-ttu-id="d6fd8-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d6fd8-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6fd8-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="d6fd8-114">analysiert ein Skript und speichert dann die analysierte Form des Skripts in einem Laufzeit-unabhängigen Format.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="d6fd8-115">Das serialisierte Skript kann dann in einer beliebigen Laufzeit deserialisiert werden, ohne dass das Skript erneut analysiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="d6fd8-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d6fd8-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d6fd8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6fd8-117">Requirements</span></span>  
 <span data-ttu-id="d6fd8-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d6fd8-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d6fd8-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6fd8-119">See Also</span></span>  
 [<span data-ttu-id="d6fd8-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d6fd8-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
