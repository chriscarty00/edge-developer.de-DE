---
description: Erfahren Sie, wie Sie In DevTools vorgenommene Änderungen auf dem Datenträger speichern.
title: Bearbeiten von Dateien mit Arbeitsbereichen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 640bb80e01f776c763af053cf8354ce90cf52e93
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564665"
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
# <a name="edit-files-with-workspaces"></a><span data-ttu-id="89bfa-104">Bearbeiten von Dateien mit Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="89bfa-104">Edit files with Workspaces</span></span>  

<span data-ttu-id="89bfa-105">Dieses Lernprogramm bietet praktische Übungen zum Einrichten und Verwenden eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="89bfa-105">This tutorial provides hands-on practice in setting up and using a Workspace.</span></span>  <span data-ttu-id="89bfa-106">Nachdem Sie einem Arbeitsbereich Dateien hinzugefügt haben, werden die Änderungen, die Sie in Ihrem Quellcode in DevTools vornehmen, auf Ihrem lokalen Computer gespeichert und nach dem Aktualisieren der Webseite beibehalten.</span><span class="sxs-lookup"><span data-stu-id="89bfa-106">After you add files to a Workspace, the changes that you make in your source code within DevTools are saved on your local computer, and are preserved after you refresh the webpage.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="89bfa-107">**Voraussetzungen**: Bevor Sie mit diesem Lernprogramm beginnen, sollten Sie wissen, wie Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="89bfa-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="89bfa-108">Erstellen einer Webseite mithilfe von HTML, CSS und JavaScript</span><span class="sxs-lookup"><span data-stu-id="89bfa-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="89bfa-109">Verwenden von DevTools zum Vornehmen grundlegender Änderungen an CSS</span><span class="sxs-lookup"><span data-stu-id="89bfa-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="89bfa-110">Ausführen eines lokalen HTTP-Webservers</span><span class="sxs-lookup"><span data-stu-id="89bfa-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="89bfa-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="89bfa-111">Overview</span></span>  

<span data-ttu-id="89bfa-112">Mit Arbeitsbereichen können Sie eine Änderung, die Sie in Devtools in einer lokalen Kopie derselben Datei auf Ihrem Computer erstellen, speichern.</span><span class="sxs-lookup"><span data-stu-id="89bfa-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="89bfa-113">Für dieses Lernprogramm sollten Sie die folgenden Einstellungen auf Ihrem Computer haben.</span><span class="sxs-lookup"><span data-stu-id="89bfa-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="89bfa-114">Sie haben den Quellcode für Ihre Website auf Ihrem Desktop.</span><span class="sxs-lookup"><span data-stu-id="89bfa-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="89bfa-115">Sie ausführen einen lokalen Webserver aus dem Quellcodeverzeichnis, sodass auf die Website unter zugegriffen werden `localhost:8080` kann.</span><span class="sxs-lookup"><span data-stu-id="89bfa-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="89bfa-116">Sie haben in Microsoft Edge geöffnet, und Sie verwenden `localhost:8080` DevTools, um die CSS der Website zu ändern.</span><span class="sxs-lookup"><span data-stu-id="89bfa-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="89bfa-117">Wenn Arbeitsbereiche aktiviert sind, werden die CSS-Änderungen, die Sie in DevTools vornehmen, im Quellcode auf Ihrem Desktop gespeichert.</span><span class="sxs-lookup"><span data-stu-id="89bfa-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="89bfa-118">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="89bfa-118">Limitations</span></span>  

<span data-ttu-id="89bfa-119">Wenn Sie ein modernes Framework verwenden, wird der Quellcode wahrscheinlich von einem Format transformiert, das einfach zu verwalten ist, in ein Format, das so optimiert ist, dass er so schnell wie möglich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="89bfa-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="89bfa-120">Workspaces ist in der Regel in der Lage, den optimierten Code mithilfe von Quellzuordnungen wieder dem ursprünglichen [Quellcode zu zuordnungen.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="89bfa-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="89bfa-121">Es gibt jedoch viele Unterschiede zwischen Frameworks darüber, wie jedes Framework Quellzuordnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="89bfa-121">But there is a lot of variation between frameworks over how each framework uses source maps.</span></span>  <span data-ttu-id="89bfa-122">Devtools unterstützt nicht alle Variationen.</span><span class="sxs-lookup"><span data-stu-id="89bfa-122">Devtools doesn't support all of the variations.</span></span>  

