---
description: Erste Schritte mit CSS
title: 'DevTools für Anfänger: Erste Schritte mit CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993303"
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

# <span data-ttu-id="f2eec-104">DevTools für Anfänger: Erste Schritte mit CSS</span><span class="sxs-lookup"><span data-stu-id="f2eec-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="f2eec-105">In diesem Lernprogramm erfahren Sie, wie Sie eine Webseite mithilfe von CSS formatieren.</span><span class="sxs-lookup"><span data-stu-id="f2eec-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="f2eec-106">Sie erfahren auch, wie Sie Microsoft Edge devtools verwenden, um mit CSS-Änderungen zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="f2eec-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="f2eec-107">Der folgende Artikel ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in denen Sie die Grundlagen der Webentwicklung und der Microsoft Edge-devtools.</span><span class="sxs-lookup"><span data-stu-id="f2eec-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="f2eec-108">Sie erhalten praktische Erfahrungen, wenn Sie tatsächlich ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="f2eec-109">Sie müssen das erste Lernprogramm nicht durchführen, bevor Sie den zweiten Schritt ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="f2eec-110">[Einrichten Ihres Codes](#set-up-your-code) zeigt, wie Sie sich einrichten.</span><span class="sxs-lookup"><span data-stu-id="f2eec-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="f2eec-111">Dieses Lernprogramm ist für absolute Anfänger konzipiert und konzentriert sich sowohl auf die **Grundlagen der Webentwicklung** als auch auf die Grundlagen der Verwendung von devtools zum Experimentieren mit CSS.</span><span class="sxs-lookup"><span data-stu-id="f2eec-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="f2eec-112">Wenn Sie ein Lernprogramm benötigen, das sich nur auf devtools konzentriert, lesen Sie [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="f2eec-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="f2eec-113">Am Anfang des Lernprogramms sollte Ihre Website wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Wie Ihre Website aktuell aussieht" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="f2eec-115">Wie Ihre Website aktuell aussieht</span><span class="sxs-lookup"><span data-stu-id="f2eec-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="f2eec-116">Nachdem Sie das Lernprogramm abgeschlossen haben, sollte die Website wie in der folgenden Abbildung dargestellt aussehen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Wie Ihre Website am Ende des Lernprogramms aussehen sollte" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="f2eec-118">Wie Ihre Website am Ende des Lernprogramms aussehen sollte</span><span class="sxs-lookup"><span data-stu-id="f2eec-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="f2eec-119">Ziele</span><span class="sxs-lookup"><span data-stu-id="f2eec-119">Goals</span></span>  

<span data-ttu-id="f2eec-120">Führen Sie dieses Lernprogramm aus, um die folgenden Konzepte und Aufgaben besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="f2eec-121">Verwenden von CSS zum Formatieren einer Webseite</span><span class="sxs-lookup"><span data-stu-id="f2eec-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="f2eec-122">Verwenden von Microsoft Edge devtools zum Experimentieren mit CSS</span><span class="sxs-lookup"><span data-stu-id="f2eec-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="f2eec-123">Der Unterschied zwischen CSS-und CSS-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="f2eec-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="f2eec-124">Sie erstellen eine echte Website.</span><span class="sxs-lookup"><span data-stu-id="f2eec-124">You are building a real website.</span></span>  

## <span data-ttu-id="f2eec-125">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f2eec-125">Prerequisites</span></span>  

<span data-ttu-id="f2eec-126">Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="f2eec-127">Führen Sie [die ersten Schritte mit HTML und dem Dom durch][DevtoolsBeginnersHtml] , oder stellen Sie sicher, dass Sie HTML und das DOM ähnlich wie in diesem Lernprogramm kennen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="f2eec-128">Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.</span><span class="sxs-lookup"><span data-stu-id="f2eec-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="f2eec-129">Das folgende Lernprogramm verwendet eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, die in Microsoft Edge integriert sind.</span><span class="sxs-lookup"><span data-stu-id="f2eec-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="f2eec-130">Einrichten Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="f2eec-130">Set up your code</span></span>  

