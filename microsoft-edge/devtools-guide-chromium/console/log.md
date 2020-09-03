---
description: Hier erfahren Sie, wie Sie Nachrichten in der Konsole protokollieren.
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3a2562eeb25bcee7c8b5195f6f2297613e37f2d6
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993149"
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





# Erste Schritte mit der Protokollierung von Nachrichten in der Konsole   



In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge devtools][MicrosoftEdgeDevTools] -Konsole protokollieren und filtern.  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Nachrichten in der **Konsole**  
:::image-end:::  

Dieses Lernprogramm soll in der entsprechenden Reihenfolge ausgeführt werden.  Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, beispielsweise die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.  

## Einrichten der Demo-und DevTools   

Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.  Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.  

1.  Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **Konsolenprotokoll Beispiele** , um Sie in einer neuen Registerkarte zu öffnen.  
    
    [Beispiele für Konsolen Protokolle][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Konzentrieren Sie die Demo, und drücken Sie dann `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um devtools zu öffnen.  Standardmäßig wird devtools rechts neben der Demo geöffnet.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools wird rechts neben der Demo geöffnet" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools wird rechts neben der Demo geöffnet  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Docken Sie devtools an den unteren Rand des Fensters an][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools angedockt am Ende der Demo" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools angedockt am Ende der Demo  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Browser in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Browser in einem separaten Fenster  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools Abdocken in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools Abdocken in einem separaten Fenster  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Anzeigen von Nachrichten, die von JavaScript protokolliert wurden   

Die meisten Nachrichten, die Sie in der Konsole sehen, stammen von den Web-Entwicklern, die das JavaScript der Seite verfasst haben.  In diesem Abschnitt möchten wir Ihnen die verschiedenen Nachrichtentypen vorstellen, die Sie wahrscheinlich in der Konsole sehen werden, und erläutern, wie Sie die einzelnen Nachrichtentypen selbst aus Ihrem eigenen JavaScript-Protokoll aufzeichnen können.  

1.  Klicken Sie in der Demo auf die Schaltfläche **Log-Informationen** .  `Hello, Console!` wird in der Konsole protokolliert.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Die Konsole nach dem Klicken auf "Protokollinformationen"" lightbox="../media/console-log-info.msft.png":::
       Die **Konsole** nach dem Klicken auf " **Protokollinformationen** "  
    :::image-end:::  
    
1.  `Hello, Console!`Klicken Sie neben der Nachricht in der Konsole auf **log.js:2**.  Das Fenster "Quellen" wird geöffnet, und die Codezeile wird hervorgehoben, die dazu geführt hat, dass die Nachricht in der Konsole protokolliert wird.  Die Nachricht wurde protokolliert, als das JavaScript der Seite ausgeführt wurde `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools öffnet das Quellen Panel, nachdem Sie auf log.js:2 Klicken" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools öffnet das **Quellen** Panel, nachdem Sie auf `log.js:2`  
    :::image-end:::  
    
1.  Navigieren Sie mit einem der folgenden Workflows zurück zur **Konsole** :  
    
    *   Klicken Sie auf die Registerkarte **Konsole** .  
    *   Drücken Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \), bis die Konsole den Fokus hat.  
    *   [Öffnen Sie das Menübefehl][DevToolsCommandMenu], beginnen `Console` Sie mit der Eingabe, wählen Sie den Befehl **Konsolen Panel anzeigen** aus, und drücken Sie dann `Enter` .  
    
1.  Klicken Sie in der Demo auf die Schaltfläche **Warnungsprotokoll** .  `Abandon Hope All Ye Who Enter` wird in der Konsole protokolliert.  So formatierte Nachrichten sind Warnungen.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Die Konsole, nachdem Sie auf "Protokoll Warnung" klicken" lightbox="../media/console-log-warning.msft.png":::
       Die **Konsole** , nachdem Sie auf " **Protokoll Warnung** " klicken  
    :::image-end:::  
    
    > [!TIP]
    > Wenn Sie den Code anzeigen möchten, der dazu geführt hat, dass eine Nachricht protokolliert wird, klicken Sie auf ein Skript \ (beispielsweise `log.js:12` \), um den Code anzuzeigen, der dazu geführt hat, dass die Nachricht formatiert wurde.  

1.  Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) vor `Abandon Hope All Ye Who Enter` .  DevTools zeigt die [Stapelüberwachung][WikiStackTrace] an, die zum Aufruf führt.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Eine Stapelüberwachung" lightbox="../media/console-log-warning-expanded.msft.png":::
       Eine Stapelüberwachung  
    :::image-end:::  
    
    In der Stapelüberwachung wird Ihnen mitgeteilt, dass eine Funktion namens `logWarning` aufgerufen wurde, die wiederum eine Funktion mit dem Namen genannt wird `quoteDante` .  Anders ausgedrückt: der Aufruf, der sich zuerst ereignet hat, befindet sich am Ende der Stapelüberwachung.  Sie können Stack-Ablaufverfolgungen jederzeit durch Aufrufen protokollieren `console.trace()` .  

