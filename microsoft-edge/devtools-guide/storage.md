---
description: Überprüfen Ihres Webspeichers, IndexedDB, Cookies und Anforderungs-/Antwort-Caches mithilfe des Speicher Panels
title: DevTools-Speicher
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Web Storage, lokaler Speicher, Sitzungsspeicher, indexeddb, Cookies, Service Worker, Cache
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567588"
---
# <span data-ttu-id="a180a-104">Speicher</span><span class="sxs-lookup"><span data-stu-id="a180a-104">Storage</span></span>

<span data-ttu-id="a180a-105">Verwenden Sie den **Speicher** Panel, um verschiedene lokal zwischengespeicherte Daten zu überprüfen und zu verwalten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="a180a-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="a180a-106">Schlüssel-Wert-Paare für [Webspeicher](#local-and-session-storage-managers) (*lokaler* und *Sitzungs* Speicher)</span><span class="sxs-lookup"><span data-stu-id="a180a-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="a180a-107">[Indizierte DB](#indexeddb-manager) -strukturierte Daten</span><span class="sxs-lookup"><span data-stu-id="a180a-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="a180a-108">[Cookies](#cookies-list) für die Domäne</span><span class="sxs-lookup"><span data-stu-id="a180a-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="a180a-109">[Cache](#cache-manager) (Anforderung/Antwort-Paare) für das Debuggen von Service Worker</span><span class="sxs-lookup"><span data-stu-id="a180a-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="a180a-110">Erweitern Sie eine dieser Kategorien, und klicken Sie auf einen untergeordneten Eintrag, um die Registerkarte Ressourcen-Manager zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a180a-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="a180a-111">Lokale und Sitzungsspeicher-Manager</span><span class="sxs-lookup"><span data-stu-id="a180a-111">Local and Session storage managers</span></span>

<span data-ttu-id="a180a-112">Verwenden Sie den *lokalen Speicher-Manager* und den *Sitzungsspeicher-Manager* , um den Webspeicher für Ihre Seite zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a180a-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="a180a-113">In den **lokalen Speicher** -und **Sitzungsspeicher** Ordnern in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Speicher Panels wird eine Liste der Ursprünge für die Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a180a-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="a180a-114">Wenn Sie einen dieser Frames auswählen, wird eine bearbeitbare Tabelle mit den aktuellen Schlüssel-Wert-Paaren geöffnet, die über [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) oder [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)(und/oder direkt aus der devtools- [Speicherliste](#storage-list)) gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a180a-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![DevTools-Cookies-Manager](./media/storage_web_storage.png)

<span data-ttu-id="a180a-116">Auf den Registerkarten *lokaler Speicher* und *Sitzungsspeicher* können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a180a-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="a180a-117">**Aktualisieren** ( `Ctrl+F5` ) die [Speicherliste](#cookies-list) , um die aktuelle Gruppe von Schlüssel-Wert-Paaren für die angegebene Domäne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a180a-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="a180a-118">(Die Liste wird bei Skript Aktualisierungen nicht automatisch aktualisiert.)</span><span class="sxs-lookup"><span data-stu-id="a180a-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="a180a-119">**Simulieren Sie das Erreichen der Speichergrenze** für Microsoft Edge Web Storage.</span><span class="sxs-lookup"><span data-stu-id="a180a-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="a180a-120">Jede Domäne und Unterdomäne verfügt über einen eigenen Speicherbereich, es gibt jedoch eine kombinierte Grenze:</span><span class="sxs-lookup"><span data-stu-id="a180a-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="a180a-121">Unter **Domänen:** bis zu 5 MBS Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="a180a-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="a180a-122">**Domänen:** bis zu 10 MBS Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="a180a-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="a180a-123">**Gesamtzahl für alle Domänen:** bis zu 50 MBS Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="a180a-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="a180a-124">Der Sitzungsspeicher wird gelöscht, sobald der letzte Browser Reiter, der auf seinen Ursprung verweist, geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a180a-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="a180a-125">Lokale Speichereinträge bleiben unbegrenzt bestehen, bis Sie programmgesteuert von der Seite oder manuell vom Benutzer gelöscht werden:</span><span class="sxs-lookup"><span data-stu-id="a180a-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="a180a-126">**Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Website Daten**</span><span class="sxs-lookup"><span data-stu-id="a180a-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Löschen von Daten aus dem Microsoft Edge Settings-Panel](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="a180a-128">Speicherliste</span><span class="sxs-lookup"><span data-stu-id="a180a-128">Storage list</span></span>

<span data-ttu-id="a180a-129">In der Tabelle " *Speicherliste* " können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a180a-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="a180a-130">Überprüfen Sie Ihre Schlüssel-Wert-Paare **, und Sortieren** Sie Sie, indem Sie in der Tabelle auf einen der Spaltennamen klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="a180a-131">**Bearbeiten** Sie den *Schlüssel* und *Wert* eines vorhandenen Eintrags, indem Sie in die Zelle klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="a180a-132">**Löschen** `Del` Sie einen Eintrag aus der Kontextmenüoption, und löschen Sie das *Element*.</span><span class="sxs-lookup"><span data-stu-id="a180a-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="a180a-133">**Fügen Sie** ein neues Schlüssel-Wert-Paar hinzu, indem Sie auf die leere Zeile am Ende der Tabelle klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="a180a-134">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="a180a-134">Shortcuts</span></span>

| <span data-ttu-id="a180a-135">Aktion</span><span class="sxs-lookup"><span data-stu-id="a180a-135">Action</span></span>              | <span data-ttu-id="a180a-136">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a180a-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="a180a-137">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a180a-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="a180a-138">Element löschen</span><span class="sxs-lookup"><span data-stu-id="a180a-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="a180a-139">Kopieren der markierten Elemente</span><span class="sxs-lookup"><span data-stu-id="a180a-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="a180a-140">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="a180a-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="a180a-141">IndexedDB-Manager</span><span class="sxs-lookup"><span data-stu-id="a180a-141">IndexedDB manager</span></span>

<span data-ttu-id="a180a-142">Verwenden Sie die Registerkarte **IndexedDB** , um die strukturierten Daten, die lokal auf einem Clientcomputer gespeichert sind, zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a180a-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="a180a-143">Insbesondere können Sie Ihre Objektspeicher und Indizes prüfen/sortieren und aktualisieren sowie einzelne Schlüssel-Wert-Einträge löschen.</span><span class="sxs-lookup"><span data-stu-id="a180a-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="a180a-144">Sie können unsere [Audiomixer-](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) Demo verwenden, um den *IndexedDB-Manager* in Microsoft Edge devtools zu testen.</span><span class="sxs-lookup"><span data-stu-id="a180a-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="a180a-145">Wenn Sie alle IndexedDB-Daten löschen möchten, die für den aktuellen Benutzer in Microsoft Edge gespeichert sind, verwenden Sie das Menü Microsoft Edge *Settings (Einstellungen* ):</span><span class="sxs-lookup"><span data-stu-id="a180a-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="a180a-146">**...** >  **Einstellungen**  >  **Löschen von Browserdaten**  >  **Cookies und gespeicherte Website Daten**</span><span class="sxs-lookup"><span data-stu-id="a180a-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="a180a-147">Der **IndexedDB** -Ordner in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Debuggers zeigt eine Liste der Ursprünge der Ressourcen an, die von der Seite geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a180a-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="a180a-148">Alle IndexedDB-Datenbanken (IDB) werden unter dem Ursprung zusammen mit den Objekt speichern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a180a-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![DevTools-IndexedDB-Manager](./media/storage_indexeddb.png)

### <span data-ttu-id="a180a-150">IndexedDB-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="a180a-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="a180a-151">Auf der *IndexedDB* -Symbolleiste können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a180a-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="a180a-152">**Refresh** ( `Ctrl+F5` ), um die aktuellen Einträge im Objektspeicher oder Index der Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a180a-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="a180a-153">Der IndexedDB-Manager wird nicht automatisch aktualisiert, wenn Änderungen an der Datenbank vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a180a-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="a180a-154">Liste der Objektspeicher Einträge</span><span class="sxs-lookup"><span data-stu-id="a180a-154">Object store entries list</span></span>

<span data-ttu-id="a180a-155">In der *Objektspeicher* -oder *Index* Tabelle können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a180a-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="a180a-156">Überprüfen Sie Ihre Schlüssel-Wert-Paare **, und Sortieren** Sie Sie, indem Sie in der Tabelle auf einen beliebigen Spaltennamen klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="a180a-157">**Refresh** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="a180a-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="a180a-158">**Element löschen** ( `Del` ), um den ausgewählten Eintrag im Objektspeicher oder-Index zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a180a-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="a180a-159">Sie können dies auch über die [Kontextmenü](#context-menu) Option " *Element löschen*" ausführen.</span><span class="sxs-lookup"><span data-stu-id="a180a-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="a180a-160">**Ausgewählte Elemente kopieren** ( `Ctrl+C` ), um das ausgewählte Element in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a180a-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="a180a-161">Sie können dies auch über die [Kontextmenü](#context-menu) Option mit der rechten Maustaste ausführen, um das *ausgewählte Element zu kopieren*.</span><span class="sxs-lookup"><span data-stu-id="a180a-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="a180a-162">**Wählen Sie alle** ( `Ctrl+A` ) aus, um alle Einträge in Ihrem Objektspeicher oder-Index auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a180a-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="a180a-163">Sie können dies auch über die [Kontextmenü](#context-menu) Option mit der rechten Maustaste und dann auf *Alle auswählen*.</span><span class="sxs-lookup"><span data-stu-id="a180a-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="a180a-164">Die Spalten der *Objektspeicher* -oder *Index* Tabelle sind sortierbar:</span><span class="sxs-lookup"><span data-stu-id="a180a-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="a180a-165">Spalte</span><span class="sxs-lookup"><span data-stu-id="a180a-165">Column</span></span> | <span data-ttu-id="a180a-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a180a-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="a180a-167">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a180a-167">Key</span></span> | <span data-ttu-id="a180a-168">Name des Schlüssel-Wert-Paars (identisch mit dem *Primärschlüssel*) beim Durchlaufen eines Objektspeichers; Name des Indexschlüssels (aktuelle Taste des Cursors) beim Durchlaufen eines Indexes</span><span class="sxs-lookup"><span data-stu-id="a180a-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="a180a-169">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="a180a-169">Primary Key</span></span> | <span data-ttu-id="a180a-170">Name des Schlüssel-Wert-Paars (Weitere Informationen zu den IDB- [Schlüsseln](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)finden Sie unter *MDN Web docs* )</span><span class="sxs-lookup"><span data-stu-id="a180a-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="a180a-171">Wert</span><span class="sxs-lookup"><span data-stu-id="a180a-171">Value</span></span> | <span data-ttu-id="a180a-172">Wert des Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="a180a-172">Value of the key-value pair</span></span>

<span data-ttu-id="a180a-173">Weitere Informationen zu [IndexedDB-Konzepten und-Verwendung](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)finden Sie unter *MDN Web docs* .</span><span class="sxs-lookup"><span data-stu-id="a180a-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="a180a-174">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="a180a-174">Context menu</span></span>

<span data-ttu-id="a180a-175">Neben der [ *IndexedDB* -Symbolleiste](#indexeddb-toolbar)können Sie auch Ihre Daten in Objekt speichern oder Indizes über das **Kontextmenü** mit der rechten Maustaste und/oder die Tasten [Kombinationen](#shortcuts)verwalten.</span><span class="sxs-lookup"><span data-stu-id="a180a-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="a180a-176">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="a180a-176">Shortcuts</span></span>

<span data-ttu-id="a180a-177">Aktion</span><span class="sxs-lookup"><span data-stu-id="a180a-177">Action</span></span> | <span data-ttu-id="a180a-178">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a180a-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="a180a-179">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a180a-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="a180a-180">Schlüssel-Wert-Paar löschen</span><span class="sxs-lookup"><span data-stu-id="a180a-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="a180a-181">Kopieren der markierten Elemente</span><span class="sxs-lookup"><span data-stu-id="a180a-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="a180a-182">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="a180a-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="a180a-183">Cookies-Manager</span><span class="sxs-lookup"><span data-stu-id="a180a-183">Cookies manager</span></span>

<span data-ttu-id="a180a-184">Verwenden Sie den *Cookies-Manager* , um die Cookies für die angegebene Domäne zu überprüfen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a180a-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="a180a-185">Der Ordner " **Cookies** " in der [*Ressourcenauswahl*](./debugger.md#resource-picker) des Debuggers zeigt eine Liste der Ursprünge der Ressourcen an, die von der Seite geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a180a-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="a180a-186">Wenn Sie einen dieser Frames auswählen, wird eine Tabelle geöffnet, die die aktuellen Cookies darstellt, die entweder über den [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) -Header oder über ein Skript mit [Document. Cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie)gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="a180a-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![DevTools-Cookies-Manager](./media/storage_cookies.png)

<span data-ttu-id="a180a-188">Über die Registerkarte " *Cookies* " können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="a180a-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="a180a-189">**Aktualisieren** `Ctrl+F5` Sie die [Liste der Cookies](#cookies-list) , um die aktuelle Gruppe von Cookies für die angegebene Domäne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a180a-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="a180a-190">(Die Liste wird nicht automatisch aktualisiert.)</span><span class="sxs-lookup"><span data-stu-id="a180a-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="a180a-191">**Löschen Sie alle Cookies** ( `Ctrl+Shift+Del` ) (Session und permanent) für den Pfad der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="a180a-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="a180a-192">**Löschen Sie alle Sitzungscookies** ( `Ctrl+Del` ) für den Pfad der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="a180a-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="a180a-193">Um die Liste der *Cookies*vollständig zu löschen, müssen Sie möglicherweise **alle Cookies für die Domäne** über die Symbolleiste des [**Netzwerk**](./network.md#toolbar) Panels löschen.</span><span class="sxs-lookup"><span data-stu-id="a180a-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="a180a-194">Liste der Cookies</span><span class="sxs-lookup"><span data-stu-id="a180a-194">Cookies list</span></span>

<span data-ttu-id="a180a-195">In der Tabelle " *Cookies-Liste* " können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a180a-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="a180a-196">Über **prüfen und Sortieren** Sie Ihre Cookies, indem Sie in der Tabelle auf einen beliebigen Spaltennamen klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="a180a-197">**Bearbeiten** Sie den *Namen* und den *Wert* eines vorhandenen Cookies, indem Sie in die Zelle klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="a180a-198">**Löschen** ( `Del` ) eines Cookies aus der [Kontextmenü](#context-menu) Option " *Cookie löschen*"</span><span class="sxs-lookup"><span data-stu-id="a180a-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="a180a-199">**Fügen Sie** ein neues Sitzungscookie für die angegebene *Domäne/* den angegebenen Pfad hinzu, indem Sie auf die leere Zeile am Ende der Tabelle klicken.</span><span class="sxs-lookup"><span data-stu-id="a180a-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="a180a-200">Dies funktioniert nur bei Sitzungscookies; permanente Cookies (mit bestimmten Ablaufdaten) müssen mit traditionellen Methoden festgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a180a-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="a180a-201">Die Werte für *Domäne* und *Pfad* werden automatisch entsprechend dem Speicherort der Seite ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a180a-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="a180a-202">Die Spalten der *Liste "Cookies* " sind sortierbar:</span><span class="sxs-lookup"><span data-stu-id="a180a-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="a180a-203">Spalte</span><span class="sxs-lookup"><span data-stu-id="a180a-203">Column</span></span> | <span data-ttu-id="a180a-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a180a-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="a180a-205">Name</span><span class="sxs-lookup"><span data-stu-id="a180a-205">Name</span></span> | <span data-ttu-id="a180a-206">Name des Cookies</span><span class="sxs-lookup"><span data-stu-id="a180a-206">Name of the cookie</span></span>
<span data-ttu-id="a180a-207">Wert</span><span class="sxs-lookup"><span data-stu-id="a180a-207">Value</span></span> | <span data-ttu-id="a180a-208">Wert des Cookies</span><span class="sxs-lookup"><span data-stu-id="a180a-208">Value of the cookie</span></span>
<span data-ttu-id="a180a-209">Domäne</span><span class="sxs-lookup"><span data-stu-id="a180a-209">Domain</span></span> | <span data-ttu-id="a180a-210">Hostname des Cookies (möglicherweise leer)</span><span class="sxs-lookup"><span data-stu-id="a180a-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="a180a-211">Pfad</span><span class="sxs-lookup"><span data-stu-id="a180a-211">Path</span></span> | <span data-ttu-id="a180a-212">URL-Pfad für das Cookie (möglicherweise leer)</span><span class="sxs-lookup"><span data-stu-id="a180a-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="a180a-213">Läuft ab</span><span class="sxs-lookup"><span data-stu-id="a180a-213">Expires</span></span> | <span data-ttu-id="a180a-214">Maximale Lebensdauer des Cookies als http-Datumsstempel.</span><span class="sxs-lookup"><span data-stu-id="a180a-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="a180a-215">`Expires` `Max-Age` Ist "Nein" oder "wurde" gesetzt, gilt der Eintrag als *Sitzungs* Cookie.</span><span class="sxs-lookup"><span data-stu-id="a180a-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="a180a-216">Nur http</span><span class="sxs-lookup"><span data-stu-id="a180a-216">HTTP only</span></span> | <span data-ttu-id="a180a-217">Gibt an, ob das Cookie mit Directive festgesetzt wurde `HttpOnly` , was darauf hinweist, dass von JavaScript aus kein Zugriff möglich ist.</span><span class="sxs-lookup"><span data-stu-id="a180a-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="a180a-218">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a180a-218">Secure</span></span> | <span data-ttu-id="a180a-219">Gibt an, ob das Cookie mit der `Secure` Direktive gesetzt wurde, was angibt, dass es nur von einer Anforderung mit SSL und dem HTTPS-Protokoll an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a180a-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="a180a-220">Weitere Informationen zu Cookie-Eigenschaften finden Sie im **MDN Web docs** [-Satz-Cookie-](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) Referenz.</span><span class="sxs-lookup"><span data-stu-id="a180a-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="a180a-221">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="a180a-221">Context menu</span></span>

<span data-ttu-id="a180a-222">Neben der [Symbolleiste](#cookies-manager)" *Cookies* " können Sie Ihre Cookies auch über das **Kontextmenü** der rechten Maustaste und/oder die Tasten [Kombinationen](#shortcuts)verwalten.</span><span class="sxs-lookup"><span data-stu-id="a180a-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="a180a-223">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="a180a-223">Shortcuts</span></span>

| <span data-ttu-id="a180a-224">Aktion</span><span class="sxs-lookup"><span data-stu-id="a180a-224">Action</span></span>                     | <span data-ttu-id="a180a-225">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a180a-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="a180a-226">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a180a-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="a180a-227">Löschen eines Cookies</span><span class="sxs-lookup"><span data-stu-id="a180a-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="a180a-228">Alle Cookies löschen</span><span class="sxs-lookup"><span data-stu-id="a180a-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="a180a-229">Löschen aller Sitzungscookies</span><span class="sxs-lookup"><span data-stu-id="a180a-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="a180a-230">Kopieren der markierten Elemente</span><span class="sxs-lookup"><span data-stu-id="a180a-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="a180a-231">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="a180a-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="a180a-232">Cache-Manager</span><span class="sxs-lookup"><span data-stu-id="a180a-232">Cache manager</span></span>

<span data-ttu-id="a180a-233">Wenn Sie auf einen bestimmten Cacheeintrag klicken, wird der Service Worker- **Cache** -Manager geöffnet, in dem Sie Cacheeinträge (*Anforderungs* -und *Antwort* Schlüssel-Wert-Paare) überprüfen und optional löschen können:</span><span class="sxs-lookup"><span data-stu-id="a180a-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Cache-Manager](./media/storage_cache.png)

### <span data-ttu-id="a180a-235">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="a180a-235">Shortcuts</span></span>

#### <span data-ttu-id="a180a-236">Cache-Manager</span><span class="sxs-lookup"><span data-stu-id="a180a-236">Cache manager</span></span>

| <span data-ttu-id="a180a-237">Aktion</span><span class="sxs-lookup"><span data-stu-id="a180a-237">Action</span></span>              | <span data-ttu-id="a180a-238">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a180a-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="a180a-239">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a180a-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="a180a-240">Element löschen</span><span class="sxs-lookup"><span data-stu-id="a180a-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="a180a-241">Kopieren der markierten Elemente</span><span class="sxs-lookup"><span data-stu-id="a180a-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="a180a-242">Alle auswählen</span><span class="sxs-lookup"><span data-stu-id="a180a-242">Select all</span></span>          | `Ctrl` + `A`  |
