---
description: Informationen zu automatischen Updates für Erweiterungen in Microsoft Edge
title: Erweiterungen für automatische Updates in Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461528"
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
# <a name="auto-update-extensions-in-microsoft-edge"></a><span data-ttu-id="01a22-104">Erweiterungen für automatische Updates in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="01a22-104">Auto-update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="01a22-105">Das automatische Aktualisieren von Erweiterungen bietet einige der gleichen Vorteile wie die automatische Aktualisierung von Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="01a22-105">Automatically updating extensions share some of the same benefits as automatically updating Microsoft Edge:</span></span>   

*   <span data-ttu-id="01a22-106">Integrieren sie Fehler- und Sicherheitsbehebungen.</span><span class="sxs-lookup"><span data-stu-id="01a22-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="01a22-107">Fügen Sie neue Features oder Leistungsverbesserungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="01a22-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="01a22-108">Verbessern Sie die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="01a22-108">Improve the user interface.</span></span>  

<span data-ttu-id="01a22-109">Früher, als nicht speicherbasierte Erweiterungen unterstützt wurden, konnten die systemeigenen Binärdateien und die Erweiterung gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="01a22-109">Previously when non-store based extensions were supported, it was possible to update the native binaries and the extension at the same time.</span></span>  <span data-ttu-id="01a22-110">Jetzt werden diese Erweiterungen im Microsoft Edge-Add-Ons-Speicher gehostet, und Updates werden mit demselben Mechanismus vorgenommen, den Microsoft Edge verwendet, den Sie nicht steuern können.</span><span class="sxs-lookup"><span data-stu-id="01a22-110">Now, those extensions are hosted in the Microsoft Edge Add-ons store and updates are made using the same mechanism that Microsoft Edge uses, which you can't control.</span></span>  <span data-ttu-id="01a22-111">Beim Aktualisieren von Erweiterungen, die von systemeigenen Binärdateien abhängig sind, sollten Sie vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="01a22-111">You should be careful when updating extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="01a22-112">Dieses Thema gilt nicht für Erweiterungen, die über das [Partner Center-Dashboard veröffentlicht][MicrosoftPartnerCenter] wurden.</span><span class="sxs-lookup"><span data-stu-id="01a22-112">This topic does not apply to extensions published using the [Partner Center][MicrosoftPartnerCenter] dashboard.</span></span>  <span data-ttu-id="01a22-113">Sie können das Dashboard verwenden, um aktualisierte Versionen für Ihre Benutzer und für den Microsoft Edge-Add-Ons-Speicher zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="01a22-113">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>

## <a name="overview"></a><span data-ttu-id="01a22-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="01a22-114">Overview</span></span>  

<span data-ttu-id="01a22-115">Alle paar Stunden überprüft Microsoft Edge, ob jede installierte Erweiterung oder App über eine Update-URL verfügt.</span><span class="sxs-lookup"><span data-stu-id="01a22-115">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="01a22-116">Erweiterungen können mithilfe des Felds im Manifest eine Update-URL angeben, die auf einen Speicherort `update_url` verweist, um eine Aktualisierungsprüfung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="01a22-116">Extensions can specify an update URL using the `update_url` field in the manifest, which points to a location to perform an update check.</span></span>  <span data-ttu-id="01a22-117">Für jeden `update_url` sendet er Anforderungen für aktualisierte Manifest-XML-Dateien.</span><span class="sxs-lookup"><span data-stu-id="01a22-117">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="01a22-118">Wenn in der Updatemanifest-XML-Datei eine neuere Version als die installierte aufgeführt ist, lädt Microsoft Edge die neuere Version herunter und installiert sie.</span><span class="sxs-lookup"><span data-stu-id="01a22-118">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="01a22-119">Der gleiche Prozess funktioniert für manuelle Updates, bei denen die neue Datei mit demselben privaten Schlüssel wie die aktuell installierte `.crx` Version signiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="01a22-119">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="01a22-120">Um den Datenschutz der Benutzer zu gewährleisten, sendet Microsoft Edge keine Kopfzeilen mit Manifestanforderungen für automatische Updates und ignoriert alle Kopfzeilen in den Antworten `Cookie` `Set-Cookie` auf diese Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="01a22-120">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="01a22-121">Update-URL</span><span class="sxs-lookup"><span data-stu-id="01a22-121">Update URL</span></span>  

