---
title: Emulieren und Testen anderer Browser
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 65ad10ff89d3e4c27abc97cea0eb18b15853dd2e
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607317"
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





# Emulieren und Testen anderer Browser   




Ihr Job endet nicht mit der Sicherstellung, dass Ihre Website über Microsoft Edge und Android hervorragend läuft.  Obwohl der Gerätemodus eine Reihe anderer Geräte wie iPhones simulieren kann, empfehlen wir Ihnen, Lösungen für die Emulation zu finden, die von anderen Browsern bereitgestellt wird.  

### Zusammenfassung  

*   Wenn Sie nicht über ein bestimmtes Gerät verfügen oder eine Stichprobenprüfung durchführen möchten, besteht die beste Möglichkeit darin, das Gerät direkt in Ihrem Browser zu emulieren.  
*   Geräteemulatoren und-Simulatoren ermöglichen Ihnen, ihre Entwicklungswebsite auf einer Reihe von Geräten von Ihrer Arbeitsstation zu imitieren.  
*   Cloud-basierte Emulatoren ermöglichen es Ihnen, Komponententests für Ihre Website auf verschiedenen Plattformen zu automatisieren.  

## Browser Emulatoren  

Browser Emulatoren eignen sich hervorragend zum Testen der Reaktionsfähigkeit einer Website, aber jeder emuliert keine Unterschiede bei der API, der CSS-Unterstützung und bestimmten Verhaltensweisen, die in einem mobilen Browser angezeigt werden.  Testen Sie Ihre Website in Browsern, die auf realen Geräten ausgeführt werden, um sicherzustellen, dass sich alles wie erwartet verhält.  

### Firefox-reaktionsfähige Entwurfsansicht  

Firefox verfügt über eine [reaktionsfähige Entwurfsansicht][MDNResponsiveDesignMode] , die Sie dazu ermutigt, das Denken in Bezug auf bestimmte Geräte zu beenden und stattdessen zu untersuchen, wie sich Ihr Design bei gängigen Bildschirmgrößen oder ihrer eigenen Größe ändert, indem Sie die Ränder ziehen.  

### EdgeHTML-Emulation  

Verwenden Sie zum Emulieren von Windows-Smartphones die [integrierte Emulation][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).  

Verwenden Sie die [IE 11-Emulation][Ie11DevToolsEmulation] , um zu simulieren, wie Ihre Seite in älteren Versionen von Internet Explorer aussehen kann.  

## Geräteemulatoren und-Simulatoren  

Gerätesimulatoren und-Emulatoren simulieren nicht nur die Browserumgebung, sondern das gesamte Gerät.  Alle sind hilfreich, um Dinge zu testen, die die Betriebssystem Integration erfordern, beispielsweise Formulareingaben mit virtuellen Tastaturen.  

### Android-Emulator  

<!--
> ##### Figure old 1  
> Stock Browser in Android Emulator  
> ![Stock Browser in Android Emulator][ImageAndroidEmulatorStockBrowser]  
-->

Derzeit gibt es keine Möglichkeit, Microsoft Edge auf einem Android-Emulator zu installieren.  Sie können jedoch den Android-Browser, die Chrom-Inhalts-Shell und Firefox für Android verwenden, die wir später in diesem Leitfaden überprüfen.  Die Chrom-Inhalts-Shell führt dieselbe Chrom-Rendering-Engine wie Microsoft Edge aus, kommt aber ohne die browserspezifischen Features vor.  

Der Android-Emulator enthält das Android-SDK, das Sie im Rahmen von [Android Studio][AndroidStudioDownload]herunterladen müssen.  Folgen Sie dann den Anweisungen zum [Einrichten eines virtuellen Geräts][AndroidStudioCreateManageVirtualDevices] , und [Starten Sie den Emulator][AndroidStudioRunAppsAndroidEmulator].  
Nachdem Ihr Emulator gestartet wurde, klicken Sie auf das Browser Symbol, und testen Sie Ihre Website auf dem alten Aktien Browser für Android.  

#### Chrom-Inhalts-Shell auf Android  

<!--
> ##### Figure old 2  
> Android Emulator Content Shell  
> ![Android Emulator Content Shell][ImageAndroidEmulatorContentShell]  
-->

Wenn Sie die Chrom-Inhalts-Shell für Android installieren möchten, lassen Sie den Emulator laufen, und führen Sie die folgenden Befehle an einer Eingabeaufforderung aus:  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Nun können Sie Ihre Website mit der Chrom-Inhalts-Shell testen.  

#### Firefox auf Android  

