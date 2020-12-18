---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Hier erfahren Sie, wie Sie Ihre Microsoft Edge-Erweiterung manuell Verpacken und testen, ob Sie richtig verpackt ist.
title: Erstellen und Testen von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Verpackung
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 44316f4dd47b3b6b26014ff24673ddfd16a72ddb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234160"
---
# Erstellen und Testen eines Microsoft Edge Extension AppX-Pakets  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Microsoft Edge-Erweiterungen sind als AppX verpackt, ähnlich wie universelle Windows-apps verpackt sind. Ab Windows 10 Anniversary Update wurde ein neues Schema für AppX eingeführt, das es einem AppX ermöglicht, eine Microsoft Edge-Erweiterung als Inhalt einzubeziehen.

Wenn Sie bereits wissen, wie Microsoft Edge Extension AppXs erstellt werden, können Sie die [Verwendung von ManifoldJS zur Paketerweiterung](./using-manifoldjs-to-package-extensions.md) überspringen, um zu erfahren, wie Sie ein Node.js basiertes Tool verwenden, um dies alles für Sie zu tun!

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request).

## Vorbereiten des Übermittlungs Ordners

Wenn Sie Ihre Erweiterung für die Übermittlung vorbereiten möchten, müssen Sie einen Ordner mit der folgenden Struktur erstellen:

![Abbildung der Ordnerstruktur. In meinem Erweiterungsordner befindet sich AppxManifest.xml, Ordner "Erweiterung" und "Objekte"](./../../media/packaging_folder-structure.png)

Im Stammverzeichnis des Ordners sollten Sie eine AppXManifest.xml-Datei angeben. Diese Datei wird verwendet, um den Inhalt und das Layout des Pakets anzugeben.

Darüber hinaus sollten Sie über einen Ordner "Objekte" verfügen, der die im Microsoft Store zu verwendenden UI-Ressourcen enthält, sowie einen Erweiterungsordner, der die Dateien Ihrer Erweiterung enthält (Skripts, Symbole usw.).

> [!IMPORTANT]
> Sie können eine andere Ordnerstruktur für Ihr Paket erstellen, die Ordnerstruktur muss aber den AppXManifest-Werten entsprechen.

### AppXManifest.xml
Die AppXManifest-Datei ist ein XML-Dokument, das Informationen enthält, die das System benötigt, um eine Windows-App bereitzustellen, anzuzeigen oder zu aktualisieren. Diese Datei enthält auch Paketidentität, Funktionen und visuelle Elemente. Jedes app-Paket muss eine AppXManifest-Datei beinhalten.

Entwickler können die folgende Vorlage für Ihre AppXManifest.xml Datei verwenden:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
  xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
  xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
  xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
  IgnorableNamespaces="uap3">

  <Identity
    Name="[REPLACE WITH PACKAGE/IDENTITYNAME]"
    Publisher="[REPLACE WITH PACKAGE/IDENTITY/PUBLISHER]"
    Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]"/>

  <Properties>
    <DisplayName>[REPLACE WITH RESERVED STORE NAME]</DisplayName>
    <PublisherDisplayName>[REPLACE WITH PACKAGE/PROPERTIES/PUBLISHERDISPLAYNAME]</PublisherDisplayName>
    <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
  </Properties>

  <Dependencies>
    <TargetDeviceFamily Name="Windows.Desktop"
      MinVersion="10.0.14393.0"
      MaxVersionTested="10.0.14800.0" />
  </Dependencies>

  <Resources>
    <Resource Language="en-us"/>
  </Resources>

  <Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
        DisplayName="[REPLACE WITH RESERVED STORE NAME]"
        Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
        Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
        Description="This is the description of the extension"
        BackgroundColor="white">
      </uap:VisualElements>
    <Extensions>
    <uap3:Extension Category="windows.appExtension">
    <uap3:AppExtension Name="com.microsoft.edge.extension"
        Id="EdgeExtension"
        PublicFolder="Extension"
      DisplayName="[REPLACE WITH RESERVED STORE NAME]">
    </uap3:AppExtension>
    </uap3:Extension>
    </Extensions>
 </Application>
