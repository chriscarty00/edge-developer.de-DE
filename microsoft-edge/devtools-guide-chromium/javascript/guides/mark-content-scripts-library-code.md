---
description: Aktivieren Sie "Markieren von Inhaltsskripts als Bibliothekscode" unter Einstellungen > Framework Library Code.
title: Markieren von Inhaltsskripts als Bibliothekscode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c1571ab909aac09e4593413e96f7d4b7723c7759
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519345"
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

# <a name="mark-content-scripts-as-library-code"></a>Markieren von Inhaltsskripts als Bibliothekscode  

Wenn Sie das Tool **Quellen** verwenden, um Code zu [durchschritten,][DevToolsJavascriptStepThroughCode]unterbrechen Sie manchmal code, den Sie nicht erkennen.  Wahrscheinlich haben Sie den Code für eine der installierten Microsoft Edge-Erweiterungen angehalten.  Führen Sie die folgenden Aktionen aus, um den Erweiterungscode nicht anzuhalten.  

1.  Wählen Sie in DevTools oben rechts das Zahnradsymbol ( Einstellungen )**aus.**  Die Seite **Einstellungen** wird angezeigt.  
1.  Wählen **Sie unter Einstellungen**die Option Liste ignorieren **aus.**  Der **Abschnitt Framework Library Code** in **Einstellungen** wird angezeigt.  
1.  Aktivieren Sie das **Kontrollkästchen Inhaltsskripts als Bibliothekscode** markieren.  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Aktivieren des Kontrollkästchens Inhaltsskripts als Bibliothekscode markieren" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Aktivieren des **Kontrollkästchens Inhaltsskripts als Bibliothekscode** markieren  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: Schritt durch den Code – Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