<!--
> ##### Figure old 3  
> Firefox Icon on Android Emulator  
> ![Firefox Icon on Android Emulator][ImageAndroidEmulatorFirefoxBrowser]  
-->

Ähnlich wie bei der Chrom-Inhalts-Shell können Sie eine APK für die Installation von Firefox auf dem Emulator erhalten.  

[Laden Sie die richtige. apk-Datei herunter][MozillaFirefoxDownload].  

Von hier aus können Sie die Datei auf einem geöffneten Emulator oder einem verbundenen Android-Gerät mit dem folgenden Befehl installieren:  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### IOS-Simulator  

Der IOS-Simulator für Mac OS X enthält Xcode, den Sie [aus dem App Store installieren][MacAppStoreXcode].  

Wenn Sie fertig sind, erfahren Sie, wie Sie mit dem Simulator über die [Apple Developer-Dokumentation][AppleSimulatorHelp]arbeiten können.  

> [!NOTE]
> Um zu vermeiden, dass Xcode jedes Mal geöffnet wird, wenn Sie den IOS-Simulator verwenden möchten, öffnen Sie ihn, und klicken Sie dann mit der rechten Maustaste auf das IOS-Simulator-Symbol in Ihrem Dock, und wählen Sie **im Dock beibehalten**aus.  Klicken Sie jetzt einfach auf dieses Symbol, wenn Sie es benötigen.  

###  Microsoft Edge (EdgeHTML)  

> ##### Abbildung1  
> Moderne IE-VM  
> ! [Modern IE VM] [ImageVMModernIe]  

Microsoft Edge \ (EdgeHTML \) Virtual Machines \ (VMS \) ermöglichen Ihnen den Zugriff auf unterschiedliche Versionen von EdgeHTML und IE auf Ihrem Computer über VirtualBox \ (oder VMware \).  Wählen Sie [auf der Download Seite einen virtuellen Computer][MicrosoftDeveloperEdgeVms]aus.  

## Cloud-basierte Emulatoren und Simulatoren  

Wenn Sie nicht in der Lage sind, die Emulatoren zu verwenden und keinen Zugriff auf reale Geräte haben, sind Cloud-basierte Emulatoren die nächstbeste Methode.  Ein großer Vorteil von Cloud-basierten Emulatoren auf realen Geräten und lokalen Emulatoren besteht darin, dass Sie Komponententests für Ihre Website auf verschiedenen Plattformen automatisieren können.  

*   [BrowserStack (kommerziell)][|::ref1::|] ist für manuelle Tests am einfachsten zu verwenden.  Wählen Sie ein Betriebssystem aus, wählen Sie Ihre Browserversion und den Gerätetyp aus, wählen Sie eine URL zum Durchsuchen aus, und es wird ein gehosteter virtueller Computer, mit dem Sie interagieren können, verwendet.  Sie können auch mehrere Emulatoren auf demselben Bildschirm ausführen, sodass Sie das Aussehen und Verhalten Ihrer APP auf mehreren Geräten gleichzeitig testen können.  
*   Mit [SauceLabs (Commercial)][SauceLabs] können Sie Komponententests innerhalb eines Emulators ausführen, was für das Skripting eines Flows über Ihre Website und die anschließende Videoaufzeichnung auf verschiedenen Geräten nützlich sein kann.  Außerdem können Sie mit Ihrer Website manuelle Tests durchführen.  
*   [Device Anywhere (kommerziell)][AppExperience] verwendet keine Emulatoren, sondern echte Geräte, die Sie remote steuern können.  Dies ist sehr nützlich für den Fall, dass Sie ein Problem auf einem bestimmten Gerät reproduzieren müssen und nicht in der Lage sind, den Fehler unter Verwendung einer der Optionen in den vorherigen Leitfäden anzuzeigen.  

 



<!-- image links -->  

<!--[ImageAndroidEmulatorStockBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-emulator-stock-browser.msft.png "Figure old 1: Stock Browser in Android Emulator"  -->  
<!--[ImageAndroidEmulatorContentShell]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-avd-contentshell.msft.png "Figure old 2: Android Emulator Content Shell"  -->  
<!--[ImageAndroidEmulatorFirefoxBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-ff-on-android-emulator.msft.png "Figure old 3: Firefox Icon on Android Emulator"  -->  
[ImageVMModernIe]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Device-mode-modern-IE-VM.msft.png "Abbildung 1: moderne IE-VM"  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML)-Emulation"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emulieren von Browsern, Bildschirmgrößen und GPS-Speicherorten"  

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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate bei Google | Tools, Leistung, Animation, UX \).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
