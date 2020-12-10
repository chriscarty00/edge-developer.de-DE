---
description: Microsoft Edge unter Linux, verbesserte webhint-Tipps im Problem Tool, neue Features für die Dienst Worker-Debuggen und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205243"
---
# <span data-ttu-id="1e1aa-104">Neuerungen in devtools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="1e1aa-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="1e1aa-105">Microsoft Edge-und Microsoft Edge-Treiber jetzt auf Linux verfügbar</span><span class="sxs-lookup"><span data-stu-id="1e1aa-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="1e1aa-106">Microsoft Edge dev wird nun auf der Grundlage von Ubuntu-, Debian-, Fedora-und openSUSE-Distributionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="1e1aa-107">Laden Sie Microsoft Edge dev `.deb` oder `.rpm` Package direkt von der [Microsoft Edge Insider-Website][MicrosoftinsiderDownloadPlatformLinux] herunter, und installieren Sie Sie, oder verwenden Sie die standardmäßigen Paket Verwaltungstools Ihrer Linux-Distribution.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="1e1aa-108">Wenn Sie eine Linux-Umgebung in ihrer Continuous Integration and Delivery \ (CI/CD \)-Lösungen verwenden, steht Microsoft Edge Driver auch unter Linux zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="1e1aa-109">Wenn Sie mit der Automatisierung von Microsoft Edge dev mit Microsoft Edge Driver beginnen möchten, navigieren Sie zur [Seite Microsoft Edge Driver Downloads][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="1e1aa-110">Hilfe zur Automatisierung von Microsoft Edge dev zusammen mit Microsoft Edge Driver finden [Sie unter Verwenden von WebDriver (Chrom) für die Testautomatisierung][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools in Microsoft Edge unter Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="1e1aa-112">DevTools in Microsoft Edge unter Linux</span><span class="sxs-lookup"><span data-stu-id="1e1aa-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="1e1aa-113">Verbesserte Tipps für webhints und Plattformen im Problem Tool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="1e1aa-114">Ein Open-Source-Tool, [webhint][WebhintMain], bietet Echtzeitfeedback für Websites und lokale Webseiten.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="1e1aa-115">Beginnen Sie mit [Microsoft Edge, Version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], und überprüfen Sie das webhint-Feedback im [Issues][DevtoolsIssuesIndex] -Tool.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="1e1aa-116">Probleme, die im Tool " **Probleme** " angezeigt werden, sind jetzt mit dem Hinzufügen der folgenden Kategorien leichter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="1e1aa-117">Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="1e1aa-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="1e1aa-118">Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="1e1aa-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="1e1aa-119">Leistung</span><span class="sxs-lookup"><span data-stu-id="1e1aa-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="1e1aa-120">Von Fallgruben</span><span class="sxs-lookup"><span data-stu-id="1e1aa-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="1e1aa-121">PWA</span><span class="sxs-lookup"><span data-stu-id="1e1aa-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="1e1aa-122">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="1e1aa-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="1e1aa-123">Sie können jetzt die Probleme von Drittanbietern mithilfe eines neuen Kontrollkästchens herausfiltern.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="1e1aa-124">Die Filterfunktionalität hilft Ihnen, Probleme im Zusammenhang mit Code aus Drittanbieterbibliotheken oder anderen Quellen zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="1e1aa-125">Damit Sie die von [webhint][WebhintMain]aufgedeckten Probleme überprüfen können, werden im Tool **Probleme** nun die folgenden Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="1e1aa-126">Verbesserte Codeausschnitte.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="1e1aa-127">Links zu anderen relevanten Panels.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="1e1aa-128">Links zur Dokumentation, die Ihnen bei der Behebung von Problemen in Ihrer Website helfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Problem Tool" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="1e1aa-130">**Problem** Tool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="1e1aa-131">Zusammengesetzte Layer sind jetzt in der 3D-Ansicht</span><span class="sxs-lookup"><span data-stu-id="1e1aa-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="1e1aa-132">Sie können jetzt **Layer** -Inhalte neben z-Index-Werten und dem Dokumentobjektmodell \ (DOM \) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="1e1aa-133">Mit dieser Funktion können Sie so oft Debuggen, ohne zwischen [3D-Ansicht][Devtools3dViewIndex] und **Layer** -Tools umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="1e1aa-134">Für ein umfassendes visuelles Debugging [werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Bereich ' zusammengesetzte Ebenen '" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="1e1aa-136">Bereich ' **zusammengesetzte Ebenen** '</span><span class="sxs-lookup"><span data-stu-id="1e1aa-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="1e1aa-137">CSS-Variablendefinitionen im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="1e1aa-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="1e1aa-138">Im Bereich " **Formatvorlagen** " werden die [CSS-Variablen][MdnUsingCssCustomProperties] nun direkt mit jeder Definition verknüpft.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="1e1aa-139">Wählen Sie die Variable aus, um die Definition der CSS-Variablen einfach anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="1e1aa-140">Im Beispiel zeigt devtools die CSS-Attribute für das `body` Element an.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="1e1aa-141">Führen Sie die folgenden Aktionen aus, um die Variablendefinition für die `--theme-body-background` CSS-Variable anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-142">Wählen Sie im Bereich **Formatvorlagen** die Option aus `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="1e1aa-143">Im Bereich " **Formatvorlagen** " wird nun die Definition der `--theme-body-background` CSS-Variable angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Mit der Formatvorlage verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="1e1aa-145">Mit der Formatvorlage verknüpfte CSS-Variable</span><span class="sxs-lookup"><span data-stu-id="1e1aa-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Mit Formatvorlagen Ziel verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="1e1aa-147">Mit Formatvorlagen Ziel verknüpfte CSS-Variable</span><span class="sxs-lookup"><span data-stu-id="1e1aa-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1e1aa-148">Verbesserungen des Service Worker-Debuggens</span><span class="sxs-lookup"><span data-stu-id="1e1aa-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="1e1aa-149">Die folgenden neuen Features in den Tools " [Netzwerk](#network-tool)", " [Anwendung](#application-tool)" und " [Quellen](#sources-tool) " unterstützen Sie beim Erstellen Ihrer [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="1e1aa-150">Verwenden Sie die folgenden Features, wenn Probleme beim Debuggen Ihrer Dienstmitarbeiter auftreten können.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="1e1aa-151">Anforderungs Routing zeigt die `startup` und- `fetch` Ereignisse basierend auf den Netzwerkanforderungen an, die von Dienst Mitarbeitern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="1e1aa-152">Der Zugriff auf die Zeitpläne erfolgt entweder über die **Anwendung** oder das **Netzwerk** Tool.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="1e1aa-153">Die Zeitpläne helfen, wenn Sie Probleme mit Servicemitarbeitern haben, und möchten sehen, ob ein Fehler mit dem oder-Ereignis vorliegt `startup` `fetch` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="1e1aa-154">Anwendungstool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="1e1aa-155">Zeigen Sie alle Routinginformationen für Dienstmitarbeiter an, und klicken Sie auf den Link neue **Netzwerkanforderungen** .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="1e1aa-156">Führen Sie die folgenden Aktionen aus, um beim Debuggen des Dienst Arbeitsthreads zusätzlichen Kontext anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-157">Navigieren Sie zu **Anwendungs**  >  **Dienst Mitarbeitern**.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="1e1aa-158">Wählen Sie **Netzwerkanforderungen**aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Öffnen des Tools "Netzwerk" im Bereich "Dienstmitarbeiter"" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="1e1aa-160">Öffnen des Tools " **Netzwerk** " im Bereich " **Dienstmitarbeiter** "</span><span class="sxs-lookup"><span data-stu-id="1e1aa-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="1e1aa-161">Das **Netzwerk** Tool wird im **Einzug** geöffnet und zeigt alle Netzwerkanforderungen für Dienstmitarbeiter an.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="1e1aa-162">Die Netzwerkanforderungen werden mithilfe von gefiltert `is:service-worker-intercepted` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Netzwerktool in der Schublade" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="1e1aa-164">**Netzwerk** Tool in der **Schublade**</span><span class="sxs-lookup"><span data-stu-id="1e1aa-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="1e1aa-165">Wenn Sie das **Netzwerk** Tool an den oberen Bereich zurücksetzen möchten, schließen Sie die **Schublade**.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Schließen der Schublade, um das Netzwerktool zurückzugeben" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="1e1aa-167">Schließen der **Schublade** , um das **Netzwerk** Tool zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="1e1aa-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="1e1aa-168">Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-168">Network tool</span></span>  

