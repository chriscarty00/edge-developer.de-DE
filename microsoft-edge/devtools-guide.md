---
description: Kennenlernen der Microsoft Edge-Entwickler Tools (EdgeHTML)
title: Microsoft Edge (EdgeHTML)-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629504"
---
# <span data-ttu-id="18f4f-104">Microsoft Edge (EdgeHTML)-Entwickler Tools</span><span class="sxs-lookup"><span data-stu-id="18f4f-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="18f4f-105">Die Microsoft Edge \ (EdgeHTML \) devtools [sind mit einer][|::ref1::|Index]von [Open Source][GithubMicrosoftChakracore]unterstützten, für moderne Front-End-Workflows optimierten und jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbaren Version erstellt.</span><span class="sxs-lookup"><span data-stu-id="18f4f-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="18f4f-106">Weitere Informationen zu den neuesten Features finden Sie unter [devtools im neuesten Update von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="18f4f-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="18f4f-107">Kern Tools</span><span class="sxs-lookup"><span data-stu-id="18f4f-107">Core tools</span></span>  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) devtools":::
   <span data-ttu-id="18f4f-109">Microsoft Edge (EdgeHTML) devtools</span><span class="sxs-lookup"><span data-stu-id="18f4f-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="18f4f-110">Zu den Microsoft Edge \ (EdgeHTML \) devtools gehören:</span><span class="sxs-lookup"><span data-stu-id="18f4f-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="18f4f-111">Ein [Element][DevtoolsGuideEdgehtml|::ref2::|] Panel zum Bearbeiten von HTML und CSS, untersuchen von Barrierefreiheitseigenschaften, Anzeigen von ereignislistern und Festlegen von Haltepunkten für DOM-Mutationen</span><span class="sxs-lookup"><span data-stu-id="18f4f-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="18f4f-112">Eine [Konsole][DevtoolsGuideEdgehtml|::ref3::|] zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens</span><span class="sxs-lookup"><span data-stu-id="18f4f-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="18f4f-113">Ein [Debugger][DevtoolsGuideEdgehtml|::ref4::|] zum Durchlaufen von Code, Festlegen von Überwachungen und Haltepunkten, Live Bearbeiten des Codes und untersuchen der Webspeicher-und Cookie-Caches</span><span class="sxs-lookup"><span data-stu-id="18f4f-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="18f4f-114">[Netzwerk][DevtoolsGuideEdgehtml|::ref5::|] Fenster zum Überwachen und prüfen von Anforderungen und Antworten aus dem Netzwerk-und Browsercache</span><span class="sxs-lookup"><span data-stu-id="18f4f-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="18f4f-115">Ein [Leistungs][DevtoolsGuideEdgehtml|::ref6::|] Panel, in dem die von Ihrer Website benötigten Zeit-und Systemressourcen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="18f4f-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="18f4f-116">Ein [Speicher][DevtoolsGuideEdgehtml|::ref7::|] Panel zum Messen der Verwendung von Speicherressourcen und zum Vergleichen von Heap-Snapshots in verschiedenen Zuständen der Code Laufzeit</span><span class="sxs-lookup"><span data-stu-id="18f4f-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="18f4f-117">Ein [Speicher][DevtoolsGuideEdgehtml|::ref8::|] Panel zum Überprüfen und Verwalten Ihres Webspeichers, IndexedDB, Cookies und Cache-Daten</span><span class="sxs-lookup"><span data-stu-id="18f4f-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="18f4f-118">Ein [Dienstmitarbeiter][DevtoolsGuideEdgehtmlServiceworkers] -Panel zum Verwalten und Debuggen von Servicemitarbeitern</span><span class="sxs-lookup"><span data-stu-id="18f4f-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="18f4f-119">Ein [Emulations][DevtoolsGuideEdgehtml|::ref9::|] Panel zum Testen Ihrer Website mit unterschiedlichen Browser Profilen, Bildschirmauflösungen und GPS-Positionskoordinaten</span><span class="sxs-lookup"><span data-stu-id="18f4f-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="18f4f-120">Bitte senden Sie Ihr [Feedback und ihre Funktionswünsche](#feedback)weiter!</span><span class="sxs-lookup"><span data-stu-id="18f4f-120">Please keep sending your [feedback and feature requests](#feedback)!</span></span>  

