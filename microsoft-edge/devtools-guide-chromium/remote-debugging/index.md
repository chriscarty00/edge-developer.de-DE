---
description: Remote Debuggen von Liveinhalten auf einem Android-Gerät von einem Windows-oder macOS-Computer aus.
title: Erste Schritte mit dem Remote Debuggen von Android-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c6bdb48460fb8f6ff26cbb02872e33cb50dd6e12
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125363"
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

# <span data-ttu-id="4eca3-104">Erste Schritte mit dem Remotedebuggen von Android-Geräten</span><span class="sxs-lookup"><span data-stu-id="4eca3-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="4eca3-105">Remote Debuggen von Liveinhalten auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="4eca3-106">Auf der folgenden Lernprogramm Seite Lernen Sie, wie Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="4eca3-107">Richten Sie Ihr Android-Gerät für das Remotedebuggen ein, und entdecken Sie es von Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="4eca3-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="4eca3-108">Überprüfen und Debuggen Sie Liveinhalte auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="4eca3-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="4eca3-109">Screencast-Inhalte von Ihrem Android-Gerät auf eine devtools-Instanz auf Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="4eca3-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="4eca3-110">Remote Debuggen die Microsoft Edge-App auf IOS-Geräten wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="4eca3-111">Das folgende Handbuch ist speziell auf das Remotedebuggen von Microsoft Edge auf Android-Geräten ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="4eca3-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="4eca3-112">Wenn Sie über ein macOS-Gerät verfügen, folgen Sie dem [Brightcove-Debugging-Leitfaden][BrightcoveSupportDebuggingMobileDevices] , um Microsoft Edge auf einem IOS-Gerät mithilfe von Safari Remote zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="4eca3-113">Weitere Informationen zum Tool Web Inspector in Safari finden Sie unter [Safari-Webentwicklungstools][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="4eca3-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="4eca3-114">Schritt 1: entdecken Ihres Android-Geräts</span><span class="sxs-lookup"><span data-stu-id="4eca3-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="4eca3-115">Der folgende Workflow funktioniert für die meisten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4eca3-115">The workflow below works for most users.</span></span>  <span data-ttu-id="4eca3-116">Wenn Sie weitere Hilfe benötigen, navigieren Sie zur [Problembehandlung: devtools erkennt den Abschnitt Android-Gerät nicht](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="4eca3-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="4eca3-117">Öffnen Sie den Bildschirm " **Entwickler Optionen** " auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4eca3-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="4eca3-118">Weitere Informationen finden Sie unter [Konfigurieren von Optionen für Entwickler auf einem Gerät][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="4eca3-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="4eca3-119">Wählen Sie **USB-Debugging aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="4eca3-120">Öffnen Sie auf Ihrem Entwicklungscomputer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4eca3-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="4eca3-121">Navigieren Sie zu der `edge://inspect` Seite in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4eca3-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="4eca3-123">Abbildung1.</span><span class="sxs-lookup"><span data-stu-id="4eca3-123">Figure 1.</span></span>  <span data-ttu-id="4eca3-124">Die `edge://inspect` Seite in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4eca3-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4eca3-125">Verbinden Sie Ihr Android-Gerät mit einem USB-Kabel direkt mit Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="4eca3-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="4eca3-126">Wenn Sie das erste Mal versuchen, eine Verbindung herzustellen, sollte eine Aufforderung zu devtools angezeigt werden, um ein unbekanntes Gerät zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="4eca3-127">Akzeptieren Sie die Eingabeaufforderung **USB-Debugging-Berechtigung zulassen** auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4eca3-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="4eca3-129">Abbildung2.</span><span class="sxs-lookup"><span data-stu-id="4eca3-129">Figure 2.</span></span>  <span data-ttu-id="4eca3-130">Die Eingabeaufforderung " **USB-Debugging-Berechtigung zulassen** " auf einem Android-Gerät</span><span class="sxs-lookup"><span data-stu-id="4eca3-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4eca3-131">Wenn der Modellname Ihres Android-Geräts angezeigt wird, hat Microsoft Edge die Verbindung zu Ihrem Gerät erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="4eca3-132">Fahren Sie mit dem Abschnitt [Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) fort.</span><span class="sxs-lookup"><span data-stu-id="4eca3-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="4eca3-133">Problembehandlung: devtools erkennt das Android-Gerät nicht.</span><span class="sxs-lookup"><span data-stu-id="4eca3-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="4eca3-134">Verwenden Sie die folgenden Tipps, um Ihnen bei der Problembehandlung der richtigen Einstellungen für Ihre Hardware zu helfen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="4eca3-135">Wenn Sie einen USB-Hub verwenden, versuchen Sie, Ihr Android-Gerät direkt an Ihren Entwicklungscomputer anzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="4eca3-136">Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie dann das USB-Kabel neu an.</span><span class="sxs-lookup"><span data-stu-id="4eca3-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="4eca3-137">Führen Sie die Aufgabe aus, während ihre Android-und Entwicklungscomputer Bildschirme entriegelt sind.</span><span class="sxs-lookup"><span data-stu-id="4eca3-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="4eca3-138">Stellen Sie sicher, dass Ihr USB-Kabel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4eca3-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="4eca3-139">Sie sollten Dateien auf Ihrem Android-Gerät über Ihren Entwicklungscomputer prüfen können.</span><span class="sxs-lookup"><span data-stu-id="4eca3-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="4eca3-140">Verwenden Sie die folgenden Tipps, um zu überprüfen, ob die Software ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="4eca3-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="4eca3-141">Wenn auf Ihrem Entwicklungscomputer Windows ausgeführt wird, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4eca3-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="4eca3-142">Weitere Informationen finden Sie unter [Installieren von OEM-USB-Treibern][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="4eca3-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="4eca3-143">Einige Kombinationen von Windows-und Android-Geräten \ (insbesondere Samsung \) erfordern zusätzliche Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="4eca3-144">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [devtools Geräte erkennt das Gerät nicht, wenn es angeschlossen ist][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="4eca3-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="4eca3-145">Verwenden Sie die folgenden Tipps, um Sie bei der Problembehandlung zu unterstützen, wenn die Eingabeaufforderung **USB-Debugging zulassen** auf Ihrem Android-Gerät nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4eca3-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="4eca3-146">Trennen Sie das USB-Kabel, und verbinden Sie es dann erneut, während sich devtools auf Ihrem Entwicklungscomputer befindet und Ihr Android-Homescreen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4eca3-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4eca3-147">Die Eingabeaufforderung wird angezeigt, wenn Ihre Android-oder Entwicklungscomputer Bildschirme gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="4eca3-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="4eca3-148">Aktualisieren der Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, damit jeder nie in den Ruhezustand wechselt</span><span class="sxs-lookup"><span data-stu-id="4eca3-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="4eca3-149">Festlegen des USB-Modus für Android auf PTP</span><span class="sxs-lookup"><span data-stu-id="4eca3-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="4eca3-150">Weitere Informationen finden Sie unter [Galaxy S4 zeigt das Dialogfeld Autorisierungs-USB-Debugging nicht][StackexchangeAndroid101933]an.</span><span class="sxs-lookup"><span data-stu-id="4eca3-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="4eca3-151">Wählen Sie auf dem Android-Gerät auf dem Bildschirm **Entwickler Optionen** die Option **USB-Debugging-Berechtigungen widerrufen** aus, um den Status auf "neu" zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="4eca3-152">Wenn Sie eine Lösung finden, die auf dieser Seite nicht aufgeführt ist, oder wenn in [devtools-Geräten das Gerät nicht erkannt][Stackoverflow21925992] wird, wenn es sich beim Stapelüberlauf befindet, fügen Sie Ihre Lösung zur Stapelüberlauf Frage hinzu.</span><span class="sxs-lookup"><span data-stu-id="4eca3-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="4eca3-153">!</span><span class="sxs-lookup"><span data-stu-id="4eca3-153">!</span></span>  

