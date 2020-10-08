---
description: Leitfaden zum Öffnen des Befehlsmenüs, Ausführen von Befehlen, Anzeigen anderer Aktionen und vieles mehr.
title: Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 54dead492e7d58053efab77c82a10e7e3c912460
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993198"
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





# Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools   

  

Das Befehlsmenü bietet eine schnelle Möglichkeit, auf der Benutzeroberfläche von Microsoft Edge devtools zu navigieren und häufige Aufgaben wie das [Deaktivieren von JavaScript][JavascriptDisable]durchzuführen.  Möglicherweise sind Sie mit einem ähnlichen Feature in Visual Studio-Code vertraut, der als [Befehls Palette][VisualStudioCodeUICommandPalette]bezeichnet wird, was die ursprüngliche Inspiration für das Befehlsmenü war.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript  
:::image-end:::  

## Öffnen des Befehlsmenüs   

Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \). Oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Befehl ausführen**aus.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-options-run-command.msft.png":::
   Befehl "ausführen"  
:::image-end:::  

## Anzeigen der anderen verfügbaren Aktionen   

Wenn Sie den Workflow verwenden, der unter [Öffnen des Befehls](#open-the-command-menu)Menüs erläutert wird, wird das Befehl-Menü mit einem `>` Zeichen vor der vorangestellt des Befehlsmenü-Textfelds geöffnet.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command.msft.png":::
   Das Befehlszeichen  
:::image-end:::  

Löschen `>` Sie das Zeichen und den Typ `?` , um andere Aktionen anzuzeigen, die über das Befehlsmenü verfügbar sind.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-help.msft.png":::
   Andere verfügbare Aktionen  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools | Microsoft docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio-Code-UI"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
