---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 160395777b2936894001adfff1450d790e8da2c4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654007"
---
# <span data-ttu-id="10e79-104">Schnittstellen ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="10e79-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="10e79-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="10e79-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="10e79-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="10e79-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="10e79-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="10e79-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="10e79-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="10e79-108">Summary</span></span>

 <span data-ttu-id="10e79-109">Member</span><span class="sxs-lookup"><span data-stu-id="10e79-109">Members</span></span>                        | <span data-ttu-id="10e79-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="10e79-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10e79-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="10e79-111">Invoke</span></span>](#invoke) | <span data-ttu-id="10e79-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="10e79-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="10e79-113">Member</span><span class="sxs-lookup"><span data-stu-id="10e79-113">Members</span></span>

#### <span data-ttu-id="10e79-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="10e79-114">Invoke</span></span> 

<span data-ttu-id="10e79-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="10e79-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="10e79-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="10e79-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="10e79-117">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="10e79-117">There are no event args and the args parameter will be null.</span></span>

