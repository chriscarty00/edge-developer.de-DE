---
description: Referenz für die CSS-Domäne Diese Domäne macht CSS-Lese-und Schreibvorgänge verfügbar. Alle CSS-Objekte (Stylesheets, Regeln und Formatvorlagen) verfügen über ein zugeordnetes `id` Objekt, das in nachfolgenden Vorgängen des verknüpften Objekts verwendet wird. Jeder Objekttyp hat eine bestimmte `id` Struktur, die nicht zwischen Objekten unterschiedlicher Art austauschbar sind. CSS-Objekte können mithilfe der `get*ForNode()` Aufrufe (die eine DOM-Knoten-ID akzeptieren) geladen werden. Ein Client kann über die Ereignisse auch Stylesheets nachverfolgen `styleSheetAdded` / `styleSheetRemoved` und anschließend die erforderlichen Stylesheet-Inhalte mit den `getStyleSheet[Text]()` Methoden laden.
title: CSS-Domäne – devtools-Protokoll Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf5efdef09b7e2d9041cd8536faaff8fb99a7f71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234016"
---
# CSS

Diese Domäne macht CSS-Lese-und Schreibvorgänge verfügbar. Alle CSS-Objekte (Stylesheets, Regeln und Formatvorlagen) verfügen über ein zugeordnetes `id` Objekt, das in nachfolgenden Vorgängen des verknüpften Objekts verwendet wird. Jeder Objekttyp hat eine bestimmte `id` Struktur, die nicht zwischen Objekten unterschiedlicher Art austauschbar sind. CSS-Objekte können mithilfe der `get*ForNode()` Aufrufe (die eine DOM-Knoten-ID akzeptieren) geladen werden. Ein Client kann über die Ereignisse auch Stylesheets nachverfolgen `styleSheetAdded` / `styleSheetRemoved` und anschließend die erforderlichen Stylesheet-Inhalte mit den `getStyleSheet[Text]()` Methoden laden.

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**Veranstaltungen**](#events) | [styleSheetAdded](#stylesheetadded), [stylesheetd](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Typen**](#types) | [Stylesheet](#stylesheetid)- [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Wert](#value), [selectorlist](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader) |
| [**Abhängigkeiten**](#dependencies) | [DOM](dom.md) |
## Methoden

### Aktivieren
Aktiviert den CSS-Agent für die angegebene Seite. Clients sollten nicht davon ausgehen, dass der CSS-Agent aktiviert wurde, bis das Ergebnis dieses Befehls empfangen wurde.

</p>

---

### Deaktivieren 
Deaktiviert den CSS-Agent für die angegebene Seite.

</p>

---

### getInlineStylesForNode
Gibt die Inline definierten Formatvorlagen (explizit im "Style"-Attribut und implizit unter Verwendung von Dom-Attributen) für einen DOM-Knoten zurück, der von angegeben wird `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ininlinestyle <br /> <i>Optional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Inline Formatvorlage für den angegebenen DOM-Knoten.</td>
        </tr>
        <tr>
            <td>Attributes <br /> <i>Optional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Attribut definierte Element Formatvorlage (z. b. durch "Width = 20 height = 100%").</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Gibt angeforderte Formatvorlagen für einen DOM-Knoten zurück, der von angegeben wird `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ininlinestyle <br /> <i>Optional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Inline Formatvorlage für den angegebenen DOM-Knoten.</td>
        </tr>
        <tr>
            <td>Attributes <br /> <i>Optional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Attribut definierte Element Formatvorlage (z. b. durch "Width = 20 height = 100%").</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>Optional</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>CSS-Regeln, die diesem Knoten entsprechen, aus allen anwendbaren Stylesheets.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>Optional</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>Pseudo Format Übereinstimmungen für diesen Knoten</td>
        </tr>
        <tr>
            <td>geerbt <br /> <i>Optional</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Eine Kette geerbter Formatvorlagen (vom übergeordneten Element des unmittelbaren Knotens bis zum Stammverzeichnis der DOM-Struktur).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>Optional</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Eine Liste der CSS-Keyframes-Animationen, die diesem Knoten entsprechen.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Fordert Informationen zu Platt Form Schriftarten an, die zum Rendern untergeordneter textnodes im angegebenen Knoten verwendet wurden.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Schriftarten</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Verwendungsstatistiken für jede verwendete Platt Form Schriftart</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Gibt den berechneten Stil für einen DOM-Knoten zurück, der von identifiziert wird `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>computestyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Berechnete Formatvorlage für den angegebenen DOM-Knoten.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Veranstaltungen

### styleSheetAdded
Wird ausgelöst, wenn ein Active Document-Stylesheet hinzugefügt wird.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>Stylesheet-Metainformationen hinzugefügt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### stylesheetd
Wird ausgelöst, wenn ein Stylesheet als Ergebnis des Client Vorgangs geändert wird.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Wird ausgelöst, wenn ein Active Document-Stylesheet entfernt wird.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Bezeichner des entfernten Stylesheets.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Typen

### <a name="stylesheetid"></a> Stylesheet-Nr `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

CSS-Regelsammlung für eine einzelne Pseudo Formatvorlage.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Pseudotyp</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Pseudo Elementtyp.</td>
        </tr>
        <tr>
            <td>entspricht</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Übereinstimmungen der CSS-Regeln, die für das Pseudo Format gelten.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Geerbte CSS-Regelsammlung aus dem Vorgängerknoten

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ininlinestyle <br /> <i>Optional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Die Inlineformatvorlage des Vorgänger Knotens, falls vorhanden, in der Stil Vererbungskette.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Übereinstimmungen mit CSS-Regeln, die dem Vorgängerknoten in der Stil Vererbungskette entsprechen.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Vergleichen von Daten für eine CSS-Regel

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Regel</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>CSS-Regel in der Übereinstimmung.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Wert `object`

Daten für eine einfache Auswahl (diese werden durch Kommas in einer Auswahlliste getrennt).

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Text</td>
            <td><code class="flyout">string</code></td>
            <td>Wert Text</td>
        </tr>
        <tr>
            <td>Bereich <br /> <i>Optional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Wertbereich in der zugrunde liegenden Ressource (sofern verfügbar).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> Selektorliste `object`

Auswahllisten Daten.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Selektoren</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Wählen Sie in der Liste aus.</td>
        </tr>
        <tr>
            <td>Text</td>
            <td><code class="flyout">string</code></td>
            <td>Regel Auswahl Text</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

CSS-Regel Darstellung

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr <br /> <i>Optional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</td>
        </tr>
        <tr>
            <td>selektorliste <br /> <i>Optional</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Regel Auswahldaten.</td>
        </tr>
        <tr>
            <td>Ursprung <br /> <i>Optional</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Herkunft des übergeordneten Stylesheets</td>
        </tr>
        <tr>
            <td>Formatvorlage</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Zugeordnete Formatvorlagendeklaration.</td>
        </tr>
        <tr>
            <td>Medien <br /> <i>Optional</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Array für Medienlisten (für Regeln mit medienabfragen) Das Array listet medienabfragen auf, die mit dem innersten beginnen und nach außen gehen.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Text Bereich innerhalb einer Ressource. Alle Zahlen sind nullbasiert.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Start Linie des Bereichs</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Start Spalte des Bereichs (inklusive).</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Endzeile des Bereichs</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Ende der Spalte des Bereichs (exklusiv).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Kurzbezeichnung</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Kurzform-Wert.</td>
        </tr>
        <tr>
            <td>wichtig <br /> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Eigenschaft eine "! Important"-Anmerkung hat (impliziert, `false` Wenn nicht vorhanden).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Darstellung des CSS-Formats

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr <br /> <i>Optional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>CSS-Eigenschaften in der Formatvorlage.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Berechnete Werte für alle in der Formatvorlage gefundenen Abkürzungen.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Text für die Formatvorlagendeklaration (sofern verfügbar).</td>
        </tr>
        <tr>
            <td>Bereich <br /> <i>Optional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Der Stil Deklarationsbereich im einschließenden Stylesheet (sofern verfügbar).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

CSS-Eigenschaften Deklarationsdaten.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Der Name der Eigenschaft.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Der Eigenschaftswert.</td>
        </tr>
        <tr>
            <td>wichtig <br /> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Eigenschaft eine "! Important"-Anmerkung hat (impliziert, `false` Wenn nicht vorhanden).</td>
        </tr>
        <tr>
            <td>implizite <br /> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Eigenschaft implizit ist (impliziert, `false` Wenn nicht vorhanden).</td>
        </tr>
        <tr>
            <td>Text <br /> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Der vollständige Eigenschafts Text wie in der Formatvorlage angegeben.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Eigenschaft vom Browser verstanden wird (impliziert, `true` Wenn nicht vorhanden).</td>
        </tr>
        <tr>
            <td>deaktiviert <br /> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Eigenschaft vom Benutzer deaktiviert wurde (nur für Quell basierte Eigenschaften vorhanden).</td>
        </tr>
        <tr>
            <td>Bereich <br /> <i>Optional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Der gesamte Eigenschaftenbereich in der einschließenden Formatvorlagendeklaration (sofern verfügbar).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

CSS Media Rule Descriptor.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Text</td>
            <td><code class="flyout">string</code></td>
            <td>Medienabfrage Text</td>
        </tr>
        <tr>
            <td>Quelle</td>
            <td><code class="flyout">string</code> <br /> <i>Zulässige Werte: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Quelle der medienabfrage: "mediaRule", wenn Sie durch eine @Media Regel angegeben wird, "importRule", wenn Sie durch eine @Import Regel angegeben wird, "linkedSheet", wenn Sie durch ein "Medien"-Attribut im Linktag eines verknüpften Stylesheets angegeben wird, "inlineSheet", wenn es durch ein "Medien"-Attribut im Style-Tag eines Inlinestylesheets angegeben wird.</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Die URL des Dokuments, das die Beschreibung der medienabfrage enthält.</td>
        </tr>
        <tr>
            <td>Bereich <br /> <i>Optional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Der zugeordnete Regelbereich (@Media oder @Import) im einschließenden Stylesheet (sofern verfügbar).</td>
        </tr>
        <tr>
            <td>Stylesheet-Nr <br /> <i>Optional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Bezeichner des Stylesheets, das dieses Objekt enthält (sofern vorhanden).</td>
        </tr>
        <tr>
            <td>medialist <br /> <i>Optional</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Array von medienabfragen</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Beschreibung der medienabfrage

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ausdrücke</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Array von medienabfrage Ausdrücken</td>
        </tr>
        <tr>
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die medienabfrage Bedingung erfüllt ist.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Medienabfrage-Ausdrucks Beschreibung.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Medienabfrage Ausdruckswert.</td>
        </tr>
        <tr>
            <td>Einheit</td>
            <td><code class="flyout">string</code></td>
            <td>Medienabfrage Ausdrucks Einheiten</td>
        </tr>
        <tr>
            <td>Features</td>
            <td><code class="flyout">string</code></td>
            <td>Medienabfrage Ausdrucks-Feature.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>Optional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Der zugeordnete Bereich des Wert Texts im einschließenden Stylesheet (sofern verfügbar).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>Optional</i></td>
            <td><code class="flyout">number</code></td>
            <td>Berechnete Länge des medienabfrage Ausdrucks (falls zutreffend).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Informationen über die Anzahl der Glyphen, die mit der angegebenen Schriftart gerendert wurden.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>familyName</td>
            <td><code class="flyout">string</code></td>
            <td>Der von Platform gemeldete Familienname der Schriftart.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob die Schriftart heruntergeladen oder lokal aufgelöst wurde.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Die Anzahl der Glyphen, die mit dieser Schriftart gerendert wurden.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

CSS-Keyframes-Regel Darstellung

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Animations</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Animations Name</td>
        </tr>
        <tr>
            <td>Keyframes</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Liste der Keyframes.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

CSS-Keyframe-Regel Darstellung

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr <br /> <i>Optional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</td>
        </tr>
        <tr>
            <td>Ursprung</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Herkunft des übergeordneten Stylesheets</td>
        </tr>
        <tr>
            <td>keyText</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Zugeordneter Schlüssel Text</td>
        </tr>
        <tr>
            <td>Formatvorlage</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Zugeordnete Formatvorlagendeklaration.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Eigenschaftsname für berechnete Formatvorlage</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Eigenschaftswert des berechneten Stils.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Metainformationen für CSS-Stylesheets.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stylesheet-Nr</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Der Stylesheet-Bezeichner.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>Stylesheet-Ressourcen-URL.</td>
        </tr>
        <tr>
            <td>deaktiviert</td>
            <td><code class="flyout">boolean</code></td>
            <td>Kennzeichnet, ob das Stylesheet deaktiviert ist.</td>
        </tr>
        <tr>
            <td>IsInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob dieses Stylesheet für Style-Tags nach Parser erstellt wird. Dieses Flag ist nicht für Document. written-Stil Kategorien definiert.</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">number</code></td>
            <td>Der Versatz des Stylesheets innerhalb der Ressource (nullbasiert)</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">number</code></td>
            <td>Spaltenoffset des Stylesheets innerhalb der Ressource (nullbasiert).</td>
        </tr>
        <tr>
            <td>Länge</td>
            <td><code class="flyout">number</code></td>
            <td>Die Größe des Inhalts (in Zeichen).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Abhängigkeiten

[DOM](dom.md)
