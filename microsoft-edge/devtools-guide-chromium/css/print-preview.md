---
description: Öffnen Sie das Tool "Rendering", und wählen Sie Emulieren von CSS-Medien > aus.
title: Erzwingen des Druckvorschaumodus von Microsoft Edge DevTools (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 0123b7abf475212304f654c04bc232e3e96f0bda
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399078"
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

# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a>Erzwingen des Druckvorschaumodus von Microsoft Edge DevTools  

Die [Druckmedienabfrage steuert,][MDNUsingMediaQueries] wie Ihre Seite beim Drucken aussieht.  So erzwingen Sie, dass Ihre Seite in den Druckvorschaumodus wechselt:  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `rendering` Sie ein, wählen **Sie Rendering anzeigen**aus, und wählen Sie dann `Enter` aus.  
1.  Wählen **Sie unter Emulieren von CSS-Medien**die Option **Drucken aus.**  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Druckvorschaumodus" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Druckvorschaumodus  
    :::image-end:::  
    
Von hier aus können Sie Ihre CSS wie jede andere Webseite anzeigen und ändern.  Navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCSSGetStarted].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsCSSGetStarted]: ./index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von Medienabfragen | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
