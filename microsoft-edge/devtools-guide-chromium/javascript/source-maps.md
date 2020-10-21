---
description: Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.
title: Zuordnen von vorverarbeitetem Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c16f59658217ab9dfb905bd814f96af21f95130d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124681"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="5088d-104">Zuordnen von vorverarbeitetem Code zu Quellcode</span><span class="sxs-lookup"><span data-stu-id="5088d-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="5088d-105">Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.</span><span class="sxs-lookup"><span data-stu-id="5088d-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="5088d-106">Verwenden Sie Quell Karten, um Ihren Quellcode dem kompilierten Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5088d-106">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="5088d-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5088d-107">Summary</span></span>  

*   <span data-ttu-id="5088d-108">Verwenden Sie Quell Karten, um Quellcode minimierte-Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5088d-108">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="5088d-109">Sie können dann kompilierten Code in der ursprünglichen Quelle lesen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="5088d-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="5088d-110">Verwenden Sie nur Pre-Processors, die Quell Karten erstellen können.</span><span class="sxs-lookup"><span data-stu-id="5088d-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="5088d-111">Überprüfen Sie, ob Ihr Webserver Quell Karten bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5088d-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="5088d-112">Erste Schritte mit Präprozessoren</span><span class="sxs-lookup"><span data-stu-id="5088d-112">Get started with preprocessors</span></span>  

