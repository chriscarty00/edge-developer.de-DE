---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879653"
---
# <span data-ttu-id="2d345-104">Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse</span><span class="sxs-lookup"><span data-stu-id="2d345-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="2d345-105">Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d345-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="2d345-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2d345-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2d345-107">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2d345-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2d345-108">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="2d345-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="2d345-109">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2d345-109">Summary</span></span>

 <span data-ttu-id="2d345-110">Member</span><span class="sxs-lookup"><span data-stu-id="2d345-110">Members</span></span>                        | <span data-ttu-id="2d345-111">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2d345-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d345-112">Höhe</span><span class="sxs-lookup"><span data-stu-id="2d345-112">Height</span></span>](#height) | <span data-ttu-id="2d345-113">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-113">The height of the window.</span></span>
[<span data-ttu-id="2d345-114">Links</span><span class="sxs-lookup"><span data-stu-id="2d345-114">Left</span></span>](#left) | <span data-ttu-id="2d345-115">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-115">The left position of the window.</span></span>
[<span data-ttu-id="2d345-116">Menubar</span><span class="sxs-lookup"><span data-stu-id="2d345-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="2d345-117">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="2d345-118">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="2d345-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="2d345-119">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d345-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="2d345-120">Status</span><span class="sxs-lookup"><span data-stu-id="2d345-120">Status</span></span>](#status) | <span data-ttu-id="2d345-121">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="2d345-122">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="2d345-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="2d345-123">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="2d345-124">Oben</span><span class="sxs-lookup"><span data-stu-id="2d345-124">Top</span></span>](#top) | <span data-ttu-id="2d345-125">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-125">The top position of the window.</span></span>
[<span data-ttu-id="2d345-126">Breite</span><span class="sxs-lookup"><span data-stu-id="2d345-126">Width</span></span>](#width) | <span data-ttu-id="2d345-127">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-127">The width of the window.</span></span>
[<span data-ttu-id="2d345-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="2d345-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="2d345-129">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d345-129">Has specified left and top values.</span></span>
[<span data-ttu-id="2d345-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="2d345-130">HasSize</span></span>](#hassize) | <span data-ttu-id="2d345-131">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="2d345-131">Has specified height and width values.</span></span>

## <span data-ttu-id="2d345-132">Member</span><span class="sxs-lookup"><span data-stu-id="2d345-132">Members</span></span>

#### <span data-ttu-id="2d345-133">Höhe</span><span class="sxs-lookup"><span data-stu-id="2d345-133">Height</span></span> 

<span data-ttu-id="2d345-134">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-134">The height of the window.</span></span>

> <span data-ttu-id="2d345-135">öffentliche uint- [Höhe](#height)</span><span class="sxs-lookup"><span data-stu-id="2d345-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="2d345-136">Links</span><span class="sxs-lookup"><span data-stu-id="2d345-136">Left</span></span> 

<span data-ttu-id="2d345-137">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-137">The left position of the window.</span></span>

> <span data-ttu-id="2d345-138">public uint [Links](#left)</span><span class="sxs-lookup"><span data-stu-id="2d345-138">public uint [Left](#left)</span></span>

<span data-ttu-id="2d345-139">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="2d345-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="2d345-140">Menubar</span><span class="sxs-lookup"><span data-stu-id="2d345-140">MenuBar</span></span> 

<span data-ttu-id="2d345-141">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="2d345-142">öffentliche int- [Menüleiste](#menubar)</span><span class="sxs-lookup"><span data-stu-id="2d345-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="2d345-143">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="2d345-143">ScrollBars</span></span> 

<span data-ttu-id="2d345-144">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d345-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="2d345-145">öffentliche int-Bild [Laufleisten](#scrollbars)</span><span class="sxs-lookup"><span data-stu-id="2d345-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="2d345-146">Status</span><span class="sxs-lookup"><span data-stu-id="2d345-146">Status</span></span> 

<span data-ttu-id="2d345-147">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="2d345-148">öffentlicher int- [Status](#status)</span><span class="sxs-lookup"><span data-stu-id="2d345-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="2d345-149">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="2d345-149">Toolbar</span></span> 

<span data-ttu-id="2d345-150">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d345-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="2d345-151">öffentliche int- [Symbolleiste](#toolbar)</span><span class="sxs-lookup"><span data-stu-id="2d345-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="2d345-152">Oben</span><span class="sxs-lookup"><span data-stu-id="2d345-152">Top</span></span> 

<span data-ttu-id="2d345-153">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-153">The top position of the window.</span></span>

> <span data-ttu-id="2d345-154">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="2d345-154">public uint [Top](#top)</span></span>

<span data-ttu-id="2d345-155">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="2d345-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="2d345-156">Breite</span><span class="sxs-lookup"><span data-stu-id="2d345-156">Width</span></span> 

<span data-ttu-id="2d345-157">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="2d345-157">The width of the window.</span></span>

> <span data-ttu-id="2d345-158">öffentliche uint- [Breite](#width)</span><span class="sxs-lookup"><span data-stu-id="2d345-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="2d345-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="2d345-159">HasPosition</span></span> 

<span data-ttu-id="2d345-160">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d345-160">Has specified left and top values.</span></span>

> <span data-ttu-id="2d345-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="2d345-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="2d345-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="2d345-162">HasSize</span></span> 

<span data-ttu-id="2d345-163">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="2d345-163">Has specified height and width values.</span></span>

> <span data-ttu-id="2d345-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="2d345-164">public int [HasSize](#hassize)()</span></span>

