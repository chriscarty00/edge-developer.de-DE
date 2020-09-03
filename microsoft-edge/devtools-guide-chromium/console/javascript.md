---
description: Hier erfahren Sie, wie Sie JavaScript in der Konsole ausführen.
title: Erste Schritte mit der Ausführung von JavaScript in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d31bcfbdf728e656c9a6fff882f939f8c24cd897
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993121"
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







# Erste Schritte mit der Ausführung von JavaScript in der Konsole   



In diesem interaktiven Lernprogramm erfahren Sie, wie Sie JavaScript in der Microsoft Edge devtools- **Konsole**ausführen.  Weitere Informationen zum Protokollieren von Nachrichten an der **Konsole**finden Sie unter [Erste Schritte mit der Protokollierung von Nachrichten][DevToolsConsoleLoggingMessages].  Weitere Informationen dazu, wie Sie JavaScript-Code pausieren und eine Zeile gleichzeitig durchlaufen, finden Sie unter [Erste Schritte mit JavaScript-Debugging][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Der Konsole" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   Der **Konsole**  
:::image-end:::  

## Übersicht   

Die **Konsole** ist ein [repl][WikiReadEvalPrintLoop], das für Read, Evaluate, Print und Loop steht.  Sie liest das JavaScript ein, das Sie eingeben, wertet den Code aus, druckt das Ergebnis des [Ausdrucks][2alityExpressionsVersusStatements]aus und führt dann eine Schleife zurück zum ersten Schritt aus.  

## Einrichten von devtools   

Dieses Lernprogramm wurde entwickelt, um die Demo zu öffnen und alle Workflows selbst zu testen.  Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.

1.  Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um die **Konsole**zu öffnen.  
1.  Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **Konsolen-JavaScript-Beispiel** , um es in einem neuen Fenster zu öffnen.  
    
    *   [Beispiel für eine Konsolen-JavaScript][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Die JavaScript-Beispielseite der Konsole Links und DevTools auf der rechten Seite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Die JavaScript-Beispielseite der Konsole Links und DevTools auf der rechten Seite  
    :::image-end:::  
    
## Anzeigen und Ändern des JavaScript-oder Dom der Seite   

Beim Erstellen oder Debuggen einer Seite ist es häufig hilfreich, Anweisungen in der **Konsole** auszuführen, um zu ändern, wie die Seite aussehen oder ausgeführt werden soll.  
    
1.  Beachten Sie den Text in der Schaltfläche.  
1.  Geben `document.getElementById('hello').textContent = 'Hello, Console!'` Sie die **Konsole** ein, und drücken Sie dann `Enter` , um den Ausdruck auszuwerten.  Beachten Sie, wie sich der Text in der Schaltfläche ändert.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="So sieht die Konsole nach der Auswertung des Ausdrucks aus" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       So sieht die **Konsole** nach der Auswertung des Ausdrucks aus  
    :::image-end:::  
    
    Unter dem Code, den Sie ausgewertet haben, wird angezeigt `"Hello, Console!"` .  Rufen Sie die vier Schritte von repl: lesen, auswerten, drucken, Schleife zurück.  Nach dem Auswerten des Codes wird von einem repl das Ergebnis des Ausdrucks gedruckt.  Daher `"Hello, Console!"` muss das Ergebnis der Auswertung sein `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Ausführen von beliebigem JavaScript, das nicht mit der Seite verbunden ist   

Manchmal möchten Sie einfach nur einen Code-Spielplatz, in dem Sie einige Codes testen oder neue JavaScript-Funktionen testen können, mit denen Sie nicht vertraut sind.  Die Konsole eignet sich hervorragend für Experimente dieser Art.  

1.  Geben `5 + 15` Sie die Konsole ein, und drücken Sie `Enter` , um den Ausdruck auszuwerten. Die Konsole druckt das Ergebnis des Ausdrucks unter dem Code aus.  In der folgenden Abbildung sollte Ihre **Konsole** das Ergebnis anzeigen, nachdem der Ausdruck ausgewertet wurde.  

1.  Geben Sie den folgenden Code in die **Konsole**ein.  Versuchen Sie, das Zeichen-für-Zeichen-Zeichen zu schreiben, anstatt es zu kopieren.  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    Wenn Sie mit der Syntax nicht vertraut sind `b=20` , lesen Sie [Definieren von Standardwerten für Funktionsargumente][Esma6DefaultParameterValues].  
    
1.  Führen Sie nun die soeben definierte Funktion aus.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Die Konsole wird angezeigt, nachdem die Ausdrücke im Codeausschnitt ausgewertet wurden." lightbox="../media/console-javascript-example-console-playground.msft.png":::
             Die **Konsole** wird angezeigt, nachdem die Ausdrücke im Codeausschnitt ausgewertet wurden.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` wird als Standardwert ausgewertet, `45` Wenn die `add` Funktion ohne ein zweites Argument aufgerufen wird `b` `20` .  

## Nächste Schritte   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

Mit devtools können Sie ein Skript mitten in der Ausführung anhalten.  Während Sie angehalten werden, können Sie die **Konsole** verwenden, um die `window` oder `DOM` der Seite zu diesem Zeitpunkt anzuzeigen und zu ändern.  Der Workflow sorgt für einen leistungsfähigen Debugging-Workflow.  Ein interaktives Lernprogramm finden Sie unter [Erste Schritte mit dem Debuggen von JavaScript][DevToolsJavascriptIndex].  

Die **Konsole** verfügt auch über eine Reihe von Funktionen, mit denen Sie die Interaktion mit einer Seite vereinfachen können.  Zum Beispiel:  

*   Anstatt `document.querySelector()` ein Element zu markieren, geben Sie Folgendes ein: `$()`  Diese Syntax wurde von jQuery inspiriert, ist aber nicht wirklich jQuery.  Es ist nur ein Alias für `document.querySelector()` .  
*   `debug(function)` legt einen Haltepunkt in der ersten Zeile dieser Funktion effektiv fest.  
*   `keys(object)` Gibt ein Array zurück, das die Schlüssel des angegebenen Objekts enthält.  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Konsolen Referenz | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Ausdrücke im Vergleich zu Anweisungen in JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Standardparameterwerte – erweiterte Parameterbehandlung – ECMAScript 6 – neue Features: Übersicht & Vergleich"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Beispiel für eine Konsolen-JavaScript | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lesen – eval – Print Loop – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/javascript) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
