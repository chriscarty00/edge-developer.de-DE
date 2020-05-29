---
description: Auf dieser Seite finden Sie eine Übersicht über die Neuerungen in EdgeHTML 12.
title: Neuerungen in EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: f16db0551d4bea3d29b974c2a35fff2adf476c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566755"
---
# Neuerungen in EdgeHTML 12

Microsoft Edge führt EdgeHTML ein, eine neue "Living"-Engine, die im Kern mit Interoperabilität entwickelt wurde, um sicherzustellen, dass Sie immer die neueste und beste Windows Web-Plattform erhalten. Microsoft Edge stellt eine saubere Unterbrechung aus der Vergangenheit dar, frei von dem Legacycode, der zur Unterstützung von ActiveX-Steuerelementen, Browser Helper Objects (BHOs) und anderen früheren Webentwicklungs Methoden erforderlich ist. Darüber hinaus bietet Microsoft Edge native PDF-Unterstützung. Ab IE11 sind die Legacy Dokumentmodi veraltet, und mit Microsoft Edge ist die Browser Infrastruktur zur Unterstützung nicht vorhanden. Weitere Informationen finden Sie im [IEBlog](https://go.microsoft.com/fwlink/p/?LinkID=519011) .

Hier sind die Änderungen, die mit EdgeHTML 12 in der ersten Version von [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) (07/2015, Build 10240) ausgeliefert wurden. Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Bruch aus der Vergangenheit: die Geburt des neuen webrendering-Moduls von Microsoft](https://blogs.windows.com/msedgedev/2015/02/26/a-break-from-the-past-the-birth-of-microsofts-new-web-rendering-engine/) und [eine Pause von der Vergangenheit, Teil 2: verabschieden von ActiveX, VBScript, AttachEvent.](https://blogs.windows.com/msedgedev/2015/05/06/a-break-from-the-past-part-2-saying-goodbye-to-activex-vbscript-attachevent/)..

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_12](https://aka.ms/devguide_edgehtml_12) Änderungen:


## Neue Funktionen

### Inhalts Sicherheitsrichtlinie 1,0
Microsoft Edge implementiert nun Content Security Policy (CSP) 1,0. Der CSP-Sicherheitsstandard ermöglicht Webentwicklern, die Ressourcen (Skript, CSS, Plugins, Bilder usw.) zu steuern, die eine bestimmte Seite abrufen oder ausführen kann, um websiteübergreifendes Skripting (XSS), Clickjacking und andere Code Injection-Angriffe zu verhindern, die bösartigen Inhalt im Kontext einer vertrauenswürdigen Webseite ausführen möchten. Weitere Informationen zu CSP in Microsoft Edge finden Sie unter [Inhalts Sicherheitsrichtlinien](https://docs.microsoft.com/microsoft-edge/dev-guide/security/content-security-policy) . 

### Filter Effekte
Microsoft Edge bietet eine einfache Möglichkeit, Elemente visuelle Effekte hinzuzufügen. Mit der `filter` Eigenschaft können Sie Weichzeichner hinzufügen, die Helligkeit anpassen, einen Schlagschatten hinzufügen, die Deckkraft ändern und mehr in ein Element umwandeln. Mit reinem CSS können Sie mehrere Filtereffekte auf ein Element anwenden und die Filter animieren. Weitere Informationen finden Sie unter [Filter Effekte](https://docs.microsoft.com/microsoft-edge/dev-guide/css/filter-effects).

### JavaScript
Die JavaScript-Unterstützung variiert etwas zwischen der endgültigen Version von Internet Explorer (IE11) und Microsoft Edge. Zu den neuen Features in Edge gehören:

| | |
|--|--|
|**Auszüge**| [Klasse](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) (experimentell), [für... von](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) |
|**Objekte**| [Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [Proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [Symbol](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [weakset](/scripting/javascript/reference/weakset-object-javascript) |
|**Funktionen** | [acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [IsInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [isNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [RAW](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw) |
|**Methoden**| [includes](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [Keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) (Array), [Repeat](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) (Zeichenfolge), [Werte](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) (Array) |
|**Andere Features**| [Funktionen](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) (experimentell), [Generatoren](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [Iteratoren](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` Flag für reguläre Ausdrücke](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) (experimentell), [Vorlagenzeichenfolgen](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), [Unicode-Codepunkt-Escapezeichen](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals) |

Einen Vergleich der JavaScript-Unterstützung über Internet Explorer, Microsoft Edge und Microsoft Store-Apps finden Sie unter [*JavaScript-Versionsinformationen*](./javascript-version-information.md).

### Medien Aufzeichnung und-Datenströme
Microsoft Edge bietet Unterstützung für die APIs für Medien Aufzeichnung und-Streams auf der Grundlage der [W3C-Spezifikation für Medien Erfassung und Datenströme](https://go.microsoft.com/fwlink/p/?LinkID=534096) . Diese JavaScript-APIs ermöglichen es Webseiten, auf Medien Aufnahmegeräte wie Webcams oder Mikrofone mit der Berechtigung des Benutzers zuzugreifen. Mithilfe der APIs für Medien Aufzeichnung und-Streams können Sie Szenarien wie das Aufzeichnen eines Fotos mithilfe einer Webcam oder das Aufzeichnen einer Sprachnachricht über ein Mikrofon erstellen. Weitere Informationen finden Sie unter Media Capture in Microsoft Edge im [Microsoft Edge Developer-Blog](https://blogs.windows.com/msedgedev/2015/05/13/announcing-media-capture-functionality-in-microsoft-edge/). 

### Neues HTML-Element und Attribute
* `meter` Element 
* `picture` Element 
* `template` Element 
* `image` Element: `srcset` und `sizes` Attribute (Microsoft Edge Developer- [Blogbeitrag](https://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/))
* `selectionDirection` Attribut
* `input type=time` und `input type=datetime-local`

### Objekt-RTC-API 
Mit der Objekt-Echtzeitkommunikation (ORTC) können Medien (Audio und/oder Video) über systemeigene JavaScript-APIs in Echtzeit direkt zwischen Webbrowsern, mobilen Geräten und Servern gestreamt (gesendet und empfangen) werden. Weitere Informationen zu ORTC in Microsoft Edge finden Sie im Entwicklerhandbuch zum Thema [Objekt RTC-API](https://docs.microsoft.com/microsoft-edge/dev-guide/realtime-communication/object-rtc-api) . 

### Leseansicht
Microsoft Edge bietet eine Leseansicht für eine optimierte, Buch ähnliche Leseerfahrung von Webseiten ohne Ablenkung von nicht miteinander verknüpften oder anderen sekundären Inhalten auf der Seite. Die Leseansicht kann über die Schaltfläche Leseansicht (Buchsymbol) auf der Adressleiste (oder mit STRG + UMSCHALT + R) ein-oder ausgeblendet werden. Weitere Informationen finden Sie in der [Leseansicht](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/reading-view) . 

### Suchanbieter Ermittlung
Die Rich-Search-Integration ist in die Microsoft Edge-Adressleiste integriert, einschließlich Suchvorschlägen, Ergebnissen aus dem Internet, dem Browserverlauf und Favoriten. Microsoft Edge folgt der [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) -Spezifikation, um Anbieter von Websuchen zu ermitteln und zu verwenden. Wenn Sie ein Suchanbieter sind, [Lesen Sie weitere](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/search-provider-discovery) Informationen dazu, wie Sie sicherstellen können, dass Microsoft Edge ihren Dienst unterstützt. 

### Unterstützung für webkit-APIs
Zur Verbesserung der Kompatibilität unterstützt Microsoft Edge eine Reihe von "-WebKit-"-APIs mit Präfix. Eine vollständige Liste der unterstützten "-WebKit-"-APIs finden Sie im [API-Katalog](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).

### Web-Audio
Microsoft Edge führt Unterstützung für die [W3C Web Audio API-](https://go.microsoft.com/fwlink/p/?LinkID=512167) Spezifikation ein. Web Audio ist eine allgemeine JavaScript-API für die Verarbeitung und Synthese von Audio in Webanwendungen, um reichhaltige Audio-und Musikerlebnisse zu bieten. Während das HTML5- `audio` Element eine grundlegende Streaming-Audiowiedergabe ermöglicht, bietet die webaudio-API eine Reihe von APIs, mit denen Sie mehrere Sounds mit enger Synchronisierung wiedergeben können, und Sie können Gain, Fades, Übergänge und grundlegende Effekte auf gemischte Audiofunktionen anwenden. Weitere [Informationen finden](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-audio) Sie im dev-Leitfaden und im [Microsoft Edge-Entwicklerblog](https://blogs.windows.com/msedgedev/2015/05/19/bringing-web-audio-to-microsoft-edge-for-interoperable-gaming-and-enthusiast-media/). 

### Web-Treiber 
Bei der [W3C-WebDriver-API](https://w3.org/TR/webdriver/) handelt es sich um eine Plattform-und sprachneutrale Schnittstelle und ein Draht Protokoll, mit der Programme oder Skripts das Verhalten eines Webbrowsers steuern können. WebDriver ermöglicht Entwicklern das Erstellen automatisierter Tests, die die Benutzerinteraktion simulieren. Dies unterscheidet sich von JavaScript-Komponententests, da WebDriver Zugriff auf Funktionen und Informationen hat, die JavaScript im Browser nicht ausführt, und es können Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer simuliert werden. WebDriver kann auch Tests über mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung verwalten.  Weitere Informationen zu den ersten Schritten mit WebDriver für Microsoft Edge finden Sie unter [WebDriver](https://docs.microsoft.com/microsoft-edge/dev-guide/tools/webdriver). 


## Neue APIs in EdgeHTML 12

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 12.  Sie werden im Format **[Schnittstellenname] aufgeführt. [ API-Name]**.

 > [!NOTE] 
 > Viele dieser APIs waren in IE11 verfügbar. Die nachstehenden Daten für EdgeHTML 12 werden als Basis für den Vergleich der ursprünglichen Version von EdgeHTML mit neueren Versionen angeboten.

<iframe height='580' scrolling='no' title='Neue APIs in EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> in EdgeHTML 12 </a> von Microsoft Edge docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe>
