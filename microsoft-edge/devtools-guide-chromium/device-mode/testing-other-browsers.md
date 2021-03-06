---
description: Ihre Aufgabe endet nicht mit der Sicherstellung, dass Ihre Website in Microsoft Edge und Android großartig ausgeführt wird.  Auch wenn der Gerätemodus in der Lage ist, eine Reihe anderer Geräte wie iPhones zu simulieren, empfehlen wir Ihnen, Lösungen für die Emulation von anderen Browsern zu prüfen.
title: Emulieren und Testen anderer Browser
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 6b1239db373bd13d798ac90ac47a10878d07cdcb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398686"
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

# <a name="emulate-and-test-other-browsers"></a>Emulieren und Testen anderer Browser  

Ihre Aufgabe endet nicht mit der Sicherstellung, dass Ihre Website in Microsoft Edge und Android großartig ausgeführt wird.  Auch wenn der Gerätemodus in der Lage ist, eine Reihe anderer Geräte wie iPhones zu simulieren, empfehlen wir Ihnen, Lösungen für die Emulation von anderen Browsern zu prüfen.  

### <a name="summary"></a>Zusammenfassung  

*   Wenn Sie nicht über ein bestimmtes Gerät verfügen oder eine Spotüberprüfung für etwas unternehmen möchten, besteht die beste Option darin, das Gerät direkt in Ihrem Browser zu emulieren.  
*   Mit Geräteemulatoren und Simulatoren können Sie Ihre Entwicklungswebsite auf einer Reihe von Geräten von Ihrer Arbeitsstation nachahmen.  
*   Mit cloudbasierten Emulatoren können Sie Komponententests für Ihre Website auf verschiedenen Plattformen automatisieren.  

## <a name="browser-emulators"></a>Browseremulatoren  

Browseremulatoren n nen sich gut für das Testen der Reaktionsfähigkeit einer Website n nen, aber jeder emuliert keine Unterschiede in API, CSS-Unterstützung und bestimmten Verhaltensweisen, die in einem mobilen Browser angezeigt werden.  Testen Sie Ihre Website auf Browsern, die auf echten Geräten ausgeführt werden, um sicher zu sein, dass sich alles wie erwartet verhält.  

### <a name="firefox-responsive-design-view"></a>Firefox Responsive Design View  

Firefox verfügt über eine [reaktionsfähige][MDNResponsiveDesignMode] Entwurfsansicht, die Sie ermutigt, nicht mehr an bestimmte Geräte zu denken und stattdessen zu untersuchen, wie sich Ihr Design bei gängigen Bildschirmgrößen oder Ihrer eigenen Größe ändert, indem Sie die Ränder ziehen.  

### <a name="edgehtml-emulation"></a>EdgeHTML-Emulation  

Verwenden Sie zum Emulieren von Windows Phones [][DevToolsEdgeHtmlEmulation]die integrierte Microsoft Edge \(EdgeHTML\)-Emulation.  

Verwenden [Sie die IE 11-Emulation,][Ie11DevToolsEmulation] um zu simulieren, wie Ihre Seite in älteren Versionen von Internet Explorer aussehen kann.  

## <a name="device-emulators-and-simulators"></a>Geräteemulatoren und -simulatoren  

Gerätesimulatoren und Emulatoren simulieren nicht nur die Browserumgebung, sondern das gesamte Gerät.  Jede dieser Funktionen ist hilfreich, um Dinge zu testen, die eine Betriebssystemintegration erfordern, z. B. Formulareingaben mit virtuellen Tastaturen.  

### <a name="android-emulator"></a>Android-Emulator  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

Derzeit gibt es keine Möglichkeit, Microsoft Edge auf einem Android-Emulator zu installieren.  Sie können jedoch den Android-Browser, die Chromium-Inhaltsshell und Firefox für Android verwenden, die wir später in diesem Handbuch lesen.  Die Chromium-Inhaltsshell führt dasselbe Chromium-Renderingmodul wie Microsoft Edge aus, kommt jedoch ohne browserspezifische Features aus.  

