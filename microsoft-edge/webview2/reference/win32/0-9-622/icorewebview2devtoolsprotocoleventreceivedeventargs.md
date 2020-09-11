---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 079b7840689fbeb2931a22f72ad78c1ce0f590b8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012181"
---
# <span data-ttu-id="2a354-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2a354-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="2a354-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2a354-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="2a354-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2a354-106">Summary</span></span>

 <span data-ttu-id="2a354-107">Member</span><span class="sxs-lookup"><span data-stu-id="2a354-107">Members</span></span>                        | <span data-ttu-id="2a354-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2a354-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2a354-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="2a354-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="2a354-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a354-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="2a354-111">Member</span><span class="sxs-lookup"><span data-stu-id="2a354-111">Members</span></span>

#### <span data-ttu-id="2a354-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="2a354-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="2a354-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a354-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="2a354-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="2a354-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

