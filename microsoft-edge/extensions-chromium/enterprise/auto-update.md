---
description: Informationen zu automatischen Updates für Erweiterungen in Microsoft Edge
title: Automatisches Aktualisieren von Erweiterungen in Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: d9901f9c39dabfab111eb7e0c34a3e267a317110
ms.sourcegitcommit: 59d8043e37b89da814f63bc85daf84e0e7167eab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "11586388"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="automatically-update-extensions-in-microsoft-edge"></a><span data-ttu-id="5f4ab-104">Automatisches Aktualisieren von Erweiterungen in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5f4ab-104">Automatically update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="5f4ab-105">Wenn Sie festlegen, dass Ihre Erweiterung automatisch aktualisiert wird, werden die folgenden Vorteile für Microsoft Edge, wenn sie auf automatische Aktualisierung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-105">When you set your extension to automatically update, your extension shares the following benefits with Microsoft Edge when set to automatically update.</span></span>  

*   <span data-ttu-id="5f4ab-106">Integrieren sie Fehler- und Sicherheitsbehebungen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="5f4ab-107">Fügen Sie neue Features oder Leistungsverbesserungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="5f4ab-108">Verbessern Sie die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-108">Improve the user interface.</span></span>  

<span data-ttu-id="5f4ab-109">Zuvor wurden nicht speicherbasierte Erweiterungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-109">Previously, non-store based extensions were supported.</span></span>  <span data-ttu-id="5f4ab-110">Außerdem haben Sie die systemeigenen Binärdateien und die Erweiterung gleichzeitig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-110">Also, you updated the native binaries and the extension at the same time.</span></span>  

<span data-ttu-id="5f4ab-111">Jetzt hostet Microsoft Edge Add-Ons-Speicher Ihre Erweiterungen, und Sie aktualisieren Ihre Erweiterung mit demselben Mechanismus wie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-111">Now, the Microsoft Edge Add-ons store hosts your extensions and you update your extension using the same mechanism as Microsoft Edge.</span></span>  <span data-ttu-id="5f4ab-112">Sie steuern den Updatemechanismus nicht.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-112">You don't control the update mechanism.</span></span>  <span data-ttu-id="5f4ab-113">Seien Sie vorsichtig, wenn Sie Erweiterungen aktualisieren, die von systemeigenen Binärdateien abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-113">Be careful when you update extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f4ab-114">Dieser Artikel gilt nicht für Erweiterungen, die Sie mit dem [Partner Center-Dashboard][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-114">This article does not apply to extensions that you publish using the [Partner Center][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] dashboard.</span></span>  <span data-ttu-id="5f4ab-115">Sie können das Dashboard verwenden, um aktualisierte Versionen für Ihre Benutzer und für den Microsoft Edge-Add-Ons-Speicher zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-115">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="5f4ab-116">Weitere Informationen finden Sie unter [Aktualisieren oder Entfernen der Erweiterung.][ExtensionsPublishUpdateExtension]</span><span class="sxs-lookup"><span data-stu-id="5f4ab-116">For more information, navigate to [Update or remove your extension][ExtensionsPublishUpdateExtension].</span></span>  

## <a name="overview"></a><span data-ttu-id="5f4ab-117">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5f4ab-117">Overview</span></span>  

<span data-ttu-id="5f4ab-118">Alle paar Stunden überprüft Microsoft Edge, ob jede installierte Erweiterung oder App über eine Update-URL verfügt.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-118">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="5f4ab-119">Verwenden Sie das Feld im Manifest, um eine Update-URL für Ihre `update_url` Erweiterung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-119">To specify an update URL for your extension, use the `update_url` field in the manifest.</span></span>  <span data-ttu-id="5f4ab-120">Das `update_url` Feld im Manifest zeigt auf einen Speicherort, um eine Aktualisierungsprüfung zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-120">The `update_url` field in the manifest points to a location to complete an update check.</span></span>  <span data-ttu-id="5f4ab-121">Für jeden `update_url` sendet er Anforderungen für aktualisierte Manifest-XML-Dateien.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-121">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="5f4ab-122">Wenn in der Updatemanifest-XML-Datei eine neuere Version als die installierte aufgeführt ist, Microsoft Edge die neuere Version heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-122">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="5f4ab-123">Der gleiche Prozess funktioniert für manuelle Updates, bei denen die neue Datei mit demselben privaten Schlüssel wie die aktuell installierte `.crx` Version signiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-123">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f4ab-124">Um den Datenschutz der Benutzer zu gewährleisten, sendet Microsoft Edge keine Kopfzeilen mit Manifestanforderungen für automatische Updates und ignoriert alle Kopfzeilen in den Antworten auf `Cookie` `Set-Cookie` diese Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-124">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="5f4ab-125">Update-URL</span><span class="sxs-lookup"><span data-stu-id="5f4ab-125">Update URL</span></span>  

