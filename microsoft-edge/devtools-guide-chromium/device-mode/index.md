---
title: Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607426"
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





# Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools   

  

Verwenden Sie den Gerätemodus, um zu sehen, wie Ihre Seite auf einem mobilen Gerät aussieht und ausgeführt wird.  

Der Gerätemodus ist der Name für die lose Sammlung von Features in Microsoft Edge devtools, mit denen Sie mobile Geräte simulieren können.  Verfügbare Features:  

*   [Simulieren eines mobilen Viewports](#simulate-a-mobile-viewport)  
*   [Einschränken des Netzwerks](#throttle-the-network-only)  
*   [Drosseln der CPU](#throttle-the-cpu-only)  
*   [Simulieren von geolokationen](#override-geolocation)  
*   [Festlegen der Ausrichtung](#set-orientation)  

## Einschränkungen   

Denken Sie an den Gerätemodus als Näherungswert für die [erste Reihenfolge][WikiApproximation] , wie Ihre Seite auf einem mobilen Gerät aussieht und sich anfühlt.  Mit dem Gerätemodus führen Sie Ihren Code nicht auf einem mobilen Gerät aus.  Sie simulieren die mobile Benutzeroberfläche auf Ihrem Laptop oder Desktop.  

Es gibt einige Aspekte von mobilen Geräten, die von devtools niemals simuliert werden können.  Die Architektur von mobilen CPUs unterscheidet sich beispielsweise von der Architektur von Laptop-oder Desktop-CPUs.  Im Zweifelsfall ist es am besten, wenn Sie Ihre Seite auf einem mobilen Gerät ausführen.  Verwenden Sie [Remote Debuggen] [DevToolsRemoteDebugging], um den Code einer Seite von Ihrem Laptop oder Desktop aus anzuzeigen, zu ändern, zu Debuggen und zu profilieren, während Sie auf einem mobilen Gerät ausgeführt wird.  

## Simulieren eines mobilen Viewports   

Klicken Sie auf **Geräte** Symbolleiste Umschalten auf Geräte ![ Symbolleiste ][ImageDeviceToolbarIcon] , um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.  

> ##### Abbildung1  
> Die Gerätesymbolleiste  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar]  

Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.  

### Reaktionsfähiger viewportmodus   

Ziehen Sie die Ziehpunkte, um die Größe des Viewports auf die gewünschten Bemaßungen zu ändern.  Oder geben Sie bestimmte Werte in die Felder Breite und Höhe ein.  In [Abbildung 2](#figure-2)ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .  

> ##### Abbildung2  
> Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus  
> ![Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus][ImageResponsiveHandles]  

#### Anzeigen von medienabfragen   

Wenn Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen möchten, klicken Sie auf **Weitere Optionen** , und wählen Sie dann **medienabfragen anzeigen**aus.  

> ##### Abbildung 3  
> Anzeigen von medienabfragen  
> ![Anzeigen von medienabfragen][ImageShowMediaQueries]  

Klicken Sie auf einen Haltepunkt, um die Breite des Viewports so zu ändern, dass der Haltepunkt ausgelöst wird.  

> ##### Abbildung4  
> Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.  
> ![Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.][ImageBreakpoint]  

#### Einrichten des Gerätetyps   

Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.  

> ##### Abbildung5  
> Liste der **Gerätetypen**  
> ![Liste der Gerätetypen][ImageDeviceType]  

In der nachstehenden Tabelle werden die Unterschiede zwischen den Optionen beschrieben.  Die **Rendering-Methode** bezieht sich darauf, ob Microsoft Edge die Seite als mobiles oder Desktop-Viewport rendert.  Das **Cursor Symbol** bezieht sich auf den Typ des Cursors, den Sie sehen, wenn Sie auf die Seite zeigen.  **Ausgelöste Ereignisse** bezieht sich darauf, ob die Seite ausgelöst `touch` wird, oder `click` Ereignisse, wenn Sie mit der Seite interagieren.  

| Option | Rendering-Methode | Cursor Symbol | Ausgelöste Ereignisse |  
|:--- |:--- |:--- |:--- |  
| Mobilgeräte | Mobilgeräte | Kreis | Toucheingabe |  
| Mobil \ (kein Touch \) | Mobilgeräte | Normal |  auf  |  
| Desktop | Desktop | Normal |  auf  |  
| Desktop \ (tippen Sie auf \) | Desktop | Kreis | Toucheingabe |  

> [!NOTE]
> Wenn die Liste **Gerätetyp** nicht angezeigt wird, klicken Sie auf **Weitere Optionen** , und wählen Sie **Gerätetyp hinzufügen**aus.  

### Ansichtsfenster Modus für mobile Geräte   

Wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren möchten, wählen Sie das Gerät in der **Geräte** Liste aus.  

> ##### Abbildung6  
> Geräteliste  
> ![Geräteliste][ImageDeviceList]  

#### Drehen des Viewports in Querformat   

Klicken **Sie auf Drehung drehen** ![ ][ImageRotateIcon] , um das Ansichtsfenster in Querformat zu drehen.  

> ##### Abbildung7  
> Querformat  
> ![Querformat][ImageLandscape]  

> [!NOTE]
> Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.  

> ##### Abbildung8  
> Die Gerätesymbolleiste  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar2]  

Siehe auch [Ausrichtung einstellen](#set-orientation).  

#### Geräterahmen anzeigen   

Wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie ein iPhone 6 simulieren, öffnen Sie **Weitere Optionen** , und wählen Sie dann **Geräterahmen anzeigen** aus, um den Frame des physikalischen Geräts um den Viewport anzuzeigen.  

> [!NOTE]
> Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies wahrscheinlich, dass devtools gerade keine Grafiken für diese bestimmte Option hat.  

> ##### Abbildung 9  
> Geräterahmen anzeigen  
> ![Geräterahmen anzeigen][ImageShowDeviceFrame]  

> ##### Abbildung 10  
> Der Geräterahmen für das iPhone 6  
> ![Der Geräterahmen für das iPhone 6][ImageIphoneFrame]  

#### Hinzufügen eines benutzerdefinierten mobilen Geräts   

So fügen Sie ein benutzerdefiniertes Gerät hinzu:  

1.  Klicken Sie auf die **Geräte** Liste, und wählen Sie dann **Bearbeiten**aus.  

> ##### Abbildung 11  
> Auswählen **von "Bearbeiten"** 
> ![ Auswählen von "Bearbeiten"][ImageEdit]  

1.  Klicken Sie auf **Benutzerdefiniertes Gerät hinzufügen**.  

1.  Geben Sie einen Namen, eine Breite und eine Höhe für das Gerät ein.  Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.  Das Feld "Gerätetyp" ist die Liste, die standardmäßig auf " **Mobiltelefon** " festgesetzt ist.  

> ##### Abbildung 12  
> Erstellen eines benutzerdefinierten Geräts  
> ![Erstellen eines benutzerdefinierten Geräts][ImageAddCustomDevice]  

### Lineale anzeigen   

Klicken Sie auf **Weitere Optionen** , und wählen Sie dann **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.  Die Größeneinheit der Lineale ist Pixel.  

> ##### Abbildung 13  
> Lineale anzeigen  
> ![Lineale anzeigen][ImageShowRulers]  

> ##### Abbildung 14  
> Lineale oberhalb und Links des Viewports  
> ![Lineale oberhalb und Links des Viewports][ImageRulers]  

### Zoomen des Viewports   

Verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.  

> ##### Abbildung 15  
> Zoom  
> ![Zoom][ImageZoomViewport]  

## Netzwerk und CPU drosseln   

Wenn Sie das Netzwerk und die CPU Drosseln möchten, wählen Sie **Mid-Tier-Handy** oder **Low-End-Handy** aus der **Drosselungs** Liste aus.  

> ##### Abbildung 16  
> Die Drosselungs Liste  
> ![Die Drosselungs Liste][ImageThrottling]  

**Mid-Tier-Handy** simuliert schnelles 3G und drosselt Ihre CPU so, dass Sie viermal langsamer als normal ist.  **Low-End-Mobile** simuliert langsames 3G und bremst Ihre CPU sechsmal langsamer als normal.  Beachten Sie, dass die Drosselung relativ zur normalen Funktion Ihres Laptops oder Desktops ist.  

> [!NOTE]
> Die **Drosselungs** Liste wird ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.  

> ##### Abbildung 17  
> Die Gerätesymbolleiste  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar3]  

### Nur die CPU drosseln   

Wenn Sie nur die CPU und nicht das Netzwerk Drosseln möchten, wechseln Sie zum **Leistungs** Panel, klicken Sie auf Einstellungen für **Aufnahmeeinstellungen** ![ ][ImageCaptureIcon] , und wählen Sie dann in der Liste **CPU** die Option **4X Verlangsamung** oder **6x Verlangsamung** aus.  

> ##### Abbildung 18  
> Die CPU-Liste  
> ![Die CPU-Liste][ImageCPU]  

### Nur das Netzwerk drosseln   

Wenn Sie nur das Netzwerk und nicht die CPU Drosseln möchten, gehen Sie zum **Netzwerk** Panel, und wählen Sie **fast 3G** oder **Slow 3G** aus der **Drosselungs** Liste aus.  

> ##### Abbildung 19  
> Die Drosselungs Liste  
> ![Die Drosselungs Liste][ImageNetwork]  

Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, geben `3G` Sie ein, und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.  

> ##### Abbildung 20  
> Das Befehlsmenü  
> ![Das Befehlsmenü][ImageCommandMenu]  

Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.  Klicken Sie auf **Aufnahme** Einstellungen aufzeichnen ![ ][ImageCaptureIcon] , und wählen Sie dann in der Liste **Netzwerk** die Option **fast 3G** oder **Slow 3G** aus.  

> ##### Abbildung 21  
> Festlegen der Netzwerk Drosselung im Leistungs Panel  
> ![Festlegen der Netzwerk Drosselung im Leistungs Panel][ImageNetwork2]  

## Überschreiben von Geolocation   

Klicken Sie auf **anpassen und Steuern von devtools** , `...` und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus, um die Benutzeroberfläche für Geolocation zu öffnen.  

> ##### Abbildung 22  
> Sensoren  
> ![Sensoren][ImageSensors]  

Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.  

> ##### Abbildung 23  
> Sensoren anzeigen  
> ![Sensoren anzeigen][ImageShowSensors]  

Wählen Sie eine der Voreinstellungen aus der Liste **Geolocation** aus, oder wählen Sie **benutzerdefinierter Speicherort** aus, um Ihre eigenen Koordinaten einzugeben, oder wählen Sie **nicht verfügbarer Speicherort** aus, um zu testen, wie sich die Seite verhält, wenn sich die Geolokation in einem Fehlerzustand befindet.  

> ##### Abbildung 24  
> Geolocation  
> ![Geolocation][ImageGeolocation]  

## Ausrichtung einstellen   

Klicken Sie zum Öffnen der UI für die Ausrichtung auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.  

> ##### Abbildung 25  
> Sensoren  
> ![Sensoren][ImageSensors2]  

Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.  

> ##### Abbildung 26  
> Sensoren anzeigen  
> ![Sensoren anzeigen][ImageShowSensors2]  

Wählen Sie eine der Voreinstellungen aus der **Ausrichtungs** Liste aus, oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um Ihre eigenen Alpha-, Beta-und Gammawerte zu definieren.  

> ##### Abbildung 27  
> Ausrichtung  
> ![Ausrichtung][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 1: die Gerätesymbolleiste"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Abbildung 2: die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Abbildung 3: Anzeigen von medienabfragen"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Abbildung 4: Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern."  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Abbildung 5: Gerätetypen Liste"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Abbildung 6: Geräteliste"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Abbildung 7: Querformat"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 8: die Gerätesymbolleiste"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Abbildung 9: Anzeigen des geräterahmens"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Abbildung 10: der Geräterahmen für das iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Abbildung 11: Auswählen von "Bearbeiten""  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Abbildung 12: Erstellen eines benutzerdefinierten Geräts"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Abbildung 13: Anzeigen der Lineale"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Abbildung 14: Lineale oberhalb und Links vom Viewport"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Abbildung 15: Zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Abbildung 16: die Drosselungs Liste"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 17: die Gerätesymbolleiste"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Abbildung 18: die CPU-Liste"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Abbildung 19: die Drosselungs Liste"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Abbildung 20: Befehlsmenü"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Abbildung 21: Festlegen der Netzwerk Drosselung im Leistungs Panel"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Abbildung 22: Sensoren"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Abbildung 23: Anzeigen von Sensoren"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Abbildung 24: Geolocation"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Abbildung 25: Sensoren"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Abbildung 26: Anzeigen von Sensoren"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Abbildung 27: Ausrichtung"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/Index "erste Schritte mit dem Remotedebuggen von Android-Geräten"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – First-Order – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
