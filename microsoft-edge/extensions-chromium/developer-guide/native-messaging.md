---
description: Unterschiede im nativen Messaging aus der Chrome-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567514"
---
# <span data-ttu-id="facc5-104">Systemeigenes Messaging</span><span class="sxs-lookup"><span data-stu-id="facc5-104">Native Messaging</span></span>  

<span data-ttu-id="facc5-105">Microsoft Edge ermöglicht jetzt die Erweiterung, die über den Microsoft Edge Addons-Katalog \ (Microsoft Edge Addons \) installiert wurde, um Nachrichten mit einer systemeigenen Anwendung mithilfe von Nachrichtenübergabe-APIs auszutauschen.</span><span class="sxs-lookup"><span data-stu-id="facc5-105">Microsoft Edge now allows Extension installed from Microsoft Edge Addons catalog \(Microsoft Edge Addons\) to exchange messages with a native application using message passing APIs.</span></span>  <span data-ttu-id="facc5-106">Wenn Sie das Feature aktivieren möchten, müssen Sie beim Implementieren des systemeigenen Messaginghosts ihrer systemeigenen Anwendung sicherstellen, dass Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="facc5-106">To enable the feature, you need to make sure of following things while implementing native messaging host of your Native Application.</span></span>  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  <span data-ttu-id="facc5-107">**Systemeigener Messaging-Host**:</span><span class="sxs-lookup"><span data-stu-id="facc5-107">**Native messaging host**:</span></span>  
    
    <span data-ttu-id="facc5-108">Um einen systemeigenen Messaging-Host zu registrieren, muss die Anwendung eine Manifestdatei installieren, die die systemeigene Messaginghost Konfiguration definiert.</span><span class="sxs-lookup"><span data-stu-id="facc5-108">In order to register a native messaging host the application must install a manifest file that defines the native messaging host configuration.</span></span>  <span data-ttu-id="facc5-109">Nachfolgend finden Sie ein Beispiel für die Manifestdatei:</span><span class="sxs-lookup"><span data-stu-id="facc5-109">Below is an example of the manifest file:</span></span>  
    
    ```xml
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
    
<span data-ttu-id="facc5-110">Die systemeigene Messaging-Host Manifestdatei muss ein gültiges JSON-Dokument sein und die folgenden Felder enthalten:</span><span class="sxs-lookup"><span data-stu-id="facc5-110">The native messaging host manifest file must be valid JSON and contains the following fields:</span></span>  

| <span data-ttu-id="facc5-111">Name</span><span class="sxs-lookup"><span data-stu-id="facc5-111">Name</span></span> | <span data-ttu-id="facc5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="facc5-112">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="facc5-113">Der Name des systemeigenen Messaginghosts.</span><span class="sxs-lookup"><span data-stu-id="facc5-113">Name of the native messaging host.</span></span> <span data-ttu-id="facc5-114">Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="facc5-114">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="facc5-115">Dieser Name darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="facc5-115">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="facc5-116">Der Name darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen.</span><span class="sxs-lookup"><span data-stu-id="facc5-116">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="facc5-117">Kurze Anwendungsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="facc5-117">Short application description.</span></span> |  
| `path` | <span data-ttu-id="facc5-118">Der Pfad zur nativen Messaging-Host-Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="facc5-118">Path to the native messaging host binary.</span></span>  <span data-ttu-id="facc5-119">Unter Windows kann der Pfad relativ zu dem Verzeichnis sein, in dem sich die Manifestdatei befindet.</span><span class="sxs-lookup"><span data-stu-id="facc5-119">On Windows, the path may be relative to the directory in which the manifest file is located.</span></span>  <span data-ttu-id="facc5-120">Unter macOS muss der Pfad absolut sein.</span><span class="sxs-lookup"><span data-stu-id="facc5-120">On macOS, the path must be absolute.</span></span>  <span data-ttu-id="facc5-121">Der Hostprozess wird gestartet, wobei das aktuelle Verzeichnis auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="facc5-121">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="facc5-122">Wenn dieser Parameter beispielsweise auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="facc5-122">For example if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="facc5-123">Der Typ der Schnittstelle, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="facc5-123">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="facc5-124">Derzeit gibt es nur einen möglichen Wert für diesen Parameter: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="facc5-124">Currently there is only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="facc5-125">Dieser Wert gibt an, dass Chrome verwenden `stdin` und `stdout` mit dem Host kommunizieren soll.</span><span class="sxs-lookup"><span data-stu-id="facc5-125">This value indicates that Chrome should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="facc5-126">Liste der Erweiterung, die auf den systemeigenen Messaging-Host zugreifen soll</span><span class="sxs-lookup"><span data-stu-id="facc5-126">list of Extension that should access to the native messaging host.</span></span>  <span data-ttu-id="facc5-127">Damit Ihre systemeigene Anwendung die Microsoft Edge Addons-Erweiterung identifizieren und kommunizieren kann, legen Sie Sie `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` in ihrer systemeigenen Messaging-Host Manifestdatei auf fest.</span><span class="sxs-lookup"><span data-stu-id="facc5-127">To enable your Native Application identify and communicate with Microsoft Edge Addons Extension, set `allowedorigins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  

