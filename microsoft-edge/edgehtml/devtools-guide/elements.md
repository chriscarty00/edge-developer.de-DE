---
description: Verwenden Sie das Panel Elemente, um die HTML-, CSS-, Dom-und Barrierefreiheit Ihrer Seite zu überprüfen.
title: DevTools-Elemente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Elemente, HTML, CSS, Dom-Haltepunkte, Ereignisse, Barrierefreiheit
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233685"
---
# <span data-ttu-id="708ef-104">Elemente</span><span class="sxs-lookup"><span data-stu-id="708ef-104">Elements</span></span>

<span data-ttu-id="708ef-105">Das Panel " **Elemente** " hilft Ihnen dabei, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="708ef-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="708ef-106">[Identifizieren und Bearbeiten von Elementen in der HTML-Struktur](#html-tree-view) der aktuellen Seite</span><span class="sxs-lookup"><span data-stu-id="708ef-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="708ef-107">Über [prüfen und Ändern von CSS](./elements/styles.md) auf der Seite, einschließlich Pseudo Zuständen und Pseudo Elementen</span><span class="sxs-lookup"><span data-stu-id="708ef-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="708ef-108">Grund [Legendes zu den CSS-Layouts und-Stilen](./elements/computed.md) auf der Seite</span><span class="sxs-lookup"><span data-stu-id="708ef-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="708ef-109">[Aufspüren von Rogue-Ereignishandlern](./elements/events.md) , damit Sie diese Debuggen können</span><span class="sxs-lookup"><span data-stu-id="708ef-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="708ef-110">[Festlegen von Debug-Haltepunkten für unerwartete visuelle Änderungen](./elements/dom-breakpoints.md) , um in den Code zu springen, der Sie verursacht</span><span class="sxs-lookup"><span data-stu-id="708ef-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="708ef-111">[Abrufen detaillierter Informationen zu den Schriftarten, die auf der Seite verwendet](./elements/fonts.md) werden, und von der Stelle, von der Sie geladen werden</span><span class="sxs-lookup"><span data-stu-id="708ef-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="708ef-112">[Anzeigen der Seite aus der Sicht einer Bildschirmsprachausgabe](./elements/accessibility.md) , um die Barrierefreiheit zu überprüfen und zu testen</span><span class="sxs-lookup"><span data-stu-id="708ef-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="708ef-113">[Überprüfen einer ausgeführten Unterschiede der CSS-Änderungen](./elements/changes.md) , die Sie beim Debuggen der Benutzeroberfläche Ihrer Seite vornehmen</span><span class="sxs-lookup"><span data-stu-id="708ef-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="708ef-114">HTML-Strukturansicht</span><span class="sxs-lookup"><span data-stu-id="708ef-114">HTML tree view</span></span>

![Das Microsoft Edge devtools-Element Panel](./media/elements.png)

1. <span data-ttu-id="708ef-116">Verwenden Sie das Tool **SELECT Element** ( `Ctrl+B` ), um ein Element in der **HTML-Strukturansicht** zu finden, indem Sie auf der Seite darauf klicken.</span><span class="sxs-lookup"><span data-stu-id="708ef-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="708ef-117">Verwenden Sie das Tool zum **hervorheben von Elementen** ( `Ctrl+Shift+L` ), um ein Element auf der Seite zu finden, indem Sie in der **HTML-Strukturansicht**darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="708ef-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="708ef-118">Öffnen Sie das Tool **Farbauswahl** ( `Ctrl+K` ), um eine Liste der verwendeten Farben auf der aktuellen Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="708ef-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="708ef-119">Wenn Sie auf eine Farbe in der Liste klicken, werden weitere Details angezeigt (Farbton, Sättigung, Helligkeit, Alpha).</span><span class="sxs-lookup"><span data-stu-id="708ef-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="708ef-120">Die *Farbauswahl* wird auch geöffnet, wenn Sie im Bereich **Formatvorlagen** auf das farbige Quadrat neben einem Farbwert klicken, sodass Sie die Farbe eines Seitenelements bearbeiten und sofort die Ergebnisse sehen können.</span><span class="sxs-lookup"><span data-stu-id="708ef-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="708ef-121">Die Schaltfläche **Barrierefreiheits Struktur** ( `Ctrl+Shift+A` ) öffnet den Bereich [Barrierefreiheit](./elements/accessibility.md) , in dem die Struktur der Seite angezeigt wird, wie dies bei einer Hilfstechnologie wie der [Windows-Sprachausgabe](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) Screenreader der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="708ef-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="708ef-122">Sie können auch \*\*\*\* `Ctrl+F` ein Element in der HTML-Strukturansicht suchen, indem Sie nach seinem Tagnamen, Attributen oder Textinhalt suchen.</span><span class="sxs-lookup"><span data-stu-id="708ef-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="708ef-123">Bearbeiten von Elementen</span><span class="sxs-lookup"><span data-stu-id="708ef-123">Editing elements</span></span>

