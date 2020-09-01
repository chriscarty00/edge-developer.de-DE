---
title: Zuordnen von vorverarbeitetem Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c791a4af4446a1209d6db77ca4787fee80d45e5c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981771"
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





# <span data-ttu-id="49e84-103">Zuordnen von vorverarbeitetem Code zu Quellcode</span><span class="sxs-lookup"><span data-stu-id="49e84-103">Map preprocessed code to source code</span></span>   




<span data-ttu-id="49e84-104">Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.</span><span class="sxs-lookup"><span data-stu-id="49e84-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="49e84-105">Verwenden Sie Quell Karten, um Ihren Quellcode dem kompilierten Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="49e84-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="49e84-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="49e84-106">Summary</span></span>  

*   <span data-ttu-id="49e84-107">Verwenden Sie Quell Karten, um Quellcode minimierte-Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="49e84-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="49e84-108">Sie können dann kompilierten Code in der ursprünglichen Quelle lesen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="49e84-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="49e84-109">Verwenden Sie nur Pre-Processors, die Quell Karten erstellen können.</span><span class="sxs-lookup"><span data-stu-id="49e84-109">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="49e84-110">Überprüfen Sie, ob Ihr Webserver Quell Karten bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="49e84-110">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="49e84-111">Erste Schritte mit Präprozessoren</span><span class="sxs-lookup"><span data-stu-id="49e84-111">Get started with preprocessors</span></span>  

