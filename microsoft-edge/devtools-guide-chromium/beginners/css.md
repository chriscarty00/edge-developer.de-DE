---
title: 'DevTools für Anfänger: Erste Schritte mit CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882737"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="b8df1-103">DevTools für Anfänger: Erste Schritte mit CSS</span><span class="sxs-lookup"><span data-stu-id="b8df1-103">DevTools for beginners: Get started with CSS</span></span>   

<span data-ttu-id="b8df1-104">In diesem Lernprogramm erfahren Sie, wie Sie eine Webseite mithilfe von CSS formatieren.</span><span class="sxs-lookup"><span data-stu-id="b8df1-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="b8df1-105">Sie erfahren auch, wie Sie Microsoft Edge devtools verwenden, um mit CSS-Änderungen zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="b8df1-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="b8df1-106">Dies ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in denen Sie die Grundlagen der Webentwicklung und der Microsoft Edge-devtools.</span><span class="sxs-lookup"><span data-stu-id="b8df1-106">This is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b8df1-107">Sie erhalten praktische Erfahrungen, wenn Sie tatsächlich ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="b8df1-108">Bevor Sie diesen Vorgang ausführen, müssen Sie das erste Lernprogramm nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-108">You don't have to complete the first tutorial before doing this one.</span></span>  <span data-ttu-id="b8df1-109">Sie können hier beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-109">You can start here.</span></span>  <span data-ttu-id="b8df1-110">[Einrichten Ihres Codes](#set-up-your-code) zeigt, wie Sie sich einrichten.</span><span class="sxs-lookup"><span data-stu-id="b8df1-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="b8df1-111">Dieses Lernprogramm ist für absolute Anfänger konzipiert und konzentriert sich sowohl auf die **Grundlagen der Webentwicklung** als auch auf die Grundlagen der Verwendung von devtools zum Experimentieren mit CSS.</span><span class="sxs-lookup"><span data-stu-id="b8df1-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="b8df1-112">Wenn Sie ein Lernprogramm benötigen, das sich nur auf devtools konzentriert, lesen Sie [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="b8df1-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="b8df1-113">Ihre Website sieht derzeit wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-113">Currently your site looks like this:</span></span>  

> ##### <span data-ttu-id="b8df1-114">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="b8df1-114">Figure 1</span></span>  
> <span data-ttu-id="b8df1-115">Wie Ihre Website aktuell aussieht</span><span class="sxs-lookup"><span data-stu-id="b8df1-115">What your site currently looks like</span></span>  
> ![Wie Ihre Website aktuell aussieht][ImageCssIntro1]  

<span data-ttu-id="b8df1-117">Nach Abschluss des Lernprogramms sieht es wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-117">After completing the tutorial, it will look like this:</span></span>  

> ##### <span data-ttu-id="b8df1-118">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="b8df1-118">Figure 2</span></span>  
> <span data-ttu-id="b8df1-119">Wie Ihre Website am Ende des Lernprogramms aussehen wird</span><span class="sxs-lookup"><span data-stu-id="b8df1-119">What your site will look like at the end of the tutorial</span></span>  
> ![Wie Ihre Website am Ende des Lernprogramms aussehen wird][ImageCssIntro2]  

## <span data-ttu-id="b8df1-121">Ziele</span><span class="sxs-lookup"><span data-stu-id="b8df1-121">Goals</span></span>   

<span data-ttu-id="b8df1-122">Am Ende dieses Lernprogramms können Sie Folgendes verstehen:</span><span class="sxs-lookup"><span data-stu-id="b8df1-122">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="b8df1-123">Verwenden von CSS zum Formatieren einer Webseite</span><span class="sxs-lookup"><span data-stu-id="b8df1-123">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="b8df1-124">Verwenden von Microsoft Edge devtools zum Experimentieren mit CSS</span><span class="sxs-lookup"><span data-stu-id="b8df1-124">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="b8df1-125">Der Unterschied zwischen CSS-und CSS-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="b8df1-125">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="b8df1-126">Sie haben auch eine echte Website!</span><span class="sxs-lookup"><span data-stu-id="b8df1-126">You'll also have a real website!</span></span>  

## <span data-ttu-id="b8df1-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b8df1-127">Prerequisites</span></span>   

<span data-ttu-id="b8df1-128">Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-128">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="b8df1-129">Führen Sie [die ersten Schritte mit HTML und dem Dom durch][DevToolsBeginnersHtml] , oder stellen Sie sicher, dass Sie ein Verständnis von HTML und dem Dom haben, das dem entspricht, was in diesem Lernprogramm unterrichtet wird.</span><span class="sxs-lookup"><span data-stu-id="b8df1-129">Complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what's taught in that tutorial.</span></span>  
*   <span data-ttu-id="b8df1-130">Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.</span><span class="sxs-lookup"><span data-stu-id="b8df1-130">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="b8df1-131">In diesem Lernprogramm wird eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, verwendet, die in Microsoft Edge integriert sind.</span><span class="sxs-lookup"><span data-stu-id="b8df1-131">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="b8df1-132">Einrichten Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="b8df1-132">Set up your code</span></span>   

<span data-ttu-id="b8df1-133">Um mit der Erstellung Ihrer Website zu beginnen, müssen Sie Ihren Code einrichten:</span><span class="sxs-lookup"><span data-stu-id="b8df1-133">In order to start creating your site, you need to set up your code:</span></span>  

