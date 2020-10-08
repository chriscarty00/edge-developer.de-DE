---
description: Verwenden Sie die Konsolen-API, um Nachrichten in die Konsole zu schreiben.
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 684c0a1e42357ceca0a0295859e64447251f191a
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993254"
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

Verwenden Sie die API-Methoden für die Konsole, um Nachrichten aus Ihrem JavaScript in die Konsole zu schreiben.  Eine interaktive Einführung in das Thema finden Sie unter [Erste Schritte mit der Protokollierung von Nachrichten in der Konsole][DevtoolsConsoleLog].  Informationen zu den Convenience `debug()` -Methoden `monitorEvents()` , die nur im **Konsolen** Bereich verfügbar sind, finden Sie unter [Console Utilities API Reference][DevtoolConsoleUtilities].  

---  

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

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-assert-button.msft.png":::
   Abbildung 1: das Ergebnis des `console.assert()` Beispiels  
:::image-end:::  

---  

## Deaktivieren  

```javascript
console.clear()
```

Löscht die Konsole.  

```javascript
console.clear();  
```  

Wenn [Protokoll beibehalten][DevtoolsConsoleReferenceLevel] aktiviert ist, ist die [Clear](#clear) -Methode deaktiviert.  

### Weitere Informationen  

*   [Deaktivieren der Konsole][DevtoolsConsoleReferenceClear]  

---  

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

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-count-button.msft.png":::
   Abbildung 2: das Ergebnis des `console.count()` Beispiels  
:::image-end:::  

---  

## countReset  

```javascript
console.countReset([label])
```  

Setzt die Anzahl zurück.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## debuggen  

```javascript
console.debug(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Verbose`

Identisch mit [Protokoll](#log) , außer unterschiedliche Protokollebenen.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-debug-button.msft.png":::
   Abbildung 3: das Ergebnis des `console.debug()` Beispiels  
:::image-end:::  

---  

## dir  

```javascript
console.dir(object)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine JSON-Darstellung des angegebenen Objekts.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-dir-button.msft.png":::
   Abbildung 4: das Ergebnis des `console.dir()` Beispiels  
:::image-end:::  

---  

## DirXML  

```javascript
console.dirxml(node)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine XML-Darstellung der untergeordneten Elemente von `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Abbildung 5: das Ergebnis des `console.dirxml()` Beispiels  
:::image-end:::  

---  

## Fehler  

```javascript
console.error(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

Druckt die `object` auf der Konsole, formatiert sie als Fehler und enthält eine Stapelüberwachung.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-error-button.msft.png":::
   Abbildung 6: das Ergebnis des `console.error()` Beispiels  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-group-button.msft.png":::
   Abbildung 7: das Ergebnis des `console.group()` Beispiels  
:::image-end:::  

---  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identisch mit der [Log](#log) -Methode, mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn Sie in der Konsole protokolliert wird.  

---  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Beendet die visuelle Gruppierung von Nachrichten.  Sehen Sie sich die [Group](#group) -Methode an.  

---  

## „Informationen”  

```javascript
console.info(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Identisch mit der [Log](#log) -Methode.  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-info-button.msft.png":::
   Abbildung 8: das Ergebnis des `console.info()` Beispiels  
:::image-end:::  

---  

## Protokoll  

```javascript
console.log(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine Nachricht an die Konsole.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-log-button.msft.png":::
   Abbildung 9: das Ergebnis des `console.log()` Beispiels  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-table-button.msft.png":::
   Abbildung 10: das Ergebnis des `console.table()` Beispiels  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-time-button.msft.png":::
   Abbildung 11: das Ergebnis des `console.time()` Beispiels  
:::image-end:::  

---  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Stoppt einen Timer.  Sehen Sie sich die [Zeit](#time) Methode an.  

---  

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

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-trace-button.msft.png":::
   Abbildung 12: das Ergebnis des `console.trace()` Beispiels  
:::image-end:::  

---  

## warnen  

```javascript
console.warn(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Warning`  

Druckt eine Warnung an die Konsole.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Das Ergebnis des Console. Assert ()-Beispiels" lightbox="../media/console-demo-warn-button.msft.png":::
   Abbildung 13: das Ergebnis des `console.warn()` Beispiels  
:::image-end:::  

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
