---
title: Erste Schritte mit dem Remote Debuggen von Android-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: c77633c4844f0e576b7dff6574000a78c8c083da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708536"
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

# Erste Schritte mit dem Remotedebuggen von Android-Geräten  

Remote Debuggen von Liveinhalten auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus.  Auf der folgenden Lernprogramm Seite Lernen Sie, wie Sie die folgenden Aktionen ausführen.  

*   Richten Sie Ihr Android-Gerät für das Remotedebuggen ein, und entdecken Sie es von Ihrem Entwicklungscomputer.  
*   Überprüfen und Debuggen Sie Liveinhalte auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer.  
*   Screencast-Inhalte von Ihrem Android-Gerät auf eine devtools-Instanz auf Ihrem Entwicklungscomputer.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Remote Debuggen die Microsoft Edge-App auf IOS-Geräten wird derzeit nicht unterstützt.  Das folgende Handbuch ist speziell auf das Remotedebuggen von Microsoft Edge auf Android-Geräten ausgerichtet.
> Wenn Sie über ein macOS-Gerät verfügen, folgen Sie dem [Brightcove-Debugging-Leitfaden][BrightcoveSupportDebuggingMobileDevices] , um Microsoft Edge auf einem IOS-Gerät mithilfe von Safari Remote zu debuggen.  Weitere Informationen zum Tool Web Inspector in Safari finden Sie unter [Safari-Webentwicklungstools][AppleDeveloperSafariTools].  

## Schritt 1: entdecken Ihres Android-Geräts  

