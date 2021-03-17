---
description: Entdecken Sie neue Workflows zum Anzeigen und Ändern von CSS in Microsoft Edge DevTools.
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 84aacbb3961f6b8f6e9a0bda8823fecbbb26ec25
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439303"
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

# <a name="css-reference"></a>CSS-Referenz  

Entdecken Sie neue Workflows in der folgenden umfassenden Referenz zu Microsoft Edge DevTools-Features im Zusammenhang mit dem Anzeigen und Ändern von CSS.  

Um die Grundlagen zu erlernen, navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCSSGetStarted].  

## <a name="choose-an-element"></a>Auswählen eines Elements  

Mit **dem Tool Elemente** von DevTools können Sie die CSS eines Elements gleichzeitig anzeigen oder ändern.  Das ausgewählte Element wird in der **DOM-Struktur hervorgehoben.**  Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.  Navigieren Sie für ein Lernprogramm zu [Css für ein Element anzeigen.][DevToolsCSSGetStartedTutorial]  

> [!NOTE]
> In der folgenden Abbildung ist das Element, das in der `h1` **DOM-Struktur** hervorgehoben ist, das ausgewählte Element.  Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.  Auf der linken Seite wird das Element im Viewport hervorgehoben, aber nur, weil die Maus derzeit in der **DOM-Struktur**auf das Element zeigt.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1.msft.png":::
   Ein Beispiel für ein ausgewähltes Element  
:::image-end:::  

Verwenden Sie eine der folgenden Aktionen, um ein Element auszuwählen.  

*   Zeigen Sie in Ihrem Viewport auf das Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen aus.**  
*   Wählen Sie in DevTools **Ein** Element auswählen \( Element auswählen ![ ](../media/select-an-element-icon.msft.png) \) oder `Control` + `Shift` + `C` \(Windows, Linux\) oder `Command` + `Shift` + `C` \(macOS\) aus, und wählen Sie dann das Element im Viewport aus.  
*   Wählen Sie in DevTools das Element in der **DOM-Struktur aus.**  
*   Führen Sie in DevTools eine Abfrage wie in der Konsole aus, zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie im Bereich Elemente anzeigen `document.querySelector('p')` **aus.** ****  

## <a name="view-css"></a>Anzeigen von CSS  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a>Anzeigen des externen Stylesheets, in dem eine Regel definiert ist  

Wählen Sie **im Bereich** Formatvorlagen den Link neben einer CSS-Regel aus, um das externe Stylesheet zu öffnen, das die Regel definiert.  

Wenn das Stylesheet vermint ist, navigieren Sie zu [Verminte Datei lesbar machen.][DevToolsJavascriptReferenceFormat]  

> [!NOTE]
> In der folgenden Abbildung werden Sie nach der Auswahl zu Zeile 2 von `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` übernommen, in der die `.content h1:first-of-type` CSS-Regel definiert ist.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Anzeigen des Stylesheets, in dem eine Regel definiert ist" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Anzeigen des Stylesheets, in dem eine Regel definiert ist  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a>Nur das CSS anzeigen, das tatsächlich auf ein Element angewendet wird  

Im **Bereich** Formatvorlagen werden alle Regeln angezeigt, die für ein Element gelten, einschließlich überschriebener Deklarationen.  Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, zeigen Sie im **Bereich Berechnet** nur das CSS an, das tatsächlich auf ein Element angewendet wird.  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Navigieren Sie im **Tool** Elemente zum **Berechneten** Bereich.  

> [!NOTE]
> In einem breiten DevTools-Fenster ist der **Berechnete** Bereich nicht vorhanden.  Der Inhalt des **Berechneten** Panels wird im **Formatvorlagenbereich** angezeigt.  

Geerbte Eigenschaften sind undurchsichtig.  Aktivieren Sie zum Anzeigen aller geerbten Werte das **Kontrollkästchen Alle** anzeigen.  

> [!NOTE]
> In der folgenden Abbildung zeigt der **Berechnete** Bereich die CSS-Eigenschaften, die auf das aktuell ausgewählte Element angewendet `h1` werden.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Der Berechnete Bereich" lightbox="../media/css-elements-computed-h1.msft.png":::
   Der **Berechnete** Bereich  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a>Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge  

