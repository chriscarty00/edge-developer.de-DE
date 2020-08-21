---
title: Bearbeiten von Dateien mit Arbeitsbereichen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8a31dd9fbfe492cf8eaacc654f7d501925f730f2
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942177"
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

# <span data-ttu-id="029ae-103">Bearbeiten von Dateien mit Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="029ae-103">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="029ae-104">Das Ziel dieses Lernprogramms ist es, praktische Übungen beim Einrichten und Verwenden von Arbeitsbereichen bereitzustellen, damit Sie Arbeitsbereiche in ihren eigenen Projekten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="029ae-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="029ae-105">Sie können die Änderungen am Quellcode auf dem lokalen Computer, den Sie in devtools vorgenommen haben, nach dem Aktivieren von Arbeitsbereichen speichern.</span><span class="sxs-lookup"><span data-stu-id="029ae-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="029ae-106">**Voraussetzungen**: bevor Sie dieses Lernprogramm starten, sollten Sie wissen, wie die folgenden Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="029ae-106">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="029ae-107">Verwenden von HTML, CSS und JavaScript zum Erstellen einer Webseite</span><span class="sxs-lookup"><span data-stu-id="029ae-107">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="029ae-108">Verwenden von devtools zum vornehmen grundlegender Änderungen an CSS</span><span class="sxs-lookup"><span data-stu-id="029ae-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="029ae-109">Ausführen eines lokalen http-Webservers</span><span class="sxs-lookup"><span data-stu-id="029ae-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="029ae-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="029ae-110">Overview</span></span>  

<span data-ttu-id="029ae-111">Mit Arbeitsbereichen können Sie eine in devtools vorgenommene Änderung auf eine lokale Kopie der gleichen Datei auf Ihrem Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="029ae-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="029ae-112">In diesem Lernprogramm sollten Sie über die folgenden Einstellungen auf Ihrem Computer verfügen.</span><span class="sxs-lookup"><span data-stu-id="029ae-112">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="029ae-113">Sie haben den Quellcode für Ihre Website auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="029ae-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="029ae-114">Sie führen einen lokalen Webserver aus dem Quellcodeverzeichnis aus, damit auf die Website zugegriffen werden kann `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="029ae-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="029ae-115">Sie `localhost:8080` haben in Microsoft Edge geöffnet, und Sie verwenden devtools, um das CSS der Website zu ändern.</span><span class="sxs-lookup"><span data-stu-id="029ae-115">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="029ae-116">Wenn Arbeitsbereiche aktiviert sind, werden die CSS-Änderungen, die Sie in devtools vornehmen, im Quellcode auf dem Desktop gespeichert.</span><span class="sxs-lookup"><span data-stu-id="029ae-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="029ae-117">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="029ae-117">Limitations</span></span>  

<span data-ttu-id="029ae-118">Wenn Sie ein modernes Framework verwenden, wird der Quellcode wahrscheinlich aus einem Format umgewandelt, das in einem für die Ausführung so schnell wie möglich optimierten Format verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="029ae-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="029ae-119">Arbeitsbereiche können den optimierten Code normalerweise mit Hilfe von [Quell Karten][TreehouseBlogSourceMaps]Ihrem ursprünglichen Quellcode wieder zuordnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="029ae-120">Es gibt jedoch viele Unterschiede zwischen Frameworks darüber, wie die einzelnen Quell Karten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="029ae-120">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="029ae-121">Devtools unterstützt einfach alle Variationen.</span><span class="sxs-lookup"><span data-stu-id="029ae-121">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="029ae-122">Arbeitsbereiche funktionieren bekanntermaßen nicht mit dem folgenden Framework.</span><span class="sxs-lookup"><span data-stu-id="029ae-122">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="029ae-123">Erstellen einer Reaktions-App</span><span class="sxs-lookup"><span data-stu-id="029ae-123">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="029ae-124">Verwandtes Feature: lokale Überschreibungen</span><span class="sxs-lookup"><span data-stu-id="029ae-124">Related feature: Local overrides</span></span>  

<span data-ttu-id="029ae-125">**Lokale Außerkraftsetzungen** ist ein weiteres devtools-Feature, das mit Arbeitsbereichen vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="029ae-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="029ae-126">Verwenden Sie lokale Außerkraftsetzungen, wenn Sie mit Änderungen an einer Seite experimentieren möchten, und Sie müssen die Änderungen über die Seitenlasten hinweg anzeigen, aber es ist Ihnen nicht wichtig, Ihre Änderungen dem Quellcode der Seite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see the changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="029ae-127">Schritt 1: Einrichten</span><span class="sxs-lookup"><span data-stu-id="029ae-127">Step 1: Set up</span></span>  

<span data-ttu-id="029ae-128">Führen Sie die folgenden Aktionen aus, um praktische Erfahrungen mit Arbeitsbereichen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="029ae-128">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="029ae-129">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="029ae-129">Set up the demo</span></span>  

1.  <span data-ttu-id="029ae-130">[Öffnen Sie die Demo][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="029ae-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Ein glitch-Projekt" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="029ae-132">Ein glitch-Projekt</span><span class="sxs-lookup"><span data-stu-id="029ae-132">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="029ae-133">Erstellen `app` Sie ein Verzeichnis auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="029ae-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="029ae-134">Speichern Sie Kopien der Dateien aus dem `workspaces-demo` Verzeichnis im `app` Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="029ae-134">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="029ae-135">Für den restlichen Teil des Lernprogramms wird das Verzeichnis als bezeichnet `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="029ae-135">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="029ae-136">Starten Sie einen lokalen Webserver in `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="029ae-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="029ae-137">Nachfolgend finden Sie einige Beispielcodes zum Starten `SimpleHTTPServer` , aber Sie können den von Ihnen bevorzugten Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="029ae-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="029ae-138">Öffnen Sie eine Registerkarte in Microsoft Edge, und wechseln Sie zu der lokal gehosteten Version der Website.</span><span class="sxs-lookup"><span data-stu-id="029ae-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="029ae-139">Sie sollten in der Lage sein, auf Sie über eine URL wie oder zu zugreifen `localhost:8080` `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="029ae-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="029ae-140">Die genaue [Portnummer][WikiPortURLs] kann unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="029ae-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Die Demo" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="029ae-142">Die Demo</span><span class="sxs-lookup"><span data-stu-id="029ae-142">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="029ae-143">Einrichten von devtools</span><span class="sxs-lookup"><span data-stu-id="029ae-143">Set up DevTools</span></span>  

