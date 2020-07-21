---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 22c5e558238e4542ebe70855c3d20837838bebb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883961"
---
# <span data-ttu-id="9056a-104">0.9.430-Interface-ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9056a-104">0.9.430 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9056a-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="9056a-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="9056a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9056a-106">Summary</span></span>

 <span data-ttu-id="9056a-107">Member</span><span class="sxs-lookup"><span data-stu-id="9056a-107">Members</span></span>                        | <span data-ttu-id="9056a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9056a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9056a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9056a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9056a-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9056a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9056a-111">Verwenden Sie die ICoreWebView2Host. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9056a-111">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="9056a-112">Member</span><span class="sxs-lookup"><span data-stu-id="9056a-112">Members</span></span>

#### <span data-ttu-id="9056a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="9056a-113">Invoke</span></span> 

<span data-ttu-id="9056a-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9056a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9056a-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9056a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="9056a-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9056a-116">There are no event args and the args parameter will be null.</span></span>

