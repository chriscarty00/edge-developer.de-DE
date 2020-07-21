---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884666"
---
# <span data-ttu-id="5ebd3-104">0.8.355-Interface-IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5ebd3-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5ebd3-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="5ebd3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5ebd3-106">Summary</span></span>

 <span data-ttu-id="5ebd3-107">Member</span><span class="sxs-lookup"><span data-stu-id="5ebd3-107">Members</span></span>                        | <span data-ttu-id="5ebd3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5ebd3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ebd3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5ebd3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5ebd3-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5ebd3-111">Verwenden Sie die IWebView2WebView. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-111">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="5ebd3-112">Member</span><span class="sxs-lookup"><span data-stu-id="5ebd3-112">Members</span></span>

#### <span data-ttu-id="5ebd3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5ebd3-113">Invoke</span></span> 

<span data-ttu-id="5ebd3-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5ebd3-115">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5ebd3-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="5ebd3-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-116">There are no event args and the args parameter will be null.</span></span>

