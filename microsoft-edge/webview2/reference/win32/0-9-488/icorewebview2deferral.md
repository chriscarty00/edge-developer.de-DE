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
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653984"
---
# <span data-ttu-id="922a4-104">Schnittstellen ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="922a4-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="922a4-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="922a4-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="922a4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="922a4-106">Summary</span></span>

 <span data-ttu-id="922a4-107">Member</span><span class="sxs-lookup"><span data-stu-id="922a4-107">Members</span></span>                        | <span data-ttu-id="922a4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="922a4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="922a4-109">Complete</span><span class="sxs-lookup"><span data-stu-id="922a4-109">Complete</span></span>](#complete) | <span data-ttu-id="922a4-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="922a4-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="922a4-111">Member</span><span class="sxs-lookup"><span data-stu-id="922a4-111">Members</span></span>

#### <span data-ttu-id="922a4-112">Complete</span><span class="sxs-lookup"><span data-stu-id="922a4-112">Complete</span></span> 

<span data-ttu-id="922a4-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="922a4-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="922a4-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="922a4-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="922a4-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="922a4-115">Complete should only be called once for each deferral taken.</span></span>

