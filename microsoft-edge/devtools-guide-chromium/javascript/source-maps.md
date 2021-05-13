---
description: Halten Sie ihren clientseitigen Code auch nach dem Kombinieren, Minimieren oder Kompilieren lesbar und debuggbar.
title: Zuordnung von vorverarbeiteten Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3240e437a917dd7074a0584b91dcc6c34576ca24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564049"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="map-preprocessed-code-to-source-code"></a>Zuordnung von vorverarbeiteten Code zu Quellcode  

Halten Sie ihren clientseitigen Code auch nach dem Kombinieren, Minimieren oder Kompilieren lesbar und debuggbar.  Verwenden Sie Quellzuordnungen, um Den Quellcode dem kompilierten Code zu zuordnungen.  

### <a name="summary"></a>Zusammenfassung  

*   Verwenden Sie source Karten, um dem Quellcode minifizierten Code zu zuordnungen.  Anschließend können Sie kompilierten Code in der ursprünglichen Quelle lesen und debuggen.  
*   Verwenden Sie nur Vorverarbeiter, die Quellprozessoren Karten.  
*   Stellen Sie sicher, dass Ihr Webserver Quellserver Karten.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Erste Schritte mit Präprozessoren  

In diesem Artikel wird erläutert, wie Sie mit JavaScript Source Karten im Tool DevTools Sources interagieren.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Verwenden eines unterstützten Präprozessors  

Verwenden Sie ein Minifier, mit dem Quellzuordnungen erstellt werden können.  <!--For the most popular options, navigate to preprocessor support section.  -->  Navigieren Sie für eine erweiterte Ansicht zu [Quellzuordnungen: Sprachen, Tools und andere Info-Wiki-Seite.][GitHubWikiSourceMapsLanguagesTools]  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Source-Karten:  

*   Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiler \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)  
*   Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-tool"></a>Source Karten in DevTools Sources tool  

Quelldateien Karten von Präprozessoren führen dazu, dass DevTools ihre ursprünglichen Dateien zusätzlich zu den minifizierten Dateien geladen.  Anschließend verwenden Sie die Originale, um Haltepunkte zu setzen und Code zu durchbrechen.  In der zwischenzeit Microsoft Edge tatsächlich ihren minifizierten Code ausgeführt.  Die Ausführung des Codes gibt Ihnen die Illusion, eine Entwicklungswebsite in der Produktion zu verwenden.  

Wenn Sie source Karten in DevTools ausführen, sollten Sie feststellen, dass javaScript nicht kompiliert wird und alle einzelnen JavaScript-Dateien angezeigt werden, auf die es verweist.  Source Karten in DevTools verwendet die Quellzuordnung, aber die zugrunde liegende Funktionalität führt tatsächlich den kompilierten Code aus.  Alle Fehler, Protokolle und Haltepunkte werden dem Entwicklungscode für ein großartiges Debuggen hinzugefügt.  Es gibt Ihnen also die Illusion, dass Sie eine Entwicklungswebsite in der Produktion ausführen.  

### <a name="enable-source-maps-in-settings"></a>Aktivieren von Karten in Einstellungen  

Quelldateien Karten standardmäßig aktiviert<!-- \(as of Microsoft Edge 39\)-->, wenn Sie sie jedoch überprüfen oder aktivieren möchten; Öffnen Sie zunächst DevTools, wählen **Sie Anpassen und Steuern von DevTools** \( `...` \) > **Einstellungen**.  Aktivieren Sie **im Bereich** Einstellungen unter **Quellen**die Option **JavaScript Source Karten**.  Sie können auch die Option **CSS-Quelldatei aktivieren Karten.**  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Aktivieren von Karten" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Aktivieren von JavaScript Source Karten**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Debuggen mit Karten  

Beim Debuggen des Codes und Karten Source Karten source Karten an zwei Stellen:  

1.  In der Konsole \(Der Link zur Quelle sollte die ursprüngliche Datei sein, nicht die generierte\)  
1.  Beim Schrittweisen durch Code \(Die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen\)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a>@sourceURL und displayName  

Obwohl sie nicht Teil der Quellzuordnungsspezifikation sind, können Sie die Entwicklung bei der Arbeit mit `@sourceURL` Evals erheblich vereinfachen.  Die Hilfshilfe wird ähnlich wie die Eigenschaft angezeigt und `//# sourceMappingURL` in den Source Map V3-Spezifikationen erwähnt.  

Durch das Hinzufügen des folgenden speziellen Kommentars in Ihren Code, der ausweicht, können Sie Evals und Inlineskripts und Formatvorlagen benennen, sodass jede als logischere Namen in Ihren DevTools angezeigt wird.  

```javascript
//# sourceURL=source.coffee
```  

Navigieren Sie zur folgenden Seite.  

*   [Demo][CssNinjaDemoSourceMapping]

Führen Sie die folgenden Aktionen aus.  

1.  Öffnen Sie DevTools, und navigieren Sie zum **Tool Quellen.**  
1.  Geben Sie einen Dateinamen in das Eingabefeld **Name your code:** ein.  
1.  Wählen Sie **die Kompilierungsschaltfläche** aus.  
1.  Es wird eine Warnung mit der ausgewerteten Summe aus der CoffeeScript-Quelle angezeigt.  
    
Wenn Sie den Unterbereich **Quellen** erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.  Wenn Sie doppelklicken, um diese Datei zu sehen, enthält sie das kompilierte JavaScript für die ursprüngliche Quelle.  In der letzten Zeile befindet sich jedoch ein Kommentar, der `// @sourceURL` die ursprüngliche Quelldatei angibt.  Dies kann Ihnen beim Debuggen beim Arbeiten mit Sprachabstraktionen helfen.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Arbeiten mit sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Arbeiten mit `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel ist ein #A0"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Ein einfaches Beispiel für die Benennung von #A0"  

[DartMain]: https://www.dartlang.org "Dart-Programmiersprache"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/closure-compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Quellkarten: Sprachen, Tools und andere | GitHub Wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Erste Schritte – google/traceur-compiler | GitHub Wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) befindet sich hier und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation und UX\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
