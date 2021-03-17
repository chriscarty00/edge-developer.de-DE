---
description: Wenn Sie die gleichen JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie es stattdessen mit Live-Ausdrücken.
title: Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Liveausdrücken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: af920de1c395489dc09b83f3cc0f24814c4f5cbe
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439226"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a>Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Liveausdrücken  

Wenn Sie denselben JavaScript-Ausdruck wiederholt in der Konsole eingeben, ist es möglicherweise einfacher, einen **Liveausdruck zu erstellen.**  Mit **Live-Ausdrücken** geben Sie einen Ausdruck einmal ein undheften ihn dann an den oberen Rand der Konsole.  Der Wert des Ausdrucks wird nahezu in Echtzeit aktualisiert.  

## <a name="create-a-live-expression"></a>Erstellen eines Liveausdrucks  

1.  [Öffnen Sie die Konsole][DevToolsConsoleReferenceOpenConsole].  
1.  Wählen **Sie Liveausdruck** erstellen \( ![ Liveausdruck ](../media/create-live-expression-icon.msft.png) erstellen \).  Das **Textfeld Live-Ausdruck** wird angezeigt.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Eingeben von document.activeElement in das Textfeld Live Expression" lightbox="../media/console-create-live-expression.msft.png":::
       Eingeben `document.activeElement` in das Textfeld **Live Expression**  
    :::image-end:::  
    
1.  Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, **** um den Ausdruck zu speichern, oder wählen Sie außerhalb des Textfelds Live expression aus.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Öffnen Sie die Konsole – Konsolenreferenz | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
