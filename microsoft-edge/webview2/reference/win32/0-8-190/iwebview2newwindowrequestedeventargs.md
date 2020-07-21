---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: cbcac385546c44e776ed48b8ae4d3ab754b614e0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885893"
---
# <span data-ttu-id="ef032-104">0.8.355-Interface-IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef032-104">0.8.355 - interface IWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="ef032-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ef032-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="ef032-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef032-106">Summary</span></span>

 <span data-ttu-id="ef032-107">Member</span><span class="sxs-lookup"><span data-stu-id="ef032-107">Members</span></span>                        | <span data-ttu-id="ef032-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef032-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef032-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ef032-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ef032-110">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ef032-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="ef032-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ef032-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="ef032-112">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="ef032-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="ef032-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ef032-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="ef032-114">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="ef032-114">Gets the new window.</span></span>
[<span data-ttu-id="ef032-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="ef032-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="ef032-116">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef032-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="ef032-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="ef032-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="ef032-118">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef032-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="ef032-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef032-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ef032-120">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="ef032-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="ef032-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ef032-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ef032-122">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="ef032-122">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="ef032-123">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (durch Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="ef032-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="ef032-124">Member</span><span class="sxs-lookup"><span data-stu-id="ef032-124">Members</span></span>

#### <span data-ttu-id="ef032-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ef032-125">get_Uri</span></span> 

<span data-ttu-id="ef032-126">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ef032-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="ef032-127">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="ef032-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ef032-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ef032-128">put_NewWindow</span></span> 

<span data-ttu-id="ef032-129">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="ef032-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="ef032-130">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="ef032-130">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="ef032-131">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef032-131">The target webview should not be navigated.</span></span> <span data-ttu-id="ef032-132">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef032-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="ef032-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="ef032-133">get_NewWindow</span></span> 

<span data-ttu-id="ef032-134">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="ef032-134">Gets the new window.</span></span>

> <span data-ttu-id="ef032-135">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="ef032-135">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="ef032-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="ef032-136">put_Handled</span></span> 

<span data-ttu-id="ef032-137">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef032-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="ef032-138">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="ef032-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="ef032-139">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef032-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="ef032-140">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="ef032-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="ef032-141">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="ef032-141">Default is false.</span></span>

#### <span data-ttu-id="ef032-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="ef032-142">get_Handled</span></span> 

<span data-ttu-id="ef032-143">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef032-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="ef032-144">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="ef032-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="ef032-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef032-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="ef032-146">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="ef032-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="ef032-147">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ef032-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="ef032-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ef032-148">GetDeferral</span></span> 

<span data-ttu-id="ef032-149">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="ef032-149">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="ef032-150">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="ef032-150">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="ef032-151">Sie können das [IWebView2Deferral](IWebView2Deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ef032-151">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="ef032-152">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="ef032-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

