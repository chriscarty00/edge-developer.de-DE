---
description: Verwenden Sie die Windows-Runtime (WinRT), um systemeigene Windows-APIs aus ihrer JavaScript-App aufzurufen.
title: Windows-Runtime (WinRT) für JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Windows-Runtime, WinRT, PWA, JavaScript
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bd67f052d0a836c754f7b58d0625e09ae8781cd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234297"
---
# Windows-Runtime (WinRT) für JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Die [Windows-Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \(oder einfach WinRT \) ist die Sammlung von systemeigenen APIs, die die [universelle Windows-Plattform](/windows/uwp/get-started/universal-application-platform-guide) \(UWP \)-Apps nutzen, die für alle [Windows 10-Gerätefamilien](/uwp/extension-sdks/device-families-overview)ausgeführt werden.  WinRT-APIs werden in einer Reihe von unterschiedlichen Sprachen wie C#, C++, Visual Basic und JavaScript projiziert.  

Als Webentwickler können Sie diese nativen Windows-APIs von JavaScript anfordern, wenn Ihre Web-App [als installierte Windows 10-app ausgeführt](../progressive-web-apps/windows-features.md#set-up-and-run-your-universal-windows-app) wird \(vom `wwahost.exe` Prozess gestartet, anstatt vom Browser \).  Darüber hinaus kann Ihre Website, die als Windows 10-app ausgeführt wird, auch das [Microsoft Edge-WebView](#webview) -Steuerelement verwenden, um unter anderem Remote-und lokale Webinhalte sowie [MSApp](#msapp) -APIs für die BLOB-und Datenstrom Behandlung anzuzeigen.  

Hier sind die WinRT-Namespace Bereiche auf oberster Ebene, die für alle Windows 10-apps verfügbar sind:  

| WinRT-Namespace | Beschreibung |  
|:--- |:--- |  
| [AI](/uwp/api/windows.AI.MachineLearning.Preview) \(Vorschau \) | Enthält Klassen, die es apps ermöglichen, maschinelle Lernmodelle zu laden, Daten als Eingaben zu binden und die Ergebnisse auszuwerten.  |  
| [ApplicationModel](/uwp/api/windows.applicationmodel) | Bietet eine APP mit Zugriff auf Kernsystem Funktionen und Laufzeitinformationen über das App-Paket und behandelt Unterbrechungs Vorgänge.  |  
| [Daten](/uwp/api/windows.data.html) | Stellt Dienstprogrammklassen für die Arbeit mit verschiedenen Datenformaten bereit, einschließlich HTML, JSON, PDF, Text und XML.  |  
| [Geräte](/uwp/api/windows.devices) | Dieser Namespace bietet Zugriff auf die Geräteanbieter auf niedriger Ebene, einschließlich ADC, GPIO, I2 C, PWM und SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Ermöglicht grundlegende Windows-Runtime-Funktionen, einschließlich der Verwaltung asynchroner Vorgänge und des Zugriffs auf Eigenschaftenspeicher.  Dieser Namespace definiert auch allgemeine Wertetypen, die den Uniform Resource Identifier \(URI \), Datums-und Uhrzeitangaben, 2D-Messungen und andere Grundwerte darstellen.  |  
| [Spiele](/uwp/api/windows.gaming.input) |Bietet Zugriff auf die Eingabe des Gamecontrollers, die Spielleiste, die Spiel Überwachung und den Spiel-Chat.  |  
| [Globalization](/uwp/api/windows.globalization) | Bietet Globalisierungsunterstützung für Sprachprofile, geographische Regionen und internationale Kalender.  |  
| [Grafiken](/uwp/api/windows.graphics) | Stellt grundlegende Datentypen bereit, die Informationen zum Zeichnen von Grafiken enthalten.  Diese Datenstrukturen werden häufig verwendet, um zu definieren, wie große Flächen bei Verwendung der CompositionVirtualDrawingSurface-Klasse gezeichnet werden.  |  
| [Management](/uwp/api/windows.management) | Bietet Funktionen zum Erzwingen einer Synchronisierung von einem Mobile Device Management \(MDM \)-Gerät auf den Server.  Dieses MDM-Synchronisierungsprotokoll basiert auf dem Open Mobile Alliance-Device Management-Standard.  |  
| [Media](/uwp/api/windows.media) | Stellt Klassen zum Erstellen und arbeiten mit Medien wie Fotos, Audioaufnahmen und Videos bereit.  |  
| [Netzwerk](/uwp/api/windows.networking) | Bietet Zugriff auf hostnames und Endpunkte, die von Netzwerk-Apps verwendet werden.  |  
| [Wahrnehmung](/uwp/api/windows.perception) | Enthält Klassen, die die Umgebung des Benutzers wahrnehmen, Apps lokalisieren und die Ursache des Geräts relativ zu den Oberflächen und Hologrammen des Benutzers ermitteln.  |  
| [Sicherheit](/uwp/api/windows.security.authentication.identity) | Enthält Klassen für die Benutzerauthentifizierung, die Verwaltung von Anmeldeinformationen, kryptografische Vorgänge und Features für den Datenschutz in Unternehmen.  |  
| [Dienste](/uwp/api/windows.services.cortana) | Bietet Zugriff auf Microsoft-Dienste für Cortana, Karten, Microsoft Store und gezielte \(Abonnement \)-Inhalte.  |  
| [Speicher](/uwp/api/windows.storage) | Enthält Klassen zum Verwalten von Dateien, Ordnern und Anwendungseinstellungen.  |  
| [System](/uwp/api/windows.system) | Ermöglicht Systemfunktionen wie das Starten von apps, das Abrufen von Informationen zu einem Benutzer und das Speichern von Arbeitsspeicher Profilen.  |  
| [UI](/uwp/api/windows.ui) | Bietet eine APP mit Zugriff auf Kernsystem Funktionen und Laufzeitinformationen zur Benutzeroberfläche.  **Hinweis**: APIs im `Windows.UI.Xaml` Namespace stehen für JavaScript-apps nicht zur Verfügung \(was möglicherweise die entsprechenden Web-Standards-basierten Technologien verwenden).  |  
| [Web](/uwp/api/windows.web) | Enthält Informationen zu Fehlern, die sich aus Webdienstvorgängen ergeben.  |  

Weitere Informationen zur Verwendung finden Sie unter [Verwenden der Windows-Runtime in JavaScript](./using-the-windows-runtime-in-javascript.md).  Wenn Sie wissen möchten, wie Sie Ihre Website als Windows-app ausführen können, versuchen Sie es mit dem Lernprogramm [für PWA für Windows anpassen](../progressive-web-apps/windows-features.md) .  

## WebView  

Mit dem [Microsoft Edge-WebView](../hosting/webview/index.md) -Steuerelement können Sie Webinhalte in Ihrer Windows 10-App hosten.  Dies ähnelt der Verwendung von `<iframe>` , bietet aber viele [Weitere Funktionen und Kontrolle](../hosting/webview/index.md#webview-versus-iframe) über die Benutzeroberfläche.  

## MSApp  

Das globale [MSApp](./reference/msapp.md) -Objekt \( `window.MSApp` \) bietet verschiedene Hilfsfunktionen für JavaScript-basierte Windows 10-apps, wie etwa Dienstprogramme zum Konvertieren zwischen webbasierten Standards und äquivalenten WinRT-Objekttypen.  
