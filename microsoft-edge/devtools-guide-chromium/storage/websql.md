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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a><span data-ttu-id="6666f-104">Anzeigen von SQL mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6666f-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="6666f-105">Die Web SQL wird [nicht beibehalten.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="6666f-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="6666f-106">In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] verwenden, um Webdaten SQL untersuchen.</span><span class="sxs-lookup"><span data-stu-id="6666f-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <a name="view-web-sql-data"></a><span data-ttu-id="6666f-107">Anzeigen von SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="6666f-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="6666f-108">Wählen Sie das **Tool Quellen** aus, um das Tool **Quellen zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="6666f-108">Choose the **Sources** tool to open the **Sources** tool.</span></span>  <span data-ttu-id="6666f-109">Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6666f-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="6666f-111">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="6666f-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6666f-112">Erweitern Sie **den Abschnitt SQL,** um Datenbanken und Tabellen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="6666f-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="6666f-113">In der folgenden Abbildung ist **unter html5meetup** eine Datenbank und **Räume** eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6666f-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Web SQL Bereich" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="6666f-115">Der **Web SQL** Bereich</span><span class="sxs-lookup"><span data-stu-id="6666f-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6666f-116">Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="6666f-116">Choose a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Anzeigen der Daten einer SQL-Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="6666f-118">Anzeigen der Daten einer SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6666f-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a><span data-ttu-id="6666f-119">Bearbeiten von SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="6666f-119">Edit Web SQL data</span></span>  

<span data-ttu-id="6666f-120">Sie können Webdaten nicht SQL bearbeiten, wenn Sie eine SQL -Tabelle anzeigen, z. B. oben.</span><span class="sxs-lookup"><span data-stu-id="6666f-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="6666f-121">Sie können jedoch Anweisungen aus der Web-SQL ausführen, die Tabellen bearbeiten oder löschen.</span><span class="sxs-lookup"><span data-stu-id="6666f-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="6666f-122">Navigieren Sie [zu Web SQL ausführen](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="6666f-122">Navigate to [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <a name="run-web-sql-queries"></a><span data-ttu-id="6666f-123">Ausführen von SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="6666f-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="6666f-124">Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6666f-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="6666f-125">Geben Sie eine web SQL-Anweisung ein, und wählen Sie dann `Enter` aus, um sie zu ausführen.</span><span class="sxs-lookup"><span data-stu-id="6666f-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="6666f-127">Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="6666f-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a><span data-ttu-id="6666f-128">Aktualisieren einer SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6666f-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="6666f-129">DevTools aktualisiert Tabellen nicht in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="6666f-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="6666f-130">Führen Sie die folgenden Aktionen aus, um die Daten in einer Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6666f-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="6666f-131">[Anzeigen der Daten in einer SQL Tabelle](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="6666f-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="6666f-132">Wählen **Sie Aktualisieren** \( Aktualisieren ![ ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6666f-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a><span data-ttu-id="6666f-133">Filtern von Spalten in einer SQL Tabelle</span><span class="sxs-lookup"><span data-stu-id="6666f-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="6666f-134">[Anzeigen der Daten in einer SQL Tabelle](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="6666f-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="6666f-135">Verwenden Sie das **Textfeld Sichtbare Spalten,** um anzugeben, welche Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6666f-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="6666f-136">Geben Sie die Spaltennamen als CSV-Liste an.</span><span class="sxs-lookup"><span data-stu-id="6666f-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Verwenden des Textfelds Sichtbare Spalten, um die Anzahl der angezeigten Spalten zu reduzieren" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="6666f-138">Verwenden des **Textfelds** Sichtbare Spalten, um die Anzahl der angezeigten Spalten zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="6666f-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a><span data-ttu-id="6666f-139">Löschen aller SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="6666f-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="6666f-140">Öffnen Sie den **Bereich Speicher** löschen.</span><span class="sxs-lookup"><span data-stu-id="6666f-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="6666f-141">Stellen Sie sicher, **dass das SQL** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6666f-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Das Kontrollkästchen SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="6666f-143">Kontrollkästchen **SQL** Web</span><span class="sxs-lookup"><span data-stu-id="6666f-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6666f-144">Wählen **Sie Websitedaten löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="6666f-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Die Schaltfläche Websitedaten löschen" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="6666f-146">Die **Schaltfläche Websitedaten** löschen</span><span class="sxs-lookup"><span data-stu-id="6666f-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6666f-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="6666f-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL Datenbank | W3C"  

> [!NOTE]
> <span data-ttu-id="6666f-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6666f-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6666f-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="6666f-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6666f-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6666f-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
