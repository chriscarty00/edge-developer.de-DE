---
description: Eine Übersicht über die Interaktion mit der aktuellen Webseite im Browser mithilfe des Konsolentools
title: Verwenden der Konsole für die Interaktion mit dem DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483478"
---
# <a name="use-the-console-to-interact-with-the-dom"></a>Verwenden der Konsole für die Interaktion mit dem DOM

Das **Konsolentool** ist nicht nur zum Protokollieren von [Informationen][DevtoolsConsoleConsoleLog] oder zum Ausführen [von beliebigem JavaScript .][DevtoolsConsoleConsoleJavascript]  Es ist auch eine hervorragende Möglichkeit, mit der Webseite im Browser zu interagieren.  Betrachten Sie es als Skriptumgebungsversion des **Inspect-Tools.**  

## <a name="read-from-the-dom"></a>Lesen aus dem DOM

Führen Sie die folgenden Aktionen aus, um auf die Kopfzeile der Webseite zu verweisen.  

1.  Öffnen Sie die **Konsole**.
    *   Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  
1.  Geben Sie den folgenden Codeausschnitt in der Konsole ein, oder kopieren Sie ihn, und fügen Sie ihn **ein.**  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Verwenden Sie document.querySelector, um einen Verweis auf die Kopfzeile in der Konsole zu erhalten." lightbox="../media/console-dom-get-reference.msft.png":::
    Um einen Verweis auf die Kopfzeile in der Konsole zu erhalten, verwenden Sie `document.querySelector`  
:::image-end:::  

Wenn Sie den Mauszeiger über das HTML-Ergebnis auswählen oder bewegen, hebt `Shift` + `Tab` DevTools die Kopfzeile für Sie hervor.  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools hebt den abschnitt hervor, den Sie in der Konsole auswählen" lightbox="../media/console-dom-highlight-element.msft.png":::
    DevTools hebt den abschnitt hervor, den Sie in der Konsole **auswählen**  
:::image-end:::  

## <a name="manipulate-the-dom"></a>Ändern des DOM

Sie können auch die Webseite bearbeiten.  Wenn Sie beispielsweise Folgendes kopieren und einfügen oder in die **Konsole**eingeben, wird um die Kopfzeile ein grüner Rahmen angezeigt.

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Verwenden Sie die Konsole, um einem Element einen Rahmen hinzuzufügen." lightbox="../media/console-dom-add-border.msft.png":::
    Verwenden Sie die Konsole, um einem Element einen Rahmen **hinzuzufügen.**  
:::image-end:::  

Abhängig von der Komplexität der Webseite kann es bedenklich sein, das richtige Element zu finden, das bearbeitet werden soll.  Sie können jedoch das **Inspect-Tool** verwenden, um Ihnen zu helfen.  Sagen Sie, Sie möchten den `Documentation` Teil in der Kopfzeile bearbeiten.

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen  
:::image-end:::  

Führen Sie die folgenden Aktionen aus, um einen direkten Verweis auf das zu bearbeitende Element zu erhalten.  

1.  Verwenden Sie das **Inspect-Tool,** um das Element zu wählen.  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Verwenden Sie das Tool Inspector, um ein Element zu wählen." lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        Verwenden Sie das Tool Inspector, um ein Element **zu** wählen.  
    :::image-end:::  
    
1.  Wählen Sie es aus, und DevTools springt zum **Element-Tool.**  
1.  Wählen Sie `...` das Menü neben dem Element in der DOM-Ansicht aus.  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="Das ausgewählte Element wird in der DOM-Struktur des Elements-Tools angezeigt, und wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten." lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        Das ausgewählte Element wird in der DOM-Struktur des **Elements-Tools** angezeigt, und wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten.  
    :::image-end:::  
    
1.  Öffnen Sie das Kontextmenü, und wählen Sie `Copy`  >  `Copy JS Path` aus.  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Kopieren des JavaScript-Pfads aus einem Element in der DOM-Ansicht des Elements-Tools" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        Kopieren des JavaScript-Pfads aus einem Element in der DOM-Ansicht des **Elements-Tools**  
    :::image-end:::  
    
1.  Wechseln Sie zurück zur **Konsole,** und fügen Sie den Befehl ein.  
    
Wenn Sie den Text des Links in ändern möchten, fügen Sie dem zuvor `My Playground` `.textContent = "My Playground"` hinzugefügten Befehl hinzu.  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Ändern des Inhalts eines Elements mithilfe der Konsole" lightbox="../media/console-dom-change-content.msft.png":::
    Ändern **des** Inhalts eines Elements mithilfe der Konsole  
:::image-end:::  

