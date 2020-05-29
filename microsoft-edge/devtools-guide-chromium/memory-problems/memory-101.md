---
title: Speicher Terminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: e3373cf1475ec0eeaabcebf1a7f49505c7a3c1bb
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611727"
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





# Speicher Terminologie   



In diesem Abschnitt werden allgemeine Ausdrücke beschrieben, die in der Speicheranalyse verwendet werden, und Sie gelten für eine Vielzahl von Arbeitsspeicherprofil Tools für verschiedene Sprachen.  

Die hier beschriebenen Begriffe und Begriffe beziehen sich auf das [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots].  Wenn Sie jemals mit dem Java-, .net-oder einem anderen Speicher Profiler gearbeitet haben, ist dies möglicherweise eine Auffrischung.  

## Objektgrößen  

Denken Sie an Arbeitsspeicher als ein Diagramm mit primitiven Typen \ (wie Zahlen und Zeichenfolgen \) und Objekten \ (assoziative Arrays \).  Sie wird möglicherweise visuell als Diagramm mit einer Reihe von miteinander verbundenen Punkten wie folgt dargestellt:  

> ##### Abbildung1  
> Visuelle Darstellung des Arbeitsspeichers  
>![Visuelle Darstellung des Arbeitsspeichers][ImageThinkGraph]  

Ein Objekt kann Speicher auf zwei Arten enthalten:  

*   Direkt vom Objekt.  
*   Implizit durch Speichern von Verweisen auf andere Objekte, wodurch verhindert wird, dass diese Objekte automatisch von einem Garbage Collector entfernt werden \ (**GC** für Short \).  

Bei der Arbeit mit dem [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots] in devtools \ (ein Tool zur Untersuchung von Speicherproblemen unter "Arbeitsspeicher" \) finden Sie möglicherweise einige verschiedene Informationsspalten.  Zwei, die sich hervorheben, sind eine **flache Größe** und eine **Beibehaltungs Größe**, doch was stellen diese dar?  

> ##### Abbildung2  
> Flache und gespeicherte Größe  
>![Flache und gespeicherte Größe][ImageShallowRetained]  

### Flache Größe  

Dies ist die Größe des Speichers, der vom Objekt gehalten wird.  

Typische JavaScript-Objekte verfügen über einen Speicherplatz, der für die Beschreibung reserviert ist, und zum Speichern unmittelbarer Werte.  In der Regel können nur Arrays und Zeichenfolgen eine beträchtliche flache Größe aufweisen.  Zeichenfolgen und externe Arrays verfügen jedoch häufig über Ihren Hauptspeicher im rendererspeicher, wodurch nur ein kleines Wrapperobjekt auf dem JavaScript-Heap verfügbar gemacht wird.  

Der Renderer-Arbeitsspeicher ist der gesamte Arbeitsspeicher des Prozesses, in dem eine geprüfte Seite gerendert wird: nativer Arbeitsspeicher + js-Heapspeicher des Page + js-Heapspeichers aller dedizierten Arbeitskräfte, die von der Seite gestartet wurden.  Dennoch kann selbst ein kleines Objekt eine große Menge an Arbeitsspeicher indirekt aufnehmen, indem verhindert wird, dass andere Objekte vom automatischen Garbage Collection-Prozess verworfen werden.  

### Beibehaltungs Größe  

Hierbei handelt es sich um die Größe des Arbeitsspeichers, der freigegeben wird, sobald das Objekt zusammen mit den abhängigen Objekten gelöscht wird, die aus den **Garbage Collector-Stämmen** (GC-Stämme \) nicht erreichbar sind.  

**Garbage Collector-Stämme** \ (GC-Stämme \) bestehen aus **Handles** , die \ (entweder lokal oder Global \) erstellt werden, wenn Sie einen Verweis vom systemeigenen Code auf ein JavaScript-Objekt außerhalb von V8 erstellen.  Alle derartigen Handles befinden sich möglicherweise in einem Heap-Snapshot unter **GC-Roots**  >  -**Handles** und globalen **GC-Stamm**  >  **Handles**.  Die Beschreibung der Handles in dieser Dokumentation, ohne die Details der Browser Implementierung zu untertauchen, ist möglicherweise verwirrend.  Sowohl Garbage Collector (GC)-Stämme als auch die Ziehpunkte sind keine Grund zur Sorge.  

Es gibt viele interne GC-Stämme, von denen die meisten nicht für die Benutzer interessant sind.  Aus Sicht der Anwendungen gibt es folgende Arten von Stämmen:  

