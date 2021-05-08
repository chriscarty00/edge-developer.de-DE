---
description: Die neuesten experimentellen Features in Microsoft Edge für Web Apps
title: Experimentelle Features | Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 641b6fd5185e7f96289c1de6482764979ee0981d
ms.sourcegitcommit: 9cc54ba3e731ecc8b713c3cf215018848f7405b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/19/2021
ms.locfileid: "11496756"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="b2d14-104">Experimentelle Features in Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="b2d14-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="b2d14-105">Microsoft Edge bietet Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="b2d14-106">Testen Und geben Sie Feedback, um zu ermitteln, ob die einzelnen Features bereit sind und wann sie [veröffentlicht werden.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="b2d14-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="b2d14-107">Experimentelle Features sind in allen Kanälen der Microsoft Edge verfügbar, aber die neuesten experimentellen Features sind nur in der Microsoft Edge Canary Channel.</span><span class="sxs-lookup"><span data-stu-id="b2d14-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="b2d14-108">Aktivieren experimenteller Features</span><span class="sxs-lookup"><span data-stu-id="b2d14-108">Turn on experimental features</span></span>  

<span data-ttu-id="b2d14-109">Führen Sie die folgenden Schritte aus, um die experimentellen Features in Microsoft Edge aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="b2d14-110">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2d14-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="b2d14-111">Stellen Sie sicher, dass Sie Microsoft Edge version verwenden, in der das Experiment in diesem Artikel aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="b2d14-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="b2d14-112">Navigieren Sie zu [Experimentelle Features](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="b2d14-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="b2d14-113">Navigieren Sie zu `edge://flags`.</span><span class="sxs-lookup"><span data-stu-id="b2d14-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="b2d14-114">Navigieren Sie zum entsprechenden Experiment.</span><span class="sxs-lookup"><span data-stu-id="b2d14-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="b2d14-115">Wählen Sie das Dropdownmenü neben der Experimentbeschreibung aus, und wählen Sie `Enabled` aus.</span><span class="sxs-lookup"><span data-stu-id="b2d14-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Wählen Sie Aktiviert aus, um ein Experiment zu aktivieren." lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="b2d14-117">Wählen **Sie Aktiviert** aus, um ein Experiment zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b2d14-118">Jedes Experiment verfügt in der Regel über ein Dropdownmenü, um die folgenden Werte zu wählen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="b2d14-119">Wenn ein experimentelles Feature keinen Eintrag zu **Experimenten**enthält, werden Anweisungen bereitgestellt, um Microsoft Edge über die Befehlszeile zu starten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="b2d14-120">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="b2d14-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="b2d14-121">Herkunfts Versuche</span><span class="sxs-lookup"><span data-stu-id="b2d14-121">Origin Trials</span></span>  