<span data-ttu-id="89bfa-123">Arbeitsbereiche funktionieren mit dem folgenden Framework nicht.</span><span class="sxs-lookup"><span data-stu-id="89bfa-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="89bfa-124">Erstellen React App</span><span class="sxs-lookup"><span data-stu-id="89bfa-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="89bfa-125">Verwandtes Feature: Lokale Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="89bfa-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="89bfa-126">**Lokale Außerkraftsetzungen** ist ein weiteres DevTools-Feature, das Arbeitsbereichen ähnelt.</span><span class="sxs-lookup"><span data-stu-id="89bfa-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="89bfa-127">Verwenden Sie lokale Außerkraftsetzungen, wenn Sie mit Änderungen an einer Webseite experimentieren möchten, und Sie müssen die Änderungen über alle Webseitenlasten hinweg anzeigen. Es ist ihnen jedoch nicht egal, ob Sie Ihre Änderungen dem Quellcode der Webseite zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="89bfa-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="89bfa-128">Schritt 1: Einrichten</span><span class="sxs-lookup"><span data-stu-id="89bfa-128">Step 1: Set up</span></span>  

<span data-ttu-id="89bfa-129">Führen Sie die folgenden Aktionen aus, um praktische Erfahrungen mit Arbeitsbereichen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="89bfa-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="89bfa-130">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="89bfa-130">Set up the demo</span></span>  

