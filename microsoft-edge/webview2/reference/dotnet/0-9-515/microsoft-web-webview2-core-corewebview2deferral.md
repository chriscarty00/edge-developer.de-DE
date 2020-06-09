---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bf198781d67761e9d6c29ee9c6a274462e92a61d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697672"
---
# <span data-ttu-id="cdc4a-104">Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="cdc4a-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="cdc4a-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cdc4a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cdc4a-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc4a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="cdc4a-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cdc4a-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cdc4a-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cdc4a-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cdc4a-109">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cdc4a-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="cdc4a-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cdc4a-110">Summary</span></span>

 <span data-ttu-id="cdc4a-111">Member</span><span class="sxs-lookup"><span data-stu-id="cdc4a-111">Members</span></span>                        | <span data-ttu-id="cdc4a-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cdc4a-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cdc4a-113">Complete</span><span class="sxs-lookup"><span data-stu-id="cdc4a-113">Complete</span></span>](#complete) | <span data-ttu-id="cdc4a-114">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="cdc4a-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="cdc4a-115">Member</span><span class="sxs-lookup"><span data-stu-id="cdc4a-115">Members</span></span>

#### <span data-ttu-id="cdc4a-116">Complete</span><span class="sxs-lookup"><span data-stu-id="cdc4a-116">Complete</span></span> 

<span data-ttu-id="cdc4a-117">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="cdc4a-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="cdc4a-118">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="cdc4a-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="cdc4a-119">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cdc4a-119">Complete should only be called once for each deferral taken.</span></span>

