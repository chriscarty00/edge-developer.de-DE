---
description: Verwenden Sie die DevTools im Windows-Modus mit hohem Kontrast, passen Sie Tastenkombinationen in den DevTools an, Visual Studio Code zu ändern, und vieles mehr.
title: Neues in DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 01d41fe5400dde427a0ac73870ace0e1211f429a
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514389"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="11f3e-104">Neues in DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="11f3e-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="11f3e-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="11f3e-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="11f3e-106">Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="11f3e-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="11f3e-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="11f3e-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="11f3e-108">Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount]um über die neuesten und besten Features in Ihren Entwicklertools auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="11f3e-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="11f3e-109">Verwenden der DevTools im Windows-Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="11f3e-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="11f3e-110">Die Microsoft Edge DevTools werden jetzt im Modus mit hohem Kontrast angezeigt, wenn sich Windows im Modus mit hohem Kontrast befindet.</span><span class="sxs-lookup"><span data-stu-id="11f3e-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools im Modus mit hohem Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="11f3e-112">Microsoft Edge DevTools im Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="11f3e-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-113">[Befolgen Sie die Anweisungen, um den Modus mit hohem Kontrast in Windows zu aktivieren.][MicrosoftSupportWindows10HighContrastMode]</span><span class="sxs-lookup"><span data-stu-id="11f3e-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="11f3e-114">Wählen Sie oder aus, um die DevTools in Microsoft Edge `F12` zu `Ctrl` + `Shift` + `I` öffnen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="11f3e-115">Die DevTools werden im Modus mit hohem Kontrast angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11f3e-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="11f3e-116">Die Microsoft Edge DevTools unterstützen derzeit den Modus mit hohem Kontrast unter Windows, jedoch nicht unter macOS.</span><span class="sxs-lookup"><span data-stu-id="11f3e-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="11f3e-117">[Chromium-Problem #1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="11f3e-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="11f3e-118">Übereinstimmung von Tastenkombinationen in devTools mit Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="11f3e-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="11f3e-119">Aus Ihrem [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) und dem [Chromium-Problemverfolgungstool][CRIssuesList]für öffentliche Fragen hat das Microsoft Edge DevTools-Team erfahren, dass Sie die Möglichkeit haben wollten, Tastenkombinationen in den DevTools anzupassen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="11f3e-120">In Microsoft Edge 84 können Sie nun Tastenkombinationen in den DevTools mit [Visual Studio Code][VisualStudioCode]übereinstimmen. Dies ist nur eines der Features, an denen das Team für die Anpassung von Verknüpfungen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="11f3e-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Übereinstimmung von Tastenkombinationen in devTools mit Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="11f3e-122">Microsoft Edge DevTools im Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="11f3e-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-123">Um das Experiment zu testen, öffnen Sie devTools-Einstellungen, indem Sie in der oberen rechten Ecke der DevTools das Symbol `?` ![ DevTools-Einstellungen auswählen oder ][ImageSettingsIcon] auswählen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="11f3e-124">Navigieren Sie zum Abschnitt **Experimente,** und aktivieren Sie die Registerkarte Einstellungen für benutzerdefinierte Tastenkombinationen **aktivieren (erfordert neu laden).**</span><span class="sxs-lookup"><span data-stu-id="11f3e-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="11f3e-125">Laden Sie jetzt die DevTools neu, öffnen Sie die Einstellungen erneut, und navigieren Sie zum **Abschnitt Verknüpfungen.**</span><span class="sxs-lookup"><span data-stu-id="11f3e-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="11f3e-126">Wählen **Sie DevTools (Standard)** in der Dropdownliste **Verknüpfungen** abwählen aus, und wählen Sie **Visual Studio Code aus.**</span><span class="sxs-lookup"><span data-stu-id="11f3e-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="11f3e-127">Die Tastenkombinationen in den DevTools entsprechen jetzt den Verknüpfungen für entsprechende Aktionen in Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="11f3e-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="11f3e-128">Beispielsweise ist die Tastenkombination zum Anhalten oder Fortsetzen des Ausführens eines Skripts in [Visual Studio Code][VisualStudioCodeShortcuts] `F5` .</span><span class="sxs-lookup"><span data-stu-id="11f3e-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="11f3e-129">Mit der **Voreinstellung DevTools (Default)** ist dieselbe Verknüpfung in devTools, aber mit der voreingestellten `F8` Visual Studio **Code,** ist diese Verknüpfung jetzt auch `F5` .</span><span class="sxs-lookup"><span data-stu-id="11f3e-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="11f3e-130">Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar, teilen Sie ihr Feedback daher bitte [mit](#getting-in-touch-with-microsoft-edge-devtools-team) dem Team!</span><span class="sxs-lookup"><span data-stu-id="11f3e-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="11f3e-131">[Chromium-#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="11f3e-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="11f3e-132">Remotedebugger von Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="11f3e-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="11f3e-133">Sie können nun Remotedebuggern Ihrer Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, mithilfe der vollen Leistung von [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="11f3e-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="11f3e-134">Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von zusammenklappbaren Und Dual-Screen-Geräten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="11f3e-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="11f3e-135">Der Emulator führt das Betriebssystem Android aus und stellt die [Microsoft Edge Android-App bereit.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="11f3e-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="11f3e-136">Laden Sie Ihre Webinhalte in der [Microsoft Edge-App, und][AndroidEdge] debuggen Sie sie mit [den Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="11f3e-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge-App, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="11f3e-138">Die Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="11f3e-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-139">Die Seite in einer Desktopinstanz von Microsoft Edge zeigt `edge://inspect` **surfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs,][PwaIndex] die auf dem [Surface Duo-Emulator ausgeführt werden.][DualScreensAndroidEmulator] [][DesktopEdge]</span><span class="sxs-lookup"><span data-stu-id="11f3e-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf edge://inspect wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="11f3e-141">Auf `edge://inspect` der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11f3e-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="11f3e-142">Wählen **Sie Überprüfen** nach der Registerkarte oder dem PWA aus, die Sie debuggen möchten, um die Microsoft Edge [DevTools zu öffnen.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="11f3e-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="11f3e-143">[Befolgen Sie die schrittweise Anleitung zum Remotedebuggern Ihrer Webinhalte im Surface Duo-Emulator.][DevToolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="11f3e-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="11f3e-144">Ändern der Größe der DevTools-Schublade einfacher</span><span class="sxs-lookup"><span data-stu-id="11f3e-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="11f3e-145">In Microsoft Edge 83 oder früher konnten Sie die Größe der [DevTools-Drawer][DevToolsDrawer] nur ändern, indem Sie auf die Symbolleiste der Drawer zeigen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="11f3e-146">Die Drawer hat sich anders verhalten als die anderen Größenänderungssteuerelemente für Bereiche in den DevTools, in denen Sie auf den Rahmen des Bereichs zeigen, um die Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="11f3e-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="11f3e-147">Wählen Sie die folgende Abbildung aus, um die Größe der Drawer in Version 83 oder früher von Microsoft Edge zu ändern.</span><span class="sxs-lookup"><span data-stu-id="11f3e-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="11f3e-149">Ändern der Größe der DevTools-Schublade in Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="11f3e-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="11f3e-150">Ab Microsoft Edge 84 können Sie nun die Größe der Drawer ändern, indem Sie auf den Rahmen der Drawer zeigen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="11f3e-151">Diese Änderung richtet das Verhalten der Größenänderung der DevTools-Drawer an der Art und Weise aus, wie Sie die Größe anderer Bereiche in devTools ändern.</span><span class="sxs-lookup"><span data-stu-id="11f3e-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="11f3e-152">Wählen Sie das folgende Bild aus, um die Größe in Aktion in Microsoft Edge 84 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="11f3e-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="11f3e-154">Ändern der Größe der DevTools-Schublade in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="11f3e-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="11f3e-155">[Chromium-#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="11f3e-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="11f3e-156">Bildschirmcastnavigationsschaltflächen zeigen den Fokus an</span><span class="sxs-lookup"><span data-stu-id="11f3e-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="11f3e-157">Beim Remotedebugieren eines [Android-Geräts,][DevToolsRemoteDebugAndroid]eines Windows [10-Geräts][DevToolsRemoteDebugWindows]oder eines Surface [Duo-Emulators][DevToolsRemoteDebugDuoEmulator]können Sie screencasting mit dem Symbol Umschaltbildschirm in der oberen linken Ecke der ![ ][ImageScreencastingIcon] DevTools umschalten.</span><span class="sxs-lookup"><span data-stu-id="11f3e-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="11f3e-158">Wenn die Screencasting aktiviert ist, können Sie über das DevTools-Fenster auf der Registerkarte in Microsoft Edge auf dem Remotegerät navigieren.</span><span class="sxs-lookup"><span data-stu-id="11f3e-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="11f3e-159">In Microsoft Edge 84 sind diese Navigationsschaltflächen jetzt auch über die Tastatur zugänglich.</span><span class="sxs-lookup"><span data-stu-id="11f3e-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Wählen Sie Umschalt+Tab aus der bildschirmcastierten URL-Leiste zeigt den Fokus auf der Schaltfläche Aktualisieren an." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="11f3e-161">Select `Shift` + `Tab` from the screencasted URL bar shows focus on the **Refresh** button</span><span class="sxs-lookup"><span data-stu-id="11f3e-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="11f3e-162">[Chromium-#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="11f3e-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="11f3e-163">Zugriff auf den Detailbereich des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="11f3e-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="11f3e-164">In Microsoft Edge 84 steht \*\*\*\* der [Detailbereich][DevToolsNetworkDetails] im Netzwerktool jetzt im Fokus, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll öffnen.][DevToolsNetworkLog]</span><span class="sxs-lookup"><span data-stu-id="11f3e-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="11f3e-165">Mit dieser Änderung können Bildschirmlesegeräte den Inhalt des Detailbereichs **vorlesen und mit ihnen** interagieren.</span><span class="sxs-lookup"><span data-stu-id="11f3e-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Detailbereich im Netzwerkbereich hat beim Öffnen den Fokus" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="11f3e-167">Der **Detailbereich** im **Netzwerktool** hat beim Öffnen den Fokus</span><span class="sxs-lookup"><span data-stu-id="11f3e-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="11f3e-168">[Chromium-#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="11f3e-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="11f3e-169">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="11f3e-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="11f3e-170">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 84 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="11f3e-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="11f3e-171">Beheben von Websiteproblemen mit dem neuen Problemtool in der DevTools-Schublade</span><span class="sxs-lookup"><span data-stu-id="11f3e-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="11f3e-172">Das neue **Problemtool** in der DevTools-Schublade wurde erstellt, um die Benachrichtigungsmüdigkeit und unübersichtlich der Konsole **zu reduzieren.**</span><span class="sxs-lookup"><span data-stu-id="11f3e-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="11f3e-173">Derzeit ist **die Konsole** der zentrale Ort für Websiteentwickler, Bibliotheken, Frameworks und Microsoft Edge zum Protokollieren von Nachrichten, Warnungen und Fehlern.</span><span class="sxs-lookup"><span data-stu-id="11f3e-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="11f3e-174">Das **Problemtool** aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und aktionsfähige Weise, links zu betroffenen Ressourcen in Microsoft Edge DevTools und bietet Anleitungen zum Beheben der Probleme.</span><span class="sxs-lookup"><span data-stu-id="11f3e-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="11f3e-175">Im Laufe der Zeit werden immer mehr Warnungen in Microsoft Edge im Tool Probleme und nicht in der Konsole **angezeigt,** was dazu beitragen sollte, die Unübersichtlichkeit in der Konsole **zu reduzieren.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11f3e-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="11f3e-176">Navigieren Sie zu Suchen und Beheben von Problemen mit dem [Microsoft Edge DevTools-Tool,][DevtoolsIssuesIndex]um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-176">To get started, navigate to [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool Probleme in der DevTools-Schublade" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="11f3e-178">Das **Tool Probleme** in der DevTools-Schublade</span><span class="sxs-lookup"><span data-stu-id="11f3e-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-179">[Chromium-Problem #1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="11f3e-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="11f3e-180">Anzeigen von Barrierefreiheitsinformationen in der QuickInfo zum Überprüfungsmodus</span><span class="sxs-lookup"><span data-stu-id="11f3e-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="11f3e-181">Die **QuickInfo zum Überprüfen des** Modus gibt [][WebhintHintsAxeNameRoleValue] jetzt an, ob das Element über einen barrierefreien Namen und eine Rolle verfügt und [tastaturfokussierbar ist.][WebhintHintsAxeKeyboard]</span><span class="sxs-lookup"><span data-stu-id="11f3e-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Die QuickInfo zum Überprüfen des Modus mit Barrierefreiheitsinformationen" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="11f3e-183">Die **QuickInfo zum Überprüfen des Modus** mit Barrierefreiheitsinformationen</span><span class="sxs-lookup"><span data-stu-id="11f3e-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-184">[Chromium-#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="11f3e-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="11f3e-185">Aktualisierungen des Leistungsbereichs</span><span class="sxs-lookup"><span data-stu-id="11f3e-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="11f3e-186">Anzeigen von Informationen zur Sperrzeit insgesamt in der Fußzeile</span><span class="sxs-lookup"><span data-stu-id="11f3e-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="11f3e-187">Nach der Aufzeichnung der Ladeleistung zeigt der Bereich **Leistung** nun Informationen zur Gesamtblockierungszeit \(TBT\) in der Fußzeile an.</span><span class="sxs-lookup"><span data-stu-id="11f3e-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="11f3e-188">TBT ist eine Lastleistungsmetrik, die quantifiziert, wie lange eine Seite benötigt, um verwendbar zu werden.</span><span class="sxs-lookup"><span data-stu-id="11f3e-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="11f3e-189">Es misst im Wesentlichen, wie lange eine Seite verwendbar zu sein scheint \(da der Inhalt auf dem Bildschirm gerendert wird\); ist jedoch nicht wirklich verwendbar, da JavaScript den Hauptthread blockiert und die Seite daher nicht auf Benutzereingaben reagiert.</span><span class="sxs-lookup"><span data-stu-id="11f3e-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="11f3e-190">TBT ist die Hauptmetrik für die 1. Eingabeverzögerung.</span><span class="sxs-lookup"><span data-stu-id="11f3e-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="11f3e-191">Verwenden Sie nicht den Seitenaktualisierungssymbolworkflow aktualisieren, um Informationen zur Gesamtsperrungszeit zu erhalten, um die Leistung der \*\*\*\* ![ Seite zu ][ImageRefreshPageIcon] erfassen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="11f3e-192">Wählen Sie stattdessen **Datensatzsymbol** aus, laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden ![ Sie dann die ][ImageRecordIcon] Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="11f3e-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="11f3e-193">Wenn angezeigt wird, hat Microsoft Edge DevTools nicht die erforderlichen Informationen aus den internen `Total Blocking Time: Unavailable` Profilerstellungsdaten in Microsoft Edge erhalten.</span><span class="sxs-lookup"><span data-stu-id="11f3e-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Informationen zur Blockierungszeit insgesamt in der Fußzeile einer Aufzeichnung des Leistungsbereichs" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="11f3e-195">Informationen zur Blockierungszeit insgesamt in der Fußzeile einer **Aufzeichnung des Leistungsbereichs**</span><span class="sxs-lookup"><span data-stu-id="11f3e-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-196">[Chromium-#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="11f3e-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="11f3e-197">Layout Shift-Ereignisse im Abschnitt neue Besen</span><span class="sxs-lookup"><span data-stu-id="11f3e-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="11f3e-198">Der neue **Abschnitt "Erfahrung"** **des** Leistungsbereichs hilft Ihnen, Layoutverschiebungen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="11f3e-199">Kumulative Layoutverschiebung \(CLS\) ist eine Metrik, mit der Sie unerwünschte visuelle Instabilitäten quantifizieren können.</span><span class="sxs-lookup"><span data-stu-id="11f3e-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="11f3e-200">Wählen Sie **das Layout shift-Ereignis** aus, um die Details der Layoutverschiebung im **Zusammenfassungsbereich anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="11f3e-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="11f3e-201">Zeigen Sie auf die **Felder Verschoben von** und Zu **Feldern,** um zu visualisieren, wo die Layoutverschiebung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="11f3e-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Die Details einer Layoutverschiebung" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="11f3e-203">Die Details einer Layoutverschiebung</span><span class="sxs-lookup"><span data-stu-id="11f3e-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="11f3e-204">Präzisere Zusageterminologie in der Konsole</span><span class="sxs-lookup"><span data-stu-id="11f3e-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="11f3e-205">Bei der Protokollierung eines `Promise` hat **die Konsole** fälschlicherweise den Wert `PromiseStatus` auf `resolved` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11f3e-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Ein Beispiel für die Konsole mit der alten aufgelösten Terminologie" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="11f3e-207">Ein Beispiel für die **Konsole** mit der alten `resolved` Terminologie</span><span class="sxs-lookup"><span data-stu-id="11f3e-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-208">Die **Konsole** verwendet nun den Begriff `fulfilled` , der an der Spezifikation ausgerichtet `Promise` ist.</span><span class="sxs-lookup"><span data-stu-id="11f3e-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="11f3e-209">Weitere Informationen zur Spezifikation `Promise` finden Sie unter States and [Fates auf GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="11f3e-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Ein Beispiel für die Konsole mit der neuen erfüllten Terminologie" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="11f3e-211">Ein Beispiel für die **Konsole** mit der neuen `fulfilled` Terminologie</span><span class="sxs-lookup"><span data-stu-id="11f3e-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-212">V8-Problem [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="11f3e-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="11f3e-213">Aktualisierungen des Formatbereichs</span><span class="sxs-lookup"><span data-stu-id="11f3e-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="11f3e-214">Unterstützung für das Revert-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="11f3e-214">Support for the revert keyword</span></span>  

<span data-ttu-id="11f3e-215">Die Benutzeroberfläche für die \*\*\*\* automatische Vervollständigung des Bereichs Formatvorlagen erkennt nun das Schlüsselwort [CSS][MDNRevert] wiederherstellen, das den kaskadierten Wert einer Eigenschaft auf den vorherigen Wert zurück setzt, der auf die Formatierung des Elements angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="11f3e-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Festlegen des Werts einer eigenschaft, die zurückgesetzt werden soll" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="11f3e-217">Festlegen des Werts einer eigenschaft, die zurückgesetzt werden soll</span><span class="sxs-lookup"><span data-stu-id="11f3e-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-218">[Chromium-#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="11f3e-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="11f3e-219">Bildvorschau</span><span class="sxs-lookup"><span data-stu-id="11f3e-219">Image previews</span></span>  

<span data-ttu-id="11f3e-220">Zeigen Sie auf einen Wert im Bereich Formatvorlagen, um eine Vorschau des `background-image` Bilds in einer QuickInfo anzuzeigen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11f3e-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Zeigen auf einen Hintergrundbildwert" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="11f3e-222">Zeigen auf einen `background-image` Wert</span><span class="sxs-lookup"><span data-stu-id="11f3e-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-223">[Chromium-#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="11f3e-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="11f3e-224">Die Farbauswahl verwendet jetzt eine durch Leerzeichen getrennte funktionale Farbtonation.</span><span class="sxs-lookup"><span data-stu-id="11f3e-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="11f3e-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] gibt an, dass Farbfunktionen, z. B. , leerzeichen `rgb()` getrennte Argumente unterstützen sollen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="11f3e-226">So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="11f3e-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="11f3e-227">Wenn Sie Farben [][DevtoolsCssReferenceColorPicker] mit der Farbauswahl auswählen oder \*\*\*\* zwischen Farbdarstellungen im Formatvorlagenbereich wechseln, indem Sie den Wert halten und auswählen, wird die Syntax des durch Leerzeichen getrennten Arguments `Shift` `background-color` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11f3e-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Formatvorlagenbereich" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="11f3e-229">Verwenden von durch Leerzeichen getrennten Argumenten im **Formatvorlagenbereich**</span><span class="sxs-lookup"><span data-stu-id="11f3e-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="11f3e-230">Sie sollten auch die Syntax im **Bereich "Berechnet"** und in der **QuickInfo "Inspect Mode"** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="11f3e-231">Microsoft Edge DevTools verwendet die neue Syntax, da bevorstehende #A0 wie [color()][CSSWGDraftsColor4Property] die veraltete Argumentsyntax durch Kommas nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="11f3e-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="11f3e-232">Die Syntax des durch Leerzeichen getrennten Arguments wird in den meisten Browsern seit einer Weile unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11f3e-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="11f3e-233">Weitere Informationen finden Sie unter [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="11f3e-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="11f3e-234">[Chromium-#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="11f3e-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="11f3e-235">Veraltetes Anzeigen des Eigenschaftenbereichs im Elementbereich</span><span class="sxs-lookup"><span data-stu-id="11f3e-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="11f3e-236">Der **Eigenschaftenbereich** im **Elementtool** ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="11f3e-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="11f3e-237">Führen `console.dir($0)` Sie stattdessen in der **Konsole** aus.</span><span class="sxs-lookup"><span data-stu-id="11f3e-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Veralteter Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="11f3e-239">Veralteter **Eigenschaftenbereich**</span><span class="sxs-lookup"><span data-stu-id="11f3e-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="11f3e-240">Verweise</span><span class="sxs-lookup"><span data-stu-id="11f3e-240">References</span></span>  

*   [<span data-ttu-id="11f3e-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="11f3e-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="11f3e-242">$0</span><span class="sxs-lookup"><span data-stu-id="11f3e-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="11f3e-243">Unterstützung von App-Verknüpfungen im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="11f3e-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="11f3e-244">Mithilfe von App-Verknüpfungen können Benutzer häufige oder empfohlene Aufgaben in einer Web-App schnell starten.</span><span class="sxs-lookup"><span data-stu-id="11f3e-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="11f3e-245">Das Menü "App-Verknüpfungen" wird nur für [Progressive Web Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.</span><span class="sxs-lookup"><span data-stu-id="11f3e-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Manifestbereich" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="11f3e-247">App-Verknüpfungen im **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="11f3e-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="11f3e-248">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="11f3e-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="11f3e-249">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="11f3e-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="11f3e-250">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="11f3e-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="11f3e-251">Kontakt zum Microsoft Edge Devtools-Team</span><span class="sxs-lookup"><span data-stu-id="11f3e-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir – Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Referenz | Microsoft Docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Customize Overview | Microsoft Docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Suchen und Beheben von Problemen mit der Registerkarte Microsoft Edge DevTools-Probleme | Microsoft Docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Erste Schritte mit Remotedebugieren von Surface Duo-Emulatoren | Microsoft Docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit remote debugging Windows 10 Devices | Microsoft Docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Überprüfen Sie die Details der | Microsoft Docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollieren von Netzwerkaktivitäts| Microsoft Docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web Apps unter Windows | Microsoft Docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Durch Leerzeichen getrennte funktionale Farb notationen – MDN-| Kann ich verwenden"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium-Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium-Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Formatvorlagenbereich | Chromium-Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Zeigen Sie grundlegende a11y-Informationen in Elementpopover-| Chromium-Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools UI-Unterstützung für den Modus &quot;Hoher Kontrast&quot; | Chromium-Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium-Fehler"  
[CR1068116]: https://crbug.com/1068116 "Problembereich für | Chromium-Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: Die Farbauswahl sollte eine moderne CSS-Farbsyntax | Chromium-Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Fügen Sie Unterstützung für das Schlüsselwort/den Wert der CSS-| Chromium-Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung – Größenanpassung der Schublade"  
[CR1081486]: https://crbug.com/1081486 "Der Tastaturfokus ist für Navigationsschaltflächen im Screencastmodus nicht | Chromium-Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte &quot;erfüllt&quot; und nicht &quot;aufgelöst&quot; | V8-Fehler"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen von Farben 3 – CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die &quot;Farbe&quot; - CSS Color Module Level 4 | W3C CSS Working Group Editor Drafts"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in das neue Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "States and Fates – domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "Wiederherstellen | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browserkompatibilität | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: Tastatur | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus mit hohem Kontrast in Windows | Windows-Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview Channels"  
[TheWebWeWant]: https://aka.ms/webwewant "The Web We Want"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="11f3e-296">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11f3e-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="11f3e-297">Die ursprüngliche Seite befindet sich [hier](https://developer.chrome.com/blog/new-in-devtools-84) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="11f3e-297">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-84) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="11f3e-299">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="11f3e-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
