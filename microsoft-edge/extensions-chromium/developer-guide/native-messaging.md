---
description: Systemeigene Messaging-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088555"
---
# <span data-ttu-id="4aea6-104">Systemeigenes Messaging</span><span class="sxs-lookup"><span data-stu-id="4aea6-104">Native messaging</span></span>  

<span data-ttu-id="4aea6-105">Erweiterungen können mit einer nativen Win32-Anwendung kommunizieren, die auf dem Gerät eines Benutzers mithilfe von Nachrichtenübergabe-APIs installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4aea6-105">Extensions can communicate with a native Win32 application installed on a user’s device using message passing APIs.</span></span> <span data-ttu-id="4aea6-106">Der systemeigene Anwendungshost kann Nachrichten mit Erweiterungen mit Standardeingabe und Standardausgabe senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-106">The native application host can send and receive messages with extensions using standard input and standard output.</span></span> <span data-ttu-id="4aea6-107">Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge ähnlich wie bei jeder anderen Erweiterung installiert.</span><span class="sxs-lookup"><span data-stu-id="4aea6-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span> <span data-ttu-id="4aea6-108">Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4aea6-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>

<span data-ttu-id="4aea6-109">Um die Erweiterung und den systemeigenen Anwendungshost zu erwerben, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="4aea6-109">To acquire the extension and native application host, you can:</span></span>

1. <span data-ttu-id="4aea6-110">Verpacken Sie die Erweiterung und den Host zusammen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-110">Package the extension and the host together.</span></span> <span data-ttu-id="4aea6-111">Wenn Benutzer das Paket installieren, werden sowohl die Erweiterung als auch der Host installiert.</span><span class="sxs-lookup"><span data-stu-id="4aea6-111">When users install the package, both the extension and the host are installed.</span></span>
1. <span data-ttu-id="4aea6-112">Installieren Sie die Erweiterung aus dem [Microsoft Edge-Add-ons-Store][EdgeAddons], und bitten Sie Ihre Durchwahl Benutzer, den Host zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4aea6-112">Install the extension from the [Microsoft Edge Add-ons store][EdgeAddons], and have your extension prompt users to install the host.</span></span> 

<span data-ttu-id="4aea6-113">Führen Sie die folgenden Schritte aus, um Ihre Erweiterung zum Senden und empfangen von Nachrichten mit systemeigenen Anwendungshosts einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4aea6-113">Refer to the steps below to setup your extension to send and receive messages with native application hosts.</span></span>

### <span data-ttu-id="4aea6-114">Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungs Manifest</span><span class="sxs-lookup"><span data-stu-id="4aea6-114">Step 1: Add permissions to the extension manifest</span></span>

<span data-ttu-id="4aea6-115">Fügen Sie die nativeMessaging-Berechtigung für die Datei **manifest.js** der Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="4aea6-115">Add the nativeMessaging permission to the extension’s **manifest.json** file.</span></span> <span data-ttu-id="4aea6-116">Nachfolgend finden Sie ein Beispiel für manifest.jsauf:</span><span class="sxs-lookup"><span data-stu-id="4aea6-116">Below is an example of manifest.json:</span></span>

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### <span data-ttu-id="4aea6-117">Schritt 2: Erstellen einer systemeigenen Messaging-Host Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="4aea6-117">Step 2: Create your native messaging host manifest file</span></span>
    
<span data-ttu-id="4aea6-118">Systemeigene Anwendungen müssen eine systemeigene Messaging-Host Manifestdatei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-118">Native applications must provide a native messaging host manifest file.</span></span> <span data-ttu-id="4aea6-119">Diese Manifestdatei enthält den Pfad zur ausführbaren systemeigenen Messaginghost-Datei, die Methode der Kommunikation mit der Erweiterung und eine Liste der zulässigen Erweiterungen, mit denen Sie kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="4aea6-119">This manifest file contains the path to the native messaging host executable, the method of communication with the extension, and a list of allowed extensions it can communicate with.</span></span> <span data-ttu-id="4aea6-120">Browser lesen und überprüfen das systemeigene Messaging-Host Manifest, werden aber nie vom Browser installiert oder verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4aea6-120">Browsers read and validate the native messaging host manifest, but it’s never installed or managed by the browser.</span></span> <span data-ttu-id="4aea6-121">Die Host Manifestdatei muss eine gültige JSON-Datei mit den folgenden Feldern sein.</span><span class="sxs-lookup"><span data-stu-id="4aea6-121">The host manifest file must be a valid json file containing the following fields.</span></span>

    
```json
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
```  




