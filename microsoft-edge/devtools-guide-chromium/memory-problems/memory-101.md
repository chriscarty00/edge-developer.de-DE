---
description: In diesem Abschnitt werden allgemeine Begriffe beschrieben, die in der Speicheranalyse verwendet werden und für eine Vielzahl von Speicherprofilerstellungstools für verschiedene Sprachen gelten.
title: Speicherterminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1579374be29f0f419ded3bf88f5dea284f0bbb1a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397790"
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

# <a name="memory-terminology"></a>Speicherterminologie  

Dieser Artikel beschreibt allgemeine Begriffe, die in der Speicheranalyse verwendet werden, und gilt für verschiedene Speicherprofilerstellungstools für verschiedene Sprachen.  

Die hier beschriebenen Begriffe und Begriffe beziehen sich auf den [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots].  Wenn Sie jemals mit dem Java, .NET oder einem anderen Speicherprofiler gearbeitet haben, kann dieser Artikel eine Aktualisierung sein.  

## <a name="object-sizes"></a>Objektgrößen  

Stellen Sie sich Speicher als Diagramm mit grundtypen \(wie Zahlen und Zeichenfolgen\) und Objekten \(assoziative Arrays\) vor.  Es kann als Diagramm mit vielen verbundenen Punkten angezeigt werden, z. B. der folgenden Abbildung.  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Visuelle Darstellung des Arbeitsspeichers" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Visuelle Darstellung des Arbeitsspeichers  
:::image-end:::  

Ein Objekt kann auf zwei Arten Arbeitsspeicher haben:  

*   Direkt durch das Objekt.  
*   Implizit durch Das Halten von Verweisen auf andere Objekte und damit verhindern, dass diese Objekte automatisch von einem Garbage Collector verworfen werden.  

Bei der Arbeit mit dem [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots] in DevTools \(ein Tool zur Untersuchung von Speicherproblemen unter **Speicher**\) können Sie sich einige verschiedene Spalten mit Informationen anschauen.  Zwei, die sich abhingen, sind **Flache Größe** und **Beibehaltene Größe,** aber was stellen diese dar?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Flache und beibehaltene Größe" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Flache und beibehaltene Größe  
:::image-end:::  

### <a name="shallow-size"></a>Flache Größe  

Dies ist die Größe des Arbeitsspeichers, der vom Objekt gehalten wird.  

Bei typischen JavaScript-Objekten ist etwas Arbeitsspeicher für die Beschreibung und das Speichern von unmittelbaren Werten reserviert.  In der Regel können nur Arrays und Zeichenfolgen eine erhebliche flache Größe aufweisen.  Zeichenfolgen und externe Arrays verfügen jedoch häufig über ihren Hauptspeicher im Rendererspeicher, was nur ein kleines Wrapperobjekt im JavaScript-Heap verfügbar macht.  

Rendererspeicher ist der ganze Speicher des Prozesses, in dem eine überprüfte Seite gerendert wird: systemeigener Speicher + JS-Heapspeicher der Seite + JS-Heapspeicher aller dedizierten Mitarbeiter, die von der Seite gestartet wurden.  Dennoch kann selbst ein kleines Objekt indirekt einen großen Speicher enthalten, indem verhindert wird, dass andere Objekte durch den automatischen Garbage Collection-Prozess verworfen werden.  

### <a name="retained-size"></a>Beibehaltene Größe  

Dies ist die Größe des Arbeitsspeichers, der freigegeben wird, nachdem das Objekt gelöscht wurde, zusammen mit den abhängigen Objekten, die aus Garbage Collector-Ursprüngen nicht erreichbar **gemacht wurden.**  

**Garbage Collector-Ursprünge** werden **** aus Handles erstellt, die \(entweder lokal oder global\) erstellt werden, wenn ein Verweis aus systemeigenem Code auf ein JavaScript-Objekt außerhalb von V8 erfolgt.  Alle diese Handles finden Sie in einer Heapmomentaufnahme unter **GC roots**  >  **Handle scope** und GC **roots**  >  **Global handles**.  Die Beschreibung der Handles in dieser Dokumentation, ohne details zur Browserimplementierung zu machen, kann verwirrend sein.  Sowohl garbage collector roots als auch die Handles müssen Sie sich keine Sorgen machen.  

Es gibt viele interne Garbage Collector-Ursprünge, von denen die meisten für die Benutzer nicht interessant sind.  Aus Der Sicht der Anwendungen gibt es folgende Arten von Ursprüngen.  

