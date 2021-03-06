---
description: So finden und analysieren Sie nicht verwendeten JavaScript- und CSS-Code in Microsoft Edge DevTools.
title: Suchen nicht verwendeten JavaScript- und CSS-Codes im Bereich "Abdeckung" in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398763"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a>Suchen von nicht verwendetem JavaScript- und CSS-Code im Bereich "Abdeckung" in Microsoft Edge DevTools  

Der **Bereich Abdeckung** in Microsoft Edge DevTools hilft Ihnen, nicht verwendeten JavaScript- und CSS-Code zu finden.  Das Entfernen nicht verwendeten Codes kann das Laden der Seite beschleunigen und Mobilfunkdaten ihrer mobilen Benutzer speichern.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analysieren der Codeabdeckung" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analysieren der Codeabdeckung  
:::image-end:::  

> [!WARNING]
> Die Suche nach nicht verwendetem Code ist relativ einfach.  Es kann jedoch schwierig sein, eine Codebasis so umgestalten, dass jede Seite nur javaScript und CSS enthält, die sie benötigt.  In diesem Handbuch wird nicht beschrieben, wie Eine Codebasis umgestaltet wird, um nicht verwendeten Code zu vermeiden, da diese Umgestaltungen stark von Ihrem Technologiestapel abhängen.  

## <a name="overview"></a>Übersicht  

Der Versand nicht verwendeter JavaScript- oder CSS-Dateien ist ein häufiges Problem bei der Webentwicklung.  Angenommen, Sie möchten die [Bootstrap-Schaltflächenkomponente auf][BootstrapButtons] Ihrer Seite verwenden.  Um die Schaltflächenkomponente zu verwenden, müssen Sie einen Link zum Bootstrap-Stylesheet in Ihrem HTML wie den folgenden hinzufügen:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Dieses Stylesheet enthält nicht nur den Code für die Schaltflächenkomponente.  Es enthält die CSS für **alle** Bootstrap-Komponenten.  Sie verwenden jedoch keine der anderen Bootstrap-Komponenten.  Ihre Seite heruntergeladen also eine Reihe von CSS, die sie nicht benötigt.  Diese zusätzliche CSS ist aus den folgenden Gründen ein Problem.  

*   Der zusätzliche Code verlangsamt die Seitenlast.  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   Wenn ein Benutzer auf die Seite auf einem mobilen Gerät zugreift, verwendet der zusätzliche Code seine Mobilfunkdaten.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a>Öffnen des Abdeckungsbereichs  

1.  [Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].  
1.  Beginnen Sie mit der `coverage` Eingabe, wählen Sie den **Befehl Abdeckung** anzeigen aus, und wählen Sie dann aus, `Enter` um den Befehl auszuführen.  Der **Bereich** Abdeckung wird in der **Schublade geöffnet.**  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Der Bereich "Abdeckung"" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       Der **Bereich "Abdeckung"**  
    :::image-end:::  
    
## <a name="record-code-coverage"></a>Aufzeichnen der Codeabdeckung  

1.  Wählen Sie eine der folgenden Schaltflächen im **Bereich Abdeckung** aus.  
    *   Wählen **Sie Start Instrumenting Coverage and Reload Page** \( Start Instrumenting Coverage and Reload Page \) aus, wenn Sie überprüfen möchten, welcher Code zum Laden der ![ Seite erforderlich ][ImageReloadIcon] ist.  
    *   Wählen **Sie Instrument Coverage** \( Instrument Coverage ![ \) aus, wenn Sie überprüfen möchten, welcher Code nach der Interaktion mit der ][ImageRecordIcon] Seite verwendet wird.  
1.  Wählen **Sie Abdeckung beenden und Ergebnisse** anzeigen \( Die Instrumentierungsabdeckung beenden und Ergebnisse anzeigen \) aus, wenn Sie die Aufzeichnung der Codeabdeckung ![ beenden ][ImageStopIcon] möchten.  
    
## <a name="analyze-code-coverage"></a>Analysieren der Codeabdeckung  

In der Tabelle im **Bereich** "Abdeckung" werden die analysierten Ressourcen und der Code in den einzelnen Ressourcen angezeigt.  Wählen Sie eine Zeile aus, um diese Ressource im Bereich Quellen zu **öffnen,** und überprüfen Sie eine Zeilenaufschlüsselung des verwendeten Codes und des nicht verwendeten Codes.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Ein Codeabdeckungsbericht" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Ein Codeabdeckungsbericht  
:::image-end:::  

*   Die **SPALTE URL** ist die URL der Ressource, die analysiert wurde.  
*   Die **Spalte Type** gibt an, ob die Ressource CSS, JavaScript oder beides enthält.  
*   Die **Spalte Bytes insgesamt** ist die Gesamtgröße der Ressource in Bytes.  
*   Die **Spalte Nicht verwendete Bytes** gibt die Anzahl der Bytes an, die nicht verwendet wurden.  
*   Die letzte, nicht benannte Spalte ist eine Visualisierung der Spalten **Total Bytes** und **Unused Bytes.**  Der rote Abschnitt der Leiste ist nicht verwendete Bytes.  Der grüne Abschnitt wird byte verwendet.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Schaltflächen – Bootstrap"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/coverage/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
