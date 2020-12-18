---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Dieser Leitfaden enthält eine Übersicht über die neuen Features und APIs in EdgeHTML 16.
title: Neue Features und APIs in EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7697114546153555d947903eda6bf8477cca3516
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233915"
---
# <span data-ttu-id="4bc0d-104">Neuerungen in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4bc0d-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="4bc0d-105">Nachfolgend finden Sie eine Liste der neuen und aktualisierten Features, die in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) Web Platform ausgeliefert wurden, als Teil des [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \ (10/2017, Build 16299 \).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="4bc0d-106">Änderungen an bestimmten Windows Insider Preview-Builds finden Sie im [Microsoft Edge-Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) und [Neuerungen in EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="4bc0d-107">Hier ist der Permalink für die folgende Liste der  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) Änderungen:</span><span class="sxs-lookup"><span data-stu-id="4bc0d-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="4bc0d-108">Neue und aktualisierte Features</span><span class="sxs-lookup"><span data-stu-id="4bc0d-108">New and updated features</span></span>  

### <span data-ttu-id="4bc0d-109">CSS-Raster Layout</span><span class="sxs-lookup"><span data-stu-id="4bc0d-109">CSS Grid Layout</span></span>  

<span data-ttu-id="4bc0d-110">Microsoft Edge unterstützt jetzt die UN-voreingestellte Implementierung des [CSS-Rasterlayouts](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="4bc0d-111">Das [Rasterlayout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) definiert ein zweidimensionales Grid-basiertes Layoutsystem, das mehr Layout-Fluidität als möglich mit der Positionierung mithilfe von Floats oder Skripts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="4bc0d-112">Im folgenden Beispiel wird das CSS-Raster Layout verwendet, um die Struktur für eine einfache Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="4bc0d-113">CSS-Raster Layout</span><span class="sxs-lookup"><span data-stu-id="4bc0d-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="4bc0d-114">Sehen Sie sich das Layout "Stift <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> -CSS-Raster" </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="4bc0d-115">CSS-Objekt-fit und Objekt-Position</span><span class="sxs-lookup"><span data-stu-id="4bc0d-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="4bc0d-116">EdgeHTML 16 führt Unterstützung für CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) -Eigenschaften und [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="4bc0d-117">Diese Eigenschaften steuern die Position und Größe des ersetzten Inhalts im Feldinhalt.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="4bc0d-118">Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="4bc0d-118">Developer Tools</span></span>  

<span data-ttu-id="4bc0d-119">In dieser Version haben wir einen wichtigen Microsoft Edge devtools-Umgestaltungs Aufwand für verbesserte Robustheit und Leistung gestartet und außerdem eine Reihe neuer Funktionen hinzugefügt, die Sie heute auf [Windows-Insider](https://insider.windows.com) -Builds verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="4bc0d-120">Weitere Informationen zu den Änderungen finden Sie im [Microsoft Edge devtools-Leitfaden](../whats-new.md) .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="4bc0d-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4bc0d-121">JavaScript</span></span>  

<span data-ttu-id="4bc0d-122">[EdgeHTML 16 baut auf JavaScript-Leistungs](https://blogs.windows.com/msedgedev/2017/10/31) Optimierungen früherer Versionen auf, indem die Fähigkeit des Chakra-Moduls erweitert wird, Funktionen zu verzögern/erneut zu verzögern, polymorphe Inline-Caches zu verwenden und Funktionen mit `try` / `finally` Blöcken zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="4bc0d-123">Darüber hinaus sind Features, die in EdgeHTML 15 erstmals in der Vorschau angezeigt werden, jetzt stabil und standardmäßig aktiviert:</span><span class="sxs-lookup"><span data-stu-id="4bc0d-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="4bc0d-124">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="4bc0d-124">New features</span></span>  

<span data-ttu-id="4bc0d-125">Standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="4bc0d-125">On by default</span></span>  

*   <span data-ttu-id="4bc0d-126">[Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \ ([Demo](https://webassembly.org/demo))</span><span class="sxs-lookup"><span data-stu-id="4bc0d-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="4bc0d-127">Shared Memory und Atomics</span><span class="sxs-lookup"><span data-stu-id="4bc0d-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="4bc0d-128">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="4bc0d-128">Payment Request API</span></span>  

<span data-ttu-id="4bc0d-129">Die [Zahlungs Anforderungs-API](../windows-integration/payment-request-api.md) ist ein offener, browserübergreifender Standard, der es Browsern ermöglicht, als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden zu fungieren (wie Kreditkarten \), die von Verbrauchern in der Cloud gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="4bc0d-130">Die API in EdgeHTML 16 wurde so aktualisiert, dass Sie der neuesten API-Spezifikation für die W3C [-Zahlungsanforderung](https://w3c.github.io/payment-request) entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="4bc0d-131">Dies umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4bc0d-131">This includes:</span></span>  

*   <span data-ttu-id="4bc0d-132">Unterstützung für die `canMakePayment()` Methode</span><span class="sxs-lookup"><span data-stu-id="4bc0d-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="4bc0d-133">Unterstützung für die `requestId` Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4bc0d-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="4bc0d-134">Unterstützung für die `id` Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4bc0d-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="4bc0d-135">Der Standardwert für den `complete()` Parameter der Methode `result` wurde von "" in "unbekannt" geändert.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="4bc0d-136">Service Workers</span><span class="sxs-lookup"><span data-stu-id="4bc0d-136">Service Workers</span></span>  

<span data-ttu-id="4bc0d-137">[Dienstmitarbeiter](https://www.w3.org/TR/service-workers-1) sind ereignisgesteuerte Skripts, die im Hintergrund einer Webseite ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="4bc0d-138">Dienstmitarbeiter aktivieren Funktionen, die zuvor nur für systemeigene apps verfügbar waren, wie das Abfangen und behandeln von Anforderungen aus dem Netzwerk, verwalten und behandeln von Hintergrundsynchronisierung, lokalem Speicher und Push-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="4bc0d-139">Die Unterstützung für Service Worker befindet sich noch in der Entwicklung, doch Sie können Ihre PWA in Microsoft Edge mit unserem experimental Service Worker-Support testen, indem Sie das Feature "Dienstmitarbeiter" in aktivieren `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="4bc0d-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="4bc0d-140">WebVR</span></span>  

<span data-ttu-id="4bc0d-141">WebVR für Microsoft Edge hat Unterstützung für [Motion Controller](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="4bc0d-142">Diese Controller haben eine präzise Position im Raum, was eine feinkörnige Interaktion mit digitalen Objekten in der virtuellen Realität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Motion-Controller" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="4bc0d-144">Motion-Controller</span><span class="sxs-lookup"><span data-stu-id="4bc0d-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="4bc0d-145">WebVR wurde ebenfalls optimiert, um zwei unterschiedliche Arten von Erfahrungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="4bc0d-146">**Windows Mixed Reality-PCs** – Desktops und Laptops mit integrierter Grafik.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="4bc0d-147">Wenn Sie an diese Geräte angeschlossen sind, können unsere immersiven Headsets mit 60 Frames pro Sekunde ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="4bc0d-148">**Windows Mixed Reality Ultra-PCs** – Desktops und Laptops mit diskreten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="4bc0d-149">Wenn Sie an diese Geräte angeschlossen sind, können unsere immersiven Headsets mit 90 Frames pro Sekunde ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="4bc0d-150">Beide Setups unterstützen die gleichen immersiven Video-und Spielerlebnisse.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="4bc0d-151">Weitere Informationen zu den bevorstehenden Windows-Mixed-Reality-Updates finden Sie im Blogbeitrag [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) Holiday Update.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="4bc0d-152">Anleitungen und Demos finden Sie im [WebVR-Entwicklerhandbuch](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="4bc0d-153">Da sich die WebVR-Spezifikation noch in der Entwicklung befindet, kann sich die Implementierung von Microsoft Edge später in der Zeile ändern.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="4bc0d-154">Neue APIs in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4bc0d-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="4bc0d-155">Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="4bc0d-156">Sie werden im Format von angezeigt `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="4bc0d-157">Obwohl die folgenden APIs im DOM verfügbar gemacht werden, kann sich das End-to-End-Verhalten einiger Entwickler weiterhin entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="4bc0d-158">Informationen zum offiziellen Word-Feature-Support finden Sie im  [Microsoft Edge-Platt Form Status](https://developer.microsoft.com/microsoft-edge/platform/status) .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="4bc0d-159">Neue APIs in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4bc0d-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="4bc0d-160">Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> in EdgeHTML 16 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc0d-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="4bc0d-161">Vorherige EdgeHTML-Versionen</span><span class="sxs-lookup"><span data-stu-id="4bc0d-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="4bc0d-162">EdgeHTML 12/Windows Build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="4bc0d-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="4bc0d-163">EdgeHTML 13/Windows Build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="4bc0d-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="4bc0d-164">EdgeHTML 14/Windows Build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="4bc0d-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="4bc0d-165">EdgeHTML 15/Windows Build 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="4bc0d-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
