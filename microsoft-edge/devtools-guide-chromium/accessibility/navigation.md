---
title: Navigieren in Microsoft Edge devtools mit Hilfstechnologien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567045"
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



Dieser Leitfaden soll Benutzern helfen, die in erster Linie auf Hilfstechnologien wie Bildschirmsprachausgaben zugreifen und Microsoft Edge devtools verwenden.  Microsoft Edge devtools ist eine Suite von Webentwickler Tools, die in den Microsoft Edge-Browser integriert sind.  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

Die Barrierefreiheit von devtools ist eine Work-in-Progress-Funktion.  Einige Panels und Registerkarten funktionieren mit Hilfstechnologien besser als andere.  Dieser Leitfaden führt Sie durch die Panels, die am häufigsten zugänglich sind, und hebt spezifische Probleme hervor, auf die Sie auf dem Weg stoßen können.  

## Übersicht   

Bevor Sie beginnen, hilft es, ein geistiges Modell für die Strukturierung der devtools-Benutzeroberfläche zu haben.  DevTools ist in eine Reihe von Tafeln unterteilt, die in [einer `tablist` Arie ][W3CWaiAriaTablist]organisiert sind.  

Beispiel:  

*   Im Panel **Elemente** können Sie DOM-Knoten oder [CSS] [DevtoolsCssIndex] anzeigen und ändern.  
*   Mit [**Console** Panel] [DevtoolsConsoleIndex] können Sie JavaScript-Protokolle und Live-Bearbeitungs Objekte lesen.  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

Im Inhaltsbereich jedes Bereichs gibt es eine Reihe unterschiedlicher Tools, die häufig als Tabstopps oder Bereiche in der Dokumentation bezeichnet werden.  
Beispielsweise enthält das Panel **Elemente** weitere Registerkarten, um Ereignislistener, die Barrierefreiheits Struktur und vieles mehr zu überprüfen.  Die Unterscheidung zwischen Registerkarten und Fensterbereichen ist etwas willkürlich.  Der einzige Grund, warum Sie möglicherweise einen oder den anderen Ausdruck sehen, besteht darin, die Konsistenz mit der restlichen offiziellen devtools-Dokumentation beizubehalten.  

## Tastenkombinationen   

Die [devtools-Tastenkombinationen] [DevtoolsShortcuts] ist ein hilfreiches Cheatsheet.  Achten Sie darauf, die Textmarke zu markieren, und beziehen Sie sich darauf, während Sie die verschiedenen Panels erkunden.  

## Öffnen von devtools   

Lesen Sie zunächst [Open Microsoft Edge devtools] [DevtoolsOpen].  Es gibt eine Reihe von Möglichkeiten, devtools zu öffnen, entweder über Tastenkombinationen oder Menüelemente.  

## Navigieren zwischen Bereichen   

### Navigieren mithilfe der Tastatur   

*   Drücken Sie bei geöffnetem devtools `Control` + `]` \ (Windows \) oder `Command` + `]` \ (macOS \), um den Fokus auf das nächste Fenster zu legen.  
*   Drücken Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \), um den Fokus auf das vorherige Panel zu legen.  
*   Es ist auch möglich, den `Shift` + `Tab` Fokus in die [Aria `tablist` ][W3CWaiAriaTablist] eines Panels zu verschieben und die Pfeiltasten zum Ändern von Panels zu verwenden, obwohl es möglicherweise schneller ist, die zuvor erwähnten Tastenkombinationen zu verwenden.  

#### Bekannte Probleme   

*   Einige Panels, wie die **Konsolen** -und **Leistungs** Bereiche, können den Fokus in den Inhaltsbereich verschieben, sobald Sie aktiviert sind.  Dadurch kann die Navigation mit Pfeiltasten schwierig werden.  
*   Der Name des ausgewählten Panels wird angekündigt, aber erst, nachdem er den fokussierten Inhalt im Panel gelesen hat.  Dies kann sehr einfach zu versäumen.  

