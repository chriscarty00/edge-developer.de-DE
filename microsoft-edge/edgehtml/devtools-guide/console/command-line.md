---
description: Verwenden der Konsolen Befehlszeile für die Interaktion mit einer ausgeführten Seite
title: DevTools-Console-Befehlszeile
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Befehlszeile der Konsole
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d7ea2bef9fa0014e4d61745636a06d508565df91
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233828"
---
# Befehlszeile der Konsole

Verwenden Sie die Befehlszeile der Konsole, um Werte auf einer Seite anzuzeigen und zu ändern, und führen Sie im Handumdrehen Debugcode aus, während Sie alle die Vorteile der automatischen Codevervollständigung in Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) nutzen. 

Geben Sie einfach ein beliebiges gültiges JavaScript an der Eingabeaufforderung ein, und drücken Sie `Enter` zum Ausführen. Verwenden Sie die mehrzeiligen Eingabe `Shift+Enter` , um eine Zeile zu unterbrechen. Verwenden `Up` Sie die `Down` Pfeiltasten, um durch die vorherigen Konsolenbefehle zu navigieren, die Sie während der aktuellen devtools-Sitzung eingegeben haben. Neben dem Standard-JavaScript und der [Konsolen-API](./console-api.md)unterstützt die Konsole auch die folgenden Befehle für:

 - [Auswählen von DOM-Objekten](#dom-selectors)
 - [Überprüfen von Objekteigenschaften](#object-inspection)
 - [Auffinden aller Ereignis-Listener für ein bestimmtes Objekt](#event-listeners)

Das in die Befehlszeile eingegebene Skript wird im [globalen Bereich](/scripting/javascript/advanced/variable-scope-javascript) des aktuell ausgewählten Fensters ausgeführt, es sei denn, die Seite wird an einem Haltepunkt angehalten. Die während der angehenden Seite eingegebenen Konsolenbefehle werden im [lokalen Bereich](/scripting/javascript/advanced/variable-scope-javascript) der aktuellen Funktion innerhalb der Aufrufliste ausgeführt.

Die Konsole hat eine Dropdownliste für den **Ziel** Ausführungskontext direkt oberhalb des Ausgabebereichs der Konsole. Die Standardauswahl ist das Dokument auf oberster Ebene, **_top**. Alle iframes im Dokument oder in ausgeführten Erweiterungen werden auch als Optionen angezeigt, sodass Sie abwechselnd Befehle in diesen Bereichen ausführen können.

## Dom-Auswahlen
Diese Konsolen Auswahl bietet einfache Abkürzungen für den schnellen Zugriff auf Objekte innerhalb des Dom:

### $ (*CSS-Auswahlzeichenfolge*)
Gibt das erste Element innerhalb des Dokuments zurück, das der angegebenen [CSS-Auswahl](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  Zeichenfolge (oder einer durch Trennzeichen getrennten Gruppe von Selektoren) entspricht. Kurzform für [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).

Beispiel: Öffnen Sie die Konsole, und geben `$('#main')` Sie ein, um das DIV-Objekt `id='main'` auf dieser Seite zurückzugeben.

![Beispiel für die Verwendung von "$"-Auswahl](../media/console_cmd_$.png)

### $ $ (*CSS-Auswahlzeichenfolge*)
Gibt ein Array von Elementen innerhalb des Dokuments zurück, die der angegebenen [CSS-Auswahl](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  Zeichenfolge (oder einer durch Trennzeichen getrennten Gruppe von Selektoren) entsprechen. Kurzform für [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).

Beispiel: Öffnen Sie die Konsole, und geben `$$('.container')` Sie ein, um alle div-Objekte `class='container'` auf dieser Seite zurückzugeben.

![Beispiel für die Verwendung von "$ $"-Auswahl](../media/console_cmd_$$.png)

### $0, $1, $2,...
Gibt die letzten Elemente zurück, die im Bereich " [**Elemente**](../elements.md) " ausgewählt sind, wobei `$0` das aktuell ausgewählte Element, `$1` das ausgewählte Element davor usw. ist.

Beispiel: Öffnen Sie devtools auf der Registerkarte **Elemente** , drücken Sie, `CTRL + B` um das Tool **Element auswählen** zu aktivieren, und klicken Sie mit der Maus auf einen Bereich auf dieser Seite. Öffnen Sie nun die Konsole, und geben `$0` Sie ein, um das Element zurückzugeben, auf das Sie gerade geklickt haben.

![Beispiel für die Verwendung der Auswahl "$0"](../media/console_cmd_$0.png)

### $x (*XPath-Ausdruck*)
Gibt ein Array von Elementen zurück, die mit dem angegebenen [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) -Ausdruck übereinstimmen. 

Beispiel: Öffnen Sie die Konsole, und geben `$x('//script[@defer]')` Sie ein, um alle `<script>` Elemente auf dieser Seite zurückzugeben, die ein `defer` Attribut enthalten.

![Beispiel für die Verwendung der Auswahl "$x"](../media/console_cmd_$x.png)

## Objektprüfung

Diese Befehle bieten schnelle Möglichkeiten zum Überprüfen der Eigenschaften eines Objekts. Das angegebene Objekt muss entweder im globalen Namespace oder im aktuellen Bereich des Debuggers definiert sein.

### dir (*Objekt*)
Gibt eine Strukturansicht-Liste der Eigenschaften für das angegebene Objekt zurück.

Beispiel: Öffnen Sie die Konsole, und geben `dir(document)` Sie die Objekteigenschaften für das Dokumentobjekt ein, das diese Seite darstellt.

![Beispiel für die Verwendung der "dir"-Methode](../media/console_cmd_dir.png)

### Keys (*Objekt*)
Gibt ein Array von Eigenschaftennamen zurück, die dem angegebenen Objekt angefügt sind.

Beispiel: Öffnen Sie die Konsole, und geben `keys(window)` Sie einen Wert ein, um alle Eigenschaften zurückzugeben, die für das globale Fensterobjekt definiert sind.

![Beispiel für die Verwendung der "Keys"-Methode](../media/console_cmd_keys.png)

### Werte (*Objekt*)
Gibt ein Array von Eigenschaftswerten zurück, die an das angegebene Objekt angefügt sind.

Beispiel: Öffnen Sie die Konsole, und geben `values(window)` Sie die Werte aller Eigenschaften (Schlüssel) zurück, die für das globale Fensterobjekt definiert sind.

![Beispiel für die Verwendung der "Values"-Methode](../media/console_cmd_values.png)

## Ereignis-Listener

Mit diesem Befehl können Sie die für ein bestimmtes Objekt registrierten Ereignislistener untersuchen. Das angegebene Objekt muss entweder im globalen Namespace oder im aktuellen Bereich des Debuggers definiert sein.

### getEventListeners (*Objekt*)
Gibt ein Objekt zurück, das einen Schlüssel für die einzelnen registrierten Ereignistypen für das angegebene Objekt enthält. Der Wert der einzelnen Schlüssel ist ein Array von Ereignislistener und zugehörigen Informationen. 

Beispiel: Öffnen Sie die Konsole, und geben `getEventListeners(document)` Sie ein, um alle Ereignislistener anzuzeigen, die für das Document-Objekt dieser Seite registriert sind.

![Beispiel für die Verwendung der "getEventListeners"-Methode](../media/console_cmd_getEventListeners.png)
