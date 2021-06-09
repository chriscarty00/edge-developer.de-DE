---
description: Eine Anleitung zum Navigieren Microsoft Edge DevTools mithilfe von Hilfstechnologien wie Bildschirmleseprogrammen.
title: Navigieren Microsoft Edge DevTools mit Hilfstechnologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2cb57a8ea1ea34506b4698d80ae0981d8716f3d2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597097"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="navigate-microsoft-edge-devtools-with-assistive-technology"></a>Navigieren Microsoft Edge DevTools mit Hilfstechnologie  

Dieser Artikel hilft Benutzern, die sich in erster Linie auf Hilfstechnologien wie Bildschirmleseprogramme verlassen, [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain]zu verwenden.  DevTools ist eine Suite von Webentwicklertools, die in den Microsoft Edge Browser integriert sind.  

Informationen zu DevTools-Features im Zusammenhang mit der Verbesserung der Barrierefreiheit einer Webseite finden Sie unter [Barrierefreiheitstestfeatures in DevTools][DevtoolsAccessibilityReference] und [Übersicht über Barrierefreiheitstests mit DevTools.](accessibility-testing-in-devtools.md)

Die Barrierefreiheit von DevTools ist eine laufende Arbeit.  Einige Tools und Registerkarten funktionieren besser mit Hilfstechnologien als andere.  Dieser Leitfaden führt Sie durch die Tools und Registerkarten, die am besten zugänglich sind, und zeigt bestimmte Probleme auf, die auf dem Weg auftreten können.  

## <a name="overview"></a>Übersicht  

DevTools ist in eine Reihe von Tools unterteilt.  (Im **Befehlsmenü**werden Tools als _Panels_bezeichnet.)  Tools sind in einer [ARIA-Registerkartenliste][W3CWaiAriaTablist] auf der Hauptsymbolleiste und auf der Schubladensymbolleiste organisiert.

Es folgen Beispiele für Tools:

*   Mit dem **Elementtool** können Sie [DOM-Knoten anzeigen und ändern][DevtoolsDomIndexNavigateDomTreeKeyboard] oder [CSS][DevtoolsCssIndex].  
*   Mit dem **Konsolentool** können Sie JavaScript-Protokolle und Livebearbeitungsobjekte lesen.  Navigieren Sie zu ["Konsole verwenden",][DevtoolsConsoleIndex]um weitere Informationen zu erfahren.

In jedem Tool gibt es eine oder mehrere Registerkartengruppen.  Das **Elementtool** enthält beispielsweise eine Reihe von Registerkarten, einschließlich **Formatvorlagen,** **Ereignislistener**und **Barrierefreiheit.**

## <a name="keyboard-shortcuts"></a>Tastenkombinationen  

[DevTools-Referenz zu Tastenkombinationen][DevtoolsShortcuts] ist ein hilfreiches Blatt mit Tricks.  Achten Sie darauf, ein Lesezeichen zu setzen, und verweisen Sie darauf, während Sie die verschiedenen Tools erkunden.

## <a name="open-devtools"></a>Öffnen von DevTools  

Navigieren Sie zunächst zu [Öffnen Microsoft Edge DevTools][DevtoolsOpen].  Es gibt eine Reihe von Möglichkeiten zum Öffnen von DevTools, entweder über Tastenkombinationen oder Menüelemente.  

## <a name="navigate-between-tools"></a>Navigieren zwischen Tools

### <a name="navigate-by-keyboard"></a>Navigieren nach Tastatur  

*   Wenn DevTools geöffnet ist, wählen Sie `Control` + `]` \(Windows, Linux\) oder `Command` + `]` \(macOS\) aus, um den Fokus auf das nächste Tool auf der Hauptsymbolleiste zu verschieben.
*   Wählen Sie `Control` + `[` \(Windows, Linux\) oder `Command` + `[` \(macOS\) aus, um den Fokus auf das vorherige Tool auf der Hauptsymbolleiste zu verschieben.
*   Wählen Sie `Tab` oder `Shift` + `Tab` wiederholt aus, bis der Fokus auf die Registerkarten der Hauptsymbolleiste oder Schubladensymbolleiste verschoben wird, und verwenden Sie dann die Pfeiltasten, um zwischen den Tools zu navigieren.

**Bekannte Probleme**  

