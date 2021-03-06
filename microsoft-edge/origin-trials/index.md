---
ms.assetid: ''
description: Experimentieren Sie sicher für einen bestimmten Zeitraum und geben Sie Feedback zu neuen Plattformfeatures.
title: Herkunfts Versuche
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, origin trials, developer
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397545"
---
# <a name="use-origin-trials-in-microsoft-edge"></a><span data-ttu-id="b7ff1-104">Verwenden von Origin Trials in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b7ff1-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="b7ff1-105">Entwickler können Origin Trials verwenden, um experimentelle APIs auf Livewebsites für einen begrenzten Zeitraum auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="b7ff1-106">Bei Verwendung von Origin Trials können Benutzer von Microsoft Edge, die Ihre Website besuchen, Code ausführen, der experimentelle APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="b7ff1-107">Um auf die experimentellen APIs auf jedem Benutzercomputer zu zugreifen, müssen Sie nicht zu feature flags `edge://flags` wechseln und diese aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="b7ff1-108">Weitere Informationen finden Sie unter Experimentelle [APIs][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="b7ff1-108">For more information, navigate to [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="b7ff1-109">Darüber hinaus können Sie Feedback zum Entwurf der API, zu Ihren Verwendungsfällen oder zur Verwendung der APIs für Browsertechniker und die Webstandard-Community bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <a name="get-started-using-origin-trials"></a><span data-ttu-id="b7ff1-110">Erste Schritte mit Origin Trials</span><span class="sxs-lookup"><span data-stu-id="b7ff1-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="b7ff1-111">Weitere Informationen zu den in Microsoft Edge verfügbaren experimentellen APIs finden Sie unter [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="b7ff1-111">For more information about the experimental APIs available in Microsoft Edge, navigate to [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="b7ff1-112">Stellen Sie sicher, dass Sie die Mindestversionsanforderungen für Microsoft Edge und das Testenddatum überprüfen, um die Eignung der Verwendung der experimentellen APIs auf Ihrer Website zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="b7ff1-113">Ein Experiment kann früher als geplant enden, wenn eine der folgenden Situationen auftritt.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="b7ff1-114">Ein wichtiger Sicherheitsvorfall.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-114">A major security incident.</span></span>  
> *   <span data-ttu-id="b7ff1-115">Wenn genügend Feedback gesammelt wird, das darauf hinweist, dass eine wesentliche Neugestaltung erforderlich ist, um die Anforderungen von Webentwicklern zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="b7ff1-116">In beiden Fällen wird eine Benachrichtigungs-E-Mail an alle Entwickler gesendet, die derzeit für das Experiment registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <a name="register-for-a-trial-of-an-experimental-api"></a><span data-ttu-id="b7ff1-117">Registrieren für eine Testversion einer experimentellen API</span><span class="sxs-lookup"><span data-stu-id="b7ff1-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="b7ff1-118">Verwenden Sie die folgenden Schritte, um sich für eine Testversion einer experimentellen API zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="b7ff1-119">Besuchen Sie die [Seite Microsoft Edge Origin Trials Developer Console.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="b7ff1-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="b7ff1-120">Wählen Sie in einem der verfügbaren Experimente die Schaltfläche Registrieren aus.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="b7ff1-121">Melden Sie sich mit Ihrem GitHub-Benutzernamen und -Kennwort bei der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="b7ff1-122">Wählen **Sie MicrosoftEdge autorisieren aus.**</span><span class="sxs-lookup"><span data-stu-id="b7ff1-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="b7ff1-123">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b7ff1-124">Um eine einzelne oder alle Unterdomänen zu registrieren, wählen Sie Festlegen der `Do you need to match all subdomains for the provided origin?` Einstellung auf `Yes` aus.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="b7ff1-125">Beispielsweise handelt es sich um eine einzelne Domäne und verwendet einen Platzhalter, um alle `https://dev.contoso.com` `https://*.contoso.com` Unterdomänen zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="b7ff1-126">Die folgenden Ursprungsformate sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="b7ff1-127">Angeben eines Unterordners für den Ursprung.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="b7ff1-128">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b7ff1-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="b7ff1-129">Verwenden eines Ursprungs mit Abfragezeichenfolgenparametern.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="b7ff1-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b7ff1-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="b7ff1-131">Wählen **Sie ACCEPT und REGISTER aus.**</span><span class="sxs-lookup"><span data-stu-id="b7ff1-131">Choose **ACCEPT and REGISTER**.</span></span>  
    
