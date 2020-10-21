---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um das CSS einer Seite anzuzeigen und zu ändern.
title: Erste Schritte mit dem Anzeigen und Ändern von CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3cd833c97cb2e7b746943f18526d09481b4e3cc5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125209"
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

# <span data-ttu-id="69c7d-104">Erste Schritte mit dem Anzeigen und Ändern von CSS</span><span class="sxs-lookup"><span data-stu-id="69c7d-104">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="69c7d-105">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen für das Anzeigen und Ändern des CSS für eine Seite mit Microsoft Edge devtools zu erlernen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="69c7d-106">Öffnen von CSS-Beispielen</span><span class="sxs-lookup"><span data-stu-id="69c7d-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="69c7d-107">Halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie **CSS-Beispiele** aus, um Sie in einem neuen Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="69c7d-108">CSS-Beispiele</span><span class="sxs-lookup"><span data-stu-id="69c7d-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="69c7d-109">Wenn Sie Ihr devtools-Fenster auf der rechten Seite Ihres Viewports [Andocken][DevToolsCustomizePlacement] möchten (in der folgenden Abbildung dargestellt \), wählen Sie **anpassen und Steuer devtools** `...` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="69c7d-110">Wählen Sie im Dropdownmenü **anpassen und Steuern des devtools** im Abschnitt **Docking Seite** die Option **Dock to right**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <span data-ttu-id="69c7d-111">Anzeigen des CSS für ein Element</span><span class="sxs-lookup"><span data-stu-id="69c7d-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="69c7d-112">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="69c7d-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="69c7d-113">Zeigen Sie auf den `Inspect Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="69c7d-114">In devtools wird das Element im Panel **Elemente** auf der Registerkarte **DOM** -Struktur `Inspect Me!` hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="69c7d-114">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="69c7d-116">Abbildung 1: das geprüfte Element ist in der **DOM-Struktur** hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="69c7d-116">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="69c7d-117">`Inspect Me!`Suchen Sie im Element den Wert des Attributs, `data-message` und kopieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="69c7d-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="69c7d-118">Geben Sie auf der Seite im **Wert von `data-message` :** TextBox den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="69c7d-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="69c7d-119">Zeigen Sie auf den `Inspect Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="69c7d-120">Wählen Sie in devtools im Panel **Elemente** die Registerkarte **Formatvorlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="69c7d-121">Auf der Registerkarte **Formatvorlagen** `Inspect Me!` ist das Element hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="69c7d-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="69c7d-122">`Inspect Me!`Suchen Sie im Element die `aloha` Klassen Regel.</span><span class="sxs-lookup"><span data-stu-id="69c7d-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="69c7d-123">Diese Regel wird angezeigt, weil Sie auf das Element angewendet wird `Inspect Me!` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="69c7d-124">`aloha`Suchen Sie in der Klasse den Wert für die `padding` Formatvorlage, und kopieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="69c7d-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="69c7d-126">Abbildung 2: CSS-Klassen, die auf das ausgewählte Element angewendet werden, wie etwa `aloha` , werden auf der Registerkarte " **Formatvorlagen** " angezeigt</span><span class="sxs-lookup"><span data-stu-id="69c7d-126">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="69c7d-127">Geben Sie auf der Seite im **Wert von `padding` :** TextBox den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="69c7d-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="69c7d-128">Hinzufügen einer CSS-Deklaration zu einem Element</span><span class="sxs-lookup"><span data-stu-id="69c7d-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="69c7d-129">Verwenden Sie die Registerkarte **Formatvorlagen** , wenn Sie einem Element CSS-Deklarationen ändern oder hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="69c7d-129">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c7d-130">Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="69c7d-131">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="69c7d-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="69c7d-132">Zeigen Sie auf den `Add A Background Color To Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="69c7d-133">Wählen Sie am `element.style` oberen Rand der Registerkarte **Formatvorlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-133">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="69c7d-134">Geben `background-color` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="69c7d-135">Geben `honeydew` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="69c7d-136">In der **DOM-Struktur** sollten Sie sehen, dass eine Inlineformatvorlagen Deklaration auf das Element angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="69c7d-136">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="69c7d-138">Abbildung 3: die `background-color:honeydew` Deklaration wurde auf das Element über den `element.style` Abschnitt der Registerkarte " **Formatvorlagen** " angewendet</span><span class="sxs-lookup"><span data-stu-id="69c7d-138">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69c7d-139">Hinzufügen einer CSS-Klasse zu einem Element</span><span class="sxs-lookup"><span data-stu-id="69c7d-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="69c7d-140">Verwenden Sie die Registerkarte **Formatvorlagen** , um zu sehen, wie ein Element aussieht, wenn eine CSS-Klasse auf ein Element angewendet oder daraus entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="69c7d-140">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c7d-141">Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="69c7d-142">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="69c7d-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="69c7d-143">Zeigen Sie auf den `Add A Class To Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="69c7d-144">Wählen Sie **CLS**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-144">Choose **.cls**.</span></span>  <span data-ttu-id="69c7d-145">DevTools zeigt ein Textfeld an, in dem Sie dem ausgewählten Elementklassen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="69c7d-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="69c7d-146">Geben `color_me` Sie das Textfeld **neue Klasse hinzufügen** ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="69c7d-147">Unterhalb des Textfelds **neue Klasse hinzufügen** wird ein Kontrollkästchen eingeblendet, in dem Sie die Klasse ein-und ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="69c7d-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="69c7d-148">Wenn `Add A Class To Me!` auf das Element andere Klassen angewendet werden, können Sie auch von hier aus umschalten.</span><span class="sxs-lookup"><span data-stu-id="69c7d-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="69c7d-150">Abbildung 4: die `color_me` Klasse wurde auf das Element mit dem Abschnitt " **. CLS** " auf der Registerkarte " **Formatvorlagen** " angewendet.</span><span class="sxs-lookup"><span data-stu-id="69c7d-150">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69c7d-151">Hinzufügen eines PseudoState zu einer Klasse</span><span class="sxs-lookup"><span data-stu-id="69c7d-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="69c7d-152">Verwenden Sie die Registerkarte **Formatvorlagen** , um eine CSS-PseudoState dauerhaft auf ein Element anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="69c7d-152">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="69c7d-153">DevTools unterstützt `:active` , `:focus` , `:hover` und `:visited` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c7d-154">Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="69c7d-155">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="69c7d-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="69c7d-156">Zeigen Sie mit der Maus auf den `Hover Over Me!` Text.</span><span class="sxs-lookup"><span data-stu-id="69c7d-156">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="69c7d-157">Die Hintergrundfarbe ändert sich.</span><span class="sxs-lookup"><span data-stu-id="69c7d-157">The background color changes.</span></span>  
1.  <span data-ttu-id="69c7d-158">Zeigen Sie auf den `Hover Over Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="69c7d-159">Wählen Sie auf der Registerkarte **Formatvorlagen** die Option **: Hov**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-159">In the **Styles** tab, choose **:hov**.</span></span>  
1.  <span data-ttu-id="69c7d-160">Aktivieren Sie das Kontrollkästchen **Hover** .</span><span class="sxs-lookup"><span data-stu-id="69c7d-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="69c7d-161">Die Hintergrundfarbe ändert sich wie zuvor, auch wenn Sie nicht tatsächlich auf das Element zeigen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="69c7d-163">Abbildung 5: `:hover` Umschalten des PseudoState für ein Element</span><span class="sxs-lookup"><span data-stu-id="69c7d-163">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69c7d-164">Ändern der Abmessungen eines Elements</span><span class="sxs-lookup"><span data-stu-id="69c7d-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="69c7d-165">Verwenden Sie das interaktive Diagramm des **Feld Modells** auf der Registerkarte **Formatvorlagen** , um die Breite, Höhe, Abstand, Seitenrand oder die Rahmenlänge eines Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="69c7d-165">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c7d-166">Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="69c7d-167">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="69c7d-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="69c7d-168">Zeigen Sie auf den `Change My Margin!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="69c7d-169">Zeigen Sie im Diagramm **Feld Modell** auf der Registerkarte **Formatvorlagen** auf **Abstand**.</span><span class="sxs-lookup"><span data-stu-id="69c7d-169">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="69c7d-170">Der Abstand eines Elements wird im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="69c7d-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="69c7d-171">Je nach Größe des devtools-Fensters müssen Sie möglicherweise an den unteren Rand der Registerkarte **Formatvorlagen** scrollen, um das **Feld Modell**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="69c7d-172">Doppelklicken Sie auf den linken Rand im **Feld Modell**, das derzeit den Wert Bedeutung hat, `-` dass das Element keinen linken Rand aufweist.</span><span class="sxs-lookup"><span data-stu-id="69c7d-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="69c7d-173">Geben `100px` Sie ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="69c7d-174">Das **Feld Modell** ist standardmäßig Pixel, akzeptiert aber auch andere Werte wie " `25%` oder" `10vw` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="69c7d-176">Abbildung 6: Bewegen des Mauszeigers über den Abstand des Elements</span><span class="sxs-lookup"><span data-stu-id="69c7d-176">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="69c7d-178">Abbildung 7: Ändern des linken Rands des Elements</span><span class="sxs-lookup"><span data-stu-id="69c7d-178">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="69c7d-179">Debuggen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="69c7d-179">Debugging Media Queries</span></span>  

