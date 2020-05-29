---
title: Bearbeiten von Dateien mit Arbeitsbereichen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601852"
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







# <span data-ttu-id="a91a8-103">Bearbeiten von Dateien mit Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="a91a8-103">Edit Files With Workspaces</span></span>   



> [!NOTE]
> <span data-ttu-id="a91a8-104">Das Ziel dieses Lernprogramms ist es, praktische Übungen beim Einrichten und Verwenden von Arbeitsbereichen bereitzustellen, damit Sie Arbeitsbereiche in ihren eigenen Projekten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a91a8-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="a91a8-105">Sie können die Änderungen am Quellcode auf dem lokalen Computer, den Sie in devtools vorgenommen haben, nach dem Aktivieren von Arbeitsbereichen speichern.</span><span class="sxs-lookup"><span data-stu-id="a91a8-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="a91a8-106">**Voraussetzungen**: bevor Sie dieses Lernprogramm starten, sollten Sie wissen, wie Sie:</span><span class="sxs-lookup"><span data-stu-id="a91a8-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="a91a8-107">Verwenden von HTML, CSS und JavaScript zum Erstellen einer Webseite</span><span class="sxs-lookup"><span data-stu-id="a91a8-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="a91a8-108">Verwenden von devtools zum vornehmen grundlegender Änderungen an CSS</span><span class="sxs-lookup"><span data-stu-id="a91a8-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="a91a8-109">Ausführen eines lokalen http-Webservers</span><span class="sxs-lookup"><span data-stu-id="a91a8-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="a91a8-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a91a8-110">Overview</span></span>   

<span data-ttu-id="a91a8-111">Mit Arbeitsbereichen können Sie eine in devtools vorgenommene Änderung auf eine lokale Kopie der gleichen Datei auf Ihrem Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="a91a8-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="a91a8-112">Nehmen wir beispielsweise an:</span><span class="sxs-lookup"><span data-stu-id="a91a8-112">For example, suppose:</span></span>  

*   <span data-ttu-id="a91a8-113">Sie haben den Quellcode für Ihre Website auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="a91a8-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="a91a8-114">Sie führen einen lokalen Webserver aus dem Quellcodeverzeichnis aus, damit auf die Website zugegriffen werden kann `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="a91a8-115">Sie `localhost:8080` haben in Microsoft Edge geöffnet, und Sie verwenden devtools, um das CSS der Website zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a91a8-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="a91a8-116">Wenn Arbeitsbereiche aktiviert sind, werden die CSS-Änderungen, die Sie in devtools vornehmen, im Quellcode auf dem Desktop gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a91a8-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="a91a8-117">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a91a8-117">Limitations</span></span>   

<span data-ttu-id="a91a8-118">Wenn Sie ein modernes Framework verwenden, wird der Quellcode wahrscheinlich aus einem Format umgewandelt, das in einem für die Ausführung so schnell wie möglich optimierten Format verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a91a8-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="a91a8-119">Arbeitsbereiche können den optimierten Code normalerweise mit Hilfe von [Quell Karten][TreehouseBlogSourceMaps]Ihrem ursprünglichen Quellcode wieder zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="a91a8-120">Es gibt jedoch viele Unterschiede zwischen Frameworks darüber, wie Sie Quell Karten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a91a8-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="a91a8-121">Devtools unterstützt einfach alle Variationen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-121">Devtools simply does support all the variations.</span></span>  

<span data-ttu-id="a91a8-122">Arbeitsbereiche funktionieren in diesen Frameworks bekanntermaßen nicht:</span><span class="sxs-lookup"><span data-stu-id="a91a8-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="a91a8-123">Erstellen einer Reaktions-App</span><span class="sxs-lookup"><span data-stu-id="a91a8-123">Create React App</span></span>  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## <span data-ttu-id="a91a8-124">Verwandtes Feature: lokale Überschreibungen</span><span class="sxs-lookup"><span data-stu-id="a91a8-124">Related feature: Local Overrides</span></span>   

<span data-ttu-id="a91a8-125">**Lokale Außerkraftsetzungen** ist ein weiteres devtools-Feature, das mit Arbeitsbereichen vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="a91a8-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="a91a8-126">Verwenden Sie lokale Außerkraftsetzungen, wenn Sie mit Änderungen an einer Seite experimentieren möchten, und Sie diese Änderungen über die Seitenlasten hinweg anzeigen müssen, es Ihnen aber nicht wichtig ist, Ihre Änderungen dem Quellcode der Seite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="a91a8-127">Schritt 1: Einrichten</span><span class="sxs-lookup"><span data-stu-id="a91a8-127">Step 1: Setup</span></span>   

