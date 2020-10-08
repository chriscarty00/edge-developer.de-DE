---
description: Anzeigen und Bearbeiten von Dateien, Erstellen von Ausschnitten, Debuggen von JavaScript und Einrichten von Arbeitsbereichen im Quellen Panel von Microsoft Edge devtools
title: Übersicht über das Quellenpanel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 029693ba27665a556446f4349c1517c53ff39b02
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993541"
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







# <span data-ttu-id="60517-104">Übersicht über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="60517-104">Sources panel overview</span></span> 



<span data-ttu-id="60517-105">Verwenden Sie das Microsoft Edge devtools **Sources** Panel, um die Folowing-Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="60517-105">Use the Microsoft Edge DevTools **Sources** panel to perform the folowing actions.</span></span>  

*   <span data-ttu-id="60517-106">[Dateien anzeigen](#view-files).</span><span class="sxs-lookup"><span data-stu-id="60517-106">[View files](#view-files).</span></span>  
*   <span data-ttu-id="60517-107">[Bearbeiten Sie CSS und JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="60517-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="60517-108">Sie können [JavaScript- **Snippets** erstellen und speichern](#create-save-and-run-snippets), die Sie möglicherweise auf einer beliebigen Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="60517-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="60517-109">**Snippets** ähneln Bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="60517-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="60517-110">[Debuggen von JavaScript](#debug-javascript)</span><span class="sxs-lookup"><span data-stu-id="60517-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="60517-111">[Richten Sie einen Arbeitsbereich ein](#set-up-a-workspace), damit Änderungen, die Sie in devtools vornehmen, in dem Code Ihres Dateisystems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="60517-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="60517-112">Anzeigen von Dateien</span><span class="sxs-lookup"><span data-stu-id="60517-112">View files</span></span> 

<span data-ttu-id="60517-113">Verwenden Sie den **Seiten** Bereich, um alle Ressourcen anzuzeigen, die von der Seite geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="60517-113">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Seitenbereich" lightbox="./media/sources-page-pane.msft.png":::
   <span data-ttu-id="60517-115">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="60517-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="60517-116">Organisation des **Seiten** Bereichs:</span><span class="sxs-lookup"><span data-stu-id="60517-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="60517-117">Die oberste Ebene, wie `top` in der vorherigen Abbildung, stellt einen [HTML-Frame][W3CHtml4Frames]dar.</span><span class="sxs-lookup"><span data-stu-id="60517-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="60517-118">Finden `top` Sie auf jeder Seite, die Sie besuchen.</span><span class="sxs-lookup"><span data-stu-id="60517-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="60517-119">stellt den Hauptdokument Frame dar.</span><span class="sxs-lookup"><span data-stu-id="60517-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="60517-120">Die zweite Ebene, wie `docs.microsoft.com` in der vorhergehenden Abbildung, stellt einen [Ursprung][HtmlstandardOrigin]dar.</span><span class="sxs-lookup"><span data-stu-id="60517-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="60517-121">Die dritte Ebene, die vierte Ebene usw., stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="60517-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="60517-122">In der vorherigen Abbildung wird beispielsweise der vollständige Pfad zur Ressource `devtools-guide-chromium`</span><span class="sxs-lookup"><span data-stu-id="60517-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="60517-123">Klicken Sie im **Seiten** Bereich auf eine Datei, um den Inhalt im **Editor** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="60517-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="60517-124">Sie können jede Art von Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="60517-124">You may view any type of file.</span></span>  <span data-ttu-id="60517-125">Für Bilder wird eine Vorschau des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60517-125">For images, you see a preview of the image.</span></span>  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Seitenbereich" lightbox="./media/sources-editor-pane.msft.png":::
   <span data-ttu-id="60517-127">Anzeigen des Inhalts `a4d10f71.index-docs.js` im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="60517-127">View the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="60517-128">Bearbeiten von CSS und JavaScript</span><span class="sxs-lookup"><span data-stu-id="60517-128">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="60517-129">Verwenden Sie den **Editor** Bereich, um CSS und JavaScript zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="60517-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="60517-130">DevTools aktualisiert die Seite, um den neuen Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="60517-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="60517-131">Wenn Sie beispielsweise eine CSS-Datei bearbeiten, indem Sie unten die Stilregel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="60517-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="60517-132">Sie sollten sehen, dass die Änderung sofort wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="60517-132">You should see that change take effect immediately.</span></span>

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Seitenbereich" lightbox="./media/edit-css.msft.png":::
   <span data-ttu-id="60517-134">Bearbeiten von CSS im **Editor** Bereich zum Ändern der Textfarbe des Untertitels in rot</span><span class="sxs-lookup"><span data-stu-id="60517-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="60517-135">CSS-Änderungen werden sofort wirksam, keine Speicherung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60517-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="60517-136">Damit JavaScript-Änderungen wirksam werden, drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="60517-136">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="60517-137">DevTools führt ein Skript nicht erneut aus, sodass nur die JavaScript-Änderungen wirksam werden, die Sie in Funktionen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="60517-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="60517-138">Beachten Sie beispielsweise in der folgenden Abbildung, wie diese `console.log('A')` nicht ausgeführt wird, während `console.log('B')` dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="60517-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="60517-139">Wenn devtools das gesamte Skript nach dem vornehmen der Änderung erneut ausführt, wurde der Text `A` in der **Konsole**protokolliert.</span><span class="sxs-lookup"><span data-stu-id="60517-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Seitenbereich" lightbox="./media/edit-js.msft.png":::
   <span data-ttu-id="60517-141">Bearbeiten von JavaScript im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="60517-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="60517-142">DevTools löscht Ihre CSS-und JavaScript-Änderungen beim erneuten Laden der Seite.</span><span class="sxs-lookup"><span data-stu-id="60517-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="60517-143">Informationen zum Speichern der Änderungen an Ihrem Dateisystem finden Sie unter [Einrichten eines Arbeitsbereichs](#set-up-a-workspace) .</span><span class="sxs-lookup"><span data-stu-id="60517-143">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="60517-144">Erstellen, speichern und Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="60517-144">Create, save, and run Snippets</span></span> 

<span data-ttu-id="60517-145">Snippets sind Skripts, die auf einer beliebigen Seite ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="60517-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="60517-146">Stellen Sie sich vor, dass Sie den folgenden Code wiederholt in der **Konsole**eingeben, um die jQuery-Bibliothek auf einer Seite einzufügen, damit Sie jQuery-Befehle über die **Konsole**ausführen können:</span><span class="sxs-lookup"><span data-stu-id="60517-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="60517-147">Stattdessen können Sie diesen Code in einem **Snippet** speichern und mit ein paar Klicks auf die Schaltfläche ausführen, wenn Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="60517-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="60517-148">DevTools speichert das **Snippet** in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="60517-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Seitenbereich" lightbox="./media/snippet.msft.png":::
   <span data-ttu-id="60517-150">Ein **Snippet** , das die jQuery-Bibliothek auf einer Seite einfügt</span><span class="sxs-lookup"><span data-stu-id="60517-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="60517-151">So führen Sie einen **Ausschnitt**aus:</span><span class="sxs-lookup"><span data-stu-id="60517-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="60517-152">Öffnen Sie die Datei über den Bereich **Snippets** , und klicken Sie auf **Ausführen** \ ( ![ die Schaltfläche Ausführen ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="60517-152">Open the file using the **Snippets** pane, and click **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="60517-153">Öffnen Sie das **[Menübefehl][DevtoolsGuideChromiumCommandMenuIndex]**, löschen `>` Sie das Zeichen, geben `!` Sie den Namen des **Snippets**ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="60517-153">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  
    
<span data-ttu-id="60517-154">Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevtoolsGuideChromiumJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="60517-154">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="60517-155">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="60517-155">Debug JavaScript</span></span> 

<span data-ttu-id="60517-156">Anstatt `console.log()` abzuleiten, wo Ihr JavaScript schief läuft, sollten Sie stattdessen die Microsoft Edge DevTools-Debugging-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="60517-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="60517-157">Die allgemeine Idee ist, einen Haltepunkt zu definieren, der eine absichtliche Unterbrechung in Ihrem Code ist, und dann schrittweise durch die Laufzeit des Codes eine Zeile zu einem Zeitpunkt zu führen.</span><span class="sxs-lookup"><span data-stu-id="60517-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="60517-158">Wenn Sie den Code schrittweise durchlaufen, können Sie die Werte aller aktuell definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="60517-158">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="60517-159">Informationen zu den Grundlagen des Debuggens in devtools finden Sie unter [Erste Schritte beim Debuggen von JavaScript][DevtoolsGuideChromiumJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="60517-159">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="./media/debugging.msft.png" alt-text="Seitenbereich" lightbox="./media/debugging.msft.png":::
   <span data-ttu-id="60517-161">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="60517-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="60517-162">Einrichten eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="60517-162">Set up a Workspace</span></span> 

<span data-ttu-id="60517-163">Wenn Sie eine Datei im **Quellen** Panel bearbeiten, gehen diese Änderungen standardmäßig verloren, wenn Sie die Seite erneut laden.</span><span class="sxs-lookup"><span data-stu-id="60517-163">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="60517-164">Mit **Arbeitsbereichen** können Sie die Änderungen, die Sie in devtools vornehmen, in Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="60517-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="60517-165">Im Wesentlichen kann devtools als Code-Editor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60517-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="60517-166">Weitere Informationen finden Sie unter [Bearbeiten von Dateien mit Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex] .</span><span class="sxs-lookup"><span data-stu-id="60517-166">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

<!--  
 


-->  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin-HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> <span data-ttu-id="60517-173">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60517-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="60517-174">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="60517-174">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="60517-176">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60517-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
