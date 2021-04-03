---
description: Die neuesten experimentellen Features in Microsoft Edge für Web Apps
title: Experimentelle Features | Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474968"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="cb7a9-104">Experimentelle Features in Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="cb7a9-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="cb7a9-105">Microsoft Edge bietet Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="cb7a9-106">Testen Und geben Sie Feedback, um zu ermitteln, ob die einzelnen Features bereit sind und wann sie [veröffentlicht werden.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="cb7a9-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="cb7a9-107">Experimentelle Features sind in allen Kanälen von Microsoft Edge verfügbar, aber die neuesten experimentellen Features sind nur im Microsoft Edge Canary-Kanal verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="cb7a9-108">Aktivieren experimenteller Features</span><span class="sxs-lookup"><span data-stu-id="cb7a9-108">Turn on experimental features</span></span>  

<span data-ttu-id="cb7a9-109">Führen Sie die folgenden Schritte aus, um \(oder off\) experimentelle Features in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="cb7a9-110">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="cb7a9-111">Stellen Sie sicher, dass Sie eine Microsoft Edge-Version verwenden, für die das Experiment in diesem Artikel aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="cb7a9-112">Navigieren Sie zu [Experimentelle Features](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="cb7a9-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="cb7a9-113">Navigieren Sie zu `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="cb7a9-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="cb7a9-114">Navigieren Sie zum entsprechenden Experiment.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="cb7a9-115">Wählen Sie das Dropdownmenü neben der Experimentbeschreibung aus, und wählen Sie `Enabled` aus.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Wählen Sie Aktiviert aus, um ein Experiment zu aktivieren." lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="cb7a9-117">Wählen **Sie Aktiviert** aus, um ein Experiment zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cb7a9-118">Jedes Experiment verfügt in der Regel über ein Dropdownmenü, um die folgenden Werte zu wählen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="cb7a9-119">Wenn ein experimentelles Feature keinen Eintrag zu **Experimenten**enthält, werden Anweisungen zum Starten von Microsoft Edge mit diesem Feature über die Befehlszeile bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="cb7a9-120">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="cb7a9-121">Herkunfts Versuche</span><span class="sxs-lookup"><span data-stu-id="cb7a9-121">Origin Trials</span></span>  

<span data-ttu-id="cb7a9-122">Microsoft Edge verwendet manchmal Ursprungstests, um Features für bestimmte Domänen oder Websites zu testen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="cb7a9-123">Möglicherweise möchten Sie eine Origin-Testversion für Ihre Website verwenden, um ein bestimmtes Feature anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="cb7a9-124">Wenn Sie Websitebesitzer sind, können Sie sich an einer Ursprungsprobe registrieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="cb7a9-125">Eine Origin-Testversion stellt Features für einen Prozentsatz der Microsoft Edge-Benutzer bereit, die Ihre Website besuchen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="cb7a9-126">Weitere Informationen zu Origin Trials finden Sie unter [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="cb7a9-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="cb7a9-127">Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="cb7a9-128">Navigieren Sie zum Deaktivieren eines experimentellen Features zu Aktivieren experimenteller [Features,](#turn-on-experimental-features)navigieren Sie zum Experiment, und wählen Sie dann `Disabled` aus.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="cb7a9-129">Features, die zum Testen verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="cb7a9-129">Features that are available to test</span></span>  

<span data-ttu-id="cb7a9-130">In der folgenden Liste werden die neuen experimentellen Web-App-Features beschrieben, die in Microsoft Edge zum Testen und Überprüfen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="cb7a9-131">Feature</span><span class="sxs-lookup"><span data-stu-id="cb7a9-131">Feature</span></span> | <span data-ttu-id="cb7a9-132">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="cb7a9-132">Microsoft Edge version</span></span> | <span data-ttu-id="cb7a9-133">Plattform</span><span class="sxs-lookup"><span data-stu-id="cb7a9-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="cb7a9-134">URI-Protokollbehandlung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="cb7a9-135">91 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb7a9-135">91 or later</span></span> | <span data-ttu-id="cb7a9-136">Windows</span><span class="sxs-lookup"><span data-stu-id="cb7a9-136">Windows</span></span> |    
| [<span data-ttu-id="cb7a9-137">URL Link Handling</span><span class="sxs-lookup"><span data-stu-id="cb7a9-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="cb7a9-138">91 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb7a9-138">91 or later</span></span> | <span data-ttu-id="cb7a9-139">Windows</span><span class="sxs-lookup"><span data-stu-id="cb7a9-139">Windows</span></span>|  
| [<span data-ttu-id="cb7a9-140">Ausführen unter Betriebssystemanmeldung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-140">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="cb7a9-141">88 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb7a9-141">88 or later</span></span> | <span data-ttu-id="cb7a9-142">Alle</span><span class="sxs-lookup"><span data-stu-id="cb7a9-142">All</span></span> |  
| [<span data-ttu-id="cb7a9-143">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="cb7a9-143">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="cb7a9-144">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb7a9-144">87 or later</span></span> | <span data-ttu-id="cb7a9-145">Alle</span><span class="sxs-lookup"><span data-stu-id="cb7a9-145">All</span></span> |  
| [<span data-ttu-id="cb7a9-146">Dateiverarbeitung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-146">File Handling</span></span>](#file-handling) | <span data-ttu-id="cb7a9-147">83 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb7a9-147">83 or later</span></span> | <span data-ttu-id="cb7a9-148">All Desktop</span><span class="sxs-lookup"><span data-stu-id="cb7a9-148">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="cb7a9-149">URI-Protokollbehandlung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-149">URI Protocol Handling</span></span>  

<span data-ttu-id="cb7a9-150">Ein einheitlicher Ressourcenbezeichner \(URI\) kann verwendet werden, um mehr als nur Links zu Webseiten und Webinhalten mithilfe des HTTP- oder FTP-Protokolls zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-150">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="cb7a9-151">URIs können verwendet werden, um Links zu allem zu beschreiben, was Sie in einem Schema codieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-151">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="cb7a9-152">Beispielsweise wird das Protokoll verwendet, um einen E-Mail-Link zu beschreiben, und das Betriebssystem \(OS\) oder der Browser entscheidet, welche Webseite oder App dieses Protokoll `mailto://` verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-152">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="cb7a9-153">Weitere Informationen zur vorhandenen browserbasierten Unterstützung finden Sie unter [Webbasierte Protokollhandler][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span><span class="sxs-lookup"><span data-stu-id="cb7a9-153">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="cb7a9-154">Mit diesem Feature können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-154">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="cb7a9-155">Registrieren Ihres PWA beim Hostbetriebssystem mithilfe des Manifests Ihrer Web-App</span><span class="sxs-lookup"><span data-stu-id="cb7a9-155">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="cb7a9-156">Deklarieren, dass ein PWA ein bestimmtes URI-Protokoll verarbeitet</span><span class="sxs-lookup"><span data-stu-id="cb7a9-156">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="cb7a9-157">Nachdem Sie einen PWA als Protokollhandler registriert haben, wird der registrierte PWA vom Betriebssystem aktiviert und empfängt den URI, wenn ein Benutzer einen Hyperlink mit einem bestimmten Schema wie oder aus einem Browser oder einer systemeigenen App `mailto://` `web+music://` wählt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-157">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="cb7a9-158">Dieses Feature erfordert, dass Sie das Web-App-Manifest so aktualisieren, dass es ein Array enthält, in das Array müssen `protocol_handlers` Sie zwei Felder angeben:</span><span class="sxs-lookup"><span data-stu-id="cb7a9-158">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="cb7a9-159">: Das Protokoll zur Verarbeitung der Anforderung, z. B. `mailto` oder `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="cb7a9-159">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="cb7a9-160">: Der HTTPS-URI im App-Bereich, der das Protokoll behandelt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-160">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="cb7a9-161">In Zukunft soll der URI, der mit dem Protokollhandlerschema beginnt, das Token `%s` ersetzen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-161">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="cb7a9-162">Aktualisieren Sie Ihr Manifest, um das Protokoll zu unterstützen, das Sie registrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-162">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="cb7a9-163">Nachdem Sie dieses Feature aktivieren, werden die folgenden Aktionen von Microsoft Edge abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-163">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="cb7a9-164">Erkennt Änderungen im Manifest</span><span class="sxs-lookup"><span data-stu-id="cb7a9-164">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="cb7a9-165">Registriert die App für das Protokoll</span><span class="sxs-lookup"><span data-stu-id="cb7a9-165">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="cb7a9-166">Wenn mehrere Apps ein Protokoll registrieren, wird dem Benutzer eine Eingabeaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-166">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="cb7a9-167">Der Benutzer wählt die entsprechende App aus der Liste aus, die vom Betriebssystem oder Browser angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-167">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="cb7a9-168">Um eine Vorschau der Protokollverarbeitung in Microsoft Edge unter Windows anzuzeigen, navigieren Sie zu [Aktivieren](#turn-on-experimental-features) experimenteller Features, und aktivieren Sie **Desktop Web Apps unterstützen Protokollhandler**.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-168">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop Web Apps support Protocol Handlers**.</span></span>  

<span data-ttu-id="cb7a9-169">Weitere Informationen zur Ausführung der Ursprungsprozedur für Protokollhandler finden Sie unter Registrieren für die Registrierung von [Web App-Protokollhandlern.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]</span><span class="sxs-lookup"><span data-stu-id="cb7a9-169">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="cb7a9-170">Beispielmanifest</span><span class="sxs-lookup"><span data-stu-id="cb7a9-170">Example Manifest</span></span>

<span data-ttu-id="cb7a9-171">In diesem Beispiel deklariert ein Web-App-Manifest, dass die App für die Verarbeitung der Protokolle und registriert `web+jngl` werden `web+jnglstore` soll.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-171">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a><span data-ttu-id="cb7a9-172">URL Link Handling</span><span class="sxs-lookup"><span data-stu-id="cb7a9-172">URL Link Handling</span></span>  

<span data-ttu-id="cb7a9-173">Ein uniform resource locator \(URL\) ist ein URI-Typ.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-173">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="cb7a9-174">Erstellen Sie eine ansprechendere Umgebung, wenn Progressive Web Apps \(PWAs\) sich als Handler für https-URIs registrieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-174">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="cb7a9-175">PWAs können anfordern, dass sie gestartet werden, wenn zugeordnete URIs aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-175">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="cb7a9-176">Wenn ein Benutzer beispielsweise einen Link zu einem Nachrichtentext aus einer E-Mail-Nachricht wählt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-176">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="cb7a9-177">Eine zugeordnete PWA zum Anzeigen von Nachrichten wird automatisch gestartet, um die Aktivierung des Links zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-177">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="cb7a9-178">Mit diesem Feature können Sie eine PWA mithilfe des Web-App-Manifests beim Browser registrieren und deklarieren, dass der Browser bestimmte Links verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-178">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="cb7a9-179">Um einen PWA beim Browser zu registrieren, fügen Sie der Manifestdatei das optionale `url_handlers` Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-179">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="cb7a9-180">Das `url_handlers` Mitglied ist ein Element, das die Ursprünge von URIs, die die `object[]` App verarbeiten möchte, gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-180">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="cb7a9-181">Die Linkbehandlung wird vom Browser mithilfe einer JSON-Datei überprüft, die `web-app-origin-association` sich am Ursprung befindet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-181">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="cb7a9-182">Die Ursprungsdatei stimmt die eingeschlossenen oder ausgeschlossenen Pfade am Ursprung weiter ab.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-182">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="cb7a9-183">Ausführliche Anweisungen zum Testen des URL-Handlers finden Sie unter [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="cb7a9-183">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="cb7a9-184">Navigieren Sie zum Anzeigen einer Vorschau der URL-Linkbehandlung in Microsoft Edge unter Windows zu [Aktivieren](#turn-on-experimental-features) experimenteller Features und Aktivieren der **Desktop-PWA-URL-Behandlung**.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-184">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="cb7a9-185">Beispiel für url_handlers im Manifest</span><span class="sxs-lookup"><span data-stu-id="cb7a9-185">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="cb7a9-186">Der folgende Codeausschnitt ist ein Beispiel-Web-App-Manifest mit dem `url_handlers` Element.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-186">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

<span data-ttu-id="cb7a9-187">Ein PWA stimmt mit einem URI für die URL-Behandlung überein, wenn der URI einer der Ursprungszeichenfolgen in entspricht und der Browser überprüft, ob der Ursprung zustimmt, dass diese App einen solchen `url_handlers` URI verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-187">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="cb7a9-188">Das Element enthält einen Ursprung, der den Bereich und auch andere nicht verwandte Ursprünge des anfordernden `url_handlers` PWA umfasst.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-188">The `url_handlers` member contains an origin that encompasses the scope and also other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="cb7a9-189">Wenn Sie URIs nicht auf denselben Bereich oder dieselbe Domäne wie die anfordernde PWA beschränken, können Sie unterschiedliche Domänennamen für denselben Inhalt verwenden, sie jedoch mit demselben PWA behandeln.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-189">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="cb7a9-190">Platzhalterabgleich</span><span class="sxs-lookup"><span data-stu-id="cb7a9-190">Wildcard matching</span></span>  

<span data-ttu-id="cb7a9-191">Verwenden Sie das Platzhalterzeichen \( `*` \), um einem oder mehreren Zeichen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-191">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="cb7a9-192">Ein Platzhalterpräfix wird in Ursprungszeichenfolgen des Mitglieds verwendet, `url_handlers` um für unterschiedliche Unterdomänen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-192">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="cb7a9-193">Das Präfix muss `*.` für diese Verwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-193">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="cb7a9-194">Das `https` Schema wird angenommen, wenn Sie ein Platzhalterpräfix verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-194">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="cb7a9-195">Beispielsweise ist der `url_handlers` Memberwert auf Übereinstimmungen und `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` festgelegt, aber nicht mit `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="cb7a9-195">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  
-->  

## <a name="run-on-os-login"></a><span data-ttu-id="cb7a9-196">Ausführen unter Betriebssystemanmeldung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-196">Run On OS Login</span></span>  

<span data-ttu-id="cb7a9-197">Mit diesem Feature können Sie Ihre App so konfigurieren, dass sie automatisch gestartet wird, wenn sich der Benutzer bei Microsoft Windows anmeldet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-197">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="cb7a9-198">Mehrere Klassen von Apps nutzen die Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-198">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="cb7a9-199">Zu den Klassen von Apps gehören E-Mails, Chats, Überwachungsdashboards und Echtzeit-Datenanzeige-Apps.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-199">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="cb7a9-200">Die Funktion ermöglicht es einem Benutzer, sich mit den Apps zu beschäftigen, sobald sich der Benutzer beim Betriebssystem anmeldet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-200">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="cb7a9-201">Mit diesem Feature wird die PWA automatisch auf die gleiche Weise wie manuell gestartet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-201">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cb7a9-202">**Ausführen unter Betriebssystemanmeldung** ist ein [leistungsstarkes Feature.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="cb7a9-202">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="cb7a9-203">Benutzer sollten entscheiden, ob sie die Funktion für die installierte Web-App aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-203">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="cb7a9-204">Aktivieren der Anmeldung unter Betriebssystem ausführen</span><span class="sxs-lookup"><span data-stu-id="cb7a9-204">Turn on Run On OS Login</span></span>  

<span data-ttu-id="cb7a9-205">Navigieren Sie zum Aktivieren **der Anmeldefunktionen** für das Betriebssystem ausführen für Ihre PWA zu [Aktivieren](#turn-on-experimental-features) experimenteller Features, und aktivieren Sie **Desktop-PWAs,** die unter Betriebssystemanmeldung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-205">To turn on **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Aktivieren des Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt wird" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="cb7a9-207">Aktivieren des **Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt** wird</span><span class="sxs-lookup"><span data-stu-id="cb7a9-207">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="cb7a9-208">Aktivieren des Features für die installierte Web-App</span><span class="sxs-lookup"><span data-stu-id="cb7a9-208">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="cb7a9-209">Um das Feature `Start app when you sign in` für eine installierte PWA zu aktivieren,</span><span class="sxs-lookup"><span data-stu-id="cb7a9-209">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="cb7a9-210">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-210">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="cb7a9-211">Navigieren Sie zu `edge://apps` .</span><span class="sxs-lookup"><span data-stu-id="cb7a9-211">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="cb7a9-212">Zeigen Sie auf Ihre App.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-212">Hover on your app.</span></span>  
1.  <span data-ttu-id="cb7a9-213">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie dann App starten **aus, wenn Sie sich anmelden.**</span><span class="sxs-lookup"><span data-stu-id="cb7a9-213">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Verwenden des Kontextmenüs zum Aktivieren der Start-App bei der Anmeldung in Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="cb7a9-215">Verwenden des Kontextmenüs zum Aktivieren der **Start-App bei der** Anmeldung in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cb7a9-215">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="cb7a9-216">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="cb7a9-216">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="cb7a9-217">ist ein neues Mitglied der Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-217">is a new member of the manifest file.</span></span>  <span data-ttu-id="cb7a9-218">Sie können Links zu Teilen, wichtigen Webseiten oder Aktionen in Ihrer Web-App definieren.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-218">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="cb7a9-219">Microsoft Windows integriert es als **Jumplists**.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-219">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="cb7a9-220">**Sprunglisten definieren** Popupmenüs, die angezeigt werden, wenn Sie eines der folgenden Benutzeroberflächenelemente verwenden und ein kontextbezogenes Menü \(rechtsklicken\) öffnen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-220">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="cb7a9-221">Eine Kachel im Startmenü</span><span class="sxs-lookup"><span data-stu-id="cb7a9-221">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="cb7a9-222">Ein Symbol auf der Taskleiste</span><span class="sxs-lookup"><span data-stu-id="cb7a9-222">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="cb7a9-223">Wenn ein Benutzer eine Verknüpfung aufruft, navigiert der Benutzer zu der vom Element der `url` Verknüpfung angegebenen Adresse.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-223">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Beispiel für Jumplists unter Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="cb7a9-225">Beispiel für **Jumplists** unter Windows 10</span><span class="sxs-lookup"><span data-stu-id="cb7a9-225">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="cb7a9-226">Verknüpfungen in der Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="cb7a9-226">Shortcuts in the Manifest file</span></span>  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="cb7a9-227">Eigenschaften von Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="cb7a9-227">Properties of shortcuts</span></span>  

<span data-ttu-id="cb7a9-228">Die folgenden Eigenschaften definieren jede Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-228">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="cb7a9-229">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb7a9-229">Property</span></span> | <span data-ttu-id="cb7a9-230">Details</span><span class="sxs-lookup"><span data-stu-id="cb7a9-230">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="cb7a9-231">Eine Zeichenfolge, die dem Benutzer auf **Sprunglisten oder** im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-231">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="cb7a9-232">Eine Zeichenfolge, die angezeigt wird, wenn nicht genügend Speicherplatz vorhanden ist, um den vollständigen Namen der Verknüpfung anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-232">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="cb7a9-233">Eine Zeichenfolge, die den Zweck der Verknüpfung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-233">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="cb7a9-234">Auf sie kann durch Hilfstechnologie zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-234">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="cb7a9-235">Der URI in der Web-App, der geöffnet wird, wenn die Verknüpfung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-235">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="cb7a9-236">Eine Reihe von Symbolen, die die Verknüpfung darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-236">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="cb7a9-237">Dateiverarbeitung</span><span class="sxs-lookup"><span data-stu-id="cb7a9-237">File Handling</span></span>  

<span data-ttu-id="cb7a9-238">Die Möglichkeit, sich als Dateityphandler zu registrieren, befindet sich in der Experimentierphase.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-238">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="cb7a9-239">Sie können die Dateitypen angeben, die Ihre App in einem Manifesteintrag verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-239">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="cb7a9-240">Während der Installation registriert das Hostbetriebssystem des Benutzers Ihre App als Dateihandler für die aufgeführten Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-240">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="cb7a9-241">Stellen Sie sicher, dass das Feature im Startcode Ihrer Apps enthalten ist und `launchQueue` die Datei verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-241">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="cb7a9-242">Chrombasierte Browser testen und gestalten dieses Feature.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-242">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="cb7a9-243">Weitere Informationen einschließlich Codebeispielen finden Sie unter [Let web applications be file handlers][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="cb7a9-243">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="cb7a9-244">Um eine Vorschau der Dateiverarbeitung in Microsoft Edge für Desktop-OSs anzuzeigen, navigieren Sie zu Aktivieren experimenteller [Features](#turn-on-experimental-features) und Aktivieren der **Dateibehandlungs-API**.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-244">To preview file handling in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="cb7a9-245">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="cb7a9-245">Providing feedback on experimental features</span></span>  

<span data-ttu-id="cb7a9-246">So geben Sie Feedback zu Microsoft Edge-Web-App-Experimenten.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-246">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="cb7a9-247">Senden Sie Ihr Feedback mithilfe **von Einstellungen und mehr** \( `...` \) > Feedback an Microsoft **senden.**</span><span class="sxs-lookup"><span data-stu-id="cb7a9-247">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="cb7a9-248">Wählen Sie `Alt` + `Shift` + `I` aus.</span><span class="sxs-lookup"><span data-stu-id="cb7a9-248">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Senden von Feedback von Ihrem PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="cb7a9-250">Senden von Feedback von Ihrem PWA</span><span class="sxs-lookup"><span data-stu-id="cb7a9-250">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Origin Trials | Microsoft Edge Developer"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrieren für die Registrierung von Web App-Protokollhandlern | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Webbasierte Protokollhandler | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Leistungsstarkes Feature – Berechtigungen | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs als URL Handlers | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Webanwendungen als Dateihandler verwenden | web.dev"  
