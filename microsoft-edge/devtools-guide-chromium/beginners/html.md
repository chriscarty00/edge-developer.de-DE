---
description: Erste Schritte mit HTML und dem DOM
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564567"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="84509-104">DevTools für Anfänger: Erste Schritte mit HTML und dem DOM</span><span class="sxs-lookup"><span data-stu-id="84509-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="84509-105">Dies ist das erste in einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung vermitteln.</span><span class="sxs-lookup"><span data-stu-id="84509-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="84509-106">Erfahren Sie mehr über eine Reihe von Webentwicklertools namens Microsoft Edge DevTools, die Ihre Produktivität erhöhen können.</span><span class="sxs-lookup"><span data-stu-id="84509-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="84509-107">In diesem bestimmten Lernprogramm erfahren Sie mehr über HTML und das DOM.</span><span class="sxs-lookup"><span data-stu-id="84509-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="84509-108">HTML ist eine der Kerntechnologien der Webentwicklung.</span><span class="sxs-lookup"><span data-stu-id="84509-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="84509-109">Es ist die Sprache, die die Struktur und den Inhalt von Webseiten steuert.</span><span class="sxs-lookup"><span data-stu-id="84509-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="84509-110">Das DOM steht auch im Zusammenhang mit der Struktur und dem Inhalt von Webseiten, erfahren Sie später mehr darüber.</span><span class="sxs-lookup"><span data-stu-id="84509-110">The DOM is also related to the structure and content of webpages, learn more about that later.</span></span>  

## <a name="goals"></a><span data-ttu-id="84509-111">Ziele</span><span class="sxs-lookup"><span data-stu-id="84509-111">Goals</span></span>  

<span data-ttu-id="84509-112">Sie lernen die Webentwicklung, indem Sie ihre eigene Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="84509-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="84509-113">Wenn Sie alle Lernprogramme in der **DevTools for Beginners-Reihe** abschließen, sieht Ihre fertige Website möglicherweise wie die folgende Abbildung aus.</span><span class="sxs-lookup"><span data-stu-id="84509-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="84509-115">Die fertige Website</span><span class="sxs-lookup"><span data-stu-id="84509-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="84509-116">Am Ende dieses Lernprogramms sollten Sie die folgenden Themen verstehen.</span><span class="sxs-lookup"><span data-stu-id="84509-116">By the end of this tutorial, you should understand the following topics.</span></span>  

*   <span data-ttu-id="84509-117">Wie HTML und das DOM die Inhalte erstellen, die auf Webseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="84509-117">How HTML and the DOM create the content that are displayed on webpages.</span></span>  
*   <span data-ttu-id="84509-118">Wie Microsoft Edge DevTools Ihnen beim Experimentieren mit HTML- und DOM-Änderungen helfen kann.</span><span class="sxs-lookup"><span data-stu-id="84509-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="84509-119">Der Unterschied zwischen HTML und dem DOM.</span><span class="sxs-lookup"><span data-stu-id="84509-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="84509-120">Sie haben auch eine echte Website.</span><span class="sxs-lookup"><span data-stu-id="84509-120">You also have a real website.</span></span>  <span data-ttu-id="84509-121">Sie können die Website verwenden, um Ihren Lebenslauf oder Blog zu hosten.</span><span class="sxs-lookup"><span data-stu-id="84509-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="84509-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="84509-122">Prerequisites</span></span>  

<span data-ttu-id="84509-123">Bevor Sie dieses Lernprogramm versuchen, müssen Sie die folgenden Voraussetzungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="84509-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="84509-124">Wenn Sie mit HTML nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="84509-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="84509-125">Laden Sie [den Microsoft Edge][MicrosoftEdgeInsider] herunter.</span><span class="sxs-lookup"><span data-stu-id="84509-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="84509-126">Dieses Lernprogramm verwendet eine Reihe von Webentwicklungstools, die als Microsoft Edge DevTools bezeichnet werden, die in die Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84509-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="84509-127">Einrichten des Codes</span><span class="sxs-lookup"><span data-stu-id="84509-127">Set up your code</span></span>  

