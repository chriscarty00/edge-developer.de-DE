---
description: Eine Übersicht über die Interaktion mit der aktuellen Webseite im Browser mithilfe des Konsolentools
title: Verwenden der Konsole für die Interaktion mit dem DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 56ce6b1d8f1ad98eeb9c141c2e9b002e7679d7de
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597018"
---
# <a name="use-the-console-to-interact-with-the-dom"></a>Verwenden der Konsole für die Interaktion mit dem DOM

Das **Konsolentool** dient nicht nur zum [Protokollieren von Informationen][DevtoolsConsoleConsoleLog] oder zum Ausführen von [beliebigem JavaScript.][DevtoolsConsoleConsoleJavascript]  Es ist auch eine hervorragende Möglichkeit, mit der Webseite im Browser zu interagieren.  Betrachten Sie es als Skriptumgebungsversion des **Inspect-Tools.**  

## <a name="read-from-the-dom"></a>Lesen aus dem DOM

Führen Sie die folgenden Aktionen aus, um auf die Kopfzeile der Webseite zu verweisen.  

1.  Öffnen Sie die **Konsole**.
    *   Wählen Sie `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn in die **Konsole**ein.  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Verwenden Sie document.querySelector, um einen Verweis auf die Kopfzeile in der Konsole abzurufen." lightbox="../media/console-dom-get-reference.msft.png":::
    Verwenden Sie zum Abrufen eines Verweises auf die Kopfzeile in der Konsole `document.querySelector`  
:::image-end:::  

Wenn Sie `Shift` + `Tab` den Mauszeiger auswählen oder über das HTML-Ergebnis bewegen, hebt DevTools die Kopfzeile für Sie hervor.  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools hebt den abschnitt hervor, den Sie in der Konsole auswählen" lightbox="../media/console-dom-highlight-element.msft.png":::
    DevTools hebt den abschnitt hervor, den Sie in der **Konsole** auswählen  
:::image-end:::  

## <a name="manipulate-the-dom"></a>Bearbeiten des DOM

Sie können auch die Webseite bearbeiten.  Wenn Sie z. B. **Folgendes**kopieren und einfügen oder in die Konsole eingeben, wird um die Kopfzeile ein grüner Rahmen angezeigt.

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Verwenden Sie die Konsole, um einem Element einen Rahmen hinzuzufügen." lightbox="../media/console-dom-add-border.msft.png":::
    Verwenden Sie die **Konsole,** um einem Element einen Rahmen hinzuzufügen.  
:::image-end:::  

Je nach Komplexität der Webseite kann es schwierig sein, das richtige Element zu finden, das bearbeitet werden kann.  Sie können jedoch das **Inspect-Tool** verwenden, um Ihnen zu helfen.  Angenommen, Sie möchten den `Documentation` Teil in der Kopfzeile bearbeiten.

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen  
:::image-end:::  

Führen Sie die folgenden Aktionen aus, um einen direkten Verweis auf das zu bearbeitende Element zu erhalten.  

1.  Verwenden **** Sie das Inspect-Tool, um das Element auszuwählen.  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Verwenden Sie zum Auswählen eines Elements das Tool Inspect" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        Verwenden Sie zum Auswählen eines Elements das **Tool Inspect**  
    :::image-end:::  
    
1.  Wählen Sie es aus, und DevTools springt zum **Elementtool.**  
1.  Wählen Sie das `...` Menü neben dem Element in der DOM-Struktur aus.  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="Das ausgewählte Element wird in der DOM-Struktur des Elements-Tools angezeigt, wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten." lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        Das ausgewählte Element wird in der DOM-Struktur des **Elements-Tools** angezeigt, wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten.  
    :::image-end:::  
    
1.  Öffnen Sie das Kontextmenü, und wählen Sie `Copy`  >  `Copy JS Path` .  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Kopieren des JavaScript-Pfads aus einem Element in der DOM-Struktur des Elements-Tools" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        Kopieren des JavaScript-Pfads aus einem Element in der DOM-Struktur des **Elements-Tools**  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Konsole,** und fügen Sie den Befehl ein.  
    
Um den Text des Links zu `My Playground` ändern, fügen `.textContent = "My Playground"` Sie dem befehl, den Sie zuvor eingefügt haben, hinzu.  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Verwenden der Konsole zum Ändern des Inhalts eines Elements" lightbox="../media/console-dom-change-content.msft.png":::
    Verwenden der **Konsole** zum Ändern des Inhalts eines Elements  
:::image-end:::  

Verwenden Sie alle JavaScript-DOM-Manipulationen, die Sie in der **Konsole**ausführen möchten.  Um dies bequemer zu gestalten, enthält die **Konsole** einige Hilfsmethoden.  

## <a name="helpful-console-utility-methods"></a>Hilfreiche Konsolenhilfsmethoden  

Viele Komfortmethoden und Verknüpfungen stehen Ihnen als [Konsolendienstprogramme][DevtoolsConsoleUtilities]zur Verfügung.  Einige der Methoden sind unglaublich leistungsstark und sind Dinge, die Sie wahrscheinlich als eine Reihe von Anweisungen in der Vergangenheit geschrieben `console.log()` haben.

### <a name="the-power-to-the-"></a>Die Leistungsfähigkeit von $

Die `$` hat in der **Konsole** besondere Möglichkeiten, und Sie können sich dies von jQuery merken.

*   `$_` speichert das Ergebnis des letzten Befehls.  Wenn Sie also eingeben `2 + 2` und auswählen und dann `Enter` `$_` eingeben, werden Sie von der **Konsole** `4` angezeigt.
*   `$0` `$4`ist ein Stapel der zuletzt überprüften Elemente ist immer das `$0` neueste.  Im vorherigen Beispiel haben Sie also gerade das Element im **Inspect-Tool** ausgewählt und `$0.textContent = "My Playground"` denselben Effekt eingegeben.
*   `$x()` ermöglicht ihnen die Auswahl von DOM-Elementen mit XPATH.
*   `$()` und `$$()` sind kürzere Versionen von for und `document.querySelector()` `document.querySelectorAll()` .  
    
Der folgende Codeausschnitt ruft beispielsweise alle Links auf der Webseite \(kurz für \) ab `$$('a')` und zeigt die `document.querySelectorAll('a')` Verknüpfungen als sortierbare Tabelle zum Kopieren und Einfügen an, z. B. in Excel.

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Abrufen aller Links auf der Webseite und Anzeigen des Ergebnisses als Tabelle" lightbox="../media/console-dom-get-all-links.msft.png":::
    Abrufen aller Links auf der Webseite und Anzeigen des Ergebnisses als Tabelle  
:::image-end:::  

Wenn Sie die Informationen jedoch nicht anzeigen möchten, sie aber als Daten abrufen möchten.  Die `$$('a')` Verknüpfung enthält die Ankerverknüpfungen und alle Eigenschaften für die einzelnen.  Das Problem besteht darin, dass Sie nur die Links und den zugehörigen Text verwenden möchten.  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Die $$-Verknüpfung gibt viel zu viele Informationen zurück." lightbox="../media/console-dom-too-much-link-information.msft.png":::
    Die `$$` Verknüpfung gibt viel zu viele Informationen zurück.  
:::image-end:::  

Die `$$` Verknüpfung verfügt über ein interessantes zusätzliches Feature.  Anstatt ein reines `NodeList` Like `document.querySelectorAll()` zurückzugeben, erhalten Sie mit der `$$` Verknüpfung alle `Array` Methoden.  Verwenden Sie `map()` die Methode, um die Informationen auf das zu reduzieren, was Sie benötigen.  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

Der Codeausschnitt gibt ein Array aller Verknüpfungen als Objekte mit `url` und `text` Eigenschaften zurück.  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Verwenden der Karte auf $$ zum Filtern von Informationen auf das absolute Minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    Verwenden der Zuordnung zum Filtern von `$$` Informationen bis zum minimalen Minimum  
:::image-end:::  

Sie sind noch nicht fertig, mehrere Links sind interne Links zur Webseite oder haben leeren Text.  Verwenden Sie die Filtermethode, um die internen Links zu entfernen.  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Abrufen der Links, die nicht leer und extern sind" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    Abrufen der Links, die nicht leer und extern sind  
:::image-end:::  

Wie am Anfang der Webseite angezeigt, können Sie auch diese Elemente ändern.  Der folgende Codeausschnitt erstellt beispielsweise einen grünen Rahmen um alle externen Links:

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Um alle externen Links hervorzuheben, fügen Sie jeweils einen grünen Rahmen hinzu." lightbox="../media/console-dom-highlight-links.msft.png":::
    Um alle externen Links hervorzuheben, fügen Sie jeweils einen grünen Rahmen hinzu.  
:::image-end:::  

Anstatt komplexes JavaScript zum Filtern von Ergebnissen zu schreiben, verwenden Sie die Leistungsfähigkeit von CSS-Selektoren.  

Führen Sie die folgenden Aktionen aus, um eine Tabelle mit den Informationen für alle Bilder auf der Webseite zu erstellen, bei denen es sich nicht um `src` `alt` Inlinebilder handelt.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Verwenden Sie zum Auswählen von Elementen eine komplexe CSS-Auswahl" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    Verwenden Sie zum Auswählen von Elementen eine komplexe CSS-Auswahl  
:::image-end:::  

Sind Sie bereit für ein noch komplexeres Beispiel?  HTML-Webseiten, die aus Markdown wie diesem Artikel generiert werden, verfügen über automatische ID-Werte für jede Überschrift, damit Sie einen Deep-Link zu diesem Abschnitt erstellen können.  Beispielsweise wird eine `# New features` Änderung an `<h1 id="new-features">New features</h1>` .  

