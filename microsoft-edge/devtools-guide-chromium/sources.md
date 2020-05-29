---
title: Übersicht über das Quellen Panel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601908"
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
   limitations under the License. -->






# <span data-ttu-id="6f6fd-103">Übersicht über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="6f6fd-103">Sources Panel Overview</span></span> 



<span data-ttu-id="6f6fd-104">Verwenden Sie das Microsoft Edge devtools **Sources** Panel für folgende Zwecke:</span><span class="sxs-lookup"><span data-stu-id="6f6fd-104">Use the Microsoft Edge DevTools **Sources** panel to:</span></span>

*   <span data-ttu-id="6f6fd-105">[Dateien anzeigen](#view-files).</span><span class="sxs-lookup"><span data-stu-id="6f6fd-105">[View files](#view-files).</span></span>  
*   <span data-ttu-id="6f6fd-106">[Bearbeiten Sie CSS und JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="6f6fd-106">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="6f6fd-107">Sie können [JavaScript- **Snippets** erstellen und speichern](#create-save-and-run-snippets), die Sie möglicherweise auf einer beliebigen Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-107">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="6f6fd-108">**Snippets** ähneln Bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-108">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="6f6fd-109">[Debuggen von JavaScript](#debug-javascript)</span><span class="sxs-lookup"><span data-stu-id="6f6fd-109">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="6f6fd-110">[Richten Sie einen Arbeitsbereich ein](#set-up-a-workspace), damit Änderungen, die Sie in devtools vornehmen, in dem Code Ihres Dateisystems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-110">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  

## <span data-ttu-id="6f6fd-111">Anzeigen von Dateien</span><span class="sxs-lookup"><span data-stu-id="6f6fd-111">View files</span></span> 

<span data-ttu-id="6f6fd-112">Verwenden Sie den **Seiten** Bereich, um alle Ressourcen anzuzeigen, die von der Seite geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-112">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

> ##### <span data-ttu-id="6f6fd-113">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="6f6fd-113">Figure 1</span></span>  
> <span data-ttu-id="6f6fd-114">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="6f6fd-114">The **Page** pane</span></span>  
> ![Abbildung 1: der Seitenbereich][ImageSourcesPagePane]  

<span data-ttu-id="6f6fd-116">Organisation des **Seiten** Bereichs:</span><span class="sxs-lookup"><span data-stu-id="6f6fd-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="6f6fd-117">Die oberste Ebene, wie `top` in [**Abbildung 1**](#figure-1), stellt einen [HTML-Frame][W3CHtml4Frames]dar.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-117">The top-level, such as `top` in [**Figure 1**](#figure-1), represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="6f6fd-118">Finden `top` Sie auf jeder Seite, die Sie besuchen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-118">Find `top` on every page that you visit.</span></span> `top` <span data-ttu-id="6f6fd-119">stellt den Hauptdokument Frame dar.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="6f6fd-120">Die zweite Ebene, wie `docs.microsoft.com` in [**Abbildung 1**](#figure-1), stellt einen [Ursprung][HtmlstandardOrigin]dar.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-120">The second-level, such as `docs.microsoft.com` in [**Figure 1**](#figure-1), represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="6f6fd-121">Die dritte Ebene, die vierte Ebene usw., stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="6f6fd-122">In [**Abbildung 1**](#figure-1) wird beispielsweise der vollständige Pfad zur Ressource `devtools-guide-chromium`</span><span class="sxs-lookup"><span data-stu-id="6f6fd-122">For example, in [**Figure 1**](#figure-1) the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

<span data-ttu-id="6f6fd-123">Klicken Sie im **Seiten** Bereich auf eine Datei, um den Inhalt im **Editor** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="6f6fd-124">Sie können jede Art von Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-124">You may view any type of file.</span></span> <span data-ttu-id="6f6fd-125">Für Bilder wird eine Vorschau des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-125">For images, you see a preview of the image.</span></span>  

> ##### <span data-ttu-id="6f6fd-126">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="6f6fd-126">Figure 2</span></span>  
> <span data-ttu-id="6f6fd-127">Anzeigen des Inhalts `a4d10f71.index-docs.js` im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="6f6fd-127">Viewing the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
> ![Abbildung2.][ImageSourcesEditorPane]  

## <span data-ttu-id="6f6fd-130">Bearbeiten von CSS und JavaScript</span><span class="sxs-lookup"><span data-stu-id="6f6fd-130">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="6f6fd-131">Verwenden Sie den **Editor** Bereich, um CSS und JavaScript zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-131">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="6f6fd-132">DevTools aktualisiert die Seite, um den neuen Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-132">DevTools updates the page to run your new code.</span></span> <span data-ttu-id="6f6fd-133">Wenn Sie beispielsweise eine CSS-Datei bearbeiten, indem Sie unten die Stilregel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="6f6fd-133">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="6f6fd-134">Sie sollten sehen, dass die Änderung sofort wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-134">You should see that change take effect immediately.</span></span>

> ##### <span data-ttu-id="6f6fd-135">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="6f6fd-135">Figure 3</span></span>  
> <span data-ttu-id="6f6fd-136">Bearbeiten von CSS im **Editor** Bereich zum Ändern der Textfarbe des Untertitels in rot</span><span class="sxs-lookup"><span data-stu-id="6f6fd-136">Editing CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
> ![Abbildung3.][ImageEditCSS]  

<span data-ttu-id="6f6fd-139">CSS-Änderungen werden sofort wirksam, keine Speicherung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-139">CSS changes take effect immediately, no save needed.</span></span> <span data-ttu-id="6f6fd-140">Damit JavaScript-Änderungen wirksam werden, drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="6f6fd-140">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span> <span data-ttu-id="6f6fd-141">DevTools führt ein Skript nicht erneut aus, sodass nur die JavaScript-Änderungen wirksam werden, die Sie in Funktionen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-141">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="6f6fd-142">In [**Abbildung 4**](#figure-4) wird beispielsweise beschrieben, wie die Funktion `console.log('A')` nicht ausgeführt wird, während `console.log('B')` dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-142">For example, in [**Figure 4**](#figure-4) note how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span> <span data-ttu-id="6f6fd-143">Wenn devtools das gesamte Skript nach dem vornehmen der Änderung erneut ausgeführt hat, wurde der Text `A` in der **Konsole**protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-143">If DevTools re-ran the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

> ##### <span data-ttu-id="6f6fd-144">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="6f6fd-144">Figure 4</span></span>  
> <span data-ttu-id="6f6fd-145">Bearbeiten von JavaScript im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="6f6fd-145">Editing JavaScript in the **Editor** pane</span></span>  
> ![Abbildung 4.][ImageEditJS]  

<span data-ttu-id="6f6fd-148">DevTools löscht Ihre CSS-und JavaScript-Änderungen beim erneuten Laden der Seite.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-148">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span> <span data-ttu-id="6f6fd-149">Informationen zum Speichern der Änderungen an Ihrem Dateisystem finden Sie unter [Einrichten eines Arbeitsbereichs](#set-up-a-workspace) .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-149">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="6f6fd-150">Erstellen, speichern und Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="6f6fd-150">Create, save, and run Snippets</span></span> 

<span data-ttu-id="6f6fd-151">Snippets sind Skripts, die auf einer beliebigen Seite ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-151">Snippets are scripts which you may run on any page.</span></span> <span data-ttu-id="6f6fd-152">Stellen Sie sich vor, dass Sie den folgenden Code wiederholt in der **Konsole**eingeben, um die jQuery-Bibliothek auf einer Seite einzufügen, damit Sie jQuery-Befehle über die **Konsole**ausführen können:</span><span class="sxs-lookup"><span data-stu-id="6f6fd-152">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="6f6fd-153">Stattdessen können Sie diesen Code in einem **Snippet** speichern und mit ein paar Klicks auf die Schaltfläche ausführen, wenn Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-153">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="6f6fd-154">DevTools speichert das **Snippet** in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-154">DevTools saves the **Snippet** to your file system.</span></span>  

> ##### <span data-ttu-id="6f6fd-155">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="6f6fd-155">Figure 5</span></span>  
> <span data-ttu-id="6f6fd-156">Ein **Snippet** , das die jQuery-Bibliothek auf einer Seite einfügt</span><span class="sxs-lookup"><span data-stu-id="6f6fd-156">A **Snippet** that inserts the jQuery library into a page</span></span>  
> ![Abbildung5.][ImageSnippet]  

<span data-ttu-id="6f6fd-159">So führen Sie einen **Ausschnitt**aus:</span><span class="sxs-lookup"><span data-stu-id="6f6fd-159">To run a **Snippet**:</span></span>

*   <span data-ttu-id="6f6fd-160">Öffnen **Sie die** Datei über den Bereich **Snippets** , und klicken Sie auf ![ die Schaltfläche Ausführen ][ImageRunIcon] .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-160">Open the file via the **Snippets** pane, and click **Run** ![The Run button][ImageRunIcon].</span></span>  
*   <span data-ttu-id="6f6fd-161">Öffnen Sie das **[Menübefehl][DevtoolsGuideChromiumCommandMenuIndex]**, löschen `>` Sie das Zeichen, geben `!` Sie den Namen des **Snippets**ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-161">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  

<span data-ttu-id="6f6fd-162">Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevtoolsGuideChromiumJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-162">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>


## <span data-ttu-id="6f6fd-163">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="6f6fd-163">Debug JavaScript</span></span> 

<span data-ttu-id="6f6fd-164">Anstatt `console.log()` abzuleiten, wo Ihr JavaScript schief läuft, sollten Sie stattdessen die Microsoft Edge DevTools-Debugging-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-164">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span> <span data-ttu-id="6f6fd-165">Die allgemeine Idee ist, einen Haltepunkt zu definieren, der eine absichtliche Unterbrechung in Ihrem Code ist, und dann schrittweise durch die Laufzeit des Codes eine Zeile zu einem Zeitpunkt zu führen.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-165">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span> <span data-ttu-id="6f6fd-166">Wenn Sie den Code schrittweise durchlaufen, können Sie die Werte aller aktuell definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-166">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="6f6fd-167">Informationen zu den Grundlagen des Debuggens in devtools finden Sie unter [Erste Schritte beim Debuggen von JavaScript][DevtoolsGuideChromiumJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-167">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

> ##### <span data-ttu-id="6f6fd-168">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="6f6fd-168">Figure 6</span></span>  
> <span data-ttu-id="6f6fd-169">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="6f6fd-169">Debugging JavaScript</span></span>  
> ![Abbildung6.][ImageDebugging]  

## <span data-ttu-id="6f6fd-172">Einrichten eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6f6fd-172">Set up a Workspace</span></span> 

<span data-ttu-id="6f6fd-173">Wenn Sie eine Datei im **Quellen** Panel bearbeiten, gehen diese Änderungen standardmäßig verloren, wenn Sie die Seite erneut laden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-173">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="6f6fd-174">Mit **Arbeitsbereichen** können Sie die Änderungen, die Sie in devtools vornehmen, in Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-174">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="6f6fd-175">Im Wesentlichen können Sie damit devtools als Code-Editor verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-175">Essentially, this lets you use DevTools as your code editor.</span></span>

<span data-ttu-id="6f6fd-176">Weitere Informationen finden Sie unter [Bearbeiten von Dateien mit Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex] .</span><span class="sxs-lookup"><span data-stu-id="6f6fd-176">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Abbildung 1: der Seitenbereich"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Abbildung 2: Anzeigen des Inhalts von "a4d10f71. Index-docs. js" im Bereich "Editor""  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Abbildung 3: Bearbeiten von CSS im Editor Bereich zum Ändern der Textfarbe des Untertitels in rot"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Abbildung 4: Bearbeiten von JavaScript im Bereich "Editor""  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Abbildung 5: ein Snippet, das die jQuery-Bibliothek auf einer Seite einfügt"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Abbildung 6: Debuggen von JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Bearbeiten von Dateien mit Arbeitsbereichen"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin-HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> <span data-ttu-id="6f6fd-189">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6f6fd-190">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f6fd-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6f6fd-192">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f6fd-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
