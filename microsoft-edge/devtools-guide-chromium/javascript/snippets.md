---
description: Codeausschnitte sind kleine Skripts, die Sie im Tool Sources von Microsoft Edge DevTools erstellen und ausführen können.  Sie können von jeder Webseite aus auf Ressourcen zugreifen und diese ausführen.  Wenn Sie einen Codeausschnitt ausführen, wird er aus dem Kontext der aktuell geöffneten Webseite ausgeführt.
title: Ausführen von Codeausschnitten von JavaScript auf jeder Webseite mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4a84e959f652320f40a501a26e9ba763c7348b33
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564112"
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
# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="f56bd-106">Ausführen von Codeausschnitten von JavaScript auf jeder Webseite mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f56bd-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f56bd-107">Wenn Sie denselben Code [][DevtoolsConsoleIndex] wiederholt in der Konsole ausführen, sollten Sie stattdessen den Code als Codeausschnitt speichern.</span><span class="sxs-lookup"><span data-stu-id="f56bd-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="f56bd-108">Codeausschnitte sind Skripts, die Sie im Tool [Quellen][DevToolsSourcesTool] erstellen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="f56bd-109">Codeausschnitte haben Zugriff auf den JavaScript-Kontext der Webseite, und Sie können Codeausschnitte auf jeder Beliebigen Webseite ausführen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="f56bd-110">Die Sicherheitseinstellungen der meisten Webseiten blockieren das Laden anderer Skripts in Codeausschnitten.</span><span class="sxs-lookup"><span data-stu-id="f56bd-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="f56bd-111">Aus diesem Grund müssen Sie den ganzen Code in einer Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="f56bd-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="f56bd-112">Codeausschnitte sind eine Alternative zu [Bookmarklets][WikiBookmarklet] mit dem Unterschied, dass Codeausschnitte nur in DevTools ausgeführt werden und nicht auf die zulässige Länge einer URL beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="f56bd-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="f56bd-113">Die Verwendung von Codeausschnitten ist eine hervorragende Möglichkeit, einige Dinge auf einer Webseite eines Drittanbieters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f56bd-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="f56bd-114">Codeänderungen in Codeausschnitten werden der aktuellen Webseite hinzugefügt und im gleichen Kontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f56bd-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="f56bd-115">Weitere Informationen zum Ändern des vorhandenen Codes einer Webseite finden Sie unter [Overrides][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="f56bd-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f56bd-116">In der folgenden Abbildung sind beispielsweise die DevTools-Homepage auf der linken Seite und ein Codeausschnitt auf der rechten Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f56bd-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Die vor dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="f56bd-118">Die Webseite vor dem Ausführen des Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="f56bd-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f56bd-119">Der Codeausschnitt von der Webseite vor dem Ausführen des Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="f56bd-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="f56bd-120">In der folgenden Abbildung wird die Webseite nach dem Ausführen des Codeausschnitts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f56bd-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="f56bd-121">Die **Konsolenschubschubte** wird angezeigt, um die Nachricht anzuzeigen, die der Codeausschnitt protokolliert, und der Inhalt der `Hello, Snippets!` Webseite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="f56bd-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Die Webseite nach dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="f56bd-123">Die Webseite nach dem Ausführen des Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="f56bd-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-tab"></a><span data-ttu-id="f56bd-124">Öffnen der Registerkarte Codeausschnitte</span><span class="sxs-lookup"><span data-stu-id="f56bd-124">Open the Snippets tab</span></span>  

<span data-ttu-id="f56bd-125">Auf **der Registerkarte Codeausschnitte** im **Bereich Navigator** auf der linken Seite werden Ihre Codeausschnitte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f56bd-125">The **Snippets** tab, in the **Navigator** pane on the left, lists your Snippets.</span></span>  <span data-ttu-id="f56bd-126">Wenn Sie einen Codeausschnitt bearbeiten möchten, müssen Sie ihn auf der Registerkarte **Codeausschnitte** öffnen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-126">When you want to edit a Snippet, you need to open it from the **Snippets** tab.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Registerkarte Codeausschnitte" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="f56bd-128">Registerkarte **Codeausschnitte**</span><span class="sxs-lookup"><span data-stu-id="f56bd-128">The **Snippets** tab</span></span>  
:::image-end:::  

