---
description: Informationen zum Erkennen von Netzwerkproblemen finden Sie im Netzwerk Panel von Microsoft Edge devtools.
title: Leitfaden zu Netzwerkproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ccd78c34a50bf235416df58aad28df9253b1b24e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993373"
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





# <span data-ttu-id="b72de-104">Leitfaden zu Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="b72de-104">Network issues guide</span></span>   




<span data-ttu-id="b72de-105">Dieser Leitfaden zeigt Ihnen, wie Sie Netzwerkprobleme oder Optimierungsmöglichkeiten im Netzwerk Panel von Microsoft Edge devtools erkennen.</span><span class="sxs-lookup"><span data-stu-id="b72de-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="b72de-106">Informationen zu den Grundlagen der **Netzwerk** Steuerung finden Sie unter [Erste Schritte][NetworkPerformance] .</span><span class="sxs-lookup"><span data-stu-id="b72de-106">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="b72de-107">Warteschlangen-oder verzögerte Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b72de-107">Queued or stalled requests</span></span>   

**<span data-ttu-id="b72de-108">Symptome</span><span class="sxs-lookup"><span data-stu-id="b72de-108">Symptoms</span></span>**  

<span data-ttu-id="b72de-109">Sechs Anforderungen werden gleichzeitig heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="b72de-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="b72de-110">Danach wird eine Reihe von Anforderungen in die Warteschlange gestellt oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="b72de-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="b72de-111">Nachdem eine der ersten sechs Anforderungen beendet wurde, wird eine der Anforderungen in der Warteschlange gestartet.</span><span class="sxs-lookup"><span data-stu-id="b72de-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="b72de-112">Im **Wasserfall** in der folgenden Abbildung beginnen die ersten sechs Anforderungen für das `edge-iconx1024.msft.png` Objekt gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="b72de-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="b72de-113">Die nachfolgenden Anforderungen werden angehalten, bis eine der ursprünglichen sechs beendet ist.</span><span class="sxs-lookup"><span data-stu-id="b72de-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="b72de-115">Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="b72de-115">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="b72de-116">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b72de-116">Causes</span></span>**  

<span data-ttu-id="b72de-117">Es werden zu viele Anforderungen an eine einzelne Domäne gestellt.</span><span class="sxs-lookup"><span data-stu-id="b72de-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="b72de-118">Bei HTTP/1.0-oder http/1.1-Verbindungen können mit Microsoft Edge maximal sechs gleichzeitige TCP-Verbindungen pro Host ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b72de-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="b72de-119">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b72de-119">Fixes</span></span>**  

*   <span data-ttu-id="b72de-120">Implementieren Sie Domänen Splitter, wenn Sie http/1.0 oder http/1.1 verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="b72de-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="b72de-121">Verwenden Sie http/2.</span><span class="sxs-lookup"><span data-stu-id="b72de-121">Use HTTP/2.</span></span>  <span data-ttu-id="b72de-122">Verwenden Sie keine Domänen Splitterung mit http/2.</span><span class="sxs-lookup"><span data-stu-id="b72de-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="b72de-123">Entfernen oder aufschieben unnötiger Anforderungen, damit kritische Anforderungen früher heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b72de-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="b72de-124">Langsame Zeit bis zum ersten Byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="b72de-124">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="b72de-125">Symptome</span><span class="sxs-lookup"><span data-stu-id="b72de-125">Symptoms</span></span>**  

<span data-ttu-id="b72de-126">Eine Anforderung verbringt lange Zeit darauf, das erste Byte vom Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b72de-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="b72de-127">In der folgenden Abbildung zeigt der lange, grüne Balken im **Wasserfall** an, dass die Anforderung lange gewartet hat.</span><span class="sxs-lookup"><span data-stu-id="b72de-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="b72de-128">Dies wurde mithilfe eines Profils simuliert, um die Netzwerkgeschwindigkeit zu begrenzen und eine Verzögerung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b72de-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="b72de-130">Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte</span><span class="sxs-lookup"><span data-stu-id="b72de-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="b72de-131">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b72de-131">Causes</span></span>**  