<span data-ttu-id="5f4ab-126">Wenn Sie Ihre eigene Erweiterung oder App hosten, müssen Sie der Datei `update_url` das Feld `manifest.json` hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-126">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="5f4ab-127">Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel für `update_url` .</span><span class="sxs-lookup"><span data-stu-id="5f4ab-127">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="5f4ab-128">Aktualisiertes Manifest</span><span class="sxs-lookup"><span data-stu-id="5f4ab-128">Updated manifest</span></span>  

<span data-ttu-id="5f4ab-129">Das aktualisierte Manifest, das vom Server zurückgegeben wird, sollte ein XML-Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-129">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="5f4ab-130">Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel der aktualisierten Manifest-XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-130">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="5f4ab-131">In der folgenden Tabelle werden die Attribute der aktualisierten Manifest-XML-Datei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-131">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="5f4ab-132">Attribut</span><span class="sxs-lookup"><span data-stu-id="5f4ab-132">Attribute</span></span> | <span data-ttu-id="5f4ab-133">Details</span><span class="sxs-lookup"><span data-stu-id="5f4ab-133">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="5f4ab-134">Die Erweiterungs-ID wird basierend auf einem Hash des öffentlichen Schlüssels generiert.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-134">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="5f4ab-135">Um die ID einer Erweiterung zu finden, öffnen Sie Microsoft Edge, und navigieren Sie zu `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="5f4ab-135">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="5f4ab-136">Eine URL zur `.crx` Datei.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-136">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="5f4ab-137">Dieser Attributwert wird von Microsoft Edge verwendet, um zu bestimmen, ob die `.crx` durch angegebene Datei heruntergeladen werden `codebase` soll.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-137">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="5f4ab-138">Es sollte mit dem Wert `version` in der Datei der Datei `manifest.json` `.crx` übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-138">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="5f4ab-139">Die Updatemanifest-XML-Datei kann Informationen zu mehreren Erweiterungen enthalten, indem mehrere Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-139">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="5f4ab-140">Testen</span><span class="sxs-lookup"><span data-stu-id="5f4ab-140">Testing</span></span>  

<span data-ttu-id="5f4ab-141">Die Standardhäufigkeit der Aktualisierungsprüfung beträgt mehrere Stunden.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-141">The default update check frequency is several hours.</span></span>  <span data-ttu-id="5f4ab-142">Um ein Update zu erzwingen, navigieren Sie zu `edge://extensions` und wählen Sie die Schaltfläche Erweiterungen **jetzt** aktualisieren aus.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-142">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="5f4ab-143">Erweiterte Verwendung: Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="5f4ab-143">Advanced usage: request parameters</span></span>  

<span data-ttu-id="5f4ab-144">Der grundlegende Mechanismus ist einfach.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-144">The basic mechanism is simple.</span></span>  <span data-ttu-id="5f4ab-145">Führen Sie die folgenden Aktionen aus, um Die Erweiterung automatisch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-145">To automatically update your extension, complete the following actions.</span></span>  

1.  <span data-ttu-id="5f4ab-146">Hochladen Ihre statische XML-Datei auf Dem Webserver, z. B. Apache.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-146">Upload your static XML file on your web server, such as Apache.</span></span>  
1.  <span data-ttu-id="5f4ab-147">Aktualisieren Sie die XML-Datei, wenn Sie neue Versionen Ihrer Erweiterungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-147">Update the XML file as you release new versions of your extensions.</span></span>  
    
<span data-ttu-id="5f4ab-148">Nutzen Sie die Tatsache, dass einige Parameter, die der Updatemanifestanforderung hinzugefügt wurden, die Erweiterung und `ID` `version` angeben.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-148">Take advantage of the fact that some parameters added to the update manifest request indicate the extension `ID` and `version`.</span></span>  <span data-ttu-id="5f4ab-149">Sie können dasselbe für alle Erweiterungen anstelle einer `update URL` statischen XML-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-149">You may use the same `update URL` for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="5f4ab-150">Um dasselbe für alle Erweiterungen zu verwenden, zeigen Sie auf eine URL, auf der dynamischer serverseitiger Code ausgeführt wird, `update URL` um die Parameter zu testen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-150">To use the same `update URL` for all your extensions, point to a URL that runs dynamic server-side code to test the parameters.</span></span>  