*   Globales Window-Objekt \ (in jedem IFRAME \).  In den Heap-Schnappschüssen gibt es ein Entfernungs Feld, bei dem es sich um die Anzahl der Eigenschaftsverweise auf dem kürzesten Beibehaltungs Pfad aus dem Fenster handelt.  
*   Dokument-DOM-Struktur, bestehend aus allen systemeigenen DOM-Knoten, die durch Durchlaufen des Dokuments erreichbar sind.  Nicht alle Knoten können js-Wrapper aufweisen, aber wenn ein Knoten über einen Wrapper verfügt, ist er lebendig, während das Dokument aktiv ist.  
*   Manchmal werden Objekte im Debugger-Kontext im **Quellen** Panel und in der **Konsole** (beispielsweise nach der Konsolen Auswertung \) gespeichert.  Erstellen Sie Heap-Schnappschüsse mit einem gelöschten **Konsolen** Panel und keine aktiven Haltepunkte im Debugger im **Quellen** Panel.

>[!TIP]
> Deaktivieren Sie die **Konsolen** Leiste, indem Sie die `clear()` Haltepunkte im **Quellen** Panel ausführen und deaktivieren, bevor Sie einen Heap-Schnappschuss im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots]aufnehmen.

Der Speicher Graph beginnt mit einem Stamm, der möglicherweise das `window` Objekt des Browsers oder das `Global` Objekt eines Node. js-Moduls ist.  Sie steuern nicht, wie dieses Stammobjekt Garbage Collection (GGT) ist.  

> ##### Abbildung 3  
> Sie können nicht steuern, wie das Stammobjekt Garbage Collection ist \ (GGT \).  
>![Sie können nicht steuern, wie das Stammobjekt Garbage Collection (GGT) ist.][ImageDontControl]  

Was nicht über den Stamm erreichbar ist, erhält Garbage Collection \ (GGT \).  

> [!NOTE]
> Die Spalten " [flache Größe](#shallow-size) " und " [Größe beibehalten](#retained-size) " stellen Daten in Bytes dar.  

## Objekte, die die Struktur beibehalten  

Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.  In der mathematischen Welt wird diese Struktur als **Diagramm** oder Speicher Diagramm bezeichnet.  Ein Diagramm wird aus **Knoten** erstellt, die über **Kanten**verbunden sind, wobei beide Bezeichnungen angegeben werden.  

*   **Knoten** \ (oder **Objekte**\) werden mit dem Namen der **Konstruktorfunktion** gekennzeichnet, die zum Erstellen verwendet wurde.  
*   **Kanten** werden mit den Namen der **Eigenschaften**gekennzeichnet.  

