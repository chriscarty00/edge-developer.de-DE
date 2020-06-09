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
ms.openlocfilehash: c3f9b8bb9451d8364424db01ea19aecedb362d59
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697168"
---
# <span data-ttu-id="e8500-104">Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="e8500-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e8500-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e8500-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e8500-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e8500-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e8500-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e8500-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e8500-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="e8500-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e8500-109">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e8500-109">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="e8500-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e8500-110">Summary</span></span>

 <span data-ttu-id="e8500-111">Member</span><span class="sxs-lookup"><span data-stu-id="e8500-111">Members</span></span>                        | <span data-ttu-id="e8500-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e8500-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8500-113">Handled</span><span class="sxs-lookup"><span data-stu-id="e8500-113">Handled</span></span>](#handled) | <span data-ttu-id="e8500-114">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e8500-114">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="e8500-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e8500-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="e8500-116">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="e8500-116">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="e8500-117">NewWindow</span><span class="sxs-lookup"><span data-stu-id="e8500-117">NewWindow</span></span>](#newwindow) | <span data-ttu-id="e8500-118">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="e8500-118">Gets the new window.</span></span>
[<span data-ttu-id="e8500-119">URI</span><span class="sxs-lookup"><span data-stu-id="e8500-119">Uri</span></span>](#uri) | <span data-ttu-id="e8500-120">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e8500-120">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="e8500-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e8500-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e8500-122">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e8500-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="e8500-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="e8500-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="e8500-124">Member</span><span class="sxs-lookup"><span data-stu-id="e8500-124">Members</span></span>

#### <span data-ttu-id="e8500-125">Handled</span><span class="sxs-lookup"><span data-stu-id="e8500-125">Handled</span></span> 

<span data-ttu-id="e8500-126">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e8500-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="e8500-127">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="e8500-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="e8500-128">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8500-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="e8500-129">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="e8500-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="e8500-130">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="e8500-130">Default is false.</span></span>

#### <span data-ttu-id="e8500-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e8500-131">IsUserInitiated</span></span> 

<span data-ttu-id="e8500-132">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="e8500-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="e8500-133">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="e8500-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="e8500-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="e8500-134">NewWindow</span></span> 

<span data-ttu-id="e8500-135">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="e8500-135">Gets the new window.</span></span>

> <span data-ttu-id="e8500-136">öffentliches CoreWebView2- [Fenster](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="e8500-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="e8500-137">URI</span><span class="sxs-lookup"><span data-stu-id="e8500-137">Uri</span></span> 

<span data-ttu-id="e8500-138">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e8500-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="e8500-139">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="e8500-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="e8500-140">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8500-140">The target webview should not be navigated.</span></span> <span data-ttu-id="e8500-141">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8500-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="e8500-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e8500-142">GetDeferral</span></span> 

<span data-ttu-id="e8500-143">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e8500-143">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="e8500-144">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="e8500-144">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="e8500-145">Sie können das CoreWebView2Deferral-Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e8500-145">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="e8500-146">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="e8500-146">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

