---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bd2ff8092ce0b8367ce4cc381e94dbd273ae1849
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880829"
---
# <span data-ttu-id="af06f-104">0.9.515-Interface-ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="af06f-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="af06f-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="af06f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="af06f-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="af06f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="af06f-107">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="af06f-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="af06f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="af06f-108">Summary</span></span>

 <span data-ttu-id="af06f-109">Member</span><span class="sxs-lookup"><span data-stu-id="af06f-109">Members</span></span>                        | <span data-ttu-id="af06f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="af06f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af06f-111">Complete</span><span class="sxs-lookup"><span data-stu-id="af06f-111">Complete</span></span>](#complete) | <span data-ttu-id="af06f-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="af06f-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="af06f-113">Member</span><span class="sxs-lookup"><span data-stu-id="af06f-113">Members</span></span>

#### <span data-ttu-id="af06f-114">Complete</span><span class="sxs-lookup"><span data-stu-id="af06f-114">Complete</span></span> 

<span data-ttu-id="af06f-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="af06f-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="af06f-116">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="af06f-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="af06f-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="af06f-117">Complete should only be called once for each deferral taken.</span></span>

