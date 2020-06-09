---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698831"
---
# <span data-ttu-id="f61f7-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f61f7-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="f61f7-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f61f7-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="f61f7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f61f7-106">Summary</span></span>

 <span data-ttu-id="f61f7-107">Member</span><span class="sxs-lookup"><span data-stu-id="f61f7-107">Members</span></span>                        | <span data-ttu-id="f61f7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f61f7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f61f7-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="f61f7-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="f61f7-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f61f7-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="f61f7-111">Member</span><span class="sxs-lookup"><span data-stu-id="f61f7-111">Members</span></span>

#### <span data-ttu-id="f61f7-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="f61f7-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="f61f7-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f61f7-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="f61f7-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f61f7-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