### Navigieren nach Befehlsmenü   

Wenn Sie ein bestimmtes Panel fokussieren möchten, verwenden Sie das [**Befehlsmenü**] [DevtoolsCommandMenuIndex]:  

1.  Drücken Sie bei geöffnetem devtools `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    Das **Befehl-Menü** ist ein Fuzzy-Such-AutoVervollständigen-Kombinationsfeld.  
1.  Geben Sie den Namen des Panels ein, das Sie öffnen möchten, und navigieren Sie dann mithilfe der `Down Arrow` auf der Tastatur zur richtigen Option.  
1.  Drücken Sie `Enter` , um einen Befehl auszuführen.  

So öffnen Sie beispielsweise das Panel **Elemente** :  

1.  Öffnen des **Befehlsmenüs**  
1.  Geben Sie `E` dann ein `L` .  Die Option **Panel > Elemente anzeigen** ist aktiviert.  
1.  Drücken Sie `Enter` , um den Befehl auszuführen, der das Fenster öffnet.  

Wenn Sie ein Panel auf diese Weise öffnen, wird der Fokus auf den Inhalt des Panels umgeleitet.  Im Fall des **Elements** -Panels wird der Fokus in die **DOM-Struktur**verschoben.  

## Element Panel   

### Überprüfen eines Elements auf der Seite   

1.  Navigieren Sie mit dem Cursor in der Sprachausgabe zu dem Element, das Sie überprüfen möchten.  
1.  Simulieren Sie mit der rechten Maustaste auf das Element, um das Kontextmenü zu öffnen.  
1.  Wählen Sie die Option über **prüfen** aus.  Dadurch wird das Panel **Elemente** geöffnet, und das Element wird in der **DOM-Struktur**fokussiert.  

<!--todo:  add dom nodes (elements pane) section when available  -->  

Die **DOM-Struktur** wird als [Aria `tree` ][W3CWaiAriaTree]angelegt.  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### Kopieren des Codes für ein Element in der DOM-Struktur   

1.  Wenn der Fokus auf einem Knoten in der **DOM-Struktur**liegt, öffnen Sie das Kontextmenü mit der rechten Maustaste.  
1.  Erweitern Sie die Option **Kopieren** .  
1.  Wählen Sie **outerHTML kopieren**aus.  

#### Bekannte Probleme   

*   Beim **Kopieren von outerHTML** wird häufig nicht der aktuelle Knoten, sondern stattdessen der übergeordnete Knoten ausgewählt.  Der Inhalt des Elements sollte sich jedoch weiterhin im kopierten outerHTML befinden.  

### Ändern der Attribute eines Elements in der DOM-Struktur   

*   Drücken Sie den Fokus auf einen Knoten in der **DOM-Struktur**, `Enter` um ihn bearbeitbar zu machen.  
*   Drücken Sie `Tab` , um zwischen den Attributwerten zu wechseln.  Wenn Sie "Leerzeichen" hören, befinden Sie sich innerhalb einer leeren Texteingabe und können einen neuen Attributwert eingeben.  
*   Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderung zu übernehmen und den gesamten Inhalt des Elements zu hören.  

#### Bekannte Probleme   

*   Wenn Sie in die Texteingabe eintippen, erhalten Sie keine Rückmeldungen.  Wenn Sie einen Tippfehler machen und die Pfeiltasten verwenden, um Ihre Eingaben zu erforschen, erhalten Sie auch kein Feedback.  Die einfachste Möglichkeit, ihre Arbeit zu überprüfen, besteht darin, die Änderung zu übernehmen und dann zu hören, dass das gesamte Element angekündigt wird.  

### Bearbeiten des HTML-Code eines Elements in der DOM-Struktur   

*   Drücken Sie den Fokus auf einen Knoten in der **DOM-Struktur**, `Enter` um ihn bearbeitbar zu machen.  
*   Drücken Sie `Tab` , um zwischen den Attributwerten zu wechseln.  Wenn Sie den Namen des Elements hören, beispielsweise "H2", befinden Sie sich innerhalb einer Texteingabe und können den Typ des Elements ändern.  
*   Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderung zu übernehmen.  

Wenn Sie beispielsweise `h3` `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \) eingeben und drücken, werden die Start-und Endtags des Elements in geändert `h3` .  

