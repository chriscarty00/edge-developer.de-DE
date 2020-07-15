---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880122"
---
# <span data-ttu-id="d5f89-104">Schnittstellen ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="d5f89-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="d5f89-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d5f89-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="d5f89-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d5f89-106">Summary</span></span>

 <span data-ttu-id="d5f89-107">Member</span><span class="sxs-lookup"><span data-stu-id="d5f89-107">Members</span></span>                        | <span data-ttu-id="d5f89-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d5f89-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d5f89-109">Complete</span><span class="sxs-lookup"><span data-stu-id="d5f89-109">Complete</span></span>](#complete) | <span data-ttu-id="d5f89-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="d5f89-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="d5f89-111">Member</span><span class="sxs-lookup"><span data-stu-id="d5f89-111">Members</span></span>

#### <span data-ttu-id="d5f89-112">Complete</span><span class="sxs-lookup"><span data-stu-id="d5f89-112">Complete</span></span> 

<span data-ttu-id="d5f89-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="d5f89-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="d5f89-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="d5f89-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="d5f89-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5f89-115">Complete should only be called once for each deferral taken.</span></span>

