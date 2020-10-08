---
description: Wenn Sie feststellen, dass Sie dieselben JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie stattdessen, Live Ausdrücke zu verwenden.
title: Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6b66c44b77cd50bc0c1575e5eceb7c8d1a01b709
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993114"
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





# Sehen Sie sich die Werte für JavaScript-Ausdrücke in Echtzeit mit Live Ausdrücken an   

  

Wenn Sie feststellen, dass Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Live Ausdruck**zu erstellen.  Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein und anheften ihn dann an den Anfang der Konsole.  Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.  

## Erstellen eines Live Ausdrucks   

1.  [Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].  
1.  Klicken Sie auf **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateLiveExpressionIcon] \).  Das Textfeld " **Live Ausdruck** " wird angezeigt.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von Document. activeElement in das Textfeld &quot;Live Ausdruck&quot;" lightbox="../media/console-create-live-expression.msft.png":::
       Eingeben `document.activeElement` in das Textfeld " **Live Ausdruck** "  
    :::image-end:::  
    
1.  Geben `Control` + `Enter` Sie \ (Windows \) oder `Command` + `Enter` \ (macOS \) ein, um den Ausdruck zu speichern, oder klicken Sie außerhalb des Textfeldes **Live Ausdruck** .  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Console-Console-Referenz öffnen | Microsoft docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
