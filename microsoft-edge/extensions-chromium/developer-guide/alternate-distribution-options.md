---
description: Informationen zum Verteilen von Erweiterungen mithilfe alternativer Methoden, die keine überprüften Speicher verwenden
title: Alternative Methode zum Verteilen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343150"
---
# <span data-ttu-id="bcfdc-104">Alternative Erweiterungsverteilungsmethoden</span><span class="sxs-lookup"><span data-stu-id="bcfdc-104">Alternate extension distribution methods</span></span>  

<span data-ttu-id="bcfdc-105">Im Allgemeinen werden Erweiterungen über den Microsoft Edge-Add-Ons-Store verteilt.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-105">Generally, extensions are distributed through the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="bcfdc-106">Es gibt einige Szenarien, in denen Entwickler Erweiterungen mithilfe alternativer Methoden verteilen müssen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-106">There are some scenarios where developers may need to distribute extensions using alternate methods.</span></span> <span data-ttu-id="bcfdc-107">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-107">For example:</span></span>

1.  <span data-ttu-id="bcfdc-108">Die Erweiterung ist mit anderer Software verknüpft und sollte zusammen mit dem Rest der gebündelten Software installiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-108">The extension is associated with other software, and it should be installed together with the rest of the bundled software.</span></span>   
1.  <span data-ttu-id="bcfdc-109">Netzwerkadministratoren möchten eine Erweiterung in ihrer Organisation verteilen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-109">Network administrators want to distribute an extension throughout their organization.</span></span>   

<span data-ttu-id="bcfdc-110">Erweiterungen, die nicht aus dem Edge-Add-Ons-Speicher geladen werden, werden als extern installierte Erweiterungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-110">Extensions that are not loaded from the Edge Add-ons store are referred to as externally installed extensions.</span></span> <span data-ttu-id="bcfdc-111">Die folgende Liste enthält alternative Methoden zum Verteilen extern installierter Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-111">The following list provides alternate methods of distributing externally installed extensions.</span></span> 

*   <span data-ttu-id="bcfdc-112">Verwenden Sie die Windows-Registrierung (nur Windows).</span><span class="sxs-lookup"><span data-stu-id="bcfdc-112">Use the Windows registry (Windows only).</span></span>  
*   <span data-ttu-id="bcfdc-113">Verwenden Sie eine bevorzugten JSON-Datei (macOS und Linux).</span><span class="sxs-lookup"><span data-stu-id="bcfdc-113">Use a preferences JSON file (macOS and Linux).</span></span>  
    
## <span data-ttu-id="bcfdc-114">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcfdc-114">Before you begin</span></span>  

<span data-ttu-id="bcfdc-115">Stellen Sie sicher, dass Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Speicher veröffentlichen, oder packen Sie eine Datei, und stellen Sie sicher, dass sie erfolgreich auf Ihrem `.crx` Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-115">Ensure that you publish your extension in the Microsoft Edge Add-ons store, or package a `.crx` file and ensure that it installs successfully on your computer.</span></span>  <span data-ttu-id="bcfdc-116">Wenn Sie die Datei mit der installieren, stellen Sie sicher, dass Sie unter dieser URL zu `.crx` `update_URL` Ihrer Erweiterung navigieren können.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-116">If you install the `.crx` file using the `update_URL`, ensure you can navigate to your extension at that URL.</span></span>  

<span data-ttu-id="bcfdc-117">Stellen Sie außerdem sicher, dass Sie über die folgenden Informationen verfügen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-117">Also, ensure that you have the following information.</span></span>    

1.  <span data-ttu-id="bcfdc-118">Der Dateipfad der `.crx` Datei oder `update_URL` die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-118">The file path of the `.crx` file, or the `update_URL` of your extension.</span></span>
1.  <span data-ttu-id="bcfdc-119">Die Version Ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-119">The version of your extension.</span></span>  <span data-ttu-id="bcfdc-120">Die Versionsinformationen sind in Ihrer Manifestdatei oder in Microsoft Edge nach `edge://extensions` dem Laden der verpackten Erweiterung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-120">The version information is available in your manifest file, or in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>   
1.  <span data-ttu-id="bcfdc-121">Die ID Ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-121">The ID of your extension.</span></span>  <span data-ttu-id="bcfdc-122">Die ID-Informationen sind in Microsoft Edge nach `edge://extensions` dem Laden der verpackten Erweiterung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-122">The ID information is available in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>  

