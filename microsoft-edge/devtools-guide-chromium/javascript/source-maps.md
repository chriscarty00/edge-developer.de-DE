---
title: Zuordnen von vorverarbeitetem Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: b48c67584b3f3253ada99e32c5dabfdccb2fa4de
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581796"
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





# <span data-ttu-id="b5da7-103">Zuordnen von vorverarbeitetem Code zu Quellcode</span><span class="sxs-lookup"><span data-stu-id="b5da7-103">Map Preprocessed Code to Source Code</span></span>   




<span data-ttu-id="b5da7-104">Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.</span><span class="sxs-lookup"><span data-stu-id="b5da7-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="b5da7-105">Verwenden Sie Quell Karten, um Ihren Quellcode dem kompilierten Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="b5da7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b5da7-106">Summary</span></span>  

*   <span data-ttu-id="b5da7-107">Verwenden Sie Quell Karten, um Quellcode minimierte-Code zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="b5da7-108">Sie können dann kompilierten Code in der ursprünglichen Quelle lesen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="b5da7-109">Verwenden Sie nur Präprozessoren, die Quell Karten erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b5da7-109">Only use preprocessors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="b5da7-110">Überprüfen Sie, ob Ihr Webserver Quell Karten bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b5da7-110">Verify that your web server is able to serve Source Maps.</span></span>  

<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="b5da7-111">Erste Schritte mit Präprozessoren</span><span class="sxs-lookup"><span data-stu-id="b5da7-111">Get started with preprocessors</span></span>  

<span data-ttu-id="b5da7-112">In diesem Artikel wird erläutert, wie Sie mit JavaScript-Quell Karten im devtools-Quellen Panel interagieren.</span><span class="sxs-lookup"><span data-stu-id="b5da7-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="b5da7-113">Verwenden eines unterstützten Präprozessors</span><span class="sxs-lookup"><span data-stu-id="b5da7-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="b5da7-114">Sie müssen ein minifier verwenden, das Quell Karten erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b5da7-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="b5da7-115">Eine erweiterte Ansicht finden Sie unter [Quell Karten: Sprachen, Tools und andere Info][GitHubWikiSourceMapsLanguagesTools] -Wiki-Seite.</span><span class="sxs-lookup"><span data-stu-id="b5da7-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="b5da7-116">Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Quell Karten verwendet:</span><span class="sxs-lookup"><span data-stu-id="b5da7-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="b5da7-117">Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="b5da7-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="b5da7-118">Compiler \ ([Closure-Compiler][GitHubGoogleClosureCompiler], [Manuskript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="b5da7-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="b5da7-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="b5da7-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  

## <span data-ttu-id="b5da7-120">Quell Karten im devtools-Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="b5da7-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="b5da7-121">Quell Karten von Präprozessoren führen dazu, dass devtools Ihre Originaldateien zusätzlich zu ihren minimierte lädt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="b5da7-122">Anschließend verwenden Sie die originale, um Haltepunkte und schrittweise Code zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b5da7-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="b5da7-123">In der Zwischenzeit wird von Microsoft Edge tatsächlich der minimierte-Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="b5da7-124">Dies gibt Ihnen die Illusion, eine Entwicklungswebsite in Production zu betreiben.</span><span class="sxs-lookup"><span data-stu-id="b5da7-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="b5da7-125">Beim Ausführen von Quell Karten in devtools sollten Sie feststellen, dass das JavaScript nicht kompiliert wurde und Sie alle einzelnen JavaScript-Dateien anzeigen können, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="b5da7-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="b5da7-126">Dies verwendet die Quell Zuordnung, doch hinter den Kulissen wird der kompilierte Code tatsächlich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="b5da7-127">Alle Fehler, Protokolle und Haltepunkte werden dem dev-Code für awesome Debugging zugeordnet!</span><span class="sxs-lookup"><span data-stu-id="b5da7-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="b5da7-128">So erhalten Sie in der Tat die Illusion, dass Sie eine dev-Website in Production ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="b5da7-129">Aktivieren von Quell Karten in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b5da7-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="b5da7-130">Quell Karten sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b5da7-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="b5da7-131">, aber wenn Sie diese überprüfen oder aktivieren möchten, Öffnen Sie zuerst devtools, klicken Sie auf die Schaltfläche **anpassen und Steuern devtools** `...` , und wählen Sie **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="b5da7-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** `...` button, and select **Settings**.</span></span>  <span data-ttu-id="b5da7-132">Aktivieren Sie im Bereich **Einstellungen** unter **Quellen**die **Option JavaScript-Quell Karten aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b5da7-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="b5da7-133">Sie können auch die **Option "CSS-Quell Karten aktivieren" aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b5da7-133">You may also check **Enable CSS Source Maps**.</span></span>  

