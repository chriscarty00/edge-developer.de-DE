---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Hier erfahren Sie, wie Sie Ihre Microsoft Edge-Erweiterung manuell Verpacken und testen, ob Sie richtig verpackt ist.
title: Erstellen und Testen von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Verpackung
ms.custom: seodec18
ms.openlocfilehash: a76737d76c8f08c8e79992f0804fdbd34d4ed970
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567383"
---
# <span data-ttu-id="f9147-104">Erstellen und Testen eines Microsoft Edge Extension AppX-Pakets</span><span class="sxs-lookup"><span data-stu-id="f9147-104">Creating and testing a Microsoft Edge extension AppX package</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="f9147-105">Microsoft Edge-Erweiterungen sind als AppX verpackt, ähnlich wie universelle Windows-apps verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="f9147-105">Microsoft Edge extensions are packaged as AppX, similar to how Universal Windows Apps are packaged.</span></span> <span data-ttu-id="f9147-106">Ab Windows 10 Anniversary Update wurde ein neues Schema für AppX eingeführt, das es einem AppX ermöglicht, eine Microsoft Edge-Erweiterung als Inhalt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="f9147-106">As of Windows 10 Anniversary Update, a new schema has been introduced for AppX that allows an AppX to include a Microsoft Edge extension as its content.</span></span>

<span data-ttu-id="f9147-107">Wenn Sie bereits wissen, wie Microsoft Edge Extension-AppXs erstellt werden, können Sie die [Verwendung von ManifoldJS zur Paketerweiterung](./using-manifoldjs-to-package-extensions.md) überspringen, um zu erfahren, wie Sie ein auf Node. js basierendes Tool verwenden, um all dies für Sie zu erledigen!</span><span class="sxs-lookup"><span data-stu-id="f9147-107">If you already know how Microsoft Edge extension AppXs are created, you can skip to [Using ManifoldJS to package extension](./using-manifoldjs-to-package-extensions.md) to learn how to use a Node.js based tool to do all of this for you!</span></span>

