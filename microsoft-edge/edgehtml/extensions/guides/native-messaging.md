---
description: Erfahren Sie, wie Sie natives Messaging verwenden können, um Ihre Erweiterung mit einer Begleit-UWP-App zu kommunizieren.
title: Systemeigene | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, native, messaging, uwp
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9a306055b8f86b92aa5c3e7cd6de44f2386307d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399358"
---
# <a name="native-messaging-in-microsoft-edge"></a><span data-ttu-id="12460-104">Natives Messaging in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="12460-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a><span data-ttu-id="12460-105">Übersicht über die systemeigene Messagingarchitektur</span><span class="sxs-lookup"><span data-stu-id="12460-105">Native messaging architecture overview</span></span>  

<span data-ttu-id="12460-106">Mit dem Windows 10 Creators Update können Microsoft Edge-Erweiterungen systemeigenes Messaging verwenden, um mit einer Begleit-App für die universelle Windows-Plattform \(UWP\) zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform \(UWP\) app.</span></span>  <span data-ttu-id="12460-107">Auf einer hohen Ebene verwenden Microsoft Edge-Erweiterungen dieselben APIs für systemeigene Nachrichten wie Chrome- und Firefox-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="12460-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span>  <span data-ttu-id="12460-108">Der systemeigene Messaginghost muss jedoch mithilfe der universellen Windows-Plattform implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="12460-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>  

