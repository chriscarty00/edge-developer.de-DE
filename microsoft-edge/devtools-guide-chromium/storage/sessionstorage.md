---
description: Anzeigen und Bearbeiten von sessionStorage mit dem Sitzungsspeicherbereich und der Konsole.
title: Anzeigen und Bearbeiten des Sitzungsspeichers mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: cf00d71302e7a1f16ba1cceaa17c9380245d12f8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398007"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="23580-104">Anzeigen und Bearbeiten des Sitzungsspeichers mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23580-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="23580-105">In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] zum Anzeigen, Bearbeiten und Löschen von SessionStorage-Schlüssel-Wert-Paaren verwenden. [][MDNSessionStorage]</span><span class="sxs-lookup"><span data-stu-id="23580-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [sessionStorage][MDNSessionStorage] key-value pairs.</span></span>  

## <a name="view-sessionstorage-keys-and-values"></a><span data-ttu-id="23580-106">Anzeigen von sessionStorage-Schlüsseln und -Werten</span><span class="sxs-lookup"><span data-stu-id="23580-106">View sessionStorage keys and values</span></span>  

1.  <span data-ttu-id="23580-107">Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="23580-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="23580-108">Der **Manifestbereich** wird standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23580-108">The **Manifest** panel is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="23580-110">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="23580-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23580-111">Erweitern Sie **das Menü Sitzungsspeicher.**</span><span class="sxs-lookup"><span data-stu-id="23580-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Das Menü "Sitzungsspeicher"" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="23580-113">Das **Menü "Sitzungsspeicher"**</span><span class="sxs-lookup"><span data-stu-id="23580-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23580-114">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="23580-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Die SessionStorage-Schlüssel-Wert-Paare" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="23580-116">Die `sessionStorage` Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="23580-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23580-117">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unterhalb der Tabelle anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="23580-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Anzeigen des Werts des x-sid-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="23580-119">Anzeigen des Werts des `x-sid` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="23580-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a><span data-ttu-id="23580-120">Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="23580-120">Create a new sessionStorage key-value pair</span></span>  

1.  <span data-ttu-id="23580-121">[Zeigen Sie die sessionStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="23580-121">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="23580-122">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="23580-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="23580-123">DevTools erstellt eine neue Zeile und konzentriert den Cursor in der **Spalte Schlüssel.**</span><span class="sxs-lookup"><span data-stu-id="23580-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen." lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="23580-125">Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23580-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a><span data-ttu-id="23580-126">Bearbeiten von sessionStorage-Schlüsseln oder -Werten</span><span class="sxs-lookup"><span data-stu-id="23580-126">Edit sessionStorage keys or values</span></span>  

1.  <span data-ttu-id="23580-127">[Zeigen Sie die sessionStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="23580-127">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="23580-128">Doppelklicken Sie in der Spalte **Schlüssel** oder **Wert** auf eine Zelle, um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="23580-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Bearbeiten eines sessionStorage-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="23580-130">Bearbeiten eines `sessionStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="23580-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a><span data-ttu-id="23580-131">SessionStorage-Schlüssel-Wert-Paare löschen</span><span class="sxs-lookup"><span data-stu-id="23580-131">Delete sessionStorage key-value pairs</span></span>  

1.  <span data-ttu-id="23580-132">[Zeigen Sie `sessionStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="23580-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="23580-133">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="23580-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="23580-134">DevTools hebt es blau hervor, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="23580-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="23580-135">Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ][ImageDeleteIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="23580-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="23580-136">Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="23580-136">Delete all sessionStorage key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="23580-137">[Zeigen Sie `sessionStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="23580-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="23580-138">Wählen **Sie Alle löschen** \( Alle löschen ![ ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="23580-138">Choose **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <a name="interact-with-sessionstorage-from-the-console"></a><span data-ttu-id="23580-139">Interagieren mit sessionStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="23580-139">Interact with sessionStorage from the Console</span></span>  

<span data-ttu-id="23580-140">Da Sie JavaScript in der Konsole \*\*\*\* ausführen können **und**die Konsole Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit über die Konsole `sessionStorage` zu **interagieren.**</span><span class="sxs-lookup"><span data-stu-id="23580-140">Since you may run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="23580-141">Verwenden Sie **das Menü JavaScript-Kontexte,** \*\*\*\* um den JavaScript-Kontext der Konsole zu ändern, wenn Sie auf die Schlüssel-Wert-Paare einer anderen Domäne als der Seite zugreifen möchten, auf der `sessionStorage` Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="23580-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="23580-143">Ändern des JavaScript-Kontexts der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="23580-143">Change the JavaScript context of the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="23580-144">Führen Sie `sessionStorage` Ihre Ausdrücke in **der Konsole**aus, die mit Ihrem JavaScript identisch ist.</span><span class="sxs-lookup"><span data-stu-id="23580-144">Run your `sessionStorage` expressions in the **Console**, the same as your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagieren mit sessionStorage über die Konsole" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="23580-146">Interagieren mit `sessionStorage` über die **Konsole**</span><span class="sxs-lookup"><span data-stu-id="23580-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="23580-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="23580-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="23580-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23580-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="23580-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="23580-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="23580-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="23580-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
