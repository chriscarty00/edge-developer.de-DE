---
description: Remotedebuggern von Liveinhalten auf einem Android-Gerät von einem Windows- oder macOS-Computer aus.
title: Erste Schritte mit remote debuggen von Android-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 61fad793ca03dbef68a5f769dbfd25e780fd9930
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398259"
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

# <a name="get-started-with-remote-debugging-android-devices"></a><span data-ttu-id="ec19f-104">Erste Schritte mit remote debuggen von Android-Geräten</span><span class="sxs-lookup"><span data-stu-id="ec19f-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="ec19f-105">Remotedebuggern von Liveinhalten auf einem Android-Gerät von Ihrem Windows- oder macOS-Computer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="ec19f-106">Auf der folgenden Lernprogrammseite erfahren Sie, wie Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="ec19f-107">Richten Sie Ihr Android-Gerät für das Remotedebubugen ein, und ermitteln Sie es auf Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="ec19f-108">Überprüfen und Debuggen von Liveinhalten auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="ec19f-109">Screencastinhalt von Ihrem Android-Gerät auf eine DevTools-Instanz auf Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="ec19f-110">Das Remotedebuding der Microsoft Edge-App auf iOS-Geräten wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec19f-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="ec19f-111">Die folgende Anleitung konzentriert sich speziell auf das Remotedebugen von Microsoft Edge auf Android-Geräten.</span><span class="sxs-lookup"><span data-stu-id="ec19f-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="ec19f-112">Wenn Sie über ein macOS-Gerät verfügen, befolgen Sie die [Anleitung zum Debuggen von Brightcove,][BrightcoveSupportDebuggingMobileDevices] um Microsoft Edge mithilfe von Safari remote auf einem iOS-Gerät zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="ec19f-113">Weitere Informationen zum Web Inspector-Tool in Safari finden Sie unter [Safari Web Development Tools][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="ec19f-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <a name="step-1-discover-your-android-device"></a><span data-ttu-id="ec19f-114">Schritt 1: Ermitteln Ihres Android-Geräts</span><span class="sxs-lookup"><span data-stu-id="ec19f-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="ec19f-115">Der folgende Workflow funktioniert für die meisten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-115">The workflow below works for most users.</span></span>  <span data-ttu-id="ec19f-116">Weitere Hilfe finden Sie unter [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span><span class="sxs-lookup"><span data-stu-id="ec19f-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="ec19f-117">Öffnen Sie **den Bildschirm Entwickleroptionen** auf Ihrem Android.</span><span class="sxs-lookup"><span data-stu-id="ec19f-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="ec19f-118">Weitere Informationen finden Sie unter [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="ec19f-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="ec19f-119">Wählen **Sie USB-Debugging aktivieren aus.**</span><span class="sxs-lookup"><span data-stu-id="ec19f-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="ec19f-120">Öffnen Sie auf Ihrem Entwicklungscomputer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec19f-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="ec19f-121">Navigieren Sie zur `edge://inspect` Seite in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec19f-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Die edge://inspect in Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="ec19f-123">Abbildung1.</span><span class="sxs-lookup"><span data-stu-id="ec19f-123">Figure 1.</span></span>  <span data-ttu-id="ec19f-124">Die `edge://inspect` Seite in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ec19f-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec19f-125">Verbinden Sie Ihr Android-Gerät über ein USB-Kabel direkt mit Ihrem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="ec19f-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="ec19f-126">Wenn Sie zum ersten Mal versuchen, eine Verbindung herzustellen, sollte eine Eingabeaufforderung zum Erkennen eines unbekannten Geräts durch DevTools angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec19f-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="ec19f-127">Akzeptieren Sie **die Berechtigungsaufforderung USB-Debugging** zulassen auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="ec19f-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Die Berechtigungsaufforderung USB-Debugging zulassen auf einem Android-Gerät" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="ec19f-129">Abbildung2.</span><span class="sxs-lookup"><span data-stu-id="ec19f-129">Figure 2.</span></span>  <span data-ttu-id="ec19f-130">Die **Berechtigungsaufforderung USB-Debugging** zulassen auf einem Android-Gerät</span><span class="sxs-lookup"><span data-stu-id="ec19f-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec19f-131">Wenn der Modellname Ihres Android-Geräts angezeigt wird, hat Microsoft Edge die Verbindung zu Ihrem Gerät erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="ec19f-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="ec19f-132">Fahren Sie mit [dem Abschnitt Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) fort.</span><span class="sxs-lookup"><span data-stu-id="ec19f-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a><span data-ttu-id="ec19f-133">Problembehandlung: DevTools erkennt das Android-Gerät nicht</span><span class="sxs-lookup"><span data-stu-id="ec19f-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="ec19f-134">Verwenden Sie die folgenden Tipps, um Ihnen bei der Problembehandlung der richtigen Einstellungen für Ihre Hardware zu helfen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="ec19f-135">Wenn Sie einen USB-Hub verwenden, versuchen Sie, Ihr Android-Gerät direkt mit Ihrem Entwicklungscomputer zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ec19f-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="ec19f-136">Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie das USB-Kabel erneut an.</span><span class="sxs-lookup"><span data-stu-id="ec19f-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="ec19f-137">Führen Sie die Aufgabe aus, während die Bildschirme ihres Android- und Entwicklungscomputers entsperrt sind.</span><span class="sxs-lookup"><span data-stu-id="ec19f-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="ec19f-138">Stellen Sie sicher, dass Das USB-Kabel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ec19f-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="ec19f-139">Sie sollten Dateien auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer aus überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="ec19f-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="ec19f-140">Verwenden Sie die folgenden Tipps, um zu überprüfen, ob Ihre Software ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="ec19f-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="ec19f-141">Wenn auf ihrem Entwicklungscomputer Windows ausgeführt wird, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ec19f-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="ec19f-142">Weitere Informationen finden Sie unter [Installieren von OEM-USB-Treibern.][AndroidDeveloperToolsOemUsb]</span><span class="sxs-lookup"><span data-stu-id="ec19f-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="ec19f-143">Einige Kombinationen von Windows- und Android-Geräten \(insbesondere Samsung\) erfordern zusätzliche Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="ec19f-144">Weitere Informationen finden Sie unter [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="ec19f-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="ec19f-145">Verwenden Sie die folgenden Tipps, um Probleme zu beheben, wenn die Eingabeaufforderung **USB-Debugging** zulassen nicht auf Ihrem Android-Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec19f-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="ec19f-146">Trennen Sie die Verbindung, und verbinden Sie das USB-Kabel erneut, während DevTools auf Ihrem Entwicklungscomputer im Fokus steht und Ihr Android-Startbildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec19f-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ec19f-147">Die Eingabeaufforderung wird angezeigt, wenn Die Bildschirme ihres Android- oder Entwicklungscomputers gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="ec19f-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="ec19f-148">Aktualisieren der Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, sodass sie niemals in den Ruhezustand gehen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="ec19f-149">Festlegen des USB-Modus für Android auf PTP.</span><span class="sxs-lookup"><span data-stu-id="ec19f-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="ec19f-150">Weitere Informationen finden Sie unter Navigieren zu [Das Dialogfeld USB-Debuggen][StackexchangeAndroid101933]autorisieren wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ec19f-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="ec19f-151">Klicken Sie auf dem \*\*\*\* Bildschirm Entwickleroptionen auf Ihrem Android-Gerät auf Widerrufen von USB-Debuggingautorisierungen, um es auf einen neuen Status zurückzusetzen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ec19f-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="ec19f-152">Wenn Sie eine Lösung finden, die auf dieser Seite oder in [DevTools Devices][Stackoverflow21925992] nicht erkannt wird, wenn das Gerät auf Stack Overflow angeschlossen ist, fügen Sie Ihre Lösung der Frage Stack Overflow hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec19f-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="ec19f-153">.</span><span class="sxs-lookup"><span data-stu-id="ec19f-153">.</span></span>  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a><span data-ttu-id="ec19f-154">Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer</span><span class="sxs-lookup"><span data-stu-id="ec19f-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="ec19f-155">Öffnen Sie Microsoft Edge auf Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="ec19f-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="ec19f-156">Navigieren Sie `edge://inspect` zu , der Modellname Ihres Android-Geräts wird angezeigt, gefolgt von der Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ec19f-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="ec19f-157">Unten sollte die auf dem Gerät ausgeführte Version von Microsoft Edge mit der Versionsnummer in Klammern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec19f-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="ec19f-158">Jede geöffnete Microsoft Edge-Registerkarte erhält einen eindeutigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="ec19f-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="ec19f-159">Sie können über einen Abschnitt mit dieser Registerkarte interagieren.</span><span class="sxs-lookup"><span data-stu-id="ec19f-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Ein verbundenes Remotegerät" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="ec19f-161">Abbildung3.</span><span class="sxs-lookup"><span data-stu-id="ec19f-161">Figure 3.</span></span>  <span data-ttu-id="ec19f-162">Ein verbundenes Remotegerät</span><span class="sxs-lookup"><span data-stu-id="ec19f-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec19f-163">Geben Sie **im Textfeld Registerkarte Öffnen** mit URL eine URL ein, und wählen Sie dann Öffnen **aus.**</span><span class="sxs-lookup"><span data-stu-id="ec19f-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="ec19f-164">Die Seite wird auf ihrem Android-Gerät auf einer neuen Registerkarte geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ec19f-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="ec19f-165">Wählen **Sie überprüfen** neben der URL aus, die Sie gerade geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="ec19f-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="ec19f-166">Eine neue DevTools-Instanz wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ec19f-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a><span data-ttu-id="ec19f-167">Weitere Aktionen: Fokussieren, Aktualisieren oder Schließen einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ec19f-167">More actions: focus, refresh, or close a tab</span></span>  