| <span data-ttu-id="4aea6-122">Name</span><span class="sxs-lookup"><span data-stu-id="4aea6-122">Name</span></span> | <span data-ttu-id="4aea6-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aea6-123">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="4aea6-124">Der Name des systemeigenen Messaginghosts.</span><span class="sxs-lookup"><span data-stu-id="4aea6-124">Name of the native messaging host.</span></span> <span data-ttu-id="4aea6-125">Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="4aea6-125">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="4aea6-126">Dieser Name darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="4aea6-126">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="4aea6-127">Der Name darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-127">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="4aea6-128">Kurze Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4aea6-128">Brief description of the application.</span></span> |  
| `path` | <span data-ttu-id="4aea6-129">Der Pfad zur nativen Messaging-Host-Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="4aea6-129">Path to the native messaging host binary.</span></span> <span data-ttu-id="4aea6-130">Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="4aea6-130">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span> <span data-ttu-id="4aea6-131">Unter macOS und Linux muss der Pfad absolut sein.</span><span class="sxs-lookup"><span data-stu-id="4aea6-131">On macOS and Linux, the path must be absolute.</span></span> <span data-ttu-id="4aea6-132">Der Hostprozess wird gestartet, wobei das aktuelle Verzeichnis auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="4aea6-132">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="4aea6-133">Wenn dieser Parameter beispielsweise auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="4aea6-133">For example, if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="4aea6-134">Der Typ der Schnittstelle, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aea6-134">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="4aea6-135">Derzeit gibt es nur einen möglichen Wert für diesen Parameter: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="4aea6-135">Currently there's only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="4aea6-136">Dieser Wert gibt an, dass Microsoft Edge `stdin` `stdout` die Kommunikation mit dem Host verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4aea6-136">This value indicates that Microsoft Edge should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="4aea6-137">Liste der Erweiterungen, die möglicherweise auf den systemeigenen Messaging-Host zugreifen können</span><span class="sxs-lookup"><span data-stu-id="4aea6-137">List of extensions that may have access to the native messaging host.</span></span>  <span data-ttu-id="4aea6-138">Damit Ihre Anwendung eine Erweiterung identifizieren und mit Ihnen kommunizieren kann, legen Sie Sie `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf fest.</span><span class="sxs-lookup"><span data-stu-id="4aea6-138">To enable your application to identify and communicate with an extension, set `allowed_origins` to `chrome-extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  


<span data-ttu-id="4aea6-139">Während der Entwicklung können Sie Ihre Erweiterung querladen, um systemeigene Nachrichten mit dem Host zu testen, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="4aea6-139">While developing, you can sideload your extension to test native messaging with the host by:</span></span>
1. <span data-ttu-id="4aea6-140">Navigieren Sie zu `edge://extensions` , und aktivieren Sie dann die Umschaltfläche des Entwicklermodus.</span><span class="sxs-lookup"><span data-stu-id="4aea6-140">Navigating to `edge://extensions`, and then turning on the Developer mode toggle button.</span></span> 
1. <span data-ttu-id="4aea6-141">Wählen Sie laden entpackt aus, und wählen Sie dann Ihr Erweiterungspaket für querladen aus.</span><span class="sxs-lookup"><span data-stu-id="4aea6-141">Choose Load unpacked, and then select your extension package to sideload.</span></span>  
1. <span data-ttu-id="4aea6-142">Wählen Sie „OK“.</span><span class="sxs-lookup"><span data-stu-id="4aea6-142">Choose OK.</span></span>
1. <span data-ttu-id="4aea6-143">Überprüfen Sie, ob auf der `edge://extensions` Seite jetzt Ihre Erweiterung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="4aea6-143">Verify the `edge://extensions` page now lists your extension.</span></span> 
1. <span data-ttu-id="4aea6-144">Kopieren Sie den Schlüssel aus der ID aus dem Erweiterungs Eintrag auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="4aea6-144">Copy the key from ID from the extension listing on the page.</span></span>

<span data-ttu-id="4aea6-145">Wenn Sie bereit sind, ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-ons-Store.</span><span class="sxs-lookup"><span data-stu-id="4aea6-145">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="4aea6-146">Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Sideloading ihrer Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aea6-146">The extension ID of the published extension may be different to the ID used while sideloading your extension.</span></span> <span data-ttu-id="4aea6-147">Wenn die ID geändert wurde, aktualisieren `allowed_origins` Sie in der Host Manifestdatei die ID der veröffentlichten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4aea6-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span> 



### <span data-ttu-id="4aea6-148">Schritt 3: Kopieren der systemeigenen Messaging-Host Manifestdatei auf Ihr System</span><span class="sxs-lookup"><span data-stu-id="4aea6-148">Step 3: Copy the native messaging host manifest file to your system</span></span>

