---
title: Neuerungen in devtools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: fc5dcc10ba3a79bd3f073e0e3504e551d7e23d70
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688178"
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

# <span data-ttu-id="d22be-103">Neuerungen in devtools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="d22be-103">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="d22be-104">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="d22be-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="d22be-105">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="d22be-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="d22be-106">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="d22be-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="d22be-107">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="d22be-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="d22be-108">Verwenden des devtools im Windows-Modus für hohen Kontrast</span><span class="sxs-lookup"><span data-stu-id="d22be-108">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="d22be-109">Die Microsoft Edge-devtools werden jetzt im Modus für hohen Kontrast angezeigt, wenn sich Windows im Modus für hohen Kontrast befindet.</span><span class="sxs-lookup"><span data-stu-id="d22be-109">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Die Microsoft Edge-devtools im Modus für hohen Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="d22be-111">Die Microsoft Edge-devtools im Modus für hohen Kontrast</span><span class="sxs-lookup"><span data-stu-id="d22be-111">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-112">[Befolgen Sie die Anweisungen zum Aktivieren des Modus für hohen Kontrast unter Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="d22be-112">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="d22be-113">Öffnen Sie das devtools in Microsoft Edge, indem Sie auf `F12` oder drücken `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="d22be-113">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="d22be-114">Die devtools werden im Modus für hohen Kontrast angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d22be-114">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="d22be-115">Der Microsoft Edge-devtools unterstützt derzeit den Modus für hohen Kontrast unter Windows, aber nicht unter macOS.</span><span class="sxs-lookup"><span data-stu-id="d22be-115">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="d22be-116">Chrom Problem [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="d22be-116">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="d22be-117">Anpassen von Tastenkombinationen im devtools an vs-Code</span><span class="sxs-lookup"><span data-stu-id="d22be-117">Match keyboard shortcuts in the DevTools to VS Code</span></span>  

