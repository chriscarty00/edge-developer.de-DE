---
description: Übersicht über Microsoft Edge-Erweiterungen (Chromium) sowie über das Erstellen und Veröffentlichen von Browsererweiterungen im Allgemeinen.
title: Microsoft Edge-Erweiterungen (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, Erweiterungen entwickeln, Browsererweiterungen, Add-Ons, Partner Center, Entwickler, Chromium-Erweiterungen
ms.openlocfilehash: 85858fc7e1159db3175c3a67c3cfd5f6dfbb448f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104700"
---
# Microsoft Edge-Erweiterungen (Chromium) 

Bei einer Erweiterung handelt es sich um ein kleines Programm, mit dem Sie \(als Entwickler\) neue Funktionen zu Microsoft Edge \(Chromium\) hinzufügen oder vorhandene Funktionalitäten ändern können.  Eine Erweiterung soll die tägliche Browsernutzung verbessern durch die Bereitstellung von Nischenfunktionen, die für ihre Zielgruppen wichtig sind.  

Die Erstellung von Erweiterungen ist sinnvoll, wenn Ihre Idee oder Ihr Produkt von der Verfügbarkeit eines bestimmten Webbrowsers abhängig ist, oder wenn die Browsernutzung verbessert werden soll. Die Funktionen, die Sie bereitstellen möchten, erweitern dabei vorhandene Websites.  Beispiele für ergänzende Funktionen sind Adblocker und Kennwortmanager.  

Eine Erweiterung ist ähnlich wie eine normale Web-App strukturiert.  Sie umfasst mindestens eine JSON-App-Manifestdatei mit grundlegenden Plattforminformationen, eine JavaScript-Datei zum Definieren von Funktionen sowie eine HTML- und eine CSS-Datei, um das Aussehen der Benutzeroberfläche zu bestimmen \(nach Bedarf\).  Um direkt mit einem Teil des Browsers zu funktionieren, z. B. mit einem Fenster oder einem Tab, müssen Sie API-Anforderungen senden und häufig auf den Namen des Browsers verweisen.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Eine Microsoft Edge-Erweiterung (Chromium)":::
  Eine Microsoft Edge-Erweiterung \(Chromium\)  
:::image-end:::  

## Grundlegende Orientierungshilfe  

Zu den am häufigsten verwendeten Browsern gehören Safari, Firefox, Chrome, Opera, Brave und Microsoft Edge.  Sehr gute Ausgangspunkte für die Suche nach Anleitungen für die Erweiterungsentwicklung und Dokumentationen sind von den Browser-Organisationen gehostete Websites.  Die folgende Tabelle ist nicht endgültig. Verwenden Sie sie bitte als hilfreichen Ausgangspunkt.  

| Webbrowser | Chromium-basiert? | Homepage Erweiterungsentwicklung |  
|:--- |:--- |:--- |  
| Safari | Nein | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Nein | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrom | Ja | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Ja | [dev.opera.com/extensions][OperaDevExtensions] |  
| Brave | Ja | Verwendet [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| neuer Microsoft Edge | Ja | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> In vielen Anleitungen auf diesen Websites werden browserspezifische APIs verwendet, die möglicherweise nicht mit dem Browser übereinstimmen, für den Sie die Erweiterung entwickeln möchten.  In den meisten Fällen funktioniert eine Chromium-Erweiterung in unterschiedlichen Chromium-Browsern auf die gleiche Weise, und die APIs funktionieren erwartungsgemäß.  Nur einige seltener verwendete APIs sind möglicherweise strikt browserspezifisch.  Links zu den Anleitungen finden Sie unter [Weitere Informationen](#see-also).  

## Warum Chrom?

Wenn Sie die Erweiterung in so vielen Browser-Erweiterungsstores wie möglich veröffentlichen möchten, muss sie für mehrere Versionen geändert werden, um an jede einzelne Browserumgebung angepasst und darin ausgeführt werden zu können.  [Safari-Erweiterungen][AppleDeveloperSafariservicesAppExtensions] können, im Gegensatz zu anderen Erweiterungstypen, sowohl Web- als auch systemeigenen Code für die Kommunikation mit den jeweiligen systemeigenen Anwendungen nutzen.  [Firefox-Erweiterungen][MDNWebextensions] haben mehr mit den anderen Erweiterungstypen gemeinsam, es gibt jedoch auch einige [Unterschiede][ExtensionworkshopPorting], die berücksichtigt werden müssen.  Allerdings gibt es eine gute Nachricht. Die letzten vier Browser in der Liste oben sind in der Lage, das selbe Codepaket zu nutzen, und minimieren die Notwendigkeit zum Ändern und Verwalten paralleler Versionen.  Das liegt daran, dass die Browser auf dem [Chromium-Open-Source-Projekt][|::ref1::|Home] basieren.  

Wenn Sie eine Chromium-Erweiterung erstellen, können Sie die geringste Menge an Code schreiben und die Anzahl der Erweiterungsstores maximieren, die Sie interessieren, und damit letztlich die Anzahl der Benutzer, die Ihre Erweiterung finden und erwerben können.  

Im Folgenden geht es hauptsächlich um Chromium-Erweiterungen.  

## Browser-Kompatibilität und Erweiterungstests  

Gelegentlich ist keine API-Übereinstimmung zwischen Chromium-Browsern gegeben.  So gibt es beispielsweise Unterschiede zwischen den Identitäts- und Zahlungs-APIs.  Um sicherzustellen, dass Ihre Erweiterung den Kundenerwartungen entspricht, überprüfen Sie den API-Status über eine offizielle Browserdokumentation wie [Chrome-APIs][ChromeDeveloperExtensionsApiIndex], [in Opera unterstützte Erweiterungs-APIs][OperaDevExtensionsApis] und [Portieren einer Chrome-Erweiterung nach Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].  

Je nach den erforderlichen APIs können diese Unterschiede dazu führen, dass Sie geringfügig unterschiedliche Codepakete für die einzelnen Stores erstellen müssen.  

Während der Entwicklung Ihrer Erweiterung können Sie sie in Ihrem Browser querladen, um sie in unterschiedlichen Umgebungen zu testen, bevor Sie sie an Browserstores übermitteln.  

## Veröffentlichen Ihrer Erweiterung in Browserstores  

Browsererweiterungen können bei den folgenden Browserstores eingereicht und darin gesucht werden.  

*   [Add-ons für Firefox ][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Opera Add-ons][OperaAddonsExtensions]  
*   [Microsoft Edge Add-ons][MicrosoftEdgeAddonsCategoryExtensions]  

Einige Stores ermöglichen es, gelistete Erweiterungen über andere Browser herunterzuladen.  Durch das Herunterladen über einen anderen Browser wird der Vorabaufwand für Sie \(als Entwickler\) u. U. verringert, und es fällt die Notwendigkeit der Übermittlung an weitere Stores weg, wenn Benutzer auf bestehende Storeeinträge über verschiedene Browser zugreifen können.  Der browserübergreifende Zugriff ist jedoch nicht für jeden Store garantiert.  Um sicherzustellen, dass Ihre Benutzer Ihre Erweiterung über unterschiedliche Browser finden können, sollten Sie einen Eintrag in jedem Browsererweiterungsstore vornehmen.  

Eine Erweiterung kann sich überschneidende Zielgruppen aufweisen, die häufig mehrere Browser verwenden. Sie könnten aber auch feststellen, dass Ihre Erweiterung an eine zuvor nicht berücksichtigte Zielgruppe gerichtet sein sollte.  Hierfür können bestehende Chromium-Erweiterungen von einem Browser zu einem anderen migriert werden.  

### Migrieren einer bestehenden Erweiterung zu Microsoft Edge  

Wenn Sie bereits eine Erweiterung für einen anderen Chromium-Browser entwickelt haben und diese dann für Microsoft Edge anbieten möchten, müssen Sie sie nicht neu schreiben.  Die Migration bestehender Chromium-Erweiterungen zu anderen Chromium-Browsern ist ganz einfach, solange die verwendeten APIs in unterschiedlichen Browsern verfügbar sind oder es andere APIs mit der erforderlichen Funktionalität gibt.  

Weitere Informationen zum Portieren Ihrer Chrome-Erweiterung finden Sie unter [Portieren einer Chrome-Erweiterung nach Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].  Sobald Sie die Erweiterung in den Zielbrowser portiert haben, besteht der nächste Schritt darin, sie zu veröffentlichen.  

### Veröffentlichen auf der Microsoft Edge Add-ons-Website  

Für die Veröffentlichung Ihrer Erweiterung für Microsoft Edge müssen Sie sich zunächst mit einem MSA-E-Mail-Konto \(@outlook.com, @live.com usw.\) [für ein Entwicklerkonto registrieren][MicrosoftDeveloperRegistration], um Ihren Erweiterungseintrag im Store einreichen zu können.  Bei der Auswahl der E-Mail-Adresse für die Registrierung sollten Sie berücksichtigen, ob Sie den Besitz der Erweiterung mit anderen Personen in Ihrer Organisation übertragen oder teilen müssen.  Nach Abschluss der Registrierung erstellen Sie eventuell eine neue Erweiterungseinreichung für den Store.  

Um die Erweiterung einreichen zu können, müssen Sie die folgenden Voraussetzungen erfüllen.  

*   Eine Archivdatei \(ZIP-Datei\), die Ihre Codedateien enthält.  
*   Alle erforderlichen visuellen Ressourcen, einschließlich eines Logos und einer kleinen Werbekachel.  
*   Optionale Werbemittel, z. B. Screenshots, größere Werbekacheln, eine URL oder eine beliebige Kombination zu Videos Ihrer Erweiterung.  
*   Informationen zu Ihrer Erweiterung, z. B. den Namen, eine kurze Beschreibung, eine lange Beschreibung und einen Link zu Ihrer Datenschutzerklärung.  

> [!NOTE]
> In den verschiedenen Stores gelten möglicherweise unterschiedliche Anforderungen für die Einreichung.  In der obigen Liste sind die [Anforderungen][ExtensionsChromiumPublish] für die Veröffentlichung einer Erweiterung für Microsoft Edge zusammengefasst.  

Nachdem Sie Ihre Erweiterung eingereicht haben, wird sie im Rahmen eines Zertifizierungsprozesses überprüft und entweder angenommen oder abgelehnt.  Die Besitzer werden über das Ergebnis und die nächsten Schritte benachrichtigt.  Wenn Sie eine aktualisierte Erweiterung für den Store einreichen, einschließlich aktualisierter Informationen zu dem Erweiterungseintrag, wird ein neuer Überprüfungsprozess gestartet.  

## Weitere Informationen  

*   [Portieren einer Google Chrome-Erweiterung][ExtensionworkshopPorting]  
*   [Erstellen einer Safari-App-Erweiterung][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Ihre erste Erweiterung (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial für die ersten Schritte (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Erste Schritte (Opera)][OperaDevExtensionsGettingStarted]  
*   [Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md &quot;Portieren einer Chrome-Erweiterung nach Microsoft Edge (Chromium) | Microsoft Docs&quot;  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md &quot;Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs&quot;  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md &quot;Veröffentlichen einer Erweiterung | Microsoft Docs&quot;  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions &quot;Entwickeln von Erweiterungen für Microsoft Edge | Microsoft-Entwickler&quot;  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration &quot;Partner Center | Microsoft-Entwickler&quot;  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions &quot;Erweiterungen für Microsoft Edge | Microsoft Edge&quot;  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions &quot;Safari-App-Erweiterungen | Apple-Entwickler&quot;  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension &quot;Erstellen einer Safari-App-Erweiterung | Apple-Entwickler&quot;  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions &quot;Was sind Erweiterungen? | Chrome-Entwickler&quot;  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index &quot;Chrome-APIs | Chrome-Entwickler&quot;  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted &quot;Tutorial für die ersten Schritte | Chrome-Entwickler&quot;  

[ChromiumHome]: https://www.chromium.org/Home &quot;Chromium&quot;  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension &quot;Portieren einer Google Chrome-Erweiterung | Erweiterungs-Workshop&quot;  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions &quot;Erweiterungen | Chrome Web Store&quot;  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions &quot;Browser-Erweiterungen | MDN&quot;  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension &quot;Ihre erste Erweiterung | MDN&quot;  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions &quot;Erweiterungen | Firefox Add-ons&quot;  

[OperaAddonsExtensions]: https://addons.opera.com/extensions &quot;Erweiterungen | Opera-Add-ons&quot;  

[OperaDevExtensions]: https://dev.opera.com/extensions &quot;Dokumentation zu Erweiterungen | Dev.Opera&quot;  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis &quot;In Opera unterstützte Erweiterungs-APIs | Dev.Opera&quot;  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started &quot;Erste Schritte | Dev.Opera"  
