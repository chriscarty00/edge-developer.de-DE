---
description: Eine Einführung in das Konsolentool innerhalb der Microsoft Edge Developer Tools.
title: Verwenden der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483207"
---
# <a name="use-the-console"></a>Verwenden der Konsole  

Das **Konsolentool** der DevTools hilft Ihnen bei verschiedenen Aufgaben.  Die folgende Liste enthält einige der Aufgaben.  

*   Erfahren Sie, warum im aktuellen Projekt etwas nicht funktioniert, und verfolgen [Sie Probleme.][DevtoolsConsoleConsoleDebugJavascript]  
*   [Erhalten Sie Informationen zum Webprojekt][DevtoolsConsoleConsoleFilters] im Browser als Protokollnachrichten.  
*   [Protokollieren von Informationen][DevtoolsConsoleConsoleLog] in Skripts zu Debuggingzwecken.  
*   [Testen Sie JavaScript-Ausdrücke][DevtoolsConsoleConsoleJavascript] live in einer [REPL-Umgebung.][WikiReadEvalPrintLoop]  
*   [Interagieren Sie mit dem Webprojekt im Browser mithilfe][DevtoolsConsoleConsoleDomInteraction] von JavaScript.  
    
Die **Konsole** ist ein hervorragendes Begleittool für andere Tools.  Die **Konsole** bietet eine leistungsstarke Möglichkeit, die aktuelle Webseite mithilfe von JavaScript zu skripten, zu überprüfen und zu bearbeiten.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Das Konsolentool wird im oberen Bereich geöffnet" lightbox="../media/console-intro-console-main.msft.png":::
         Das **Konsolentool** wird im oberen Bereich geöffnet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Konsole im unteren Bereich mit dem oben geöffneten Elementtool" lightbox="../media/console-intro-console-panel.msft.png":::
         **Konsole** im unteren Bereich mit dem oben geöffneten **Elementtool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Die schnellste Möglichkeit, die Konsole direkt zu **öffnen,** besteht in der Auswahl `Control` + `Shift` + `J` von \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).  

## <a name="error-reports-and-console"></a>Fehlerberichte und Konsole  

**Konsole** ist der Standardspeicherort, an dem JavaScript- und Konnektivitätsfehler gemeldet werden.  Wenn Fehler auftreten, wird neben dem Symbol **Einstellungen** in DevTools eine Schaltfläche angezeigt, die die Anzahl der Fehler und Warnungen anzeigt.  Wählen Sie es aus, um die **Konsole zu öffnen** und das Problem zu zeigen.  Weitere Informationen finden Sie unter [Debuggen von Fehlern, die in der Konsole gemeldet wurden.][DevtoolsConsoleConsoleDebugJavascript]  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools enthält detaillierte Informationen zum Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools enthält detaillierte Informationen zum Fehler in der **Konsole**  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a>Überprüfen und Filtern von Informationen auf der aktuellen Webseite  

Wenn Sie devTools auf einer Webseite öffnen, wird wahrscheinlich eine Informationsflut angezeigt, die bei der Konsole protokolliert **wurde.**  Die Menge der Informationen wird zu einem Problem, wenn Sie wichtige Informationen identifizieren müssen.  Verwenden Sie das Tool Probleme in DevTools, um die wichtigen Informationen anzeigen zu können, die eine [Aktion][DevtoolsIssuesIndex] benötigt.  Ein Teil des Geräuschs bleibt erhalten, weshalb es gut ist, über die automatisierten Protokoll- und Filteroptionen [in][DevtoolsConsoleConsoleFilters] der Konsole zu **wissen.**  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools mit einer Konsole voller Nachrichten" lightbox="../media/console-intro-noise.msft.png":::
   DevTools mit einer **Konsole** voller Nachrichten  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a>Protokollinformationen, die in der Konsole angezeigt werden  