<span data-ttu-id="01a22-122">Wenn Sie Ihre eigene Erweiterung oder App hosten, müssen Sie der Datei `update_url` das Feld `manifest.json` hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="01a22-122">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="01a22-123">Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel für `update_url` .</span><span class="sxs-lookup"><span data-stu-id="01a22-123">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="01a22-124">Aktualisiertes Manifest</span><span class="sxs-lookup"><span data-stu-id="01a22-124">Updated manifest</span></span>  

<span data-ttu-id="01a22-125">Das aktualisierte Manifest, das vom Server zurückgegeben wird, sollte ein XML-Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="01a22-125">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="01a22-126">Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel der aktualisierten Manifest-XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="01a22-126">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="01a22-127">In der folgenden Tabelle werden die Attribute der aktualisierten Manifest-XML-Datei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="01a22-127">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="01a22-128">Attribut</span><span class="sxs-lookup"><span data-stu-id="01a22-128">Attribute</span></span> | <span data-ttu-id="01a22-129">Details</span><span class="sxs-lookup"><span data-stu-id="01a22-129">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="01a22-130">Die Erweiterungs-ID wird basierend auf einem Hash des öffentlichen Schlüssels generiert.</span><span class="sxs-lookup"><span data-stu-id="01a22-130">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="01a22-131">Um die ID einer Erweiterung zu finden, öffnen Sie Microsoft Edge, und navigieren Sie zu `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="01a22-131">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="01a22-132">Eine URL zur `.crx` Datei.</span><span class="sxs-lookup"><span data-stu-id="01a22-132">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="01a22-133">Dieser Attributwert wird von Microsoft Edge verwendet, um zu bestimmen, ob die `.crx` durch angegebene Datei heruntergeladen werden `codebase` soll.</span><span class="sxs-lookup"><span data-stu-id="01a22-133">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="01a22-134">Es sollte mit dem Wert `version` in der Datei der Datei `manifest.json` `.crx` übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="01a22-134">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="01a22-135">Die Updatemanifest-XML-Datei kann Informationen zu mehreren Erweiterungen enthalten, indem mehrere Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="01a22-135">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="01a22-136">Testen</span><span class="sxs-lookup"><span data-stu-id="01a22-136">Testing</span></span>  

<span data-ttu-id="01a22-137">Die Standardhäufigkeit der Aktualisierungsprüfung beträgt mehrere Stunden.</span><span class="sxs-lookup"><span data-stu-id="01a22-137">The default update check frequency is several hours.</span></span>  <span data-ttu-id="01a22-138">Um ein Update zu erzwingen, navigieren Sie zu `edge://extensions` und wählen Sie die Schaltfläche Erweiterungen **jetzt** aktualisieren aus.</span><span class="sxs-lookup"><span data-stu-id="01a22-138">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="01a22-139">Erweiterte Verwendung: Anforderungsparameter</span><span class="sxs-lookup"><span data-stu-id="01a22-139">Advanced usage: request parameters</span></span>  

<span data-ttu-id="01a22-140">Der grundlegende Mechanismus für die automatische Aktualisierung ist so einfach wie das Ablegen einer statischen XML-Datei auf einem Beliebigen Webserver wie Apache und das Aktualisieren der XML-Datei, wenn Sie neue Versionen Ihrer Erweiterungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="01a22-140">The basic auto-update mechanism is as easy as dropping a static XML file onto any web server such as Apache, and updating the XML file as you release new versions of your extensions.</span></span>  

<span data-ttu-id="01a22-141">Sie können die Tatsache nutzen, dass der Updatemanifestanforderung Parameter hinzugefügt werden, die die Erweiterungs-ID und Version angeben.</span><span class="sxs-lookup"><span data-stu-id="01a22-141">You may take advantage of the fact that parameters are added to the update manifest request that indicate the extension ID and version.</span></span> <span data-ttu-id="01a22-142">Sie können die gleiche Update-URL für alle Erweiterungen anstelle einer statischen XML-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="01a22-142">You can use the same update URL for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="01a22-143">Um dieselbe Update-URL für alle Erweiterungen zu verwenden, zeigen Sie auf eine URL, auf der dynamischer serverseitiger Code ausgeführt wird, um diese Parameter zu testen.</span><span class="sxs-lookup"><span data-stu-id="01a22-143">To use the same update URL for all your extensions, point to a URL that runs dynamic server-side code to test these parameters.</span></span>  