### <a name="open-the-snippets-tab-with-a-mouse"></a><span data-ttu-id="f56bd-129">Öffnen der Registerkarte Codeausschnitte mit der Maus</span><span class="sxs-lookup"><span data-stu-id="f56bd-129">Open the Snippets tab with a mouse</span></span>  

1.  <span data-ttu-id="f56bd-130">Wählen Sie die **Registerkarte Quellen** aus.  Das **Tool Quellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f56bd-130">Choose the **Sources** tab.  The **Sources** tool appears.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Tool Quellen, auf dem die Registerkarte Seite links geöffnet ist" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="f56bd-132">Das **Tool Quellen,** auf dem die **Registerkarte Seite** links geöffnet ist</span><span class="sxs-lookup"><span data-stu-id="f56bd-132">The **Sources** tool with the **Page** tab open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f56bd-133">Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Codeausschnitte** aus.  Wenn Sie auf die **Option Codeausschnitte** zugreifen möchten, müssen Sie möglicherweise weitere **Registerkarten** \( ![ Weitere Registerkarten ](../media/more-tabs-icon.msft.png) \) auswählen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-133">In the **Navigator** pane (on the left), choose the **Snippets** tab.  To access the **Snippets** option, you may need to choose **More tabs** \(![More tabs](../media/more-tabs-icon.msft.png)\).</span></span>  
    
### <a name="open-the-snippets-tab-with-the-command-menu"></a><span data-ttu-id="f56bd-134">Öffnen Sie die Registerkarte Codeausschnitte mit dem Befehlsmenü.</span><span class="sxs-lookup"><span data-stu-id="f56bd-134">Open the Snippets tab with the Command Menu</span></span>  

1.  <span data-ttu-id="f56bd-135">Wählen Sie in DevTools alles aus, damit DevTools den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="f56bd-135">Select anything in DevTools, so that DevTools has focus.</span></span>  
1.  <span data-ttu-id="f56bd-136">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-136">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="f56bd-137">Geben `Snippets` Sie ein, **wählen Sie Codeausschnitte**anzeigen aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-137">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl Codeausschnitte anzeigen" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="f56bd-139">Der **Befehl Codeausschnitte** anzeigen</span><span class="sxs-lookup"><span data-stu-id="f56bd-139">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="f56bd-140">Erstellen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f56bd-140">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-tool"></a><span data-ttu-id="f56bd-141">Erstellen eines Codeausschnitts über das Tool Quellen</span><span class="sxs-lookup"><span data-stu-id="f56bd-141">Create a Snippet through the Sources tool</span></span>  

