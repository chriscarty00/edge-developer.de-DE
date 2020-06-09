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
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698935"
---
# <span data-ttu-id="b3f51-104">Schnittstellen ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="b3f51-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="b3f51-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="b3f51-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="b3f51-106">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="b3f51-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="b3f51-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b3f51-107">Summary</span></span>

 <span data-ttu-id="b3f51-108">Member</span><span class="sxs-lookup"><span data-stu-id="b3f51-108">Members</span></span>                        | <span data-ttu-id="b3f51-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b3f51-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3f51-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="b3f51-110">get_Height</span></span>](#get_height) | <span data-ttu-id="b3f51-111">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-111">The height of the window.</span></span>
[<span data-ttu-id="b3f51-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="b3f51-112">get_Left</span></span>](#get_left) | <span data-ttu-id="b3f51-113">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-113">The left position of the window.</span></span> <span data-ttu-id="b3f51-114">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="b3f51-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="b3f51-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="b3f51-116">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="b3f51-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="b3f51-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="b3f51-118">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3f51-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="b3f51-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="b3f51-119">get_Status</span></span>](#get_status) | <span data-ttu-id="b3f51-120">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="b3f51-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="b3f51-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="b3f51-122">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="b3f51-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="b3f51-123">get_Top</span></span>](#get_top) | <span data-ttu-id="b3f51-124">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-124">The top position of the window.</span></span> <span data-ttu-id="b3f51-125">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="b3f51-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="b3f51-126">get_Width</span></span>](#get_width) | <span data-ttu-id="b3f51-127">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-127">The width of the window.</span></span>
[<span data-ttu-id="b3f51-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="b3f51-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="b3f51-129">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="b3f51-129">Has specified left and top values.</span></span>
[<span data-ttu-id="b3f51-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="b3f51-130">HasSize</span></span>](#hassize) | <span data-ttu-id="b3f51-131">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="b3f51-131">Has specified height and width values.</span></span>

<span data-ttu-id="b3f51-132">Diese Felder entsprechen dem "windowFeatures", das an Window. Open übergeben wurde, wie in[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="b3f51-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="b3f51-133">Member</span><span class="sxs-lookup"><span data-stu-id="b3f51-133">Members</span></span>

#### <span data-ttu-id="b3f51-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="b3f51-134">get_Height</span></span> 

<span data-ttu-id="b3f51-135">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-135">The height of the window.</span></span>

> <span data-ttu-id="b3f51-136">öffentliche HRESULT- [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="b3f51-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="b3f51-137">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="b3f51-137">Minimum value is 100.</span></span> <span data-ttu-id="b3f51-138">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="b3f51-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="b3f51-139">get_Left</span></span> 

<span data-ttu-id="b3f51-140">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-140">The left position of the window.</span></span> <span data-ttu-id="b3f51-141">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="b3f51-142">öffentliche HRESULT- [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="b3f51-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="b3f51-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="b3f51-143">get_MenuBar</span></span> 

<span data-ttu-id="b3f51-144">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="b3f51-145">öffentliche HRESULT- [get_MenuBar](#get_menubar)(bool \* Menüleiste)</span><span class="sxs-lookup"><span data-stu-id="b3f51-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="b3f51-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="b3f51-146">get_ScrollBars</span></span> 

<span data-ttu-id="b3f51-147">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3f51-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="b3f51-148">öffentliche HRESULT- [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="b3f51-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="b3f51-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="b3f51-149">get_Status</span></span> 

<span data-ttu-id="b3f51-150">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="b3f51-151">Public HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="b3f51-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="b3f51-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="b3f51-152">get_Toolbar</span></span> 

<span data-ttu-id="b3f51-153">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3f51-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="b3f51-154">öffentliche HRESULT- [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="b3f51-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="b3f51-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="b3f51-155">get_Top</span></span> 

<span data-ttu-id="b3f51-156">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-156">The top position of the window.</span></span> <span data-ttu-id="b3f51-157">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="b3f51-158">Public HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="b3f51-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="b3f51-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="b3f51-159">get_Width</span></span> 

<span data-ttu-id="b3f51-160">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="b3f51-160">The width of the window.</span></span>

> <span data-ttu-id="b3f51-161">öffentliche HRESULT- [get_Width](#get_width)(UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="b3f51-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="b3f51-162">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="b3f51-162">Minimum value is 100.</span></span> <span data-ttu-id="b3f51-163">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="b3f51-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="b3f51-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="b3f51-164">HasPosition</span></span> 

<span data-ttu-id="b3f51-165">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="b3f51-165">Has specified left and top values.</span></span>

> <span data-ttu-id="b3f51-166">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="b3f51-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="b3f51-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="b3f51-167">HasSize</span></span> 

<span data-ttu-id="b3f51-168">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="b3f51-168">Has specified height and width values.</span></span>

> <span data-ttu-id="b3f51-169">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="b3f51-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

