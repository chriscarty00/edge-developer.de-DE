---
description: Codeausschnitte sind kleine Skripts, die Sie im Tool Sources von Microsoft Edge DevTools erstellen und ausführen können.  Sie können von jeder Webseite aus auf Ressourcen zugreifen und diese ausführen.  Wenn Sie einen Codeausschnitt ausführen, wird er aus dem Kontext der aktuell geöffneten Webseite ausgeführt.
title: Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439423"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a>Ausführen von Codeausschnitten von JavaScript auf einer beliebigen Webseite mit Microsoft Edge DevTools  

Wenn Sie denselben Code [][DevtoolsConsoleIndex] wiederholt in der Konsole ausführen, sollten Sie stattdessen den Code als Codeausschnitt speichern.  Codeausschnitte sind Skripts, die Sie im Tool [Quellen][DevToolsSourcesTool] erstellen.  Codeausschnitte haben Zugriff auf den JavaScript-Kontext der Webseite, und Sie können Codeausschnitte auf jeder Beliebigen Webseite ausführen.  Die Sicherheitseinstellungen der meisten Webseiten blockieren das Laden anderer Skripts in Codeausschnitten.  Aus diesem Grund müssen Sie den ganzen Code in einer Datei enthalten.  

Codeausschnitte sind eine Alternative zu [Bookmarklets][WikiBookmarklet] mit dem Unterschied, dass Codeausschnitte nur in DevTools ausgeführt werden und nicht auf die zulässige Länge einer URL beschränkt sind.  

