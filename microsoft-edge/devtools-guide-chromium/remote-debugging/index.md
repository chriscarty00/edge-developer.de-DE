---
description: Remotedebuggern von Liveinhalten auf einem Android-Gerät von einem Windows oder macOS-Computer.
title: Erste Schritte mit Remotedebugging von Android-Geräten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d5a5ea8faef40925fb0fb986eb984ac9ae4f051b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565106"
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
# <a name="get-started-with-remote-debugging-android-devices"></a>Erste Schritte mit Remotedebugging von Android-Geräten  

Remotedebuggern von Liveinhalten auf einem Android-Gerät von Ihrem Windows oder macOS-Computer.  Auf der folgenden Lernprogrammseite erfahren Sie, wie Sie die folgenden Aktionen ausführen.  

*   Richten Sie Ihr Android-Gerät für das Remotedebubugen ein, und ermitteln Sie es auf Ihrem Entwicklungscomputer.  
*   Überprüfen und Debuggen von Liveinhalten auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer.  
*   Screencastinhalt von Ihrem Android-Gerät auf eine DevTools-Instanz auf Ihrem Entwicklungscomputer.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Remotedebuding Microsoft Edge App auf iOS-Geräten wird derzeit nicht unterstützt.  Das folgende Handbuch konzentriert sich speziell auf Remotedebug-Microsoft Edge auf Android-Geräten.
> Wenn Sie über ein macOS-Gerät verfügen, befolgen Sie die Anleitung zum Debuggen von [Brightcove,][BrightcoveSupportDebuggingMobileDevices] um die Microsoft Edge auf einem iOS-Gerät mithilfe von Safari remote zu debuggen.  Weitere Informationen zum Web Inspector-Tool in Safari finden Sie unter [Safari Web Development Tools][AppleDeveloperSafariTools].  

## <a name="step-1-discover-your-android-device"></a>Schritt 1: Ermitteln Ihres Android-Geräts  

