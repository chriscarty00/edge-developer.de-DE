---
description: Informationen zu unterstützten manifestschlüssel sowie zu den bekannten Problemen/Chrom Inkompatibilitäten finden Sie hier.
title: Erweiterungen – unterstützte manifestschlüssel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: deeff12251d25efaed1b40c98594c616a0d9c99a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567464"
---
# Unterstützte Manifest-Schlüssel  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Jede Erweiterung hat eine JSON-formatierte Manifestdatei mit dem Namen manifest.json. Diese Datei enthält wichtige Informationen für die Erweiterung, die vom Namen bis zu den Berechtigungen reicht. Sofern in einer der folgenden Hinweise nicht angegeben, folgen die Eigenschaften von Microsoft Edge-Manifesten der gleichen Implementierung wie Chrome.

Im folgenden finden Sie ein Beispiel für eine [Microsoft Edge JSON-Manifestdatei](./supported-manifest-keys/json-manifest-example.md).

## Erforderliche Schlüssel

Die folgenden Schlüssel sind erforderlich:

Schlüssel | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :--------------
[Autor](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Empfohlene Tasten

Die folgenden Schlüssel werden empfohlen:

Schlüssel | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :--------------
browser_specific_settings | | Gibt den bevorzugten Status der Erweiterung im Browser an. Der Browser kann es in einer zukünftigen Version abhängig von Faktoren wie der Reputation der Erweiterung oder der Gesamtzahl der Schaltflächen, die sich bereits in der Adressleiste des Benutzers befinden, in einer zukünftigen Version respektieren. Dies kann verwendet werden, um die Standardposition des `browserAction` Symbols anzugeben. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> In Chrome nicht unterstützt.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[Symbole](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | Wird derzeit in Microsoft Edge ignoriert.



## browser_action oder page_action Tasten

Sie können nur einen der folgenden Schlüssel (oder keine) hinzufügen:

Schlüssel | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | Microsoft Edge unterstützt nicht die folgende Syntax:  `browser_action : {"default_icon" : "icon.png" }`   <br/>Die Größe für Symbole muss angegeben werden. <br/>Bevorzugte Größen: 20px, 25px, 30px, 40px. <br/> Weitere unterstützte Größen: 19px, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | Microsoft Edge unterstützt nicht die folgende Syntax:  `page_action : {"default_icon" : "icon.png" }`   <br/>Die Größe für Symbole muss angegeben werden. <br/>Bevorzugte Größen: 20px, 25px, 30px, 40px. <br/>Weitere unterstützte Größen: 19px, 35px, 38px.|

## Optionale Tasten

Die folgenden Schlüssel sind optional:

Schlüssel | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :--------------
[Hintergrund](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Persistent ist ein erforderliches Feld für Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | Die Inhalts Sicherheitsrichtlinie einer Seite blockiert websockets in Inhalts Skripts, wodurch eine nicht definierte Ausnahme generiert wird. | Microsoft Edge-Erweiterungen unterstützen derzeit nur [Standardrichtlinien Einschränkungen](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy): `script-src 'self'; object-src 'self'` |
[Inkognito](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[Berechtigungen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Unterstützte Berechtigungen
Die folgenden [Berechtigungen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) werden unterstützt:


| Berechtigung         | Beschreibung                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \ <all_urls \ >       | Ermöglicht es Hintergrund-und Inhalts Skripts, mit allen Webseiten mit zusätzlichen [Privilegien](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions)zu interagieren.                                                                                  |
| contextMenus       | Ermöglicht den Zugriff auf die `contextMenus` API. Dies ermöglicht das Hinzufügen von Elementen zum Kontextmenü von Microsoft Edge.                                                                                                                                                                                     |
| Cookies            | Gewährt Zugriff auf die `cookies` API. Damit können Sie Cookies Abfragen und ändern sowie benachrichtigt werden, wenn Sie sich ändern.                                                                                                                                                           |
| Geolocation        | Erlauben Sie der Erweiterung, die HTML5 `geolocation` -API zu verwenden, ohne den Benutzer zur Genehmigung aufzufordern.                                                                                                                                                                                   |
| im Leerlauf               | Gewährt Zugriff auf die `idle` API. Dies ermöglicht die Erkennung, wenn sich der Leerlaufzustand des Computers ändert.                                                                                                                                                                                    |
| Speicher            | Gewährt Zugriff auf die `storage` API. Dadurch können Änderungen an Benutzerdaten gespeichert, abgerufen und nachverfolgt werden.                                                                                                                                                                             |
| Registerkarten               | Gewährt Zugriff auf die `tabs` API, um mit dem Tab-System des Browsers zu interagieren. Dadurch können Registerkarten im Browser erstellt, geändert und neu angeordnet werden, einschließlich der URLs, die den einzelnen Registerkarten zugeordnet sind.                                                                                       |
| unlimitedStorage   | Ermöglicht [Speicher. local](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) , unbegrenzten Speicherplatz (je nach Systemressourcen) statt 5MB zu haben. Das Max-Speicher-pro-Schlüssel-Wert-Paar wird auch von 5MB auf unbegrenzt (je nach Systemressourcen) erhöht. |
| Webnavigation      | Gewährt Zugriff auf die `webNavigation` API. Dadurch können Benachrichtigungen über den Status von Navigationsanforderungen empfangen werden.                                                                                                                                                              |
| WebRequest         | Gewährt Zugriff auf die `webRequest` API. Dies ermöglicht das beobachten und Analysieren von Datenverkehr sowie das Abfangen, blockieren oder Ändern der Anforderung in Flight.                                                                                                                               |
| webRequestBlocking | Erforderlich, wenn eine Erweiterung die `webRequest` API in einer Blockierungs Weise verwendet.                                                                                                                                                                                                           |

'""'
