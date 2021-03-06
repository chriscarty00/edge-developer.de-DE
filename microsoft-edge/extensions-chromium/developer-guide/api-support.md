---
description: Liste der unterstützten APIs, die beim Erstellen von Microsoft Edge-Erweiterungen verwendet werden.
title: Unterstützte APIs für Microsoft Edge-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, extensions development, browser extensions, add-ons, extension api , developer, web development
ms.openlocfilehash: 20e924b5c973b9ecd433feeb3a772c6d17746369
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398105"
---
# <a name="supported-apis-for-microsoft-edge-extensions"></a>Unterstützte APIs für Microsoft Edge-Erweiterungen

Die folgende Tabelle enthält eine Liste der APIs, die Sie beim Erstellen von Erweiterungen für den Microsoft Edge \(Chromium\)-Browser verwenden können.

| API                                   | Beschreibung                                            
|---------------------------------------|----------------------------------------------------------|
| [Wecker](https://developer.chrome.com/extensions/alarms) | Planen Sie, dass Code regelmäßig oder zu einem bestimmten Zeitpunkt in der Zukunft ausgeführt wird. |
| [Lesezeichen](https://developer.chrome.com/extensions/bookmarks) | Erstellen, Organisieren und Bearbeiten von Lesezeichen. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Verwenden Sie Browseraktionen, um Symbole auf der Symbolleiste in Microsoft Edge zu platzieren. Sie können auch Browseraktionen verwenden, um eine QuickInfo, ein Signal oder ein Popup hinzuzufügen. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Entfernen von Browserdaten aus dem lokalen Profil eines Benutzers. |
| [Befehle](https://developer.chrome.com/extensions/commands) | Fügen Sie Tastenkombinationen hinzu, die Aktionen in Ihrer Erweiterung auslösen. Beispielsweise eine Aktion zum Öffnen des Browsers oder Senden eines Befehls an die Erweiterung. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | Im Allgemeinen können Sie mit Inhaltseinstellungen das Verhalten von Microsoft Edge auf jeder Website anstatt global anpassen. Ändern Sie Einstellungen, die steuern, ob Websites Features wie Cookies, JavaScript und Plug-Ins verwenden können. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Fügen Sie dem Kontextmenü in Microsoft Edge Elemente hinzu. Menüelemente können auf verschiedene Objekte angewendet werden, z. B. Bilder, Hyperlinks und Seiten. |
| [Cookies](https://developer.chrome.com/extensions/cookies) | Abfragen und Ändern von Cookies und Empfangen von Benachrichtigungen, wenn sie sich ändern. |
| [debugger](https://developer.chrome.com/extensions/debugger) | Fügen Sie eine oder mehrere Registerkarten an, um die Netzwerkinteraktion zu instrumentieren, JavaScript zu debuggen, das DOM zu ändern, CSS zu ändern und so weiter. Verwenden Sie die debugger tabId, um Registerkarten mit sendCommand als Ziel zu verwenden, und routen Sie Ereignisse nach tabId von onEvent-Rückrufen. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Ergreifen Sie Aktionen abhängig vom Inhalt einer Seite, ohne die Berechtigung zum Lesen des Seiteninhalts zu benötigen. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Bietet mehr Datenschutz, indem Netzwerkanforderungen blockiert oder geändert werden, indem deklarative Regeln angegeben werden. Zulassen, dass Erweiterungen Netzwerkanforderungen ändern, ohne die Anforderung abzufangen und den Inhalt anzuzeigen. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Erfassen sie den Inhalt eines Bildschirms, einzelner Fenster oder Registerkarten. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interagieren mit dem überprüften Fenster.  Rufen Sie beispielsweise die Registerkarten-ID von Seiten ab, werten Sie Code aus, aktualisieren Sie Seiten, oder rufen Sie Ressourcen auf einer Seite ab. |
| [devtools.network](https://developer.chrome.com/extensions/devtools_network) | Abrufen von Informationen zu Netzwerkanforderungen, die von den Entwicklertools im Netzwerkbereich angezeigt werden. |
| [devtools.panels](https://developer.chrome.com/extensions/devtools.panels) | Integrieren Sie Ihre Erweiterung in die Benutzeroberfläche des Entwicklertools-Fensters, indem Sie eigene Panels erstellen, auf vorhandene Panels zugreifen oder Seitenleisten hinzufügen. |
| [Downloads](https://developer.chrome.com/extensions/downloads) | Programmgesteuert starten, überwachen, bearbeiten und suchen Sie nach Downloads. |
| [enterprise.hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Hier erhalten Sie den Hersteller und das Modell der Hardwareplattform, auf der der Browser ausgeführt wird. Diese API ist nur für Durch die Unternehmensrichtlinie installierte Erweiterungen verfügbar. |
| [Ereignisse](https://developer.chrome.com/extensions/events) | Häufige Typen, die von APIs verwendet werden, die Ereignisse zur Benachrichtigung beim Auftreten eines interessanten Ereignisses anfingen. |
| [erweiterung](https://developer.chrome.com/extensions/extension) | Jede Erweiterungsseite kann die Hilfsprogramme dieser API verwenden. Es umfasst Unterstützung für den Austausch von Nachrichten zwischen Erweiterungen und Inhaltsskripts, die unter Message Passing beschrieben wird. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Enthält Typdeklarationen für Microsoft Edge-Erweiterungen. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Verwalten von Schriftarteinstellungen in Microsoft Edge. |
| [Verlauf](https://developer.chrome.com/extensions/history) | Interagieren Sie mit dem Browserdatensatz der besuchten Seiten. Sie können URLs im Browserverlauf hinzufügen, entfernen oder abfragen. Um die Verlaufsseite mit Ihrer eigenen Version zu überschreiben, navigieren Sie zu Seiten außer Kraft setzen. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implementieren Sie die Internationalisierung in Ihrer gesamten App oder Erweiterung. |
| [Leerlauf](https://developer.chrome.com/extensions/idle) | Erkennen, wann sich der Leerlaufzustand des Computers ändert. |
| [Verwaltung](https://developer.chrome.com/extensions/management) | Verwalten Sie die Liste der installierten oder ausgeführten Erweiterungen. Es ist nützlich für Erweiterungen, die die integrierte Seite Neue Registerkarte überschreiben. |
| [Benachrichtigungen](https://developer.chrome.com/extensions/notifications) | Erstellen Sie umfangreiche Benachrichtigungen mithilfe von Vorlagen, und zeigen Sie sie im Systemfach an. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Registrieren Sie Schlüsselwörter in der Microsoft Edge-Adressleiste, auch bekannt als "Omnibox". |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Fügen Sie der Microsoft Edge-Symbolleiste rechts neben der Adressleiste Symbole hinzu. Seitenaktionen sind Aktionen, die auf der aktuellen Seite ergriffen werden können und nicht auf alle Seiten anwendbar sind. Seitenaktionen werden ausgegraut angezeigt, wenn sie inaktiv sind. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Speichern Sie Registerkarten als MHTML-Dateien.|
| [permissions](https://developer.chrome.com/extensions/permissions) | Rufen Sie deklarierte, optionale Berechtigungen zur Laufzeit statt zur Installationszeit ab. Sie können diese API verwenden, um den Benutzern die erforderlichen und genehmigten Berechtigungen zu zeigen. |
| [Ein/Aus](https://developer.chrome.com/extensions/power) | Überschreiben Sie die Energieverwaltungsfeatures des Systems. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Verwenden Sie Ereignisse zum Abfragen von Druckern, deren Funktionen und zum Übermitteln von Druckaufträgen. |
| [Datenschutz](https://developer.chrome.com/extensions/privacy) | Steuern von Features in Microsoft Edge, die sich auf den Datenschutz eines Benutzers auswirkt. Diese API hängt vom Prototyp ab, um die Konfiguration `EdgeSetting` von Microsoft Edge zu erhalten und zu `types` festlegen. |
| [proxy](https://developer.chrome.com/extensions/proxy) | Verwalten von Proxyeinstellungen für Microsoft Edge. Diese API hängt vom Prototyp der API ab, um die Proxykonfiguration von Microsoft Edge zu erhalten und `EdgeSetting` `types` zu festlegen. |
| [runtime](https://developer.chrome.com/extensions/runtime) | Rufen Sie die Hintergrundseite ab, geben Sie Details zum Manifest zurück, und lauschen Und reagieren Sie auf Ereignisse im App- oder Erweiterungslebenszyklus. Sie können auch den relativen Pfad von URLs in vollqualifizierte URLs konvertieren. |
| [sessions](https://developer.chrome.com/extensions/sessions) | Abfragen und Wiederherstellen von Registerkarten und Fenstern aus einer Browsersitzung. |
| [Speicher](https://developer.chrome.com/extensions/storage) | Speichern, Abrufen und Nachverfolgen von Änderungen an Benutzerdaten. |
| [system.memory](https://developer.chrome.com/extensions/system_memory) | Die `system.memory` API. |
| [system.storage](https://developer.chrome.com/extensions/system_storage) | Abfragen von Informationen zu Speichergeräten. Sie können auch Benachrichtigungen empfangen, wenn Speichergeräte angeschlossen oder getrennt sind. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interagieren mit Registerkartenmedienstreams. |
| [Registerkarten](https://developer.chrome.com/extensions/tabs) | Interagieren Sie mit dem Registerkartensystem des Browsers, um Registerkarten zu erstellen, zu ändern und neu anordnen zu können. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Greifen Sie auf die wichtigsten Websites zu, die auch als am häufigsten besuchte Websites bezeichnet werden, die auf der neuen Registerkartenseite angezeigt werden. Diese Websites enthalten keine vom Benutzer angepassten Verknüpfungen. |
| [tts](https://developer.chrome.com/extensions/tts) | Wiedergabe von synthetisiertem Text-zu-Sprache(TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implementieren Sie ein Text-zu-Sprache-Modul (Text-to-Speech) mithilfe einer Erweiterung. Erweiterungen, die sich für die Verwendung dieser API registrieren, empfangen Ereignisse, die zu sprechende Sprechaussprechungen und andere Parameter enthalten. Erweiterungen können dann jede verfügbare Webtechnologie verwenden, um Sprache zu synthetisieren und ausausgaben und Ereignisse an die aufrufende Funktion zurücksennen, um den Status zu melden. |
| [Typen](https://developer.chrome.com/extensions/types) | Geben Sie Deklarationen für Microsoft Edge ein. |
| [webNavigation](https://developer.chrome.com/extensions/webNavigation) | Empfangen von Benachrichtigungen über den Status von Navigationsanforderungen. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Beobachten und Analysieren des Datenverkehrs. Abfangen, Blockieren oder Ändern von Anforderungen. |
| [windows](https://developer.chrome.com/extensions/windows) | Interagieren Sie mit Browserfenstern, um Fenster im Browser zu erstellen, zu ändern und neu anordnen zu können. |



## <a name="unsupported-extension-apis"></a>Nicht unterstützte Erweiterungs-APIs

Microsoft Edge unterstützt die folgenden Erweiterungs-APIs nicht:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` – Alternativ können Sie ein OAuth2-Token zum Authentifizieren `launchWebAuthFlow` von Benutzern abrufen.
* `chrome.instanceID`.


## <a name="additional-considerations-for-supported-apis"></a>Zusätzliche Überlegungen zu unterstützten APIs

* Der Benutzer muss mit einem MSA- oder Azure Active Directory-Konto bei Microsoft Edge angemeldet sein, um zu `chrome.identity.getProfileUserInfo` verwenden. Wenn der Benutzer mit einem lokalen Active Directory-Konto bei Microsoft Edge angemeldet ist, gibt die API die E-Mail- und `null` ID-Werte zurück.

* Microsoft Edge unterstützt keine Erweiterungen, die Chrome Web Store-Zahlungen verwenden, da es zum Anfordern von `identity.getAuthtoken` Token für angemeldete Benutzer verwendet wird. Diese Token werden an die REST-basierte Lizenzierungs-API gesendet. 


<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/apps/external_extensions).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
