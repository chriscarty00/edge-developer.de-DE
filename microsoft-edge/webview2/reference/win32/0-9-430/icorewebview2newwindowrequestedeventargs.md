---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 73f62e7130d50028b527353c6ba1a238f694dcda
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885681"
---
# <span data-ttu-id="e76c3-104">0.9.430-Interface-ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e76c3-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="e76c3-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e76c3-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="e76c3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e76c3-106">Summary</span></span>

 <span data-ttu-id="e76c3-107">Member</span><span class="sxs-lookup"><span data-stu-id="e76c3-107">Members</span></span>                        | <span data-ttu-id="e76c3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e76c3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e76c3-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e76c3-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e76c3-110">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e76c3-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="e76c3-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e76c3-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="e76c3-112">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="e76c3-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="e76c3-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e76c3-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="e76c3-114">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="e76c3-114">Gets the new window.</span></span>
[<span data-ttu-id="e76c3-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="e76c3-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="e76c3-116">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e76c3-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="e76c3-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="e76c3-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="e76c3-118">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e76c3-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="e76c3-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e76c3-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="e76c3-120">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="e76c3-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="e76c3-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e76c3-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e76c3-122">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e76c3-122">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="e76c3-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (durch Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="e76c3-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="e76c3-124">Member</span><span class="sxs-lookup"><span data-stu-id="e76c3-124">Members</span></span>

#### <span data-ttu-id="e76c3-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e76c3-125">get_Uri</span></span> 

<span data-ttu-id="e76c3-126">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e76c3-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="e76c3-127">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="e76c3-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e76c3-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e76c3-128">put_NewWindow</span></span> 

<span data-ttu-id="e76c3-129">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="e76c3-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="e76c3-130">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="e76c3-130">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="e76c3-131">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="e76c3-131">The target webview should not be navigated.</span></span> <span data-ttu-id="e76c3-132">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e76c3-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="e76c3-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e76c3-133">get_NewWindow</span></span> 

<span data-ttu-id="e76c3-134">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="e76c3-134">Gets the new window.</span></span>

> <span data-ttu-id="e76c3-135">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="e76c3-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="e76c3-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="e76c3-136">put_Handled</span></span> 

<span data-ttu-id="e76c3-137">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e76c3-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="e76c3-138">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="e76c3-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="e76c3-139">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e76c3-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="e76c3-140">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="e76c3-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="e76c3-141">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="e76c3-141">Default is false.</span></span>

#### <span data-ttu-id="e76c3-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="e76c3-142">get_Handled</span></span> 

<span data-ttu-id="e76c3-143">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e76c3-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="e76c3-144">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="e76c3-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="e76c3-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e76c3-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="e76c3-146">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="e76c3-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="e76c3-147">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="e76c3-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="e76c3-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e76c3-148">GetDeferral</span></span> 

<span data-ttu-id="e76c3-149">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e76c3-149">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="e76c3-150">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="e76c3-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="e76c3-151">Sie können das [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e76c3-151">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="e76c3-152">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="e76c3-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

