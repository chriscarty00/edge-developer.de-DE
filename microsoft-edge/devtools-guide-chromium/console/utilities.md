---
title: API-Referenz für Konsolen Dienstprogramme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: efa03e02813d718514f73445bc0dceb3a1a83f39
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708828"
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

In der folgenden Abbildung wird ein einfacher Ausdruck \ ( `2 + 2` \) ausgewertet.  `$_`Anschließend wird die Eigenschaft ausgewertet, die den gleichen Wert enthält.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   Abbildung 1: `$_` ist der zuletzt ausgewertete Ausdruck  
:::image-end:::  

In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.  Auswerten, `$_.length` um die Länge des Arrays zu ermitteln, wird der Wert, der in Änderungen gespeichert wird, `$_` zum neuesten ausgewerteten Ausdruck `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ ändert sich, wenn neue Befehle ausgewertet werden" lightbox="../media/console-array-length.msft.png":::
   Abbildung 2: `$_` Änderungen, wenn neue Befehle ausgewertet werden  
:::image-end:::  

## Zuletzt ausgewähltes Element oder JavaScript-Objekt  

```console
$0
```  

Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.  `$1` Gibt die zweite zuletzt ausgewählte Person zurück usw.  Die `$0` `$1` Befehle,,, und werden `$2` `$3` `$4` als historischer Bezug auf die letzten fünf im Bereich **Elemente** geprüften DOM-Elemente oder die letzten fünf im **Speicher** Bereich ausgewählten JavaScript-Heapobjekte ausgeführt.  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

In der folgenden Abbildung ist ein `img` Element im Panel **Elemente** ausgewählt.  Wurde im **Konsolen** Einzug `$0` ausgewertet und zeigt dasselbe Element an.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Das $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Abbildung 3: die `$0`  
:::image-end:::  

In der folgenden Abbildung zeigt das Bild ein anderes Element, das auf der gleichen Seite markiert ist.  Das `$0` jetzt bezieht sich auf das neu ausgewählte Element, `$1` gibt aber die zuvor ausgewählte zurück.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="Das $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Abbildung 4: die `$1`  
:::image-end:::  

## Abfrageauswahl  

```console
$(selector, [startNode])
```  

Gibt den Verweis auf das erste DOM-Element mit der angegebenen CSS-Auswahl zurück.  Diese Methode ist ein Alias für die [Document. querySelector ()][MDNDocumentQuerySelector] -Methode.  

In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ (' Img ')" lightbox="../media/console-element-selector-image.msft.png":::
   Abbildung 5: die `$('img')`  
:::image-end:::  

Zeigen Sie auf das zurückgegebene Ergebnis, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **im Element Panel** anzeigen aus, um es im Dom zu finden, oder **Scrollen Sie in zu Ansicht** , um es auf der Seite anzuzeigen.  

In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ (' Img '). src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Abbildung 6: die `$('img').src`  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

In der folgenden Abbildung `img` befindet sich das erste Element nach dem `title--image` und zeigt die `src` ordnungsgemäße zurückgegeben wird.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="Der $ (' img ', Document. querySelector (' Titel--Bild ')). src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Abbildung 7: die `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet wird `$` , wird die Funktionalität überschrieben und `$` entspricht der Implementierung aus dieser Bibliothek.  

## Abfrageauswahl alle  

```console
$$(selector, [startNode])
```  

Gibt ein Array von Elementen zurück, die der angegebenen CSS-Auswahl entsprechen.  Diese Methode entspricht dem Aufrufen der [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] -Methode.  

Verwenden Sie im folgenden Codebeispiel und in der Abbildung `$$()` ein Array aller `<img>` Elemente im aktuellen Dokument, und zeigen Sie den Wert der `src` Eigenschaft für jedes Element an.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Verwenden von $ $ (), um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen" lightbox="../media/console-element-selector-image-all.msft.png":::
   Abbildung 8: verwenden `$$()` , um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

