---
description: Anzeigen und Bearbeiten von Dateien, Erstellen von Ausschnitten, Debuggen von JavaScript und Einrichten von Arbeitsbereichen im Quellen Panel von Microsoft Edge devtools
title: Übersicht über das Quellenpanel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233720"
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

# <span data-ttu-id="c005c-104">Übersicht über das Quellenpanel</span><span class="sxs-lookup"><span data-stu-id="c005c-104">Sources panel overview</span></span>  

<span data-ttu-id="c005c-105">Verwenden Sie das Panel Microsoft Edge devtools **Sources** , um die folgenden Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c005c-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="c005c-106">[Anzeigen von Dateien](#display-files)</span><span class="sxs-lookup"><span data-stu-id="c005c-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="c005c-107">[Bearbeiten Sie CSS und JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="c005c-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="c005c-108">Sie können [JavaScript- **Snippets** erstellen und speichern](#create-save-and-run-snippets), die Sie möglicherweise auf einer beliebigen Webseite ausführen.</span><span class="sxs-lookup"><span data-stu-id="c005c-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="c005c-109">**Snippets** ähneln Bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="c005c-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="c005c-110">[Debuggen von JavaScript](#debug-javascript)</span><span class="sxs-lookup"><span data-stu-id="c005c-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="c005c-111">[Richten Sie einen Arbeitsbereich ein](#set-up-a-workspace), damit Änderungen, die Sie in devtools vornehmen, in dem Code Ihres Dateisystems gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c005c-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="c005c-112">Anzeigen von Dateien</span><span class="sxs-lookup"><span data-stu-id="c005c-112">Display files</span></span>  

<span data-ttu-id="c005c-113">Verwenden Sie den **Seiten** Bereich, um alle Ressourcen anzuzeigen, die von der Seite geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="c005c-113">Use the **Page** pane to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Seitenbereich" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="c005c-115">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="c005c-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="c005c-116">Organisation des **Seiten** Bereichs:</span><span class="sxs-lookup"><span data-stu-id="c005c-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="c005c-117">Die oberste Ebene, wie `top` in der vorherigen Abbildung, stellt einen [HTML-Frame][W3CHtml4Frames]dar.</span><span class="sxs-lookup"><span data-stu-id="c005c-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="c005c-118">Finden `top` Sie auf jeder Seite, die Sie besuchen.</span><span class="sxs-lookup"><span data-stu-id="c005c-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="c005c-119">stellt den Hauptdokument Frame dar.</span><span class="sxs-lookup"><span data-stu-id="c005c-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="c005c-120">Die zweite Ebene, wie `docs.microsoft.com` in der vorhergehenden Abbildung, stellt einen [Ursprung][HtmlstandardOrigin]dar.</span><span class="sxs-lookup"><span data-stu-id="c005c-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="c005c-121">Die dritte Ebene, die vierte Ebene usw., stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="c005c-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="c005c-122">In der vorherigen Abbildung wird beispielsweise der vollständige Pfad zur Ressource `devtools-guide-chromium`</span><span class="sxs-lookup"><span data-stu-id="c005c-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="c005c-123">Wählen Sie im **Seiten** Bereich eine Datei aus, um den Inhalt im **Editor** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c005c-123">Choose a file in the **Page** pane to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="c005c-124">Sie können jede Art von Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c005c-124">You may display any type of file.</span></span>  <span data-ttu-id="c005c-125">Bei Bildern wird eine Vorschau des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c005c-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Anzeigen der Inhalte von a4d10f71.index-docs.js im Bereich "Editor"" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="c005c-127">Anzeigen des Inhalts `a4d10f71.index-docs.js` im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="c005c-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="c005c-128">Bearbeiten von CSS und JavaScript</span><span class="sxs-lookup"><span data-stu-id="c005c-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="c005c-129">Verwenden Sie den **Editor** Bereich, um CSS und JavaScript zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c005c-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="c005c-130">DevTools aktualisiert die Seite, um den neuen Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c005c-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="c005c-131">Wenn Sie beispielsweise eine CSS-Datei bearbeiten, indem Sie unten die Stilregel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="c005c-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="c005c-132">Diese Änderung sollte sofort wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="c005c-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editor Bereich zum Ändern der Textfarbe des Untertitels in rot" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="c005c-134">Bearbeiten von CSS im **Editor** Bereich zum Ändern der Textfarbe des Untertitels in rot</span><span class="sxs-lookup"><span data-stu-id="c005c-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="c005c-135">CSS-Änderungen werden sofort wirksam, keine Speicherung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c005c-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="c005c-136">Damit JavaScript-Änderungen wirksam werden, wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="c005c-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="c005c-137">DevTools führt ein Skript nicht erneut aus, sodass nur die JavaScript-Änderungen wirksam werden, die Sie in Funktionen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c005c-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="c005c-138">Beachten Sie beispielsweise in der folgenden Abbildung, wie diese `console.log('A')` nicht ausgeführt wird, während `console.log('B')` dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c005c-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="c005c-139">Wenn devtools das gesamte Skript nach dem vornehmen der Änderung erneut ausführt, wurde der Text `A` in der **Konsole**protokolliert.</span><span class="sxs-lookup"><span data-stu-id="c005c-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Bearbeiten von JavaScript im Bereich "Editor"" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="c005c-141">Bearbeiten von JavaScript im Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="c005c-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="c005c-142">DevTools löscht Ihre CSS-und JavaScript-Änderungen beim erneuten Laden der Seite.</span><span class="sxs-lookup"><span data-stu-id="c005c-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="c005c-143">Navigieren Sie zum [Einrichten eines Arbeitsbereichs](#set-up-a-workspace) , um zu erfahren, wie Sie die Änderungen in Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="c005c-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="c005c-144">Erstellen, speichern und Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c005c-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="c005c-145">Snippets sind Skripts, die auf einer beliebigen Seite ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c005c-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="c005c-146">Stellen Sie sich vor, dass Sie den folgenden Code wiederholt in der **Konsole**eingeben, um die jQuery-Bibliothek auf einer Seite einzufügen, damit Sie jQuery-Befehle über die **Konsole**ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c005c-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="c005c-147">Stattdessen können Sie diesen Code in einem **Snippet** speichern und mit ein paar Klicks auf die Schaltfläche ausführen, wenn Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="c005c-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="c005c-148">DevTools speichert das **Snippet** in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="c005c-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Snippet, das die jQuery-Bibliothek auf einer Seite einfügt" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="c005c-150">Ein **Snippet** , das die jQuery-Bibliothek auf einer Seite einfügt</span><span class="sxs-lookup"><span data-stu-id="c005c-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="c005c-151">So führen Sie einen **Ausschnitt**aus:</span><span class="sxs-lookup"><span data-stu-id="c005c-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="c005c-152">Öffnen Sie die Datei über den Bereich **Snippets** , und wählen Sie **Ausführen** \ ( ![ die Schaltfläche Ausführen ][ImageRunIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="c005c-152">Open the file using the **Snippets** pane, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="c005c-153">Öffnen Sie das [Menübefehl][DevtoolsGuideChromiumCommandMenuIndex], löschen `>` Sie das Zeichen, geben `!` Sie den Namen des **Snippets**ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c005c-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="c005c-154">Navigieren Sie zum [Ausführen von Codeausschnitten auf jeder Seite][DevtoolsGuideChromiumJavascriptSnippets] , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c005c-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="c005c-155">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="c005c-155">Debug JavaScript</span></span>  

<span data-ttu-id="c005c-156">Anstatt `console.log()` abzuleiten, wo Ihr JavaScript schief läuft, sollten Sie stattdessen die Microsoft Edge DevTools-Debugging-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="c005c-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="c005c-157">Die allgemeine Idee ist, einen Haltepunkt zu definieren, der eine absichtliche Unterbrechung in Ihrem Code ist, und dann schrittweise durch die Laufzeit des Codes eine Zeile zu einem Zeitpunkt zu führen.</span><span class="sxs-lookup"><span data-stu-id="c005c-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="c005c-158">Wenn Sie den Code schrittweise durchlaufen, können Sie die Werte aller aktuell definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="c005c-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="c005c-159">Navigieren Sie zu den [ersten Schritten beim Debuggen von JavaScript][DevtoolsGuideChromiumJavascriptIndex] , um die Grundlagen des Debuggens in devtools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="c005c-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Debuggen von JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="c005c-161">Debuggen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="c005c-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="c005c-162">Einrichten eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c005c-162">Set up a Workspace</span></span>  

<span data-ttu-id="c005c-163">Wenn Sie eine Datei im **Quellen** Tool bearbeiten, gehen diese Änderungen standardmäßig verloren, wenn Sie die Seite erneut laden.</span><span class="sxs-lookup"><span data-stu-id="c005c-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="c005c-164">Mit **Arbeitsbereichen** können Sie die Änderungen, die Sie in devtools vornehmen, in Ihrem Dateisystem speichern.</span><span class="sxs-lookup"><span data-stu-id="c005c-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="c005c-165">Im Wesentlichen kann devtools als Code-Editor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c005c-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="c005c-166">Navigieren Sie zu den ersten Schritten, um [Dateien mit Arbeitsbereichen zu bearbeiten][DevtoolsGuideChromiumWorkspacesIndex] .</span><span class="sxs-lookup"><span data-stu-id="c005c-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <span data-ttu-id="c005c-167">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c005c-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Herkunft | HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> <span data-ttu-id="c005c-174">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c005c-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c005c-175">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c005c-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c005c-177">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c005c-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
