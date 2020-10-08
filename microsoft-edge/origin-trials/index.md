---
ms.assetid: ''
description: Experimentieren Sie sicher während eines bestimmten Zeitraums, und geben Sie Feedback zu neuen Plattformfeatures.
title: Herkunfts Versuche
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, Origin Trials, Entwickler
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846528"
---
# <span data-ttu-id="562e2-104">Verwenden von Ursprungs versuchen in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="562e2-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="562e2-105">Entwickler können mithilfe von Origin Trials experimentelle APIs auf Live-Websites für einen bestimmten Zeitraum testen.</span><span class="sxs-lookup"><span data-stu-id="562e2-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="562e2-106">Bei Verwendung von Ursprungs Testversionen können Benutzer von Microsoft Edge, die Ihre Website besuchen, Code ausführen, der experimentelle APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="562e2-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="562e2-107">Wenn Sie auf die experimentellen APIs auf jedem Benutzer Computer zugreifen möchten, müssen Sie nicht zu den `edge://flags` Feature-Flags wechseln und diese aktivieren.</span><span class="sxs-lookup"><span data-stu-id="562e2-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="562e2-108">Weitere Informationen finden Sie unter [experimentelle APIs][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="562e2-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="562e2-109">Darüber hinaus können Sie Feedback über das Design der API, ihre Anwendungsfälle oder Ihre Erfahrungen mithilfe der APIs für Browser Ingenieure und die Web-Standard Community bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="562e2-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="562e2-110">Erste Schritte mit Origin-Testversionen</span><span class="sxs-lookup"><span data-stu-id="562e2-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="562e2-111">Weitere Informationen zu den in Microsoft Edge verfügbaren experimentellen APIs finden Sie unter [Entwicklerkonsole für Microsoft Edge Origin Trials][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="562e2-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="562e2-112">Stellen Sie sicher, dass Sie die Mindestsystemanforderungen für Microsoft Edge und das Enddatum der Testversion überprüfen, um die Eignung der Verwendung der experimentellen APIs auf Ihrer Website zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="562e2-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="562e2-113">Ein Experiment kann früher als geplant enden, wenn eine der folgenden Situationen eintritt.</span><span class="sxs-lookup"><span data-stu-id="562e2-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="562e2-114">Ein wichtiger Sicherheitsvorfall.</span><span class="sxs-lookup"><span data-stu-id="562e2-114">A major security incident.</span></span>  
> *   <span data-ttu-id="562e2-115">Wenn genügend Feedback erfasst wird, das darauf hinweist, dass eine größere Neugestaltung erforderlich ist, um die Anforderungen von Webentwicklern zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="562e2-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="562e2-116">In beiden Fällen wird eine Benachrichtigungs-e-Mail an alle Entwickler gesendet, die zurzeit beim Experiment registriert sind.</span><span class="sxs-lookup"><span data-stu-id="562e2-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="562e2-117">Registrieren für eine Testversion einer experimentellen API</span><span class="sxs-lookup"><span data-stu-id="562e2-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="562e2-118">Führen Sie die folgenden Schritte aus, um sich für eine Testversion einer experimentellen API zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="562e2-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="562e2-119">Besuchen Sie die [Microsoft Edge Origin Trials-Entwickler Konsolen][DeveloperMicrsoftEdgeOriginTrials] Seite.</span><span class="sxs-lookup"><span data-stu-id="562e2-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="562e2-120">Wählen Sie die Schaltfläche Registrieren in einem der verfügbaren Experimente aus.</span><span class="sxs-lookup"><span data-stu-id="562e2-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="562e2-121">Melden Sie sich mit Ihrem GitHub-Nutzernamen und Kennwort bei der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="562e2-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="562e2-122">Wählen Sie **MicrosoftEdge autorisieren**aus.</span><span class="sxs-lookup"><span data-stu-id="562e2-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="562e2-123">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="562e2-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="562e2-124">Wenn Sie eine einzelne oder alle Unterdomänen registrieren möchten, wählen Sie `Do you need to match all subdomains for the provided origin?` Einstellung festlegen auf aus `Yes` .</span><span class="sxs-lookup"><span data-stu-id="562e2-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="562e2-125">Beispielsweise `https://dev.contoso.com` handelt es sich um eine einzelne Domäne, bei der `https://*.contoso.com` alle Unterdomänen als Platzhalter dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="562e2-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="562e2-126">Die folgenden Ursprungs Formate sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="562e2-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="562e2-127">Angeben eines Unterordners für den Ursprung</span><span class="sxs-lookup"><span data-stu-id="562e2-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="562e2-128">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="562e2-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="562e2-129">Verwenden eines Ursprungs mit Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="562e2-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="562e2-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="562e2-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="562e2-131">Wählen Sie **annehmen und registrieren**aus.</span><span class="sxs-lookup"><span data-stu-id="562e2-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="562e2-132">Anwenden des Tokens</span><span class="sxs-lookup"><span data-stu-id="562e2-132">Apply your token</span></span>  