## Registerkarten des Elements-Panels   

Der Bereich "Elemente" enthält zusätzliche Registerkarten zum Überprüfen von **Elementen** wie dem auf ein Element angewendeten CSS oder der entsprechenden Stelle in der Barrierefreiheits Struktur.  

*   Wenn Sie den Fokus auf einen Knoten in der **DOM-Struktur**legen, drücken `Tab` Sie, bis Sie hören, dass der Bereich **Formatvorlagen** ausgewählt ist.  
*   Verwenden Sie die `Right Arrow` , um andere verfügbare Registerkarten zu erkunden.  

Die **DOM-Struktur** wandelt Elemente mit `href` Attributen in fokussierbare Links um, sodass Sie möglicherweise mehrmals drücken müssen, `Tab` um den Bereich " **Formatvorlagen** " zu erreichen.  

### Bekannte Probleme   

Auf die Registerkarten " **DOM-Haltepunkte** " und " **Eigenschaften** " kann nicht zugegriffen werden.  

### Bereich ' Formatvorlagen '   

Suchen Sie im Bereich **Formatvorlagen** nach Steuerelementen zum Filtern von Formatvorlagen, Umschalten von Element Zuständen \ (wie [`:active`][MDNActive] und [`:focus`][MDNFocus] \), Umschalten von Klassen und Hinzufügen neuer Klassen.  Darüber hinaus gibt es ein leistungsfähiges Tool zum Überprüfen von Stilen zum untersuchen und Ändern von Formatvorlagen, die derzeit auf das Element angewendet werden, das sich in der **DOM-Struktur**befindet.  