> [!NOTE]
> <span data-ttu-id="12460-109">Die unten beschriebene Methode \(Herstellen einer Verbindung mit einer UWP-App über AppService\) ist der einzige unterstützte Mechanismus zum Aktivieren der Kommunikation zwischen Microsoft Edge-Erweiterungen und systemeigenen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="12460-109">The method outlined below \(connecting to a UWP app via AppService\) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span>  <span data-ttu-id="12460-110">Weitere Informationen [](#adding-a-desktop-bridge-component) zum Aktivieren der Kommunikation mit älteren Win32-Komponenten finden Sie im Abschnitt Hinzufügen einer Desktopbrücke-Komponente in diesem Handbuch.</span><span class="sxs-lookup"><span data-stu-id="12460-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span>  

<span data-ttu-id="12460-111">Die systemeigene Messagingarchitektur in Microsoft Edge nutzt die vorhandene API als zugrunde liegende Prozesskommunikation [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\)-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="12460-111">The native messaging architecture in Microsoft Edge leverages the existing [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API as the underlying inter-process communication \(IPC\) infrastructure.</span></span>  <span data-ttu-id="12460-112">UWP-Apps verwenden die `AppService` API, um miteinander zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-112">UWP apps use the `AppService` API to communicate with one another.</span></span>  <span data-ttu-id="12460-113">Aus diesem Grund können Microsoft Edge-Erweiterungen jetzt mit UWP-Apps kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-113">Because of this, Microsoft Edge extensions are now able to communicate with UWP apps.</span></span>  

![Systemeigene Messagingarchitektur](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a><span data-ttu-id="12460-115">Wann und wann systemeigenes Messaging nicht verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="12460-115">When and when not to use native messaging</span></span>  

<span data-ttu-id="12460-116">Natives Messaging fügt Ihrer Erweiterung eine ganz neue Ebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="12460-116">Native messaging adds a whole new layer to your extension.</span></span>  <span data-ttu-id="12460-117">Durch die Implementierung einer UWP-Begleit-App für Ihre Erweiterung stehen Ihnen die folgenden Möglichkeiten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="12460-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>  

*   <span data-ttu-id="12460-118">Synchronisieren Sie Daten \(z. B. Anmeldeinformationen\) mit einer Begleit-UWP-App.</span><span class="sxs-lookup"><span data-stu-id="12460-118">Synchronize data \(for example credentials\) with a companion UWP app.</span></span>  
*   <span data-ttu-id="12460-119">Implementieren Sie strengere Verschlüsselungs-/Entschlüsselungsalgorithmen, die in Web-APIs nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="12460-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>  
*   <span data-ttu-id="12460-120">Zugreifen auf Ressourcen, auf die nicht über Web-APIs zugegriffen werden kann, z. B. Hardware oder USB-Geräte</span><span class="sxs-lookup"><span data-stu-id="12460-120">Access resources that are not accessible through web APIs, for example hardware or USB devices</span></span>  

<span data-ttu-id="12460-121">Es gibt einige Instanzen, in denen systemeigenes Messaging aufgrund von Sicherheits- oder Richtlinieneinschränkungen nicht verwendet werden sollte:</span><span class="sxs-lookup"><span data-stu-id="12460-121">There are a few instances where native messaging should not be used due to security or policy restrictions:</span></span>  

*   <span data-ttu-id="12460-122">Ändern von Benutzereinstellungen in Microsoft Edge oder Windows, z. B. Ändern des Standardbrowsers oder Suchanbieters.</span><span class="sxs-lookup"><span data-stu-id="12460-122">Modifying user settings in either Microsoft Edge or Windows, for example changing the default browser or search provider.</span></span>  
*   <span data-ttu-id="12460-123">Aktionen, die gegen Microsoft Store-Richtlinien für Apps und Erweiterungen verstoßen.</span><span class="sxs-lookup"><span data-stu-id="12460-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>  
*   <span data-ttu-id="12460-124">Übertragen von Daten an den Remoteendpunkt über den systemeigenen Nachrichtenhost.</span><span class="sxs-lookup"><span data-stu-id="12460-124">Transferring data to remote endpoint via native message host.</span></span>  
*   <span data-ttu-id="12460-125">Zulassen, dass andere Apps Inhalte herunterladen, die das Erweiterungsverhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="12460-125">Allowing other apps to download content that changes extension behavior.</span></span>  

## <a name="demos"></a><span data-ttu-id="12460-126">Demos</span><span class="sxs-lookup"><span data-stu-id="12460-126">Demos</span></span>  

<span data-ttu-id="12460-127">Informationen dazu, wie eine native Microsoft Edge-Messagingerweiterung aussieht, die sowohl eine #A0 als auch eine Desktopbrücke hat, finden Sie in den [Beispielen SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) und [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="12460-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>  

### <a name="how-it-works"></a><span data-ttu-id="12460-128">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="12460-128">How it works</span></span>  

<span data-ttu-id="12460-129">Die Microsoft Edge-Erweiterungskomponente des Beispiels verwendet ihr Inhaltsskript, um zu erkennen, wann ein Benutzer Informationen eintippt, die verschlüsselt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12460-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span>  <span data-ttu-id="12460-130">Die Erweiterung teilt dies der Desktop-Brücke-Komponente über systemeigenes Messaging mit.</span><span class="sxs-lookup"><span data-stu-id="12460-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span>  <span data-ttu-id="12460-131">Wenn der Benutzer bereit ist, die Daten zu übermitteln, gibt die Erweiterung einen verschlüsselten Wert zurück an die Website zurück.</span><span class="sxs-lookup"><span data-stu-id="12460-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>  

> [!NOTE]
> <span data-ttu-id="12460-132">Dieses Beispiel funktioniert nur auf einer Webseite, die benutzerdefinierte Ereignisse verwendet, um mit dem Inhaltsskript der Erweiterung zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-132">This sample will only work on a webpage that uses custom events to communicate with the content script of the extension.</span></span>  <span data-ttu-id="12460-133">Der Beispielordner enthält eine [HTML-Datei zum](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) Testen der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="12460-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>  

<span data-ttu-id="12460-134">In diesem Beispiel wird die UWP-App verwendet, um Antworten von der Desktopbrücke an Microsoft Edge zu übergeben, die dann per Rückruf an die Microsoft Edge-Erweiterung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="12460-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span>  <span data-ttu-id="12460-135">Während in diesem Beispiel der systemeigene Messaginghost in der Haupt-App ausgeführt wird, kann er auch als Hintergrundaufgabe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="12460-135">While this example has the native messaging host run in the main app, it is also able to run as a background task.</span></span>  <span data-ttu-id="12460-136">Um zwischen den beiden zu wechseln, müssen Sie das Hintergrundskript der Erweiterung bearbeiten und die Zeichenfolge innerhalb in `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` ändern.</span><span class="sxs-lookup"><span data-stu-id="12460-136">Switching between the two requires editing the background script of the extension, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>  

## <a name="chrome-vs-microsoft-edge-implementation"></a><span data-ttu-id="12460-137">Chrome vs. Microsoft Edge-Implementierung</span><span class="sxs-lookup"><span data-stu-id="12460-137">Chrome vs Microsoft Edge implementation</span></span>  

<span data-ttu-id="12460-138">Während Chrome die Route der Verwendung von NACHRICHTENübergehenden APIs für ihre Erweiterungen für die Kommunikation mit Apps begeht, verwendet Microsoft Edge die API, mit der microsoft Edge-Erweiterungen und [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) UWP-Apps kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="12460-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>  

<span data-ttu-id="12460-139">In diesem Abschnitt werden die Unterschiede zwischen der Verarbeitung von Chrome und Microsoft Edge mit der nativen Messagingimplementierung erläutert.</span><span class="sxs-lookup"><span data-stu-id="12460-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>  

### <a name="registration-and-host-manifest"></a><span data-ttu-id="12460-140">Registrierung und Hostmanifest</span><span class="sxs-lookup"><span data-stu-id="12460-140">Registration and host manifest</span></span>  

<span data-ttu-id="12460-141">Damit Ihre App von Ihrer Erweiterung als systemeigener Messaginghost erkannt wird, muss sie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="12460-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>  

<span data-ttu-id="12460-142">Für [die Registrierung von nativen](https://developer.chrome.com/extensions/nativeMessaging) Chrome-Messaginghosts muss Ihre App eine Manifestdatei an einer beliebigen Stelle im Windows-Dateisystem installieren, die die systemeigene Messaginghostkonfiguration definiert.</span><span class="sxs-lookup"><span data-stu-id="12460-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>  

<span data-ttu-id="12460-143">Das folgende JSON ist ein Beispiel für Einstellungen für die Konfigurationsdatei:</span><span class="sxs-lookup"><span data-stu-id="12460-143">The following JSON is an example of settings for the config file:</span></span>  

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="12460-144">Um diese Datei zu installieren, muss die App:</span><span class="sxs-lookup"><span data-stu-id="12460-144">To install this file, the app would need to:</span></span>  

1.  <span data-ttu-id="12460-145">Registrieren Sie die Manifestdatei an einem vordefinierten Speicherort in der Registrierung, der die Hostkonfiguration definiert:</span><span class="sxs-lookup"><span data-stu-id="12460-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        <span data-ttu-id="12460-146">or</span><span class="sxs-lookup"><span data-stu-id="12460-146">or</span></span>  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  <span data-ttu-id="12460-147">Legen Sie den Standardwert dieses Schlüssels auf den vollständigen Pfad zur Manifestdatei fest, z. B.</span><span class="sxs-lookup"><span data-stu-id="12460-147">Set the default value of that key to the full path to the manifest file, for example</span></span> `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

<span data-ttu-id="12460-148">Für Microsoft Edge müssen Sie zum Registrieren eines [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(nativen Messaginghosts\) die UWP-Begleit-App in das gleiche Paket wie ihre Erweiterung einbeigen und die [AppService-Erweiterung](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in der Datei Ihres Projekts `Package.appxmanifest` angeben.</span><span class="sxs-lookup"><span data-stu-id="12460-148">For Microsoft Edge, in order to register an [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(native messaging host\) you must include the UWP companion app in the same package as your extension and specify the [AppService extension](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in the `Package.appxmanifest` file of your project.</span></span>  <span data-ttu-id="12460-149">Die `EntryPoint` Attribute und können von Ihnen konfiguriert `Name` werden:</span><span class="sxs-lookup"><span data-stu-id="12460-149">The `EntryPoint` and `Name` attributes may be configured by you:</span></span>  

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...   
    </Application>
</Applications>
```  

<span data-ttu-id="12460-150">Außerdem müssen Sie festlegen, welche Erweiterungen eine Verbindung mit dem Dienst herstellen dürfen.</span><span class="sxs-lookup"><span data-stu-id="12460-150">You also need to set which extensions are allowed to connect to the service.</span></span>  <span data-ttu-id="12460-151">Da Microsoft Edge nicht über eine entsprechende Manifesteigenschaft in appxManifest verfügt, muss dies zur Laufzeit von Ihrer `"allowed_origins"` UWP-App bestimmt und erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="12460-151">Because Microsoft Edge does not have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span>  <span data-ttu-id="12460-152">Da Microsoft Edge die Verbindung im Namen der Erweiterung aufbaut, sucht die App den Paketfamiliennamen des Anrufers, um zu ermitteln, ob die Durchwahl durch Microsoft Edge verbunden ist, um den Anrufer zu steuern oder zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-152">Since Microsoft Edge establishes the connection on behalf of the extension, the app looks up the Package Family Name of the caller to determine if extension is being connected by Microsoft Edge to control or authenticate the caller.</span></span>  <span data-ttu-id="12460-153">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="12460-153">For example</span></span>   

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```  

### <a name="message-sending"></a><span data-ttu-id="12460-154">Senden von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="12460-154">Message sending</span></span>  

<span data-ttu-id="12460-155">Damit eine App und eine Erweiterung miteinander kommunizieren können, müssen Nachrichten an und von ihnen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="12460-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>  

<span data-ttu-id="12460-156">Chrome-Erweiterungen initiieren eine Nachricht mithilfe der API, um eine Nachricht über einen nicht persistenten Kanal an den systemeigenen [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Host zu senden.</span><span class="sxs-lookup"><span data-stu-id="12460-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span>  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="12460-157">Der erste Parameter ist der Name des systemeigenen Hosts, nach dem Chrome in der Registrierung für das Manifest sucht.</span><span class="sxs-lookup"><span data-stu-id="12460-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span>  <span data-ttu-id="12460-158">Das Manifest gibt die EXE an, die Chrome in einem Sandkasten startet, und die Nachricht wird mithilfe von std i/o gesendet.</span><span class="sxs-lookup"><span data-stu-id="12460-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span>  
<span data-ttu-id="12460-159">Erweiterungen richten auch einen beständigen Kanal mithilfe der API ein, die den Namen des systemeigenen Hosts `runtime.connectNative` als einzigen Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="12460-159">Extensions also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span>  

<span data-ttu-id="12460-160">Microsoft Edge verwendet dasselbe Konstrukt wie die systemeigene Messaging-API in Chrome, um Microsoft Edge-Erweiterungen die Angabe zu ermöglichen, mit welchem App-Dienst eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12460-160">Microsoft Edge uses the same construct as the native messaging API in Chrome to allow Microsoft Edge extensions to specify which app service to connect to.</span></span>  <span data-ttu-id="12460-161">Der erste Parameter in `runtime.sendNativeMessage` gibt den Namen des App-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="12460-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span>  <span data-ttu-id="12460-162">Im Abschnitt [Registrierung und Hostmanifest](#registration-and-host-manifest) ist dies `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="12460-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span>  <span data-ttu-id="12460-163">Die Microsoft Edge-Erweiterungsplattform schränkt den systemeigenen Messaginghost auf eine UWP-App ein, die in derselben AppX wie die Erweiterung verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="12460-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span>  <span data-ttu-id="12460-164">Dadurch werden alle Sicherheitsrisiken im Zusammenhang mit böswilligen Angriffen verringert, die versuchen, Microsoft Edge mit einem anderen Paketfamiliennamen zu verbinden, indem Manifesteinträge manimaniert werden.</span><span class="sxs-lookup"><span data-stu-id="12460-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span>  

<span data-ttu-id="12460-165">Dies bedeutet, dass Microsoft Edge denselben Paketfamiliennamen wie die Erweiterung neben dem in der API angegebenen Namen verwendet, um den Anbieter des App-Diensts `AppService` eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="12460-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="12460-166">Dies kann nicht einfach vom [Microsoft Edge Extension Toolkit konvertiert werden.](./porting-chrome-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="12460-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span>  <span data-ttu-id="12460-167">Alle Erweiterungen, die die Berechtigung angibt, werden als erforderlich gekennzeichnet, dass für diese `"nativeMessaging"` Komponente eine manuelle Konvertierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="12460-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>  

### <a name="communication-protocol"></a><span data-ttu-id="12460-168">Kommunikationsprotokoll</span><span class="sxs-lookup"><span data-stu-id="12460-168">Communication protocol</span></span>  

<span data-ttu-id="12460-169">Das Kommunikationsprotokoll für systemeigene Nachrichten bestimmt, wie Nachrichten vor dem Senden formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="12460-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>  

<span data-ttu-id="12460-170">Chrome startet jeden systemeigenen Messaginghost in einem separaten Prozess und kommuniziert mit ihm mithilfe von Standardeingaben und Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="12460-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span>  <span data-ttu-id="12460-171">Das gleiche Format wird verwendet, um Nachrichten in beide Richtungen zu senden: Jede Nachricht wird mithilfe von JSON serialisiert, UTF-8 codiert und der 32-Bit-Nachrichtenlänge in systemeigener Bytereihenfolge vorangegangen.</span><span class="sxs-lookup"><span data-stu-id="12460-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>  

<span data-ttu-id="12460-172">Für Microsoft Edge wird die Hintergrundaufgabe/Haupt-App, die den App-Dienst implementiert, von der Plattform gestartet.</span><span class="sxs-lookup"><span data-stu-id="12460-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span>  <span data-ttu-id="12460-173">Beim Start wird `Run` die Methode der Hintergrundaufgabe aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="12460-173">On startup, the `Run` method of the background task is invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service is not stopped and ended.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="12460-174">Wenn Ihre Erweiterung eine Nachricht an Ihre UWP-App sendet, wird [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) das Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="12460-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) event will be raised.</span></span>  <span data-ttu-id="12460-175">Diese JSON-formatierte Nachricht wird dann in das erste KeyValue-Paar eines Objekts [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) stringifiziert.</span><span class="sxs-lookup"><span data-stu-id="12460-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object.</span></span>  <span data-ttu-id="12460-176">:</span><span class="sxs-lookup"><span data-stu-id="12460-176">:</span></span>  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="12460-177">Wenn Ihre UWP-App eine Antwort an Ihre Erweiterung zurücksendet, wird dem [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) Objekt eine `ValueSet` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="12460-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) will be added to the `ValueSet` object.</span></span>  <span data-ttu-id="12460-178">Die `Key` Eigenschaft wird von Microsoft Edge ignoriert, die Eigenschaft enthält jedoch eine gültige `Value` JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="12460-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>  

### <a name="callback"></a><span data-ttu-id="12460-179">Rückruf</span><span class="sxs-lookup"><span data-stu-id="12460-179">Callback</span></span>  

<span data-ttu-id="12460-180">Für Rückrufe verwendet Chrome die Funktion, mit der eine Rückruffunktion asynchrone Antworten vom Senden [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) einer Nachricht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="12460-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>  

<span data-ttu-id="12460-181">Microsoft Edge verwendet die Methode des Objekts, damit die App ein Objekt zurück an [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) die Erweiterung senden [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) kann.</span><span class="sxs-lookup"><span data-stu-id="12460-181">Microsoft Edge uses the [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) method  of the [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) object to let the app send a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object back to the extension.</span></span>  

### <a name="message-size-limit"></a><span data-ttu-id="12460-182">Grenzwert für die Nachrichtengröße</span><span class="sxs-lookup"><span data-stu-id="12460-182">Message size limit</span></span>  

<span data-ttu-id="12460-183">Nachrichten, die zwischen einer Erweiterung und einer App hin- und hergeschickt werden, haben unterschiedliche Einschränkungen für die Nachrichtengröße für Chrome und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12460-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>  

<span data-ttu-id="12460-184">Chrome hat die folgenden Einschränkungen bei der Nachrichtengröße:</span><span class="sxs-lookup"><span data-stu-id="12460-184">Chrome has the following message size limitations:</span></span>  

*   <span data-ttu-id="12460-185">Grenzwert für einzelne Nachrichten vom systemeigenen Messaginghost: 1 MB</span><span class="sxs-lookup"><span data-stu-id="12460-185">Single message limit from native messaging host:  1 MB</span></span>  
*   <span data-ttu-id="12460-186">Grenzwert für einzelne Nachrichten, der an den systemeigenen Messaginghost gesendet wird: 4 GB</span><span class="sxs-lookup"><span data-stu-id="12460-186">Single message limit sent to native messaging host:  4 GB</span></span>  

<span data-ttu-id="12460-187">Für Microsoft Edge hat microsoft Edge zwar keine Beschränkung der Nachrichtengröße \(abhängig vom Arbeitsspeicher\), aber Microsoft Edge schützt sich vor fehlgeleiteten nativen Apps, indem die folgenden Größenbeschränkungen für Nachrichten `AppService` gelten:</span><span class="sxs-lookup"><span data-stu-id="12460-187">For Microsoft Edge, while `AppService` has no limit on message size \(dependent on memory\), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>  

*   <span data-ttu-id="12460-188">Grenzwert für einzelne Nachrichten von der UWP-App zur Erweiterung: 1 MB</span><span class="sxs-lookup"><span data-stu-id="12460-188">Single message limit from UWP app to extension: 1 MB</span></span>  
*   <span data-ttu-id="12460-189">Grenzwert für einzelne Nachrichten von der Erweiterung auf die UWP-App: 100 MB</span><span class="sxs-lookup"><span data-stu-id="12460-189">Single message limit from extension to UWP app: 100 MB</span></span>  

### <a name="native-messaging-connections"></a><span data-ttu-id="12460-190">Native Messagingverbindungen</span><span class="sxs-lookup"><span data-stu-id="12460-190">Native messaging connections</span></span>  

<span data-ttu-id="12460-191">Es gibt zwei Arten von Verbindungen für systemeigenes Messaging. persistent und nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="12460-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>  
<span data-ttu-id="12460-192">Eine **dauerhafte** Verbindung ist eine Verbindung, die solange ausgeführt wird, bis der Port zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="12460-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span>  <span data-ttu-id="12460-193">Eine **nicht dauerhafte** Verbindung ist eine Verbindung, die für eine Nachricht gleichzeitig geöffnet wird und nach der Zustellung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="12460-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>  

#### <a name="persistent"></a><span data-ttu-id="12460-194">Permanent</span><span class="sxs-lookup"><span data-stu-id="12460-194">Persistent</span></span>  

<span data-ttu-id="12460-195">Für Chrome wird eine dauerhafte Verbindung hergestellt, indem ein Messagingport mithilfe von erstellt [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) wird.</span><span class="sxs-lookup"><span data-stu-id="12460-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="12460-196">Sobald der Port hergestellt wurde, startet Chrome einen systemeigenen Messaginghostprozess, der ausgeführt wird, bis der Port zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="12460-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>  

<span data-ttu-id="12460-197">Sobald ein Messagingport mit Microsoft Edge erstellt wurde, startet Microsoft Edge den und führt ihn so lange aus, bis `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) der Port zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="12460-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) and keeps it running until the port is destroyed.</span></span>  <span data-ttu-id="12460-198">Der folgende Codeausschnitt zeigt, wie eine dauerhafte Verbindung von einer UWP-App aus hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12460-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span>  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a><span data-ttu-id="12460-199">Nicht beständig</span><span class="sxs-lookup"><span data-stu-id="12460-199">Non-persistent</span></span>  

<span data-ttu-id="12460-200">Wenn eine Nachricht in Chrome gesendet wird, ohne einen Messagingport zu erstellen, startet Chrome einen neuen systemeigenen Messaginghostprozess [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) für jede Nachricht.</span><span class="sxs-lookup"><span data-stu-id="12460-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span>  <span data-ttu-id="12460-201">Die erste vom Hostprozess generierte Nachricht wird als Antwort auf die ursprüngliche Anforderung und alle anderen Nachrichten behandelt, nachdem sie ignoriert wurden.</span><span class="sxs-lookup"><span data-stu-id="12460-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>  

<span data-ttu-id="12460-202">Microsoft Edge beendet und beendet die Verbindung, nachdem jede Antwort auf jede Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="12460-202">Microsoft Edge stops and ends the connection after every response to each message has been received.</span></span>  <span data-ttu-id="12460-203">Der folgende Codeausschnitt zeigt eine nicht dauerhafte Verbindung, die mit der hergestellt wird, wird dann innerhalb der UWP-App beendet, nachdem eine Anforderung empfangen und als `AppServiceConnection` gespeichert [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) wurde.</span><span class="sxs-lookup"><span data-stu-id="12460-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true).</span></span>  

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```  

### <a name="permission"></a><span data-ttu-id="12460-204">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="12460-204">Permission</span></span>  

<span data-ttu-id="12460-205">Um die native Messagingnutzung mit Ihrer Erweiterung zu aktivieren, müssen Sie sowohl für Chrome als auch für Microsoft Edge die `"nativeMessaging"` Berechtigung in Der Datei `manifest.json` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="12460-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you must declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>  

## <a name="app-services"></a><span data-ttu-id="12460-206">App-Dienste</span><span class="sxs-lookup"><span data-stu-id="12460-206">App services</span></span>  

<span data-ttu-id="12460-207">In diesem Abschnitt werden die Auswirkungen von App-Diensten auf die systemeigene Messagingleistung und den Speicher von Microsoft Edge erläutert.</span><span class="sxs-lookup"><span data-stu-id="12460-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>  

### <a name="performance"></a><span data-ttu-id="12460-208">Leistung</span><span class="sxs-lookup"><span data-stu-id="12460-208">Performance</span></span>  

<span data-ttu-id="12460-209">App-Dienste werden von der Vordergrund-App "gesponsert", die sie aufruft, die für systemeigene Messagingzwecke Microsoft Edge ist.</span><span class="sxs-lookup"><span data-stu-id="12460-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span>  <span data-ttu-id="12460-210">Dies bedeutet, dass App-Dienste so lange ausgeführt werden können, wie Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12460-210">This means that app services can run as long as Microsoft Edge is running.</span></span>  

<span data-ttu-id="12460-211">In Bezug auf die Latenz verwenden App-Dienste Benannte Pipes, die nach der ersten Verbindung zwei Apps die direkte Kommunikation ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="12460-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span>  <span data-ttu-id="12460-212">Diese Kommunikationsmethode erzeugt eine geringe Latenz.</span><span class="sxs-lookup"><span data-stu-id="12460-212">This method of communication produces low latency.</span></span>  <span data-ttu-id="12460-213">Auf Geräten mit langsamen CPUs wird nach dem Starten des Prozesses, der den #A0 hostet (~80 ms zum Starten der Hintergrundaufgabe auf einigen Geräten\) eine anfängliche Wartezeit auftreten.</span><span class="sxs-lookup"><span data-stu-id="12460-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service \(~80ms to startup the background task on some devices\).</span></span>  <span data-ttu-id="12460-214">Nach dem Start sollte die Leistung auf langsamen CPU-Geräten gut sein.</span><span class="sxs-lookup"><span data-stu-id="12460-214">After start-up, performance on slow CPU devices should be good.</span></span>  

### <a name="memory"></a><span data-ttu-id="12460-215">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="12460-215">Memory</span></span>  

<span data-ttu-id="12460-216">Der einem App-Dienst zugewiesene Arbeitsspeicher wird aus dem Kontingent für Microsoft Edge herausgenommen.</span><span class="sxs-lookup"><span data-stu-id="12460-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span>  <span data-ttu-id="12460-217">Wenn Microsoft Edge zu viele App-Dienste startet, besteht die Möglichkeit, dass der Arbeitsspeicher nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12460-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span>  <span data-ttu-id="12460-218">Die üblichen Speicherdeckel für Hintergrundaufgabe werden für App-Dienste erzwungen.</span><span class="sxs-lookup"><span data-stu-id="12460-218">The usual background task memory caps are enforced on app services.</span></span>  <span data-ttu-id="12460-219">Beispielsweise kann eine Hintergrundaufgabe des App-Diensts auf einem Gerät mit 512 MB nicht größer als 16 MB sein.</span><span class="sxs-lookup"><span data-stu-id="12460-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span>  <span data-ttu-id="12460-220">Diese Anzahl steigt, wenn die Geräte nach oben skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="12460-220">This number goes up as the devices scale up.</span></span>  

## <a name="creating-an-extension-with-native-messaging"></a><span data-ttu-id="12460-221">Erstellen einer Erweiterung mit systemeigenem Messaging</span><span class="sxs-lookup"><span data-stu-id="12460-221">Creating an extension with native messaging</span></span>  

<span data-ttu-id="12460-222">Um systemeigenes Messaging zu testen, benötigt Ihre Erweiterung einen Paketfamiliennamen.</span><span class="sxs-lookup"><span data-stu-id="12460-222">In order to test native messaging, your extension needs a Package Family Name.</span></span>  <span data-ttu-id="12460-223">Microsoft Edge verwendet dies, um die identität des systemeigenen Nachrichtenhosts zu ermitteln, d. h., Ihre Erweiterung sollte verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="12460-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span>  

<span data-ttu-id="12460-224">So erstellen Sie Ihre Erweiterung mit systemeigenem Messaging in Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="12460-224">To create your extension with native messaging in Visual Studio:</span></span>  

1.  <span data-ttu-id="12460-225">Erstellen Sie ein UWP-Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="12460-225">Create a UWP project in Visual Studio.</span></span>  
1.  <span data-ttu-id="12460-226">[Hinzufügen `AppService` zu Ihrer UWP-App](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="12460-226">[Add `AppService` to your UWP app](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>  
    *   <span data-ttu-id="12460-227">Sie können optional konfigurieren, dass sie an diesem Punkt in der [ `AppService` Haupt-App](/windows/uwp/launch-resume/convert-app-service-in-process) statt als Hintergrundaufgabe gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="12460-227">You can optionally [configure `AppService` to be hosted in the main app](/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>  
1.  <span data-ttu-id="12460-228">Erstellen und testen Sie Ihr UWP-Projekt.</span><span class="sxs-lookup"><span data-stu-id="12460-228">Build and test your UWP project.</span></span>  
    *   <span data-ttu-id="12460-229">Optional können Sie eine [Desktop-Brücke-Komponente hinzufügen.](#adding-a-desktop-bridge-component)</span><span class="sxs-lookup"><span data-stu-id="12460-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>  
1.  <span data-ttu-id="12460-230">Erstellen Sie eine Microsoft Edge-Erweiterung, die systemeigenes Messaging für die Kommunikation mit der UWP-Begleit-App verwendet.</span><span class="sxs-lookup"><span data-stu-id="12460-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span>  <span data-ttu-id="12460-231">Die Erweiterungsdateien können einem Ordner mit dem Namen `Extension` im UWP-Projekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="12460-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span>  <span data-ttu-id="12460-232">Alle Dateien unter diesem Ordner, einschließlich Unterordner, müssen ihre Eigenschaften so konfiguriert haben, dass und `Build Action=Content` `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="12460-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  <span data-ttu-id="12460-233">Stellen Sie `manifest.json` sicher, dass diese Eigenschaften ebenfalls konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="12460-233">Make sure `manifest.json` is also configured with these properties.</span></span>  
1.  <span data-ttu-id="12460-234">Ändern Sie die Datei im Projekt, um Erweiterungsmetadaten zu enthalten, und konvertieren Sie sie in eine kopflose `package.manifest.xml` App, indem Sie `AppListEntry="none"` folgendes hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="12460-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>  
    
    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">
    
    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>
       
       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```  
    
1.  <span data-ttu-id="12460-235">Verwenden Sie `AppService` den für die UWP konfigurierten Namen in den systemeigenen Messaging-APIs.</span><span class="sxs-lookup"><span data-stu-id="12460-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>  
1.  <span data-ttu-id="12460-236">Erstellen und [Bereitstellen des](#deploying) UWP-Projekts \(mit der optionalen Desktop bridge-Komponente\).</span><span class="sxs-lookup"><span data-stu-id="12460-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span></span>  
1.  <span data-ttu-id="12460-237">[Packen](#packaging) Sie Ihre systemeigene Messagingerweiterung, sobald sie für die Store-Übermittlung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="12460-237">[Package](#packaging) your native messaging extension once it is ready for Store submission</span></span>  
    
> [!NOTE]
> <span data-ttu-id="12460-238">Verweisen Sie [auf den Abschnitt Demos,](#demos) um ein Beispiel für eine vollständige systemeigene Messagingerweiterung zu finden.</span><span class="sxs-lookup"><span data-stu-id="12460-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>  

## <a name="adding-a-desktop-bridge-component"></a><span data-ttu-id="12460-239">Hinzufügen einer Desktopbrücke-Komponente</span><span class="sxs-lookup"><span data-stu-id="12460-239">Adding a Desktop Bridge component</span></span>  

<span data-ttu-id="12460-240">Wenn Sie Ihrem Paket eine Desktop-Brücke-Komponente hinzufügen möchten, müssen Sie Ihr Win32-Projekt in einem Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="12460-240">If you want to add a Desktop Bridge component to your package, you must create and build your Win32 project in Visual Studio.</span></span>  <span data-ttu-id="12460-241">Informationen zum Konvertieren Ihrer win32-App in UWP finden Sie unter Portieren von Apps zu [Windows 10 über desktop bridge](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="12460-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span>  <span data-ttu-id="12460-242">Nach der Visual Studio können Sie dem Paket die ausführbare Datei Win32 hinzufügen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="12460-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>  

1.  <span data-ttu-id="12460-243">Fügen Sie das Win32-Projekt derselben Lösung wie das UWP-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="12460-243">Add the Win32 project to the same solution as the UWP project.</span></span>  
1.  <span data-ttu-id="12460-244">Legen Sie das Win32-Projekt als abhängiges Projekt für das UWP-Projekt ein:</span><span class="sxs-lookup"><span data-stu-id="12460-244">Set the Win32 project as a dependent project for the UWP project:</span></span>  
    
    ![Einrichten von Projektabhängigkeiten](../media/project-dependencies.png)  
    
1.  <span data-ttu-id="12460-246">Erstellen Sie `Win32` einen Ordner innerhalb des UWP-Projekts.</span><span class="sxs-lookup"><span data-stu-id="12460-246">Create a `Win32` folder within the UWP project.</span></span>  <span data-ttu-id="12460-247">Kopieren Sie die erforderlichen Binärdateien für `Win32` das Projekt in diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="12460-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span>  <span data-ttu-id="12460-248">Konfigurieren Sie die Eigenschaften aller Binärdateien so, dass `Build Action=Content` und `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="12460-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  
    
    ![Ordner mit win32- und UWP-App-Dateien](../media/desktop-bridge.png)  
    
1.  <span data-ttu-id="12460-250">Ändern Sie die UWP-Projektdatei, um alle erforderlichen Binärdateien für das Projekt mithilfe des PostBuild-Ereignisbefehls in diesen `Win32` Ordner zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="12460-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span>  <span data-ttu-id="12460-251">Dadurch wird sichergestellt, dass die aktualisierten Binärdateien jedes Mal in den Ordner kopiert werden, wenn die Lösung neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="12460-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  <span data-ttu-id="12460-252">Ändern `package.manifest.xml` Sie, indem Sie `<desktop:Extension>` dem Element das Element `<Extensions>` hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="12460-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a><span data-ttu-id="12460-253">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="12460-253">Deploying</span></span>  

<span data-ttu-id="12460-254">Nachdem Sie Ihr UWP-Projekt \(und optional Win32-Projekt\) wie oben beschrieben konfiguriert haben, können Sie die Lösung mithilfe von Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="12460-254">Once you have configured your UWP project \(and optionally Win32 project\) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>  

![Build-Inprocess-Projekt](../media/native-message-uwp-debug.png)  

<span data-ttu-id="12460-256">Sobald die Lösung ordnungsgemäß bereitgestellt wurde, sollte Ihre Erweiterung in Microsoft Edge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12460-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>  

![Erweiterung, die in Microsoft Edge angezeigt wird](../media/secureextension.png)  

## <a name="packaging"></a><span data-ttu-id="12460-258">Verpacken</span><span class="sxs-lookup"><span data-stu-id="12460-258">Packaging</span></span>  

> [!NOTE]
> <span data-ttu-id="12460-259">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="12460-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="12460-260">[Senden Sie eine Anforderung,](https://developer.microsoft.com/microsoft-edge/extensions/requests/) teil des Microsoft Store zu sein, und werden Sie für zukünftige Updates in Betracht gezogen.</span><span class="sxs-lookup"><span data-stu-id="12460-260">[Send a request](https://developer.microsoft.com/microsoft-edge/extensions/requests/) to be a part of the Microsoft Store, and be considered for future updates.</span></span>  

<span data-ttu-id="12460-261">Sie können ein Store-Paket für die Übermittlung an das Windows Dev Center mithilfe der integrierten Visual Studio generieren:</span><span class="sxs-lookup"><span data-stu-id="12460-261">You may generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>  

![Erstellen eines Store-Pakets](../media/create-store-package.png)  

## <a name="debugging"></a><span data-ttu-id="12460-263">Debuggen</span><span class="sxs-lookup"><span data-stu-id="12460-263">Debugging</span></span>  

<span data-ttu-id="12460-264">Die Anweisungen zum Debuggen hängen davon ab, welche Komponente Sie testen möchten:</span><span class="sxs-lookup"><span data-stu-id="12460-264">The instructions for debugging vary depending on which component you want to test out:</span></span>  

### <a name="debugging-the-extension"></a><span data-ttu-id="12460-265">Debuggen der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="12460-265">Debugging the extension</span></span>  

<span data-ttu-id="12460-266">Sobald die Lösung bereitgestellt wurde, wird die Erweiterung in Microsoft Edge installiert.</span><span class="sxs-lookup"><span data-stu-id="12460-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span>  <span data-ttu-id="12460-267">Informationen zum [Debuggen](./debugging-extensions.md) einer Erweiterung finden Sie im Debughandbuch.</span><span class="sxs-lookup"><span data-stu-id="12460-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>  

### <a name="debugging-the-uwp-app"></a><span data-ttu-id="12460-268">Debuggen der UWP-App</span><span class="sxs-lookup"><span data-stu-id="12460-268">Debugging the UWP app</span></span>  

<span data-ttu-id="12460-269">Die UWP-App wird gestartet, wenn die Erweiterung versucht, eine Verbindung mit ihr über [systemeigene Messaging-APIs herzustellen.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)</span><span class="sxs-lookup"><span data-stu-id="12460-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="12460-270">Sie müssen die UWP-App nur debuggen, wenn der Prozess gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="12460-270">You must debug the UWP app only once the process starts.</span></span>  <span data-ttu-id="12460-271">Dies kann auf der Seite Eigenschaft des Projekts konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="12460-271">This may be configured using the Property page of the project:</span></span>  

1.  <span data-ttu-id="12460-272">Zeigen Visual Studio sie auf Ihr UWP-App-Projekt, und öffnen Sie das Kontextmenü \(rechtsklicken\)</span><span class="sxs-lookup"><span data-stu-id="12460-272">In Visual Studio, hover on your UWP app project and open the contextual menu \(right-click\)</span></span>  
1.  <span data-ttu-id="12460-273">Eigenschaften **auswählen**</span><span class="sxs-lookup"><span data-stu-id="12460-273">Select **Properties**</span></span>  
1.  <span data-ttu-id="12460-274">Check **Do not launch, but debug my code when it starts**</span><span class="sxs-lookup"><span data-stu-id="12460-274">Check **Do not launch, but debug my code when it starts**</span></span>  
    
    ![Auswählen des Startfelds](../media/native-message-do-not-launch.png)  
    
<span data-ttu-id="12460-276">In Visual Studio Können Sie jetzt Haltepunkte im Code festlegen, an dem Sie debuggen möchten, und dann den Debugger starten, indem Sie F5 drücken.</span><span class="sxs-lookup"><span data-stu-id="12460-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span>  <span data-ttu-id="12460-277">Sobald Sie mit der Erweiterung interagieren, um eine Verbindung mit der UWP-App herzustellen, Visual Studio automatisch an den Prozess anfügen.</span><span class="sxs-lookup"><span data-stu-id="12460-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>  

### <a name="debugging-the-desktop-bridge"></a><span data-ttu-id="12460-278">Debuggen der Desktopbrücke</span><span class="sxs-lookup"><span data-stu-id="12460-278">Debugging the Desktop Bridge</span></span>  

<span data-ttu-id="12460-279">Obwohl es verschiedene Methoden zum Debuggen einer [Desktopbrücke](/windows/msix/desktop/desktop-to-uwp-debug) \(konvertierte Win32-App\) gibt, gilt für diese Szenarien nur die PLMDebug-Option.</span><span class="sxs-lookup"><span data-stu-id="12460-279">Even though there are various [methods for debugging a Desktop Bridge](/windows/msix/desktop/desktop-to-uwp-debug) \(converted Win32 app\), the only one applicable for this scenarios is the PLMDebug option.</span></span>  <span data-ttu-id="12460-280">Sie können der Startfunktion auch Debugcode hinzufügen, um einen bestimmten Zeitraum zu warten, sodass Sie Visual Studio Prozess anfügen können.</span><span class="sxs-lookup"><span data-stu-id="12460-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>  
