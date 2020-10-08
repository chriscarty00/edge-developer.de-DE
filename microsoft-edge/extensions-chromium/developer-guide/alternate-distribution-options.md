---
description: Der Prozess der Verteilung der Erweiterung um einen anderen Mechanismus als überprüfte Speicher
title: Alternative Methode zur Verteilung der Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015695"
---
# <span data-ttu-id="fd76d-104">Alternative Methode zur Verteilung der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="fd76d-104">Alternate Method of Distributing Extension</span></span>  

<span data-ttu-id="fd76d-105">Wenn Sie ein Entwickler sind, der eine Erweiterung als Teil des Installationsvorgangs für andere Software oder einen Netzwerkadministrator verteilen möchte, der eine Erweiterung in der gesamten Organisation verteilen möchte, unterstützt Microsoft Edge die folgenden Erweiterungs Installationsmethoden:</span><span class="sxs-lookup"><span data-stu-id="fd76d-105">If you are a developer who wants to distribute an Extension as part of the installation process for other software, or a network admin that want to distribute an Extension throughout their organization, Microsoft Edge supports the following Extension installation methods:</span></span>  

*   **<span data-ttu-id="fd76d-106">Verwenden der Windows-Registrierung \ (nur Windows \)</span><span class="sxs-lookup"><span data-stu-id="fd76d-106">Using the Windows registry \(Windows only\)</span></span>**  

<span data-ttu-id="fd76d-107">Microsoft Edge unterstützt die Installation einer Erweiterung, die auf einer `update_URL` .</span><span class="sxs-lookup"><span data-stu-id="fd76d-107">Microsoft Edge supports installing an Extension hosted at an `update_URL`.</span></span>  <span data-ttu-id="fd76d-108">Unter Windows muss der `update_URL` Verweis auf den Microsoft Edge Addons-Katalog (Microsoft Edge Addons \) verweisen, in dem die Erweiterung gehostet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fd76d-108">On Windows, the `update_URL` must point to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\) where the Extension must be hosted.</span></span>  

> [!NOTE]
> <span data-ttu-id="fd76d-109">Externe Installation der Erweiterung über eine JSON-Einstellungen-Datei für macOS</span><span class="sxs-lookup"><span data-stu-id="fd76d-109">External installation of Extension via a preferences json file for macOS</span></span> <!--and Linux--> <span data-ttu-id="fd76d-110">werden noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd76d-110">are not supported yet.</span></span>  <span data-ttu-id="fd76d-111">Dieser Funktions Support steht in Kürze zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd76d-111">This feature support will soon be available.</span></span>

## <span data-ttu-id="fd76d-112">Verwenden der Windows-Registrierung</span><span class="sxs-lookup"><span data-stu-id="fd76d-112">Using the Windows registry</span></span>  

<span data-ttu-id="fd76d-113">Veröffentlichen Sie zunächst die Erweiterung in den Microsoft Edge-Addons, oder Verpacken Sie eine. Wagon-Datei, und stellen Sie sicher, dass Sie erfolgreich installiert wird.</span><span class="sxs-lookup"><span data-stu-id="fd76d-113">First, publish the Extension in the Microsoft Edge Addons, or package a .crx file and make sure that it installs successfully.</span></span>  

<span data-ttu-id="fd76d-114">Die Schritte zum Installieren der Erweiterung über die Registrierung in Windows sind:</span><span class="sxs-lookup"><span data-stu-id="fd76d-114">The steps to install Extension via registry in windows are:</span></span>  

*   <span data-ttu-id="fd76d-115">Suchen oder erstellen Sie den folgenden Schlüssel in der Registrierung:</span><span class="sxs-lookup"><span data-stu-id="fd76d-115">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="fd76d-116">32-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="fd76d-116">32-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   <span data-ttu-id="fd76d-117">64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="fd76d-117">64-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   <span data-ttu-id="fd76d-118">Erstellen Sie einen neuen Schlüssel \ (Ordner \) unter dem Erweiterungs Schlüssel mit dem gleichen Namen wie die ID der Erweiterung \ (beispielsweise `aaaaaaaaaabbbbbbbbbbcccccccccc` \).</span><span class="sxs-lookup"><span data-stu-id="fd76d-118">Create a new key \(folder\) under the Extensions key with the same name as the ID of your Extension \(for example, `aaaaaaaaaabbbbbbbbbbcccccccccc`\).</span></span>  
*   <span data-ttu-id="fd76d-119">Erstellen Sie in Ihrem Erweiterungs Schlüssel eine Eigenschaft, `update_url` und legen Sie Sie auf den Wert: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (dieser verweist auf den Namen ihrer Erweiterung in Microsoft Edge-Addons).</span><span class="sxs-lookup"><span data-stu-id="fd76d-119">In your Extension key, create a property, `update_url`, and set it to the value: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`,  \(this points to the crx of your extension in the Microsoft Edge Addons\).</span></span> <span data-ttu-id="fd76d-120">Wenn Sie eine Erweiterung aus dem Chrome Web Store installieren möchten, geben Sie die URL des Chrome Web Store-Updates an `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="fd76d-120">If you want to install an extension from the Chrome Web Store, please provide the Chrome Web Store update URL, `https://clients2.google.com/service/update2/crx`.</span></span>  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   <span data-ttu-id="fd76d-121">Starten Sie den Browser, und wechseln `edge://extensions` Sie zu; die Erweiterung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd76d-121">Launch the browser and go to `edge://extensions`; you should see the extension listed.</span></span>  

## <span data-ttu-id="fd76d-122">Aktualisieren und deinstallieren</span><span class="sxs-lookup"><span data-stu-id="fd76d-122">Updating and uninstalling</span></span>  

<span data-ttu-id="fd76d-123">Microsoft Edge scannt die Metadaten-Einträge in der Registrierung jedes Mal, wenn der Browser gestartet wird, und nimmt alle erforderlichen Änderungen an den installierten externen Erweiterungen vor.</span><span class="sxs-lookup"><span data-stu-id="fd76d-123">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any necessary changes to the installed external extensions.</span></span>  

<span data-ttu-id="fd76d-124">Wenn Sie Ihre Erweiterung auf eine neue Version aktualisieren möchten, aktualisieren Sie die Datei, und aktualisieren Sie dann die Version in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fd76d-124">To update your extension to a new version, update the file, and then update the version in the registry.</span></span>  

<span data-ttu-id="fd76d-125">Wenn Sie Ihre Erweiterung deinstallieren möchten (beispielsweise wenn Ihre Software deinstalliert wird), entfernen Sie Ihre Einstellungsdatei \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) oder die Metadaten aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fd76d-125">To uninstall your extension \(for example, if your software is uninstalled\), remove your preference file \(`aaaaaaaaaabbbbbbbbbbcccccccccc.json`\) or the metadata from the registry.</span></span>  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="fd76d-126">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd76d-126">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fd76d-127">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/apps/external_extensions).</span><span class="sxs-lookup"><span data-stu-id="fd76d-127">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="fd76d-129">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd76d-129">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
