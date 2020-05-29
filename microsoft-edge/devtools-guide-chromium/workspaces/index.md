---
title: Bearbeiten von Dateien mit Arbeitsbereichen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601852"
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







# Bearbeiten von Dateien mit Arbeitsbereichen   



> [!NOTE]
> Das Ziel dieses Lernprogramms ist es, praktische Übungen beim Einrichten und Verwenden von Arbeitsbereichen bereitzustellen, damit Sie Arbeitsbereiche in ihren eigenen Projekten verwenden können.  Sie können die Änderungen am Quellcode auf dem lokalen Computer, den Sie in devtools vorgenommen haben, nach dem Aktivieren von Arbeitsbereichen speichern.  

> [!CAUTION]
> **Voraussetzungen**: bevor Sie dieses Lernprogramm starten, sollten Sie wissen, wie Sie:  
> *   [Verwenden von HTML, CSS und JavaScript zum Erstellen einer Webseite][MDNWebGettingStarted]  
> *   [Verwenden von devtools zum vornehmen grundlegender Änderungen an CSS][DevToolsCssIndex]  
> *   [Ausführen eines lokalen http-Webservers][MDNSimpleLocalHTTPServer]  

## Übersicht   

Mit Arbeitsbereichen können Sie eine in devtools vorgenommene Änderung auf eine lokale Kopie der gleichen Datei auf Ihrem Computer speichern.  Nehmen wir beispielsweise an:  

*   Sie haben den Quellcode für Ihre Website auf dem Desktop.  
*   Sie führen einen lokalen Webserver aus dem Quellcodeverzeichnis aus, damit auf die Website zugegriffen werden kann `localhost:8080` .  
*   Sie `localhost:8080` haben in Microsoft Edge geöffnet, und Sie verwenden devtools, um das CSS der Website zu ändern.  

Wenn Arbeitsbereiche aktiviert sind, werden die CSS-Änderungen, die Sie in devtools vornehmen, im Quellcode auf dem Desktop gespeichert.  

## Einschränkungen   

Wenn Sie ein modernes Framework verwenden, wird der Quellcode wahrscheinlich aus einem Format umgewandelt, das in einem für die Ausführung so schnell wie möglich optimierten Format verwaltet werden kann.  
Arbeitsbereiche können den optimierten Code normalerweise mit Hilfe von [Quell Karten][TreehouseBlogSourceMaps]Ihrem ursprünglichen Quellcode wieder zuordnen.  Es gibt jedoch viele Unterschiede zwischen Frameworks darüber, wie Sie Quell Karten verwenden.  Devtools unterstützt einfach alle Variationen.  

Arbeitsbereiche funktionieren in diesen Frameworks bekanntermaßen nicht:  

*   Erstellen einer Reaktions-App  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## Verwandtes Feature: lokale Überschreibungen   

**Lokale Außerkraftsetzungen** ist ein weiteres devtools-Feature, das mit Arbeitsbereichen vergleichbar ist.  Verwenden Sie lokale Außerkraftsetzungen, wenn Sie mit Änderungen an einer Seite experimentieren möchten, und Sie diese Änderungen über die Seitenlasten hinweg anzeigen müssen, es Ihnen aber nicht wichtig ist, Ihre Änderungen dem Quellcode der Seite zuzuordnen.  

<!--Todo: add section when content is ready  -->  

## Schritt 1: Einrichten   

Führen Sie dieses Lernprogramm aus, um praktische Erfahrungen mit Arbeitsbereichen zu erhalten.  

### Einrichten der Demo   