Der Android-Emulator enthält das Android SDK, das Sie als Teil von [Android Studio herunterladen müssen.][AndroidStudioDownload]  Befolgen Sie dann die Anweisungen, [um ein virtuelles Gerät zu einrichten][AndroidStudioCreateManageVirtualDevices] und den Emulator zu [starten.][AndroidStudioRunAppsAndroidEmulator]  
Nachdem Der Emulator gestartet wurde, wählen Sie das Symbol Browser aus, und testen Sie Ihre Website im alten Stock Browser für Android.  

#### <a name="chromium-content-shell-on-android"></a>Chromium-Inhaltsshell unter Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Um die Chromium-Inhaltsshell für Android zu installieren, lassen Sie den Emulator ausgeführt, und führen Sie den folgenden Befehl aus.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Jetzt können Sie Ihre Website mit der Chromium-Inhaltsshell testen.  

#### <a name="firefox-on-android"></a>Firefox unter Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Ähnlich wie bei der Chromium-Inhaltsshell können Sie eine APK zum Installieren von Firefox auf dem Emulator erhalten.  

[Laden Sie die richtige .apk-Datei herunter.][MozillaFirefoxDownload]  

Führen Sie den folgenden Befehl aus, um die Datei auf einem geöffneten Emulator oder verbundenen Android-Gerät zu installieren.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a>iOS-Simulator  

Der iOS-Simulator für Mac OS X enthält Xcode, den Sie [im App Store installieren.][MacAppStoreXcode]  

Wenn Sie fertig sind, erfahren Sie, wie Sie mit dem Simulator in der [Apple Developer-Dokumentation arbeiten.][AppleSimulatorHelp]  

> [!NOTE]
> Um zu vermeiden, dass Xcode jedes Mal geöffnet werden muss, wenn Sie den iOS-Simulator verwenden möchten, öffnen Sie ihn, zeigen Sie auf das iOS-Simulator-Symbol in Ihrem Dock, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **In Dock**halten aus.  Wählen Sie jetzt einfach das Symbol aus, wann immer Sie es benötigen.  

###  <a name="microsoft-edge-edgehtml"></a>Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Moderner IE-VM" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   Moderner IE-VM  
:::image-end:::  

Microsoft Edge \(EdgeHTML\) Virtuelle Computer \(VMs\) ermöglichen Ihnen den Zugriff auf verschiedene Versionen von EdgeHTML und IE auf Ihrem Computer über VirtualBox \(or VMWare\).  Wählen Sie [auf der Downloadseite einen virtuellen Computer aus.][MicrosoftDeveloperEdgeVms]  

## <a name="cloud-based-emulators-and-simulators"></a>Cloudbasierte Emulatoren und Simulatoren  

Wenn Sie die Emulatoren nicht verwenden können und keinen Zugriff auf echte Geräte haben, sind cloudbasierte Emulatoren das nächste Beste.  Ein großer Vorteil cloudbasierter Emulatoren gegenüber echten Geräten und lokalen Emulatoren besteht in der Möglichkeit, Komponententests für Ihre Website auf verschiedenen Plattformen zu automatisieren.  

*   [BrowserStack (kommerziell)][|::ref1::|] ist am einfachsten für manuelle Tests zu verwenden.  Sie wählen ein Betriebssystem aus, wählen Die Browserversion und den Gerätetyp aus, wählen eine ZU durchsuchende URL aus, und es wird ein gehosteter virtueller Computer, mit dem Sie interagieren können, hochgedreht.  Sie können auch mehrere Emulatoren auf demselben Bildschirm ausführen, sodass Sie das Aussehen und Gefühl Ihrer App auf mehreren Geräten gleichzeitig testen können.  
*   [Mit "SauceLabs" (kommerziell)][SauceLabs] können Sie Komponententests innerhalb eines Emulators ausführen. Dies kann sehr nützlich sein, um einen Fluss durch Ihre Website zu schreiben und die Videoaufzeichnung danach auf verschiedenen Geräten zu sehen.  Sie können auch manuelle Tests mit Ihrer Website durchführen.  
*   [Device Anywhere (kommerziell)][AppExperience] verwendet keine Emulatoren, sondern echte Geräte, die Sie remote steuern können.  Dies ist sehr nützlich, wenn Sie ein Problem auf einem bestimmten Gerät reproduzieren müssen und den Fehler möglicherweise nicht mithilfe einer der Optionen in den vorherigen Anleitungen anzeigen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML) – Emulations-| Microsoft Docs"  

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
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate bei Google | Tools, Performance, Animation, UX\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
