---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: ee740f7d227ae98d451ba1c5e8f1017fe92514a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011370"
---
# <span data-ttu-id="1b777-104">0.9.579-Interface-ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="1b777-104">0.9.579 - interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="1b777-105">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="1b777-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="1b777-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1b777-106">Summary</span></span>

 <span data-ttu-id="1b777-107">Member</span><span class="sxs-lookup"><span data-stu-id="1b777-107">Members</span></span>                        | <span data-ttu-id="1b777-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1b777-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b777-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="1b777-109">get_Height</span></span>](#get_height) | <span data-ttu-id="1b777-110">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-110">The height of the window.</span></span>
[<span data-ttu-id="1b777-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="1b777-111">get_Left</span></span>](#get_left) | <span data-ttu-id="1b777-112">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-112">The left position of the window.</span></span> <span data-ttu-id="1b777-113">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="1b777-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="1b777-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="1b777-115">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="1b777-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="1b777-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="1b777-117">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b777-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="1b777-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="1b777-118">get_Status</span></span>](#get_status) | <span data-ttu-id="1b777-119">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="1b777-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="1b777-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="1b777-121">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="1b777-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="1b777-122">get_Top</span></span>](#get_top) | <span data-ttu-id="1b777-123">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-123">The top position of the window.</span></span> <span data-ttu-id="1b777-124">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="1b777-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="1b777-125">get_Width</span></span>](#get_width) | <span data-ttu-id="1b777-126">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-126">The width of the window.</span></span>
[<span data-ttu-id="1b777-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="1b777-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="1b777-128">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b777-128">Has specified left and top values.</span></span>
[<span data-ttu-id="1b777-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="1b777-129">HasSize</span></span>](#hassize) | <span data-ttu-id="1b777-130">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="1b777-130">Has specified height and width values.</span></span>

<span data-ttu-id="1b777-131">Diese Felder entsprechen dem "windowFeatures", das an Window. Open übergeben wurde, wie in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="1b777-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="1b777-132">Member</span><span class="sxs-lookup"><span data-stu-id="1b777-132">Members</span></span>

#### <span data-ttu-id="1b777-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="1b777-133">get_Height</span></span> 

<span data-ttu-id="1b777-134">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-134">The height of the window.</span></span>

> <span data-ttu-id="1b777-135">öffentliche HRESULT- [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="1b777-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="1b777-136">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="1b777-136">Minimum value is 100.</span></span> <span data-ttu-id="1b777-137">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="1b777-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="1b777-138">get_Left</span></span> 

<span data-ttu-id="1b777-139">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-139">The left position of the window.</span></span> <span data-ttu-id="1b777-140">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="1b777-141">öffentliche HRESULT- [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="1b777-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="1b777-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="1b777-142">get_MenuBar</span></span> 

<span data-ttu-id="1b777-143">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="1b777-144">öffentliche HRESULT- [get_MenuBar](#get_menubar)(bool \* Menüleiste)</span><span class="sxs-lookup"><span data-stu-id="1b777-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="1b777-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="1b777-145">get_ScrollBars</span></span> 

<span data-ttu-id="1b777-146">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b777-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="1b777-147">öffentliche HRESULT- [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="1b777-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="1b777-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="1b777-148">get_Status</span></span> 

<span data-ttu-id="1b777-149">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="1b777-150">Public HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="1b777-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="1b777-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="1b777-151">get_Toolbar</span></span> 

<span data-ttu-id="1b777-152">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b777-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="1b777-153">öffentliche HRESULT- [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="1b777-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="1b777-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="1b777-154">get_Top</span></span> 

<span data-ttu-id="1b777-155">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-155">The top position of the window.</span></span> <span data-ttu-id="1b777-156">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="1b777-157">Public HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="1b777-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="1b777-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="1b777-158">get_Width</span></span> 

<span data-ttu-id="1b777-159">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1b777-159">The width of the window.</span></span>

> <span data-ttu-id="1b777-160">öffentliche HRESULT- [get_Width](#get_width)(UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="1b777-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="1b777-161">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="1b777-161">Minimum value is 100.</span></span> <span data-ttu-id="1b777-162">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="1b777-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="1b777-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="1b777-163">HasPosition</span></span> 

<span data-ttu-id="1b777-164">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b777-164">Has specified left and top values.</span></span>

> <span data-ttu-id="1b777-165">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="1b777-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="1b777-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="1b777-166">HasSize</span></span> 

<span data-ttu-id="1b777-167">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="1b777-167">Has specified height and width values.</span></span>

> <span data-ttu-id="1b777-168">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="1b777-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