Das grundlegende Konzept für den Bereich " **Formatvorlagen** " ist, dass nur die Formatvorlagen für den aktuell ausgewählten Knoten in der **DOM-Struktur**angezeigt werden.  Nehmen wir beispielsweise an, dass Sie die Formatvorlagen eines `<header>` Knotens überprüft haben und nun die Formatvorlagen für einen Knoten sehen möchten `<footer>` .  Dazu müssen Sie zuerst den `<footer>` Knoten in der **DOM-Struktur**auswählen.  Möglicherweise finden Sie es schneller, wenn Sie den Workflow über [prüfen](#inspect-an-element-on-the-page) verwenden, um einen Knoten zu inspizieren, der sich in der allgemeinen Nähe des `footer` Knotens befindet \ (beispielsweise ein Link in der Fußzeile \), der die **DOM-Struktur**fokussiert, und dann mit der Tastatur zu dem exakten Knoten navigieren, an dem Sie interessiert sind.  

#### Navigieren im Bereich "Formatvorlagen"   

Da alle Formatvorlagen Tools auf die eine oder andere Weise wieder mit dem Bereich " **Formatvorlagen** " verbunden sind, ist es sinnvoll, dieses Tool zuerst zu beherrschen.  

*   Drücken Sie den Fokus im Bereich " **Formatvorlagen** ", `Tab` um den Fokus zu verschieben und den Inhalt zu untersuchen.  
*   Drücken Sie `Tab` , bis die erste Formatvorlage aktiviert ist.  Wenn Sie eine Sprachausgabe verwenden, wird diese erste Formatvorlage als "Element. Style {} " angekündigt.  
*   Drücken Sie `Down Arrow` , um in der Liste der Formatvorlagen in der Reihenfolge der Spezifität zu navigieren.  Eine Sprachausgabe kündigt jede Formatvorlage an, beginnend mit dem Namen der CSS-Datei, der Liniennummer, auf der die Formatvorlage angezeigt wird, und dem Namen der Formatvorlage.  Beispiel: "Main. CSS: 233. card__img {} "  
*   Drücken Sie `Enter` , um eine Formatvorlage detaillierter zu überprüfen.  Der Fokus beginnt mit einer bearbeitbaren Version des Formatvorlagen namens.  
*   Drücken Sie `Tab` , um zwischen bearbeitbaren Versionen jeder CSS-Eigenschaft und den entsprechenden Werten zu wechseln.  Am Ende jedes Formatvorlagen Blocks befindet sich ein leeres bearbeitbares Textfeld, das Sie zum Hinzufügen weiterer CSS-Eigenschaften verwenden können.  
*   Sie können weiterhin drücken, `Tab` um die Liste der Formatvorlagen zu durchlaufen, oder drücken Sie, `Escape` um diesen Modus zu verlassen, und kehren Sie zur Navigation durch die Pfeiltasten zurück.  

Achten Sie darauf, dass Sie über die [Formatvorlagenbereich-Tastatur Referenz] [DevtoolsShortcutsStylesPaneKeyboard] Weitere Tastenkombinationen lesen.  

##### Bekannte Probleme   

*   Wenn Sie das Feld bearbeitbares Textfeld **Filtern** verwenden, können Sie nicht mehr in der Liste der Formatvorlagen navigieren.  

#### Elementzustand umschalten   

Zum Umschalten des Zustands eines Elements, beispielsweise `:active` oder `:focus` :  

1.  Navigieren Sie zum Bereich **Formatvorlagen** , und drücken Sie, `Tab` bis die Schaltfläche **Element Zustand umschalten** den Fokus hat.  
1.  Drücken Sie `Enter` , um die Sammlung von Element Zuständen zu erweitern.  Die Elementzustände werden als Gruppe von Kontrollkästchen angezeigt.  
1.  Drücken Sie, `Tab` bis der erste Zustand, den `:active` Fokus hat.  
1.  Drücken Sie `Space` , um Sie zu aktivieren.  Wenn das aktuell ausgewählte Element in der DOM-Struktur eine `:active` Formatvorlage aufweist, wird es nun angewendet.  
1.  Drücken `Tab` Sie weiter, um alle verfügbaren Status zu durchsuchen.  

#### Hinzufügen einer vorhandenen Klasse   

Neben der Schaltfläche " **Elementzustand umschalten** " befindet sich die Schaltfläche " **Elementklassen** ".  Verschieben Sie den Fokus darauf, indem Sie `Tab` dann drücken `Enter` .  Der Fokus wird in ein Textfeld "Bearbeiten" mit der Bezeichnung " **neue Klasse hinzufügen**" verschoben.  

Die Schaltfläche **Elementklassen** wird in erster Linie zum Hinzufügen vorhandener Klassen zu einem Element verwendet.  Wenn Ihr Stylesheet beispielsweise eine Hilfsklasse mit dem Namen enthalten hat, `.clearfix` können Sie `.` in das Feld "Textfeld bearbeiten" drücken, um eine Vorschlagsliste mit Kursen anzuzeigen, und verwenden Sie die `Down Arrow` , um den Vorschlag zu finden `.clearfix` .  Oder geben Sie den Kursnamen selbst ein, und drücken Sie `Enter` ihn, um ihn anzuwenden.  

#### Hinzufügen einer neuen Stilregel   

Neben der Schaltfläche **Element Klassen** befindet sich die Schaltfläche **neue Stilregel** .  Verschieben Sie den Fokus, indem Sie die Taste drücken `Tab` und drücken `Enter` .  Der Fokus wird in ein bearbeitbares Textfeld innerhalb des Formatvorlagen Inspektors verschoben.  Der anfängliche Textinhalt des Felds ist der Tagnamen des Elements, das in der **DOM-Struktur**ausgewählt ist.  
Sie können einen beliebigen Kursnamen in dieses Feld eingeben und dann `Tab` zum Zuweisen von CSS-Eigenschaften drücken.  

### Registerkarte "berechnet"   

Drücken Sie auf der Registerkarte **berechnet** den Fokus, `Tab` um den Fokus zu verschieben und den Inhalt zu durchsuchen.  Auf der Registerkarte " **berechnet** " gibt es Steuerelemente, mit denen Sie untersuchen können, welche CSS-Eigenschaften tatsächlich auf ein Element in der Reihenfolge der Spezifität angewendet werden.  

<!--todo: add computed tab section when available  -->  

#### Erkunden aller berechneten Formatvorlagen   

Drücken `Tab` Sie, bis Sie die Sammlung berechneter Formatvorlagen erreichen.  Diese werden als [Aria `tree` ][W3CWaiAriaTree]dargestellt.  Durch das Erweitern einer ListBox wird aufgezeigt, welche CSS-Auswahlen die berechnete Formatvorlage anwenden.  Diese Auswahlen sind nach Spezifität geordnet.  Eine Sprachausgabe gibt den berechneten Wert bekannt, den die CSS-Auswahl aktuell abgleichen soll, den Dateinamen des Stylesheets, das die Auswahl enthält, und die Nummer der Zeile für die Auswahl.  

#### Bekannte Probleme   

*   Wenn Sie das Textfeld " **Filter** " verwenden, können Sie keine Formatvorlagen mehr überprüfen.  

### Registerkarte "Ereignis-Listener"   

Über die Registerkarte **Ereignislistener** können Sie innerhalb des **Elements** Panels die Ereignis-Listener überprüfen, die auf ein Element angewendet wurden.  Drücken Sie im Bereich **Formatvorlagen** den Fokus, `Right Arrow` um zur Registerkarte **Ereignis Listener** zu navigieren.  

#### Untersuchen von Ereignis Listenern   

Ereignis-Listener werden als [Aria `tree` ][W3CWaiAriaTree]dargestellt.  Sie können die Pfeiltasten verwenden, um zu navigieren.  Eine Sprachausgabe gibt den Namen des DOM-Objekts bekannt, an das der Ereignis-Listener angefügt ist, sowie den Dateinamen, in dem der Ereignislistener definiert ist, und die Nummer der Zeile.  

### Bereich "Barrierefreiheit"   

Wenn Sie den Fokus auf den Bereich **Barrierefreiheit** setzen, drücken Sie, `Tab` um den Fokus in den Inhalt zu verschieben.  Im Bereich " **Barrierefreiheit** " gibt es Steuerelemente zum Durchsuchen der Barrierefreiheits Struktur, die Aria-Attribute, die auf ein Element angewendet werden, und die berechneten Barrierefreiheitseigenschaften.  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### Barrierefreiheits Struktur   

Die **Barrierefreiheits Struktur** wird als [Aria `tree` ][W3CWaiAriaTree] dargestellt, wobei jede `treeitem` einem Element im DOM entspricht.  In der Struktur wird die berechnete Rolle für den ausgewählten Knoten angekündigt.  Generische Elemente wie `div` und `span` werden in der Struktur als "GenericContainer" angekündigt.  Verwenden Sie die Pfeiltasten, um die Struktur zu durchlaufen und die Beziehungen zwischen übergeordneten und untergeordneten Elemente zu erkunden.  

#### Bekannte Probleme   

*   Der vom **Barrierefreiheits** Bereich verwendete [Aria `tree` ][W3CWaiAriaTree] -Typ wird in Microsoft Edge für macOS-Sprachausgaben wie VoiceOver möglicherweise nicht ordnungsgemäß verfügbar gemacht.  Abonnieren Sie [Chromium Issue #868480][ChromiumIssues868480] , um über den Fortschritt in diesem Problem informiert zu werden.  
*   Alle Abschnitte **Aria-Attribute** und **berechnete Eigenschaften** werden als [Aria `tree` ][W3CWaiAriaTree]-Objekte gekennzeichnet, aber derzeit ist keine Fokusverwaltung vorhanden, und die Tastatur ist nicht funktionsfähig.  

## Überwachungs Panel   

Im Bereich " **Audits** " sollten Sie eine Reihe von Tests für eine Website ausführen, um nach häufigen Problemen im Zusammenhang mit Leistung, Barrierefreiheit, SEO und einer Reihe anderer Kategorien zu suchen.  

### Konfigurieren und Ausführen einer Überwachung   

1.  Beim ersten Öffnen des **Überwachungs** Panels wird der Fokus auf die Schaltfläche " **Überwachung ausführen** " am Ende des Formulars eingestellt.  Standardmäßig ist das Formular so konfiguriert, dass Audits für jede Kategorie mithilfe der mobilen Emulation auf einer simulierten 3G-Verbindung ausgeführt werden.  
1.  Verwenden `Shift` + `Tab` oder zurück navigieren im Durchsuchen-Modus, um die Überwachungseinstellungen zu ändern.  
1.  Wenn Sie zum Ausführen der Überwachung bereit sind, navigieren Sie zurück zur Schaltfläche **Überwachung ausführen** , und drücken Sie `Enter` .  
1.  Der Fokus wird in ein modales Fenster mit einer Schaltfläche " **Abbrechen** " verschoben, mit der Sie die Überwachung beenden können.  Sie können eine Reihe von earcons hören, während die Überwachung ausgeführt wird, und die Seite mehrmals aktualisieren.  

#### Bekannte Probleme   

*   Die verschiedenen Abschnitte des Konfigurations Formulars sind derzeit nicht mit einem `fieldset` Element gekennzeichnet.  Es ist möglicherweise einfacher, im Durchsuchen-Modus zu navigieren, um herauszufinden, welche Steuerelemente jedem Abschnitt zugeordnet sind.  
*   Wenn die Überwachung nicht mehr ausgeführt wird, gibt es keine earcon-oder Live Region-Ankündigung.  In der Regel dauert es ungefähr 30 Sekunden, nach denen Sie in der Lage sein sollten, zu den Ergebnissen zu navigieren.  Die Verwendung des Durchsuchen-Modus ist möglicherweise die einfachste Methode, um die Ergebnisse zu erreichen.  

### Navigieren im Überwachungsbericht   

Der Überwachungsbericht ist in Abschnitte gegliedert, die den einzelnen Überwachungskategorien entsprechen.  Der Bericht wird mit einer Liste der Bewertungen für jede Kategorie geöffnet.  Diese Punkte sind auch Links, die verwendet werden können, um die entsprechenden Abschnitte zu überspringen.  In jedem Abschnitt handelt es sich `details` um erweiterbare Elemente, die Informationen zu übergebenen oder fehlgeschlagenen Audits enthalten.  Standardmäßig werden nur fehlerhafte Überwachungen angezeigt.  Jeder Abschnitt endet mit einem Final `details` -Element, das alle übergebenen Audits enthält.  

Verwenden Sie zum Ausführen einer neuen Überwachung `Shift` + `Tab` den Bericht, und suchen Sie nach der Schaltfläche **Audit durchführen** .  

## Feedback senden   

*   Senden Sie devtools-Fehlerberichte oder Funktionsanforderungen an den [Chromium Issue Tracker][MonorailChromiumIssues].  
*   Senden Sie Feedback zu diesem Dokument an [GitHub][GithubEdgeDeveloperNewIssue].  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-Menu/Index.MD "Ausführen von Befehlen mit dem Befehlsmenü" Microsoft Edge devtools "  
[DevtoolsConsoleIndex]: .. /Console/Index.MD "Console Overview"  
[DevtoolsCssIndex]: .. /CSS/Index.MD "erste Schritte mit dem anzeigen und Ändern von CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /Open.MD "Microsoft Edge devtools" öffnen  
[DevtoolsShortcuts]: .. /Shortcuts.MD "Microsoft Edge devtools"-Tastenkombinationen  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # Formatvorlagen-Bereich-Tastenkombinationen "Formatvorlagenbereich-Tastenkombinationen – Microsoft Edge devtools-Tastenkombinationen"  

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
