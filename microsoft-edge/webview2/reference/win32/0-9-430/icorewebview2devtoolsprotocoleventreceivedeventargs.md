---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 5292acf08102afdda33da43575b2e0e584247ecb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653868"
---
# <span data-ttu-id="9ca52-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ca52-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9ca52-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9ca52-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9ca52-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca52-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="9ca52-107">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9ca52-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="9ca52-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9ca52-108">Summary</span></span>

 <span data-ttu-id="9ca52-109">Member</span><span class="sxs-lookup"><span data-stu-id="9ca52-109">Members</span></span>                        | <span data-ttu-id="9ca52-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9ca52-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ca52-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="9ca52-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="9ca52-112">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9ca52-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="9ca52-113">Member</span><span class="sxs-lookup"><span data-stu-id="9ca52-113">Members</span></span>

#### <span data-ttu-id="9ca52-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="9ca52-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="9ca52-115">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9ca52-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="9ca52-116">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="9ca52-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

