---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: c941629ab8ee87c0c964b00798878bb69265669a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011391"
---
# <span data-ttu-id="b942a-104">0.9.579-Interface-ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b942a-104">0.9.579 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b942a-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b942a-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="b942a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b942a-106">Summary</span></span>

 <span data-ttu-id="b942a-107">Member</span><span class="sxs-lookup"><span data-stu-id="b942a-107">Members</span></span>                        | <span data-ttu-id="b942a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b942a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b942a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b942a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b942a-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b942a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b942a-111">Verwenden Sie die ICoreWebView2Controller. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b942a-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="b942a-112">Member</span><span class="sxs-lookup"><span data-stu-id="b942a-112">Members</span></span>

#### <span data-ttu-id="b942a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b942a-113">Invoke</span></span> 

<span data-ttu-id="b942a-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b942a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b942a-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b942a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b942a-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="b942a-116">There are no event args and the args parameter will be null.</span></span>

