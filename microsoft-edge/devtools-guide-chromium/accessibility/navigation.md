---
title: Navigieren in Microsoft Edge devtools mit Hilfstechnologien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567045"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="b4faa-103">Navigieren in Microsoft Edge devtools mit Hilfstechnologien</span><span class="sxs-lookup"><span data-stu-id="b4faa-103">Navigate Microsoft Edge DevTools With Assistive Technology</span></span>   



<span data-ttu-id="b4faa-104">Dieser Leitfaden soll Benutzern helfen, die in erster Linie auf Hilfstechnologien wie Bildschirmsprachausgaben zugreifen und Microsoft Edge devtools verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-104">This guide aims to help users who primarily rely on assistive technology like screen readers access and use Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b4faa-105">Microsoft Edge devtools ist eine Suite von Webentwickler Tools, die in den Microsoft Edge-Browser integriert sind.</span><span class="sxs-lookup"><span data-stu-id="b4faa-105">Microsoft Edge DevTools is a suite of web developer tools built into the Microsoft Edge browser.</span></span>  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

<span data-ttu-id="b4faa-106">Die Barrierefreiheit von devtools ist eine Work-in-Progress-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b4faa-106">The accessibility of DevTools is a work-in-progress.</span></span>  <span data-ttu-id="b4faa-107">Einige Panels und Registerkarten funktionieren mit Hilfstechnologien besser als andere.</span><span class="sxs-lookup"><span data-stu-id="b4faa-107">Some panels and tabs work better with assistive technology than others.</span></span>  <span data-ttu-id="b4faa-108">Dieser Leitfaden führt Sie durch die Panels, die am häufigsten zugänglich sind, und hebt spezifische Probleme hervor, auf die Sie auf dem Weg stoßen können.</span><span class="sxs-lookup"><span data-stu-id="b4faa-108">This guide walks you through the panels which are the most accessible and highlights specific issues you may encounter along the way.</span></span>  

## <span data-ttu-id="b4faa-109">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b4faa-109">Overview</span></span>   

<span data-ttu-id="b4faa-110">Bevor Sie beginnen, hilft es, ein geistiges Modell für die Strukturierung der devtools-Benutzeroberfläche zu haben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-110">Before starting, it helps to have a mental model of how the DevTools UI is structured.</span></span>  <span data-ttu-id="b4faa-111">DevTools ist in eine Reihe von Tafeln unterteilt, die in [einer `tablist` Arie ][W3CWaiAriaTablist]organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="b4faa-111">DevTools is divided into a series of panels which are organized into an [ARIA `tablist`][W3CWaiAriaTablist].</span></span>  

<span data-ttu-id="b4faa-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b4faa-112">For example:</span></span>  

*   <span data-ttu-id="b4faa-113">Im Panel **Elemente** können Sie DOM-Knoten oder [CSS] [DevtoolsCssIndex] anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="b4faa-113">The **Elements** panel lets you view and change DOM nodes or [CSS][DevtoolsCssIndex].</span></span>  
*   <span data-ttu-id="b4faa-114">Mit [**Console** Panel] [DevtoolsConsoleIndex] können Sie JavaScript-Protokolle und Live-Bearbeitungs Objekte lesen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-114">The [**Console** panel][DevtoolsConsoleIndex] lets you read JavaScript logs and live edit objects.</span></span>  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

<span data-ttu-id="b4faa-115">Im Inhaltsbereich jedes Bereichs gibt es eine Reihe unterschiedlicher Tools, die häufig als Tabstopps oder Bereiche in der Dokumentation bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-115">Within the content area of each panel, there are a number of different tools, often referred to as tabs or panes in the documentation.</span></span>  
<span data-ttu-id="b4faa-116">Beispielsweise enthält das Panel **Elemente** weitere Registerkarten, um Ereignislistener, die Barrierefreiheits Struktur und vieles mehr zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-116">For instance, the **Elements** panel contains additional tabs to inspect event listeners, the accessibility tree, and much more.</span></span>  <span data-ttu-id="b4faa-117">Die Unterscheidung zwischen Registerkarten und Fensterbereichen ist etwas willkürlich.</span><span class="sxs-lookup"><span data-stu-id="b4faa-117">The distinction between tabs and panes is somewhat arbitrary.</span></span>  <span data-ttu-id="b4faa-118">Der einzige Grund, warum Sie möglicherweise einen oder den anderen Ausdruck sehen, besteht darin, die Konsistenz mit der restlichen offiziellen devtools-Dokumentation beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b4faa-118">The only reason you may see one term or the other is to maintain consistency with the rest of the official DevTools documentation.</span></span>  

## <span data-ttu-id="b4faa-119">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="b4faa-119">Keyboard shortcuts</span></span>   

<span data-ttu-id="b4faa-120">Die [devtools-Tastenkombinationen] [DevtoolsShortcuts] ist ein hilfreiches Cheatsheet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-120">The [DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] is a helpful cheatsheet.</span></span>  <span data-ttu-id="b4faa-121">Achten Sie darauf, die Textmarke zu markieren, und beziehen Sie sich darauf, während Sie die verschiedenen Panels erkunden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-121">Be sure to bookmark it and refer back to it as you explore the different panels.</span></span>  

## <span data-ttu-id="b4faa-122">Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="b4faa-122">Open DevTools</span></span>   

