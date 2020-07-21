---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b30b6e35388ab01433b2c879db82d9c4136fae99
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885424"
---
# <span data-ttu-id="8e80a-104">0.9.515-Interface-ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="8e80a-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="8e80a-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8e80a-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="8e80a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8e80a-106">Summary</span></span>

 <span data-ttu-id="8e80a-107">Member</span><span class="sxs-lookup"><span data-stu-id="8e80a-107">Members</span></span>                        | <span data-ttu-id="8e80a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8e80a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e80a-109">Complete</span><span class="sxs-lookup"><span data-stu-id="8e80a-109">Complete</span></span>](#complete) | <span data-ttu-id="8e80a-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8e80a-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="8e80a-111">Member</span><span class="sxs-lookup"><span data-stu-id="8e80a-111">Members</span></span>

#### <span data-ttu-id="8e80a-112">Complete</span><span class="sxs-lookup"><span data-stu-id="8e80a-112">Complete</span></span> 

<span data-ttu-id="8e80a-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8e80a-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="8e80a-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="8e80a-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="8e80a-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e80a-115">Complete should only be called once for each deferral taken.</span></span>

