---
description: Erfahren Sie, wie Sie Ihr Microsoft Edge-Erweiterungspaket lokalisieren, damit es nach der Veröffentlichung für mehrere Locales bereit ist.
title: Lokalisierung von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, web development, html, css, javascript, developer
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397720"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a><span data-ttu-id="dd9b4-104">Lokalisieren von Microsoft Edge-Erweiterungen für Windows und den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="dd9b4-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="dd9b4-105">In diesem Handbuch wird beschrieben, wie Sie Ihre Microsoft Edge-Erweiterung lokalisieren, sodass sie nach der Veröffentlichung für mehrere Locales bereit ist.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span>  <span data-ttu-id="dd9b4-106">Um Ihre Erweiterung vollständig zu lokalisieren, müssen Sie die Schritte für Windows und den Microsoft Store ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="dd9b4-107">Wenn Sie Ihre Erweiterungsressourcen für Microsoft Edge lokalisieren möchten, erfahren Sie, wie Sie das i18n-Framework im [Internationalisierungshandbuch verwenden.](../internationalization.md)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="dd9b4-108">Wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt, können Sie zu Lokalisieren von Name und Beschreibung [im Microsoft Store springen.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

## <a name="the-localization-process-overview"></a><span data-ttu-id="dd9b4-109">Übersicht über den Lokalisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="dd9b4-109">The localization process overview</span></span>  

<span data-ttu-id="dd9b4-110">Der erste Schritt, um Ihre Erweiterung für eine breite Zielgruppe verfügbar zu machen, besteht in der Konfiguration der [AppxManifest](#configuring-the-appxmanifest) für mehrere Sprachen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span>  <span data-ttu-id="dd9b4-111">Im Microsoft Store zeigt dies Benutzern, welche Sprachen Ihre Erweiterung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span>  <span data-ttu-id="dd9b4-112">Bestimmte Felder im AppxManifest müssen ebenfalls geändert werden, wenn der Name Ihrer Erweiterung in der [Windows-Benutzeroberfläche](#localizing-extension-resources-for-windows-and-the-microsoft-store)und im Microsoft Store lokalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>  

<span data-ttu-id="dd9b4-113">Sobald Ihr AppxManifest konfiguriert ist, [](#creating-json-string-resources) müssen Sie JSON-Zeichenfolgenressourcen für die Sprachen erstellen, die Sie als unterstützt angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span>  <span data-ttu-id="dd9b4-114">Dies erfordert das Erstellen einer Datei für jede Sprache, in der jede Datei alle `.resjson` Benutzeroberflächenzeichenfolgen dieser Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-114">This requires creating a `.resjson` file for each language, where each file has all the UI strings of that language within it.</span></span>  

<span data-ttu-id="dd9b4-115">Nachdem die Dateien für die unterstützten Sprachen erstellt wurden, muss eine `.resjson` [.pri-Ressourcendatei erstellt werden.](#creating-the-resources-file)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-115">After the `.resjson` files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="dd9b4-116">Dies wird mithilfe einer Konfigurationsdatei für das MakePRI-Tool erstellt, das im [Windows 10 SDK enthalten ist.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-116">This will be created by using a configuration file to the MakePRI tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>  

> [!NOTE]
> <span data-ttu-id="dd9b4-117">Wenn Sie nur das Windows 10 SDK herunterladen, um das Tool zu verwenden, können Sie nur die Features Windows SDK Signing Tools for Desktop Apps und Windows SDK for UWP Managed App auswählen, um den Download leichter zu `MakePri.exe` halten. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd9b4-117">If you are only downloading the Windows 10 SDK to use the `MakePri.exe` tool, you can select only the **Windows SDK Signing Tools for Desktop Apps** and **Windows SDK for UWP Managed App** features to keep the download lighter.</span></span>  <span data-ttu-id="dd9b4-118">Das `MakePri.exe` Tool wird in Unterordnern von `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-118">The `MakePri.exe` tool will appear in subfolders of `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0`.</span></span>  

<span data-ttu-id="dd9b4-119">Nachdem Sie Ihre Erweiterung hochgeladen haben, müssen Sie den Namen und die Beschreibung im [Microsoft Store lokalisieren.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

> [!NOTE]
> <span data-ttu-id="dd9b4-120">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="dd9b4-121">**Kontaktieren Sie uns mit** Ihren Anforderungen, Teil des Microsoft Store zu sein, und wir werden Sie für ein zukünftiges Update in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-121">**Reach out to us** with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>  

## <a name="configuring-the-appxmanifest"></a><span data-ttu-id="dd9b4-122">Konfigurieren des AppXManifest</span><span class="sxs-lookup"><span data-stu-id="dd9b4-122">Configuring the AppXManifest</span></span>  

<span data-ttu-id="dd9b4-123">Die Liste Unterstützte Sprachen Ihrer Erweiterung im Microsoft Store wird basierend auf den AppXManifest-Werten generiert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-123">Your extension's Supported languages list in the Microsoft Store is generated based on its AppXManifest values.</span></span>  <span data-ttu-id="dd9b4-124">Diese Liste wird mithilfe des Elements `Resource` angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-124">This list is specified using the `Resource` element.</span></span>  

![App-Details](../../media/language-app-details.png)  

<span data-ttu-id="dd9b4-126">Um die Liste der Sprachen anzugeben, die von Ihrer Erweiterung unterstützt werden, können Sie ein Element im folgenden Format hinzufügen \(Dieses Element zeigt Unterstützung für Englisch, Deutsch und Französisch im `Resource` `Resource` Microsoft Store\):</span><span class="sxs-lookup"><span data-stu-id="dd9b4-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below \(this `Resource` element will show support for English, German, and French in the Microsoft Store\):</span></span>  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

<span data-ttu-id="dd9b4-127">Weitere [Informationen zu den](/windows/uwp/publish/supported-languages) vom Microsoft Store unterstützten Sprachen/Sprachcodes finden Sie unter Unterstützte Sprachen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-127">See [Supported languages](/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>  

<span data-ttu-id="dd9b4-128">Um lokalisierte Zeichenfolgen für alle öffentlich sichtbaren Elemente im AppxManifest anzugeben, müssen Sie einen Ressourcenbezeichner im Format `ms-resource:<resource id>` verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>  

<span data-ttu-id="dd9b4-129">Die folgenden Codeausschnitte machen ein vollständiges AppxManifest.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="dd9b4-130">Die folgenden Werte sollten aus lokalisierten Ressourcendateien abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-130">The following values should be retrieved from localized resource files:</span></span>  

*   <span data-ttu-id="dd9b4-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd9b4-131">Properties\DisplayName</span></span>  
*   <span data-ttu-id="dd9b4-132">Eigenschaften\Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd9b4-132">Properties\Description</span></span>  
*   <span data-ttu-id="dd9b4-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="dd9b4-133">Properties\PublisherDisplayName</span></span>  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   <span data-ttu-id="dd9b4-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd9b4-134">Applications\Application\VisualElements\DisplayName</span></span>  
*   <span data-ttu-id="dd9b4-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="dd9b4-135">Applications\Application\VisualElements\Description</span></span>  
*   <span data-ttu-id="dd9b4-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd9b4-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>  

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

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a><span data-ttu-id="dd9b4-137">Lokalisieren von Erweiterungsressourcen für Windows und den Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="dd9b4-137">Localizing extension resources for Windows and the Microsoft Store</span></span>  

<span data-ttu-id="dd9b4-138">Da Ihr AppxManifest nun für mehrere Sprachen konfiguriert ist, sollten Sie einige wichtige Unterschiede zwischen dem Lokalisieren der Benutzeroberfläche in Ihrer Erweiterung und der Lokalisierung Ihrer Erweiterung für Windows und dem Microsoft Store kennen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="dd9b4-139">Microsoft Edge-Erweiterungen werden zwar nicht außerhalb von Microsoft Edge ausgeführt, die Verwaltung kann jedoch in Windows erfolgen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span>  <span data-ttu-id="dd9b4-140">Beispielsweise können Benutzer ihre Erweiterungen in der Einstellungs-App verwalten:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-140">For example, users can manage their extensions in the Settings app:</span></span>  

![Einstellungs-App](../../media/settings.png)  

<span data-ttu-id="dd9b4-142">Der Name der Erweiterung, die in der App "Einstellungen" in Windows angezeigt wird, stammt aus dem AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span>  <span data-ttu-id="dd9b4-143">Wenn dieser Wert in Englisch hartcodiert ist, wird die englische Version des Namens auf nicht englischen Windows-Geräten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span>  <span data-ttu-id="dd9b4-144">Wenn das Branding Ihrer Erweiterung nur Auf Englisch ist, ist es in Ordnung, sie hartcodiert zu lassen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>  

> [!NOTE]
> <span data-ttu-id="dd9b4-145">Wenn Sie lokalisierte Namen für Ihre Microsoft Edge-Erweiterung in Windows verwenden [](./extensions-in-the-windows-dev-center.md#name-reservation) möchten, stellen Sie sicher, dass die lokalisierten Namen auch verfügbar und reserviert sind, bevor Sie die Änderungen in der AppXManifest-Datei vornehmen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span>  <span data-ttu-id="dd9b4-146">Wenn die Namen nicht reserviert sind, erhalten Sie den folgenden Fehler, wenn Sie das endgültige Paket in Windows Dev Center hochladen:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span>  
> 
> ![Sprachfehler](../../media/language-error.png)  

<span data-ttu-id="dd9b4-148">Die i18n-basierte Lokalisierungsinfrastruktur, die für JavaScript-Erweiterungen definiert ist, gilt nur innerhalb der Microsoft Edge-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>  

<span data-ttu-id="dd9b4-149">Außerhalb von Microsoft Edge, in Windows und im Microsoft Store, basiert das einzige unterstützte Lokalisierungsframework auf dem Lokalisierungsframework für die universelle Windows-Plattform (UWP).</span><span class="sxs-lookup"><span data-stu-id="dd9b4-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>  

<span data-ttu-id="dd9b4-150">Wir unterstützen zwar JSON-basierte Ressourcen für HTML-basierte Windows-Apps, aber das Schema für die JSON-Ressourcen ist nicht mit dem Schema für JavaScript-Erweiterungen definiert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>  

<span data-ttu-id="dd9b4-151">Es folgen die wichtigsten Unterschiede bei [HTML-basierten Windows-Apps:](/previous-versions/windows/apps/hh465228(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="dd9b4-151">The following are the key differences in [HTML based Windows apps](/previous-versions/windows/apps/hh465228(v=win.10)):</span></span>  

*   <span data-ttu-id="dd9b4-152">Ressourcen werden in `.resjson` Dateien anstelle von Dateien `.json` angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-152">Resources are specified in `.resjson` files instead of `.json` files.</span></span>  
*   <span data-ttu-id="dd9b4-153">Die unterstützten Locales sollten in der AppXManifest-Datei angegeben werden, dabei ist das erste Locale das Standard-Locale.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>  
*   <span data-ttu-id="dd9b4-154">HTML-basierte Windows-Apps-Ressourcen verwenden das folgende Schema:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-154">HTML based Windows apps resources use the following schema:</span></span>  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    <span data-ttu-id="dd9b4-155">Das durch einen Unterstrich bezeichnete Name/Wert-Paar sind Kommentare für die entsprechende Zeichenfolgenressource.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>  
*   `.resjson` <span data-ttu-id="dd9b4-156">Dateien werden in Dateien kompiliert, die während der Erstellung `.pri` von AppX-Paketen enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-156">files are compiled into `.pri` files which must be included during AppX package creation.</span></span>  
    
### <a name="creating-json-string-resources"></a><span data-ttu-id="dd9b4-157">Erstellen von JSON-Zeichenfolgenressourcen</span><span class="sxs-lookup"><span data-stu-id="dd9b4-157">Creating JSON string resources</span></span>  

<span data-ttu-id="dd9b4-158">Mit einem konfigurierten AppxManifest und den unterschiedenen i18n- und UWP-Lokalisierungsframeworks können Sie Ihre Ressourcendateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>  

<span data-ttu-id="dd9b4-159">Nur eine Ressourcenzeichenfolge im Manifest gilt für Microsoft Edge-Erweiterungspakete.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span>  <span data-ttu-id="dd9b4-160">Die `DisplayName` Zeichenfolge wird häufig in JavaScript-Erweiterungen lokalisiert und kann problemlos den von Windows erwarteten Dateien zugeordnet `.resjson` werden.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the `.resjson` files that Windows expects.</span></span>  <span data-ttu-id="dd9b4-161">Unter der Annahme, dass dies die einzige Ressource ist, die Sie lokalisieren möchten, finden Sie hier eine Beispieldatei, `.resjson` die erstellt werden sollte:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-161">Assuming that this is the only resource that you would like to localize, here is a sample `.resjson` file that should be created:</span></span>  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

<span data-ttu-id="dd9b4-162">Die Ressourcen-ID in jeder `.resjson` Datei muss mit der ID übereinstimmen, die im AppXManifest verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-162">The resource ID in each `.resjson` file needs to match the ID used in the AppXManifest.</span></span>  <span data-ttu-id="dd9b4-163">Unter Verwendung des `.resjson` obigen Beispielausschnitts sollte der entsprechende AppXManifest-Eintrag folgendes sein:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-163">Using the example `.resjson` snippet above, the corresponding AppXManifest entry should be:</span></span>  

`DisplayName="ms-resource:DisplayName"`  

<span data-ttu-id="dd9b4-164">Jede sprache, die Ihre Erweiterung unterstützt, sollte über eine entsprechende Ressourcendatei verfügen und in der `.resjson` folgenden Ordnerstruktur platziert werden:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-164">Each language that your extension supports should have a corresponding resources `.resjson` file and be placed in the following folder structure:</span></span>  

![Sprachordnerstruktur](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a><span data-ttu-id="dd9b4-166">Erstellen der Ressourcendatei</span><span class="sxs-lookup"><span data-stu-id="dd9b4-166">Creating the resources file</span></span>  

<span data-ttu-id="dd9b4-167">Nachdem Sie alle Dateien erstellt haben, können Sie den Paketressourcenindex `.resjson` \(PRI\) erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-167">Once you've created all your `.resjson` files, you're ready to create your package resource index \(PRI\) file.</span></span>  <span data-ttu-id="dd9b4-168">In dieser Datei werden die Ressourcen für alle unterstützten Sprachen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-168">This file stores the resources for all your supported languages.</span></span>  <span data-ttu-id="dd9b4-169">Dazu können Sie das **MakePRI-Tool** verwenden, das im Windows 10 SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>  

<span data-ttu-id="dd9b4-170">Zuerst müssen Sie die Konfigurationsdatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-170">First you'll need to create the configuration file.</span></span>  <span data-ttu-id="dd9b4-171">Dadurch werden die Standardqualifizierer und die Plattform für die Ressourcen definiert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-171">This defines the default qualifiers and platform for the resources.</span></span>  <span data-ttu-id="dd9b4-172">Erstellen Sie in diesem Beispiel die Standardsprache `English (US)` und die Plattform Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-172">For this example, make the default language `English (US)` and the platform Windows 10.</span></span>  <span data-ttu-id="dd9b4-173">Erstellen Sie dazu eine `priconfig.xml` Datei mit dem folgenden Inhalt in der `[Root folder]` :</span><span class="sxs-lookup"><span data-stu-id="dd9b4-173">To do this, create a `priconfig.xml` file with the following content in the `[Root folder]`:</span></span>  

![priconfig im Ordner](../../media/priconfig.png)  

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

<span data-ttu-id="dd9b4-175">Jetzt können Sie die Konfigurationsdatei und das Tool MakePRI verwenden, um die Datei resources.pri zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span>  <span data-ttu-id="dd9b4-176">In diesem Beispiel ist der Stammspeicherort für das Projekt `[Root folder]` .</span><span class="sxs-lookup"><span data-stu-id="dd9b4-176">For this example, the root location for the project will be `[Root folder]`.</span></span>  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

<span data-ttu-id="dd9b4-177">Sie sollten nun eine resources.pri-Datei im Stammordner haben:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-177">You should now have one resources.pri file in your root folder:</span></span>  

![Ressourcenordner](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a><span data-ttu-id="dd9b4-179">Lokalisieren von Name und Beschreibung im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="dd9b4-179">Localizing name and description in the Microsoft Store</span></span>  

<span data-ttu-id="dd9b4-180">Sobald Sie versuchen, ihr vollständiges, lokalisiertes Paket hochzuladen, erkennt das Windows Dev Center, dass mehrere Sprachen unterstützt werden, und überprüft, ob sie über entsprechende lokalisierte Namen und Beschreibungen für jede Sprache verfügen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span>  <span data-ttu-id="dd9b4-181">Wenn einer der lokalisierten Werte fehlt, wird Ihre Übermittlung blockiert, bis Sie die Werte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>  

<span data-ttu-id="dd9b4-182">Wenn Sie nur einen lokalisierten Namen und eine Beschreibung für den Microsoft Store (und nicht Windows) bereitstellen möchten, können Sie dazu alle lokalisierten Namen für Ihre Erweiterung [reservieren.](./extensions-in-the-windows-dev-center.md#name-reservation)</span><span class="sxs-lookup"><span data-stu-id="dd9b4-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>  

<span data-ttu-id="dd9b4-183">Nachdem Sie zusätzliche lokalisierte Namen reserviert haben, können Sie eine aktualisierte Übermittlung erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-183">Once you've reserved additional localized names, you can create an updated submission.</span></span>  <span data-ttu-id="dd9b4-184">Im Abschnitt Beschreibung können Sie zusätzliche Sprachen für Ihren Microsoft Store-Eintrag verwalten:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>  

![Verwalten von Beschreibungssprachen](../../media/manage-description-languages.png)  

<span data-ttu-id="dd9b4-186">Nachdem Sie weitere Sprachen verwalten ausgewählt **haben,** können Sie auswählen, welche Sprachen Sie Ihrem Microsoft Store-Eintrag hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-186">Once you've selected **Manage additional languages**, you'll get to select which languages you want to add to your Microsoft Store listing.</span></span>  <span data-ttu-id="dd9b4-187">Die neue Sprache wird im **Abschnitt** Beschreibung als zusätzliche **Beschreibungssprache** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-187">The new language will show up as **Additional description language** in the **Description** section.</span></span>  

<span data-ttu-id="dd9b4-188">Sie können auf den einzelnen \*\*\*\* Link im Abschnitt Beschreibung klicken, um einen lokalisierten Namen und eine Beschreibung, Versionshinweise und visuelle Ressourcen für jede Sprache zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-188">You can click on the individual link in the **Description** section to provide a localized name and description, release notes, and visual assets for each language.</span></span>  <span data-ttu-id="dd9b4-189">Die Beschreibung für den Microsoft Store wird nicht aus dem AppXManifest extrahiert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span>  <span data-ttu-id="dd9b4-190">Jede lokalisierte Beschreibung muss manuell im Windows Dev Center eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>  

![Japanische App-Beschreibung](../../media/japanese-app-description.png)  

<span data-ttu-id="dd9b4-192">Nachdem die lokalisierten Beschreibungen übermittelt und die Erweiterung veröffentlicht wurde, wird jedem Benutzer, der auf eine lokalisierte Seite der Erweiterung im Microsoft Store zutritt, die folgende Benutzeroberfläche angezeigt:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>  

![japanischer Windows Store](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a><span data-ttu-id="dd9b4-194">AppxManifest-Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd9b4-194">AppxManifest samples</span></span>  

### <a name="non-localized-appxmanifest"></a><span data-ttu-id="dd9b4-195">Nicht lokalisierte AppxManifest</span><span class="sxs-lookup"><span data-stu-id="dd9b4-195">Non-localized AppxManifest</span></span>  

<span data-ttu-id="dd9b4-196">Das folgende Beispiel zeigt ein AppxManifest, das nicht lokalisiert ist und nur das `en-us` Locale unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-196">The following example shows an AppxManifest that isn't localized, and only supports the `en-us` locale.</span></span>  

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

#### <a name="localized-appxmanifest"></a><span data-ttu-id="dd9b4-197">Lokalisierte AppxManifest</span><span class="sxs-lookup"><span data-stu-id="dd9b4-197">Localized AppxManifest</span></span>  

<span data-ttu-id="dd9b4-198">Dieses AppxManifest-Beispiel ist für acht weitere Locales neben "en-us" lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="dd9b4-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="dd9b4-199">Beachten Sie `ms-resource:<resource id>` die Vorkommen:</span><span class="sxs-lookup"><span data-stu-id="dd9b4-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>  

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
