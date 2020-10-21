---
description: Erste Schritte mit HTML und dem Dom
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem Dom'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f17b68845ef746fa2612cdf4d02cc7e1003baabb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125300"
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

# <span data-ttu-id="d8d29-104">DevTools für Anfänger: Erste Schritte mit HTML und dem Dom</span><span class="sxs-lookup"><span data-stu-id="d8d29-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="d8d29-105">Dies ist das erste in einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung beibringen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="d8d29-106">Darüber hinaus erhalten Sie Informationen zu einer Reihe von Webentwickler Tools namens Microsoft Edge devtools, die Ihre Produktivität steigern können.</span><span class="sxs-lookup"><span data-stu-id="d8d29-106">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="d8d29-107">In diesem speziellen Lernprogramm erfahren Sie mehr über HTML und das DOM.</span><span class="sxs-lookup"><span data-stu-id="d8d29-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="d8d29-108">HTML ist eine der Kerntechnologien der Web-Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="d8d29-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="d8d29-109">Diese Sprache steuert die Struktur und den Inhalt von Webseiten.</span><span class="sxs-lookup"><span data-stu-id="d8d29-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="d8d29-110">Das Dom ist auch mit der Struktur und dem Inhalt von Webseiten verknüpft, aber Sie werden später mehr darüber erfahren.</span><span class="sxs-lookup"><span data-stu-id="d8d29-110">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="d8d29-111">Ziele</span><span class="sxs-lookup"><span data-stu-id="d8d29-111">Goals</span></span>  

<span data-ttu-id="d8d29-112">Sie werden Web-Entwicklung lernen, indem Sie Ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="d8d29-113">Wenn Sie alle Lernprogramme in der *devtools für Anfänger* -Serie abgeschlossen haben, sieht die fertige Website wie in der folgenden Abbildung aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-113">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="d8d29-115">Die fertige Website</span><span class="sxs-lookup"><span data-stu-id="d8d29-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="d8d29-116">Am Ende dieses Lernprogramms können Sie Folgendes verstehen:</span><span class="sxs-lookup"><span data-stu-id="d8d29-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="d8d29-117">So erstellen HTML und Dom die Inhalte, die auf Webseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8d29-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="d8d29-118">So können Sie mithilfe von Microsoft Edge devtools mit HTML-und Dom-Änderungen experimentieren.</span><span class="sxs-lookup"><span data-stu-id="d8d29-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="d8d29-119">Der Unterschied zwischen HTML und dem Dom.</span><span class="sxs-lookup"><span data-stu-id="d8d29-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="d8d29-120">Sie haben auch eine echte Website!</span><span class="sxs-lookup"><span data-stu-id="d8d29-120">You'll also have a real website!</span></span>  <span data-ttu-id="d8d29-121">Mit dieser Website können Sie Ihren Lebenslauf oder Ihren Blog hosten.</span><span class="sxs-lookup"><span data-stu-id="d8d29-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="d8d29-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d8d29-122">Prerequisites</span></span>  

<span data-ttu-id="d8d29-123">Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus:</span><span class="sxs-lookup"><span data-stu-id="d8d29-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="d8d29-124">Wenn Sie mit HTML nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="d8d29-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="d8d29-125">Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.</span><span class="sxs-lookup"><span data-stu-id="d8d29-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="d8d29-126">In diesem Lernprogramm wird eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, verwendet, die in Microsoft Edge integriert sind.</span><span class="sxs-lookup"><span data-stu-id="d8d29-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="d8d29-127">Einrichten Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="d8d29-127">Set up your code</span></span>  

