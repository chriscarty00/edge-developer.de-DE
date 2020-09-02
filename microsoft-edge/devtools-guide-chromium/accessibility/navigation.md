---
title: Navigieren in Microsoft Edge devtools mit Hilfstechnologien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 544d6a6ecb8dabe262e7c28aa7fc072610604be0
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986059"
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

# Navigieren in Microsoft Edge devtools mit Hilfstechnologien  

Der folgende Artikel soll Benutzern helfen, die in erster Linie auf Hilfstechnologien wie Bildschirmsprachausgaben zugreifen und [Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain]verwenden.  [Microsoft Edge devtools][MicrosoftEdgeDevtoolsMain] ist eine Suite von Webentwickler Tools, die in den Microsoft Edge-Browser integriert sind.  Wenn Sie nach devtools-Features suchen, die sich auf die Verbesserung der Barrierefreiheit einer Webseite beziehen, finden Sie Informationen unter [Barrierefreiheits Referenz][DevtoolsAccessibilityReference].  

Die Barrierefreiheit von devtools ist eine Work-in-Progress-Funktion.  Einige Panels und Registerkarten funktionieren mit Hilfstechnologien besser als andere.  Dieser Leitfaden führt Sie durch die Panels, die am häufigsten zugänglich sind, und hebt spezifische Probleme hervor, auf die Sie auf dem Weg stoßen können.  

## Übersicht  

Bevor Sie beginnen, hilft es, ein geistiges Modell für die Strukturierung der devtools-Benutzeroberfläche zu haben.  DevTools ist in eine Reihe von Tafeln unterteilt, die in einem [Aria-TabList][W3CWaiAriaTablist]organisiert sind.  

Zum Beispiel:  

*   Im **Element** Fenster können Sie [DOM-Knoten] [DevtoolsDomIndexNavigateDomTreeKeyboard] oder [CSS][DevtoolsCssIndex][anzeigen und ändern.  
*   Im [Konsolenfeld][DevtoolsConsoleIndex] können Sie JavaScript-Protokolle und Live-Bearbeitungs Objekte lesen.  

Im Inhaltsbereich jedes Bereichs gibt es eine Reihe unterschiedlicher Tools, die häufig als Tabstopps oder Bereiche in der Dokumentation bezeichnet werden.  
Beispielsweise enthält das Panel **Elemente** weitere Registerkarten, um Ereignislistener, die Barrierefreiheits Struktur und vieles mehr zu überprüfen.  Die Unterscheidung zwischen Registerkarten und Fensterbereichen ist etwas willkürlich.  Der einzige Grund, warum Sie möglicherweise einen oder den anderen Ausdruck sehen, besteht darin, die Konsistenz mit der restlichen offiziellen devtools-Dokumentation beizubehalten.  

## Tastenkombinationen  

Die [devtools-Tastenkombinationen] [DevtoolsShortcuts] ist ein hilfreiches Cheatsheet.  Achten Sie darauf, die Textmarke zu markieren, und beziehen Sie sich darauf, während Sie die verschiedenen Panels erkunden.  

## Open DevTools  

Informationen zu den ersten Schritten finden Sie unter [Open Microsoft Edge devtools] [DevtoolsOpen].  Es gibt eine Reihe von Möglichkeiten, devtools zu öffnen, entweder über Tastenkombinationen oder Menüelemente.  

## Navigieren zwischen Bereichen  

### Navigieren mithilfe der Tastatur  

*   Wenn devtools geöffnet ist, wählen Sie `Control` + `]` \ (Windows \) oder `Command` + `]` \ (macOS \) aus, um den Fokus auf das nächste Fenster zu legen.  
*   Wählen Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \) aus, um den Fokus auf das vorherige Panel zu legen.  
*   Es ist auch möglich, den `Shift` + `Tab` Fokus in das Aria- [TabList][W3CWaiAriaTablist] eines Panels zu verschieben und die Pfeiltasten zum Ändern von Panels zu verwenden, obwohl es möglicherweise schneller ist, die zuvor erwähnten Tastenkombinationen zu verwenden.  

**Bekannte Probleme**  

