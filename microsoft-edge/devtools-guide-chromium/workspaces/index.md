---
description: Erfahren Sie, wie Sie In DevTools vorgenommene Änderungen auf dem Datenträger speichern.
title: Bearbeiten von Dateien mit Arbeitsbereichen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 17f9ced15dbacd62c9ffe40e4af889925a8155fb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399246"
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

# <a name="edit-files-with-workspaces"></a>Bearbeiten von Dateien mit Arbeitsbereichen  

> [!NOTE]
> Ziel dieses Lernprogramms ist es, praktische Übungen zum Einrichten und Verwenden von Arbeitsbereichen zu bieten, damit Sie Arbeitsbereiche in Ihren eigenen Projekten verwenden können.  Sie können die Änderungen am Quellcode auf Ihrem lokalen Computer speichern, die Sie in DevTools vorgenommen haben, nachdem Sie Arbeitsbereiche aktiviert haben.  

> [!IMPORTANT]
> **Voraussetzungen**: Bevor Sie mit diesem Lernprogramm beginnen, sollten Sie wissen, wie Sie die folgenden Aktionen ausführen.  
> 
> *   [Erstellen einer Webseite mithilfe von HTML, CSS und JavaScript][MDNWebGettingStarted]  
> *   [Verwenden von DevTools zum Vornehmen grundlegender Änderungen an CSS][DevToolsCssIndex]  
> *   [Ausführen eines lokalen HTTP-Webservers][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a>Übersicht  

Mit Arbeitsbereichen können Sie eine Änderung, die Sie in Devtools in einer lokalen Kopie derselben Datei auf Ihrem Computer erstellen, speichern.  Für dieses Lernprogramm sollten Sie die folgenden Einstellungen auf Ihrem Computer haben.  

*   Sie haben den Quellcode für Ihre Website auf Ihrem Desktop.  
*   Sie ausführen einen lokalen Webserver aus dem Quellcodeverzeichnis, sodass auf die Website unter zugegriffen werden `localhost:8080` kann.  
*   Sie haben in Microsoft Edge geöffnet und verwenden `localhost:8080` DevTools, um die CSS der Website zu ändern.  

Wenn Arbeitsbereiche aktiviert sind, werden die CSS-Änderungen, die Sie in DevTools vornehmen, im Quellcode auf Ihrem Desktop gespeichert.  

## <a name="limitations"></a>Einschränkungen  

Wenn Sie ein modernes Framework verwenden, wird der Quellcode wahrscheinlich von einem Format transformiert, das einfach zu verwalten ist, in ein Format, das so optimiert ist, dass er so schnell wie möglich ausgeführt werden kann.  

Workspaces ist in der Regel in der Lage, den optimierten Code mithilfe von Quellzuordnungen wieder dem ursprünglichen [Quellcode zu zuordnungen.][TreehouseBlogSourceMaps]  Es gibt jedoch viele Unterschiede zwischen Frameworks darüber, wie die einzelnen Quellzuordnungen verwendet werden.  Devtools unterstützt einfach alle Variationen.  

Arbeitsbereiche funktionieren mit dem folgenden Framework nicht.  

*   Erstellen von React App  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a>Verwandtes Feature: Lokale Außerkraftsetzungen  

**Lokale Außerkraftsetzungen** ist ein weiteres DevTools-Feature, das Arbeitsbereichen ähnelt.  Verwenden Sie lokale Außerkraftsetzungen, wenn Sie mit Änderungen an einer Webseite experimentieren möchten, und Sie müssen die Änderungen über alle Webseitenlasten hinweg anzeigen. Es ist ihnen jedoch nicht egal, ob Sie Ihre Änderungen dem Quellcode der Webseite zuordnen möchten.  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a>Schritt 1: Einrichten  

Führen Sie die folgenden Aktionen aus, um praktische Erfahrungen mit Arbeitsbereichen zu erhalten.  

### <a name="set-up-the-demo"></a>Einrichten der Demo  

1.  [Öffnen Sie die Demo][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Ein Glitch-Projekt" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Ein Glitch-Projekt  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Erstellen Sie `app` ein Verzeichnis auf Ihrem Desktop.  Speichern Sie Kopien der Dateien aus dem `workspaces-demo` Verzeichnis in das `app` Verzeichnis.  Für den Rest des Lernprogramms wird das Verzeichnis als `~/Desktop/app` bezeichnet.  
1.  Starten Eines lokalen Webservers in `~/Desktop/app` .  Im Folgenden finden Sie einige Beispielcode zum Starten, aber Sie können den von Ihnen `SimpleHTTPServer` bevorzugten Server verwenden.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Öffnen Sie eine Registerkarte in Microsoft Edge, und navigieren Sie zu lokal gehosteter Version der Website.  Sie sollten über eine URL wie oder darauf `localhost:8080` zugreifen `http://0.0.0.0:8080` können.  Die genaue [Portnummer][WikiPortURLs] kann unterschiedlich sein.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Die Demo" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       Die Demo  
    :::image-end:::  
    
### <a name="set-up-devtools"></a>Einrichten von DevTools  

1.  Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um den **Konsolenbereich** von DevTools zu öffnen.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Konsolenbereich" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       **Konsolenbereich**  
    :::image-end:::  
    
1.  Wählen Sie das **Tool Quellen** aus.  
1.  Wählen Sie **den Dateisystembereich** aus.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Der Dateisystembereich" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       Der **Dateisystembereich**  
    :::image-end:::  
    
1.  Wählen **Sie Ordner zum Arbeitsbereich hinzufügen aus.**  
1.  Geben Sie `~/Desktop/app` ein.  
1.  Wählen **Sie Zulassen** aus, um DevTools die Berechtigung zum Lesen und Schreiben in das Verzeichnis zu erteilen.  
    Im **Dateisystembereich** befindet sich nun ein grüner Punkt neben `index.html` , `script.js` und `styles.css` .  Diese grünen Punkte bedeuten, dass DevTools eine Zuordnung zwischen den Netzwerkressourcen der Seite und den Dateien in eingerichtet `~/Desktop/app` hat.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Der Dateisystembereich zeigt jetzt eine Zuordnung zwischen den lokalen Dateien und den Netzwerkdateien an." lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       Der **Dateisystembereich** zeigt jetzt eine Zuordnung zwischen den lokalen Dateien und den Netzwerkdateien an.  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a>Schritt 2: Speichern einer CSS-Änderung auf dem Datenträger  

1.  Öffnen Sie `styles.css`.  
    
    > [!NOTE]
    > Die `color` Eigenschaft von Elementen ist auf `h1` `fuchsia` festgelegt.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Styles.css in einem Texteditor anzeigen" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Anzeigen `styles.css` in einem Texteditor  
    :::image-end:::  
    
1.  Wählen Sie das **Elementtool** aus.  
1.  Ändern Sie den Wert der `color` Eigenschaft des Elements in Ihre Bevorzugte `<h1>` Farbe.  
    Denken Sie daran, dass Sie das Element in der DOM-Struktur auswählen müssen, um die darauf angewendeten CSS-Regeln im Bereich `<h1>` **Formatvorlagen anzuzeigen.** ****  Der grüne Punkt neben `styles.css:1` bedeutet, dass alle änderungen, die Sie machen, zugeordnet `~/Desktop/app/styles.css` werden.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Der grüne Indikator, dass die Datei verknüpft ist" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       Der grüne Indikator, dass die Datei verknüpft ist  
    :::image-end:::  
    
1.  Öffnen `styles.css` Sie erneut in einem Text-Editor.  Die `color` Eigenschaft wird nun auf Ihre bevorzugte Farbe festgelegt.  
1.  Aktualisieren Sie die Seite.  Die Farbe des Elements `<h1>` ist weiterhin auf Ihre Bevorzugte Farbe festgelegt.  Die Änderung bleibt bei einer Aktualisierung erhalten, da devTools die Änderung bei der Änderung auf dem Datenträger gespeichert hat.  Und dann, wenn Sie die Seite aktualisiert haben, hat Ihr lokaler Server die geänderte Kopie der Datei vom Datenträger aus bedient.  
    
## <a name="step-3-save-an-html-change-to-disk"></a>Schritt 3: Speichern einer HTML-Änderung auf dem Datenträger  

### <a name="change-html-from-the-elements-panel"></a>Ändern von HTML aus dem Elementbereich  

Sie können änderungen am HTML aus dem Elementbereich vornehmen, aber Ihre Änderungen an der DOM-Struktur werden nicht auf dem Datenträger gespeichert und wirken sich nur auf die aktuelle Browsersitzung aus.  

Die DOM-Struktur ist nicht html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-panel"></a>Ändern von HTML im Bereich Quellen  

Wenn Sie eine Änderung am Html der Seite speichern möchten, verwenden Sie den **Bereich Quellen.**  

1.  Wählen Sie das **Tool Quellen** aus.  
1.  Wählen Sie den **Seitenbereich** aus.  
1.  Wählen **Sie (Index)** aus.  Der HTML-Code für die Seite wird geöffnet.  
1.  Ersetzen Sie `<h1>Workspaces Demo</h1>` durch `<h1>I ❤️  Cake</h1>`.  Überprüfen Sie die folgende Abbildung.  
1.  Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um die Änderung zu speichern.  
1.  Aktualisieren Sie die Seite.  Das `<h1>` Element zeigt weiterhin den neuen Text an.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Ändern von HTML im Bereich Quellen" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Ändern von HTML im **Bereich Quellen**  
    :::image-end:::  
    
1.  Öffnen Sie `~/Desktop/app/index.html`.  Das `<h1>` Element enthält den neuen Text.  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a>Schritt 4: Speichern einer JavaScript-Änderung auf dem Datenträger  

Der **Bereich** Quellen ist auch der Ort, an dem Änderungen an JavaScript vorgenommen werden können.  Manchmal müssen Sie jedoch auf andere Bereiche zugreifen, **** z. B. auf das **Tool Elemente** oder den Konsolenbereich, während Sie Änderungen an Ihrer Website vornehmen.  Es gibt eine Möglichkeit, den Bereich **Quellen** zusammen mit anderen Panels zu öffnen.  

1.  Wählen Sie das **Elementtool** aus.  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.  Das **Befehlsmenü** wird geöffnet.  
1.  Geben `QS` Sie ein, und wählen Sie **Dann Schnellquelle anzeigen aus.**  Am unteren Rand des DevTools-Fensters befindet sich nun ein **Schnellquellenbereich.**  Der Bereich zeigt den Inhalt von an, der die letzte Datei ist, die `index.html` Sie im Bereich Quellen **bearbeitet** haben.  Im **Schnellquellenbereich** erhalten Sie **** den Editor aus dem Bereich Quellen, sodass Sie Dateien bearbeiten können, während andere Bereiche geöffnet sind.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Öffnen des Schnellquellenbereichs mithilfe des Befehlsmenüs" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Öffnen des **Schnellquellenbereichs** mithilfe **des Befehlsmenüs**  
    :::image-end:::  
    
1.  Wählen `Control` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) aus, um das Dialogfeld **Datei öffnen zu** öffnen.  Überprüfen Sie die folgende Abbildung.  
1.  Geben `script` Sie ein, und wählen Sie **dann app/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Öffnen script.js mithilfe des Dialogfelds Datei öffnen" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Öffnen `script.js` mithilfe des **Dialogfelds Datei** öffnen  
    :::image-end:::  
    
    > [!NOTE]
    > Der `Save Changes To Disk With Workspaces` Link in der Demo wird regelmäßig stylet.  
    
1.  Fügen Sie den folgenden Code am ende des **script.js** im **Schnellquellenbereich** hinzu.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um die Änderung zu speichern.  
1.  Aktualisieren Sie die Seite.  
    
    > [!NOTE]
    > Der Link auf der Seite ist jetzt italisiert.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Der Link auf der Seite ist jetzt italisiert" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       Der Link auf der Seite ist jetzt italisiert  
    :::image-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

Verwenden Sie das, was Sie in diesem Lernprogramm gelernt haben, um Arbeitsbereiche in Ihrem eigenen Projekt zu einrichten.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arbeitsbereiche Demodateien | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content – CSS: Cascading StyleSheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Erste Schritte mit der | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ausführen eines einfachen lokalen HTTP-| MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in DOM – Web-APIs | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Eine Einführung in Quellkarten | Treehouse-Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(Computernetzwerk\) – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
