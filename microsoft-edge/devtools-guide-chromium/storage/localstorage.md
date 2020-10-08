---
description: Anzeigen und Bearbeiten von localStorage mit dem lokalen Speicherbereich und der Konsole
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: aa5365d1764ea0db537ea24464f9c76441f05322
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993555"
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





# <span data-ttu-id="ac804-104">Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="ac804-104">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ac804-105">In diesem Leitfaden wird gezeigt, wie Sie [localStorage][MDNWindowsLocalStorage] -Schlüssel-Wert-Paare mithilfe von [Microsoft Edge devtools][MicrosoftEdgeDevTools] anzeigen, bearbeiten und löschen.</span><span class="sxs-lookup"><span data-stu-id="ac804-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="ac804-106">Anzeigen von localStorage-Schlüsseln und-Werten</span><span class="sxs-lookup"><span data-stu-id="ac804-106">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="ac804-107">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ac804-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="ac804-108">Standardmäßig wird der Bereich **Manifest** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac804-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="ac804-110">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="ac804-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ac804-111">Erweitern Sie das Menü **lokaler Speicher** .</span><span class="sxs-lookup"><span data-stu-id="ac804-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="ac804-113">Das Menü " **lokaler Speicher** "</span><span class="sxs-lookup"><span data-stu-id="ac804-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ac804-114">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac804-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="ac804-116">Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne</span><span class="sxs-lookup"><span data-stu-id="ac804-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ac804-117">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac804-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="ac804-119">Anzeigen des Werts des `eventLogQueue_Online` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ac804-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ac804-120">Erstellen eines neuen localStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="ac804-120">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="ac804-121">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="ac804-121">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="ac804-122">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ac804-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="ac804-123">DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.</span><span class="sxs-lookup"><span data-stu-id="ac804-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="ac804-125">Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen</span><span class="sxs-lookup"><span data-stu-id="ac804-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ac804-126">Bearbeiten von localStorage-Schlüsseln oder-Werten</span><span class="sxs-lookup"><span data-stu-id="ac804-126">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="ac804-127">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="ac804-127">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="ac804-128">Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac804-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="ac804-130">Bearbeiten eines `localStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ac804-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ac804-131">Löschen von localStorage-Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="ac804-131">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="ac804-132">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="ac804-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="ac804-133">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="ac804-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="ac804-134">DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac804-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="ac804-135">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen** \ ( ![ Auswahl löschen ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ac804-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="ac804-136">Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="ac804-136">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="ac804-137">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="ac804-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="ac804-138">Wählen Sie **Alle löschen** \ ( ![ Alle löschen ][ImageClearIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="ac804-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="ac804-139">Interagieren mit localStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="ac804-139">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="ac804-140">Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `localStorage` der **Konsole**zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="ac804-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="ac804-141">Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `localStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die angezeigte Seite zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="ac804-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="ac804-143">Ändern des JavaScript-Kontexts der Konsole</span><span class="sxs-lookup"><span data-stu-id="ac804-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ac804-144">Führen Sie Ihre `localStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.</span><span class="sxs-lookup"><span data-stu-id="ac804-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="ac804-146">Interagieren mit `localStorage` der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="ac804-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="ac804-149">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac804-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ac804-150">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="ac804-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="ac804-152">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ac804-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
