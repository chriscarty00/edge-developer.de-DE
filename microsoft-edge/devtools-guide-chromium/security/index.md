---
title: Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611910"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="5cdc2-103">Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="5cdc2-103">Understand Security Issues With Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="5cdc2-104">Öffnen des Fensters "Sicherheit"</span><span class="sxs-lookup"><span data-stu-id="5cdc2-104">Open the Security panel</span></span>   

<span data-ttu-id="5cdc2-105">Der Bereich " **Sicherheit** " ist der wichtigste Ort in devtools, um die Sicherheit einer Seite zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="5cdc2-106">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="5cdc2-106">[Open DevTools][DevToolsOpen].</span></span>  

1.  <span data-ttu-id="5cdc2-107">Klicken Sie auf die Registerkarte **Sicherheit** , um das **Sicherheits** Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    > ##### <span data-ttu-id="5cdc2-108">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="5cdc2-108">Figure 1</span></span>  
    > <span data-ttu-id="5cdc2-109">Das Sicherheitspanel</span><span class="sxs-lookup"><span data-stu-id="5cdc2-109">The Security panel</span></span>  
    > ![Das Sicherheitspanel][ImageSecurityPanel]  
    
## <span data-ttu-id="5cdc2-111">Häufig auftretende Probleme</span><span class="sxs-lookup"><span data-stu-id="5cdc2-111">Common problems</span></span>   

### <span data-ttu-id="5cdc2-112">Nicht sichere Haupt Ursprünge</span><span class="sxs-lookup"><span data-stu-id="5cdc2-112">Non-secure main origins</span></span>   

<span data-ttu-id="5cdc2-113">Wenn der Haupt Ursprung einer Seite nicht sicher ist, lautet die **Sicherheitsübersicht** , dass **Diese Seite nicht sicher ist**.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

> ##### <span data-ttu-id="5cdc2-114">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="5cdc2-114">Figure 2</span></span>  
> <span data-ttu-id="5cdc2-115">Eine nicht sichere Seite</span><span class="sxs-lookup"><span data-stu-id="5cdc2-115">A non-secure page</span></span>  
> ![Eine nicht sichere Seite][ImageNonSecurePage]  

<span data-ttu-id="5cdc2-117">Dieses Problem tritt auf, wenn die URL, die Sie besucht haben, über HTTP angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-117">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="5cdc2-118">Um die Sicherheit zu gewährleisten, müssen Sie Sie über HTTPS anfordern.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-118">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="5cdc2-119">Wenn Sie beispielsweise die URL in der Adressleiste betrachten, sieht Sie wahrscheinlich ähnlich aus `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="5cdc2-119">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="5cdc2-120">Um die URL zu sichern, sollte die URL `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="5cdc2-120">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="5cdc2-121">Wenn Sie bereits HTTPS auf dem Server eingerichtet haben, müssen Sie lediglich den Server so konfigurieren, dass alle HTTP-Anforderungen an https umgeleitet werden, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-121">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="5cdc2-122">Wenn Sie HTTPS auf dem Server nicht eingerichtet haben, können Sie durch [verschlüsseln][LetsEncrypt] eine ﻿kostenlose und relativ einfache Möglichkeit zum Starten des Prozesses bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-122">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="5cdc2-123">Oder Sie können das Hosten Ihrer Website in einem CDN in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-123">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="5cdc2-124">Die meisten wichtigen CDNs-Host Websites sind jetzt standardmäßig auf HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-124">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="5cdc2-125">Der [use https][WebhintUseHttps] -Hinweis in [webhint][Webhint] kann dazu beitragen, den Vorgang zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an https weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-125">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="5cdc2-126">Gemischter Inhalt</span><span class="sxs-lookup"><span data-stu-id="5cdc2-126">Mixed content</span></span>   

<span data-ttu-id="5cdc2-127">**Gemischte Inhalte** bedeuten, dass der Haupt Ursprung einer Seite sicher ist, die Seite jedoch Ressourcen von nicht sicheren Ursprüngen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-127">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="5cdc2-128">Gemischte Inhaltsseiten sind nur teilweise geschützt, da der HTTP-Inhalt für Sniffer zugänglich und anfällig für man-in-the-Middle-Angriffe ist.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-128">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

