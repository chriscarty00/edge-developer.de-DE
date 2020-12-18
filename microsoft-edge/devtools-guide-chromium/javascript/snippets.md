---
description: Snippets sind kleine Skripts, die Sie im Quellen Tool von Microsoft Edge devtools erstellen und ausführen können.  Sie können auf jeder beliebigen Webseite auf Ressourcen zugreifen und diese ausführen.  Wenn Sie einen Ausschnitt ausführen, wird er im Kontext der aktuell geöffneten Webseite ausgeführt.
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230957"
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

# <span data-ttu-id="31899-106">Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Webseite mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="31899-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="31899-107">Wenn Sie denselben Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausführen, sollten Sie stattdessen den Code als Snippet speichern.</span><span class="sxs-lookup"><span data-stu-id="31899-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="31899-108">Ausschnitte sind Skripts, die Sie im [Quellen][DevToolsSourcesTool] Tool erstellen.</span><span class="sxs-lookup"><span data-stu-id="31899-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="31899-109">Snippets haben Zugriff auf den JavaScript-Kontext der Webseite, und Sie können Ausschnitte auf einer beliebigen Webseite ausführen.</span><span class="sxs-lookup"><span data-stu-id="31899-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="31899-110">Die Sicherheitseinstellungen der meisten Webseiten blockieren das Laden anderer Skripts in Ausschnitten.</span><span class="sxs-lookup"><span data-stu-id="31899-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="31899-111">Aus diesem Grund müssen Sie den gesamten Code in eine Datei aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="31899-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="31899-112">Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet] mit dem Unterschied, dass Ausschnitte nur in devtools ausgeführt werden und nicht auf die zulässige Länge einer URL begrenzt sind.</span><span class="sxs-lookup"><span data-stu-id="31899-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="31899-113">Die Verwendung von Snippets ist eine hervorragende Möglichkeit, ein paar Dinge auf einer Drittanbieter-Webseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="31899-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="31899-114">Code Änderungen in Ausschnitten werden der aktuellen Webseite hinzugefügt und im gleichen Kontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31899-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="31899-115">Weitere Informationen zum Ändern des vorhandenen Codes einer Webseite finden Sie unter [Außerkraftsetzungen][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="31899-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="31899-116">In der folgenden Abbildung ist beispielsweise die devtools-Homepage auf der linken Seite und ein Codeausschnitt Quellcode auf der rechten Seite zu sehen.</span><span class="sxs-lookup"><span data-stu-id="31899-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Die vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="31899-118">Die Webseite vor dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="31899-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="31899-119">Der Snippet-Quellcode auf der Webseite, bevor der Codeausschnitt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31899-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="31899-120">In der folgenden Abbildung wird die Webseite nach dem Ausführen des Snippets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31899-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="31899-121">Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Webseite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="31899-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Die Webseite nach dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="31899-123">Die Webseite nach dem Ausführen des Snippets</span><span class="sxs-lookup"><span data-stu-id="31899-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="31899-124">Öffnen des Bereichs "Snippets"</span><span class="sxs-lookup"><span data-stu-id="31899-124">Open the Snippets pane</span></span>  

<span data-ttu-id="31899-125">Im Bereich **Snippets** werden Ihre Snippets aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="31899-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="31899-126">Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Der Bereich "Ausschnitte"" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="31899-128">Der Bereich " **Ausschnitte** "</span><span class="sxs-lookup"><span data-stu-id="31899-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="31899-129">Öffnen des Bereichs "Ausschnitte" mit einer Maus</span><span class="sxs-lookup"><span data-stu-id="31899-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="31899-130">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Tool zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="31899-131">Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="31899-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Tool "Quellen" mit geöffnetem Seitenbereich auf der linken Seite" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="31899-133">Das Tool " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**</span><span class="sxs-lookup"><span data-stu-id="31899-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31899-134">Wählen Sie die Registerkarte **Snippets** aus, um den Bereich **Snippets** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="31899-135">Möglicherweise müssen Sie **weitere Registerkarten** auswählen \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \), um auf die Option **Snippets** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="31899-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="31899-136">Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="31899-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="31899-137">Setzen Sie den Cursor an eine beliebige Stelle in devtools.</span><span class="sxs-lookup"><span data-stu-id="31899-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="31899-138">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="31899-139">Geben `Snippets` Sie **Snippets anzeigen**ein, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="31899-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl ' Snippets anzeigen '" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="31899-141">Der Befehl ' **Snippets anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="31899-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31899-142">Erstellen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="31899-142">Create Snippets</span></span>  