Führen Sie die folgenden Aktionen aus, um alle automatischen Überschriften aufzuführen, die kopiert und eingefügt werden sollen.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

Das Ergebnis ist Text, der Inhalte für jede Überschrift enthält, gefolgt von der vollständigen URL, die darauf zeigt.  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Abrufen aller Überschriften und der generierten URLs von der Webseite" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    Abrufen aller Überschriften und der generierten URLs von der Webseite  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a>Bereinigen mit "Löschen und Kopieren"

Bei der Entwicklung in der **Konsole**kann es unübersichtlich werden.  Möglicherweise ist es frustrierend, beim Kopieren und Einfügen ergebnisse auszuwählen.  Die folgenden beiden Hilfsmethoden helfen Ihnen.  

*   `copy()` kopiert alles, was Sie in die Zwischenablage geben.  Die `copy()` Methode ist besonders nützlich, wenn Sie sie mit dieser Kopie des letzten `$_` Ergebnisses kombinieren.
*   `clear()` löscht die **Konsole**.

### <a name="read-and-monitor-events"></a>Lesen und Überwachen von Ereignissen

Zwei weitere interessante Hilfsmethoden der **Konsole** befassen sich mit der Ereignisbehandlung.

*   `getEventListeners(node)` Listet alle Ereignislistener eines Knotens auf.
*   `monitorEvents(node, events)` überwacht und protokolliert die Ereignisse, die auf einem Knoten auftreten.

