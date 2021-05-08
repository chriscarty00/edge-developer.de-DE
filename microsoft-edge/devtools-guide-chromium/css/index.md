---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen und Ändern des CSS einer Seite verwenden.
title: Erste Schritte mit dem Anzeigen und Ändern von CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399092"
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

# <a name="get-started-with-viewing-and-changing-css"></a><span data-ttu-id="a6ad5-104">Erste Schritte mit dem Anzeigen und Ändern von CSS</span><span class="sxs-lookup"><span data-stu-id="a6ad5-104">Get started with viewing and changing CSS</span></span>  

<span data-ttu-id="a6ad5-105">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen des Anzeigens und Änderns der CSS für eine Seite mithilfe von Microsoft Edge DevTools zu erlernen.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <a name="open-css-examples"></a><span data-ttu-id="a6ad5-106">Öffnen von CSS-Beispielen</span><span class="sxs-lookup"><span data-stu-id="a6ad5-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="a6ad5-107">Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **CSS-Beispiele aus,** um sie in einem neuen Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="a6ad5-108">CSS-Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6ad5-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="a6ad5-109">Wenn Sie Ihr [DevTools-Fenster][DevToolsCustomizePlacement] rechts neben Ihrem Viewport \(in der folgenden Abbildung angezeigt) andocken möchten, wählen Sie Anpassen und Steuern von **DevTools aus.** `...`</span><span class="sxs-lookup"><span data-stu-id="a6ad5-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="a6ad5-110">Wählen Sie **im Dropdownmenü Anpassen** und Steuern von DevTools im Abschnitt **Dock** nach rechts **Dock aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <a name="view-the-css-for-an-element"></a><span data-ttu-id="a6ad5-111">Anzeigen der CSS für ein Element</span><span class="sxs-lookup"><span data-stu-id="a6ad5-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="a6ad5-112">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a6ad5-113">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Inspect Me!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="a6ad5-114">In DevTools wird das **Element im Elementtool** im **BEREICH DOM-Struktur** `Inspect Me!` hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-114">In DevTools, on the **Elements** tool, in the **DOM Tree** panel, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Das überprüfte Element wird in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="a6ad5-116">Das überprüfte Element wird in der **DOM-Struktur hervorgehoben.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-116">The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="a6ad5-117">Suchen Sie `Inspect Me!` im Element nach dem Wert des `data-message` Attributs, und kopieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="a6ad5-118">Geben Sie auf der Seite im **Textfeld Wert von `data-message` :** den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="a6ad5-119">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Inspect Me!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="a6ad5-120">Wählen Sie in DevTools im **Tool Elemente** den Bereich **Formatvorlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-120">In DevTools, on the **Elements** tool, select the **Styles** panel.</span></span>  
    1.  <span data-ttu-id="a6ad5-121">Im **Bereich Formatvorlagen** wird `Inspect Me!` das Element hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-121">In the **Styles** panel, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="a6ad5-122">Suchen Sie `Inspect Me!` im Element nach der `aloha` Klassenregel.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="a6ad5-123">Diese Regel wird angezeigt, da sie auf das Element angewendet `Inspect Me!` wird.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-123">This rule is displayed, because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="a6ad5-124">Suchen Sie `aloha` in der Klasse nach dem Wert für die `padding` Formatvorlage, und kopieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="CSS-Klassen, die auf das überprüfte Element angewendet werden, werden im Bereich Formatvorlagen hervorgehoben." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="a6ad5-126">CSS-Klassen werden auf das ausgewählte Element angewendet, z. B. `aloha` , werden im **Formatvorlagenbereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-126">CSS classes is applied to the selected element, such as `aloha`, are displayed in the **Styles** panel</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="a6ad5-127">Geben Sie auf der Seite im **Textfeld Wert von `padding` :** den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="a6ad5-128">Hinzufügen einer CSS-Deklaration zu einem Element</span><span class="sxs-lookup"><span data-stu-id="a6ad5-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="a6ad5-129">Verwenden Sie **den Formatvorlagenbereich,** wenn Sie einem Element CSS-Deklarationen ändern oder hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-129">Use the **Styles** panel when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6ad5-130">Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a6ad5-131">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a6ad5-132">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Add A Background Color To Me!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a6ad5-133">Wählen `element.style` Sie am oberen Rand des **Formatvorlagenbereichs** aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-133">Choose `element.style` near the top of the **Styles** panel.</span></span>  
