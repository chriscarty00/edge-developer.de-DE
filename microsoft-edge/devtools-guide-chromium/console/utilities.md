---
description: Ein Verweis auf Komfortbefehle, die in der Microsoft Edge DevTools Console verfügbar sind.
title: API-Referenz zu Konsolen-Dienstprogrammen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c6a0356bd590809f9164aa62fd42156f901cef0f
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483282"
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
# <a name="console-utilities-api-reference"></a>API-Referenz zu Konsolen-Dienstprogrammen  

Die Console Utilities-API enthält eine Auflistung von Komfortbefehlen, um die folgenden allgemeinen Aufgaben auszuführen.  

*   Auswählen und Überprüfen von DOM-Elementen  
*   Anzeigen von Daten im lesbaren Format  
*   Beenden und Starten des Profilers  
*   Überwachen von DOM-Ereignissen  
    
> [!WARNING]
> Die folgenden Befehle funktionieren nur in der Microsoft Edge DevTools **Console**.  Die Befehle funktionieren nicht, wenn sie aus Ihren Skripts ausgeführt werden.  

Weitere Informationen zu den `console.log()` und-Methoden und den restlichen Methoden finden `console.error()` Sie unter Console API `console.*` [Reference][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Kürzlich ausgewerteter Ausdruck  

### <a name="console-syntax"></a>Konsolensyntax  

```console
$_
```  

Dieser Befehl gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.  

### <a name="console-example"></a>Konsolenbeispiel  

In der folgenden Abbildung wird ein einfacher Ausdruck \( `2 + 2` \) ausgewertet.  Die `$_` Eigenschaft wird dann ausgewertet, die denselben Wert enthält.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   `$_` ist der zuletzt ausgewertete Ausdruck  
:::image-end:::  

In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.  Auswerten, um die Länge des Arrays zu finden, wird der in gespeicherte Wert `$_.length` `$_` zum neuesten ausgewerteten Ausdruck, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ ändert sich, wenn neue Befehle ausgewertet werden" lightbox="../media/console-array-length.msft.png":::
   `$_` Änderungen bei der Auswertung neuer Befehle  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a>Zuletzt ausgewähltes Element oder JavaScript-Objekt  

### <a name="console-syntax"></a>Konsolensyntax  

```console
$0
```  

Dieser Befehl gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.  `$1` gibt die zuletzt ausgewählte zweite zurück, und so weiter.  Die Befehle , , , und funktionieren als verlaufshistorische Referenz zu den letzten fünf DOM-Elementen, die im Elementtool oder den letzten fünf im Speichertool ausgewählten `$0` `$1` `$2` `$3` `$4` JavaScript-Heapobjekten überprüft wurden. **** ****  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a>Konsolenbeispiel  

In der folgenden Abbildung wird `img` ein Element im **Elementtool ausgewählt.**  In der **Konsolenschube** `$0` wurde ausgewertet und zeigt dasselbe Element an.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Die $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Der `$0`  
:::image-end:::  

In der folgenden Abbildung zeigt das Bild ein anderes Element an, das auf derselben Webseite ausgewählt wurde.  The `$0` bezieht sich nun auf das neu ausgewählte Element, während das zuvor ausgewählte Element zurückgegeben `$1` wird.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="Die $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Der `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a>Abfrageauswahl  

### <a name="console-syntax"></a>Konsolensyntax  

```console
$(selector, [startNode])
```  

Dieser Befehl gibt den Verweis auf das erste DOM-Element mit dem angegebenen CSS-Selektor zurück.  Diese Methode ist ein Alias für die [document.querySelector()-Methode.][MdnDocsWebApiDocumentQueryselector]  

### <a name="console-example"></a>Konsolenbeispiel  

In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element auf der Webseite zurückgegeben.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Der `$('img')`  
:::image-end:::  

Führen Sie die folgenden Aktionen aus, um das erste Element im DOM zu finden oder es auf der Webseite zu finden und anzuzeigen.  

1.  Zeigen Sie auf das zurückgegebene Ergebnis.  
1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Wählen Sie **Einblenden im Elementbereich aus.**  

In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die `src` Eigenschaft wird angezeigt.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Der `$('img').src`  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, , der ein Element oder einen Knoten angibt, von dem aus `startNode` nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

In der folgenden Abbildung wird das erste Element, nachdem das Element gefunden wurde, und die Eigenschaft des `img` `title--image` Elements `src` `img` zurückgegeben.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Der `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet, wird die Funktionalität überschrieben und entspricht der Implementierung `$` `$` aus dieser Bibliothek.  

---  

## <a name="query-selector-all"></a>Abfrageauswahl alle  

### <a name="console-syntax"></a>Konsolensyntax  

```console
$$(selector, [startNode])
```  

Dieser Befehl gibt ein Array von Elementen zurück, die mit dem angegebenen CSS-Selektor übereinstimmen.  Diese Methode entspricht dem Ausführen der [document.querySelectorAll()-Methode.][MdnDocsWebApiDocumentQueryselectorall]  

### <a name="console-example"></a>Konsolenbeispiel  

Verwenden Sie im folgenden Codebeispiel und der folgenden Abbildung, um ein Array aller Elemente auf der aktuellen Webseite zu erstellen und den Wert der Eigenschaft `$$()` `<img>` für jedes Element `src` anzuzeigen.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Verwenden von $$() zum Auswählen aller Bilder auf der Webseite und Anzeigen der Quellen" lightbox="../media/console-element-selector-image-all.msft.png":::
   Verwenden, `$$()` um alle Bilder auf der Webseite zu wählen und die Quellen anzuzeigen  
:::image-end:::  

Diese Methode unterstützt auch einen zweiten Parameter, , der ein Element oder einen Knoten angibt, von dem aus `startNode` nach Elementen gesucht werden soll.  Der Standardwert des Parameters ist `document` .  

Im folgenden Codebeispiel und der folgenden Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der abbildung verwendet, um ein Array aller Elemente zu erstellen, die auf der aktuellen Webseite nach dem ausgewählten `$$()` `<img>` Knoten angezeigt werden.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Verwenden von $$(), um alle Bilder zu wählen, die nach dem angegebenen <div->-Element auf der Webseite angezeigt werden, und die Quellen anzuzeigen" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Verwenden, um alle Bilder zu wählen, die nach dem angegebenen Element auf der Webseite angezeigt `$$()` `<div>` werden, und die Quellen anzuzeigen  
:::image-end:::  

> [!NOTE]
> Wählen `Shift` + `Enter` Sie in **der Konsole** aus, um eine neue Zeile zu starten, ohne das Skript auszuführen.  

---  

## <a name="xpath"></a>XPath  

### <a name="console-syntax"></a>Konsolensyntax  

```console
$x(path, [startNode])
```  

Dieser Befehl gibt ein Array von DOM-Elementen zurück, die mit dem angegebenen XPath-Ausdruck übereinstimmen.  

### <a name="console-example"></a>Konsolenbeispiel  

Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente auf der Webseite `<p>` zurückgegeben.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Verwenden eines XPath-Selektors" lightbox="../media/console-array-xpath.msft.png":::
   Verwenden eines XPath-Selektors  
:::image-end:::  

Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente zurückgegeben, die Elemente `<p>` `<a>` enthalten.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Verwenden eines komplizierteren XPath-Selektors" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Verwenden eines komplizierteren XPath-Selektors  
:::image-end:::  

Ähnlich wie die anderen Selektorbefehle hat einen optionalen zweiten Parameter, der ein Element oder einen Knoten angibt, von dem aus `$x(path)` nach Elementen gesucht werden `startNode` soll.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Verwenden eines XPath-Selektors mit startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Verwenden eines XPath-Selektors mit `startNode`  
:::image-end:::  

---  

## <a name="clear"></a>clear  

### <a name="console-syntax"></a>Konsolensyntax  

```console
clear()
```  

Mit diesem Kommmnad wird die Konsole des Verlaufs geräumt.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
clear()
```  

## <a name="copy"></a>copy  

### <a name="console-syntax"></a>Konsolensyntax  

```console
copy(object)
```  

Diese Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
copy($0)
```  

---  

## <a name="debug"></a>debuggen  

### <a name="console-syntax"></a>Konsolensyntax  

```console
debug(method)
```  

>[!NOTE]
> Das [Chromium Problem #1050237][CR1050237] ist die Nachverfolgung eines Fehlers mit der `debug()` Funktion.  Wenn das Problem auftreten sollte, versuchen Sie stattdessen, [Haltepunkte zu][DevtoolsJavascriptBreakpoints] verwenden.  

Wenn Sie die angegebene Methode anfordern, ruft der Debugger die Methode im Tool Sources auf und bricht **sie** auf.  Sie können den Code schrittweise ausführen und debuggen.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Durchbrechen einer Methode mit debug()" lightbox="../media/console-debug-text.msft.png":::
   Durchbrechen einer Methode mit `debug()`  
:::image-end:::  

Verwenden Sie diese Methode, um die Unterbrechung der Methode zu beenden, oder verwenden Sie `undebug(method)` die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.  

Weitere Informationen zu Haltepunkten finden Sie unter [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].  

---  

## <a name="dir"></a>dir  

### <a name="console-syntax"></a>Konsolensyntax  

```console
dir(object)
```  

Dieser Befehl zeigt eine Objektformatliste aller Eigenschaften für das angegebene Objekt an.  Diese Methode ist ein Alias für die [console.dir()-Methode.][MdnDocsWebApiConsoleDir]  

Werten `document.head` Sie in der Konsole **aus,** um den HTML-Code zwischen den tags `<head>` und zu `</head>` anzeigen.  

### <a name="console-example"></a>Konsolenbeispiel  

Im folgenden Codebeispiel und der folgenden Abbildung wird nach verwendung in der Konsole ein Objektstileintrag `console.dir()` **angezeigt.**  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Protokollierung von document.head mit dir()-Methode" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Protokollierung `document.head` mit `dir()` Methode  
:::image-end:::  

Weitere Informationen finden Sie unter [console.dir()][DevToolsConsoleApiConsoleDirObject] in der Konsolen-API.  

---  

## <a name="dirxml"></a>dirxml  

### <a name="console-syntax"></a>Konsolensyntax  

```console
dirxml(object)
```  

Dieser Befehl druckt eine XML-Darstellung des angegebenen Objekts, wie im **Elementtool** angezeigt.  Diese Methode entspricht der [console.dirxml()-Methode.][MdnDocsWebApiConsoleDirxml]  

---  

## <a name="inspect"></a>inspect  

### <a name="console-syntax"></a>Konsolensyntax  

```console
inspect(object/method)
```  

Dieser Befehl wird geöffnet und wählt das angegebene Element oder Objekt im entsprechenden Bereich aus: entweder das **Elementtool** für DOM-Elemente oder das **Speichertool** für JavaScript-Heapobjekte.  

### <a name="console-example"></a>Konsolenbeispiel  

Im folgenden Codebeispiel und der folgenden Abbildung wird `document.body` das im **Elementtool** geöffnet.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Überprüfen eines Elements mit inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Überprüfen eines Elements mit `inspect()`  
:::image-end:::  

Beim Übergeben einer Zu überprüfenden Methode öffnet die Methode die Webseite im **Tool Sources,** damit Sie diese überprüfen können.  

---  

## <a name="geteventlisteners"></a>getEventListeners  

### <a name="console-syntax"></a>Konsolensyntax  

```console
getEventListeners(object)
```  

Dieser Befehl gibt die Ereignislistener zurück, die für das angegebene Objekt registriert sind.  Der Rückgabewert ist ein Objekt, das ein Array für jeden registrierten Ereignistyp \(z. B. `click` oder `keydown` \) enthält.  Die Member der einzelnen Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.  

### <a name="console-example"></a>Konsolenbeispiel  

Im folgenden Codeausschnitt und der folgenden Abbildung werden alle ereignislistener aufgeführt, die für das Objekt `document` registriert sind.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Ausgabe der Verwendung von getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Das Ergebnis der Verwendung `getEventListeners(document)`  
:::image-end:::  

Wenn mehrere Listener für das angegebene Objekt registriert sind, enthält das Array ein Element für jeden Listener.  In der folgenden Abbildung werden zwei Ereignislistener für das `document` Element für das Ereignis `click` registriert.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Mehrere Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Mehrere Listener  
:::image-end:::  

Sie können jedes der folgenden Objekte weiter erweitern, um die Eigenschaften zu erkunden.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Erweiterte Ansicht des Listenerobjekts" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Erweiterte Ansicht des Listenerobjekts  
:::image-end:::  

---  

## <a name="keys"></a>Tasten  

### <a name="console-syntax"></a>Konsolensyntax  

```console
keys(object)
```  

Dieser Befehl gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.  Um die zugeordneten Werte derselben Eigenschaften zu erhalten, verwenden Sie `values()` .  

### <a name="console-example"></a>Konsolenbeispiel  

Angenommen, Ihre Anwendung hat das folgende Objekt definiert.  

```console
var player1 = {"name": "Ted", "level": 42}
```  

In den folgenden Codebeispielen und abbildung wird davon ausgegangen, dass das Ergebnis im globalen Namespace \(zur Einfachheit\) definiert wurde, bevor Sie die Konsole `player1` eingeben und in die Konsole `keys(player1)` `values(player1)` eingeben.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Die Befehle keys() und values()" lightbox="../media/console-keys-values.msft.png":::
   Die `keys()` Befehle und `values()`  
:::image-end:::  

---  

## <a name="monitor"></a>Monitor  

### <a name="console-syntax"></a>Konsolensyntax  

```console
monitor(method)
```  

Mit diesem Befehl wird eine Meldung an die Konsole protokolliert, die den Methodennamen zusammen mit den Argumenten an die -Methode als Teil einer Anforderung angibt.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Die monitor()-Methode" lightbox="../media/console-function-monitor-sum.msft.png":::
   Die `monitor()` Methode  
:::image-end:::  

Verwenden `unmonitor(method)` Sie, um die Überwachung zu beenden.  

---  

## <a name="monitorevents"></a>monitorEvents  

### <a name="console-syntax"></a>Konsolensyntax  

```console
monitorEvents(object[, events])
```  

Wenn eines der angegebenen Ereignisse für das angegebene Objekt auftritt, wird das Ereignisobjekt bei der Konsole protokolliert.  Sie können ein einzelnes zu überwachende Ereignis, ein Array von Ereignissen oder einen der generischen Ereignistypen angeben, die einer vordefinierten Auflistung von Ereignissen zugeordnet sind.  

### <a name="console-example"></a>Konsolenbeispiel  

Überprüfen Sie das folgende Codebeispiel und die folgende Abbildung.  

Im Folgenden werden alle Größenänderungsereignisse des Fensterobjekts überwacht.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Überwachen von Fenstergrößeereignissen" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Überwachen von Fenstergrößeereignissen  
:::image-end:::  

Der folgende Codeausschnitt definiert ein Array, um sowohl ereignisse als `resize` `scroll` auch ereignisse des Window-Objekts zu überwachen.  

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
   Überwachen wichtiger Ereignisse  
:::image-end:::  

---  

## <a name="profile"></a>profile  

### <a name="console-syntax"></a>Konsolensyntax  

```console
profile([name])
```  

Mit diesem Befehl wird eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen gestartet.  Die [profileEnd()-Methode](#profileend) schließt das Profil ab und zeigt die Ergebnisse im **Speichertool** an.  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Konsolenbeispiel  

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

---  

## <a name="profileend"></a>profileEnd  

### <a name="console-syntax"></a>Konsolensyntax  

```console
profileEnd([name])
```  

Dieser Befehl schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speichertool** an.  Sie müssen die [profile()-Methode](#profile) ausführen.  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Konsolenbeispiel  

1.  Führen Sie die [profile()-Methode](#profile) aus, um die Profilerstellung zu starten.  
1.  Führen Sie `profileEnd()` die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool** anzeigen.  
    
    ```console
    profileEnd("My profile")
    ```  

Profile können auch geschachtelt sein.  Im folgenden Codebeispiel und der folgenden Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Das Ergebnis wird als Heap-Momentaufnahme im **Speichertool** angezeigt.  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Gruppieren von Profilen" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Gruppieren von Profilen  
:::image-end:::  

> [!NOTE]
> Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.  

---  

## <a name="queryobjects"></a>queryObjects  

### <a name="console-syntax"></a>Konsolensyntax  

```console
queryObjects(Constructor)
```  

Dieser Befehl gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.  Der Bereich von `queryObjects()` ist der aktuell ausgewählte Laufzeitkontext in der **Konsole**.  

### <a name="console-example"></a>Konsolenbeispiel  

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

### <a name="console-syntax"></a>Konsolensyntax  

```console
table(data[, columns])
```  

Dieser Befehl protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt in mit optionalen Spaltenüberschriften.  

### <a name="console-example"></a>Konsolenbeispiel  

Im folgenden Codebeispiel und der folgenden Abbildung wird eine Liste der Namen angezeigt, die eine Tabelle in der Konsole verwenden.  

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
   Das Ergebnis der `table()` Methode  
:::image-end:::  

---  

## <a name="undebug"></a>undebug  

### <a name="console-syntax"></a>Konsolensyntax  

```console
undebug(method)
```  

Mit diesem Befehl wird das Debuggen der angegebenen Methode beendet. Wenn also die Methode angefordert wird, wird der Debugger nicht mehr aufgerufen.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a>unmonitor  

### <a name="console-syntax"></a>Konsolensyntax  

```console
unmonitor(method)
```  

Mit diesem Befehl wird die Überwachung der angegebenen Methode beendet.  Diese Methode wird in Zusammenarbeit mit der [monitor()-Methode](#monitor) verwendet.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a>unmonitorEvents  

### <a name="console-syntax"></a>Konsolensyntax  

```console
unmonitorEvents(object[, events])
```  

Mit diesem Befehl werden Überwachungsereignisse für das angegebene Objekt und die angegebenen Ereignisse beendet.  

### <a name="console-example"></a>Konsolenbeispiel  

Der folgende Codeausschnitt beendet beispielsweise die Ereignisüberwachung für das Window-Objekt.  

```console
unmonitorEvents(window);
```  

Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.  Der folgende Code startet beispielsweise die Überwachung aller Ereignisse für das aktuell ausgewählte Element und beendet dann Überwachungsereignisse \(möglicherweise, um das Rauschen in der `mouse` Konsolenausgabe `mousemove` zu reduzieren\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a>werte  

### <a name="console-syntax"></a>Konsolensyntax  

```console
values(object)
```  

Dieser Befehl gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.  

### <a name="console-example"></a>Konsolenbeispiel  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir – Konsolen-API-| Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Beschleunigen sie die JavaScript-Laufzeit | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problem 1050237: debug(function) funktioniert nicht | Chromium Fehler"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
