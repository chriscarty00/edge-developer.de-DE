---
title: API-Referenz für Konsolen Dienstprogramme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601796"
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





# API-Referenz für Konsolen Dienstprogramme   



Die API für Konsolen Dienstprogramme enthält eine Sammlung von praktischen Befehlen zum Ausführen allgemeiner Aufgaben: auswählen und Überprüfen von DOM-Elementen, Anzeigen von Daten im lesbaren Format, beenden und Starten des Profilers sowie überwachen von DOM-Ereignissen.  

> [!WARNING]
> Die folgenden Befehle funktionieren nur in der Microsoft Edge devtools-Konsole.  Die Befehle funktionieren nicht, wenn Sie aus Ihren Skripts ausgeführt werden.  

Suchen Sie `console.log()` nach `console.error()` und die restlichen `console.*` Methoden?  Siehe [API-Referenz][DevToolsConsoleApi]für die Konsole.  

## Kürzlich ausgewerteter Ausdruck  

```console
$_
```  

Gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.  

In [Abbildung 1](#figure-1)wird ein einfacher Ausdruck \ ( `2 + 2` \) ausgewertet.  `$_`Anschließend wird die Eigenschaft ausgewertet, die den gleichen Wert enthält.  

> ##### Abbildung1  
> `$_` ist der zuletzt ausgewertete Ausdruck  
> ![$ _ ist der zuletzt ausgewertete Ausdruck][ImageRecentExpression]  

In [Abbildung 2](#figure-2)enthält der ausgewertete Ausdruck zunächst ein Array von Namen.  Auswerten, `$_.length` um die Länge des Arrays zu ermitteln, wird der Wert, der in Änderungen gespeichert wird, `$_` zum neuesten ausgewerteten Ausdruck `4` .  

> ##### Abbildung2  
> `$_` ändert sich, wenn neue Befehle ausgewertet werden  
> ![$ _ ändert sich, wenn neue Befehle ausgewertet werden][ImageChangedRecentExpression]  

## Zuletzt ausgewähltes Element oder JavaScript-Objekt  

```console
$0
```  

Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.  `$1` Gibt die zweite zuletzt ausgewählte Person zurück usw.  Die `$0` `$1` Befehle,,, und werden `$2` `$3` `$4` als historischer Bezug auf die letzten fünf im Bereich **Elemente** geprüften DOM-Elemente oder die letzten fünf im **Speicher** Bereich ausgewählten JavaScript-Heapobjekte ausgeführt.  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

In [Abbildung 3](#figure-3) `img` wird im Panel **Elemente** ein Element ausgewählt.  Wurde im **Konsolen** Einzug `$0` ausgewertet und zeigt dasselbe Element an.  

> ##### Abbildung 3  
> Der `$0`  
> ![Das $0][ImageElement0]  

In [Abbildung 4](#figure-4)zeigt das Bild ein anderes Element, das auf der gleichen Seite markiert ist.  Das `$0` jetzt bezieht sich auf das neu ausgewählte Element, `$1` gibt aber die zuvor ausgewählte zurück.  

> ##### Abbildung4  
> Der `$1`  
> ![Das $1][ImageElement1]  

## Abfrageauswahl  

```console
$(selector, [startNode])
```  

Gibt den Verweis auf das erste DOM-Element mit der angegebenen CSS-Auswahl zurück.  Diese Methode ist ein Alias für die [Document. querySelector ()][MDNDocumentQuerySelector] -Methode.  

In [Abbildung 5](#figure-5)wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.  

> ##### Abbildung5  
> Der `$('img')`  
> ![$ (' Img ')][ImageElementImg]  

Klicken Sie mit der rechten Maustaste auf das zurückgegebene Ergebnis, und wählen Sie **im Element Fenster** anzeigen aus, um es im Dom zu finden, oder **Scrollen Sie zur Ansicht** , um es auf der Seite anzuzeigen.  

In [Abbildung 6](#figure-6)wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.  

> ##### Abbildung6  
> Der `$('img').src`  
> ![$ (' Img '). src][ImageElementImgSource]  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  Der Standardwert für diesen Parameter ist `document` .  

In [Abbildung 7](#figure-7) `img` befindet sich das erste Element nach dem `title--image` und zeigt die `src` ordnungsgemäße Rückgabe zurück.  

> ##### Abbildung7  
> Der $ (' img ', Document. querySelector (' Titel--Bild ')). src  
> ![Der $ (' img ', Document. querySelector (' Titel--Bild ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet wird `$` , wird diese Funktionalität überschrieben und `$` entspricht der Implementierung aus dieser Bibliothek.  

## Abfrageauswahl alle  

```console
$$(selector, [startNode])
```  

Gibt ein Array von Elementen zurück, die der angegebenen CSS-Auswahl entsprechen.  Diese Methode entspricht dem Aufrufen der [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] -Methode.  

In [Abbildung 8](#figure-8)verwenden Sie, `$$()` um ein Array aller `<img>` Elemente im aktuellen Dokument zu erstellen und den Wert der `src` Eigenschaft für jedes Element anzuzeigen.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### Abbildung8  
> Verwenden `$$()` , um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen  
> ![Verwenden von $ $ (), um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen][ImageArrayElementImgSource]  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  Der Standardwert für diesen Parameter ist `document` .  

In [Abbildung 9](#figure-9)wird eine geänderte Version von [Abbildung 8](#figure-8) verwendet `$$()` , um ein Array aller Elemente zu erstellen `<img>` , die im aktuellen Dokument nach dem ausgewählten Knoten angezeigt werden.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### Abbildung 9  
> Verwenden `$$()` zum Auswählen aller Bilder, die nach dem angegebenen `<div>` Element im Dokument angezeigt werden, und Anzeigen der Quellen  
> ![Verwenden von $ $ (), um alle Bilder auszuwählen, die nach dem angegebenen <div->-Element im Dokument angezeigt werden, und Anzeigen der Quellen][ImageArrayElementImgNodeSource]  

> [!NOTE]
> Drücken Sie `Shift` + `Enter` in der Konsole, um eine neue Zeile zu starten, ohne das Skript auszuführen.  

## XPath  

```console
$x(path, [startNode])
```  

Gibt ein Array von DOM-Elementen zurück, die dem angegebenen XPath-Ausdruck entsprechen.  

In [Abbildung 10](#figure-10) `<p>` werden alle Elemente auf der Seite zurückgegeben.  

```console
$x("//p")
```  

> ##### Abbildung 10  
> Verwenden einer XPath-Auswahl  
> ![Verwenden einer XPath-Auswahl][ImageArrayXpath]  

In [Abbildung 11](#figure-11) `<p>` werden alle Elemente zurückgegeben, die `<a>` Elemente enthalten.  

```console
$x("//p[a]")
```  

> ##### Abbildung 11  
> Verwenden einer komplexeren XPath-Auswahl  
> ![Verwenden einer komplexeren XPath-Auswahl][ImageArrayXpathChild]  

Ähnlich wie bei den anderen Auswahlbefehlen `$x(path)` verfügt ein optionaler zweiter Parameter, der `startNode` ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  

> ##### Abbildung 12  
> Verwenden einer XPath-Auswahl mit `startNode`  
> ![Verwenden einer XPath-Auswahl mit startNode][ImageArrayXpathNode]  

## Deaktivieren  

```console
clear()
```  

Löscht die Konsole des Verlaufs.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

Die `copy(object)` Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.  

```console
copy($0)
```  

## debuggen  

```console
debug(method)
```  

>[!NOTE]
> Das [Chrom Problem #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.  Wenn dieses Problem auftritt, versuchen Sie stattdessen, [Haltepunkte zu verwenden][DevtoolsJavascriptBreakpoints] .  

Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im Bereich " **Quellen** " unterbricht, sodass Sie den Code schrittweise durchlaufen und Debuggen können.  

```console
debug("debug");
```  

> ##### Abbildung 13  
> Durchbrechen innerhalb einer Methode mit `debug()`  
> ![Durchbrechen innerhalb einer Methode mit Debug ()][ImageDebugMethod]  

Verwenden Sie diese Option, `undebug(method)` um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.  

Weitere Informationen zu Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Zeigt eine Objektstil Auflistung aller Eigenschaften für das angegebene Objekt an.  Diese Methode ist ein Alias für die [Console. dir ()][MDNConsoleDir] -Methode.  

Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den `<head>` und- `</head>` Tags anzuzeigen.  In [Abbildung 14](#figure-14)wird nach `console.dir()` der Verwendung in der Konsole ein Objektformat Eintrag angezeigt.  

```console
document.head;
dir(document.head);
```  

> ##### Abbildung 14  
> Protokollierung `document.head` mit `dir()` Methode  
> ![Protokollierungs Dokument. Head mit dir ()-Methode][ImageLogObject]  

Weitere Informationen finden Sie im [`console.dir()`][DevToolsConsoleApiConsoleDirObject] Eintrag in der Konsolen-API.  

## DirXML  

```console
dirxml(object)
```  

Druckt eine XML-Darstellung des angegebenen Objekts, wie auf der Registerkarte **Elemente** zu sehen ist.  Diese Methode entspricht der [Console. DirXML ()][MDNConsoleDirxml] -Methode.  

## prüfen  

```console
inspect(object/method)
```  

Das angegebene Element oder Objekt wird in der entsprechenden Leiste geöffnet und markiert: entweder der **Element Panel für** DOM-Elemente oder der **Speicher** Panel für JavaScript-Heapobjekte.  

In [Abbildung 15](#figure-15)wird das `document.body` im **Element** Fenster geöffnet.  

```console
inspect(document.body);
```  

> ##### Abbildung 15  
> Überprüfen eines Elements mit `inspect()`  
> ![Überprüfen eines Elements mit Inspect ()][ImageInspectElement]  

Beim Übergeben einer zu überprüfenden Methode wird das Dokument im **Quellen** Panel geöffnet, damit Sie es überprüfen können.  

## getEventListeners  

```console
getEventListeners(object)
```  

Gibt die für das angegebene Objekt registrierten Ereignislistener zurück.  Der Rückgabewert ist ein Objekt, das für jeden registrierten Ereignistyp \ (wie `click` oder \) ein Array enthält `keydown` .  Die Mitglieder jedes Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.  In [Abbildung 16](#figure-16)werden alle Ereignislistener aufgelistet, die für das Document-Objekt registriert sind.  

```console
getEventListeners(document);
```  

> ##### Abbildung 16  
> Ausgabe der Verwendung `getEventListeners(document)`  
> ![Ausgabe der Verwendung von getEventListeners (Dokument)][ImageGetListeners]  

Wenn mehr als ein Listener für das angegebene Objekt registriert ist, enthält das Array ein Element für jeden Listener.  In [Abbildung 16](#figure-16)sind zwei Ereignis-Listener für das Dokumentelement für das Ereignis registriert `click` .  

> ##### Abbildung 17  
> Mehrere Listener  
> ![Mehrere Listener][ImageMultipleListeners]  

Sie können jedes der folgenden Objekte erweitern, um die Eigenschaften zu untersuchen.  

> ##### Abbildung 18  
> Erweiterte Ansicht des Listener-Objekts  
> ![Erweiterte Ansicht des Listener-Objekts][ImageListenersExpanded]  

## Tasten  

```console
keys(object)
```  

Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.  Um die zugeordneten Werte der gleichen Eigenschaften abzurufen, verwenden Sie `values()` .  

Angenommen, Ihre Anwendung hat das folgende Objekt definiert.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

In [Abbildung 19](#figure-19)wurde davon ausgegangen, dass das Ergebnis `player1` vor der Eingabe `keys(player1)` und in der Konsole im globalen Namespace \ (zur Vereinfachung \) definiert wurde `values(player1)` .  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### Abbildung 19  
> Die `keys()` `values()` Befehle und  
> ![Die Befehle "Keys ()" und "Values ()"][ImageConsoleKeysValues]  

## Monitor  

```console
monitor(method)
```  

Protokolliert eine Nachricht an die Konsole, die den Methodennamen zusammen mit den Argumenten angibt, die beim Aufrufen an die Methode übergeben werden.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### Abbildung 20  
> Die `monitor()` Methode  
> ![Die Monitor ()-Methode][ImageConsoleMonitorSum]  

Verwenden Sie diese Einstellung `unmonitor(method)` , um die Überwachung zu beenden.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Wenn eines der angegebenen Ereignisse für das angegebene Objekt eintritt, wird das Ereignisobjekt in der Konsole protokolliert.  Sie können ein einzelnes Ereignis angeben, das überwacht werden soll, ein Array von Ereignissen oder einen der generischen Ereignistypen, die einer vordefinierten Sammlung von Ereignissen zugeordnet sind.  Siehe [Abbildung 21](#figure-21).  

Im folgenden werden alle Größen Änderungsereignisse für das Window-Objekt überwacht.  

```console
monitorEvents(window, "resize");
```  

> ##### Abbildung 21  
> Überwachen von Fenstergrößen Ereignissen  
> ![Überwachen von Fenstergrößen Ereignissen][ImageMonitorResize]  

Im folgenden wird ein Array zum Überwachen `resize` von beiden und `scroll` Ereignissen für das Window-Objekt definiert.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Sie können auch einen der verfügbaren Arten von Ereignissen angeben, Zeichenfolgen, die vordefinierten Gruppen von Ereignissen zugeordnet sind.  In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugehörigen Ereigniszuordnungen angezeigt.  

| Ereignistyp | Entsprechende zugeordnete Ereignisse |  
|:--- |:--- |  
| `mouse` | "klicken", "DblClick", "MouseDown", "MouseMove", "Mouse Out", "MouseOver", "MouseUp", "Mausrad" |  
| `key` | "KeyDown"; "keypress"; "KeyUp"; "TextInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "Blur"; "ändern"; "Fokus"; "Zurücksetzen"; "Größe"; "Scrollen"; "auswählen"; "Absenden"; "Zoom" |  

In [Abbildung 22](#figure-22)ist der `key` Ereignistyp, der `key` Ereignissen in einem Eingabetextfeld entspricht, aktuell im Bereich **Elemente** ausgewählt.  

```console
monitorEvents($0, "key");
```  

In [Abbildung 22](#figure-22) wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.  

> ##### Abbildung 22  
> Überwachen von Schlüsselereignissen  
> ![Überwachen von Schlüsselereignissen][ImageMonitorKey]  

## profile  

```console
profile([name])
```  

Startet eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen.  Die [profileEnd ()](#profileend) -Methode vervollständigt das Profil und zeigt die Ergebnisse im **Speicher** Panel an.  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Führen `profile()` Sie die Methode aus, um die Profilerstellung zu starten.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Führen Sie die [profileEnd ()](#profileend) -Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.  

Profile können auch geschachtelt sein.  In [Abbildung 23](#figure-23) ist das Ergebnis unabhängig von der Reihenfolge identisch.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.  

## profileEnd  

```console
profileEnd([name])
```  

Schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speicher** Panel an.  Sie müssen die [profile ()](#profile) -Methode ausführen.  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Führen Sie die [profile ()](#profile) -Methode aus, um die Profilerstellung zu starten.  
1.  Führen `profileEnd()` Sie die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.  
    
    ```console
    profileEnd("My profile")
    ```  

Profile können auch geschachtelt sein.  In [Abbildung 23](#figure-23) ist das Ergebnis unabhängig von der Reihenfolge identisch.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Das Ergebnis wird als Heap-Momentaufnahme im **Speicher** Panel angezeigt.  

> ##### Abbildung 23  
> Gruppierte profile  
> ![Gruppierte profile][ImageGroupedProfiles]  

> [!NOTE]
> Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.  

## Tabelle  

```console
table(data[, columns])
```  

Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt mit optionalen Spaltenüberschriften.  In [Abbildung 24](#figure-24)wird eine Liste mit Namen angezeigt, die eine Tabelle in der Konsole verwenden.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

> ##### Abbildung 24  
> Die `table()` Methode  
> ![Die Table ()-Methode][ImageConsoleTable]  

## undebug  

```console
undebug(method)
```  

Beendet das Debuggen der angegebenen Methode, sodass der Debugger beim Aufrufen der Methode nicht mehr aufgerufen wird.  

```console
undebug(getData);
```  

## Unmonitor  

```console
unmonitor(method)
```  

Beendet die Überwachung der angegebenen Methode.  Dies wird in Concert mit der [Monitor ()](#monitor) -Methode verwendet.  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Beendet das Überwachen von Ereignissen für das angegebene Objekt und die Ereignisse.  Im folgenden Beispiel werden alle Ereignisüberwachungen für das Window-Objekt angehalten.  

```console
unmonitorEvents(window);
```  

Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.  Mit dem folgenden Code wird beispielsweise das Überwachen aller `mouse` Ereignisse für das aktuell ausgewählte Element gestartet und dann die Überwachung von `mousemove` Ereignissen beendet \ (vielleicht, um Rauschen in der Konsolenausgabe zu verringern \).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## Werte  

```console
values(object)
```  

Gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Abbildung 1: $ _ ist der zuletzt ausgewertete Ausdruck"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Abbildung 2: $ _ ändert sich, wenn neue Befehle ausgewertet werden"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Abbildung 3: die $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Abbildung 4: die $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Abbildung 5: $ (' img ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Abbildung 6: $ (' img '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Abbildung 7: $ (' img ', Document. querySelector (' Titel--Bild ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Abbildung 8: Verwenden von $ $ () zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Abbildung 9: Verwenden von $ $ () zum Auswählen aller Bilder, die nach dem angegebenen <div->-Element im Dokument angezeigt werden, und Anzeigen der Quellen"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Abbildung 10: Verwenden einer XPath-Auswahl"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Abbildung 11: Verwenden einer komplexeren XPath-Auswahl"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Abbildung 12: Verwenden einer XPath-Auswahl mit startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Abbildung 13: durchbrechen innerhalb einer Methode mit Debug ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Abbildung 14: Protokollieren von Document. Body mit dir ()-Methode"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Abbildung 15: Überprüfen eines Elements mit Inspect ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Abbildung 16: Ausgabe der Verwendung von getEventListeners (Dokument)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Abbildung 17: mehrere Listener"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Abbildung 18: Erweiterte Ansicht des Listener-Objekts"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Abbildung 19: die Befehle "Keys ()" und "Values ()""  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Abbildung 20: die Monitor ()-Methode"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Abbildung 21: Überwachen von Fenstergrößen Ereignissen"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Abbildung 22: Überwachen von Schlüsselereignissen"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Abbildung 23: gruppierte profile"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Abbildung 24: die Tabelle ()-Methode"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir-Console-API-Referenz"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Beschleunigen der JavaScript-Laufzeit"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problem 1050237: Debuggen (Funktion) funktioniert nicht | Monorail"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
