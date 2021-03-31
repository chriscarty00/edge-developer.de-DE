---
description: Überprüfen Sie mithilfe des Speicherbereichs Ihren Webspeicher, IndexedDB, Cookies und Anforderungs-/Antwortcaches.
title: Speicher | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, web storage, local storage, session storage, indexeddb, cookies, service worker, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398896"
---
# <a name="storage"></a><span data-ttu-id="118e9-104">Speicher</span><span class="sxs-lookup"><span data-stu-id="118e9-104">Storage</span></span>

<span data-ttu-id="118e9-105">Verwenden Sie **den Speicherbereich,** um verschiedene lokal zwischengespeicherte Daten zu überprüfen und zu verwalten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="118e9-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>  

*   <span data-ttu-id="118e9-106">[Webspeicher](#local-and-session-storage-managers) \(Lokaler und Sitzungsspeicher\) Schlüssel-/Wertepaare</span><span class="sxs-lookup"><span data-stu-id="118e9-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span></span>  
*   <span data-ttu-id="118e9-107">[Indizierte strukturierte DB-Daten](#indexeddb-manager)</span><span class="sxs-lookup"><span data-stu-id="118e9-107">[Indexed DB](#indexeddb-manager) structured data</span></span>  
*   <span data-ttu-id="118e9-108">[Cookies](#cookies-list) für die Domäne</span><span class="sxs-lookup"><span data-stu-id="118e9-108">[Cookies](#cookies-list) for the domain</span></span>  
*   <span data-ttu-id="118e9-109">[Cache](#cache-manager) \(Anforderungs-/Antwortpaare\) für das Debuggen von Dienstmitarbeitern</span><span class="sxs-lookup"><span data-stu-id="118e9-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span></span>  

<span data-ttu-id="118e9-110">Erweitern Sie eine dieser Kategorien, und klicken Sie auf einen untergeordneten Eintrag, um die Registerkarte Ressourcen-Manager zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="118e9-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>  

## <a name="local-and-session-storage-managers"></a><span data-ttu-id="118e9-111">Lokale und Sitzungsspeichermanager</span><span class="sxs-lookup"><span data-stu-id="118e9-111">Local and Session storage managers</span></span>  

<span data-ttu-id="118e9-112">Verwenden Sie den lokalen Speicher-Manager und den Sitzungsspeicher-Manager, um den Webspeicher für Ihre Seite zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="118e9-112">Use the Local Storage manager and Session Storage manager to inspect and manage the web storage for your page.</span></span>  

<span data-ttu-id="118e9-113">In den  **Ordnern** Lokaler Speicher und Sitzungsspeicher in der Ressourcenauswahl des Speicherbereichs wird eine Liste der Ursprünge für die Seite angezeigt. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="118e9-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [Resource picker](./debugger.md#resource-picker) display a list of origins for the page.</span></span>  <span data-ttu-id="118e9-114">Wenn Sie einen dieser Frames auswählen, wird eine bearbeitbare Tabelle der aktuellen Schlüssel-Wert-Paare geöffnet, die über [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) oder [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)festgelegt wurden, bzw. \(bzw. direkt aus der DevTools [Storage-Liste](#storage-list)\).</span><span class="sxs-lookup"><span data-stu-id="118e9-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively \(and/or set directly from the  DevTools [Storage list](#storage-list)\).</span></span>  

![DevTools Storage Manager](./media/storage_web_storage.png)  

<span data-ttu-id="118e9-116">Auf den Registerkarten Lokaler Speicher und Sitzungsspeicher können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-116">From the Local Storage and Session Storage tabs you can:</span></span>  

*   <span data-ttu-id="118e9-117">**Aktualisieren** Sie `Ctrl+F5` \( \) die [Speicherliste,](#cookies-list) um die aktuellen Schlüssel-Werte-Paare für die angegebene Domäne zu sehen.</span><span class="sxs-lookup"><span data-stu-id="118e9-117">**Refresh** \(`Ctrl+F5`\) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span>  <span data-ttu-id="118e9-118">\(Die Liste wird bei Skriptupdates nicht automatisch aktualisiert.\)</span><span class="sxs-lookup"><span data-stu-id="118e9-118">\(The list does not auto-refresh upon script updates.\)</span></span>  
*   <span data-ttu-id="118e9-119">**Simulieren Sie das Erreichen des Speichergrenzwerts**  für Microsoft Edge-Webspeicher.</span><span class="sxs-lookup"><span data-stu-id="118e9-119">**Simulate reaching the storage limit**  for Microsoft Edge web storage.</span></span>  <span data-ttu-id="118e9-120">Jede Domäne und Unterdomäne verfügt über einen eigenen Speicherbereich, es gibt jedoch einen kombinierten Grenzwert:</span><span class="sxs-lookup"><span data-stu-id="118e9-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>  
    *   <span data-ttu-id="118e9-121">**Unterdomänen**: bis zu 5 MBs Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="118e9-121">**Subdomains**:  up to 5 MBs of space</span></span>  
    *   <span data-ttu-id="118e9-122">**Domänen:** bis zu 10 MBs Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="118e9-122">**Domains**:  up to 10 MBs of space</span></span>  
    *   <span data-ttu-id="118e9-123">**Gesamt für alle Domänen:** bis zu 50 MBs Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="118e9-123">**Total for all domains**:  up to 50 MBs of space</span></span>  

   <span data-ttu-id="118e9-124">Der Sitzungsspeicher wird gelöscht, sobald die letzte Browserregisterkarte, die auf den Ursprung des Browsers verweisen, geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="118e9-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span>  <span data-ttu-id="118e9-125">Lokale Speichereinträge bleiben auf unbestimmte Zeit bestehen, bis sie programmgesteuert von der Seite oder manuell vom Benutzer gelöscht werden:</span><span class="sxs-lookup"><span data-stu-id="118e9-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>  

   <span data-ttu-id="118e9-126">**Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Websitedaten**</span><span class="sxs-lookup"><span data-stu-id="118e9-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

![Löschen von Browserdaten aus dem Bereich "Microsoft Edge-Einstellungen"](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a><span data-ttu-id="118e9-128">Speicherliste</span><span class="sxs-lookup"><span data-stu-id="118e9-128">Storage list</span></span>  

<span data-ttu-id="118e9-129">In der Tabelle Speicherliste können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-129">From the Storage list table you can:</span></span>  

*   <span data-ttu-id="118e9-130">**Überprüfen und sortieren Sie Ihre** Paare, indem Sie in der Tabelle auf einen der `key/value` Spaltennamen klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-130">**Inspect and sort** your `key/value` pairs by clicking on either column name in the table.</span></span>  
*   <span data-ttu-id="118e9-131">**Bearbeiten** Sie `Key` das und eines `Value` vorhandenen Eintrags, indem Sie in die Zelle klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-131">**Edit** the `Key` and `Value` of an existing entry by clicking in the cell.</span></span>  
*   <span data-ttu-id="118e9-132">**Löschen** Sie `Del` \( \) einen Eintrag aus der Kontextmenüoption mit der rechten Maustaste, **Element löschen**.</span><span class="sxs-lookup"><span data-stu-id="118e9-132">**Delete** \(`Del`\) an entry from the right-click context menu option, **Delete item**.</span></span>  
*   <span data-ttu-id="118e9-133">**Fügen** Sie ein neues Paar hinzu, indem Sie auf die leere Zeile am `key/value` unteren Rand der Tabelle klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-133">**Add** a new `key/value` pair by clicking on the empty row at the bottom of the table.</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="118e9-134">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="118e9-134">Shortcuts</span></span>

| <span data-ttu-id="118e9-135">Aktion</span><span class="sxs-lookup"><span data-stu-id="118e9-135">Action</span></span> | <span data-ttu-id="118e9-136">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="118e9-136">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="118e9-137">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="118e9-137">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="118e9-138">Element löschen</span><span class="sxs-lookup"><span data-stu-id="118e9-138">Delete item</span></span> | `Del` |  
| <span data-ttu-id="118e9-139">Kopieren ausgewählter Elemente</span><span class="sxs-lookup"><span data-stu-id="118e9-139">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="118e9-140">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="118e9-140">Select all</span></span> | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a><span data-ttu-id="118e9-141">IndexedDB Manager</span><span class="sxs-lookup"><span data-stu-id="118e9-141">IndexedDB manager</span></span>  

<span data-ttu-id="118e9-142">Verwenden Sie **die Registerkarte IndexedDB,** um die lokal auf einem Clientcomputer gespeicherten strukturierten Daten zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="118e9-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span>  <span data-ttu-id="118e9-143">Insbesondere können Sie Ihre Objektspeicher und -indizes überprüfen/sortieren und aktualisieren sowie einzelne Schlüsselwerteinträge löschen.</span><span class="sxs-lookup"><span data-stu-id="118e9-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>  

> [!TIP]
> <span data-ttu-id="118e9-144">Sie können unsere [Audiomixerdemo](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) verwenden, um den *IndexedDB-Manager* in Microsoft Edge DevTools zu testen.</span><span class="sxs-lookup"><span data-stu-id="118e9-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="118e9-145">Verwenden Sie das Menü Microsoft **Edge-Einstellungen,** um alle indexedDB-Daten zu löschen, die für den aktuellen Benutzer in Microsoft Edge gespeichert sind:</span><span class="sxs-lookup"><span data-stu-id="118e9-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge **Settings** menu:</span></span>  

<span data-ttu-id="118e9-146">**...** >  **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Websitedaten**</span><span class="sxs-lookup"><span data-stu-id="118e9-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

<span data-ttu-id="118e9-147">Der Ordner in der Ressourcenauswahl des Debuggers zeigt eine Liste der Ursprünge der von der `IndexedDB` Seite geladenen Ressourcen an. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="118e9-147">The `IndexedDB` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="118e9-148">Alle IndexedDB \(IDB\)-Datenbanken werden zusammen mit ihren Objektspeichern unter dem Ursprung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="118e9-148">Any IndexedDB \(IDB\) databases will be listed under the origin, along with their object stores.</span></span>  

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a><span data-ttu-id="118e9-150">IndexedDB Toolbar</span><span class="sxs-lookup"><span data-stu-id="118e9-150">IndexedDB Toolbar</span></span>  

<span data-ttu-id="118e9-151">Über die IndexedDB-Symbolleiste können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-151">From the IndexedDB toolbar you can:</span></span>  

*   <span data-ttu-id="118e9-152">**Aktualisieren** Sie \( \), um die aktuellen Einträge im Objektspeicher oder `Ctrl` + `F5` -index Ihrer Datenbank zu sehen.</span><span class="sxs-lookup"><span data-stu-id="118e9-152">**Refresh** \(`Ctrl`+`F5`\) to see the current entries in the object store or index of your database.</span></span>  <span data-ttu-id="118e9-153">Der IndexedDB-Manager aktualisiert die Datenbank nicht automatisch, wenn Änderungen an der Datenbank vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="118e9-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>  

### <a name="object-store-entries-list"></a><span data-ttu-id="118e9-154">Liste der Objektspeichereinträge</span><span class="sxs-lookup"><span data-stu-id="118e9-154">Object store entries list</span></span>  

<span data-ttu-id="118e9-155">Im Objektspeicher oder in der Indextabelle können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-155">From the Object store or Index table you can:</span></span>  

*   <span data-ttu-id="118e9-156">**Überprüfen und sortieren Sie** Ihre Schlüssel-Wert-Paare, indem Sie auf einen beliebigen Spaltennamen in der Tabelle klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="118e9-157">**Refresh** \( `Ctrl` + `F5` \)</span><span class="sxs-lookup"><span data-stu-id="118e9-157">**Refresh** \(`Ctrl`+`F5`\)</span></span>  
*   <span data-ttu-id="118e9-158">**Löschen Sie das** Element \( `Del` \), um den ausgewählten Eintrag im Objektspeicher oder -index zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="118e9-158">**Delete item** \(`Del`\) to remove the selected entry in your object store or index.</span></span>  <span data-ttu-id="118e9-159">Sie können dies auch über [](#context-menu) die Kontextmenüoption Löschen mit der rechten Maustaste **tun.**</span><span class="sxs-lookup"><span data-stu-id="118e9-159">You can also do this from the right-click [context menu](#context-menu) option, **Delete item**.</span></span>  
*   <span data-ttu-id="118e9-160">**Kopieren Sie ausgewählte Elemente** \( `Ctrl` + `C` \), um das ausgewählte Element in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="118e9-160">**Copy selected items** \(`Ctrl`+`C`\) to copy the selected item to your clipboard.</span></span>  <span data-ttu-id="118e9-161">Sie können dies auch über [](#context-menu) die Kontextmenüoption "Ausgewähltes **Element kopieren" mit der rechten**Maustaste tun.</span><span class="sxs-lookup"><span data-stu-id="118e9-161">You can also do this from the right-click [context menu](#context-menu) option, **Copy selected item**.</span></span>  
*   <span data-ttu-id="118e9-162">**Wählen Sie** alle \( `Ctrl` + `A` \) aus, um alle Einträge im Objektspeicher oder -index auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="118e9-162">**Select all** \(`Ctrl`+`A`\) to select all the entries in your object store or index.</span></span>  <span data-ttu-id="118e9-163">Sie können dies auch über [](#context-menu) die Kontextmenüoption **"Alle auswählen" mit**der rechten Maustaste tun.</span><span class="sxs-lookup"><span data-stu-id="118e9-163">You can also do this from the right-click [context menu](#context-menu) option, **Select all**.</span></span>  

<span data-ttu-id="118e9-164">Die Spalten des Objektspeichers oder der Indextabelle sind sortierbar:</span><span class="sxs-lookup"><span data-stu-id="118e9-164">The columns of the Object store or Index table are sortable:</span></span>  

| <span data-ttu-id="118e9-165">Spalte</span><span class="sxs-lookup"><span data-stu-id="118e9-165">Column</span></span> | <span data-ttu-id="118e9-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="118e9-166">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="118e9-167">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="118e9-167">Key</span></span> | <span data-ttu-id="118e9-168">Name des Schlüssel-Wert-Paars \(identisch mit **Primärschlüssel**\) beim Iterieren über einen Objektspeicher; Name des Indexschlüssels \(aktueller Schlüssel des Cursors\) beim Iterieren eines Indexes</span><span class="sxs-lookup"><span data-stu-id="118e9-168">Name of the key-value pair \(same as **Primary Key**\) when iterating over an object store; Name of the index key \(cursor's current key\) when iterating over an index</span></span> |  
| <span data-ttu-id="118e9-169">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="118e9-169">Primary Key</span></span> | <span data-ttu-id="118e9-170">Name des Schlüssel-Wert-Paars \(Weitere Informationen zu IDB-Schlüsseln finden Sie unter **MDN-Web-Dokumente** \) [](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)</span><span class="sxs-lookup"><span data-stu-id="118e9-170">Name of the key-value pair \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span></span> |  
| <span data-ttu-id="118e9-171">Wert</span><span class="sxs-lookup"><span data-stu-id="118e9-171">Value</span></span> | <span data-ttu-id="118e9-172">Wert des Schlüssel-Wert-Paares</span><span class="sxs-lookup"><span data-stu-id="118e9-172">Value of the key-value pair</span></span> |  

<span data-ttu-id="118e9-173">Weitere Informationen zu [IndexedDB-Konzepten](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)und -Verwendung finden Sie in DEN MDN-Web-Dokumenten. </span><span class="sxs-lookup"><span data-stu-id="118e9-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>  

### <a name="context-menu"></a><span data-ttu-id="118e9-174">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="118e9-174">Context menu</span></span>  

<span data-ttu-id="118e9-175">Zusätzlich zur [ *IndexedDB-Symbolleiste* ](#indexeddb-toolbar)können Sie Ihre Daten auch in Objektspeichern  oder Indizes über das Kontextmenü und/oder die Tastenkombinationen [verwalten.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="118e9-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="118e9-176">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="118e9-176">Shortcuts</span></span>

| <span data-ttu-id="118e9-177">Aktion</span><span class="sxs-lookup"><span data-stu-id="118e9-177">Action</span></span> | <span data-ttu-id="118e9-178">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="118e9-178">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="118e9-179">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="118e9-179">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="118e9-180">Schlüssel-Wert-Paar löschen</span><span class="sxs-lookup"><span data-stu-id="118e9-180">Delete key-value pair</span></span> | `Del` |  
| <span data-ttu-id="118e9-181">Kopieren ausgewählter Elemente</span><span class="sxs-lookup"><span data-stu-id="118e9-181">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="118e9-182">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="118e9-182">Select all</span></span> | `Ctrl +`<span data-ttu-id="118e9-183">A'</span><span class="sxs-lookup"><span data-stu-id="118e9-183">A\`</span></span> |  

## <a name="cookies-manager"></a><span data-ttu-id="118e9-184">Cookies-Manager</span><span class="sxs-lookup"><span data-stu-id="118e9-184">Cookies manager</span></span>  

<span data-ttu-id="118e9-185">Verwenden Sie den Cookies-Manager, um die Cookies für die angegebene Domäne zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="118e9-185">Use the Cookies manager to inspect and manage the cookies for the given domain.</span></span>  

<span data-ttu-id="118e9-186">Der Ordner in der Ressourcenauswahl des Debuggers zeigt eine Liste der Ursprünge der von der `Cookies` Seite geladenen Ressourcen an. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="118e9-186">The `Cookies` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="118e9-187">Wenn Sie einen dieser Frames auswählen, wird eine Tabelle geöffnet, die die aktuellen Cookies darstellt, die entweder vom [HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Cookies) oder über ein Skript mit [Document.cookie festgelegt werden.](https://developer.mozilla.org/docs/Web/API/Document/cookie)</span><span class="sxs-lookup"><span data-stu-id="118e9-187">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>  

![DevTools Cookies Manager](./media/storage_cookies.png)  

<span data-ttu-id="118e9-189">Auf der Registerkartensymbolleiste Cookies können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-189">From the Cookies tab toolbar you can:</span></span>  

*   <span data-ttu-id="118e9-190">**Aktualisieren** Sie `Ctrl` + `F5` \( \) die [Liste Cookies,](#cookies-list) um den aktuellen Satz von Cookies für die angegebene Domäne zu sehen.</span><span class="sxs-lookup"><span data-stu-id="118e9-190">**Refresh** \(`Ctrl`+`F5`\) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span>  <span data-ttu-id="118e9-191">\(Die Liste wird nicht automatisch aktualisiert.\)</span><span class="sxs-lookup"><span data-stu-id="118e9-191">\(The list does not auto-refresh.\)</span></span>  
*   <span data-ttu-id="118e9-192">**Löschen Sie alle** Cookies \( `Ctrl` + `Shift` + `Del` \) \(session and permanent\) für den Pfad der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="118e9-192">**Delete all cookies** \(`Ctrl`+`Shift`+`Del`\) \(session and permanent\) for the path of the current page.</span></span>  
*   <span data-ttu-id="118e9-193">**Löschen Sie alle Sitzungscookies** \( `Ctrl` + `Del` \) für den Pfad der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="118e9-193">**Delete all session cookies** \(`Ctrl`+`Del`\) for the path of the current page.</span></span>  

<span data-ttu-id="118e9-194">Um Ihre Cookiesliste vollständig zu löschen, müssen Sie möglicherweise alle Cookies für **die** Domäne über die Symbolleiste [des](./network.md#toolbar) Netzwerkpanels löschen.</span><span class="sxs-lookup"><span data-stu-id="118e9-194">To completely clear your Cookies list, you might need to **Clear all cookies for the domain** from the [Network](./network.md#toolbar) panel toolbar.</span></span>  

### <a name="cookies-list"></a><span data-ttu-id="118e9-195">Liste der Cookies</span><span class="sxs-lookup"><span data-stu-id="118e9-195">Cookies list</span></span>  

<span data-ttu-id="118e9-196">In der Listentabelle Cookies können Sie:</span><span class="sxs-lookup"><span data-stu-id="118e9-196">From the Cookies list table you can:</span></span>  

*   <span data-ttu-id="118e9-197">**Überprüfen und sortieren Sie** Ihre Cookies, indem Sie auf einen beliebigen Spaltennamen in der Tabelle klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-197">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="118e9-198">**Bearbeiten** Sie `Name` das und eines `Value` vorhandenen Cookies, indem Sie in die Zelle klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-198">**Edit** the `Name` and `Value` of an existing cookie by clicking in the cell.</span></span>  
*   <span data-ttu-id="118e9-199">**Löschen** Sie `Del` \( \) ein Cookie aus der Kontextmenüoption mit [der](#context-menu) rechten Maustaste, `Delete cookie` .</span><span class="sxs-lookup"><span data-stu-id="118e9-199">**Delete** \(`Del`\) a cookie from the right-click [context menu](#context-menu) option, `Delete cookie`.</span></span>  
*   <span data-ttu-id="118e9-200">**Fügen** Sie ein neues Sitzungscookie für die angegebene hinzu, indem Sie unten in der Tabelle auf die leere `Domain/Path` Zeile klicken.</span><span class="sxs-lookup"><span data-stu-id="118e9-200">**Add** a new session cookie for the given `Domain/Path` by clicking on the empty row at the bottom of the table.</span></span>  <span data-ttu-id="118e9-201">Dies funktioniert nur für Sitzungscookies. Dauerhafte Cookies \(mit bestimmten Ablaufdatum\) müssen mit herkömmlichen Methoden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="118e9-201">This only works for session cookies; permanent cookies \(with specific expiry dates\) must be set with traditional methods.</span></span>  <span data-ttu-id="118e9-202">Die Werte und werden automatisch entsprechend der Position `Domain` `Path` der Seite gefüllt.</span><span class="sxs-lookup"><span data-stu-id="118e9-202">The `Domain` and `Path` values are auto-filled according to the location of the page.</span></span>  

<span data-ttu-id="118e9-203">Die Spalten der Liste Cookies können sortiert werden:</span><span class="sxs-lookup"><span data-stu-id="118e9-203">The columns of the Cookies list are sortable:</span></span>

| <span data-ttu-id="118e9-204">Spalte</span><span class="sxs-lookup"><span data-stu-id="118e9-204">Column</span></span> | <span data-ttu-id="118e9-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="118e9-205">Description</span></span> |  
| :--- | :--- |  
| <span data-ttu-id="118e9-206">Name</span><span class="sxs-lookup"><span data-stu-id="118e9-206">Name</span></span> | <span data-ttu-id="118e9-207">Name des Cookies</span><span class="sxs-lookup"><span data-stu-id="118e9-207">Name of the cookie</span></span> |  
| <span data-ttu-id="118e9-208">Wert</span><span class="sxs-lookup"><span data-stu-id="118e9-208">Value</span></span> | <span data-ttu-id="118e9-209">Wert des Cookies</span><span class="sxs-lookup"><span data-stu-id="118e9-209">Value of the cookie</span></span> |  
| <span data-ttu-id="118e9-210">Domäne</span><span class="sxs-lookup"><span data-stu-id="118e9-210">Domain</span></span> | <span data-ttu-id="118e9-211">Hostname des Cookies \(kann leer sein\)</span><span class="sxs-lookup"><span data-stu-id="118e9-211">Host name of the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="118e9-212">Pfad</span><span class="sxs-lookup"><span data-stu-id="118e9-212">Path</span></span> | <span data-ttu-id="118e9-213">URL-Pfad für das Cookie \(kann leer sein\)</span><span class="sxs-lookup"><span data-stu-id="118e9-213">URL path for the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="118e9-214">Läuft ab</span><span class="sxs-lookup"><span data-stu-id="118e9-214">Expires</span></span> | <span data-ttu-id="118e9-215">Maximale Lebensdauer des Cookies als HTTP-Datumsstempel.</span><span class="sxs-lookup"><span data-stu-id="118e9-215">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span>  <span data-ttu-id="118e9-216">Wenn nein `Expires` oder `Max-Age` festgelegt wurde, wird der Eintrag als Sitzungscookie betrachtet.</span><span class="sxs-lookup"><span data-stu-id="118e9-216">If no `Expires` or `Max-Age` was set, the entry is considered a Session cookie.</span></span>  |  
| <span data-ttu-id="118e9-217">Nur HTTP</span><span class="sxs-lookup"><span data-stu-id="118e9-217">HTTP only</span></span> | <span data-ttu-id="118e9-218">Gibt an, ob das Cookie mit Direktive festgelegt wurde, was angibt, dass von JavaScript nicht auf das Cookie `HttpOnly` zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="118e9-218">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span> |  
| <span data-ttu-id="118e9-219">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="118e9-219">Secure</span></span> | <span data-ttu-id="118e9-220">Gibt an, ob das Cookie mit der Direktive festgelegt wurde, und gibt an, dass es nur über eine Anforderung mit SSL und dem HTTPS-Protokoll an den `Secure` Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="118e9-220">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>  |  

<span data-ttu-id="118e9-221">Weitere Informationen zu Cookieeigenschaften finden Sie in der [Set-Cookie-Referenz](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) für MDN-Webdoks. </span><span class="sxs-lookup"><span data-stu-id="118e9-221">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>  

### <a name="context-menu"></a><span data-ttu-id="118e9-222">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="118e9-222">Context menu</span></span>  

<span data-ttu-id="118e9-223">Zusätzlich zur Registerkartensymbolleiste Cookies [können](#cookies-manager)Sie Ihre Cookies  auch über das Kontextmenü und/oder die Tastenkombinationen [verwalten.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="118e9-223">In addition to the Cookies tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="118e9-224">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="118e9-224">Shortcuts</span></span>  

| <span data-ttu-id="118e9-225">Aktion</span><span class="sxs-lookup"><span data-stu-id="118e9-225">Action</span></span> | <span data-ttu-id="118e9-226">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="118e9-226">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="118e9-227">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="118e9-227">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="118e9-228">Löschen des Cookies</span><span class="sxs-lookup"><span data-stu-id="118e9-228">Delete cookie</span></span> | `Del` |  
| <span data-ttu-id="118e9-229">Löschen aller Cookies</span><span class="sxs-lookup"><span data-stu-id="118e9-229">Delete all cookies</span></span> | `Ctrl`+`Shift`+`Del` |  
| <span data-ttu-id="118e9-230">Löschen aller Sitzungscookies</span><span class="sxs-lookup"><span data-stu-id="118e9-230">Delete all session cookies</span></span> | `Ctrl`+`Del` |  
| <span data-ttu-id="118e9-231">Kopieren ausgewählter Elemente</span><span class="sxs-lookup"><span data-stu-id="118e9-231">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="118e9-232">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="118e9-232">Select all</span></span> | `Ctrl`+`A` |  

### <a name="cache-manager"></a><span data-ttu-id="118e9-233">Cache-Manager</span><span class="sxs-lookup"><span data-stu-id="118e9-233">Cache manager</span></span>  

<span data-ttu-id="118e9-234">Wenn Sie auf einen bestimmten Cacheeintrag  klicken, wird der Cache-Manager des Dienstmitarbeiters geöffnet, in dem Sie Cacheeinträge \( und `Request` Schlüssel-/Wertpaare\ überprüfen und optional `Response` löschen können):</span><span class="sxs-lookup"><span data-stu-id="118e9-234">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries \(`Request` and `Response` key/value pairs\):</span></span>  

![Cache-Manager](./media/storage_cache.png)  

### <a name="shortcuts"></a><span data-ttu-id="118e9-236">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="118e9-236">Shortcuts</span></span>  

#### <a name="cache-manager"></a><span data-ttu-id="118e9-237">Cache-Manager</span><span class="sxs-lookup"><span data-stu-id="118e9-237">Cache manager</span></span>  

| <span data-ttu-id="118e9-238">Aktion</span><span class="sxs-lookup"><span data-stu-id="118e9-238">Action</span></span> | <span data-ttu-id="118e9-239">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="118e9-239">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="118e9-240">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="118e9-240">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="118e9-241">Element löschen</span><span class="sxs-lookup"><span data-stu-id="118e9-241">Delete item</span></span> | `Del` |  
| <span data-ttu-id="118e9-242">Kopieren ausgewählter Elemente</span><span class="sxs-lookup"><span data-stu-id="118e9-242">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="118e9-243">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="118e9-243">Select all</span></span> | `Ctrl`+`A` |  
