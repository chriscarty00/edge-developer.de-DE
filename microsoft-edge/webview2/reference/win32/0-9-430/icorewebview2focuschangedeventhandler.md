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
ms.openlocfilehash: 3d70e87f9521beb8761d61012305f6d5eb06f923
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653786"
---
# <span data-ttu-id="02910-104">Schnittstellen ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="02910-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="02910-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="02910-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="02910-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="02910-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="02910-107">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="02910-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="02910-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="02910-108">Summary</span></span>

 <span data-ttu-id="02910-109">Member</span><span class="sxs-lookup"><span data-stu-id="02910-109">Members</span></span>                        | <span data-ttu-id="02910-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="02910-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02910-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="02910-111">Invoke</span></span>](#invoke) | <span data-ttu-id="02910-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="02910-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="02910-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="02910-113">There are no event args for this event.</span></span>

## <span data-ttu-id="02910-114">Member</span><span class="sxs-lookup"><span data-stu-id="02910-114">Members</span></span>

#### <span data-ttu-id="02910-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="02910-115">Invoke</span></span> 

<span data-ttu-id="02910-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="02910-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="02910-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="02910-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="02910-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="02910-118">There are no event args and the args parameter will be null.</span></span>

