---
description: Erste Schritte mit CSS
title: 'DevTools für Anfänger: Erste Schritte mit CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 6f34cfa8610848505c8aa795c4fab16e5d2a98ed
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564644"
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

# <a name="devtools-for-beginners-get-started-with-css"></a><span data-ttu-id="bb86d-104">DevTools für Anfänger: Erste Schritte mit CSS</span><span class="sxs-lookup"><span data-stu-id="bb86d-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="bb86d-105">In diesem Lernprogramm erfahren Sie, wie Sie css zum Formatieren einer Webseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="bb86d-106">Außerdem erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um mit CSS-Änderungen zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="bb86d-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="bb86d-107">Der folgende Artikel ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in dem Sie die Grundlagen der Webentwicklung und Microsoft Edge DevTools lernen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="bb86d-108">Sie erhalten praktische Erfahrung, indem Sie ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="bb86d-109">Sie müssen das erste Lernprogramm nicht abschließen, bevor Sie das zweite folgen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="bb86d-110">[Das Einrichten des Codes zeigt,](#set-up-your-code) wie Sie eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="bb86d-111">Dieses Lernprogramm ist für absolute Anfänger \*\*\*\* konzipiert und konzentriert sich sowohl auf die Grundlagen der Webentwicklung als auch auf die Grundlagen der Verwendung von DevTools zum Experimentieren mit CSS.</span><span class="sxs-lookup"><span data-stu-id="bb86d-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="bb86d-112">Wenn Sie ein Lernprogramm wünschen, das sich nur auf DevTools konzentriert, navigieren Sie zu Erste Schritte [Anzeigen und][DevtoolsCssIndex]Ändern von CSS .</span><span class="sxs-lookup"><span data-stu-id="bb86d-112">If you want a tutorial that only focuses on DevTools, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="bb86d-113">Am Anfang des Lernprogramms sollte Ihre Website wie die folgende Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Wie Ihre Website derzeit aussieht" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="bb86d-115">Wie Ihre Website derzeit aussieht</span><span class="sxs-lookup"><span data-stu-id="bb86d-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="bb86d-116">Nachdem Sie das Lernprogramm abgeschlossen haben, sollte Ihre Website wie die folgende Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Wie Ihre Website am Ende des Lernprogramms aussehen soll" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="bb86d-118">Wie Ihre Website am Ende des Lernprogramms aussehen soll</span><span class="sxs-lookup"><span data-stu-id="bb86d-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <a name="goals"></a><span data-ttu-id="bb86d-119">Ziele</span><span class="sxs-lookup"><span data-stu-id="bb86d-119">Goals</span></span>  

<span data-ttu-id="bb86d-120">Folgen Sie diesem Lernprogramm, um die folgenden Konzepte und Aufgaben besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="bb86d-121">Verwenden von CSS zum Formatieren einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="bb86d-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="bb86d-122">Verwenden von Microsoft Edge DevTools zum Experimentieren mit CSS.</span><span class="sxs-lookup"><span data-stu-id="bb86d-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="bb86d-123">Der Unterschied zwischen CSS- und CSS-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="bb86d-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="bb86d-124">Sie erstellen eine echte Website.</span><span class="sxs-lookup"><span data-stu-id="bb86d-124">You are building a real website.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="bb86d-125">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="bb86d-125">Prerequisites</span></span>  

<span data-ttu-id="bb86d-126">Bevor Sie dieses Lernprogramm versuchen, müssen Sie die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="bb86d-127">Führen Erste Schritte html und das [DOM][DevtoolsBeginnersHtml] aus, oder stellen Sie sicher, dass Sie ein Verständnis von HTML und dom haben, ähnlich dem, was in diesem Lernprogramm vermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bb86d-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="bb86d-128">Laden Sie [den Microsoft Edge][MicrosoftEdgeInsider] herunter.</span><span class="sxs-lookup"><span data-stu-id="bb86d-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="bb86d-129">Im folgenden Lernprogramm wird eine Reihe von Webentwicklungstools verwendet, die als Microsoft Edge DevTools bezeichnet werden und in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb86d-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="bb86d-130">Einrichten des Codes</span><span class="sxs-lookup"><span data-stu-id="bb86d-130">Set up your code</span></span>  

