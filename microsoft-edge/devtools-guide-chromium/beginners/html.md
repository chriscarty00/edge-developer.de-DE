---
description: Erste Schritte mit HTML und dem DOM
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564567"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools für Anfänger: Erste Schritte mit HTML und dem DOM  

Dies ist das erste in einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung vermitteln.  Erfahren Sie mehr über eine Reihe von Webentwicklertools namens Microsoft Edge DevTools, die Ihre Produktivität erhöhen können.  

In diesem bestimmten Lernprogramm erfahren Sie mehr über HTML und das DOM.  HTML ist eine der Kerntechnologien der Webentwicklung.  Es ist die Sprache, die die Struktur und den Inhalt von Webseiten steuert.  Das DOM steht auch im Zusammenhang mit der Struktur und dem Inhalt von Webseiten, erfahren Sie später mehr darüber.  

## <a name="goals"></a>Ziele  

Sie lernen die Webentwicklung, indem Sie ihre eigene Website erstellen.  Wenn Sie alle Lernprogramme in der **DevTools for Beginners-Reihe** abschließen, sieht Ihre fertige Website möglicherweise wie die folgende Abbildung aus.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="../media/beginners-html-finished.msft.png":::
   Die fertige Website  
:::image-end:::  

Am Ende dieses Lernprogramms sollten Sie die folgenden Themen verstehen.  

*   Wie HTML und das DOM die Inhalte erstellen, die auf Webseiten angezeigt werden.  
*   Wie Microsoft Edge DevTools Ihnen beim Experimentieren mit HTML- und DOM-Änderungen helfen kann.  
*   Der Unterschied zwischen HTML und dem DOM.  

Sie haben auch eine echte Website.  Sie können die Website verwenden, um Ihren Lebenslauf oder Blog zu hosten.  

## <a name="prerequisites"></a>Voraussetzungen  

Bevor Sie dieses Lernprogramm versuchen, müssen Sie die folgenden Voraussetzungen erfüllen:  

*   Wenn Sie mit HTML nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].  
*   Laden Sie [den Microsoft Edge][MicrosoftEdgeInsider] herunter.  Dieses Lernprogramm verwendet eine Reihe von Webentwicklungstools, die als Microsoft Edge DevTools bezeichnet werden, die in die Microsoft Edge.  

## <a name="set-up-your-code"></a>Einrichten des Codes  

Sie erstellen Ihre Website in einem Onlinecode-Editor namens Glitch.  

1.  Öffnen Sie [den Quellcode][GlitchAlluringShockIndex].  Diese Registerkarte wird in diesem **Lernprogramm als Editorregisterkarte** bezeichnet.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Die Registerkarte Editor" lightbox="../media/beginners-html-setup1.msft.png":::
       Die Registerkarte Editor  
    :::image-end:::  
    
1.  Wählen **Sie alluring-shock**aus.  Das Project Optionen wird in der oberen linken Ecke geöffnet.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menü Project Optionen" lightbox="../media/beginners-html-setup2.msft.png":::
       Menü Project Optionen  
    :::image-end:::  
    
1.  Wählen **Sie #A0 Project**aus.  Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert nach dem Zufallsprinzip einen neuen Namen für das Projekt.  Der Inhalt ist der gleiche wie zuvor.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Das gemixte Projekt" lightbox="../media/beginners-html-setup3.msft.png":::
       Das gemixte Projekt  
    :::image-end:::  
    
1.  Wenn Sie planen, das nächste Lernprogramm in dieser Reihe zu beenden, wählen Sie **Anmelden** aus, und melden Sie sich mit Ihrem GitHub oder Ihrem Facebook-Konto bei Glitch an.  Wenn Sie sich nicht bei Ihrem Konto anmelden, verlieren Sie die Möglichkeit, das Projekt zu bearbeiten, nachdem Sie die Bearbeitungsregisterkarte geschlossen haben.  
1.  Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**  Eine neue Registerkarte wird geöffnet, auf der die Liveseite angezeigt wird.  Diese Registerkarte wird in diesem **Lernprogramm als Liveregisterkarte** bezeichnet.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Die Registerkarte Live" lightbox="../media/beginners-html-setup4.msft.png":::
       Die Registerkarte Live  
    :::image-end:::  
    
## <a name="add-content"></a>Hinzufügen von Inhalten  

Ihre Website ist ziemlich leer.  Führen Sie die folgenden Schritte aus, um einige Inhalte hinzuzufügen.  

1.  Ersetzen Sie **auf der Registerkarte Editor**durch `<!-- You're "About Me" will go here.  -->` `<h1>About Me</h1>` .  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Der neue Code wird auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add1.msft.png":::
             Der neue Code wird auf der Registerkarte Editor hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Zeigen Sie Ihre Änderungen auf der **Registerkarte Live an.**  Der Text `About Me` ist auf der Seite sichtbar.  Der Text, der größer als der umgebende Text ist, da `<h1>` das Element eine Abschnittsüberschrift darstellt.  In Ihrem Webbrowser werden Überschriften automatisch in größeren Schriftgraden formatiert.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift wird auf der Registerkarte Live angezeigt." lightbox="../media/beginners-html-add2.msft.png":::
       Die neue Überschrift wird auf der Registerkarte Live angezeigt.  
    :::image-end:::  
    
