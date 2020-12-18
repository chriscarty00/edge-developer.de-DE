---
description: Verwenden des Emulations Panels zum Testen unterschiedlicher Browser Profile, Bildschirmgrößen und Auflösungen sowie GPS-Positionskoordinaten
title: DevTools-Emulation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Geräteemulation, reaktionsfähiges Design, Geolocation, Auflösung
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233811"
---
# Emulation  

> [!NOTE]
> Der neue Microsoft Edge basiert auf Chromium, und beginnt mit Version 75.  Wenn Sie weitere Informationen wünschen, [Laden Sie den neuen Microsoft Edge herunter][MicrosoftNewEdge], und probieren Sie die neuen [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromium]aus.  
> 
> Wenn Sie unterschiedliche Geräte, Browser, Bildschirmgrößen und Auflösungen im neuen devtools emulieren möchten, navigieren Sie zum [emulieren mobiler Geräte in Microsoft Edge \ (Chrom \) devtools][DevtoolsGuideChromiumDeviceMode].  

Das **Emulations** Panel hilft bei den folgenden Aktivitäten.    

*   Simulieren verschiedener [Geräteprofile](#device), [Browser](#browser-profile)und [Bildschirmgrößen und-Auflösungen](#display)  
*   Testen verschiedener [Geolocation-Einstellungen und-Koordinaten](#geolocation)  

:::image type="complex" source="./media/emulation.png" alt-text="Das Microsoft Edge devtools-Emulations Panel" lightbox="./media/emulation.png":::
   Das Microsoft Edge devtools- **Emulations** Panel  
:::image-end:::  

1.  Die Schaltfläche für die **Beibehaltung der Emulationseinstellungen** speichert alle von Ihnen vorgenommenen Änderungen an den Standardeinstellungen für die Desktop Emulation, auch wenn Sie das devtools schließen und erneut öffnen.  

1.  Mit der Schaltfläche " **Emulationseinstellungen zurücksetzen** " werden Ihre Emulationseinstellungen wieder auf das standardmäßige Desktop Browserprofil und die Microsoft Edge-Benutzer-Agent-Zeichenfolge zurückgesetzt, wobei GPS deaktiviert ist.  

1.  Wenn eine dieser Optionen von der Standardeinstellung geändert wird, wird auf der Registerkarte **Emulation** eine Informationswarnung angezeigt, die darauf hinweist, dass einige Aspekte des Verhaltens Ihres Browsers emuliert werden.  

## Gerät  

Wählen Sie aus einer vordefinierten Liste von Windows-Geräteprofilen aus, die die anderen Emulationsoptionen automatisch konfigurieren oder Ihre eigene **benutzerdefinierte** Konfiguration angeben.  Wechseln Sie zurück zu **Standard** , um alle Emulations Tools zurückzusetzen.  

## Modus  

### Browser Profil  

Eine schnelle Möglichkeit zum Simulieren der auf einem Windows Phone-Gerät ausgeführten Seite besteht darin, die **Browser Profil** Einstellung auf **Windows Phone**zu ändern.  

#### Benutzer-Agent-Zeichenfolge  

Das Ändern der Zeichenfolge des Benutzer-Agents, um einen anderen Browser zu imitieren, ist ein guter erster Schritt beim Debuggen von Fehlern, die nur in Microsoft Edge stattfinden.  

Skripts verwenden die Zeichenfolge des Benutzer-Agents, um festzustellen, welcher Browser verwendet wird.  Das Skript kann Front-End-, Back-End-oder Front-End-und Back-End-Daten sein.  Obwohl Ihr Code keine Browsererkennung verwendet, kann der Code ihn von einer JavaScript-Bibliothek eines Drittanbieters oder von einem serverseitigen Skript erben.  

Das Problem bei der Browsererkennung besteht darin, dass Sie Funktionen in Ihrer Webseite mithilfe von Annahmen zu Browserfunktionen skalieren oder ändern können. Stattdessen sollten Sie die Funktionserkennung verwenden, um die Funktionen Ihres Browsers zu erkennen.  Unerwartetes Verhalten kann aufgrund einer der folgenden Situationen auftreten.  

*   Code, der auf Windows Internet Explorer 8 ausgerichtet ist, kann in Microsoft Edge anders ausgeführt werden.  
*   Ein Feature, das Ihr Browser unterstützen sollte, ist aufgrund einer vom Entwickler vorgenommenen Annahme deaktiviert.  

Wenn das Problem durch Ändern der Zeichenfolge des Benutzer-Agents behoben wird, ist die Browsererkennung wahrscheinlich eine Ursache.  

## Anzeige  

Zeigen Sie Emulation an, um eine Vorschau Ihrer Website auf unterschiedlichen Bildschirmgrößen und Auflösungen anzuzeigen.  

*   herkömmliche Desktop Monitore  
*   kleinere mobile Bildschirme  
*   neuere Monitore mit hoher Auflösung  

Emulationen werden angepasst, um zu versuchen, die physikalischen Dimensionen der emulierten Bildschirme anzupassen.  Emulierte Pixel können komprimiert oder erweitert angezeigt werden. Eine Emulation wird nicht empfohlen, wenn Sie die pixelperfekte Positionierung von HTML-Elementen testen müssen.  Die Emulation eignet sich jedoch gut für das Testen von reaktionsfähigen Designs und das identifizieren größerer Element Positionierungsprobleme.  

### Ausrichtung  

Wählen Sie im **quer** Format oder **Hochformat** aus.  

### Lösung  

Wählen Sie aus einer vordefinierten Liste gängiger Geräte Auflösungen aus, oder geben Sie Ihre eigene **benutzerdefinierte** Konfiguration an.  Es werden Auflösungen von bis zu 80 Zoll und 3820 x 2160 unterstützt.  

## Geolocation  

Wenn Ihre Website die [Geolocation-API][MdnGeolocationUsing] zum Bereitstellen von standortbasierten Diensten verwendet, stehen die folgenden Aktivitäten über die Bequemlichkeit Ihres Desktops zur Verfügung.  

*   Einfaches Testen unterschiedlicher GPS-Koordinaten  
*   Einfaches Testen unterschiedlicher Sensorzustände  

Die Einstellungen setzen alle tatsächlichen GPS-Koordinaten und den Sensorzustand auf Geräten außer Kraft, die Geolokation unterstützen.  

Ihre Website muss vor der Verwendung des Gerätespeicher Orts die Berechtigung eines Benutzers anfordern und ihm die Genehmigung erteilen.  Testen Sie, wie sich Ihre Website über den Microsoft Edge **Settings** -Bereich mit und ohne Standort Berechtigungen verhält.  

**...** >  **Einstellungen**  >  **Erweiterte Einstellungen anzeigen**  >  **Website Berechtigungen**  >  **Verwalten** von  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Verwalten von Websiteberechtigungen über den Microsoft Edge Settings-Dialog" lightbox="./media/settings_manage_permissions.png":::
   Verwalten von Websiteberechtigungen über den Microsoft Edge **Settings** -Dialog  
:::image-end:::  

## Tastenkombinationen

| Aktion  | Tastenkombination  |  
|:--- |:--- |  
| Zurücksetzen von Emulationseinstellungen | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "Geolocation-API | MDN"  
