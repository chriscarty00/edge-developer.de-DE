---
title: Neuerungen in devtools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7651430c581346d1f140f0a5974b8aa9bb809204
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "10709024"
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

# <span data-ttu-id="3ae0e-103">Neuerungen in devtools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="3ae0e-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="3ae0e-104">Nach dem aktualisierten Chrom-Terminplan passen wir unseren Zeitplan für bevorstehende Microsoft Edge-Versionen an und kündigen die Microsoft Edge 82-Version.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="3ae0e-105">Schauen Sie sich unseren [Blogbeitrag][WindowsBlogStableRelease] an, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="3ae0e-106">Hier sind die neuen Features, die im devtools in Microsoft Edge 83 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="3ae0e-107">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="3ae0e-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="3ae0e-108">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="3ae0e-109">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="3ae0e-110">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="3ae0e-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="3ae0e-111">Remotedebuggen von Microsoft Edge auf Windows 10-Geräten</span><span class="sxs-lookup"><span data-stu-id="3ae0e-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="3ae0e-112">Die [Remote Tools für Microsoft Edge \ (Beta \)-][RemoteTools] APP ist jetzt im [Microsoft Store][MicrosoftStore]verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="3ae0e-113">Mit dieser APP, die das [Windows-Geräte Portal][WindowsDevicePortal]erweitert, können Sie eine Verbindung von der Instanz von Microsoft Edge, die auf Ihrem Entwicklungscomputer ausgeführt wird, mit einem Windows 10-Remotegerät herstellen, eine Liste der Ziele anzeigen (alle Registerkarten in Microsoft Edge und [PWAs][PWADoc] werden auf dem Windows 10-Gerät geöffnet), und die devtools auf dem Entwicklungscomputer für ein Ziel verwenden, das auf dem Remote</span><span class="sxs-lookup"><span data-stu-id="3ae0e-113">Using this app, which extends the [Windows Device Portal][WindowsDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PWADoc] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Die im Microsoft Store verfügbare Remote Tools für Microsoft Edge (Beta)-app" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="3ae0e-115">Abbildung 1: die APP [Remote Tools für Microsoft Edge (Beta)][RemoteTools] , die im [Microsoft Store][MicrosoftStore] verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="3ae0e-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-116">[Lesen Sie unseren Leitfaden zum Einrichten Ihres Windows 10-Geräts und ihres Entwicklungscomputers für das Remotedebuggen][RemoteDebuggingWin10].</span><span class="sxs-lookup"><span data-stu-id="3ae0e-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][RemoteDebuggingWin10].</span></span>  <span data-ttu-id="3ae0e-117">Informieren Sie uns über Ihre Remote Debugging-Erfahrung, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="3ae0e-118">Neue Möglichkeiten für den Zugriff auf Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-118">New ways to access Settings</span></span>  

