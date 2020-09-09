---
description: Emulieren Sie farbsehstörungen, docken Sie Links im Befehlsmenü an, und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8ce8979a7128217b72aee42c05a0048b511f9cae
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004328"
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

# <span data-ttu-id="184df-104">Neuerungen in devtools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="184df-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="184df-105">Nach dem aktualisierten Chrom-Terminplan passen wir unseren Zeitplan für bevorstehende Microsoft Edge-Versionen an und kündigen die Microsoft Edge 82-Version.</span><span class="sxs-lookup"><span data-stu-id="184df-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="184df-106">Schauen Sie sich unseren [Blogbeitrag][WindowsBlogStableRelease] an, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="184df-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="184df-107">Hier sind die neuen Features, die im devtools in Microsoft Edge 83 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="184df-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="184df-108">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="184df-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="184df-109">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="184df-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="184df-110">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="184df-110">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="184df-111">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="184df-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="184df-112">Remotedebuggen von Microsoft Edge auf Windows 10-Geräten</span><span class="sxs-lookup"><span data-stu-id="184df-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="184df-113">Die [Remote Tools für Microsoft Edge \ (Beta \)-][RemoteTools] APP ist jetzt im [Microsoft Store][MicrosoftStore]verfügbar.</span><span class="sxs-lookup"><span data-stu-id="184df-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="184df-114">Mit dieser APP, die das [Windows-Geräte Portal][WindowsUwpDebugTestPerfDevicePortal]erweitert, können Sie eine Verbindung von der Instanz von Microsoft Edge, die auf Ihrem Entwicklungscomputer ausgeführt wird, mit einem Windows 10-Remotegerät herstellen, eine Liste der Ziele anzeigen (alle Registerkarten in Microsoft Edge und [PWAs][PprgressiveWebAppsChromiumIndex] werden auf dem Windows 10-Gerät geöffnet), und die devtools auf dem Entwicklungscomputer für ein Ziel verwenden, das auf dem Remote</span><span class="sxs-lookup"><span data-stu-id="184df-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Die im Microsoft Store verfügbare Remote Tools für Microsoft Edge (Beta)-app" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="184df-116">Abbildung 1: die APP [Remote Tools für Microsoft Edge (Beta)][RemoteTools] , die im [Microsoft Store][MicrosoftStore] verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="184df-116">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="184df-117">[Lesen Sie unseren Leitfaden zum Einrichten Ihres Windows 10-Geräts und ihres Entwicklungscomputers für das Remotedebuggen][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="184df-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="184df-118">Informieren Sie uns über Ihre Remote Debugging-Erfahrung, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) klicken.</span><span class="sxs-lookup"><span data-stu-id="184df-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="184df-119">Neue Möglichkeiten für den Zugriff auf Einstellungen</span><span class="sxs-lookup"><span data-stu-id="184df-119">New ways to access Settings</span></span>  

<span data-ttu-id="184df-120">Es gibt Unmengen von Einstellungen für die devtools, die Sie anpassen können, um die devtools aussehen zu lassen, zu fühlen und zu arbeiten, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="184df-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="184df-121">In Microsoft Edge 83 ist der Zugriff auf die [Einstellungen][DevtoolsCustomizeIndexSettings] im devtools jetzt viel einfacher.</span><span class="sxs-lookup"><span data-stu-id="184df-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="184df-122">Öffnen Sie die Einstellungen mit dem Zahnradsymbol neben "Console Alerts" und dem Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="184df-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Das Zahnradsymbol öffnet die Einstellungen im devtools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="184df-124">Abbildung 2: das Zahnradsymbol öffnet die **Einstellungen** im devtools</span><span class="sxs-lookup"><span data-stu-id="184df-124">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="184df-125">Sie können die [Einstellungen][DevtoolsCustomizeIndexSettings] auch über das Hauptmenü unter **"** **Weitere Tools**" öffnen.</span><span class="sxs-lookup"><span data-stu-id="184df-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Hauptmenü > weitere Tools > Einstellungen" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="184df-127">Abbildung 3: **Hauptmenü**  >  **Weitere**  >  **Einstellungen** für Tools</span><span class="sxs-lookup"><span data-stu-id="184df-127">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="184df-128">Chrom Problem [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="184df-128">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="184df-129">Neue und verbesserte infobars</span><span class="sxs-lookup"><span data-stu-id="184df-129">New and improved infobars</span></span>