1.  Klicken Sie auf **Fehler protokollieren**.  Die folgende Fehlermeldung wird protokolliert: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Eine Fehlermeldung" lightbox="../media/console-log-error.msft.png":::
       Eine Fehlermeldung  
    :::image-end:::  
    
1.  Klicken Sie auf **Protokolltabelle**.  Eine Tabelle über berühmte Interpreten wird an der Konsole angemeldet.  
    
    > [!NOTE]
    > Die `birthday` Spalte wird nur für eine Zeile ausgefüllt.  Überprüfen Sie den Code, um zu ermitteln, warum dies der Grund ist.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Eine Tabelle in der Konsole" lightbox="../media/console-log-table.msft.png":::
       Eine Tabelle in der **Konsole**  
    :::image-end:::  
    
1.  Klicken Sie auf **Protokollgruppe**.  Unter dem Label sind die Namen von vier berühmten, kriminalisch bekämpften Schildkröten gruppiert `Adolescent Irradiated Espionage Tortoises` .  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Eine Gruppe von Nachrichten in der Konsole" lightbox="../media/console-log-group.msft.png":::
       Eine Gruppe von Nachrichten in der **Konsole**  
    :::image-end:::  
    
1.  Klicken Sie auf **Benutzerdefiniert protokollieren**.  Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird in der Konsole protokolliert.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole" lightbox="../media/console-log-custom.msft.png":::
       Eine Nachricht mit benutzerdefinierter Formatierung in der **Konsole**  
    :::image-end:::  
    
Der Grundgedanke hierbei ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten von Ihrem JavaScript-Konto in der Konsole protokollieren möchten `console` .  Jede Methode formatiert Nachrichten unterschiedlich.  

Es gibt noch mehr Methoden als das, was in diesem Abschnitt gezeigt wurde.  In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.  

## Anzeigen von vom Browser protokollierten Nachrichten   

Der Browser protokolliert auch Nachrichten an der Konsole.  Dies geschieht in der Regel, wenn ein Problem mit der Seite vorliegt.  

1.  Klicken Sie auf **Ursache 404**.  Der Browser protokolliert einen HTTP-Statuscode des `404` Netzwerkfehlers, weil das JavaScript der Seite versucht hat, eine Datei abzurufen, die nicht vorhanden ist.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ein 404-Fehler in der Konsole" lightbox="../media/console-cause-404.msft.png":::
       `404`Fehler in der **Konsole**  
    :::image-end:::  
    
1.  Klicken Sie auf **Fehler verursachen**.  Der Browser protokolliert eine nicht abgefangene `TypeError` , da JavaScript versucht, einen nicht vorhandenen DOM-Knoten zu aktualisieren.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Ein TypeError in der Konsole" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` in der **Konsole**  
    :::image-end:::  
    
1.  Klicken Sie auf die Dropdownliste **Protokollebenen** , und aktivieren Sie die Option **verbose** , wenn Sie deaktiviert ist.  Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.  Sie müssen dies tun, um sicherzustellen, dass die nächste Nachricht, die Sie protokollieren, sichtbar ist.  
    
    > [!NOTE]
    > Wenn die Dropdownliste Standardebenen deaktiviert ist, müssen Sie möglicherweise die Sidebar der **Konsole** schließen.  Filtern nach Nachrichtenquelle unten, um weitere Informationen zur Sidebar der **Konsole** zu erhalten.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Aktivieren der ausführlichen Protokollebene" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Aktivieren der ausführlichen Protokollebene  
    :::image-end:::  
    
