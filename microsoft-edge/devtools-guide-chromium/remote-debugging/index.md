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
# Erste Schritte mit dem Remote Debuggen von Android-Geräten   



Remote Debuggen von Liveinhalten auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus.  In diesem Lernprogramm lernen Sie, wie Sie:  

*   Richten Sie Ihr Android-Gerät für das Remotedebuggen ein, und entdecken Sie es von Ihrem Entwicklungscomputer.  
*   Überprüfen und Debuggen Sie Liveinhalte auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer.  
*   Screencast-Inhalte von Ihrem Android-Gerät auf eine devtools-Instanz auf Ihrem Entwicklungscomputer.  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## Schritt 1: entdecken Ihres Android-Geräts   

Der folgende Workflow funktioniert für die meisten Benutzer.  Informationen finden Sie unter [Problembehandlung: devtools erkennt das Android-Gerät nicht](#troubleshooting-devtools-is-not-detecting-the-android-device) , um weitere Hilfe zu erhalten.  

1.  Öffnen Sie den Bildschirm " **Entwickler Optionen** " auf Ihrem Android-Gerät.  Weitere Informationen finden Sie unter [Konfigurieren von Optionen für Entwickler auf dem Gerät](https://developer.android.com/studio/debug/dev-options.html).  
1.  Wählen Sie **USB-Debugging aktivieren**aus.  
1.  Öffnen Sie auf Ihrem Entwicklungscomputer Microsoft Edge.  
1.  [Öffnen Sie devtools][DevToolsOpen].  
1.  Wählen Sie in devtools das **Hauptmenü** und `...` dann **Weitere Tools**  >  **Remote Devices**aus.  
    
    > ##### Abbildung1  
    > Öffnen des Reiters " **Remote Devices** " über das **Hauptmenü**  
    > ! [Öffnen der Registerkarte ' Remote Devices ' über das Hauptmenü] [ImageOpenRemoteDevices]  

1.  Öffnen Sie in devtools die Registerkarte **Einstellungen** .  

1.  Stellen Sie sicher, dass das Kontrollkästchen **USB-Geräte entdecken** aktiviert ist.  
    
    > ##### Abbildung2  
    > Das Kontrollkästchen " **USB-Geräte entdecken** " ist aktiviert.  
    > ! [Das Kontrollkästchen USB-Geräte entdecken ist aktiviert] [ImageDiscoverUSBDevices]  

1.  Verbinden Sie Ihr Android-Gerät mit einem USB-Kabel direkt mit Ihrem Entwicklungscomputer.  Wenn Sie dies zum ersten Mal ausführen, sehen Sie in der Regel, dass devtools ein unbekanntes Gerät gefunden hat.  Wenn ein grüner Punkt und der Text unter dem Modellnamen Ihres Android-Geräts **verbunden** sind, hat devtools die Verbindung zu Ihrem Gerät erfolgreich hergestellt.  Fahren Sie mit [Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine)fort.  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  Wenn Ihr Gerät als " **unbekannt**" angezeigt wird, akzeptieren Sie die Eingabeaufforderung " **USB-Debugging-Genehmigung zulassen** " auf Ihrem Android-Gerät.  

### Problembehandlung: devtools erkennt das Android-Gerät nicht.   

Stellen Sie sicher, dass Ihre Hardware richtig eingerichtet ist:  

*   Wenn Sie einen USB-Hub verwenden, sollten Sie stattdessen das Android-Gerät direkt an Ihren Entwicklungscomputer anschließen.  
*   Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie es dann wieder an.  Tun Sie es, während die Bildschirme Ihres Android-und Entwicklungscomputers entriegelt sind.  
*   Stellen Sie sicher, dass Ihr USB-Kabel funktioniert.  Sie sollten Dateien auf Ihrem Android-Gerät über Ihren Entwicklungscomputer prüfen können.  

Stellen Sie sicher, dass Ihre Software richtig eingerichtet ist:  

*   Wenn auf Ihrem Entwicklungscomputer Windows ausgeführt wird, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.  Siehe [Installieren von OEM-USB-Treibern][AndroidUSBDrivers].  
    
*   Einige Kombinationen von Windows-und Android-Geräten (insbesondere Samsung) erfordern eine zusätzliche Einrichtung.  Weitere Informationen finden Sie unter [devtools Devices erkennt Device nicht, wenn es angeschlossen wird] [StackOverflowDevicesNotDetected].  
    
Wenn auf Ihrem Android-Gerät die Eingabeaufforderung **USB-Debugging zulassen** nicht angezeigt wird, versuchen Sie Folgendes:  

*   Trennen Sie das USB-Kabel, und verbinden Sie es dann erneut, während sich devtools auf Ihrem Entwicklungscomputer befindet und Ihr Android-Homescreen angezeigt wird.  Mit anderen Worten: Manchmal wird die Eingabeaufforderung nicht angezeigt, wenn Ihre Android-oder Entwicklungscomputer Bildschirme gesperrt sind.
*   Aktualisieren Sie die Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, damit Sie nie in den Ruhezustand wechseln.  
*   Festlegen des USB-Modus für Android auf PTP  Siehe [Galaxy S4 zeigt das Dialogfeld "Autorisieren von USB-Debuggen" nicht][StackExchangeGalaxyS4DoesNotShowDialogBox]an.  
*   Wählen Sie auf Ihrem Android-Gerät auf dem Bildschirm **Entwickler Optionen** die Option **USB-Debugging-Berechtigungen widerrufen** aus, um den Status auf "neu" zurückzusetzen.  

Wenn Sie eine Lösung finden, die in diesem Abschnitt oder in [devtools Devices Device nicht erkannt wird, wenn Sie angeschlossen sind] [StackOverflowDevicesNotDetected] oder bitte eine Antwort auf diese Stapelüberlauf Frage hinzufügen<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf dem Entwicklungscomputer   

1.  Öffnen Sie Microsoft Edge auf Ihrem Android-Gerät.  

1.  Wählen Sie auf der Registerkarte **Remote Geräte** die Registerkarte aus, die dem Modellnamen Ihres Android-Geräts entspricht.  
    Oben auf dieser Seite sehen Sie den Modellnamen Ihres Android-Geräts, gefolgt von der Seriennummer.  Darunter sollte die Version von Microsoft Edge auf dem Gerät mit der Versionsnummer in Klammern angezeigt werden.  Jede geöffnete Microsoft Edge-Registerkarte erhält einen eigenen Abschnitt.  In diesem Abschnitt können Sie mit dieser Registerkarte interagieren.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  Geben Sie im Textfeld **neue Registerkarte** eine URL ein, und wählen Sie dann **Öffnen**aus.  Die Seite wird in einer neuen Registerkarte auf Ihrem Android-Gerät geöffnet.  

1.  Wählen Sie neben der soeben geöffneten URL über **prüfen** aus.  Eine neue devtools-Instanz wird geöffnet.  Die Version von Microsoft Edge, die auf Ihrem Android-Gerät ausgeführt wird, bestimmt die Version von devtools, die auf Ihrem Entwicklungscomputer geöffnet wird.  
    Wenn auf Ihrem Android-Gerät also eine sehr alte Version von Microsoft Edge ausgeführt wird, sieht die devtools-Instanz möglicherweise sehr unterschiedlich aus, als Sie es gewohnt sind.  

### Weitere Aktionen: Erneutes Laden, fokussieren oder Schließen einer Registerkarte   

Wählen Sie **Weitere Optionen** `...` neben der Registerkarte aus, die Sie erneut laden, fokussieren oder schließen möchten.  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### Überprüfen von Elementen   

Wechseln Sie zum Panel **Elemente** der devtools-Instanz, und zeigen Sie mit der Maus auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.  

Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im **Element** Bereich auszuwählen.  Wählen **Sie Element** ![ ][ImageSelectElementIcon] in ihrer devtools-Instanz auswählen aus, und wählen Sie dann das Element auf dem Bildschirm Ihres Android-Geräts aus.  

> [!NOTE]
> **Element auswählen** ist nach der ersten Auswahl deaktiviert, damit Sie es jedes Mal wieder aktivieren müssen, wenn Sie dieses Feature verwenden möchten.  

### Screencast Ihres Android-Bildschirms auf Ihrem Entwicklungscomputer   

Wählen Sie **Screencast** umschalten ![ Screencast aus ][ImageToggleScreencastIcon] , um den Inhalt Ihres Android-Geräts in ihrer devtools-Instanz anzuzeigen.  

Sie können mit dem Screencast auf verschiedene Arten interagieren:  

*   Klicks werden in TAPS übersetzt, wobei die richtigen Touch-Ereignisse auf dem Gerät ausgelöst werden.  
*   Tastenanschläge auf dem Computer werden an das Gerät gesendet.  
*   Wenn Sie eine Pinch-Geste simulieren möchten, halten Sie `Shift` beim Ziehen gedrückt.  
*   Verwenden Sie zum Scrollen das Trackpad oder Mausrad, oder werfen Sie den Mauszeiger auf.

Einige Hinweise zu Screencasts:  

*   Screencasts zeigen nur Seiteninhalte an.  Transparente Abschnitte des Screencasts stellen Geräteschnittstellen dar, beispielsweise die Microsoft Edge-Adressleiste, die Android-Statusleiste oder die Android-Tastatur.  
*   Screencasts wirken sich negativ auf die Frame-Raten aus.  Deaktivieren Sie das Screencasting beim Messen von Scrolls oder Animationen, um eine genauere Vorstellung von der Leistung Ihrer Seite zu erhalten.  
*   Wenn Ihr Android-Gerät gesperrt ist, wird der Inhalt Ihres Screencasts nicht mehr angezeigt.  Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortzusetzen.  





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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
