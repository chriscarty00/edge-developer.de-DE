---
description: Überprüfen Sie mithilfe des Sicherheits Panels, ob eine Seite vollständig durch HTTPS geschützt ist.
title: Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2538f80b08c8162d27f075775075a8b81c5f7725
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993576"
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
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-secure.msft.png":::
       Das **Sicherheits** Panel  
    :::image-end:::  
    
## Häufig auftretende Probleme   

### Nicht sichere Haupt Ursprünge   

Wenn der Haupt Ursprung einer Seite nicht sicher ist, lautet die **Sicherheitsübersicht** , dass **Diese Seite nicht sicher ist**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Eine nicht sichere Seite" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Eine nicht sichere Seite  
:::image-end:::  

Dieses Problem tritt auf, wenn die URL, die Sie besucht haben, über HTTP angefordert wurde.  Um die Sicherheit zu gewährleisten, müssen Sie Sie über HTTPS anfordern.  Wenn Sie beispielsweise die URL in der Adressleiste betrachten, sieht Sie wahrscheinlich ähnlich aus `http://example.com` .  Um die URL zu sichern, sollte die URL `https://example.com` .  

Wenn Sie bereits HTTPS auf dem Server eingerichtet haben, müssen Sie lediglich den Server so konfigurieren, dass alle HTTP-Anforderungen an https umgeleitet werden, um dieses Problem zu beheben.  

Wenn Sie HTTPS auf dem Server nicht eingerichtet haben, können Sie durch [verschlüsseln][LetsEncrypt] eine ﻿kostenlose und relativ einfache Möglichkeit zum Starten des Prozesses bereitstellen.  Oder Sie können das Hosten Ihrer Website in einem CDN in Frage stellen.  Die meisten wichtigen CDNs-Host Websites sind jetzt standardmäßig auf HTTPS.  

> [!TIP]
> Der [use https][WebhintUseHttps] -Hinweis in [webhint][Webhint] kann dazu beitragen, den Vorgang zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an https weitergeleitet werden.  

### Gemischter Inhalt   

**Gemischte Inhalte** bedeuten, dass der Haupt Ursprung einer Seite sicher ist, die Seite jedoch Ressourcen von nicht sicheren Ursprüngen angefordert hat.  Gemischte Inhaltsseiten sind nur teilweise geschützt, da der HTTP-Inhalt für Sniffer zugänglich und anfällig für man-in-the-Middle-Angriffe ist.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Gemischter Inhalt" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Gemischter Inhalt  
:::image-end:::  

Klicken Sie in der vorherigen Abbildung auf **Ansicht 1 Anforderung in der Netzwerksteuerung** , um die **Netzwerk** Steuerung zu öffnen und den Filter anzuwenden, `mixed-content:displayed` damit im **Netzwerkprotokoll** nur nicht sichere Ressourcen angezeigt werden.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Gemischte Ressourcen im Netzwerkprotokoll" lightbox="../media/security-network-filter.msft.png":::
   Gemischte Ressourcen im **Netzwerkprotokoll**  
:::image-end:::  

## Details anzeigen   

### Haupt Ursprungszertifikat anzeigen   

Klicken Sie in der **Sicherheitsübersicht**auf **Zertifikat anzeigen** , um das Zertifikat schnell auf den Haupt Ursprung zu überprüfen.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Ein Haupt Ursprungszertifikat" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Ein Haupt Ursprungszertifikat  
:::image-end:::  

### Anzeigen von Ursprungs Details   

Klicken Sie auf einen der Einträge im Navigationsbereich auf der linken Seite, um die Details des Ursprungs anzuzeigen.  Auf der Seite "Details" können Sie die Verbindungs-und Zertifikatinformationen anzeigen.  Die Informationen zur Transparenz der Zertifikate werden ebenfalls angezeigt, wenn Sie verfügbar sind.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Details des Haupt Ursprungs" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Details des Haupt Ursprungs  
:::image-end:::  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  


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