1.  Klicken Sie auf **Verletzung verursachen**.  Die Seite reagiert für ein paar Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` auf der Konsole.  Die genaue Dauer kann variieren.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Eine Verletzung in der Konsole" lightbox="../media/console-cause-violation.msft.png":::
       Eine Verletzung in der **Konsole**  
    :::image-end:::  
    
## Filtern von Nachrichten   

Auf einigen Seiten wird die Konsole mit Nachrichten überschwemmt.  DevTools bietet viele verschiedene Methoden zum Filtern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.  

### Nach Protokollebene Filtern   

Jeder `console` Methode wird ein Schweregrad zugewiesen: `Verbose` , `Info` , `Warning` , oder `Error` .  Beispielsweise `console.log()` ist eine Nachricht auf einer `Info` Ebene, während `console.error()` die Nachricht auf eine `Error` Ebene lautet.  

1.  Klicken Sie auf die Dropdownliste **Protokollebenen** , und deaktivieren Sie **Fehler**.  Eine Ebene ist deaktiviert, wenn daneben kein Häkchen mehr vorhanden ist.  Die `Error` Nachrichten auf der Ebene verschwinden.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deaktivieren von Nachrichten auf Fehlerebene in der Konsole" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Deaktivieren von Nachrichten auf Fehlerebene in der **Konsole**  
    :::image-end:::  
    
1.  Klicken Sie erneut auf die Dropdownliste **Protokollebenen** , und aktivieren Sie dann **Fehler**erneut.  Die `Error` Nachrichten auf der Ebene werden erneut angezeigt.  

### Filtern nach Text   

Wenn Sie nur Nachrichten anzeigen möchten, die eine exakte Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.  

1.  Geben Sie `Dave` in das Textfeld **Filter** ein.  Alle Nachrichten, die die Zeichenfolge nicht enthalten, `Dave` werden ausgeblendet.  Möglicherweise wird auch die `Adolescent Irradiated Espionage Tortoises` Beschriftung angezeigt.  Das ist ein Fehler.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtern von Nachrichten, die Dave nicht enthalten" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtern von Nachrichten, die nicht enthalten sind `Dave`  
    :::image-end:::  
    
1.  Löschen `Dave` aus dem Textfeld " **Filter** "  Alle Nachrichten werden wieder angezeigt.  

### Nach regulärem Ausdruck filtern   

Wenn Sie alle Nachrichten anzeigen möchten, die anstelle einer bestimmten Zeichenfolge ein Textmuster enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].  

1.  Geben Sie `/^[AH]/` in das Textfeld **Filter** ein.  Geben Sie dieses Muster in [regexr][|::ref1::|Main] ein, um zu erläutern, was es tut.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtern von Nachrichten, die nicht dem Muster entsprechen `/^[AH]/`  
    :::image-end:::  
    
1.  Löschen `/^[AH]/` aus dem Textfeld " **Filter** "  Alle Nachrichten sind wieder sichtbar.  

### Nach Nachrichtenquelle Filtern   

Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammen, verwenden Sie die **Seitenleiste**.  

1.  Klicken Sie auf **Console Sidebar anzeigen** \ ( ![ Konsolen ][ImageShowConsoleSidebarIcon] -Sidebar anzeigen \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Die Seitenleiste" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Die Seitenleiste  
    :::image-end:::  
    
1.  Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) neben der Anzahl der Nachrichten.  In der folgenden Abbildung wird die Anzahl der Nachrichten als **13 Nachrichten**angezeigt.  Die **Seitenleiste** zeigt eine Liste der URLs, die dazu geführt haben, dass Nachrichten protokolliert werden.  Beispielsweise `log.js` verursachte 11 Nachrichten.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Anzeigen der Quelle von Nachrichten in der Seitenleiste" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Anzeigen der Quelle von Nachrichten in der Seitenleiste  
    :::image-end:::  
    
### Nach Benutzer Nachrichten filtern   

Wenn Sie zuvor auf **Protokollinformationen**geklickt haben, wurde ein Skript aufgerufen, um `console.log('Hello, Console!')` die Nachricht in der Konsole zu protokollieren.  Nachrichten, die von JavaScript wie diesem protokolliert werden, werden als **Benutzer Nachrichten**bezeichnet.  Wenn Sie hingegen auf **Ursache 404**geklickt haben, hat der Browser die Meldung auf eine Ebene protokolliert, `Error` die besagt, dass die angeforderte Ressource nicht gefunden wurde.  Nachrichten wie diese werden als **Browser Nachrichten**angesehen.  Verwenden Sie die **Seitenleiste** , um Browser Nachrichten zu filtern und nur Benutzer Nachrichten anzuzeigen.  

1.  Klicken Sie auf **9 Benutzer Nachrichten**.  Die Browser Nachrichten werden ausgeblendet.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtern von Browser Nachrichten" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtern von Browser Nachrichten  
    :::image-end:::  
    
1.  Klicken Sie auf **13 Nachrichten** , um alle Nachrichten erneut anzuzeigen.  

## Verwenden der Konsole neben einem anderen Panel   

Was passiert, wenn Sie Formatvorlagen bearbeiten, aber Sie müssen das Konsolenprotokoll schnell auf etwas überprüfen? Verwenden Sie die Schublade.  

1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Drücken Sie `Escape` .  Die Registerkarte "Konsole" des **Fachs** wird geöffnet.  Es enthält alle Features des Konsolen Panels, die Sie in diesem Lernprogramm verwendet haben.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Die Registerkarte ' Konsole ' im Einzug" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Die Registerkarte ' **Konsole** ' im **Einzug**  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

<!--
 


-->  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Position von Microsoft Edge devtools | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md "Konsolen Referenz | Microsoft docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung von Nachrichten | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "Regexr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stack-Trace – Wikipedia"  


> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
