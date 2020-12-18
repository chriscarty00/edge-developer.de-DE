---
description: Informationen zum Anzeigen und Ändern von IndexedDB-Daten mit dem Anwendungs Panel und Snippets.
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231202"
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

# <span data-ttu-id="b3373-104">Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="b3373-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b3373-105">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [IndexedDB][MDNIndexedDBAPI] -Daten anzuzeigen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b3373-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="b3373-106">Es wird davon ausgegangen, dass Sie mit devtools vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="b3373-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="b3373-107">Außerdem wird davon ausgegangen, dass Sie mit IndexedDB vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="b3373-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="b3373-108">Wenn dies nicht der Fall ist, navigieren Sie zu [using IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="b3373-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="b3373-109">Anzeigen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="b3373-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="b3373-110">Wählen Sie die Registerkarte **Anwendung** aus, um das **Anwendungs** Tool zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b3373-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="b3373-111">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b3373-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="b3373-113">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="b3373-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b3373-114">Erweitern Sie das **IndexedDB** -Menü, um zu überprüfen, welche Datenbanken verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b3373-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Das IndexedDB-Menü" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="b3373-116">Das **IndexedDB** -Menü</span><span class="sxs-lookup"><span data-stu-id="b3373-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="b3373-117">\ ( ![ Datenbanksymbol ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` stellt eine Datenbank dar, wobei `notes` der Name der Datenbank und `https://mdn.github.io` der Ursprung ist, der auf die Datenbank zugreift.</span><span class="sxs-lookup"><span data-stu-id="b3373-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="b3373-118">\ ( ![ Objektspeicher Symbol ][ImageObjectStoreIcon] \) `notes` ist ein Objektspeicher.</span><span class="sxs-lookup"><span data-stu-id="b3373-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="b3373-119">**Titel** und **Text** sind [Indizes][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="b3373-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b3373-120">**Bekannte Einschränkung**  Datenbanken von Drittanbietern werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3373-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="b3373-121">Wenn Sie beispielsweise eine Anzeige in `<iframe>` Ihre Seite einbetten und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="b3373-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="b3373-122">Navigieren Sie zu [Issue #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="b3373-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="b3373-123">Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b3373-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Die Notes-Datenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="b3373-125">Die **Notes** -Datenbank</span><span class="sxs-lookup"><span data-stu-id="b3373-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b3373-126">Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b3373-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b3373-127">IndexedDB-Daten werden in Echtzeit nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3373-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="b3373-128">Navigieren Sie zu [IndexedDB-Daten aktualisieren](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="b3373-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Der Notizen Objektspeicher" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="b3373-130">Der **Notizen** Objektspeicher</span><span class="sxs-lookup"><span data-stu-id="b3373-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="b3373-131">**Gesamt** Anzahl der Einträge ist die Gesamtzahl der Schlüssel-Wert-Paare im Objektspeicher.</span><span class="sxs-lookup"><span data-stu-id="b3373-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="b3373-132">Der **Schlüsselgenerator Wert** ist der nächste verfügbare Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b3373-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="b3373-133">Das Feld wird nur angezeigt, wenn [Schlüsselgeneratoren][MDNBasicConceptsKeyGenerator]verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3373-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="b3373-134">Wählen Sie in der Spalte **Wert** eine Zelle aus, um den Wert zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b3373-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Anzeigen eines IndexedDB-Werts" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="b3373-136">Anzeigen eines **IndexedDB** -Werts</span><span class="sxs-lookup"><span data-stu-id="b3373-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b3373-137">Wählen Sie in der folgenden Abbildung einen Index wie **Titel** oder **Text** aus, um den Objektspeicher entsprechend den Werten dieses Indexes zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="b3373-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Sortieren eines Objektspeichers anhand eines Indexes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="b3373-139">Sortieren eines Objektspeichers anhand eines Indexes</span><span class="sxs-lookup"><span data-stu-id="b3373-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b3373-140">Aktualisieren von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="b3373-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="b3373-141">IndexedDB-Werte im **Anwendungs** Tool werden in Echtzeit nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3373-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="b3373-142">Wählen Sie **Aktualisieren** \ ( ![ Aktualisieren \) aus, wenn Sie ][ImageReloadIcon] einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und wählen Sie **Datenbank aktualisieren** aus, um alle Daten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b3373-142">Choose **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Anzeigen einer Datenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="b3373-144">Anzeigen einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="b3373-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="b3373-145">Bearbeiten von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="b3373-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="b3373-146">IndexedDB-Schlüssel und-Werte können vom **Anwendungs** Tool nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b3373-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="b3373-147">Da devtools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in devtools ausführen, um IndexedDB-Daten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b3373-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="b3373-148">Bearbeiten von IndexedDB-Daten mit Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="b3373-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="b3373-149">[Snippets][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von JavaScript-Codeblöcken in devtools.</span><span class="sxs-lookup"><span data-stu-id="b3373-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="b3373-150">Wenn Sie einen Ausschnitt ausführen, wird das Ergebnis in der **Konsole**protokolliert.</span><span class="sxs-lookup"><span data-stu-id="b3373-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="b3373-151">Sie können einen Ausschnitt zum Ausführen von JavaScript-Code zum Bearbeiten einer IndexedDB-Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3373-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Verwenden eines Snippets für die Interaktion mit IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="b3373-153">Verwenden eines Snippets für die Interaktion mit IndexedDB</span><span class="sxs-lookup"><span data-stu-id="b3373-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="b3373-154">Löschen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="b3373-154">Delete IndexedDB data</span></span>  

