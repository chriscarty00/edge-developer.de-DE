---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 74cd0451e111780078714b17e5bd1097c56d6b2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877574"
---
# <span data-ttu-id="c0212-104">Schnittstellen ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c0212-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c0212-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c0212-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="c0212-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c0212-106">Summary</span></span>

 <span data-ttu-id="c0212-107">Member</span><span class="sxs-lookup"><span data-stu-id="c0212-107">Members</span></span>                        | <span data-ttu-id="c0212-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c0212-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0212-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0212-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c0212-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c0212-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c0212-111">Verwenden Sie die ICoreWebView2Controller. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0212-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="c0212-112">Member</span><span class="sxs-lookup"><span data-stu-id="c0212-112">Members</span></span>

#### <span data-ttu-id="c0212-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0212-113">Invoke</span></span> 

<span data-ttu-id="c0212-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c0212-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c0212-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c0212-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c0212-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="c0212-116">There are no event args and the args parameter will be null.</span></span>

