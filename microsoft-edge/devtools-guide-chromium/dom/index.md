---
description: Hier erfahren Sie, wie Sie Knoten anzeigen, nach Knoten suchen, Knoten bearbeiten, auf Knoten in der Konsole verweisen, Knoten Änderungen unterbrechen und vieles mehr.
title: Erste Schritte beim Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8c0b544f2c4717a01d09c287f1167c81456a97f3
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125027"
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

# Erste Schritte beim Anzeigen und Ändern des DOM  

Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen zum Anzeigen und Ändern des DOM einer Seite mit Microsoft Edge devtools zu erfahren.  

In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen Dom und HTML kennen.  Eine Erläuterung finden Sie unter [Anhang: HTML im Vergleich zum Dom](#appendix-html-versus-the-dom) .  

## Öffnen von Dom-Beispielen  

1.  Halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie **DOM-Beispiele** aus, die auf einer neuen Registerkarte geöffnet werden sollen.  
    
    [DOM-Beispiele][GlitchDomExamples]  
    
## DOM-Knoten anzeigen  

In der DOM-Struktur des Elements Panels werden alle DOM-bezogenen Aktivitäten in devtools durchführen.  

### Überprüfen eines Knotens  

Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist über **prüfen** eine schnelle Möglichkeit, devtools zu öffnen und diesen Knoten zu untersuchen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter **Knoten überprüfen die**Option **Michelangelo** aus, und wählen Sie über **prüfen**aus.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Überprüfen eines Knotens  
    :::image-end:::  
    
    1.  Das **Element** Panel von devtools wird geöffnet.  `<li>Michelangelo</li>` ist in der **DOM-Struktur**hervorgehoben.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Markieren des `Michelangelo` Knotens  
        :::image-end:::  
        
        1.  Klicken Sie in der oberen linken Ecke von devtools auf das Symbol **inspizieren** \ ( ![ Inspect ][ImageInspectIcon] \).  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Das Symbol "über **prüfen** "  
            :::image-end:::  
            
1.  Klicken Sie unter **Knoten prüfen**auf den Text **Tokyo** .  Ist nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.  

Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.  Weitere Informationen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCssGetStarted].  

### Navigieren in der DOM-Struktur mithilfe einer Tastatur  

Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit der Tastatur in der DOM-Struktur navigieren.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter **DOM-Struktur mit einer Tastatur navigieren mit der**rechten Maustaste **Ringo** aus, und wählen Sie über **prüfen**aus.  `<li>Ringo</li>` ist in der DOM-Struktur ausgewählt.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Überprüfen des `Ringo` Knotens  
    :::image-end:::  
    
    1.  Drücken Sie zweimal die `Up` Pfeiltaste.  `<ul>`  markiert ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Überprüfen des `ul` Knotens  
        :::image-end:::  
        
    1.  Drücken Sie die `Left` Pfeiltaste.  Die `<ul>` Liste wird reduziert.  
    1.  Drücken Sie `Left` erneut die Pfeiltaste.  Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.  In diesem Fall ist es die `<div>` mit der ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Drücken Sie `Down` zweimal die Pfeiltaste, damit Sie die `<ul>` Liste, die Sie soeben reduziert haben, erneut ausgewählt haben.  Es sollte wie folgt aussehen: `<ul>... </ul>`  
    1.  Drücken Sie die `Right` Pfeiltaste.  Die Liste wird erweitert.  

### Scrollen Sie in die Ansicht  

