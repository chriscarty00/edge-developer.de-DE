---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 0dc9886bc2282d08855ccb40cb8b06b4ffadb659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886114"
---
# <span data-ttu-id="b4554-104">0.8.355-Interface-IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b4554-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b4554-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b4554-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="b4554-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b4554-106">Summary</span></span>

 <span data-ttu-id="b4554-107">Member</span><span class="sxs-lookup"><span data-stu-id="b4554-107">Members</span></span>                        | <span data-ttu-id="b4554-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b4554-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b4554-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b4554-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b4554-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b4554-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b4554-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4554-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="b4554-112">Member</span><span class="sxs-lookup"><span data-stu-id="b4554-112">Members</span></span>

#### <span data-ttu-id="b4554-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b4554-113">Invoke</span></span> 

<span data-ttu-id="b4554-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b4554-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b4554-115">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b4554-115">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="b4554-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="b4554-116">There are no event args and the args parameter will be null.</span></span>