### <span data-ttu-id="b3373-155">Löschen eines IndexedDB-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="b3373-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="b3373-156">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="b3373-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="b3373-157">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="b3373-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="b3373-158">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="b3373-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen." lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="b3373-160">Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b3373-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b3373-161">Drücken Sie die Eingabe `Delete` Taste, oder wählen Sie **Ausgewählte löschen** ( ![ Ausgewählte löschen ][ImageDeleteIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="b3373-161">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="b3373-163">Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde</span><span class="sxs-lookup"><span data-stu-id="b3373-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b3373-164">Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher</span><span class="sxs-lookup"><span data-stu-id="b3373-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="b3373-165">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="b3373-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Anzeigen eines Objektspeichers" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="b3373-167">Anzeigen eines Objektspeichers</span><span class="sxs-lookup"><span data-stu-id="b3373-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b3373-168">Wählen Sie **Objektspeicher löschen** \ ( ![ Objektspeicher löschen ][ImageClearIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="b3373-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="b3373-169">Löschen einer IndexedDB-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b3373-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="b3373-170">[Zeigen Sie die IndexedDB-Datenbank](#view-indexeddb-data) an, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="b3373-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="b3373-171">Wählen Sie **Datenbank löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="b3373-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Schaltfläche "Datenbank löschen"" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="b3373-173">Schaltfläche " **Datenbank löschen** "</span><span class="sxs-lookup"><span data-stu-id="b3373-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b3373-174">Löschen des gesamten IndexedDB-Speichers</span><span class="sxs-lookup"><span data-stu-id="b3373-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="b3373-175">Öffnen Sie den Bereich **Speicher löschen** .</span><span class="sxs-lookup"><span data-stu-id="b3373-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="b3373-176">Stellen Sie sicher, dass das Kontrollkästchen **IndexedDB** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3373-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="b3373-177">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="b3373-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Der Bereich "Speicher löschen"" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="b3373-179">Der Bereich " **Speicher löschen** "</span><span class="sxs-lookup"><span data-stu-id="b3373-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b3373-180">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="b3373-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-devtools: Anzeigen von IFRAME-IndexedDB-Datenbanken – Chrom-Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Schlüssel Generator – grundlegende Konzepte | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Verwenden eines Index-using IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="b3373-188">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3373-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b3373-189">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3373-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b3373-191">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b3373-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
