---
description: Informationen zum Anzeigen von WebSQL-Daten aus dem Anwendungs Panel von Microsoft Edge devtools
title: Anzeigen von WebSQL-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 802f21cb4cadfa3ee08ddd8feeea8b8132551740
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231174"
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

# <span data-ttu-id="e154e-104">Anzeigen von WebSQL-Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="e154e-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="e154e-105">Die Web SQL-Spezifikation wird [nicht verwaltet][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="e154e-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="e154e-106">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um Web SQL-Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e154e-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="e154e-107">Anzeigen von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="e154e-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="e154e-108">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Tool zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e154e-108">Select the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="e154e-109">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e154e-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="e154e-111">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="e154e-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e154e-112">Erweitern Sie den Abschnitt **Web SQL** , um Datenbanken und Tabellen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e154e-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="e154e-113">In der folgenden Abbildung ist unter **html5meetup** eine Datenbank, und **rooms** ist eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e154e-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Der Web SQL-Bereich" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="e154e-115">Der **Web SQL-** Bereich</span><span class="sxs-lookup"><span data-stu-id="e154e-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e154e-116">Wählen Sie eine Tabelle aus, um die Daten für diese Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e154e-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Anzeigen der Daten einer Web SQL-Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="e154e-118">Anzeigen der Daten einer Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e154e-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e154e-119">Bearbeiten von Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="e154e-119">Edit Web SQL data</span></span>  

<span data-ttu-id="e154e-120">Sie können keine Web SQL-Daten bearbeiten, wenn Sie eine Web SQL-Tabelle anzeigen, wie im vorherigen Beispiel zuvor.</span><span class="sxs-lookup"><span data-stu-id="e154e-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="e154e-121">Sie können jedoch in der Web SQL-Konsole Anweisungen zum Bearbeiten oder Löschen von Tabellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="e154e-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="e154e-122">Weitere Informationen finden Sie unter [Ausführen von WebSQL-Abfragen](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="e154e-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="e154e-123">Ausführen von Web SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="e154e-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="e154e-124">Wählen Sie eine Datenbank aus, um eine Konsole für diese Datenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e154e-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="e154e-125">Geben Sie eine Web SQL-Anweisung ein, und wählen Sie Sie aus, `Enter` um Sie auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e154e-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="e154e-127">Verwenden der Web SQL-Konsole zum Löschen einer Zeile aus einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="e154e-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e154e-128">Aktualisieren einer Web SQL-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e154e-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="e154e-129">DevTools aktualisiert Tabellen nicht in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="e154e-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="e154e-130">Führen Sie die folgenden Aktionen aus, um die Daten in einer Tabelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e154e-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="e154e-131">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="e154e-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="e154e-132">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="e154e-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="e154e-133">Filtern von Spalten in einer SQL-Webtabelle</span><span class="sxs-lookup"><span data-stu-id="e154e-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="e154e-134">[Anzeigen der Daten in einer SQL-Webtabelle](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="e154e-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="e154e-135">Verwenden Sie das Textfeld **sichtbare Spalten** , um anzugeben, welche Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e154e-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="e154e-136">Geben Sie die Spaltennamen als CSV-Liste an.</span><span class="sxs-lookup"><span data-stu-id="e154e-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Verwenden Sie das Textfeld "sichtbare Spalten", um die Anzahl der angezeigten Spalten zu verringern." lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="e154e-138">Verwenden Sie das Textfeld " **sichtbare Spalten** ", um die Anzahl der angezeigten Spalten zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e154e-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e154e-139">Löschen aller Web SQL-Daten</span><span class="sxs-lookup"><span data-stu-id="e154e-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="e154e-140">Öffnen Sie den Bereich **Speicher löschen** .</span><span class="sxs-lookup"><span data-stu-id="e154e-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="e154e-141">Stellen Sie sicher, dass das Kontrollkästchen **Web SQL** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e154e-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Das Web SQL-Kontrollkästchen" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="e154e-143">Das **Web SQL-** Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="e154e-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e154e-144">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="e154e-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Schaltfläche "Website Daten löschen"" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="e154e-146">Schaltfläche " **Website Daten löschen** "</span><span class="sxs-lookup"><span data-stu-id="e154e-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e154e-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e154e-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL-Datenbank | W3C"  

> [!NOTE]
> <span data-ttu-id="e154e-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e154e-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e154e-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/websql) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e154e-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e154e-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e154e-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
