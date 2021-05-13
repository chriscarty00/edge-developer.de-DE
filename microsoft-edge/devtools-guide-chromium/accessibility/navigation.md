---
description: Eine Anleitung zum Navigieren Microsoft Edge DevTools mithilfe von Hilfstechnologien wie Bildschirmlesegeräten.
title: Navigieren Microsoft Edge DevTools mit Hilfstechnologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: cf2742dfb08ee482b26fe43417b7454e5b6ff809
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564581"
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

Der folgende Artikel soll Benutzern helfen, die sich hauptsächlich auf Hilfstechnologie wie Bildschirmlesegeräte verlassen, auf Microsoft Edge devTools zugreifen und [diese verwenden.][MicrosoftEdgeDevtoolsMain]  [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain] ist eine Suite von Webentwicklertools, die in den Microsoft Edge sind.  Wenn Sie nach DevTools-Features im Zusammenhang mit der Verbesserung der Barrierefreiheit einer Webseite suchen, navigieren Sie zu [Barrierefreiheitsreferenz][DevtoolsAccessibilityReference].  

Die Barrierefreiheit von DevTools ist in Bearbeitung.  Einige Panels und Registerkarten funktionieren mit Hilfstechnologie besser als andere.  Dieser Leitfaden führt Sie durch die Panels, die am zugänglichsten sind, und hebt spezifische Probleme hervor, die auf dem Weg auftreten können.  

## <a name="overview"></a>Übersicht  

Vor dem Start hilft es, ein mentales Modell der Struktur der DevTools-Benutzeroberfläche zu haben.  DevTools ist in eine Reihe von Panels unterteilt, die in eine [ARIA-Registerkartenliste unterteilt sind.][W3CWaiAriaTablist]  

Beispiel:  

*   Mit **dem Elementtool** können Sie [DOM-Knoten][DevtoolsDomIndexNavigateDomTreeKeyboard] oder CSS anzeigen und [ändern.][DevtoolsCssIndex]  
*   Im [Konsolenbereich][DevtoolsConsoleIndex] können Sie JavaScript-Protokolle und Livebearbeitungsobjekte lesen.  

Im Inhaltsbereich der einzelnen Bereiche finden Sie eine Reihe unterschiedlicher Tools, die in der Dokumentation häufig als Registerkarten oder Bereiche bezeichnet werden.  
Das **Elementtool** enthält beispielsweise zusätzliche Registerkarten zum Überprüfen von Ereignislistenern, der Barrierefreiheitsstruktur und vielem mehr.  Der Unterschied zwischen Registerkarten und Fensterausschnitten ist etwas willkürlich.  Der einzige Grund, warum Sie den einen oder anderen Ausdruck überprüfen können, besteht in der Beibehaltung der Konsistenz mit dem Rest der offiziellen DevTools-Dokumentation.  

## <a name="keyboard-shortcuts"></a>Tastenkombinationen  

[DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] ist ein hilfreiches Cheatsheet.  Achten Sie darauf, ein Lesezeichen zu setzen, und verweisen Sie beim Erkunden der verschiedenen Panels darauf.  

## <a name="open-devtools"></a>Öffnen von DevTools  

Navigieren Sie zu [Öffnen sie Microsoft Edge DevTools][DevtoolsOpen].  Es gibt eine Reihe von Möglichkeiten, DevTools zu öffnen, entweder über Tastenkombinationen oder Menüelemente.  

## <a name="navigate-between-panels"></a>Navigieren zwischen Panels  

### <a name="navigate-by-keyboard"></a>Navigieren über die Tastatur  

*   Wenn DevTools geöffnet ist, wählen `Control` + `]` Sie \(Windows, Linux\) oder `Command` + `]` \(macOS\) aus, um den fokus auf den nächsten Bereich zu legen.  
*   Wählen `Control` + `[` Sie \(Windows, Linux\) oder `Command` + `[` \(macOS\) aus, um den vorherigen Bereich zu fokussieren.  
*   Es ist auch möglich, den Fokus in die `Shift` + `Tab` [Registerkartenliste ARIA][W3CWaiAriaTablist] eines Panels zu verschieben und die Pfeiltasten zum Ändern von Panels zu verwenden, obwohl es möglicherweise schneller ist, die zuvor erwähnten Verknüpfungen zu verwenden.  

