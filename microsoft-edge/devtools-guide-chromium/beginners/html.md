---
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem Dom'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: d992a6ca68de07c879ca8e319ee6c22782924a6b
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882730"
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

# <span data-ttu-id="33088-103">DevTools für Anfänger: Erste Schritte mit HTML und dem Dom</span><span class="sxs-lookup"><span data-stu-id="33088-103">DevTools for beginners: Get started with HTML and the DOM</span></span>   

<span data-ttu-id="33088-104">Dies ist das erste in einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung beibringen.</span><span class="sxs-lookup"><span data-stu-id="33088-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="33088-105">Darüber hinaus erhalten Sie Informationen zu einer Reihe von Webentwickler Tools namens Microsoft Edge devtools, die Ihre Produktivität steigern können.</span><span class="sxs-lookup"><span data-stu-id="33088-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="33088-106">In diesem speziellen Lernprogramm erfahren Sie mehr über HTML und das DOM.</span><span class="sxs-lookup"><span data-stu-id="33088-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="33088-107">HTML ist eine der Kerntechnologien der Web-Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="33088-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="33088-108">Diese Sprache steuert die Struktur und den Inhalt von Webseiten.</span><span class="sxs-lookup"><span data-stu-id="33088-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="33088-109">Das Dom ist auch mit der Struktur und dem Inhalt von Webseiten verknüpft, aber Sie werden später mehr darüber erfahren.</span><span class="sxs-lookup"><span data-stu-id="33088-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="33088-110">Ziele</span><span class="sxs-lookup"><span data-stu-id="33088-110">Goals</span></span>   

<span data-ttu-id="33088-111">Sie werden Web-Entwicklung lernen, indem Sie Ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="33088-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="33088-112">Wenn Sie alle Lernprogramme in der *devtools für Anfänger* -Serie abgeschlossen haben, sieht Ihre fertige Website wie in **Abbildung 1**aus.</span><span class="sxs-lookup"><span data-stu-id="33088-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like **Figure 1**.</span></span>  

> ##### <span data-ttu-id="33088-113">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="33088-113">Figure 1</span></span>  
> <span data-ttu-id="33088-114">Die fertige Website</span><span class="sxs-lookup"><span data-stu-id="33088-114">The finished site</span></span>  
> ![Die fertige Website][ImageHtmlFinished]  

<span data-ttu-id="33088-116">Am Ende dieses Lernprogramms können Sie Folgendes verstehen:</span><span class="sxs-lookup"><span data-stu-id="33088-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="33088-117">So erstellen HTML und Dom die Inhalte, die auf Webseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33088-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="33088-118">So können Sie mithilfe von Microsoft Edge devtools mit HTML-und Dom-Änderungen experimentieren.</span><span class="sxs-lookup"><span data-stu-id="33088-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="33088-119">Der Unterschied zwischen HTML und dem Dom.</span><span class="sxs-lookup"><span data-stu-id="33088-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="33088-120">Sie haben auch eine echte Website!</span><span class="sxs-lookup"><span data-stu-id="33088-120">You'll also have a real website!</span></span>  <span data-ttu-id="33088-121">Mit dieser Website können Sie Ihren Lebenslauf oder Ihren Blog hosten.</span><span class="sxs-lookup"><span data-stu-id="33088-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="33088-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="33088-122">Prerequisites</span></span>   

<span data-ttu-id="33088-123">Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus:</span><span class="sxs-lookup"><span data-stu-id="33088-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="33088-124">Wenn Sie mit HTML nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="33088-124">If you're unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="33088-125">Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.</span><span class="sxs-lookup"><span data-stu-id="33088-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="33088-126">In diesem Lernprogramm wird eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, verwendet, die in Microsoft Edge integriert sind.</span><span class="sxs-lookup"><span data-stu-id="33088-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="33088-127">Einrichten Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="33088-127">Set up your code</span></span>   

<span data-ttu-id="33088-128">Sie werden Ihre Website in einem Online Code-Editor mit dem Namen glitch erstellen.</span><span class="sxs-lookup"><span data-stu-id="33088-128">You're going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="33088-129">Öffnen Sie den [Quellcode][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="33088-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="33088-130">Diese Registerkarte wird in diesem Lernprogramm als **Registerkarte "Editor** " bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="33088-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    > ##### <span data-ttu-id="33088-131">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="33088-131">Figure 2</span></span>  
    > <span data-ttu-id="33088-132">Die Registerkarte "Editor"</span><span class="sxs-lookup"><span data-stu-id="33088-132">The editor tab</span></span>  
    > ![Die Registerkarte "Editor"][ImageHtmlSetup1]  