<span data-ttu-id="a91a8-128">Führen Sie dieses Lernprogramm aus, um praktische Erfahrungen mit Arbeitsbereichen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a91a8-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="a91a8-129">Einrichten der Demo</span><span class="sxs-lookup"><span data-stu-id="a91a8-129">Set up the demo</span></span>   

1.  <span data-ttu-id="a91a8-130">[Öffnen Sie die Demo][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="a91a8-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### <span data-ttu-id="a91a8-131">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="a91a8-131">Figure 1</span></span>  
    > <span data-ttu-id="a91a8-132">Ein glitch-Projekt ![ ein glitch-Projekt][ImageGlitchProject]</span><span class="sxs-lookup"><span data-stu-id="a91a8-132">A Glitch project ![A Glitch project][ImageGlitchProject]</span></span>  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="a91a8-133">Erstellen `app` Sie ein Verzeichnis auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="a91a8-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="a91a8-134">Speichern Sie Kopien der Dateien im `workspaces-demo` Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="a91a8-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="a91a8-135">Im weiteren Verlauf dieses Lernprogramms wird dieses Verzeichnis als bezeichnet `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="a91a8-136">Starten Sie einen lokalen Webserver in `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="a91a8-137">Nachfolgend finden Sie einige Beispielcodes zum Starten `SimpleHTTPServer` , aber Sie können den von Ihnen bevorzugten Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="a91a8-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  <span data-ttu-id="a91a8-138">Öffnen Sie eine Registerkarte in Microsoft Edge, und wechseln Sie zu der lokal gehosteten Version der Website.</span><span class="sxs-lookup"><span data-stu-id="a91a8-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="a91a8-139">Sie sollten in der Lage sein, auf Sie über eine URL wie oder zu zugreifen `localhost:8080` `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="a91a8-140">Die genaue [Portnummer][WikiPortURLs] kann unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="a91a8-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-141">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="a91a8-141">Figure 2</span></span>  
    > <span data-ttu-id="a91a8-142">Die Demo</span><span class="sxs-lookup"><span data-stu-id="a91a8-142">The demo</span></span>  
    > <span data-ttu-id="a91a8-143">! [Demo] [Imagedemo]</span><span class="sxs-lookup"><span data-stu-id="a91a8-143">![The demo][ImageDemo]</span></span>  

### <span data-ttu-id="a91a8-144">Einrichten von devtools</span><span class="sxs-lookup"><span data-stu-id="a91a8-144">Set up DevTools</span></span>   

1.  <span data-ttu-id="a91a8-145">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um die **Konsolen** Leiste von devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-146">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="a91a8-146">Figure 3</span></span>  
    > <span data-ttu-id="a91a8-147">Die **Konsolen** Leiste</span><span class="sxs-lookup"><span data-stu-id="a91a8-147">The **Console** panel</span></span>  
    > <span data-ttu-id="a91a8-148">! [Konsolenfeld] [ImageConsolePanel]</span><span class="sxs-lookup"><span data-stu-id="a91a8-148">![The Console panel][ImageConsolePanel]</span></span>  

1.  <span data-ttu-id="a91a8-149">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-149">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="a91a8-150">Klicken Sie auf die Registerkarte **Dateisystem** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-150">Click the **Filesystem** tab.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-151">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="a91a8-151">Figure 4</span></span>  
    > <span data-ttu-id="a91a8-152">Die Registerkarte " **Dateisystem** "</span><span class="sxs-lookup"><span data-stu-id="a91a8-152">The **Filesystem** tab</span></span>  
    > <span data-ttu-id="a91a8-153">! [Die Registerkarte ' Dateisystem '] [Imagefilesystem]</span><span class="sxs-lookup"><span data-stu-id="a91a8-153">![The Filesystem tab][ImageFilesystem]</span></span>  

1.  <span data-ttu-id="a91a8-154">Klicken Sie auf **Ordner zum Arbeitsbereich hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a91a8-154">Click **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="a91a8-155">Wählen Sie aus `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-155">Select `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="a91a8-156">Klicken Sie auf **zulassen** , um devtools die Berechtigung zum Lesen und Schreiben in das Verzeichnis zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-156">Click **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="a91a8-157">Auf der Registerkarte **Dateisystem** befindet sich nun ein grüner Punkt neben `index.html` , `script.js` und `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-157">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="a91a8-158">Diese grünen Punkte bedeuten, dass devtools eine Zuordnung zwischen den Netzwerkressourcen der Seite und den Dateien in erstellt hat `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-158">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-159">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="a91a8-159">Figure 5</span></span>  
    > <span data-ttu-id="a91a8-160">Die Registerkarte " **Dateisystem** " zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerk-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="a91a8-160">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    > <span data-ttu-id="a91a8-161">! [Die Registerkarte "Dateisystem" zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerken an.] [Imagemapping]</span><span class="sxs-lookup"><span data-stu-id="a91a8-161">![The Filesystem tab now shows a mapping between the local files and the network ones][ImageMapping]</span></span>  

## <span data-ttu-id="a91a8-162">Schritt 2: Speichern einer CSS-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="a91a8-162">Step 2: Save a CSS change to disk</span></span>   

1.  <span data-ttu-id="a91a8-163">Öffnen Sie `styles.css`.</span><span class="sxs-lookup"><span data-stu-id="a91a8-163">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="a91a8-164">Die `color` Eigenschaft von `h1` Elements ist auf gesetzt `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-164">The `color` property of `h1` elements is set to `fuchsia`.</span></span>
    
    > ##### <span data-ttu-id="a91a8-165">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="a91a8-165">Figure 6</span></span>  
    > <span data-ttu-id="a91a8-166">Anzeigen `styles.css` in einem Text-Editor</span><span class="sxs-lookup"><span data-stu-id="a91a8-166">Viewing `styles.css` in a text editor</span></span>  
    > <span data-ttu-id="a91a8-167">! [Anzeigen von Formatvorlagen. CSS in einem Text-Editor] [ImageStylesFuchsia]</span><span class="sxs-lookup"><span data-stu-id="a91a8-167">![Viewing styles.css in a text editor][ImageStylesFuchsia]</span></span>  


1.  <span data-ttu-id="a91a8-168">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-168">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="a91a8-169">Ändern Sie den Wert der `color` Eigenschaft des `<h1>` Elements in Ihre bevorzugte Farbe.</span><span class="sxs-lookup"><span data-stu-id="a91a8-169">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="a91a8-170">Beachten Sie, dass Sie auf das `<h1>` Element in der **DOM-Struktur** klicken müssen, um die darauf angewendeten CSS-Regeln im Bereich " **Formatvorlagen** " anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-170">Remember that you need to click the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="a91a8-171">Der grüne Punkt neben `styles.css:1` bedeutet, dass alle von Ihnen vorgenommenen Änderungen zugeordnet werden `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="a91a8-171">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-172">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="a91a8-172">Figure 7</span></span>  
    > <span data-ttu-id="a91a8-173">Der grüne Indikator, mit dem die Datei verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="a91a8-173">The green indicator that the file is linked</span></span>  
    > <span data-ttu-id="a91a8-174">! [Der grüne Indikator, dass die Datei verknüpft ist] [ImageStylesGreen]</span><span class="sxs-lookup"><span data-stu-id="a91a8-174">![The green indicator that the file is linked][ImageStylesGreen]</span></span>  

1.  <span data-ttu-id="a91a8-175">`styles.css`In einem Text-Editor erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-175">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="a91a8-176">Die `color` Eigenschaft ist nun auf Ihre Lieblingsfarbe eingestellt.</span><span class="sxs-lookup"><span data-stu-id="a91a8-176">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="a91a8-177">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="a91a8-177">Reload the page.</span></span>  <span data-ttu-id="a91a8-178">Die Farbe des `<h1>` Elements wird weiterhin auf Ihre bevorzugte Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a91a8-178">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="a91a8-179">Das funktioniert, weil devtools die Änderung auf dem Datenträger gespeichert hat, wenn Sie die Änderung vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="a91a8-179">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="a91a8-180">Und dann, als Sie die Seite neu geladen haben, diente der lokale Server der geänderten Kopie der Datei vom Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a91a8-180">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  

## <span data-ttu-id="a91a8-181">Schritt 3: Speichern einer HTML-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="a91a8-181">Step 3: Save an HTML change to disk</span></span>   

### <span data-ttu-id="a91a8-182">Ändern von HTML über das Panel "Elemente"</span><span class="sxs-lookup"><span data-stu-id="a91a8-182">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="a91a8-183">Sie können Änderungen am HTML-Code über das Element Panel vornehmen, Ihre Änderungen an der DOM-Struktur werden aber nicht auf dem Datenträger gespeichert und wirken sich nur auf die aktuelle Browsersitzung aus.</span><span class="sxs-lookup"><span data-stu-id="a91a8-183">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="a91a8-184">Die DOM-Struktur ist kein HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="a91a8-184">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### <span data-ttu-id="a91a8-185">Ändern von HTML aus dem Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="a91a8-185">Change HTML from the Sources panel</span></span>   

<span data-ttu-id="a91a8-186">Wenn Sie eine Änderung am HTML-Code der Seite speichern möchten, verwenden Sie das **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="a91a8-186">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="a91a8-187">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-187">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="a91a8-188">Klicken Sie auf die Registerkarte **Seite** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-188">Click the **Page** tab.</span></span>  
1.  <span data-ttu-id="a91a8-189">Klicken Sie auf **(Index)**.</span><span class="sxs-lookup"><span data-stu-id="a91a8-189">Click **(index)**.</span></span>  <span data-ttu-id="a91a8-190">Der HTML-Code für die Seite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a91a8-190">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="a91a8-191">Ersetzen Sie `<h1>Workspaces Demo</h1>` durch `<h1>I ❤️  Cake</h1>`.</span><span class="sxs-lookup"><span data-stu-id="a91a8-191">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="a91a8-192">Siehe [Abbildung 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="a91a8-192">See [Figure 8](#figure-8).</span></span>  
1.  <span data-ttu-id="a91a8-193">Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a91a8-193">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="a91a8-194">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="a91a8-194">Reload the page.</span></span>  <span data-ttu-id="a91a8-195">Das `<h1>` Element zeigt weiterhin den neuen Text an.</span><span class="sxs-lookup"><span data-stu-id="a91a8-195">The `<h1>` element is still displaying the new text.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-196">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="a91a8-196">Figure 8</span></span>  
    > <span data-ttu-id="a91a8-197">Zeile 12 wurde auf</span><span class="sxs-lookup"><span data-stu-id="a91a8-197">Line 12 has been set to</span></span> `I ❤️  Cake`  
    > <span data-ttu-id="a91a8-198">! [Ändern von HTML aus dem Quellen Panel] [ImageSourcesCakeHTML]</span><span class="sxs-lookup"><span data-stu-id="a91a8-198">![Changing HTML from the Sources panel][ImageSourcesCakeHTML]</span></span>  

1.  <span data-ttu-id="a91a8-199">Öffnen Sie `~/Desktop/app/index.html`.</span><span class="sxs-lookup"><span data-stu-id="a91a8-199">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="a91a8-200">Das `<h1>` Element enthält den neuen Text.</span><span class="sxs-lookup"><span data-stu-id="a91a8-200">The `<h1>` element contains the new text.</span></span>  

## <span data-ttu-id="a91a8-201">Schritt 4: Speichern einer JavaScript-Änderung auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="a91a8-201">Step 4: Save a JavaScript change to disk</span></span>   

<span data-ttu-id="a91a8-202">Der Bereich " **Quellen** " ist auch der Ort, an dem Sie Änderungen an JavaScript vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="a91a8-202">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="a91a8-203">Manchmal müssen Sie aber auch auf andere Panels zugreifen, beispielsweise auf das Panel **Elemente** oder den **Konsolen** Panel, während Sie Änderungen an Ihrer Website vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-203">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="a91a8-204">Es gibt eine Möglichkeit, das **Quellen** Panel parallel zu anderen Panels zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-204">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="a91a8-205">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="a91a8-205">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="a91a8-206">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="a91a8-206">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="a91a8-207">Das **Befehlsmenü** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a91a8-207">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="a91a8-208">Geben `QS` Sie ein, und wählen Sie dann **schnell Quelle anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="a91a8-208">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="a91a8-209">Am unteren Rand des devtools-Fensters befindet sich nun eine **schnell Ausgangs** Registerkarte.  Auf der Registerkarte wird der Inhalt von angezeigt `index.html` , die letzte Datei, die Sie im **Quellen** Panel bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="a91a8-209">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="a91a8-210">Auf der Registerkarte " **schnell Quelle** " finden Sie den Editor im **Quellen** Panel, sodass Sie Dateien bearbeiten können, während andere Panels geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="a91a8-210">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-211">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="a91a8-211">Figure 9</span></span>  
    > <span data-ttu-id="a91a8-212">Öffnen der Registerkarte " **schnell** Start" über das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="a91a8-212">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    > <span data-ttu-id="a91a8-213">! [Öffnen der Registerkarte ' schnell Quelle ' mithilfe des Befehlsmenüs] [ImageCommandMenuQuickSource]</span><span class="sxs-lookup"><span data-stu-id="a91a8-213">![Opening the Quick Source tab using Command Menu][ImageCommandMenuQuickSource]</span></span>  

1.  <span data-ttu-id="a91a8-214">Drücken Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \), um das Dialogfeld **Datei öffnen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a91a8-214">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="a91a8-215">Siehe [Abbildung 10](#figure-10).</span><span class="sxs-lookup"><span data-stu-id="a91a8-215">See [Figure 10](#figure-10).</span></span>  
1.  <span data-ttu-id="a91a8-216">Geben `script` Sie ein, und wählen Sie dann **App/Script. js**aus.</span><span class="sxs-lookup"><span data-stu-id="a91a8-216">Type `script`, then select **app/script.js**.</span></span>  
    
    > ##### <span data-ttu-id="a91a8-217">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="a91a8-217">Figure 10</span></span>  
    > <span data-ttu-id="a91a8-218">Öffnen `script.js` mithilfe des Dialogfelds " **Datei öffnen** "</span><span class="sxs-lookup"><span data-stu-id="a91a8-218">Opening `script.js` using the **Open File** dialog</span></span>  
    > <span data-ttu-id="a91a8-219">! [Öffnen von "Script. js" im Dialogfeld "Datei öffnen"] [ImageOpenFileDialog]</span><span class="sxs-lookup"><span data-stu-id="a91a8-219">![Opening script.js using the Open File dialog][ImageOpenFileDialog]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a91a8-220">Der `Save Changes To Disk With Workspaces` Link in der Demo wird regelmäßig gestaltet.</span><span class="sxs-lookup"><span data-stu-id="a91a8-220">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="a91a8-221">Fügen Sie den folgenden Code am Ende von **Skript. js** mithilfe der Registerkarte **schnell** Zugriff hinzu.</span><span class="sxs-lookup"><span data-stu-id="a91a8-221">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="a91a8-222">Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a91a8-222">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="a91a8-223">Laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="a91a8-223">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a91a8-224">Der Link auf der Seite ist jetzt kursiv.</span><span class="sxs-lookup"><span data-stu-id="a91a8-224">The link on the page is now italic.</span></span>
    
    > ##### <span data-ttu-id="a91a8-225">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="a91a8-225">Figure 11</span></span>  
    > <span data-ttu-id="a91a8-226">Der Link auf der Seite ist jetzt kursiv</span><span class="sxs-lookup"><span data-stu-id="a91a8-226">The link on the page is now italic</span></span>  
    > <span data-ttu-id="a91a8-227">! [Der Link auf der Seite ist jetzt kursiv] [ImageScriptItalic]</span><span class="sxs-lookup"><span data-stu-id="a91a8-227">![The link on the page is now italic][ImageScriptItalic]</span></span>  

