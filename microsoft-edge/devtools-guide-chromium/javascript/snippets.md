---
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581817"
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





# Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools   



Wenn Sie feststellen, dass derselbe Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausgeführt wird, sollten Sie stattdessen den Code als Snippet speichern.  Ausschnitte sind Skripts, die Sie im [ **Quellen** Panel][DevToolsSourcesPanel]erstellen.  Sie haben Zugriff auf den JavaScript-Kontext der Seite, und Sie können Sie auf einer beliebigen Seite ausführen.  Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet].  
Firefox devtools verfügt über ein ähnliches Feature wie Snippets mit [dem Namen "][MDNScratchpad]Zwischenablage".  

[**Abbildung 1**](#figure-1) zeigt beispielsweise die devtools-Homepage auf der linken Seite und einen Snippet-Quellcode auf der rechten Seite.  

> ##### Abbildung1  
> Aussehen der Seite vor dem Ausführen des Snippets  
> ![Aussehen der Seite vor dem Ausführen des Snippets][ImageSnippetSplitScreen]  

Der Snippet-Quellcode aus [**Abbildung 1**](#figure-1):  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

[**Abbildung 2**](#figure-2) zeigt, wie die Seite nach der Ausführung des Snippets aussieht.  Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Seite ändert sich vollständig.  

> ##### Abbildung2  
> Aussehen der Seite nach dem Ausführen des Snippets  
> ![Aussehen der Seite nach dem Ausführen des Snippets][ImageSnippetSplitScreenAfter]  

## Öffnen des Bereichs "Snippets"   

Im Bereich **Snippets** werden Ihre Snippets aufgelistet.  Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.  

> ##### Abbildung 3  
> Der Bereich " **Ausschnitte** "  
> ![Der Bereich "Ausschnitte"][ImageSnippetsPane]  

### Öffnen des Bereichs "Ausschnitte" mit einer Maus   

1.  Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.  Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.  

    > ##### Abbildung4  
    > Das Fenster " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**  
    > ![Das Fenster "Quellen" mit geöffnetem Seitenbereich auf der linken Seite][ImageSourcesPageEmpty]  

1.  Klicken Sie auf die Registerkarte **Snippets** , um den Bereich **Snippets** zu öffnen.  Möglicherweise müssen Sie auf **Weitere** Registerkarten weitere Registerkarten klicken, um auf ![ ][ImageMoreTabsIcon] die Option **Snippets** zuzugreifen.  

### Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü   

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.  
1.  Beginnen `Snippets` Sie mit der Eingabe, wählen Sie **Snippets anzeigen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.  

    > ##### Abbildung5  
    > Der Befehl ' **Snippets anzeigen** '  
    > ![Der Befehl ' Snippets anzeigen '][ImageShowSnippetsSearch]  

## Erstellen von Ausschnitten   

### Erstellen eines Snippets über das Quellen Panel   

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie auf **neuer Ausschnitt**.  
1.  Geben Sie einen Namen für das Snippet ein, und drücken Sie `Enter` zum Speichern.  

    > ##### Abbildung6  
    > Benennen eines Snippets  
    > ![Benennen eines Snippets][ImageSnippetName]  

### Erstellen eines Snippets über das Befehlsmenü   

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.  
1.  Beginnen `Snippet` Sie mit der Eingabe, wählen Sie **Neues Snippet erstellen**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.  

    > ##### Abbildung7  
    > Der Befehl zum Erstellen eines neuen Snippets  
    > ![Der Befehl zum Erstellen eines neuen Snippets][ImageCreateSnippetSearch]  

Weitere Informationen finden Sie unter [Umbenennen von Snippets](#rename-snippets) , wenn Sie Ihrem neuen Snippet einen benutzerdefinierten Namen zuweisen möchten.  

## Bearbeiten von Ausschnitten   

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie im Bereich **Snippets** auf den Namen des Ausschnitts, den Sie bearbeiten möchten, um ihn im **Code-Editor**zu öffnen.  

    > ##### Abbildung8  
    > Der Code-Editor  
    > ![Der Code-Editor][ImageSnippetEditor]  

1.  Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.  
1.  Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben. Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.  

    > ##### Abbildung 9  
    > Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt  
    > ![Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt][ImageUnsavedSnippet]  

## Ausführen von Ausschnitten   

### Ausführen eines Snippets im Quellen Panel   

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie auf den Namen des Ausschnitts, den Sie ausführen möchten.  Das Snippet wird im **Code-Editor**geöffnet.  
1.  Klicken Sie auf **Snippet** ![ Run Snippet ausführen ][ImageRunSnippetIcon] , oder drücken Sie `Control` + `Enter` \ (Windows \) oder `Command` + `Enter` \ (macOS \).  

### Ausführen eines Snippets mit dem Befehlsmenü   

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen.  
1.  Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.  

    > ##### Abbildung 10  
    > Ausführen eines Snippets über das Befehlsmenü  
    > ![Ausführen eines Snippets über das Befehlsmenü][ImageRunSnippetCommand]  

1.  Drücken Sie `Enter` zum Ausführen des Snippets.  

## Umbenennen von Ausschnitten   

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Umbenennen**aus.  

## Löschen von Ausschnitten   

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Entfernen**aus.  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Abbildung 1: Aussehen der Seite vor dem Ausführen des Snippets"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Abbildung 2: Aussehen der Seite nach dem Ausführen des Snippets"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Abbildung 3: der Bereich "Ausschnitte""  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Abbildung 4: das Fenster "Quellen" mit geöffnetem Seitenbereich auf der linken Seite"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Abbildung 5: Befehl ' Snippets anzeigen '"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Abbildung 6: Benennen eines Snippets"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Abbildung 7: der Befehl zum Erstellen eines neuen Snippets"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Abbildung 8: der Code-Editor"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Abbildung 9: ein Sternchen neben dem Ausschnitt Namen, der nicht gespeicherten Code angibt"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Abbildung 10: Ausführen eines Snippets über das Befehlsmenü"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole"  
[DevToolsSourcesPanel]: ../sources.md "Übersicht über das Quellen Panel"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
