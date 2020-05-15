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
ms.openlocfilehash: 81d3fe4620dcb439933d661d7b061819b5e07a00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654018"
---
# <span data-ttu-id="37775-104">Schnittstellen ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="37775-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="37775-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="37775-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="37775-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="37775-106">Summary</span></span>

 <span data-ttu-id="37775-107">Member</span><span class="sxs-lookup"><span data-stu-id="37775-107">Members</span></span>                        | <span data-ttu-id="37775-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="37775-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37775-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="37775-109">Invoke</span></span>](#invoke) | <span data-ttu-id="37775-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="37775-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="37775-111">Member</span><span class="sxs-lookup"><span data-stu-id="37775-111">Members</span></span>

#### <span data-ttu-id="37775-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="37775-112">Invoke</span></span> 

<span data-ttu-id="37775-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="37775-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="37775-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="37775-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