> [!TIP]
> <span data-ttu-id="18f4f-121">[Testen Sie Microsoft Edge \ (EdgeHTML \) kostenlos in einem beliebigen Browser][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="18f4f-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="18f4f-122">Das Microsoft Edge-Team hat sich mit [BrowserStack][BrowserstackEdgehtml] zusammengetan, um ﻿kostenlose Live-und automatisierte Tests für Microsoft Edge (EdgeHTML \) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18f4f-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="18f4f-123">Microsoft Store-App</span><span class="sxs-lookup"><span data-stu-id="18f4f-123">Microsoft Store app</span></span>  

<span data-ttu-id="18f4f-124">Die **Microsoft Edge \ (EdgeHTML \)-devtools** sind [nun][DevtoolsGuideEdgehtmlWhatsnew] als eigenständige [Windows 10-App aus dem Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview]sowie über die in-Browser- `F12` Tooling-Umgebung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18f4f-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="18f4f-125">Bei der Store-Version wird ein **Auswahl** Bereich für das Anfügen zum Öffnen von lokalen und Remote Seiten Zielen sowie ein Layout mit Registerkarten zum einfachen Umschalten zwischen devtools-Instanzen geliefert.</span><span class="sxs-lookup"><span data-stu-id="18f4f-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="18f4f-126">Lokales Debuggen</span><span class="sxs-lookup"><span data-stu-id="18f4f-126">Local debugging</span></span>  

<span data-ttu-id="18f4f-127">Wenn Sie eine Seite lokal debuggen möchten, starten Sie einfach die Microsoft Edge devtools-app.</span><span class="sxs-lookup"><span data-stu-id="18f4f-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="18f4f-128">Der **lokale** Teil des Auswahlfelds zeigt alle aktiven EdgeHTML-Inhalts Prozesse an, einschließlich der geöffneten Edge-Browser-Registerkarten, mit [PWAs][PwasEdgehtmlIndex] \ ( `WWAHost.exe` Prozesse \) und [WebView][HostingWebview] -Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="18f4f-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="18f4f-129">Wählen Sie das gewünschte Ziel aus, um eine neue Registerkarten Instanz des devtools anzufügen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="18f4f-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Lokales Panel der devtools-App":::
   <span data-ttu-id="18f4f-131">Lokales Panel der devtools-App</span><span class="sxs-lookup"><span data-stu-id="18f4f-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="18f4f-132">Remote Debuggen</span><span class="sxs-lookup"><span data-stu-id="18f4f-132">Remote debugging</span></span>  

<span data-ttu-id="18f4f-133">Die Microsoft Edge devtools-App bietet grundlegende Unterstützung für das Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [devtools-Protokoll][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="18f4f-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="18f4f-134">Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionalität des [Debuggers][DevtoolsGuideEdgehtml|::ref10::|], [Elemente][DevtoolsGuideEdgehtml|::ref11::|] \ (für schreibgeschützte Vorgänge \) und [Konsolen][DevtoolsGuideEdgehtml|::ref12::|] Panels ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18f4f-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="18f4f-135">Das Remote Debuggen ist auf Microsoft Edge \ (EdgeHTML \), auf dem Desktop Hosts ausgeführt werden, mit Unterstützung für andere EdgeHTML-Hosts und Windows 10-Geräte in zukünftigen Versionen limitiert.</span><span class="sxs-lookup"><span data-stu-id="18f4f-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="18f4f-136">Um zu beginnen, lesen Sie den Abschnitt [*Microsoft Edge devtools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der [devtools-Protokoll][DevtoolsProtocolEdgehtmlIndex] Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="18f4f-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="DevTools-App-Remote Panel":::
   <span data-ttu-id="18f4f-138">DevTools-App-Remote Panel</span><span class="sxs-lookup"><span data-stu-id="18f4f-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="18f4f-139">Allgemeine Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="18f4f-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="18f4f-140">Alle Tastenkombinationen wurden in der neuesten Version von Windows überprüft.</span><span class="sxs-lookup"><span data-stu-id="18f4f-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="18f4f-141">Wenn Sie eine Verknüpfung nicht verwenden können, aktualisieren Sie Ihre Kopie von Windows.</span><span class="sxs-lookup"><span data-stu-id="18f4f-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="18f4f-142">Diese Tastenkombinationen steuern das Hauptfenster von devtools und sollten über alle Tools hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="18f4f-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="18f4f-143">Aktion</span><span class="sxs-lookup"><span data-stu-id="18f4f-143">Action</span></span> | <span data-ttu-id="18f4f-144">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="18f4f-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="18f4f-145">DevTools anzeigen/ausblenden \ (wird zum zuletzt angezeigten Fenster geöffnet)</span><span class="sxs-lookup"><span data-stu-id="18f4f-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="18f4f-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="18f4f-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="18f4f-147">Umschalten der Docking-Taste \ (Abdocken/unten/rechts \)</span><span class="sxs-lookup"><span data-stu-id="18f4f-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="18f4f-148">Datei öffnen</span><span class="sxs-lookup"><span data-stu-id="18f4f-148">Open file</span></span> | `Ctrl`<span data-ttu-id="18f4f-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="18f4f-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="18f4f-150">Anzeigen des nicht bearbeitbaren HTML-Quellcodes im Debugger</span><span class="sxs-lookup"><span data-stu-id="18f4f-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="18f4f-151">Konsole am unteren Rand eines beliebigen anderen Tools einblenden/ausblenden</span><span class="sxs-lookup"><span data-stu-id="18f4f-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="18f4f-152">Wechseln zu Elementen \ (DOM-Explorer \)</span><span class="sxs-lookup"><span data-stu-id="18f4f-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="18f4f-153">Zur Konsole wechseln</span><span class="sxs-lookup"><span data-stu-id="18f4f-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="18f4f-154">Wechseln zu Debugger</span><span class="sxs-lookup"><span data-stu-id="18f4f-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="18f4f-155">Zum Netzwerk wechseln</span><span class="sxs-lookup"><span data-stu-id="18f4f-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="18f4f-156">Wechseln zur Leistung</span><span class="sxs-lookup"><span data-stu-id="18f4f-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="18f4f-157">Wechseln zum Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="18f4f-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="18f4f-158">Wechseln zur Emulation</span><span class="sxs-lookup"><span data-stu-id="18f4f-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="18f4f-159">Hilfedokument</span><span class="sxs-lookup"><span data-stu-id="18f4f-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="18f4f-160">Nächstes Tool</span><span class="sxs-lookup"><span data-stu-id="18f4f-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="18f4f-161">Vorheriges Tool</span><span class="sxs-lookup"><span data-stu-id="18f4f-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="18f4f-162">Vorheriges Tool \ (aus Verlauf \)</span><span class="sxs-lookup"><span data-stu-id="18f4f-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="18f4f-163">Nächstes Tool \ (aus Verlauf \)</span><span class="sxs-lookup"><span data-stu-id="18f4f-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="18f4f-164">Nächster teilframe</span><span class="sxs-lookup"><span data-stu-id="18f4f-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="18f4f-165">Vorheriger teilframe</span><span class="sxs-lookup"><span data-stu-id="18f4f-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="18f4f-166">Nächste Übereinstimmung im Suchfeld</span><span class="sxs-lookup"><span data-stu-id="18f4f-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="18f4f-167">Vorherige Übereinstimmung im Suchfeld</span><span class="sxs-lookup"><span data-stu-id="18f4f-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="18f4f-168">Suchen im Suchfeld</span><span class="sxs-lookup"><span data-stu-id="18f4f-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="18f4f-169">Konzentrieren Sie sich am unteren Rand auf die Konsole.</span><span class="sxs-lookup"><span data-stu-id="18f4f-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="18f4f-170">Starten von devtools to Console</span><span class="sxs-lookup"><span data-stu-id="18f4f-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="18f4f-171">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="18f4f-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="18f4f-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="18f4f-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="18f4f-173">Wenn Sie das Debuggen durchgeführt und an einem Haltepunkt angehalten haben, setzt die Aktion **Seite aktualisieren** die Laufzeit zuerst fort.</span><span class="sxs-lookup"><span data-stu-id="18f4f-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="18f4f-174">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="18f4f-174">Feedback</span></span>  

<span data-ttu-id="18f4f-175">Bitte senden Sie Ihr Feedback, damit Sie die Microsoft Edge \ (EdgeHTML \) devtools für Sie verbessern können.</span><span class="sxs-lookup"><span data-stu-id="18f4f-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="18f4f-176">Öffnen Sie einfach die Tools \ ( `F12` \), und wählen Sie die Schaltfläche [Feedback senden](#microsoft-edge-edgehtml-developer-tools) aus.</span><span class="sxs-lookup"><span data-stu-id="18f4f-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="18f4f-177">Werden Sie [Windows-Insider][WindowsInsiderProgram] , um eine Vorschau der [neuesten Features in devtools][DevtoolsGuideEdgehtmlWhatsnew]anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18f4f-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="18f4f-178">Verwenden Sie die Windows-Feedback-Hub-App zum Posten, nach oben abstimmen, Nachverfolgung und Support für allgemeine Windows-Vorschläge und-Probleme.</span><span class="sxs-lookup"><span data-stu-id="18f4f-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Konsole"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Debugger"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elemente"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Speicher"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Netzwerk"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Leistung"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Dienstmitarbeiter"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Speicher"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools im neuesten Windows 10-Update (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Microsoft Edge (EdgeHTML) devtools-Protokoll"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) für Windows 10-apps"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Progressive Web-Apps (EdgeHTML) unter Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge devtools Preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Windows-Insider-Programm"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Testen des Microsoft Edge-Browsers kostenlos | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
