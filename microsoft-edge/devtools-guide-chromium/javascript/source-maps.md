---
description: Halten Sie ihren clientseitigen Code auch nach dem Kombinieren, Minimieren oder Kompilieren lesbar und debuggbar.
title: Zuordnung von vorverarbeiteten Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3240e437a917dd7074a0584b91dcc6c34576ca24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564049"
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
# <a name="map-preprocessed-code-to-source-code"></a><span data-ttu-id="d706a-104">Zuordnung von vorverarbeiteten Code zu Quellcode</span><span class="sxs-lookup"><span data-stu-id="d706a-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="d706a-105">Halten Sie ihren clientseitigen Code auch nach dem Kombinieren, Minimieren oder Kompilieren lesbar und debuggbar.</span><span class="sxs-lookup"><span data-stu-id="d706a-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="d706a-106">Verwenden Sie Quellzuordnungen, um Den Quellcode dem kompilierten Code zu zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="d706a-106">Use source maps to map your source code to your compiled code.</span></span>  

### <a name="summary"></a><span data-ttu-id="d706a-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d706a-107">Summary</span></span>  

*   <span data-ttu-id="d706a-108">Verwenden Sie source Karten, um dem Quellcode minifizierten Code zu zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="d706a-108">Use Source Maps to map minified code to source code.</span></span>  <span data-ttu-id="d706a-109">Anschließend können Sie kompilierten Code in der ursprünglichen Quelle lesen und debuggen.</span><span class="sxs-lookup"><span data-stu-id="d706a-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="d706a-110">Verwenden Sie nur Vorverarbeiter, die Quellprozessoren Karten.</span><span class="sxs-lookup"><span data-stu-id="d706a-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="d706a-111">Stellen Sie sicher, dass Ihr Webserver Quellserver Karten.</span><span class="sxs-lookup"><span data-stu-id="d706a-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a><span data-ttu-id="d706a-112">Erste Schritte mit Präprozessoren</span><span class="sxs-lookup"><span data-stu-id="d706a-112">Get started with preprocessors</span></span>  

<span data-ttu-id="d706a-113">In diesem Artikel wird erläutert, wie Sie mit JavaScript Source Karten im Tool DevTools Sources interagieren.</span><span class="sxs-lookup"><span data-stu-id="d706a-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources tool.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a><span data-ttu-id="d706a-114">Verwenden eines unterstützten Präprozessors</span><span class="sxs-lookup"><span data-stu-id="d706a-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="d706a-115">Verwenden Sie ein Minifier, mit dem Quellzuordnungen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="d706a-115">Use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="d706a-116">Navigieren Sie für eine erweiterte Ansicht zu [Quellzuordnungen: Sprachen, Tools und andere Info-Wiki-Seite.][GitHubWikiSourceMapsLanguagesTools]</span><span class="sxs-lookup"><span data-stu-id="d706a-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="d706a-117">Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Source-Karten:</span><span class="sxs-lookup"><span data-stu-id="d706a-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="d706a-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="d706a-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="d706a-119">Compiler \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="d706a-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="d706a-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="d706a-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <a name="source-maps-in-devtools-sources-tool"></a><span data-ttu-id="d706a-121">Source Karten in DevTools Sources tool</span><span class="sxs-lookup"><span data-stu-id="d706a-121">Source Maps in DevTools Sources tool</span></span>  

