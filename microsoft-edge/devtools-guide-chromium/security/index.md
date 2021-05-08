---
description: Verwenden Sie den Sicherheitsbereich, um sicherzustellen, dass eine Seite vollständig durch HTTPS geschützt ist.
title: Verstehen von Sicherheitsproblemen mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397776"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a><span data-ttu-id="00880-104">Verstehen von Sicherheitsproblemen mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="00880-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a><span data-ttu-id="00880-105">Öffnen des Sicherheitsbereichs</span><span class="sxs-lookup"><span data-stu-id="00880-105">Open the Security panel</span></span>  

<span data-ttu-id="00880-106">Der **Sicherheitsbereich** ist der Hauptort in DevTools für die Überprüfung der Sicherheit einer Seite.</span><span class="sxs-lookup"><span data-stu-id="00880-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="00880-107">[Öffnen Sie DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="00880-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="00880-108">Wählen Sie die **Registerkarte Sicherheit** aus, um das **Sicherheitstool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="00880-108">Choose the **Security** tab to open the **Security** tool.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Der Sicherheitsbereich" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="00880-110">Der **Sicherheitsbereich**</span><span class="sxs-lookup"><span data-stu-id="00880-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <a name="common-problems"></a><span data-ttu-id="00880-111">Häufige Probleme</span><span class="sxs-lookup"><span data-stu-id="00880-111">Common problems</span></span>  

### <a name="non-secure-main-origins"></a><span data-ttu-id="00880-112">Nicht sichere Hauptherkunft</span><span class="sxs-lookup"><span data-stu-id="00880-112">Non-secure main origins</span></span>  

<span data-ttu-id="00880-113">Wenn der Hauptherkunft einer Seite \*\*\*\* nicht sicher ist, heißt es in der Sicherheitsübersicht, **dass diese Seite nicht sicher ist.**</span><span class="sxs-lookup"><span data-stu-id="00880-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Eine nicht sichere Seite" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="00880-115">Eine nicht sichere Seite</span><span class="sxs-lookup"><span data-stu-id="00880-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="00880-116">Dieses Problem tritt auf, wenn die url, die Sie besucht haben, über HTTP angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="00880-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="00880-117">Um die Sicherheit zu gewährleisten, müssen Sie sie über HTTPS anfordern.</span><span class="sxs-lookup"><span data-stu-id="00880-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="00880-118">Wenn Sie sich beispielsweise die URL in der Adressleiste anschauen, sieht sie wahrscheinlich ähnlich aus wie `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="00880-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="00880-119">Um die Sicherheit zu gewährleisten, sollte die URL `https://example.com` sein.</span><span class="sxs-lookup"><span data-stu-id="00880-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="00880-120">Wenn Sie HTTPS bereits auf Ihrem Server eingerichtet haben, müssen Sie nur den Server so konfigurieren, dass alle HTTP-Anforderungen an HTTPS umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="00880-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="00880-121">Wenn Sie HTTPS nicht auf Ihrem Server eingerichtet haben, bietet [Let's Encrypt][LetsEncrypt] eine kostenlose und relativ einfache Möglichkeit, den Prozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="00880-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="00880-122">Sie können auch erwägen, Ihre Website auf einem CDN.</span><span class="sxs-lookup"><span data-stu-id="00880-122">Or, you may consider hosting your site on a CDN.</span></span>  <span data-ttu-id="00880-123">Die meisten wichtigen CDNs hosten jetzt standardmäßig Websites auf HTTPS.</span><span class="sxs-lookup"><span data-stu-id="00880-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="00880-124">Der [Hinweis HTTPS][WebhintUseHttps] in [Webhint][Webhint] verwenden kann dazu beitragen, den Prozess zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an HTTPS geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="00880-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <a name="mixed-content"></a><span data-ttu-id="00880-125">Gemischte Inhalte</span><span class="sxs-lookup"><span data-stu-id="00880-125">Mixed content</span></span>  

<span data-ttu-id="00880-126">**Gemischter** Inhalt bedeutet, dass der Hauptherkunft einer Seite sicher ist, die Seite jedoch Ressourcen aus nicht sicheren Ursprüngen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="00880-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="00880-127">Seiten mit gemischten Inhalten sind nur teilweise geschützt, da der Zugriff auf den HTTP-Inhalt für Schnüffeler und anfällig für Man-in-the-Middle-Angriffe ist.</span><span class="sxs-lookup"><span data-stu-id="00880-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Gemischte Inhalte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="00880-129">Gemischte Inhalte</span><span class="sxs-lookup"><span data-stu-id="00880-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="00880-130">Wählen Sie in der vorherigen Abbildung die Option \*\*\*\* Anforderung **anzeigen im** Netzwerkbereich aus, um das Netzwerktool zu öffnen und den Filter anzuwenden, sodass im Netzwerkprotokoll nur nicht sichere Ressourcen `mixed-content:displayed` angezeigt werden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00880-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** tool and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Gemischte Ressourcen im Netzwerkprotokoll" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="00880-132">Gemischte Ressourcen im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="00880-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <a name="view-details"></a><span data-ttu-id="00880-133">Details anzeigen</span><span class="sxs-lookup"><span data-stu-id="00880-133">View details</span></span>  

### <a name="view-main-origin-certificate"></a><span data-ttu-id="00880-134">Hauptursprungzertifikat anzeigen</span><span class="sxs-lookup"><span data-stu-id="00880-134">View main origin certificate</span></span>  

<span data-ttu-id="00880-135">Wählen Sie **in der Sicherheitsübersicht**Zertifikat **anzeigen aus,** um das Zertifikat schnell auf den Hauptursprung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="00880-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Ein Hauptursprungzertifikat" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="00880-137">Ein Hauptursprungzertifikat</span><span class="sxs-lookup"><span data-stu-id="00880-137">A main origin certificate</span></span>  
:::image-end:::  

### <a name="view-origin-details"></a><span data-ttu-id="00880-138">Anzeigen von Ursprungsdetails</span><span class="sxs-lookup"><span data-stu-id="00880-138">View origin details</span></span>  

<span data-ttu-id="00880-139">Wählen Sie einen der Einträge im linken Navigationsgerät aus, um die Details des Ursprungs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00880-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="00880-140">Auf der Detailseite können Sie Verbindungs- und Zertifikatinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="00880-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="00880-141">Informationen zur Zertifikattransparenz werden ebenfalls angezeigt, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="00880-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Hauptherkunftsdetails" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="00880-143">Hauptherkunftsdetails</span><span class="sxs-lookup"><span data-stu-id="00880-143">Main origin details</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="00880-144">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="00880-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Let's Encrypt – Kostenlose SSL/TLS-Zertifikate"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Verwenden von HTTPS-| Webhintdokumentation"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="00880-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00880-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="00880-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/security/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="00880-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="00880-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="00880-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
