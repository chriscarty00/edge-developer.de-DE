---
title: Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611910"
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





# Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Öffnen des Fensters "Sicherheit"   

Der Bereich " **Sicherheit** " ist der wichtigste Ort in devtools, um die Sicherheit einer Seite zu überprüfen.  

1.  [Öffnen Sie devtools][DevToolsOpen].  

1.  Klicken Sie auf die Registerkarte **Sicherheit** , um das **Sicherheits** Fenster zu öffnen.  
    
    > ##### Abbildung1  
    > Das Sicherheitspanel  
    > ![Das Sicherheitspanel][ImageSecurityPanel]  
    
## Häufig auftretende Probleme   

### Nicht sichere Haupt Ursprünge   

Wenn der Haupt Ursprung einer Seite nicht sicher ist, lautet die **Sicherheitsübersicht** , dass **Diese Seite nicht sicher ist**.  

> ##### Abbildung2  
> Eine nicht sichere Seite  
> ![Eine nicht sichere Seite][ImageNonSecurePage]  

Dieses Problem tritt auf, wenn die URL, die Sie besucht haben, über HTTP angefordert wurde.  Um die Sicherheit zu gewährleisten, müssen Sie Sie über HTTPS anfordern.  Wenn Sie beispielsweise die URL in der Adressleiste betrachten, sieht Sie wahrscheinlich ähnlich aus `http://example.com` .  Um die URL zu sichern, sollte die URL `https://example.com` .  

Wenn Sie bereits HTTPS auf dem Server eingerichtet haben, müssen Sie lediglich den Server so konfigurieren, dass alle HTTP-Anforderungen an https umgeleitet werden, um dieses Problem zu beheben.  

Wenn Sie HTTPS auf dem Server nicht eingerichtet haben, können Sie durch [verschlüsseln][LetsEncrypt] eine ﻿kostenlose und relativ einfache Möglichkeit zum Starten des Prozesses bereitstellen.  Oder Sie können das Hosten Ihrer Website in einem CDN in Frage stellen.  Die meisten wichtigen CDNs-Host Websites sind jetzt standardmäßig auf HTTPS.  

> [!TIP]
> Der [use https][WebhintUseHttps] -Hinweis in [webhint][Webhint] kann dazu beitragen, den Vorgang zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an https weitergeleitet werden.  

### Gemischter Inhalt   

**Gemischte Inhalte** bedeuten, dass der Haupt Ursprung einer Seite sicher ist, die Seite jedoch Ressourcen von nicht sicheren Ursprüngen angefordert hat.  Gemischte Inhaltsseiten sind nur teilweise geschützt, da der HTTP-Inhalt für Sniffer zugänglich und anfällig für man-in-the-Middle-Angriffe ist.  

> ##### Abbildung 3  
> Gemischter Inhalt  
> ![Gemischter Inhalt][ImageMixedContent]  

Klicken Sie in [Abbildung 3](#figure-3)auf **Ansicht 1 Anforderung in der Netzwerksteuerung** , um das **Netzwerk** Panel zu öffnen und den Filter anzuwenden, `mixed-content:displayed` damit im **Netzwerkprotokoll** nur nicht sichere Ressourcen angezeigt werden.  

> ##### Abbildung4  
> Gemischte Ressourcen im Netzwerkprotokoll  
> ![Gemischte Ressourcen im Netzwerkprotokoll][ImageMixedResourcesNetworkLog]  

## Details anzeigen   

### Haupt Ursprungszertifikat anzeigen   

Klicken Sie in der **Sicherheitsübersicht**auf **Zertifikat anzeigen** , um das Zertifikat schnell auf den Haupt Ursprung zu überprüfen.  

> ##### Abbildung5  
> Ein Haupt Ursprungszertifikat  
> ![Ein Haupt Ursprungszertifikat][ImageCertificate]  

### Anzeigen von Ursprungs Details   

Klicken Sie auf einen der Einträge im Navigationsbereich auf der linken Seite, um die Details des Ursprungs anzuzeigen.  Auf der Seite "Details" können Sie die Verbindungs-und Zertifikatinformationen anzeigen.  Die Informationen zur Transparenz der Zertifikate werden ebenfalls angezeigt, wenn Sie verfügbar sind.  

> ##### Abbildung6  
> Details des Haupt Ursprungs  
> ![Details des Haupt Ursprungs][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Abbildung 1: das Sicherheitspanel"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Abbildung 2: eine nicht sichere Seite"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Abbildung 3: gemischter Inhalt"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Abbildung 4: gemischte Ressourcen im Netzwerkprotokoll"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Abbildung 5: ein Haupt Ursprungszertifikat"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Abbildung 6: Details des Haupt Ursprungs"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  


[LetsEncrypt]: https://letsencrypt.org "Verschlüsseln-﻿kostenlose SSL/TLS-Zertifikate"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Verwenden von HTTPS | webhint-Dokumentation"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/security/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
