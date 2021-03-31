---
description: Erste Schritte mit CSS
title: 'DevTools für Anfänger: Erste Schritte mit CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 6a7135e144123917535e7c43e6a3cd608ec0c8a7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439437"
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

# <a name="devtools-for-beginners-get-started-with-css"></a>DevTools für Anfänger: Erste Schritte mit CSS  

In diesem Lernprogramm erfahren Sie, wie Sie css zum Formatieren einer Webseite verwenden.  Außerdem erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um mit CSS-Änderungen zu experimentieren.  

Der folgende Artikel ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in dem Sie die Grundlagen der Webentwicklung und Microsoft Edge DevTools lernen.  Sie erhalten praktische Erfahrung, indem Sie ihre eigene Website erstellen.  Sie müssen das erste Lernprogramm nicht abschließen, bevor Sie das zweite folgen.  [Das Einrichten des Codes zeigt,](#set-up-your-code) wie Sie eingerichtet werden.  

> [!NOTE]
> Dieses Lernprogramm ist für absolute Anfänger **** konzipiert und konzentriert sich sowohl auf die Grundlagen der Webentwicklung als auch auf die Grundlagen der Verwendung von DevTools zum Experimentieren mit CSS.  Wenn Sie ein Lernprogramm wünschen, das sich nur auf DevTools konzentriert, navigieren Sie zu Erste Schritte mit dem Anzeigen und Ändern [von CSS][DevtoolsCssIndex].  

Am Anfang des Lernprogramms sollte Ihre Website wie die folgende Abbildung aussehen.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Wie Ihre Website derzeit aussieht" lightbox="../media/beginners-css-intro1.msft.png":::
   Wie Ihre Website derzeit aussieht  
:::image-end:::  

Nachdem Sie das Lernprogramm abgeschlossen haben, sollte Ihre Website wie die folgende Abbildung aussehen.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Wie Ihre Website am Ende des Lernprogramms aussehen soll" lightbox="../media/beginners-css-intro2.msft.png":::
   Wie Ihre Website am Ende des Lernprogramms aussehen soll  
:::image-end:::  

## <a name="goals"></a>Ziele  

Folgen Sie diesem Lernprogramm, um die folgenden Konzepte und Aufgaben besser zu verstehen.  

*   Verwenden von CSS zum Formatieren einer Webseite.  
*   Verwenden von Microsoft Edge DevTools zum Experimentieren mit CSS.  
*   Der Unterschied zwischen CSS- und CSS-Frameworks.  

Sie erstellen eine echte Website.  

## <a name="prerequisites"></a>Voraussetzungen  

Bevor Sie dieses Lernprogramm versuchen, müssen Sie die folgenden Voraussetzungen erfüllen.  

*   Führen [Sie Erste Schritte mit HTML und dem DOM][DevtoolsBeginnersHtml] aus, oder stellen Sie sicher, dass Sie ein Verständnis von HTML und dom haben, ähnlich dem, was in diesem Lernprogramm vermittelt wird.  
*   Laden Sie den [Microsoft Edge-Webbrowser][MicrosoftEdgeInsider] herunter.  Im folgenden Lernprogramm wird eine Reihe von Webentwicklungstools verwendet, die als Microsoft Edge DevTools bezeichnet werden und in Microsoft Edge integrierte Sind.  

## <a name="set-up-your-code"></a>Einrichten des Codes  

Zum Erstellen Ihrer Website müssen Sie zunächst die folgenden Aktionen ausführen, um Ihren Code einrichten zu können.  

> [!NOTE]
> Wenn Sie das erste Lernprogramm in der Reihe bereits abgeschlossen haben, fahren Sie mit dem nächsten Abschnitt fort.  Verwenden Sie weiterhin Den Code aus dem letzten Lernprogramm, [Erste Schritte mit HTML und dem DOM][DevtoolsBeginnersHtml].  

1.  Öffnen Sie [den Quellcode][GlitchCookedAmphibianIndex].  Auf die Fokusregisterkarte Ihres Browsers wird als **Bearbeitungsregisterkarte verwiesen.**  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Registerkarte Bearbeiten" lightbox="../media/beginners-css-setup1.msft.png":::
       Registerkarte **"Bearbeiten"**  
    :::image-end:::  
    
1.  Wählen **Sie 4-amphibisch aus.**  Ein Menü wird angezeigt.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Das Menü Projektoptionen" lightbox="../media/beginners-css-setup2.msft.png":::
       Das Menü Projektoptionen  
    :::image-end:::  

1.  Wählen Sie **#A0 aus.**  Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.  
    
    > [!NOTE]
    > Glitch generiert einen zufälligen Namen für das neue Projekt.  
    
1.  Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**  Eine weitere Registerkarte wird mit einer Liveansicht Ihrer Website geöffnet.  Auf die Registerkarte "Fokus" Ihres Browsers wird als **Liveregisterkarte verwiesen.**  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Die Registerkarte Live" lightbox="../media/beginners-css-setup3.msft.png":::
       Die **Registerkarte Live**  
    :::image-end:::  

## <a name="understand-css"></a>Verstehen von CSS  

**CSS** ist eine Computersprache, die das Layout und formatieren von Webseiten bestimmt.  Die folgende Abbildung ist ein Absatz mit einem Rahmen.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Der Text wurde mit CSS formatiert" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Der Text wurde mit CSS formatiert  
:::image-end:::  

Der folgende Codeausschnitt ist der HTML- und CSS-Code, der zum Erstellen des Absatzes in der vorherigen Abbildung verwendet wird.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` sieht wahrscheinlich neu für Sie aus.  Der Rest sollte vertraut aussehen.  Falls nicht, führen Sie [Erste Schritte mit HTML und dem DOM][DevtoolsBeginnersHtml] aus, bevor Sie die folgenden Abschnitte versuchen.  

## <a name="add-inline-styles"></a>Hinzufügen von Inlineformatvorlagen  

Führen Sie die folgenden Aktionen aus, um **Inlineformatvorlagen zum** Anwenden von Formatvorlagen auf ein einzelnes Element zu verwenden.  

1.  Wechseln Sie zurück zur Bearbeitungsregisterkarte, und öffnen Sie `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Öffnen `index.html` auf der Bearbeitungsregisterkarte  
    :::image-end:::  
    
1.  Hinzufügen `style="background-color: aliceblue;"` zu Ihrer `<nav>` .  Im folgenden Codeblock ist die vierte Codezeile die, die Sie ändern müssen.  Der Rest ist einfach da, damit Sie sicherstellen können, dass Sie den neuen Code an der richtigen Stelle platzieren.  
    
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
    
1.  Navigieren Sie zur Registerkarte Live, um die **Änderungen anzeigen zu können.**  Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Die Hintergrundfarbe hinter den Links Start und Kontakt ist jetzt blau." lightbox="../media/beginners-css-inline2.msft.png":::
       Die Hintergrundfarbe hinter den **Links "Start"** **und** "Kontakt" ist jetzt blau.  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a>Erneutes Verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets  

In einem vorherigen Codeausschnitt hat ein Inlineformat auf ein einzelnes Tag eine `<p>` Formatvorlage angewendet.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Was passiert, wenn alle Elemente auf Ihrer Webseite auf die `<p>` gleiche Weise gestaltet werden sollen?  Sie müssen den Code kopieren und in jedes einzelne `<p>` Tag auf Ihrer Website einfügen.  Das ist viel Zeit und Aufwand.  Und wenn Sie eine Bearbeitung erstellen müssen, müssen Sie jedes Tag erneut ändern.  Führen Sie die folgenden Aktionen aus, um ein **internes Stylesheet zu** verwenden, um Ihre CSS einmal so zu schreiben, dass sie auf mehrere Elemente angewendet wird.  

1.  Klicken Sie auf der Registerkarte Live auf **Kontakt,** um zur Kontaktseite zu navigieren.  Beachten Sie die Schriftart **von Home** und **Contact**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Die Seite Kontakt" lightbox="../media/beginners-css-internal1.msft.png":::
       Die Seite "Kontakt"  
    :::image-end:::  
    
1.  Öffnen Sie **auf der Registerkarte Editor** `contact.html` .  
1.  Fügen Sie den folgenden Code zu `contact.html` hinzu.  Denken Sie daran, dass die Zeilen, die mit beginnen und mit `<style>` `</style>` enden, das sind, was Sie hinzufügen müssen.  Der andere Code ist nur da, damit Sie wissen, wo sie den neuen Code setzen.  
    
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
    
1.  Wechseln Sie zurück zur **Registerkarte Live.**  
1.  Wählen **Sie Kontakt** aus, um zur Kontaktseite zurück zu wechseln.  Die Schriftart von **Home** und **Contact** hat sich geändert.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Die Schriftart der Links Start und Kontakt wurde geändert." lightbox="../media/beginners-css-internal2.msft.png":::
       Die Schriftart der **Links "Start"** und **"Kontakt"** wurde geändert.  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a>Verstehen interner Stylesheets  

Interne Stylesheets wenden Formatvorlagen mithilfe **von Selektoren an.**  Selektoren sind Muster, die auf ein oder mehrere HTML-Elemente angewendet werden können.  Im vorherigen Codeausschnitt wurde die folgende Formatvorlage hinzugefügt.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` ist ein Selektor, der in "jedes `<li>` Element, das ein Element `<a>` enthält" übersetzt wird.  Der Browser ändert die Schriftart der Links **"Start"** und **"Kontakt",** da jede Taggruppe dem Muster entspricht.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` ist eine **Deklaration**.  Eine Deklaration besteht aus den folgenden beiden Teilen.  

:::row:::
   :::column span="1":::
      **property**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      Die Eigenschaft beschreibt eine allgemeine Möglichkeit, die Formatvorlage des Elements zu ändern.  
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

Gibt dem Browser beispielsweise die folgende Anweisung: "Legen Sie die Schriftart von Elementen `font-family: 'Courier New', Courier, serif` fest, die mit dem Muster `li a` übereinstimmen auf `'Courier New'` .  Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .  Wenn dies nicht verfügbar ist, verwenden Sie `serif` ."  

### <a name="add-multiple-selectors-to-a-ruleset"></a>Hinzufügen mehrerer Selektoren zu einem Regelsatz  

Ein Block von CSS-Code wie der folgende Codeausschnitt wird als **Regelsatz bezeichnet.**  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Führen Sie die folgenden Aktionen aus, um Kommas zum Hinzufügen mehrerer Selektoren zu einem Regelsatz zu verwenden.  

1.  Öffnen Sie **auf der Registerkarte Editor** `contact.html` .  
1.  Nach `li a` dem Typ `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    Der vorherige Codeausschnitt weist den Browser an, Elemente auf die gleiche Weise zu formatieren wie `<h1>` Elemente, die mit dem Muster `li a` übereinstimmen.  
    
1.  Navigieren Sie zur **Registerkarte Live**.  
1.  Wählen Sie den **Link Kontakt** aus, um zur Kontaktseite zurück zu wechseln.  Wenden Sie sich **jetzt an mich!** hat dieselbe Schriftart wie die Navigationslinks.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Der Text Contact Me!  hat jetzt die gleiche Schriftart wie die Links Start und Kontakt" lightbox="../media/beginners-css-multiple1.msft.png":::
       Der Text **Contact Me!** hat jetzt die gleiche Schriftart wie die **Links "Start"** **und "Kontakt"**  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a>Experimentieren mit DevTools  

Wenn Sie ihre Reise fortsetzen, um ein Experte für Webentwicklung zu werden, ist CSS möglicherweise kompliziert.  Sie können css schreiben und erwarten, dass es auf eine Weise angezeigt wird, aber der Browser macht etwas völlig anderes.  Microsoft Edge DevTools erleichtert das Experimentieren mit Änderungen und zeigt sofort an, wie sich die Änderungen auf die Seite auswirken.  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a>Hinzufügen einer Deklaration zu einem vorhandenen Regelt in DevTools  

Führen Sie die folgenden Aktionen aus, um die Formatvorlage eines vorhandenen Elements zu iterieren, fügen Sie einem vorhandenen Regelsatz eine Deklaration hinzu.  

1.  Zeigen Sie auf **den Startlink,** öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Überprüfen aus.**  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Überprüfen des Links Start" lightbox="../media/beginners-css-add1.msft.png":::
       Überprüfen des Links "Start"  
    :::image-end:::  
    
    DevTools wird neben Ihrer Seite geöffnet.  Der Code, der den Startlink darstellt, ist in der `<a href="/">Home</a>` DOM-Struktur blau hervorgehoben.  Der Codeausschnitt und die Vorschau sollten in Erste Schritte mit HTML und [dem DOM vertraut sein.][DevtoolsBeginnersHtml]  
    
    :::row:::
       :::column span="":::
          In der folgenden Abbildung wird die zuvor hinzugefügte Deklaration auf der `font-family: 'Courier New', Courier, serif` `contact.html` Registerkarte **Formatvorlagen** unterhalb der DOM-Struktur angezeigt.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Die Registerkarte Formatvorlagen befindet sich unterhalb der DOM-Struktur." lightbox="../media/beginners-css-add2.msft.png":::
             Die **Registerkarte Formatvorlagen** befindet sich unterhalb der DOM-Struktur.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Wenn Ihr DevTools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Die Registerkarte Formatvorlagen befindet sich rechts neben der DOM-Struktur." lightbox="../media/beginners-css-add3.msft.png":::
             Die **Registerkarte Formatvorlagen** befindet sich rechts neben der DOM-Struktur.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen Sie unten die leere Zeile `font-family: 'Courier New', Courier, Serif` aus, um eine neue Deklaration hinzuzufügen.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Hinzufügen einer neuen Deklaration" lightbox="../media/beginners-css-add4.msft.png":::
       Hinzufügen einer neuen Deklaration  
    :::image-end:::  
    
1.  Geben `color` Sie ein, und wählen Sie `Enter` aus.  Die Benutzeroberfläche für die automatische Vervollständigung schlägt Bei der Eingabe Optionen vor.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Typfarbe" lightbox="../media/beginners-css-add5.msft.png":::
       Typ `color`  
    :::image-end:::  
    
1.  Geben `magenta` Sie ein, und wählen Sie `Enter` aus.  Der ganze Text auf der Kontaktseite ist jetzt Magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Typ Magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Typ `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a>Bearbeiten einer Deklaration in DevTools  

Führen Sie die folgenden Aktionen aus, um vorhandene Deklarationen in DevTools zu bearbeiten.  

1.  Wählen Sie das magentafarbene Quadrat neben `magenta` aus.  Eine Farbauswahl wird angezeigt.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Die Farbauswahl" lightbox="../media/beginners-css-edit1.msft.png":::
       Die Farbauswahl  
    :::image-end:::  
    
1.  Verwenden Sie die Farbauswahl, um den Schrifttext in eine Farbe zu ändern, die Ihnen gefällt.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Ändern der Schriftfarbe in Lila mit der Farbauswahl" lightbox="../media/beginners-css-edit2.msft.png":::
       Ändern der Schriftfarbe in Lila mit der Farbauswahl  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a>Hinzufügen eines neuen Regelsets in DevTools  

Führen Sie die folgenden Aktionen aus, um neue Regelsätze in DevTools hinzuzufügen.  

1.  Wählen **Sie Neue Formatvorlageregel** \( ![ Neue Formatregel ](../media/new-style-rule-icon.msft.png) \) aus, die sich neben **CLS befindet.**  Als Auswahl wird ein leeres `a` Regelset angezeigt.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Hinzufügen einer neuen Regel" lightbox="../media/beginners-css-rule1.msft.png":::
       Hinzufügen einer neuen Regel  
    :::image-end:::  
    
1.  Ersetzen Sie `a` durch `a:hover`.  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Ersetzen sie durch a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Ersetzen `a` durch `a:hover`  
    :::image-end:::  
    
    `:hover` ist eine **Pseudoklasse**.  Verwenden Sie Pseudoklassen für Stilelemente, die spezielle Zustände eingeben können.  Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie mit dem Mauszeiger auf ein Element `<a>` zeigen.  
    
1.  Wählen Sie zwischen den Klammern aus, um eine neue Deklaration hinzuzufügen.  
1.  Geben `background-color` Sie den Deklarationsnamen ein, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Geben Sie Hintergrundfarbe ein" lightbox="../media/beginners-css-rule3.msft.png":::
       Typ `background-color`  
    :::image-end:::  
    
1.  Geben `green` Sie den Deklarationswert ein, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Typ grün" lightbox="../media/beginners-css-rule4.msft.png":::
       Typ `green`  
    :::image-end:::  
    
1.  Zeigen Sie mit der Maus über den **Startlink.**  Der Hintergrund des Links wird grün.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Zeigen Sie auf den Startlink, um den grünen Hintergrund zu zeigen." lightbox="../media/beginners-css-rule5.msft.png":::
       Zeigen Sie auf den Startlink, um den grünen Hintergrund zu zeigen.  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a>Erneutes Verwenden von Formatvorlagen über Seiten hinweg mit externen Stylesheets  

In einem vorherigen Schritt haben Sie den folgenden Codeausschnitt als internes Stylesheet zu `contact.html` hinzugefügt.  

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

Was passiert, wenn Sie die gleiche `index.html` Art und Weise formatieren möchten?  Was passiert, wenn Sie eine große Anzahl von Seiten hatten, auf die Sie Ihre Formatvorlagen anwenden wollten?  Sie müssen das interne Stylesheet kopieren und in jede einzelne Webseite auf Ihrer Website einfügen.  Führen Sie die folgenden Aktionen aus, um ein **externes Stylesheet** hinzuzufügen, damit Sie Ihre CSS einmal schreiben und auf mehrere Seiten anwenden können.  

1.  Aktualisieren Sie zunächst die Registerkarte Live, um die Änderungen zu entfernen, die Sie in DevTools vorgenommen haben.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Nachdem Sie die Seite aktualisiert haben, sind die In DevTools vorgenommenen Änderungen nicht mehr verfügbar." lightbox="../media/beginners-css-external1.msft.png":::
        Nachdem Sie die Seite aktualisiert haben, sind die In DevTools vorgenommenen Änderungen nicht mehr verfügbar.  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor, und** öffnen Sie `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Löschen Sie alles zwischen `<style>` und , einschließlich und `</style>` `<style>` `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Das Styletag wurde entfernt." lightbox="../media/beginners-css-external3.msft.png":::
       Das Styletag wurde entfernt.  
    :::image-end:::  
    
1.  Öffnen `index.html` und entfernen Sie das `style="background-color: aliceblue;"` `<nav>` Tag.  Sie haben nun alle CSS entfernt, die Sie ihrer Website zuvor hinzugefügt haben.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Die Inlineformatvorlage wurde aus dem Navigationselement entfernt." lightbox="../media/beginners-css-external4.msft.png":::
       Die Inlineformatvorlage wurde aus dem Navigationselement entfernt.  
    :::image-end:::  
    
1.  Wählen **Sie Neue Datei aus.**  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Das Dialogfeld neue Datei" lightbox="../media/beginners-css-external5.msft.png":::
       Das Dialogfeld neue Datei  
    :::image-end:::  
    
1.  Ersetzen `cool-file.js` Sie `style.css` durch, und wählen Sie Datei hinzufügen **aus.**  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style.css" lightbox="../media/beginners-css-external6.msft.png":::
       Typ `style.css`  
    :::image-end:::  
    
1.  Fügen Sie der Datei den folgenden Codeausschnitt `style.css` hinzu.  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Hinzufügen von Code zu style.css" lightbox="../media/beginners-css-external7.msft.png":::
       Hinzufügen von Code zu `style.css`  
    :::image-end:::  
    
    Stellen Sie sicher, dass Sie ein externes Stylesheet erstellt haben. Ihre HTML ist sich nicht bewusst, dass sie vorhanden ist.  
    
1.  Öffnen Sie `index.html`.  
1.  Fügen `<link rel="stylesheet" href="style.css">` Sie Zu Ihrem HTML hinzu.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link zu style.css" lightbox="../media/beginners-css-external8.msft.png":::
       Link zu `style.css`  
    :::image-end:::  
    
1.  Öffnen Sie `contact.html` die Datei, und fügen Sie den Link dort hinzu.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link zu style.css in contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Link zu `style.css` in `contact.html`  
    :::image-end:::  
    
1.  Navigieren Sie zur **Registerkarte Live**.  Die Startseite hat nun die gleiche Schriftart aus dem letzten Abschnitt und einen blauen Navigationsbereich.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Die Homepage" lightbox="../media/beginners-css-external10.msft.png":::
       Die Homepage  
    :::image-end:::  
    
1.  Wählen Sie den **Link Kontakt** aus, um zur Kontaktseite zu navigieren.  Die Kontaktseite hat die gleiche Formatierung wie die Homepage.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Die Kontaktseite" lightbox="../media/beginners-css-external11.msft.png":::
       Die Kontaktseite  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a>Verwenden eines CSS-Frameworks  

**CSS-Frameworks** sind Von anderen Entwicklern erstellte Stilsammlungen, die das Erstellen attraktiver Websites vereinfachen.  Anstatt Formatvorlagen selbst zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.  

1.  Kopieren Sie den folgenden Code:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Öffnen Sie die Bearbeitungsregisterkarte, und fügen Sie den Code in `contact.html` ein.  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link zum Framework in contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Link zum Framework in `contact.html`  
    :::image-end:::  
    
1.  Öffnen Sie `index.html` die Datei, und fügen Sie den Code dort hinzu.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link zum Framework in index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Link zum Framework in `index.html`  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur Registerkarte Live, um Ihre Änderungen zu sehen.  Während die Hintergrundfarbe des Elements und die Schriftart der und-Elemente identisch sind, hat sich die Schriftart `<nav>` `<li>` der anderen Elemente `<a>` geändert.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Einige Schriftarten auf der Startseite wurden aufgrund des Frameworks geändert." lightbox="../media/beginners-css-framework3.msft.png":::
       Einige Schriftarten auf der Startseite wurden aufgrund des Frameworks geändert.  
    :::image-end:::  
    
### <a name="use-a-class"></a>Verwenden einer Klasse  

Im letzten Abschnitt haben Sie Bootstrap zu Ihren Webseiten hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.  MIT CSS-Frameworks können Sie wichtige Änderungen an Ihrer Seite mit sehr wenig Code vornehmen.  Führen Sie die folgenden Aktionen aus, um den Header zu ändern.  

1.  Kopieren Sie den folgenden Codeausschnitt.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Fügen Sie dem Tag in den vorherigen `<header>` Codeausschnitt `index.html` hinzu.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Hinzufügen von Klassen in index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Hinzufügen von Klassen in `index.html`  
    :::image-end:::  
    
1.  Fügen Sie den Code zu Ihrem `<header>` Tag in `contact.html` hinzu.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Hinzufügen von Klassen in contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Hinzufügen von Klassen in `contact.html`  
    :::image-end:::  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte Live an.  Es gibt ein großes, graues Feld um ihre Kopfzeile.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Der Header hat jetzt ein großes, graues Feld um ihn herum." lightbox="../media/beginners-css-jumbotron3.msft.png":::
       Der Header hat jetzt ein großes, graues Feld um ihn herum.  
    :::image-end:::  
    
### <a name="understand-classes"></a>Verstehen von Klassen  

Mit Klassen können Sie Beliebigen Elementen Auflistungen von Formatvorlagen zuweisen.  Verwenden Sie den folgenden Codeausschnitt, um mehrere Formatvorlagen auf das Element `<header>` anzuwenden, nachdem Sie das `class` Attribut auf festgelegt `jumbotron` haben.  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Ein Vorteil einer Klasse besteht in der Möglichkeit, Formatvorlagen auf alle elemente anzuwenden, die Sie möchten.  Angenommen, Sie möchten die Hintergrundfarbe einiger Elemente auf Lila festlegen, aber `<p>` nicht auf alle `<p>` Elemente.  Verwenden Sie den folgenden Codeausschnitt, um die Formatvorlage in einer Klasse zu definieren.  

```css
.custom-background {
  background-color: purple;
}
```  

Wenden Sie als Nächstes die Klasse nur auf die `<p>` Elemente an, die Sie formaten möchten.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a>Ausrichten von Elementen  

Führen Sie die folgenden Aktionen zum Bootstrapen aus und stellen Sie Klassen zum Ausrichten von Elementen zur Verfügung.  

1.  Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie `index.html` .  
1.  Hinzufügen `class="container-fluid"` zu Ihrem `<body>` Tag.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Hinzufügen der Container-Fluid-Klasse" lightbox="../media/beginners-css-align1.msft.png":::
       Hinzufügen der `container-fluid` Klasse  
    :::image-end:::  
    
1.  `<nav>`Umschließen Sie Ihre und `<main>` -Elemente in `<div class="row">` .  Stellen Sie sicher, dass `</div>` Sie `</main>` nach, um das neue Tag ordnungsgemäß zu schließen.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Hinzufügen einer Zeile" lightbox="../media/beginners-css-align2.msft.png":::
       Hinzufügen einer Zeile  
    :::image-end:::  
    
1.  Fügen `class="col-3"` Sie Ihrem Tag und Ihrem Tag `<nav>` `class="col-9"` `<main>` hinzu.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Hinzufügen der Klassen col-3 und col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Hinzufügen der `col-3` `col-9` Und-Klassen  
    :::image-end:::  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte Live an.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Der Navigationsinhalt befindet sich jetzt links vom Hauptinhalt" lightbox="../media/beginners-css-align4.msft.png":::
       Der Navigationsinhalt befindet sich jetzt links vom Hauptinhalt  
    :::image-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

Herzlichen Glückwunsch, Sie sind fertig.  

*   Die beste Möglichkeit, die Webentwicklung zu verbessern, ist das Erstellen von weiteren Websites.  Machen Sie sich keine Gedanken über das Brechen von Zeug.  Machen Sie einfach Spaß und lernen Sie so viel wie möglich auf dem Weg.  
*   Weitere Informationen zum Formatieren von Webseiten finden Sie unter [Einführung in CSS][MDNCssFirstSteps].  
*   Weitere Informationen zur Verwendung von DevTools zum Experimentieren mit dem CSS einer Seite finden Sie unter Erste Schritte mit dem Anzeigen und Ändern [von CSS][DevtoolsCssIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "Entwicklungstools für Einsteiger: Erste Schritte mit HTML und dem DOM | Microsoft-Dokumentation"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - 4-amphibische | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Erste Schritte für css | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/beginners/css) wird von [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