<span data-ttu-id="b4faa-123">Lesen Sie zunächst [Open Microsoft Edge devtools] [DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="b4faa-123">To get started, read through [Open Microsoft Edge DevTools][DevtoolsOpen].</span></span>  <span data-ttu-id="b4faa-124">Es gibt eine Reihe von Möglichkeiten, devtools zu öffnen, entweder über Tastenkombinationen oder Menüelemente.</span><span class="sxs-lookup"><span data-stu-id="b4faa-124">There are a number of ways to open DevTools, either through keyboard shortcuts or menu items.</span></span>  

## <span data-ttu-id="b4faa-125">Navigieren zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="b4faa-125">Navigate between panels</span></span>   

### <span data-ttu-id="b4faa-126">Navigieren mithilfe der Tastatur</span><span class="sxs-lookup"><span data-stu-id="b4faa-126">Navigate by keyboard</span></span>   

*   <span data-ttu-id="b4faa-127">Drücken Sie bei geöffnetem devtools `Control` + `]` \ (Windows \) oder `Command` + `]` \ (macOS \), um den Fokus auf das nächste Fenster zu legen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-127">With DevTools open, press `Control`+`]` \(Windows\) or `Command`+`]` \(macOS\) to focus the next panel.</span></span>  
*   <span data-ttu-id="b4faa-128">Drücken Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \), um den Fokus auf das vorherige Panel zu legen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-128">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) to focus the previous panel.</span></span>  
*   <span data-ttu-id="b4faa-129">Es ist auch möglich, den `Shift` + `Tab` Fokus in die [Aria `tablist` ][W3CWaiAriaTablist] eines Panels zu verschieben und die Pfeiltasten zum Ändern von Panels zu verwenden, obwohl es möglicherweise schneller ist, die zuvor erwähnten Tastenkombinationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-129">It is also possible to use `Shift`+`Tab` to move focus into the [ARIA `tablist`][W3CWaiAriaTablist] of a panel and use the arrow keys to change panels, though it may be faster to use the previously mentioned shortcuts.</span></span>  

#### <span data-ttu-id="b4faa-130">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-130">Known issues</span></span>   

*   <span data-ttu-id="b4faa-131">Einige Panels, wie die **Konsolen** -und **Leistungs** Bereiche, können den Fokus in den Inhaltsbereich verschieben, sobald Sie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="b4faa-131">Some panels, such as the **Console** and **Performance** panels, may move focus into their content area as soon as they are activated.</span></span>  <span data-ttu-id="b4faa-132">Dadurch kann die Navigation mit Pfeiltasten schwierig werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-132">This may make navigating by arrow keys difficult.</span></span>  
*   <span data-ttu-id="b4faa-133">Der Name des ausgewählten Panels wird angekündigt, aber erst, nachdem er den fokussierten Inhalt im Panel gelesen hat.</span><span class="sxs-lookup"><span data-stu-id="b4faa-133">The name of the selected panel is announced, but only after it has read the focused content in the panel.</span></span>  <span data-ttu-id="b4faa-134">Dies kann sehr einfach zu versäumen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-134">This may make it very easy to miss.</span></span>  

### <span data-ttu-id="b4faa-135">Navigieren nach Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="b4faa-135">Navigate by Command Menu</span></span>   

<span data-ttu-id="b4faa-136">Wenn Sie ein bestimmtes Panel fokussieren möchten, verwenden Sie das [**Befehlsmenü**] [DevtoolsCommandMenuIndex]:</span><span class="sxs-lookup"><span data-stu-id="b4faa-136">To focus a specific panel, use the [**Command Menu**][DevtoolsCommandMenuIndex]:</span></span>  

