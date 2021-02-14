---
description: Systemeigene Messagingdokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 2d629762d4c7c75832905cfbf8c2d5311191092d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327701"
---
# <span data-ttu-id="dc384-104">Systemeigenes Messaging</span><span class="sxs-lookup"><span data-stu-id="dc384-104">Native messaging</span></span>  

<span data-ttu-id="dc384-105">Erweiterungen kommunizieren mit einer systemeigenen Win32-Anwendung, die auf dem Gerät eines Benutzers installiert ist, und verwenden APIs zum Übergeben von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dc384-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="dc384-106">Der systemeigene Anwendungshost sendet und empfängt Nachrichten mit Erweiterungen mithilfe von Standardeingabe und Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="dc384-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="dc384-107">Erweiterungen, die natives Messaging verwenden, werden in Microsoft Edge ähnlich wie jede andere Erweiterung installiert.</span><span class="sxs-lookup"><span data-stu-id="dc384-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="dc384-108">Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dc384-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="dc384-109">Um die Erweiterung und den systemeigenen Anwendungshost zu erwerben, verfügen Sie über zwei Verteilungsmodelle.</span><span class="sxs-lookup"><span data-stu-id="dc384-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="dc384-110">Packen Sie Ihre Erweiterung und den Host zusammen.</span><span class="sxs-lookup"><span data-stu-id="dc384-110">Package your extension and the host together.</span></span>  <span data-ttu-id="dc384-111">Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.</span><span class="sxs-lookup"><span data-stu-id="dc384-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="dc384-112">Installieren Sie Ihre Erweiterung mithilfe des [Microsoft Edge-Add-Ons-Speichers,] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]und Die Benutzer werden aufgefordert, den Host zu installieren.</span><span class="sxs-lookup"><span data-stu-id="dc384-112">Install your extension using the [Microsoft Edge Add-ons store] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="dc384-113">Informationen zum Erstellen Ihrer Erweiterung zum Senden und Empfangen von Nachrichten mit systemeigenen Anwendungshosts finden Sie in den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="dc384-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="dc384-114">Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungsmanifest</span><span class="sxs-lookup"><span data-stu-id="dc384-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="dc384-115">Fügen Sie `nativeMessaging` die Berechtigung zummanifest.js\*\* datei\*\* der Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc384-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="dc384-116">Der folgende Codeausschnitt ist ein Beispiel für **manifest.jsauf**.</span><span class="sxs-lookup"><span data-stu-id="dc384-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="dc384-117">Schritt 2: Erstellen der systemeigenen Messaginghostmanifestdatei</span><span class="sxs-lookup"><span data-stu-id="dc384-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="dc384-118">Systemeigene Anwendungen müssen eine systemeigene Messaginghostmanifestdatei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dc384-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="dc384-119">Die Manifestdatei enthält die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="dc384-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="dc384-120">Der Pfad zur nativen Messaginghostlaufzeit.</span><span class="sxs-lookup"><span data-stu-id="dc384-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="dc384-121">Die Methode der Kommunikation mit der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dc384-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="dc384-122">Eine Liste der zulässigen Erweiterungen, mit denen kommuniziert wird.</span><span class="sxs-lookup"><span data-stu-id="dc384-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="dc384-123">Der Browser liest und überprüft das systemeigene Messaginghostmanifest.</span><span class="sxs-lookup"><span data-stu-id="dc384-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="dc384-124">Der Browser installiert oder verwaltet die systemeigene Messaginghostmanifestdatei nicht.</span><span class="sxs-lookup"><span data-stu-id="dc384-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="dc384-125">Die Hostmanifestdatei muss eine gültige JSON-Datei sein, die die folgenden Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="dc384-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc384-126">Gibt den Namen des systemeigenen Messaginghosts an.</span><span class="sxs-lookup"><span data-stu-id="dc384-126">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="dc384-127">Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="dc384-127">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="dc384-128">Dieser Wert darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc384-128">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="dc384-129">Dieser Wert darf nicht mit einem Punkt beginnen oder enden, und einem Punkt darf kein weiterer Punkt folgen.</span><span class="sxs-lookup"><span data-stu-id="dc384-129">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc384-130">Beschreibt die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dc384-130">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc384-131">Gibt den Pfad zur nativen Messaginghost-Binärdatei an.</span><span class="sxs-lookup"><span data-stu-id="dc384-131">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="dc384-132">Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="dc384-132">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="dc384-133">Unter macOS und Linux muss der Pfad absolut sein.</span><span class="sxs-lookup"><span data-stu-id="dc384-133">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="dc384-134">Der Hostprozess beginnt mit dem Verzeichnis, das die Host binär enthält, mit dem aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dc384-134">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="dc384-135">Wenn dieser Parameter beispielsweise auf \(Windows\) festgelegt ist, wird die Binärdatei mit dem aktuellen `C:\Application\nm_host.exe` Verzeichnis \( `C:\Application\` \) gestartet.</span><span class="sxs-lookup"><span data-stu-id="dc384-135">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc384-136">Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc384-136">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="dc384-137">Dieser Wert gibt Microsoft Edge an, den Host zu `stdin` verwenden und mit ihm zu `stdout` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="dc384-137">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="dc384-138">Der einzige zulässige Wert ist `stdio` .</span><span class="sxs-lookup"><span data-stu-id="dc384-138">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc384-139">Gibt die Liste der Erweiterungen an, die Zugriff auf den systemeigenen Messaginghost haben.</span><span class="sxs-lookup"><span data-stu-id="dc384-139">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="dc384-140">Damit Ihre Anwendung eine Erweiterung identifizieren und mit dieser kommunizieren kann, legen Sie in der systemeigenen Messaginghostmanifestdatei den folgenden Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc384-140">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="dc384-141">Laden Sie Ihre Erweiterung quer, um systemeigenes Messaging mit dem Host zu testen.</span><span class="sxs-lookup"><span data-stu-id="dc384-141">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="dc384-142">Führen Sie die folgenden Schritte aus, um die Erweiterung während der Entwicklung quer zu laden und `microsoft_catalog_extension_id` abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dc384-142">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="dc384-143">Navigieren Sie `edge://extensions` zu , und aktivieren Sie dann die Umschaltfläche für den Entwicklermodus.</span><span class="sxs-lookup"><span data-stu-id="dc384-143">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="dc384-144">Choose **Load unpacked**, and then select your extension package to sideload.</span><span class="sxs-lookup"><span data-stu-id="dc384-144">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="dc384-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc384-145">Choose **OK**.</span></span>  
1.  <span data-ttu-id="dc384-146">Navigieren Sie zu `edge://extensions` der Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="dc384-146">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="dc384-147">Kopieren Sie den Schlüssel von `microsoft_catalog_extension_id` \(ID\) aus dem Erweiterungseintrag auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="dc384-147">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  

<span data-ttu-id="dc384-148">Wenn Sie bereit sind, Ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Store.</span><span class="sxs-lookup"><span data-stu-id="dc384-148">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="dc384-149">Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Querladen der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc384-149">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="dc384-150">Wenn sich die ID geändert hat, aktualisieren Sie `allowed_origins` in der Hostmanifestdatei mit der ID Ihrer veröffentlichten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dc384-150">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="dc384-151">Schritt 3: Kopieren der systemeigenen Messaginghostmanifestdatei in Ihr System</span><span class="sxs-lookup"><span data-stu-id="dc384-151">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="dc384-152">Im letzten Schritt wird die systemeigene Messaginghostmanifestdatei auf Ihren Computer kopiert und sichergestellt, dass die Manifestdatei ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="dc384-152">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="dc384-153">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass sich die Manifestdatei am erwarteten Speicherort befindet.</span><span class="sxs-lookup"><span data-stu-id="dc384-153">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="dc384-154">Der Standort variiert je nach Plattform.</span><span class="sxs-lookup"><span data-stu-id="dc384-154">The location varies by platform.</span></span>  

### [<span data-ttu-id="dc384-155">Windows</span><span class="sxs-lookup"><span data-stu-id="dc384-155">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="dc384-156">Die Manifestdatei kann sich an einer beliebigen Stelle im Dateisystem befinden.</span><span class="sxs-lookup"><span data-stu-id="dc384-156">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="dc384-157">Das Anwendungsinstallationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für den Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc384-157">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="dc384-158">Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="dc384-158">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="dc384-159">So fügen Sie dem Verzeichnis mit dem Manifestschlüssel einen Registrierungsschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc384-159">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="dc384-160">Führen Sie den Befehl an der Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="dc384-160">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="dc384-161">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="dc384-161">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="dc384-162">Erstellen Sie `.reg` eine Datei, und führen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="dc384-162">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="dc384-163">Kopieren Sie den folgenden Befehl in eine `.reg` Datei.</span><span class="sxs-lookup"><span data-stu-id="dc384-163">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="dc384-164">Führen Sie die `.reg` Datei aus.</span><span class="sxs-lookup"><span data-stu-id="dc384-164">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="dc384-165">Microsoft Edge fragt den `HKEY_CURRENT_USER` Stammschlüssel ab, gefolgt von `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="dc384-165">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="dc384-166">In beiden Schlüsseln wird zuerst die 32-Bit-Registrierung durchsucht, und dann wird die 64-Bit-Registrierung durchsucht, um systemeigene Messaginghosts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dc384-166">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="dc384-167">Der Registrierungsschlüssel gibt den Speicherort des systemeigenen Messaginghostmanifests an.</span><span class="sxs-lookup"><span data-stu-id="dc384-167">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="dc384-168">Wenn Microsoft Edge den Registrierungsschlüssel an einem der zuvor aufgeführten Speicherorte findet, werden die in diesem Absatz aufgeführten Speicherorte nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="dc384-168">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in this paragraph.</span></span>  <span data-ttu-id="dc384-169">Wenn Sie die obige Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie sie über `.reg` eine Administratorbefehlsaufforderung ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc384-169">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="dc384-170">macOS</span><span class="sxs-lookup"><span data-stu-id="dc384-170">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="dc384-171">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dc384-171">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="dc384-172">Systemweite systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc384-172">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="dc384-173">Die Manifestdatei muss z. B. an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dc384-173">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="dc384-174">Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dc384-174">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="dc384-175">Die Manifestdatei muss z. B. an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dc384-175">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="dc384-176">Das  `{Channel_Name}` In muss einer der folgenden Werte `Microsoft Edge {Channel_Name}` sein.</span><span class="sxs-lookup"><span data-stu-id="dc384-176">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="dc384-177">Canary</span><span class="sxs-lookup"><span data-stu-id="dc384-177">Canary</span></span>  
    *   <span data-ttu-id="dc384-178">Dev</span><span class="sxs-lookup"><span data-stu-id="dc384-178">Dev</span></span>  
    *   <span data-ttu-id="dc384-179">Beta</span><span class="sxs-lookup"><span data-stu-id="dc384-179">Beta</span></span>  

    <span data-ttu-id="dc384-180">Bei Verwendung des `{Channel_Name}` Stable-Kanals ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc384-180">When using the Stable channel, `{Channel_Name}` isn't required.</span></span>  

### [<span data-ttu-id="dc384-181">Linux</span><span class="sxs-lookup"><span data-stu-id="dc384-181">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="dc384-182">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dc384-182">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="dc384-183">Systemweite systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc384-183">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="dc384-184">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dc384-184">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="dc384-185">Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dc384-185">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="dc384-186">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dc384-186">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="dc384-187">Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei bereitstellen und Berechtigungen für die Hostlaufzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc384-187">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-Ons"

> [!NOTE]
> <span data-ttu-id="dc384-189">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc384-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dc384-190">Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="dc384-190">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="dc384-192">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc384-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