<span data-ttu-id="3ae0e-119">Es gibt Unmengen von Einstellungen für die devtools, die Sie anpassen können, um die devtools aussehen zu lassen, zu fühlen und zu arbeiten, wie Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="3ae0e-120">In Microsoft Edge 83 ist der Zugriff auf die [Einstellungen][OverviewSettings] im devtools jetzt viel einfacher.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-120">In Microsoft Edge 83, accessing [Settings][OverviewSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="3ae0e-121">Öffnen Sie die Einstellungen mit dem Zahnradsymbol neben "Console Alerts" und dem Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Das Zahnradsymbol öffnet die Einstellungen im devtools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="3ae0e-123">Abbildung 2: das Zahnradsymbol öffnet die **Einstellungen** im devtools</span><span class="sxs-lookup"><span data-stu-id="3ae0e-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-124">Sie können die [Einstellungen][OverviewSettings] auch über das Hauptmenü unter **"** **Weitere Tools**" öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-124">You are also able to open [Settings][OverviewSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Hauptmenü > weitere Tools > Einstellungen" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="3ae0e-126">Abbildung 3: **Hauptmenü**  >  **Weitere**  >  **Einstellungen** für Tools</span><span class="sxs-lookup"><span data-stu-id="3ae0e-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-127">Chrom Problem [#1050855][crbug1050855]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-127">Chromium issue [#1050855][crbug1050855]</span></span>

### <span data-ttu-id="3ae0e-128">Neue und verbesserte infobars</span><span class="sxs-lookup"><span data-stu-id="3ae0e-128">New and improved infobars</span></span>

<span data-ttu-id="3ae0e-129">Informations Benachrichtigungs leisten \ (Infoleisten \) in devtools haben nun ein verbessertes Aussehen und mehr Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="3ae0e-130">In Microsoft Edge 83 können infobars leichter gelesen und Schaltflächen bereitgestellt werden, damit Sie die relevante Aktion sofort durchführen können.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="3ae0e-132">Abbildung 4: Infoleiste für das schöne Drucken einer minimierte-Datei in Microsoft Edge, Version 83</span><span class="sxs-lookup"><span data-stu-id="3ae0e-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-133">Chrom Problem [#1056348][crbug1056348]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-133">Chromium issue [#1056348][crbug1056348]</span></span>

### <span data-ttu-id="3ae0e-134">Navigieren in der Farbauswahl mit der Tastatur</span><span class="sxs-lookup"><span data-stu-id="3ae0e-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="3ae0e-135">Bei der [Farbauswahl][ColorPicker] handelt es sich um eine Benutzeroberfläche für Änderungen und Deklarationen im [Element Panel][ElementsDoc] `color` `background-color` .</span><span class="sxs-lookup"><span data-stu-id="3ae0e-135">The [Color Picker][ColorPicker] is a GUI in the [Elements panel][ElementsDoc] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="3ae0e-136">In früheren Versionen von Microsoft Edge konnten Sie nicht über die Tastatur in der [Farbauswahl][ColorPicker] im Bereich " **Schattierungen** " navigieren.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][ColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Sie können jetzt Ihre Tastatur verwenden, um die Auswahl im Bereich "Schattierungen" der Farbauswahl zu verschieben." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="3ae0e-138">Abbildung 5: Sie können nun Ihre Tastatur verwenden, um die Auswahl im Bereich " **Schattierungen** " der [Farbauswahl][ColorPicker] zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][ColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-139">In Microsoft Edge 83 können Sie nun die Tastatur verwenden, um den Auswahlbereich im Abschnitt **Schattierungen** der Farbauswahl zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="3ae0e-140">Chrom Problem [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-140">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="3ae0e-141">Die Registerkarte "Eigenschaften" wird nun nach einer Seitenaktualisierung gefüllt</span><span class="sxs-lookup"><span data-stu-id="3ae0e-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="3ae0e-142">In Microsoft Edge 81 und früheren Versionen wurde die **Registerkarte Eigenschaften** im [Element Panel][ElementsDoc] durch Seitenaktualisierungen unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][ElementsDoc] was broken by page refreshes.</span></span>  <span data-ttu-id="3ae0e-143">Wenn Sie die Seite aktualisiert haben, wurden die Eigenschaften des aktuell ausgewählten Elements auf der **Registerkarte Eigenschaften** nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="In Microsoft Edge 81 und früher war die Registerkarte "Eigenschaften" nach einer Seitenaktualisierung leer" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="3ae0e-145">Abbildung 6: in Microsoft Edge 81 und früher war die **Registerkarte "Eigenschaften"** nach einer Seitenaktualisierung leer</span><span class="sxs-lookup"><span data-stu-id="3ae0e-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-146">In Microsoft Edge 83 können Sie nun die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung auf der **Registerkarte Eigenschaften**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="In Microsoft Edge 83 werden auf der Registerkarte "Eigenschaften" die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="3ae0e-148">Abbildung 7: in Microsoft Edge 83 werden auf der **Registerkarte "Eigenschaften"** die Eigenschaften des aktuell ausgewählten Elements nach einer Seitenaktualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-149">Chrom Problem [#1050999][crbug1050999]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-149">Chromium issue [#1050999][crbug1050999]</span></span>  

### <span data-ttu-id="3ae0e-150">Verwenden Sie die Pfeiltasten, um im Tool "Änderungen" zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="3ae0e-151">Das **Tool "Änderungen"** verfolgt alle Änderungen, die Sie an CSS oder JavaScript im devtools vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="3ae0e-152">Sie können das **Tool "Änderungen"** verwenden, um schnell alle Ihre Änderungen anzuzeigen und diese wieder in Ihren Editor/Ihre IDE zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="3ae0e-153">Öffnen Sie das **Tool "Änderungen** ", indem `Ctrl` + `Shift` + `P` Sie auf die devtools drücken, um das [Befehlsmenü][DevToolsCommandMenuIndex] zu öffnen und einzugeben `changes` .</span><span class="sxs-lookup"><span data-stu-id="3ae0e-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="3ae0e-154">Wählen Sie den Befehl **Änderungen anzeigen** aus, und führen Sie ihn aus, um das **Tool Änderungen** im devtools-Einzug zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="3ae0e-155">Wenn Sie eine Änderung an einer minimierte-Datei vorgenommen haben, können Sie mit dem **Tool "Änderungen"** horizontal scrollen, um den gesamten minimierte-Code anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="3ae0e-156">Ab Microsoft Edge 83 können Sie jetzt mit den Pfeiltasten auf der Tastatur horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="In Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um Ihren minimierte-Code im Tool "Änderungen" anzuzeigen." lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="3ae0e-158">Abbildung 8: in Microsoft Edge 83 können Sie mit den Pfeiltasten horizontal scrollen, um die am minimierte-Code vorgenommenen Änderungen im **Tool "Änderungen"** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-159">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie uns Ihr Feedback, indem Sie uns [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-160">Chrom Problem [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-160">Chromium issue [#963183][crbug963183]</span></span>  

## <span data-ttu-id="3ae0e-161">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="3ae0e-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="3ae0e-162">In den folgenden Abschnitten werden weitere in Microsoft Edge 83 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="3ae0e-163">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="3ae0e-164">Öffnen Sie die [Registerkarte "Rendering"][RenderingDoc] , und verwenden Sie das neue Feature "nach **eifern des Sehvermögens** ", um eine bessere Vorstellung davon zu erhalten, wie Personen mit unterschiedlichen Arten von Sehstörungen Ihre Website erleben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-164">Open the [Rendering tab][RenderingDoc] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulieren verschwommener Sehkraft" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="3ae0e-166">Abbildung 9: emulieren verschwommener Visionen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-167">DevTools ist in der Lage, unscharfe Sehkraft und die folgenden [Arten von farbsehstörungen][ColorBlindnessTypes]zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="3ae0e-168">Farbsehstörungen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-168">Color Vision Deficiency</span></span> | <span data-ttu-id="3ae0e-169">Details</span><span class="sxs-lookup"><span data-stu-id="3ae0e-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="3ae0e-170">Protanopie</span><span class="sxs-lookup"><span data-stu-id="3ae0e-170">Protanopia</span></span> | <span data-ttu-id="3ae0e-171">Die Unfähigkeit, jedes rote Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="3ae0e-172">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="3ae0e-172">Deuteranopia</span></span> | <span data-ttu-id="3ae0e-173">Die Unfähigkeit, grünes Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="3ae0e-174">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="3ae0e-174">Tritanopia</span></span> | <span data-ttu-id="3ae0e-175">Die Unfähigkeit, ein blaues Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="3ae0e-176">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="3ae0e-176">Achromatopsia</span></span> | <span data-ttu-id="3ae0e-177">Die Unfähigkeit, eine beliebige Farbe wahrzunehmen, mit Ausnahme von Grautönen \ (extrem selten \).</span><span class="sxs-lookup"><span data-stu-id="3ae0e-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="3ae0e-178">Es gibt weniger Extreme Versionen dieser farbsehstörungen, und tatsächlich sind Sie häufiger.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="3ae0e-179">Bei Protanomalie handelt es sich beispielsweise um eine reduzierte Empfindlichkeit für rotes Licht (im Gegensatz zu Protanopie, was die vollständige Unfähigkeit, rotes Licht wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="3ae0e-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="3ae0e-180">Allerdings sind diese omaly Sehstörungen nicht so klar definiert: jede Person mit einem solchen Sehstörungen ist anders und kann die Dinge anders sehen (in der Lage sein, mehr/weniger der relevanten Farben wahrzunehmen).</span><span class="sxs-lookup"><span data-stu-id="3ae0e-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="3ae0e-181">Wenn Sie für die extremeren Simulationen in devtools entwerfen, sind Ihre Web-Apps garantiert auch für Personen mit Protanomalie, Deuteranomalie, Tritanomaly und achromatomaly zugänglich.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="3ae0e-182">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-183">Chrom Problem [#1003700][crbug1003700]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-183">Chromium issue [#1003700][crbug1003700]</span></span>  

### <span data-ttu-id="3ae0e-184">Emulieren von Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="3ae0e-184">Emulate locales</span></span>  

<span data-ttu-id="3ae0e-185">Emulieren Sie Gebietsschemas, indem Sie einen Speicherort im **Sensor**  >  **Standort**festlegen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="3ae0e-186">[Öffnen Sie das **Menübefehl** ][DevToolsCommandMenuIndex] , und geben Sie den Namen `Sensors` ein, um auf den Reiter **Sensoren** zuzugreifen.  Nach dem Ausführen dieser Aktionen ändert devtools das aktuelle Standardgebietsschema, was sich auf den folgenden Code auswirkt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="3ae0e-187">APIs, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="3ae0e-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="3ae0e-188">Andere JavaScript-APIs für Gebietsschema, beispielsweise `String.prototype.localeCompare` und `*.prototype.toLocaleString` , beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="3ae0e-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="3ae0e-189">DOM-APIs wie `navigator.language` und</span><span class="sxs-lookup"><span data-stu-id="3ae0e-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="3ae0e-190">Der [`Accept-Language`][MDNAcceptLanguage] HTTP-Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="3ae0e-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="3ae0e-191">Updates für `navigator.language` und `navigator.languages` werden nicht sofort angezeigt, sondern erst nach der nächsten Navigation oder beim erneuten Laden der Seite.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page reload.</span></span>  <span data-ttu-id="3ae0e-192">Änderungen am `Accept-Language` http-Header werden nur für nachfolgende Anforderungen wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulieren eines Gebietsschemas" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="3ae0e-194">Abbildung 10: Emulieren eines Gebietsschemas</span><span class="sxs-lookup"><span data-stu-id="3ae0e-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-195">Informationen zum Testen einer Demo finden Sie unter [Beispiel für gebietsschemaabhängigen Code][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="3ae0e-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="3ae0e-196">Chrom Problem [#1051822][crbug1051822]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-196">Chromium issue [#1051822][crbug1051822]</span></span>

### <span data-ttu-id="3ae0e-197">Debuggen von Richtlinien für die übergreifende Einbettungs Richtlinie (COEP)</span><span class="sxs-lookup"><span data-stu-id="3ae0e-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="3ae0e-198">Das Netzwerk Panel bietet nun Informationen zu Debuginformationen [über die Ursprungs Einbettungs Richtlinie][COEP] .</span><span class="sxs-lookup"><span data-stu-id="3ae0e-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="3ae0e-199">Die Spalte **Status** bietet nun eine kurze Erläuterung dazu, warum eine Anforderung blockiert wurde, sowie einen Link, um die Überschriften dieser Anforderung für weiteres Debuggen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="3ae0e-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Blockierte Anforderungen in der Spalte \* \* Status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="3ae0e-201">Abbildung 11: blockierte Anforderungen in der Spalte "Status"</span><span class="sxs-lookup"><span data-stu-id="3ae0e-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-202">Im Abschnitt " **Antwort Kopfzeilen** " auf der Registerkarte " **Kopfzeilen** " finden Sie weitere Anleitungen zur Behebung der Probleme:</span><span class="sxs-lookup"><span data-stu-id="3ae0e-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="3ae0e-204">Abbildung 12: Weitere Anleitungen im Abschnitt "Antwort Kopfzeilen"</span><span class="sxs-lookup"><span data-stu-id="3ae0e-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-205">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-206">Chrom Problem [#1051466][crbug1051466]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-206">Chromium issue [#1051466][crbug1051466]</span></span>  

### <span data-ttu-id="3ae0e-207">Anzeigen von Netzwerkanforderungen, die einen bestimmten Cookie-Pfad festzulegen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-207">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="3ae0e-208">Verwenden Sie das `cookie-path` Schlüsselwort New Filter in der Gruppe **Netzwerk** , um sich auf die Netzwerkanforderungen zu konzentrieren, die einen bestimmten [Cookie-Pfad][MDNCookiePath]festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-208">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="3ae0e-209">Schauen Sie sich [Filter Anforderungen nach Eigenschaften][NetworkProperties] an, um weitere Stichwörter wie zu entdecken `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="3ae0e-209">Check out [Filter requests by properties][NetworkProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="3ae0e-210">Andocken von Links über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="3ae0e-210">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="3ae0e-211">Öffnen Sie das [Befehl-Menü][DevToolsCommandMenuIndex] , und führen Sie den `Dock to left` Befehl aus, um devtools Links vom Viewport zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-211">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, angedockt Links vom Viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="3ae0e-213">Abbildung 13: devtools, angedockt Links vom Viewport</span><span class="sxs-lookup"><span data-stu-id="3ae0e-213">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3ae0e-214">Das Feature " **Dock to Left** " wurde seit Microsoft Edge 75 zur Verfügung gestellt, war aber zuvor nur über das [**Hauptmenü**][MainMenuDoc]zugänglich.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-214">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][MainMenuDoc].</span></span>  <span data-ttu-id="3ae0e-215">Das neue Feature in Microsoft Edge 83 ist, dass Sie nun über das Befehlsmenü auf dieses Feature zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-215">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="3ae0e-216">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-216">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-217">Chrom Problem [#1011679][crbug1011679]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-217">Chromium issue [#1011679][crbug1011679]</span></span>  

### <span data-ttu-id="3ae0e-218">Das Panel "Audits" ist jetzt das Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="3ae0e-218">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="3ae0e-219">Das devtools-Team erhielt häufig Feedback von Webentwicklern, dass es zwar möglich war, [Leuchtturm][GithubGoogleChromeLighthouse] von devtools aus zu starten, als Sie es ausprobierten, dass Sie das Panel "Leuchtturm" nicht finden konnten, daher ist das **Audit** Panel nun das **Leuchtturm** -Panel.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-219">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Das Leuchtturm-Panel" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="3ae0e-221">Abbildung 14: Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="3ae0e-221">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3ae0e-222">Das **Leuchtturm** -Panel bietet Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-222">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="3ae0e-223">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und die Daten, die Sie möglicherweise sammeln.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-223">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="3ae0e-224">Löschen aller lokalen Außerkraftsetzungen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="3ae0e-224">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="3ae0e-225">Nachdem Sie **lokale Überschreibungen** eingerichtet haben, können Sie mit der rechten Maustaste auf einen Ordner klicken und die Option " **alle Überschreibungen löschen** " auswählen, um alle lokalen Überschreibungen in diesem Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-225">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Alle Außerkraftsetzungen löschen" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="3ae0e-227">Abbildung 15: Löschen aller Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="3ae0e-227">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-228">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-228">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-229">Chrom Problem [#1016501][crbug1016501]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-229">Chromium issue [#1016501][crbug1016501]</span></span>  

### <span data-ttu-id="3ae0e-230">Benutzeroberfläche für lange Aufgaben aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3ae0e-230">Updated Long tasks UI</span></span>  

<span data-ttu-id="3ae0e-231">Eine **lange Aufgabe** ist JavaScript-Code, der den Hauptthread lange Zeit monopolisiert, wodurch eine Webseite blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-231">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="3ae0e-232">Sie haben in der Lage sein, [lange Aufgaben im Leistungs Panel][LongTasksInPerformancePanel] für eine Weile zu visualisieren, doch in Microsoft Edge 83 wurde die Benutzeroberfläche für die lange Aufgaben Visualisierung im Leistungs Panel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-232">You have been able to [visualize Long Tasks in the Performance panel][LongTasksInPerformancePanel] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="3ae0e-233">Der lange Aufgabenbereich eines Vorgangs wird nun mit einem gestreiften roten Hintergrund eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-233">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Die neue Benutzeroberfläche für lange Aufgaben" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="3ae0e-235">Abbildung 16: die neue Benutzeroberfläche für lange Aufgaben</span><span class="sxs-lookup"><span data-stu-id="3ae0e-235">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="3ae0e-236">Senden Sie Ihr Feedback, indem Sie [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-236">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="3ae0e-237">Chrom Problem [#1054447][crbug1054447]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-237">Chromium issue [#1054447][crbug1054447]</span></span>  

### <span data-ttu-id="3ae0e-238">Unterstützung für Maskierungs Symbole im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="3ae0e-238">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="3ae0e-239">Android Oreo hat Adaptive Symbole eingeführt, die APP-Symbole in einer Vielzahl von Formen in verschiedenen Gerätemodellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-239">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="3ae0e-240">**Maskierungs Symbole** sind ein neues Symbol Format, das adaptive Symbole unterstützt, mit denen Sie sicherstellen können, dass Ihr [PWA][PWADoc] -Symbol auf Geräten gut aussieht, die den Standard für Maskierungs fähige Symbole unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-240">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PWADoc] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="3ae0e-241">Aktivieren Sie das Kontrollkästchen **nur den Mindestbereich für abgesicherten Bereich für maskierte Symbole anzeigen** im Bereich **Manifest** , um zu überprüfen, ob Ihr Maskierungs Symbol auf Android Oreo-Geräten gut aussieht.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-241">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Kontrollkästchen "nur den kleinsten sicheren Bereich für maskierte Symbole anzeigen"" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="3ae0e-243">Abbildung 17: Kontrollkästchen **nur den kleinsten sicheren Bereich für Maskierungs Symbole anzeigen**</span><span class="sxs-lookup"><span data-stu-id="3ae0e-243">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3ae0e-244">Dieses Feature wurde in Microsoft Edge 81 gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-244">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="3ae0e-245">Die hier in Microsoft Edge 83 behandelten Updates wurden nicht in [Neuerungen in devtools (Microsoft Edge 81)][WhatsNew81]behandelt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-245">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="3ae0e-246">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="3ae0e-246">Feedback</span></span>  

<span data-ttu-id="3ae0e-247">So besprechen Sie die neuen Features und Änderungen in diesem Beitrag oder alles, was mit devtools zu tun hat:</span><span class="sxs-lookup"><span data-stu-id="3ae0e-247">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="3ae0e-248">Senden Sie Ihr Feedback über das **Feedback** -Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="3ae0e-248">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="3ae0e-249">Tweet bei [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="3ae0e-249">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="3ae0e-250">Einen Vorschlag an [das gewünschte Web][TheWebWeWant] senden</span><span class="sxs-lookup"><span data-stu-id="3ae0e-250">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="3ae0e-251">Datei Fehler in diesem Dokument im [Edge-Entwickler-][GitHubMicrosoftDocsEdgeDeveloperNewIssue] Repository</span><span class="sxs-lookup"><span data-stu-id="3ae0e-251">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/03/feedback-icon.msft.png" alt-text="Das \* \* Feedback \* \*-Symbol in der Microsoft Edge-devtools" lightbox="../../media/2020/03/feedback-icon.msft.png":::
   <span data-ttu-id="3ae0e-253">Abbildung 18: das Symbol " **Feedback** " in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="3ae0e-253">Figure 18:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="3ae0e-254">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="3ae0e-254">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3ae0e-255">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-255">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3ae0e-256">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-256">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge – Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview-Kanäle"  
[TheWebWeWant]: https://aka.ms/webwewant "Das gewünschte Web"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Neuerungen in devtools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte beim Anzeigen und Ändern von CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Ändern der Platzierung aus dem Hauptmenü"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Hauptthread Aktivität anzeigen"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendern""  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Erste Schritte mit dem Remote Debuggen von Windows 10-Geräten"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Haltepunkte für die Code Zeile"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Übersicht über das Windows-Geräte Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Remote Tools für Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Update für stabile Kanal Versionen für Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Arten der Farbenblindheit"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Akzeptieren – Sprache"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Beispiel für gebietsschemaabhängigen Code"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problem 963183: devtools sind nicht WCAG-kompatibel"  
[crbug1003700]: https://crbug.com/1003700 "Problem 1003700: Hinzufügen von devtools-Unterstützung für farbsehstörungen-Fehlersimulation"  
[crbug1011679]: https://crbug.com/1011679 "Problem 1011679: Einführung von "Dock to Left" über das Befehlsmenü"  
[crbug1016501]: https://crbug.com/1016501 "Problem 1016501: Feature Request: Schaltfläche zum Löschen aller lokalen Außerkraftsetzungen"  
[crbug1050999]: https://crbug.com/1050999 "Problem 1050999: Registerkarte "Eigenschaften""  
[crbug1051466]: https://crbug.com/1051466 "Problem 1051466: unterstützen des Coop/COEP-Debuggens in devtools"  
[crbug1054447]: https://crbug.com/1054447 "Problem 1054447: Aktualisieren von Leistungs Metriken in der devtools-Zeitachse"  
[crbug1051822]: https://crbug.com/1051822 "Problem 1051822: devtools: Hinzufügen einer Benutzeroberfläche zum Emulieren des Gebietsschemas"
[crbug1041830]: https://crbug.com/1041830 "Problem 1041830: verbessern der Farben für Haltepunkte"
[crbug1050855]: https://crbug.com/1050855 "Problem 1050855: die Ansicht "Einstellungen" ist schwer zu erkennen"
[crbug1056348]: https://crbug.com/1056348 "Problem 1056348: Infoleiste-Komponentenaktualisierung"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Erläuterte Coop-und COEP-Cross-Origin-Opener-Richtlinie"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Erläuterte Coop-und COEP-Richtlinien für die Ursprungs Einbettung"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse GitHub Repo"  

> [!NOTE]
> <span data-ttu-id="3ae0e-293">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3ae0e-294">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/03/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="3ae0e-294">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="3ae0e-296">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3ae0e-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
