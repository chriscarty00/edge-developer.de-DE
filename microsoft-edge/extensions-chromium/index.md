---
description: Die Übersicht über die Microsoft Edge-Erweiterungen (Chrom) sowie das Erstellen und Veröffentlichen von Browsererweiterungen im Allgemeinen.
title: Microsoft Edge (Chrom)-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler, Chrom-Erweiterungen
ms.openlocfilehash: 2c4c34805e93bf6fbae57f1d0230cc821d1f3f65
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684699"
---
# Microsoft Edge (Chrom)-Erweiterungen  

Eine Erweiterung ist ein kleines Programm, das Sie (der Entwickler \) verwenden können, um neue Features zu Microsoft Edge \ (Chrom \) hinzuzufügen oder die vorhandene Funktionalität zu ändern.  Eine Erweiterung dient dazu, den Alltag des Nutzers zu verbessern, indem eine Nische Funktionalität bereitgestellt wird, die für Zielgruppen wichtig ist.  

Sie können Erweiterungen erstellen, wenn Ihre Idee oder Ihr Produkt von der Verfügbarkeit eines bestimmten Webbrowsers abhängt oder die Browserumgebung erweitert, in der die Funktionalität, die Sie bereitstellen möchten, vorhandene Websites erweitert.  Beispiele für Begleit Erfahrungen sind das Hinzufügen von Administratoren und Kenn Wort Managern.  

Eine Erweiterung ist ähnlich wie eine normale Web-App strukturiert.  Sie umfasst mindestens eine JSON-App-Manifestdatei, die grundlegende Plattforminformationen, eine JavaScript-Datei zum Definieren von Funktionen sowie eine HTML-und CSS-Datei enthält, um das Aussehen der Benutzeroberfläche zu ermitteln \ (nach Bedarf \).  Wenn Sie direkt mit einem Teil des Browsers arbeiten möchten, beispielsweise einem Fenster oder einer Registerkarte, müssen Sie API-Anforderungen senden und häufig auf den Browser nach Namen verweisen.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Eine Microsoft Edge (Chrom)-Erweiterung":::
  Eine Microsoft Edge \ (Chrom \)-Erweiterung  
:::image-end:::  

## Grundlegende Anleitungen  

Zu den am häufigsten verwendeten Browsern gehören Safari, Firefox, Chrome, Opera, Brave und Microsoft Edge.  Großartige Orte zum beginnen der Erweiterungs Entwicklung Tutorials und Dokumentations Recherchen sind Websites, die von den Browser Organisationen gehostet werden.  Die folgende Tabelle ist nicht endgültig, bitte verwenden Sie Sie als hilfreichen Ausgangspunkt.  

