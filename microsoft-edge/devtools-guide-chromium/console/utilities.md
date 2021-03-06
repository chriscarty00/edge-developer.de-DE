---
description: Ein Verweis auf Komfortbefehle, die in der Microsoft Edge DevTools-Konsole verfügbar sind.
title: Referenz zur Konsolen-Hilfsprogramme-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398826"
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

# <a name="console-utilities-api-reference"></a>Referenz zur Konsolen-Hilfsprogramme-API  

Die Console Utilities-API enthält eine Auflistung von Komfortbefehlen zum Ausführen gängiger Aufgaben: Auswählen und Überprüfen von DOM-Elementen, Anzeigen von Daten im lesbaren Format, Beenden und Starten des Profilers und Überwachen von DOM-Ereignissen.  

> [!WARNING]
> Die folgenden Befehle funktionieren nur in der Microsoft Edge DevTools-Konsole.  Die Befehle funktionieren nicht, wenn sie aus Ihren Skripts ausgeführt werden.  

Navigieren Sie `console.log()` für `console.error()` die und-Methoden der restlichen `console.*` Methoden zu [Konsolen-API-Referenz][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Kürzlich ausgewerteter Ausdruck  

```console
$_
```  

Gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.  

In der folgenden Abbildung wird ein einfacher Ausdruck \( `2 + 2` \) ausgewertet.  Die `$_` Eigenschaft wird dann ausgewertet, die denselben Wert enthält.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   Abbildung 1:  `$_` ist der zuletzt ausgewertete Ausdruck  
:::image-end:::  

In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.  Auswerten, um die Länge des Arrays zu finden, wird der in Änderungen gespeicherte Wert zum `$_.length` `$_` neuesten ausgewerteten Ausdruck, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ ändert sich, wenn neue Befehle ausgewertet werden" lightbox="../media/console-array-length.msft.png":::
   Abbildung 2:  `$_` Änderungen bei der Auswertung neuer Befehle  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a>Kürzlich ausgewähltes Element oder JavaScript-Objekt  

```console
$0
```  

Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.  `$1` gibt den zweiten zuletzt ausgewählten zurück, und so weiter.  Die Befehle , , , und funktionieren als verlaufshistorische Referenz zu den letzten fünf DOM-Elementen, die im Elementtool oder den letzten fünf im Speichertool ausgewählten `$0` `$1` `$2` `$3` `$4` JavaScript-Heapobjekten überprüft wurden. **** ****  

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

In der folgenden Abbildung wird `img` ein Element im **Elementtool ausgewählt.**  In der **Konsolenschube** `$0` wurde ausgewertet und zeigt dasselbe Element an.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Die $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Abbildung 3: Die `$0`  
:::image-end:::  

In der folgenden Abbildung zeigt die Abbildung ein anderes Element, das auf derselben Seite ausgewählt ist.  The `$0` bezieht sich nun auf das neu ausgewählte Element, während das zuvor ausgewählte Element zurückgegeben `$1` wird.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="Die $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Abbildung 4: Die `$1`  
:::image-end:::  

## <a name="query-selector"></a>Abfrageauswahl  

```console
$(selector, [startNode])
```  

Gibt den Verweis auf das erste DOM-Element mit dem angegebenen CSS-Selektor zurück.  Diese Methode ist ein Alias für die [document.querySelector()-Methode.][MDNDocumentQuerySelector]  

In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Abbildung 5: Die `$('img')`  
:::image-end:::  

Zeigen Sie auf das zurückgegebene Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie Im Elementbereich einblenden aus, um es im DOM zu finden, oder scrollen Sie **in** ansicht, um es auf der Seite anzuzeigen. ****  

In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Abbildung 6: Die `$('img').src`  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, von dem aus nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

In der folgenden Abbildung wird das erste Element gefunden, nachdem das gefunden wurde und das ordnungsgemäß `img` `title--image` angezeigt `src` wird.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Abbildung 7: Die `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet, wird die Funktionalität überschrieben und entspricht der Implementierung `$` `$` aus dieser Bibliothek.  

## <a name="query-selector-all"></a>Abfrageauswahl alle  

```console
$$(selector, [startNode])
```  

Gibt ein Array von Elementen zurück, die mit dem angegebenen CSS-Selektor übereinstimmen.  Diese Methode entspricht dem Ausführen der [document.querySelectorAll()-Methode.][MDNDocumentQuerySelectorAll]  

Im folgenden Codebeispiel und der folgenden Abbildung können Sie ein Array aller Elemente im aktuellen Dokument erstellen und den Wert der Eigenschaft `$$()` `<img>` für jedes Element `src` anzeigen.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Verwenden von $$() zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen" lightbox="../media/console-element-selector-image-all.msft.png":::
   Abbildung 8: Verwenden `$$()` zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, von dem aus nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

Im folgenden Codebeispiel und der folgenden Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der abbildung verwendet, um ein Array aller Elemente zu erstellen, die im aktuellen Dokument nach dem ausgewählten `$$()` `<img>` Knoten angezeigt werden.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Verwenden von $$(), um alle Bilder auszuwählen, die nach dem angegebenen <div> im Dokument angezeigt werden, und die Quellen anzeigen" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Abbildung 9: `$$()` Verwenden, um alle Bilder auszuwählen, die nach dem angegebenen Element im Dokument angezeigt werden, und `<div>` die Quellen anzeigen  
:::image-end:::  

> [!NOTE]
> Wählen `Shift` + `Enter` Sie in der Konsole aus, um eine neue Zeile zu starten, ohne das Skript auszuführen.  

## <a name="xpath"></a>XPath  

```console
$x(path, [startNode])
```  

Gibt ein Array von DOM-Elementen zurück, die mit dem angegebenen XPath-Ausdruck übereinstimmen.  

Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente auf der Seite `<p>` zurückgegeben.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Verwenden eines XPath-Selektors" lightbox="../media/console-array-xpath.msft.png":::
   Abbildung 10: Verwenden eines XPath-Selektors  
:::image-end:::  

Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente zurückgegeben, die Elemente `<p>` `<a>` enthalten.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Verwenden eines komplizierteren XPath-Selektors" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Abbildung 11: Verwenden eines komplizierteren XPath-Selektors  
:::image-end:::  

Ähnlich wie die anderen Selektorbefehle verfügt über einen optionalen zweiten Parameter, der ein Element oder einen Knoten angibt, von dem aus `$x(path)` nach Elementen gesucht werden `startNode` soll.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Verwenden eines XPath-Selektors mit startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Abbildung 12: Verwenden eines XPath-Selektors mit `startNode`  
:::image-end:::  

## <a name="clear"></a>clear  

```console
clear()
```  

Die Konsole des Verlaufs wird geräumt.  

```console
clear()
```  

## <a name="copy"></a>copy  

```console
copy(object)
```  

Die `copy(object)` Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.  

```console
copy($0)
```  

## <a name="debug"></a>debuggen  

```console
debug(method)
```  

>[!NOTE]
> Das [#A0 #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.  Wenn das Problem auftreten sollte, versuchen Sie stattdessen, [Haltepunkte zu][DevtoolsJavascriptBreakpoints] verwenden.  

Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im **Sources-Tool** umbricht, sodass Sie den Code schrittweise durchbrechen und debuggen können.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Durchbrechen einer Methode mit debug()" lightbox="../media/console-debug-text.msft.png":::
   Abbildung 13: Einbrechen in eine Methode mit `debug()`  
:::image-end:::  

Verwenden `undebug(method)` Sie diese Option, um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.  

Weitere Informationen zu Haltepunkten finden Sie unter [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].  

## <a name="dir"></a>dir  

```console
dir(object)
```  

Zeigt eine Objektformatliste aller Eigenschaften für das angegebene Objekt an.  Diese Methode ist ein Alias für die [console.dir()-Methode.][MDNConsoleDir]  

Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den tags und zu `<head>` `</head>` anzeigen.  Im folgenden Codebeispiel und der folgenden Abbildung wird nach der Verwendung in der Konsole eine Auflistung im `console.dir()` Objektstil angezeigt.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Protokollierung von document.head mit dir()-Methode" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Abbildung 14: `document.head` Protokollierung mit `dir()` Methode  
:::image-end:::  

Weitere Informationen finden Sie unter Eintrag [`console.dir()`][DevToolsConsoleApiConsoleDirObject] in der Konsolen-API.  

## <a name="dirxml"></a>dirxml  

```console
dirxml(object)
```  

Druckt eine XML-Darstellung des angegebenen Objekts, wie im **Elementtool** angezeigt.  Diese Methode entspricht der [console.dirxml()-Methode.][MDNConsoleDirxml]  

## <a name="inspect"></a>inspect  

```console
inspect(object/method)
```  

Öffnet und wählt das angegebene Element oder Objekt im entsprechenden Bereich aus: entweder das **Elementtool** für DOM-Elemente oder das **Speichertool** für JavaScript-Heapobjekte.  

Im folgenden Codebeispiel und der folgenden Abbildung wird `document.body` das im **Elementtool** geöffnet.  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Überprüfen eines Elements mit inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Abbildung 15: Überprüfen eines Elements mit `inspect()`  
:::image-end:::  

Beim Übergeben einer Zu überprüfenden Methode öffnet **** die Methode das Dokument im Sources-Tool, damit Sie es überprüfen können.  

## <a name="geteventlisteners"></a>getEventListeners  

```console
getEventListeners(object)
```  

Gibt die Ereignislistener zurück, die für das angegebene Objekt registriert sind.  Der Rückgabewert ist ein Objekt, das ein Array für jeden registrierten Ereignistyp \(z. B. `click` oder `keydown` \) enthält.  Die Member der einzelnen Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.  In der folgenden Codebeispielfigur werden alle ereignislistener aufgeführt, die für das Dokumentobjekt registriert sind.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Ausgabe der Verwendung von getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Abbildung 16: Das Ergebnis der Verwendung `getEventListeners(document)`  
:::image-end:::  

Wenn mehrere Listener für das angegebene Objekt registriert sind, enthält das Array ein Element für jeden Listener.  In der folgenden Abbildung sind zwei Ereignislistener für das Dokumentelement für das Ereignis `click` registriert.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Mehrere Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Abbildung 17: Mehrere Listener  
:::image-end:::  

Sie können jedes der folgenden Objekte weiter erweitern, um die Eigenschaften zu erkunden.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Erweiterte Ansicht des Listenerobjekts" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Abbildung 18: Erweiterte Ansicht des Listenerobjekts  
:::image-end:::  

## <a name="keys"></a>Tasten  

```console
keys(object)
```  

Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.  Um die zugeordneten Werte derselben Eigenschaften zu erhalten, verwenden Sie `values()` .  

Angenommen, Ihre Anwendung hat das folgende Objekt definiert.  

```console
var player1 =   
```  

In den folgenden Codebeispielen und abbildung wird davon ausgegangen, dass das Ergebnis vor der Eingabe und in der Konsole im globalen `player1` Namespace \(zur Einfachheit\) `keys(player1)` `values(player1)` definiert wurde.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Die Befehle keys() und values()" lightbox="../media/console-keys-values.msft.png":::
   Abbildung 19: Die `keys()` Befehle und `values()`  
:::image-end:::  

## <a name="monitor"></a>Monitor  

```console
monitor(method)
```  

Protokolliert eine Nachricht an die Konsole, die den Methodennamen zusammen mit den Argumenten angibt, die beim Aufgerufen an die -Methode übergeben werden.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Die monitor()-Methode" lightbox="../media/console-function-monitor-sum.msft.png":::
   Abbildung 20: Die `monitor()` Methode  
:::image-end:::  

Verwenden `unmonitor(method)` Sie, um die Überwachung zu beenden.  

## <a name="monitorevents"></a>monitorEvents  

```console
monitorEvents(object[, events])
```  

Wenn eines der angegebenen Ereignisse für das angegebene Objekt auftritt, wird das Ereignisobjekt bei der Konsole protokolliert.  Sie können ein einzelnes zu überwachende Ereignis, ein Array von Ereignissen oder einen der generischen Ereignistypen angeben, die einer vordefinierten Auflistung von Ereignissen zugeordnet sind.  Überprüfen Sie das folgende Codebeispiel und die folgende Abbildung.  

Im Folgenden werden alle Größenänderungsereignisse des Fensterobjekts überwacht.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Überwachen von Fenstergrößeereignissen" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Abbildung 21: Überwachen von Fenstergrößeereignissen  
:::image-end:::  

Im Folgenden wird ein Array definiert, das sowohl die Ereignisse als `resize` `scroll` auch das Fensterobjekt überwacht.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Sie können auch einen der verfügbaren Ereignistypen angeben, Zeichenfolgen, die vordefinierten Ereignissätzen zuordnungen.  In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugeordneten Ereigniszuordnungen angezeigt.  

| Ereignistyp | Entsprechende zugeordnete Ereignisse |  
|:--- |:--- |  
| `mouse` | "click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel" |  
| `key` | "keydown", "keypress", "keyup", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom" |  

Im folgenden Codebeispiel wird der Ereignistyp, der Ereignissen in einem Eingabetextfeld entspricht, `key` `key` derzeit im **Elementtool** ausgewählt.  

```console
monitorEvents($0, "key");
```  

In der folgenden Abbildung wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Überwachen wichtiger Ereignisse" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Abbildung 22: Überwachen wichtiger Ereignisse  
:::image-end:::  

## <a name="profile"></a>profile  

```console
profile([name])
```  

Startet eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen.  Die [profileEnd()-Methode](#profileend) schließt das Profil ab und zeigt die Ergebnisse im **Speichertool** an.  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Führen Sie die `profile()` Methode aus, um die Profilerstellung zu starten.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Führen Sie die [profileEnd()-Methode](#profileend) aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool anzeigen** zu können.  

Profile können auch geschachtelt sein.  In den folgenden Codebeispielen und abbildung ist das Ergebnis unabhängig von der Reihenfolge gleich.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.  

## <a name="profileend"></a>profileEnd  

```console
profileEnd([name])
```  

Schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speichertool** an.  Sie müssen die [profile()-Methode](#profile) ausführen.  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Führen Sie die [profile()-Methode](#profile) aus, um die Profilerstellung zu starten.  
1.  Führen Sie `profileEnd()` die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool** anzeigen.  
    
    ```console
    profileEnd("My profile")
    ```  

Profile können auch geschachtelt sein.  Im folgenden Codebeispiel und in der abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Das Ergebnis wird als Heap-Momentaufnahme im **Speichertool** angezeigt.  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Gruppieren von Profilen" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Abbildung 23: Gruppieren von Profilen  
:::image-end:::  

> [!NOTE]
> Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.  

## <a name="queryobjects"></a>queryObjects  

```console
queryObjects(Constructor)
```  

Gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.  Der Bereich `queryObjects()` von ist der aktuell ausgewählte Laufzeitkontext in der Konsole.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Gibt alle `Promises` zurück.  
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
      
      Gibt alle Objekte zurück, die mit instanziiert `new functionName()` wurden.  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>Tabelle  

```console
table(data[, columns])
```  

Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt in mit optionalen Spaltenüberschriften.  Im folgenden Codebeispiel und der folgenden Abbildung wird eine Liste der Namen angezeigt, die eine Tabelle in der Konsole verwenden.  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Das Ergebnis der table()-Methode" lightbox="../media/console-table-display.msft.png":::
   Abbildung 24: Das Ergebnis der `table()` Methode  
:::image-end:::  

## <a name="undebug"></a>undebug  

```console
undebug(method)
```  

Beendet das Debuggen der angegebenen Methode, sodass beim Aufruf der Methode der Debugger nicht mehr aufgerufen wird.  

```console
undebug(getData);
```  

## <a name="unmonitor"></a>unmonitor  

```console
unmonitor(method)
```  

Beendet die Überwachung der angegebenen Methode.  Diese Methode wird in Zusammenarbeit mit der [monitor()-Methode](#monitor) verwendet.  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a>unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Beendet Überwachungsereignisse für das angegebene Objekt und die angegebenen Ereignisse.  Im Folgenden wird beispielsweise die Ereignisüberwachung für das Window-Objekt beendet.  

```console
unmonitorEvents(window);
```  

Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.  Der folgende Code startet beispielsweise die Überwachung aller Ereignisse für das aktuell ausgewählte Element und beendet dann Überwachungsereignisse \(möglicherweise, um das Rauschen in der `mouse` Konsolenausgabe `mousemove` zu reduzieren\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a>werte  

```console
values(object)
```  

Gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir – Konsolen-API-Referenz"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Beschleunigen der JavaScript-Runtime"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problem 1050237: debug(function) funktioniert nicht | Monorail"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
