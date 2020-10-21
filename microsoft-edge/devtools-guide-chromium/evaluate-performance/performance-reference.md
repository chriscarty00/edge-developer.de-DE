---
description: Im Modus Zeitachsenereignisse werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsen-Ereignisverweis, um mehr über die einzelnen Zeitachse-Ereignistypen zu erfahren.
title: Ereignisreferenz der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 989d4d84345fedc1c5aef2cb8d893db3c0e1634b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124901"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Ereignisreferenz der Zeitachse  

Im Modus Zeitachsenereignisse werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsen-Ereignisverweis, um mehr über die einzelnen Zeitachse-Ereignistypen zu erfahren.  

## Allgemeine zeitachsenereignis Eigenschaften  

Bestimmte Details sind in Ereignissen aller Typen vorhanden, während einige nur für bestimmte Ereignistypen gelten.  In diesem Abschnitt werden Eigenschaften aufgelistet, die für unterschiedliche Ereignistypen üblich sind.  Eigenschaften, die für bestimmte Ereignistypen spezifisch sind, werden in den verweisen für die folgenden Ereignistypen aufgeführt.  

| Eigenschaft | Wann wird angezeigt |  
|:--- |:--- |  
| Aggregierte Zeit | Für Ereignisse mit **geschachtelten Ereignissen**die Zeit, die für jede Kategorie von Ereignissen übernommen wurde. |  
| Aufrufliste | Für Ereignisse mit **untergeordneten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird. |  
| CPU-Zeit | Wie viel CPU-Zeit das aufgezeichnete Ereignis beansprucht hat. |  
| Details | Weitere Details zum Ereignis. |  
| Dauer \ (zum Zeitstempel \) | Wie lange das Ereignis dauerte, bis alle untergeordneten Elemente abgeschlossen waren; timestamp ist der Zeitpunkt, zu dem das Ereignis aufgetreten ist, relativ zu dem Zeitpunkt, zu dem die Aufzeichnung gestartet wurde. |  
| Selbst Zeit | Die Dauer des Ereignisses ohne untergeordnete Elemente. |  
| Verwendete Heapgröße | Die Menge des Arbeitsspeichers, der von der Anwendung beim Aufzeichnen des Ereignisses verwendet wird, und die Änderung der verwendeten Heapgröße seit dem letzten Sampling in Delta \ (+/-\). |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## Laden von Ereignissen  

In diesem Abschnitt werden Ereignisse aufgelistet, die zu Lade Kategorie und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| HTML analysieren |  Microsoft Edge hat den HTML-Analyse Algorithmus ausgeführt. |  
| Fertig stellen des Ladens |  Eine Netzwerkanforderung wurde abgeschlossen. |  
| Empfangen von Daten |  Die Daten für eine Anforderung wurden empfangen.  Es gibt mindestens ein Receive-Datenereignis. |  
| Antwort empfangen |  Die anfängliche HTTP-Antwort einer Anforderung. |  
| Anfrage senden |  Eine Netzwerkanforderung wurde gesendet. |  

### Laden von Ereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Ressource | Die URL der angeforderten Ressource. |  
| Preview | Vorschau der angeforderten Ressource \ (nur Bilder \). |  
| Request-Methode | Die für die Anforderung verwendete HTTP-Methode \ ( `GET` oder Beispiels `POST` Weise \). |  
| Status Code | HTTP-Antwortcode. |  
| MIME-Typ | Der MIME-Typ der angeforderten Ressource. |  
| Codierte Datenlänge | Die Länge der angeforderten Ressource in Bytes. |  

## Skripting-Ereignisse  

