---
description: Verwenden Sie das Tool Sources, um JavaScript anzuzeigen, zu ändern und zu debuggen, das vom Server zurückgegeben wird, und um die Ressourcen zu überprüfen, aus der die aktuelle Webseite ist.  Um das Tool Sources als Entwicklungsumgebung zu verwenden, fügen Sie einem Arbeitsbereich Quelldateien hinzu.
title: Übersicht über das Tool „Quellen“
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6ba6a7615c2d9e2b70975af01edeeb3e10db8e59
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579743"
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
# <a name="sources-tool-overview"></a>Übersicht über das Tool „Quellen“  

Verwenden Sie **das Sources-Tool,** um Front-End-JavaScript-Code anzuzeigen, zu ändern und zu debuggen und die Ressourcen zu überprüfen, die die aktuelle Webseite enthalten.  Das **Tool Sources** verfügt über drei Bereiche:  

| Bereich | Aktionen |
|---|---|
| **Navigatorbereich** | Navigieren Sie zwischen den Ressourcen, die vom Server zurückgegeben werden, um die aktuelle Webseite zu erstellen.  Wählen Sie Dateien, Bilder und andere Ressourcen aus, und zeigen Sie ihre Pfade an.  Richten Sie optional einen lokalen Arbeitsbereich ein, um Änderungen direkt in Quelldateien zu speichern. |
| **Editorbereich** | Zeigen Sie JavaScript, HTML, CSS und andere Dateien an, die vom Server zurückgegeben werden.  Nehmen Sie experimentelle Bearbeitungen an JavaScript oder CSS vor.  Ihre Änderungen werden beibehalten, bis Sie die Seite aktualisieren oder nach der Seitenaktualisierung beibehalten werden, wenn Sie in einer lokalen Datei mit Arbeitsbereichen speichern. Wenn Sie Arbeitsbereiche oder Außerkraftsetzungen verwenden, können Sie auch HTML-Dateien bearbeiten. |
| **Debuggerbereich** | Verwenden Sie den JavaScript-Debugger, um Haltepunkte festzulegen, die Ausführung von JavaScript anzuhalten und den Code einschließlich der von Ihnen vorgenommenen Änderungen zu durchbrechen, während Sie die angegebenen JavaScript-Ausdrücke ansehen.  Beobachten und manuell ändern Sie die Werte von Variablen, die sich im Bereich der aktuellen Codezeile befinden. |

Die folgende Abbildung zeigt den **Navigatorbereich,** der mit einem roten Feld **** in der linken oberen Ecke von DevTools hervorgehoben ist, den Editorbereich oben rechts und den **Debuggerbereich** unten hervorgehoben.  Ganz links ist der Hauptteil des Browserfensters, in dem die gerenderte Webseite abgeblendet angezeigt wird, da der Debugger an einem Haltepunkt angehalten wird:

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Die Bereiche des Tools "Quellen" im schmalen Layout" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   Die Bereiche des Tools "Quellen" im schmalen Layout  
:::image-end:::  

Wenn DevTools breit ist, wird der **Debuggerbereich** rechts platziert und umfasst **Scope** und **Watch**:  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Vom Server zurückgegebenes JavaScript navigieren, anzeigen, bearbeiten und debuggen" lightbox="../media/sources-panes-wide-layout.msft.png":::
   Vom Server zurückgegebenes JavaScript navigieren, anzeigen, bearbeiten und debuggen  
:::image-end:::  

Um die Größe des Sources-Tools zu maximieren, entfernen Sie DevTools in ein separates Fenster, und verschieben Sie optional das DevTools-Fenster auf einen separaten Monitor.  Siehe [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].