1.  <span data-ttu-id="b4faa-137">Drücken Sie bei geöffnetem devtools `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-137">With DevTools open, press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    <span data-ttu-id="b4faa-138">Das **Befehl-Menü** ist ein Fuzzy-Such-AutoVervollständigen-Kombinationsfeld.</span><span class="sxs-lookup"><span data-stu-id="b4faa-138">The **Command Menu** is a fuzzy search autocomplete combobox.</span></span>  
1.  <span data-ttu-id="b4faa-139">Geben Sie den Namen des Panels ein, das Sie öffnen möchten, und navigieren Sie dann mithilfe der `Down Arrow` auf der Tastatur zur richtigen Option.</span><span class="sxs-lookup"><span data-stu-id="b4faa-139">Type the name of the panel you want to open, then use the `Down Arrow` on the keyboard to navigate to the correct option.</span></span>  
1.  <span data-ttu-id="b4faa-140">Drücken Sie `Enter` , um einen Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-140">Press `Enter` to run a command.</span></span>  

<span data-ttu-id="b4faa-141">So öffnen Sie beispielsweise das Panel **Elemente** :</span><span class="sxs-lookup"><span data-stu-id="b4faa-141">For example, to open the **Elements** panel:</span></span>  

1.  <span data-ttu-id="b4faa-142">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="b4faa-142">Open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="b4faa-143">Geben Sie `E` dann ein `L` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-143">Type `E` then `L`.</span></span>  <span data-ttu-id="b4faa-144">Die Option **Panel > Elemente anzeigen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b4faa-144">The **Panel > Show Elements** option is selected.</span></span>  
1.  <span data-ttu-id="b4faa-145">Drücken Sie `Enter` , um den Befehl auszuführen, der das Fenster öffnet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-145">Press `Enter` to run the command that opens the panel.</span></span>  

<span data-ttu-id="b4faa-146">Wenn Sie ein Panel auf diese Weise öffnen, wird der Fokus auf den Inhalt des Panels umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-146">Opening a panel this way directs focus to the contents of the panel.</span></span>  <span data-ttu-id="b4faa-147">Im Fall des **Elements** -Panels wird der Fokus in die **DOM-Struktur**verschoben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-147">In the case of the **Elements** panel, focus moves into the **DOM Tree**.</span></span>  

## <span data-ttu-id="b4faa-148">Element Panel</span><span class="sxs-lookup"><span data-stu-id="b4faa-148">Elements panel</span></span>   

### <span data-ttu-id="b4faa-149">Überprüfen eines Elements auf der Seite</span><span class="sxs-lookup"><span data-stu-id="b4faa-149">Inspect an element on the page</span></span>   

1.  <span data-ttu-id="b4faa-150">Navigieren Sie mit dem Cursor in der Sprachausgabe zu dem Element, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="b4faa-150">Navigate to the element you want to inspect using the cursor in the screen reader.</span></span>  
1.  <span data-ttu-id="b4faa-151">Simulieren Sie mit der rechten Maustaste auf das Element, um das Kontextmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-151">Simulate a right-mouse click on the element to open the context menu.</span></span>  
1.  <span data-ttu-id="b4faa-152">Wählen Sie die Option über **prüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="b4faa-152">Choose the **Inspect** option.</span></span>  <span data-ttu-id="b4faa-153">Dadurch wird das Panel **Elemente** geöffnet, und das Element wird in der **DOM-Struktur**fokussiert.</span><span class="sxs-lookup"><span data-stu-id="b4faa-153">This opens the **Elements** panel and focuses the element in the **DOM Tree**.</span></span>  

<!--todo:  add dom nodes (elements pane) section when available  -->  

<span data-ttu-id="b4faa-154">Die **DOM-Struktur** wird als [Aria `tree` ][W3CWaiAriaTree]angelegt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-154">The **DOM Tree** is laid out as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### <span data-ttu-id="b4faa-155">Kopieren des Codes für ein Element in der DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4faa-155">Copy the code for an element in the DOM Tree</span></span>   

1.  <span data-ttu-id="b4faa-156">Wenn der Fokus auf einem Knoten in der **DOM-Struktur**liegt, öffnen Sie das Kontextmenü mit der rechten Maustaste.</span><span class="sxs-lookup"><span data-stu-id="b4faa-156">With focus on a node in the **DOM Tree**, bring up the right-click context menu.</span></span>  
1.  <span data-ttu-id="b4faa-157">Erweitern Sie die Option **Kopieren** .</span><span class="sxs-lookup"><span data-stu-id="b4faa-157">Expand the **Copy** option.</span></span>  
1.  <span data-ttu-id="b4faa-158">Wählen Sie **outerHTML kopieren**aus.</span><span class="sxs-lookup"><span data-stu-id="b4faa-158">Select **Copy outerHTML**.</span></span>  

#### <span data-ttu-id="b4faa-159">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-159">Known issues</span></span>   

*   <span data-ttu-id="b4faa-160">Beim **Kopieren von outerHTML** wird häufig nicht der aktuelle Knoten, sondern stattdessen der übergeordnete Knoten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-160">**Copy outerHTML** often does not select the current node but instead selects the parent node.</span></span>  <span data-ttu-id="b4faa-161">Der Inhalt des Elements sollte sich jedoch weiterhin im kopierten outerHTML befinden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-161">However, the contents of the element should still be in the copied outerHTML.</span></span>  

### <span data-ttu-id="b4faa-162">Ändern der Attribute eines Elements in der DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4faa-162">Modify the attributes of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="b4faa-163">Drücken Sie den Fokus auf einen Knoten in der **DOM-Struktur**, `Enter` um ihn bearbeitbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-163">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="b4faa-164">Drücken Sie `Tab` , um zwischen den Attributwerten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b4faa-164">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="b4faa-165">Wenn Sie "Leerzeichen" hören, befinden Sie sich innerhalb einer leeren Texteingabe und können einen neuen Attributwert eingeben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-165">When you hear "space" you are inside of an empty text input and are able to type a new attribute value.</span></span>  
*   <span data-ttu-id="b4faa-166">Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderung zu übernehmen und den gesamten Inhalt des Elements zu hören.</span><span class="sxs-lookup"><span data-stu-id="b4faa-166">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change and hear the entire contents of the element.</span></span>  

#### <span data-ttu-id="b4faa-167">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-167">Known issues</span></span>   

*   <span data-ttu-id="b4faa-168">Wenn Sie in die Texteingabe eintippen, erhalten Sie keine Rückmeldungen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-168">When you type into the text input you get no feedback.</span></span>  <span data-ttu-id="b4faa-169">Wenn Sie einen Tippfehler machen und die Pfeiltasten verwenden, um Ihre Eingaben zu erforschen, erhalten Sie auch kein Feedback.</span><span class="sxs-lookup"><span data-stu-id="b4faa-169">If you make a typo and use the arrow keys to explore your input you also get no feedback.</span></span>  <span data-ttu-id="b4faa-170">Die einfachste Möglichkeit, ihre Arbeit zu überprüfen, besteht darin, die Änderung zu übernehmen und dann zu hören, dass das gesamte Element angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4faa-170">The easiest way to check your work is to accept the change, then listen for the entire element to be announced.</span></span>  

### <span data-ttu-id="b4faa-171">Bearbeiten des HTML-Code eines Elements in der DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4faa-171">Edit the HTML of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="b4faa-172">Drücken Sie den Fokus auf einen Knoten in der **DOM-Struktur**, `Enter` um ihn bearbeitbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-172">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="b4faa-173">Drücken Sie `Tab` , um zwischen den Attributwerten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b4faa-173">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="b4faa-174">Wenn Sie den Namen des Elements hören, beispielsweise "H2", befinden Sie sich innerhalb einer Texteingabe und können den Typ des Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="b4faa-174">When you hear the name of the element, for instance, "h2", you are inside of a text input and may change the type of the element.</span></span>  
*   <span data-ttu-id="b4faa-175">Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-175">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change.</span></span>  

<span data-ttu-id="b4faa-176">Wenn Sie beispielsweise `h3` `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \) eingeben und drücken, werden die Start-und Endtags des Elements in geändert `h3` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-176">For example, typing `h3` and pressing `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) changes the start and end tags of the element to `h3`.</span></span>  

## <span data-ttu-id="b4faa-177">Registerkarten des Elements-Panels</span><span class="sxs-lookup"><span data-stu-id="b4faa-177">Elements panel tabs</span></span>   

<span data-ttu-id="b4faa-178">Der Bereich "Elemente" enthält zusätzliche Registerkarten zum Überprüfen von **Elementen** wie dem auf ein Element angewendeten CSS oder der entsprechenden Stelle in der Barrierefreiheits Struktur.</span><span class="sxs-lookup"><span data-stu-id="b4faa-178">The **Elements** panel contains additional tabs for inspecting things like the CSS applied to an element or the relevant place in the accessibility tree.</span></span>  

