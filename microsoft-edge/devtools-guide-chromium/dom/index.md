---
description: Anzeigen von Knoten, Suchen nach Knoten, Bearbeiten von Knoten, Referenzknoten in der Konsole, Umbruch bei Knotenänderungen und vieles mehr.
title: Erste Schritte mit dem Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bb2b733cfa3597c47f0a20de00e9c8b506e7c41c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398329"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a>Erste Schritte mit dem Anzeigen und Ändern des DOM  

Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen des Anzeigens und Änderns des DOM einer Seite mithilfe von Microsoft Edge DevTools zu erlernen.  

In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen DOM und HTML kennen.  Navigieren Sie [zu Anhang: HTML im Vergleich zum DOM,](#appendix-html-versus-the-dom) um eine Erläuterung zu erhalten.  

## <a name="open-dom-examples"></a>Öffnen von DOM-Beispielen  

1.  Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **DOM-Beispiele aus,** um sie auf einer neuen Registerkarte zu öffnen.  
    
    [DOM-Beispiele][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Anzeigen von DOM-Knoten  

In der DOM-Struktur des Elements-Panels werden alle DOM-bezogenen Aktivitäten in DevTools verwendet.  

### <a name="inspect-a-node"></a>Überprüfen eines Knotens  

Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist **Inspect** eine schnelle Möglichkeit, DevTools zu öffnen und den Knoten zu untersuchen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Prüfen eines Knotens**mit der rechten Option **"Michelangelo"** aus, und wählen Sie **Inspect aus.**  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Überprüfen eines Knotens  
    :::image-end:::  
    
    1.  Das **Elementtool** von DevTools wird geöffnet.  `<li>Michelangelo</li>` wird in der **DOM-Struktur hervorgehoben.**  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Hervorheben des Knotens "Michelangelo"" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Hervorheben des `Michelangelo` Knotens  
        :::image-end:::  
        
        1.  Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ][ImageInspectIcon] \) aus.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Symbol "Überprüfen"" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Das **Symbol "Überprüfen"**  
            :::image-end:::  
            
1.  Wählen **Sie unter Überprüfen eines Knotens**den **Tokio-Text** aus.  Wird nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.  

Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.  Navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCssGetStarted].  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Navigieren in der DOM-Struktur mit einer Tastatur  

Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit der Tastatur in der DOM-Struktur navigieren.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Navigieren in der DOM-Struktur mit einer Tastatur**mit der rechten Option **Ringo** aus, und wählen Sie **Überprüfen aus.**  `<li>Ringo</li>` ist in der DOM-Struktur ausgewählt.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Knotens Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Überprüfen des `Ringo` Knotens  
    :::image-end:::  
    
    1.  Wählen Sie `Up` die Pfeiltaste 2 mal aus.  `<ul>`  markiert ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des ul-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Überprüfen des `ul` Knotens  
        :::image-end:::  
        
    1.  Wählen Sie `Left` die Pfeiltaste aus.  Die `<ul>` Liste wird reduziert.  
    1.  Wählen Sie `Left` die Pfeiltaste erneut aus.  Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.  In diesem Fall ist es die `<div>` mit der ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Wählen Sie die Pfeiltaste 2 mal aus, damit Sie die Liste, die Sie `Down` `<ul>` gerade reduziert haben, erneut ausgewählt haben.  Es sollte wie folgt aussehen: `<ul>... </ul>`  
    1.  Wählen Sie `Right` die Pfeiltaste aus.  Die Liste wird erweitert.  

### <a name="scroll-into-view"></a>Bildlauf in die Ansicht  

