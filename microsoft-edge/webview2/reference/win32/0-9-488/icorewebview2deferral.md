---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7d21db7c3f0a66f60f32e92b3951151b8d13a002
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698078"
---
# <span data-ttu-id="cb81c-104">Schnittstellen ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="cb81c-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="cb81c-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cb81c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cb81c-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cb81c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="cb81c-107">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cb81c-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="cb81c-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cb81c-108">Summary</span></span>

 <span data-ttu-id="cb81c-109">Member</span><span class="sxs-lookup"><span data-stu-id="cb81c-109">Members</span></span>                        | <span data-ttu-id="cb81c-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cb81c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cb81c-111">Complete</span><span class="sxs-lookup"><span data-stu-id="cb81c-111">Complete</span></span>](#complete) | <span data-ttu-id="cb81c-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="cb81c-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="cb81c-113">Member</span><span class="sxs-lookup"><span data-stu-id="cb81c-113">Members</span></span>

#### <span data-ttu-id="cb81c-114">Complete</span><span class="sxs-lookup"><span data-stu-id="cb81c-114">Complete</span></span> 

<span data-ttu-id="cb81c-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="cb81c-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="cb81c-116">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="cb81c-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="cb81c-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb81c-117">Complete should only be called once for each deferral taken.</span></span>