1.  <span data-ttu-id="33088-134">Klicken Sie auf **verführerisch – Schock**.</span><span class="sxs-lookup"><span data-stu-id="33088-134">Click **alluring-shock**.</span></span>  <span data-ttu-id="33088-135">Das Menü Projektoptionen wird in der oberen linken Ecke geöffnet.</span><span class="sxs-lookup"><span data-stu-id="33088-135">The Project Options menu opens in the top-left corner.</span></span>  
    
    > #### <span data-ttu-id="33088-136">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="33088-136">Figure 3</span></span>  
    > <span data-ttu-id="33088-137">Das Menü "Projektoptionen"</span><span class="sxs-lookup"><span data-stu-id="33088-137">The Project Options menu</span></span>  
    > ![Das Menü "Projektoptionen"][ImageHtmlSetup2]  
    
1.  <span data-ttu-id="33088-139">Klicken Sie auf **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="33088-139">Click **Remix Project**.</span></span>  <span data-ttu-id="33088-140">Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="33088-140">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="33088-141">Der Inhalt ist derselbe wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="33088-141">The content is the same as before.</span></span>  
    
    > ##### <span data-ttu-id="33088-142">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="33088-142">Figure 4</span></span>  
    > <span data-ttu-id="33088-143">Das Remix-Projekt</span><span class="sxs-lookup"><span data-stu-id="33088-143">The remixed project</span></span>  
    > ![Das Remix-Projekt][ImageHtmlSetup3]  
    
1.  <span data-ttu-id="33088-145">Wenn Sie beabsichtigen, das nächste Lernprogramm in dieser Serie abzuschließen, klicken Sie auf **Anmelden** , und registrieren Sie sich bei glitch mit Ihrem GitHub-oder Facebook-Konto.</span><span class="sxs-lookup"><span data-stu-id="33088-145">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="33088-146">Wenn Sie sich nicht anmelden, verlieren Sie die Möglichkeit, dieses Projekt zu bearbeiten, wenn Sie die Registerkarte "Bearbeiten" schließen.</span><span class="sxs-lookup"><span data-stu-id="33088-146">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="33088-147">Klicken Sie auf **anzeigen** , und wählen Sie **in einem neuen Fenster**aus.</span><span class="sxs-lookup"><span data-stu-id="33088-147">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="33088-148">Daraufhin wird eine neue Registerkarte geöffnet, auf der Sie die Live Seite anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="33088-148">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="33088-149">Diese Registerkarte wird in diesem Lernprogramm als **"Live"-Registerkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="33088-149">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="33088-150">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="33088-150">Figure 5</span></span>  
    > <span data-ttu-id="33088-151">Die Registerkarte "Live"</span><span class="sxs-lookup"><span data-stu-id="33088-151">The live tab</span></span>  
    > ![Die Registerkarte "Live"][ImageHtmlSetup4]  
    
## <span data-ttu-id="33088-153">Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="33088-153">Add content</span></span>   

<span data-ttu-id="33088-154">Ihre Website ist ziemlich leer.</span><span class="sxs-lookup"><span data-stu-id="33088-154">Your site is pretty empty.</span></span>  <span data-ttu-id="33088-155">Führen Sie die folgenden Schritte aus, um Inhalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="33088-155">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="33088-156">Ersetzen Sie auf der **Registerkarte Editor** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="33088-156">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="33088-157">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="33088-157">Figure 6</span></span>  
    > <span data-ttu-id="33088-158">Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="33088-158">The new code is highlighted in the editor tab</span></span>  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd1]  
    
1.  <span data-ttu-id="33088-160">Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  Der Text `About Me` wird auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33088-160">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="33088-161">Sie ist größer als der restliche Text, da das `<h1>` Element eine Abschnittsüberschrift darstellt.</span><span class="sxs-lookup"><span data-stu-id="33088-161">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="33088-162">Ihr Webbrowserformat Vorlagen für Überschriften in größeren Schriftgraden automatisch.</span><span class="sxs-lookup"><span data-stu-id="33088-162">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    > ##### <span data-ttu-id="33088-163">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="33088-163">Figure 7</span></span>  
    > <span data-ttu-id="33088-164">Die neue Überschrift wird auf der Registerkarte "Live" angezeigt</span><span class="sxs-lookup"><span data-stu-id="33088-164">The new heading is visible in the live tab</span></span>  
    > ![Die neue Überschrift wird auf der Registerkarte "Live" angezeigt][ImageHtmlAdd2]  
    
