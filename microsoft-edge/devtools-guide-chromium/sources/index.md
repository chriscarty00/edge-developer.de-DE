---
description: Verwenden Sie das Tool Sources, um JavaScript anzuzeigen, zu ändern und zu debuggen, das vom Server zurückgegeben wird, und um die Ressourcen zu überprüfen, aus der die aktuelle Webseite ist.  Um das Tool Sources als Entwicklungsumgebung zu verwenden, fügen Sie einem Arbeitsbereich Quelldateien hinzu.
title: Übersicht über das Tool „Quellen“
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6ba6a7615c2d9e2b70975af01edeeb3e10db8e59
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579743"
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
# <a name="sources-tool-overview"></a><span data-ttu-id="aedbe-105">Übersicht über das Tool „Quellen“</span><span class="sxs-lookup"><span data-stu-id="aedbe-105">Sources tool overview</span></span>  

<span data-ttu-id="aedbe-106">Verwenden Sie **das Sources-Tool,** um Front-End-JavaScript-Code anzuzeigen, zu ändern und zu debuggen und die Ressourcen zu überprüfen, die die aktuelle Webseite enthalten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-106">Use the **Sources** tool to view, modify, and debug front-end JavaScript code, and to inspect the resources that make up the current webpage.</span></span>  <span data-ttu-id="aedbe-107">Das **Tool Sources** verfügt über drei Bereiche:</span><span class="sxs-lookup"><span data-stu-id="aedbe-107">The **Sources** tool has three panes:</span></span>  

| <span data-ttu-id="aedbe-108">Bereich</span><span class="sxs-lookup"><span data-stu-id="aedbe-108">Pane</span></span> | <span data-ttu-id="aedbe-109">Aktionen</span><span class="sxs-lookup"><span data-stu-id="aedbe-109">Actions</span></span> |
|---|---|
| <span data-ttu-id="aedbe-110">**Navigatorbereich**</span><span class="sxs-lookup"><span data-stu-id="aedbe-110">**Navigator** pane</span></span> | <span data-ttu-id="aedbe-111">Navigieren Sie zwischen den Ressourcen, die vom Server zurückgegeben werden, um die aktuelle Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-111">Navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="aedbe-112">Wählen Sie Dateien, Bilder und andere Ressourcen aus, und zeigen Sie ihre Pfade an.</span><span class="sxs-lookup"><span data-stu-id="aedbe-112">Select files, images, and other resources, and view their paths.</span></span>  <span data-ttu-id="aedbe-113">Richten Sie optional einen lokalen Arbeitsbereich ein, um Änderungen direkt in Quelldateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="aedbe-113">Optionally, set up a local Workspace to save changes directly to source files.</span></span> |
| <span data-ttu-id="aedbe-114">**Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="aedbe-114">**Editor** pane</span></span> | <span data-ttu-id="aedbe-115">Zeigen Sie JavaScript, HTML, CSS und andere Dateien an, die vom Server zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-115">View JavaScript, HTML, CSS, and other files that are returned from the server.</span></span>  <span data-ttu-id="aedbe-116">Nehmen Sie experimentelle Bearbeitungen an JavaScript oder CSS vor.</span><span class="sxs-lookup"><span data-stu-id="aedbe-116">Make experimental edits to JavaScript or CSS.</span></span>  <span data-ttu-id="aedbe-117">Ihre Änderungen werden beibehalten, bis Sie die Seite aktualisieren oder nach der Seitenaktualisierung beibehalten werden, wenn Sie in einer lokalen Datei mit Arbeitsbereichen speichern.</span><span class="sxs-lookup"><span data-stu-id="aedbe-117">Your changes are preserved until you refresh the page, or are preserved after page refresh if you save to a local file with Workspaces.</span></span> <span data-ttu-id="aedbe-118">Wenn Sie Arbeitsbereiche oder Außerkraftsetzungen verwenden, können Sie auch HTML-Dateien bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-118">When you use Workspaces or Overrides, you can edit HTML files as well.</span></span> |
| <span data-ttu-id="aedbe-119">**Debuggerbereich**</span><span class="sxs-lookup"><span data-stu-id="aedbe-119">**Debugger** pane</span></span> | <span data-ttu-id="aedbe-120">Verwenden Sie den JavaScript-Debugger, um Haltepunkte festzulegen, die Ausführung von JavaScript anzuhalten und den Code einschließlich der von Ihnen vorgenommenen Änderungen zu durchbrechen, während Sie die angegebenen JavaScript-Ausdrücke ansehen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-120">Use the JavaScript Debugger to set breakpoints, pause running JavaScript, and step through the code, including any edits you have made, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="aedbe-121">Beobachten und manuell ändern Sie die Werte von Variablen, die sich im Bereich der aktuellen Codezeile befinden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-121">Watch and manually change the values of variables that are in-scope for the current line of code.</span></span> |

<span data-ttu-id="aedbe-122">Die folgende Abbildung zeigt den **Navigatorbereich,** der mit einem roten Feld in der linken oberen Ecke von DevTools hervorgehoben ist, den Editorbereich oben rechts und den **Debuggerbereich** unten hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-122">The following figure shows the **Navigator** pane highlighted with a red box in the upper left corner of DevTools, the **Editor** pane highlighted in the upper right, and the **Debugger** pane highlighted on the bottom.</span></span>  <span data-ttu-id="aedbe-123">Ganz links ist der Hauptteil des Browserfensters, in dem die gerenderte Webseite abgeblendet angezeigt wird, da der Debugger an einem Haltepunkt angehalten wird:</span><span class="sxs-lookup"><span data-stu-id="aedbe-123">On the far left side is the main part of the browser window, showing the rendered webpage grayed-out because the debugger is paused on a breakpoint:</span></span>

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Die Bereiche des Tools Quellen im schmalen Layout" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   <span data-ttu-id="aedbe-125">Die Bereiche des Tools "Quellen" im schmalen Layout</span><span class="sxs-lookup"><span data-stu-id="aedbe-125">The panes of the Sources tool, in narrow layout</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-126">Wenn DevTools breit ist, wird der **Debuggerbereich** rechts platziert und umfasst **Scope** und **Watch**:</span><span class="sxs-lookup"><span data-stu-id="aedbe-126">When DevTools is wide, the **Debugger** pane is placed on the right, and includes **Scope** and **Watch**:</span></span>  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Vom Server zurückgegebenes JavaScript navigieren, anzeigen, bearbeiten und debuggen" lightbox="../media/sources-panes-wide-layout.msft.png":::
   <span data-ttu-id="aedbe-128">Vom Server zurückgegebenes JavaScript navigieren, anzeigen, bearbeiten und debuggen</span><span class="sxs-lookup"><span data-stu-id="aedbe-128">Navigate, view, edit, and debug JavaScript returned by the server</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-129">Um die Größe des Sources-Tools zu maximieren, entfernen Sie DevTools in ein separates Fenster, und verschieben Sie optional das DevTools-Fenster auf einen separaten Monitor.</span><span class="sxs-lookup"><span data-stu-id="aedbe-129">To maximize the size of the Sources tool, undock DevTools into a separate window, and optionally move the DevTools window to a separate monitor.</span></span>  <span data-ttu-id="aedbe-130">Siehe [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="aedbe-130">See [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span></span>

