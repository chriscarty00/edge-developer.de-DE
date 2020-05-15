---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: d43cbe741cc9cd8b027a21115133db9377a95658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653898"
---
# <span data-ttu-id="b84b4-104">Schnittstellen IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="b84b4-104">interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="b84b4-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b84b4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b84b4-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="b84b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="b84b4-107">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b84b4-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="b84b4-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b84b4-108">Summary</span></span>

 <span data-ttu-id="b84b4-109">Member</span><span class="sxs-lookup"><span data-stu-id="b84b4-109">Members</span></span>                        | <span data-ttu-id="b84b4-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b84b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b84b4-111">Complete</span><span class="sxs-lookup"><span data-stu-id="b84b4-111">Complete</span></span>](#complete) | <span data-ttu-id="b84b4-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="b84b4-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="b84b4-113">Member</span><span class="sxs-lookup"><span data-stu-id="b84b4-113">Members</span></span>

#### <span data-ttu-id="b84b4-114">Complete</span><span class="sxs-lookup"><span data-stu-id="b84b4-114">Complete</span></span> 

<span data-ttu-id="b84b4-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="b84b4-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="b84b4-116">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="b84b4-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="b84b4-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b84b4-117">Complete should only be called once for each deferral taken.</span></span>