1.  <span data-ttu-id="33088-166">Klicken Sie auf der **Registerkarte Editor** `<p>I am learning HTML.  Recent accomplishments:</p>` auf die Zeile, die Sie gerade eingefügt haben `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="33088-166">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### <span data-ttu-id="33088-167">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="33088-167">Figure 8</span></span>  
    > <span data-ttu-id="33088-168">Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="33088-168">The new code is highlighted in the editor tab</span></span>  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd3]  
    
1.  <span data-ttu-id="33088-170">Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.</span><span class="sxs-lookup"><span data-stu-id="33088-170">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="33088-171">Zurück auf der **Registerkarte "Editor"** fügen Sie eine Liste ihrer Leistungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="33088-171">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="33088-172">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="33088-172">Figure 9</span></span>  
    > <span data-ttu-id="33088-173">Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="33088-173">The new code is highlighted in the editor tab</span></span>  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd4]  
    
1.  <span data-ttu-id="33088-175">Wiederkehren Sie zur **Registerkarte Live** zurück, um sicherzustellen, dass der neue Inhalt richtig angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="33088-175">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    > ##### <span data-ttu-id="33088-176">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="33088-176">Figure 10</span></span>  
    > <span data-ttu-id="33088-177">Die neue Liste wird auf der Registerkarte "Live" angezeigt</span><span class="sxs-lookup"><span data-stu-id="33088-177">The new list is visible in the live tab</span></span>  
    > ![Die neue Liste wird auf der Registerkarte "Live" angezeigt][ImageHtmlAdd5]  
    
## <span data-ttu-id="33088-179">Experimentieren mit Inhaltsänderungen in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="33088-179">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="33088-180">Wenn Sie eine große Seite mit viel HTML entwickelt haben, können Sie sich vorstellen, dass es möglicherweise etwas mühsam ist, zwischen der Registerkarte "Editor" und der Registerkarte "Live" hunderte Male hin-und herzugehen, um Ihre Änderungen zu sehen, insbesondere dann, wenn Sie nicht genau wissen, was auf der Seite eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="33088-180">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="33088-181">Microsoft Edge devtools kann Ihnen beim Experimentieren mit Inhaltsänderungen helfen, ohne die Live-Registerkarte verlassen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="33088-181">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="33088-182">Lernen Sie den Unterschied zwischen HTML und dem Dom kennen</span><span class="sxs-lookup"><span data-stu-id="33088-182">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="33088-183">Bevor Sie mit der Bearbeitung Ihrer Inhalte von Microsoft Edge devtools beginnen, ist es hilfreich, den Unterschied zwischen HTML und dem Dom zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="33088-183">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="33088-184">Am besten lernen Sie mit einem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="33088-184">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="33088-185">Wechseln Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der Text angezeigt `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="33088-185">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    > ###### <span data-ttu-id="33088-186">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="33088-186">Figure 11</span></span>  
    > <span data-ttu-id="33088-187">Unten auf der Seite kann der Text `A new element!?!` angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="33088-187">At the bottom of the page the text `A new element!?!` can be seen</span></span>  
    > ![Am unteren Rand der Seite wird der Text ein neues Element!?!][ImageHtmlDom1]  
    
1.  <span data-ttu-id="33088-190">Wechseln Sie zurück zur **Registerkarte Editor** , und versuchen Sie, diesen Text zu finden `index.html` .</span><span class="sxs-lookup"><span data-stu-id="33088-190">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="33088-191">Es ist nicht da!</span><span class="sxs-lookup"><span data-stu-id="33088-191">It's not there!</span></span>  
    
    > ##### <span data-ttu-id="33088-192">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="33088-192">Figure 12</span></span>  
    > <span data-ttu-id="33088-193">Der mysteriöse Text `A new element!?!` ist nirgendwo zu finden</span><span class="sxs-lookup"><span data-stu-id="33088-193">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    > ![Der mysteriöse Text ein neues Element!?!][ImageHtmlDom2]  
    
