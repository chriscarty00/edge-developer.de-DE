---
description: Dieses Handbuch bietet eine Übersicht über die Entwicklerfeatures und -standards, die in EdgeHTML 16 enthalten sind.
title: Neue Features und APIs in EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399197"
---
# <a name="whats-new-in-edgehtml-16"></a><span data-ttu-id="dedc1-104">Neues in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="dedc1-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="dedc1-105">Hier finden Sie eine Liste der neuen und aktualisierten Features, die im Rahmen des [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\) auf der [EdgeHTML 16-Webplattform](https://blogs.windows.com/msedgedev/2017/10/17) ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="dedc1-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="dedc1-106">Änderungen an bestimmten Windows Insider Preview-Builds finden Sie unter [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) und [What's New in EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="dedc1-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="dedc1-107">Hier sehen Sie den Permalink für die folgende Liste der Änderungen:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="dedc1-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <a name="new-and-updated-features"></a><span data-ttu-id="dedc1-108">Neue und aktualisierte Features</span><span class="sxs-lookup"><span data-stu-id="dedc1-108">New and updated features</span></span>  

### <a name="css-grid-layout"></a><span data-ttu-id="dedc1-109">CSS-Rasterlayout</span><span class="sxs-lookup"><span data-stu-id="dedc1-109">CSS Grid Layout</span></span>  

<span data-ttu-id="dedc1-110">Microsoft Edge unterstützt jetzt die implementierung ohne Präfix von [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="dedc1-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="dedc1-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) definiert ein zweidimensionales rasterbasiertes Layoutsystem, das mehr Layoutfluidität als möglich durch positionierung mithilfe von Floats oder Skripts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="dedc1-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="dedc1-112">Im folgenden Beispiel wird css Grid Layout verwendet, um die Struktur für eine einfache Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dedc1-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="dedc1-113">CSS-Rasterlayout</span><span class="sxs-lookup"><span data-stu-id="dedc1-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="dedc1-114">Weitere Informationen finden Sie im <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> Stift-CSS-Rasterlayout </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) auf </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="dedc1-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <a name="css-object-fit-and-object-position"></a><span data-ttu-id="dedc1-115">CSS-Objekt-Anpassung und Objektposition</span><span class="sxs-lookup"><span data-stu-id="dedc1-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="dedc1-116">In EdgeHTML 16 wird die Unterstützung von CSS-Eigenschaften und [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) . [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position)</span><span class="sxs-lookup"><span data-stu-id="dedc1-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="dedc1-117">Diese Eigenschaften steuern die Position und Größe des ersetzten Inhalts innerhalb des Inhaltsfelds.</span><span class="sxs-lookup"><span data-stu-id="dedc1-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <a name="developer-tools"></a><span data-ttu-id="dedc1-118">Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="dedc1-118">Developer Tools</span></span>  

