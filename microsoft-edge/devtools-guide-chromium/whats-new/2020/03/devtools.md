---
title: Neuerungen in devtools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/31/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: f90bbde9b2b220cd8a333a81d520d4c6e56eaa90
ms.sourcegitcommit: 4e6c0959bc01eb0ceb4b85dce791670916fb5b48
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2020
ms.locfileid: "10918634"
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

# <span data-ttu-id="6e820-103">Neuerungen in devtools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="6e820-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="6e820-104">Nach dem aktualisierten Chrom-Terminplan passen wir unseren Zeitplan für bevorstehende Microsoft Edge-Versionen an und kündigen die Microsoft Edge 82-Version.</span><span class="sxs-lookup"><span data-stu-id="6e820-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="6e820-105">Schauen Sie sich unseren [Blogbeitrag][WindowsBlogStableRelease] an, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e820-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="6e820-106">Hier sind die neuen Features, die im devtools in Microsoft Edge 83 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6e820-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="6e820-107">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="6e820-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="6e820-108">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="6e820-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="6e820-109">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="6e820-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="6e820-110">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="6e820-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="6e820-111">Remotedebuggen von Microsoft Edge auf Windows 10-Geräten</span><span class="sxs-lookup"><span data-stu-id="6e820-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="6e820-112">Die [Remote Tools für Microsoft Edge \ (Beta \)-][RemoteTools] APP ist jetzt im [Microsoft Store][MicrosoftStore]verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e820-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="6e820-113">Mit dieser APP, die das [Windows-Geräte Portal][WindowsUwpDebugTestPerfDevicePortal]erweitert, können Sie eine Verbindung von der Instanz von Microsoft Edge, die auf Ihrem Entwicklungscomputer ausgeführt wird, mit einem Windows 10-Remotegerät herstellen, eine Liste der Ziele anzeigen (alle Registerkarten in Microsoft Edge und [PWAs][PprgressiveWebAppsChromiumIndex] werden auf dem Windows 10-Gerät geöffnet), und die devtools auf dem Entwicklungscomputer für ein Ziel verwenden, das auf dem Remote</span><span class="sxs-lookup"><span data-stu-id="6e820-113">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Die im Microsoft Store verfügbare Remote Tools für Microsoft Edge (Beta)-app" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="6e820-115">Abbildung 1: die APP [Remote Tools für Microsoft Edge (Beta)][RemoteTools] , die im [Microsoft Store][MicrosoftStore] verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="6e820-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-116">[Lesen Sie unseren Leitfaden zum Einrichten Ihres Windows 10-Geräts und ihres Entwicklungscomputers für das Remotedebuggen][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="6e820-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="6e820-117">Informieren Sie uns über Ihre Remote Debugging-Erfahrung, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="6e820-118">Neue Möglichkeiten für den Zugriff auf Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6e820-118">New ways to access Settings</span></span>  

