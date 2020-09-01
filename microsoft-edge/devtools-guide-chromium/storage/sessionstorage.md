---
title: Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d0631f69a082a2a73c51e4359c21cf94636d665e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983569"
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





# <span data-ttu-id="6557e-103">Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="6557e-103">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="6557e-104">In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`sessionStorage`][MDNSessionStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.</span><span class="sxs-lookup"><span data-stu-id="6557e-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="6557e-105">Anzeigen von sessionStorage-Schlüsseln und-Werten</span><span class="sxs-lookup"><span data-stu-id="6557e-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="6557e-106">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6557e-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="6557e-107">Standardmäßig wird der Bereich **Manifest** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6557e-107">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="6557e-109">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="6557e-109">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6557e-110">Erweitern Sie das Menü **Sitzungsspeicher** .</span><span class="sxs-lookup"><span data-stu-id="6557e-110">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Das Menü "Sitzungsspeicher"" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="6557e-112">Das Menü " **Sitzungsspeicher** "</span><span class="sxs-lookup"><span data-stu-id="6557e-112">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6557e-113">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6557e-113">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Die Schlüssel-Wert-Paare "sessionStorage"" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="6557e-115">Die `sessionStorage` Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="6557e-115">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6557e-116">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6557e-116">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Anzeigen des Werts des x-sid-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="6557e-118">Anzeigen des Werts des `x-sid` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6557e-118">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6557e-119">Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="6557e-119">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="6557e-120">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="6557e-120">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6557e-121">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6557e-121">Double-click the empty part of the table.</span></span>  <span data-ttu-id="6557e-122">DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.</span><span class="sxs-lookup"><span data-stu-id="6557e-122">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="6557e-124">Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen</span><span class="sxs-lookup"><span data-stu-id="6557e-124">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6557e-125">Bearbeiten von sessionStorage-Schlüsseln oder-Werten</span><span class="sxs-lookup"><span data-stu-id="6557e-125">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="6557e-126">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="6557e-126">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6557e-127">Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6557e-127">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Bearbeiten eines sessionStorage-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="6557e-129">Bearbeiten eines `sessionStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6557e-129">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6557e-130">Löschen von sessionStorage-Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="6557e-130">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="6557e-131">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="6557e-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6557e-132">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="6557e-132">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="6557e-133">DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.</span><span class="sxs-lookup"><span data-stu-id="6557e-133">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="6557e-134">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen** \ ( ![ Auswahl löschen ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6557e-134">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="6557e-135">Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="6557e-135">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="6557e-136">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="6557e-136">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="6557e-137">Wählen Sie **Alle löschen** \ ( ![ Alle löschen ][ImageClearIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="6557e-137">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="6557e-138">Interagieren mit sessionStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="6557e-138">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="6557e-139">Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `sessionStorage` der **Konsole**zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="6557e-139">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="6557e-140">Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `sessionStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die Seite zugreifen möchten, auf der Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="6557e-140">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="6557e-142">Ändern des JavaScript-Kontexts der Konsole</span><span class="sxs-lookup"><span data-stu-id="6557e-142">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6557e-143">Führen Sie Ihre `sessionStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.</span><span class="sxs-lookup"><span data-stu-id="6557e-143">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagieren mit sessionStorage über die Konsole" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="6557e-145">Interagieren mit `sessionStorage` der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="6557e-145">Interact with `sessionStorage` from the **Console**</span></span>  
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
> <span data-ttu-id="6557e-148">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6557e-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6557e-149">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6557e-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6557e-151">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6557e-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
