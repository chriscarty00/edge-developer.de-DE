---
description: Einführung in die Microsoft Edge-Entwicklertools (EdgeHTML)
title: Microsoft Edge-Entwicklertools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
experimental: true
experiment_id: 51fe4b97-3e55-41
ms.localizationpriority: high
ms.openlocfilehash: 0c01b761d1aa1fb645b15b0be5d5d6e4265e646e
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10985968"
---
# <span data-ttu-id="97be1-104">Microsoft Edge-Entwicklertools (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="97be1-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="97be1-105">Die Microsoft Edge\(EdgeHTML\) DevTools basieren auf [TypeScript][|::ref1::|Index], werden von [Open-Source][GithubMicrosoftChakracore] unterstützt, sind für moderne Front-End-Workflows optimiert und jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97be1-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="97be1-106">Wenn Sie mehr über die neuesten Funktionen erfahren möchten, lesen Sie [DevTools in der neuesten Version von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="97be1-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="97be1-107">Grundlegende Tools</span><span class="sxs-lookup"><span data-stu-id="97be1-107">Core tools</span></span>  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="97be1-109">Microsoft Edge (EdgeHTML) DevTools</span><span class="sxs-lookup"><span data-stu-id="97be1-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="97be1-110">Die Microsoft Edge \(EdgeHTML\) DevTools umfassen:</span><span class="sxs-lookup"><span data-stu-id="97be1-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="97be1-111">Einen Bereich [Elemente][DevtoolsGuideEdgehtml|::ref2::|] zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignis-Listenern und Festlegen von Haltepunkten für DOM-Mutationen</span><span class="sxs-lookup"><span data-stu-id="97be1-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="97be1-112">Eine [Konsole][DevtoolsGuideEdgehtml|::ref3::|] zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens</span><span class="sxs-lookup"><span data-stu-id="97be1-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="97be1-113">Einen [Debugger][DevtoolsGuideEdgehtml|::ref4::|] zum Durchlaufen von Code, Einstellen von Uhren und Haltepunkten, Livebearbeiten von Code und Überprüfen Ihrer Webspeicher- und Cookie-Caches</span><span class="sxs-lookup"><span data-stu-id="97be1-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="97be1-114">Einen Bereich [Netzwerk][DevtoolsGuideEdgehtml|::ref5::|] zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache</span><span class="sxs-lookup"><span data-stu-id="97be1-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="97be1-115">Einen Bereich [Leistung][DevtoolsGuideEdgehtml|::ref6::|], um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="97be1-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="97be1-116">Einen Bereich [Arbeitsspeicher][DevtoolsGuideEdgehtml|::ref7::|] zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Zuständen der Code-Runtime</span><span class="sxs-lookup"><span data-stu-id="97be1-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="97be1-117">Einen Bereich [Speicher][DevtoolsGuideEdgehtml|::ref8::|] zum Überprüfen und Verwalten Ihres Webspeichers, Ihrer IndexedDB, Ihrer Cookies und Ihrer Cachedaten</span><span class="sxs-lookup"><span data-stu-id="97be1-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="97be1-118">Einen Bereich [Dienstmitarbeiter][DevtoolsGuideEdgehtmlServiceworkers] zum Verwalten und Debuggen Ihrer Servicemitarbeiter</span><span class="sxs-lookup"><span data-stu-id="97be1-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="97be1-119">Einen Bereich [Emulation][DevtoolsGuideEdgehtml|::ref9::|] zum Testen Ihrer Website mit unterschiedlichen Browserprofilen, Bildschirmauflösungen und GPS-Positionskoordinaten</span><span class="sxs-lookup"><span data-stu-id="97be1-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="97be1-120">Bitte senden Sie weiterhin [Feedback und Feature-Anfragen](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span><span class="sxs-lookup"><span data-stu-id="97be1-120">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

