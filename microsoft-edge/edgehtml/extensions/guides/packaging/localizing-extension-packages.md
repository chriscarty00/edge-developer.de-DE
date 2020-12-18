---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Erfahren Sie, wie Sie Ihr Microsoft Edge-Erweiterungspaket lokalisieren, damit es bei der Veröffentlichung für mehrere Gebietsschemas bereit ist.
title: Lokalisierung von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cfa85eda47fd71099bb5d201d1cf85992931228c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234153"
---
# <span data-ttu-id="f034f-104">Lokalisieren von Microsoft Edge-Erweiterungen für Windows und den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f034f-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="f034f-105">In diesem Leitfaden wird erläutert, wie Sie Ihre Microsoft Edge-Erweiterung lokalisieren können, damit Sie bei der Veröffentlichung für mehrere Gebietsschemas bereit steht.</span><span class="sxs-lookup"><span data-stu-id="f034f-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span> <span data-ttu-id="f034f-106">Um Ihre Erweiterung vollständig zu lokalisieren, müssen Sie die Schritte für Windows und den Microsoft Store Befolgen.</span><span class="sxs-lookup"><span data-stu-id="f034f-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>

<span data-ttu-id="f034f-107">Wenn Sie Ihre Erweiterungs Ressourcen für Microsoft Edge lokalisieren möchten, erfahren Sie, wie Sie das i18n-Framework im [Internationalisierungs Leit Faden](../internationalization.md)verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f034f-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>


