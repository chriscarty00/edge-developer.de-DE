---
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 005d2650a1633d49a8c6c2550c4b2c0c2e3f3be6
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601846"
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







# CSS-Referenz   



Entdecken Sie neue Workflows in dieser umfassenden Referenz zu den Microsoft Edge devtools-Features, die sich auf das Anzeigen und Ändern von CSS beziehen.  

Informationen zu den Grundlagen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCSSGetStarted] .  

## Auswählen eines Elements   

Mit dem Element Panel von devtools können **Sie das CSS** eines Elements gleichzeitig anzeigen oder ändern.  Das ausgewählte Element ist in der **DOM-Struktur**hervorgehoben.  Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.  Weitere Informationen finden Sie unter [Anzeigen des CSS für ein Element][DevToolsCSSGetStartedTutorial] für ein Lernprogramm.  

> [!NOTE]
> In [Abbildung 1](#figure-1)ist das `h1` Element, das in der **DOM-Struktur** hervorgehoben wird, das ausgewählte Element.  Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.  Auf der linken Seite ist das Element im Viewport hervorgehoben, allerdings nur, weil die Maus gerade in der DOM- **Struktur**darüber schwebt.  

> ##### Abbildung1  
> Ein Beispiel für ein ausgewähltes Element  
> ![Ein Beispiel für ein ausgewähltes Element][ImageSelectedElement]  

Es gibt viele Möglichkeiten zum Auswählen eines Elements:  

*   Klicken Sie im Viewport mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen**aus.  
*   Klicken Sie in devtools auf **Element auswählen** , ![ Wählen Sie ein Element aus, ][ImageSelectAnElementIcon] oder drücken Sie \ ( `Control` + `Shift` + `C` Windows \) oder `Command` + `Shift` + `C` \ (macOS \), und klicken Sie dann auf das Element im Viewport.  
*   Klicken Sie in devtools auf das Element in der **DOM-Struktur**.  
*   Führen Sie in devtools eine Abfrage wie `document.querySelector('p')` in der **Konsole**aus, klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie dann **im Dialogfeldelemente**anzeigen aus.  

## CSS anzeigen   

### Anzeigen des externen Stylesheets, in dem eine Regel definiert ist   

Klicken Sie im Bereich **Formatvorlagen** auf den Link neben einer CSS-Regel, um das externe Stylesheet zu öffnen, das die Regel definiert.  

Wenn das Stylesheet minimierte ist, lesen Sie [Erstellen einer minimierte-Datei][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Klicken Sie in [Abbildung 2](#figure-2) `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` auf die Zeile 2 von, in der `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` die `.content h1:first-of-type` CSS-Regel definiert ist.  

> ##### Abbildung2  
> Anzeigen des Stylesheets, in dem eine Regel definiert ist  
> ![Anzeigen des Stylesheets, in dem eine Regel definiert ist][ImageViewRuleStylesheet]  

### Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird   

Auf der Registerkarte **Formatvorlagen** werden alle Regeln angezeigt, die für ein Element gelten, einschließlich Deklarationen, die überschrieben wurden.  Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, verwenden Sie die Registerkarte **berechnet** , um nur das CSS anzuzeigen, das tatsächlich auf ein Element angewendet wird.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wechseln Sie im **Element** Fenster zur Registerkarte **berechnet** .  

> [!NOTE]
> In einem breiten devtools-Fenster ist die Registerkarte **berechnet** nicht vorhanden.  Der Inhalt der Registerkarte **berechnet** wird auf der Registerkarte **Formatvorlagen** angezeigt.  

Geerbte Eigenschaften sind nicht transparent.  Aktivieren Sie das Kontrollkästchen **Alle anzeigen** , um alle geerbten Werte anzuzeigen.  

> [!NOTE]
> In [Abbildung 3](#figure-3)werden auf der Registerkarte **berechnet** die CSS-Eigenschaften angezeigt, die auf das aktuell ausgewählte Element angewendet werden `h1` .  

> ##### Abbildung 3  
> Die Registerkarte " **berechnet** "  
> ![Die Registerkarte "berechnet"][ImageComputedTab]  

### Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge   

Verwenden Sie die Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.  

### Anzeigen von geerbten CSS-Eigenschaften   

Aktivieren Sie das Kontrollkästchen **Alle anzeigen** auf der Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.  

### Anzeigen des Box-Modells für ein Element   

Wenn Sie [das Feld Modell][MDNBoxModel] eines Elements anzeigen möchten, wechseln Sie zur Registerkarte **Formatvorlagen** .  Wenn Ihr devtools-Fenster schmal ist, befindet sich das **Feld Modell** Diagramm unten auf der Registerkarte.  

Um einen Wert zu ändern, doppelklicken Sie darauf.  

> [!NOTE]
> In [Abbildung 4](#figure-4)zeigt das **Diagramm auf** der Registerkarte **Formatvorlagen** das Feld Modell für das aktuell ausgewählte `h1` Element.  

> ##### Abbildung4  
> Das Diagramm des **Feld Modells**  
> ![Das Diagramm des Feld Modells][ImageBoxModel]  

### Suchen und Filtern des CSS eines Elements   

Verwenden Sie das Textfeld " **Filter** " auf den Registerkarten " **Formatvorlagen** " und " **berechnet** ", um nach bestimmten CSS-Eigenschaften oder-Werten zu suchen.  

Wenn Sie auch geerbte Eigenschaften auf der Registerkarte **berechnet** durchsuchen möchten, aktivieren Sie das Kontrollkästchen **Alle anzeigen** .  

> [!NOTE]
> In [Abbildung 5](#figure-5)wird die Registerkarte **Formatvorlagen** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage enthalten `color` .  

> ##### Abbildung5  
> Filtern der Registerkarte " **Formatvorlagen** "  
> ![Filtern der Registerkarte "Formatvorlagen"][ImageStylesFilter]  

> [!NOTE]
> In [Abbildung 6](#figure-6)wird die Registerkarte **berechnet** so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage enthalten `100%` .  

> ##### Abbildung6  
> Filtern der **berechneten** Registerkarte  
> ![Filtern der berechneten Registerkarte][ImageComputerFilter]  

### Umschalten einer Pseudoklasse   

So wechseln Sie eine Pseudoklasse wie `:active` , `:focus` , `:hover` oder `:visited` :  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wechseln Sie im **Element** Fenster zur Registerkarte **Formatvorlagen** .  
1.  Klicken Sie auf **: Hov**.  
1.  Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.  

> [!NOTE]
> Wechseln Sie in [Abbildung 7](#figure-7)zur `:hover` Pseudoklasse.  Überprüfen Sie im Viewport, ob die `background-color: cornflowerblue` Deklaration auf das Element angewendet wird, obwohl das Element nicht tatsächlich über den Zeiger bewegt wird.  

> ##### Abbildung7  
> Umschalten der `:hover` Pseudoklasse  
> ![Umschalten der: hover-Pseudoklasse][ImagePseudoClass]  

Weitere Informationen finden Sie unter [Hinzufügen eines PseudoState zu einer Klasse][DevToolsCSSGetStartedAddPseudoState] für ein interaktives Lernprogramm. 

### Anzeigen einer Seite im Druckmodus   

So zeigen Sie eine Seite im Druckmodus an:  

1.  [Öffnen des Befehlsmenüs][DevToolsCommandMenu]  
1.  Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .  
1.  Wählen Sie für die Dropdownliste **CSS-Medien emulieren** die Option **Drucken**aus.  

### Anzeigen der verwendeten und nicht verwendeten CSS mit der Registerkarte "Coverage"   

Auf der Registerkarte Coverage wird angezeigt, welche CSS-Seiten tatsächlich verwendet werden.  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), während sich devtools im Fokus befindet, um das Befehlsmenü zu öffnen.  
1.  Beginnen `coverage` Sie mit der Eingabe, und wählen Sie **Berichterstattung anzeigen**aus.  Die Registerkarte Coverage wird angezeigt.  
    
    > ##### Abbildung8  
    > Öffnen der Registerkarte "Abdeckung" über das Befehlsmenü  
    > ![Öffnen der Registerkarte "Abdeckung" über das Befehlsmenü][ImageCommandMenu]  
    
    > ##### Abbildung 9  
    > Die Registerkarte "Coverage"  
    > ![Die Registerkarte "Coverage"][ImageCoverageEmpty]  
    
1.  Klicken Sie auf **Instrumentations Abdeckung starten, und aktualisieren Sie die Abdeckung für die Seiten** ![ Anfang Instrumentation, und aktualisieren Sie die Seite ][ImageRefreshIcon] .  Die Seite wird aktualisiert, und die Registerkarte Coverage bietet eine Übersicht darüber, wie viel CSS \ (und JavaScript \) aus jeder Datei, die der Browser lädt, verwendet wird.  Grün steht für verwendetes CSS.  Rot steht für nicht verwendetes CSS.  
    
    > ##### Abbildung 10  
    > Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird  
    > ![Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird][ImageCoverageOverview]  

1.  Klicken Sie auf eine CSS-Datei, um eine Zeile für Zeile zu sehen, welche CSS-Datei verwendet wird.  
    
    > [!NOTE]
    > In [Abbildung 11](#figure-11)werden die Zeilen 145 bis 147 und 149 bis 151 nicht `b66bc881.site-ltr.css` verwendet, während Zeilen 163 bis 166 verwendet werden.  
    
    > ##### Abbildung 11  
    > Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS  
    > ![Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS][ImageCoverageDetail]  
    
### Erzwingen des Druckvorschau Modus   

Siehe [Erzwingen von devtools in den Druckvorschau Modus][DevToolsCssPrintPreview].  

## CSS ändern   

<!-- todo s/CSS declaration/declaration/ -->  

### Hinzufügen einer CSS-Deklaration zu einem Element   

Da die Reihenfolge der Deklarationen beeinflusst, wie ein Element formatiert wird, können Sie Deklarationen auf unterschiedliche Weise hinzufügen:  

*   [Fügen Sie eine Inline Deklaration hinzu](#add-an-inline-declaration).  Entspricht dem Hinzufügen eines `style` Attributs zum HTML-Code eines Elements.  
*   [Hinzufügen einer Deklaration zu einer Formatvorlagenregel](#add-a-declaration-to-a-style-rule)  

**Welchen Workflow sollten Sie verwenden?** In den meisten Fällen möchten Sie wahrscheinlich den Inline Deklarations Workflow verwenden.  Inline Deklarationen haben eine höhere Spezifität als externe, sodass der Inline-Workflow sicherstellt, dass die Änderungen in dem Element wie erwartet wirksam werden.  Weitere Informationen zur Spezifität finden Sie unter [Selektor-Typen][MDNSelectorTypes] .  

Wenn Sie alle Formatvorlagen des Elements Debuggen und insbesondere testen möchten, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.  

#### Hinzufügen einer Inline Deklaration   

So fügen Sie eine Inline Deklaration hinzu:  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Klicken Sie im Bereich " **Formatvorlagen** " zwischen den Klammern des Abschnitts " **Element. Format** ".  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftsnamen ein, und drücken Sie `Enter` .  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und drücken Sie `Enter` .  Überprüfen Sie in der **DOM-Struktur**, ob `style` dem Element ein Attribut hinzugefügt wurde.  

> [!NOTE]
> In [Abbildung 12](#figure-12)wurden die `margin-top` `background-color` Eigenschaften und auf das ausgewählte Element angewendet.  Überprüfen Sie in der **DOM-Struktur** , ob die Deklarationen im `style` Attribut für ein Element widergespiegelt werden.  

> ##### Abbildung 12  
> Hinzufügen von Inline Deklarationen  
> ![Hinzufügen von Inline Deklarationen][ImageInlineDeclarations]  

#### Hinzufügen einer Deklaration zu einer Stilregel   

So fügen Sie einer vorhandenen Stilregel eine Deklaration hinzu:  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Klicken Sie im Bereich **Formatvorlagen** auf die eckigen Klammern der Stilregel, der Sie die Deklaration hinzufügen möchten.  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftsnamen ein, und drücken Sie `Enter` .  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und drücken Sie `Enter` .  

> ##### Abbildung 13  
> Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Stilregel  
> ![Hinzufügen einer Deklaration zu einer Formatvorlagenregel][ImageAddDeclarationExistingRule]  

### Ändern des Namens oder Werts einer Deklaration   

Doppelklicken Sie auf den Namen oder Wert einer Deklaration, um Sie zu ändern.  Informationen dazu finden Sie unter [Ändern von Deklarations Werten mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts) für Tastenkombinationen, um einen Wert schnell zu erhöhen oder zu verringern `0.1` `1` `10` `100` .  

> ##### Abbildung 14  
> Ändern des Werts der `border-bottom-style`  
> ![Ändern des Werts einer Deklaration][ImageAddDeclarationExistingRule2]  

### Ändern von Deklarations Werten mit Tastenkombinationen   

Wenn Sie den Wert einer Deklaration bearbeiten, können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen festen Betrag zu erhöhen:  

*   Drücken Sie `Alt` + `Up` \ (Windows \) oder `Option` + `Up` \ (macOS \), um den Wert zu erhöhen `0.1` .  
*   Drücken Sie, `Up` um den Wert nach `1` oder nach zu ändern, `0.1` Wenn der aktuelle Wert zwischen `-1` und ist `1` .  
*   Drücken Sie `Shift` + `Up` , um den Wert zu erhöhen `10` .  
*   Drücken Sie `Shift` + `Page Up` \ (Windows \) oder `Shift` + `Command` + `Up` \ (macOS \), um den Wert um zu erhöhen `100` .  

Das Dekrementieren funktioniert auch.  Ersetzen Sie einfach alle `Up` oben genannten Instanzen durch `Down` .  

### Hinzufügen einer Klasse zu einem Element   

So fügen Sie einem Element eine Klasse hinzu:  

1.  [Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.  
1.  Klicken Sie auf **. CLS**.  
1.  Geben Sie den Namen der Klasse in das Textfeld **neue Klasse hinzufügen** ein.  
1.  Drücken Sie `Enter` .  

> ##### Abbildung 15  
> Der Bereich " **Element Klassen** "  
> ![Der Bereich "Element Klassen"][ImageElementClasses]  

### Umschalten einer Klasse   

So aktivieren oder deaktivieren Sie eine Klasse für ein Element:  

1.  [Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.  
1.  Öffnen Sie den Bereich **Element Klassen** .  Weitere Informationen finden Sie unter [Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).  Unter dem Textfeld " **neue Klasse hinzufügen** " befinden sich alle Klassen, die auf dieses Element angewendet werden.  
1.  Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.  

### Hinzufügen einer Stilregel   

So fügen Sie eine neue Stilregel hinzu:  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Klicken Sie auf **neue** Stilregel Regel ![ ][ImageNewStyleRuleIcon] .  DevTools fügt eine neue Regel unterhalb der **Element. Style** -Regel ein.  

> [!NOTE]
> In [Abbildung 16](#figure-16)fügt devtools die Stilregel hinzu, `h1.devsite-page-title` nachdem Sie **auf neue Stilregel**geklickt haben.  

> ##### Abbildung 16  
> Hinzufügen einer neuen Stilregel  
> ![Hinzufügen einer neuen Stilregel][ImageStyleRule]  

#### Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll   

Wenn Sie [eine neue Stilregel hinzufügen](#add-a-style-rule), klicken und **halten Sie** die neue Stilregel Regel neu, um ![ auszuwählen, ][ImageNewStyleRuleIcon] welchem Stylesheet die Stilregel hinzugefügt werden soll.  

> ##### Abbildung 17  
> Auswählen eines Stylesheets  
> ![Auswählen eines Stylesheets][ImageChooseStylesheet]  

#### Hinzufügen einer Stilregel zu einem bestimmten Speicherort   

So fügen Sie auf der Registerkarte **Formatvorlagen** eine Stilregel zu einer bestimmten Position hinzu:  

1.  Zeigen Sie mit der Maus auf die Stilregel, die sich direkt darüber befindet, wo Sie die neue Stilregel hinzufügen möchten.  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Klicken Sie unter Formatvorlagenregel einfügen auf **Stil Regel einfügen** ![ ][ImageNewStyleRuleIcon] .  

> ##### Abbildung 18  
> **Einfügen einer Stilregel unten**  
> ![Einfügen einer Stilregel unten][ImageInsertStyleRuleBelow]  

### Anzeigen der Symbolleiste "Weitere Aktionen"   

Auf der Symbolleiste **Weitere Aktionen** können Sie Folgendes ausführen:  

*   Fügen Sie eine Stilregel direkt unter die Regel ein, auf die Sie sich konzentrieren möchten.  
*   Fügen `background-color` `color` `box-shadow` `text-shadow` Sie der Stilregel, auf die Sie sich konzentrieren, eine,-oder-Deklaration hinzu.  

So zeigen Sie die Symbolleiste " **Weitere Aktionen** " an:  

1.  Zeigen Sie auf der Registerkarte **Formatvorlagen** auf eine Stilregel.  **Weitere Aktionen** `...` wird in der unteren rechten Ecke des Abschnitts Stilregel angezeigt.  
    
    > [!NOTE]
    > Zeigen Sie in [Abbildung 19](#figure-19)auf die `.header-holder.has-default-focus` Stilregel, und klicken Sie unten rechts im Abschnitt Stilregel auf **Weitere Aktionen** .  
    
    > ##### Abbildung 19  
    > Aufdecken **weiterer Aktionen**  
    > ![Aufdecken weiterer Aktionen][ImageRevealMore]  
    
1.  Zeigen Sie auf **Weitere Aktionen** `...` , um die oben genannten Aktionen anzuzeigen.  
    
    > [!NOTE]
    > Die **Regel "Stil einfügen" unterhalb** der Aktion wird nach dem Hovern auf **Weitere Aktionen**angezeigt.  
    
    > ##### Abbildung 20  
    > Die Symbolleiste " **Weitere Aktionen** "  
    > ![Die Symbolleiste "Weitere Aktionen"][ImageInsertStyleRuleBelow2]  
    
### Umschalten einer Deklaration   

So aktivieren oder deaktivieren Sie eine einzelne Deklaration:  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Zeigen Sie im Bereich **Formatvorlagen** auf die Regel, die die Deklaration definiert.  Kontrollkästchen werden neben jeder Deklaration angezeigt.  
1.  Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Deklaration.  Wenn Sie eine Deklaration deaktivieren, wird Sie von devtools durchgestrichen, um anzugeben, dass Sie nicht mehr aktiv ist.  

> [!NOTE]
> In [Abbildung 21](#figure-21)wurde die `margin-top` Eigenschaft für das aktuell ausgewählte Element deaktiviert.  

> ##### Abbildung 21  
> Umschalten einer Deklaration  
> ![Umschalten einer Deklaration][ImageToggleDeclaration]  

### Hinzufügen einer Hintergrundfarben Deklaration   

So fügen Sie einem `background-color` Element eine Deklaration hinzu:  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `background-color` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Klicken Sie auf **Hintergrundfarbe hinzu** fügen ![ , um Hintergrundfarbe hinzuzufügen ][ImageAddBackgroundColorIcon] .  

> ##### Abbildung 22  
> **Hinzufügen einer Hintergrundfarbe**  
> ![Hinzufügen einer Hintergrundfarbe][ImageAddBackgroundColor]  

### Hinzufügen einer Farb Deklaration   

So fügen Sie einem `color` Element eine Deklaration hinzu:  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `color` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Klicken Sie auf **Farbe** hinzufügen ![ ][ImageAddColorIcon] .  

> ##### Abbildung 23  
> **Farbe hinzufügen**  
> ![Farbe hinzufügen][ImageAddColor]  

### Hinzufügen einer Box-Shadow-Deklaration   

So fügen Sie einem `box-shadow` Element eine Deklaration hinzu:  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `box-shadow` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Klicken Sie auf **Feld** Schatten hinzufügen ![ ][ImageAddBoxShadowIcon] .  

> ##### Abbildung 24  
> **Feld Schatten hinzufügen**  
> ![Feld Schatten hinzufügen][ImageAddBoxShadow]  

### Hinzufügen einer Text-Shadow-Deklaration   

So fügen Sie einem `text-shadow` Element eine Deklaration hinzu:  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `text-shadow` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Klicken Sie auf **Text** Schatten hinzufügen ![ , um Text Schatten hinzuzufügen ][ImageAddTextShadowIcon] .  

> ##### Abbildung 25  
> **Hinzufügen von Text Schatten**  
> ![Hinzufügen von Text Schatten][ImageAddTextShadow]  

### Ändern von Farben mit der Farbauswahl   

Die **Farbauswahl** bietet eine GUI für Änderungen `color` und `background-color` Deklarationen.  

So öffnen Sie die **Farbauswahl**:  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Suchen Sie auf der Registerkarte **Formatvorlagen** nach der `color` `background-color` oder ähnlichen Deklaration, die Sie ändern möchten.  Links vom `color` `background-color` oder ähnlichen Wert befindet sich ein kleines Quadrat, das eine Vorschau der Farbe ist.  
    
    > [!NOTE]
    > In [Abbildung 26](#figure-26)ist das kleine Quadrat links von `rgba(0, 0, 0, 0.7)` einer Vorschau dieser Farbe.  
    
    > ##### Abbildung 26  
    > Farbvorschau  
    > ![Farbvorschau][ImageColorPreview]  
    
1.  Klicken Sie auf die Vorschau, um die **Farbauswahl**zu öffnen.  
    
    > ##### Abbildung 27  
    > Die **Farbauswahl**  
    > ![Die Farbauswahl][ImageColorPicker]  
    
Nachfolgend finden Sie eine Beschreibung der einzelnen UI-Elemente der **Farbauswahl**:  

> ##### Abbildung 28  
> Die Farbauswahl mit Anmerkungen  
> ![Die Farbauswahl mit Anmerkungen][ImageColorPickerAnnotated]  

1.  **Schattierungen**.  
1.  **Pipette**.  Sehen Sie sich das [Beispiel einer Farbe auf der Seite mit der Pipette an](#sample-a-color-off-the-page-with-the-eyedropper).  
1.  **In die Zwischenablage kopieren**  Kopieren Sie den **Anzeigewert** in Ihre Zwischenablage.  
1.  **Anzeigewert**.  Die RGBA-, HSLA-oder Hex-Darstellung der Farbe.  
1.  **Farb Palette**  Klicken Sie auf eines dieser Quadrate, um die Farbe in das Quadrat zu ändern.  
1.  **Farbton**aus.  
1.  **Deckkraft**.  
1.  **Anzeigen des Wert Umschalters**  Wechseln zwischen den RGBA-, HSLA-und Hex-Darstellungen der aktuellen Farbe  
1.  **Farbpaletten-Switcher**  Wechseln zwischen der [Material Design Palette][MaterialDesignColorSystem], einer benutzerdefinierten Palette oder einer Seitenfarben-Palette  DevTools generiert die Seiten Farbpalette basierend auf den Farben, die in ihren Stylesheets gefunden werden.  

#### Beispiel für eine Farbe auf der Seite mit der Pipette   

Wenn Sie die **Farbauswahl**öffnen, ist **die Pipette** ![ ][ImageEyedropperIcon] standardmäßig aktiviert.  So ändern Sie die ausgewählte Farbe auf eine andere Farbe auf der Seite:  

1.  Zeigen Sie mit der Maus auf die Zielfarbe im Viewport.  
1.  Klicken Sie, um zu bestätigen.  
    
    > [!NOTE]
    > In [Abbildung 29](#figure-29)zeigt die **Farbauswahl** einen aktuellen Farbwert von, der sich in der `rgba(0,0,0,0.7)` Nähe von schwarz befindet.  Diese Farbe sollte auf das Schwarz geändert werden, das aktuell im Viewport hervorgehoben ist, nachdem auf das schwarze geklickt wurde.  
    
    > ##### Abbildung 29  
    > Verwenden der Pipette  
    > ![Verwenden der Pipette][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Abbildung 1: ein Beispiel für ein ausgewähltes Element"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Abbildung 2: Anzeigen des Stylesheets, in dem eine Regel definiert ist"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Abbildung 3: die Registerkarte "berechnet""  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Abbildung 4: das Diagramm des Feld Modells"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Abbildung 5: Filtern der Registerkarte "Formatvorlagen""  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Abbildung 6: Filtern der berechneten Registerkarte"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Abbildung 7: Umschalten der: hover-Pseudoklasse"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Abbildung 8: Öffnen der Registerkarte Coverage über das Befehlsmenü"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Abbildung 9: Registerkarte "Coverage""  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Abbildung 10: eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Abbildung 11: eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Abbildung 12: Hinzufügen von Inline Deklarationen"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Abbildung 13: Hinzufügen einer Deklaration zu einer Formatvorlagenregel"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Abbildung 14: Ändern des Werts einer Deklaration"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Abbildung 15: Bereich "Element Klassen""  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Abbildung 16: Hinzufügen einer neuen Stilregel"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Abbildung 17: Auswählen eines Stylesheets"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Abbildung 18: Einfügen einer Stilregel nach unten"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Abbildung 19: aufdecken weiterer Aktionen"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Abbildung 20: die Symbolleiste "Weitere Aktionen""  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Abbildung 21: Umschalten einer Deklaration"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Abbildung 22: Hinzufügen einer Hintergrundfarbe"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Abbildung 23: Hinzufügen von Farben"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Abbildung 24: Hinzufügen eines Feld Schattens"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Abbildung 25: Hinzufügen von Text Schatten"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Abbildung 26: Farbvorschau"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Abbildung 27: die Farbauswahl"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Abbildung 28: die Farbauswahl mit Anmerkungen"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Abbildung 29: Verwenden der Pipette"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte beim Anzeigen und Ändern von CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Hinzufügen eines PseudoState zu einer Klasse – erste Schritte mit dem anzeigen und Ändern von CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Anzeigen der CSS für ein Element – erste Schritte mit dem anzeigen und Ändern von CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Erstellen einer minimierte-Datei lesbar-JavaScript-Debug-Referenz"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Das Farbsystem – Material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Das Feld Modell | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Auswahltypen – Spezifität | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
