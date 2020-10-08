---
description: Ihr Job endet nicht mit der Sicherstellung, dass Ihre Website über Microsoft Edge und Android hervorragend läuft.  Obwohl der Gerätemodus eine Reihe anderer Geräte wie iPhones simulieren kann, empfehlen wir Ihnen, Lösungen für die Emulation zu finden, die von anderen Browsern bereitgestellt wird.
title: Emulieren und Testen anderer Browser
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1b76447aa86837abac88bc4727eb7f4ee082342a
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992911"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="214e7-105">Emulieren und Testen anderer Browser</span><span class="sxs-lookup"><span data-stu-id="214e7-105">Emulate and test other browsers</span></span>   




<span data-ttu-id="214e7-106">Ihr Job endet nicht mit der Sicherstellung, dass Ihre Website über Microsoft Edge und Android hervorragend läuft.</span><span class="sxs-lookup"><span data-stu-id="214e7-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="214e7-107">Obwohl der Gerätemodus eine Reihe anderer Geräte wie iPhones simulieren kann, empfehlen wir Ihnen, Lösungen für die Emulation zu finden, die von anderen Browsern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="214e7-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="214e7-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="214e7-108">Summary</span></span>  

*   <span data-ttu-id="214e7-109">Wenn Sie nicht über ein bestimmtes Gerät verfügen oder eine Stichprobenprüfung durchführen möchten, besteht die beste Möglichkeit darin, das Gerät direkt in Ihrem Browser zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="214e7-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="214e7-110">Geräteemulatoren und-Simulatoren ermöglichen Ihnen, ihre Entwicklungswebsite auf einer Reihe von Geräten von Ihrer Arbeitsstation zu imitieren.</span><span class="sxs-lookup"><span data-stu-id="214e7-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="214e7-111">Cloud-basierte Emulatoren ermöglichen es Ihnen, Komponententests für Ihre Website auf verschiedenen Plattformen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="214e7-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="214e7-112">Browser Emulatoren</span><span class="sxs-lookup"><span data-stu-id="214e7-112">Browser emulators</span></span>  

<span data-ttu-id="214e7-113">Browser Emulatoren eignen sich hervorragend zum Testen der Reaktionsfähigkeit einer Website, aber jeder emuliert keine Unterschiede bei der API, der CSS-Unterstützung und bestimmten Verhaltensweisen, die in einem mobilen Browser angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="214e7-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="214e7-114">Testen Sie Ihre Website in Browsern, die auf realen Geräten ausgeführt werden, um sicherzustellen, dass sich alles wie erwartet verhält.</span><span class="sxs-lookup"><span data-stu-id="214e7-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="214e7-115">Firefox-reaktionsfähige Entwurfsansicht</span><span class="sxs-lookup"><span data-stu-id="214e7-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="214e7-116">Firefox verfügt über eine [reaktionsfähige Entwurfsansicht][MDNResponsiveDesignMode] , die Sie dazu ermutigt, das Denken in Bezug auf bestimmte Geräte zu beenden und stattdessen zu untersuchen, wie sich Ihr Design bei gängigen Bildschirmgrößen oder ihrer eigenen Größe ändert, indem Sie die Ränder ziehen.</span><span class="sxs-lookup"><span data-stu-id="214e7-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="214e7-117">EdgeHTML-Emulation</span><span class="sxs-lookup"><span data-stu-id="214e7-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="214e7-118">Verwenden Sie zum Emulieren von Windows-Smartphones die [integrierte Emulation][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="214e7-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="214e7-119">Verwenden Sie die [IE 11-Emulation][Ie11DevToolsEmulation] , um zu simulieren, wie Ihre Seite in älteren Versionen von Internet Explorer aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="214e7-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="214e7-120">Geräteemulatoren und-Simulatoren</span><span class="sxs-lookup"><span data-stu-id="214e7-120">Device emulators and simulators</span></span>  

