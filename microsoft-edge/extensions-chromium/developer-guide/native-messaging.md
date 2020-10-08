---
description: Systemeigene Messaging-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100252"
---
# <span data-ttu-id="796cc-104">Systemeigenes Messaging</span><span class="sxs-lookup"><span data-stu-id="796cc-104">Native messaging</span></span>  

<span data-ttu-id="796cc-105">Erweiterungen kommunizieren mit einer nativen Win32-Anwendung, die mithilfe von Nachrichtenübergabe-APIs auf dem Gerät eines Benutzers installiert ist.</span><span class="sxs-lookup"><span data-stu-id="796cc-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="796cc-106">Der systemeigene Anwendungshost sendet und empfängt Nachrichten mit Erweiterungen mit Standardeingabe und Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="796cc-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="796cc-107">Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge ähnlich wie bei jeder anderen Erweiterung installiert.</span><span class="sxs-lookup"><span data-stu-id="796cc-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="796cc-108">Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.</span><span class="sxs-lookup"><span data-stu-id="796cc-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="796cc-109">Sie verfügen über zwei Verteilungsmodelle, um die Erweiterung und den systemeigenen Anwendungshost zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="796cc-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="796cc-110">Verpacken Sie Ihre Erweiterung und den Host zusammen.</span><span class="sxs-lookup"><span data-stu-id="796cc-110">Package your extension and the host together.</span></span>  <span data-ttu-id="796cc-111">Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.</span><span class="sxs-lookup"><span data-stu-id="796cc-111">When a user installs the package, both the extension and the host are installed.</span></span>
*   <span data-ttu-id="796cc-112">Installieren Sie Ihre Erweiterung mit dem [Microsoft Edge-Add-on-Store][EdgeAddons], und ihre Erweiterung fordert die Benutzer auf, den Host zu installieren.</span><span class="sxs-lookup"><span data-stu-id="796cc-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="796cc-113">Wenn Sie Ihre Erweiterung zum Senden und empfangen von Nachrichten mit systemeigenen Anwendungshosts erstellen möchten, lesen Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="796cc-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="796cc-114">Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungs Manifest</span><span class="sxs-lookup"><span data-stu-id="796cc-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="796cc-115">Fügen Sie die `nativeMessaging` Berechtigung zum **manifest.js** Datei der Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="796cc-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="796cc-116">Der folgende Codeausschnitt ist ein Beispiel für **manifest.js**ein.</span><span class="sxs-lookup"><span data-stu-id="796cc-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="796cc-117">Schritt 2 – Erstellen einer systemeigenen Messaging-Host Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="796cc-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="796cc-118">Systemeigene Anwendungen müssen eine systemeigene Messaging-Host Manifestdatei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="796cc-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="796cc-119">Die Manifestdatei enthält den Pfad zur systemeigenen Messaging-Host Laufzeit, die Methode der Kommunikation mit der Erweiterung und eine Liste der zulässigen Erweiterungen, mit denen Sie kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="796cc-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span></span>  <span data-ttu-id="796cc-120">Der Browser liest und überprüft das systemeigene Messaging-Host Manifest.</span><span class="sxs-lookup"><span data-stu-id="796cc-120">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="796cc-121">Der Browser installiert oder verwaltet die systemeigene Messaging-Host Manifestdatei nicht.</span><span class="sxs-lookup"><span data-stu-id="796cc-121">The browser does not install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="796cc-122">Die Host Manifestdatei muss eine gültige JSON-Datei mit den folgenden Schlüsseln sein.</span><span class="sxs-lookup"><span data-stu-id="796cc-122">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="796cc-123">Gibt den Namen des systemeigenen Messaginghosts an.</span><span class="sxs-lookup"><span data-stu-id="796cc-123">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="796cc-124">Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="796cc-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="796cc-125">Dieser Wert darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="796cc-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="796cc-126">Dieser Wert darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen.</span><span class="sxs-lookup"><span data-stu-id="796cc-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="796cc-127">Beschreibt die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="796cc-127">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="796cc-128">Gibt den Pfad zur nativen Messaging-Host-Binärdatei an.</span><span class="sxs-lookup"><span data-stu-id="796cc-128">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="796cc-129">Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="796cc-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="796cc-130">Unter macOS und Linux muss der Pfad absolut sein.</span><span class="sxs-lookup"><span data-stu-id="796cc-130">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="796cc-131">Der Hostprozess beginnt mit dem aktuellen Verzeichnis, das auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="796cc-131">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="796cc-132">Beispiel: \ (Windows \), wenn dieser Parameter auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet \ ( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="796cc-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="796cc-133">Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="796cc-133">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="796cc-134">Dieser Wert weist Microsoft Edge an, zu verwenden `stdin` und `stdout` mit dem Host zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="796cc-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="796cc-135">Der einzige akzeptable Wert ist `stdio` .</span><span class="sxs-lookup"><span data-stu-id="796cc-135">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="796cc-136">Gibt die Liste der Erweiterungen an, die auf den systemeigenen Messaging-Host zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="796cc-136">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="796cc-137">Damit Ihre Anwendung eine Erweiterung erkennen und mit Ihnen kommunizieren kann, legen Sie in der systemeigenen Messaging-Host Manifestdatei den folgenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="796cc-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="796cc-138">Querladen Sie Ihre Erweiterung, um systemeigene Nachrichten mit dem Host zu testen.</span><span class="sxs-lookup"><span data-stu-id="796cc-138">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="796cc-139">`microsoft_catalog_extension_id`Führen Sie die folgenden Schritte aus, um die Erweiterung während der Entwicklung zu querladen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="796cc-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="796cc-140">Navigieren Sie zu `edge://extensions` , und aktivieren Sie dann die Umschaltfläche des Entwicklermodus.</span><span class="sxs-lookup"><span data-stu-id="796cc-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="796cc-141">Wählen Sie **Laden entpackt**aus, und wählen Sie dann Ihr Erweiterungspaket für querladen aus.</span><span class="sxs-lookup"><span data-stu-id="796cc-141">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="796cc-142">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="796cc-142">Choose **OK**.</span></span>
1.  <span data-ttu-id="796cc-143">Navigieren Sie zu `edge://extensions` Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="796cc-143">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="796cc-144">Kopieren Sie den Schlüssel von `microsoft_catalog_extension_id` \ (ID \) aus dem Erweiterungs Eintrag auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="796cc-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>

<span data-ttu-id="796cc-145">Wenn Sie bereit sind, ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-ons-Store.</span><span class="sxs-lookup"><span data-stu-id="796cc-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="796cc-146">Die Erweiterungs-ID der veröffentlichten Erweiterung kann von der beim Sideloading der Erweiterung verwendeten ID abweichen.</span><span class="sxs-lookup"><span data-stu-id="796cc-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="796cc-147">Wenn die ID geändert wurde, aktualisieren `allowed_origins` Sie in der Host Manifestdatei die ID der veröffentlichten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="796cc-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="796cc-148">Schritt 3 – Kopieren der systemeigenen Messaging-Host Manifestdatei auf Ihr System</span><span class="sxs-lookup"><span data-stu-id="796cc-148">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="796cc-149">Der letzte Schritt besteht darin, die systemeigene Messaging-Host Manifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass Sie ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="796cc-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span></span>  <span data-ttu-id="796cc-150">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihre Manifestdatei an dem erwarteten Ort abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="796cc-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="796cc-151">Der Standort variiert je nach Plattform.</span><span class="sxs-lookup"><span data-stu-id="796cc-151">The location varies by platform.</span></span>  

### [<span data-ttu-id="796cc-152">Windows</span><span class="sxs-lookup"><span data-stu-id="796cc-152">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="796cc-153">Die Manifestdatei befindet sich möglicherweise an einer beliebigen Stelle im Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="796cc-153">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="796cc-154">Das Anwendungs Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für diesen Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen.</span><span class="sxs-lookup"><span data-stu-id="796cc-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="796cc-155">Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="796cc-155">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="796cc-156">So fügen Sie dem Verzeichnis mit dem manifestschlüssel einen Registrierungsschlüssel hinzu</span><span class="sxs-lookup"><span data-stu-id="796cc-156">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="796cc-157">Befehl "ausführen" in der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="796cc-157">Run command in command prompt.</span></span>    
    
    1.  <span data-ttu-id="796cc-158">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="796cc-158">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="796cc-159">Erstellen `.reg` Sie eine Datei, und führen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="796cc-159">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="796cc-160">Kopieren Sie den folgenden Befehl in eine `.reg` Datei.</span><span class="sxs-lookup"><span data-stu-id="796cc-160">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="796cc-161">Führen Sie die `.reg` Datei aus.</span><span class="sxs-lookup"><span data-stu-id="796cc-161">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="796cc-162">Microsoft Edge fragt zuerst die 32-Bit-Registrierung und dann die 64-Bit-Registrierung ab, um systemeigene Messaginghosts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="796cc-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span>  <span data-ttu-id="796cc-163">Wenn Sie die obige `.reg` Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie Sie über eine Eingabeaufforderung des Administrators ausführen.</span><span class="sxs-lookup"><span data-stu-id="796cc-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="796cc-164">macOS</span><span class="sxs-lookup"><span data-stu-id="796cc-164">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="796cc-165">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="796cc-165">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="796cc-166">Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="796cc-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="796cc-167">Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="796cc-167">For example, the manifest file must be stored in following location.</span></span> 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="796cc-168">Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im unter `NativeMessagingHosts` Verzeichnis des Benutzerprofilverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="796cc-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="796cc-169">Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="796cc-169">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="796cc-170">Die  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="796cc-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="796cc-171">Canary</span><span class="sxs-lookup"><span data-stu-id="796cc-171">Canary</span></span>  
    *   <span data-ttu-id="796cc-172">Dev</span><span class="sxs-lookup"><span data-stu-id="796cc-172">Dev</span></span>  
    *   <span data-ttu-id="796cc-173">Beta</span><span class="sxs-lookup"><span data-stu-id="796cc-173">Beta</span></span>  

    <span data-ttu-id="796cc-174">Bei Verwendung des stable-Kanals `{Channel_Name}` ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="796cc-174">When using the Stable channel, `{Channel_Name}` is not required.</span></span>  

### [<span data-ttu-id="796cc-175">Linux</span><span class="sxs-lookup"><span data-stu-id="796cc-175">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="796cc-176">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="796cc-176">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="796cc-177">Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="796cc-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="796cc-178">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="796cc-178">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="796cc-179">Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im unter `NativeMessagingHosts` Verzeichnis des Benutzerprofilverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="796cc-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="796cc-180">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="796cc-180">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="796cc-181">Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei angeben, und führen Sie Berechtigungen für die Host Laufzeit aus.</span><span class="sxs-lookup"><span data-stu-id="796cc-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="796cc-182">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="796cc-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="796cc-183">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="796cc-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="796cc-185">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="796cc-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-ons"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
