---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e7fbc952a44bdd38e6e59c46adafb8e71b7904b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653983"
---
# <span data-ttu-id="7c17a-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7c17a-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="7c17a-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7c17a-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="7c17a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7c17a-106">Summary</span></span>

 <span data-ttu-id="7c17a-107">Member</span><span class="sxs-lookup"><span data-stu-id="7c17a-107">Members</span></span>                        | <span data-ttu-id="7c17a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7c17a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7c17a-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7c17a-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="7c17a-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c17a-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="7c17a-111">Member</span><span class="sxs-lookup"><span data-stu-id="7c17a-111">Members</span></span>

#### <span data-ttu-id="7c17a-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7c17a-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="7c17a-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c17a-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="7c17a-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7c17a-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

