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
ms.openlocfilehash: 428bf795edbfc7df843f9d100502e65c45440412
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653896"
---
# <span data-ttu-id="22b4d-104">Schnittstellen ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="22b4d-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="22b4d-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="22b4d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="22b4d-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="22b4d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="22b4d-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="22b4d-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="22b4d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="22b4d-108">Summary</span></span>

 <span data-ttu-id="22b4d-109">Member</span><span class="sxs-lookup"><span data-stu-id="22b4d-109">Members</span></span>                        | <span data-ttu-id="22b4d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="22b4d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="22b4d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="22b4d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="22b4d-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22b4d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="22b4d-113">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="22b4d-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="22b4d-114">Member</span><span class="sxs-lookup"><span data-stu-id="22b4d-114">Members</span></span>

#### <span data-ttu-id="22b4d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="22b4d-115">Invoke</span></span> 

<span data-ttu-id="22b4d-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22b4d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="22b4d-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="22b4d-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="22b4d-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="22b4d-118">There are no event args and the args parameter will be null.</span></span>

