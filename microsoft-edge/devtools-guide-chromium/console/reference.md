---
title: Konsolen Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601785"
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





# Konsolen Referenz   



Diese Seite ist eine Referenz zu Features, die sich auf die Microsoft Edge devtools-Konsole beziehen.  Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um aufgezeichnete Nachrichten anzuzeigen und JavaScript auszuführen.  Wenn dies nicht der Fall ist, lesen Sie [Erste Schritte mit der Ausführung von JavaScript in der Konsole][DevToolsConsoleJavascript] und erste [Schritte mit der Protokollierung von Nachrichten in der Konsole][DevToolsConsoleLog].  

Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` Siehe [Console API Reference][DevToolsConsoleApi]suchen.  Referenz für Funktionen wie `monitorEvents()` Siehe [API-Referenz für die Konsolen Dienstprogramme][DevToolsConsoleUtilities].  

## Öffnen der Konsole   

Sie können die Konsole als [Panel](#open-the-console-panel) oder als [Registerkarte im Einzug](#open-the-console-tab-in-the-drawer)öffnen.  

### Öffnen des Konsolen Panels   

Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).  

> ##### Abbildung1  
> Die Konsolen Leiste  
> ![Die Konsolen Leiste][ImageConsolePanel]  

Wenn Sie die Konsolen Leiste über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Panel** -Badge befindet.  

> ##### Abbildung2  
> Der Befehl zum Anzeigen des Konsolen Felds  
> ![Der Befehl zum Anzeigen des Konsolen Felds][ImageCommandShowConsole]  

### Öffnen der Registerkarte "Konsole" im Einzug   

Drücken `Escape` oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Konsolen Einzug anzeigen**aus.  

> ##### Abbildung 3  
> Konsolen Einzug anzeigen  
> ![Konsolen Einzug anzeigen][ImageShowConsoleDrawer]  

Die Schublade wird unten im devtools-Fenster eingeblendet, und die Registerkarte **Konsole** wird geöffnet.  

> ##### Abbildung4  
> Die Registerkarte ' Konsole ' im Einzug  
> ![Die Registerkarte ' Konsole ' im Einzug][ImageDrawerConsole]  

Wenn Sie die Registerkarte Konsole über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Einschub** Symbol neben dem Symbol befindet.  

> ##### Abbildung5  
> Befehl zum Anzeigen der Registerkarte "Konsole" im Einzug  
> ![Befehl zum Anzeigen der Registerkarte "Konsole" im Einzug][ImageShowDrawerCommand]  

### Öffnen von Konsoleneinstellungen   

Klicken **Sie auf Konsoleneinstellungen** ![ ][ImageSettingsButtonIcon] .  

> ##### Abbildung6  
> Konsoleneinstellungen  
> ![Konsoleneinstellungen][ImageConsoleSettings]  

Die folgenden Links erläutern jede Einstellung:  

*   [**Netzwerk ausblenden**](#hide-network-messages)  
*   [**Protokoll beibehalten**](#persist-messages-across-page-loads)  
*   [**Nur ausgewählter Kontext**](#filter-out-messages-from-different-contexts)  
*   [**Gruppieren ähnlich**](#disable-message-grouping)  
*   [**Protokollieren von XMLHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Eifrige Auswertung**](#disable-eager-evaluation)  
*   [**AutoVervollständigen aus Verlauf**](#disable-autocomplete-from-history)  

### Öffnen der Konsolen Leiste   

Klicken Sie auf **Console** Sidebar anzeigen, ![ ][ImageShowConsoleSidebarIcon] um die Seitenleiste anzuzeigen, die für das Filtern nützlich ist.  

> ##### Abbildung7  
> Konsolen Leiste  
> ![Konsolen Leiste][ImageConsoleSidebar]  

## Anzeigen von Nachrichten   

Dieser Abschnitt enthält Features, die ändern, wie Nachrichten in der Konsole angezeigt werden.  Weitere Informationen finden Sie unter [Anzeigen von Nachrichten][DevToolsConsoleViewMessages] für eine praktische Exemplarische Vorgehensweise.  

### Deaktivieren der Nachrichten Gruppierung   

[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie **Gruppe ähnlich** , um das Standardverhalten der Nachrichten Gruppierung der Konsole zu deaktivieren.  Ein Beispiel finden Sie unter [Protokoll XMLHttpRequest und Abrufen von Anforderungen](#log-xhr-and-fetch-requests) .  

### Protokollieren von XMLHttpRequest und Abrufen von Anforderungen   

[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie **Protokoll-XMLHttpRequests** , um alle `XMLHttpRequest` und `Fetch` Anforderungen an die Konsole während des Auftretens zu protokollieren.  

> ##### Abbildung8  
> Protokollierung `XMLHttpRequest` und `Fetch` Anforderungen  
> ![Protokollieren von XMLHttpRequest-und Fetch-Anforderungen][ImageXhrGrouped]  

Die oberste Nachricht in [Abbildung 8](#figure-8) zeigt das standardmäßige Gruppierungs Verhalten der Konsole.  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### Beibehalten von Nachrichten über Seitenlasten   

Standardmäßig wird die Konsole gelöscht, wenn Sie eine neue Seite laden.  Wenn Sie Nachrichten über Seitenlasten hinweg beibehalten möchten, öffnen Sie die [Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie dann das Kontrollkästchen **Protokoll beibehalten** .  

### Ausblenden von Netzwerknachrichten   

Standardmäßig protokolliert der Browser Netzwerknachrichten an die **Konsole**.  Beispielsweise stellt die ausgewählte Nachricht in [Abbildung 9](#figure-9) einen Statuscode von dar `429` .  

> ##### Abbildung 9  
> Eine 429-Nachricht in der Konsole  
> ! [Eine 429-Nachricht in der Konsole] [Image429Message]  

So blenden Sie Netzwerknachrichten aus:  

1.  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings).  
1.  Aktivieren Sie das Kontrollkästchen **Netzwerk ausblenden** .  

## Filtern von Nachrichten   

Es gibt viele Möglichkeiten, Nachrichten in der Konsole zu filtern.  

### Filtern von Browser Nachrichten   

[Öffnen Sie die Konsolen Leiste](#open-the-console-sidebar) , und klicken Sie auf **Benutzer Meldungen** , um nur Nachrichten anzuzeigen, die aus dem JavaScript der Seite stammen.  

> ##### Abbildung 10  
> Anzeigen von Benutzer Nachrichten  
> ! [Anzeigen von Benutzer Nachrichten] [ImageUserMessages]  

### Nach Protokollebene Filtern   

DevTools weist jeder `console.*` Methode einen Schweregrad zu.  Es gibt 4 Ebenen: `Verbose` , `Info` , `Warning` und `Error` .  Befindet sich beispielsweise `console.log()` in der `Info` Gruppe, während `console.error()` sich in der `Error` Gruppe befindet.  Die [API-Referenz][DevToolsConsoleApi] für die Konsole beschreibt den Schweregrad jeder anwendbaren Methode.  Jede Nachricht, die der Browser auf der Konsole anmeldet, hat auch einen Schweregrad.  Sie können jede Ebene von Nachrichten verbergen, an denen Sie nicht interessiert sind.  Wenn Sie beispielsweise nur an `Error` Nachrichten interessiert sind, können Sie die anderen drei Gruppen ausblenden.  

Klicken Sie auf die Dropdownliste **Protokollebenen** , um die Option oder `Verbose` `Info` `Warning` `Error` Nachrichten zu aktivieren oder zu deaktivieren.  

> ##### Abbildung 11  
> Dropdownliste " **Protokollebenen** "  
> ! [Protokollebenen-Dropdown] [ImageLogLevels]  

Sie können auch nach Protokollebene filtern, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar) und dann auf **Fehler**, **Warnungen**, **Informationen**oder **ausführlich**klicken.  

> ##### Abbildung 12  
> Verwenden der Seitenleiste zum Anzeigen von Warnungen  
> ! [Verwenden der Seitenleiste zum Anzeigen von Warnungen] [ImageSidebarWarnings]  

### Filtern von Nachrichten nach URL   

Geben `url:` Sie gefolgt von einer URL ein, um nur Nachrichten anzuzeigen, die von dieser URL stammen.  Nachdem Sie devtools eingegeben haben `url:` , werden alle relevanten URLs angezeigt.  Domänen funktionieren ebenfalls.  Wenn Sie beispielsweise `https://example.com/a.js` `https://example.com/b.js` Nachrichten protokollieren, `url:https://example.com` können Sie sich auf die Nachrichten aus diesen beiden Skripts konzentrieren.  

