---
description: Organisieren Sie Ressourcen nach Frame, Domäne, Typ oder anderen Kriterien.
title: Anzeigen von Seitenressourcen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993590"
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





# Anzeigen von Seitenressourcen mit Microsoft Edge devtools   

  

In diesem Leitfaden lernen Sie, wie Sie Microsoft Edge devtools verwenden, um die Ressourcen einer Webseite anzuzeigen.  Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.  Beispiele für Ressourcen sind CSS-, JavaScript-und HTML-Dateien sowie Bilder.  

In diesem Leitfaden wird davon ausgegangen, dass Sie mit den Grundlagen der [Webentwicklung][MDNLearnWebDevelopment] und der [Microsoft Edge-devtools][MicrosoftEdgeDevTools]vertraut sind.  

## Öffnen von Ressourcen   

Wenn Sie den Namen der Ressource kennen, die Sie überprüfen möchten, bietet das **Befehlsmenü** eine schnelle Möglichkeit zum Öffnen der Ressource.  

1.  Drücken Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \).  Das Dialogfeld **Datei öffnen** wird geöffnet.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-command-menu-empty.msft.png":::
       Dialogfeld ' **Datei öffnen** '  
    :::image-end:::  
    
1.  Wählen Sie die Datei aus der Dropdownliste aus, oder geben Sie den Dateinamen ein, und drücken Sie `Enter` im Feld AutoVervollständigen, sobald die richtige Datei hervorgehoben ist.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Geben Sie im Dialogfeld " **Datei öffnen** " einen Dateinamen ein.  
    :::image-end:::  
    
### Öffnen von Ressourcen im Netzwerk Panel   

Weitere Informationen finden Sie unter [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-response.msft.png":::
   Überprüfen einer Ressource im **Netzwerk** Panel  
:::image-end:::  

### Anzeigen von Ressourcen im Netzwerk Panel von anderen Panels   

Im Abschnitt [Ressourcen durchsuchen](#browse-resources) wird gezeigt, wie Sie Ressourcen aus verschiedenen Teilen der devtools-Benutzeroberfläche anzeigen können.  Wenn Sie jemals eine Ressource im **Netzwerk** Panel überprüfen möchten, klicken Sie mit der rechten Maustaste auf die Ressource, und wählen Sie **in der Netzwerksteuerung**anzeigen aus.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Im Netzwerk Panel anzeigen**  
:::image-end:::  

## Ressourcen durchsuchen   

### Durchsuchen von Ressourcen im Netzwerk Panel   

Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-resources.msft.png":::
   Seitenressourcen im **Netzwerk** Protokoll  
:::image-end:::  

### Durchsuchen nach Verzeichnissen   

So zeigen Sie die Ressourcen einer Seite an, die nach Verzeichnis geordnet ist:  

1.  Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.  
1.  Klicken Sie auf das **Seiten** Register, um die Ressourcen der Seite anzuzeigen.  Der **Seiten** Bereich wird geöffnet.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-empty.msft.png":::
       **Seiten** Bereich  
    :::image-end:::  
    
    Nachfolgend finden Sie eine Aufschlüsselung der nicht offensichtlichen Elemente in der vorherigen Abbildung.  
    
    | Seitenelement | Beschreibung |  
    |:--- |:--- |  
    | `top` | Der Haupt Kontext des Dokument [Browsers][MDNInlineFrame] |  
    | `airhorner.com` | Die Domäne.  Alle darunter geschachtelten Ressourcen stammen aus dieser Domäne.  Beispielsweise ist die vollständige URL der `comlink.global.j` Datei wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Ein Verzeichnis. |  
    | `(index)` | Das HTML-Hauptdokument. |  
    | `sw.js` | Ein Service Worker-Laufzeitkontext. |  
    
1.  Klicken Sie auf eine Ressource, um Sie im **Editor**anzuzeigen.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resource.msft.png":::
       Anzeigen einer Datei im **Editor**  
    :::image-end:::  
    
### Nach Dateiname suchen   

Standardmäßig werden im **Seiten** Bereich Ressourcen nach Verzeichnis gruppiert.  So deaktivieren Sie diese Gruppierung und zeigen die Ressourcen für jede Domäne als flache Liste an:  

1.  Öffnen des **Seiten** Bereichs  Siehe [Verzeichnis durchsuchen](#browse-by-directory).  
1.  Klicken Sie auf **Weitere Optionen** `...` , und deaktivieren Sie " **Gruppieren nach"**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Die Option **"Gruppieren nach"**  
    :::image-end:::  
    
    Ressourcen sind nach Dateityp geordnet.  Innerhalb der einzelnen Dateitypen werden die Ressourcen alphabetisch geordnet.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       **Seiten** Bereich nach Deaktivierung des **Ordners "Gruppieren nach"**  
    :::image-end:::  
    
### Nach Dateityp suchen   

So gruppieren Sie Ressourcen basierend auf Ihrem Dateityp zusammen:  

1.  Klicken Sie auf die Registerkarte **Anwendung** .  Das **Anwendungs** Fenster wird geöffnet.  Standardmäßig wird der Bereich **Manifest** in der Regel zuerst geöffnet.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       **Anwendungs** Panel  
    :::image-end:::  
    
1.  Scrollen Sie nach unten zum Bereich **Frames** .  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Der Bereich " **Frames** "  
    :::image-end:::  
    
1.  Erweitern Sie die Abschnitte, an denen Sie interessiert sind.  
1.  Klicken Sie auf eine Ressource, um Sie anzuzeigen.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Anzeigen einer Ressource im **Anwendungs** Panel  
    :::image-end:::  
    
#### Dateien nach Typ im Netzwerk Panel durchsuchen   

Siehe [Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtern nach CSS im **Netzwerk** Protokoll  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Nach Ressourcentyp Filtern – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<IFRAME->: das Inline Frame-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Web-Entwicklung kennenlernen | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