> [!NOTE]
> <span data-ttu-id="f9147-108">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="f9147-108">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="f9147-109">Nachdem Sie Ihre Erweiterung erstellt, verpackt und getestet haben, senden Sie uns bitte eine Anfrage über unser [Extension-Übermittlungsformular](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="f9147-109">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>



## <span data-ttu-id="f9147-110">Vorbereiten des Übermittlungs Ordners</span><span class="sxs-lookup"><span data-stu-id="f9147-110">Preparing the submission folder</span></span>

<span data-ttu-id="f9147-111">Wenn Sie Ihre Erweiterung für die Übermittlung vorbereiten möchten, müssen Sie einen Ordner mit der folgenden Struktur erstellen:</span><span class="sxs-lookup"><span data-stu-id="f9147-111">To prepare your extension for submission, you need to create a folder with the following structure:</span></span>

![Abbildung der Ordnerstruktur.](./../../media/packaging_folder-structure.png)

<span data-ttu-id="f9147-114">Im Stammverzeichnis des Ordners sollten Sie eine AppXManifest. XML-Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9147-114">At the root of the folder, you should include an AppXManifest.xml file.</span></span> <span data-ttu-id="f9147-115">Diese Datei wird verwendet, um den Inhalt und das Layout des Pakets anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9147-115">This file is used to specify the contents and layout of the package.</span></span>

<span data-ttu-id="f9147-116">Darüber hinaus sollten Sie über einen Ordner "Objekte" verfügen, der die im Microsoft Store zu verwendenden UI-Ressourcen enthält, sowie einen Erweiterungsordner, der die Dateien Ihrer Erweiterung enthält (Skripts, Symbole usw.).</span><span class="sxs-lookup"><span data-stu-id="f9147-116">You should also have an Assets folder which contains the UI assets to be used in the Microsoft Store, and an Extension folder that contains your extension's files (scripts, icons, etc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9147-117">Sie können eine andere Ordnerstruktur für Ihr Paket erstellen, die Ordnerstruktur muss aber den AppXManifest-Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f9147-117">You can create a different folder structure for your package, but the folder structure must match the AppXManifest values.</span></span>

### <span data-ttu-id="f9147-118">AppXManifest. XML</span><span class="sxs-lookup"><span data-stu-id="f9147-118">AppXManifest.xml</span></span>
<span data-ttu-id="f9147-119">Die AppXManifest-Datei ist ein XML-Dokument, das Informationen enthält, die das System benötigt, um eine Windows-App bereitzustellen, anzuzeigen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f9147-119">The AppXManifest file is an XML document that contains info the system needs to deploy, display, or update a Windows app.</span></span> <span data-ttu-id="f9147-120">Diese Datei enthält auch Paketidentität, Funktionen und visuelle Elemente.</span><span class="sxs-lookup"><span data-stu-id="f9147-120">This file also includes package identity, capabilities, and visual elements.</span></span> <span data-ttu-id="f9147-121">Jedes app-Paket muss eine AppXManifest-Datei beinhalten.</span><span class="sxs-lookup"><span data-stu-id="f9147-121">Every app package must include one AppXManifest file.</span></span>

<span data-ttu-id="f9147-122">Entwickler können die folgende Vorlage für Ihre AppXManifest. XML-Datei verwenden:</span><span class="sxs-lookup"><span data-stu-id="f9147-122">Developers can use the following template for their AppXManifest.xml file:</span></span>

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

#### <span data-ttu-id="f9147-123">Werte der APP-Identitäts Vorlage</span><span class="sxs-lookup"><span data-stu-id="f9147-123">App identity template values</span></span>
<span data-ttu-id="f9147-124">Nachdem Sie [den Namen ihrer Erweiterung](./extensions-in-the-windows-dev-center.md#name-reservation) über das Windows dev Center reserviert haben, werden Sie in der Lage sein, die erforderlichen Paket Identitätsinformationen zu finden, die zum Ersetzen der folgenden Werte in AppXManifest. XML erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="f9147-124">Once you've [reserved the name of your extension](./extensions-in-the-windows-dev-center.md#name-reservation) through the Windows Dev Center, you'll be able to find the necessary package identity information needed to replace the following values in AppXManifest.xml:</span></span>

- `Name`
- `Publisher`
- `DisplayName`
- `PublisherDisplayName`

<span data-ttu-id="f9147-125">Mit den folgenden Schritten können Sie auf die Seite der APP-Identität zugreifen:</span><span class="sxs-lookup"><span data-stu-id="f9147-125">You can access your App identity page using the following steps:</span></span>

1. <span data-ttu-id="f9147-126">Navigieren Sie zu [Windows dev Center](https://developer.microsoft.com/windows/).</span><span class="sxs-lookup"><span data-stu-id="f9147-126">Navigate to [Windows Dev Center](https://developer.microsoft.com/windows/).</span></span>
2. <span data-ttu-id="f9147-127">Registrieren Sie sich bei Ihrem Entwicklerkonto.</span><span class="sxs-lookup"><span data-stu-id="f9147-127">Sign in to your developer account.</span></span>
3. <span data-ttu-id="f9147-128">Navigieren Sie zum Dashboard.</span><span class="sxs-lookup"><span data-stu-id="f9147-128">Navigate to the Dashboard.</span></span>
4. <span data-ttu-id="f9147-129">Wählen Sie den Namen der Erweiterung aus.</span><span class="sxs-lookup"><span data-stu-id="f9147-129">Select the name of your extension.</span></span>

   ![Erweiterungsliste](./../../media/select-app.png)
5. <span data-ttu-id="f9147-131">Navigieren Sie zur Seite App-Identität, die sich unter dem Abschnitt App-Verwaltung befindet (nachdem Sie Ihre APP registriert haben).</span><span class="sxs-lookup"><span data-stu-id="f9147-131">Navigate to the App identity page which is under the App management section (after you've registered your app).</span></span>

   ![Seite für die APP-Identität](./../../media/app-identity.png)


<span data-ttu-id="f9147-133">Sie können jetzt die AppXManifest-Vorlage mit Werten auf der Seite "App-Identität" füllen, wie in der Vorlage angegeben:</span><span class="sxs-lookup"><span data-stu-id="f9147-133">You can now populate the AppXManifest template with values from the App identity page, as indicated in the template:</span></span>


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

#### <span data-ttu-id="f9147-134">JSON-Manifest-vorlagenwerte</span><span class="sxs-lookup"><span data-stu-id="f9147-134">JSON manifest template values</span></span>
<span data-ttu-id="f9147-135">Einige Werte in der AppXManifest müssen mit denen übereinstimmen, die im JSON-Manifest definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9147-135">Some values in the AppXManifest need to match those that are defined in the JSON manifest.</span></span> <span data-ttu-id="f9147-136">Aktualisieren Sie die folgenden Werte in appxmanifest. XML auf der Grundlage Ihres JSON-Erweiterungs Manifests:</span><span class="sxs-lookup"><span data-stu-id="f9147-136">Please update the following values in appxmanifest.xml based on your extension JSON manifest:</span></span>

- `Version` <span data-ttu-id="f9147-137">– Dies ist die Version, die im JSON-Manifest ihrer Erweiterung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="f9147-137">- This is the version listed in your extension's JSON manifest.</span></span> <span data-ttu-id="f9147-138">Die Zeichenfolge muss mit dem x. x. x. x-Format übereinstimmen, wobei die letzte Ganzzahl 0 sein muss.</span><span class="sxs-lookup"><span data-stu-id="f9147-138">The string needs to match the X.X.X.X format where the last integer has to be 0.</span></span> <span data-ttu-id="f9147-139">z.B.</span><span class="sxs-lookup"><span data-stu-id="f9147-139">E.g.</span></span> <span data-ttu-id="f9147-140">1.2.3.0</span><span class="sxs-lookup"><span data-stu-id="f9147-140">1.2.3.0</span></span>

   ```xml
   <Identity
     Name="37369abigailc.MyExtension"
     Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
     Version="1.0.0.0" />
   ```

- `Description` <span data-ttu-id="f9147-141">– Dies ist eine Kopie der Beschreibung im JSON-Manifest ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="f9147-141">- This is a copy of the description in your extension's JSON manifest.</span></span>

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


### <span data-ttu-id="f9147-142">Objektordner</span><span class="sxs-lookup"><span data-stu-id="f9147-142">Assets folder</span></span>

<span data-ttu-id="f9147-143">Im Ordner "Objekte" sind drei verschiedene Symbolgrößen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f9147-143">Within the Assets folder you will need three different icon sizes.</span></span> <span data-ttu-id="f9147-144">Diese Symbole werden im Microsoft Store und in der Windows-Benutzeroberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9147-144">These icons will be used in the Microsoft Store and the Windows UI.</span></span> <span data-ttu-id="f9147-145">Weitere Informationen zu diesen Symbolen finden Sie im [Design](./../design.md#icons-for-packaging) Handbuch.</span><span class="sxs-lookup"><span data-stu-id="f9147-145">For more information on these icons, see the [Design](./../design.md#icons-for-packaging) guide.</span></span>

![Ordner "Objekte" mit drei Symbolgrößen](./../../media/assets-folder.png)

<span data-ttu-id="f9147-147">Nachdem Sie die erforderlichen UI-Ressourcen erstellt haben, aktualisieren Sie AppXManifest. XML so, dass Sie auf die richtigen Dateien verweisen:</span><span class="sxs-lookup"><span data-stu-id="f9147-147">Once you've created the necessary UI assets, update AppXManifest.xml to point to the correct files:</span></span>

- <span data-ttu-id="f9147-148">44 x 44</span><span class="sxs-lookup"><span data-stu-id="f9147-148">44x44</span></span>

   ```xml
   Square44x44Logo="Assets/icon_44.png"
   ```

- <span data-ttu-id="f9147-149">50x50</span><span class="sxs-lookup"><span data-stu-id="f9147-149">50x50</span></span>

  ```xml
   <Logo>Assets/icon_50.png</Logo>
  ```

- <span data-ttu-id="f9147-150">150x150</span><span class="sxs-lookup"><span data-stu-id="f9147-150">150x150</span></span>

  ```xml
  Square150x150Logo="Assets/icon_150.png"
  ```


### <span data-ttu-id="f9147-151">Erweiterungsordner</span><span class="sxs-lookup"><span data-stu-id="f9147-151">Extension folder</span></span>
<span data-ttu-id="f9147-152">Kopieren Sie Ihre Erweiterungsdateien (wobei die Ordnerstruktur bleibt) in den Ordner "Erweiterung".</span><span class="sxs-lookup"><span data-stu-id="f9147-152">Copy your extension files (keeping the folder structure) into the Extension folder.</span></span> <span data-ttu-id="f9147-153">Stellen Sie sicher, dass `manifest.json` sich der Ordner "root" befindet.</span><span class="sxs-lookup"><span data-stu-id="f9147-153">Make sure `manifest.json` is at the root your Extension folder.</span></span>

![Erweiterungsordner mit allen Erweiterungsdateien darin](./../../media/extension-folder.png)


### <span data-ttu-id="f9147-155">Unterstützen von mehr als einem Gebietsschema</span><span class="sxs-lookup"><span data-stu-id="f9147-155">Supporting more than one locale</span></span>
<span data-ttu-id="f9147-156">Wenn Ihre Erweiterung mehr als eine Sprache unterstützt, möchten Sie möglicherweise das AppX-Paket mit allen benötigten Gebietsschemas konfigurieren, damit das richtige lokalisierte Symbol und die richtige Beschreibung im Microsoft Store angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9147-156">If your extension supports more than one language, you may want to configure the AppX package with all the locales that you need so that the correct localized icon and description appear in the Microsoft Store.</span></span> <span data-ttu-id="f9147-157">Weitere Informationen finden Sie unter [Lokalisieren von Erweiterungspaketen](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="f9147-157">See [Localizing extension packages](./localizing-extension-packages.md) for more information.</span></span>

### <span data-ttu-id="f9147-158">Erstellen eines AppX</span><span class="sxs-lookup"><span data-stu-id="f9147-158">Creating an Appx</span></span>

<span data-ttu-id="f9147-159">Um eine AppX zu erstellen, müssen Sie den Pfad für makeappx finden.</span><span class="sxs-lookup"><span data-stu-id="f9147-159">To create an Appx, you'll need to find the path for makeappx.</span></span> <span data-ttu-id="f9147-160">Dieser befindet sich normalerweise am folgenden Speicherort, wenn Sie sich auf einem 64-Bit-Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="f9147-160">This is usually located in the following location if you're on a 64-bit machine.</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

<span data-ttu-id="f9147-161">Führen Sie den folgenden Befehl aus, um das AppX-Paket für Ihre Erweiterung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f9147-161">Execute the following command to create the AppX package for your extension:</span></span>

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

<span data-ttu-id="f9147-162">Dies sollte ungefähr wie folgt aussehen, nachdem Sie die Pfade ausgefüllt haben:</span><span class="sxs-lookup"><span data-stu-id="f9147-162">This should look something like this once you've filled in the paths:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### <span data-ttu-id="f9147-163">Entpacken eines AppX</span><span class="sxs-lookup"><span data-stu-id="f9147-163">Unpacking an Appx</span></span>
<span data-ttu-id="f9147-164">Möglicherweise möchten Sie einen zuvor generierten AppX entpacken und als Ausgangspunkt für die nächste Iteration der Erweiterung verwenden oder bestätigen, dass der AppX richtig erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9147-164">You may want to unpack a previously generated AppX and use it as a starting point for the next iteration of your extension or to confirm that the AppX was created correctly.</span></span>

<span data-ttu-id="f9147-165">Dazu können Sie den folgenden Befehl ausführen, um das AppX-Paket Ihrer Microsoft Edge-Erweiterung zu entpacken:</span><span class="sxs-lookup"><span data-stu-id="f9147-165">To do this, you can execute the following command to unpack the AppX package of your Microsoft Edge extension:</span></span>

`[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]`

<span data-ttu-id="f9147-166">Dies sollte in etwa wie folgt aussehen, wenn ausgefüllt:</span><span class="sxs-lookup"><span data-stu-id="f9147-166">This should look something like this when filled out:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"`





## <span data-ttu-id="f9147-167">Testen eines AppX-Pakets</span><span class="sxs-lookup"><span data-stu-id="f9147-167">Testing an AppX package</span></span>

<span data-ttu-id="f9147-168">Sie können Ihr Microsoft Edge Extension AppX-Paket testen, indem Sie es in Microsoft Edge Sideloading.</span><span class="sxs-lookup"><span data-stu-id="f9147-168">You can test your Microsoft Edge extension AppX package by sideloading it in Microsoft Edge.</span></span> <span data-ttu-id="f9147-169">Sideloading das Erweiterungs AppX-Paket ist mit Sideloading einer universellen Windows-App vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="f9147-169">Sideloading the extension AppX package is similar to sideloading a Universal Windows app.</span></span> <span data-ttu-id="f9147-170">Sie müssen ein Zertifikat zum Signieren des Pakets erstellen und dann das Paket zu Windows hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9147-170">You will need to create a certificate for signing the package, and then add the package to Windows.</span></span>

### <span data-ttu-id="f9147-171">Signatur</span><span class="sxs-lookup"><span data-stu-id="f9147-171">Signing</span></span>

<span data-ttu-id="f9147-172">Informationen zum Signieren und Zertifizierungsprozess für Pakete finden Sie unter [Erstellen eines App-Paketsignatur Zertifikats](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) und unter [Signieren eines App-Pakets mit SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9147-172">See [How to create an app package signing certificate](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) and [How to sign an app package using SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) for info on the signing and certification process for packages.</span></span>

> [!NOTE]
> <span data-ttu-id="f9147-173">Sie müssen kein Erweiterungspaket signieren, bevor Sie es an den Microsoft Store übermitteln. der Store-Aufnahmevorgang übernimmt das für Sie!</span><span class="sxs-lookup"><span data-stu-id="f9147-173">You do not need to sign an extension package before submitting it to the Microsoft Store; the Store ingestion process will take care of that for you!</span></span>

<span data-ttu-id="f9147-174">Nachdem Sie das Paket mit dem von Ihnen erstellten Zertifikat signiert haben, wird das Zertifikat für die Bereitstellung von App-Paketen nach wie vor nicht vom lokalen Computer als vertrauenswürdig eingestuft, bis Sie es im Speicher für vertrauenswürdige Zertifikate des lokalen Computers installieren.</span><span class="sxs-lookup"><span data-stu-id="f9147-174">After you've signed the package with the certificate that you created, the certificate is still not trusted by the local machine for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="f9147-175">Dazu können Sie certutil. exe verwenden, das im Lieferumfang von Windows enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f9147-175">You can use Certutil.exe, which comes with Windows to do this.</span></span>

<span data-ttu-id="f9147-176">Wenn Sie Zertifikate mit WindowsCertutil. exe installieren möchten, führen Sie "cmd. exe" als Administrator aus, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="f9147-176">To install certificates with WindowsCertutil.exe, run Cmd.exe as administrator and run the following command:</span></span>

`Certutil -addStore TrustedPeople MyKey.cer`

<span data-ttu-id="f9147-177">Sobald die Zertifikate nicht mehr verwendet werden, sollten Sie Sie entfernen, indem Sie den folgenden Befehl an einer Eingabeaufforderung des Administrators ausführen:</span><span class="sxs-lookup"><span data-stu-id="f9147-177">Once the certificates are no longer in use, it is recommended that you remove them by running the following command from an administrator command prompt:</span></span>

`Certutil -delStore TrustedPeople certID`

<span data-ttu-id="f9147-178">Die CERT-ID ist die fortlaufende Nummer des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="f9147-178">The certID is the serial number of the certificate.</span></span> <span data-ttu-id="f9147-179">Führen Sie zum Ermitteln der Seriennummer des Zertifikats den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="f9147-179">To determine the certificate serial number, run the following command:</span></span>

`Certutil -store TrustedPeople`

### <span data-ttu-id="f9147-180">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="f9147-180">Deploying</span></span>
<span data-ttu-id="f9147-181">Sie können das Microsoft Edge Extension AppX-Paket bereitstellen, indem Sie den folgenden Befehl in PowerShell (als Administrator) ausführen:</span><span class="sxs-lookup"><span data-stu-id="f9147-181">You can deploy the Microsoft Edge Extension AppX package by running the following command in PowerShell (as administrator):</span></span>

`Add-AppxPackage [path to AppX]`

## <span data-ttu-id="f9147-182">Automatisiertes Testen mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="f9147-182">Automated testing with WebDriver</span></span>

<span data-ttu-id="f9147-183">Ab dem Jubiläums Update können Sie Ihre Erweiterung in Microsoft Edge mit WebDriver programmgesteuert querladen und so automatisierte Erweiterungen testen, wenn Microsoft Edge im WebDriver-Modus gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f9147-183">As of the Anniversary Update, you can programmatically sideload your extension in Microsoft Edge with WebDriver, enabling automated testing of extensions when Microsoft Edge is launched in WebDriver mode.</span></span> <span data-ttu-id="f9147-184">Auf diese Weise können Sie automatisierte Tests für alle Erweiterungen einrichten, die Inhalte auf einer Seite manipulieren, und sicherstellen, dass das richtige Verhalten gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f9147-184">This will allow you to set up automated tests for any extension that manipulates content on a page and verify that the correct behavior is exhibited.</span></span>

<span data-ttu-id="f9147-185">Wenn Sie Ihre Erweiterung für automatisierte Tests querladen möchten, müssen Sie den Ordner der Erweiterung unter speichern `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` .</span><span class="sxs-lookup"><span data-stu-id="f9147-185">To sideload your extension for automated testing, you'll need to store your extension's folder under `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\`.</span></span> <span data-ttu-id="f9147-186">Nachdem sich Ihre Erweiterung im `LocalState` Verzeichnis befindet, müssen Sie ein [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) Objekt erstellen und ihm die Funktion hinzufügen `extensionPaths` .</span><span class="sxs-lookup"><span data-stu-id="f9147-186">Once your extension is in the `LocalState` directory, you'll need to create an [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) object, and add the `extensionPaths` capability to it.</span></span> <span data-ttu-id="f9147-187">Der Wert dieser Funktion ist eine Matrix von absoluten Pfaden zu den Erweiterungen (im `LocalState` Verzeichnis), die Sie beim Start von Microsoft Edge im WebDriver-Modus auf Seite laden möchten.</span><span class="sxs-lookup"><span data-stu-id="f9147-187">The value of this capability is an array of absolute paths to the extensions (in the `LocalState` directory) you wish to have side loaded when Microsoft Edge starts in WebDriver mode.</span></span>

<span data-ttu-id="f9147-188">Schauen Sie sich die folgende [C#-Datei](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) an, um ein vollständiges Beispiel für das Laden von Erweiterungen in Microsoft Edge mit WebDriver zu finden.</span><span class="sxs-lookup"><span data-stu-id="f9147-188">Check out the following [C# file](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) for a complete sample on side loading extensions in Microsoft Edge with WebDriver.</span></span>