<span data-ttu-id="bb86d-131">Zum Erstellen Ihrer Website müssen Sie zunächst die folgenden Aktionen ausführen, um Ihren Code einrichten zu können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="bb86d-132">Wenn Sie das erste Lernprogramm in der Reihe bereits abgeschlossen haben, fahren Sie mit dem nächsten Abschnitt fort.</span><span class="sxs-lookup"><span data-stu-id="bb86d-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="bb86d-133">Verwenden Sie weiterhin Ihren Code aus dem letzten Lernprogramm, [Erste Schritte HTML und dem DOM verwenden.][DevtoolsBeginnersHtml]</span><span class="sxs-lookup"><span data-stu-id="bb86d-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="bb86d-134">Öffnen Sie [den Quellcode][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="bb86d-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="bb86d-135">Auf die Fokusregisterkarte Ihres Browsers wird als **Bearbeitungsregisterkarte verwiesen.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Registerkarte "Bearbeiten"" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="bb86d-137">Registerkarte **"Bearbeiten"**</span><span class="sxs-lookup"><span data-stu-id="bb86d-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-138">Wählen **Sie 4-amphibisch aus.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="bb86d-139">Ein Menü wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menü Project Optionen" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="bb86d-141">Menü Project Optionen</span><span class="sxs-lookup"><span data-stu-id="bb86d-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="bb86d-142">Wählen **Sie #A0 Project**aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="bb86d-143">Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="bb86d-144">Glitch generiert einen zufälligen Namen für das neue Projekt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="bb86d-145">Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-145">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="bb86d-146">Eine weitere Registerkarte wird mit einer Liveansicht Ihrer Website geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bb86d-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="bb86d-147">Auf die Registerkarte "Fokus" Ihres Browsers wird als **Liveregisterkarte verwiesen.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Die Registerkarte Live" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="bb86d-149">Die **Registerkarte Live**</span><span class="sxs-lookup"><span data-stu-id="bb86d-149">The **live tab**</span></span>  
    :::image-end:::  

## <a name="understand-css"></a><span data-ttu-id="bb86d-150">Verstehen von CSS</span><span class="sxs-lookup"><span data-stu-id="bb86d-150">Understand CSS</span></span>  

<span data-ttu-id="bb86d-151">**CSS** ist eine Computersprache, die das Layout und formatieren von Webseiten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="bb86d-152">Die folgende Abbildung ist ein Absatz mit einem Rahmen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Der Text wurde mit CSS formatiert" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="bb86d-154">Der Text wurde mit CSS formatiert</span><span class="sxs-lookup"><span data-stu-id="bb86d-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="bb86d-155">Der folgende Codeausschnitt ist der HTML- und CSS-Code, der zum Erstellen des Absatzes in der vorherigen Abbildung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb86d-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="bb86d-156">sieht wahrscheinlich neu für Sie aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-156">probably looks new to you.</span></span>  <span data-ttu-id="bb86d-157">Der Rest sollte vertraut aussehen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-157">The rest should look familiar.</span></span>  <span data-ttu-id="bb86d-158">Wenn dies [nicht der Erste Schritte, müssen][DevtoolsBeginnersHtml] Sie html und das DOM verwenden, bevor Sie die folgenden Abschnitte versuchen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <a name="add-inline-styles"></a><span data-ttu-id="bb86d-159">Hinzufügen von Inlineformatvorlagen</span><span class="sxs-lookup"><span data-stu-id="bb86d-159">Add inline styles</span></span>  

<span data-ttu-id="bb86d-160">Führen Sie die folgenden Aktionen aus, um **Inlineformatvorlagen zum** Anwenden von Formatvorlagen auf ein einzelnes Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="bb86d-161">Wechseln Sie zurück zur Bearbeitungsregisterkarte, und öffnen Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="bb86d-163">Öffnen `index.html` auf der Bearbeitungsregisterkarte</span><span class="sxs-lookup"><span data-stu-id="bb86d-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-164">Hinzufügen `style="background-color: aliceblue;"` zu Ihrer `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="bb86d-165">Im folgenden Codeblock ist die vierte Codezeile die, die Sie ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="bb86d-166">Der Rest ist einfach da, damit Sie sicherstellen können, dass Sie den neuen Code an der richtigen Stelle platzieren.</span><span class="sxs-lookup"><span data-stu-id="bb86d-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
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
    
1.  <span data-ttu-id="bb86d-167">Navigieren Sie zur Registerkarte Live, um die **Änderungen anzeigen zu können.**  Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.</span><span class="sxs-lookup"><span data-stu-id="bb86d-167">To display the changes, navigate to the **live tab**.  The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Die Hintergrundfarbe hinter den Links "Start" und "Kontakt" ist jetzt blau." lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="bb86d-169">Die Hintergrundfarbe hinter den **Links "Start"** **und** "Kontakt" ist jetzt blau.</span><span class="sxs-lookup"><span data-stu-id="bb86d-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a><span data-ttu-id="bb86d-170">Erneutes Verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="bb86d-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="bb86d-171">In einem vorherigen Codeausschnitt hat ein Inlineformat auf ein einzelnes Tag eine `<p>` Formatvorlage angewendet.</span><span class="sxs-lookup"><span data-stu-id="bb86d-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="bb86d-172">Was passiert, wenn alle Elemente auf Ihrer Webseite auf die `<p>` gleiche Weise gestaltet werden sollen?</span><span class="sxs-lookup"><span data-stu-id="bb86d-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="bb86d-173">Sie müssen den Code kopieren und in jedes einzelne `<p>` Tag auf Ihrer Website einfügen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-173">You have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="bb86d-174">Das ist viel Zeit und Aufwand.</span><span class="sxs-lookup"><span data-stu-id="bb86d-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="bb86d-175">Und wenn Sie eine Bearbeitung erstellen müssen, müssen Sie jedes Tag erneut ändern.</span><span class="sxs-lookup"><span data-stu-id="bb86d-175">And, if you needed to make an edit, you have to change every tag again.</span></span>  <span data-ttu-id="bb86d-176">Führen Sie die folgenden Aktionen aus, um ein **internes Stylesheet zu** verwenden, um Ihre CSS einmal so zu schreiben, dass sie auf mehrere Elemente angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb86d-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="bb86d-177">Klicken Sie auf der Registerkarte Live auf **Kontakt,** um zur Kontaktseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="bb86d-177">In the live tab, choose **Contact** to navigate to the contact page.</span></span>  <span data-ttu-id="bb86d-178">Beachten Sie die Schriftart **von Home** und **Contact**.</span><span class="sxs-lookup"><span data-stu-id="bb86d-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Die Seite "Kontakt"" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="bb86d-180">Die Seite "Kontakt"</span><span class="sxs-lookup"><span data-stu-id="bb86d-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-181">Öffnen Sie **auf der Registerkarte Editor** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-181">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="bb86d-182">Fügen Sie den folgenden Code zu `contact.html` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="bb86d-183">Denken Sie daran, dass die Zeilen, die mit beginnen und mit `<style>` `</style>` enden, das sind, was Sie hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="bb86d-184">Der andere Code ist nur da, damit Sie wissen, wo sie den neuen Code setzen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-184">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="bb86d-185">Wechseln Sie zurück zur **Registerkarte Live.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="bb86d-186">Wählen **Sie Kontakt** aus, um zur Kontaktseite zurück zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="bb86d-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="bb86d-187">Die Schriftart von **Home** und **Contact** hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="bb86d-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Die Schriftart der Links "Start" und "Kontakt" wurde geändert." lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="bb86d-189">Die Schriftart der **Links "Start"** und **"Kontakt"** wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="bb86d-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a><span data-ttu-id="bb86d-190">Verstehen interner Stylesheets</span><span class="sxs-lookup"><span data-stu-id="bb86d-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="bb86d-191">Interne Stylesheets wenden Formatvorlagen mithilfe **von Selektoren an.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="bb86d-192">Selektoren sind Muster, die auf ein oder mehrere HTML-Elemente angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="bb86d-193">Im vorherigen Codeausschnitt wurde die folgende Formatvorlage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="bb86d-194">ist ein Selektor, der in "jedes `<li>` Element, das ein Element `<a>` enthält" übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="bb86d-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="bb86d-195">Der Browser ändert die Schriftart der Links **"Start"** und **"Kontakt",** da jede Taggruppe dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="bb86d-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="bb86d-196">ist eine **Deklaration**.</span><span class="sxs-lookup"><span data-stu-id="bb86d-196">is a **declaration**.</span></span>  <span data-ttu-id="bb86d-197">Eine Deklaration besteht aus den folgenden beiden Teilen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="bb86d-198">property</span><span class="sxs-lookup"><span data-stu-id="bb86d-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb86d-199">Die Eigenschaft beschreibt eine allgemeine Möglichkeit, die Formatvorlage des Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bb86d-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="bb86d-200">value</span><span class="sxs-lookup"><span data-stu-id="bb86d-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb86d-201">Der Wert beschreibt genau, wie sich die Formatvorlage des Elements ändern soll.</span><span class="sxs-lookup"><span data-stu-id="bb86d-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="bb86d-202">Gibt dem Browser beispielsweise die folgende Anweisung: "Legen Sie die Schriftart von Elementen `font-family: 'Courier New', Courier, serif` fest, die mit dem Muster `li a` übereinstimmen auf `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="bb86d-203">Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="bb86d-204">Wenn dies nicht verfügbar ist, verwenden Sie `serif` ."</span><span class="sxs-lookup"><span data-stu-id="bb86d-204">If that is not available, use `serif`."</span></span>  

### <a name="add-multiple-selectors-to-a-ruleset"></a><span data-ttu-id="bb86d-205">Hinzufügen mehrerer Selektoren zu einem Regelsatz</span><span class="sxs-lookup"><span data-stu-id="bb86d-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="bb86d-206">Ein Block von CSS-Code wie der folgende Codeausschnitt wird als **Regelsatz bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-206">A block of CSS code like the following code snippet is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="bb86d-207">Führen Sie die folgenden Aktionen aus, um Kommas zum Hinzufügen mehrerer Selektoren zu einem Regelsatz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="bb86d-208">Öffnen Sie **auf der Registerkarte Editor** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="bb86d-209">Nach `li a` dem Typ `, h1` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="bb86d-210">Der vorherige Codeausschnitt weist den Browser an, Elemente auf die gleiche Weise zu formatieren wie `<h1>` Elemente, die mit dem Muster `li a` übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="bb86d-211">Navigieren Sie zur **Registerkarte Live**.</span><span class="sxs-lookup"><span data-stu-id="bb86d-211">Navigate to the **live tab**.</span></span>  
1.  <span data-ttu-id="bb86d-212">Wählen Sie den **Link Kontakt** aus, um zur Kontaktseite zurück zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="bb86d-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="bb86d-213">Wenden Sie sich **jetzt an mich!**</span><span class="sxs-lookup"><span data-stu-id="bb86d-213">Now, **Contact Me!**</span></span> <span data-ttu-id="bb86d-214">hat dieselbe Schriftart wie die Navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="bb86d-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Der Text Contact Me!  hat jetzt die gleiche Schriftart wie die Links "Start" und "Kontakt"" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="bb86d-217">Der Text **Contact Me!**</span><span class="sxs-lookup"><span data-stu-id="bb86d-217">The text **Contact Me!**</span></span> <span data-ttu-id="bb86d-218">hat jetzt die gleiche Schriftart wie die **Links "Start"** **und "Kontakt"**</span><span class="sxs-lookup"><span data-stu-id="bb86d-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a><span data-ttu-id="bb86d-219">Experimentieren mit DevTools</span><span class="sxs-lookup"><span data-stu-id="bb86d-219">Experiment with DevTools</span></span>  

<span data-ttu-id="bb86d-220">Wenn Sie ihre Reise fortsetzen, um ein Experte für Webentwicklung zu werden, ist CSS möglicherweise kompliziert.</span><span class="sxs-lookup"><span data-stu-id="bb86d-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="bb86d-221">Sie können css schreiben und erwarten, dass es auf eine Weise angezeigt wird, aber der Browser macht etwas völlig anderes.</span><span class="sxs-lookup"><span data-stu-id="bb86d-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="bb86d-222">Microsoft Edge DevTools erleichtert das Experimentieren mit Änderungen und zeigt sofort an, wie sich die Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="bb86d-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately display how the changes affect the page.</span></span>  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a><span data-ttu-id="bb86d-223">Hinzufügen einer Deklaration zu einem vorhandenen Regelt in DevTools</span><span class="sxs-lookup"><span data-stu-id="bb86d-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="bb86d-224">Führen Sie die folgenden Aktionen aus, um die Formatvorlage eines vorhandenen Elements zu iterieren, fügen Sie einem vorhandenen Regelsatz eine Deklaration hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="bb86d-225">Zeigen Sie auf **den Startlink,** öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-225">Hover on the **Home** link, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Überprüfen des Links "Start"" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="bb86d-227">Überprüfen des Links "Start"</span><span class="sxs-lookup"><span data-stu-id="bb86d-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="bb86d-228">DevTools wird neben Ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bb86d-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="bb86d-229">Der Code, der den Startlink darstellt, ist in der `<a href="/">Home</a>` DOM-Struktur blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="bb86d-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="bb86d-230">Der Codeausschnitt und die Vorschau sollten aus der Erste Schritte mit HTML und [dem DOM vertraut sein.][DevtoolsBeginnersHtml]</span><span class="sxs-lookup"><span data-stu-id="bb86d-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="bb86d-231">In der folgenden Abbildung wird die zuvor hinzugefügte Deklaration auf der `font-family: 'Courier New', Courier, serif` `contact.html` Registerkarte **Formatvorlagen** unterhalb der DOM-Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is displayed in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Die Registerkarte Formatvorlagen befindet sich unterhalb der DOM-Struktur." lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="bb86d-233">Die **Registerkarte Formatvorlagen** befindet sich unterhalb der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb86d-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="bb86d-234">Wenn Ihr DevTools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb86d-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Die Registerkarte Formatvorlagen befindet sich rechts neben der DOM-Struktur." lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="bb86d-236">Die **Registerkarte Formatvorlagen** befindet sich rechts neben der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb86d-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="bb86d-237">Wählen Sie unten die leere Zeile `font-family: 'Courier New', Courier, Serif` aus, um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Hinzufügen einer neuen Deklaration" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="bb86d-239">Hinzufügen einer neuen Deklaration</span><span class="sxs-lookup"><span data-stu-id="bb86d-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-240">Geben `color` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="bb86d-241">Die Benutzeroberfläche für die automatische Vervollständigung schlägt Bei der Eingabe Optionen vor.</span><span class="sxs-lookup"><span data-stu-id="bb86d-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Typfarbe" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="bb86d-243">Typ</span><span class="sxs-lookup"><span data-stu-id="bb86d-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-244">Geben `magenta` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="bb86d-245">Der ganze Text auf der Kontaktseite ist jetzt Magenta.</span><span class="sxs-lookup"><span data-stu-id="bb86d-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Typ Magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="bb86d-247">Typ</span><span class="sxs-lookup"><span data-stu-id="bb86d-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a><span data-ttu-id="bb86d-248">Bearbeiten einer Deklaration in DevTools</span><span class="sxs-lookup"><span data-stu-id="bb86d-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="bb86d-249">Führen Sie die folgenden Aktionen aus, um vorhandene Deklarationen in DevTools zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bb86d-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="bb86d-250">Wählen Sie das magentafarbene Quadrat neben `magenta` aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="bb86d-251">Eine Farbauswahl wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Die Farbauswahl" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="bb86d-253">Die Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="bb86d-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-254">Verwenden Sie die Farbauswahl, um den Schrifttext in eine Farbe zu ändern, die Ihnen gefällt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Ändern der Schriftfarbe in Lila mit der Farbauswahl" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="bb86d-256">Ändern der Schriftfarbe in Lila mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="bb86d-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a><span data-ttu-id="bb86d-257">Hinzufügen eines neuen Regelsets in DevTools</span><span class="sxs-lookup"><span data-stu-id="bb86d-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="bb86d-258">Führen Sie die folgenden Aktionen aus, um neue Regelsätze in DevTools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="bb86d-259">Wählen **Sie Neue Formatvorlageregel** \( ![ Neue Formatregel ](../media/new-style-rule-icon.msft.png) \) aus, die sich neben **CLS befindet.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-259">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) which is next to **.cls**.</span></span>  <span data-ttu-id="bb86d-260">Als Auswahl wird ein leeres `a` Regelset angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Hinzufügen einer neuen Regel" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="bb86d-262">Hinzufügen einer neuen Regel</span><span class="sxs-lookup"><span data-stu-id="bb86d-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-263">Ersetzen Sie `a` durch `a:hover`.</span><span class="sxs-lookup"><span data-stu-id="bb86d-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Ersetzen sie durch a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="bb86d-265">Ersetzen `a` durch</span><span class="sxs-lookup"><span data-stu-id="bb86d-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="bb86d-266">ist eine **Pseudoklasse**.</span><span class="sxs-lookup"><span data-stu-id="bb86d-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="bb86d-267">Verwenden Sie Pseudoklassen für Stilelemente, die spezielle Zustände eingeben können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="bb86d-268">Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie mit dem Mauszeiger auf ein Element `<a>` zeigen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="bb86d-269">Wählen Sie zwischen den Klammern aus, um eine neue Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="bb86d-270">Geben `background-color` Sie den Deklarationsnamen ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Geben Sie Hintergrundfarbe ein" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="bb86d-272">Typ</span><span class="sxs-lookup"><span data-stu-id="bb86d-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-273">Geben `green` Sie den Deklarationswert ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="bb86d-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Typ grün" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="bb86d-275">Typ</span><span class="sxs-lookup"><span data-stu-id="bb86d-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-276">Zeigen Sie mit der Maus über den **Startlink.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="bb86d-277">Der Hintergrund des Links wird grün.</span><span class="sxs-lookup"><span data-stu-id="bb86d-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Zeigen Sie auf den Startlink, um den grünen Hintergrund zu zeigen." lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="bb86d-279">Zeigen Sie auf den Startlink, um den grünen Hintergrund zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-279">Hover on the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a><span data-ttu-id="bb86d-280">Erneutes Verwenden von Formatvorlagen über Seiten hinweg mit externen Stylesheets</span><span class="sxs-lookup"><span data-stu-id="bb86d-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="bb86d-281">In einem vorherigen Schritt haben Sie den folgenden Codeausschnitt als internes Stylesheet zu `contact.html` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="bb86d-282">Was passiert, wenn Sie die gleiche `index.html` Art und Weise formatieren möchten?</span><span class="sxs-lookup"><span data-stu-id="bb86d-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="bb86d-283">Was passiert, wenn Sie eine große Anzahl von Seiten hatten, auf die Sie Ihre Formatvorlagen anwenden wollten?</span><span class="sxs-lookup"><span data-stu-id="bb86d-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="bb86d-284">Sie müssen das interne Stylesheet kopieren und in jede einzelne Webseite auf Ihrer Website einfügen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-284">You have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="bb86d-285">Führen Sie die folgenden Aktionen aus, um ein **externes Stylesheet** hinzuzufügen, damit Sie Ihre CSS einmal schreiben und auf mehrere Seiten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="bb86d-286">Aktualisieren Sie zunächst die Registerkarte Live, um die Änderungen zu entfernen, die Sie in DevTools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="bb86d-286">First, refresh the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Nachdem Sie die Seite aktualisiert haben, sind die In DevTools vorgenommenen Änderungen nicht mehr verfügbar." lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="bb86d-288">Nachdem Sie die Seite aktualisiert haben, sind die In DevTools vorgenommenen Änderungen nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb86d-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-289">Wechseln Sie zurück zur **Registerkarte Editor, und** öffnen Sie `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="bb86d-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="bb86d-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-292">Löschen Sie alles zwischen `<style>` und , einschließlich und `</style>` `<style>` `</style>` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Das Styletag wurde entfernt." lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="bb86d-294">Das Styletag wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-295">Öffnen `index.html` und entfernen Sie das `style="background-color: aliceblue;"` `<nav>` Tag.</span><span class="sxs-lookup"><span data-stu-id="bb86d-295">Open `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="bb86d-296">Sie haben nun alle CSS entfernt, die Sie ihrer Website zuvor hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="bb86d-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Die Inlineformatvorlage wurde aus dem Navigationselement entfernt." lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="bb86d-298">Die Inlineformatvorlage wurde aus dem Navigationselement entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-299">Wählen **Sie Neue Datei aus.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Das Dialogfeld neue Datei" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="bb86d-301">Das Dialogfeld neue Datei</span><span class="sxs-lookup"><span data-stu-id="bb86d-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-302">Ersetzen `cool-file.js` Sie `style.css` durch, und wählen Sie Datei hinzufügen **aus.**</span><span class="sxs-lookup"><span data-stu-id="bb86d-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style.css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="bb86d-304">Typ</span><span class="sxs-lookup"><span data-stu-id="bb86d-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-305">Fügen Sie der Datei den folgenden Codeausschnitt `style.css` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-305">Add the following code snippet to your `style.css` file.</span></span>  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Hinzufügen von Code zu style.css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="bb86d-307">Hinzufügen von Code zu</span><span class="sxs-lookup"><span data-stu-id="bb86d-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="bb86d-308">Stellen Sie sicher, dass Sie ein externes Stylesheet erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bb86d-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="bb86d-309">Ihre HTML ist sich nicht bewusst, dass sie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bb86d-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="bb86d-310">Öffnen Sie `index.html`.</span><span class="sxs-lookup"><span data-stu-id="bb86d-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="bb86d-311">Fügen `<link rel="stylesheet" href="style.css">` Sie Zu Ihrem HTML hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link zu style.css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="bb86d-313">Link zu</span><span class="sxs-lookup"><span data-stu-id="bb86d-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-314">Öffnen Sie `contact.html` die Datei, und fügen Sie den Link dort hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link zu style.css in contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="bb86d-316">Link zu `style.css` in</span><span class="sxs-lookup"><span data-stu-id="bb86d-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-317">Navigieren Sie zur **Registerkarte Live**.  Die Startseite hat nun die gleiche Schriftart aus dem letzten Abschnitt und einen blauen Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="bb86d-317">Navigate to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Die Homepage" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="bb86d-319">Die Homepage</span><span class="sxs-lookup"><span data-stu-id="bb86d-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-320">Wählen Sie den **Link Kontakt** aus, um zur Kontaktseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="bb86d-320">Choose the **Contact** link to navigate to the contact page.</span></span>  <span data-ttu-id="bb86d-321">Die Kontaktseite hat die gleiche Formatierung wie die Homepage.</span><span class="sxs-lookup"><span data-stu-id="bb86d-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="bb86d-323">Die Kontaktseite</span><span class="sxs-lookup"><span data-stu-id="bb86d-323">The contact page</span></span>  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a><span data-ttu-id="bb86d-324">Verwenden eines CSS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="bb86d-324">Use a CSS framework</span></span>  

