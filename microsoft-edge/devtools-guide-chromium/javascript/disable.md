---
title: Deaktivieren von JavaScript mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 587f4780432b1b2b964462d2d7f5779f447f1313
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982916"
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





# Deaktivieren von JavaScript mit Microsoft Edge devtools   



, Um zu sehen, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist.  

1.  [Öffnen Sie Microsoft Edge devtools][DevToolsOpen].  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Beginnen `javascript` Sie mit der Eingabe, wählen Sie **JavaScript deaktivieren**aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.  JavaScript ist jetzt deaktiviert.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       Wählen Sie im **Befehlsmenü** **JavaScript deaktivieren** aus.  
    :::image-end:::  
    
    Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol nebenquellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Das Warnungssymbol neben **Quellen**  
    :::image-end:::  
    
JavaScript bleibt auf dieser Registerkarte so lange deaktiviert, wie Sie devtools geöffnet haben.  

Möglicherweise möchten Sie die Seite neu laden, um festzustellen, ob und wie die Seite beim Laden von JavaScript abhängig ist.  

Führen Sie die folgenden Aktionen aus, um JavaScript wieder zu aktivieren.  

*   Öffnen Sie das **Befehl-Menü** erneut, und führen Sie den Befehl aus `Enable JavaScript` .  
*   Schließen Sie devtools.  

<!--  
## Feedback   


-->  

<!-- links -->  

[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
