---
description: Protokollieren von Nachrichten und Ausführen von JavaScript in der Microsoft Edge DevTools Console.
title: Protokollieren von Nachrichten im Konsolentool
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483480"
---
# <a name="log-messages-in-the-console-tool"></a>Protokollieren von Nachrichten im Konsolentool  

Seit browsern entwicklertools angeboten werden, ist **die Konsole** ein Favorit.  Der Grund ist einfach.  

*   In den meisten Programmierkursen lernen Sie, eine Art Druckbefehl auszudrucken, um Einblicke in das Geschehen zu erhalten.  

Vor den DevTools waren Sie auf eine oder -Anweisung zum `alert()` `document.write()` Debuggen im Browser beschränkt.  

Wenn Sie Informationen in der Konsole protokollieren **möchten,** stehen Ihnen zahlreiche Methoden zur Verfügung.  Überprüfen Sie alle verfügbaren Methoden in der [API-Referenz][DevtoolsConsoleApi].  Im folgenden Codeausschnitt werden die wichtigsten Methoden aufgeführt.  

```javascript
// prints the text to the console as  a log message
console.log('This is a log message')
// prints the text to the console as an informational message
console.info('This is some information') 
// prints the text to the console as an error message
console.error('This is an error')
// prints the text to the console as a warning
console.warn('This is a warning') 
```  

Kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu Konsolennachrichtenbeispiele: [Protokoll, Informationen, Fehler und Warnen.][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]  Wenn Sie eine Beliebige Methode in der Konsole **ausprobieren,** scheinen die und -Methoden dasselbe zu tun, während die und-Methoden ein Symbol neben der Nachricht und eine Möglichkeit zum Überprüfen der Stapelverfolgung der Nachricht `log()` `info()` `error()` `warn()` anzeigen. [][WikiStackTrace]  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="In der Konsole werden die Nachrichten von verschiedenen Protokoll-APIs angezeigt." lightbox="../media/console-log-examples.msft.png":::
   In **der Konsole** werden die Nachrichten von verschiedenen Protokoll-APIs angezeigt.  
:::image-end:::  

Es ist jedoch weiterhin eine gute Idee, und für verschiedene Protokollaufgaben zu verwenden, da Sie mit dem Typ in der Konsole `info()` `log()` filtern [können.][DevtoolsConsoleConsoleFilters]  

## <a name="different-types-of-logs"></a>Verschiedene Typen von Protokollen  

Anstelle von Protokolltext können Sie gültige JavaScript- oder DOM-Verweise an die Konsole **senden.**  Die **Konsole** ist elegant und bestimmt den Typ, den Sie senden.  Anschließend erhalten Sie die bestmögliche Darstellung.  Kopieren Und fügen Sie den folgenden Codeausschnitt in die **Konsole** ein, oder navigieren Sie zum Anzeigen der Ergebnisse zu [Konsolennachrichtenbeispiele: Protokollieren verschiedener Typen][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].  

```javascript
let x = 2;
// logs the value of x
console.log(x);
// logs the name x and value of x
console.log({x})   
// logs a DOM reference  
console.log(document.querySelector('body'));
// logs an Object
console.log({"type":"life", "meaning": 42});
let w3techs = ['HTML', 'CSS', 'SVG', 'MathML'];
// logs an Array
console.log(w3techs);
```  

Jedes Ergebnis wird auf andere Weise angezeigt.  Verwenden Sie die Dreiecke, um die Informationen umschalten und die einzelnen Details genauer analysieren.  Die geschweiften geschweiften Zeichen um die Variable sind ein kleiner Trick, um viele Protokollnachrichten zu vermeiden, bei denen Sie nur einen Wert erhalten, aber nicht wissen, wo sie `{}` `x` ihren Ursprung hat.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Protokollvariablen unterschiedlicher Typen in der Konsole" lightbox="../media/console-log-types.msft.png":::
         Protokollvariablen unterschiedlicher Typen in der **Konsole**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Protokollvariablen unterschiedlicher Typen in der Konsole mit erweiterten zusätzlichen Informationen" lightbox="../media/console-log-types-expanded.msft.png":::
         Protokollvariablen unterschiedlicher Typen in der **Konsole** mit erweiterten zusätzlichen Informationen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a>Formatieren und Konvertieren von Werten mit Specifiern