Verwenden Sie alle JavaScript-DOM-Manipulationen, die Sie in der Konsole **tun möchten.**  Um dies einfacher zu machen, bietet **die Konsole** einige Hilfsmethoden.  

## <a name="helpful-console-utility-methods"></a>Hilfreiche Konsolenprogrammmethoden  

Viele Komfortmethoden und Verknüpfungen stehen Ihnen als [Konsolenprogramme zur Verfügung.][DevtoolsConsoleUtilities]  Einige der Methoden sind unglaublich leistungsfähig und sind Dinge, die Sie wahrscheinlich in der Vergangenheit als eine Reihe von `console.log()` Anweisungen geschrieben haben.

### <a name="the-power-to-the-"></a>Power to the $

Der `$` verfügt über spezielle Befugnisse in der **Konsole,** und Sie können sich das von jQuery merken.

*   `$_` speichert das Ergebnis des letzten Befehls.  Wenn Sie also eingeben und `2 + 2` auswählen `Enter` und dann `$_` eingeben, zeigt die **Konsole** Sie `4` an.
*   `$0` to `$4` ist ein Stapel der letzten überprüften Elemente ist immer der `$0` neueste.  Daher haben Sie im früheren Beispiel das Element im Tool **"Inspector"** ausgewählt, und geben Sie ein, `$0.textContent = "My Playground"` um denselben Effekt zu erzielen.
*   `$x()` ermöglicht ihnen die Auswahl von DOM-Elementen mithilfe von XPATH.
*   `$()` und `$$()` sind kürzere Versionen von für und `document.querySelector()` `document.querySelectorAll()` .  
    
Der folgende Codeausschnitt ruft z. B. alle Links auf der Webseite \(wie kurz für \) ab und zeigt die Links als sortierbare Tabelle zum Kopieren und Einfügen an, z. B. in `$$('a')` `document.querySelectorAll('a')` Excel.

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Alle Links auf der Webseite erhalten und das Ergebnis als Tabelle anzeigen" lightbox="../media/console-dom-get-all-links.msft.png":::
    Alle Links auf der Webseite erhalten und das Ergebnis als Tabelle anzeigen  
:::image-end:::  

Wenn Sie die Informationen jedoch nicht anzeigen möchten, sie jedoch als Daten verwenden möchten.  Die `$$('a')` Verknüpfung stellt die Verankerungslinks und alle Eigenschaften für die einzelnen Verknüpfungen zurVerknüpfung.  Das Problem ist, dass Sie nur die Links und den zugehörigen Text verwenden möchten.  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Die Verknüpfung $$ gibt viel zu viele Informationen zurück." lightbox="../media/console-dom-too-much-link-information.msft.png":::
    Die `$$` Verknüpfung gibt viel zu viele Informationen zurück.  
:::image-end:::  

Die `$$` Verknüpfung verfügt über ein interessantes zusätzliches Feature.  Anstatt ein reines Like zurückgibt, erhalten Sie mit der Verknüpfung `NodeList` `document.querySelectorAll()` alle `$$` `Array` Methoden.  Verwenden `map()` Sie die Methode, um die Informationen auf das zu reduzieren, was Sie benötigen.  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

Der Codeausschnitt gibt ein Array aller Links als Objekte mit und `url` Eigenschaften `text` zurück.  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Verwenden der Karte auf $$ zum Filtern von Informationen auf das Minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    Verwenden der Karte `$$` auf, um Informationen auf das Minimum zu filtern  
:::image-end:::  

Sie sind noch nicht fertig, mehrere Links sind interne Links zur Webseite oder haben leeren Text.  Verwenden Sie die Filtermethode, um die internen Links zu entfernen.  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Get the links that aren't empty and are external" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    Get the links that aren't empty and are external  
:::image-end:::  

Wie am Anfang der Webseite angezeigt, können Sie diese Elemente auch ändern.  Der folgende Codeausschnitt erstellt beispielsweise einen grünen Rahmen um alle externen Links:

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Um alle externen Links zu markieren, fügen Sie jeweils einen grünen Rahmen hinzu" lightbox="../media/console-dom-highlight-links.msft.png":::
    Um alle externen Links zu markieren, fügen Sie jeweils einen grünen Rahmen hinzu  
:::image-end:::  

Anstatt komplexes JavaScript zum Filtern von Ergebnissen zu schreiben, verwenden Sie die Leistung von CSS-Selektoren.  

Führen Sie die folgenden Aktionen aus, um eine Tabelle mit den Und-Informationen für alle Bilder auf der Webseite zu erstellen, die keine `src` `alt` Inlinebilder sind.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Verwenden Sie zum Auswählen von Elementen einen komplexen CSS-Selektor" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    Verwenden Sie zum Auswählen von Elementen einen komplexen CSS-Selektor  
:::image-end:::  

