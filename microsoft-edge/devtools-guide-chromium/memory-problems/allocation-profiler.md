---
description: Verwenden Sie die Zuordnungsinstrumentation auf der Zeitachse, um Objekte zu finden, die nicht ordnungsgemäß gesammelt werden, und behalten Sie weiterhin Arbeitsspeicher bei.
title: Verwenden der Zuordnungsinstrumentation auf der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: a02249840256b1e5a2469a253d765eb888527662
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564084"
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
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a>Verwenden der Zuordnungsinstrumentation auf der Zeitachse  

Verwenden **Sie die Zuordnungsinstrumentation auf der** Zeitachse, um Objekte zu finden, die nicht ordnungsgemäß gesammelt werden, und behalten Sie weiterhin Arbeitsspeicher bei.  

## <a name="how-allocation-instrumentation-on-timeline-works"></a>Funktionsweise der Zuweisungsinstrumentation auf der Zeitachse  

**Die Zuordnungsinstrumentation auf der Zeitachse** kombiniert die detaillierten Snapshotinformationen des **Heap-Profilers** mit der inkrementellen Aktualisierung und Nachverfolgung des **Leistungsbereichs.**  Auf ähnliche Weise umfasst das Nachverfolgen der Heapzuweisung für Objekte das Starten einer Aufzeichnung, das Ausführen einer Abfolge von Aktionen und das Beenden der Aufzeichnung für die Analyse.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**Die Zuordnungsinstrumentation auf der** Zeitachse nimmt in regelmäßigen Abständen Heapmomentaufnahmen während der Aufzeichnung \(so häufig wie alle 50 ms\) und eine letzte Momentaufnahme am Ende der Aufzeichnung auf.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Zuordnungsinstrumentation auf der Zeitachse" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Zuordnungsinstrumentation auf der Zeitachse**  
:::image-end:::  

> [!NOTE]
> Die Zahl nach der ist eine Objekt-ID, die in den mehreren Momentaufnahmen, die während der `@` Aufzeichnungssitzung erstellt wurden, beibehalten wird.  Die ID des beständigen Objekts ermöglicht einen genauen Vergleich zwischen Heapzuständen.  Objekte werden während der Garbage Collections verschoben, sodass das Anzeigen der Adresse eines Objekts keinen Sinn macht.  

## <a name="enable-allocation-instrumentation-on-timeline"></a>Aktivieren der Zuordnungsinstrumentation auf der Zeitachse  

Führen Sie die folgenden Aktionen aus, um mit der Verwendung der **Zuordnungsinstrumentation auf der Zeitachse zu beginnen.**  

1.  [Öffnen Sie devTools][DevtoolsOpenIndex].  
1.  Öffnen Sie **den Bereich** Arbeitsspeicher, wählen Sie das **Optionsfeld Zuordnungsinstrumentation auf der Zeitachse** aus.  
1.  Start recording (Aufzeichnung starten.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Profiler für Datensatzheapzuordnungen" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Profiler für Datensatzheapzuordnungen  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a>Lesen einer Zeitachse für die Heapzuweisung  

Die Zeitachse für die Heapzuordnung zeigt an, wo Objekte erstellt werden, und identifiziert den Aufbewahrungspfad.  In der folgenden Abbildung geben die Balken oben an, wann neue Objekte im Heap gefunden werden.  

Die Höhe der einzelnen Balken entspricht der Größe der zuletzt zugewiesenen Objekte, und die Farbe der Balken gibt an, ob diese Objekte noch in der letzten Heapmomentaufnahme gespeichert sind.  Blaue Balken zeigen Objekte an, die am Ende der Zeitachse noch live sind, graue Balken zeigen Objekte an, die während der Zeitachse zugewiesen wurden, aber seitdem garbage collected wurden.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Zuordnungsinstrumentation auf Zeitachsenmomentaufnahme" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Zuordnungsinstrumentation auf Zeitachsenmomentaufnahme**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

Sie können die Schieberegler in der obigen Zeitachse verwenden, um in diese bestimmte Momentaufnahme zu zoomen und die Objekte zu überprüfen, die zu diesem Zeitpunkt kürzlich zugewiesen wurden:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Zoomen in die Momentaufnahme" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Zoomen in die Momentaufnahme  
:::image-end:::  

Wenn Sie ein bestimmtes Objekt im Heap auswählen, wird die Aufbewahrungsstruktur im unteren Teil der Heapmomentaufnahme angezeigt.  Wenn Sie den Aufbewahrungspfad zum Objekt untersuchen, sollten Sie genügend Informationen erhalten, um zu verstehen, warum das Objekt nicht erfasst wurde, und Sie sollten die erforderlichen Codeänderungen vornehmen, um den unnötigen Verweis zu entfernen.  

## <a name="view-memory-allocation-by-function"></a>Anzeigen der Speicherzuweisung nach Funktion  

Sie können die Speicherzuweisung über die JavaScript-Funktion anzeigen.  Weitere Informationen finden Sie unter Untersuchen der [Speicherzuordnung nach Funktion][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Öffnen Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Untersuchen der Speicherzuweisung nach Funktion – Beheben von Speicherproblemen | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Herunterladen eines Microsoft Edge Kanals"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