<span data-ttu-id="d706a-122">Quelldateien Karten von Präprozessoren führen dazu, dass DevTools ihre ursprünglichen Dateien zusätzlich zu den minifizierten Dateien geladen.</span><span class="sxs-lookup"><span data-stu-id="d706a-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="d706a-123">Anschließend verwenden Sie die Originale, um Haltepunkte zu setzen und Code zu durchbrechen.</span><span class="sxs-lookup"><span data-stu-id="d706a-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="d706a-124">In der zwischenzeit Microsoft Edge tatsächlich ihren minifizierten Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d706a-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  <span data-ttu-id="d706a-125">Die Ausführung des Codes gibt Ihnen die Illusion, eine Entwicklungswebsite in der Produktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d706a-125">The running of the code gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="d706a-126">Wenn Sie source Karten in DevTools ausführen, sollten Sie feststellen, dass javaScript nicht kompiliert wird und alle einzelnen JavaScript-Dateien angezeigt werden, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="d706a-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and all of the individual JavaScript files it references are displayed.</span></span>  <span data-ttu-id="d706a-127">Source Karten in DevTools verwendet die Quellzuordnung, aber die zugrunde liegende Funktionalität führt tatsächlich den kompilierten Code aus.</span><span class="sxs-lookup"><span data-stu-id="d706a-127">Source Maps in DevTools is using source mapping, but the underlying functionality actually runs the compiled code.</span></span>  <span data-ttu-id="d706a-128">Alle Fehler, Protokolle und Haltepunkte werden dem Entwicklungscode für ein großartiges Debuggen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d706a-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging.</span></span>  <span data-ttu-id="d706a-129">Es gibt Ihnen also die Illusion, dass Sie eine Entwicklungswebsite in der Produktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="d706a-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <a name="enable-source-maps-in-settings"></a><span data-ttu-id="d706a-130">Aktivieren von Karten in Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d706a-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="d706a-131">Quelldateien Karten standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="d706a-131">Source Maps are enabled by default</span></span><!-- \(as of Microsoft Edge 39\)--><span data-ttu-id="d706a-132">, wenn Sie sie jedoch überprüfen oder aktivieren möchten; Öffnen Sie zunächst DevTools, wählen **Sie Anpassen und Steuern von DevTools** \( `...` \) > **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d706a-132">, but if you want to double-check or enable them; first open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="d706a-133">Aktivieren Sie **im Bereich** Einstellungen unter **Quellen**die Option **JavaScript Source Karten**.</span><span class="sxs-lookup"><span data-stu-id="d706a-133">On the **Preferences** pane, under **Sources**, turn on **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="d706a-134">Sie können auch die Option **CSS-Quelldatei aktivieren Karten.**</span><span class="sxs-lookup"><span data-stu-id="d706a-134">You may also turn on the **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Aktivieren von Karten" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="d706a-136">Aktivieren von JavaScript Source Karten</span><span class="sxs-lookup"><span data-stu-id="d706a-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a><span data-ttu-id="d706a-137">Debuggen mit Karten</span><span class="sxs-lookup"><span data-stu-id="d706a-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="d706a-138">Beim Debuggen des Codes und Karten Source Karten source Karten an zwei Stellen:</span><span class="sxs-lookup"><span data-stu-id="d706a-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="d706a-139">In der Konsole \(Der Link zur Quelle sollte die ursprüngliche Datei sein, nicht die generierte\)</span><span class="sxs-lookup"><span data-stu-id="d706a-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="d706a-140">Beim Schrittweisen durch Code \(Die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen\)</span><span class="sxs-lookup"><span data-stu-id="d706a-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a><span data-ttu-id="d706a-141">@sourceURL und displayName</span><span class="sxs-lookup"><span data-stu-id="d706a-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="d706a-142">Obwohl sie nicht Teil der Quellzuordnungsspezifikation sind, können Sie die Entwicklung bei der Arbeit mit `@sourceURL` Evals erheblich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="d706a-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="d706a-143">Die Hilfshilfe wird ähnlich wie die Eigenschaft angezeigt und `//# sourceMappingURL` in den Source Map V3-Spezifikationen erwähnt.</span><span class="sxs-lookup"><span data-stu-id="d706a-143">The helper is displayed similar to the `//# sourceMappingURL` property and is mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="d706a-144">Durch das Hinzufügen des folgenden speziellen Kommentars in Ihren Code, der ausweicht, können Sie Evals und Inlineskripts und Formatvorlagen benennen, sodass jede als logischere Namen in Ihren DevTools angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d706a-144">By including the following special comment in your code, which is evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="d706a-145">Navigieren Sie zur folgenden Seite.</span><span class="sxs-lookup"><span data-stu-id="d706a-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="d706a-146">Demo</span><span class="sxs-lookup"><span data-stu-id="d706a-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="d706a-147">Führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d706a-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="d706a-148">Öffnen Sie DevTools, und navigieren Sie zum **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="d706a-148">Open DevTools and navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="d706a-149">Geben Sie einen Dateinamen in das Eingabefeld **Name your code:** ein.</span><span class="sxs-lookup"><span data-stu-id="d706a-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="d706a-150">Wählen Sie **die Kompilierungsschaltfläche** aus.</span><span class="sxs-lookup"><span data-stu-id="d706a-150">Choose the **compile** button.</span></span>  
1.  <span data-ttu-id="d706a-151">Es wird eine Warnung mit der ausgewerteten Summe aus der CoffeeScript-Quelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d706a-151">An alert appears, showing the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="d706a-152">Wenn Sie den Unterbereich **Quellen** erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d706a-152">If you expand the **Sources** sub-panel you now display a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="d706a-153">Wenn Sie doppelklicken, um diese Datei zu sehen, enthält sie das kompilierte JavaScript für die ursprüngliche Quelle.</span><span class="sxs-lookup"><span data-stu-id="d706a-153">If you double-click to view this file, it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="d706a-154">In der letzten Zeile befindet sich jedoch ein Kommentar, der `// @sourceURL` die ursprüngliche Quelldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="d706a-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="d706a-155">Dies kann Ihnen beim Debuggen beim Arbeiten mit Sprachabstraktionen helfen.</span><span class="sxs-lookup"><span data-stu-id="d706a-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Arbeiten mit sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="d706a-157">Arbeiten mit</span><span class="sxs-lookup"><span data-stu-id="d706a-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d706a-158">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d706a-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel ist ein #A0"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Ein einfaches Beispiel für die Benennung von #A0"  

[DartMain]: https://www.dartlang.org "Dart-Programmiersprache"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/closure-compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Quellkarten: Sprachen, Tools und andere | GitHub Wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Erste Schritte – google/traceur-compiler | GitHub Wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="d706a-168">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d706a-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d706a-169">Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) befindet sich hier und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation und UX\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d706a-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d706a-171">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d706a-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