Informationen zum Laden der oben gezeigten Debugdemowebseite finden Sie unter Der grundlegende Ansatz für die Verwendung [eines Debuggers](#the-basic-approach-to-using-a-debugger)weiter unten.

## <a name="using-the-navigator-pane-to-select-files"></a>Verwenden des Navigatorbereichs zum Auswählen von Dateien

Verwenden Sie **den Navigatorbereich** (links), um zwischen den Ressourcen zu navigieren, die vom Server zurückgegeben werden, um die aktuelle Webseite zu erstellen.  Wählen Sie Dateien, Bilder und andere Ressourcen aus, und zeigen Sie ihre Pfade an.  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Der Bereich Navigator" lightbox="../media/navigator-pane.msft.png":::
   Der **Bereich Navigator**
:::image-end:::  

Um auf alle ausgeblendeten Registerkarten des Navigatorbereichs zu zugreifen, wählen Sie ![ Weitere Registerkarten ](../media/more-tabs-icon.msft.png) ( Weitere Registerkarten )**aus.**

Die folgenden Unterabschnitte umfassen den Navigatorbereich:
*   [Verwenden der Registerkarte Seite zum Erkunden von Ressourcen, die die aktuelle Webseite erstellen](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)
*   [Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien](#using-the-overrides-tab-to-override-server-files-with-local-files)
*   [Verwenden der Registerkarte Inhaltsskripts für Microsoft Edge Erweiterungen](#using-the-content-scripts-tab-for-microsoft-edge-extensions)
*   [Verwenden der Registerkarte Codeausschnitte zum Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)
*   [Öffnen von Dateien mithilfe des Befehlsmenüs](#using-the-command-menu-to-open-files)

### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a>Verwenden der Registerkarte Seite zum Erkunden von Ressourcen, die die aktuelle Webseite erstellen

Verwenden Sie **die Registerkarte Seite** des **Navigatorbereichs,** um das dateisystem zu erkunden, das vom Server zurückgegeben wird, um die aktuelle Webseite zu erstellen.  Wählen Sie eine JavaScript-Datei zum Anzeigen, Bearbeiten und Debuggen aus.  Auf **der Registerkarte** Seite werden alle Ressourcen aufgeführt, die die Seite geladen hat.

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="Die Registerkarte Seite im Navigatorbereich des Tools Quellen" lightbox="../media/sources-page-tab.msft.png":::
   Die **Registerkarte Seite** im **Navigatorbereich** des **Tools Quellen**
:::image-end:::  

Wählen Sie auf **** der Registerkarte Seite eine Datei aus, um eine Datei im Editorbereich **anzuzeigen.**  Für ein Bild wird eine Vorschau des Bilds angezeigt.  

Zeigen Sie zum Anzeigen der URL oder des Pfads für eine Ressource auf die Ressource.

Zum Laden einer Datei in eine neue Registerkarte des Browsers oder zum Anzeigen anderer Aktionen klicken Sie mit der rechten Maustaste auf den Dateinamen.
   
#### <a name="icons-in-the-page-tab"></a>Symbole auf der Registerkarte Seite

Auf **der Registerkarte** Seite werden die folgenden Symbole verwendet:
*   Das **Fenstersymbol** stellt zusammen mit der Bezeichnung den `top` Hauptdokumentrahmen dar, bei dem es sich um einen [HTML-Frame handelt.][W3CHtml4Frames]  
*   Das **Cloudsymbol** stellt einen [Ursprung dar.][HtmlstandardOrigin]  
*   Das **Ordnersymbol** stellt ein Verzeichnis dar.
*   Das **Seitensymbol** stellt eine Ressource dar.  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a>Gruppieren von Dateien nach Ordnern oder als flache Liste

Auf **der Registerkarte** Seite werden Dateien oder Ressourcen nach Server und Verzeichnis oder als flache Liste angezeigt.

So ändern Sie die Gruppierung von Ressourcen:

1.  Wählen Sie neben den Registerkarten im Navigatorbereich (links) die **Schaltfläche ...** (**Weitere Optionen**) aus.  Es wird ein Menü angezeigt.
1.  Wählen Sie die Option **Gruppe nach Ordner aus, oder** deaktivieren Sie sie.  

### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a>Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs

Verwenden Sie **die Registerkarte Dateisystem** des **Navigatorbereichs,** um Einem Arbeitsbereich Dateien hinzuzufügen, sodass Änderungen, die Sie in DevTools vornehmen, in Ihrem lokalen Dateisystem gespeichert werden.

Eine Datei, die sich in einem Arbeitsbereich befindet, wird in devTools durch einen grünen Punkt neben dem Dateinamen gekennzeichnet. 

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Die Registerkarte Dateisystem für einen Arbeitsbereich" lightbox="../media/sources-filesystem-tab.msft.png":::
   Die **Registerkarte Dateisystem** für einen Arbeitsbereich
:::image-end:::  

Wenn Sie eine Datei im **** Tool Quellen bearbeiten, werden Ihre Änderungen standardmäßig verworfen, wenn Sie die Webseite aktualisieren.  Das **Tool Sources** arbeitet mit einer Kopie der Front-End-Ressourcen, die vom Webserver zurückgegeben werden.  Wenn Sie diese vom Server zurückgegebenen Front-End-Dateien ändern, werden die Änderungen nicht beibehalten, da Sie die Quelldateien nicht geändert haben.  Sie müssen ihre Bearbeitungen auch im tatsächlichen Quellcode anwenden und dann erneut auf dem Server bereitstellen.

Wenn Sie hingegen einen Arbeitsbereich verwenden, werden Änderungen, die Sie an Ihrem Front-End-Code vornehmen, beim Aktualisieren der Webseite beibehalten.  Wenn Sie mit einem Arbeitsbereich den vom Server zurückgegebenen Front-End-Code bearbeiten, wendet das Tool Quellen ihre Bearbeitungen auch auf den lokalen Quellcode an.  Damit andere Benutzer Ihre Änderungen sehen können, müssen Sie nur die geänderten Quelldateien erneut auf dem Server bereitstellen.

Arbeitsbereiche funktionieren gut, wenn der vom Server zurückgegebene JavaScript-Code mit dem lokalen JavaScript-Quellcode identisch ist.  Arbeitsbereiche funktionieren nicht so gut, wenn Ihr Workflow Transformationen im Quellcode umfasst, z. B. Verminung oder [TypeScript-Kompilierung.][TypescriptlangMain]  

Weitere Informationen finden Sie im Lernprogramm [Dateien mit Arbeitsbereichen bearbeiten.][DevtoolsGuideChromiumWorkspacesIndex]

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a>Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien

Verwenden Sie die Registerkarte **** Außerkraftsetzungen des **Navigatorbereichs,** um Seitenressourcen (z. B. Bilder) mit Dateien aus einem lokalen Ordner zu überschreiben.

Elemente auf dieser Registerkarte überschreiben, was der Server an den Browser sendet, auch nachdem der Server die Objekte gesendet hat.  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="Die Registerkarte Außerkraftsetzungen des Navigatorbereichs" lightbox="../media/overrides-tab.msft.png":::
   Die **Registerkarte Außerkraftsetzungen** des **Navigatorbereichs**
:::image-end:::  

Das **Overrides-Feature** ähnelt Arbeitsbereichen.  Verwenden Sie Außerkraftsetzungen, wenn Sie mit Änderungen an einer Webseite experimentieren möchten, und Sie müssen die Änderungen nach dem Aktualisieren der Webseite behalten. Es ist Ihnen jedoch nicht egal, ob Sie Ihre Änderungen dem Quellcode der Webseite zuordnen möchten.  

Eine Datei, die eine datei überschreibt, die vom Server zurückgegeben wird, wird durch einen lila Punkt neben dem Dateinamen in devTools angegeben.

#### <a name="see-also"></a>Weitere Informationen:

*   [Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools][DevtoolsJavascriptOverrides]

*   [Zuordnung von vorverarbeiteten Code zu Quellcode][DevToolsJavaScriptSourceMaps]

### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a>Verwenden der Registerkarte Inhaltsskripts für Microsoft Edge Erweiterungen

Verwenden Sie **die Registerkarte Inhaltsskripts** im **Navigatorbereich,** um alle Inhaltsskripts anzuzeigen, die von einer installierten Microsoft Edge geladen wurden. 

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="Die Registerkarte Inhaltsskripts im Navigatorbereich" lightbox="../media/content-scripts-tab.msft.png":::
   Die **Registerkarte Inhaltsskripts** im **Navigatorbereich**
:::image-end:::  

Wenn der Debugger codeschritte, den Sie nicht erkennen, möchten Sie diesen Code möglicherweise als Bibliothekscode markieren, um einen Schritt in diesen Code zu vermeiden.  Weitere [Informationen finden Sie unter Markieren von Inhaltsskripts als Bibliothekscode][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].

#### <a name="see-also"></a>Weitere Informationen:

*   [Inhaltsskripts][MDNContentScripts]
*   [Erstellen eines Erweiterungslernprogramms Teil 2][ExtensionsChromiumGetstartPart2ContentScripts]

### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a>Verwenden der Registerkarte Codeausschnitte zum Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Webseite

Verwenden Sie **die Registerkarte** Codeausschnitte des **Navigatorbereichs,** um JavaScript-Codeausschnitte zu erstellen und zu speichern, sodass Sie diese Codeausschnitte problemlos auf jeder Webseite ausführen können.

:::image type="complex" source="../media/snippet.msft.png" alt-text="Ein Codeausschnitt, der die jQuery-Bibliothek in eine Webseite einfüge" lightbox="../media/snippet.msft.png":::
   Ein Codeausschnitt, der die jQuery-Bibliothek in eine Webseite einfüge  
:::image-end:::  

Angenommen, Sie geben häufig den folgenden Code in die Konsole **ein,** um die jQuery-Bibliothek in eine Seite zu einfügen, damit Sie jQuery-Befehle über die Konsole **ausführen können:**  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Stattdessen können Sie diesen Code in einem Codeausschnitt **speichern** und dann bei Bedarf problemlos ausführen.  Wenn Sie `Ctrl` + `S` \(Windows/Linux\) oder `Command` + `S` \(macOS\) auswählen, **** speichert DevTools den Codeausschnitt in Ihrem Dateisystem.  

Es gibt mehrere Möglichkeiten zum Ausführen eines Codeausschnitts:
*   Wählen Sie **im Bereich Navigator** die Registerkarte **Codeausschnitte** aus, und wählen Sie dann die Codeausschnittdatei aus, um sie zu öffnen.  Wählen Sie dann unten im Editorbereich **Ausführen** \( ![ Die Schaltfläche Ausführen ](../media/run-snippet-icon.msft.png) \).  
*   Wenn DevTools den Fokus hat, wählen Sie `Ctrl` + `P` \(Windows/Linux\) oder `Command` + `P` \(macOS\) [][DevToolsCommandMenuIndex]aus, um das Befehlsmenü zu öffnen, und geben Sie dann `!` ein. 

Codeausschnitte ähneln Bookmarklets.

#### <a name="see-also"></a>Weitere Informationen:

*   [Ausführen von Codeausschnitten von JavaScript auf jeder Webseite mit Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptSnippets]

### <a name="using-the-command-menu-to-open-files"></a>Öffnen von Dateien mithilfe des Befehlsmenüs

Zum Öffnen einer Datei können Sie neben **** der Verwendung des **Navigatorbereichs** im Tool Quellen das Befehlsmenü von überall in DevTools verwenden.

*   Wählen Sie an beliebiger Stelle in DevTools `Ctrl` + `P` auf Windows/Linux oder `Command` + `P` auf macOS aus.  Das Befehlsmenü wird angezeigt und listet alle Ressourcen auf, die sich auf den Registerkarten des **Navigatorbereichs** des **Tools Quellen** befinden.  
*   Oder wählen Sie neben den Registerkarten **** des **Navigatorbereichs** im Tool Quellen die **Schaltfläche ...** (**Weitere**Optionen ) aus, und wählen Sie dann Datei **öffnen aus.**  

Geben Sie zum Anzeigen und Auswählen aus einer Liste aller .js `.js` ein.

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Öffnen einer Datei mithilfe des Befehlsmenüs" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   Öffnen einer Datei mithilfe des Befehlsmenüs
:::image-end:::

Wenn Sie `?` eingeben, werden im Befehlsmenü mehrere Befehle angezeigt, darunter **... Öffnen Sie die Datei**.  Wenn Sie das `Backspace` Befehlsmenü löschen möchten, wird eine Liste der Dateien angezeigt.

Weitere Informationen finden Sie unter [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].

## <a name="using-the-editor-pane-to-view-or-edit-files"></a>Verwenden des Editorbereichs zum Anzeigen oder Bearbeiten von Dateien

Verwenden Sie den **Editorbereich,** um die front-end-Dateien anzuzeigen, die vom Server zurückgegeben werden, um die aktuelle Webseite zu verfassen, einschließlich JavaScript, HTML, CSS und Bilddateien.  Wenn Sie die Front-End-Dateien im **Editorbereich bearbeiten,** aktualisiert DevTools die Webseite, um den geänderten Code ausführen zu können.  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="Der Editorbereich im Tool Quellen" lightbox="../media/editor-pane.msft.png":::
   Der **Editorbereich** im **Tool Quellen**  
:::image-end:::

Der **Editorbereich** bietet die folgende Unterstützungsebene für verschiedene Dateitypen:

| Dateityp | Unterstützte Aktionen |
|---|---|
| JavaScript | Anzeigen, Bearbeiten und Debuggen. |
| CSS | Anzeigen und Bearbeiten. |
| HTML | Anzeigen und Bearbeiten. |
| Images | „Ansicht“ aus. |

Standardmäßig werden Bearbeitungen verworfen, wenn Sie die Webseite aktualisieren.  Informationen zum Speichern der Änderungen an Ihrem Dateisystem finden Sie unter Verwenden der Registerkarte Dateisystem zum Definieren eines [lokalen Arbeitsbereichs](#using-the-filesystem-tab-to-define-a-local-workspace)oben.

Die folgenden Unterabschnitte umfassen den Editorbereich:
*   [Bearbeiten einer JavaScript-Datei](#editing-a-javascript-file)
*   [Neuformatieren einer minifizierten JavaScript-Datei mit Hübschdruck](#reformatting-a-minified-javascript-file-with-pretty-print)
*   [Zuordnen von minifizierten Code zu Ihrem Quellcode zum Anzeigen lesbaren Codes](#mapping-minified-code-to-your-source-code-to-show-readable-code)
*   [Transformationen vom Quellcode in kompilierten Front-End-Code](#transformations-from-source-code-to-compiled-front-end-code)
*   [Bearbeiten einer CSS-Datei](#editing-a-css-file)
*   [Bearbeiten einer HTML-Datei](#editing-an-html-file)
*   [Zu einer Zeilennummer oder Funktion](#going-to-a-line-number-or-function)
*   [Anzeigen von Quelldateien bei Verwendung eines anderen Tools](#displaying-source-files-when-using-a-different-tool)

### <a name="editing-a-javascript-file"></a>Bearbeiten einer JavaScript-Datei

Um eine JavaScript-Datei in DevTools zu bearbeiten, verwenden Sie den **Editorbereich** im **Tool Quellen.**

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Bearbeiten von JavaScript im Editorbereich" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   Bearbeiten von JavaScript im **Editorbereich**  
:::image-end:::

Um eine Datei in den Editorbereich zu laden, verwenden Sie die Registerkarte **Seite** im **Navigatorbereich** (links).  Oder verwenden Sie das **Befehlsmenü**wie folgt: Wählen Sie oben rechts von DevTools die Option **DevTools** anpassen und steuern \( \) aus, und wählen Sie dann `...` Datei öffnen **aus.**

#### <a name="save-and-undo"></a>Speichern und Rückgängig machen

Damit JavaScript-Änderungen wirksam werden, wählen `Ctrl` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\).  

Wenn Sie eine Datei ändern, wird neben dem Dateinamen ein Sternchen angezeigt.
*   Um Änderungen zu speichern, wählen Sie `Ctrl` + `S` unter Windows/Linux oder `Command` + `S` unter macOS aus.
*   Um eine Änderung rückgängig zu machen, wählen Sie `Ctrl` + `Z` unter Windows/Linux oder `Command` + `Z` unter macOS aus.

Standardmäßig werden Ihre Bearbeitungen verworfen, wenn Sie die Webseite aktualisieren.  Weitere Informationen zum Speichern der Änderungen im lokalen Dateisystem finden Sie unter [Bearbeiten von Dateien mit Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex].

#### <a name="find-and-replace"></a>Suchen und Ersetzen

Um Text in der aktuellen **** Datei zu finden, wählen Sie den Editorbereich aus, um ihm den Fokus zu geben, und wählen Sie dann unter `Ctrl` + `F` Windows/Linux oder `Command` + `F` unter macOS aus.  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Suchen und Ersetzen im Editorbereich des Tools Quellen" lightbox="../media/find-replace.msft.png":::
   **Suchen** und **Ersetzen**im **Editorbereich** des **Tools Quellen**
:::image-end:::

Zum Suchen und Ersetzen von Text wählen Sie die Schaltfläche **Ersetzen** (**A-\>B**) links vom Textfeld **Suchen** aus. Die **Schaltfläche Ersetzen** (**A-\>B**) wird beim Anzeigen einer bearbeitbaren Datei angezeigt.

#### <a name="showing-the-changes-you-made"></a>Anzeigen der vorgenommenen Änderungen

Klicken Sie zum Überprüfen der änderungen, die **** Sie an einer Datei vorgenommen haben, mit der rechten Maustaste in den Editorbereich, und wählen Sie **dann Lokale Änderungen aus.**

Die **Drawer** wird am unteren Rand von DevTools geöffnet und zeigt Ihre Änderungen auf der Registerkarte **Änderungen** an.

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Anzeigen lokaler Änderungen auf der Registerkarte Änderungen der Drawer" lightbox="../media/local-modifications.msft.png":::
   Anzeigen **lokaler Änderungen**auf der Registerkarte **Änderungen** der **Drawer**
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a>Änderungen innerhalb einer Funktion werden wirksam

DevTools wird kein Skript erneut ausgeführt, daher sind die einzigen JavaScript-Änderungen, die wirksam werden, Änderungen, die Sie innerhalb von Funktionen vornehmen.  In der folgenden Abbildung haben wir beispielsweise den folgenden Code zu dem vom Server zurückgegebenen JavaScript hinzugefügt:  
*   Wir haben die Anweisung `console.log('A')` außerhalb einer beliebigen Funktion hinzugefügt.  
*   Wir haben die Anweisung `console.log('B')` in einer Funktion `onClick` hinzugefügt.  
Anschließend haben wir die Änderungen gespeichert, Zahlen in das Formular eingegeben und dann die Formularschaltfläche ausgewählt, um das Formular zu senden.  

Nach dem Absenden des Formulars wird , das sich auf globaler Ebene befindet, nicht ausgeführt, aber innerhalb einer Funktion wird ausgeführt, und es wird an `console.log('A')` `console.log('B')` die Konsole `onClick` `B` ausgegeben:

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript auf globaler Ebene wird nicht erneut ausgeführt" lightbox="../media/edit-js.msft.png":::
   JavaScript auf globaler Ebene wird nicht erneut ausgeführt  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a>Neuformatieren einer minifizierten JavaScript-Datei mit Hübschdruck

Um eine Datei mit ziemlicher Grafik neu zu formatieren, um sie lesbar zu machen, wählen Sie am unteren Rand des Editorbereichs die Schaltfläche Ziemlich drucken \( Format **** ![ ](../media/format-icon.msft.png) \) aus, die als geschweifte Klammern angezeigt wird.  Wenn oben im **Editorbereich** eine Schaltfläche "Ziemlich drucken" angezeigt wird, können Sie diese Schaltfläche auswählen.

:::image type="complex" source="../media/minified.msft.png" alt-text="Die Schaltfläche "Hübsch drucken"" lightbox="../media/minified.msft.png":::
   Die **Schaltfläche "Hübsch drucken"**  
:::image-end:::  

Die neu formatierte Datei wird auf einer neuen Registerkarte angezeigt, die `:formatted` an den Dateinamen angefügt ist.  Der neu formatierte Code ist schreibgeschützt.  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Eine ziemlich gedruckte (neu formatierte) JavaScript-Datei" lightbox="../media/pretty-printed.msft.png":::
   Eine ziemlich gedruckte (neu formatierte) JavaScript-Datei  
:::image-end:::  

So führen Sie einen Bildlauf der neu formatierten Datei zu dem Code durch, den Sie in der minifizierten Datei auswählen: 
1.   Wenn die Registerkarte neu formatierte Datei geöffnet ist, schließen Sie sie.  
1.   Wählen Sie code in der verminten Datei im Editorbereich aus.
1.   Wählen Sie die **Schaltfläche Hübsch drucken** aus.
Der formatierte Code wird auf einer neuen Registerkarte mit einem Bildlauf zu dem ausgewählten Code angezeigt.

Weitere Informationen finden Sie unter [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a>Zuordnen von minifizierten Code zu Ihrem Quellcode zum Anzeigen lesbaren Codes

Quellzuordnungen von Präprozessoren führen dazu, dass DevTools ihre ursprünglichen JavaScript-Quelldateien zusätzlich zu ihren minifizierten, transformierten JavaScript-Dateien, die vom Server zurückgegeben werden, laden.  Anschließend zeigen Sie die ursprünglichen Quelldateien an, während Sie Haltepunkte festlegen und Code schrittweise durchbrechen.  In der zwischenzeit Microsoft Edge tatsächlich ihren minifizierten Code ausgeführt.  

Wenn Sie im **Editorbereich** mit der rechten Maustaste auf eine JavaScript-Datei klicken und dann Quellzuordnung hinzufügen **auswählen,** wird ein Popupfeld mit einem Textfeld **quellzuordnungs-URL** und einer Schaltfläche Hinzufügen **angezeigt.**

Der Source-Mapping-Ansatz sorgt dafür, dass Ihr Front-End-Code auch nach dem Kombinieren, Verfälschen oder Kompilieren des Codes für den Menschen lesbar und debuggbar bleibt.
Weitere Informationen finden Sie unter [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a>Transformationen vom Quellcode in kompilierten Front-End-Code

Wenn Sie ein Framework verwenden, das Ihre JavaScript-Dateien transformiert, z. B. React, kann sich Ihr lokales JavaScript von dem Front-End-JavaScript unterscheiden, das vom Server zurückgegeben wird.  Arbeitsbereiche werden in diesem Szenario nicht unterstützt, aber die Quellcodezuordnung wird in diesem Szenario unterstützt.  

In einer Entwicklungsumgebung kann Ihr Server Ihre Quellzuordnungen und Ihre Originaldateien oder Dateien für `.ts` `.jsx` React.  Das **Tool Sources** zeigt diese Dateien an, ermöglicht es Ihnen jedoch nicht, diese Dateien zu bearbeiten.  Wenn Sie Haltepunkte festlegen und den Debugger verwenden, zeigt DevTools Ihre Ursprünglichen oder Dateien an, aber tatsächlich wird die minifizierte Version Ihrer `.ts` `.jsx` JavaScript-Dateien durchschritten.

In diesem Szenario ist das **Sources-Tool** nützlich, um das transformierte Front-End-JavaScript, das vom Server zurückgegeben wird, zu überprüfen und zu durchsichten.  Verwenden Sie den Debugger, um Watch-Ausdrücke zu definieren, und verwenden Sie die Konsole, um JavaScript-Ausdrücke ein eingeben, um Daten zu bearbeiten, die in den Bereich sind.

### <a name="editing-a-css-file"></a>Bearbeiten einer CSS-Datei

Es gibt zwei Möglichkeiten zum Bearbeiten von CSS in DevTools:
*   Im **Tool Elemente** arbeiten Sie mit einer CSS-Einstellung gleichzeitig über Benutzeroberflächensteuerelemente.  Dieser Ansatz wird in den meisten Fällen empfohlen.  Weitere Informationen finden Sie unter [Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen.][DevToolsInspectStylesEditFonts]
*   Im **Tool Quellen** verwenden Sie einen Text-Editor.

Das Tool Sources unterstützt das direkte Bearbeiten einer CSS-Datei.  Wenn Sie z. B. die CSS-Datei aus dem Lernprogramm Dateien mit [Arbeitsbereichen][DevtoolsGuideChromiumWorkspacesIndex] bearbeiten bearbeiten, um der folgenden Formatvorlagenregel zu entsprechen, wird das Element in der oberen linken Ecke der gerenderten Webseite `H1` in Grün geändert:

```css
h1 {
  color: green;
}  
```

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Bearbeiten von CSS im Editorbereich, um die Textfarbe der H1-Überschrift in Grün zu ändern" lightbox="../media/edit-css.msft.png":::
   Bearbeiten von CSS im **Editorbereich,** um die Textfarbe der Überschrift in `H1` Grün zu ändern  
:::image-end:::  

#A0 werden sofort wirksam. Sie müssen die Änderungen nicht manuell speichern.

#### <a name="see-also"></a>Weitere Informationen:

*   [Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen][DevToolsInspectStylesEditFonts]

*   [DevTools für Anfänger: Erste Schritte mit CSS][DevToolsBeginnersCss] – Lernprogramm

### <a name="editing-an-html-file"></a>Bearbeiten einer HTML-Datei

Es gibt zwei Möglichkeiten zum Bearbeiten von HTML in DevTools:  
*   Im **Elementtool** arbeiten Sie mit einem HTML-Element gleichzeitig über Benutzeroberflächensteuerelemente.  
*   Im **Tool Quellen** verwenden Sie einen Text-Editor.  

:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="Der HTML-Editor des Sources-Tools" lightbox="../media/sources-html-editor.msft.png":::
   Der HTML-Editor des **Sources-Tools**
:::image-end:::  

Im Gegensatz zu einer JavaScript- oder CSS-Datei kann eine vom Webserver zurückgegebene HTML-Datei nicht direkt im Tool Quellen bearbeitet werden.  Zum Bearbeiten einer HTML-Datei mit dem Editor des Tools Sources muss sich die HTML-Datei in einem Arbeitsbereich oder auf der Registerkarte **Außerkraftsetzungen** befinden.  Lesen Sie die folgenden Unterabschnitte des aktuellen Artikels:
*   [Verwenden der Registerkarte Dateisystem zum Definieren eines lokalen Arbeitsbereichs](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [Verwenden der Registerkarte Außerkraftsetzungen zum Außerkraft setzen von Serverdateien mit lokalen Dateien](#using-the-overrides-tab-to-override-server-files-with-local-files)
    
Um Änderungen zu speichern, wählen Sie `Ctrl` + `S` unter Windows/Linux oder `Command` + `S` unter macOS aus.  Eine bearbeitete Datei wird durch ein Sternchen markiert.  

Um Text zu finden, wählen Sie `Ctrl` + `F` unter Windows/Linux oder `Command` + `F` unter macOS aus.

Um eine Bearbeitung rückgängig zu machen, wählen Sie `Ctrl` + `Z` unter Windows/Linux oder `Command` + `Z` unter macOS aus.

Um andere Befehle beim Bearbeiten einer HTML-Datei anzuzeigen, klicken Sie im Bereich Editor mit der rechten Maustaste auf die HTML-Datei.

Sie können HTML auch mithilfe eines HTML-Editors anstelle von DevTools bearbeiten.  Der Artikel [DevTools für Anfänger: Erste][DevToolsBeginnersHtml] Schritte mit HTML und das DOM verwendet eine Website, die die HTML-Bearbeitung auf der Webseite ermöglicht.

### <a name="going-to-a-line-number-or-function"></a>Zu einer Zeilennummer oder Funktion

Um zu einer Zeilennummer oder einem Symbol (z. B. einem Funktionsnamen) in der Datei zu wechseln, die im Editorbereich geöffnet ist, können Sie das Befehlsmenü verwenden, anstatt einen Bildlauf durch die Datei auszuführen.

1.   Wählen Sie **im Bereich Navigator** die Ellipsen (...) aus. (**Weitere Optionen**), und wählen Sie dann Datei öffnen **aus.**  Das Befehlsmenü wird angezeigt.  
1.   Geben Sie eines der folgenden Zeichen ein:  

| Zeichen | Befehlsname | Zweck |
|---|---|---|
| \: | **Zur Zeile wechseln** | Wechseln Sie zu einer Zeilennummer. |
| \@ | **Wechseln zum Symbol** | Wechseln Sie zu einer Funktion.  Wenn Sie eingeben, werden im Befehlsmenü die Funktionen aufgelistet, die sich in der Im Editorbereich geöffneten `@` JavaScript-Datei befinden. |
   
Weitere Informationen finden Sie unter [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].

### <a name="displaying-source-files-when-using-a-different-tool"></a>Anzeigen von Quelldateien bei Verwendung eines anderen Tools

Der Hauptort zum Anzeigen von Quelldateien in devTools befindet sich im **Sources-Tool.**  Manchmal müssen Sie jedoch auf andere Tools wie **Elemente** oder **Konsole**zugreifen, während Sie Ihre Quelldateien anzeigen oder bearbeiten.  Verwenden Sie **das Tool Schnellquellen** in der [Schublade][DevtoolsCustomizeIndexDrawer].

1.  Wählen Sie ein anderes Tool als das **Sources-Tool** aus, z. B. das **Elementtool.**  
1.  Wählen `Ctrl` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\).  Das Befehlsmenü wird geöffnet.  
1.  Geben `Quick Source` Sie ein, und wählen Sie **Dann Schnellquelle anzeigen aus.**  Am unteren Rand des DevTools-Fensters wird **** die Schublade angezeigt, und der Schnellquellenbereich ist ausgewählt.  Der **Schnellquellenbereich** enthält die letzte Datei, die Sie im **Tool Quellen** in einer kompakten Version des DevTools-Code-Editors bearbeitet haben.  
1.  Wählen `Ctrl` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) **** aus, um das Dialogfeld Datei öffnen zu öffnen.  

## <a name="using-the-debugger-pane-to-debug-javascript-code"></a>Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code

Verwenden Sie den JavaScript-Debugger, um den vom Server zurückgegebenen JavaScript-Code zu durchschritten. Der Debugger enthält den **Debuggerbereich** sowie Haltepunkte, die Sie für Codezeilen im **Editorbereich festlegen.**

Mit dem Debugger durchschritten Sie den Code, während Sie alle angegebenen JavaScript-Ausdrücke ansehen.  Beobachten und manuell ändern Sie Variablenwerte, und zeigen Sie automatisch an, welche Variablen sich im Bereich der aktuellen Anweisung befinden.

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="Der Debuggerbereich des Tools Quellen  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   Der **Debuggerbereich** des **Tools Quellen**  
:::image-end:::  

Der Debugger unterstützt standardmäßige Debugaktionen, z. B.:  
*   Festlegen von Haltepunkten, um Code anzuhalten.
*   Schrittweises Durchfingen von Code.
*   Anzeigen und Bearbeiten von Eigenschaften und Variablen.
*   Beobachten der Werte von JavaScript-Ausdrücken.
*   Anzeigen der Aufrufliste (die Sequenz der bisher verwendeten Funktionsaufrufe).

Der Debugger in DevTools ist so konzipiert, dass er wie der [Debugger in][CodeVisualStudioComDocsEditorDebugging] Visual Studio Code und der [Debugger in Visual Studio.][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]

Die folgenden Unterabschnitte umfassen das Debuggen:
*   [Der grundlegende Ansatz für die Verwendung eines Debuggers](#the-basic-approach-to-using-a-debugger)
*   [Vorteile von Watch und Scope des Debuggers gegenüber console.log](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)
*   [Debuggen von Visual Studio Code direkt](#debug-from-visual-studio-code-directly)
*   [Artikel zum Debuggen](#articles-about-debugging)

### <a name="the-basic-approach-to-using-a-debugger"></a>Der grundlegende Ansatz für die Verwendung eines Debuggers

Zur Problembehandlung von JavaScript-Code können Sie `console.log()` Anweisungen im **Editorbereich** einfügen.  Ein weiterer, leistungsstärkerer Ansatz ist die Verwendung des Debuggers Microsoft Edge DevTools.  Die Verwendung eines Debuggers kann einfacher als sein, sobald Sie mit dem `console.log()` Debuggeransatz vertraut sind.

Um einen Debugger auf einer Webseite zu verwenden, legen Sie in der Regel einen Haltepunkt ein und senden dann ein Formular von der Webseite wie folgt:

1.  Öffnen Sie die Webseite auf einer neuen Registerkarte des Browsers.  Öffnen Sie beispielsweise diese Formularwebseite auf einer neuen Registerkarte: Demo: Erste Schritte Debuggen von JavaScript mit Microsoft Edge [(Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].

1.  Wählen Sie diese Option aus, um das `F12` **Fenster DevTools** zu öffnen, und wählen Sie dann die Registerkarte **Quellen** aus.

1.  Wählen Sie **im Bereich Navigator** (links) die Registerkarte **Seite** aus, und wählen Sie dann die JavaScript-Datei aus, z. B. `get-started.js` .

1.  Wählen Sie **im Bereich Editor** eine Zeilennummer in der Nähe einer verdächtigen Codezeile aus, um einen Haltepunkt für diese Zeile zu setzen.  In der folgenden Abbildung wird ein Haltepunkt für die Zeile `var sum = addend1 + addend2;` festgelegt.

1.  Geben Sie auf der Webseite Werte ein, und übermitteln Sie das Formular.  Geben Sie beispielsweise Zahlen wie und ein, und wählen Sie dann die Schaltfläche Nummer 1 hinzufügen `5` und `1` Nummer **2 aus.**  

    Der Debugger führt den JavaScript-Code aus und hält dann am Haltepunkt an.  Der Debugger befindet sich nun im Angehalten-Modus, sodass Sie die Werte der Eigenschaften überprüfen können, die sich im Bereich befinden, und den Code schrittweise durchschritten.

    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Eingeben des angehaltenen Modus des Debuggers" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        Eingeben des angehaltenen Modus des Debuggers  
    :::image-end:::  

    In der obigen Abbildung haben wir die Watch-Ausdrücke und hinzugefügt und zwei Zeilen über `sum` `typeof sum` den Haltepunkt gestuft.

1.  Untersuchen Sie die Werte im **Bereich Bereich,** in dem alle Variablen oder Eigenschaften angezeigt werden, die sich im Bereich des aktuellen Haltepunkts befinden, und deren Werte.  Oder fügen Sie Ausdrücke im Bereich **"Watch"** hinzu.  Diese Ausdrücke sind dieselben Ausdrücke, die Sie in eine Anweisung schreiben `console.log` würden, um Ihren Code zu debuggen.  Verwenden Sie die Konsole, um JavaScript-Befehle zum Bearbeiten von Daten im aktuellen Kontext **auszuführen.**  Wählen Sie aus, um die Konsole zu `Esc` öffnen.  

1.  Gehen Sie durch den Code, indem Sie die Steuerelemente am oberen Rand des **Debuggerbereichs** verwenden, z. B. **Step** ( `F9` ).

#### <a name="see-also"></a>Weitere Informationen:

*   [Erste Schritte mit dem Debuggen][DevtoolsGuideChromiumJavascriptIndex] von JavaScript – ein Lernprogramm mit einer vorhandenen, einfachen Webseite, die einige Formularsteuerelemente enthält.

### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a>Vorteile des Debuggers Watch and Scope over console\.log

Diese drei Ansätze sind äquivalent:

*   Vorübergehendes Hinzufügen der Anweisungen `console.log(sum)` und `console.log(typeof sum)` im Code, wobei sich der Bereich `sum` befindet.
*   Ausstellen der Anweisungen und im Konsolenbereich der DevTools, wenn der Debugger angehalten wird, `sum` wo sich der Bereich `console.log(typeof sum)` **** `sum` befindet.
*   Festlegen **** der `sum` Watch-Ausdrücke und `typeof sum` im **Debuggerbereich.**

Wenn sich die Variable im Bereich befindet und ihr Wert automatisch im Bereich bereich des `sum` `sum` **Debuggerbereichs** angezeigt wird, **** werden sie auch im Editorbereich überlagert, wo berechnet `sum` wird.  Daher müssten Sie wahrscheinlich keinen Watch-Ausdruck für `sum` definieren.

Der Debugger bietet eine reichhaltigere, flexiblere Anzeige und Umgebung als eine `console.log` Anweisung.  Im Debugger können Sie z. B. die Werte aller derzeit definierten Eigenschaften und Variablen anzeigen und ändern, wenn Sie den Code durchschritten haben.  Sie können auch JavaScript-Anweisungen in der **Konsole ausschreiben,** z. B. um Werte in einem Array zu ändern, das sich im Bereich des Bereichs ist.  (Wählen Sie **Esc**aus, um die Konsole anzeigen zu können.)

Haltepunkte und Watch-Ausdrücke werden beim Aktualisieren der Webseite beibehalten.

### <a name="debug-from-visual-studio-code-directly"></a>Debuggen von Visual Studio Code direkt

Verwenden Sie die **Microsoft Edge Tools for VS Code** extension for Visual Studio Code, um den vollständigeren Debugger von Visual Studio Code anstelle des DevTools-Debuggers zu Visual Studio Code.

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="Die Microsoft Edge Tools for VS Code extension for Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   Die **Microsoft Edge Tools for VS Code** extension for Visual Studio Code  
:::image-end:::  

Diese Erweiterung bietet Zugriff auf die **Elemente** und **Netzwerktools** von Microsoft Edge DevTools innerhalb Microsoft Visual Studio Code.  

Weitere Informationen finden Sie [unter Visual Studio Code übersicht][DevToolsVSCodeIndex] und GitHub Readme-Seite, Microsoft Edge Developer Tools for [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].

### <a name="articles-about-debugging"></a>Artikel zum Debuggen

In den folgenden Artikeln werden der **Debuggerbereich** und die Haltepunkte aufgeführt:

*   [Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] – Ein Lernprogramm (mit Bildschirmaufzeichnungen) mit einem vorhandenen, einfachen Projekt.

*   [Verwenden der Debuggerfeatures][DevToolsJavaScriptReference] : Verwenden des Debuggers zum Festlegen von Haltepunkten, Schrittweises Durchbrechen von Code, Anzeigen und Ändern von Variablenwerten, Beobachten von JavaScript-Ausdrücken und Anzeigen der Aufrufliste.

*   [Anhalten des Codes mit Haltepunkten][DevToolsJavaScriptBreakpoints] – Festlegen grundlegender und spezieller Haltepunkte im Debugger.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools für Anfänger: Erste Schritte mit CSS | Microsoft Docs"
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools für Anfänger: Erste Schritte mit HTML und der DOM-| Microsoft Docs"
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer – Anpassen Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links) | Microsoft Docs"
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Führen Sie Codeausschnitte von JavaScript auf jeder Webseite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Bearbeiten von Dateien mit Arbeitsbereichen | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Formatvorlagenbereich | Microsoft Docs"
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Anhalten des Codes mit Haltepunkten | Microsoft Docs"
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Markieren von Inhaltsskripts als Bibliothekscode | Microsoft Docs"
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Verwenden der Debuggerfeatures | Microsoft Docs"
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Neuvergrößern einer minifizierten JavaScript-Datei mit Hübschdruck – Verwenden Sie die Debuggerfeatures | Microsoft Docs"
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Map preprocessed code to source code | Microsoft Docs"
[DevToolsVSCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code Übersicht | Microsoft Docs"
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Erstellen eines Erweiterungs-Lernprogramms Teil 2 | Microsoft Docs"
<!-- external: -->
[CodeVisualStudioComDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Debuggen – Visual Studio Code | Microsoft Docs"
[DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Navigieren Sie durch Code mit Visual Studio Debugger| Microsoft Docs"
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Entwicklertools für Visual Studio Code | GitHub"
[DevtoolsGlitchMeDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demo: Erste Schritte Debuggen von JavaScript mit Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Ursprung | HTML-Standard"  
[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Inhaltsskripts | MDN"  
[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/sources) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