## <span data-ttu-id="a91a8-228">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a91a8-228">Next steps</span></span>   

<span data-ttu-id="a91a8-229">Verwenden Sie das gelernte in diesem Lernprogramm, um Arbeitsbereiche in Ihrem eigenen Projekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a91a8-229">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Abbildung 1: ein glitch-Projekt mit einem zufällig generierten Namen"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[Imagedemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo.msft.png "Abbildung 2: die Demo"
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo.msft.png "Figure 2: The demo"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Console.msft.png "Abbildung 3: die Konsolen Leiste"  
[Imagefilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem.msft.png "Abbildung 4: die Registerkarte" Dateisystem "
[ImageFilesystem]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-sources-filesystem.msft.png "Figure 4: The Filesystem tab"  
[Imagemapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-Folder.msft.png "Abbildung 5: die Registerkarte" Dateisystem "zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerken an."
[ImageMapping]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png "Figure 5: The Filesystem tab now shows a mapping between the local files and the network ones"  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-CSS.msft.png "Abbildung 6: Anzeigen von Formatvorlagen. CSS in einem Text-Editor"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-Styles-CSS.msft.png "Abbildung 7: der grüne Indikator, mit dem die Datei verknüpft ist"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-Page-H1.msft.png "Abbildung 8: Ändern von HTML aus dem Quellen Panel"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Show-Quick-Source.msft.png "Abbildung 9: Öffnen der Registerkarte" Schnellstart "mit dem Befehlsmenü"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Script.msft.png "Abbildung 10: Öffnen von" Script. js "im Dialogfeld" Datei öffnen "  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-Styles-Quick-Source-Script.msft.png "Abbildung 11: der Link auf der Seite ist jetzt kursiv"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte beim Anzeigen und Ändern von CSS"  

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
> <span data-ttu-id="a91a8-249">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a91a8-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a91a8-250">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a91a8-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="a91a8-252">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a91a8-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
