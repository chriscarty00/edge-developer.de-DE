---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 59e051c0537357fed89d6300db69ea479b656c7e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010516"
---
# <span data-ttu-id="3d89e-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse</span><span class="sxs-lookup"><span data-stu-id="3d89e-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="3d89e-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3d89e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3d89e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3d89e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3d89e-107">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="3d89e-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="3d89e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3d89e-108">Summary</span></span>

 <span data-ttu-id="3d89e-109">Member</span><span class="sxs-lookup"><span data-stu-id="3d89e-109">Members</span></span>                        | <span data-ttu-id="3d89e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3d89e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d89e-111">Höhe</span><span class="sxs-lookup"><span data-stu-id="3d89e-111">Height</span></span>](#height) | <span data-ttu-id="3d89e-112">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-112">The height of the window.</span></span>
[<span data-ttu-id="3d89e-113">Links</span><span class="sxs-lookup"><span data-stu-id="3d89e-113">Left</span></span>](#left) | <span data-ttu-id="3d89e-114">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-114">The left position of the window.</span></span>
[<span data-ttu-id="3d89e-115">Menubar</span><span class="sxs-lookup"><span data-stu-id="3d89e-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="3d89e-116">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="3d89e-117">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="3d89e-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="3d89e-118">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d89e-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="3d89e-119">Status</span><span class="sxs-lookup"><span data-stu-id="3d89e-119">Status</span></span>](#status) | <span data-ttu-id="3d89e-120">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="3d89e-121">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="3d89e-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="3d89e-122">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="3d89e-123">Oben</span><span class="sxs-lookup"><span data-stu-id="3d89e-123">Top</span></span>](#top) | <span data-ttu-id="3d89e-124">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-124">The top position of the window.</span></span>
[<span data-ttu-id="3d89e-125">Breite</span><span class="sxs-lookup"><span data-stu-id="3d89e-125">Width</span></span>](#width) | <span data-ttu-id="3d89e-126">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-126">The width of the window.</span></span>
[<span data-ttu-id="3d89e-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="3d89e-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="3d89e-128">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d89e-128">Has specified left and top values.</span></span>
[<span data-ttu-id="3d89e-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="3d89e-129">HasSize</span></span>](#hassize) | <span data-ttu-id="3d89e-130">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="3d89e-130">Has specified height and width values.</span></span>

## <span data-ttu-id="3d89e-131">Member</span><span class="sxs-lookup"><span data-stu-id="3d89e-131">Members</span></span>

#### <span data-ttu-id="3d89e-132">Höhe</span><span class="sxs-lookup"><span data-stu-id="3d89e-132">Height</span></span> 

<span data-ttu-id="3d89e-133">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-133">The height of the window.</span></span>

> <span data-ttu-id="3d89e-134">öffentliche uint- [Höhe](#height)</span><span class="sxs-lookup"><span data-stu-id="3d89e-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="3d89e-135">Links</span><span class="sxs-lookup"><span data-stu-id="3d89e-135">Left</span></span> 

<span data-ttu-id="3d89e-136">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-136">The left position of the window.</span></span>

> <span data-ttu-id="3d89e-137">public uint [Links](#left)</span><span class="sxs-lookup"><span data-stu-id="3d89e-137">public uint [Left](#left)</span></span>

<span data-ttu-id="3d89e-138">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="3d89e-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="3d89e-139">Menubar</span><span class="sxs-lookup"><span data-stu-id="3d89e-139">MenuBar</span></span> 

<span data-ttu-id="3d89e-140">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="3d89e-141">öffentliche int- [Menüleiste](#menubar)</span><span class="sxs-lookup"><span data-stu-id="3d89e-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="3d89e-142">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="3d89e-142">ScrollBars</span></span> 

<span data-ttu-id="3d89e-143">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d89e-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="3d89e-144">öffentliche int-Bild [Laufleisten](#scrollbars)</span><span class="sxs-lookup"><span data-stu-id="3d89e-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="3d89e-145">Status</span><span class="sxs-lookup"><span data-stu-id="3d89e-145">Status</span></span> 

<span data-ttu-id="3d89e-146">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="3d89e-147">öffentlicher int- [Status](#status)</span><span class="sxs-lookup"><span data-stu-id="3d89e-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="3d89e-148">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="3d89e-148">Toolbar</span></span> 

<span data-ttu-id="3d89e-149">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d89e-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="3d89e-150">öffentliche int- [Symbolleiste](#toolbar)</span><span class="sxs-lookup"><span data-stu-id="3d89e-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="3d89e-151">Oben</span><span class="sxs-lookup"><span data-stu-id="3d89e-151">Top</span></span> 

<span data-ttu-id="3d89e-152">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-152">The top position of the window.</span></span>

> <span data-ttu-id="3d89e-153">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="3d89e-153">public uint [Top](#top)</span></span>

<span data-ttu-id="3d89e-154">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="3d89e-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="3d89e-155">Breite</span><span class="sxs-lookup"><span data-stu-id="3d89e-155">Width</span></span> 

<span data-ttu-id="3d89e-156">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3d89e-156">The width of the window.</span></span>

> <span data-ttu-id="3d89e-157">öffentliche uint- [Breite](#width)</span><span class="sxs-lookup"><span data-stu-id="3d89e-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="3d89e-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="3d89e-158">HasPosition</span></span> 

<span data-ttu-id="3d89e-159">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d89e-159">Has specified left and top values.</span></span>

> <span data-ttu-id="3d89e-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="3d89e-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="3d89e-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="3d89e-161">HasSize</span></span> 

<span data-ttu-id="3d89e-162">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="3d89e-162">Has specified height and width values.</span></span>

> <span data-ttu-id="3d89e-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="3d89e-163">public int [HasSize](#hassize)()</span></span>