> [!NOTE] 
> <span data-ttu-id="bcfdc-123">In den folgenden `1.0` Beispielen wird die Version und `aaaaaaaaaabbbbbbbbbbcccccccccc` die ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-123">The following examples use `1.0` as the version, and `aaaaaaaaaabbbbbbbbbbcccccccccc` for the ID.</span></span>  

## <span data-ttu-id="bcfdc-124">Verwenden der Windows-Registrierung (nur Windows)</span><span class="sxs-lookup"><span data-stu-id="bcfdc-124">Use the Windows registry (Windows only)</span></span>  

<span data-ttu-id="bcfdc-125">Führen Sie die folgenden Schritte aus, um Ihre Erweiterung mithilfe der Windows-Registrierung zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-125">To distribute your extension using the Windows registry, perform the following steps.</span></span>

1.  <span data-ttu-id="bcfdc-126">Suchen oder erstellen Sie den folgenden Schlüssel in der Registrierung:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-126">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="bcfdc-127">32-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="bcfdc-127">32-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`.</span></span>  
    *   <span data-ttu-id="bcfdc-128">64-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="bcfdc-128">64-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`.</span></span>  
1.  <span data-ttu-id="bcfdc-129">Erstellen Sie einen neuen Schlüssel oder Ordner unter **"Erweiterungen"** mit demselben Namen wie die ID Ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-129">Create a new key, or folder, under **Extensions** with the same name as the ID of your extension.</span></span> <span data-ttu-id="bcfdc-130">Erstellen Sie beispielsweise den Schlüssel mit dem Namen `aaaaaaaaaabbbbbbbbbbcccccccccc` .</span><span class="sxs-lookup"><span data-stu-id="bcfdc-130">For example, create the key with the name `aaaaaaaaaabbbbbbbbbbcccccccccc`.</span></span>  
1.  <span data-ttu-id="bcfdc-131">Erstellen Sie **im Schlüssel "Extensions"** die `update_url` Eigenschaft, und legen Sie den Wert auf . `https://edge.microsoft.com/extensionwebstorebase/v1/crx`</span><span class="sxs-lookup"><span data-stu-id="bcfdc-131">In the **Extensions** key, create the `update_url` property, and set the value to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="bcfdc-132">Die Eigenschaft verweist auf die Datei Ihrer Erweiterung im `update_url` `.crx` Microsoft Edge-Add-Ons-Speicher.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-132">The `update_url` property points to the `.crx` file of your extension in the Microsoft Edge Add-ons store.</span></span>  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="bcfdc-133">Wenn Sie eine Erweiterung aus dem Chrome Web Store installieren möchten, legen Sie den Wert auf `update_url` . `https://clients2.google.com/service/update2/crx`</span><span class="sxs-lookup"><span data-stu-id="bcfdc-133">If you want to install an extension from the Chrome Web Store, set the value of `update_url` to `https://clients2.google.com/service/update2/crx`.</span></span>  
  
1.  <span data-ttu-id="bcfdc-134">Stellen Sie sicher, dass Ihre Erweiterung in Microsoft Edge aufgeführt ist, indem Sie zu `edge://extensions` navigieren.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-134">Verify that your extension is listed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="bcfdc-135">Verwenden einer bevorzugten JSON-Datei (macOS und Linux)</span><span class="sxs-lookup"><span data-stu-id="bcfdc-135">Use a preferences JSON file (macOS and Linux)</span></span>  

<span data-ttu-id="bcfdc-136">Führen Sie die folgenden Schritte aus, um Ihre Erweiterung mithilfe einer bevorzugten JSON-Datei zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-136">To distribute your extension using a preferences JSON file, perform the following steps.</span></span>