<span data-ttu-id="ec19f-168">Wählen **Sie Fokusregisterkarte**aus, **laden**oder **schließen** Sie neben der Registerkarte, die Sie fokussieren, aktualisieren oder schließen möchten.</span><span class="sxs-lookup"><span data-stu-id="ec19f-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, refresh, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Die Schaltflächen zum Fokussieren, Aktualisieren oder Schließen einer Registerkarte" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="ec19f-170">Abbildung 4.</span><span class="sxs-lookup"><span data-stu-id="ec19f-170">Figure 4.</span></span>  <span data-ttu-id="ec19f-171">Die Schaltflächen zum Fokussieren, Aktualisieren oder Schließen einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ec19f-171">The buttons for focusing, refreshing, or closing a tab</span></span>  
:::image-end:::  

### <a name="inspect-elements"></a><span data-ttu-id="ec19f-172">Überprüfen von Elementen</span><span class="sxs-lookup"><span data-stu-id="ec19f-172">Inspect elements</span></span>  

<span data-ttu-id="ec19f-173">Navigieren Sie zum **Elementtool** Ihrer DevTools-Instanz, und zeigen Sie auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.</span><span class="sxs-lookup"><span data-stu-id="ec19f-173">Navigate to the **Elements** tool of your DevTools instance, and hover on an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="ec19f-174">Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im Tool **Elemente auszuwählen.**</span><span class="sxs-lookup"><span data-stu-id="ec19f-174">You may also select an element on your Android device screen to select it in the **Elements** tool.</span></span>  <span data-ttu-id="ec19f-175">Wählen **Sie Element** auswählen \( Element auswählen \) in Ihrer DevTools-Instanz aus, und wählen Sie dann das Element auf dem ![ ][ImageSelectElementIcon] Android-Gerätebildschirm aus.</span><span class="sxs-lookup"><span data-stu-id="ec19f-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="ec19f-176">**Select Element** ist nach der ersten Auswahl deaktiviert, daher müssen Sie es jedes Mal erneut aktivieren, wenn Sie das Feature verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ec19f-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <a name="screencast-your-android-screen-to-your-development-machine"></a><span data-ttu-id="ec19f-177">Screencast your Android screen to your development machine</span><span class="sxs-lookup"><span data-stu-id="ec19f-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="ec19f-178">Wählen **Sie Screencast \( Screencast** \) umschalten aus, um den Inhalt Ihres Android-Geräts in Ihrer ![ ][ImageToggleScreencastIcon] DevTools-Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="ec19f-179">Sie können auf folgende Weise mit dem Screencast interagieren.</span><span class="sxs-lookup"><span data-stu-id="ec19f-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="ec19f-180">Auswahlen werden in Tipptasten übersetzt, die richtige Touchereignisse auf dem Gerät abfeuern.</span><span class="sxs-lookup"><span data-stu-id="ec19f-180">Chooses are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="ec19f-181">Tastaturanschläge auf Ihrem Computer werden an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="ec19f-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="ec19f-182">Halten Sie beim Ziehen gedrückt, um eine `Shift` Prisegeste zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="ec19f-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="ec19f-183">Wenn Sie einen Bildlauf durchführen möchten, verwenden Sie das Trackpad oder mausrad oder bewegen Sie sich mit dem Mauszeiger.</span><span class="sxs-lookup"><span data-stu-id="ec19f-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="ec19f-184">Verwenden Sie die folgenden Tipps, um Ihnen beim Screencast zu helfen.</span><span class="sxs-lookup"><span data-stu-id="ec19f-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="ec19f-185">Screencasts zeigen nur Seiteninhalte an.</span><span class="sxs-lookup"><span data-stu-id="ec19f-185">Screencasts only display page content.</span></span>  <span data-ttu-id="ec19f-186">Transparente Teile des Screencasts stellen Geräteschnittstellen dar, z. B. die Microsoft Edge-Adressleiste, die Android-Statusleiste oder die Android-Tastatur.</span><span class="sxs-lookup"><span data-stu-id="ec19f-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="ec19f-187">Screencasts wirken sich negativ auf die Frameraten aus.</span><span class="sxs-lookup"><span data-stu-id="ec19f-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="ec19f-188">Deaktivieren Sie das Screencasting, während Sie Bildlauf oder Animationen messen, um ein genaueres Bild der Leistung Ihrer Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ec19f-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="ec19f-189">Wenn der Bildschirm Ihres Android-Geräts gesperrt wird, wird der Inhalt des Screencasts ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ec19f-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="ec19f-190">Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="ec19f-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ec19f-191">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ec19f-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Konfigurieren von On-Device-Entwickleroptionen | Android Developer"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installieren von OEM-USB-Treibern | Android-Entwickler"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Safari Web Development Tools | Apple Developer"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Debuggen auf mobilen | Unterstützung von Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb – Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevTools-Geräte erkennen gerät nicht, wenn es angeschlossen ist – Stack Overflow"  

> [!NOTE]
> <span data-ttu-id="ec19f-198">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec19f-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ec19f-199">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="ec19f-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ec19f-201">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ec19f-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
