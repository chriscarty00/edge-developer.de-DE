---
description: Eine Übersicht über die Interaktion mit der aktuellen Webseite im Browser mithilfe des Konsolentools
title: Verwenden der Konsole für die Interaktion mit dem DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483478"
---
# <a name="use-the-console-to-interact-with-the-dom"></a><span data-ttu-id="f061f-104">Verwenden der Konsole für die Interaktion mit dem DOM</span><span class="sxs-lookup"><span data-stu-id="f061f-104">Use the Console to interact with the DOM</span></span>

<span data-ttu-id="f061f-105">Das **Konsolentool** ist nicht nur zum Protokollieren von [Informationen][DevtoolsConsoleConsoleLog] oder zum Ausführen [von beliebigem JavaScript .][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="f061f-105">The **Console** tool isn't only for [logging information][DevtoolsConsoleConsoleLog] or to [run arbitrary JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  <span data-ttu-id="f061f-106">Es ist auch eine hervorragende Möglichkeit, mit der Webseite im Browser zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="f061f-106">It also is a great way to interact with the webpage in the browser.</span></span>  <span data-ttu-id="f061f-107">Betrachten Sie es als Skriptumgebungsversion des **Inspect-Tools.**</span><span class="sxs-lookup"><span data-stu-id="f061f-107">Consider it a script-environment version of the **Inspect** tool.</span></span>  

## <a name="read-from-the-dom"></a><span data-ttu-id="f061f-108">Lesen aus dem DOM</span><span class="sxs-lookup"><span data-stu-id="f061f-108">Read from the DOM</span></span>

<span data-ttu-id="f061f-109">Führen Sie die folgenden Aktionen aus, um auf die Kopfzeile der Webseite zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f061f-109">To reference the header of the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-110">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f061f-110">Open the **Console**.</span></span>
    *   <span data-ttu-id="f061f-111">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="f061f-111">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="f061f-112">Geben Sie den folgenden Codeausschnitt in der Konsole ein, oder kopieren Sie ihn, und fügen Sie ihn **ein.**</span><span class="sxs-lookup"><span data-stu-id="f061f-112">Type or copy and paste the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Verwenden Sie document.querySelector, um einen Verweis auf die Kopfzeile in der Konsole zu erhalten." lightbox="../media/console-dom-get-reference.msft.png":::
    <span data-ttu-id="f061f-114">Um einen Verweis auf die Kopfzeile in der Konsole zu erhalten, verwenden Sie</span><span class="sxs-lookup"><span data-stu-id="f061f-114">To get a reference to the header in console, use</span></span> `document.querySelector`  
:::image-end:::  

<span data-ttu-id="f061f-115">Wenn Sie den Mauszeiger über das HTML-Ergebnis auswählen oder bewegen, hebt `Shift` + `Tab` DevTools die Kopfzeile für Sie hervor.</span><span class="sxs-lookup"><span data-stu-id="f061f-115">If you select `Shift`+`Tab` or move your mouse cursor over the HTML result, DevTools highlights the header for you.</span></span>  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools hebt den abschnitt hervor, den Sie in der Konsole auswählen" lightbox="../media/console-dom-highlight-element.msft.png":::
    <span data-ttu-id="f061f-117">DevTools hebt den abschnitt hervor, den Sie in der Konsole **auswählen**</span><span class="sxs-lookup"><span data-stu-id="f061f-117">DevTools highlights the section you choose in the **Console**</span></span>  
:::image-end:::  

## <a name="manipulate-the-dom"></a><span data-ttu-id="f061f-118">Ändern des DOM</span><span class="sxs-lookup"><span data-stu-id="f061f-118">Manipulate the DOM</span></span>

<span data-ttu-id="f061f-119">Sie können auch die Webseite bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f061f-119">You may manipulate the webpage, too.</span></span>  <span data-ttu-id="f061f-120">Wenn Sie beispielsweise Folgendes kopieren und einfügen oder in die **Konsole**eingeben, wird um die Kopfzeile ein grüner Rahmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f061f-120">For example, if you copy and paste or type the following into the **Console**, a green border displays around the header.</span></span>

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Verwenden Sie die Konsole, um einem Element einen Rahmen hinzuzufügen." lightbox="../media/console-dom-add-border.msft.png":::
    <span data-ttu-id="f061f-122">Verwenden Sie die Konsole, um einem Element einen Rahmen **hinzuzufügen.**</span><span class="sxs-lookup"><span data-stu-id="f061f-122">To add a border to an element, use the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-123">Abhängig von der Komplexität der Webseite kann es bedenklich sein, das richtige Element zu finden, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f061f-123">Depending on the complexity of the webpage, It may be daunting to find the right element to manipulate.</span></span>  <span data-ttu-id="f061f-124">Sie können jedoch das **Inspect-Tool** verwenden, um Ihnen zu helfen.</span><span class="sxs-lookup"><span data-stu-id="f061f-124">But you may use the **Inspect** tool to help you.</span></span>  <span data-ttu-id="f061f-125">Sagen Sie, Sie möchten den `Documentation` Teil in der Kopfzeile bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f061f-125">Say you want to manipulate the `Documentation` part in the header.</span></span>

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    <span data-ttu-id="f061f-127">Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen</span><span class="sxs-lookup"><span data-stu-id="f061f-127">Display the element that you inspect on the screen</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-128">Führen Sie die folgenden Aktionen aus, um einen direkten Verweis auf das zu bearbeitende Element zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f061f-128">To get a direct reference to the element to manipulate, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-129">Verwenden Sie das **Inspect-Tool,** um das Element zu wählen.</span><span class="sxs-lookup"><span data-stu-id="f061f-129">Use the **Inspect** tool to choose the element.</span></span>  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Verwenden Sie das Tool Inspector, um ein Element zu wählen." lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        <span data-ttu-id="f061f-131">Verwenden Sie das Tool Inspector, um ein Element **zu** wählen.</span><span class="sxs-lookup"><span data-stu-id="f061f-131">To choose an element, use the **Inspector** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f061f-132">Wählen Sie es aus, und DevTools springt zum **Element-Tool.**</span><span class="sxs-lookup"><span data-stu-id="f061f-132">Choose it and DevTools jumps to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="f061f-133">Wählen Sie `...` das Menü neben dem Element in der DOM-Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="f061f-133">Choose the `...` menu next to the element in the DOM view.</span></span>  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="Das ausgewählte Element wird in der DOM-Struktur des Elements-Tools angezeigt, und wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten." lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        <span data-ttu-id="f061f-135">Das ausgewählte Element wird in der DOM-Struktur des **Elements-Tools** angezeigt, und wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f061f-135">The chosen element displays in the DOM tree of the **Elements** tool, choose the overflow menu to get more features</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f061f-136">Öffnen Sie das Kontextmenü, und wählen Sie `Copy`  >  `Copy JS Path` aus.</span><span class="sxs-lookup"><span data-stu-id="f061f-136">Open the contextual menu and choose `Copy` > `Copy JS Path`.</span></span>  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Kopieren des JavaScript-Pfads aus einem Element in der DOM-Ansicht des Elements-Tools" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        <span data-ttu-id="f061f-138">Kopieren des JavaScript-Pfads aus einem Element in der DOM-Ansicht des **Elements-Tools**</span><span class="sxs-lookup"><span data-stu-id="f061f-138">Copy the JavaScript path from an element in the DOM view of the **Elements** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f061f-139">Wechseln Sie zurück zur **Konsole,** und fügen Sie den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="f061f-139">Go back to the **Console** and paste the command.</span></span>  
    
<span data-ttu-id="f061f-140">Wenn Sie den Text des Links in ändern möchten, fügen Sie dem zuvor `My Playground` `.textContent = "My Playground"` hinzugefügten Befehl hinzu.</span><span class="sxs-lookup"><span data-stu-id="f061f-140">To change the text of the link to `My Playground`, add `.textContent = "My Playground"` to the command you previously pasted.</span></span>  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Ändern des Inhalts eines Elements mithilfe der Konsole" lightbox="../media/console-dom-change-content.msft.png":::
    <span data-ttu-id="f061f-142">Ändern **des** Inhalts eines Elements mithilfe der Konsole</span><span class="sxs-lookup"><span data-stu-id="f061f-142">Use the **Console** to change the content of an element</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-143">Verwenden Sie alle JavaScript-DOM-Manipulationen, die Sie in der Konsole **tun möchten.**</span><span class="sxs-lookup"><span data-stu-id="f061f-143">Use any JavaScript DOM manipulations you want to do in the **Console**.</span></span>  <span data-ttu-id="f061f-144">Um dies einfacher zu machen, bietet **die Konsole** einige Hilfsmethoden.</span><span class="sxs-lookup"><span data-stu-id="f061f-144">To make it more convenient, the **Console** comes with a few helper methods.</span></span>  

## <a name="helpful-console-utility-methods"></a><span data-ttu-id="f061f-145">Hilfreiche Konsolenprogrammmethoden</span><span class="sxs-lookup"><span data-stu-id="f061f-145">Helpful Console utility methods</span></span>  

<span data-ttu-id="f061f-146">Viele Komfortmethoden und Verknüpfungen stehen Ihnen als [Konsolenprogramme zur Verfügung.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="f061f-146">Many convenience methods and shortcuts are available to you as [Console Utilities][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="f061f-147">Einige der Methoden sind unglaublich leistungsfähig und sind Dinge, die Sie wahrscheinlich in der Vergangenheit als eine Reihe von `console.log()` Anweisungen geschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="f061f-147">Some of the methods are incredibly powerful and are things you probably wrote as a series of `console.log()` statements in the past.</span></span>

### <a name="the-power-to-the-"></a><span data-ttu-id="f061f-148">Power to the $</span><span class="sxs-lookup"><span data-stu-id="f061f-148">The power to the $</span></span>

<span data-ttu-id="f061f-149">Der `$` verfügt über spezielle Befugnisse in der **Konsole,** und Sie können sich das von jQuery merken.</span><span class="sxs-lookup"><span data-stu-id="f061f-149">The `$` has special powers in **Console** and you may remember that from jQuery.</span></span>

*   `$_` <span data-ttu-id="f061f-150">speichert das Ergebnis des letzten Befehls.</span><span class="sxs-lookup"><span data-stu-id="f061f-150">stores the result of the last command.</span></span>  <span data-ttu-id="f061f-151">Wenn Sie also eingeben und `2 + 2` auswählen `Enter` und dann `$_` eingeben, zeigt die **Konsole** Sie `4` an.</span><span class="sxs-lookup"><span data-stu-id="f061f-151">So, if you type `2 + 2` and select `Enter`, and then type `$_`, the **Console** displays you `4`.</span></span>
*   `$0` <span data-ttu-id="f061f-152">to `$4` ist ein Stapel der letzten überprüften Elemente ist immer der `$0` neueste.</span><span class="sxs-lookup"><span data-stu-id="f061f-152">to `$4` is a stack of the last inspected elements `$0` is always the newest one.</span></span>  <span data-ttu-id="f061f-153">Daher haben Sie im früheren Beispiel das Element im Tool **"Inspector"** ausgewählt, und geben Sie ein, `$0.textContent = "My Playground"` um denselben Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f061f-153">So in the earlier example, you just chose the element in the **Inspector** tool and type `$0.textContent = "My Playground"` to get the same effect.</span></span>
*   `$x()` <span data-ttu-id="f061f-154">ermöglicht ihnen die Auswahl von DOM-Elementen mithilfe von XPATH.</span><span class="sxs-lookup"><span data-stu-id="f061f-154">allows you to choose DOM elements using XPATH.</span></span>
*   `$()` <span data-ttu-id="f061f-155">und `$$()` sind kürzere Versionen von für und `document.querySelector()` `document.querySelectorAll()` .</span><span class="sxs-lookup"><span data-stu-id="f061f-155">and `$$()` are shorter versions of for `document.querySelector()` and `document.querySelectorAll()`.</span></span>  
    
<span data-ttu-id="f061f-156">Der folgende Codeausschnitt ruft z. B. alle Links auf der Webseite \(wie kurz für \) ab und zeigt die Links als sortierbare Tabelle zum Kopieren und Einfügen an, z. B. in `$$('a')` `document.querySelectorAll('a')` Excel.</span><span class="sxs-lookup"><span data-stu-id="f061f-156">For example, the following code snippet retrieves all the links in the webpage \(as `$$('a')` is short for `document.querySelectorAll('a')`\) and displays the links as a sortable table to copy and paste, for example, into Excel.</span></span>

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Alle Links auf der Webseite erhalten und das Ergebnis als Tabelle anzeigen" lightbox="../media/console-dom-get-all-links.msft.png":::
    <span data-ttu-id="f061f-158">Alle Links auf der Webseite erhalten und das Ergebnis als Tabelle anzeigen</span><span class="sxs-lookup"><span data-stu-id="f061f-158">Get all links in the webpage and display the result as a table</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-159">Wenn Sie die Informationen jedoch nicht anzeigen möchten, sie jedoch als Daten verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f061f-159">However, if you don't want to display the information, but you want to grab it as data.</span></span>  <span data-ttu-id="f061f-160">Die `$$('a')` Verknüpfung stellt die Verankerungslinks und alle Eigenschaften für die einzelnen Verknüpfungen zurVerknüpfung.</span><span class="sxs-lookup"><span data-stu-id="f061f-160">The `$$('a')` shortcut provides the anchor links and all of the properties for each one.</span></span>  <span data-ttu-id="f061f-161">Das Problem ist, dass Sie nur die Links und den zugehörigen Text verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f061f-161">The problem is that you only want the links and the related text.</span></span>  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Die Verknüpfung $$ gibt viel zu viele Informationen zurück." lightbox="../media/console-dom-too-much-link-information.msft.png":::
    <span data-ttu-id="f061f-163">Die `$$` Verknüpfung gibt viel zu viele Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="f061f-163">The `$$` shortcut returns far too much information</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-164">Die `$$` Verknüpfung verfügt über ein interessantes zusätzliches Feature.</span><span class="sxs-lookup"><span data-stu-id="f061f-164">The `$$` shortcut has an interesting extra feature.</span></span>  <span data-ttu-id="f061f-165">Anstatt ein reines Like zurückgibt, erhalten Sie mit der Verknüpfung `NodeList` `document.querySelectorAll()` alle `$$` `Array` Methoden.</span><span class="sxs-lookup"><span data-stu-id="f061f-165">Instead of returning a pure `NodeList` like `document.querySelectorAll()`, the `$$` shortcut gives you all of the `Array` methods.</span></span>  <span data-ttu-id="f061f-166">Verwenden `map()` Sie die Methode, um die Informationen auf das zu reduzieren, was Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="f061f-166">Use `map()` method to reduce the information to what you need.</span></span>  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

<span data-ttu-id="f061f-167">Der Codeausschnitt gibt ein Array aller Links als Objekte mit und `url` Eigenschaften `text` zurück.</span><span class="sxs-lookup"><span data-stu-id="f061f-167">The code snippet returns an Array of all the links as objects with `url` and `text` properties.</span></span>  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Verwenden der Karte auf $$ zum Filtern von Informationen auf das Minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    <span data-ttu-id="f061f-169">Verwenden der Karte `$$` auf, um Informationen auf das Minimum zu filtern</span><span class="sxs-lookup"><span data-stu-id="f061f-169">Use map on `$$` to filter information down to the bare minimum</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-170">Sie sind noch nicht fertig, mehrere Links sind interne Links zur Webseite oder haben leeren Text.</span><span class="sxs-lookup"><span data-stu-id="f061f-170">You aren't done yet, several links are internal links to the webpage or have empty text.</span></span>  <span data-ttu-id="f061f-171">Verwenden Sie die Filtermethode, um die internen Links zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f061f-171">Use the filter method to get rid of the internal links.</span></span>  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Get the links that aren't empty and are external" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    <span data-ttu-id="f061f-173">Get the links that aren't empty and are external</span><span class="sxs-lookup"><span data-stu-id="f061f-173">Get the links that aren't empty and are external</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-174">Wie am Anfang der Webseite angezeigt, können Sie diese Elemente auch ändern.</span><span class="sxs-lookup"><span data-stu-id="f061f-174">As displayed at the start of the webpage, you may also change these elements.</span></span>  <span data-ttu-id="f061f-175">Der folgende Codeausschnitt erstellt beispielsweise einen grünen Rahmen um alle externen Links:</span><span class="sxs-lookup"><span data-stu-id="f061f-175">For example, the following code snippet creates a green border around all external links:</span></span>

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Um alle externen Links zu markieren, fügen Sie jeweils einen grünen Rahmen hinzu" lightbox="../media/console-dom-highlight-links.msft.png":::
    <span data-ttu-id="f061f-177">Um alle externen Links zu markieren, fügen Sie jeweils einen grünen Rahmen hinzu</span><span class="sxs-lookup"><span data-stu-id="f061f-177">To highlight all external links, add a green border around each</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-178">Anstatt komplexes JavaScript zum Filtern von Ergebnissen zu schreiben, verwenden Sie die Leistung von CSS-Selektoren.</span><span class="sxs-lookup"><span data-stu-id="f061f-178">Instead of writing complex JavaScript to filter results, use the power of CSS selectors.</span></span>  

<span data-ttu-id="f061f-179">Führen Sie die folgenden Aktionen aus, um eine Tabelle mit den Und-Informationen für alle Bilder auf der Webseite zu erstellen, die keine `src` `alt` Inlinebilder sind.</span><span class="sxs-lookup"><span data-stu-id="f061f-179">To create a table of the `src` and `alt` information for all images on the webpage that aren't inline images, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-180">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f061f-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="f061f-181">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="f061f-181">Type or copy and paste the following code snippet.</span></span>  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Verwenden Sie zum Auswählen von Elementen einen komplexen CSS-Selektor" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    <span data-ttu-id="f061f-183">Verwenden Sie zum Auswählen von Elementen einen komplexen CSS-Selektor</span><span class="sxs-lookup"><span data-stu-id="f061f-183">To choose elements, use a complex CSS selector</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-184">Bereit für ein noch komplexeres Beispiel?</span><span class="sxs-lookup"><span data-stu-id="f061f-184">Ready for an even more complex example?</span></span>  <span data-ttu-id="f061f-185">HTML-Webseiten, die aus markdown wie diesem Artikel generiert werden, verfügen über automatische ID-Werte für jede Überschrift, damit Sie einen tiefen Link zu diesem Abschnitt erstellen können.</span><span class="sxs-lookup"><span data-stu-id="f061f-185">HTML webpages generated from markdown like this article, have automatic ID values for each heading to allow you to deep link to that section.</span></span>  <span data-ttu-id="f061f-186">Beispiel: Eine `# New features` Änderung in `<h1 id="new-features">New features</h1>` .</span><span class="sxs-lookup"><span data-stu-id="f061f-186">For example, a `# New features` changes to `<h1 id="new-features">New features</h1>`.</span></span>  

<span data-ttu-id="f061f-187">Führen Sie die folgenden Aktionen aus, um alle automatischen Überschriften auflisten, die kopiert und eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f061f-187">To list of all of the automatic headings to copy and paste, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-188">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f061f-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="f061f-189">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="f061f-189">Type or copy and paste the following code snippet.</span></span>  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

<span data-ttu-id="f061f-190">Das Ergebnis ist Text, der Inhalt für jede Überschrift enthält, gefolgt von der vollständigen URL, die darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="f061f-190">The result is text that contains content for each heading followed by the full URL that points to it.</span></span>  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Alle Überschriften und generierten URLs von der Webseite erhalten" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    <span data-ttu-id="f061f-192">Alle Überschriften und generierten URLs von der Webseite erhalten</span><span class="sxs-lookup"><span data-stu-id="f061f-192">Get all the headings and the generated URLs from the webpage</span></span>  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a><span data-ttu-id="f061f-193">Bereinigen mit Clear und Copy</span><span class="sxs-lookup"><span data-stu-id="f061f-193">Clean up with clear and copy</span></span>

<span data-ttu-id="f061f-194">Bei der Entwicklung in der **Konsole**wird es möglicherweise unordentlich.</span><span class="sxs-lookup"><span data-stu-id="f061f-194">When developing in the **Console**, things may get messy.</span></span>  <span data-ttu-id="f061f-195">Es kann frustrierend sein, beim Kopieren und Einfügen zu versuchen, Ergebnisse zu wählen.</span><span class="sxs-lookup"><span data-stu-id="f061f-195">You may find it frustrating to try to choose results while you copy and paste.</span></span>  <span data-ttu-id="f061f-196">Die folgenden beiden Hilfsmethoden helfen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="f061f-196">The following two utility methods help you.</span></span>  

*   `copy()` <span data-ttu-id="f061f-197">kopiert alles, was Sie der Zwischenablage geben.</span><span class="sxs-lookup"><span data-stu-id="f061f-197">copies whatever you give it to the clipboard.</span></span>  <span data-ttu-id="f061f-198">Die Methode ist besonders nützlich, wenn Sie sie mit der Kopie des `copy()` `$_` letzten Ergebnisses kombinieren.</span><span class="sxs-lookup"><span data-stu-id="f061f-198">The `copy()` method is especially useful when you mix it with `$_` that copies the last result.</span></span>
*   `clear()` <span data-ttu-id="f061f-199">Die Konsole **wird geräumt.**</span><span class="sxs-lookup"><span data-stu-id="f061f-199">clears the **Console**.</span></span>

### <a name="read-and-monitor-events"></a><span data-ttu-id="f061f-200">Lesen und Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f061f-200">Read and monitor events</span></span>

<span data-ttu-id="f061f-201">Zwei weitere interessante Hilfsmethoden von **Console beschäftigen** sich mit der Ereignisbehandlung.</span><span class="sxs-lookup"><span data-stu-id="f061f-201">Two other interesting utility methods of **Console** deal with event handling.</span></span>

*   `getEventListeners(node)` <span data-ttu-id="f061f-202">listet alle Ereignislistener eines Knotens auf.</span><span class="sxs-lookup"><span data-stu-id="f061f-202">lists all the event listeners of a node.</span></span>
*   `monitorEvents(node, events)` <span data-ttu-id="f061f-203">überwacht und protokolliert die Ereignisse, die auf einem Knoten auftreten.</span><span class="sxs-lookup"><span data-stu-id="f061f-203">monitors and logs the events that happen on a node.</span></span>

<span data-ttu-id="f061f-204">Führen Sie die folgenden Aktionen aus, um den gesamten Ereignislistener auflisten, der dem ersten Formular auf der Webseite zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f061f-204">To list all of the event listener assigned to the first form in the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-205">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f061f-205">Open the **Console**.</span></span>  
1.  <span data-ttu-id="f061f-206">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="f061f-206">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Alle Ereignislistener für das erste Formular auf der Webseite erhalten" lightbox="../media/console-dom-get-form-events.msft.png":::
    <span data-ttu-id="f061f-208">Alle Ereignislistener für das erste Formular auf der Webseite erhalten</span><span class="sxs-lookup"><span data-stu-id="f061f-208">Get all events listeners for the first form in the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-209">Wenn Sie überwachen, erhalten Sie \*\*\*\* immer dann eine Benachrichtigung in der Konsole, wenn sich etwas an den angegebenen Elementen ändert.</span><span class="sxs-lookup"><span data-stu-id="f061f-209">When you monitor, you to get a notification in the **Console** every time something changes to the specified elements.</span></span>  <span data-ttu-id="f061f-210">Sie definieren die Ereignisse, die Sie abhören möchten, als zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="f061f-210">You define the events you want to listen to as a second parameter.</span></span>  <span data-ttu-id="f061f-211">Es ist wichtig, dass Sie die Ereignisse definieren, die Sie überwachen möchten, andernfalls wird jedes Ereignis gemeldet, das mit dem Element passiert.</span><span class="sxs-lookup"><span data-stu-id="f061f-211">It is important for you to define the events that you want to monitor, otherwise any event happening to the element is reported.</span></span>

<span data-ttu-id="f061f-212">Führen Sie die \*\*\*\* folgenden Aktionen aus, um bei jedem Bildlauf eine Benachrichtigung in der Konsole zu erhalten, die Größe des Fensters zu ändern oder wenn der Benutzer das Suchformular einr nen soll.</span><span class="sxs-lookup"><span data-stu-id="f061f-212">To get a notification in the **Console** every time you scroll, resize the window, or when the user types in the search form, complete the following actions.</span></span>  

1.  <span data-ttu-id="f061f-213">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f061f-213">Open the **Console**.</span></span>  
1.  <span data-ttu-id="f061f-214">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="f061f-214">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Konsole zeigt jedes Bildlaufereignis an, das im Fenster passiert" lightbox="../media/console-dom-monitor-events.msft.png":::
    <span data-ttu-id="f061f-216">**Konsole** zeigt jedes Bildlaufereignis an, das im Fenster passiert</span><span class="sxs-lookup"><span data-stu-id="f061f-216">**Console** displays every scroll event that happens on the Window</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-217">Um eine Beliebige Tastenaktion für das aktuell ausgewählte Element zu protokollieren, konzentrieren Sie sich auf das Suchformular in der Kopfzeile, und wählen Sie einige Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="f061f-217">To log any key action on the currently chosen element, focus on the search form in the header and select some keys.</span></span>  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Konsole zeigt Keyupereignisse an, die im Formular auftreten" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    <span data-ttu-id="f061f-219">**Konsole** zeigt `keyup` Ereignisse an, die im Formular auftreten</span><span class="sxs-lookup"><span data-stu-id="f061f-219">**Console** displays `keyup` events that happen on the form</span></span>  
:::image-end:::  

<span data-ttu-id="f061f-220">Entfernen Sie die überwachung, die Sie mithilfe des folgenden Codeausschnitts festgelegt haben, um sie zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f061f-220">To stop it, remove the monitoring you set using the following code snippet.</span></span>  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a><span data-ttu-id="f061f-221">Wiederverwendung von DOM-Manipulationsskripts</span><span class="sxs-lookup"><span data-stu-id="f061f-221">Reuse DOM manipulation scripts</span></span>

<span data-ttu-id="f061f-222">Möglicherweise ist es hilfreich, das DOM über die Konsole zu **bearbeiten.**</span><span class="sxs-lookup"><span data-stu-id="f061f-222">You may find it useful to manipulate the DOM from the **Console**.</span></span>  <span data-ttu-id="f061f-223">Möglicherweise stoßen Sie bald auf die Einschränkungen der **Konsole** als Entwicklungsplattform.</span><span class="sxs-lookup"><span data-stu-id="f061f-223">You may soon run into the limitations of the **Console** as a development platform.</span></span>  <span data-ttu-id="f061f-224">Die gute Nachricht ist, dass [das Sources-Tool][DevtoolsSourcesIndex] in DevTools eine voll ausgestattete Entwicklungsumgebung bietet.</span><span class="sxs-lookup"><span data-stu-id="f061f-224">The good news is that the [Sources][DevtoolsSourcesIndex] tool in DevTools offers a fully featured development environment.</span></span>  <span data-ttu-id="f061f-225">Im **Tool Quellen** können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f061f-225">In the **Sources** tool, you may complete the following actions.</span></span>  

*   <span data-ttu-id="f061f-226">Store Skripts für die Konsole als [Codeausschnitte .][DevToolsJavascriptSnippets] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f061f-226">Store your scripts for the **Console** as [Snippets][DevToolsJavascriptSnippets].</span></span>  
*   <span data-ttu-id="f061f-227">Führen Sie die Skripts auf einer Webseite mithilfe einer Tastenkombination oder des Editors aus.</span><span class="sxs-lookup"><span data-stu-id="f061f-227">Run the scripts in a webpage using a keyboard shortcut or the editor.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f061f-228">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f061f-228">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Führen Sie Codeausschnitte von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