## <span data-ttu-id="4eca3-154">Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf dem Entwicklungscomputer</span><span class="sxs-lookup"><span data-stu-id="4eca3-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="4eca3-155">Öffnen Sie Microsoft Edge auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4eca3-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="4eca3-156">Navigieren Sie zu `edge://inspect` , wird der Modellname Ihres Android-Geräts angezeigt, gefolgt von der Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4eca3-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="4eca3-157">Darunter sollte die Version von Microsoft Edge, die auf dem Gerät ausgeführt wird, mit der Versionsnummer in Klammern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4eca3-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="4eca3-158">Auf jeder geöffneten Microsoft Edge-Registerkarte wird ein eindeutiger Abschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="4eca3-159">Sie können mit dieser Registerkarte in einem Abschnitt interagieren.</span><span class="sxs-lookup"><span data-stu-id="4eca3-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="4eca3-161">Abbildung3.</span><span class="sxs-lookup"><span data-stu-id="4eca3-161">Figure 3.</span></span>  <span data-ttu-id="4eca3-162">Ein verbundenes Remotegerät</span><span class="sxs-lookup"><span data-stu-id="4eca3-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4eca3-163">Geben Sie im Textfeld **Öffnen mit URL** eine URL ein, und wählen Sie dann **Öffnen**aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="4eca3-164">Die Seite wird in einer neuen Registerkarte auf Ihrem Android-Gerät geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4eca3-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="4eca3-165">Wählen Sie neben der soeben geöffneten URL über **prüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="4eca3-166">Eine neue devtools-Instanz wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4eca3-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="4eca3-167">Weitere Aktionen: fokussieren, erneutes Laden oder Schließen einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="4eca3-167">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="4eca3-168">Wählen Sie die **Registerkarte Fokus**, **erneut laden**oder **Schließen** neben der Registerkarte aus, die Sie fokussieren, erneut laden oder schließen möchten.</span><span class="sxs-lookup"><span data-stu-id="4eca3-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="4eca3-170">Abbildung 4.</span><span class="sxs-lookup"><span data-stu-id="4eca3-170">Figure 4.</span></span>  <span data-ttu-id="4eca3-171">Die Schaltflächen zum fokussieren, erneuten Laden oder Schließen einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="4eca3-171">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="4eca3-172">Überprüfen von Elementen</span><span class="sxs-lookup"><span data-stu-id="4eca3-172">Inspect elements</span></span>  

