---
description: Verwenden Sie virtuelle Geräte im Gerätemodus für Microsoft Edge zum Erstellen von mobilen First-Websites.
title: Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: eababe8112b5d888671a8955e16f0fe1c89564fb
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993016"
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

Klicken Sie auf **Gerätesymbolleiste umschalten** \ ( ![ Gerätesymbolleiste umschalten ][ImageDeviceToolbarIcon] \), um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die Gerätesymbolleiste  
:::image-end:::  

Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.  

### Reaktionsfähiger viewportmodus   

Ziehen Sie die Ziehpunkte, um die Größe des Viewports auf die gewünschten Bemaßungen zu ändern.  Oder geben Sie bestimmte Werte in die Felder Breite und Höhe ein.  In der folgenden Abbildung ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus  
:::image-end:::  

#### Anzeigen von medienabfragen   

Wenn Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen möchten, klicken Sie auf **Weitere Optionen** , und wählen Sie dann **medienabfragen anzeigen**aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Anzeigen von medienabfragen" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Anzeigen von medienabfragen**  
:::image-end:::  

Klicken Sie auf einen Haltepunkt, um die Breite des Viewports so zu ändern, dass der Haltepunkt ausgelöst wird.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern." lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.  
:::image-end:::  

#### Einrichten des Gerätetyps   

Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste der Gerätetypen" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Liste der **Gerätetypen**  
:::image-end:::  

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

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Geräteliste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   **Geräte** Liste  
:::image-end:::  

#### Drehen des Viewports in Querformat   

Klicken Sie auf **drehen** \ ( ![ drehen ][ImageRotateIcon] \), um das Ansichtsfenster in Querformat zu drehen.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Querformat" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   Querformat  
:::image-end:::  

> [!NOTE]
> Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

Siehe auch [Ausrichtung einstellen](#set-orientation).  

#### Geräterahmen anzeigen   

Wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie ein iPhone 6 simulieren, öffnen Sie **Weitere Optionen** , und wählen Sie dann **Geräterahmen anzeigen** aus, um den Frame des physikalischen Geräts um den Viewport anzuzeigen.  

> [!NOTE]
> Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies wahrscheinlich, dass devtools gerade keine Grafiken für diese bestimmte Option hat.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Geräterahmen anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Geräterahmen anzeigen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Der Geräterahmen für das iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Der Geräterahmen für das iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Hinzufügen eines benutzerdefinierten mobilen Geräts   

So fügen Sie ein benutzerdefiniertes Gerät hinzu:  

1.  Klicken Sie auf die **Geräte** Liste, und wählen Sie dann **Bearbeiten**aus.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Wählen Sie bearbeiten aus." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Wählen Sie **Bearbeiten** aus.  
    :::image-end:::  
    
1.  Klicken Sie auf **Benutzerdefiniertes Gerät hinzufügen**.  
1.  Geben Sie einen Namen, eine Breite und eine Höhe für das Gerät ein.  Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.  Das Feld "Gerätetyp" ist die Liste, die standardmäßig auf " **Mobiltelefon** " festgesetzt ist.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Erstellen eines benutzerdefinierten Geräts" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Erstellen eines benutzerdefinierten Geräts  
    :::image-end:::  

### Lineale anzeigen   

Klicken Sie auf **Weitere Optionen** , und wählen Sie dann **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.  Die Größeneinheit der Lineale ist Pixel.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Lineale anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **Lineale anzeigen**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Lineale oberhalb und Links des Viewports" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Lineale oberhalb und Links des Viewports  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Zoomen des Viewports   

Verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Netzwerk und CPU drosseln   

Wenn Sie das Netzwerk und die CPU Drosseln möchten, wählen Sie **Mid-Tier-Handy** oder **Low-End-Handy** aus der **Drosselungs** Liste aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Drosselungs Liste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Die **Drosselungs** Liste  
:::image-end:::  

**Mid-Tier-Handy** simuliert schnelles 3G und drosselt Ihre CPU so, dass Sie viermal langsamer als normal ist.  **Low-End-Mobile** simuliert langsames 3G und bremst Ihre CPU sechsmal langsamer als normal.  Beachten Sie, dass die Drosselung relativ zur normalen Funktion Ihres Laptops oder Desktops ist.  

> [!NOTE]
> Die **Drosselungs** Liste ist ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

### Nur die CPU drosseln   

Wenn Sie nur die CPU und nicht das Netzwerk Drosseln möchten, wechseln Sie zum **Leistungs** Panel, klicken Sie auf **Aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \), und wählen Sie dann in der **CPU** -Liste die Option **4X Verlangsamung** oder **6x Verlangsamung** aus.  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die CPU-Liste" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   Die **CPU** -Liste  
:::image-end:::  

### Nur das Netzwerk drosseln   

Wenn Sie nur das Netzwerk und nicht die CPU Drosseln möchten, gehen Sie zum **Netzwerk** Panel, und wählen Sie **fast 3G** oder **Slow 3G** aus der **Drosselungs** Liste aus.  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Drosselungs Liste" lightbox="../media/device-mode-network-throttle.msft.png":::
   Die **Drosselungs** Liste  
:::image-end:::  

Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen, geben `3G` Sie ein, und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   Das **Befehlsmenü**  
:::image-end:::  

Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.  Klicken Sie auf **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \), und wählen Sie dann in der Liste **Netzwerk** die Option **fast 3G** oder **Slow 3G** aus.  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Einrichten der Netzwerk Drosselung im Leistungs Panel" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   Einrichten der Netzwerk Drosselung im **Leistungs** Panel  
:::image-end:::  

## Überschreiben von Geolocation   

Klicken Sie zum Öffnen der Benutzeroberfläche für Geolocation auf **anpassen und Steuern von devtools** \ ( `...` \), und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **Sensoren**  
:::image-end:::  

Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Sensoren anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **Sensoren anzeigen**  
:::image-end:::  

Wählen Sie eine der Voreinstellungen aus der Liste **Geolocation** aus, oder wählen Sie **benutzerdefinierter Speicherort** aus, um Ihre eigenen Koordinaten einzugeben, oder wählen Sie **nicht verfügbarer Speicherort** aus, um zu testen, wie sich die Seite verhält, wenn sich die Geolokation in einem Fehlerzustand befindet.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **Geolocation**  
:::image-end:::  

## Ausrichtung einstellen   

:::row:::
   :::column span="":::
      Klicken Sie zum Öffnen der UI für die Ausrichtung auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensoren**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Sensoren anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Sensoren anzeigen**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Wählen Sie eine der Voreinstellungen aus der **Ausrichtungs** Liste aus, oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um Ihre eigenen Alpha-, Beta-und Gammawerte zu definieren.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **Ausrichtung**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/Index.MD "erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs "  

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
