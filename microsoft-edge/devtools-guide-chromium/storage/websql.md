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





# <span data-ttu-id="71ae2-103">Anzeigen von WebSQL-Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="71ae2-103">View Web SQL Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="71ae2-104">Die Web SQL-Spezifikation wird [nicht verwaltet][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="71ae2-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="71ae2-105">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um Web SQL-Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="71ae2-106">Anzeigen von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="71ae2-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="71ae2-107">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="71ae2-108">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="71ae2-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-109">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="71ae2-109">Figure 1</span></span>  
    > <span data-ttu-id="71ae2-110">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="71ae2-110">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifestPane]  
    
1.  <span data-ttu-id="71ae2-112">Erweitern Sie den Abschnitt **Web SQL** , um Datenbanken und Tabellen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="71ae2-113">In [Abbildung 2](#figure-2) unten ist **html5meetup** eine Datenbank, und **rooms** ist eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="71ae2-113">In [Figure 2](#figure-2) below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-114">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="71ae2-114">Figure 2</span></span>  
    > <span data-ttu-id="71ae2-115">Der Web SQL-Bereich</span><span class="sxs-lookup"><span data-stu-id="71ae2-115">The Web SQL pane</span></span>  
    > ![Der Web SQL-Bereich][ImageWebSQLPane]  

1.  <span data-ttu-id="71ae2-117">Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-117">Select a table to view the data for that table.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-118">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="71ae2-118">Figure 3</span></span>  
    > <span data-ttu-id="71ae2-119">Anzeigen der Daten der **rooms** Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="71ae2-119">Viewing the data of the **rooms** Web SQL table</span></span>  
    > ![Anzeigen der Daten einer Web SQL-Tabelle][ImageWebSQLTable]  

## <span data-ttu-id="71ae2-121">Bearbeiten von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="71ae2-121">Edit Web SQL data</span></span>   

<span data-ttu-id="71ae2-122">Sie können keine Web SQL-Daten bearbeiten, wenn Sie eine Web SQL-Tabelle anzeigen, wie in **Abbildung 3 oben dargestellt** .</span><span class="sxs-lookup"><span data-stu-id="71ae2-122">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="71ae2-123">Sie können jedoch in der Web SQL-Konsole Anweisungen zum Bearbeiten oder Löschen von Tabellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-123">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="71ae2-124">Weitere Informationen finden Sie unter [Ausführen von WebSQL-Abfragen](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="71ae2-124">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="71ae2-125">Ausführen von Web SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="71ae2-125">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="71ae2-126">Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-126">Select a database to open a console for that database.</span></span>  

1.  <span data-ttu-id="71ae2-127">Geben Sie eine Web SQL-Anweisung ein, und drücken Sie dann `Enter` , um Sie auszuführen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-127">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-128">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="71ae2-128">Figure 4</span></span>  
    > <span data-ttu-id="71ae2-129">Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus der Tabelle " **Räume** "</span><span class="sxs-lookup"><span data-stu-id="71ae2-129">Using the Web SQL Console to delete a row from the **rooms** table</span></span>  
    > ![Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle][ImageWebSQLEdit]  

## <span data-ttu-id="71ae2-131">Aktualisieren einer Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="71ae2-131">Refresh a Web SQL table</span></span>   

<span data-ttu-id="71ae2-132">DevTools aktualisiert Tabellen nicht in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="71ae2-132">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="71ae2-133">So aktualisieren Sie die Daten in einer Tabelle:</span><span class="sxs-lookup"><span data-stu-id="71ae2-133">To update the data in a table:</span></span>  

1.  <span data-ttu-id="71ae2-134">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="71ae2-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="71ae2-135">Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="71ae2-135">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="71ae2-136">Filtern von Spalten in einer SQL-Webtabelle</span><span class="sxs-lookup"><span data-stu-id="71ae2-136">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="71ae2-137">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="71ae2-137">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="71ae2-138">Verwenden Sie das Textfeld **sichtbare Spalten** , um anzugeben, welche Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71ae2-138">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="71ae2-139">Geben Sie die Spaltennamen als CSV-Liste an.</span><span class="sxs-lookup"><span data-stu-id="71ae2-139">Provide the column names as a CSV list.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-140">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="71ae2-140">Figure 5</span></span>  
    > <span data-ttu-id="71ae2-141">Verwenden des Textfelds " **sichtbare Spalten** ", um nur die `room_name` und `last_updated` Spalten anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="71ae2-141">Using the **Visible Columns** text box to only show the `room_name` and `last_updated` columns</span></span>  
    > ![Verwenden des Textfelds "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern][ImageWebSQLFilter]  

## <span data-ttu-id="71ae2-143">Löschen aller Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="71ae2-143">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="71ae2-144">Öffnen Sie den Bereich **Speicher löschen** .</span><span class="sxs-lookup"><span data-stu-id="71ae2-144">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="71ae2-145">Stellen Sie sicher, dass das Kontrollkästchen **Web SQL** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="71ae2-145">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-146">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="71ae2-146">Figure 6</span></span>  
    > <span data-ttu-id="71ae2-147">Das **Web SQL-** Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="71ae2-147">The **Web SQL** checkbox</span></span>  
    > ![Das Web SQL-Kontrollkästchen][ImageWebSQLCheckbox]  

1.  <span data-ttu-id="71ae2-149">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="71ae2-149">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="71ae2-150">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="71ae2-150">Figure 7</span></span>  
    > <span data-ttu-id="71ae2-151">Schaltfläche " **Website Daten löschen** "</span><span class="sxs-lookup"><span data-stu-id="71ae2-151">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="71ae2-162">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71ae2-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71ae2-163">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="71ae2-163">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="71ae2-165">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71ae2-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