1.  <span data-ttu-id="f56bd-142">[Öffnen Sie die Registerkarte Codeausschnitte](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="f56bd-142">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="f56bd-143">Wählen **Sie Neuer Codeausschnitt aus.**</span><span class="sxs-lookup"><span data-stu-id="f56bd-143">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="f56bd-144">Geben Sie einen Namen für Ihren Codeausschnitt ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f56bd-144">Enter a name for your Snippet, and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Codeausschnitts" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="f56bd-146">Benennen eines Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="f56bd-146">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="f56bd-147">Erstellen eines Codeausschnitts über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="f56bd-147">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="f56bd-148">Fokussieren Sie den Cursor an einer stelle in DevTools.</span><span class="sxs-lookup"><span data-stu-id="f56bd-148">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="f56bd-149">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-149">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="f56bd-150">Geben `Snippet` Sie ein, wählen **Sie Neuen Codeausschnitt erstellen**aus, und wählen Sie dann `Enter` aus, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-150">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Codeausschnitts" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="f56bd-152">Der Befehl zum Erstellen eines neuen Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="f56bd-152">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f56bd-153">Um Ihren neuen Codeausschnitt mit einem benutzerdefinierten Namen umzubenennen, navigieren Sie zu [Umbenennen von Codeausschnitten](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="f56bd-153">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="f56bd-154">Bearbeiten von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f56bd-154">Edit Snippets</span></span>  

1.  <span data-ttu-id="f56bd-155">[Öffnen Sie die Registerkarte Codeausschnitte](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="f56bd-155">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="f56bd-156">Wählen Sie auf der Registerkarte Codeausschnitte den Namen des **Codeausschnitts** aus, den Sie bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="f56bd-156">In the **Snippets** tab, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="f56bd-157">Es wird im **Code-Editor geöffnet.**</span><span class="sxs-lookup"><span data-stu-id="f56bd-157">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="f56bd-159">Der **Code-Editor**</span><span class="sxs-lookup"><span data-stu-id="f56bd-159">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f56bd-160">Verwenden Sie **den Code-Editor,** um Ihrem Codeausschnitt JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-160">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="f56bd-161">Wenn neben dem Namen Ihres Codeausschnitts ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="f56bd-161">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="f56bd-162">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f56bd-162">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="f56bd-164">Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an.</span><span class="sxs-lookup"><span data-stu-id="f56bd-164">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="f56bd-165">Ausführen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f56bd-165">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-tool"></a><span data-ttu-id="f56bd-166">Ausführen eines Codeausschnitts aus dem Tool "Quellen"</span><span class="sxs-lookup"><span data-stu-id="f56bd-166">Run a Snippet from the Sources tool</span></span>  

1.  <span data-ttu-id="f56bd-167">[Öffnen Sie die Registerkarte Codeausschnitte](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="f56bd-167">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="f56bd-168">Wählen Sie den Namen des Codeausschnitts aus, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="f56bd-168">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="f56bd-169">Der Codeausschnitt wird im **Code-Editor geöffnet.**</span><span class="sxs-lookup"><span data-stu-id="f56bd-169">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="f56bd-170">Wählen **Sie Codeausschnitt** ausführen \( ![ Codeausschnitt ausführen ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f56bd-170">Choose **Run snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\).</span></span>
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="f56bd-171">Ausführen eines Codeausschnitts mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="f56bd-171">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="f56bd-172">Fokussieren Sie den Cursor an einer stelle in DevTools.</span><span class="sxs-lookup"><span data-stu-id="f56bd-172">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="f56bd-173">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f56bd-173">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="f56bd-174">Löschen Sie das Zeichen, und geben Sie das Zeichen gefolgt vom Namen des Codeausschnitts ein, `>` `!` den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="f56bd-174">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Codeausschnitts aus dem Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="f56bd-176">Ausführen eines Codeausschnitts aus dem **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="f56bd-176">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f56bd-177">Wählen `Enter` Sie diese Option aus, um den Codeausschnitt ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="f56bd-177">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="f56bd-178">Umbenennen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f56bd-178">Rename Snippets</span></span>  

1.  <span data-ttu-id="f56bd-179">[Öffnen Sie die Registerkarte Codeausschnitte](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="f56bd-179">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="f56bd-180">Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Umbenennen aus.**</span><span class="sxs-lookup"><span data-stu-id="f56bd-180">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="f56bd-181">Löschen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f56bd-181">Delete Snippets</span></span>  

1.  <span data-ttu-id="f56bd-182">[Öffnen Sie die Registerkarte Codeausschnitte](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="f56bd-182">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="f56bd-183">Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Entfernen aus.**</span><span class="sxs-lookup"><span data-stu-id="f56bd-183">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f56bd-184">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f56bd-184">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Konsolenübersicht | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Außerkraftsetzungen | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad-| MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-| Wikipedia"  

> [!NOTE]
> <span data-ttu-id="f56bd-190">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f56bd-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f56bd-191">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="f56bd-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f56bd-193">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f56bd-193">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