Wenn Sie die DOM-Struktur anzeigen, interessieren Sie sich möglicherweise für einen DOM-Knoten, der sich derzeit nicht im Viewport befindet.  Angenommen, Sie haben einen Bildlauf zum unteren Rand der Seite durchgeführt, und Sie interessieren sich für den Knoten am oberen Rand `<h1>` der Seite.  **Mit einem Bildlauf** in die Ansicht können Sie den Viewport schnell neu positionieren, sodass Sie den Knoten überprüfen können.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Scroll into View**mit der rechten Option **Magritte aus,** und wählen Sie **Inspect aus.**  
1.  Scrollen Sie zum Unteren Rand der Seite DOM-Beispiele.  
1.  Der `<li>Magritte</li>` Knoten sollte weiterhin in der DOM-Struktur ausgewählt werden.  Wenn nicht, wechseln Sie zurück zu [Bildlauf in die Ansicht,](#scroll-into-view) und starten Sie von vorn.  
1.  Zeigen Sie auf `<li>Magritte</li>` den Knoten, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Scroll into view aus.**  Ihr Viewport führt einen Bildlauf nach oben aus, sodass Sie den **Knoten Magritte überprüfen** können.  Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn Sie die Option In Ansicht **scrollen nicht überprüfen** können.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Bildlauf in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Bildlauf in die Ansicht**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Suchen nach Knoten  

Sie können die DOM-Struktur nach Zeichenfolge, CSS-Selektor oder XPath-Selektor durchsuchen.  

1.  Fokussieren Sie den Cursor auf das **Elementtool.**  
1.  Wählen `Control` + `F` Sie \(Windows, Linux\) oder `Command` + `F` \(macOS\) aus.  Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.  
1.  Geben Sie `The Moon is a Harsh Mistress` ein.  Der letzte Satz wird in der DOM-Struktur hervorgehoben.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Hervorheben der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Hervorheben der Abfrage in der Suchleiste  
    :::image-end:::  
    
Wie oben erwähnt, unterstützt die Suchleiste auch CSS- und XPath-Selektoren.  

## <a name="edit-the-dom"></a>Bearbeiten des DOM  

Sie können das DOM im Schnellmodus bearbeiten und überprüfen, wie sich die Änderungen auf die Seite auswirken.  

### <a name="edit-content"></a>Bearbeiten von Inhalten  

Doppelklicken Sie zum Bearbeiten des Inhalts eines Knotens in der DOM-Struktur auf den Inhalt.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Inhalt bearbeiten**mit der rechten Option **Michelle** aus, und wählen Sie **Inspect aus.**  
    1.  Doppelklicken Sie in der DOM-Struktur auf `Michelle` .  Doppelklicken Sie also auf den Text zwischen `<li>` und `</li>` .  Der Text wird hervorgehoben, um anzugeben, dass er ausgewählt ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Bearbeiten des Texts  
        :::image-end:::  
        
    1.  Delete `Michelle` , type , `Leela` then select to confirm the `Enter` change.  Der Text im DOM wird von **Michelle** zu **Leela geändert.**  

### <a name="edit-attributes"></a>Bearbeiten von Attributen  

Doppelklicken Sie zum Bearbeiten von Attributen auf den Attributnamen oder -wert.  Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Attribute bearbeiten**mit der rechten Option **Howard** aus, und wählen Sie **Inspect aus.**  
1.  Doppelklicken Sie `<li>` auf .  Der Text wird hervorgehoben, um anzugeben, dass der Knoten ausgewählt ist.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Bearbeiten des Knotens  
    :::image-end:::  
    
1.  Wählen Sie `Right` die Pfeiltaste aus, fügen Sie ein Leerzeichen hinzu, geben Sie `style="background-color:gold"` ein, und wählen Sie dann `Enter` aus.  Die Hintergrundfarbe des Knotens wird in Gold geändert.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Formatattributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Hinzufügen eines `style` Attributs zum Knoten  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Knotentyp bearbeiten  

Doppelklicken Sie zum Bearbeiten des Knotentyps auf den Typ, und geben Sie dann den neuen Typ ein.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Knotentyp bearbeiten**mit der rechten Option **Hank aus,** und wählen Sie **Inspect aus.**  
    1.  Doppelklicken Sie `<li>` auf .  Der Text `li` wird hervorgehoben.  
    1.  Delete `li` , type , `button` then select `Enter` .  Der `<li>` Knoten wird in einen Knoten `<button>` geändert.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Ändern des Knotentyps in `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Neu anordnen von DOM-Knoten  

Ziehen Sie Knoten, um sie neu anordnen zu können.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter Neu anordnen von **DOM-Knoten**mit der rechten Option **"Elvis Presley"** aus, und wählen Sie **Inspect aus.**  
    
    > [!NOTE]
    > Es ist das letzte Element in der Liste.  
    
    1.  Ziehen Sie in der DOM-Struktur `<li>Elvis Presley</li>` an den oberen Rand der Liste.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen Sie den Knoten an den oberen Rand der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Ziehen Sie den Knoten an den oberen Rand der Liste  
        :::image-end:::  
        
### <a name="force-state"></a>Force-Status  

Sie können erzwingen, dass Knoten in Zustände wie `:active` , , , und `:hover` `:focus` `:visited` `:focus-within` verbleiben.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Zeigen **Sie unter Force-Zustand**auf **Der Herr der Fliegt.**  Die Hintergrundfarbe wird orange.  
    1.  Zeigen Sie **auf Der Herr der Fliegt,** öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Überprüfen **aus.**  
    1.  Zeigen Sie `<li class="demo--hover">The Lord of the Flies</li>` auf , öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), und wählen Sie Force **State**  >  **:hover aus.**  Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  Die Hintergrundfarbe bleibt orange, auch wenn Sie nicht mit dem Mauszeiger auf den Knoten zeigen.  

### <a name="hide-a-node"></a>Ausblenden eines Knotens  

Wählen `H` Sie diese Option aus, um einen Knoten auszublenden.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Knoten ausblenden**mit der rechten Option The Stars My **Destination** aus, und wählen Sie **Inspect aus.**  
    1.  Wählen Sie den `H` Schlüssel aus.  Der Knoten ist ausgeblendet.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="So sieht der Knoten im DOM-Struktur aus, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           So sieht der Knoten im DOM-Struktur aus, nachdem er ausgeblendet wurde  
        :::image-end:::  
        
    1.  Wählen Sie `H` den Schlüssel erneut aus.  Der Knoten wird erneut angezeigt.  

### <a name="delete-a-node"></a>Löschen eines Knotens  

Wählen `Delete` Sie diese Option aus, um einen Knoten zu löschen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Knoten löschen**mit der rechten Option Foundation **aus,** und wählen Sie **Inspect aus.**  
    1.  Wählen Sie den `Delete` Schlüssel aus.  Der Knoten wird gelöscht.  
    1.  Wählen `Control` + `Z` Sie \(Windows, Linux\) oder `Command` + `Z` \(macOS\) aus.  Die letzte Aktion wird rückgängig gemacht, und der Knoten wird erneut angezeigt.  

## <a name="access-nodes-in-the-console"></a>Zugriffsknoten in der Konsole  

DevTools bietet einige Verknüpfungen für den Zugriff auf DOM-Knoten über die Konsole oder das Abrufen von JavaScript-Verweisen auf die einzelnen.  

### <a name="reference-the-currently-selected-node-with-0"></a>Verweisen auf den aktuell ausgewählten Knoten mit $0  

Wenn Sie einen Knoten überprüfen, bedeutet der Text neben dem Knoten, dass Sie in der Konsole mit der Variablen auf `== $0` diesen Knoten verweisen `$0` können.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Verweis auf den aktuell ausgewählten Knoten mit $0**die linke Hand **der** Dunklen aus, und wählen Sie **Überprüfen aus.**  
    1.  Wählen Sie die `Escape` Taste aus, um die Konsolenschubschubte zu öffnen.  
    1.  Geben `$0` Sie den Schlüssel ein, und wählen Sie diesen `Enter` aus.  Das Ergebnis des Ausdrucks zeigt, dass `$0` als ausgewertet `<li>The Left Hand of Darkness</li>` wird.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Das Ergebnis des ersten `$0` Ausdrucks in der **Konsole**  
        :::image-end:::  
        
    1.  Zeigen Sie auf das Ergebnis.  Der Knoten wird im Viewport hervorgehoben.  
    1.  Wählen `<li>Dune</li>` Sie in der DOM-Struktur aus, geben Sie die Konsole erneut `$0` ein, und wählen Sie dann erneut `Enter` aus.  Ausgewertet `$0` wird nun als `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Das Ergebnis des zweiten `$0` Ausdrucks in der **Konsole**  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Speichern als globale Variable  

Wenn Sie mehrmals auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Zeigen **Sie unter Store as global variable**auf The Big **Sleep**, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen**aus.  
    1.  Zeigen Sie in der DOM-Struktur auf, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `<li>The Big Sleep</li>` Maustaste\), und wählen Sie Store als globale Variable **aus.**  Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  
    1.  Geben `temp1` Sie in die Konsole ein, und wählen Sie dann `Enter` aus.  Das Ergebnis des Ausdrucks zeigt, dass die Variable zum Knoten ausgewertet wird.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des temp1-Ausdrucks" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Das Ergebnis des `temp1` Ausdrucks  
        :::image-end:::  
        