### <span data-ttu-id="31899-143">Erstellen eines Snippets über das Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="31899-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="31899-144">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="31899-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="31899-145">Wählen Sie **Neues Snippet**aus.</span><span class="sxs-lookup"><span data-stu-id="31899-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="31899-146">Geben Sie einen Namen für das Snippet ein, und wählen Sie dann `Enter` Speichern aus.</span><span class="sxs-lookup"><span data-stu-id="31899-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Snippets" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="31899-148">Benennen eines Snippets</span><span class="sxs-lookup"><span data-stu-id="31899-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="31899-149">Erstellen eines Snippets über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="31899-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="31899-150">Setzen Sie den Cursor an eine beliebige Stelle in devtools.</span><span class="sxs-lookup"><span data-stu-id="31899-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="31899-151">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="31899-152">Geben `Snippet` Sie ein, wählen Sie **Neues Snippet erstellen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="31899-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Snippets" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="31899-154">Der Befehl zum Erstellen eines neuen Snippets</span><span class="sxs-lookup"><span data-stu-id="31899-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="31899-155">Wenn Sie den neuen Ausschnitt mit einem benutzerdefinierten Namen umbenennen möchten, navigieren Sie zu [Snippets umbenennen](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="31899-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="31899-156">Bearbeiten von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="31899-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="31899-157">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="31899-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="31899-158">Wählen Sie im Bereich **Snippets** den Namen des Ausschnitts aus, den Sie bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="31899-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="31899-159">Sie wird im **Code-Editor**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="31899-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="31899-161">Der **Code-Editor**</span><span class="sxs-lookup"><span data-stu-id="31899-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31899-162">Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="31899-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="31899-163">Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="31899-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="31899-164">Wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="31899-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Namen des Ausschnitts zeigt nicht gespeicherten Code an." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="31899-166">Ein Sternchen neben dem Namen des Ausschnitts zeigt nicht gespeicherten Code an.</span><span class="sxs-lookup"><span data-stu-id="31899-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31899-167">Ausführen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="31899-167">Run Snippets</span></span>  

### <span data-ttu-id="31899-168">Ausführen eines Snippets im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="31899-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="31899-169">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="31899-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="31899-170">Wählen Sie den Namen des Ausschnitts aus, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="31899-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="31899-171">Das Snippet wird im **Code-Editor**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="31899-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="31899-172">Wählen Sie **Snippet ausführen** \ ( ![ Snippet ausführen ][ImageRunSnippetIcon] ) aus, oder wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="31899-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="31899-173">Ausführen eines Snippets mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="31899-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="31899-174">Setzen Sie den Cursor an eine beliebige Stelle in devtools.</span><span class="sxs-lookup"><span data-stu-id="31899-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="31899-175">Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="31899-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="31899-176">Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="31899-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Snippets über das Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="31899-178">Ausführen eines Snippets über das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="31899-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31899-179">Wählen Sie aus `Enter` , um den Ausschnitt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="31899-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="31899-180">Umbenennen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="31899-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="31899-181">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="31899-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="31899-182">Zeigen Sie auf den Namen des Snippets, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Umbenennen**aus.</span><span class="sxs-lookup"><span data-stu-id="31899-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="31899-183">Löschen von Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="31899-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="31899-184">[Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="31899-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="31899-185">Zeigen Sie auf den Namen des Snippets, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="31899-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="31899-186">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="31899-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das Quellen Tool | Microsoft docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Außerkraftsetzungen | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> <span data-ttu-id="31899-192">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31899-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="31899-193">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="31899-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="31899-195">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31899-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
