---
description: Snippets sind kleine Skripts, die Sie im Quellen Tool von Microsoft Edge devtools erstellen und ausführen können.  Sie können auf jeder beliebigen Webseite auf Ressourcen zugreifen und diese ausführen.  Wenn Sie einen Ausschnitt ausführen, wird er im Kontext der aktuell geöffneten Webseite ausgeführt.
title: Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230957"
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

# Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Webseite mit Microsoft Edge devtools  

Wenn Sie denselben Code wiederholt in der [Konsole][DevtoolsConsoleIndex] ausführen, sollten Sie stattdessen den Code als Snippet speichern.  Ausschnitte sind Skripts, die Sie im [Quellen][DevToolsSourcesTool] Tool erstellen.  Snippets haben Zugriff auf den JavaScript-Kontext der Webseite, und Sie können Ausschnitte auf einer beliebigen Webseite ausführen.  Die Sicherheitseinstellungen der meisten Webseiten blockieren das Laden anderer Skripts in Ausschnitten.  Aus diesem Grund müssen Sie den gesamten Code in eine Datei aufnehmen.  

Snippets sind eine Alternative zu [Bookmarklets][WikiBookmarklet] mit dem Unterschied, dass Ausschnitte nur in devtools ausgeführt werden und nicht auf die zulässige Länge einer URL begrenzt sind.  

Die Verwendung von Snippets ist eine hervorragende Möglichkeit, ein paar Dinge auf einer Drittanbieter-Webseite zu ändern.  Code Änderungen in Ausschnitten werden der aktuellen Webseite hinzugefügt und im gleichen Kontext ausgeführt.  Weitere Informationen zum Ändern des vorhandenen Codes einer Webseite finden Sie unter [Außerkraftsetzungen][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      In der folgenden Abbildung ist beispielsweise die devtools-Homepage auf der linken Seite und ein Codeausschnitt Quellcode auf der rechten Seite zu sehen.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Die vor dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Die Webseite vor dem Ausführen des Snippets  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Der Snippet-Quellcode auf der Webseite, bevor der Codeausschnitt ausgeführt wird.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

In der folgenden Abbildung wird die Webseite nach dem Ausführen des Snippets angezeigt.  Der **Konsolen Einzug** wird eingeblendet, um die Meldung anzuzeigen, die `Hello, Snippets!` vom Snippet protokolliert wird, und der Inhalt der Webseite ändert sich vollständig.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Die Webseite nach dem Ausführen des Snippets" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Die Webseite nach dem Ausführen des Snippets  
:::image-end:::  

## Öffnen des Bereichs "Snippets"  

Im Bereich **Snippets** werden Ihre Snippets aufgelistet.  Wenn Sie einen Ausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Snippets** öffnen.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Der Bereich "Ausschnitte"" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Der Bereich " **Ausschnitte** "  
:::image-end:::  

### Öffnen des Bereichs "Ausschnitte" mit einer Maus  

1.  Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Tool zu öffnen.  Der **Seiten** Bereich wird normalerweise standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Tool "Quellen" mit geöffnetem Seitenbereich auf der linken Seite" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Das Tool " **Quellen** " mit geöffnetem Seitenbereich auf der linken **Seite**  
    :::image-end:::  
    
1.  Wählen Sie die Registerkarte **Snippets** aus, um den Bereich **Snippets** zu öffnen.  Möglicherweise müssen Sie **weitere Registerkarten** auswählen \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \), um auf die Option **Snippets** zuzugreifen.  
    
### Öffnen des Bereichs "Ausschnitte" mit dem Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Geben `Snippets` Sie **Snippets anzeigen**ein, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl ' Snippets anzeigen '" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Der Befehl ' **Snippets anzeigen** '  
    :::image-end:::  
    
## Erstellen von Ausschnitten  

### Erstellen eines Snippets über das Quellen Panel  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Wählen Sie **Neues Snippet**aus.  
1.  Geben Sie einen Namen für das Snippet ein, und wählen Sie dann `Enter` Speichern aus.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Snippets" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Benennen eines Snippets  
    :::image-end:::  
    
### Erstellen eines Snippets über das Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Geben `Snippet` Sie ein, wählen Sie **Neues Snippet erstellen**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Snippets" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Der Befehl zum Erstellen eines neuen Snippets  
    :::image-end:::  
    
Wenn Sie den neuen Ausschnitt mit einem benutzerdefinierten Namen umbenennen möchten, navigieren Sie zu [Snippets umbenennen](#rename-snippets).  

## Bearbeiten von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Wählen Sie im Bereich **Snippets** den Namen des Ausschnitts aus, den Sie bearbeiten möchten.  Sie wird im **Code-Editor**geöffnet.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Der **Code-Editor**  
    :::image-end:::  
    
1.  Verwenden Sie den **Code-Editor** , um Ihrem Snippet JavaScript hinzuzufügen.  
1.  Wenn neben dem Namen des Snippets ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.  Wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus, um Sie zu speichern.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Namen des Ausschnitts zeigt nicht gespeicherten Code an." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Ein Sternchen neben dem Namen des Ausschnitts zeigt nicht gespeicherten Code an.  
    :::image-end:::  
    
## Ausführen von Ausschnitten  

### Ausführen eines Snippets im Quellen Panel  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Wählen Sie den Namen des Ausschnitts aus, den Sie ausführen möchten.  Das Snippet wird im **Code-Editor**geöffnet.  
1.  Wählen Sie **Snippet ausführen** \ ( ![ Snippet ausführen ][ImageRunSnippetIcon] ) aus, oder wählen Sie `Control` + `Enter` \ (Windows, Linux \) oder `Command` + `Enter` \ (macOS \) aus.  
    
### Ausführen eines Snippets mit dem Befehlsmenü  

1.  Setzen Sie den Cursor an eine beliebige Stelle in devtools.  
1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das Befehlsmenü zu öffnen.  
1.  Löschen `>` Sie das Zeichen, und geben `!` Sie das Zeichen gefolgt vom Namen des Ausschnitts ein, den Sie ausführen möchten.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Snippets über das Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       Ausführen eines Snippets über das **Befehlsmenü**  
    :::image-end:::  
    
1.  Wählen Sie aus `Enter` , um den Ausschnitt auszuführen.  

## Umbenennen von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Zeigen Sie auf den Namen des Snippets, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Umbenennen**aus.  
    
## Löschen von Ausschnitten  

1.  [Öffnen Sie den Bereich **Snippets** ](#open-the-snippets-pane).  
1.  Zeigen Sie auf den Namen des Snippets, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Entfernen**aus.  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das Quellen Tool | Microsoft docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Außerkraftsetzungen | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Zwischenablage | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
