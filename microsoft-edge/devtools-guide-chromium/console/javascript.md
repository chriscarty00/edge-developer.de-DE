---
description: Erfahren Sie, wie Sie JavaScript in der Konsole ausführen.
title: Erste Schritte mit der Ausführung von JavaScript in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398819"
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

# <a name="get-started-with-running-javascript-in-the-console"></a>Erste Schritte mit der Ausführung von JavaScript in der Konsole  

In diesem interaktiven Lernprogramm wird gezeigt, wie Sie JavaScript in der Microsoft Edge DevTools-Konsole **ausführen.**  Weitere Informationen zum Protokollieren von Nachrichten an der **Konsole**finden Sie unter Erste Schritte [mit protokollieren von Nachrichten.][DevToolsConsoleLoggingMessages]  Weitere Informationen zum Anhalten von JavaScript-Code und zum Schrittweisen Durchfahren des Codes in einer Zeile finden Sie unter Erste Schritte mit [Debuggen von JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Die Konsole" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   Die **Konsole**  
:::image-end:::  

## <a name="overview"></a>Übersicht  

Die **Konsole** ist eine [REPL][WikiReadEvalPrintLoop], die für Read, Evaluate, Print und Loop steht.  Es liest das JavaScript, das Sie eingeben, wertet Den Code aus, druckt das Ergebnis Ihres Ausdrucks aus [und][2alityExpressionsVersusStatements]führt dann eine Schleife zurück zum ersten Schritt.  

## <a name="set-up-devtools"></a>Einrichten von DevTools  

Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.  Wenn Sie physisch folgen, werden Sie sich die Workflows wahrscheinlich später merken.

1.  Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um die Konsole **zu öffnen.**  
1.  Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **Javascript-Beispiel** für Konsole aus, um in einem neuen Fenster zu öffnen.  
    
    *   [Beispiel für JavaScript für konsolen][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Die Seite "Konsolen-JavaScript-Beispiel" links und DevTools auf der rechten Seite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Die Seite "Konsolen-JavaScript-Beispiel" links und DevTools auf der rechten Seite  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a>Anzeigen und Ändern des JavaScript oder DOM der Seite  

Beim Erstellen oder Debuggen einer Seite ist es **** häufig hilfreich, Anweisungen in der Konsole auszuführen, um das Aussehen oder die Ausführung der Seite zu ändern.  
    
1.  Beachten Sie den Text auf der Schaltfläche.  
1.  Geben `document.getElementById('hello').textContent = 'Hello, Console!'` Sie in die **Konsole** ein, und wählen Sie dann `Enter` aus, um den Ausdruck auszuwerten.  Beachten Sie, wie sich der Text innerhalb der Schaltfläche ändert.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aussehen der Konsole nach der Auswertung des Ausdrucks" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Aussehen der **Konsole** nach der Auswertung des Ausdrucks  
    :::image-end:::  
    
    `"Hello, Console!"`, wird unterhalb des von Ihnen ausgewerteten Codes angezeigt.  Denken Sie an die 4 Schritte von REPL: Lesen, Auswerten, Drucken, Schleifen.  Nach der Auswertung des Codes druckt eine REPL das Ergebnis des Ausdrucks.  Dies `"Hello, Console!"` muss das Ergebnis der Auswertung `document.getElementById('hello').textContent = 'Hello, Console!'` sein.  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a>Ausführen von beliebigem JavaScript, das nicht mit der Seite in Zusammenhang steht  

Manchmal möchten Sie nur einen Codespielplatz, in dem Sie Code testen oder neue JavaScript-Features ausprobieren können, mit denen Sie nicht vertraut sind.  Die **Konsole** ist ein perfekter Ort für diese Art von Experimenten.  

1.  Geben `5 + 15` Sie in die Konsole ein, und wählen Sie `Enter` aus, um den Ausdruck auszuwerten. Die Konsole druckt das Ergebnis des Ausdrucks unter Ihrem Code aus.  In der folgenden Abbildung sollte ihre **Konsole** das Ergebnis nach der Auswertung des Ausdrucks anzeigen.  

1.  Geben Sie den folgenden Code in die **Konsole ein.**  Versuchen Sie, sie zeichen-für-zeichen- und nicht kopierend eintippen.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Wenn Sie mit der Syntax nicht vertraut sind, navigieren Sie, um Standardwerte `b=20` [für Funktionsargumente zu definieren.][Esma6DefaultParameterValues]  
    
1.  Führen Sie nun die Funktion aus, die Sie gerade definiert haben.  
    
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
    
    `add(25)` wird ausgewertet, da, wenn die Funktion ohne ein zweites Argument aufgerufen `45` `add` wird, `b` standardmäßig auf `20` .  

## <a name="next-steps"></a>Nächste Schritte  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

Mit DevTools können Sie ein Skript mitten in der Ausführung anhalten.  Während Sie angehalten sind, können **** Sie die Konsole verwenden, um den Oder der Seite zu diesem Zeitpunkt ein- und `window` zu `DOM` ändern.  Der Workflow sorgt für einen leistungsstarken Debugworkflow.  Ein interaktives Lernprogramm finden Sie unter [Erste Schritte mit debuggen von JavaScript][DevToolsJavascriptIndex].  

Die **Konsole** verfügt außerdem über eine Reihe von Komfortfunktionen, die die Interaktion mit einer Seite vereinfachen.  Zum Beispiel:  

*   Anstatt ein Element auszuwählen, geben `document.querySelector()` Sie `$()` ein .  Diese Syntax wird von jQuery inspiriert, ist aber nicht wirklich jQuery.  Es handelt sich lediglich um einen Alias für `document.querySelector()` .  
*   `debug(function)` legt effektiv einen Haltepunkt in der ersten Zeile dieser Funktion fest.  
*   `keys(object)` gibt ein Array zurück, das die Schlüssel des angegebenen Objekts enthält.  

Weitere Informationen zu den Komfortfunktionen finden Sie unter [Console Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Konsolenreferenz | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Ausdrücke und Anweisungen in JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Standardparameterwerte - Erweiterte Parameterbehandlung - ECMAScript 6 – Neue Features: Übersicht & Vergleich"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Javascript-Beispiel für | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lese-eval-print-Schleife – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/javascript) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
