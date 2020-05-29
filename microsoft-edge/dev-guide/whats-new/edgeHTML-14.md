---
description: Auf dieser Seite finden Sie eine Übersicht über die Neuerungen in EdgeHTML 14.
title: Neuerungen in EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 5e9e0d5d9a53c5ecbfeb4b93c3b453a3d2904e2b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566788"
---
# Neuerungen in EdgeHTML 14
Hier sind die Änderungen, die mit EdgeHTML 14 ausgeliefert wurden, ab dem [Windows 10 Anniversary Update](https://blogs.windows.com/windowsexperience/2016/06/29/windows-10-anniversary-update-available-august-2/) (08/2016, Build 14393). Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Einführung in EdgeHTML 14 mit dem Windows 10 Anniversary Update](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14).

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_14](https://aka.ms/devguide_edgehtml_14) Änderungen:

## Neue Funktionen

### Extensions
Erweiterungen sind kleine Programme, die verwendet werden können, um Microsoft Edge neue Features hinzuzufügen oder die vorhandene Funktionalität zu ändern. Erweiterungen dienen dazu, den Alltag des Nutzers zu verbessern, indem Sie Nischen Funktionen zur Verfügung stellen, die für Zielgruppen wichtig sind. Microsoft Edge unterstützt ein neues HTML-, JavaScript-und CSS-basiertes Erweiterungsmodell. Dieses neue Modell ist Chrome-kompatibel, was bedeutet, dass vorhandene Chrome Extension-Entwickler Ihre Erweiterungen zu Microsoft Edge mit minimalen Änderungen migrieren können. Weitere Informationen finden Sie in den [Microsoft Edge Extensions](https://docs.microsoft.com/microsoft-edge/extensions) -Entwickler Dokumenten. 

### FETCH-API
Die [Fetch-API](https://fetch.spec.whatwg.org/#fetch-api) verwendet die `fetch` Methode zum Abrufen von Ressourcen. In der Vergangenheit wurde dies erreicht `XMLHttpRequest` . FETCH ist nicht nur einfacher zu verwenden, sondern bietet auch niedrigeren Zugriff auf Anfragen und Antworten. Weitere Informationen zur FETCH-API finden Sie im Microsoft Edge-Blogbeitrag, [Fetch (oder die unbestreitbaren Einschränkungen von XMLHttpRequest)](https://blogs.windows.com/msedgedev/2016/05/24/fetch-and-xhr-limitations/).

### JavaScript

EdgeHTML 14 bietet eine Reihe von neuen und experimentellen Features für Chakra, das JavaScript-Modul, das Microsoft Edge antreibt:

#### Neue Features (standardmäßig aktiviert)

* [Standardparameter](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) (ES2015)
* [Exponentialwert-Operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) (ES2016)
* [Array. Prototype. includes](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) (ES2016)
* [Object. Values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) und [Object. Entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) (ES2017)

#### Experimentelle JavaScript-Features (aktiviert mit *about: Flags*)

* [Module](https://blogs.windows.com/msedgedev/2016/05/17/es6-modules-and-beyond/) (ES2015)
* [Async/await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) (ES2017)
* [Regex-Symbole](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) (ES2015)

Weitere Informationen finden Sie unter [*Vorschau von ES6-Modulen und mehr von ES2015, ES2016 und darüber hinaus*](https://blogs.windows.com/msedgedev/2016/05/17/es6-modules-and-beyond/) und [*asynchroner Code wird mit ES2016 Async-Funktionsunterstützung in Chakra und Microsoft Edge vereinfacht*](https://blogs.windows.com/msedgedev/2015/09/30/asynchronous-code-gets-easier-with-es2016-async-function-support-in-chakra-and-microsoft-edge/).

### Web-Authentifizierungs-API (Fido 2,0 Web-API)
Die Webauthentifizierungs-API (ehemals Fido 2,0) in Microsoft Edge ermöglicht Webanwendungen die Verwendung von [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) Biometrie für die Benutzerauthentifizierung, damit Sie und Ihre Benutzer alle Probleme und Risiken der Kennwortverwaltung vermeiden können, einschließlich der Kenn Wort erraten, Phishing-und Keylogger-Angriffe. Die aktuelle Microsoft Edge-Implementierung (MS-prefixes) basiert auf einem früheren Entwurf der Webauthentifizierungs Spezifikation und wird sich wahrscheinlich in Zukunft ändern. Weitere Informationen finden Sie unter Webauthentifizierung: [Webauthentifizierung und Windows Hello](https://docs.microsoft.com/microsoft-edge/dev-guide/device/web-authentication).

### Web-Benachrichtigungen
Webbenachrichtigungen ermöglichen Websites das Anzeigen von Benachrichtigungen, um Benutzer außerhalb des Kontexts der Webseite und des Browsers zu benachrichtigen, um Benutzer über neue Nachrichten oder Benachrichtigungen auf dem Laufenden zu halten und Websites zu ermöglichen, die Benutzerbindung zu verbessern. Webbenachrichtigungen in Microsoft Edge sind vollständig in die Benachrichtigungs Plattform und das Wartungs Center in Windows 10 integriert, sodass eine konsistente Benutzeroberfläche mit anderen apps im gesamten System und einfache Steuerungen über Berechtigungen und ruhige Stunden bereitgestellt werden. Weitere Informationen finden Sie [unter Web-Benachrichtigungen in Microsoft Edge](https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge/) . 

### Web Speech-API
Die [Web Speech-API](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) ist eine JavaScript-API aus zwei Teilen: Spracherkennung und Sprachsynthese (oder Text-zu-Sprache). Zu diesem Zeitpunkt unterstützt Microsoft Edge nur die Sprachsynthese. Die Sprachsynthese umfasst die Konvertierung von Text in Sprache, die ein Benutzer über seine Lautsprecher hört. Weitere Informationen finden Sie im Artikel [Web Speech: Speech Synthesis](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-speech-api) Developer Guide. 

## Neue APIs in EdgeHTML 14

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 14. Sie werden im Format **[Schnittstellenname] aufgeführt. [ API-Name]**.
<iframe height='585' scrolling='no' title='Neue APIs in EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> in EdgeHTML 14 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .
</iframe>