Im folgenden Codebeispiel und in der Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der Abbildung verwendet, `$$()` um ein Array aller `<img>` Elemente zu erstellen, die im aktuellen Dokument nach dem ausgewählten Knoten angezeigt werden.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Verwenden von $ $ (), um alle Bilder auszuwählen, die nach dem angegebenen <div->-Element im Dokument angezeigt werden, und Anzeigen der Quellen" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Abbildung 9: verwenden `$$()` , um alle Bilder auszuwählen, die nach dem angegebenen `<div>` Element im Dokument angezeigt werden, und Anzeigen der Quellen  
:::image-end:::  

> [!NOTE]
> Drücken Sie `Shift` + `Enter` in der Konsole, um eine neue Zeile zu starten, ohne das Skript auszuführen.  

## XPath  

```console
$x(path, [startNode])
```  

Gibt ein Array von DOM-Elementen zurück, die dem angegebenen XPath-Ausdruck entsprechen.  

Im folgenden Codebeispiel und in der Abbildung `<p>` werden alle Elemente auf der Seite zurückgegeben.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Verwenden einer XPath-Auswahl" lightbox="../media/console-array-xpath.msft.png":::
   Abbildung 10: Verwenden einer XPath-Auswahl  
:::image-end:::  

Im folgenden Codebeispiel und in der Abbildung `<p>` werden alle Elemente `<a>` zurückgegeben, die Elemente enthalten.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Verwenden einer komplexeren XPath-Auswahl" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Abbildung 11: Verwenden einer komplexeren XPath-Auswahl  
:::image-end:::  