*   <span data-ttu-id="b4faa-179">Wenn Sie den Fokus auf einen Knoten in der **DOM-Struktur**legen, drücken `Tab` Sie, bis Sie hören, dass der Bereich **Formatvorlagen** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b4faa-179">With focus on a node in the **DOM Tree**, press `Tab` until you hear that the **Styles** pane is selected.</span></span>  
*   <span data-ttu-id="b4faa-180">Verwenden Sie die `Right Arrow` , um andere verfügbare Registerkarten zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-180">Use the `Right Arrow` to explore other available tabs.</span></span>  

<span data-ttu-id="b4faa-181">Die **DOM-Struktur** wandelt Elemente mit `href` Attributen in fokussierbare Links um, sodass Sie möglicherweise mehrmals drücken müssen, `Tab` um den Bereich " **Formatvorlagen** " zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-181">The **DOM Tree** turns elements with `href` attributes into focusable links, so you may need to press `Tab` more than once to reach the **Styles** pane.</span></span>  

### <span data-ttu-id="b4faa-182">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-182">Known issues</span></span>   

<span data-ttu-id="b4faa-183">Auf die Registerkarten " **DOM-Haltepunkte** " und " **Eigenschaften** " kann nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-183">The **DOM Breakpoints** and **Properties** tabs are not keyboard accessible.</span></span>  

### <span data-ttu-id="b4faa-184">Bereich ' Formatvorlagen '</span><span class="sxs-lookup"><span data-stu-id="b4faa-184">Styles pane</span></span>   

<span data-ttu-id="b4faa-185">Suchen Sie im Bereich **Formatvorlagen** nach Steuerelementen zum Filtern von Formatvorlagen, Umschalten von Element Zuständen \ (wie [`:active`][MDNActive] und [`:focus`][MDNFocus] \), Umschalten von Klassen und Hinzufügen neuer Klassen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-185">In the **Styles** pane find controls for filtering styles, toggling element states \(such as [`:active`][MDNActive] and [`:focus`][MDNFocus]\), toggling classes, and adding new classes.</span></span>  <span data-ttu-id="b4faa-186">Darüber hinaus gibt es ein leistungsfähiges Tool zum Überprüfen von Stilen zum untersuchen und Ändern von Formatvorlagen, die derzeit auf das Element angewendet werden, das sich in der **DOM-Struktur**befindet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-186">There is also a powerful style inspection tool to explore and modify styles currently applied to the element that is in focus in the **DOM Tree**.</span></span>  

<span data-ttu-id="b4faa-187">Das grundlegende Konzept für den Bereich " **Formatvorlagen** " ist, dass nur die Formatvorlagen für den aktuell ausgewählten Knoten in der **DOM-Struktur**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-187">The key concept to understand about the **Styles** pane is that it only shows styles for the currently-selected node in the **DOM Tree**.</span></span>  <span data-ttu-id="b4faa-188">Nehmen wir beispielsweise an, dass Sie die Formatvorlagen eines `<header>` Knotens überprüft haben und nun die Formatvorlagen für einen Knoten sehen möchten `<footer>` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-188">For example, suppose you are done inspecting the styles of a `<header>` node, and now you want to look at the styles for a `<footer>` node.</span></span>  <span data-ttu-id="b4faa-189">Dazu müssen Sie zuerst den `<footer>` Knoten in der **DOM-Struktur**auswählen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-189">To do that, you first need to select the `<footer>` node in the **DOM Tree**.</span></span>  <span data-ttu-id="b4faa-190">Möglicherweise finden Sie es schneller, wenn Sie den Workflow über [prüfen](#inspect-an-element-on-the-page) verwenden, um einen Knoten zu inspizieren, der sich in der allgemeinen Nähe des `footer` Knotens befindet \ (beispielsweise ein Link in der Fußzeile \), der die **DOM-Struktur**fokussiert, und dann mit der Tastatur zu dem exakten Knoten navigieren, an dem Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="b4faa-190">You may find it faster to use the [Inspect](#inspect-an-element-on-the-page) workflow to inspect a node that is in the general vicinity of the `footer` node \(such as a link within the footer\), which focuses the **DOM Tree**, and then use your keyboard to navigate to the exact node in which you are interested.</span></span>  

#### <span data-ttu-id="b4faa-191">Navigieren im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="b4faa-191">Navigate the Styles pane</span></span>   

<span data-ttu-id="b4faa-192">Da alle Formatvorlagen Tools auf die eine oder andere Weise wieder mit dem Bereich " **Formatvorlagen** " verbunden sind, ist es sinnvoll, dieses Tool zuerst zu beherrschen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-192">Because all of the style tools connect in one way or another back to the **Styles** pane, it makes sense to master this tool first.</span></span>  