<span data-ttu-id="5f4ab-151">Im folgenden Beispiel wird das Format der Anforderungsparameter der Update-URL veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-151">The following example demonstrates the format of the request parameters of update URL.</span></span>  

```url
?x={extension_data}
```  

<span data-ttu-id="5f4ab-152">In diesem Beispiel `{extension_data}` handelt es sich um eine URL-codierte Zeichenfolge, die das folgende Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-152">In this example, `{extension_data}` is a URL-encoded string that uses the following format.</span></span>  

```url
id={id}&v={version}
```  

<span data-ttu-id="5f4ab-153">Die folgenden beiden Erweiterungen verweisen beispielsweise beide auf die gleiche Update-URL `http://contoso.com/extension_updates.php` .</span><span class="sxs-lookup"><span data-stu-id="5f4ab-153">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*   <span data-ttu-id="5f4ab-154">Erweiterung 1</span><span class="sxs-lookup"><span data-stu-id="5f4ab-154">Extension 1</span></span>  
    *   <span data-ttu-id="5f4ab-155">ID:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-155">ID:</span></span> `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   <span data-ttu-id="5f4ab-156">Update-URL:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-156">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="5f4ab-157">Version:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-157">Version:</span></span> `1.1`  
*   <span data-ttu-id="5f4ab-158">Erweiterung 2</span><span class="sxs-lookup"><span data-stu-id="5f4ab-158">Extension 2</span></span>  
    *   <span data-ttu-id="5f4ab-159">ID:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-159">ID:</span></span> `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   <span data-ttu-id="5f4ab-160">Update-URL:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-160">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="5f4ab-161">Version:</span><span class="sxs-lookup"><span data-stu-id="5f4ab-161">Version:</span></span> `0.4`  


<span data-ttu-id="5f4ab-162">Im Folgenden sind die Anforderungen zum Aktualisieren jeder Erweiterung zu finden.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-162">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="5f4ab-163">Sie können auch mehrere Erweiterungen in einer einzigen Anforderung für jede eindeutige Update-URL auflisten.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-163">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="5f4ab-164">Im folgenden Beispiel werden die vorherigen Anforderungen in einer einzigen Anforderung zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-164">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="5f4ab-165">Wenn Sie eine einzelne Anforderung senden und die Anzahl der installierten Erweiterungen, die dieselbe Update-URL verwenden, zu lang ist, werden bei der Updateüberprüfung weitere Anforderungen `GET` gestellt.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-165">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="5f4ab-166">Eine `GET` Anforderungs-URL ist zu lang, wenn sie ungefähr 2000 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-166">A `GET` request URL is too long if it's approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f4ab-167">In Zukunft kann eine einzelne `POST` Anforderung mehrere Anforderungen `GET` ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-167">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="5f4ab-168">Die `POST` Anforderung kann die Anforderungsparameter im `POST` Textkörper enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-168">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="5f4ab-169">Erweiterte Verwendung: Minimale Browserversion</span><span class="sxs-lookup"><span data-stu-id="5f4ab-169">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="5f4ab-170">Als neue APIs-Version für das Microsoft Edge können Sie eine aktualisierte Version Ihrer Erweiterung oder App veröffentlichen, die nur mit neueren versionen Microsoft Edge kann.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-170">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="5f4ab-171">Wenn Microsoft Edge automatisch aktualisiert wird, kann es einige Tage dauern, bis die meisten Benutzer auf diese neue Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-171">When Microsoft Edge is automatically updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="5f4ab-172">Um sicherzustellen, dass ein bestimmtes Update nur für Microsoft Edge versionen gilt, die aktuell oder neuer als eine bestimmte Version sind, fügen Sie das `prodversionmin` Attribut in Ihrem Updatemanifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-172">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="5f4ab-173">Im folgenden Codeausschnitt gibt der Attributwert von an, dass Ihre App automatisch auf die Version aktualisiert wird, wenn der Benutzer Microsoft Edge `prodversionmin` `3.0.193.0` oder neuer ausgeführt `2.0` `3.0.193.0` wird.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-173">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app automatically updated to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Aktualisieren oder Entfernen Der Erweiterungs-| Microsoft Docs"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> <span data-ttu-id="5f4ab-176">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f4ab-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5f4ab-177">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/docs/apps/autoupdate).</span><span class="sxs-lookup"><span data-stu-id="5f4ab-177">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5f4ab-179">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5f4ab-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