*   <span data-ttu-id="b72de-132">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="b72de-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="b72de-133">Der Server reagiert langsam.</span><span class="sxs-lookup"><span data-stu-id="b72de-133">The server is slow to respond.</span></span>  <span data-ttu-id="b72de-134">Hosten Sie den Server lokal, um festzustellen, ob es sich um eine langsame Verbindung oder einen Server handelt.</span><span class="sxs-lookup"><span data-stu-id="b72de-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="b72de-135">Wenn Sie beim Zugriff auf einen lokalen Server weiterhin langsam auf das erste Byte \ (TTFB \) zugreifen, ist der Server langsam.</span><span class="sxs-lookup"><span data-stu-id="b72de-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="b72de-136">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b72de-136">Fixes</span></span>**  

*   <span data-ttu-id="b72de-137">Wenn die Verbindung langsam ist, sollten Sie das Hosten von Inhalten in einem CDN oder Ändern von Hostinganbieter in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="b72de-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="b72de-138">Wenn der Server langsam ist, empfiehlt es sich, Datenbankabfragen zu optimieren, einen Cache zu implementieren oder Ihre Serverkonfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b72de-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="b72de-139">Langsamer Download von Inhalten</span><span class="sxs-lookup"><span data-stu-id="b72de-139">Slow content download</span></span>   

**<span data-ttu-id="b72de-140">Symptome</span><span class="sxs-lookup"><span data-stu-id="b72de-140">Symptoms</span></span>**  

<span data-ttu-id="b72de-141">Eine Anforderung dauert lange zum herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b72de-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="b72de-142">In der folgenden Abbildung bedeutet der lange, blaue Balken im **Wasserfall** neben dem PNG, dass es lange dauert, bis der Download erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="b72de-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="b72de-144">Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt</span><span class="sxs-lookup"><span data-stu-id="b72de-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="b72de-145">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b72de-145">Causes</span></span>**  

*   <span data-ttu-id="b72de-146">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="b72de-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="b72de-147">Viele Inhalte werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="b72de-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="b72de-148">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b72de-148">Fixes</span></span>**  

*   <span data-ttu-id="b72de-149">Bedenken Sie, dass Sie Ihre Inhalte in einem CDN hosten oder Hosting-Anbieter ändern.</span><span class="sxs-lookup"><span data-stu-id="b72de-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="b72de-150">Senden Sie weniger Bytes, indem Sie Ihre Anforderungen optimieren.</span><span class="sxs-lookup"><span data-stu-id="b72de-150">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="b72de-151">Wissens Spenden</span><span class="sxs-lookup"><span data-stu-id="b72de-151">Contribute knowledge</span></span>  

<span data-ttu-id="b72de-152">Haben Sie ein Netzwerkproblem, das diesem Leitfaden hinzugefügt werden sollte?</span><span class="sxs-lookup"><span data-stu-id="b72de-152">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="b72de-153">Senden Sie einen Tweet an [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="b72de-153">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="b72de-154">Wählen Sie **Feedback senden** \ ( ![ Feedback senden ][ImageSendFeedbackIcon] \) im devtools aus, oder drücken Sie \ ( `Alt` + `Shift` + `I` Windows \) oder `Option` + `Shift` + `I` \ (macOS \), um Feedback-oder Funktionsanforderungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b72de-154">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="b72de-155">[Öffnen Sie ein Problem][WebFundamentalsIssue] mit dem docs Repo.</span><span class="sxs-lookup"><span data-stu-id="b72de-155">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Neues Problem – MicrosoftDocs/Edge – Entwickler"  

> [!NOTE]
> <span data-ttu-id="b72de-158">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b72de-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b72de-159">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/network/issues) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Jonathan Garber][JonathanGarbee] \ (Google Developer Expert für Web Technology) verfasst.</span><span class="sxs-lookup"><span data-stu-id="b72de-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b72de-161">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b72de-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