</Applications>
</Package>
```  

#### Werte der APP-Identitäts Vorlage
Nachdem Sie [den Namen ihrer Erweiterung](./extensions-in-the-windows-dev-center.md#name-reservation) über das Windows dev Center reserviert haben, werden Sie in der Lage sein, die erforderlichen Paket Identitätsinformationen zu finden, die zum Ersetzen der folgenden Werte in AppXManifest.xml erforderlich sind:

-   `Name`
-   `Publisher`
-   `DisplayName`
-   `PublisherDisplayName`

Mit den folgenden Schritten können Sie auf die Seite der APP-Identität zugreifen:

1.  Navigieren Sie zu [Windows dev Center](https://developer.microsoft.com/windows/).
2.  Registrieren Sie sich bei Ihrem Entwicklerkonto.
3.  Navigieren Sie zum Dashboard.
4.  Wählen Sie den Namen der Erweiterung aus.
    
    ![Erweiterungsliste](./../../media/select-app.png)
    
5.  Navigieren Sie zur Seite App-Identität, die sich unter dem Abschnitt App-Verwaltung befindet (nachdem Sie Ihre APP registriert haben).
    
    ![Seite für die APP-Identität](./../../media/app-identity.png)
    
Sie können jetzt die AppXManifest-Vorlage mit Werten auf der Seite "App-Identität" füllen, wie in der Vorlage angegeben:

```xml
<Identity
  Name="37369abigailc.MyExtension"
  Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
  Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]" />

<Properties>
  <DisplayName>My Extension</DisplayName>
  <PublisherDisplayName>abigailc</PublisherDisplayName>
  <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