<span data-ttu-id="b2d14-122">Microsoft Edge verwendet manchmal Ursprungstests, um Features für bestimmte Domänen oder Websites zu testen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="b2d14-123">Möglicherweise möchten Sie eine Origin-Testversion für Ihre Website verwenden, um ein bestimmtes Feature anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="b2d14-124">Wenn Sie Websitebesitzer sind, können Sie sich an einer Ursprungsprobe registrieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="b2d14-125">Eine Origin-Testversion bietet Features für einen Prozentsatz der Microsoft Edge, die Ihre Website besuchen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="b2d14-126">Weitere Informationen zu Origin Trials finden Sie unter [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="b2d14-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b2d14-127">Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="b2d14-128">Navigieren Sie zum Deaktivieren eines experimentellen Features zu Aktivieren experimenteller [Features,](#turn-on-experimental-features)navigieren Sie zum Experiment, und wählen Sie dann `Disabled` aus.</span><span class="sxs-lookup"><span data-stu-id="b2d14-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="b2d14-129">Features, die zum Testen verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="b2d14-129">Features that are available to test</span></span>  

<span data-ttu-id="b2d14-130">In der folgenden Liste werden die neuen experimentellen Web-App-Features beschrieben, die zum Testen und Überprüfen auf Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2d14-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="b2d14-131">Feature</span><span class="sxs-lookup"><span data-stu-id="b2d14-131">Feature</span></span> | <span data-ttu-id="b2d14-132">Microsoft Edge Version</span><span class="sxs-lookup"><span data-stu-id="b2d14-132">Microsoft Edge version</span></span> | <span data-ttu-id="b2d14-133">Plattform</span><span class="sxs-lookup"><span data-stu-id="b2d14-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="b2d14-134">URI-Protokollbehandlung</span><span class="sxs-lookup"><span data-stu-id="b2d14-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="b2d14-135">91 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-135">91 or later</span></span> | <span data-ttu-id="b2d14-136">Windows und Linux</span><span class="sxs-lookup"><span data-stu-id="b2d14-136">Windows and Linux</span></span> |    
| [<span data-ttu-id="b2d14-137">URL Link Handling</span><span class="sxs-lookup"><span data-stu-id="b2d14-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="b2d14-138">91 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-138">91 or later</span></span> | <span data-ttu-id="b2d14-139">Windows</span><span class="sxs-lookup"><span data-stu-id="b2d14-139">Windows</span></span>|
| [<span data-ttu-id="b2d14-140">Überlagerung von Fenstersteuerelementen für Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="b2d14-140">Window Controls Overlay for Desktop Apps</span></span>](#window-controls-overlay-for-installed-desktop-web-apps) | <span data-ttu-id="b2d14-141">91 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-141">91 or later</span></span> | <span data-ttu-id="b2d14-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2d14-142">Windows 10</span></span>|   
| [<span data-ttu-id="b2d14-143">Ausführen unter Betriebssystemanmeldung</span><span class="sxs-lookup"><span data-stu-id="b2d14-143">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="b2d14-144">88 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-144">88 or later</span></span> | <span data-ttu-id="b2d14-145">Alle</span><span class="sxs-lookup"><span data-stu-id="b2d14-145">All</span></span> |  
| [<span data-ttu-id="b2d14-146">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="b2d14-146">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="b2d14-147">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-147">87 or later</span></span> | <span data-ttu-id="b2d14-148">Alle</span><span class="sxs-lookup"><span data-stu-id="b2d14-148">All</span></span> |  
| [<span data-ttu-id="b2d14-149">Dateiverarbeitung</span><span class="sxs-lookup"><span data-stu-id="b2d14-149">File Handling</span></span>](#file-handling) | <span data-ttu-id="b2d14-150">83 oder höher</span><span class="sxs-lookup"><span data-stu-id="b2d14-150">83 or later</span></span> | <span data-ttu-id="b2d14-151">All Desktop</span><span class="sxs-lookup"><span data-stu-id="b2d14-151">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="b2d14-152">URI-Protokollbehandlung</span><span class="sxs-lookup"><span data-stu-id="b2d14-152">URI Protocol Handling</span></span>  

<span data-ttu-id="b2d14-153">Ein einheitlicher Ressourcenbezeichner \(URI\) kann verwendet werden, um mehr als nur Links zu Webseiten und Webinhalten mithilfe des HTTP- oder FTP-Protokolls zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-153">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="b2d14-154">URIs können verwendet werden, um Links zu allem zu beschreiben, was Sie in einem Schema codieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-154">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="b2d14-155">Beispielsweise wird das Protokoll verwendet, um einen E-Mail-Link zu beschreiben, und das Betriebssystem \(OS\) oder der Browser entscheidet, welche Webseite oder App dieses Protokoll `mailto://` verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="b2d14-155">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="b2d14-156">Weitere Informationen zur vorhandenen browserbasierten Unterstützung finden Sie unter [Webbasierte Protokollhandler][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span><span class="sxs-lookup"><span data-stu-id="b2d14-156">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="b2d14-157">Mit diesem Feature können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-157">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="b2d14-158">Registrieren Der PWA mit dem Hostbetriebssystem mithilfe des Manifests Ihrer Web-App</span><span class="sxs-lookup"><span data-stu-id="b2d14-158">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="b2d14-159">Deklarieren, dass PWA ein bestimmtes URI-Protokoll verarbeitet</span><span class="sxs-lookup"><span data-stu-id="b2d14-159">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="b2d14-160">Nachdem Sie einen PWA als Protokollhandler registriert haben, wird der registrierte PWA vom Betriebssystem aktiviert und empfängt den URI, wenn ein Benutzer einen Hyperlink mit einem bestimmten Schema wie oder aus einem Browser oder einer systemeigenen App aus `mailto://` `web+music://` wählt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-160">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="b2d14-161">Dieses Feature erfordert, dass Sie das Web-App-Manifest so aktualisieren, dass es ein Array enthält, in das Array müssen `protocol_handlers` Sie zwei Felder angeben:</span><span class="sxs-lookup"><span data-stu-id="b2d14-161">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="b2d14-162">: Das Protokoll zur Verarbeitung der Anforderung, z. B. `mailto` oder `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="b2d14-162">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="b2d14-163">: Der HTTPS-URI im App-Bereich, der das Protokoll behandelt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-163">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="b2d14-164">In Zukunft soll der URI, der mit dem Protokollhandlerschema beginnt, das Token `%s` ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-164">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="b2d14-165">Aktualisieren Sie Ihr Manifest, um das Protokoll zu unterstützen, das Sie registrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-165">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="b2d14-166">Nachdem Sie dieses Feature aktivieren, Microsoft Edge die folgenden Aktionen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-166">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="b2d14-167">Erkennt Änderungen im Manifest</span><span class="sxs-lookup"><span data-stu-id="b2d14-167">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="b2d14-168">Registriert die App für das Protokoll</span><span class="sxs-lookup"><span data-stu-id="b2d14-168">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="b2d14-169">Wenn mehrere Apps ein Protokoll registrieren, wird dem Benutzer eine Eingabeaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-169">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="b2d14-170">Der Benutzer wählt die entsprechende App aus der Liste aus, die vom Betriebssystem oder Browser angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-170">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="b2d14-171">Wenn Sie eine Vorschau der Protokollverarbeitung in Microsoft Edge Windows anzeigen möchten, navigieren Sie zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features, und aktivieren Sie desktop **PWA Protocol handling**.</span><span class="sxs-lookup"><span data-stu-id="b2d14-171">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA Protocol handling**.</span></span>  

<span data-ttu-id="b2d14-172">Weitere Informationen zur Ausführung der Ursprungsprozedur für Protokollhandler finden Sie unter Registrieren für die Registrierung von [Web App-Protokollhandlern.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]</span><span class="sxs-lookup"><span data-stu-id="b2d14-172">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="b2d14-173">Beispielmanifest</span><span class="sxs-lookup"><span data-stu-id="b2d14-173">Example Manifest</span></span>

<span data-ttu-id="b2d14-174">In diesem Beispiel deklariert ein Web-App-Manifest, dass die App für die Verarbeitung der Protokolle und registriert `web+jngl` werden `web+jnglstore` soll.</span><span class="sxs-lookup"><span data-stu-id="b2d14-174">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

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
 
## <a name="url-link-handling"></a><span data-ttu-id="b2d14-175">URL Link Handling</span><span class="sxs-lookup"><span data-stu-id="b2d14-175">URL Link Handling</span></span>  

<span data-ttu-id="b2d14-176">Ein uniform resource locator \(URL\) ist ein URI-Typ.</span><span class="sxs-lookup"><span data-stu-id="b2d14-176">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="b2d14-177">Erstellen Sie eine ansprechendere Umgebung, wenn Progressive Web Apps \(PWAs\) sich als Handler für https-URIs registrieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-177">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="b2d14-178">PWAs können anfordern, dass sie gestartet werden, wenn zugeordnete URIs aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-178">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="b2d14-179">Wenn ein Benutzer beispielsweise einen Link zu einem Nachrichtentext aus einer E-Mail-Nachricht wählt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-179">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="b2d14-180">Eine zugeordnete PWA zum Anzeigen von Nachrichten wird automatisch gestartet, um die Aktivierung des Links zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-180">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="b2d14-181">Mit diesem Feature können Sie eine PWA mit dem Browser mithilfe des Web-App-Manifests registrieren und deklarieren, dass der Browser bestimmte Links verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-181">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="b2d14-182">Um eine PWA beim Browser zu registrieren, fügen Sie der Manifestdatei das optionale `url_handlers` Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2d14-182">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="b2d14-183">Das `url_handlers` Mitglied ist ein Element, das die Ursprünge von URIs, die die `object[]` App verarbeiten möchte, gruppen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-183">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="b2d14-184">Die Linkbehandlung wird vom Browser mithilfe einer JSON-Datei überprüft, die `web-app-origin-association` sich am Ursprung befindet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-184">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="b2d14-185">Die Ursprungsdatei stimmt die eingeschlossenen oder ausgeschlossenen Pfade am Ursprung weiter ab.</span><span class="sxs-lookup"><span data-stu-id="b2d14-185">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="b2d14-186">Ausführliche Anweisungen zum Testen des URL-Handlers finden Sie unter [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="b2d14-186">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="b2d14-187">Navigieren Sie zum Anzeigen der URL-Linkbehandlung in Microsoft Edge Windows zu [Aktivieren](#turn-on-experimental-features) experimenteller Features, und aktivieren Sie **desktop PWA URL Handling**.</span><span class="sxs-lookup"><span data-stu-id="b2d14-187">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="b2d14-188">Beispiel für url_handlers im Manifest</span><span class="sxs-lookup"><span data-stu-id="b2d14-188">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="b2d14-189">Der folgende Codeausschnitt ist ein Beispiel-Web-App-Manifest mit dem `url_handlers` Element.</span><span class="sxs-lookup"><span data-stu-id="b2d14-189">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

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

<span data-ttu-id="b2d14-190">Ein PWA stimmt mit einem URI für die URL-Behandlung überein, wenn der URI mit einer der Ursprungszeichenfolgen in übereinstimmen und der Browser überprüft, ob der Ursprung zustimmt, dass diese App einen solchen `url_handlers` URI verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b2d14-190">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="b2d14-191">Das Element enthält einen Ursprung, der den Bereich und andere nicht verwandte Ursprünge der anfordernden `url_handlers` PWA.</span><span class="sxs-lookup"><span data-stu-id="b2d14-191">The `url_handlers` member contains an origin that encompasses the scope and other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="b2d14-192">Wenn Sie URIs nicht auf denselben Bereich oder dieselbe Domäne beschränken wie die anfordernde PWA können Sie unterschiedliche Domänennamen für denselben Inhalt verwenden, sie jedoch mit demselben PWA.</span><span class="sxs-lookup"><span data-stu-id="b2d14-192">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="b2d14-193">Platzhalterabgleich</span><span class="sxs-lookup"><span data-stu-id="b2d14-193">Wildcard matching</span></span>  

<span data-ttu-id="b2d14-194">Verwenden Sie das Platzhalterzeichen \( `*` \), um einem oder mehreren Zeichen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-194">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="b2d14-195">Ein Platzhalterpräfix wird in Ursprungszeichenfolgen des Mitglieds verwendet, `url_handlers` um für unterschiedliche Unterdomänen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-195">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="b2d14-196">Das Präfix muss `*.` für diese Verwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-196">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="b2d14-197">Das `https` Schema wird angenommen, wenn Sie ein Platzhalterpräfix verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-197">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="b2d14-198">Beispielsweise ist der `url_handlers` Memberwert auf Übereinstimmungen und `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` festgelegt, aber nicht mit `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="b2d14-198">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a><span data-ttu-id="b2d14-199">Überlagerung von Fenstersteuerelementen für installierte Desktop-Web-Apps</span><span class="sxs-lookup"><span data-stu-id="b2d14-199">Window Controls Overlay for installed desktop web apps</span></span>  

<span data-ttu-id="b2d14-200">Um eine immersive Titelleiste wie eine systemeigene App für Ihre installierte Desktop-Web-App zu erstellen, werden mit der **Window Controls Overlay-Funktion** die folgenden Aktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-200">To create an immersive title bar like a native app for your desktop installed web app, the **Window Controls Overlay** feature completes the following actions.</span></span>  
    
1.  <span data-ttu-id="b2d14-201">Entfernt die vom System reservierte Titelleiste.</span><span class="sxs-lookup"><span data-stu-id="b2d14-201">Removes the system reserved title bar.</span></span>  <span data-ttu-id="b2d14-202">Sie umfasst in der Regel die Breite des Clientframes.</span><span class="sxs-lookup"><span data-stu-id="b2d14-202">It usually spans the width of the client frame.</span></span>  
1.  <span data-ttu-id="b2d14-203">Ersetzt sie durch eine Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-203">Replaces it with an overlay.</span></span>  <span data-ttu-id="b2d14-204">Sie enthält nur die kritischen Fenstersteuerelemente, die für einen Benutzer erforderlich sind, um das Fenster selbst zu steuern.</span><span class="sxs-lookup"><span data-stu-id="b2d14-204">It contains just the critical system required window controls necessary for a user to control the window itself.</span></span>  
    
<span data-ttu-id="b2d14-205">Nachdem eine Überlagerung zur Verfügung steht, steht Ihnen der gesamte Webclientbereich zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-205">After it provides an overlay, the entire web client area is available for you to use.</span></span>  <span data-ttu-id="b2d14-206">Dieses Feature enthält eine Manifestaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-206">This feature includes a manifest update.</span></span>  <span data-ttu-id="b2d14-207">Es bietet Ihnen Möglichkeiten, die Größe und Position der Überlagerung zu bestimmen, um Ihnen bei der Organisation von Inhalten zu helfen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-207">It provides ways for you to determine the size and position of the overlay to help you arrange content.</span></span>  

<span data-ttu-id="b2d14-208">Navigieren Sie zum Anzeigen einer Vorschau der Fenstersteuerelementüberlagerungen in Microsoft Edge für Windows 10 zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features und navigieren Sie zu **Desktop-PWA-Fenstersteuerelemente-Überlagerung**.</span><span class="sxs-lookup"><span data-stu-id="b2d14-208">To preview the Window Controls Overlays in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.</span></span>   

### <a name="examples-of-title-bar-area-customization"></a><span data-ttu-id="b2d14-209">Beispiele für die Anpassung des Titelleistenbereichs</span><span class="sxs-lookup"><span data-stu-id="b2d14-209">Examples of title bar area customization</span></span>  

<span data-ttu-id="b2d14-210">Dieses Feature basiert auf der Möglichkeit in nativen Apps, die Titelleiste anzupassen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-210">This feature is based on the ability in native apps to customize the title bar.</span></span>  <span data-ttu-id="b2d14-211">Sie können eine Titelleiste für wichtige App-Aktionen oder -Benachrichtigungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-211">You may customize a title bar for important app actions or notifications.</span></span>  <span data-ttu-id="b2d14-212">Lesen Sie die folgenden Beispiele für Microsoft Visual Studio Code und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b2d14-212">Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.</span></span>  

#### <a name="visual-studio-code"></a><span data-ttu-id="b2d14-213">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b2d14-213">Visual Studio Code</span></span>  

<span data-ttu-id="b2d14-214">Microsoft Visual Studio Code ist ein beliebter Editor, der auf Electron baut und auf mehreren Desktopplattformen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b2d14-214">Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.</span></span>  

<span data-ttu-id="b2d14-215">Im folgenden Beispiel wird Visual Studio Code die Titelleiste verwendet, um die verfügbare Bildschirmimmobilie zu maximieren, um den aktuellen Dateinamen und die Menüstruktur auf oberster Ebene in die Titelleiste zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-215">The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.</span></span>  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Ein Beispiel für die Titelleiste in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   <span data-ttu-id="b2d14-217">Ein Beispiel für die Titelleiste in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b2d14-217">An example of the title bar in Visual Studio Code</span></span>  
:::image-end:::  

#### <a name="microsoft-teams"></a><span data-ttu-id="b2d14-218">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b2d14-218">Microsoft Teams</span></span>  

<span data-ttu-id="b2d14-219">Die Tools für die Zusammenarbeit und Kommunikation am Arbeitsplatz Microsoft Teams auch mit Electron erstellt und auf mehreren Desktopplattformen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2d14-219">Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.</span></span>  <span data-ttu-id="b2d14-220">Im folgenden Beispiel werden Microsoft Teams und `back` `forward` Navigationsschaltflächen, ein Suchfeld und Benutzerprofilsteuerelemente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-220">In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.</span></span>  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Ein Beispiel für die Titelleiste in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   <span data-ttu-id="b2d14-222">Ein Beispiel für die Titelleiste in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b2d14-222">An example of the title bar in Microsoft Teams</span></span>  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a><span data-ttu-id="b2d14-223">Überlagerungsfenstersteuerelemente in einem framelosen Fenster</span><span class="sxs-lookup"><span data-stu-id="b2d14-223">Overlay Window Controls on a Frameless Window</span></span>  

<span data-ttu-id="b2d14-224">Um den adressierbaren Bereich für Webinhalte zu maximieren, erstellt der Browser ein frameloses Fenster.</span><span class="sxs-lookup"><span data-stu-id="b2d14-224">To maximize the addressable area for web content, the browser creates a frameless window.</span></span>  <span data-ttu-id="b2d14-225">Ein rahmenloses Fenster entfernt alle Browserbenutzeroberflächen, mit Ausnahme der als Überlagerung bereitgestellten Fenstersteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="b2d14-225">A frameless window removes all browser UI, except for the window controls provided as an overlay.</span></span>  <span data-ttu-id="b2d14-226">Mit der Überlagerung von Fenstersteuerelementen können Benutzer die App weiterhin minimieren, maximieren, wiederherstellen und schließen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-226">The window controls overlay allows users to still minimize, maximize, restore, and close the app.</span></span>  <span data-ttu-id="b2d14-227">Darüber hinaus bietet es über das Web-App-Menü Zugriff auf relevante Browsersteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="b2d14-227">It also provides access to relevant browser controls using the web app menu.</span></span>  <span data-ttu-id="b2d14-228">Für Chromium browser enthält die Überlagerung die folgenden Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="b2d14-228">For Chromium-based browsers, the overlay includes the following controls.</span></span>  

*   <span data-ttu-id="b2d14-229">Ein ziehbarer Bereich mit der gleichen Breite und Höhe der einzelnen Fenstersteuerelementschaltflächen</span><span class="sxs-lookup"><span data-stu-id="b2d14-229">A draggable region the same width and height of each of the window control buttons</span></span>  
*   <span data-ttu-id="b2d14-230">Die **Einstellungen und mehr** \(...\)-Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="b2d14-230">The **Settings and more** \(...\) button</span></span>  
*   <span data-ttu-id="b2d14-231">Die Schaltflächen des Fenstersteuerelements minimieren, maximieren, wiederherstellen und schließen</span><span class="sxs-lookup"><span data-stu-id="b2d14-231">The window control buttons minimize, maximize, restore, and close</span></span>  
    
<span data-ttu-id="b2d14-232">Neben den zuvor aufgeführten Steuerelementen wird die in der Überlagerung angezeigte Benutzeroberfläche in den folgenden Szenarien dynamisch angepasst.</span><span class="sxs-lookup"><span data-stu-id="b2d14-232">Besides the previously listed controls, the UI displayed in the overlay is dynamically resized in the following scenarios.</span></span>  

*   <span data-ttu-id="b2d14-233">Wenn eine installierte Web-App gestartet wird, wird der Ursprung der Webseite links vom Menü **Einstellungen** und mehr \(...\) für einige Sekunden angezeigt und wird dann ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-233">When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.</span></span>  
*   <span data-ttu-id="b2d14-234">Wenn ein Benutzer mithilfe des Menüs **Einstellungen** und mehr \(...\) mit einer Erweiterung interagiert, wird das Symbol der Erweiterung in der Überlagerung links neben dem Menü mit drei Punkten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-234">If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.</span></span>  <span data-ttu-id="b2d14-235">Nachdem Sie ein Erweiterungsdialogfeld beendet haben, wird das Symbol aus der Überlagerung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-235">After you exit any extension dialog, the icon is removed from the overlay.</span></span>  
    
| <span data-ttu-id="b2d14-236">Sprachrichtung</span><span class="sxs-lookup"><span data-stu-id="b2d14-236">Language direction</span></span> | <span data-ttu-id="b2d14-237">Überlagerungsspeicherort</span><span class="sxs-lookup"><span data-stu-id="b2d14-237">Overlay location</span></span> | <span data-ttu-id="b2d14-238">Details</span><span class="sxs-lookup"><span data-stu-id="b2d14-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b2d14-239">Von links nach rechts \(LTR\)</span><span class="sxs-lookup"><span data-stu-id="b2d14-239">Left-to-right \(LTR\)</span></span> | <span data-ttu-id="b2d14-240">Links oben im Clientbereich</span><span class="sxs-lookup"><span data-stu-id="b2d14-240">Upper left of the client area</span></span> | <span data-ttu-id="b2d14-241">Die Steuerelemente werden gekippt</span><span class="sxs-lookup"><span data-stu-id="b2d14-241">The controls are flipped</span></span> |  
| <span data-ttu-id="b2d14-242">Von rechts nach links \(RTL\)</span><span class="sxs-lookup"><span data-stu-id="b2d14-242">Right-to-left \(RTL\)</span></span> | <span data-ttu-id="b2d14-243">Obere rechte Ecke des Clientbereichs</span><span class="sxs-lookup"><span data-stu-id="b2d14-243">Upper right corner of the client area</span></span> |  |  

> [!IMPORTANT]
> <span data-ttu-id="b2d14-244">Die Überlagerung befindet sich immer über dem Z-Index des Webinhalts und akzeptiert alle Benutzereingaben, ohne sie an den Webinhalt weiter zu fließen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-244">The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.</span></span>  

### <a name="working-around-the-window-controls-overlay"></a><span data-ttu-id="b2d14-245">Arbeiten an der Überlagerung von Fenstersteuerelementen</span><span class="sxs-lookup"><span data-stu-id="b2d14-245">Working around the Window Controls Overlay</span></span>  

<span data-ttu-id="b2d14-246">Ihre Webinhalte müssen den reservierten Bereich für die Steuerelementüberlagerung beachten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-246">Your web content must be aware of the reserved area for the controls overlay.</span></span>  <span data-ttu-id="b2d14-247">Stellen Sie sicher, dass der reservierte Bereich keine Benutzerinteraktion erwartet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-247">Ensure the reserved area doesn't expect user interaction.</span></span>  <span data-ttu-id="b2d14-248">Fragen Sie den Browser nach dem umgebenden Rechteck und der Sichtbarkeit der Steuerelementüberlagerung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-248">Query the browser for the bounding rectangle and visibility of the controls overlay.</span></span>  <span data-ttu-id="b2d14-249">Die Informationen werden Ihnen über JavaScript-APIs und CSS-Umgebungsvariablen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-249">The information is provided to you through JavaScript APIs and CSS environment variables.</span></span>  

#### <a name="javascript-apis"></a><span data-ttu-id="b2d14-250">JavaScript-APIs</span><span class="sxs-lookup"><span data-stu-id="b2d14-250">JavaScript APIs</span></span>  

<span data-ttu-id="b2d14-251">Mit einem `windowControlsOverlay` neuen Objekt in der Eigenschaft können Sie das `window.navigator` begrenzungsgebundene Rechteck der Steuerelementüberlagerung abfragen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-251">A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.</span></span>  

<span data-ttu-id="b2d14-252">Das `windowControlsOverlay` Objekt verfügt über die folgenden beiden Objekte.</span><span class="sxs-lookup"><span data-stu-id="b2d14-252">The `windowControlsOverlay` object has the following two objects.</span></span>  

*   `getBoundingClientRect()` <span data-ttu-id="b2d14-253"> gibt ein `DOMRect`-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d14-253">returns a `DOMRect` object.</span></span>  <span data-ttu-id="b2d14-254">Das `DOMRect` Objekt stellt den Bereich unter der Fenstersteuerelementüberlagerung dar.</span><span class="sxs-lookup"><span data-stu-id="b2d14-254">The `DOMRect` object represents the area under the window controls overlay.</span></span>  
*   `visible` <span data-ttu-id="b2d14-255">ist ein boolescher Wert, der angibt, dass die Steuerelementüberlagerung gerendert und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-255">is a boolean that indicates that the controls overlay is rendered and displayed.</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="b2d14-256">Aus Datenschutzgründen ist der Zugriff auf Elemente `windowControlsOverlay` `iframe` im Webinhalt nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="b2d14-256">For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.</span></span>  

<span data-ttu-id="b2d14-257">Wenn die Überlagerungsgröße geändert wird, wird ein Ereignis für das Objekt ausgeführt, um den Client zu benachrichtigen, das `geometrychange` `navigator.windowControlsOverlay` Inhaltslayout neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-257">Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.</span></span>  <span data-ttu-id="b2d14-258">Das neu berechnete Inhaltslayout basiert auf dem neuen umgebenden Rechteck der Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-258">The recalculated content layout is based on the new bounding rectangle of the overlay.</span></span>  

#### <a name="css-environment-variables"></a><span data-ttu-id="b2d14-259">CSS-Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="b2d14-259">CSS Environment Variables</span></span>  

<span data-ttu-id="b2d14-260">Neben der JavaScript-API können Sie CSS zum Abfragen des umgebenden Rechtecks der Steuerelementüberlagerung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-260">Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.</span></span>  <span data-ttu-id="b2d14-261">Verwenden Sie die folgenden vier neuen CSS-Umgebungsvariablen zum Abfragen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-261">Use the following four new CSS environment variables to accomplish to query.</span></span>  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a><span data-ttu-id="b2d14-262">Definieren von draggable Regions in Web Content</span><span class="sxs-lookup"><span data-stu-id="b2d14-262">Define Draggable Regions in Web Content</span></span>  

<span data-ttu-id="b2d14-263">Benutzer erwarten, dass sie den oberen Bereich eines Fensters packen und ziehen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-263">Users expect to grab and drag the upper region of a window.</span></span>  <span data-ttu-id="b2d14-264">Um die Erwartungen zu erfüllen, deklarieren Sie bestimmte Teile des Webinhalts als draggable.</span><span class="sxs-lookup"><span data-stu-id="b2d14-264">To accommodate the expectation, declare specific parts of the web content as draggable.</span></span>  
<span data-ttu-id="b2d14-265">Um anzugeben, dass ein Element draggierbar ist, verwenden Sie die WebKit-proprietäre `-webkit-app-region` CSS-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b2d14-265">To specify an element is draggable, use the WebKit-proprietary `-webkit-app-region` CSS property.</span></span>  <span data-ttu-id="b2d14-266">Die CSS-Arbeitsgruppe bemüht sich weiterhin, die Eigenschaft zu `app-region` standardisieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-266">The CSS working group continues efforts to standardize the `app-region` property.</span></span>  

### <a name="custom-title-bar-example"></a><span data-ttu-id="b2d14-267">Beispiel für benutzerdefinierte Titelleiste</span><span class="sxs-lookup"><span data-stu-id="b2d14-267">Custom title bar example</span></span>  

<span data-ttu-id="b2d14-268">Im folgenden Beispiel wird angezeigt, wie die neuen Features eine Web-App mit einer benutzerdefinierten Titelleiste erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-268">The following example displays how the new features create a web app with a custom title bar.</span></span>  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Beispiel für eine benutzerdefinierte Titelleiste in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   <span data-ttu-id="b2d14-270">Beispiel für eine benutzerdefinierte Titelleiste in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b2d14-270">Example of a custom title bar in Microsoft Teams</span></span>  
:::image-end:::  

#### <a name="manifestwebmanifest"></a><span data-ttu-id="b2d14-271">manifest.webmanifest</span><span class="sxs-lookup"><span data-stu-id="b2d14-271">manifest.webmanifest</span></span>  

<span data-ttu-id="b2d14-272">Legen Sie im Manifest array `display_override` auf  `window-controls-overlay` .</span><span class="sxs-lookup"><span data-stu-id="b2d14-272">In the manifest, set `display_override` array to  `window-controls-overlay`.</span></span>  <span data-ttu-id="b2d14-273">Legen Sie die Farbe für die Titelleiste auf `theme_color` Ihre Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="b2d14-273">Set the `theme_color` to your choice of color for the title bar.</span></span>  <span data-ttu-id="b2d14-274">Legen Sie den Anzeigemodus auf einen geeigneten Fallback für den Fall ein, wenn eine oder `display_override` `window-controls-overlay` nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-274">Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.</span></span>  

<span data-ttu-id="b2d14-275">Der folgende Codeausschnitt enthält die empfohlenen Manifestupdates.</span><span class="sxs-lookup"><span data-stu-id="b2d14-275">The following code snippet includes the recommended manifest updates.</span></span>  

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

### <a name="indexhtml"></a><span data-ttu-id="b2d14-276">index.html</span><span class="sxs-lookup"><span data-stu-id="b2d14-276">index.html</span></span>  

<span data-ttu-id="b2d14-277">Die folgenden IDs stellen die beiden Hauptbereiche der Webseite dar.</span><span class="sxs-lookup"><span data-stu-id="b2d14-277">The following IDs represent the two main regions of the webpage.</span></span>  

*   `titleBarContainer`  
*   `mainContent`  
    
<span data-ttu-id="b2d14-278">Das Element mit der ID ist auf festgelegt, und das untergeordnete `div` `titleBar` Suchfeldelement ist auf `draggable` `input` `nonDraggable` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-278">The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.</span></span>  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

<span data-ttu-id="b2d14-279">Im Element mit der ID stellt der mit der ID den sichtbaren Teil des `div` `titleBarContainer` `div` `titleBar` Titelleistenbereichs dar.</span><span class="sxs-lookup"><span data-stu-id="b2d14-279">In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.</span></span>  

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
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a><span data-ttu-id="b2d14-280">style.css</span><span class="sxs-lookup"><span data-stu-id="b2d14-280">style.css</span></span>  

<span data-ttu-id="b2d14-281">Die bereiche draggable und non-draggable werden mit und `-webkit-app-region: drag` `-webkit-app-region: no-drag` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-281">The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.</span></span>  

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

<span data-ttu-id="b2d14-282">Für das Element werden Ränder festgelegt, um sicherzustellen, dass die Titelleiste bis an die Ränder `body` `0` des Fensters reicht.</span><span class="sxs-lookup"><span data-stu-id="b2d14-282">For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.</span></span>  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

<span data-ttu-id="b2d14-283">Die ID verwendet und legt den auf fest, der den Container am `titleBarContainer` oberen Rand der Webseite `position: absolute` `top` `titlebar-area-inset-top` anheften soll.</span><span class="sxs-lookup"><span data-stu-id="b2d14-283">The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.</span></span>  <span data-ttu-id="b2d14-284">Der `bottom` wird auf festgelegt und fällt auf `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` zurück, wenn die Fenstersteuerelementüberlagerung nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b2d14-284">The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.</span></span>  <span data-ttu-id="b2d14-285">Die Hintergrundfarbe der `titleBarContainer` ID ist identisch mit der `theme_color` .</span><span class="sxs-lookup"><span data-stu-id="b2d14-285">The background color of the `titleBarContainer` ID is the same as the `theme_color`.</span></span>  <span data-ttu-id="b2d14-286">Die Breite ist auf festgelegt, sodass das Element die Breite der Webseite ausfüllt und unter der Überlagerung fließt, wenn es für eine zusammenhängende `100%` `div` Darstellung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b2d14-286">The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.</span></span>  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

<span data-ttu-id="b2d14-287">Die ID verwendet und fügt sie auch `titleBar` am oberen Rand des `position: absolute` `top: titlebar-area-inset-top` Fensters an.</span><span class="sxs-lookup"><span data-stu-id="b2d14-287">The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.</span></span>  <span data-ttu-id="b2d14-288">Standardmäßig wird die volle Breite des Fensters verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-288">By default, it consumes the full width of the window.</span></span>  <span data-ttu-id="b2d14-289">The `left` and edges are set to and `right` `titlebar-area-inset-left` `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.</span><span class="sxs-lookup"><span data-stu-id="b2d14-289">The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.</span></span>  <span data-ttu-id="b2d14-290">Außerdem soll verhindert werden, dass versucht wird, das verbrauchte Fenster zu ziehen, stattdessen wird `user-select: none` Text im Element `div` hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="b2d14-290">It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.</span></span>  

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

<span data-ttu-id="b2d14-291">Der Container für die ID wird ebenfalls mit fixiert und am unteren Rand `mainContent` `position: absolute` der Webseite angefügt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-291">The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.</span></span>  <span data-ttu-id="b2d14-292">Der wird auf festgelegt und fällt zurück, um den verbleibenden Platz unterhalb der `height` `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` Titelleiste zu füllen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-292">The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.</span></span>  <span data-ttu-id="b2d14-293">Es wird `overflow-y: scroll` so definiert, dass der Inhalt vertikal im Container scrollen kann.</span><span class="sxs-lookup"><span data-stu-id="b2d14-293">It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.</span></span>  

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

<span data-ttu-id="b2d14-294">In Fällen, in denen der Browser die Überlagerung von Fenstersteuerelementen nicht unterstützt, wird eine CSS-Variable hinzugefügt, um eine Standardhöhe für die Titelleiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-294">For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.</span></span>  <span data-ttu-id="b2d14-295">Die Grenzen von und IDs werden zunächst so festgelegt, dass sie den gesamten Clientbereich füllen, und Sie müssen ihn nicht ändern, wenn die Überlagerung `titleBarContainer` `mainContent` nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-295">The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.</span></span>  

<span data-ttu-id="b2d14-296">Der folgende Codeausschnitt enthält alle empfohlenen CSS-Updates.</span><span class="sxs-lookup"><span data-stu-id="b2d14-296">The following code snippet includes all the recommended CSS updates.</span></span>

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

## <a name="run-on-os-login"></a><span data-ttu-id="b2d14-297">Ausführen unter Betriebssystemanmeldung</span><span class="sxs-lookup"><span data-stu-id="b2d14-297">Run On OS Login</span></span>  

<span data-ttu-id="b2d14-298">Mit diesem Feature können Sie Ihre App so konfigurieren, dass sie automatisch gestartet wird, wenn sich der Benutzer bei Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d14-298">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="b2d14-299">Mehrere Klassen von Apps nutzen die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b2d14-299">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="b2d14-300">Zu den Klassen von Apps gehören E-Mails, Chats, Überwachungsdashboards und Echtzeit-Datenanzeige-Apps.</span><span class="sxs-lookup"><span data-stu-id="b2d14-300">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="b2d14-301">Die Funktion ermöglicht es einem Benutzer, sich mit den Apps zu beschäftigen, sobald sich der Benutzer beim Betriebssystem anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-301">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="b2d14-302">Dieses Feature startet die PWA automatisch auf die gleiche Weise, wie sie manuell gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-302">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b2d14-303">**Ausführen unter Betriebssystemanmeldung** ist ein [leistungsstarkes Feature.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="b2d14-303">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="b2d14-304">Benutzer sollten entscheiden, ob sie die Funktion für die installierte Web-App aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-304">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="b2d14-305">Aktivieren der Anmeldung unter Betriebssystem ausführen</span><span class="sxs-lookup"><span data-stu-id="b2d14-305">Turn on Run On OS Login</span></span>  

<span data-ttu-id="b2d14-306">Navigieren Sie zum Anzeigen einer Vorschau der Run **On Os Login-Funktionen** für PWA zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features und Aktivieren von **Desktop-PWAs,** die unter Betriebssystemanmeldung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-306">To preview the **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Aktivieren des Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt wird" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="b2d14-308">Aktivieren des **Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt** wird</span><span class="sxs-lookup"><span data-stu-id="b2d14-308">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="b2d14-309">Aktivieren des Features für die installierte Web-App</span><span class="sxs-lookup"><span data-stu-id="b2d14-309">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="b2d14-310">Um das Feature `Start app when you sign in` für eine installierte PWA</span><span class="sxs-lookup"><span data-stu-id="b2d14-310">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="b2d14-311">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2d14-311">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="b2d14-312">Navigieren Sie zu `edge://apps`.</span><span class="sxs-lookup"><span data-stu-id="b2d14-312">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="b2d14-313">Zeigen Sie auf Ihre App.</span><span class="sxs-lookup"><span data-stu-id="b2d14-313">Hover on your app.</span></span>  
1.  <span data-ttu-id="b2d14-314">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie dann App starten **aus, wenn Sie sich anmelden.**</span><span class="sxs-lookup"><span data-stu-id="b2d14-314">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Verwenden Sie das Kontextmenü, um die Start-App zu aktivieren, wenn Sie sich in der App Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="b2d14-316">Verwenden Sie das Kontextmenü, um die **Start-App** zu aktivieren, wenn Sie sich in der App Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2d14-316">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="b2d14-317">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="b2d14-317">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="b2d14-318">ist ein neues Mitglied der Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="b2d14-318">is a new member of the manifest file.</span></span>  <span data-ttu-id="b2d14-319">Sie können Links zu Teilen, wichtigen Webseiten oder Aktionen in Ihrer Web-App definieren.</span><span class="sxs-lookup"><span data-stu-id="b2d14-319">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="b2d14-320">Microsoft Windows integriert es als **Jumplists**.</span><span class="sxs-lookup"><span data-stu-id="b2d14-320">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="b2d14-321">**Sprunglisten definieren** Popupmenüs, die angezeigt werden, wenn Sie eines der folgenden Benutzeroberflächenelemente verwenden und ein kontextbezogenes Menü \(rechtsklicken\) öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-321">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="b2d14-322">Eine Kachel im Startmenü</span><span class="sxs-lookup"><span data-stu-id="b2d14-322">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="b2d14-323">Ein Symbol auf der Taskleiste</span><span class="sxs-lookup"><span data-stu-id="b2d14-323">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="b2d14-324">Wenn ein Benutzer eine Verknüpfung aufruft, navigiert der Benutzer zu der vom Element der `url` Verknüpfung angegebenen Adresse.</span><span class="sxs-lookup"><span data-stu-id="b2d14-324">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Ein Beispiel für Jumplists auf Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="b2d14-326">Ein Beispiel für **Jumplists** auf Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2d14-326">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="b2d14-327">Verknüpfungen in der Manifestdatei</span><span class="sxs-lookup"><span data-stu-id="b2d14-327">Shortcuts in the Manifest file</span></span>  

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

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="b2d14-328">Eigenschaften von Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="b2d14-328">Properties of shortcuts</span></span>  

<span data-ttu-id="b2d14-329">Die folgenden Eigenschaften definieren jede Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b2d14-329">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="b2d14-330">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2d14-330">Property</span></span> | <span data-ttu-id="b2d14-331">Details</span><span class="sxs-lookup"><span data-stu-id="b2d14-331">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="b2d14-332">Eine Zeichenfolge, die dem Benutzer auf **Sprunglisten oder** im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-332">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="b2d14-333">Eine Zeichenfolge, die angezeigt wird, wenn nicht genügend Speicherplatz vorhanden ist, um den vollständigen Namen der Verknüpfung anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="b2d14-333">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="b2d14-334">Eine Zeichenfolge, die den Zweck der Verknüpfung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-334">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="b2d14-335">Auf sie kann durch Hilfstechnologie zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="b2d14-335">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="b2d14-336">Der URI in der Web-App, der geöffnet wird, wenn die Verknüpfung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-336">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="b2d14-337">Eine Reihe von Symbolen, die die Verknüpfung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2d14-337">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="b2d14-338">Dateiverarbeitung</span><span class="sxs-lookup"><span data-stu-id="b2d14-338">File Handling</span></span>  

<span data-ttu-id="b2d14-339">Die Möglichkeit, sich als Dateityphandler zu registrieren, befindet sich in der Experimentierphase.</span><span class="sxs-lookup"><span data-stu-id="b2d14-339">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="b2d14-340">Sie können die Dateitypen angeben, die Ihre App in einem Manifesteintrag verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b2d14-340">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="b2d14-341">Während der Installation registriert das Hostbetriebssystem des Benutzers Ihre App als Dateihandler für die aufgeführten Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="b2d14-341">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="b2d14-342">Stellen Sie sicher, dass das Feature im Startcode Ihrer Apps enthalten ist und `launchQueue` die Datei verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b2d14-342">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="b2d14-343">Chromium Browser testen und gestalten dieses Feature.</span><span class="sxs-lookup"><span data-stu-id="b2d14-343">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="b2d14-344">Weitere Informationen einschließlich Codebeispielen finden Sie unter [Let web applications be file handlers][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="b2d14-344">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="b2d14-345">Wenn Sie eine Vorschau der Dateiverarbeitung in Microsoft Edge für Windows 10 anzeigen möchten, navigieren Sie zu Aktivieren experimenteller [Features](#turn-on-experimental-features) und Aktivieren der **Dateibehandlungs-API**.</span><span class="sxs-lookup"><span data-stu-id="b2d14-345">To preview file handling in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="b2d14-346">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="b2d14-346">Providing feedback on experimental features</span></span>  

<span data-ttu-id="b2d14-347">So geben Sie Feedback zu Microsoft Edge Web-App-Experimenten.</span><span class="sxs-lookup"><span data-stu-id="b2d14-347">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="b2d14-348">Senden Sie Ihr Feedback **Einstellungen und mehr** \( `...` \) > Feedback an Microsoft **senden.**</span><span class="sxs-lookup"><span data-stu-id="b2d14-348">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="b2d14-349">Wählen Sie `Alt` + `Shift` + `I` aus.</span><span class="sxs-lookup"><span data-stu-id="b2d14-349">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Senden von Feedback von PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="b2d14-351">Senden von Feedback von PWA</span><span class="sxs-lookup"><span data-stu-id="b2d14-351">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Origin Trials | Microsoft Edge Entwickler"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrieren für die Registrierung von Web App-Protokollhandlern | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Webbasierte Protokollhandler | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Leistungsstarkes Feature – Berechtigungen | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs als URL Handlers | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Webanwendungen als Dateihandler verwenden | web.dev"  