| Webbrowser | Chrom basiert? | Homepage der Erweiterungs Entwicklung |  
|:--- |:--- |:--- |  
| Safari | Nein | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Nein | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrom | Ja | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Oper | Ja | [dev.opera.com/extensions][OperaDevExtensions] |  
| Mutig | Ja | Verwendet [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| neuer Microsoft Edge | Ja | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Viele der Lernprogramme der Websites verwenden browserspezifische APIs, die möglicherweise nicht mit dem Browser übereinstimmen, für den Sie sich entwickeln.  In den meisten Fällen funktioniert eine Chrom-Erweiterung wie in verschiedenen Chrom-Browsern, und die APIs funktionieren wie erwartet.  Nur einige seltener verwendete APIs sind möglicherweise strikt browserspezifisch.  Links zu den Lernprogrammen finden Sie unter [Siehe auch](#see-also).  

## Warum Chrom  

Wenn Sie Ihre Erweiterung in möglichst vielen Browser Erweiterungs speichern veröffentlichen möchten, muss Sie für mehrere Versionen geändert werden, damit Sie in jeder unterschiedlichen Browserumgebung ausgerichtet und ausgeführt werden können.  [Safari-Erweiterungen][AppleDeveloperSafariservicesAppExtensions]können im Gegensatz zu anderen Erweiterungstypen sowohl Web-als auch systemeigenen Code nutzen, um mit systemeigenen Anwendungen zu kommunizieren.  [Firefox-Erweiterungen][MDNWebextensions] haben mehr gemeinsam mit den anderen Erweiterungstypen, aber es gibt auch einige [Unterschiede][ExtensionworkshopPorting] , die Sie in den Blick nehmen sollten.  Allerdings gibt es einige gute Neuigkeiten; die letzten vier Browser in der obigen Tabelle sind in der Lage, dasselbe Code Paket zu nutzen und die Anforderung zum Ändern und verwalten paralleler Versionen zu minimieren.  Das liegt daran, dass die Browser auf dem [Chromium Open-Source-Projekt][|::ref1::|Home]basieren.  

Durch das Erstellen einer Chrom Erweiterung können Sie die geringste Menge an Code schreiben, um die Anzahl der Erweiterungsspeicher, auf die Sie Zielen, zu maximieren, und letztendlich die Anzahl der Benutzer, die ihre Erweiterung finden und erwerben können.  

Die folgenden Inhalte konzentrieren sich hauptsächlich auf Chrom-Erweiterungen.  

## Browser Kompatibilität und Erweiterungs Tests  

Gelegentlich gibt es keine API-Parität zwischen Chrom-Browsern.  Beispielsweise gibt es Unterschiede bei den Identitäts-und Zahlungs-APIs.  Um sicherzustellen, dass Ihre Erweiterung die Erwartungen der Kunden erfüllt, überprüfen Sie die API-Status über die offizielle Browserdokumentation, wie etwa [Chrome-APIs][ChromeDeveloperExtensionsApiIndex], [in Opera Unterstützte Erweiterungs-APIs][OperaDevExtensionsApis]und [Port Chrome-Erweiterung zu Microsoft (Chrom) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  

Je nach den von Ihnen benötigten APIs können diese Unterschiede bedeuten, dass Sie etwas andere Code Pakete mit kleinen Unterschieden im Code für die einzelnen Stores erstellen müssen.  

Wenn Sie Ihre Erweiterung entwickeln, können Sie Sie in Ihrem Browser querladen, um Sie in verschiedenen Umgebungen zu testen, bevor Sie Ihre Erweiterung an Browser Speicher übermitteln.  

## Veröffentlichen der Erweiterung für Browser Speicher  

Sie können Browser-Erweiterungen in den folgenden Browser-Stores einreichen und suchen.  

*   [Firefox-Browser-Add-ons][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Opera-Addons][OperaAddonsExtensions]  
*   [Microsoft Edge-Add-ons][MicrosoftEdgeAddonsCategoryExtensions]  

In einigen Stores können Sie aufgelistete Erweiterungen von anderen Browsern herunterladen.  Wenn Sie von einem anderen Browser herunterladen, können Sie möglicherweise \ (der Entwickler \) den Aufwand im Voraus speichern und die Anforderung zum einreichen an weitere Speicher entfernen, wenn Benutzer zu den vorhandenen Store-Einträgen in verschiedenen Browsern navigieren können.  Der browserübergreifende Zugriff wird jedoch nicht durch Browser Speicher gewährleistet.  Um sicherzustellen, dass die Benutzer ihre Erweiterung in verschiedenen Browsern finden können, sollten Sie einen Eintrag in jedem Browser Erweiterungsspeicher verwalten.  

Eine Erweiterung hat möglicherweise überlappende Zielgruppen, die häufig mehrere Browser verwenden, oder Sie können feststellen, dass Sie auf eine Zielgruppe ausgerichtet sein sollte, die nicht zuvor vorhanden ist.  Damit dies möglich ist, können vorhandene Chrom Erweiterungen von einem Browser zu einem anderen migriert werden.  

### Migrieren einer vorhandenen Erweiterung zu Microsoft Edge  

Wenn Sie bereits eine Erweiterung für einen anderen Chromium-Browser entwickelt haben und dies anbieten und sicherstellen möchten, dass Sie über Microsoft Edge funktioniert, müssen Sie Ihre Erweiterung nicht neu schreiben.  Das Migrieren vorhandener Chrom-Erweiterungen zu anderen Chrom-Browsern ist unkompliziert, solange die von Ihnen verwendeten APIs in verschiedenen Browsern verfügbar sind oder andere APIs vorhanden sind, die die erforderliche Funktionalität bereitstellen.  

Weitere Informationen zum Portieren ihrer Chrome-Erweiterung finden Sie unter [Port Chrome Extensions to Microsoft (Chrom) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  Nachdem Sie Ihre Erweiterung in den Zielbrowser portiert haben, besteht der nächste Schritt darin, Sie zu veröffentlichen.  

### Veröffentlichen auf der Microsoft Edge-Add-ons-Website  

Um mit der Veröffentlichung ihrer Erweiterung zu Microsoft Edge zu beginnen, müssen Sie sich [für ein Entwicklerkonto][MicrosoftDeveloperRegistration] mit einem MSA-e-Mail-Konto registrieren \ (@Outlook. com, @Live. com usw. \), um den Eintrag für die Erweiterung im Store zu übermitteln.  Wenn Sie eine e-Mail-Adresse für die Registrierung auswählen, sollten Sie berücksichtigen, ob Sie den Besitz der Erweiterung mit anderen Personen in Ihrer Organisation übertragen oder teilen müssen.  Nachdem die Registrierung abgeschlossen ist, können Sie eine neue Übermittlungserweiterung an den Store erstellen.  

Um Ihre Durchwahl an den Store zu übermitteln, müssen Sie die folgenden Voraussetzungen erfüllen.  

*   Eine Archiv-Datei (. zip), die ihre Codedateien enthält.  
*   Alle erforderlichen visuellen Ressourcen, einschließlich eines Logos und einer kleinen Werbe Kachel.  
*   Optionale Werbemittel wie Screenshots, größere Werbe Kacheln, eine URL oder eine beliebige Kombination mit Videos ihrer Erweiterung.  
*   Informationen, die ihre Erweiterung beschreiben, wie Name, Kurzbeschreibung, lange Beschreibung und ein Link zu ihren Datenschutzrichtlinien.  

> [!NOTE]
> Unterschiedliche Speicher können unterschiedliche Übermittlungsanforderungen aufweisen.  In der obigen Liste sind die [Voraussetzungen][ExtensionsChromiumPublish] für die Veröffentlichung einer Erweiterung von Microsoft Edge zusammengefasst.  

Nachdem Sie den Übermittlungsvorgang abgeschlossen haben, wird Ihre Erweiterung überprüft, und entweder wird der Zertifizierungsprozess erfolgreich durchlaufen oder fehlgeschlagen.  Besitzer werden über das Ergebnis informiert und geben die nächsten Schritte nach Bedarf an.  Wenn Sie eine aktualisierte Erweiterung an den Store übermitteln, einschließlich Updates für die Details zur Erweiterung, wird ein neuer Überprüfungsprozess gestartet.  

## Weitere Informationen  

*   [Portieren einer Google Chrome-Erweiterung][ExtensionworkshopPorting]  
*   [Erstellen einer Safari-App-Erweiterung][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Ihre erste Durchwahl (Firefox)][MDNWebextensionsYourFirst]  
*   [Lernprogramm "erste Schritte" (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Erste Schritte (Opera)][OperaDevExtensionsGettingStarted]  
*   [Erste Schritte mit Microsoft Edge (Chrom)-Erweiterungen][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port Chrome-Erweiterung zu Microsoft (Chrom) Edge | Microsoft docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Erste Schritte mit Microsoft Edge (Chrom)-Erweiterungen | Microsoft docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Veröffentlichen einer Erweiterung | Microsoft docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Entwickeln von Erweiterungen für Microsoft Edge | Microsoft-Entwickler"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Microsoft-Entwickler"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Erweiterungen für Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Safari-App-Erweiterungen | Apple-Entwickler"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Erstellen einer Safari-App-Erweiterung | Apple-Entwickler"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Was sind Erweiterungen? | Chrome-Entwickler"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Chrome-APIs | Chrome-Entwickler"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Lernprogramm für erste Schritte | Chrome-Entwickler"  

[ChromiumHome]: https://www.chromium.org/Home "Chrom"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portieren einer Google Chrome-Erweiterung | Erweiterungs Werkstatt"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Browser Erweiterungen | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Ihre erste Erweiterung | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Erweiterungen | Firefox Add-ons"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Erweiterungen | Opera-Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Erweiterungen-Dokumentation | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "In Opera Unterstützte Erweiterungs-APIs | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Erste Schritte | Dev. Opera"  
