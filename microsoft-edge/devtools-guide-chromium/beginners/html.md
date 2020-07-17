---
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem Dom'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: d992a6ca68de07c879ca8e319ee6c22782924a6b
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882730"
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

# DevTools für Anfänger: Erste Schritte mit HTML und dem Dom   

Dies ist das erste in einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung beibringen.  Darüber hinaus erhalten Sie Informationen zu einer Reihe von Webentwickler Tools namens Microsoft Edge devtools, die Ihre Produktivität steigern können.  

In diesem speziellen Lernprogramm erfahren Sie mehr über HTML und das DOM.  HTML ist eine der Kerntechnologien der Web-Entwicklung.  Diese Sprache steuert die Struktur und den Inhalt von Webseiten.  Das Dom ist auch mit der Struktur und dem Inhalt von Webseiten verknüpft, aber Sie werden später mehr darüber erfahren.  

## Ziele   

Sie werden Web-Entwicklung lernen, indem Sie Ihre eigene Website erstellen.  Wenn Sie alle Lernprogramme in der *devtools für Anfänger* -Serie abgeschlossen haben, sieht Ihre fertige Website wie in **Abbildung 1**aus.  

> ##### Abbildung1  
> Die fertige Website  
> ![Die fertige Website][ImageHtmlFinished]  

Am Ende dieses Lernprogramms können Sie Folgendes verstehen:  

*   So erstellen HTML und Dom die Inhalte, die auf Webseiten angezeigt werden.  
*   So können Sie mithilfe von Microsoft Edge devtools mit HTML-und Dom-Änderungen experimentieren.  
*   Der Unterschied zwischen HTML und dem Dom.  

Sie haben auch eine echte Website!  Mit dieser Website können Sie Ihren Lebenslauf oder Ihren Blog hosten.  

## Voraussetzungen   

Bevor Sie dieses Lernprogramm ausführen, führen Sie die folgenden Voraussetzungen aus:  

*   Wenn Sie mit HTML nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].  
*   Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] -Webbrowser herunter.  In diesem Lernprogramm wird eine Reihe von Webentwicklungstools, so genannte Microsoft Edge-devtools, verwendet, die in Microsoft Edge integriert sind.  

## Einrichten Ihres Codes   

Sie werden Ihre Website in einem Online Code-Editor mit dem Namen glitch erstellen.  

1.  Öffnen Sie den [Quellcode][GlitchAlluringShockIndex].  Diese Registerkarte wird in diesem Lernprogramm als **Registerkarte "Editor** " bezeichnet.  
    > ##### Abbildung2  
    > Die Registerkarte "Editor"  
    > ![Die Registerkarte "Editor"][ImageHtmlSetup1]  

1.  Klicken Sie auf **verführerisch – Schock**.  Das Menü Projektoptionen wird in der oberen linken Ecke geöffnet.  
    
    > #### Abbildung 3  
    > Das Menü "Projektoptionen"  
    > ![Das Menü "Projektoptionen"][ImageHtmlSetup2]  
    
1.  Klicken Sie auf **Remix Project**.  Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.  Der Inhalt ist derselbe wie zuvor.  
    
    > ##### Abbildung4  
    > Das Remix-Projekt  
    > ![Das Remix-Projekt][ImageHtmlSetup3]  
    
1.  Wenn Sie beabsichtigen, das nächste Lernprogramm in dieser Serie abzuschließen, klicken Sie auf **Anmelden** , und registrieren Sie sich bei glitch mit Ihrem GitHub-oder Facebook-Konto.  Wenn Sie sich nicht anmelden, verlieren Sie die Möglichkeit, dieses Projekt zu bearbeiten, wenn Sie die Registerkarte "Bearbeiten" schließen.  
1.  Klicken Sie auf **anzeigen** , und wählen Sie **in einem neuen Fenster**aus.  Daraufhin wird eine neue Registerkarte geöffnet, auf der Sie die Live Seite anzeigen können.  Diese Registerkarte wird in diesem Lernprogramm als **"Live"-Registerkarte** bezeichnet.  
    
    > ##### Abbildung5  
    > Die Registerkarte "Live"  
    > ![Die Registerkarte "Live"][ImageHtmlSetup4]  
    
