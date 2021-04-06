---
description: Native Messagingdokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475211"
---
# <a name="native-messaging"></a><span data-ttu-id="c8819-104">Systemeigenes Messaging</span><span class="sxs-lookup"><span data-stu-id="c8819-104">Native messaging</span></span>  

<span data-ttu-id="c8819-105">Erweiterungen kommunizieren mit einer systemeigenen Win32-App, die auf dem Gerät eines Benutzers installiert ist, mithilfe von APIs, die Nachrichten übergeben.</span><span class="sxs-lookup"><span data-stu-id="c8819-105">Extensions communicate with a native Win32 app installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="c8819-106">Der systemeigene App-Host sendet und empfängt Nachrichten mit Erweiterungen mithilfe von Standardeingaben und Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="c8819-106">The native app host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="c8819-107">Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge ähnlich wie jede andere Erweiterung installiert.</span><span class="sxs-lookup"><span data-stu-id="c8819-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="c8819-108">Native Apps werden jedoch nicht von Microsoft Edge installiert oder verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c8819-108">However, native apps are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="c8819-109">Zum Erwerben der Erweiterung und des nativen App-Hosts verfügen Sie über zwei Verteilungsmodelle.</span><span class="sxs-lookup"><span data-stu-id="c8819-109">To acquire the extension and native app host, you have two distribution models.</span></span>  