> [!NOTE]
> <span data-ttu-id="f034f-108">Wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt, können Sie [im Microsoft Store mit dem Lokalisieren von Name und Beschreibung](#localizing-name-and-description-in-the-microsoft-store)fortfahren.</span><span class="sxs-lookup"><span data-stu-id="f034f-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>


## <span data-ttu-id="f034f-109">Übersicht über den Lokalisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="f034f-109">The localization process overview</span></span>

<span data-ttu-id="f034f-110">Der erste Schritt zur Verfügbarkeit ihrer Erweiterung für ein breites Publikum besteht darin, die AppxManifest für mehrere Sprachen zu [Konfigurieren](#configuring-the-appxmanifest) .</span><span class="sxs-lookup"><span data-stu-id="f034f-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span> <span data-ttu-id="f034f-111">Im Microsoft Store werden die Benutzer in den von der Erweiterung unterstützten Sprachen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f034f-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span> <span data-ttu-id="f034f-112">Bestimmte Felder in der AppxManifest müssen ebenfalls geändert werden, wenn der Name der Erweiterung [in der Windows-Benutzeroberfläche und im Microsoft Store lokalisiert](#localizing-extension-resources-for-windows-and-the-microsoft-store)werden soll.</span><span class="sxs-lookup"><span data-stu-id="f034f-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>


<span data-ttu-id="f034f-113">Nachdem Ihr AppxManifest konfiguriert wurde, müssen sie JSON- [Zeichenfolgenressourcen](#creating-json-string-resources) für die Sprachen erstellen, die Sie als unterstützt angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f034f-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span> <span data-ttu-id="f034f-114">Dies erfordert das Erstellen einer resjson-Datei für jede Sprache, in der jede Datei alle UI-Zeichenfolgen dieser Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="f034f-114">This requires creating a .resjson file for each language, where each file has all the UI strings of that language within it.</span></span>


<span data-ttu-id="f034f-115">Nachdem die resjson-Dateien für die unterstützten Sprachen erstellt wurden, [muss eine PRI-Ressourcendatei erstellt werden](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="f034f-115">After the .resjson files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="f034f-116">Diese wird mithilfe einer Konfigurationsdatei für das **"makepri** -Tool erstellt, das im Lieferumfang des [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f034f-116">This will be created by using a configuration file to the **MakePRI** tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> 

> [!NOTE]
> <span data-ttu-id="f034f-117">Wenn Sie das Windows 10 SDK nur herunterladen, um das MakePri.exe-Tool zu verwenden, können Sie nur die Features "Windows SDK-Signatur Tools für Desktop-Apps" und "Windows SDK für UWP-verwaltete Apps" auswählen, um das Herunterladen leichter zu halten.</span><span class="sxs-lookup"><span data-stu-id="f034f-117">If you are only downloading the Windows 10 SDK to use the MakePri.exe tool, you can select only the "Windows SDK Signing Tools for Desktop Apps" and "Windows SDK for UWP Managed Apps" features to keep the download lighter.</span></span> <span data-ttu-id="f034f-118">Das MakePri.exe-Tool wird in Unterordnern von C:\Program Files (x86)-Kits\10\bin\10.0.17713.0. angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f034f-118">The MakePri.exe tool will appear in subfolders of C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0.</span></span>


<span data-ttu-id="f034f-119">Nachdem Sie Ihre Erweiterung hochgeladen haben, besteht der letzte Schritt darin, [den Namen und die Beschreibung im Microsoft Store zu lokalisieren](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="f034f-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>

> [!NOTE]
> <span data-ttu-id="f034f-120">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="f034f-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="f034f-121">Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="f034f-121">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>



## <span data-ttu-id="f034f-122">Konfigurieren des AppXManifest</span><span class="sxs-lookup"><span data-stu-id="f034f-122">Configuring the AppXManifest</span></span>

<span data-ttu-id="f034f-123">Die Liste der unterstützten Sprachen der Erweiterung wird im Microsoft Store basierend auf Ihren AppXManifest-Werten generiert.</span><span class="sxs-lookup"><span data-stu-id="f034f-123">Your extension's "Supported languages" list in the Microsoft Store is generated based on its AppXManifest values.</span></span> <span data-ttu-id="f034f-124">Diese Liste wird mit dem `Resource` Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="f034f-124">This list is specified using the `Resource` element.</span></span>


![Einstellungen Bild-Sprache-App-Details](./../../media/language-app-details.png)

<span data-ttu-id="f034f-126">Wenn Sie die Liste der Sprachen angeben möchten, die von der Erweiterung unterstützt werden, können Sie ein `Resource` Element im unten gezeigten Format hinzufügen (dieses `Resource` Element zeigt die Unterstützung für Englisch, Deutsch und Französisch im Microsoft Store):</span><span class="sxs-lookup"><span data-stu-id="f034f-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below (this `Resource` element will show support for English, German, and French in the Microsoft Store):</span></span>

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

<span data-ttu-id="f034f-127">Informationen zu den vom Microsoft Store unterstützten Sprachen/Sprachencodes finden Sie unter [Unterstützte Sprachen](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .</span><span class="sxs-lookup"><span data-stu-id="f034f-127">See [Supported languages](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>


<span data-ttu-id="f034f-128">Um lokalisierte Zeichenfolgen für alle öffentlich sichtbaren Elemente in der AppxManifest anzugeben, müssen Sie einen Ressourcenbezeichner im Format von verwenden `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="f034f-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>

<span data-ttu-id="f034f-129">Die folgenden Snippets machen eine vollständige AppxManifest.</span><span class="sxs-lookup"><span data-stu-id="f034f-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="f034f-130">Die folgenden Werte sollten aus lokalisierten Ressourcendateien abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="f034f-130">The following values should be retrieved from localized resource files:</span></span>

- <span data-ttu-id="f034f-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="f034f-131">Properties\DisplayName</span></span>
- <span data-ttu-id="f034f-132">Properties\Description</span><span class="sxs-lookup"><span data-stu-id="f034f-132">Properties\Description</span></span>
- <span data-ttu-id="f034f-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="f034f-133">Properties\PublisherDisplayName</span></span>


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- <span data-ttu-id="f034f-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="f034f-134">Applications\Application\VisualElements\DisplayName</span></span>
- <span data-ttu-id="f034f-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="f034f-135">Applications\Application\VisualElements\Description</span></span>
- <span data-ttu-id="f034f-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="f034f-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```


## <span data-ttu-id="f034f-137">Lokalisieren von Erweiterungs Ressourcen für Windows und den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f034f-137">Localizing extension resources for Windows and the Microsoft Store</span></span>

<span data-ttu-id="f034f-138">Nachdem Ihr AppxManifest für mehrere Sprachen konfiguriert wurde, gibt es einige wichtige Unterschiede, die Sie kennen sollten, wenn Sie die Benutzeroberfläche in ihrer Erweiterung lokalisieren und ihre Erweiterung für Windows und den Microsoft Store lokalisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f034f-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>

<span data-ttu-id="f034f-139">Während Microsoft Edge-Erweiterungen nicht außerhalb von Microsoft Edge ausgeführt werden, kann die Verwaltung in Windows erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f034f-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span> <span data-ttu-id="f034f-140">Beispielsweise können Benutzer Ihre Erweiterungen in der Einstellungs-APP verwalten:</span><span class="sxs-lookup"><span data-stu-id="f034f-140">For example, users can manage their extensions in the Settings app:</span></span>


![Bild ' Einstellungen '](./../../media/settings.png)



<span data-ttu-id="f034f-142">Der Name der Erweiterung, die in der Einstellungs-APP in Windows angezeigt wird, stammt aus dem AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="f034f-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span> <span data-ttu-id="f034f-143">Wenn dieser Wert in Englisch hart codiert ist, wird die englische Version des Namens auf nicht englischen Windows-Geräten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f034f-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span> <span data-ttu-id="f034f-144">Wenn das Branding Ihrer Erweiterung nur Englisch ist, ist es in Ordnung, Sie hart codiert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="f034f-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>


> [!NOTE]
> <span data-ttu-id="f034f-145">Wenn Sie lokalisierte Namen für Ihre Microsoft Edge-Erweiterung in Windows verwenden möchten, stellen Sie sicher, dass die lokalisierten Namen ebenfalls [verfügbar und reserviert](./extensions-in-the-windows-dev-center.md#name-reservation) sind, bevor Sie die Änderungen in der AppXManifest-Datei vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f034f-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span> <span data-ttu-id="f034f-146">Wenn die Namen nicht reserviert sind, erhalten Sie die folgende Fehlermeldung beim Hochladen des endgültigen Pakets in Windows dev Center:</span><span class="sxs-lookup"><span data-stu-id="f034f-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span></br></br>

![Sprachfehler](./../../media/language-error.png)</br></br>


<span data-ttu-id="f034f-148">Die für JavaScript-Erweiterungen definierte i18n-basierte Lokalisierungs Infrastruktur ist nur innerhalb der Microsoft Edge-Umgebung anwendbar.</span><span class="sxs-lookup"><span data-stu-id="f034f-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>

<span data-ttu-id="f034f-149">Außerhalb von Microsoft Edge, in Windows und im Microsoft Store, basiert das einzige unterstützte Lokalisierungs Framework auf dem Lokalisierungs Framework für die universelle Windows-Plattform (UWP).</span><span class="sxs-lookup"><span data-stu-id="f034f-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>

<span data-ttu-id="f034f-150">Obwohl wir JSON-basierte Ressourcen für HTML-basierte Windows-apps unterstützen, entspricht das Schema für die JSON-Ressourcen nicht dem für JavaScript-Erweiterungen definierten.</span><span class="sxs-lookup"><span data-stu-id="f034f-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>


<span data-ttu-id="f034f-151">Im folgenden finden Sie die wichtigsten Unterschiede in [HTML-basierten Windows-apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span><span class="sxs-lookup"><span data-stu-id="f034f-151">The following are the key differences in [HTML based Windows apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span></span>
-    <span data-ttu-id="f034f-152">Ressourcen werden in resjson-Dateien anstelle von JSON-Dateien angegeben.</span><span class="sxs-lookup"><span data-stu-id="f034f-152">Resources are specified in .resjson files instead of .json files.</span></span>
-    <span data-ttu-id="f034f-153">Die unterstützten Gebietsschemas sollten in der AppXManifest-Datei angegeben werden, wobei das erste Gebietsschema das Standardgebietsschema ist.</span><span class="sxs-lookup"><span data-stu-id="f034f-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>
-    <span data-ttu-id="f034f-154">HTML-basierte Windows-apps-Ressourcen verwenden das folgende Schema:</span><span class="sxs-lookup"><span data-stu-id="f034f-154">HTML based Windows apps resources use the following schema:</span></span>
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    <span data-ttu-id="f034f-155">Das Name-Wert-Paar, das durch einen Unterstrich gekennzeichnet ist, ist ein Kommentar für die entsprechende Zeichenfolgenressource.</span><span class="sxs-lookup"><span data-stu-id="f034f-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>
-    <span data-ttu-id="f034f-156">resjson-Dateien werden in PRI-Dateien kompiliert, die während der AppX-Paketerstellung enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="f034f-156">.resjson files are compiled into .pri files which must be included during AppX package creation.</span></span>


### <span data-ttu-id="f034f-157">Erstellen von JSON-Zeichenfolgenressourcen</span><span class="sxs-lookup"><span data-stu-id="f034f-157">Creating JSON string resources</span></span>
<span data-ttu-id="f034f-158">Mit einem konfigurierten AppxManifest in der Hand und den Unterschieden zwischen den hervorgehobenen i18n-und UWP-Lokalisierungs Frameworks können Sie Ihre Ressourcendateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>

<span data-ttu-id="f034f-159">Nur eine Ressourcenzeichenfolge im Manifest ist auf Microsoft Edge-Erweiterungspakete anwendbar.</span><span class="sxs-lookup"><span data-stu-id="f034f-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span> <span data-ttu-id="f034f-160">Die `DisplayName` Zeichenfolge wird häufig in JavaScript-Erweiterungen lokalisiert und kann problemlos den resjson-Dateien zugeordnet werden, die von Windows erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="f034f-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the .resjson files that Windows expects.</span></span> <span data-ttu-id="f034f-161">Wenn Sie davon ausgehen, dass dies die einzige Ressource ist, die Sie lokalisieren möchten, finden Sie hier eine Beispiel-resjson-Datei, die erstellt werden soll:</span><span class="sxs-lookup"><span data-stu-id="f034f-161">Assuming that this is the only resource that you would like to localize, here is a sample .resjson file that should be created:</span></span>

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

<span data-ttu-id="f034f-162">Die Ressourcen-ID in jeder resjson-Datei muss mit der im AppXManifest verwendeten ID übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f034f-162">The resource ID in each .resjson file needs to match the ID used in the AppXManifest.</span></span> <span data-ttu-id="f034f-163">Mit dem obigen Beispiel. resjson-Snippet sollte der entsprechende AppXManifest-Eintrag wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="f034f-163">Using the example .resjson snippet above, the corresponding AppXManifest entry should be:</span></span>

`DisplayName="ms-resource:DisplayName"`

<span data-ttu-id="f034f-164">Jede Sprache, die von der Erweiterung unterstützt wird, sollte über eine entsprechende Resources. resjson-Datei verfügen und in der folgenden Ordnerstruktur abgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f034f-164">Each language that your extension supports should have a corresponding resources.resjson file and be placed in the following folder structure:</span></span>

![Sprachordner Struktur](./../../media/resources-folder.png)


### <span data-ttu-id="f034f-166">Erstellen der Ressourcendatei</span><span class="sxs-lookup"><span data-stu-id="f034f-166">Creating the resources file</span></span>
<span data-ttu-id="f034f-167">Nachdem Sie alle Ihre resjson-Dateien erstellt haben, können Sie Ihre PRI-Datei (Package Resource Index) erstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-167">Once you've created all your .resjson files, you're ready to create your package resource index (PRI) file.</span></span> <span data-ttu-id="f034f-168">Diese Datei speichert die Ressourcen für alle unterstützten Sprachen.</span><span class="sxs-lookup"><span data-stu-id="f034f-168">This file stores the resources for all your supported languages.</span></span> <span data-ttu-id="f034f-169">Dazu können Sie das **"makepri** -Tool verwenden, das im Lieferumfang des Windows 10 SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f034f-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>


<span data-ttu-id="f034f-170">Zunächst müssen Sie die Konfigurationsdatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-170">First you'll need to create the configuration file.</span></span> <span data-ttu-id="f034f-171">Damit werden die Standardqualifizierer und die Plattform für die Ressourcen definiert.</span><span class="sxs-lookup"><span data-stu-id="f034f-171">This defines the default qualifiers and platform for the resources.</span></span> <span data-ttu-id="f034f-172">Führen Sie in diesem Beispiel die Standardsprache Englisch (USA) und die Plattform Windows 10 aus.</span><span class="sxs-lookup"><span data-stu-id="f034f-172">For this example, make the default language English (US) and the platform Windows 10.</span></span> <span data-ttu-id="f034f-173">Erstellen Sie dazu eine priconfig.xml-Datei mit folgendem Inhalt im [root-Ordner]:</span><span class="sxs-lookup"><span data-stu-id="f034f-173">To do this, create a priconfig.xml file with the following content in the [Root folder]:</span></span>

![priconfig im Ordner](./../../media/priconfig.png)


```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```

<span data-ttu-id="f034f-175">Nun können Sie die Konfigurationsdatei und das "makepri-Tool verwenden, um die Datei" Resources. pri "zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span> <span data-ttu-id="f034f-176">In diesem Beispiel wird der Stammspeicherort für das Projekt [Stammordner] sein.</span><span class="sxs-lookup"><span data-stu-id="f034f-176">For this example, the root location for the project will be [Root folder].</span></span>


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

<span data-ttu-id="f034f-177">Sie sollten nun über eine Datei "Resources. pri" im Stammordner verfügen:</span><span class="sxs-lookup"><span data-stu-id="f034f-177">You should now have one resources.pri file in your root folder:</span></span>

![Ordner "Ressourcen"](./../../media/resources.png)


## <span data-ttu-id="f034f-179">Lokalisieren von Name und Beschreibung im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f034f-179">Localizing name and description in the Microsoft Store</span></span>

<span data-ttu-id="f034f-180">Nachdem Sie das vollständige, lokalisierte Paket hochgeladen haben, wird im Windows dev Center festgestellt, dass mehr als eine Sprache unterstützt wird, und es wird überprüft, ob Sie über entsprechende lokalisierte Namen und Beschreibungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="f034f-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span> <span data-ttu-id="f034f-181">Wenn einer der lokalisierten Werte fehlt, wird ihre Übermittlung blockiert, bis Sie die Werte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>

<span data-ttu-id="f034f-182">Wenn Sie nur einen lokalisierten Namen und eine Beschreibung für den Microsoft Store (und nicht für Windows) bereitstellen möchten, können Sie dies tun, indem Sie [alle lokalisierten Namen für Ihre Erweiterung reservieren](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="f034f-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>


<span data-ttu-id="f034f-183">Nachdem Sie weitere lokalisierte Namen reserviert haben, können Sie eine aktualisierte Übermittlung erstellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-183">Once you've reserved additional localized names, you can create an updated submission.</span></span> <span data-ttu-id="f034f-184">Im Abschnitt Beschreibung können Sie weitere Sprachen für Ihren Microsoft Store-Eintrag verwalten:</span><span class="sxs-lookup"><span data-stu-id="f034f-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>

![Beschreibung der japanischen App – verwalten](./../../media/manage-description-languages.png)

<span data-ttu-id="f034f-186">Nachdem Sie "zusätzliche Sprachen verwalten" ausgewählt haben, können Sie auswählen, welche Sprachen Sie Ihrem Microsoft Store-Eintrag hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f034f-186">Once you've selected "Manage additional languages", you'll get to select which languages you want to add to your Microsoft Store listing.</span></span> <span data-ttu-id="f034f-187">Die neue Sprache wird im Abschnitt "Beschreibung" als "zusätzliche Beschreibungssprache" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f034f-187">The new language will show up as 'Additional description language' in the "Description" section.</span></span>

<span data-ttu-id="f034f-188">Sie können auf den einzelnen Link im Abschnitt "Beschreibung" klicken, um einen lokalisierten Namen und eine Beschreibung, Anmerkungen zur Version und visuelle Ressourcen für jede Sprache bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f034f-188">You can click on the individual link in the "Description" section to provide a localized name and description, release notes, and visual assets for each language.</span></span> <span data-ttu-id="f034f-189">Die Beschreibung für den Microsoft Store wird nicht aus dem AppXManifest extrahiert.</span><span class="sxs-lookup"><span data-stu-id="f034f-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span> <span data-ttu-id="f034f-190">Jede lokalisierte Beschreibung muss manuell in das Windows dev Center eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="f034f-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>

![Beschreibung der japanischen App](./../../media/japanese-app-description.png)

<span data-ttu-id="f034f-192">Sobald die lokalisierten Beschreibungen übermittelt und die Erweiterung veröffentlicht wurde, wird jedem, der auf eine lokalisierte Seite der Erweiterung im Microsoft Store zugreift, die folgende Benutzeroberfläche angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f034f-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>

![japanischer Windows Store](./../../media/japanese-windows-store.png)
 

## <span data-ttu-id="f034f-194">AppxManifest-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f034f-194">AppxManifest samples</span></span>

### <span data-ttu-id="f034f-195">Nicht lokalisierte AppxManifest</span><span class="sxs-lookup"><span data-stu-id="f034f-195">Non-localized AppxManifest</span></span>
<span data-ttu-id="f034f-196">Das folgende Beispiel zeigt eine AppxManifest, die nicht lokalisiert ist, und unterstützt nur das "en-US"-Gebietsschema.</span><span class="sxs-lookup"><span data-stu-id="f034f-196">The following example shows an AppxManifest that isn't localized, and only supports the "en-us" locale.</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```


#### <span data-ttu-id="f034f-197">Lokalisierte AppxManifest</span><span class="sxs-lookup"><span data-stu-id="f034f-197">Localized AppxManifest</span></span>
<span data-ttu-id="f034f-198">Dieses AppxManifest-Beispiel ist für acht andere Gebietsschemas außer "en-US" lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="f034f-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="f034f-199">Beachten Sie die `ms-resource:<resource id>` Vorkommnisse:</span><span class="sxs-lookup"><span data-stu-id="f034f-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```
