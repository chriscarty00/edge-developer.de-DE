---
title: Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601719"
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





# Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools   



Die Registerkarte Coverage in Microsoft Edge devtools hilft Ihnen, ungenutzte JavaScript-und CSS-Codes zu finden.  Wenn Sie nicht verwendeten Code entfernen, können Sie das Laden der Seite beschleunigen und Ihre mobilen Benutzer mobil Daten speichern.  

> ##### Abbildung1  
> Analysieren der Codeabdeckung  
> ![Analysieren der Codeabdeckung][ImageExample]  

> [!WARNING]
> Das Auffinden unbenutzten Codes ist relativ einfach.  Das Umgestalten einer CodeBase, damit jede Seite nur das JavaScript und das CSS liefert, die Sie benötigt, ist möglicherweise schwierig.  In diesem Leitfaden wird nicht behandelt, wie Sie eine CodeBase umgestalten, um nicht verwendeten Code zu vermeiden, da diese umgestalten in hohem Maße von Ihrem Technologiestapel abhängen.  

## Übersicht   

Das Versenden unbenutzter JavaScript-oder CSS-Probleme ist ein häufiges Problem in der Webentwicklung.  Nehmen wir beispielsweise an, dass Sie die [Bootstrap-Schaltflächenkomponente][BootstrapButtons] auf der Seite verwenden möchten.  Um die Button-Komponente zu verwenden, müssen Sie einen Link zum Bootstrap-Stylesheet in Ihrem HTML-Code hinzufügen, wie hier:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Dieses Stylesheet enthält nicht nur den Code für die Schaltflächenkomponente.  Sie enthält das CSS für **alle** Bootstrap-Komponenten.  Sie verwenden jedoch keine der anderen Bootstrap-Komponenten.  Ihre Seite lädt also eine Reihe von CSS herunter, die nicht benötigt werden.  Dieses extra-CSS ist aus den folgenden Gründen ein Problem.  

*   Der zusätzliche Code verlangsamt das Laden der Seite.  <!--See [Render-Blocking CSS][render].  -->  
*   Wenn ein Benutzer auf die Seite auf einem mobilen Gerät zugreift, verwendet der zusätzliche Code Ihre zellularen Daten.  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## Öffnen der Registerkarte "Abdeckung"   

1.  [Öffnen des Befehlsmenüs][DevToolsCommandMenu]  
1.  Beginnen `coverage` Sie mit der Eingabe, wählen Sie den Befehl **Coverage anzeigen** aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.  Die Registerkarte **Coverage** wird im **Einzug**geöffnet.  

    > ##### Abbildung2  
    > Die Registerkarte " **Coverage** "  
    > ![Die Registerkarte "Coverage"][ImageCoverage]  

## Aufzeichnen von Codeabdeckung   

1.  Klicken Sie auf der Registerkarte **Coverage** auf eine der folgenden Schaltflächen:  
    *   Klicken Sie auf **Instrumentations Abdeckung starten und Seiten** ![ Anfang Instrumentations Abdeckung und Reload erneut laden, ][ImageReloadIcon] Wenn Sie sehen möchten, welcher Code zum Laden der Seite erforderlich ist.  
    *   Klicken Sie auf **Instrument** Coverage ![ Instrumentation Coverage ][ImageRecordIcon] , wenn Sie sehen möchten, welcher Code nach der Interaktion mit der Seite verwendet wird.  
1.  Klicken Sie auf **Instrumentations Abdeckung beenden und Ergebnisse anzeigen** , ![ um die Abdeckung der Instrumentation zu beenden und Ergebnisse anzuzeigen, ][ImageStopIcon] Wenn Sie die Aufzeichnung der Codeabdeckung beenden möchten.  

## Analysieren der Codeabdeckung   

Die Tabelle auf der Registerkarte **Coverage** zeigt Ihnen, welche Ressourcen analysiert wurden und wie viel Code innerhalb der einzelnen Ressourcen verwendet wird. Klicken Sie auf eine Zeile, um diese Ressource im **Quellen** Panel zu öffnen, und sehen Sie eine zeilenweise Aufschlüsselung von verwendetem Code und nicht verwendetem Code.  

> ##### Abbildung 3  
> Code Coverage-Bericht  
> ![Code Coverage-Bericht][ImageExample]  

*   Die **URL** -Spalte ist die URL der Ressource, die analysiert wurde.  
*   In der Spalte **Typ** wird angegeben, ob die Ressource CSS, JavaScript oder beides enthält.  
*   Die Spalte " **Gesamt Bytes** " gibt die Gesamtgröße der Ressource in Bytes an.  
*   Die Spalte "nicht **verwendete Bytes** " gibt die Anzahl der Bytes an, die nicht verwendet wurden.  
*   Die letzte, unbenannte Spalte ist eine Visualisierung der Spalten **Gesamt Bytes** und **nicht verwendete Bytes** .  Der Rote Bereich der Leiste ist nicht verwendete Bytes.  Der grüne Abschnitt wird in Bytes verwendet.  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Abbildung 1: Analysieren der Codeabdeckung"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Abbildung 2: Registerkarte "Coverage""  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Abbildung 3: ein Code Coverage-Bericht"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Schaltflächen – Bootstrap"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/coverage/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
