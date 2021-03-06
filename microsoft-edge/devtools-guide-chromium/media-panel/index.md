---
description: Verwenden Sie das Medientool, um Informationen anzuzeigen und die Media Player pro Browserregisterkarte zu debuggen.
title: Anzeigen und Debuggen von Informationen zu Media Playern
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 7680faa13f65a2ea6f0a8b085316b5ed67bfdaba
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398406"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="view-and-debug-media-players-information"></a>Anzeigen und Debuggen von Informationen zu Media Playern  

Verwenden Sie **das Medientool** in Microsoft Edge DevTools, um Informationen anzuzeigen und die Media Player pro Browserregisterkarte zu debuggen.  

## <a name="open-the-media-tool"></a>Öffnen des Medientools  

Das **Medientool** ist der wichtigste Ort in DevTools zum Überprüfen des Media Players einer Webseite.

1.  [Öffnen Sie DevTools][DevtoolsGuideChromiumOpen].  
1.  Zum Öffnen des **Medienbereichs** wählen **Sie Anpassen und Steuern devTools** `...`  >  **Weitere Tools**  >  **Medien aus.**  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Medienbereich" lightbox="../media/media-panel-empty.msft.png":::
       **Medienbereich**  
    :::image-end:::  
    
## <a name="view-media-players-information"></a>Anzeigen von Informationen zu Media Playern  

1.  Navigieren Sie zu einer Webseite mit einem Media Player, z. B. der folgenden Webseite.  
    
    [Maximieren der Produktivität mit den Edge-Entwicklertools][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  Im Menü **Player** wird ein Media Player angezeigt.  
1.  Wählen Sie den Spieler aus.  Im **Bereich** Eigenschaften werden die Eigenschaften des Media Players angezeigt.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Medieneigenschaften" lightbox="../media/media-panel-view.msft.png":::
       Medieneigenschaften  
    :::image-end:::  
    
1.  Um alle Media Player-Ereignisse anzeigen zu können, wählen Sie den **Bereich Ereignisse** aus.  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Medienereignisse" lightbox="../media/media-panel-events.msft.png":::
       Medienereignisse  
    :::image-end:::  
    
1.  Wählen Sie zum Anzeigen der Media Player-Nachrichtenprotokolle den **Bereich Nachrichten** aus.  Sie können die Nachrichten nach Protokollebene oder Zeichenfolge filtern.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mediennachrichten" lightbox="../media/media-panel-messages.msft.png":::
       Mediennachrichten  
    :::image-end:::  
    
1.  Im **Zeitachsenbereich** werden die Medienwiedergabe und der Pufferstatus live angezeigt.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Medienzeitachse" lightbox="../media/media-panel-timeline.msft.png":::
       Medienzeitachse  
    :::image-end:::  
    
### <a name="remote-debugging"></a>Remotedebugging  

Zeigen Sie die Media Player-Informationen auf einem Android-Gerät von Ihrem Windows- oder macOS-Computer an.  

1.  Navigieren Sie zum Einrichten des Remotedebu debuggings zu [Erste Schritte mit Remotedebugen von Android-Geräten.][DevtoolsGuideChromiumRemoteDebuggingIndex]  
1.  Zeigen Sie die Media Player-Informationen remote an.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a>Ausblenden und Anzeigen von Media Playern  

Manchmal führen Sie mehrere Media Player auf einer Webseite aus, oder verwenden Sie die gleiche Browserregisterkarte, um verschiedene Webseiten zu durchsuchen, jeweils mit Media Playern.

Sie können festlegen, dass \(oder show\) jeder Media Player ausgeblendet werden soll, um ein einfacheres Debuggen zu ermöglichen.  

1.  Navigieren Sie mit derselben Browserregisterkarte zu mehreren verschiedenen Videoweb webseiten.  
1.  Führen Sie eine der folgenden Aktionen aus, um Media Player auszublenden.  
    *   Um einen Media Player auszublenden, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Player ausblenden aus.**  
    *   Um alle anderen Media Player auszublenden, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Alle anderen **ausblenden aus.**  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ausblenden von Media Playern" lightbox="../media/media-panel-hide-show.msft.png":::
       Ausblenden von Media Playern  
    :::image-end:::  
    
## <a name="export-media-player-information"></a>Exportieren von Media Player-Informationen  

1.  Wenn Sie die Media Player-Informationen als JSON-Datei herunterladen möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Playerinformationen speichern aus.**  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportieren von Medieninformationen" lightbox="../media/media-panel-save.msft.png":::
       Exportieren von Medieninformationen  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximieren der Produktivität mit den Edge-Entwicklertools | Bing Video"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

