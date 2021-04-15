---
description: Eine umfassende Referenz für jedes Feature und Verhalten der Konsolenbenutzeroberfläche in Microsoft Edge DevTools.
title: Konsolenreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: adc3f6c33d6e1a2f6c7db8336c5ab803e76c3307
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483269"
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
# <a name="console-reference"></a><span data-ttu-id="8df24-104">Konsolenreferenz</span><span class="sxs-lookup"><span data-stu-id="8df24-104">Console reference</span></span>  

<span data-ttu-id="8df24-105">Dieser Artikel ist eine Referenz zu Features im Zusammenhang mit der Microsoft Edge DevTools-Konsole.</span><span class="sxs-lookup"><span data-stu-id="8df24-105">This article is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="8df24-106">Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um protokollierte Nachrichten anzeigen und JavaScript ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8df24-106">It assumes you're already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="8df24-107">Wenn nicht, navigieren Sie zu [Erste Schritte mit der Ausführung von JavaScript in][DevtoolsConsoleConsoleJavascript] der Konsole und Erste Schritte mit der [Protokollierung von Nachrichten in der Konsole][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="8df24-107">If not, navigate to [Get started with running JavaScript in the Console][DevtoolsConsoleConsoleJavascript] and [Get started with logging messages in the Console][DevtoolsConsoleConsoleLog].</span></span>  