<span data-ttu-id="d22be-118">Aus Ihrem [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) und dem " [Chromium Public Issue Tracker][CRIssuesList]" hat das Microsoft Edge devtools-Team gelernt, dass Sie die Möglichkeit haben möchten, Tastenkombinationen im devtools anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d22be-118">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="d22be-119">In Microsoft Edge 84 können Sie jetzt die Tastenkombinationen im devtools mit dem [vs-Code][VSCode]vergleichen, bei dem es sich nur um eine der Features handelt, an denen das Team für die Anpassung der Tastenkombinationen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="d22be-119">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [VS Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Anpassen von Tastenkombinationen im devtools an vs-Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="d22be-121">Die Microsoft Edge-devtools im Modus für hohen Kontrast</span><span class="sxs-lookup"><span data-stu-id="d22be-121">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-122">Um das Experiment zu testen, öffnen Sie die devtools-Einstellungen, indem Sie `?` ![ in der oberen rechten Ecke des devtools das Symbol devtools Settings (Symbol) drücken oder auswählen ][ImageSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="d22be-122">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="d22be-123">Navigieren Sie zum Abschnitt **Experimente** , und aktivieren Sie die **Registerkarte Einstellungen für benutzerdefinierte Tastenkombinationen aktivieren (erfordert Reload)**.</span><span class="sxs-lookup"><span data-stu-id="d22be-123">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="d22be-124">Laden Sie nun das devtools erneut, öffnen Sie die Einstellungen erneut, und navigieren Sie zum Abschnitt **Verknüpfungen** .</span><span class="sxs-lookup"><span data-stu-id="d22be-124">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="d22be-125">Wählen Sie im Dropdownmenü **Tastenkombinationen von Voreinstellungen** **devtools (Standard)** aus, und wählen Sie **Visual Studio-Code**aus.</span><span class="sxs-lookup"><span data-stu-id="d22be-125">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="d22be-126">Die Tastenkombinationen im devtools entsprechen nun den Tastenkombinationen für äquivalente Aktionen in vs-Code.</span><span class="sxs-lookup"><span data-stu-id="d22be-126">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

<span data-ttu-id="d22be-127">Die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in vs- [Code][VSCodeShortcuts] lautet beispielsweise `F5` .</span><span class="sxs-lookup"><span data-stu-id="d22be-127">For example, the keyboard shortcut for pausing or continuing running a script in [VS Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="d22be-128">Wenn die **devtools (Standardeinstellung)** voreingestellt ist, ist die gleiche Verknüpfung in der devtools, `F8` aber mit der **Visual Studio-Code** Vorgabe, diese Verknüpfung nun auch `F5` .</span><span class="sxs-lookup"><span data-stu-id="d22be-128">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="d22be-129">Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar, geben Sie also bitte Ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) an das Team weiter!</span><span class="sxs-lookup"><span data-stu-id="d22be-129">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="d22be-130">Chrom Problem [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="d22be-130">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="d22be-131">Remote Debuggen von Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="d22be-131">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="d22be-132">Sie können jetzt Ihre Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, mithilfe der vollen Leistung des [Microsoft Edge-devtools][DevToolsChromiumGuide]Remotedebuggen.</span><span class="sxs-lookup"><span data-stu-id="d22be-132">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="d22be-133">Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von faltbaren und Dual-Screen-Geräten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="d22be-133">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="d22be-134">Der Emulator führt das Android-Betriebssystem aus und bietet die [Microsoft Edge Android-App][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="d22be-134">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="d22be-135">Laden Sie Ihren Webinhalt in die [Microsoft Edge-App][AndroidEdge] , und Debuggen Sie ihn mit dem [Microsoft Edge-devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="d22be-135">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge-APP, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="d22be-137">Die Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="d22be-137">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-138">Die `edge://inspect` Seite in einer Desktop Instanz von [Microsoft Edge][DesktopEdge] zeigt die **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaIndex] , die auf dem [Surface Duo-Emulator][DualScreensAndroidEmulator]ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d22be-138">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf der Seite "Edge://Inspect" wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="d22be-140">`edge://inspect`Auf der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d22be-140">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="d22be-141">Wenn Sie auf die Registerkarte oder PWA **prüfen** , die Sie debuggen möchten, wird die [Microsoft Edge-devtools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="d22be-141">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="d22be-142">[Befolgen Sie die schrittweise Anleitung zum Remotedebuggen von Webinhalten im Surface Duo-Emulator][DevToolsRemoteDebugDuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="d22be-142">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="d22be-143">Einfachere Größe der devtools-Schublade</span><span class="sxs-lookup"><span data-stu-id="d22be-143">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="d22be-144">In Microsoft Edge 83 oder früheren Versionen konnten Sie die Größe der devtools- [Schublade][DevToolsDrawer] nur ändern, indem Sie in der Symbolleiste des Zeichners auf die Maus zeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-144">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="d22be-145">Die Schublade verhält sich anders als die anderen Größen Steuerelemente für Bereiche im devtools, in denen Sie den Mauszeiger über den Rand des Bereichs bewegen, um die Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d22be-145">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="d22be-146">Wählen Sie die folgende Abbildung aus, um zu sehen, wie die Größe der Schublade in Version 83 oder früher von Microsoft Edge funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="d22be-146">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der devtools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="d22be-148">Ändern der Größe der devtools-Schublade in Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="d22be-148">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="d22be-149">Ab Microsoft Edge 84 können Sie jetzt die Größe der Schublade ändern, indem Sie auf den Rahmen des Ziehpunkts zeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-149">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="d22be-150">Diese Änderung richtet das Verhalten beim Ändern der Größe des devtools-Einschubs an die Art und Weise aus, wie Sie die Größe anderer Bereiche im devtools ändern.</span><span class="sxs-lookup"><span data-stu-id="d22be-150">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="d22be-151">Wählen Sie die folgende Abbildung aus, um die Größenänderung in Aktion in Microsoft Edge 84 anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-151">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der devtools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="d22be-153">Ändern der Größe der devtools-Schublade in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="d22be-153">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="d22be-154">Chrom Problem [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="d22be-154">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="d22be-155">Screencasting-Navigationsschaltflächen zeigen den Fokus an</span><span class="sxs-lookup"><span data-stu-id="d22be-155">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="d22be-156">Beim Remotedebuggen eines [Android-Geräts][DevToolsRemoteDebugAndroid], eines [Windows 10-Geräts][DevToolsRemoteDebugWindows]oder eines [Surface Duo-Emulators][DevToolsRemoteDebugDuoEmulator]können Sie das Screencasting mit dem ![ Screencast ][ImageScreencastingIcon] -Symbol in der oberen linken Ecke des devtools umschalten.</span><span class="sxs-lookup"><span data-stu-id="d22be-156">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="d22be-157">Wenn Screencasting aktiviert ist, können Sie über das devtools-Fenster auf der Registerkarte in Microsoft Edge auf dem Remotegerät navigieren.</span><span class="sxs-lookup"><span data-stu-id="d22be-157">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="d22be-158">In Microsoft Edge 84 sind für diese Navigationsschaltflächen nun auch Tastaturzugriff möglich.</span><span class="sxs-lookup"><span data-stu-id="d22be-158">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Durch Drücken von UMSCHALT + TAB aus der screencasted-URL-Leiste wird der Fokus auf der Schaltfläche Aktualisieren angezeigt." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="d22be-160">Das Drücken der `Shift` + `Tab` screencasted-URL-Leiste zeigt den Fokus auf die Schaltfläche " **Aktualisieren** ".</span><span class="sxs-lookup"><span data-stu-id="d22be-160">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="d22be-161">Chrom Problem [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="d22be-161">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="d22be-162">Der Bereich "Details zum Netzwerkbereich" ist jetzt verfügbar</span><span class="sxs-lookup"><span data-stu-id="d22be-162">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="d22be-163">In Microsoft Edge 84 nimmt der [Bereich "Details" im Bereich][DevToolsNetworkDetails] " **Netzwerk** " nun den Fokus, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll][DevToolsNetworkLog]öffnen.</span><span class="sxs-lookup"><span data-stu-id="d22be-163">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="d22be-164">Diese Änderung ermöglicht es Bildschirmsprachausgaben, den Inhalt des **Detail** Bereichs zu lesen und mit Ihnen zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="d22be-164">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Bereich "Details" im Netzwerkbereich nimmt beim Öffnen den Fokus auf" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="d22be-166">Der Bereich " **Details** " im **Netzwerk** Bereich nimmt beim Öffnen den Fokus auf</span><span class="sxs-lookup"><span data-stu-id="d22be-166">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="d22be-167">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="d22be-167">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="d22be-168">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="d22be-168">Announcements from the Chromium project</span></span>  

<span data-ttu-id="d22be-169">In den folgenden Abschnitten werden weitere in Microsoft Edge 84 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="d22be-169">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="d22be-170">Beheben von Problemen mit der Website mit dem Tool "neue Probleme" im devtools-Einzug</span><span class="sxs-lookup"><span data-stu-id="d22be-170">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="d22be-171">Das Tool "neue **Probleme** " im devtools-Einzug wurde entwickelt, um die Ermüdung der Benachrichtigung und die unaufgeräumtheit der **Konsole**zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d22be-171">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="d22be-172">Derzeit ist die **Konsole** der zentrale Ort für Websiteentwickler,-Bibliotheken,-Frameworks und Microsoft Edge, um Nachrichten, Warnungen und Fehler zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="d22be-172">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="d22be-173">Das **Issues** -Tool aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und umsetzbar, Links zu betroffenen Ressourcen in Microsoft Edge-devtools und enthält Anleitungen zum Beheben der Probleme.</span><span class="sxs-lookup"><span data-stu-id="d22be-173">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="d22be-174">Im Laufe der Zeit sollten Sie mehr und mehr Warnungen in der Microsoft Edge-Oberflächenbehandlung im Tool Probleme und nicht in der **Konsole**sehen, was dazu beitragen sollte, die **Fehler** in der **Konsole**zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d22be-174">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="d22be-175">Informationen zu den ersten Schritten finden Sie unter [Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues-Tool][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="d22be-175">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool "Probleme" im devtools-Einzug" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="d22be-177">Das Tool " **Probleme** " im devtools-Einzug</span><span class="sxs-lookup"><span data-stu-id="d22be-177">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-178">Chrom Problem [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="d22be-178">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="d22be-179">Anzeigen von barrierefreiheitsinformationen im Tooltip des Prüfmodus</span><span class="sxs-lookup"><span data-stu-id="d22be-179">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="d22be-180">Die QuickInfo für den **Prüfmodus** gibt jetzt an, ob das Element über einen [Namen und eine Rolle][WebhintHintsAxeNameRoleValue] für Barrierefreiheit verfügt und die [Tastatur fokussierbar][WebhintHintsAxeKeyboard]ist.</span><span class="sxs-lookup"><span data-stu-id="d22be-180">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="ToolTip des Prüfmodus mit Informationen zur Barrierefreiheit" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="d22be-182">ToolTip des **Prüfmodus** mit Informationen zur Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="d22be-182">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-183">Chrom Problem [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="d22be-183">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="d22be-184">Updates für das Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="d22be-184">Performance panel updates</span></span>  

#### <span data-ttu-id="d22be-185">Anzeigen der gesamten Blockierungszeit Informationen in der Fußzeile</span><span class="sxs-lookup"><span data-stu-id="d22be-185">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="d22be-186">Nachdem Sie die Auslastungs Leistung aufgezeichnet haben, wird im Bereich " **Leistung** " nun die Gesamt Blockierungszeit angezeigt. \ (TBT \) Informationen in der Fußzeile.</span><span class="sxs-lookup"><span data-stu-id="d22be-186">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="d22be-187">TBT ist eine Load Performance-Metrik, die quantifiziert, wie lange eine Seite verwendet werden kann, um nutzbar zu werden.</span><span class="sxs-lookup"><span data-stu-id="d22be-187">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="d22be-188">Es misst im Wesentlichen, wie lange eine Seite als verwendbar angezeigt wird \ (weil der Inhalt auf dem Bildschirm gerendert wird \); ist aber nicht wirklich brauchbar, da JavaScript den Hauptthread blockiert und daher die Seite nicht auf Benutzereingaben reagiert.</span><span class="sxs-lookup"><span data-stu-id="d22be-188">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="d22be-189">TBT ist die wichtigste Metrik für die Annäherung an die erste Eingabeverzögerung.</span><span class="sxs-lookup"><span data-stu-id="d22be-189">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="d22be-190">Verwenden Sie zum Abrufen der Gesamtzeit Informationen für die Blockierung nicht das Symbol Workflow zum Aktualisieren der **Seitenaktualisierung,** ![ um die ][ImageRefreshPageIcon] Ladeleistung der Seite aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d22be-190">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="d22be-191">Wählen Sie stattdessen **Record** ![ das Symbol Datensatz aufzeichnen aus ][ImageRecordIcon] , laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden Sie die Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="d22be-191">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="d22be-192">Wenn Sie sehen `Total Blocking Time: Unavailable` , hat Microsoft Edge devtools die erforderlichen Informationen nicht aus den internen Profilerstellungsdaten in Microsoft Edge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d22be-192">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Gesamtzahl der Blockierungszeit Informationen in der Fußzeile einer Leistungsbereich-Aufzeichnung" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="d22be-194">Gesamtzahl der Blockierungszeit Informationen in der Fußzeile einer **Leistungs** Bereich-Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="d22be-194">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-195">Chrom Problem [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="d22be-195">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="d22be-196">Layout-Schicht Ereignisse im Abschnitt "neue Benutzeroberfläche"</span><span class="sxs-lookup"><span data-stu-id="d22be-196">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="d22be-197">Der Abschnitt "neue **Benutzeroberfläche** " im **Leistungs** Bereich hilft Ihnen, Layout-Schichten zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="d22be-197">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="d22be-198">Die kumulative Layout-Schicht \ (CLS \) ist eine Metrik, mit der Sie unerwünschte visuelle Instabilität quantifizieren können.</span><span class="sxs-lookup"><span data-stu-id="d22be-198">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="d22be-199">Wählen Sie das **Layout-Schicht** -Ereignis aus, um die Details der Layout-Verschiebung im **Zusammenfassungs** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-199">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="d22be-200">Zeigen Sie mit der Maus auf die Felder **verschoben von** und **verschoben in** , um zu veranschaulichen, wo die Verschiebung des Layouts aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d22be-200">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Die Details einer Layout-Verschiebung" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="d22be-202">Die Details einer Layout-Verschiebung</span><span class="sxs-lookup"><span data-stu-id="d22be-202">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="d22be-203">Genauere Terminologie für Versprechungen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="d22be-203">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="d22be-204">Bei der Protokollierung `Promise` von a wurde der Wert für die **Konsole** fälschlicherweise `PromiseStatus` auf gesetzt `resolved` .</span><span class="sxs-lookup"><span data-stu-id="d22be-204">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Ein Beispiel für die Konsole unter Verwendung der alten aufgelösten Terminologie" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="d22be-206">Beispiel für die **Konsole** unter Verwendung der alten `resolved` Terminologie</span><span class="sxs-lookup"><span data-stu-id="d22be-206">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-207">Die **Konsole** verwendet nun den Ausdruck `fulfilled` , der an der Spezifikation ausgerichtet ist `Promise` .</span><span class="sxs-lookup"><span data-stu-id="d22be-207">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="d22be-208">Weitere Informationen zur `Promise` Spezifikation finden Sie unter [Zustände und Schicksale auf GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="d22be-208">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Ein Beispiel für die Konsole unter Verwendung der neuen erfüllten Terminologie" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="d22be-210">Ein Beispiel für die **Konsole** unter Verwendung der neuen `fulfilled` Terminologie</span><span class="sxs-lookup"><span data-stu-id="d22be-210">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-211">V8-Problem [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="d22be-211">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="d22be-212">Aktualisierungen des Formatvorlagenbereichs</span><span class="sxs-lookup"><span data-stu-id="d22be-212">Styles pane updates</span></span>  

#### <span data-ttu-id="d22be-213">Unterstützung für das Schlüsselwort "Revert"</span><span class="sxs-lookup"><span data-stu-id="d22be-213">Support for the revert keyword</span></span>  

<span data-ttu-id="d22be-214">Die AutoVervollständigen-Benutzeroberfläche des Bereichs " **Formatvorlagen** " erkennt nun das [Revert][MDNRevert] CSS-Schlüsselwort, das den kaskadierten Wert einer Eigenschaft auf den vorherigen Wert zurücksetzt, der auf das Styling des Elements angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d22be-214">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Festlegen des Werts einer Eigenschaft auf "Zurücksetzen"" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="d22be-216">Festlegen des Werts einer Eigenschaft auf "Zurücksetzen"</span><span class="sxs-lookup"><span data-stu-id="d22be-216">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-217">Chrom Problem [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="d22be-217">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="d22be-218">Bildvorschau</span><span class="sxs-lookup"><span data-stu-id="d22be-218">Image previews</span></span>  

<span data-ttu-id="d22be-219">Zeigen Sie mit der Maus auf einen `background-image` Wert im Bereich **Formatvorlagen** , um eine Vorschau des Bilds in einer QuickInfo anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-219">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Bewegen des Mauszeigers über einen Hintergrund-Image-Wert" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="d22be-221">Zeigen auf einen `background-image` Wert</span><span class="sxs-lookup"><span data-stu-id="d22be-221">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-222">Chrom Problem [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="d22be-222">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="d22be-223">Die Farbauswahl verwendet nun die durch Leerzeichen getrennte funktionale Farb Notation</span><span class="sxs-lookup"><span data-stu-id="d22be-223">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="d22be-224">[CSS-Farb Modulstufe 4][CSSWGDraftsColor4Changes3] gibt an, dass Farbfunktionen, wie beispielsweise `rgb()` , Leerzeichen getrennte Argumente unterstützen sollen.</span><span class="sxs-lookup"><span data-stu-id="d22be-224">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="d22be-225">So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="d22be-225">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="d22be-226">Wenn Sie Farben mit der [Farbauswahl][DevtoolsCssReferenceColorPicker] auswählen oder zwischen Farbdarstellungen im **Formatvorlagen** Bereich wechseln, indem Sie `Shift` den Wert halten und auswählen `background-color` , wird die Argumentsyntax mit Leerzeichengetrennt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d22be-226">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Bereich "Formatvorlagen"" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="d22be-228">Verwenden von durch Leerzeichen getrennten Argumenten im Bereich " **Formatvorlagen** "</span><span class="sxs-lookup"><span data-stu-id="d22be-228">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="d22be-229">Außerdem sollten Sie die Syntax im **berechneten** Bereich und die QuickInfo für den **Überprüfungsmodus** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d22be-229">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="d22be-230">Microsoft Edge devtools verwendet die neue Syntax, da anstehende CSS-Features wie [Color ()][CSSWGDraftsColor4Property] die veraltete Komma getrennte Argumentsyntax nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d22be-230">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="d22be-231">Die Syntax für das Leerzeichen getrennte Argument wurde in den meisten Browsern eine Zeitlang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d22be-231">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="d22be-232">Weitere Informationen finden Sie unter [kann ich: Leerzeichen getrennte funktionale Farb Notationen verwenden?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="d22be-232">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="d22be-233">Chrom Problem [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="d22be-233">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="d22be-234">Missbilligung des Eigenschaftenbereichs im Bereich "Elemente"</span><span class="sxs-lookup"><span data-stu-id="d22be-234">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="d22be-235">Der Bereich " **Eigenschaften** " im Bereich " **Elemente** " ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d22be-235">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="d22be-236">`console.dir($0)`Stattdessen in der **Konsole** ausführen.</span><span class="sxs-lookup"><span data-stu-id="d22be-236">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Der veraltete Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="d22be-238">Der veraltete **Eigenschaften** Bereich</span><span class="sxs-lookup"><span data-stu-id="d22be-238">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="d22be-239">Verweise</span><span class="sxs-lookup"><span data-stu-id="d22be-239">References</span></span>  

*   [<span data-ttu-id="d22be-240">Console. dir ()</span><span class="sxs-lookup"><span data-stu-id="d22be-240">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="d22be-241">$0</span><span class="sxs-lookup"><span data-stu-id="d22be-241">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="d22be-242">Unterstützung für App-Tastenkombinationen im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="d22be-242">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="d22be-243">App-Tastenkombinationen helfen Benutzern, häufige oder empfohlene Aufgaben in einer Web-App schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="d22be-243">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="d22be-244">Das Menü "App-Tastenkombinationen" wird nur für [Progressive Web-Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.</span><span class="sxs-lookup"><span data-stu-id="d22be-244">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Bereich "Manifest"" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="d22be-246">App-Verknüpfungen im Bereich " **Manifest** "</span><span class="sxs-lookup"><span data-stu-id="d22be-246">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="d22be-247">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="d22be-247">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="d22be-248">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="d22be-248">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="d22be-249">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d22be-249">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="d22be-250">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="d22be-250">Getting in touch with Microsoft Edge Devtools team</span></span>  

  

<span data-ttu-id="d22be-251">So besprechen Sie die neuen Features und Änderungen im Beitrag oder alles, was mit devtools zu tun hat:</span><span class="sxs-lookup"><span data-stu-id="d22be-251">To discuss the new features and changes in the post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="d22be-252">Senden Sie Ihr Feedback über das **Feedback** -Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="d22be-252">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="d22be-253">Tweet bei [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="d22be-253">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="d22be-254">Einen Vorschlag an [das gewünschte Web][TheWebWeWant] senden</span><span class="sxs-lookup"><span data-stu-id="d22be-254">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="d22be-255">Datei Fehler auf dieser Seite im [Edge-Entwickler-][GitHubMicrosoftDocsEdgeDeveloperNewIssue] Repository</span><span class="sxs-lookup"><span data-stu-id="d22be-255">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="d22be-257">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="d22be-257">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Symbol für devtools-Einstellungen"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "DevTools-Symbol zum Umschalten des Screencasts"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "DevTools-Symbol "Seite aktualisieren""
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "DevTools-Leistungs Panel-Daten Satz Symbol"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir-Console-API-Referenz | Microsoft docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Referenz | Microsoft docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Übersicht anpassen | Microsoft docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Suchen und Beheben von Problemen mit der Registerkarte "Microsoft Edge devtools Issues" | Microsoft docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit dem Remote Debuggen von Android-Geräten | Microsoft docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren | Microsoft docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit dem Remote Debuggen von Windows 10-Geräten | Microsoft docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource | Microsoft docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokoll Netzwerkaktivität | Microsoft docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows | Microsoft docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android-App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Leerzeichen getrennte funktionelle Farb Notationen-MDN | Kann ich verwenden"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: zulassen der Anpassung von Tastenkombinationen/Tastenkombinationen | Chrom Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatibel | Chrom Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Bereich "Formatvorlagen" | Chrom Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Anzeigen von grundlegenden a11y-Informationen in Element popover | Chrom Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools-UI-Unterstützung für Modus mit hohem Kontrast | Chrom Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chrom Fehler"  
[CR1068116]: https://crbug.com/1068116 "Bereich "Schiffs Probleme" | Chrom Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: die Farbauswahl sollte eine moderne CSS-Farb Syntax erstellen | Chrom Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Unterstützung für das CSS "Revert"-Schlüsselwort/-Wert hinzufügen | Chrom Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung-drawer Resizer"  
[CR1081486]: https://crbug.com/1081486 "Der Tastaturfokus ist für Navigationsschaltflächen im Screencast-Modus nicht sichtbar | Chrom Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte "erfüllt" sein, nicht "aufgelöst" | V8-Bugs"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen aus Farben 3-CSS-Farb Modulebene 4 | W3C CSS-Arbeitsgruppen-Editor-Entwürfe"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die Farbe-CSS-Farb Modulebene 4 | W3C CSS-Arbeitsgruppen-Editor-Entwürfe"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in das neue Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Staaten und Schicksale-Domenic/Promises-umbrechen | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "Zurücksetzen | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browser Kompatibilität | MDN"  

[VSCode]: https://code.visualstudio.com/ "Visual Studio-Code"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio-Code Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axt: Tastatur | Webhint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role-Wert | Webhint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus für hohen Kontrast in Windows | Windows-Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge – Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview-Kanäle"  
[TheWebWeWant]: https://aka.ms/webwewant "Das gewünschte Web"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="d22be-306">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d22be-306">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d22be-307">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/05/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d22be-307">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d22be-309">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d22be-309">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
