---
description: Verwenden Sie die Zuweisungs Instrumentation auf der Zeitachse, um Objekte zu finden, die nicht ordnungsgemäß von der Garbage Collection erfasst werden, und den Speicher weiterhin beizubehalten.
title: Verwenden der Zuordnungs Instrumentation auf der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 58a951c4241ae0fe7dce70f523a701694b8254f9
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993506"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# Verwenden der Zuordnungs Instrumentation auf der Zeitachse  

Verwenden Sie die **Zuweisungs Instrumentation auf der Zeitachse** , um Objekte zu finden, die nicht ordnungsgemäß von der Garbage Collection erfasst werden, und den Speicher weiterhin beizubehalten.  

## Funktionsweise der Zuordnungs Instrumentation auf der Zeitachse  

Die **Zuweisungs Instrumentation auf Zeitachse** kombiniert die detaillierten Schnappschuss Informationen des **Heap-Profilers** mit der inkrementellen Aktualisierung und Nachverfolgung des **Leistungs** Panels.  Ebenso umfasst das Nachverfolgen der Heapzuordnung für Objekte das Starten einer Aufzeichnung, das Durchführen einer Abfolge von Aktionen und das Beenden der Aufzeichnung zur Analyse.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

Die **Zuweisungs Instrumentation auf der Zeitachse** nimmt in regelmäßigen Abständen Heap-Snapshots (so häufig wie alle 50-ms \) und einen letzten Snapshot am Ende der Aufzeichnung an.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Zuordnungs Instrumentation auf Zeitachse" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Zuordnungs Instrumentation auf Zeitachse**  
:::image-end:::  

> [!NOTE]
> Die Zahl nach der `@` ist eine Objekt-ID, die über die verschiedenen Snapshots, die während der Aufzeichnungssitzung aufgenommen wurden, beibehalten wird.  Die persistente Objekt-ID ermöglicht einen präzisen Vergleich zwischen Heap Zuständen.  Objekte werden während Garbage Collections verschoben, daher ist es sinnlos, die Adresse eines Objekts anzuzeigen.  

## Aktivieren der Zuordnungs Instrumentation auf der Zeitachse  

Führen Sie die folgenden Aktionen aus, um die **Zuweisungs Instrumentation auf der Zeitachse**zu verwenden.  

1.  [Öffnen Sie das devtools][DevtoolsOpenIndex].  
1.  Öffnen Sie den Bereich " **Speicher** ", und aktivieren Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** .  
1.  Start recording (Aufzeichnung starten.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Datensatz-Heapzuweisungen Profiler" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Datensatz-Heapzuweisungen Profiler  
    :::image-end:::  
    
## Lesen einer Heap Zuordnungs Zeitachse  

Die Zeitachse der Heapzuweisung zeigt an, wo Objekte erstellt werden, und identifiziert den Beibehaltungs Pfad.  In der folgenden Abbildung geben die Balken am oberen Rand an, wenn neue Objekte im Heap gefunden werden.  

Die Höhe der einzelnen Balken entspricht der Größe der zuletzt zugeordneten Objekte, und die Farbe der Balken gibt an, ob diese Objekte weiterhin im endgültigen Heap-Snapshot enthalten sind.  Blaue Balken zeigen Objekte an, die am Ende der Zeitachse weiterhin aktiv sind, und graue Balken zeigen Objekte an, die während der Zeitachse zugewiesen wurden, die aber seither als Garbage Collection erfasst wurden.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Zuordnungs Instrumentation auf der Zeitachse-Momentaufnahme" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Zuordnungs Instrumentation auf der Zeitachse** -Momentaufnahme  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Sie können die Schieberegler in der obigen Zeitachse verwenden, um den jeweiligen Schnappschuss zu vergrößern und die Objekte anzuzeigen, die kürzlich zu diesem Zeitpunkt zugewiesen wurden:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Vergrößern des Schnappschusses" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Vergrößern des Schnappschusses  
:::image-end:::  

Wenn Sie auf ein bestimmtes Objekt im Heap klicken, wird im unteren Teil des Heap-Snapshots die Beibehaltungs Struktur angezeigt.  Wenn Sie den Beibehaltungs Pfad für das Objekt untersuchen, sollten Sie genügend Informationen erhalten, um zu verstehen, warum das Objekt nicht erfasst wurde, und Sie sollten die erforderlichen Codeänderungen vornehmen, um den unnötigen Verweis zu entfernen.  

## Anzeigen der Speicherzuweisung nach Funktion  

Sie können die Speicherzuweisung nach JavaScript-Funktion anzeigen.  Weitere Informationen finden Sie unter [untersuchen der Speicherzuweisung nach Funktion][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Öffnen Sie Microsoft Edge (Chrom) devtools | Microsoft docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Untersuchen der Speicherzuweisung nach Funktion – beheben von Speicherproblemen | Microsoft docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Herunterladen eines Microsoft Edge-Kanals"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