> ##### Abbildung 13  
> Ein URL-Filter  
> ! [Ein URL-Filter] [ImageUrlFilter]  

Geben `-url:` Sie ein, um Nachrichten aus dieser URL auszublenden.  Dies wird als negativer URL-Filter bezeichnet.  

> ##### Abbildung 14  
> Ein negativer URL-Filter, der alle Nachrichten ausblendet, die der URL entsprechen `https://b.wal.co`  
> ! [Ein negativer URL-Filter, der alle Nachrichten ausblendet, die der URL entsprechen https://b.wal.co ] [ImageNegativeUrlFilter1]  

Sie können auch Nachrichten von einer einzelnen URL anzeigen, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar), den Abschnitt **Benutzer Nachrichten** erweitern und dann auf die URL des Skripts klicken, das die Nachrichten enthält, auf die Sie sich konzentrieren möchten.  

> ##### Abbildung 15  
> Anzeigen der von Ihnen gelieferten Nachrichten `wp-ad.min.js`  
> ! [Anzeigen der Nachrichten, die von WP-AD. min. js stammen] [ImageNegativeUrlFilter2]  

### Filtern von Nachrichten aus unterschiedlichen Kontexten   

Angenommen, Sie haben eine Anzeige \ (AD \) auf Ihrer Seite.  Die Anzeige ist in eine eingebettete `<iframe>` und generiert viele Nachrichten in der Konsole.  Da die Anzeige in einem anderen JavaScript- [Kontext](#select-javascript-context)ausgeführt wird, besteht eine Möglichkeit zum Ausblenden der Nachrichten darin, die [Konsoleneinstellungen zu öffnen](#open-console-settings) und das Kontrollkästchen **nur ausgewählten Kontext** zu aktivieren.  

### Filtern von Nachrichten, die nicht mit einem regulären Ausdrucksmuster übereinstimmen   

Geben Sie einen regulären Ausdruck wie `/[gm][ta][mi]/` im Textfeld **Filter** ein, um alle Nachrichten zu filtern, die nicht mit diesem Muster übereinstimmen.  DevTools überprüft, ob das Muster im Nachrichtentext gefunden wurde, oder das Skript, das die Protokollierung der Nachricht verursacht hat.  

> ##### Abbildung 16  
> Filtern von Nachrichten, die nicht übereinstimmen `/[gm][ta][mi]/`  
> ! [Filtern von Nachrichten, die nicht mit dem Regex-Ausdruck übereinstimmen] [ImageRegExFilter]  

## Ausführen von JavaScript   

Dieser Abschnitt enthält Features in Bezug auf die Ausführung von JavaScript in der Konsole.  Eine praktische Exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevToolsConsoleOverviewJavascript] .  

