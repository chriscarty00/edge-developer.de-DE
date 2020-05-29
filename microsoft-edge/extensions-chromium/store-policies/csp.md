---
description: Inhalts Sicherheitsrichtlinie für Edge (Chrom)-Erweiterungen.
title: Inhalts Sicherheitsrichtlinie (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 52d6d0afb38401250183788726013d521a269f06
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567473"
---
# <span data-ttu-id="c9e7e-104">Inhalts Sicherheitsrichtlinie \ (CSP \)</span><span class="sxs-lookup"><span data-stu-id="c9e7e-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="c9e7e-105">Um eine große Klasse potenzieller Probleme mit Website übergreifendem Skripting zu verringern, hat das Microsoft Edge-Erweiterungssystem das allgemeine Konzept der [Inhalts Sicherheitsrichtlinie (CSP \)][W3CContentSecurityPolicy]übernommen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="c9e7e-106">Dies führt einige ziemlich strenge Richtlinien ein, die Erweiterungen standardmäßig sicherer machen, und bietet Ihnen die Möglichkeit, Regeln für die Typen von Inhalten zu erstellen und zu erzwingen, die von ihren Erweiterungen und Anwendungen geladen und ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="c9e7e-107">Im Allgemeinen funktioniert CSP als Block-allowlisting-Mechanismus für Ressourcen, die von ihren Erweiterungen geladen oder ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="c9e7e-108">Wenn Sie eine angemessene Richtlinie für Ihre Erweiterung definieren, können Sie die Ressourcen, die ihre Erweiterung erfordert, sorgfältig berücksichtigen und den Browser bitten, sicherzustellen, dass dies die einzigen Ressourcen ist, auf die ihre Erweiterung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="c9e7e-109">Diese Richtlinien bieten Sicherheit über die Host Berechtigungen für Ihre Erweiterungsanforderungen. Es handelt sich um eine zusätzliche Schutzebene, die nicht ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-109">These policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="c9e7e-110">Im Web wird eine solche Richtlinie über einen HTTP-Header oder- `meta` Element definiert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="c9e7e-111">Innerhalb des Microsoft Edge-Erweiterungssystems ist kein geeigneter Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="c9e7e-112">Stattdessen wird eine Erweiterungs Richtlinie über die `manifest.json` Datei für die Erweiterung wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-112">Instead, an Extension policy is defined via the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="c9e7e-113">Ausführliche Informationen zur CSP-Syntax finden Sie in der [Inhalts Sicherheitsrichtlinien-Spezifikation][W3CContentSecurityPolicy] und im Artikel ["eine Einführung in die Inhaltssicherheit"][HTML5RocksIntroductionContentSecurityPolicy] auf HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <span data-ttu-id="c9e7e-114">Standardmäßige Richtlinieneinschränkungen</span><span class="sxs-lookup"><span data-stu-id="c9e7e-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="c9e7e-115">Pakete, die keine definieren, `manifest_version` verfügen nicht über eine Standardrichtlinie für Inhaltssicherheit.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="c9e7e-116">Für diejenigen, die `manifest_version` 2 auswählen, gibt es eine Standardrichtlinie für Inhaltssicherheit:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-116">Those that select `manifest_version` 2, have a default content security policy of:</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="c9e7e-117">Diese Richtlinie bietet Sicherheit, indem Erweiterungen und Anwendungen auf drei Arten eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-117">This policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="c9e7e-118">Eval und verwandte Funktionen sind deaktiviert</span><span class="sxs-lookup"><span data-stu-id="c9e7e-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="c9e7e-119">Code wie den folgenden funktioniert nicht:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="c9e7e-120">Die Auswertung von Zeichenfolgen mit JavaScript wie diesem ist ein häufig verwendeter XSS-Angriffsvektor.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="c9e7e-121">Stattdessen sollten Sie Code wie folgt schreiben:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="c9e7e-122">Inline-JavaScript wird nicht ausgeführt</span><span class="sxs-lookup"><span data-stu-id="c9e7e-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="c9e7e-123">Inline-JavaScript wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="c9e7e-124">Diese Einschränkung `<script>` verbietet sowohl Inline Blöcke als auch Inline-Ereignishandler wie `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="c9e7e-125">Mit der ersten Einschränkung wird eine große Klasse von websiteübergreifenden Skripting-Angriffen gelöscht, da Sie das Skript, das von einem böswilligen Drittanbieter bereitgestellt wird, nicht versehentlich ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="c9e7e-126">Allerdings ist es erforderlich, dass Sie Ihren Code mit einer sauberen Trennung zwischen Inhalt und Verhalten schreiben \ (was Sie natürlich ohnehin tun sollten, oder? \).</span><span class="sxs-lookup"><span data-stu-id="c9e7e-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="c9e7e-127">Ein Beispiel kann dies deutlicher machen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-127">An example may make this clearer.</span></span>  <span data-ttu-id="c9e7e-128">Sie können versuchen, ein Popup-Fenster für eine Browser Aktion zu schreiben, das `pop-up.html` Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="c9e7e-129">Drei Dinge müssen sich ändern, um diese Arbeit wie erwartet zu gestalten:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="c9e7e-130">Die `clickHandler` Definition muss in eine externe JavaScript-Datei verschoben werden \ ( `popup.js` kann ein gutes Ziel sein).</span><span class="sxs-lookup"><span data-stu-id="c9e7e-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="c9e7e-131">Die Definitionen des Inline-Ereignishandlers müssen in Bezug auf `addEventListener` und extrahiert werden `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="c9e7e-132">Wenn Sie das Programm zurzeit mithilfe von Code wie starten `<body onload="main();">` , sollten Sie es in der Weise ersetzen, indem Sie das `DOMContentLoaded` Ereignis des Dokuments oder das `load` Ereignis des Fensters abhängig von Ihren Anforderungen einbinden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="c9e7e-133">Verwenden Sie das erstere, da es in der Regel schneller auslöst.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="c9e7e-134">Der `setTimeout` Aufruf muss neu geschrieben werden, um zu verhindern, dass die Zeichenfolge `"awesome(); totallyAwesome()"` in JavaScript für die Ausführung konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="c9e7e-135">Diese Änderungen können etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="c9e7e-136">Es werden nur lokale Skript-und Objektressourcen geladen</span><span class="sxs-lookup"><span data-stu-id="c9e7e-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="c9e7e-137">Skript-und Objektressourcen können nur aus dem Erweiterungspaket geladen werden, nicht aus dem ganzen Web.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="c9e7e-138">Dadurch wird sichergestellt, dass Ihre Erweiterung nur den von Ihnen ausdrücklich genehmigten Code ausführt, wodurch verhindert wird, dass ein aktiver Netzwerk Angreifer Ihre Anforderung für eine Ressource in böswilliger Weise umleitet.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="c9e7e-139">Anstatt Code zu schreiben, der von jQuery \ (oder einer anderen Bibliothek \) abhängig ist, die von einem externen CDN geladen werden, sollten Sie die spezifische Version von jQuery in Ihrem Erweiterungspaket einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="c9e7e-140">Das heißt, statt:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-140">That is, instead of:</span></span>  

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

<span data-ttu-id="c9e7e-141">Laden Sie die Datei herunter, fügen Sie Sie in Ihr Paket ein, und schreiben Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-141">Download the file, include it in your package, and write:</span></span>  

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

## <span data-ttu-id="c9e7e-142">Entspannen der Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c9e7e-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="c9e7e-143">Inline Skript</span><span class="sxs-lookup"><span data-stu-id="c9e7e-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="c9e7e-144">Inline Skripts können durch Angabe des Base64-codierten Hashs des Quellcodes in der Richtlinie zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="c9e7e-145">Dieser Hash muss vom verwendeten Hashalgorithmus (SHA256, SHA384 oder SHA512 \) vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="c9e7e-146">Ein Beispiel finden Sie unter [Hash Verwendung für \ <Skript \ > Elemente][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-146">See [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] for an example.</span></span>  

**<span data-ttu-id="c9e7e-147">Remote Skript</span><span class="sxs-lookup"><span data-stu-id="c9e7e-147">Remote Script</span></span>**  

<span data-ttu-id="c9e7e-148">Wenn Sie einige externe JavaScript-oder Objektressourcen benötigen, können Sie die Richtlinie in begrenztem Umfang lockern, indem Sie allowlisting, um sicherzustellen, woher Skripts akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="c9e7e-149">Überprüfen Sie, ob Laufzeitressourcen, die mit erhöhten Berechtigungen einer Erweiterung geladen werden, genau die erwarteten Ressourcen sind und nicht durch einen aktiven Netzwerk Angreifer ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="c9e7e-150">Da [man-in-the-Middle-Angriffe][WikiManMiddleAttacks] sowohl trivial als auch unauffindbar über HTTP sind, werden diese Ursprünge nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="c9e7e-151">Derzeit können entwicklerlist-Ursprünge mit den folgenden Schemas zulassen: `blob` ,, `filesystem` `https` und `extension` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="c9e7e-152">Der Host-Teil des Ursprungs muss explizit für die `https` und-Schemas angegeben werden `extension` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="c9e7e-153">Generische Platzhalter wie https: `https://*` und `https://*.com` sind nicht zulässig; Platzhalter für Subdomänen wie `https://*.example.com` zulässig.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="c9e7e-154">Domänen in der [Liste der öffentlichen Suffixe][PublicSuffixList] werden auch als generische Domänen auf oberster Ebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="c9e7e-155">Um eine Ressource aus diesen Domänen zu laden, muss die Unterdomäne explizit aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="c9e7e-156">Ist beispielsweise `https://*.cloudfront.net` ungültig, kann aber `https://XXXX.cloudfront.net` `https://*.XXXX.cloudfront.net` allowlisted sein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be allowlisted.</span></span>  

<span data-ttu-id="c9e7e-157">Zur Vereinfachung der Entwicklung können Ressourcen, die über HTTP von Servern auf dem lokalen Computer geladen werden, allowlisted werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be allowlisted.</span></span>  <span data-ttu-id="c9e7e-158">Sie könnenlist-Skript-und Objektquellen an einem beliebigen Port einer der beiden `http://127.0.0.1` oder zulassen `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="c9e7e-159">Die Beschränkung für Ressourcen, die über HTTP geladen werden, gilt nur für die Ressourcen, die direkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="c9e7e-160">Sie sind nach wie vor kostenlos, um beispielsweise XMLHttpRequest-Verbindungen zu beliebigen Ursprungs zu machen, die Ihnen gefallen; die Standardrichtlinie schränkt `connect-src` oder keine der anderen CSP-Direktiven in irgendeiner Weise ein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-160">You are still free, for example, to make XMLHTTPRequest connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="c9e7e-161">Eine lockere Richtliniendefinition, mit der Skriptressourcen von example.com über HTTPS geladen werden können, sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-161">A relaxed policy definition which allows script resources to be loaded from example.com over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="c9e7e-162">Beide `script-src` und `object-src` werden durch die Richtlinie definiert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="c9e7e-163">Microsoft Edge akzeptiert keine Richtlinie, die die einzelnen Werte nicht auf \ (mindestens \) ' `self` ' beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="c9e7e-164">JavaScript ausgewertet</span><span class="sxs-lookup"><span data-stu-id="c9e7e-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="c9e7e-165">Die Richtlinie für `eval()` und verwandte Funktionen wie und `setTimeout(String)` `setInterval(String)` `new Function(String)` können durch Hinzufügen `unsafe-eval` zu Ihrer Richtlinie gelockert werden:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="c9e7e-166">Wir empfehlen jedoch dringend, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-166">However, we strongly recommend against doing this.</span></span>  <span data-ttu-id="c9e7e-167">Diese Funktionen sind berüchtigte XSS-Angriffsvektoren.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-167">These functions are notorious XSS attack vectors.</span></span>  

## <span data-ttu-id="c9e7e-168">Verschärfen der Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c9e7e-168">Tightening the default policy</span></span>  

<span data-ttu-id="c9e7e-169">Sie können diese Richtlinie selbstverständlich so anziehen, wie es Ihre Erweiterung zulässt, um die Sicherheit zu Lasten der Bequemlichkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="c9e7e-170">Um anzugeben, dass Ihre Erweiterung nur Ressourcen eines beliebigen Typs \ (Bilder usw.) aus dem zugehörigen Erweiterungspaket laden kann, ist beispielsweise eine Richtlinie von `default-src 'self'` geeignet.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <span data-ttu-id="c9e7e-171">Inhalts Skripts</span><span class="sxs-lookup"><span data-stu-id="c9e7e-171">Content Scripts</span></span>  

<span data-ttu-id="c9e7e-172">Die zu diskutierende Richtlinie gilt für die Hintergrundseiten und Ereignis Seiten der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="c9e7e-173">Die Art und Weise, wie die Inhalts Skripts auf die Inhalts Skripts der Erweiterung angewendet werden, ist komplizierter.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="c9e7e-174">Inhalts Skripts unterliegen in der Regel nicht dem CSP der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="c9e7e-175">Da Inhalts Skripts keine HTML-Datei sind, ist dies hauptsächlich darauf zu verwenden, dass Sie auch dann verwendet werden können, `eval` Wenn der CSP der Erweiterung nicht angibt `unsafe-eval` , dies aber nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="c9e7e-176">Darüber hinaus gilt der CSP der Seite nicht für Inhalts Skripts.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="c9e7e-177">Komplizierter sind `<script>` Tags, die Inhalts Skripts erstellen und in das DOM der Seite einfügen, auf der Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="c9e7e-178">Diese werden als mit Dom-injizierte Skripts weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="c9e7e-179">Dom-injizierte Skripts, die unmittelbar nach der Injektion in die Seite ausgeführt werden, werden wie erwartet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="c9e7e-180">Stellen Sie sich ein Inhalts Skript mit dem folgenden Code als einfaches Beispiel vor:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="c9e7e-181">Dieses Inhalts Skript bewirkt `alert` unmittelbar nach dem `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="c9e7e-182">Beachten Sie, dass dies unabhängig von der von einer Seite angegebenen Richtlinie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="c9e7e-183">Das Verhalten wird jedoch sowohl innerhalb des DOM-injizierten Skripts als auch bei Skripten komplizierter, die nicht unmittelbar nach der Injektion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="c9e7e-184">Stellen Sie sich vor, dass Ihre Erweiterung auf einer Seite ausgeführt wird, die einen zugeordneten CSP bereitstellt, der angibt `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="c9e7e-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="c9e7e-185">Stellen Sie sich nun vor, dass das Inhalts Skript den folgenden Code ausführt:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="c9e7e-186">Wenn ein Benutzer auf diese Schaltfläche klickt, `onclick` wird das Skript nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-186">If a user clicks on that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="c9e7e-187">Dies liegt daran, dass das Skript nicht sofort ausgeführt wurde und Code nicht interpretiert wird, bis das Click-Ereignis nicht als Teil des Inhalts Skripts betrachtet wird, daher schränkt der CSP der Seite \ (nicht der Erweiterung \) das Verhalten ein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-187">This is because the script did not immediately run and code is not interpreted until the click event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="c9e7e-188">Und da dieser CSP nicht angibt `unsafe-inline` , wird der Inline-Ereignishandler blockiert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="c9e7e-189">Die richtige Methode zum Implementieren des gewünschten Verhaltens in diesem Fall ist das Hinzufügen des `onclick` Handlers als Funktion aus dem Inhalts Skript wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="c9e7e-190">Ein anderes ähnliches Problem tritt auf, wenn das Inhalts Skript Folgendes ausführt:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="c9e7e-191">In diesem Fall wird das Skript ausgeführt, und die Benachrichtigung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="c9e7e-192">In diesem Fall gehen Sie jedoch wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="c9e7e-193">Während das anfängliche Skript ausgeführt wird, wird der Anruf an `eval` blockiert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="c9e7e-194">Das heißt, während die anfängliche Skriptlaufzeit zulässig ist, wird das Verhalten innerhalb des Skripts vom CSP der Seite reguliert.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="c9e7e-195">Je nachdem, wie Sie in ihrer Erweiterung Dom-injizierte Skripts schreiben, kann sich die Änderung des CSP der Seite auf das Verhalten der Erweiterung auswirken.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="c9e7e-196">Da Inhalts Skripts nicht vom CSP der Seite betroffen sind, ist dies ein guter Grund, um das Inhalts Skript so weit wie möglich von der Erweiterung zu versetzen, anstatt von Dom-injizierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Eine Einführung in die Inhalts Sicherheitsrichtlinie – HTML5 rockt"  
[PublicSuffixList]: https://publicsuffix.org/list "Anzeigen der Liste der öffentlichen Suffixe"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Hash Verwendung für \ <Skript \ > Elemente – Inhalts Sicherheitsrichtlinienebene 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Inhalts Sicherheitsrichtlinienebene 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Man-in-the-Middle-Angriff – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="c9e7e-202">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c9e7e-203">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="c9e7e-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c9e7e-205">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c9e7e-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
