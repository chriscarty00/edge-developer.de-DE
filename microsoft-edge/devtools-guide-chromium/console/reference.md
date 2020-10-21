---
description: Eine umfassende Referenz zu jedem Feature und Verhalten im Zusammenhang mit der Konsolen-UI in Microsoft Edge devtools
title: Konsolen Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125258"
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

# <span data-ttu-id="f5613-104">Konsolen Referenz</span><span class="sxs-lookup"><span data-stu-id="f5613-104">Console Reference</span></span>  

<span data-ttu-id="f5613-105">Diese Seite ist eine Referenz zu Features, die sich auf die Microsoft Edge devtools-Konsole beziehen.</span><span class="sxs-lookup"><span data-stu-id="f5613-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="f5613-106">Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um aufgezeichnete Nachrichten anzuzeigen und JavaScript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f5613-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="f5613-107">Wenn dies nicht der Fall ist, navigieren Sie zu erste [Schritte mit der Ausführung von JavaScript in der Konsole][DevToolsConsoleJavascript] , und [beginnen Sie mit der Protokollierung von Nachrichten in der Konsole][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="f5613-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="f5613-108">Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` Siehe [Console API Reference][DevToolsConsoleApi]suchen.</span><span class="sxs-lookup"><span data-stu-id="f5613-108">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="f5613-109">Wenn Sie auf Funktionen wie verweisen möchten `monitorEvents()` , navigieren Sie zu [API-Referenz für Konsolen Dienstprogramme][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="f5613-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="f5613-110">Öffnen der Konsole</span><span class="sxs-lookup"><span data-stu-id="f5613-110">Open the Console</span></span>  

<span data-ttu-id="f5613-111">Sie können die Konsole als [Panel](#open-the-console-panel) oder als [Registerkarte im Einzug](#open-the-console-tab-in-the-drawer)öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5613-111">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="f5613-112">Öffnen des Konsolen Panels</span><span class="sxs-lookup"><span data-stu-id="f5613-112">Open the Console panel</span></span>  

<span data-ttu-id="f5613-113">Wählen Sie `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="f5613-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="f5613-115">Die **Konsolen** Leiste</span><span class="sxs-lookup"><span data-stu-id="f5613-115">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="f5613-116">Wenn Sie die Konsolen Leiste über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Panel** -Badge befindet.</span><span class="sxs-lookup"><span data-stu-id="f5613-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="f5613-118">Der Befehl zum Anzeigen des **Konsolen** Panels</span><span class="sxs-lookup"><span data-stu-id="f5613-118">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="f5613-119">Öffnen der Registerkarte "Konsole" im Einzug</span><span class="sxs-lookup"><span data-stu-id="f5613-119">Open the Console tab in the Drawer</span></span>  

<span data-ttu-id="f5613-120">Wählen Sie `Escape` **devtools anpassen und Steuern** aus, und `...` Klicken Sie dann auf **Konsolen Einzug anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f5613-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="f5613-122">Konsolen Einzug anzeigen</span><span class="sxs-lookup"><span data-stu-id="f5613-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="f5613-123">Die Schublade wird unten im devtools-Fenster eingeblendet, und die Registerkarte **Konsole** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f5613-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="f5613-125">Die Registerkarte ' **Konsole** ' im **Einzug**</span><span class="sxs-lookup"><span data-stu-id="f5613-125">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="f5613-126">Wenn Sie die Registerkarte Konsole über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Einschub** Symbol neben dem Symbol befindet.</span><span class="sxs-lookup"><span data-stu-id="f5613-126">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="f5613-128">Der Befehl zum Anzeigen der Registerkarte " **Konsole** " im **Einzug**</span><span class="sxs-lookup"><span data-stu-id="f5613-128">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="f5613-129">Öffnen von Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="f5613-129">Open Console Settings</span></span>  

