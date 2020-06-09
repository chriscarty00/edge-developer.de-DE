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
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698777"
---
# <span data-ttu-id="9b060-104">Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="9b060-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="9b060-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9b060-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9b060-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="9b060-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9b060-107">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9b060-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="9b060-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9b060-108">Summary</span></span>

 <span data-ttu-id="9b060-109">Member</span><span class="sxs-lookup"><span data-stu-id="9b060-109">Members</span></span>                        | <span data-ttu-id="9b060-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9b060-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b060-111">Handled</span><span class="sxs-lookup"><span data-stu-id="9b060-111">Handled</span></span>](#handled) | <span data-ttu-id="9b060-112">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9b060-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="9b060-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9b060-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="9b060-114">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="9b060-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="9b060-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="9b060-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="9b060-116">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="9b060-116">Gets the new window.</span></span>
[<span data-ttu-id="9b060-117">URI</span><span class="sxs-lookup"><span data-stu-id="9b060-117">Uri</span></span>](#uri) | <span data-ttu-id="9b060-118">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="9b060-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="9b060-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="9b060-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="9b060-120">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b060-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="9b060-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9b060-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9b060-122">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9b060-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="9b060-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="9b060-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="9b060-124">Member</span><span class="sxs-lookup"><span data-stu-id="9b060-124">Members</span></span>

#### <span data-ttu-id="9b060-125">Handled</span><span class="sxs-lookup"><span data-stu-id="9b060-125">Handled</span></span> 

<span data-ttu-id="9b060-126">Gibt an, ob der NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9b060-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="9b060-127">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="9b060-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="9b060-128">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b060-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="9b060-129">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="9b060-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="9b060-130">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="9b060-130">Default is false.</span></span>

#### <span data-ttu-id="9b060-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9b060-131">IsUserInitiated</span></span> 

<span data-ttu-id="9b060-132">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="9b060-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="9b060-133">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="9b060-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="9b060-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="9b060-134">NewWindow</span></span> 

<span data-ttu-id="9b060-135">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="9b060-135">Gets the new window.</span></span>

> <span data-ttu-id="9b060-136">öffentliches CoreWebView2- [Fenster](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="9b060-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="9b060-137">URI</span><span class="sxs-lookup"><span data-stu-id="9b060-137">Uri</span></span> 

<span data-ttu-id="9b060-138">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="9b060-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="9b060-139">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="9b060-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="9b060-140">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b060-140">The target webview should not be navigated.</span></span> <span data-ttu-id="9b060-141">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b060-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="9b060-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="9b060-142">WindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="9b060-143">Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b060-143">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="9b060-144">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b060-144">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="9b060-145">öffentliche CoreWebView2WindowFeatures- [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="9b060-145">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="9b060-146">Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b060-146">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="9b060-147">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9b060-147">GetDeferral</span></span> 

<span data-ttu-id="9b060-148">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9b060-148">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9b060-149">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="9b060-149">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="9b060-150">Sie können das CoreWebView2Deferral-Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9b060-150">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="9b060-151">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="9b060-151">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

