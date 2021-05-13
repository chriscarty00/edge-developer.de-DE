---
description: Anzeigen von Anwendungscachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: ec0d1a003e621ecc2220c3eb0d03992bcd8fffa1
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565022"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools  

> [!WARNING]
> Die Anwendungscache-API [wird von der Webplattform entfernt.][HTMLStandardOfflineWebApplications]  

<!--todo: Replace [HTMLStandardOfflineWebApplications] with [WebDevAppcacheRemoval].  -->  

In diesem Handbuch erfahren Sie, wie Sie [Microsoft Edge DevTools verwenden,][MicrosoftEdgeDevTools] um Anwendungscacheressourcen [zu][MDNWebAPIsWindowApplicationCache] überprüfen.  

## <a name="view-application-cache-data"></a>Anzeigen von Anwendungscachedaten  

1.  Wählen Sie oben in DevTools das **Tool Anwendung** aus.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  

1.  Erweitern Sie den **Abschnitt Anwendungscache,** und wählen Sie einen Cache aus, um die Ressourcen anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Der Bereich Anwendungscache" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Der **Bereich Anwendungscache**  
    :::image-end:::  

Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.  

Die **Spalte Type** stellt die Kategorie der Ressource [dar.][MDNHTMLResourcesInAnApplicationCache]  

| Kategorie | Details |  
|:--- |:--- |  
| `Explicit` | Diese Ressource wurde explizit im Manifest aufgeführt. |  
| `Fallback` | Die URL ist ein Fallback für eine andere Ressource.  Die URL der anderen Ressource ist in DevTools nicht aufgeführt. |  
| `Master` | Das `manifest` Attribut für die Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist. |  
| `Network` | Das Manifest hat angegeben, dass die Ressource aus dem Netzwerk stammen muss. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches angeben.**  Der **Anwendungscache** kann die folgenden Zustände haben.  

| Status | Details |  
|:--- |:--- |  
| `CHECKING` | Das Manifest wird abgerufen und auf Updates überprüft. |  
| `DOWNLOADING` | Dem Cache werden Ressourcen hinzugefügt. |  
| `IDLE` | Der Cache hat keine neuen Änderungen. |  
| `OBSOLETE` | Der Cache wird gelöscht. |  
| `UPDATEREADY` |  Eine neue Version des Caches ist verfügbar. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Offlinewebanwendungen – HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache – Web-APIs | MDN"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Vorbereiten der AppCache-| web.dev"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
