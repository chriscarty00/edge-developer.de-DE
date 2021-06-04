---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Mobile-First-Websites zu erstellen.
title: Emulieren mobiler Geräte in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, emulation, device, simulation, mobile
ms.openlocfilehash: b62a1799b1707fc4c6890bb7ad9ad4aa9afab113
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564406"
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
# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a>Emulieren mobiler Geräte in Microsoft Edge DevTools  

Verwenden **Sie die Geräteemulation,** um das Aussehen und Reagieren Ihrer Seite auf einem mobilen Gerät zu erahnen.  Die Microsoft Edge DevTools bieten eine Sammlung von Funktionen, mit deren Hilfe Sie mobile Geräte emulieren können.  Die Auflistung enthält die folgenden Features.  

*   [Simulieren eines mobilen Viewports](#simulate-a-mobile-viewport)  
*   [Drosseln des Netzwerks](#throttle-the-network-only)  
*   [Drosseln der CPU](#throttle-the-cpu-only)  
*   [Simulieren von Geolocation](#override-geolocation)  
*   [Festlegen der Ausrichtung](#set-orientation)  
*   [Festlegen der Benutzer-Agent-Zeichenfolge](#set-user-agent-string)  

## <a name="limitations"></a>Einschränkungen  

**Bei der Geräteemulation** [handelt][WikiApproximation] es sich um eine Näherung des Aussehens und Fühlungsgefühls Ihrer Seite auf einem mobilen Gerät in erster Ordnung.  **Bei der Geräteemulation** wird Der Code nicht tatsächlich auf einem mobilen Gerät ausgeführt.  Stattdessen simulieren Sie die mobile Benutzeroberfläche von Ihrem Laptop oder Desktop aus.  

Einige Aspekte mobiler Geräte werden in DevTools nie emuliert.  Beispielsweise ist die Architektur mobiler CPUs anders als die Architektur von Laptop- oder Desktop-CPUs.  Im Zweifelsfall sollten Sie Ihre Seite am besten auf einem mobilen Gerät ausführen.  Verwenden Sie [Remotedebugging][DevToolsRemoteDebugging] zum Interagieren mit dem Code einer Seite von Ihrem Computer, während Ihre Seite tatsächlich auf einem mobilen Gerät ausgeführt wird.  Sie können alle vier anzeigen, ändern, debuggen, profilieren oder alle vier anzeigen, während Sie mit dem Code interagieren.  Ihr Computer kann ein Notizbuch oder ein Desktopcomputer sein.  

## <a name="simulate-a-mobile-viewport"></a>Simulieren eines mobilen Viewports  

Wählen **Sie Geräteemulation** umschalten \( ![ Gerätesymbolleiste ](../media/toggle-device-toolbar-dark-icon.msft.png) umschalten \) oder **DevTools** anpassen und steuern \( `...` \) > Geräteemulation, **** um die Benutzeroberfläche zu öffnen, mit der Sie einen mobilen Ansichtsfenster simulieren können.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Die Gerätesymbolleiste  
:::image-end:::  

Standardmäßig wird die Gerätesymbolleiste im Modus "Responsive Viewport" geöffnet.  

### <a name="responsive-viewport-mode"></a>Responsive Viewport Mode  

Ziehen Sie die Ziehpunkte, um das Aussehen und Aussehen Ihrer Seite in mehreren Bildschirmgrößen schnell zu testen, um die Größe des Ansichtsfensters auf die erforderlichen Dimensionen zu ändern.  Sie können auch bestimmte Werte in die Felder Breite und Höhe eingeben.  In der folgenden Abbildung wird die Breite auf und `626` die Höhe auf `516` festgelegt.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Ziehpunkte zum Ändern der Dimensionen des Ansichtsfensters im Modus Responsive Viewport" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Die Ziehpunkte zum Ändern der Dimensionen des Ansichtsfensters im Modus "Responsive Viewport"  
:::image-end:::  

#### <a name="show-media-queries"></a>Anzeigen von Medienabfragen  

Wenn Sie Medienabfragen auf Ihrer Seite definiert haben, springen Sie zu den Viewportdimensionen, in denen diese Medienabfragen wirksam werden, indem Sie Haltepunkte für Medienabfragen über Dem Viewport anzeigen.  Wählen **Sie Weitere Optionen**  >  **Medienabfragen anzeigen aus.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Anzeigen von Medienabfragen" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Anzeigen von Medienabfragen**  
:::image-end:::  

Wählen Sie einen Haltepunkt aus, um die Breite des Viewports so zu ändern, dass die Medienabfrage ausgelöst wird.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Wählen Sie einen Haltepunkt aus, um die Breite des Ansichtsfensters zu ändern." lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Wählen Sie einen Haltepunkt aus, um die Breite des Ansichtsfensters zu ändern.  
:::image-end:::  

#### <a name="set-the-device-type"></a>Festlegen des Gerätetyps  

Verwenden Sie die **Liste Gerätetyp,** um ein mobiles Gerät oder Desktopgerät zu simulieren.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Die Liste Gerätetyp" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Die **Liste "Gerätetyp"**  
:::image-end:::  

In der folgenden Tabelle werden die Unterschiede zwischen den verfügbaren Gerätetypoptionen beschrieben.  Die Spalte Rendering-Methode bezieht sich darauf, ob Microsoft Edge Seite als mobiler Oder Desktop-Viewport gerendert wird.  Die Spalte Cursorsymbol bezieht sich auf den Cursortyp, der angezeigt wird, wenn Sie auf die Seite zeigen.  Die Spalte Ereignisse, die ausgelöst wird, bezieht sich darauf, ob die Seite ausgelöst wird oder ob Ereignisse ausgelöst `touch` `click` werden, wenn Sie mit der Seite interagieren.  

| Option | Renderingmethode | Cursorsymbol | Ausgelöste Ereignisse |  
|:--- |:--- |:--- |:--- |  
| Mobilgeräte | Mobilgeräte | Kreis | Toucheingabe |  
| Mobil \(keine Berührung\) | Mobilgeräte | Normal |  wählen Sie  |  
| Desktop | Desktop | Normal |  wählen Sie  |  
| Desktop \(touch\) | Desktop | Kreis | Toucheingabe |  

> [!NOTE]
> Wenn die **Liste Gerätetyp** nicht angezeigt wird, wählen Sie **Weitere Optionen**  >  **Gerätetyp hinzufügen aus.**  

### <a name="mobile-device-viewport-mode"></a>Ansichtsportmodus für mobile Geräte  

Um die Abmessungen eines bestimmten mobilen Geräts zu simulieren, wählen Sie das Gerät in der Liste **Gerät** aus.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Die Geräteliste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Die **Geräteliste**  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a>Drehen des Ansichtsfensters in die Querformatausrichtung  

Testen Sie Ihre Webseite im Querformat.  

*   Um den Ansichtsfenster in die Querformatausrichtung zu drehen, wählen Sie **Drehen** \( ![ Drehen ](../media/rotate-dark-icon.msft.png) \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Seite, die im Querformat angezeigt wird" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Seite, die im Querformat angezeigt wird  
    :::image-end:::  
    
> [!NOTE]
> Die **Schaltfläche Drehen** wird ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

Weitere Informationen finden Sie unter Festlegen [der Ausrichtung](#set-orientation).  

#### <a name="show-device-frame"></a>Anzeigen des Geräteframes  

Zeigen Sie den physischen Geräterahmen um den Viewport an, wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren, z. B. iPhone 6.  

1.  Öffnen **Sie Weitere Optionen**.  
1.  Wählen **Sie Geräterahmen anzeigen aus.**  

> [!NOTE]
> Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies, dass DevTools keine Art für die Option hat.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Anzeigen des Geräteframes" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Anzeigen des Geräteframes  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Der Geräterahmen für iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Der Geräterahmen für iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a>Hinzufügen eines benutzerdefinierten mobilen Geräts  

Wenn die option für mobile Geräte, die Sie benötigen, nicht in der Standardliste enthalten ist, können Sie ein benutzerdefiniertes Gerät hinzufügen.  Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Gerät hinzuzufügen.  

1.  Wählen Sie **die Liste Gerät** > Bearbeiten **aus.**  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Wählen Sie Bearbeiten aus" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Wählen Sie **Bearbeiten aus**  
    :::image-end:::  
    
1.  Wählen **Sie Benutzerdefiniertes Gerät hinzufügen aus.**  
1.  Geben **Sie unter Emulierte**Geräte den Gerätenamen, die Bildschirmbreite und die Bildschirmhöhe für das benutzerdefinierte Gerät ein.  Das [Gerätepixelverhältnis,][MDNWindowDevicePixelRatio] [die Benutzer-Agent-Zeichenfolge][MDNUserAgent]und [die Gerätetypfelder](#set-the-device-type) sind optional.  Das Gerätetypfeld ist standardmäßig **auf Mobile festgelegt.**  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Erstellen eines benutzerdefinierten Geräts" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Erstellen eines benutzerdefinierten Geräts  
    :::image-end:::  
    
### <a name="show-rulers"></a>Anzeigen von Lineale  

Wenn Sie Bildschirmmaße messen müssen, können Sie Lineale verwenden, um die Bildschirmgröße in Pixeln zu messen.  Wählen **Sie Weitere Optionen**  >  **Lineale anzeigen** aus, um Lineale oben und links vom Viewport anzuzeigen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Menüelement zum Anzeigen von Lineale" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Menüelement zum Anzeigen von Lineale  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Lineale oberhalb und links vom Viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Lineale oberhalb und links vom Viewport  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a>Zoomen des Viewports  

Verwenden Sie die Zoomliste zum Vergrößern oder Verkleinern, um das Aussehen und Das Gefühl Ihrer Seite auf mehreren Zoomstufen zu testen. ****  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a>Drosseln des Netzwerks und der CPU  

Mobile Geräte haben häufig Netzwerk- und CPU-Einschränkungen.  Stellen Sie sicher, dass Sie testen, wie schnell Ihre Seite geladen wird und wie sie mit unterschiedlichen Internet- und CPU-Geschwindigkeiten reagiert.  

Drosseln Sie das Netzwerk und die CPU.  

1.  Wählen **Sie Drosselungsliste** aus, und ändern Sie die Voreinstellung in **Mobile** Oder **Low-End Mobile der Mittleren Ebene.**  
    *   **Mid-Tier Mobile** simuliert `fast 3G` und drosselt Ihre CPU.  Er ist viermal langsamer als normal.  
    *   **Low-End Mobile** simuliert `slow 3G` und drosselt Ihre CPU.  Sie ist sechsmal langsamer als normal.  
    
Die Drosselung basiert auf der normalen Funktion Ihres Laptops oder Desktops.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Einschränkungsliste in der Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Die **Einschränkungsliste** in der Gerätesymbolleiste  
:::image-end:::  

> [!NOTE]
> Wenn die **Einschränkungsliste** ausgeblendet ist, ist **die Gerätesymbolleiste** zu schmal.  Erhöhen Sie die Breite **der**Gerätesymbolleiste, um auf die Einschränkungsliste **zu zugreifen.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Die **Gerätesymbolleiste**  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a>Nur die CPU drosseln  

Führen Sie die folgenden Schritte aus, um nur die CPU und nicht das Netzwerk zu drosseln.

1.  Wählen Sie **den Bereich** Leistung aus, und wählen Sie **Capture Einstellungen** \( Capture ![ Einstellungen ](../media/capture-settings-icon.msft.png) \).
1.  Wählen **Sie CPU**  >  **4x Verlangsamung** oder **6x Verlangsamung aus.**
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die CPU-Liste im Leistungsbereich" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Die **CPU-Liste** im **Leistungsbereich**  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a>Drosseln des Netzwerks  

Führen Sie die folgenden Schritte aus, um das Netzwerk zu drosseln.

1.  Wählen Sie das **Netzwerktool** aus.
1.  Wählen **Sie Online**Fast  >  **3G** or Slow 3G **aus.**
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Einschränkungsliste im Netzwerkbereich" lightbox="../media/device-mode-network-throttle.msft.png":::
       Die **Einschränkungsliste** im Netzwerkbereich  
    :::image-end:::  
    
    Oder wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) **** `3G` **** **** aus, um das Befehlsmenü zu öffnen, geben Sie ein, und wählen Sie Schnelle 3G-Drosselung aktivieren oder langsame 3G aktivieren aus.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
Sie können die Netzwerkeinschränkung auch im Bereich **Leistung** festlegen.  

1.  Wählen **Sie Capture Einstellungen** \( Capture Einstellungen ![ \) aus, und wählen Sie die Liste Netzwerk aus, und ändern Sie die Voreinstellung in Fast ](../media/capture-settings-icon.msft.png) **3G** oder **Slow 3G**. ****  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Festlegen der Netzwerkeinschränkung aus dem Leistungsbereich" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Festlegen der Netzwerkeinschränkung aus dem **Leistungsbereich**  
    :::image-end:::  
    
## <a name="override-geolocation"></a>Außerkraftsetzung der Geolocation  

:::row:::
   :::column span="":::
      Wenn Ihre Seite von Geolocationinformationen von einem mobilen Gerät abhängt, um ordnungsgemäß gerendert zu werden, stellen Sie unterschiedliche Geolocations mithilfe der geolocation-überschreibenden Benutzeroberfläche zur Verfügung.  

      1.  Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere Tools **Sensoren**  >  **aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren für Geolocation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensoren** für Geolocation  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen Sie das Befehlsmenü.  
          *   Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).  
      1. Geben `Sensors` Sie ein, und wählen **Sie Sensoren anzeigen aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Anzeigen von Sensoren für geolocation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Anzeigen von Sensoren** für geolocation  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Im Bereich **Sensoren** können Sie einen der vordefinierten Speicherorte auswählen, die in DevTools enthalten sind, indem Sie das **Dropdownmenü** Speicherort verwenden.  Wenn Sie einen benutzerdefinierten Speicherort eingeben, wählen Sie **Andere...** und geben Sie die Koordinaten Ihres benutzerdefinierten Speicherorts ein.  Wenn Sie Ihre Seite in einem Fehlerzustand testen möchten, wenn Standortinformationen nicht verfügbar sind, wählen Sie **Location unavailable aus.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Sensorbereich mit ausgewählter voreingestellter Position" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    **Sensorbereich** mit ausgewählter voreingestellter Position.  
:::image-end:::

## <a name="set-orientation"></a>Festlegen der Ausrichtung  

:::row:::
   :::column span="":::
      Wenn Ihre Seite von Ausrichtungsinformationen eines mobilen Geräts abhängt, um ordnungsgemäß gerendert zu werden, öffnen Sie die Ausrichtungsbenutzeroberfläche.  

      1.  Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere Tools **Sensoren**  >  **aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren für die Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensoren für** die Ausrichtung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen Sie das Befehlsmenü.  
          *   Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).  
      1. Geben `Sensors` Sie ein, und wählen **Sie Sensoren anzeigen aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Anzeigen von Sensoren für die Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Anzeigen von Sensoren** für die Ausrichtung  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Im **Bereich Sensoren** können Sie im Dropdownmenü Ausrichtung eine voreingestellte Ausrichtung auswählen. ****  Wenn Sie Ihre eigene Ausrichtung eingeben, wählen Sie **Benutzerdefinierte**Ausrichtung aus, und geben Sie Ihre eigenen [Alpha-,][MDNDeviceOrientaitonAlpha] [Beta-][MDNDeviceOrientaitonBeta]und [Gammawerte][MDNDeviceOrientaitonGamma] ein.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ausrichtungsoptionen im Bereich Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Ausrichtungsoptionen** im **Bereich Sensoren**  
:::image-end:::  

## <a name="set-user-agent-string"></a>Festlegen der Zeichenfolge des Benutzer-Agents  

:::row:::
   :::column span="":::
      Wenn Ihre Seite von der Benutzer-Agent-Zeichenfolge eines mobilen Geräts abhängt, um ordnungsgemäß gerendert zu werden, verwenden Sie den Bereich Netzwerkbedingungen, um unterschiedliche Zeichenfolgen für den Benutzer-Agent zur Verfügung zu stellen. ****  
      
      1.  Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere **Tools**  >  **Netzwerkbedingungen aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Eintrag Netzwerkbedingungen im Menü Weitere Tools" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         **Eintrag "Netzwerkbedingungen"** im Menü **Weitere** Tools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Öffnen Sie das Befehlsmenü.  
          *   Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).  
      1. Geben `Network conditions` Sie ein, und wählen **Sie Netzwerkbedingungen anzeigen aus.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Anzeigen von Netzwerkbedingungen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Anzeigen von Netzwerkbedingungen**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Aktivieren Sie **neben Benutzer-Agent**das **Kontrollkästchen** Automatisch auswählen.  Wählen Sie dann **Custom...** aus, um aus einer Liste vordefinierter Benutzer-Agent-Zeichenfolgen auszuwählen.  Geben Sie die Zeichenfolge in Enter a custom user agent ein, um Eine eigene Zeichenfolge für den **Benutzer-Agent ein eingeben.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Festlegen der Zeichenfolge für den Benutzer-Agent auf Microsoft Edge macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Festlegen der Zeichenfolge für den Benutzer-Agent auf Microsoft Edge macOS  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent-| MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – Erste Reihenfolge – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