*   <span data-ttu-id="b4faa-193">Drücken Sie den Fokus im Bereich " **Formatvorlagen** ", `Tab` um den Fokus zu verschieben und den Inhalt zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-193">With focus on the **Styles** pane, press `Tab` to move focus inside and explore the contents.</span></span>  
*   <span data-ttu-id="b4faa-194">Drücken Sie `Tab` , bis die erste Formatvorlage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b4faa-194">Press `Tab` until the first style becomes active.</span></span>  <span data-ttu-id="b4faa-195">Wenn Sie eine Sprachausgabe verwenden, wird diese erste Formatvorlage als "Element. Style {} " angekündigt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-195">If you are using a screen reader this first style is announced as "element.style {}".</span></span>  
*   <span data-ttu-id="b4faa-196">Drücken Sie `Down Arrow` , um in der Liste der Formatvorlagen in der Reihenfolge der Spezifität zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-196">Press `Down Arrow` to navigate the list of styles in order of specificity.</span></span>  <span data-ttu-id="b4faa-197">Eine Sprachausgabe kündigt jede Formatvorlage an, beginnend mit dem Namen der CSS-Datei, der Liniennummer, auf der die Formatvorlage angezeigt wird, und dem Namen der Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="b4faa-197">A screen reader announces each style starting with the name of the CSS file, the line number on which the style appears, and the name of the style.</span></span>  <span data-ttu-id="b4faa-198">Beispiel: "Main. CSS: 233. card__img {} "</span><span class="sxs-lookup"><span data-stu-id="b4faa-198">For example: "main.css:233 .card__img {}"</span></span>  
*   <span data-ttu-id="b4faa-199">Drücken Sie `Enter` , um eine Formatvorlage detaillierter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-199">Press `Enter` to inspect a style in more detail.</span></span>  <span data-ttu-id="b4faa-200">Der Fokus beginnt mit einer bearbeitbaren Version des Formatvorlagen namens.</span><span class="sxs-lookup"><span data-stu-id="b4faa-200">Focus begins on an editable version of the style name.</span></span>  
*   <span data-ttu-id="b4faa-201">Drücken Sie `Tab` , um zwischen bearbeitbaren Versionen jeder CSS-Eigenschaft und den entsprechenden Werten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b4faa-201">Press `Tab` to move between editable versions of each CSS property and their corresponding values.</span></span>  <span data-ttu-id="b4faa-202">Am Ende jedes Formatvorlagen Blocks befindet sich ein leeres bearbeitbares Textfeld, das Sie zum Hinzufügen weiterer CSS-Eigenschaften verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b4faa-202">At the end of each style block is a blank editable text field which you may use to add additional CSS properties.</span></span>  
*   <span data-ttu-id="b4faa-203">Sie können weiterhin drücken, `Tab` um die Liste der Formatvorlagen zu durchlaufen, oder drücken Sie, `Escape` um diesen Modus zu verlassen, und kehren Sie zur Navigation durch die Pfeiltasten zurück.</span><span class="sxs-lookup"><span data-stu-id="b4faa-203">You may continue to press `Tab` to move through the list of styles, or press `Escape` to exit this mode and go back to navigating by arrow keys.</span></span>  

<span data-ttu-id="b4faa-204">Achten Sie darauf, dass Sie über die [Formatvorlagenbereich-Tastatur Referenz] [DevtoolsShortcutsStylesPaneKeyboard] Weitere Tastenkombinationen lesen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-204">Be sure to read through the [Styles pane keyboard reference][DevtoolsShortcutsStylesPaneKeyboard] for additional shortcuts.</span></span>  

##### <span data-ttu-id="b4faa-205">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-205">Known Issues</span></span>   

*   <span data-ttu-id="b4faa-206">Wenn Sie das Feld bearbeitbares Textfeld **Filtern** verwenden, können Sie nicht mehr in der Liste der Formatvorlagen navigieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-206">If you use the **Filter** editable text field, you are no longer be able to navigate the list of styles.</span></span>  

#### <span data-ttu-id="b4faa-207">Elementzustand umschalten</span><span class="sxs-lookup"><span data-stu-id="b4faa-207">Toggle element state</span></span>   

<span data-ttu-id="b4faa-208">Zum Umschalten des Zustands eines Elements, beispielsweise `:active` oder `:focus` :</span><span class="sxs-lookup"><span data-stu-id="b4faa-208">To toggle the state of an element, such as `:active` or `:focus`:</span></span>  

1.  <span data-ttu-id="b4faa-209">Navigieren Sie zum Bereich **Formatvorlagen** , und drücken Sie, `Tab` bis die Schaltfläche **Element Zustand umschalten** den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="b4faa-209">Navigate to the **Styles** pane and press `Tab` until the **Toggle Element State** button has focus.</span></span>  
1.  <span data-ttu-id="b4faa-210">Drücken Sie `Enter` , um die Sammlung von Element Zuständen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b4faa-210">Press `Enter` to expand the collection of element states.</span></span>  <span data-ttu-id="b4faa-211">Die Elementzustände werden als Gruppe von Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-211">The element states are presented as a group of checkboxes.</span></span>  
1.  <span data-ttu-id="b4faa-212">Drücken Sie, `Tab` bis der erste Zustand, den `:active` Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="b4faa-212">Press `Tab` until the first state, `:active`, has focus.</span></span>  
1.  <span data-ttu-id="b4faa-213">Drücken Sie `Space` , um Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-213">Press `Space` to enable it.</span></span>  <span data-ttu-id="b4faa-214">Wenn das aktuell ausgewählte Element in der DOM-Struktur eine `:active` Formatvorlage aufweist, wird es nun angewendet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-214">If the currently-selected element in the DOM Tree has an `:active` style, it is now applied.</span></span>  
1.  <span data-ttu-id="b4faa-215">Drücken `Tab` Sie weiter, um alle verfügbaren Status zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-215">Continue pressing `Tab` to explore all of the available states.</span></span>  

#### <span data-ttu-id="b4faa-216">Hinzufügen einer vorhandenen Klasse</span><span class="sxs-lookup"><span data-stu-id="b4faa-216">Add an existing class</span></span>   

