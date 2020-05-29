---
title: Öffnen von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601887"
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
   limitations under the License. -->





# Öffnen von Microsoft Edge devtools   



Es gibt viele Möglichkeiten, Microsoft Edge devtools zu öffnen, da unterschiedliche Benutzer schnellen Zugriff auf verschiedene Teile der devtools-Benutzeroberfläche wünschen.  

## Öffnen des Elements Panels zum Überprüfen des DOM oder CSS   

Wenn Sie die Formatvorlagen oder Attribute eines DOM-Knotens überprüfen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen**aus.  

> ##### Abbildung1  
> Die Option "über **prüfen** "  
> ![Die Option "überprüfen"][ImageInspectOption]  

Oder drücken Sie `Control` + `Shift` + `C` \ (Windows \) oder `Command` + `Option` + `C` \ (macOS \).  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Öffnen des Konsolen Panels zum Anzeigen von protokollierten Nachrichten oder Ausführen von JavaScript   

Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um direkt in den **Konsolen** Fenster zu wechseln.  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Öffnen des letzten geöffneten Panels   

Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).  

## Öffnen von devtools über das Haupt Menü von Microsoft Edge  

Klicken Sie auf **Einstellungen und mehr \ (Alt + F \)** `...` , und wählen Sie dann **Weitere Tools**-  >  **Entwicklertools**aus.  

> ##### Abbildung2  
> Öffnen von devtools über das Microsoft Edge-Hauptmenü  
> ![Öffnen von devtools über das Microsoft Edge-Hauptmenü][ImageOpenFromMain]  

## Automatisches Öffnen von devtools auf jeder neuen Registerkarte   

Öffnen Sie Microsoft Edge über die Befehlszeile, und übergeben Sie die `--auto-open-devtools-for-tabs` Kennzeichnung.  

Windows \ (cmd \):  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

Windows \ (PowerShell \):  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

macOS  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Abbildung 1: die Option "überprüfen""  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Abbildung 2: Öffnen von devtools aus dem Microsoft Edge-Hauptmenü"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/open) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
