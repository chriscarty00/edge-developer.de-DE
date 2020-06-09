---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2908ad851a7899d2ea053bfa50616c8b244bca6c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698825"
---
# <span data-ttu-id="72b57-104">Schnittstellen ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="72b57-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="72b57-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="72b57-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="72b57-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="72b57-106">Summary</span></span>

 <span data-ttu-id="72b57-107">Member</span><span class="sxs-lookup"><span data-stu-id="72b57-107">Members</span></span>                        | <span data-ttu-id="72b57-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="72b57-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72b57-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="72b57-109">Invoke</span></span>](#invoke) | <span data-ttu-id="72b57-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="72b57-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="72b57-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="72b57-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="72b57-112">Member</span><span class="sxs-lookup"><span data-stu-id="72b57-112">Members</span></span>

#### <span data-ttu-id="72b57-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="72b57-113">Invoke</span></span> 

<span data-ttu-id="72b57-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="72b57-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="72b57-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="72b57-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="72b57-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="72b57-116">There are no event args and the args parameter will be null.</span></span>

