---
description: Verwenden Sie das Tool Probleme, um Probleme mit Ihrer Website zu finden und zu beheben.
title: Suchen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e16bd926ea5bae35ad82f54ac5d1ae2028e3c59d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398974"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a><span data-ttu-id="5ad8c-104">Suchen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool</span><span class="sxs-lookup"><span data-stu-id="5ad8c-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="5ad8c-105">Das **Tool Probleme** in Microsoft Edge DevTools reduziert die Benachrichtigungsermüdung und Unübersichtlichkeit der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="5ad8c-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="5ad8c-106">Verwenden Sie es, um Lösungen für probleme zu finden, die vom Browser erkannt werden, z. B. Cookieprobleme und gemischte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="5ad8c-107">In Microsoft Edge 84 unterstützt das **Problemtool** drei Arten von Problemen:</span><span class="sxs-lookup"><span data-stu-id="5ad8c-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="5ad8c-108">Cookieprobleme</span><span class="sxs-lookup"><span data-stu-id="5ad8c-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="5ad8c-109">Gemischte Inhalte</span><span class="sxs-lookup"><span data-stu-id="5ad8c-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="5ad8c-110">COEP-Probleme</span><span class="sxs-lookup"><span data-stu-id="5ad8c-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="5ad8c-111">Das Microsoft Edge DevTools-Team plant, weitere Problemtypen in zukünftigen Versionen von Microsoft Edge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="5ad8c-112">Öffnen Sie das Tool Probleme in der DevTools-Schublade.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="5ad8c-113">Navigieren Sie zu einer Webseite, [z. B. samesite-sandbox.glitch.me][GlitchSamesiteSandbox], die zu behebende Probleme enthält.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-113">Navigate to a webpage, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="5ad8c-114">[Öffnen Sie DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5ad8c-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="5ad8c-115">Klicken Sie **in der gelben** Warnleiste auf die Schaltfläche Zu Probleme wechseln.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Wechseln Sie zu Schaltfläche Probleme in der gelben Warnleiste, wenn Probleme erkannt werden" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="5ad8c-117">Die **Schaltfläche Zu Probleme** wechseln in der gelben Warnleiste, wenn Probleme erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="5ad8c-118">Alternativ wählen Sie **im Menü** Weitere Tools die Option **Probleme** aus.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Problemtool im Menü Weitere Tools" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="5ad8c-120">**Problemtool** im **Menü Weitere** Tools</span><span class="sxs-lookup"><span data-stu-id="5ad8c-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="5ad8c-121">Wählen Sie **bei Bedarf die** Schaltfläche Seite laden aus.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-121">Choose the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Problemtool in der DevTools Drawer with Reload page button" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="5ad8c-123">**Problemtool** in der DevTools Drawer with **Reload page button**</span><span class="sxs-lookup"><span data-stu-id="5ad8c-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="5ad8c-124">Die in der Konsole **gemeldeten** Probleme sind schwer zu verstehen, z. B. die Cookiewarnungen in der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="5ad8c-125">Basierend auf den gemeldeten Problemen ist möglicherweise nicht klar, was Sie tun müssen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Problemtool in der DevTools-Drawer mit drei Cookieproblemen" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="5ad8c-127">**Problemtool** in der DevTools-Drawer mit drei Cookieproblemen</span><span class="sxs-lookup"><span data-stu-id="5ad8c-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a><span data-ttu-id="5ad8c-128">Anzeigen von Elementen im Problemtool</span><span class="sxs-lookup"><span data-stu-id="5ad8c-128">View items in the Issues tool</span></span>  

<span data-ttu-id="5ad8c-129">Das **Tool Probleme** in der DevTools-Drawer stellt Warnungen strukturiert, aggregiert und aktionensfähig zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="5ad8c-130">Wählen Sie ein Element im **Tool Probleme** aus, um Anleitungen zum Beheben des Problems und zum Suchen betroffener Ressourcen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-130">Choose an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Markieren von websiteübergreifenden Cookies als sicheres Problem, das im Problemtool geöffnet ist" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="5ad8c-132">**Markieren von websiteübergreifenden Cookies als sicheres** Problem, das im **Problemtool geöffnet** ist</span><span class="sxs-lookup"><span data-stu-id="5ad8c-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="5ad8c-133">Jedes Element besteht aus vier Komponenten:</span><span class="sxs-lookup"><span data-stu-id="5ad8c-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="5ad8c-134">Eine Überschrift, die das Problem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="5ad8c-135">Eine Beschreibung, die den Kontext und die Lösung enthält.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="5ad8c-136">Ein **ABSCHNITT "AFFECTED RESOURCES",** der Mit Ressourcen im entsprechenden DevTools-Kontext wie dem Netzwerkbereich verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="5ad8c-137">Links zu weiteren Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="5ad8c-138">Wählen Sie Elemente in **AFFECTED RESOURCES aus,** um Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-138">Choose items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="5ad8c-139">Im folgenden Beispiel wirkt sich das Problem **"Websiteübergreifende Cookies** als Sicher markieren" auf ein Cookie und zwei Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Betroffene Ressourcen im Problemtool geöffnet" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="5ad8c-141">Betroffene Ressourcen werden im Tool **Probleme** in der DevTools-Schublade geöffnet</span><span class="sxs-lookup"><span data-stu-id="5ad8c-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a><span data-ttu-id="5ad8c-142">Anzeigen von Problemen im Kontext</span><span class="sxs-lookup"><span data-stu-id="5ad8c-142">View issues in context</span></span>  

1.  <span data-ttu-id="5ad8c-143">Wählen Sie einen Ressourcenlink aus, um das Element im entsprechenden Kontext in DevTools zu sehen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-143">Choose a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="5ad8c-144">Wählen Sie im folgenden Beispiel unter Anforderungen die Cookies aus, die `samesite-sandbox.glitch.me` dieser Anforderung zugeordnet sind. </span><span class="sxs-lookup"><span data-stu-id="5ad8c-144">In the following example, choose `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Anzeigen des betroffenen Cookies im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="5ad8c-146">Anzeigen des betroffenen Cookies im **DevTools-Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="5ad8c-146">View the affected cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="5ad8c-147">Scrollen Sie, um das Element mit einem Problem zu sehen: für das folgende Beispiel das `ck02` Cookie.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-147">Scroll to view the item with a problem:  for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="5ad8c-148">Zeigen Sie auf die **Spalte SameSite,** um den vom Problem `None` erkannten Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-148">Hover on the **SameSite** column to review the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Kein Wert in der Spalte SameSite für das ck02-Cookie im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="5ad8c-150">Wert in der **Spalte SameSite** für das `ck02` Cookie im **DevTools-Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="5ad8c-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5ad8c-151">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="5ad8c-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "SameSite-Cookietests | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite-Cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Gemischte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Cross-Origin Embedder Policy | Web Incubator Community Group"  

> [!NOTE]
> <span data-ttu-id="5ad8c-157">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5ad8c-158">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) und wird von [Sam Dutton][SamDutton] \(Developer Advocate\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5ad8c-160">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5ad8c-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
