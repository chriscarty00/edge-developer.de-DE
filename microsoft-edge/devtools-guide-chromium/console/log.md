---
description: Erfahren Sie, wie Sie Nachrichten an der Konsole protokollieren.
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439289"
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

# <a name="get-started-with-logging-messages-in-the-console"></a>Erste Schritte mit der Protokollierung von Nachrichten in der Konsole  

In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge DevTools-Konsole][MicrosoftEdgeDevTools] protokollieren und filtern.  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Nachrichten in der **Konsole**  
:::image-end:::  

Dieses Lernprogramm soll in der Reihenfolge abgeschlossen werden.  Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, z. B. die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.  

## <a name="set-up-the-demo-and-devtools"></a>Einrichten der Demo und DevTools  

Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.  Wenn Sie physisch folgen, werden Sie sich die Workflows wahrscheinlich später merken.  

1.  Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **Konsolenprotokollbeispiele** aus, um auf einer neuen Registerkarte zu öffnen.  
    
    [Beispiele für Konsolenprotokolle][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Fokussieren Sie die Demo, und wählen Sie `Control` + `Shift` + `J` dann \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um DevTools zu öffnen.  Standardmäßig wird DevTools rechts neben der Demo geöffnet.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools wird rechts neben der Demo geöffnet" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools wird rechts neben der Demo geöffnet  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Dock DevTools am unteren Rand des Fensters][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools am Unteren Rand der Demo angedockt" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools am Unteren Rand der Demo angedockt  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Trennen Sie DevTools in ein separates Fenster.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Browser in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Browser in einem separaten Fenster  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Trennen Sie DevTools in ein separates Fenster.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools in einem separaten Fenster entdockt" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools in einem separaten Fenster entdockt  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a>Anzeigen von Nachrichten, die von JavaScript protokolliert wurden  

Die meisten Nachrichten, die in der Konsole angezeigt **werden,** stammen von den Webentwicklern, die das JavaScript der Seite geschrieben haben.  Das Ziel dieses Abschnitts besteht in der Einführung in die verschiedenen Nachrichtentypen, die Sie wahrscheinlich in der **Konsole**überprüfen werden, und zu erläutern, wie Sie jeden Nachrichtentyp selbst aus Ihrem eigenen JavaScript protokollieren können.  

1.  Wählen Sie in der Demo die Schaltfläche **Protokollinformationen** aus.  `Hello, Console!` wird bei der Konsole protokolliert.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Die Konsole nach der Auswahl von Protokollinformationen" lightbox="../media/console-log-info.msft.png":::
       Die **Konsole** nach der Auswahl von **Protokollinformationen**  
    :::image-end:::  
    
1.  Wählen Sie neben `Hello, Console!` der Nachricht in der Konsole **log.js:2 aus.**  Der Bereich Quellen wird geöffnet und die Codezeile hervorgehoben, die dazu führte, dass die Nachricht bei der Konsole protokolliert wurde.  Die Nachricht wurde protokolliert, als das JavaScript der Seite angezeigt `console.log('Hello, Console!')` wurde.
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools öffnet das Sources-Tool, nachdem Sie log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools öffnet das **Tool "Quellen",** nachdem Sie die Option `log.js:2`  
    :::image-end:::  
    
1.  Navigieren Sie mithilfe **eines** der folgenden Workflows zurück zur Konsole:  
    
    *   Wählen Sie das **Konsolentool** aus.  
    *   Wählen `Control` + `[` Sie \(Windows, Linux\) oder `Command` + `[` \(macOS\) aus, bis das **Konsolentool** im Fokus steht.  
    *   [Öffnen Sie das Befehlsmenü,][DevToolsCommandMenu] `Console` geben Sie ein, wählen Sie den Befehl **Konsolenbereich** anzeigen aus, und wählen Sie dann `Enter` aus.  
    
1.  Wählen Sie **in der Demo** die Schaltfläche Protokollwarnung aus.  `Abandon Hope All Ye Who Enter` wird bei der Konsole **protokolliert.**  Nachrichten, die so formatiert sind, sind Warnungen.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Die Konsole nach der Auswahl der Protokollwarnung" lightbox="../media/console-log-warning.msft.png":::
       Die **Konsole** nach der Auswahl der **Protokollwarnung**  
    :::image-end:::  
    
    > [!TIP]
    > Wenn Sie den Code anzeigen möchten, der dazu führte, dass eine Nachricht auf eine bestimmte Weise protokolliert wurde, wählen Sie ein Skript \(z. B. \) aus, um den Code zu sehen, der dazu führte, dass die Nachricht `log.js:12` formatiert wurde.  

1.  Wählen Sie **das Symbol Erweitern** \( Erweitern ![ ](../media/expand-icon.msft.png) \) vor `Abandon Hope All Ye Who Enter` aus.  DevTools zeigt die [Stapelverfolgung an,][WikiStackTrace] die zum Aufruf führt.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Eine Stapelverfolgung" lightbox="../media/console-log-warning-expanded.msft.png":::
       Eine Stapelverfolgung  
    :::image-end:::  
    
    Die Stapelverfolgung gibt an, dass eine Funktion namens ausgeführt wird, die `logWarning` wiederum eine Funktion mit dem Namen ausgeführt `quoteDante` wird.  Mit anderen Worten, die Anforderung, die zuerst passiert ist, befindet sich am unteren Rand der Stapelverfolgung.  Sie können Stapelverfolgungen jederzeit protokollieren, indem Sie `console.trace()` ausführen.  

1.  Wählen **Sie Protokollfehler aus.**  Die folgende Fehlermeldung wird protokolliert: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Eine Fehlermeldung" lightbox="../media/console-log-error.msft.png":::
       Eine Fehlermeldung  
    :::image-end:::  
    
1.  Wählen **Sie Protokolltabelle**aus.  Eine Tabelle über bekannte Künstler wird bei der Konsole **protokolliert.**  
    
    > [!NOTE]
    > Die `birthday` Spalte wird nur für eine Zeile aufgefüllt.  Überprüfen Sie den Code, um zu ermitteln, warum dies der Grund ist.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Eine Tabelle in der Konsole" lightbox="../media/console-log-table.msft.png":::
       Eine Tabelle in der **Konsole**  
    :::image-end:::  
    
1.  Wählen **Sie Protokollgruppe aus.**  Die Namen von 4 bekannten Schildkröten zur Bekämpfung von Straftaten werden unter der Bezeichnung `Adolescent Irradiated Espionage Tortoises` gruppieren.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Eine Gruppe von Nachrichten in der Konsole" lightbox="../media/console-log-group.msft.png":::
       Eine Gruppe von Nachrichten in der **Konsole**  
    :::image-end:::  
    
1.  Wählen **Sie Log Custom aus.**  Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird bei der Konsole protokolliert.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole" lightbox="../media/console-log-custom.msft.png":::
       Eine Nachricht mit benutzerdefinierter Formatierung in der **Konsole**  
    :::image-end:::  
    
Die Hauptidee hier ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten über Ihr JavaScript an der Konsole `console` protokollieren möchten.  Jede Methode formatiert Nachrichten unterschiedlich.  

Es gibt noch mehr Methoden als in diesem Abschnitt gezeigt.  In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.  

## <a name="view-messages-logged-by-the-browser"></a>Vom Browser protokollierte Nachrichten anzeigen  

Der Browser protokolliert nachrichten auch an der Konsole.  Dies geschieht in der Regel, wenn ein Problem mit der Seite vor liegt.  

1.  Wählen **Sie Ursache 404 aus.**  Der Browser protokolliert einen HTTP-Statuscode des Netzwerkfehlers, da das JavaScript der Seite versucht hat, eine datei zu abrufen, die `404` nicht vorhanden ist.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ein 404-Fehler in der Konsole" lightbox="../media/console-cause-404.msft.png":::
       Ein `404` Fehler in der **Konsole**  
    :::image-end:::  
    
1.  Wählen **Sie Ursache Fehler aus.**  Der Browser protokolliert einen nicht abgefangenen Knoten, da javaScript versucht, `TypeError` einen nicht vorhandenen DOM-Knoten zu aktualisieren.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Ein TypeError in der Konsole" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` in der **Konsole**  
    :::image-end:::  
    
1.  Wählen Sie **das Dropdownmenü Protokollebenen** aus, und aktivieren Sie die **Option Verbose,** wenn sie deaktiviert ist.  Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.  Sie müssen dies tun, um sicherzustellen, dass die nächste nachricht, die Sie protokollieren, sichtbar ist.  
    
    > [!NOTE]
    > Wenn das Dropdownmenü Standardebenen deaktiviert ist, müssen Sie möglicherweise die **Konsolenseite** schließen.  Filtern Sie unten nach Nachrichtenquelle, um weitere Informationen zur **Konsolen-Sidebar** zu erhalten.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Aktivieren der ausführlichen Protokollebene" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Aktivieren der ausführlichen Protokollebene  
    :::image-end:::  
    
1.  Wählen Sie **Ursache Verletzung aus.**  Die Seite reagiert für einige Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` an der Konsole.  Die genaue Dauer kann variieren.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Ein Verstoß in der Konsole" lightbox="../media/console-cause-violation.msft.png":::
       Ein Verstoß in der **Konsole**  
    :::image-end:::  
    
## <a name="filter-messages"></a>Filtern von Nachrichten  

Auf einigen Webseiten wird **** die Konsole mit Nachrichten überflutet.  DevTools bietet viele verschiedene Möglichkeiten zum Herausfiltern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.  

### <a name="filter-by-log-level"></a>Filtern nach Protokollebene  

Jeder `console` Methode wird ein Schweregrad zugewiesen: , , oder `Verbose` `Info` `Warning` `Error` .  Beispielsweise handelt es `console.log()` sich um eine Nachricht auf `Info` Ebene, während es sich um eine `console.error()` Nachricht auf `Error` -Ebene handelt.  

1.  Wählen Sie **das Dropdownmenü Protokollebenen** aus, und deaktivieren Sie **Fehler.**  Eine Ebene ist deaktiviert, wenn kein Häkchen mehr daneben ist.  Die `Error` Nachrichten auf -Ebene werden nicht mehr angezeigt.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deaktivieren von Nachrichten auf Fehlerebene in der Konsole" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Deaktivieren von Nachrichten auf Fehlerebene in der **Konsole**  
    :::image-end:::  
    
1.  Wählen Sie **erneut das Dropdownmenü** Protokollebenen aus, und aktivieren Sie **Fehler erneut.**  Die `Error` Nachrichten auf -Ebene werden erneut angezeigt.  

### <a name="filter-by-text"></a>Filtern nach Text  

Wenn Sie nur Nachrichten anzeigen möchten, die eine genaue Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.  

1.  Geben `Dave` Sie in das Textfeld **Filter** ein.  Alle Nachrichten, die die Zeichenfolge nicht `Dave` enthalten, werden ausgeblendet.  Sie können auch die Bezeichnung `Adolescent Irradiated Espionage Tortoises` überprüfen.  Dies ist ein Fehler.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtern sie alle Nachrichten heraus, die Dave nicht enthalten" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtern von Nachrichten, die nicht enthalten sind `Dave`  
    :::image-end:::  
    
1.  Löschen `Dave` sie **** aus dem Textfeld Filter.  Alle Nachrichten werden erneut angezeigt.  

### <a name="filter-by-regular-expression"></a>Filtern nach regulärem Ausdruck  

Wenn Sie alle Nachrichten anzeigen möchten, die ein Textmuster anstelle einer bestimmten Zeichenfolge enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].  

1.  Geben `/^[AH]/` Sie in das Textfeld **Filter** ein.  Geben Sie das Muster in [RegExr ein,][|::ref1::|Main] um eine Erläuterung ihrer Aktivitäten zu erhalten.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtern von Nachrichten, die nicht mit dem Muster übereinstimmen `/^[AH]/`  
    :::image-end:::  
    
1.  Löschen `/^[AH]/` sie **** aus dem Textfeld Filter.  Alle Nachrichten sind wieder sichtbar.  

### <a name="filter-by-message-source"></a>Filtern nach Nachrichtenquelle  

Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammten, verwenden Sie die **Sidebar**.  

1.  Wählen **Sie Konsolenseite anzeigen** \( ![ Konsolenseite anzeigen ](../media/show-console-sidebar-icon.msft.png) \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Die Seitenleiste" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Die Seitenleiste  
    :::image-end:::  
    
1.  Wählen Sie **das Symbol Erweitern** \( Erweitern ![ ](../media/expand-icon.msft.png) \) neben der Anzahl der Nachrichten aus.  In der folgenden Abbildung wird die Anzahl der Nachrichten als **13 Nachrichten angegeben.**  Die **Seitenleiste** zeigt eine Liste der URLs an, die dazu führte, dass Nachrichten protokolliert wurden.  Beispielsweise wurden `log.js` 11 Nachrichten verursacht.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Anzeigen der Nachrichtenquelle in der Seitenleiste" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Anzeigen der Nachrichtenquelle in der Seitenleiste  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a>Filtern nach Benutzernachrichten  

Wenn Sie zuvor Log **Info**auswählen, ein Skript mit dem Namen, um die Nachricht bei `console.log('Hello, Console!')` der Konsole zu protokollieren.  Nachrichten, die von JavaScript wie diesem protokolliert werden, sind **benannte Benutzernachrichten.**  Wenn Sie dagegen Ursache **404**auswählen, protokolliert der Browser eine Meldung auf -Ebene, die besagt, dass die `Error` angeforderte Ressource nicht gefunden wird.  Nachrichten wie diese werden als **Browsernachrichten betrachtet.**  Verwenden Sie **die Seitenleiste,** um Browsernachrichten herausfiltern und nur Benutzernachrichten anzuzeigen.  

1.  Wählen **Sie 9 Benutzernachrichten aus.**  Die Browsernachrichten werden ausgeblendet.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtern von Browsernachrichten" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtern von Browsernachrichten  
    :::image-end:::  
    
1.  Wählen **Sie 13 Nachrichten aus,** um alle Nachrichten erneut zu zeigen.  

## <a name="use-the-console-alongside-any-other-tools"></a>Verwenden der Konsole zusammen mit anderen Tools  

Wenn Sie Formatvorlagen bearbeiten, aber schnell im Konsolenprotokoll nach etwas suchen müssen, verwenden Sie die Drawer.  

1.  Wählen Sie das **Elementtool** aus.  
1.  Wählen Sie `Escape` aus.  Das **Konsolentool** in **der Schublade** wird geöffnet.  Es verfügt über alle Features des Konsolenbereichs, die Sie in diesem Lernprogramm verwendet haben.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Das **Konsolentool** in **der Schublade**  
    :::image-end:::  
    
## <a name="see-also"></a>Weitere Informationen  

*   Weitere Features und Workflows im **** Zusammenhang mit der Konsolenbenutzeroberfläche finden Sie unter [Konsolenreferenz][DevToolsConsoleApi].  
*   Weitere Informationen zu allen methoden, die in View `console` messages logged from [JavaScript](#view-messages-logged-from-javascript) gezeigt werden, und die anderen Methoden, die in diesem Artikel nicht behandelt werden, finden Sie unter `console` Console API [Reference][DevToolsConsoleReference].  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) developer tools | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Platzierung von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Konsolenreferenz | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stapelverfolgung – Wikipedia"  
> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