Der folgende Workflow funktioniert für die meisten Benutzer.  Weitere Hilfe finden Sie unter [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.  

1.  Öffnen Sie **den Bildschirm Entwickleroptionen** auf Ihrem Android.  Weitere Informationen finden Sie unter [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].  
1.  Wählen **Sie USB-Debugging aktivieren aus.**  
1.  Öffnen Sie auf dem Entwicklungscomputer Microsoft Edge.  
1.  Navigieren Sie zur `edge://inspect` Seite in Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Die edge://inspect in Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Abbildung1.  Die `edge://inspect` Seite in Microsoft Edge  
    :::image-end:::  
    
1.  Verbinden Ihr Android-Gerät über ein USB-Kabel direkt an Ihren Entwicklungscomputer senden.  Wenn Sie zum ersten Mal versuchen, eine Verbindung herzustellen, sollte eine Eingabeaufforderung zum Erkennen eines unbekannten Geräts durch DevTools angezeigt werden.  Akzeptieren Sie **die Berechtigungsaufforderung USB-Debugging** zulassen auf Ihrem Android-Gerät.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Die Berechtigungsaufforderung USB-Debugging zulassen auf einem Android-Gerät" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Abbildung2.  Die **Berechtigungsaufforderung USB-Debugging** zulassen auf einem Android-Gerät  
    :::image-end:::  
    
1.  Wenn der Modellname Ihres Android-Geräts angezeigt wird, Microsoft Edge die Verbindung zu Ihrem Gerät erfolgreich hergestellt.  Fahren Sie mit [dem Abschnitt Schritt 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) fort.  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a>Problembehandlung: DevTools erkennt das Android-Gerät nicht  

Verwenden Sie die folgenden Tipps, um Ihnen bei der Problembehandlung der richtigen Einstellungen für Ihre Hardware zu helfen.  

*   Wenn Sie einen USB-Hub verwenden, versuchen Sie, Ihr Android-Gerät direkt mit Ihrem Entwicklungscomputer zu verbinden.  
*   Versuchen Sie, das USB-Kabel zwischen Ihrem Android-Gerät und dem Entwicklungscomputer zu trennen, und schließen Sie das USB-Kabel erneut an.  Führen Sie die Aufgabe aus, während die Bildschirme ihres Android- und Entwicklungscomputers entsperrt sind.  
*   Stellen Sie sicher, dass Das USB-Kabel funktioniert.  Sie sollten Dateien auf Ihrem Android-Gerät von Ihrem Entwicklungscomputer aus überprüfen können.  

Verwenden Sie die folgenden Tipps, um zu überprüfen, ob Ihre Software ordnungsgemäß eingerichtet ist.  

*   Wenn ihr Entwicklungscomputer ausgeführt Windows, versuchen Sie, die USB-Treiber für Ihr Android-Gerät manuell zu installieren.  Weitere Informationen finden Sie unter [Installieren von OEM-USB-Treibern.][AndroidDeveloperToolsOemUsb]  
*   Einige Kombinationen von Windows und Android-Geräten \(insbesondere Samsung\) erfordern zusätzliche Einstellungen.  Weitere Informationen finden Sie unter [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].  

Verwenden Sie die folgenden Tipps, um Probleme zu beheben, wenn die Eingabeaufforderung **USB-Debugging** zulassen nicht auf Ihrem Android-Gerät angezeigt wird.  

*   Trennen Sie die Verbindung, und verbinden Sie das USB-Kabel erneut, während DevTools auf Ihrem Entwicklungscomputer im Fokus steht und Ihr Android-Startbildschirm angezeigt wird.  
    
    > [!NOTE]
    > Die Eingabeaufforderung wird angezeigt, wenn Die Bildschirme ihres Android- oder Entwicklungscomputers gesperrt sind.  

*   Aktualisieren der Anzeigeeinstellungen für Ihr Android-Gerät und Ihren Entwicklungscomputer, sodass sie niemals in den Ruhezustand gehen.  
*   Festlegen des USB-Modus für Android auf PTP.  Weitere Informationen finden Sie unter Navigieren zu [Das Dialogfeld USB-Debuggen][StackexchangeAndroid101933]autorisieren wird nicht angezeigt.  
*   Klicken Sie auf dem **** Bildschirm Entwickleroptionen auf Ihrem Android-Gerät auf Widerrufen von USB-Debuggingautorisierungen, um es auf einen neuen Status zurückzusetzen. ****  

Wenn Sie eine Lösung finden, die auf dieser Seite oder in [DevTools Devices][Stackoverflow21925992] nicht erkannt wird, wenn das Gerät auf Stack Overflow angeschlossen ist, fügen Sie Ihre Lösung der Frage Stack Overflow hinzu.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->.  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a>Schritt 2: Debuggen von Inhalten auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer  

1.  Öffnen Microsoft Edge auf Ihrem Android-Gerät.  
1.  Navigieren Sie `edge://inspect` zu , der Modellname Ihres Android-Geräts wird angezeigt, gefolgt von der Seriennummer des Geräts.  Unten sollte die Version von Microsoft Edge auf dem Gerät ausgeführt werden, mit der Versionsnummer in Klammern angezeigt werden.  Jede geöffnete Microsoft Edge erhält einen eindeutigen Abschnitt.  Sie können über einen Abschnitt mit dieser Registerkarte interagieren.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Ein verbundenes Remotegerät" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Abbildung3.  Ein verbundenes Remotegerät  
    :::image-end:::  
    
1.  Geben Sie **im Textfeld Registerkarte Öffnen** mit URL eine URL ein, und wählen Sie dann Öffnen **aus.**  Die Seite wird auf ihrem Android-Gerät auf einer neuen Registerkarte geöffnet.  
1.  Wählen **Sie überprüfen** neben der URL aus, die Sie gerade geöffnet haben.  Eine neue DevTools-Instanz wird geöffnet.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a>Weitere Aktionen: Fokussieren, Aktualisieren oder Schließen einer Registerkarte  

Wählen **Sie Fokusregisterkarte**aus, **laden**oder **schließen** Sie neben der Registerkarte, die Sie fokussieren, aktualisieren oder schließen möchten.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Die Schaltflächen zum Fokussieren, Aktualisieren oder Schließen einer Registerkarte" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Abbildung 4.  Die Schaltflächen zum Fokussieren, Aktualisieren oder Schließen einer Registerkarte  
:::image-end:::  

### <a name="inspect-elements"></a>Überprüfen von Elementen  

Navigieren Sie zum **Elementtool** Ihrer DevTools-Instanz, und zeigen Sie auf ein Element, um es im Viewport Ihres Android-Geräts zu markieren.  

Sie können auch ein Element auf dem Bildschirm Ihres Android-Geräts auswählen, um es im Tool **Elemente auszuwählen.**  Wählen **Sie Element** auswählen \( Element auswählen \) in Ihrer DevTools-Instanz aus, und wählen Sie dann das Element auf dem ![ ](../media/select-element-icon.msft.png) Android-Gerätebildschirm aus.  

> [!NOTE]
> **Select Element** ist nach der ersten Auswahl deaktiviert, daher müssen Sie es jedes Mal erneut aktivieren, wenn Sie das Feature verwenden möchten.  

### <a name="screencast-your-android-screen-to-your-development-machine"></a>Screencast your Android screen to your development machine  

Wählen **Sie Screencast \( Screencast** \) umschalten aus, um den Inhalt Ihres Android-Geräts in Ihrer ![ ](../media/toggle-screencast-icon.msft.png) DevTools-Instanz anzuzeigen.  

Sie können auf folgende Weise mit dem Screencast interagieren.  

*   Auswahlen werden in Tipptasten übersetzt, die richtige Touchereignisse auf dem Gerät abfeuern.  
*   Tastaturanschläge auf Ihrem Computer werden an das Gerät gesendet.  
*   Halten Sie beim Ziehen gedrückt, um eine `Shift` Prisegeste zu simulieren.  
*   Wenn Sie einen Bildlauf durchführen möchten, verwenden Sie das Trackpad oder mausrad oder bewegen Sie sich mit dem Mauszeiger.

> [!NOTE]
> Verwenden Sie die folgenden Tipps, um Ihnen beim Screencast zu helfen.  
> 
> *   Screencasts zeigen nur Seiteninhalte an.  Transparente Teile des Screencasts stellen Geräteschnittstellen dar, z. B. die Microsoft Edge Adressleiste, die Android-Statusleiste oder die Android-Tastatur.  
> *   Screencasts wirken sich negativ auf die Frameraten aus.  Deaktivieren Sie das Screencasting, während Sie Bildlauf oder Animationen messen, um ein genaueres Bild der Leistung Ihrer Seite zu erhalten.  
> *   Wenn der Bildschirm Ihres Android-Geräts gesperrt wird, wird der Inhalt des Screencasts ausgeblendet.  Entsperren Sie den Bildschirm Ihres Android-Geräts, um den Screencast automatisch fortsetzen zu können.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Konfigurieren von On-Device-Entwickleroptionen | Android Developer"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installieren von OEM-USB-Treibern | Android-Entwickler"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Safari Web Development Tools | Apple Developer"  

[BrightcoveSupportDebuggingMobileDevices]: https://general.support.brightcove.com/developer/debugging-mobile-devices.html "Debuggen auf mobilen | Unterstützung von Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb – Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevTools-Geräte erkennen gerät nicht, wenn es angeschlossen ist – Stack Overflow"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
