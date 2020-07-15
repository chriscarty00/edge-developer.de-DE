---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 3fdbe4d978a6a703576dd1135f7b79efad1befa5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881095"
---
# <span data-ttu-id="fdbdd-104">0.9.430-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fdbdd-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fdbdd-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fdbdd-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="fdbdd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="fdbdd-107">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="fdbdd-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fdbdd-108">Summary</span></span>

 <span data-ttu-id="fdbdd-109">Member</span><span class="sxs-lookup"><span data-stu-id="fdbdd-109">Members</span></span>                        | <span data-ttu-id="fdbdd-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fdbdd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fdbdd-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="fdbdd-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="fdbdd-112">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="fdbdd-113">Member</span><span class="sxs-lookup"><span data-stu-id="fdbdd-113">Members</span></span>

#### <span data-ttu-id="fdbdd-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="fdbdd-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="fdbdd-115">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="fdbdd-116">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

