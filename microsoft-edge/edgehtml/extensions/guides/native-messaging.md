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
# <a name="native-messaging-in-microsoft-edge"></a>Natives Messaging in Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a>Übersicht über die systemeigene Messagingarchitektur  

Mit dem Windows 10 Creators Update können Microsoft Edge-Erweiterungen systemeigenes Messaging verwenden, um mit einer Begleit-App für die universelle Windows-Plattform \(UWP\) zu kommunizieren.  Auf einer hohen Ebene verwenden Microsoft Edge-Erweiterungen dieselben APIs für systemeigene Nachrichten wie Chrome- und Firefox-Erweiterungen.  Der systemeigene Messaginghost muss jedoch mithilfe der universellen Windows-Plattform implementiert werden.  

> [!NOTE]
> Die unten beschriebene Methode \(Herstellen einer Verbindung mit einer UWP-App über AppService\) ist der einzige unterstützte Mechanismus zum Aktivieren der Kommunikation zwischen Microsoft Edge-Erweiterungen und systemeigenen Komponenten.  Weitere Informationen [](#adding-a-desktop-bridge-component) zum Aktivieren der Kommunikation mit älteren Win32-Komponenten finden Sie im Abschnitt Hinzufügen einer Desktopbrücke-Komponente in diesem Handbuch.  

Die systemeigene Messagingarchitektur in Microsoft Edge nutzt die vorhandene API als zugrunde liegende Prozesskommunikation [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\)-Infrastruktur.  UWP-Apps verwenden die `AppService` API, um miteinander zu kommunizieren.  Aus diesem Grund können Microsoft Edge-Erweiterungen jetzt mit UWP-Apps kommunizieren.  

![Systemeigene Messagingarchitektur](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a>Wann und wann systemeigenes Messaging nicht verwendet werden soll  

Natives Messaging fügt Ihrer Erweiterung eine ganz neue Ebene hinzu.  Durch die Implementierung einer UWP-Begleit-App für Ihre Erweiterung stehen Ihnen die folgenden Möglichkeiten zur Verfügung:  

*   Synchronisieren Sie Daten \(z. B. Anmeldeinformationen\) mit einer Begleit-UWP-App.  
*   Implementieren Sie strengere Verschlüsselungs-/Entschlüsselungsalgorithmen, die in Web-APIs nicht verfügbar sind.  
*   Zugreifen auf Ressourcen, auf die nicht über Web-APIs zugegriffen werden kann, z. B. Hardware oder USB-Geräte  

Es gibt einige Instanzen, in denen systemeigenes Messaging aufgrund von Sicherheits- oder Richtlinieneinschränkungen nicht verwendet werden sollte:  

*   Ändern von Benutzereinstellungen in Microsoft Edge oder Windows, z. B. Ändern des Standardbrowsers oder Suchanbieters.  
*   Aktionen, die gegen Microsoft Store-Richtlinien für Apps und Erweiterungen verstoßen.  
*   Übertragen von Daten an den Remoteendpunkt über den systemeigenen Nachrichtenhost.  
*   Zulassen, dass andere Apps Inhalte herunterladen, die das Erweiterungsverhalten ändern.  

## <a name="demos"></a>Demos  

Informationen dazu, wie eine native Microsoft Edge-Messagingerweiterung aussieht, die sowohl eine #A0 als auch eine Desktopbrücke hat, finden Sie in den [Beispielen SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) und [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) auf GitHub.  

### <a name="how-it-works"></a>Funktionsweise  

Die Microsoft Edge-Erweiterungskomponente des Beispiels verwendet ihr Inhaltsskript, um zu erkennen, wann ein Benutzer Informationen eintippt, die verschlüsselt werden sollen.  Die Erweiterung teilt dies der Desktop-Brücke-Komponente über systemeigenes Messaging mit.  Wenn der Benutzer bereit ist, die Daten zu übermitteln, gibt die Erweiterung einen verschlüsselten Wert zurück an die Website zurück.  

> [!NOTE]
> Dieses Beispiel funktioniert nur auf einer Webseite, die benutzerdefinierte Ereignisse verwendet, um mit dem Inhaltsskript der Erweiterung zu kommunizieren.  Der Beispielordner enthält eine [HTML-Datei zum](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) Testen der Erweiterung.  

In diesem Beispiel wird die UWP-App verwendet, um Antworten von der Desktopbrücke an Microsoft Edge zu übergeben, die dann per Rückruf an die Microsoft Edge-Erweiterung gesendet wird.  Während in diesem Beispiel der systemeigene Messaginghost in der Haupt-App ausgeführt wird, kann er auch als Hintergrundaufgabe ausgeführt werden.  Um zwischen den beiden zu wechseln, müssen Sie das Hintergrundskript der Erweiterung bearbeiten und die Zeichenfolge innerhalb in `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` ändern.  

## <a name="chrome-vs-microsoft-edge-implementation"></a>Chrome vs. Microsoft Edge-Implementierung  

Während Chrome die Route der Verwendung von NACHRICHTENübergehenden APIs für ihre Erweiterungen für die Kommunikation mit Apps begeht, verwendet Microsoft Edge die API, mit der microsoft Edge-Erweiterungen und [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) UWP-Apps kommunizieren können.  

In diesem Abschnitt werden die Unterschiede zwischen der Verarbeitung von Chrome und Microsoft Edge mit der nativen Messagingimplementierung erläutert.  

### <a name="registration-and-host-manifest"></a>Registrierung und Hostmanifest  

Damit Ihre App von Ihrer Erweiterung als systemeigener Messaginghost erkannt wird, muss sie registriert werden.  

Für [die Registrierung von nativen](https://developer.chrome.com/extensions/nativeMessaging) Chrome-Messaginghosts muss Ihre App eine Manifestdatei an einer beliebigen Stelle im Windows-Dateisystem installieren, die die systemeigene Messaginghostkonfiguration definiert.  

Das folgende JSON ist ein Beispiel für Einstellungen für die Konfigurationsdatei:  

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

Um diese Datei zu installieren, muss die App:  

1.  Registrieren Sie die Manifestdatei an einem vordefinierten Speicherort in der Registrierung, der die Hostkonfiguration definiert:  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        or  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  Legen Sie den Standardwert dieses Schlüssels auf den vollständigen Pfad zur Manifestdatei fest, z. B. `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

Für Microsoft Edge müssen Sie zum Registrieren eines [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(nativen Messaginghosts\) die UWP-Begleit-App in das gleiche Paket wie ihre Erweiterung einbeigen und die [AppService-Erweiterung](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in der Datei Ihres Projekts `Package.appxmanifest` angeben.  Die `EntryPoint` Attribute und können von Ihnen konfiguriert `Name` werden:  

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

Außerdem müssen Sie festlegen, welche Erweiterungen eine Verbindung mit dem Dienst herstellen dürfen.  Da Microsoft Edge nicht über eine entsprechende Manifesteigenschaft in appxManifest verfügt, muss dies zur Laufzeit von Ihrer `"allowed_origins"` UWP-App bestimmt und erzwungen werden.  Da Microsoft Edge die Verbindung im Namen der Erweiterung aufbaut, sucht die App den Paketfamiliennamen des Anrufers, um zu ermitteln, ob die Durchwahl durch Microsoft Edge verbunden ist, um den Anrufer zu steuern oder zu authentifizieren.  Beispiel:   

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

### <a name="message-sending"></a>Senden von Nachrichten  

Damit eine App und eine Erweiterung miteinander kommunizieren können, müssen Nachrichten an und von ihnen gesendet werden.  

Chrome-Erweiterungen initiieren eine Nachricht mithilfe der API, um eine Nachricht über einen nicht persistenten Kanal an den systemeigenen [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Host zu senden.  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

Der erste Parameter ist der Name des systemeigenen Hosts, nach dem Chrome in der Registrierung für das Manifest sucht.  Das Manifest gibt die EXE an, die Chrome in einem Sandkasten startet, und die Nachricht wird mithilfe von std i/o gesendet.  
Erweiterungen richten auch einen beständigen Kanal mithilfe der API ein, die den Namen des systemeigenen Hosts `runtime.connectNative` als einzigen Parameter verwendet.  

Microsoft Edge verwendet dasselbe Konstrukt wie die systemeigene Messaging-API in Chrome, um Microsoft Edge-Erweiterungen die Angabe zu ermöglichen, mit welchem App-Dienst eine Verbindung hergestellt werden soll.  Der erste Parameter in `runtime.sendNativeMessage` gibt den Namen des App-Diensts an.  Im Abschnitt [Registrierung und Hostmanifest](#registration-and-host-manifest) ist dies `"com.microsoft.inventory"` .  Die Microsoft Edge-Erweiterungsplattform schränkt den systemeigenen Messaginghost auf eine UWP-App ein, die in derselben AppX wie die Erweiterung verpackt ist.  Dadurch werden alle Sicherheitsrisiken im Zusammenhang mit böswilligen Angriffen verringert, die versuchen, Microsoft Edge mit einem anderen Paketfamiliennamen zu verbinden, indem Manifesteinträge manimaniert werden.  

Dies bedeutet, dass Microsoft Edge denselben Paketfamiliennamen wie die Erweiterung neben dem in der API angegebenen Namen verwendet, um den Anbieter des App-Diensts `AppService` eindeutig zu identifizieren.  

> [!NOTE]
> Dies kann nicht einfach vom [Microsoft Edge Extension Toolkit konvertiert werden.](./porting-chrome-extensions.md)  Alle Erweiterungen, die die Berechtigung angibt, werden als erforderlich gekennzeichnet, dass für diese `"nativeMessaging"` Komponente eine manuelle Konvertierung erforderlich ist.  

### <a name="communication-protocol"></a>Kommunikationsprotokoll  

Das Kommunikationsprotokoll für systemeigene Nachrichten bestimmt, wie Nachrichten vor dem Senden formatiert werden.  

Chrome startet jeden systemeigenen Messaginghost in einem separaten Prozess und kommuniziert mit ihm mithilfe von Standardeingaben und Standardausgabe.  Das gleiche Format wird verwendet, um Nachrichten in beide Richtungen zu senden: Jede Nachricht wird mithilfe von JSON serialisiert, UTF-8 codiert und der 32-Bit-Nachrichtenlänge in systemeigener Bytereihenfolge vorangegangen.  

Für Microsoft Edge wird die Hintergrundaufgabe/Haupt-App, die den App-Dienst implementiert, von der Plattform gestartet.  Beim Start wird `Run` die Methode der Hintergrundaufgabe aufgerufen:  

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

Wenn Ihre Erweiterung eine Nachricht an Ihre UWP-App sendet, wird [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) das Ereignis ausgelöst.  Diese JSON-formatierte Nachricht wird dann in das erste KeyValue-Paar eines Objekts [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) stringifiziert.  :  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

Wenn Ihre UWP-App eine Antwort an Ihre Erweiterung zurücksendet, wird dem [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) Objekt eine `ValueSet` hinzugefügt.  Die `Key` Eigenschaft wird von Microsoft Edge ignoriert, die Eigenschaft enthält jedoch eine gültige `Value` JSON-Zeichenfolge.  

### <a name="callback"></a>Rückruf  

Für Rückrufe verwendet Chrome die Funktion, mit der eine Rückruffunktion asynchrone Antworten vom Senden [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) einer Nachricht verarbeiten kann.  

Microsoft Edge verwendet die Methode des Objekts, damit die App ein Objekt zurück an [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) die Erweiterung senden [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) kann.  

### <a name="message-size-limit"></a>Grenzwert für die Nachrichtengröße  

Nachrichten, die zwischen einer Erweiterung und einer App hin- und hergeschickt werden, haben unterschiedliche Einschränkungen für die Nachrichtengröße für Chrome und Microsoft Edge.  

Chrome hat die folgenden Einschränkungen bei der Nachrichtengröße:  

*   Grenzwert für einzelne Nachrichten vom systemeigenen Messaginghost: 1 MB  
*   Grenzwert für einzelne Nachrichten, der an den systemeigenen Messaginghost gesendet wird: 4 GB  

Für Microsoft Edge hat microsoft Edge zwar keine Beschränkung der Nachrichtengröße \(abhängig vom Arbeitsspeicher\), aber Microsoft Edge schützt sich vor fehlgeleiteten nativen Apps, indem die folgenden Größenbeschränkungen für Nachrichten `AppService` gelten:  

*   Grenzwert für einzelne Nachrichten von der UWP-App zur Erweiterung: 1 MB  
*   Grenzwert für einzelne Nachrichten von der Erweiterung auf die UWP-App: 100 MB  

### <a name="native-messaging-connections"></a>Native Messagingverbindungen  

Es gibt zwei Arten von Verbindungen für systemeigenes Messaging. persistent und nicht persistent.  
Eine **dauerhafte** Verbindung ist eine Verbindung, die solange ausgeführt wird, bis der Port zerstört wird.  Eine **nicht dauerhafte** Verbindung ist eine Verbindung, die für eine Nachricht gleichzeitig geöffnet wird und nach der Zustellung geschlossen wird.  

#### <a name="persistent"></a>Permanent  

Für Chrome wird eine dauerhafte Verbindung hergestellt, indem ein Messagingport mithilfe von erstellt [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) wird.  Sobald der Port hergestellt wurde, startet Chrome einen systemeigenen Messaginghostprozess, der ausgeführt wird, bis der Port zerstört wurde.  

Sobald ein Messagingport mit Microsoft Edge erstellt wurde, startet Microsoft Edge den und führt ihn so lange aus, bis `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) der Port zerstört wird.  Der folgende Codeausschnitt zeigt, wie eine dauerhafte Verbindung von einer UWP-App aus hergestellt wird.  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a>Nicht beständig  

Wenn eine Nachricht in Chrome gesendet wird, ohne einen Messagingport zu erstellen, startet Chrome einen neuen systemeigenen Messaginghostprozess [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) für jede Nachricht.  Die erste vom Hostprozess generierte Nachricht wird als Antwort auf die ursprüngliche Anforderung und alle anderen Nachrichten behandelt, nachdem sie ignoriert wurden.  

Microsoft Edge beendet und beendet die Verbindung, nachdem jede Antwort auf jede Nachricht empfangen wurde.  Der folgende Codeausschnitt zeigt eine nicht dauerhafte Verbindung, die mit der hergestellt wird, wird dann innerhalb der UWP-App beendet, nachdem eine Anforderung empfangen und als `AppServiceConnection` gespeichert [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) wurde.  

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

### <a name="permission"></a>Berechtigung  

Um die native Messagingnutzung mit Ihrer Erweiterung zu aktivieren, müssen Sie sowohl für Chrome als auch für Microsoft Edge die `"nativeMessaging"` Berechtigung in Der Datei `manifest.json` deklarieren.  

## <a name="app-services"></a>App-Dienste  

In diesem Abschnitt werden die Auswirkungen von App-Diensten auf die systemeigene Messagingleistung und den Speicher von Microsoft Edge erläutert.  

### <a name="performance"></a>Leistung  

App-Dienste werden von der Vordergrund-App "gesponsert", die sie aufruft, die für systemeigene Messagingzwecke Microsoft Edge ist.  Dies bedeutet, dass App-Dienste so lange ausgeführt werden können, wie Microsoft Edge ausgeführt wird.  

In Bezug auf die Latenz verwenden App-Dienste Benannte Pipes, die nach der ersten Verbindung zwei Apps die direkte Kommunikation ermöglichen.  Diese Kommunikationsmethode erzeugt eine geringe Latenz.  Auf Geräten mit langsamen CPUs wird nach dem Starten des Prozesses, der den #A0 hostet (~80 ms zum Starten der Hintergrundaufgabe auf einigen Geräten\) eine anfängliche Wartezeit auftreten.  Nach dem Start sollte die Leistung auf langsamen CPU-Geräten gut sein.  

### <a name="memory"></a>Arbeitsspeicher  

Der einem App-Dienst zugewiesene Arbeitsspeicher wird aus dem Kontingent für Microsoft Edge herausgenommen.  Wenn Microsoft Edge zu viele App-Dienste startet, besteht die Möglichkeit, dass der Arbeitsspeicher nicht mehr verfügbar ist.  Die üblichen Speicherdeckel für Hintergrundaufgabe werden für App-Dienste erzwungen.  Beispielsweise kann eine Hintergrundaufgabe des App-Diensts auf einem Gerät mit 512 MB nicht größer als 16 MB sein.  Diese Anzahl steigt, wenn die Geräte nach oben skaliert werden.  

## <a name="creating-an-extension-with-native-messaging"></a>Erstellen einer Erweiterung mit systemeigenem Messaging  

Um systemeigenes Messaging zu testen, benötigt Ihre Erweiterung einen Paketfamiliennamen.  Microsoft Edge verwendet dies, um die identität des systemeigenen Nachrichtenhosts zu ermitteln, d. h., Ihre Erweiterung sollte verpackt werden.  

So erstellen Sie Ihre Erweiterung mit systemeigenem Messaging in Visual Studio:  

1.  Erstellen Sie ein UWP-Projekt in Visual Studio.  
1.  [Hinzufügen `AppService` zu Ihrer UWP-App](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).  
    *   Sie können optional konfigurieren, dass sie an diesem Punkt in der [ `AppService` Haupt-App](/windows/uwp/launch-resume/convert-app-service-in-process) statt als Hintergrundaufgabe gehostet werden.  
1.  Erstellen und testen Sie Ihr UWP-Projekt.  
    *   Optional können Sie eine [Desktop-Brücke-Komponente hinzufügen.](#adding-a-desktop-bridge-component)  
1.  Erstellen Sie eine Microsoft Edge-Erweiterung, die systemeigenes Messaging für die Kommunikation mit der UWP-Begleit-App verwendet.  Die Erweiterungsdateien können einem Ordner mit dem Namen `Extension` im UWP-Projekt hinzugefügt werden.  Alle Dateien unter diesem Ordner, einschließlich Unterordner, müssen ihre Eigenschaften so konfiguriert haben, dass und `Build Action=Content` `Copy to Output Directory=Copy Always` .  Stellen Sie `manifest.json` sicher, dass diese Eigenschaften ebenfalls konfiguriert sind.  
1.  Ändern Sie die Datei im Projekt, um Erweiterungsmetadaten zu enthalten, und konvertieren Sie sie in eine kopflose `package.manifest.xml` App, indem Sie `AppListEntry="none"` folgendes hinzufügen:  
    
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
    
1.  Verwenden Sie `AppService` den für die UWP konfigurierten Namen in den systemeigenen Messaging-APIs.  
1.  Erstellen und [Bereitstellen des](#deploying) UWP-Projekts \(mit der optionalen Desktop bridge-Komponente\).  
1.  [Packen](#packaging) Sie Ihre systemeigene Messagingerweiterung, sobald sie für die Store-Übermittlung bereit ist.  
    
> [!NOTE]
> Verweisen Sie [auf den Abschnitt Demos,](#demos) um ein Beispiel für eine vollständige systemeigene Messagingerweiterung zu finden.  

## <a name="adding-a-desktop-bridge-component"></a>Hinzufügen einer Desktopbrücke-Komponente  

Wenn Sie Ihrem Paket eine Desktop-Brücke-Komponente hinzufügen möchten, müssen Sie Ihr Win32-Projekt in einem Visual Studio.  Informationen zum Konvertieren Ihrer win32-App in UWP finden Sie unter Portieren von Apps zu [Windows 10 über desktop bridge](/windows/uwp/porting/desktop-to-uwp-root).  Nach der Visual Studio können Sie dem Paket die ausführbare Datei Win32 hinzufügen, indem Sie die folgenden Schritte ausführen:  

1.  Fügen Sie das Win32-Projekt derselben Lösung wie das UWP-Projekt hinzu.  
1.  Legen Sie das Win32-Projekt als abhängiges Projekt für das UWP-Projekt ein:  
    
    ![Einrichten von Projektabhängigkeiten](../media/project-dependencies.png)  
    
1.  Erstellen Sie `Win32` einen Ordner innerhalb des UWP-Projekts.  Kopieren Sie die erforderlichen Binärdateien für `Win32` das Projekt in diesen Ordner.  Konfigurieren Sie die Eigenschaften aller Binärdateien so, dass `Build Action=Content` und `Copy to Output Directory=Copy Always` .  
    
    ![Ordner mit win32- und UWP-App-Dateien](../media/desktop-bridge.png)  
    
1.  Ändern Sie die UWP-Projektdatei, um alle erforderlichen Binärdateien für das Projekt mithilfe des PostBuild-Ereignisbefehls in diesen `Win32` Ordner zu kopieren.  Dadurch wird sichergestellt, dass die aktualisierten Binärdateien jedes Mal in den Ordner kopiert werden, wenn die Lösung neu erstellt wird.  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  Ändern `package.manifest.xml` Sie, indem Sie `<desktop:Extension>` dem Element das Element `<Extensions>` hinzufügen:  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a>Bereitstellen  

Nachdem Sie Ihr UWP-Projekt \(und optional Win32-Projekt\) wie oben beschrieben konfiguriert haben, können Sie die Lösung mithilfe von Visual Studio.  

![Build-Inprocess-Projekt](../media/native-message-uwp-debug.png)  

Sobald die Lösung ordnungsgemäß bereitgestellt wurde, sollte Ihre Erweiterung in Microsoft Edge angezeigt werden.  

![Erweiterung, die in Microsoft Edge angezeigt wird](../media/secureextension.png)  

## <a name="packaging"></a>Verpacken  

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.  [Senden Sie eine Anforderung,](https://developer.microsoft.com/microsoft-edge/extensions/requests/) teil des Microsoft Store zu sein, und werden Sie für zukünftige Updates in Betracht gezogen.  

Sie können ein Store-Paket für die Übermittlung an das Windows Dev Center mithilfe der integrierten Visual Studio generieren:  

![Erstellen eines Store-Pakets](../media/create-store-package.png)  

## <a name="debugging"></a>Debuggen  

Die Anweisungen zum Debuggen hängen davon ab, welche Komponente Sie testen möchten:  

### <a name="debugging-the-extension"></a>Debuggen der Erweiterung  

Sobald die Lösung bereitgestellt wurde, wird die Erweiterung in Microsoft Edge installiert.  Informationen zum [Debuggen](./debugging-extensions.md) einer Erweiterung finden Sie im Debughandbuch.  

### <a name="debugging-the-uwp-app"></a>Debuggen der UWP-App  

Die UWP-App wird gestartet, wenn die Erweiterung versucht, eine Verbindung mit ihr über [systemeigene Messaging-APIs herzustellen.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)  Sie müssen die UWP-App nur debuggen, wenn der Prozess gestartet wird.  Dies kann auf der Seite Eigenschaft des Projekts konfiguriert werden:  

1.  Zeigen Visual Studio sie auf Ihr UWP-App-Projekt, und öffnen Sie das Kontextmenü \(rechtsklicken\)  
1.  Eigenschaften **auswählen**  
1.  Check **Do not launch, but debug my code when it starts**  
    
    ![Auswählen des Startfelds](../media/native-message-do-not-launch.png)  
    
In Visual Studio Können Sie jetzt Haltepunkte im Code festlegen, an dem Sie debuggen möchten, und dann den Debugger starten, indem Sie F5 drücken.  Sobald Sie mit der Erweiterung interagieren, um eine Verbindung mit der UWP-App herzustellen, Visual Studio automatisch an den Prozess anfügen.  

### <a name="debugging-the-desktop-bridge"></a>Debuggen der Desktopbrücke  

Obwohl es verschiedene Methoden zum Debuggen einer [Desktopbrücke](/windows/msix/desktop/desktop-to-uwp-debug) \(konvertierte Win32-App\) gibt, gilt für diese Szenarien nur die PLMDebug-Option.  Sie können der Startfunktion auch Debugcode hinzufügen, um einen bestimmten Zeitraum zu warten, sodass Sie Visual Studio Prozess anfügen können.  