<span data-ttu-id="01a22-144">Im folgenden Beispiel wird das Format der Anforderungsparameter der Update-URL veranschaulicht: `?x={extension_data}` .</span><span class="sxs-lookup"><span data-stu-id="01a22-144">The following example demonstrates the format of the request parameters of update URL: `?x={extension_data}`.</span></span>

<span data-ttu-id="01a22-145">In diesem Beispiel `{extension_data}` handelt es sich um eine URL-codierte Zeichenfolge, die das folgende Format verwendet: `id={id}&v={version}` .</span><span class="sxs-lookup"><span data-stu-id="01a22-145">In this example, `{extension_data}` is a URL-encoded string that uses the following format: `id={id}&v={version}`.</span></span>

<span data-ttu-id="01a22-146">Die folgenden beiden Erweiterungen verweisen beispielsweise beide auf die gleiche Update-URL `http://contoso.com/extension_updates.php` .</span><span class="sxs-lookup"><span data-stu-id="01a22-146">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*  <span data-ttu-id="01a22-147">Erweiterung 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"</span><span class="sxs-lookup"><span data-stu-id="01a22-147">Extension 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"</span></span>
*  <span data-ttu-id="01a22-148">Erweiterung 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0,4"</span><span class="sxs-lookup"><span data-stu-id="01a22-148">Extension 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0.4"</span></span>


<span data-ttu-id="01a22-149">Im Folgenden sind die Anforderungen zum Aktualisieren jeder Erweiterung zu finden.</span><span class="sxs-lookup"><span data-stu-id="01a22-149">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="01a22-150">Sie können auch mehrere Erweiterungen in einer einzigen Anforderung für jede eindeutige Update-URL auflisten.</span><span class="sxs-lookup"><span data-stu-id="01a22-150">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="01a22-151">Im folgenden Beispiel werden die vorherigen Anforderungen in einer einzigen Anforderung zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="01a22-151">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="01a22-152">Wenn Sie eine einzelne Anforderung senden und die Anzahl der installierten Erweiterungen, die dieselbe Update-URL verwenden, zu lang ist, werden bei der Updateüberprüfung weitere Anforderungen `GET` gestellt.</span><span class="sxs-lookup"><span data-stu-id="01a22-152">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="01a22-153">Eine `GET` Anforderungs-URL ist zu lang, wenn sie ungefähr 2000 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="01a22-153">A `GET` request URL is too long if it is approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="01a22-154">In Zukunft kann eine einzelne `POST` Anforderung mehrere Anforderungen `GET` ersetzen.</span><span class="sxs-lookup"><span data-stu-id="01a22-154">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="01a22-155">Die `POST` Anforderung kann die Anforderungsparameter im `POST` Textkörper enthalten.</span><span class="sxs-lookup"><span data-stu-id="01a22-155">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="01a22-156">Erweiterte Verwendung: Minimale Browserversion</span><span class="sxs-lookup"><span data-stu-id="01a22-156">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="01a22-157">Als neue APIs-Version für das Microsoft Edge-Erweiterungssystem können Sie eine aktualisierte Version Ihrer Erweiterung oder App veröffentlichen, die nur mit neueren Microsoft Edge-Versionen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="01a22-157">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="01a22-158">Wenn Microsoft Edge automatisch aktualisiert wird, kann es einige Tage dauern, bis die meisten Benutzer auf diese neue Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="01a22-158">When Microsoft Edge is auto-updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="01a22-159">Um sicherzustellen, dass ein bestimmtes Update nur für Microsoft Edge-Versionen gilt, die aktuell oder neuer als eine bestimmte Version sind, fügen Sie das `prodversionmin` Attribut in Ihrem Updatemanifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="01a22-159">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="01a22-160">Im folgenden Codeausschnitt gibt der Attributwert von an, dass Ihre App nur dann automatisch auf die Version aktualisiert wird, wenn der Benutzer Microsoft Edge oder neuer `prodversionmin` `3.0.193.0` ausgeführt `2.0` `3.0.193.0` hat.</span><span class="sxs-lookup"><span data-stu-id="01a22-160">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app auto-updates to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> <span data-ttu-id="01a22-162">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01a22-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="01a22-163">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/docs/apps/autoupdate/).</span><span class="sxs-lookup"><span data-stu-id="01a22-163">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate/).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="01a22-165">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="01a22-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