*   Einige Panels, beispielsweise die **Konsolen** -und **Leistungs** Panels, können den Fokus in den Bereich des Bereichs Inhalts verschieben, sobald die einzelnen Panels aktiviert sind.  Dadurch kann die Navigation mit Pfeiltasten schwierig werden.  
*   Der Name des ausgewählten Panels wird angekündigt, aber erst, nachdem er den fokussierten Inhalt im Panel gelesen hat.  Dies kann sehr einfach zu versäumen.  

### Navigieren nach Befehlsmenü  

Wenn Sie ein bestimmtes Panel fokussieren möchten, verwenden Sie das [Befehlsmenü][DevtoolsCommandMenuIndex]:  

1.  Wenn devtools geöffnet ist, wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.  
    Das **Befehl-Menü** ist ein Fuzzy-Such-AutoVervollständigen-Kombinationsfeld.  
1.  Geben Sie den Namen des Panels ein, das Sie öffnen möchten, und navigieren Sie dann mithilfe der `Down Arrow` auf der Tastatur zur richtigen Option.  
1.  Wählen Sie aus `Enter` , um einen Befehl auszuführen.  

Führen Sie die folgenden Aktionen aus, um das Panel **Elemente** zu öffnen.  

1.  Öffnen des **Befehlsmenüs**  
1.  Geben Sie `E` dann ein `L` .  Die Option **Panel > Elemente anzeigen** ist aktiviert.  
1.  Wählen Sie aus `Enter` , um den Befehl zum Öffnen des Panels auszuführen.  

Öffnen Sie ein Panel auf diese Weise, um den Fokus auf den Inhalt des Panels zu lenken.  Im Fall des **Elements** -Panels wird der Fokus in die **DOM-Struktur**verschoben.  

## Element Panel  

### Überprüfen eines Elements auf der Seite  

1.  Navigieren Sie mit dem Cursor in der Sprachausgabe zu dem Element, das Sie überprüfen möchten.  
1.  Simulieren Sie mit der rechten Maustaste auf das Element, um das Kontextmenü zu öffnen.  
1.  Wählen Sie die Option über **prüfen** aus.  Dadurch [wird das Element Fenster geöffnet, und das Element wird in der DOM-Struktur fokussiert] [DevtoolsDomIndexViewDomNodes].  

Die **DOM-Struktur** wird als Aria- [Struktur][W3CWaiAriaTree]angelegt.  Ein Beispiel finden Sie unter [Navigieren in der **DOM-Struktur** mit einer Tastatur] [DevtoolsDomIndexNavigateDomTreeKeyboard].  

### Kopieren des Codes für ein Element in der DOM-Struktur  

1.  Wenn sich der Fokus auf einem Knoten in der **DOM-Struktur**befindet, zeigen Sie auf den Knoten, und öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \).  
1.  Erweitern Sie die Option **Kopieren** .  
1.  Wählen Sie **outerHTML kopieren**aus.  

**Bekannte Probleme**  

*   Beim **Kopieren von outerHTML** wird häufig nicht der aktuelle Knoten, sondern stattdessen der übergeordnete Knoten ausgewählt.  Der Inhalt des Elements sollte sich jedoch weiterhin im kopierten outerHTML befinden.  

### Ändern der Attribute eines Elements in der DOM-Struktur  

*   Wenn der Fokus auf einem Knoten in der **DOM-Struktur**liegt, wählen Sie ihn aus, `Enter` um ihn bearbeitbar zu machen.  
*   Wählen Sie diese Option aus `Tab` , um zwischen Attributwerten zu wechseln.  Wenn Sie "Leerzeichen" hören, befinden Sie sich innerhalb einer leeren Texteingabe und können einen neuen Attributwert eingeben.  
*   Wählen Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \) aus, um die Änderung zu übernehmen und den gesamten Inhalt des Elements zu hören.  

**Bekannte Probleme**  

*   Wenn Sie in die Texteingabe eintippen, erhalten Sie keine Rückmeldungen.  Wenn Sie einen Tippfehler machen und die Pfeiltasten verwenden, um Ihre Eingaben zu erforschen, erhalten Sie auch kein Feedback.  Die einfachste Möglichkeit, ihre Arbeit zu überprüfen, besteht darin, die Änderung zu übernehmen und dann zu hören, dass das gesamte Element angekündigt wird.  

### Bearbeiten des HTML-Code eines Elements in der DOM-Struktur  

