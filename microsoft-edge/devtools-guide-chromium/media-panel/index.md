---
description: Verwenden Sie das Medienfenster, um Informationen anzuzeigen und die Media Player pro Browser-Registerkarte zu debuggen.
title: Anzeigen und Debuggen von Medienplayer-Informationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105195"
---
# Anzeigen und Debuggen von Medienplayer-Informationen  

Verwenden Sie das **Medien** Fenster in Microsoft Edge devtools, um Informationen anzuzeigen und die Media Player pro Browser-Registerkarte zu debuggen.  

## Öffnen des Medien Panels  

Der **Medien** Bereich ist der wichtigste Ort in devtools, um den Media Player einer Webseite zu überprüfen.

1.  [Öffnen Sie devtools][DevtoolsGuideChromiumOpen].  
1.  Um das **Medien** Panel zu öffnen, wählen Sie **anpassen und Steuern devtools** `...`  >  **Weitere Tools**  >  **Medien**aus.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-empty.msft.png":::
       **Medien** Panel  
    :::image-end:::  
    
## Anzeigen von Informationen zu Medien Teilnehmern  

1.  Navigieren Sie zu einer Webseite mit einem Media Player, beispielsweise der folgenden Website.  
    
    [Maximieren der Produktivität mit den Edge-Entwickler Tools][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  Unter dem **Player** -Menü wird ein Media-Player angezeigt.  
1.  Wählen Sie den Player aus.  Auf der Registerkarte " **Eigenschaften** " werden die Eigenschaften des Media Players angezeigt.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-view.msft.png":::
       Medieneigenschaften  
    :::image-end:::  
    
1.  Wenn Sie alle Media Player-Ereignisse anzeigen möchten, wählen Sie die Registerkarte **Ereignisse** aus.  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-events.msft.png":::
       Medienereignisse  
    :::image-end:::  
    
1.  Um die Media Player-Nachrichtenprotokolle anzuzeigen, wählen Sie die Registerkarte **Nachrichten** aus.  Sie können die Nachrichten nach Protokollebene oder Zeichenfolge filtern.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-messages.msft.png":::
       Medien Nachrichten  
    :::image-end:::  
    
1.  Auf der Registerkarte **Zeitachse** werden die Medienwiedergabe und der Pufferstatus Live angezeigt.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-timeline.msft.png":::
       Medienzeitachse  
    :::image-end:::  
    
### Remotedebugging  

Zeigen Sie die Medienwiedergabe Informationen auf einem Android-Gerät von Ihrem Windows-oder macOS-Computer aus an.  

1.  Wenn Sie das Remotedebuggen einrichten möchten, navigieren Sie zu den [ersten Schritten mit dem Remotedebuggen von Android-Geräten][DevtoolsGuideChromiumRemoteDebuggingIndex].  
1.  Anzeigen der Medienplayer-Informationen per Remotezugriff  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Ausblenden und Anzeigen von Media Playern  

Manchmal führen Sie mehr als einen Media Player auf einer Webseite aus, oder Sie verwenden dieselbe Browserregister Karte, um verschiedene Webseiten zu durchsuchen, die jeweils mit Media Playern angezeigt werden.

Sie können festlegen, dass die einzelnen Media Player ausgeblendet werden, um das Debugging zu vereinfachen.  

1.  Navigieren Sie mit der gleichen Browserregister Karte zu verschiedenen Video Webseiten.  
1.  Wenn Sie Medienplayer ausblenden möchten, führen Sie eine der folgenden Aktionen aus.  
    *   Wenn Sie einen Media Player ausblenden möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Player ausblenden**aus.  
    *   Wenn Sie alle anderen Media Player ausblenden möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **alle anderen ausblenden**aus.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-hide-show.msft.png":::
       Ausblenden von Media Playern  
    :::image-end:::  
    
## Exportieren von Media Player-Informationen  

1.  Wenn Sie die Media Player-Informationen als JSON-Datei herunterladen möchten, zeigen Sie auf einen Media Player, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Player-Informationen speichern**aus.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Medien Panel" lightbox="../media/media-panel-save.msft.png":::
       Exportieren von Medieninformationen  
    :::image-end:::  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Öffnen von Microsoft Edge devtools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximieren der Produktivität mit den Edge-Entwickler Tools | Bing-Video"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

