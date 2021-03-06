---
description: Eine umfassende Referenz zu allen Features und Verhaltensweisen im Zusammenhang mit der Konsolenbenutzeroberfläche in Microsoft Edge DevTools.
title: Konsolenreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399162"
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

# <a name="console-reference"></a><span data-ttu-id="8f4c6-104">Konsolenreferenz</span><span class="sxs-lookup"><span data-stu-id="8f4c6-104">Console reference</span></span>  

<span data-ttu-id="8f4c6-105">Diese Seite ist ein Verweis auf Features im Zusammenhang mit der Microsoft Edge DevTools-Konsole.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="8f4c6-106">Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um protokollierte Nachrichten anzeigen und JavaScript ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="8f4c6-107">Wenn nicht, navigieren Sie zu [Erste Schritte mit der Ausführung von JavaScript in][DevToolsConsoleJavascript] der Konsole, und beginnen Sie mit der Protokollierung von Nachrichten in der [Konsole.][DevToolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="8f4c6-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="8f4c6-108">Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` suchen, navigieren Sie zu [Konsolen-API-Referenz][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="8f4c6-108">If you are looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="8f4c6-109">Für den Verweis auf Funktionen wie `monitorEvents()` navigieren Sie zu Console [Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="8f4c6-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="8f4c6-110">Öffnen der Konsole</span><span class="sxs-lookup"><span data-stu-id="8f4c6-110">Open the Console</span></span>  

<span data-ttu-id="8f4c6-111">Sie können die **Konsole** als Tool [im](#open-the-console-tool) oberen Bereich oder als Tool [in der Schublade öffnen.](#open-the-console-tool-in-the-drawer)</span><span class="sxs-lookup"><span data-stu-id="8f4c6-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="8f4c6-112">Öffnen des Konsolentools</span><span class="sxs-lookup"><span data-stu-id="8f4c6-112">Open the Console tool</span></span>  

<span data-ttu-id="8f4c6-113">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Das Konsolentool" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="8f4c6-115">Das **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="8f4c6-116">Wenn Sie das **Konsolentool** über [das][DevToolsCommandMenu]Befehlsmenü öffnen möchten, beginnen Sie mit der Eingabe, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Panel-Badge** daneben hat. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8f4c6-116">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Der Befehl zum Anzeigen des Konsolenbereichs" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="8f4c6-118">Der Befehl zum Anzeigen des **Konsolentools**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-118">The command to show the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="8f4c6-119">Öffnen Des Konsolentools in der Schublade</span><span class="sxs-lookup"><span data-stu-id="8f4c6-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="8f4c6-120">Wählen `Escape` Oder wählen Sie Anpassen und Steuern **DevTools** \( `...` \) und wählen Sie dann **Konsolenschubschubre anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Show console drawer" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="8f4c6-122">Show console drawer</span><span class="sxs-lookup"><span data-stu-id="8f4c6-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="8f4c6-123">Die Schublade wird unten im DevTools-Fenster angezeigt, und das **Konsolentool** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="8f4c6-125">Das **Konsolentool** in **der Schublade**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="8f4c6-126">Wenn Sie das **Konsolentool** über [das][DevToolsCommandMenu]Befehlsmenü öffnen möchten, beginnen Sie mit der Eingabe, und führen Sie dann den Befehl Konsole anzeigen aus, neben dem das `Console` **Drawer-Signal** steht. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8f4c6-126">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Der Befehl zum Anzeigen des **Console**-Tools in der Schublade" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="8f4c6-128">Der Befehl zum Anzeigen des **Konsolentools** in der **Schublade**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-128">The command to show the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="8f4c6-129">Öffnen von Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-129">Open Console Settings</span></span>  

<span data-ttu-id="8f4c6-130">Wählen **Sie Konsoleneinstellungen** \( ![ Symbol für Konsoleneinstellungen ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8f4c6-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Konsoleneinstellungen" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="8f4c6-132">Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="8f4c6-133">In den folgenden Links werden die einzelnen Einstellungen erläutert:</span><span class="sxs-lookup"><span data-stu-id="8f4c6-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="8f4c6-134">Netzwerk ausblenden</span><span class="sxs-lookup"><span data-stu-id="8f4c6-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="8f4c6-135">Protokoll beibehalten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="8f4c6-136">Nur ausgewählter Kontext</span><span class="sxs-lookup"><span data-stu-id="8f4c6-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="8f4c6-137">Gruppe ähnlich</span><span class="sxs-lookup"><span data-stu-id="8f4c6-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="8f4c6-138">Log XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="8f4c6-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="8f4c6-139">Begierde Auswertung</span><span class="sxs-lookup"><span data-stu-id="8f4c6-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="8f4c6-140">Autocomplete From History</span><span class="sxs-lookup"><span data-stu-id="8f4c6-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="8f4c6-141">Öffnen der Konsolenseite</span><span class="sxs-lookup"><span data-stu-id="8f4c6-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="8f4c6-142">Wählen **Sie Konsolenseite anzeigen** \( Konsolenseite anzeigen \) aus, um die Seitenleiste zu ![ ][ImageShowConsoleSidebarIcon] zeigen, die für die Filterung hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Konsolen-Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="8f4c6-144">**Konsole** Sidebar</span><span class="sxs-lookup"><span data-stu-id="8f4c6-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="8f4c6-145">Anzeigen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-145">View messages</span></span>  

<span data-ttu-id="8f4c6-146">Dieser Abschnitt enthält Features, die die Art und Weise ändern, wie Nachrichten in der Konsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="8f4c6-147">Eine praktische exemplarische Vorgehensweise finden Sie unter Anzeigen [von Nachrichten.][DevToolsConsoleViewMessages]</span><span class="sxs-lookup"><span data-stu-id="8f4c6-147">For a hands-on walkthrough, navigate to [View messages][DevToolsConsoleViewMessages].</span></span>  

### <a name="disable-message-grouping"></a><span data-ttu-id="8f4c6-148">Deaktivieren der Nachrichtengruppe</span><span class="sxs-lookup"><span data-stu-id="8f4c6-148">Disable message grouping</span></span>  

<span data-ttu-id="8f4c6-149">[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie **"Gruppe", um** das Standardmäßige Nachrichtengruppenverhalten der Konsole zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="8f4c6-150">Navigieren Sie beispielsweise zu [Log XHR und Fetch requests](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="8f4c6-150">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="8f4c6-151">Protokollierung von XHR- und Fetch-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="8f4c6-152">[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie **Log XMLHttpRequests,** um alle und Anforderungen an die Konsole zu `XMLHttpRequest` `Fetch` protokollieren.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Protokollieren von XMLHttpRequest- und Fetch-Anforderungen" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="8f4c6-154">Protokoll `XMLHttpRequest` und `Fetch` Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="8f4c6-155">In der oberen Meldung in der vorherigen Abbildung wird das Standardgruppenverhalten der **Konsole angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="8f4c6-156">Beibehalten von Nachrichten über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="8f4c6-156">Persist messages across page loads</span></span>  

<span data-ttu-id="8f4c6-157">Standardmäßig wird die Konsole beim Laden einer neuen Seite deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="8f4c6-158">Um Nachrichten über Seitenlasten hinweg zu speichern, [öffnen Sie Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie dann das **Kontrollkästchen Protokoll** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="8f4c6-159">Ausblenden von Netzwerknachrichten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-159">Hide network messages</span></span>  

<span data-ttu-id="8f4c6-160">Standardmäßig protokolliert der Browser Netzwerknachrichten an die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="8f4c6-161">In der folgenden Abbildung stellt die ausgewählte Nachricht den HTTP-Statuscode von `429` dar.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Eine 429-Nachricht in der Konsole" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="8f4c6-163">Eine `429` Nachricht in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="8f4c6-164">So blenden Sie Netzwerknachrichten aus:</span><span class="sxs-lookup"><span data-stu-id="8f4c6-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="8f4c6-165">[Öffnen Sie Konsoleneinstellungen](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="8f4c6-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="8f4c6-166">Aktivieren Sie **das Kontrollkästchen Netzwerk** ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="8f4c6-167">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-167">Filter messages</span></span>  

<span data-ttu-id="8f4c6-168">Es gibt viele Möglichkeiten, Nachrichten in der Konsole herausfiltern.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-168">There are many ways to filter out messages in the Console.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="8f4c6-169">Filtern von Browsernachrichten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-169">Filter out browser messages</span></span>  

<span data-ttu-id="8f4c6-170">[Öffnen Sie die Konsolen-Seitenleiste,](#open-the-console-sidebar) und wählen Sie **Benutzernachrichten aus,** um nur Nachrichten aus dem JavaScript der Seite anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Anzeigen von Benutzernachrichten" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="8f4c6-172">Anzeigen von Benutzernachrichten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-172">View user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="8f4c6-173">Filtern nach Protokollebene</span><span class="sxs-lookup"><span data-stu-id="8f4c6-173">Filter by log level</span></span>  

<span data-ttu-id="8f4c6-174">DevTools weist jeder `console.*` Methode einen Schweregrad zu.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="8f4c6-175">Es gibt 4 Ebenen: `Verbose` `Info` , , und `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="8f4c6-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="8f4c6-176">Befindet sich `console.log()` z. B. in `Info` der Gruppe, während sie sich in der `console.error()` Gruppe `Error` befindet.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="8f4c6-177">Die [Konsolen-API-Referenz][DevToolsConsoleApi] beschreibt den Schweregrad jeder anwendbaren Methode.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="8f4c6-178">Jede Nachricht, die der Browser bei der Konsole anmeldet, hat auch einen Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="8f4c6-179">Sie können eine beliebige Ebene von Nachrichten ausblenden, an der Sie nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="8f4c6-180">Wenn Sie beispielsweise nur an Nachrichten interessiert sind, können Sie die anderen `Error` 3 Gruppen ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="8f4c6-181">Wählen Sie **das Dropdownmenü Protokollebenen** aus, um Nachrichten zu aktivieren `Verbose` oder zu `Info` `Warning` `Error` deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-181">Choose the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Dropdownliste "Protokollebenen"" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="8f4c6-183">Dropdownliste **"Protokollebenen"**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="8f4c6-184">Sie können auch nach Protokollebene filtern, indem Sie die [Konsolenseite öffnen](#open-the-console-sidebar) und dann **Fehler,** **Warnungen,** **Info**oder **Verbose öffnen.**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and thenchoosing **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Anzeigen von Warnungen mithilfe der Seitenleiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="8f4c6-186">Anzeigen von Warnungen mithilfe der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="8f4c6-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="8f4c6-187">Filtern von Nachrichten nach URL</span><span class="sxs-lookup"><span data-stu-id="8f4c6-187">Filter messages by URL</span></span>  

<span data-ttu-id="8f4c6-188">Geben Sie eine URL ein, um nur Nachrichten anzeigen zu `url:` können, die von dieser URL stammten.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="8f4c6-189">Nachdem Sie `url:` DevTools eingeben, werden alle relevanten URLs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="8f4c6-190">Domänen funktionieren auch.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-190">Domains also work.</span></span>  <span data-ttu-id="8f4c6-191">Wenn beispielsweise Nachrichten protokollieren und diese protokollieren, können Sie sich auf die Nachrichten aus diesen `https://example.com/a.js` `https://example.com/b.js` `url:https://example.com` 2 Skripts konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Ein URL-Filter" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="8f4c6-193">Ein URL-Filter</span><span class="sxs-lookup"><span data-stu-id="8f4c6-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="8f4c6-194">Geben `-url:` Sie ein, um Nachrichten aus dieser URL auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="8f4c6-195">Dies wird als negativer URL-Filter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der https://b.wal.co URL übereinstimmen" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="8f4c6-197">Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der `https://b.wal.co` URL übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="8f4c6-198">Sie können auch Nachrichten von einer einzelnen URL anzeigen, \*\*\*\* indem Sie die Konsolenseite [öffnen,](#open-the-console-sidebar)den Abschnitt Benutzernachrichten erweitern und dann die URL des Skripts mit den Nachrichten angeben, auf die Sie sich konzentrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and thenchoosing the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Anzeigen der Nachrichten, die von der wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="8f4c6-200">Anzeigen der Nachrichten, die von</span><span class="sxs-lookup"><span data-stu-id="8f4c6-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="8f4c6-201">Filtern von Nachrichten aus unterschiedlichen Kontexten</span><span class="sxs-lookup"><span data-stu-id="8f4c6-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="8f4c6-202">Angenommen, Sie haben eine Ankündigung \(ad\) auf Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="8f4c6-203">Die Anzeige ist in eine eingebettet `<iframe>` und generiert viele Nachrichten in Ihrer Konsole.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="8f4c6-204">Da die Anzeige in einem anderen [JavaScript-Kontext](#select-javascript-context)ausgeführt wird, besteht eine Möglichkeit \*\*\*\* zum Ausblenden der Nachrichten im Öffnen von Konsoleneinstellungen und Aktivieren des Kontrollkästchens Nur ausgewählter Kontext. [](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="8f4c6-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and turn on the **Selected Context Only** checkbox.</span></span>  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a><span data-ttu-id="8f4c6-205">Filtern von Nachrichten, die nicht mit einem Muster für reguläre Ausdrücke übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="8f4c6-206">Geben Sie einen regulären Ausdruck ein, z. B. in das Textfeld Filter, um alle Nachrichten herausfiltern, `/[gm][ta][mi]/` die nicht mit diesem Muster übereinstimmen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8f4c6-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="8f4c6-207">DevTools überprüft, ob das Muster im Nachrichtentext oder im Skript gefunden wird, das dazu führte, dass die Nachricht protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtern von Nachrichten, die nicht mit dem regex-Ausdruck übereinstimmen" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="8f4c6-209">Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` regex-Ausdruck übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="8f4c6-210">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="8f4c6-210">Run JavaScript</span></span>  

<span data-ttu-id="8f4c6-211">Dieser Abschnitt enthält Features im Zusammenhang mit der Ausführung von JavaScript in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="8f4c6-212">Eine praktische exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevToolsConsoleOverviewJavascript].</span><span class="sxs-lookup"><span data-stu-id="8f4c6-212">For a hands-on walkthrough, navigate to [Run JavaScript][DevToolsConsoleOverviewJavascript].</span></span>  

### <a name="re-run-expressions-from-history"></a><span data-ttu-id="8f4c6-213">Erneutes Ausführen von Ausdrücken aus dem Verlauf</span><span class="sxs-lookup"><span data-stu-id="8f4c6-213">Re-run expressions from history</span></span>  

<span data-ttu-id="8f4c6-214">Wählen Sie den Schlüssel aus, um den Verlauf von JavaScript-Ausdrücken zu durchschreiben, die Sie `Up Arrow` zuvor in der Konsole verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-214">Select the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="8f4c6-215">Wählen `Enter` Sie diese Option aus, um den Ausdruck erneut ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-215">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="8f4c6-216">Beobachten des Werts eines Ausdrucks in Echtzeit mit Liveausdrücken</span><span class="sxs-lookup"><span data-stu-id="8f4c6-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="8f4c6-217">Wenn Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="8f4c6-218">Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein undheften ihn dann an den oberen Rand der Konsole.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="8f4c6-219">Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="8f4c6-220">Navigieren Sie [zu JavaScript Expression Values in Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="8f4c6-220">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="disable-eager-evaluation"></a><span data-ttu-id="8f4c6-221">Deaktivieren der Begierdeauswertung</span><span class="sxs-lookup"><span data-stu-id="8f4c6-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="8f4c6-222">Wenn Sie In-JavaScript-Ausdrücke in der Konsole eingeben, zeigt die Bewertung mit **Begierde** eine Vorschau des Rückgabewerts für diesen Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="8f4c6-223">[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie das Kontrollkästchen Bewertungsgierig, um die Rückgabewertvorschauen zu deaktivieren. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8f4c6-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <a name="disable-autocomplete-from-history"></a><span data-ttu-id="8f4c6-224">Deaktivieren des automatischen Kompletierens aus dem Verlauf</span><span class="sxs-lookup"><span data-stu-id="8f4c6-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="8f4c6-225">Beim Eingeben eines Ausdrucks zeigt das Popupfenster für die automatische Vervollständigung für die Konsole Ausdrücke an, die Sie zuvor durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="8f4c6-226">Diese Ausdrücke werden mit dem Zeichen `>` vorkonfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="8f4c6-227">[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie das Kontrollkästchen **AutoComplete From History,** um die Anzeige von Ausdrücken aus Ihrem Verlauf zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="8f4c6-228">In der folgenden Abbildung `document.querySelector('a')` und `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Im Popup für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt." lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="8f4c6-230">Im Popup für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <a name="select-javascript-context"></a><span data-ttu-id="8f4c6-231">Auswählen des JavaScript-Kontexts</span><span class="sxs-lookup"><span data-stu-id="8f4c6-231">Select JavaScript context</span></span>  

<span data-ttu-id="8f4c6-232">Standardmäßig ist das **JavaScript-Kontextdropdown** auf **top**festgelegt, das den [Browserkontext][MDNBrowsingContext] des Hauptdokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Das Dropdownmenü "JavaScript-Kontext"" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="8f4c6-234">Das **Dropdownmenü "JavaScript-Kontext"**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="8f4c6-235">Angenommen, Sie haben eine Anzeige auf Ihrer Seite eingebettet in `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="8f4c6-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="8f4c6-236">Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="8f4c6-237">Sie sollten zuerst den Browserkontext der Anzeige im **Dropdownmenü JavaScript-Kontext** auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Auswählen eines anderen JavaScript-Kontexts" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="8f4c6-239">Auswählen eines anderen JavaScript-Kontexts</span><span class="sxs-lookup"><span data-stu-id="8f4c6-239">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="8f4c6-240">Löschen der Konsole</span><span class="sxs-lookup"><span data-stu-id="8f4c6-240">Clear the Console</span></span>  

<span data-ttu-id="8f4c6-241">Sie können einen der folgenden Workflows verwenden, um die Konsole zu löschen:</span><span class="sxs-lookup"><span data-stu-id="8f4c6-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="8f4c6-242">Wählen **Sie Clear Console** \( Clear Console ![ ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8f4c6-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="8f4c6-243">Zeigen Sie auf eine Nachricht, öffnen Sie das Kontextmenü \(righ-click\), und wählen Sie **Konsole löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="8f4c6-243">Hover on a message, open the contextual menu \(righ-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="8f4c6-244">Geben `clear()` Sie in die Konsole **ein,** und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-244">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="8f4c6-245">Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="8f4c6-246">Wählen `Control` + `L` Sie **aus, während sich die Konsole** im Fokus befindet.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-246">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8f4c6-247">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8f4c6-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Anzeigen protokollierter Nachrichten – Übersicht über | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ausführen von JavaScript – Übersicht über | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Verfolgen Sie JavaScript-Ausdruckswerte in Echtzeit mit Live Expressions | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browserkontext | MDN"  

> [!NOTE]
> <span data-ttu-id="8f4c6-257">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8f4c6-258">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="8f4c6-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8f4c6-260">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f4c6-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
