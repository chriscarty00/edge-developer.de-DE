---
description: Suchen und Analysieren von nicht verwendetem Javascript und CSS-Code in Microsoft Edge devtools
title: Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 19bc15578e00e5a9f3389529f589e9790280a0e4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993093"
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

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analysieren der Codeabdeckung" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analysieren der Codeabdeckung  
:::image-end:::  

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

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Die Registerkarte "Coverage"" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       Die Registerkarte " **Coverage** "  
    :::image-end:::  
    
## Aufzeichnen von Codeabdeckung   

1.  Klicken Sie auf der Registerkarte **Coverage** auf eine der folgenden Schaltflächen:  
    *   Klicken Sie auf **Instrumentations Abdeckung starten und Seite neu laden** ( ![ Start Instrumentation Coverage and Reload Page ][ImageReloadIcon] \), wenn Sie sehen möchten, welcher Code zum Laden der Seite erforderlich ist.  
    *   Klicken Sie auf **Instrument Coverage** \ ( ![ Instrument Coverage ][ImageRecordIcon] \), wenn Sie sehen möchten, welcher Code nach der Interaktion mit der Seite verwendet wird.  
1.  Klicken Sie auf **Instrumentations Abdeckung beenden und Ergebnisse anzeigen** \ ( ![ Instrumentations Abdeckung beenden und Ergebnisse anzeigen ][ImageStopIcon] \), wenn Sie die Aufzeichnung der Codeabdeckung beenden möchten.  
    
## Analysieren der Codeabdeckung   

Die Tabelle auf der Registerkarte **Coverage** zeigt Ihnen, welche Ressourcen analysiert wurden und wie viel Code innerhalb der einzelnen Ressourcen verwendet wird.  Klicken Sie auf eine Zeile, um diese Ressource im **Quellen** Panel zu öffnen, und sehen Sie eine zeilenweise Aufschlüsselung von verwendetem Code und nicht verwendetem Code.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Code Coverage-Bericht" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Code Coverage-Bericht  
:::image-end:::  

*   Die **URL** -Spalte ist die URL der Ressource, die analysiert wurde.  
*   In der Spalte **Typ** wird angegeben, ob die Ressource CSS, JavaScript oder beides enthält.  
*   Die Spalte " **Gesamt Bytes** " gibt die Gesamtgröße der Ressource in Bytes an.  
*   Die Spalte "nicht **verwendete Bytes** " gibt die Anzahl der Bytes an, die nicht verwendet wurden.  
*   Die letzte, unbenannte Spalte ist eine Visualisierung der Spalten **Gesamt Bytes** und **nicht verwendete Bytes** .  Der Rote Bereich der Leiste ist nicht verwendete Bytes.  Der grüne Abschnitt wird in Bytes verwendet.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  

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
