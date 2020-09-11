---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 4b280a16c18c84641f91efd39407f93db968f69d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012178"
---
# <span data-ttu-id="62fc6-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="62fc6-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="62fc6-105">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="62fc6-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="62fc6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="62fc6-106">Summary</span></span>

 <span data-ttu-id="62fc6-107">Member</span><span class="sxs-lookup"><span data-stu-id="62fc6-107">Members</span></span>                        | <span data-ttu-id="62fc6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="62fc6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="62fc6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="62fc6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="62fc6-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62fc6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="62fc6-111">Member</span><span class="sxs-lookup"><span data-stu-id="62fc6-111">Members</span></span>

#### <span data-ttu-id="62fc6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="62fc6-112">Invoke</span></span> 

<span data-ttu-id="62fc6-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62fc6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="62fc6-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="62fc6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