<span data-ttu-id="8df24-108">Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` suchen, navigieren Sie zu [Konsolen-API-Referenz][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="8df24-108">If you're looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="8df24-109">Für den Verweis auf Funktionen wie `monitorEvents()` navigieren Sie zu Console [Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="8df24-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="8df24-110">Öffnen der Konsole</span><span class="sxs-lookup"><span data-stu-id="8df24-110">Open the Console</span></span>  

<span data-ttu-id="8df24-111">Sie können die **Konsole** als Tool [im](#open-the-console-tool) oberen Bereich oder als Tool [in der Schublade öffnen.](#open-the-console-tool-in-the-drawer)</span><span class="sxs-lookup"><span data-stu-id="8df24-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="8df24-112">Öffnen des Konsolentools</span><span class="sxs-lookup"><span data-stu-id="8df24-112">Open the Console tool</span></span>  

<span data-ttu-id="8df24-113">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Das Konsolentool" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="8df24-115">Das **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="8df24-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-116">Um das **Konsolentool** im [Befehlsmenü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie den Befehl Konsole anzeigen ein, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Panel-Badge** daneben hat. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8df24-116">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ausführen des Befehls zum Anzeigen des Konsolentools" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="8df24-118">Ausführen des Befehls zum Anzeigen des **Konsolentools**</span><span class="sxs-lookup"><span data-stu-id="8df24-118">Run the command to display the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="8df24-119">Öffnen Des Konsolentools in der Schublade</span><span class="sxs-lookup"><span data-stu-id="8df24-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="8df24-120">Wählen `Esc` Oder wählen Sie Anpassen und Steuern **DevTools** \( `...` \) und wählen Sie dann **Konsolenschubschubre anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="8df24-120">Select `Esc` or choose **Customize and control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Show console drawer" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="8df24-122">Show console drawer</span><span class="sxs-lookup"><span data-stu-id="8df24-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="8df24-123">Die Schublade wird unten im DevTools-Fenster angezeigt, und das **Konsolentool** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8df24-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="8df24-125">Das **Konsolentool** in **der Schublade**</span><span class="sxs-lookup"><span data-stu-id="8df24-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-126">Um das **Konsolentool** im Befehlsmenü zu [öffnen,][DevtoolsCommandMenuIndex]geben Sie den Befehl Konsole anzeigen ein, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Drawer-Badge** daneben hat. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8df24-126">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Führen Sie den Befehl aus, um das Tool **Console** in der Schublade anzeigen zu können." lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="8df24-128">Ausführen des Befehls zum Anzeigen des **Konsolentools** in der **Schublade**</span><span class="sxs-lookup"><span data-stu-id="8df24-128">Run the command to display the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="8df24-129">Öffnen von Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8df24-129">Open Console Settings</span></span>  

<span data-ttu-id="8df24-130">Wählen Sie **die Schaltfläche Konsoleneinstellungen** \( ![ Symbol für ](../media/settings-button-icon.msft.png) Konsoleneinstellungen \) aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-130">Choose the **Console Settings** \(![Console Settings icon](../media/settings-button-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Konsoleneinstellungen" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="8df24-132">Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="8df24-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="8df24-133">In den folgenden Links werden die einzelnen Einstellungen erläutert.</span><span class="sxs-lookup"><span data-stu-id="8df24-133">The following links explain each setting.</span></span>  

*   [<span data-ttu-id="8df24-134">Netzwerk ausblenden</span><span class="sxs-lookup"><span data-stu-id="8df24-134">Hide network</span></span>](#hide-network-messages)  
*   [<span data-ttu-id="8df24-135">Protokoll beibehalten</span><span class="sxs-lookup"><span data-stu-id="8df24-135">Preserve log</span></span>](#persist-messages-across-page-loads)  
*   [<span data-ttu-id="8df24-136">Nur ausgewählter Kontext</span><span class="sxs-lookup"><span data-stu-id="8df24-136">Selected context only</span></span>](#filter-out-messages-from-different-contexts)  
*   [<span data-ttu-id="8df24-137">Gruppe ähnlich</span><span class="sxs-lookup"><span data-stu-id="8df24-137">Group similar</span></span>](#turn-off-message-grouping)  
*   [<span data-ttu-id="8df24-138">Protokoll-XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="8df24-138">Log XMLHttpRequests</span></span>](#log-xhr-and-fetch-requests)  
*   [<span data-ttu-id="8df24-139">Begierde Auswertung</span><span class="sxs-lookup"><span data-stu-id="8df24-139">Eager evaluation</span></span>](#turn-off-eager-evaluation)  
*   [<span data-ttu-id="8df24-140">AutoComplete aus dem Verlauf</span><span class="sxs-lookup"><span data-stu-id="8df24-140">Autocomplete from history</span></span>](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="8df24-141">Öffnen der Konsolenseite</span><span class="sxs-lookup"><span data-stu-id="8df24-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="8df24-142">Zum Anzeigen der **Seitenleiste**wählen Sie **Konsolenseiteleiste anzeigen** \( ![ Konsolenseiteleiste ](../media/show-console-sidebar-icon.msft.png) anzeigen \).</span><span class="sxs-lookup"><span data-stu-id="8df24-142">To display the **Sidebar**, choose **Show console sidebar** \(![Show console sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  <span data-ttu-id="8df24-143">Die **Sidebar** hilft Ihnen beim Filtern.</span><span class="sxs-lookup"><span data-stu-id="8df24-143">The **Sidebar** is helps you filter.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Konsolen-Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **<span data-ttu-id="8df24-145">Konsolen-Sidebar</span><span class="sxs-lookup"><span data-stu-id="8df24-145">Console Sidebar</span></span>**  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="8df24-146">Anzeigen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8df24-146">View messages</span></span>  

<span data-ttu-id="8df24-147">Dieser Abschnitt enthält Features, die die Art und Weise ändern, wie Nachrichten in der Konsole angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8df24-147">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="8df24-148">Eine praktische exemplarische Vorgehensweise finden Sie unter Anzeigen [von Nachrichten.][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]</span><span class="sxs-lookup"><span data-stu-id="8df24-148">For a hands-on walkthrough, navigate to [View messages][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span></span>  

### <a name="turn-off-message-grouping"></a><span data-ttu-id="8df24-149">Deaktivieren der Nachrichtengruppe</span><span class="sxs-lookup"><span data-stu-id="8df24-149">Turn off message grouping</span></span>  

<span data-ttu-id="8df24-150">Wenn Sie das Standardmäßige Nachrichtengruppenverhalten der Konsole deaktivieren **möchten,** öffnen Sie [Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie das Kontrollkästchen neben Ähnlich **gruppieren.**</span><span class="sxs-lookup"><span data-stu-id="8df24-150">To turn off the default message grouping behavior of the **Console**, [open Console Settings](#open-console-settings) and choose the checkbox next to **Group similar**.</span></span>  <span data-ttu-id="8df24-151">Navigieren Sie beispielsweise zu [Log XHR und Fetch requests](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="8df24-151">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="8df24-152">Protokollierung von XHR- und Fetch-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df24-152">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="8df24-153">Öffnen Sie konsoleneinstellungen, und wählen Sie das Kontrollkästchen neben `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**aus, \*\*\*\* [](#open-console-settings) um alle Und Anforderungen an die Konsole zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="8df24-153">To log all `XMLHttpRequest` and `Fetch` requests to the **Console** as each happens, [open Console Settings](#open-console-settings) and choose the checkbox next to **Log XMLHttpRequests**.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Protokollieren von XMLHttpRequest- und Fetch-Anforderungen" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="8df24-155">Protokoll `XMLHttpRequest` und `Fetch` Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df24-155">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-156">In der oberen Meldung in der vorherigen Abbildung wird das Standardgruppenverhalten der **Konsole angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="8df24-156">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="8df24-157">Beibehalten von Nachrichten über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="8df24-157">Persist messages across page loads</span></span>  

<span data-ttu-id="8df24-158">Wenn Sie eine neue Webseite laden, wird die Konsole mit der Standardaktion **deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8df24-158">When you load a new webpage, the default action clears the **Console**.</span></span>  <span data-ttu-id="8df24-159">Um Nachrichten über Seitenlasten hinweg zu speichern, [öffnen Sie Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie das Kontrollkästchen neben **Protokoll beibehalten**.</span><span class="sxs-lookup"><span data-stu-id="8df24-159">To persist messages across page loads, [open Console Settings](#open-console-settings) and choose the checkbox next to **Preserve Log**.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="8df24-160">Ausblenden von Netzwerknachrichten</span><span class="sxs-lookup"><span data-stu-id="8df24-160">Hide network messages</span></span>  

<span data-ttu-id="8df24-161">Die Standardaktion für Microsoft Edge besteht im Protokollieren von Netzwerknachrichten an der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="8df24-161">The default action for Microsoft Edge is to logs network messages to the **Console**.</span></span>  <span data-ttu-id="8df24-162">In der folgenden Abbildung stellt die ausgewählte Nachricht den HTTP-Statuscode von `429` dar.</span><span class="sxs-lookup"><span data-stu-id="8df24-162">In the following figure, the chosen message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Eine 429-Nachricht in der Konsole" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="8df24-164">Eine `429` Nachricht in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="8df24-164">A `429` message in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-165">Führen Sie die folgenden Aktionen aus, um Netzwerknachrichten auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8df24-165">To hide network messages, complete the following actions.</span></span>  

1.  <span data-ttu-id="8df24-166">[Öffnen Sie Konsoleneinstellungen](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="8df24-166">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="8df24-167">Aktivieren Sie das Kontrollkästchen neben **Netzwerk ausblenden**.</span><span class="sxs-lookup"><span data-stu-id="8df24-167">Choose the checkbox next to **Hide Network**.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="8df24-168">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8df24-168">Filter messages</span></span>  

<span data-ttu-id="8df24-169">Es gibt viele Möglichkeiten zum Filtern von Nachrichten in der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="8df24-169">Many ways exist to filter out messages in the **Console**.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="8df24-170">Filtern von Browsernachrichten</span><span class="sxs-lookup"><span data-stu-id="8df24-170">Filter out browser messages</span></span>  

<span data-ttu-id="8df24-171">[Öffnen Sie die Konsolenseite,](#open-the-console-sidebar) und wählen Sie **# Benutzernachrichten aus,** um nur Nachrichten anzuzeigen, die aus dem JavaScript der Webseite stammten.</span><span class="sxs-lookup"><span data-stu-id="8df24-171">[Open the Console Sidebar](#open-the-console-sidebar) and choose **# user messages** to only display messages that came from the JavaScript of the webpage.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Anzeigen von Benutzernachrichten" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="8df24-173">Anzeigen von Benutzernachrichten</span><span class="sxs-lookup"><span data-stu-id="8df24-173">Display user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="8df24-174">Filtern nach Protokollebene</span><span class="sxs-lookup"><span data-stu-id="8df24-174">Filter by log level</span></span>  

<span data-ttu-id="8df24-175">DevTools weist jeder `console.*` Methode eine der vier Schweregrade zu.</span><span class="sxs-lookup"><span data-stu-id="8df24-175">DevTools assigns each `console.*` method one of the four severity levels.</span></span>  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
<span data-ttu-id="8df24-176">Befindet sich `console.log()` z. B. in der `Info` Gruppe, befindet `console.error()` sich jedoch in der `Error` Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8df24-176">For example, `console.log()` is in the `Info` group, but `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="8df24-177">Die [Konsolen-API-Referenz][DevToolsConsoleApi] beschreibt den Schweregrad jeder anwendbaren Methode.</span><span class="sxs-lookup"><span data-stu-id="8df24-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="8df24-178">Jede Nachricht, die der Browser bei der Konsole anmeldet, hat auch einen Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="8df24-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="8df24-179">Sie können eine beliebige Ebene von Nachrichten ausblenden, an der Sie nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="8df24-179">You may hide any level of messages that you're not interested in.</span></span>  <span data-ttu-id="8df24-180">Wenn Sie beispielsweise nur an Nachrichten interessiert sind, können Sie die anderen `Error` drei Gruppen ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8df24-180">For example, if you're only interested in `Error` messages, you may hide the other three groups.</span></span>  

<span data-ttu-id="8df24-181">Wählen Sie zum Filtern der Nachrichten das **Dropdownmenü Protokollebenen** aus, und wählen Sie `Verbose` , , oder `Info` `Warning` `Error` aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-181">To filter the messages, choose the **Log Levels** dropdown and choose `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Dropdownliste "Protokollebenen"" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="8df24-183">Dropdownliste **"Protokollebenen"**</span><span class="sxs-lookup"><span data-stu-id="8df24-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-184">Um die Protokollebene zum Filtern zu verwenden, öffnen Sie die [Konsolen-Seitenleiste,](#open-the-console-sidebar) und wählen Sie dann **Fehler,** **Warnungen,** **Info**oder **Verbose aus.**</span><span class="sxs-lookup"><span data-stu-id="8df24-184">To use the log level to filter, [open the Console Sidebar](#open-the-console-sidebar) and then choose **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Anzeigen von Warnungen mithilfe der Seitenleiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="8df24-186">Anzeigen von Warnungen mithilfe der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="8df24-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="8df24-187">Filtern von Nachrichten nach URL</span><span class="sxs-lookup"><span data-stu-id="8df24-187">Filter messages by URL</span></span>  

<span data-ttu-id="8df24-188">Geben Sie eine URL ein, um nur Nachrichten anzeigen zu `url:` können, die von dieser URL stammten.</span><span class="sxs-lookup"><span data-stu-id="8df24-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="8df24-189">Nach der Eingabe `url:` zeigt DevTools alle relevanten URLs an.</span><span class="sxs-lookup"><span data-stu-id="8df24-189">After you type `url:`, DevTools displays all relevant URLs.</span></span>  <span data-ttu-id="8df24-190">Domänen funktionieren auch.</span><span class="sxs-lookup"><span data-stu-id="8df24-190">Domains also work.</span></span>  <span data-ttu-id="8df24-191">Wenn beispielsweise Nachrichten protokollieren und diese protokollieren, können Sie sich auf die Nachrichten `https://example.com/a.js` `https://example.com/b.js` aus diesen beiden `url:https://example.com` Skripts konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="8df24-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` allows you to focus on the messages from these two scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Ein URL-Filter" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="8df24-193">Ein URL-Filter</span><span class="sxs-lookup"><span data-stu-id="8df24-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-194">Geben Sie ein, um Nachrichten aus einer URL `-url:` auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8df24-194">To hide messages from a URL, type `-url:`.</span></span>  <span data-ttu-id="8df24-195">Es ist ein negativer URL-Filter.</span><span class="sxs-lookup"><span data-stu-id="8df24-195">It's a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der https://b.wal.co URL übereinstimmen" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="8df24-197">Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der `https://b.wal.co` URL übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="8df24-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="8df24-198">Führen Sie zum Anzeigen von Nachrichten von einer einzelnen URL die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-198">To display messages from a single URL, complete the following actions.</span></span>  

1.  <span data-ttu-id="8df24-199">[Öffnen Sie die Konsolenseitenleiste](#open-the-console-sidebar).</span><span class="sxs-lookup"><span data-stu-id="8df24-199">[Open the Console Sidebar](#open-the-console-sidebar).</span></span>  
1.  <span data-ttu-id="8df24-200">Erweitern Sie den **Abschnitt # Benutzernachrichten.**</span><span class="sxs-lookup"><span data-stu-id="8df24-200">Expand the **# user messages** section.</span></span>  
1.  <span data-ttu-id="8df24-201">Wählen Sie die URL des Skripts aus, das die Nachrichten enthält, auf die Sie sich konzentrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8df24-201">Choose the URL of the script that contains the messages on which you want to focus.</span></span>  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Anzeigen der Nachrichten, die von der wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="8df24-203">Anzeigen der Nachrichten, die von</span><span class="sxs-lookup"><span data-stu-id="8df24-203">Display the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="8df24-204">Filtern von Nachrichten aus unterschiedlichen Kontexten</span><span class="sxs-lookup"><span data-stu-id="8df24-204">Filter out messages from different contexts</span></span>  

<span data-ttu-id="8df24-205">Angenommen, Sie haben eine Ankündigung \(ad\) auf Ihrer Webseite.</span><span class="sxs-lookup"><span data-stu-id="8df24-205">Suppose that you have an advertisement \(ad\) on your webpage.</span></span>  <span data-ttu-id="8df24-206">Die Anzeige ist in eine eingebettet `<iframe>` und generiert viele Nachrichten in Ihrer **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="8df24-206">The ad is embedded in an `<iframe>` and generates many messages in your **Console**.</span></span>  <span data-ttu-id="8df24-207">Da die Anzeige in einem anderen [JavaScript-Kontext](#choose-javascript-context)ausgeführt wird, besteht eine Möglichkeit zum Ausblenden der Nachrichten in dem Öffnen von Konsoleneinstellungen und dem Aktivieren des Kontrollkästchens neben Nur ausgewählter **Kontext**. [](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="8df24-207">Because the ad is running in a different [JavaScript context](#choose-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and choose the checkbox next to **Selected Context Only**.</span></span>  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a><span data-ttu-id="8df24-208">Filtern von Nachrichten, die keinem Muster für reguläre Ausdrücke entsprechen</span><span class="sxs-lookup"><span data-stu-id="8df24-208">Filter out messages that don't match a regular expression pattern</span></span>  

<span data-ttu-id="8df24-209">Geben Sie einen regulären Ausdruck wie z. B. in das Textfeld Filter ein, um alle Nachrichten herausfiltern, die nicht `/[gm][ta][mi]/` mit diesem Muster übereinstimmen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8df24-209">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** textbox to filter out any messages that don't match that pattern.</span></span>  <span data-ttu-id="8df24-210">DevTools überprüft, ob das Muster im Nachrichtentext oder im Skript gefunden wird, das dazu führte, dass die Nachricht protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="8df24-210">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtern von Nachrichten, die nicht mit dem regex-Ausdruck übereinstimmen" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="8df24-212">Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` regex-Ausdruck übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="8df24-212">Filter out any messages that don't match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="8df24-213">Ausführen von JavaScript</span><span class="sxs-lookup"><span data-stu-id="8df24-213">Run JavaScript</span></span>  

<span data-ttu-id="8df24-214">Dieser Abschnitt enthält Features im Zusammenhang mit der Ausführung von JavaScript in der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="8df24-214">This section contains features related to running JavaScript in the **Console**.</span></span>  <span data-ttu-id="8df24-215">Eine praktische exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="8df24-215">For a hands-on walkthrough, navigate to [Run JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  

### <a name="rerun-expressions-from-history"></a><span data-ttu-id="8df24-216">Erneutes Ausführen von Ausdrücken aus dem Verlauf</span><span class="sxs-lookup"><span data-stu-id="8df24-216">Rerun expressions from history</span></span>  

<span data-ttu-id="8df24-217">Wählen `Up Arrow` Sie diese Option aus, um den Verlauf von JavaScript-Ausdrücken zu durchschreiben, die Sie zuvor in der Konsole verwendet **haben.**</span><span class="sxs-lookup"><span data-stu-id="8df24-217">Select `Up Arrow` to cycle through the history of JavaScript expressions that you ran earlier in the **Console**.</span></span>  <span data-ttu-id="8df24-218">Wählen `Enter` Sie diese Option aus, um den Ausdruck erneut ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8df24-218">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="8df24-219">Beobachten des Werts eines Ausdrucks in Echtzeit mit Live-Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="8df24-219">Watch the value of an expression in real time with Live Expressions</span></span>  

<span data-ttu-id="8df24-220">Wenn Sie denselben JavaScript-Ausdruck wiederholt \*\*\*\* in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="8df24-220">If you find yourself typing the same JavaScript expression in the **Console** repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="8df24-221">Mit **Live-Ausdrücken**geben Sie einen Ausdruck einmal ein und an den oberen Rand der **Konsole an.**</span><span class="sxs-lookup"><span data-stu-id="8df24-221">With **Live Expressions**, you type an expression once and then pin it to the top of your **Console**.</span></span>  <span data-ttu-id="8df24-222">Der Wert des Ausdrucks wird in nahezu Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8df24-222">The value of the expression updates in near real time.</span></span>  <span data-ttu-id="8df24-223">Navigieren Sie [zu JavaScript Expression Values in Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="8df24-223">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="turn-off-eager-evaluation"></a><span data-ttu-id="8df24-224">Deaktivieren der Bewertung von "Begierig"</span><span class="sxs-lookup"><span data-stu-id="8df24-224">Turn off Eager Evaluation</span></span>  

<span data-ttu-id="8df24-225">**Bei der** Begierdeauswertung wird eine Vorschau des Rückgabewerts angezeigt, während Sie In-JavaScript-Ausdrücke in der **Konsole eingeben.**</span><span class="sxs-lookup"><span data-stu-id="8df24-225">**Eager Evaluation** displays a preview of the return value as you type JavaScript expressions in the **Console**.</span></span>  <span data-ttu-id="8df24-226">Führen Sie die folgenden Aktionen aus, um die Vorschau des Rückgabewerts zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8df24-226">To turn off the return value previews, complete the following actions.</span></span>  

1.  <span data-ttu-id="8df24-227">[Öffnen Sie Konsoleneinstellungen](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="8df24-227">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="8df24-228">Entfernen Sie das Kontrollkästchen neben **Bewertung mit Begierde**.</span><span class="sxs-lookup"><span data-stu-id="8df24-228">Remove the checkbox next to **Eager Evaluation**.</span></span>  
    
### <a name="turn-off-autocomplete-from-history"></a><span data-ttu-id="8df24-229">Deaktivieren des automatischen Kompletierens aus dem Verlauf</span><span class="sxs-lookup"><span data-stu-id="8df24-229">Turn off autocomplete from history</span></span>  

<span data-ttu-id="8df24-230">Beim Eingeben eines Ausdrucks zeigt das Popupfenster für die automatische Vervollständigung für die **Konsole** Ausdrücke an, die Sie zuvor durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="8df24-230">As you type out an expression, the autocomplete popup window for the **Console** displays expressions that you ran earlier.</span></span>  <span data-ttu-id="8df24-231">Die Ausdrücke werden mit dem Zeichen `>` vorkonfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8df24-231">The expressions are pre-pended with the `>` character.</span></span>  <span data-ttu-id="8df24-232">Um die Anzeige von Ausdrücken [](#open-console-settings) aus Ihrem Verlauf zu beenden, öffnen Sie Konsoleneinstellungen, und entfernen Sie das Kontrollkästchen neben **AutoComplete From History.**</span><span class="sxs-lookup"><span data-stu-id="8df24-232">To stop displaying expressions from your history, [open Console Settings](#open-console-settings) and remove the checkbox next to **Autocomplete From History** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="8df24-233">In der folgenden Abbildung `document.querySelector('a')` und `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.</span><span class="sxs-lookup"><span data-stu-id="8df24-233">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Im Popupmenü für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt." lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="8df24-235">Im Popupmenü für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8df24-235">The autocomplete popup menu displays expressions from history</span></span>  
:::image-end:::  

### <a name="choose-javascript-context"></a><span data-ttu-id="8df24-236">Auswählen des JavaScript-Kontexts</span><span class="sxs-lookup"><span data-stu-id="8df24-236">Choose JavaScript context</span></span>  

<span data-ttu-id="8df24-237">Die Standardoption für das **JavaScript-Kontextdropdown** ist **top**, das den [Browserkontext der][MdnDocsGlossaryBrowsingContext] Hauptwebseite darstellt.</span><span class="sxs-lookup"><span data-stu-id="8df24-237">The default option for the **JavaScript Context** dropdown is **top**, which represents the [browsing context][MdnDocsGlossaryBrowsingContext] of the main webpage.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Das Dropdownmenü "JavaScript-Kontext"" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="8df24-239">Das **Dropdownmenü "JavaScript-Kontext"**</span><span class="sxs-lookup"><span data-stu-id="8df24-239">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="8df24-240">Angenommen, Sie haben eine Anzeige auf Ihrer Webseite eingebettet in `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="8df24-240">Suppose you have an ad on your webpage embedded in an `<iframe>`.</span></span>  <span data-ttu-id="8df24-241">Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="8df24-241">You want to run JavaScript to tweak the DOM of the ad.</span></span>  <span data-ttu-id="8df24-242">Wählen Sie zunächst den Browserkontext der Anzeige im **Dropdownmenü JavaScript-Kontext** aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-242">First, choose the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Auswählen eines anderen JavaScript-Kontexts" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="8df24-244">Auswählen eines anderen JavaScript-Kontexts</span><span class="sxs-lookup"><span data-stu-id="8df24-244">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="8df24-245">Löschen der Konsole</span><span class="sxs-lookup"><span data-stu-id="8df24-245">Clear the Console</span></span>  

<span data-ttu-id="8df24-246">Führen Sie **einen**der folgenden Workflows aus, um die Konsole zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8df24-246">To clear the **Console**, complete any of the following workflows.</span></span>  

*   <span data-ttu-id="8df24-247">Wählen Sie **die Schaltfläche Konsole** löschen \( Konsole löschen ![ ](../media/clear-console-button-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-247">Choose the **Clear Console** \(![Clear Console](../media/clear-console-button-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="8df24-248">Zeigen Sie auf eine Nachricht, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Konsole löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="8df24-248">Hover on a message, open the contextual menu \(right-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="8df24-249">Geben `clear()` Sie in die Konsole **ein,** und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-249">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="8df24-250">Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.</span><span class="sxs-lookup"><span data-stu-id="8df24-250">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="8df24-251">Wählen `Control` + `L` Sie **aus, während sich die Konsole** im Fokus befindet.</span><span class="sxs-lookup"><span data-stu-id="8df24-251">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8df24-252">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8df24-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokollieren von Nachrichten im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Verwenden der Konsolenanwendung | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Überprüfen und Filtern von Informationen auf der aktuellen Webseite | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Überwachen von Änderungen in JavaScript mithilfe von Live Expressions | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browserkontext | MDN"  

> [!NOTE]
> <span data-ttu-id="8df24-262">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8df24-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8df24-263">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="8df24-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8df24-265">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8df24-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