1.  <span data-ttu-id="33088-196">Wechseln Sie zurück zur **Registerkarte Live**, klicken Sie mit der rechten Maustaste `A new element!?!` , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="33088-196">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="33088-197">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="33088-197">Figure 13</span></span>  
    > <span data-ttu-id="33088-198">Überprüfen von Text</span><span class="sxs-lookup"><span data-stu-id="33088-198">Inspecting some text</span></span>  
    > ![Überprüfen von Text][ImageHtmlDom3]  
    
    <span data-ttu-id="33088-200">DevTools wird neben ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="33088-200">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="33088-201">ist blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="33088-201">is highlighted blue.</span></span>  <span data-ttu-id="33088-202">Obwohl diese Struktur in devtools wie Ihr HTML-Code aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="33088-202">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    > ##### <span data-ttu-id="33088-203">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="33088-203">Figure 14</span></span>  
    > <span data-ttu-id="33088-204">DevTools ist neben der Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="33088-204">DevTools is open alongside the page</span></span>  
    > ![DevTools ist neben der Seite geöffnet.][ImageHtmlDom4]  
    
<span data-ttu-id="33088-206">Wenn Ihre Seite geladen wird, verwendet der Browser Ihren HTML-Code, um den *anfänglichen* Inhalt der Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33088-206">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="33088-207">Das Dom steht für den *aktuellen* Inhalt der Seite, der sich im Laufe der Zeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="33088-207">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="33088-208">Der mysteriöse `<div>A new element!?!</div>` Inhalt wird Ihrer Seite hinzugefügt, weil das `<script src="new.js"></script>` Tag am unteren Rand des HTML-Tags liegt.</span><span class="sxs-lookup"><span data-stu-id="33088-208">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="33088-209">Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33088-209">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="33088-210">Sie werden in einem späteren Lernprogramm mehr über JavaScript erfahren, aber betrachten Sie es jetzt als Programmiersprache, mit der der Inhalt Ihrer Seite geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="33088-210">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="33088-211">In diesem speziellen Fall fügt JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="33088-211">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="33088-212">Deshalb ist dieser mysteriöse Text auf Ihrer Live-Seite sichtbar, aber nicht in Ihrem HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="33088-212">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="33088-213">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="33088-213">Edit the DOM</span></span>   

<span data-ttu-id="33088-214">Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Registerkarte "Live" zu verlassen, probieren Sie devtools aus.</span><span class="sxs-lookup"><span data-stu-id="33088-214">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="33088-215">Klicken Sie in devtools mit der rechten Maustaste, `Your site!` und wählen Sie **als HTML bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="33088-215">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  

    > ##### <span data-ttu-id="33088-216">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="33088-216">Figure 15</span></span>  
    > <span data-ttu-id="33088-217">Bearbeiten des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="33088-217">Editing the node as HTML</span></span>  
    > ![Bearbeiten des Knotens als HTML][ImageHtmlEdit1]  
    
1.  <span data-ttu-id="33088-219">Ersetzen Sie dies `<p>Your site!</p>` durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="33088-219">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="33088-220">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="33088-220">Figure 16</span></span>  
    > <span data-ttu-id="33088-221">Bearbeiten des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="33088-221">Editing the node as HTML</span></span>  
    > ![Bearbeiten des Knotens als HTML][ImageHtmlEdit2]  
    
1.  <span data-ttu-id="33088-223">Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderungen zu speichern, oder klicken Sie auf eine Stelle außerhalb des Felds.</span><span class="sxs-lookup"><span data-stu-id="33088-223">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="33088-224">Ihre Änderungen werden automatisch in der Live Ansicht Ihrer Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33088-224">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="33088-225">Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33088-225">The text `Your site!` has been replaced with the new content.</span></span>  
    
    > ##### <span data-ttu-id="33088-226">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="33088-226">Figure 17</span></span>  
    > <span data-ttu-id="33088-227">Der neue Inhalt wird sofort auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33088-227">The new content shows up immediately on the page</span></span>  
    > ![Der neue Inhalt wird sofort auf der Seite angezeigt.][ImageHtmlEdit3]  
    