<span data-ttu-id="aedbe-131">Informationen zum Laden der oben gezeigten Debugdemowebseite finden Sie unter Der grundlegende Ansatz für die Verwendung [eines Debuggers](#the-basic-approach-to-using-a-debugger)weiter unten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-131">To load the debugging demo webpage that's shown above, see [The basic approach to using a debugger](#the-basic-approach-to-using-a-debugger), below.</span></span>

## <a name="using-the-navigator-pane-to-select-files"></a><span data-ttu-id="aedbe-132">Verwenden des Navigatorbereichs zum Auswählen von Dateien</span><span class="sxs-lookup"><span data-stu-id="aedbe-132">Using the Navigator pane to select files</span></span>

<span data-ttu-id="aedbe-133">Verwenden Sie **den Navigatorbereich** (links), um zwischen den Ressourcen zu navigieren, die vom Server zurückgegeben werden, um die aktuelle Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-133">Use the **Navigator** pane (on the left) to navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="aedbe-134">Wählen Sie Dateien, Bilder und andere Ressourcen aus, und zeigen Sie ihre Pfade an.</span><span class="sxs-lookup"><span data-stu-id="aedbe-134">Select files, images, and other resources, and view their paths.</span></span>  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Der Bereich Navigator" lightbox="../media/navigator-pane.msft.png":::
   <span data-ttu-id="aedbe-136">Der **Bereich Navigator**</span><span class="sxs-lookup"><span data-stu-id="aedbe-136">The **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-137">Um auf alle ausgeblendeten Registerkarten des Navigatorbereichs zu zugreifen, wählen Sie ![ Weitere Registerkarten ](../media/more-tabs-icon.msft.png) ( Weitere Registerkarten )**aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-137">To access any hidden tabs of the Navigator pane, select ![More tabs](../media/more-tabs-icon.msft.png) (**More tabs**).</span></span>

<span data-ttu-id="aedbe-138">Die folgenden Unterabschnitte umfassen den Navigatorbereich:</span><span class="sxs-lookup"><span data-stu-id="aedbe-138">The following subsections cover the Navigator pane:</span></span>
*   [<span data-ttu-id="aedbe-139">Verwenden der Registerkarte Seite zum Erkunden von Ressourcen, die die aktuelle Webseite erstellen</span><span class="sxs-lookup"><span data-stu-id="aedbe-139">Using the Page tab to explore resources that construct the current webpage</span></span>](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)
*   [<span data-ttu-id="aedbe-140">Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="aedbe-140">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="aedbe-141">Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien</span><span class="sxs-lookup"><span data-stu-id="aedbe-141">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
*   [<span data-ttu-id="aedbe-142">Verwenden der Registerkarte Inhaltsskripts für Microsoft Edge Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="aedbe-142">Using the Content scripts tab for Microsoft Edge extensions</span></span>](#using-the-content-scripts-tab-for-microsoft-edge-extensions)
*   [<span data-ttu-id="aedbe-143">Verwenden der Registerkarte Codeausschnitte zum Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite</span><span class="sxs-lookup"><span data-stu-id="aedbe-143">Using the Snippets tab to run JavaScript code snippets on any page</span></span>](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)
*   [<span data-ttu-id="aedbe-144">Öffnen von Dateien mithilfe des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="aedbe-144">Using the Command Menu to open files</span></span>](#using-the-command-menu-to-open-files)

### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a><span data-ttu-id="aedbe-145">Verwenden der Registerkarte Seite zum Erkunden von Ressourcen, die die aktuelle Webseite erstellen</span><span class="sxs-lookup"><span data-stu-id="aedbe-145">Using the Page tab to explore resources that construct the current webpage</span></span>

<span data-ttu-id="aedbe-146">Verwenden Sie **die Registerkarte Seite** des **Navigatorbereichs,** um das dateisystem zu erkunden, das vom Server zurückgegeben wird, um die aktuelle Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-146">Use the **Page** tab of the **Navigator** pane to explore the file system that's returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="aedbe-147">Wählen Sie eine JavaScript-Datei zum Anzeigen, Bearbeiten und Debuggen aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-147">Select a JavaScript file to view, edit, and debug it.</span></span>  <span data-ttu-id="aedbe-148">Auf **der Registerkarte** Seite werden alle Ressourcen aufgeführt, die die Seite geladen hat.</span><span class="sxs-lookup"><span data-stu-id="aedbe-148">The **Page** tab lists all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="Die Registerkarte Seite im Navigatorbereich des Tools Quellen" lightbox="../media/sources-page-tab.msft.png":::
   <span data-ttu-id="aedbe-150">Die **Registerkarte Seite** im **Navigatorbereich** des **Tools Quellen**</span><span class="sxs-lookup"><span data-stu-id="aedbe-150">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-151">Wählen Sie auf der Registerkarte Seite eine Datei aus, um eine Datei im Editorbereich **anzuzeigen.**  Für ein Bild wird eine Vorschau des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-151">To display a file in the **Editor** pane, select a file in the **Page** tab.  For an image, a preview of the image is displayed.</span></span>  

<span data-ttu-id="aedbe-152">Zeigen Sie zum Anzeigen der URL oder des Pfads für eine Ressource auf die Ressource.</span><span class="sxs-lookup"><span data-stu-id="aedbe-152">To display the URL or path for a resource, hover over the resource.</span></span>

<span data-ttu-id="aedbe-153">Zum Laden einer Datei in eine neue Registerkarte des Browsers oder zum Anzeigen anderer Aktionen klicken Sie mit der rechten Maustaste auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-153">To load a file into a new tab of the browser, or to display other actions, right-click on the file name.</span></span>
   
#### <a name="icons-in-the-page-tab"></a><span data-ttu-id="aedbe-154">Symbole auf der Registerkarte Seite</span><span class="sxs-lookup"><span data-stu-id="aedbe-154">Icons in the Page tab</span></span>

<span data-ttu-id="aedbe-155">Auf **der Registerkarte** Seite werden die folgenden Symbole verwendet:</span><span class="sxs-lookup"><span data-stu-id="aedbe-155">The **Page** tab uses the following icons:</span></span>
*   <span data-ttu-id="aedbe-156">Das **Fenstersymbol** stellt zusammen mit der Bezeichnung den `top` Hauptdokumentrahmen dar, bei dem es sich um einen [HTML-Frame handelt.][W3CHtml4Frames]</span><span class="sxs-lookup"><span data-stu-id="aedbe-156">The **window** icon, along with the label `top`, represents the main document frame, which is an [HTML frame][W3CHtml4Frames].</span></span>  
*   <span data-ttu-id="aedbe-157">Das **Cloudsymbol** stellt einen [Ursprung dar.][HtmlstandardOrigin]</span><span class="sxs-lookup"><span data-stu-id="aedbe-157">The **cloud** icon represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="aedbe-158">Das **Ordnersymbol** stellt ein Verzeichnis dar.</span><span class="sxs-lookup"><span data-stu-id="aedbe-158">The **folder** icon represents a directory.</span></span>
*   <span data-ttu-id="aedbe-159">Das **Seitensymbol** stellt eine Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="aedbe-159">The **page** icon represents a resource.</span></span>  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a><span data-ttu-id="aedbe-160">Gruppieren von Dateien nach Ordnern oder als flache Liste</span><span class="sxs-lookup"><span data-stu-id="aedbe-160">Group files by folder or as a flat list</span></span>

<span data-ttu-id="aedbe-161">Auf **der Registerkarte** Seite werden Dateien oder Ressourcen nach Server und Verzeichnis oder als flache Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-161">The **Page** tab displays files or resources grouped by server and directory, or as a flat list.</span></span>

<span data-ttu-id="aedbe-162">So ändern Sie die Gruppierung von Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-162">To change how resources are grouped:</span></span>

1.  <span data-ttu-id="aedbe-163">Wählen Sie neben den Registerkarten im Navigatorbereich (links) die **Schaltfläche ...** (**Weitere Optionen**) aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-163">Next to the tabs on the Navigator pane (on the left), select the **...** (**More options**) button.</span></span>  <span data-ttu-id="aedbe-164">Es wird ein Menü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-164">A menu appears.</span></span>
1.  <span data-ttu-id="aedbe-165">Wählen Sie die Option **Gruppe nach Ordner aus, oder** deaktivieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="aedbe-165">Select or clear the **Group by folder** option.</span></span>  

### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a><span data-ttu-id="aedbe-166">Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="aedbe-166">Using the Filesystem tab to define a local Workspace</span></span>

<span data-ttu-id="aedbe-167">Verwenden Sie **die Registerkarte Dateisystem** des **Navigatorbereichs,** um Einem Arbeitsbereich Dateien hinzuzufügen, sodass Änderungen, die Sie in DevTools vornehmen, in Ihrem lokalen Dateisystem gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-167">Use the **Filesystem** tab of the **Navigator** pane to add files to a Workspace, so that changes you make in DevTools get saved to your local file system.</span></span>

<span data-ttu-id="aedbe-168">Eine Datei, die sich in einem Arbeitsbereich befindet, wird in devTools durch einen grünen Punkt neben dem Dateinamen gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="aedbe-168">A file that's in a Workspace is indicated by a green dot next to the file name, throughout DevTools.</span></span> 

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Die Registerkarte Dateisystem für einen Arbeitsbereich" lightbox="../media/sources-filesystem-tab.msft.png":::
   <span data-ttu-id="aedbe-170">Die **Registerkarte Dateisystem** für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="aedbe-170">The **Filesystem** tab, for a Workspace</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-171">Wenn Sie eine Datei im Tool Quellen bearbeiten, werden Ihre Änderungen standardmäßig verworfen, wenn Sie die Webseite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aedbe-171">By default, when you edit a file in the **Sources** tool, your changes are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="aedbe-172">Das **Tool Sources** arbeitet mit einer Kopie der Front-End-Ressourcen, die vom Webserver zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-172">The **Sources** tool works with a copy of the front-end resources that are returned by the web server.</span></span>  <span data-ttu-id="aedbe-173">Wenn Sie diese vom Server zurückgegebenen Front-End-Dateien ändern, werden die Änderungen nicht beibehalten, da Sie die Quelldateien nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-173">When you modify these front-end files that are returned by the server, the changes don't persist, because you didn't change the source files.</span></span>  <span data-ttu-id="aedbe-174">Sie müssen ihre Bearbeitungen auch im tatsächlichen Quellcode anwenden und dann erneut auf dem Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-174">You need to also apply your edits in your actual source code, and then re-deploy to the server.</span></span>

<span data-ttu-id="aedbe-175">Wenn Sie hingegen einen Arbeitsbereich verwenden, werden Änderungen, die Sie an Ihrem Front-End-Code vornehmen, beim Aktualisieren der Webseite beibehalten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-175">In contrast, when you use a Workspace, changes that you make to your front-end code are preserved when you refresh the webpage.</span></span>  <span data-ttu-id="aedbe-176">Wenn Sie mit einem Arbeitsbereich den vom Server zurückgegebenen Front-End-Code bearbeiten, wendet das Tool Quellen ihre Bearbeitungen auch auf den lokalen Quellcode an.</span><span class="sxs-lookup"><span data-stu-id="aedbe-176">With a Workspace, when you edit the front-end code that's returned by the server, the Sources tool also applies your edits to your local source code.</span></span>  <span data-ttu-id="aedbe-177">Damit andere Benutzer Ihre Änderungen sehen können, müssen Sie nur die geänderten Quelldateien erneut auf dem Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-177">Then for other users to see your changes, you only need to redeploy your changed source files to the server.</span></span>

<span data-ttu-id="aedbe-178">Arbeitsbereiche funktionieren gut, wenn der vom Server zurückgegebene JavaScript-Code mit dem lokalen JavaScript-Quellcode identisch ist.</span><span class="sxs-lookup"><span data-stu-id="aedbe-178">Workspaces work well when the JavaScript code that's returned by the server is the same as your local JavaScript source code.</span></span>  <span data-ttu-id="aedbe-179">Arbeitsbereiche funktionieren nicht so gut, wenn Ihr Workflow Transformationen im Quellcode umfasst, z. B. Verminung oder [TypeScript-Kompilierung.][TypescriptlangMain]</span><span class="sxs-lookup"><span data-stu-id="aedbe-179">Workspaces don't work as well when your workflow involves transformations on your source code, such as minification or [TypeScript][TypescriptlangMain] compilation.</span></span>  

<span data-ttu-id="aedbe-180">Weitere Informationen finden Sie im Lernprogramm [Dateien mit Arbeitsbereichen bearbeiten.][DevtoolsGuideChromiumWorkspacesIndex]</span><span class="sxs-lookup"><span data-stu-id="aedbe-180">For more information, see the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a><span data-ttu-id="aedbe-181">Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien</span><span class="sxs-lookup"><span data-stu-id="aedbe-181">Using the Overrides tab to override server files with local files</span></span>

<span data-ttu-id="aedbe-182">Verwenden Sie die Registerkarte Außerkraftsetzungen des **Navigatorbereichs,** um Seitenressourcen (z. B. Bilder) mit Dateien aus einem lokalen Ordner zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-182">Use the **Overrides** tab of the **Navigator** pane to override page assets (such as images) with files from a local folder.</span></span>

<span data-ttu-id="aedbe-183">Elemente auf dieser Registerkarte überschreiben, was der Server an den Browser sendet, auch nachdem der Server die Objekte gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="aedbe-183">Items in this tab override what the server sends to the browser, even after the server has sent the assets.</span></span>  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="Die Registerkarte Außerkraftsetzungen des Navigatorbereichs" lightbox="../media/overrides-tab.msft.png":::
   <span data-ttu-id="aedbe-185">Die **Registerkarte Außerkraftsetzungen** des **Navigatorbereichs**</span><span class="sxs-lookup"><span data-stu-id="aedbe-185">The **Overrides** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-186">Das **Overrides-Feature** ähnelt Arbeitsbereichen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-186">The **Overrides** feature is similar to Workspaces.</span></span>  <span data-ttu-id="aedbe-187">Verwenden Sie Außerkraftsetzungen, wenn Sie mit Änderungen an einer Webseite experimentieren möchten, und Sie müssen die Änderungen nach dem Aktualisieren der Webseite behalten. Es ist Ihnen jedoch nicht egal, ob Sie Ihre Änderungen dem Quellcode der Webseite zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-187">Use Overrides when you want to experiment with changes to a webpage, and you need to keep the changes after you refresh the webpage, but you don't care about mapping your changes to the source code of the webpage.</span></span>  

<span data-ttu-id="aedbe-188">Eine Datei, die eine datei überschreibt, die vom Server zurückgegeben wird, wird durch einen lila Punkt neben dem Dateinamen in devTools angegeben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-188">A file that overrides a file that is returned by the server is indicated by a purple dot next to the file name, throughout DevTools.</span></span>

#### <a name="see-also"></a><span data-ttu-id="aedbe-189">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-189">See also</span></span>

*   [<span data-ttu-id="aedbe-190">Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aedbe-190">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>][DevtoolsJavascriptOverrides]

*   [<span data-ttu-id="aedbe-191">Zuordnung von vorverarbeiteten Code zu Quellcode</span><span class="sxs-lookup"><span data-stu-id="aedbe-191">Map preprocessed code to source code</span></span>][DevToolsJavaScriptSourceMaps]

### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a><span data-ttu-id="aedbe-192">Verwenden der Registerkarte Inhaltsskripts für Microsoft Edge Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="aedbe-192">Using the Content scripts tab for Microsoft Edge extensions</span></span>

<span data-ttu-id="aedbe-193">Verwenden Sie **die Registerkarte Inhaltsskripts** im **Navigatorbereich,** um alle Inhaltsskripts anzuzeigen, die von einer installierten Microsoft Edge geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-193">Use the **Content scripts** tab of the **Navigator** pane to view any content scripts that were loaded by a Microsoft Edge extension that you installed.</span></span> 

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="Die Registerkarte Inhaltsskripts im Navigatorbereich" lightbox="../media/content-scripts-tab.msft.png":::
   <span data-ttu-id="aedbe-195">Die **Registerkarte Inhaltsskripts** im **Navigatorbereich**</span><span class="sxs-lookup"><span data-stu-id="aedbe-195">The **Content scripts** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-196">Wenn der Debugger codeschritte, den Sie nicht erkennen, möchten Sie diesen Code möglicherweise als Bibliothekscode markieren, um einen Schritt in diesen Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-196">When the debugger steps into code that you don't recognize, you might want to mark that code as Library code, to avoid stepping into that code.</span></span>  <span data-ttu-id="aedbe-197">Weitere [Informationen finden Sie unter Markieren von Inhaltsskripts als Bibliothekscode][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span><span class="sxs-lookup"><span data-stu-id="aedbe-197">See [Mark content scripts as Library code][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span></span>

#### <a name="see-also"></a><span data-ttu-id="aedbe-198">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-198">See also</span></span>

*   [<span data-ttu-id="aedbe-199">Inhaltsskripts</span><span class="sxs-lookup"><span data-stu-id="aedbe-199">Content scripts</span></span>][MDNContentScripts]
*   [<span data-ttu-id="aedbe-200">Erstellen eines Erweiterungslernprogramms Teil 2</span><span class="sxs-lookup"><span data-stu-id="aedbe-200">Create an extension tutorial Part 2</span></span>][ExtensionsChromiumGetstartPart2ContentScripts]

### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a><span data-ttu-id="aedbe-201">Verwenden der Registerkarte Codeausschnitte zum Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Webseite</span><span class="sxs-lookup"><span data-stu-id="aedbe-201">Using the Snippets tab to run JavaScript code snippets on any webpage</span></span>

<span data-ttu-id="aedbe-202">Verwenden Sie **die Registerkarte** Codeausschnitte des **Navigatorbereichs,** um JavaScript-Codeausschnitte zu erstellen und zu speichern, sodass Sie diese Codeausschnitte problemlos auf jeder Webseite ausführen können.</span><span class="sxs-lookup"><span data-stu-id="aedbe-202">Use the **Snippets** tab of the **Navigator** pane to create and save JavaScript code snippets, so that you can easily run these snippets on any webpage.</span></span>

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Codeausschnitt, der die jQuery-Bibliothek in eine Webseite einfüge" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="aedbe-204">Ein Codeausschnitt, der die jQuery-Bibliothek in eine Webseite einfüge</span><span class="sxs-lookup"><span data-stu-id="aedbe-204">A Snippet that inserts the jQuery library into a webpage</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-205">Angenommen, Sie geben häufig den folgenden Code in die Konsole **ein,** um die jQuery-Bibliothek in eine Seite zu einfügen, damit Sie jQuery-Befehle über die Konsole **ausführen können:**</span><span class="sxs-lookup"><span data-stu-id="aedbe-205">For example, suppose you frequently enter the following code in the **Console**, to insert the jQuery library into a page so that you can run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="aedbe-206">Stattdessen können Sie diesen Code in einem Codeausschnitt **speichern** und dann bei Bedarf problemlos ausführen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-206">Instead, you can save this code in a **Snippet** and then easily run it whenever you need to.</span></span>  <span data-ttu-id="aedbe-207">Wenn Sie `Ctrl` + `S` \(Windows/Linux\) oder `Command` + `S` \(macOS\) auswählen, speichert DevTools den Codeausschnitt in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="aedbe-207">When you select `Ctrl`+`S` \(Windows/Linux\) or `Command`+`S` \(macOS\), DevTools saves the **Snippet** to your file system.</span></span>  

<span data-ttu-id="aedbe-208">Es gibt mehrere Möglichkeiten zum Ausführen eines Codeausschnitts:</span><span class="sxs-lookup"><span data-stu-id="aedbe-208">There are multiple ways to run a Snippet:</span></span>
*   <span data-ttu-id="aedbe-209">Wählen Sie **im Bereich Navigator** die Registerkarte **Codeausschnitte** aus, und wählen Sie dann die Codeausschnittdatei aus, um sie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-209">In the **Navigator** pane, select the **Snippets** tab, and then select the snippets file to open it.</span></span>  <span data-ttu-id="aedbe-210">Wählen Sie dann unten im Editorbereich **Ausführen** \( ![ Die Schaltfläche Ausführen ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="aedbe-210">Then at the bottom of the Editor pane, select **Run** \(![The Run button](../media/run-snippet-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="aedbe-211">Wenn DevTools den Fokus hat, wählen Sie `Ctrl` + `P` \(Windows/Linux\) oder `Command` + `P` \(macOS\) [][DevToolsCommandMenuIndex]aus, um das Befehlsmenü zu öffnen, und geben Sie dann `!` ein.</span><span class="sxs-lookup"><span data-stu-id="aedbe-211">When DevTools has focus, select `Ctrl`+`P` \(Windows/Linux\) or `Command`+`P` \(macOS\) to open the [Command Menu][DevToolsCommandMenuIndex], and then type `!`.</span></span> 

<span data-ttu-id="aedbe-212">Codeausschnitte ähneln Bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="aedbe-212">Snippets are similar to bookmarklets.</span></span>

#### <a name="see-also"></a><span data-ttu-id="aedbe-213">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-213">See also</span></span>

*   [<span data-ttu-id="aedbe-214">Ausführen von Codeausschnitten von JavaScript auf jeder Webseite mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aedbe-214">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>][DevtoolsGuideChromiumJavascriptSnippets]

### <a name="using-the-command-menu-to-open-files"></a><span data-ttu-id="aedbe-215">Öffnen von Dateien mithilfe des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="aedbe-215">Using the Command Menu to open files</span></span>

<span data-ttu-id="aedbe-216">Zum Öffnen einer Datei können Sie neben der Verwendung des **Navigatorbereichs** im Tool Quellen das Befehlsmenü von überall in DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-216">To open a file, in addition to using the **Navigator** pane within the **Sources** tool, you can use the Command Menu from anywhere within DevTools.</span></span>

*   <span data-ttu-id="aedbe-217">Wählen Sie an beliebiger Stelle in DevTools `Ctrl` + `P` auf Windows/Linux oder `Command` + `P` auf macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-217">From anywhere in DevTools, select `Ctrl`+`P` on Windows/Linux or `Command`+`P` on macOS.</span></span>  <span data-ttu-id="aedbe-218">Das Befehlsmenü wird angezeigt und listet alle Ressourcen auf, die sich auf den Registerkarten des **Navigatorbereichs** des **Tools Quellen** befinden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-218">The Command Menu appears, and lists all the resources that are in the tabs of the **Navigator** pane of the **Sources** tool.</span></span>  
*   <span data-ttu-id="aedbe-219">Oder wählen Sie neben den Registerkarten des **Navigatorbereichs** im Tool Quellen die **Schaltfläche ...** (**Weitere**Optionen ) aus, und wählen Sie dann Datei **öffnen aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-219">Or, next to the tabs of the **Navigator** pane in the **Sources** tool, select the **...** (**More options**) button, and then select **Open File**.</span></span>  

<span data-ttu-id="aedbe-220">Geben Sie zum Anzeigen und Auswählen aus einer Liste aller .js `.js` ein.</span><span class="sxs-lookup"><span data-stu-id="aedbe-220">To display and pick from a list of all .js files, type `.js`.</span></span>

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Öffnen einer Datei mithilfe des Befehlsmenüs" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   <span data-ttu-id="aedbe-222">Öffnen einer Datei mithilfe des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="aedbe-222">Opening a file by using the Command Menu</span></span>
:::image-end:::

<span data-ttu-id="aedbe-223">Wenn Sie `?` eingeben, werden im Befehlsmenü mehrere Befehle angezeigt, darunter **... Öffnen Sie die Datei**.</span><span class="sxs-lookup"><span data-stu-id="aedbe-223">If you type `?`, the Command Menu shows several commands, including **... Open file**.</span></span>  <span data-ttu-id="aedbe-224">Wenn Sie das `Backspace` Befehlsmenü löschen möchten, wird eine Liste der Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-224">If you select `Backspace` to clear the Command Menu, a list of files is shown.</span></span>

<span data-ttu-id="aedbe-225">Weitere Informationen finden Sie unter [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="aedbe-225">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

## <a name="using-the-editor-pane-to-view-or-edit-files"></a><span data-ttu-id="aedbe-226">Verwenden des Editorbereichs zum Anzeigen oder Bearbeiten von Dateien</span><span class="sxs-lookup"><span data-stu-id="aedbe-226">Using the Editor pane to view or edit files</span></span>

<span data-ttu-id="aedbe-227">Verwenden Sie den **Editorbereich,** um die front-end-Dateien anzuzeigen, die vom Server zurückgegeben werden, um die aktuelle Webseite zu verfassen, einschließlich JavaScript, HTML, CSS und Bilddateien.</span><span class="sxs-lookup"><span data-stu-id="aedbe-227">Use the **Editor** pane to view the front-end files that are returned from the server to compose the current webpage, including JavaScript, HTML, CSS, and image files.</span></span>  <span data-ttu-id="aedbe-228">Wenn Sie die Front-End-Dateien im **Editorbereich bearbeiten,** aktualisiert DevTools die Webseite, um den geänderten Code ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="aedbe-228">When you edit the front-end files in the **Editor** pane, DevTools updates the webpage to run the modified code.</span></span>  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="Der Editorbereich im Tool Quellen" lightbox="../media/editor-pane.msft.png":::
   <span data-ttu-id="aedbe-230">Der **Editorbereich** im **Tool Quellen**</span><span class="sxs-lookup"><span data-stu-id="aedbe-230">The **Editor** pane in the **Sources** tool</span></span>  
:::image-end:::

<span data-ttu-id="aedbe-231">Der **Editorbereich** bietet die folgende Unterstützungsebene für verschiedene Dateitypen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-231">The **Editor** pane has the following level of support for various file types:</span></span>

| <span data-ttu-id="aedbe-232">Dateityp</span><span class="sxs-lookup"><span data-stu-id="aedbe-232">File Type</span></span> | <span data-ttu-id="aedbe-233">Unterstützte Aktionen</span><span class="sxs-lookup"><span data-stu-id="aedbe-233">Supported Actions</span></span> |
|---|---|
| <span data-ttu-id="aedbe-234">JavaScript</span><span class="sxs-lookup"><span data-stu-id="aedbe-234">JavaScript</span></span> | <span data-ttu-id="aedbe-235">Anzeigen, Bearbeiten und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-235">View, edit, and debug.</span></span> |
| <span data-ttu-id="aedbe-236">CSS</span><span class="sxs-lookup"><span data-stu-id="aedbe-236">CSS</span></span> | <span data-ttu-id="aedbe-237">Anzeigen und Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-237">View and edit.</span></span> |
| <span data-ttu-id="aedbe-238">HTML</span><span class="sxs-lookup"><span data-stu-id="aedbe-238">HTML</span></span> | <span data-ttu-id="aedbe-239">Anzeigen und Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-239">View and edit.</span></span> |
| <span data-ttu-id="aedbe-240">Images</span><span class="sxs-lookup"><span data-stu-id="aedbe-240">Images</span></span> | <span data-ttu-id="aedbe-241">„Ansicht“ aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-241">View.</span></span> |

<span data-ttu-id="aedbe-242">Standardmäßig werden Bearbeitungen verworfen, wenn Sie die Webseite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aedbe-242">By default, edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="aedbe-243">Informationen zum Speichern der Änderungen an Ihrem Dateisystem finden Sie unter Verwenden der Registerkarte Dateisystem zum Definieren eines [lokalen Arbeitsbereichs](#using-the-filesystem-tab-to-define-a-local-workspace)oben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-243">For information about how to save the changes to your file system, see [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.</span></span>

<span data-ttu-id="aedbe-244">Die folgenden Unterabschnitte umfassen den Editorbereich:</span><span class="sxs-lookup"><span data-stu-id="aedbe-244">The following subsections cover the Editor pane:</span></span>
*   [<span data-ttu-id="aedbe-245">Bearbeiten einer JavaScript-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-245">Editing a JavaScript file</span></span>](#editing-a-javascript-file)
*   [<span data-ttu-id="aedbe-246">Neuformatieren einer minifizierten JavaScript-Datei mit Hübschdruck</span><span class="sxs-lookup"><span data-stu-id="aedbe-246">Reformatting a minified JavaScript file with pretty-print</span></span>](#reformatting-a-minified-javascript-file-with-pretty-print)
*   [<span data-ttu-id="aedbe-247">Zuordnen von minifizierten Code zu Ihrem Quellcode zum Anzeigen lesbaren Codes</span><span class="sxs-lookup"><span data-stu-id="aedbe-247">Mapping minified code to your source code to show readable code</span></span>](#mapping-minified-code-to-your-source-code-to-show-readable-code)
*   [<span data-ttu-id="aedbe-248">Transformationen vom Quellcode in kompilierten Front-End-Code</span><span class="sxs-lookup"><span data-stu-id="aedbe-248">Transformations from source code to compiled front-end code</span></span>](#transformations-from-source-code-to-compiled-front-end-code)
*   [<span data-ttu-id="aedbe-249">Bearbeiten einer CSS-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-249">Editing a CSS file</span></span>](#editing-a-css-file)
*   [<span data-ttu-id="aedbe-250">Bearbeiten einer HTML-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-250">Editing an HTML file</span></span>](#editing-an-html-file)
*   [<span data-ttu-id="aedbe-251">Zu einer Zeilennummer oder Funktion</span><span class="sxs-lookup"><span data-stu-id="aedbe-251">Going to a line number or function</span></span>](#going-to-a-line-number-or-function)
*   [<span data-ttu-id="aedbe-252">Anzeigen von Quelldateien bei Verwendung eines anderen Tools</span><span class="sxs-lookup"><span data-stu-id="aedbe-252">Displaying source files when using a different tool</span></span>](#displaying-source-files-when-using-a-different-tool)

### <a name="editing-a-javascript-file"></a><span data-ttu-id="aedbe-253">Bearbeiten einer JavaScript-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-253">Editing a JavaScript file</span></span>

<span data-ttu-id="aedbe-254">Um eine JavaScript-Datei in DevTools zu bearbeiten, verwenden Sie den **Editorbereich** im **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-254">To edit a JavaScript file in DevTools, use the **Editor** pane, within the **Sources** tool.</span></span>

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Bearbeiten von JavaScript im Editorbereich" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   <span data-ttu-id="aedbe-256">Bearbeiten von JavaScript im **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="aedbe-256">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::

<span data-ttu-id="aedbe-257">Um eine Datei in den Editorbereich zu laden, verwenden Sie die Registerkarte **Seite** im **Navigatorbereich** (links).</span><span class="sxs-lookup"><span data-stu-id="aedbe-257">To load a file into the Editor pane, use the **Page** tab in the **Navigator** pane (on the left).</span></span>  <span data-ttu-id="aedbe-258">Oder verwenden Sie das **Befehlsmenü**wie folgt: Wählen Sie oben rechts von DevTools die Option **DevTools** anpassen und steuern \( \) aus, und wählen Sie dann `...` Datei öffnen **aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-258">Or use the **Command Menu**, as follows: in the upper right of DevTools, select **Customize and control DevTools** \(`...`\) and then select **Open File**.</span></span>

#### <a name="save-and-undo"></a><span data-ttu-id="aedbe-259">Speichern und Rückgängig machen</span><span class="sxs-lookup"><span data-stu-id="aedbe-259">Save and Undo</span></span>

<span data-ttu-id="aedbe-260">Damit JavaScript-Änderungen wirksam werden, wählen `Ctrl` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="aedbe-260">For JavaScript changes to take effect, select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  

<span data-ttu-id="aedbe-261">Wenn Sie eine Datei ändern, wird neben dem Dateinamen ein Sternchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-261">If you change a file, an asterisk appears next to the file name.</span></span>
*   <span data-ttu-id="aedbe-262">Um Änderungen zu speichern, wählen Sie `Ctrl` + `S` unter Windows/Linux oder `Command` + `S` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-262">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>
*   <span data-ttu-id="aedbe-263">Um eine Änderung rückgängig zu machen, wählen Sie `Ctrl` + `Z` unter Windows/Linux oder `Command` + `Z` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-263">To undo a change, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="aedbe-264">Standardmäßig werden Ihre Bearbeitungen verworfen, wenn Sie die Webseite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aedbe-264">By default, your edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="aedbe-265">Weitere Informationen zum Speichern der Änderungen im lokalen Dateisystem finden Sie unter [Bearbeiten von Dateien mit Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex].</span><span class="sxs-lookup"><span data-stu-id="aedbe-265">For more information about how to save the changes in your local file system, see [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

#### <a name="find-and-replace"></a><span data-ttu-id="aedbe-266">Suchen und Ersetzen</span><span class="sxs-lookup"><span data-stu-id="aedbe-266">Find and Replace</span></span>

<span data-ttu-id="aedbe-267">Um Text in der aktuellen Datei zu finden, wählen Sie den Editorbereich aus, um ihm den Fokus zu geben, und wählen Sie dann unter `Ctrl` + `F` Windows/Linux oder `Command` + `F` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-267">To find text in the current file, select the **Editor** pane to give it focus, and then select `Ctrl`+`F` on Windows/Linux, or `Command`+`F` on macOS.</span></span>  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Suchen und Ersetzen im Editorbereich des Tools Quellen" lightbox="../media/find-replace.msft.png":::
   <span data-ttu-id="aedbe-269">**Suchen** und **Ersetzen**im **Editorbereich** des **Tools Quellen**</span><span class="sxs-lookup"><span data-stu-id="aedbe-269">**Find** and **Replace**, in the **Editor** pane of the **Sources** tool</span></span>
:::image-end:::

<span data-ttu-id="aedbe-270">Zum Suchen und Ersetzen von Text wählen Sie die Schaltfläche **Ersetzen** (**A-\>B**) links vom Textfeld **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-270">To find and replace text, select the **Replace** (**A-\>B**) button to the left of the **Find** textbox.</span></span> <span data-ttu-id="aedbe-271">Die **Schaltfläche Ersetzen** (**A-\>B**) wird beim Anzeigen einer bearbeitbaren Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-271">The **Replace** (**A-\>B**) button appears when viewing an editable file.</span></span>

#### <a name="showing-the-changes-you-made"></a><span data-ttu-id="aedbe-272">Anzeigen der vorgenommenen Änderungen</span><span class="sxs-lookup"><span data-stu-id="aedbe-272">Showing the changes you made</span></span>

<span data-ttu-id="aedbe-273">Klicken Sie zum Überprüfen der änderungen, die Sie an einer Datei vorgenommen haben, mit der rechten Maustaste in den Editorbereich, und wählen Sie **dann Lokale Änderungen aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-273">To review the changes you made to a file, right-click in the **Editor** pane and then select **Local Modifications**.</span></span>

<span data-ttu-id="aedbe-274">Die **Drawer** wird am unteren Rand von DevTools geöffnet und zeigt Ihre Änderungen auf der Registerkarte **Änderungen** an.</span><span class="sxs-lookup"><span data-stu-id="aedbe-274">The **Drawer** opens at the bottom of DevTools, showing your changes within the **Changes** tab.</span></span>

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Anzeigen lokaler Änderungen auf der Registerkarte Änderungen der Drawer" lightbox="../media/local-modifications.msft.png":::
   <span data-ttu-id="aedbe-276">Anzeigen **lokaler Änderungen**auf der Registerkarte **Änderungen** der **Drawer**</span><span class="sxs-lookup"><span data-stu-id="aedbe-276">Showing **Local Modifications**, in the **Changes** tab of the **Drawer**</span></span>
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a><span data-ttu-id="aedbe-277">Änderungen innerhalb einer Funktion werden wirksam</span><span class="sxs-lookup"><span data-stu-id="aedbe-277">Changes inside a function take effect</span></span>

<span data-ttu-id="aedbe-278">DevTools wird kein Skript erneut ausgeführt, daher sind die einzigen JavaScript-Änderungen, die wirksam werden, Änderungen, die Sie innerhalb von Funktionen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-278">DevTools doesn't re-run a script, so the only JavaScript changes that take effect are changes that you make within functions.</span></span>  <span data-ttu-id="aedbe-279">In der folgenden Abbildung haben wir beispielsweise den folgenden Code zu dem vom Server zurückgegebenen JavaScript hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="aedbe-279">For example, in the following figure, we added the following code to the JavaScript that is returned by the server:</span></span>  
*   <span data-ttu-id="aedbe-280">Wir haben die Anweisung `console.log('A')` außerhalb einer beliebigen Funktion hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-280">We added the statement `console.log('A')` outside of any function.</span></span>  
*   <span data-ttu-id="aedbe-281">Wir haben die Anweisung `console.log('B')` in einer Funktion `onClick` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-281">We added the statement `console.log('B')` inside an `onClick` function.</span></span>  
<span data-ttu-id="aedbe-282">Anschließend haben wir die Änderungen gespeichert, Zahlen in das Formular eingegeben und dann die Formularschaltfläche ausgewählt, um das Formular zu senden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-282">We then saved the changes, entered numbers into the form, and then selected the form button to send the form.</span></span>  

<span data-ttu-id="aedbe-283">Nach dem Absenden des Formulars wird , das sich auf globaler Ebene befindet, nicht ausgeführt, aber innerhalb einer Funktion wird ausgeführt, und es wird an `console.log('A')` `console.log('B')` die Konsole `onClick` `B` ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="aedbe-283">After submitting the form, `console.log('A')`, which is at global scope, doesn't run, but `console.log('B')`, inside an `onClick` function, does run, outputting `B` to the Console:</span></span>

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript auf globaler Ebene wird nicht erneut ausgeführt" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="aedbe-285">JavaScript auf globaler Ebene wird nicht erneut ausgeführt</span><span class="sxs-lookup"><span data-stu-id="aedbe-285">Global-scope JavaScript is not re-run</span></span>  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="aedbe-286">Neuformatieren einer minifizierten JavaScript-Datei mit Hübschdruck</span><span class="sxs-lookup"><span data-stu-id="aedbe-286">Reformatting a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="aedbe-287">Um eine Datei mit ziemlicher Grafik neu zu formatieren, um sie lesbar zu machen, wählen Sie am unteren Rand des Editorbereichs die Schaltfläche Ziemlich drucken \( Format ![ ](../media/format-icon.msft.png) \) aus, die als geschweifte Klammern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aedbe-287">To use pretty-print to reformat a file to make it readable, select the **Pretty print** button \(![Format](../media/format-icon.msft.png)\), which is shown as braces, at the bottom of the Editor pane.</span></span>  <span data-ttu-id="aedbe-288">Wenn oben im **Editorbereich** eine Schaltfläche "Ziemlich drucken" angezeigt wird, können Sie diese Schaltfläche auswählen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-288">Or, if a **Pretty-print** button appears at the top of the Editor pane, you can select that button.</span></span>

:::image type="complex" source="../media/minified.msft.png" alt-text="Die Schaltfläche Hübsch drucken" lightbox="../media/minified.msft.png":::
   <span data-ttu-id="aedbe-290">Die **Schaltfläche "Hübsch drucken"**</span><span class="sxs-lookup"><span data-stu-id="aedbe-290">The **Pretty print** button</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-291">Die neu formatierte Datei wird auf einer neuen Registerkarte angezeigt, die `:formatted` an den Dateinamen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="aedbe-291">The reformatted file appears in a new tab, with `:formatted` appended to the file name.</span></span>  <span data-ttu-id="aedbe-292">Der neu formatierte Code ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-292">The reformatted code is read-only.</span></span>  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Eine ziemlich gedruckte (neu formatierte) JavaScript-Datei" lightbox="../media/pretty-printed.msft.png":::
   <span data-ttu-id="aedbe-294">Eine ziemlich gedruckte (neu formatierte) JavaScript-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-294">A pretty-printed (reformatted) JavaScript file</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-295">So führen Sie einen Bildlauf der neu formatierten Datei zu dem Code durch, den Sie in der minifizierten Datei auswählen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-295">To make the reformatted file scroll to the code that you select in the minified file:</span></span> 
1.   <span data-ttu-id="aedbe-296">Wenn die Registerkarte neu formatierte Datei geöffnet ist, schließen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="aedbe-296">If the reformatted file tab is open, close it.</span></span>  
1.   <span data-ttu-id="aedbe-297">Wählen Sie code in der verminten Datei im Editorbereich aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-297">Select some code in the minified file in the Editor pane.</span></span>
1.   <span data-ttu-id="aedbe-298">Wählen Sie die **Schaltfläche Hübsch drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-298">Select the **Pretty print** button.</span></span>
<span data-ttu-id="aedbe-299">Der formatierte Code wird auf einer neuen Registerkarte mit einem Bildlauf zu dem ausgewählten Code angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-299">The formatted code appears in a new tab, scrolled to the code that you selected.</span></span>

<span data-ttu-id="aedbe-300">Weitere Informationen finden Sie unter [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span><span class="sxs-lookup"><span data-stu-id="aedbe-300">For more information, see [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span></span>  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a><span data-ttu-id="aedbe-301">Zuordnen von minifizierten Code zu Ihrem Quellcode zum Anzeigen lesbaren Codes</span><span class="sxs-lookup"><span data-stu-id="aedbe-301">Mapping minified code to your source code to show readable code</span></span>

<span data-ttu-id="aedbe-302">Quellzuordnungen von Präprozessoren führen dazu, dass DevTools ihre ursprünglichen JavaScript-Quelldateien zusätzlich zu ihren minifizierten, transformierten JavaScript-Dateien, die vom Server zurückgegeben werden, laden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-302">Source maps from preprocessors cause DevTools to load your original JavaScript source files in addition to your minified, transformed JavaScript files that are returned by the server.</span></span>  <span data-ttu-id="aedbe-303">Anschließend zeigen Sie die ursprünglichen Quelldateien an, während Sie Haltepunkte festlegen und Code schrittweise durchbrechen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-303">You then view your original source files while you set breakpoints and step through code.</span></span>  <span data-ttu-id="aedbe-304">In der zwischenzeit Microsoft Edge tatsächlich ihren minifizierten Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-304">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  

<span data-ttu-id="aedbe-305">Wenn Sie im **Editorbereich** mit der rechten Maustaste auf eine JavaScript-Datei klicken und dann Quellzuordnung hinzufügen **auswählen,** wird ein Popupfeld mit einem Textfeld **quellzuordnungs-URL** und einer Schaltfläche Hinzufügen **angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-305">In the **Editor** pane, if you right-click a JavaScript file and then select **Add source map**, a popup box appears, with a **Source map URL** textbox and an **Add** button.</span></span>

<span data-ttu-id="aedbe-306">Der Source-Mapping-Ansatz sorgt dafür, dass Ihr Front-End-Code auch nach dem Kombinieren, Verfälschen oder Kompilieren des Codes für den Menschen lesbar und debuggbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-306">The source-mapping approach keeps your front-end code human-readable and debuggable even after you combine, minify, or compile it.</span></span>
<span data-ttu-id="aedbe-307">Weitere Informationen finden Sie unter [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="aedbe-307">For more information, see [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span></span>

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a><span data-ttu-id="aedbe-308">Transformationen vom Quellcode in kompilierten Front-End-Code</span><span class="sxs-lookup"><span data-stu-id="aedbe-308">Transformations from source code to compiled front-end code</span></span>

<span data-ttu-id="aedbe-309">Wenn Sie ein Framework verwenden, das Ihre JavaScript-Dateien transformiert, z. B. React, kann sich Ihr lokales JavaScript von dem Front-End-JavaScript unterscheiden, das vom Server zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aedbe-309">If you use a framework that transforms your JavaScript files, such as React, your local source JavaScript might be different than the front-end JavaScript that's returned by the server.</span></span>  <span data-ttu-id="aedbe-310">Arbeitsbereiche werden in diesem Szenario nicht unterstützt, aber die Quellcodezuordnung wird in diesem Szenario unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-310">Workspaces aren't supported in this scenario, but source code mapping is supported in this scenario.</span></span>  

<span data-ttu-id="aedbe-311">In einer Entwicklungsumgebung kann Ihr Server Ihre Quellzuordnungen und Ihre Originaldateien oder Dateien für `.ts` `.jsx` React.</span><span class="sxs-lookup"><span data-stu-id="aedbe-311">In a development environment, your server might include your source maps and your original `.ts` or `.jsx` files for React.</span></span>  <span data-ttu-id="aedbe-312">Das **Tool Sources** zeigt diese Dateien an, ermöglicht es Ihnen jedoch nicht, diese Dateien zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-312">The **Sources** tool displays these files, but doesn't allow you to edit these files.</span></span>  <span data-ttu-id="aedbe-313">Wenn Sie Haltepunkte festlegen und den Debugger verwenden, zeigt DevTools Ihre Ursprünglichen oder Dateien an, aber tatsächlich wird die minifizierte Version Ihrer `.ts` `.jsx` JavaScript-Dateien durchschritten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-313">When you set breakpoints and use the debugger, DevTools displays your original `.ts` or `.jsx` files, but actually steps-through the minified version of your JavaScript files.</span></span>

<span data-ttu-id="aedbe-314">In diesem Szenario ist das **Sources-Tool** nützlich, um das transformierte Front-End-JavaScript, das vom Server zurückgegeben wird, zu überprüfen und zu durchsichten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-314">In this scenario, the **Sources** tool is useful for inspecting and stepping-through the transformed, front-end JavaScript that's returned from the server.</span></span>  <span data-ttu-id="aedbe-315">Verwenden Sie den Debugger, um Watch-Ausdrücke zu definieren, und verwenden Sie die Konsole, um JavaScript-Ausdrücke ein eingeben, um Daten zu bearbeiten, die in den Bereich sind.</span><span class="sxs-lookup"><span data-stu-id="aedbe-315">Use the debugger to define Watch expressions, and use the Console to enter JavaScript expressions to manipulate data that's in-scope.</span></span>

### <a name="editing-a-css-file"></a><span data-ttu-id="aedbe-316">Bearbeiten einer CSS-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-316">Editing a CSS file</span></span>

<span data-ttu-id="aedbe-317">Es gibt zwei Möglichkeiten zum Bearbeiten von CSS in DevTools:</span><span class="sxs-lookup"><span data-stu-id="aedbe-317">There are two ways to edit CSS in DevTools:</span></span>
*   <span data-ttu-id="aedbe-318">Im **Tool Elemente** arbeiten Sie mit einer CSS-Einstellung gleichzeitig über Benutzeroberflächensteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="aedbe-318">In the **Elements** tool, you work with one CSS setting at a time, through user interface controls.</span></span>  <span data-ttu-id="aedbe-319">Dieser Ansatz wird in den meisten Fällen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-319">This approach is recommended in most cases.</span></span>  <span data-ttu-id="aedbe-320">Weitere Informationen finden Sie unter [Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen.][DevToolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="aedbe-320">For more information, see [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span></span>
*   <span data-ttu-id="aedbe-321">Im **Tool Quellen** verwenden Sie einen Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="aedbe-321">In the **Sources** tool, you use a text editor.</span></span>

<span data-ttu-id="aedbe-322">Das Tool Sources unterstützt das direkte Bearbeiten einer CSS-Datei.</span><span class="sxs-lookup"><span data-stu-id="aedbe-322">The Sources tool supports directly editing a CSS file.</span></span>  <span data-ttu-id="aedbe-323">Wenn Sie z. B. die CSS-Datei aus dem Lernprogramm Dateien mit [Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex] bearbeiten bearbeiten, um der folgenden Formatvorlagenregel zu entsprechen, wird das Element in der oberen linken Ecke der gerenderten Webseite `H1` in Grün geändert:</span><span class="sxs-lookup"><span data-stu-id="aedbe-323">For example, if you edit the CSS file from the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to match the style rule below, the `H1` element in the upper left of the rendered webpage changes to green:</span></span>

```css
h1 {
  color: green;
}  
```

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editorbereich, um die Textfarbe der H1-Überschrift in Grün zu ändern" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="aedbe-325">Bearbeiten von CSS im **Editorbereich,** um die Textfarbe der Überschrift in `H1` Grün zu ändern</span><span class="sxs-lookup"><span data-stu-id="aedbe-325">Edit CSS in the **Editor** pane to change the text color of the `H1` heading to green</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-326">#A0 werden sofort wirksam. Sie müssen die Änderungen nicht manuell speichern.</span><span class="sxs-lookup"><span data-stu-id="aedbe-326">CSS changes take effect immediately; you don't need to manually save the changes.</span></span>

#### <a name="see-also"></a><span data-ttu-id="aedbe-327">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-327">See also</span></span>

*   [<span data-ttu-id="aedbe-328">Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="aedbe-328">Edit CSS font styles and settings in the Styles pane</span></span>][DevToolsInspectStylesEditFonts]

*   <span data-ttu-id="aedbe-329">[DevTools für Anfänger: Erste Schritte mit CSS][DevToolsBeginnersCss] – Lernprogramm</span><span class="sxs-lookup"><span data-stu-id="aedbe-329">[DevTools for beginners: Get started with CSS][DevToolsBeginnersCss] - tutorial</span></span>

### <a name="editing-an-html-file"></a><span data-ttu-id="aedbe-330">Bearbeiten einer HTML-Datei</span><span class="sxs-lookup"><span data-stu-id="aedbe-330">Editing an HTML file</span></span>

<span data-ttu-id="aedbe-331">Es gibt zwei Möglichkeiten zum Bearbeiten von HTML in DevTools:</span><span class="sxs-lookup"><span data-stu-id="aedbe-331">There are two ways to edit HTML in DevTools:</span></span>  
*   <span data-ttu-id="aedbe-332">Im **Elementtool** arbeiten Sie mit einem HTML-Element gleichzeitig über Benutzeroberflächensteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="aedbe-332">In the **Elements** tool, you work with one HTML element at a time, through user interface controls.</span></span>  
*   <span data-ttu-id="aedbe-333">Im **Tool Quellen** verwenden Sie einen Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="aedbe-333">In the **Sources** tool, you use a text editor.</span></span>  

:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="Der HTML-Editor des Sources-Tools" lightbox="../media/sources-html-editor.msft.png":::
   <span data-ttu-id="aedbe-335">Der HTML-Editor des **Sources-Tools**</span><span class="sxs-lookup"><span data-stu-id="aedbe-335">The HTML editor of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="aedbe-336">Im Gegensatz zu einer JavaScript- oder CSS-Datei kann eine vom Webserver zurückgegebene HTML-Datei nicht direkt im Tool Quellen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-336">Unlike a JavaScript or CSS file, an HTML file that is returned by the web server cannot be directly edited in the Sources tool.</span></span>  <span data-ttu-id="aedbe-337">Zum Bearbeiten einer HTML-Datei mit dem Editor des Tools Sources muss sich die HTML-Datei in einem Arbeitsbereich oder auf der Registerkarte **Außerkraftsetzungen** befinden.  Lesen Sie die folgenden Unterabschnitte des aktuellen Artikels:</span><span class="sxs-lookup"><span data-stu-id="aedbe-337">To edit an HTML file using the Editor of the Sources tool, the HTML file must be in a Workspace or on the **Overrides** tab.  See these subsections of the current article:</span></span>
*   [<span data-ttu-id="aedbe-338">Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="aedbe-338">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="aedbe-339">Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien</span><span class="sxs-lookup"><span data-stu-id="aedbe-339">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
    
<span data-ttu-id="aedbe-340">Um Änderungen zu speichern, wählen Sie `Ctrl` + `S` unter Windows/Linux oder `Command` + `S` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-340">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>  <span data-ttu-id="aedbe-341">Eine bearbeitete Datei wird durch ein Sternchen markiert.</span><span class="sxs-lookup"><span data-stu-id="aedbe-341">An edited file is marked by an asterisk.</span></span>  

<span data-ttu-id="aedbe-342">Um Text zu finden, wählen Sie `Ctrl` + `F` unter Windows/Linux oder `Command` + `F` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-342">To find text, select `Ctrl`+`F` on Windows/Linux or `Command`+`F` on macOS.</span></span>

<span data-ttu-id="aedbe-343">Um eine Bearbeitung rückgängig zu machen, wählen Sie `Ctrl` + `Z` unter Windows/Linux oder `Command` + `Z` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-343">To undo an edit, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="aedbe-344">Um andere Befehle beim Bearbeiten einer HTML-Datei anzuzeigen, klicken Sie im Bereich Editor mit der rechten Maustaste auf die HTML-Datei.</span><span class="sxs-lookup"><span data-stu-id="aedbe-344">To view other commands while editing an HTML file, in the Editor pane, right-click the HTML file.</span></span>

<span data-ttu-id="aedbe-345">Sie können HTML auch mithilfe eines HTML-Editors anstelle von DevTools bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-345">You can also edit HTML by using an HTML editor, rather than DevTools.</span></span>  <span data-ttu-id="aedbe-346">Der Artikel [DevTools für Anfänger: Erste][DevToolsBeginnersHtml] Schritte mit HTML und das DOM verwendet eine Website, die die HTML-Bearbeitung auf der Webseite ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="aedbe-346">For example, the article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.</span></span>

### <a name="going-to-a-line-number-or-function"></a><span data-ttu-id="aedbe-347">Zu einer Zeilennummer oder Funktion</span><span class="sxs-lookup"><span data-stu-id="aedbe-347">Going to a line number or function</span></span>

<span data-ttu-id="aedbe-348">Um zu einer Zeilennummer oder einem Symbol (z. B. einem Funktionsnamen) in der Datei zu wechseln, die im Editorbereich geöffnet ist, können Sie das Befehlsmenü verwenden, anstatt einen Bildlauf durch die Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-348">To go to a line number or symbol (such as a function name) in the file which is open in the Editor pane, you can use the Command Menu, rather than scrolling through the file.</span></span>

1.   <span data-ttu-id="aedbe-349">Wählen Sie **im Bereich Navigator** die Ellipsen (...) aus. (**Weitere Optionen**), und wählen Sie dann Datei öffnen **aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-349">In the **Navigator** pane, select the ellipses (...) (**More options**), and then select **Open File**.</span></span>  <span data-ttu-id="aedbe-350">Das Befehlsmenü wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-350">The Command Menu appears.</span></span>  
1.   <span data-ttu-id="aedbe-351">Geben Sie eines der folgenden Zeichen ein:</span><span class="sxs-lookup"><span data-stu-id="aedbe-351">Type one of the following characters:</span></span>  

| <span data-ttu-id="aedbe-352">Zeichen</span><span class="sxs-lookup"><span data-stu-id="aedbe-352">Character</span></span> | <span data-ttu-id="aedbe-353">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="aedbe-353">Command name</span></span> | <span data-ttu-id="aedbe-354">Zweck</span><span class="sxs-lookup"><span data-stu-id="aedbe-354">Purpose</span></span> |
|---|---|---|
| <span data-ttu-id="aedbe-355">\:</span><span class="sxs-lookup"><span data-stu-id="aedbe-355">\:</span></span> | **<span data-ttu-id="aedbe-356">Zur Zeile wechseln</span><span class="sxs-lookup"><span data-stu-id="aedbe-356">Go to line</span></span>** | <span data-ttu-id="aedbe-357">Wechseln Sie zu einer Zeilennummer.</span><span class="sxs-lookup"><span data-stu-id="aedbe-357">Go to a line number.</span></span> |
| \@ | **<span data-ttu-id="aedbe-358">Wechseln zum Symbol</span><span class="sxs-lookup"><span data-stu-id="aedbe-358">Go to symbol</span></span>** | <span data-ttu-id="aedbe-359">Wechseln Sie zu einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="aedbe-359">Go to a function.</span></span>  <span data-ttu-id="aedbe-360">Wenn Sie eingeben, werden im Befehlsmenü die Funktionen aufgelistet, die sich in der Im Editorbereich geöffneten `@` JavaScript-Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-360">When you type `@`, the Command Menu lists the functions that are found in the JavaScript file which is open in the Editor pane.</span></span> |
   
<span data-ttu-id="aedbe-361">Weitere Informationen finden Sie unter [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="aedbe-361">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

### <a name="displaying-source-files-when-using-a-different-tool"></a><span data-ttu-id="aedbe-362">Anzeigen von Quelldateien bei Verwendung eines anderen Tools</span><span class="sxs-lookup"><span data-stu-id="aedbe-362">Displaying source files when using a different tool</span></span>

<span data-ttu-id="aedbe-363">Der Hauptort zum Anzeigen von Quelldateien in devTools befindet sich im **Sources-Tool.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-363">The main place to view source files in the DevTools is within the **Sources** tool.</span></span>  <span data-ttu-id="aedbe-364">Manchmal müssen Sie jedoch auf andere Tools wie **Elemente** oder **Konsole**zugreifen, während Sie Ihre Quelldateien anzeigen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-364">But sometimes you need to access other tools, such as **Elements** or **Console**, while viewing or editing your source files.</span></span>  <span data-ttu-id="aedbe-365">Verwenden Sie **das Tool Schnellquellen** in der [Schublade][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="aedbe-365">Use the **Quick Sources** tool in the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>

1.  <span data-ttu-id="aedbe-366">Wählen Sie ein anderes Tool als das **Sources-Tool** aus, z. B. das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-366">Select a tool other than the **Sources** tool, such as the **Elements** tool.</span></span>  
1.  <span data-ttu-id="aedbe-367">Wählen `Ctrl` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="aedbe-367">Select `Ctrl`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="aedbe-368">Das Befehlsmenü wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aedbe-368">The Command Menu opens.</span></span>  
1.  <span data-ttu-id="aedbe-369">Geben `Quick Source` Sie ein, und wählen Sie **Dann Schnellquelle anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-369">Type `Quick Source`, and then select **Show Quick Source**.</span></span>  <span data-ttu-id="aedbe-370">Am unteren Rand des DevTools-Fensters wird die Schublade angezeigt, und der Schnellquellenbereich ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-370">At the bottom of the DevTools window, the Drawer appears, with the **Quick Source** panel selected.</span></span>  <span data-ttu-id="aedbe-371">Der **Schnellquellenbereich** enthält die letzte Datei, die Sie im **Tool Quellen** in einer kompakten Version des DevTools-Code-Editors bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-371">The **Quick Source** panel contains the last file you edited in the **Sources** tool, within a compact version of the DevTools code editor.</span></span>  
1.  <span data-ttu-id="aedbe-372">Wählen `Ctrl` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) aus, um das Dialogfeld Datei öffnen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-372">Select `Ctrl`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  

## <a name="using-the-debugger-pane-to-debug-javascript-code"></a><span data-ttu-id="aedbe-373">Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code</span><span class="sxs-lookup"><span data-stu-id="aedbe-373">Using the Debugger pane to debug JavaScript code</span></span>

<span data-ttu-id="aedbe-374">Verwenden Sie den JavaScript-Debugger, um den vom Server zurückgegebenen JavaScript-Code zu durchschritten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-374">Use the JavaScript debugger to step through the JavaScript code that's returned by the server.</span></span> <span data-ttu-id="aedbe-375">Der Debugger enthält den **Debuggerbereich** sowie Haltepunkte, die Sie für Codezeilen im **Editorbereich festlegen.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-375">The debugger includes the **Debugger** pane, along with breakpoints that you set on lines of code in the **Editor** pane.</span></span>

<span data-ttu-id="aedbe-376">Mit dem Debugger durchschritten Sie den Code, während Sie alle angegebenen JavaScript-Ausdrücke ansehen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-376">With the debugger, you step through the code, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="aedbe-377">Beobachten und manuell ändern Sie Variablenwerte, und zeigen Sie automatisch an, welche Variablen sich im Bereich der aktuellen Anweisung befinden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-377">Watch and manually change variable values, and automatically show which variables are in-scope for the current statement.</span></span>

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="Der Debuggerbereich des Tools Quellen  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   <span data-ttu-id="aedbe-379">Der **Debuggerbereich** des **Tools Quellen**</span><span class="sxs-lookup"><span data-stu-id="aedbe-379">The **Debugger** pane of the **Sources** tool</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-380">Der Debugger unterstützt standardmäßige Debugaktionen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="aedbe-380">The debugger supports standard debugging actions, such as:</span></span>  
*   <span data-ttu-id="aedbe-381">Festlegen von Haltepunkten, um Code anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-381">Setting breakpoints, to pause code.</span></span>
*   <span data-ttu-id="aedbe-382">Schrittweises Durchfingen von Code.</span><span class="sxs-lookup"><span data-stu-id="aedbe-382">Stepping through code.</span></span>
*   <span data-ttu-id="aedbe-383">Anzeigen und Bearbeiten von Eigenschaften und Variablen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-383">Viewing and editing properties and variables.</span></span>
*   <span data-ttu-id="aedbe-384">Beobachten der Werte von JavaScript-Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="aedbe-384">Watching the values of JavaScript expressions.</span></span>
*   <span data-ttu-id="aedbe-385">Anzeigen der Aufrufliste (die Sequenz der bisher verwendeten Funktionsaufrufe).</span><span class="sxs-lookup"><span data-stu-id="aedbe-385">Viewing the call stack (the sequence of function calls so far).</span></span>

<span data-ttu-id="aedbe-386">Der Debugger in DevTools ist so konzipiert, dass er wie der [Debugger in][CodeVisualStudioComDocsEditorDebugging] Visual Studio Code und der [Debugger in Visual Studio.][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]</span><span class="sxs-lookup"><span data-stu-id="aedbe-386">The debugger in DevTools is designed to look, feel, and work like [the debugger in Visual Studio Code][CodeVisualStudioComDocsEditorDebugging] and [the debugger in Visual Studio][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span></span>

<span data-ttu-id="aedbe-387">Die folgenden Unterabschnitte umfassen das Debuggen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-387">The following subsections cover debugging:</span></span>
*   [<span data-ttu-id="aedbe-388">Der grundlegende Ansatz für die Verwendung eines Debuggers</span><span class="sxs-lookup"><span data-stu-id="aedbe-388">The basic approach to using a debugger</span></span>](#the-basic-approach-to-using-a-debugger)
*   [<span data-ttu-id="aedbe-389">Vorteile von Watch und Scope des Debuggers gegenüber console.log</span><span class="sxs-lookup"><span data-stu-id="aedbe-389">Advantages of the debugger's Watch and Scope over console.log</span></span>](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)
*   [<span data-ttu-id="aedbe-390">Debuggen von Visual Studio Code direkt</span><span class="sxs-lookup"><span data-stu-id="aedbe-390">Debug from Visual Studio Code directly</span></span>](#debug-from-visual-studio-code-directly)
*   [<span data-ttu-id="aedbe-391">Artikel zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="aedbe-391">Articles about debugging</span></span>](#articles-about-debugging)

### <a name="the-basic-approach-to-using-a-debugger"></a><span data-ttu-id="aedbe-392">Der grundlegende Ansatz für die Verwendung eines Debuggers</span><span class="sxs-lookup"><span data-stu-id="aedbe-392">The basic approach to using a debugger</span></span>

<span data-ttu-id="aedbe-393">Zur Problembehandlung von JavaScript-Code können Sie `console.log()` Anweisungen im **Editorbereich** einfügen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-393">To troubleshoot JavaScript code, you can insert `console.log()` statements in the **Editor** pane.</span></span>  <span data-ttu-id="aedbe-394">Ein weiterer, leistungsstärkerer Ansatz ist die Verwendung des Debuggers Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="aedbe-394">Another, more powerful approach is to use the debugger of Microsoft Edge DevTools.</span></span>  <span data-ttu-id="aedbe-395">Die Verwendung eines Debuggers kann einfacher als sein, sobald Sie mit dem `console.log()` Debuggeransatz vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="aedbe-395">Using a debugger can actually be simpler than `console.log()`, once you're familiar with the debugger approach.</span></span>

<span data-ttu-id="aedbe-396">Um einen Debugger auf einer Webseite zu verwenden, legen Sie in der Regel einen Haltepunkt ein und senden dann ein Formular von der Webseite wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aedbe-396">To use a debugger on a webpage, you typically set a breakpoint and then send a form from the webpage, as follows:</span></span>

1.  <span data-ttu-id="aedbe-397">Öffnen Sie die Webseite auf einer neuen Registerkarte des Browsers.</span><span class="sxs-lookup"><span data-stu-id="aedbe-397">Open the webpage in a new tab of the browser.</span></span>  <span data-ttu-id="aedbe-398">Öffnen Sie beispielsweise diese Formularwebseite auf einer neuen Registerkarte: Demo: Erste Schritte Debuggen von JavaScript mit Microsoft Edge [(Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span><span class="sxs-lookup"><span data-stu-id="aedbe-398">For example, open this form webpage in a new tab: [Demo: Get Started Debugging JavaScript with Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span></span>

1.  <span data-ttu-id="aedbe-399">Wählen Sie diese Option aus, um das `F12` **Fenster DevTools** zu öffnen, und wählen Sie dann die Registerkarte **Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="aedbe-399">Select `F12` to open the **DevTools** window, and then select the **Sources** tab.</span></span>

1.  <span data-ttu-id="aedbe-400">Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Seite** aus, und wählen Sie dann die JavaScript-Datei aus, z. B. `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="aedbe-400">In the **Navigator** pane (on the left), select the **Page** tab, and then select the JavaScript file, such as `get-started.js`.</span></span>

1.  <span data-ttu-id="aedbe-401">Wählen Sie **im Bereich Editor** eine Zeilennummer in der Nähe einer verdächtigen Codezeile aus, um einen Haltepunkt für diese Zeile zu setzen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-401">In the **Editor** pane, select a line number near a suspect line of code, to set a breakpoint on that line.</span></span>  <span data-ttu-id="aedbe-402">In der folgenden Abbildung wird ein Haltepunkt für die Zeile `var sum = addend1 + addend2;` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-402">In the figure below, a breakpoint is set on the line `var sum = addend1 + addend2;`.</span></span>

1.  <span data-ttu-id="aedbe-403">Geben Sie auf der Webseite Werte ein, und übermitteln Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="aedbe-403">In the webpage, enter values and submit the form.</span></span>  <span data-ttu-id="aedbe-404">Geben Sie beispielsweise Zahlen wie und ein, und wählen Sie dann die Schaltfläche Nummer 1 hinzufügen `5` und `1` Nummer **2 aus.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-404">For example, enter numbers, such as `5` and `1`, then select the button **Add Number 1 and Number 2**.</span></span>  

    <span data-ttu-id="aedbe-405">Der Debugger führt den JavaScript-Code aus und hält dann am Haltepunkt an.</span><span class="sxs-lookup"><span data-stu-id="aedbe-405">The debugger runs the JavaScript code and then pauses at the breakpoint.</span></span>  <span data-ttu-id="aedbe-406">Der Debugger befindet sich nun im Angehalten-Modus, sodass Sie die Werte der Eigenschaften überprüfen können, die sich im Bereich befinden, und den Code schrittweise durchschritten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-406">The debugger is now in Paused mode, so you can inspect the values of the properties that are in-scope, and step through the code.</span></span>

    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Eingeben des angehaltenen Modus des Debuggers" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        <span data-ttu-id="aedbe-408">Eingeben des angehaltenen Modus des Debuggers</span><span class="sxs-lookup"><span data-stu-id="aedbe-408">Entering Paused mode of the debugger</span></span>  
    :::image-end:::  

    <span data-ttu-id="aedbe-409">In der obigen Abbildung haben wir die Watch-Ausdrücke und hinzugefügt und zwei Zeilen über `sum` `typeof sum` den Haltepunkt gestuft.</span><span class="sxs-lookup"><span data-stu-id="aedbe-409">In the above figure, we added the Watch expressions `sum` and `typeof sum`, and stepped two lines past the breakpoint.</span></span>

1.  <span data-ttu-id="aedbe-410">Untersuchen Sie die Werte im **Bereich Bereich,** in dem alle Variablen oder Eigenschaften angezeigt werden, die sich im Bereich des aktuellen Haltepunkts befinden, und deren Werte.</span><span class="sxs-lookup"><span data-stu-id="aedbe-410">Examine the values in the **Scope** pane, which shows all variables or properties that are in-scope for the current breakpoint, and their values.</span></span>  <span data-ttu-id="aedbe-411">Oder fügen Sie Ausdrücke im Bereich **"Watch"** hinzu.</span><span class="sxs-lookup"><span data-stu-id="aedbe-411">Or, add expressions in the **Watch** pane.</span></span>  <span data-ttu-id="aedbe-412">Diese Ausdrücke sind dieselben Ausdrücke, die Sie in eine Anweisung schreiben `console.log` würden, um Ihren Code zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-412">These expressions are the same expressions that you would write within a `console.log` statement to debug your code.</span></span>  <span data-ttu-id="aedbe-413">Verwenden Sie die Konsole, um JavaScript-Befehle zum Bearbeiten von Daten im aktuellen Kontext **auszuführen.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-413">To run JavaScript commands to manipulate data in the current context, use the **Console**.</span></span>  <span data-ttu-id="aedbe-414">Wählen Sie aus, um die Konsole zu `Esc` öffnen.</span><span class="sxs-lookup"><span data-stu-id="aedbe-414">To open the console, select `Esc`.</span></span>  

1.  <span data-ttu-id="aedbe-415">Gehen Sie durch den Code, indem Sie die Steuerelemente am oberen Rand des **Debuggerbereichs** verwenden, z. B. **Step** ( `F9` ).</span><span class="sxs-lookup"><span data-stu-id="aedbe-415">Step through the code by using the controls at the top of the **Debugger** pane, such as **Step** (`F9`).</span></span>

#### <a name="see-also"></a><span data-ttu-id="aedbe-416">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="aedbe-416">See also</span></span>

*   <span data-ttu-id="aedbe-417">[Erste Schritte mit dem Debuggen][DevtoolsGuideChromiumJavascriptIndex] von JavaScript – ein Lernprogramm mit einer vorhandenen, einfachen Webseite, die einige Formularsteuerelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="aedbe-417">[Get started with debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] - a tutorial using an existing, simple webpage that contains a few form controls.</span></span>

### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a><span data-ttu-id="aedbe-418">Vorteile des Debuggers Watch and Scope over console\.log</span><span class="sxs-lookup"><span data-stu-id="aedbe-418">Advantages of the debugger\'s Watch and Scope over console\.log</span></span>

<span data-ttu-id="aedbe-419">Diese drei Ansätze sind äquivalent:</span><span class="sxs-lookup"><span data-stu-id="aedbe-419">These three approaches are equivalent:</span></span>

*   <span data-ttu-id="aedbe-420">Vorübergehendes Hinzufügen der Anweisungen `console.log(sum)` und `console.log(typeof sum)` im Code, wobei sich der Bereich `sum` befindet.</span><span class="sxs-lookup"><span data-stu-id="aedbe-420">Temporarily adding the statements `console.log(sum)` and `console.log(typeof sum)` in the code, where `sum` is in-scope.</span></span>
*   <span data-ttu-id="aedbe-421">Ausstellen der Anweisungen und im Konsolenbereich der DevTools, wenn der Debugger angehalten wird, `sum` wo sich der Bereich `console.log(typeof sum)` `sum` befindet.</span><span class="sxs-lookup"><span data-stu-id="aedbe-421">Issuing the statements `sum` and `console.log(typeof sum)` in the **Console** pane of the DevTools, when the debugger is paused where `sum` is in-scope.</span></span>
*   <span data-ttu-id="aedbe-422">Festlegen der `sum` Watch-Ausdrücke und `typeof sum` im **Debuggerbereich.**</span><span class="sxs-lookup"><span data-stu-id="aedbe-422">Setting the **Watch** expressions `sum` and `typeof sum` in the **Debugger** pane.</span></span>

<span data-ttu-id="aedbe-423">Wenn sich die Variable im Bereich befindet und ihr Wert automatisch im Bereich bereich des `sum` `sum` **Debuggerbereichs** angezeigt wird, werden sie auch im Editorbereich überlagert, wo berechnet `sum` wird.</span><span class="sxs-lookup"><span data-stu-id="aedbe-423">When the variable `sum` is in-scope, `sum` and its value are automatically shown in the **Scope** section of the **Debugger** pane, and are also overlaid in the Editor pane where `sum` is calculated.</span></span>  <span data-ttu-id="aedbe-424">Daher müssten Sie wahrscheinlich keinen Watch-Ausdruck für `sum` definieren.</span><span class="sxs-lookup"><span data-stu-id="aedbe-424">So you probably wouldn't need to define a Watch expression for `sum`.</span></span>

<span data-ttu-id="aedbe-425">Der Debugger bietet eine reichhaltigere, flexiblere Anzeige und Umgebung als eine `console.log` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="aedbe-425">The debugger gives a richer, more flexible display and environment than a `console.log` statement.</span></span>  <span data-ttu-id="aedbe-426">Im Debugger können Sie z. B. die Werte aller derzeit definierten Eigenschaften und Variablen anzeigen und ändern, wenn Sie den Code durchschritten haben.</span><span class="sxs-lookup"><span data-stu-id="aedbe-426">For example, in the debugger, as you step through the code, you can display and change the values of all currently defined properties and variables.</span></span>  <span data-ttu-id="aedbe-427">Sie können auch JavaScript-Anweisungen in der **Konsole ausschreiben,** z. B. um Werte in einem Array zu ändern, das sich im Bereich des Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="aedbe-427">You can also issue JavaScript statements in the **Console**, such as to change values in an array that's in-scope.</span></span>  <span data-ttu-id="aedbe-428">(Wählen Sie **Esc**aus, um die Konsole anzeigen zu können.)</span><span class="sxs-lookup"><span data-stu-id="aedbe-428">(To display the Console, select **Esc**.)</span></span>

<span data-ttu-id="aedbe-429">Haltepunkte und Watch-Ausdrücke werden beim Aktualisieren der Webseite beibehalten.</span><span class="sxs-lookup"><span data-stu-id="aedbe-429">Breakpoints and Watch expressions are preserved when you refresh the webpage.</span></span>

### <a name="debug-from-visual-studio-code-directly"></a><span data-ttu-id="aedbe-430">Debuggen von Visual Studio Code direkt</span><span class="sxs-lookup"><span data-stu-id="aedbe-430">Debug from Visual Studio Code directly</span></span>

<span data-ttu-id="aedbe-431">Verwenden Sie die **Microsoft Edge Tools for VS Code** extension for Visual Studio Code, um den vollständigeren Debugger von Visual Studio Code anstelle des DevTools-Debuggers zu Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="aedbe-431">To use the more full-featured debugger of Visual Studio Code instead of the DevTools debugger, use the **Microsoft Edge Tools for VS Code** extension for Visual Studio Code.</span></span>

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="Die Microsoft Edge Tools for VS Code extension for Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   <span data-ttu-id="aedbe-433">Die **Microsoft Edge Tools for VS Code** extension for Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="aedbe-433">The **Microsoft Edge Tools for VS Code** extension for Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="aedbe-434">Diese Erweiterung bietet Zugriff auf die **Elemente** und **Netzwerktools** von Microsoft Edge DevTools innerhalb Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="aedbe-434">This extension provides access to the **Elements** and **Network** tools of Microsoft Edge DevTools, from within Microsoft Visual Studio Code.</span></span>  

<span data-ttu-id="aedbe-435">Weitere Informationen finden Sie [unter Visual Studio Code übersicht][DevToolsVSCodeIndex] und GitHub Readme-Seite, Microsoft Edge Developer Tools for [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="aedbe-435">For more information, see [Visual Studio Code overview][DevToolsVSCodeIndex] and the GitHub Readme page, [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="articles-about-debugging"></a><span data-ttu-id="aedbe-436">Artikel zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="aedbe-436">Articles about debugging</span></span>

<span data-ttu-id="aedbe-437">In den folgenden Artikeln werden der **Debuggerbereich** und die Haltepunkte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="aedbe-437">The following articles cover the **Debugger** pane and breakpoints:</span></span>

*   <span data-ttu-id="aedbe-438">[Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] – Ein Lernprogramm (mit Bildschirmaufzeichnungen) mit einem vorhandenen, einfachen Projekt.</span><span class="sxs-lookup"><span data-stu-id="aedbe-438">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - A tutorial (with screen captures), using an existing, simple project.</span></span>

*   <span data-ttu-id="aedbe-439">[Verwenden der Debuggerfeatures][DevToolsJavaScriptReference] : Verwenden des Debuggers zum Festlegen von Haltepunkten, Schrittweises Durchbrechen von Code, Anzeigen und Ändern von Variablenwerten, Beobachten von JavaScript-Ausdrücken und Anzeigen der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="aedbe-439">[Use the debugger features][DevToolsJavaScriptReference] - How to use the debugger to set breakpoints, step through code, view and modify variable values, watch JavaScript expressions, and view the call stack.</span></span>

*   <span data-ttu-id="aedbe-440">[Anhalten des Codes mit Haltepunkten][DevToolsJavaScriptBreakpoints] – Festlegen grundlegender und spezieller Haltepunkte im Debugger.</span><span class="sxs-lookup"><span data-stu-id="aedbe-440">[Pause your code with breakpoints][DevToolsJavaScriptBreakpoints] - How to set basic and specialized breakpoints in the debugger.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aedbe-441">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="aedbe-441">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools für Anfänger: Erste Schritte mit CSS | Microsoft Docs"
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools für Anfänger: Erste Schritte mit HTML und der DOM-| Microsoft Docs"
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer – Anpassen Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links) | Microsoft Docs"
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Führen Sie Codeausschnitte von JavaScript auf jeder Webseite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Formatvorlagenbereich | Microsoft Docs"
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Anhalten des Codes mit Haltepunkten | Microsoft Docs"
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Markieren von Inhaltsskripts als Bibliothekscode | Microsoft Docs"
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Verwenden der Debuggerfeatures | Microsoft Docs"
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Neuvergrößern einer minifizierten JavaScript-Datei mit Hübschdruck – Verwenden Sie die Debuggerfeatures | Microsoft Docs"
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Map preprocessed code to source code | Microsoft Docs"
[DevToolsVSCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code Übersicht | Microsoft Docs"
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Erstellen eines Erweiterungs-Lernprogramms Teil 2 | Microsoft Docs"
<!-- external: -->
[CodeVisualStudioComDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Debuggen – Visual Studio Code | Microsoft Docs"
[DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Navigieren Sie durch Code mit Visual Studio Debugger| Microsoft Docs"
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Entwicklertools für Visual Studio Code | GitHub"
[DevtoolsGlitchMeDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demo: Erste Schritte Debuggen von JavaScript mit Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Ursprung | HTML-Standard"  
[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Inhaltsskripts | MDN"  
[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"

> [!NOTE]
> <span data-ttu-id="aedbe-467">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aedbe-467">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aedbe-468">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="aedbe-468">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="aedbe-470">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aedbe-470">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