<span data-ttu-id="b4faa-217">Neben der Schaltfläche " **Elementzustand umschalten** " befindet sich die Schaltfläche " **Elementklassen** ".</span><span class="sxs-lookup"><span data-stu-id="b4faa-217">Adjacent to the **Toggle Element State** button is the **Element Classes** button.</span></span>  <span data-ttu-id="b4faa-218">Verschieben Sie den Fokus darauf, indem Sie `Tab` dann drücken `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-218">Move focus to it by pressing `Tab` then `Enter`.</span></span>  <span data-ttu-id="b4faa-219">Der Fokus wird in ein Textfeld "Bearbeiten" mit der Bezeichnung " **neue Klasse hinzufügen**" verschoben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-219">Focus moves into an edit text field labeled **Add New Class**.</span></span>  

<span data-ttu-id="b4faa-220">Die Schaltfläche **Elementklassen** wird in erster Linie zum Hinzufügen vorhandener Klassen zu einem Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-220">The **Element Classes** button is primarily used for adding existing classes to an element.</span></span>  <span data-ttu-id="b4faa-221">Wenn Ihr Stylesheet beispielsweise eine Hilfsklasse mit dem Namen enthalten hat, `.clearfix` können Sie `.` in das Feld "Textfeld bearbeiten" drücken, um eine Vorschlagsliste mit Kursen anzuzeigen, und verwenden Sie die `Down Arrow` , um den Vorschlag zu finden `.clearfix` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-221">For example, if your stylesheet contained a helper class named `.clearfix` you may press `.` inside of the edit text field to see a suggestion list of classes and use the `Down Arrow` to find the `.clearfix` suggestion.</span></span>  <span data-ttu-id="b4faa-222">Oder geben Sie den Kursnamen selbst ein, und drücken Sie `Enter` ihn, um ihn anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-222">Or type the class name out yourself and press `Enter` to apply it.</span></span>  

#### <span data-ttu-id="b4faa-223">Hinzufügen einer neuen Stilregel</span><span class="sxs-lookup"><span data-stu-id="b4faa-223">Add a new style rule</span></span>   

<span data-ttu-id="b4faa-224">Neben der Schaltfläche **Element Klassen** befindet sich die Schaltfläche **neue Stilregel** .</span><span class="sxs-lookup"><span data-stu-id="b4faa-224">Adjacent to the **Element Classes** button is the **New Style Rule** button.</span></span>  <span data-ttu-id="b4faa-225">Verschieben Sie den Fokus, indem Sie die Taste drücken `Tab` und drücken `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-225">Move focus to it by pressing `Tab` and press `Enter`.</span></span>  <span data-ttu-id="b4faa-226">Der Fokus wird in ein bearbeitbares Textfeld innerhalb des Formatvorlagen Inspektors verschoben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-226">Focus moves into an editable text field inside of the style inspector.</span></span>  <span data-ttu-id="b4faa-227">Der anfängliche Textinhalt des Felds ist der Tagnamen des Elements, das in der **DOM-Struktur**ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b4faa-227">The initial text content of the field is the tag name of the element that is selected in the **DOM Tree**.</span></span>  
<span data-ttu-id="b4faa-228">Sie können einen beliebigen Kursnamen in dieses Feld eingeben und dann `Tab` zum Zuweisen von CSS-Eigenschaften drücken.</span><span class="sxs-lookup"><span data-stu-id="b4faa-228">You may type any class name you want into this field and then press `Tab` to assign CSS properties to it.</span></span>  

### <span data-ttu-id="b4faa-229">Registerkarte "berechnet"</span><span class="sxs-lookup"><span data-stu-id="b4faa-229">Computed tab</span></span>   

<span data-ttu-id="b4faa-230">Drücken Sie auf der Registerkarte **berechnet** den Fokus, `Tab` um den Fokus zu verschieben und den Inhalt zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-230">With focus on the **Computed** tab, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="b4faa-231">Auf der Registerkarte " **berechnet** " gibt es Steuerelemente, mit denen Sie untersuchen können, welche CSS-Eigenschaften tatsächlich auf ein Element in der Reihenfolge der Spezifität angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-231">Within the **Computed** tab there are controls for exploring which CSS properties are actually applied to an element in order of specificity.</span></span>  

<!--todo: add computed tab section when available  -->  

#### <span data-ttu-id="b4faa-232">Erkunden aller berechneten Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="b4faa-232">Explore all computed styles</span></span>   

<span data-ttu-id="b4faa-233">Drücken `Tab` Sie, bis Sie die Sammlung berechneter Formatvorlagen erreichen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-233">Press `Tab` until you reach the collection of computed styles.</span></span>  <span data-ttu-id="b4faa-234">Diese werden als [Aria `tree` ][W3CWaiAriaTree]dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-234">These are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="b4faa-235">Durch das Erweitern einer ListBox wird aufgezeigt, welche CSS-Auswahlen die berechnete Formatvorlage anwenden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-235">Expanding a listbox reveals which CSS selectors are applying the computed style.</span></span>  <span data-ttu-id="b4faa-236">Diese Auswahlen sind nach Spezifität geordnet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-236">These selectors are organized by specificity.</span></span>  <span data-ttu-id="b4faa-237">Eine Sprachausgabe gibt den berechneten Wert bekannt, den die CSS-Auswahl aktuell abgleichen soll, den Dateinamen des Stylesheets, das die Auswahl enthält, und die Nummer der Zeile für die Auswahl.</span><span class="sxs-lookup"><span data-stu-id="b4faa-237">A screen reader announces the computed value, which CSS selector is currently matching, the filename of the stylesheet that contains the selector, and the line number for the selector.</span></span>  

#### <span data-ttu-id="b4faa-238">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-238">Known issues</span></span>   

*   <span data-ttu-id="b4faa-239">Wenn Sie das Textfeld " **Filter** " verwenden, können Sie keine Formatvorlagen mehr überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-239">If you use the **Filter** text field, you are no longer able to inspect styles.</span></span>  

### <span data-ttu-id="b4faa-240">Registerkarte "Ereignis-Listener"</span><span class="sxs-lookup"><span data-stu-id="b4faa-240">Event listeners tab</span></span>   

<span data-ttu-id="b4faa-241">Über die Registerkarte **Ereignislistener** können Sie innerhalb des **Elements** Panels die Ereignis-Listener überprüfen, die auf ein Element angewendet wurden.  Drücken Sie im Bereich **Formatvorlagen** den Fokus, `Right Arrow` um zur Registerkarte **Ereignis Listener** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-241">From within the **Elements** panel you may inspect the event listeners applied to an element using the **Event Listeners** tab.  With focus on the **Styles** pane, press the `Right Arrow` to navigate to the **Event Listeners** tab.</span></span>  

#### <span data-ttu-id="b4faa-242">Untersuchen von Ereignis Listenern</span><span class="sxs-lookup"><span data-stu-id="b4faa-242">Explore event listeners</span></span>   

<span data-ttu-id="b4faa-243">Ereignis-Listener werden als [Aria `tree` ][W3CWaiAriaTree]dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-243">Event listeners are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="b4faa-244">Sie können die Pfeiltasten verwenden, um zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-244">You may use the arrow keys to navigate them.</span></span>  <span data-ttu-id="b4faa-245">Eine Sprachausgabe gibt den Namen des DOM-Objekts bekannt, an das der Ereignis-Listener angefügt ist, sowie den Dateinamen, in dem der Ereignislistener definiert ist, und die Nummer der Zeile.</span><span class="sxs-lookup"><span data-stu-id="b4faa-245">A screen reader announces the name of the DOM object that the event listener is attached to, as well as the file name where the event listener is defined and the line number.</span></span>  