<span data-ttu-id="84509-128">Sie erstellen Ihre Website in einem Onlinecode-Editor namens Glitch.</span><span class="sxs-lookup"><span data-stu-id="84509-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="84509-129">Öffnen Sie [den Quellcode][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="84509-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="84509-130">Diese Registerkarte wird in diesem **Lernprogramm als Editorregisterkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="84509-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Die Registerkarte Editor" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="84509-132">Die Registerkarte Editor</span><span class="sxs-lookup"><span data-stu-id="84509-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-133">Wählen **Sie alluring-shock**aus.</span><span class="sxs-lookup"><span data-stu-id="84509-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="84509-134">Das Project Optionen wird in der oberen linken Ecke geöffnet.</span><span class="sxs-lookup"><span data-stu-id="84509-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menü Project Optionen" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="84509-136">Menü Project Optionen</span><span class="sxs-lookup"><span data-stu-id="84509-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-137">Wählen **Sie #A0 Project**aus.</span><span class="sxs-lookup"><span data-stu-id="84509-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="84509-138">Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="84509-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="84509-139">Der Inhalt ist der gleiche wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="84509-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Das gemixte Projekt" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="84509-141">Das gemixte Projekt</span><span class="sxs-lookup"><span data-stu-id="84509-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-142">Wenn Sie planen, das nächste Lernprogramm in dieser Reihe zu beenden, wählen Sie **Anmelden** aus, und melden Sie sich mit Ihrem GitHub oder Ihrem Facebook-Konto bei Glitch an.</span><span class="sxs-lookup"><span data-stu-id="84509-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign into Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="84509-143">Wenn Sie sich nicht bei Ihrem Konto anmelden, verlieren Sie die Möglichkeit, das Projekt zu bearbeiten, nachdem Sie die Bearbeitungsregisterkarte geschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="84509-143">If you choose to not sign into your account, you lose the ability to edit the project after you close the editing tab.</span></span>  
1.  <span data-ttu-id="84509-144">Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**</span><span class="sxs-lookup"><span data-stu-id="84509-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="84509-145">Eine neue Registerkarte wird geöffnet, auf der die Liveseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="84509-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="84509-146">Diese Registerkarte wird in diesem **Lernprogramm als Liveregisterkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="84509-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Die Registerkarte Live" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="84509-148">Die Registerkarte Live</span><span class="sxs-lookup"><span data-stu-id="84509-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="84509-149">Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="84509-149">Add content</span></span>  

<span data-ttu-id="84509-150">Ihre Website ist ziemlich leer.</span><span class="sxs-lookup"><span data-stu-id="84509-150">Your site is pretty empty.</span></span>  <span data-ttu-id="84509-151">Führen Sie die folgenden Schritte aus, um einige Inhalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="84509-151">Follow the steps below to add some content to it.</span></span>  

