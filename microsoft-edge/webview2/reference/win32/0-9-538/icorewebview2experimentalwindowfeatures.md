---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 2672f2aac842fd475f6148c439dbecdacd7793ee
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885403"
---
# <span data-ttu-id="95aa6-104">Schnittstellen ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="95aa6-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="95aa6-105">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="95aa6-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="95aa6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="95aa6-106">Summary</span></span>

 <span data-ttu-id="95aa6-107">Member</span><span class="sxs-lookup"><span data-stu-id="95aa6-107">Members</span></span>                        | <span data-ttu-id="95aa6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="95aa6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95aa6-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="95aa6-109">get_Height</span></span>](#get_height) | <span data-ttu-id="95aa6-110">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-110">The height of the window.</span></span>
[<span data-ttu-id="95aa6-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="95aa6-111">get_Left</span></span>](#get_left) | <span data-ttu-id="95aa6-112">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-112">The left position of the window.</span></span> <span data-ttu-id="95aa6-113">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="95aa6-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="95aa6-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="95aa6-115">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="95aa6-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="95aa6-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="95aa6-117">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95aa6-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="95aa6-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="95aa6-118">get_Status</span></span>](#get_status) | <span data-ttu-id="95aa6-119">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="95aa6-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="95aa6-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="95aa6-121">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="95aa6-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="95aa6-122">get_Top</span></span>](#get_top) | <span data-ttu-id="95aa6-123">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-123">The top position of the window.</span></span> <span data-ttu-id="95aa6-124">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="95aa6-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="95aa6-125">get_Width</span></span>](#get_width) | <span data-ttu-id="95aa6-126">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-126">The width of the window.</span></span>
[<span data-ttu-id="95aa6-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="95aa6-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="95aa6-128">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="95aa6-128">Has specified left and top values.</span></span>
[<span data-ttu-id="95aa6-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="95aa6-129">HasSize</span></span>](#hassize) | <span data-ttu-id="95aa6-130">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="95aa6-130">Has specified height and width values.</span></span>

<span data-ttu-id="95aa6-131">Diese Felder entsprechen dem "windowFeatures", das an Window. Open übergeben wurde, wie in[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="95aa6-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="95aa6-132">Member</span><span class="sxs-lookup"><span data-stu-id="95aa6-132">Members</span></span>

#### <span data-ttu-id="95aa6-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="95aa6-133">get_Height</span></span> 

<span data-ttu-id="95aa6-134">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-134">The height of the window.</span></span>

> <span data-ttu-id="95aa6-135">öffentliche HRESULT- [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="95aa6-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="95aa6-136">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="95aa6-136">Minimum value is 100.</span></span> <span data-ttu-id="95aa6-137">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="95aa6-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="95aa6-138">get_Left</span></span> 

<span data-ttu-id="95aa6-139">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-139">The left position of the window.</span></span> <span data-ttu-id="95aa6-140">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="95aa6-141">öffentliche HRESULT- [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="95aa6-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="95aa6-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="95aa6-142">get_MenuBar</span></span> 

<span data-ttu-id="95aa6-143">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="95aa6-144">öffentliche HRESULT- [get_MenuBar](#get_menubar)(bool \* Menüleiste)</span><span class="sxs-lookup"><span data-stu-id="95aa6-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="95aa6-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="95aa6-145">get_ScrollBars</span></span> 

<span data-ttu-id="95aa6-146">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95aa6-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="95aa6-147">öffentliche HRESULT- [get_ScrollBars](#get_scrollbars)(bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="95aa6-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="95aa6-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="95aa6-148">get_Status</span></span> 

<span data-ttu-id="95aa6-149">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="95aa6-150">Public HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="95aa6-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="95aa6-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="95aa6-151">get_Toolbar</span></span> 

<span data-ttu-id="95aa6-152">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95aa6-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="95aa6-153">öffentliche HRESULT- [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="95aa6-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="95aa6-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="95aa6-154">get_Top</span></span> 

<span data-ttu-id="95aa6-155">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-155">The top position of the window.</span></span> <span data-ttu-id="95aa6-156">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="95aa6-157">Public HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="95aa6-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="95aa6-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="95aa6-158">get_Width</span></span> 

<span data-ttu-id="95aa6-159">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="95aa6-159">The width of the window.</span></span>

> <span data-ttu-id="95aa6-160">öffentliche HRESULT- [get_Width](#get_width)(UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="95aa6-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="95aa6-161">Der Mindestwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="95aa6-161">Minimum value is 100.</span></span> <span data-ttu-id="95aa6-162">Schlägt fehl, wenn HasSize falsch ist.</span><span class="sxs-lookup"><span data-stu-id="95aa6-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="95aa6-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="95aa6-163">HasPosition</span></span> 

<span data-ttu-id="95aa6-164">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="95aa6-164">Has specified left and top values.</span></span>

> <span data-ttu-id="95aa6-165">Public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="95aa6-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="95aa6-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="95aa6-166">HasSize</span></span> 

<span data-ttu-id="95aa6-167">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="95aa6-167">Has specified height and width values.</span></span>

> <span data-ttu-id="95aa6-168">Public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="95aa6-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

