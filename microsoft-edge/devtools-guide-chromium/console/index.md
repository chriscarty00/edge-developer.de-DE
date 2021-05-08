---
description: Eine Einführung in das Konsolentool innerhalb der Microsoft Edge Developer Tools.
title: Verwenden der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483207"
---
# <a name="use-the-console"></a><span data-ttu-id="d52d3-104">Verwenden der Konsole</span><span class="sxs-lookup"><span data-stu-id="d52d3-104">Use the Console</span></span>  

<span data-ttu-id="d52d3-105">Das **Konsolentool** der DevTools hilft Ihnen bei verschiedenen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d52d3-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="d52d3-106">Die folgende Liste enthält einige der Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d52d3-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="d52d3-107">Erfahren Sie, warum im aktuellen Projekt etwas nicht funktioniert, und verfolgen [Sie Probleme.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="d52d3-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="d52d3-108">[Erhalten Sie Informationen zum Webprojekt][DevtoolsConsoleConsoleFilters] im Browser als Protokollnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d52d3-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="d52d3-109">[Protokollieren von Informationen][DevtoolsConsoleConsoleLog] in Skripts zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="d52d3-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="d52d3-110">[Testen Sie JavaScript-Ausdrücke][DevtoolsConsoleConsoleJavascript] live in einer [REPL-Umgebung.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="d52d3-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="d52d3-111">[Interagieren Sie mit dem Webprojekt im Browser mithilfe][DevtoolsConsoleConsoleDomInteraction] von JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d52d3-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="d52d3-112">Die **Konsole** ist ein hervorragendes Begleittool für andere Tools.</span><span class="sxs-lookup"><span data-stu-id="d52d3-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="d52d3-113">Die **Konsole** bietet eine leistungsstarke Möglichkeit, die aktuelle Webseite mithilfe von JavaScript zu skripten, zu überprüfen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d52d3-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Das Konsolentool wird im oberen Bereich geöffnet" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="d52d3-115">Das **Konsolentool** wird im oberen Bereich geöffnet</span><span class="sxs-lookup"><span data-stu-id="d52d3-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Konsole im unteren Bereich mit dem oben geöffneten Elementtool" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="d52d3-117">**Konsole** im unteren Bereich mit dem oben geöffneten **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="d52d3-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d52d3-118">Die schnellste Möglichkeit, die Konsole direkt zu **öffnen,** besteht in der Auswahl `Control` + `Shift` + `J` von \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d52d3-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="d52d3-119">Fehlerberichte und Konsole</span><span class="sxs-lookup"><span data-stu-id="d52d3-119">Error reports and Console</span></span>  

<span data-ttu-id="d52d3-120">**Konsole** ist der Standardspeicherort, an dem JavaScript- und Konnektivitätsfehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d52d3-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="d52d3-121">Wenn Fehler auftreten, wird neben dem Symbol **Einstellungen** in DevTools eine Schaltfläche angezeigt, die die Anzahl der Fehler und Warnungen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d52d3-121">If any errors occur, a button displays next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="d52d3-122">Wählen Sie es aus, um die **Konsole zu öffnen** und das Problem zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-122">Choose it to open the **Console** and display the problem.</span></span>  <span data-ttu-id="d52d3-123">Weitere Informationen finden Sie unter [Debuggen von Fehlern, die in der Konsole gemeldet wurden.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="d52d3-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools enthält detaillierte Informationen zum Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="d52d3-125">DevTools enthält detaillierte Informationen zum Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="d52d3-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="d52d3-126">Überprüfen und Filtern von Informationen auf der aktuellen Webseite</span><span class="sxs-lookup"><span data-stu-id="d52d3-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="d52d3-127">Wenn Sie devTools auf einer Webseite öffnen, wird wahrscheinlich eine Informationsflut angezeigt, die bei der Konsole protokolliert **wurde.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-127">When you open the DevTools on a webpage, you're likely to display a deluge of information logged to the **Console**.</span></span>  <span data-ttu-id="d52d3-128">Die Menge der Informationen wird zu einem Problem, wenn Sie wichtige Informationen identifizieren müssen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="d52d3-129">Verwenden Sie das Tool Probleme in DevTools, um die wichtigen Informationen anzeigen zu können, die eine [Aktion][DevtoolsIssuesIndex] benötigt.</span><span class="sxs-lookup"><span data-stu-id="d52d3-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>  <span data-ttu-id="d52d3-130">Ein Teil des Geräuschs bleibt erhalten, weshalb es gut ist, über die automatisierten Protokoll- und Filteroptionen [in][DevtoolsConsoleConsoleFilters] der Konsole zu **wissen.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-130">Much of the noise remains, which is why it's a good idea to know about the [automated log and filter options][DevtoolsConsoleConsoleFilters] in the **Console**.</span></span>  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools mit einer Konsole voller Nachrichten" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="d52d3-132">DevTools mit einer **Konsole** voller Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d52d3-132">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="d52d3-133">Protokollinformationen, die in der Konsole angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="d52d3-133">Log information to display in the Console</span></span>  

<span data-ttu-id="d52d3-134">Der beliebteste Verwendungsfall für die **Konsole** ist die Protokollierung von Informationen aus Ihren Skripts mithilfe der `console.log()` -Methode oder anderer ähnlicher Methoden.</span><span class="sxs-lookup"><span data-stu-id="d52d3-134">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="d52d3-135">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-135">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-136">Wählen **Sie**zum Öffnen der Konsole `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="d52d3-136">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="d52d3-137">Navigieren Sie [zu Konsolennachrichtenbeispiele: Protokoll, Info, Fehler][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]und Warn , oder kopieren und führen Sie den folgenden Codeausschnitt in der Konsole **aus.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-137">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  <span data-ttu-id="d52d3-138">Die **Konsole** zeigt die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="d52d3-138">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Konsole voller Nachrichten, die durch Democode verursacht werden" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="d52d3-140">**Konsole** voller Nachrichten, die durch Democode verursacht werden</span><span class="sxs-lookup"><span data-stu-id="d52d3-140">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d52d3-141">Viele nützliche Methoden stehen zur Verfügung, wenn Sie mit der **Konsole arbeiten.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-141">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="d52d3-142">Weitere Informationen finden Sie unter [Protokollieren von Nachrichten im Konsolentool.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="d52d3-142">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="d52d3-143">Testen Sie Ihr JavaScript live in der Konsole</span><span class="sxs-lookup"><span data-stu-id="d52d3-143">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="d52d3-144">Die **Konsole** ist nicht nur ein Ort zum Protokollieren von Informationen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-144">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="d52d3-145">Die **Konsole** ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="d52d3-145">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="d52d3-146">Wenn Sie JavaScript in der Konsole **schreiben,** wird der Code sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d52d3-146">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="d52d3-147">Möglicherweise ist es hilfreich, einige neue JavaScript-Features zu testen oder einige schnelle Berechnungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-147">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="d52d3-148">Darüber hinaus erhalten Sie alle Features, die Sie von einer modernen Bearbeitungsumgebung erwarten, z. B. autocompletion, syntax highlighting und history.</span><span class="sxs-lookup"><span data-stu-id="d52d3-148">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="d52d3-149">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-149">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-150">Navigieren Sie zur **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="d52d3-150">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="d52d3-151">Geben Sie `2 + 2` ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-151">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="d52d3-152">Die **Konsole** zeigt das Ergebnis `4` in der folgenden Zeile an.</span><span class="sxs-lookup"><span data-stu-id="d52d3-152">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="d52d3-153">Dieses **Feature für die** Begierdebewertung ist hilfreich, um zu debuggen und zu überprüfen, ob Sie keine Fehler im Code machen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-153">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Die Konsole zeigt das Ergebnis von 2 + 2 live an, während Sie es eingeben" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="d52d3-155">Die **Konsole** zeigt das Ergebnis von `2 + 2` live an, während Sie es eingeben</span><span class="sxs-lookup"><span data-stu-id="d52d3-155">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="d52d3-156">Wählen Sie aus, um den JavaScript-Ausdruck in der **Konsole ausführen** und optional ein Ergebnis anzeigen zu `Enter` können.</span><span class="sxs-lookup"><span data-stu-id="d52d3-156">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="d52d3-157">Anschließend können Sie den nächsten JavaScript-Code schreiben, der in der Konsole ausgeführt **werden soll.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-157">Then, you may write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Mehrere Zeilen JavaScript-Code nacheinander ausführen" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="d52d3-159">Mehrere Zeilen JavaScript-Code nacheinander ausführen</span><span class="sxs-lookup"><span data-stu-id="d52d3-159">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="d52d3-160">Standardmäßig führen Sie JavaScript-Code in einer einzelnen Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="d52d3-160">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="d52d3-161">Geben Sie zum Ausführen einer Zeile Ihr JavaScript ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="d52d3-161">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="d52d3-162">Wählen Sie anstelle von aus, um die Einzeilerbeschränkung `Shift` + `Enter` zu `Enter` umgehen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-162">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="d52d3-163">Wählen Sie ähnlich wie bei anderen Befehlszeilenerfahrungen aus, um auf Ihre vorherigen JavaScript-Befehle zu `Arrow-Up` zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-163">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="d52d3-164">Das AutoCompletion-Feature der **Konsole** ist eine hervorragende Möglichkeit, um sich mit nicht vertrauten Methoden vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-164">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="d52d3-165">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-165">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-166">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="d52d3-166">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d52d3-167">Geben Sie `doc` ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-167">Type `doc`.</span></span>  
1.  <span data-ttu-id="d52d3-168">Wählen `document` Sie aus dem Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="d52d3-168">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="d52d3-169">Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-169">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="d52d3-170">Geben Sie `.bo` ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-170">Type `.bo`.</span></span>  
1.  <span data-ttu-id="d52d3-171">Wählen `tab` Sie aus, um `document.body` zu erhalten .</span><span class="sxs-lookup"><span data-stu-id="d52d3-171">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="d52d3-172">Geben Sie einen anderen ein, um die vollständige Liste der im Textkörper der aktuellen Webseite verfügbaren Eigenschaften und `.` Methoden anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-172">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="d52d3-173">Weitere Informationen zu allen Möglichkeiten \*\*\*\* zum Arbeiten mit konsolen finden Sie unter [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="d52d3-173">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Konsolenautocompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="d52d3-175">\*\*\*\* Konsolenautocompletion von JavaScript-Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="d52d3-175">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="d52d3-176">Interagieren mit der aktuellen Webseite im Browser</span><span class="sxs-lookup"><span data-stu-id="d52d3-176">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="d52d3-177">Die **Konsole** hat Zugriff auf das [Window-Objekt][MdnDocsWebApiWindow] des Browsers.</span><span class="sxs-lookup"><span data-stu-id="d52d3-177">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="d52d3-178">Sie können Skripts schreiben, die mit der aktuellen Webseite interagieren.</span><span class="sxs-lookup"><span data-stu-id="d52d3-178">You may write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="d52d3-179">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-179">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-180">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="d52d3-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d52d3-181">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-181">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Kopieren des Inhalts der obersten Überschrift (h1) aus dem DOM und Anzeigen in der Konsole" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="d52d3-183">Kopieren Sie den Inhalt der obersten Überschrift \( `h1` \) aus dem DOM, und zeigen Sie sie in der Konsole **an.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-183">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="d52d3-184">Anstatt nur von der Webseite zu lesen, können Sie sie auch ändern.</span><span class="sxs-lookup"><span data-stu-id="d52d3-184">Instead of only reading from the webpage, you may also change it.</span></span>  <span data-ttu-id="d52d3-185">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="d52d3-185">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-186">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="d52d3-186">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d52d3-187">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-187">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Schreiben von Text in das DOM in der Konsole" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="d52d3-189">Schreiben von Text in das DOM in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="d52d3-189">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="d52d3-190">Sie haben die Hauptüberschrift der Webseite in **"Rocking the Console" geändert.**</span><span class="sxs-lookup"><span data-stu-id="d52d3-190">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="d52d3-191">Die **Methoden des Konsolenprogramms** machen den Zugriff auf die aktuelle Webseite und das Bearbeiten der aktuellen Webseite einfach.</span><span class="sxs-lookup"><span data-stu-id="d52d3-191">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="d52d3-192">Weitere Informationen finden Sie unter [Console Utilities API reference][DevtoolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="d52d3-192">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="d52d3-193">Um beispielsweise einen grünen Rahmen um alle Links auf der aktuellen Webseite hinzuzufügen, führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d52d3-193">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="d52d3-194">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="d52d3-194">Open the **Console**.</span></span>  
1.  <span data-ttu-id="d52d3-195">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="d52d3-195">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Bearbeiten einer Auswahl von Elementen mithilfe der Konsole" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="d52d3-197">Bearbeiten einer Auswahl von Elementen mithilfe der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="d52d3-197">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="d52d3-198">Weitere Informationen zum Arbeiten mit dem DOM finden Sie unter [Verwenden der Konsole für die Interaktion mit dem DOM][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="d52d3-198">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="d52d3-199">Weitere Informationen zur Konsole</span><span class="sxs-lookup"><span data-stu-id="d52d3-199">Learn more about Console</span></span>  

<span data-ttu-id="d52d3-200">Weitere Informationen zur Konsole finden Sie unter **Console** [reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities]und Console API [reference][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="d52d3-200">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d52d3-201">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d52d3-201">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Debuggen von Fehlern, die im Konsolenmodus | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Verwenden der Konsole für die Interaktion mit der DOM-| Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtern von Konsolennachrichten | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokollieren von Nachrichten im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevtoolsIssuesIndex]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Beispiele für Konsolenmeldungen: Protokollierung, Informationen, Fehler und | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-| Wikipedia"  
