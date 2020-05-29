---
title: Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601747"
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

> ##### Abbildung1  
> Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript  
> ![Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript][ImageDisableJS]  

## Öffnen des Befehlsmenüs   

Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \). Oder klicken Sie auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Befehl ausführen**aus.  

> ##### Abbildung2  
> Befehl "ausführen"  
> ![Befehl "ausführen"][ImageRunCommand]  

## Anzeigen der anderen verfügbaren Aktionen   

Wenn Sie den Workflow verwenden, der unter [Öffnen des Befehls](#open-the-command-menu)Menüs erläutert wird, wird das Befehl-Menü mit einem `>` Zeichen, das dem Befehlsmenü-Textfeld vorangestellt wird, geöffnet.  

> ##### Abbildung 3  
> Das Befehlszeichen  
> ![Das Befehlszeichen][ImageCommandCharacter]  

Löschen `>` Sie das Zeichen und den Typ `?` , um andere Aktionen anzuzeigen, die über das Befehlsmenü verfügbar sind.  

> ##### Abbildung4  
> Andere verfügbare Aktionen  
> ![Andere verfügbare Aktionen][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Abbildung 1: Verwenden des Befehlsmenüs zum Deaktivieren von JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Abbildung 2: Befehl "ausführen""  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Abbildung 3: das Befehlszeichen"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Abbildung 4: Weitere verfügbare Aktionen"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Deaktivieren von JavaScript mit Microsoft Edge devtools"  

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