1.  <span data-ttu-id="029ae-144">Wählen Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) aus, um die **Konsolen** Leiste von devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-144">Select `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="029ae-146">Die **Konsolen** Leiste</span><span class="sxs-lookup"><span data-stu-id="029ae-146">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-147">Wählen Sie die Registerkarte **Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-147">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="029ae-148">Wählen Sie die Registerkarte **Dateisystem** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-148">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Die Registerkarte "Dateisystem"" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="029ae-150">Die Registerkarte " **Dateisystem** "</span><span class="sxs-lookup"><span data-stu-id="029ae-150">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-151">Wählen Sie **Ordner zum Arbeitsbereich hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-151">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="029ae-152">Geben Sie `~/Desktop/app` ein.</span><span class="sxs-lookup"><span data-stu-id="029ae-152">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="029ae-153">Wählen Sie **zulassen** aus, um devtools die Berechtigung zum Lesen und Schreiben in das Verzeichnis zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="029ae-153">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="029ae-154">Auf der Registerkarte **Dateisystem** befindet sich nun ein grüner Punkt neben `index.html` , `script.js` und `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="029ae-154">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="029ae-155">Diese grünen Punkte bedeuten, dass devtools eine Zuordnung zwischen den Netzwerkressourcen der Seite und den Dateien in erstellt hat `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="029ae-155">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Die Registerkarte "Dateisystem" zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerk-Dateien an." lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="029ae-157">Die Registerkarte " **Dateisystem** " zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerk-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="029ae-157">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="029ae-158">Schritt 2: Speichern einer CSS-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="029ae-158">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="029ae-159">Öffnen Sie `styles.css`.</span><span class="sxs-lookup"><span data-stu-id="029ae-159">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="029ae-160">Die `color` Eigenschaft von `h1` Elements ist auf gesetzt `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="029ae-160">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Anzeigen von Formatvorlagen. CSS in einem Text-Editor" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="029ae-162">Anzeigen `styles.css` in einem Text-Editor</span><span class="sxs-lookup"><span data-stu-id="029ae-162">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-163">Wählen Sie die Registerkarte **Elemente** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-163">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="029ae-164">Ändern Sie den Wert der `color` Eigenschaft des `<h1>` Elements in Ihre bevorzugte Farbe.</span><span class="sxs-lookup"><span data-stu-id="029ae-164">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="029ae-165">Beachten Sie, dass Sie das `<h1>` Element in der **DOM-Struktur** auswählen müssen, um die darauf angewendeten CSS-Regeln im Bereich " **Formatvorlagen** " anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="029ae-165">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="029ae-166">Der grüne Punkt neben `styles.css:1` bedeutet, dass alle von Ihnen vorgenommenen Änderungen zugeordnet werden `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="029ae-166">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Der grüne Indikator, mit dem die Datei verknüpft ist" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="029ae-168">Der grüne Indikator, mit dem die Datei verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="029ae-168">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-169">`styles.css`In einem Text-Editor erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-169">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="029ae-170">Die `color` Eigenschaft ist nun auf Ihre Lieblingsfarbe eingestellt.</span><span class="sxs-lookup"><span data-stu-id="029ae-170">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="029ae-171">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="029ae-171">Refresh the page.</span></span>  <span data-ttu-id="029ae-172">Die Farbe des `<h1>` Elements wird weiterhin auf Ihre bevorzugte Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="029ae-172">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="029ae-173">Die Änderung bleibt über eine Aktualisierung bestehen, denn wenn Sie die Änderung vorgenommen haben, devtools die Änderung auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="029ae-173">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="029ae-174">Und dann, wenn Sie die Seite aktualisiert haben, hat der lokale Server die geänderte Kopie der Datei vom Datenträger bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="029ae-174">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="029ae-175">Schritt 3: Speichern einer HTML-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="029ae-175">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="029ae-176">Ändern von HTML über das Panel "Elemente"</span><span class="sxs-lookup"><span data-stu-id="029ae-176">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="029ae-177">Sie können Änderungen am HTML-Code über das Element Panel vornehmen, Ihre Änderungen an der DOM-Struktur werden aber nicht auf dem Datenträger gespeichert und wirken sich nur auf die aktuelle Browsersitzung aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-177">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="029ae-178">Die DOM-Struktur ist kein HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="029ae-178">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <span data-ttu-id="029ae-179">Ändern von HTML aus dem Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="029ae-179">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="029ae-180">Wenn Sie eine Änderung am HTML-Code der Seite speichern möchten, verwenden Sie das **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="029ae-180">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="029ae-181">Wählen Sie die Registerkarte **Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-181">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="029ae-182">Wählen Sie die Registerkarte **Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-182">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="029ae-183">Wählen Sie **(Index)** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-183">Choose **(index)**.</span></span>  <span data-ttu-id="029ae-184">Der HTML-Code für die Seite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="029ae-184">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="029ae-185">Ersetzen Sie `<h1>Workspaces Demo</h1>` durch `<h1>I ❤️  Cake</h1>`.</span><span class="sxs-lookup"><span data-stu-id="029ae-185">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="029ae-186">Sehen Sie sich die folgende Abbildung an.</span><span class="sxs-lookup"><span data-stu-id="029ae-186">See the following figure.</span></span>  
1.  <span data-ttu-id="029ae-187">Wählen Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \) aus, um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="029ae-187">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="029ae-188">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="029ae-188">Refresh the page.</span></span>  <span data-ttu-id="029ae-189">Das `<h1>` Element zeigt weiterhin den neuen Text an.</span><span class="sxs-lookup"><span data-stu-id="029ae-189">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Ändern von HTML aus dem Quellen Panel" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="029ae-191">Ändern von HTML aus dem **Quellen** Panel</span><span class="sxs-lookup"><span data-stu-id="029ae-191">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-192">Öffnen Sie `~/Desktop/app/index.html`.</span><span class="sxs-lookup"><span data-stu-id="029ae-192">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="029ae-193">Das `<h1>` Element enthält den neuen Text.</span><span class="sxs-lookup"><span data-stu-id="029ae-193">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="029ae-194">Schritt 4: Speichern einer JavaScript-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="029ae-194">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="029ae-195">Der Bereich " **Quellen** " ist auch der Ort, an dem Sie Änderungen an JavaScript vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="029ae-195">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="029ae-196">Manchmal müssen Sie aber auch auf andere Panels zugreifen, beispielsweise auf das Panel **Elemente** oder den **Konsolen** Panel, während Sie Änderungen an Ihrer Website vornehmen.</span><span class="sxs-lookup"><span data-stu-id="029ae-196">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="029ae-197">Es gibt eine Möglichkeit, das **Quellen** Panel parallel zu anderen Panels zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-197">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="029ae-198">Wählen Sie die Registerkarte **Elemente** aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-198">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="029ae-199">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-199">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="029ae-200">Das **Befehlsmenü** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="029ae-200">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="029ae-201">Geben `QS` Sie ein, und wählen Sie dann **schnell Quelle anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-201">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="029ae-202">Am unteren Rand des devtools-Fensters befindet sich nun eine **schnell Ausgangs** Registerkarte.  Auf der Registerkarte wird der Inhalt von angezeigt `index.html` , die letzte Datei, die Sie im **Quellen** Panel bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="029ae-202">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="029ae-203">Auf der Registerkarte " **schnell Quelle** " finden Sie den Editor im **Quellen** Panel, sodass Sie Dateien bearbeiten können, während andere Panels geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="029ae-203">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Öffnen der Registerkarte "Schnellstart" mithilfe des Befehlsmenüs" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="029ae-205">Öffnen der Registerkarte " **schnell** Start" mithilfe des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="029ae-205">Open the **Quick Source** tab using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="029ae-206">Wählen Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \) aus, um das Dialogfeld **Datei öffnen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="029ae-206">Select `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="029ae-207">Sehen Sie sich die folgende Abbildung an.</span><span class="sxs-lookup"><span data-stu-id="029ae-207">See the following figure.</span></span>  
1.  <span data-ttu-id="029ae-208">Geben `script` Sie ein, und wählen Sie dann \*\*App/#b0 \*\*aus.</span><span class="sxs-lookup"><span data-stu-id="029ae-208">Type `script`, then select **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Öffnen von script.js im Dialogfeld "Datei öffnen"" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="029ae-210">Öffnen `script.js` mithilfe des Dialogfelds " **Datei öffnen** "</span><span class="sxs-lookup"><span data-stu-id="029ae-210">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="029ae-211">Der `Save Changes To Disk With Workspaces` Link in der Demo wird regelmäßig gestaltet.</span><span class="sxs-lookup"><span data-stu-id="029ae-211">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="029ae-212">Fügen Sie den folgenden Code unten in **script.js** mithilfe der Registerkarte **schnell** Zugriff hinzu.</span><span class="sxs-lookup"><span data-stu-id="029ae-212">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="029ae-213">Wählen Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \) aus, um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="029ae-213">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="029ae-214">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="029ae-214">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="029ae-215">Der Link auf der Seite ist jetzt kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="029ae-215">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Der Link auf der Seite ist jetzt kursiv formatiert" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="029ae-217">Der Link auf der Seite ist jetzt kursiv formatiert</span><span class="sxs-lookup"><span data-stu-id="029ae-217">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="029ae-218">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="029ae-218">Next steps</span></span>  

<span data-ttu-id="029ae-219">Verwenden Sie das gelernte in diesem Lernprogramm, um Arbeitsbereiche in Ihrem eigenen Projekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="029ae-219">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
    -->  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Demo Dateien für Arbeitsbereiche | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Inhalt – CSS: Cascading Stylesheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Erste Schritte mit dem Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ausführen eines einfachen lokalen HTTP-Servers | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in DOM-Web-APIs | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Eine Einführung in Quell Karten | Baumhaus-Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \ (Computer Networking \) – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="029ae-228">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="029ae-228">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="029ae-229">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="029ae-229">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="029ae-231">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="029ae-231">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
