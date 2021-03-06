---
description: Erfahren Sie, wie Sie Netzwerkprobleme im Netzwerkbereich von Microsoft Edge DevTools erkennen.
title: Leitfaden zu Netzwerkproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 12cc447fa9d8ef8624e8528430eabc25ab523dd0
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398273"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="network-issues-guide"></a><span data-ttu-id="16efb-104">Leitfaden zu Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="16efb-104">Network issues guide</span></span>  

<span data-ttu-id="16efb-105">In diesem Handbuch erfahren Sie, wie Sie Netzwerkprobleme oder Optimierungsmöglichkeiten im Netzwerkbereich von Microsoft Edge DevTools erkennen.</span><span class="sxs-lookup"><span data-stu-id="16efb-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="16efb-106">Um die Grundlagen des Netzwerktools **zu** erlernen, navigieren Sie zu [Erste Schritte][NetworkPerformance].</span><span class="sxs-lookup"><span data-stu-id="16efb-106">To learn the basics of the **Network** tool, navigate to [Get Started][NetworkPerformance].</span></span>  

## <a name="queued-or-stalled-requests"></a><span data-ttu-id="16efb-107">Anforderungen in der Warteschlange oder in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="16efb-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="16efb-108">Symptome</span><span class="sxs-lookup"><span data-stu-id="16efb-108">Symptoms</span></span>**  

<span data-ttu-id="16efb-109">Sechs Anforderungen werden gleichzeitig heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="16efb-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="16efb-110">Anschließend wird eine Reihe von Anforderungen in die Warteschlange gestellt oder ins Stocken geraten.</span><span class="sxs-lookup"><span data-stu-id="16efb-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="16efb-111">Sobald eine der ersten sechs Anforderungen abgeschlossen ist, wird eine der Anforderungen in der Warteschlange gestartet.</span><span class="sxs-lookup"><span data-stu-id="16efb-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="16efb-112">Im **Wasserfall** in der folgenden Abbildung beginnen die ersten sechs Anforderungen für die `edge-iconx1024.msft.png` Ressource gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="16efb-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="16efb-113">Die nachfolgenden Anforderungen werden bis zum Ende einer der ursprünglichen sechs Beendete beendet.</span><span class="sxs-lookup"><span data-stu-id="16efb-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ein Beispiel für eine in die Warteschlange eingereihte oder in die Warteschlange geplatzte Datenreihe im Netzwerkbereich" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="16efb-115">Ein Beispiel für eine in der Warteschlange oder in der Warteschlange geplatzte Datenreihe im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="16efb-115">An example of a queued or stalled series in the **Network** tool</span></span>  
:::image-end:::  

**<span data-ttu-id="16efb-116">Ursachen</span><span class="sxs-lookup"><span data-stu-id="16efb-116">Causes</span></span>**  

<span data-ttu-id="16efb-117">Es werden zu viele Anforderungen für eine einzelne Domäne vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="16efb-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="16efb-118">Bei HTTP/1.0- oder HTTP/1.1-Verbindungen ermöglicht Microsoft Edge maximal sechs gleichzeitige TCP-Verbindungen pro Host.</span><span class="sxs-lookup"><span data-stu-id="16efb-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="16efb-119">Fixes</span><span class="sxs-lookup"><span data-stu-id="16efb-119">Fixes</span></span>**  

*   <span data-ttu-id="16efb-120">Implementieren Sie die Domänensharding, wenn Sie HTTP/1.0 oder HTTP/1.1 verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="16efb-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="16efb-121">Verwenden Sie HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="16efb-121">Use HTTP/2.</span></span>  <span data-ttu-id="16efb-122">Verwenden Sie keine Domänensharding mit HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="16efb-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="16efb-123">Entfernen oder Aufschub unnötiger Anforderungen, sodass kritische Anforderungen früher heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="16efb-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <a name="slow-time-to-first-byte-ttfb"></a><span data-ttu-id="16efb-124">Slow Time To First Byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="16efb-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="16efb-125">Symptome</span><span class="sxs-lookup"><span data-stu-id="16efb-125">Symptoms</span></span>**  

