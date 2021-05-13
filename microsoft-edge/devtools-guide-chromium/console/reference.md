---
description: Eine umfassende Referenz für jedes Feature und Verhalten der Konsolenbenutzeroberfläche in Microsoft Edge DevTools.
title: Konsolenreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: f14663ca1883c0a81184f9a4fa67ddcbd3f08a24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564525"
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
# <a name="console-reference"></a>Konsolenreferenz  

Dieser Artikel ist eine Referenz zu Features im Zusammenhang mit der Microsoft Edge DevTools Console.  Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um protokollierte Nachrichten anzeigen und JavaScript ausführen zu können.  Wenn nicht, navigieren Sie zu [Erste Schritte mit der Ausführung von JavaScript in][DevtoolsConsoleConsoleJavascript] der Konsole und Erste Schritte mit der [Protokollierung von Nachrichten in der Konsole][DevtoolsConsoleConsoleLog].  

Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` suchen, navigieren Sie zu [Konsolen-API-Referenz][DevToolsConsoleApi].  Für den Verweis auf Funktionen wie `monitorEvents()` navigieren Sie zu Console [Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Öffnen der Konsole  

Sie können die **Konsole** als Tool [im](#open-the-console-tool) oberen Bereich oder als Tool [in der Schublade öffnen.](#open-the-console-tool-in-the-drawer)  

### <a name="open-the-console-tool"></a>Öffnen des Konsolentools  

Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Das Konsolentool" lightbox="../media/console-hello-console.msft.png":::
   Das **Konsolentool**  
:::image-end:::  

Um das **Konsolentool** im [Befehlsmenü][DevtoolsCommandMenuIndex]zu öffnen, geben Sie den Befehl Konsole anzeigen ein, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Panel-Badge** daneben hat. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Ausführen des Befehls zum Anzeigen des Konsolentools" lightbox="../media/console-command-menu-show-console.msft.png":::
   Ausführen des Befehls zum Anzeigen des **Konsolentools**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Öffnen Des Konsolentools in der Schublade  

Wählen `Esc` Oder wählen Sie Anpassen und Steuern **DevTools** \( `...` \) und wählen Sie dann **Konsolenschubschubre anzeigen aus.**  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Show console drawer" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Show console drawer**  
:::image-end:::  

Die Schublade wird unten im DevTools-Fenster angezeigt, und das **Konsolentool** wird geöffnet.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Das **Konsolentool** in **der Schublade**  
:::image-end:::  

Um das **Konsolentool** im Befehlsmenü zu [öffnen,][DevtoolsCommandMenuIndex]geben Sie den Befehl Konsole anzeigen ein, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Drawer-Badge** daneben hat. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Führen Sie den Befehl aus, um das Tool **Console** in der Schublade anzeigen zu können." lightbox="../media/console-command-menu-show-console.msft.png":::
   Ausführen des Befehls zum Anzeigen des **Konsolentools** in der **Schublade**  
:::image-end:::  

### <a name="open-console-settings"></a>Öffnen sie konsolen Einstellungen  

Wählen Sie **die Schaltfläche Konsole Einstellungen** \( Konsole Einstellungen Symbol ![ ](../media/settings-button-icon.msft.png) \) aus.  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Konsolen Einstellungen" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Konsolen Einstellungen**  
:::image-end:::  

In den folgenden Links werden die einzelnen Einstellungen erläutert.  

*   [Netzwerk ausblenden](#hide-network-messages)  
*   [Protokoll beibehalten](#persist-messages-across-page-loads)  
*   [Nur ausgewählter Kontext](#filter-out-messages-from-different-contexts)  
*   [Gruppe ähnlich](#turn-off-message-grouping)  
*   [Protokoll-XMLHttpRequests](#log-xhr-and-fetch-requests)  
*   [Begierde Auswertung](#turn-off-eager-evaluation)  
*   [AutoComplete aus dem Verlauf](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a>Öffnen der Konsolenseite  

Zum Anzeigen der **Seitenleiste**wählen Sie **Konsolenseiteleiste anzeigen** \( ![ Konsolenseiteleiste ](../media/show-console-sidebar-icon.msft.png) anzeigen \).  Die **Sidebar** hilft Ihnen beim Filtern.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Konsolen-Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Konsolen-Sidebar**  
:::image-end:::  

## <a name="view-messages"></a>Anzeigen von Nachrichten  

Dieser Abschnitt enthält Features, die die Art und Weise ändern, wie Nachrichten in der Konsole angezeigt werden.  Eine praktische exemplarische Vorgehensweise finden Sie unter Anzeigen [von Nachrichten.][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]  

### <a name="turn-off-message-grouping"></a>Deaktivieren der Nachrichtengruppe  

Um das Standardmäßige Nachrichtengruppenverhalten der Konsole zu **deaktivieren,** öffnen Sie [Console Einstellungen,](#open-console-settings) und aktivieren Sie das Kontrollkästchen neben **Ähnlich gruppieren.**  Navigieren Sie beispielsweise zu [Log XHR und Fetch requests](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Protokollierung von XHR- und Fetch-Anforderungen  

Wenn Sie alle Und Anforderungen an die Konsole protokollieren möchten, öffnen Sie console Einstellungen, und aktivieren Sie das Kontrollkästchen neben `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. **** [](#open-console-settings)  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Protokollieren von XMLHttpRequest- und Fetch-Anforderungen" lightbox="../media/console-xhr-fetch.msft.png":::
   Protokoll `XMLHttpRequest` und `Fetch` Anforderungen  
:::image-end:::  

In der oberen Meldung in der vorherigen Abbildung wird das Standardgruppenverhalten der **Konsole angezeigt.**  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Beibehalten von Nachrichten über Seitenlasten hinweg  

Wenn Sie eine neue Webseite laden, wird die Konsole mit der Standardaktion **deaktiviert.**  Wenn Sie Nachrichten über Seitenlasten hinweg beibehalten möchten, öffnen Sie [console Einstellungen,](#open-console-settings) und aktivieren Sie das Kontrollkästchen neben **Protokoll beibehalten.**  

### <a name="hide-network-messages"></a>Ausblenden von Netzwerknachrichten  

Die Standardaktion für Microsoft Edge ist das Protokollieren von Netzwerknachrichten an die **Konsole**.  In der folgenden Abbildung stellt die ausgewählte Nachricht den HTTP-Statuscode von `429` dar.  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Eine 429-Nachricht in der Konsole" lightbox="../media/console-show-network.msft.png":::
   Eine `429` Nachricht in der **Konsole**  
:::image-end:::  

Führen Sie die folgenden Aktionen aus, um Netzwerknachrichten auszublenden.  

1.  [Öffnen Sie Console Einstellungen](#open-console-settings).  
1.  Aktivieren Sie das Kontrollkästchen neben **Netzwerk ausblenden**.  
    
## <a name="filter-messages"></a>Filtern von Nachrichten  

Es gibt viele Möglichkeiten zum Filtern von Nachrichten in der **Konsole.**  

### <a name="filter-out-browser-messages"></a>Filtern von Browsernachrichten  

[Öffnen Sie die Konsolenseite,](#open-the-console-sidebar) und wählen Sie **# Benutzernachrichten aus,** um nur Nachrichten anzuzeigen, die aus dem JavaScript der Webseite stammten.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Anzeigen von Benutzernachrichten" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Anzeigen von Benutzernachrichten  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtern nach Protokollebene  

DevTools weist jeder `console.*` Methode eine der vier Schweregrade zu.  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
Befindet sich `console.log()` z. B. in der `Info` Gruppe, befindet `console.error()` sich jedoch in der `Error` Gruppe.  Die [Konsolen-API-Referenz][DevToolsConsoleApi] beschreibt den Schweregrad jeder anwendbaren Methode.  Jede Nachricht, die der Browser bei der Konsole anmeldet, hat auch einen Schweregrad.  Sie können eine beliebige Ebene von Nachrichten ausblenden, an der Sie nicht interessiert sind.  Wenn Sie beispielsweise nur an Nachrichten interessiert sind, können Sie die anderen `Error` drei Gruppen ausblenden.  

Wählen Sie zum Filtern der Nachrichten das **Dropdownmenü Protokollebenen** aus, und wählen Sie `Verbose` , , oder `Info` `Warning` `Error` aus.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Dropdownliste "Protokollebenen"" lightbox="../media/console-log-level-default-levels.msft.png":::
   Dropdownliste **"Protokollebenen"**  
:::image-end:::  

Um die Protokollebene zum Filtern zu verwenden, öffnen Sie die [Konsolen-Seitenleiste,](#open-the-console-sidebar) und wählen Sie dann **Fehler,** **Warnungen,** **Info**oder **Verbose aus.**  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Anzeigen von Warnungen mithilfe der Seitenleiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   Anzeigen von Warnungen mithilfe der Seitenleiste  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtern von Nachrichten nach URL  

Geben Sie eine URL ein, um nur Nachrichten anzeigen zu `url:` können, die von dieser URL stammten.  Nach der Eingabe `url:` zeigt DevTools alle relevanten URLs an.  Domänen funktionieren auch.  Wenn beispielsweise Nachrichten protokollieren und diese protokollieren, können Sie sich auf die Nachrichten `https://example.com/a.js` `https://example.com/b.js` aus diesen beiden `url:https://example.com` Skripts konzentrieren.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Ein URL-Filter" lightbox="../media/console-filter-text.msft.png":::
   Ein URL-Filter  
:::image-end:::  

Geben Sie ein, um Nachrichten aus einer URL `-url:` auszublenden.  Es ist ein negativer URL-Filter.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der https://b.wal.co URL übereinstimmen" lightbox="../media/console-negative-filter-text.msft.png":::
   Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der `https://b.wal.co` URL übereinstimmen
:::image-end:::  

Führen Sie zum Anzeigen von Nachrichten von einer einzelnen URL die folgenden Aktionen aus.  

1.  [Öffnen Sie die Konsolenseitenleiste](#open-the-console-sidebar).  
1.  Erweitern Sie den **Abschnitt # Benutzernachrichten.**  
1.  Wählen Sie die URL des Skripts aus, das die Nachrichten enthält, auf die Sie sich konzentrieren möchten.  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Anzeigen der Nachrichten, die von der wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Anzeigen der Nachrichten, die von `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtern von Nachrichten aus unterschiedlichen Kontexten  

Angenommen, Sie haben eine Ankündigung \(ad\) auf Ihrer Webseite.  Die Anzeige ist in eine eingebettet `<iframe>` und generiert viele Nachrichten in Ihrer **Konsole.**  Da die Anzeige in einem anderen [JavaScript-Kontext](#choose-javascript-context)ausgeführt wird, besteht eine Möglichkeit zum Ausblenden der Nachrichten im Öffnen von [Console Einstellungen](#open-console-settings) und aktivieren Sie das Kontrollkästchen neben Nur ausgewählter **Kontext**.  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a>Filtern von Nachrichten, die keinem Muster für reguläre Ausdrücke entsprechen  

Geben Sie einen regulären Ausdruck wie z. B. in das Textfeld Filter ein, um alle Nachrichten herausfiltern, die nicht `/[gm][ta][mi]/` mit diesem Muster übereinstimmen. ****  DevTools überprüft, ob das Muster im Nachrichtentext oder im Skript gefunden wird, das dazu führte, dass die Nachricht protokolliert wurde.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtern von Nachrichten, die nicht mit dem regex-Ausdruck übereinstimmen" lightbox="../media/console-filter-regex.msft.png":::
   Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` regex-Ausdruck übereinstimmen  
:::image-end:::  

## <a name="run-javascript"></a>Ausführen von JavaScript  

Dieser Abschnitt enthält Features im Zusammenhang mit der Ausführung von JavaScript in der **Konsole.**  Eine praktische exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevtoolsConsoleConsoleJavascript].  

### <a name="rerun-expressions-from-history"></a>Erneutes Ausführen von Ausdrücken aus dem Verlauf  

Wählen `Up Arrow` Sie diese Option aus, um den Verlauf von JavaScript-Ausdrücken zu durchschreiben, die Sie zuvor in der Konsole verwendet **haben.**  Wählen `Enter` Sie diese Option aus, um den Ausdruck erneut ausführen zu können.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Beobachten des Werts eines Ausdrucks in Echtzeit mit Live-Ausdrücken  

Wenn Sie denselben JavaScript-Ausdruck wiederholt **** in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**  Mit **Live-Ausdrücken**geben Sie einen Ausdruck einmal ein und an den oberen Rand der **Konsole an.**  Der Wert des Ausdrucks wird in nahezu Echtzeit aktualisiert.  Navigieren Sie [zu JavaScript Expression Values in Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].  

### <a name="turn-off-eager-evaluation"></a>Deaktivieren der Bewertung von "Begierig"  

**Bei der** Begierdeauswertung wird eine Vorschau des Rückgabewerts angezeigt, während Sie In-JavaScript-Ausdrücke in der **Konsole eingeben.**  Führen Sie die folgenden Aktionen aus, um die Vorschau des Rückgabewerts zu deaktivieren.  

1.  [Öffnen Sie Console Einstellungen](#open-console-settings).  
1.  Entfernen Sie das Kontrollkästchen neben **Bewertung mit Begierde**.  
    
### <a name="turn-off-autocomplete-from-history"></a>Deaktivieren des automatischen Kompletierens aus dem Verlauf  

Beim Eingeben eines Ausdrucks zeigt das Popupfenster für die automatische Vervollständigung für die **Konsole** Ausdrücke an, die Sie zuvor durchgeführt haben.  Die Ausdrücke werden mit dem Zeichen `>` vorkonfiguriert.  Um die Anzeige von Ausdrücken aus Dem Verlauf zu beenden, öffnen Sie console [Einstellungen,](#open-console-settings) und entfernen Sie das Kontrollkästchen neben **autocomplete From History.**  

> [!NOTE]
> In der folgenden Abbildung `document.querySelector('a')` und `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Im Popupmenü für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt." lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   Im Popupmenü für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt.  
:::image-end:::  

### <a name="choose-javascript-context"></a>Auswählen des JavaScript-Kontexts  

Die Standardoption für das **JavaScript-Kontextdropdown** ist **top**, das den [Browserkontext der][MdnDocsGlossaryBrowsingContext] Hauptwebseite darstellt.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Das Dropdownmenü "JavaScript-Kontext"" lightbox="../media/console-dom-level-top.msft.png":::
   Das **Dropdownmenü "JavaScript-Kontext"**  
:::image-end:::  

Angenommen, Sie haben eine Anzeige auf Ihrer Webseite eingebettet in `<iframe>` .  Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.  Wählen Sie zunächst den Browserkontext der Anzeige im **Dropdownmenü JavaScript-Kontext** aus.  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Auswählen eines anderen JavaScript-Kontexts" lightbox="../media/console-dom-level-multiple.msft.png":::
   Auswählen eines anderen JavaScript-Kontexts  
:::image-end:::  

## <a name="clear-the-console"></a>Löschen der Konsole  

Führen Sie **einen**der folgenden Workflows aus, um die Konsole zu löschen.  

*   Wählen Sie **die Schaltfläche Konsole** löschen \( Konsole löschen ![ ](../media/clear-console-button-icon.msft.png) \) aus.  
*   Zeigen Sie auf eine Nachricht, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Konsole löschen aus.**  
*   Geben `clear()` Sie in die Konsole **ein,** und wählen Sie `Enter` aus.  
*   Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.  
*   Wählen `Control` + `L` Sie **aus, während sich die Konsole** im Fokus befindet.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokollieren von Nachrichten im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Verwenden der Konsolenanwendung | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Überprüfen und Filtern von Informationen auf der aktuellen Webseite | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Überwachen von Änderungen in JavaScript mithilfe von Live Expressions | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit Microsoft Edge DevTools Command | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browserkontext | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