> [!TIP]
> <span data-ttu-id="97be1-121">[Testen Sie auf Microsoft Edge \(EdgeHTML\) kostenlos mit jedem Browser][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="97be1-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="97be1-122">Das Microsoft Edge-Team hat sich mit [BrowserStack][BrowserstackEdgehtml] zusammengetan, um ﻿kostenlose Live- und automatisierte Tests auf Microsoft Edge bereitzustellen. \(EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="97be1-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="97be1-123">Microsoft Store-App</span><span class="sxs-lookup"><span data-stu-id="97be1-123">Microsoft Store app</span></span>  

<span data-ttu-id="97be1-124">Die **Microsoft Edge \(EdgeHTML\) DevTools** sind [jetzt][DevtoolsGuideEdgehtmlWhatsnew] als eigenständige [Windows 10-App im Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview] erhältlich, und zwar zusätzlich zur browserabhängigen \(`F12`\) Tooling-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="97be1-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="97be1-125">Die Store-Version enthält einen Bereich **Auswahl** zum Anfügen an geöffnete lokale und remote Seitenziele und ein Layout im Registerkartenformat für den einfachen Wechsel zwischen DevTools-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="97be1-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="97be1-126">Lokales Debugging</span><span class="sxs-lookup"><span data-stu-id="97be1-126">Local debugging</span></span>  

<span data-ttu-id="97be1-127">Um eine Seite lokal zu debuggen, starten Sie einfach die Microsoft Edge DevTools-App.</span><span class="sxs-lookup"><span data-stu-id="97be1-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="97be1-128">Im Bereich **Lokal** der Auswahl werden alle aktiven EdgeHTML-Inhaltsprozesse angezeigt, einschließlich der geöffneten Edge-Browser-Registerkarten, in denen [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe`-Prozesse\) und [WebView][HostingWebview]-Steuerelemente ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="97be1-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="97be1-129">Wählen Sie das Ziel, das angehängt werden soll, und öffnen Sie eine neue Registerkarten-Instanz der DevTools.</span><span class="sxs-lookup"><span data-stu-id="97be1-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="97be1-131">DevTools-App, Bereich "Lokal"</span><span class="sxs-lookup"><span data-stu-id="97be1-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="97be1-132">Remotedebugging</span><span class="sxs-lookup"><span data-stu-id="97be1-132">Remote debugging</span></span>  

<span data-ttu-id="97be1-133">Die Microsoft Edge DevTools-App bietet grundlegende Unterstützung beim Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="97be1-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="97be1-134">Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionen der Bereiche [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elemente][DevtoolsGuideEdgehtml|::ref11::|] \(für schreibgeschützte Vorgänge\) und [Konsole][DevtoolsGuideEdgehtml|::ref12::|] bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="97be1-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="97be1-135">Das Remote-Debugging ist auf Microsoft Edge \(EdgeHTML\), auf dem Desktop-Hosts ausgeführt werden, begrenzt und unterstützt andere EdgeHTML-Hosts und Windows 10-Geräte, die mit zukünftigen Versionen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="97be1-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="97be1-136">Lesen Sie zu Beginn den Abschnitt [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der Dokumente [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="97be1-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   <span data-ttu-id="97be1-138">DevTools-App, Bereich "Remote"</span><span class="sxs-lookup"><span data-stu-id="97be1-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="97be1-139">Allgemeine Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="97be1-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="97be1-140">Alle Tastenkombinationen wurden in der aktuellen Windows-Version überprüft.</span><span class="sxs-lookup"><span data-stu-id="97be1-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="97be1-141">Wenn Sie eine Tastenkombination nicht verwenden können, aktualisieren Sie Ihre Windows-Version.</span><span class="sxs-lookup"><span data-stu-id="97be1-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="97be1-142">Mit diesen Tastenkombinationen wird das DevTools-Hauptfenster gesteuert, und sie sollten bei allen Tools funktionieren.</span><span class="sxs-lookup"><span data-stu-id="97be1-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="97be1-143">Aktion</span><span class="sxs-lookup"><span data-stu-id="97be1-143">Action</span></span> | <span data-ttu-id="97be1-144">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="97be1-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="97be1-145">DevTools ein-/ausblenden\(zuletzt angezeigter Bereich wird geöffnet\)</span><span class="sxs-lookup"><span data-stu-id="97be1-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="97be1-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="97be1-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="97be1-147">Docking umschalten \(Ausdocken/Unten/Rechts\)</span><span class="sxs-lookup"><span data-stu-id="97be1-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="97be1-148">Datei öffnen</span><span class="sxs-lookup"><span data-stu-id="97be1-148">Open file</span></span> | `Ctrl`<span data-ttu-id="97be1-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="97be1-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="97be1-150">Nicht bearbeitbaren HTML-Quellcode im Debugger anzeigen</span><span class="sxs-lookup"><span data-stu-id="97be1-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="97be1-151">Konsole am unteren Rand eines beliebigen anderen Tools ein-/ausblenden</span><span class="sxs-lookup"><span data-stu-id="97be1-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="97be1-152">Zu Elementen wechseln \(DOM-Explorer\)</span><span class="sxs-lookup"><span data-stu-id="97be1-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="97be1-153">Zu Konsole wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="97be1-154">Zu Debugger wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="97be1-155">Zu Netzwerk wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="97be1-156">Zu Leistung wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="97be1-157">Zu Arbeitsspeicher wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="97be1-158">Zu Emulation wechseln</span><span class="sxs-lookup"><span data-stu-id="97be1-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="97be1-159">Hilfedokument</span><span class="sxs-lookup"><span data-stu-id="97be1-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="97be1-160">Nächstes Tool</span><span class="sxs-lookup"><span data-stu-id="97be1-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="97be1-161">Vorheriges Tool</span><span class="sxs-lookup"><span data-stu-id="97be1-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="97be1-162">Vorheriges Tool \(aus Verlauf\)</span><span class="sxs-lookup"><span data-stu-id="97be1-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="97be1-163">Nächstes Tool \(aus Verlauf\)</span><span class="sxs-lookup"><span data-stu-id="97be1-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="97be1-164">Nächster Hilfsrahmen</span><span class="sxs-lookup"><span data-stu-id="97be1-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="97be1-165">Vorheriger Hilfsrahmen</span><span class="sxs-lookup"><span data-stu-id="97be1-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="97be1-166">Nächste Übereinstimmung im Suchfeld</span><span class="sxs-lookup"><span data-stu-id="97be1-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="97be1-167">Vorherige Übereinstimmung im Suchfeld</span><span class="sxs-lookup"><span data-stu-id="97be1-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="97be1-168">Über Suchfeld suchen</span><span class="sxs-lookup"><span data-stu-id="97be1-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="97be1-169">Fokus auf Konsole unten richten</span><span class="sxs-lookup"><span data-stu-id="97be1-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="97be1-170">DevTools in Konsole starten</span><span class="sxs-lookup"><span data-stu-id="97be1-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="97be1-171">Seite aktualisieren</span><span class="sxs-lookup"><span data-stu-id="97be1-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="97be1-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="97be1-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="97be1-173">Wenn Sie Debuggen und an einem Haltepunkt angehalten werden, setzen Sie zuerst mit der Aktion **Seite aktualisieren** die Laufzeit fort.</span><span class="sxs-lookup"><span data-stu-id="97be1-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="97be1-174">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="97be1-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="97be1-175">Bitte senden Sie uns Ihr Feedback, damit wir die Microsoft Edge \(EdgeHTML \) DevTools für Sie verbessern können!</span><span class="sxs-lookup"><span data-stu-id="97be1-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="97be1-176">Öffnen Sie einfach die Tools \(`F12`\), und wählen Sie die Schaltfläche [Feedback senden](#microsoft-edge-edgehtml-developer-tools) aus.</span><span class="sxs-lookup"><span data-stu-id="97be1-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="97be1-177">Werden Sie [Windows-Insider][WindowsInsiderProgram], um die [neuesten Funktionen der DevTools][DevtoolsGuideEdgehtmlWhatsnew] in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="97be1-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="97be1-178">Verwenden Sie die Windows Feedback-Hub-App, um allgemeine Vorschläge und Probleme in Bezug auf Windows zu posten, zu empfehlen zu verfolgen oder Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="97be1-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Konsole"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Debugger"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elemente"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Arbeitsspeicher"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Netzwerk"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Leistung"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Dienstmitarbeiter"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Speicher"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools im neuesten Windows 10-Update (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Microsoft Edge (EdgeHTML) DevTools Protocol"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools-Vorschau – DevTools-Protokoll-Clients"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) für Windows 10-Apps"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Progressive Web Apps (EdgeHTML) unter Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools-Vorschau"  

[WindowsInsiderProgram]: https://insider.windows.com "Windows-Insider-Programm"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Kostenlose Microsoft Edge-Browser-Tests | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
