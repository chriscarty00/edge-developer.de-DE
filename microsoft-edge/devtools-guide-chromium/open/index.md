---
description: Alle Möglichkeiten zum Öffnen des Microsoft Edge-devtools
title: Öffnen von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d21ebbf0b84be757c1b7a69d36b3bd3cc8403c6d
ms.sourcegitcommit: 77c8f42cc84600c2b853b15aaaecf0749b74bb01
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2020
ms.locfileid: "11238223"
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
*   Wählen Sie `Control` + `Shift` + `C` \ (Windows, Linux \) oder `Command` + `Option` + `C` \ (macOS \) aus.  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Die Option "überprüfen"" lightbox="../media/bing-right-click-inspect.msft.png":::
   Die Option "über **prüfen** "  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Öffnen des Konsolen Panels  

Mit den folgenden Aufgaben können Sie den [Konsolen][DevtoolsConsoleIndex] Bereich öffnen, um aufgezeichnete Nachrichten anzuzeigen oder JavaScript auszuführen.  

*   Führen Sie die folgenden Schritte aus, um den [Konsolen][DevtoolsConsoleIndex] Bereich zu öffnen.  
    
    1.  [Öffnen Sie devtools](#open-microsoft-edge-devtools).  
    1.  Wählen Sie den [Konsolen][DevtoolsConsoleIndex] Bereich aus.  

*   Wenn Sie direkt in den [Konsolen][DevtoolsConsoleIndex] Bereich springen möchten, wählen Sie `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) aus.  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevtoolsShortcutsIndex].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Öffnen des vorherigen Panels  

Um zum vorherigen Panel zu wechseln, das Sie geöffnet hatten, wählen Sie `Control` + `Shift` + `I` \ (Windows, Linux \) oder `Command` + `Option` + `I` \ (macOS \) aus.  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevtoolsShortcutsIndex].  

## Öffnen von Microsoft Edge devtools  

Verwenden Sie eine der folgenden Optionen, um devtools zu öffnen.  

*   Verwenden Sie die Microsoft Edge-Benutzeroberfläche.  
    
    1.  Wählen Sie das Symbol **Einstellungen und mehr** \ ( `...` \) aus.  
    1.  Wählen Sie **Weitere Tools**aus.  
    1.  Wählen Sie **Entwickler Tools**aus.  
    
*   Verwenden Sie die Tastatur.  
    *   Wählen Sie `F12` oder `Control` + `Shift` + `I` \ (Windows, Linux \) oder `Command` + `Option` + `I` \ (macOS \) aus.  

Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Öffnen von devtools über das Haupt Menü von Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Öffnen von devtools über das Haupt Menü von Microsoft Edge  
:::image-end:::  

## Automatisches Öffnen von devtools auf jeder neuen Registerkarte  

Wenn Sie devtools auf jeder neuen Registerkarte automatisch öffnen möchten, öffnen Sie Microsoft Edge über die Befehlszeile, und übergeben Sie die `--auto-open-devtools-for-tabs` Kennzeichnung.  

### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Aktivieren oder Deaktivieren der Tastenkombination F12  

Führen Sie die folgenden Aktionen aus, um die Einstellung für die `F12` Tastenkombination zu ändern, die das devtools öffnet.  

1.  Wählen Sie das Symbol " **Einstellungen" und "Weitere** \ ( `...` \)" > **Einstellungen**aus.  
1.  Geben Sie in " **Sucheinstellungen**" ein `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="Das Öffnen des devtools, wenn die Taste F12 gedrückt wird" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       Das **Öffnen des devtools, wenn die Taste F12 gedrückt wird**  
    :::image-end:::  
    
1.  Wählen Sie **devtools öffnen aus, wenn die Taste F12 gedrückt wird** , um die Einstellung auf aus \ (oder auf \) umzuschalten.  Schalten Sie die Einstellung auf aus, um die Tastenkombination zu beenden, um `F12` devtools zu öffnen.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="Die Option "devtools öffnen, wenn die Taste F12 gedrückt wird" ist deaktiviert" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       Die Option " **devtools öffnen, wenn die Taste F12 gedrückt wird** " ist deaktiviert  
    :::image-end:::  
    
1.  Nachdem Sie die Umschaltfläche auf aus festgesetzt haben, wählen Sie aus, `F12` um zu bestätigen, dass devtools nicht mehr geöffnet wird.  
    
    > [!NOTE]
    > Nachdem Sie die **devtools öffnen, wenn die Taste F12 gedrückt wird** , um die devtools zu öffnen, führen Sie eine der folgenden Aktionen aus.  
    > 
    > *   Wählen Sie aus `Ctrl` + `Shift` + `I` .  
    > *   Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > über **prüfen**.  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/open) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
