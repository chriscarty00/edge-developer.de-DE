---
description: Dieser Artikel enthält Eine Dokumentation zu den Microsoft Edge-Clienthinweisen und der Benutzer-Agent-Zeichenfolge
title: Erkennen von Microsoft Edge in Ihrer Website
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides, user-agent client hints, user agent client hints, ua client hints, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578779"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a><span data-ttu-id="999ec-104">Erkennen von Microsoft Edge in Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="999ec-104">How to detect Microsoft Edge in your website</span></span>  

<span data-ttu-id="999ec-105">Browser bieten Mechanismen für Websites zum Erkennen von Browserinformationen wie Marke und Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="999ec-105">Browsers provide mechanisms for websites to detect browser information such as brand and version number.</span></span>  <span data-ttu-id="999ec-106">Die Mechanismen erkennen auch andere Gerätemerkmale wie das Hostbetriebssystem.</span><span class="sxs-lookup"><span data-stu-id="999ec-106">The mechanisms also detect other device characteristics like the host operating system.</span></span>  <span data-ttu-id="999ec-107">Zwei solche Mechanismen, die auf Microsoft Edge unterstützt werden, sind [User-Agent-Clienthinweise](#user-agent-client-hints) und [User-Agent-Zeichenfolgen.](#user-agent-string)</span><span class="sxs-lookup"><span data-stu-id="999ec-107">Two such mechanisms supported on Microsoft Edge are [User-Agent Client Hints](#user-agent-client-hints) and [User-Agent strings](#user-agent-string).</span></span>  <span data-ttu-id="999ec-108">Nach einer jahrzehntelangen Verwendung User-Agent Zeichenfolgen veraltet und haben eine lange Vorgeschichte als Ursache für Probleme mit der Websitekompatibilität.</span><span class="sxs-lookup"><span data-stu-id="999ec-108">After decades of use, User-Agent strings are outdated and have a long history as the cause of website compatibility issues.</span></span>  <span data-ttu-id="999ec-109">Stattdessen empfiehlt das Microsoft Edge, einen verbesserten Mechanismus zum Abrufen von Browserinformationen namens [User-Agent Client Hints zu verwenden.](#user-agent-client-hints)</span><span class="sxs-lookup"><span data-stu-id="999ec-109">Instead, the Microsoft Edge team recommends you use an improved mechanism to retrieve browser information named [User-Agent Client Hints](#user-agent-client-hints).</span></span>  <span data-ttu-id="999ec-110">In diesem Artikel werden die beiden Mechanismen beschrieben, die Microsoft Edge zum Abrufen von Benutzer-Agent-Informationen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="999ec-110">This article outlines the two mechanisms Microsoft Edge supports for retrieving user agent information.</span></span>  

|  | <span data-ttu-id="999ec-111">Serverseitig</span><span class="sxs-lookup"><span data-stu-id="999ec-111">Server-side</span></span> | <span data-ttu-id="999ec-112">Clientseitig</span><span class="sxs-lookup"><span data-stu-id="999ec-112">Client-side</span></span> |  
|:--- |:--- |:--- | 
| <span data-ttu-id="999ec-113">**User-Agent-Clienthinweise** \(empfohlen\)</span><span class="sxs-lookup"><span data-stu-id="999ec-113">**User-Agent Client Hints** \(recommended\)</span></span> | `Sec-CH-UA` <span data-ttu-id="999ec-114">HTTPS-Header</span><span class="sxs-lookup"><span data-stu-id="999ec-114">HTTPS header</span></span> | `navigator.userAgentData` <span data-ttu-id="999ec-115">JavaScript-Methode</span><span class="sxs-lookup"><span data-stu-id="999ec-115">JavaScript method</span></span> |  
| <span data-ttu-id="999ec-116">**User-Agent-Zeichenfolge** \(legacy\)</span><span class="sxs-lookup"><span data-stu-id="999ec-116">**User-Agent string** \(legacy\)</span></span> | `User-Agent` <span data-ttu-id="999ec-117">HTTPS-Header</span><span class="sxs-lookup"><span data-stu-id="999ec-117">HTTPS header</span></span> | `navigator.userAgent` <span data-ttu-id="999ec-118">JavaScript-Methode</span><span class="sxs-lookup"><span data-stu-id="999ec-118">JavaScript method</span></span> |  

<span data-ttu-id="999ec-119">Microsoft empfiehlt, die [Featureerkennung nach][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] Möglichkeit aus den folgenden Gründen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="999ec-119">Microsoft recommends that you use [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] whenever possible for the following reasons.</span></span>  

*   <span data-ttu-id="999ec-120">Verbessern Sie die Code-Wartbarkeit.</span><span class="sxs-lookup"><span data-stu-id="999ec-120">Improve code maintainability.</span></span>  
*   <span data-ttu-id="999ec-121">Reduzieren Sie die Anfälligkeit von Code.</span><span class="sxs-lookup"><span data-stu-id="999ec-121">Reduce code fragility.</span></span>  
*   <span data-ttu-id="999ec-122">Reduzieren Sie den Codebruch durch Änderungen an der User-Agent Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="999ec-122">Reduce code breakage from changes to the User-Agent string.</span></span>  
    
<span data-ttu-id="999ec-123">Wenn [die Featureerkennung][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] nicht anwendbar ist und Sie die Benutzer-Agent-Erkennung verwenden müssen, verwenden Sie das folgende Format, um Microsoft Edge-Agent auf Windows und Android zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="999ec-123">When [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable and you must use user agent detection, use the following format to detect Microsoft Edge user agent on Windows and Android.</span></span>  

## <a name="user-agent-client-hints"></a><span data-ttu-id="999ec-124">User-Agent Clienthinweise</span><span class="sxs-lookup"><span data-stu-id="999ec-124">User-Agent Client Hints</span></span>  

<span data-ttu-id="999ec-125">Ab Microsoft Edge Version 90 können Sie auf eine sauberere und datenschutzerhaltende Weise auf Browserinformationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="999ec-125">Starting in Microsoft Edge version 90, access browser information in a cleaner, more privacy-preserving way.</span></span>  

### <a name="user-agent-client-hints-https-header"></a><span data-ttu-id="999ec-126">User-Agent Client hints HTTPS Header</span><span class="sxs-lookup"><span data-stu-id="999ec-126">User-Agent Client Hints HTTPS Header</span></span>  

<span data-ttu-id="999ec-127">Standardmäßig senden Chromium browser einschließlich Microsoft Edge den `Accept-CH-UA` Antwortheader im folgenden Format.</span><span class="sxs-lookup"><span data-stu-id="999ec-127">By default, Chromium browsers including Microsoft Edge send the `Accept-CH-UA` response header in the following format.</span></span>  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> <span data-ttu-id="999ec-128">Clienthinweise werden nur über sichere Verbindungen mit `HTTPS` gesendet.</span><span class="sxs-lookup"><span data-stu-id="999ec-128">Client Hints are only sent over secure connections using `HTTPS`.</span></span>  

<span data-ttu-id="999ec-129">Die folgenden Hinweise zur niedrigen Entropie werden standardmäßig gesendet.</span><span class="sxs-lookup"><span data-stu-id="999ec-129">The following low entropy hints are sent by default.</span></span>  <span data-ttu-id="999ec-130">Wenn Sie auf weitere Informationen zugreifen müssen, senden Sie einen der folgenden Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="999ec-130">If you need to access more information, send one of the following request headers.</span></span>  

#### <a name="user-agent-request-and-response-headers"></a><span data-ttu-id="999ec-131">User-Agent- und Antwortheader</span><span class="sxs-lookup"><span data-stu-id="999ec-131">User-Agent request and response headers</span></span>  

| <span data-ttu-id="999ec-132">Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="999ec-132">Request header</span></span> | <span data-ttu-id="999ec-133">Beispielantwortwert</span><span class="sxs-lookup"><span data-stu-id="999ec-133">Example response value</span></span> |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a><span data-ttu-id="999ec-134">User-Agent Client hints JavaScript API</span><span class="sxs-lookup"><span data-stu-id="999ec-134">User-Agent Client Hints JavaScript API</span></span>  

<span data-ttu-id="999ec-135">Der Standardwert für die Antwort von `navigator.userAgentData` verwendet das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="999ec-135">The default response value from `navigator.userAgentData` uses the following format.</span></span>  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

<span data-ttu-id="999ec-136">Wenn Sie auf ausführlichere Informationen zugreifen müssen, verwenden Sie die [getHighEntropyValues()-Methode.][GithubWicgUaClientHintsGethighentropyvalues]</span><span class="sxs-lookup"><span data-stu-id="999ec-136">If you need to access more detailed information, use the [getHighEntropyValues()][GithubWicgUaClientHintsGethighentropyvalues] method.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="999ec-137">Der folgende Codeausschnitt sendet eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="999ec-137">The following code snippet sends a request.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="999ec-138">So erhalten Sie die folgende Antwort.</span><span class="sxs-lookup"><span data-stu-id="999ec-138">To receive the following response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a><span data-ttu-id="999ec-139">Empfohlene Verwendung von User-Agent Clienthinweisen</span><span class="sxs-lookup"><span data-stu-id="999ec-139">Recommended uses of User-Agent Client Hints</span></span>  

<span data-ttu-id="999ec-140">Der Satz von Marken und die zugeordnete Anzeigereihenfolge ändern sich im Laufe der Zeit, sodass Sie niemals Indizes in das Array der zurückgegebenen Marken hart coden sollten.</span><span class="sxs-lookup"><span data-stu-id="999ec-140">The set of brands and the associated display order change over time, so you should never hard-code indices into the array of returned brands.</span></span>  <span data-ttu-id="999ec-141">Damit Sie ähnliche Probleme frühzeitig auf Ihrer Website erkennen können, enthält der Browser einen Markenwert, der sich im Laufe der Zeit ändert und aufgrund von häufigen Problemen bei der Analyse von Zeichenfolgen als Unterbrechung `GREASE` formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="999ec-141">To help ensure you spot similar issues in your website early, the browser includes a `GREASE` brand value that changes over time and is formatted to break because of common string parsing issues.</span></span>  

<span data-ttu-id="999ec-142">Wenn Sie die Featureerkennung nicht verwenden [können,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]verwenden Sie keine hartcodierte Liste bekannter Chromium Browser für die Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="999ec-142">If you're prevented from using [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection], don't use a hardcoded list of known Chromium-based browsers for verification.</span></span>  <span data-ttu-id="999ec-143">Beispiele für hartcodierte Browsernamen sind `Microsoft Edge` und `Google Chrome` .</span><span class="sxs-lookup"><span data-stu-id="999ec-143">Examples of hardcoded browser names include `Microsoft Edge` and `Google Chrome`.</span></span>  <span data-ttu-id="999ec-144">Gründe, [warum die][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] Featureerkennung nicht anwendbar ist, können die folgende Situation sein.</span><span class="sxs-lookup"><span data-stu-id="999ec-144">Reasons why [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable may include the following situation.</span></span>  

*   <span data-ttu-id="999ec-145">Eine Behebung eines Chromium in einer späteren Version muss vermieden werden, und die betroffenen Browser sind außerhalb einer Überprüfung der Marke und Version schwer zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="999ec-145">A fix for a Chromium bug in a later version must be avoided and the affected browsers are difficult to detect outside of a verification of the brand and version.</span></span>  
    
<span data-ttu-id="999ec-146">Stattdessen sollten Sie die Marke überprüfen, um sicherzustellen, dass Ihre Erkennung für alle betroffenen `Chromium` browserbasierten Chromium gilt.</span><span class="sxs-lookup"><span data-stu-id="999ec-146">Instead, you should verify the `Chromium` brand, which ensures your detection applies to all affected Chromium-based browsers.</span></span>  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a><span data-ttu-id="999ec-147">Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="999ec-147">User agent string</span></span>  

<span data-ttu-id="999ec-148">Nach Möglichkeit empfiehlt Microsoft, die Verwendung Microsoft Edge Browsererkennungslogik basierend auf der Zeichenfolge des Benutzer-Agents zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="999ec-148">Wherever possible, Microsoft recommends you minimize your use of Microsoft Edge browser detection logic based on the user agent string.</span></span>  <span data-ttu-id="999ec-149">Wenn Sie einen guten Grund haben, den Benutzer-Agent zu erkennen, empfiehlt das Microsoft Edge-Team, dass Sie [Benutzer-Agent-Clienthinweise](#user-agent-client-hints) als primäre Erkennungslogik verwenden.</span><span class="sxs-lookup"><span data-stu-id="999ec-149">If you have a good reason to detect the user agent, the Microsoft Edge team recommends you use [User-Agent Client Hints](#user-agent-client-hints) as the primary detection logic.</span></span>  <span data-ttu-id="999ec-150">[Benutzer-Agent-Clienthinweise reduzieren](#user-agent-client-hints) auch die erforderliche Anzahl analysierter Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="999ec-150">[User-Agent Client Hints](#user-agent-client-hints) also reduces the required number of parsed strings.</span></span>  <span data-ttu-id="999ec-151">Für den Legacyverweis wird jedoch das folgende Format für die Zeichenfolge User-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="999ec-151">However, for legacy reference, the following format is used for the User-Agent string.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="999ec-152">Bei Windows verwendet der `User-Agent` HTTP-Anforderungsheader das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="999ec-152">On Windows, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="999ec-153">Unter Android verwendet der `User-Agent` HTTP-Anforderungsheader das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="999ec-153">On Android, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="999ec-154">Der Antwortwert der `navigator.userAgent` Methode verwendet das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="999ec-154">The response value from `navigator.userAgent` method uses the following format.</span></span>  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

<span data-ttu-id="999ec-155">Plattformbezeichner ändern sich basierend auf dem verwendeten Betriebssystem, und die Versionsnummern werden ebenfalls erhöht, sobald die Zeit vergeht.</span><span class="sxs-lookup"><span data-stu-id="999ec-155">Platform identifiers change based on the operating system used, and the version numbers also increment as time passes.</span></span>  <span data-ttu-id="999ec-156">Das Format ist identisch mit dem Chromium Benutzer-Agent, der am Ende ein neues Token `Edg` hinzube kommt.</span><span class="sxs-lookup"><span data-stu-id="999ec-156">The format is the same as the Chromium user agent with the addition of a new `Edg` token at the end.</span></span>  <span data-ttu-id="999ec-157">Microsoft hat das Token ausgewählt, um Kompatibilitätsprobleme zu vermeiden, die durch eine Zeichenfolge verursacht wurden, die Microsoft Edge EdgeHTML verwendet `Edg` `Edge` wurde.</span><span class="sxs-lookup"><span data-stu-id="999ec-157">Microsoft chose the `Edg` token to avoid compatibility issues caused by `Edge` string, which was used legacy Microsoft Edge browser based on EdgeHTML.</span></span>  <span data-ttu-id="999ec-158">Das `Edg` Token entspricht auch vorhandenen [Token,][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] die unter iOS und Android verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="999ec-158">The `Edg` token is also consistent with [existing tokens][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] used on iOS and Android.</span></span>

## <a name="map-the-user-agent-string-to-browser-name"></a><span data-ttu-id="999ec-159">Ordnen Sie die Zeichenfolge des Benutzer-Agents dem Browsernamen zu.</span><span class="sxs-lookup"><span data-stu-id="999ec-159">Map the user agent string to browser name</span></span>  

<span data-ttu-id="999ec-160">Ordnen Sie die Zeichenfolgentoken des Benutzer-Agents einem besser lesbaren Browsernamen zu, der im Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="999ec-160">Map the user agent string tokens to a more human-readable browser name to use in code.</span></span>  <span data-ttu-id="999ec-161">Es ist heute ein gängiges Muster im Web.</span><span class="sxs-lookup"><span data-stu-id="999ec-161">It's a common pattern on the web today.</span></span>  <span data-ttu-id="999ec-162">Wenn Sie das neue Token einem Browsernamen zuordnungen, empfiehlt Microsoft, einen anderen Namen als den für den älteren Microsoft Edge-Browser verwendeten Namen zu verwenden, um zu vermeiden, dass versehentlich ältere Problemumgehungen angewendet werden, die für Chromium-basierte Browser nicht anwendbar `Edg` sind.</span><span class="sxs-lookup"><span data-stu-id="999ec-162">When you map the new `Edg` token to a browser name, Microsoft recommends that you use a different name than the one used for the legacy Microsoft Edge browser to avoid accidentally applying any legacy workarounds that aren't applicable to Chromium-based browsers.</span></span>

## <a name="user-agent-overrides"></a><span data-ttu-id="999ec-163">Außerkraftsetzungen des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="999ec-163">User Agent overrides</span></span>  

<span data-ttu-id="999ec-164">Manchmal erkennt eine Website den neuen Microsoft Edge-Agent nicht.</span><span class="sxs-lookup"><span data-stu-id="999ec-164">Sometimes, a website doesn't recognize the new Microsoft Edge user agent.</span></span>  <span data-ttu-id="999ec-165">Dies führt dazu, dass eine Reihe von Features der Website möglicherweise nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="999ec-165">As a result, a set of the features of the website may not work correctly.</span></span>  <span data-ttu-id="999ec-166">Wenn Microsoft über die Arten von Problemen benachrichtigt wird, kontaktiert Microsoft Sie \(ein Websitebesitzer\) und informiert Sie über den aktualisierten Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="999ec-166">When Microsoft is notified about the types of issues, Microsoft contacts you \(a website owner\) and informs you about the updated user agent.</span></span>  

<span data-ttu-id="999ec-167">Möglicherweise benötigen Sie mehr Zeit, um die Erkennungslogik des Benutzer-Agents für Ihre Website zu aktualisieren und zu testen, um die von Microsoft gemeldeten Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="999ec-167">You may need more time to update and test the user agent detection logic for your website to address the issues reported by Microsoft.</span></span>  <span data-ttu-id="999ec-168">Um die Kompatibilität für Ihre Benutzer zu maximieren, verwenden Microsoft Edge Beta und Stable eine Liste von Außerkraftsetzungen des Benutzer-Agents.</span><span class="sxs-lookup"><span data-stu-id="999ec-168">To maximize compatibility for your users, the Microsoft Edge Beta and Stable channels use a list of user agent overrides.</span></span>  <span data-ttu-id="999ec-169">Verwenden Sie die Außerkraftsetzungen des Benutzer-Agents, während Sie Ihre Website aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="999ec-169">Use the user agent overrides while you update your website.</span></span>  <span data-ttu-id="999ec-170">Die Liste der von Microsoft bereitgestellten Außerkraftsetzungen des Benutzer-Agents.</span><span class="sxs-lookup"><span data-stu-id="999ec-170">The list of user agent overrides provided by Microsoft.</span></span>  

<span data-ttu-id="999ec-171">Die Außerkraftsetzungen geben neue Benutzer-Agent-Werte an, die Microsoft Edge anstelle des Standardbenutzer-Agents für bestimmte Websites senden.</span><span class="sxs-lookup"><span data-stu-id="999ec-171">The overrides specify new user agent values that Microsoft Edge sends instead of the default user agent for specific websites.</span></span>  <span data-ttu-id="999ec-172">Führen Sie die folgenden Aktionen aus, um die Liste der derzeit angewendeten Benutzer-Agent-Überschreibungen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="999ec-172">To display the list of user agent overrides that are currently applied, complete the following actions.</span></span>  

1.  <span data-ttu-id="999ec-173">Öffnen Sie Microsoft Edge Beta oder Stable-Kanal.</span><span class="sxs-lookup"><span data-stu-id="999ec-173">Open the Microsoft Edge Beta or Stable channel.</span></span>  
1.  <span data-ttu-id="999ec-174">Navigieren Sie zu `edge://compat/useragent`.</span><span class="sxs-lookup"><span data-stu-id="999ec-174">Navigate to `edge://compat/useragent`.</span></span>  
    
<span data-ttu-id="999ec-175">Die Microsoft Edge Canary- und Dev-Kanäle empfangen derzeit keine Außerkraftsetzungen des Benutzer-Agents.</span><span class="sxs-lookup"><span data-stu-id="999ec-175">The Microsoft Edge Canary and Dev channels don't currently receive user agent overrides.</span></span>  <span data-ttu-id="999ec-176">Die Microsoft Edge Canary- und Dev-Kanäle stellen Umgebungen bereit, die den Standardbenutzer-agent Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="999ec-176">The Microsoft Edge Canary and Dev channels provide environments that use the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="999ec-177">Verwenden Sie Microsoft Edge Canary- und Dev-Kanäle, um Probleme auf Ihrer Website zu reproduzieren, die durch den Standardbenutzer-Agent Microsoft Edge werden.</span><span class="sxs-lookup"><span data-stu-id="999ec-177">Use the Microsoft Edge Canary and Dev channels to easily reproduce issues on your website caused by the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="999ec-178">Führen Sie die folgenden Aktionen aus, um Außerkraftsetzungen des Benutzer-Agents in Microsoft Edge Beta oder Stable-Kanälen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="999ec-178">To turn off user agent overrides in the Microsoft Edge Beta or Stable channels, complete the following actions.</span></span>  

1.  <span data-ttu-id="999ec-179">Öffnen Sie Ihre Befehlszeilen-App.</span><span class="sxs-lookup"><span data-stu-id="999ec-179">Open your command-line app.</span></span>  
1.  <span data-ttu-id="999ec-180">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="999ec-180">Copy and paste the following code snippet.</span></span>  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  <span data-ttu-id="999ec-181">Führen Sie die Microsoft Edge-App mithilfe des Codeausschnitts aus.</span><span class="sxs-lookup"><span data-stu-id="999ec-181">Run the Microsoft Edge app using the code snippet.</span></span>  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge für iOS und Android: Was Entwickler über ihre | Microsoft Windows Blogs"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. getHighEntropyValues-Methode – User-Agent Clienthinweise | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementieren von Featureerkennungs| MDN"  