1.  **<span data-ttu-id="b8df1-134">Wenn Sie das erste Lernprogramm in dieser Serie bereits abgeschlossen haben, überspringen Sie diesen Abschnitt!</span><span class="sxs-lookup"><span data-stu-id="b8df1-134">If you have already completed the first tutorial in this series, skip this section!</span></span>  <span data-ttu-id="b8df1-135">Verwenden Sie weiterhin ihren Code aus dem letzten Lernprogramm, [Erste Schritte mit HTML und dem Dom][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="b8df1-135">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>**  
1.  <span data-ttu-id="b8df1-136">Öffnen Sie den [Quellcode][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="b8df1-136">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="b8df1-137">Diese Registerkarte Ihres Browsers wird als **Registerkarte "Bearbeiten"** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-137">This tab of your browser will be called the **editing tab**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-138">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="b8df1-138">Figure 3</span></span>  
    > <span data-ttu-id="b8df1-139">Die Registerkarte ' bearbeiten '</span><span class="sxs-lookup"><span data-stu-id="b8df1-139">The editing tab</span></span>  
    > ![Die Registerkarte ' bearbeiten '][ImageCssSetup1]  
    
1.  <span data-ttu-id="b8df1-141">Klicken Sie auf **gekocht-Amphibien**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-141">Click **cooked-amphibian**.</span></span>  <span data-ttu-id="b8df1-142">Ein Menü wird eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-142">A menu pops up.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-143">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="b8df1-143">Figure 4</span></span>  
    > <span data-ttu-id="b8df1-144">Das Menü "Projektoptionen"</span><span class="sxs-lookup"><span data-stu-id="b8df1-144">The Project Options menu</span></span>  
    > ![Das Menü "Projektoptionen"][ImageCssSetup2]  

1.  <span data-ttu-id="b8df1-146">Klicken Sie auf **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-146">Click **Remix Project**.</span></span>  <span data-ttu-id="b8df1-147">Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="b8df1-147">Glitch creates a copy of the project that you can edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b8df1-148">Glitch generiert einen zufälligen Namen für das neue Projekt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-148">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="b8df1-149">Klicken Sie auf **anzeigen** , und wählen Sie **in einem neuen Fenster**aus.</span><span class="sxs-lookup"><span data-stu-id="b8df1-149">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="b8df1-150">Eine andere Registerkarte wird mit einer Live Ansicht Ihrer Website geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-150">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="b8df1-151">Dieser Reiter Ihres Browsers wird als **"Live"-Reiter**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-151">This tab of your browser will be called the **live tab**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-152">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="b8df1-152">Figure 5</span></span>  
    > <span data-ttu-id="b8df1-153">Die Registerkarte "Live"</span><span class="sxs-lookup"><span data-stu-id="b8df1-153">The live tab</span></span>  
    > ![Die Registerkarte "Live"][ImageCssSetup3]  

## <span data-ttu-id="b8df1-155">Grundlegendes zu CSS</span><span class="sxs-lookup"><span data-stu-id="b8df1-155">Understand CSS</span></span>   

<span data-ttu-id="b8df1-156">**CSS** ist eine Computersprache, die das Layout und die Gestaltung von Webseiten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-156">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="b8df1-157">Hier ist beispielsweise ein Absatz mit einem Rahmen:</span><span class="sxs-lookup"><span data-stu-id="b8df1-157">For example, here is a paragraph with a border:</span></span>  

> ##### <span data-ttu-id="b8df1-158">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="b8df1-158">Figure 6</span></span>  
> <span data-ttu-id="b8df1-159">Dies wurde mit CSS formatiert</span><span class="sxs-lookup"><span data-stu-id="b8df1-159">This has been styled with CSS</span></span>  
> ![Dies wurde mit CSS formatiert][ImageCssStyled]  

<span data-ttu-id="b8df1-161">Hier ist der HTML-und CSS-Code, der zum Erstellen dieses Absatzes verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="b8df1-161">Here is the HTML and CSS code used to create that paragraph:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="b8df1-162">sieht Ihnen vielleicht neu aus.</span><span class="sxs-lookup"><span data-stu-id="b8df1-162">probably looks new to you.</span></span>  <span data-ttu-id="b8df1-163">Der andere sollte vertraut aussehen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-163">The rest should look familiar.</span></span>  <span data-ttu-id="b8df1-164">Wenn dies nicht der Fall ist, [beginnen Sie mit HTML und dem Dom][DevToolsBeginnersHtml] , bevor Sie dieses Lernprogramm durchführen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-164">If not, complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] before attempting this tutorial.</span></span>  

## <span data-ttu-id="b8df1-165">Hinzufügen von Inlineformatvorlagen</span><span class="sxs-lookup"><span data-stu-id="b8df1-165">Add inline styles</span></span>   

<span data-ttu-id="b8df1-166">Verwenden Sie **Inlineformatvorlagen** , wenn Sie Formatvorlagen auf ein einzelnes Element anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b8df1-166">Use **inline styles** when you want to apply styles to a single element.</span></span>  <span data-ttu-id="b8df1-167">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-167">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-168">Wechseln Sie zurück zur Registerkarte Bearbeitung, und öffnen Sie Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-168">Go back to the editing tab and open `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-169">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="b8df1-169">Figure 7</span></span>  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  <span data-ttu-id="b8df1-171">`style="background-color: aliceblue;"`Zu ihrer hinzufügen `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-171">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="b8df1-172">Im Code-Block unten ist die vierte Codezeile diejenige, die Sie ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-172">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="b8df1-173">Der andere ist nur da, damit Sie sicher sein können, dass Sie den neuen Code an die richtige Stelle setzen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-173">The rest is just there so you can be sure that you're putting the new code in the right place.</span></span>  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  <span data-ttu-id="b8df1-174">Wechseln Sie zum **Reiter "Live"** , um die Änderungen anzuzeigen!</span><span class="sxs-lookup"><span data-stu-id="b8df1-174">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="b8df1-175">Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.</span><span class="sxs-lookup"><span data-stu-id="b8df1-175">The background of the `<nav>` section is now blue.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-176">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="b8df1-176">Figure 8</span></span>  
    > <span data-ttu-id="b8df1-177">Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau</span><span class="sxs-lookup"><span data-stu-id="b8df1-177">The background color behind the Home and Contact links is now blue</span></span>  
    > ![Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau][ImageCssInline2]  

## <span data-ttu-id="b8df1-179">Wieder verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="b8df1-179">Re-use styles on a single page with internal stylesheets</span></span>   

<span data-ttu-id="b8df1-180">Zuvor haben Sie eine Inlineformatvorlage gesehen, die eine Formatvorlage auf eine einzelne `<p>` Kategorie wie die folgende angewendet hat:</span><span class="sxs-lookup"><span data-stu-id="b8df1-180">Earlier, you saw an inline style that applied a style to a single `<p>` tag like this:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="b8df1-181">Was ist, wenn Sie möchten, dass alle `<p>` Elemente auf Ihrer Webseite auf die gleiche Weise formatiert werden?</span><span class="sxs-lookup"><span data-stu-id="b8df1-181">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="b8df1-182">Sie müssten den Code in jeder einzelnen `<p>` Kategorie auf Ihrer Website kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-182">You'd have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="b8df1-183">Das ist viel Zeit und Mühe.</span><span class="sxs-lookup"><span data-stu-id="b8df1-183">That's a lot of time and effort.</span></span>  <span data-ttu-id="b8df1-184">Und wenn Sie eine Bearbeitung vornehmen mussten, müssten Sie jedes Tag erneut ändern.</span><span class="sxs-lookup"><span data-stu-id="b8df1-184">And, if you needed to make an edit, you'd have to change every tag again.</span></span>  <span data-ttu-id="b8df1-185">Mit **internen Stylesheets** können Sie Ihr CSS einmal schreiben, damit es auf mehrere Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8df1-185">**Internal stylesheets** allow you to write your CSS once so that it applies to multiple elements.</span></span>  <span data-ttu-id="b8df1-186">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-186">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-187">Klicken Sie auf der Registerkarte Live auf **Kontakt** , um zur Kontaktseite zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-187">In the live tab, click **Contact** to go to the contact page.</span></span>  <span data-ttu-id="b8df1-188">Beachten Sie die Schriftart für " **Privat** " und " **Kontakt**".</span><span class="sxs-lookup"><span data-stu-id="b8df1-188">Notice the font of **Home** and **Contact**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-189">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="b8df1-189">Figure 9</span></span>  
    > <span data-ttu-id="b8df1-190">Die Kontaktseite</span><span class="sxs-lookup"><span data-stu-id="b8df1-190">The Contact page</span></span>  
    > ![Die Kontaktseite][ImageCssInternal1]  

1.  <span data-ttu-id="b8df1-192">Wechseln Sie auf der **Registerkarte Editor**zu `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-192">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="b8df1-193">Fügen Sie den folgenden Code hinzu `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-193">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="b8df1-194">Beachten Sie, dass die Zeilen, die mit `<style>` und endet mit beginnen, das `</style>` hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-194">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="b8df1-195">Der andere Code ist gerade vorhanden, damit Sie wissen, wo der neue Code platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8df1-195">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="b8df1-196">Wechseln Sie zurück zur **Registerkarte Live**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-196">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="b8df1-197">Klicken Sie auf **Kontakt** , um zur Kontaktseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b8df1-197">Click **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="b8df1-198">Die Schriftart von " **Start** " und " **Kontakt** " hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="b8df1-198">The font of **Home** and **Contact** has changed.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-199">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="b8df1-199">Figure 10</span></span>  
    > <span data-ttu-id="b8df1-200">Die Schriftart der Links für "Start" und "Kontakt" wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="b8df1-200">The font of the Home and Contact links has changed</span></span>  
    > ![Die Schriftart der Links für "Start" und "Kontakt" wurde geändert.][ImageCssInternal2]  
    
### <span data-ttu-id="b8df1-202">Grundlegendes zu internen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="b8df1-202">Understand internal stylesheets</span></span>   

<span data-ttu-id="b8df1-203">Interne Stylesheets wenden Formatvorlagen mithilfe von **Auswahlen**an.</span><span class="sxs-lookup"><span data-stu-id="b8df1-203">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="b8df1-204">Auswahlen sind Muster, die möglicherweise für ein oder mehrere HTML-Elemente gelten.</span><span class="sxs-lookup"><span data-stu-id="b8df1-204">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="b8df1-205">Im vorherigen Codebeispiel:</span><span class="sxs-lookup"><span data-stu-id="b8df1-205">For example, in the previous code:</span></span>  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` <span data-ttu-id="b8df1-206">ist eine Auswahl, die in "Any" übersetzt wird, `<li>` die eine enthält `<a>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-206">is a selector that translates to "any `<li>` that contains an `<a>`".</span></span>  <span data-ttu-id="b8df1-207">Der Browser ändert die Schriftart der Links **Home** und **Contact** , da diese dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-207">The browser changes the font of the **Home** and **Contact** links because they match this pattern.</span></span>  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="b8df1-208">ist eine **Deklaration**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-208">is a **declaration**.</span></span>  <span data-ttu-id="b8df1-209">Eine Deklaration besteht aus zwei Teilen: einer **Eigenschaft** und einem **Wert**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-209">A declaration is made of two parts: a **property** and a **value**.</span></span>  `font-family` <span data-ttu-id="b8df1-210">ist die Eigenschaft und `'Courier New', Courier, serif` der Wert dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b8df1-210">is the property, and `'Courier New', Courier, serif` is the value of that property.</span></span>  <span data-ttu-id="b8df1-211">Die Eigenschaft beschreibt eine allgemeine Möglichkeit, die Art des Elements zu ändern, und der Wert gibt an, wie genau es geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8df1-211">The property describes a general way that you can change the element's style, and the value says how exactly it should change.</span></span>  <span data-ttu-id="b8df1-212">Gibt beispielsweise `font-family: 'Courier New', Courier, serif` dem Browser folgende Anweisung aus: "die Schriftart von Elementen, die dem Muster entsprechen, auf festzulegen `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-212">For example, `font-family: 'Courier New', Courier, serif` gives the browser this instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="b8df1-213">Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-213">If that font isn't available, use `Courier`.</span></span>  <span data-ttu-id="b8df1-214">Wenn dies nicht möglich ist, verwenden Sie `serif` . "</span><span class="sxs-lookup"><span data-stu-id="b8df1-214">If that isn't available, use `serif`."</span></span>  

### <span data-ttu-id="b8df1-215">Hinzufügen mehrerer Auswahlen zu einem RuleSet</span><span class="sxs-lookup"><span data-stu-id="b8df1-215">Add multiple selectors to a ruleset</span></span>   

<span data-ttu-id="b8df1-216">Ein Block mit CSS-Code wie dem, was unten angezeigt wird, wird als **RuleSet**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-216">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="b8df1-217">Verwenden Sie Kommas, um einem RuleSet mehrere Auswahlen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-217">Use commas to add multiple selectors to a ruleset.</span></span>  <span data-ttu-id="b8df1-218">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-218">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-219">Öffnen Sie auf der **Registerkarte Editor den Reiter** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-219">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="b8df1-220">Nach `li a` Typ `, h1` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-220">After `li a` type `, h1`.</span></span>  

    ```html
    ...
        ...
            ...
            <style>
                li a, h1 {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        ...
    ...
    ```  

    <span data-ttu-id="b8df1-221">Dadurch wird der Browser so formatiert, `<h1>` dass er Elemente auf die gleiche Weise anweist wie Elemente, die dem Muster entsprechen `li a` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-221">This tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="b8df1-222">Wechseln Sie zur **Registerkarte Live**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-222">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="b8df1-223">Klicken Sie auf den Link **Kontakt** , um zur Kontaktseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b8df1-223">Click the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="b8df1-224">**Kontaktieren Sie mich jetzt!**</span><span class="sxs-lookup"><span data-stu-id="b8df1-224">Now, **Contact Me!**</span></span> <span data-ttu-id="b8df1-225">hat die gleiche Schriftart wie die Navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="b8df1-225">has the same font as the navigation links.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-226">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="b8df1-226">Figure 11</span></span>  
    > <span data-ttu-id="b8df1-227">Der Text "Kontakt!"</span><span class="sxs-lookup"><span data-stu-id="b8df1-227">The text 'Contact Me!'</span></span> <span data-ttu-id="b8df1-228">hat nun dieselbe Schriftart wie die Links für "Privat" und "Kontakt"</span><span class="sxs-lookup"><span data-stu-id="b8df1-228">now has the same font as the Home and Contact links</span></span>  
    > ![Der Text kontaktiere mich!][ImageCssMultiple1]  

## <span data-ttu-id="b8df1-231">Experimentieren mit devtools</span><span class="sxs-lookup"><span data-stu-id="b8df1-231">Experiment with DevTools</span></span>   

<span data-ttu-id="b8df1-232">Wenn Sie Ihre Reise in die Master-Webentwicklung fortsetzen, werden Sie feststellen, dass CSS schwierig sein kann.</span><span class="sxs-lookup"><span data-stu-id="b8df1-232">As you continue your journey to master web development, you'll find that CSS can be tricky.</span></span>  <span data-ttu-id="b8df1-233">Sie schreiben einige CSS-Daten und erwarten, dass Sie auf eine Art und Weise angezeigt werden, doch der Browser hat etwas völlig anderes.</span><span class="sxs-lookup"><span data-stu-id="b8df1-233">You'll write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="b8df1-234">Microsoft Edge devtools macht es einfach, mit Änderungen zu experimentieren und sofort zu sehen, wie sich diese Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="b8df1-234">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how those changes affect the page.</span></span>  

### <span data-ttu-id="b8df1-235">Hinzufügen einer Deklaration zu einem vorhandenen rulet-Element in devtools</span><span class="sxs-lookup"><span data-stu-id="b8df1-235">Add a declaration to an existing rulest in DevTools</span></span>   

<span data-ttu-id="b8df1-236">Wenn Sie die Formatvorlage eines vorhandenen Elements durchlaufen möchten, fügen Sie eine Deklaration zu einem vorhandenen RuleSet hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8df1-236">When you want to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  <span data-ttu-id="b8df1-237">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-237">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-238">Klicken Sie mit der rechten Maustaste auf den Link **Start** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="b8df1-238">Right-click the **Home** link and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-239">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="b8df1-239">Figure 12</span></span>  
    > <span data-ttu-id="b8df1-240">Überprüfen des Start Links</span><span class="sxs-lookup"><span data-stu-id="b8df1-240">Inspecting the Home link</span></span>  
    > ![Überprüfen des Start Links][ImageCssAdd1]  
    
    <span data-ttu-id="b8df1-242">DevTools wird neben ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-242">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="b8df1-243">Der Code, der den Link "Start" darstellt, `<a href="/">Home</a>` wird in der DOM-Struktur blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="b8df1-243">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="b8df1-244">Dies sollte aus den ersten [Schritten mit HTML und dem Dom][DevToolsBeginnersHtml]vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="b8df1-244">This should be familiar from [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>  <span data-ttu-id="b8df1-245">Auf der Registerkarte **Formatvorlagen** unterhalb der DOM-Struktur können Sie die `font-family: 'Courier New', Courier, serif` Deklaration sehen, die Sie zuvor hinzugefügt haben `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-245">In the **Styles** tab below the DOM Tree you can see the `font-family: 'Courier New', Courier, serif` declaration that you added to `contact.html` earlier.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-246">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="b8df1-246">Figure 13</span></span>  
    > <span data-ttu-id="b8df1-247">Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b8df1-247">The Styles tab is below the DOM Tree</span></span>  
    > ![Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur.][ImageCssAdd2]  
    
    <span data-ttu-id="b8df1-249">Wenn Ihr devtools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b8df1-249">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-250">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="b8df1-250">Figure 14</span></span>  
    > <span data-ttu-id="b8df1-251">Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b8df1-251">The Styles tab is to the right of the DOM Tree</span></span>  
    > ![Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur.][ImageCssAdd3]  
    
1.  <span data-ttu-id="b8df1-253">Klicken Sie unten auf das Leerzeichen `font-family: 'Courier New', Courier, Serif` , um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-253">Click the whitespace below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-254">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="b8df1-254">Figure 15</span></span>  
    > <span data-ttu-id="b8df1-255">Hinzufügen einer neuen Deklaration</span><span class="sxs-lookup"><span data-stu-id="b8df1-255">Adding a new declaration</span></span>  
    > ![Hinzufügen einer neuen Deklaration][ImageCssAdd4]  
    
1.  <span data-ttu-id="b8df1-257">Geben `color` Sie ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-257">Type `color` and then press `Enter`.</span></span>  <span data-ttu-id="b8df1-258">Die AutoVervollständigen-Benutzeroberfläche schlägt Optionen während der Eingabe vor.</span><span class="sxs-lookup"><span data-stu-id="b8df1-258">The autocomplete UI suggests options as you type.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-259">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="b8df1-259">Figure 16</span></span>  
    > <span data-ttu-id="b8df1-260">Tippen</span><span class="sxs-lookup"><span data-stu-id="b8df1-260">Typing</span></span> `color`  
    > ![Eingeben von Farben][ImageCssAdd5]  

1.  <span data-ttu-id="b8df1-262">Geben `magenta` Sie ein, und drücken Sie dann `Enter` erneut.</span><span class="sxs-lookup"><span data-stu-id="b8df1-262">Type `magenta` and then press `Enter` again.</span></span>  <span data-ttu-id="b8df1-263">Der gesamte Text auf der Kontaktseite ist jetzt Magenta.</span><span class="sxs-lookup"><span data-stu-id="b8df1-263">All of the text on the contact page is now magenta.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-264">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="b8df1-264">Figure 17</span></span>  
    > <span data-ttu-id="b8df1-265">Tippen</span><span class="sxs-lookup"><span data-stu-id="b8df1-265">Typing</span></span> `magenta`  
    > ![Eingeben von Magenta][ImageCssAdd6]  
    
### <span data-ttu-id="b8df1-267">Bearbeiten einer Deklaration in devtools</span><span class="sxs-lookup"><span data-stu-id="b8df1-267">Edit a declaration in DevTools</span></span>   

<span data-ttu-id="b8df1-268">Sie können auch vorhandene Deklarationen in devtools bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b8df1-268">You can also edit existing declarations in DevTools.</span></span>  <span data-ttu-id="b8df1-269">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-269">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-270">Klicken Sie auf das Magenta-Quadrat neben `magenta` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-270">Click the magenta square next to `magenta`.</span></span>  <span data-ttu-id="b8df1-271">Eine Farbauswahl wird eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-271">A color picker pops up.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-272">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="b8df1-272">Figure 18</span></span>  
    > <span data-ttu-id="b8df1-273">Die Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="b8df1-273">The Color Picker</span></span>  
    > ![Die Farbauswahl][ImageCssEdit1]  
    
1.  <span data-ttu-id="b8df1-275">Verwenden Sie die Farbauswahl, um den Schriftart Text in eine Farbe zu ändern, die Ihnen gefällt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-275">Use the color picker to change the font text to a color that you like.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-276">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="b8df1-276">Figure 19</span></span>  
    > <span data-ttu-id="b8df1-277">Ändern der Schriftfarbe in Lila mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="b8df1-277">Changing the font color to purple with the Color Picker</span></span>  
    > ![Ändern der Schriftfarbe in Lila mit der Farbauswahl][ImageCssEdit2]  

### <span data-ttu-id="b8df1-279">Hinzufügen eines neuen RuleSets in devtools</span><span class="sxs-lookup"><span data-stu-id="b8df1-279">Add a new ruleset in DevTools</span></span>   

<span data-ttu-id="b8df1-280">Sie können auch neue RuleSets in devtools hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-280">You can also add new rulesets in DevTools.</span></span>  <span data-ttu-id="b8df1-281">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-281">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-282">Klicken Sie auf **neue** Stilregel Regel ![ ][ImageNewStyleRuleIcon] , die sich neben **CLS**befindet.</span><span class="sxs-lookup"><span data-stu-id="b8df1-282">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] which is next to **.cls**.</span></span>  <span data-ttu-id="b8df1-283">Ein leerer RuleSet wird `a` als Auswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-283">An empty ruleset appears with `a` as the selector.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-284">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="b8df1-284">Figure 20</span></span>  
    > <span data-ttu-id="b8df1-285">Hinzufügen einer neuen Regel</span><span class="sxs-lookup"><span data-stu-id="b8df1-285">Adding a new rule</span></span>  
    > ![Hinzufügen einer neuen Regel][ImageCssRule1]  
    
1.  <span data-ttu-id="b8df1-287">Ersetzen Sie `a` durch `a:hover`.</span><span class="sxs-lookup"><span data-stu-id="b8df1-287">Replace `a` with `a:hover`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-288">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="b8df1-288">Figure 21</span></span>  
    > <span data-ttu-id="b8df1-289">Ersetzen `a` durch</span><span class="sxs-lookup"><span data-stu-id="b8df1-289">Replacing `a` with</span></span> `a:hover`  
    > ![Ersetzen eines durch a:hover][ImageCssRule2]  
    
    `:hover` <span data-ttu-id="b8df1-291">ist eine **Pseudoklasse**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-291">is a **pseudo-class**.</span></span>  <span data-ttu-id="b8df1-292">Verwenden Sie Pseudoklassen, um Elemente zu formatieren, wenn Sie spezielle Zustände eingeben.</span><span class="sxs-lookup"><span data-stu-id="b8df1-292">Use pseudo-classes to style elements when they enter special states.</span></span>  <span data-ttu-id="b8df1-293">Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie auf ein Element zeigen `<a>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-293">For example, the `a:hover` style only takes effect when you're hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="b8df1-294">Klicken Sie zwischen den Klammern, um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-294">Click between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="b8df1-295">Geben `background-color` Sie den Namen der Deklaration ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-295">Type `background-color` for the declaration name and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-296">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="b8df1-296">Figure 22</span></span>  
    > <span data-ttu-id="b8df1-297">Tippen</span><span class="sxs-lookup"><span data-stu-id="b8df1-297">Typing</span></span> `background-color`  
    > ![Hintergrundfarbe eingeben][ImageCssRule3]  
    
1.  <span data-ttu-id="b8df1-299">Geben `green` Sie für den Deklarations Wert ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-299">Type `green` for the declaration value and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-300">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="b8df1-300">Figure 23</span></span>  
    > <span data-ttu-id="b8df1-301">Tippen</span><span class="sxs-lookup"><span data-stu-id="b8df1-301">Typing</span></span> `green`  
    > ![Eingeben von grün][ImageCssRule4]  
    
1.  <span data-ttu-id="b8df1-303">Zeigen Sie mit der Maus auf den Link " **Start** ".</span><span class="sxs-lookup"><span data-stu-id="b8df1-303">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="b8df1-304">Der Hintergrund des Links wird grün.</span><span class="sxs-lookup"><span data-stu-id="b8df1-304">The background of the link turns green.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-305">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="b8df1-305">Figure 24</span></span>  
    > <span data-ttu-id="b8df1-306">Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="b8df1-306">Hovering over the Home link to reveal its green background</span></span>  
    > ![Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen][ImageCssRule5]  
    
## <span data-ttu-id="b8df1-308">Wieder verwenden von Formatvorlagen auf mehreren Seiten mit externen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="b8df1-308">Re-use styles across pages with external stylesheets</span></span>   

<span data-ttu-id="b8df1-309">Zuvor haben Sie dieses interne Stylesheet hinzugefügt `contact.html` :</span><span class="sxs-lookup"><span data-stu-id="b8df1-309">Earlier you added this internal stylesheet to `contact.html`:</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="b8df1-310">Was ist, wenn Sie `index.html` die gleiche Weise formatieren möchten?</span><span class="sxs-lookup"><span data-stu-id="b8df1-310">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="b8df1-311">Was ist, wenn Sie mehr als *tausend* Seiten haben und diese Formatvorlagen auf alle anwenden möchten?</span><span class="sxs-lookup"><span data-stu-id="b8df1-311">What if you had a *thousand* pages and you wanted to apply these styles to all of them?</span></span>  <span data-ttu-id="b8df1-312">Sie müssen dieses interne Stylesheet in jede einzelne Webseite auf Ihrer Website kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-312">You'd have to copy and paste this internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="b8df1-313">Mit **externen Stylesheets** können Sie Ihren CSS-Eintrag noch einmal auf mehrere Seiten anwenden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-313">**External stylesheets** allow you to write your CSS once yet apply it to multiple pages.</span></span>  <span data-ttu-id="b8df1-314">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-314">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-315">Laden Sie zunächst die Registerkarte "Live" neu, um die Änderungen zu entfernen, die Sie in devtools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="b8df1-315">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-316">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="b8df1-316">Figure 25</span></span>  
    >  <span data-ttu-id="b8df1-317">Nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-317">After reloading the page the changes that were made in DevTools are gone</span></span>  
    > ![ <span data-ttu-id="b8df1-318">Nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-318">After reloading the page the changes that were made in DevTools are gone</span></span>][ImageCssExternal01]  
    
1.  <span data-ttu-id="b8df1-319">Wechseln Sie zurück zur **Registerkarte Editor** , und öffnen Sie Sie `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-319">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-320">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="b8df1-320">Figure 26</span></span>  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  <span data-ttu-id="b8df1-322">Löschen Sie alles zwischen `<style>` und `</style>` , einschließlich `<style>` und `</style>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-322">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-323">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="b8df1-323">Figure 27</span></span>  
    > <span data-ttu-id="b8df1-324">Das Stil-Tag wurde entfernt</span><span class="sxs-lookup"><span data-stu-id="b8df1-324">The style tag has been removed</span></span>  
    > ![Das Stil-Tag wurde entfernt][ImageCssExternal03]  
    
1.  <span data-ttu-id="b8df1-326">Wechseln Sie zu `index.html` der Kategorie, und entfernen Sie Sie `style="background-color: aliceblue;"` `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-326">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="b8df1-327">Sie haben jetzt alle CSS entfernt, die Sie zuvor zu Ihrer Website hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="b8df1-327">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-328">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="b8df1-328">Figure 28</span></span>  
    > <span data-ttu-id="b8df1-329">Die Inlineformatvorlage wurde aus dem NAV-Element entfernt</span><span class="sxs-lookup"><span data-stu-id="b8df1-329">The inline style has been removed from the nav element</span></span>  
    > ![Die Inlineformatvorlage wurde aus dem NAV-Element entfernt][ImageCssExternal04]  

1.  <span data-ttu-id="b8df1-331">Klicken Sie auf **neue Datei**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-331">Click **New File**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-332">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="b8df1-332">Figure 29</span></span>  
    > <span data-ttu-id="b8df1-333">Dialogfeld ' neue Datei '</span><span class="sxs-lookup"><span data-stu-id="b8df1-333">The new file dialog</span></span>  
    > ![Dialogfeld ' neue Datei '][ImageCssExternal05]  
    
1.  <span data-ttu-id="b8df1-335">Ersetzen `cool-file.js` `style.css` Sie durch, und klicken Sie dann auf **Datei hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="b8df1-335">Replace `cool-file.js` with `style.css` and then click **Add File**.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-336">Abbildung 30</span><span class="sxs-lookup"><span data-stu-id="b8df1-336">Figure 30</span></span>  
    > <span data-ttu-id="b8df1-337">Tippen</span><span class="sxs-lookup"><span data-stu-id="b8df1-337">Typing</span></span> `style.css`  
    > ![Eingeben von Style. CSS][ImageCssExternal06]  
    
1.  <span data-ttu-id="b8df1-339">Fügen Sie diesen Code in `style.css` Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="b8df1-339">Paste this code into `style.css`:</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    > ##### <span data-ttu-id="b8df1-340">Abbildung 31</span><span class="sxs-lookup"><span data-stu-id="b8df1-340">Figure 31</span></span>  
    > <span data-ttu-id="b8df1-341">Hinzufügen von Code zu</span><span class="sxs-lookup"><span data-stu-id="b8df1-341">Adding code to</span></span> `style.css`  
    > ![Hinzufügen von Code zu Style. CSS][ImageCssExternal07]  
    
    <span data-ttu-id="b8df1-343">An diesem Punkt haben Sie ein externes Stylesheet erstellt, doch Ihr HTML-Code weiß noch nicht, dass es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b8df1-343">At this point, you have created an external stylesheet, but your HTML doesn't know that it exists, yet.</span></span>  
    
1.  <span data-ttu-id="b8df1-344">Öffnen Sie `index.html`.</span><span class="sxs-lookup"><span data-stu-id="b8df1-344">Open `index.html`.</span></span>  
1.  <span data-ttu-id="b8df1-345">Dem `<link rel="stylesheet" href="style.css">` HTML-Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-345">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### <span data-ttu-id="b8df1-346">Abbildung 32</span><span class="sxs-lookup"><span data-stu-id="b8df1-346">Figure 32</span></span>  
    > <span data-ttu-id="b8df1-347">Verknüpfen mit</span><span class="sxs-lookup"><span data-stu-id="b8df1-347">Linking to</span></span> `style.css`  
    > ![Verknüpfen mit Style. CSS][ImageCssExternal08]  

1.  <span data-ttu-id="b8df1-349">Wechseln Sie zu, `contact.html` und fügen Sie den Link auch dort hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8df1-349">Go to `contact.html` and add the link there, too.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-350">Abbildung 33</span><span class="sxs-lookup"><span data-stu-id="b8df1-350">Figure 33</span></span>  
    > <span data-ttu-id="b8df1-351">Verknüpfen mit `style.css` in</span><span class="sxs-lookup"><span data-stu-id="b8df1-351">Linking to `style.css` in</span></span> `contact.html`  
    > ![Verknüpfen mit Style. CSS in contact.html][ImageCssExternal09]  

1.  <span data-ttu-id="b8df1-353">Wechseln Sie zur **Registerkarte Live**.  Auf der Startseite befindet sich nun die gleiche Schriftart wie im letzten Abschnitt und ein blauer Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="b8df1-353">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-354">Abbildung 34</span><span class="sxs-lookup"><span data-stu-id="b8df1-354">Figure 34</span></span>  
    > <span data-ttu-id="b8df1-355">Die Startseite</span><span class="sxs-lookup"><span data-stu-id="b8df1-355">The home page</span></span>  
    > ![Die Startseite][ImageCssExternal10]  
    
1.  <span data-ttu-id="b8df1-357">Klicken Sie auf den Link **Kontakt** , um zur Kontaktseite zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-357">Click the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="b8df1-358">Die Seite "Kontakt" hat dieselbe Formatierung wie die Startseite.</span><span class="sxs-lookup"><span data-stu-id="b8df1-358">The contact page has the same formatting as the home page.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-359">Abbildung 35</span><span class="sxs-lookup"><span data-stu-id="b8df1-359">Figure 35</span></span>  
    > <span data-ttu-id="b8df1-360">Die Kontaktseite</span><span class="sxs-lookup"><span data-stu-id="b8df1-360">The contact page</span></span>  
    > ![Die Kontaktseite][ImageCssExternal11]  
    
## <span data-ttu-id="b8df1-362">Verwenden eines CSS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="b8df1-362">Use a CSS framework</span></span>   

<span data-ttu-id="b8df1-363">**CSS-Frameworks** sind Sammlungen von Formatvorlagen, die von anderen Entwicklern erstellt wurden, die das Erstellen attraktiver Websites vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-363">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="b8df1-364">Anstatt selbst Formatvorlagen zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b8df1-364">Instead of defining styles yourself, a framework gives you a collection of styles that you can use on your page elements.</span></span>  

1.  <span data-ttu-id="b8df1-365">Kopieren Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="b8df1-365">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="b8df1-366">Wechseln Sie zur Registerkarte Bearbeitung, und fügen Sie den Code in ein `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-366">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-367">Abbildung 36</span><span class="sxs-lookup"><span data-stu-id="b8df1-367">Figure 36</span></span>  
    > <span data-ttu-id="b8df1-368">Verknüpfen mit dem Framework in</span><span class="sxs-lookup"><span data-stu-id="b8df1-368">Linking to the framework in</span></span> `contact.html`  
    > ![Verknüpfen mit dem Framework in contact.html][ImageCssFramework1]  
    
1.  <span data-ttu-id="b8df1-370">Fügen Sie den Code `index.html` ebenfalls ein.</span><span class="sxs-lookup"><span data-stu-id="b8df1-370">Paste the code into `index.html`, as well.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-371">Abbildung 37</span><span class="sxs-lookup"><span data-stu-id="b8df1-371">Figure 37</span></span>  
    > <span data-ttu-id="b8df1-372">Verknüpfen mit dem Framework in</span><span class="sxs-lookup"><span data-stu-id="b8df1-372">Linking to the framework in</span></span> `index.html`  
    > ![Verknüpfen mit dem Framework in index.html][ImageCssFramework2]  
    
1.  <span data-ttu-id="b8df1-374">Kehren Sie zur Registerkarte Live zurück, um Ihre Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-374">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="b8df1-375">Während die Hintergrundfarbe von `<nav>` und die Schriftart der `li a` Elemente identisch sind, hat sich die Schriftart der anderen Elemente geändert.</span><span class="sxs-lookup"><span data-stu-id="b8df1-375">While the background color of the `<nav>` and the font of the `li a` elements are the same, the font of the other elements has changed.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-376">Abbildung 38</span><span class="sxs-lookup"><span data-stu-id="b8df1-376">Figure 38</span></span>  
    > <span data-ttu-id="b8df1-377">Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert</span><span class="sxs-lookup"><span data-stu-id="b8df1-377">Some of the font on the home page has changed because of the framework</span></span>  
    > ![Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert][ImageCssFramework3]  

### <span data-ttu-id="b8df1-379">Verwenden einer Klasse</span><span class="sxs-lookup"><span data-stu-id="b8df1-379">Use a class</span></span>   

<span data-ttu-id="b8df1-380">Im letzten Abschnitt haben Sie Ihren Webseiten Bootstrap hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-380">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="b8df1-381">CSS-Frameworks können Ihnen helfen, wichtige Änderungen an Ihrer Seite mit sehr wenig Code vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-381">CSS frameworks can help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="b8df1-382">Probieren Sie es jetzt aus, indem Sie die Kopfzeile ändern:</span><span class="sxs-lookup"><span data-stu-id="b8df1-382">Try it now by changing your header:</span></span>  

1.  <span data-ttu-id="b8df1-383">Kopieren Sie diesen Code:</span><span class="sxs-lookup"><span data-stu-id="b8df1-383">Copy this code:</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="b8df1-384">Fügen Sie diesen Code zu Ihrem `<header>` Tag in hinzu `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-384">Add this code to your `<header>` tag in `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-385">Abbildung 39</span><span class="sxs-lookup"><span data-stu-id="b8df1-385">Figure 39</span></span>  
    > <span data-ttu-id="b8df1-386">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="b8df1-386">Adding classes in</span></span> `index.html`  
    > ![Hinzufügen von Klassen in index.html][ImageCssJumbotron1]  
    
1.  <span data-ttu-id="b8df1-388">Fügen Sie dem Tag auch den Code hinzu `<header>` `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-388">Add the code to your `<header>` tag in `contact.html`, too.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-389">Abbildung 40</span><span class="sxs-lookup"><span data-stu-id="b8df1-389">Figure 40</span></span>  
    > <span data-ttu-id="b8df1-390">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="b8df1-390">Adding classes in</span></span> `contact.html`  
    > ![Hinzufügen von Klassen in contact.html][ImageCssJumbotron2]  
    
1.  <span data-ttu-id="b8df1-392">Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  Es gibt jetzt ein großes, graues Feld um ihre Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="b8df1-392">View your changes in the live tab.  There's a big, grey box around your header now.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-393">Abbildung 41</span><span class="sxs-lookup"><span data-stu-id="b8df1-393">Figure 41</span></span>  
    > <span data-ttu-id="b8df1-394">Die Kopfzeile hat nun ein großes, graues Feld um Sie herum</span><span class="sxs-lookup"><span data-stu-id="b8df1-394">The header now has a big, grey box around it</span></span>  
    > ![Die Kopfzeile hat nun ein großes, graues Feld um Sie herum][ImageCssJumbotron3]  
    
### <span data-ttu-id="b8df1-396">Grundlegendes zu Klassen</span><span class="sxs-lookup"><span data-stu-id="b8df1-396">Understand classes</span></span>   

<span data-ttu-id="b8df1-397">Mit Klassen können Sie Auflistungen von Formatvorlagen beliebigen Elementen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-397">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="b8df1-398">So können Sie beispielsweise festlegen, dass das `class` Attribut der `<header>` Tags auf `jumbotron` die folgenden Formatvorlagen angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="b8df1-398">For example, setting the `class` attribute of the `<header>` tags to `jumbotron` applied the following styles to them:</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="b8df1-399">Ein Vorteil von Kursen besteht darin, dass Sie Formatvorlagen auf alle gewünschten Elemente anwenden können.</span><span class="sxs-lookup"><span data-stu-id="b8df1-399">One advantage of classes is that they let you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="b8df1-400">Angenommen, Sie möchten die Hintergrundfarbe *einiger* `<p>` Elemente auf lila, aber nicht auf *alle* Farben einstellen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-400">For example, suppose you want to set the background color of *some* `<p>` elements to purple, but not *all* of them.</span></span>  <span data-ttu-id="b8df1-401">Sie können die Formatvorlage in einer Klasse definieren:</span><span class="sxs-lookup"><span data-stu-id="b8df1-401">You could define the style in a class:</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="b8df1-402">Und wenden Sie dann die Klasse nur auf die `<p>` Elemente an, die Sie formatieren möchten:</span><span class="sxs-lookup"><span data-stu-id="b8df1-402">And then apply the class to only the `<p>` elements that you want to style:</span></span>  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### <span data-ttu-id="b8df1-403">Ausrichten von Elementen</span><span class="sxs-lookup"><span data-stu-id="b8df1-403">Align elements</span></span>   

<span data-ttu-id="b8df1-404">Bootstrap stellt auch Klassen zum Ausrichten von Elementen bereit.</span><span class="sxs-lookup"><span data-stu-id="b8df1-404">Bootstrap also provides classes for aligning elements.</span></span>  <span data-ttu-id="b8df1-405">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="b8df1-405">Try it now:</span></span>  

1.  <span data-ttu-id="b8df1-406">Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-406">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="b8df1-407">`class="container-fluid"`Zu Ihrem Tag hinzufügen `<body>` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-407">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-408">Abbildung 42</span><span class="sxs-lookup"><span data-stu-id="b8df1-408">Figure 42</span></span>  
    > <span data-ttu-id="b8df1-409">Hinzufügen der `container-fluid` Klasse</span><span class="sxs-lookup"><span data-stu-id="b8df1-409">Adding the `container-fluid` class</span></span>  
    > ![Hinzufügen der Container-Fluid Klasse][ImageCssAlign1]  

1.  <span data-ttu-id="b8df1-411">Umbrechen `<nav>` `<main>` von und Elementen in `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="b8df1-411">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="b8df1-412">Stellen Sie sicher, dass Sie `</div>` `</main>` die neue Kategorie ordnungsgemäß schließen, um Sie zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-412">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-413">Abbildung 43</span><span class="sxs-lookup"><span data-stu-id="b8df1-413">Figure 43</span></span>  
    > <span data-ttu-id="b8df1-414">Hinzufügen einer Zeile</span><span class="sxs-lookup"><span data-stu-id="b8df1-414">Adding a row</span></span>  
    > ![Hinzufügen einer Zeile][ImageCssAlign2]  
    
1.  <span data-ttu-id="b8df1-416">Fügen Sie `class="col-3"` Ihrem `<nav>` Tag und `class="col-9"` Ihrem `<main>` Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8df1-416">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-417">Abbildung 44</span><span class="sxs-lookup"><span data-stu-id="b8df1-417">Figure 44</span></span>  
    > <span data-ttu-id="b8df1-418">Hinzufügen der `col-3` und- `col-9` Klassen</span><span class="sxs-lookup"><span data-stu-id="b8df1-418">Adding the `col-3` and `col-9` classes</span></span>  
    > ![Hinzufügen der Klassen Col-3 und Col-9][ImageCssAlign3]  
    
1.  <span data-ttu-id="b8df1-420">Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.</span><span class="sxs-lookup"><span data-stu-id="b8df1-420">View your changes in the live tab.</span></span>  
    
    > ##### <span data-ttu-id="b8df1-421">Abbildung 45</span><span class="sxs-lookup"><span data-stu-id="b8df1-421">Figure 45</span></span>  
    > <span data-ttu-id="b8df1-422">Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-422">The nav content is now to the left of the main content</span></span>  
    > ![Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.][ImageCssAlign4]  
    
## <span data-ttu-id="b8df1-424">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="b8df1-424">Next steps</span></span>   

<span data-ttu-id="b8df1-425">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="b8df1-425">Congratulations!</span></span>  <span data-ttu-id="b8df1-426">Fertig!</span><span class="sxs-lookup"><span data-stu-id="b8df1-426">You're done!</span></span>  

*   <span data-ttu-id="b8df1-427">Die beste Methode, um die Web-Entwicklung zu verbessern, besteht darin, weitere Websites zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-427">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="b8df1-428">Machen Sie sich keine Sorgen, wenn Sie etwas kaputt machen.</span><span class="sxs-lookup"><span data-stu-id="b8df1-428">Don't worry about breaking stuff.</span></span>  <span data-ttu-id="b8df1-429">Sie haben einfach nur Spaß und lernen so viel wie möglich auf dem Weg.</span><span class="sxs-lookup"><span data-stu-id="b8df1-429">Just have fun and learn as much as you can along the way.</span></span>  
*   <span data-ttu-id="b8df1-430">Schauen Sie sich die [Einführung in CSS][MDNCssFirstSteps] an, um weitere Informationen zum Formatieren von Webseiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8df1-430">Check out [Introduction to CSS][MDNCssFirstSteps] to learn lots more about styling web pages.</span></span>  
*   <span data-ttu-id="b8df1-431">Arbeiten Sie [im ersten Schritt mit dem anzeigen und Ändern des CSS][DevtoolsCssIndex] -Lernprogramms, um mehr darüber zu erfahren, wie Sie devtools verwenden können, um mit dem CSS einer Seite zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="b8df1-431">Work through our [Get Started with Viewing and Changing CSS][DevtoolsCssIndex] tutorial to learn more about how you can use DevTools to experiment with a page's CSS.</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Abbildung 1: wie Ihre Website aktuell aussieht"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Abbildung 2: wie Ihre Website am Ende des Lernprogramms aussehen wird"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Abbildung 3: die Registerkarte "Bearbeiten""  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Abbildung 4: das Menü "Projektoptionen""  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Abbildung 5: die Registerkarte "Live""  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Abbildung 6: Dies wurde mit CSS formatiert"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Abbildung 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Abbildung 8: die Hintergrundfarbe hinter den Links für "Start" und "Kontakt" ist jetzt blau"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Abbildung 9: die Kontaktseite"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Abbildung 10: die Schriftart der Links für "Start" und "Kontakt" wurde geändert"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Abbildung 11: der Text "Kontakt!" hat nun dieselbe Schriftart wie die Links "Privat" und "Kontakt""  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Abbildung 12: Überprüfen des Start Links"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Abbildung 13: die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Abbildung 14: die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Abbildung 15: Hinzufügen einer neuen Deklaration"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Abbildung 16: eingeben von Farben"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Abbildung 17: eingeben von Magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Abbildung 18: die Farbauswahl"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Abbildung 19: Ändern der Schriftfarbe in Lila mit der Farbauswahl"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Abbildung 20: Hinzufügen einer neuen Regel"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Abbildung 21: Ersetzen eines durch a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Abbildung 22: eingeben von Hintergrundfarbe"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Abbildung 23: eingeben von grün"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Abbildung 24: zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen."  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Abbildung 25: nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Abbildung 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Abbildung 27: das Style-Tag wurde entfernt"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Abbildung 28: die Inlineformatvorlage wurde aus dem NAV-Element entfernt"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Abbildung 29: Dialogfeld "neue Datei""  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Abbildung 30: eingeben von Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Abbildung 31: Hinzufügen von Code zu Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Abbildung 32: Verknüpfen mit Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Abbildung 33: Verknüpfen mit Style. CSS in contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Abbildung 34: die Startseite"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Abbildung 35: die Kontaktseite"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Abbildung 36: Verknüpfen mit dem Framework in contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Abbildung 37: Verknüpfen mit dem Framework in index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Abbildung 38: einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Abbildung 39: Hinzufügen von Klassen in index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Abbildung 40: Hinzufügen von Klassen in contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Abbildung 41: die Kopfzeile hat nun ein großes, graues Feld um Sie herum"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Abbildung 42: Hinzufügen der Container Fluid Klasse"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Abbildung 43: Hinzufügen einer Zeile"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Abbildung 44: Hinzufügen der Klassen Col-3 und Col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Abbildung 45: der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt."  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools für Anfänger: Erste Schritte mit HTML und dem Dom"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte beim Anzeigen und Ändern von CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-gekocht-Amphibien | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "CSS-erste Schritte | MDN"  

> [!NOTE]
> <span data-ttu-id="b8df1-482">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8df1-482">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b8df1-483">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/css) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8df1-483">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b8df1-485">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b8df1-485">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