<span data-ttu-id="bb86d-325">**CSS-Frameworks** sind Von anderen Entwicklern erstellte Stilsammlungen, die das Erstellen attraktiver Websites vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="bb86d-326">Anstatt Formatvorlagen selbst zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bb86d-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="bb86d-327">Kopieren Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="bb86d-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="bb86d-328">Öffnen Sie die Bearbeitungsregisterkarte, und fügen Sie den Code in `contact.html` ein.</span><span class="sxs-lookup"><span data-stu-id="bb86d-328">Open the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link zum Framework in contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="bb86d-330">Link zum Framework in</span><span class="sxs-lookup"><span data-stu-id="bb86d-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-331">Öffnen Sie `index.html` die Datei, und fügen Sie den Code dort hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link zum Framework in index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="bb86d-333">Link zum Framework in</span><span class="sxs-lookup"><span data-stu-id="bb86d-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-334">Wechseln Sie zurück zur Registerkarte Live, um Ihre Änderungen zu sehen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="bb86d-335">Während die Hintergrundfarbe des Elements und die Schriftart der und-Elemente identisch sind, hat sich die Schriftart `<nav>` `<li>` der anderen Elemente `<a>` geändert.</span><span class="sxs-lookup"><span data-stu-id="bb86d-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Einige Schriftarten auf der Startseite wurden aufgrund des Frameworks geändert." lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="bb86d-337">Einige Schriftarten auf der Startseite wurden aufgrund des Frameworks geändert.</span><span class="sxs-lookup"><span data-stu-id="bb86d-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <a name="use-a-class"></a><span data-ttu-id="bb86d-338">Verwenden einer Klasse</span><span class="sxs-lookup"><span data-stu-id="bb86d-338">Use a class</span></span>  

