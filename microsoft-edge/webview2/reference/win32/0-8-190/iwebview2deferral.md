---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: f40d0baa415ccc76747993c4070bb05eaf76fe56
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878610"
---
# <span data-ttu-id="20b38-104">0.8.355-Interface-IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="20b38-104">0.8.355 - interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="20b38-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="20b38-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="20b38-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="20b38-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="20b38-107">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="20b38-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="20b38-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="20b38-108">Summary</span></span>

 <span data-ttu-id="20b38-109">Member</span><span class="sxs-lookup"><span data-stu-id="20b38-109">Members</span></span>                        | <span data-ttu-id="20b38-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="20b38-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="20b38-111">Complete</span><span class="sxs-lookup"><span data-stu-id="20b38-111">Complete</span></span>](#complete) | <span data-ttu-id="20b38-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="20b38-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="20b38-113">Member</span><span class="sxs-lookup"><span data-stu-id="20b38-113">Members</span></span>

#### <span data-ttu-id="20b38-114">Complete</span><span class="sxs-lookup"><span data-stu-id="20b38-114">Complete</span></span> 

<span data-ttu-id="20b38-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="20b38-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="20b38-116">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="20b38-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="20b38-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20b38-117">Complete should only be called once for each deferral taken.</span></span>