In diesem Abschnitt werden Ereignisse aufgelistet, die zu der Kategorie Skripting gehören, und deren Eigenschaften.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Animations Frame gebrannt | Ein geplanter Animationsframe wird ausgelöst, und der zugehörige Rückrufhandler wird aufgerufen. |  
| Animations Frame Abbrechen |  Ein geplanter Animationsframe wurde abgebrochen. |  
| GC-Ereignis |  Garbage Collection ist aufgetreten. |  
| DOMContentLoaded |  Das [DOMContentLoaded-Ereignis][MDNWindowDOMContentLoadedEvent] wurde vom Browser ausgelöst.  Dieses Ereignis wird ausgelöst, wenn der gesamte Dom-Inhalt der Seite geladen und analysiert wurde. |  
| Auswerten des Skripts | Ein Skript wurde ausgewertet. |  
| Ereignis | Ein JavaScript-Ereignis \ (Beispiel: `mousedown` oder `key` \). |  
| Funktionsaufruf | Es wurde ein JavaScript-Funktionsaufruf der obersten Ebene durchgeführt \ (wird nur angezeigt, wenn der Browser JavaScript-Modul wechselt). |  
| Timer installieren | Ein Zeitgeber wurde mit [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] oder [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]erstellt. |  
| Animationsrahmen anfordern | Ein `requestAnimationFrame()` Anruf hat einen neuen Frame geplant. |  
| Timer entfernen | Ein zuvor erstellter Zeitgeber wurde gelöscht. |  
| Zeit |  Ein Skript mit dem Namen [Console. time ()][ConsoleApiTime]. |  
| Endzeit | Ein Skript mit dem Namen [Console. timeEnd ()][ConsoleApiTimeEnd]. |  
| Timer ausgelöst | Ein Timer, der mit oder geplant `setInterval()` wurde `setTimeout()` . |  
| XMLHttpRequest Ready-Statusänderung | Der Zustand "Ready" eines XMLHttpRequest wurde geändert. |  
| XMLHttpRequest Load | Ein `XMLHTTPRequest` beendeten Ladevorgang. |  

### Skripting-Ereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Timer-ID | Die Timer-ID. |  
| Timeout | Das vom Zeitgeber angegebene Timeout. |  
| Wiederholt | Boolescher Wert, der angibt, ob der Zeitgeber wiederholt wird. |  
| Funktionsaufruf | Eine Funktion, die aufgerufen wurde. |  

## Rendern von Ereignissen  

In diesem Abschnitt werden Ereignisse aufgelistet, die zu einer Rendering-Kategorie und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Ungültiges Layout | Das Seitenlayout wurde durch eine DOM-Änderung ungültig. |  
| Layout | Ein Seitenlayout wurde abgeschlossen. |  
| Neuberechnen des Formats | Neu berechnete Microsoft Edge-Element Formatvorlagen |  
| Scroll | Der Inhalt der geschachtelten Ansicht wurde gescrollt. |  

### Rendern von Ereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Layout ungültig | Bei Layout-Datensätzen ist die Stapelüberwachung des Codes, der das Layout verursacht hat, ungültig. |  
| Knoten, die Layout benötigen | Bei Layout-Datensätzen wird die Anzahl der Knoten, die vor dem Neulayout als Layout erforderlich markiert wurden, gestartet.  In der Regel handelt es sich um die Knoten, die vom Entwickler Code für ungültig erklärt wurden, sowie einen Pfad aufwärts zum Neulayout-Stamm. |  
| Layout-Strukturgröße | Bei Layout-Datensätzen die Gesamtzahl der Knoten unter dem umlayout-Stamm \ (der Knoten, mit dem Microsoft Edge das Neulayout startet \). |  
| Bereich ' Layout ' | Mögliche Werte sind `Partial` \ (die Umgrenzung des Re-Layouts ist ein Teil des DOM \) oder `Whole document` . |  
| Betroffene Elemente | Zum Neuberechnen von Formatvorlagen Datensätzen die Anzahl der Elemente, die von einer Neuberechnung des Formats betroffen sind. |  
| Formatvorlagen ungültig | Zum Neuberechnen von Formatvorlagen Datensätzen wird die Stapelüberwachung des Codes bereitgestellt, der die Formatvorlage ungültig wurde. |  

## Malen von Ereignissen  

In diesem Abschnitt werden Ereignisse aufgelistet, die zur Kategorie "Malerei" und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Composite-Layer | Die zusammengesetzten Bildebenen für das Microsoft-Edge-Rendering-Modul |  
| Bild decodieren | Eine Bildressource wurde dekodiert. |  
| Bildgröße | Die Größe eines Bilds wurde aus den systemeigenen Dimensionen geändert. |  
| Paint | Zusammengesetzte Ebenen wurden in einen Bereich der Anzeige gemalt.  Wenn Sie den Mauszeiger über einen Paint-Eintrag bewegen, wird der Bereich der Anzeige, der aktualisiert wurde, hervorgehoben. |  

### Zeichnen von Ereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Pfad | Für Paint-Ereignisse die x-und y-Koordinaten des Paint-Rechtecks. |  
| Dimensionen | Für Paint-Ereignisse die Höhe und Breite des bemalten Bereichs. |  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referenz zur Zeit Konsolen-API"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-API-Referenz"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenster: DOMContentLoaded-Ereignis | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Flavio Copes][FlavioCopes] \ (vollständiger Stack-Entwickler \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
