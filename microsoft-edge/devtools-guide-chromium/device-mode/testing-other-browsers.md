---
description: Ihre Aufgabe endet nicht mit der Sicherstellung, dass Ihre Website in Microsoft Edge und Android großartig ausgeführt wird.  Auch wenn der Gerätemodus in der Lage ist, eine Reihe anderer Geräte wie iPhones zu simulieren, empfehlen wir Ihnen, Lösungen für die Emulation von anderen Browsern zu prüfen.
title: Emulieren und Testen anderer Browser
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 22153a54df7c5b92236a745be8e3bbac9a52d247
ms.sourcegitcommit: fa8bedfc83fbd1c4ce7bda8c69586c4f24007beb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "11481366"
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
# <a name="emulate-and-test-other-browsers"></a><span data-ttu-id="4c244-105">Emulieren und Testen anderer Browser</span><span class="sxs-lookup"><span data-stu-id="4c244-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="4c244-106">Ihre Aufgabe endet nicht mit der Sicherstellung, dass Ihre Website in Microsoft Edge und Android großartig ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c244-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="4c244-107">Auch wenn der Gerätemodus in der Lage ist, eine Reihe anderer Geräte wie iPhones zu simulieren, empfehlen wir Ihnen, Lösungen für die Emulation von anderen Browsern zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="4c244-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <a name="summary"></a><span data-ttu-id="4c244-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4c244-108">Summary</span></span>  

*   <span data-ttu-id="4c244-109">Wenn Sie nicht über ein bestimmtes Gerät verfügen oder eine Spotüberprüfung für etwas unternehmen möchten, besteht die beste Option darin, das Gerät direkt in Ihrem Browser zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="4c244-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="4c244-110">Mit Geräteemulatoren und Simulatoren können Sie Ihre Entwicklungswebsite auf einer Reihe von Geräten von Ihrer Arbeitsstation nachahmen.</span><span class="sxs-lookup"><span data-stu-id="4c244-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="4c244-111">Mit cloudbasierten Emulatoren können Sie Komponententests für Ihre Website auf verschiedenen Plattformen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="4c244-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <a name="browser-emulators"></a><span data-ttu-id="4c244-112">Browseremulatoren</span><span class="sxs-lookup"><span data-stu-id="4c244-112">Browser emulators</span></span>  

<span data-ttu-id="4c244-113">Browseremulatoren n nen sich gut für das Testen der Reaktionsfähigkeit einer Website n nen, aber jeder emuliert keine Unterschiede in API, CSS-Unterstützung und bestimmten Verhaltensweisen, die in einem mobilen Browser angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c244-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that is displayed on a mobile browser.</span></span>  <span data-ttu-id="4c244-114">Testen Sie Ihre Website auf Browsern, die auf echten Geräten ausgeführt werden, um sicher zu sein, dass sich alles wie erwartet verhält.</span><span class="sxs-lookup"><span data-stu-id="4c244-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <a name="firefox-responsive-design-view"></a><span data-ttu-id="4c244-115">Firefox Responsive Design View</span><span class="sxs-lookup"><span data-stu-id="4c244-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="4c244-116">Firefox verfügt über eine [reaktionsfähige][MDNResponsiveDesignMode] Entwurfsansicht, die Sie ermutigt, nicht mehr an bestimmte Geräte zu denken und stattdessen zu untersuchen, wie sich Ihr Design bei gängigen Bildschirmgrößen oder Ihrer eigenen Größe ändert, indem Sie die Ränder ziehen.</span><span class="sxs-lookup"><span data-stu-id="4c244-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <a name="edgehtml-emulation"></a><span data-ttu-id="4c244-117">EdgeHTML-Emulation</span><span class="sxs-lookup"><span data-stu-id="4c244-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="4c244-118">Verwenden Sie zum Emulieren von Windows Phones [][ArchiveMicrosoftEdgeDevtoolsEmulation]die integrierte Microsoft Edge \(EdgeHTML\)-Emulation.</span><span class="sxs-lookup"><span data-stu-id="4c244-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][ArchiveMicrosoftEdgeDevtoolsEmulation].</span></span>  

<span data-ttu-id="4c244-119">Verwenden [Sie die IE 11-Emulation,][Ie11DevToolsEmulation] um zu simulieren, wie Ihre Seite in älteren Versionen von Internet Explorer aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="4c244-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <a name="device-emulators-and-simulators"></a><span data-ttu-id="4c244-120">Geräteemulatoren und -simulatoren</span><span class="sxs-lookup"><span data-stu-id="4c244-120">Device emulators and simulators</span></span>  