Ähnlich wie bei den anderen Auswahlbefehlen `$x(path)` verfügt ein optionaler zweiter Parameter, der `startNode` ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Verwenden einer XPath-Auswahl mit startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Abbildung 12: Verwenden einer XPath-Auswahl mit `startNode`  
:::image-end:::  

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
> Das [Chrom Problem #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.  Wenn das Problem auftritt, versuchen Sie stattdessen, [Haltepunkte zu verwenden][DevtoolsJavascriptBreakpoints] .  

Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im Bereich " **Quellen** " unterbricht, sodass Sie den Code schrittweise durchlaufen und Debuggen können.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Durchbrechen innerhalb einer Methode mit Debug ()" lightbox="../media/console-debug-text.msft.png":::
   Abbildung 13: durchbrechen innerhalb einer Methode mit `debug()`  
:::image-end:::  

Verwenden Sie diese Option, `undebug(method)` um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.  

Weitere Informationen zu Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Zeigt eine Objektstil Auflistung aller Eigenschaften für das angegebene Objekt an.  Diese Methode ist ein Alias für die [Console. dir ()][MDNConsoleDir] -Methode.  

Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den `<head>` und- `</head>` Tags anzuzeigen.  Im folgenden Codebeispiel und in der Abbildung wird nach der Verwendung in der Konsole ein Objektformat Eintrag angezeigt `console.dir()` .  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Protokollierungs Dokument. Head mit dir ()-Methode" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Abbildung 14: Protokollierung `document.head` mit `dir()` Methode  
:::image-end:::  

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

Im folgenden Codebeispiel und in der Abbildung `document.body` wird das im Panel **Elemente** geöffnet.  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Überprüfen eines Elements mit Inspect ()" lightbox="../media/console-inspect-document-body.msft.png":::
   Abbildung 15: Überprüfen eines Elements mit `inspect()`  
:::image-end:::  

Beim Übergeben einer zu überprüfenden Methode wird das Dokument im **Quellen** Panel geöffnet, damit Sie es überprüfen können.  

## getEventListeners  

```console
getEventListeners(object)
```  

Gibt die für das angegebene Objekt registrierten Ereignislistener zurück.  Der Rückgabewert ist ein Objekt, das für jeden registrierten Ereignistyp \ (wie `click` oder \) ein Array enthält `keydown` .  Die Mitglieder jedes Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.  Im folgenden Codebeispiel werden alle für das Document-Objekt registrierten Ereignislistener aufgelistet.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Ausgabe der Verwendung von getEventListeners (Dokument)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Abbildung 16: das Ergebnis der Verwendung `getEventListeners(document)`  
:::image-end:::  

Wenn mehr als ein Listener für das angegebene Objekt registriert ist, enthält das Array ein Element für jeden Listener.  In der folgenden Abbildung sind zwei Ereignis-Listener für das Document-Element für das `click` Ereignis registriert.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Mehrere Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Abbildung 17: mehrere Listener  
:::image-end:::  

Sie können jedes der folgenden Objekte erweitern, um die Eigenschaften zu untersuchen.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Erweiterte Ansicht des Listener-Objekts" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Abbildung 18: Erweiterte Ansicht des Listener-Objekts  
:::image-end:::  

## Tasten  

```console
keys(object)
```  

Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.  Um die zugeordneten Werte der gleichen Eigenschaften abzurufen, verwenden Sie `values()` .  

Angenommen, Ihre Anwendung hat das folgende Objekt definiert.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

In den folgenden Codebeispielen und einer Abbildung wird davon ausgegangen, dass das Ergebnis `player1` vor der Eingabe `keys(player1)` und in der Konsole im globalen Namespace \ (zur Vereinfachung \) definiert wurde `values(player1)` .  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Die Befehle "Keys ()" und "Values ()"" lightbox="../media/console-keys-values.msft.png":::
   Abbildung 19: die `keys()` `values()` Befehle und  
:::image-end:::  

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

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Die Monitor ()-Methode" lightbox="../media/console-function-monitor-sum.msft.png":::
   Abbildung 20: die `monitor()` Methode  
:::image-end:::  

Verwenden Sie diese Einstellung `unmonitor(method)` , um die Überwachung zu beenden.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Wenn eines der angegebenen Ereignisse für das angegebene Objekt eintritt, wird das Ereignisobjekt in der Konsole protokolliert.  Sie können ein einzelnes Ereignis angeben, das überwacht werden soll, ein Array von Ereignissen oder einen der generischen Ereignistypen, die einer vordefinierten Sammlung von Ereignissen zugeordnet sind.  Das folgende Codebeispiel und die Abbildung finden Sie hier.  

Im folgenden werden alle Größen Änderungsereignisse für das Window-Objekt überwacht.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Überwachen von Fenstergrößen Ereignissen" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Abbildung 21: Überwachen von Fenstergrößen Ereignissen  
:::image-end:::  

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

Im folgenden Codebeispiel ist der `key` Ereignistyp, der `key` Ereignissen in einem Eingabetextfeld entspricht, aktuell im Bereich **Elemente** ausgewählt.  

```console
monitorEvents($0, "key");
```  

In der folgenden Abbildung wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Überwachen von Schlüsselereignissen" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Abbildung 22: Überwachen von Schlüsselereignissen  
:::image-end:::  

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

Profile können auch geschachtelt sein.  In den folgenden Codebeispielen und Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.  

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

Profile können auch geschachtelt sein.  Im folgenden Codebeispiel und in Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Das Ergebnis wird als Heap-Momentaufnahme im **Speicher** Panel angezeigt.  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Gruppierte profile" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Abbildung 23: gruppierte profile  
:::image-end:::  

> [!NOTE]
> Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.  

## queryObjects  

```console
queryObjects(Constructor)
```  

Gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.  Der Bereich von `queryObjects()` ist der aktuell ausgewählte Laufzeitkontext in der Konsole.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Gibt alle zurück `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Gibt alle HTML-Elemente zurück.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Gibt alle Objekte zurück, die mithilfe von instanziiert wurden `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## Tabelle  

```console
table(data[, columns])
```  

Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt mit optionalen Spaltenüberschriften.  Im folgenden Codebeispiel und in der Abbildung wird eine Liste mit Namen angezeigt, die eine Tabelle in der Konsole verwenden.  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Das Ergebnis der Tabelle ()-Methode" lightbox="../media/console-table-display.msft.png":::
   Abbildung 24: das Ergebnis der `table()` Methode  
:::image-end:::  

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

Beendet die Überwachung der angegebenen Methode.  Diese Methode wird in Concert mit der [Monitor ()](#monitor) -Methode verwendet.  

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
