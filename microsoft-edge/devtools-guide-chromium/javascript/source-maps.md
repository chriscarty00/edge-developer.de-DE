---
description: Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.
title: Zuordnen von vorverarbeitetem Code zu Quellcode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bd04c7bae6f57d4fe3f9b293d70775aa99db3dd1
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993233"
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

# Zuordnen von vorverarbeitetem Code zu Quellcode  

Halten Sie den clientseitigen Code lesbar und debugfähigen, selbst nachdem Sie ihn kombiniert, minify oder kompiliert haben.  Verwenden Sie Quell Karten, um Ihren Quellcode dem kompilierten Code zuzuordnen.  

### Zusammenfassung  

*   Verwenden Sie Quell Karten, um Quellcode minimierte-Code zuzuordnen. Sie können dann kompilierten Code in der ursprünglichen Quelle lesen und Debuggen.  
*   Verwenden Sie nur Pre-Processors, die Quell Karten erstellen können.  
*   Überprüfen Sie, ob Ihr Webserver Quell Karten bereitstellen kann.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## Erste Schritte mit Präprozessoren  

In diesem Artikel wird erläutert, wie Sie mit JavaScript-Quell Karten im devtools-Quellen Panel interagieren.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## Verwenden eines unterstützten Präprozessors  

Sie müssen ein minifier verwenden, das Quell Karten erstellen kann.  <!--For the most popular options, see the preprocessor support section.  -->  Eine erweiterte Ansicht finden Sie unter [Quell Karten: Sprachen, Tools und andere Info][GitHubWikiSourceMapsLanguagesTools] -Wiki-Seite.  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Die folgenden Typen von Präprozessoren werden häufig in Kombination mit Quell Karten verwendet:  

*   Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiler \ ([Closure-Compiler][GitHubGoogleClosureCompiler], [Manuskript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)  
*   Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)  
    
## Quell Karten im devtools-Quellen Panel  

Quell Karten von Präprozessoren führen dazu, dass devtools Ihre Originaldateien zusätzlich zu ihren minimierte lädt.  Anschließend verwenden Sie die originale, um Haltepunkte und schrittweise Code zu definieren.  In der Zwischenzeit wird von Microsoft Edge tatsächlich der minimierte-Code ausgeführt. Dies gibt Ihnen die Illusion, eine Entwicklungswebsite in Production zu betreiben.  

Beim Ausführen von Quell Karten in devtools sollten Sie feststellen, dass das JavaScript nicht kompiliert wurde und Sie alle einzelnen JavaScript-Dateien anzeigen können, auf die es verweist.  Dies verwendet die Quell Zuordnung, doch hinter den Kulissen wird der kompilierte Code tatsächlich ausgeführt.  Alle Fehler, Protokolle und Haltepunkte werden dem dev-Code für awesome Debugging zugeordnet!  So erhalten Sie in der Tat die Illusion, dass Sie eine dev-Website in Production ausführen.  

### Aktivieren von Quell Karten in den Einstellungen  

Quell Karten sind standardmäßig aktiviert. <!--\(as of Microsoft Edge 39\)-->, aber wenn Sie diese überprüfen oder aktivieren möchten, Öffnen Sie zuerst devtools, klicken Sie auf die Schaltfläche **anpassen und Steuern devtools** \ ( `...` \), und wählen Sie **Einstellungen**aus.  Aktivieren Sie im Bereich **Einstellungen** unter **Quellen**die **Option JavaScript-Quell Karten aktivieren**.  Sie können auch die **Option "CSS-Quell Karten aktivieren" aktivieren**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Quell Karten aktivieren" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Aktivieren von JavaScript-Quell Karten**  
:::image-end:::  

### Debuggen mit Quell Karten  

Wenn Sie Ihren Code und die Quell Karten Debuggen aktiviert haben, werden Quell Karten an zwei Stellen angezeigt:  

1.  In der Konsole \ (der Link zur Quelle sollte die ursprüngliche Datei und nicht die generierte sein. \)  
1.  Wenn Sie Code durchlaufen \ (die Links in der Aufrufliste sollten die ursprüngliche Quelldatei öffnen \)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## @sourceURL und DisplayName  

Obwohl es sich nicht um die Quell Karten Spezifikation handelt, `@sourceURL` können Sie die Entwicklung beim Arbeiten mit evals erheblich vereinfachen.  Dieser Helfer sieht der Eigenschaft sehr ähnlich `//# sourceMappingURL` und wird in den Spezifikationen des Quell Karten-V3-Codes tatsächlich erwähnt.  

Indem Sie den folgenden speziellen Kommentar in Ihren Code einbeziehen, der EVALED ist, können Sie evals und Inlineskripts und-Formatvorlagen benennen, damit jeder in Ihrem devtools als logischere Namen angezeigt wird.  

```javascript
//# sourceURL=source.coffee
```  

Navigieren Sie zur folgenden Seite.  

*   [Demo][CssNinjaDemoSourceMapping]

Führen Sie die folgenden Aktionen aus.  

1.  Öffnen Sie das devtools, und wechseln Sie zum **Quellen** Panel.  
1.  Geben Sie einen Dateinamen in das Eingabefeld " **Name Your Code:** " ein.  
1.  Klicken Sie auf die Schaltfläche **Kompilieren** .  
1.  Eine Benachrichtigung mit der ausgewerteten Summe aus der CoffeeScript-Quelle wird angezeigt.  
    
Wenn Sie die Untergruppe " **Quellen** " erweitern, wird nun eine neue Datei mit dem benutzerdefinierten Dateinamen angezeigt, den Sie zuvor eingegeben haben.  Wenn Sie zum Anzeigen dieser Datei doppelklicken, enthält Sie das kompilierte JavaScript für die ursprüngliche Quelle.  In der letzten Zeile ist jedoch ein Kommentar, `// @sourceURL` der die ursprüngliche Quelldatei angibt.  Dies kann Ihnen beim Debuggen beim Arbeiten mit sprach Abstraktionen helfen.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Arbeiten mit sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Arbeiten mit `sourceURL`  
:::image-end:::  

## Kontakt mit dem Microsoft Edge devtools-Team

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel ist ein JavaScript-Compiler"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Ein einfaches Beispiel für//# sourceURL eval Naming"  

[DartMain]: https://www.dartlang.org "Dart-Programmiersprache"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/Closure-Compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Quell Karten: Sprachen, Tools und andere Informationen | GitHub-wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Erste Schritte-Google/Traceur-Compiler | GitHub-wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Paul Bakaus][PaulBakaus] \ (Open Web Developer Advocate, Google: Tools, Performance, Animation und UX) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
