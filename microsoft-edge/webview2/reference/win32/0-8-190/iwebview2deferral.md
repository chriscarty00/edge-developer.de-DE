---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: a1c00c29a3e063cd995c9f0eb287d870fd1211dc
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886145"
---
# <span data-ttu-id="38750-104">0.8.355-Interface-IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="38750-104">0.8.355 - interface IWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="38750-105">Diese Schnittstelle wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="38750-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="38750-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="38750-106">Summary</span></span>

 <span data-ttu-id="38750-107">Member</span><span class="sxs-lookup"><span data-stu-id="38750-107">Members</span></span>                        | <span data-ttu-id="38750-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="38750-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38750-109">Complete</span><span class="sxs-lookup"><span data-stu-id="38750-109">Complete</span></span>](#complete) | <span data-ttu-id="38750-110">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="38750-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="38750-111">Member</span><span class="sxs-lookup"><span data-stu-id="38750-111">Members</span></span>

#### <span data-ttu-id="38750-112">Complete</span><span class="sxs-lookup"><span data-stu-id="38750-112">Complete</span></span> 

<span data-ttu-id="38750-113">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="38750-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="38750-114">Public HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="38750-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="38750-115">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="38750-115">Complete should only be called once for each deferral taken.</span></span>

