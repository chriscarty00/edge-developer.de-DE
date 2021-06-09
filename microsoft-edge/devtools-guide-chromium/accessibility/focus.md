---
description: Öffnen Sie die Konsole, erstellen Sie einen Live-Ausdruck, und legen Sie den Ausdruck auf document.activeElement fest.
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2fd53caccefefb0b0bce4b5c82f30632e11a3cb6
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597108"
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
# <a name="track-which-element-has-focus"></a>Nachverfolgen, welches Element den Fokus hat  

Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation einer Seite.  Beim Navigieren auf der Seite mit der `Tab` Taste wird der Fokusring manchmal ausgeblendet, da das Element, das den Fokus hat, ausgeblendet ist.  

So verfolgen Sie das fokussierte Element in DevTools:

1.  Öffnen Sie die **Konsole**.  
1.  Wählen **Sie "Liveausdruck erstellen"** \( ![ Liveausdruck erstellen ](../media/create-live-expression-icon.msft.png) \) aus.  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Liveausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Erstellen eines Liveausdrucks  
    :::image-end:::  
    
1.  Geben Sie `document.activeElement` ein.  
1.  Um den Ausdruck zu speichern, wählen Sie außerhalb des Liveausdrucks aus.
    
Der unten angezeigte Wert `document.activeElement` ist das Ergebnis des Ausdrucks.  

Da dieser Ausdruck immer das fokussierte Element darstellt, haben Sie jetzt eine Möglichkeit, immer nachzuverfolgen, welches Element den Fokus hat.  

*   Zeigen Sie auf das Ergebnis, um das fokussierte Element im Viewport hervorzuheben.  
*   Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Einblenden" im Bereich "Elemente"** aus, um das Element in der DOM-Struktur im **Elementtool** anzuzeigen.  
*   Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Store als globale Variable** aus, um einen Variablenverweis auf den Knoten zu erstellen, den Sie in der **Konsole**verwenden können.  


## <a name="see-also"></a>Weitere Informationen:

*  [Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü](test-analyze-no-focus-indicator.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
