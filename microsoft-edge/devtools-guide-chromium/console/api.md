---
description: Verwenden Sie die Konsolen-API, um Nachrichten in die Konsole zu schreiben.
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398049"
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

# <a name="console-api-reference"></a>Konsolen-API-Referenz  

Verwenden Sie die Console-API-Methoden, um Nachrichten aus Ihrem JavaScript in die Konsole zu schreiben.  Eine interaktive Einführung in das Thema finden Sie unter Erste Schritte [mit protokollieren von Nachrichten an der Konsole.][DevtoolsConsoleLog]  Navigieren Sie zu `debug()` `monitorEvents()` [Konsolenprogramme-API-Referenz,][DevtoolConsoleUtilities] **** um die Praktischkeitsmethoden wie oder die nur im Konsolenbereich verfügbar sind zu navigieren.  

---  

## <a name="assert"></a>assert  

```javascript
console.assert(expression, object)
```

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Schreibt einen [Fehler](#error) in die Konsole, wenn `expression` er in ausgewertet `false` wird.  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Das Ergebnis des Beispiels console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   Abbildung 1: Das Ergebnis des `console.assert()` Beispiels  
:::image-end:::  

---  

## <a name="clear"></a>clear  

```javascript
console.clear()
```

Die Konsole wird geräumt.  

```javascript
console.clear();  
```  

Wenn ["Protokoll beibehalten"][DevtoolsConsoleReferenceLevel] aktiviert ist, ist [die clear-Methode](#clear) deaktiviert.  

### <a name="see-also"></a>Weitere Informationen  

*   [Löschen der Konsole][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

```javascript
console.count([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Schreibt die Anzahl der Aufrufe der [Count-Methode](#count) in derselben Zeile und mit derselben `label` .  Verwenden Sie die [countReset-Methode,](#countreset) um die Anzahl zurückzusetzen.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Das Ergebnis des Beispiels console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   Abbildung 2: Das Ergebnis des `console.count()` Beispiels  
:::image-end:::  

---  

## <a name="countreset"></a>countReset  

```javascript
console.countReset([label])
```  

Setzt eine Anzahl zurück.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a>debuggen  

```javascript
console.debug(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Verbose`

Identisch mit [Protokoll mit](#log) Ausnahme unterschiedlicher Protokollebene.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Das Ergebnis des Beispiels console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   Abbildung 3: Das Ergebnis des `console.debug()` Beispiels  
:::image-end:::  

---  

## <a name="dir"></a>dir  

```javascript
console.dir(object)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine JSON-Darstellung des angegebenen Objekts.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Das Ergebnis des Beispiels console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   Abbildung 4: Das Ergebnis des `console.dir()` Beispiels  
:::image-end:::  

---  

## <a name="dirxml"></a>dirxml  

```javascript
console.dirxml(node)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine XML-Darstellung der untergeordneten Elemente von `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Das Ergebnis des Console.dirxml()-Beispiels" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Abbildung 5: Das Ergebnis des `console.dirxml()` Beispiels  
:::image-end:::  

---  

## <a name="error"></a>Fehler  

```javascript
console.error(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

Druckt `object` die in die Konsole, formatiert sie als Fehler und enthält eine Stapelverfolgung.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Das Ergebnis des Beispiels console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   Abbildung 6: Das Ergebnis des `console.error()` Beispiels  
:::image-end:::  

---  

## <a name="group"></a>Gruppe  

```javascript
console.group(label)
```  

Gruppen von Nachrichten visuell, bis [die groupEnd-Methode](#groupend) verwendet wird.  Verwenden Sie [die groupCollapsed-Methode,](#groupcollapsed) um die Gruppe zu reduzieren, wenn sie anfänglich bei der Konsole protokolliert wird.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Das Ergebnis des Beispiels console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   Abbildung 7: Das Ergebnis des `console.group()` Beispiels  
:::image-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Identisch mit der [Protokollmethode,](#log) mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn sie bei der Konsole protokolliert wird.  

---  

## <a name="groupend"></a>groupEnd  

```javascript
console.groupEnd(label)
```  

Beendet das visuelle Gruppieren von Nachrichten.  Navigieren Sie zur [Gruppenmethode.](#group)  

---  

## <a name="info"></a>„Informationen”  

```javascript
console.info(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Identisch mit der [Protokollmethode.](#log)  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Das Ergebnis des beispiels console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   Abbildung 8: Das Ergebnis des `console.info()` Beispiels  
:::image-end:::  

---  

## <a name="log"></a>log  

```javascript
console.log(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine Nachricht an die Konsole.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Das Ergebnis des Beispiels console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   Abbildung 9: Das Ergebnis des `console.log()` Beispiels  
:::image-end:::  

---  

## <a name="table"></a>Tabelle  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Das Ergebnis des Beispiels console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   Abbildung 10: Das Ergebnis des `console.table()` Beispiels  
:::image-end:::  

---  

## <a name="time"></a>time  

```javascript
console.time([label])
```  

Startet einen neuen Timer.  Verwenden Sie [die timeEnd-Methode,](#timeend) um den Timer zu beenden und die verstrichene Zeit in der Konsole zu drucken.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Das Ergebnis des Beispiels console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   Abbildung 11: Das Ergebnis des `console.time()` Beispiels  
:::image-end:::  

---  

## <a name="timeend"></a>timeEnd  

```javascript
console.timeEnd([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Stoppt einen Timer.  Navigieren Sie zur [Time-Methode.](#time)  

---  

## <a name="trace"></a>trace  

```javascript
console.trace()
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

Druckt eine Stapelverfolgung in die Konsole.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Das Ergebnis des Beispiels console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   Abbildung 12: Das Ergebnis des `console.trace()` Beispiels  
:::image-end:::  

---  

## <a name="warn"></a>warnen  

```javascript
console.warn(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Warning`  

Druckt eine Warnung an die Konsole.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Das Ergebnis des Console.warn()-Beispiels" lightbox="../media/console-demo-warn-button.msft.png":::
   Abbildung 13: Das Ergebnis des `console.warn()` Beispiels  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Apireferenz für Konsolenprogramme"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Löschen der Konsole – Konsolenreferenz"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Nachrichten über Seitenlasten hinweg beibehalten – Konsolenreferenz"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium)-Entwicklertools"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
