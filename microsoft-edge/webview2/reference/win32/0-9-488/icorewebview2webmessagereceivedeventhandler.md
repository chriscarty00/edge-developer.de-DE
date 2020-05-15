---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 73af2e217ca645536623eca18ceafad3270529cd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654003"
---
# <span data-ttu-id="680e5-104">Schnittstellen ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="680e5-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="680e5-105">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="680e5-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="680e5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="680e5-106">Summary</span></span>

 <span data-ttu-id="680e5-107">Member</span><span class="sxs-lookup"><span data-stu-id="680e5-107">Members</span></span>                        | <span data-ttu-id="680e5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="680e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="680e5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="680e5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="680e5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="680e5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="680e5-111">Member</span><span class="sxs-lookup"><span data-stu-id="680e5-111">Members</span></span>

#### <span data-ttu-id="680e5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="680e5-112">Invoke</span></span> 

<span data-ttu-id="680e5-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="680e5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="680e5-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="680e5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

