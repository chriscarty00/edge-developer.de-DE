---
description: Im Zeitachsenereignissemodus werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsenereignisverweis, um mehr über jeden Zeitachsenereignistyp zu erfahren.
title: Zeitachsenereignisreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b8a15dd3503a891698d1f96bdc99946163d738ff
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564210"
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
# <a name="timeline-event-reference"></a>Zeitachsenereignisreferenz  

Im Zeitachsenereignissemodus werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsenereignisverweis, um mehr über jeden Zeitachsenereignistyp zu erfahren.  

## <a name="common-timeline-event-properties"></a>Allgemeine Eigenschaften des Zeitachsenereigniss  

Bestimmte Details sind in Ereignissen aller Typen vorhanden, während einige nur für bestimmte Ereignistypen gelten.  In diesem Abschnitt werden Eigenschaften aufgeführt, die unterschiedlichen Ereignistypen gemeinsam sind.  Eigenschaften, die für bestimmte Ereignistypen spezifisch sind, werden in den Verweisen für die folgenden Ereignistypen aufgeführt.  

| Eigenschaft | Wann wird sie angezeigt? |  
|:--- |:--- |  
| Aggregierte Zeit | Bei Ereignissen mit **geschachtelten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird. |  
| Aufrufliste | Für Ereignisse mit **untergeordneten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird. |  
| CPU-Zeit | Wie viel CPU-Zeit das aufgezeichnete Ereignis in Anspruch nahm. |  
| Details | Weitere Details zum Ereignis. |  
| Duration \(at time-stamp\) | Wie lange es ge dauern hat, bis das Ereignis mit allen seinen kindern abgeschlossen wurde; zeitstempel ist der Zeitpunkt, zu dem das Ereignis aufgetreten ist, relativ zum Zeitpunkt des Beginns der Aufzeichnung. |  
| Self time | Die Dauer des Ereignisses ohne seine kinder. |  
| Verwendete Heapgröße | Der von der Anwendung beim Aufzeichnen des Ereignisses verwendete Arbeitsspeicher, und die delta \(+/-\)-Änderung in der verwendeten Heapgröße seit dem letzten Sampling. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a>Laden von Ereignissen  

In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie Laden und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Analysieren von HTML |  Microsoft Edge den HTML-Analysealgorithmus. |  
| Beenden des Ladens |  Eine Netzwerkanforderung wurde abgeschlossen. |  
| Empfangsdaten |  Daten für eine Anforderung wurden empfangen.  Es gibt mindestens ein Receive Data-Ereignis. |  
| Antwort empfangen |  Die anfängliche HTTP-Antwort einer Anforderung. |  
| Sendeanforderung |  Eine Netzwerkanforderung wurde gesendet. |  

### <a name="loading-event-properties"></a>Laden von Ereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Ressource | Die URL der angeforderten Ressource. |  
| Preview | Vorschau der angeforderten Ressource \(nur Bilder\). |  
| Request-Methode | DIE HTTP-Methode, die für die Anforderung \( `GET` oder `POST` , z. B. \) verwendet wird. |  
| Statuscode | HTTP-Antwortcode. |  
| MIME-Typ | MIME-Typ der angeforderten Ressource. |  
| Codierte Datenlänge | Länge der angeforderten Ressource in Bytes. |  

## <a name="scripting-events"></a>Skriptingereignisse  

In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie "Scripting" und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Animationsframe ausgelöst | Ein geplanter Animationsframe wurde ausgelöst, und der Rückrufhandler wird aufgerufen. |  
| Abbrechen des Animationsframes |  Ein geplanter Animationsframe wurde abgebrochen. |  
| GC-Ereignis |  Die Garbage Collection ist aufgetreten. |  
| DOMContentLoaded |  Das [DOMContentLoaded-Ereignis][MDNWindowDOMContentLoadedEvent] wurde vom Browser ausgelöst.  Dieses Ereignis wird ausgelöst, wenn der ganze DOM-Inhalt der Seite geladen und analysiert wird. |  
| Auswerten des Skripts | Ein Skript wurde ausgewertet. |  
| Ereignis | Ein JavaScript-Ereignis \(z. B. `mousedown` , oder `key` \). |  
| Funktionsaufruf | Ein JavaScript-Funktionsaufruf auf oberster Ebene wurde vorgenommen \(wird nur angezeigt, wenn der Browser das JavaScript-Modul aufruft\). |  
| Installieren des Timers | Ein Timer wurde mit [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] oder [setTimeout() erstellt.][MDNWindowOrWorkerGlobalScopeSetTimeout] |  
| Animationsframe anfordern | Ein `requestAnimationFrame()` Anruf hat einen neuen Frame geplant. |  
| Timer entfernen | Ein zuvor erstellter Zeitgeber wurde geräumt. |  
| Zeit |  Ein Skript mit dem Namen [console.time()][ConsoleApiTime]. |  
| Zeitende | Ein Skript mit dem Namen [console.timeEnd()][ConsoleApiTimeEnd]. |  
| Timer Fired | Ein timer fired that was scheduled with `setInterval()` or `setTimeout()` . |  
| XHR Ready State Change | Der Bereitzustand einer XMLHTTPRequest wurde geändert. |  
| XHR Load | Ein `XMLHTTPRequest` fertiges Laden. |  