<span data-ttu-id="dedc1-119">In dieser Version haben wir eine wichtige Umgestaltung von Microsoft Edge DevTools für eine verbesserte Robustheit und Leistung gestartet und außerdem eine Reihe neuer Features hinzugefügt, die Sie heute auf [Windows-Insider-Builds verwenden](https://insider.windows.com) können.</span><span class="sxs-lookup"><span data-stu-id="dedc1-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="dedc1-120">Weitere Informationen zu den Geänderten finden Sie im [Microsoft Edge DevTools-Handbuch.](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="dedc1-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <a name="javascript"></a><span data-ttu-id="dedc1-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="dedc1-121">JavaScript</span></span>  

<span data-ttu-id="dedc1-122">[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) baut auf Javascript-Leistungsoptimierungen früherer Versionen auf, indem die Fähigkeit des Moduls zum Zurück-/Zurückspeichern von Funktionen erweitert, polymorphe Inlinecaches verwendet und Funktionen mit Blöcken optimiert `try` / `finally` werden.</span><span class="sxs-lookup"><span data-stu-id="dedc1-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="dedc1-123">Darüber hinaus sind features first previewed in EdgeHTML 15 jetzt stabil und standardmäßig aktiviert:</span><span class="sxs-lookup"><span data-stu-id="dedc1-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <a name="new-features"></a><span data-ttu-id="dedc1-124">Neue Features</span><span class="sxs-lookup"><span data-stu-id="dedc1-124">New features</span></span>  

<span data-ttu-id="dedc1-125">Standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="dedc1-125">On by default</span></span>  

*   <span data-ttu-id="dedc1-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([Demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="dedc1-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="dedc1-127">Freigegebener Speicher und Atome</span><span class="sxs-lookup"><span data-stu-id="dedc1-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a><span data-ttu-id="dedc1-128">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="dedc1-128">Payment Request API</span></span>  

<span data-ttu-id="dedc1-129">Die [Zahlungsanforderungs-API](../windows-integration/payment-request-api.md) ist ein offener, browserübergreifender Standard, mit dem Browser als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden \(z. B. Kreditkarten\) fungieren können, die Verbraucher in der Cloud gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="dedc1-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="dedc1-130">Die API in EdgeHTML 16 wurde so aktualisiert, dass sie der neuesten W3C [Payment Request-API-Spezifikation](https://w3c.github.io/payment-request) entspricht.</span><span class="sxs-lookup"><span data-stu-id="dedc1-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="dedc1-131">Dies umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dedc1-131">This includes:</span></span>  

*   <span data-ttu-id="dedc1-132">Unterstützung für die `canMakePayment()` Methode</span><span class="sxs-lookup"><span data-stu-id="dedc1-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="dedc1-133">Unterstützung für die `requestId` Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dedc1-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="dedc1-134">Unterstützung für die `id` Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dedc1-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="dedc1-135">Der Standardwert für den Parameter `complete()` der Methode wurde von " " in `result` "unbekannt" geändert.</span><span class="sxs-lookup"><span data-stu-id="dedc1-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <a name="service-workers"></a><span data-ttu-id="dedc1-136">Service Workers</span><span class="sxs-lookup"><span data-stu-id="dedc1-136">Service Workers</span></span>  

<span data-ttu-id="dedc1-137">[Service Workers](https://www.w3.org/TR/service-workers-1) sind ereignisgesteuerte Skripts, die im Hintergrund einer Webseite ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dedc1-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="dedc1-138">Service workers aktivieren Funktionen, die bisher nur für systemeigene Apps verfügbar waren, z. B. das Abfangen und Behandeln von Anforderungen aus dem Netzwerk, das Verwalten und Behandeln der Hintergrundsynchronisierung, des lokalen Speichers und der Pushbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="dedc1-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="dedc1-139">Die Unterstützung für Servicemitarbeiter befindet sich noch in der Entwicklung, Aber Sie können Ihre PWA in Microsoft Edge mit unserer experimentellen Service worker-Unterstützung testen, indem Sie das Service Worker-Feature in `about:flags` aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dedc1-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <a name="webvr"></a><span data-ttu-id="dedc1-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="dedc1-140">WebVR</span></span>  

<span data-ttu-id="dedc1-141">WebVR für Microsoft Edge hat unterstützung für [Bewegungscontroller hinzugefügt.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="dedc1-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="dedc1-142">Diese Controller haben eine präzise Position im Raum, sodass eine feinkörnige Interaktion mit digitalen Objekten in der virtuellen Realität ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="dedc1-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Bewegungscontroller" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="dedc1-144">Bewegungscontroller</span><span class="sxs-lookup"><span data-stu-id="dedc1-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="dedc1-145">WebVR wurde außerdem optimiert, um zwei verschiedene Arten von Erfahrungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dedc1-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="dedc1-146">**Windows Mixed Reality PCs** – Desktops und Laptops mit integrierten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="dedc1-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="dedc1-147">Wenn sie an diese Geräte angeschlossen werden, werden unsere immersiven Headsets mit 60 Frames pro Sekunde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dedc1-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="dedc1-148">**Windows Mixed Reality Ultra PCs** – Desktops und Laptops mit separaten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="dedc1-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="dedc1-149">Wenn sie an diese Geräte angeschlossen werden, werden unsere immersiven Headsets mit 90 Frames pro Sekunde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dedc1-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="dedc1-150">Beide Setups unterstützen dieselbe immersive Video- und Spielerfahrung.</span><span class="sxs-lookup"><span data-stu-id="dedc1-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="dedc1-151">Weitere Informationen zu den anstehenden Windows Mixed Reality-Updates finden Sie im [Windows Mixed Reality-Blogbeitrag](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) zum Feiertagsupdate.</span><span class="sxs-lookup"><span data-stu-id="dedc1-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="dedc1-152">Anleitungen und Demos finden Sie im [WebVR Developer Guide](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="dedc1-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="dedc1-153">Da die WebVR-Spezifikation noch in der Entwicklung ist, kann sich die Implementierung von Microsoft Edge später ändern.</span><span class="sxs-lookup"><span data-stu-id="dedc1-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <a name="new-apis-in-edgehtml-16"></a><span data-ttu-id="dedc1-154">Neue APIs in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="dedc1-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="dedc1-155">Hier ist die vollständige Liste der neuen APIs in EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="dedc1-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="dedc1-156">Sie sind im Format `[interface name].[api name]` aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dedc1-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="dedc1-157">Obwohl die folgenden APIs im DOM verfügbar gemacht werden, ist das End-to-End-Verhalten einiger möglicherweise noch in der Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="dedc1-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="dedc1-158">Das offizielle Wort zur Featureunterstützung finden Sie unter Microsoft Edge-Plattformstatus. [](https://developer.microsoft.com/microsoft-edge/platform/status)</span><span class="sxs-lookup"><span data-stu-id="dedc1-158">Refer to [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="dedc1-159">Neue APIs in EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="dedc1-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="dedc1-160">Weitere Informationen finden Sie in den neuen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> APIs des Stifts in EdgeHTML 16 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) auf </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="dedc1-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <a name="previous-edgehtml-releases"></a><span data-ttu-id="dedc1-161">Frühere EdgeHTML-Versionen</span><span class="sxs-lookup"><span data-stu-id="dedc1-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="dedc1-162">EdgeHTML 12 / Windows Build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="dedc1-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="dedc1-163">EdgeHTML 13 / Windows Build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="dedc1-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="dedc1-164">EdgeHTML 14 / Windows Build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="dedc1-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="dedc1-165">EdgeHTML 15 / Windows Build 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="dedc1-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
