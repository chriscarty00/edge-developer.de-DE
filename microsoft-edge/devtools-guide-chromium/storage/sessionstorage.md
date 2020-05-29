---
title: Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612081"
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





# <span data-ttu-id="3d047-103">Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="3d047-103">View And Edit Session Storage With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="3d047-104">In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`sessionStorage`][MDNSessionStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.</span><span class="sxs-lookup"><span data-stu-id="3d047-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="3d047-105">Anzeigen von sessionStorage-Schlüsseln und-Werten</span><span class="sxs-lookup"><span data-stu-id="3d047-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="3d047-106">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d047-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="3d047-107">Standardmäßig wird der Bereich **Manifest** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d047-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="3d047-108">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="3d047-108">Figure 1</span></span>  
    > <span data-ttu-id="3d047-109">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="3d047-109">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  <span data-ttu-id="3d047-111">Erweitern Sie das Menü **Sitzungsspeicher** .</span><span class="sxs-lookup"><span data-stu-id="3d047-111">Expand the **Session Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="3d047-112">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="3d047-112">Figure 2</span></span>  
    > <span data-ttu-id="3d047-113">Das Menü " **Sitzungsspeicher** "</span><span class="sxs-lookup"><span data-stu-id="3d047-113">The **Session Storage** Menu</span></span>  
    > ![Das Menü "Sitzungsspeicher"][ImageSessionStorageMenu]  

1.  <span data-ttu-id="3d047-115">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d047-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="3d047-116">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="3d047-116">Figure 3</span></span>  
    > <span data-ttu-id="3d047-117">Die sessionStorage-Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="3d047-117">The sessionStorage key-value pairs</span></span>  
    > ![Die Schlüssel-Wert-Paare "sessionStorage"][ImageSessionStorage]  

1.  <span data-ttu-id="3d047-119">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d047-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="3d047-120">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="3d047-120">Figure 4</span></span>  
    > <span data-ttu-id="3d047-121">Anzeigen des Werts des `x-sid` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d047-121">Viewing the value of the `x-sid` key</span></span>  
    > ![Anzeigen des Werts des x-sid-Schlüssels][ImageSessionStorageViewer]  

## <span data-ttu-id="3d047-123">Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="3d047-123">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="3d047-124">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="3d047-124">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3d047-125">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3d047-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="3d047-126">DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.</span><span class="sxs-lookup"><span data-stu-id="3d047-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="3d047-127">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="3d047-127">Figure 5</span></span>  
    > <span data-ttu-id="3d047-128">Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen</span><span class="sxs-lookup"><span data-stu-id="3d047-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen][ImageSessionStorageCreate]  

## <span data-ttu-id="3d047-130">Bearbeiten von sessionStorage-Schlüsseln oder-Werten</span><span class="sxs-lookup"><span data-stu-id="3d047-130">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="3d047-131">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="3d047-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3d047-132">Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3d047-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="3d047-133">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="3d047-133">Figure 6</span></span>  
    > <span data-ttu-id="3d047-134">Bearbeiten eines `sessionStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d047-134">Editing a `sessionStorage` key</span></span>  
    > ![Bearbeiten eines sessionStorage-Schlüssels][ImageSessionStorageEdit]  

## <span data-ttu-id="3d047-136">Löschen von sessionStorage-Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="3d047-136">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="3d047-137">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="3d047-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3d047-138">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d047-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="3d047-139">DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3d047-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="3d047-140">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen Löschen** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="3d047-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="3d047-141">Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="3d047-141">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="3d047-142">[Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="3d047-142">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="3d047-143">Wählen Sie **alle** löschen aus ![ ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="3d047-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="3d047-144">Interagieren mit sessionStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="3d047-144">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="3d047-145">Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `sessionStorage` der **Konsole**zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="3d047-145">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="3d047-146">Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `sessionStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die Seite zugreifen möchten, auf der Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="3d047-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    > ##### <span data-ttu-id="3d047-147">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="3d047-147">Figure 7</span></span>  
    > <span data-ttu-id="3d047-148">Ändern des JavaScript-Kontexts der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3d047-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Ändern des JavaScript-Kontexts der Konsole][ImageJSContext]  

1.  <span data-ttu-id="3d047-150">Führen Sie Ihre `sessionStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.</span><span class="sxs-lookup"><span data-stu-id="3d047-150">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="3d047-151">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="3d047-151">Figure 8</span></span>  
    > <span data-ttu-id="3d047-152">Interagieren mit `sessionStorage` der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3d047-152">Interacting with `sessionStorage` from the **Console**</span></span>  
    > ![Interagieren mit sessionStorage über die Konsole][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Abbildung 2: das Menü "Sitzungsspeicher""  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Abbildung 3: sessionStorage-Schlüssel-Wert-Paare"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Abbildung 4: Anzeigen des Werts des x-sid-Schlüssels"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Abbildung 5: der leere Teil der Tabelle, doppelklicken Sie, um ein neues Schlüssel-Wert-Paar zu erstellen"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Abbildung 6: Bearbeiten eines sessionStorage-Schlüssels"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Abbildung 7: Ändern des JavaScript-Kontexts der Konsole"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Abbildung 8: interagieren mit sessionStorage über die Konsole"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="3d047-164">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d047-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3d047-165">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d047-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="3d047-167">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d047-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