<span data-ttu-id="f2eec-131">Um Ihre Website zu erstellen, müssen Sie zunächst die folgenden Aktionen ausführen, um den Code einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f2eec-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="f2eec-132">Wenn Sie das erste Lernprogramm in der Serie bereits abgeschlossen haben, fahren Sie mit dem nächsten Abschnitt fort.</span><span class="sxs-lookup"><span data-stu-id="f2eec-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="f2eec-133">Verwenden Sie weiterhin ihren Code aus dem letzten Lernprogramm, [Erste Schritte mit HTML und dem Dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="f2eec-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="f2eec-134">Öffnen Sie den [Quellcode][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="f2eec-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="f2eec-135">Auf die Registerkarte "im Fokus" Ihres Browsers wird als **Registerkarte "Bearbeiten"** verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Die Registerkarte ' bearbeiten '" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="f2eec-137">Die Registerkarte ' **Bearbeiten** '</span><span class="sxs-lookup"><span data-stu-id="f2eec-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-138">Wählen Sie **gekocht-Amphibien**aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="f2eec-139">Ein Menü wird eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Das Menü "Projektoptionen"" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="f2eec-141">Das Menü "Projektoptionen"</span><span class="sxs-lookup"><span data-stu-id="f2eec-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="f2eec-142">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="f2eec-143">Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f2eec-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f2eec-144">Glitch generiert einen zufälligen Namen für das neue Projekt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="f2eec-145">Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-145">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="f2eec-146">Eine andere Registerkarte wird mit einer Live Ansicht Ihrer Website geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="f2eec-147">Auf die Registerkarte "auf dem Fokus" Ihres Browsers wird als **"Live"-Registerkarte**verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Die Registerkarte "Live"" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="f2eec-149">Die **Registerkarte "Live"**</span><span class="sxs-lookup"><span data-stu-id="f2eec-149">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="f2eec-150">Grundlegendes zu CSS</span><span class="sxs-lookup"><span data-stu-id="f2eec-150">Understand CSS</span></span>  

<span data-ttu-id="f2eec-151">**CSS** ist eine Computersprache, die das Layout und die Gestaltung von Webseiten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="f2eec-152">Die folgende Abbildung ist ein Absatz mit einem Rahmen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Der Text wurde mit CSS formatiert" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="f2eec-154">Der Text wurde mit CSS formatiert</span><span class="sxs-lookup"><span data-stu-id="f2eec-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="f2eec-155">Der folgende Codeausschnitt ist der HTML-und CSS-Code, der zum Erstellen des Absatzes in der vorherigen Abbildung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2eec-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="f2eec-156">sieht Ihnen vielleicht neu aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-156">probably looks new to you.</span></span>  <span data-ttu-id="f2eec-157">Der andere sollte vertraut aussehen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-157">The rest should look familiar.</span></span>  <span data-ttu-id="f2eec-158">Wenn dies nicht der Fall ist, führen Sie die ersten [Schritte mit HTML und dem Dom durch][DevtoolsBeginnersHtml] , bevor Sie die folgenden Abschnitte versuchen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="f2eec-159">Hinzufügen von Inlineformatvorlagen</span><span class="sxs-lookup"><span data-stu-id="f2eec-159">Add inline styles</span></span>  

<span data-ttu-id="f2eec-160">Führen Sie die folgenden Aktionen aus, um **Inlineformatvorlagen** zum Anwenden von Formatvorlagen auf ein einzelnes Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="f2eec-161">Wechseln Sie zurück zur Registerkarte Bearbeitung, und öffnen Sie Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="f2eec-163">`index.html`Auf der Registerkarte "Bearbeiten" öffnen</span><span class="sxs-lookup"><span data-stu-id="f2eec-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-164">`style="background-color: aliceblue;"`Zu ihrer hinzufügen `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="f2eec-165">Im Code-Block unten ist die vierte Codezeile diejenige, die Sie ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="f2eec-166">Der restliche Bereich ist gerade vorhanden, sodass Sie sicherstellen können, dass Sie den neuen Code an die richtige Stelle setzen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="f2eec-167">Wechseln Sie zum **Reiter "Live"** , um die Änderungen anzuzeigen!</span><span class="sxs-lookup"><span data-stu-id="f2eec-167">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="f2eec-168">Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.</span><span class="sxs-lookup"><span data-stu-id="f2eec-168">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="f2eec-170">Die Hintergrundfarbe hinter dem **Start** -und **Kontakt** Link ist jetzt blau</span><span class="sxs-lookup"><span data-stu-id="f2eec-170">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f2eec-171">Wieder verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="f2eec-171">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="f2eec-172">In einem vorherigen Codeausschnitt hat eine Inlineformatvorlage eine Formatvorlage auf eine einzelne `<p>` Kategorie angewendet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-172">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="f2eec-173">Was ist, wenn Sie möchten, dass alle `<p>` Elemente auf Ihrer Webseite auf die gleiche Weise formatiert werden?</span><span class="sxs-lookup"><span data-stu-id="f2eec-173">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="f2eec-174">Sie müssten den Code in jeder einzelnen `<p>` Kategorie auf Ihrer Website kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-174">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="f2eec-175">Das ist viel Zeit und Mühe.</span><span class="sxs-lookup"><span data-stu-id="f2eec-175">That is a lot of time and effort.</span></span>  <span data-ttu-id="f2eec-176">Und wenn Sie eine Bearbeitung vornehmen mussten, müssten Sie jedes Tag erneut ändern.</span><span class="sxs-lookup"><span data-stu-id="f2eec-176">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="f2eec-177">Führen Sie die folgenden Aktionen aus, um ein **internes Stylesheet** zu verwenden, um das CSS einmal zu schreiben, damit es auf mehrere Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2eec-177">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="f2eec-178">Klicken Sie auf der Registerkarte Live auf **Kontakt** , um zur Kontaktseite zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-178">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="f2eec-179">Beachten Sie die Schriftart für " **Privat** " und " **Kontakt**".</span><span class="sxs-lookup"><span data-stu-id="f2eec-179">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="f2eec-181">Die Kontaktseite</span><span class="sxs-lookup"><span data-stu-id="f2eec-181">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-182">Wechseln Sie auf der **Registerkarte Editor**zu `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-182">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="f2eec-183">Fügen Sie den folgenden Code hinzu `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-183">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="f2eec-184">Beachten Sie, dass die Zeilen, die mit `<style>` und endet mit beginnen, das `</style>` hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-184">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="f2eec-185">Der andere Code ist gerade vorhanden, damit Sie wissen, wo der neue Code platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2eec-185">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="f2eec-186">Wechseln Sie zurück zur **Registerkarte Live**.</span><span class="sxs-lookup"><span data-stu-id="f2eec-186">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="f2eec-187">Wählen Sie **Kontakt** aus, um zur Kontaktseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f2eec-187">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="f2eec-188">Die Schriftart von " **Start** " und " **Kontakt** " hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f2eec-188">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Die Schriftart der Links für "Start" und "Kontakt" wurde geändert." lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="f2eec-190">Die Schriftart der Links für " **Start** " und " **Kontakt** " wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="f2eec-190">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f2eec-191">Grundlegendes zu internen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="f2eec-191">Understand internal stylesheets</span></span>  

<span data-ttu-id="f2eec-192">Interne Stylesheets wenden Formatvorlagen mithilfe von **Auswahlen**an.</span><span class="sxs-lookup"><span data-stu-id="f2eec-192">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="f2eec-193">Auswahlen sind Muster, die möglicherweise für ein oder mehrere HTML-Elemente gelten.</span><span class="sxs-lookup"><span data-stu-id="f2eec-193">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="f2eec-194">Im vorherigen Codeausschnitt wurde die folgende Formatvorlage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-194">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="f2eec-195">ist eine Auswahl, die in "jedes Element mit `<li>` einem `<a>` Element" übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f2eec-195">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="f2eec-196">Der Browser ändert die Schriftart der **Home** -und **Contact** -Links, weil jede der Kategorien mit dem Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-196">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="f2eec-197">ist eine **Deklaration**.</span><span class="sxs-lookup"><span data-stu-id="f2eec-197">is a **declaration**.</span></span>  <span data-ttu-id="f2eec-198">Eine Deklaration besteht aus zwei Teilen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-198">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="f2eec-199">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2eec-199">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f2eec-200">Die Eigenschaft beschreibt eine allgemeine Methode, mit der Sie die Formatvorlage des Elements ändern können.</span><span class="sxs-lookup"><span data-stu-id="f2eec-200">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="f2eec-201">value</span><span class="sxs-lookup"><span data-stu-id="f2eec-201">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f2eec-202">Der Wert beschreibt genau, wie sich die Formatvorlage des Elements ändern soll.</span><span class="sxs-lookup"><span data-stu-id="f2eec-202">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="f2eec-203">Gibt beispielsweise dem `font-family: 'Courier New', Courier, serif` Browser die folgende Anweisung aus: "die Schriftart von Elementen, die dem Muster entsprechen, auf festzulegen `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-203">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="f2eec-204">Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-204">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="f2eec-205">Wenn dies nicht möglich ist, verwenden Sie `serif` . "</span><span class="sxs-lookup"><span data-stu-id="f2eec-205">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="f2eec-206">Hinzufügen mehrerer Auswahlen zu einem RuleSet</span><span class="sxs-lookup"><span data-stu-id="f2eec-206">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="f2eec-207">Ein Block mit CSS-Code wie dem, was unten angezeigt wird, wird als **RuleSet**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-207">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="f2eec-208">Führen Sie die folgenden Aktionen aus, um einen RuleSet mithilfe von Kommas mehrere Auswahlen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-208">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="f2eec-209">Öffnen Sie auf der **Registerkarte Editor den Reiter** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-209">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="f2eec-210">Nach `li a` Typ `, h1` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-210">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="f2eec-211">Im vorherigen Codeausschnitt wird der Browser angewiesen, Formatvorlagen `<h1>` Elemente auf die gleiche Weise zu formatieren wie Elemente, die dem Muster entsprechen `li a` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-211">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="f2eec-212">Wechseln Sie zur **Registerkarte Live**.</span><span class="sxs-lookup"><span data-stu-id="f2eec-212">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="f2eec-213">Wählen Sie den Link **Kontakt** aus, um zur Kontaktseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f2eec-213">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="f2eec-214">**Kontaktieren Sie mich jetzt!**</span><span class="sxs-lookup"><span data-stu-id="f2eec-214">Now, **Contact Me!**</span></span> <span data-ttu-id="f2eec-215">hat die gleiche Schriftart wie die Navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="f2eec-215">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Der Text kontaktiere mich!  hat nun dieselbe Schriftart wie die Links für "Privat" und "Kontakt"" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="f2eec-218">Der Text **kontaktiere mich!**</span><span class="sxs-lookup"><span data-stu-id="f2eec-218">The text **Contact Me!**</span></span> <span data-ttu-id="f2eec-219">hat nun dieselbe Schriftart wie die Links für " **Privat** " und " **Kontakt** "</span><span class="sxs-lookup"><span data-stu-id="f2eec-219">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f2eec-220">Experimentieren mit devtools</span><span class="sxs-lookup"><span data-stu-id="f2eec-220">Experiment with DevTools</span></span>  

<span data-ttu-id="f2eec-221">Wenn Sie Ihre Reise fortsetzen, um ein Experte für Webentwicklung zu werden, können Sie feststellen, dass CSS schwierig ist.</span><span class="sxs-lookup"><span data-stu-id="f2eec-221">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="f2eec-222">Sie können einige CSS-Daten schreiben und davon ausgehen, dass Sie auf eine Art und Weise angezeigt werden, doch der Browser hat etwas völlig anderes.</span><span class="sxs-lookup"><span data-stu-id="f2eec-222">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="f2eec-223">Microsoft Edge devtools macht es einfach, mit Änderungen zu experimentieren und sofort zu sehen, wie sich die Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="f2eec-223">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="f2eec-224">Hinzufügen einer Deklaration zu einem vorhandenen rulet-Element in devtools</span><span class="sxs-lookup"><span data-stu-id="f2eec-224">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="f2eec-225">Führen Sie die folgenden Aktionen aus, um die Formatvorlage eines vorhandenen Elements zu durchlaufen, und fügen Sie eine Deklaration zu einem vorhandenen RuleSet hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2eec-225">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="f2eec-226">Zeigen Sie auf den Link " **Start** ", öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-226">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Überprüfen des Start Links" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="f2eec-228">Überprüfen des Start Links</span><span class="sxs-lookup"><span data-stu-id="f2eec-228">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f2eec-229">DevTools wird neben ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-229">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="f2eec-230">Der Code, der den Link "Start" darstellt, `<a href="/">Home</a>` wird in der DOM-Struktur blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="f2eec-230">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="f2eec-231">Der Codeausschnitt und die Vorschau sollten von den ersten [Schritten mit HTML und dem Dom][DevtoolsBeginnersHtml]vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="f2eec-231">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="f2eec-232">In der folgenden Abbildung wird die `font-family: 'Courier New', Courier, serif` Deklaration, die Sie zuvor hinzugefügt haben, auf `contact.html` der Registerkarte **Formatvorlagen** unter der DOM-Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-232">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur." lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="f2eec-234">Die Registerkarte " **Formatvorlagen** " befindet sich unterhalb der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2eec-234">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="f2eec-235">Wenn Ihr devtools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2eec-235">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur." lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="f2eec-237">Die Registerkarte " **Formatvorlagen** " befindet sich rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2eec-237">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f2eec-238">Wählen Sie die leere Zeile unten aus `font-family: 'Courier New', Courier, Serif` , um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-238">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Hinzufügen einer neuen Deklaration" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="f2eec-240">Hinzufügen einer neuen Deklaration</span><span class="sxs-lookup"><span data-stu-id="f2eec-240">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-241">Geben `color` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-241">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="f2eec-242">Die AutoVervollständigen-Benutzeroberfläche schlägt Optionen während der Eingabe vor.</span><span class="sxs-lookup"><span data-stu-id="f2eec-242">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Farbe eingeben" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="f2eec-244">Typ</span><span class="sxs-lookup"><span data-stu-id="f2eec-244">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-245">Geben `magenta` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-245">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="f2eec-246">Der gesamte Text auf der Kontaktseite ist jetzt Magenta.</span><span class="sxs-lookup"><span data-stu-id="f2eec-246">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Typ Magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="f2eec-248">Typ</span><span class="sxs-lookup"><span data-stu-id="f2eec-248">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="f2eec-249">Bearbeiten einer Deklaration in devtools</span><span class="sxs-lookup"><span data-stu-id="f2eec-249">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="f2eec-250">Führen Sie die folgenden Aktionen aus, um vorhandene Deklarationen in devtools zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f2eec-250">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="f2eec-251">Wählen Sie das Magenta-Quadrat neben aus `magenta` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-251">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="f2eec-252">Eine Farbauswahl wird eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-252">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Die Farbauswahl" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="f2eec-254">Die Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="f2eec-254">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-255">Verwenden Sie die Farbauswahl, um den Schriftart Text in eine Farbe zu ändern, die Ihnen gefällt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-255">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Ändern der Schriftfarbe in Lila mit der Farbauswahl" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="f2eec-257">Ändern der Schriftfarbe in Lila mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="f2eec-257">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f2eec-258">Hinzufügen eines neuen RuleSets in devtools</span><span class="sxs-lookup"><span data-stu-id="f2eec-258">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="f2eec-259">Führen Sie die folgenden Aktionen aus, um neue RuleSets in devtools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-259">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="f2eec-260">Wählen Sie **neue** Stilregel-Regel \ ( ![ neue Stilregel ][ImageNewStyleRuleIcon] \) aus, die sich neben **CLS**befindet.</span><span class="sxs-lookup"><span data-stu-id="f2eec-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="f2eec-261">Ein leerer RuleSet wird `a` als Auswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-261">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Hinzufügen einer neuen Regel" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="f2eec-263">Hinzufügen einer neuen Regel</span><span class="sxs-lookup"><span data-stu-id="f2eec-263">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-264">Ersetzen Sie `a` durch `a:hover`.</span><span class="sxs-lookup"><span data-stu-id="f2eec-264">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Ersetzen eines durch a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="f2eec-266">Ersetzen `a` durch</span><span class="sxs-lookup"><span data-stu-id="f2eec-266">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="f2eec-267">ist eine **Pseudoklasse**.</span><span class="sxs-lookup"><span data-stu-id="f2eec-267">is a **pseudo-class**.</span></span>  <span data-ttu-id="f2eec-268">Verwenden Sie Pseudoklassen für Formatvorlagenelemente, die möglicherweise spezielle Zustände eingeben.</span><span class="sxs-lookup"><span data-stu-id="f2eec-268">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="f2eec-269">Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie auf ein Element zeigen `<a>` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-269">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="f2eec-270">Wählen Sie zwischen den Klammern aus, um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-270">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="f2eec-271">Geben `background-color` Sie für den Deklarations Namen ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-271">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Hintergrundfarbe eingeben" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="f2eec-273">Typ</span><span class="sxs-lookup"><span data-stu-id="f2eec-273">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-274">Geben `green` Sie für den Deklarations Wert ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-274">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Typ grün" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="f2eec-276">Typ</span><span class="sxs-lookup"><span data-stu-id="f2eec-276">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-277">Zeigen Sie mit der Maus auf den Link " **Start** ".</span><span class="sxs-lookup"><span data-stu-id="f2eec-277">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="f2eec-278">Der Hintergrund des Links wird grün.</span><span class="sxs-lookup"><span data-stu-id="f2eec-278">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="f2eec-280">Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="f2eec-280">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f2eec-281">Wieder verwenden von Formatvorlagen auf mehreren Seiten mit externen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="f2eec-281">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="f2eec-282">In einem vorherigen Schritt haben Sie den folgenden Codeausschnitt als internes Stylesheet hinzugefügt `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-282">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="f2eec-283">Was ist, wenn Sie `index.html` die gleiche Weise formatieren möchten?</span><span class="sxs-lookup"><span data-stu-id="f2eec-283">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="f2eec-284">Was ist, wenn Sie über eine große Anzahl von Seiten verfügen, auf die Sie Ihre Formatvorlagen anwenden möchten?</span><span class="sxs-lookup"><span data-stu-id="f2eec-284">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="f2eec-285">Sie müssten das interne Stylesheet in jede einzelne Webseite auf Ihrer Website kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-285">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="f2eec-286">Führen Sie die folgenden Aktionen aus, um ein **externes Stylesheet** hinzuzufügen, das es Ihnen ermöglicht, Ihre CSS einmal zu schreiben und auf mehrere Seiten anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-286">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="f2eec-287">Laden Sie zunächst die Registerkarte "Live" neu, um die Änderungen zu entfernen, die Sie in devtools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="f2eec-287">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Nachdem Sie die Seite aktualisiert haben, sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden." lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="f2eec-289">Nachdem Sie die Seite aktualisiert haben, sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-289">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-290">Wechseln Sie zurück zur **Registerkarte Editor** , und öffnen Sie Sie `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-290">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="f2eec-292">contact.html</span><span class="sxs-lookup"><span data-stu-id="f2eec-292">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-293">Löschen Sie alles zwischen `<style>` und `</style>` , einschließlich `<style>` und `</style>` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-293">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Das Stil-Tag wurde entfernt" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="f2eec-295">Das Stil-Tag wurde entfernt</span><span class="sxs-lookup"><span data-stu-id="f2eec-295">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-296">Wechseln Sie zu `index.html` der Kategorie, und entfernen Sie Sie `style="background-color: aliceblue;"` `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-296">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="f2eec-297">Sie haben jetzt alle CSS entfernt, die Sie zuvor zu Ihrer Website hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="f2eec-297">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Die Inlineformatvorlage wurde aus dem NAV-Element entfernt" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="f2eec-299">Die Inlineformatvorlage wurde aus dem NAV-Element entfernt</span><span class="sxs-lookup"><span data-stu-id="f2eec-299">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-300">Wählen Sie **neue Datei**aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-300">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Dialogfeld ' neue Datei '" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="f2eec-302">Dialogfeld ' neue Datei '</span><span class="sxs-lookup"><span data-stu-id="f2eec-302">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-303">Ersetzen `cool-file.js` `style.css` Sie durch, und wählen Sie **Datei hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="f2eec-303">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type Style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="f2eec-305">Typ</span><span class="sxs-lookup"><span data-stu-id="f2eec-305">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-306">Fügen Sie der Datei den folgenden Codeausschnitt hinzu `style.css` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-306">Add the following code snippet to your `style.css` file.</span></span>  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Hinzufügen von Code zu Style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="f2eec-308">Hinzufügen von Code zu</span><span class="sxs-lookup"><span data-stu-id="f2eec-308">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="f2eec-309">Stellen Sie sicher, dass Sie ein externes Stylesheet erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f2eec-309">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="f2eec-310">Ihr HTML-Code ist sich nicht bewusst, dass es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2eec-310">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="f2eec-311">Öffnen Sie `index.html`.</span><span class="sxs-lookup"><span data-stu-id="f2eec-311">Open `index.html`.</span></span>  
1.  <span data-ttu-id="f2eec-312">Dem `<link rel="stylesheet" href="style.css">` HTML-Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-312">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link zu Style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="f2eec-314">Link zu</span><span class="sxs-lookup"><span data-stu-id="f2eec-314">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-315">Öffnen `contact.html` Sie die Datei, und fügen Sie den Link dort hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2eec-315">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link zu Style. CSS in contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="f2eec-317">Link zu `style.css` in</span><span class="sxs-lookup"><span data-stu-id="f2eec-317">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-318">Wechseln Sie zur **Registerkarte Live**.  Auf der Startseite befindet sich nun die gleiche Schriftart wie im letzten Abschnitt und ein blauer Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="f2eec-318">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Die Startseite" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="f2eec-320">Die Startseite</span><span class="sxs-lookup"><span data-stu-id="f2eec-320">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-321">Wählen Sie den Link **Kontakt** aus, um zur Kontaktseite zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-321">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="f2eec-322">Die Seite "Kontakt" hat dieselbe Formatierung wie die Startseite.</span><span class="sxs-lookup"><span data-stu-id="f2eec-322">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="f2eec-324">Die Kontaktseite</span><span class="sxs-lookup"><span data-stu-id="f2eec-324">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f2eec-325">Verwenden eines CSS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="f2eec-325">Use a CSS framework</span></span>  

<span data-ttu-id="f2eec-326">**CSS-Frameworks** sind Sammlungen von Formatvorlagen, die von anderen Entwicklern erstellt wurden, die das Erstellen attraktiver Websites vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-326">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="f2eec-327">Anstatt selbst Formatvorlagen zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f2eec-327">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="f2eec-328">Kopieren Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="f2eec-328">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="f2eec-329">Wechseln Sie zur Registerkarte Bearbeitung, und fügen Sie den Code in ein `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-329">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link zum Framework in contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="f2eec-331">Link zum Framework in</span><span class="sxs-lookup"><span data-stu-id="f2eec-331">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-332">Öffnen `index.html` Sie die Datei, und fügen Sie den Code dort hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2eec-332">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link zum Framework in index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="f2eec-334">Link zum Framework in</span><span class="sxs-lookup"><span data-stu-id="f2eec-334">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-335">Kehren Sie zur Registerkarte Live zurück, um Ihre Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-335">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="f2eec-336">Während die Hintergrundfarbe des `<nav>` Elements und die Schriftart der `<li>` `<a>` Elemente und identisch sind, hat sich die Schriftart der anderen Elemente geändert.</span><span class="sxs-lookup"><span data-stu-id="f2eec-336">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="f2eec-338">Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert</span><span class="sxs-lookup"><span data-stu-id="f2eec-338">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f2eec-339">Verwenden einer Klasse</span><span class="sxs-lookup"><span data-stu-id="f2eec-339">Use a class</span></span>  

<span data-ttu-id="f2eec-340">Im letzten Abschnitt haben Sie Ihren Webseiten Bootstrap hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-340">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="f2eec-341">CSS-Frameworks helfen Ihnen, wichtige Änderungen an Ihrer Seite mit sehr wenig Code vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-341">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="f2eec-342">Führen Sie die folgenden Aktionen aus, um die Kopfzeile zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f2eec-342">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="f2eec-343">Kopieren Sie den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-343">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="f2eec-344">Fügen Sie dem Tag in den vorherigen Codeausschnitt hinzu `<header>` `index.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-344">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Hinzufügen von Kursen in index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="f2eec-346">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="f2eec-346">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-347">Fügen Sie den Code zu Ihrem `<header>` Tag in hinzu `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-347">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Hinzufügen von Kursen in contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="f2eec-349">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="f2eec-349">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-350">Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  In der Kopfzeile befindet sich ein großes, graues Feld.</span><span class="sxs-lookup"><span data-stu-id="f2eec-350">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Die Kopfzeile hat nun ein großes, graues Feld um Sie herum" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="f2eec-352">Die Kopfzeile hat nun ein großes, graues Feld um Sie herum</span><span class="sxs-lookup"><span data-stu-id="f2eec-352">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="f2eec-353">Grundlegendes zu Klassen</span><span class="sxs-lookup"><span data-stu-id="f2eec-353">Understand classes</span></span>  

<span data-ttu-id="f2eec-354">Mit Klassen können Sie Auflistungen von Formatvorlagen beliebigen Elementen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-354">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="f2eec-355">Verwenden Sie den folgenden Codeausschnitt, um mehrere Formatvorlagen auf das Element anzuwenden, `<header>` nachdem Sie das `class` Attribut auf gesetzt haben `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-355">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="f2eec-356">Ein Vorteil einer Klasse besteht darin, dass Sie Formatvorlagen auf die gewünschten Elemente anwenden können.</span><span class="sxs-lookup"><span data-stu-id="f2eec-356">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="f2eec-357">Angenommen, Sie möchten die Hintergrundfarbe einiger `<p>` Elemente auf lila, aber nicht auf alle `<p>` Elemente einstellen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-357">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="f2eec-358">Verwenden Sie den folgenden Codeausschnitt, um die Formatvorlage in einer Klasse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f2eec-358">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="f2eec-359">Wenden Sie dann die Klasse nur auf die `<p>` Elemente an, die Sie formatieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f2eec-359">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="f2eec-360">Ausrichten von Elementen</span><span class="sxs-lookup"><span data-stu-id="f2eec-360">Align elements</span></span>  

<span data-ttu-id="f2eec-361">Führen Sie die folgenden Aktionen aus, um einen Bootstrap durchzuführen und Klassen zum Ausrichten von Elementen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-361">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="f2eec-362">Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-362">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="f2eec-363">`class="container-fluid"`Zu Ihrem Tag hinzufügen `<body>` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-363">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Hinzufügen der Container-Fluid Klasse" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="f2eec-365">Hinzufügen der `container-fluid` Klasse</span><span class="sxs-lookup"><span data-stu-id="f2eec-365">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-366">Umbrechen `<nav>` `<main>` von und Elementen in `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="f2eec-366">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="f2eec-367">Stellen Sie sicher, dass Sie `</div>` `</main>` die neue Kategorie ordnungsgemäß schließen, um Sie zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-367">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Hinzufügen einer Zeile" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="f2eec-369">Hinzufügen einer Zeile</span><span class="sxs-lookup"><span data-stu-id="f2eec-369">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-370">Fügen Sie `class="col-3"` Ihrem `<nav>` Tag und `class="col-9"` Ihrem `<main>` Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2eec-370">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Hinzufügen der Klassen Col-3 und Col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="f2eec-372">Hinzufügen der `col-3` und- `col-9` Klassen</span><span class="sxs-lookup"><span data-stu-id="f2eec-372">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f2eec-373">Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.</span><span class="sxs-lookup"><span data-stu-id="f2eec-373">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt." lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="f2eec-375">Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-375">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f2eec-376">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="f2eec-376">Next steps</span></span>  

<span data-ttu-id="f2eec-377">Herzlichen Glückwunsch, Sie haben es geschafft.</span><span class="sxs-lookup"><span data-stu-id="f2eec-377">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="f2eec-378">Die beste Methode, um die Web-Entwicklung zu verbessern, besteht darin, weitere Websites zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-378">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="f2eec-379">Machen Sie sich keine Sorgen, wenn Sie etwas kaputt machen.</span><span class="sxs-lookup"><span data-stu-id="f2eec-379">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="f2eec-380">Machen Sie einfach Spaß und lernen Sie so viel wie möglich auf dem Weg.</span><span class="sxs-lookup"><span data-stu-id="f2eec-380">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="f2eec-381">Weitere Informationen zum Formatieren von Webseiten finden Sie unter [Einführung in CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="f2eec-381">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="f2eec-382">Weitere Informationen dazu, wie Sie devtools verwenden können, um mit dem CSS einer Seite zu experimentieren, finden Sie unter [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="f2eec-382">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools für Anfänger: Erste Schritte mit HTML und dem Dom | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-gekocht-Amphibien | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "CSS-erste Schritte | MDN"  

> [!NOTE]
> <span data-ttu-id="f2eec-388">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2eec-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f2eec-389">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/css) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2eec-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f2eec-391">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f2eec-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
