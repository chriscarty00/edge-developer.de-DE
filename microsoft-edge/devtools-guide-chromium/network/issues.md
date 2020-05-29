---
title: Leitfaden zu Netzwerkproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611805"
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





# <span data-ttu-id="b7924-103">Leitfaden zu Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="b7924-103">Network Issues Guide</span></span>   




<span data-ttu-id="b7924-104">Dieser Leitfaden zeigt Ihnen, wie Sie Netzwerkprobleme oder Optimierungsmöglichkeiten im Netzwerk Panel von Microsoft Edge devtools erkennen.</span><span class="sxs-lookup"><span data-stu-id="b7924-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="b7924-105">Informationen zu den Grundlagen der Netzwerksteuerung finden Sie unter [Erste Schritte][NetworkPerformance] .</span><span class="sxs-lookup"><span data-stu-id="b7924-105">See [Get Started][NetworkPerformance] to learn the basics of the Network panel.</span></span>  

## <span data-ttu-id="b7924-106">Warteschlangen-oder verzögerte Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7924-106">Queued or stalled requests</span></span>   

### <span data-ttu-id="b7924-107">Symptome</span><span class="sxs-lookup"><span data-stu-id="b7924-107">Symptoms</span></span>  

<span data-ttu-id="b7924-108">Sechs Anforderungen werden gleichzeitig heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="b7924-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="b7924-109">Danach wird eine Reihe von Anforderungen in die Warteschlange gestellt oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="b7924-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="b7924-110">Nachdem eine der ersten sechs Anforderungen beendet wurde, wird eine der Anforderungen in der Warteschlange gestartet.</span><span class="sxs-lookup"><span data-stu-id="b7924-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="b7924-111">Im **Wasserfall** in [Abbildung 1](#figure-1)beginnen die ersten sechs Anforderungen für das `edge-iconx1024.msft.png` Objekt gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="b7924-111">In the **Waterfall** in [Figure 1](#figure-1), the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="b7924-112">Die nachfolgenden Anforderungen werden angehalten, bis eine der ursprünglichen sechs beendet ist.</span><span class="sxs-lookup"><span data-stu-id="b7924-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

> ##### <span data-ttu-id="b7924-113">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="b7924-113">Figure 1</span></span>  
> <span data-ttu-id="b7924-114">Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="b7924-114">An example of a queued or stalled series in the Network panel</span></span>  
> ![Ein Beispiel für eine Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel][ImageStalled]  

### <span data-ttu-id="b7924-116">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b7924-116">Causes</span></span>  

<span data-ttu-id="b7924-117">Es werden zu viele Anforderungen an eine einzelne Domäne gestellt.</span><span class="sxs-lookup"><span data-stu-id="b7924-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="b7924-118">Bei HTTP/1.0-oder http/1.1-Verbindungen können mit Microsoft Edge maximal sechs gleichzeitige TCP-Verbindungen pro Host ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b7924-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

### <span data-ttu-id="b7924-119">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b7924-119">Fixes</span></span>  

*   <span data-ttu-id="b7924-120">Implementieren Sie Domänen Splitter, wenn Sie http/1.0 oder http/1.1 verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="b7924-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="b7924-121">Verwenden Sie http/2.</span><span class="sxs-lookup"><span data-stu-id="b7924-121">Use HTTP/2.</span></span>  <span data-ttu-id="b7924-122">Verwenden Sie keine Domänen Splitterung mit http/2.</span><span class="sxs-lookup"><span data-stu-id="b7924-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="b7924-123">Entfernen oder aufschieben unnötiger Anforderungen, damit kritische Anforderungen früher heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b7924-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  

## <span data-ttu-id="b7924-124">Langsame Zeit bis zum ersten Byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="b7924-124">Slow Time To First Byte (TTFB)</span></span>   

### <span data-ttu-id="b7924-125">Symptome</span><span class="sxs-lookup"><span data-stu-id="b7924-125">Symptoms</span></span>  

