---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Deferral
ms.openlocfilehash: 533aefe8b14ae3cabfddd32cb588014067bfdd42
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010285"
---
# <span data-ttu-id="1b9ac-104">0.9.579-Interface-ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="1b9ac-104">0.9.579 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="1b9ac-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1b9ac-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="1b9ac-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1b9ac-106">Summary</span></span>

 <span data-ttu-id="1b9ac-107">Member</span><span class="sxs-lookup"><span data-stu-id="1b9ac-107">Members</span></span>                        | <span data-ttu-id="1b9ac-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1b9ac-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b9ac-109">Complete</span><span class="sxs-lookup"><span data-stu-id="1b9ac-109">Complete</span></span>](#complete) | <span data-ttu-id="1b9ac-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="1b9ac-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="1b9ac-111">Member</span><span class="sxs-lookup"><span data-stu-id="1b9ac-111">Members</span></span>

#### <span data-ttu-id="1b9ac-112">Complete</span><span class="sxs-lookup"><span data-stu-id="1b9ac-112">Complete</span></span> 

<span data-ttu-id="1b9ac-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="1b9ac-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="1b9ac-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="1b9ac-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="1b9ac-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1b9ac-115">Complete should only be called once for each deferral taken.</span></span>