### Erneutes Ausführen von Ausdrücken aus dem Protokoll   

Drücken Sie die Eingabe `Up Arrow` Taste, um den Verlauf der JavaScript-Ausdrücke zu durchlaufen, die Sie zuvor in der Konsole ausgeführt haben.  Drücken Sie, `Enter` um diesen Ausdruck erneut auszuführen.  

### Überwachen des Werts eines Ausdrucks in Echtzeit mit Live Ausdrücken   

Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.  Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.  Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.  Informationen finden Sie unter Anzeigen von [Werten für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken][DevToolsConsoleLiveExpressions].  

### Deaktivieren der eifrigen Auswertung   

Während Sie JavaScript-Ausdrücke in der Konsole eingeben, zeigt die **eifrige Auswertung** eine Vorschau des Rückgabewerts für diesen Ausdruck.  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **eifrige Auswertung** , um die Vorschau des Rückgabewerts zu deaktivieren.  

### Deaktivieren von AutoVervollständigen aus dem Protokoll   

Wenn Sie einen Ausdruck eingeben, zeigt das Popupfenster AutoVervollständigen für die Konsole Ausdrücke an, die Sie zuvor ausgeführt haben.  Diesen Ausdrücken wird das Zeichen vorangestellt `>` .  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **AutoVervollständigen aus Verlauf** , um die Anzeige von Ausdrücken aus Ihrem Protokoll zu beenden.  