<span data-ttu-id="16efb-126">Eine Anforderung wartet lange darauf, das erste Byte vom Server zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16efb-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="16efb-127">In der folgenden Abbildung gibt die lange grüne Leiste im **Wasserfall** an, dass die Anforderung lange gewartet hat.</span><span class="sxs-lookup"><span data-stu-id="16efb-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="16efb-128">Dies wurde mithilfe eines Profils simuliert, um die Netzwerkgeschwindigkeit einzuschränken und eine Verzögerung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="16efb-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ein Beispiel für eine Anforderung mit einem langsamen Time To First Byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="16efb-130">Ein Beispiel für eine Anforderung mit einem langsamen Time To First Byte</span><span class="sxs-lookup"><span data-stu-id="16efb-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="16efb-131">Ursachen</span><span class="sxs-lookup"><span data-stu-id="16efb-131">Causes</span></span>**  

*   <span data-ttu-id="16efb-132">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="16efb-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="16efb-133">Der Server reagiert langsam.</span><span class="sxs-lookup"><span data-stu-id="16efb-133">The server is slow to respond.</span></span>  <span data-ttu-id="16efb-134">Hosten Sie den Server lokal, um festzustellen, ob die Verbindung oder der Server langsam ist.</span><span class="sxs-lookup"><span data-stu-id="16efb-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="16efb-135">Wenn Sie beim Zugriff auf einen lokalen Server immer noch ein langsames Time To First Byte \(TTFB\) erhalten, ist der Server langsam.</span><span class="sxs-lookup"><span data-stu-id="16efb-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="16efb-136">Fixes</span><span class="sxs-lookup"><span data-stu-id="16efb-136">Fixes</span></span>**  

*   <span data-ttu-id="16efb-137">Wenn die Verbindung langsam ist, sollten Sie Ihre Inhalte auf einem CDN hosten oder Hostinganbieter ändern.</span><span class="sxs-lookup"><span data-stu-id="16efb-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="16efb-138">Wenn der Server langsam ist, sollten Sie datenbankabfragen optimieren, einen Cache implementieren oder Ihre Serverkonfiguration ändern.</span><span class="sxs-lookup"><span data-stu-id="16efb-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <a name="slow-content-download"></a><span data-ttu-id="16efb-139">Langsamer Inhaltsdownload</span><span class="sxs-lookup"><span data-stu-id="16efb-139">Slow content download</span></span>  

**<span data-ttu-id="16efb-140">Symptome</span><span class="sxs-lookup"><span data-stu-id="16efb-140">Symptoms</span></span>**  

<span data-ttu-id="16efb-141">Das Herunterladen einer Anforderung dauert sehr lange.</span><span class="sxs-lookup"><span data-stu-id="16efb-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="16efb-142">In der folgenden Abbildung bedeutet die lange, blaue Leiste im **Wasserfall** neben dem Png, dass der Download lange gezeitet hat.</span><span class="sxs-lookup"><span data-stu-id="16efb-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ein Beispiel für eine Anforderung, die lange dauert, bis sie heruntergeladen wird" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="16efb-144">Ein Beispiel für eine Anforderung, die lange dauert, bis sie heruntergeladen wird</span><span class="sxs-lookup"><span data-stu-id="16efb-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="16efb-145">Ursachen</span><span class="sxs-lookup"><span data-stu-id="16efb-145">Causes</span></span>**  

*   <span data-ttu-id="16efb-146">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="16efb-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="16efb-147">Viele Inhalte werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="16efb-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="16efb-148">Fixes</span><span class="sxs-lookup"><span data-stu-id="16efb-148">Fixes</span></span>**  

*   <span data-ttu-id="16efb-149">Erwägen Sie, Ihre Inhalte auf einem CDN zu hosten oder Hostinganbieter zu ändern.</span><span class="sxs-lookup"><span data-stu-id="16efb-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="16efb-150">Senden Sie weniger Bytes, indem Sie Ihre Anforderungen optimieren.</span><span class="sxs-lookup"><span data-stu-id="16efb-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="16efb-151">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="16efb-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Überprüfen der Netzwerkaktivitäten in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Neues Problem – MicrosoftDocs/edge-developer"  

> [!NOTE]
> <span data-ttu-id="16efb-154">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16efb-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="16efb-155">Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/network/issues) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="16efb-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="16efb-157">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16efb-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
