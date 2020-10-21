---
description: Snippets sind kleine Skripts, die Sie im Quellen Panel von Microsoft Edge devtools erstellen und ausführen können.  Sie können auf jeder beliebigen Seite darauf zugreifen und diese ausführen.  Wenn Sie einen Ausschnitt ausführen, wird er im Kontext der aktuell geöffneten Seite ausgeführt.
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124740"
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

# <span data-ttu-id="b5b10-106">Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="b5b10-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b5b10-107">Wenn Sie feststellen, dass derselbe Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausgeführt wird, sollten Sie stattdessen den Code als Snippet speichern.</span><span class="sxs-lookup"><span data-stu-id="b5b10-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="b5b10-108">Ausschnitte sind Skripts, die Sie im [Quellen][DevToolsSourcesPanel] Panel erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="b5b10-109">Sie haben Zugriff auf den JavaScript-Kontext der Seite, und Sie können Sie auf einer beliebigen Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="b5b10-110">Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="b5b10-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="b5b10-111">Firefox devtools verfügt über ein ähnliches Feature wie Snippets mit [dem Namen "][MDNScratchpad]Zwischenablage".</span><span class="sxs-lookup"><span data-stu-id="b5b10-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="b5b10-112">In der folgenden Abbildung ist beispielsweise die devtools-Homepage auf der linken Seite und ein Codeausschnitt Quellcode auf der rechten Seite zu sehen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="b5b10-114">Aussehen der Seite vor dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="b5b10-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="b5b10-115">Der Snippet-Quellcode aus der vorhergehenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="b5b10-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="b5b10-116">In der folgenden Abbildung wird die Seite nach dem Ausführen des Snippets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5b10-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="b5b10-117">Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Seite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="b5b10-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="b5b10-119">Aussehen der Seite nach dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="b5b10-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="b5b10-120">Öffnen des Bereichs "Snippets"</span><span class="sxs-lookup"><span data-stu-id="b5b10-120">Open the Snippets pane</span></span>  

<span data-ttu-id="b5b10-121">Im Bereich **Snippets** werden Ihre Snippets aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b5b10-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="b5b10-122">Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="b5b10-124">Der Bereich " **Ausschnitte** "</span><span class="sxs-lookup"><span data-stu-id="b5b10-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="b5b10-125">Öffnen des Bereichs "Ausschnitte" mit einer Maus</span><span class="sxs-lookup"><span data-stu-id="b5b10-125">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="b5b10-126">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="b5b10-127">Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b5b10-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="b5b10-129">Das Fenster " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**</span><span class="sxs-lookup"><span data-stu-id="b5b10-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5b10-130">Klicken Sie auf die Registerkarte **Snippets** , um den Bereich **Snippets** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="b5b10-131">Möglicherweise müssen Sie **weitere Registerkarten** auswählen \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \), um auf die Option **Snippets** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-131">You might need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="b5b10-132">Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="b5b10-132">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="b5b10-133">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="b5b10-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="b5b10-134">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-134">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5b10-135">Beginnen `Snippets` Sie mit der Eingabe, wählen Sie **Snippets anzeigen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-135">Start typing `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="b5b10-137">Der Befehl ' **Snippets anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="b5b10-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b5b10-138">Erstellen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b5b10-138">Create Snippets</span></span>  

### <span data-ttu-id="b5b10-139">Erstellen eines Snippets über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="b5b10-139">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="b5b10-140">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="b5b10-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5b10-141">Wählen Sie **Neues Snippet**aus.</span><span class="sxs-lookup"><span data-stu-id="b5b10-141">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="b5b10-142">Geben Sie einen Namen für das Snippet ein, und wählen Sie dann `Enter` Speichern aus.</span><span class="sxs-lookup"><span data-stu-id="b5b10-142">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="b5b10-144">Benennen eines Snippets</span><span class="sxs-lookup"><span data-stu-id="b5b10-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b5b10-145">Erstellen eines Snippets über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="b5b10-145">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="b5b10-146">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="b5b10-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="b5b10-147">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5b10-148">Beginnen `Snippet` Sie mit der Eingabe, wählen Sie **Neues Snippet erstellen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-148">Start typing `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="b5b10-150">Der Befehl zum Erstellen eines neuen Snippets</span><span class="sxs-lookup"><span data-stu-id="b5b10-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b5b10-151">Weitere Informationen finden Sie unter [Umbenennen von Snippets](#rename-snippets) , wenn Sie Ihrem neuen Snippet einen benutzerdefinierten Namen zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="b5b10-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="b5b10-152">Bearbeiten von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b5b10-152">Edit Snippets</span></span>  

1.  <span data-ttu-id="b5b10-153">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="b5b10-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5b10-154">Klicken Sie im Bereich **Snippets** auf den Namen des Ausschnitts, den Sie bearbeiten möchten, um ihn im **Code-Editor**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="b5b10-156">Der **Code-Editor**</span><span class="sxs-lookup"><span data-stu-id="b5b10-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5b10-157">Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="b5b10-158">Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="b5b10-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="b5b10-159">Wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b5b10-159">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="b5b10-161">Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt</span><span class="sxs-lookup"><span data-stu-id="b5b10-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b5b10-162">Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b5b10-162">Run Snippets</span></span>  

### <span data-ttu-id="b5b10-163">Ausführen eines Snippets im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="b5b10-163">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="b5b10-164">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="b5b10-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5b10-165">Klicken Sie auf den Namen des Ausschnitts, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="b5b10-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="b5b10-166">Das Snippet wird im **Code-Editor**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b5b10-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="b5b10-167">Wählen Sie **Snippet ausführen** \ ( ![ Snippet ausführen ][ImageRunSnippetIcon] ) aus, oder wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="b5b10-167">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="b5b10-168">Ausführen eines Snippets mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="b5b10-168">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="b5b10-169">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="b5b10-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="b5b10-170">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-170">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5b10-171">Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="b5b10-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="b5b10-173">Ausführen eines Snippets über das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="b5b10-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5b10-174">Wählen Sie aus `Enter` , um den Ausschnitt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b5b10-174">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="b5b10-175">Umbenennen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b5b10-175">Rename Snippets</span></span>  

1.  <span data-ttu-id="b5b10-176">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="b5b10-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5b10-177">Klicken Sie mit der rechten Maustaste auf den Ausschnitt Namen, und wählen Sie **Umbenennen**aus.</span><span class="sxs-lookup"><span data-stu-id="b5b10-177">Right-click the Snippet name and choose **Rename**.</span></span>  
    
## <span data-ttu-id="b5b10-178">Löschen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b5b10-178">Delete Snippets</span></span>  

1.  <span data-ttu-id="b5b10-179">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="b5b10-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5b10-180">Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="b5b10-180">Right-click the Snippet name and choose **Remove**.</span></span>  
    
## <span data-ttu-id="b5b10-181">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="b5b10-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Übersicht über das Quellen Panel | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="b5b10-186">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5b10-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b5b10-187">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5b10-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b5b10-189">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5b10-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
