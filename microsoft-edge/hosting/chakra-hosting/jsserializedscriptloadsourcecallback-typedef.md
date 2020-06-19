---
description: Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden. Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752199"
---
# <span data-ttu-id="189c4-104">JsSerializedScriptLoadSourceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="189c4-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="189c4-105">Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden.</span><span class="sxs-lookup"><span data-stu-id="189c4-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="189c4-106">Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="189c4-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="189c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="189c4-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="189c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="189c4-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="189c4-109">Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="189c4-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="189c4-110">Das Skript wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="189c4-110">The script returned.</span></span>  
  
## <span data-ttu-id="189c4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="189c4-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="189c4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="189c4-112">Requirements</span></span>  
 <span data-ttu-id="189c4-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="189c4-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="189c4-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="189c4-114">See Also</span></span>  
 [<span data-ttu-id="189c4-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="189c4-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)