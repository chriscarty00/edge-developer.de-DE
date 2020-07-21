---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 135289994bdfe5481018c479b7a1d9c372ecb256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885109"
---
# <span data-ttu-id="0820b-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="0820b-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="0820b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0820b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0820b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0820b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0820b-107">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0820b-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="0820b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0820b-108">Summary</span></span>

 <span data-ttu-id="0820b-109">Member</span><span class="sxs-lookup"><span data-stu-id="0820b-109">Members</span></span>                        | <span data-ttu-id="0820b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0820b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0820b-111">Complete</span><span class="sxs-lookup"><span data-stu-id="0820b-111">Complete</span></span>](#complete) | <span data-ttu-id="0820b-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="0820b-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="0820b-113">Member</span><span class="sxs-lookup"><span data-stu-id="0820b-113">Members</span></span>

#### <span data-ttu-id="0820b-114">Complete</span><span class="sxs-lookup"><span data-stu-id="0820b-114">Complete</span></span> 

<span data-ttu-id="0820b-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="0820b-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="0820b-116">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="0820b-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="0820b-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0820b-117">Complete should only be called once for each deferral taken.</span></span>