*   Einige Tools, z. B. die **Konsolen-** und **Leistungstools,** können den Fokus in den Inhaltsbereich des Tools verschieben, sobald das Tool ausgewählt ist.  Dies kann die Navigation mithilfe von Pfeiltasten erschweren.  
*   Der Name des ausgewählten Tools wird angekündigt, jedoch erst nach ankündigung des fokussierten Inhalts im Tool.  Diese Abfolge von Ankündigungen kann es leicht machen, den Namen des Tools zu übersehen.

### <a name="navigate-by-command-menu"></a>Navigieren nach Befehlsmenü  

Um ein bestimmtes Tool auszuwählen, verwenden Sie das [Befehlsmenü.][DevtoolsCommandMenuIndex]  Im Befehlsmenü wird ein Tool als _Panel_bezeichnet.

1.  Wenn DevTools geöffnet ist, wählen Sie `Control` + `Shift` + `P` \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü**zu öffnen.  
    Das **Befehlsmenü** ist ein AutoVervollständigen-Kombinationsfeld für die Fuzzysuche.  
1.  Geben Sie den Namen eines Panels (Tools) ein, und navigieren Sie dann `Down Arrow` über die Tastatur zur richtigen Option.  
1.  Wählen Sie `Enter` aus, um einen Befehl auszuführen.  

So öffnen Sie das **Elementtool:**

1.  Öffnen Sie das **Befehlsmenü**.  
1.  Geben Sie `E` dann `L` .  Die Option **"Panel > Elemente anzeigen"** ist ausgewählt.  
1.  Wählen Sie `Enter` .  

Wenn Sie ein Tool auf diese Weise öffnen, wird der Fokus im Inhaltsbereich des Tools platziert.  Im Fall des **Elements-Tools** wird der Fokus in die **DOM-Struktur**verschoben.

## <a name="elements-tool"></a>Elementtool

### <a name="inspect-an-element-on-the-page"></a>Überprüfen eines Elements auf der Seite  

1.  Navigieren Sie mithilfe des Cursors in der Sprachausgabe zu dem element, das Sie überprüfen möchten.  
1.  Simulieren Sie einen Rechtsklick auf das Element, um das Kontextmenü zu öffnen.  
1.  Wählen Sie die Option **"Überprüfen"** aus.  This [opens the Elements tool and focuses the element in the DOM Tree][DevtoolsDomIndexViewDomNodes].  