> ##### <span data-ttu-id="5cdc2-129">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="5cdc2-129">Figure 3</span></span>  
> <span data-ttu-id="5cdc2-130">Gemischter Inhalt</span><span class="sxs-lookup"><span data-stu-id="5cdc2-130">Mixed content</span></span>  
> ![Gemischter Inhalt][ImageMixedContent]  

<span data-ttu-id="5cdc2-132">Klicken Sie in [Abbildung 3](#figure-3)auf **Ansicht 1 Anforderung in der Netzwerksteuerung** , um das **Netzwerk** Panel zu öffnen und den Filter anzuwenden, `mixed-content:displayed` damit im **Netzwerkprotokoll** nur nicht sichere Ressourcen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-132">In [Figure 3](#figure-3), click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

> ##### <span data-ttu-id="5cdc2-133">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="5cdc2-133">Figure 4</span></span>  
> <span data-ttu-id="5cdc2-134">Gemischte Ressourcen im Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="5cdc2-134">Mixed resources in the Network Log</span></span>  
> ![Gemischte Ressourcen im Netzwerkprotokoll][ImageMixedResourcesNetworkLog]  

## <span data-ttu-id="5cdc2-136">Details anzeigen</span><span class="sxs-lookup"><span data-stu-id="5cdc2-136">View details</span></span>   

### <span data-ttu-id="5cdc2-137">Haupt Ursprungszertifikat anzeigen</span><span class="sxs-lookup"><span data-stu-id="5cdc2-137">View main origin certificate</span></span>   

<span data-ttu-id="5cdc2-138">Klicken Sie in der **Sicherheitsübersicht**auf **Zertifikat anzeigen** , um das Zertifikat schnell auf den Haupt Ursprung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-138">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

> ##### <span data-ttu-id="5cdc2-139">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="5cdc2-139">Figure 5</span></span>  
> <span data-ttu-id="5cdc2-140">Ein Haupt Ursprungszertifikat</span><span class="sxs-lookup"><span data-stu-id="5cdc2-140">A main origin certificate</span></span>  
> ![Ein Haupt Ursprungszertifikat][ImageCertificate]  

### <span data-ttu-id="5cdc2-142">Anzeigen von Ursprungs Details</span><span class="sxs-lookup"><span data-stu-id="5cdc2-142">View origin details</span></span>   

<span data-ttu-id="5cdc2-143">Klicken Sie auf einen der Einträge im Navigationsbereich auf der linken Seite, um die Details des Ursprungs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-143">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="5cdc2-144">Auf der Seite "Details" können Sie die Verbindungs-und Zertifikatinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-144">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="5cdc2-145">Die Informationen zur Transparenz der Zertifikate werden ebenfalls angezeigt, wenn Sie verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-145">Certificate transparency information is also shown when available.</span></span>  

> ##### <span data-ttu-id="5cdc2-146">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="5cdc2-146">Figure 6</span></span>  
> <span data-ttu-id="5cdc2-147">Details des Haupt Ursprungs</span><span class="sxs-lookup"><span data-stu-id="5cdc2-147">Main origin details</span></span>  
> ![Details des Haupt Ursprungs][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Abbildung 1: das Sicherheitspanel"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Abbildung 2: eine nicht sichere Seite"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Abbildung 3: gemischter Inhalt"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Abbildung 4: gemischte Ressourcen im Netzwerkprotokoll"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Abbildung 5: ein Haupt Ursprungszertifikat"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Abbildung 6: Details des Haupt Ursprungs"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  


[LetsEncrypt]: https://letsencrypt.org "Verschlüsseln-﻿kostenlose SSL/TLS-Zertifikate"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Verwenden von HTTPS | webhint-Dokumentation"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="5cdc2-160">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-160">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5cdc2-161">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/security/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5cdc2-161">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="5cdc2-163">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5cdc2-163">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