1.  Fügen Sie zurück auf **der Registerkarte Editor**die Zeile unten ein, in der Sie gerade eingefügt `<p>I am learning HTML.  Recent accomplishments:</p>` `<h1>About Me</h1>` haben.  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Der aktualisierte Code wird auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add3.msft.png":::
             Der aktualisierte Code wird auf der Registerkarte Editor hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Zeigen Sie Ihre Änderung auf der **Registerkarte Live an.**  
1.  Fügen Sie auf **der Registerkarte Editor**eine Liste Ihrer Erfolge hinzu:  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Der aktualisierte Code wird auch auf der Registerkarte Editor hervorgehoben." lightbox="../media/beginners-html-add4.msft.png":::
             Der aktualisierte Code wird auch auf der Registerkarte Editor hervorgehoben.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wechseln Sie erneut zur Registerkarte **Live,** um sicherzustellen, dass der neue Inhalt ordnungsgemäß angezeigt wird.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Die neue Liste wird auf der Registerkarte Live angezeigt." lightbox="../media/beginners-html-add5.msft.png":::
       Die neue Liste wird auf der Registerkarte Live angezeigt.  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimentieren mit Inhaltsänderungen in Microsoft Edge DevTools  

Wenn Sie eine große Seite mit viel HTML entwickelt haben, ist es etwas mühsam, hunderte Male zwischen der Editorregisterkarte und der Liveregisterkarte hin- und her zu wechseln, um Ihre Änderungen anzeigen zu können, insbesondere wenn Sie nicht sicher sind, was genau auf der Seite angezeigt werden soll.  Microsoft Edge DevTools hilft Ihnen, mit Inhaltsänderungen zu experimentieren, ohne die **Liveregisterkarte zu verlassen.**  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Erfahren Sie mehr über den Unterschied zwischen HTML und dem DOM  

Bevor Sie mit der Bearbeitung Ihrer Inhalte Microsoft Edge DevTools beginnen, sollten Sie den Unterschied zwischen HTML und dem DOM verstehen.  Die beste Methode, um zu lernen, ist ein Beispiel:  

1.  Navigieren Sie zur **Registerkarte Live**.  Am unteren Rand der Seite wird der `A new element!?!` Text angezeigt.  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Am unteren Rand der Seite der Text Ein neues Element!?! wird angezeigt" lightbox="../media/beginners-html-dom1.msft.png":::
       Am unteren Rand der Seite wird der `A new element!?!` Text angezeigt  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Editor,** und versuchen Sie, den Text in zu `index.html` finden.  Der Text ist nicht enthalten.  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Der Geheimnistext Ein neues Element!?! ist nirgends in index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       Der Mysterientext `A new element!?!` ist in keinem Land zu finden `index.html`  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Registerkarte Live,** zeigen Sie auf , öffnen Sie das kontextbezogene Menü \(mit der rechten Maustaste `A new element!?!` auf\), und wählen Sie **Überprüfen**aus.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="../media/beginners-html-dom3.msft.png":::
       Überprüfen von Text  
    :::image-end:::  
    
    DevTools wird neben Ihrer Seite geöffnet.  `<div>A new element!?!</div>` ist blau hervorgehoben.  Obwohl diese Struktur in DevTools wie Ihr HTML aussieht, handelt es sich tatsächlich um die **DOM-Struktur**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet" lightbox="../media/beginners-html-dom4.msft.png":::
       DevTools ist neben der Seite geöffnet  
    :::image-end:::  
    
Wenn Ihre Seite geladen wird, verwendet der Browser Ihre HTML, um *den* anfänglichen Inhalt der Seite zu erstellen.  Das DOM stellt den *aktuellen Inhalt* der Seite dar, der sich im Laufe der Zeit ändern kann.  Der rätselhafte Inhalt wird Ihrer Seite aufgrund des Tags am unteren `<div>A new element!?!</div>` `<script src="new.js"></script>` Rand Ihres HTML hinzugefügt.  Dieses Tag bewirkt, dass javaScript-Code ausgeführt wird.  Erfahren Sie mehr über JavaScript in einem späteren Lernprogramm, sehen Sie es aber vorerst als Programmiersprache an, die den Inhalt Ihrer Seite ändern kann.  In diesem speziellen Fall wird Der JavaScript-Code `<div>A new element!?!</div>` zu Ihrer Seite hinzufügt.  Aus diesem Grund ist dieser Mysterientext auf Ihrer Liveseite sichtbar, aber nicht in Ihrem HTML.  

### <a name="edit-the-dom"></a>Bearbeiten des DOM  

Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Liveregisterkarte zu verlassen, versuchen Sie DevTools.  

