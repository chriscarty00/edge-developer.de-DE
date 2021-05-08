---
description: Enterprise Richtliniendokumentation für Edgeerweiterungen (Chromium).
title: Übereinstimmungsmuster
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: fcb87b62cac063c7663f575fa3d992b187408c28
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461248"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="match-patterns"></a><span data-ttu-id="c24e0-104">Übereinstimmungsmuster</span><span class="sxs-lookup"><span data-stu-id="c24e0-104">Match Patterns</span></span>

<span data-ttu-id="c24e0-105">Hostberechtigungen und Inhaltsskriptabgleich basieren auf einer Reihe von URLs, die durch Übereinstimmungsmuster definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c24e0-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="c24e0-106">Ein Übereinstimmungsmuster ist im Wesentlichen eine URL, die mit einem zulässigen Schema beginnt ( , , , oder , und die `http` ' ' Zeichen enthalten `https` `file` `ftp` `*` kann.</span><span class="sxs-lookup"><span data-stu-id="c24e0-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="c24e0-107">Das spezielle Muster `<all_urls>` entspricht jeder URL, die mit einem zulässigen Schema beginnt.</span><span class="sxs-lookup"><span data-stu-id="c24e0-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="c24e0-108">Jedes Übereinstimmungsmuster hat 3 Teile:</span><span class="sxs-lookup"><span data-stu-id="c24e0-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="c24e0-109">_schema_ – z. `http` B. `file` oder oder</span><span class="sxs-lookup"><span data-stu-id="c24e0-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="c24e0-110">Der Zugriff `file` auf URLs erfolgt nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="c24e0-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="c24e0-111">Der Benutzer muss die Verwaltungsseite Erweiterungen besuchen und sich für jede Erweiterung, die sie anfordert, `file` für den Zugriff entscheiden.</span><span class="sxs-lookup"><span data-stu-id="c24e0-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="c24e0-112">– z. `www.google.com` B. `*.google.com` oder ; wenn das Schema `*` datei ist, gibt es keinen Hostteil.</span><span class="sxs-lookup"><span data-stu-id="c24e0-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="c24e0-113">– z. B. `/*` , `/foo*` oder `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="c24e0-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="c24e0-114">Der Pfad muss in einer Hostberechtigung vorhanden sein, wird jedoch immer als `/*` behandelt.</span><span class="sxs-lookup"><span data-stu-id="c24e0-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="c24e0-115">Die grundlegende Syntax:</span><span class="sxs-lookup"><span data-stu-id="c24e0-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="c24e0-116">Die Bedeutung von `*` hängt davon ab, ob sie sich im Schema-, Host- oder Pfadteil befindet.</span><span class="sxs-lookup"><span data-stu-id="c24e0-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="c24e0-117">Wenn das Schema `*` ist , entspricht es entweder oder , und nicht , oder `http` `https` `file` `ftp` .</span><span class="sxs-lookup"><span data-stu-id="c24e0-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="c24e0-118">Wenn der Host nur `*` ist, entspricht er einem beliebigen Host.</span><span class="sxs-lookup"><span data-stu-id="c24e0-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="c24e0-119">Wenn der Host ist, entspricht er dem angegebenen Host oder einer `*.hostname` der Unterdomänen.</span><span class="sxs-lookup"><span data-stu-id="c24e0-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="c24e0-120">Im Abschnitt Pfad entspricht jede `*` 0 oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c24e0-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="c24e0-121">In der folgenden Tabelle sind einige gültige Muster aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c24e0-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="c24e0-122">Muster</span><span class="sxs-lookup"><span data-stu-id="c24e0-122">Pattern</span></span> | <span data-ttu-id="c24e0-123">Was dies bedeutet</span><span class="sxs-lookup"><span data-stu-id="c24e0-123">What it does</span></span> | <span data-ttu-id="c24e0-124">Beispiele für übereinstimmende URLs</span><span class="sxs-lookup"><span data-stu-id="c24e0-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="c24e0-125">Entspricht einer beliebigen URL, die das http-Schema verwendet</span><span class="sxs-lookup"><span data-stu-id="c24e0-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="c24e0-126">Entspricht jeder URL, die das http-Schema auf einem beliebigen Host verwendet, solange der Pfad mit beginnt</span><span class="sxs-lookup"><span data-stu-id="c24e0-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="c24e0-127">Entspricht jeder URL, die das https-Schema verwendet, befindet sich auf einem Host \(z. B. `google.com` `www.google.com` , oder `docs.google.com` `google.com` \), solange der Pfad mit beginnt und `/foo` mit endet</span><span class="sxs-lookup"><span data-stu-id="c24e0-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="c24e0-128">Entspricht der angegebenen URL</span><span class="sxs-lookup"><span data-stu-id="c24e0-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="c24e0-129">Entspricht einer lokalen Datei, deren Pfad mit beginnt</span><span class="sxs-lookup"><span data-stu-id="c24e0-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="c24e0-130">Entspricht jeder URL, die das `http` Schema verwendet und sich auf dem Host befindet</span><span class="sxs-lookup"><span data-stu-id="c24e0-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="c24e0-131">Entspricht jeder URL, die mit oder `http://mail.google.com` `https://mail.google.com` beginnt.</span><span class="sxs-lookup"><span data-stu-id="c24e0-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="c24e0-132">Entspricht jeder URL, die ein zulässiges Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="c24e0-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="c24e0-133">\(Am Anfang dieses Abschnitts finden Sie eine Liste der zulässigen Schemas.\)</span><span class="sxs-lookup"><span data-stu-id="c24e0-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="c24e0-134">Im Folgenden finden Sie einige Beispiele für `_invalid_` Muster übereinstimmungen:</span><span class="sxs-lookup"><span data-stu-id="c24e0-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="c24e0-135">Ungültiges Muster</span><span class="sxs-lookup"><span data-stu-id="c24e0-135">Bad pattern</span></span> | <span data-ttu-id="c24e0-136">Warum es schlecht ist</span><span class="sxs-lookup"><span data-stu-id="c24e0-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="c24e0-137">Nein</span><span class="sxs-lookup"><span data-stu-id="c24e0-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="c24e0-138">' ' im Host kann nur von einem `*` ' ' oder ' ' gefolgt `.` `/` werden</span><span class="sxs-lookup"><span data-stu-id="c24e0-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="c24e0-139">Wenn ' `*` ' in `_host_` ist, muss es das erste Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="c24e0-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="c24e0-140">Fehlendes `_scheme_` Trennzeichen \(' `/` ' sollte " `//` "\) sein.</span><span class="sxs-lookup"><span data-stu-id="c24e0-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="c24e0-141">Ungültig</span><span class="sxs-lookup"><span data-stu-id="c24e0-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="c24e0-142">Einige Schemas werden nicht in allen Kontexten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c24e0-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="c24e0-143">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c24e0-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c24e0-144">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/match_patterns).</span><span class="sxs-lookup"><span data-stu-id="c24e0-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c24e0-146">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c24e0-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
