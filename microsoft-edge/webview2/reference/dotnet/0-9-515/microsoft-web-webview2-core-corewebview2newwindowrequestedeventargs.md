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
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654084"
---
# <span data-ttu-id="414d3-104">Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="414d3-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="414d3-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="414d3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="414d3-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="414d3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="414d3-107">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="414d3-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="414d3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="414d3-108">Summary</span></span>

 <span data-ttu-id="414d3-109">Member</span><span class="sxs-lookup"><span data-stu-id="414d3-109">Members</span></span>                        | <span data-ttu-id="414d3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="414d3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="414d3-111">Handled</span><span class="sxs-lookup"><span data-stu-id="414d3-111">Handled</span></span>](#handled) | <span data-ttu-id="414d3-112">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="414d3-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="414d3-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="414d3-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="414d3-114">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="414d3-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="414d3-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="414d3-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="414d3-116">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="414d3-116">Gets the new window.</span></span>
[<span data-ttu-id="414d3-117">URI</span><span class="sxs-lookup"><span data-stu-id="414d3-117">Uri</span></span>](#uri) | <span data-ttu-id="414d3-118">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="414d3-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="414d3-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="414d3-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="414d3-120">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="414d3-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="414d3-121">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="414d3-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="414d3-122">Member</span><span class="sxs-lookup"><span data-stu-id="414d3-122">Members</span></span>

#### <span data-ttu-id="414d3-123">Handled</span><span class="sxs-lookup"><span data-stu-id="414d3-123">Handled</span></span> 

<span data-ttu-id="414d3-124">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="414d3-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="414d3-125">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="414d3-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="414d3-126">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="414d3-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="414d3-127">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="414d3-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="414d3-128">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="414d3-128">Default is false.</span></span>

#### <span data-ttu-id="414d3-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="414d3-129">IsUserInitiated</span></span> 

<span data-ttu-id="414d3-130">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="414d3-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="414d3-131">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="414d3-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="414d3-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="414d3-132">NewWindow</span></span> 

<span data-ttu-id="414d3-133">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="414d3-133">Gets the new window.</span></span>

> <span data-ttu-id="414d3-134">öffentliches CoreWebView2- [Fenster](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="414d3-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="414d3-135">URI</span><span class="sxs-lookup"><span data-stu-id="414d3-135">Uri</span></span> 

<span data-ttu-id="414d3-136">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="414d3-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="414d3-137">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="414d3-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="414d3-138">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="414d3-138">The target webview should not be navigated.</span></span> <span data-ttu-id="414d3-139">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="414d3-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="414d3-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="414d3-140">GetDeferral</span></span> 

<span data-ttu-id="414d3-141">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="414d3-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="414d3-142">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="414d3-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="414d3-143">Sie können das CoreWebView2Deferral-Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="414d3-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="414d3-144">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="414d3-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