<span data-ttu-id="214e7-121">Gerätesimulatoren und-Emulatoren simulieren nicht nur die Browserumgebung, sondern das gesamte Gerät.</span><span class="sxs-lookup"><span data-stu-id="214e7-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="214e7-122">Alle sind hilfreich, um Dinge zu testen, die die Betriebssystem Integration erfordern, beispielsweise Formulareingaben mit virtuellen Tastaturen.</span><span class="sxs-lookup"><span data-stu-id="214e7-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="214e7-123">Android-Emulator</span><span class="sxs-lookup"><span data-stu-id="214e7-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="214e7-124">Derzeit gibt es keine Möglichkeit, Microsoft Edge auf einem Android-Emulator zu installieren.</span><span class="sxs-lookup"><span data-stu-id="214e7-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="214e7-125">Sie können jedoch den Android-Browser, die Chrom-Inhalts-Shell und Firefox für Android verwenden, die wir später in diesem Leitfaden überprüfen.</span><span class="sxs-lookup"><span data-stu-id="214e7-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="214e7-126">Die Chrom-Inhalts-Shell führt dieselbe Chrom-Rendering-Engine wie Microsoft Edge aus, kommt aber ohne die browserspezifischen Features vor.</span><span class="sxs-lookup"><span data-stu-id="214e7-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="214e7-127">Der Android-Emulator enthält das Android-SDK, das Sie im Rahmen von [Android Studio][AndroidStudioDownload]herunterladen müssen.</span><span class="sxs-lookup"><span data-stu-id="214e7-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="214e7-128">Folgen Sie dann den Anweisungen zum [Einrichten eines virtuellen Geräts][AndroidStudioCreateManageVirtualDevices] , und [Starten Sie den Emulator][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="214e7-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="214e7-129">Nachdem Ihr Emulator gestartet wurde, klicken Sie auf das Browser Symbol, und testen Sie Ihre Website auf dem alten Aktien Browser für Android.</span><span class="sxs-lookup"><span data-stu-id="214e7-129">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="214e7-130">Chrom-Inhalts-Shell auf Android</span><span class="sxs-lookup"><span data-stu-id="214e7-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="214e7-131">Wenn Sie die Chrom-Inhalts-Shell für Android installieren möchten, lassen Sie den Emulator laufen, und führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="214e7-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="214e7-132">Nun können Sie Ihre Website mit der Chrom-Inhalts-Shell testen.</span><span class="sxs-lookup"><span data-stu-id="214e7-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="214e7-133">Firefox auf Android</span><span class="sxs-lookup"><span data-stu-id="214e7-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="214e7-134">Ähnlich wie bei der Chrom-Inhalts-Shell können Sie eine APK für die Installation von Firefox auf dem Emulator erhalten.</span><span class="sxs-lookup"><span data-stu-id="214e7-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="214e7-135">[Laden Sie die richtige. apk-Datei herunter][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="214e7-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="214e7-136">Führen Sie den folgenden Befehl aus, um die Datei auf einem geöffneten Emulator oder einem verbundenen Android-Gerät zu installieren.</span><span class="sxs-lookup"><span data-stu-id="214e7-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="214e7-137">IOS-Simulator</span><span class="sxs-lookup"><span data-stu-id="214e7-137">iOS simulator</span></span>  