*   Window global object \(in each iframe\).  In den Heapmomentaufnahmen ist ein Abstandsfeld enthalten, das die Anzahl der Eigenschaftsverweise auf dem kürzesten Aufbewahrungspfad vom Fenster aus ist.  
*   Dokument-DOM-Struktur, die aus allen systemeigenen DOM-Knoten besteht, die durch Durchlaufen des Dokuments erreichbar sind.  Nicht alle Knoten verfügen möglicherweise über JS-Wrapper, aber wenn ein Knoten über einen Wrapper verfügt, ist er lebendig, während das Dokument noch am Leben ist.  
*   Manchmal können Objekte im Debuggerkontext im Bereich **Quellen** und in der **Konsole** \(z. B. nach der Konsolenauswertung\) beibehalten werden.  Erstellen Sie Heapmomentaufnahmen mit einem geräumten **Konsolenbereich** und keine aktiven Haltepunkte im Debugger im **Bereich** Quellen.

>[!TIP]
> Deaktivieren Sie **den Konsolenbereich,** indem Sie Haltepunkte im Bereich Quellen ausführen und deaktivieren, bevor Sie eine `clear()` **** Heapmomentaufnahme im [Speicherbereich erstellen.][DevtoolsMemoryProblemsHeapSnapshots]

Das Speicherdiagramm beginnt mit einem Stamm, der das Objekt des Browsers oder das Objekt eines Node.js `window` `Global` sein kann.  Sie können nicht steuern, wie dieses Stammobjekt im Garbage Collection-Objekt gesammelt wird.  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird.  
:::image-end:::  

Was vom Stamm aus nicht erreichbar ist, wird garbage collected.  

