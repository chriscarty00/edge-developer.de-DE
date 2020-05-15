---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e1917a4383e6e5d8aaf79464c4607d8f2d4f0cdc
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653746"
---
# <span data-ttu-id="cd9a9-104">Schnittstellen IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cd9a9-104">interface IWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="cd9a9-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="cd9a9-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cd9a9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="cd9a9-107">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="cd9a9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cd9a9-108">Summary</span></span>

 <span data-ttu-id="cd9a9-109">Member</span><span class="sxs-lookup"><span data-stu-id="cd9a9-109">Members</span></span>                        | <span data-ttu-id="cd9a9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd9a9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd9a9-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cd9a9-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="cd9a9-112">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="cd9a9-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cd9a9-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="cd9a9-114">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="cd9a9-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cd9a9-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="cd9a9-116">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-116">Gets the new window.</span></span>
[<span data-ttu-id="cd9a9-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="cd9a9-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="cd9a9-118">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="cd9a9-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="cd9a9-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="cd9a9-120">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="cd9a9-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cd9a9-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="cd9a9-122">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="cd9a9-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cd9a9-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cd9a9-124">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-124">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="cd9a9-125">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (durch Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="cd9a9-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="cd9a9-126">Member</span><span class="sxs-lookup"><span data-stu-id="cd9a9-126">Members</span></span>

#### <span data-ttu-id="cd9a9-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cd9a9-127">get_Uri</span></span> 

<span data-ttu-id="cd9a9-128">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="cd9a9-129">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="cd9a9-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cd9a9-130">put_NewWindow</span></span> 

<span data-ttu-id="cd9a9-131">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="cd9a9-132">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-132">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="cd9a9-133">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-133">The target webview should not be navigated.</span></span> <span data-ttu-id="cd9a9-134">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="cd9a9-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cd9a9-135">get_NewWindow</span></span> 

<span data-ttu-id="cd9a9-136">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-136">Gets the new window.</span></span>

> <span data-ttu-id="cd9a9-137">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-137">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="cd9a9-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="cd9a9-138">put_Handled</span></span> 

<span data-ttu-id="cd9a9-139">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="cd9a9-140">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="cd9a9-141">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="cd9a9-142">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="cd9a9-143">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-143">Default is false.</span></span>

#### <span data-ttu-id="cd9a9-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="cd9a9-144">get_Handled</span></span> 

<span data-ttu-id="cd9a9-145">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="cd9a9-146">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="cd9a9-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cd9a9-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="cd9a9-148">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="cd9a9-149">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="cd9a9-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cd9a9-150">GetDeferral</span></span> 

<span data-ttu-id="cd9a9-151">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-151">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="cd9a9-152">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="cd9a9-152">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="cd9a9-153">Sie können das [IWebView2Deferral](IWebView2Deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-153">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="cd9a9-154">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="cd9a9-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

