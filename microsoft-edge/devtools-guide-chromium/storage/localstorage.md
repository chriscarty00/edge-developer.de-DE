---
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612011"
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





# <span data-ttu-id="9be39-103">Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9be39-103">View And Edit Local Storage With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="9be39-104">In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`localStorage`][MDNWindowsLocalStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.</span><span class="sxs-lookup"><span data-stu-id="9be39-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`localStorage`][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="9be39-105">Anzeigen von localStorage-Schlüsseln und-Werten</span><span class="sxs-lookup"><span data-stu-id="9be39-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="9be39-106">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9be39-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="9be39-107">Standardmäßig wird der Bereich **Manifest** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9be39-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="9be39-108">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="9be39-108">Figure 1</span></span>  
    > <span data-ttu-id="9be39-109">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="9be39-109">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  <span data-ttu-id="9be39-111">Erweitern Sie das Menü **lokaler Speicher** .</span><span class="sxs-lookup"><span data-stu-id="9be39-111">Expand the **Local Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="9be39-112">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="9be39-112">Figure 2</span></span>  
    > <span data-ttu-id="9be39-113">Das Menü " **lokaler Speicher** " zeigt zwei Domänen an: `https://business.bing.com` und</span><span class="sxs-lookup"><span data-stu-id="9be39-113">The **Local Storage** menu shows two domains: `https://business.bing.com` and</span></span> `https://www.bing.com`  
    > ![Das Menü "lokaler Speicher"][ImageLocalStorageMenu]  

1.  <span data-ttu-id="9be39-115">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9be39-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="9be39-116">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="9be39-116">Figure 3</span></span>  
    > <span data-ttu-id="9be39-117">Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne</span><span class="sxs-lookup"><span data-stu-id="9be39-117">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    > ![Die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne][ImageLocalStorage]  

1.  <span data-ttu-id="9be39-119">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9be39-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="9be39-120">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="9be39-120">Figure 4</span></span>  
    > <span data-ttu-id="9be39-121">Anzeigen des Werts des `eventLogQueue_Online` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="9be39-121">Viewing the value of the `eventLogQueue_Online` key</span></span>  
    > ![Anzeigen des Werts des eventLogQueue_Online Schlüssels][ImageLocalStorageViewer]  

## <span data-ttu-id="9be39-123">Erstellen eines neuen `localStorage` Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="9be39-123">Create a new `localStorage` key-value pair</span></span>   

1.  <span data-ttu-id="9be39-124">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="9be39-124">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="9be39-125">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9be39-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="9be39-126">DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.</span><span class="sxs-lookup"><span data-stu-id="9be39-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="9be39-127">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="9be39-127">Figure 5</span></span>  
    > <span data-ttu-id="9be39-128">Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen</span><span class="sxs-lookup"><span data-stu-id="9be39-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen][ImageLocalStorageCreate]  

## <span data-ttu-id="9be39-130">Bearbeiten von `localStorage` Schlüsseln oder Werten</span><span class="sxs-lookup"><span data-stu-id="9be39-130">Edit `localStorage` keys or values</span></span>   

1.  <span data-ttu-id="9be39-131">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="9be39-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="9be39-132">Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9be39-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="9be39-133">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="9be39-133">Figure 6</span></span>  
    > <span data-ttu-id="9be39-134">Bearbeiten eines `localStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="9be39-134">Editing a `localStorage` key</span></span>  
    > ![Bearbeiten eines localStorage-Schlüssels][ImageLocalStorageEdit]  

## <span data-ttu-id="9be39-136">Löschen von `localStorage` Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="9be39-136">Delete `localStorage` key-value pairs</span></span>   

1.  <span data-ttu-id="9be39-137">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="9be39-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="9be39-138">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="9be39-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="9be39-139">DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.</span><span class="sxs-lookup"><span data-stu-id="9be39-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="9be39-140">Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen Löschen** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="9be39-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="9be39-141">Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="9be39-141">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="9be39-142">[Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="9be39-142">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="9be39-143">Wählen Sie **alle** löschen aus ![ ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="9be39-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="9be39-144">Interagieren mit `localStorage` der Konsole</span><span class="sxs-lookup"><span data-stu-id="9be39-144">Interact with `localStorage` from the Console</span></span>   

<span data-ttu-id="9be39-145">Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `localStorage` der **Konsole**zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="9be39-145">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="9be39-146">Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `localStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die angezeigte Seite zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="9be39-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    > ##### <span data-ttu-id="9be39-147">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="9be39-147">Figure 7</span></span>  
    > <span data-ttu-id="9be39-148">Ändern des JavaScript-Kontexts der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="9be39-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Ändern des JavaScript-Kontexts der Konsole][ImageJSContext]  

1.  <span data-ttu-id="9be39-150">Führen Sie Ihre `localStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.</span><span class="sxs-lookup"><span data-stu-id="9be39-150">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="9be39-151">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="9be39-151">Figure 8</span></span>  
    > <span data-ttu-id="9be39-152">Interagieren mit `localStorage` der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="9be39-152">Interacting with `localStorage` from the **Console**</span></span>  
    > ![Interagieren mit localStorage über die Konsole][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Abbildung 2: lokales Speicher-Menü"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Abbildung 3: die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Abbildung 4: Anzeigen des Werts des eventLogQueue_Online Schlüssels"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Abbildung 5: der leere Teil der Tabelle, doppelklicken Sie, um ein neues Schlüssel-Wert-Paar zu erstellen"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Abbildung 6: Bearbeiten eines localStorage-Schlüssels"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Abbildung 7: Ändern des JavaScript-Kontexts der Konsole"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Abbildung 8: interagieren mit localStorage über die Konsole"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="9be39-164">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be39-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9be39-165">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9be39-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9be39-167">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9be39-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
