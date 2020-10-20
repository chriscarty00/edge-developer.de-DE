---
description: Liste der unterstützten APIs, die beim Erstellen von Microsoft Edge-Erweiterungen verwendet werden.
title: Unterstützte APIs für Microsoft Edge-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Add-ons, Erweiterungs-API, Entwickler, Web-Entwicklung
ms.openlocfilehash: 868473393da6cefbf146fb7acd6c9816903bd253
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120392"
---
# Unterstützte APIs für Microsoft Edge-Erweiterungen

Die folgende Tabelle enthält eine Liste der APIs, die Sie beim Erstellen von Erweiterungen für den Microsoft Edge \ (Chromium \)-Browser verwenden können.

| API                                   | Beschreibung                                            
|---------------------------------------|----------------------------------------------------------|
| [Wecker](https://developer.chrome.com/extensions/alarms) | Planen Sie den Code so, dass er periodisch oder zu einem bestimmten Zeitpunkt in der Zukunft ausgeführt wird. |
| [Lesezeichen](https://developer.chrome.com/extensions/bookmarks) | Erstellen, organisieren und Bearbeiten von Textmarken |
| [BrowserAction](https://developer.chrome.com/extensions/browserAction) | Verwenden Sie Browser Aktionen, um Symbole auf der Symbolleiste in Microsoft Edge zu platzieren. Sie können auch Browser Aktionen verwenden, um eine QuickInfo, ein Signal oder ein Popup hinzuzufügen. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Entfernen Sie das Browsen von Daten aus dem lokalen Profil eines Benutzers. |
| [Befehle](https://developer.chrome.com/extensions/commands) | Fügen Sie Tastenkombinationen hinzu, die Aktionen in ihrer Erweiterung auslösen. Beispielsweise eine Aktion zum Öffnen des Browsers oder Senden eines Befehls an die Erweiterung. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | Im Allgemeinen können Sie mit den Inhaltseinstellungen das Verhalten von Microsoft Edge auf jeder Website und nicht global anpassen. Ändern Sie die Einstellungen, die Steuern, ob Websites Funktionen wie Cookies, JavaScript und Plugins verwenden können. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Hinzufügen von Elementen zum Kontextmenü in Microsoft Edge Menüelemente können auf verschiedene Objekte wie Bilder, Hyperlinks und Seiten angewendet werden. |
| [Cookies](https://developer.chrome.com/extensions/cookies) | Sie können Cookies Abfragen und ändern sowie Benachrichtigungen empfangen, wenn Sie sich ändern. |
| [Debugger](https://developer.chrome.com/extensions/debugger) | Anfügen an eine oder mehrere Registerkarten zum Instrumentieren der Netzwerkinteraktion, Debuggen von JavaScript, Ändern des DOM, Ändern von CSS usw. Verwenden Sie den Debugger-tabid, um Tabstopps mit sendCommand zu Zielen, und leiten Sie Ereignisse von tabid aus OnEvent-Rückrufen weiter. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Führen Sie Aktionen abhängig vom Inhalt einer Seite aus, ohne dass die Berechtigung zum Lesen des Seiteninhalts erforderlich ist. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Bietet mehr Datenschutz durch das Blockieren oder Ändern von Netzwerkanforderungen durch Angeben von deklarativen Regeln. Zulassen, dass Erweiterungen Netzwerkanforderungen ändern, ohne die Anforderung abzufangen und den Inhalt anzuzeigen. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Erfassen des Inhalts eines Bildschirms, einzelner Fenster oder Registerkarten |
| [devtools. inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interagieren mit dem geprüften Fenster Rufen Sie beispielsweise die Registerkarten-ID von Seiten ab, Werten Sie Code aus, laden Sie Seiten neu, oder rufen Sie Ressourcen auf einer Seite auf. |
| [devtools. Network](https://developer.chrome.com/extensions/devtools_network) | Rufen Sie Informationen zu Netzwerkanforderungen ab, die von den Entwickler Tools in der Netzwerksteuerung angezeigt werden. |
| [devtools. Panels](https://developer.chrome.com/extensions/devtools.panels) | Integrieren Sie Ihre Erweiterung in die Benutzeroberfläche des Entwickler Tools-Fensters, indem Sie eigene Panels erstellen, auf vorhandene Panels zugreifen oder Seitenleisten hinzufügen. |
| [Downloads](https://developer.chrome.com/extensions/downloads) | Programmgesteuertes starten, überwachen, manipulieren und suchen nach Downloads. |
| [Enterprise. hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Rufen Sie den Hersteller und das Modell der Hardwareplattform ab, auf der der Browser ausgeführt wird. Diese API steht nur für Erweiterungen zur Verfügung, die von Unternehmensrichtlinien installiert werden. |
| [Ereignisse](https://developer.chrome.com/extensions/events) | Allgemeine Typen, die von APIs verwendet werden, die Ereignisse auslösen, um Sie zu benachrichtigen, wenn ein interessantes Ereignis eintritt. |
| [Erweiterung](https://developer.chrome.com/extensions/extension) | Jede Erweiterungsseite kann die Dienstprogramme dieser API verwenden. Sie enthält Unterstützung für den Austausch von Nachrichten zwischen Erweiterungen und Inhalts Skripts, die unter Nachrichtenübergabe beschrieben werden. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Enthält Typdeklarationen für Microsoft Edge-Erweiterungen. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Verwalten von Schriftarteinstellungen in Microsoft Edge |
| [Verlauf](https://developer.chrome.com/extensions/history) | Interagieren Sie mit dem Browser-Eintrag der besuchten Seiten. Sie können URLs im Verlauf des Browsers hinzufügen, entfernen oder Abfragen. Informationen zum Überschreiben der Verlaufsseite mit ihrer eigenen Version finden Sie unter Überschreiben von Seiten. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implementieren Sie die Internationalisierung für Ihre gesamte APP oder Erweiterung. |
| [im Leerlauf](https://developer.chrome.com/extensions/idle) | Erkennen, wenn sich der Leerlaufzustand des Computers ändert. |
| [Management](https://developer.chrome.com/extensions/management) | Verwalten Sie die Liste der installierten oder ausgeführten Erweiterungen. Dies ist hilfreich bei Erweiterungen, die die integrierte neue Registerkarte überschreiben. |
| [Benachrichtigungen](https://developer.chrome.com/extensions/notifications) | Erstellen Sie mithilfe von Vorlagen Rich-Benachrichtigungen, und zeigen Sie Sie in der Taskleiste an. |
| [Omnibox](https://developer.chrome.com/extensions/omnibox) | Registrieren Sie Schlüsselwörter in der Microsoft Edge-Adressleiste, die auch als Omnibox bezeichnet wird. |
| [PageAction](https://developer.chrome.com/extensions/pageAction) | Fügen Sie der Microsoft Edge-Symbolleiste rechts neben der Adressleiste Symbole hinzu. Seitenaktionen sind Aktionen, die auf der aktuellen Seite ausgeführt werden können und nicht für alle Seiten gelten. Seitenaktionen werden abgeblendet angezeigt, wenn Sie inaktiv sind. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Speichern Sie Tabstopps als MHTML-Dateien.|
| [Berechtigungen](https://developer.chrome.com/extensions/permissions) | Abrufen deklarierter, optionaler Berechtigungen zur Laufzeit anstatt zur Installationszeit. Sie können diese API verwenden, um die erforderlichen und genehmigten Berechtigungen für Ihre Benutzer anzuzeigen. |
| [Ein/Aus](https://developer.chrome.com/extensions/power) | Überschreiben Sie die Energieverwaltungsfeatures des Systems. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Verwenden von Ereignissen zum Abfragen von Druckern, deren Funktionen und zum Übermitteln von Druckaufträgen |
| [Datenschutz](https://developer.chrome.com/extensions/privacy) | Steuerelementfeatures in Microsoft Edge, die sich auf die Privatsphäre eines Benutzers auswirken. Diese API hängt vom `EdgeSetting` Prototyp von ab `types` , um die Konfiguration von Microsoft Edge abzurufen und einzurichten. |
| [Proxy](https://developer.chrome.com/extensions/proxy) | Verwalten von Proxyeinstellungen für Microsoft Edge Diese API hängt vom `EdgeSetting` Prototyp der API ab `types` , um die Proxykonfiguration von Microsoft Edge abzurufen und einzurichten. |
| [Runtime](https://developer.chrome.com/extensions/runtime) | Rufen Sie die Hintergrundseite ab, geben Sie Details zu dem Manifest zurück, und lauschen Sie den Ereignissen im APP-oder Extension Lifecycle, und reagieren Sie darauf. Sie können auch den relativen Pfad von URLs in vollqualifizierte URLs konvertieren. |
| [Sitzungen](https://developer.chrome.com/extensions/sessions) | Sie können Registerkarten und Fenster aus einer Browsersitzung Abfragen und wiederherstellen. |
| [Speicher](https://developer.chrome.com/extensions/storage) | Speichern, abrufen und nachvollziehen von Änderungen an Benutzerdaten |
| [System. Memory](https://developer.chrome.com/extensions/system_memory) | Die `system.memory` API. |
| [System. Storage](https://developer.chrome.com/extensions/system_storage) | Abfrageinformationen zu Speichergeräten. Sie können auch Benachrichtigungen empfangen, wenn Speichergeräte angefügt oder getrennt werden. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interagieren mit Tab-Mediendatenströmen |
| [Registerkarten](https://developer.chrome.com/extensions/tabs) | Interagieren Sie mit dem Tab-System des Browsers, um Tabstopps zu erstellen, zu ändern und neu anzuordnen. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Greifen Sie auf die wichtigsten Websites zu, die auch als "am häufigsten besuchte Websites" bezeichnet werden, die auf der Registerkarte "neu" angezeigt werden. Diese Websites beinhalten keine vom Benutzer angepassten Tastenkombinationen. |
| [Sprachausgabe](https://developer.chrome.com/extensions/tts) | Wiedergeben von synthetischem Text-zu-Sprache (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implementieren Sie ein TTS-Modul (Text-to-Speech) mithilfe einer Erweiterung. Erweiterungen, die sich für die Verwendung dieser API registrieren, empfangen Ereignisse, die gesprochene Äußerungen und andere Parameter enthalten. Erweiterungen können dann jede verfügbare Webtechnologie verwenden, um Sprache zu synthetisieren und auszugeben und Ereignisse an die aufrufende Funktion zurückzusenden, um den Status zu melden. |
| [Typen](https://developer.chrome.com/extensions/types) | Geben Sie Deklarationen für Microsoft Edge ein. |
| [Webnavigation](https://developer.chrome.com/extensions/webNavigation) | Empfangen von Benachrichtigungen über den Status von Navigationsanforderungen |
| [WebRequest](https://developer.chrome.com/extensions/webRequest) | Beobachten und analysieren Sie den Datenverkehr. Abfangen, blockieren oder Ändern von Anforderungen |
| [windows](https://developer.chrome.com/extensions/windows) | Interagieren Sie mit Browserfenstern, um Fenster im Browser zu erstellen, zu ändern und neu anzuordnen. |



## Nicht unterstützte Erweiterungs-APIs

Microsoft Edge unterstützt die folgenden Erweiterungs-APIs nicht:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` – Als Alternative können Sie `launchWebAuthFlow` zum Abrufen eines OAuth2-Tokens zum Authentifizieren von Benutzern verwenden.
* `chrome.instanceID`.


## Weitere Überlegungen zu unterstützten APIs

* Der Benutzer muss bei Microsoft Edge mit einem zu verwendenden MSA-oder Azure Active Directory-Konto angemeldet sein `chrome.identity.getProfileUserInfo` . Wenn der Benutzer mit einem lokalen Active Directory-Konto bei Microsoft Edge angemeldet ist, gibt die API `null` die Werte für e-Mail und ID zurück.

* Microsoft Edge unterstützt keine Erweiterungen, die Chrome Web Store-Zahlungen verwenden `identity.getAuthtoken` , da Sie zum Anfordern von Token für signierte Benutzer verwendet werden. Diese Token werden an die RESTful-basierte Lizenzierungs-API gesendet. 


<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/apps/external_extensions).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