<span data-ttu-id="bb86d-339">Im letzten Abschnitt haben Sie Bootstrap zu Ihren Webseiten hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="bb86d-340">MIT CSS-Frameworks können Sie wichtige Änderungen an Ihrer Seite mit sehr wenig Code vornehmen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="bb86d-341">Führen Sie die folgenden Aktionen aus, um den Header zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bb86d-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="bb86d-342">Kopieren Sie den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="bb86d-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="bb86d-343">Fügen Sie dem Tag in den vorherigen `<header>` Codeausschnitt `index.html` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Hinzufügen von Klassen in index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="bb86d-345">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="bb86d-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-346">Fügen Sie den Code zu Ihrem `<header>` Tag in `contact.html` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Hinzufügen von Klassen in contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="bb86d-348">Hinzufügen von Klassen in</span><span class="sxs-lookup"><span data-stu-id="bb86d-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-349">Zeigen Sie Ihre Änderungen auf der Registerkarte Live an.  Es gibt ein großes, graues Feld um ihre Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="bb86d-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Der Header hat jetzt ein großes, graues Feld um ihn herum." lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="bb86d-351">Der Header hat jetzt ein großes, graues Feld um ihn herum.</span><span class="sxs-lookup"><span data-stu-id="bb86d-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <a name="understand-classes"></a><span data-ttu-id="bb86d-352">Verstehen von Klassen</span><span class="sxs-lookup"><span data-stu-id="bb86d-352">Understand classes</span></span>  