<span data-ttu-id="33088-229">Dieser Workflow eignet sich gut zum Experimentieren mit Inhaltsänderungen.</span><span class="sxs-lookup"><span data-stu-id="33088-229">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="33088-230">Wenn Sie die Seite neu laden oder die Registerkarte schließen, sind Ihre Änderungen für immer verschwunden.</span><span class="sxs-lookup"><span data-stu-id="33088-230">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="33088-231">Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihr HTML-Code kopieren.</span><span class="sxs-lookup"><span data-stu-id="33088-231">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="33088-232">In den nächsten Abschnitten werden weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33088-232">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="33088-233">Neuanordnen von Knoten</span><span class="sxs-lookup"><span data-stu-id="33088-233">Reorder nodes</span></span>   

<span data-ttu-id="33088-234">Sie können auch die Reihenfolge der DOM-Knoten ändern.</span><span class="sxs-lookup"><span data-stu-id="33088-234">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="33088-235">Auf Ihrer Webseite befindet sich beispielsweise das Navigationsmenü in der Nähe des unteren Rands.</span><span class="sxs-lookup"><span data-stu-id="33088-235">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="33088-236">So verschieben Sie Sie an den Anfang:</span><span class="sxs-lookup"><span data-stu-id="33088-236">To move it to the top:</span></span>  

1.  <span data-ttu-id="33088-237">Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von devtools.</span><span class="sxs-lookup"><span data-stu-id="33088-237">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="33088-238">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="33088-238">Figure 18</span></span>  
    > <span data-ttu-id="33088-239">Der Navigationsknoten ist in devtools blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="33088-239">The nav node is highlighted blue in DevTools</span></span>  
    > ![Der Navigationsknoten ist in devtools blau hervorgehoben.][ImageHtmlReorder1]  
    
1.  <span data-ttu-id="33088-241">Ziehen Sie den `<nav>` Knoten an den Anfang, sodass er das erste untergeordnete Element unterhalb des `<body>` Knotens ist.</span><span class="sxs-lookup"><span data-stu-id="33088-241">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    > ##### <span data-ttu-id="33088-242">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="33088-242">Figure 19</span></span>  
    > <span data-ttu-id="33088-243">Ziehen des Navigationsknotens nach oben</span><span class="sxs-lookup"><span data-stu-id="33088-243">Dragging the nav node to the top</span></span>  
    > ![Ziehen des Navigationsknotens nach oben][ImageHtmlReorder2]  
    
    <span data-ttu-id="33088-245">Der `<nav>` Knoten wird jetzt oben auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33088-245">The `<nav>` node is now displaying at the top of your page.</span></span>  
    
    > ##### <span data-ttu-id="33088-246">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="33088-246">Figure 20</span></span>  
    > <span data-ttu-id="33088-247">Der Navigationsknoten befindet sich am oberen Rand der Seite.</span><span class="sxs-lookup"><span data-stu-id="33088-247">The nav node is at the top of the page</span></span>  
    > ![Der Navigationsknoten befindet sich am oberen Rand der Seite.][ImageHtmlReorder3]  
    
### <span data-ttu-id="33088-249">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="33088-249">Delete a node</span></span>   

