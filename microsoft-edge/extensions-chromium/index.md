---
description: Eine Übersicht über das Erstellen und Veröffentlichen von Microsoft Edge (Chromium)-Erweiterungen.
title: Übersicht über Microsoft Edge (Chromium)-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, Erweiterungen entwickeln, Browsererweiterungen, Add-Ons, Partner Center, Entwickler, Chromium-Erweiterungen
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327526"
---
# Übersicht über Microsoft Edge (Chromium)-Erweiterungen  

Eine Erweiterung ist ein kleines Programm, das Sie zum Hinzufügen oder Ändern von Features für Microsoft Edge \(Chromium\) verwenden.  Eine Erweiterung soll die täglichen Browsererfahrungen eines Benutzers verbessern.  Es bietet Nischenfunktionen, die für eine Zielgruppe wichtig sind.  

Sie können eine Erweiterung erstellen, wenn Sie über eine Idee oder ein Produkt verfügen, die auf einer der folgenden Bedingungen basiert.  

*   Ein bestimmter Webbrowser.  
*   Verbesserungen an features von bestimmten Webseiten.  
    
Beispiele für Begleiterfahrungen sind Anzeigenblocker und Kennwortmanager.  

Eine Erweiterung ist ähnlich wie eine normale Web-App strukturiert.  Sie sollte mindestens die folgenden Features enthalten.

*   Eine App-Manifest-JSON-Datei, die grundlegende Plattforminformationen enthält.  
*   Eine JavaScript-Datei, die Funktionalität definiert.  
*   HTML- und CSS-Dateien, die die Benutzeroberfläche definieren.  