<span data-ttu-id="5088d-113">In diesem Artikel wird erläutert, wie Sie mit JavaScript-Quell Karten im devtools-Quellen Panel interagieren.</span><span class="sxs-lookup"><span data-stu-id="5088d-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="5088d-114">Verwenden eines unterstützten Präprozessors</span><span class="sxs-lookup"><span data-stu-id="5088d-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="5088d-115">Sie müssen ein minifier verwenden, das Quell Karten erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5088d-115">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="5088d-116">Navigieren Sie für eine erweiterte Ansicht zu [Quell Karten: Sprachen, Tools und andere Info][GitHubWikiSourceMapsLanguagesTools] -Wiki-Seite.</span><span class="sxs-lookup"><span data-stu-id="5088d-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="5088d-117">Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Quell Karten verwendet:</span><span class="sxs-lookup"><span data-stu-id="5088d-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="5088d-118">Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="5088d-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="5088d-119">Compiler \ ([Closure-Compiler][GitHubGoogleClosureCompiler], [Manuskript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="5088d-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="5088d-120">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="5088d-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="5088d-121">Quell Karten im devtools-Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="5088d-121">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="5088d-122">Quell Karten von Präprozessoren führen dazu, dass devtools Ihre Originaldateien zusätzlich zu ihren minimierte lädt.</span><span class="sxs-lookup"><span data-stu-id="5088d-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="5088d-123">Anschließend verwenden Sie die originale, um Haltepunkte und schrittweise Code zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5088d-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="5088d-124">In der Zwischenzeit wird von Microsoft Edge tatsächlich der minimierte-Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5088d-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="5088d-125">Dies gibt Ihnen die Illusion, eine Entwicklungswebsite in Production zu betreiben.</span><span class="sxs-lookup"><span data-stu-id="5088d-125">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="5088d-126">Beim Ausführen von Quell Karten in devtools sollten Sie feststellen, dass das JavaScript nicht kompiliert wurde und Sie alle einzelnen JavaScript-Dateien anzeigen können, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="5088d-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="5088d-127">Dies verwendet die Quell Zuordnung, doch hinter den Kulissen wird der kompilierte Code tatsächlich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5088d-127">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="5088d-128">Alle Fehler, Protokolle und Haltepunkte werden dem dev-Code für awesome Debugging zugeordnet!</span><span class="sxs-lookup"><span data-stu-id="5088d-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="5088d-129">So erhalten Sie in der Tat die Illusion, dass Sie eine dev-Website in Production ausführen.</span><span class="sxs-lookup"><span data-stu-id="5088d-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="5088d-130">Aktivieren von Quell Karten in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="5088d-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="5088d-131">Quell Karten sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5088d-131">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="5088d-132">, aber wenn Sie diese überprüfen oder aktivieren möchten, Öffnen Sie zuerst devtools, klicken Sie auf die Schaltfläche **anpassen und Steuern devtools** \ ( `...` \), und wählen Sie **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="5088d-132">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and choose **Settings**.</span></span>  <span data-ttu-id="5088d-133">Aktivieren Sie im Bereich **Einstellungen** unter **Quellen**die **Option JavaScript-Quell Karten aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="5088d-133">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="5088d-134">Sie können auch die **Option "CSS-Quell Karten aktivieren" aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="5088d-134">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Quell Karten aktivieren" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="5088d-136">Aktivieren von JavaScript-Quell Karten</span><span class="sxs-lookup"><span data-stu-id="5088d-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <span data-ttu-id="5088d-137">Debuggen mit Quell Karten</span><span class="sxs-lookup"><span data-stu-id="5088d-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="5088d-138">Wenn Sie Ihren Code und die Quell Karten Debuggen aktiviert haben, werden Quell Karten an zwei Stellen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5088d-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="5088d-139">In der Konsole \ (der Link zur Quelle sollte die ursprüngliche Datei und nicht die generierte sein. \)</span><span class="sxs-lookup"><span data-stu-id="5088d-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="5088d-140">Wenn Sie Code durchlaufen \ (die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen \)</span><span class="sxs-lookup"><span data-stu-id="5088d-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <span data-ttu-id="5088d-141">@sourceURL und DisplayName</span><span class="sxs-lookup"><span data-stu-id="5088d-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="5088d-142">Obwohl es sich nicht um die Quell Karten Spezifikation handelt, `@sourceURL` können Sie die Entwicklung beim Arbeiten mit evals erheblich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5088d-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="5088d-143">Dieser Helfer sieht der Eigenschaft sehr ähnlich `//# sourceMappingURL` und wird in den Spezifikationen des Quell Karten-V3-Codes tatsächlich erwähnt.</span><span class="sxs-lookup"><span data-stu-id="5088d-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="5088d-144">Indem Sie den folgenden speziellen Kommentar in Ihren Code einbeziehen, der EVALED ist, können Sie evals und Inlineskripts und-Formatvorlagen benennen, damit jeder in Ihrem devtools als logischere Namen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5088d-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="5088d-145">Navigieren Sie zur folgenden Seite.</span><span class="sxs-lookup"><span data-stu-id="5088d-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="5088d-146">Demo</span><span class="sxs-lookup"><span data-stu-id="5088d-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="5088d-147">Führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="5088d-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="5088d-148">Öffnen Sie das devtools, und wechseln Sie zum **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="5088d-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="5088d-149">Geben Sie einen Dateinamen in das Eingabefeld " **Name Your Code:** " ein.</span><span class="sxs-lookup"><span data-stu-id="5088d-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="5088d-150">Klicken Sie auf die Schaltfläche **Kompilieren** .</span><span class="sxs-lookup"><span data-stu-id="5088d-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="5088d-151">Eine Benachrichtigung mit der ausgewerteten Summe aus der CoffeeScript-Quelle wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5088d-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="5088d-152">Wenn Sie die Untergruppe " **Quellen** " erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="5088d-152">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="5088d-153">Wenn Sie zum Anzeigen dieser Datei doppelklicken, enthält Sie das kompilierte JavaScript für die ursprüngliche Quelle.</span><span class="sxs-lookup"><span data-stu-id="5088d-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="5088d-154">In der letzten Zeile ist jedoch ein Kommentar, `// @sourceURL` der die ursprüngliche Quelldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="5088d-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="5088d-155">Dies kann Ihnen beim Debuggen beim Arbeiten mit sprach Abstraktionen helfen.</span><span class="sxs-lookup"><span data-stu-id="5088d-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Quell Karten aktivieren" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="5088d-157">Arbeiten mit</span><span class="sxs-lookup"><span data-stu-id="5088d-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <span data-ttu-id="5088d-158">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="5088d-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel ist ein JavaScript-Compiler"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Ein einfaches Beispiel für//# sourceURL eval Naming"  

[DartMain]: https://www.dartlang.org "Dart-Programmiersprache"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/Closure-Compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Quell Karten: Sprachen, Tools und andere Informationen | GitHub-wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Erste Schritte-Google/Traceur-Compiler | GitHub-wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="5088d-168">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5088d-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5088d-169">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate, Google: Tools, Performance, Animation und UX) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5088d-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="5088d-171">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5088d-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
