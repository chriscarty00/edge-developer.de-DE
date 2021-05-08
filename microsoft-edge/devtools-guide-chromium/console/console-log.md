---
description: Protokollieren von Nachrichten und Ausführen von JavaScript in der Microsoft Edge DevTools Console.
title: Protokollieren von Nachrichten im Konsolentool
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483480"
---
# <a name="log-messages-in-the-console-tool"></a><span data-ttu-id="11a9f-104">Protokollieren von Nachrichten im Konsolentool</span><span class="sxs-lookup"><span data-stu-id="11a9f-104">Log messages in the Console tool</span></span>  

<span data-ttu-id="11a9f-105">Seit browsern entwicklertools angeboten werden, ist **die Konsole** ein Favorit.</span><span class="sxs-lookup"><span data-stu-id="11a9f-105">Ever since browsers started to offer developer tools, the **Console** is a favorite.</span></span>  <span data-ttu-id="11a9f-106">Der Grund ist einfach.</span><span class="sxs-lookup"><span data-stu-id="11a9f-106">The reason is simple.</span></span>  

*   <span data-ttu-id="11a9f-107">In den meisten Programmierkursen lernen Sie, eine Art Druckbefehl auszudrucken, um Einblicke in das Geschehen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="11a9f-107">In most programming courses, you learn to output some kind of print command to gain insights about what happens.</span></span>  

<span data-ttu-id="11a9f-108">Vor den DevTools waren Sie auf eine oder -Anweisung zum `alert()` `document.write()` Debuggen im Browser beschränkt.</span><span class="sxs-lookup"><span data-stu-id="11a9f-108">Before the DevTools, you were limited to an `alert()` or `document.write()` statement to debug in the browser.</span></span>  

