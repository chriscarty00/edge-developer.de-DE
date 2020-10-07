---
description: How to view and change IndexedDB data with the Application panel and Snippets.
title: View And Change IndexedDB Data With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 6b1209ddcbfac305535d9d61e001441dbf61b6ec
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993562"
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





# <span data-ttu-id="250a1-104">View and change IndexedDB data with Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="250a1-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="250a1-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span><span class="sxs-lookup"><span data-stu-id="250a1-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="250a1-106">It assumes you are familiar with DevTools.</span><span class="sxs-lookup"><span data-stu-id="250a1-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="250a1-107">It also assumes you are familiar with IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="250a1-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="250a1-108">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="250a1-108">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="250a1-109">View IndexedDB data</span><span class="sxs-lookup"><span data-stu-id="250a1-109">View IndexedDB data</span></span>   

1.  <span data-ttu-id="250a1-110">Select the **Application** tab to open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="250a1-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="250a1-111">The **Manifest** pane usually opens by default.</span><span class="sxs-lookup"><span data-stu-id="250a1-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="250a1-113">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="250a1-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="250a1-114">Expand the **IndexedDB** menu to see which databases are available.</span><span class="sxs-lookup"><span data-stu-id="250a1-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="250a1-116">The **IndexedDB** menu</span><span class="sxs-lookup"><span data-stu-id="250a1-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="250a1-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span><span class="sxs-lookup"><span data-stu-id="250a1-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="250a1-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span><span class="sxs-lookup"><span data-stu-id="250a1-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="250a1-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="250a1-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="250a1-120">**Known Limitation**  Third-party databases are not visible.</span><span class="sxs-lookup"><span data-stu-id="250a1-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="250a1-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span><span class="sxs-lookup"><span data-stu-id="250a1-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="250a1-122">See [issue #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="250a1-122">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="250a1-123">Select a database to see the origin and version number.</span><span class="sxs-lookup"><span data-stu-id="250a1-123">Select a database to see the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="250a1-125">The **notes** database</span><span class="sxs-lookup"><span data-stu-id="250a1-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="250a1-126">Select an object store to see the key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="250a1-126">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="250a1-127">IndexedDB data does not update in real-time.</span><span class="sxs-lookup"><span data-stu-id="250a1-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="250a1-128">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="250a1-128">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="250a1-130">The **notes** object store</span><span class="sxs-lookup"><span data-stu-id="250a1-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="250a1-131">**Total entries** is the total number of key-value pairs in the object store.</span><span class="sxs-lookup"><span data-stu-id="250a1-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="250a1-132">**Key generator value** is the next available key.</span><span class="sxs-lookup"><span data-stu-id="250a1-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="250a1-133">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="250a1-133">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="250a1-134">Select a cell in the **Value** column to expand that value.</span><span class="sxs-lookup"><span data-stu-id="250a1-134">Select a cell in the **Value** column to expand that value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="250a1-136">View an **IndexedDB** value</span><span class="sxs-lookup"><span data-stu-id="250a1-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="250a1-137">Select an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span><span class="sxs-lookup"><span data-stu-id="250a1-137">Select an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="250a1-139">Sort an object store by an index</span><span class="sxs-lookup"><span data-stu-id="250a1-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="250a1-140">Refresh IndexedDB data</span><span class="sxs-lookup"><span data-stu-id="250a1-140">Refresh IndexedDB data</span></span>   

<span data-ttu-id="250a1-141">IndexedDB values in the **Application** panel do not update in real-time.</span><span class="sxs-lookup"><span data-stu-id="250a1-141">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="250a1-142">Select **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span><span class="sxs-lookup"><span data-stu-id="250a1-142">Select **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="250a1-144">View a database</span><span class="sxs-lookup"><span data-stu-id="250a1-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="250a1-145">Edit IndexedDB data</span><span class="sxs-lookup"><span data-stu-id="250a1-145">Edit IndexedDB data</span></span>   

<span data-ttu-id="250a1-146">IndexedDB keys and values are not editable from the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="250a1-146">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="250a1-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span><span class="sxs-lookup"><span data-stu-id="250a1-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="250a1-148">Edit IndexedDB data with Snippets</span><span class="sxs-lookup"><span data-stu-id="250a1-148">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="250a1-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span><span class="sxs-lookup"><span data-stu-id="250a1-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="250a1-150">When you run a Snippet, the result is logged to the **Console**.</span><span class="sxs-lookup"><span data-stu-id="250a1-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="250a1-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span><span class="sxs-lookup"><span data-stu-id="250a1-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="250a1-153">Use a Snippet to interact with IndexedDB</span><span class="sxs-lookup"><span data-stu-id="250a1-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="250a1-154">Delete IndexedDB data</span><span class="sxs-lookup"><span data-stu-id="250a1-154">Delete IndexedDB data</span></span>   

### <span data-ttu-id="250a1-155">Delete an IndexedDB key-value pair</span><span class="sxs-lookup"><span data-stu-id="250a1-155">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="250a1-156">[View an IndexedDB object store](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="250a1-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="250a1-157">Select the key-value pair that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="250a1-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="250a1-158">DevTools highlights it to indicate that it is selected.</span><span class="sxs-lookup"><span data-stu-id="250a1-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="250a1-160">Select a key-value pair in order to delete it</span><span class="sxs-lookup"><span data-stu-id="250a1-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="250a1-161">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span><span class="sxs-lookup"><span data-stu-id="250a1-161">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="250a1-163">How the object store looks after the key-value pair has been deleted</span><span class="sxs-lookup"><span data-stu-id="250a1-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="250a1-164">Delete all key-value pairs in an object store</span><span class="sxs-lookup"><span data-stu-id="250a1-164">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="250a1-165">[View an IndexedDB object store](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="250a1-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="250a1-167">View an object store</span><span class="sxs-lookup"><span data-stu-id="250a1-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="250a1-168">Select **Clear object store** \(![Clear object store][ImageClearIcon]\).</span><span class="sxs-lookup"><span data-stu-id="250a1-168">Select **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="250a1-169">Delete an IndexedDB database</span><span class="sxs-lookup"><span data-stu-id="250a1-169">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="250a1-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="250a1-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="250a1-171">Select **Delete database**.</span><span class="sxs-lookup"><span data-stu-id="250a1-171">Select **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="250a1-173">The **Delete database** button</span><span class="sxs-lookup"><span data-stu-id="250a1-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="250a1-174">Delete all IndexedDB storage</span><span class="sxs-lookup"><span data-stu-id="250a1-174">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="250a1-175">Open the **Clear storage** pane.</span><span class="sxs-lookup"><span data-stu-id="250a1-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="250a1-176">Make sure that the **IndexedDB** checkbox is enabled.</span><span class="sxs-lookup"><span data-stu-id="250a1-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="250a1-177">Select **Clear site data**.</span><span class="sxs-lookup"><span data-stu-id="250a1-177">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="250a1-179">The **Clear storage** pane</span><span class="sxs-lookup"><span data-stu-id="250a1-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chromium) Developer tools | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Run snippets of JavaScript on any page with Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: Show iframe IndexedDB databases - chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Key Generator - Basic Concepts | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Using IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Using an index - Using IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="250a1-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="250a1-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="250a1-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="250a1-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="250a1-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="250a1-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
