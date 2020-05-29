---
title: Übersicht über das Quellen Panel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601908"
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
   limitations under the License. -->






# Übersicht über das Quellen Panel 



Verwenden Sie das Microsoft Edge devtools **Sources** Panel für folgende Zwecke:

*   [Dateien anzeigen](#view-files).  
*   [Bearbeiten Sie CSS und JavaScript](#edit-css-and-javascript).  
*   Sie können [JavaScript- **Snippets** erstellen und speichern](#create-save-and-run-snippets), die Sie möglicherweise auf einer beliebigen Seite ausführen.  **Snippets** ähneln Bookmarklets.  
*   [Debuggen von JavaScript](#debug-javascript)  
*   [Richten Sie einen Arbeitsbereich ein](#set-up-a-workspace), damit Änderungen, die Sie in devtools vornehmen, in dem Code Ihres Dateisystems gespeichert werden.  

## Anzeigen von Dateien 

Verwenden Sie den **Seiten** Bereich, um alle Ressourcen anzuzeigen, die von der Seite geladen wurden.

> ##### Abbildung1  
> **Seiten** Bereich  
> ![Abbildung 1: der Seitenbereich][ImageSourcesPagePane]  

Organisation des **Seiten** Bereichs:  
*   Die oberste Ebene, wie `top` in [**Abbildung 1**](#figure-1), stellt einen [HTML-Frame][W3CHtml4Frames]dar.  Finden `top` Sie auf jeder Seite, die Sie besuchen. `top` stellt den Hauptdokument Frame dar.  
*   Die zweite Ebene, wie `docs.microsoft.com` in [**Abbildung 1**](#figure-1), stellt einen [Ursprung][HtmlstandardOrigin]dar.  
*   Die dritte Ebene, die vierte Ebene usw., stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.  In [**Abbildung 1**](#figure-1) wird beispielsweise der vollständige Pfad zur Ressource `devtools-guide-chromium` `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

Klicken Sie im **Seiten** Bereich auf eine Datei, um den Inhalt im **Editor** Bereich anzuzeigen.  Sie können jede Art von Datei anzeigen. Für Bilder wird eine Vorschau des Bilds angezeigt.  

> ##### Abbildung2  
> Anzeigen des Inhalts `a4d10f71.index-docs.js` im Bereich " **Editor** "  
> ![Abbildung2. Anzeigen des Inhalts von "a4d10f71. Index-docs. js" im Bereich "Editor"][ImageSourcesEditorPane]  

## Bearbeiten von CSS und JavaScript 

Verwenden Sie den **Editor** Bereich, um CSS und JavaScript zu bearbeiten.  DevTools aktualisiert die Seite, um den neuen Code auszuführen. Wenn Sie beispielsweise eine CSS-Datei bearbeiten, indem Sie unten die Stilregel hinzufügen:

```css
.metadata.page-metadata {
    color: red;
}
```

Sie sollten sehen, dass die Änderung sofort wirksam wird.

> ##### Abbildung 3  
> Bearbeiten von CSS im **Editor** Bereich zum Ändern der Textfarbe des Untertitels in rot  
> ![Abbildung3. Bearbeiten von CSS im Editor Bereich zum Ändern der Textfarbe des Untertitels in rot][ImageEditCSS]  

CSS-Änderungen werden sofort wirksam, keine Speicherung erforderlich. Damit JavaScript-Änderungen wirksam werden, drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \). DevTools führt ein Skript nicht erneut aus, sodass nur die JavaScript-Änderungen wirksam werden, die Sie in Funktionen vornehmen.  In [**Abbildung 4**](#figure-4) wird beispielsweise beschrieben, wie die Funktion `console.log('A')` nicht ausgeführt wird, während `console.log('B')` dies der Fall ist. Wenn devtools das gesamte Skript nach dem vornehmen der Änderung erneut ausgeführt hat, wurde der Text `A` in der **Konsole**protokolliert.  

> ##### Abbildung4  
> Bearbeiten von JavaScript im Bereich " **Editor** "  
> ![Abbildung 4. Bearbeiten von JavaScript im Bereich "Editor"][ImageEditJS]  

DevTools löscht Ihre CSS-und JavaScript-Änderungen beim erneuten Laden der Seite. Informationen zum Speichern der Änderungen an Ihrem Dateisystem finden Sie unter [Einrichten eines Arbeitsbereichs](#set-up-a-workspace) .  

## Erstellen, speichern und Ausführen von Ausschnitten 

Snippets sind Skripts, die auf einer beliebigen Seite ausgeführt werden können. Stellen Sie sich vor, dass Sie den folgenden Code wiederholt in der **Konsole**eingeben, um die jQuery-Bibliothek auf einer Seite einzufügen, damit Sie jQuery-Befehle über die **Konsole**ausführen können:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Stattdessen können Sie diesen Code in einem **Snippet** speichern und mit ein paar Klicks auf die Schaltfläche ausführen, wenn Sie ihn benötigen.  DevTools speichert das **Snippet** in Ihrem Dateisystem.  

> ##### Abbildung5  
> Ein **Snippet** , das die jQuery-Bibliothek auf einer Seite einfügt  
> ![Abbildung5. Ein Snippet, das die jQuery-Bibliothek auf einer Seite einfügt][ImageSnippet]  

So führen Sie einen **Ausschnitt**aus:

*   Öffnen **Sie die** Datei über den Bereich **Snippets** , und klicken Sie auf ![ die Schaltfläche Ausführen ][ImageRunIcon] .  
*   Öffnen Sie das **[Menübefehl][DevtoolsGuideChromiumCommandMenuIndex]**, löschen `>` Sie das Zeichen, geben `!` Sie den Namen des **Snippets**ein, und drücken Sie dann `Enter` .  

Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevtoolsGuideChromiumJavascriptSnippets] .


## Debuggen von JavaScript 

Anstatt `console.log()` abzuleiten, wo Ihr JavaScript schief läuft, sollten Sie stattdessen die Microsoft Edge DevTools-Debugging-Tools verwenden. Die allgemeine Idee ist, einen Haltepunkt zu definieren, der eine absichtliche Unterbrechung in Ihrem Code ist, und dann schrittweise durch die Laufzeit des Codes eine Zeile zu einem Zeitpunkt zu führen. Wenn Sie den Code schrittweise durchlaufen, können Sie die Werte aller aktuell definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.

Informationen zu den Grundlagen des Debuggens in devtools finden Sie unter [Erste Schritte beim Debuggen von JavaScript][DevtoolsGuideChromiumJavascriptIndex] .

> ##### Abbildung6  
> Debuggen von JavaScript  
> ![Abbildung6. Debuggen von JavaScript][ImageDebugging]  

## Einrichten eines Arbeitsbereichs 

Wenn Sie eine Datei im **Quellen** Panel bearbeiten, gehen diese Änderungen standardmäßig verloren, wenn Sie die Seite erneut laden.  Mit **Arbeitsbereichen** können Sie die Änderungen, die Sie in devtools vornehmen, in Ihrem Dateisystem speichern.  Im Wesentlichen können Sie damit devtools als Code-Editor verwenden.

Weitere Informationen finden Sie unter [Bearbeiten von Dateien mit Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex] .

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Abbildung 1: der Seitenbereich"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Abbildung 2: Anzeigen des Inhalts von "a4d10f71. Index-docs. js" im Bereich "Editor""  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Abbildung 3: Bearbeiten von CSS im Editor Bereich zum Ändern der Textfarbe des Untertitels in rot"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Abbildung 4: Bearbeiten von JavaScript im Bereich "Editor""  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Abbildung 5: ein Snippet, das die jQuery-Bibliothek auf einer Seite einfügt"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Abbildung 6: Debuggen von JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Bearbeiten von Dateien mit Arbeitsbereichen"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin-HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
