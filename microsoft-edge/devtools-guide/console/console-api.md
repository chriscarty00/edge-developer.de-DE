---
description: Verwenden der Konsolen-API zum programmgesteuerten Debuggen und profilieren Ihres Codes
title: DevTools-Console-Console-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Konsolen-API
ms.custom: seodec18
ms.openlocfilehash: d722934c3694c3c23e367141158ad45f6d03b175
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568462"
---
# Konsolen-API

Die *Konsolen-API* bietet Befehlszeilen-und programmgesteuerten Zugriff auf die devtools-Konsole über das globale `console` Objekt, sodass Sie:

 - [Protokollieren von benutzerdefinierten Nachrichten](#logging-custom-messages) von Ihrem Code
 - Über [Prüfen von Objekten und Elementen](#inspecting-objects-and-elements) und Protokollieren der zugehörigen Informationen
 - [Testen und Messen Ihres Codes](#testing-and-measuring) durch Festlegen von Assertionen, Timer und Leistungsindikatoren
 - Erstellen [Sie Schnappschüsse des Heaps](#taking-heap-snapshots) , um den Speicherverbrauch Ihres ausgeführten Codes zu bewerten und Speicherverluste zu identifizieren.
 - [Verfolgen Sie Ihre callstacks](#tracing-callstacks) , um zu verstehen, woher Ihr Code aufgerufen wird. 
 - [Organisieren der Protokollausgabe](#organizing-log-output) , um das Debuggen zu rationalisieren

Im folgenden finden Sie die Befehle und Formatierungsparameter, die von Microsoft Edge zurzeit unterstützt werden. Sie funktionieren ähnlich wie bei wichtigen Browsern.

## Protokollieren benutzerdefinierter Nachrichten

Ihr Code kann verschiedene Typen von benutzerdefinierten Nachrichten an die Konsole senden, einschließlich:

Nachrichtentyp  | &nbsp;   |
:------------------- | :------ |
[**Error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) und [ **Exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)| Kritische Fehler und Fehler
[**Warnung ()**](https://developer.mozilla.org/docs/Web/API/Console/warn) | Mögliche Fehler oder unerwartetes Verhalten 
[**Info ()**](https://developer.mozilla.org/docs/Web/API/Console/info) | Nützliche, aber nicht kritische Informationen
[**Log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) und [ **Debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log) | Allgemeines Debuggen (ohne ein System Warnungssymbol in der Konsole zu generieren)

   
Sie können diese zusammen mit den anderen Nachrichten, die von Microsoft Edge generiert wurden, aus dem Konsolenbereich gruppieren und filtern. Alle benutzerdefinierten Nachrichten Methoden erfordern einen Zeichenfolgenparameter (Message) und optionale Format Ersetzungsparameter. Microsoft Edge unterstützt die folgenden Formatierungsoptionen:

Format-Parameter | &nbsp;
:------------------- | :--- |
**% b** | Binär
**% c** | Inline-CSS-Formatvorlage (siehe Beispiel unten)
**% d**, **% i** | Ganze Zahl 
**% f** | Gleitkomma  
**% s** | Zeichenfolge 
**% x** | Hexadezimal 
**% e** | Exponent 

So können Sie beispielsweise Zeichenfolgen-und ganzzahlige Variablen in Ihre Protokollmeldung einbeziehen:

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

Und so können Sie einer Protokollnachricht mit Inline-CSS () einen grünen Hervorhebungseffekt hinzufügen `%c` :

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Konsolenprotokoll mit Inlineformatvorlagen](../media/console_api_css.png)

## Untersuchen von Objekten und Elementen

Überprüfbare Objekte werden in der Konsole in einer reduzierten Strukturansicht mit erweiterbaren Knoten angezeigt. Die Konsole erkennt, ob Sie einen DOM-Knoten (wie ein div) oder ein JavaScript-Objekt (wie ein Ereignis) senden, und zeigt diese automatisch als erkannten Typ an.

Sie können auch eine bestimmte Ausgabe erzwingen:

Befehl | &nbsp;
:------------------- | :--- |
[**dir ()**](https://developer.mozilla.org/docs/Web/API/Console/dir) | Wird als über JavaScript-Objekt angezeigt
[**DirXML ()**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | Anzeige als über DOM-Knoten

Versuchen Sie beispielsweise, die Konsole zu öffnen und die folgenden Ausgaben für das `<div id='main'>` Element auf dieser Seite zu vergleichen:

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Vergleich der Ausgabe "dir" versus "DirXML"](../media/console_api_dir.png)

### Auswählen eines **Elements im Element Panel**

Sie können ein Element innerhalb des HTML-Struktur Kontexts der Seite direkt aus der Konsole für das sofortige Layout und das Debuggen von Stilen auswählen.

Befehl | &nbsp;
:------------------- | :--- |
**Select ()** | Wechselt zum Element **Panel und legt den Fokus** auf das angegebene Element fest.

Wenn Sie beispielsweise die Konsole auf dieser Seite öffnen, geben Sie Folgendes ein:

```javascript
console.select(document.querySelector("body"));
```

Der devtools wechselt zum **Element Panel (** sofern es nicht bereits der aktuelle ist) und legt den Fokus in der [*HTML-Strukturansicht*](../elements.md#html-tree-view) auf das angegebene Element fest.

![Beispiel für die "Select"-Methode](../media/console_api_select.png)

## Testen und Messen

### Testen des Codes

Fügen Sie dem Code Konsolen-API-Test Assertionen hinzu, um Komponententests durchführen und den Code während der Ausführung im Browser Debuggen zu können.

Befehl | &nbsp;
:------------ | :-------------
[**Assert ()**](https://developer.mozilla.org/docs/Web/API/Console/assert) | Protokolliert eine Fehlermeldung einer Konsole, wenn der bereitgestellte Ausdruck *false*ergibt.

Zusätzlich zum logischen Ausdruck, den Sie als testbare Assertion angeben, können Sie eine optionale Nachricht und Formatierungsparameter hinzufügen, wie Sie dies für andere [benutzerdefinierte Konsolen Nachrichten](#logging-custom-messages)verwenden würden. Beispiel:

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Beispiel für die "Assert"-Methode](../media/console_api_assert.png)

### Zählen von Ausführungen im Code

Sie können Indikatoren in Ihrem Code so einstellen, dass Sie nachverfolgen, wie oft der umgebende Code ausgeführt wird. Durch das Festlegen von Indikatoren können Sie sicherstellen, dass Ihr Code wie erwartet ausgeführt wird, und Sie bei der Diagnose von Leistungsengpässen unterstützen.

Befehl | &nbsp;
:------------ | :-------------
[**Anzahl ()**](https://developer.mozilla.org/docs/Web/API/Console/count) | Inkrementiert und protokolliert die Anzahl der Male, die *count ()* für die angegebene Bezeichnung ausgeführt wurde.
[**countReset()**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | Setzt die Anzahl für die angegebene Indikator Beschriftung auf NULL zurück.

So können Sie beispielsweise die folgenden Zeilen in der Konsole ausführen:

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 . . . führt zu:
> Mein Counter: 1

### Timing Ihres Codes

Instrumentieren Sie Ihren Code mit beschrifteten Timern, um zu messen, wie lange es dauert, einen bestimmten Vorgang abzuschließen.

Befehl | &nbsp;
:------------ | :-------------
[**Zeit ()**](https://developer.mozilla.org/docs/Web/API/Console/time) | Startet einen Zeitgeber mit der angegebenen Bezeichnung.
[**timeEnd()**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | Beendet den Zeitgeber mit der angegebenen Bezeichnung und meldet die verstrichene Zeit (in Millisekunden).
[**Timestamp ()**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | Meldet die aktuelle Systemzeit (in Millisekunden).

Versuchen Sie beispielsweise, die folgenden Zeilen in der Konsole auszuführen:

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### Erstellen von Heap-Schnappschüssen

Erstellen Sie Schnappschüsse des Heaps, um den Speicherverbrauch Ihres ausgeführten Codes zu bewerten und Speicherverluste zu identifizieren.

Befehl | &nbsp;
:------------ | :-------------
**takeHeapSnapshot()** | Zeichnet Details über den aktuellen JavaScript-Heap und die zugeordneten Objekte auf.

Der devtools- [Speicher Profiler](../memory.md#toolbar) muss ausgeführt werden, um Heap-Schnappschüsse aufnehmen zu können. Jeder Schnappschuss wird in der [*Zusammenfassung*](../memory.md#snapshot-summary) des [**Speicher**](../memory.md) Bereichs zur weiteren Überprüfung als Kachel angezeigt.

## Ablauf Verfolgungs callstacks

Verstehen, woher der Code aufgerufen wird, welcher Code ausgeführt wird und wie lange die Ausführung dauert, kann hilfreich sein, um Langsamkeit oder unerwartetes Verhalten zu analysieren. Eine Stapelüberwachung zeigt Ihnen den Ausführungspfad, den Ihr Code zum Erreichen des Codes benötigte, von der Ablaufverfolgungsanforderung aufwärts durch den Pfad. 

Befehl | &nbsp;
:------------ | :-------------
[**Trace ()**](https://developer.mozilla.org/docs/Web/API/Console/trace) | Gibt eine Ablaufverfolgung der aktuellen Skript Ausführungs callstack aus.

Führen Sie beispielsweise den folgenden Code in der Konsole aus:

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

. . . Gibt die folgenden Stapelablaufverfolgungen aus:
> Console. Trace () bei c (eval Code: 8:3) at a (eval Code: 2:3) at eval Code (eval Code: 14:1)
> 
> Console. Trace () bei c (eval Code: 8:3) at b (eval Code: 5:3) at d (eval Code: 11:3) at eval Code (eval Code: 15:1)

## Organisieren der Protokollausgabe

Um die gesamte vorherige Konsolenausgabe einfach zu löschen, verwenden Sie *Console. Clear ()* (oder `CTRL + L` ). Dadurch wird der BackStack des befehlsverlaufs der Konsole nicht gelöscht (Sie können ihn weiterhin mit der nach-oben-und nach-unten-Taste durchlaufen).

Befehl | &nbsp;
:------------ | :-------------
[**Clear ()**](https://developer.mozilla.org/docs/Web/API/Console/clear) | Löscht alle vorherigen Konsolenausgaben.

Wenn Ihr Code viele Konsolen Nachrichten ausgibt, können Sie ihn mit den folgenden Befehlen visuell in geschachtelte Blöcke organisieren:

 Befehl | &nbsp;
:------------ | :-------------
[**Group ()**](https://developer.mozilla.org/docs/Web/API/Console/group) | Startet eine neue Schachtelungsebene für die Konsolenausgabe mit der angegebenen (optionalen) Beschriftung.
[**groupCollapsed()**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | Startet eine neue Schachtelungsebene für die Konsolenausgabe mit der angegebenen (optionalen) Bezeichnung, das Gruppierungssteuerelement wird jedoch standardmäßig reduziert und muss erweitert werden (durch Klicken auf das Pfeil-Steuerelement), um die untergeordnete Ausgabe anzuzeigen.
[**groupEnd()**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | Beendet die Schachtelungs Gruppe für die angegebene Beschriftung.

Versuchen Sie beispielsweise, die folgenden Befehle in der Konsole einzugeben:

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

. . . und erweitern Sie dann die Steuerelemente *Gruppe 1* und *Gruppe 1,1* , um zu sehen, wie die Protokoll Kommentare geschachtelt sind:

![Gruppieren von Nachrichten in der Konsole](../media/console_api_group.png)

Manchmal ist es einfacher, ein JavaScript-Objekt oder-Array in tabellarischer Form zu visualisieren, anstatt eine flache Liste zu erstellen. Dazu können Sie den Befehl *Console. Table ()* verwenden:

Befehl | &nbsp;
:------------ | :-------------
[**Tabelle ()**](https://developer.mozilla.org/docs/Web/API/Console/table) | Gibt das angegebene Array oder Objekt in tabellarischer Form an die Konsole aus.

Beispielsweise das folgende Object-Array:

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

. . . wird als Tabelle in der Konsole gerendert:

![Anzeigen eines Objektarrays als Tabelle in der Konsole](../media/console_api_table.png)