Um direkt mit einem Teil des Browsers zu funktionieren, z. B. mit einem Fenster oder einem Tab, müssen Sie API-Anforderungen senden und häufig auf den Namen des Browsers verweisen.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Eine Microsoft Edge-Erweiterung (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Eine Microsoft Edge-Erweiterung \(Chromium\)  
:::image-end:::  

##  <a name="basic-guidance"></a>Grundlegende Orientierungshilfe  

Zu den beliebtesten Browsern zum Erstellen von Erweiterungen gehören Safari, Firefox, Chrome, Opera, Brave und Microsoft Edge.  Sehr gute Ausgangspunkte für die Suche nach Anleitungen für die Erweiterungsentwicklung und Dokumentationen sind von den Browser-Organisationen gehostete Websites.  Die folgende Tabelle ist nicht endgültig und kann als Ausgangspunkt verwendet werden.  

| Webbrowser | Chromium-basiert? | Webseite zur Erweiterungsentwicklung |  
|:--- |:--- |:--- |  
| Safari | Nein | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Nein | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrom | Ja | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Ja | [dev.opera.com/extensions][OperaDevExtensions] |  
| Brave | Ja | Verwendet [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| neuer Microsoft Edge | Ja | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Viele Lernprogramme der Websites verwenden browserspezifische APIs, die möglicherweise nicht mit dem Browser übereinstimmen, für den Sie entwickeln.  In den meisten Fällen funktioniert eine Chromium-Erweiterung in unterschiedlichen Chromium-Browsern auf die gleiche Weise, und die APIs funktionieren erwartungsgemäß.  Nur einige seltener verwendete APIs sind möglicherweise strikt browserspezifisch.  Links zu den Lernprogrammen finden Sie unter [Siehe auch](#see-also).  

##  <a name="why-chromium"></a>Warum Chromium?  

Wenn Sie Ihre Erweiterung im Erweiterungsspeicher für jeden Browser veröffentlichen möchten, muss sie für jede Version so geändert werden, dass sie in jeder unterschiedlichen Browserumgebung ziel- und ausgeführt wird.  Beispielsweise können [Safari-Erweiterungen][AppleDeveloperSafariservicesAppExtensions] sowohl Web- als auch systemeigenen Code verwenden, um mit entsprechenden systemeigenen Anwendungen zu kommunizieren.  Die letzten vier Browser in der vorherigen Tabelle verwenden dasselbe Codepaket und minimieren die Notwendigkeit, parallele Versionen zu verwalten.  Diese Browser basieren auf dem [Open-Source-Projekt Chromium.][|::ref1::|Home]  

Erstellen Sie eine Chromium-Erweiterung, um die geringste Menge an Code zu schreiben.  Es richtet sich auch an die maximale Anzahl von Erweiterungsspeichern und letztendlich an die maximale Anzahl von Benutzern, die Ihre Erweiterung finden und erwerben.  

Im Folgenden geht es hauptsächlich um Chromium-Erweiterungen.  

##  <a name="browser-compatibility-and-extension-testing"></a>Browser-Kompatibilität und Erweiterungstests  

Gelegentlich ist die API-Parität zwischen Chromium-Browsern nicht vorhanden.  So gibt es beispielsweise Unterschiede zwischen den Identitäts- und Zahlungs-APIs.  Um sicherzustellen, dass Ihre Erweiterung die Erwartungen der Kunden erfüllt, überprüfen Sie den API-Status in den folgenden offiziellen Browser-Dokumenten.  

*   [Chrome-APIs][ChromeDeveloperExtensionsApiIndex]  
*   [In Opera unterstützte Erweiterungs-APIs][OperaDevExtensionsApis]  
*   [Port chrome extension to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
Die von Ihnen benötigten APIs definieren die Änderungen, die Sie vornehmen müssen, um die Unterschiede zwischen den einzelnen Browsern zu erkennen.  Dies kann bedeuten, dass Sie für jeden Speicher geringfügig unterschiedliche Codepakete mit kleinen Unterschieden erstellen müssen.  

Um Ihre Erweiterung in verschiedenen Umgebungen zu testen, bevor Sie sie an einen Browserspeicher übermitteln, laden Sie sie während der Entwicklung quer in Ihren Browser.  

##  <a name="publish-your-extension-to-browser-stores"></a>Veröffentlichen Ihrer Erweiterung in Browserstores  

Browsererweiterungen können bei den folgenden Browserstores eingereicht und darin gesucht werden.  

*   [Add-ons für Firefox ][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Opera Add-ons][OperaAddonsExtensions]  
*   [Microsoft Edge Add-ons][MicrosoftEdgeAddonsCategoryExtensions]  

Einige Stores ermöglichen es, gelistete Erweiterungen über andere Browser herunterzuladen.  Der browserübergreifende Zugriff ist jedoch nicht für jeden Store garantiert.  Um sicherzustellen, dass Ihre Benutzer Ihre Erweiterung in verschiedenen Browsern finden, sollten Sie einen Eintrag in jedem Browsererweiterungsspeicher verwalten.  

Benutzer müssen Ihre Erweiterung möglicherweise in verschiedenen Browsern installieren. In diesem Szenario können Sie vorhandene Chromium-Erweiterungen von einem Browser in einen anderen migrieren.  

###  <a name="migrate-an-existing-extension-to-microsoft-edge"></a>Migrieren einer bestehenden Erweiterung zu Microsoft Edge  

Wenn Sie bereits eine Erweiterung für einen anderen Chromium-Browser entwickelt haben, können Sie sie an den Microsoft Edge-Add-Ons-Speicher übermitteln. Sie müssen Ihre Erweiterung nicht umschreiben und überprüfen, ob sie in Microsoft Edge funktioniert.  Wenn Sie eine vorhandene Chromium-Erweiterung zu anderen Chromium-Browsern migrieren, stellen Sie sicher, dass für Ihren Zielbrowser dieselben APIs oder Alternativen verfügbar sind.  

Weitere Informationen zum Portieren Ihrer Chrome-Erweiterung zu Microsoft Edge finden Sie unter Portieren von [Chrome-Erweiterungen zu Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome] Nachdem Sie Ihre Erweiterung auf den Zielbrowser portierst, besteht der nächste Schritt in der Veröffentlichung.  

###  <a name="publish-to-the-microsoft-edge-add-ons-website"></a>Veröffentlichen auf der Microsoft Edge-Add-Ons-Website  

Um mit der Veröffentlichung Ihrer [][MicrosoftDeveloperRegistration] Erweiterung in Microsoft Edge zu beginnen, müssen Sie sich für ein Entwicklerkonto mit einem MSA-E-Mail-Konto registrieren, um Ihren Erweiterungseintrag an den Store zu übermitteln.  Ein MSA-E-Mail-Konto enthält `@outlook.com` `@live.com` , und so weiter.  Wenn Sie eine zu registrierende E-Mail-Adresse auswählen, sollten Sie überlegen, ob Sie den Besitz der Erweiterung an andere Personen in Ihrer Organisation übertragen oder teilen müssen.  Nach Abschluss der Registrierung erstellen Sie eventuell eine neue Erweiterungseinreichung für den Store.  

Um Ihre Erweiterung an den Store zu übermitteln, stellen Sie sicher, dass Sie die folgenden Elemente bereitstellen.  

*   Eine Archivdatei `.zip` \( \), die Ihre Codedateien enthält.  
*   Alle erforderlichen visuellen Ressourcen, die ein Logo und eine kleine Werbekachel enthalten.  
*   Optionale Werbemedien, z. B. Screenshots, Werbekacheln und eine Video-URL.  
*   Informationen, die Ihre Erweiterung beschreiben, z. B. den Namen, eine kurze Beschreibung und einen Link zu Datenschutzrichtlinien.  

> [!NOTE]
> In den verschiedenen Stores gelten möglicherweise unterschiedliche Anforderungen für die Einreichung.  In der obigen Liste sind die [Anforderungen zum Veröffentlichen][ExtensionsChromiumPublish] einer Erweiterung für Microsoft Edge zusammengefasst.  

Nachdem Sie Ihre Erweiterung erfolgreich übermittelt haben, wird ihre Erweiterung einem Überprüfungsprozess unterzogen und besteht den Zertifizierungsprozess entweder durch oder schlägt diesen fehl.  Die Besitzer werden über das Ergebnis und die nächsten Schritte benachrichtigt.  Wenn Sie ein Erweiterungsupdate an den Speicher übermitteln, wird ein neuer Überprüfungsprozess gestartet.  

## <a name="see-also"></a>Weitere Informationen  

*   [Portierung einer Google Chrome-Erweiterung][ExtensionworkshopPorting]  
*   [Erstellen einer Safari-App-Erweiterung][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Ihre erste Erweiterung (Firefox)][MDNWebextensionsYourFirst]  
*   [Lernprogramm "Erste Schritte" (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Erste Schritte (Opera)][OperaDevExtensionsGettingStarted]  
*   [Erste Schritte mit Microsoft Edge (Chromium)-Erweiterungen][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port chrome extension to Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Veröffentlichen einer Erweiterung | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Entwickeln von Erweiterungen für Microsoft Edge | Microsoft-Entwickler"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Microsoft-Entwickler"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Erweiterungen für Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Safari-App-Erweiterungen | Apple-Entwickler"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Erstellen einer Safari-App-Erweiterung | Apple-Entwickler"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Was sind Erweiterungen? | Chrome-Entwickler"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Chrome-APIs | Chrome-Entwickler"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial für die ersten Schritte | Chrome-Entwickler"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portieren einer Google Chrome-Erweiterung | Erweiterungs-Workshop"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Browser-Erweiterungen | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Ihre erste Erweiterung | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Erweiterungen | Firefox Add-ons"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Erweiterungen | Opera-Add-ons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Erweiterungsdokumentation | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "In Opera unterstützten Erweiterungs-APIs | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Erste Schritte | Dev. Opera"  
