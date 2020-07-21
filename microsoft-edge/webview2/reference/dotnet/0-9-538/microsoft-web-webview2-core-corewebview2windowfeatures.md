---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: d6d6f52456823488c07288c8ed07b9655a29883a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884437"
---
# <span data-ttu-id="d6a45-104">Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse</span><span class="sxs-lookup"><span data-stu-id="d6a45-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="d6a45-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d6a45-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d6a45-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d6a45-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d6a45-107">Fenster Features für ein WebView-Popupfenster</span><span class="sxs-lookup"><span data-stu-id="d6a45-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="d6a45-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d6a45-108">Summary</span></span>

 <span data-ttu-id="d6a45-109">Member</span><span class="sxs-lookup"><span data-stu-id="d6a45-109">Members</span></span>                        | <span data-ttu-id="d6a45-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d6a45-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d6a45-111">Höhe</span><span class="sxs-lookup"><span data-stu-id="d6a45-111">Height</span></span>](#height) | <span data-ttu-id="d6a45-112">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-112">The height of the window.</span></span>
[<span data-ttu-id="d6a45-113">Links</span><span class="sxs-lookup"><span data-stu-id="d6a45-113">Left</span></span>](#left) | <span data-ttu-id="d6a45-114">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-114">The left position of the window.</span></span>
[<span data-ttu-id="d6a45-115">Menubar</span><span class="sxs-lookup"><span data-stu-id="d6a45-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="d6a45-116">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="d6a45-117">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="d6a45-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="d6a45-118">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6a45-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="d6a45-119">Status</span><span class="sxs-lookup"><span data-stu-id="d6a45-119">Status</span></span>](#status) | <span data-ttu-id="d6a45-120">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="d6a45-121">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="d6a45-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="d6a45-122">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="d6a45-123">Oben</span><span class="sxs-lookup"><span data-stu-id="d6a45-123">Top</span></span>](#top) | <span data-ttu-id="d6a45-124">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-124">The top position of the window.</span></span>
[<span data-ttu-id="d6a45-125">Breite</span><span class="sxs-lookup"><span data-stu-id="d6a45-125">Width</span></span>](#width) | <span data-ttu-id="d6a45-126">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-126">The width of the window.</span></span>
[<span data-ttu-id="d6a45-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="d6a45-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="d6a45-128">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6a45-128">Has specified left and top values.</span></span>
[<span data-ttu-id="d6a45-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="d6a45-129">HasSize</span></span>](#hassize) | <span data-ttu-id="d6a45-130">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="d6a45-130">Has specified height and width values.</span></span>

## <span data-ttu-id="d6a45-131">Member</span><span class="sxs-lookup"><span data-stu-id="d6a45-131">Members</span></span>

#### <span data-ttu-id="d6a45-132">Höhe</span><span class="sxs-lookup"><span data-stu-id="d6a45-132">Height</span></span> 

<span data-ttu-id="d6a45-133">Die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-133">The height of the window.</span></span>

> <span data-ttu-id="d6a45-134">öffentliche uint- [Höhe](#height)</span><span class="sxs-lookup"><span data-stu-id="d6a45-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="d6a45-135">Links</span><span class="sxs-lookup"><span data-stu-id="d6a45-135">Left</span></span> 

<span data-ttu-id="d6a45-136">Die linke Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-136">The left position of the window.</span></span>

> <span data-ttu-id="d6a45-137">public uint [Links](#left)</span><span class="sxs-lookup"><span data-stu-id="d6a45-137">public uint [Left](#left)</span></span>

<span data-ttu-id="d6a45-138">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="d6a45-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="d6a45-139">Menubar</span><span class="sxs-lookup"><span data-stu-id="d6a45-139">MenuBar</span></span> 

<span data-ttu-id="d6a45-140">Gibt an, ob die Menüleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="d6a45-141">öffentliche int- [Menüleiste](#menubar)</span><span class="sxs-lookup"><span data-stu-id="d6a45-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="d6a45-142">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="d6a45-142">ScrollBars</span></span> 

<span data-ttu-id="d6a45-143">Gibt an, ob Bildlaufleisten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6a45-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="d6a45-144">öffentliche int-Bild [Laufleisten](#scrollbars)</span><span class="sxs-lookup"><span data-stu-id="d6a45-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="d6a45-145">Status</span><span class="sxs-lookup"><span data-stu-id="d6a45-145">Status</span></span> 

<span data-ttu-id="d6a45-146">Gibt an, ob eine Statusleiste hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="d6a45-147">öffentlicher int- [Status](#status)</span><span class="sxs-lookup"><span data-stu-id="d6a45-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="d6a45-148">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="d6a45-148">Toolbar</span></span> 

<span data-ttu-id="d6a45-149">Gibt an, ob die Browsersymbolleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6a45-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="d6a45-150">öffentliche int- [Symbolleiste](#toolbar)</span><span class="sxs-lookup"><span data-stu-id="d6a45-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="d6a45-151">Oben</span><span class="sxs-lookup"><span data-stu-id="d6a45-151">Top</span></span> 

<span data-ttu-id="d6a45-152">Die obere Position des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-152">The top position of the window.</span></span>

> <span data-ttu-id="d6a45-153">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="d6a45-153">public uint [Top](#top)</span></span>

<span data-ttu-id="d6a45-154">Schlägt fehl, wenn HasPosition falsch ist.</span><span class="sxs-lookup"><span data-stu-id="d6a45-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="d6a45-155">Breite</span><span class="sxs-lookup"><span data-stu-id="d6a45-155">Width</span></span> 

<span data-ttu-id="d6a45-156">Die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d6a45-156">The width of the window.</span></span>

> <span data-ttu-id="d6a45-157">öffentliche uint- [Breite](#width)</span><span class="sxs-lookup"><span data-stu-id="d6a45-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="d6a45-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="d6a45-158">HasPosition</span></span> 

<span data-ttu-id="d6a45-159">Hat den Wert für left und Top angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6a45-159">Has specified left and top values.</span></span>

> <span data-ttu-id="d6a45-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="d6a45-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="d6a45-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="d6a45-161">HasSize</span></span> 

<span data-ttu-id="d6a45-162">Hat die angegebenen Werte für Höhe und Breite.</span><span class="sxs-lookup"><span data-stu-id="d6a45-162">Has specified height and width values.</span></span>

> <span data-ttu-id="d6a45-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="d6a45-163">public int [HasSize](#hassize)()</span></span>