<span data-ttu-id="4aea6-149">Der letzte Schritt besteht darin, die systemeigene Messaging-Host Manifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass Sie ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="4aea6-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it’s configured correctly.</span></span> <span data-ttu-id="4aea6-150">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die systemeigene Messaging-Host Datei am erwarteten Ort abgelegt wird, da Sie je nach Plattform variiert.</span><span class="sxs-lookup"><span data-stu-id="4aea6-150">Follow the steps below to ensure the native messaging host file is placed in the expected location because it varies by platform.</span></span>
    
<span data-ttu-id="4aea6-151">**Windows**.</span><span class="sxs-lookup"><span data-stu-id="4aea6-151">**Windows**.</span></span> <span data-ttu-id="4aea6-152">Die Manifestdatei befindet sich möglicherweise an einer beliebigen Stelle im Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="4aea6-152">The manifest file may be located anywhere in the file system.</span></span> <span data-ttu-id="4aea6-153">Das Anwendungs Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für diesen Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-153">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span> <span data-ttu-id="4aea6-154">Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="4aea6-154">The following commands are examples of registry keys.</span></span>
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="4aea6-155">oder</span><span class="sxs-lookup"><span data-stu-id="4aea6-155">or</span></span>  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="4aea6-156">,</span><span class="sxs-lookup"><span data-stu-id="4aea6-156">,</span></span>  
    
<span data-ttu-id="4aea6-157">Führen Sie an einer Eingabeaufforderung den folgenden Befehl aus, um dem Ordner mit der Manifestdatei einen Registrierungsschlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-157">Run the following command at a command prompt to add a registry key to the folder with the manifest file.</span></span>
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
<span data-ttu-id="4aea6-158">Alternativ können Sie den folgenden Befehl in eine REG-Datei kopieren und ausführen, um den Registrierungsschlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-158">Alternatively, copy the following command to a .reg file and run it to add the registry key.</span></span> 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  <span data-ttu-id="4aea6-159">Microsoft Edge fragt zuerst die 32-Bit-Registrierung und dann die 64-Bit-Registrierung ab, um systemeigene Messaginghosts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4aea6-159">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span> <span data-ttu-id="4aea6-160">Wenn Sie die obige reg-Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie Sie über eine Eingabeaufforderung des Administrators ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aea6-160">If you run the above .reg file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>


<span data-ttu-id="4aea6-161">**Mac OS**.</span><span class="sxs-lookup"><span data-stu-id="4aea6-161">**macOS**.</span></span> <span data-ttu-id="4aea6-162">Die Manifestdatei muss wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="4aea6-162">The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="4aea6-163">Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4aea6-163">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span> <span data-ttu-id="4aea6-164">Beispielsweise muss die Manifestdatei in gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4aea6-164">For example, the manifest file must be stored in</span></span> `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. <span data-ttu-id="4aea6-165">Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im NativeMessagingHosts-Unterverzeichnis im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4aea6-165">User-specific native messaging hosts, which are available to the current user only, are located in the NativeMessagingHosts  subdirectory in the user profile directory.</span></span> <span data-ttu-id="4aea6-166">Beispielsweise muss die Manifestdatei in gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4aea6-166">For example, the manifest file must be stored in</span></span>  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    <span data-ttu-id="4aea6-167">dabei `ChannelName` kann es sich um Canary, dev oder Beta handeln.</span><span class="sxs-lookup"><span data-stu-id="4aea6-167">where `ChannelName` may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="4aea6-168">Bei Verwendung des stable-Kanals `ChannelName` ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4aea6-168">When using the Stable channel, `ChannelName` isn't required.</span></span>


<span data-ttu-id="4aea6-169">**Linux** Die Manifestdatei muss wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="4aea6-169">**Linux** The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="4aea6-170">Systemweite systemeigene Messaginghosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span><span class="sxs-lookup"><span data-stu-id="4aea6-170">System-wide native messaging hosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span></span>

1. <span data-ttu-id="4aea6-171">Benutzerspezifische systemeigene Messaginghosts:  `/etc/opt/edge/native-messaging-hosts`</span><span class="sxs-lookup"><span data-stu-id="4aea6-171">User-specific native messaging hosts:  `/etc/opt/edge/native-messaging-hosts`</span></span>


> [!NOTE]
> <span data-ttu-id="4aea6-172">Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei angeben, und führen Sie Berechtigungen für die ausführbare Host-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="4aea6-172">Ensure that you provide read permissions on the manifest file, and execute permissions on the host executable.</span></span>


> [!NOTE]
> <span data-ttu-id="4aea6-173">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aea6-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4aea6-174">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="4aea6-174">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4aea6-176">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4aea6-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-ons"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
