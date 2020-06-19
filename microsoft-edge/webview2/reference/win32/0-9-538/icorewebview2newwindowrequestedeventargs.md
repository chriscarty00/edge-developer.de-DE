---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 03c943c87f07344ab4e3d1a7c707a993a795cdba
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751849"
---
# <span data-ttu-id="17316-104">Schnittstellen ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="17316-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="17316-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="17316-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="17316-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="17316-106">Summary</span></span>

 <span data-ttu-id="17316-107">Member</span><span class="sxs-lookup"><span data-stu-id="17316-107">Members</span></span>                        | <span data-ttu-id="17316-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="17316-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17316-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="17316-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="17316-110">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17316-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="17316-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="17316-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="17316-112">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="17316-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="17316-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="17316-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="17316-114">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="17316-114">Gets the new window.</span></span>
[<span data-ttu-id="17316-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="17316-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="17316-116">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="17316-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="17316-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="17316-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="17316-118">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="17316-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="17316-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="17316-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="17316-120">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17316-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="17316-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="17316-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="17316-122">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="17316-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="17316-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="17316-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="17316-124">Member</span><span class="sxs-lookup"><span data-stu-id="17316-124">Members</span></span>

#### <span data-ttu-id="17316-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="17316-125">get_Handled</span></span> 

<span data-ttu-id="17316-126">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17316-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="17316-127">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="17316-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="17316-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="17316-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="17316-129">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="17316-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="17316-130">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="17316-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="17316-131">WebView2-Steuerelemente können Popupfenster anzeigen, da der Popupblocker deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="17316-131">WebView2 controls may display pop-up windows because the Pop-Up blocker is turned off.</span></span> <span data-ttu-id="17316-132">Wenn Sie verhindern möchten, dass nicht vom Benutzer initiierte Popup-Fenster angezeigt werden, verwenden Sie `get_IsUserInitiated` .</span><span class="sxs-lookup"><span data-stu-id="17316-132">To block non-user initiated pop-up windows from being displayed, use `get_IsUserInitiated`.</span></span>

#### <span data-ttu-id="17316-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="17316-133">get_NewWindow</span></span> 

<span data-ttu-id="17316-134">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="17316-134">Gets the new window.</span></span>

> <span data-ttu-id="17316-135">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="17316-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="17316-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="17316-136">get_Uri</span></span> 

<span data-ttu-id="17316-137">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="17316-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="17316-138">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="17316-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="17316-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="17316-139">GetDeferral</span></span> 

<span data-ttu-id="17316-140">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="17316-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="17316-141">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="17316-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="17316-142">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="17316-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="17316-143">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="17316-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="17316-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="17316-144">put_Handled</span></span> 

<span data-ttu-id="17316-145">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17316-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="17316-146">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="17316-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="17316-147">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17316-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="17316-148">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="17316-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="17316-149">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="17316-149">Default is false.</span></span>

#### <span data-ttu-id="17316-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="17316-150">put_NewWindow</span></span> 

<span data-ttu-id="17316-151">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="17316-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="17316-152">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="17316-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="17316-153">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="17316-153">The target webview should not be navigated.</span></span> <span data-ttu-id="17316-154">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17316-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>