<span data-ttu-id="33088-250">Sie können auch Knoten aus der DOM-Struktur entfernen.</span><span class="sxs-lookup"><span data-stu-id="33088-250">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="33088-251">Klicken Sie in der **DOM-Struktur**auf `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="33088-251">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="33088-252">DevTools hebt den Knoten Blau hervor.</span><span class="sxs-lookup"><span data-stu-id="33088-252">DevTools highlights the node blue.</span></span>  
    
    > ##### <span data-ttu-id="33088-253">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="33088-253">Figure 21</span></span>  
    > <span data-ttu-id="33088-254">Auswählen des zu löschenden Knotens</span><span class="sxs-lookup"><span data-stu-id="33088-254">Selecting the node to be deleted</span></span>  
    > ![Auswählen des zu löschenden Knotens][ImageHtmlDelete1]  
    
1.  <span data-ttu-id="33088-256">Drücken Sie die `Delete` Taste auf der Tastatur.</span><span class="sxs-lookup"><span data-stu-id="33088-256">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="33088-257">Der `<div>A new element!?!</div>` Knoten wird aus ihrer DOM-Struktur entfernt.</span><span class="sxs-lookup"><span data-stu-id="33088-257">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="33088-258">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="33088-258">Figure 22</span></span>  
    > <span data-ttu-id="33088-259">Der Knoten wurde gelöscht</span><span class="sxs-lookup"><span data-stu-id="33088-259">The node has been deleted</span></span>  
    > ![Der Knoten wurde gelöscht][ImageHtmlDelete2]  
    
## <span data-ttu-id="33088-261">Kopieren der Änderungen</span><span class="sxs-lookup"><span data-stu-id="33088-261">Copy your changes</span></span>   

<span data-ttu-id="33088-262">Sie haben es fast geschafft.</span><span class="sxs-lookup"><span data-stu-id="33088-262">You're almost done.</span></span>  <span data-ttu-id="33088-263">Sie haben in devtools einige Änderungen an Ihrer Seite vorgenommen, die aber noch nicht in Ihrem Quellcode gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="33088-263">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="33088-264">Aktualisieren Sie Ihren **Live-Reiter**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="33088-264">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="33088-265">Insbesondere kehrt der Text `Your site!` zum Anfang der Seite zurück, und der Text `A new element!?!` kehrt nach unten zurück.</span><span class="sxs-lookup"><span data-stu-id="33088-265">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    > ##### <span data-ttu-id="33088-266">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="33088-266">Figure 23</span></span>  
    > <span data-ttu-id="33088-267">Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden</span><span class="sxs-lookup"><span data-stu-id="33088-267">The changes that you've made are gone</span></span>  
    > ![Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden][ImageHtmlCopy1]  

1.  <span data-ttu-id="33088-269">Kopieren Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="33088-269">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  <span data-ttu-id="33088-270">Wechseln Sie zurück zur **Registerkarte Editor** , und ersetzen Sie den Inhalt Ihrer `index.html` Datei durch den Code, den Sie soeben kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="33088-270">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    > ##### <span data-ttu-id="33088-271">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="33088-271">Figure 24</span></span>  
    > <span data-ttu-id="33088-272">Aussehen der `index.html` Datei</span><span class="sxs-lookup"><span data-stu-id="33088-272">How your `index.html` file should look</span></span>  
    > ![So sollte Ihre index.html-Datei aussehen][ImageHtmlCopy2]  
    
## <span data-ttu-id="33088-274">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="33088-274">Next steps</span></span>   

*   <span data-ttu-id="33088-275">Führen Sie das nächste Lernprogramm in dieser Serie, [Erste Schritte mit CSS][DevToolsBeginnersCss], aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Stiländerungen in Microsoft Edge devtools experimentieren.</span><span class="sxs-lookup"><span data-stu-id="33088-275">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="33088-276">Lesen Sie [Einführung in das DOM][MDNIntroductionDom] , um mehr über das DOM zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="33088-276">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="33088-277">Schauen Sie sich einen Kurs wie [Einführung in die Webentwicklung][CourseraIntroductionToWebDevelopment] an, um mehr praktische Erfahrungen mit der Webentwicklung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="33088-277">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Abbildung 1: die fertige Website"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Abbildung 2: die Registerkarte "Editor""  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Abbildung 3: das Menü "Projektoptionen""  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Abbildung 4: das Remix-Projekt"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Abbildung 5: die Registerkarte "Live""  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Abbildung 6: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Abbildung 7: die neue Überschrift wird auf der Registerkarte "Live" angezeigt"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Abbildung 8: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Abbildung 9: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Abbildung 10: die neue Liste wird auf der Registerkarte "Live" angezeigt"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Abbildung 11: am unteren Rand der Seite der Text ein neues Element!?! kann angezeigt werden"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Abbildung 12: der mysteriöse Text ein neues Element!?! ist nirgendwo in index.html zu finden"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Abbildung 13: Überprüfen von Text"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Abbildung 14: devtools ist neben der Seite geöffnet"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Abbildung 15: Bearbeiten des Knotens als HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Abbildung 16: Bearbeiten des Knotens als HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Abbildung 17: der neue Inhalt wird sofort auf der Seite angezeigt."  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Abbildung 18: der Navigationsknoten ist in devtools blau hervorgehoben"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Abbildung 19: Ziehen des Navigationsknotens nach oben"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Abbildung 20: der Navigationsknoten befindet sich am oberen Rand der Seite."  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Abbildung 21: Auswählen des zu löschenden Knotens"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Abbildung 22: der Knoten wurde gelöscht"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Abbildung 23: die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Abbildung 24: Aussehen Ihrer index.html-Datei"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools für Anfänger: Erste Schritte mit CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in die Web-Entwicklung | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-verführerisch-Schock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="33088-308">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33088-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="33088-309">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="33088-309">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="33088-311">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="33088-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
