---
description: Snippets sind kleine Skripts, die Sie im Quellen Panel von Microsoft Edge devtools erstellen und ausführen können.  Sie können auf jeder beliebigen Seite darauf zugreifen und diese ausführen.  Wenn Sie einen Ausschnitt ausführen, wird er im Kontext der aktuell geöffneten Seite ausgeführt.
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124740"
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

Wenn Sie feststellen, dass derselbe Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausgeführt wird, sollten Sie stattdessen den Code als Snippet speichern.  Ausschnitte sind Skripts, die Sie im [Quellen][DevToolsSourcesPanel] Panel erstellen.  Sie haben Zugriff auf den JavaScript-Kontext der Seite, und Sie können Sie auf einer beliebigen Seite ausführen.  Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet].  
Firefox devtools verfügt über ein ähnliches Feature wie Snippets mit [dem Namen "][MDNScratchpad]Zwischenablage".  

In der folgenden Abbildung ist beispielsweise die devtools-Homepage auf der linken Seite und ein Codeausschnitt Quellcode auf der rechten Seite zu sehen.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Aussehen der Seite vor dem Ausführen des Snippets  
:::image-end:::  

Der Snippet-Quellcode aus der vorhergehenden Abbildung.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

In der folgenden Abbildung wird die Seite nach dem Ausführen des Snippets angezeigt.  Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Seite ändert sich vollständig.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Aussehen der Seite nach dem Ausführen des Snippets  
:::image-end:::  

## Öffnen des Bereichs "Snippets"  

Im Bereich **Snippets** werden Ihre Snippets aufgelistet.  Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Der Bereich " **Ausschnitte** "  
:::image-end:::  

### Öffnen des Bereichs "Ausschnitte" mit einer Maus  

1.  Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.  Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Das Fenster " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**  
    :::image-end:::  
    
1.  Klicken Sie auf die Registerkarte **Snippets** , um den Bereich **Snippets** zu öffnen.  Möglicherweise müssen Sie **weitere Registerkarten** auswählen \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \), um auf die Option **Snippets** zuzugreifen.  
    
### Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Beginnen `Snippets` Sie mit der Eingabe, wählen Sie **Snippets anzeigen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Der Befehl ' **Snippets anzeigen** '  
    :::image-end:::  
    
## Erstellen von Ausschnitten  

### Erstellen eines Snippets über das Quellen Panel  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Wählen Sie **Neues Snippet**aus.  
1.  Geben Sie einen Namen für das Snippet ein, und wählen Sie dann `Enter` Speichern aus.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Benennen eines Snippets  
    :::image-end:::  
    
### Erstellen eines Snippets über das Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Beginnen `Snippet` Sie mit der Eingabe, wählen Sie **Neues Snippet erstellen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Der Befehl zum Erstellen eines neuen Snippets  
    :::image-end:::  
    
Weitere Informationen finden Sie unter [Umbenennen von Snippets](#rename-snippets) , wenn Sie Ihrem neuen Snippet einen benutzerdefinierten Namen zuweisen möchten.  

## Bearbeiten von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie im Bereich **Snippets** auf den Namen des Ausschnitts, den Sie bearbeiten möchten, um ihn im **Code-Editor**zu öffnen.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Der **Code-Editor**  
    :::image-end:::  
    
1.  Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.  
1.  Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben. Wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus, um Sie zu speichern.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Ein Sternchen neben dem Namen des Snippets, das nicht gespeicherten Code angibt  
    :::image-end:::  
    
## Ausführen von Ausschnitten  

### Ausführen eines Snippets im Quellen Panel  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie auf den Namen des Ausschnitts, den Sie ausführen möchten.  Das Snippet wird im **Code-Editor**geöffnet.  
1.  Wählen Sie **Snippet ausführen** \ ( ![ Snippet ausführen ][ImageRunSnippetIcon] ) aus, oder wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus.  
    
### Ausführen eines Snippets mit dem Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in der devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Aussehen der Seite vor dem Ausführen des Snippets" lightbox="../media/javascript-search-run-command.msft.png":::
       Ausführen eines Snippets über das **Befehlsmenü**  
    :::image-end:::  
    
1.  Wählen Sie aus `Enter` , um den Ausschnitt auszuführen.  

## Umbenennen von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie mit der rechten Maustaste auf den Ausschnitt Namen, und wählen Sie **Umbenennen**aus.  
    
## Löschen von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Klicken Sie mit der rechten Maustaste auf den Snippet-Namen, und wählen Sie **Entfernen**aus.  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Übersicht über das Quellen Panel | Microsoft docs"  

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
