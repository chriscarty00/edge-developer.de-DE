---
description: Entdecken Sie neue Workflows zum Anzeigen und Ändern von CSS in Microsoft Edge devtools.
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: de0fb33e1e080045383f3c0fb50919297cbff5bc
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993072"
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

Entdecken Sie neue Workflows in der folgenden umfassenden Referenz zu den Microsoft Edge devtools-Features, die sich auf das Anzeigen und Ändern von CSS beziehen.  

Informationen zu den Grundlagen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCSSGetStarted] .  

## Auswählen eines Elements  

Mit dem Element Panel von devtools können **Sie das CSS** eines Elements gleichzeitig anzeigen oder ändern.  Das ausgewählte Element ist in der **DOM-Struktur**hervorgehoben.  Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.  Weitere Informationen finden Sie unter [Anzeigen des CSS für ein Element][DevToolsCSSGetStartedTutorial] für ein Lernprogramm.  

> [!NOTE]
> In der folgenden Abbildung ist das `h1` in der **DOM-Struktur** hervorgehobene Element das ausgewählte Element.  Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.  Auf der linken Seite ist das Element im Viewport hervorgehoben, allerdings nur, weil die Maus gerade in der DOM- **Struktur**darüber schwebt.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1.msft.png":::
   Ein Beispiel für ein ausgewähltes Element  
:::image-end:::  

Verwenden Sie eine der folgenden Aktionen, um ein Element auszuwählen.  

*   Zeigen Sie im Viewport auf das Element, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
*   Wählen Sie in devtools **Element auswählen** \ ( ![ Element auswählen ][ImageSelectAnElementIcon] \) aus, oder wählen Sie `Control` + `Shift` + `C` \ (Windows \) oder `Command` + `Shift` + `C` \ (macOS \) aus, und wählen Sie dann das Element im Viewport aus.  
*   Wählen Sie in devtools das Element in der **DOM-Struktur**aus.  
*   Führen Sie in devtools eine Abfrage wie `document.querySelector('p')` in der **Konsole**aus, zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **im Dialogfeldelemente**anzeigen aus.  

## CSS anzeigen  

### Anzeigen des externen Stylesheets, in dem eine Regel definiert ist  

Wählen Sie im Bereich **Formatvorlagen** den Link neben einer CSS-Regel aus, um das externe Stylesheet zu öffnen, das die Regel definiert.  