<span data-ttu-id="bb86d-353">Mit Klassen können Sie Beliebigen Elementen Auflistungen von Formatvorlagen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="bb86d-354">Verwenden Sie den folgenden Codeausschnitt, um mehrere Formatvorlagen auf das Element `<header>` anzuwenden, nachdem Sie das `class` Attribut auf festgelegt `jumbotron` haben.</span><span class="sxs-lookup"><span data-stu-id="bb86d-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="bb86d-355">Ein Vorteil einer Klasse besteht in der Möglichkeit, Formatvorlagen auf alle elemente anzuwenden, die Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="bb86d-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="bb86d-356">Angenommen, Sie möchten die Hintergrundfarbe einiger Elemente auf Lila festlegen, aber `<p>` nicht auf alle `<p>` Elemente.</span><span class="sxs-lookup"><span data-stu-id="bb86d-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="bb86d-357">Verwenden Sie den folgenden Codeausschnitt, um die Formatvorlage in einer Klasse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bb86d-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="bb86d-358">Wenden Sie als Nächstes die Klasse nur auf die `<p>` Elemente an, die Sie formaten möchten.</span><span class="sxs-lookup"><span data-stu-id="bb86d-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a><span data-ttu-id="bb86d-359">Ausrichten von Elementen</span><span class="sxs-lookup"><span data-stu-id="bb86d-359">Align elements</span></span>  