1.  **<span data-ttu-id="facc5-128">Systemeigener Messaging-Hostspeicherort</span><span class="sxs-lookup"><span data-stu-id="facc5-128">Native messaging host location</span></span>**  
    
    <span data-ttu-id="facc5-129">Der Speicherort der Manifestdatei hängt von der Plattform ab.</span><span class="sxs-lookup"><span data-stu-id="facc5-129">The location of the manifest file depends on the platform.</span></span>  
    
    <span data-ttu-id="facc5-130">Unter Windows kann sich die Manifestdatei an einer beliebigen Stelle im Dateisystem befinden.</span><span class="sxs-lookup"><span data-stu-id="facc5-130">On Windows, the manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="facc5-131">Das Anwendungs Installationsprogramm muss Registrierungsschlüssel erstellen</span><span class="sxs-lookup"><span data-stu-id="facc5-131">The application installer must create registry key</span></span>  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="facc5-132">oder</span><span class="sxs-lookup"><span data-stu-id="facc5-132">or</span></span>  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="facc5-133">,</span><span class="sxs-lookup"><span data-stu-id="facc5-133">,</span></span>  
    
    <span data-ttu-id="facc5-134">und legen Sie den Standardwert für diesen Schlüssel auf den vollständigen Pfad zur Manifestdatei fest.</span><span class="sxs-lookup"><span data-stu-id="facc5-134">and set default value of that key to the full path to the manifest file.</span></span>  <span data-ttu-id="facc5-135">Verwenden Sie beispielsweise den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="facc5-135">For example, using the following command:</span></span>  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    <span data-ttu-id="facc5-136">oder verwenden Sie die folgende REG-Datei:</span><span class="sxs-lookup"><span data-stu-id="facc5-136">or using the following .reg file:</span></span>  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    <span data-ttu-id="facc5-137">Wenn Microsoft Edge nach systemeigenen Messaginghosts sucht, wird zuerst die 32-Bit-Registrierung abgefragt, dann die 64-Bit-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="facc5-137">When Microsoft Edge looks for native messaging hosts, the 32-bit registry is queried first, then the 64-bit registry.</span></span>  

<span data-ttu-id="facc5-138">Unter macOS werden die systemweiten systemeigenen Messaginghosts an einem festen Speicherort nachgeschlagen, während die nativen Messaginghosts auf Benutzerebene in einem Unterverzeichnis im Benutzerprofilverzeichnis nachgeschlagen werden `NativeMessagingHosts` .</span><span class="sxs-lookup"><span data-stu-id="facc5-138">On macOS, the system-wide native messaging hosts are looked up at a fixed location, while the user-level native messaging hosts are looked up in a subdirectory within the user profile directory called `NativeMessagingHosts`.</span></span>  

<span data-ttu-id="facc5-139">Microsoft Edge unter macOS \ (systemweit \):</span><span class="sxs-lookup"><span data-stu-id="facc5-139">Microsoft Edge on macOS \(system-wide\) :</span></span>  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

<span data-ttu-id="facc5-140">Microsoft Edge unter macOS \ (benutzerspezifischer Standardpfad \):</span><span class="sxs-lookup"><span data-stu-id="facc5-140">Microsoft Edge on macOS \(user-specific, default path\):</span></span>  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` <span data-ttu-id="facc5-141">kann Canary, dev oder Beta sein.</span><span class="sxs-lookup"><span data-stu-id="facc5-141">may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="facc5-142">Für stable-Kanal `Microsoft Edge` sollte nur verwendet werden, `<ChannelName`>"ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="facc5-142">For stable channel, only `Microsoft Edge` should be used, `<ChannelName`>\` is not required.</span></span>

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="facc5-143">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="facc5-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="facc5-144">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="facc5-144">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="facc5-146">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="facc5-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
