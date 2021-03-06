---
description: Fehlercodes für Windows-Runtime-Apps mit JavaScript
title: Fehlercodes für Windows-Runtime-Apps mit JavaScript
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e7241d675a6f488e70eefb20c40149683f965c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398490"
---
# <a name="error-codes-for-windows-runtime-apps-using-javascript"></a>Fehlercodes für Windows-Runtime-Apps mit JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Hier sind die Fehlercodes, die von der Microsoft Visual Studio beim Entwickeln von Windows-Runtime-Apps mit JavaScript angezeigt werden.  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9601: "RemoteURI kann nicht *geladen werden.*  Eine App kann Remotewebinhalte nicht im lokalen Kontext laden." | Weitere Informationen dazu, was im Webkontext zulässig ist, finden Sie unter [Features and restrictions by context][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "'javascript:' ist ein ungültiger Attributwert und wird ignoriert.  Verwenden Sie keine "javascript:"-URIs im lokalen Kontext." | Aus Sicherheitsgründen können Sie keine "javascript:"-URIs im lokalen Kontext verwenden.  Weitere Informationen dazu, was im lokalen Kontext zulässig ist, finden Sie unter [Features und Einschränkungen nach Kontext][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "Das ActiveX-Plug-In mit der Klassen-ID *classID kann*nicht geladen werden.  Apps können keine steuerelemente ActiveX laden." | Windows-Runtime-Apps mit JavaScript unterstützen keine benutzerdefinierten Microsoft ActiveXcontrols.  Wenn Sie ein Benutzeroberflächensteuerelement benötigen, verwenden Sie ein Standardwebsteuerelement, eine Steuerelementbibliothek oder erstellen Sie ein eigenes benutzerdefiniertes Steuerelement.  Wenn Sie eine benutzerdefinierte Logik ausführen müssen, erstellen Sie stattdessen ein benutzerdefiniertes Windows-Runtime-Objekt.  Weitere Informationen zu anderen HTML-, CSS- und JavaScript-Unterschieden finden Sie unter [HTML, CSS und JavaScript-Features und -Unterschiede][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "Kann nicht zu *uri* navigieren, da eine ungültige Zeichencodierung verwendet wird.  Eine App kann nur zu UTF8-codierten Dateien navigieren." | Alle HTML-, JavaScript- und CSS-Dateien, auf die von einer Windows-Runtime zugegriffen wird, müssen als 8-Bit-Unicode-Transformationsformat (UTF-8) codiert werden.  Weitere Informationen zu anderen HTML-, CSS- und JavaScript-Unterschieden finden Sie unter [HTML, CSS und JavaScript-Features und -Unterschiede][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "Von *sourceURI* kann nicht zu *targetURI* navigiert werden, da sich der Ziel-URI in einer höheren Sicherheitszone befindet.  Sie können nicht von einer Zone mit niedrigerer Sicherheit zu einer Zone mit höherer Sicherheit navigieren, es sei denn, Sie navigieren von einem Webkontext-URI zu einem lokalen Kontext-URI, und Sie haben den lokalen Kontext-URI mit der MSApp.addPublicLocalApplicationUri-Methode registriert." | Weitere Informationen finden Sie unter [MSApp.addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: *"URI* kann nicht geladen werden, da eine HTTP-Verbindung verwendet wird und das nur ms-https-connections-meta-Element vorhanden ist.  Nur HTTPS-Verbindungen sind zulässig, wenn Sie das meta-element ms-https-connections-only verwenden.  Verwenden Sie eine HTTPS-Verbindung, oder entfernen Sie das Metaelement, wenn Sie keine sichere Verbindung benötigen." | Weitere Informationen finden Sie unter [How to require an HTTPS connection][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "Die App kann den URI aufgrund dieses Fehlers nicht bei *uri* *starten: failureCode*." | Eine fehlende Ressource oder eine ungültige Datei sind häufige Ursachen für diesen Fehler.  |  
| APPHOST9608: "Die App konnte aufgrund dieses Fehlers nicht zur Seite about:blank navigieren: *errorCode*." |  |  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9610: "Die App hat bei der Vorbereitung der Navigation zu einer benutzerdefinierten Fehlerseite einen Fehler *gefunden: errorCode*." |  |  
| APPHOST9611: "Die App konnte aufgrund dieses Fehlers nicht zu einer benutzerdefinierten Fehlerseite navigieren: *errorCode*." |  |  
| APPHOST9613: "Die App konnte aufgrund dieses Fehlers nicht zu *uri*  navigieren: *errorCode*." |  |  
| APPHOST9614: "Ein Dokument in einem iframe hat den *doc-Modus requestedDocMode* angefordert, aber das System erzwingt den *aktuellenDocMode-Dokumentmodus.*  Der iframe verwendet den *currentDocMode-Dokumentmodus."* | Weitere Informationen zum Anzeigen von Remotewebinhalten finden Sie unter [Link zu externen Webseiten][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: "Die App kann die Datei nicht unter *uri* herunterladen, da sie programmgesteuert außerhalb des lokalen Kontexts aufgerufen wurde." | Tritt auf, wenn Inhalte im Webkontext versuchen, eine Datei programmgesteuert herunterzuladen.  |  
| APPHOST9616: "Dieser URI kann keine Geolocation-APIs verwenden.  Geolocation-APIs können nur von einem URI aufgerufen werden, der Teil des Pakets ist oder im ApplicationContentUris-Element des Manifests enthalten ist." | Weitere Informationen dazu, was im Webkontext zulässig ist, finden Sie unter [Features and restrictions by context][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "Dieser URI kann keine Zwischenablage-APIs verwenden.  Die Zwischenablage-APIs können nur von einem URI aufgerufen werden, der Teil des Pakets ist oder im ApplicationContentUris-Element des Manifests enthalten ist." | Weitere Informationen dazu, was im Webkontext zulässig ist, finden Sie unter [Features and restrictions by context][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "Dieser URI kann window.close nicht verwenden.  Die window.close-Methode kann nur von verpackten Inhalten aufgerufen werden, die mit einem ms-appx-URI-Schema geladen wurden." | Weitere Informationen dazu, was im Webkontext zulässig ist, finden Sie unter [Features and restrictions by context][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "Die App kann nicht zu *uri* navigieren, da eine Seite im Webkontext nicht das Dokument auf oberster Ebene der App sein kann.  Laden Sie stattdessen die Seite in einem iframe." | Sie können ihre Seite auf oberster Ebene nicht zu einer Remotewebseite navigieren, Aber Ihre App kann eine Webseite in einem [iframe anzeigen.][MDNIframe]  Weitere Informationen zum Anzeigen von Remotewebinhalten finden Sie unter [Link zu externen Webseiten][PreviousVersionsWindowsAppsHh780594].  |  

| Fehler | Hinweise |  
|:--- |:--- |  
| APPHOST9620: "Diese App wurde geschlossen, da sie eine HTTP-Verbindung verwendet hat und das nur ms-https-connections-only-Metaelement vorhanden ist.  Nur HTTPS-Verbindungen sind zulässig, wenn Sie das meta-element ms-https-connections-only verwenden.  Verwenden Sie eine HTTPS-Verbindung, oder entfernen Sie das Metaelement, wenn Sie keine sichere Verbindung benötigen." | Weitere Informationen finden Sie unter [How to require an HTTPS connection][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "Die App konnte die *URL* aufgrund dieses Fehlers nicht auflösen: *errorCode*." | Eine häufige Ursache für diesen Fehler ist eine fehlende Datei.  |  
| APPHOST9624: "Die App kann kein Skript zum Laden der *URL* verwenden, da die URL eine andere App startet.  Nur eine direkte Benutzerinteraktion kann eine andere App starten." | Apps können andere Apps nicht direkt starten.  Andere Apps können vom Benutzer gestartet werden, wenn die App bestimmte Verträge implementiert.  Weitere Informationen finden Sie unter [App-Verträge und Erweiterungen][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Ein direkter Verweis auf die `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` Ressourcendatei wurde erkannt.  Diese Referenz verursacht Fehler, wenn sie außerhalb der Debugumgebung verwendet werden." | Aufgrund des Dateipfads von wird diese PNG-Datei als lokalisierte Ressource behandelt, wodurch der Fehler verursacht wird, dass auf lokalisierte Ressourcen nicht direkt `logo.scale-140.png` verwiesen werden kann.  Weitere [Informationen finden Sie unter Globalizing your app (HTML),][PreviousVersionsWindowsAppsHh465006] wenn Sie diese Datei als Sprachressource verwenden möchten.  Andernfalls versuchen Sie, das problematische Verzeichnis umbenennen.  |  

## <a name="see-also"></a>Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Geolocator-Klasse | Microsoft Docs"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "addPublicLocalApplicationUri-Methode | Microsoft Docs"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "So benötigen Sie eine HTTPS-Verbindung (HTML)-| Microsoft Docs"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "App-Verträge und -Erweiterungen (Windows-Runtime-Apps) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalisieren der App (HTML)-| Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Features und Einschränkungen nach Kontext (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "HTML-, CSS- und JavaScript-Features und -Unterschiede (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Verknüpfen mit externen Webseiten (HTML) | Microsoft Docs"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: Das Inlineframe-Element | MDN"  