<span data-ttu-id="d8d29-128">Sie werden Ihre Website in einem Online Code-Editor mit dem Namen glitch erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="d8d29-129">Öffnen Sie den [Quellcode][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="d8d29-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="d8d29-130">Diese Registerkarte wird in diesem Lernprogramm als **Registerkarte "Editor** " bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="d8d29-132">Die Registerkarte "Editor"</span><span class="sxs-lookup"><span data-stu-id="d8d29-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-133">Wählen Sie **verführerisch – Schock**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="d8d29-134">Das Menü Projektoptionen wird in der oberen linken Ecke geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="d8d29-136">Das Menü "Projektoptionen"</span><span class="sxs-lookup"><span data-stu-id="d8d29-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-137">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="d8d29-138">Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-138">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="d8d29-139">Der Inhalt ist derselbe wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="d8d29-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="d8d29-141">Das Remix-Projekt</span><span class="sxs-lookup"><span data-stu-id="d8d29-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-142">Wenn Sie beabsichtigen, das nächste Lernprogramm in dieser Serie abzuschließen, wählen Sie **Anmelden** und bei glitch mit Ihrem GitHub-oder Facebook-Konto anmelden aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="d8d29-143">Wenn Sie sich nicht anmelden, verlieren Sie die Möglichkeit, dieses Projekt zu bearbeiten, wenn Sie die Registerkarte "Bearbeiten" schließen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-143">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="d8d29-144">Wählen Sie **anzeigen** aus, und wählen Sie **in einem neuen Fenster**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="d8d29-145">Daraufhin wird eine neue Registerkarte geöffnet, auf der Sie die Live Seite anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="d8d29-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="d8d29-146">Diese Registerkarte wird in diesem Lernprogramm als **"Live"-Registerkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-146">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="d8d29-148">Die Registerkarte "Live"</span><span class="sxs-lookup"><span data-stu-id="d8d29-148">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d8d29-149">Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="d8d29-149">Add content</span></span>  

<span data-ttu-id="d8d29-150">Ihre Website ist ziemlich leer.</span><span class="sxs-lookup"><span data-stu-id="d8d29-150">Your site is pretty empty.</span></span>  <span data-ttu-id="d8d29-151">Führen Sie die folgenden Schritte aus, um Inhalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-151">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="d8d29-152">Ersetzen Sie auf der **Registerkarte Editor** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="d8d29-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="d8d29-154">Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="d8d29-155">Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  Der Text `About Me` wird auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="d8d29-156">Sie ist größer als der restliche Text, da das `<h1>` Element eine Abschnittsüberschrift darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-156">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="d8d29-157">Ihr Webbrowserformat Vorlagen für Überschriften in größeren Schriftgraden automatisch.</span><span class="sxs-lookup"><span data-stu-id="d8d29-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="d8d29-159">Die neue Überschrift wird auf der Registerkarte "Live" angezeigt</span><span class="sxs-lookup"><span data-stu-id="d8d29-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-160">Klicken Sie auf der **Registerkarte Editor** `<p>I am learning HTML.  Recent accomplishments:</p>` auf die Zeile, die Sie gerade eingefügt haben `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="d8d29-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="d8d29-162">Der aktualisierte Code ist auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="d8d29-163">Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.</span><span class="sxs-lookup"><span data-stu-id="d8d29-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="d8d29-164">Zurück auf der **Registerkarte "Editor"** fügen Sie eine Liste ihrer Leistungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="d8d29-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="d8d29-166">Der aktualisierte Code wird auch auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="d8d29-167">Wiederkehren Sie zur **Registerkarte Live** zurück, um sicherzustellen, dass der neue Inhalt richtig angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8d29-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="d8d29-169">Die neue Liste wird auf der Registerkarte "Live" angezeigt</span><span class="sxs-lookup"><span data-stu-id="d8d29-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d8d29-170">Experimentieren mit Inhaltsänderungen in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="d8d29-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d8d29-171">Wenn Sie eine große Seite mit viel HTML entwickelt haben, können Sie sich vorstellen, dass es möglicherweise etwas mühsam ist, zwischen der Registerkarte "Editor" und der Registerkarte "Live" hunderte Male hin-und herzugehen, um Ihre Änderungen zu sehen, insbesondere dann, wenn Sie nicht genau wissen, was auf der Seite eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8d29-171">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="d8d29-172">Microsoft Edge devtools kann Ihnen beim Experimentieren mit Inhaltsänderungen helfen, ohne die Live-Registerkarte verlassen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-172">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="d8d29-173">Lernen Sie den Unterschied zwischen HTML und dem Dom kennen</span><span class="sxs-lookup"><span data-stu-id="d8d29-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="d8d29-174">Bevor Sie mit der Bearbeitung Ihrer Inhalte von Microsoft Edge devtools beginnen, ist es hilfreich, den Unterschied zwischen HTML und dem Dom zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-174">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="d8d29-175">Am besten lernen Sie mit einem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d8d29-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="d8d29-176">Wechseln Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der Text angezeigt `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="d8d29-176">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="d8d29-179">Am unteren Rand der Seite wird der Text ein neues Element!?!</span><span class="sxs-lookup"><span data-stu-id="d8d29-179">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="d8d29-180">kann angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="d8d29-180">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-181">Wechseln Sie zurück zur **Registerkarte Editor** , und versuchen Sie, diesen Text zu finden `index.html` .</span><span class="sxs-lookup"><span data-stu-id="d8d29-181">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="d8d29-182">Es ist nicht da!</span><span class="sxs-lookup"><span data-stu-id="d8d29-182">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="d8d29-185">Der mysteriöse Text `A new element!?!` ist nirgendwo zu finden</span><span class="sxs-lookup"><span data-stu-id="d8d29-185">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-186">Wechseln Sie zurück zur **Registerkarte Live**, klicken Sie mit der rechten Maustaste `A new element!?!` , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-186">Go back to the **live tab**, right-click `A new element!?!`, and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="d8d29-188">Überprüfen von Text</span><span class="sxs-lookup"><span data-stu-id="d8d29-188">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="d8d29-189">DevTools wird neben ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-189">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="d8d29-190">ist blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-190">is highlighted blue.</span></span>  <span data-ttu-id="d8d29-191">Obwohl diese Struktur in devtools wie Ihr HTML-Code aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="d8d29-191">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="d8d29-193">DevTools ist neben der Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-193">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d8d29-194">Wenn Ihre Seite geladen wird, verwendet der Browser Ihren HTML-Code, um den *anfänglichen* Inhalt der Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-194">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="d8d29-195">Das Dom steht für den *aktuellen* Inhalt der Seite, der sich im Laufe der Zeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="d8d29-195">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="d8d29-196">Der mysteriöse `<div>A new element!?!</div>` Inhalt wird Ihrer Seite hinzugefügt, weil das `<script src="new.js"></script>` Tag am unteren Rand des HTML-Tags liegt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-196">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="d8d29-197">Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8d29-197">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="d8d29-198">Sie werden in einem späteren Lernprogramm mehr über JavaScript erfahren, aber betrachten Sie es jetzt als Programmiersprache, mit der der Inhalt Ihrer Seite geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8d29-198">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="d8d29-199">In diesem speziellen Fall fügt JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="d8d29-199">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="d8d29-200">Deshalb ist dieser mysteriöse Text auf Ihrer Live-Seite sichtbar, aber nicht in Ihrem HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="d8d29-200">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="d8d29-201">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="d8d29-201">Edit the DOM</span></span>  

<span data-ttu-id="d8d29-202">Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Registerkarte "Live" zu verlassen, probieren Sie devtools aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-202">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="d8d29-203">Klicken Sie in devtools mit der rechten Maustaste, `Your site!` und wählen Sie **als HTML bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="d8d29-203">In DevTools, right-click `Your site!` and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="d8d29-205">Bearbeiten des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="d8d29-205">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-206">Ersetzen Sie dies `<p>Your site!</p>` durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="d8d29-206">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="d8d29-208">Aktualisieren des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="d8d29-208">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="d8d29-209">Wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus, um Ihre Änderungen zu speichern, oder klicken Sie auf eine Stelle außerhalb des Felds.</span><span class="sxs-lookup"><span data-stu-id="d8d29-209">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="d8d29-210">Ihre Änderungen werden automatisch in der Live Ansicht Ihrer Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-210">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="d8d29-211">Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-211">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="d8d29-213">Der neue Inhalt wird sofort auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-213">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d8d29-214">Dieser Workflow eignet sich gut zum Experimentieren mit Inhaltsänderungen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-214">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="d8d29-215">Wenn Sie die Seite neu laden oder die Registerkarte schließen, sind Ihre Änderungen für immer verschwunden.</span><span class="sxs-lookup"><span data-stu-id="d8d29-215">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="d8d29-216">Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihr HTML-Code kopieren.</span><span class="sxs-lookup"><span data-stu-id="d8d29-216">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="d8d29-217">In den nächsten Abschnitten werden weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-217">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="d8d29-218">Neuanordnen von Knoten</span><span class="sxs-lookup"><span data-stu-id="d8d29-218">Reorder nodes</span></span>  

<span data-ttu-id="d8d29-219">Sie können auch die Reihenfolge der DOM-Knoten ändern.</span><span class="sxs-lookup"><span data-stu-id="d8d29-219">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="d8d29-220">Auf Ihrer Webseite befindet sich beispielsweise das Navigationsmenü in der Nähe des unteren Rands.</span><span class="sxs-lookup"><span data-stu-id="d8d29-220">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="d8d29-221">So verschieben Sie Sie an den Anfang:</span><span class="sxs-lookup"><span data-stu-id="d8d29-221">To move it to the top:</span></span>  

1.  <span data-ttu-id="d8d29-222">Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von devtools.</span><span class="sxs-lookup"><span data-stu-id="d8d29-222">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="d8d29-224">Der Navigationsknoten ist in devtools blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-224">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-225">Ziehen Sie den `<nav>` Knoten an den Anfang, sodass er das erste untergeordnete Element unterhalb des `<body>` Knotens ist.</span><span class="sxs-lookup"><span data-stu-id="d8d29-225">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="d8d29-227">Ziehen des Navigationsknotens nach oben</span><span class="sxs-lookup"><span data-stu-id="d8d29-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="d8d29-228">Der `<nav>` Knoten wird jetzt oben auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-228">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="d8d29-230">Der Navigationsknoten befindet sich am oberen Rand der Seite.</span><span class="sxs-lookup"><span data-stu-id="d8d29-230">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="d8d29-231">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="d8d29-231">Delete a node</span></span>  

<span data-ttu-id="d8d29-232">Sie können auch Knoten aus der DOM-Struktur entfernen.</span><span class="sxs-lookup"><span data-stu-id="d8d29-232">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="d8d29-233">Klicken Sie in der **DOM-Struktur**auf `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="d8d29-233">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="d8d29-234">DevTools hebt den Knoten Blau hervor.</span><span class="sxs-lookup"><span data-stu-id="d8d29-234">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="d8d29-236">Auswählen des zu löschenden Knotens</span><span class="sxs-lookup"><span data-stu-id="d8d29-236">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-237">Drücken Sie die `Delete` Taste auf der Tastatur.</span><span class="sxs-lookup"><span data-stu-id="d8d29-237">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="d8d29-238">Der `<div>A new element!?!</div>` Knoten wird aus ihrer DOM-Struktur entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-238">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="d8d29-240">Der Knoten wurde gelöscht</span><span class="sxs-lookup"><span data-stu-id="d8d29-240">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d8d29-241">Kopieren der Änderungen</span><span class="sxs-lookup"><span data-stu-id="d8d29-241">Copy your changes</span></span>  

<span data-ttu-id="d8d29-242">Sie haben es fast geschafft.</span><span class="sxs-lookup"><span data-stu-id="d8d29-242">You're almost done.</span></span>  <span data-ttu-id="d8d29-243">Sie haben in devtools einige Änderungen an Ihrer Seite vorgenommen, die aber noch nicht in Ihrem Quellcode gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d8d29-243">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="d8d29-244">Aktualisieren Sie Ihren **Live-Reiter**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d8d29-244">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="d8d29-245">Insbesondere kehrt der Text `Your site!` zum Anfang der Seite zurück, und der Text `A new element!?!` kehrt nach unten zurück.</span><span class="sxs-lookup"><span data-stu-id="d8d29-245">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="d8d29-247">Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden</span><span class="sxs-lookup"><span data-stu-id="d8d29-247">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8d29-248">Kopieren Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="d8d29-248">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="d8d29-249">Wechseln Sie zurück zur **Registerkarte Editor** , und ersetzen Sie den Inhalt Ihrer `index.html` Datei durch den Code, den Sie soeben kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="d8d29-249">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="d8d29-251">Aussehen der `index.html` Datei</span><span class="sxs-lookup"><span data-stu-id="d8d29-251">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d8d29-252">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d8d29-252">Next steps</span></span>  

*   <span data-ttu-id="d8d29-253">Führen Sie das nächste Lernprogramm in dieser Serie, [Erste Schritte mit CSS][DevToolsBeginnersCss], aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Stiländerungen in Microsoft Edge devtools experimentieren.</span><span class="sxs-lookup"><span data-stu-id="d8d29-253">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="d8d29-254">Lesen Sie [Einführung in das DOM][MDNIntroductionDom] , um mehr über das DOM zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d8d29-254">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="d8d29-255">Schauen Sie sich einen Kurs wie [Einführung in die Webentwicklung][CourseraIntroductionToWebDevelopment] an, um mehr praktische Erfahrungen mit der Webentwicklung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8d29-255">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <span data-ttu-id="d8d29-256">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d8d29-256">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in die Web-Entwicklung | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-verführerisch-Schock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="d8d29-263">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8d29-263">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d8d29-264">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8d29-264">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d8d29-266">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8d29-266">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
