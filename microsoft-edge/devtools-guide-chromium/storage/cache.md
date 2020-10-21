---
description: Informationen zum Anzeigen von Cache Daten aus dem Anwendungs Panel von Microsoft Edge devtools
title: Anzeigen von Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 5ab5fd0b3b504443e495f1d5108907a4551e6ac6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125440"
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

# Anzeigen von Cachedaten mit Microsoft Edge devtools  

Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Cache][MDNCache] Daten zu überprüfen.  

Wenn Sie versuchen, http- [Cache][MDNHTTPCaching] -Daten zu überprüfen, ist dies nicht die gewünschte Richtlinie.  Suchen Sie in der Spalte **Größe** des **Netzwerkprotokolls**nach den Informationen.  Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].  

## Anzeigen von Cachedaten  

1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  
    
1.  Erweitern Sie den Abschnitt **Cache Speicher** , um verfügbare Caches anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage.msft.png":::
       Verfügbare Caches  
    :::image-end:::  
    
1.  Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Anzeigen des Inhalts eines Caches  
    :::image-end:::  
    
1.  Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Anzeigen der HTTP-Header einer Ressource  
    :::image-end:::  
    
1.  Wählen Sie **Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Anzeigen des Inhalts einer Ressource  
    :::image-end:::  
    
## Aktualisieren einer Ressource  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Wählen Sie die Ressource aus, die Sie aktualisieren möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Auswählen einer zu aktualisierden Ressource  
    :::image-end:::  
    
1.  Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.  
    
## Filtern von Ressourcen  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Verwenden Sie das Textfeld nach **Pfad filtern** , um alle Ressourcen zu filtern, die nicht dem von Ihnen bereitgestellten Pfad entsprechen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen  
    :::image-end:::  
    
## Löschen einer Ressource  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data)  
1.  Wählen Sie die Ressource aus, die Sie löschen möchten.  DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Auswählen einer zu löschenden Ressource  
    :::image-end:::  
    
1.  Wählen Sie " **Ausgewählte löschen** " aus ![ ][ImageDeleteIcon] .  
    
## Löschen aller Cachedaten  

1.  Öffnen Sie die **Anwendung**  >  **Clear Storage**.  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Cache Speicher** aktiviert ist.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Das Kontrollkästchen " **Cache Speicher** "  
    :::image-end:::  
    
1.  Wählen Sie **Website Daten löschen**aus.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Schaltfläche " **Website Daten löschen** "  
    :::image-end:::  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Protokoll Netzwerkaktivität | Microsoft docs"  

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
