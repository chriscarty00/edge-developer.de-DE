---
description: Anzeigen und Ändern von IndexedDB-Daten mit dem Anwendungsbereich und Codeausschnitten.
title: Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 719348067b1343ca3d7781737fa6441f92ad7ba1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439710"
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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a><span data-ttu-id="f43f1-104">Anzeigen und Ändern von IndexedDB-Daten mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f43f1-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f43f1-105">In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools zum Anzeigen][MicrosoftEdgeDevTools] und Ändern von [IndexedDB-Daten][MDNIndexedDBAPI] verwenden.</span><span class="sxs-lookup"><span data-stu-id="f43f1-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="f43f1-106">Es wird davon ausgegangen, dass Sie mit DevTools vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="f43f1-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="f43f1-107">Außerdem wird davon ausgegangen, dass Sie mit IndexedDB vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="f43f1-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="f43f1-108">Wenn nicht, navigieren Sie zu [Verwenden von IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="f43f1-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <a name="view-indexeddb-data"></a><span data-ttu-id="f43f1-109">Anzeigen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f43f1-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="f43f1-110">Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="f43f1-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="f43f1-111">Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f43f1-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="f43f1-113">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="f43f1-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43f1-114">Erweitern Sie **das Menü IndexedDB,** um zu überprüfen, welche Datenbanken verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f43f1-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Das Menü IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="f43f1-116">Das **Menü IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="f43f1-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="f43f1-117">\( ![ Database icon ](../media/database-icon.msft.png) \) represents a `notes - https://mdn.github.io` database, where is the name of the `notes` database and is the origin that `https://mdn.github.io` accesses the database.</span><span class="sxs-lookup"><span data-stu-id="f43f1-117">\(![Database icon](../media/database-icon.msft.png)\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="f43f1-118">\( ![ Objektspeichersymbol ](../media/object-store-icon.msft.png) \) `notes` ist ein Objektspeicher.</span><span class="sxs-lookup"><span data-stu-id="f43f1-118">\(![Object Store icon](../media/object-store-icon.msft.png)\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="f43f1-119">**title** und **body** sind [Indizes][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="f43f1-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f43f1-120">**Bekannte Einschränkung**  Drittanbieterdatenbanken sind nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f43f1-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="f43f1-121">Wenn Sie beispielsweise eine zum Einbetten einer Anzeige auf Ihrer Seite verwenden und Ihr Anzeigennetzwerk IndexedDB verwendet, sind die IndexedDB-Daten für Ihr Anzeigennetzwerk `<iframe>` nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f43f1-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="f43f1-122">Navigieren Sie zum [Problem #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="f43f1-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="f43f1-123">Wählen Sie eine Datenbank aus, um den Ursprung und die Versionsnummer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f43f1-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Die Notizendatenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="f43f1-125">Die **Notizendatenbank**</span><span class="sxs-lookup"><span data-stu-id="f43f1-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43f1-126">Wählen Sie einen Objektspeicher aus, um die Schlüssel-Wert-Paare zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f43f1-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f43f1-127">IndexedDB-Daten werden nicht in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f43f1-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="f43f1-128">Navigieren Sie zu [IndexedDB-Daten aktualisieren.](#refresh-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="f43f1-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Der Notes-Objektspeicher" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="f43f1-130">Der **Notes-Objektspeicher**</span><span class="sxs-lookup"><span data-stu-id="f43f1-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="f43f1-131">**Total entries** is the total number of key-value pairs in the object store.</span><span class="sxs-lookup"><span data-stu-id="f43f1-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="f43f1-132">**Der Schlüsselgeneratorwert** ist der nächste verfügbare Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f43f1-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="f43f1-133">Das Feld wird nur angezeigt, wenn [Schlüsselgeneratoren verwendet werden.][MDNBasicConceptsKeyGenerator]</span><span class="sxs-lookup"><span data-stu-id="f43f1-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="f43f1-134">Wählen Sie eine Zelle in der **Spalte Wert** aus, um den Wert zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="f43f1-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Anzeigen eines IndexedDB-Werts" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="f43f1-136">Anzeigen eines **IndexedDB-Werts**</span><span class="sxs-lookup"><span data-stu-id="f43f1-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43f1-137">Wählen Sie in  der  folgenden Abbildung einen Index aus, z. B. Titel oder Textkörper, um den Objektspeicher nach den Werten dieses Indexes zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="f43f1-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Sortieren eines Objektspeichers nach einem Index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="f43f1-139">Sortieren eines Objektspeichers nach einem Index</span><span class="sxs-lookup"><span data-stu-id="f43f1-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a><span data-ttu-id="f43f1-140">Aktualisieren von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f43f1-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="f43f1-141">IndexedDB-Werte im **Anwendungstool** werden nicht in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f43f1-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="f43f1-142">Wählen **Sie Aktualisieren** \( Aktualisieren ![ \) aus, wenn Sie einen Objektspeicher anzeigen, um die Daten zu aktualisieren, oder zeigen Sie eine Datenbank an, und wählen Sie Datenbank aktualisieren aus, um ](../media/reload-icon.msft.png) alle Daten zu aktualisieren. </span><span class="sxs-lookup"><span data-stu-id="f43f1-142">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Anzeigen einer Datenbank" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="f43f1-144">Anzeigen einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="f43f1-144">View a database</span></span>  
:::image-end:::  

## <a name="edit-indexeddb-data"></a><span data-ttu-id="f43f1-145">Bearbeiten von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f43f1-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="f43f1-146">IndexedDB-Schlüssel und -Werte können nicht über das **Anwendungstool bearbeitet** werden.</span><span class="sxs-lookup"><span data-stu-id="f43f1-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="f43f1-147">Da DevTools jedoch Zugriff auf den Seitenkontext hat, können Sie JavaScript-Code in DevTools ausführen, um IndexedDB-Daten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f43f1-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <a name="edit-indexeddb-data-with-snippets"></a><span data-ttu-id="f43f1-148">Bearbeiten von IndexedDB-Daten mit Codeausschnitten</span><span class="sxs-lookup"><span data-stu-id="f43f1-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="f43f1-149">[Codeausschnitte][DevtoolsJavascriptSnippets] sind eine Möglichkeit zum Speichern und Ausführen von Blöcken von JavaScript-Code in DevTools.</span><span class="sxs-lookup"><span data-stu-id="f43f1-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="f43f1-150">Wenn Sie einen Codeausschnitt ausführen, wird das Ergebnis bei der **Konsole protokolliert.**</span><span class="sxs-lookup"><span data-stu-id="f43f1-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="f43f1-151">Sie können einen Codeausschnitt zum Ausführen von JavaScript-Code verwenden, um eine IndexedDB-Datenbank zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f43f1-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Verwenden eines Codeausschnitts für die Interaktion mit IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="f43f1-153">Verwenden eines Codeausschnitts für die Interaktion mit IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f43f1-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <a name="delete-indexeddb-data"></a><span data-ttu-id="f43f1-154">Löschen von IndexedDB-Daten</span><span class="sxs-lookup"><span data-stu-id="f43f1-154">Delete IndexedDB data</span></span>  

### <a name="delete-an-indexeddb-key-value-pair"></a><span data-ttu-id="f43f1-155">Löschen eines IndexedDB-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="f43f1-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="f43f1-156">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f43f1-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="f43f1-157">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f43f1-157">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="f43f1-158">DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f43f1-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="f43f1-160">Wählen Sie ein Schlüssel-Wert-Paar aus, um es zu löschen</span><span class="sxs-lookup"><span data-stu-id="f43f1-160">Choose a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43f1-161">Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ](../media/delete-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="f43f1-161">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aussehen des Objektspeichers nach dem Löschen des Schlüssel-Wert-Paars" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="f43f1-163">Aussehen des Objektspeichers nach dem Löschen des Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="f43f1-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a><span data-ttu-id="f43f1-164">Löschen aller Schlüssel-Wert-Paare in einem Objektspeicher</span><span class="sxs-lookup"><span data-stu-id="f43f1-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="f43f1-165">[Anzeigen eines IndexedDB-Objektspeichers](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f43f1-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Anzeigen eines Objektspeichers" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="f43f1-167">Anzeigen eines Objektspeichers</span><span class="sxs-lookup"><span data-stu-id="f43f1-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43f1-168">Wählen **Sie Clear object store** \( Clear object store ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f43f1-168">Choose **Clear object store** \(![Clear object store](../media/clear-icon.msft.png)\).</span></span>  
    
### <a name="delete-an-indexeddb-database"></a><span data-ttu-id="f43f1-169">Löschen einer IndexedDB-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f43f1-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="f43f1-170">[Zeigen Sie die IndexedDB-Datenbank an,](#view-indexeddb-data) die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f43f1-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="f43f1-171">Wählen **Sie Datenbank löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="f43f1-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Die Schaltfläche Datenbank löschen" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="f43f1-173">Die **Schaltfläche Datenbank löschen**</span><span class="sxs-lookup"><span data-stu-id="f43f1-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a><span data-ttu-id="f43f1-174">Löschen des ganzen IndexedDB-Speichers</span><span class="sxs-lookup"><span data-stu-id="f43f1-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="f43f1-175">Öffnen Sie den **Speicherbereich** löschen.</span><span class="sxs-lookup"><span data-stu-id="f43f1-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="f43f1-176">Stellen Sie sicher, dass das **Kontrollkästchen IndexedDB** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f43f1-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="f43f1-177">Wählen **Sie Websitedaten löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="f43f1-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Der Speicherbereich löschen" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="f43f1-179">Der **Speicherbereich löschen**</span><span class="sxs-lookup"><span data-stu-id="f43f1-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f43f1-180">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f43f1-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: iframe IndexedDB-Datenbanken anzeigen - Chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Key Generator – Grundlegende Konzepte | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API-| MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexedDB-| MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Verwenden eines Indexes – Verwenden von IndexedDB-| MDN"  

> [!NOTE]
> <span data-ttu-id="f43f1-188">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f43f1-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f43f1-189">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="f43f1-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f43f1-191">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f43f1-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