> ##### <span data-ttu-id="b5da7-134">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="b5da7-134">Figure 1</span></span>  
> <span data-ttu-id="b5da7-135">Quell Karten aktivieren</span><span class="sxs-lookup"><span data-stu-id="b5da7-135">Enable Source Maps</span></span>  
> ![Quell Karten aktivieren][ImageSourceMaps]  

### <span data-ttu-id="b5da7-137">Debuggen mit Quell Karten</span><span class="sxs-lookup"><span data-stu-id="b5da7-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="b5da7-138">Wenn Sie Ihren Code und die Quell Karten Debuggen aktiviert haben, werden Quell Karten an zwei Stellen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b5da7-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="b5da7-139">In der Konsole \ (der Link zur Quelle sollte die ursprüngliche Datei und nicht die generierte sein. \)</span><span class="sxs-lookup"><span data-stu-id="b5da7-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="b5da7-140">Wenn Sie Code durchlaufen \ (die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen \)</span><span class="sxs-lookup"><span data-stu-id="b5da7-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  

<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## <span data-ttu-id="b5da7-141">@sourceURL und DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5da7-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="b5da7-142">Obwohl es sich nicht um die Quell Karten Spezifikation handelt, `@sourceURL` können Sie die Entwicklung beim Arbeiten mit evals erheblich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="b5da7-143">Dieser Helfer sieht der Eigenschaft sehr ähnlich `//# sourceMappingURL` und wird in den Spezifikationen des Quell Karten-V3-Codes tatsächlich erwähnt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="b5da7-144">Indem Sie den folgenden speziellen Kommentar in Ihren Code einbeziehen, der EVALED ist, können Sie evals und Inlineskripts und-Formatvorlagen benennen, damit jeder in Ihrem devtools als logischere Namen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5da7-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="b5da7-145">Navigieren Sie zur folgenden Seite.</span><span class="sxs-lookup"><span data-stu-id="b5da7-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="b5da7-146">Demo</span><span class="sxs-lookup"><span data-stu-id="b5da7-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="b5da7-147">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b5da7-147">Follow these steps.</span></span>  

1.  <span data-ttu-id="b5da7-148">Öffnen Sie das devtools, und wechseln Sie zum **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="b5da7-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="b5da7-149">Geben Sie einen Dateinamen in das Eingabefeld " **_Name Your Code:_** " ein.</span><span class="sxs-lookup"><span data-stu-id="b5da7-149">Enter in a filename into the **_Name your code:_** input field.</span></span>  
1.  <span data-ttu-id="b5da7-150">Klicken Sie auf die Schaltfläche **Kompilieren** .</span><span class="sxs-lookup"><span data-stu-id="b5da7-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="b5da7-151">Eine Benachrichtigung mit der ausgewerteten Summe aus der CoffeeScript-Quelle wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  

<span data-ttu-id="b5da7-152">Wenn Sie die Untergruppe " **_Quellen_** " erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b5da7-152">If you expand the **_Sources_** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="b5da7-153">Wenn Sie zum Anzeigen dieser Datei doppelklicken, enthält Sie das kompilierte JavaScript für die ursprüngliche Quelle.</span><span class="sxs-lookup"><span data-stu-id="b5da7-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="b5da7-154">In der letzten Zeile ist jedoch ein Kommentar, `// @sourceURL` der die ursprüngliche Quelldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="b5da7-155">Dies kann Ihnen beim Debuggen beim Arbeiten mit sprach Abstraktionen helfen.</span><span class="sxs-lookup"><span data-stu-id="b5da7-155">This may help you with debugging while working with language abstractions.</span></span>  

> ##### <span data-ttu-id="b5da7-156">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="b5da7-156">Figure 2</span></span>
> <span data-ttu-id="b5da7-157">Arbeiten mit sourceURL</span><span class="sxs-lookup"><span data-stu-id="b5da7-157">Working with sourceURL</span></span>  
> ![Arbeiten mit sourceURL][ImageCoffeeScript]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageSourceMaps]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png "Abbildung 1: Aktivieren von Quell Karten"  
[ImageCoffeeScript]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-coffeeeeeeee.msft.png "Abbildung 2: Arbeiten mit sourceURL"  

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
> <span data-ttu-id="b5da7-170">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5da7-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b5da7-171">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate, Google: Tools, Performance, Animation und UX) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5da7-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b5da7-173">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5da7-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
