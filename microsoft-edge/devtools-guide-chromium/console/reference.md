---
description: Eine umfassende Referenz zu jedem Feature und Verhalten im Zusammenhang mit der Konsolen-UI in Microsoft Edge devtools
title: Konsolen Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125258"
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

Diese Seite ist eine Referenz zu Features, die sich auf die Microsoft Edge devtools-Konsole beziehen.  Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um aufgezeichnete Nachrichten anzuzeigen und JavaScript auszuführen.  Wenn dies nicht der Fall ist, navigieren Sie zu erste [Schritte mit der Ausführung von JavaScript in der Konsole][DevToolsConsoleJavascript] , und [beginnen Sie mit der Protokollierung von Nachrichten in der Konsole][DevToolsConsoleLog].  

Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` Siehe [Console API Reference][DevToolsConsoleApi]suchen.  Wenn Sie auf Funktionen wie verweisen möchten `monitorEvents()` , navigieren Sie zu [API-Referenz für Konsolen Dienstprogramme][DevToolsConsoleUtilities].  

## Öffnen der Konsole  

Sie können die Konsole als [Panel](#open-the-console-panel) oder als [Registerkarte im Einzug](#open-the-console-tab-in-the-drawer)öffnen.  

### Öffnen des Konsolen Panels  

Wählen Sie `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) aus.  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-hello-console.msft.png":::
   Die **Konsolen** Leiste  
:::image-end:::  

Wenn Sie die Konsolen Leiste über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Panel** -Badge befindet.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-command-menu-show-console.msft.png":::
   Der Befehl zum Anzeigen des **Konsolen** Panels  
:::image-end:::  

### Öffnen der Registerkarte "Konsole" im Einzug  

Wählen Sie `Escape` **devtools anpassen und Steuern** aus, und `...` Klicken Sie dann auf **Konsolen Einzug anzeigen**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Konsolen Einzug anzeigen**  
:::image-end:::  

Die Schublade wird unten im devtools-Fenster eingeblendet, und die Registerkarte **Konsole** wird geöffnet.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Die Registerkarte ' **Konsole** ' im **Einzug**  
:::image-end:::  

Wenn Sie die Registerkarte Konsole über das [Befehlsmenü][DevToolsCommandMenu]öffnen möchten, beginnen Sie mit der Eingabe, `Console` und führen Sie dann den Befehl **Konsole anzeigen** aus, auf dem sich das **Einschub** Symbol neben dem Symbol befindet.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-command-menu-show-console.msft.png":::
   Der Befehl zum Anzeigen der Registerkarte " **Konsole** " im **Einzug**  
:::image-end:::  

### Öffnen von Konsoleneinstellungen  

Wählen Sie **Konsoleneinstellungen** \ ( ![ Symbol für Konsoleneinstellungen ][ImageSettingsButtonIcon] \) aus.  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Konsoleneinstellungen**  
:::image-end:::  

Die folgenden Links erläutern jede Einstellung:  

