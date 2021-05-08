---
description: Verwenden Sie den Sicherheitsbereich, um sicherzustellen, dass eine Seite vollständig durch HTTPS geschützt ist.
title: Verstehen von Sicherheitsproblemen mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397776"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a>Verstehen von Sicherheitsproblemen mit Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a>Öffnen des Sicherheitsbereichs  

Der **Sicherheitsbereich** ist der Hauptort in DevTools für die Überprüfung der Sicherheit einer Seite.  

1.  [Öffnen Sie DevTools][DevToolsOpen].  
1.  Wählen Sie die **Registerkarte Sicherheit** aus, um das **Sicherheitstool zu** öffnen.  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Der Sicherheitsbereich" lightbox="../media/security-security-overview-secure.msft.png":::
       Der **Sicherheitsbereich**  
    :::image-end:::  
    
## <a name="common-problems"></a>Häufige Probleme  

### <a name="non-secure-main-origins"></a>Nicht sichere Hauptherkunft  

Wenn der Hauptherkunft einer Seite **** nicht sicher ist, heißt es in der Sicherheitsübersicht, **dass diese Seite nicht sicher ist.**  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Eine nicht sichere Seite" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Eine nicht sichere Seite  
:::image-end:::  

Dieses Problem tritt auf, wenn die url, die Sie besucht haben, über HTTP angefordert wurde.  Um die Sicherheit zu gewährleisten, müssen Sie sie über HTTPS anfordern.  Wenn Sie sich beispielsweise die URL in der Adressleiste anschauen, sieht sie wahrscheinlich ähnlich aus wie `http://example.com` .  Um die Sicherheit zu gewährleisten, sollte die URL `https://example.com` sein.  

Wenn Sie HTTPS bereits auf Ihrem Server eingerichtet haben, müssen Sie nur den Server so konfigurieren, dass alle HTTP-Anforderungen an HTTPS umgeleitet werden.  

Wenn Sie HTTPS nicht auf Ihrem Server eingerichtet haben, bietet [Let's Encrypt][LetsEncrypt] eine kostenlose und relativ einfache Möglichkeit, den Prozess zu starten.  Sie können auch erwägen, Ihre Website auf einem CDN.  Die meisten wichtigen CDNs hosten jetzt standardmäßig Websites auf HTTPS.  

> [!TIP]
> Der [Hinweis HTTPS][WebhintUseHttps] in [Webhint][Webhint] verwenden kann dazu beitragen, den Prozess zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an HTTPS geleitet werden.  

### <a name="mixed-content"></a>Gemischte Inhalte  

**Gemischter** Inhalt bedeutet, dass der Hauptherkunft einer Seite sicher ist, die Seite jedoch Ressourcen aus nicht sicheren Ursprüngen angefordert hat.  Seiten mit gemischten Inhalten sind nur teilweise geschützt, da der Zugriff auf den HTTP-Inhalt für Schnüffeler und anfällig für Man-in-the-Middle-Angriffe ist.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Gemischte Inhalte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Gemischte Inhalte  
:::image-end:::  

Wählen Sie in der vorherigen Abbildung die Option **** Anforderung **anzeigen im** Netzwerkbereich aus, um das Netzwerktool zu öffnen und den Filter anzuwenden, sodass im Netzwerkprotokoll nur nicht sichere Ressourcen `mixed-content:displayed` angezeigt werden. ****  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Gemischte Ressourcen im Netzwerkprotokoll" lightbox="../media/security-network-filter.msft.png":::
   Gemischte Ressourcen im **Netzwerkprotokoll**  
:::image-end:::  

## <a name="view-details"></a>Details anzeigen  

### <a name="view-main-origin-certificate"></a>Hauptursprungzertifikat anzeigen  

Wählen Sie **in der Sicherheitsübersicht**Zertifikat **anzeigen aus,** um das Zertifikat schnell auf den Hauptursprung zu überprüfen.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Ein Hauptursprungzertifikat" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Ein Hauptursprungzertifikat  
:::image-end:::  

### <a name="view-origin-details"></a>Anzeigen von Ursprungsdetails  

Wählen Sie einen der Einträge im linken Navigationsgerät aus, um die Details des Ursprungs anzuzeigen.  Auf der Detailseite können Sie Verbindungs- und Zertifikatinformationen anzeigen.  Informationen zur Zertifikattransparenz werden ebenfalls angezeigt, wenn verfügbar.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Hauptherkunftsdetails" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Hauptherkunftsdetails  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Let's Encrypt – Kostenlose SSL/TLS-Zertifikate"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Verwenden von HTTPS-| Webhintdokumentation"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/security/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