1.  <span data-ttu-id="bcfdc-137">Stellen Sie bei Verwendung von Linux sicher, dass Ihre Erweiterungsdatei auf dem Computer verfügbar ist, auf dem die `.crx` Erweiterung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-137">When using Linux, ensure your `.crx` extension file is available on the machine that the extension will be installed on.</span></span> <span data-ttu-id="bcfdc-138">Kopieren Sie die Erweiterungsdatei in ein lokales Verzeichnis, oder verwenden Sie eine `.crx` Netzwerkfreigabe, die vom Computer aus erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-138">Copy the `.crx` extension file to a local directory, or use a  network share that is reachable from the machine.</span></span> 
1.  <span data-ttu-id="bcfdc-139">Erstellen Sie eine JSON-Datei, in der der Name der Datei der ID Ihrer Erweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-139">Create a JSON file where the name of the file corresponds to the ID of your extension.</span></span> <span data-ttu-id="bcfdc-140">Erstellen Sie beispielsweise eine JSON-Datei mit dem `aaaaaaaaaabbbbbbbbbbcccccccccc.json` Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-140">For example, create a JSON file with the file name `aaaaaaaaaabbbbbbbbbbcccccccccc.json`.</span></span>  
1.  <span data-ttu-id="bcfdc-141">Speichern Sie die JSON-Datei je nach Betriebssystem in einem der folgenden Ordner.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-141">Depending on your operating system, save the JSON file to one of the following folders.</span></span>   
    *   **<span data-ttu-id="bcfdc-142">macOS</span><span class="sxs-lookup"><span data-stu-id="bcfdc-142">macOS</span></span>**  
        *   <span data-ttu-id="bcfdc-143">Benutzerspezifisch:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-143">User specific:</span></span> `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   <span data-ttu-id="bcfdc-144">Alle Benutzer:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-144">All users:</span></span> `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        <span data-ttu-id="bcfdc-145">Um zu verhindern, dass nicht autorisierte Benutzer Erweiterungen für alle Benutzer installieren, stellen Sie sicher, dass die Erweiterungsdatei schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-145">To prevent unauthorized users from installing extensions for all users, ensure your extension file is read only.</span></span> <span data-ttu-id="bcfdc-146">Stellen Sie außerdem sicher, dass die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-146">Additionally, ensure that the following conditions are met:</span></span>
        
        *   <span data-ttu-id="bcfdc-147">Jedes Verzeichnis im Pfad befindet sich im Besitz des Benutzerstamms.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-147">Every directory in the path is owned by the user root.</span></span>  
        *   <span data-ttu-id="bcfdc-148">Jedes Verzeichnis im Pfad wird der oder der `admin` Gruppe `wheel` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-148">Every directory in the path is assigned to the `admin` or `wheel` group.</span></span>  
        *   <span data-ttu-id="bcfdc-149">Jedes Verzeichnis im Pfad ist nicht weltschreibbar.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-149">Every directory in the path isn't world writable.</span></span>  
        *   <span data-ttu-id="bcfdc-150">Der Pfad muss auch frei von symbolischen Verknüpfungen sein.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-150">The path must also be free of symbolic links.</span></span>  
        
    *   **<span data-ttu-id="bcfdc-151">Linux</span><span class="sxs-lookup"><span data-stu-id="bcfdc-151">Linux</span></span>**  
        *   <span data-ttu-id="bcfdc-152">Benutzerspezifisch:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-152">User specific:</span></span> `~/.config/microsoft-edge/External Extensions/`  
        *   <span data-ttu-id="bcfdc-153">Alle Benutzer:</span><span class="sxs-lookup"><span data-stu-id="bcfdc-153">All users:</span></span> `/usr/share/microsoft-edge/extensions/`  
1.  <span data-ttu-id="bcfdc-154">Kopieren Sie je nach Szenario den entsprechenden Code, der in Ihre JSON-Datei folgt.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-154">Depending on your scenario, copy the appropriate code that follows to your JSON file.</span></span> 
    *   <span data-ttu-id="bcfdc-155">Gilt nur für Linux.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-155">Applies to Linux only.</span></span> <span data-ttu-id="bcfdc-156">Wenn Sie die Installation über eine Datei installieren, geben Sie den Speicherort und die Version mit `external_crx` und `external_version` an.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-156">If you install from a file, specify the location and version using `external_crx` and `external_version`.</span></span>  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   <span data-ttu-id="bcfdc-157">Gilt für macOS und Linux.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-157">Applies to macOS and Linux.</span></span> <span data-ttu-id="bcfdc-158">Wenn Sie eine Installation von einem `update_URL` installieren, geben Sie die Update-URL mithilfe von `external_update_url` an.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-158">If you install from an `update_URL`, specify the update URL using `external_update_url`.</span></span> 
        
        <span data-ttu-id="bcfdc-159">Kopieren Sie den folgenden Code in Ihre JSON-Datei, wenn Sie nur aus lokalen `.crx` Dateien unter Linux installieren.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-159">Copy the following code to your JSON file when installing from local `.crx` files on Linux only.</span></span>  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  <span data-ttu-id="bcfdc-160">Kopieren Sie den folgenden Code bei der Installation aus dem Microsoft Edge-Add-Ons-Store unter macOS und Linux in Ihre JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-160">Copy the following code to your JSON file when installing from the Microsoft Edge Add-ons store on macOS and Linux.</span></span>
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  <span data-ttu-id="bcfdc-161">Um Erweiterungen für bestimmte Locales zu installieren, listen Sie die unterstützten Locales mithilfe `supported_locale` auf.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-161">To install extensions for specific locales, list the supported locales using `supported_locale`.</span></span>  <span data-ttu-id="bcfdc-162">Sie können auch übergeordnete Locales angeben, um die Erweiterung für alle Sprach-Locales zu installieren, die dieses übergeordnete Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-162">You may also specify parent locales to install your extension for all language locales that use that parent.</span></span> <span data-ttu-id="bcfdc-163">Wenn Sie beispielsweise das übergeordnete Locale verwenden, wird ihre Erweiterung für alle englischen Locales installiert, z. B. `en` `en-US` , und so `en-GB` weiter.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-163">For example, when using the parent locale `en`, your extension installs for all English locales, such as `en-US`, `en-GB`, and so on.</span></span>  <span data-ttu-id="bcfdc-164">Wenn Benutzer ihr Locale in ihrem Browser ändern, werden extern installierte Erweiterungen deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-164">When users change their locale in their browser, externally installed extensions are uninstalled.</span></span>  <span data-ttu-id="bcfdc-165">Verwenden Sie zum Installieren der Erweiterung für ein beliebiges Locale nicht `supported_locales` .</span><span class="sxs-lookup"><span data-stu-id="bcfdc-165">To install your extension for any locale, do not use `supported_locales`.</span></span>  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  <span data-ttu-id="bcfdc-166">Stellen Sie sicher, dass Ihre Erweiterung in Microsoft Edge installiert ist, indem Sie zu `edge://extensions` navigieren.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-166">Verify that your extension is installed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="bcfdc-167">Aktualisieren und Deinstallieren extern installierter Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="bcfdc-167">Update and uninstall externally installed extensions</span></span>