> [!NOTE]
> In [Abbildung 17](#figure-17) `document.querySelector('a')` `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.  

> ##### Abbildung 17  
> Das AutoVervollständigen-Popup, das Ausdrücke aus dem Protokoll zeigt  
> ! [AutoVervollständigen-Popup mit Ausdrücken aus dem Protokoll] [ImageHistoryAutocomplete]  

### JavaScript-Kontext auswählen   

Standardmäßig ist die Dropdownliste **JavaScript-Kontext** auf **oben**gesetzt, was den [Browserkontext][MDNBrowsingContext] des Hauptdokuments darstellt.  

> ##### Abbildung 18  
> Die **JavaScript-Kontext** Dropdownliste  
> ! [Der JavaScript-Kontext-Dropdown] [Imagejavascriptcontext]  

Angenommen, Sie haben eine Anzeige auf Ihrer Seite eingebettet in eine `<iframe>` .  Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.  Wählen Sie zuerst den Browserkontext der Anzeige aus der Dropdownliste **JavaScript-Kontext** aus.  

> ##### Abbildung 19  
> Auswählen eines anderen JavaScript-Kontexts  
> ! [Auswählen eines anderen JavaScript-Kontexts] [Imageselectcontext]  

## Deaktivieren der Konsole   

Sie können eine der folgenden Workflows verwenden, um die Konsole zu löschen:  

*   Klicken **Sie auf Konsole löschen** ![ ][ImageClearConsoleIcon] .  
*   Klicken Sie mit der rechten Maustaste auf eine Nachricht, und wählen Sie **Konsole löschen**aus.  
*   Geben `clear()` Sie die Konsole ein, und drücken Sie dann `Enter` .  
*   Rufen `console.clear()` Sie über das JavaScript für Ihre Webseite an.  
*   Drücken Sie `Control` + `L` , während sich die Konsole im Fokus befindet.  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Abbildung 1: die Konsolen Leiste"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Abbildung 2: der Befehl zum Anzeigen des Konsolenbereichs"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Abbildung 3: Anzeigen der Konsolen Schublade"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Abbildung 4: die Registerkarte "Konsole" im Einzug"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Abbildung 5: der Befehl zum Anzeigen der Registerkarte "Konsole" im Einzug"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Abbildung 6: Konsoleneinstellungen"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Abbildung 7: Konsolen-Seitenleiste"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Abbildung 8: Protokollieren von XMLHttpRequest-und Fetch-Anforderungen"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Show-Network.msft.png "Abbildung 9: eine 429-Meldung in der Konsole"  
[ImageUserMessages]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-drawer-user-messages.msft.png "Abbildung 10: Anzeigen von Benutzer Nachrichten"  
[ImageLogLevels]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Level-default-Levels.msft.png "Abbildung 11: die Dropdownliste" Protokollebenen "  
[ImageSidebarWarnings]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Warnings.msft.png "Abbildung 12: Verwenden der Seitenleiste zum Anzeigen von Warnungen"  
[ImageUrlFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text.msft.png "Abbildung 13: ein URL-Filter"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-negative-Filter-Text.msft.png "Abbildung 14: ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der URL übereinstimmen https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-specified.msft.png "Abbildung 15: Anzeigen der Nachrichten, die von WP-AD. min. js stammen"  
[ImageRegExFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Regex.msft.png "Abbildung 16: Filtern von Nachrichten, die nicht mit dem Regex-Ausdruck übereinstimmen"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Filter-Text-AutoFilter-History.msft.png "Abbildung 17: das AutoVervollständigen-Popup, in dem Ausdrücke aus dem Verlauf angezeigt werden"  
[Imagejavascriptcontext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-Top.msft.png "Abbildung 18: die JavaScript-Kontext Dropdownliste"  
[Imageselectcontext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-DOM-Level-Multiple.msft.png "Abbildung 19: Auswählen eines anderen JavaScript-Kontexts"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Anzeigen von protokollierten Nachrichten – Übersicht über die Konsole"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Ausführen von JavaScript – Übersicht über die Konsole"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Erste Schritte mit der Ausführung von JavaScript in der Konsole"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "API-Referenz für Konsolen Dienstprogramme"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browsing-Kontext | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
