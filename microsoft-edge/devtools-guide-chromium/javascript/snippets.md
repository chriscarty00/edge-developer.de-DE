---
description: Codeausschnitte sind kleine Skripts, die Sie im Tool Sources von Microsoft Edge DevTools erstellen und ausführen können.  Sie können von jeder Webseite aus auf Ressourcen zugreifen und diese ausführen.  Wenn Sie einen Codeausschnitt ausführen, wird er aus dem Kontext der aktuell geöffneten Webseite ausgeführt.
title: Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439423"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="ee89e-106">Ausführen von Codeausschnitten von JavaScript auf einer beliebigen Webseite mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee89e-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ee89e-107">Wenn Sie denselben Code [][DevtoolsConsoleIndex] wiederholt in der Konsole ausführen, sollten Sie stattdessen den Code als Codeausschnitt speichern.</span><span class="sxs-lookup"><span data-stu-id="ee89e-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="ee89e-108">Codeausschnitte sind Skripts, die Sie im Tool [Quellen][DevToolsSourcesTool] erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="ee89e-109">Codeausschnitte haben Zugriff auf den JavaScript-Kontext der Webseite, und Sie können Codeausschnitte auf jeder Beliebigen Webseite ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="ee89e-110">Die Sicherheitseinstellungen der meisten Webseiten blockieren das Laden anderer Skripts in Codeausschnitten.</span><span class="sxs-lookup"><span data-stu-id="ee89e-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="ee89e-111">Aus diesem Grund müssen Sie den ganzen Code in einer Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="ee89e-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="ee89e-112">Codeausschnitte sind eine Alternative zu [Bookmarklets][WikiBookmarklet] mit dem Unterschied, dass Codeausschnitte nur in DevTools ausgeführt werden und nicht auf die zulässige Länge einer URL beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="ee89e-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="ee89e-113">Die Verwendung von Codeausschnitten ist eine hervorragende Möglichkeit, einige Dinge auf einer Webseite eines Drittanbieters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ee89e-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="ee89e-114">Codeänderungen in Codeausschnitten werden der aktuellen Webseite hinzugefügt und im gleichen Kontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee89e-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="ee89e-115">Weitere Informationen zum Ändern des vorhandenen Codes einer Webseite finden Sie unter [Overrides][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="ee89e-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ee89e-116">In der folgenden Abbildung sind beispielsweise die DevTools-Homepage auf der linken Seite und ein Codeausschnitt auf der rechten Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ee89e-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Die vor dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="ee89e-118">Die Webseite vor dem Ausführen des Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="ee89e-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ee89e-119">Der Codeausschnitt von der Webseite vor dem Ausführen des Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="ee89e-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ee89e-120">In der folgenden Abbildung wird die Webseite nach dem Ausführen des Codeausschnitts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee89e-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="ee89e-121">Die **Konsolenschubschubte** wird angezeigt, um die Nachricht anzuzeigen, die der Codeausschnitt protokolliert, und der Inhalt der `Hello, Snippets!` Webseite ändert sich vollständig.</span><span class="sxs-lookup"><span data-stu-id="ee89e-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Die Webseite nach dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="ee89e-123">Die Webseite nach dem Ausführen des Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="ee89e-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-pane"></a><span data-ttu-id="ee89e-124">Öffnen des Codeausschnittbereichs</span><span class="sxs-lookup"><span data-stu-id="ee89e-124">Open the Snippets pane</span></span>  

<span data-ttu-id="ee89e-125">Im **Bereich Codeausschnitte** werden Ihre Codeausschnitte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ee89e-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="ee89e-126">Wenn Sie einen Codeausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Codeausschnitte** öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Der Bereich Codeausschnitte" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="ee89e-128">Der **Bereich Codeausschnitte**</span><span class="sxs-lookup"><span data-stu-id="ee89e-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a><span data-ttu-id="ee89e-129">Öffnen des Codeausschnittbereichs mit der Maus</span><span class="sxs-lookup"><span data-stu-id="ee89e-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="ee89e-130">Wählen Sie die **Registerkarte Quellen** aus, um das Tool **Quellen zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="ee89e-131">Der **Seitenbereich** wird in der Regel standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ee89e-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Tool Quellen mit links geöffneten Seitenbereich" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="ee89e-133">Das **Tool Quellen** mit links geöffneten Seitenbereich </span><span class="sxs-lookup"><span data-stu-id="ee89e-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee89e-134">Wählen Sie die **Registerkarte Codeausschnitte** aus, um den **Codeausschnittbereich zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="ee89e-135">Möglicherweise müssen Sie weitere **Registerkarten** \( Weitere Registerkarten \) auswählen, um ![ auf die Option ](../media/more-tabs-icon.msft.png) **Codeausschnitte zu** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-135">You may need to choose **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) to access the **Snippets** option.</span></span>  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a><span data-ttu-id="ee89e-136">Öffnen Sie den Codeausschnittbereich mit dem Befehlsmenü.</span><span class="sxs-lookup"><span data-stu-id="ee89e-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="ee89e-137">Fokussieren Sie den Cursor an einer stelle in DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee89e-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="ee89e-138">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ee89e-139">Geben `Snippets` Sie ein, **wählen Sie Codeausschnitte**anzeigen aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl Codeausschnitte anzeigen" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="ee89e-141">Der **Befehl Codeausschnitte** anzeigen</span><span class="sxs-lookup"><span data-stu-id="ee89e-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="ee89e-142">Erstellen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="ee89e-142">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-panel"></a><span data-ttu-id="ee89e-143">Erstellen eines Codeausschnitts über den Bereich Quellen</span><span class="sxs-lookup"><span data-stu-id="ee89e-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="ee89e-144">[Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ee89e-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ee89e-145">Wählen **Sie Neuer Codeausschnitt aus.**</span><span class="sxs-lookup"><span data-stu-id="ee89e-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="ee89e-146">Geben Sie einen Namen für Ihren Codeausschnitt ein, und wählen Sie dann `Enter` zum Speichern aus.</span><span class="sxs-lookup"><span data-stu-id="ee89e-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Codeausschnitts" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="ee89e-148">Benennen eines Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="ee89e-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="ee89e-149">Erstellen eines Codeausschnitts über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="ee89e-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="ee89e-150">Fokussieren Sie den Cursor an einer stelle in DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee89e-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="ee89e-151">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ee89e-152">Geben `Snippet` Sie ein, wählen **Sie Neuen Codeausschnitt erstellen**aus, und wählen Sie dann `Enter` aus, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Codeausschnitts" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="ee89e-154">Der Befehl zum Erstellen eines neuen Codeausschnitts</span><span class="sxs-lookup"><span data-stu-id="ee89e-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ee89e-155">Um Ihren neuen Codeausschnitt mit einem benutzerdefinierten Namen umzubenennen, navigieren Sie zu [Umbenennen von Codeausschnitten](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="ee89e-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="ee89e-156">Bearbeiten von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="ee89e-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="ee89e-157">[Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ee89e-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ee89e-158">Wählen Sie im Bereich Codeausschnitte den Namen des **Codeausschnitts** aus, den Sie bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="ee89e-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="ee89e-159">Es wird im **Code-Editor geöffnet.**</span><span class="sxs-lookup"><span data-stu-id="ee89e-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="ee89e-161">Der **Code-Editor**</span><span class="sxs-lookup"><span data-stu-id="ee89e-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee89e-162">Verwenden Sie **den Code-Editor,** um Ihrem Codeausschnitt JavaScript hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="ee89e-163">Wenn neben dem Namen Ihres Codeausschnitts ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.</span><span class="sxs-lookup"><span data-stu-id="ee89e-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="ee89e-164">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ee89e-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="ee89e-166">Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an.</span><span class="sxs-lookup"><span data-stu-id="ee89e-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="ee89e-167">Ausführen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="ee89e-167">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-panel"></a><span data-ttu-id="ee89e-168">Ausführen eines Codeausschnitts im Bereich Quellen</span><span class="sxs-lookup"><span data-stu-id="ee89e-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="ee89e-169">[Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ee89e-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ee89e-170">Wählen Sie den Namen des Codeausschnitts aus, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="ee89e-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="ee89e-171">Der Codeausschnitt wird im **Code-Editor geöffnet.**</span><span class="sxs-lookup"><span data-stu-id="ee89e-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="ee89e-172">Wählen **Sie Codeausschnitt** ausführen \( ![ Codeausschnitt ausführen ](../media/run-snippet-icon.msft.png) \) oder `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ee89e-172">Choose **Run Snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="ee89e-173">Ausführen eines Codeausschnitts mit dem Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="ee89e-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="ee89e-174">Fokussieren Sie den Cursor an einer stelle in DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee89e-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="ee89e-175">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee89e-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ee89e-176">Löschen Sie das Zeichen, und geben Sie das Zeichen gefolgt vom Namen des Codeausschnitts ein, `>` `!` den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="ee89e-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Codeausschnitts aus dem Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="ee89e-178">Ausführen eines Codeausschnitts aus dem **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="ee89e-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee89e-179">Wählen `Enter` Sie diese Option aus, um den Codeausschnitt ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ee89e-179">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="ee89e-180">Umbenennen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="ee89e-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="ee89e-181">[Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ee89e-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ee89e-182">Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Umbenennen aus.**</span><span class="sxs-lookup"><span data-stu-id="ee89e-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="ee89e-183">Löschen von Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="ee89e-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="ee89e-184">[Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ee89e-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ee89e-185">Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Entfernen aus.**</span><span class="sxs-lookup"><span data-stu-id="ee89e-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ee89e-186">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ee89e-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Konsolenübersicht | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Außerkraftsetzungen | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad-| MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-| Wikipedia"  

> [!NOTE]
> <span data-ttu-id="ee89e-192">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee89e-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ee89e-193">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="ee89e-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ee89e-195">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee89e-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