1.  Zeigen Sie in DevTools auf , öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Your site!` Maustaste\), und wählen **Sie Bearbeiten als HTML aus.**  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Bearbeiten des Knotens als HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Bearbeiten des Knotens als HTML  
    :::image-end:::  
    
1.  Ersetzen `<p>Your site!</p>` Sie durch den folgenden Code.  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Aktualisieren des Knotens als HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Aktualisieren des Knotens als HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um Ihre Änderungen zu speichern, oder wählen Sie außerhalb des Felds aus.  Ihre Änderungen werden automatisch in der Liveansicht Ihrer Seite angezeigt.  Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt" lightbox="../media/beginners-html-edit3.msft.png":::
       Der neue Inhalt wird sofort auf der Seite angezeigt  
    :::image-end:::  
    
Dieser Workflow ist nur für das Experimentieren mit Inhaltsänderungen gut.  Wenn Sie die Seite aktualisieren oder die Registerkarte schließen, sind Ihre Änderungen für immer weg.  Wenn Sie diesen Workflow verwenden und Ihre Änderungen speichern möchten, müssen Sie diese Änderungen manuell in Ihren HTML-Code kopieren.  In den nächsten Abschnitten werden einige weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur gezeigt.  

## <a name="reorder-nodes"></a>Neu anordnen von Knoten  

Sie können auch die Reihenfolge der DOM-Knoten ändern.  Beispielsweise befindet sich das Navigationsmenü auf Ihrer Webseite in der Nähe des unteren Rands.  So verschieben Sie ihn nach oben:  

1.  Suchen Sie `<nav>` den Knoten in der **DOM-Struktur** von DevTools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in DevTools blau hervorgehoben." lightbox="../media/beginners-html-reorder1.msft.png":::
       Der Navigationsknoten ist in DevTools blau hervorgehoben.  
    :::image-end:::  
    
1.  Ziehen Sie `<nav>` den Knoten nach oben, sodass der Knoten das erste untergeordnete Objekt des `<body>` Knotens ist.  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          Der `<nav>` Knoten wird nun oben auf Der Seite angezeigt.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Ziehen des Navigationsknotens nach oben" lightbox="../media/beginners-html-reorder2.msft.png":::
             Ziehen des Navigationsknotens nach oben  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich am oberen Rand der Seite." lightbox="../media/beginners-html-reorder3.msft.png":::
             Der Navigationsknoten befindet sich am oberen Rand der Seite.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a>Löschen eines Knotens  

Sie können auch Knoten aus der DOM-Struktur entfernen.  

1.  Wählen Sie **in der DOM-Struktur**die Option `<div>A new element!?!</div>` aus.  DevTools hebt den Knoten blau hervor.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Auswählen des zu löschende Knotens" lightbox="../media/beginners-html-delete1.msft.png":::
       Auswählen des zu löschende Knotens  
    :::image-end:::  
    
1.  Wählen Sie `Delete` die Taste auf der Tastatur aus.  Der `<div>A new element!?!</div>` Knoten wird aus der DOM-Struktur entfernt.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht" lightbox="../media/beginners-html-delete2.msft.png":::
       Der Knoten wurde gelöscht  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Kopieren Der Änderungen  

Sie sind fast fertig.  Sie haben einige Änderungen an Ihrer Seite in DevTools vorgenommen, aber sie werden noch nicht im Quellcode gespeichert.  

1.  Aktualisieren Sie Ihre **Live-Registerkarte**.  Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, verschwinden.  Insbesondere wird der Text am oberen Rand der Seite `Your site!` zurückgegeben, und der Text `A new element!?!` kehrt nach unten zurück.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind nicht mehr" lightbox="../media/beginners-html-copy1.msft.png":::
       Die von Ihnen vorgenommenen Änderungen sind nicht mehr  
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
    
1.  Wechseln Sie zurück zur **Registerkarte Editor,** und ersetzen Sie den Inhalt Ihrer Datei durch den `index.html` Code, den Sie gerade kopiert haben.  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="So sollte ihre index.html aussehen" lightbox="../media/beginners-html-copy2.msft.png":::
       So sollte `index.html` Ihre Datei aussehen  
    :::image-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

*   Führen Sie das nächste Lernprogramm in dieser Reihe [Erste Schritte css][DevToolsBeginnersCss]aus, um zu erfahren, wie Sie Ihre Seite formatieren und mit Formatänderungen in devTools Microsoft Edge experimentieren.  
*   Lesen [Sie Einführung in das DOM,][MDNIntroductionDom] um mehr über das DOM zu erfahren.  
*   Sehen Sie sich einen Kurs wie [Einführung in die Webentwicklung an,][CourseraIntroductionToWebDevelopment] um mehr praktische Webentwicklungserfahrung zu erhalten.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS-| Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in web development | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html – verlockende | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML-| MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite wurde [hier gefunden](https://developers.google.com/web/tools/chrome-devtools/beginners/html) und von [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