Ein besonderes Feature aller Protokollmethoden ist, dass Sie Inserenten in Ihrer Protokollnachricht verwenden können.  Specifiers sind Teil einer Protokollnachricht und beginnen mit einem Prozentzeichen \( \) zeichen und ermöglichen es Ihnen, bestimmte Werte in verschiedenen Formaten zu protokollieren und `%` sogar zu konvertieren.  

*   `%s` Protokolle als Zeichenfolgen
*   `%i` oder `%d` protokolle als Ganze Zahlen
*   `%f` Protokolle als Gleitkommawert
*   `%o` Protokolle als erweiterbares DOM-Element
*   `%O` Protokolle als erweiterbares JavaScript-Objekt
*   `%c` ermöglicht es Ihnen, Ihre Nachricht mit CSS zu formatieren

```javascript
// logs "10x console developer"
console.log('%ix %s developer', 10, 'console');
// logs PI => 3.141592653589793
console.log(Math.PI); 
// logs PI as an integer = 3
console.log('%i', Math.PI); 
// logs the webpage body as a DOM node
console.log('%o', document.body); 
// logs the body of the webpage as a JavaScript object with all properties
console.log('%O', document.body); 
// Displays the message as red and big
console.log('%cImportant message follows','color:red;font-size:40px');
```  

Im ersten Beispiel wird angezeigt, dass die Reihenfolge der Ersetzung von Specifiern die Parameterreihenfolge nach der Zeichenfolge ist.  Wenn Sie die Ergebnisse anzeigen möchten, kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu [Konsolennachrichtenbeispiele: Protokollierung mit Specifiern][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].  Erweitern Sie die Informationen im Protokoll, um den großen Unterschied zwischen und `%o` zu `%O` anzeigen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Verwenden von Specifiern zum Protokollieren und Konvertieren von Werten" lightbox="../media/console-log-specifiers.msft.png":::
         Verwenden von Specifiern zum Protokollieren und Konvertieren von Werten  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Erweitern der Ergebnisse zeigt den Unterschied zwischen %O an und %o specifier – der Textkörper wird entweder als erweiterbarer DOM-Knoten oder als vollständige Liste aller JavaScript-Eigenschaften auf dem Webseitentext angezeigt." lightbox="../media/console-log-specifiers-expanded.msft.png":::
        Erweitern der Ergebnisse zeigt den Unterschied zwischen dem und dem Specifier an – der Textkörper wird entweder als erweiterbarer DOM-Knoten oder als vollständige Liste aller JavaScript-Eigenschaften im Webseitentext `%O` `%o` angezeigt.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a>Gruppenprotokollnachrichten

Wenn Sie viele Informationen protokollieren, können Sie die und-Methoden verwenden, um Protokollmeldungen als erweiterbare und einklappbare Gruppen `group` `groupCollapsed` in der Konsole **anzeigen.**  Gruppen können geschachtelt und benannt werden, um die Daten viel einfacher zu verstehen.  

```javascript
console.group("Passengers: Heart of Gold");
console.log('Zaphod');
console.log('Trillian');
console.log('Ford');
console.log('Arthur');
console.log('Marvin');
console.groupCollapsed("Hidden");
console.log('(Frankie & Benjy)');
console.groupEnd("Hidden");
console.groupEnd("Passengers: Heart of Gold");

let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
for (tech in technologies) {
  console.groupCollapsed(tech);
  technologies[tech].forEach(t => console.log(t));
  console.groupEnd(tech);
}
```  

