---
title: Anzeigen von WebSQL-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8b2e6d1a117e401f9e579cb28f81da9676eea979
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983460"
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





# Anzeigen von WebSQL-Daten mit Microsoft Edge devtools   



> [!WARNING]
> Die Web SQL-Spezifikation wird [nicht verwaltet][W3CWebSQLStatus].  

Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um Web SQL-Daten zu überprüfen.  

## Anzeigen von Web SQL-Daten   

1.  Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.  Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  
    
1.  Erweitern Sie den Abschnitt **Web SQL** , um Datenbanken und Tabellen anzuzeigen.  In der folgenden Abbildung ist unter **html5meetup** eine Datenbank, und **rooms** ist eine Tabelle.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Der Web SQL-Bereich" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Der **Web SQL-** Bereich  
    :::image-end:::  
    
1.  Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Anzeigen der Daten einer Web SQL-Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Anzeigen der Daten einer Web SQL-Tabelle  
    :::image-end:::  
    
## Bearbeiten von Web SQL-Daten   

Sie können keine Web SQL-Daten bearbeiten, wenn Sie eine Web SQL-Tabelle anzeigen, wie in **Abbildung 3 oben dargestellt** .  Sie können jedoch in der Web SQL-Konsole Anweisungen zum Bearbeiten oder Löschen von Tabellen ausführen.  Weitere Informationen finden Sie unter [Ausführen von WebSQL-Abfragen](#run-web-sql-queries).  

## Ausführen von Web SQL-Abfragen   

1.  Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.  
1.  Geben Sie eine Web SQL-Anweisung ein, und drücken Sie dann `Enter` , um Sie auszuführen.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle  
    :::image-end:::  
    
## Aktualisieren einer Web SQL-Tabelle   

DevTools aktualisiert Tabellen nicht in Echtzeit.  So aktualisieren Sie die Daten in einer Tabelle:  

1.  [Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)  
1.  Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.  
    
## Filtern von Spalten in einer SQL-Webtabelle   

1.  [Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)  
1.  Verwenden Sie das Textfeld **sichtbare Spalten** , um anzugeben, welche Spalten angezeigt werden sollen.  Geben Sie die Spaltennamen als CSV-Liste an.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Verwenden Sie das Textfeld "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern." lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Verwenden Sie das Textfeld " **sichtbare Spalten** ", um die Anzahl der angezeigten Spalten zu verringern.  
    :::image-end:::  
    
## Löschen aller Web SQL-Daten   

1.  Öffnen Sie den Bereich **Speicher löschen** .  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Web SQL** aktiviert ist.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Das Web SQL-Kontrollkästchen" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Das **Web SQL-** Kontrollkästchen  
    :::image-end:::  
    
1.  Wählen Sie **Website Daten löschen**aus.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Schaltfläche "Website Daten löschen"" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Schaltfläche " **Website Daten löschen** "  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL-Datenbank | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
