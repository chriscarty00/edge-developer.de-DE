---
description: Alle Möglichkeiten zum Öffnen des Microsoft Edge-devtools
title: Öffnen von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ffc05a1eff2cdb7f3020a7dbb853a7520a0502dd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993597"
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

Mit den folgenden Aufgaben können Sie die Formatvorlagen oder Attribute eines DOM-Knotens überprüfen.

*   Zeigen Sie auf das Element, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
*   Drücken Sie `Control` + `Shift` + `C` \ (Windows \) oder `Command` + `Option` + `C` \ (macOS \).  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="Die Option * * Inspect * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   Die Option "über **prüfen** "  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Öffnen des Konsolen Panels  

Mit den folgenden Aufgaben können Sie den [Konsolen][DevToolsConsoleIndex] Bereich öffnen, um aufgezeichnete Nachrichten anzuzeigen oder JavaScript auszuführen.  

*   Führen Sie die folgenden Schritte aus, um den [Konsolen][DevToolsConsoleIndex] Bereich zu öffnen.  
    
    1.  [Öffnen Sie devtools](#open-microsoft-edge-devtools).  
    1.  Wählen Sie den [Konsolen][DevToolsConsoleIndex] Bereich aus.  

*   Wenn Sie direkt in den [Konsolen][DevToolsConsoleIndex] Bereich springen möchten, drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Öffnen des vorherigen Panels  

Wenn Sie zum vorherigen geöffneten Fenster springen möchten, drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  

## Öffnen von Microsoft Edge devtools  

Mit den folgenden Aufgaben können Sie devtools öffnen.  

*   Führen Sie die folgenden Schritte aus, um Microsoft Edge devtools zu öffnen.  
    
    1.  Wählen Sie das  `...` Symbol \ (die **Einstellungen und** das Symbol "Weitere" \) aus.  
    1.  Wählen Sie **Weitere Tools**aus.  
    1.  Wählen Sie **Entwickler Tools**aus.  
    
*   Um Microsoft Edge devtools zu öffnen, drücken Sie `F12` oder `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Öffnen von devtools über das Haupt Menü von Microsoft Edge" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Öffnen von devtools über das Haupt Menü von Microsoft Edge  
:::image-end:::  

## Automatisches Öffnen von devtools auf jeder neuen Registerkarte  

Wenn Sie devtools auf jeder neuen Registerkarte automatisch öffnen möchten, öffnen Sie Microsoft Edge über die Befehlszeile, und übergeben Sie die `--auto-open-devtools-for-tabs` Kennzeichnung.  

#### [CMD (Windows)](#tab/cmd-windows/)  

<a id="selenium-tools-install"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-windows/)  

<a id="selenium-tools-install"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [bash (macOS)](#tab/bash-macos/)  

<a id="selenium-tools-install"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

* * *  

<!-- links -->  

[DevToolsConsoleIndex]: ./console/index.md "Übersicht über die Konsole | Microsoft docs"  
[DevtoolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen – Microsoft docs"  

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