1.  [Öffnen Sie die Demo][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### Abbildung1  
    > Ein glitch-Projekt ![ ein glitch-Projekt][ImageGlitchProject]  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  Erstellen `app` Sie ein Verzeichnis auf dem Desktop.  Speichern Sie Kopien der Dateien im `workspaces-demo` Verzeichnis.  Im weiteren Verlauf dieses Lernprogramms wird dieses Verzeichnis als bezeichnet `~/Desktop/app` .  
1.  Starten Sie einen lokalen Webserver in `~/Desktop/app` .  Nachfolgend finden Sie einige Beispielcodes zum Starten `SimpleHTTPServer` , aber Sie können den von Ihnen bevorzugten Server verwenden.  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  Öffnen Sie eine Registerkarte in Microsoft Edge, und wechseln Sie zu der lokal gehosteten Version der Website.  Sie sollten in der Lage sein, auf Sie über eine URL wie oder zu zugreifen `localhost:8080` `http://0.0.0.0:8080` .  Die genaue [Portnummer][WikiPortURLs] kann unterschiedlich sein.  
    
    > ##### Abbildung2  
    > Die Demo  
    > ! [Demo] [Imagedemo]  

### Einrichten von devtools   

1.  Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um die **Konsolen** Leiste von devtools zu öffnen.  
    
    > ##### Abbildung 3  
    > Die **Konsolen** Leiste  
    > ! [Konsolenfeld] [ImageConsolePanel]  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Klicken Sie auf die Registerkarte **Dateisystem** .  
    
    > ##### Abbildung4  
    > Die Registerkarte " **Dateisystem** "  
    > ! [Die Registerkarte ' Dateisystem '] [Imagefilesystem]  

1.  Klicken Sie auf **Ordner zum Arbeitsbereich hinzufügen**.  
1.  Wählen Sie aus `~/Desktop/app` .  
1.  Klicken Sie auf **zulassen** , um devtools die Berechtigung zum Lesen und Schreiben in das Verzeichnis zu erteilen.  
    Auf der Registerkarte **Dateisystem** befindet sich nun ein grüner Punkt neben `index.html` , `script.js` und `styles.css` .  Diese grünen Punkte bedeuten, dass devtools eine Zuordnung zwischen den Netzwerkressourcen der Seite und den Dateien in erstellt hat `~/Desktop/app` .  
    
    > ##### Abbildung5  
    > Die Registerkarte " **Dateisystem** " zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerk-Dateien an.  
    > ! [Die Registerkarte "Dateisystem" zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerken an.] [Imagemapping]  

## Schritt 2: Speichern einer CSS-Änderung auf einem Datenträger   

1.  Öffnen Sie `styles.css`.  
    
    > [!NOTE]
    >Die `color` Eigenschaft von `h1` Elements ist auf gesetzt `fuchsia` .
    
    > ##### Abbildung6  
    > Anzeigen `styles.css` in einem Text-Editor  
    > ! [Anzeigen von Formatvorlagen. CSS in einem Text-Editor] [ImageStylesFuchsia]  


1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Ändern Sie den Wert der `color` Eigenschaft des `<h1>` Elements in Ihre bevorzugte Farbe.  
    Beachten Sie, dass Sie auf das `<h1>` Element in der **DOM-Struktur** klicken müssen, um die darauf angewendeten CSS-Regeln im Bereich " **Formatvorlagen** " anzuzeigen.  Der grüne Punkt neben `styles.css:1` bedeutet, dass alle von Ihnen vorgenommenen Änderungen zugeordnet werden `~/Desktop/app/styles.css` .  
    
    > ##### Abbildung7  
    > Der grüne Indikator, mit dem die Datei verknüpft ist  
    > ! [Der grüne Indikator, dass die Datei verknüpft ist] [ImageStylesGreen]  

1.  `styles.css`In einem Text-Editor erneut öffnen.  Die `color` Eigenschaft ist nun auf Ihre Lieblingsfarbe eingestellt.  
1.  Laden Sie die Seite neu.  Die Farbe des `<h1>` Elements wird weiterhin auf Ihre bevorzugte Farbe festgelegt.  Das funktioniert, weil devtools die Änderung auf dem Datenträger gespeichert hat, wenn Sie die Änderung vorgenommen haben.  Und dann, als Sie die Seite neu geladen haben, diente der lokale Server der geänderten Kopie der Datei vom Datenträger.  

## Schritt 3: Speichern einer HTML-Änderung auf einem Datenträger   

### Ändern von HTML über das Panel "Elemente"  

Sie können Änderungen am HTML-Code über das Element Panel vornehmen, Ihre Änderungen an der DOM-Struktur werden aber nicht auf dem Datenträger gespeichert und wirken sich nur auf die aktuelle Browsersitzung aus.  
Die DOM-Struktur ist kein HTML-Code.  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### Ändern von HTML aus dem Quellen Panel   

Wenn Sie eine Änderung am HTML-Code der Seite speichern möchten, verwenden Sie das **Quellen** Panel.  

1.  Klicken Sie auf die Registerkarte **Quellen** .  
1.  Klicken Sie auf die Registerkarte **Seite** .  
1.  Klicken Sie auf **(Index)**.  Der HTML-Code für die Seite wird geöffnet.  
1.  Ersetzen Sie `<h1>Workspaces Demo</h1>` durch `<h1>I ❤️  Cake</h1>`.  Siehe [Abbildung 8](#figure-8).  
1.  Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.  
1.  Laden Sie die Seite neu.  Das `<h1>` Element zeigt weiterhin den neuen Text an.  
    
    > ##### Abbildung8  
    > Zeile 12 wurde auf `I ❤️  Cake`  
    > ! [Ändern von HTML aus dem Quellen Panel] [ImageSourcesCakeHTML]  

1.  Öffnen Sie `~/Desktop/app/index.html`.  Das `<h1>` Element enthält den neuen Text.  

## Schritt 4: Speichern einer JavaScript-Änderung auf einem Datenträger   

Der Bereich " **Quellen** " ist auch der Ort, an dem Sie Änderungen an JavaScript vornehmen können.  Manchmal müssen Sie aber auch auf andere Panels zugreifen, beispielsweise auf das Panel **Elemente** oder den **Konsolen** Panel, während Sie Änderungen an Ihrer Website vornehmen.  Es gibt eine Möglichkeit, das **Quellen** Panel parallel zu anderen Panels zu öffnen.  

1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \).  Das **Befehlsmenü** wird geöffnet.  
1.  Geben `QS` Sie ein, und wählen Sie dann **schnell Quelle anzeigen**aus.  Am unteren Rand des devtools-Fensters befindet sich nun eine **schnell Ausgangs** Registerkarte.  Auf der Registerkarte wird der Inhalt von angezeigt `index.html` , die letzte Datei, die Sie im **Quellen** Panel bearbeitet haben.  Auf der Registerkarte " **schnell Quelle** " finden Sie den Editor im **Quellen** Panel, sodass Sie Dateien bearbeiten können, während andere Panels geöffnet sind.  
    
    > ##### Abbildung 9  
    > Öffnen der Registerkarte " **schnell** Start" über das **Befehlsmenü**  
    > ! [Öffnen der Registerkarte ' schnell Quelle ' mithilfe des Befehlsmenüs] [ImageCommandMenuQuickSource]  

1.  Drücken Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \), um das Dialogfeld **Datei öffnen** zu öffnen.  Siehe [Abbildung 10](#figure-10).  
1.  Geben `script` Sie ein, und wählen Sie dann **App/Script. js**aus.  
    
    > ##### Abbildung 10  
    > Öffnen `script.js` mithilfe des Dialogfelds " **Datei öffnen** "  
    > ! [Öffnen von "Script. js" im Dialogfeld "Datei öffnen"] [ImageOpenFileDialog]  
    
    > [!NOTE]
    > Der `Save Changes To Disk With Workspaces` Link in der Demo wird regelmäßig gestaltet.  
    
1.  Fügen Sie den folgenden Code am Ende von **Skript. js** mithilfe der Registerkarte **schnell** Zugriff hinzu.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.  
1.  Laden Sie die Seite neu.  
    
    > [!NOTE]
    > Der Link auf der Seite ist jetzt kursiv.
    
    > ##### Abbildung 11  
    > Der Link auf der Seite ist jetzt kursiv  
    > ! [Der Link auf der Seite ist jetzt kursiv] [ImageScriptItalic]  

## Nächste Schritte   

Verwenden Sie das gelernte in diesem Lernprogramm, um Arbeitsbereiche in Ihrem eigenen Projekt einzurichten.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Abbildung 1: ein glitch-Projekt mit einem zufällig generierten Namen"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[Imagedemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo.msft.png "Abbildung 2: die Demo"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Console.msft.png "Abbildung 3: die Konsolen Leiste"  
[Imagefilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem.msft.png "Abbildung 4: die Registerkarte" Dateisystem "  
[Imagemapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-Folder.msft.png "Abbildung 5: die Registerkarte" Dateisystem "zeigt nun eine Zuordnung zwischen den lokalen Dateien und den Netzwerken an."  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-CSS.msft.png "Abbildung 6: Anzeigen von Formatvorlagen. CSS in einem Text-Editor"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-Styles-CSS.msft.png "Abbildung 7: der grüne Indikator, mit dem die Datei verknüpft ist"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-Page-H1.msft.png "Abbildung 8: Ändern von HTML aus dem Quellen Panel"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Show-Quick-Source.msft.png "Abbildung 9: Öffnen der Registerkarte" Schnellstart "mit dem Befehlsmenü"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Script.msft.png "Abbildung 10: Öffnen von" Script. js "im Dialogfeld" Datei öffnen "  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-Styles-Quick-Source-Script.msft.png "Abbildung 11: der Link auf der Seite ist jetzt kursiv"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte beim Anzeigen und Ändern von CSS"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Demo Dateien für Arbeitsbereiche | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Inhalt – CSS: Cascading Stylesheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Erste Schritte mit dem Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ausführen eines einfachen lokalen HTTP-Servers | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in DOM-Web-APIs | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Eine Einführung in Quell Karten | Baumhaus-Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \ (Computer Networking \) – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
