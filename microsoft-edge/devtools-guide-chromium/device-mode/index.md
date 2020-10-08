---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge zum Erstellen von mobilen First-Websites.
title: Emulieren von mobilen Geräten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web Development, F12 Tools, devtools, Emulation, Device, Simulation, Mobile
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997089"
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

# Emulieren von mobilen Geräten in Microsoft Edge devtools  

Verwenden Sie die **Geräteemulation** , um ungefähr zu sehen, wie Ihre Seite auf einem mobilen Gerät aussieht und reagiert.  Die Microsoft Edge-devtools bieten eine Sammlung von Features, die Ihnen beim emulieren mobiler Geräte helfen.  Die Sammlung umfasst die folgenden Features.  

*   [Simulieren eines mobilen Viewports](#simulate-a-mobile-viewport)  
*   [Netzwerk drosseln](#throttle-the-network-only)  
*   [Drosseln der CPU](#throttle-the-cpu-only)  
*   [Geolokation simulieren](#override-geolocation)  
*   [Ausrichtung einstellen](#set-orientation)  
*   [Benutzer-Agent-Zeichenfolge einrichten](#set-user-agent-string)  

## Einschränkungen  

Die **Geräteemulation** ist eine Näherung des Erscheinungsbild Ihrer Seite auf einem mobilen Gerät in [erster Reihe][WikiApproximation] .  Die **Geräteemulation** führt Ihren Code nicht auf einem mobilen Gerät aus.  Stattdessen simulieren Sie die mobile Benutzeroberfläche auf Ihrem Laptop oder Desktop.  

Einige Aspekte von mobilen Geräten werden in devtools nie emuliert.  Die Architektur von mobilen CPUs unterscheidet sich beispielsweise von der Architektur von Laptop-oder Desktop-CPUs.  Im Zweifelsfall ist es am besten, wenn Sie Ihre Seite auf einem mobilen Gerät ausführen.  Verwenden Sie [Remote Debuggen] [DevToolsRemoteDebugging], um mit dem Code einer Seite von Ihrem Computer zu interagieren, während Ihre Seite auf einem mobilen Gerät ausgeführt wird.  Sie können anzeigen, ändern, Debuggen, Profil oder alle vier während der Interaktion mit dem Code.  Ihr Computer kann ein Notizbuch oder ein Desktopcomputer sein.  

## Simulieren eines mobilen Viewports  

Wählen Sie **Geräteemulation umschalten**  \ ( ![ Gerätesymbolleiste umschalten ][ImageDeviceToolbarIcon] \) aus, oder wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Geräteemulation** aus, um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Die Gerätesymbolleiste  
:::image-end:::  

Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.  

### Reaktionsfähiger viewportmodus  

Ziehen Sie die Ziehpunkte, um das Aussehen und Verhalten Ihrer Seite über mehrere Bildschirmgrößen schnell zu testen, um die Größe des Viewports auf die gewünschten Abmessungen zu ändern.  Sie können auch bestimmte Werte in die Felder Breite und Höhe eingeben.  In der folgenden Abbildung ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus  
:::image-end:::  

#### Anzeigen von medienabfragen  

Wenn Sie medienabfragen auf der Seite definiert haben, wechseln Sie zu den Viewport-Dimensionen, in denen diese medienabfragen wirksam werden, indem Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen.  Wählen Sie **Weitere Optionen**  >  **Anzeigen von medienabfragen**aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Anzeigen von medienabfragen**  
:::image-end:::  

Wählen Sie einen Haltepunkt aus, um die Breite des Viewports so zu ändern, dass die medienabfrage ausgelöst wird.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Wählen Sie einen Haltepunkt aus, um die Breite des Viewports zu ändern.  
:::image-end:::  

#### Einrichten des Gerätetyps  

Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Liste der **Gerätetypen**  
:::image-end:::  

In der folgenden Tabelle werden die Unterschiede zwischen den verfügbaren Optionen für Gerätetypen beschrieben.  Die Spalte "Rendering-Methode" bezieht sich darauf, ob Microsoft Edge die Seite als mobiles oder Desktop-Viewport rendert.  Die Spalte Cursor Symbol bezieht sich auf den Typ des Cursors, den Sie sehen, wenn Sie auf der Seite zeigen.  Die Spalte "ausgelöste Ereignisse" bezieht sich darauf, ob die Seite ausgelöst `touch` `click` wird oder Ereignisse bei der Interaktion mit der Seite ausgelöst werden.  

| Option | Rendering-Methode | Cursor Symbol | Ausgelöste Ereignisse |  
|:--- |:--- |:--- |:--- |  
| Mobilgeräte | Mobilgeräte | Kreis | Toucheingabe |  
| Mobil \ (kein Touch \) | Mobilgeräte | Normal |  auf  |  
| Desktop | Desktop | Normal |  auf  |  
| Desktop \ (tippen Sie auf \) | Desktop | Kreis | Toucheingabe |  

> [!NOTE]
> Wenn die Liste **Gerätetyp** nicht angezeigt wird, wählen Sie **Weitere Optionen**  >  **Add Device Type**aus.  

### Ansichtsfenster Modus für mobile Geräte  

Wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren möchten, wählen Sie das Gerät in der **Geräte** Liste aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   **Geräte** Liste  
:::image-end:::  

#### Drehen des Viewports in Querformat  

Testen Sie Ihre Webseite im Querformat.  

*   Wenn Sie das Ansichtsfenster in Querformat drehen möchten, wählen Sie **drehen** \ ( ![ drehen ][ImageRotateIcon] \) aus.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Im Querformat angezeigte Seite  
    :::image-end:::  
    
> [!NOTE]
> Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

Weitere Informationen finden Sie unter [Ausrichtung einstellen](#set-orientation).  

#### Geräterahmen anzeigen  

Zeigen Sie den Frame des physikalischen Geräts um das Viewport an, wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie einem iPhone 6 simulieren.  

1.  Öffnen Sie **Weitere Optionen**.  
1.  Wählen Sie **Geräterahmen anzeigen**aus.  

> [!NOTE]
> Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies, dass devtools keine Grafiken für diese Option besitzt.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Geräterahmen anzeigen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Der Geräterahmen für das iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Hinzufügen eines benutzerdefinierten mobilen Geräts  

Wenn die von Ihnen benötigte Option für das Mobile Gerät nicht in der Standardliste enthalten ist, können Sie ein benutzerdefiniertes Gerät hinzufügen.  Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Gerät hinzuzufügen.  

1.  Wählen Sie die **Geräte** Liste > **Bearbeiten**aus.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Wählen Sie **Bearbeiten** aus.  
    :::image-end:::  
    
1.  Wählen Sie **Benutzerdefiniertes Gerät hinzufügen**aus.  
1.  Geben Sie auf **emulierten Geräten**einen Gerätenamen, eine Bildschirmbreite und eine Bildschirmhöhe für das benutzerdefinierte Gerät ein.  Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.  Das Feld "Gerätetyp" ist standardmäßig auf " **Mobil**" eingestellt.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Erstellen eines benutzerdefinierten Geräts  
    :::image-end:::  
    
### Lineale anzeigen  

Wenn Sie Bildschirmdimensionen messen müssen, können Sie die Bildschirmgröße in Pixeln mithilfe von Linealen messen.  Wählen Sie **Weitere Optionen**  >  **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Menüelement zum Anzeigen von Linealen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Lineale oberhalb und Links des Viewports  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Zoomen des Viewports  

Wenn Sie das Aussehen und Verhalten Ihrer Seite mit mehreren Zoomstufen testen möchten, verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Netzwerk und CPU drosseln  

Mobile Geräte verfügen häufig über Netzwerk-und CPU-Einschränkungen.  Stellen Sie sicher, dass Sie testen, wie schnell Ihre Seite geladen wird und wie Sie mit unterschiedlichen Internet-und CPU-Geschwindigkeiten reagiert.  

Drosseln Sie das Netzwerk und die CPU.  

1.  Wählen Sie **Drosselungs** Liste aus, und ändern Sie die voreingestellten auf **Mid-Tier-Handy** oder **Low-End-Mobiltelefon**.  
    *   **Mid-Tier-Handy** simuliert `fast 3G` und drosselt Ihre CPU.  Sie ist viermal langsamer als normal.  
    *   **Low-End Mobile** simuliert `slow 3G` und drosselt Ihre CPU.  Sie ist sechsmal langsamer als normal.  
    
Die gesamte Drosselung basiert auf der normalen Funktion Ihres Laptops oder Desktops.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Die **Drosselungs** Liste auf der Gerätesymbolleiste  
:::image-end:::  

> [!NOTE]
> Wenn die **Drosselungs Liste** ausgeblendet ist, ist die **Gerätesymbolleiste** zu schmal.  Um auf die **Drosselungs Liste**zuzugreifen, vergrößern Sie die Breite der **Gerätesymbolleiste**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

### Nur die CPU drosseln  

Führen Sie die folgenden Schritte aus, um nur die CPU und nicht das Netzwerk zu drosseln.

1.  Wählen Sie das Panel **Leistung** aus, und wählen Sie **Aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus.
1.  Wählen Sie **CPU**  >  **4X Verlangsamung** oder **6x Verlangsamung**aus.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Die **CPU** -Liste im **Leistungs** Panel  
    :::image-end:::  
    
### Nur das Netzwerk drosseln  

Führen Sie die folgenden Schritte aus, um nur das Netzwerk zu drosseln:

1.  Wählen Sie das **Netzwerk** Panel aus.
1.  Wählen Sie **Online**  >  **fast 3G** oder **Slow 3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-network-throttle.msft.png":::
       Die **Drosselungs** Liste im Netzwerk Panel  
    :::image-end:::  
    
    Oder wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen, geben Sie ein `3G` , und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.  

1.  Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahme ][ImageCaptureIcon] Einstellungen \) aus, und wählen Sie die **Netzwerk** Liste aus, und ändern Sie die Voreinstellung auf **fast 3G** oder **Slow 3G**.  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Einrichten der Netzwerk Drosselung im **Leistungs** Panel  
    :::image-end:::  
    
## Überschreiben von Geolocation  

:::row:::
   :::column span="":::
      Wenn Ihre Seite von Geolocation-Informationen eines mobilen Geräts abhängt, um Sie ordnungsgemäß zu rendern, stellen Sie unterschiedliche geolokationen mithilfe der Benutzeroberfläche Überschreiben von Geolocation bereit.  

      1.  Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**-  >  **Sensoren**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensoren** für geolocation  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen des Befehlsmenüs  
          *   Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.  
      1. Geben `Sensors` Sie ein, und wählen Sie **Sensoren anzeigen**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Sensoren** für Geolocation anzeigen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Im Bereich " **Sensoren** " können Sie mithilfe des Dropdownmenüs " **Standort** " einen der vordefinierten Speicherorte auswählen, die in devtools enthalten sind.  Wenn Sie einen benutzerdefinierten Speicherort eingeben möchten, wählen Sie **andere** aus. und geben Sie die Koordinaten des benutzerdefinierten Speicherorts ein.  Wenn Sie Ihre Seite in einem Fehlerzustand testen möchten, wenn Standortinformationen nicht verfügbar sind, wählen Sie **Speicherort nicht verfügbar**aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    Bereich " **Sensoren** " mit ausgewählter Vorwahl Position.  
:::image-end:::

## Ausrichtung einstellen  

:::row:::
   :::column span="":::
      Wenn Ihre Seite von den Orientierungs Informationen eines mobilen Geräts abhängt, um Sie ordnungsgemäß zu rendern, öffnen Sie die Benutzeroberfläche für die Ausrichtung.  

      1.  Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**-  >  **Sensoren**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensoren** zur Ausrichtung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen des Befehlsmenüs  
          *   Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.  
      1. Geben `Sensors` Sie ein, und wählen Sie **Sensoren anzeigen**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Anzeigen von Sensoren** zur Ausrichtung  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Im **Sensor** Panel können Sie eine voreingestellte Ausrichtung aus dem Dropdownmenü **Ausrichtung** auswählen.  Wenn Sie eine eigene Ausrichtung eingeben möchten, wählen Sie **benutzerdefinierte Ausrichtung**aus, und geben Sie Ihre eigenen [Alpha][MDNDeviceOrientaitonAlpha]-, [Beta][MDNDeviceOrientaitonBeta]-und [Gammawerte][MDNDeviceOrientaitonGamma] ein.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Ausrichtungs** Optionen im **Sensor** Panel  
:::image-end:::  

## Benutzer-Agent-Zeichenfolge einrichten  

:::row:::
   :::column span="":::
      Wenn Ihre Seite davon abhängt, ob die Benutzer-Agent-Zeichenfolge von einem mobilen Gerät ordnungsgemäß gerendert wird, verwenden Sie den Panel **Netzwerkbedingungen** , um unterschiedliche Benutzer-Agent-Zeichenfolgen bereitzustellen  
      
      1.  Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **Netzwerkbedingungen**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         Eintrag " **Netzwerkbedingungen** " im Menü " **Weitere Tools** "  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen des Befehlsmenüs  
          *   Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.  
      1. Geben `Network conditions` Sie ein, und wählen Sie **Netzwerkbedingungen anzeigen**aus.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Netzwerkbedingungen anzeigen**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Deaktivieren Sie neben **Benutzer-Agent**das Kontrollkästchen **automatisch auswählen** .  Wählen Sie dann **Benutzerdefiniert** aus, um aus einer Liste vordefinierter Benutzer-Agent-Zeichenfolgen auszuwählen.  Wenn Sie eine eigene Benutzer-Agent-Zeichenfolge eingeben möchten, geben Sie die Zeichenfolge in **Geben Sie einen benutzerdefinierten Benutzer-Agent ein**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Einrichten der Benutzer-Agent-Zeichenfolge auf Microsoft Edge unter macOS  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/Index.MD "erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. Beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. Gamma | MDN"  

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