<span data-ttu-id="b7924-126">Eine Anforderung verbringt lange Zeit darauf, das erste Byte vom Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b7924-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="b7924-127">In [Abbildung 2](#figure-2)zeigt der lange, grüne Balken im **Wasserfall** an, dass die Anforderung lange gewartet hat.</span><span class="sxs-lookup"><span data-stu-id="b7924-127">In [Figure 2](#figure-2), the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="b7924-128">Dies wurde mithilfe eines Profils simuliert, um die Netzwerkgeschwindigkeit zu begrenzen und eine Verzögerung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7924-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

> ##### <span data-ttu-id="b7924-129">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="b7924-129">Figure 2</span></span>  
> <span data-ttu-id="b7924-130">Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte</span><span class="sxs-lookup"><span data-stu-id="b7924-130">An example of a request with a slow Time To First Byte</span></span>  
> ![Ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte][ImageSlowTimeToFirstByte]  

### <span data-ttu-id="b7924-132">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b7924-132">Causes</span></span>  

*   <span data-ttu-id="b7924-133">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="b7924-133">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="b7924-134">Der Server reagiert langsam.</span><span class="sxs-lookup"><span data-stu-id="b7924-134">The server is slow to respond.</span></span>  <span data-ttu-id="b7924-135">Hosten Sie den Server lokal, um festzustellen, ob es sich um eine langsame Verbindung oder einen Server handelt.</span><span class="sxs-lookup"><span data-stu-id="b7924-135">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="b7924-136">Wenn Sie beim Zugriff auf einen lokalen Server weiterhin langsam auf das erste Byte \ (TTFB \) zugreifen, ist der Server langsam.</span><span class="sxs-lookup"><span data-stu-id="b7924-136">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  

### <span data-ttu-id="b7924-137">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b7924-137">Fixes</span></span>  

*   <span data-ttu-id="b7924-138">Wenn die Verbindung langsam ist, sollten Sie das Hosten von Inhalten in einem CDN oder Ändern von Hostinganbieter in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="b7924-138">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="b7924-139">Wenn der Server langsam ist, empfiehlt es sich, Datenbankabfragen zu optimieren, einen Cache zu implementieren oder Ihre Serverkonfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b7924-139">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  

## <span data-ttu-id="b7924-140">Langsamer Download von Inhalten</span><span class="sxs-lookup"><span data-stu-id="b7924-140">Slow content download</span></span>   

### <span data-ttu-id="b7924-141">Symptome</span><span class="sxs-lookup"><span data-stu-id="b7924-141">Symptoms</span></span>  

<span data-ttu-id="b7924-142">Eine Anforderung dauert lange zum herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b7924-142">A request takes a long time to download.</span></span>  

<span data-ttu-id="b7924-143">In [Abbildung 3](#figure-3)bedeutet der lange, blaue Balken im **Wasserfall** neben dem PNG, dass es lange dauert, bis der Download erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="b7924-143">In [Figure 3](#figure-3), the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

> ##### <span data-ttu-id="b7924-144">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="b7924-144">Figure 3</span></span>  
> <span data-ttu-id="b7924-145">Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt</span><span class="sxs-lookup"><span data-stu-id="b7924-145">An example of a request that takes a long time to download</span></span>  
> ![Ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt][ImageSlowContentDownload]  

### <span data-ttu-id="b7924-147">Ursachen</span><span class="sxs-lookup"><span data-stu-id="b7924-147">Causes</span></span>  

*   <span data-ttu-id="b7924-148">Die Verbindung zwischen dem Client und dem Server ist langsam.</span><span class="sxs-lookup"><span data-stu-id="b7924-148">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="b7924-149">Viele Inhalte werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="b7924-149">A lot of content is being downloaded.</span></span>  

### <span data-ttu-id="b7924-150">Korrekturen</span><span class="sxs-lookup"><span data-stu-id="b7924-150">Fixes</span></span>  

*   <span data-ttu-id="b7924-151">Bedenken Sie, dass Sie Ihre Inhalte in einem CDN hosten oder Hosting-Anbieter ändern.</span><span class="sxs-lookup"><span data-stu-id="b7924-151">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="b7924-152">Senden Sie weniger Bytes, indem Sie Ihre Anforderungen optimieren.</span><span class="sxs-lookup"><span data-stu-id="b7924-152">Send fewer bytes by optimizing your requests.</span></span>  

## <span data-ttu-id="b7924-153">Wissens Spenden</span><span class="sxs-lookup"><span data-stu-id="b7924-153">Contribute knowledge</span></span>  

<span data-ttu-id="b7924-154">Haben Sie ein Netzwerkproblem, das diesem Leitfaden hinzugefügt werden sollte?</span><span class="sxs-lookup"><span data-stu-id="b7924-154">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="b7924-155">Senden Sie einen Tweet an [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="b7924-155">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="b7924-156">Wählen **Sie Feedback senden Feedback** ![ senden ][ImageSendFeedbackIcon] im devtools aus, oder drücken Sie `Alt` + `Shift` + `I` \ (Windows \) oder `Option` + `Shift` + `I` \ (macOS \), um Feedback-oder Funktionsanforderungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b7924-156">Select **Send Feedback** ![Send Feedback][ImageSendFeedbackIcon] in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="b7924-157">[Öffnen Sie ein Problem][WebFundamentalsIssue] mit dem docs Repo.</span><span class="sxs-lookup"><span data-stu-id="b7924-157">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Abbildung 1: Beispiel einer Reihe von Warteschlangen oder verzögerten Datenreihen im Netzwerk Panel"  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Abbildung 2: ein Beispiel für eine Anforderung mit einer langsamen Zeit bis zum ersten Byte"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Abbildung 3: ein Beispiel für eine Anforderung, deren Download viel Zeit in Anspruch nimmt"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Neues Problem – MicrosoftDocs/Edge – Entwickler"  

> [!NOTE]
> <span data-ttu-id="b7924-163">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7924-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b7924-164">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/network/issues) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Jonathan Garber][JonathanGarbee] \ (Google Developer Expert für Web Technology) verfasst.</span><span class="sxs-lookup"><span data-stu-id="b7924-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b7924-166">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b7924-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
