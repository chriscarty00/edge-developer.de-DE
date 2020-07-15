---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: aeefa0257a273f0eecd99d3f666adc03be709d9a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880493"
---
# <span data-ttu-id="c318e-104">0.9.515-Interface-ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c318e-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c318e-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="c318e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c318e-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c318e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c318e-107">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c318e-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="c318e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c318e-108">Summary</span></span>

 <span data-ttu-id="c318e-109">Member</span><span class="sxs-lookup"><span data-stu-id="c318e-109">Members</span></span>                        | <span data-ttu-id="c318e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c318e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c318e-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c318e-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="c318e-112">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c318e-112">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c318e-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c318e-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="c318e-114">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="c318e-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="c318e-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c318e-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="c318e-116">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="c318e-116">Gets the new window.</span></span>
[<span data-ttu-id="c318e-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c318e-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="c318e-118">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c318e-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="c318e-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c318e-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c318e-120">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c318e-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="c318e-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c318e-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="c318e-122">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c318e-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c318e-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c318e-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="c318e-124">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="c318e-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="c318e-125">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="c318e-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="c318e-126">Member</span><span class="sxs-lookup"><span data-stu-id="c318e-126">Members</span></span>

#### <span data-ttu-id="c318e-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c318e-127">get_Handled</span></span> 

<span data-ttu-id="c318e-128">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c318e-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c318e-129">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="c318e-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="c318e-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c318e-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="c318e-131">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="c318e-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="c318e-132">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="c318e-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="c318e-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c318e-133">get_NewWindow</span></span> 

<span data-ttu-id="c318e-134">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="c318e-134">Gets the new window.</span></span>

> <span data-ttu-id="c318e-135">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="c318e-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="c318e-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c318e-136">get_Uri</span></span> 

<span data-ttu-id="c318e-137">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c318e-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="c318e-138">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="c318e-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="c318e-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c318e-139">GetDeferral</span></span> 

<span data-ttu-id="c318e-140">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c318e-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c318e-141">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="c318e-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c318e-142">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c318e-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="c318e-143">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="c318e-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="c318e-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c318e-144">put_Handled</span></span> 

<span data-ttu-id="c318e-145">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="c318e-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c318e-146">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="c318e-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="c318e-147">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c318e-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="c318e-148">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="c318e-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="c318e-149">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="c318e-149">Default is false.</span></span>

#### <span data-ttu-id="c318e-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c318e-150">put_NewWindow</span></span> 

<span data-ttu-id="c318e-151">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="c318e-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="c318e-152">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="c318e-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="c318e-153">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="c318e-153">The target webview should not be navigated.</span></span> <span data-ttu-id="c318e-154">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c318e-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

