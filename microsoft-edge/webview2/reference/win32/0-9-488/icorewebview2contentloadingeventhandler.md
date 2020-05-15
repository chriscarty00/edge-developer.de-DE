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
ms.openlocfilehash: e0f2350cbf91789402a340e56ef9b3309ba38e77
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653990"
---
# <span data-ttu-id="17a40-104">Schnittstellen ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="17a40-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="17a40-105">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="17a40-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="17a40-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="17a40-106">Summary</span></span>

 <span data-ttu-id="17a40-107">Member</span><span class="sxs-lookup"><span data-stu-id="17a40-107">Members</span></span>                        | <span data-ttu-id="17a40-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="17a40-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17a40-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="17a40-109">Invoke</span></span>](#invoke) | <span data-ttu-id="17a40-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="17a40-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="17a40-111">Member</span><span class="sxs-lookup"><span data-stu-id="17a40-111">Members</span></span>

#### <span data-ttu-id="17a40-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="17a40-112">Invoke</span></span> 

<span data-ttu-id="17a40-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="17a40-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="17a40-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="17a40-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