1.  <span data-ttu-id="89bfa-131">[Öffnen Sie die Demo][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="89bfa-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Ein Glitch-Projekt" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="89bfa-133">Ein Glitch-Projekt</span><span class="sxs-lookup"><span data-stu-id="89bfa-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="89bfa-134">Erstellen Sie `app` ein Verzeichnis auf Ihrem Desktop.</span><span class="sxs-lookup"><span data-stu-id="89bfa-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="89bfa-135">Speichern Sie Kopien der Dateien aus dem `workspaces-demo` Verzeichnis in das `app` Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="89bfa-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="89bfa-136">Für den Rest des Lernprogramms wird das Verzeichnis als `~/Desktop/app` bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="89bfa-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="89bfa-137">Starten Eines lokalen Webservers in `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="89bfa-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="89bfa-138">Im Folgenden finden Sie einige Beispielcode zum Starten, aber Sie können den von Ihnen `SimpleHTTPServer` bevorzugten Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="89bfa-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="89bfa-139">Öffnen Sie eine Registerkarte in Microsoft Edge, und navigieren Sie zur lokal gehosteten Version der Website.</span><span class="sxs-lookup"><span data-stu-id="89bfa-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="89bfa-140">Sie sollten über eine URL wie oder darauf `localhost:8080` zugreifen `http://0.0.0.0:8080` können.</span><span class="sxs-lookup"><span data-stu-id="89bfa-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="89bfa-141">Die genaue [Portnummer][WikiPortURLs] kann unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="89bfa-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Die Demo" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="89bfa-143">Die Demo</span><span class="sxs-lookup"><span data-stu-id="89bfa-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="89bfa-144">Einrichten von DevTools</span><span class="sxs-lookup"><span data-stu-id="89bfa-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="89bfa-145">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um den **Konsolenbereich** von DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="89bfa-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Konsolenbereich" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="89bfa-147">**Konsolenbereich**</span><span class="sxs-lookup"><span data-stu-id="89bfa-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-148">Navigieren Sie zum **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-148">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="89bfa-149">Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Dateisystem** aus.</span><span class="sxs-lookup"><span data-stu-id="89bfa-149">In the **Navigator** pane (on the left), choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Registerkarte Filesystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="89bfa-151">Registerkarte **Filesystem**</span><span class="sxs-lookup"><span data-stu-id="89bfa-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-152">Wählen **Sie Ordner zum Arbeitsbereich hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="89bfa-153">Geben Sie `~/Desktop/app` ein.</span><span class="sxs-lookup"><span data-stu-id="89bfa-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="89bfa-154">Wählen **Sie Zulassen** aus, um DevTools die Berechtigung zum Lesen und Schreiben in das Verzeichnis zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="89bfa-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="89bfa-155">Auf der **Registerkarte Dateisystem** wird nun neben , und ein grüner `index.html` Punkt `script.js` `styles.css` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89bfa-155">In the **Filesystem** tab, a green dot now appears next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="89bfa-156">Ein grüner Punkt gibt an, dass DevTools eine Zuordnung zwischen einer Netzwerkressource der Seite und der Datei in eingerichtet `~/Desktop/app` hat.</span><span class="sxs-lookup"><span data-stu-id="89bfa-156">A green dot indicates that DevTools has established a mapping between a network resource of the page, and the file in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Die Registerkarte Dateisystem zeigt jetzt eine Zuordnung zwischen den lokalen Dateien und den Netzwerkdateien an." lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="89bfa-158">Die **Registerkarte Dateisystem** zeigt jetzt eine Zuordnung zwischen den lokalen Dateien und den Netzwerkdateien an.</span><span class="sxs-lookup"><span data-stu-id="89bfa-158">The **Filesystem** tab now indicates a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="89bfa-159">Schritt 2: Speichern einer CSS-Änderung auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="89bfa-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="89bfa-160">Öffnen Sie `styles.css`.</span><span class="sxs-lookup"><span data-stu-id="89bfa-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="89bfa-161">Die `color` Eigenschaft von Elementen ist auf `h1` `fuchsia` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89bfa-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Styles.css in einem Texteditor anzeigen" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="89bfa-163">Anzeigen `styles.css` in einem Texteditor</span><span class="sxs-lookup"><span data-stu-id="89bfa-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-164">Wählen Sie das **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="89bfa-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="89bfa-165">Ändern Sie den Wert der `color` Eigenschaft des Elements in Ihre Bevorzugte `<h1>` Farbe.</span><span class="sxs-lookup"><span data-stu-id="89bfa-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="89bfa-166">Denken Sie daran, dass Sie das Element in der DOM-Struktur auswählen müssen, um die darauf angewendeten CSS-Regeln im Bereich `<h1>` **Formatvorlagen anzuzeigen.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="89bfa-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="89bfa-167">Der grüne Punkt neben `styles.css:1` bedeutet, dass alle änderungen, die Sie machen, zugeordnet `~/Desktop/app/styles.css` werden.</span><span class="sxs-lookup"><span data-stu-id="89bfa-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Der grüne Indikator, dass die Datei verknüpft ist" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="89bfa-169">Der grüne Indikator, dass die Datei verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="89bfa-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-170">Öffnen `styles.css` Sie erneut in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="89bfa-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="89bfa-171">Die `color` Eigenschaft wird nun auf Ihre bevorzugte Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89bfa-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="89bfa-172">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89bfa-172">Refresh the page.</span></span>  <span data-ttu-id="89bfa-173">Die Farbe des Elements `<h1>` ist weiterhin auf Ihre Bevorzugte Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89bfa-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="89bfa-174">Die Änderung bleibt bei einer Aktualisierung erhalten, da devTools die Änderung bei der Änderung auf dem Datenträger gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="89bfa-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="89bfa-175">Und dann, wenn Sie die Seite aktualisiert haben, hat Ihr lokaler Server die geänderte Kopie der Datei vom Datenträger aus bedient.</span><span class="sxs-lookup"><span data-stu-id="89bfa-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="89bfa-176">Schritt 3: Speichern einer HTML-Änderung auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="89bfa-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="89bfa-177">Ändern von HTML aus dem Elementbereich</span><span class="sxs-lookup"><span data-stu-id="89bfa-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="89bfa-178">Sie können änderungen am HTML aus dem Elementbereich vornehmen, aber Ihre Änderungen an der DOM-Struktur werden nicht auf dem Datenträger gespeichert und wirken sich nur auf die aktuelle Browsersitzung aus.</span><span class="sxs-lookup"><span data-stu-id="89bfa-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="89bfa-179">Die DOM-Struktur ist nicht html.</span><span class="sxs-lookup"><span data-stu-id="89bfa-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-tool"></a><span data-ttu-id="89bfa-180">Ändern von HTML aus dem Sources-Tool</span><span class="sxs-lookup"><span data-stu-id="89bfa-180">Change HTML from the Sources tool</span></span>  

<span data-ttu-id="89bfa-181">Wenn Sie eine Änderung am HTML der Webseite speichern möchten, verwenden Sie das **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-181">If you want to save a change to the HTML of the webpage, use the **Sources** tool.</span></span>  

1.  <span data-ttu-id="89bfa-182">Navigieren Sie zum **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-182">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="89bfa-183">Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="89bfa-183">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="89bfa-184">Wählen **Sie (Index)** aus.</span><span class="sxs-lookup"><span data-stu-id="89bfa-184">Choose **(index)**.</span></span>  <span data-ttu-id="89bfa-185">Der HTML-Code für die Seite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="89bfa-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="89bfa-186">Ersetzen Sie `<h1>Workspaces Demo</h1>` durch `<h1>I ❤️  Cake</h1>`.</span><span class="sxs-lookup"><span data-stu-id="89bfa-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="89bfa-187">Überprüfen Sie die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="89bfa-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="89bfa-188">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="89bfa-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="89bfa-189">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89bfa-189">Refresh the page.</span></span>  <span data-ttu-id="89bfa-190">Das `<h1>` Element zeigt den neuen Text weiterhin an, nachdem die Seite aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89bfa-190">The `<h1>` element continues to display the new text after the page is refreshed.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Ändern von HTML aus dem Sources-Tool" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="89bfa-192">Ändern von HTML aus dem **Sources-Tool**</span><span class="sxs-lookup"><span data-stu-id="89bfa-192">Change HTML from the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-193">Öffnen Sie `~/Desktop/app/index.html`.</span><span class="sxs-lookup"><span data-stu-id="89bfa-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="89bfa-194">Das `<h1>` Element enthält den neuen Text.</span><span class="sxs-lookup"><span data-stu-id="89bfa-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="89bfa-195">Schritt 4: Speichern einer JavaScript-Änderung auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="89bfa-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="89bfa-196">Der Hauptort für die Verwendung des Code-Editors von DevTools ist das **Sources-Tool.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-196">The main place to use the code editor of DevTools is the **Sources** tool.</span></span>  <span data-ttu-id="89bfa-197">Manchmal müssen Sie jedoch beim Bearbeiten von Dateien \*\*\*\* auf andere Tools zugreifen, z. B. auf das **Elementtool** oder den Konsolenbereich.</span><span class="sxs-lookup"><span data-stu-id="89bfa-197">But sometimes you need to access other tools, such as the **Elements** tool or the **Console** panel, while editing files.</span></span>  <span data-ttu-id="89bfa-198">Mit **dem Tool Quick Source** erhalten Sie nur den Editor aus dem **Sources-Tool,** während jedes Tool geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="89bfa-198">The **Quick Source** tool gives you just the editor from the **Sources** tool, while any tool is open.</span></span>  

<span data-ttu-id="89bfa-199">Gehen Sie wie folgt vor, um den DevTools-Code-Editor zusammen mit anderen Tools zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="89bfa-199">To open the DevTools code editor alongside other tools, do the following:</span></span>  

1.  <span data-ttu-id="89bfa-200">Navigieren Sie zum **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-200">Navigate to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="89bfa-201">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="89bfa-201">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="89bfa-202">Das **Befehlsmenü** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="89bfa-202">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="89bfa-203">Geben `Quick Source` Sie ein, und wählen Sie **dann Schnellquelle anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="89bfa-203">Type `Quick Source`, and then choose **Show Quick Source**.</span></span>  <span data-ttu-id="89bfa-204">Am unteren Rand des DevTools-Fensters wird das **Quick Source-Tool** angezeigt, das den Inhalt von angibt, der die letzte Datei ist, die Sie im Tool `index.html` Quellen **bearbeitet** haben.</span><span class="sxs-lookup"><span data-stu-id="89bfa-204">At the bottom of the DevTools window, the **Quick Source** tool appears, displaying the contents of `index.html`, which is the last file you edited in the **Sources** tool.</span></span>    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Öffnen Des Schnellquellentools mithilfe des Befehlsmenüs" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="89bfa-206">Öffnen Des **Schnellquellentools** mithilfe des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="89bfa-206">Open the **Quick Source** tool by using the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="89bfa-207">Wählen `Control` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) \*\*\*\* aus, um das Dialogfeld Datei öffnen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="89bfa-207">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="89bfa-208">Überprüfen Sie die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="89bfa-208">Review the following figure.</span></span>  
1.  <span data-ttu-id="89bfa-209">Geben `script` Sie ein, und wählen Sie **dann app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="89bfa-209">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Öffnen script.js mithilfe des Dialogfelds Datei öffnen" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="89bfa-211">Öffnen `script.js` mithilfe des **Dialogfelds Datei** öffnen</span><span class="sxs-lookup"><span data-stu-id="89bfa-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="89bfa-212">Der `Save Changes To Disk With Workspaces` Link in der Demo wird regelmäßig stylet.</span><span class="sxs-lookup"><span data-stu-id="89bfa-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="89bfa-213">Fügen Sie den folgenden Code am Ende der **script.js** mithilfe des **Quick Source-Tools** hinzu.</span><span class="sxs-lookup"><span data-stu-id="89bfa-213">Add the following code to the bottom of **script.js** using the **Quick Source** tool.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="89bfa-214">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="89bfa-214">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="89bfa-215">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89bfa-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="89bfa-216">Der Link auf der Seite ist jetzt italisiert.</span><span class="sxs-lookup"><span data-stu-id="89bfa-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Der Link auf der Seite ist jetzt italisiert" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="89bfa-218">Der Link auf der Seite ist jetzt italisiert</span><span class="sxs-lookup"><span data-stu-id="89bfa-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="89bfa-219">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="89bfa-219">Next steps</span></span>  

<span data-ttu-id="89bfa-220">Verwenden Sie das, was Sie in diesem Lernprogramm gelernt haben, um Arbeitsbereiche in Ihrem eigenen Projekt zu einrichten.</span><span class="sxs-lookup"><span data-stu-id="89bfa-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="89bfa-221">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="89bfa-221">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arbeitsbereiche Demodateien | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content – CSS: Cascading StyleSheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Erste Schritte mit der | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ausführen eines einfachen lokalen HTTP-| MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in DOM – Web-APIs | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Eine Einführung in Karten | Treehouse-Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(Computernetzwerk\) – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="89bfa-230">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89bfa-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="89bfa-231">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="89bfa-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="89bfa-233">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="89bfa-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
