---
description: Informationen zum Anzeigen und Bearbeiten von sessionStorage mit dem Sitzungsspeicher Bereich und der Konsole.
title: Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993548"
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





# <span data-ttu-id="07616-104">Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="07616-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="07616-105">In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`sessionStorage`][MDNSessionStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.</span><span class="sxs-lookup"><span data-stu-id="07616-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="07616-106">Anzeigen von sessionStorage-Schlüsseln und-Werten</span><span class="sxs-lookup"><span data-stu-id="07616-106">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="07616-107">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07616-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="07616-108">Standardmäßig wird der Bereich **Manifest** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07616-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="07616-110">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="07616-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07616-111">Erweitern Sie das Menü **Sitzungsspeicher** .</span><span class="sxs-lookup"><span data-stu-id="07616-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="07616-113">Das Menü " **Sitzungsspeicher** "</span><span class="sxs-lookup"><span data-stu-id="07616-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07616-114">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="07616-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="07616-116">Die `sessionStorage` Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="07616-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07616-117">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="07616-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="07616-119">Anzeigen des Werts des `x-sid` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="07616-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="07616-120">Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="07616-120">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="07616-121">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="07616-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="07616-122">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="07616-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="07616-123">DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.</span><span class="sxs-lookup"><span data-stu-id="07616-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="07616-125">Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen</span><span class="sxs-lookup"><span data-stu-id="07616-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="07616-126">Bearbeiten von sessionStorage-Schlüsseln oder-Werten</span><span class="sxs-lookup"><span data-stu-id="07616-126">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="07616-127">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="07616-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="07616-128">Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="07616-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="07616-130">Bearbeiten eines `sessionStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="07616-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="07616-131">Löschen von sessionStorage-Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="07616-131">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="07616-132">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="07616-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="07616-133">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="07616-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="07616-134">DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.</span><span class="sxs-lookup"><span data-stu-id="07616-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="07616-135">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen** \ ( ![ Auswahl löschen ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="07616-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="07616-136">Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="07616-136">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="07616-137">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="07616-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="07616-138">Wählen Sie **Alle löschen** \ ( ![ Alle löschen ][ImageClearIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="07616-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="07616-139">Interagieren mit sessionStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="07616-139">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="07616-140">Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `sessionStorage` der **Konsole**zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="07616-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="07616-141">Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `sessionStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die Seite zugreifen möchten, auf der Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="07616-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="07616-143">Ändern des JavaScript-Kontexts der Konsole</span><span class="sxs-lookup"><span data-stu-id="07616-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07616-144">Führen Sie Ihre `sessionStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.</span><span class="sxs-lookup"><span data-stu-id="07616-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="07616-146">Interagieren mit `sessionStorage` der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="07616-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="07616-149">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07616-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="07616-150">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="07616-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="07616-152">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07616-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