### <a name="copy-js-path"></a>Kopieren des JS-Pfads  

Kopieren Sie den JavaScript-Pfad in einen Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Zeigen **Sie unter JS-Pfad**kopieren auf **The Brothers Karamazov,** öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen aus.**  
    1.  Zeigen Sie in der DOM-Struktur auf, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `<li>The Brothers Karamazov</li>` Maustaste\), und wählen Sie **Kopieren**  >  **JS-Pfad kopieren aus.**  Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.  
    1.  Wählen `Control` + `V` Sie \(Windows, Linux\) oder `Command` + `V` \(macOS\) aus, um den Ausdruck in die Konsole zu einfügen.  
    1.  Wählen `Enter` Sie diese Option aus, um den Ausdruck auszuwerten.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Copy JS Path-Ausdrucks" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Das Ergebnis des **Copy JS Path-Ausdrucks**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Pause bei DOM-Änderungen  

Mit DevTools können Sie das JavaScript einer Seite anhalten, wenn JavaScript das DOM ändert.  

### <a name="break-on-attribute-modifications"></a>Unterbrechung von Attributänderungen  

Verwenden Sie Haltepunkte für Attributänderung, wenn Sie das JavaScript anhalten möchten, das bewirkt, dass sich jedes Attribut eines Knotens ändert.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Break on attribute modifications**mit der rechten Option **"Sauerkraut" aus,** und wählen Sie **Inspect aus.**  
    1.  Zeigen Sie in der DOM-Struktur auf , öffnen Sie das kontextbezogene Menü \(mit der rechten Maustaste auf\), und wählen Sie `<li id="target">Sauerkraut</li>` **Break On**  >  **Attribute Modifications aus.**  Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechung von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Unterbrechung von Attributänderungen**  
        :::image-end:::  
        
    1.  Im nächsten Schritt werden Sie angewiesen, eine Schaltfläche zu wählen, mit der der Code der Seite angehalten wird.  Nachdem die Seite angehalten wurde, können Sie keinen Bildlauf mehr auf der Seite durchführen.  Sie müssen Skript **fortsetzen** \( Skript fortsetzen \) auswählen, damit die Seite wieder ![ ][ImageResumeScriptIcon] scrollbar ist.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Where to resume script running" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Where to resume script running  
        :::image-end:::  
        
    1.  Wählen Sie **oben die Schaltfläche Hintergrund** festlegen aus.  Dadurch wird das `style` Attribut des Knotens auf . `background-color:thistle`  DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass das Attribut geändert wurde.  
    1.  Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ][ImageResumeScriptIcon] \), wie bereits erwähnt.  
    
