---
title: Neue Features und APIs in EdgeHTML 17
description: Dieser Leitfaden enthält eine Übersicht über die Entwicklerfeatures und-Standards, die in EdgeHTML 17 enthalten sind.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 75429528fd814963a8c78e27f85564223fb2d3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233721"
---
# Neuerungen in EdgeHTML 17  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Nachfolgend finden Sie eine Liste der neuen und aktualisierten Features, die in [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30) Web Platform als Teil des [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/27) \ (04/2018, Build 17134 \) geliefert wurden.  Änderungen an bestimmten [Windows Insider](https://insider.windows.com) Preview-Builds finden Sie im [Microsoft Edge-Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) und [Neuerungen in EdgeHTML](../whats-new.md).  

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_17](./edgehtml-17.md) Änderungen:  

## Neue und aktualisierte Features  

### Aria 1,1-Rollen,-Zustände und-Ereignisse  

EdgeHTML 17 fügt Unterstützung für verschiedene Rollen, Zustände und Eigenschaften aus der [1,1-Spezifikation für barrierefreie Rich-Internet-Anwendungen (WAI-ARIA)](https://w3.org/TR/wai-aria-1.1)hinzu, einschließlich [Feed](https://www.w3.org/TR/wai-aria-1.1#feed), [Form](https://www.w3.org/TR/wai-aria-1.1#form), [Aria-haspopup](https://w3.org/TR/wai-aria-1.1#aria-haspopup), [Aria-Platzhalter](https://w3.org/TR/wai-aria-1.1#aria-placeholder)und vielem mehr; eine [vollständige Liste der Aria-Updates finden Sie im Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299).  Mit diesem Update unterstützt EdgeHTML 17 nun alle Rollen und Attribute, die in WAI-ARIA 1,1 definiert sind.  <!--  Check out the [Accessibility](../../accessibility.md) docs for more information about accessibility in Microsoft Edge.  -->  

### CSS-Maskierung  

EdgeHTML 17 umfasst experimentelle Unterstützung für [CSS-Maskierungen](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking).  Mit der partiellen Implementierung werden die Eigenschaften CSS [Mask-Image](https://developer.mozilla.org/docs/Web/CSS/mask-image) und [Mask-size](https://developer.mozilla.org/docs/Web/CSS/mask-size) eingeführt.  Aktivieren Sie das Flag "CSS-Maskierung aktivieren" in about: Flags für das Experimentieren!  

### CSS-Transformationen für SVG-Elemente  

EdgeHTML 17 unterstützt jetzt CSS-Transformationen für SVG-Elemente und Präsentationsattribute.  Dadurch können SVG-Elemente visuell manipuliert werden, einschließlich drehen, skalieren, verschieben, neigen oder übersetzen.  

### Erweiterungen  

Microsoft Edge unterstützt jetzt die [Benachrichtigungs-API](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) , in der Benachrichtigungen aus Erweiterungen angezeigt werden.  Erweiterungsentwickler können nun unterschiedliche Arten von Benachrichtigungen erstellen (Standard, Liste, Bild usw.), die eine vollständige Benutzerinteraktion unterstützen.  Die Benachrichtigungen werden auch automatisch beim Wartungs Center angemeldet.  Besuchen Sie das [Benachrichtigungs Beispiel](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) , wie Sie diese API in ihrer Erweiterung verwenden können.  

EdgeHTML 17 unterstützt nun auch die `Tabs.reload()` Methode als Teil der standardmäßigen Tab-API-Klasse.  Auch neu im Windows 10 April 2018-Update können Benutzer nun auswählen, dass Erweiterungen während des InPrivate-Browsens ausgeführt werden sollen.  

Weitere Informationen zu Erweiterungs Updates in dieser Version finden Sie im Blogbeitrag [neue Funktionen für Erweiterungen im Windows 10 April 2018-Update](https://blogs.windows.com/msedgedev/2018/05/24).  

### DevTools  

Diese Version von devtools wird auf zwei Arten ausgeliefert: als herkömmliche in-Browser- `F12` Tools für Microsoft Edge und Vorschau als eigenständige [Windows 10-App](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) aus dem Microsoft Store!  

:::image type="complex" source="../../devtools-protocol/media/microsoft-edge-devtools.png" alt-text="Microsoft Edge devtools-App" lightbox="../../devtools-protocol/media/microsoft-edge-devtools.png":::
   Microsoft Edge devtools-App  
:::image-end:::  

Die Tools wurden auch mit einer Reihe wichtiger Features aktualisiert, einschließlich der grundlegenden Unterstützung für das [Remotedebuggen](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) \ (über unser neues [devtools-Protokoll](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)\), [PWA-Debugfunktionen](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging), IndexedDB- [Cacheverwaltung](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection), [vertikales Andocken](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) und vieles mehr! Darüber hinaus haben wir den Gesamtaufwand für die [Umgestaltung](./edgehtml-16.md) der letzten Version im Rahmen der laufenden Investitionen in Leistung und Zuverlässigkeit fortgesetzt.  

Weitere Informationen finden Sie [unter devtools im neuesten Windows 10-Update (EdgeHTML 17)](../../devtools-guide/whats-new/edgehtml-17.md) .  

### JavaScript  

Mit EdgeHTML 17 führt das Chakra JavaScript-Modul Leistungsverbesserungen in einer Reihe von Schlüsselbereichen ein:  

:::row:::
   :::column span="1":::
      **Schlankerer Speicherbedarf**  
   :::column-end:::
   :::column span="2":::
      *   \ (Re-\) verzögern der Analyse für [Pfeil Funktionen](https://github.com/Microsoft/ChakraCore/pull/4105) und [Methoden für Objekt Literale](https://github.com/Microsoft/ChakraCore/pull/4136)  
      *   [RegExp-Bytecode-Refactoring](https://github.com/Microsoft/ChakraCore/pull/3915)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Schnellere integrierte JavaScript-Add-ins**
   :::column-end:::
   :::column span="2":::
      *   [Geben Sie Freigabe für Objekt. erstellen ein.](https://github.com/Microsoft/ChakraCore/pull/3901)  
      *   [Polymorpher Inline Cache für Object. assign](https://github.com/Microsoft/ChakraCore/pull/3792)  
      *   [JSON. Parse/stringify-Optimierungen](https://github.com/Microsoft/ChakraCore/pull/4077)  
      *   [Umschreiben von Array-Iteratoren in JavaScript und schneller für... der](https://github.com/Microsoft/ChakraCore/pull/4095)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Web-Assemblierung**
   :::column-end:::
   :::column span="2":::
      *   [Support für inling](https://github.com/Microsoft/ChakraCore/pull/3681)  
   :::column-end:::
:::row-end:::  

Schauen Sie sich die [Verbesserte JavaScript-und webassemblyleistung in EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/06/19) an, um alle Details zu erfahren.  

### Medienelement

EdgeHTML 17 enthält Updates für [HTMLMediaElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) , einschließlich:  

*   Das neue `preload` Attribut für das [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) Element gibt an, welche Daten vorab geladen werden sollen.
*   Durch das Hinzufügen der [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) Methode und der [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) Eigenschaft können Entwickler das Audiogerät auswählen.  
    
    > [!NOTE]
    > Dies steht in RTC noch nicht zur Verfügung.  
    
### Media Capture-API  

Microsoft Edge unterstützt jetzt die Bildschirmaufnahme in RTC über die [Media Capture-API](https://w3c.github.io/mediacapture-screen-share).  Mit diesem Feature können Webseiten die Ausgabe des Anzeigegeräts eines Benutzers aufzeichnen, das häufig zum Übertragen eines Desktops für Plug-in-freie virtuelle Besprechungen oder Präsentationen verwendet wird.  

### Progressive Web Apps  

Ab EdgeHTML 17 sind Dienstmitarbeiter und Push-Benachrichtigungen standardmäßig aktiviert \ (Weitere Informationen zu diesen Features finden Sie im Blogbeitrags [Mitarbeiter: gehen Sie über die Seite hinaus](https://blogs.windows.com/msedgedev/2017/12/19)).  Damit ist die Suite der Technologien (einschließlich des FETCH-Netzwerks und der Push-und Cache-APIs \) abgeschlossen, die die technische Grundlage für Progressive Web-Apps \ (PWAs \) unter Windows 10 bildet.  

PWAs sind einfach Web-Apps, die mit systemeigenen App-ähnlichen Features auf unterstützenden Plattformen und Browser Modulen wie Installation/Startbildschirm, Offline-Support und Push-Benachrichtigungen [schrittweise verbessert](https://en.wikipedia.org/wiki/Progressive_enhancement) werden.  Unter Windows 10 mit dem Microsoft Edge \ (EdgeHTML \)-Modul genießen PWAs den zusätzlichen Vorteil, dass Sie unabhängig vom Browserfenster als [universelle Windows-Plattform](/windows/uwp/get-started/whats-a-uwp) -apps ausgeführt werden.  

Jenseits von PWAs können Service Mitarbeiter und die Cache-API Entwicklern die Möglichkeit geben, Netzwerkanforderungen abzufangen und aus dem Cache zu antworten.  Eine Website muss nicht einmal eine vollständige Web-App sein, um die Vorteile des Service Worker-Caches für die Leistung und Zuverlässigkeit von feinem seitenladevorgang zu nutzen, sowie die Möglichkeit, eine Offline-Erfahrung in Zeiten ohne Internetverbindung oder schlechter Qualität bereitzustellen.  

Besuchen Sie unsere [fortschrittlichen Web-Apps unter Windows](../../progressive-web-apps/index.md) docs, um mehr über Service Mitarbeiter und Details zu PWAs unter Windows 10 zu erfahren.  

### Web-Sicherheit  

EdgeHTML 17 stellt Unterstützung für die Integrität von subressourcen vor \ (Sri \).  Die unter [Ressourcen Integrität](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) ist ein Sicherheitsfeature, mit dem Browser überprüfen können, ob abgerufene Ressourcen (wie Bilder, Skripts, Schriftarten usw.) ohne unerwartete Manipulation zugestellt werden.  

Fügen Sie ein `integrity` Attribut, das eine kryptografische Hash Darstellung der Ressource enthält, die Sie auf Ihrer Webseite zu laden erwarten, in ein `<script>` oder `<link>` -Element ein, wie im folgenden Beispiel gezeigt.  Anschließend vergleicht Microsoft Edge die angeforderte Ressource mit dem im Attribut definierten Hash `integrity` .  Wenn Sie nicht übereinstimmen, führt Microsoft Edge die Ressource nicht aus und gibt einen Fehler an das Netzwerk zurück.  

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```  

Auch neu in EdgeHTML 17: der Anforderungsheader " [Upgrade-unsecure-](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) Request" ermöglicht Browsern die Anforderung eines sicheren Browsing-Erlebnisses.  Dieser Header teilt dem Server mit, dass der Browser das Upgrade unsicherer Anforderungen unterstützt, und der Benutzer sollte, falls verfügbar, zu einer sicheren Version der Website umgeleitet werden.  

### Variable Schriftarten
Die vollständige Unterstützung für Variable Schriftarten \ (einschließlich CSS- [Variationseinstellungen](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) und [Schriftart-optischer Größe](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)\) steht in EdgeHTML 17 zur Verfügung.  Mit Variablen Schriftarten können Entwickler das Aussehen von scheinbar unterschiedlichen Schriftarten mit einer einzelnen Schriftart durch Anpassen verschiedener Achsen erreichen, wodurch die Notwendigkeit für mehrere Schriftartdateien und eine bessere Leistung verringert wird.  

Nehmen Sie an [einer Expedition Teil, um zu erfahren, welche Variablen Schriftarten Web-Entwickler und-Designer bereitstellen](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts)und wie Sie Sie auf Ihrer Website verwenden.  Und erfahren Sie mehr über Variable Schriftarten im Blogbeitrag, [indem Sie mit Variablen Schriftarten ausdrucksstarke, ausdrucksstarke Typografie zu Microsoft Edge bringen](https://blogs.windows.com/msedgedev/2018/03/13).  

<iframe height='456' scrolling='no' title='Beispiele für Variable Tiden Tickets' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Sehen Sie sich die Stift <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> Variable Tides Ticket </a> -Beispiele von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe>  

## Neue APIs in EdgeHTML 17  

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 17.  Sie werden im Format von angezeigt `[interface name].[api name]` .  

> [!NOTE] 
> Obwohl die folgenden APIs im DOM verfügbar gemacht werden, kann sich das End-to-End-Verhalten einiger Entwickler weiterhin entwickeln.  Informationen zum offiziellen Word-Feature-Support finden Sie im  [Microsoft Edge-Platt Form Status](https://developer.microsoft.com/microsoft-edge/platform/status) .  

<iframe height='580' scrolling='no' title='Neue APIs in EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> in EdgeHTML 17 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe>  

> [!TIP]
> Wir haben uns mit anderen Browsern und der Web-Community [zusammengetan,](https://blogs.windows.com/msedgedev/2017/10/18) um [MDN Web docs](https://developer.mozilla.org) als den definitiven Ort für nützliche, unvoreingenommene, Browser unabhängige Dokumentationen für aktuelle und neu auf Standards basierende Webtechnologien zu übernehmen.  Details zur EdgeHTML-API-Unterstützung finden Sie direkt auf jeder Seite der [MDN-Webverweis Bibliothek](https://developer.mozilla.org/docs/Web).  Besuchen Sie den [Platt Form Status](https://developer.microsoft.com/microsoft-edge/status) von Microsoft Edge für die neuesten Features, die in Microsoft Edge unterstützt werden.  

## Vorherige EdgeHTML-Versionen  

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)  

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)  

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)  

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)  