<span data-ttu-id="bb86d-360">Führen Sie die folgenden Aktionen zum Bootstrapen aus und stellen Sie Klassen zum Ausrichten von Elementen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bb86d-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="bb86d-361">Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie `index.html` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="bb86d-362">Hinzufügen `class="container-fluid"` zu Ihrem `<body>` Tag.</span><span class="sxs-lookup"><span data-stu-id="bb86d-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Hinzufügen der Container-Fluid-Klasse" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="bb86d-364">Hinzufügen der `container-fluid` Klasse</span><span class="sxs-lookup"><span data-stu-id="bb86d-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-365">`<nav>`Umschließen Sie Ihre und `<main>` -Elemente in `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="bb86d-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="bb86d-366">Stellen Sie sicher, dass `</div>` Sie `</main>` nach, um das neue Tag ordnungsgemäß zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bb86d-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Hinzufügen einer Zeile" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="bb86d-368">Hinzufügen einer Zeile</span><span class="sxs-lookup"><span data-stu-id="bb86d-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-369">Fügen `class="col-3"` Sie Ihrem Tag und Ihrem Tag `<nav>` `class="col-9"` `<main>` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bb86d-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Hinzufügen der Klassen col-3 und col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="bb86d-371">Hinzufügen der `col-3` `col-9` Und-Klassen</span><span class="sxs-lookup"><span data-stu-id="bb86d-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bb86d-372">Zeigen Sie Ihre Änderungen auf der Registerkarte Live an.</span><span class="sxs-lookup"><span data-stu-id="bb86d-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Der Navigationsinhalt befindet sich jetzt links vom Hauptinhalt" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="bb86d-374">Der Navigationsinhalt befindet sich jetzt links vom Hauptinhalt</span><span class="sxs-lookup"><span data-stu-id="bb86d-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="bb86d-375">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="bb86d-375">Next steps</span></span>  

<span data-ttu-id="bb86d-376">Herzlichen Glückwunsch, Sie sind fertig.</span><span class="sxs-lookup"><span data-stu-id="bb86d-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="bb86d-377">Die beste Möglichkeit, die Webentwicklung zu verbessern, ist das Erstellen von weiteren Websites.</span><span class="sxs-lookup"><span data-stu-id="bb86d-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="bb86d-378">Machen Sie sich keine Gedanken über das Brechen von Zeug.</span><span class="sxs-lookup"><span data-stu-id="bb86d-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="bb86d-379">Machen Sie einfach Spaß und lernen Sie so viel wie möglich auf dem Weg.</span><span class="sxs-lookup"><span data-stu-id="bb86d-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="bb86d-380">Weitere Informationen zum Formatieren von Webseiten finden Sie unter [Einführung in CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="bb86d-380">To learn more about styling web pages, navigate to [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="bb86d-381">Weitere Informationen zur Verwendung von DevTools zum Experimentieren mit dem CSS einer Seite finden Sie unter Erste Schritte Anzeigen und Ändern von [CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="bb86d-381">To learn more about how to use DevTools to experiment with the CSS of a page, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bb86d-382">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="bb86d-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM | Microsoft-Dokumentation"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte Mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - 4-amphibische | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Erste Schritte für css | MDN"  

> [!NOTE]
> <span data-ttu-id="bb86d-388">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb86d-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bb86d-389">Die ursprüngliche Seite wurde [hier gefunden](https://developers.google.com/web/tools/chrome-devtools/beginners/css) und von [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="bb86d-389">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="bb86d-391">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bb86d-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