### <a name="break-on-node-removal"></a>Unterbrechung beim Entfernen von Knoten  

Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte für die Knotenentfernung.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Unterbrechung beim Entfernen**von Knoten mit der rechten Option **Neuromancer aus,** und wählen Sie **Inspect aus.**  
    1.  Zeigen Sie in der DOM-Struktur auf , öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie Beim Knotenentfernung `<li id="target">Neuromancer</li>` ****  >  **pausenlos aus.**  Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  
    1.  Wählen Sie oben **die Schaltfläche** Löschen aus.  DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass der Knoten entfernt wurde.  
    1.  Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ][ImageResumeScriptIcon] \).  
    
### <a name="break-on-subtree-modifications"></a>Unterbrechung bei Änderungen der Unterstruktur  

Nachdem Sie einen Unterstrukturänderungs-Haltepunkt auf einem Knoten eingefügt haben, hält DevTools die Seite an, wenn eines der untergeordneten Elemente des Knotens hinzugefügt oder entfernt wird.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen **Sie unter Break on Subtree Modifications**mit der rechten Option A Fire Upon The **Deep** aus, und wählen Sie **Inspect aus.**  
    1.  Zeigen Sie in der DOM-Struktur auf , der den obigen Knoten ist, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Bei Unterstrukturänderungen `<ul id="target">` `<li>A Fire Upon the Deep</li>` ****  >  **pausen aus.**  Wenn die Option nicht angezeigt wird, navigieren Sie zu [Anhang: Fehlende Optionen](#appendix-missing-options).  
    1.  Wählen **Sie Untergeordnetes Hinzufügen aus.**  Der Code wird angehalten, da `<li>` der Liste ein Knoten hinzugefügt wurde.  
    1.  Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ][ImageResumeScriptIcon] \).  
    