<span data-ttu-id="11a9f-109">Wenn Sie Informationen in der Konsole protokollieren **möchten,** stehen Ihnen zahlreiche Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="11a9f-109">If you want to log information in the **Console**, lots of methods are available to you.</span></span>  <span data-ttu-id="11a9f-110">Überprüfen Sie alle verfügbaren Methoden in der [API-Referenz][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="11a9f-110">Review all of available methods in the [API reference][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="11a9f-111">Im folgenden Codeausschnitt werden die wichtigsten Methoden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="11a9f-111">The following code snippet lists the most important methods.</span></span>  

```javascript
// prints the text to the console as  a log message
console.log('This is a log message')
// prints the text to the console as an informational message
console.info('This is some information') 
// prints the text to the console as an error message
console.error('This is an error')
// prints the text to the console as a warning
console.warn('This is a warning') 
```  

<span data-ttu-id="11a9f-112">Kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu Konsolennachrichtenbeispiele: [Protokoll, Informationen, Fehler und Warnen.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]</span><span class="sxs-lookup"><span data-stu-id="11a9f-112">Copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: log, info, error, and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].</span></span>  <span data-ttu-id="11a9f-113">Wenn Sie eine Beliebige Methode in der Konsole **ausprobieren,** scheinen die und -Methoden dasselbe zu tun, während die und-Methoden ein Symbol neben der Nachricht und eine Möglichkeit zum Überprüfen der Stapelverfolgung der Nachricht `log()` `info()` `error()` `warn()` anzeigen. [][WikiStackTrace]</span><span class="sxs-lookup"><span data-stu-id="11a9f-113">When you try any method in the **Console**, the `log()` and `info()` methods seem to do the same thing, while the `error()` and `warn()` methods display an icon next to the message and a way to inspect the [stack trace][WikiStackTrace] of the message.</span></span>  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="In der Konsole werden die Nachrichten von verschiedenen Protokoll-APIs angezeigt." lightbox="../media/console-log-examples.msft.png":::
   <span data-ttu-id="11a9f-115">In **der Konsole** werden die Nachrichten von verschiedenen Protokoll-APIs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11a9f-115">The **Console** displays the messages from different log APIs</span></span>  
:::image-end:::  

<span data-ttu-id="11a9f-116">Es ist jedoch weiterhin eine gute Idee, und für verschiedene Protokollaufgaben zu verwenden, da Sie mit dem Typ in der Konsole `info()` `log()` filtern [können.][DevtoolsConsoleConsoleFilters]</span><span class="sxs-lookup"><span data-stu-id="11a9f-116">It is, however, still a good idea to use `info()` and `log()` for different log tasks as that allows you to [filter using type in the Console][DevtoolsConsoleConsoleFilters].</span></span>  

## <a name="different-types-of-logs"></a><span data-ttu-id="11a9f-117">Verschiedene Typen von Protokollen</span><span class="sxs-lookup"><span data-stu-id="11a9f-117">Different types of logs</span></span>  

<span data-ttu-id="11a9f-118">Anstelle von Protokolltext können Sie gültige JavaScript- oder DOM-Verweise an die Konsole **senden.**</span><span class="sxs-lookup"><span data-stu-id="11a9f-118">Instead of log text you may send any valid JavaScript or DOM references to the **Console**.</span></span>  <span data-ttu-id="11a9f-119">Die **Konsole** ist elegant und bestimmt den Typ, den Sie senden.</span><span class="sxs-lookup"><span data-stu-id="11a9f-119">The **Console** is elegant and it determines the type that you send it.</span></span>  <span data-ttu-id="11a9f-120">Anschließend erhalten Sie die bestmögliche Darstellung.</span><span class="sxs-lookup"><span data-stu-id="11a9f-120">It then gives you the best possible representation.</span></span>  <span data-ttu-id="11a9f-121">Kopieren Und fügen Sie den folgenden Codeausschnitt in die **Konsole** ein, oder navigieren Sie zum Anzeigen der Ergebnisse zu [Konsolennachrichtenbeispiele: Protokollieren verschiedener Typen][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span><span class="sxs-lookup"><span data-stu-id="11a9f-121">Copy and paste the following code snippet in the **Console** or to display the results, navigate to [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span></span>  

```javascript
let x = 2;
// logs the value of x
console.log(x);
// logs the name x and value of x
console.log({x})   
// logs a DOM reference  
console.log(document.querySelector('body'));
// logs an Object
console.log({"type":"life", "meaning": 42});
let w3techs = ['HTML', 'CSS', 'SVG', 'MathML'];
// logs an Array
console.log(w3techs);
```  

<span data-ttu-id="11a9f-122">Jedes Ergebnis wird auf andere Weise angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11a9f-122">Each result is displayed in a different way.</span></span>  <span data-ttu-id="11a9f-123">Verwenden Sie die Dreiecke, um die Informationen umschalten und die einzelnen Details genauer analysieren.</span><span class="sxs-lookup"><span data-stu-id="11a9f-123">Use the triangles to toggle the information and analyze each one in more detail.</span></span>  <span data-ttu-id="11a9f-124">Die geschweiften geschweiften Zeichen um die Variable sind ein kleiner Trick, um viele Protokollnachrichten zu vermeiden, bei denen Sie nur einen Wert erhalten, aber nicht wissen, wo sie `{}` `x` ihren Ursprung hat.</span><span class="sxs-lookup"><span data-stu-id="11a9f-124">The curly brace characters `{}` around the `x` variable are a nice little trick to avoid lots of log messages where you only get a value but you don't know where it originated.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Protokollvariablen unterschiedlicher Typen in der Konsole" lightbox="../media/console-log-types.msft.png":::
         <span data-ttu-id="11a9f-126">Protokollvariablen unterschiedlicher Typen in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="11a9f-126">Log variables of different types in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Protokollvariablen unterschiedlicher Typen in der Konsole mit erweiterten zusätzlichen Informationen" lightbox="../media/console-log-types-expanded.msft.png":::
         <span data-ttu-id="11a9f-128">Protokollvariablen unterschiedlicher Typen in der **Konsole** mit erweiterten zusätzlichen Informationen</span><span class="sxs-lookup"><span data-stu-id="11a9f-128">Log variables of different types in the **Console** with expanded extra information</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a><span data-ttu-id="11a9f-129">Formatieren und Konvertieren von Werten mit Specifiern</span><span class="sxs-lookup"><span data-stu-id="11a9f-129">Format and convert values with specifiers</span></span>

<span data-ttu-id="11a9f-130">Ein besonderes Feature aller Protokollmethoden ist, dass Sie Inserenten in Ihrer Protokollnachricht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="11a9f-130">A special feature of all the log methods is that you may use specifiers in your log message.</span></span>  <span data-ttu-id="11a9f-131">Specifiers sind Teil einer Protokollnachricht und beginnen mit einem Prozentzeichen \( \) zeichen und ermöglichen es Ihnen, bestimmte Werte in verschiedenen Formaten zu protokollieren und `%` sogar zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11a9f-131">Specifiers are part of a log message and start with a percentage sign \(`%`\) character and allow you to log certain values in different formats and even convert each.</span></span>  

*   `%s` <span data-ttu-id="11a9f-132">Protokolle als Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="11a9f-132">logs as Strings</span></span>
*   `%i` <span data-ttu-id="11a9f-133">oder `%d` protokolle als Ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="11a9f-133">or `%d` logs as Integers</span></span>
*   `%f` <span data-ttu-id="11a9f-134">Protokolle als Gleitkommawert</span><span class="sxs-lookup"><span data-stu-id="11a9f-134">logs as a floating-point value</span></span>
*   `%o` <span data-ttu-id="11a9f-135">Protokolle als erweiterbares DOM-Element</span><span class="sxs-lookup"><span data-stu-id="11a9f-135">logs as an expandable DOM element</span></span>
*   `%O` <span data-ttu-id="11a9f-136">Protokolle als erweiterbares JavaScript-Objekt</span><span class="sxs-lookup"><span data-stu-id="11a9f-136">logs as an expandable JavaScript object</span></span>
*   `%c` <span data-ttu-id="11a9f-137">ermöglicht es Ihnen, Ihre Nachricht mit CSS zu formatieren</span><span class="sxs-lookup"><span data-stu-id="11a9f-137">allows you to style you message with CSS</span></span>

```javascript
// logs "10x console developer"
console.log('%ix %s developer', 10, 'console');
// logs PI => 3.141592653589793
console.log(Math.PI); 
// logs PI as an integer = 3
console.log('%i', Math.PI); 
// logs the webpage body as a DOM node
console.log('%o', document.body); 
// logs the body of the webpage as a JavaScript object with all properties
console.log('%O', document.body); 
// Displays the message as red and big
console.log('%cImportant message follows','color:red;font-size:40px');
```  

<span data-ttu-id="11a9f-138">Im ersten Beispiel wird angezeigt, dass die Reihenfolge der Ersetzung von Specifiern die Parameterreihenfolge nach der Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="11a9f-138">The first example displays that the order of replacement of specifiers is the parameter order following the string.</span></span>  <span data-ttu-id="11a9f-139">Wenn Sie die Ergebnisse anzeigen möchten, kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu [Konsolennachrichtenbeispiele: Protokollierung mit Specifiern][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span><span class="sxs-lookup"><span data-stu-id="11a9f-139">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span></span>  <span data-ttu-id="11a9f-140">Erweitern Sie die Informationen im Protokoll, um den großen Unterschied zwischen und `%o` zu `%O` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11a9f-140">Expand the information in the log to display the huge difference between `%o` and `%O`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Verwenden von Specifiern zum Protokollieren und Konvertieren von Werten" lightbox="../media/console-log-specifiers.msft.png":::
         <span data-ttu-id="11a9f-142">Verwenden von Specifiern zum Protokollieren und Konvertieren von Werten</span><span class="sxs-lookup"><span data-stu-id="11a9f-142">Use specifiers to log and convert values</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Erweitern der Ergebnisse zeigt den Unterschied zwischen %O an und %o specifier – der Textkörper wird entweder als erweiterbarer DOM-Knoten oder als vollständige Liste aller JavaScript-Eigenschaften auf dem Webseitentext angezeigt." lightbox="../media/console-log-specifiers-expanded.msft.png":::
        <span data-ttu-id="11a9f-144">Erweitern der Ergebnisse zeigt den Unterschied zwischen dem und dem Specifier an – der Textkörper wird entweder als erweiterbarer DOM-Knoten oder als vollständige Liste aller JavaScript-Eigenschaften im Webseitentext `%O` `%o` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11a9f-144">Expand the results displays the difference between the `%O` and `%o` specifier - the body is either displayed as an expandable DOM node or as a full list of all JavaScript properties on the webpage body</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a><span data-ttu-id="11a9f-145">Gruppenprotokollnachrichten</span><span class="sxs-lookup"><span data-stu-id="11a9f-145">Group log messages</span></span>

<span data-ttu-id="11a9f-146">Wenn Sie viele Informationen protokollieren, können Sie die und-Methoden verwenden, um Protokollmeldungen als erweiterbare und einklappbare Gruppen `group` `groupCollapsed` in der Konsole **anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="11a9f-146">If you log much information, you may use the `group` and `groupCollapsed` methods to display log messages as expandable and collapsible groups in the **Console**.</span></span>  <span data-ttu-id="11a9f-147">Gruppen können geschachtelt und benannt werden, um die Daten viel einfacher zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="11a9f-147">Groups may be nested and named to make the data much easier to understand.</span></span>  

```javascript
console.group("Passengers: Heart of Gold");
console.log('Zaphod');
console.log('Trillian');
console.log('Ford');
console.log('Arthur');
console.log('Marvin');
console.groupCollapsed("Hidden");
console.log('(Frankie & Benjy)');
console.groupEnd("Hidden");
console.groupEnd("Passengers: Heart of Gold");

let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
for (tech in technologies) {
  console.groupCollapsed(tech);
  technologies[tech].forEach(t => console.log(t));
  console.groupEnd(tech);
}
```  

<span data-ttu-id="11a9f-148">Auch im zweiten Beispiel können die Gruppennamen optional generiert werden.</span><span class="sxs-lookup"><span data-stu-id="11a9f-148">Also in the second example, the group names may be optionally generated.</span></span>  <span data-ttu-id="11a9f-149">Wenn Sie die Ergebnisse anzeigen möchten, kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu Konsolennachrichtenbeispiele: [Gruppieren von Protokollen][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span><span class="sxs-lookup"><span data-stu-id="11a9f-149">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: grouping logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span></span>  <span data-ttu-id="11a9f-150">Sie können die einzelnen Abschnitte erweitern und reduzieren.</span><span class="sxs-lookup"><span data-stu-id="11a9f-150">You may expand and collapse each of the sections.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Viele Werte als Gruppen protokollieren" lightbox="../media/console-log-groups.msft.png":::
         <span data-ttu-id="11a9f-152">Viele Werte als Gruppen protokollieren</span><span class="sxs-lookup"><span data-stu-id="11a9f-152">Log lots of values as groups</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Jede Gruppe kann erweitert und reduziert werden" lightbox="../media/console-log-groups-expanded.msft.png":::
        <span data-ttu-id="11a9f-154">Jede Gruppe kann erweitert und reduziert werden</span><span class="sxs-lookup"><span data-stu-id="11a9f-154">Each group may be expanded and collapsed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a><span data-ttu-id="11a9f-155">Anzeigen komplexer Daten als Tabellen</span><span class="sxs-lookup"><span data-stu-id="11a9f-155">Display complex data as tables</span></span>  

<span data-ttu-id="11a9f-156">Die Methode protokolliert komplexe Daten nicht als ein zusammenklappbares und erweiterbares Objekt, sondern als Tabelle, die Sie mit `console.table()` unterschiedlichen Kopfzeilen sortieren können.</span><span class="sxs-lookup"><span data-stu-id="11a9f-156">The `console.table()` method logs complex data not as a collapsible and expandable object, but as a table that you may sort using different headers.</span></span>  <span data-ttu-id="11a9f-157">Eine sortierte Tabelle erleichtert es den Personen, die Informationen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="11a9f-157">A sorted table makes it much easier for people to review the information.</span></span>  <span data-ttu-id="11a9f-158">Navigieren Sie zum Anzeigen in einem Beispiel zu [Konsolennachrichtenbeispiele: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span><span class="sxs-lookup"><span data-stu-id="11a9f-158">To display it in an example, navigate to [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span></span>

```javascript
let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
// log technologies as an object
console.log(technologies);
// display technologies as a table
console.table(technologies);

// get the dimensions of the webpage body
let bodyDimensions = document.body.getBoundingClientRect();
// display dimensions as an object
console.log(bodyDimensions);
// display dimensions as a table
console.table(bodyDimensions);
```  

:::image type="complex" source="../media/console-log-table.msft.png" alt-text="Anzeigen von Daten mit console.table, um das Lesen zu vereinfachen" lightbox="../media/console-log-table.msft.png":::
   <span data-ttu-id="11a9f-160">Anzeigen von Daten `console.table` mit, um das Lesen zu vereinfachen</span><span class="sxs-lookup"><span data-stu-id="11a9f-160">Display data with `console.table` to make it much easier to read</span></span>
:::image-end:::  

<span data-ttu-id="11a9f-161">Die Ausgabe von weist nicht nur ein Tabellenformat auf, `console.table` wenn sie in der Konsole angezeigt **wird.**</span><span class="sxs-lookup"><span data-stu-id="11a9f-161">The output of `console.table` has a table format not only when it displays in the **Console**.</span></span>    <span data-ttu-id="11a9f-162">Wenn Sie beispielsweise eine Tabelle kopieren und in Excel, Word oder ein anderes Produkt einfügen, das tabellarische Daten unterstützt, bleibt die Struktur erhalten.</span><span class="sxs-lookup"><span data-stu-id="11a9f-162">For example, if you copy and paste a table into Excel, Word, or any other product that supports tabular data, the structure remains intact.</span></span>  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

<span data-ttu-id="11a9f-163">Wenn die Daten benannte Parameter haben, können Sie mit der Methode auch eine von Spalten für jede Eigenschaft angeben, die `console.table()` als zweiter Parameter angezeigt werden `Array` soll.</span><span class="sxs-lookup"><span data-stu-id="11a9f-163">If the data has named parameters, the `console.table()` method also allows you to specify an `Array` of columns for each property to display as a second parameter.</span></span>  <span data-ttu-id="11a9f-164">Das folgende Beispiel zeigt, wie Sie ein Array von Spalten angeben, das besser lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="11a9f-164">The following example displays how to specify an array of columns that is more readable.</span></span>  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filterinformationen, die console.table anzeigt und ein Array von Eigenschaften bereitstellen, die als zweiter Parameter angezeigt werden" lightbox="../media/console-log-table-filtered.msft.png":::
   <span data-ttu-id="11a9f-166">Filtern von Informationen, die ein Array von Eigenschaften anzeigen und `console.table` bereitstellen, das als zweiter Parameter angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="11a9f-166">Filter information that `console.table` displays and provide an array of properties to display as a second parameter</span></span>  
:::image-end:::  

<span data-ttu-id="11a9f-167">Möglicherweise sind Sie versucht, die Protokollmethoden als Hauptmittel zum Debuggen von Webseiten zu verwenden, da Protokollmethoden einfach zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="11a9f-167">You may be tempted to use the log methods as your main means to debug webpages, because log methods are simple to use.</span></span>  <span data-ttu-id="11a9f-168">Berücksichtigen Sie das Ergebnis einer `console.log()` beliebigen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="11a9f-168">Consider the result of any `console.log()` request.</span></span>  <span data-ttu-id="11a9f-169">Liveprodukte sollten kein Protokoll verwenden, das zum Debuggen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="11a9f-169">Live products shouldn't use any log that was used to debug.</span></span>  <span data-ttu-id="11a9f-170">Dies kann Insiderinformationen für Personen enthalten.</span><span class="sxs-lookup"><span data-stu-id="11a9f-170">It may reveal inside information to people.</span></span>  <span data-ttu-id="11a9f-171">Und das in der Konsole **erstellte** Rauschen ist überwältigend.</span><span class="sxs-lookup"><span data-stu-id="11a9f-171">And the noise created in the **Console** is overwhelming.</span></span>  <span data-ttu-id="11a9f-172">Wenn Sie [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] oder [Live Expressions][DevtoolsConsoleLiveExpressions]verwenden, können Sie feststellen, dass Ihre Workflows effektiver sind und bessere Ergebnisse erzielen.</span><span class="sxs-lookup"><span data-stu-id="11a9f-172">When you use [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] or [Live Expressions][DevtoolsConsoleLiveExpressions], you may find that your workflows are more effective and you get better results.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="11a9f-173">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="11a9f-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtern von Konsolennachrichten | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Überwachen von Änderungen in JavaScript mithilfe von Live Expressions | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-examples.html "Beispiele für Konsolenmeldungen: Protokollierung, Informationen, Fehler und | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-types.html "Beispiele für Konsolenmeldungen: Protokollieren verschiedener | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-groups.html "Beispiele für Konsolenmeldungen: Gruppieren von Protokollen | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-specifiers.html "Beispiele für Konsolenmeldungen: Protokollierung mit | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-table.html "Beispiele für Konsolenmeldungen: Verwenden von | GitHub"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stapelverfolgungs-| Wikipedia"  