<span data-ttu-id="4eca3-173">Wechseln Sie zum Panel **Elemente** der devtools-Instanz, und zeigen Sie mit der Maus auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4eca3-173">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="4eca3-174">Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im **Element** Bereich auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-174">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="4eca3-175">Wählen **Sie** ![ ][ImageSelectElementIcon] in ihrer devtools-Instanz das Symbol Element \ (Element auswählen \) aus, und wählen Sie dann das Element auf dem Bildschirm Ihres Android-Geräts aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="4eca3-176">**Element auswählen** ist nach der ersten Auswahl deaktiviert, damit Sie es jedes Mal wieder aktivieren müssen, wenn Sie das Feature verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4eca3-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="4eca3-177">Screencast Ihres Android-Bildschirms auf Ihrem Entwicklungscomputer</span><span class="sxs-lookup"><span data-stu-id="4eca3-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="4eca3-178">Wählen Sie **Screencast umschalten** \ ( ![ Screencast ][ImageToggleScreencastIcon] \) Symbol aus, um den Inhalt Ihres Android-Geräts in ihrer devtools-Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="4eca3-179">Sie können mit dem Screencast wie folgt interagieren:</span><span class="sxs-lookup"><span data-stu-id="4eca3-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="4eca3-180">Klicks werden in TAPS übersetzt, wobei die richtigen Touch-Ereignisse auf dem Gerät ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4eca3-180">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="4eca3-181">Tastenanschläge auf dem Computer werden an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="4eca3-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="4eca3-182">Wenn Sie eine Pinch-Geste simulieren möchten, halten Sie `Shift` beim Ziehen gedrückt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="4eca3-183">Verwenden Sie zum Scrollen das Trackpad oder Mausrad, oder werfen Sie den Mauszeiger auf.</span><span class="sxs-lookup"><span data-stu-id="4eca3-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="4eca3-184">Verwenden Sie die folgenden Tipps, um Ihnen einen Screencast zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="4eca3-185">Screencasts zeigen nur Seiteninhalte an.</span><span class="sxs-lookup"><span data-stu-id="4eca3-185">Screencasts only display page content.</span></span>  <span data-ttu-id="4eca3-186">Transparente Abschnitte des Screencasts stellen Geräteschnittstellen dar, beispielsweise die Microsoft Edge-Adressleiste, die Android-Statusleiste oder die Android-Tastatur.</span><span class="sxs-lookup"><span data-stu-id="4eca3-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="4eca3-187">Screencasts wirken sich negativ auf die Frame-Raten aus.</span><span class="sxs-lookup"><span data-stu-id="4eca3-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="4eca3-188">Deaktivieren Sie das Screencasting beim Messen von Scrolls oder Animationen, um eine genauere Vorstellung von der Leistung Ihrer Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4eca3-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="4eca3-189">Wenn Ihr Android-Gerät gesperrt ist, wird der Inhalt Ihres Screencasts nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="4eca3-190">Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4eca3-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <span data-ttu-id="4eca3-191">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="4eca3-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Konfigurieren von Optionen für Entwickler auf einem Gerät | Android-Entwickler"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installieren von OEM-USB-Treibern | Android-Entwickler"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Safari-Webentwicklungs Tools | Apple-Entwickler"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Debuggen auf mobilen Geräten | Brightcove-Support"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB-Android-Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevTools-Geräte erkennen das Gerät nicht, wenn ein eingesteckter Stapelüberlauf vorliegt"  

> [!NOTE]
> <span data-ttu-id="4eca3-198">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4eca3-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4eca3-199">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4eca3-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4eca3-201">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4eca3-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
