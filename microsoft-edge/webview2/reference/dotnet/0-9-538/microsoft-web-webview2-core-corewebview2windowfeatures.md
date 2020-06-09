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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698915"
---
# <span data-ttu-id="a9317-104">Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse</span><span class="sxs-lookup"><span data-stu-id="a9317-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="a9317-105">Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9317-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="a9317-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a9317-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a9317-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="a9317-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a9317-108">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="a9317-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="a9317-109">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a9317-109">Summary</span></span>

 <span data-ttu-id="a9317-110">Member</span><span class="sxs-lookup"><span data-stu-id="a9317-110">Members</span></span>                        | <span data-ttu-id="a9317-111">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a9317-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a9317-112">Höhe</span><span class="sxs-lookup"><span data-stu-id="a9317-112">Height</span></span>](#height) | <span data-ttu-id="a9317-113">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-113">The height of the window.</span></span>
[<span data-ttu-id="a9317-114">Links</span><span class="sxs-lookup"><span data-stu-id="a9317-114">Left</span></span>](#left) | <span data-ttu-id="a9317-115">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-115">The left position of the window.</span></span>
[<span data-ttu-id="a9317-116">Menubar</span><span class="sxs-lookup"><span data-stu-id="a9317-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="a9317-117">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="a9317-118">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="a9317-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="a9317-119">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9317-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="a9317-120">Status</span><span class="sxs-lookup"><span data-stu-id="a9317-120">Status</span></span>](#status) | <span data-ttu-id="a9317-121">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="a9317-122">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="a9317-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="a9317-123">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="a9317-124">Oben</span><span class="sxs-lookup"><span data-stu-id="a9317-124">Top</span></span>](#top) | <span data-ttu-id="a9317-125">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-125">The top position of the window.</span></span>
[<span data-ttu-id="a9317-126">Breite</span><span class="sxs-lookup"><span data-stu-id="a9317-126">Width</span></span>](#width) | <span data-ttu-id="a9317-127">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-127">The width of the window.</span></span>
[<span data-ttu-id="a9317-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="a9317-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="a9317-129">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9317-129">Has specified left and top values.</span></span>
[<span data-ttu-id="a9317-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="a9317-130">HasSize</span></span>](#hassize) | <span data-ttu-id="a9317-131">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="a9317-131">Has specified height and width values.</span></span>

## <span data-ttu-id="a9317-132">Member</span><span class="sxs-lookup"><span data-stu-id="a9317-132">Members</span></span>

#### <span data-ttu-id="a9317-133">Höhe</span><span class="sxs-lookup"><span data-stu-id="a9317-133">Height</span></span> 

<span data-ttu-id="a9317-134">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-134">The height of the window.</span></span>

> <span data-ttu-id="a9317-135">öffentliche uint- [Höhe](#height)</span><span class="sxs-lookup"><span data-stu-id="a9317-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="a9317-136">Links</span><span class="sxs-lookup"><span data-stu-id="a9317-136">Left</span></span> 

<span data-ttu-id="a9317-137">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-137">The left position of the window.</span></span>

> <span data-ttu-id="a9317-138">public uint [Links](#left)</span><span class="sxs-lookup"><span data-stu-id="a9317-138">public uint [Left](#left)</span></span>

<span data-ttu-id="a9317-139">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a9317-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="a9317-140">Menubar</span><span class="sxs-lookup"><span data-stu-id="a9317-140">MenuBar</span></span> 

<span data-ttu-id="a9317-141">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="a9317-142">öffentliche int- [Menüleiste](#menubar)</span><span class="sxs-lookup"><span data-stu-id="a9317-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="a9317-143">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="a9317-143">ScrollBars</span></span> 

<span data-ttu-id="a9317-144">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9317-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="a9317-145">öffentliche int-Bild [Laufleisten](#scrollbars)</span><span class="sxs-lookup"><span data-stu-id="a9317-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="a9317-146">Status</span><span class="sxs-lookup"><span data-stu-id="a9317-146">Status</span></span> 

<span data-ttu-id="a9317-147">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="a9317-148">öffentlicher int- [Status](#status)</span><span class="sxs-lookup"><span data-stu-id="a9317-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="a9317-149">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="a9317-149">Toolbar</span></span> 

<span data-ttu-id="a9317-150">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9317-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="a9317-151">öffentliche int- [Symbolleiste](#toolbar)</span><span class="sxs-lookup"><span data-stu-id="a9317-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="a9317-152">Oben</span><span class="sxs-lookup"><span data-stu-id="a9317-152">Top</span></span> 

<span data-ttu-id="a9317-153">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-153">The top position of the window.</span></span>

> <span data-ttu-id="a9317-154">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="a9317-154">public uint [Top](#top)</span></span>

<span data-ttu-id="a9317-155">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="a9317-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="a9317-156">Breite</span><span class="sxs-lookup"><span data-stu-id="a9317-156">Width</span></span> 

<span data-ttu-id="a9317-157">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9317-157">The width of the window.</span></span>

> <span data-ttu-id="a9317-158">öffentliche uint- [Breite](#width)</span><span class="sxs-lookup"><span data-stu-id="a9317-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="a9317-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="a9317-159">HasPosition</span></span> 

<span data-ttu-id="a9317-160">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9317-160">Has specified left and top values.</span></span>

> <span data-ttu-id="a9317-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="a9317-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="a9317-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="a9317-162">HasSize</span></span> 

<span data-ttu-id="a9317-163">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="a9317-163">Has specified height and width values.</span></span>

> <span data-ttu-id="a9317-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="a9317-164">public int [HasSize](#hassize)()</span></span>