### <span data-ttu-id="b4faa-246">Bereich "Barrierefreiheit"</span><span class="sxs-lookup"><span data-stu-id="b4faa-246">Accessibility pane</span></span>   

<span data-ttu-id="b4faa-247">Wenn Sie den Fokus auf den Bereich **Barrierefreiheit** setzen, drücken Sie, `Tab` um den Fokus in den Inhalt zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b4faa-247">With focus on the **Accessibility** pane, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="b4faa-248">Im Bereich " **Barrierefreiheit** " gibt es Steuerelemente zum Durchsuchen der Barrierefreiheits Struktur, die Aria-Attribute, die auf ein Element angewendet werden, und die berechneten Barrierefreiheitseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4faa-248">Within the **Accessibility** pane there are controls for exploring the accessibility tree, the ARIA attributes applied to an element, and the computed accessibility properties.</span></span>  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### <span data-ttu-id="b4faa-249">Barrierefreiheits Struktur</span><span class="sxs-lookup"><span data-stu-id="b4faa-249">Accessibility Tree</span></span>   

<span data-ttu-id="b4faa-250">Die **Barrierefreiheits Struktur** wird als [Aria `tree` ][W3CWaiAriaTree] dargestellt, wobei jede `treeitem` einem Element im DOM entspricht.</span><span class="sxs-lookup"><span data-stu-id="b4faa-250">The **Accessibility Tree** is presented as an [ARIA `tree`][W3CWaiAriaTree] where each `treeitem` corresponds to an element in the DOM.</span></span>  <span data-ttu-id="b4faa-251">In der Struktur wird die berechnete Rolle für den ausgewählten Knoten angekündigt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-251">The tree announces the computed role for the selected node.</span></span>  <span data-ttu-id="b4faa-252">Generische Elemente wie `div` und `span` werden in der Struktur als "GenericContainer" angekündigt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-252">Generic elements like `div` and `span` are announced as "GenericContainer" in the tree.</span></span>  <span data-ttu-id="b4faa-253">Verwenden Sie die Pfeiltasten, um die Struktur zu durchlaufen und die Beziehungen zwischen übergeordneten und untergeordneten Elemente zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-253">Use the arrow keys to traverse the tree and explore parent-child relationships.</span></span>  

#### <span data-ttu-id="b4faa-254">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-254">Known issues</span></span>   