<span data-ttu-id="4c244-121">Gerätesimulatoren und Emulatoren simulieren nicht nur die Browserumgebung, sondern das gesamte Gerät.</span><span class="sxs-lookup"><span data-stu-id="4c244-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="4c244-122">Jede dieser Funktionen ist hilfreich, um Dinge zu testen, die eine Betriebssystemintegration erfordern, z. B. Formulareingaben mit virtuellen Tastaturen.</span><span class="sxs-lookup"><span data-stu-id="4c244-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <a name="android-emulator"></a><span data-ttu-id="4c244-123">Android-Emulator</span><span class="sxs-lookup"><span data-stu-id="4c244-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="4c244-124">Derzeit gibt es keine Möglichkeit, Microsoft Edge auf einem Android-Emulator zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4c244-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="4c244-125">Sie können jedoch den Android-Browser, die Chromium-Inhaltsshell und Firefox für Android verwenden, die wir später in diesem Handbuch lesen.</span><span class="sxs-lookup"><span data-stu-id="4c244-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="4c244-126">Die Chromium-Inhaltsshell führt dasselbe Chromium-Renderingmodul wie Microsoft Edge aus, kommt jedoch ohne browserspezifische Features aus.</span><span class="sxs-lookup"><span data-stu-id="4c244-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="4c244-127">Der Android-Emulator enthält das Android SDK, das Sie als Teil von [Android Studio herunterladen müssen.][AndroidStudioDownload]</span><span class="sxs-lookup"><span data-stu-id="4c244-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="4c244-128">Befolgen Sie dann die Anweisungen, [um ein virtuelles Gerät zu einrichten][AndroidStudioCreateManageVirtualDevices] und den Emulator zu [starten.][AndroidStudioRunAppsAndroidEmulator]</span><span class="sxs-lookup"><span data-stu-id="4c244-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="4c244-129">Nachdem Der Emulator gestartet wurde, wählen Sie das Symbol Browser aus, und testen Sie Ihre Website im alten Stock Browser für Android.</span><span class="sxs-lookup"><span data-stu-id="4c244-129">Once your emulator is booted, choose on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <a name="chromium-content-shell-on-android"></a><span data-ttu-id="4c244-130">Chromium-Inhaltsshell unter Android</span><span class="sxs-lookup"><span data-stu-id="4c244-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="4c244-131">Um die Chromium-Inhaltsshell für Android zu installieren, lassen Sie den Emulator ausgeführt, und führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="4c244-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="4c244-132">Jetzt können Sie Ihre Website mit der Chromium-Inhaltsshell testen.</span><span class="sxs-lookup"><span data-stu-id="4c244-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <a name="firefox-on-android"></a><span data-ttu-id="4c244-133">Firefox unter Android</span><span class="sxs-lookup"><span data-stu-id="4c244-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="4c244-134">Ähnlich wie bei der Chromium-Inhaltsshell können Sie eine APK zum Installieren von Firefox auf dem Emulator erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c244-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="4c244-135">[Laden Sie die richtige .apk-Datei herunter.][MozillaFirefoxDownload]</span><span class="sxs-lookup"><span data-stu-id="4c244-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="4c244-136">Führen Sie den folgenden Befehl aus, um die Datei auf einem geöffneten Emulator oder verbundenen Android-Gerät zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4c244-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a><span data-ttu-id="4c244-137">iOS-Simulator</span><span class="sxs-lookup"><span data-stu-id="4c244-137">iOS simulator</span></span>  

<span data-ttu-id="4c244-138">Der iOS-Simulator für Mac OS X enthält Xcode, den Sie [im App Store installieren.][MacAppStoreXcode]</span><span class="sxs-lookup"><span data-stu-id="4c244-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="4c244-139">Wenn Sie fertig sind, erfahren Sie, wie Sie mit dem Simulator in der [Apple Developer-Dokumentation arbeiten.][AppleSimulatorHelp]</span><span class="sxs-lookup"><span data-stu-id="4c244-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="4c244-140">Um zu vermeiden, dass Xcode jedes Mal geöffnet werden muss, wenn Sie den iOS-Simulator verwenden möchten, öffnen Sie ihn, zeigen Sie auf das iOS-Simulator-Symbol in Ihrem Dock, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **In Dock**halten aus.</span><span class="sxs-lookup"><span data-stu-id="4c244-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, hover on the iOS Simulator icon in your dock, open the contextual menu \(right-click\), and choose **Keep in Dock**.</span></span>  <span data-ttu-id="4c244-141">Wählen Sie jetzt einfach das Symbol aus, wann immer Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="4c244-141">Now just choose the icon whenever you need it.</span></span>  