*   [**Netzwerk ausblenden**](#hide-network-messages)  
*   [**Protokoll beibehalten**](#persist-messages-across-page-loads)  
*   [**Nur ausgewählter Kontext**](#filter-out-messages-from-different-contexts)  
*   [**Gruppieren ähnlich**](#disable-message-grouping)  
*   [**Protokollieren von XMLHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Eifrige Auswertung**](#disable-eager-evaluation)  
*   [**AutoVervollständigen aus Verlauf**](#disable-autocomplete-from-history)  
    
### Öffnen der Konsolen Leiste  

Wählen Sie **Console Sidebar anzeigen** aus ![ ][ImageShowConsoleSidebarIcon] , um die Seitenleiste anzuzeigen, die für das Filtern nützlich ist.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console** Seitenleiste  
:::image-end:::  

## Anzeigen von Nachrichten  

Dieser Abschnitt enthält Features, die ändern, wie Nachrichten in der Konsole angezeigt werden.  Weitere Informationen finden Sie unter [Anzeigen von Nachrichten][DevToolsConsoleViewMessages] für eine praktische Exemplarische Vorgehensweise.  

### Deaktivieren der Nachrichten Gruppierung  

[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie **Gruppe ähnlich** , um das Standardverhalten der Nachrichten Gruppierung der Konsole zu deaktivieren.  Ein Beispiel finden Sie unter [Protokoll XMLHttpRequest und Abrufen von Anforderungen](#log-xhr-and-fetch-requests) .  

### Protokollieren von XMLHttpRequest und Abrufen von Anforderungen  

[Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie **Protokoll-XMLHttpRequests** , um alle `XMLHttpRequest` und `Fetch` Anforderungen an die Konsole während des Auftretens zu protokollieren.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-xhr-fetch.msft.png":::
   Protokoll `XMLHttpRequest` und `Fetch` Anforderungen  
:::image-end:::  
Die oberste Nachricht in der vorherigen Abbildung zeigt das standardmäßige Gruppierungs Verhalten der **Konsole**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### Beibehalten von Nachrichten über Seitenlasten  

Standardmäßig wird die Konsole gelöscht, wenn Sie eine neue Seite laden.  Wenn Sie Nachrichten über Seitenlasten hinweg beibehalten möchten, öffnen Sie die [Konsoleneinstellungen](#open-console-settings) , und aktivieren Sie dann das Kontrollkästchen **Protokoll beibehalten** .  

### Ausblenden von Netzwerknachrichten  

Standardmäßig protokolliert der Browser Netzwerknachrichten an die **Konsole**.  In der folgenden Abbildung stellt die ausgewählte Nachricht einen HTTP-Statuscode von dar `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-show-network.msft.png":::
   Eine `429` Nachricht in der **Konsole**  
:::image-end:::  
So blenden Sie Netzwerknachrichten aus:  

1.  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings).  
1.  Aktivieren Sie das Kontrollkästchen **Netzwerk ausblenden** .  
    
## Filtern von Nachrichten  

Es gibt viele Möglichkeiten, Nachrichten in der Konsole zu filtern.  

### Filtern von Browser Nachrichten  

[Öffnen Sie die Konsolen Leiste](#open-the-console-sidebar) , und wählen Sie **Benutzer Nachrichten** aus, um nur Nachrichten anzuzeigen, die aus dem JavaScript der Seite stammen.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Anzeigen von Benutzer Nachrichten  
:::image-end:::  

### Nach Protokollebene Filtern  

DevTools weist jeder `console.*` Methode einen Schweregrad zu.  Es gibt 4 Ebenen: `Verbose` , `Info` , `Warning` und `Error` .  Befindet sich beispielsweise `console.log()` in der `Info` Gruppe, während `console.error()` sich in der `Error` Gruppe befindet.  Die [API-Referenz][DevToolsConsoleApi] für die Konsole beschreibt den Schweregrad jeder anwendbaren Methode.  Jede Nachricht, die der Browser auf der Konsole anmeldet, hat auch einen Schweregrad.  Sie können jede Ebene von Nachrichten verbergen, an denen Sie nicht interessiert sind.  Wenn Sie beispielsweise nur an `Error` Nachrichten interessiert sind, können Sie die anderen drei Gruppen ausblenden.  

Klicken Sie auf die Dropdownliste **Protokollebenen** , um die Option oder `Verbose` `Info` `Warning` `Error` Nachrichten zu aktivieren oder zu deaktivieren.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-log-level-default-levels.msft.png":::
   Dropdownliste " **Protokollebenen** "  
:::image-end:::  

Sie können auch nach Protokollebene filtern, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar) und dann auf **Fehler**, **Warnungen**, **Informationen**oder **ausführlich**klicken.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   Verwenden der Seitenleiste zum Anzeigen von Warnungen  
:::image-end:::  

### Filtern von Nachrichten nach URL  

Geben `url:` Sie gefolgt von einer URL ein, um nur Nachrichten anzuzeigen, die von dieser URL stammen.  Nachdem Sie devtools eingegeben haben `url:` , werden alle relevanten URLs angezeigt.  Domänen funktionieren ebenfalls.  Wenn Sie beispielsweise `https://example.com/a.js` `https://example.com/b.js` Nachrichten protokollieren, `url:https://example.com` können Sie sich auf die Nachrichten aus diesen beiden Skripts konzentrieren.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text.msft.png":::
   Ein URL-Filter  
:::image-end:::  

Geben `-url:` Sie ein, um Nachrichten aus dieser URL auszublenden.  Dies wird als negativer URL-Filter bezeichnet.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-negative-filter-text.msft.png":::
   Ein negativer URL-Filter, mit dem alle Nachrichten ausgeblendet werden, die der `https://b.wal.co` URL entsprechen
:::image-end:::  

Sie können auch Nachrichten von einer einzelnen URL anzeigen, indem Sie [die Konsolen Leiste öffnen](#open-the-console-sidebar), den Abschnitt **Benutzer Nachrichten** erweitern und dann auf die URL des Skripts klicken, das die Nachrichten enthält, auf die Sie sich konzentrieren möchten.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text-specified.msft.png":::
   Anzeigen der von Ihnen gelieferten Nachrichten `wp-ad.min.js`  
:::image-end:::  

### Filtern von Nachrichten aus unterschiedlichen Kontexten  

Angenommen, Sie haben eine Anzeige \ (AD \) auf Ihrer Seite.  Die Anzeige ist in eine eingebettete `<iframe>` und generiert viele Nachrichten in der Konsole.  Da die Anzeige in einem anderen JavaScript- [Kontext](#select-javascript-context)ausgeführt wird, besteht eine Möglichkeit zum Ausblenden der Nachrichten darin, die [Konsoleneinstellungen zu öffnen](#open-console-settings) und das Kontrollkästchen **nur ausgewählten Kontext** zu aktivieren.  

### Filtern von Nachrichten, die nicht mit einem regulären Ausdrucksmuster übereinstimmen  

Geben Sie einen regulären Ausdruck wie `/[gm][ta][mi]/` im Textfeld **Filter** ein, um alle Nachrichten zu filtern, die nicht mit diesem Muster übereinstimmen.  DevTools überprüft, ob das Muster im Nachrichtentext gefunden wurde, oder das Skript, das die Protokollierung der Nachricht verursacht hat.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-regex.msft.png":::
   Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` Regex-Ausdruck übereinstimmen  
:::image-end:::  

## Ausführen von JavaScript  

Dieser Abschnitt enthält Features in Bezug auf die Ausführung von JavaScript in der Konsole.  Eine praktische Exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevToolsConsoleOverviewJavascript] .  

### Erneutes Ausführen von Ausdrücken aus dem Protokoll  

Drücken Sie die Eingabe `Up Arrow` Taste, um den Verlauf der JavaScript-Ausdrücke zu durchlaufen, die Sie zuvor in der Konsole ausgeführt haben.  Wählen Sie diese Option aus, `Enter` um diesen Ausdruck erneut auszuführen.  

### Überwachen des Werts eines Ausdrucks in Echtzeit mit Live Ausdrücken  

Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.  Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.  Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.  Schauen Sie [sich die Werte für JavaScript-Ausdrücke in Real-Time mit Live Ausdrücken an][DevToolsConsoleLiveExpressions].  

### Deaktivieren der eifrigen Auswertung  

Während Sie JavaScript-Ausdrücke in der Konsole eingeben, zeigt die **eifrige Auswertung** eine Vorschau des Rückgabewerts für diesen Ausdruck.  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **eifrige Auswertung** , um die Vorschau des Rückgabewerts zu deaktivieren.  

### Deaktivieren von AutoVervollständigen aus dem Protokoll  

Wenn Sie einen Ausdruck eingeben, zeigt das Popupfenster AutoVervollständigen für die Konsole Ausdrücke an, die Sie zuvor ausgeführt haben.  Diesen Ausdrücken wird das Zeichen vorangestellt `>` .  [Öffnen Sie die Konsoleneinstellungen](#open-console-settings) , und deaktivieren Sie das Kontrollkästchen **AutoVervollständigen aus Verlauf** , um die Anzeige von Ausdrücken aus Ihrem Protokoll zu beenden.  

> [!NOTE]
> In der folgenden Abbildung `document.querySelector('a')` `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   Das AutoVervollständigen-Popup zeigt Ausdrücke aus dem Protokoll an  
:::image-end:::  

### JavaScript-Kontext auswählen  

Standardmäßig ist die Dropdownliste **JavaScript-Kontext** auf **oben**gesetzt, was den [Browserkontext][MDNBrowsingContext] des Hauptdokuments darstellt.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-dom-level-top.msft.png":::
   Die **JavaScript-Kontext** Dropdownliste  
:::image-end:::  

Angenommen, Sie haben eine Anzeige auf Ihrer Seite eingebettet in eine `<iframe>` .  Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.  Wählen Sie zuerst den Browserkontext der Anzeige aus der Dropdownliste **JavaScript-Kontext** aus.  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Die Konsolen Leiste" lightbox="../media/console-dom-level-multiple.msft.png":::
   Auswählen eines anderen JavaScript-Kontexts  
:::image-end:::  

## Deaktivieren der Konsole  

Sie können eine der folgenden Workflows verwenden, um die Konsole zu löschen:  

*   Wählen Sie **Konsole löschen** ( ![ Konsole löschen ][ImageClearConsoleIcon] ).  
*   Klicken Sie mit der rechten Maustaste auf eine Nachricht, und wählen Sie **Konsole löschen**aus.  
*   Geben Sie `clear()` in die Konsole ein, und wählen Sie dann aus `Enter` .  
*   Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.  
*   Wählen Sie aus `Control` + `L` , während sich die Konsole im Fokus befindet.  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Anzeigen von protokollierten Nachrichten – Übersicht über die Konsole | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ausführen von JavaScript – Übersicht über die Konsole | Microsoft docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsole | Microsoft docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an | Microsoft docs"  
[DevToolsConsoleLog]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  

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
