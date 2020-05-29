---
title: Verwenden der Zuordnungs Instrumentation auf der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ab7a270e1d599e254aaaf4515b6898cb1d9782fc
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611734"
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

Bei der **Zuweisungs Instrumentation auf der Zeitachse** werden Heap-Snapshots in der gesamten Aufzeichnung (so häufig wie alle 50-ms! \) und ein letzter Snapshot am Ende der Aufzeichnung regelmäßig verwendet.  

> ##### Abbildung1  
> **Zuordnungs Instrumentation auf Zeitachse**  
> ![Zuordnungs Instrumentation auf Zeitachse][ImageObjectTracker]  

> [!NOTE]
> Die Zahl nach der `@` ist eine Objekt-ID, die über die verschiedenen Snapshots, die während der Aufzeichnungssitzung aufgenommen wurden, beibehalten wird.  Die persistente Objekt-ID ermöglicht einen präzisen Vergleich zwischen Heap Zuständen.  Objekte werden während Garbage Collections verschoben, daher ist es sinnlos, die Adresse eines Objekts anzuzeigen.  

## Aktivieren der Zuordnungs Instrumentation auf der Zeitachse  

Führen Sie die folgenden Schritte aus, um die **Zuweisungs Instrumentation auf Zeitachse**zu verwenden.  

1.  [Öffnen Sie das devtools][DevtoolsOpenIndex].  
1.  Öffnen Sie den Bereich " **Speicher** ", und aktivieren Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** .  
1.  Start recording (Aufzeichnung starten.  

> ##### Abbildung2  
> Datensatz-Heapzuweisungen Profiler  
> ![Datensatz-Heapzuweisungen Profiler][ImageRecordHeap]  

## Lesen einer Heap Zuordnungs Zeitachse  

Die Zeitachse der Heapzuweisung zeigt an, wo Objekte erstellt werden, und identifiziert den Beibehaltungs Pfad.  In [Abbildung 3](#figure-3)geben die Balken am oberen Rand an, wenn neue Objekte im Heap gefunden werden.  

Die Höhe der einzelnen Balken entspricht der Größe der zuletzt zugeordneten Objekte, und die Farbe der Balken gibt an, ob diese Objekte weiterhin im endgültigen Heap-Snapshot enthalten sind.  Blaue Balken zeigen Objekte an, die am Ende der Zeitachse weiterhin aktiv sind, und graue Balken zeigen Objekte an, die während der Zeitachse zugewiesen wurden, die aber seither als Garbage Collection erfasst wurden.  

> ##### Abbildung 3  
> **Zuordnungs Instrumentation auf der Zeitachse** -Momentaufnahme  
> ![Zuordnungs Instrumentation auf der Zeitachse-Momentaufnahme][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Sie können die Schieberegler in der obigen Zeitachse verwenden, um den jeweiligen Schnappschuss zu vergrößern und die Objekte anzuzeigen, die kürzlich zu diesem Zeitpunkt zugewiesen wurden:  

> ##### Abbildung4  
> Vergrößern des Schnappschusses  
> ![Vergrößern des Schnappschusses][ImageSliders]  

Wenn Sie auf ein bestimmtes Objekt im Heap klicken, wird im unteren Teil des Heap-Snapshots die Beibehaltungs Struktur angezeigt.  Wenn Sie den Beibehaltungs Pfad für das Objekt untersuchen, sollten Sie genügend Informationen erhalten, um zu verstehen, warum das Objekt nicht erfasst wurde, und Sie sollten die erforderlichen Codeänderungen vornehmen, um den unnötigen Verweis zu entfernen.  

## Anzeigen der Speicherzuweisung nach Funktion   

Sie können die Speicherzuweisung nach JavaScript-Funktion anzeigen.  Weitere Informationen finden Sie unter [untersuchen der Speicherzuweisung nach Funktion][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .  

<!--## Feedback   -->  



<!-- image links -->  

[ImageObjectTracker]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png "Abbildung 1: Zuordnungs Instrumentation auf Zeitachse"  
[ImageRecordHeap]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png "Abbildung 2: Aufzeichnen von Heapzuweisungen Profiler"  
[ImageCollected]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timelines-snapshot.msft.png "Abbildung 3: Zuordnungs Instrumentation auf der Zeitachse-Momentaufnahme"  
[ImageSliders]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png "Abbildung 4: Vergrößern des Schnappschusses"  

<!-- links -->  

[DevToolsOpenIndex]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge (Chrom) devtools"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: /microsoft-edge/devtools-guide-chromium/memory-problems/index#investigate-memory-allocation-by-function "Untersuchen der Speicherzuweisung nach Funktions Behebung von Speicherproblemen"  

<!--[HeapProfiler]: ../profile/memory-problems/heap-snapshots ""  -->  
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
