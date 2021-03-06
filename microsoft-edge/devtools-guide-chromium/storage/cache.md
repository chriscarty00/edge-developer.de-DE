---
description: Anzeigen von Cachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Cachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 7e0523e3293bbdafa9c3575344714da708fffe62
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397538"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a>Anzeigen von Cachedaten mit Microsoft Edge DevTools  

In diesem Handbuch wird gezeigt, wie [Sie Microsoft Edge DevTools zum Überprüfen][MicrosoftEdgeDevTools] von [Cachedaten][MDNCache] verwenden.  

Wenn Sie versuchen, HTTP-Cachedaten [zu][MDNHTTPCaching] überprüfen, ist dies nicht die von Ihnen personenbezogene Anleitung.  Suchen Sie in der Spalte **Größe** des Netzwerkprotokolls **nach den Informationen.**  Navigieren Sie zu [Netzwerkaktivität protokollieren.][DevtoolsNetworkLogActivity]  

## <a name="view-cache-data"></a>Anzeigen von Cachedaten  

1.  Wählen Sie die **Registerkarte Anwendung** aus, um den Bereich **Anwendung zu** öffnen.  Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  
    
1.  Erweitern Sie den **Abschnitt Cachespeicher,** um verfügbare Caches anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Verfügbare Caches" lightbox="../media/storage-application-cache-storage.msft.png":::
       Verfügbare Caches  
    :::image-end:::  
    
1.  Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Anzeigen des Inhalts eines Caches" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Anzeigen des Inhalts eines Caches  
    :::image-end:::  
    
1.  Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Anzeigen der HTTP-Header einer Ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Anzeigen der HTTP-Header einer Ressource  
    :::image-end:::  
    
1.  Wählen **Sie Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Anzeigen des Inhalts einer Ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Anzeigen des Inhalts einer Ressource  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a>Aktualisieren einer Ressource  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data).  
1.  Wählen Sie die Ressource aus, die Sie aktualisieren möchten.  DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Auswählen einer ressource, die aktualisiert werden soll" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Auswählen einer ressource, die aktualisiert werden soll  
    :::image-end:::  
    
1.  Wählen **Sie Aktualisieren** \( Aktualisieren ![ ][ImageRefreshIcon] \).  
    
## <a name="filter-resources"></a>Filtern von Ressourcen  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data).  
1.  Verwenden Sie **das Textfeld Nach Pfad** filtern, um Ressourcen herausfiltern, die nicht mit dem von Ihnen zur Verfügung stellten Pfad übereinstimmen.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen  
    :::image-end:::  
    
## <a name="delete-a-resource"></a>Löschen einer Ressource  

1.  [Anzeigen der Daten für einen Cache](#view-cache-data).  
1.  Wählen Sie die Ressource aus, die Sie löschen möchten.  DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Auswählen einer zu löschende Ressource" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Auswählen einer zu löschende Ressource  
    :::image-end:::  
    
1.  Wählen **Sie Ausgewählte \(** ![ Ausgewähltes Löschen ][ImageDeleteIcon] \) löschen aus.  
    
## <a name="delete-all-cache-data"></a>Löschen aller Cachedaten  

1.  Öffnen **Sie Application**Clear  >  **Storage**.  
1.  Stellen Sie sicher, dass **das Kontrollkästchen Cachespeicher** aktiviert ist.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Das Kontrollkästchen Speicher zwischenspeichern" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Das **Kontrollkästchen Speicher zwischenspeichern**  
    :::image-end:::  
    
1.  Wählen **Sie Websitedaten löschen aus.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Die Schaltfläche Websitedaten löschen" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Die **Schaltfläche Websitedaten** löschen  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Protokollieren von Netzwerkaktivitäts| Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Zwischenspeicherung | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cache) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
