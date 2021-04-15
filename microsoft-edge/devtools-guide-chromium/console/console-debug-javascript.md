---
description: JavaScript-Fehler werden von Entwicklertools gemeldet und debuggen jeweils in der Konsole
title: Nachverfolgen von Fehlern mithilfe der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483472"
---
# <a name="debug-errors-reported-in-console"></a><span data-ttu-id="be296-104">In der Konsole gemeldete Debugfehler</span><span class="sxs-lookup"><span data-stu-id="be296-104">Debug errors reported in Console</span></span>  

<span data-ttu-id="be296-105">Die erste Erfahrung, die Sie mit der **Konsole haben,** ist wahrscheinlich ein Fehler in einem Skript.</span><span class="sxs-lookup"><span data-stu-id="be296-105">The first experience you have with the **Console** is probably an error in a script.</span></span>  <span data-ttu-id="be296-106">Navigieren Sie zu JavaScript-Fehler, der im [Konsolentool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="be296-106">To try it, navigate to [JavaScript error reported in the Console tool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span></span>  

<span data-ttu-id="be296-107">Wenn Sie DevTools im Browser öffnen, zeigt eine Schaltfläche oben rechts einen Fehler für die Webseite an.</span><span class="sxs-lookup"><span data-stu-id="be296-107">If you open DevTools in the browser, a button on the top right displays an error for the webpage.</span></span>  
<span data-ttu-id="be296-108">Wählen Sie die Schaltfläche aus, um Sie zur **Konsole zu führen,** und geben Sie weitere Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="be296-108">Choose the button to take you to the **Console** and give you more information about the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools enthält detaillierte Informationen zum Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="be296-110">DevTools enthält detaillierte Informationen zum Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="be296-110">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="be296-111">Aus den Informationen können Sie erfassen, dass sich der Fehler in Zeile 16 der Datei `error.html` befindet.</span><span class="sxs-lookup"><span data-stu-id="be296-111">From the information, you may gather that the error is on line 16 of the `error.html` file.</span></span>  <span data-ttu-id="be296-112">Wenn Sie den Link rechts neben der Konsole auswählen, führt er Sie zum Tool Sources und hebt die Codezeile mit `error.html:16` dem Fehler hervor. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="be296-112">If you choose the `error.html:16` link on the right of the **Console**, it takes you to the **Sources** tool and highlights the line of code with the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="Das Tool Sources hebt die Codezeile hervor, die den Fehler verursacht." lightbox="../media/console-debug-displays-in-sources.msft.png":::
   <span data-ttu-id="be296-114">Das **Tool Sources** hebt die Codezeile hervor, die den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="be296-114">The **Sources** tool highlights the line of code that causes the error</span></span>  
:::image-end:::  

<span data-ttu-id="be296-115">Das Skript versucht, das erste Element im Dokument zu erhalten `h2` und einen roten Rahmen um das Dokument zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="be296-115">The script tries to get the first `h2` element in the document and paint a red border around it.</span></span>  <span data-ttu-id="be296-116">Es ist `h2` jedoch kein Element vorhanden, sodass das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="be296-116">But no `h2` element exists, so the script fails.</span></span>  

## <a name="find-and-debug-network-issues"></a><span data-ttu-id="be296-117">Suchen und Debuggen von Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="be296-117">Find and debug network issues</span></span>  

<span data-ttu-id="be296-118">Andere Fehler, die die **Konsole** meldet, sind Netzwerkfehler.</span><span class="sxs-lookup"><span data-stu-id="be296-118">Other errors that the **Console** reports are network errors.</span></span>  <span data-ttu-id="be296-119">Navigieren Sie zum Netzwerkfehler, der in der Konsole gemeldet wurde, um sie in Aktion [anzeigen zu können.][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]</span><span class="sxs-lookup"><span data-stu-id="be296-119">To display it in action, navigate to the [Network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="Konsole zeigt einen Netzwerk- und einen JavaScript-Fehler an" lightbox="../media/console-debug-network-error.msft.png":::
   <span data-ttu-id="be296-121">**Konsole** zeigt einen Netzwerk- und einen JavaScript-Fehler an</span><span class="sxs-lookup"><span data-stu-id="be296-121">**Console** displays a Network and a JavaScript error</span></span>  
:::image-end:::  

<span data-ttu-id="be296-122">Die Tabelle zeigt an, aber auf der Webseite ändert `loading` sich nichts, da die Daten nie abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="be296-122">The table displays `loading`, but nothing changes on the webpage because the data is never retrieved.</span></span>  <span data-ttu-id="be296-123">In der **Konsole**sind die folgenden beiden Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="be296-123">In the **Console**, the following two errors occurred.</span></span>  

*   <span data-ttu-id="be296-124">Ein Netzwerkfehler, der mit der `GET` HTTP-Methode gefolgt von einem URI beginnt.</span><span class="sxs-lookup"><span data-stu-id="be296-124">A network error that starts with `GET` HTTP method followed by a URI.</span></span>  
*   <span data-ttu-id="be296-125">Ein `Uncaught (in promise) TypeError: data.forEach is not a function` Fehler.</span><span class="sxs-lookup"><span data-stu-id="be296-125">An `Uncaught (in promise) TypeError: data.forEach is not a function` error.</span></span>  
    
<span data-ttu-id="be296-126">Wenn Sie den Link in der Konsole `network-error.html:40` **auswählen,** führt DevTools Sie zum **Sources-Tool.**</span><span class="sxs-lookup"><span data-stu-id="be296-126">If you choose the `network-error.html:40` link in the **Console**, DevTools takes you to the **Sources** tool.</span></span>  <span data-ttu-id="be296-127">Die problematische Codezeile wird hervorgehoben und gefolgt von einer `error` \( `x` \)-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="be296-127">The problematic line of code is highlighted and followed by an `error` \(`x`\) button.</span></span>  <span data-ttu-id="be296-128">Wählen Sie zum `Failed to load resource: the server responded with a status of 404 ()` Anzeigen der Fehlermeldung die Schaltfläche **Fehler** \( `x` \) aus.</span><span class="sxs-lookup"><span data-stu-id="be296-128">To display the `Failed to load resource: the server responded with a status of 404 ()` error message, choose the **error** \(`x`\) button.</span></span>  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Wählen Sie den Link zur Webseite aus, und Code, in dem der Fehler auftritt, wird das Tool Quellen geöffnet." lightbox="../media/console-debug-network-error-code-line.msft.png":::
         <span data-ttu-id="be296-130">Wählen Sie den Link zur Webseite aus, und Code, in dem der Fehler auftritt, wird das **Tool Quellen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="be296-130">Choose the link to the webpage and code where the error occurs line opens the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Verwenden Sie das Tool Quellen, um den Fehler in JavaScript zu finden." lightbox="../media/console-debug-network-error-sources.msft.png":::
         <span data-ttu-id="be296-132">Verwenden Sie das Tool Quellen, um den Fehler in JavaScript **zu** finden.</span><span class="sxs-lookup"><span data-stu-id="be296-132">To find the error in JavaScript, use the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="be296-133">Im Beispiel informiert der Fehler Sie, dass die angeforderte URL nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="be296-133">In the example, the error informs you that the requested URL isn't found.</span></span>  <span data-ttu-id="be296-134">Führen Sie als Nächstes die folgenden Aktionen aus, um das **Netzwerktool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="be296-134">Next, complete the following actions to open the **Network** tool.</span></span>  

1.  <span data-ttu-id="be296-135">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="be296-135">Open the **Console**.</span></span>  
1.  <span data-ttu-id="be296-136">Wählen Sie den URI aus, der dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="be296-136">Choose the URI associated with the error.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="Konsole zeigt einen HTTP-Statuscode des Fehlers an, nachdem eine Ressource nicht geladen wurde" lightbox="../media/console-debug-network-error-url.msft.png":::
   <span data-ttu-id="be296-138">**Konsole** zeigt einen HTTP-Statuscode des Fehlers an, nachdem eine Ressource nicht geladen wurde</span><span class="sxs-lookup"><span data-stu-id="be296-138">**Console** displays an HTTP status code of the error after a resource isn't loaded</span></span>  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="Das Netzwerktool zeigt weitere Informationen zur fehlgeschlagenen Anforderung an." lightbox="../media/console-debug-network-error-network.msft.png":::
           <span data-ttu-id="be296-140">Das **Netzwerktool** zeigt weitere Informationen zur fehlgeschlagenen Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="be296-140">The **Network** tool displays more information about the failed request</span></span>  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Überprüfen der Kopfzeilen im Netzwerktool kann mehr Einblick geben" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           <span data-ttu-id="be296-142">Überprüfen der Kopfzeilen im **Netzwerktool** kann mehr Einblick geben</span><span class="sxs-lookup"><span data-stu-id="be296-142">Inspect the headers in the **Network** tool may give more insight</span></span>  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="be296-143">Was war das Problem?</span><span class="sxs-lookup"><span data-stu-id="be296-143">What was the problem?</span></span>  <span data-ttu-id="be296-144">Zwei Schrägstriche \( `//` \) treten im angeforderten URI nach dem Wort `repos` auf.</span><span class="sxs-lookup"><span data-stu-id="be296-144">Two slash characters \(`//`\) occur in the requested URI after the word `repos`.</span></span>  <span data-ttu-id="be296-145">Öffnen Sie das **Tool Quellen,** und überprüfen Sie Zeile 26.</span><span class="sxs-lookup"><span data-stu-id="be296-145">Open the **Sources** tool and inspect line 26.</span></span>  <span data-ttu-id="be296-146">Ein nachgestellter Schrägstrich \( \) tritt am Ende des `/` Basis-URI auf.</span><span class="sxs-lookup"><span data-stu-id="be296-146">A trailing slash character \(`/`\) occurs at the end of the base URI.</span></span>  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="Das Tool Quellen zeigt die Codezeile mit dem Fehler an." lightbox="../media/console-debug-network-error-code-error.msft.png":::
   <span data-ttu-id="be296-148">Das **Tool Quellen** zeigt die Codezeile mit dem Fehler an.</span><span class="sxs-lookup"><span data-stu-id="be296-148">The **Sources** tool displays the line of code with the error</span></span>  
:::image-end:::  

<span data-ttu-id="be296-149">Um keine Fehler in der Konsole zu **überprüfen,** navigieren Sie zu [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span><span class="sxs-lookup"><span data-stu-id="be296-149">To review no errors in the **Console**, navigate to [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="Das Beispiel ohne Fehler lädt Informationen aus GitHub und zeigt es an." lightbox="../media/console-debug-network-error-fixed.msft.png":::
   <span data-ttu-id="be296-151">Das Beispiel ohne Fehler lädt Informationen aus GitHub und zeigt es an.</span><span class="sxs-lookup"><span data-stu-id="be296-151">The example without any errors loads information from GitHub and displays it</span></span>  
:::image-end:::  

<span data-ttu-id="be296-152">Stellen Sie sicher, dass Sie defensiv Codierungstechniken bereitstellen, um die vorherigen Benutzererfahrungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="be296-152">Ensure you provide defensive coding techniques to avoid the previous user experiences.</span></span>  <span data-ttu-id="be296-153">Stellen Sie außerdem sicher, dass Ihr Code Fehler abfängt und jede in der **Konsole angezeigt wird.**</span><span class="sxs-lookup"><span data-stu-id="be296-153">Also, ensure your code catches errors and display each in the **Console**.</span></span>  <span data-ttu-id="be296-154">Navigieren Sie [zu Netzwerkfehlerbericht in Konsole und Benutzeroberfläche,][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] und überprüfen Sie die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="be296-154">Navigate to [Network error reporting in Console and UI][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] and review the following items.</span></span>  

*   <span data-ttu-id="be296-155">Stellen Sie dem Benutzer die Benutzeroberfläche zur Verfügung, dass etwas schief gelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="be296-155">Provide UI to the user that something went wrong.</span></span>  
*   <span data-ttu-id="be296-156">Geben Sie **in der Konsole**hilfreiche Informationen zum Netzwerkfehler aus Ihrem Code an.</span><span class="sxs-lookup"><span data-stu-id="be296-156">In the **Console**, provide helpful information about the Network error from your code.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Ein Beispiel, das Fehler abfängt und meldet" lightbox="../media/console-debug-network-error-report.msft.png":::
   <span data-ttu-id="be296-158">Ein Beispiel, das Fehler abfängt und meldet</span><span class="sxs-lookup"><span data-stu-id="be296-158">An example that catches and reports errors</span></span>  
:::image-end:::  

<span data-ttu-id="be296-159">Der folgende Codeausschnitt fängt Fehler mithilfe der Methode ab und meldet `handleErrors` sie, insbesondere die `throw Error` Zeile.</span><span class="sxs-lookup"><span data-stu-id="be296-159">The following code snippet catches and reports errors using the `handleErrors` method, specifically the `throw Error` line.</span></span>  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a><span data-ttu-id="be296-160">Erstellen von Fehlern und Ablaufverfolgungen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="be296-160">Create errors and traces in the Console</span></span>

<span data-ttu-id="be296-161">Neben dem Beispiel im vorherigen Abschnitt können Sie auch verschiedene Fehler und Ablaufverfolgungsprobleme `throw Error` in der **Konsole erstellen.**</span><span class="sxs-lookup"><span data-stu-id="be296-161">Besides the `throw Error` example in the previous section, you may also create different errors and trace problems in the **Console**.</span></span>  
<span data-ttu-id="be296-162">Navigieren Sie zum Anzeigen von zwei erstellten Fehlermeldungen in der **Konsole**zu [Erstellen von Fehlerberichten und -assertionen in der Konsole.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]</span><span class="sxs-lookup"><span data-stu-id="be296-162">To display two created error messages in the **Console**, navigate to [Creating error reports and assertions in Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span></span>  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Von der Konsole erstellte Fehlermeldungen" lightbox="../media/console-debug-error-assert.msft.png":::
   <span data-ttu-id="be296-164">Von der Konsole erstellte **Fehlermeldungen**</span><span class="sxs-lookup"><span data-stu-id="be296-164">Error messages created from **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="be296-165">Der folgende Codeausschnitt wurde im vorherigen Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="be296-165">The following code snippet was used in the previous example.</span></span>  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

<span data-ttu-id="be296-166">Sie verfügen über drei Funktionen, die sich nacheinander gegenseitig anfordern.</span><span class="sxs-lookup"><span data-stu-id="be296-166">You have three functions that request each other in succession.</span></span>  

*   `first()`  
*   `second()`  
*   `third()`  
    
<span data-ttu-id="be296-167">Jeder sendet ein `name` Argument an das andere.</span><span class="sxs-lookup"><span data-stu-id="be296-167">Each sends a `name` argument to the other.</span></span>  <span data-ttu-id="be296-168">In der Funktion überprüfen Sie, ob das Argument vorhanden ist, und wenn nicht, protokollieren Sie einen Fehler, dass der Name `third()` `name` nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="be296-168">In the `third()` function, you check if the `name` argument exists and if it doesn't, you log an error that name isn't defined.</span></span>  <span data-ttu-id="be296-169">Wenn definiert, verwenden Sie die -Methode, um zu überprüfen, ob das `name` Argument weniger als acht Buchstaben lang `assert()` `name` ist.</span><span class="sxs-lookup"><span data-stu-id="be296-169">If `name` is defined, you use the `assert()` method to check if the `name` argument is fewer than eight letters long.</span></span>  <span data-ttu-id="be296-170">Sie fordern die `first()` Funktion dreimal mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="be296-170">You request the `first()` function three times, with the following parameters.</span></span>  

*   <span data-ttu-id="be296-171">Kein Argument, das die `console.error()` Methode in der Funktion `third()` auslöst.</span><span class="sxs-lookup"><span data-stu-id="be296-171">No argument that triggers the `console.error()` method in the `third()` function.</span></span>  
*   <span data-ttu-id="be296-172">Der Ausdruck als Parameter für die Funktion verursacht keinen Fehler, da argument vorhanden ist und kürzer `Console` `first()` als acht Buchstaben `name` ist.</span><span class="sxs-lookup"><span data-stu-id="be296-172">The term `Console` as a parameter to the `first()` function doesn't cause an error because `name` argument exists and is shorter than eight letters.</span></span>  
*   <span data-ttu-id="be296-173">Der Ausdruck als zu verwendende Parameter bewirkt, dass die Methode einen Fehler gemeldet, da der Parameter länger als `Microsoft Edge Canary` `first()` acht Buchstaben `console.assert()` ist.</span><span class="sxs-lookup"><span data-stu-id="be296-173">The phrase `Microsoft Edge Canary` as a parameter to `first()` function causes the `console.assert()` method to report an error, because the parameter is longer than eight letters.</span></span>  
    
<span data-ttu-id="be296-174">Verwenden Sie die `console.assert()` -Methode, um bedingte Fehlerberichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be296-174">Use the `console.assert()` method to create conditional error reports.</span></span>  <span data-ttu-id="be296-175">Die folgenden beiden Beispiele haben dasselbe Ergebnis, aber eines benötigt eine zusätzliche `if{}` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="be296-175">The following two examples have the same result, but one needs an extra `if{}` statement.</span></span>  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> <span data-ttu-id="be296-176">Die zweite und dritte Codezeilen führen den gleichen Test aus.</span><span class="sxs-lookup"><span data-stu-id="be296-176">The second and third lines of the code perform the same test.</span></span>  <span data-ttu-id="be296-177">Da die Assertion ein negatives Ergebnis aufzeichnen muss, testen Sie für den Fall `x < 40` `if` und für die `x >= 40` Assertion.</span><span class="sxs-lookup"><span data-stu-id="be296-177">Because the assertion needs to record a negative result, you test for `x < 40` in the `if` case and `x >= 40` for the assertion.</span></span>  

<span data-ttu-id="be296-178">Wenn Sie nicht sicher sind, welche Funktion eine andere Funktion anfordert, verwenden Sie die Methode, um nach zu verfolgen, welche Funktionen angefordert werden, um zu der `console.trace()` aktuellen zu kommen.</span><span class="sxs-lookup"><span data-stu-id="be296-178">If you aren't sure which function requests another function, use the `console.trace()` method to track which functions are requested to get to the current one.</span></span>  <span data-ttu-id="be296-179">Navigieren Sie zum Anzeigen der Ablaufverfolgung in der **Konsole**zu [Erstellen von Ablaufverfolgungen in der Konsole.][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]</span><span class="sxs-lookup"><span data-stu-id="be296-179">To display the trace in the **Console**, navigate to [Creating traces in Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span></span>  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

<span data-ttu-id="be296-180">Das Ergebnis ist eine Ablaufverfolgung, die mit dem Namen und dann und im zweiten Beispiel mit dem Namen angezeigt `here()` `there()` `everywhere()` `everywhere()` wird.</span><span class="sxs-lookup"><span data-stu-id="be296-180">The result is a trace to display that `here()` is named `there()` and then `everywhere()` and in the second example that it's named `everywhere()`.</span></span>  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Eine von der Konsole erstellte Ablaufverfolgung" lightbox="../media/console-debug-trace.msft.png":::
   <span data-ttu-id="be296-182">Eine von der Konsole erstellte **Ablaufverfolgung**</span><span class="sxs-lookup"><span data-stu-id="be296-182">A trace created from **Console**</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="be296-183">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="be296-183">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Im Konsolentool gemeldeter JavaScript-Fehler | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Erstellen von Fehlerberichten und Assertionen in Konsolen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Netzwerkfehler in Konsolen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "In Konsolenkonsolen gemeldeter Netzwerkfehler | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Netzwerkfehlerberichte in Konsolen- und Benutzeroberflächen| GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Erstellen von Ablaufverfolgungen in konsolen | GitHub"  