<span data-ttu-id="6e820-119">Es gibt Unmengen von Einstellungen für die devtools, die Sie anpassen können, um die devtools aussehen zu lassen, zu fühlen und zu arbeiten, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="6e820-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="6e820-120">In Microsoft Edge 83 ist der Zugriff auf die [Einstellungen][DevtoolsCustomizeIndexSettings] im devtools jetzt viel einfacher.</span><span class="sxs-lookup"><span data-stu-id="6e820-120">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="6e820-121">Öffnen Sie die Einstellungen mit dem Zahnradsymbol neben "Console Alerts" und dem Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="6e820-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Das Zahnradsymbol öffnet die Einstellungen im devtools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="6e820-123">Abbildung 2: das Zahnradsymbol öffnet die **Einstellungen** im devtools</span><span class="sxs-lookup"><span data-stu-id="6e820-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-124">Sie können die [Einstellungen][DevtoolsCustomizeIndexSettings] auch über das Hauptmenü unter **"** **Weitere Tools**" öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e820-124">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Hauptmenü > weitere Tools > Einstellungen" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="6e820-126">Abbildung 3: **Hauptmenü**  >  **Weitere**  >  **Einstellungen** für Tools</span><span class="sxs-lookup"><span data-stu-id="6e820-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-127">Chrom Problem [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="6e820-127">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="6e820-128">Neue und verbesserte infobars</span><span class="sxs-lookup"><span data-stu-id="6e820-128">New and improved infobars</span></span>

<span data-ttu-id="6e820-129">Informations Benachrichtigungs leisten \ (Infoleisten \) in devtools haben nun ein verbessertes Aussehen und mehr Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="6e820-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="6e820-130">In Microsoft Edge 83 können infobars leichter gelesen und Schaltflächen bereitgestellt werden, damit Sie die relevante Aktion sofort durchführen können.</span><span class="sxs-lookup"><span data-stu-id="6e820-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="6e820-132">Abbildung 4: Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge, Version 83</span><span class="sxs-lookup"><span data-stu-id="6e820-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-133">Chrom Problem [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="6e820-133">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="6e820-134">Navigieren in der Farbauswahl mit der Tastatur</span><span class="sxs-lookup"><span data-stu-id="6e820-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="6e820-135">Bei der [Farbauswahl][DevtoolsCssReferenceColorPicker] handelt es sich um eine Benutzeroberfläche für Änderungen und Deklarationen im [Element Panel][DevtoolsCssIndex] `color` `background-color` .</span><span class="sxs-lookup"><span data-stu-id="6e820-135">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="6e820-136">In früheren Versionen von Microsoft Edge konnten Sie nicht über die Tastatur in der [Farbauswahl][DevtoolsCssReferenceColorPicker] im Bereich " **Schattierungen** " navigieren.</span><span class="sxs-lookup"><span data-stu-id="6e820-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Sie können jetzt Ihre Tastatur verwenden, um die Auswahl im Bereich "Schattierungen" der Farbauswahl zu verschieben." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="6e820-138">Abbildung 5: Sie können nun Ihre Tastatur verwenden, um die Auswahl im Bereich " **Schattierungen** " der [Farbauswahl][DevtoolsCssReferenceColorPicker] zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6e820-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-139">In Microsoft Edge 83 können Sie nun die Tastatur verwenden, um den Auswahlbereich im Abschnitt **Schattierungen** der Farbauswahl zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6e820-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="6e820-140">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="6e820-140">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="6e820-141">Die Registerkarte "Eigenschaften" wird nun nach einer Seitenaktualisierung gefüllt</span><span class="sxs-lookup"><span data-stu-id="6e820-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="6e820-142">In Microsoft Edge 81 und früheren Versionen wurde die **Registerkarte Eigenschaften** im [Element Panel][DevtoolsCssIndex] durch Seitenaktualisierungen unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="6e820-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="6e820-143">Wenn Sie die Seite aktualisiert haben, wurden die Eigenschaften des aktuell ausgewählten Elements auf der **Registerkarte Eigenschaften** nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6e820-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="In Microsoft Edge 81 und früher war die Registerkarte "Eigenschaften" nach einer Seitenaktualisierung leer" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="6e820-145">Abbildung 6: in Microsoft Edge 81 und früher war die **Registerkarte "Eigenschaften"** nach einer Seitenaktualisierung leer</span><span class="sxs-lookup"><span data-stu-id="6e820-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-146">In Microsoft Edge 83 können Sie nun die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung auf der **Registerkarte Eigenschaften**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e820-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="In Microsoft Edge 83 werden auf der Registerkarte "Eigenschaften" die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="6e820-148">Abbildung 7: in Microsoft Edge 83 werden auf der **Registerkarte "Eigenschaften"** die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e820-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-149">Chrom Problem [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="6e820-149">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="6e820-150">Verwenden Sie die Pfeiltasten, um im Tool "Änderungen" zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="6e820-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="6e820-151">Das **Tool "Änderungen"** verfolgt alle Änderungen, die Sie an CSS oder JavaScript im devtools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="6e820-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="6e820-152">Sie können das **Tool "Änderungen"** verwenden, um schnell alle Ihre Änderungen anzuzeigen und diese wieder in Ihren Editor/Ihre IDE zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="6e820-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="6e820-153">Öffnen Sie das **Tool "Änderungen** ", indem `Ctrl` + `Shift` + `P` Sie auf die devtools drücken, um das [Befehlsmenü][DevToolsCommandMenuIndex] zu öffnen und einzugeben `changes` .</span><span class="sxs-lookup"><span data-stu-id="6e820-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="6e820-154">Wählen Sie den Befehl **Änderungen anzeigen** aus, und führen Sie ihn aus, um das **Tool Änderungen** im devtools-Einzug zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e820-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="6e820-155">Wenn Sie eine Änderung an einer minimierte-Datei vorgenommen haben, können Sie mit dem **Tool "Änderungen"** horizontal scrollen, um den gesamten minimierte-Code anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e820-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="6e820-156">Ab Microsoft Edge 83 können Sie jetzt mit den Pfeiltasten auf der Tastatur horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="6e820-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="In Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um Ihren minimierte-Code im Tool "Änderungen" anzuzeigen." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="6e820-158">Abbildung 8: in Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um die am minimierte-Code vorgenommenen Änderungen im **Tool "Änderungen"** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e820-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-159">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie uns Ihr Feedback, indem Sie uns [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-160">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="6e820-160">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="6e820-161">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="6e820-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="6e820-162">In den folgenden Abschnitten werden weitere in Microsoft Edge 83 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="6e820-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="6e820-163">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="6e820-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="6e820-164">Öffnen Sie die [Registerkarte "Rendering"][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] , und verwenden Sie das neue Feature "nach **eifern des Sehvermögens** ", um eine bessere Vorstellung davon zu erhalten, wie Personen mit unterschiedlichen Arten von Sehstörungen Ihre Website erleben.</span><span class="sxs-lookup"><span data-stu-id="6e820-164">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulieren verschwommener Sehkraft" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="6e820-166">Abbildung 9: emulieren verschwommener Visionen</span><span class="sxs-lookup"><span data-stu-id="6e820-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-167">DevTools ist in der Lage, unscharfe Sehkraft und die folgenden [Arten von farbsehstörungen][ColorBlindnessTypes]zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="6e820-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="6e820-168">Farbsehstörungen</span><span class="sxs-lookup"><span data-stu-id="6e820-168">Color Vision Deficiency</span></span> | <span data-ttu-id="6e820-169">Details</span><span class="sxs-lookup"><span data-stu-id="6e820-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="6e820-170">Protanopie</span><span class="sxs-lookup"><span data-stu-id="6e820-170">Protanopia</span></span> | <span data-ttu-id="6e820-171">Die Unfähigkeit, jedes rote Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6e820-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="6e820-172">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="6e820-172">Deuteranopia</span></span> | <span data-ttu-id="6e820-173">Die Unfähigkeit, grünes Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6e820-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="6e820-174">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="6e820-174">Tritanopia</span></span> | <span data-ttu-id="6e820-175">Die Unfähigkeit, ein blaues Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6e820-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="6e820-176">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="6e820-176">Achromatopsia</span></span> | <span data-ttu-id="6e820-177">Die Unfähigkeit, eine beliebige Farbe wahrzunehmen, mit Ausnahme von Grautönen \ (extrem selten \).</span><span class="sxs-lookup"><span data-stu-id="6e820-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="6e820-178">Es gibt weniger Extreme Versionen dieser farbsehstörungen, und tatsächlich sind Sie häufiger.</span><span class="sxs-lookup"><span data-stu-id="6e820-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="6e820-179">Bei Protanomalie handelt es sich beispielsweise um eine reduzierte Empfindlichkeit für rotes Licht (im Gegensatz zu Protanopie, was die vollständige Unfähigkeit, rotes Licht wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="6e820-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="6e820-180">Allerdings sind diese omaly Sehstörungen nicht so klar definiert: jede Person mit einem solchen Sehstörungen ist anders und kann die Dinge anders sehen (in der Lage sein, mehr/weniger der relevanten Farben wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="6e820-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="6e820-181">Wenn Sie für die extremeren Simulationen in devtools entwerfen, sind Ihre Web-Apps garantiert auch für Personen mit Protanomalie, Deuteranomalie, Tritanomaly und achromatomaly zugänglich.</span><span class="sxs-lookup"><span data-stu-id="6e820-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="6e820-182">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-183">Chrom Problem [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="6e820-183">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="6e820-184">Emulieren von Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="6e820-184">Emulate locales</span></span>  

<span data-ttu-id="6e820-185">Emulieren Sie Gebietsschemas, indem Sie einen Speicherort im **Sensor**  >  **Standort**festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e820-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="6e820-186">[Öffnen Sie das **Menübefehl** ][DevToolsCommandMenuIndex] , und geben Sie den Namen `Sensors` ein, um auf den Reiter **Sensoren** zuzugreifen.  Nach dem Ausführen dieser Aktionen ändert devtools das aktuelle Standardgebietsschema, was sich auf den folgenden Code auswirkt.</span><span class="sxs-lookup"><span data-stu-id="6e820-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="6e820-187">APIs, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="6e820-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="6e820-188">Andere JavaScript-APIs für Gebietsschema, beispielsweise `String.prototype.localeCompare` und `*.prototype.toLocaleString` , beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="6e820-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="6e820-189">DOM-APIs wie `navigator.language` und</span><span class="sxs-lookup"><span data-stu-id="6e820-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="6e820-190">Der [`Accept-Language`][MDNAcceptLanguage] HTTP-Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="6e820-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="6e820-191">Updates für `navigator.language` und `navigator.languages` werden nicht sofort, sondern nur nach der nächsten Navigation oder Seitenaktualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e820-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="6e820-192">Änderungen am `Accept-Language` http-Header werden nur für nachfolgende Anforderungen wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="6e820-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulieren eines Gebietsschemas" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="6e820-194">Abbildung 10: Emulieren eines Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="6e820-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-195">Informationen zum Testen einer Demo finden Sie unter [Beispiel für gebietsschemaabhängigen Code][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="6e820-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="6e820-196">Chrom Problem [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="6e820-196">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="6e820-197">Debuggen von Richtlinien für die übergreifende Einbettungs Richtlinie (COEP)</span><span class="sxs-lookup"><span data-stu-id="6e820-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="6e820-198">Das Netzwerk Panel bietet nun Informationen zu Debuginformationen [über die Ursprungs Einbettungs Richtlinie][COEP] .</span><span class="sxs-lookup"><span data-stu-id="6e820-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="6e820-199">Die Spalte **Status** bietet nun eine kurze Erläuterung dazu, warum eine Anforderung blockiert wurde, sowie einen Link, um die Überschriften dieser Anforderung für weiteres Debuggen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="6e820-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Blockierte Anforderungen in der Spalte \* \* Status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="6e820-201">Abbildung 11: blockierte Anforderungen in der Spalte "Status"</span><span class="sxs-lookup"><span data-stu-id="6e820-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-202">Im Abschnitt " **Antwort Kopfzeilen** " auf der Registerkarte " **Kopfzeilen** " finden Sie weitere Anleitungen zur Behebung der Probleme:</span><span class="sxs-lookup"><span data-stu-id="6e820-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="6e820-204">Abbildung 12: Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"</span><span class="sxs-lookup"><span data-stu-id="6e820-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-205">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-206">Chrom Problem [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="6e820-206">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="6e820-207">Neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints</span><span class="sxs-lookup"><span data-stu-id="6e820-207">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="6e820-208">Das Quellen Panel enthält neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints:</span><span class="sxs-lookup"><span data-stu-id="6e820-208">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="6e820-209">Haltepunkte \ (</span><span class="sxs-lookup"><span data-stu-id="6e820-209">Breakpoints \(</span></span>![Haltepunkt](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="6e820-211">\) werden durch rote Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e820-211">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="6e820-212">Bedingte Haltepunkte \ (</span><span class="sxs-lookup"><span data-stu-id="6e820-212">Conditional Breakpoints \(</span></span>![Bedingter Haltepunkt](../../media/2020/03/conditional.msft.png)<span data-ttu-id="6e820-214">\) werden durch halb rote halb weiße Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e820-214">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="6e820-215">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="6e820-215">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="6e820-217">\) werden durch rote Kreise mit Konsolen Symbolen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e820-217">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="6e820-218">Die Motivation für die neuen Symbole bestand darin, die Benutzeroberfläche mit anderen GUI-Debugging-Tools konsistenter zu gestalten \ (die normalerweise Farb Haltepunkte rot \) und die Unterscheidung zwischen den drei Features auf einen Blick zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="6e820-218">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="6e820-219">Chrom Problem [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="6e820-219">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="6e820-220">Anzeigen von Netzwerkanforderungen, die einen bestimmten Cookie-Pfad festzulegen</span><span class="sxs-lookup"><span data-stu-id="6e820-220">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="6e820-221">Verwenden Sie das `cookie-path` Schlüsselwort New Filter in der Gruppe **Netzwerk** , um sich auf die Netzwerkanforderungen zu konzentrieren, die einen bestimmten [Cookie-Pfad][MDNCookiePath]festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6e820-221">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="6e820-222">Schauen Sie sich [Filter Anforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties] an, um weitere Stichwörter wie zu entdecken `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="6e820-222">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="6e820-223">Andocken von Links über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="6e820-223">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="6e820-224">Öffnen Sie das [Befehl-Menü][DevToolsCommandMenuIndex] , und führen Sie den `Dock to left` Befehl aus, um devtools Links vom Viewport zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6e820-224">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, angedockt Links vom Viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="6e820-226">Abbildung 13: devtools, angedockt Links vom Viewport</span><span class="sxs-lookup"><span data-stu-id="6e820-226">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6e820-227">Das Feature " **Dock to Left** " wurde seit Microsoft Edge 75 zur Verfügung gestellt, war aber zuvor nur über das [**Hauptmenü**][DevtoolsCustomizePlacementsChangeMainMenu]zugänglich.</span><span class="sxs-lookup"><span data-stu-id="6e820-227">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="6e820-228">Das neue Feature in Microsoft Edge 83 ist, dass Sie nun über das Befehlsmenü auf dieses Feature zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6e820-228">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="6e820-229">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-229">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-230">Chrom Problem [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="6e820-230">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="6e820-231">Das Panel "Audits" ist jetzt das Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="6e820-231">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="6e820-232">Das devtools-Team erhielt häufig Feedback von Webentwicklern, dass es zwar möglich war, [Leuchtturm][GithubGoogleChromeLighthouse] von devtools aus zu starten, als Sie es ausprobierten, dass Sie das Panel "Leuchtturm" nicht finden konnten, daher ist das **Audit** Panel nun das **Leuchtturm** -Panel.</span><span class="sxs-lookup"><span data-stu-id="6e820-232">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Das Leuchtturm-Panel" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="6e820-234">Abbildung 14: Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="6e820-234">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6e820-235">Das **Leuchtturm** -Panel bietet Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="6e820-235">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="6e820-236">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und die Daten, die Sie möglicherweise sammeln.</span><span class="sxs-lookup"><span data-stu-id="6e820-236">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="6e820-237">Löschen aller lokalen Außerkraftsetzungen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="6e820-237">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="6e820-238">Nachdem Sie **lokale Überschreibungen** eingerichtet haben, können Sie mit der rechten Maustaste auf einen Ordner klicken und die Option " **alle Überschreibungen löschen** " auswählen, um alle lokalen Überschreibungen in diesem Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6e820-238">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Alle Außerkraftsetzungen löschen" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="6e820-240">Abbildung 15: Löschen aller Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="6e820-240">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-241">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-241">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-242">Chrom Problem [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="6e820-242">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="6e820-243">Benutzeroberfläche für lange Aufgaben aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6e820-243">Updated Long tasks UI</span></span>  

<span data-ttu-id="6e820-244">Eine **lange Aufgabe** ist JavaScript-Code, der den Hauptthread lange Zeit monopolisiert, wodurch eine Webseite blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e820-244">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="6e820-245">Sie haben in der Lage sein, [lange Aufgaben im Leistungs Panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] für eine Weile zu visualisieren, doch in Microsoft Edge 83 wurde die Benutzeroberfläche für die lange Aufgaben Visualisierung im Leistungs Panel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6e820-245">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="6e820-246">Der lange Aufgabenbereich eines Vorgangs wird nun mit einem gestreiften roten Hintergrund eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="6e820-246">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Die neue Benutzeroberfläche für lange Aufgaben" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="6e820-248">Abbildung 16: die neue Benutzeroberfläche für lange Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6e820-248">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="6e820-249">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="6e820-249">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="6e820-250">Chrom Problem [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="6e820-250">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="6e820-251">Unterstützung für Maskierungs Symbole im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="6e820-251">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="6e820-252">Android Oreo hat Adaptive Symbole eingeführt, die APP-Symbole in einer Vielzahl von Formen in verschiedenen Gerätemodellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e820-252">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="6e820-253">**Maskierungs Symbole** sind ein neues Symbol Format, das adaptive Symbole unterstützt, mit denen Sie sicherstellen können, dass Ihr [PWA][PprgressiveWebAppsChromiumIndex] -Symbol auf Geräten gut aussieht, die den Standard für Maskierungs fähige Symbole unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6e820-253">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="6e820-254">Aktivieren Sie das Kontrollkästchen **nur den Mindestbereich für abgesicherten Bereich für maskierte Symbole anzeigen** im Bereich **Manifest** , um zu überprüfen, ob Ihr Maskierungs Symbol auf Android Oreo-Geräten gut aussieht.</span><span class="sxs-lookup"><span data-stu-id="6e820-254">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Kontrollkästchen "nur den kleinsten sicheren Bereich für maskierte Symbole anzeigen"" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="6e820-256">Abbildung 17: Kontrollkästchen **nur den kleinsten sicheren Bereich für Maskierungs Symbole anzeigen**</span><span class="sxs-lookup"><span data-stu-id="6e820-256">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6e820-257">Dieses Feature wurde in Microsoft Edge 81 gestartet.</span><span class="sxs-lookup"><span data-stu-id="6e820-257">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="6e820-258">Die hier in Microsoft Edge 83 behandelten Updates wurden nicht in [Neuerungen in devtools (Microsoft Edge 81)][WhatsNew81]behandelt.</span><span class="sxs-lookup"><span data-stu-id="6e820-258">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="6e820-259">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="6e820-259">Feedback</span></span>  

<span data-ttu-id="6e820-260">So besprechen Sie die neuen Features und Änderungen in diesem Beitrag oder alles, was mit devtools zu tun hat:</span><span class="sxs-lookup"><span data-stu-id="6e820-260">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="6e820-261">Senden Sie Ihr Feedback über das **Feedback** -Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="6e820-261">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="6e820-262">Tweet bei [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="6e820-262">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="6e820-263">Einen Vorschlag an [das gewünschte Web][TheWebWeWant] senden</span><span class="sxs-lookup"><span data-stu-id="6e820-263">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="6e820-264">Datei Fehler in diesem Dokument im [Edge-Entwickler-][GitHubMicrosoftDocsEdgeDeveloperNewIssue] Repository</span><span class="sxs-lookup"><span data-stu-id="6e820-264">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/03/feedback-icon.msft.png" alt-text="Das \* \* Feedback \* \*-Symbol in der Microsoft Edge-devtools" lightbox="../../media/2020/03/feedback-icon.msft.png":::
   <span data-ttu-id="6e820-266">Abbildung 18: das Symbol " **Feedback** " in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="6e820-266">Figure 18:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="6e820-267">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="6e820-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="6e820-268">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e820-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="6e820-269">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6e820-269">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem-MicrosoftDocs/Edge-Developer-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview-Kanäle"  
[TheWebWeWant]: https://webwewant.fyi "Das gewünschte Web"  

[WhatsNew81]: ../01/devtools.md "Neuerungen in devtools (Microsoft Edge 81) | Microsoft docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl | Microsoft docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Ändern der Platzierung aus dem Hauptmenü | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Hauptthread Aktivität anzeigen | Microsoft docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendering" | Microsoft docs"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit dem Remote Debuggen von Windows 10-Geräten | Microsoft docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Code Haltepunkte – Anleitung zum Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools | Microsoft docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Übersicht über das Windows-Geräte Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Remote Tools für Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Update für stabile Kanal Versionen für Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Arten der Farbenblindheit"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Akzeptieren – Sprache"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Beispiel für gebietsschemaabhängigen Code"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Problem 963183: devtools sind nicht WCAG-kompatibel"  
[CR1003700]: https://crbug.com/1003700 "Problem 1003700: Hinzufügen von devtools-Unterstützung für farbsehstörungen-Fehlersimulation"  
[CR1011679]: https://crbug.com/1011679 "Problem 1011679: Einführung von "Dock to Left" über das Befehlsmenü"  
[CR1016501]: https://crbug.com/1016501 "Problem 1016501: Feature Request: Schaltfläche zum Löschen aller lokalen Außerkraftsetzungen"  
[CR1050999]: https://crbug.com/1050999 "Problem 1050999: Registerkarte "Eigenschaften""  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: unterstützen des Coop/COEP-Debuggens in devtools"  
[CR1054447]: https://crbug.com/1054447 "Problem 1054447: Aktualisieren von Leistungs Metriken in der devtools-Zeitachse"  
[CR1051822]: https://crbug.com/1051822 "Problem 1051822: devtools: Hinzufügen einer Benutzeroberfläche zum Emulieren des Gebietsschemas"
[CR1041830]: https://crbug.com/1041830 "Problem 1041830: verbessern der Farben für Haltepunkte"
[CR1050855]: https://crbug.com/1050855 "Problem 1050855: die Ansicht "Einstellungen" ist schwer zu erkennen"
[CR1056348]: https://crbug.com/1056348 "Problem 1056348: Infoleiste-Komponentenaktualisierung"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Erläuterte Coop-und COEP-Cross-Origin-Opener-Richtlinie"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Erläuterte Coop-und COEP-Richtlinien für die Ursprungs Einbettung"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse GitHub Repo"  

> [!NOTE]
> <span data-ttu-id="6e820-310">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e820-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6e820-311">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/03/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6e820-311">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6e820-313">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6e820-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
