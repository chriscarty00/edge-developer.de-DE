---
title: Übersicht über die Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601786"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Übersicht über die Konsole   

  

Auf dieser Seite wird erläutert, wie die Microsoft Edge devtools-Konsole das Entwickeln von Webseiten vereinfacht.  Die Konsole hat zwei hauptsächliche Verwendungsmöglichkeiten: [Anzeigen von protokollierten Nachrichten](#viewing-logged-messages) und [Ausführen von JavaScript](#running-javascript).  

## Anzeigen von angemeldeten Nachrichten   

Web-Entwickler protokollieren häufig Nachrichten an die Konsole, um sicherzustellen, dass Ihr JavaScript wie erwartet funktioniert.  Wenn Sie eine Nachricht protokollieren möchten, fügen Sie einen Ausdruck wie `console.log('Hello, Console!')` in Ihr JavaScript ein.  Wenn der Browser Ihr JavaScript ausführt und einen Ausdruck wie diesen sieht, wird die Nachricht in der Konsole protokolliert.  Nehmen wir beispielsweise an, dass Sie das HTML und JavaScript für eine Seite schreiben:  

```html
<!doctype html>
<html>
  <head>
    <title>Console Demo</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <script>
      console.log('Loading!');
      const h1 = document.querySelector('h1');
      console.log(h1.textContent);
      console.assert(document.querySelector('h2'), 'h2 not found!');
      const artists = [
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
      ];
      console.table(artists);
      setTimeout(() => {
        h1.textContent = 'Hello, Console!';
        console.log(h1.textContent);
      }, 3000);
    </script>
  </body>
</html>
```  

[Abbildung 1](#figure-1) zeigt, wie die Konsole aussieht, nachdem Sie die Seite geladen und 3 Sekunden gewartet hat.  Versuchen Sie herauszufinden, welche Codezeilen der Browser veranlasst hat, die Nachrichten zu protokollieren.  

> ##### Abbildung1  
> Die Konsolen Leiste  
> ![Die Konsolen Leiste][ImageConsole]  

Web-Entwickler protokollieren Nachrichten aus zwei allgemeinen Gründen:  

*   Sicherstellen, dass der Code in der richtigen Reihenfolge ausgeführt wird  
*   Überprüfen der Werte von Variablen zu einem bestimmten Zeitpunkt  

Lesen Sie [Erste Schritte mit der Protokollierung von Nachrichten][DevtoolsConsoleLoggingMessages] , um praktische Erfahrungen mit der Protokollierung zu erhalten.  Die vollständige Liste der Methoden finden Sie in der [API-Referenz][DevToolsConsoleAPI] für die Konsole `console` .  Der Hauptunterschied zwischen den Methoden besteht darin, wie die Daten, die protokolliert werden, angezeigt werden.  

## Ausführen von JavaScript   

Die Konsole ist auch ein [repl][WikiREPLoop].  Sie können JavaScript in der Konsole ausführen, um mit der geprüften Seite zu interagieren.  [Abbildung 2](#figure-2) zeigt beispielsweise die Konsole neben der devtools-Startseite, und [Abbildung 3](#figure-3) zeigt dieselbe Seite nach der Verwendung der Konsole, um die obere Überschrift der Seite zu ändern.  

> ##### Abbildung2  
> Das Konsolenfeld neben der devtools-Startseite  
> ![Das Konsolenfeld neben der devtools-Startseite][ImageConsoleOverview]  

> ##### Abbildung 3  
> Verwenden der Konsole zum Ändern der obersten Überschrift der Seite  
> ![Verwenden der Konsole zum Ändern der obersten Überschrift der Seite][ImageConsoleChangeTitle]  

Das Ändern der Seite über die Konsole ist möglich, da die Konsole Vollzugriff auf das [Fenster][MDNWindow] der Seite hat.  DevTools verfügt über einige komfortable Funktionen, mit denen Sie eine Seite leichter überprüfen können.  Nehmen wir beispielsweise an, dass Ihr JavaScript eine Funktion mit dem Namen `hideModal` .  Durch Ausführen wird der `debug(hideModal)` Code in der ersten Zeile des `hideModal` nächsten Ausführungszeitraums angehalten.  Die vollständige Liste der Dienstprogrammfunktionen finden Sie unter [API-Referenz][DevtoolsConsoleUtilitiesDebug] für die Konsolen Dienstprogramme.  

Wenn Sie JavaScript ausführen, müssen Sie nicht mit der Seite interagieren.  Sie können die Konsole verwenden, um neuen Code auszuprobieren, der sich nicht auf die Seite bezieht.  Angenommen, Sie haben soeben die integrierte JavaScript-Array [Zuordnungsmethode ()][MDNMap] kennengelernt, und Sie möchten damit experimentieren.  
Die **Konsole** ist ein guter Ort, um die Funktion auszuprobieren.  

Lesen Sie [Erste Schritte mit der Ausführung von JavaScript][ImageConsoleChangeTitle] , um praktische Erfahrungen mit der Ausführung von JavaScript in der Konsole zu erhalten.  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Abbildung 1: die Konsolen Leiste"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Abbildung 3: Verwenden der Konsole zum Ändern der obersten Überschrift der Seite"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Abbildung 2: die Konsolen Leiste neben der devtools-Startseite"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Erste Schritte mit der Ausführung von JavaScript in der Konsole"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Debug-API-Referenz für Console Utilities"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. Prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lesen – eval – Print Loop – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
