---
description: Öffnen Sie die Konsole, erstellen Sie einen Liveausdruck, und legen Sie den Ausdruck auf document.activeElement.
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2c2040c690441fb33c802cf454dc7a1e3f33c494
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439170"
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

Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation einer Seite.  Beim Navigieren auf der Seite mit der Taste wird der Fokusring manchmal ausgeblendet, da das Element mit dem Fokus `Tab` ausgeblendet ist.  

Führen Sie die folgenden Aktionen aus, um das fokussierte Element in DevTools nachverfolgt zu haben.  

1.  Öffnen Sie die **Konsole**.  
1.  Wählen **Sie Liveausdruck** erstellen \( ![ Liveausdruck ](../media/create-live-expression-icon.msft.png) erstellen \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Liveausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Erstellen eines Liveausdrucks  
    :::image-end:::  
    
1.  Geben Sie `document.activeElement` ein.  
1.  Wählen Sie außerhalb der **zu speichernde Live** Expression-Benutzeroberfläche aus.  
    
Der unten angezeigte `document.activeElement` Wert ist das Ergebnis des Ausdrucks.  

Da dieser Ausdruck immer das fokussierte Element darstellt, haben Sie nun eine Möglichkeit, immer nachverfolgt zu werden, welches Element den Fokus hat.  

*   Zeigen Sie auf das Ergebnis, um das fokussierte Element im Viewport zu markieren.  
*   Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü **** \(klicken Sie mit der rechten Maustaste\), und wählen Sie im Bereich Elemente anzeigen aus, um das Element im DOM-Struktur im **Elementtool anzuzeigen.**  
*   Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Store als globale** Variable aus, um einen Variablenverweis auf den Knoten zu erstellen, den Sie in der Konsole verwenden **können.**  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
