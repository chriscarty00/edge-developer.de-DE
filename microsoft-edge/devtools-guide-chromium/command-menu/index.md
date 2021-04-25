---
description: Eine Anleitung zum Öffnen des Befehlsmenüs, Ausführen von Befehlen, Überprüfen anderer Aktionen und vieles mehr.
title: Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b815934da73f9f023629564da7bea14da166ff9b
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519191"
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

# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a>Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü  

Das Befehlsmenü bietet eine schnelle Möglichkeit, die Microsoft Edge DevTools-Benutzeroberfläche zu navigieren und allgemeine Aufgaben auszuführen, z. B. das Deaktivieren [von JavaScript][JavascriptDisable].  Möglicherweise kennen Sie ein ähnliches Feature in Microsoft Visual Studio Code, die [Befehlspalette][VisualStudioCodeUICommandPalette], die die ursprüngliche Inspiration für das Befehlsmenü war.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript  
:::image-end:::  

## <a name="open-the-command-menu"></a>Öffnen des Befehlsmenüs  

Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus. Oder wählen **Sie Customize and Control DevTools** \( `...` \) > Run Command **aus.**  

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

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Befehlspalette – Visual Studio Codebenutzeroberfläche"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