<span data-ttu-id="184df-130">Informations Benachrichtigungs leisten \ (Infoleisten \) in devtools haben nun ein verbessertes Aussehen und mehr Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="184df-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="184df-131">In Microsoft Edge 83 können infobars leichter gelesen und Schaltflächen bereitgestellt werden, damit Sie die relevante Aktion sofort durchführen können.</span><span class="sxs-lookup"><span data-stu-id="184df-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="184df-133">Abbildung 4: Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge, Version 83</span><span class="sxs-lookup"><span data-stu-id="184df-133">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="184df-134">Chrom Problem [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="184df-134">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="184df-135">Navigieren in der Farbauswahl mit der Tastatur</span><span class="sxs-lookup"><span data-stu-id="184df-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="184df-136">Bei der [Farbauswahl][DevtoolsCssReferenceColorPicker] handelt es sich um eine Benutzeroberfläche für Änderungen und Deklarationen im [Element Panel][DevtoolsCssIndex] `color` `background-color` .</span><span class="sxs-lookup"><span data-stu-id="184df-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="184df-137">In früheren Versionen von Microsoft Edge konnten Sie nicht über die Tastatur in der [Farbauswahl][DevtoolsCssReferenceColorPicker] im Bereich " **Schattierungen** " navigieren.</span><span class="sxs-lookup"><span data-stu-id="184df-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Sie können jetzt Ihre Tastatur verwenden, um die Auswahl im Bereich "Schattierungen" der Farbauswahl zu verschieben." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="184df-139">Abbildung 5: Sie können nun Ihre Tastatur verwenden, um die Auswahl im Bereich " **Schattierungen** " der [Farbauswahl][DevtoolsCssReferenceColorPicker] zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="184df-139">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="184df-140">In Microsoft Edge 83 können Sie nun die Tastatur verwenden, um den Auswahlbereich im Abschnitt **Schattierungen** der Farbauswahl zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="184df-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="184df-141">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="184df-141">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="184df-142">Die Registerkarte "Eigenschaften" wird nun nach einer Seitenaktualisierung gefüllt</span><span class="sxs-lookup"><span data-stu-id="184df-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="184df-143">In Microsoft Edge 81 und früheren Versionen wurde die **Registerkarte Eigenschaften** im [Element Panel][DevtoolsCssIndex] durch Seitenaktualisierungen unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="184df-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="184df-144">Wenn Sie die Seite aktualisiert haben, wurden die Eigenschaften des aktuell ausgewählten Elements auf der **Registerkarte Eigenschaften** nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="184df-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="In Microsoft Edge 81 und früher war die Registerkarte "Eigenschaften" nach einer Seitenaktualisierung leer" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="184df-146">Abbildung 6: in Microsoft Edge 81 und früher war die **Registerkarte "Eigenschaften"** nach einer Seitenaktualisierung leer</span><span class="sxs-lookup"><span data-stu-id="184df-146">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="184df-147">In Microsoft Edge 83 können Sie nun die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung auf der **Registerkarte Eigenschaften**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="184df-147">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="In Microsoft Edge 83 werden auf der Registerkarte "Eigenschaften" die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="184df-149">Abbildung 7: in Microsoft Edge 83 werden auf der **Registerkarte "Eigenschaften"** die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="184df-149">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="184df-150">Chrom Problem [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="184df-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="184df-151">Verwenden Sie die Pfeiltasten, um im Tool "Änderungen" zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="184df-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="184df-152">Das **Tool "Änderungen"** verfolgt alle Änderungen, die Sie an CSS oder JavaScript im devtools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="184df-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="184df-153">Sie können das **Tool "Änderungen"** verwenden, um schnell alle Ihre Änderungen anzuzeigen und diese wieder in Ihren Editor/Ihre IDE zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="184df-153">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="184df-154">Öffnen Sie das **Tool "Änderungen** ", indem `Ctrl` + `Shift` + `P` Sie auf die devtools drücken, um das [Befehlsmenü][DevToolsCommandMenuIndex] zu öffnen und einzugeben `changes` .</span><span class="sxs-lookup"><span data-stu-id="184df-154">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="184df-155">Wählen Sie den Befehl **Änderungen anzeigen** aus, und führen Sie ihn aus, um das **Tool Änderungen** im devtools-Einzug zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="184df-155">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="184df-156">Wenn Sie eine Änderung an einer minimierte-Datei vorgenommen haben, können Sie mit dem **Tool "Änderungen"** horizontal scrollen, um den gesamten minimierte-Code anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="184df-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="184df-157">Ab Microsoft Edge 83 können Sie jetzt mit den Pfeiltasten auf der Tastatur horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="184df-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="In Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um Ihren minimierte-Code im Tool "Änderungen" anzuzeigen." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="184df-159">Abbildung 8: in Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um die am minimierte-Code vorgenommenen Änderungen im **Tool "Änderungen"** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="184df-159">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="184df-160">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie uns Ihr Feedback, indem Sie uns [tweeten][PostTweetEdgeDevTools] oder auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) klicken.</span><span class="sxs-lookup"><span data-stu-id="184df-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-161">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="184df-161">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="184df-162">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="184df-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="184df-163">In den folgenden Abschnitten werden weitere in Microsoft Edge 83 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="184df-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="184df-164">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="184df-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="184df-165">Öffnen Sie die [Registerkarte "Rendering"][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] , und verwenden Sie das neue Feature "nach **eifern des Sehvermögens** ", um eine bessere Vorstellung davon zu erhalten, wie Personen mit unterschiedlichen Arten von Sehstörungen Ihre Website erleben.</span><span class="sxs-lookup"><span data-stu-id="184df-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulieren verschwommener Sehkraft" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="184df-167">Abbildung 9: emulieren verschwommener Visionen</span><span class="sxs-lookup"><span data-stu-id="184df-167">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="184df-168">DevTools ist in der Lage, unscharfe Sehkraft und die folgenden [Arten von farbsehstörungen][ColorBlindnessTypes]zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="184df-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="184df-169">Farbsehstörungen</span><span class="sxs-lookup"><span data-stu-id="184df-169">Color Vision Deficiency</span></span> | <span data-ttu-id="184df-170">Details</span><span class="sxs-lookup"><span data-stu-id="184df-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="184df-171">Protanopie</span><span class="sxs-lookup"><span data-stu-id="184df-171">Protanopia</span></span> | <span data-ttu-id="184df-172">Die Unfähigkeit, jedes rote Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="184df-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="184df-173">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="184df-173">Deuteranopia</span></span> | <span data-ttu-id="184df-174">Die Unfähigkeit, grünes Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="184df-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="184df-175">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="184df-175">Tritanopia</span></span> | <span data-ttu-id="184df-176">Die Unfähigkeit, ein blaues Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="184df-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="184df-177">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="184df-177">Achromatopsia</span></span> | <span data-ttu-id="184df-178">Die Unfähigkeit, eine beliebige Farbe wahrzunehmen, mit Ausnahme von Grautönen \ (extrem selten \).</span><span class="sxs-lookup"><span data-stu-id="184df-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="184df-179">Es gibt weniger Extreme Versionen dieser farbsehstörungen, und tatsächlich sind Sie häufiger.</span><span class="sxs-lookup"><span data-stu-id="184df-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="184df-180">Bei Protanomalie handelt es sich beispielsweise um eine reduzierte Empfindlichkeit für rotes Licht (im Gegensatz zu Protanopie, was die vollständige Unfähigkeit, rotes Licht wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="184df-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="184df-181">Allerdings sind diese omaly Sehstörungen nicht so klar definiert: jede Person mit einem solchen Sehstörungen ist anders und kann die Dinge anders sehen (in der Lage sein, mehr/weniger der relevanten Farben wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="184df-181">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="184df-182">Wenn Sie für die extremeren Simulationen in devtools entwerfen, sind Ihre Web-Apps garantiert auch für Personen mit Protanomalie, Deuteranomalie, Tritanomaly und achromatomaly zugänglich.</span><span class="sxs-lookup"><span data-stu-id="184df-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="184df-183">Senden Sie Ihr Feedback per [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="184df-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-184">Chrom Problem [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="184df-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="184df-185">Emulieren von Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="184df-185">Emulate locales</span></span>  

<span data-ttu-id="184df-186">Emulieren Sie Gebietsschemas, indem Sie einen Speicherort im **Sensor**  >  **Standort**festlegen.</span><span class="sxs-lookup"><span data-stu-id="184df-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="184df-187">[Öffnen Sie das **Menübefehl** ][DevToolsCommandMenuIndex] , und geben Sie den Namen `Sensors` ein, um auf den Reiter **Sensoren** zuzugreifen.  Nach dem Ausführen dieser Aktionen ändert devtools das aktuelle Standardgebietsschema, was sich auf den folgenden Code auswirkt.</span><span class="sxs-lookup"><span data-stu-id="184df-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="184df-188">APIs, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="184df-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="184df-189">Andere JavaScript-APIs für Gebietsschema, beispielsweise `String.prototype.localeCompare` und `*.prototype.toLocaleString` , beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="184df-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="184df-190">DOM-APIs wie `navigator.language` und</span><span class="sxs-lookup"><span data-stu-id="184df-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="184df-191">Der [`Accept-Language`][MDNAcceptLanguage] HTTP-Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="184df-191">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="184df-192">Updates für `navigator.language` und `navigator.languages` werden nicht sofort, sondern nur nach der nächsten Navigation oder Seitenaktualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="184df-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="184df-193">Änderungen am `Accept-Language` http-Header werden nur für nachfolgende Anforderungen wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="184df-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulieren eines Gebietsschemas" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="184df-195">Abbildung 10: Emulieren eines Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="184df-195">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="184df-196">Informationen zum Testen einer Demo finden Sie unter [Beispiel für gebietsschemaabhängigen Code][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="184df-196">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="184df-197">Chrom Problem [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="184df-197">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="184df-198">Debuggen von Richtlinien für die übergreifende Einbettungs Richtlinie (COEP)</span><span class="sxs-lookup"><span data-stu-id="184df-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="184df-199">Das Netzwerk Panel bietet nun Informationen zu Debuginformationen [über die Ursprungs Einbettungs Richtlinie][COEP] .</span><span class="sxs-lookup"><span data-stu-id="184df-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="184df-200">Die Spalte **Status** bietet nun eine kurze Erläuterung dazu, warum eine Anforderung blockiert wurde, sowie einen Link, um die Überschriften dieser Anforderung für weiteres Debuggen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="184df-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Blockierte Anforderungen in der Spalte \* \* Status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="184df-202">Abbildung 11: blockierte Anforderungen in der Spalte "Status"</span><span class="sxs-lookup"><span data-stu-id="184df-202">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="184df-203">Im Abschnitt " **Antwort Kopfzeilen** " auf der Registerkarte " **Kopfzeilen** " finden Sie weitere Anleitungen zur Behebung der Probleme:</span><span class="sxs-lookup"><span data-stu-id="184df-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="184df-205">Abbildung 12: Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"</span><span class="sxs-lookup"><span data-stu-id="184df-205">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="184df-206">Senden Sie Ihr Feedback per [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="184df-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-207">Chrom Problem [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="184df-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="184df-208">Neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints</span><span class="sxs-lookup"><span data-stu-id="184df-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="184df-209">Das Quellen Panel enthält neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints:</span><span class="sxs-lookup"><span data-stu-id="184df-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="184df-210">Haltepunkte \ (</span><span class="sxs-lookup"><span data-stu-id="184df-210">Breakpoints \(</span></span>![Haltepunkt](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="184df-212">\) werden durch rote Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="184df-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="184df-213">Bedingte Haltepunkte \ (</span><span class="sxs-lookup"><span data-stu-id="184df-213">Conditional Breakpoints \(</span></span>![Bedingter Haltepunkt](../../media/2020/03/conditional.msft.png)<span data-ttu-id="184df-215">\) werden durch halb rote halb weiße Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="184df-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="184df-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="184df-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="184df-218">\) werden durch rote Kreise mit Konsolen Symbolen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="184df-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="184df-219">Die Motivation für die neuen Symbole bestand darin, die Benutzeroberfläche mit anderen GUI-Debugging-Tools konsistenter zu gestalten \ (die normalerweise Farb Haltepunkte rot \) und die Unterscheidung zwischen den drei Features auf einen Blick zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="184df-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="184df-220">Chrom Problem [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="184df-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="184df-221">Anzeigen von Netzwerkanforderungen, die einen bestimmten Cookie-Pfad festzulegen</span><span class="sxs-lookup"><span data-stu-id="184df-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="184df-222">Verwenden Sie das `cookie-path` Schlüsselwort New Filter in der Gruppe **Netzwerk** , um sich auf die Netzwerkanforderungen zu konzentrieren, die einen bestimmten [Cookie-Pfad][MDNCookiePath]festzulegen.</span><span class="sxs-lookup"><span data-stu-id="184df-222">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="184df-223">Schauen Sie sich [Filter Anforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties] an, um weitere Stichwörter wie zu entdecken `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="184df-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="184df-224">Andocken von Links über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="184df-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="184df-225">Öffnen Sie das [Befehl-Menü][DevToolsCommandMenuIndex] , und führen Sie den `Dock to left` Befehl aus, um devtools Links vom Viewport zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="184df-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, angedockt Links vom Viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="184df-227">Abbildung 13: devtools, angedockt Links vom Viewport</span><span class="sxs-lookup"><span data-stu-id="184df-227">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="184df-228">Das Feature " **Dock to Left** " wurde seit Microsoft Edge 75 zur Verfügung gestellt, war aber zuvor nur über das [**Hauptmenü**][DevtoolsCustomizePlacementsChangeMainMenu]zugänglich.</span><span class="sxs-lookup"><span data-stu-id="184df-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="184df-229">Das neue Feature in Microsoft Edge 83 ist, dass Sie nun über das Befehlsmenü auf dieses Feature zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="184df-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="184df-230">Senden Sie Ihr Feedback per [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="184df-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-231">Chrom Problem [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="184df-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="184df-232">Das Panel "Audits" ist jetzt das Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="184df-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="184df-233">Das devtools-Team erhielt häufig Feedback von Webentwicklern, dass es zwar möglich war, [Leuchtturm][GithubGoogleChromeLighthouse] von devtools aus zu starten, als Sie es ausprobierten, dass Sie das Panel "Leuchtturm" nicht finden konnten, daher ist das **Audit** Panel nun das **Leuchtturm** -Panel.</span><span class="sxs-lookup"><span data-stu-id="184df-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Das Leuchtturm-Panel" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="184df-235">Abbildung 14: Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="184df-235">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="184df-236">Das **Leuchtturm** -Panel bietet Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="184df-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="184df-237">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und die Daten, die Sie möglicherweise sammeln.</span><span class="sxs-lookup"><span data-stu-id="184df-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="184df-238">Löschen aller lokalen Außerkraftsetzungen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="184df-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="184df-239">Nachdem Sie **lokale Überschreibungen** eingerichtet haben, können Sie mit der rechten Maustaste auf einen Ordner klicken und die Option " **alle Überschreibungen löschen** " auswählen, um alle lokalen Überschreibungen in diesem Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="184df-239">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Alle Außerkraftsetzungen löschen" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="184df-241">Abbildung 15: Löschen aller Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="184df-241">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="184df-242">Senden Sie Ihr Feedback per [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="184df-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-243">Chrom Problem [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="184df-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="184df-244">Benutzeroberfläche für lange Aufgaben aktualisiert</span><span class="sxs-lookup"><span data-stu-id="184df-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="184df-245">Eine **lange Aufgabe** ist JavaScript-Code, der den Hauptthread lange Zeit monopolisiert, wodurch eine Webseite blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="184df-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="184df-246">Sie haben in der Lage sein, [lange Aufgaben im Leistungs Panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] für eine Weile zu visualisieren, doch in Microsoft Edge 83 wurde die Benutzeroberfläche für die lange Aufgaben Visualisierung im Leistungs Panel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="184df-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="184df-247">Der lange Aufgabenbereich eines Vorgangs wird nun mit einem gestreiften roten Hintergrund eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="184df-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Die neue Benutzeroberfläche für lange Aufgaben" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="184df-249">Abbildung 16: die neue Benutzeroberfläche für lange Aufgaben</span><span class="sxs-lookup"><span data-stu-id="184df-249">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="184df-250">Senden Sie Ihr Feedback per [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="184df-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="184df-251">Chrom Problem [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="184df-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="184df-252">Unterstützung für Maskierungs Symbole im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="184df-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="184df-253">Android Oreo hat Adaptive Symbole eingeführt, die APP-Symbole in einer Vielzahl von Formen in verschiedenen Gerätemodellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="184df-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="184df-254">**Maskierungs Symbole** sind ein neues Symbol Format, das adaptive Symbole unterstützt, mit denen Sie sicherstellen können, dass Ihr [PWA][PprgressiveWebAppsChromiumIndex] -Symbol auf Geräten gut aussieht, die den Standard für Maskierungs fähige Symbole unterstützen.</span><span class="sxs-lookup"><span data-stu-id="184df-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="184df-255">Aktivieren Sie das Kontrollkästchen **nur den Mindestbereich für abgesicherten Bereich für maskierte Symbole anzeigen** im Bereich **Manifest** , um zu überprüfen, ob Ihr Maskierungs Symbol auf Android Oreo-Geräten gut aussieht.</span><span class="sxs-lookup"><span data-stu-id="184df-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Kontrollkästchen "nur den kleinsten sicheren Bereich für maskierte Symbole anzeigen"" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="184df-257">Abbildung 17: Kontrollkästchen **nur den kleinsten sicheren Bereich für Maskierungs Symbole anzeigen**</span><span class="sxs-lookup"><span data-stu-id="184df-257">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="184df-258">Dieses Feature wurde in Microsoft Edge 81 gestartet.</span><span class="sxs-lookup"><span data-stu-id="184df-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="184df-259">Die hier in Microsoft Edge 83 behandelten Updates wurden nicht in [Neuerungen in devtools (Microsoft Edge 81)][WhatsNew81]behandelt.</span><span class="sxs-lookup"><span data-stu-id="184df-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="184df-260">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="184df-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="184df-261">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="184df-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="184df-262">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="184df-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="184df-263">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="184df-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

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
> <span data-ttu-id="184df-304">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184df-304">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="184df-305">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/03/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="184df-305">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="184df-307">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="184df-307">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