### <a name="apply-your-token"></a><span data-ttu-id="b7ff1-132">Anwenden des Tokens</span><span class="sxs-lookup"><span data-stu-id="b7ff1-132">Apply your token</span></span>  

<span data-ttu-id="b7ff1-133">Ein Token wird sofort generiert und auf der [Seite Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="b7ff1-134">Verwenden Sie eine der folgenden Methoden, um die Testversion auf Ihrer Website zu verwenden, um das Token auf Ihre Seite anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="b7ff1-135">Fügen Sie dem Tag auf jeder Seite, die die experimentelle API verwendet, den Attributwert und das Token `origin-trial` `meta` hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="b7ff1-136">Fügen `Origin-Trial` Sie dem HTTP-Antwortheader Ihres Servers hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="b7ff1-137">Ihr Token ist 6 Wochen gültig.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="b7ff1-138">Bevor Ihre Testversion endet, werden Erinnerungs-E-Mails an Sie gesendet, die Um Ihr Feedback bitten und Sie bitten, ihre Testversion zu verlängern, bevor Ihr Token abläuft.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <a name="opt-out-of-an-experiment"></a><span data-ttu-id="b7ff1-139">Abmelden eines Experiments</span><span class="sxs-lookup"><span data-stu-id="b7ff1-139">Opt out of an experiment</span></span>  

<span data-ttu-id="b7ff1-140">Wenn Sie ein Experiment abmelden möchten, verwenden Sie eine der folgenden Methoden, um Ihr Token zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="b7ff1-141">Entfernen Sie `meta` das Tag von jeder Seite, auf der die experimentelle API verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="b7ff1-142">Entfernen `Origin-Trial` Sie aus dem HTTP-Antwortheader Ihres Servers.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a><span data-ttu-id="b7ff1-143">Erkennen experimenteller Features und Bereitstellen eines Fallbacks</span><span class="sxs-lookup"><span data-stu-id="b7ff1-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="b7ff1-144">Stellen Sie bei der Verwendung experimenteller APIs sicher, dass Sie allen Besuchern Ihrer Website eine Arbeitserfahrung bieten.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="b7ff1-145">Besucher können Browser verwenden, die die experimentellen APIs, die Sie Ihrem Code hinzugefügt haben, nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="b7ff1-146">Wenn Ihr Token abläuft, bevor Sie es verlängern, ist die experimentelle API nicht mehr verfügbar, was zu Fehlern führen kann.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="b7ff1-147">Um diese Situation zu vermeiden, stellen Sie sicher, dass Sie features erkennen, die in Ihrem Browser verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="b7ff1-148">Weitere Informationen finden Sie unter Implementieren der [Featureerkennung][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="b7ff1-148">For more information, navigate to [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <a name="roadmap-for-allowed-origins"></a><span data-ttu-id="b7ff1-149">Roadmap für zulässige Ursprünge</span><span class="sxs-lookup"><span data-stu-id="b7ff1-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="b7ff1-150">Das Microsoft Edge Origin Trials-Portal unterstützt heute nur SSL-aktivierte Ursprünge, was bedeutet, dass für Websites HTTPS ordnungsgemäß implementiert sein muss, um sich für ein Experiment registrieren zu können.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="b7ff1-151">In Zukunft sind die folgenden sicheren Ursprünge geplant.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="b7ff1-152">Registrieren `http://localhost` Sie sich als Ursprung für Ihre Experimente.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="b7ff1-153">Navigieren Sie `http://localhost` zu, `edge://flags` und legen Sie das Experiment auf Enabled **(Aktiviert) vor,** um es heute zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-153">To use `http://localhost` today, navigate to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="b7ff1-154">Verwenden Sie Erweiterungen `extensions://` mit präfixen Ursprüngen, um sich für Experimente zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b7ff1-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementieren von Featureerkennungs| MDN"  