<span data-ttu-id="bcfdc-168">Microsoft Edge überprüft die Metadateneinträge in der Registrierung jedes Mal, wenn der Browser gestartet wird, und nimmt änderungen an den extern installierten Erweiterungen vor.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-168">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any changes to the externally installed extensions.</span></span>  

<span data-ttu-id="bcfdc-169">Um Ihre Erweiterung auf eine neue Version zu aktualisieren, aktualisieren Sie die Version in der Manifestdatei, und aktualisieren Sie dann die Version in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-169">To update your extension to a new version, update the version in the manifest file, and then update the version in the registry.</span></span>  

<span data-ttu-id="bcfdc-170">Möglicherweise müssen Sie extern installierte Erweiterungen deinstallieren, die als Teil eines Softwarepakets installiert wurden, das zuvor auf dem Computer installiert war.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-170">You may need to uninstall externally installed extensions, which were installed as part of a bundle of software that was previously installed on the machine.</span></span>  <span data-ttu-id="bcfdc-171">Um Ihre Erweiterung zu deinstallieren, entfernen Sie Ihre bevorzugten JSON-Dateien, oder entfernen Sie den Schlüssel aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-171">To uninstall your extension, remove your preferences JSON file or remove the key from the registry.</span></span>   

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="bcfdc-172">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcfdc-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  <span data-ttu-id="bcfdc-173">Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/apps/external_extensions)</span><span class="sxs-lookup"><span data-stu-id="bcfdc-173">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="bcfdc-175">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bcfdc-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
