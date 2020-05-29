---
title: Erste Schritte mit dem Remote Debuggen von Android-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611819"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# <span data-ttu-id="530ed-103">Erste Schritte mit dem Remote Debuggen von Android-Geräten</span><span class="sxs-lookup"><span data-stu-id="530ed-103">Get Started with Remote Debugging Android Devices</span></span>   



<span data-ttu-id="530ed-104">Remote Debuggen von Liveinhalten auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="530ed-105">In diesem Lernprogramm lernen Sie, wie Sie:</span><span class="sxs-lookup"><span data-stu-id="530ed-105">This tutorial teaches you how to:</span></span>  

*   <span data-ttu-id="530ed-106">Richten Sie Ihr Android-Gerät für das Remotedebuggen ein, und entdecken Sie es von Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="530ed-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="530ed-107">Überprüfen und Debuggen Sie Liveinhalte auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="530ed-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="530ed-108">Screencast-Inhalte von Ihrem Android-Gerät auf eine devtools-Instanz auf Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="530ed-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## <span data-ttu-id="530ed-109">Schritt 1: entdecken Ihres Android-Geräts</span><span class="sxs-lookup"><span data-stu-id="530ed-109">Step 1: Discover your Android device</span></span>   

<span data-ttu-id="530ed-110">Der folgende Workflow funktioniert für die meisten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="530ed-110">The workflow below works for most users.</span></span>  <span data-ttu-id="530ed-111">Informationen finden Sie unter [Problembehandlung: devtools erkennt das Android-Gerät nicht](#troubleshooting-devtools-is-not-detecting-the-android-device) , um weitere Hilfe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="530ed-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="530ed-112">Öffnen Sie den Bildschirm " **Entwickler Optionen** " auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="530ed-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="530ed-113">Weitere Informationen finden Sie unter [Konfigurieren von Optionen für Entwickler auf dem Gerät](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="530ed-113">See [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="530ed-114">Wählen Sie **USB-Debugging aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="530ed-115">Öffnen Sie auf Ihrem Entwicklungscomputer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="530ed-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="530ed-116">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="530ed-116">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="530ed-117">Wählen Sie in devtools das **Hauptmenü** und `...` dann **Weitere Tools**  >  **Remote Devices**aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-117">In DevTools, select the **Main Menu** `...` then select **More tools** > **Remote devices**.</span></span>  
    
    > ##### <span data-ttu-id="530ed-118">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="530ed-118">Figure 1</span></span>  
    > <span data-ttu-id="530ed-119">Öffnen des Reiters " **Remote Devices** " über das **Hauptmenü**</span><span class="sxs-lookup"><span data-stu-id="530ed-119">Opening the **Remote Devices** tab via the **Main Menu**</span></span>  
    > <span data-ttu-id="530ed-120">! [Öffnen der Registerkarte ' Remote Devices ' über das Hauptmenü] [ImageOpenRemoteDevices]</span><span class="sxs-lookup"><span data-stu-id="530ed-120">![Opening the Remote Devices tab via the Main Menu][ImageOpenRemoteDevices]</span></span>  

1.  <span data-ttu-id="530ed-121">Öffnen Sie in devtools die Registerkarte **Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="530ed-121">In DevTools, open the **Settings** tab.</span></span>  

1.  <span data-ttu-id="530ed-122">Stellen Sie sicher, dass das Kontrollkästchen **USB-Geräte entdecken** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="530ed-122">Make sure that the **Discover USB devices** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="530ed-123">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="530ed-123">Figure 2</span></span>  
    > <span data-ttu-id="530ed-124">Das Kontrollkästchen " **USB-Geräte entdecken** " ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="530ed-124">The **Discover USB Devices** checkbox is enabled</span></span>  
    > <span data-ttu-id="530ed-125">! [Das Kontrollkästchen USB-Geräte entdecken ist aktiviert] [ImageDiscoverUSBDevices]</span><span class="sxs-lookup"><span data-stu-id="530ed-125">![The Discover USB Devices checkbox is enabled][ImageDiscoverUSBDevices]</span></span>  

1.  <span data-ttu-id="530ed-126">Verbinden Sie Ihr Android-Gerät mit einem USB-Kabel direkt mit Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="530ed-126">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="530ed-127">Wenn Sie dies zum ersten Mal ausführen, sehen Sie in der Regel, dass devtools ein unbekanntes Gerät gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="530ed-127">The first time you do this, you usually see that DevTools has detected an unknown device.</span></span>  <span data-ttu-id="530ed-128">Wenn ein grüner Punkt und der Text unter dem Modellnamen Ihres Android-Geräts **verbunden** sind, hat devtools die Verbindung zu Ihrem Gerät erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="530ed-128">If you see a green dot and the text **Connected** below the model name of your Android device, then DevTools has successfully established the connection to your device.</span></span>  <span data-ttu-id="530ed-129">Fahren Sie mit [Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine)fort.</span><span class="sxs-lookup"><span data-stu-id="530ed-129">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  <span data-ttu-id="530ed-130">Wenn Ihr Gerät als " **unbekannt**" angezeigt wird, akzeptieren Sie die Eingabeaufforderung " **USB-Debugging-Genehmigung zulassen** " auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="530ed-130">If your device is showing up as **Unknown**, accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  

### <span data-ttu-id="530ed-131">Problembehandlung: devtools erkennt das Android-Gerät nicht.</span><span class="sxs-lookup"><span data-stu-id="530ed-131">Troubleshooting: DevTools is not detecting the Android device</span></span>   

<span data-ttu-id="530ed-132">Stellen Sie sicher, dass Ihre Hardware richtig eingerichtet ist:</span><span class="sxs-lookup"><span data-stu-id="530ed-132">Make sure that your hardware is set up correctly:</span></span>  

*   <span data-ttu-id="530ed-133">Wenn Sie einen USB-Hub verwenden, sollten Sie stattdessen das Android-Gerät direkt an Ihren Entwicklungscomputer anschließen.</span><span class="sxs-lookup"><span data-stu-id="530ed-133">If you are using a USB hub, try connecting your Android device directly to your development machine instead.</span></span>  
*   <span data-ttu-id="530ed-134">Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie es dann wieder an.</span><span class="sxs-lookup"><span data-stu-id="530ed-134">Try unplugging the USB cable between your Android device and development machine, and then plugging it back in.</span></span>  <span data-ttu-id="530ed-135">Tun Sie es, während die Bildschirme Ihres Android-und Entwicklungscomputers entriegelt sind.</span><span class="sxs-lookup"><span data-stu-id="530ed-135">Do it while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="530ed-136">Stellen Sie sicher, dass Ihr USB-Kabel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="530ed-136">Make sure that your USB cable works.</span></span>  <span data-ttu-id="530ed-137">Sie sollten Dateien auf Ihrem Android-Gerät über Ihren Entwicklungscomputer prüfen können.</span><span class="sxs-lookup"><span data-stu-id="530ed-137">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="530ed-138">Stellen Sie sicher, dass Ihre Software richtig eingerichtet ist:</span><span class="sxs-lookup"><span data-stu-id="530ed-138">Make sure that your software is set up correctly:</span></span>  

*   <span data-ttu-id="530ed-139">Wenn auf Ihrem Entwicklungscomputer Windows ausgeführt wird, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="530ed-139">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="530ed-140">Siehe [Installieren von OEM-USB-Treibern][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="530ed-140">See [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
    
*   <span data-ttu-id="530ed-141">Einige Kombinationen von Windows-und Android-Geräten (insbesondere Samsung) erfordern eine zusätzliche Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="530ed-141">Some combinations of Windows and Android devices (especially Samsung) require extra set up.</span></span>  <span data-ttu-id="530ed-142">Weitere Informationen finden Sie unter [devtools Devices erkennt Device nicht, wenn es angeschlossen wird] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="530ed-142">See [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  
    
<span data-ttu-id="530ed-143">Wenn auf Ihrem Android-Gerät die Eingabeaufforderung **USB-Debugging zulassen** nicht angezeigt wird, versuchen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="530ed-143">If you do not see the **Allow USB Debugging** prompt on your Android device try:</span></span>  

*   <span data-ttu-id="530ed-144">Trennen Sie das USB-Kabel, und verbinden Sie es dann erneut, während sich devtools auf Ihrem Entwicklungscomputer befindet und Ihr Android-Homescreen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="530ed-144">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  <span data-ttu-id="530ed-145">Mit anderen Worten: Manchmal wird die Eingabeaufforderung nicht angezeigt, wenn Ihre Android-oder Entwicklungscomputer Bildschirme gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="530ed-145">In other words, sometimes the prompt does not show up when your Android or development machine screens are locked.</span></span>
*   <span data-ttu-id="530ed-146">Aktualisieren Sie die Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, damit Sie nie in den Ruhezustand wechseln.</span><span class="sxs-lookup"><span data-stu-id="530ed-146">Updating the display settings for your Android device and development machine so that they never go to sleep.</span></span>  
*   <span data-ttu-id="530ed-147">Festlegen des USB-Modus für Android auf PTP</span><span class="sxs-lookup"><span data-stu-id="530ed-147">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="530ed-148">Siehe [Galaxy S4 zeigt das Dialogfeld "Autorisieren von USB-Debuggen" nicht][StackExchangeGalaxyS4DoesNotShowDialogBox]an.</span><span class="sxs-lookup"><span data-stu-id="530ed-148">See [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="530ed-149">Wählen Sie auf Ihrem Android-Gerät auf dem Bildschirm **Entwickler Optionen** die Option **USB-Debugging-Berechtigungen widerrufen** aus, um den Status auf "neu" zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="530ed-149">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="530ed-150">Wenn Sie eine Lösung finden, die in diesem Abschnitt oder in [devtools Devices Device nicht erkannt wird, wenn Sie angeschlossen sind] [StackOverflowDevicesNotDetected] oder bitte eine Antwort auf diese Stapelüberlauf Frage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="530ed-150">If you find a solution that is not mentioned in this section or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] or please add an answer to that Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="530ed-151">!</span><span class="sxs-lookup"><span data-stu-id="530ed-151">!</span></span>  

## <span data-ttu-id="530ed-152">Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf dem Entwicklungscomputer</span><span class="sxs-lookup"><span data-stu-id="530ed-152">Step 2: Debug content on your Android device from your development machine</span></span>   

1.  <span data-ttu-id="530ed-153">Öffnen Sie Microsoft Edge auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="530ed-153">Open Microsoft Edge on your Android device.</span></span>  

1.  <span data-ttu-id="530ed-154">Wählen Sie auf der Registerkarte **Remote Geräte** die Registerkarte aus, die dem Modellnamen Ihres Android-Geräts entspricht.</span><span class="sxs-lookup"><span data-stu-id="530ed-154">In the **Remote Devices** tab, select the tab that matches your Android device model name.</span></span>  
    <span data-ttu-id="530ed-155">Oben auf dieser Seite sehen Sie den Modellnamen Ihres Android-Geräts, gefolgt von der Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="530ed-155">At the top of this page, you see the model name of your Android device, followed by its serial number.</span></span>  <span data-ttu-id="530ed-156">Darunter sollte die Version von Microsoft Edge auf dem Gerät mit der Versionsnummer in Klammern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="530ed-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="530ed-157">Jede geöffnete Microsoft Edge-Registerkarte erhält einen eigenen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="530ed-157">Each open Microsoft Edge tab gets its own section.</span></span>  <span data-ttu-id="530ed-158">In diesem Abschnitt können Sie mit dieser Registerkarte interagieren.</span><span class="sxs-lookup"><span data-stu-id="530ed-158">You may interact with that tab from this section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  <span data-ttu-id="530ed-159">Geben Sie im Textfeld **neue Registerkarte** eine URL ein, und wählen Sie dann **Öffnen**aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-159">In the **New tab** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="530ed-160">Die Seite wird in einer neuen Registerkarte auf Ihrem Android-Gerät geöffnet.</span><span class="sxs-lookup"><span data-stu-id="530ed-160">The page opens in a new tab on your Android device.</span></span>  

1.  <span data-ttu-id="530ed-161">Wählen Sie neben der soeben geöffneten URL über **prüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-161">Select **Inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="530ed-162">Eine neue devtools-Instanz wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="530ed-162">A new DevTools instance opens.</span></span>  <span data-ttu-id="530ed-163">Die Version von Microsoft Edge, die auf Ihrem Android-Gerät ausgeführt wird, bestimmt die Version von devtools, die auf Ihrem Entwicklungscomputer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="530ed-163">The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.</span></span>  
    <span data-ttu-id="530ed-164">Wenn auf Ihrem Android-Gerät also eine sehr alte Version von Microsoft Edge ausgeführt wird, sieht die devtools-Instanz möglicherweise sehr unterschiedlich aus, als Sie es gewohnt sind.</span><span class="sxs-lookup"><span data-stu-id="530ed-164">So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.</span></span>  

### <span data-ttu-id="530ed-165">Weitere Aktionen: Erneutes Laden, fokussieren oder Schließen einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="530ed-165">More actions: reload, focus, or close a tab</span></span>   

<span data-ttu-id="530ed-166">Wählen Sie **Weitere Optionen** `...` neben der Registerkarte aus, die Sie erneut laden, fokussieren oder schließen möchten.</span><span class="sxs-lookup"><span data-stu-id="530ed-166">Select **More Options** `...` next to the tab that you want to reload, focus, or close.</span></span>  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### <span data-ttu-id="530ed-167">Überprüfen von Elementen</span><span class="sxs-lookup"><span data-stu-id="530ed-167">Inspect elements</span></span>   

<span data-ttu-id="530ed-168">Wechseln Sie zum Panel **Elemente** der devtools-Instanz, und zeigen Sie mit der Maus auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.</span><span class="sxs-lookup"><span data-stu-id="530ed-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="530ed-169">Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im **Element** Bereich auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="530ed-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="530ed-170">Wählen **Sie Element** ![ ][ImageSelectElementIcon] in ihrer devtools-Instanz auswählen aus, und wählen Sie dann das Element auf dem Bildschirm Ihres Android-Geräts aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="530ed-171">**Element auswählen** ist nach der ersten Auswahl deaktiviert, damit Sie es jedes Mal wieder aktivieren müssen, wenn Sie dieses Feature verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="530ed-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use this feature.</span></span>  

### <span data-ttu-id="530ed-172">Screencast Ihres Android-Bildschirms auf Ihrem Entwicklungscomputer</span><span class="sxs-lookup"><span data-stu-id="530ed-172">Screencast your Android screen to your development machine</span></span>   

<span data-ttu-id="530ed-173">Wählen Sie **Screencast** umschalten ![ Screencast aus ][ImageToggleScreencastIcon] , um den Inhalt Ihres Android-Geräts in ihrer devtools-Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="530ed-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="530ed-174">Sie können mit dem Screencast auf verschiedene Arten interagieren:</span><span class="sxs-lookup"><span data-stu-id="530ed-174">You are able to interact with the screencast in multiple ways:</span></span>  

*   <span data-ttu-id="530ed-175">Klicks werden in TAPS übersetzt, wobei die richtigen Touch-Ereignisse auf dem Gerät ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="530ed-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="530ed-176">Tastenanschläge auf dem Computer werden an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="530ed-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="530ed-177">Wenn Sie eine Pinch-Geste simulieren möchten, halten Sie `Shift` beim Ziehen gedrückt.</span><span class="sxs-lookup"><span data-stu-id="530ed-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="530ed-178">Verwenden Sie zum Scrollen das Trackpad oder Mausrad, oder werfen Sie den Mauszeiger auf.</span><span class="sxs-lookup"><span data-stu-id="530ed-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

<span data-ttu-id="530ed-179">Einige Hinweise zu Screencasts:</span><span class="sxs-lookup"><span data-stu-id="530ed-179">Some notes on screencasts:</span></span>  

*   <span data-ttu-id="530ed-180">Screencasts zeigen nur Seiteninhalte an.</span><span class="sxs-lookup"><span data-stu-id="530ed-180">Screencasts only display page content.</span></span>  <span data-ttu-id="530ed-181">Transparente Abschnitte des Screencasts stellen Geräteschnittstellen dar, beispielsweise die Microsoft Edge-Adressleiste, die Android-Statusleiste oder die Android-Tastatur.</span><span class="sxs-lookup"><span data-stu-id="530ed-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
*   <span data-ttu-id="530ed-182">Screencasts wirken sich negativ auf die Frame-Raten aus.</span><span class="sxs-lookup"><span data-stu-id="530ed-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="530ed-183">Deaktivieren Sie das Screencasting beim Messen von Scrolls oder Animationen, um eine genauere Vorstellung von der Leistung Ihrer Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="530ed-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
*   <span data-ttu-id="530ed-184">Wenn Ihr Android-Gerät gesperrt ist, wird der Inhalt Ihres Screencasts nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="530ed-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="530ed-185">Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="530ed-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-More-Tools-Remote-Devices.msft.png "Abbildung 1: Öffnen der Registerkarte" Remotegeräte "über das Hauptmenü  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "Abbildung 2: das Kontrollkästchen" USB-Geräte entdecken "ist aktiviert.  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Installieren von OEM-USB-Treibern | Android-Entwickler"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "devtools-Geräte erkennen das Gerät nicht, wenn ein Stapelüberlauf eingesteckt wird"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-Android-Enthusiast Stack Exchange"  

> [!NOTE]
> <span data-ttu-id="530ed-192">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="530ed-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="530ed-193">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="530ed-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="530ed-195">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="530ed-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
