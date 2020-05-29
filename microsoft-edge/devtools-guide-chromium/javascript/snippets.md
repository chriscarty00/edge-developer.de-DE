---
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581817"
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





# <span data-ttu-id="c2b54-103">Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="c2b54-103">Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c2b54-104">Wenn Sie feststellen, dass derselbe Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausgeführt wird, sollten Sie stattdessen den Code als Snippet speichern.</span><span class="sxs-lookup"><span data-stu-id="c2b54-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="c2b54-105">Ausschnitte sind Skripts, die Sie im [ **Quellen** Panel][DevToolsSourcesPanel]erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-105">Snippets are scripts that you author in the [**Sources** panel][DevToolsSourcesPanel].</span></span>  <span data-ttu-id="c2b54-106">Sie haben Zugriff auf den JavaScript-Kontext der Seite, und Sie können Sie auf einer beliebigen Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="c2b54-107">Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="c2b54-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="c2b54-108">Firefox devtools verfügt über ein ähnliches Feature wie Snippets mit [dem Namen "][MDNScratchpad]Zwischenablage".</span><span class="sxs-lookup"><span data-stu-id="c2b54-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="c2b54-109">[**Abbildung 1**](#figure-1) zeigt beispielsweise die devtools-Homepage auf der linken Seite und einen Snippet-Quellcode auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="c2b54-109">For example, [**Figure 1**](#figure-1) shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

> ##### <span data-ttu-id="c2b54-110">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="c2b54-110">Figure 1</span></span>  
> <span data-ttu-id="c2b54-111">Aussehen der Seite vor dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="c2b54-111">How the page looks before running the Snippet</span></span>  
> ![Aussehen der Seite vor dem Ausführen des Snippets][ImageSnippetSplitScreen]  

