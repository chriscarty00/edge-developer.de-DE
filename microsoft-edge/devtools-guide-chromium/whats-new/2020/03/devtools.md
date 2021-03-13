---
description: Emulieren von Farbsichtschwächen, Dock To Left im Befehlsmenü und vieles mehr.
title: Neues in DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: f97155b12a679f630ce80c007e7f0ca693e19876
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408353"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a><span data-ttu-id="39c96-104">Neues in DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="39c96-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="39c96-105">Nach dem aktualisierten Chromium-Zeitplan passen wir unseren Zeitplan für anstehende Microsoft Edge-Versionen an und brechen die Microsoft Edge 82-Version ab.</span><span class="sxs-lookup"><span data-stu-id="39c96-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="39c96-106">Weitere Informationen finden Sie [in unserem][WindowsBlogStableRelease] Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="39c96-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="39c96-107">Hier sind die neuen Features, die in den DevTools in Microsoft Edge 83 verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="39c96-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="39c96-108">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="39c96-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="39c96-109">Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="39c96-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="39c96-110">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="39c96-110">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="39c96-111">Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount]um über die neuesten und besten Features in Ihren Entwicklertools auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="39c96-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a><span data-ttu-id="39c96-112">Remotedebuggern von Microsoft Edge auf Windows 10-Geräten</span><span class="sxs-lookup"><span data-stu-id="39c96-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="39c96-113">Die [Remotetools für Microsoft Edge \(Beta\)-App][RemoteTools] ist jetzt im [Microsoft Store verfügbar.][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="39c96-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="39c96-114">Mit dieser App, die das [Windows-Geräteportal][WindowsUwpDebugTestPerfDevicePortal]erweitert, können Sie von der Instanz von Microsoft Edge, die auf Ihrem Entwicklungscomputer ausgeführt wird, eine Verbindung mit einem Windows 10-Remotegerät herstellen, eine Liste der Ziele \(alle Registerkarten in Microsoft Edge und [PWAs,][ProgressiveWebAppsChromiumIndex] die auf dem Windows 10-Gerät geöffnet sind) anzeigen und die DevTools auf Ihrem Entwicklungscomputer für ein Ziel verwenden, das auf dem Remotegerät windows 10 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c96-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, display a list of targets \(all tabs in Microsoft Edge and [PWAs][ProgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Die im Microsoft Store verfügbare Remotetools für Microsoft Edge (Beta)-App" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="39c96-116">Die im Microsoft Store verfügbare Remotetools für [Microsoft Edge (Beta)-App][RemoteTools] [][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="39c96-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-117">[Lesen Sie unsere Anleitung zum Einrichten Ihres Windows 10-Geräts und Ihres Entwicklungscomputers für das Remotedebugen.][DevtoolsRemoteDebuggingWindows]</span><span class="sxs-lookup"><span data-stu-id="39c96-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="39c96-118">Teilen Sie uns Ihre Remotedebubuingerfahrung [mit,][PostTweetEdgeDevTools] indem Sie das Symbol Feedback senden [twittern](#getting-in-touch-with-microsoft-edge-devtools-team) oder aufrufen.</span><span class="sxs-lookup"><span data-stu-id="39c96-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <a name="new-ways-to-access-settings"></a><span data-ttu-id="39c96-119">Neue Möglichkeiten für den Zugriff auf Einstellungen</span><span class="sxs-lookup"><span data-stu-id="39c96-119">New ways to access Settings</span></span>  

<span data-ttu-id="39c96-120">Es gibt eine Menge von Einstellungen für die DevTools, die Sie anpassen können, damit die DevTools so aussehen, fühlen und funktionieren, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="39c96-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="39c96-121">In Microsoft Edge 83 ist der Zugriff [auf Einstellungen][DevtoolsCustomizeIndexSettings] in devTools jetzt viel einfacher.</span><span class="sxs-lookup"><span data-stu-id="39c96-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span>  <span data-ttu-id="39c96-122">Öffnen Sie Einstellungen mit dem Zahnradsymbol neben Konsolenwarnungen und dem Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="39c96-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Das Zahnradsymbol öffnet Einstellungen in den DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="39c96-124">Das Zahnradsymbol öffnet **Einstellungen** in den DevTools</span><span class="sxs-lookup"><span data-stu-id="39c96-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-125">Sie können Einstellungen auch [im][DevtoolsCustomizeIndexSettings] Hauptmenü unter **Weitere** Tools **öffnen.**</span><span class="sxs-lookup"><span data-stu-id="39c96-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Hauptmenü > Weitere Tools > Einstellungen" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="39c96-127">**Hauptmenü**  >  **Weitere Tools**  >  **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="39c96-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-128">[Chromium-Problem #1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="39c96-128">Chromium issue [#1050855][CR1050855]</span></span>

### <a name="new-and-improved-infobars"></a><span data-ttu-id="39c96-129">Neue und verbesserte Infoleisten</span><span class="sxs-lookup"><span data-stu-id="39c96-129">New and improved infobars</span></span>

<span data-ttu-id="39c96-130">Informationsbenachrichtigungsleisten \(infobars\) in DevTools haben jetzt ein verbessertes Aussehen und mehr Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="39c96-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="39c96-131">In Microsoft Edge 83 sind Infoleisten einfacher zu lesen und schaltflächen zur Verfügung zu stellen, damit Sie die entsprechende Aktion sofort ergreifen können.</span><span class="sxs-lookup"><span data-stu-id="39c96-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infoleiste zum drucken einer verminten Datei in Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="39c96-133">Infoleiste zum drucken einer verminten Datei in Microsoft Edge Version 83</span><span class="sxs-lookup"><span data-stu-id="39c96-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-134">[Chromium-#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="39c96-134">Chromium issue [#1056348][CR1056348]</span></span>

### <a name="navigate-the-color-picker-with-your-keyboard"></a><span data-ttu-id="39c96-135">Navigieren in der Farbauswahl mit der Tastatur</span><span class="sxs-lookup"><span data-stu-id="39c96-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="39c96-136">Die [Farbauswahl ist][DevtoolsCssReferenceColorPicker] eine GUI im [Bereich Elemente][DevtoolsCssIndex] zum Ändern `color` und `background-color` Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="39c96-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="39c96-137">In früheren Versionen von Microsoft Edge konnten \*\*\*\* Sie nicht mit der Tastatur im Abschnitt Schattierungen der [Farbauswahl][DevtoolsCssReferenceColorPicker] navigieren.</span><span class="sxs-lookup"><span data-stu-id="39c96-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Sie können nun ihre Tastatur verwenden, um die Auswahl im Abschnitt Schattierungen der Farbauswahl zu verschieben." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="39c96-139">Sie können nun ihre Tastatur verwenden, um die Auswahl im Abschnitt **Schattierungen** der [Farbauswahl zu verschieben.][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="39c96-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-140">In Microsoft Edge 83 können Sie nun die Tastatur verwenden, \*\*\*\* um die Auswahl im Abschnitt Schattierungen der Farbauswahl zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="39c96-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="39c96-141">[Chromium-#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="39c96-141">Chromium issue [#963183][CR963183]</span></span>  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a><span data-ttu-id="39c96-142">Registerkarte "Eigenschaften" wird jetzt nach einer Seitenaktualisierung auffüllt</span><span class="sxs-lookup"><span data-stu-id="39c96-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="39c96-143">In Microsoft Edge 81 und früheren Versionen wurde die Registerkarte **Eigenschaften** im [Bereich Elemente][DevtoolsCssIndex] durch Seitenaktualisierungen unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="39c96-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="39c96-144">Beim Aktualisieren der Seite wurden auf der Registerkarte **Eigenschaften** die Eigenschaften des aktuell ausgewählten Elements nicht auffüllt.</span><span class="sxs-lookup"><span data-stu-id="39c96-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="In Microsoft Edge 81 und früher war die Registerkarte Eigenschaften nach einer Seitenaktualisierung leer." lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="39c96-146">In Microsoft Edge 81 und früher war die Registerkarte **Eigenschaften** nach einer Seitenaktualisierung leer.</span><span class="sxs-lookup"><span data-stu-id="39c96-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-147">In Microsoft Edge 83 können Sie nun die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung auf der Registerkarte **Eigenschaften anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="39c96-147">In Microsoft Edge 83, you are now able to display the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="In Microsoft Edge 83 zeigt die Registerkarte Eigenschaften die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung an." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="39c96-149">In Microsoft Edge 83 zeigt die Registerkarte **Eigenschaften** die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung an.</span><span class="sxs-lookup"><span data-stu-id="39c96-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-150">[Chromium-#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="39c96-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a><span data-ttu-id="39c96-151">Verwenden der Pfeiltasten zum Scrollen im Tool "Änderungen"</span><span class="sxs-lookup"><span data-stu-id="39c96-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="39c96-152">Das **Tool Änderungen verfolgt** alle Änderungen, die Sie an CSS oder JavaScript in devTools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="39c96-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="39c96-153">Sie können das Tool **"Änderungen"** verwenden, um alle Ihre Änderungen schnell anzeigen und diese zu Ihrem Editor/Ihrer IDE zurück zu bringen.</span><span class="sxs-lookup"><span data-stu-id="39c96-153">You are able to use the **Changes tool** to quickly display all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="39c96-154">Um das Tool **Änderungen zu öffnen,** wählen Sie `Ctrl` + `Shift` + `P` in devTools aus, um das [Befehlsmenü zu öffnen, und][DevToolsCommandMenuIndex] geben Sie `changes` ein.</span><span class="sxs-lookup"><span data-stu-id="39c96-154">To open the **Changes tool**, select `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and type `changes`.</span></span>  <span data-ttu-id="39c96-155">Wählen Sie den Befehl **Änderungen anzeigen aus,** und führen Sie den Befehl Änderungen anzeigen aus, um das **Tool Änderungen** in der DevTools-Schublade zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39c96-155">choose and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="39c96-156">Wenn Sie eine Änderung an einer minifizierten Datei vorgenommen haben, können Sie mit dem Tool Änderungen horizontal scrollen, um den ganzen verminten Code anzeigen zu können. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="39c96-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to display all of your minified code.</span></span>  <span data-ttu-id="39c96-157">Ab Microsoft Edge 83 können Sie nun mit den Pfeiltasten auf der Tastatur horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="39c96-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="In Microsoft Edge 83 können Sie einen horizontalen Bildlauf mit den Pfeiltasten durchführen, um ihren verminten Code im Tool "Änderungen" anzeigen zu können." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="39c96-159">In Microsoft Edge 83 können Sie einen horizontalen Bildlauf mit den Pfeiltasten durchführen, um die Änderungen, die Sie am verminten Code vorgenommen haben, im Tool **"Änderungen" anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="39c96-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to display the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-160">Wenn Sie Bildschirmlesegeräte oder die Tastatur verwenden, um [][PostTweetEdgeDevTools] die DevTools zu navigieren, senden Sie uns Ihr Feedback, indem Sie an uns twittern oder das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) drücken!</span><span class="sxs-lookup"><span data-stu-id="39c96-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-161">[Chromium-#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="39c96-161">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="39c96-162">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="39c96-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="39c96-163">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 83 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="39c96-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <a name="emulate-vision-deficiencies"></a><span data-ttu-id="39c96-164">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="39c96-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="39c96-165">Öffnen Sie [die Registerkarte Rendering,][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] und verwenden Sie das neue **Feature "Visionsmangel** emulieren", um eine bessere Vorstellung davon zu erhalten, wie Personen mit unterschiedlichen Arten von Sehschwächen Ihre Website erleben.</span><span class="sxs-lookup"><span data-stu-id="39c96-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulieren von verschwommenen Visionen" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="39c96-167">Emulieren von verschwommenen Visionen</span><span class="sxs-lookup"><span data-stu-id="39c96-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-168">DevTools ist in der Lage, verschwommenes Sehen und die folgenden Arten von Farbsichtschwächen [zu emulieren.][ColorBlindnessTypes]</span><span class="sxs-lookup"><span data-stu-id="39c96-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="39c96-169">Farbvisionsmangel</span><span class="sxs-lookup"><span data-stu-id="39c96-169">Color Vision Deficiency</span></span> | <span data-ttu-id="39c96-170">Details</span><span class="sxs-lookup"><span data-stu-id="39c96-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="39c96-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="39c96-171">Protanopia</span></span> | <span data-ttu-id="39c96-172">Die Unfähigkeit, ein rotes Licht zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="39c96-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="39c96-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="39c96-173">Deuteranopia</span></span> | <span data-ttu-id="39c96-174">Die Unfähigkeit, grünes Licht zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="39c96-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="39c96-175">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="39c96-175">Tritanopia</span></span> | <span data-ttu-id="39c96-176">Die Unfähigkeit, blaues Licht zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="39c96-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="39c96-177">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="39c96-177">Achromatopsia</span></span> | <span data-ttu-id="39c96-178">Die Unfähigkeit, jede Farbe zu erkennen, mit Ausnahme von Grauschattierungen \(äußerst selten\).</span><span class="sxs-lookup"><span data-stu-id="39c96-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="39c96-179">Es gibt weniger extreme Versionen dieser Farbsichtschwächen, und tatsächlich sind sie häufiger.</span><span class="sxs-lookup"><span data-stu-id="39c96-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="39c96-180">Beispielsweise ist Protanomaly eine reduzierte Empfindlichkeit für rotes Licht (im Gegensatz zur Protanopie, was die vollständige Unfähigkeit ist, rotes Licht zu erkennen).</span><span class="sxs-lookup"><span data-stu-id="39c96-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="39c96-181">Diese **-omaly** vision-Mängel sind jedoch nicht so klar definiert: Jede Person mit einem solchen Sehschwäche ist anders und sieht die Dinge möglicherweise anders \(in der Lage, mehr/weniger der relevanten Farben zu erkennen\).</span><span class="sxs-lookup"><span data-stu-id="39c96-181">However, these **-omaly** vision deficiencies are not as clearly defined:  every person with such a vision deficiency is different and may see things differently \(being able to perceive more/less of the relevant colors\).</span></span>  

<span data-ttu-id="39c96-182">Durch das Entwerfen für extremere Simulationen in DevTools sind Ihre Web-Apps garantiert auch für Personen mit protanomaly, deuteranomaly, tritanomaly und achromatomaly zugänglich.</span><span class="sxs-lookup"><span data-stu-id="39c96-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="39c96-183">Senden Sie Ihr Feedback, [indem Sie][PostTweetEdgeDevTools] das Symbol Feedback senden twittern oderchoosing! [](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="39c96-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-184">[Chromium-#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="39c96-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <a name="emulate-locales"></a><span data-ttu-id="39c96-185">Emulieren von Locales</span><span class="sxs-lookup"><span data-stu-id="39c96-185">Emulate locales</span></span>  

<span data-ttu-id="39c96-186">Emulieren von Locales durch Festlegen einer Position in **Sensors**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="39c96-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="39c96-187">[Öffnen Sie das **Befehlsmenü,** ][DevToolsCommandMenuIndex] und geben `Sensors` Sie ein, um auf die Registerkarte **Sensoren zu** zugreifen.  Nach dem Ausführen dieser Aktionen ändert DevTools das aktuelle Standard-Locale, was sich auf den folgenden Code ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="39c96-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="39c96-188">APIs, z. B.:</span><span class="sxs-lookup"><span data-stu-id="39c96-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="39c96-189">Andere locale- aware JavaScript-APIs wie `String.prototype.localeCompare` und `*.prototype.toLocaleString` , z. B.:</span><span class="sxs-lookup"><span data-stu-id="39c96-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="39c96-190">DOM-APIs wie `navigator.language` und</span><span class="sxs-lookup"><span data-stu-id="39c96-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="39c96-191">Der [Header der Accept-Language-HTTP-Anforderung][MDNAcceptLanguage]</span><span class="sxs-lookup"><span data-stu-id="39c96-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="39c96-192">Aktualisierungen `navigator.language` an und werden nicht sofort angezeigt, sondern erst nach der nächsten Navigation oder `navigator.languages` Seitenaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="39c96-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="39c96-193">Änderungen am `Accept-Language` HTTP-Header werden nur für nachfolgende Anforderungen widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="39c96-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulieren eines Locale" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="39c96-195">Emulieren eines Locale</span><span class="sxs-lookup"><span data-stu-id="39c96-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-196">Navigieren Sie zum Beispiel [locale-dependent code,][MathiasByensLocaleDemo]um eine Demo zu testen.</span><span class="sxs-lookup"><span data-stu-id="39c96-196">To try a demo, navigate to [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="39c96-197">[Chromium-#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="39c96-197">Chromium issue [#1051822][CR1051822]</span></span>

### <a name="cross-origin-embedder-policy-coep-debugging"></a><span data-ttu-id="39c96-198">Debuggen von Cross-Origin Embedder Policy (COEP)</span><span class="sxs-lookup"><span data-stu-id="39c96-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="39c96-199">Der Bereich Netzwerk stellt nun Informationen zum Debuggen von [Ursprungseinbettungsrichtlinien][COEP] zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39c96-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="39c96-200">Die **Spalte Status** enthält nun eine kurze Erläuterung, warum eine Anforderung blockiert wurde, sowie einen Link zum Anzeigen der Kopfzeilen dieser Anforderung zum weiteren Debuggen:</span><span class="sxs-lookup"><span data-stu-id="39c96-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Blockierte Anforderungen in der Spalte **Status**" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="39c96-202">Blockierte Anforderungen in der **Spalte Status**</span><span class="sxs-lookup"><span data-stu-id="39c96-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-203">Der **Abschnitt Antwortkopfzeilen** auf der Registerkarte **Kopfzeilen** enthält weitere Anleitungen zum Beheben der Probleme:</span><span class="sxs-lookup"><span data-stu-id="39c96-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Weitere Anleitungen im Abschnitt Antwortkopfzeilen" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="39c96-205">Weitere Anleitungen im **Abschnitt Antwortkopfzeilen**</span><span class="sxs-lookup"><span data-stu-id="39c96-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-206">Senden Sie Ihr Feedback, [indem Sie][PostTweetEdgeDevTools] das Symbol Feedback senden twittern oderchoosing! [](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="39c96-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-207">[Chromium-#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="39c96-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="39c96-208">Neue Symbole für Haltepunkte, bedingte Haltepunkte und Protokollpunkte</span><span class="sxs-lookup"><span data-stu-id="39c96-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="39c96-209">Der Bereich Quellen enthält neue Symbole für Haltepunkte, bedingte Haltepunkte und Protokollpunkte:</span><span class="sxs-lookup"><span data-stu-id="39c96-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="39c96-210">Haltepunkte \(</span><span class="sxs-lookup"><span data-stu-id="39c96-210">Breakpoints \(</span></span>![Haltepunkt](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="39c96-212">\) werden durch rote Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39c96-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="39c96-213">Bedingte Haltepunkte \(</span><span class="sxs-lookup"><span data-stu-id="39c96-213">Conditional Breakpoints \(</span></span>![Bedingter Haltepunkt](../../media/2020/03/conditional.msft.png)<span data-ttu-id="39c96-215">\) werden durch halbrote halbweiße Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39c96-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="39c96-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="39c96-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="39c96-218">\) werden durch rote Kreise mit Konsolensymbolen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39c96-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="39c96-219">Die Motivation für die neuen Symbole war, die Benutzeroberfläche mit anderen GUI-Debuggingtools \(die in der Regel rote Haltepunkte rot\) konsistenter zu machen und die Unterscheidung zwischen den drei Features auf einen Blick zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="39c96-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="39c96-220">[Chromium-#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="39c96-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a><span data-ttu-id="39c96-221">Anzeigen von Netzwerkanforderungen, die einen bestimmten Cookiepfad festlegen</span><span class="sxs-lookup"><span data-stu-id="39c96-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="39c96-222">Verwenden Sie das neue Filterschlüsselwort im Netzwerktool, um sich auf die Netzwerkanforderungen zu `cookie-path` konzentrieren, die einen bestimmten [Cookiepfad festlegen.][MDNCookiePath] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="39c96-222">Use the new `cookie-path` filter keyword in the **Network** tool to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="39c96-223">Weitere Schlüsselwörter [wie "Filter requests by properties"][DevtoolsNetworkReferenceFilterRequestsProperties] finden Sie unter Filtern von Anforderungen nach `cookie-path` Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39c96-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <a name="dock-to-left-from-the-command-menu"></a><span data-ttu-id="39c96-224">Vom Befehlsmenü nach links andocken</span><span class="sxs-lookup"><span data-stu-id="39c96-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="39c96-225">Öffnen Sie [das Befehlsmenü,][DevToolsCommandMenuIndex] und führen Sie den `Dock to left` Befehl aus, um DevTools links vom Viewport zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="39c96-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, die links vom Viewport angedockt sind" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="39c96-227">DevTools, die links vom Viewport angedockt sind</span><span class="sxs-lookup"><span data-stu-id="39c96-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="39c96-228">Das **Dock to left-Feature** steht seit Microsoft Edge 75 zur Verfügung, war aber zuvor nur über das [Hauptmenü zugänglich.][DevtoolsCustomizePlacementsChangeMainMenu]</span><span class="sxs-lookup"><span data-stu-id="39c96-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="39c96-229">Das neue Feature in Microsoft Edge 83 ist, dass Sie nun über das Befehlsmenü auf dieses Feature zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="39c96-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="39c96-230">Senden Sie Ihr Feedback, [indem Sie][PostTweetEdgeDevTools] das Symbol Feedback senden twittern oderchoosing! [](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="39c96-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-231">[Chromium-#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="39c96-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a><span data-ttu-id="39c96-232">Der Prüfbereich ist jetzt das Bereich "Leuchttürme".</span><span class="sxs-lookup"><span data-stu-id="39c96-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="39c96-233">Das DevTools-Team hat häufig Feedback von Webentwicklern erhalten, dass es zwar [möglich war, "Faroty"][GithubGoogleChromeLighthouse] von DevTools ausführen zu können, aber als sie es ausprobiert haben, konnten sie das Panel "Leuchtturm" nicht finden, sodass das Panel "Audits" jetzt das **Panel "Leuchttürme"** ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="39c96-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Das Leuchttürmenpanel" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="39c96-235">Das Leuchttürmenpanel</span><span class="sxs-lookup"><span data-stu-id="39c96-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="39c96-236">Das **Bereich "Leuchttürme"** enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="39c96-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="39c96-237">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle daten, die sie sammeln können.</span><span class="sxs-lookup"><span data-stu-id="39c96-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <a name="delete-all-local-overrides-in-a-folder"></a><span data-ttu-id="39c96-238">Löschen aller lokalen Außerkraftsetzungen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="39c96-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="39c96-239">Nachdem Sie **lokale** Außerkraftsetzungen eingerichtet haben, können Sie mit dem Mauszeiger auf ein \*\*\*\* Verzeichnis zeigen, das Kontextmenü \(mit der rechten Maustaste auf\) öffnen und die neue Option Alle Außerkraftsetzungen löschen auswählen, um alle lokalen Außerkraftsetzungen in diesem Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="39c96-239">After setting up **Local Overrides** you may hover on a directory, open the contextual menu \(right-click\), and choose the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Löschen aller Außerkraftsetzungen" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="39c96-241">Löschen aller Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="39c96-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-242">Senden Sie Ihr Feedback, [indem Sie][PostTweetEdgeDevTools] das Symbol Feedback senden twittern oderchoosing! [](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="39c96-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-243">[Chromium-#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="39c96-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <a name="updated-long-tasks-ui"></a><span data-ttu-id="39c96-244">Benutzeroberfläche für lange Aufgaben aktualisiert</span><span class="sxs-lookup"><span data-stu-id="39c96-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="39c96-245">Eine **lange Aufgabe** ist JavaScript-Code, der den Hauptthread für eine lange Zeit eindrist, was dazu führt, dass eine Webseite einfriert.</span><span class="sxs-lookup"><span data-stu-id="39c96-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="39c96-246">Sie können lange [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] Aufgaben seit einer Weile im Bereich Leistung visualisieren, aber in Microsoft Edge 83 wurde die Benutzeroberfläche für die Visualisierung langer Aufgaben im Bereich Leistung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="39c96-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="39c96-247">Der Teil "Lange Aufgabe" eines Vorgangs wird nun mit einem streifenroten Hintergrund eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="39c96-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Die neue Benutzeroberfläche für lange Aufgaben" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="39c96-249">Die neue Benutzeroberfläche für lange Aufgaben</span><span class="sxs-lookup"><span data-stu-id="39c96-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="39c96-250">Senden Sie Ihr Feedback, [indem Sie][PostTweetEdgeDevTools] das Symbol Feedback senden twittern oderchoosing! [](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="39c96-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="39c96-251">[Chromium-#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="39c96-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <a name="maskable-icon-support-in-the-manifest-pane"></a><span data-ttu-id="39c96-252">Maskierbare Symbolunterstützung im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="39c96-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="39c96-253">Android Oreo hat adaptive Symbole eingeführt, die App-Symbole in einer Vielzahl von Formen in verschiedenen Gerätemodellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c96-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="39c96-254">**Maskierbare Symbole** sind ein neues Symbolformat, das adaptive Symbole unterstützt, mit denen Sie sicherstellen können, dass Ihr [PWA-Symbol][ProgressiveWebAppsChromiumIndex] auf Geräten gut aussieht, die den Standard für maskierbare Symbole unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39c96-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][ProgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="39c96-255">Aktivieren Sie das neue Kontrollkästchen Nur den minimalen sicheren Bereich für **maskierbare** Symbole im **Manifestbereich** anzeigen, um zu überprüfen, ob Ihr maskierbares Symbol auf Android Oreo-Geräten gut aussieht.</span><span class="sxs-lookup"><span data-stu-id="39c96-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Kontrollkästchen nur den minimalen sicheren Bereich für maskierbare Symbole anzeigen" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="39c96-257">Das **Kontrollkästchen Nur den minimalen sicheren Bereich für maskierbare Symbole** anzeigen</span><span class="sxs-lookup"><span data-stu-id="39c96-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="39c96-258">Dieses Feature wurde in Microsoft Edge 81 gestartet.</span><span class="sxs-lookup"><span data-stu-id="39c96-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="39c96-259">Die hier in Microsoft Edge 83 behandelten Updates wurden in [What's New In DevTools (Microsoft Edge 81) nicht behandelt.][WhatsNew81]</span><span class="sxs-lookup"><span data-stu-id="39c96-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="39c96-260">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="39c96-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="39c96-261">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c96-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="39c96-262">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="39c96-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="39c96-263">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="39c96-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Neues in DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Führen Sie Befehle mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit dem Farbauswahl-| Microsoft Docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Ändern der Platzierung aus dem Hauptmenü | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Anzeigen der Hauptthreadaktivität | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte Rendering | Microsoft Docs"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web Apps unter Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit remote debugging Windows 10 Devices | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Zeilen-von-Code-Haltepunkte – So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filteranforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Übersicht über das Windows-Geräteportal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Remotetools für Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Update für Stable-Kanalversionen für Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem – MicrosoftDocs/Edge-Entwickler – GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter-Konto"  
[TheWebWeWant]: https://webwewant.fyi "The Web We Want"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Arten von Farbblindheit"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie-| MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Locale-dependent code example"  

[CR963183]: https://crbug.com/963183 "Problem 963183: DevTools sind nicht WCAG-kompatibel"  
[CR1003700]: https://crbug.com/1003700 "Issue 1003700: Add DevTools support for Color Vision Deficiency simulation"  
[CR1011679]: https://crbug.com/1011679 "Problem 1011679: Einführung von "Dock nach links" mithilfe des Befehlsmenüs"  
[CR1016501]: https://crbug.com/1016501 "Problem 1016501: Featureanforderung: Schaltfläche zum Löschen aller lokalen Überschreibungen"  
[CR1050999]: https://crbug.com/1050999 "Problem 1050999: Registerkarte Eigenschaften"  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: Unterstützung des COOP/COEP-Debuggings in DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problem 1054447: Aktualisieren von Leistungsmetriken in der DevTools-Zeitachse"  
[CR1051822]: https://crbug.com/1051822 "Problem 1051822: DevTools: Hinzufügen einer Benutzeroberfläche zum Emulieren des Locale"
[CR1041830]: https://crbug.com/1041830 "Problem 1041830: Verbessern von Farben für Haltepunkte"
[CR1050855]: https://crbug.com/1050855 "Problem 1050855: Einstellungsansicht ist schwer zu erkennen"
[CR1056348]: https://crbug.com/1056348 "Problem 1056348: Aktualisierung der Infoleistenkomponente"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP und COEP erläutert – Cross-Origin Opener Policy"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 ""COOP" und "COEP" erläutert – Richtlinie für einbettende Herkunft"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Leuchttürme | GitHub"  

> [!NOTE]
> <span data-ttu-id="39c96-305">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c96-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="39c96-306">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/03/devtools/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="39c96-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="39c96-308">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39c96-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