Die **DOM-Struktur** ist als [ARIA-Struktur][W3CWaiAriaTree]angeordnet.  Navigieren Sie beispielsweise zu [Navigieren in der **DOM-Struktur** mit einer Tastatur][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Kopieren des Codes für ein Element in der DOM-Struktur  

1.  Zeigen Sie mit dem Fokus auf einen Knoten in der **DOM-Struktur**auf den Knoten, und öffnen Sie das Kontextmenü \(rechtsklick\).  
1.  Erweitern Sie die Option **"Kopieren".**  
1.  Choose **Copy outerHTML**.  

**Bekannte Probleme**  

*   **Beim Kopieren von outerHTML** wird häufig nicht der aktuelle Knoten, sondern stattdessen der übergeordnete Knoten ausgewählt.  Der Inhalt des Elements sollte sich jedoch weiterhin im kopierten outerHTML-Element befinden.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Ändern der Attribute eines Elements in der DOM-Struktur  

*   Wenn Sie den Fokus auf einem Knoten in der **DOM-Struktur**haben, wählen Sie diese `Enter` aus, um sie bearbeitbar zu machen.  
*   Wählen Sie `Tab` diese Option aus, um zwischen Attributwerten zu wechseln.  Wenn Sie "Leerzeichen" hören, befinden Sie sich innerhalb einer leeren Texteingabe und können einen neuen Attributwert eingeben.  
*   Wählen Sie `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um die Änderung zu akzeptieren und den gesamten Inhalt des Elements zu hören.  

**Bekannte Probleme**  

*   Wenn Sie die Texteingabe eingeben, erhalten Sie kein Feedback.  Wenn Sie einen Tippfehler ausführen und die Pfeiltasten verwenden, um Ihre Eingabe zu untersuchen, erhalten Sie auch kein Feedback.  Die einfachste Möglichkeit, Ihre Arbeit zu überprüfen, besteht darin, die Änderung zu akzeptieren und dann zu überwachen, bis das gesamte Element angekündigt wird.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Bearbeiten des HTML-Codes eines Elements in der DOM-Struktur  

*   Wenn Sie den Fokus auf einem Knoten in der **DOM-Struktur**haben, wählen Sie diese `Enter` aus, um sie bearbeitbar zu machen.  
*   Wählen Sie `Tab` diese Option aus, um zwischen Attributwerten zu wechseln.  Wenn Sie beispielsweise den Namen des Elements hören, `h2` befinden Sie sich innerhalb einer Texteingabe und können den Typ des Elements ändern.  
*   Wählen Sie `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um die Änderung zu akzeptieren.  

Wenn Sie z. B. `h3` `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) eingeben und auswählen, ändern sich die Start- und Endtags des `h3` Elements.  

## <a name="tabs-in-the-elements-tool"></a>Registerkarten im Elementtool

Das **** Elementtool enthält zusätzliche Registerkarten zum Überprüfen von Elementen wie dem CSS, das auf ein Element angewendet wurde, oder der relevanten Stelle in der Barrierefreiheitsstruktur.  

*   Wenn Sie den Fokus auf einem Knoten in der **DOM-Struktur**haben, wählen `Tab` Sie aus, bis Sie hören, dass die Registerkarte **"Formatvorlagen"** ausgewählt ist.  
*   Verwenden Sie `Right Arrow` die, um andere verfügbare Registerkarten zu erkunden.

Die **DOM-Struktur** wandelt Elemente mit `href` Attributen in fokussierbare Links um, sodass Sie möglicherweise mehrmals auswählen `Tab` müssen, um den **Bereich "Formatvorlagen"** zu erreichen.  

**Bekannte Probleme**  

Auf die **REGISTERKARTEn DOM-Haltepunkte** und **Eigenschaften** kann nicht über die Tastatur zugegriffen werden.  

### <a name="styles-pane"></a>Formatvorlagenbereich  

Suchen Sie im Bereich **"Formatvorlagen"** nach Steuerelementen zum Filtern von Formatvorlagen, zum Umschalten von Elementzuständen \(z. B. [:active][MDNActive] und [:focus][MDNFocus]\), zum Umschalten von Klassen und zum Hinzufügen neuer Klassen.  Es gibt auch ein leistungsstarkes Tool zur Stilüberprüfung, um Formatvorlagen zu untersuchen und zu ändern, die derzeit auf das Element angewendet werden, das in der **DOM-Struktur**im Fokus steht.  

Das wichtigste Konzept für den Bereich **Formatvorlagen** besteht darin, dass nur Formatvorlagen für den aktuell ausgewählten Knoten in der **DOM-Struktur**angezeigt werden.  Angenommen, Sie sind fertig mit der Überprüfung der Formatvorlagen eines `<header>` Knotens, und nun möchten Sie sich die Formatvorlagen für einen `<footer>` Knoten ansehen.  Dazu müssen Sie zuerst den `<footer>` Knoten in der **DOM-Struktur**auswählen.  Möglicherweise ist es schneller, den [Inspect-Workflow](#inspect-an-element-on-the-page) zu verwenden, um einen Knoten zu überprüfen, der sich in der allgemeinen Nähe des `footer` Knotens \(z. B. ein Link in der Fußzeile\) befindet, der die **DOM-Struktur**konzentriert, und dann mit der Tastatur zu dem genauen Knoten navigieren, an dem Sie interessiert sind.  

#### <a name="navigate-the-styles-pane"></a>Navigieren im Bereich "Formatvorlagen"  

Da alle Formatvorlagentools auf eine oder andere Weise wieder mit dem Bereich **Formatvorlagen** verbunden sind, ist es sinnvoll, zunächst ein Experte für dieses Tool zu werden.  

*   Wenn Sie den Fokus auf den Bereich **"Formatvorlagen"** legen, wählen Sie aus, `Tab` um den Fokus nach innen zu verschieben und den Inhalt zu erkunden.  
*   Wählen Sie `Tab` aus, bis die erste Formatvorlage aktiv wird.  Wenn Sie eine Sprachausgabe verwenden, wird diese erste Formatvorlage als `element.style {}` angekündigt.  
*   Wählen Sie `Down Arrow` diese Option aus, um in der Liste der Formatvorlagen in der Reihenfolge der Spezifität zu navigieren.  Eine Sprachausgabe gibt jede Formatvorlage an, beginnend mit dem Namen der CSS-Datei, der Zeilennummer, auf der die Formatvorlage angezeigt wird, und dem Namen der Formatvorlage.  Beispiel: `main.css:233 .card__img {}`.  
*   Wählen Sie diese Option `Enter` aus, um eine Formatvorlage ausführlicher zu prüfen.  Der Fokus beginnt auf einer bearbeitbaren Version des Formatvorlagennamens.  
*   Wählen Sie `Tab` aus, um zwischen bearbeitbaren Versionen jeder CSS-Eigenschaft und den entsprechenden Werten zu wechseln.  Am Ende jedes Formatvorlagenblocks befindet sich ein leeres bearbeitbares Textfeld, mit dem Sie zusätzliche CSS-Eigenschaften hinzufügen können.  
*   Sie können weiterhin `Tab` auswählen, um durch die Liste der Formatvorlagen zu navigieren, oder `Escape` den Modus verlassen und mithilfe von Pfeiltasten wieder navigieren.  

Navigieren Sie für weitere Verknüpfungen zu [Formatvorlagenbereich-Tastaturreferenz][DevtoolsShortcutsStylesPaneKeyboard].  

**Bekannte Probleme**  

*   Wenn Sie **** das bearbeitbare Textfeld Filter verwenden, können Sie nicht mehr in der Liste der Formatvorlagen navigieren.  

#### <a name="toggle-element-state"></a>Umschalten des Elementstatus  

So schalten Sie den Status eines Elements um, z. B. `:active` `:focus` oder:  

1.  Navigieren Sie zum Bereich **"Formatvorlagen",** und wählen Sie `Tab` aus, bis die Schaltfläche **"Elementstatus umschalten"** den Fokus hat.  
1.  Wählen Sie `Enter` diese Option aus, um die Auflistung der Elementzustände zu erweitern.  Die Elementzustände werden als Gruppe von Kontrollkästchen angezeigt.  
1.  Select `Tab` until the first state, , has `:active` focus.  
1.  Wählen Sie `Space` diese Option aus, um sie zu aktivieren.  Wenn das aktuell ausgewählte Element in der DOM-Struktur eine `:active` Formatvorlage aufweist, wird es jetzt angewendet.  
1.  Halten Sie `Tab` sich, um alle verfügbaren Zustände zu erkunden.  

#### <a name="add-an-existing-class"></a>Hinzufügen einer vorhandenen Klasse  

Neben der Schaltfläche **"Elementstatus umschalten"** befindet sich die Schaltfläche **"Elementklassen".**  Um den Fokus darauf zu verschieben, wählen Sie ihn `Tab` aus, und wählen Sie dann `Enter` aus.  Der Fokus wird in ein Bearbeitungstextfeld mit der Bezeichnung **"Neue Klasse hinzufügen"** verschoben.  

Die Schaltfläche **"Elementklassen"** wird in erster Linie zum Hinzufügen vorhandener Klassen zu einem Element verwendet.  Wenn Ihr Stylesheet beispielsweise eine Hilfsklasse mit dem Namen `.clearfix` enthielt, können Sie `.` innerhalb des Textfelds zum Bearbeiten eine Vorschlagsliste von Klassen anzeigen und den `Down Arrow` Vorschlag `.clearfix` suchen.  Oder geben Sie den Klassennamen selbst ein, und wählen Sie `Enter` ihn aus.  

#### <a name="add-a-new-style-rule"></a>Hinzufügen einer neuen Formatvorlagenregel  

Neben der Schaltfläche **"Elementklassen"** befindet sich die Schaltfläche **"Neue Formatvorlagenregel".**  Um den Fokus darauf zu verschieben, wählen Sie ihn `Tab` aus, und wählen Sie dann `Enter` aus.  Der Fokus wird in ein bearbeitbares Textfeld innerhalb des Formatvorlageninspektors verschoben.  Der anfängliche Textinhalt des Felds ist der Tagname des Elements, das in der **DOM-Struktur**ausgewählt ist.  
Sie können einen beliebigen Klassennamen in dieses Feld eingeben und dann `Tab` css-Eigenschaften zuweisen.  

### <a name="computed-tab"></a>Berechnete Registerkarte  

Wenn Sie den Fokus auf der Registerkarte **"Berechnet"** haben, wählen Sie die Option `Tab` aus, um den Fokus nach innen zu verschieben und den Inhalt zu erkunden.  Auf der Registerkarte **"Berechnet"** gibt es Steuerelemente zum Untersuchen, welche CSS-Eigenschaften tatsächlich in der Reihenfolge der Spezifität auf ein Element angewendet werden.  

<!--todo: add Computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Erkunden aller berechneten Formatvorlagen  

Wählen Sie diese Option `Tab` aus, bis Sie die Sammlung berechneter Formatvorlagen erreichen.  Diese werden als [ARIA-Struktur][W3CWaiAriaTree]dargestellt.  Beim Erweitern eines Listenfelds wird angezeigt, welche CSS-Selektoren die berechnete Formatvorlage anwenden.  Diese Selektoren sind nach Spezifität organisiert.  Eine Sprachausgabe gibt den berechneten Wert an, mit dem die CSS-Auswahl derzeit übereinstimmt, den Dateinamen des Stylesheets, das den Selektor enthält, und die Zeilennummer für den Selektor.  

**Bekannte Probleme**  

*   Wenn Sie das Textfeld ** Filter ** verwenden, können Sie keine Formatvorlagen mehr überprüfen.  

### <a name="event-listeners-tab"></a>Registerkarte "Ereignislistener"  

Um die Ereignislistener zu überprüfen, die auf ein Element angewendet werden, wählen Sie **das** Elementtool aus, und wählen Sie dann die Registerkarte **Ereignislistener** aus (gruppiert mit der Registerkarte **"Formatvorlagen").**

#### <a name="explore-event-listeners"></a>Erkunden von Ereignislistenern  

Ereignislistener werden als [ARIA-Struktur][W3CWaiAriaTree]dargestellt.  Sie können die Pfeiltasten verwenden, um sie zu navigieren.  Eine Sprachausgabe gibt den Namen des DOM-Objekts an, an das der Ereignislistener angefügt ist, sowie den Dateinamen, an dem der Ereignislistener definiert ist, und die Zeilennummer.  

### <a name="accessibility-tab"></a>Registerkarte "Barrierefreiheit"

Wählen Sie die `Tab` Taste aus, um **** sich auf der Registerkarte **"Barrierefreiheit"** im Elementtool zu bewegen.

Die Registerkarte **"Barrierefreiheit"** befindet sich in der Nähe der Registerkarte **"Formatvorlagen".** Auf der Registerkarte "Barrierefreiheit" gibt es Steuerelemente zum Untersuchen der Barrierefreiheitsstruktur, der auf ein Element angewendeten ARIA-Attribute und der berechneten Barrierefreiheitseigenschaften.  Navigieren Sie für weitere Informationen auf [der Registerkarte "Barrierefreiheit" zu "Barrierefreiheit testen".][DevtoolsAccessibilityTab]

#### <a name="accessibility-tree"></a>Barrierefreiheitsstruktur  

Die **Barrierefreiheitsstruktur** wird als [ARIA-Struktur][W3CWaiAriaTree] dargestellt, wobei jede einem `treeitem` Element im DOM entspricht.  Die Struktur gibt die berechnete Rolle für den ausgewählten Knoten an.  Generische Elemente wie `div` und werden in der Struktur als `span` "GenericContainer" angekündigt.  Verwenden Sie die Pfeiltasten, um die Struktur zu durchlaufen und Beziehungen zwischen übergeordneten und untergeordneten Elementen zu untersuchen.  

**Bekannte Probleme**  

*   Der Typ der [ARIA-Struktur,][W3CWaiAriaTree] die von der Registerkarte **"Barrierefreiheit"** verwendet wird, wird in Microsoft Edge für macOS-Bildschirmleseprogramme wie VoiceOver möglicherweise nicht ordnungsgemäß verfügbar gemacht.  Abonnieren Sie [Chromium Problem #868480,][ChromiumIssues868480] um über den Fortschritt dieses Problems informiert zu werden.  
*   Jeder Abschnitt mit **ARIA-Attributen** und **berechneten Eigenschaften** ist als [ARIA-Struktur][W3CWaiAriaTree]gekennzeichnet, verfügt jedoch derzeit nicht über die Fokusverwaltung und ist nicht tastaturoperierbar.  

## <a name="lighthouse-tool"></a>Tool "Springen"

**Der Auslauf** führt eine Reihe von Tests für eine Website aus, um allgemeine Probleme im Zusammenhang mit Leistung, Barrierefreiheit, SEO und einer Reihe anderer Kategorien zu überprüfen.  

### <a name="configure-and-generate-a-report"></a>Konfigurieren und Generieren eines Berichts

1.  Beim ersten Öffnen des **Tools Werkzeuge ** in DevTools wird der Fokus auf die Schaltfläche Bericht generieren gesetzt. ****  Standardmäßig ist das Formular so konfiguriert, dass berichte für jede Kategorie mithilfe der mobilen Emulation auf einer simulierten 3G Verbindung ausgeführt werden.  
1.  Um die Berichtseinstellungen zu ändern, verwenden Sie diese, um den Fokus auf die Einstellungen für `Shift` + `Tab` **Denkzustand**zu setzen, oder navigieren Sie zurück im Modus "Durchsuchen".  
1.  Wenn Sie bereit sind, den Bericht auszuführen, navigieren Sie zurück zur Schaltfläche Bericht **generieren,** und wählen Sie `Enter` .  
1.  Der Fokus wird in ein modales Fenster mit einer Schaltfläche **"Abbrechen"** verschoben, mit der Sie die Überwachung beenden können.  Möglicherweise hören Sie eine Reihe von Ohrhörern, während die Überwachung ausgeführt wird und die Seite mehrmals aktualisiert.  

**Bekannte Probleme**  

*   Die verschiedenen Abschnitte des Konfigurationsformulars sind derzeit nicht mit einem `fieldset` Element gekennzeichnet.  Möglicherweise ist es einfacher, im Suchmodus zu navigieren, um herauszufinden, welche Steuerelemente den einzelnen Abschnitten zugeordnet sind.  
*   Es gibt keine Ankündigung für Ohrhörer oder Liveregionen, wenn die Überwachung abgeschlossen ist.  In der Regel dauert die Überwachung ca. 30 Sekunden, danach sollten Sie zu den Ergebnissen navigieren können.  Die Verwendung des Suchmodus ist möglicherweise die einfachste Möglichkeit, um die Ergebnisse zu erzielen.  

### <a name="navigate-the-lighthouse-report"></a>Navigieren im Bericht "Vererzung"  

Der Bericht über die Prüfung ist in Abschnitte unterteilt, die den einzelnen Überwachungskategorien entsprechen.  Der Bericht wird mit einer Liste der Bewertungen für jede Kategorie geöffnet.  Diese Bewertungen sind auch Links, die Sie verwenden können, um zu den relevanten Abschnitten zu springen.  Innerhalb jedes Abschnitts befinden sich erweiterbare `details` Elemente, die Informationen zu erfolgreichen oder fehlgeschlagenen Prüfungen enthalten.  Standardmäßig werden nur fehlerhafte Überwachungen angezeigt.  Jeder Abschnitt endet mit einem endgültigen `details` Element, das alle übergebenen Überwachungen enthält.  

Wenn Sie eine neue Überwachung ausführen möchten, beenden Sie `Shift` + `Tab` den Bericht, und wählen Sie die Schaltfläche **"Bericht generieren"** aus.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsAccessibilityReference]: reference.md "Features für Barrierefreiheitstests in DevTools | Microsoft-Dokumente"  
[DevtoolsAccessibilityTab]: accessibility-tab.md "Testen der Barrierefreiheit mithilfe der Registerkarte &quot;Barrierefreiheit&quot; | Microsoft-Dokumente"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft-Dokumente"  
[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte Mit Anzeigen und Ändern von CSS-| Microsoft-Dokumente"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes "DOM-Knoten anzeigen – Erste Schritte mit dem Anzeigen und Ändern des DOM-| Microsoft Docs"  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get started with viewing and changing the DOM | Microsoft Docs"  
[DevtoolsOpen]: .. /open/index.md "Open Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcuts]: .. /shortcuts/index.md "Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts "Styles panel keyboard shortcuts - Microsoft Edge DevTools keyboard shortcuts | Microsoft Docs"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problem 868480 – Verfügbarmachen von ARIA-Strukturen als Tabellen in der Mac-Barrierefreiheit"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Neues Problem – MicrosoftDocs/edge-developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ":active | Mdn"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ":focus | Mdn"  

[MonorailChromiumIssues]: https://crbug.com "Probleme – Chromium – Monochrom"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (role) – BARRIEREFREIE RICH INTERNET-Anwendungen (INTRANET-ARIA) 1.1 | W3c"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "tree (role) – BARRIEREFREIE RICH INTERNET-Anwendungen (SILVERLIGHT-ARIA) 1.1 | W3c"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) und wurde von [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[RobDodson]: https://developers.google.com/web/resources/contributors#rob-dodson  