*   <span data-ttu-id="b4faa-255">Der vom **Barrierefreiheits** Bereich verwendete [Aria `tree` ][W3CWaiAriaTree] -Typ wird in Microsoft Edge für macOS-Sprachausgaben wie VoiceOver möglicherweise nicht ordnungsgemäß verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b4faa-255">The type of [ARIA `tree`][W3CWaiAriaTree] used by the **Accessibility** pane may not be properly exposed in Microsoft Edge for macOS screen readers like VoiceOver.</span></span>  <span data-ttu-id="b4faa-256">Abonnieren Sie [Chromium Issue #868480][ChromiumIssues868480] , um über den Fortschritt in diesem Problem informiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-256">Subscribe to [Chromium issue #868480][ChromiumIssues868480] to be informed about progress on this issue.</span></span>  
*   <span data-ttu-id="b4faa-257">Alle Abschnitte **Aria-Attribute** und **berechnete Eigenschaften** werden als [Aria `tree` ][W3CWaiAriaTree]-Objekte gekennzeichnet, aber derzeit ist keine Fokusverwaltung vorhanden, und die Tastatur ist nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="b4faa-257">Each of the **ARIA Attributes** and **Computed Properties** sections are marked up as an [ARIA `tree`][W3CWaiAriaTree], but each does not currently have focus management and is not keyboard operable.</span></span>  

## <span data-ttu-id="b4faa-258">Überwachungs Panel</span><span class="sxs-lookup"><span data-stu-id="b4faa-258">Audits panel</span></span>   

<span data-ttu-id="b4faa-259">Im Bereich " **Audits** " sollten Sie eine Reihe von Tests für eine Website ausführen, um nach häufigen Problemen im Zusammenhang mit Leistung, Barrierefreiheit, SEO und einer Reihe anderer Kategorien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-259">The **Audits** panel you should run a series of tests against a site to check for common issues related to performance, accessibility, SEO, and a number of other categories.</span></span>  

### <span data-ttu-id="b4faa-260">Konfigurieren und Ausführen einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="b4faa-260">Configure and run an audit</span></span>   

1.  <span data-ttu-id="b4faa-261">Beim ersten Öffnen des **Überwachungs** Panels wird der Fokus auf die Schaltfläche " **Überwachung ausführen** " am Ende des Formulars eingestellt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-261">When the **Audits** panel is first opened, focus is placed on the **Run Audit** button at the end of the form.</span></span>  <span data-ttu-id="b4faa-262">Standardmäßig ist das Formular so konfiguriert, dass Audits für jede Kategorie mithilfe der mobilen Emulation auf einer simulierten 3G-Verbindung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-262">By default the form is configured to run audits for every category using mobile emulation on a simulated 3G connection.</span></span>  
1.  <span data-ttu-id="b4faa-263">Verwenden `Shift` + `Tab` oder zurück navigieren im Durchsuchen-Modus, um die Überwachungseinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b4faa-263">Use `Shift`+`Tab` or navigate back in Browse mode to change the audit settings.</span></span>  
1.  <span data-ttu-id="b4faa-264">Wenn Sie zum Ausführen der Überwachung bereit sind, navigieren Sie zurück zur Schaltfläche **Überwachung ausführen** , und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b4faa-264">When you are ready to run the audit, navigate back to the **Run Audit** button and press `Enter`.</span></span>  
1.  <span data-ttu-id="b4faa-265">Der Fokus wird in ein modales Fenster mit einer Schaltfläche " **Abbrechen** " verschoben, mit der Sie die Überwachung beenden können.</span><span class="sxs-lookup"><span data-stu-id="b4faa-265">Focus moves into a modal window with a **Cancel** button which allows you to exit the audit.</span></span>  <span data-ttu-id="b4faa-266">Sie können eine Reihe von earcons hören, während die Überwachung ausgeführt wird, und die Seite mehrmals aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-266">You may hear a series of earcons as the audit runs and refreshes the page multiple times.</span></span>  

#### <span data-ttu-id="b4faa-267">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4faa-267">Known issues</span></span>   

*   <span data-ttu-id="b4faa-268">Die verschiedenen Abschnitte des Konfigurations Formulars sind derzeit nicht mit einem `fieldset` Element gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-268">The different sections of the configuration form are not currently marked up with a `fieldset` element.</span></span>  <span data-ttu-id="b4faa-269">Es ist möglicherweise einfacher, im Durchsuchen-Modus zu navigieren, um herauszufinden, welche Steuerelemente jedem Abschnitt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4faa-269">It may be easier to navigate them in Browse mode to figure out which controls are associated with each section.</span></span>  
*   <span data-ttu-id="b4faa-270">Wenn die Überwachung nicht mehr ausgeführt wird, gibt es keine earcon-oder Live Region-Ankündigung.</span><span class="sxs-lookup"><span data-stu-id="b4faa-270">There is no earcon or live region announcement when the audit is finished running.</span></span>  <span data-ttu-id="b4faa-271">In der Regel dauert es ungefähr 30 Sekunden, nach denen Sie in der Lage sein sollten, zu den Ergebnissen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b4faa-271">Generally it takes about 30 seconds, after which you should be able to navigate to the results.</span></span>  <span data-ttu-id="b4faa-272">Die Verwendung des Durchsuchen-Modus ist möglicherweise die einfachste Methode, um die Ergebnisse zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-272">Using Browse mode may be the easiest way to reach the results.</span></span>  

### <span data-ttu-id="b4faa-273">Navigieren im Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="b4faa-273">Navigate the audit report</span></span>   

<span data-ttu-id="b4faa-274">Der Überwachungsbericht ist in Abschnitte gegliedert, die den einzelnen Überwachungskategorien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-274">The audit report is organized into sections that correspond with each of the audit categories.</span></span>  <span data-ttu-id="b4faa-275">Der Bericht wird mit einer Liste der Bewertungen für jede Kategorie geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b4faa-275">The report opens with a list of scores for each category.</span></span>  <span data-ttu-id="b4faa-276">Diese Punkte sind auch Links, die verwendet werden können, um die entsprechenden Abschnitte zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="b4faa-276">These scores are also links which are able to be used to skip to the relevant sections.</span></span>  <span data-ttu-id="b4faa-277">In jedem Abschnitt handelt es sich `details` um erweiterbare Elemente, die Informationen zu übergebenen oder fehlgeschlagenen Audits enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4faa-277">Within each section are expandable `details` elements, which contain information relating to passed or failed audits.</span></span>  <span data-ttu-id="b4faa-278">Standardmäßig werden nur fehlerhafte Überwachungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-278">By default, only failing audits are shown.</span></span>  <span data-ttu-id="b4faa-279">Jeder Abschnitt endet mit einem Final `details` -Element, das alle übergebenen Audits enthält.</span><span class="sxs-lookup"><span data-stu-id="b4faa-279">Each section ends with a final `details` element which contains all of the passed audits.</span></span>  

<span data-ttu-id="b4faa-280">Verwenden Sie zum Ausführen einer neuen Überwachung `Shift` + `Tab` den Bericht, und suchen Sie nach der Schaltfläche **Audit durchführen** .</span><span class="sxs-lookup"><span data-stu-id="b4faa-280">To run a new audit, use `Shift`+`Tab` to exit the report and look for the **Perform An Audit** button.</span></span>  

## <span data-ttu-id="b4faa-281">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="b4faa-281">Feedback</span></span>   

*   <span data-ttu-id="b4faa-282">Senden Sie devtools-Fehlerberichte oder Funktionsanforderungen an den [Chromium Issue Tracker][MonorailChromiumIssues].</span><span class="sxs-lookup"><span data-stu-id="b4faa-282">Send DevTools bug reports or feature requests to [Chromium Issue Tracker][MonorailChromiumIssues].</span></span>  
*   <span data-ttu-id="b4faa-283">Senden Sie Feedback zu diesem Dokument an [GitHub][GithubEdgeDeveloperNewIssue].</span><span class="sxs-lookup"><span data-stu-id="b4faa-283">Send any feedback related to this document to [GitHub][GithubEdgeDeveloperNewIssue].</span></span>  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-Menu/Index.MD "Ausführen von Befehlen mit dem Befehlsmenü" Microsoft Edge devtools "  
[DevtoolsConsoleIndex]: .. /Console/Index.MD "Console Overview"  
[DevtoolsCssIndex]: .. /CSS/Index.MD "erste Schritte mit dem anzeigen und Ändern von CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /Open.MD "Microsoft Edge devtools" öffnen  
[DevtoolsShortcuts]: .. /Shortcuts.MD "Microsoft Edge devtools"-Tastenkombinationen  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # Formatvorlagen-Bereich-Tastenkombinationen "Formatvorlagenbereich-Tastenkombinationen – Microsoft Edge devtools-Tastenkombinationen"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problem 868480 – verfügbar machen von Aria-Strukturen als Tabellen unter Mac-Barrierefreiheit"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Neues Problem-MicrosoftDocs/Edge-Developer | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": aktiv | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Fokus | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Probleme – Chrom – Monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (Rolle)-barrierefreie Rich-Internet-Anwendungen (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Struktur (Rolle) – barrierefreie Rich-Internet-Anwendungen (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> <span data-ttu-id="b4faa-297">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4faa-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b4faa-298">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) gefunden und von [Rob Dodson][RobDodson] (Mitwirkender, Google webfundamentals \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4faa-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) and is authored by [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="b4faa-300">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b4faa-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
