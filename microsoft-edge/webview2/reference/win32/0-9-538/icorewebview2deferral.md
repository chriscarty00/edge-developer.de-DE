---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698828"
---
# <span data-ttu-id="4c777-104">Schnittstellen ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="4c777-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="4c777-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4c777-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="4c777-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4c777-106">Summary</span></span>

 <span data-ttu-id="4c777-107">Member</span><span class="sxs-lookup"><span data-stu-id="4c777-107">Members</span></span>                        | <span data-ttu-id="4c777-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4c777-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c777-109">Complete</span><span class="sxs-lookup"><span data-stu-id="4c777-109">Complete</span></span>](#complete) | <span data-ttu-id="4c777-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4c777-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="4c777-111">Member</span><span class="sxs-lookup"><span data-stu-id="4c777-111">Members</span></span>

#### <span data-ttu-id="4c777-112">Complete</span><span class="sxs-lookup"><span data-stu-id="4c777-112">Complete</span></span> 

<span data-ttu-id="4c777-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4c777-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="4c777-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="4c777-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="4c777-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4c777-115">Complete should only be called once for each deferral taken.</span></span>

