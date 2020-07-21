---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c42e353c80335b6dccdad49b470e68fa5ae2f559
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884253"
---
# <span data-ttu-id="6980d-104">0.9.430-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6980d-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="6980d-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6980d-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="6980d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6980d-106">Summary</span></span>

 <span data-ttu-id="6980d-107">Member</span><span class="sxs-lookup"><span data-stu-id="6980d-107">Members</span></span>                        | <span data-ttu-id="6980d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6980d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6980d-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="6980d-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="6980d-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6980d-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="6980d-111">Member</span><span class="sxs-lookup"><span data-stu-id="6980d-111">Members</span></span>

#### <span data-ttu-id="6980d-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="6980d-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="6980d-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6980d-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="6980d-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6980d-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