<span data-ttu-id="1e1aa-169">Debuggen von Netzwerkanforderungen, die über Dienstmitarbeiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="1e1aa-170">Sie können Netzwerkanforderungen auch über das **Anwendungs** Tool öffnen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="1e1aa-171">Für jede Anforderung zeigen devtools die folgenden Informationen [im Bereich "Anzeigedauer][DevtoolsNetworkReferenceViewTimingBreakdownRequest] " an.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="1e1aa-172">Der Anfang einer Anforderung und die Dauer des Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="1e1aa-173">Änderungen an der Service Worker-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="1e1aa-174">Die Laufzeit eines `fetch` Ereignishandlers.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="1e1aa-175">Die Laufzeit aller `fetch` Ereignisse zum Laden eines Clients.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Bereich "Anzeigedauer"" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="1e1aa-177">Bereich " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="1e1aa-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-178">Quellen Tool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-178">Sources tool</span></span>  

<span data-ttu-id="1e1aa-179">In früheren Versionen von Microsoft Edge war der Grad der Tiefe in der Aufrufliste auf den JavaScript-Code in Ihrem Dienstmitarbeiter limitiert.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="1e1aa-180">In Microsoft Edge 88 zeigt die Aufrufliste nun den Initiator von Anforderungen an, die über Ihren Dienstmitarbeiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="1e1aa-181">Zum Auffinden des Initiators der Anforderung verwenden Sie die Aufrufliste Ihres JavaScript-Codes im Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="1e1aa-182">Die Aufrufliste in den folgenden Zahlen beginnt mit dem JavaScript-Code in Ihrem Dienstmitarbeiter und zeigt einen Verweis auf die ursprüngliche Webanforderungs Seite als an `(index):157` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="1e1aa-183">In der zweiten Abbildung wird der Bezug ausgewählt und der Initiator geöffnet, der die Anforderung gestellt hat.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="1e1aa-184">Der Initiator in der zweiten Abbildung ist die Webseite.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Der service-worker.js Datei-und Aufruf Stapel, der den Absender anfordert" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="1e1aa-186">Der `service-worker.js` Datei-und Aufruf Stapel, der den Absender anfordert</span><span class="sxs-lookup"><span data-stu-id="1e1aa-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Die (Index-) Webseite ist der Anforderungs Initiator" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="1e1aa-188">Die `(index)` Webseite ist der Anforderungs Initiator</span><span class="sxs-lookup"><span data-stu-id="1e1aa-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1e1aa-189">Kopieren des Eigenschaftswerts einer Netzwerkanforderung</span><span class="sxs-lookup"><span data-stu-id="1e1aa-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="1e1aa-190">Kopieren Sie im Tool **Netzwerk** den Eigenschaftswert einer Netzwerkanforderung unter Verwendung der Option neuer **Kopier Wert** .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="1e1aa-191">Der Eigenschaftswert wird als decodierter JSON-Wert kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="1e1aa-192">In früheren Versionen von Microsoft Edge mussten Sie einen Wert mithilfe einer der folgenden Aktionen kopieren.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="1e1aa-193">Markieren Sie den gesamten Text, und kopieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="1e1aa-194">Speichern Sie den Wert als globale Variable (sofern zutreffend), und kopieren Sie Sie aus der devtools- [Konsole][DevtoolsConsoleIndex].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="1e1aa-195">Navigieren Sie zum Kopieren des Eigenschaftswerts in die Zwischenablage, um eine [formatierte Antwort-JSON in die Zwischenablage zu kopieren][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="1e1aa-196">Navigieren Sie zu Issue [1132084][CR1132084], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Kopieren des Eigenschaftswerts in devtools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="1e1aa-198">Kopieren des Eigenschaftswerts in devtools</span><span class="sxs-lookup"><span data-stu-id="1e1aa-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Einfügen des Eigenschaftswerts in Visual Studio-Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="1e1aa-200">Einfügen des Eigenschaftswerts in Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="1e1aa-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="1e1aa-201">Anpassen von Tastenkombinationen für mehrere Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="1e1aa-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="1e1aa-202">[Seit Microsoft Edge, Version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], können Sie Tastenkombinationen für jede Aktion in devtools anpassen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="1e1aa-203">In Microsoft Edge, Version 88, können Sie jetzt Multi-drücken Sie Tastenkombinationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="1e1aa-204">Wenn Sie eine Tastenkombination für eine Aktion im devtools festlegen möchten, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente** , und aktivieren Sie das Kontrollkästchen neben **Tastenkombinationen-Editor aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="1e1aa-205">Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter Aktivieren des Features für den [Tasten Kombinations-Editor][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="1e1aa-206">Die rote Markierung zeigt beispielsweise eine Tastenkombination mit mehreren drücken an, die für die Aktion " **Aufzeichnen von Ereignissen starten** " angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="1e1aa-207">Navigieren Sie zu [Issue #174309][CR174309], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Tastenkombinationen für Akkorde" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="1e1aa-209">Tastenkombinationen für mehrere Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="1e1aa-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="1e1aa-210">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="1e1aa-210">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="1e1aa-211">Neue CSS-Visualisierungstools für Winkel</span><span class="sxs-lookup"><span data-stu-id="1e1aa-211">New CSS angle visualization tools</span></span>  

<span data-ttu-id="1e1aa-212">DevTools unterstützt jetzt das Debuggen von CSS-Winkeln besser.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-212">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="1e1aa-213">Wenn auf der Seite auf einem HTML-Element ein CSS-Winkel angewendet wurde, wird neben dem Winkel im **Formatvorlagen** Tool ein Clock-Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-213">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="1e1aa-214">Wenn Sie die Uhr-Überlagerung umschalten möchten, wählen Sie das Symbol Uhr aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-214">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="1e1aa-215">Wenn Sie den Winkel ändern möchten, wählen Sie eine beliebige Stelle in der Uhr aus, oder ziehen Sie die Nadel.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-215">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="1e1aa-216">Zum Ändern des Winkelwerts können Sie auch Maus-und Tastenkombinationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-216">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="1e1aa-217">Navigieren Sie zu Problemen [1126178][CR1126178] und [1138633][CR1138633], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-217">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="1e1aa-218">Für das Beispiel wird der folgende CSS-Winkel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-218">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="CSS-Winkel" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="1e1aa-220">CSS-Winkel</span><span class="sxs-lookup"><span data-stu-id="1e1aa-220">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-221">Simulieren der Speicherkontingent Größe im Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="1e1aa-221">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="1e1aa-222">Sie können jetzt die Größe des Speicherkontingents im **Speicher** Bereich außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-222">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="1e1aa-223">Dieses Feature ermöglicht es Ihnen, verschiedene Geräte zu simulieren und das Verhalten Ihrer Website oder app in Szenarien mit geringer Verfügbarkeit zu testen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-223">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="1e1aa-224">Führen Sie die folgenden Aktionen aus, um das Speicherkontingent zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-224">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-225">Navigieren Sie zum **Anwendungs**  >  **Speicher**.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-225">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="1e1aa-226">Aktivieren Sie das Kontrollkästchen **benutzerdefinierten Speicherkontingent simulieren** .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-226">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="1e1aa-227">Geben Sie eine gültige Nummer ein.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-227">Enter a valid number.</span></span>  
    
<span data-ttu-id="1e1aa-228">Weitere Informationen zum Emulieren von mobilen Geräten und anderen Features in der devtools finden Sie unter [emulieren von mobilen Geräten in Microsoft Edge devtools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-228">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="1e1aa-229">Navigieren Sie zu Problemen [945786][CR945786] und [1146985][CR1146985], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-229">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simulieren der Speicherkontingent Größe" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="1e1aa-231">Simulieren der Speicherkontingent Größe</span><span class="sxs-lookup"><span data-stu-id="1e1aa-231">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-232">Melden von CORS-Fehlern im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="1e1aa-232">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="1e1aa-233">Testen Sie diese Funktion, indem Sie zur [CORS-Fehler Demo][GlitchCorsErrors]navigieren.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-233">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="1e1aa-234">Öffnen Sie das Tool **Netzwerk** , aktualisieren Sie die Seite, und beobachten Sie die fehlerhafte CORS-Netzwerkanforderung.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-234">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="1e1aa-235">In der Spalte Status wird der **CORS-Fehler**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-235">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="1e1aa-236">Wenn Sie auf den Fehler zeigen, wird in der QuickInfo nun der Fehlercode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-236">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="1e1aa-237">In Microsoft Edge, Version 87 und früheren Versionen, devtools nur den generischen **(fehlerhaften)** Status für CORS-Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-237">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="1e1aa-238">Navigieren Sie zu Issue [1141824][CR1141824], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-238">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="CORS-Fehler" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="1e1aa-240">CORS-Fehler</span><span class="sxs-lookup"><span data-stu-id="1e1aa-240">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-241">Frame Details-Ansicht Updates</span><span class="sxs-lookup"><span data-stu-id="1e1aa-241">Frame details view updates</span></span>  

#### <span data-ttu-id="1e1aa-242">Informationen zur übergreifenden Isolierung in der Ansicht "Frame Details"</span><span class="sxs-lookup"><span data-stu-id="1e1aa-242">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="1e1aa-243">Der übergreifende isolierte Status wird nun unter dem Abschnitt **Sicherheit & Isolierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-243">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="1e1aa-244">Im Abschnitt neue **API-Verfügbarkeit** werden die Verfügbarkeit von `SharedArrayBuffer` s \ (SAB \) und die Angabe, ob die Puffer freigegeben werden können, angezeigt `postMessage()` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-244">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="1e1aa-245">Eine veraltete Warnung wird angezeigt, wenn das SAB-Element und `postMessage()` derzeit verfügbar ist, der Kontext aber nicht über eine isolierte Herkunft verfügt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-245">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="1e1aa-246">`SharedArrayBuffers`Navigieren Sie zu [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated], wenn Sie weitere Informationen zur isolierten Ursprungs Isolierung benötigen und warum Sie für Features wie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-246">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="1e1aa-247">Navigieren Sie zu Issue [1139899][CR1139899], um Echtzeitupdates dieser Funktion im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-247">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informationen über einen anderen Ursprung" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="1e1aa-249">Informationen über einen anderen Ursprung</span><span class="sxs-lookup"><span data-stu-id="1e1aa-249">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="1e1aa-250">Neue Web Worker-Informationen in der Ansicht "Frame Details"</span><span class="sxs-lookup"><span data-stu-id="1e1aa-250">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="1e1aa-251">DevTools organisiert nun Web-Worker unter dem entsprechenden übergeordneten Frame.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-251">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="1e1aa-252">Beispiel: Wenn der `someName` Frame erstellt wird `worker.js` , `worker.js` wird unter `someName` in der Liste **Frames** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-252">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="1e1aa-253">Führen Sie die folgenden Aktionen aus, um die Details des Web Worker anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-253">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-254">Öffnen Sie das **Anwendungs** Tool.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-254">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="1e1aa-255">Erweitern Sie einen Frame, der Web Workers enthält.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-255">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="1e1aa-256">Erweitern Sie die **Worker** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-256">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="1e1aa-257">Wählen Sie eine Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-257">Choose a worker.</span></span>  
    
<span data-ttu-id="1e1aa-258">Navigieren Sie zu Problemen [1122507][CR1122507] und [1051466][CR1051466], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-258">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informationen für Web-Worker" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="1e1aa-260">Informationen für Web-Worker</span><span class="sxs-lookup"><span data-stu-id="1e1aa-260">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="1e1aa-261">Anzeigen von Details zum Öffnen des Frames für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="1e1aa-261">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="1e1aa-262">DevTools organisiert nun geöffnete [Fenster][MdnWindowConstructors] unter dem relevanten übergeordneten [Frame][MdnWindowFrames].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-262">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="1e1aa-263">Wenn beispielsweise der `top` Frame a an geöffnet `Window` wird `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , `Window` wird unter `top` in der Liste **Frames** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-263">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="1e1aa-264">Führen Sie die folgenden Aktionen aus, um den Frame anzuzeigen, der für das Öffnen eines anderen Fensters im **Element** Tool verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-264">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-265">Öffnen Sie die **Frame** Struktur.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-265">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="1e1aa-266">Erweitern Sie **geöffnete Fenster** , und wählen `Window` Sie den für den übergeordneten Frame aus, den Sie wissen möchten.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-266">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="1e1aa-267">Wählen Sie den Link **öffnender Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-267">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="1e1aa-268">Die Details werden angezeigt, in welchem Frame die Eröffnung eines anderen verursacht wurde `Window` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-268">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="1e1aa-269">Führen Sie die folgenden Aktionen aus, um den Öffner im **Element** -Tool anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-269">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-270">Öffnen Sie die **Frame** Struktur.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-270">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="1e1aa-271">Wählen Sie ein geöffnetes Fenster aus, um die Details zu öffnen `Window` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-271">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="1e1aa-272">Wählen Sie den Link **öffnender Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-272">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="1e1aa-273">Navigieren Sie zu Issue [1107766][CR1107766], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Details zum geöffneten Frame" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="1e1aa-275">Details zum geöffneten Frame</span><span class="sxs-lookup"><span data-stu-id="1e1aa-275">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-276">Kopieren von StackTrace für den Netzwerk Initiator</span><span class="sxs-lookup"><span data-stu-id="1e1aa-276">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="1e1aa-277">Führen Sie die folgenden Aktionen aus, um den StackTrace in Ihre Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-277">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e1aa-278">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="1e1aa-278">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="1e1aa-279">Wählen **Copy**Sie Copy  >  **StackTrace**kopieren aus.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-279">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="1e1aa-280">Navigieren Sie zu Issue [1139615][CR1139615], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Kopieren von StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="1e1aa-282">Kopieren von StackTrace</span><span class="sxs-lookup"><span data-stu-id="1e1aa-282">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-283">Vorschau von WASM-Variablenwert bei Mouseover</span><span class="sxs-lookup"><span data-stu-id="1e1aa-283">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="1e1aa-284">Verwenden Sie dieses Feature, um den Wert einer Webassembly \ (WASM \)-Variablen zu überprüfen, wenn der Code angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-284">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="1e1aa-285">Um den aktuellen Wert einer Variablen anzuzeigen, zeigen Sie auf eine Variable.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-285">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="1e1aa-286">Navigieren Sie zu Problemen [1058836][CR1058836] und [1071432][CR1071432], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-286">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vorschau WASM-Variable bei Mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="1e1aa-288">Vorschau WASM-Variable bei Mouseover</span><span class="sxs-lookup"><span data-stu-id="1e1aa-288">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="1e1aa-289">Einheitliche Maßeinheiten für die Größe von Dateien und Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="1e1aa-289">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="1e1aa-290">DevTools wird jetzt immer wieder verwendet `kB` , um die Größe von Dateien und Arbeitsspeicher anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-290">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="1e1aa-291">Zuvor devtools Mixed `kB` und `KiB` .</span><span class="sxs-lookup"><span data-stu-id="1e1aa-291">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="1e1aa-292">oder Kilobyte \ (10 ^ 3 oder 1000 Bytes \)</span><span class="sxs-lookup"><span data-stu-id="1e1aa-292">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="1e1aa-293">oder Kibibyte \ (2 ^ 10 oder 1024 Bytes \)</span><span class="sxs-lookup"><span data-stu-id="1e1aa-293">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="1e1aa-294">Beispiel: das **Netzwerk** Tool, das zuvor `kB` in den Etiketten verwendet, aber `KiB` in Berechnungen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-294">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="1e1aa-295">Ihr Feedback hat gezeigt, dass diese Inkonsistenz Verwirrung verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-295">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="1e1aa-296">Navigieren Sie zu Issue [1035309][CR1035309], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-296">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="1e1aa-297">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="1e1aa-297">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="1e1aa-298">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview Channels] [MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-298">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="1e1aa-299">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-299">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="1e1aa-300">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="1e1aa-300">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "3D-Ansicht | Microsoft docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Übersicht über die Konsole | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Tasten Kombinations-Editors – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Aktivieren von zusammengesetzten Layern in der 3D-Ansicht – experimentelle Features | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Kopieren der formatierten Antwort JSON in die Zwischenablage – Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Anzeigen der zeitlichen Aufschlüsselung einer Anforderung – Netzwerkanalyse Referenz | Microsoft docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Verwenden von WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows | Microsoft docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Anpassen von Tastenkombinationen in Einstellungen-Neuerungen in devtools (Microsoft Edge 87) | Microsoft docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "webhint-Feedback im Bereich "Probleme" – Neuerungen in devtools (Microsoft Edge 85) | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "WebDriver herunterladen | Microsoft-Entwickler"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Herunterladen von Microsoft Edge-Insider Kanälen"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio-Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR174309]: https://crbug.com/174309 "Problem 174309: devtools: zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chrom Fehler"  
[CR945786]: https://crbug.com/945786 "Problem 945786: devtools: zulassen des Überschreibens von Navigator. Storage. Estimate () | Chrom Fehler"  
[CR1029427]: https://crbug.com/1029427 "Problem 1029427: Reduzieren des Performance-Overhead beim Protokollnachrichten Versand im Front-End | Chrom Fehler"  
[CR1035309]: https://crbug.com/1035309 "Problem 1035309: devtools sollte konsistent MB verwenden, um Megabyte zu bedeuten, nicht Mebibyte | Chrom Fehler"  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: unterstützen des Coop/COEP-Debuggens in devtools | Chrom Fehler"  
[CR1058836]: https://crbug.com/1058836 "Problem 1058836: UX-Probleme rund um das WASM-Debuggen | Chrom Fehler"  
[CR1071432]: https://crbug.com/1071432 "Problem 1071432: ☂️ WASM Basic Developer Experience | Chrom Fehler"  
[CR1107766]: https://crbug.com/1107766 "Problem 1107766: zeigt Informationen zu Frames an, die von "Window. Open ()" in der Frame Struktur generiert wurden | Chrom Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Surface Worker-Informationen in der Frame Strukturansicht | Chrom Fehler"  
[CR1126178]: https://crbug.com/1126178 "Problem 1126178: ☂ devtools: CSS <Typ> Komponenten | Chrom Fehler"  
[CR1130556]: https://crbug.com/1130556 "Problem 1130556: devtools: Testen von Bild Fallbacks (Emulation) | Chrom Fehler"  
[CR1132084]: https://crbug.com/1132084 "Problem 1132084: keine einfache Möglichkeit zum Kopieren von JSON-Anforderungsnutzlast | Chrom Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chrom Fehler"  
[CR1138633]: https://crbug.com/1138633 "Problem 1138633: devtools: CSS <Winkel> Komponente sollte das Erscheinungsbild Ihrer Eigenschaft im Hintergrund der Uhr widerspiegeln | Chrom Fehler"  
[CR1139615]: https://crbug.com/1139615 "Problem 1139615: Netzwerk Initiator sollte die Möglichkeit bieten, die Stapelüberwachung zu kopieren | Chrom Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame Detailansicht | Chrom Fehler"  
[CR1139945]: https://crbug.com/1139945 "Problem 1139945: Symbole für Flexbox-CSS-Eigenschaften im Bereich "Formatvorlagen" | Chrom Fehler"  
[CR1141824]: https://crbug.com/1141824 "Problem 1141824: verbessern der CORS-Fehlerberichterstattung in devtools | Chrom Fehler"  
[CR1144090]: https://crbug.com/1144090 "Problem 1144090: Hinzufügen von Flex-Stil Adornern zur Elementstruktur | Chrom Fehler"  
[CR1146985]: https://crbug.com/1146985 "Problem 1146985: der gelöschte Text wird weiterhin im Textfeld "Speicher" im Abschnitt "dev tools" angezeigt | Chrom Fehler"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "CORS-Fehler | Glitch"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Übergreifende Ressourcenfreigabe (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Konstruktoren – Fenster | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. Frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Barrierefreiheit | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Kompatibilität | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Leistung | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Fallstricke | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sicherheit | webhint"  

> [!NOTE]
> <span data-ttu-id="1e1aa-351">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-351">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1e1aa-352">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/11/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e1aa-352">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="1e1aa-354">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e1aa-354">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