*   Wenn der Fokus auf einem Knoten in der **DOM-Struktur**liegt, wählen Sie ihn aus, `Enter` um ihn bearbeitbar zu machen.  
*   Wählen Sie diese Option aus `Tab` , um zwischen Attributwerten zu wechseln.  Wenn Sie beispielsweise den Namen des Elements hören, `h2` befinden Sie sich innerhalb einer Texteingabe und können den Typ des Elements ändern.  
*   Wählen Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \) aus, um die Änderung zu übernehmen.  

Wenn Sie beispielsweise `h3` `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \) eingeben und auswählen, ändern sich die Start-und Endtags des `h3` Elements.  

## Registerkarten des Elements-Panels  

Der Bereich "Elemente" enthält zusätzliche Registerkarten zum Überprüfen von **Elementen** wie dem auf ein Element angewendeten CSS oder der entsprechenden Stelle in der Barrierefreiheits Struktur.  

*   Wenn der Fokus auf einem Knoten in der **DOM-Struktur**liegt, wählen Sie aus, `Tab` bis Sie hören, dass der Bereich **Formatvorlagen** ausgewählt ist.  
*   Verwenden Sie die `Right Arrow` , um andere verfügbare Registerkarten zu erkunden.  

Die **DOM-Struktur** wandelt Elemente mit `href` Attributen in fokussierbare Links um, daher müssen Sie möglicherweise mehrmals auswählen, `Tab` um den Bereich " **Formatvorlagen** " zu erreichen.  

**Bekannte Probleme**  

Auf die Registerkarten " **DOM-Haltepunkte** " und " **Eigenschaften** " kann nicht zugegriffen werden.  

### Bereich ' Formatvorlagen '  

Suchen Sie im Bereich **Formatvorlagen** nach Steuerelementen zum Filtern von Formatvorlagen, Umschalten von Element Zuständen \ (wie [: aktiv][MDNActive] und [: Fokus][MDNFocus]\), Umschalten von Klassen und Hinzufügen neuer Klassen.  Darüber hinaus gibt es ein leistungsfähiges Tool zum Überprüfen von Stilen zum untersuchen und Ändern von Formatvorlagen, die derzeit auf das Element angewendet werden, das sich in der **DOM-Struktur**befindet.  

Das grundlegende Konzept für den Bereich " **Formatvorlagen** " ist, dass nur die Formatvorlagen für den aktuell ausgewählten Knoten in der **DOM-Struktur**angezeigt werden.  Nehmen wir beispielsweise an, dass Sie die Formatvorlagen eines `<header>` Knotens überprüft haben und nun die Formatvorlagen für einen Knoten sehen möchten `<footer>` .  Dazu müssen Sie zuerst den `<footer>` Knoten in der **DOM-Struktur**auswählen.  Möglicherweise finden Sie es schneller, wenn Sie den Workflow über [prüfen](#inspect-an-element-on-the-page) verwenden, um einen Knoten zu inspizieren, der sich in der allgemeinen Nähe des `footer` Knotens befindet \ (beispielsweise ein Link in der Fußzeile \), der die **DOM-Struktur**fokussiert, und dann mit der Tastatur zu dem exakten Knoten navigieren, an dem Sie interessiert sind.  

#### Navigieren im Bereich "Formatvorlagen"  

Da alle Formatvorlagen Tools auf die eine oder andere Weise wieder mit dem Bereich " **Formatvorlagen** " verbunden sind, ist es sinnvoll, zunächst ein Experte in diesem Tool zu werden.  

*   Wählen Sie im Bereich " **Formatvorlagen** " den Fokus aus, `Tab` um den Fokus nach innen zu verschieben und den Inhalt zu untersuchen.  
*   Wählen Sie aus `Tab` , bis die erste Formatvorlage aktiviert ist.  Wenn Sie eine Sprachausgabe verwenden, wird diese erste Formatvorlage als angekündigt `element.style {}` .  
*   Wählen Sie diese Option aus `Down Arrow` , um in der Liste der Formatvorlagen in der Reihenfolge der Spezifität zu navigieren.  Eine Sprachausgabe kündigt jede Formatvorlage an, beginnend mit dem Namen der CSS-Datei, der Liniennummer, auf der die Formatvorlage angezeigt wird, und dem Namen der Formatvorlage.  Beispiel: `main.css:233 .card__img {}`.  
*   Wählen Sie diese Option `Enter` aus, um eine Formatvorlage detaillierter zu prüfen.  Der Fokus beginnt mit einer bearbeitbaren Version des Formatvorlagen namens.  
*   Wählen Sie diese Option aus `Tab` , um zwischen bearbeitbaren Versionen jeder CSS-Eigenschaft und den entsprechenden Werten zu wechseln.  Am Ende jedes Formatvorlagen Blocks befindet sich ein leeres bearbeitbares Textfeld, das Sie zum Hinzufügen weiterer CSS-Eigenschaften verwenden können.  
*   Sie können weiterhin auswählen, `Tab` um die Liste der Formatvorlagen zu durchlaufen, oder Sie können `Escape` den Modus beenden und zur Navigation durch die Pfeiltasten zurückkehren.  

Weitere Tastenkombinationen finden Sie unter [Tastatur Referenz für Formatvorlagenbereich] [DevtoolsShortcutsStylesPaneKeyboard].  

**Bekannte Probleme**  

*   Wenn Sie das Feld bearbeitbares Textfeld **Filtern** verwenden, können Sie nicht mehr in der Liste der Formatvorlagen navigieren.  

#### Elementzustand umschalten  

Zum Umschalten des Zustands eines Elements, beispielsweise `:active` oder `:focus` :  

1.  Navigieren Sie zum Bereich **Formatvorlagen** , und wählen Sie aus, `Tab` bis die Schaltfläche **Element Zustand umschalten** den Fokus besitzt.  
1.  Wählen Sie aus `Enter` , um die Sammlung von Element Zuständen zu erweitern.  Die Elementzustände werden als Gruppe von Kontrollkästchen angezeigt.  
1.  Wählen Sie, `Tab` bis der erste Zustand, den `:active` Fokus hat.  
1.  Wählen Sie diese Option aus `Space` , um Sie zu aktivieren.  Wenn das aktuell ausgewählte Element in der DOM-Struktur eine `:active` Formatvorlage aufweist, wird es nun angewendet.  
1.  Halten Sie die Maustaste gedrückt `Tab` , um alle verfügbaren Status zu erkunden.  

#### Hinzufügen einer vorhandenen Klasse  

Neben der Schaltfläche " **Elementzustand umschalten** " befindet sich die Schaltfläche " **Elementklassen** ".  Wenn Sie den Fokus darauf verschieben möchten, wählen Sie aus, `Tab` und wählen Sie aus `Enter` .  Der Fokus wird in ein Textfeld "Bearbeiten" mit der Bezeichnung " **neue Klasse hinzufügen**" verschoben.  

Die Schaltfläche **Elementklassen** wird in erster Linie zum Hinzufügen vorhandener Klassen zu einem Element verwendet.  Wenn Ihr Stylesheet beispielsweise eine Hilfsklasse mit dem Namen enthalten hat, `.clearfix` können Sie `.` innerhalb des Felds "Text bearbeiten" auswählen, um eine Vorschlagsliste mit Kursen anzuzeigen, und verwenden Sie die `Down Arrow` , um den Vorschlag zu finden `.clearfix` .  Oder geben Sie den Kursnamen selbst ein, und wählen Sie `Enter` ihn aus, um ihn anzuwenden.  

#### Hinzufügen einer neuen Stilregel  

Neben der Schaltfläche **Element Klassen** befindet sich die Schaltfläche **neue Stilregel** .  Wenn Sie den Fokus darauf verschieben möchten, wählen Sie aus, `Tab` und wählen Sie aus `Enter` .  Der Fokus wird in ein bearbeitbares Textfeld innerhalb des Formatvorlagen Inspektors verschoben.  Der anfängliche Textinhalt des Felds ist der Tagnamen des Elements, das in der **DOM-Struktur**ausgewählt ist.  
Sie können in dieses Feld einen beliebigen Kursnamen eingeben und dann `Tab` ihm CSS-Eigenschaften zuweisen.  

### Registerkarte "berechnet"  

Wählen Sie auf der Registerkarte **berechnet** den Fokus aus, `Tab` um den Fokus zu verschieben und den Inhalt zu untersuchen.  Auf der Registerkarte " **berechnet** " gibt es Steuerelemente, mit denen Sie untersuchen können, welche CSS-Eigenschaften tatsächlich auf ein Element in der Reihenfolge der Spezifität angewendet werden.  

<!--todo: add computed tab section when available  -->  

#### Erkunden aller berechneten Formatvorlagen  

Wählen Sie diese Option aus, `Tab` bis Sie die Sammlung von berechneten Formatvorlagen erreichen.  Diese werden als Aria- [Struktur][W3CWaiAriaTree]dargestellt.  Durch das Erweitern einer ListBox wird aufgezeigt, welche CSS-Auswahlen die berechnete Formatvorlage anwenden.  Diese Auswahlen sind nach Spezifität geordnet.  Eine Sprachausgabe gibt den berechneten Wert bekannt, den die CSS-Auswahl aktuell abgleichen soll, den Dateinamen des Stylesheets, das die Auswahl enthält, und die Nummer der Zeile für die Auswahl.  

**Bekannte Probleme**  

*   Wenn Sie das Textfeld " **Filter** " verwenden, können Sie keine Formatvorlagen mehr überprüfen.  

### Registerkarte "Ereignis-Listener"  

Über die Registerkarte **Ereignislistener** können Sie innerhalb des **Elements** Panels die Ereignis-Listener überprüfen, die auf ein Element angewendet wurden.  Wählen Sie im Bereich **Formatvorlagen** den Fokus aus, `Right Arrow` um zur Registerkarte **Ereignis Listener** zu navigieren.  

#### Untersuchen von Ereignis Listenern  

Ereignis-Listener werden als [Aria-Struktur][W3CWaiAriaTree]dargestellt.  Sie können die Pfeiltasten verwenden, um zu navigieren.  Eine Sprachausgabe gibt den Namen des DOM-Objekts bekannt, an das der Ereignis-Listener angefügt ist, sowie den Dateinamen, in dem der Ereignislistener definiert ist, und die Nummer der Zeile.  

### Bereich "Barrierefreiheit"  

Wählen Sie im Bereich **Barrierefreiheit** den Fokus aus, `Tab` um den Fokus nach innen zu verschieben und den Inhalt zu untersuchen.  Im [Bereich Barrierefreiheit][DevtoolsAccessibilityReference] gibt es Steuerelemente zum Durchsuchen der Barrierefreiheits Struktur, die Aria-Attribute, die auf ein Element angewendet werden, und die berechneten Barrierefreiheitseigenschaften.  

#### Barrierefreiheits Struktur  

Die **Barrierefreiheits Struktur** wird als Aria- [Struktur][W3CWaiAriaTree] dargestellt, wobei jede `treeitem` einem Element im DOM entspricht.  In der Struktur wird die berechnete Rolle für den ausgewählten Knoten angekündigt.  Generische Elemente wie `div` und `span` werden in der Struktur als "GenericContainer" angekündigt.  Verwenden Sie die Pfeiltasten, um die Struktur zu durchlaufen und die Beziehungen zwischen übergeordneten und untergeordneten Elemente zu erkunden.  

**Bekannte Probleme**  

*   Der Typ der [Aria-Struktur][W3CWaiAriaTree] , die vom **Barrierefreiheits** Bereich verwendet wird, wird möglicherweise in Microsoft Edge für macOS-Sprachausgaben wie VoiceOver nicht richtig verfügbar gemacht.  Abonnieren Sie [Chromium Issue #868480][ChromiumIssues868480] , um über den Fortschritt in diesem Problem informiert zu werden.  
*   Alle Abschnitte **Aria-Attribute** und **berechnete Eigenschaften** werden als [Aria-Struktur][W3CWaiAriaTree]gekennzeichnet, aber derzeit ist keine Fokusverwaltung vorhanden, und die Tastatur ist nicht funktionsfähig.  

## Überwachungs Panel  

Im Bereich " **Audits** " sollten Sie eine Reihe von Tests für eine Website ausführen, um nach häufigen Problemen im Zusammenhang mit Leistung, Barrierefreiheit, SEO und einer Reihe anderer Kategorien zu suchen.  

### Konfigurieren und Ausführen einer Überwachung  

1.  Beim ersten Öffnen des **Überwachungs** Panels wird der Fokus auf die Schaltfläche " **Überwachung ausführen** " am Ende des Formulars eingestellt.  Standardmäßig ist das Formular so konfiguriert, dass Audits für jede Kategorie mithilfe der mobilen Emulation auf einer simulierten 3G-Verbindung ausgeführt werden.  
1.  Verwenden `Shift` + `Tab` oder zurück navigieren im Durchsuchen-Modus, um die Überwachungseinstellungen zu ändern.  
1.  Wenn Sie zum Ausführen der Überwachung bereit sind, navigieren Sie zurück zur Schaltfläche **Überwachung ausführen** , und wählen Sie aus `Enter` .  
1.  Der Fokus wird in ein modales Fenster mit einer Schaltfläche " **Abbrechen** " verschoben, mit der Sie die Überwachung beenden können.  Sie können eine Reihe von earcons hören, während die Überwachung ausgeführt wird, und die Seite mehrmals aktualisieren.  

**Bekannte Probleme**  

*   Die verschiedenen Abschnitte des Konfigurations Formulars sind derzeit nicht mit einem `fieldset` Element gekennzeichnet.  Es ist möglicherweise einfacher, im Durchsuchen-Modus zu navigieren, um herauszufinden, welche Steuerelemente jedem Abschnitt zugeordnet sind.  
*   Wenn die Überwachung nicht mehr ausgeführt wird, gibt es keine earcon-oder Live Region-Ankündigung.  In der Regel dauert es ungefähr 30 Sekunden, nach denen Sie in der Lage sein sollten, zu den Ergebnissen zu navigieren.  Die Verwendung des Durchsuchen-Modus ist möglicherweise die einfachste Methode, um die Ergebnisse zu erreichen.  

### Navigieren im Überwachungsbericht  

Der Überwachungsbericht ist in Abschnitte gegliedert, die den einzelnen Überwachungskategorien entsprechen.  Der Bericht wird mit einer Liste der Bewertungen für jede Kategorie geöffnet.  Diese Punkte sind auch Links, die verwendet werden können, um die entsprechenden Abschnitte zu überspringen.  In jedem Abschnitt handelt es sich `details` um erweiterbare Elemente, die Informationen zu übergebenen oder fehlgeschlagenen Audits enthalten.  Standardmäßig werden nur fehlerhafte Überwachungen angezeigt.  Jeder Abschnitt endet mit einem Final `details` -Element, das alle übergebenen Audits enthält.  

Verwenden Sie zum Ausführen einer neuen Überwachung `Shift` + `Tab` den Bericht, und suchen Sie nach der Schaltfläche **Audit durchführen** .  

## Kontakt mit dem Microsoft Edge devtools-Team

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Barrierefreiheits Referenz | Microsoft docs"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Der Bereich Barrierefreiheit – Referenz zu Barrierefreiheit | Microsoft docs"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /DOM/Index.MD # View-Dom-Nodes "DOM-Knoten anzeigen – erste Schritte beim Anzeigen und Ändern des DOM | Microsoft docs "  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /DOM/Index.MD # Navigate-the-DOM-Tree-with-a-Keyboard "Navigieren in der DOM-Struktur mit einer Tastatur – erste Schritte beim Anzeigen und Ändern des DOM | Microsoft docs "  
[DevtoolsOpen]: .. /Open.MD "Microsoft Edge-devtools öffnen | Microsoft docs "  
[DevtoolsShortcuts]: .. /Shortcuts.MD "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs "  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # Formatvorlagen-Bereich-Tastenkombinationen "Formatvorlagenbereich – Tastenkombinationen für Microsoft Edge devtools-Tastenkombinationen | Microsoft docs "  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problem 868480 – verfügbar machen von Aria-Strukturen als Tabellen unter Mac-Barrierefreiheit"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Neues Problem-MicrosoftDocs/Edge-Developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": aktiv | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Fokus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Probleme – Chrom – Monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (Rolle)-barrierefreie Rich-Internet-Anwendungen (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Struktur (Rolle) – barrierefreie Rich-Internet-Anwendungen (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) gefunden und von [Rob Dodson][RobDodson] (Mitwirkender, Google webfundamentals \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
