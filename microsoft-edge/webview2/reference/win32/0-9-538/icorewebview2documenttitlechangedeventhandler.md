---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 674b97cce835721f3ffa622115d237ef81939a91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010278"
---
# <span data-ttu-id="3045d-104">0.9.579-Interface-ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3045d-104">0.9.579 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3045d-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="3045d-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="3045d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3045d-106">Summary</span></span>

 <span data-ttu-id="3045d-107">Member</span><span class="sxs-lookup"><span data-stu-id="3045d-107">Members</span></span>                        | <span data-ttu-id="3045d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3045d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3045d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3045d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3045d-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3045d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3045d-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3045d-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="3045d-112">Member</span><span class="sxs-lookup"><span data-stu-id="3045d-112">Members</span></span>

#### <span data-ttu-id="3045d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="3045d-113">Invoke</span></span> 

<span data-ttu-id="3045d-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3045d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3045d-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3045d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3045d-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3045d-116">There are no event args and the args parameter will be null.</span></span>

