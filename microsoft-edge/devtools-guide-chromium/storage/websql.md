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





# <span data-ttu-id="2b6b3-103">Anzeigen von WebSQL-Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="2b6b3-103">View Web SQL data with Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="2b6b3-104">Die Web SQL-Spezifikation wird [nicht verwaltet][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="2b6b3-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="2b6b3-105">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um Web SQL-Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="2b6b3-106">Anzeigen von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="2b6b3-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="2b6b3-107">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="2b6b3-108">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="2b6b3-110">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="2b6b3-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2b6b3-111">Erweitern Sie den Abschnitt **Web SQL** , um Datenbanken und Tabellen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-111">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="2b6b3-112">In der folgenden Abbildung ist unter **html5meetup** eine Datenbank, und **rooms** ist eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-112">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Der Web SQL-Bereich" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="2b6b3-114">Der **Web SQL-** Bereich</span><span class="sxs-lookup"><span data-stu-id="2b6b3-114">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2b6b3-115">Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-115">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Anzeigen der Daten einer Web SQL-Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="2b6b3-117">Anzeigen der Daten einer Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2b6b3-117">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2b6b3-118">Bearbeiten von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="2b6b3-118">Edit Web SQL data</span></span>   

<span data-ttu-id="2b6b3-119">Sie können keine Web SQL-Daten bearbeiten, wenn Sie eine Web SQL-Tabelle anzeigen, wie in **Abbildung 3 oben dargestellt** .</span><span class="sxs-lookup"><span data-stu-id="2b6b3-119">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="2b6b3-120">Sie können jedoch in der Web SQL-Konsole Anweisungen zum Bearbeiten oder Löschen von Tabellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-120">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="2b6b3-121">Weitere Informationen finden Sie unter [Ausführen von WebSQL-Abfragen](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="2b6b3-121">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="2b6b3-122">Ausführen von Web SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="2b6b3-122">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="2b6b3-123">Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-123">Select a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="2b6b3-124">Geben Sie eine Web SQL-Anweisung ein, und drücken Sie dann `Enter` , um Sie auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-124">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="2b6b3-126">Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="2b6b3-126">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2b6b3-127">Aktualisieren einer Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2b6b3-127">Refresh a Web SQL table</span></span>   

<span data-ttu-id="2b6b3-128">DevTools aktualisiert Tabellen nicht in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-128">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="2b6b3-129">So aktualisieren Sie die Daten in einer Tabelle:</span><span class="sxs-lookup"><span data-stu-id="2b6b3-129">To update the data in a table:</span></span>  

1.  <span data-ttu-id="2b6b3-130">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="2b6b3-130">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="2b6b3-131">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-131">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="2b6b3-132">Filtern von Spalten in einer SQL-Webtabelle</span><span class="sxs-lookup"><span data-stu-id="2b6b3-132">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="2b6b3-133">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="2b6b3-133">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="2b6b3-134">Verwenden Sie das Textfeld **sichtbare Spalten** , um anzugeben, welche Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-134">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="2b6b3-135">Geben Sie die Spaltennamen als CSV-Liste an.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-135">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Verwenden Sie das Textfeld "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern." lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="2b6b3-137">Verwenden Sie das Textfeld " **sichtbare Spalten** ", um die Anzahl der angezeigten Spalten zu verringern.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-137">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2b6b3-138">Löschen aller Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="2b6b3-138">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="2b6b3-139">Öffnen Sie den Bereich **Speicher löschen** .</span><span class="sxs-lookup"><span data-stu-id="2b6b3-139">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="2b6b3-140">Stellen Sie sicher, dass das Kontrollkästchen **Web SQL** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-140">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Das Web SQL-Kontrollkästchen" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="2b6b3-142">Das **Web SQL-** Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="2b6b3-142">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2b6b3-143">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-143">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Schaltfläche "Website Daten löschen"" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="2b6b3-145">Schaltfläche " **Website Daten löschen** "</span><span class="sxs-lookup"><span data-stu-id="2b6b3-145">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL-Datenbank | W3C"  

> [!NOTE]
> <span data-ttu-id="2b6b3-148">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2b6b3-149">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b6b3-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="2b6b3-151">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2b6b3-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