Auch im zweiten Beispiel können die Gruppennamen optional generiert werden.  Wenn Sie die Ergebnisse anzeigen möchten, kopieren Und fügen Sie den vorherigen Codeausschnitt in die **Konsole** ein, oder navigieren Sie zu Konsolennachrichtenbeispiele: [Gruppieren von Protokollen][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].  Sie können die einzelnen Abschnitte erweitern und reduzieren.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Viele Werte als Gruppen protokollieren" lightbox="../media/console-log-groups.msft.png":::
         Viele Werte als Gruppen protokollieren  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Jede Gruppe kann erweitert und reduziert werden" lightbox="../media/console-log-groups-expanded.msft.png":::
        Jede Gruppe kann erweitert und reduziert werden  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a>Anzeigen komplexer Daten als Tabellen  

Die Methode protokolliert komplexe Daten nicht als ein zusammenklappbares und erweiterbares Objekt, sondern als Tabelle, die Sie mit `console.table()` unterschiedlichen Kopfzeilen sortieren können.  Eine sortierte Tabelle erleichtert es den Personen, die Informationen zu überprüfen.  Navigieren Sie zum Anzeigen in einem Beispiel zu [Konsolennachrichtenbeispiele: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].

```javascript
let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
// log technologies as an object
console.log(technologies);
// display technologies as a table
console.table(technologies);

// get the dimensions of the webpage body
let bodyDimensions = document.body.getBoundingClientRect();
// display dimensions as an object
console.log(bodyDimensions);
// display dimensions as a table
console.table(bodyDimensions);
```  

:::image type="complex" source="../media/console-log-table.msft.png" alt-text="Anzeigen von Daten mit console.table, um das Lesen zu vereinfachen" lightbox="../media/console-log-table.msft.png":::
   Anzeigen von Daten `console.table` mit, um das Lesen zu vereinfachen
:::image-end:::  

Die Ausgabe von weist nicht nur ein Tabellenformat auf, `console.table` wenn sie in der Konsole angezeigt **wird.**    Wenn Sie beispielsweise eine Tabelle kopieren und in Excel, Word oder ein anderes Produkt einfügen, das tabellarische Daten unterstützt, bleibt die Struktur erhalten.  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

Wenn die Daten benannte Parameter haben, können Sie mit der Methode auch eine von Spalten für jede Eigenschaft angeben, die `console.table()` als zweiter Parameter angezeigt werden `Array` soll.  Das folgende Beispiel zeigt, wie Sie ein Array von Spalten angeben, das besser lesbar ist.  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filterinformationen, die console.table anzeigt und ein Array von Eigenschaften bereitstellen, die als zweiter Parameter angezeigt werden" lightbox="../media/console-log-table-filtered.msft.png":::
   Filtern von Informationen, die ein Array von Eigenschaften anzeigen und `console.table` bereitstellen, das als zweiter Parameter angezeigt werden soll  
:::image-end:::  

Möglicherweise sind Sie versucht, die Protokollmethoden als Hauptmittel zum Debuggen von Webseiten zu verwenden, da Protokollmethoden einfach zu verwenden sind.  Berücksichtigen Sie das Ergebnis einer `console.log()` beliebigen Anforderung.  Liveprodukte sollten kein Protokoll verwenden, das zum Debuggen verwendet wurde.  Dies kann Insiderinformationen für Personen enthalten.  Und das in der Konsole **erstellte** Rauschen ist überwältigend.  Wenn Sie [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] oder [Live Expressions][DevtoolsConsoleLiveExpressions]verwenden, können Sie feststellen, dass Ihre Workflows effektiver sind und bessere Ergebnisse erzielen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtern von Konsolennachrichten | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Überwachen von Änderungen in JavaScript mithilfe von Live Expressions | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-examples.html "Beispiele für Konsolenmeldungen: Protokollierung, Informationen, Fehler und | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-types.html "Beispiele für Konsolenmeldungen: Protokollieren verschiedener | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-groups.html "Beispiele für Konsolenmeldungen: Gruppieren von Protokollen | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-specifiers.html "Beispiele für Konsolenmeldungen: Protokollierung mit | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-table.html "Beispiele für Konsolenmeldungen: Verwenden von | GitHub"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stapelverfolgungs-| Wikipedia"  