1.  <span data-ttu-id="84509-152">Ersetzen Sie **auf der Registerkarte Editor**durch `<!-- You're "About Me" will go here.  -->` `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="84509-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Der neue Code wird auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="84509-154">Der neue Code wird auf der Registerkarte Editor hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="84509-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="84509-155">Zeigen Sie Ihre Änderungen auf der **Registerkarte Live an.**  Der Text `About Me` ist auf der Seite sichtbar.</span><span class="sxs-lookup"><span data-stu-id="84509-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="84509-156">Der Text, der größer als der umgebende Text ist, da `<h1>` das Element eine Abschnittsüberschrift darstellt.</span><span class="sxs-lookup"><span data-stu-id="84509-156">The text larger than the surrounding text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="84509-157">In Ihrem Webbrowser werden Überschriften automatisch in größeren Schriftgraden formatiert.</span><span class="sxs-lookup"><span data-stu-id="84509-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift wird auf der Registerkarte Live angezeigt." lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="84509-159">Die neue Überschrift wird auf der Registerkarte Live angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-160">Fügen Sie zurück auf **der Registerkarte Editor**die Zeile unten ein, in der Sie gerade eingefügt `<p>I am learning HTML.  Recent accomplishments:</p>` `<h1>About Me</h1>` haben.</span><span class="sxs-lookup"><span data-stu-id="84509-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Der aktualisierte Code wird auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="84509-162">Der aktualisierte Code wird auf der Registerkarte Editor hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="84509-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="84509-163">Zeigen Sie Ihre Änderung auf der **Registerkarte Live an.**</span><span class="sxs-lookup"><span data-stu-id="84509-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="84509-164">Fügen Sie auf **der Registerkarte Editor**eine Liste Ihrer Erfolge hinzu:</span><span class="sxs-lookup"><span data-stu-id="84509-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Der aktualisierte Code wird auch auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="84509-166">Der aktualisierte Code wird auch auf der Registerkarte Editor hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="84509-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="84509-167">Wechseln Sie erneut zur Registerkarte **Live,** um sicherzustellen, dass der neue Inhalt ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="84509-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Die neue Liste wird auf der Registerkarte Live angezeigt." lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="84509-169">Die neue Liste wird auf der Registerkarte Live angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="84509-170">Experimentieren mit Inhaltsänderungen in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="84509-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="84509-171">Wenn Sie eine große Seite mit viel HTML entwickelt haben, ist es etwas mühsam, hunderte Male zwischen der Editorregisterkarte und der Liveregisterkarte hin- und her zu wechseln, um Ihre Änderungen anzeigen zu können, insbesondere wenn Sie nicht sicher sind, was genau auf der Seite angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84509-171">If you were developing a big page with a lot of HTML, it is somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to display your changes, especially if you are unsure what exactly to put on the page.</span></span>  <span data-ttu-id="84509-172">Microsoft Edge DevTools hilft Ihnen, mit Inhaltsänderungen zu experimentieren, ohne die **Liveregisterkarte zu verlassen.**</span><span class="sxs-lookup"><span data-stu-id="84509-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="84509-173">Erfahren Sie mehr über den Unterschied zwischen HTML und dem DOM</span><span class="sxs-lookup"><span data-stu-id="84509-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="84509-174">Bevor Sie mit der Bearbeitung Ihrer Inhalte Microsoft Edge DevTools beginnen, sollten Sie den Unterschied zwischen HTML und dem DOM verstehen.</span><span class="sxs-lookup"><span data-stu-id="84509-174">Before you start editing your content from Microsoft Edge DevTools, you should understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="84509-175">Die beste Methode, um zu lernen, ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="84509-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="84509-176">Navigieren Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der `A new element!?!` Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-176">Navigate to the **live tab**.  At the bottom of your page, the text `A new element!?!` is displayed.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Am unteren Rand der Seite der Text Ein neues Element!?! wird angezeigt" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="84509-179">Am unteren Rand der Seite wird der `A new element!?!` Text angezeigt</span><span class="sxs-lookup"><span data-stu-id="84509-179">At the bottom of the page the text `A new element!?!` is displayed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-180">Wechseln Sie zurück zur **Registerkarte Editor,** und versuchen Sie, den Text in zu `index.html` finden.</span><span class="sxs-lookup"><span data-stu-id="84509-180">Go back to the **editor tab** and try to find the text in `index.html`.</span></span>  <span data-ttu-id="84509-181">Der Text ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="84509-181">The text is not there.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Der Geheimnistext Ein neues Element!?! ist nirgends in index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="84509-184">Der Mysterientext `A new element!?!` ist in keinem Land zu finden</span><span class="sxs-lookup"><span data-stu-id="84509-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-185">Wechseln Sie zurück zur **Registerkarte Live,** zeigen Sie auf , öffnen Sie das kontextbezogene Menü \(mit der rechten Maustaste `A new element!?!` auf\), und wählen Sie **Überprüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="84509-185">Go back to the **live tab**, hover on `A new element!?!`, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="84509-187">Überprüfen von Text</span><span class="sxs-lookup"><span data-stu-id="84509-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="84509-188">DevTools wird neben Ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="84509-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="84509-189">ist blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="84509-189">is highlighted blue.</span></span>  <span data-ttu-id="84509-190">Obwohl diese Struktur in DevTools wie Ihr HTML aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="84509-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="84509-192">DevTools ist neben der Seite geöffnet</span><span class="sxs-lookup"><span data-stu-id="84509-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="84509-193">Wenn Ihre Seite geladen wird, verwendet der Browser Ihre HTML, um *den* anfänglichen Inhalt der Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84509-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="84509-194">Das DOM stellt den *aktuellen Inhalt* der Seite dar, der sich im Laufe der Zeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="84509-194">The DOM represents the *current* content of the page, which may change over time.</span></span>  <span data-ttu-id="84509-195">Der rätselhafte Inhalt wird Ihrer Seite aufgrund des Tags am unteren `<div>A new element!?!</div>` `<script src="new.js"></script>` Rand Ihres HTML hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="84509-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="84509-196">Dieses Tag bewirkt, dass javaScript-Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84509-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="84509-197">Erfahren Sie mehr über JavaScript in einem späteren Lernprogramm, sehen Sie es aber vorerst als Programmiersprache an, die den Inhalt Ihrer Seite ändern kann.</span><span class="sxs-lookup"><span data-stu-id="84509-197">Learn more about JavaScript in a later tutorial, but for now think of it as a programming language that may change the content of your page.</span></span>  <span data-ttu-id="84509-198">In diesem speziellen Fall wird Der JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="84509-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="84509-199">Aus diesem Grund ist dieser Mysterientext auf Ihrer Liveseite sichtbar, aber nicht in Ihrem HTML.</span><span class="sxs-lookup"><span data-stu-id="84509-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="84509-200">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="84509-200">Edit the DOM</span></span>  

<span data-ttu-id="84509-201">Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Liveregisterkarte zu verlassen, versuchen Sie DevTools.</span><span class="sxs-lookup"><span data-stu-id="84509-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="84509-202">Zeigen Sie in DevTools auf , öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Your site!` Maustaste\), und wählen **Sie Bearbeiten als HTML aus.**</span><span class="sxs-lookup"><span data-stu-id="84509-202">In DevTools, hover on `Your site!`, open the contextual menu \(right-click\), and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Bearbeiten des Knotens als HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="84509-204">Bearbeiten des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="84509-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-205">Ersetzen `<p>Your site!</p>` Sie durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="84509-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Aktualisieren des Knotens als HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="84509-207">Aktualisieren des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="84509-207">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="84509-208">Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um Ihre Änderungen zu speichern, oder wählen Sie außerhalb des Felds aus.</span><span class="sxs-lookup"><span data-stu-id="84509-208">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or choose outside of the box.</span></span>  <span data-ttu-id="84509-209">Ihre Änderungen werden automatisch in der Liveansicht Ihrer Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="84509-210">Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.</span><span class="sxs-lookup"><span data-stu-id="84509-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="84509-212">Der neue Inhalt wird sofort auf der Seite angezeigt</span><span class="sxs-lookup"><span data-stu-id="84509-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="84509-213">Dieser Workflow ist nur für das Experimentieren mit Inhaltsänderungen gut.</span><span class="sxs-lookup"><span data-stu-id="84509-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="84509-214">Wenn Sie die Seite aktualisieren oder die Registerkarte schließen, sind Ihre Änderungen für immer weg.</span><span class="sxs-lookup"><span data-stu-id="84509-214">If you refresh the page or close the tab, your changes are gone forever.</span></span>  <span data-ttu-id="84509-215">Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihren HTML-Code kopieren.</span><span class="sxs-lookup"><span data-stu-id="84509-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="84509-216">In den nächsten Abschnitten werden einige weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur gezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-216">The next couple of sections show you some more ways that you may change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="84509-217">Neu anordnen von Knoten</span><span class="sxs-lookup"><span data-stu-id="84509-217">Reorder nodes</span></span>  

