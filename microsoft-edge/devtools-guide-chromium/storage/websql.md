---
title: Anzeigen von WebSQL-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612060"
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
    
    > ##### Abbildung1  
    > Bereich ' Manifest '  
    > ![Bereich ' Manifest '][ImageManifestPane]  
    
1.  Erweitern Sie den Abschnitt **Web SQL** , um Datenbanken und Tabellen anzuzeigen.  In [Abbildung 2](#figure-2) unten ist **html5meetup** eine Datenbank, und **rooms** ist eine Tabelle.  
    
    > ##### Abbildung2  
    > Der Web SQL-Bereich  
    > ![Der Web SQL-Bereich][ImageWebSQLPane]  

1.  Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzuzeigen.  
    
    > ##### Abbildung 3  
    > Anzeigen der Daten der **rooms** Web SQL-Tabelle  
    > ![Anzeigen der Daten einer Web SQL-Tabelle][ImageWebSQLTable]  

## Bearbeiten von Web SQL-Daten   

Sie können keine Web SQL-Daten bearbeiten, wenn Sie eine Web SQL-Tabelle anzeigen, wie in **Abbildung 3 oben dargestellt** .  Sie können jedoch in der Web SQL-Konsole Anweisungen zum Bearbeiten oder Löschen von Tabellen ausführen.  Weitere Informationen finden Sie unter [Ausführen von WebSQL-Abfragen](#run-web-sql-queries).  

## Ausführen von Web SQL-Abfragen   

1.  Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.  

1.  Geben Sie eine Web SQL-Anweisung ein, und drücken Sie dann `Enter` , um Sie auszuführen.  
    
    > ##### Abbildung4  
    > Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus der Tabelle " **Räume** "  
    > ![Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle][ImageWebSQLEdit]  

## Aktualisieren einer Web SQL-Tabelle   

DevTools aktualisiert Tabellen nicht in Echtzeit.  So aktualisieren Sie die Daten in einer Tabelle:  

1.  [Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)  
1.  Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .  

## Filtern von Spalten in einer SQL-Webtabelle   

1.  [Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)  
1.  Verwenden Sie das Textfeld **sichtbare Spalten** , um anzugeben, welche Spalten angezeigt werden sollen.  Geben Sie die Spaltennamen als CSV-Liste an.  
    
    > ##### Abbildung5  
    > Verwenden des Textfelds " **sichtbare Spalten** ", um nur die `room_name` und `last_updated` Spalten anzuzeigen  
    > ![Verwenden des Textfelds "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern][ImageWebSQLFilter]  

## Löschen aller Web SQL-Daten   

1.  Öffnen Sie den Bereich **Speicher löschen** .  
1.  Stellen Sie sicher, dass das Kontrollkästchen **Web SQL** aktiviert ist.  
    
    > ##### Abbildung6  
    > Das **Web SQL-** Kontrollkästchen  
    > ![Das Web SQL-Kontrollkästchen][ImageWebSQLCheckbox]  

1.  Wählen Sie **Website Daten löschen**aus.  
    
    > ##### Abbildung7  
    > Schaltfläche " **Website Daten löschen** "  
    > ![Schaltfläche "Website Daten löschen"][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Abbildung 2: der Web SQL-Bereich"  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Abbildung 3: Anzeigen der Daten einer Web SQL-Tabelle"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Abbildung 4: Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Abbildung 5: Verwenden des Textfelds "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Abbildung 6: das Kontrollkästchen "Web SQL""  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Abbildung 7: die Schaltfläche "Website Daten löschen""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

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