<span data-ttu-id="214e7-138">Der IOS-Simulator für Mac OS X enthält Xcode, den Sie [aus dem App Store installieren][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="214e7-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="214e7-139">Wenn Sie fertig sind, erfahren Sie, wie Sie mit dem Simulator über die [Apple Developer-Dokumentation][AppleSimulatorHelp]arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="214e7-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="214e7-140">Um zu vermeiden, dass Xcode jedes Mal geöffnet wird, wenn Sie den IOS-Simulator verwenden möchten, öffnen Sie ihn, und klicken Sie dann mit der rechten Maustaste auf das IOS-Simulator-Symbol in Ihrem Dock, und wählen Sie **im Dock beibehalten**aus.</span><span class="sxs-lookup"><span data-stu-id="214e7-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and select **Keep in Dock**.</span></span>  <span data-ttu-id="214e7-141">Klicken Sie jetzt einfach auf dieses Symbol, wenn Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="214e7-141">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="214e7-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="214e7-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="214e7-144">Moderne IE-VM</span><span class="sxs-lookup"><span data-stu-id="214e7-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="214e7-145">Microsoft Edge \ (EdgeHTML \) Virtual Machines \ (VMS \) ermöglichen Ihnen den Zugriff auf unterschiedliche Versionen von EdgeHTML und IE auf Ihrem Computer über VirtualBox \ (oder VMware \).</span><span class="sxs-lookup"><span data-stu-id="214e7-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="214e7-146">Wählen Sie [auf der Download Seite einen virtuellen Computer][MicrosoftDeveloperEdgeVms]aus.</span><span class="sxs-lookup"><span data-stu-id="214e7-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="214e7-147">Cloud-basierte Emulatoren und Simulatoren</span><span class="sxs-lookup"><span data-stu-id="214e7-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="214e7-148">Wenn Sie nicht in der Lage sind, die Emulatoren zu verwenden und keinen Zugriff auf reale Geräte haben, sind Cloud-basierte Emulatoren die nächstbeste Methode.</span><span class="sxs-lookup"><span data-stu-id="214e7-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="214e7-149">Ein großer Vorteil von Cloud-basierten Emulatoren auf realen Geräten und lokalen Emulatoren besteht darin, dass Sie Komponententests für Ihre Website auf verschiedenen Plattformen automatisieren können.</span><span class="sxs-lookup"><span data-stu-id="214e7-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="214e7-150">[BrowserStack (kommerziell)][|::ref1::|] ist für manuelle Tests am einfachsten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="214e7-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="214e7-151">Wählen Sie ein Betriebssystem aus, wählen Sie Ihre Browserversion und den Gerätetyp aus, wählen Sie eine URL zum Durchsuchen aus, und es wird ein gehosteter virtueller Computer, mit dem Sie interagieren können, verwendet.</span><span class="sxs-lookup"><span data-stu-id="214e7-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="214e7-152">Sie können auch mehrere Emulatoren auf demselben Bildschirm ausführen, sodass Sie das Aussehen und Verhalten Ihrer APP auf mehreren Geräten gleichzeitig testen können.</span><span class="sxs-lookup"><span data-stu-id="214e7-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="214e7-153">Mit [SauceLabs (Commercial)][SauceLabs] können Sie Komponententests innerhalb eines Emulators ausführen, was für das Skripting eines Flows über Ihre Website und die anschließende Videoaufzeichnung auf verschiedenen Geräten nützlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="214e7-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="214e7-154">Außerdem können Sie mit Ihrer Website manuelle Tests durchführen.</span><span class="sxs-lookup"><span data-stu-id="214e7-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="214e7-155">[Device Anywhere (kommerziell)][AppExperience] verwendet keine Emulatoren, sondern echte Geräte, die Sie remote steuern können.</span><span class="sxs-lookup"><span data-stu-id="214e7-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="214e7-156">Dies ist sehr nützlich für den Fall, dass Sie ein Problem auf einem bestimmten Gerät reproduzieren müssen und nicht in der Lage sind, den Fehler unter Verwendung einer der Optionen in den vorherigen Leitfäden anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="214e7-156">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

<!--  
 


-->  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML)-Emulation | Microsoft docs"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emulieren von Browsern, Bildschirmgrößen und GPS-Speicherorten | Microsoft docs"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Herunterladen virtueller Computer"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Erstellen und Verwalten von virtuellen Geräten | Android-Entwickler"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Android Studio-und SDK-Tools herunterladen | Android-Entwickler"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Ausführen von apps auf dem Android-Emulator | Android-Entwickler"  

[AppExperience]: https://www.sigos.com/app-experience/ "App-Erfahrung"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Simulator-Hilfe-aktuell | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode im Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Reaktionsfähiger Entwurfsmodus | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Herunterladen des Firefox-Browsers"  
[SauceLabs]: https://saucelabs.com "Sauce Labs"  

> [!NOTE]
> <span data-ttu-id="214e7-170">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="214e7-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="214e7-171">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate bei Google | Tools, Leistung, Animation, UX \).</span><span class="sxs-lookup"><span data-stu-id="214e7-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="214e7-173">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="214e7-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