Erfahren Sie [, wie Sie ein Profil mit dem Heap Profiler aufzeichnen][DevtoolsMemoryProblemsHeapSnapshots].  Einige der auffälligen Elemente, die in der Heap-Snapshot-Aufzeichnung im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots] in [Abbildung 4](#figure-4) angezeigt werden, umfassen Abstand: die Entfernung vom Garbage Collector \ (GC \)-Stamm.  Wenn sich fast alle Objekte desselben Typs im gleichen Abstand befinden und einige wenige in größerer Entfernung sind, ist das eine Untersuchung Wert.  

> ##### Abbildung4  
> Abstand vom Stamm  
>![Abstand vom Stamm][ImageRoot]  

## Dominators  

Dominator-Objekte bestehen aus einer Struktur, da jedes Objekt genau einen Dominator hat.  Ein Dominator eines Objekts kann keine direkten Bezüge auf ein Objekt aufweisen, das es dominiert; Das bedeutet, dass die Struktur des Dominators keine Spanning-Struktur des Diagramms ist.  

[Abbildung 5](#figure-5):  

*   Knoten 1 dominiert Knoten 2  
*   Knoten 2 dominiert die Knoten 3, 4 und 6  
*   Knoten 3 dominiert Knoten 5  
*   Knoten 5 dominiert Knoten 8  
*   Knoten 6 dominiert Knoten 7  

> ##### Abbildung5  
> Struktur des Dominators  
>![Struktur des Dominators][ImageDominatorsSpanning]  

In [Abbildung 6](#figure-6)ist Knoten `#3` der Dominator von `#10` , aber `#7` es gibt auch in jedem einfachen Pfad vom Garbage Collector \ (GC \) bis `#10` .  Daher ist ein Objekt b ein Dominator eines Objekts a, wenn b in jedem einfachen Pfad vom Stamm zum Objekt a vorhanden ist.  

> ##### Abbildung6  
> Animierte Dominator-Illustration  
>![Animierte Dominator-Illustration][ImageDominators]  

## V8-Besonderheiten  

Bei der Profilerstellung von Arbeitsspeicher ist es hilfreich zu verstehen, warum Heap Momentaufnahmen auf eine bestimmte Weise aussehen.  In diesem Abschnitt werden einige speicherbezogene Themen beschrieben, die speziell der **virtuellen V8-JavaScript-Maschine** \ (V8 VM oder VM \) entsprechen.  

### JavaScript-Objektdarstellung  

Es gibt drei primitive Typen:  

*   Zahlen \ (Beispiel `3.14159...` : \)  
*   Boolesche Werte \ ( `true` oder `false` \)  
*   Zeichenfolgen \ (Beispiel `"Werner Heisenberg"` : \)  

Primitive können nicht auf andere Werte verweisen und sind immer Blatt-oder Endpunkt Knoten.  

**Nummern** können entweder wie folgt gespeichert werden:  

*   eine direkte 31-Bit-Ganzzahl, die als **kleine ganze Zahlen** (**SMI**s \) bezeichnet wird, oder  
*   Heap-Objekte, die als **Heap-Nummern**bezeichnet werden. Heap-Nummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, wie etwa **Doubles**, oder wenn ein Wert **geschachtelt**werden muss, wie beispielsweise das Festlegen von Eigenschaften.  

**Zeichenfolgen** können entweder in folgendem gespeichert werden:  

*   der **VM-Heap**oder
*   extern im **Speicher des Renderers**.  Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, wenn beispielsweise Skript Quellen und andere Inhalte, die aus dem Web empfangen werden, gespeichert werden, anstatt auf den VM-Heap kopiert zu werden.

Der Arbeitsspeicher für neue JavaScript-Objekte wird von einem dedizierten JavaScript-Heap zugeordnet \ (oder **VM-Heap**\).  Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher so lange am Leben, wie es mindestens einen starken Bezug auf Sie gibt.  

Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt**bezeichnet.  Systemeigene Objekte werden im Gegensatz zu Heap Objekten nicht vom V8-Garbage Collector während ihrer gesamten Lebensdauer verwaltet und können nur über JavaScript mit dem JavaScript-Wrapperobjekt aufgerufen werden.  

**Cons String** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verknüpft sind und ein Ergebnis der Verkettung sind.  Die Verknüpfung des **Cons-Zeichenfolgen** Inhalts erfolgt nur bei Bedarf. Ein Beispiel wäre, wenn eine Teilzeichenfolge einer verknüpften Zeichenfolge erstellt werden muss.

Wenn Sie beispielsweise verketten `a` und `b` erhalten Sie eine Zeichenfolge, die `(a, b)` das Ergebnis der Verkettung darstellt.  Wenn Sie später `d` mit diesem Ergebnis verkettet haben, erhalten Sie eine weitere **Cons-Zeichenfolge**: `((a, b, d)` .  

**Matrix** ist ein Objekt mit numerischen Schlüsseln. **Arrays** werden in der V8-VM umfassend verwendet, um große Datenmengen zu speichern. Sätze von Schlüssel-Wert-Paaren, wie Wörterbücher, werden von **Arrays**gesichert.  

Ein typisches JavaScript-Objekt wird nur als einer von zwei **Array** Typen gespeichert:  

*   benannte Eigenschaften und  
*   numerische Elemente  

Wenn eine geringe Anzahl von Eigenschaften vorhanden ist, werden die Eigenschaften intern im JavaScript-Objekt gespeichert.  

**Map** ist ein Objekt, das sowohl die Art des Objekts als auch das Layout beschreibt. Karten werden beispielsweise verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff][V8FastProperties]zu beschreiben.  


### Objektgruppen  

Jede Gruppe **systemeigene Objekte** besteht aus Objekten, die gegenseitige Bezüge aufeinander abhalten.  Nehmen Sie beispielsweise eine DOM-Unterstruktur in Frage, bei der jeder Knoten über einen Link zum relativen übergeordneten Element und Links zum nächsten untergeordneten Element und zum nächsten nebengeordneten Element verfügt, wodurch ein verbundenes Diagramm entsteht.  Beachten Sie, dass systemeigene Objekte nicht im JavaScript-Heap dargestellt werden, daher haben systemeigene Objekte die Größe 0 (null). Stattdessen werden Wrapper Objekte erstellt.  

Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt für die Umleitung von Befehlen an ihn.  Eine Objektgruppe enthält wiederum Wrapper Objekte.  Dadurch wird jedoch kein nicht sammelbarer Zyklus erstellt, da der Garbage Collector \ (GC \) intelligent genug ist, Objektgruppen freizugeben, deren Wrapper nicht mehr referenziert werden. Aber zu vergessen, einen einzelnen Wrapper freizugeben, enthält die gesamte Gruppe und zugehörige Wrapper.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageThinkGraph]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-thinkgraph.msft.png "Abbildung 1: visuelle Darstellung des Arbeitsspeichers"  
[ImageShallowRetained]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-shallow-retained.msft.png "Abbildung 2: flache und gespeicherte Größe"  
[ImageDontControl]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dontcontrol.msft.png "Abbildung 3: Sie können nicht steuern, wie das Stammobjekt als Garbage Collection (GGT) festgestellt wird."  
[ImageRoot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-root.msft.png "Abbildung 4: Abstand vom Stamm"  
[ImageDominatorsSpanning]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominatorsspanning.msft.png "Abbildung 5: Dominator-Struktur"  
[ImageDominators]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominators.msft.gif "Abbildung 6: animierte Dominator-Abbildung"  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems/heap-snapshots "/microsoft-edge/devtools-guide-chromium/media/memory-problems"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Fast-Eigenschaften in V8 | V8"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