Der folgende Workflow funktioniert für die meisten Benutzer.  Weitere Hilfe finden Sie unter [Problembehandlung: devtools erkennt den Abschnitt für Android-Geräte nicht](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Öffnen Sie den Bildschirm " **Entwickler Optionen** " auf Ihrem Android-Gerät.  Weitere Informationen finden Sie unter [Konfigurieren von Optionen für Entwickler auf einem Gerät][AndroidDeveloperStudioDevOptions].  
1.  Wählen Sie **USB-Debugging aktivieren**aus.  
1.  Öffnen Sie auf Ihrem Entwicklungscomputer Microsoft Edge.  
1.  Navigieren Sie zu der `edge://inspect` Seite in Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Die Seite "Edge://Inspect" in Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Abbildung1.  Die `edge://inspect` Seite in Microsoft Edge  
    :::image-end:::  
    
1.  Verbinden Sie Ihr Android-Gerät mit einem USB-Kabel direkt mit Ihrem Entwicklungscomputer.  Wenn Sie das erste Mal eine Verbindung herstellen, sehen Sie in der Regel eine Aufforderung zu devtools, um ein unbekanntes Gerät zu erkennen.  Akzeptieren Sie die Eingabeaufforderung **USB-Debugging-Berechtigung zulassen** auf Ihrem Android-Gerät.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Die Eingabeaufforderung "USB-Debugging-Berechtigung zulassen" auf einem Android-Gerät" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Abbildung2.  Die Eingabeaufforderung " **USB-Debugging-Berechtigung zulassen** " auf einem Android-Gerät  
    :::image-end:::  
    
1.  Wenn der Modellname Ihres Android-Geräts angezeigt wird, hat Microsoft Edge die Verbindung zu Ihrem Gerät erfolgreich hergestellt.  Fahren Sie mit dem Abschnitt [Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) fort.  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### Problembehandlung: devtools erkennt das Android-Gerät nicht.  

Verwenden Sie die folgenden Tipps, um Ihnen bei der Problembehandlung der richtigen Einstellungen für Ihre Hardware zu helfen.  

*   Wenn Sie einen USB-Hub verwenden, versuchen Sie, Ihr Android-Gerät direkt an Ihren Entwicklungscomputer anzuschließen.  
*   Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie dann das USB-Kabel neu an.  Führen Sie die Aufgabe aus, während ihre Android-und Entwicklungscomputer Bildschirme entriegelt sind.  
*   Stellen Sie sicher, dass Ihr USB-Kabel funktioniert.  Sie sollten Dateien auf Ihrem Android-Gerät über Ihren Entwicklungscomputer prüfen können.  

Verwenden Sie die folgenden Tipps, um zu überprüfen, ob die Software ordnungsgemäß eingerichtet ist.  

*   Wenn auf Ihrem Entwicklungscomputer Windows ausgeführt wird, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.  Weitere Informationen finden Sie unter [Installieren von OEM-USB-Treibern][AndroidDeveloperToolsOemUsb].  
*   Einige Kombinationen von Windows-und Android-Geräten \ (insbesondere Samsung \) erfordern zusätzliche Einstellungen.  Weitere Informationen finden Sie unter [devtools Geräte erkennen das Gerät nicht, wenn es angeschlossen][Stackoverflow21925992]ist.  

Verwenden Sie die folgenden Tipps, um Sie bei der Problembehandlung zu unterstützen, wenn Sie die Aufforderung zum **USB-Debugging** auf Ihrem Android-Gerät nicht anzeigen.  

*   Trennen Sie das USB-Kabel, und verbinden Sie es dann erneut, während sich devtools auf Ihrem Entwicklungscomputer befindet und Ihr Android-Homescreen angezeigt wird.  
    
    > [!NOTE]
    > Möglicherweise wird die Eingabeaufforderung nicht angezeigt, wenn Ihre Android-oder Entwicklungscomputer Bildschirme gesperrt sind.  

*   Aktualisieren der Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, damit jeder nie in den Ruhezustand wechselt  
*   Festlegen des USB-Modus für Android auf PTP  Weitere Informationen finden Sie unter [Galaxy S4 zeigt das Dialogfeld Autorisierungs-USB-Debugging nicht][StackexchangeAndroid101933]an.  
*   Wählen Sie auf Ihrem Android-Gerät auf dem Bildschirm **Entwickler Optionen** die Option **USB-Debugging-Berechtigungen widerrufen** aus, um den Status auf "neu" zurückzusetzen.  

Wenn Sie eine Lösung finden, die auf dieser Seite nicht aufgeführt ist, oder wenn in [devtools-Geräten das Gerät nicht erkannt][Stackoverflow21925992] wird, wenn es sich beim Stapelüberlauf befindet, fügen Sie Ihre Lösung zur Stapelüberlauf Frage hinzu.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf dem Entwicklungscomputer  

1.  Öffnen Sie Microsoft Edge auf Ihrem Android-Gerät.  
1.  Auf der `edge://inspect` Seite wird der Modellname Ihres Android-Geräts, gefolgt von der Seriennummer des Geräts, angezeigt.  Darunter sollte die Version von Microsoft Edge auf dem Gerät mit der Versionsnummer in Klammern angezeigt werden.  Auf jeder geöffneten Microsoft Edge-Registerkarte wird ein eindeutiger Abschnitt angezeigt.  Sie können mit dieser Registerkarte in einem Abschnitt interagieren.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Ein verbundenes Remotegerät" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Abbildung3.  Ein verbundenes Remotegerät  
    :::image-end:::  
    
1.  Geben Sie im Textfeld **Tab mit URL öffnen** eine URL ein, und wählen Sie dann **Öffnen**aus.  Die Seite wird in einer neuen Registerkarte auf Ihrem Android-Gerät geöffnet.  
1.  Wählen Sie neben der soeben geöffneten URL über **prüfen** aus.  Eine neue devtools-Instanz wird geöffnet.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### Weitere Aktionen: fokussieren, erneutes Laden oder Schließen einer Registerkarte  

Wählen Sie die **Registerkarte Fokus**, **erneut laden**oder **Schließen** neben der Registerkarte aus, die Sie fokussieren, erneut laden oder schließen möchten.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Die Schaltflächen zum fokussieren, erneuten Laden oder Schließen einer Registerkarte" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Abbildung 4.  Die Schaltflächen zum fokussieren, erneuten Laden oder Schließen einer Registerkarte  
:::image-end:::  

### Überprüfen von Elementen  

Wechseln Sie zum Panel **Elemente** der devtools-Instanz, und zeigen Sie mit der Maus auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.  

Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im **Element** Bereich auszuwählen.  Wählen Sie in ihrer devtools-Instanz **Element** auswählen Element auswählen aus ![ ][ImageSelectElementIcon] , und wählen Sie dann das Element auf dem Bildschirm Ihres Android-Geräts aus.  

> [!NOTE]
> **Element auswählen** ist nach der ersten Auswahl deaktiviert, damit Sie es jedes Mal wieder aktivieren müssen, wenn Sie das Feature verwenden möchten.  

### Screencast Ihres Android-Bildschirms auf Ihrem Entwicklungscomputer  

Wählen Sie **Screencast** Toggle ![ Screencast ][ImageToggleScreencastIcon] -Symbol aus, um den Inhalt Ihres Android-Geräts in ihrer devtools-Instanz anzuzeigen.  

Sie können mit dem Screencast wie folgt interagieren:  

*   Klicks werden in TAPS übersetzt, wobei die richtigen Touch-Ereignisse auf dem Gerät ausgelöst werden.  
*   Tastenanschläge auf dem Computer werden an das Gerät gesendet.  
*   Wenn Sie eine Pinch-Geste simulieren möchten, halten Sie `Shift` beim Ziehen gedrückt.  
*   Verwenden Sie zum Scrollen das Trackpad oder Mausrad, oder werfen Sie den Mauszeiger auf.

> [!NOTE]
> Verwenden Sie die folgenden Tipps, um Ihnen einen Screencast zu ermöglichen.  
> 
> *   Screencasts zeigen nur Seiteninhalte an.  Transparente Abschnitte des Screencasts stellen Geräteschnittstellen dar, beispielsweise die Microsoft Edge-Adressleiste, die Android-Statusleiste oder die Android-Tastatur.  
> *   Screencasts wirken sich negativ auf die Frame-Raten aus.  Deaktivieren Sie das Screencasting beim Messen von Scrolls oder Animationen, um eine genauere Vorstellung von der Leistung Ihrer Seite zu erhalten.  
> *   Wenn Ihr Android-Gerät gesperrt ist, wird der Inhalt Ihres Screencasts nicht mehr angezeigt.  Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortzusetzen.  

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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
