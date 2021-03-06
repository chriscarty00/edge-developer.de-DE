---
description: Anzeigen und Bearbeiten von Dateien, Erstellen von Codeausschnitten, Debuggen von JavaScript und Einrichten von Arbeitsbereichen im Bereich Quellen von Microsoft Edge DevTools.
title: Übersicht über das Quellenpanel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4677bf82d3506a4b8d6336ded7ab557b794fd3df
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397762"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="sources-panel-overview"></a><span data-ttu-id="a0036-104">Übersicht über das Quellenpanel</span><span class="sxs-lookup"><span data-stu-id="a0036-104">Sources panel overview</span></span>  

<span data-ttu-id="a0036-105">Verwenden Sie den \*\*\*\* Microsoft Edge DevTools Sources-Bereich, um die folgenden Aktionen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a0036-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="a0036-106">[Anzeigen von Dateien](#display-files).</span><span class="sxs-lookup"><span data-stu-id="a0036-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="a0036-107">[Bearbeiten von CSS und JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="a0036-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="a0036-108">[Erstellen und speichern **Sie Codeausschnitte** von JavaScript](#create-save-and-run-snippets), die Sie auf jeder Beliebigen Webseite ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a0036-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="a0036-109">**Codeausschnitte** ähneln Bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="a0036-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="a0036-110">[Debuggen von JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="a0036-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="a0036-111">[Richten Sie einen Arbeitsbereich](#set-up-a-workspace)ein, damit Änderungen, die Sie in DevTools vornehmen, im Code ihres Dateisystems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a0036-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <a name="display-files"></a><span data-ttu-id="a0036-112">Anzeigen von Dateien</span><span class="sxs-lookup"><span data-stu-id="a0036-112">Display files</span></span>  

<span data-ttu-id="a0036-113">Verwenden \*\*\*\* Des Seitenbereichs; , um alle Ressourcen, die die Seite geladen hat, anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a0036-113">Use the **Page** panel; to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Seitenbereich" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="a0036-115">**Seitenbereich**</span><span class="sxs-lookup"><span data-stu-id="a0036-115">The **Page** panel</span></span>  
:::image-end:::  

<span data-ttu-id="a0036-116">So wird **der Seitenbereich** organisiert:</span><span class="sxs-lookup"><span data-stu-id="a0036-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="a0036-117">Die oberste Ebene, z. B. `top` in der vorherigen Abbildung, stellt einen [HTML-Frame dar.][W3CHtml4Frames]</span><span class="sxs-lookup"><span data-stu-id="a0036-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="a0036-118">Suchen `top` Sie auf jeder Seite, die Sie besuchen.</span><span class="sxs-lookup"><span data-stu-id="a0036-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="a0036-119">stellt den Hauptdokumentrahmen dar.</span><span class="sxs-lookup"><span data-stu-id="a0036-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="a0036-120">Die zweite Ebene, z. B. `docs.microsoft.com` in der vorherigen Abbildung, stellt einen [Ursprung dar.][HtmlstandardOrigin]</span><span class="sxs-lookup"><span data-stu-id="a0036-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="a0036-121">Die dritte Ebene, die vierte Ebene und so weiter stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0036-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="a0036-122">In der vorherigen Abbildung ist z. B. der vollständige Pfad zur `devtools-guide-chromium` Ressource</span><span class="sxs-lookup"><span data-stu-id="a0036-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="a0036-123">Wählen Sie eine Datei im **Bereich Seite** aus, um den Inhalt im **Editorbereich anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="a0036-123">Choose a file in the **Page** panel to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="a0036-124">Sie können einen beliebigen Dateityp anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0036-124">You may display any type of file.</span></span>  <span data-ttu-id="a0036-125">Für Bilder wird eine Vorschau des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0036-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Anzeigen des Inhalts von a4d10f71.index-docs.js im Editorbereich" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="a0036-127">Anzeigen des Inhalts `a4d10f71.index-docs.js` im **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="a0036-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** panel</span></span>  
:::image-end:::  

## <a name="edit-css-and-javascript"></a><span data-ttu-id="a0036-128">Bearbeiten von CSS und JavaScript</span><span class="sxs-lookup"><span data-stu-id="a0036-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="a0036-129">Verwenden Sie den **Editorbereich,** um CSS und JavaScript zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a0036-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="a0036-130">DevTools aktualisiert die Seite, um den neuen Code ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="a0036-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="a0036-131">Wenn Sie z. B. eine CSS-Datei bearbeiten, indem Sie die folgende Formatvorlagenregel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="a0036-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="a0036-132">Diese Änderung sollte sofort wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="a0036-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editorbereich, um die Textfarbe des Untertitels in Rot zu ändern" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="a0036-134">Bearbeiten von CSS im **Editorbereich,** um die Textfarbe des Untertitels in Rot zu ändern</span><span class="sxs-lookup"><span data-stu-id="a0036-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="a0036-135">CSS-Änderungen werden sofort wirksam, es ist kein Speichern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0036-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="a0036-136">Damit JavaScript-Änderungen wirksam werden, wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="a0036-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="a0036-137">DevTools führt kein Skript erneut aus, daher sind die einzigen JavaScript-Änderungen, die wirksam werden, diejenigen, die Sie innerhalb von Funktionen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a0036-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="a0036-138">Beachten Sie beispielsweise in der folgenden Abbildung, wie `console.log('A')` nicht ausgeführt wird. `console.log('B')`</span><span class="sxs-lookup"><span data-stu-id="a0036-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="a0036-139">Wenn DevTools das gesamte Skript nach der Änderung erneut ausgeführt hat, wird der Text `A` bei der **Konsole protokolliert.**</span><span class="sxs-lookup"><span data-stu-id="a0036-139">If DevTools re-runs the entire script after making the change, then the text `A` is logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Bearbeiten von JavaScript im Editorbereich" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="a0036-141">Bearbeiten von JavaScript im **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="a0036-141">Editing JavaScript in the **Editor** panel</span></span>  
:::image-end:::  

<span data-ttu-id="a0036-142">DevTools löscht Ihre CSS- und JavaScript-Änderungen, wenn Sie die Seite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a0036-142">DevTools erases your CSS and JavaScript changes when you refresh the page.</span></span>  <span data-ttu-id="a0036-143">Navigieren Sie [zu Einrichten eines Arbeitsbereichs,](#set-up-a-workspace) um zu erfahren, wie Sie die Änderungen an Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="a0036-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <a name="create-save-and-run-snippets"></a><span data-ttu-id="a0036-144">Erstellen, Speichern und Ausführen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="a0036-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="a0036-145">Codeausschnitte sind Skripts, die Sie auf jeder Beliebigen Seite ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a0036-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="a0036-146">Stellen Sie sich vor, Sie geben den folgenden Code wiederholt in die Konsole **ein,** um die jQuery-Bibliothek in eine Seite zu einfügen, damit Sie jQuery-Befehle aus der Konsole **ausführen können.**</span><span class="sxs-lookup"><span data-stu-id="a0036-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="a0036-147">Stattdessen können Sie diesen Code in einem Codeausschnitt **speichern** und mit ein paar Schaltflächenklicks ausführen, wenn Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="a0036-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="a0036-148">DevTools speichert den **Codeausschnitt** in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="a0036-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Codeausschnitt, der die jQuery-Bibliothek in eine Seite einfüge" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="a0036-150">Ein **Codeausschnitt,** der die jQuery-Bibliothek in eine Seite einfüge</span><span class="sxs-lookup"><span data-stu-id="a0036-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="a0036-151">So führen Sie einen **Codeausschnitt aus:**</span><span class="sxs-lookup"><span data-stu-id="a0036-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="a0036-152">Öffnen Sie die Datei mithilfe des **Codeausschnittbereichs,** und wählen Sie **Ausführen** \( ![ Die Schaltfläche Ausführen ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a0036-152">Open the file using the **Snippets** panel, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="a0036-153">Öffnen Sie [das Befehlsmenü,][DevtoolsGuideChromiumCommandMenuIndex]löschen Sie das Zeichen, geben Sie ein, geben Sie den Namen Ihres Codeausschnitts `>` `!` ein, und wählen Sie dann \*\*\*\* `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a0036-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="a0036-154">Navigieren Sie [zu Codeausschnitte von beliebigen Seiten ausführen,][DevtoolsGuideChromiumJavascriptSnippets] um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0036-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <a name="debug-javascript"></a><span data-ttu-id="a0036-155">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="a0036-155">Debug JavaScript</span></span>  

<span data-ttu-id="a0036-156">Anstatt zu verwenden, um zu abfingen, wo Ihr JavaScript falsch läuft, sollten Sie stattdessen die `console.log()` Microsoft Edge DevTools-Debuggingtools verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0036-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="a0036-157">Die allgemeine Idee besteht im Festlegen eines Haltepunkts, bei dem es sich um einen beabsichtigten Stopport im Code handelt, und dann die Laufzeit des Codes, eine Zeile nach der anderen, zu durchbrechen.</span><span class="sxs-lookup"><span data-stu-id="a0036-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="a0036-158">Wenn Sie den Code durchschritten, können Sie die Werte aller derzeit definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="a0036-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="a0036-159">Navigieren Sie zu Erste Schritte mit Debuggen von [JavaScript,][DevtoolsGuideChromiumJavascriptIndex] um die Grundlagen des Debuggens in DevTools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="a0036-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Debuggen von JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="a0036-161">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="a0036-161">Debug JavaScript</span></span>  
:::image-end:::  

## <a name="set-up-a-workspace"></a><span data-ttu-id="a0036-162">Einrichten eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a0036-162">Set up a Workspace</span></span>  

<span data-ttu-id="a0036-163">Wenn Sie eine Datei im \*\*\*\* Tool Quellen bearbeiten, gehen diese Änderungen beim Aktualisieren der Seite standardmäßig verloren.</span><span class="sxs-lookup"><span data-stu-id="a0036-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you refresh the page.</span></span>  <span data-ttu-id="a0036-164">**Mit Arbeitsbereichen** können Sie die Änderungen, die Sie in DevTools vornehmen, in Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="a0036-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="a0036-165">Im Wesentlichen kann DevTools als Code-Editor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0036-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="a0036-166">Navigieren Sie [zu Bearbeiten von Dateien mit Arbeitsbereichen,][DevtoolsGuideChromiumWorkspacesIndex] um die ersten Schritte zu starten.</span><span class="sxs-lookup"><span data-stu-id="a0036-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a0036-167">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a0036-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft Docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Ursprung | HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> <span data-ttu-id="a0036-174">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0036-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a0036-175">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a0036-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a0036-177">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a0036-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
