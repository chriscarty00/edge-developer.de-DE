---
description: Verwenden Sie das Tool Probleme, um Probleme mit Ihrer Website zu finden und zu beheben.
title: Suchen und Beheben von Problemen mit dem tool Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 64954d632416f7d1353269d04c1550ca7a0652b7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564182"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Suchen und Beheben von Problemen mit dem tool Microsoft Edge DevTools  

Das **Tool Probleme** in Microsoft Edge DevTools reduziert die Benachrichtigungsmüdigkeit und Unübersichtlichkeit der **Konsole.**  Verwenden Sie es, um Lösungen für probleme zu finden, die vom Browser erkannt werden, z. B. Cookieprobleme und gemischte Inhalte.  

> [!NOTE]
> In Microsoft Edge 84 unterstützt das **Problemtool** drei Arten von Problemen:  
> *   [Cookieprobleme][MDNSameSiteCookies]  
> *   [Gemischte Inhalte][MDNMixedContent]  
> *   [COEP-Probleme][W3CCOEPSpec]
> 
> Das Microsoft Edge DevTools-Team plant, weitere Problemtypen in zukünftigen Versionen von Microsoft Edge.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Öffnen Sie das Tool Probleme in der DevTools-Schublade.  

1.  Navigieren Sie zu einer Webseite, [z. B. samesite-sandbox.glitch.me][GlitchSamesiteSandbox], die zu behebende Probleme enthält.  
1.  [Öffnen Sie DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Klicken Sie **in der gelben** Warnleiste auf die Schaltfläche Zu Probleme wechseln.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Wechseln Sie zu Schaltfläche Probleme in der gelben Warnleiste, wenn Probleme erkannt werden" lightbox="../media/issues-open-issues-tab.msft.png":::
             Die **Schaltfläche Zu Probleme** wechseln in der gelben Warnleiste, wenn Probleme erkannt werden.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Alternativ wählen Sie **im Menü** Weitere Tools die Option **Probleme** aus.  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Problemtool im Menü Weitere Tools" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Problemtool** im **Menü Weitere** Tools  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Wählen Sie **bei Bedarf die** Schaltfläche Seite laden aus.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Problemtool in der DevTools Drawer with Reload page button" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Problemtool** in der DevTools Drawer with **Reload page button**  
    :::image-end:::  

    Die in der Konsole **gemeldeten** Probleme sind schwer zu verstehen, z. B. die Cookiewarnungen in der folgenden Abbildung.  Basierend auf den gemeldeten Problemen ist möglicherweise nicht klar, was Sie tun müssen.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Problemtool in der DevTools-Drawer mit drei Cookieproblemen" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Problemtool** in der DevTools-Drawer mit drei Cookieproblemen  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Anzeigen von Elementen im Problemtool  

Das **Tool Probleme** in der DevTools-Drawer stellt Warnungen strukturiert, aggregiert und aktionensfähig zur Verfügung.  

1.  Wählen Sie ein Element im **Tool Probleme** aus, um Anleitungen zum Beheben des Problems und zum Suchen betroffener Ressourcen zu erhalten.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Markieren von websiteübergreifenden Cookies als sicheres Problem, das im Problemtool geöffnet ist" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Markieren von websiteübergreifenden Cookies als sicheres** Problem, das im **Problemtool geöffnet** ist  
    :::image-end:::  
    
    Jedes Element besteht aus vier Komponenten:  
    
    *   Eine Überschrift, die das Problem beschreibt.  
    *   Eine Beschreibung, die den Kontext und die Lösung enthält.  
    *   Ein **ABSCHNITT "AFFECTED RESOURCES",** der Mit Ressourcen im entsprechenden DevTools-Kontext wie dem Netzwerkbereich verknüpft.  
    *   Links zu weiteren Anleitungen.  
    
1.  Wählen Sie Elemente in **AFFECTED RESOURCES aus,** um Details anzuzeigen.  Im folgenden Beispiel wirkt sich das Problem **"Websiteübergreifende Cookies** als Sicher markieren" auf ein Cookie und zwei Anforderungen aus.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Betroffene Ressourcen im Problemtool geöffnet" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Betroffene Ressourcen werden im Tool **Probleme** in der DevTools-Schublade geöffnet  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Anzeigen von Problemen im Kontext  

1.  Wählen Sie einen Ressourcenlink aus, um das Element im entsprechenden Kontext in DevTools zu sehen.  Wählen Sie im folgenden Beispiel unter Anforderungen die Cookies aus, die `samesite-sandbox.glitch.me` dieser Anforderung zugeordnet sind. ****  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Anzeigen des betroffenen Cookies im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-request.msft.png":::
       Anzeigen des betroffenen Cookies im **DevTools-Netzwerktool**  
    :::image-end:::  

1.  Scrollen Sie, um das Element mit einem Problem zu sehen: für das folgende Beispiel das `ck02` Cookie.  Zeigen Sie auf die **Spalte SameSite,** um den vom Problem `None` erkannten Wert zu überprüfen.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Kein Wert in der Spalte SameSite für das ck02-Cookie im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` Wert in der **Spalte SameSite** für das `ck02` Cookie im **DevTools-Netzwerktool**  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "SameSite-Cookietests | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite-Cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Gemischte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Cross-Origin Embedder Policy | Web Incubator Community Group"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) und wird von [Sam Dutton][SamDutton] \(Developer Advocate\) verfasst.  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
