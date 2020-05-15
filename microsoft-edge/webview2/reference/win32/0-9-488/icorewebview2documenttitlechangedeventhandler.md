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
ms.openlocfilehash: 25e6318a695d67995f6fbf1b2ad4b02e1a982860
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653973"
---
# <span data-ttu-id="5a8e3-104">Schnittstellen ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5a8e3-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5a8e3-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="5a8e3-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="5a8e3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5a8e3-106">Summary</span></span>

 <span data-ttu-id="5a8e3-107">Member</span><span class="sxs-lookup"><span data-stu-id="5a8e3-107">Members</span></span>                        | <span data-ttu-id="5a8e3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5a8e3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5a8e3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5a8e3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5a8e3-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5a8e3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5a8e3-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a8e3-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="5a8e3-112">Member</span><span class="sxs-lookup"><span data-stu-id="5a8e3-112">Members</span></span>

#### <span data-ttu-id="5a8e3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5a8e3-113">Invoke</span></span> 

<span data-ttu-id="5a8e3-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5a8e3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5a8e3-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5a8e3-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="5a8e3-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="5a8e3-116">There are no event args and the args parameter will be null.</span></span>