</Properties>
```  

#### JSON-Manifest-vorlagenwerte
Einige Werte in der AppXManifest müssen mit denen übereinstimmen, die im JSON-Manifest definiert sind. Aktualisieren Sie die folgenden Werte in appxmanifest.xml auf Grundlage Ihres JSON-Erweiterungs Manifests:

-   `Version` – Dies ist die Version, die im JSON-Manifest ihrer Erweiterung aufgeführt ist. Die Zeichenfolge muss mit dem x. x. x. x-Format übereinstimmen, wobei die letzte Ganzzahl 0 sein muss. z.B. 1.2.3.0
    
    ```xml
    <Identity
         Name="37369abigailc.MyExtension"
         Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
         Version="1.0.0.0" />
    ```  
    
-   `Description` – Dies ist eine Kopie der Beschreibung im JSON-Manifest ihrer Erweiterung.
    
    ```xml
    <uap:VisualElements
         AppListEntry="none"
         DisplayName="My Extension"
         Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
         Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
         Description="This extension will allow you to quickly print by clicking the browser action."
         BackgroundColor="white">
    </uap:VisualElements>
    ```  
    
### Objektordner

Im Ordner "Objekte" sind drei verschiedene Symbolgrößen erforderlich. Diese Symbole werden im Microsoft Store und in der Windows-Benutzeroberfläche verwendet. Weitere Informationen zu diesen Symbolen finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.

![Ordner "Objekte" mit drei Symbolgrößen](./../../media/assets-folder.png)

Nachdem Sie die erforderlichen UI-Ressourcen erstellt haben, aktualisieren Sie AppXManifest.xml so, dass Sie auf die richtigen Dateien verweisen:

-   44 x 44
    
    ```xml
    Square44x44Logo="Assets/icon_44.png"
    ```  
    
-   50x50
    
    ```xml
    <Logo>Assets/icon_50.png</Logo>
    ```  
    
-   150x150
    
    ```xml
    Square150x150Logo="Assets/icon_150.png"
    ```  
    
### Erweiterungsordner
Kopieren Sie Ihre Erweiterungsdateien (wobei die Ordnerstruktur bleibt) in den Ordner "Erweiterung". Stellen Sie sicher, dass `manifest.json` sich der Ordner "root" befindet.

![Erweiterungsordner mit allen Erweiterungsdateien darin](./../../media/extension-folder.png)

### Unterstützen von mehr als einem Gebietsschema
Wenn Ihre Erweiterung mehr als eine Sprache unterstützt, möchten Sie möglicherweise das AppX-Paket mit allen benötigten Gebietsschemas konfigurieren, damit das richtige lokalisierte Symbol und die richtige Beschreibung im Microsoft Store angezeigt werden. Weitere Informationen finden Sie unter [Lokalisieren von Erweiterungspaketen](./localizing-extension-packages.md) .

### Erstellen eines AppX

Um eine AppX zu erstellen, müssen Sie den Pfad für makeappx finden. Dieser befindet sich normalerweise am folgenden Speicherort, wenn Sie sich auf einem 64-Bit-Computer befinden.

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

Führen Sie den folgenden Befehl aus, um das AppX-Paket für Ihre Erweiterung zu erstellen:

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

Dies sollte ungefähr wie folgt aussehen, nachdem Sie die Pfade ausgefüllt haben:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### Entpacken eines AppX
Möglicherweise möchten Sie einen zuvor generierten AppX entpacken und als Ausgangspunkt für die nächste Iteration der Erweiterung verwenden oder bestätigen, dass der AppX richtig erstellt wurde.

Dazu können Sie den folgenden Befehl ausführen, um das AppX-Paket Ihrer Microsoft Edge-Erweiterung zu entpacken:

```shell
[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]
```  

Dies sollte in etwa wie folgt aussehen, wenn ausgefüllt:

```text
C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"
```  

## Testen eines AppX-Pakets

Sie können Ihr Microsoft Edge Extension AppX-Paket testen, indem Sie es in Microsoft Edge Sideloading. Sideloading das Erweiterungs AppX-Paket ist mit Sideloading einer universellen Windows-App vergleichbar. Sie müssen ein Zertifikat zum Signieren des Pakets erstellen und dann das Paket zu Windows hinzufügen.

### Signatur

Informationen zum Signieren und Zertifizierungsprozess für Pakete finden Sie unter [Erstellen eines App-Paketsignatur Zertifikats](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) und unter [Signieren eines App-Pakets mit SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) .

> [!NOTE]
> Sie müssen kein Erweiterungspaket signieren, bevor Sie es an den Microsoft Store übermitteln. der Store-Aufnahmevorgang übernimmt das für Sie!

Nachdem Sie das Paket mit dem von Ihnen erstellten Zertifikat signiert haben, wird das Zertifikat für die Bereitstellung von App-Paketen nach wie vor nicht vom lokalen Computer als vertrauenswürdig eingestuft, bis Sie es im Speicher für vertrauenswürdige Zertifikate des lokalen Computers installieren. Sie können Certutil.exe verwenden, das im Lieferumfang von Windows enthalten ist.

Wenn Sie Zertifikate mit WindowsCertutil.exe installieren möchten, führen Sie Cmd.exe als Administrator aus, und führen Sie den folgenden Befehl aus:

```shell
Certutil -addStore TrustedPeople MyKey.cer
```  

Sobald die Zertifikate nicht mehr verwendet werden, sollten Sie Sie entfernen, indem Sie den folgenden Befehl an einer Eingabeaufforderung des Administrators ausführen:

```shell
Certutil -delStore TrustedPeople certID
```  

Die CERT-ID ist die fortlaufende Nummer des Zertifikats. Führen Sie zum Ermitteln der Seriennummer des Zertifikats den folgenden Befehl aus:

```shell
Certutil -store TrustedPeople
```  

### Bereitstellen
Sie können das Microsoft Edge Extension AppX-Paket bereitstellen, indem Sie den folgenden Befehl in PowerShell (als Administrator) ausführen:

```powershell
Add-AppxPackage [path to AppX]
```  

## Automatisiertes Testen mit WebDriver

Ab dem Jubiläums Update können Sie Ihre Erweiterung in Microsoft Edge mit WebDriver programmgesteuert querladen und so automatisierte Erweiterungen testen, wenn Microsoft Edge im WebDriver-Modus gestartet wird. Auf diese Weise können Sie automatisierte Tests für alle Erweiterungen einrichten, die Inhalte auf einer Seite manipulieren, und sicherstellen, dass das richtige Verhalten gezeigt wird.

Wenn Sie Ihre Erweiterung für automatisierte Tests querladen möchten, müssen Sie den Ordner der Erweiterung unter speichern `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` . Nachdem sich Ihre Erweiterung im `LocalState` Verzeichnis befindet, müssen Sie ein [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) Objekt erstellen und ihm die Funktion hinzufügen `extensionPaths` . Der Wert dieser Funktion ist eine Matrix von absoluten Pfaden zu den Erweiterungen (im `LocalState` Verzeichnis), die Sie beim Start von Microsoft Edge im WebDriver-Modus auf Seite laden möchten.

Schauen Sie sich die folgende [C#-Datei](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) an, um ein vollständiges Beispiel für das Laden von Erweiterungen in Microsoft Edge mit WebDriver zu finden.
