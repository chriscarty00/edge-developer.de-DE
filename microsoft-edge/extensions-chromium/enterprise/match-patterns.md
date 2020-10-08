---
description: Unternehmensrichtlinien Dokumentation für Edge (Chrom)-Erweiterungen.
title: Übereinstimmungsmuster
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 59427769a010ca774833a809d3025e7594634202
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015660"
---
# <span data-ttu-id="ce59c-104">Übereinstimmungsmuster</span><span class="sxs-lookup"><span data-stu-id="ce59c-104">Match Patterns</span></span>

<span data-ttu-id="ce59c-105">Die Host Berechtigungen und die Inhalts Skript Übereinstimmung basieren auf einer Gruppe von URLs, die durch Übereinstimmungsmuster definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce59c-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="ce59c-106">Ein Übereinstimmungsmuster ist im Grunde eine URL, die mit einem zulässigen Schema beginnt (,,, `http` `https` oder, `file` `ftp` und das "Zeichen enthalten kann `*` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="ce59c-107">Das besondere Muster `<all_urls>` entspricht einer beliebigen URL, die mit einem zulässigen Schema beginnt.</span><span class="sxs-lookup"><span data-stu-id="ce59c-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="ce59c-108">Jedes Übereinstimmungsmuster besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="ce59c-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="ce59c-109">_Schema_ – beispielsweise `http` oder `file` oder</span><span class="sxs-lookup"><span data-stu-id="ce59c-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="ce59c-110">Der Zugriff auf `file` URLs erfolgt nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="ce59c-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="ce59c-111">Der Benutzer muss die Seite "erweiterungenverwaltung" besuchen und sich `file` für jede Erweiterung, die ihn anfordert, für den Zugriff entscheiden.</span><span class="sxs-lookup"><span data-stu-id="ce59c-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="ce59c-112">– beispielsweise `www.google.com` oder `*.google.com` oder `*` ; Wenn es sich bei dem Schema um eine Datei handelt, gibt es kein Host-Part.</span><span class="sxs-lookup"><span data-stu-id="ce59c-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="ce59c-113">– beispielsweise, `/*` , `/foo*` oder `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="ce59c-114">Der Pfad muss in einer Host Berechtigung vorhanden sein, wird aber immer als behandelt `/*` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="ce59c-115">Die grundlegende Syntax:</span><span class="sxs-lookup"><span data-stu-id="ce59c-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="ce59c-116">Die Bedeutung von `*` hängt davon ab, ob Sie im Schema-, Host-oder Path-Webpart enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ce59c-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="ce59c-117">Wenn es sich um ein Schema handelt `*` , entspricht es entweder `http` oder `https` , und nicht `file` , oder `ftp` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="ce59c-118">Wenn der Host gerade ist `*` , ist er mit jedem Host identisch.</span><span class="sxs-lookup"><span data-stu-id="ce59c-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="ce59c-119">Wenn es sich um einen Host handelt `*.hostname` , entspricht er dem angegebenen Host oder einer der Unterdomänen.</span><span class="sxs-lookup"><span data-stu-id="ce59c-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="ce59c-120">Im Abschnitt Path werden jeweils `*` 0 oder mehr Zeichen abgleichen.</span><span class="sxs-lookup"><span data-stu-id="ce59c-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="ce59c-121">In der folgenden Tabelle sind einige gültige Muster dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce59c-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="ce59c-122">Muster</span><span class="sxs-lookup"><span data-stu-id="ce59c-122">Pattern</span></span> | <span data-ttu-id="ce59c-123">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="ce59c-123">What it does</span></span> | <span data-ttu-id="ce59c-124">Beispiele für übereinstimmende URLs</span><span class="sxs-lookup"><span data-stu-id="ce59c-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="ce59c-125">Entspricht einer URL, die das http-Schema verwendet</span><span class="sxs-lookup"><span data-stu-id="ce59c-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="ce59c-126">Entspricht einer URL, die das http-Schema verwendet, auf einem beliebigen Host, solange der Pfad beginnt mit</span><span class="sxs-lookup"><span data-stu-id="ce59c-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="ce59c-127">Entspricht einer beliebigen URL, die das HTTPS-Schema verwendet, befindet sich auf einem `google.com` Host \ (wie `www.google.com` , `docs.google.com` oder `google.com` \), solange der Pfad mit beginnt `/foo` und endet mit</span><span class="sxs-lookup"><span data-stu-id="ce59c-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="ce59c-128">Entspricht der angegebenen URL</span><span class="sxs-lookup"><span data-stu-id="ce59c-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="ce59c-129">Entspricht einer beliebigen lokalen Datei, deren Pfad mit beginnt</span><span class="sxs-lookup"><span data-stu-id="ce59c-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="ce59c-130">Entspricht einer URL, die das `http` Schema verwendet und sich auf dem Host befindet</span><span class="sxs-lookup"><span data-stu-id="ce59c-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="ce59c-131">Entspricht einer URL, die mit "oder" beginnt `http://mail.google.com` `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="ce59c-132">Entspricht einer URL, die ein zulässiges Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce59c-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="ce59c-133">\ (Die Liste der zulässigen Schemas finden Sie am Anfang dieses Abschnitts. \)</span><span class="sxs-lookup"><span data-stu-id="ce59c-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="ce59c-134">Nachfolgend finden Sie einige Beispiele für `_invalid_` Musterübereinstimmungen:</span><span class="sxs-lookup"><span data-stu-id="ce59c-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="ce59c-135">Fehlerhaftes Muster</span><span class="sxs-lookup"><span data-stu-id="ce59c-135">Bad pattern</span></span> | <span data-ttu-id="ce59c-136">Warum es schlecht ist</span><span class="sxs-lookup"><span data-stu-id="ce59c-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="ce59c-137">Nein</span><span class="sxs-lookup"><span data-stu-id="ce59c-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="ce59c-138">' ' `*` im Host kann nur mit einem ' `.` ' oder ' ' verfolgt werden `/` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="ce59c-139">Wenn " `*` " in der ist `_host_` , muss es das erste Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="ce59c-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="ce59c-140">Fehlendes `_scheme_` Trennzeichen \ (' `/` ' sollte "sein" `//` \)</span><span class="sxs-lookup"><span data-stu-id="ce59c-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="ce59c-141">Ungültig</span><span class="sxs-lookup"><span data-stu-id="ce59c-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="ce59c-142">Einige Schemas werden in allen Kontexten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce59c-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="ce59c-143">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce59c-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ce59c-144">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/match_patterns/).</span><span class="sxs-lookup"><span data-stu-id="ce59c-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns/).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="ce59c-146">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ce59c-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
