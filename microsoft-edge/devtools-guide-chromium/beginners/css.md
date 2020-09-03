---
description: Erste Schritte mit CSS
title: 'DevTools für Anfänger: Erste Schritte mit CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993303"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# DevTools für Anfänger: Erste Schritte mit CSS  

In diesem Lernprogramm erfahren Sie, wie Sie eine Webseite mithilfe von CSS formatieren.  Sie erfahren auch, wie Sie Microsoft Edge devtools verwenden, um mit CSS-Änderungen zu experimentieren.  

Der folgende Artikel ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in denen Sie die Grundlagen der Webentwicklung und der Microsoft Edge-devtools.  Sie erhalten praktische Erfahrungen, wenn Sie tatsächlich ihre eigene Website erstellen.  Sie müssen das erste Lernprogramm nicht durchführen, bevor Sie den zweiten Schritt ausführen.  [Einrichten Ihres Codes](#set-up-your-code) zeigt, wie Sie sich einrichten.  

> [!NOTE]
> Dieses Lernprogramm ist für absolute Anfänger konzipiert und konzentriert sich sowohl auf die **Grundlagen der Webentwicklung** als auch auf die Grundlagen der Verwendung von devtools zum Experimentieren mit CSS.  Wenn Sie ein Lernprogramm benötigen, das sich nur auf devtools konzentriert, lesen Sie [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].  

Am Anfang des Lernprogramms sollte Ihre Website wie in der folgenden Abbildung aussehen.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Wie Ihre Website aktuell aussieht" lightbox="../media/beginners-css-intro1.msft.png":::
   Wie Ihre Website aktuell aussieht  
:::image-end:::  

Nachdem Sie das Lernprogramm abgeschlossen haben, sollte die Website wie in der folgenden Abbildung dargestellt aussehen.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Wie Ihre Website am Ende des Lernprogramms aussehen sollte" lightbox="../media/beginners-css-intro2.msft.png":::
   Wie Ihre Website am Ende des Lernprogramms aussehen sollte  
:::image-end:::  

## Ziele  

Führen Sie dieses Lernprogramm aus, um die folgenden Konzepte und Aufgaben besser zu verstehen.  

*   Verwenden von CSS zum Formatieren einer Webseite  
*   Verwenden von Microsoft Edge devtools zum Experimentieren mit CSS  
*   Der Unterschied zwischen CSS-und CSS-Frameworks.  

Sie erstellen eine echte Website.  

## Voraussetzungen  

Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus.  

*   Führen Sie [die ersten Schritte mit HTML und dem Dom durch][DevtoolsBeginnersHtml] , oder stellen Sie sicher, dass Sie HTML und das DOM ähnlich wie in diesem Lernprogramm kennen.  
*   Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.  Das folgende Lernprogramm verwendet eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, die in Microsoft Edge integriert sind.  

## Einrichten Ihres Codes  

Um Ihre Website zu erstellen, müssen Sie zunächst die folgenden Aktionen ausführen, um den Code einzurichten.  

> [!NOTE]
> Wenn Sie das erste Lernprogramm in der Serie bereits abgeschlossen haben, fahren Sie mit dem nächsten Abschnitt fort.  Verwenden Sie weiterhin ihren Code aus dem letzten Lernprogramm, [Erste Schritte mit HTML und dem Dom][DevtoolsBeginnersHtml].  

1.  Öffnen Sie den [Quellcode][GlitchCookedAmphibianIndex].  Auf die Registerkarte "im Fokus" Ihres Browsers wird als **Registerkarte "Bearbeiten"** verwiesen.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Die Registerkarte ' bearbeiten '" lightbox="../media/beginners-css-setup1.msft.png":::
       Die Registerkarte ' **Bearbeiten** '  
    :::image-end:::  
    
1.  Wählen Sie **gekocht-Amphibien**aus.  Ein Menü wird eingeblendet.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Das Menü "Projektoptionen"" lightbox="../media/beginners-css-setup2.msft.png":::
       Das Menü "Projektoptionen"  
    :::image-end:::  

1.  Wählen Sie **Remix Project**aus.  Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.  
    
    > [!NOTE]
    > Glitch generiert einen zufälligen Namen für das neue Projekt.  
    
1.  Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.  Eine andere Registerkarte wird mit einer Live Ansicht Ihrer Website geöffnet.  Auf die Registerkarte "auf dem Fokus" Ihres Browsers wird als **"Live"-Registerkarte**verwiesen.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Die Registerkarte "Live"" lightbox="../media/beginners-css-setup3.msft.png":::
       Die **Registerkarte "Live"**  
    :::image-end:::  

## Grundlegendes zu CSS  

**CSS** ist eine Computersprache, die das Layout und die Gestaltung von Webseiten bestimmt.  Die folgende Abbildung ist ein Absatz mit einem Rahmen.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Der Text wurde mit CSS formatiert" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Der Text wurde mit CSS formatiert  
:::image-end:::  

Der folgende Codeausschnitt ist der HTML-und CSS-Code, der zum Erstellen des Absatzes in der vorherigen Abbildung verwendet wird.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` sieht Ihnen vielleicht neu aus.  Der andere sollte vertraut aussehen.  Wenn dies nicht der Fall ist, führen Sie die ersten [Schritte mit HTML und dem Dom durch][DevtoolsBeginnersHtml] , bevor Sie die folgenden Abschnitte versuchen.  

## Hinzufügen von Inlineformatvorlagen  

Führen Sie die folgenden Aktionen aus, um **Inlineformatvorlagen** zum Anwenden von Formatvorlagen auf ein einzelnes Element zu verwenden.  

1.  Wechseln Sie zurück zur Registerkarte Bearbeitung, und öffnen Sie Sie `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       `index.html`Auf der Registerkarte "Bearbeiten" öffnen  
    :::image-end:::  
    
1.  `style="background-color: aliceblue;"`Zu ihrer hinzufügen `<nav>` .  Im Code-Block unten ist die vierte Codezeile diejenige, die Sie ändern müssen.  Der restliche Bereich ist gerade vorhanden, sodass Sie sicherstellen können, dass Sie den neuen Code an die richtige Stelle setzen.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Wechseln Sie zum **Reiter "Live"** , um die Änderungen anzuzeigen!  Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau" lightbox="../media/beginners-css-inline2.msft.png":::
       Die Hintergrundfarbe hinter dem **Start** -und **Kontakt** Link ist jetzt blau  
    :::image-end:::  
    
## Wieder verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets  

In einem vorherigen Codeausschnitt hat eine Inlineformatvorlage eine Formatvorlage auf eine einzelne `<p>` Kategorie angewendet.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Was ist, wenn Sie möchten, dass alle `<p>` Elemente auf Ihrer Webseite auf die gleiche Weise formatiert werden?  Sie müssten den Code in jeder einzelnen `<p>` Kategorie auf Ihrer Website kopieren und einfügen.  Das ist viel Zeit und Mühe.  Und wenn Sie eine Bearbeitung vornehmen mussten, müssten Sie jedes Tag erneut ändern.  Führen Sie die folgenden Aktionen aus, um ein **internes Stylesheet** zu verwenden, um das CSS einmal zu schreiben, damit es auf mehrere Elemente angewendet wird.  

1.  Klicken Sie auf der Registerkarte Live auf **Kontakt** , um zur Kontaktseite zu gelangen.  Beachten Sie die Schriftart für " **Privat** " und " **Kontakt**".  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-internal1.msft.png":::
       Die Kontaktseite  
    :::image-end:::  
    
1.  Wechseln Sie auf der **Registerkarte Editor**zu `contact.html` .  
1.  Fügen Sie den folgenden Code hinzu `contact.html` .  Beachten Sie, dass die Zeilen, die mit `<style>` und endet mit beginnen, das `</style>` hinzufügen müssen.  Der andere Code ist gerade vorhanden, damit Sie wissen, wo der neue Code platziert werden soll.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Wechseln Sie zurück zur **Registerkarte Live**.  
1.  Wählen Sie **Kontakt** aus, um zur Kontaktseite zurückzukehren.  Die Schriftart von " **Start** " und " **Kontakt** " hat sich geändert.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Die Schriftart der Links für "Start" und "Kontakt" wurde geändert." lightbox="../media/beginners-css-internal2.msft.png":::
       Die Schriftart der Links für " **Start** " und " **Kontakt** " wurde geändert.  
    :::image-end:::  
    
### Grundlegendes zu internen Stylesheets  

Interne Stylesheets wenden Formatvorlagen mithilfe von **Auswahlen**an.  Auswahlen sind Muster, die möglicherweise für ein oder mehrere HTML-Elemente gelten.  Im vorherigen Codeausschnitt wurde die folgende Formatvorlage hinzugefügt.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` ist eine Auswahl, die in "jedes Element mit `<li>` einem `<a>` Element" übersetzt wird.  Der Browser ändert die Schriftart der **Home** -und **Contact** -Links, weil jede der Kategorien mit dem Muster übereinstimmt.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` ist eine **Deklaration**.  Eine Deklaration besteht aus zwei Teilen.  

:::row:::
   :::column span="1":::
      **Eigenschaft**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      Die Eigenschaft beschreibt eine allgemeine Methode, mit der Sie die Formatvorlage des Elements ändern können.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      Der Wert beschreibt genau, wie sich die Formatvorlage des Elements ändern soll.  
   :::column-end:::
:::row-end:::  

Gibt beispielsweise dem `font-family: 'Courier New', Courier, serif` Browser die folgende Anweisung aus: "die Schriftart von Elementen, die dem Muster entsprechen, auf festzulegen `li a` `'Courier New'` .  Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .  Wenn dies nicht möglich ist, verwenden Sie `serif` . "  

### Hinzufügen mehrerer Auswahlen zu einem RuleSet  

Ein Block mit CSS-Code wie dem, was unten angezeigt wird, wird als **RuleSet**bezeichnet.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Führen Sie die folgenden Aktionen aus, um einen RuleSet mithilfe von Kommas mehrere Auswahlen hinzuzufügen.  

1.  Öffnen Sie auf der **Registerkarte Editor den Reiter** `contact.html` .  
1.  Nach `li a` Typ `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    Im vorherigen Codeausschnitt wird der Browser angewiesen, Formatvorlagen `<h1>` Elemente auf die gleiche Weise zu formatieren wie Elemente, die dem Muster entsprechen `li a` .  
    
1.  Wechseln Sie zur **Registerkarte Live**.  
1.  Wählen Sie den Link **Kontakt** aus, um zur Kontaktseite zurückzukehren.  **Kontaktieren Sie mich jetzt!** hat die gleiche Schriftart wie die Navigationslinks.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Der Text kontaktiere mich!  hat nun dieselbe Schriftart wie die Links für "Privat" und "Kontakt"" lightbox="../media/beginners-css-multiple1.msft.png":::
       Der Text **kontaktiere mich!** hat nun dieselbe Schriftart wie die Links für " **Privat** " und " **Kontakt** "  
    :::image-end:::  
    
## Experimentieren mit devtools  

Wenn Sie Ihre Reise fortsetzen, um ein Experte für Webentwicklung zu werden, können Sie feststellen, dass CSS schwierig ist.  Sie können einige CSS-Daten schreiben und davon ausgehen, dass Sie auf eine Art und Weise angezeigt werden, doch der Browser hat etwas völlig anderes.  Microsoft Edge devtools macht es einfach, mit Änderungen zu experimentieren und sofort zu sehen, wie sich die Änderungen auf die Seite auswirken.  

### Hinzufügen einer Deklaration zu einem vorhandenen rulet-Element in devtools  

Führen Sie die folgenden Aktionen aus, um die Formatvorlage eines vorhandenen Elements zu durchlaufen, und fügen Sie eine Deklaration zu einem vorhandenen RuleSet hinzu.  

1.  Zeigen Sie auf den Link " **Start** ", öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Überprüfen des Start Links" lightbox="../media/beginners-css-add1.msft.png":::
       Überprüfen des Start Links  
    :::image-end:::  
    
    DevTools wird neben ihrer Seite geöffnet.  Der Code, der den Link "Start" darstellt, `<a href="/">Home</a>` wird in der DOM-Struktur blau hervorgehoben.  Der Codeausschnitt und die Vorschau sollten von den ersten [Schritten mit HTML und dem Dom][DevtoolsBeginnersHtml]vertraut sein.  
    
    :::row:::
       :::column span="":::
          In der folgenden Abbildung wird die `font-family: 'Courier New', Courier, serif` Deklaration, die Sie zuvor hinzugefügt haben, auf `contact.html` der Registerkarte **Formatvorlagen** unter der DOM-Struktur angezeigt.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur." lightbox="../media/beginners-css-add2.msft.png":::
             Die Registerkarte " **Formatvorlagen** " befindet sich unterhalb der DOM-Struktur.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Wenn Ihr devtools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur." lightbox="../media/beginners-css-add3.msft.png":::
             Die Registerkarte " **Formatvorlagen** " befindet sich rechts neben der DOM-Struktur.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen Sie die leere Zeile unten aus `font-family: 'Courier New', Courier, Serif` , um eine neue Deklaration hinzuzufügen.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Hinzufügen einer neuen Deklaration" lightbox="../media/beginners-css-add4.msft.png":::
       Hinzufügen einer neuen Deklaration  
    :::image-end:::  
    
1.  Geben `color` Sie ein, und wählen Sie aus `Enter` .  Die AutoVervollständigen-Benutzeroberfläche schlägt Optionen während der Eingabe vor.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Farbe eingeben" lightbox="../media/beginners-css-add5.msft.png":::
       Typ `color`  
    :::image-end:::  
    
1.  Geben `magenta` Sie ein, und wählen Sie aus `Enter` .  Der gesamte Text auf der Kontaktseite ist jetzt Magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Typ Magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Typ `magenta`  
    :::image-end:::  
    
### Bearbeiten einer Deklaration in devtools  

Führen Sie die folgenden Aktionen aus, um vorhandene Deklarationen in devtools zu bearbeiten.  

1.  Wählen Sie das Magenta-Quadrat neben aus `magenta` .  Eine Farbauswahl wird eingeblendet.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Die Farbauswahl" lightbox="../media/beginners-css-edit1.msft.png":::
       Die Farbauswahl  
    :::image-end:::  
    
1.  Verwenden Sie die Farbauswahl, um den Schriftart Text in eine Farbe zu ändern, die Ihnen gefällt.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Ändern der Schriftfarbe in Lila mit der Farbauswahl" lightbox="../media/beginners-css-edit2.msft.png":::
       Ändern der Schriftfarbe in Lila mit der Farbauswahl  
    :::image-end:::  
    
### Hinzufügen eines neuen RuleSets in devtools  

Führen Sie die folgenden Aktionen aus, um neue RuleSets in devtools hinzuzufügen.  

1.  Wählen Sie **neue** Stilregel-Regel \ ( ![ neue Stilregel ][ImageNewStyleRuleIcon] \) aus, die sich neben **CLS**befindet.  Ein leerer RuleSet wird `a` als Auswahl angezeigt.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Hinzufügen einer neuen Regel" lightbox="../media/beginners-css-rule1.msft.png":::
       Hinzufügen einer neuen Regel  
    :::image-end:::  
    
1.  Ersetzen Sie `a` durch `a:hover`.  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Ersetzen eines durch a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Ersetzen `a` durch `a:hover`  
    :::image-end:::  
    
    `:hover` ist eine **Pseudoklasse**.  Verwenden Sie Pseudoklassen für Formatvorlagenelemente, die möglicherweise spezielle Zustände eingeben.  Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie auf ein Element zeigen `<a>` .  
    
1.  Wählen Sie zwischen den Klammern aus, um eine neue Deklaration hinzuzufügen.  
1.  Geben `background-color` Sie für den Deklarations Namen ein, und wählen Sie aus `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Hintergrundfarbe eingeben" lightbox="../media/beginners-css-rule3.msft.png":::
       Typ `background-color`  
    :::image-end:::  
    
1.  Geben `green` Sie für den Deklarations Wert ein, und wählen Sie aus `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Typ grün" lightbox="../media/beginners-css-rule4.msft.png":::
       Typ `green`  
    :::image-end:::  
    
1.  Zeigen Sie mit der Maus auf den Link " **Start** ".  Der Hintergrund des Links wird grün.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen" lightbox="../media/beginners-css-rule5.msft.png":::
       Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen  
    :::image-end:::  
    
## Wieder verwenden von Formatvorlagen auf mehreren Seiten mit externen Stylesheets  

In einem vorherigen Schritt haben Sie den folgenden Codeausschnitt als internes Stylesheet hinzugefügt `contact.html` .  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

Was ist, wenn Sie `index.html` die gleiche Weise formatieren möchten?  Was ist, wenn Sie über eine große Anzahl von Seiten verfügen, auf die Sie Ihre Formatvorlagen anwenden möchten?  Sie müssten das interne Stylesheet in jede einzelne Webseite auf Ihrer Website kopieren und einfügen.  Führen Sie die folgenden Aktionen aus, um ein **externes Stylesheet** hinzuzufügen, das es Ihnen ermöglicht, Ihre CSS einmal zu schreiben und auf mehrere Seiten anzuwenden.  

1.  Laden Sie zunächst die Registerkarte "Live" neu, um die Änderungen zu entfernen, die Sie in devtools vorgenommen haben.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Nachdem Sie die Seite aktualisiert haben, sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden." lightbox="../media/beginners-css-external1.msft.png":::
        Nachdem Sie die Seite aktualisiert haben, sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor** , und öffnen Sie Sie `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Löschen Sie alles zwischen `<style>` und `</style>` , einschließlich `<style>` und `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Das Stil-Tag wurde entfernt" lightbox="../media/beginners-css-external3.msft.png":::
       Das Stil-Tag wurde entfernt  
    :::image-end:::  
    
1.  Wechseln Sie zu `index.html` der Kategorie, und entfernen Sie Sie `style="background-color: aliceblue;"` `<nav>` .  Sie haben jetzt alle CSS entfernt, die Sie zuvor zu Ihrer Website hinzugefügt haben.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Die Inlineformatvorlage wurde aus dem NAV-Element entfernt" lightbox="../media/beginners-css-external4.msft.png":::
       Die Inlineformatvorlage wurde aus dem NAV-Element entfernt  
    :::image-end:::  
    
1.  Wählen Sie **neue Datei**aus.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Dialogfeld ' neue Datei '" lightbox="../media/beginners-css-external5.msft.png":::
       Dialogfeld ' neue Datei '  
    :::image-end:::  
    
1.  Ersetzen `cool-file.js` `style.css` Sie durch, und wählen Sie **Datei hinzufügen**aus.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type Style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
       Typ `style.css`  
    :::image-end:::  
    
1.  Fügen Sie der Datei den folgenden Codeausschnitt hinzu `style.css` .  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Hinzufügen von Code zu Style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       Hinzufügen von Code zu `style.css`  
    :::image-end:::  
    
    Stellen Sie sicher, dass Sie ein externes Stylesheet erstellt haben. Ihr HTML-Code ist sich nicht bewusst, dass es vorhanden ist.  
    
1.  Öffnen Sie `index.html`.  
1.  Dem `<link rel="stylesheet" href="style.css">` HTML-Code hinzufügen.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link zu Style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       Link zu `style.css`  
    :::image-end:::  
    
1.  Öffnen `contact.html` Sie die Datei, und fügen Sie den Link dort hinzu.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link zu Style. CSS in contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Link zu `style.css` in `contact.html`  
    :::image-end:::  
    
1.  Wechseln Sie zur **Registerkarte Live**.  Auf der Startseite befindet sich nun die gleiche Schriftart wie im letzten Abschnitt und ein blauer Navigationsbereich.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Die Startseite" lightbox="../media/beginners-css-external10.msft.png":::
       Die Startseite  
    :::image-end:::  
    
1.  Wählen Sie den Link **Kontakt** aus, um zur Kontaktseite zu gelangen.  Die Seite "Kontakt" hat dieselbe Formatierung wie die Startseite.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-external11.msft.png":::
       Die Kontaktseite  
    :::image-end:::  
    
## Verwenden eines CSS-Frameworks  

**CSS-Frameworks** sind Sammlungen von Formatvorlagen, die von anderen Entwicklern erstellt wurden, die das Erstellen attraktiver Websites vereinfachen.  Anstatt selbst Formatvorlagen zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.  

1.  Kopieren Sie den folgenden Code:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Wechseln Sie zur Registerkarte Bearbeitung, und fügen Sie den Code in ein `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link zum Framework in contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Link zum Framework in `contact.html`  
    :::image-end:::  
    
1.  Öffnen `index.html` Sie die Datei, und fügen Sie den Code dort hinzu.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link zum Framework in index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Link zum Framework in `index.html`  
    :::image-end:::  
    
1.  Kehren Sie zur Registerkarte Live zurück, um Ihre Änderungen anzuzeigen.  Während die Hintergrundfarbe des `<nav>` Elements und die Schriftart der `<li>` `<a>` Elemente und identisch sind, hat sich die Schriftart der anderen Elemente geändert.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert" lightbox="../media/beginners-css-framework3.msft.png":::
       Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert  
    :::image-end:::  
    
### Verwenden einer Klasse  

Im letzten Abschnitt haben Sie Ihren Webseiten Bootstrap hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.  CSS-Frameworks helfen Ihnen, wichtige Änderungen an Ihrer Seite mit sehr wenig Code vorzunehmen.  Führen Sie die folgenden Aktionen aus, um die Kopfzeile zu ändern.  

1.  Kopieren Sie den folgenden Codeausschnitt.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Fügen Sie dem Tag in den vorherigen Codeausschnitt hinzu `<header>` `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Hinzufügen von Kursen in index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Hinzufügen von Klassen in `index.html`  
    :::image-end:::  
    
1.  Fügen Sie den Code zu Ihrem `<header>` Tag in hinzu `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Hinzufügen von Kursen in contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Hinzufügen von Klassen in `contact.html`  
    :::image-end:::  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  In der Kopfzeile befindet sich ein großes, graues Feld.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Die Kopfzeile hat nun ein großes, graues Feld um Sie herum" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       Die Kopfzeile hat nun ein großes, graues Feld um Sie herum  
    :::image-end:::  
    
### Grundlegendes zu Klassen  

Mit Klassen können Sie Auflistungen von Formatvorlagen beliebigen Elementen zuweisen.  Verwenden Sie den folgenden Codeausschnitt, um mehrere Formatvorlagen auf das Element anzuwenden, `<header>` nachdem Sie das `class` Attribut auf gesetzt haben `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Ein Vorteil einer Klasse besteht darin, dass Sie Formatvorlagen auf die gewünschten Elemente anwenden können.  Angenommen, Sie möchten die Hintergrundfarbe einiger `<p>` Elemente auf lila, aber nicht auf alle `<p>` Elemente einstellen.  Verwenden Sie den folgenden Codeausschnitt, um die Formatvorlage in einer Klasse zu definieren.  

```css
.custom-background {
  background-color: purple;
}
```  

Wenden Sie dann die Klasse nur auf die `<p>` Elemente an, die Sie formatieren möchten.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### Ausrichten von Elementen  

Führen Sie die folgenden Aktionen aus, um einen Bootstrap durchzuführen und Klassen zum Ausrichten von Elementen bereitzustellen.  

1.  Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie Sie `index.html` .  
1.  `class="container-fluid"`Zu Ihrem Tag hinzufügen `<body>` .  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Hinzufügen der Container-Fluid Klasse" lightbox="../media/beginners-css-align1.msft.png":::
       Hinzufügen der `container-fluid` Klasse  
    :::image-end:::  
    
1.  Umbrechen `<nav>` `<main>` von und Elementen in `<div class="row">` .  Stellen Sie sicher, dass Sie `</div>` `</main>` die neue Kategorie ordnungsgemäß schließen, um Sie zu beenden.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Hinzufügen einer Zeile" lightbox="../media/beginners-css-align2.msft.png":::
       Hinzufügen einer Zeile  
    :::image-end:::  
    
1.  Fügen Sie `class="col-3"` Ihrem `<nav>` Tag und `class="col-9"` Ihrem `<main>` Tag hinzu.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Hinzufügen der Klassen Col-3 und Col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Hinzufügen der `col-3` und- `col-9` Klassen  
    :::image-end:::  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt." lightbox="../media/beginners-css-align4.msft.png":::
       Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.  
    :::image-end:::  
    
## Nächste Schritte  

Herzlichen Glückwunsch, Sie haben es geschafft.  

*   Die beste Methode, um die Web-Entwicklung zu verbessern, besteht darin, weitere Websites zu erstellen.  Machen Sie sich keine Sorgen, wenn Sie etwas kaputt machen.  Machen Sie einfach Spaß und lernen Sie so viel wie möglich auf dem Weg.  
*   Weitere Informationen zum Formatieren von Webseiten finden Sie unter [Einführung in CSS][MDNCssFirstSteps].  
*   Weitere Informationen dazu, wie Sie devtools verwenden können, um mit dem CSS einer Seite zu experimentieren, finden Sie unter [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools für Anfänger: Erste Schritte mit HTML und dem Dom | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-gekocht-Amphibien | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "CSS-erste Schritte | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/css) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