Der beliebteste Verwendungsfall für die **Konsole** ist die Protokollierung von Informationen aus Ihren Skripts mithilfe der `console.log()` -Methode oder anderer ähnlicher Methoden.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Wählen **Sie**zum Öffnen der Konsole `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  
1.  Navigieren Sie [zu Konsolennachrichtenbeispiele: Protokoll, Info, Fehler][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]und Warn , oder kopieren und führen Sie den folgenden Codeausschnitt in der Konsole **aus.**  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  Die **Konsole** zeigt die Ergebnisse an.  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Konsole voller Nachrichten, die durch Democode verursacht werden" lightbox="../media/console-intro-logging.msft.png":::
       **Konsole** voller Nachrichten, die durch Democode verursacht werden  
    :::image-end:::  
    
Viele nützliche Methoden stehen zur Verfügung, wenn Sie mit der **Konsole arbeiten.**  Weitere Informationen finden Sie unter [Protokollieren von Nachrichten im Konsolentool.][DevtoolsConsoleConsoleLog]  

## <a name="try-your-javascript-live-in-the-console"></a>Testen Sie Ihr JavaScript live in der Konsole  

Die **Konsole** ist nicht nur ein Ort zum Protokollieren von Informationen.  Die **Konsole** ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]  Wenn Sie JavaScript in der Konsole **schreiben,** wird der Code sofort ausgeführt.  Möglicherweise ist es hilfreich, einige neue JavaScript-Features zu testen oder einige schnelle Berechnungen durchzuführen.  Darüber hinaus erhalten Sie alle Features, die Sie von einer modernen Bearbeitungsumgebung erwarten, z. B. autocompletion, syntax highlighting und history.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Navigieren Sie zur **Konsole**.  
1.  Geben Sie `2 + 2` ein.  
    
Die **Konsole** zeigt das Ergebnis `4` in der folgenden Zeile an.  Dieses **Feature für die** Begierdebewertung ist hilfreich, um zu debuggen und zu überprüfen, ob Sie keine Fehler im Code machen.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Die Konsole zeigt das Ergebnis von 2 + 2 live an, während Sie es eingeben" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   Die **Konsole** zeigt das Ergebnis von `2 + 2` live an, während Sie es eingeben  
:::image-end:::  

Wählen Sie aus, um den JavaScript-Ausdruck in der **Konsole ausführen** und optional ein Ergebnis anzeigen zu `Enter` können.  Anschließend können Sie den nächsten JavaScript-Code schreiben, der in der Konsole ausgeführt **werden soll.**  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Mehrere Zeilen JavaScript-Code nacheinander ausführen" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Mehrere Zeilen JavaScript-Code nacheinander ausführen  
:::image-end:::  

Standardmäßig führen Sie JavaScript-Code in einer einzelnen Zeile aus.  Geben Sie zum Ausführen einer Zeile Ihr JavaScript ein, und wählen Sie dann `Enter` aus.  Wählen Sie anstelle von aus, um die Einzeilerbeschränkung `Shift` + `Enter` zu `Enter` umgehen.  Wählen Sie ähnlich wie bei anderen Befehlszeilenerfahrungen aus, um auf Ihre vorherigen JavaScript-Befehle zu `Arrow-Up` zugreifen.  Das AutoCompletion-Feature der **Konsole** ist eine hervorragende Möglichkeit, um sich mit nicht vertrauten Methoden vertraut zu machen.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie `doc` ein.  
1.  Wählen `document` Sie aus dem Dropdownmenü aus.  
1.  Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.  
1.  Geben Sie `.bo` ein.  
1.  Wählen `tab` Sie aus, um `document.body` zu erhalten .  
1.  Geben Sie einen anderen ein, um die vollständige Liste der im Textkörper der aktuellen Webseite verfügbaren Eigenschaften und `.` Methoden anzuzeigen.  
    
Weitere Informationen zu allen Möglichkeiten **** zum Arbeiten mit konsolen finden Sie unter [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Konsolenautocompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **** Konsolenautocompletion von JavaScript-Ausdrücken  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a>Interagieren mit der aktuellen Webseite im Browser  

Die **Konsole** hat Zugriff auf das [Window-Objekt][MdnDocsWebApiWindow] des Browsers.  Sie können Skripts schreiben, die mit der aktuellen Webseite interagieren.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Kopieren des Inhalts der obersten Überschrift (h1) aus dem DOM und Anzeigen in der Konsole" lightbox="../media/console-intro-reading-DOM.msft.png":::
   Kopieren Sie den Inhalt der obersten Überschrift \( `h1` \) aus dem DOM, und zeigen Sie sie in der Konsole **an.**  
:::image-end:::  

Anstatt nur von der Webseite zu lesen, können Sie sie auch ändern.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Schreiben von Text in das DOM in der Konsole" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   Schreiben von Text in das DOM in der **Konsole**  
:::image-end:::  

Sie haben die Hauptüberschrift der Webseite in **"Rocking the Console" geändert.**  Die **Methoden des Konsolenprogramms** machen den Zugriff auf die aktuelle Webseite und das Bearbeiten der aktuellen Webseite einfach.  Weitere Informationen finden Sie unter [Console Utilities API reference][DevtoolsConsoleUtilities].  Um beispielsweise einen grünen Rahmen um alle Links auf der aktuellen Webseite hinzuzufügen, führen Sie die folgenden Aktionen aus.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Bearbeiten einer Auswahl von Elementen mithilfe der Konsole" lightbox="../media/console-intro-changing-styles.msft.png":::
    Bearbeiten einer Auswahl von Elementen mithilfe der **Konsole**  
:::image-end:::  

Weitere Informationen zum Arbeiten mit dem DOM finden Sie unter [Verwenden der Konsole für die Interaktion mit dem DOM][DevtoolsConsoleConsoleDomInteraction].  

## <a name="learn-more-about-console"></a>Weitere Informationen zur Konsole  

Weitere Informationen zur Konsole finden Sie unter **Console** [reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities]und Console API [reference][DevtoolsConsoleApi].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Debuggen von Fehlern, die im Konsolenmodus | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Verwenden der Konsole für die Interaktion mit der DOM-| Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtern von Konsolennachrichten | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokollieren von Nachrichten im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevtoolsIssuesIndex]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Beispiele für Konsolenmeldungen: Protokollierung, Informationen, Fehler und | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lese-eval-print-| Wikipedia"  
