---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 77cf5ffce5eb6fbb6d310968c998a3f65c08b11a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884218"
---
# <span data-ttu-id="43a00-104">0.9.430-Interface-ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="43a00-104">0.9.430 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="43a00-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="43a00-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="43a00-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="43a00-106">Summary</span></span>

 <span data-ttu-id="43a00-107">Member</span><span class="sxs-lookup"><span data-stu-id="43a00-107">Members</span></span>                        | <span data-ttu-id="43a00-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="43a00-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="43a00-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="43a00-109">Invoke</span></span>](#invoke) | <span data-ttu-id="43a00-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43a00-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="43a00-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="43a00-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="43a00-112">Member</span><span class="sxs-lookup"><span data-stu-id="43a00-112">Members</span></span>

#### <span data-ttu-id="43a00-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="43a00-113">Invoke</span></span> 

<span data-ttu-id="43a00-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43a00-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="43a00-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="43a00-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="43a00-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="43a00-116">There are no event args and the args parameter will be null.</span></span>