Wenn Sie die DOM-Struktur anzeigen, sind Sie möglicherweise an einem DOM-Knoten interessiert, der sich derzeit nicht im Viewport befindet.  Angenommen, Sie haben einen Bildlauf zum Ende der Seite durchgeführt, und Sie sind an dem `<h1>` Knoten oben auf der Seite interessiert.  Durch **Scrollen in die Ansicht** können Sie das Ansichtsfenster schnell neu positionieren, damit Sie den Knoten sehen können.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Ansicht scrollen**mit der rechten Maustaste auf **Magritte** , und wählen Sie über **prüfen**aus.  
1.  Scrollen Sie zum Ende der Seite "DOM-Beispiele".  
1.  Der `<li>Magritte</li>` Knoten sollte weiterhin in ihrer DOM-Struktur ausgewählt sein.  Wenn dies nicht der Fall ist, gehen Sie zurück, um [in die Ansicht zu scrollen](#scroll-into-view) und neu zu beginnen  
1.  Klicken Sie mit der rechten Maustaste auf den `<li>Magritte</li>` Knoten, und wählen Sie **in Ansicht scrollen**aus.  Ihr Viewport führt einen Bildlauf nach oben durch, damit Sie den **Magritte** -Knoten sehen können.  Weitere Informationen finden Sie im [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option **Scrollen in Ansicht** nicht angezeigt werden kann.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Scrollen Sie in die Ansicht**  
    :::image-end:::  

### Suchen nach Knoten  

Sie können die DOM-Struktur nach Zeichenfolge, CSS-Auswahl oder XPath-Auswahl Durchsuchen.  

1.  Fokussieren Sie den Cursor auf das **Element** Panel.  
1.  Wählen Sie `Control` + `F` \ (Windows, Linux \) oder `Command` + `F` \ (macOS \) aus.  Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.  
1.  Geben Sie `The Moon is a Harsh Mistress` ein.  Der letzte Satz ist in der DOM-Struktur hervorgehoben.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Markieren der Abfrage in der Suchleiste  
    :::image-end:::  
    
Wie bereits erwähnt, unterstützt die Suchleiste auch CSS-und XPath-Auswahlen.  

## Bearbeiten des DOM  

Sie können das Dom im Handumdrehen bearbeiten und sehen, wie sich diese Änderungen auf die Seite auswirken.  

### Bearbeiten von Inhalten  

Um den Inhalt eines Knotens zu bearbeiten, doppelklicken Sie auf den Inhalt in der DOM-Struktur.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Inhalt bearbeiten**mit der rechten Maustaste auf **Michelle** , und wählen Sie über **prüfen**aus.  
    1.  Doppelklicken Sie in der DOM-Struktur auf `Michelle` .  Mit anderen Worten: Doppelklicken Sie auf den Text zwischen `<li>` und `</li>` .  Der Text wird hervorgehoben, um anzugeben, dass er markiert ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Bearbeiten des Texts  
        :::image-end:::  
        
    1.  Löschen `Michelle` Sie, geben `Leela` Sie ein, und wählen Sie dann aus, `Enter` um die Änderung zu bestätigen.  Der Text im Dom wechselt von **Michelle** zu **Leela**.  

### Bearbeiten von Attributen  

Um Attribute zu bearbeiten, doppelklicken Sie auf den Attributnamen oder-Wert.  Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Attribute bearbeiten**mit der rechten Maustaste auf **Howard** , und wählen Sie über **prüfen**aus.  
1.  Doppelklicken Sie auf `<li>` .  Der Text wird hervorgehoben, um anzugeben, dass der Knoten markiert ist.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Bearbeiten des Knotens  
    :::image-end:::  
    
1.  Drücken Sie die `Right` Pfeiltaste, fügen Sie ein Leerzeichen hinzu, geben `style="background-color:gold"` Sie ein, und wählen Sie dann aus `Enter` .  Die Hintergrundfarbe des Knotens ändert sich in Gold.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Hinzufügen eines `style` Attributs zum Knoten  
    :::image-end:::  
    
### Knotentyp bearbeiten  

Um den Typ eines Knotens zu bearbeiten, doppelklicken Sie auf den Typ, und geben Sie dann den neuen Typ ein.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Knotentyp bearbeiten**mit der rechten Maustaste auf **Hank** , und wählen Sie über **prüfen**aus.  
    1.  Doppelklicken Sie auf `<li>` .  Der Text `li` ist hervorgehoben.  
    1.  Löschen `li` Sie, geben `button` Sie ein, und wählen Sie dann aus `Enter` .  Der `<li>` Knoten wird in einen `<button>` Knoten geändert.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Ändern des Knotentyps in `button`  
        :::image-end:::  
        
### Neuanordnen von DOM-Knoten  

Ziehen Sie Knoten, um Sie neu anzuordnen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **DOM-Knoten neu anordnen**auf **Elvis Presley** , und wählen Sie über **prüfen**aus.  
    
    > [!NOTE]
    > Dies ist das letzte Element in der Liste.  
    
    1.  Ziehen Sie den Mauszeiger in der DOM-Struktur `<li>Elvis Presley</li>` an den Anfang der Liste.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Ziehen des Knotens an den Anfang der Liste  
        :::image-end:::  
        
### Zustand erzwingen  

Sie können die Knoten zwingen, in Zuständen wie,,, und zu bleiben `:active` `:hover` `:focus` `:visited` `:focus-within` .  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Zeigen Sie unter **Kraftzustand**auf **den Lord of the Flies**.  Die Hintergrundfarbe wird Orange.  
    1.  Klicken Sie mit der rechten Maustaste **auf den Lord of the Flies** und wählen Sie **prüfen**aus.  
    1.  Klicken Sie mit der rechten Maustaste `<li class="demo--hover">The Lord of the Flies</li>` , und wählen Sie **Zustand erzwingen**  >  **: hover**aus.  Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt wird.  Die Hintergrundfarbe bleibt Orange, auch wenn Sie nicht tatsächlich über den Knoten zeigen.  

### Ausblenden eines Knotens  

Wählen Sie aus `H` , um einen Knoten auszublenden.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Knoten ausblenden**mit der rechten Maustaste auf **den Stern mein Ziel** , und wählen Sie über **prüfen**aus.  
    1.  Drücken Sie die Eingabe `H` Taste.  Der Knoten ist ausgeblendet.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde  
        :::image-end:::  
        
    1.  Drücken Sie die `H` Taste erneut.  Der Knoten wird wieder angezeigt.  

### Löschen eines Knotens  

Wählen Sie aus `Delete` , um einen Knoten zu löschen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Knoten löschen mit der**rechten Maustaste auf **Fundament** , und wählen Sie über **prüfen**aus.  
    1.  Drücken Sie die Eingabe `Delete` Taste.  Der Knoten wird gelöscht.  
    1.  Wählen Sie `Control` + `Z` \ (Windows, Linux \) oder `Command` + `Z` \ (macOS \) aus.  Die letzte Aktion wird rückgängig gemacht, und der Knoten wird wieder angezeigt.  

## Access-Knoten in der Konsole  

DevTools bietet einige Tastenkombinationen für den Zugriff auf DOM-Knoten über die Konsole oder das Abrufen von JavaScript-verweisen auf jede einzelne.  

### Verweisen auf den aktuell ausgewählten Knoten mit $0  

Wenn Sie einen Knoten überprüfen, `== $0` bedeutet der Text neben dem Knoten, dass Sie auf diesen Knoten in der Konsole mit der Variablen verweisen können `$0` .  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter **Bezug auf den aktuell ausgewählten Knoten mit $0 mit**der rechten Maustaste **die linke Hand von Darkness** aus, und wählen Sie über **prüfen**aus.  
    1.  Drücken Sie die Eingabe `Escape` Taste, um den Konsolen Einzug zu öffnen.  
    1.  Geben `$0` Sie ein, und drücken Sie die Eingabe `Enter` Taste.  Das Ergebnis des Ausdrucks zeigt, dass `$0` ausgewertet wird `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Das Ergebnis des ersten `$0` Ausdrucks in der **Konsole**  
        :::image-end:::  
        
    1.  Zeigen Sie mit der Maus auf das Ergebnis.  Der Knoten ist im Viewport hervorgehoben.  
    1.  Klicken Sie `<li>Dune</li>` in die DOM-Struktur, geben Sie `$0` die Konsole erneut ein, und wählen Sie dann `Enter` erneut aus.  Wird nun `$0` ausgewertet `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Das Ergebnis des zweiten `$0` Ausdrucks in der **Konsole**  
        :::image-end:::  
        
### Speichern als globale Variable  

Wenn Sie viele Male wieder auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter **als globale Variable speichern** **den großen Ruhezustand** aus, und wählen Sie über **prüfen**aus.  
    1.  Klicken Sie `<li>The Big Sleep</li>` mit der rechten Maustaste in die DOM-Struktur, und wählen Sie **als globale Variable speichern**aus.  Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt wird.  
    1.  Geben `temp1` Sie die Konsole ein, und wählen Sie dann aus `Enter` .  Das Ergebnis des Ausdrucks zeigt, dass die Variable zum Knoten ausgewertet wird.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Das Ergebnis des `temp1` Ausdrucks  
        :::image-end:::  
        
### Kopieren des js-Pfads  

Kopieren Sie den JavaScript-Pfad zu einem Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **js-Pfad kopieren**mit der rechten Maustaste auf **die Brüder Karamazov** , und wählen Sie über **prüfen**aus.  
    1.  Klicken Sie `<li>The Brothers Karamazov</li>` mit der rechten Maustaste in die DOM **Copy**-Struktur, und wählen Sie Copy  >  **js Path**kopieren aus.  Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.  
    1.  Wählen Sie `Control` + `V` \ (Windows, Linux \) oder `Command` + `V` \ (macOS \) aus, um den Ausdruck in die Konsole einzufügen.  
    1.  Wählen Sie aus `Enter` , um den Ausdruck auszuwerten.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Das Ergebnis des Ausdrucks " **js-Pfad kopieren** "  
        :::image-end:::  
        
## Änderungen am Dom unterbrechen  

Mit devtools können Sie das JavaScript einer Seite anhalten, wenn das DOM vom JavaScript geändert wird.  

### Unterbrechen von Attributänderungen  

Verwenden Sie die Attribut Änderungs Haltepunkte, wenn Sie das JavaScript anhalten möchten, das dazu führt, dass das Attribut eines Knotens geändert wird.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Umbruch bei Attributänderungen auf** **Sauerkraut** , und wählen Sie über **prüfen**aus.  
    1.  Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Sauerkraut</li>` und wählen Sie **bei**  >  **Attributänderungen**aufheben aus.  Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Unterbrechen von Attributänderungen**  
        :::image-end:::  
        
    1.  Im nächsten Schritt werden Sie angewiesen, auf eine Schaltfläche zu klicken, mit der der Code der Seite angehalten wird.  Nachdem die Seite angehalten wurde, können Sie die Seite nicht mehr scrollen.  Sie müssen **Resume-Skript** \ ( ![ Resume ][ImageResumeScriptIcon] -Skript \) auswählen, um die Seite erneut scrollen zu lassen.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Wo wird das Skript fortgesetzt?  
        :::image-end:::  
        
    1.  Klicken Sie oben auf die Schaltfläche **Hintergrund einstellen** .  Dadurch wird das `style` Attribut des Knotens auf festgelegt `background-color:thistle` .  DevTools hält die Seite an und hebt den Code hervor, der zum Ändern des Attributs geführt hat.  
    1.  Wählen Sie, wie bereits erwähnt, **fortsetzen-Skript** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.  
    
### Unterbrechung beim Entfernen von Knoten  

Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte für die Knoten Entfernung.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Klicken Sie unter **Unterbrechungs Vorgang beim Entfernen von Knoten mit der**rechten Maustaste auf **Neuromancer** , und wählen Sie über **prüfen**aus.  
    1.  Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Neuromancer</li>` und wählen Sie **Unterbrechung beim**  >  **Entfernen von Knoten**aus.  Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.  
    1.  Klicken Sie oben auf die Schaltfläche **Löschen** .  DevTools hält die Seite an und hebt den Code hervor, der dazu geführt hat, dass der Knoten entfernt wurde.  
    1.  Wählen Sie **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.  
    
### Unterbrechen von Änderungen an Teilstruktur  

Nachdem Sie einen Haltepunkt für die Unterstruktur Änderung auf einem Knoten platziert haben, wird die Seite von devtools angehalten, wenn ein Nachfolger des Knotens hinzugefügt oder entfernt wird.  

1.  [Öffnen Sie DOM-Beispiele](#open-dom-examples).  
1.  Wählen Sie unter unter **Brechung bei Teilstruktur Änderungen**mit der rechten Maustaste **ein Feuer auf der Tiefe** aus, und wählen Sie über **prüfen**aus.  
    1.  Klicken Sie in der DOM-Struktur mit der rechten Maustaste auf `<ul id="target">` den Knoten oben `<li>A Fire Upon the Deep</li>` , und wählen Sie unter Teil **Break On**  >  **Strukturänderungen**aufheben aus.  Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.  
    1.  Wählen Sie **Kind hinzufügen**aus.  Der Code wird angehalten `<li>` , weil der Liste ein Knoten hinzugefügt wurde.  
    1.  Wählen Sie **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.  
    
## Nächste Schritte  

, Die die meisten der Dom-bezogenen Features in devtools abdeckt.  Sie können die restlichen Personen entdecken, indem Sie mit der rechten Maustaste auf Knoten in der DOM-Struktur klicken und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.  Siehe auch [Tastenkombinationen im Element Panel][DevToolsShortcutsElements].  

Schauen Sie sich die [Microsoft Edge devtools-Startseite][MicrosoftEdgeDevTools] an, um alles mögliche zu entdecken, was Sie mit devtools tun können.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## Anhang: HTML im Vergleich zum Dom  

Im folgenden Abschnitt wird schnell der Unterschied zwischen HTML und dem Dom erläutert.  

:::row:::
   :::column span="":::
      Wenn Sie eine Seite mit einem Webbrowser anfordern, gibt der Server HTML wie den folgenden Codeausschnitt zurück.  

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
      Der Browser analysiert den HTML-Code und erstellt eine Struktur von Objekten wie der folgenden Liste.  
      
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
      Im Moment sieht es genauso aus wie das HTML, aber angenommen, das Skript, auf das am Ende des HTML-Codes verwiesen wird, führt den folgenden Codeausschnitt aus.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Dieser Code entfernt den `h1` Knoten und fügt `p` dem DOM einen weiteren Knoten hinzu.  Das vollständige Dom zeigt nun die folgende Liste an.  
      
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

Der HTML-Code für die Seite ist jetzt anders als das DOM.  Mit anderen Worten, HTML steht für den anfänglichen Seiteninhalt, und das DOM steht für den aktuellen Seiteninhalt.  Wenn JavaScript-Knoten hinzugefügt, entfernt oder bearbeitet werden, wird das DOM anders als das HTML-Code.  

Weitere Informationen finden Sie unter [Einführung in das DOM][MDNIntroductionToDOM] .  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## Anhang: fehlende Optionen  

Viele der Anweisungen in diesem Lernprogramm weisen Sie an, mit der rechten Maustaste auf einen Knoten in der DOM-Struktur zu klicken und dann im Kontextmenü, das eingeblendet wird, eine Option auszuwählen.  Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit der rechten Maustaste auf den Knotentext zu klicken.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Wo klicken, wenn nicht alle Optionen angezeigt werden  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Tastenkombinationen im Element Panel – Tastenkombinationen für Microsoft Edge devtools | Microsoft docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chrom) devtools Dom-Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