<span data-ttu-id="69c7d-180">[Medienabfragen][MDNUsingMediaGueries] stellen eine Möglichkeit dar, damit Ihr Web-Produkt auf Änderungen in den Konfigurationseinstellungen für jeden Benutzer reagiert.</span><span class="sxs-lookup"><span data-stu-id="69c7d-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="69c7d-181">Der bedeutendste Anwendungsfall besteht darin, dem Produkt je nach Größe des Viewports ein anderes CSS-Layout bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="69c7d-182">Das Verwenden separater Layouts ermöglicht ein Layout mit einer Spalte für mobile Geräte und mehrspaltige Layouts, wenn mehr Bildschirm Auflagen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="69c7d-183">Führen Sie die folgenden Schritte aus, wenn Sie die medienabfragen, die Sie in Ihrem CSS definiert haben, Debuggen oder testen möchten.</span><span class="sxs-lookup"><span data-stu-id="69c7d-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="69c7d-184">Öffnen Sie die Entwicklertools, und wählen Sie in der oberen linken Ecke das Symbol " **Gerätesymbolleiste umschalten** " aus, oder wählen Sie `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` unter macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="69c7d-186">Abbildung 8: Öffnen der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="69c7d-186">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c7d-187">Wenn die Gerätesymbolleiste geöffnet ist, wählen Sie das `...` Menü oben rechts aus, und wählen Sie **medienabfragen anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="69c7d-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="69c7d-188">Oberhalb der Anzeige der Seite sollten farbige Balken angezeigt werden, die die verschiedenen medienabfragen darstellen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-188">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="69c7d-190">Abbildung 9: Anzeigen von medienabfragen in der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="69c7d-190">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c7d-191">Zeigen Sie mit der Maus auf die Begrenzungen in den Balken, um die Werte der verschiedenen medienabfragen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-191">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="69c7d-192">Wählen Sie die einzelnen Seiten aus, um die Größe der Webseite anzupassen.</span><span class="sxs-lookup"><span data-stu-id="69c7d-192">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="69c7d-194">Abbildung 10: Auswählen der medienabfrage aus der Vorschauleiste</span><span class="sxs-lookup"><span data-stu-id="69c7d-194">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c7d-195">Um medienabfragen zu Debuggen und die CSS-Datei im Editor zu öffnen, bewegen Sie den `Sources` Mauszeiger auf einem beliebigen Balkensegment, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="69c7d-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="69c7d-197">Abbildung 11: Anzeigen von medienabfragen im Quellen-Editor</span><span class="sxs-lookup"><span data-stu-id="69c7d-197">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69c7d-198">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="69c7d-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "CSS-Beispiele – Microsoft Edge (Chrom) devtools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von medienabfragen | MDN"  

> [!NOTE]
> <span data-ttu-id="69c7d-202">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69c7d-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="69c7d-203">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="69c7d-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="69c7d-205">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69c7d-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
