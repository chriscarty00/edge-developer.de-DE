---
description: Anzeigen und Bearbeiten von Dateien, Erstellen von Codeausschnitten, Debuggen von JavaScript und Einrichten von Arbeitsbereichen im Bereich Quellen von Microsoft Edge DevTools.
title: Übersicht über das Quellenpanel
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4677bf82d3506a4b8d6336ded7ab557b794fd3df
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397762"
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

# <a name="sources-panel-overview"></a>Übersicht über das Quellenpanel  

Verwenden Sie den **** Microsoft Edge DevTools Sources-Bereich, um die folgenden Aktionen durchzuführen.  

*   [Anzeigen von Dateien](#display-files).  
*   [Bearbeiten von CSS und JavaScript](#edit-css-and-javascript).  
*   [Erstellen und speichern **Sie Codeausschnitte** von JavaScript](#create-save-and-run-snippets), die Sie auf jeder Beliebigen Webseite ausführen können.  **Codeausschnitte** ähneln Bookmarklets.  
*   [Debuggen von JavaScript](#debug-javascript).  
*   [Richten Sie einen Arbeitsbereich](#set-up-a-workspace)ein, damit Änderungen, die Sie in DevTools vornehmen, im Code ihres Dateisystems gespeichert werden.  
    
## <a name="display-files"></a>Anzeigen von Dateien  

Verwenden **** Des Seitenbereichs; , um alle Ressourcen, die die Seite geladen hat, anzeigen zu können.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Seitenbereich" lightbox="../media/sources-page-pane.msft.png":::
   **Seitenbereich**  
:::image-end:::  

So wird **der Seitenbereich** organisiert:  
*   Die oberste Ebene, z. B. `top` in der vorherigen Abbildung, stellt einen [HTML-Frame dar.][W3CHtml4Frames]  Suchen `top` Sie auf jeder Seite, die Sie besuchen.  `top` stellt den Hauptdokumentrahmen dar.  
*   Die zweite Ebene, z. B. `docs.microsoft.com` in der vorherigen Abbildung, stellt einen [Ursprung dar.][HtmlstandardOrigin]  
*   Die dritte Ebene, die vierte Ebene und so weiter stellen Verzeichnisse und Ressourcen dar, die von diesem Ursprung geladen wurden.  In der vorherigen Abbildung ist z. B. der vollständige Pfad zur `devtools-guide-chromium` Ressource `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Wählen Sie eine Datei im **Bereich Seite** aus, um den Inhalt im **Editorbereich anzuzeigen.**  Sie können einen beliebigen Dateityp anzeigen.  Für Bilder wird eine Vorschau des Bilds angezeigt.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Anzeigen des Inhalts von a4d10f71.index-docs.js im Editorbereich" lightbox="../media/sources-editor-pane.msft.png":::
   Anzeigen des Inhalts `a4d10f71.index-docs.js` im **Editorbereich**  
:::image-end:::  

## <a name="edit-css-and-javascript"></a>Bearbeiten von CSS und JavaScript  

Verwenden Sie den **Editorbereich,** um CSS und JavaScript zu bearbeiten.  DevTools aktualisiert die Seite, um den neuen Code ausführen zu können.  Wenn Sie z. B. eine CSS-Datei bearbeiten, indem Sie die folgende Formatvorlagenregel hinzufügen:

```css
.metadata.page-metadata {
    color: red;
}
```

Diese Änderung sollte sofort wirksam werden.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editorbereich, um die Textfarbe des Untertitels in Rot zu ändern" lightbox="../media/edit-css.msft.png":::
   Bearbeiten von CSS im **Editorbereich,** um die Textfarbe des Untertitels in Rot zu ändern  
:::image-end:::  

CSS-Änderungen werden sofort wirksam, es ist kein Speichern erforderlich.  Damit JavaScript-Änderungen wirksam werden, wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\).  DevTools führt kein Skript erneut aus, daher sind die einzigen JavaScript-Änderungen, die wirksam werden, diejenigen, die Sie innerhalb von Funktionen vornehmen.  Beachten Sie beispielsweise in der folgenden Abbildung, wie `console.log('A')` nicht ausgeführt wird. `console.log('B')`  Wenn DevTools das gesamte Skript nach der Änderung erneut ausgeführt hat, wird der Text `A` bei der **Konsole protokolliert.**  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Bearbeiten von JavaScript im Editorbereich" lightbox="../media/edit-js.msft.png":::
   Bearbeiten von JavaScript im **Editorbereich**  
:::image-end:::  

DevTools löscht Ihre CSS- und JavaScript-Änderungen, wenn Sie die Seite aktualisieren.  Navigieren Sie [zu Einrichten eines Arbeitsbereichs,](#set-up-a-workspace) um zu erfahren, wie Sie die Änderungen an Ihrem Dateisystem speichern.  

## <a name="create-save-and-run-snippets"></a>Erstellen, Speichern und Ausführen von Codeausschnitten  

Codeausschnitte sind Skripts, die Sie auf jeder Beliebigen Seite ausführen können.  Stellen Sie sich vor, Sie geben den folgenden Code wiederholt in die Konsole **ein,** um die jQuery-Bibliothek in eine Seite zu einfügen, damit Sie jQuery-Befehle aus der Konsole **ausführen können.**  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Stattdessen können Sie diesen Code in einem Codeausschnitt **speichern** und mit ein paar Schaltflächenklicks ausführen, wenn Sie ihn benötigen.  DevTools speichert den **Codeausschnitt** in Ihrem Dateisystem.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Codeausschnitt, der die jQuery-Bibliothek in eine Seite einfüge" lightbox="../media/snippet.msft.png":::
   Ein **Codeausschnitt,** der die jQuery-Bibliothek in eine Seite einfüge  
:::image-end:::  

So führen Sie einen **Codeausschnitt aus:**

*   Öffnen Sie die Datei mithilfe des **Codeausschnittbereichs,** und wählen Sie **Ausführen** \( ![ Die Schaltfläche Ausführen ][ImageRunIcon] \).  
*   Öffnen Sie [das Befehlsmenü,][DevtoolsGuideChromiumCommandMenuIndex]löschen Sie das Zeichen, geben Sie ein, geben Sie den Namen Ihres Codeausschnitts `>` `!` ein, und wählen Sie dann **** `Enter` aus.  
    
Navigieren Sie [zu Codeausschnitte von beliebigen Seiten ausführen,][DevtoolsGuideChromiumJavascriptSnippets] um weitere Informationen zu erhalten.

## <a name="debug-javascript"></a>Debuggen von JavaScript  

Anstatt zu verwenden, um zu abfingen, wo Ihr JavaScript falsch läuft, sollten Sie stattdessen die `console.log()` Microsoft Edge DevTools-Debuggingtools verwenden.  Die allgemeine Idee besteht im Festlegen eines Haltepunkts, bei dem es sich um einen beabsichtigten Stopport im Code handelt, und dann die Laufzeit des Codes, eine Zeile nach der anderen, zu durchbrechen.  Wenn Sie den Code durchschritten, können Sie die Werte aller derzeit definierten Eigenschaften und Variablen anzeigen und ändern, JavaScript in der **Konsole**ausführen und vieles mehr.

Navigieren Sie zu Erste Schritte mit Debuggen von [JavaScript,][DevtoolsGuideChromiumJavascriptIndex] um die Grundlagen des Debuggens in DevTools zu erfahren.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Debuggen von JavaScript" lightbox="../media/debugging.msft.png":::
   Debuggen von JavaScript  
:::image-end:::  

## <a name="set-up-a-workspace"></a>Einrichten eines Arbeitsbereichs  

Wenn Sie eine Datei im **** Tool Quellen bearbeiten, gehen diese Änderungen beim Aktualisieren der Seite standardmäßig verloren.  **Mit Arbeitsbereichen** können Sie die Änderungen, die Sie in DevTools vornehmen, in Ihrem Dateisystem speichern.  Im Wesentlichen kann DevTools als Code-Editor verwendet werden.

Navigieren Sie [zu Bearbeiten von Dateien mit Arbeitsbereichen,][DevtoolsGuideChromiumWorkspacesIndex] um die ersten Schritte zu starten.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft Docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Ursprung | HTML-Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
