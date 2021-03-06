---
description: Anzeigen von SQL-Daten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von SQL mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 326fe492a3436a40d81c8e31db99a26da4ea054f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397552"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a>Anzeigen von SQL mit Microsoft Edge DevTools  

> [!WARNING]
> Die Web SQL wird [nicht beibehalten.][W3CWebSQLStatus]  

In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] verwenden, um Webdaten SQL untersuchen.  

## <a name="view-web-sql-data"></a>Anzeigen von SQL-Daten  

1.  Wählen Sie das **Tool Quellen** aus, um das Tool **Quellen zu** öffnen.  Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  
    
1.  Erweitern Sie **den Abschnitt SQL,** um Datenbanken und Tabellen anzeigen zu können.  In der folgenden Abbildung ist **unter html5meetup** eine Datenbank und **Räume** eine Tabelle.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Web SQL Bereich" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Der **Web SQL** Bereich  
    :::image-end:::  
    
1.  Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Anzeigen der Daten einer SQL-Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Anzeigen der Daten einer SQL-Tabelle  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a>Bearbeiten von SQL-Daten  

Sie können Webdaten nicht SQL bearbeiten, wenn Sie eine SQL -Tabelle anzeigen, z. B. oben.  Sie können jedoch Anweisungen aus der Web-SQL ausführen, die Tabellen bearbeiten oder löschen.  Navigieren Sie [zu Web SQL ausführen](#run-web-sql-queries).  

## <a name="run-web-sql-queries"></a>Ausführen von SQL-Abfragen  

1.  Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.  
1.  Geben Sie eine web SQL-Anweisung ein, und wählen Sie dann `Enter` aus, um sie zu ausführen.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a>Aktualisieren einer SQL-Tabelle  

DevTools aktualisiert Tabellen nicht in Echtzeit.  Führen Sie die folgenden Aktionen aus, um die Daten in einer Tabelle zu aktualisieren.  

1.  [Anzeigen der Daten in einer SQL Tabelle](#view-web-sql-data).  
1.  Wählen **Sie Aktualisieren** \( Aktualisieren ![ ][ImageRefreshIcon] \).  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a>Filtern von Spalten in einer SQL Tabelle  

1.  [Anzeigen der Daten in einer SQL Tabelle](#view-web-sql-data).  
1.  Verwenden Sie das **Textfeld Sichtbare Spalten,** um anzugeben, welche Spalten angezeigt werden sollen.  Geben Sie die Spaltennamen als CSV-Liste an.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Verwenden des Textfelds Sichtbare Spalten, um die Anzahl der angezeigten Spalten zu reduzieren" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Verwenden des **Textfelds** Sichtbare Spalten, um die Anzahl der angezeigten Spalten zu reduzieren  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a>Löschen aller SQL-Daten  

1.  Öffnen Sie den **Bereich Speicher** löschen.  
1.  Stellen Sie sicher, **dass das SQL** aktiviert ist.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Das Kontrollkästchen SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Kontrollkästchen **SQL** Web  
    :::image-end:::  
    
1.  Wählen **Sie Websitedaten löschen aus.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Die Schaltfläche Websitedaten löschen" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Die **Schaltfläche Websitedaten** löschen  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL Datenbank | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
