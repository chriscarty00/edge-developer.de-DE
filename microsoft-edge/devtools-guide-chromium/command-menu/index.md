---
description: Eine Anleitung zum Öffnen des Befehlsmenüs, Ausführen von Befehlen, Überprüfen anderer Aktionen und vieles mehr.
title: Ausführen von Befehlen Microsoft Edge DevTools-Befehlsmenü
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 973b440a27b0c4c06ba118fc09e4162a8fa346e8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564490"
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
# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a>Ausführen von Befehlen Microsoft Edge DevTools-Befehlsmenü  

Das Befehlsmenü bietet eine schnelle Möglichkeit, Microsoft Edge DevTools-Benutzeroberfläche zu navigieren und allgemeine Aufgaben wie das Deaktivieren [von JavaScript auszuführen.][JavascriptDisable]  Möglicherweise kennen Sie ein ähnliches Feature in Microsoft Visual Studio Code, der [Befehlspalette,][VisualStudioCodeUICommandPalette]die die ursprüngliche Inspiration für das Befehlsmenü war.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript  
:::image-end:::  

## <a name="open-the-command-menu"></a>Öffnen des Befehlsmenüs  

Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\). Oder wählen **Sie Customize and Control DevTools** \( `...` \) > Run Command **aus.**  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Befehl ausführen" lightbox="../media/command-menu-options-run-command.msft.png":::
   Befehl ausführen  
:::image-end:::  

## <a name="display-other-available-actions"></a>Anzeigen anderer verfügbarer Aktionen  

Wenn Sie den unter [Öffnen](#open-the-command-menu)des Befehlsmenüs beschriebenen Workflow verwenden, wird das Befehlsmenü mit einem Zeichen geöffnet, das im Textfeld Befehlsmenü `>` vorkonfiguriert ist.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Das Befehlszeichen" lightbox="../media/command-menu-run-command.msft.png":::
   Das Befehlszeichen  
:::image-end:::  

Löschen Sie `>` das Zeichen und den `?` Typ, um andere Aktionen anzuzeigen, die im Befehlsmenü verfügbar sind.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Andere verfügbare Aktionen" lightbox="../media/command-menu-help.msft.png":::
   Andere verfügbare Aktionen  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deaktivieren von JavaScript mit Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio Code Benutzeroberfläche"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