<span data-ttu-id="c2b54-113">Der Snippet-Quellcode aus [**Abbildung 1**](#figure-1):</span><span class="sxs-lookup"><span data-stu-id="c2b54-113">The Snippet source code from [**Figure 1**](#figure-1):</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="c2b54-114">[**Abbildung 2**](#figure-2) zeigt, wie die Seite nach der Ausführung des Snippets aussieht.</span><span class="sxs-lookup"><span data-stu-id="c2b54-114">[**Figure 2**](#figure-2) shows how the page looks after running the Snippet.</span></span>  <span data-ttu-id="c2b54-115">Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Seite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="c2b54-115">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

> ##### <span data-ttu-id="c2b54-116">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="c2b54-116">Figure 2</span></span>  
> <span data-ttu-id="c2b54-117">Aussehen der Seite nach dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="c2b54-117">How the page looks after running the Snippet</span></span>  
> ![Aussehen der Seite nach dem Ausführen des Snippets][ImageSnippetSplitScreenAfter]  

## <span data-ttu-id="c2b54-119">Öffnen des Bereichs "Snippets"</span><span class="sxs-lookup"><span data-stu-id="c2b54-119">Open the Snippets pane</span></span>   

<span data-ttu-id="c2b54-120">Im Bereich **Snippets** werden Ihre Snippets aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c2b54-120">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="c2b54-121">Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-121">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

> ##### <span data-ttu-id="c2b54-122">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="c2b54-122">Figure 3</span></span>  
> <span data-ttu-id="c2b54-123">Der Bereich " **Ausschnitte** "</span><span class="sxs-lookup"><span data-stu-id="c2b54-123">The **Snippets** pane</span></span>  
> ![Der Bereich "Ausschnitte"][ImageSnippetsPane]  

### <span data-ttu-id="c2b54-125">Öffnen des Bereichs "Ausschnitte" mit einer Maus</span><span class="sxs-lookup"><span data-stu-id="c2b54-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="c2b54-126">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="c2b54-127">Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c2b54-127">The **Page** pane usually opens by default.</span></span>  

    > ##### <span data-ttu-id="c2b54-128">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="c2b54-128">Figure 4</span></span>  
    > <span data-ttu-id="c2b54-129">Das Fenster " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**</span><span class="sxs-lookup"><span data-stu-id="c2b54-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    > ![Das Fenster "Quellen" mit geöffnetem Seitenbereich auf der linken Seite][ImageSourcesPageEmpty]  

1.  <span data-ttu-id="c2b54-131">Klicken Sie auf die Registerkarte **Snippets** , um den Bereich **Snippets** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-131">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="c2b54-132">Möglicherweise müssen Sie auf **Weitere** Registerkarten weitere Registerkarten klicken, um auf ![ ][ImageMoreTabsIcon] die Option **Snippets** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-132">You might need to click **More Tabs** ![More Tabs][ImageMoreTabsIcon] in order to access the **Snippets** option.</span></span>  

### <span data-ttu-id="c2b54-133">Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="c2b54-133">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="c2b54-134">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="c2b54-134">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="c2b54-135">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-135">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c2b54-136">Beginnen `Snippets` Sie mit der Eingabe, wählen Sie **Snippets anzeigen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-136">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="c2b54-137">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="c2b54-137">Figure 5</span></span>  
    > <span data-ttu-id="c2b54-138">Der Befehl ' **Snippets anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="c2b54-138">The **Show Snippets** command</span></span>  
    > ![Der Befehl ' Snippets anzeigen '][ImageShowSnippetsSearch]  

## <span data-ttu-id="c2b54-140">Erstellen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c2b54-140">Create Snippets</span></span>   

### <span data-ttu-id="c2b54-141">Erstellen eines Snippets über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="c2b54-141">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="c2b54-142">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c2b54-142">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c2b54-143">Klicken Sie auf **neuer Ausschnitt**.</span><span class="sxs-lookup"><span data-stu-id="c2b54-143">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="c2b54-144">Geben Sie einen Namen für das Snippet ein, und drücken Sie `Enter` zum Speichern.</span><span class="sxs-lookup"><span data-stu-id="c2b54-144">Enter a name for your Snippet then press `Enter` to save.</span></span>  

    > ##### <span data-ttu-id="c2b54-145">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="c2b54-145">Figure 6</span></span>  
    > <span data-ttu-id="c2b54-146">Benennen eines Snippets</span><span class="sxs-lookup"><span data-stu-id="c2b54-146">Naming a Snippet</span></span>  
    > ![Benennen eines Snippets][ImageSnippetName]  

### <span data-ttu-id="c2b54-148">Erstellen eines Snippets über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="c2b54-148">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="c2b54-149">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="c2b54-149">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="c2b54-150">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-150">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c2b54-151">Beginnen `Snippet` Sie mit der Eingabe, wählen Sie **Neues Snippet erstellen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-151">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="c2b54-152">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="c2b54-152">Figure 7</span></span>  
    > <span data-ttu-id="c2b54-153">Der Befehl zum Erstellen eines neuen Snippets</span><span class="sxs-lookup"><span data-stu-id="c2b54-153">The command for creating a new Snippet</span></span>  
    > ![Der Befehl zum Erstellen eines neuen Snippets][ImageCreateSnippetSearch]  

<span data-ttu-id="c2b54-155">Weitere Informationen finden Sie unter [Umbenennen von Snippets](#rename-snippets) , wenn Sie Ihrem neuen Snippet einen benutzerdefinierten Namen zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2b54-155">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="c2b54-156">Bearbeiten von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c2b54-156">Edit Snippets</span></span>   

1.  <span data-ttu-id="c2b54-157">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c2b54-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c2b54-158">Klicken Sie im Bereich **Snippets** auf den Namen des Ausschnitts, den Sie bearbeiten möchten, um ihn im **Code-Editor**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-158">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  

    > ##### <span data-ttu-id="c2b54-159">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="c2b54-159">Figure 8</span></span>  
    > <span data-ttu-id="c2b54-160">Der Code-Editor</span><span class="sxs-lookup"><span data-stu-id="c2b54-160">The Code Editor</span></span>  
    > ![Der Code-Editor][ImageSnippetEditor]  

1.  <span data-ttu-id="c2b54-162">Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="c2b54-163">Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="c2b54-163">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="c2b54-164">Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c2b54-164">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  

    > ##### <span data-ttu-id="c2b54-165">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="c2b54-165">Figure 9</span></span>  
    > <span data-ttu-id="c2b54-166">Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt</span><span class="sxs-lookup"><span data-stu-id="c2b54-166">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    > ![Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt][ImageUnsavedSnippet]  

## <span data-ttu-id="c2b54-168">Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c2b54-168">Run Snippets</span></span>   

### <span data-ttu-id="c2b54-169">Ausführen eines Snippets im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="c2b54-169">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="c2b54-170">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c2b54-170">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c2b54-171">Klicken Sie auf den Namen des Ausschnitts, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2b54-171">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="c2b54-172">Das Snippet wird im **Code-Editor**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c2b54-172">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="c2b54-173">Klicken Sie auf **Snippet** ![ Run Snippet ausführen ][ImageRunSnippetIcon] , oder drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c2b54-173">Click **Run Snippet** ![Run Snippet][ImageRunSnippetIcon], or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  

### <span data-ttu-id="c2b54-174">Ausführen eines Snippets mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="c2b54-174">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="c2b54-175">Setzen Sie den Cursor an eine beliebige Stelle in der devtools.</span><span class="sxs-lookup"><span data-stu-id="c2b54-175">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="c2b54-176">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2b54-176">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c2b54-177">Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2b54-177">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  

    > ##### <span data-ttu-id="c2b54-178">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="c2b54-178">Figure 10</span></span>  
    > <span data-ttu-id="c2b54-179">Ausführen eines Snippets über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="c2b54-179">Running a Snippet from the Command Menu</span></span>  
    > ![Ausführen eines Snippets über das Befehlsmenü][ImageRunSnippetCommand]  

1.  <span data-ttu-id="c2b54-181">Drücken Sie `Enter` zum Ausführen des Snippets.</span><span class="sxs-lookup"><span data-stu-id="c2b54-181">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="c2b54-182">Umbenennen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c2b54-182">Rename Snippets</span></span>   

1.  <span data-ttu-id="c2b54-183">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c2b54-183">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c2b54-184">Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Umbenennen**aus.</span><span class="sxs-lookup"><span data-stu-id="c2b54-184">Right-click the Snippet name and select **Rename**.</span></span>  

## <span data-ttu-id="c2b54-185">Löschen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="c2b54-185">Delete Snippets</span></span>   

1.  <span data-ttu-id="c2b54-186">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c2b54-186">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c2b54-187">Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="c2b54-187">Right-click the Snippet name and select **Remove**.</span></span>  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Abbildung 1: Aussehen der Seite vor dem Ausführen des Snippets"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Abbildung 2: Aussehen der Seite nach dem Ausführen des Snippets"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Abbildung 3: der Bereich "Ausschnitte""  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Abbildung 4: das Fenster "Quellen" mit geöffnetem Seitenbereich auf der linken Seite"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Abbildung 5: Befehl ' Snippets anzeigen '"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Abbildung 6: Benennen eines Snippets"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Abbildung 7: der Befehl zum Erstellen eines neuen Snippets"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Abbildung 8: der Code-Editor"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Abbildung 9: ein Sternchen neben dem Ausschnitt Namen, der nicht gespeicherten Code angibt"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Abbildung 10: Ausführen eines Snippets über das Befehlsmenü"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole"  
[DevToolsSourcesPanel]: ../sources.md "Übersicht über das Quellen Panel"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="c2b54-202">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2b54-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c2b54-203">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2b54-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="c2b54-205">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2b54-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