1.  <span data-ttu-id="a6ad5-134">Geben `background-color` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="a6ad5-135">Geben `honeydew` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="a6ad5-136">In der **DOM-Struktur**wird eine auf das Element angewendete Inlineformatdeklaration angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-136">In the **DOM Tree**, an inline style declaration applied to the element is displayed.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Hinzufügen einer CSS-Deklaration zum Element mithilfe des Formatvorlagenbereichs" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="a6ad5-138">Die Deklaration wird mithilfe des Abschnitts `background-color:honeydew` `element.style` des Formatvorlagenbereichs auf das **Element** angewendet.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-138">The `background-color:honeydew` declaration is applied to the element using the `element.style` section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a><span data-ttu-id="a6ad5-139">Hinzufügen einer CSS-Klasse zu einem Element</span><span class="sxs-lookup"><span data-stu-id="a6ad5-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="a6ad5-140">Navigieren Sie zum Formatvorlagenbereich, um zu zeigen, wie ein Element aussieht, wenn eine CSS-Klasse auf ein Element angewendet oder aus diesem entfernt **wird.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-140">To display how an element looks when a CSS class is applied to or removed from an element, navigate to the **Styles** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6ad5-141">Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a6ad5-142">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a6ad5-143">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Add A Class To Me!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a6ad5-144">Wählen **Sie .cls**aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-144">Choose **.cls**.</span></span>  <span data-ttu-id="a6ad5-145">DevTools zeigt ein Textfeld an, in dem Sie dem ausgewählten Element Klassen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="a6ad5-146">Geben `color_me` Sie in das Textfeld Neue Klasse **hinzufügen** ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="a6ad5-147">Unterhalb des Textfelds Neue **Klasse** hinzufügen wird ein Kontrollkästchen angezeigt, in dem Sie die Klasse ein- und ausschalten können.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="a6ad5-148">Wenn auf das Element andere Klassen angewendet wurden, können Sie auch von hier aus `Add A Class To Me!` umschalten.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Anwenden der color_me-Klasse auf das Element" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="a6ad5-150">Die `color_me` Klasse wird mithilfe des **Abschnitts CLS** des Formatvorlagenbereichs auf das **Element** angewendet.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-150">The `color_me` class is applied to the element using the **.cls** section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a><span data-ttu-id="a6ad5-151">Hinzufügen eines Pseudozustands zu einer Klasse</span><span class="sxs-lookup"><span data-stu-id="a6ad5-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="a6ad5-152">Verwenden Sie **den Formatvorlagenbereich,** um einen CSS-Pseudozustand dauerhaft auf ein Element anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-152">Use the **Styles** panel to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="a6ad5-153">DevTools unterstützt `:active` , `:focus` , und `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="a6ad5-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6ad5-154">Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a6ad5-155">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a6ad5-156">Zeigen Sie auf den `Hover Over Me!` Text.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-156">Hover on the `Hover Over Me!` text.</span></span>  <span data-ttu-id="a6ad5-157">Die Hintergrundfarbe ändert sich.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-157">The background color changes.</span></span>  
1.  <span data-ttu-id="a6ad5-158">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Hover Over Me!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a6ad5-159">Wählen Sie **im Bereich** Formatvorlagen die Option **:hov aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-159">In the **Styles** panel, choose **:hov**.</span></span>  
1.  <span data-ttu-id="a6ad5-160">Aktivieren Sie das **Kontrollkästchen :hover.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="a6ad5-161">Die Hintergrundfarbe ändert sich wie zuvor, auch wenn Sie nicht mit dem Mauszeiger auf das Element zeigen.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Umschalten des Hover-Pseudozustands für ein Element" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="a6ad5-163">Umschalten des `:hover` Pseudozustands für ein Element</span><span class="sxs-lookup"><span data-stu-id="a6ad5-163">Toggle the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a><span data-ttu-id="a6ad5-164">Ändern der Dimensionen eines Elements</span><span class="sxs-lookup"><span data-stu-id="a6ad5-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="a6ad5-165">Verwenden Sie **das interaktive** \*\*\*\* Diagramm Box Model im Bereich Formatvorlagen, um die Breite, Höhe, Abstand, Rand- oder Rahmenlänge eines Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-165">Use the **Box Model** interactive diagram in the **Styles** panel to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="a6ad5-166">Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a6ad5-167">[Öffnen Sie CSS-Beispiele](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a6ad5-168">Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Change My Margin!` Maustaste\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a6ad5-169">Zeigen Sie **im Diagramm Feldmodell** im Bereich **Formatvorlagen** auf **Abstand.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-169">In the **Box Model** diagram in the **Styles** panel, hover on **padding**.</span></span>  <span data-ttu-id="a6ad5-170">Der Abstand eines Elements wird im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="a6ad5-171">Abhängig von der Größe Ihres DevTools-Fensters müssen Sie \*\*\*\* möglicherweise einen Bildlauf zum unteren Rand des Formatvorlagenbereichs durchführen, um das **Feldmodell anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** panel to display the **Box Model**.</span></span>  

