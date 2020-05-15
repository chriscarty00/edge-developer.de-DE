---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: cf321ff1091883827b7ce6cda7248a06f1128867
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653960"
---
# <span data-ttu-id="e5d19-104">Schnittstellen IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e5d19-104">interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e5d19-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e5d19-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e5d19-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d19-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="e5d19-107">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e5d19-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="e5d19-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e5d19-108">Summary</span></span>

 <span data-ttu-id="e5d19-109">Member</span><span class="sxs-lookup"><span data-stu-id="e5d19-109">Members</span></span>                        | <span data-ttu-id="e5d19-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e5d19-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5d19-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e5d19-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="e5d19-112">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5d19-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="e5d19-113">Member</span><span class="sxs-lookup"><span data-stu-id="e5d19-113">Members</span></span>

#### <span data-ttu-id="e5d19-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e5d19-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="e5d19-115">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5d19-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="e5d19-116">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e5d19-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