<span data-ttu-id="84509-218">Sie können auch die Reihenfolge der DOM-Knoten ändern.</span><span class="sxs-lookup"><span data-stu-id="84509-218">You may also change the order of DOM nodes.</span></span>  <span data-ttu-id="84509-219">Beispielsweise befindet sich das Navigationsmenü auf Ihrer Webseite in der Nähe des unteren Rands.</span><span class="sxs-lookup"><span data-stu-id="84509-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="84509-220">So verschieben Sie ihn nach oben:</span><span class="sxs-lookup"><span data-stu-id="84509-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="84509-221">Suchen Sie `<nav>` den Knoten in der **DOM-Struktur** von DevTools.</span><span class="sxs-lookup"><span data-stu-id="84509-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in DevTools blau hervorgehoben." lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="84509-223">Der Navigationsknoten ist in DevTools blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="84509-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-224">Ziehen Sie `<nav>` den Knoten nach oben, sodass der Knoten das erste untergeordnete Objekt des `<body>` Knotens ist.</span><span class="sxs-lookup"><span data-stu-id="84509-224">Drag the `<nav>` node to the top, so that the node is the first child of the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="84509-225">Der `<nav>` Knoten wird nun oben auf Der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84509-225">The `<nav>` node is now displaying at the top of your page.</span></span>  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Ziehen des Navigationsknotens nach oben" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="84509-227">Ziehen des Navigationsknotens nach oben</span><span class="sxs-lookup"><span data-stu-id="84509-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich am oberen Rand der Seite." lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="84509-229">Der Navigationsknoten befindet sich am oberen Rand der Seite.</span><span class="sxs-lookup"><span data-stu-id="84509-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="84509-230">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="84509-230">Delete a node</span></span>  

