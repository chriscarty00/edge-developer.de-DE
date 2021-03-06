---
description: Organisieren Sie Ressourcen nach Frame, Domäne, Typ oder anderen Kriterien.
title: Anzeigen von Seitenressourcen mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 75063b23f23c25ff4fe2e7f6e044a2de9a7b1ccd
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398224"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a>Anzeigen von Seitenressourcen mit Microsoft Edge DevTools  

In diesem Handbuch erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen der Ressourcen einer Webseite verwenden.  Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.  Beispiele für Ressourcen sind CSS-, JavaScript- und HTML-Dateien sowie Bilder.  

In diesem Handbuch wird davon ausgegangen, [][MDNLearnWebDevelopment] dass Sie mit den Grundlagen der Webentwicklung und [Microsoft Edge DevTools vertraut sind.][MicrosoftEdgeDevTools]  

## <a name="open-resources"></a>Öffnen von Ressourcen  

Wenn Sie den Namen der Ressource kennen, die **** Sie überprüfen möchten, bietet das Befehlsmenü eine schnelle Möglichkeit zum Öffnen der Ressource.  

1.  Wählen `Control` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) aus.  Das **Dialogfeld Datei öffnen** wird geöffnet.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Dialogfeld Datei öffnen" lightbox="../media/resources-command-menu-empty.msft.png":::
       Dialogfeld **Datei** öffnen  
    :::image-end:::  
    
1.  Wählen Sie die Datei aus dem Dropdownmenü aus, oder beginnen Sie mit der Eingabe des Dateinamens, und wählen Sie aus, sobald die richtige Datei `Enter` im Feld autoComplete hervorgehoben ist.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Geben Sie einen Dateinamen im Dialogfeld Datei öffnen ein." lightbox="../media/resources-command-menu-file-search.msft.png":::
       Geben Sie einen Dateinamen im Dialogfeld **Datei öffnen** ein.  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a>Öffnen von Ressourcen im Netzwerktool  

Navigieren Sie zu [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Überprüfen einer Ressource im Netzwerktool" lightbox="../media/resources-network-response.msft.png":::
   Überprüfen einer Ressource im **Netzwerktool**  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a>Aufschluss über Ressourcen im Netzwerktool in anderen Panels  

Im [Abschnitt Ressourcen durchsuchen](#browse-resources) unten erfahren Sie, wie Sie Ressourcen aus verschiedenen Teilen der DevTools-Benutzeroberfläche anzeigen.  Wenn Sie jemals eine Ressource **** im Netzwerktool überprüfen möchten, zeigen Sie auf die Ressource, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Im Netzwerkbereich einblenden **aus.**  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Anzeige im Netzwerkbereich" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Anzeige im Netzwerkbereich**  
:::image-end:::  

## <a name="browse-resources"></a>Durchsuchen von Ressourcen  

### <a name="browse-resources-in-the-network-panel"></a>Durchsuchen von Ressourcen im Netzwerkbereich  

Navigieren Sie zu [Netzwerkaktivität protokollieren.][DevtoolsNetworkLogActivity]  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Seitenressourcen im Netzwerkprotokoll" lightbox="../media/resources-network-resources.msft.png":::
   Seitenressourcen im **Netzwerkprotokoll**  
:::image-end:::  

### <a name="browse-by-directory"></a>Durchsuchen nach Verzeichnis  

So zeigen Sie die Ressourcen einer nach Verzeichnis organisierten Seite an:  

1.  Wählen Sie das **Tool Quellen** aus, um den Bereich **Quellen zu** öffnen.  
1.  Wählen Sie den **Bereich** Seite aus, um die Ressourcen der Seite anzeigen zu können.  Der **Bereich Seite** wird geöffnet.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Seitenbereich" lightbox="../media/resources-sources-page-empty.msft.png":::
       **Seitenbereich**  
    :::image-end:::  
    
    Hier ist eine Aufschlüsselung der nicht offensichtlichen Elemente in der vorherigen Abbildung.  
    
    | Seitenelement | Beschreibung |  
    |:--- |:--- |  
    | `top` | Der Hauptkontext [für das Durchsuchen von Dokumenten][MDNInlineFrame]. |  
    | `airhorner.com` | Die Domäne.  Alle ressourcen, die unter ihr geschachtelt sind, stammen aus dieser Domäne.  Die vollständige URL der Datei ist z. B. `comlink.global.j` wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Ein Verzeichnis. |  
    | `(index)` | Das Haupt-HTML-Dokument. |  
    | `sw.js` | Ein Laufzeitkontext eines Dienstarbeitsmitarbeiters. |  
    
1.  Wählen Sie eine Ressource aus, um sie im **Editor anzeigen zu können.**  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Anzeigen einer Datei im Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       Anzeigen einer Datei im **Editor**  
    :::image-end:::  
    
### <a name="browse-by-filename"></a>Durchsuchen nach Dateiname  

Standardmäßig werden im **Seitenbereich** Ressourcen nach Verzeichnis gruppen.  So deaktivieren Sie diese Gruppierung, und zeigen Sie die Ressourcen für jede Domäne als flache Liste an:  

1.  Öffnen Sie den **Seitenbereich.**  Navigieren Sie [zu Durchsuchen nach Verzeichnis](#browse-by-directory).  
1.  Wählen **Sie Weitere Optionen aus,** und deaktivieren Sie `...` **"Nach Ordner" gruppieren.**  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Die Option "Gruppe nach Ordner"" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Die **Option "Gruppe nach Ordner"**  
    :::image-end:::  
    
    Ressourcen sind nach Dateityp organisiert.  Innerhalb jedes Dateityps sind die Ressourcen alphabetisch angeordnet.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Der Seitenbereich nach der Deaktivierung von "Gruppe nach Ordner"" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       Der **Seitenbereich** nach der Deaktivierung **von "Gruppe nach Ordner"**  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a>Durchsuchen nach Dateityp  

So gruppieren Sie Ressourcen basierend auf ihrem Dateityp:  

1.  Wählen Sie die **Registerkarte Anwendung** aus.  Das **Tool Anwendung** wird geöffnet.  Standardmäßig wird der **Manifestbereich** in der Regel zuerst geöffnet.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Das Anwendungstool" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Das **Anwendungstool**  
    :::image-end:::  
    
1.  Scrollen Sie **** nach unten zum Frames-Bereich.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Der Bereich Frames" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Der **Bereich Frames**  
    :::image-end:::  
    
1.  Erweitern Sie die Abschnitte, an denen Sie interessiert sind.  
1.  Wählen Sie eine Ressource aus, um sie anzeigen zu können.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Anzeigen einer Ressource im Anwendungsbereich" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Anzeigen einer Ressource im **Anwendungsbereich**  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a>Durchsuchen von Dateien nach Typ im Netzwerkbereich  

Navigieren Sie [zu Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtern nach CSS im Netzwerkprotokoll" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtern nach CSS im **Netzwerkprotokoll**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtern nach Ressourcentyp – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspect the details of the resource - Inspect network activity in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Protokollnetzwerkaktivität – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: Das Inlineframe-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Erfahren Sie mehr über | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
