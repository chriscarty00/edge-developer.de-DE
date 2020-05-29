---
title: Anzeigen von Seitenressourcen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611917"
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
    
    > ##### Abbildung1  
    > Dialogfeld ' **Datei öffnen** '  
    > ![Dialogfeld ' Datei öffnen '][ImageOpenFile]  
    
1.  Wählen Sie die Datei aus der Dropdownliste aus, oder geben Sie den Dateinamen ein, und drücken Sie `Enter` im Feld AutoVervollständigen, sobald die richtige Datei hervorgehoben ist.  
    
    > ##### Abbildung2  
    > Eingeben eines Datei namens im Dialogfeld " **Datei öffnen** "  
    > ![Eingeben eines Datei namens im Dialogfeld "Datei öffnen"][ImageFileSearch]  
    
### Öffnen von Ressourcen im Netzwerk Panel   

Weitere Informationen finden Sie unter [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].  

> ##### Abbildung 3  
> Überprüfen einer Ressource im Netzwerk Panel  
> ![Überprüfen einer Ressource im Netzwerk Panel][ImageNetworkResponse]  

### Anzeigen von Ressourcen im Netzwerk Panel von anderen Panels   

Im Abschnitt [Ressourcen durchsuchen](#browse-resources) wird gezeigt, wie Sie Ressourcen aus verschiedenen Teilen der devtools-Benutzeroberfläche anzeigen können.  Wenn Sie jemals eine Ressource im **Netzwerk** Panel überprüfen möchten, klicken Sie mit der rechten Maustaste auf die Ressource, und wählen Sie **in der Netzwerksteuerung**anzeigen aus.  

> ##### Abbildung4  
> Die Option " **im Netzwerk anzeigen"**  
> ![Im Netzwerk Panel anzeigen][ImageRevealNetwork]  

## Ressourcen durchsuchen   

### Durchsuchen von Ressourcen im Netzwerk Panel   

Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].  

> ##### Abbildung5  
> Seitenressourcen im Netzwerkprotokoll  
> ![Seitenressourcen im Netzwerkprotokoll][ImageNetworkLog]  

### Durchsuchen nach Verzeichnissen   

So zeigen Sie die Ressourcen einer Seite an, die nach Verzeichnis geordnet ist:  

1.  Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.  
1.  Klicken Sie auf das **Seiten** Register, um die Ressourcen der Seite anzuzeigen.  Der **Seiten** Bereich wird geöffnet.  
    
    > ##### Abbildung6  
    > **Seiten** Bereich  
    > ![Seitenbereich][ImagePage]  
    
    Nachfolgend finden Sie eine Aufschlüsselung der nicht offensichtlichen Elemente in [Abbildung 6](#figure-6):  
    
    | Seitenelement | Beschreibung |  
    |:--- |:--- |  
    | `top` | Der Haupt Kontext des Dokument [Browsers][MDNInlineFrame] |  
    | `airhorner.com` | Die Domäne.  Alle darunter geschachtelten Ressourcen stammen aus dieser Domäne.  Beispielsweise ist die vollständige URL der `comlink.global.j` Datei wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Ein Verzeichnis. |  
    | `(index)` | Das HTML-Hauptdokument. |  
    | `sw.js` | Ein Service Worker-Laufzeitkontext. |  
    
1.  Klicken Sie auf eine Ressource, um Sie im **Editor**anzuzeigen.  
    
    > ##### Abbildung7  
    > Anzeigen einer Datei im **Editor**  
    > ![Anzeigen einer Datei im Editor][ImageSourcesView]  
    
### Nach Dateiname suchen   

Standardmäßig werden im **Seiten** Bereich Ressourcen nach Verzeichnis gruppiert.  So deaktivieren Sie diese Gruppierung und zeigen die Ressourcen für jede Domäne als flache Liste an:  

1.  Öffnen des **Seiten** Bereichs  Siehe [Verzeichnis durchsuchen](#browse-by-directory).  
1.  Klicken Sie auf **Weitere Optionen** `...` , und deaktivieren Sie " **Gruppieren nach"**.  
    
    > ##### Abbildung8  
    > Die Option **"Gruppieren nach"**  
    > ![Die Option "Gruppieren nach"][ImageGroupByFolder]  
    
    Ressourcen sind nach Dateityp geordnet.  Innerhalb der einzelnen Dateitypen werden die Ressourcen alphabetisch geordnet.  
    
    > ##### Abbildung 9  
    > **Seiten** Bereich nach Deaktivierung des **Ordners "Gruppieren nach"**  
    > ![Seitenbereich nach Deaktivierung des Ordners "Gruppieren nach"][ImageFileNames]  
    
### Nach Dateityp suchen   

So gruppieren Sie Ressourcen basierend auf Ihrem Dateityp zusammen:  

1.  Klicken Sie auf die Registerkarte **Anwendung** .  Das **Anwendungs** Fenster wird geöffnet.  Standardmäßig wird der Bereich **Manifest** in der Regel zuerst geöffnet.  
    
    > ##### Abbildung 10  
    > **Anwendungs** Panel  
    > ![Anwendungs Panel][ImageApplication]  
    
1.  Scrollen Sie nach unten zum Bereich **Frames** .  
    
    > ##### Abbildung 11  
    > Der Bereich " **Frames** "  
    > ![Der Bereich "Frames"][ImageFrames]  
    
1.  Erweitern Sie die Abschnitte, an denen Sie interessiert sind.  
1.  Klicken Sie auf eine Ressource, um Sie anzuzeigen.  
    
    > ##### Abbildung 12  
    > Anzeigen einer Ressource im **Anwendungs** Panel  
    > ![Anzeigen einer Ressource im Anwendungs Panel][ImageApplicationView]  

#### Dateien nach Typ im Netzwerk Panel durchsuchen   

Siehe [Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].  

> ##### Abbildung 13  
> Filtern nach CSS im Netzwerkprotokoll  
> ![Filtern nach CSS im Netzwerkprotokoll][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Abbildung 1: Dialogfeld "Datei öffnen""  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Abbildung 2: Eingeben eines Datei namens in das Dialogfeld "Datei öffnen""  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Abbildung 3: Überprüfen einer Ressource im * * Netzwerk * *-Panel"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Abbildung 4: Anzeigen in der Netzwerksteuerung"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Abbildung 5: Seitenressourcen im Netzwerkprotokoll"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Abbildung 6: der Seitenbereich"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Abbildung 7: Anzeigen einer Datei im Editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Abbildung 8: die Option "Gruppieren nach""  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Abbildung 9: der Seitenbereich nach dem Deaktivieren des Ordners "Gruppieren nach""  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Abbildung 10: Anwendungs Panel"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Abbildung 11: der Bereich "Frames""  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Abbildung 12: Anzeigen einer Ressource im Anwendungs Panel"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Abbildung 13: Filtern nach CSS im Netzwerkprotokoll"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Nach Ressourcentyp Filtern – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Überprüfen der Details der Ressource – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  

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
