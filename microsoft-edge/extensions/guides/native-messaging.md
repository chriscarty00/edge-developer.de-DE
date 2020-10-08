---
description: Erfahren Sie, wie Sie mithilfe von systemeigenem Messaging ihre Erweiterung mit einer Begleit UWP-App kommunizieren können.
title: Erweiterungen – systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Native, Messaging, UWP
ms.openlocfilehash: 83f80e112180317c38763225c1cdd015da4238b0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567410"
---
# Systemeigenes Messaging in Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Übersicht über die native Messaging-Architektur

Mit dem Windows 10 Creators-Update können Microsoft Edge-Erweiterungen natives Messaging verwenden, um mit einer Companion-App für die universelle Windows-Plattform (UWP) zu kommunizieren.  Auf hoher Ebene verwenden Microsoft Edge-Erweiterungen dieselben APIs für natives Messaging wie Chrome-und Firefox-Erweiterungen. Der systemeigene Messaging-Host muss jedoch mithilfe der universellen Windows-Plattform implementiert werden.

> [!NOTE]
> Die nachstehende Methode (Herstellen einer Verbindung mit einer UWP-App über AppService) ist der einzige unterstützte Mechanismus zum Aktivieren der Kommunikation zwischen Microsoft-Edge-Erweiterungen und systemeigenen Komponenten. Weitere Informationen dazu, wie Sie die Kommunikation mit Legacy-Win32-Komponenten aktivieren, finden Sie im Abschnitt [Hinzufügen einer Desktop Brücken Komponente](#adding-a-desktop-bridge-component) dieses Handbuchs. 

 Die native Messaging-Architektur von Microsoft Edge nutzt die vorhandene [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API als zugrunde liegende Infrastruktur für die Inter-Process Communication (IPC). UWP-Apps verwenden die `AppService` API, um miteinander zu kommunizieren. Aus diesem Grund können Microsoft Edge-Erweiterungen nun mit UWP-apps kommunizieren.

![systemeigene Messaging Architektur](./../media/native-messaging-architecture.png)


### Zeitpunkt und Zeitpunkt der Verwendung von systemeigenem Messaging

Systemeigene Nachrichten fügen ihrer Erweiterung eine ganz neue Ebene hinzu. Wenn Sie eine UWP-Begleit-App für Ihre Erweiterung implementieren, stehen Ihnen die folgenden Möglichkeiten zur Verfügung:

* Synchronisieren Sie Daten (z. b. Anmeldeinformationen) mit einer Begleit UWP-app.
* Implementieren Sie stärkere Verschlüsselungs-/Entschlüsselungsalgorithmen, die in Web-APIs nicht verfügbar sind.
* Zugriff auf Ressourcen, auf die über Web-APIs nicht zugegriffen werden kann, beispielsweise Hardware-oder USB-Geräte

Es gibt ein paar Fälle, in denen systemeigenes Messaging aufgrund von Sicherheits-oder Richtlinieneinschränkungen nicht verwendet werden kann:

* Ändern von Benutzereinstellungen in Microsoft Edge oder Windows, beispielsweise Ändern des Standardbrowsers oder Suchanbieters.
* Aktionen, die gegen die Microsoft Store-Richtlinien für apps und Erweiterungen verstoßen.
* Übertragen von Daten an den Remoteendpunkt über den systemeigenen Nachrichten Host
* Zulassen, dass andere apps Inhalte herunterladen, die das Erweiterungs Verhalten ändern.

## Demos

Wenn Sie sich ein Bild davon machen möchten, wie eine Microsoft Edge Native Messaging-Erweiterung mit einer Begleit UWP-APP und einer Desktop Brücke aussieht, lesen Sie die Beispiele für [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) und [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) auf GitHub.

### Funktionsweise

Die Microsoft-Komponente "Edge Extension" des Beispiels verwendet das Inhalts Skript, um zu erkennen, wenn ein Benutzerinformationen eingibt, die verschlüsselt werden sollen. Mit der Erweiterung wird diese über systemeigene Nachrichten an die Desktop-Bridge-Komponente kommuniziert. Wenn der Benutzer bereit ist, die Daten zu übermitteln, gibt die Erweiterung einen verschlüsselten Wert zurück an die Website zurück.

> [!NOTE]
> Dieses Beispiel funktioniert nur auf einer Webseite, die benutzerdefinierte Ereignisse verwendet, um mit dem Inhalts Skript der Erweiterung zu kommunizieren. Der Beispielordner enthält eine [HTML-Datei](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) , mit der die Erweiterung getestet werden soll.

In diesem Beispiel wird die UWP-App verwendet, um Antworten von der Desktop Brücke an Microsoft Edge zu übergeben, die dann per Rückruf an die Microsoft Edge-Erweiterung gesendet wird. Während in diesem Beispiel der systemeigene Messaging-Host in der Haupt-app ausgeführt wird, kann er auch als Hintergrundaufgabe ausgeführt werden. Für den Wechsel zwischen den beiden muss das Hintergrundskript der Erweiterung bearbeitet werden, wobei die Zeichenfolge in in geändert wird `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` .

## Chrome vs Microsoft Edge-Implementierung

Während Chrome die Route für die Verwendung von APIs für die Nachrichtenübergabe für Ihre Erweiterungen für die Kommunikation mit Apps verwendet, nutzt Microsoft Edge die [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API, die jetzt Microsoft Edge Extensions-und UWP-Apps für die Kommunikation ermöglicht.

In diesem Abschnitt werden die Unterschiede zwischen der Implementierung von systemeigenem Messaging durch Chrome und Microsoft Edge erläutert.

### Registrierung und Host Manifest
Damit Ihre APP von ihrer Erweiterung als systemeigener Messaging-Host erkannt wird, muss Sie registriert sein.


Bei der [nativen Messaging](https://developer.chrome.com/extensions/nativeMessaging) -Host Registrierung von Chrome muss Ihre APP eine Manifestdatei an einer beliebigen Stelle im Windows-Dateisystem installieren, die die systemeigene Messaginghost Konfiguration definiert.

Das folgende JSON-Beispiel zeigt, wie die Konfigurationsdatei eingerichtet werden kann:

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

Um diese Datei zu installieren, muss die APP:

1. Registrieren Sie die Manifestdatei an einem vordefinierten Speicherort in der Registrierung, in dem die Hostkonfiguration definiert ist:
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     oder
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. Legen Sie den Standardwert für diesen Schlüssel auf den vollständigen Pfad zur Manifestdatei fest, beispielsweise  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




Für Microsoft Edge [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) müssen Sie die UWP-Begleit-app in das gleiche Paket wie Ihre Erweiterung einbeziehen und die [AppService-Erweiterung](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in der Projektdatei angeben, um einen (nativen Messaging-Host) registrieren zu können `Package.appxmanifest` . Die `EntryPoint` `Name` Attribute und können von Ihnen konfiguriert werden:

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


Darüber hinaus müssen Sie die Durchwahl (n) für die Verbindung mit dem Dienst einstellen. Da Microsoft Edge `"allowed_origins"` in seinen AppxManifest keine entsprechende Manifest-Eigenschaft aufweist, muss dies zur Laufzeit von der UWP-App bestimmt und erzwungen werden. Da Microsoft Edge die Verbindung für die Erweiterung herstellt, kann die APP den Namen der paketfamilie des Anrufers nachschlagen, um festzustellen, ob Sie mit Microsoft Edge verbunden sind, um den Anrufer zu kontrollieren oder zu authentifizieren. z.B. 

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



### Nachrichtenversand

Damit eine APP und eine Erweiterung miteinander kommunizieren können, müssen Nachrichten an und von Ihnen gesendet werden.

Chrome-Erweiterungen initiieren eine Nachricht mithilfe der [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API, um eine Nachricht mit einem nicht persistenten Kanal an den systemeigenen Host zu übermitteln. 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

Der erste Parameter ist der Name des systemeigenen Hosts, in dem Chrome in der Registrierung für das Manifest nachschlägt. Das Manifest gibt die exe-Nachricht an, die von Chrome in einem Sandkasten gestartet wird, und die Nachricht wird mithilfe von Std-i/o gesendet. Erweiterungen können auch einen beständigen Kanal mithilfe der `runtime.connectNative` API einrichten, die den Namen des systemeigenen Hosts als einzigen Parameter übernimmt. 

Microsoft Edge verwendet das gleiche Konstrukt wie die native Messaging-API von Chrome, damit Microsoft Edge-Erweiterungen angeben können, mit welchem App-Dienst eine Verbindung hergestellt werden soll. Der erste Parameter in `runtime.sendNativeMessage` gibt den Namen des App-Diensts an. Im Abschnitt [Registrierung und Host Manifest](#registration-and-host-manifest) ist dies `"com.microsoft.inventory"` . Die Microsoft Edge-Erweiterungs Plattform schränkt den systemeigenen Messaging-Host auf eine UWP-App ein, die im gleichen AppX wie die Erweiterung verpackt ist. Dadurch werden alle Sicherheitsrisiken verringert, die mit böswilligen Angriffen einhergehen, die versuchen, Microsoft Edge mit einem anderen Paket Familiennamen zu verbinden, indem Sie Manifest-Einträge manipulieren. 

Dies bedeutet, dass Microsoft Edge neben dem in der API angegebenen Namen denselben Paket Familiennamen wie die Erweiterung verwendet, `AppService` um den Anbieter des App-Diensts eindeutig zu identifizieren.  

> [!NOTE]
> Dies kann nicht einfach vom [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md)konvertiert werden. Alle Erweiterungen, die die Berechtigung angeben, werden `"nativeMessaging"` als obligatorische manuelle Konvertierung für diese Komponente gekennzeichnet.





### Kommunikationsprotokoll

Das Kommunikationsprotokoll für systemeigene Messaging bestimmt, wie Nachrichten vor dem Senden formatiert werden.

Chrome startet jeden systemeigenen Messaging-Host in einem separaten Prozess und kommuniziert mit ihm über die Standardeingabe und die Standardausgabe. Das gleiche Format wird verwendet, um Nachrichten in beide Richtungen zu senden: jede Nachricht wird mit JSON, UTF-8-codiert und mit der 32-Bit-Nachrichtenlänge in der systemeigenen Bytereihenfolge vorangestellt.


Für Microsoft Edge wird die Hintergrundaufgabe/Haupt-APP, die den App-Dienst implementiert, von der Plattform gestartet. Beim Start wird die Methode der Hintergrundaufgabe `Run` aufgerufen:  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```

Wenn Ihre Erweiterung eine Nachricht an Ihre UWP-App sendet, [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) wird das Ereignis ausgelöst. Diese JSON-formatierte Nachricht wird dann in das erste keywert-Paar eines [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) Objekts stringified. :

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

Wenn Ihre UWP-App eine Antwort an Ihre Durchwahl zurücksendet, [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) wird Sie dem Objekt hinzugefügt `ValueSet` . Die `Key` Eigenschaft wird von Microsoft Edge ignoriert, die `Value` Eigenschaft enthält jedoch eine gültige JSON-Zeichenfolge.

### Rückruf

Für Rückrufe verwendet Chrome [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) eine Rückruffunktion, mit der jede asynchrone Antwort vom Senden einer Nachricht verarbeitet werden kann.

Microsoft Edge verwendet die [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) Methode des Objekts [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) , damit die APP ein [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) Objekt wieder an die Erweiterung senden kann.


### Beschränkung der Nachrichtengröße
Nachrichten, die zwischen einer Erweiterung und einer APP hin-und hergesendet werden, weisen für Chrome und Microsoft Edge unterschiedliche Einschränkungen für die Nachrichtengröße auf.

Chrome weist die folgenden Einschränkungen für die Nachrichtengröße auf:
- Grenzwert für einzelne Nachrichten vom systemeigenen Messaging-Host: 1 MB
- Einzige Nachrichtengrenze, die an den systemeigenen Messaging-Host gesendet wird: 4 GB

Für Microsoft Edge ist zwar `AppService` keine Beschränkung der Nachrichtengröße (abhängig vom Arbeitsspeicher) vorhanden, doch Microsoft Edge schützt sich selbst vor Fehlverhalten von systemeigenen apps, indem die folgenden Einschränkungen für die Nachrichtengröße auferlegt werden:
- Beschränkung einzelner Nachrichten von der UWP-App zur Erweiterung: 1 MB
- Beschränkung einzelner Nachrichten von der Erweiterung auf die UWP-App: 100 MB



### Systemeigene Messagingverbindungen

Es gibt zwei Arten von Verbindungen für systemeigene Nachrichten. persistent und nicht persistent.
Eine **dauerhafte** Verbindung ist eine Verbindung, die weiterhin ausgeführt wird, bis der Port zerstört wird. Eine **nicht persistente** Verbindung ist eine Verbindung, die für eine Nachricht gleichzeitig geöffnet und nach der Zustellung geschlossen wird.

#### Permanent

Bei Chrome wird eine dauerhafte Verbindung hergestellt, indem ein Messagingport mithilfe von erstellt wird [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) . Sobald der Port erstellt wurde, startet Chrome einen systemeigenen Messaging-Hostprozess, der bis zum zerstörten Port weiter ausgeführt wird.

Für Microsoft Edge wird nach dem Erstellen eines Messagingports mit `runtime.connectNative` Microsoft Edge das Programm gestartet, [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) und es wird weiterhin ausgeführt, bis der Port zerstört wird. Der folgende Codeausschnitt zeigt, wie eine dauerhafte Verbindung in einer UWP-App hergestellt wird. 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### Nicht persistent

Wenn eine Nachricht mit [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome gesendet wird, ohne einen Messagingport zu erstellen, startet Chrome einen neuen systemeigenen Messaging-Hostprozess für jede Nachricht. Die erste vom Hostprozess generierte Nachricht wird als Antwort auf die ursprüngliche Anforderung verarbeitet, und alle anderen Nachrichten werden ignoriert.

Microsoft Edge beendet die Verbindung, nachdem die Antwort jeder Nachricht empfangen wurde. Der folgende Codeausschnitt zeigt eine nicht persistente Verbindung, die dadurch hergestellt wird `AppServiceConnection` , dass Sie in der UWP-App beendet wird, nachdem eine Anforderung empfangen und als eine gespeichert wurde [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .

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

### Berechtigung

Um die Verwendung der systemeigenen Messagingfunktion mit ihrer Erweiterung zu aktivieren, müssen Sie für Chrome und Microsoft Edge die `"nativeMessaging"` Berechtigung in Ihrer `manifest.json` Datei deklarieren.


## App-Dienste
In diesem Abschnitt werden die Auswirkungen von App-Diensten auf die Microsoft Edge-systemeigene Messagingleistung und den Arbeitsspeicher erläutert.

### Leistung

App-Dienste werden von der Vordergrund-APP, die Sie anruft, "gesponsert", was für systemeigene Messagingzwecke Microsoft Edge ist. Dies bedeutet, dass APP-Dienste ausgeführt werden können, solange Microsoft Edge ausgeführt wird.

In Bezug auf Latenz verwenden App-Dienste Named Pipes, die nach der ersten Verbindung zwei apps direkt kommunizieren lassen. Diese Methode der Kommunikation erzeugt eine niedrige Latenzzeit. Bei Geräten mit langsamen CPUs wird nach dem Starten des Prozesses, der den App-Dienst hostet (~ 80ms zum Starten der Hintergrundaufgabe auf einigen Geräten), eine anfängliche Latenzzeit auftreten. Nach dem Start sollte die Leistung auf langsamen CPU-Geräten gut sein. 


### Arbeitsspeicher
Der einem App-Dienst zugewiesene Arbeitsspeicher wird aus dem für Microsoft Edge zugewiesenen Kontingent herausgenommen. Wenn Microsoft Edge also zu viele APP-Dienste startet, besteht die Möglichkeit, dass Ihnen der Arbeitsspeicher ausgeht. Die üblichen Speicher Caps für Hintergrundaufgaben werden für App-Dienste erzwungen. Auf einem 512 MB-Gerät kann eine APP-Dienst Hintergrundaufgabe beispielsweise nicht größer als 16MB sein. Diese Nummer steigt, wenn die Geräte skaliert werden.


## Erstellen einer Erweiterung mit systemeigenem Messaging

Damit systemeigene Nachrichten getestet werden können, benötigt Ihre Erweiterung einen Paket Familiennamen. Microsoft Edge ermittelt mithilfe dieser Methode die Identität des systemeigenen Nachrichten Hosts, was bedeutet, dass Ihre Erweiterung verpackt werden sollte. 


So erstellen Sie Ihre Erweiterung mit systemeigenem Messaging in Visual Studio:

1. Erstellen Sie ein UWP-Projekt in Visual Studio.
2. [ `AppService` Zu ihrer UWP-app hinzufügen](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).
   - Sie können an dieser Stelle optional [konfigurieren `AppService` , dass Sie in der Haupt-App](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) statt als Hintergrundaufgabe gehostet werden.
3. Erstellen und testen Sie Ihr UWP-Projekt.
   - Optional können Sie eine [Desktop Brücken Komponente](#adding-a-desktop-bridge-component)hinzufügen.
4. Erstellen Sie eine Microsoft Edge-Erweiterung, die systemeigene Nachrichten für die Kommunikation mit der UWP-Begleit-App verwendet. Die Erweiterungsdateien können einem `Extension` im UWP-Projekt benannten Ordner hinzugefügt werden. Alle Dateien unterhalb dieses Ordners, einschließlich Unterordnern, müssen ihre Eigenschaften so konfiguriert haben, dass `Build Action=Content` und `Copy to Output Directory=Copy Always` . Stellen Sie sicher, dass `manifest.json` auch diese Eigenschaften konfiguriert sind.
5. Ändern `package.manifest.xml` Sie die Datei im Projekt so, dass Sie Erweiterungs Metadaten enthält, und konvertieren Sie Sie in eine headless-APP, indem Sie Folgendes hinzufügen `AppListEntry="none"` :

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

6. Verwenden Sie den `AppService` für UWP konfigurierten Namen in den systemeigenen Messaging-APIs.
7. Erstellen und [Bereitstellen](#deploying) des UWP-Projekts (mit der optionalen Desktop Brücken Komponente)
8. [Verpacken](#packaging) der nativen Messaging-Erweiterung, sobald Sie für die Übermittlung an den Store bereit ist

> [!NOTE]
> Verweisen Sie auf den Abschnitt [Demos](#demos) , um ein Beispiel für eine vollständige Native Messaging-Erweiterung zu finden.


## Hinzufügen einer Desktop Brücken Komponente 
Wenn Sie dem Paket eine Desktop Brücken Komponente hinzufügen möchten, müssen Sie Ihr Win32-Projekt in Visual Studio erstellen und erstellen. Informationen dazu, wie Sie Ihre Win32-app in UWP konvertieren, finden Sie unter [Portieren von apps auf Windows 10 über die Desktop-Brücke](/windows/uwp/porting/desktop-to-uwp-root). Nachdem Sie in Visual Studio erstellt haben, können Sie die ausführbare Win32-Datei zum Paket hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Fügen Sie das Win32-Projekt der gleichen Projektmappe wie das UWP-Projekt hinzu. 

2. Das Win32-Projekt als abhängiges Projekt für das UWP-Projekt einrichten:

    ![Einrichten von Projektabhängigkeiten](./../media/project-dependencies.PNG)

3. Erstellen Sie einen `Win32` Ordner im UWP-Projekt. Kopieren Sie die erforderlichen Binärdateien für das `Win32` Projekt in diesen Ordner. Konfigurieren Sie die Eigenschaften aller Binärdateien wie `Build Action=Content` und `Copy to Output Directory=Copy Always` .

    ![Ordner mit Win32-und UWP-APP-Dateien](./../media/desktop-bridge.png)

4. Ändern Sie die UWP-Projektdatei, um alle erforderlichen Binärdateien für das `Win32` Projekt in diesen Ordner mit dem Befehl Postbuild-Ereignis zu kopieren. Dadurch wird sichergestellt, dass die aktualisierten Binärdateien jedes Mal in den Ordner kopiert werden, wenn die Projektmappe neu erstellt wird.

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. Ändern `package.manifest.xml` `<desktop:Extension>` Sie, indem Sie das Element zum Element hinzufügen `<Extensions>` :

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## Bereitstellen
Nachdem Sie Ihr UWP-Projekt (und optional Win32-Projekt) wie oben beschrieben konfiguriert haben, können Sie die Projektmappe mit Visual Studio bereitstellen.

![Erstellen eines InProcess-Projekts](../media/native-message-uwp-debug.PNG)

Nachdem die Lösung richtig bereitgestellt wurde, sollte Ihre Erweiterung in Microsoft Edge angezeigt werden.

![in Microsoft Edge angezeigte Erweiterung](../media/secureextension.png)

## Verpacken

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.


Mit der integrierten Funktionalität von Visual Studio können Sie ein Store-Paket für die Übermittlung an das Windows dev Center generieren:


![Erstellen eines Store-Pakets](../media/create-store-package.PNG)

## Debuggen
Die Anweisungen für das Debuggen variieren je nachdem, welche Komponente Sie testen möchten:

### Debuggen der Erweiterung
Nachdem die Lösung bereitgestellt wurde, wird die Erweiterung in Microsoft Edge installiert. Informationen zum Debuggen einer Erweiterung finden Sie im Leitfaden zur [Fehlerbehebung](./debugging-extensions.md) .


### Debuggen der UWP-App
Die UWP-APP wird gestartet, wenn die Erweiterung versucht, eine Verbindung mit der [systemeigenen Messaging-API](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)herzustellen. Sie müssen die UWP-app nur Debuggen, nachdem der Prozess gestartet wurde. Dies kann über die Eigenschaftenseite des Projekts konfiguriert werden:

1.  Klicken Sie in Visual Studio mit der rechten Maustaste auf das UWP-App-Projekt.
2.  Eigenschaften auswählen
3.  Aktivieren Sie "nicht starten, aber meinen Code beim Starten Debuggen"

    ![Feld "nicht starten" auswählen](../media/native-message-do-not-launch.png)

In Visual Studio können Sie jetzt Haltepunkte im Code festlegen, in dem Sie debuggen möchten, und dann den Debugger starten, indem Sie F5 drücken. Sobald Sie mit der Erweiterung interagieren, um eine Verbindung mit der UWP-App herzustellen, wird Visual Studio automatisch an den Prozess angefügt.


### Debuggen der Desktop Brücke
Obwohl es verschiedene [Methoden zum Debuggen einer Desktop Brücke](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (konvertierte Win32-APP) gibt, ist die einzige Anwendung für diese Szenarien die PLMDebug-Option. Sie können der Startfunktion auch Debugcode hinzufügen, um eine Wartezeit für eine bestimmte Zeit durchzuführen, sodass Sie Visual Studio an den Prozess anfügen können.
