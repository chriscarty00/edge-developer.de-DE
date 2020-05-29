---
title: Anzeigen von Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612074"
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





# Anzeigen von Cache Daten mit Microsoft Edge devtools   



Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Cache][MDNCache] Daten zu überprüfen.  

Wenn Sie versuchen, http- [Cache][MDNHTTPCaching] -Daten zu überprüfen, ist dies nicht die gewünschte Richtlinie.  
Suchen Sie in der Spalte **Größe** des **Netzwerkprotokolls**nach den Informationen.  Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].  

## Anzeigen von Cachedaten   

1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.  
    
    > ##### Abbildung1  
    > Bereich ' Manifest '  
    > ![Bereich ' Manifest '][ImageManifestPane]  

1.  Erweitern Sie den Abschnitt **Cache Speicher** , um verfügbare Caches anzuzeigen.  
    
    > ##### Abbildung2  
    > Verfügbare Caches  
    > ![Verfügbare Caches][ImageCache]  

1.  Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.  
    
    > ##### Abbildung 3  
    > Anzeigen des Inhalts eines Caches  
    > ![Anzeigen des Inhalts eines Caches][ImageCacheView]  

1.  Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzuzeigen.  
    
    > ##### Abbildung4  
    > Anzeigen der HTTP-Header einer Ressource  
    > ![Anzeigen der HTTP-Header einer Ressource][ImageViewCacheResource]  

1.  Wählen Sie **Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.  
    
    > ##### Abbildung5  
    > Anzeigen des Inhalts einer Ressource  
    > ![Anzeigen des Inhalts einer Ressource][ImageCacheContent]  

## Aktualisieren einer Ressource   

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Wählen Sie die Ressource aus, die Sie aktualisieren möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    > ##### Abbildung6  
    > Auswählen einer Ressource  
    > ![Auswählen einer Ressource][ImageCacheSelected]  

1.  Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .  

## Filtern von Ressourcen   

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Verwenden Sie das Textfeld nach **Pfad filtern** , um alle Ressourcen zu filtern, die nicht dem von Ihnen bereitgestellten Pfad entsprechen.  
    
    > ##### Abbildung7  
    > Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen  
    > ![Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen][ImageCacheFilter]  

## Löschen einer Ressource   

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Wählen Sie die Ressource aus, die Sie löschen möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    > ##### Abbildung8  
    > Auswählen einer Ressource  
    > ![Auswählen einer Ressource][ImageCacheSelected2]  

1.  Wählen Sie **ausgewählte** löschen ausgewählt löschen aus ![ ][ImageDeleteIcon] .  

## Löschen aller Cachedaten   

1.  Öffnen Sie die **Anwendung**  >  **Clear Storage**.  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Cache Speicher** aktiviert ist.  
    
    > ##### Abbildung 9  
    > Das Kontrollkästchen " **Cache Speicher** "  
    > ![Das Kontrollkästchen "Cache Speicher"][ImageCacheCheckbox]  

1.  Wählen Sie **Website Daten löschen**aus.  
    
    > ##### Abbildung 10  
    > Schaltfläche " **Website Daten löschen** "  
    > ![Schaltfläche "Website Daten löschen"][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Abbildung 2: verfügbare Caches"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Abbildung 3: Anzeigen des Inhalts eines Caches"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Abbildung 4: Anzeigen der HTTP-Header einer Ressource"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Abbildung 5: Anzeigen des Inhalts einer Ressource"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Abbildung 6: Auswählen einer Ressource"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Abbildung 7: Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Abbildung 8: Auswählen einer Ressource"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Abbildung 9: das Kontrollkästchen "Cache Speicher""  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Abbildung 10: die Schaltfläche "Website Daten löschen""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Protokollieren von Netzwerkaktivitäten"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
