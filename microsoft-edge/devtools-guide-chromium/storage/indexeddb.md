---
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612088"
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





# <span data-ttu-id="f5c42-103">Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="f5c42-103">View And Change IndexedDB Data With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="f5c42-104">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [IndexedDB][MDNIndexedDBAPI] -Daten anzuzeigen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f5c42-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="f5c42-105">Es wird davon ausgegangen, dass Sie mit devtools vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="f5c42-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="f5c42-106">Außerdem wird davon ausgegangen, dass Sie mit IndexedDB vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="f5c42-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="f5c42-107">Wenn dies nicht der Fall ist, lesen Sie [Verwenden von IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="f5c42-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="f5c42-108">Anzeigen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f5c42-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="f5c42-109">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5c42-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="f5c42-110">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f5c42-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="f5c42-111">Figure 1</span></span>  
    > <span data-ttu-id="f5c42-112">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="f5c42-112">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  <span data-ttu-id="f5c42-114">Erweitern Sie das **IndexedDB** -Menü, um zu sehen, welche Datenbanken verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f5c42-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-115">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="f5c42-115">Figure 2</span></span>  
    > <span data-ttu-id="f5c42-116">Das **IndexedDB** -Menü</span><span class="sxs-lookup"><span data-stu-id="f5c42-116">The **IndexedDB** menu</span></span>  
    > ![Das IndexedDB-Menü][ImageIndexedDBMenu]  
    
    *   ![<span data-ttu-id="f5c42-118">Das Datenbanksymbol ][ImageDatabaseIcon] `notes - https://mdn.github.io` stellt eine Datenbank dar, wobei `notes` der Name der Datenbank und `https://mdn.github.io` der Ursprung für den Zugriff auf die Datenbank ist.</span><span class="sxs-lookup"><span data-stu-id="f5c42-118">Database icon][ImageDatabaseIcon] `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   ![<span data-ttu-id="f5c42-119">Das Objektspeicher Symbol ][ImageObjectStoreIcon] `notes` ist ein Objektspeicher.</span><span class="sxs-lookup"><span data-stu-id="f5c42-119">Object Store icon][ImageObjectStoreIcon] `notes` is an object store.</span></span>  
    *   <span data-ttu-id="f5c42-120">**Titel** und **Text** sind [Indizes][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="f5c42-120">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f5c42-121">**Bekannte Einschränkung**  Datenbanken von Drittanbietern werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c42-121">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="f5c42-122">Wenn Sie beispielsweise eine Anzeige in `<iframe>` Ihre Seite einbetten und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f5c42-122">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="f5c42-123">Weitere Informationen finden Sie unter [Problem #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="f5c42-123">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="f5c42-124">Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5c42-124">Select a database to see the origin and version number.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-125">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="f5c42-125">Figure 3</span></span>  
    > <span data-ttu-id="f5c42-126">Die **Notes** -Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5c42-126">The **notes** database</span></span>  
    > ![Die Notes-Datenbank][ImageIndexedDBDatabase]  
    
1.  <span data-ttu-id="f5c42-128">Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5c42-128">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f5c42-129">IndexedDB-Daten werden in Echtzeit nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f5c42-129">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="f5c42-130">Siehe [Aktualisieren von IndexedDB-Daten](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f5c42-130">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="f5c42-131">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="f5c42-131">Figure 4</span></span>  
    > <span data-ttu-id="f5c42-132">Der **Notizen** Objektspeicher</span><span class="sxs-lookup"><span data-stu-id="f5c42-132">The **notes** object store</span></span>  
    > ![Der Notizen Objektspeicher][ImageIndexedDBObjectStore]  

    *   <span data-ttu-id="f5c42-134">**Gesamt** Anzahl der Einträge ist die Gesamtzahl der Schlüssel-Wert-Paare im Objektspeicher.</span><span class="sxs-lookup"><span data-stu-id="f5c42-134">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="f5c42-135">Der **Schlüsselgenerator Wert** ist der nächste verfügbare Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f5c42-135">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="f5c42-136">Dieses Feld wird nur angezeigt, wenn [Schlüsselgeneratoren][MDNBasicConceptsKeyGenerator]verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5c42-136">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  

1.  <span data-ttu-id="f5c42-137">Wählen Sie in der Spalte **Wert** eine Zelle aus, um diesen Wert zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="f5c42-137">Select a cell in the **Value** column to expand that value.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-138">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="f5c42-138">Figure 5</span></span>  
    > <span data-ttu-id="f5c42-139">Anzeigen eines IndexedDB-Werts</span><span class="sxs-lookup"><span data-stu-id="f5c42-139">Viewing an IndexedDB value</span></span>  
    > ![Anzeigen eines IndexedDB-Werts][ImageIndexedBDValue]  
    
1.  <span data-ttu-id="f5c42-141">Wählen Sie einen Index wie **Titel** oder **Textkörper** in [Abbildung 6](#figure-6)aus, um den Objektspeicher entsprechend den Werten dieses Indexes zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="f5c42-141">Select an index, such as **title** or **body** in [Figure 6](#figure-6), to sort the object store according to the values of that index.</span></span>  
   
    > ##### <span data-ttu-id="f5c42-142">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="f5c42-142">Figure 6</span></span>  
    > <span data-ttu-id="f5c42-143">Ein Objektspeicher, der alphabetisch nach dem **Titel** Schlüssel sortiert ist</span><span class="sxs-lookup"><span data-stu-id="f5c42-143">An object store that is sorted alphabetically according to the **title** key</span></span>  
    > ![Sortieren eines Objektspeichers anhand eines Indexes][ImageIndexedDBIndex]  

## <span data-ttu-id="f5c42-145">Aktualisieren von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f5c42-145">Refresh IndexedDB data</span></span>   

<span data-ttu-id="f5c42-146">IndexedDB-Werte im **Anwendungs** Panel werden nicht in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f5c42-146">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="f5c42-147">Wählen **Sie Aktualisierung aktualisieren** aus, ![ Wenn Sie ][ImageReloadIcon] einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und klicken Sie auf **Datenbank aktualisieren** , um alle Daten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f5c42-147">Select **Refresh** ![Refresh][ImageReloadIcon] when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

> ##### <span data-ttu-id="f5c42-148">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="f5c42-148">Figure 7</span></span>  
> <span data-ttu-id="f5c42-149">Anzeigen einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5c42-149">Viewing a database</span></span>  
> ![Anzeigen einer Datenbank][ImageIndexedDBDatabase2]  

## <span data-ttu-id="f5c42-151">Bearbeiten von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f5c42-151">Edit IndexedDB data</span></span>   

<span data-ttu-id="f5c42-152">IndexedDB-Schlüssel und-Werte können im **Anwendungs** Panel nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f5c42-152">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="f5c42-153">Da devtools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in devtools ausführen, um IndexedDB-Daten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5c42-153">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="f5c42-154">Bearbeiten von IndexedDB-Daten mit Ausschnitten</span><span class="sxs-lookup"><span data-stu-id="f5c42-154">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="f5c42-155">[Snippets][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von JavaScript-Codeblöcken in devtools.</span><span class="sxs-lookup"><span data-stu-id="f5c42-155">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="f5c42-156">Wenn Sie einen Ausschnitt ausführen, wird das Ergebnis in der **Konsole**protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f5c42-156">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="f5c42-157">Sie können einen Ausschnitt zum Ausführen von JavaScript-Code zum Bearbeiten einer IndexedDB-Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5c42-157">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

> ##### <span data-ttu-id="f5c42-158">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="f5c42-158">Figure 8</span></span>  
> <span data-ttu-id="f5c42-159">Verwenden eines Snippets für die Interaktion mit IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f5c42-159">Using a Snippet to interact with IndexedDB</span></span>  
> ![Verwenden eines Snippets für die Interaktion mit IndexedDB][ImageIndexedDBSnippet]  

## <span data-ttu-id="f5c42-161">Löschen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f5c42-161">Delete IndexedDB data</span></span>   

### <span data-ttu-id="f5c42-162">Löschen eines IndexedDB-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="f5c42-162">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="f5c42-163">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="f5c42-163">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="f5c42-164">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f5c42-164">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="f5c42-165">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="f5c42-165">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-166">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="f5c42-166">Figure 9</span></span>  
    > <span data-ttu-id="f5c42-167">Auswählen eines Schlüssel-Wert-Paars, um es zu löschen</span><span class="sxs-lookup"><span data-stu-id="f5c42-167">Selecting a key-value pair in order to delete it</span></span>  
    > ![Auswählen eines Schlüssel-Wert-Paars, um es zu löschen][ImageIndexedDBKeyValuePair]  

1.  <span data-ttu-id="f5c42-169">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen Löschen** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="f5c42-169">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  
    
    > ##### <span data-ttu-id="f5c42-170">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="f5c42-170">Figure 10</span></span>  
    > <span data-ttu-id="f5c42-171">Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde</span><span class="sxs-lookup"><span data-stu-id="f5c42-171">How the object store looks after the key-value pair has been deleted</span></span>  
    > ![Wie der Objektspeicher aussieht, nachdem das Schlüssel-Wert-Paar gelöscht wurde][ImageIndexedDBKeyValuePairDeleted]  

### <span data-ttu-id="f5c42-173">Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher</span><span class="sxs-lookup"><span data-stu-id="f5c42-173">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="f5c42-174">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="f5c42-174">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="f5c42-175">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="f5c42-175">Figure 11</span></span>  
    > <span data-ttu-id="f5c42-176">Anzeigen eines Objektspeichers</span><span class="sxs-lookup"><span data-stu-id="f5c42-176">Viewing an object store</span></span>  
    > ![Anzeigen eines Objektspeichers][ImageIndexedDBObjectStore]  

1.  <span data-ttu-id="f5c42-178">Wählen Sie **Objektspeicher löschen** ![ , Objektspeicher löschen aus ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="f5c42-178">Select **Clear object store** ![Clear object store][ImageClearIcon].</span></span>  

### <span data-ttu-id="f5c42-179">Löschen einer IndexedDB-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5c42-179">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="f5c42-180">[Zeigen Sie die IndexedDB-Datenbank](#view-indexeddb-data) an, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f5c42-180">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="f5c42-181">Wählen Sie **Datenbank löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="f5c42-181">Select **Delete database**.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-182">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="f5c42-182">Figure 12</span></span>  
    > <span data-ttu-id="f5c42-183">Schaltfläche " **Datenbank löschen** "</span><span class="sxs-lookup"><span data-stu-id="f5c42-183">The **Delete database** button</span></span>  
    > ![Schaltfläche "Datenbank löschen"][ImageIndexedDBDatabase]  

### <span data-ttu-id="f5c42-185">Löschen des gesamten IndexedDB-Speichers</span><span class="sxs-lookup"><span data-stu-id="f5c42-185">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="f5c42-186">Öffnen Sie den Bereich **Speicher löschen** .</span><span class="sxs-lookup"><span data-stu-id="f5c42-186">Open the **Clear storage** pane.</span></span>  

1.  <span data-ttu-id="f5c42-187">Stellen Sie sicher, dass das Kontrollkästchen **IndexedDB** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5c42-187">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  

1.  <span data-ttu-id="f5c42-188">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="f5c42-188">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="f5c42-189">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="f5c42-189">Figure 13</span></span>  
    > <span data-ttu-id="f5c42-190">Der Bereich " **Speicher löschen** " ![ im Bereich "Speicher löschen"][ImageIndexedDBClearStorage]</span><span class="sxs-lookup"><span data-stu-id="f5c42-190">The **Clear storage** pane ![The Clear storage pane][ImageIndexedDBClearStorage]</span></span>  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Abbildung 2: das IndexedDB-Menü"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Abbildung 3: die notes_db-Datenbank"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Abbildung 4: der notes_os Objektspeicher"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Abbildung 5: Anzeigen eines IndexedDB-Werts"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Abbildung 6: Sortieren eines Objektspeichers anhand eines Indexes"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Abbildung 7: Anzeigen einer Datenbank"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Abbildung 8: Verwenden eines Ausschnitts für die Interaktion mit IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Abbildung 9: Auswählen eines Schlüssel-Wert-Paars, um es zu löschen"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Abbildung 10: Aussehen des Objektspeichers, nachdem das Schlüssel-Wert-Paar gelöscht wurde"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Abbildung 11: Anzeigen eines Objektspeichers"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Abbildung 12: die Schaltfläche "Datenbank löschen""  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Abbildung 13: der Bereich "Speicher löschen""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-devtools: Anzeigen von IFRAME-IndexedDB-Datenbanken – Chrom-Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Schlüssel Generator – grundlegende Konzepte | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Verwenden eines Index-using IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="f5c42-211">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5c42-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f5c42-212">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5c42-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f5c42-214">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f5c42-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
