---
description: Anzeigen und Bearbeiten von Dateien, Erstellen von Ausschnitten, Debuggen von JavaScript und Einrichten von Arbeitsbereichen im Quellen Panel von Microsoft Edge devtools
title: Übersicht über das Quellenpanel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233720"
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

# Übersicht über das Quellenpanel  

Verwenden Sie das Panel Microsoft Edge devtools **Sources** , um die folgenden Aktionen auszuführen.  

*   [Anzeigen von Dateien](#display-files)  
*   [Bearbeiten Sie CSS und JavaScript](#edit-css-and-javascript).  
*   Sie können [JavaScript- **Snippets** erstellen und speichern](#create-save-and-run-snippets), die Sie möglicherweise auf einer beliebigen Webseite ausführen.  **Snippets** ähneln Bookmarklets.  
*   [Debuggen von JavaScript](#debug-javascript)  
*   [Richten Sie einen Arbeitsbereich ein](#set-up-a-workspace), damit Änderungen, die Sie in devtools vornehmen, in dem Code Ihres Dateisystems gespeichert werden.  
    
## Anzeigen von Dateien  

Verwenden Sie den **Seiten** Bereich, um alle Ressourcen anzuzeigen, die von der Seite geladen wurden.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Seitenbereich" lightbox="../media/sources-page-pane.msft.png":::
   **Seiten** Bereich  
:::image-end:::  

Organisation des **Seiten** Bereichs:  
*   Die oberste Ebene, wie `top` in der vorherigen Abbildung, stellt einen [HTML-Frame][W3CHtml4Frames]dar.  Finden `top` Sie auf jeder Seite, die Sie besuchen.  `top` stellt den Hauptdokument Frame dar.  
*   Die zweite Ebene, wie `docs.microsoft.com` in der vorhergehenden Abbildung, stellt einen [Ursprung][HtmlstandardOrigin]dar.  
*   Die dritte Ebene, die vierte Ebene usw., stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.  In der vorherigen Abbildung wird beispielsweise der vollständige Pfad zur Ressource `devtools-guide-chromium` `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Wählen Sie im **Seiten** Bereich eine Datei aus, um den Inhalt im **Editor** Bereich anzuzeigen.  Sie können jede Art von Datei anzeigen.  Bei Bildern wird eine Vorschau des Bilds angezeigt.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Anzeigen der Inhalte von a4d10f71.index-docs.js im Bereich Editor" lightbox="../media/sources-editor-pane.msft.png":::
   Anzeigen des Inhalts `a4d10f71.index-docs.js` im Bereich " **Editor** "  
:::image-end:::  

## Bearbeiten von CSS und JavaScript  

Verwenden Sie den **Editor** Bereich, um CSS und JavaScript zu bearbeiten.  DevTools aktualisiert die Seite, um den neuen Code auszuführen.  Wenn Sie beispielsweise eine CSS-Datei bearbeiten, indem Sie unten die Stilregel hinzufügen:

```css
.metadata.page-metadata {
    color: red;
}
```

Diese Änderung sollte sofort wirksam werden.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editor Bereich zum Ändern der Textfarbe des Untertitels in rot" lightbox="../media/edit-css.msft.png":::
   Bearbeiten von CSS im **Editor** Bereich zum Ändern der Textfarbe des Untertitels in rot  
:::image-end:::  

CSS-Änderungen werden sofort wirksam, keine Speicherung erforderlich.  Damit JavaScript-Änderungen wirksam werden, wählen Sie `Control` + `S` \ (Windows, Linux \) oder `Command` + `S` \ (macOS \) aus.  DevTools führt ein Skript nicht erneut aus, sodass nur die JavaScript-Änderungen wirksam werden, die Sie in Funktionen vornehmen.  Beachten Sie beispielsweise in der folgenden Abbildung, wie diese `console.log('A')` nicht ausgeführt wird, während `console.log('B')` dies der Fall ist.  Wenn devtools das gesamte Skript nach dem vornehmen der Änderung erneut ausführt, wurde der Text `A` in der **Konsole**protokolliert.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Bearbeiten von JavaScript im Bereich Editor" lightbox="../media/edit-js.msft.png":::
   Bearbeiten von JavaScript im Bereich " **Editor** "  
:::image-end:::  

DevTools löscht Ihre CSS-und JavaScript-Änderungen beim erneuten Laden der Seite.  Navigieren Sie zum [Einrichten eines Arbeitsbereichs](#set-up-a-workspace) , um zu erfahren, wie Sie die Änderungen in Ihrem Dateisystem speichern.  

## Erstellen, speichern und Ausführen von Ausschnitten  

Snippets sind Skripts, die auf einer beliebigen Seite ausgeführt werden können.  Stellen Sie sich vor, dass Sie den folgenden Code wiederholt in der **Konsole**eingeben, um die jQuery-Bibliothek auf einer Seite einzufügen, damit Sie jQuery-Befehle über die **Konsole**ausführen können.  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Stattdessen können Sie diesen Code in einem **Snippet** speichern und mit ein paar Klicks auf die Schaltfläche ausführen, wenn Sie ihn benötigen.  DevTools speichert das **Snippet** in Ihrem Dateisystem.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Snippet, das die jQuery-Bibliothek auf einer Seite einfügt" lightbox="../media/snippet.msft.png":::
   Ein **Snippet** , das die jQuery-Bibliothek auf einer Seite einfügt  
:::image-end:::  

So führen Sie einen **Ausschnitt**aus:

*   Öffnen Sie die Datei über den Bereich **Snippets** , und wählen Sie **Ausführen** \ ( ![ die Schaltfläche Ausführen ][ImageRunIcon] \) aus.  
*   Öffnen Sie das [Menübefehl][DevtoolsGuideChromiumCommandMenuIndex], löschen `>` Sie das Zeichen, geben `!` Sie den Namen des **Snippets**ein, und wählen Sie dann aus `Enter` .  
    
Navigieren Sie zum [Ausführen von Codeausschnitten auf jeder Seite][DevtoolsGuideChromiumJavascriptSnippets] , um weitere Informationen zu erhalten.

## Debuggen von JavaScript  

Anstatt `console.log()` abzuleiten, wo Ihr JavaScript schief läuft, sollten Sie stattdessen die Microsoft Edge DevTools-Debugging-Tools verwenden.  Die allgemeine Idee ist, einen Haltepunkt zu definieren, der eine absichtliche Unterbrechung in Ihrem Code ist, und dann schrittweise durch die Laufzeit des Codes eine Zeile zu einem Zeitpunkt zu führen.  Wenn Sie den Code schrittweise durchlaufen, können Sie die Werte aller aktuell definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.

Navigieren Sie zu den [ersten Schritten beim Debuggen von JavaScript][DevtoolsGuideChromiumJavascriptIndex] , um die Grundlagen des Debuggens in devtools zu erfahren.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Debuggen von JavaScript" lightbox="../media/debugging.msft.png":::
   Debuggen von JavaScript  
:::image-end:::  

## Einrichten eines Arbeitsbereichs  

Wenn Sie eine Datei im **Quellen** Tool bearbeiten, gehen diese Änderungen standardmäßig verloren, wenn Sie die Seite erneut laden.  Mit **Arbeitsbereichen** können Sie die Änderungen, die Sie in devtools vornehmen, in Ihrem Dateisystem speichern.  Im Wesentlichen kann devtools als Code-Editor verwendet werden.

Navigieren Sie zu den ersten Schritten, um [Dateien mit Arbeitsbereichen zu bearbeiten][DevtoolsGuideChromiumWorkspacesIndex] .

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Herkunft | HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
