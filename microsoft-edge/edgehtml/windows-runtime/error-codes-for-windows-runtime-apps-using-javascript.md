---
description: Fehlercodes für Windows-Runtime-apps mit JavaScript.
title: Fehlercodes für Windows-Runtime-Apps mit JavaScript
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5a04a9c348a29aee2ec5936e7d923377dd53b21c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234298"
---
# Fehlercodes für Windows-Runtime-Apps mit JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Nachfolgend finden Sie die Fehlercodes, die von der Microsoft Visual Studio-Konsole bei der Entwicklung von Windows-Runtime-apps mit JavaScript angezeigt werden.  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9601: " *remoteURI*kann nicht geladen werden.  Eine APP kann keine Remote-Webinhalte im lokalen Kontext laden. " | Weitere Informationen dazu, was im webkontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "' JavaScript: ' ist ein ungültiger Attributwert und wird ignoriert.  Verwenden Sie nicht "JavaScript:"-URIs im lokalen Kontext. " | Aus Sicherheitsgründen können Sie "JavaScript:"-URIs nicht im lokalen Kontext verwenden.  Weitere Informationen dazu, was im lokalen Kontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "das ActiveX-Plug-in kann nicht geladen werden, das die Klassen-ID *ClassID*hat.  Apps können keine ActiveX-Steuerelemente laden. " | Windows-Runtime-apps mit JavaScript unterstützen keine benutzerdefinierten Microsoft-ActiveXcontrols.  Wenn Sie ein UI-Steuerelement benötigen, verwenden Sie ein Standardmäßiges Websteuerelement, eine Steuerelementbibliothek, oder erstellen Sie ein eigenes benutzerdefiniertes Steuerelement.  Wenn Sie eine benutzerdefinierte Logik ausführen müssen, erstellen Sie stattdessen ein benutzerdefiniertes Windows-Runtime-Objekt.  Informationen zu anderen HTML-, CSS-und JavaScript-Unterschieden finden Sie unter [HTML-, CSS-und JavaScript-Features und-Unterschiede][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "kann nicht zu *URI* navigieren, da eine ungültige Zeichencodierung verwendet wird.  Eine APP kann nur zu UTF8-codierten Dateien navigieren. " | Alle HTML-, JavaScript-und CSS-Formate, auf die eine Windows-Runtime zugreift, müssen als 8-Bit-Unicode-Transformations Format (UTF-8) codiert sein.  Informationen zu anderen HTML-, CSS-und JavaScript-Unterschieden finden Sie unter [HTML-, CSS-und JavaScript-Features und-Unterschiede][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "kann nicht von *SourceUri* zu *targetURI* navigieren, da sich der Ziel-URI in einer höheren Sicherheitszone befindet.  Sie können nicht von einer Zone mit geringerer Sicherheit zu einer Zone mit höherer Sicherheit navigieren, es sei denn, Sie navigieren zu einem lokalen Kontext-URI aus einem webkontext-URI, und Sie haben den lokalen Kontext-URI mit der MSApp. addPublicLocalApplicationUri-Methode registriert. " | Weitere Informationen finden Sie unter [MSApp. addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: " *URI* kann nicht geladen werden, weil eine HTTP-Verbindung verwendet wird und das Meta-Element" MS-HTTPS-Connections-only "vorhanden ist.  Nur HTTPS-Verbindungen sind zulässig, wenn Sie das Meta-Element "MS-HTTPS-Connections-only" verwenden.  Verwenden Sie eine HTTPS-Verbindung, oder entfernen Sie das Meta-Element, wenn Sie keine sichere Verbindung benötigen. " | Weitere Informationen finden Sie unter [Vorgehensweise zum Anfordern einer HTTPS-Verbindung][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "die APP kann den URI bei *URI* aufgrund dieses Fehlers nicht starten: *failureCode*." | Eine fehlende Ressource oder eine ungültige Datei sind häufige Ursachen für diesen Fehler.  |  
| APPHOST9608: "die APP konnte wegen dieses Fehlers nicht zu der leeren Seite" about: "navigieren: *errorCode*." |  |  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9610: "die APP hat einen Fehler beim Vorbereiten der Navigation zu einer benutzerdefinierten Fehlerseite gefunden: *errorCode*." |  |  
| APPHOST9611: "die APP konnte aufgrund dieses Fehlers nicht zu einer benutzerdefinierten Fehlerseite navigieren: *errorCode*." |  |  
| APPHOST9613: "die APP konnte aufgrund dieses Fehlers nicht zu *URI*  navigieren: *errorCode*." |  |  
| APPHOST9614: "ein Dokument in einem IFRAME hat den *requestedDocMode* -doc-Modus angefordert, das System erzwingt aber den *currentDocMode* -doc-Modus.  Der iframe verwendet den *currentDocMode* -doc-Modus. " | Weitere Informationen zum Anzeigen von Remote-Webinhalten finden Sie unter so wird es [gemacht: Verknüpfen mit externen Webseiten][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: "die APP kann die Datei nicht bei *URI* herunterladen, da Sie programmgesteuert außerhalb des lokalen Kontexts aufgerufen wurde." | Tritt auf, wenn Inhalt im webkontext versucht, eine Datei programmgesteuert herunterzuladen.  |  
| APPHOST9616: "dieser URI kann keine Geolocation-APIs verwenden.  Geolocation-APIs können nur von einem URI aufgerufen werden, der Teil des Pakets ist oder im ApplicationContentUris-Element des Manifests enthalten ist. " | Weitere Informationen dazu, was im webkontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "dieser URI kann keine Zwischenablage-APIs verwenden.  Die Zwischenablage-APIs können nur von einem URI aufgerufen werden, der Teil des Pakets ist oder im ApplicationContentUris-Element des Manifests enthalten ist. " | Weitere Informationen dazu, was im webkontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "dieser URI kann" Window. Close "nicht verwenden.  Die Window. Close-Methode kann nur aus gepacktem Inhalt aufgerufen werden, der mit einem MS-AppX-URI-Schema geladen wurde. " | Weitere Informationen dazu, was im webkontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "die APP kann nicht zu *URI* navigieren, da eine Seite im webkontext nicht das Dokument der obersten Ebene der APP sein kann.  Laden Sie die Seite stattdessen in einem iframe. " | Sie können nicht auf der Seite auf oberster Ebene zu einer Remote Webseite navigieren, aber Ihre APP kann eine Webseite in einem [iframe][MDNIframe]anzeigen.  Weitere Informationen zum Anzeigen von Remote-Webinhalten finden Sie unter so wird es [gemacht: Verknüpfen mit externen Webseiten][PreviousVersionsWindowsAppsHh780594].  |  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9620: "diese APP wurde geschlossen, weil Sie eine HTTP-Verbindung verwendet hat und das Meta-Element" MS-HTTPS-Connections-only "vorhanden ist.  Nur HTTPS-Verbindungen sind zulässig, wenn Sie das Meta-Element "MS-HTTPS-Connections-only" verwenden.  Verwenden Sie eine HTTPS-Verbindung, oder entfernen Sie das Meta-Element, wenn Sie keine sichere Verbindung benötigen. " | Weitere Informationen finden Sie unter [Vorgehensweise zum Anfordern einer HTTPS-Verbindung][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "die APP konnte die *URL* aufgrund dieses Fehlers nicht beheben: *errorCode*." | Eine häufige Ursache für diesen Fehler ist eine fehlende Datei.  |  
| APPHOST9624: "die APP kann das Skript zum Laden der *URL* -URL nicht verwenden, da die URL eine andere APP startet.  Nur direkte Benutzerinteraktion kann eine andere app starten. " | Apps können keine anderen apps direkt starten.  Andere apps können vom Benutzer gestartet werden, wenn die APP bestimmte Verträge implementiert.  Weitere Informationen finden Sie unter [App-Verträge und Erweiterungen][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Es wurde ein direkter Verweis auf die Ressourcendatei `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` gefunden.  Dieser Verweis verursacht Fehler bei Verwendung außerhalb der Debug-Umgebung. " | Aufgrund des Dateipfad von `logo.scale-140.png` wird diese PNG-Datei als lokalisierte Ressource behandelt, wodurch der Fehler dadurch verursacht wird, dass lokalisierte Ressourcen nicht direkt referenziert werden können.  Weitere Informationen finden Sie unter [globalisieren Ihrer APP (HTML)][PreviousVersionsWindowsAppsHh465006] , wenn Sie diese Datei als Sprachressource verwenden möchten.  Versuchen Sie andernfalls, das problematische Verzeichnis umzubenennen.  |  

## Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "GeoLocator-Klasse | Microsoft docs"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "addPublicLocalApplicationUri-Methode | Microsoft docs"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Anfordern einer HTTPS-Verbindung (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "App-Verträge und-Erweiterungen (Windows-Runtime-Apps) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalisieren Ihrer APP (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Features und Einschränkungen nach Kontext (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "HTML-, CSS-und JavaScript-Features und-Unterschiede (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Link zu externen Webseiten (HTML) | Microsoft docs"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<IFRAME->: das Inline Frame-Element | MDN"  