## Hinzufügen von Inhalten   

Ihre Website ist ziemlich leer.  Führen Sie die folgenden Schritte aus, um Inhalte hinzuzufügen.  

1.  Ersetzen Sie auf der **Registerkarte Editor** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### Abbildung6  
    > Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd1]  
    
1.  Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  Der Text `About Me` wird auf der Seite angezeigt.  Sie ist größer als der restliche Text, da das `<h1>` Element eine Abschnittsüberschrift darstellt.  Ihr Webbrowserformat Vorlagen für Überschriften in größeren Schriftgraden automatisch.  
    
    > ##### Abbildung7  
    > Die neue Überschrift wird auf der Registerkarte "Live" angezeigt  
    > ![Die neue Überschrift wird auf der Registerkarte "Live" angezeigt][ImageHtmlAdd2]  
    
1.  Klicken Sie auf der **Registerkarte Editor** `<p>I am learning HTML.  Recent accomplishments:</p>` auf die Zeile, die Sie gerade eingefügt haben `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### Abbildung8  
    > Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd3]  
    
1.  Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  
1.  Zurück auf der **Registerkarte "Editor"** fügen Sie eine Liste ihrer Leistungen hinzu:  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### Abbildung 9  
    > Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
    > ![Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.][ImageHtmlAdd4]  
    
1.  Wiederkehren Sie zur **Registerkarte Live** zurück, um sicherzustellen, dass der neue Inhalt richtig angezeigt wird.  
    
    > ##### Abbildung 10  
    > Die neue Liste wird auf der Registerkarte "Live" angezeigt  
    > ![Die neue Liste wird auf der Registerkarte "Live" angezeigt][ImageHtmlAdd5]  
    
## Experimentieren mit Inhaltsänderungen in Microsoft Edge devtools   

Wenn Sie eine große Seite mit viel HTML entwickelt haben, können Sie sich vorstellen, dass es möglicherweise etwas mühsam ist, zwischen der Registerkarte "Editor" und der Registerkarte "Live" hunderte Male hin-und herzugehen, um Ihre Änderungen zu sehen, insbesondere dann, wenn Sie nicht genau wissen, was auf der Seite eingefügt werden soll.  Microsoft Edge devtools kann Ihnen beim Experimentieren mit Inhaltsänderungen helfen, ohne die Live-Registerkarte verlassen zu müssen.  

### Lernen Sie den Unterschied zwischen HTML und dem Dom kennen   

Bevor Sie mit der Bearbeitung Ihrer Inhalte von Microsoft Edge devtools beginnen, ist es hilfreich, den Unterschied zwischen HTML und dem Dom zu verstehen.  Am besten lernen Sie mit einem Beispiel:  

1.  Wechseln Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der Text angezeigt `A new element!?!` .  
    
    > ###### Abbildung 11  
    > Unten auf der Seite kann der Text `A new element!?!` angezeigt werden  
    > ![Am unteren Rand der Seite wird der Text ein neues Element!?! kann angezeigt werden][ImageHtmlDom1]  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor** , und versuchen Sie, diesen Text zu finden `index.html` .  Es ist nicht da!  
    
    > ##### Abbildung 12  
    > Der mysteriöse Text `A new element!?!` ist nirgendwo zu finden `index.html`  
    > ![Der mysteriöse Text ein neues Element!?! ist nirgendwo in index.html zu finden][ImageHtmlDom2]  
    
1.  Wechseln Sie zurück zur **Registerkarte Live**, klicken Sie mit der rechten Maustaste `A new element!?!` , und wählen Sie über **prüfen**aus.  
    
    > ##### Abbildung 13  
    > Überprüfen von Text  
    > ![Überprüfen von Text][ImageHtmlDom3]  
    
    DevTools wird neben ihrer Seite geöffnet.  `<div>A new element!?!</div>` ist blau hervorgehoben.  Obwohl diese Struktur in devtools wie Ihr HTML-Code aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.  
    
    > ##### Abbildung 14  
    > DevTools ist neben der Seite geöffnet.  
    > ![DevTools ist neben der Seite geöffnet.][ImageHtmlDom4]  
    
Wenn Ihre Seite geladen wird, verwendet der Browser Ihren HTML-Code, um den *anfänglichen* Inhalt der Seite zu erstellen.  Das Dom steht für den *aktuellen* Inhalt der Seite, der sich im Laufe der Zeit ändern kann.  Der mysteriöse `<div>A new element!?!</div>` Inhalt wird Ihrer Seite hinzugefügt, weil das `<script src="new.js"></script>` Tag am unteren Rand des HTML-Tags liegt.  Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird.  Sie werden in einem späteren Lernprogramm mehr über JavaScript erfahren, aber betrachten Sie es jetzt als Programmiersprache, mit der der Inhalt Ihrer Seite geändert werden kann.  In diesem speziellen Fall fügt JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzu.  Deshalb ist dieser mysteriöse Text auf Ihrer Live-Seite sichtbar, aber nicht in Ihrem HTML-Code.  

### Bearbeiten des DOM   

Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Registerkarte "Live" zu verlassen, probieren Sie devtools aus.  

1.  Klicken Sie in devtools mit der rechten Maustaste, `Your site!` und wählen Sie **als HTML bearbeiten**aus.  

    > ##### Abbildung 15  
    > Bearbeiten des Knotens als HTML  
    > ![Bearbeiten des Knotens als HTML][ImageHtmlEdit1]  
    
1.  Ersetzen Sie dies `<p>Your site!</p>` durch den folgenden Code.  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### Abbildung 16  
    > Bearbeiten des Knotens als HTML  
    > ![Bearbeiten des Knotens als HTML][ImageHtmlEdit2]  
    
1.  Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderungen zu speichern, oder klicken Sie auf eine Stelle außerhalb des Felds.  Ihre Änderungen werden automatisch in der Live Ansicht Ihrer Seite angezeigt.  Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.  
    
    > ##### Abbildung 17  
    > Der neue Inhalt wird sofort auf der Seite angezeigt.  
    > ![Der neue Inhalt wird sofort auf der Seite angezeigt.][ImageHtmlEdit3]  
    
Dieser Workflow eignet sich gut zum Experimentieren mit Inhaltsänderungen.  Wenn Sie die Seite neu laden oder die Registerkarte schließen, sind Ihre Änderungen für immer verschwunden.  Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihr HTML-Code kopieren.  In den nächsten Abschnitten werden weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur angezeigt.  

## Neuanordnen von Knoten   

Sie können auch die Reihenfolge der DOM-Knoten ändern.  Auf Ihrer Webseite befindet sich beispielsweise das Navigationsmenü in der Nähe des unteren Rands.  So verschieben Sie Sie an den Anfang:  

1.  Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von devtools.  
    
    > ##### Abbildung 18  
    > Der Navigationsknoten ist in devtools blau hervorgehoben.  
    > ![Der Navigationsknoten ist in devtools blau hervorgehoben.][ImageHtmlReorder1]  
    
1.  Ziehen Sie den `<nav>` Knoten an den Anfang, sodass er das erste untergeordnete Element unterhalb des `<body>` Knotens ist.  
    > ##### Abbildung 19  
    > Ziehen des Navigationsknotens nach oben  
    > ![Ziehen des Navigationsknotens nach oben][ImageHtmlReorder2]  
    
    Der `<nav>` Knoten wird jetzt oben auf der Seite angezeigt.  
    
    > ##### Abbildung 20  
    > Der Navigationsknoten befindet sich am oberen Rand der Seite.  
    > ![Der Navigationsknoten befindet sich am oberen Rand der Seite.][ImageHtmlReorder3]  
    
### Löschen eines Knotens   

Sie können auch Knoten aus der DOM-Struktur entfernen.  

1.  Klicken Sie in der **DOM-Struktur**auf `<div>A new element!?!</div>` .  DevTools hebt den Knoten Blau hervor.  
    
    > ##### Abbildung 21  
    > Auswählen des zu löschenden Knotens  
    > ![Auswählen des zu löschenden Knotens][ImageHtmlDelete1]  
    
1.  Drücken Sie die `Delete` Taste auf der Tastatur.  Der `<div>A new element!?!</div>` Knoten wird aus ihrer DOM-Struktur entfernt.  
    
    > ##### Abbildung 22  
    > Der Knoten wurde gelöscht  
    > ![Der Knoten wurde gelöscht][ImageHtmlDelete2]  
    
## Kopieren der Änderungen   

Sie haben es fast geschafft.  Sie haben in devtools einige Änderungen an Ihrer Seite vorgenommen, die aber noch nicht in Ihrem Quellcode gespeichert sind.  

1.  Aktualisieren Sie Ihren **Live-Reiter**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden ausgeblendet.  Insbesondere kehrt der Text `Your site!` zum Anfang der Seite zurück, und der Text `A new element!?!` kehrt nach unten zurück.  
    
    > ##### Abbildung 23  
    > Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden  
    > ![Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden][ImageHtmlCopy1]  

1.  Kopieren Sie den folgenden Code.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  Wechseln Sie zurück zur **Registerkarte Editor** , und ersetzen Sie den Inhalt Ihrer `index.html` Datei durch den Code, den Sie soeben kopiert haben.  
    
    > ##### Abbildung 24  
    > Aussehen der `index.html` Datei  
    > ![So sollte Ihre index.html-Datei aussehen][ImageHtmlCopy2]  
    
## Nächste Schritte   

*   Führen Sie das nächste Lernprogramm in dieser Serie, [Erste Schritte mit CSS][DevToolsBeginnersCss], aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Stiländerungen in Microsoft Edge devtools experimentieren.  
*   Lesen Sie [Einführung in das DOM][MDNIntroductionDom] , um mehr über das DOM zu erfahren.  
*   Schauen Sie sich einen Kurs wie [Einführung in die Webentwicklung][CourseraIntroductionToWebDevelopment] an, um mehr praktische Erfahrungen mit der Webentwicklung zu erhalten.  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Abbildung 1: die fertige Website"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Abbildung 2: die Registerkarte "Editor""  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Abbildung 3: das Menü "Projektoptionen""  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Abbildung 4: das Remix-Projekt"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Abbildung 5: die Registerkarte "Live""  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Abbildung 6: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Abbildung 7: die neue Überschrift wird auf der Registerkarte "Live" angezeigt"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Abbildung 8: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Abbildung 9: der neue Code ist auf der Registerkarte "Editor" hervorgehoben"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Abbildung 10: die neue Liste wird auf der Registerkarte "Live" angezeigt"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Abbildung 11: am unteren Rand der Seite der Text ein neues Element!?! kann angezeigt werden"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Abbildung 12: der mysteriöse Text ein neues Element!?! ist nirgendwo in index.html zu finden"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Abbildung 13: Überprüfen von Text"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Abbildung 14: devtools ist neben der Seite geöffnet"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Abbildung 15: Bearbeiten des Knotens als HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Abbildung 16: Bearbeiten des Knotens als HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Abbildung 17: der neue Inhalt wird sofort auf der Seite angezeigt."  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Abbildung 18: der Navigationsknoten ist in devtools blau hervorgehoben"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Abbildung 19: Ziehen des Navigationsknotens nach oben"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Abbildung 20: der Navigationsknoten befindet sich am oberen Rand der Seite."  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Abbildung 21: Auswählen des zu löschenden Knotens"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Abbildung 22: der Knoten wurde gelöscht"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Abbildung 23: die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Abbildung 24: Aussehen Ihrer index.html-Datei"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools für Anfänger: Erste Schritte mit CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in die Web-Entwicklung | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-verführerisch-Schock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Katherine Jackson][KatherineJackson] (Technical Writer intern, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
