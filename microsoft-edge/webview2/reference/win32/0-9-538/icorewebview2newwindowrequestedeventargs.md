---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: bb18b6662fd5921406e19b3c333c97f8a1cd0dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879436"
---
# <span data-ttu-id="900a3-104">Schnittstellen ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="900a3-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="900a3-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="900a3-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="900a3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="900a3-106">Summary</span></span>

 <span data-ttu-id="900a3-107">Member</span><span class="sxs-lookup"><span data-stu-id="900a3-107">Members</span></span>                        | <span data-ttu-id="900a3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="900a3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="900a3-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="900a3-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="900a3-110">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="900a3-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="900a3-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="900a3-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="900a3-112">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="900a3-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="900a3-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="900a3-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="900a3-114">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="900a3-114">Gets the new window.</span></span>
[<span data-ttu-id="900a3-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="900a3-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="900a3-116">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="900a3-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="900a3-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="900a3-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="900a3-118">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="900a3-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="900a3-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="900a3-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="900a3-120">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="900a3-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="900a3-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="900a3-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="900a3-122">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="900a3-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="900a3-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="900a3-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="900a3-124">Member</span><span class="sxs-lookup"><span data-stu-id="900a3-124">Members</span></span>

#### <span data-ttu-id="900a3-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="900a3-125">get_Handled</span></span> 

<span data-ttu-id="900a3-126">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="900a3-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="900a3-127">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="900a3-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="900a3-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="900a3-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="900a3-129">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="900a3-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="900a3-130">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="900a3-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="900a3-131">Der Edge-Popupblocker ist für WebView deaktiviert, damit die APP dieses Flag verwenden kann, um nicht vom Benutzer initiierte Popups zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="900a3-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="900a3-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="900a3-132">get_NewWindow</span></span> 

<span data-ttu-id="900a3-133">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="900a3-133">Gets the new window.</span></span>

> <span data-ttu-id="900a3-134">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="900a3-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="900a3-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="900a3-135">get_Uri</span></span> 

<span data-ttu-id="900a3-136">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="900a3-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="900a3-137">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="900a3-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="900a3-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="900a3-138">GetDeferral</span></span> 

<span data-ttu-id="900a3-139">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="900a3-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="900a3-140">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="900a3-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="900a3-141">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="900a3-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="900a3-142">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="900a3-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="900a3-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="900a3-143">put_Handled</span></span> 

<span data-ttu-id="900a3-144">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="900a3-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="900a3-145">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="900a3-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="900a3-146">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="900a3-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="900a3-147">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="900a3-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="900a3-148">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="900a3-148">Default is false.</span></span>

#### <span data-ttu-id="900a3-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="900a3-149">put_NewWindow</span></span> 

<span data-ttu-id="900a3-150">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="900a3-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="900a3-151">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="900a3-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="900a3-152">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="900a3-152">The target webview should not be navigated.</span></span> <span data-ttu-id="900a3-153">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="900a3-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

