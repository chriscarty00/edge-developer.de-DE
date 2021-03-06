---
description: Öffnen Sie das Befehlsmenü, und führen Sie den Befehl "JavaScript deaktivieren" aus.
title: Deaktivieren von JavaScript mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2067944fa17c332dd15ffb3ef97afe02d35685ed
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398560"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a>Deaktivieren von JavaScript mit Microsoft Edge DevTools  

Führen Sie die folgenden Aktionen aus, um anzuzeigen, wie eine Webseite aussieht und sich verhält, wenn JavaScript deaktiviert ist.  

1.  [Öffnen Sie Microsoft Edge DevTools][DevToolsOpen].  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/javascript-console-command.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Beginnen Sie mit der `javascript` Eingabe, wählen **Sie JavaScript deaktivieren**aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  JavaScript ist jetzt deaktiviert.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Wählen Sie im Befehlsmenü JavaScript deaktivieren aus." lightbox="../media/javascript-console-command-javascript.msft.png":::
       Wählen **Sie im Befehlsmenü JavaScript** deaktivieren **aus.**  
    :::image-end:::  
    
    Das gelbe Warnsymbol neben **Quellen** erinnert Sie daran, dass JavaScript deaktiviert ist.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Das Warnungssymbol neben Quellen" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Das Warnungssymbol neben **Quellen**  
    :::image-end:::  
    
JavaScript bleibt auf der Registerkarte deaktiviert, solange DevTools geöffnet ist.  

Möglicherweise möchten Sie die Seite aktualisieren, um zu überprüfen, ob und wie die Webseite beim Laden von JavaScript abhängt.  

Führen Sie die folgenden Aktionen aus, um JavaScript erneut zu aktivieren.  

*   Öffnen Sie **das Befehlsmenü** erneut, und führen Sie den Befehl `Enable JavaScript` aus.  
*   Schließen Sie DevTools.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