*   <span data-ttu-id="c8819-110">Packen Sie Ihre Erweiterung und den Host zusammen.</span><span class="sxs-lookup"><span data-stu-id="c8819-110">Package your extension and the host together.</span></span>  <span data-ttu-id="c8819-111">Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.</span><span class="sxs-lookup"><span data-stu-id="c8819-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="c8819-112">Installieren Sie Ihre Erweiterung mithilfe des [Microsoft Edge-Add-Ons-Speichers,][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]und Ihre Erweiterung fordert Benutzer auf, den Host zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c8819-112">Install your extension using the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="c8819-113">Führen Sie die folgenden Schritte aus, um Ihre Erweiterung zum Senden und Empfangen von Nachrichten mit systemeigenen App-Hosts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8819-113">To create your extension to send and receive messages with native app hosts, complete the following steps.</span></span>  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a><span data-ttu-id="c8819-114">Schritt 1 : Hinzufügen von Berechtigungen zum Erweiterungsmanifest</span><span class="sxs-lookup"><span data-stu-id="c8819-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="c8819-115">Fügen Sie `nativeMessaging` der Dateimanifest.js\*\* der\*\* Erweiterung die Berechtigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8819-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="c8819-116">Der folgende Codeausschnitt ist ein Beispiel für **manifest.jsin**.</span><span class="sxs-lookup"><span data-stu-id="c8819-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a><span data-ttu-id="c8819-117">Schritt 2 : Erstellen Der systemeigenen Messaginghostmanifestdatei</span><span class="sxs-lookup"><span data-stu-id="c8819-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="c8819-118">Systemeigene Apps müssen eine systemeigene Messaginghostmanifestdatei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c8819-118">Native apps must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="c8819-119">Die Manifestdatei enthält die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="c8819-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="c8819-120">Der Pfad zur nativen Messaginghost-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="c8819-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="c8819-121">Die Methode der Kommunikation mit der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8819-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="c8819-122">Eine Liste der zulässigen Erweiterungen, mit denen sie kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="c8819-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="c8819-123">Der Browser liest und überprüft das systemeigene Messaginghostmanifest.</span><span class="sxs-lookup"><span data-stu-id="c8819-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="c8819-124">Der Browser installiert oder verwaltet die systemeigene Messaginghostmanifestdatei nicht.</span><span class="sxs-lookup"><span data-stu-id="c8819-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="c8819-125">Die Hostmanifestdatei muss eine gültige JSON-Datei sein, die die folgenden Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="c8819-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="c8819-126">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c8819-126">Key</span></span>**  
   :::column-end:::
   :::column span="3":::
      **<span data-ttu-id="c8819-127">Details</span><span class="sxs-lookup"><span data-stu-id="c8819-127">Details</span></span>**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="c8819-128">Gibt den Namen des systemeigenen Messaginghosts an.</span><span class="sxs-lookup"><span data-stu-id="c8819-128">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="c8819-129">Clients übergeben die Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="c8819-129">Clients pass the string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="c8819-130">Der Wert darf nur alphanumerische Kleinbuchstaben, Unterstriche und Punkte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8819-130">The value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="c8819-131">Der Wert darf nicht mit einem Punkt beginnen oder enden, und einem Punkt darf kein weiterer Punkt gefolgt werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-131">The value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="c8819-132">Beschreibt die App.</span><span class="sxs-lookup"><span data-stu-id="c8819-132">Describes the app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="c8819-133">Gibt den Pfad zur nativen Messaginghost-Binärdatei an.</span><span class="sxs-lookup"><span data-stu-id="c8819-133">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="c8819-134">Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="c8819-134">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="c8819-135">Unter macOS und Linux muss der Pfad absolut sein.</span><span class="sxs-lookup"><span data-stu-id="c8819-135">On macOS and Linux, the path must be absolute.</span></span>  
          
      <span data-ttu-id="c8819-136">Der Hostprozess beginnt mit dem aktuellen Verzeichnis, das auf das Verzeichnis festgelegt ist, das die Host binär enthält.</span><span class="sxs-lookup"><span data-stu-id="c8819-136">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="c8819-137">Wenn der Parameter beispielsweise auf \(Windows\) festgelegt ist, wird die Binärdatei mit dem aktuellen `C:\App\nm_host.exe` Verzeichnis \( `C:\App\` \) gestartet.</span><span class="sxs-lookup"><span data-stu-id="c8819-137">For example \(Windows\), if the parameter is set to `C:\App\nm_host.exe`, the binary is started using the current directory \(`C:\App\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="c8819-138">Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8819-138">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="c8819-139">Der Wert anweisen Microsoft Edge, den Host zu `stdin` verwenden und mit ihm zu `stdout` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c8819-139">The value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="c8819-140">Der einzige akzeptable Wert ist `stdio` .</span><span class="sxs-lookup"><span data-stu-id="c8819-140">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="c8819-141">Gibt die Liste der Erweiterungen an, die Zugriff auf den systemeigenen Messaginghost haben.</span><span class="sxs-lookup"><span data-stu-id="c8819-141">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="c8819-142">Um Ihre App für die Identifizierung und Kommunikation mit einer Erweiterung zu aktivieren, legen Sie in der manifesten Datei des nativen Messaginghosts den folgenden Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8819-142">To turn on your app to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c8819-143">Querladen Der Erweiterung, um systemeigene Messaging mit dem Host zu testen.</span><span class="sxs-lookup"><span data-stu-id="c8819-143">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="c8819-144">Führen Sie die folgenden Aktionen aus, um die Erweiterung während der Entwicklung quer zu laden und `microsoft_catalog_extension_id` abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8819-144">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following actions.</span></span>  

1.  <span data-ttu-id="c8819-145">Navigieren Sie `edge://extensions` zu , und aktivieren Sie dann die Umschaltfläche Entwicklermodus.</span><span class="sxs-lookup"><span data-stu-id="c8819-145">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="c8819-146">Wählen **Sie Auspacken laden**aus, und wählen Sie dann ihr Erweiterungspaket aus, das quergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8819-146">Choose **Load unpacked**, and then choose your extension package to sideload.</span></span>  
1.  <span data-ttu-id="c8819-147">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8819-147">Choose **OK**.</span></span>  
1.  <span data-ttu-id="c8819-148">Navigieren Sie zu `edge://extensions` Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="c8819-148">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="c8819-149">Kopieren Sie den Schlüssel `microsoft_catalog_extension_id` aus \(ID\) aus dem Erweiterungseintrag auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="c8819-149">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  
    
<span data-ttu-id="c8819-150">Wenn Sie bereit sind, Ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Speicher.</span><span class="sxs-lookup"><span data-stu-id="c8819-150">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="c8819-151">Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Querladen der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8819-151">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="c8819-152">Wenn die ID geändert wurde, aktualisieren Sie `allowed_origins` in der Hostmanifestdatei mit der ID Ihrer veröffentlichten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8819-152">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a><span data-ttu-id="c8819-153">Schritt 3 : Kopieren der systemeigenen Messaginghostmanifestdatei in Ihr System</span><span class="sxs-lookup"><span data-stu-id="c8819-153">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="c8819-154">Der letzte Schritt besteht darin, die systemeigene Messaginghostmanifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass die Manifestdatei ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="c8819-154">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="c8819-155">Führen Sie die folgenden Aktionen aus, um sicherzustellen, dass die Manifestdatei am erwarteten Speicherort platziert wird.</span><span class="sxs-lookup"><span data-stu-id="c8819-155">To ensure your manifest file is placed in the expected location, complete the following the actions.</span></span>  <span data-ttu-id="c8819-156">Der Standort variiert je nach Plattform.</span><span class="sxs-lookup"><span data-stu-id="c8819-156">The location varies by platform.</span></span>

> [!NOTE]
> <span data-ttu-id="c8819-157">Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei bereitstellen und Berechtigungen für die Hostlaufzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8819-157">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

### [<a name="windows"></a><span data-ttu-id="c8819-158">Windows</span><span class="sxs-lookup"><span data-stu-id="c8819-158">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="c8819-159">Die Manifestdatei kann sich an einer beliebigen Stelle im Dateisystem befinden.</span><span class="sxs-lookup"><span data-stu-id="c8819-159">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="c8819-160">Das App-Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert des Schlüssels auf den vollständigen Pfad der Manifestdatei festlegen.</span><span class="sxs-lookup"><span data-stu-id="c8819-160">The app installer must create a registry key and set the default value of the key to the full path of the manifest file.</span></span>  <span data-ttu-id="c8819-161">Die folgenden Speicherorte sind Beispiele für Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8819-161">The following locations are examples of registry keys.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

<span data-ttu-id="c8819-162">Führen Sie eine der folgenden Aktionen aus, um dem Verzeichnis einen Registrierungsschlüssel mit dem Manifestschlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8819-162">To add a registry key to the directory with the manifest key, complete one of the following actions.</span></span>  

*   <span data-ttu-id="c8819-163">Führen Sie den Befehl in der Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="c8819-163">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="c8819-164">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="c8819-164">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   <span data-ttu-id="c8819-165">Erstellen Sie `.reg` eine Datei, und führen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="c8819-165">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="c8819-166">Kopieren Sie den folgenden Befehl in eine `.reg` Datei.</span><span class="sxs-lookup"><span data-stu-id="c8819-166">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="c8819-167">Führen Sie die `.reg` Datei aus.</span><span class="sxs-lookup"><span data-stu-id="c8819-167">Run the `.reg` file.</span></span>  
        
<span data-ttu-id="c8819-168">Microsoft Edge fragt den `HKEY_CURRENT_USER` Stammschlüssel ab, gefolgt von `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="c8819-168">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="c8819-169">In beiden Schlüsseln wird zuerst die 32-Bit-Registrierung durchsucht, und dann wird die 64-Bit-Registrierung durchsucht, um systemeigene Messaginghosts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c8819-169">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="c8819-170">Der Registrierungsschlüssel gibt den Speicherort des systemeigenen Messaginghostmanifests an.</span><span class="sxs-lookup"><span data-stu-id="c8819-170">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="c8819-171">Wenn die Registrierungseinträge für Microsoft Edge nicht den Speicherort des Hostmanifests haben, werden die Registrierungsspeicherorte Chromium und Chrome als Ausweichoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8819-171">If the registry entries for Microsoft Edge don't have the location of the host manifest, the Chromium and Chrome registry locations are used as fallback options.</span></span>  <span data-ttu-id="c8819-172">Wenn Microsoft Edge den Registrierungsschlüssel an einem der zuvor aufgeführten Speicherorte findet, werden die im folgenden Codeausschnitt aufgeführten Speicherorte nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="c8819-172">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in the following code snippet.</span></span>  <span data-ttu-id="c8819-173">Wenn Sie die erstellte Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie sie mithilfe einer `.reg` Administrator-Eingabeaufforderung ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8819-173">If you run your created `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>

<span data-ttu-id="c8819-174">Die folgende Liste ist die Suchreihenfolge für die Registrierungsstandorte.</span><span class="sxs-lookup"><span data-stu-id="c8819-174">The following list is the search order for the registry locations.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> <span data-ttu-id="c8819-175">Wenn Sie Erweiterungen für die Microsoft Edge-Add-Ons und den Chrome Webstore haben, müssen Sie die Erweiterungs-IDs hinzufügen, die den beiden Speichern in der Hostmanifestdatei entspricht, da nur das Hostmanifest gelesen wird, das dem ersten gefundenen Registrierungsspeicherort `allowed_origins` entspricht.</span><span class="sxs-lookup"><span data-stu-id="c8819-175">If you have extensions on the Microsoft Edge Add-ons and the Chrome Webstore, you must add the extension IDs corresponding to both the stores in the `allowed_origins` of the host manifest file because only the host manifest corresponding to the first registry location found is read.</span></span>  

### [<a name="macos"></a><span data-ttu-id="c8819-176">macOS</span><span class="sxs-lookup"><span data-stu-id="c8819-176">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="c8819-177">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c8819-177">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="c8819-178">Systemweite systemweite native Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c8819-178">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="c8819-179">Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-179">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   <span data-ttu-id="c8819-180">Benutzerspezifische native Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c8819-180">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="c8819-181">Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-181">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    <span data-ttu-id="c8819-182">Der  `{Channel_Name}` `Microsoft Edge {Channel_Name}` In-Wert muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c8819-182">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    <span data-ttu-id="c8819-183">Bei Verwendung des ` {Channel_Name}` Stable-Kanals ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8819-183">When using the Stable channel, ` {Channel_Name}` isn't required.</span></span>  
    
### [<a name="linux"></a><span data-ttu-id="c8819-184">Linux</span><span class="sxs-lookup"><span data-stu-id="c8819-184">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="c8819-185">Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c8819-185">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="c8819-186">Systemweite systemweite native Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c8819-186">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="c8819-187">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-187">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="c8819-188">Benutzerspezifische native Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c8819-188">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="c8819-189">Die Manifestdatei muss an folgendem Speicherort gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-189">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-Ons"

> [!NOTE]
> <span data-ttu-id="c8819-191">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8819-191">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c8819-192">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="c8819-192">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c8819-194">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8819-194">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