## <a name="next-steps"></a>Nächste Schritte  

Dies deckt die meisten DOM-bezogenen Features in DevTools ab.  Sie können die restlichen Features ermitteln, indem Sie auf Knoten in der DOM-Struktur zeigen, das Kontextmenü \(rechtsklicken\) öffnen und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.  Navigieren Sie zu [Tastenkombinationen des Elements-Panels.][DevToolsShortcutsElements]  

Sehen Sie sich die [Microsoft Edge DevTools-Homepage an,][MicrosoftEdgeDevTools] um alles andere zu entdecken, was Sie mit DevTools tun können.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Anhang: HTML im Vergleich zum DOM  

Im folgenden Abschnitt wird der Unterschied zwischen HTML und DOM schnell erläutert.  

:::row:::
   :::column span="":::
      Wenn Sie einen Webbrowser zum Anfordern einer Seite verwenden, gibt der Server HTML wie den folgenden Codeausschnitt zurück.  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      Der Browser analysiert den HTML-Code und erstellt eine Struktur mit Objekten wie der folgenden Liste.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird als DOM bezeichnet.  

:::row:::
   :::column span="":::
      Derzeit sieht es genauso aus wie der HTML- Code, aber angenommen, das Skript, auf das unten im HTML verwiesen wird, führt den folgenden Codeausschnitt aus.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Dieser Code entfernt den `h1` Knoten und fügt dem DOM einen weiteren Knoten `p` hinzu.  Das vollständige DOM zeigt nun die folgende Liste an.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

Der HTML-Code für die Seite ist jetzt anders als das DOM.  Mit anderen Worten, HTML stellt anfänglichen Seiteninhalt dar, und das DOM stellt den aktuellen Seiteninhalt dar.  Wenn JavaScript Knoten hinzufügt, entfernt oder bearbeitet, wird das DOM anders als der HTML-Code.  

Navigieren Sie [zu Einführung in das DOM,][MDNIntroductionToDOM] um weitere Informationen zu erhalten.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Anhang: Fehlende Optionen  

In vielen Anweisungen in diesem Lernprogramm werden Sie angewiesen, den Mauszeiger auf einen Knoten in der DOM-Struktur zu zeigen, das Kontextmenü \(rechtsklicken\) zu öffnen und dann eine Option aus dem Kontextmenü zu wählen, das angezeigt wird.  Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit dem Mauszeiger vom Knotentext zu zeigen und das Kontextmenü \(rechtsklicken\) zu öffnen.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Auswählen, ob nicht alle Optionen angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Auswählen, ob nicht alle Optionen angezeigt werden  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) Developer Tools | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Tastenkombinationen des Elements-Tools – Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
