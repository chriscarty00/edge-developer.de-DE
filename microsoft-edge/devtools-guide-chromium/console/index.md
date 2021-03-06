---
description: Die Hauptanwendung der Microsoft Edge DevTools-Konsole sind die Protokollierung von Nachrichten und das Ausführen von JavaScript.
title: Konsole – Übersicht
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399120"
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

# <a name="console-overview"></a>Konsole – Übersicht  

  

Auf dieser Seite wird erläutert, wie die Microsoft Edge DevTools-Konsole die Entwicklung von Webseiten vereinfacht.  Die **Konsole** hat zwei Hauptverwendungszwecke: [Anzeigen protokollierter Nachrichten und](#viewing-logged-messages) Ausführen von [JavaScript](#running-javascript).  

## <a name="viewing-logged-messages"></a>Anzeigen protokollierter Nachrichten  

Webentwickler protokollieren häufig Nachrichten an der Konsole, um sicherzustellen, dass ihr JavaScript wie erwartet funktioniert.  Um eine Nachricht zu protokollieren, fügen Sie einen Ausdruck wie `console.log('Hello, Console!')` in Ihr JavaScript ein.  Wenn der Browser Ihr JavaScript ausgeführt und einen Ausdruck wie ihn verarbeitet, protokolliert der Browser die Nachricht an der **Konsole.**  

:::row:::
   :::column span="":::
      Html und JavaScript für die Seite.  
      
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
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
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
   :::column-end:::
   :::column span="":::
      In der folgenden Abbildung zeigt die **Konsole** die Ergebnisse des Ladens der Seite an und wartet 3 Sekunden.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Konsolenbereich" lightbox="../media/console-console-demo.msft.png":::
         Das **Konsolentool**  
      :::image-end:::  
      
      Versuchen Sie zu bestimmen, welche Codezeilen den Browser dazu führte, dass die Nachrichten protokolliert wurden.  
   :::column-end:::
:::row-end:::  

Webentwickler protokollieren Nachrichten aus den folgenden 2 allgemeinen Gründen.  

*   Stellen Sie sicher, dass Code in der richtigen Reihenfolge ausgeführt wird.  
*   Überprüfen der Werte von Variablen zu einem bestimmten Zeitpunkt.  

Um praktische Erfahrungen mit der Protokollierung zu erhalten, navigieren Sie zu [Erste Schritte mit Protokollierungsmeldungen][DevtoolsConsoleLoggingMessages].  Navigieren Sie zur Konsolen-API-Referenz, um die vollständige Liste der Methoden `console` [zu durchsuchen.][DevToolsConsoleAPI]  Der Hauptunterschied zwischen den Methoden besteht in der Anzeige der protokollierten Daten.  

## <a name="running-javascript"></a>Ausführen von JavaScript  

Die **Konsole** ist auch eine [REPL][WikiREPLoop].  Sie können JavaScript in der Konsole **ausführen,** um mit der überprüften Seite zu interagieren.   

:::row:::
   :::column span="":::
      In der folgenden Abbildung wird **die Konsole** neben der DevTools-Homepage angezeigt.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Das Konsolentool neben der DevTools-Homepage" lightbox="../media/devtools-console-empty.msft.png":::
         Das **Konsolentool** neben der DevTools-Homepage  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      In der folgenden Abbildung wird dieselbe Seite nach der Verwendung der **Konsole** angezeigt, um die obere Überschrift der Seite zu ändern.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Ändern der oberen Überschrift der Seite mithilfe der Konsole" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Ändern **der** oberen Überschrift der Seite mithilfe der Konsole  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Das Ändern der Seite über die **Konsole** ist möglich, da die **Konsole** Vollzugriff auf das [Fenster][MDNWindow] der Seite hat.  DevTools verfügt über einige Komfortfunktionen, die das Überprüfen einer Seite vereinfachen.  Angenommen, Ihr JavaScript enthält eine Funktion namens `hideModal` .  Beim `debug(hideModal)` Ausführen wird der Code in der ersten Zeile des nächsten `hideModal` Ausführungslaufs angehalten.  Weitere Informationen zur vollständigen Liste der Hilfsfunktionen finden Sie unter [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].  

Wenn Sie JavaScript ausführen, müssen Sie nicht mit der Seite interagieren.  Sie können die Konsole **verwenden,** um neuen Code zu testen, der nichts mit der Seite zu tun hat.  Angenommen, Sie haben gerade etwas über die integrierte JavaScript Array [map()-Methode][MDNMap] erfahren, und Sie möchten damit experimentieren.  
Die **Konsole** ist ein guter Ort, um die Funktion auszuprobieren.  

Weitere praktische Erfahrungen mit der Ausführung von JavaScript in der **Konsole finden**Sie unter Erste Schritte mit der Ausführung [von JavaScript][DevtoolsConsoleRunningJavascript].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsolenkonsole | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "debug – Apireferenz für Konsolenprogramme | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-Schleife – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
