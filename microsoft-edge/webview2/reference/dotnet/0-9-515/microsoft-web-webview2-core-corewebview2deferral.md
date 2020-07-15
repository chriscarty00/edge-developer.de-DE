---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4df74c4a645b6bfa17228860f627910d374e19c4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878722"
---
# <span data-ttu-id="74d8f-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="74d8f-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="74d8f-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="74d8f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="74d8f-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="74d8f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="74d8f-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="74d8f-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="74d8f-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="74d8f-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="74d8f-109">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="74d8f-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="74d8f-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="74d8f-110">Summary</span></span>

 <span data-ttu-id="74d8f-111">Member</span><span class="sxs-lookup"><span data-stu-id="74d8f-111">Members</span></span>                        | <span data-ttu-id="74d8f-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="74d8f-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74d8f-113">Complete</span><span class="sxs-lookup"><span data-stu-id="74d8f-113">Complete</span></span>](#complete) | <span data-ttu-id="74d8f-114">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="74d8f-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="74d8f-115">Member</span><span class="sxs-lookup"><span data-stu-id="74d8f-115">Members</span></span>

#### <span data-ttu-id="74d8f-116">Complete</span><span class="sxs-lookup"><span data-stu-id="74d8f-116">Complete</span></span> 

<span data-ttu-id="74d8f-117">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="74d8f-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="74d8f-118">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="74d8f-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="74d8f-119">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="74d8f-119">Complete should only be called once for each deferral taken.</span></span>