<span data-ttu-id="562e2-133">Ein Token wird sofort generiert und auf der [Microsoft Edge Origin Trials-Entwickler Konsolen][DeveloperMicrsoftEdgeOriginTrials] Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="562e2-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="562e2-134">Wenn Sie die Testversion auf Ihrer Website verwenden möchten, verwenden Sie eine der folgenden Methoden, um das Token auf Ihre Seite anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="562e2-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="562e2-135">Fügen Sie dem `origin-trial` `meta` Tag auf jeder Seite, die die experimental-API verwendet, den Attributwert und das Token hinzu.</span><span class="sxs-lookup"><span data-stu-id="562e2-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="562e2-136">Fügen Sie `Origin-Trial` den HTTP-Antwortheader Ihres Servers hinzu.</span><span class="sxs-lookup"><span data-stu-id="562e2-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="562e2-137">Ihr Token ist für 6 Wochen gültig.</span><span class="sxs-lookup"><span data-stu-id="562e2-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="562e2-138">Bevor Ihr Testabonnement endet, werden Erinnerungs-e-Mails an Sie gesendet, die nach Ihrem Feedback Fragen, und Sie bitten, Ihre Testversion zu erneuern, bevor Ihr Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="562e2-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="562e2-139">Deaktivieren eines Experiments</span><span class="sxs-lookup"><span data-stu-id="562e2-139">Opt out of an experiment</span></span>  

<span data-ttu-id="562e2-140">Wenn Sie ein Experiment deaktivieren möchten, verwenden Sie eine der folgenden Methoden, um Ihr Token zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="562e2-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="562e2-141">Entfernen Sie die `meta` Kategorie von jeder Seite, die die experimental-API verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="562e2-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="562e2-142">Entfernen Sie `Origin-Trial` aus dem HTTP-Antwortheader Ihres Servers.</span><span class="sxs-lookup"><span data-stu-id="562e2-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="562e2-143">Erkennen experimenteller Features und Bereitstellen eines Fallbacks</span><span class="sxs-lookup"><span data-stu-id="562e2-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="562e2-144">Stellen Sie bei der Verwendung von experimentellen APIs sicher, dass Sie allen Besuchern Ihrer Website ein Arbeitserlebnis bieten.</span><span class="sxs-lookup"><span data-stu-id="562e2-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="562e2-145">Besucher können Browser verwenden, die die experimentellen APIs, die Sie Ihrem Code hinzugefügt haben, nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="562e2-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="562e2-146">Wenn Ihr Token abläuft, bevor Sie es erneuern, ist die experimentelle API nicht mehr verfügbar, was zu Fehlern führen kann.</span><span class="sxs-lookup"><span data-stu-id="562e2-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="562e2-147">Um dies zu vermeiden, stellen Sie sicher, dass Sie die in Ihrem Browser verfügbaren Funktionen erkennen.</span><span class="sxs-lookup"><span data-stu-id="562e2-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="562e2-148">Weitere Informationen finden Sie unter [Implementieren der Feature-Erkennung][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="562e2-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="562e2-149">Roadmap für zulässige Ursprünge</span><span class="sxs-lookup"><span data-stu-id="562e2-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="562e2-150">Das Microsoft Edge-Ursprungs testportal unterstützt heute nur SSL-aktivierte Ursprünge, was bedeutet, dass für Websites https richtig implementiert sein muss, damit Sie sich für ein Experiment registrieren können.</span><span class="sxs-lookup"><span data-stu-id="562e2-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="562e2-151">In Zukunft sind die folgenden sicheren Ursprünge geplant.</span><span class="sxs-lookup"><span data-stu-id="562e2-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="562e2-152">Registrieren `http://localhost` Sie sich als Ursprung für ihre Experimente.</span><span class="sxs-lookup"><span data-stu-id="562e2-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="562e2-153">Um heute zu verwenden `http://localhost` , wechseln Sie zu, `edge://flags` und legen Sie das Experiment auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="562e2-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="562e2-154">Verwenden Sie Erweiterungen mit `extensions://` vorfesten Ursprüngen, um sich bei Experimenten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="562e2-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials-Entwicklerkonsole | Microsoft docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementieren der Feature-Erkennung | MDN"  