### <a name="scripting-event-properties"></a>Eigenschaften des Skriptereigniss  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Zeitgeber-ID | Die Zeitgeber-ID. |  
| Timeout | Das vom Timer angegebene Timeout. |  
| Wiederholungen | Boolean, der angibt, ob der Timer wiederholt wird. |  
| Funktionsaufruf | Eine Funktion, die aufgerufen wurde. |  

## <a name="rendering-events"></a>Renderingereignisse  

In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie Rendering und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Ungültiges Layout | Das Seitenlayout wurde durch eine DOM-Änderung ungültig. |  
| Layout | Ein Seitenlayout wurde abgeschlossen. |  
| Formatvorlage neu berechnen | Microsoft Edge neu berechneten Elementformatvorlagen. |  
| Scroll | Der Inhalt der geschachtelten Ansicht wurde geschachtelt. |  

### <a name="rendering-event-properties"></a>Renderingereigniseigenschaften  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Layout ungültig | Bei Layoutdatensätzen die Stapelverfolgung des Codes, der dazu führte, dass das Layout ungültig wurde. |  
| Knoten, die Layout benötigen | Für Layoutdatensätze die Anzahl der Knoten, die vor dem Neulayout als layout erforderlich gekennzeichnet wurden.  Dies sind normalerweise die Knoten, die durch Entwicklercode ungültig wurden, sowie ein Pfad nach oben zum Neulayout des Stamms. |  
| Layoutstrukturgröße | Für Layoutdatensätze die Gesamtanzahl der Knoten unter dem Neulayoutstamm \(der Knoten, der Microsoft Edge neulayout\ startet). |  
| Layoutbereich | Mögliche Werte sind `Partial` \(die Neulayoutgrenze ist ein Teil des DOM\) oder `Whole document` . |  
| Betroffene Elemente | Bei Neuberechnung von Formatvorlagedatensätzen die Anzahl der Elemente, die von einer Formatvorlage neu berechnet werden. |  
| Formatvorlagen ungültig | Stellt für Die Neuberechnung von Formatvorlagedatensätzen die Stapelverfolgung des Codes zur Ursache der Format ungültigen Formatvorlage. |  

## <a name="painting-events"></a>Malereignisse  

In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie "Malen" und deren Eigenschaften gehören.  

| Ereignis | Beschreibung |  
|:--- |:--- |  
| Zusammengesetzte Ebenen | Die zusammengesetzten Bildebenen für das Microsoft Edge Rendermodul. |  
| Bilddecode | Eine Bildressource wurde decodiert. |  
| Bildgröße | Die Größe eines Bilds wurde von den systemeigenen Dimensionen angepasst. |  
| Paint | Zusammengesetzte Ebenen wurden in einen Bereich der Anzeige dargestellt.  Wenn Sie auf einen Paint zeigen, wird der Bereich der aktualisierten Anzeige hervorgehoben. |  

### <a name="painting-event-properties"></a>Eigenschaften des Painting-Ereignisses  

| Eigenschaft | Beschreibung |  
|:--- |:--- |  
| Pfad | Für Paint ereignisse die x- und y-Koordinaten des Farbrechtecks. |  
| Dimensionen | Bei Paint die Höhe und Breite des gefärbten Bereich. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time – Konsolen-API-Referenz"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd – Konsolen-API-Referenz"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenster: DOMContentLoaded-Ereignis | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Flavio Copes][FlavioCopes] \(Full Stack Developer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors#flavio-copes  