<span data-ttu-id="f5613-130">Wählen Sie **Konsoleneinstellungen** \ ( ![ Symbol für Konsoleneinstellungen ][ImageSettingsButtonIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="f5613-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="f5613-132">Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="f5613-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="f5613-133">Die folgenden Links erläutern jede Einstellung:</span><span class="sxs-lookup"><span data-stu-id="f5613-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="f5613-134">Netzwerk ausblenden</span><span class="sxs-lookup"><span data-stu-id="f5613-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="f5613-135">Protokoll beibehalten</span><span class="sxs-lookup"><span data-stu-id="f5613-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="f5613-136">Nur ausgewählter Kontext</span><span class="sxs-lookup"><span data-stu-id="f5613-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="f5613-137">Gruppieren ähnlich</span><span class="sxs-lookup"><span data-stu-id="f5613-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="f5613-138">Protokollieren von XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="f5613-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="f5613-139">Eifrige Auswertung</span><span class="sxs-lookup"><span data-stu-id="f5613-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="f5613-140">AutoVervollständigen aus Verlauf</span><span class="sxs-lookup"><span data-stu-id="f5613-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="f5613-141">Öffnen der Konsolen Leiste</span><span class="sxs-lookup"><span data-stu-id="f5613-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="f5613-142">Wählen Sie **Console Sidebar anzeigen** aus ![ ][ImageShowConsoleSidebarIcon] , um die Seitenleiste anzuzeigen, die für das Filtern nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5613-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="f5613-144">**Console** Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="f5613-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="f5613-145">Anzeigen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-145">View messages</span></span>  

<span data-ttu-id="f5613-146">Dieser Abschnitt enthält Features, die ändern, wie Nachrichten in der Konsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5613-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="f5613-147">Weitere Informationen finden Sie unter [Anzeigen von Nachrichten][DevToolsConsoleViewMessages] für eine praktische Exemplarische Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="f5613-147">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="f5613-148">Deaktivieren der Nachrichten Gruppierung</span><span class="sxs-lookup"><span data-stu-id="f5613-148">Disable message grouping</span></span>  

<span data-ttu-id="f5613-149">[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie **Gruppe ähnlich** , um das Standardverhalten der Nachrichten Gruppierung der Konsole zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="f5613-150">Ein Beispiel finden Sie unter [Protokoll XMLHttpRequest und Abrufen von Anforderungen](#log-xhr-and-fetch-requests) .</span><span class="sxs-lookup"><span data-stu-id="f5613-150">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="f5613-151">Protokollieren von XMLHttpRequest und Abrufen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5613-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="f5613-152">[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie **Protokoll-XMLHttpRequests** , um alle `XMLHttpRequest` und `Fetch` Anforderungen an die Konsole während des Auftretens zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="f5613-154">Protokoll `XMLHttpRequest` und `Fetch` Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5613-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="f5613-155">Die oberste Nachricht in der vorherigen Abbildung zeigt das standardmäßige Gruppierungs Verhalten der **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f5613-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="f5613-156">Beibehalten von Nachrichten über Seitenlasten</span><span class="sxs-lookup"><span data-stu-id="f5613-156">Persist messages across page loads</span></span>  

<span data-ttu-id="f5613-157">Standardmäßig wird die Konsole gelöscht, wenn Sie eine neue Seite laden.</span><span class="sxs-lookup"><span data-stu-id="f5613-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="f5613-158">Wenn Sie Nachrichten über Seitenlasten hinweg beibehalten möchten, öffnen Sie die [Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie dann das Kontrollkästchen **Protokoll beibehalten** .</span><span class="sxs-lookup"><span data-stu-id="f5613-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="f5613-159">Ausblenden von Netzwerknachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-159">Hide network messages</span></span>  

<span data-ttu-id="f5613-160">Standardmäßig protokolliert der Browser Netzwerknachrichten an die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="f5613-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="f5613-161">In der folgenden Abbildung stellt die ausgewählte Nachricht einen HTTP-Statuscode von dar `429` .</span><span class="sxs-lookup"><span data-stu-id="f5613-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="f5613-163">Eine `429` Nachricht in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="f5613-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="f5613-164">So blenden Sie Netzwerknachrichten aus:</span><span class="sxs-lookup"><span data-stu-id="f5613-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="f5613-165">[Öffnen Sie die Konsoleneinstellungen](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="f5613-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="f5613-166">Aktivieren Sie das Kontrollkästchen **Netzwerk ausblenden** .</span><span class="sxs-lookup"><span data-stu-id="f5613-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="f5613-167">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-167">Filter messages</span></span>  

<span data-ttu-id="f5613-168">Es gibt viele Möglichkeiten, Nachrichten in der Konsole zu filtern.</span><span class="sxs-lookup"><span data-stu-id="f5613-168">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="f5613-169">Filtern von Browser Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-169">Filter out browser messages</span></span>  

<span data-ttu-id="f5613-170">[Öffnen Sie die Konsolen Leiste](#open-the-console-sidebar) , und wählen Sie **Benutzer Nachrichten** aus, um nur Nachrichten anzuzeigen, die aus dem JavaScript der Seite stammen.</span><span class="sxs-lookup"><span data-stu-id="f5613-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="f5613-172">Anzeigen von Benutzer Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-172">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="f5613-173">Nach Protokollebene Filtern</span><span class="sxs-lookup"><span data-stu-id="f5613-173">Filter by log level</span></span>  

<span data-ttu-id="f5613-174">DevTools weist jeder `console.*` Methode einen Schweregrad zu.</span><span class="sxs-lookup"><span data-stu-id="f5613-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="f5613-175">Es gibt 4 Ebenen: `Verbose` , `Info` , `Warning` und `Error` .</span><span class="sxs-lookup"><span data-stu-id="f5613-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="f5613-176">Befindet sich beispielsweise `console.log()` in der `Info` Gruppe, während `console.error()` sich in der `Error` Gruppe befindet.</span><span class="sxs-lookup"><span data-stu-id="f5613-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="f5613-177">Die [API-Referenz][DevToolsConsoleApi] für die Konsole beschreibt den Schweregrad jeder anwendbaren Methode.</span><span class="sxs-lookup"><span data-stu-id="f5613-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="f5613-178">Jede Nachricht, die der Browser auf der Konsole anmeldet, hat auch einen Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="f5613-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="f5613-179">Sie können jede Ebene von Nachrichten verbergen, an denen Sie nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="f5613-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="f5613-180">Wenn Sie beispielsweise nur an `Error` Nachrichten interessiert sind, können Sie die anderen drei Gruppen ausblenden.</span><span class="sxs-lookup"><span data-stu-id="f5613-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="f5613-181">Klicken Sie auf die Dropdownliste **Protokollebenen** , um die Option oder `Verbose` `Info` `Warning` `Error` Nachrichten zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-181">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="f5613-183">Dropdownliste " **Protokollebenen** "</span><span class="sxs-lookup"><span data-stu-id="f5613-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="f5613-184">Sie können auch nach Protokollebene filtern, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar) und dann auf **Fehler**, **Warnungen**, **Informationen**oder **ausführlich**klicken.</span><span class="sxs-lookup"><span data-stu-id="f5613-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="f5613-186">Verwenden der Seitenleiste zum Anzeigen von Warnungen</span><span class="sxs-lookup"><span data-stu-id="f5613-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="f5613-187">Filtern von Nachrichten nach URL</span><span class="sxs-lookup"><span data-stu-id="f5613-187">Filter messages by URL</span></span>  

<span data-ttu-id="f5613-188">Geben `url:` Sie gefolgt von einer URL ein, um nur Nachrichten anzuzeigen, die von dieser URL stammen.</span><span class="sxs-lookup"><span data-stu-id="f5613-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="f5613-189">Nachdem Sie devtools eingegeben haben `url:` , werden alle relevanten URLs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5613-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="f5613-190">Domänen funktionieren ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="f5613-190">Domains also work.</span></span>  <span data-ttu-id="f5613-191">Wenn Sie beispielsweise `https://example.com/a.js` `https://example.com/b.js` Nachrichten protokollieren, `url:https://example.com` können Sie sich auf die Nachrichten aus diesen beiden Skripts konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="f5613-193">Ein URL-Filter</span><span class="sxs-lookup"><span data-stu-id="f5613-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="f5613-194">Geben `-url:` Sie ein, um Nachrichten aus dieser URL auszublenden.</span><span class="sxs-lookup"><span data-stu-id="f5613-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="f5613-195">Dies wird als negativer URL-Filter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f5613-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="f5613-197">Ein negativer URL-Filter, mit dem alle Nachrichten ausgeblendet werden, die der `https://b.wal.co` URL entsprechen</span><span class="sxs-lookup"><span data-stu-id="f5613-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="f5613-198">Sie können auch Nachrichten von einer einzelnen URL anzeigen, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar), den Abschnitt **Benutzer Nachrichten** erweitern und dann auf die URL des Skripts klicken, das die Nachrichten enthält, auf die Sie sich konzentrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f5613-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="f5613-200">Anzeigen der von Ihnen gelieferten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f5613-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="f5613-201">Filtern von Nachrichten aus unterschiedlichen Kontexten</span><span class="sxs-lookup"><span data-stu-id="f5613-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="f5613-202">Angenommen, Sie haben eine Anzeige \ (AD \) auf Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="f5613-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="f5613-203">Die Anzeige ist in eine eingebettete `<iframe>` und generiert viele Nachrichten in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="f5613-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="f5613-204">Da die Anzeige in einem anderen JavaScript- [Kontext](#select-javascript-context)ausgeführt wird, besteht eine Möglichkeit zum Ausblenden der Nachrichten darin, die [Konsoleneinstellungen zu öffnen](#open-console-settings) und das Kontrollkästchen **nur ausgewählten Kontext** zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="f5613-205">Filtern von Nachrichten, die nicht mit einem regulären Ausdrucksmuster übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="f5613-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="f5613-206">Geben Sie einen regulären Ausdruck wie `/[gm][ta][mi]/` im Textfeld **Filter** ein, um alle Nachrichten zu filtern, die nicht mit diesem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f5613-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="f5613-207">DevTools überprüft, ob das Muster im Nachrichtentext gefunden wurde, oder das Skript, das die Protokollierung der Nachricht verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f5613-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="f5613-209">Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` Regex-Ausdruck übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="f5613-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="f5613-210">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="f5613-210">Run JavaScript</span></span>  

<span data-ttu-id="f5613-211">Dieser Abschnitt enthält Features in Bezug auf die Ausführung von JavaScript in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="f5613-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="f5613-212">Eine praktische Exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="f5613-212">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="f5613-213">Erneutes Ausführen von Ausdrücken aus dem Protokoll</span><span class="sxs-lookup"><span data-stu-id="f5613-213">Re-run expressions from history</span></span>  

<span data-ttu-id="f5613-214">Drücken Sie die Eingabe `Up Arrow` Taste, um den Verlauf der JavaScript-Ausdrücke zu durchlaufen, die Sie zuvor in der Konsole ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="f5613-214">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="f5613-215">Wählen Sie diese Option aus, `Enter` um diesen Ausdruck erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f5613-215">Select `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="f5613-216">Überwachen des Werts eines Ausdrucks in Echtzeit mit Live Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="f5613-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="f5613-217">Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5613-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="f5613-218">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.</span><span class="sxs-lookup"><span data-stu-id="f5613-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="f5613-219">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f5613-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="f5613-220">Schauen Sie [sich die Werte für JavaScript-Ausdrücke in Real-Time mit Live Ausdrücken an][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="f5613-220">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="f5613-221">Deaktivieren der eifrigen Auswertung</span><span class="sxs-lookup"><span data-stu-id="f5613-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="f5613-222">Während Sie JavaScript-Ausdrücke in der Konsole eingeben, zeigt die **eifrige Auswertung** eine Vorschau des Rückgabewerts für diesen Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f5613-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="f5613-223">[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **eifrige Auswertung** , um die Vorschau des Rückgabewerts zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="f5613-224">Deaktivieren von AutoVervollständigen aus dem Protokoll</span><span class="sxs-lookup"><span data-stu-id="f5613-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="f5613-225">Wenn Sie einen Ausdruck eingeben, zeigt das Popupfenster AutoVervollständigen für die Konsole Ausdrücke an, die Sie zuvor ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="f5613-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="f5613-226">Diesen Ausdrücken wird das Zeichen vorangestellt `>` .</span><span class="sxs-lookup"><span data-stu-id="f5613-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="f5613-227">[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **AutoVervollständigen aus Verlauf** , um die Anzeige von Ausdrücken aus Ihrem Protokoll zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f5613-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="f5613-228">In der folgenden Abbildung `document.querySelector('a')` `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.</span><span class="sxs-lookup"><span data-stu-id="f5613-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="f5613-230">Das AutoVervollständigen-Popup zeigt Ausdrücke aus dem Protokoll an</span><span class="sxs-lookup"><span data-stu-id="f5613-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="f5613-231">JavaScript-Kontext auswählen</span><span class="sxs-lookup"><span data-stu-id="f5613-231">Select JavaScript context</span></span>  

<span data-ttu-id="f5613-232">Standardmäßig ist die Dropdownliste **JavaScript-Kontext** auf **oben**gesetzt, was den [Browserkontext][MDNBrowsingContext] des Hauptdokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5613-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="f5613-234">Die **JavaScript-Kontext** Dropdownliste</span><span class="sxs-lookup"><span data-stu-id="f5613-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="f5613-235">Angenommen, Sie haben eine Anzeige auf Ihrer Seite eingebettet in eine `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="f5613-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="f5613-236">Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="f5613-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="f5613-237">Wählen Sie zuerst den Browserkontext der Anzeige aus der Dropdownliste **JavaScript-Kontext** aus.</span><span class="sxs-lookup"><span data-stu-id="f5613-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="f5613-239">Auswählen eines anderen JavaScript-Kontexts</span><span class="sxs-lookup"><span data-stu-id="f5613-239">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="f5613-240">Deaktivieren der Konsole</span><span class="sxs-lookup"><span data-stu-id="f5613-240">Clear the Console</span></span>  

<span data-ttu-id="f5613-241">Sie können eine der folgenden Workflows verwenden, um die Konsole zu löschen:</span><span class="sxs-lookup"><span data-stu-id="f5613-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="f5613-242">Wählen Sie **Konsole löschen** ( ![ Konsole löschen ][ImageClearConsoleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="f5613-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="f5613-243">Klicken Sie mit der rechten Maustaste auf eine Nachricht, und wählen Sie **Konsole löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="f5613-243">Right-click a message and then choose **Clear Console**.</span></span>  
*   <span data-ttu-id="f5613-244">Geben Sie `clear()` in die Konsole ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f5613-244">Enter `clear()` in the Console and then select `Enter`.</span></span>  
*   <span data-ttu-id="f5613-245">Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.</span><span class="sxs-lookup"><span data-stu-id="f5613-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="f5613-246">Wählen Sie aus `Control` + `L` , während sich die Konsole im Fokus befindet.</span><span class="sxs-lookup"><span data-stu-id="f5613-246">Select `Control`+`L` while the Console is in focus.</span></span>  
    
## <span data-ttu-id="f5613-247">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f5613-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Anzeigen von protokollierten Nachrichten – Übersicht über die Konsole | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ausführen von JavaScript – Übersicht über die Konsole | Microsoft docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsole | Microsoft docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an | Microsoft docs"  
[DevToolsConsoleLog]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browsing-Kontext | MDN"  

> [!NOTE]
> <span data-ttu-id="f5613-257">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5613-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f5613-258">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5613-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f5613-260">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f5613-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