> [!NOTE]
> Sowohl die [Spalten "Flache Größe"](#shallow-size) [als auch "Beibehaltene Größe"](#retained-size) stellen Daten in Bytes dar.  

## <a name="objects-retaining-tree"></a>Aufbewahrungsstruktur für Objekte  

Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.  In der mathematischen Welt wird diese Struktur als Diagramm **oder** Speicherdiagramm bezeichnet.  Ein Diagramm wird aus Knoten **erstellt,** die über Kanten verbunden **sind,** die beide Beschriftungen erhalten.  

*   **Knoten** \(oder **Objekte**\) werden mit **** dem Namen der Konstruktorfunktion gekennzeichnet, die zum Erstellen verwendet wurde.  
*   **Kanten** werden mit den Namen von Eigenschaften **gekennzeichnet.**  

Erfahren [Sie, wie Sie ein Profil mit dem Heap Profiler aufzeichnen.][DevtoolsMemoryProblemsHeapSnapshots]  In der folgenden Abbildung sind einige der wichtigsten Dinge in der Heap Snapshot-Aufzeichnung im [Tool Speicher][DevtoolsMemoryProblemsHeapSnapshots] enthalten: der Abstand zum Garbage Collector-Stamm.  Wenn sich fast alle Objekte desselben Typs in derselben Entfernung befinden und einige wenige sich in größerer Entfernung befinden, ist dies eine Untersuchung wert.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Abstand zum Stamm" lightbox="../media/memory-problems-root.msft.png":::
   Abstand zum Stamm  
:::image-end:::  

## <a name="dominators"></a>Dominante  

Dominantor-Objekte bestehen aus einer Strukturstruktur, da jedes Objekt über genau einen Dominanter verfügt.  Einem #A0 eines Objekts fehlen möglicherweise direkte Verweise auf ein objekt, das es überragt. Das heißt, die Struktur des Dominantors ist keine spannende Struktur des Diagramms.  

In der folgenden Abbildung ist die folgende Anweisung true.  

*   Knoten 1 überwiegen Knoten 2  
*   Knoten 2 überwiegen die Knoten 3, 4 und 6  
*   Knoten 3 überwiegen Knoten 5  
*   Knoten 5 überwiegen Knoten 8  
*   Knoten 6 überwiegen Knoten 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Struktur der dominanten Struktur" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Struktur der dominanten Struktur  
:::image-end:::  

In der folgenden Abbildung ist Knoten der Dominante von , ist aber auch in jedem einfachen Pfad von `#3` `#10` Garbage Collector zu `#7` `#10` vorhanden.  Daher ist ein Objekt B ein Dominanter eines Objekts A, wenn B in jedem einfachen Pfad vom Stamm zum Objekt A vorhanden ist.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Animierte Dominantor-Illustration" lightbox="../media/memory-problems-dominators.msft.gif":::
   Animierte Dominantor-Illustration  
:::image-end:::  

## <a name="v8-specifics"></a>V8-Spezifische  

Beim Profilerstellungsspeicher ist es hilfreich zu verstehen, warum Heapmomentaufnahmen auf eine bestimmte Weise aussehen.  In diesem Abschnitt werden einige Speicherthemen beschrieben, die speziell dem **virtuellen V8-JavaScript-Computer** \(V8 VM oder VM\) zugeordnet sind.  

### <a name="javascript-object-representation"></a>JavaScript-Objektdarstellung  

Es gibt drei Grundtypen:  

*   Zahlen \(z. B. `3.14159...` \)  
*   Booleans \( `true` oder `false` \)  
*   Zeichenfolgen \(z. B. `"Werner Heisenberg"` \)  

Grundtypen können nicht auf andere Werte verweisen und sind immer Blatt- oder Endknoten.  

**Zahlen** können wie folgt gespeichert werden:  

*   ein sofortiger ganzzahliger 31-Bit-Wert, der als **kleine ganze Zahlen** \(**SMI**s\) bezeichnet wird, oder  
*   Heapobjekte, die als **Heapnummern bezeichnet werden.** Heapnummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, z. B. **Doubles**oder wenn ein Wert geschachtelt werden **muss,** z. B. festlegen von Eigenschaften darauf.  

**Zeichenfolgen** können in einer der beiden Dateien gespeichert werden:  

*   der **VM-Heap**oder
*   extern im **Speicher des Renderers**.  Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, in dem beispielsweise Skriptquellen und andere Inhalte gespeichert werden, die aus dem Web empfangen werden, anstatt in den VM-Heap kopiert zu werden.

Der Arbeitsspeicher für neue JavaScript-Objekte wird über einen dedizierten JavaScript-Heap \(oder **VM-Heap\)** zugewiesen.  Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher am Leben, solange mindestens ein starker Verweis darauf besteht.  

Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt bezeichnet.**  Systemeigene Objekte werden im Gegensatz zu Heapobjekten nicht während ihrer gesamten Lebensdauer vom V8-Garbage Collector verwaltet und können nur über JavaScript mithilfe des JavaScript-Wrapperobjekts zugegriffen werden.  

**Cons string** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verbunden werden, und ist ein Ergebnis der Verkettung.  Die Verbindung der **Inhalte der Cons-Zeichenfolge** erfolgt nur nach Bedarf.  Wenn z. B. eine Teilzeichenfolge einer angeschlossenen Zeichenfolge erstellt werden muss.

Wenn Sie z. B. und verketten, erhalten Sie eine Zeichenfolge, die das Ergebnis der `a` `b` `(a, b)` Verkettung darstellt.  Wenn Sie später mit diesem Ergebnis `d` verkettet sind, erhalten Sie eine weitere **Cons-Zeichenfolge:** `((a, b, d)` .  

**Array** ist ein Objekt mit numerischen Schlüsseln. **Arrays** werden in der V8 VM umfassend zum Speichern großer Datenmengen verwendet. Sätze von Schlüssel-Wert-Paaren, z. B. Wörterbücher, werden durch **Arrays gesichert.**  

Ein typisches JavaScript-Objekt wird nur als einer von zwei **Arraytypen** gespeichert:  

*   benannte Eigenschaften und  
*   numerische Elemente  

Bei einer kleinen Anzahl von Eigenschaften werden die Eigenschaften intern im JavaScript-Objekt gespeichert.  

**Map** ist ein Objekt, das sowohl den Objekttyp als auch das Layout beschreibt. Beispielsweise werden Karten verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff zu beschreiben.][V8FastProperties]  

### <a name="object-groups"></a>Objektgruppen  

Jede **systemeigene Objektgruppe** besteht aus Objekten, die gegenseitige Verweise aufeinander enthalten.  Stellen Sie sich beispielsweise eine DOM-Unterstruktur vor, in der jeder Knoten eine Verknüpfung zum relativen übergeordneten Element und Links zum nächsten untergeordneten und nächsten gleichgeordneten Element hat und daher ein verbundenes Diagramm bildet.  

> [!NOTE]
> Systemeigene Objekte werden nicht im JavaScript-Heap dargestellt.  Die fehlende Darstellung ist der Grund, warum systemeigene Objekte die Größe Null haben. Stattdessen werden Wrapperobjekte erstellt.  

Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt zum Umleiten von Befehlen an dieses Objekt.  Eine Objektgruppe enthält wiederum Wrapperobjekte.  Dadurch wird jedoch kein unkollektierbarer Zyklus erstellt, da Garbage Collector intelligent genug ist, um Objektgruppen frei zu lassen, auf deren Wrapper nicht mehr verwiesen wird.  Vergessen sie jedoch, einen einzelnen Wrapper zu veröffentlichen, enthält die gesamte Gruppe und die zugehörigen Wrapper.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Aufzeichnen von Heapmomentaufnahmen | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Schnelle Eigenschaften in V8-| V8"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