Die Verwendung von Codeausschnitten ist eine hervorragende Möglichkeit, einige Dinge auf einer Webseite eines Drittanbieters zu ändern.  Codeänderungen in Codeausschnitten werden der aktuellen Webseite hinzugefügt und im gleichen Kontext ausgeführt.  Weitere Informationen zum Ändern des vorhandenen Codes einer Webseite finden Sie unter [Overrides][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      In der folgenden Abbildung sind beispielsweise die DevTools-Homepage auf der linken Seite und ein Codeausschnitt auf der rechten Seite dargestellt.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Die vor dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Die Webseite vor dem Ausführen des Codeausschnitts  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Der Codeausschnitt von der Webseite vor dem Ausführen des Codeausschnitts.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

In der folgenden Abbildung wird die Webseite nach dem Ausführen des Codeausschnitts angezeigt.  Die **Konsolenschubschubte** wird angezeigt, um die Nachricht anzuzeigen, die der Codeausschnitt protokolliert, und der Inhalt der `Hello, Snippets!` Webseite ändert sich vollständig.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Die Webseite nach dem Ausführen des Codeausschnitts" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Die Webseite nach dem Ausführen des Codeausschnitts  
:::image-end:::  

## <a name="open-the-snippets-pane"></a>Öffnen des Codeausschnittbereichs  

Im **Bereich Codeausschnitte** werden Ihre Codeausschnitte aufgelistet.  Wenn Sie einen Codeausschnitt bearbeiten möchten, müssen Sie ihn im Bereich **Codeausschnitte** öffnen.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Der Bereich Codeausschnitte" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Der **Bereich Codeausschnitte**  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a>Öffnen des Codeausschnittbereichs mit der Maus  

1.  Wählen Sie die **Registerkarte Quellen** aus, um das Tool **Quellen zu** öffnen.  Der **Seitenbereich** wird in der Regel standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Das Tool Quellen mit links geöffneten Seitenbereich" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Das **Tool Quellen** mit links geöffneten Seitenbereich ****  
    :::image-end:::  
    
1.  Wählen Sie die **Registerkarte Codeausschnitte** aus, um den **Codeausschnittbereich zu** öffnen.  Möglicherweise müssen Sie weitere **Registerkarten** \( Weitere Registerkarten \) auswählen, um ![ auf die Option ](../media/more-tabs-icon.msft.png) **Codeausschnitte zu** zugreifen.  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a>Öffnen Sie den Codeausschnittbereich mit dem Befehlsmenü.  

1.  Fokussieren Sie den Cursor an einer stelle in DevTools.  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.  
1.  Geben `Snippets` Sie ein, **wählen Sie Codeausschnitte**anzeigen aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Der Befehl Codeausschnitte anzeigen" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Der **Befehl Codeausschnitte** anzeigen  
    :::image-end:::  
    
## <a name="create-snippets"></a>Erstellen von Codeausschnitten  

### <a name="create-a-snippet-through-the-sources-panel"></a>Erstellen eines Codeausschnitts über den Bereich Quellen  

1.  [Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).  
1.  Wählen **Sie Neuer Codeausschnitt aus.**  
1.  Geben Sie einen Namen für Ihren Codeausschnitt ein, und wählen Sie dann `Enter` zum Speichern aus.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Benennen eines Codeausschnitts" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Benennen eines Codeausschnitts  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a>Erstellen eines Codeausschnitts über das Befehlsmenü  

1.  Fokussieren Sie den Cursor an einer stelle in DevTools.  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.  
1.  Geben `Snippet` Sie ein, wählen **Sie Neuen Codeausschnitt erstellen**aus, und wählen Sie dann `Enter` aus, um den Befehl auszuführen.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Der Befehl zum Erstellen eines neuen Codeausschnitts" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Der Befehl zum Erstellen eines neuen Codeausschnitts  
    :::image-end:::  
    
Um Ihren neuen Codeausschnitt mit einem benutzerdefinierten Namen umzubenennen, navigieren Sie zu [Umbenennen von Codeausschnitten](#rename-snippets).  

## <a name="edit-snippets"></a>Bearbeiten von Codeausschnitten  

1.  [Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).  
1.  Wählen Sie im Bereich Codeausschnitte den Namen des **Codeausschnitts** aus, den Sie bearbeiten möchten.  Es wird im **Code-Editor geöffnet.**  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Der Code-Editor" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Der **Code-Editor**  
    :::image-end:::  
    
1.  Verwenden Sie **den Code-Editor,** um Ihrem Codeausschnitt JavaScript hinzuzufügen.  
1.  Wenn neben dem Namen Ihres Codeausschnitts ein Sternchen angezeigt wird, bedeutet dies, dass Sie nicht gespeicherten Code haben.  Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Ein Sternchen neben dem Codeausschnittnamen gibt nicht gespeicherten Code an.  
    :::image-end:::  
    
## <a name="run-snippets"></a>Ausführen von Codeausschnitten  

### <a name="run-a-snippet-from-the-sources-panel"></a>Ausführen eines Codeausschnitts im Bereich Quellen  

1.  [Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).  
1.  Wählen Sie den Namen des Codeausschnitts aus, den Sie ausführen möchten.  Der Codeausschnitt wird im **Code-Editor geöffnet.**  
1.  Wählen **Sie Codeausschnitt** ausführen \( ![ Codeausschnitt ausführen ](../media/run-snippet-icon.msft.png) \) oder `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\).  
    
### <a name="run-a-snippet-with-the-command-menu"></a>Ausführen eines Codeausschnitts mit dem Befehlsmenü  

1.  Fokussieren Sie den Cursor an einer stelle in DevTools.  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü zu öffnen.  
1.  Löschen Sie das Zeichen, und geben Sie das Zeichen gefolgt vom Namen des Codeausschnitts ein, `>` `!` den Sie ausführen möchten.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ausführen eines Codeausschnitts aus dem Befehlsmenü" lightbox="../media/javascript-search-run-command.msft.png":::
       Ausführen eines Codeausschnitts aus dem **Befehlsmenü**  
    :::image-end:::  
    
1.  Wählen `Enter` Sie diese Option aus, um den Codeausschnitt ausführen zu können.  

## <a name="rename-snippets"></a>Umbenennen von Codeausschnitten  

1.  [Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).  
1.  Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Umbenennen aus.**  
    
## <a name="delete-snippets"></a>Löschen von Codeausschnitten  

1.  [Öffnen Sie den **Bereich Codeausschnitte** ](#open-the-snippets-pane).  
1.  Zeigen Sie auf den Codeausschnittnamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Entfernen aus.**  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Konsolenübersicht | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Außerkraftsetzungen | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad-| MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-| Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
