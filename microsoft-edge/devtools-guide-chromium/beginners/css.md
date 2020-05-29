---
title: DevTools für Anfänger
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0064f0427b6bd5689e888cccfe2c650492898bb2
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581594"
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

Dies ist das zweite Lernprogramm in einer Reihe von Lernprogrammen, in denen Sie die Grundlagen der Webentwicklung und der Microsoft Edge-devtools.  Sie erhalten praktische Erfahrungen, wenn Sie tatsächlich ihre eigene Website erstellen.  Bevor Sie diesen Vorgang ausführen, müssen Sie das erste Lernprogramm nicht ausführen.  Sie können hier beginnen.  [Einrichten Ihres Codes](#set-up-your-code) zeigt, wie Sie sich einrichten.  

> [!NOTE]
> Dieses Lernprogramm ist für absolute Anfänger konzipiert und konzentriert sich sowohl auf die **Grundlagen der Webentwicklung** als auch auf die Grundlagen der Verwendung von devtools zum Experimentieren mit CSS.  Wenn Sie ein Lernprogramm benötigen, das sich nur auf devtools konzentriert, lesen Sie [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsCssIndex].  

Ihre Website sieht derzeit wie folgt aus:  

> ##### Abbildung1  
> Wie Ihre Website aktuell aussieht  
> ![Wie Ihre Website aktuell aussieht][ImageCssIntro1]  

Nach Abschluss des Lernprogramms sieht es wie folgt aus:  

> ##### Abbildung2  
> Wie Ihre Website am Ende des Lernprogramms aussehen wird  
> ![Wie Ihre Website am Ende des Lernprogramms aussehen wird][ImageCssIntro2]  

## Ziele   

Am Ende dieses Lernprogramms können Sie Folgendes verstehen:  

*   Verwenden von CSS zum Formatieren einer Webseite  
*   Verwenden von Microsoft Edge devtools zum Experimentieren mit CSS  
*   Der Unterschied zwischen CSS-und CSS-Frameworks.  

Sie haben auch eine echte Website!  

## Voraussetzungen   

Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus:  

*   Führen Sie [die ersten Schritte mit HTML und dem Dom durch][DevToolsBeginnersHtml] , oder stellen Sie sicher, dass Sie ein Verständnis von HTML und dem Dom haben, das dem entspricht, was in diesem Lernprogramm unterrichtet wird.  
*   Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.  In diesem Lernprogramm wird eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, verwendet, die in Microsoft Edge integriert sind.  

## Einrichten Ihres Codes   

Um mit der Erstellung Ihrer Website zu beginnen, müssen Sie Ihren Code einrichten:  

1.  **Wenn Sie das erste Lernprogramm in dieser Serie bereits abgeschlossen haben, überspringen Sie diesen Abschnitt!  Verwenden Sie weiterhin ihren Code aus dem letzten Lernprogramm, [Erste Schritte mit HTML und dem Dom][DevToolsBeginnersHtml].**  
1.  Öffnen Sie den [Quellcode][GlitchCookedAmphibianIndex].  Diese Registerkarte Ihres Browsers wird als **Registerkarte "Bearbeiten"** bezeichnet.  
    
    > ##### Abbildung 3  
    > Die Registerkarte ' bearbeiten '  
    > ![Die Registerkarte ' bearbeiten '][ImageCssSetup1]  
    
1.  Klicken Sie auf **gekocht-Amphibien**.  Ein Menü wird eingeblendet.  
    
    > ##### Abbildung4  
    > Das Menü "Projektoptionen"  
    > ![Das Menü "Projektoptionen"][ImageCssSetup2]  

1.  Klicken Sie auf **Remix Project**.  Glitch erstellt eine Kopie des Projekts, das Sie bearbeiten können.  
    
    > [!NOTE]
    > Glitch generiert einen zufälligen Namen für das neue Projekt.  
    
1.  Klicken Sie auf **anzeigen** , und wählen Sie **in einem neuen Fenster**aus.  Eine andere Registerkarte wird mit einer Live Ansicht Ihrer Website geöffnet.  Dieser Reiter Ihres Browsers wird als **"Live"-Reiter**bezeichnet.  
    
    > ##### Abbildung5  
    > Die Registerkarte "Live"  
    > ![Die Registerkarte "Live"][ImageCssSetup3]  

## Grundlegendes zu CSS   

**CSS** ist eine Computersprache, die das Layout und die Gestaltung von Webseiten bestimmt.  Hier ist beispielsweise ein Absatz mit einem Rahmen:  

> ##### Abbildung6  
> Dies wurde mit CSS formatiert  
> ![Dies wurde mit CSS formatiert][ImageCssStyled]  

Hier ist der HTML-und CSS-Code, der zum Erstellen dieses Absatzes verwendet wird:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` sieht Ihnen vielleicht neu aus.  Der andere sollte vertraut aussehen.  Wenn dies nicht der Fall ist, [beginnen Sie mit HTML und dem Dom][DevToolsBeginnersHtml] , bevor Sie dieses Lernprogramm durchführen.  

## Hinzufügen von Inlineformatvorlagen   

Verwenden Sie **Inlineformatvorlagen** , wenn Sie Formatvorlagen auf ein einzelnes Element anwenden möchten.  Probieren Sie es jetzt aus:  

1.  Wechseln Sie zurück zur Registerkarte Bearbeitung, und öffnen Sie Sie `index.html` .  
    
    > ##### Abbildung7  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  `style="background-color: aliceblue;"`Zu ihrer hinzufügen `<nav>` .  Im Code-Block unten ist die vierte Codezeile diejenige, die Sie ändern müssen.  Der andere ist nur da, damit Sie sicher sein können, dass Sie den neuen Code an die richtige Stelle setzen.  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  Wechseln Sie zum **Reiter "Live"** , um die Änderungen anzuzeigen!  Der Hintergrund des `<nav>` Abschnitts ist jetzt blau.  
    
    > ##### Abbildung8  
    > Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau  
    > ![Die Hintergrundfarbe hinter dem Start-und Kontakt Link ist jetzt blau][ImageCssInline2]  

## Wieder verwenden von Formatvorlagen auf einer einzelnen Seite mit internen Stylesheets   

Zuvor haben Sie eine Inlineformatvorlage gesehen, die eine Formatvorlage auf eine einzelne `<p>` Kategorie wie die folgende angewendet hat:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Was ist, wenn Sie möchten, dass alle `<p>` Elemente auf Ihrer Webseite auf die gleiche Weise formatiert werden?  Sie müssten den Code in jeder einzelnen `<p>` Kategorie auf Ihrer Website kopieren und einfügen.  Das ist viel Zeit und Mühe.  Und wenn Sie eine Bearbeitung vornehmen mussten, müssten Sie jedes Tag erneut ändern.  Mit **internen Stylesheets** können Sie Ihr CSS einmal schreiben, damit es auf mehrere Elemente angewendet wird.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf der Registerkarte Live auf **Kontakt** , um zur Kontaktseite zu gelangen.  Beachten Sie die Schriftart für " **Privat** " und " **Kontakt**".  
    
    > ##### Abbildung 9  
    > Die Kontaktseite  
    > ![Die Kontaktseite][ImageCssInternal1]  

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
1.  Klicken Sie auf **Kontakt** , um zur Kontaktseite zurückzukehren.  Die Schriftart von " **Start** " und " **Kontakt** " hat sich geändert.  
    
    > ##### Abbildung 10  
    > Die Schriftart der Links für "Start" und "Kontakt" wurde geändert.  
    > ![Die Schriftart der Links für "Start" und "Kontakt" wurde geändert.][ImageCssInternal2]  
    
### Grundlegendes zu internen Stylesheets   

Interne Stylesheets wenden Formatvorlagen mithilfe von **Auswahlen**an.  Auswahlen sind Muster, die möglicherweise für ein oder mehrere HTML-Elemente gelten.  Im vorherigen Codebeispiel:  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` ist eine Auswahl, die in "Any" übersetzt wird, `<li>` die eine enthält `<a>` .  Der Browser ändert die Schriftart der Links **Home** und **Contact** , da diese dem Muster entsprechen.  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` ist eine **Deklaration**.  Eine Deklaration besteht aus zwei Teilen: einer **Eigenschaft** und einem **Wert**.  `font-family` ist die Eigenschaft und `'Courier New', Courier, serif` der Wert dieser Eigenschaft.  Die Eigenschaft beschreibt eine allgemeine Möglichkeit, die Art des Elements zu ändern, und der Wert gibt an, wie genau es geändert werden soll.  Gibt beispielsweise `font-family: 'Courier New', Courier, serif` dem Browser folgende Anweisung aus: "die Schriftart von Elementen, die dem Muster entsprechen, auf festzulegen `li a` `'Courier New'` .  Wenn diese Schriftart nicht verfügbar ist, verwenden Sie `Courier` .  Wenn dies nicht möglich ist, verwenden Sie `serif` . "  

### Hinzufügen mehrerer Auswahlen zu einem RuleSet   

Ein Block mit CSS-Code wie dem, was unten angezeigt wird, wird als **RuleSet**bezeichnet.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Verwenden Sie Kommas, um einem RuleSet mehrere Auswahlen hinzuzufügen.  Probieren Sie es jetzt aus:  

1.  Öffnen Sie auf der **Registerkarte Editor den Reiter** `contact.html` .  
1.  Nach `li a` Typ `, h1` .  

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

    Dadurch wird der Browser so formatiert, `<h1>` dass er Elemente auf die gleiche Weise anweist wie Elemente, die dem Muster entsprechen `li a` .  
    
1.  Wechseln Sie zur **Registerkarte Live**.  
1.  Klicken Sie auf den Link **Kontakt** , um zur Kontaktseite zurückzukehren.  **Kontaktieren Sie mich jetzt!** hat die gleiche Schriftart wie die Navigationslinks.  
    
    > ##### Abbildung 11  
    > Der Text "Kontakt!" hat nun dieselbe Schriftart wie die Links für "Privat" und "Kontakt"  
    > ![Der Text kontaktiere mich!  hat nun dieselbe Schriftart wie die Links für "Privat" und "Kontakt"][ImageCssMultiple1]  

## Experimentieren mit devtools   

Wenn Sie Ihre Reise in die Master-Webentwicklung fortsetzen, werden Sie feststellen, dass CSS schwierig sein kann.  Sie schreiben einige CSS-Daten und erwarten, dass Sie auf eine Art und Weise angezeigt werden, doch der Browser hat etwas völlig anderes.  Microsoft Edge devtools macht es einfach, mit Änderungen zu experimentieren und sofort zu sehen, wie sich diese Änderungen auf die Seite auswirken.  

### Hinzufügen einer Deklaration zu einem vorhandenen rulet-Element in devtools   

Wenn Sie die Formatvorlage eines vorhandenen Elements durchlaufen möchten, fügen Sie eine Deklaration zu einem vorhandenen RuleSet hinzu.  Probieren Sie es jetzt aus:  

1.  Klicken Sie mit der rechten Maustaste auf den Link **Start** , und wählen Sie über **prüfen**aus.  
    
    > ##### Abbildung 12  
    > Überprüfen des Start Links  
    > ![Überprüfen des Start Links][ImageCssAdd1]  
    
    DevTools wird neben ihrer Seite geöffnet.  Der Code, der den Link "Start" darstellt, `<a href="/">Home</a>` wird in der DOM-Struktur blau hervorgehoben.  Dies sollte aus den ersten [Schritten mit HTML und dem Dom][DevToolsBeginnersHtml]vertraut sein.  Auf der Registerkarte **Formatvorlagen** unterhalb der DOM-Struktur können Sie die `font-family: 'Courier New', Courier, serif` Deklaration sehen, die Sie zuvor hinzugefügt haben `contact.html` .  
    
    > ##### Abbildung 13  
    > Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur.  
    > ![Die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur.][ImageCssAdd2]  
    
    Wenn Ihr devtools-Fenster breit ist, befindet sich die Registerkarte Formatvorlagen rechts neben der DOM-Struktur.  
    
    > ##### Abbildung 14  
    > Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur.  
    > ![Die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur.][ImageCssAdd3]  
    
1.  Klicken Sie unten auf das Leerzeichen `font-family: 'Courier New', Courier, Serif` , um eine neue Deklaration hinzuzufügen.  
    
    > ##### Abbildung 15  
    > Hinzufügen einer neuen Deklaration  
    > ![Hinzufügen einer neuen Deklaration][ImageCssAdd4]  
    
1.  Geben `color` Sie ein, und drücken Sie dann `Enter` .  Die AutoVervollständigen-Benutzeroberfläche schlägt Optionen während der Eingabe vor.  
    
    > ##### Abbildung 16  
    > Tippen `color`  
    > ![Eingeben von Farben][ImageCssAdd5]  

1.  Geben `magenta` Sie ein, und drücken Sie dann `Enter` erneut.  Der gesamte Text auf der Kontaktseite ist jetzt Magenta.  
    
    > ##### Abbildung 17  
    > Tippen `magenta`  
    > ![Eingeben von Magenta][ImageCssAdd6]  
    
### Bearbeiten einer Deklaration in devtools   

Sie können auch vorhandene Deklarationen in devtools bearbeiten.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf das Magenta-Quadrat neben `magenta` .  Eine Farbauswahl wird eingeblendet.  
    
    > ##### Abbildung 18  
    > Die Farbauswahl  
    > ![Die Farbauswahl][ImageCssEdit1]  
    
1.  Verwenden Sie die Farbauswahl, um den Schriftart Text in eine Farbe zu ändern, die Ihnen gefällt.  
    
    > ##### Abbildung 19  
    > Ändern der Schriftfarbe in Lila mit der Farbauswahl  
    > ![Ändern der Schriftfarbe in Lila mit der Farbauswahl][ImageCssEdit2]  

### Hinzufügen eines neuen RuleSets in devtools   

Sie können auch neue RuleSets in devtools hinzufügen.  Probieren Sie es jetzt aus:  

1.  Klicken Sie auf **neue** Stilregel Regel ![ ][ImageNewStyleRuleIcon] , die sich neben **CLS**befindet.  Ein leerer RuleSet wird `a` als Auswahl angezeigt.  
    
    > ##### Abbildung 20  
    > Hinzufügen einer neuen Regel  
    > ![Hinzufügen einer neuen Regel][ImageCssRule1]  
    
1.  Ersetzen Sie `a` durch `a:hover`.  
    
    > ##### Abbildung 21  
    > Ersetzen `a` durch `a:hover`  
    > ![Ersetzen eines durch a:hover][ImageCssRule2]  
    
    `:hover` ist eine **Pseudoklasse**.  Verwenden Sie Pseudoklassen, um Elemente zu formatieren, wenn Sie spezielle Zustände eingeben.  Beispielsweise wird die `a:hover` Formatvorlage nur wirksam, wenn Sie auf ein Element zeigen `<a>` .  
    
1.  Klicken Sie zwischen den Klammern, um eine neue Deklaration hinzuzufügen.  
1.  Geben `background-color` Sie den Namen der Deklaration ein, und drücken Sie dann `Enter` .  
    
    > ##### Abbildung 22  
    > Tippen `background-color`  
    > ![Hintergrundfarbe eingeben][ImageCssRule3]  
    
1.  Geben `green` Sie für den Deklarations Wert ein, und drücken Sie dann `Enter` .  
    
    > ##### Abbildung 23  
    > Tippen `green`  
    > ![Eingeben von grün][ImageCssRule4]  
    
1.  Zeigen Sie mit der Maus auf den Link " **Start** ".  Der Hintergrund des Links wird grün.  
    
    > ##### Abbildung 24  
    > Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen  
    > ![Zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen][ImageCssRule5]  
    
## Wieder verwenden von Formatvorlagen auf mehreren Seiten mit externen Stylesheets   

Zuvor haben Sie dieses interne Stylesheet hinzugefügt `contact.html` :  

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

Was ist, wenn Sie `index.html` die gleiche Weise formatieren möchten?  Was ist, wenn Sie mehr als *tausend* Seiten haben und diese Formatvorlagen auf alle anwenden möchten?  Sie müssen dieses interne Stylesheet in jede einzelne Webseite auf Ihrer Website kopieren und einfügen.  Mit **externen Stylesheets** können Sie Ihren CSS-Eintrag noch einmal auf mehrere Seiten anwenden.  Probieren Sie es jetzt aus:  

1.  Laden Sie zunächst die Registerkarte "Live" neu, um die Änderungen zu entfernen, die Sie in devtools vorgenommen haben.  
    
    > ##### Abbildung 25  
    >  Nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.  
    > ![ Nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden.][ImageCssExternal01]  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor** , und öffnen Sie Sie `contact.html` .  
    
    > ##### Abbildung 26  
    > `contact.html`  
    > ![Contact. html][ImageCssExternal02]  
    
1.  Löschen Sie alles zwischen `<style>` und `</style>` , einschließlich `<style>` und `</style>` .  
    
    > ##### Abbildung 27  
    > Das Stil-Tag wurde entfernt  
    > ![Das Stil-Tag wurde entfernt][ImageCssExternal03]  
    
1.  Wechseln Sie zu `index.html` der Kategorie, und entfernen Sie Sie `style="background-color: aliceblue;"` `<nav>` .  Sie haben jetzt alle CSS entfernt, die Sie zuvor zu Ihrer Website hinzugefügt haben.  
    
    > ##### Abbildung 28  
    > Die Inlineformatvorlage wurde aus dem NAV-Element entfernt  
    > ![Die Inlineformatvorlage wurde aus dem NAV-Element entfernt][ImageCssExternal04]  

1.  Klicken Sie auf **neue Datei**.  
    
    > ##### Abbildung 29  
    > Dialogfeld ' neue Datei '  
    > ![Dialogfeld ' neue Datei '][ImageCssExternal05]  
    
1.  Ersetzen `cool-file.js` `style.css` Sie durch, und klicken Sie dann auf **Datei hinzufügen**.  
    
    > ##### Abbildung 30  
    > Tippen `style.css`  
    > ![Eingeben von Style. CSS][ImageCssExternal06]  
    
1.  Fügen Sie diesen Code in `style.css` Folgendes ein:  
    
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
    
    > ##### Abbildung 31  
    > Hinzufügen von Code zu `style.css`  
    > ![Hinzufügen von Code zu Style. CSS][ImageCssExternal07]  
    
    An diesem Punkt haben Sie ein externes Stylesheet erstellt, doch Ihr HTML-Code weiß noch nicht, dass es vorhanden ist.  
    
1.  Öffnen Sie `index.html`.  
1.  Dem `<link rel="stylesheet" href="style.css">` HTML-Code hinzufügen.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### Abbildung 32  
    > Verknüpfen mit `style.css`  
    > ![Verknüpfen mit Style. CSS][ImageCssExternal08]  

1.  Wechseln Sie zu, `contact.html` und fügen Sie den Link auch dort hinzu.  
    
    > ##### Abbildung 33  
    > Verknüpfen mit `style.css` in `contact.html`  
    > ![Verknüpfen mit Style. CSS in Contact. html][ImageCssExternal09]  

1.  Wechseln Sie zur **Registerkarte Live**.  Auf der Startseite befindet sich nun die gleiche Schriftart wie im letzten Abschnitt und ein blauer Navigationsbereich.  
    
    > ##### Abbildung 34  
    > Die Startseite  
    > ![Die Startseite][ImageCssExternal10]  
    
1.  Klicken Sie auf den Link **Kontakt** , um zur Kontaktseite zu gelangen.  Die Seite "Kontakt" hat dieselbe Formatierung wie die Startseite.  
    
    > ##### Abbildung 35  
    > Die Kontaktseite  
    > ![Die Kontaktseite][ImageCssExternal11]  
    
## Verwenden eines CSS-Frameworks   

**CSS-Frameworks** sind Sammlungen von Formatvorlagen, die von anderen Entwicklern erstellt wurden, die das Erstellen attraktiver Websites vereinfachen.  Anstatt selbst Formatvorlagen zu definieren, bietet Ihnen ein Framework eine Sammlung von Formatvorlagen, die Sie für Ihre Seitenelemente verwenden können.  

1.  Kopieren Sie den folgenden Code:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Wechseln Sie zur Registerkarte Bearbeitung, und fügen Sie den Code in ein `contact.html` .  
    
    > ##### Abbildung 36  
    > Verknüpfen mit dem Framework in `contact.html`  
    > ![Verknüpfen mit dem Framework in Contact. html][ImageCssFramework1]  
    
1.  Fügen Sie den Code `index.html` ebenfalls ein.  
    
    > ##### Abbildung 37  
    > Verknüpfen mit dem Framework in `index.html`  
    > ![Verknüpfen mit dem Framework in Index. html][ImageCssFramework2]  
    
1.  Kehren Sie zur Registerkarte Live zurück, um Ihre Änderungen anzuzeigen.  Während die Hintergrundfarbe von `<nav>` und die Schriftart der `li a` Elemente identisch sind, hat sich die Schriftart der anderen Elemente geändert.  
    
    > ##### Abbildung 38  
    > Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert  
    > ![Einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert][ImageCssFramework3]  

### Verwenden einer Klasse   

Im letzten Abschnitt haben Sie Ihren Webseiten Bootstrap hinzugefügt, wodurch die Schriftarten einiger Elemente auf Ihrer Website geändert wurden.  CSS-Frameworks können Ihnen helfen, wichtige Änderungen an Ihrer Seite mit sehr wenig Code vorzunehmen.  Probieren Sie es jetzt aus, indem Sie die Kopfzeile ändern:  

1.  Kopieren Sie diesen Code:  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Fügen Sie diesen Code zu Ihrem `<header>` Tag in hinzu `index.html` .  
    
    > ##### Abbildung 39  
    > Hinzufügen von Klassen in `index.html`  
    > ![Hinzufügen von Klassen in "index. html"][ImageCssJumbotron1]  
    
1.  Fügen Sie dem Tag auch den Code hinzu `<header>` `contact.html` .  
    
    > ##### Abbildung 40  
    > Hinzufügen von Klassen in `contact.html`  
    > ![Hinzufügen von Klassen in Contact. html][ImageCssJumbotron2]  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  Es gibt jetzt ein großes, graues Feld um ihre Kopfzeile.  
    
    > ##### Abbildung 41  
    > Die Kopfzeile hat nun ein großes, graues Feld um Sie herum  
    > ![Die Kopfzeile hat nun ein großes, graues Feld um Sie herum][ImageCssJumbotron3]  
    
### Grundlegendes zu Klassen   

Mit Klassen können Sie Auflistungen von Formatvorlagen beliebigen Elementen zuweisen.  So können Sie beispielsweise festlegen, dass das `class` Attribut der `<header>` Tags auf `jumbotron` die folgenden Formatvorlagen angewendet wird:  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Ein Vorteil von Kursen besteht darin, dass Sie Formatvorlagen auf alle gewünschten Elemente anwenden können.  Angenommen, Sie möchten die Hintergrundfarbe *einiger* `<p>` Elemente auf lila, aber nicht auf *alle* Farben einstellen.  Sie können die Formatvorlage in einer Klasse definieren:  

```css
.custom-background {
  background-color: purple;
}
```  

Und wenden Sie dann die Klasse nur auf die `<p>` Elemente an, die Sie formatieren möchten:  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### Ausrichten von Elementen   

Bootstrap stellt auch Klassen zum Ausrichten von Elementen bereit.  Probieren Sie es jetzt aus:  

1.  Wechseln Sie zurück zur Registerkarte Editor, und öffnen Sie Sie `index.html` .  
1.  `class="container-fluid"`Zu Ihrem Tag hinzufügen `<body>` .  
    
    > ##### Abbildung 42  
    > Hinzufügen der `container-fluid` Klasse  
    > ![Hinzufügen der Container-Fluid Klasse][ImageCssAlign1]  

1.  Umbrechen `<nav>` `<main>` von und Elementen in `<div class="row">` .  Stellen Sie sicher, dass Sie `</div>` `</main>` die neue Kategorie ordnungsgemäß schließen, um Sie zu beenden.  
    
    > ##### Abbildung 43  
    > Hinzufügen einer Zeile  
    > ![Hinzufügen einer Zeile][ImageCssAlign2]  
    
1.  Fügen Sie `class="col-3"` Ihrem `<nav>` Tag und `class="col-9"` Ihrem `<main>` Tag hinzu.  
    
    > ##### Abbildung 44  
    > Hinzufügen der `col-3` und- `col-9` Klassen  
    > ![Hinzufügen der Klassen Col-3 und Col-9][ImageCssAlign3]  
    
1.  Zeigen Sie Ihre Änderungen auf der Registerkarte "Live" an.  
    
    > ##### Abbildung 45  
    > Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.  
    > ![Der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt.][ImageCssAlign4]  
    
## Nächste Schritte   

Herzlichen Glückwunsch!  Fertig!  

*   Die beste Methode, um die Web-Entwicklung zu verbessern, besteht darin, weitere Websites zu erstellen.  Machen Sie sich keine Sorgen, wenn Sie etwas kaputt machen.  Sie haben einfach nur Spaß und lernen so viel wie möglich auf dem Weg.  
*   Schauen Sie sich die [Einführung in CSS][MDNCssFirstSteps] an, um weitere Informationen zum Formatieren von Webseiten zu erhalten.  
*   Arbeiten Sie [im ersten Schritt mit dem anzeigen und Ändern des CSS][DevtoolsCssIndex] -Lernprogramms, um mehr darüber zu erfahren, wie Sie devtools verwenden können, um mit dem CSS einer Seite zu experimentieren.  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Abbildung 1: wie Ihre Website aktuell aussieht"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Abbildung 2: wie Ihre Website am Ende des Lernprogramms aussehen wird"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Abbildung 3: die Registerkarte "Bearbeiten""  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Abbildung 4: das Menü "Projektoptionen""  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Abbildung 5: die Registerkarte "Live""  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Abbildung 6: Dies wurde mit CSS formatiert"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Abbildung 7: Index. html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Abbildung 8: die Hintergrundfarbe hinter den Links für "Start" und "Kontakt" ist jetzt blau"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Abbildung 9: die Kontaktseite"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Abbildung 10: die Schriftart der Links für "Start" und "Kontakt" wurde geändert"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Abbildung 11: der Text "Kontakt!" hat nun dieselbe Schriftart wie die Links "Privat" und "Kontakt""  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Abbildung 12: Überprüfen des Start Links"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Abbildung 13: die Registerkarte "Formatvorlagen" befindet sich unterhalb der DOM-Struktur"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Abbildung 14: die Registerkarte "Formatvorlagen" befindet sich rechts neben der DOM-Struktur"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Abbildung 15: Hinzufügen einer neuen Deklaration"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Abbildung 16: eingeben von Farben"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Abbildung 17: eingeben von Magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Abbildung 18: die Farbauswahl"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Abbildung 19: Ändern der Schriftfarbe in Lila mit der Farbauswahl"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Abbildung 20: Hinzufügen einer neuen Regel"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Abbildung 21: Ersetzen eines durch a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Abbildung 22: eingeben von Hintergrundfarbe"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Abbildung 23: eingeben von grün"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Abbildung 24: zeigen Sie mit der Maus auf den Link "Start", um den grünen Hintergrund anzuzeigen."  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Abbildung 25: nach dem erneuten Laden der Seite sind die Änderungen, die in devtools vorgenommen wurden, nicht mehr vorhanden"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Abbildung 26: Contact. html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Abbildung 27: das Style-Tag wurde entfernt"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Abbildung 28: die Inlineformatvorlage wurde aus dem NAV-Element entfernt"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Abbildung 29: Dialogfeld "neue Datei""  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Abbildung 30: eingeben von Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Abbildung 31: Hinzufügen von Code zu Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Abbildung 32: Verknüpfen mit Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Abbildung 33: Verknüpfen mit Style. CSS in Contact. html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Abbildung 34: die Startseite"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Abbildung 35: die Kontaktseite"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Abbildung 36: Verknüpfen mit dem Framework in Contact. html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Abbildung 37: Verknüpfen mit dem Framework in Index. html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Abbildung 38: einige der Schriftart auf der Startseite wurden aufgrund des Frameworks geändert"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Abbildung 39: Hinzufügen von Klassen in Index. html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Abbildung 40: Hinzufügen von Klassen in Contact. html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Abbildung 41: die Kopfzeile hat nun ein großes, graues Feld um Sie herum"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Abbildung 42: Hinzufügen der Container Fluid Klasse"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Abbildung 43: Hinzufügen einer Zeile"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Abbildung 44: Hinzufügen der Klassen Col-3 und Col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Abbildung 45: der Navigations Inhalt befindet sich jetzt links neben dem Hauptinhalt."  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools für Anfänger: Erste Schritte mit HTML und dem Dom"  
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte beim Anzeigen und Ändern von CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "Index. html-gekocht-Amphibien | Glitch"  

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