**Bekannte Probleme**  

*   Einige Panels, z. **** B. die **Konsolen-** und Leistungstools, können den Fokus in den Bereich "Panelinhalt" verschieben, sobald jedes Panel aktiviert ist.  Dies kann die Navigation durch Pfeiltasten erschweren.  
*   Der Name des ausgewählten Panels wird angekündigt, jedoch erst, nachdem er den fokussierten Inhalt im Bereich gelesen hat.  Dies kann es sehr einfach machen, sie zu verpassen.  

### <a name="navigate-by-command-menu"></a>Navigieren nach Befehlsmenü  

Verwenden Sie das Befehlsmenü, um einen bestimmten Bereich [zu fokussieren:][DevtoolsCommandMenuIndex]  

1.  Wenn DevTools geöffnet ist, wählen Sie `Control` + `Shift` + `P` \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    Das **Befehlsmenü** ist ein fuzzy search autocomplete combobox.  
1.  Geben Sie den Namen des Zu öffnende Panels ein, und navigieren Sie dann auf der Tastatur zur `Down Arrow` richtigen Option.  
1.  Wählen `Enter` Sie aus, um einen Befehl auszuführen.  

Führen Sie die folgenden Aktionen aus, um das **Elementtool zu** öffnen.  

1.  Öffnen Sie das **Befehlsmenü**.  
1.  Geben `E` Sie dann `L` ein.  Die **Option Panel > Elemente** anzeigen ist ausgewählt.  
1.  Wählen `Enter` Sie diese Option aus, um den Befehl auszuführen, mit dem der Bereich geöffnet wird.  

Öffnen Sie einen Bereich auf diese Weise, um den Fokus auf den Inhalt des Panels zu konzentrieren.  Im Fall des **Elements-Tools** wird der Fokus in die **DOM-Struktur verlagert.**  

## <a name="elements-panel"></a>Elementbereich  

### <a name="inspect-an-element-on-the-page"></a>Überprüfen eines Elements auf der Seite  

1.  Navigieren Sie zu dem Element, das Sie überprüfen möchten, indem Sie den Cursor in der Bildschirmausgabe verwenden.  
1.  Simulieren Sie einen Rechtsklick mithilfe einer Maus auf das Element, um das Kontextmenü zu öffnen.  
1.  Wählen Sie die **Option Überprüfen** aus.  Dadurch wird der Bereich Elemente geöffnet und das Element in der #A0 ][DevtoolsDomIndexViewDomNodes] fokussiert.  

