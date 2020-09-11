---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 79af7b28b8b8ab7e2e2b6612f121208b8d917725
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010271"
---
# <span data-ttu-id="7a7a0-104">0.9.579-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7a7a0-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="7a7a0-105">Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7a7a0-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="7a7a0-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7a7a0-106">Summary</span></span>

 <span data-ttu-id="7a7a0-107">Member</span><span class="sxs-lookup"><span data-stu-id="7a7a0-107">Members</span></span>                        | <span data-ttu-id="7a7a0-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7a7a0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a7a0-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7a7a0-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="7a7a0-110">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a7a0-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="7a7a0-111">Member</span><span class="sxs-lookup"><span data-stu-id="7a7a0-111">Members</span></span>

#### <span data-ttu-id="7a7a0-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7a7a0-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="7a7a0-113">Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a7a0-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="7a7a0-114">Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7a7a0-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

