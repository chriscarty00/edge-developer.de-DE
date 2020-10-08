---
description: Verwenden des Emulations Panels zum Testen unterschiedlicher Browser Profile, Bildschirmgrößen und Auflösungen sowie GPS-Positionskoordinaten
title: DevTools-Emulation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Geräteemulation, reaktionsfähiges Design, Geolocation, Auflösung
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567637"
---
# Emulation

Das *Emulations* Panel hilft Ihnen dabei, Folgendes zu tun:
 - Simulieren verschiedener [Geräteprofile](#device), [Browser](#browser-profile), [Bildschirmgrößen und Auflösungen](#display)
 - Testen verschiedener [Geolocation-Einstellungen und-Koordinaten](#geolocation)

![Das Microsoft Edge devtools-Emulations Panel](./media/emulation.png)

1. Mit der Schaltfläche für die **Beibehaltung der Emulationseinstellungen** werden alle von Ihnen vorgenommenen Änderungen an den Standardeinstellungen für die Desktop Emulation gespeichert, auch wenn Sie das devtools schließen und erneut öffnen. 

2. Mit der Schaltfläche " **Emulationseinstellungen zurücksetzen** " werden Ihre Emulationseinstellungen wieder auf das standardmäßige *Desktop* Browserprofil und die Microsoft Edge-Benutzer-Agent-Zeichenfolge zurückgesetzt, wobei GPS deaktiviert ist.

3. Wenn eine dieser Optionen von der Standardeinstellung geändert wird, wird auf der Registerkarte **Emulation** eine Informationswarnung angezeigt, die darauf hinweist, dass ein Aspekt des Verhaltens Ihres Browsers emuliert wird.

## Gerät

Wählen Sie aus einer vordefinierten Liste von Windows-Geräteprofilen aus, die die anderen Emulationsoptionen automatisch konfigurieren oder Ihre eigene *benutzerdefinierte* Konfigurations. Wechseln Sie zurück zu *Standard* , um alle Emulations Tools zurückzusetzen.

## Modus

### Browser Profil
Eine schnelle Möglichkeit zum Simulieren der auf einem Windows Phone-Gerät ausgeführten Seite besteht darin, die **Browser Profil** Einstellung auf *Windows Phone*zu ändern.

#### Benutzer-Agent-Zeichenfolge

Das Ändern der Zeichenfolge des Benutzer-Agents, um einen anderen Browser zu imitieren, ist ein guter erster Schritt beim Debuggen von Fehlern, die nur in Microsoft Edge stattfinden. 

Frontend-und/oder Back-End-Skripte verwenden manchmal die Zeichenfolge des Benutzer-Agents, um zu ermitteln, welchen Browser Sie verwenden. Und selbst wenn Sie die Browsererkennung nicht in Ihrem eigenen Code verwenden, verwenden Sie möglicherweise eine JavaScript-Bibliothek eines Drittanbieters oder ein serverseitiges Skript.

Das Problem bei der Browsererkennung besteht darin, dass Sie häufig verwendet wird, um die Features in einer Webseite zu skalieren oder zu ändern, basierend auf dem, was der Entwickler, der das Skript schreibt, von Ihrem Browser abhängt, anstatt zu erkennen, was Ihr Browser tatsächlich mithilfe der Feature-Erkennung tun kann. Dies kann zu unerwartetem Verhalten führen, da Code, der auf Windows Internet Explorer 8 ausgerichtet ist, in Microsoft Edge sehr unterschiedlich ausgeführt werden kann. oder ein Feature, das Ihr Browser hervorragend unterstützt, ist möglicherweise aufgrund einer vom Entwickler vorgenommenen Annahme deaktiviert.

Wenn das Problem durch Ändern der Zeichenfolge des Benutzer-Agents behoben wird, ist die Browsererkennung wahrscheinlich eine Ursache.

## Anzeige

Mit der Anzeige Emulation können Sie eine Vorschau Ihrer Website auf unterschiedlichen Bildschirmgrößen und-Auflösungen anzeigen: von herkömmlichen Desktop Monitoren bis zu kleineren mobilen Bildschirmen oder neueren Displays mit hoher Auflösung.

Emulationen sind so angepasst, dass Sie den physikalischen Abmessungen der emulierten Bildschirme entsprechen. Emulierte Pixel werden möglicherweise komprimiert oder erweitert angezeigt, und es wird keine Emulation empfohlen, wenn Sie die pixelperfekte Positionierung von HTML-Elementen testen müssen. Die Emulation eignet sich jedoch gut für das Testen von reaktionsfähigen Designs und das identifizieren größerer Element Positionierungsprobleme.

### Ausrichtung

Wählen Sie im *quer* Format oder *Hochformat* aus.

### Lösung

Wählen Sie aus einer vordefinierten Liste gängiger Geräte Auflösungen aus, oder geben Sie Ihre eigene *benutzerdefinierte* Konfiguration an. Es werden Auflösungen von bis zu 80 Zoll und 3820 x 2160 unterstützt.

## Geolocation

Wenn Ihre Website die [Geolocation-API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) verwendet, um standortbasierte Dienste bereitzustellen, können Sie unterschiedliche GPS-Koordinaten und Sensorzustände ganz einfach aus der Bequemlichkeit Ihres Desktops testen. Mit diesen Einstellungen werden alle tatsächlichen GPS-Koordinaten und der Sensorzustand auf Computern, die Geolokation unterstützen, außer Kraft gesetzt. 

Wie bei jeder Verwendung personenbezogener Daten im Internet müssen Ihre Benutzer zunächst Ihrer Website die Berechtigung erteilen, Ihren Standort zu verwenden. Sie können über den Microsoft Edge *Settings* -Bereich testen, wie sich Ihre Website mit und ohne Standort Berechtigungen verhält:

**...** >  **Einstellungen**  >  **Erweiterte Einstellungen anzeigen**  >  **Website Berechtigungen**  >  **Verwalten** von

![Verwalten von Websiteberechtigungen über den Microsoft Edge Settings-Dialog](./media/settings_manage_permissions.png)

## Verknüpfungen

| Aktion                   | Tastenkombination               |
|:-------------------------|:-----------------------|
| Zurücksetzen von Emulationseinstellungen | `CTRL` + `SHIFT` + `L` |