<span data-ttu-id="49e84-112">In diesem Artikel wird erläutert, wie Sie mit JavaScript-Quell Karten im devtools-Quellen Panel interagieren.</span><span class="sxs-lookup"><span data-stu-id="49e84-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="49e84-113">Verwenden eines unterstützten Präprozessors</span><span class="sxs-lookup"><span data-stu-id="49e84-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="49e84-114">Sie müssen ein minifier verwenden, das Quell Karten erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="49e84-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="49e84-115">Eine erweiterte Ansicht finden Sie unter [Quell Karten: Sprachen, Tools und andere Info][GitHubWikiSourceMapsLanguagesTools] -Wiki-Seite.</span><span class="sxs-lookup"><span data-stu-id="49e84-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="49e84-116">Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Quell Karten verwendet:</span><span class="sxs-lookup"><span data-stu-id="49e84-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="49e84-117">Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="49e84-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="49e84-118">Compiler \ ([Closure-Compiler][GitHubGoogleClosureCompiler], [Manuskript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="49e84-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="49e84-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="49e84-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="49e84-120">Quell Karten im devtools-Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="49e84-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="49e84-121">Quell Karten von Präprozessoren führen dazu, dass devtools Ihre Originaldateien zusätzlich zu ihren minimierte lädt.</span><span class="sxs-lookup"><span data-stu-id="49e84-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="49e84-122">Anschließend verwenden Sie die originale, um Haltepunkte und schrittweise Code zu definieren.</span><span class="sxs-lookup"><span data-stu-id="49e84-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="49e84-123">In der Zwischenzeit wird von Microsoft Edge tatsächlich der minimierte-Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49e84-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="49e84-124">Dies gibt Ihnen die Illusion, eine Entwicklungswebsite in Production zu betreiben.</span><span class="sxs-lookup"><span data-stu-id="49e84-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="49e84-125">Beim Ausführen von Quell Karten in devtools sollten Sie feststellen, dass das JavaScript nicht kompiliert wurde und Sie alle einzelnen JavaScript-Dateien anzeigen können, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="49e84-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="49e84-126">Dies verwendet die Quell Zuordnung, doch hinter den Kulissen wird der kompilierte Code tatsächlich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49e84-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="49e84-127">Alle Fehler, Protokolle und Haltepunkte werden dem dev-Code für awesome Debugging zugeordnet!</span><span class="sxs-lookup"><span data-stu-id="49e84-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="49e84-128">So erhalten Sie in der Tat die Illusion, dass Sie eine dev-Website in Production ausführen.</span><span class="sxs-lookup"><span data-stu-id="49e84-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="49e84-129">Aktivieren von Quell Karten in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="49e84-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="49e84-130">Quell Karten sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="49e84-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="49e84-131">, aber wenn Sie diese überprüfen oder aktivieren möchten, Öffnen Sie zuerst devtools, klicken Sie auf die Schaltfläche **anpassen und Steuern devtools** \ ( `...` \), und wählen Sie **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="49e84-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and select **Settings**.</span></span>  <span data-ttu-id="49e84-132">Aktivieren Sie im Bereich **Einstellungen** unter **Quellen**die **Option JavaScript-Quell Karten aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="49e84-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="49e84-133">Sie können auch die **Option "CSS-Quell Karten aktivieren" aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="49e84-133">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Quell Karten aktivieren" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   <span data-ttu-id="49e84-135">Quell Karten aktivieren</span><span class="sxs-lookup"><span data-stu-id="49e84-135">Enable Source Maps</span></span>  
:::image-end:::  

### <span data-ttu-id="49e84-136">Debuggen mit Quell Karten</span><span class="sxs-lookup"><span data-stu-id="49e84-136">Debugging with Source Maps</span></span>  

<span data-ttu-id="49e84-137">Wenn Sie Ihren Code und die Quell Karten Debuggen aktiviert haben, werden Quell Karten an zwei Stellen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="49e84-137">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="49e84-138">In der Konsole \ (der Link zur Quelle sollte die ursprüngliche Datei und nicht die generierte sein. \)</span><span class="sxs-lookup"><span data-stu-id="49e84-138">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="49e84-139">Wenn Sie Code durchlaufen \ (die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen \)</span><span class="sxs-lookup"><span data-stu-id="49e84-139">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## <span data-ttu-id="49e84-140">@sourceURL und DisplayName</span><span class="sxs-lookup"><span data-stu-id="49e84-140">@sourceURL and displayName</span></span>  

<span data-ttu-id="49e84-141">Obwohl es sich nicht um die Quell Karten Spezifikation handelt, `@sourceURL` können Sie die Entwicklung beim Arbeiten mit evals erheblich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="49e84-141">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="49e84-142">Dieser Helfer sieht der Eigenschaft sehr ähnlich `//# sourceMappingURL` und wird in den Spezifikationen des Quell Karten-V3-Codes tatsächlich erwähnt.</span><span class="sxs-lookup"><span data-stu-id="49e84-142">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="49e84-143">Indem Sie den folgenden speziellen Kommentar in Ihren Code einbeziehen, der EVALED ist, können Sie evals und Inlineskripts und-Formatvorlagen benennen, damit jeder in Ihrem devtools als logischere Namen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="49e84-143">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="49e84-144">Navigieren Sie zur folgenden Seite.</span><span class="sxs-lookup"><span data-stu-id="49e84-144">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="49e84-145">Demo</span><span class="sxs-lookup"><span data-stu-id="49e84-145">demo</span></span>][CssNinjaDemoSourceMapping]
    
<span data-ttu-id="49e84-146">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="49e84-146">Follow these steps.</span></span>  

1.  <span data-ttu-id="49e84-147">Öffnen Sie das devtools, und wechseln Sie zum **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="49e84-147">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="49e84-148">Geben Sie einen Dateinamen in das Eingabefeld " **Name Your Code:** " ein.</span><span class="sxs-lookup"><span data-stu-id="49e84-148">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="49e84-149">Klicken Sie auf die Schaltfläche **Kompilieren** .</span><span class="sxs-lookup"><span data-stu-id="49e84-149">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="49e84-150">Eine Benachrichtigung mit der ausgewerteten Summe aus der CoffeeScript-Quelle wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49e84-150">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="49e84-151">Wenn Sie die Untergruppe " **Quellen** " erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="49e84-151">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="49e84-152">Wenn Sie zum Anzeigen dieser Datei doppelklicken, enthält Sie das kompilierte JavaScript für die ursprüngliche Quelle.</span><span class="sxs-lookup"><span data-stu-id="49e84-152">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="49e84-153">In der letzten Zeile ist jedoch ein Kommentar, `// @sourceURL` der die ursprüngliche Quelldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="49e84-153">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="49e84-154">Dies kann Ihnen beim Debuggen beim Arbeiten mit sprach Abstraktionen helfen.</span><span class="sxs-lookup"><span data-stu-id="49e84-154">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Arbeiten mit sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="49e84-156">Arbeiten mit sourceURL</span><span class="sxs-lookup"><span data-stu-id="49e84-156">Working with sourceURL</span></span>  
:::image-end:::  

<!--  
## Feedback   


-->  

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
> <span data-ttu-id="49e84-166">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49e84-166">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49e84-167">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate, Google: Tools, Performance, Animation und UX) erstellt.</span><span class="sxs-lookup"><span data-stu-id="49e84-167">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="49e84-169">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49e84-169">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
