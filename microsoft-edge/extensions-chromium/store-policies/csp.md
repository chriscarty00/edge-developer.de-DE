---
description: Inhaltssicherheitsrichtlinie für Edgeerweiterungen (Chromium).
title: Inhaltssicherheitsrichtlinie (Content Security Policy, CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397517"
---
# <a name="content-security-policy-csp"></a><span data-ttu-id="31cd4-104">Inhaltssicherheitsrichtlinie \(CSP\)</span><span class="sxs-lookup"><span data-stu-id="31cd4-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="31cd4-105">Um eine große Klasse potenzieller websiteübergreifender Skriptingprobleme zu beheben, hat das Microsoft Edge Extension-System das allgemeine Konzept der Inhaltssicherheitsrichtlinie [\(CSP\) integriert.][W3CContentSecurityPolicy]</span><span class="sxs-lookup"><span data-stu-id="31cd4-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="31cd4-106">Dies führt einige ziemlich strenge Richtlinien ein, die Erweiterungen standardmäßig sicherer machen, und bietet Ihnen die Möglichkeit, Regeln für die Inhaltstypen zu erstellen und zu erzwingen, die von Ihren Erweiterungen und Anwendungen geladen und ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="31cd4-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="31cd4-107">Im Allgemeinen funktioniert CSP als Block-/Allowlisting-Mechanismus für Ressourcen, die von Ihren Erweiterungen geladen oder ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="31cd4-108">Wenn Sie eine angemessene Richtlinie für Ihre Erweiterung definieren, können Sie die Für ihre Erweiterung benötigten Ressourcen sorgfältig berücksichtigen und den Browser bitten, sicherzustellen, dass diese Ressourcen die einzigen Ressourcen sind, auf die Ihre Erweiterung Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="31cd4-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="31cd4-109">Die Richtlinien bieten Sicherheit über die Hostberechtigungen, die Ihre Erweiterung anfordert. Sie sind eine zusätzliche Schutzebene, keine Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="31cd4-109">The policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="31cd4-110">Im Web wird eine solche Richtlinie über einen HTTP-Header oder -Element `meta` definiert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="31cd4-111">Innerhalb des Microsoft Edge Extension-Systems ist keine der beiden Mechanismen geeignet.</span><span class="sxs-lookup"><span data-stu-id="31cd4-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="31cd4-112">Stattdessen wird eine Erweiterungsrichtlinie mithilfe der Datei für die `manifest.json` Erweiterung wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="31cd4-112">Instead, an Extension policy is defined using the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="31cd4-113">Ausführliche Informationen zur #A0 finden Sie in [][W3CContentSecurityPolicy] der Spezifikation für Inhaltssicherheitsrichtlinien und im Artikel ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] auf HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="31cd4-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <a name="default-policy-restrictions"></a><span data-ttu-id="31cd4-114">Standardrichtlinieneinschränkungen</span><span class="sxs-lookup"><span data-stu-id="31cd4-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="31cd4-115">Pakete, die keine `manifest_version` definieren, verfügen nicht über eine Standardrichtlinie für die Inhaltssicherheit.</span><span class="sxs-lookup"><span data-stu-id="31cd4-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="31cd4-116">Pakete, die `manifest_version` 2 auswählen, verfügen über die folgende Standardrichtlinie für die Inhaltssicherheit.</span><span class="sxs-lookup"><span data-stu-id="31cd4-116">Packages that choose `manifest_version` 2, have a the follwoing default content security policy.</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="31cd4-117">Die Richtlinie erhöht die Sicherheit, indem Erweiterungen und Anwendungen auf drei Arten eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="31cd4-117">The policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="31cd4-118">Eval und zugehörige Funktionen sind deaktiviert</span><span class="sxs-lookup"><span data-stu-id="31cd4-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="31cd4-119">Code wie der folgende funktioniert nicht:</span><span class="sxs-lookup"><span data-stu-id="31cd4-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="31cd4-120">Die Auswertung von Zeichenfolgen von JavaScript wie dieser ist ein gängiger XSS-Angriffsvektor.</span><span class="sxs-lookup"><span data-stu-id="31cd4-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="31cd4-121">Stattdessen sollten Sie Code wie:</span><span class="sxs-lookup"><span data-stu-id="31cd4-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="31cd4-122">Inline-JavaScript wird nicht ausgeführt</span><span class="sxs-lookup"><span data-stu-id="31cd4-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="31cd4-123">Inline-JavaScript wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="31cd4-124">Diese Einschränkung verbietet sowohl Inlineblöcke als auch `<script>` Inlineereignishandler, z. B. `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="31cd4-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="31cd4-125">Mit der ersten Einschränkung wird eine große Klasse von websiteübergreifenden Skriptangriffen gelöscht, da es Ihnen nicht möglich ist, das skript versehentlich auszuführen, das von einem böswilligen Drittanbieter bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="31cd4-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="31cd4-126">Es ist jedoch erforderlich, dass Sie Ihren Code mit einer sauberen Trennung zwischen Inhalt und Verhalten \(was Sie natürlich trotzdem tun sollten, richtig?\) schreiben.</span><span class="sxs-lookup"><span data-stu-id="31cd4-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="31cd4-127">Ein Beispiel kann dies deutlicher machen.</span><span class="sxs-lookup"><span data-stu-id="31cd4-127">An example may make this clearer.</span></span>  <span data-ttu-id="31cd4-128">Sie können versuchen, ein Browseraktion-Popup als einzelnes Popup zu schreiben, `pop-up.html` das:</span><span class="sxs-lookup"><span data-stu-id="31cd4-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

<span data-ttu-id="31cd4-129">Drei Dinge müssen sich ändern, damit dies so funktioniert, wie Sie es erwarten:</span><span class="sxs-lookup"><span data-stu-id="31cd4-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="31cd4-130">Die `clickHandler` Definition muss in eine externe JavaScript-Datei \( verschoben werden. `popup.js`</span><span class="sxs-lookup"><span data-stu-id="31cd4-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="31cd4-131">Die Inlineereignishandlerdefinitionen müssen im Sinne von umgeschrieben und in `addEventListener` extrahiert `popup.js` werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="31cd4-132">Wenn Sie Ihr Programm derzeit mit Code wie starten, sollten Sie es ersetzen, indem Sie es je nach Ihren Anforderungen in das Dokumentereignis oder das Ereignis des `<body onload="main();">` `DOMContentLoaded` `load` Fensters einhaken.</span><span class="sxs-lookup"><span data-stu-id="31cd4-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="31cd4-133">Verwenden Sie erstere, da sie im Allgemeinen schneller ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="31cd4-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="31cd4-134">Der `setTimeout` Aufruf muss umgeschrieben werden, um zu vermeiden, dass die Zeichenfolge zur Ausführung in `"awesome(); totallyAwesome()"` JavaScript konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="31cd4-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="31cd4-135">Diese Änderungen können etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="31cd4-135">Those changes may look something like the following:</span></span>  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**<span data-ttu-id="31cd4-136">Nur lokale Skript- und Objektressourcen werden geladen</span><span class="sxs-lookup"><span data-stu-id="31cd4-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="31cd4-137">Skript- und Objektressourcen können nur aus dem Erweiterungspaket geladen werden, nicht aus dem Web.</span><span class="sxs-lookup"><span data-stu-id="31cd4-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="31cd4-138">Dadurch wird sichergestellt, dass ihre Erweiterung nur den speziell genehmigten Code ausgeführt, um zu verhindern, dass ein aktiver Netzwerkangreifer Ihre Anforderung für eine Ressource böswillig umleiten kann.</span><span class="sxs-lookup"><span data-stu-id="31cd4-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="31cd4-139">Anstatt Code zu schreiben, der vom Laden von jQuery \(oder einer anderen Bibliothek\) aus einem externen CDN abhängt, sollten Sie erwägen, die spezifische Version von jQuery in Das Erweiterungspaket zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="31cd4-140">Das heißt, anstatt:</span><span class="sxs-lookup"><span data-stu-id="31cd4-140">That is, instead of:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

<span data-ttu-id="31cd4-141">Laden Sie die Datei herunter, fügen Sie sie in Ihr Paket ein, und schreiben Sie:</span><span class="sxs-lookup"><span data-stu-id="31cd4-141">Download the file, include it in your package, and write:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## <a name="relaxing-the-default-policy"></a><span data-ttu-id="31cd4-142">Lockern der Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="31cd4-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="31cd4-143">Inlineskript</span><span class="sxs-lookup"><span data-stu-id="31cd4-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="31cd4-144">Inlineskripts können zulässig sein, indem der base64-codierte Hash des Quellcodes in der Richtlinie angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31cd4-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="31cd4-145">Diesem Hash muss der verwendete Hashalgorithmus \(sha256, sha384 oder sha512\) vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="31cd4-146">Navigieren Sie beispielsweise zu [Hashverwendung für \<script\> Elemente][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span><span class="sxs-lookup"><span data-stu-id="31cd4-146">For an example, navigate to [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span></span>  

**<span data-ttu-id="31cd4-147">Remoteskript</span><span class="sxs-lookup"><span data-stu-id="31cd4-147">Remote Script</span></span>**  

<span data-ttu-id="31cd4-148">Wenn Sie externe JavaScript- oder Objektressourcen benötigen, können Sie die Richtlinie in begrenztem Umfang lockern, indem Sie sichere Ursprünge zulassen, von denen Skripts akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31cd4-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="31cd4-149">Stellen Sie sicher, dass Laufzeitressourcen, die mit erhöhten Berechtigungen einer Erweiterung geladen werden, genau die Ressourcen sind, die Sie erwarten, und nicht durch einen aktiven Netzwerkangreifer ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="31cd4-150">Da [Man-in-the-Middle-Angriffe][WikiManMiddleAttacks] sowohl trivial als auch über HTTP nicht nachweisbar sind, werden diese Ursprünge nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="31cd4-151">Derzeit können Entwickler Die Ursprünge der Liste mit den folgenden Schemas zulassen: `blob` , , , und `filesystem` `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="31cd4-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="31cd4-152">Der Hostteil des Ursprungs muss explizit für die `https` Und-Schemas angegeben `extension` werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="31cd4-153">Generische Platzhalter wie https:, und sind nicht `https://*` `https://*.com` zulässig. Unterdomänen-Platzhalter wie `https://*.example.com` sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="31cd4-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="31cd4-154">Domänen in der [Liste öffentliches Suffix][PublicSuffixList] werden auch als generische Domänen auf oberster Ebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="31cd4-155">Zum Laden einer Ressource aus diesen Domänen muss die Unterdomäne explizit aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="31cd4-156">Ist z. `https://*.cloudfront.net` B. nicht gültig, `https://XXXX.cloudfront.net` kann aber auch `https://*.XXXX.cloudfront.net` `allowlisted` sein.</span><span class="sxs-lookup"><span data-stu-id="31cd4-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be `allowlisted`.</span></span>  

<span data-ttu-id="31cd4-157">Zur Erleichterung der Entwicklung können Ressourcen, die über HTTP von Servern auf Ihrem lokalen Computer geladen werden, `allowlisted` sein.</span><span class="sxs-lookup"><span data-stu-id="31cd4-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be `allowlisted`.</span></span>  <span data-ttu-id="31cd4-158">Sie können Skript- und Objektquellen für einen beliebigen Port von oder `http://127.0.0.1` `http://localhost` zulassen.</span><span class="sxs-lookup"><span data-stu-id="31cd4-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="31cd4-159">Die Einschränkung für über HTTP geladene Ressourcen gilt nur für die Ressourcen, die direkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="31cd4-160">Beispielsweise können Sie weiterhin Verbindungen zu beliebigen Ursprüngen herstellen. Die Standardrichtlinie schränkt keine oder keine der anderen `XMLHTTPRequest` `connect-src` #A0 ein.</span><span class="sxs-lookup"><span data-stu-id="31cd4-160">You are still free, for example, to make `XMLHTTPRequest` connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="31cd4-161">Eine lockere Richtliniendefinition, die das Laden von Skriptressourcen von `example.com` über HTTPS ermöglicht, kann wie dies aussehen:</span><span class="sxs-lookup"><span data-stu-id="31cd4-161">A relaxed policy definition which allows script resources to be loaded from `example.com` over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="31cd4-162">Beide `script-src` und werden durch die Richtlinie `object-src` definiert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="31cd4-163">Microsoft Edge akzeptiert keine Richtlinie, die nicht jeden dieser Werte auf \(mindestens\) ' ' `self` eingrenzt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="31cd4-164">Ausgewertetes JavaScript</span><span class="sxs-lookup"><span data-stu-id="31cd4-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="31cd4-165">Die Richtlinie für und zugehörige Funktionen wie , und können durch Hinzufügen zu `eval()` `setTimeout(String)` Ihrer Richtlinie `setInterval(String)` `new Function(String)` `unsafe-eval` gelockert werden:</span><span class="sxs-lookup"><span data-stu-id="31cd4-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="31cd4-166">Sie sollten jedoch lockere Richtlinien vermeiden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-166">However, you should avoid relaxing policies.</span></span>  <span data-ttu-id="31cd4-167">Die Funktionen sind berüchtigte XSS-Angriffsvektoren.</span><span class="sxs-lookup"><span data-stu-id="31cd4-167">The functions are notorious XSS attack vectors.</span></span>  

## <a name="tightening-the-default-policy"></a><span data-ttu-id="31cd4-168">Straffen der Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="31cd4-168">Tightening the default policy</span></span>  

<span data-ttu-id="31cd4-169">Sie können diese Richtlinie natürlich in dem Umfang festziehen, den Ihre Erweiterung zulässt, um die Sicherheit auf Kosten der Benutzerfreundlichkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="31cd4-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="31cd4-170">Um anzugeben, dass Ihre Erweiterung nur Ressourcen eines beliebigen Typs \(Bilder und so weiter\) aus dem zugeordneten Erweiterungspaket laden kann, kann beispielsweise eine Richtlinie von `default-src 'self'` geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="31cd4-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a><span data-ttu-id="31cd4-171">Inhaltsskripts</span><span class="sxs-lookup"><span data-stu-id="31cd4-171">Content Scripts</span></span>  

<span data-ttu-id="31cd4-172">Die zu besprechende Richtlinie gilt für die Hintergrund- und Ereignisseiten der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="31cd4-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="31cd4-173">Die Anwendung der Inhaltsskripts auf die Inhaltsskripts der Erweiterung ist komplizierter.</span><span class="sxs-lookup"><span data-stu-id="31cd4-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="31cd4-174">Inhaltsskripts unterliegen im Allgemeinen nicht dem CSP der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="31cd4-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="31cd4-175">Da Inhaltsskripts keine HTML sind, besteht der Hauptauswirkungen davon, dass sie auch dann verwendet werden können, wenn der CSP der Erweiterung nicht angegeben wird, obwohl dies `eval` `unsafe-eval` nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="31cd4-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="31cd4-176">Darüber hinaus gilt der CSP der Seite nicht für Inhaltsskripts.</span><span class="sxs-lookup"><span data-stu-id="31cd4-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="31cd4-177">Komplizierter sind Tags, die Inhaltsskripts erstellen und in das DOM der Seite setzen, `<script>` auf der sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="31cd4-178">Diese werden in Zukunft als DOM-injizierte Skripts referenziert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="31cd4-179">DOM-injizierte Skripts, die unmittelbar nach dem Einspritzen in die Seite ausgeführt werden, werden erwartungsgleich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="31cd4-180">Stellen Sie sich ein Inhaltsskript mit dem folgenden Code als einfaches Beispiel vor:</span><span class="sxs-lookup"><span data-stu-id="31cd4-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="31cd4-181">Dieses Inhaltsskript bewirkt eine `alert` unmittelbar nach dem `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="31cd4-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="31cd4-182">Beachten Sie, dass dies unabhängig von der Richtlinie ausgeführt wird, die von einer Seite angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="31cd4-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="31cd4-183">Das Verhalten wird jedoch sowohl innerhalb dieses DOM-injizierten Skripts als auch für alle Skripts, die nicht sofort nach der Einspritzung ausgeführt werden, komplizierter.</span><span class="sxs-lookup"><span data-stu-id="31cd4-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="31cd4-184">Stellen Sie sich vor, Ihre Erweiterung wird auf einer Seite ausgeführt, die einen zugeordneten CSP enthält, der `script-src 'self'` angibt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="31cd4-185">Stellen Sie sich nun vor, das Inhaltsskript führt den folgenden Code aus:</span><span class="sxs-lookup"><span data-stu-id="31cd4-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="31cd4-186">Wenn ein Benutzer diese Schaltfläche aus wählt, wird das `onclick` Skript nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-186">If a user chooses that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="31cd4-187">Dies liegt daran, dass das Skript nicht sofort ausgeführt wurde und Code erst interpretiert wird, wenn das Ereignis als Teil des Inhaltsskripts betrachtet wird, sodass der CSP der Seite \(nicht der Erweiterung\) das Verhalten `click` einschränkt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-187">This is because the script did not immediately run and code is not interpreted until the `click` event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="31cd4-188">Und da dieser CSP keine Angabe macht, wird der `unsafe-inline` Inlineereignishandler blockiert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="31cd4-189">Die richtige Möglichkeit, das gewünschte Verhalten in diesem Fall zu implementieren, kann sein, den Handler wie eine Funktion aus dem `onclick` Inhaltsskript wie folgt hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="31cd4-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="31cd4-190">Ein weiteres ähnliches Problem tritt auf, wenn das Inhaltsskript Folgendes ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="31cd4-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="31cd4-191">In diesem Fall wird das Skript ausgeführt und die Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31cd4-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="31cd4-192">Gehen Sie jedoch wie in diesem Fall vor:</span><span class="sxs-lookup"><span data-stu-id="31cd4-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="31cd4-193">Während das erste Skript ausgeführt wird, wird der `eval` Aufruf von blockiert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="31cd4-194">Das heißt, während die anfängliche Skriptlaufzeit zulässig ist, wird das Verhalten innerhalb des Skripts durch den CSP der Seite reguliert.</span><span class="sxs-lookup"><span data-stu-id="31cd4-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="31cd4-195">Je nachdem, wie Sie dominjizierte Skripts in Ihre Erweiterung schreiben, können Änderungen am CSP der Seite das Verhalten Ihrer Erweiterung beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="31cd4-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="31cd4-196">Da Inhaltsskripts nicht vom CSP der Seite betroffen sind, ist dies ein guter Grund, um so viel Verhalten wie möglich ihrer Erweiterung in das Inhaltsskript anstelle von DOM-injizierten Skripts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Eine Einführung in die Inhaltssicherheitsrichtlinie | HTML5-Rock"  
[PublicSuffixList]: https://publicsuffix.org/list "ANZEIGEN DER ÖFFENTLICHEN SUFFIXLISTE"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Hashverwendung für \<Script\>-Elemente – Inhaltssicherheitsrichtlinie Ebene 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Inhaltssicherheitsrichtlinie Ebene 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Man-in-the-Middle-| Wikipedia"  

> [!NOTE]
> <span data-ttu-id="31cd4-202">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31cd4-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="31cd4-203">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="31cd4-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="31cd4-205">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31cd4-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