Wenn das Stylesheet minimierte ist, lesen Sie [Erstellen einer minimierte-Datei][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> In der folgenden Abbildung werden Sie nach der Auswahl `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` an Zeile 2 von `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , in der die `.content h1:first-of-type` CSS-Regel definiert ist, weitergeleitet.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Anzeigen des Stylesheets, in dem eine Regel definiert ist  
:::image-end:::  

### Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird  

Auf der Registerkarte **Formatvorlagen** werden alle Regeln angezeigt, die für ein Element gelten, einschließlich Deklarationen, die überschrieben wurden.  Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, verwenden Sie die Registerkarte **berechnet** , um nur das CSS anzuzeigen, das tatsächlich auf ein Element angewendet wird.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wechseln Sie im **Element** Fenster zur Registerkarte **berechnet** .  

> [!NOTE]
> In einem breiten devtools-Fenster ist die Registerkarte **berechnet** nicht vorhanden.  Der Inhalt der Registerkarte **berechnet** wird auf der Registerkarte **Formatvorlagen** angezeigt.  

Geerbte Eigenschaften sind nicht transparent.  Aktivieren Sie das Kontrollkästchen **Alle anzeigen** , um alle geerbten Werte anzuzeigen.  

> [!NOTE]
> In der folgenden Abbildung werden auf der Registerkarte **berechnet** die CSS-Eigenschaften angezeigt, die auf das aktuell ausgewählte Element angewendet werden `h1` .  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-computed-h1.msft.png":::
   Die Registerkarte " **berechnet** "  
:::image-end:::  

### Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge  

Verwenden Sie die Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.  

### Anzeigen von geerbten CSS-Eigenschaften  

Aktivieren Sie das Kontrollkästchen **Alle anzeigen** auf der Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.  

### Anzeigen des Box-Modells für ein Element  

Wenn Sie [das Feld Modell][MDNBoxModel] eines Elements anzeigen möchten, wechseln Sie zur Registerkarte **Formatvorlagen** .  Wenn Ihr devtools-Fenster schmal ist, befindet sich das **Feld Modell** Diagramm unten auf der Registerkarte.  

Wählen Sie einen Wert aus, und bearbeiten Sie ihn, um einen Wert zu ändern.  

> [!NOTE]
> In der folgenden Abbildung wird im **Feld Modell** Diagramm auf der Registerkarte **Formatvorlagen** das Feld Modell für das aktuell ausgewählte `h1` Element angezeigt.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Das Diagramm des **Feld Modells**  
:::image-end:::  

### Suchen und Filtern des CSS eines Elements  

Verwenden Sie das Textfeld " **Filter** " auf den Registerkarten " **Formatvorlagen** " und " **berechnet** ", um nach bestimmten CSS-Eigenschaften oder-Werten zu suchen.  

Wenn Sie auch geerbte Eigenschaften auf der Registerkarte **berechnet** durchsuchen möchten, aktivieren Sie das Kontrollkästchen **Alle anzeigen** .  

> [!NOTE]
> In der folgenden Abbildung wird die Registerkarte **Formatvorlagen** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage enthalten `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtern der Registerkarte " **Formatvorlagen** "  
:::image-end:::  

> [!NOTE]
> In der folgenden Abbildung wird die Registerkarte **berechnet** so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage enthalten `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtern der **berechneten** Registerkarte  
:::image-end:::  

### Umschalten einer Pseudoklasse  

Führen Sie die folgenden Aktionen aus, um eine Pseudoklasse wie, `:active` `:focus` , oder zu wechseln `:hover` `:visited` .  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wechseln Sie im **Element** Fenster zur Registerkarte **Formatvorlagen** .  
1.  Wählen Sie **: Hov**aus.  
1.  Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.  

> [!NOTE]
> Wechseln Sie in der folgenden Abbildung zur `:hover` Pseudoklasse.  Überprüfen Sie im Viewport, ob die `background-color: cornflowerblue` Deklaration auf das Element angewendet wird, obwohl das Element nicht tatsächlich über den Zeiger bewegt wird.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Umschalten der `:hover` Pseudoklasse  
:::image-end:::  

Ein interaktives Lernprogramm finden Sie unter [Hinzufügen eines PseudoState zu einer Klasse][DevToolsCSSGetStartedAddPseudoState].  

### Anzeigen einer Seite im Druckmodus  

Führen Sie die folgenden Aktionen aus, um eine Seite im Druckmodus anzuzeigen.  

1.  [Öffnen des Befehlsmenüs][DevToolsCommandMenu]  
1.  Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .  
1.  Wählen Sie für die Dropdownliste **CSS-Medien emulieren** die Option **Drucken**aus.  

### Anzeigen der verwendeten und nicht verwendeten CSS mit der Registerkarte "Coverage"  

Auf der Registerkarte Coverage wird angezeigt, welche CSS-Seiten tatsächlich verwendet werden.  

1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, während sich devtools im Fokus befindet, um [das Befehlsmenü zu öffnen][DevToolsCommandMenu].  
1.  Beginnen `coverage` Sie mit der Eingabe, und wählen Sie **Berichterstattung anzeigen**aus.  Die Registerkarte Coverage wird angezeigt.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Öffnen der Registerkarte " **Abdeckung** " über das **Befehlsmenü**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             Die Registerkarte " **Coverage** "  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen Sie **Instrumentations Abdeckung starten und aktualisieren Sie die Seite** aus, und aktualisieren Sie die Seite ![ mit der Instrumentations Abdeckung und aktualisieren Sie die Seite ][ImageRefreshIcon] .  Die Seite wird aktualisiert, und die Registerkarte Coverage bietet eine Übersicht darüber, wie viel CSS \ (und JavaScript \) aus jeder Datei, die der Browser lädt, verwendet wird.  Grün steht für verwendetes CSS.  Rot steht für nicht verwendetes CSS.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Eine Übersicht darüber, wie viel CSS \ (und JavaScript \) verwendet und nicht verwendet wird  
    :::image-end:::  

1.  Wählen Sie eine CSS-Datei aus, um eine Zeile für Zeile aufzuschlüsseln, was CSS verwendet.  
    
    > [!NOTE]
    > In der folgenden Abbildung werden die Zeilen 145 bis 147 und 149 bis 151 nicht `b66bc881.site-ltr.css` verwendet, während Zeilen 163 bis 166 verwendet werden.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-sources-css-coverage.msft.png":::
       Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS  
    :::image-end:::  
    
### Erzwingen des Druckvorschau Modus  

Siehe [Erzwingen von devtools in den Druckvorschau Modus][DevToolsCssPrintPreview].  

## CSS ändern  

<!-- todo s/CSS declaration/declaration/ -->  

### Hinzufügen einer CSS-Deklaration zu einem Element  

Die Reihenfolge der Deklarationen wirkt sich darauf aus, wie ein Element formatiert wird, indem Sie die folgende Liste verwenden, um Deklarationen auf unterschiedliche Weise hinzuzufügen.  

*   [Fügen Sie eine Inline Deklaration hinzu](#add-an-inline-declaration).  Entspricht dem Hinzufügen eines `style` Attributs zum HTML-Code eines Elements.  
*   [Hinzufügen einer Deklaration zu einer Formatvorlagenregel](#add-a-declaration-to-a-style-rule)  

**Welchen Workflow sollten Sie verwenden?** In den meisten Fällen möchten Sie wahrscheinlich den Inline Deklarations Workflow verwenden.  Inline Deklarationen haben eine höhere Spezifität als externe, sodass der Inline-Workflow sicherstellt, dass die Änderungen in Ihrem erwarteten Element wirksam werden.  Weitere Informationen zur Spezifität finden Sie unter [Selector-Typen][MDNSelectorTypes].  

Wenn Sie alle Formatvorlagen des Elements Debuggen und insbesondere testen möchten, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.  

#### Hinzufügen einer Inline Deklaration  

Führen Sie die folgenden Aktionen aus, um eine Inline Deklaration hinzuzufügen.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wählen Sie im Bereich **Formatvorlagen** zwischen den Klammern des Abschnitts **Element. Format** aus.  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftsnamen ein, und wählen Sie aus `Enter` .  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie aus `Enter` .  Überprüfen Sie in der **DOM-Struktur**, ob `style` dem Element ein Attribut hinzugefügt wurde.  

> [!NOTE]
> In der folgenden Abbildung wurden die `margin-top` `background-color` Eigenschaften und auf das ausgewählte Element angewendet.  Überprüfen Sie in der **DOM-Struktur** , ob die Deklarationen im `style` Attribut für ein Element widergespiegelt werden.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Hinzufügen von Inline Deklarationen  
:::image-end:::  

#### Hinzufügen einer Deklaration zu einer Stilregel  

Führen Sie die folgenden Aktionen aus, um eine Deklaration zu einer vorhandenen Stilregel hinzuzufügen.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wählen Sie im Bereich **Formatvorlagen** zwischen den Klammern der Stilregel aus, der Sie die Deklaration hinzufügen möchten.  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftsnamen ein, und wählen Sie aus `Enter` .  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie aus `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Stilregel  
:::image-end:::  

### Ändern des Namens oder Werts einer Deklaration  

Wählen Sie den Namen oder den Wert einer Deklaration aus, und bearbeiten Sie ihn, um ihn zu ändern.  Informationen dazu finden Sie unter [Ändern von Deklarations Werten mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts) für Tastenkombinationen, um einen Wert schnell zu erhöhen oder zu verringern `0.1` `1` `10` `100` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Ändern des Werts der `border-bottom-style` Deklaration  
:::image-end:::  

### Ändern von Deklarations Werten mit Tastenkombinationen  

Wenn Sie den Wert einer Deklaration bearbeiten, können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen bestimmten Betrag zu erhöhen.  

*   Wählen Sie `Alt` + `Up` \ (Windows \) oder `Option` + `Up` \ (macOS \) aus, um den Wert zu erhöhen `0.1` .  
*   Wählen Sie aus, `Up` um den Wert nach `1` oder nach zu ändern, `0.1` Wenn der aktuelle Wert zwischen `-1` und ist `1` .  
*   Wählen Sie aus `Shift` + `Up` , um zu inkrementieren `10` .  
*   Wählen Sie `Shift` + `Page Up` \ (Windows \) oder `Shift` + `Command` + `Up` \ (macOS \) aus, um den Wert zu erhöhen `100` .  

Das Dekrementieren funktioniert auch.  Ersetzen Sie einfach alle `Up` oben genannten Instanzen durch `Down` .  

### Hinzufügen einer Klasse zu einem Element  

Führen Sie die folgenden Aktionen aus, um einem Element eine Klasse hinzuzufügen.  

1.  [Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.  
1.  Wählen Sie **CLS**aus.  
1.  Geben Sie den Namen der Klasse in das Textfeld **neue Klasse hinzufügen** ein.  
1.  Wählen Sie aus `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Der Bereich " **Element Klassen** "  
:::image-end:::  

### Umschalten einer Klasse  

Führen Sie die folgenden Aktionen aus, um eine Klasse für ein Element zu aktivieren oder zu deaktivieren.  

1.  [Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.  
1.  Öffnen Sie den Bereich **Element Klassen** .  Weitere Informationen finden Sie unter [Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).  Unter dem Textfeld " **neue Klasse hinzufügen** " befinden sich alle Klassen, die auf das jeweilige Element angewendet werden.  
1.  Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.  

### Hinzufügen einer Stilregel  

Führen Sie die folgenden Aktionen aus, um eine neue Stilregel hinzuzufügen.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Wählen Sie **neue Formatvorlagenregel** \ ( ![ neue Stilregel ][ImageNewStyleRuleIcon] \) aus.  DevTools fügt eine neue Regel unterhalb der **Element. Style** -Regel ein.  

> [!NOTE]
> In der folgenden Abbildung fügt devtools die Stilregel hinzu, `h1.devsite-page-title` nachdem Sie eine **neue Stilregel**ausgewählt haben.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Hinzufügen einer neuen Stilregel  
:::image-end:::  

#### Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll  

Wenn Sie [eine neue Stilregel hinzufügen](#add-a-style-rule)möchten, wählen Sie **neue** Stilregel aus, und halten Sie die Regel \ (neue Stilregel \) gedrückt, um ![ auszuwählen, ][ImageNewStyleRuleIcon] welchem Stylesheet die Stilregel hinzugefügt werden soll.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Auswählen eines Stylesheets  
:::image-end:::  

#### Hinzufügen einer Stilregel zu einem bestimmten Speicherort  

Führen Sie die folgenden Aktionen aus, um einer bestimmten Position auf der Registerkarte **Formatvorlagen** eine Stilregel hinzuzufügen.  

1.  Zeigen Sie mit der Maus auf die Stilregel, die sich direkt darüber befindet, wo Sie die neue Stilregel hinzufügen möchten.  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Wählen Sie **unter** \ (Stilregel ![ Einfügen unter \) die Option Stilregel einfügen aus ][ImageNewStyleRuleIcon] .  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Einfügen einer Stilregel unten**  
:::image-end:::  

### Anzeigen der Symbolleiste "Weitere Aktionen"  

Auf der Symbolleiste **Weitere Aktionen** können Sie die folgenden Aktionen ausführen:  

*   Fügen Sie eine Stilregel direkt unter die Regel ein, auf die Sie sich konzentrieren möchten.  
*   Fügen `background-color` `color` `box-shadow` `text-shadow` Sie der Stilregel, auf die Sie sich konzentrieren, eine,-oder-Deklaration hinzu.  

Führen Sie die folgenden Aktionen aus, um die Symbolleiste **Weitere Aktionen** anzuzeigen.  

1.  Zeigen Sie auf der Registerkarte **Formatvorlagen** auf eine Stilregel.  **More Actions** `...` In der unteren rechten Ecke des Abschnitts Stilregel werden weitere Aktionen angezeigt.  
    
    > [!NOTE]
    > Zeigen Sie in der folgenden Abbildung auf die `.header-holder.has-default-focus` Stilregel, und **Weitere Aktionen** werden in der unteren rechten Ecke des Abschnitts Stilregel eingeblendet.  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       **Weitere Aktionen** anzeigen \ ( `...` \)  
    :::image-end:::  
    
1.  Zeigen Sie auf **Weitere Aktionen** \ ( `...` \), um die oben genannten Aktionen anzuzeigen.  
    
    > [!NOTE]
    > Die **Regel "Stil einfügen" unterhalb** der Aktion wird nach dem Hovern auf **Weitere Aktionen**angezeigt.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Die Symbolleiste " **Weitere Aktionen** "  
    :::image-end:::  
    
### Umschalten einer Deklaration  

Führen Sie die folllwoing-Aktionen aus, um eine einzelne Deklaration auf \ (oder aus \) umzuschalten.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Zeigen Sie im Bereich **Formatvorlagen** auf die Regel, die die Deklaration definiert.  Neben jeder Deklaration wird ein Kontrollkästchen angezeigt.  
1.  Aktivieren Sie das Kontrollkästchen neben der Deklaration.  Wenn Sie eine Deklaration deaktivieren, wird Sie von devtools durchgestrichen, um anzugeben, dass Sie nicht mehr aktiv ist.  

> [!NOTE]
> In der folgenden Abbildung wurde die `margin-top` Eigenschaft für das aktuell ausgewählte Element deaktiviert.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Umschalten einer Deklaration  
:::image-end:::  

### Hinzufügen einer Hintergrundfarben Deklaration  

Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `background-color` .  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `background-color` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Wählen Sie **Hintergrundfarbe hinzufügen** \ ( ![ Hintergrundfarbe hinzufügen ][ImageAddBackgroundColorIcon] \) aus.  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Hinzufügen einer Hintergrundfarbe**  
:::image-end:::  

### Hinzufügen einer Farb Deklaration  

Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `color` .  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `color` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Wählen Sie **Farbe hinzufügen** ( ![ Farbe hinzufügen ][ImageAddColorIcon] ) aus.  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Farbe hinzufügen**  
:::image-end:::  

### Hinzufügen einer Box-Shadow-Deklaration  

Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `box-shadow` .  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `box-shadow` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Wählen Sie " **Feld Schatten hinzufügen** " aus ![ ][ImageAddBoxShadowIcon] .  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Feld Schatten hinzufügen**  
:::image-end:::  

### Hinzufügen einer Text-Shadow-Deklaration  

Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `text-shadow` .  

1.  Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `text-shadow` .  
1.  [Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).  
1.  Wählen Sie **Text Schatten hinzufügen** \ ( ![ Text Schatten hinzufügen ][ImageAddTextShadowIcon] ) aus.  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Hinzufügen von Text Schatten**  
:::image-end:::  

### Ändern von Farben mit der Farbauswahl  

Die **Farbauswahl** bietet eine GUI für Änderungen `color` und `background-color` Deklarationen.  

Führen Sie die folgenden Aktionen aus, um die **Farbauswahl**zu öffnen.  

1.  [Wählen Sie ein Element aus](#select-an-element).  
1.  Suchen Sie auf der Registerkarte **Formatvorlagen** nach der `color` `background-color` oder ähnlichen Deklaration, die Sie ändern möchten.  Links vom `color` `background-color` oder ähnlichen Wert befindet sich ein kleines Quadrat, das eine Vorschau der Farbe ist.  
    
    > [!NOTE]
    > In der folgenden Abbildung ist das kleine Quadrat links von `rgba(0, 0, 0, 0.7)` einer Vorschau dieser Farbe.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Farbvorschau  
    :::image-end:::  
    
1.  Wählen Sie die Vorschau aus, um die **Farbauswahl**zu öffnen.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       Die **Farbauswahl**  
    :::image-end:::  
    
Die folgende Abbildung und Listen beschreibt der einzelnen UI-Elemente der **Farbauswahl**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   Die **Farbauswahl**mit Anmerkungen  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Schattierungen**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Pipette**  
   :::column-end:::
   :::column span="2":::
      Weitere Informationen finden Sie unter [Beispiel für eine Farbe außerhalb der Seite mit der Pipette](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3  
   :::column-end:::
   :::column span="1":::
      **In Zwischenablage kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie den **Anzeigewert** in Ihre Zwischenablage.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4  
   :::column-end:::
   :::column span="1":::
      **Anzeigewert**  
   :::column-end:::
   :::column span="2":::
      Die RGBA-, HSLA-oder Hex-Darstellung der Farbe.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Farb Palette**  
   :::column-end:::
   :::column span="2":::
      Wählen Sie eines der Quadrate aus, um die Farbe in das Quadrat zu ändern.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Farbton**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      7  
   :::column-end:::
   :::column span="1":::
      **Opacity**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      8  
   :::column-end:::
   :::column span="1":::
      **Anzeigewert-Umschalter**  
   :::column-end:::
   :::column span="2":::
      Wechseln zwischen den RGBA-, HSLA-und Hex-Darstellungen der aktuellen Farbe  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **Farbpaletten-Umschalter**  
   :::column-end:::
   :::column span="2":::
      Wechseln zwischen der [Material Design Palette][MaterialDesignColorSystem], einer benutzerdefinierten Palette oder einer Seitenfarben-Palette  DevTools generiert die Seiten Farbpalette basierend auf den Farben, die in ihren Stylesheets gefunden werden.  
   :::column-end:::
:::row-end:::  

#### Beispiel für eine Farbe auf der Seite mit der Pipette  

Wenn Sie die **Farbauswahl**öffnen, ist die **Pipette** (Pipette ![ ][ImageEyedropperIcon] ) standardmäßig aktiviert.  Führen Sie die folgenden Aktionen aus, um die ausgewählte Farbe auf eine andere Farbe auf der Seite zu ändern.  

1.  Zeigen Sie mit der Maus auf die Zielfarbe im Viewport.  
1.  Wählen Sie aus, um zu bestätigen.  
    
    > [!NOTE]
    > In der folgenden Abbildung zeigt die **Farbauswahl** einen aktuellen Farbwert von, der sich in der `rgba(0,0,0,0.7)` Nähe von schwarz befindet.  Die spezifische Farbe sollte auf die Version von Schwarz geändert werden, die aktuell im Viewport hervorgehoben ist, nachdem Sie Sie ausgewählt haben.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Verwenden der Pipette  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Hinzufügen eines PseudoState zu einer Klasse – erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Anzeigen der CSS für ein Element – erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp) | Microsoft docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Erstellen einer minimierte-Datei lesbar – JavaScript-Debug-Referenz | Microsoft docs"  

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