1.  <span data-ttu-id="a6ad5-172">Doppelklicken Sie im **Feldmodell**auf den linken Rand, der aktuell bedeutet, dass das Element keinen linken `-` Rand hat.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="a6ad5-173">Geben `100px` Sie ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="a6ad5-174">Das **Feldmodell** ist standardmäßig auf Pixel festgelegt, akzeptiert aber auch andere Werte, z. B. `25%` , oder `10vw` .</span><span class="sxs-lookup"><span data-stu-id="a6ad5-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Zeigen auf den Abstand des Elements" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="a6ad5-176">Zeigen auf den Abstand des Elements</span><span class="sxs-lookup"><span data-stu-id="a6ad5-176">Hover on the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Ändern des linken Rands des Elements" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="a6ad5-178">Ändern des linken Rands des Elements</span><span class="sxs-lookup"><span data-stu-id="a6ad5-178">Change the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a><span data-ttu-id="a6ad5-179">Debuggen von Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="a6ad5-179">Debugging Media Queries</span></span>  

<span data-ttu-id="a6ad5-180">[Medienabfragen][MDNUsingMediaGueries] sind eine Möglichkeit, ihr Webprodukt auf Änderungen in den Konfigurationseinstellungen für jeden Benutzer zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="a6ad5-181">Der wichtigste Verwendungsfall ist die Bereitstellung eines anderen CSS-Layouts in Abhängigkeit von den Abmessungen des Viewports.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="a6ad5-182">Die Verwendung separater Layouts ermöglicht ein einspaltiges Layout für mobile Geräte und mehrspaltige Layouts, wenn mehr Bildschirmaufteilung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="a6ad5-183">Wenn Sie die in Ihrer CSS definierten Medienabfragen debuggen oder testen möchten, verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="a6ad5-184">Öffnen Sie die Entwicklertools, und wählen Sie auf der linken oberen Seite das Symbol Symbolleiste des Umschaltgeräts aus, oder wählen Sie \*\*\*\* `Ctrl` + `Shift` + `M` \( unter `Cmd` + `Shift` + `M` macOS\).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Öffnen der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="a6ad5-186">Öffnen der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="a6ad5-186">Open the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a6ad5-187">Wenn die Gerätesymbolleiste geöffnet ist, wählen Sie das `...` Menü oben rechts aus, und wählen Sie **Medienabfragen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="a6ad5-188">Die farbigen Balken, die über der Webseite angezeigt werden, stellen die verschiedenen Medienabfragen dar.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-188">The colored bars displayed above the webpage represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Anzeigen von Medienabfragen in der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="a6ad5-190">Anzeigen von Medienabfragen in der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="a6ad5-190">Show Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a6ad5-191">Zeigen Sie auf die Begrenzungen in den Balken, um die Werte der verschiedenen Medienabfragen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-191">Hover on the boundaries in the bars to display the values of the different media queries.</span></span>  <span data-ttu-id="a6ad5-192">Wählen Sie jeweils aus, um die zu ändernde Webseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-192">Choose each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Auswählen von Medienabfragen in der Vorschauleiste" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="a6ad5-194">Auswählen von Medienabfragen in der Vorschauleiste</span><span class="sxs-lookup"><span data-stu-id="a6ad5-194">Choose Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a6ad5-195">Um Medienabfragen zu debuggen und die #A0 im Editor zu öffnen, zeigen Sie auf eines der Balkensegmente, öffnen Sie das Kontextmenü `Sources` \(rechtsklicken\), und wählen Sie `reveal in source code` aus.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Enthebnen von Medienabfragen im Quellen-Editor" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="a6ad5-197">Enthebnen von Medienabfragen im Quellen-Editor</span><span class="sxs-lookup"><span data-stu-id="a6ad5-197">Reveal Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a6ad5-198">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a6ad5-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "CSS-Beispiele – Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von Medienabfragen | MDN"  

> [!NOTE]
> <span data-ttu-id="a6ad5-202">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a6ad5-203">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a6ad5-205">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a6ad5-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
