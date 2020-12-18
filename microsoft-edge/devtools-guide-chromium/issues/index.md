---
description: Verwenden Sie das Tool Probleme, um Probleme mit Ihrer Website zu finden und zu beheben.
title: Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 8bd3e5950572a9d3fdce71ec6cd935f6b6d6a0b7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230663"
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

# Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool  

Das **Problem** Tool in Microsoft Edge devtools verringert die Ermüdung der Benachrichtigung und die unaufgeräumtheit der **Konsole**.  Verwenden Sie es, um Lösungen für vom Browser erkannte Probleme zu finden, wie etwa Cookie-Probleme und gemischte Inhalte.  

> [!NOTE]
> In Microsoft Edge 84 unterstützt das **Issues** -Tool drei Arten von Problemen:  
> *   [Cookie-Probleme][MDNSameSiteCookies]  
> *   [Gemischter Inhalt][MDNMixedContent]  
> *   [COEP-Probleme][W3CCOEPSpec]
> 
> Das Microsoft Edge devtools-Team plant, weitere Problemtypen in zukünftigen Versionen von Microsoft Edge zu unterstützen.  

## Öffnen des Tools "Probleme" im devtools-Einzug  

1.  Besuchen Sie eine Seite wie [SameSite-Sandbox.Glitch.me][GlitchSamesiteSandbox], die Probleme enthält, die behoben werden können.  
1.  [Öffnen Sie devtools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Klicken Sie auf der gelben Warnleiste auf die Schaltfläche **Gehe zu Problemen** .  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Schaltfläche ' Probleme ' in der gelben Warnleiste, wenn Probleme erkannt werden" lightbox="../media/issues-open-issues-tab.msft.png":::
             Die Schaltfläche " **Probleme wechseln** " in der gelben Warnleiste, wenn Probleme erkannt werden.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Sie können auch im Menü **Weitere Tools** die Option **Probleme** auswählen.  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Tool ' Probleme ' im Menü ' Weitere Tools '" lightbox="../media//issues-more-tools-menu.msft.png":::
             Tool ' **Probleme** ' im Menü ' **Weitere Tools** '  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Wählen Sie bei Bedarf die Schaltfläche **Seite neu laden** aus.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Tool ' Probleme ' in der devtools-Schublade mit der Schaltfläche ' Seite neu laden '" lightbox="../media/issues-tab-before-refresh.msft.png":::
       Tool ' **Probleme** ' in der devtools-Schublade mit der Schaltfläche ' **Seite neu laden** '  
    :::image-end:::  

    Die in der **Konsole** gemeldeten Probleme sind schwer verständlich, wie etwa die Cookie-Warnungen in der folgenden Abbildung.  Basierend auf den gemeldeten Problemen ist es möglicherweise nicht klar, was Sie tun müssen.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Tool "Probleme" im devtools-Einzug mit drei Problemen mit Cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       Tool " **Probleme** " im devtools-Einzug mit drei Problemen mit Cookies  
    :::image-end:::  
    
## Anzeigen von Elementen im Tool "Probleme"  

Das Tool " **Probleme** " im devtools-Einzug zeigt Warnungen auf strukturierter, aggregierter und umsetzbarer Weise an.  

1.  Wählen Sie ein Element im **Issues** -Tool aus, um Anleitungen zur Behebung des Problems und zum Auffinden betroffener Ressourcen zu erhalten.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Markieren von websiteübergreifenden Cookies als sicheres Problem im Tool "Probleme"" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Markieren von websiteübergreifenden Cookies als sicheres** Problem im Tool " **Probleme** "  
    :::image-end:::  
    
    Jedes Element verfügt über vier Komponenten:  
    
    *   Eine Überschrift, die das Problem beschreibt.  
    *   Eine Beschreibung, die den Kontext und die Lösung bereitstellt.  
    *   Ein Abschnitt " **betroffene Ressourcen** ", der Links zu Ressourcen im entsprechenden devtools-Kontext wie dem Netzwerk Panel enthält.  
    *   Links zu weiteren Anleitungen.  
    
1.  Wählen Sie Elemente in **betroffenen Ressourcen** aus, um Details anzuzeigen.  Im folgenden Beispiel wirkt sich das **kennzeichnen von websiteübergreifenden Cookies als sicheres** Problem auf ein Cookie und zwei Anforderungen aus.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Auf der Registerkarte "Issues Drawer" geöffnete betroffene Ressourcen" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Im Tool " **Probleme** " im devtools-Einzug geöffnete betroffene Ressourcen  
    :::image-end:::  
    
## Anzeigen von Problemen im Kontext  

1.  Wählen Sie einen Ressourcen Link aus, um das Element im entsprechenden Kontext in devtools anzuzeigen.  Wählen Sie im folgenden Beispiel `samesite-sandbox.glitch.me` unter **Anforderungen** aus, um die Cookies anzuzeigen, die dieser Anforderung angefügt sind.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Anzeigen des betroffenen Cookies im devtools-Netzwerk Panel" lightbox="../media/issues-tab-view-request.msft.png":::
       Anzeigen des betroffenen Cookies im devtools- **Netzwerk** Panel  
    :::image-end:::  

1.  Scrollen Sie, um das Element mit einem Problem anzuzeigen: im folgenden Beispiel wird das `ck02` Cookie angezeigt.  Zeigen Sie mit der Maus auf die Spalte **SameSite** , um den `None` Wert anzuzeigen, der vom Problem erkannt wurde.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Kein Wert in der Spalte "SameSite" für das ck02-Cookie im devtools-Netzwerk Panel" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` Wert in der Spalte " **SameSite** " für das `ck02` Cookie im devtools- **Netzwerk** Panel  
    :::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "SameSite-Cookie-Tests | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite Cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Gemischter Inhalt | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Richtlinien für die übergreifende Einbettung | Webinkubator-Community-Gruppe"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) gefunden und von [Sam Dutton][SamDutton] (Entwickler Anwalt \) erstellt.  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
