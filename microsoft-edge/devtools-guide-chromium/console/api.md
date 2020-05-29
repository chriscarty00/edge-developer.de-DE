---
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601754"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Konsolen-API-Referenz   

  

Verwenden Sie die API-Methoden für die Konsole, um Nachrichten aus Ihrem JavaScript in die Konsole zu schreiben.  Eine interaktive Einführung in das Thema finden Sie unter [Erste Schritte mit der Protokollierung von Nachrichten in der Konsole][DevtoolsConsoleLog] .  Weitere Informationen finden Sie unter [Console Utilities API Reference] [DevtoolConsoleUtilities] , wenn Sie nach den Convenience-Methoden suchen, die `debug()` `monitorEvents()` nur über die Konsole verfügbar sind.  

## kann  

```javascript
console.assert(expression, object)
```

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Schreibt einen [Fehler](#error) in die Konsole, wenn `expression` ausgewertet wird `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### Abbildung1  
> Das Ergebnis des `console.assert()` Beispiels  
> ![Das Ergebnis des Console. Assert ()-Beispiels][ImageAssert]  

## Deaktivieren  

```javascript
console.clear()
```

Löscht die Konsole.  

```javascript
console.clear();  
```  

Wenn [Protokoll beibehalten][DevtoolsConsoleReferenceLevel] aktiviert ist, ist die [Clear](#clear) -Methode deaktiviert.  

Siehe auch: [Löschen der Konsole][DevtoolsConsoleReferenceClear]  

## Anzahl  

```javascript
console.count([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Schreibt die Häufigkeit, mit der die [count](#count) -Methode in derselben Zeile und mit der gleichen aufgerufen wurde `label` .  Verwenden Sie die [countReset](#countreset) -Methode, um die Anzahl zurückzusetzen.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### Abbildung2  
> Das Ergebnis des `console.count()` Beispiels  
> ![Das Ergebnis des Console. Count ()-Beispiels][ImageCount]  

## countReset  

```javascript
console.countReset([label])
```  

Setzt die Anzahl zurück.  

```javascript
console.countReset();
console.countReset('coffee');
```  

## debuggen  

```javascript
console.debug(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Identisch mit der [Log](#log) -Methode.  

```javascript
console.debug('debug');  
```  

> ##### Abbildung 3  
> Das Ergebnis des `console.debug()` Beispiels  
> ![Das Ergebnis des Console. Debug ()-Beispiels][ImageDebug]  

## dir  

```javascript
console.dir(object)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine JSON-Darstellung des angegebenen Objekts.  

```javascript
console.dir(document.head);
```  

> ##### Abbildung4  
> Das Ergebnis des `console.dir()` Beispiels  
> ![Das Ergebnis des Console. dir ()-Beispiels][ImageDir]  

## DirXML  

```javascript
console.dirxml(node)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine XML-Darstellung der untergeordneten Elemente von `node` .  

```javascript
console.dirxml(document);
```  

> ##### Abbildung5  
> Das Ergebnis des `console.dirxml()` Beispiels  
> ![Das Ergebnis des Console. DirXML ()-Beispiels][ImageDirXml]  

## Fehler  

```javascript
console.error(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

Druckt die `object` auf der Konsole, formatiert sie als Fehler und enthält eine Stapelüberwachung.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### Abbildung6  
> Das Ergebnis des `console.error()` Beispiels  
> ![Das Ergebnis des Console. Error ()-Beispiels][ImageError]  

## Gruppe  

```javascript
console.group(label)
```  

Gruppiert Nachrichten visuell, bis die [groupEnd](#groupend) -Methode verwendet wird.  Verwenden Sie die [groupCollapsed](#groupcollapsed) -Methode, um die Gruppe zu reduzieren, wenn Sie zuerst in der Konsole angemeldet ist.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### Abbildung7  
> Das Ergebnis des `console.group()` Beispiels  
> ![Das Ergebnis des Console. Group ()-Beispiels][ImageGroup]  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identisch mit der [Log](#log) -Methode, mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn Sie in der Konsole protokolliert wird.  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Beendet die visuelle Gruppierung von Nachrichten.  Sehen Sie sich die [Group](#group) -Methode an.  

## „Informationen”  

```javascript
console.info(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Identisch mit der [Log](#log) -Methode.  

```javascript
console.info('info');
```  

> ##### Abbildung8  
> Das Ergebnis des `console.info()` Beispiels  
> ![Das Ergebnis des Console.info ()-Beispiels][ImageInfo]  

## Protokoll  

```javascript
console.log(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine Nachricht an die Konsole.  

```javascript
console.log('log');
```  

> ##### Abbildung 9  
> Das Ergebnis des `console.log()` Beispiels  
> ![Das Ergebnis des Console. log ()-Beispiels][ImageLog]  

## Tabelle  

```javascript
console.table(array)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Protokolliert ein Array von Objekten als Tabelle.  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

> ##### Abbildung 10  
> Das Ergebnis des `console.table()` Beispiels  
> ![Das Ergebnis des Console. Table ()-Beispiels][ImageTable]  

## time  

```javascript
console.time([label])
```  

Startet einen neuen Timer.  Verwenden Sie die [timeEnd](#timeend) -Methode, um den Zeitgeber zu beenden und die verstrichene Zeit auf der Konsole zu drucken.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### Abbildung 11  
> Das Ergebnis des `console.time()` Beispiels  
> ![Das Ergebnis des Console. time ()-Beispiels][ImageTime]  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Stoppt einen Timer.  Sehen Sie sich die [Zeit](#time) Methode an.  

## Trace  

```javascript
console.trace()
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine Stapelüberwachung auf der Konsole.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### Abbildung 12  
> Das Ergebnis des `console.trace()` Beispiels  
> ![Das Ergebnis des Console. Trace ()-Beispiels][ImageTrace]  

## warnen  

```javascript
console.warn(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Warning`  

Druckt eine Warnung an die Konsole.  

```javascript
console.warn('warn');
```  

> ##### Abbildung 13  
> Das Ergebnis des `console.warn()` Beispiels  
> ![Das Ergebnis des Console. Warn ()-Beispiels][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Abbildung 1: das Ergebnis des Console. Assert ()-Beispiels"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Abbildung 2: das Ergebnis des Console. Count ()-Beispiels"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Abbildung 3: das Ergebnis des Console. Debug ()-Beispiels"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Abbildung 4: das Ergebnis des Console. dir ()-Beispiels"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Abbildung 5: das Ergebnis des Console. DirXML ()-Beispiels"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Abbildung 6: das Ergebnis des Console. Error ()-Beispiels"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Abbildung 7: das Ergebnis des Console. Group ()-Beispiels"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Abbildung 8: das Ergebnis des Console.info ()-Beispiels"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Abbildung 9: das Ergebnis des Console. log ()-Beispiels"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Abbildung 10: das Ergebnis des Console. Table ()-Beispiels"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Abbildung 11: das Ergebnis des Console. time ()-Beispiels"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Abbildung 12: das Ergebnis des Console. Trace ()-Beispiels"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Abbildung 13: das Ergebnis des Console. Warn ()-Beispiels"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "API-Referenz für Konsolen Dienstprogramme"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Deaktivieren der Konsole-Konsolen Referenz"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Beibehalten von Nachrichten über Seitenlasten – Konsolen Referenz"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolen Referenz"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
