---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880129"
---
# <span data-ttu-id="011d8-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="011d8-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="011d8-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="011d8-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="011d8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="011d8-106">Summary</span></span>

 <span data-ttu-id="011d8-107">Member</span><span class="sxs-lookup"><span data-stu-id="011d8-107">Members</span></span>                        | <span data-ttu-id="011d8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="011d8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="011d8-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="011d8-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="011d8-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="011d8-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="011d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="011d8-111">Members</span></span>

#### <span data-ttu-id="011d8-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="011d8-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="011d8-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="011d8-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="011d8-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="011d8-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