Der **DOM-Baum** ist als [ARIA-Struktur ausgelegt.][W3CWaiAriaTree]  Navigieren Sie beispielsweise zu [Navigieren Sie in der **#A0** mit einer Tastatur][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Kopieren des Codes für ein Element in der DOM-Struktur  

1.  Zeigen Sie mit dem Fokus auf einen Knoten in der **DOM-Struktur**auf den Knoten, und öffnen Sie das Kontextmenü \(rechtsklicken\).  
1.  Erweitern Sie die **Option Kopieren.**  
1.  Wählen **Sie Kopieren outerHTML**aus.  

**Bekannte Probleme**  

*   **Copy outerHTML** wählt häufig nicht den aktuellen Knoten aus, sondern den übergeordneten Knoten.  Der Inhalt des Elements sollte sich jedoch weiterhin im kopierten outerHTML-Element enthalten.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Ändern der Attribute eines Elements in der DOM-Struktur  

*   Mit dem Fokus auf einem Knoten in der **DOM-Struktur**wählen Sie aus, `Enter` um ihn bearbeitbar zu machen.  
*   Wählen `Tab` Sie diese Option aus, um zwischen Attributwerten zu wechseln.  Wenn Sie "Leerzeichen" hören, befinden Sie sich innerhalb einer leeren Texteingabe und können einen neuen Attributwert eingeben.  
*   Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um die Änderung zu akzeptieren und den gesamten Inhalt des Elements zu hören.  

**Bekannte Probleme**  

*   Wenn Sie in die Texteingabe eingeben, erhalten Sie kein Feedback.  Wenn Sie einen Tippfehler erstellen und die Pfeiltasten verwenden, um Ihre Eingaben zu erkunden, erhalten Sie auch kein Feedback.  Die einfachste Möglichkeit, Ihre Arbeit zu überprüfen, besteht in der Annahme der Änderung, und lauschen Sie dann, ob das gesamte Element angekündigt werden soll.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Bearbeiten des HTML eines Elements in der DOM-Struktur  

*   Mit dem Fokus auf einem Knoten in der **DOM-Struktur**wählen Sie aus, `Enter` um ihn bearbeitbar zu machen.  
*   Wählen `Tab` Sie diese Option aus, um zwischen Attributwerten zu wechseln.  Wenn Sie beispielsweise den Namen des Elements hören, befinden Sie sich innerhalb einer Texteingabe und können den Typ `h2` des Elements ändern.  
*   Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um die Änderung zu akzeptieren.  

Wenn Sie z. B. `h3` `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) `h3` eingeben und auswählen, ändern sich die Start- und Endtags des Elements.  

## <a name="elements-tool-panels"></a>Elemente-Toolpanels  

Das **Elementtool** enthält zusätzliche Registerkarten zum Überprüfen von Elementen wie dem auf ein Element angewendeten CSS oder dem relevanten Ort in der Barrierefreiheitsstruktur.  

*   Wählen Sie mit Fokus auf einem Knoten in der **DOM-Struktur**aus, bis Sie hören, dass der Bereich `Tab` **Formatvorlagen** ausgewählt ist.  
*   Verwenden Sie `Right Arrow` die, um andere verfügbare Registerkarten zu erkunden.  

Die **DOM-Struktur** wandelt Elemente mit Attributen in fokussierbare Links um, sodass Sie möglicherweise mehr als einmal auswählen müssen, um den Bereich `href` `Tab` **Formatvorlagen zu** erreichen.  

**Bekannte Probleme**  

Auf **die Registerkarten DOM-Haltepunkte** und Eigenschaften kann nicht über die Tastatur zugegriffen werden. ****  

### <a name="styles-pane"></a>Formatvorlagenbereich  

Suchen Sie **im Bereich** Formatvorlagen nach Steuerelementen zum Filtern von Formatvorlagen, zum Toggen von Elementzuständen \(z. B. [:active][MDNActive] und [:focus][MDNFocus]\), zum Toggen von Klassen und zum Hinzufügen neuer Klassen.  Es gibt auch ein leistungsfähiges Formatprüfungstool zum Untersuchen und Ändern von Formatvorlagen, die derzeit auf das Element angewendet werden, das im Fokus der **DOM-Struktur steht.**  

Das wichtigste Konzept, das Sie im Bereich **Formatvorlagen** verstehen müssen, ist, dass nur Formatvorlagen für den aktuell ausgewählten Knoten in der **DOM-Struktur angezeigt werden.**  Angenommen, Sie prüfen die Formatvorlagen eines Knotens, und jetzt möchten Sie die Formatvorlagen `<header>` für einen Knoten `<footer>` betrachten.  Dazu müssen Sie zunächst den Knoten in der `<footer>` **DOM-Struktur auswählen.**  Möglicherweise ist es schneller, den [Inspect-Workflow](#inspect-an-element-on-the-page) zu verwenden, um einen Knoten zu überprüfen, der sich in der allgemeinen Nähe des Knotens \(z. B. ein Link in der Fußzeile\) befindet, der die DOM-Struktur in den Mittelpunkt stellt, und dann mit der Tastatur zu dem genauen Knoten zu navigieren, an dem Sie interessiert `footer` sind. ****  

#### <a name="navigate-the-styles-pane"></a>Navigieren im Bereich Formatvorlagen  

Da alle Formatvorlagentools auf die eine oder **** andere Weise wieder mit dem Formatvorlagenbereich verbinden, ist es sinnvoll, zuerst ein Experte für dieses Tool zu werden.  

*   Mit dem Fokus auf den **Bereich Formatvorlagen** wählen Sie aus, um den Fokus innerhalb zu verschieben `Tab` und den Inhalt zu erkunden.  
*   Wählen `Tab` Sie aus, bis die erste Formatvorlage aktiv wird.  Wenn Sie eine Bildschirmleseausgabe verwenden, wird diese erste Formatvorlage als `element.style {}` angekündigt.  
*   Wählen `Down Arrow` Sie diese Option aus, um in der Liste der Formatvorlagen in der Reihenfolge der Spezifizität zu navigieren.  Eine Bildschirmleseausgabe gibt jede Formatvorlage an, beginnend mit dem Namen der CSS-Datei, der Zeilennummer, in der die Formatvorlage angezeigt wird, und dem Namen der Formatvorlage.  Beispiel: `main.css:233 .card__img {}`.  
*   Wählen `Enter` Sie diese Option aus, um eine Formatvorlage ausführlicher zu prüfen.  Der Fokus beginnt mit einer bearbeitbaren Version des Formatnamens.  
*   Wählen `Tab` Sie diese Option aus, um zwischen bearbeitbaren Versionen jeder CSS-Eigenschaft und den entsprechenden Werten zu wechseln.  Am Ende jedes Formatvorlagenblocks befindet sich ein leeres, bearbeitbares Textfeld, das Sie zum Hinzufügen zusätzlicher CSS-Eigenschaften verwenden können.  
*   Sie können weiterhin auswählen, um durch die Liste der Formatvorlagen zu navigieren, oder wählen Sie aus, um den Modus zu beenden und zur Navigation durch `Tab` `Escape` Pfeiltasten zurückzufahren.  

Navigieren Sie zu [Formatvorlagenbereichtastaturreferenz][DevtoolsShortcutsStylesPaneKeyboard].  

**Bekannte Probleme**  

*   Wenn Sie das Bearbeitungstextfeld **Filter** verwenden, können Sie nicht mehr in der Liste der Formatvorlagen navigieren.  

#### <a name="toggle-element-state"></a>Zustand des Umschaltelements  

So schalten Sie den Status eines Elements um, z. B. `:active` oder `:focus` :  

1.  Navigieren Sie zum **Bereich Formatvorlagen,** und wählen Sie aus, bis die Schaltfläche `Tab` **Umschaltfläche Elementstatus** den Fokus hat.  
1.  Wählen `Enter` Sie diese Option aus, um die Auflistung der Elementzustände zu erweitern.  Die Elementzustände werden als Gruppe von Kontrollkästchen dargestellt.  
1.  Wählen `Tab` Sie aus, bis der erste Zustand , `:active` den Fokus hat.  
1.  Wählen `Space` Sie diese Option aus, um sie zu aktivieren.  Wenn das aktuell ausgewählte Element in der DOM-Struktur über eine Formatvorlage `:active` verfügt, wird es nun angewendet.  
1.  Halten `Tab` Sie sich, um alle verfügbaren Zustände zu erkunden.  

#### <a name="add-an-existing-class"></a>Hinzufügen einer vorhandenen Klasse  

Neben der Schaltfläche **Umschaltfläche Elementstatus** befindet sich die **Schaltfläche Elementklassen.**  Um den Fokus darauf zu verschieben, wählen `Tab` Sie aus, und wählen Sie `Enter` aus.  Der Fokus wechselt in ein Bearbeitungstextfeld mit der Bezeichnung **Neue Klasse hinzufügen.**  

Die **Schaltfläche Elementklassen** wird hauptsächlich zum Hinzufügen vorhandener Klassen zu einem Element verwendet.  Wenn Ihr Stylesheet beispielsweise eine Hilfsklasse namens enthielt, können Sie innerhalb des Bearbeitungstextfelds auswählen, um eine Vorschlagsliste mit Klassen anzeigen und den Vorschlag `.clearfix` `.` `Down Arrow` `.clearfix` suchen.  Oder geben Sie den Klassennamen selbst ein, und wählen Sie `Enter` ihn aus, um ihn anzuwenden.  

#### <a name="add-a-new-style-rule"></a>Hinzufügen einer neuen Formatvorlageregel  

Neben der Schaltfläche **Elementklassen** befindet sich die **Schaltfläche Neue Formatvorlageregel.**  Um den Fokus darauf zu verschieben, wählen `Tab` Sie aus, und wählen Sie `Enter` aus.  Der Fokus wird in ein bearbeitbares Textfeld innerhalb des Formatprüfungsinspektors bewegt.  Der anfängliche Textinhalt des Felds ist der Tagname des Elements, das in der **DOM-Struktur ausgewählt ist.**  
Sie können einen beliebigen Klassennamen in dieses Feld eingeben und dann auswählen, um `Tab` ihm CSS-Eigenschaften zuzuordnen.  

### <a name="computed-tab"></a>Registerkarte "Berechnet"  

Mit dem Fokus auf der Registerkarte **Berechnet** wählen Sie aus, um den Fokus nach innen zu verschieben `Tab` und den Inhalt zu erkunden.  Auf der **Registerkarte Berechnet gibt** es Steuerelemente zum Untersuchen, welche CSS-Eigenschaften tatsächlich auf ein Element in der Reihenfolge der Spezifizität angewendet werden.  

<!--todo: add computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Erkunden aller berechneten Formatvorlagen  

Wählen `Tab` Sie aus, bis Sie die Sammlung berechneter Formatvorlagen erreicht haben.  Diese werden als [ARIA-Struktur dargestellt.][W3CWaiAriaTree]  Beim Erweitern eines Listenfelds wird angezeigt, welche CSS-Selektoren die berechnete Formatvorlage anwenden.  Diese Selektoren sind nach Spezifizität organisiert.  Eine Bildschirmleseausgabe gibt den berechneten Wert an, mit dem der CSS-Selektor derzeit übereinstimmen soll, den Dateinamen des Stylesheets, das die Auswahl enthält, und die Zeilennummer für die Auswahl.  

**Bekannte Probleme**  

*   Wenn Sie das Textfeld **Filter** verwenden, können Sie formatvorlagen nicht mehr überprüfen.  

### <a name="event-listeners-tab"></a>Registerkarte "Ereignislistener"  

Innerhalb des **Elements-Tools** können Sie die Ereignislistener überprüfen, die auf ein Element angewendet wurden, indem Sie die Registerkarte **Ereignislistener** verwenden.  Wählen Sie im Bereich **Formatvorlagen** den Aus, um zum Bereich `Right Arrow` Ereignislistener **zu** navigieren.  

#### <a name="explore-event-listeners"></a>Erkunden von Ereignislistenern  

Ereignislistener werden als [ARIA-Struktur dargestellt.][W3CWaiAriaTree]  Sie können die Pfeiltasten verwenden, um sie zu navigieren.  Eine Bildschirmleseausgabe gibt den Namen des DOM-Objekts an, an das der Ereignislistener angefügt ist, sowie den Dateinamen, in dem der Ereignislistener definiert ist, und die Zeilennummer.  

### <a name="accessibility-pane"></a>Barrierefreiheitsbereich  

Mit fokus auf **den** Bereich Barrierefreiheit wählen Sie aus, um den Fokus innerhalb zu verschieben und den Inhalt zu `Tab` erkunden.  Im Bereich [Barrierefreiheit][DevtoolsAccessibilityReference] gibt es Steuerelemente zum Untersuchen der Barrierefreiheitsstruktur, der auf ein Element angewendeten ARIA-Attribute und der berechneten Barrierefreiheitseigenschaften.  

#### <a name="accessibility-tree"></a>Barrierefreiheitsstruktur  

Die **Barrierefreiheitsstruktur** wird als [ARIA-Struktur dargestellt,][W3CWaiAriaTree] wobei jede einem `treeitem` Element im DOM entspricht.  Die Struktur gibt die berechnete Rolle für den ausgewählten Knoten an.  Generische Elemente wie und werden in der Struktur als `div` `span` "GenericContainer" angekündigt.  Verwenden Sie die Pfeiltasten, um die Struktur zu durchlaufen und Beziehungen zwischen übergeordneten und untergeordneten Daten zu erkunden.  

**Bekannte Probleme**  

*   Der Typ der vom Barrierefreiheitsbereich verwendeten [ARIA-Struktur][W3CWaiAriaTree] wird möglicherweise in Microsoft Edge für macOS-Sprachleser wie VoiceOver nicht ordnungsgemäß verfügbar gemacht. ****  Abonnieren Sie [Chromium Problem #868480,][ChromiumIssues868480] um über den Fortschritt in diesem Problem informiert zu werden.  
*   Jeder der Abschnitte **"ARIA Attributes"** und **"Computed Properties"** wird als [ARIA-Struktur][W3CWaiAriaTree]gekennzeichnet, verfügt aber zurzeit nicht über die Fokusverwaltung und kann nicht über die Tastatur ausgeführt werden.  

## <a name="audits-panel"></a>Überwachungspanel  

Mit **dem Tool** "Audits" sollten Sie eine Reihe von Tests für eine Website ausführen, um nach häufigen Problemen im Zusammenhang mit Leistung, Barrierefreiheit, SEO und einer Reihe anderer Kategorien zu suchen.  

### <a name="configure-and-run-an-audit"></a>Konfigurieren und Ausführen einer Überwachung  

1.  Wenn das **Überwachungstool** zum ersten Mal **** geöffnet wird, wird der Fokus auf der Schaltfläche Überwachung ausführen am Ende des Formulars platziert.  Standardmäßig ist das Formular so konfiguriert, dass Überwachungen für jede Kategorie mithilfe der mobilen Emulation für eine simulierte 3G werden.  
1.  Verwenden `Shift` + `Tab` oder navigieren Sie zurück im Durchsuchen-Modus, um die Überwachungseinstellungen zu ändern.  
1.  Wenn Sie bereit sind, die Überwachung ausführen zu können, navigieren Sie zurück zur Schaltfläche **Überwachung ausführen,** und wählen Sie `Enter` aus.  
1.  Der Fokus wechselt in ein modales Fenster mit einer **Schaltfläche Abbrechen,** mit der Sie die Überwachung beenden können.  Möglicherweise hören Sie eine Reihe von Earcons, wenn die Überwachung ausgeführt wird und die Seite mehrmals aktualisiert wird.  

**Bekannte Probleme**  

*   Die verschiedenen Abschnitte des Konfigurationsformulars sind derzeit nicht mit einem Element `fieldset` gekennzeichnet.  Es ist möglicherweise einfacher, sie im Durchsuchen-Modus zu navigieren, um herauszufinden, welche Steuerelemente den einzelnen Abschnitten zugeordnet sind.  
*   Es gibt keine Ankündigung für earcon oder live region, wenn die Überwachung abgeschlossen ist.  Im Allgemeinen dauert es ungefähr 30 Sekunden, danach sollten Sie zu den Ergebnissen navigieren können.  Die Verwendung des Durchsuchen-Modus ist möglicherweise die einfachste Möglichkeit, um die Ergebnisse zu erreichen.  

### <a name="navigate-the-audit-report"></a>Navigieren im Überwachungsbericht  

Der Überwachungsbericht ist in Abschnitte unterteilt, die den einzelnen Überwachungskategorien entsprechen.  Der Bericht wird mit einer Liste der Ergebnisse für jede Kategorie geöffnet.  Diese Bewertungen sind auch Links, die verwendet werden können, um zu den relevanten Abschnitten zu springen.  In jedem Abschnitt sind erweiterbare Elemente enthalten, die Informationen zu `details` bestandenen oder fehlgeschlagenen Prüfungen enthalten.  Standardmäßig werden nur fehlerhafte Überwachungen angezeigt.  Jeder Abschnitt endet mit einem endgültigen `details` Element, das alle übergebenen Überwachungen enthält.  

Verwenden Sie zum Ausführen einer neuen Überwachung, um den Bericht zu beenden und nach der Schaltfläche `Shift` + `Tab` Überwachung **ausführen zu** suchen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Barrierefreiheitsreferenz | Microsoft Docs"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Der Bereich Barrierefreiheit – Barrierefreiheitsreferenz | Microsoft Docs"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Führen Sie Befehle mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte Mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes "DOM-Knoten anzeigen – Erste Schritte mit dem Anzeigen und Ändern der DOM-| Microsoft Docs"  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get started with viewing and changing the DOM | Microsoft Docs"  
[DevtoolsOpen]: .. /open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcuts]: .. /shortcuts/index.md "Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts "Stile panel keyboard shortcuts - Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problem 868480 – Verfügbar machen von ARIA-Baumstrukturen als Tabellen in Mac-Barrierefreiheit"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Neues Problem – MicrosoftDocs/edge-developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ":active | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ":focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Probleme - Chromium - Monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (role) – Accessible Rich Internet Applications (WAI-ARIA) 1.1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Struktur (Rolle) – Accessible Rich Internet Applications (WAI-ARIA) 1.1 | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) und wird von [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[RobDodson]: https://developers.google.com/web/resources/contributors#rob-dodson  
