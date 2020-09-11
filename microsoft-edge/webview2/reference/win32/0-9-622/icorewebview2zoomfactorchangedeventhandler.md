---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 116679e5b4168803af1c7e2909eb590af2378623
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012117"
---
# <span data-ttu-id="619f5-104">Schnittstellen ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="619f5-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="619f5-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="619f5-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="619f5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="619f5-106">Summary</span></span>

 <span data-ttu-id="619f5-107">Member</span><span class="sxs-lookup"><span data-stu-id="619f5-107">Members</span></span>                        | <span data-ttu-id="619f5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="619f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="619f5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="619f5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="619f5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="619f5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="619f5-111">Verwenden Sie die ICoreWebView2Controller. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="619f5-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="619f5-112">Member</span><span class="sxs-lookup"><span data-stu-id="619f5-112">Members</span></span>

#### <span data-ttu-id="619f5-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="619f5-113">Invoke</span></span> 

<span data-ttu-id="619f5-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="619f5-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="619f5-115">Public HRESULT [Invoke](#invoke)(ICoreWebView2Controller \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="619f5-115">public HRESULT [Invoke](#invoke)(ICoreWebView2Controller \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="619f5-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="619f5-116">There are no event args and the args parameter will be null.</span></span>

