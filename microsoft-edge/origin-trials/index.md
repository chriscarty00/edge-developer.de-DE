---
ms.assetid: ''
description: Safely experiment for a fixed period of time and provide feedback on new platform features.
title: Origin Trials
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, origin trials, developer
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846528"
---
# <span data-ttu-id="8df08-104">Use Origin Trials in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8df08-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="8df08-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span><span class="sxs-lookup"><span data-stu-id="8df08-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="8df08-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span><span class="sxs-lookup"><span data-stu-id="8df08-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="8df08-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span><span class="sxs-lookup"><span data-stu-id="8df08-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="8df08-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="8df08-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="8df08-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span><span class="sxs-lookup"><span data-stu-id="8df08-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="8df08-110">Get started using Origin Trials</span><span class="sxs-lookup"><span data-stu-id="8df08-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="8df08-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="8df08-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="8df08-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span><span class="sxs-lookup"><span data-stu-id="8df08-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="8df08-113">An experiment may end earlier than planned if any of the following situations occur.</span><span class="sxs-lookup"><span data-stu-id="8df08-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="8df08-114">A major security incident.</span><span class="sxs-lookup"><span data-stu-id="8df08-114">A major security incident.</span></span>  
> *   <span data-ttu-id="8df08-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span><span class="sxs-lookup"><span data-stu-id="8df08-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="8df08-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span><span class="sxs-lookup"><span data-stu-id="8df08-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="8df08-117">Register for a trial of an experimental API</span><span class="sxs-lookup"><span data-stu-id="8df08-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="8df08-118">Use the following steps to register for a trial of an experimental API.</span><span class="sxs-lookup"><span data-stu-id="8df08-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="8df08-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span><span class="sxs-lookup"><span data-stu-id="8df08-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="8df08-120">Choose the Register button on any of the available experiments.</span><span class="sxs-lookup"><span data-stu-id="8df08-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="8df08-121">Sign into the Developer Console using your GitHub username and password.</span><span class="sxs-lookup"><span data-stu-id="8df08-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="8df08-122">Choose **Authorize MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="8df08-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="8df08-123">Complete the form.</span><span class="sxs-lookup"><span data-stu-id="8df08-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8df08-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span><span class="sxs-lookup"><span data-stu-id="8df08-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="8df08-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span><span class="sxs-lookup"><span data-stu-id="8df08-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="8df08-126">The following origin formats are not allowed.</span><span class="sxs-lookup"><span data-stu-id="8df08-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="8df08-127">Specifying a subfolder on the origin.</span><span class="sxs-lookup"><span data-stu-id="8df08-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="8df08-128">For example,</span><span class="sxs-lookup"><span data-stu-id="8df08-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="8df08-129">Using an origin with query string parameters.</span><span class="sxs-lookup"><span data-stu-id="8df08-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="8df08-130">For example,</span><span class="sxs-lookup"><span data-stu-id="8df08-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="8df08-131">Choose **ACCEPT and REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="8df08-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="8df08-132">Apply your token</span><span class="sxs-lookup"><span data-stu-id="8df08-132">Apply your token</span></span>  

<span data-ttu-id="8df08-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span><span class="sxs-lookup"><span data-stu-id="8df08-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="8df08-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span><span class="sxs-lookup"><span data-stu-id="8df08-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="8df08-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span><span class="sxs-lookup"><span data-stu-id="8df08-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="8df08-136">Add `Origin-Trial` to the HTTP response header of your server.</span><span class="sxs-lookup"><span data-stu-id="8df08-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="8df08-137">Your token is valid for 6 weeks.</span><span class="sxs-lookup"><span data-stu-id="8df08-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="8df08-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span><span class="sxs-lookup"><span data-stu-id="8df08-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="8df08-139">Opt out of an experiment</span><span class="sxs-lookup"><span data-stu-id="8df08-139">Opt out of an experiment</span></span>  

<span data-ttu-id="8df08-140">To opt out of an experiment, use one of the following methods to remove your token.</span><span class="sxs-lookup"><span data-stu-id="8df08-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="8df08-141">Remove the `meta` tag from every page that used the experimental API.</span><span class="sxs-lookup"><span data-stu-id="8df08-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="8df08-142">Remove `Origin-Trial` from the HTTP response header of your server.</span><span class="sxs-lookup"><span data-stu-id="8df08-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="8df08-143">Detect experimental features and provide a fallback</span><span class="sxs-lookup"><span data-stu-id="8df08-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="8df08-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span><span class="sxs-lookup"><span data-stu-id="8df08-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="8df08-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span><span class="sxs-lookup"><span data-stu-id="8df08-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="8df08-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span><span class="sxs-lookup"><span data-stu-id="8df08-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="8df08-147">To avoid this situation, ensure you detect features available in your browser.</span><span class="sxs-lookup"><span data-stu-id="8df08-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="8df08-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="8df08-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="8df08-149">Roadmap for Allowed Origins</span><span class="sxs-lookup"><span data-stu-id="8df08-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="8df08-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span><span class="sxs-lookup"><span data-stu-id="8df08-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="8df08-151">In the future, the following secure origins are planned.</span><span class="sxs-lookup"><span data-stu-id="8df08-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="8df08-152">Register `http://localhost` as the origin for your experiments.</span><span class="sxs-lookup"><span data-stu-id="8df08-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="8df08-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="8df08-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="8df08-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span><span class="sxs-lookup"><span data-stu-id="8df08-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementing feature detection | MDN"  
