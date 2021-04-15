---
description: Verwenden Sie die Konsolen-API, um Nachrichten in die Konsole zu schreiben.
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 54b89e25501449a1e5119afa812a0535fbc6ffbb
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483254"
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

Das **Konsolentool** ist hilfreich, wenn Sie mehrere Aufgaben in devTools ausführen.  APIs stehen in Ihren Skripts zur Verfügung. Convenience-Methoden sind nur für **** die Verwendung im Konsolentool verfügbar, z. B. für `debug()` die `monitorEvents()` und-Methoden.  Weitere Informationen zum Einstieg **** in die Konsole finden Sie unter Erste Schritte mit der [Protokollierung von Nachrichten an der Konsole.][DevtoolsConsoleConsoleLog]  Weitere Informationen zu den Komfortmethoden in der **Konsole finden**Sie unter [Console Utilities API Reference][DevtoolConsoleUtilities].  

---  

## <a name="assert"></a>assert  

Diese Methode schreibt einen [Fehler in](#error) die **Konsole,** wenn `expression` sie in ausgewertet `false` wird.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.assert(expression, object)
```

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const x = 5;
      const y = 3;
      const reason = 'x is expected to be less than y';
      console.assert(x < y, {x, y, reason});
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Das Ergebnis des Beispiels console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         Das Ergebnis des `console.assert()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a>clear  

Mit dieser Methode wird die **Konsole geräumt.**  

Wenn [Das Protokoll beibehalten][DevtoolsConsoleReferenceFilter] aktiviert ist, ist die [clear-Methode](#clear) deaktiviert.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.clear()
```

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a>Weitere Informationen  

*   [Löschen der Konsole][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

Diese Methode schreibt die Anzahl der Aufrufe der [Count-Methode](#count) in derselben Zeile und mit derselben `label` .  Verwenden Sie die [countReset-Methode,](#countreset) um die Anzahl zurückzusetzen.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.count([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.count();
      console.count('coffee');
      console.count();
      console.count();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Das Ergebnis des Beispiels console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         Das Ergebnis des `console.count()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a>countReset  

Mit dieser Methode wird eine Anzahl zurückgesetzt.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.countReset();
      console.countReset('coffee');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a>debuggen  

Diese Methode ist mit der [Protokollmethode identisch,](#log) mit Ausnahme der unterschiedlichen Protokollebene.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.debug(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Verbose`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Das Ergebnis des Beispiels console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         Das Ergebnis des `console.debug()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a>dir  

Diese Methode druckt eine JSON-Darstellung des angegebenen Objekts.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.dir(object)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Das Ergebnis des Beispiels console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         Das Ergebnis des `console.dir()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a>dirxml  

Diese Methode druckt eine XML-Darstellung der untergeordneten Elemente von `node` aus.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.dirxml(node)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Das Ergebnis des Console.dirxml()-Beispiels" lightbox="../media/console-demo-dirxml-button.msft.png":::
         Das Ergebnis des `console.dirxml()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a>Fehler  

Diese Methode druckt `object` die in die **Konsole,** formatiert sie als Fehler und enthält eine Stapelverfolgung.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.error(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Das Ergebnis des Beispiels console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         Das Ergebnis des `console.error()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a>Gruppe  

Diese Methode gruppieren Nachrichten visuell, bis [die groupEnd-Methode](#groupend) verwendet wird.  Verwenden Sie die [groupCollapsed-Methode,](#groupcollapsed) um die Gruppe zu reduzieren, wenn sie sich zunächst bei der Konsole **anmeldet.**  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const label = 'Adolescent Irradiated Espionage Tortoises';
      console.group(label);
      console.info('Leo');
      console.info('Mike');
      console.info('Don');
      console.info('Raph');
      console.groupEnd(label);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Das Ergebnis des Beispiels console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         Das Ergebnis des `console.group()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

Diese Methode ist identisch mit der [Protokollmethode,](#log) mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn sie sich bei der Konsole **anmeldet.**  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a>groupEnd  

Diese Methode beendet das visuelle Gruppieren von Nachrichten.  Navigieren Sie zur [Gruppenmethode.](#group)  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a>Info  

Diese Methode ist identisch mit der [Protokollmethode.](#log)  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.info(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Das Ergebnis des beispiels console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         Das Ergebnis des `console.info()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a>log  

Diese Methode druckt eine Nachricht an die **Konsole**.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.log(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Das Ergebnis des Beispiels console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         Das Ergebnis des `console.log()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>Tabelle  

Diese Methode protokolliert ein Array von Objekten als Tabelle.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.table(array)
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
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
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Das Ergebnis des Beispiels console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         Das Ergebnis des `console.table()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a>time  

Diese Methode startet einen neuen Timer.  Verwenden Sie die [timeEnd-Methode,](#timeend) um den Timer zu beenden und die verstrichene Zeit in der Konsole **zu drucken.**  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.time();
      for (var i = 0; i < 100000; i++) {
          let square = i ** 2;
      }
      console.timeEnd();
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Das Ergebnis des Beispiels console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         Das Ergebnis des `console.time()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a>timeEnd  

Mit dieser Methode wird ein Timer angehalten.  Weitere Informationen finden Sie in der [Time-Methode.](#time)  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.timeEnd([label])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

---  

## <a name="trace"></a>trace  

Diese Methode druckt eine Stapelverfolgung an die **Konsole**.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.trace()
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const first = () => { second(); };
      const second = () => { third(); };
      const third = () => { fourth(); };
      const fourth = () => { console.trace(); };
      first();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Das Ergebnis des Beispiels console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         Das Ergebnis des `console.trace()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a>warnen  

Diese Methode druckt eine Warnung an die **Konsole**.  

### <a name="javascript-syntax"></a>#A0  

```javascript
console.warn(object [, object, ...])
```  

[Protokollebene][DevtoolsConsoleReferencePersist]: `Warning`  

### <a name="javascript-example"></a>JavaScript-Beispiel  

:::row:::
   :::column span="1":::
      Eingabe  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Ausgabe
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Das Ergebnis des Console.warn()-Beispiels" lightbox="../media/console-demo-warn-button.msft.png":::
         Das Ergebnis des `console.warn()` Beispiels  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Löschen der Konsole – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Nachrichten über Seitenlasten hinweg beibehalten – Konsolenreferenz | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools (Übersicht) | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
