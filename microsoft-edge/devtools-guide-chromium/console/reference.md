---
description: Eine umfassende Referenz zu allen Features und Verhaltensweisen im Zusammenhang mit der Konsolenbenutzeroberfläche in Microsoft Edge DevTools.
title: Konsolenreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d6fed1681e64f8f57c2e577017d623039a7b4152
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439367"
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

Diese Seite ist ein Verweis auf Features im Zusammenhang mit der Microsoft Edge DevTools-Konsole.  Es wird davon ausgegangen, dass Sie bereits mit der Verwendung der Konsole vertraut sind, um protokollierte Nachrichten anzeigen und JavaScript ausführen zu können.  Wenn nicht, navigieren Sie zu [Erste Schritte mit der Ausführung von JavaScript in][DevToolsConsoleJavascript] der Konsole, und beginnen Sie mit der Protokollierung von Nachrichten in der [Konsole.][DevToolsConsoleLog]  

Wenn Sie nach der API-Referenz für Funktionen wie `console.log()` suchen, navigieren Sie zu [Konsolen-API-Referenz][DevToolsConsoleApi].  Für den Verweis auf Funktionen wie `monitorEvents()` navigieren Sie zu Console [Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Öffnen der Konsole  

Sie können die **Konsole** als Tool [im](#open-the-console-tool) oberen Bereich oder als Tool [in der Schublade öffnen.](#open-the-console-tool-in-the-drawer)  

### <a name="open-the-console-tool"></a>Öffnen des Konsolentools  

Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Das Konsolentool" lightbox="../media/console-hello-console.msft.png":::
   Das **Konsolentool**  
:::image-end:::  

Wenn Sie das **Konsolentool** über [das][DevToolsCommandMenu]Befehlsmenü öffnen möchten, beginnen Sie mit der Eingabe, und führen Sie dann den Befehl Konsole anzeigen aus, der das `Console` **Panel-Badge** daneben hat. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Der Befehl zum Anzeigen des Konsolenbereichs" lightbox="../media/console-command-menu-show-console.msft.png":::
   Der Befehl zum Anzeigen des **Konsolentools**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Öffnen Des Konsolentools in der Schublade  

Wählen `Escape` Oder wählen Sie Anpassen und Steuern **DevTools** \( `...` \) und wählen Sie dann **Konsolenschubschubre anzeigen aus.**  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Show console drawer" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Show console drawer**  
:::image-end:::  

Die Schublade wird unten im DevTools-Fenster angezeigt, und das **Konsolentool** wird geöffnet.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Das **Konsolentool** in **der Schublade**  
:::image-end:::  

Wenn Sie das **Konsolentool** über [das][DevToolsCommandMenu]Befehlsmenü öffnen möchten, beginnen Sie mit der Eingabe, und führen Sie dann den Befehl Konsole anzeigen aus, neben dem das `Console` **Drawer-Signal** steht. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Der Befehl zum Anzeigen des **Console**-Tools in der Schublade" lightbox="../media/console-command-menu-show-console.msft.png":::
   Der Befehl zum Anzeigen des **Konsolentools** in der **Schublade**  
:::image-end:::  

### <a name="open-console-settings"></a>Öffnen von Konsoleneinstellungen  

Wählen **Sie Konsoleneinstellungen** \( ![ Symbol für Konsoleneinstellungen ](../media/settings-button-icon.msft.png) \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Konsoleneinstellungen" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Konsoleneinstellungen**  
:::image-end:::  

In den folgenden Links werden die einzelnen Einstellungen erläutert:  

*   [**Netzwerk ausblenden**](#hide-network-messages)  
*   [**Protokoll beibehalten**](#persist-messages-across-page-loads)  
*   [**Nur ausgewählter Kontext**](#filter-out-messages-from-different-contexts)  
*   [**Gruppe ähnlich**](#disable-message-grouping)  
*   [**Log XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Begierde Auswertung**](#disable-eager-evaluation)  
*   [**Autocomplete From History**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a>Öffnen der Konsolenseite  

Wählen **Sie Konsolenseite anzeigen** \( Konsolenseite anzeigen \) aus, um die Seitenleiste zu ![ ](../media/show-console-sidebar-icon.msft.png) zeigen, die für die Filterung hilfreich ist.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Konsolen-Sidebar" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Konsole** Sidebar  
:::image-end:::  

## <a name="view-messages"></a>Anzeigen von Nachrichten  

Dieser Abschnitt enthält Features, die die Art und Weise ändern, wie Nachrichten in der Konsole angezeigt werden.  Eine praktische exemplarische Vorgehensweise finden Sie unter Anzeigen [von Nachrichten.][DevToolsConsoleViewMessages]  

### <a name="disable-message-grouping"></a>Deaktivieren der Nachrichtengruppe  

[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie **"Gruppe", um** das Standardmäßige Nachrichtengruppenverhalten der Konsole zu deaktivieren.  Navigieren Sie beispielsweise zu [Log XHR und Fetch requests](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Protokollierung von XHR- und Fetch-Anforderungen  

[Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie **Log XMLHttpRequests,** um alle und Anforderungen an die Konsole zu `XMLHttpRequest` `Fetch` protokollieren.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Protokollieren von XMLHttpRequest- und Fetch-Anforderungen" lightbox="../media/console-xhr-fetch.msft.png":::
   Protokoll `XMLHttpRequest` und `Fetch` Anforderungen  
:::image-end:::  
In der oberen Meldung in der vorherigen Abbildung wird das Standardgruppenverhalten der **Konsole angezeigt.**  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Beibehalten von Nachrichten über Seitenlasten hinweg  

Standardmäßig wird die Konsole beim Laden einer neuen Seite deaktiviert.  Um Nachrichten über Seitenlasten hinweg zu speichern, [öffnen Sie Konsoleneinstellungen,](#open-console-settings) und aktivieren Sie dann das **Kontrollkästchen Protokoll** beibehalten.  

### <a name="hide-network-messages"></a>Ausblenden von Netzwerknachrichten  

Standardmäßig protokolliert der Browser Netzwerknachrichten an die **Konsole**.  In der folgenden Abbildung stellt die ausgewählte Nachricht den HTTP-Statuscode von `429` dar.  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Eine 429-Nachricht in der Konsole" lightbox="../media/console-show-network.msft.png":::
   Eine `429` Nachricht in der **Konsole**  
:::image-end:::  
So blenden Sie Netzwerknachrichten aus:  

1.  [Öffnen Sie Konsoleneinstellungen](#open-console-settings).  
1.  Aktivieren Sie **das Kontrollkästchen Netzwerk** ausblenden.  
    
## <a name="filter-messages"></a>Filtern von Nachrichten  

Es gibt viele Möglichkeiten, Nachrichten in der Konsole herausfiltern.  

### <a name="filter-out-browser-messages"></a>Filtern von Browsernachrichten  

[Öffnen Sie die Konsolen-Seitenleiste,](#open-the-console-sidebar) und wählen Sie **Benutzernachrichten aus,** um nur Nachrichten aus dem JavaScript der Seite anzeigen zu können.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Anzeigen von Benutzernachrichten" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Anzeigen von Benutzernachrichten  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtern nach Protokollebene  

DevTools weist jeder `console.*` Methode einen Schweregrad zu.  Es gibt 4 Ebenen: `Verbose` `Info` , , und `Warning` `Error` .  Befindet sich `console.log()` z. B. in `Info` der Gruppe, während sie sich in der `console.error()` Gruppe `Error` befindet.  Die [Konsolen-API-Referenz][DevToolsConsoleApi] beschreibt den Schweregrad jeder anwendbaren Methode.  Jede Nachricht, die der Browser bei der Konsole anmeldet, hat auch einen Schweregrad.  Sie können eine beliebige Ebene von Nachrichten ausblenden, an der Sie nicht interessiert sind.  Wenn Sie beispielsweise nur an Nachrichten interessiert sind, können Sie die anderen `Error` 3 Gruppen ausblenden.  

Wählen Sie **das Dropdownmenü Protokollebenen** aus, um Nachrichten zu aktivieren `Verbose` oder zu `Info` `Warning` `Error` deaktivieren.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Dropdownliste Protokollebenen" lightbox="../media/console-log-level-default-levels.msft.png":::
   Dropdownliste **"Protokollebenen"**  
:::image-end:::  

Sie können auch nach Protokollebene filtern, indem Sie die [Konsolenseite öffnen](#open-the-console-sidebar) und dann **Fehler,** **Warnungen,** **Info**oder **Verbose öffnen.**  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Anzeigen von Warnungen mithilfe der Seitenleiste" lightbox="../media/console-sidebar-warnings.msft.png":::
   Anzeigen von Warnungen mithilfe der Seitenleiste  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtern von Nachrichten nach URL  

Geben Sie eine URL ein, um nur Nachrichten anzeigen zu `url:` können, die von dieser URL stammten.  Nachdem Sie `url:` DevTools eingeben, werden alle relevanten URLs gezeigt.  Domänen funktionieren auch.  Wenn beispielsweise Nachrichten protokollieren und diese protokollieren, können Sie sich auf die Nachrichten aus diesen `https://example.com/a.js` `https://example.com/b.js` `url:https://example.com` 2 Skripts konzentrieren.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Ein URL-Filter" lightbox="../media/console-filter-text.msft.png":::
   Ein URL-Filter  
:::image-end:::  

Geben `-url:` Sie ein, um Nachrichten aus dieser URL auszublenden.  Dies wird als negativer URL-Filter bezeichnet.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der https://b.wal.co URL übereinstimmen" lightbox="../media/console-negative-filter-text.msft.png":::
   Ein negativer URL-Filter, der alle Nachrichten ausblendet, die mit der `https://b.wal.co` URL übereinstimmen
:::image-end:::  

Sie können auch Nachrichten von einer einzelnen URL anzeigen, **** indem Sie die Konsolenseite [öffnen,](#open-the-console-sidebar)den Abschnitt Benutzernachrichten erweitern und dann die URL des Skripts mit den Nachrichten angeben, auf die Sie sich konzentrieren möchten.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Anzeigen der Nachrichten, die von der wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Anzeigen der Nachrichten, die von `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtern von Nachrichten aus unterschiedlichen Kontexten  

Angenommen, Sie haben eine Ankündigung \(ad\) auf Ihrer Seite.  Die Anzeige ist in eine eingebettet `<iframe>` und generiert viele Nachrichten in Ihrer Konsole.  Da die Anzeige in einem anderen [JavaScript-Kontext](#select-javascript-context)ausgeführt wird, besteht eine Möglichkeit **** zum Ausblenden der Nachrichten im Öffnen von Konsoleneinstellungen und Aktivieren des Kontrollkästchens Nur ausgewählter Kontext. [](#open-console-settings)  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a>Filtern von Nachrichten, die nicht mit einem Muster für reguläre Ausdrücke übereinstimmen  

Geben Sie einen regulären Ausdruck ein, z. B. in das Textfeld Filter, um alle Nachrichten herausfiltern, `/[gm][ta][mi]/` die nicht mit diesem Muster übereinstimmen. ****  DevTools überprüft, ob das Muster im Nachrichtentext oder im Skript gefunden wird, das dazu führte, dass die Nachricht protokolliert wurde.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtern von Nachrichten, die nicht mit dem regex-Ausdruck übereinstimmen" lightbox="../media/console-filter-regex.msft.png":::
   Filtern von Nachrichten, die nicht mit dem `/[gm][ta][mi]/` regex-Ausdruck übereinstimmen  
:::image-end:::  

## <a name="run-javascript"></a>Ausführen von JavaScript  

Dieser Abschnitt enthält Features im Zusammenhang mit der Ausführung von JavaScript in der Konsole.  Eine praktische exemplarische Vorgehensweise finden Sie unter [Ausführen von JavaScript][DevToolsConsoleOverviewJavascript].  

### <a name="re-run-expressions-from-history"></a>Erneutes Ausführen von Ausdrücken aus dem Verlauf  

Wählen Sie den Schlüssel aus, um den Verlauf von JavaScript-Ausdrücken zu durchschreiben, die Sie `Up Arrow` zuvor in der Konsole verwendet haben.  Wählen `Enter` Sie diese Option aus, um den Ausdruck erneut ausführen zu können.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Beobachten des Werts eines Ausdrucks in Echtzeit mit Liveausdrücken  

Wenn Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**  Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein undheften ihn dann an den oberen Rand der Konsole.  Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.  Navigieren Sie [zu JavaScript Expression Values in Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].  

### <a name="disable-eager-evaluation"></a>Deaktivieren der Begierdeauswertung  

Wenn Sie In-JavaScript-Ausdrücke in der Konsole eingeben, zeigt die Bewertung mit **Begierde** eine Vorschau des Rückgabewerts für diesen Ausdruck an.  [Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie das Kontrollkästchen Bewertungsgierig, um die Rückgabewertvorschauen zu deaktivieren. ****  

### <a name="disable-autocomplete-from-history"></a>Deaktivieren des automatischen Kompletierens aus dem Verlauf  

Beim Eingeben eines Ausdrucks zeigt das Popupfenster für die automatische Vervollständigung für die Konsole Ausdrücke an, die Sie zuvor durchgeführt haben.  Diese Ausdrücke werden mit dem Zeichen `>` vorkonfiguriert.  [Öffnen Sie Konsoleneinstellungen,](#open-console-settings) und deaktivieren Sie das Kontrollkästchen **AutoComplete From History,** um die Anzeige von Ausdrücken aus Ihrem Verlauf zu beenden.  

> [!NOTE]
> In der folgenden Abbildung `document.querySelector('a')` und `document.querySelector('img')` sind Ausdrücke, die zuvor ausgewertet wurden.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Im Popup für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt." lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   Im Popup für die automatische Vervollständigung werden Ausdrücke aus dem Verlauf angezeigt.  
:::image-end:::  

### <a name="select-javascript-context"></a>Auswählen des JavaScript-Kontexts  

Standardmäßig ist das **JavaScript-Kontextdropdown** auf **top**festgelegt, das den [Browserkontext][MDNBrowsingContext] des Hauptdokuments darstellt.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Das Dropdownmenü JavaScript-Kontext" lightbox="../media/console-dom-level-top.msft.png":::
   Das **Dropdownmenü "JavaScript-Kontext"**  
:::image-end:::  

Angenommen, Sie haben eine Anzeige auf Ihrer Seite eingebettet in `<iframe>` .  Sie möchten JavaScript ausführen, um das DOM der Anzeige zu optimieren.  Sie sollten zuerst den Browserkontext der Anzeige im **Dropdownmenü JavaScript-Kontext** auswählen.  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Auswählen eines anderen JavaScript-Kontexts" lightbox="../media/console-dom-level-multiple.msft.png":::
   Auswählen eines anderen JavaScript-Kontexts  
:::image-end:::  

## <a name="clear-the-console"></a>Löschen der Konsole  

Sie können einen der folgenden Workflows verwenden, um die Konsole zu löschen:  

*   Wählen **Sie Clear Console** \( Clear Console ![ ](../media/clear-console-button-icon.msft.png) \).  
*   Zeigen Sie auf eine Nachricht, öffnen Sie das Kontextmenü \(righ-click\), und wählen Sie **Konsole löschen aus.**  
*   Geben `clear()` Sie in die Konsole **ein,** und wählen Sie `Enter` aus.  
*   Führen `console.clear()` Sie das JavaScript für Ihre Webseite aus.  
*   Wählen `Control` + `L` Sie **aus, während sich die Konsole** im Fokus befindet.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Anzeigen protokollierter Nachrichten – Übersicht über | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Ausführen von JavaScript – Übersicht über | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Erste Schritte mit der Ausführung von JavaScript in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Verfolgen Sie JavaScript-Ausdruckswerte in Echtzeit mit Live Expressions | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Erste Schritte mit der Protokollierung von Nachrichten in der Konsolenkonsole | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Browserkontext | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
