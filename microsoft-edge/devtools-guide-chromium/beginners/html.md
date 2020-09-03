---
description: Erste Schritte mit HTML und dem Dom
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem Dom'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 182885cb97dbd1672d33b257569b0d841466985b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993282"
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

Sie werden Web-Entwicklung lernen, indem Sie Ihre eigene Website erstellen.  Wenn Sie alle Lernprogramme in der *devtools für Anfänger* -Serie abgeschlossen haben, sieht die fertige Website wie in der folgenden Abbildung aus.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-finished.msft.png":::
   Die fertige Website  
:::image-end:::  

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
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Die Registerkarte "Editor"" lightbox="../media/beginners-html-setup1.msft.png":::
       Die Registerkarte "Editor"  
    :::image-end:::  
    
1.  Klicken Sie auf **verführerisch – Schock**.  Das Menü Projektoptionen wird in der oberen linken Ecke geöffnet.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Das Menü "Projektoptionen"" lightbox="../media/beginners-html-setup2.msft.png":::
       Das Menü "Projektoptionen"  
    :::image-end:::  
    
1.  Klicken Sie auf **Remix Project**.  Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.  Der Inhalt ist derselbe wie zuvor.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Das Remix-Projekt" lightbox="../media/beginners-html-setup3.msft.png":::
       Das Remix-Projekt  
    :::image-end:::  
    
1.  Wenn Sie beabsichtigen, das nächste Lernprogramm in dieser Serie abzuschließen, klicken Sie auf **Anmelden** , und registrieren Sie sich bei glitch mit Ihrem GitHub-oder Facebook-Konto.  Wenn Sie sich nicht anmelden, verlieren Sie die Möglichkeit, dieses Projekt zu bearbeiten, wenn Sie die Registerkarte "Bearbeiten" schließen.  
1.  Klicken Sie auf **anzeigen** , und wählen Sie **in einem neuen Fenster**aus.  Daraufhin wird eine neue Registerkarte geöffnet, auf der Sie die Live Seite anzeigen können.  Diese Registerkarte wird in diesem Lernprogramm als **"Live"-Registerkarte** bezeichnet.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Die Registerkarte "Live"" lightbox="../media/beginners-html-setup4.msft.png":::
       Die Registerkarte "Live"  
    :::image-end:::  
    
## Hinzufügen von Inhalten   

Ihre Website ist ziemlich leer.  Führen Sie die folgenden Schritte aus, um Inhalte hinzuzufügen.  

1.  Ersetzen Sie auf der **Registerkarte Editor** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Der neue Code ist auf der Registerkarte "Editor" hervorgehoben." lightbox="../media/beginners-html-add1.msft.png":::
             Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  Der Text `About Me` wird auf der Seite angezeigt.  Sie ist größer als der restliche Text, da das `<h1>` Element eine Abschnittsüberschrift darstellt.  Ihr Webbrowserformat Vorlagen für Überschriften in größeren Schriftgraden automatisch.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift wird auf der Registerkarte "Live" angezeigt" lightbox="../media/beginners-html-add2.msft.png":::
       Die neue Überschrift wird auf der Registerkarte "Live" angezeigt  
    :::image-end:::  
    