<span data-ttu-id="84509-231">Sie können auch Knoten aus der DOM-Struktur entfernen.</span><span class="sxs-lookup"><span data-stu-id="84509-231">You may also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="84509-232">Wählen Sie **in der DOM-Struktur**die Option `<div>A new element!?!</div>` aus.</span><span class="sxs-lookup"><span data-stu-id="84509-232">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="84509-233">DevTools hebt den Knoten blau hervor.</span><span class="sxs-lookup"><span data-stu-id="84509-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Auswählen des zu löschende Knotens" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="84509-235">Auswählen des zu löschende Knotens</span><span class="sxs-lookup"><span data-stu-id="84509-235">Choose the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-236">Wählen Sie `Delete` die Taste auf der Tastatur aus.</span><span class="sxs-lookup"><span data-stu-id="84509-236">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="84509-237">Der `<div>A new element!?!</div>` Knoten wird aus der DOM-Struktur entfernt.</span><span class="sxs-lookup"><span data-stu-id="84509-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="84509-239">Der Knoten wurde gelöscht</span><span class="sxs-lookup"><span data-stu-id="84509-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="84509-240">Kopieren Der Änderungen</span><span class="sxs-lookup"><span data-stu-id="84509-240">Copy your changes</span></span>  

<span data-ttu-id="84509-241">Sie sind fast fertig.</span><span class="sxs-lookup"><span data-stu-id="84509-241">You're almost done.</span></span>  <span data-ttu-id="84509-242">Sie haben einige Änderungen an Ihrer Seite in DevTools vorgenommen, aber sie werden noch nicht im Quellcode gespeichert.</span><span class="sxs-lookup"><span data-stu-id="84509-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="84509-243">Aktualisieren Sie Ihre **Live-Registerkarte**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, verschwinden.</span><span class="sxs-lookup"><span data-stu-id="84509-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="84509-244">Insbesondere wird der Text am oberen Rand der Seite `Your site!` zurückgegeben, und der Text `A new element!?!` kehrt nach unten zurück.</span><span class="sxs-lookup"><span data-stu-id="84509-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind nicht mehr" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="84509-246">Die von Ihnen vorgenommenen Änderungen sind nicht mehr</span><span class="sxs-lookup"><span data-stu-id="84509-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84509-247">Kopieren Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="84509-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="84509-248">Wechseln Sie zurück zur **Registerkarte Editor,** und ersetzen Sie den Inhalt Ihrer Datei durch den `index.html` Code, den Sie gerade kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="84509-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="So sollte ihre index.html aussehen" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="84509-250">So sollte `index.html` Ihre Datei aussehen</span><span class="sxs-lookup"><span data-stu-id="84509-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="84509-251">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="84509-251">Next steps</span></span>  

*   <span data-ttu-id="84509-252">Führen Sie das nächste Lernprogramm in dieser Reihe [Erste Schritte css][DevToolsBeginnersCss]aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Formatänderungen in devTools Microsoft Edge experimentieren.</span><span class="sxs-lookup"><span data-stu-id="84509-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="84509-253">Lesen [Sie Einführung in das DOM,][MDNIntroductionDom] um mehr über das DOM zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="84509-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="84509-254">Sehen Sie sich einen Kurs wie [Einführung in die Webentwicklung an,][CourseraIntroductionToWebDevelopment] um mehr praktische Webentwicklungserfahrung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84509-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="84509-255">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="84509-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS-| Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in web development | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html – verlockende | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML-| MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| MDN"  

> [!NOTE]
> <span data-ttu-id="84509-262">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84509-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="84509-263">Die ursprüngliche Seite wurde [hier gefunden](https://developers.google.com/web/tools/chrome-devtools/beginners/html) und von [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="84509-263">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="84509-265">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="84509-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
