---
title: Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931211"
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

# Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools  

> [!WARNING]
> Die Anwendungs Cache-API wird [aus der Web-Plattform entfernt][HTMLStandardOfflineWebApplications].  

Dieser Leitfaden zeigt Ihnen, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Anwendungs Cache][MDNWebAPIsWindowApplicationCache] Ressourcen zu überprüfen.  

## Anzeigen von Anwendungs Cache Daten  

1.  Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.  Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  

1.  Erweitern Sie den Abschnitt **Anwendungscache** , und wählen Sie einen Cache aus, um die Ressourcen anzuzeigen.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Der Anwendungs Cache Bereich" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Der **Anwendungs Cache** Bereich  
    :::image-end:::  

Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.  

Die Spalte **Typ** steht [für die Kategorie der Ressource][MDNHTMLResourcesInAnApplicationCache].  

| Kategorie | Details |  
|:--- |:--- |  
| `Explicit` | Diese Ressource wurde explizit im Manifest aufgeführt. |  
| `Fallback` | Die URL ist ein Fallback für eine andere Ressource.  Die URL der anderen Ressource ist in devtools nicht aufgeführt. |  
| `Master` | Das `manifest` Attribut der Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist. |  
| `Network` | Das Manifest hat angegeben, dass die Ressource aus dem Netzwerk stammen muss. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches**angeben.  Der **Anwendungs Cache** kann die folgenden Zustände aufweisen.  

| Status | Details |  
|:--- |:--- |  
| `CHECKING` | Das Manifest wird abgerufen und auf Updates überprüft. |  
| `DOWNLOADING` | Ressourcen werden dem Cache hinzugefügt. |  
| `IDLE` | Der Cache hat keine neuen Änderungen. |  
| `OBSOLETE` | Der Cache wird gelöscht. |  
| `UPDATEREADY` |  Eine neue Version des Caches ist verfügbar. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Offline-Webanwendungen – HTML-Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-Web-APIs | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