1.  Klicken Sie auf der **Registerkarte Editor** `<p>I am learning HTML.  Recent accomplishments:</p>` auf die Zeile, die Sie gerade eingefügt haben `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Der neue Code ist auf der Registerkarte "Editor" hervorgehoben." lightbox="../media/beginners-html-add3.msft.png":::
             Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live"** an.  
1.  Zurück auf der **Registerkarte "Editor"** fügen Sie eine Liste ihrer Leistungen hinzu:  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Der neue Code ist auf der Registerkarte "Editor" hervorgehoben." lightbox="../media/beginners-html-add4.msft.png":::
             Der neue Code ist auf der Registerkarte "Editor" hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wiederkehren Sie zur **Registerkarte Live** zurück, um sicherzustellen, dass der neue Inhalt richtig angezeigt wird.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Die neue Liste wird auf der Registerkarte "Live" angezeigt" lightbox="../media/beginners-html-add5.msft.png":::
       Die neue Liste wird auf der Registerkarte "Live" angezeigt  
    :::image-end:::  
    
## Experimentieren mit Inhaltsänderungen in Microsoft Edge devtools   

Wenn Sie eine große Seite mit viel HTML entwickelt haben, können Sie sich vorstellen, dass es möglicherweise etwas mühsam ist, zwischen der Registerkarte "Editor" und der Registerkarte "Live" hunderte Male hin-und herzugehen, um Ihre Änderungen zu sehen, insbesondere dann, wenn Sie nicht genau wissen, was auf der Seite eingefügt werden soll.  Microsoft Edge devtools kann Ihnen beim Experimentieren mit Inhaltsänderungen helfen, ohne die Live-Registerkarte verlassen zu müssen.  

### Lernen Sie den Unterschied zwischen HTML und dem Dom kennen   

Bevor Sie mit der Bearbeitung Ihrer Inhalte von Microsoft Edge devtools beginnen, ist es hilfreich, den Unterschied zwischen HTML und dem Dom zu verstehen.  Am besten lernen Sie mit einem Beispiel:  

1.  Wechseln Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der Text angezeigt `A new element!?!` .  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Am unteren Rand der Seite wird der Text ein neues Element!?! kann angezeigt werden" lightbox="../media/beginners-html-dom1.msft.png":::
       Am unteren Rand der Seite wird der Text ein neues Element!?! kann angezeigt werden  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor** , und versuchen Sie, diesen Text zu finden `index.html` .  Es ist nicht da!  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Der mysteriöse Text ein neues Element!?! ist nirgendwo in index.html zu finden" lightbox="../media/beginners-html-dom2.msft.png":::
       Der mysteriöse Text `A new element!?!` ist nirgendwo zu finden `index.html`  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Live**, klicken Sie mit der rechten Maustaste `A new element!?!` , und wählen Sie über **prüfen**aus.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="../media/beginners-html-dom3.msft.png":::
       Überprüfen von Text  
    :::image-end:::  
    
    DevTools wird neben ihrer Seite geöffnet.  `<div>A new element!?!</div>` ist blau hervorgehoben.  Obwohl diese Struktur in devtools wie Ihr HTML-Code aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet." lightbox="../media/beginners-html-dom4.msft.png":::
       DevTools ist neben der Seite geöffnet.  
    :::image-end:::  
    
Wenn Ihre Seite geladen wird, verwendet der Browser Ihren HTML-Code, um den *anfänglichen* Inhalt der Seite zu erstellen.  Das Dom steht für den *aktuellen* Inhalt der Seite, der sich im Laufe der Zeit ändern kann.  Der mysteriöse `<div>A new element!?!</div>` Inhalt wird Ihrer Seite hinzugefügt, weil das `<script src="new.js"></script>` Tag am unteren Rand des HTML-Tags liegt.  Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird.  Sie werden in einem späteren Lernprogramm mehr über JavaScript erfahren, aber betrachten Sie es jetzt als Programmiersprache, mit der der Inhalt Ihrer Seite geändert werden kann.  In diesem speziellen Fall fügt JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzu.  Deshalb ist dieser mysteriöse Text auf Ihrer Live-Seite sichtbar, aber nicht in Ihrem HTML-Code.  

### Bearbeiten des DOM   

Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Registerkarte "Live" zu verlassen, probieren Sie devtools aus.  

1.  Klicken Sie in devtools mit der rechten Maustaste, `Your site!` und wählen Sie **als HTML bearbeiten**aus.  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Bearbeiten des Knotens als HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Bearbeiten des Knotens als HTML  
    :::image-end:::  
    
1.  Ersetzen Sie dies `<p>Your site!</p>` durch den folgenden Code.  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Bearbeiten des Knotens als HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Bearbeiten des Knotens als HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \), um die Änderungen zu speichern, oder klicken Sie auf eine Stelle außerhalb des Felds.  Ihre Änderungen werden automatisch in der Live Ansicht Ihrer Seite angezeigt.  Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt." lightbox="../media/beginners-html-edit3.msft.png":::
       Der neue Inhalt wird sofort auf der Seite angezeigt.  
    :::image-end:::  
    
Dieser Workflow eignet sich gut zum Experimentieren mit Inhaltsänderungen.  Wenn Sie die Seite neu laden oder die Registerkarte schließen, sind Ihre Änderungen für immer verschwunden.  Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihr HTML-Code kopieren.  In den nächsten Abschnitten werden weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur angezeigt.  

## Neuanordnen von Knoten   

Sie können auch die Reihenfolge der DOM-Knoten ändern.  Auf Ihrer Webseite befindet sich beispielsweise das Navigationsmenü in der Nähe des unteren Rands.  So verschieben Sie Sie an den Anfang:  

1.  Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von devtools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in devtools blau hervorgehoben." lightbox="../media/beginners-html-reorder1.msft.png":::
       Der Navigationsknoten ist in devtools blau hervorgehoben.  
    :::image-end:::  
    
1.  Ziehen Sie den `<nav>` Knoten an den Anfang, sodass er das erste untergeordnete Element unterhalb des `<body>` Knotens ist.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Ziehen des Navigationsknotens nach oben" lightbox="../media/beginners-html-reorder2.msft.png":::
             Ziehen des Navigationsknotens nach oben  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Der `<nav>` Knoten wird jetzt oben auf der Seite angezeigt.  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich am oberen Rand der Seite." lightbox="../media/beginners-html-reorder3.msft.png":::
             Der Navigationsknoten befindet sich am oberen Rand der Seite.  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### Löschen eines Knotens   

Sie können auch Knoten aus der DOM-Struktur entfernen.  

1.  Klicken Sie in der **DOM-Struktur**auf `<div>A new element!?!</div>` .  DevTools hebt den Knoten Blau hervor.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Auswählen des zu löschenden Knotens" lightbox="../media/beginners-html-delete1.msft.png":::
       Auswählen des zu löschenden Knotens  
    :::image-end:::  
    
1.  Drücken Sie die `Delete` Taste auf der Tastatur.  Der `<div>A new element!?!</div>` Knoten wird aus ihrer DOM-Struktur entfernt.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht" lightbox="../media/beginners-html-delete2.msft.png":::
       Der Knoten wurde gelöscht  
    :::image-end:::  
    
## Kopieren der Änderungen   

Sie haben es fast geschafft.  Sie haben in devtools einige Änderungen an Ihrer Seite vorgenommen, die aber noch nicht in Ihrem Quellcode gespeichert sind.  

1.  Aktualisieren Sie Ihren **Live-Reiter**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden ausgeblendet.  Insbesondere kehrt der Text `Your site!` zum Anfang der Seite zurück, und der Text `A new element!?!` kehrt nach unten zurück.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden" lightbox="../media/beginners-html-copy1.msft.png":::
       Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden  
    :::image-end:::  
    
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
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="So sollte Ihre index.html-Datei aussehen" lightbox="../media/beginners-html-copy2.msft.png":::
       Aussehen der `index.html` Datei  
    :::image-end:::  
    
## Nächste Schritte   

*   Führen Sie das nächste Lernprogramm in dieser Serie, [Erste Schritte mit CSS][DevToolsBeginnersCss], aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Stiländerungen in Microsoft Edge devtools experimentieren.  
*   Lesen Sie [Einführung in das DOM][MDNIntroductionDom] , um mehr über das DOM zu erfahren.  
*   Schauen Sie sich einen Kurs wie [Einführung in die Webentwicklung][CourseraIntroductionToWebDevelopment] an, um mehr praktische Erfahrungen mit der Webentwicklung zu erhalten.  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS | Microsoft docs"  

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