Bereit für ein noch komplexeres Beispiel?  HTML-Webseiten, die aus markdown wie diesem Artikel generiert werden, verfügen über automatische ID-Werte für jede Überschrift, damit Sie einen tiefen Link zu diesem Abschnitt erstellen können.  Beispiel: Eine `# New features` Änderung in `<h1 id="new-features">New features</h1>` .  

Führen Sie die folgenden Aktionen aus, um alle automatischen Überschriften auflisten, die kopiert und eingefügt werden sollen.  

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

Das Ergebnis ist Text, der Inhalt für jede Überschrift enthält, gefolgt von der vollständigen URL, die darauf verweist.  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Alle Überschriften und generierten URLs von der Webseite erhalten" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    Alle Überschriften und generierten URLs von der Webseite erhalten  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a>Bereinigen mit Clear und Copy

Bei der Entwicklung in der **Konsole**wird es möglicherweise unordentlich.  Es kann frustrierend sein, beim Kopieren und Einfügen zu versuchen, Ergebnisse zu wählen.  Die folgenden beiden Hilfsmethoden helfen Ihnen.  

*   `copy()` kopiert alles, was Sie der Zwischenablage geben.  Die Methode ist besonders nützlich, wenn Sie sie mit der Kopie des `copy()` `$_` letzten Ergebnisses kombinieren.
*   `clear()` Die Konsole **wird geräumt.**

### <a name="read-and-monitor-events"></a>Lesen und Überwachen von Ereignissen

Zwei weitere interessante Hilfsmethoden von **Console beschäftigen** sich mit der Ereignisbehandlung.

*   `getEventListeners(node)` listet alle Ereignislistener eines Knotens auf.
*   `monitorEvents(node, events)` überwacht und protokolliert die Ereignisse, die auf einem Knoten auftreten.

Führen Sie die folgenden Aktionen aus, um den gesamten Ereignislistener auflisten, der dem ersten Formular auf der Webseite zugewiesen ist.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Alle Ereignislistener für das erste Formular auf der Webseite erhalten" lightbox="../media/console-dom-get-form-events.msft.png":::
    Alle Ereignislistener für das erste Formular auf der Webseite erhalten  
:::image-end:::  

Wenn Sie überwachen, erhalten Sie **** immer dann eine Benachrichtigung in der Konsole, wenn sich etwas an den angegebenen Elementen ändert.  Sie definieren die Ereignisse, die Sie abhören möchten, als zweiten Parameter.  Es ist wichtig, dass Sie die Ereignisse definieren, die Sie überwachen möchten, andernfalls wird jedes Ereignis gemeldet, das mit dem Element passiert.

Führen Sie die **** folgenden Aktionen aus, um bei jedem Bildlauf eine Benachrichtigung in der Konsole zu erhalten, die Größe des Fensters zu ändern oder wenn der Benutzer das Suchformular einr nen soll.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Konsole zeigt jedes Bildlaufereignis an, das im Fenster passiert" lightbox="../media/console-dom-monitor-events.msft.png":::
    **Konsole** zeigt jedes Bildlaufereignis an, das im Fenster passiert  
:::image-end:::  

Um eine Beliebige Tastenaktion für das aktuell ausgewählte Element zu protokollieren, konzentrieren Sie sich auf das Suchformular in der Kopfzeile, und wählen Sie einige Schlüssel aus.  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Konsole zeigt Keyupereignisse an, die im Formular auftreten" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    **Konsole** zeigt `keyup` Ereignisse an, die im Formular auftreten  
:::image-end:::  

Entfernen Sie die überwachung, die Sie mithilfe des folgenden Codeausschnitts festgelegt haben, um sie zu beenden.  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a>Wiederverwendung von DOM-Manipulationsskripts

Möglicherweise ist es hilfreich, das DOM über die Konsole zu **bearbeiten.**  Möglicherweise stoßen Sie bald auf die Einschränkungen der **Konsole** als Entwicklungsplattform.  Die gute Nachricht ist, dass [das Sources-Tool][DevtoolsSourcesIndex] in DevTools eine voll ausgestattete Entwicklungsumgebung bietet.  Im **Tool Quellen** können Sie die folgenden Aktionen ausführen.  

*   Speichern Sie Ihre Skripts für **die Konsole** [als Codeausschnitte.][DevToolsJavascriptSnippets]  
*   Führen Sie die Skripts auf einer Webseite mithilfe einer Tastenkombination oder des Editors aus.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
