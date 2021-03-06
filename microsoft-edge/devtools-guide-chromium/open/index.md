---
description: Alle Möglichkeiten zum Öffnen von Microsoft Edge DevTools.
title: Öffnen von Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 770a9d3e7a0eaaecf322d2ca847d971d1ad11b9a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398266"
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

# <a name="open-microsoft-edge-devtools"></a>Öffnen von Microsoft Edge DevTools  

Es gibt viele Möglichkeiten, Microsoft Edge DevTools zu öffnen, da unterschiedliche Benutzer schnellen Zugriff auf verschiedene Teile der DevTools-Benutzeroberfläche wünschen.  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Öffnen Sie den Bereich Elemente, um das DOM oder die CSS zu überprüfen.  

Mit jeder der folgenden Aufgaben können Sie die Formatvorlagen oder Attribute eines DOM-Knotens überprüfen.

*   Zeigen Sie auf das Element, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Überprüfen aus.**  
*   Wählen `Control` + `Shift` + `C` Sie \(Windows, Linux\) oder `Command` + `Option` + `C` \(macOS\) aus.  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Die Option Inspect" lightbox="../media/bing-right-click-inspect.msft.png":::
   Die **Option Inspect**  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Öffnen des Konsolenbereichs  

Mit jeder der folgenden Aufgaben [][DevtoolsConsoleIndex] können Sie den Konsolenbereich öffnen, um protokollierte Nachrichten anzuzeigen oder JavaScript auszuführen.  

*   Verwenden Sie die folgenden Schritte, um den [Konsolenbereich zu][DevtoolsConsoleIndex] öffnen.  
    
    1.  [Öffnen Sie DevTools](#open-microsoft-edge-devtools).  
    1.  Wählen Sie den [Bereich Konsole][DevtoolsConsoleIndex] aus.  

*   Um direkt in den [Konsolenbereich zu][DevtoolsConsoleIndex] springen, wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Öffnen des vorherigen Panels  

Um zum vorherigen Bereich zu springen, den Sie geöffnet haben, wählen Sie `Control` + `Shift` + `I` \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\).  Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

## <a name="open-microsoft-edge-devtools"></a>Öffnen von Microsoft Edge DevTools  

Verwenden Sie eine der folgenden Optionen, um DevTools zu öffnen.  

*   Verwenden Sie die Microsoft Edge-Benutzeroberfläche.  
    
    1.  Wählen Sie **das Symbol Einstellungen und mehr** \( `...` \) > Weitere **Tools**Developer  >   **Tools aus.**  
    
*   Verwenden Sie die Tastatur.  
    *   Wählen `F12` Oder `Control` + `Shift` + `I` \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\).  

Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Öffnen von DevTools über das Microsoft Edge-Hauptmenü" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Öffnen von DevTools über das Microsoft Edge-Hauptmenü  
:::image-end:::  

## <a name="auto-open-devtools-on-every-new-tab"></a>Automatisches Öffnen von DevTools auf jeder neuen Registerkarte  

Zum automatischen Öffnen von DevTools auf jeder neuen Registerkarte öffnen Sie Microsoft Edge über die Befehlszeile, und übergeben Sie das `--auto-open-devtools-for-tabs` Flag.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Ein- oder Ausschalten der F12-Tastenkombination  

Führen Sie die folgenden Aktionen aus, um die Tastenkombinationseinstellung zu ändern, mit der `F12` die DevTools geöffnet werden.  

1.  Wählen Sie das Symbol **Einstellungen und mehr** \( `...` \) symbol > Einstellungen **aus.**  
1.  Geben **Sie unter Sucheinstellungen** `Developer Tools` ein.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="Öffnen Sie die DevTools, wenn die F12-TASTE gedrückt wird." lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       Öffnen **Sie die DevTools, wenn die F12-TASTE gedrückt** wird.  
    :::image-end:::  
    
1.  Wählen **Sie DevTools öffnen aus, wenn die F12-Taste** gedrückt wird, um die Einstellung auf \(oder ein\) zu schalten.  Umschalten Sie die Einstellung auf aus, um zu `F12` verhindern, dass die Tastenkombination DevTools öffnet.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="The Open the DevTools when the F12 key is pressed setting is turned off" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       The **Open the DevTools when the F12 key is pressed** setting is turned off  
    :::image-end:::  
    
1.  Nachdem Sie den Umschalter auf deaktiviert festgelegt haben, wählen Sie aus, um `F12` zu bestätigen, dass DevTools nicht mehr geöffnet ist.  
    
    > [!NOTE]
    > Nachdem Sie die Einstellung DevTools öffnen deaktiviert haben, wenn die **F12-TASTE** gedrückt wird, führen Sie eine der folgenden Aktionen aus, um die DevTools zu öffnen.  
    > 
    > *   Wählen Sie `Ctrl` + `Shift` + `I` aus.  
    > *   Öffnen Sie das Kontextmenü \(mit der rechten Maustaste\) > **Überprüfen**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/open) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
