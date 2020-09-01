---
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982007"
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





# <span data-ttu-id="4c0cc-103">Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4c0cc-103">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="4c0cc-104">Wenn Sie feststellen, dass derselbe Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausgeführt wird, sollten Sie stattdessen den Code als Snippet speichern.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="4c0cc-105">Ausschnitte sind Skripts, die Sie im [Quellen][DevToolsSourcesPanel] Panel erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-105">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="4c0cc-106">Sie haben Zugriff auf den JavaScript-Kontext der Seite, und Sie können Sie auf einer beliebigen Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="4c0cc-107">Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="4c0cc-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="4c0cc-108">Firefox devtools verfügt über ein ähnliches Feature wie Snippets mit [dem Namen "][MDNScratchpad]Zwischenablage".</span><span class="sxs-lookup"><span data-stu-id="4c0cc-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="4c0cc-109">In der folgenden Abbildung ist beispielsweise die devtools-Homepage auf der linken Seite und ein Codeausschnitt Quellcode auf der rechten Seite zu sehen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-109">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="4c0cc-111">Aussehen der Seite vor dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="4c0cc-111">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="4c0cc-112">Der Snippet-Quellcode aus der vorhergehenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-112">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="4c0cc-113">In der folgenden Abbildung wird die Seite nach dem Ausführen des Snippets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-113">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="4c0cc-114">Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Seite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-114">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aussehen der Seite nach dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="4c0cc-116">Aussehen der Seite nach dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="4c0cc-116">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="4c0cc-117">Öffnen des Bereichs "Snippets"</span><span class="sxs-lookup"><span data-stu-id="4c0cc-117">Open the Snippets pane</span></span>   

<span data-ttu-id="4c0cc-118">Im Bereich **Snippets** werden Ihre Snippets aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-118">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="4c0cc-119">Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-119">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Der Bereich "Ausschnitte"" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="4c0cc-121">Der Bereich " **Ausschnitte** "</span><span class="sxs-lookup"><span data-stu-id="4c0cc-121">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="4c0cc-122">Öffnen des Bereichs "Ausschnitte" mit einer Maus</span><span class="sxs-lookup"><span data-stu-id="4c0cc-122">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="4c0cc-123">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-123">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="4c0cc-124">Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-124">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Fenster "Quellen" mit geöffnetem Seitenbereich auf der linken Seite" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="4c0cc-126">Das Fenster " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**</span><span class="sxs-lookup"><span data-stu-id="4c0cc-126">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4c0cc-127">Klicken Sie auf die Registerkarte **Snippets** , um den Bereich **Snippets** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-127">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="4c0cc-128">Möglicherweise müssen Sie auf **weitere Registerkarten** \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \) klicken, um auf die Option **Snippets** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-128">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="4c0cc-129">Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="4c0cc-129">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="4c0cc-130">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-130">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4c0cc-131">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-131">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4c0cc-132">Beginnen `Snippets` Sie mit der Eingabe, wählen Sie **Snippets anzeigen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-132">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl ' Snippets anzeigen '" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="4c0cc-134">Der Befehl ' **Snippets anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="4c0cc-134">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4c0cc-135">Erstellen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="4c0cc-135">Create Snippets</span></span>   

### <span data-ttu-id="4c0cc-136">Erstellen eines Snippets über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="4c0cc-136">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="4c0cc-137">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-137">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4c0cc-138">Klicken Sie auf **neuer Ausschnitt**.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-138">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="4c0cc-139">Geben Sie einen Namen für das Snippet ein, und drücken Sie `Enter` zum Speichern.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-139">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Snippets" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="4c0cc-141">Benennen eines Snippets</span><span class="sxs-lookup"><span data-stu-id="4c0cc-141">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4c0cc-142">Erstellen eines Snippets über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="4c0cc-142">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="4c0cc-143">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-143">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4c0cc-144">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-144">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4c0cc-145">Beginnen `Snippet` Sie mit der Eingabe, wählen Sie **Neues Snippet erstellen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-145">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Snippets" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="4c0cc-147">Der Befehl zum Erstellen eines neuen Snippets</span><span class="sxs-lookup"><span data-stu-id="4c0cc-147">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4c0cc-148">Weitere Informationen finden Sie unter [Umbenennen von Snippets](#rename-snippets) , wenn Sie Ihrem neuen Snippet einen benutzerdefinierten Namen zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-148">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="4c0cc-149">Bearbeiten von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="4c0cc-149">Edit Snippets</span></span>   

1.  <span data-ttu-id="4c0cc-150">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-150">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4c0cc-151">Klicken Sie im Bereich **Snippets** auf den Namen des Ausschnitts, den Sie bearbeiten möchten, um ihn im **Code-Editor**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-151">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="4c0cc-153">Der **Code-Editor**</span><span class="sxs-lookup"><span data-stu-id="4c0cc-153">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4c0cc-154">Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-154">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="4c0cc-155">Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-155">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="4c0cc-156">Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-156">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="4c0cc-158">Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt</span><span class="sxs-lookup"><span data-stu-id="4c0cc-158">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4c0cc-159">Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="4c0cc-159">Run Snippets</span></span>   

### <span data-ttu-id="4c0cc-160">Ausführen eines Snippets im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="4c0cc-160">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="4c0cc-161">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-161">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4c0cc-162">Klicken Sie auf den Namen des Ausschnitts, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-162">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="4c0cc-163">Das Snippet wird im **Code-Editor**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-163">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="4c0cc-164">Klicken Sie auf **Snippet ausführen** \ ( ![ Snippet ausführen ][ImageRunSnippetIcon] ), oder drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-164">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="4c0cc-165">Ausführen eines Snippets mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="4c0cc-165">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="4c0cc-166">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-166">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="4c0cc-167">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-167">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4c0cc-168">Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-168">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Snippets über das Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="4c0cc-170">Ausführen eines Snippets über das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="4c0cc-170">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4c0cc-171">Drücken Sie `Enter` zum Ausführen des Snippets.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-171">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="4c0cc-172">Umbenennen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="4c0cc-172">Rename Snippets</span></span>   

1.  <span data-ttu-id="4c0cc-173">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-173">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4c0cc-174">Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Umbenennen**aus.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-174">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="4c0cc-175">Löschen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="4c0cc-175">Delete Snippets</span></span>   

1.  <span data-ttu-id="4c0cc-176">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="4c0cc-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="4c0cc-177">Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-177">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Übersicht über das Quellen Panel | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="4c0cc-182">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4c0cc-183">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4c0cc-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4c0cc-185">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c0cc-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
