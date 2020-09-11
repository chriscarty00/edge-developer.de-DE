---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WindowFeatures
ms.openlocfilehash: 90b5a09a752250dc342e7eefad031c9b5b83d345
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012119"
---
# <span data-ttu-id="a82b3-104">Schnittstellen ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="a82b3-104">interface ICoreWebView2WindowFeatures</span></span> 

```
interface ICoreWebView2WindowFeatures
  : public IUnknown
```

<span data-ttu-id="a82b3-105">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="a82b3-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="a82b3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a82b3-106">Summary</span></span>

 <span data-ttu-id="a82b3-107">Member</span><span class="sxs-lookup"><span data-stu-id="a82b3-107">Members</span></span>                        | <span data-ttu-id="a82b3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a82b3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a82b3-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="a82b3-109">get_Height</span></span>](#get_height) | <span data-ttu-id="a82b3-110">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-110">The height of the window.</span></span>
[<span data-ttu-id="a82b3-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="a82b3-111">get_Left</span></span>](#get_left) | <span data-ttu-id="a82b3-112">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-112">The left position of the window.</span></span> <span data-ttu-id="a82b3-113">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="a82b3-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="a82b3-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="a82b3-115">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="a82b3-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="a82b3-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="a82b3-117">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a82b3-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="a82b3-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="a82b3-118">get_Status</span></span>](#get_status) | <span data-ttu-id="a82b3-119">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="a82b3-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="a82b3-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="a82b3-121">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="a82b3-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="a82b3-122">get_Top</span></span>](#get_top) | <span data-ttu-id="a82b3-123">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-123">The top position of the window.</span></span> <span data-ttu-id="a82b3-124">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="a82b3-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="a82b3-125">get_Width</span></span>](#get_width) | <span data-ttu-id="a82b3-126">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-126">The width of the window.</span></span>
[<span data-ttu-id="a82b3-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="a82b3-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="a82b3-128">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="a82b3-128">Has specified left and top values.</span></span>
[<span data-ttu-id="a82b3-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="a82b3-129">HasSize</span></span>](#hassize) | <span data-ttu-id="a82b3-130">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="a82b3-130">Has specified height and width values.</span></span>

<span data-ttu-id="a82b3-131">Diese Felder entsprechen dem "windowFeatures", das an Window. Open übergeben wurde, wie in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="a82b3-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="a82b3-132">Member</span><span class="sxs-lookup"><span data-stu-id="a82b3-132">Members</span></span>

#### <span data-ttu-id="a82b3-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="a82b3-133">get_Height</span></span> 

<span data-ttu-id="a82b3-134">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-134">The height of the window.</span></span>

> <span data-ttu-id="a82b3-135">öffentliche HRESULT- [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="a82b3-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="a82b3-136">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="a82b3-136">Minimum value is 100.</span></span> <span data-ttu-id="a82b3-137">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="a82b3-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="a82b3-138">get_Left</span></span> 

<span data-ttu-id="a82b3-139">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-139">The left position of the window.</span></span> <span data-ttu-id="a82b3-140">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="a82b3-141">öffentliche HRESULT- [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="a82b3-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="a82b3-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="a82b3-142">get_MenuBar</span></span> 

<span data-ttu-id="a82b3-143">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="a82b3-144">öffentliche HRESULT- [get_MenuBar](#get_menubar)(bool \* Menüleiste)</span><span class="sxs-lookup"><span data-stu-id="a82b3-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="a82b3-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="a82b3-145">get_ScrollBars</span></span> 

<span data-ttu-id="a82b3-146">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a82b3-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="a82b3-147">öffentliche HRESULT- [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="a82b3-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="a82b3-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="a82b3-148">get_Status</span></span> 

<span data-ttu-id="a82b3-149">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="a82b3-150">Public HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="a82b3-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="a82b3-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="a82b3-151">get_Toolbar</span></span> 

<span data-ttu-id="a82b3-152">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a82b3-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="a82b3-153">öffentliche HRESULT- [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="a82b3-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="a82b3-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="a82b3-154">get_Top</span></span> 

<span data-ttu-id="a82b3-155">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-155">The top position of the window.</span></span> <span data-ttu-id="a82b3-156">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="a82b3-157">Public HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="a82b3-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="a82b3-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="a82b3-158">get_Width</span></span> 

<span data-ttu-id="a82b3-159">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a82b3-159">The width of the window.</span></span>

> <span data-ttu-id="a82b3-160">öffentliche HRESULT- [get_Width](#get_width)(UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="a82b3-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="a82b3-161">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="a82b3-161">Minimum value is 100.</span></span> <span data-ttu-id="a82b3-162">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a82b3-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="a82b3-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="a82b3-163">HasPosition</span></span> 

<span data-ttu-id="a82b3-164">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="a82b3-164">Has specified left and top values.</span></span>

> <span data-ttu-id="a82b3-165">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="a82b3-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="a82b3-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="a82b3-166">HasSize</span></span> 

<span data-ttu-id="a82b3-167">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="a82b3-167">Has specified height and width values.</span></span>

> <span data-ttu-id="a82b3-168">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="a82b3-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