###  <a name="microsoft-edge-edgehtml"></a><span data-ttu-id="4c244-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4c244-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Moderner IE-VM" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="4c244-144">Moderner IE-VM</span><span class="sxs-lookup"><span data-stu-id="4c244-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="4c244-145">Microsoft Edge \(EdgeHTML\) Virtuelle Computer \(VMs\) ermöglichen Ihnen den Zugriff auf verschiedene Versionen von EdgeHTML und IE auf Ihrem Computer über VirtualBox \(or VMWare\).</span><span class="sxs-lookup"><span data-stu-id="4c244-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="4c244-146">Wählen Sie [auf der Downloadseite einen virtuellen Computer aus.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="4c244-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <a name="cloud-based-emulators-and-simulators"></a><span data-ttu-id="4c244-147">Cloudbasierte Emulatoren und Simulatoren</span><span class="sxs-lookup"><span data-stu-id="4c244-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="4c244-148">Wenn Sie die Emulatoren nicht verwenden können und keinen Zugriff auf echte Geräte haben, sind cloudbasierte Emulatoren das nächste Beste.</span><span class="sxs-lookup"><span data-stu-id="4c244-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="4c244-149">Ein großer Vorteil cloudbasierter Emulatoren gegenüber echten Geräten und lokalen Emulatoren besteht in der Möglichkeit, Komponententests für Ihre Website auf verschiedenen Plattformen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="4c244-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="4c244-150">[BrowserStack (kommerziell)][|::ref1::|] ist am einfachsten für manuelle Tests zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c244-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="4c244-151">Sie wählen ein Betriebssystem aus, wählen Die Browserversion und den Gerätetyp aus, wählen eine ZU durchsuchende URL aus, und es wird ein gehosteter virtueller Computer, mit dem Sie interagieren können, hochgedreht.</span><span class="sxs-lookup"><span data-stu-id="4c244-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="4c244-152">Sie können auch mehrere Emulatoren auf demselben Bildschirm ausführen, sodass Sie das Aussehen und Gefühl Ihrer App auf mehreren Geräten gleichzeitig testen können.</span><span class="sxs-lookup"><span data-stu-id="4c244-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="4c244-153">[Mit "SauceLabs" (kommerziell)][SauceLabs] können Sie Komponententests innerhalb eines Emulators ausführen. Dies kann sehr nützlich sein, um einen Fluss durch Ihre Website zu schreiben und die Videoaufzeichnung danach auf verschiedenen Geräten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="4c244-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="4c244-154">Sie können auch manuelle Tests mit Ihrer Website durchführen.</span><span class="sxs-lookup"><span data-stu-id="4c244-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="4c244-155">[Device Anywhere (kommerziell)][AppExperience] verwendet keine Emulatoren, sondern echte Geräte, die Sie remote steuern können.</span><span class="sxs-lookup"><span data-stu-id="4c244-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="4c244-156">Dies ist sehr nützlich, wenn Sie ein Problem auf einem bestimmten Gerät reproduzieren müssen und den Fehler möglicherweise nicht mithilfe einer der Optionen in den vorherigen Anleitungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4c244-156">This is very useful in the event where you need to reproduce a problem on a specific device and may not display the bug using any of the options in the previous guides.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4c244-157">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="4c244-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[ArchiveMicrosoftEdgeDevtoolsEmulation]: /archive/microsoft-edge/legacy/developer/devtools-guide/emulation "Emulations-| Microsoft Docs"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emulieren von Browsern, Bildschirmgrößen und GPS-| Microsoft Docs"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Herunterladen virtueller Computer"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Erstellen und Verwalten von virtuellen | Android-Entwickler"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Herunterladen von Android Studio- und SDK-Tools | Android-Entwickler"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Ausführen von Apps auf dem Android-Emulator | Android-Entwickler"  

[AppExperience]: https://www.sigos.com/app-experience/ "App-Erfahrung"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Simulatorhilfe – aktuelle | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode im Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Responsive Design Mode | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Herunterladen des Firefox-Browsers"  
[SauceLabs]: https://saucelabs.com "Sauce Labs"  

> [!NOTE]
> <span data-ttu-id="4c244-171">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c244-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4c244-172">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate bei Google | Tools, Performance, Animation, UX\).</span><span class="sxs-lookup"><span data-stu-id="4c244-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4c244-174">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c244-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