Führen Sie die folgenden Aktionen aus, um alle Ereignislistener aufzuführen, die dem ersten Formular auf der Webseite zugewiesen sind.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Abrufen aller Ereignislistener für das erste Formular auf der Webseite" lightbox="../media/console-dom-get-form-events.msft.png":::
    Abrufen aller Ereignislistener für das erste Formular auf der Webseite  
:::image-end:::  

Beim Überwachen erhalten Sie jedes Mal eine Benachrichtigung in der **Konsole,** wenn sich etwas an den angegebenen Elementen ändert.  Sie definieren die Ereignisse, auf die Sie lauschen möchten, als zweiten Parameter.  Es ist wichtig, dass Sie die Ereignisse definieren, die Sie überwachen möchten, andernfalls werden alle Ereignisse gemeldet, die mit dem Element geschehen.

Führen Sie die folgenden Aktionen aus, um jedes Mal, wenn Sie einen Bildlauf durchführen, die Größe des Fensters ändern oder wenn der Benutzer eine Eingabe im Suchformular durchführt, eine Benachrichtigung in der **Konsole** zu erhalten.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Konsole zeigt jedes Bildlaufereignis an, das im Fenster auftritt" lightbox="../media/console-dom-monitor-events.msft.png":::
    **Konsole** zeigt jedes Bildlaufereignis an, das im Fenster auftritt  
:::image-end:::  

Um eine Tastenaktion für das aktuell ausgewählte Element zu protokollieren, konzentrieren Sie sich auf das Suchformular in der Kopfzeile, und wählen Sie einige Schlüssel aus.  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Konsole zeigt Keyupereignisse an, die im Formular auftreten" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    **Konsole** zeigt `keyup` Ereignisse an, die im Formular auftreten  
:::image-end:::  

Um sie zu beenden, entfernen Sie die von Ihnen festgelegte Überwachung mithilfe des folgenden Codeausschnitts.  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a>Wiederverwenden von DOM-Manipulationsskripts

Möglicherweise ist es hilfreich, das DOM über die **Konsole**zu bearbeiten.  Möglicherweise gelten bald die Einschränkungen der **Konsole** als Entwicklungsplattform.  Die gute Nachricht ist, dass das [Tool "Quellen"][DevtoolsSourcesIndex] in DevTools eine entwicklungsumgebung mit vollem Funktionsumfang bietet.  Im **Tool "Quellen"** können Sie die folgenden Aktionen ausführen.  

*   Store Die Skripts für die **Konsole** als [Codeausschnitte.][DevToolsJavascriptSnippets]  
*   Führen Sie die Skripts auf einer Webseite mithilfe einer Tastenkombination oder des Editors aus.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft-Dokumente"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft-Dokumente"  
[DevtoolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolenprogramme | Microsoft-Dokumente"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf jeder Seite mit Microsoft Edge DevTools | Microsoft-Dokumente"  
[DevtoolsSourcesIndex]: ../sources/index.md "Übersicht über die Quellentools | Microsoft-Dokumente"  
