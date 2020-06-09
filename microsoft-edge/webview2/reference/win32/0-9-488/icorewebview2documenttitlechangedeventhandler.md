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
ms.openlocfilehash: 84ff41eeb30d5c3561666a71f989e02163419152
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697966"
---
# <span data-ttu-id="21c4c-104">Schnittstellen ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="21c4c-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="21c4c-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="21c4c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="21c4c-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="21c4c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="21c4c-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="21c4c-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="21c4c-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="21c4c-108">Summary</span></span>

 <span data-ttu-id="21c4c-109">Member</span><span class="sxs-lookup"><span data-stu-id="21c4c-109">Members</span></span>                        | <span data-ttu-id="21c4c-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="21c4c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21c4c-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="21c4c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="21c4c-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="21c4c-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="21c4c-113">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="21c4c-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="21c4c-114">Member</span><span class="sxs-lookup"><span data-stu-id="21c4c-114">Members</span></span>

#### <span data-ttu-id="21c4c-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="21c4c-115">Invoke</span></span> 

<span data-ttu-id="21c4c-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="21c4c-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="21c4c-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="21c4c-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="21c4c-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="21c4c-118">There are no event args and the args parameter will be null.</span></span>

