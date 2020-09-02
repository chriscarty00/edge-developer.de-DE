---
title: Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d837723ed68c6d088e7b345ae86c7a0312b46496
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986129"
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

# <span data-ttu-id="cc803-103">Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool</span><span class="sxs-lookup"><span data-stu-id="cc803-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="cc803-104">Das **Problem** Tool in Microsoft Edge devtools verringert die Ermüdung der Benachrichtigung und die unaufgeräumtheit der **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="cc803-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="cc803-105">Verwenden Sie es, um Lösungen für vom Browser erkannte Probleme zu finden, wie etwa Cookie-Probleme und gemischte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="cc803-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="cc803-106">In Microsoft Edge 84 unterstützt das **Issues** -Tool drei Arten von Problemen:</span><span class="sxs-lookup"><span data-stu-id="cc803-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="cc803-107">Cookie-Probleme</span><span class="sxs-lookup"><span data-stu-id="cc803-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="cc803-108">Gemischter Inhalt</span><span class="sxs-lookup"><span data-stu-id="cc803-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="cc803-109">COEP-Probleme</span><span class="sxs-lookup"><span data-stu-id="cc803-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="cc803-110">Das Microsoft Edge devtools-Team plant, weitere Problemtypen in zukünftigen Versionen von Microsoft Edge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cc803-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="cc803-111">Öffnen des Tools "Probleme" im devtools-Einzug</span><span class="sxs-lookup"><span data-stu-id="cc803-111">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="cc803-112">Besuchen Sie eine Seite wie [SameSite-Sandbox.Glitch.me][GlitchSamesiteSandbox], die Probleme enthält, die behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="cc803-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="cc803-113">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="cc803-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="cc803-114">Klicken Sie auf der gelben Warnleiste auf die Schaltfläche **Gehe zu Problemen** .</span><span class="sxs-lookup"><span data-stu-id="cc803-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Schaltfläche ' Probleme ' in der gelben Warnleiste, wenn Probleme erkannt werden" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="cc803-116">Die Schaltfläche " **Probleme wechseln** " in der gelben Warnleiste, wenn Probleme erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="cc803-116">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="cc803-117">Sie können auch im Menü **Weitere Tools** die Option **Probleme** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cc803-117">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Tool ' Probleme ' im Menü ' Weitere Tools '" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="cc803-119">Tool ' **Probleme** ' im Menü ' **Weitere Tools** '</span><span class="sxs-lookup"><span data-stu-id="cc803-119">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="cc803-120">Wählen Sie bei Bedarf die Schaltfläche **Seite neu laden** aus.</span><span class="sxs-lookup"><span data-stu-id="cc803-120">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Tool ' Probleme ' in der devtools-Schublade mit der Schaltfläche ' Seite neu laden '" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="cc803-122">Tool ' **Probleme** ' in der devtools-Schublade mit der Schaltfläche ' **Seite neu laden** '</span><span class="sxs-lookup"><span data-stu-id="cc803-122">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="cc803-123">Die in der **Konsole** gemeldeten Probleme sind schwer verständlich, wie etwa die Cookie-Warnungen in der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="cc803-123">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="cc803-124">Basierend auf den gemeldeten Problemen ist es möglicherweise nicht klar, was Sie tun müssen.</span><span class="sxs-lookup"><span data-stu-id="cc803-124">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Tool "Probleme" im devtools-Einzug mit drei Problemen mit Cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="cc803-126">Tool " **Probleme** " im devtools-Einzug mit drei Problemen mit Cookies</span><span class="sxs-lookup"><span data-stu-id="cc803-126">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="cc803-127">Anzeigen von Elementen im Tool "Probleme"</span><span class="sxs-lookup"><span data-stu-id="cc803-127">View items in the Issues tool</span></span>  

<span data-ttu-id="cc803-128">Das Tool " **Probleme** " im devtools-Einzug zeigt Warnungen auf strukturierter, aggregierter und umsetzbarer Weise an.</span><span class="sxs-lookup"><span data-stu-id="cc803-128">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="cc803-129">Wählen Sie ein Element im **Issues** -Tool aus, um Anleitungen zur Behebung des Problems und zum Auffinden betroffener Ressourcen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cc803-129">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Markieren von websiteübergreifenden Cookies als sicheres Problem im Tool "Probleme"" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="cc803-131">**Markieren von websiteübergreifenden Cookies als sicheres** Problem im Tool " **Probleme** "</span><span class="sxs-lookup"><span data-stu-id="cc803-131">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="cc803-132">Jedes Element verfügt über vier Komponenten:</span><span class="sxs-lookup"><span data-stu-id="cc803-132">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="cc803-133">Eine Überschrift, die das Problem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cc803-133">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="cc803-134">Eine Beschreibung, die den Kontext und die Lösung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cc803-134">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="cc803-135">Ein Abschnitt " **betroffene Ressourcen** ", der Links zu Ressourcen im entsprechenden devtools-Kontext wie dem Netzwerk Panel enthält.</span><span class="sxs-lookup"><span data-stu-id="cc803-135">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="cc803-136">Links zu weiteren Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="cc803-136">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="cc803-137">Wählen Sie Elemente in **betroffenen Ressourcen** aus, um Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cc803-137">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="cc803-138">Im folgenden Beispiel wirkt sich das **kennzeichnen von websiteübergreifenden Cookies als sicheres** Problem auf ein Cookie und zwei Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="cc803-138">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Auf der Registerkarte "Issues Drawer" geöffnete betroffene Ressourcen" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="cc803-140">Im Tool " **Probleme** " im devtools-Einzug geöffnete betroffene Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cc803-140">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="cc803-141">Anzeigen von Problemen im Kontext</span><span class="sxs-lookup"><span data-stu-id="cc803-141">View issues in context</span></span>  

1.  <span data-ttu-id="cc803-142">Wählen Sie einen Ressourcen Link aus, um das Element im entsprechenden Kontext in devtools anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cc803-142">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="cc803-143">Wählen Sie im folgenden Beispiel `samesite-sandbox.glitch.me` unter **Anforderungen** aus, um die Cookies anzuzeigen, die dieser Anforderung angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="cc803-143">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Anzeigen des betroffenen Cookies im devtools-Netzwerk Panel" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="cc803-145">Anzeigen des betroffenen Cookies im devtools- **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="cc803-145">View the affected cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="cc803-146">Scrollen Sie, um das Element mit einem Problem anzuzeigen: im folgenden Beispiel wird das `ck02` Cookie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc803-146">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="cc803-147">Zeigen Sie mit der Maus auf die Spalte **SameSite** , um den `None` Wert anzuzeigen, der vom Problem erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="cc803-147">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Kein Wert in der Spalte "SameSite" für das ck02-Cookie im devtools-Netzwerk Panel" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="cc803-149">Wert in der Spalte " **SameSite** " für das `ck02` Cookie im devtools- **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="cc803-149">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

## <span data-ttu-id="cc803-150">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="cc803-150">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "SameSite-Cookie-Tests | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite Cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Gemischter Inhalt | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Richtlinien für die übergreifende Einbettung | Webinkubator-Community-Gruppe"  

> [!NOTE]
> <span data-ttu-id="cc803-156">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc803-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cc803-157">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) gefunden und von [Sam Dutton][SamDutton] (Entwickler Anwalt \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cc803-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cc803-159">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cc803-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