<span data-ttu-id="708ef-124">Sie können ein Element bearbeiten, indem Sie in der HTML-Strukturansicht mit der rechten Maustaste darauf klicken und im Kontextmenü **als HTML bearbeiten** auswählen.</span><span class="sxs-lookup"><span data-stu-id="708ef-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="708ef-125">Das Kontextmenü bietet auch Optionen zum Löschen, Ausschneiden, kopieren, einfügen, Einrichten von CSS-Pseudoklassen (*: aktiv*, *: Fokus*, *: hover*, *: besucht*) und Hinzufügen von Attributen.</span><span class="sxs-lookup"><span data-stu-id="708ef-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="708ef-126">Eine weitere Möglichkeit zum Bearbeiten eines Attributs und/oder des zugehörigen Werts besteht darin, in der HTML-Strukturansicht auf das Attribut zu doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="708ef-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Kontextmenü der HTML-Strukturansicht](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="708ef-128">Das Bearbeiten der HTML-Struktur hat keinen Einfluss auf das zugrunde liegende Quellmarkup.</span><span class="sxs-lookup"><span data-stu-id="708ef-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="708ef-129">Beim Aktualisieren der Seite werden Ihre Änderungen zurückgesetzt und nur das Layout gerendert, das von der Seitenquelle bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="708ef-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="708ef-130">Sie können ihren geänderten HTML-Code in die Zwischenablage **Kopieren** , indem Sie mit der rechten Maustaste auf das gewünschte Element klicken (oder das globale `html` Element, wenn die gesamte Seite angezeigt werden soll), um das Kontextmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="708ef-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="708ef-131">(Optionen für**Ausschneiden** und **Einfügen** sind ebenfalls verfügbar).</span><span class="sxs-lookup"><span data-stu-id="708ef-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="708ef-132">Im Bereich " [Formatvorlagen](./elements/styles.md) " können Sie auch CSS-Pseudo Zustände und Pseudoelemente hinzufügen/löschen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="708ef-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="708ef-133">Tool Bereiche</span><span class="sxs-lookup"><span data-stu-id="708ef-133">Tool Panes</span></span>

<span data-ttu-id="708ef-134">Nachdem Sie ein interessantes Seitenelement ausgewählt haben, können Sie die Toolfenster verwenden, um die unterschiedlichen Formatvorlagen und Barrierefreiheitseigenschaften weiter zu überprüfen, die Ereignislistener anzuzeigen und die Haltepunkte für die DOM-Mutation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="708ef-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Fenster ' Tools ' im Bereich ' Elemente '](./media/elements_toolpanes.png)

1. <span data-ttu-id="708ef-136">[**Formatvorlagen**](./elements/styles.md): aktuell angewendete Formatvorlagen, die nach Stylesheets angeordnet sind</span><span class="sxs-lookup"><span data-stu-id="708ef-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="708ef-137">[**Berechnet**](./elements/computed.md): aktuell angewendete Formatvorlagen, die nach CSS-Attributen strukturiert sind</span><span class="sxs-lookup"><span data-stu-id="708ef-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="708ef-138">[**Ereignisse**](./elements/events.md): Ereignis-Listener, die für das aktuelle Element und übergeordnete Elemente registriert sind</span><span class="sxs-lookup"><span data-stu-id="708ef-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="708ef-139">[**DOM-Haltepunkte**](./elements/dom-breakpoints.md): Dom-mutations Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="708ef-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="708ef-140">[**Schriftarten**](./elements/fonts.md): aktuell angewendete Schriftarten für ein ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="708ef-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="708ef-141">[**Barrierefreiheit**](./elements/accessibility.md): Barrierefreiheitseigenschaften</span><span class="sxs-lookup"><span data-stu-id="708ef-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="708ef-142">[**Änderungen**](./elements/changes.md): während der Diagnosesitzung vorgenommene CSS-Änderungen</span><span class="sxs-lookup"><span data-stu-id="708ef-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="708ef-143">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="708ef-143">Shortcuts</span></span>

| <span data-ttu-id="708ef-144">Aktion</span><span class="sxs-lookup"><span data-stu-id="708ef-144">Action</span></span>               | <span data-ttu-id="708ef-145">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="708ef-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="708ef-146">Element Panel</span><span class="sxs-lookup"><span data-stu-id="708ef-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="708ef-147">Element Hervorhebung</span><span class="sxs-lookup"><span data-stu-id="708ef-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="708ef-148">Element auswählen</span><span class="sxs-lookup"><span data-stu-id="708ef-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="708ef-149">Farbwähler</span><span class="sxs-lookup"><span data-stu-id="708ef-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="708ef-150">Barrierefreiheits Struktur</span><span class="sxs-lookup"><span data-stu-id="708ef-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