Verwenden Sie den **Berechneten** Bereich.  Navigieren Sie [zu Nur css anzeigen, das tatsächlich auf ein Element angewendet wird.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-inherited-css-properties"></a>Anzeigen geerbter CSS-Eigenschaften  

Aktivieren Sie **das Kontrollkästchen Alle** anzeigen im **Bereich Berechnet.**  Navigieren Sie [zu Nur css anzeigen, das tatsächlich auf ein Element angewendet wird.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-the-box-model-for-an-element"></a>Anzeigen des Boxmodells für ein Element  

Zum Anzeigen [des Feldmodells][MDNBoxModel] eines Elements navigieren Sie zum **Formatvorlagenbereich.**  Wenn Ihr DevTools-Fenster schmal ist, befindet sich das **Box Model-Diagramm** am unteren Rand des Panels.  

Wählen Und bearbeiten Sie einen Wert, um einen Wert zu ändern.  

> [!NOTE]
> In der folgenden Abbildung zeigt das **** **Diagramm Feldmodell** im Bereich Formatvorlagen das Feldmodell für das aktuell ausgewählte `h1` Element.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Das Diagramm "Boxmodell"" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Das **Diagramm "Boxmodell"**  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a>Suchen und Filtern der CSS eines Elements  

Verwenden Sie **das Textfeld Filter** in den **Feldern Formatvorlagen** und **Berechnet,** um nach bestimmten CSS-Eigenschaften oder -Werten zu suchen.  

Aktivieren Sie das Kontrollkästchen Alle anzeigen, um auch geerbte Eigenschaften im **Berechneten** Bereich **zu** durchsuchen.  

> [!NOTE]
> In der folgenden Abbildung wird der **Formatvorlagenbereich** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage `color` enthalten.  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtern des Formatvorlagenbereichs" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtern des **Formatvorlagenbereichs**  
:::image-end:::  

> [!NOTE]
> In der folgenden Abbildung wird der **Berechnete** Bereich so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage `100%` enthalten.  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtern des berechneten Panels" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtern des **berechneten Panels**  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a>Umschalten einer Pseudoklasse  

Führen Sie die folgenden Aktionen aus, um eine Pseudoklasse wie `:active` , `:focus` , oder `:hover` umzuschalten. `:visited`  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Navigieren Sie **im Tool** Elemente zum **Formatvorlagenbereich.**  
1.  Wählen **Sie :hov**aus.  
1.  Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.  

> [!NOTE]
> In der folgenden Abbildung umschalten Sie die `:hover` Pseudoklasse.  Vergewissern Sie sich im viewport, dass die Deklaration auf das Element angewendet wird, auch wenn das Element nicht tatsächlich über `background-color: cornflowerblue` das Element bewegt wird.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Umschalten der Pseudoklasse :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Umschalten `:hover` der Pseudoklasse  
:::image-end:::  

Navigieren Sie für ein interaktives Lernprogramm zu [Hinzufügen eines Pseudozustands zu einer Klasse][DevToolsCSSGetStartedAddPseudoState].  

### <a name="view-a-page-in-print-mode"></a>Anzeigen einer Seite im Druckmodus  

Führen Sie die folgenden Aktionen aus, um eine Seite im Druckmodus zu sehen.  

1.  [Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].  
1.  Beginnen Sie mit der `Rendering` Eingabe und wählen Sie `Show Rendering` aus.  
1.  Wählen Sie **im Dropdownmenü Emulieren von CSS-Medien** die Option **Drucken aus.**  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a>Anzeigen verwendeter und nicht verwendeter CSS mit dem Tool "Abdeckung"  

Das **Coverage-Tool** zeigt, welche CSS eine Seite tatsächlich verwendet.  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, während DevTools [][DevToolsCommandMenu]im Fokus steht, um das Befehlsmenü zu öffnen.  
1.  Beginnen Sie mit der `coverage` Eingabe und wählen Sie Abdeckung anzeigen **aus.**  Das **Abdeckungstool** wird angezeigt.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Öffnen des Coverage-Tools über das Befehlsmenü" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Öffnen Sie **das Tool** "Abdeckung" im **Befehlsmenü.**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Das Tool "Abdeckung"" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             Das **Tool "Abdeckung"**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen **Sie Die Instrumentierungsabdeckung starten aus, und aktualisieren Sie die Seite** \( Starten Sie die ![ Instrumentierungsabdeckung, und aktualisieren Sie die Seite ](../media/refresh-icon.msft.png) \).  Die Seite wird aktualisiert, und das **Coverage-Tool** bietet eine Übersicht darüber, wie viel CSS \(und JavaScript\) aus jeder Datei verwendet wird, die der Browser lädt.  Grün steht für verwendete CSS.  Rot steht für nicht verwendete CSS.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Eine Übersicht darüber, wie viel CSS \(und JavaScript\) verwendet und nicht verwendet wird  
    :::image-end:::  

1.  Wählen Sie eine CSS-Datei aus, um eine zeilenweise Aufschlüsselung der verwendeten CSS-Dateien anzeigen zu können.  
    
    > [!NOTE]
    > In der folgenden Abbildung werden die Zeilen 145 bis 147 und 149 bis 151 nicht verwendet, während die Zeilen `b66bc881.site-ltr.css` 163 bis 166 verwendet werden.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Eine zeilenweise Aufschlüsselung der verwendeten und nicht verwendeten CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       Eine zeilenweise Aufschlüsselung der verwendeten und nicht verwendeten CSS  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a>Erzwingen des Druckvorschaumodus  

Navigieren Sie [zu Erzwingen von DevTools in den Druckvorschaumodus.][DevToolsCssPrintPreview]  

## <a name="change-css"></a>Ändern von CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a>Hinzufügen einer CSS-Deklaration zu einem Element  

Die Reihenfolge der Deklarationen wirkt sich darauf aus, wie ein Element formatiert wird. Verwenden Sie die folgende Liste, um Deklarationen auf unterschiedliche Weise hinzuzufügen.  

*   [Fügen Sie eine Inlinedeklaration hinzu.](#add-an-inline-declaration)  Entspricht dem Hinzufügen `style` eines Attributs zum HTML eines Elements.  
*   [Fügen Sie einer Formatvorlageregel eine Deklaration hinzu.](#add-a-declaration-to-a-style-rule)  

**Welchen Workflow sollten Sie verwenden?** In den meisten Szenarien möchten Sie wahrscheinlich den Inlinedeklarationsworkflow verwenden.  Inlinedeklarationen haben eine höhere Spezifizität als externe, sodass der Inlineworkflow sicherstellt, dass die Änderungen in Ihrem erwarteten Element wirksam werden.  Weitere Informationen zur Spezifizität finden Sie unter [Selector Types][MDNSelectorTypes].  

Wenn Sie Formatvorlagen des Elements debuggen und speziell testen müssen, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.  

#### <a name="add-an-inline-declaration"></a>Hinzufügen einer Inlinedeklaration  

Führen Sie die folgenden Aktionen aus, um eine Inlinedeklaration hinzuzufügen.  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Wählen Sie **im Bereich** Formatvorlagen zwischen den Klammern des **Abschnitts element.style** aus.  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftennamen ein, und wählen Sie `Enter` aus.  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie `Enter` aus.  Überprüfen Sie **in der DOM-Struktur,** ob dem Element ein `style` Attribut hinzugefügt wurde.  

> [!NOTE]
> In der folgenden Abbildung wurden `margin-top` die Eigenschaften und auf das ausgewählte Element `background-color` angewendet.  Überprüfen Sie **in der DOM-Struktur,** ob die Deklarationen im `style` Attribut für ein Element enthalten sind.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Hinzufügen von Inlinedeklarationen" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Hinzufügen von Inlinedeklarationen  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a>Hinzufügen einer Deklaration zu einer Formatvorlageregel  

Führen Sie die folgenden Aktionen aus, um einer vorhandenen Formatvorlageregel eine Deklaration hinzuzufügen.  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Wählen Sie **im Bereich** Formatvorlagen zwischen den Klammern der Formatvorlagenregel aus, der Sie die Deklaration hinzufügen möchten.  Der Cursor konzentriert sich, sodass Sie Text eingeben können.  
1.  Geben Sie einen Eigenschaftennamen ein, und wählen Sie `Enter` aus.  
1.  Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie `Enter` aus.  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Hinzufügen einer Deklaration zu einer Formatvorlageregel" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Formatvorlageregel  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a>Ändern eines Deklarationsnamens oder -werts  

Wählen Und bearbeiten Sie den Namen oder Wert einer Deklaration, um sie zu ändern.  Für Verknüpfungen zum schnellen Inkrementieren oder Dekrementieren eines Werts durch , , oder Einheiten navigieren Sie zu Ändern von `0.1` `1` `10` `100` [Deklarationswerte mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts).  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Ändern des Werts einer Deklaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Ändern des Werts der `border-bottom-style` Deklaration  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a>Ändern von Deklarationswerten mit Tastenkombinationen  

Beim Bearbeiten des Werts einer Deklaration können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen bestimmten Betrag zu erhöhen.  

*   Wählen `Alt` + `Up` Sie \(Windows, Linux\) oder `Option` + `Up` \(macOS\) aus, um um zu `0.1` erhöhen.  
*   Wählen `Up` Sie diese Option aus, um den Wert durch oder durch zu ändern, wenn sich der aktuelle Wert zwischen und `1` `0.1` `-1` `1` befindet.  
*   Wählen `Shift` + `Up` Sie aus, um um zu `10` erhöhen.  
*   Wählen `Shift` + `Page Up` Sie \(Windows, Linux\) oder `Shift` + `Command` + `Up` \(macOS\) aus, um den Wert um zu `100` erhöhen.  

Die Dekrementierung funktioniert ebenfalls.  Ersetzen Sie einfach jede oben `Up` genannte Instanz durch `Down` .  

### <a name="add-a-class-to-an-element"></a>Hinzufügen einer Klasse zu einem Element  

Führen Sie die folgenden Aktionen aus, um einem Element eine Klasse hinzuzufügen.  

1.  [Wählen Sie das Element](#choose-an-element) in der **DOM-Struktur aus.**  
1.  Wählen **Sie .cls**aus.  
1.  Geben Sie den Namen der Klasse in das Textfeld **Neue Klasse** hinzufügen ein.  
1.  Wählen Sie `Enter` aus.  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Der Bereich Elementklassen" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Der **Bereich Elementklassen**  
:::image-end:::  

### <a name="toggle-a-class"></a>Umschalten einer Klasse  

Führen Sie die folgenden Aktionen aus, um eine Klasse für ein Element zu aktivieren oder zu deaktivieren.  

1.  [Wählen Sie das Element](#choose-an-element) in der **DOM-Struktur aus.**  
1.  Öffnen Sie den **Bereich Elementklassen.**  Navigieren Sie [zu Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).  Unterhalb des **Textfelds Neue Klasse** hinzufügen werden alle Klassen auf das spezifische Element angewendet.  
1.  Aktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.  

### <a name="add-a-style-rule"></a>Hinzufügen einer Formatvorlageregel  

Führen Sie die folgenden Aktionen aus, um eine neue Formatvorlageregel hinzuzufügen.  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Wählen **Sie Neue Formatvorlageregel** \( ![ Neue Formatvorlageregel ](../media/new-style-rule-icon.msft.png) \).  DevTools fügt eine neue Regel unter der **element.style-Regel** ein.  

> [!NOTE]
> In der folgenden Abbildung fügt DevTools die `h1.devsite-page-title` Formatvorlageregel hinzu, nachdem Sie **Neue Formatvorlageregel auswählen.**  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Hinzufügen einer neuen Formatvorlageregel" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Hinzufügen einer neuen Formatvorlageregel  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a>Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll  

Wenn [Sie eine neue Formatvorlageregel hinzufügen,](#add-a-style-rule)wählen Sie Neue Formatvorlageregel \( Neue Formatvorlageregel \) aus, und halten Sie diese fest, um zu wählen, zu welchem Stylesheet die **** ![ ](../media/new-style-rule-icon.msft.png) Formatvorlageregel hinzugefügt werden soll.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Auswählen eines Stylesheets" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Auswählen eines Stylesheets  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a>Hinzufügen einer Formatvorlageregel zu einem bestimmten Speicherort  

Führen Sie die folgenden Aktionen aus, um einer bestimmten Position im Formatvorlagenbereich eine **Formatregel hinzuzufügen.**  

1.  Zeigen Sie auf die Formatvorlageregel, die sich direkt über der Stelle befindet, an der Sie die neue Formatvorlageregel hinzufügen möchten.  
1.  [Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)  
1.  Wählen **Sie Formatvorlageregel einfügen unten** \( ![ Formatvorlageregel einfügen unten symbol ](../media/new-style-rule-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Einfügen von Formatvorlageregel unten" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Einfügen von Formatvorlageregel unten**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a>Anzeigen der Symbolleiste "Weitere Aktionen"  

Mit **der Symbolleiste** Weitere Aktionen können Sie die folgenden Aktionen ausführen.  

*   Fügen Sie eine Formatvorlageregel direkt unterhalb der Formatvorlage ein, auf die Sie sich konzentrieren.  
*   Fügen Sie der Formatregel, auf die Sie sich konzentrieren, eine , , oder `background-color` `color` `box-shadow` `text-shadow` -Deklaration hinzu.  

Führen Sie die folgenden Aktionen aus, um die Symbolleiste **Weitere Aktionen anzuzeigen.**  

1.  Zeigen Sie **im Bereich** Formatvorlagen auf eine Formatvorlageregel.  **Weitere Aktionen** \( \) werden unten rechts im Abschnitt `...` Formatregel angezeigt.  
    
    > [!NOTE]
    > Zeigen Sie in der folgenden Abbildung auf die Formatregel, und weitere Aktionen werden unten rechts im Abschnitt `.header-holder.has-default-focus` Formatregel angezeigt. ****  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Weitere Aktionen" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Reveal **More Actions** \( `...` \)  
    :::image-end:::  
    
1.  Zeigen Sie auf **Weitere Aktionen** \( `...` \), um die oben genannten Aktionen zu zeigen.  
    
    > [!NOTE]
    > Die **Aktion Style Rule Below** einfügen wird nach dem Zeigen auf weitere Aktionen **angezeigt.**  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Die Symbolleiste "Weitere Aktionen"" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Die **Symbolleiste "Weitere Aktionen"**  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a>Umschalten einer Deklaration  

Führen Sie die folgenden Aktionen aus, um eine einzelne Deklaration auf \(oder off\) umzuschalten.  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Zeigen Sie **im Bereich** Formatvorlagen auf die Regel, die die Deklaration definiert.  Neben jeder Deklaration wird ein Kontrollkästchen angezeigt.  
1.  Aktivieren Sie \(oder deaktivieren Sie\) das Kontrollkästchen neben der Deklaration.  Wenn Sie eine Deklaration deaktivieren, durchkreuzt DevTools sie, um anzugeben, dass sie nicht mehr aktiv ist.  

> [!NOTE]
> In der folgenden Abbildung wurde die Eigenschaft für das aktuell ausgewählte Element `margin-top` deaktiviert.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Umschalten einer Deklaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Umschalten einer Deklaration  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a>Hinzufügen einer Hintergrundfarbdeklaration  

Führen Sie die folgenden Aktionen aus, um einem `background-color` Element eine Deklaration hinzuzufügen.  

1.  Zeigen Sie auf die Formatvorlageregel, der Sie die `background-color` Deklaration hinzufügen möchten.  
1.  [Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)  
1.  Wählen **Sie Hintergrundfarbe hinzufügen** \( Symbol ![ Hintergrundfarbe hinzufügen ](../media/add-background-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Hinzufügen von Hintergrundfarbe" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Hinzufügen von Hintergrundfarbe**  
:::image-end:::  

### <a name="add-a-color-declaration"></a>Hinzufügen einer Farbdeklaration  

Führen Sie die folgenden Aktionen aus, um einem `color` Element eine Deklaration hinzuzufügen.  

1.  Zeigen Sie auf die Formatvorlageregel, der Sie die `color` Deklaration hinzufügen möchten.  
1.  [Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)  
1.  Wählen **Sie Farbe hinzufügen** \( ![ Farbsymbol hinzufügen ](../media/add-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Hinzufügen von Farbe" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Hinzufügen von Farbe**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a>Hinzufügen einer Box-Shadow-Deklaration  

Führen Sie die folgenden Aktionen aus, um einem `box-shadow` Element eine Deklaration hinzuzufügen.  

1.  Zeigen Sie auf die Formatvorlageregel, der Sie die `box-shadow` Deklaration hinzufügen möchten.  
1.  [Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)  
1.  Wählen **Sie Hinzufügen von Feldschatten** \( Hinzufügen des ![ Feldschattensymbols ](../media/add-box-shadow-icon.msft.png) \) aus.  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Hinzufügen von Box Shadow" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Hinzufügen von Box Shadow**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a>Hinzufügen einer Text-Schatten-Deklaration  

Führen Sie die folgenden Aktionen aus, um einem `text-shadow` Element eine Deklaration hinzuzufügen.  

1.  Zeigen Sie auf die Formatvorlageregel, der Sie die `text-shadow` Deklaration hinzufügen möchten.  
1.  [Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)  
1.  Wählen **Sie Textschatten** hinzufügen \( ![ Textschattensymbol ](../media/add-text-shadow-icon.msft.png) hinzufügen \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Hinzufügen von Textschatten" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Hinzufügen von Textschatten**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a>Ändern von Farben mit der Farbauswahl  

Die **Farbauswahl bietet** eine GUI zum Ändern `color` und `background-color` Deklarationen.  

Führen Sie die folgenden Aktionen aus, um die **Farbauswahl zu öffnen.**  

1.  [Wählen Sie ein Element aus.](#choose-an-element)  
1.  Suchen Sie **im Bereich** Formatvorlagen nach der , oder ähnlichen Deklaration, die Sie `color` ändern `background-color` möchten.  Links vom Wert , oder einem ähnlichen Wert befindet sich ein kleines Quadrat, das eine `color` `background-color` Vorschau der Farbe ist.  
    
    > [!NOTE]
    > In der folgenden Abbildung ist das kleine Quadrat links von eine `rgba(0, 0, 0, 0.7)` Vorschau dieser Farbe.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Farbvorschau" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Farbvorschau  
    :::image-end:::  
    
1.  Wählen Sie die Vorschau aus, um die **Farbauswahl zu öffnen.**  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Die Farbauswahl" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       Die **Farbauswahl**  
    :::image-end:::  
    
In der folgenden Abbildung und Liste werden die einzelnen Benutzeroberflächenelemente der Farbauswahl **aufgeführt.**  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Die Farbauswahl mit Anmerkungen" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   The **Color Picker**, annotated  
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
      **Eyedropper**  
   :::column-end:::
   :::column span="2":::
      Weitere Informationen finden Sie unter [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).  
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
      Kopieren Sie **den Anzeigewert** in die Zwischenablage.  
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
      Die RGBA-, HSLA- oder Hexdarstellung der Farbe.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Farbpalette**  
   :::column-end:::
   :::column span="2":::
      Wählen Sie eines der Quadrate aus, um die Farbe in dieses Quadrat zu ändern.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Hue**  
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
      **Display Value Switcher**  
   :::column-end:::
   :::column span="2":::
      Umschalten zwischen den RGBA-, HSLA- und Hex-Darstellungen der aktuellen Farbe.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **Farbpaletten-Switcher**  
   :::column-end:::
   :::column span="2":::
      Umschalten zwischen der [Palette Materialdesign,][MaterialDesignColorSystem]einer benutzerdefinierten Palette oder einer Seitenfarbenpalette.  DevTools generiert die Seitenfarbpalette basierend auf den Farben, die sie in Ihren Stylesheets findet.  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a>Beispiel für eine Farbe von der Seite mit der Eyedropper  

Wenn Sie die **Farbauswahl öffnen,** ist **die Eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) standardmäßig aktiviert.  Führen Sie die folgenden Aktionen aus, um die ausgewählte Farbe in eine andere Farbe auf der Seite zu ändern.  

1.  Zeigen Sie im Viewport auf die Zielfarbe.  
1.  Wählen Sie aus, um dies zu bestätigen.  
    
    > [!NOTE]
    > In der folgenden Abbildung zeigt die **Farbauswahl** den aktuellen Farbwert von , der in der Nähe von `rgba(0,0,0,0.7)` Schwarz liegt.  Die spezifische Farbe sollte in die Version von Schwarz geändert werden, die derzeit im Ansichtsfenster hervorgehoben ist, nachdem Sie sie ausgewählt haben.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Verwenden der Eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Verwenden der Eyedropper  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Führen Sie Befehle mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Hinzufügen eines Pseudozustands zu einer Klasse – Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Anzeigen der CSS für ein Element – Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Erzwingen von Microsoft Edge DevTools in den Druckvorschaumodus (CSS Print Media Type) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Eine minifizierte Datei lesbar machen – JavaScript Debugging Reference | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Das Farbsystem – Materialdesign"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Das Feldmodell | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Auswahltypen – Spezifizitätstypen | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  