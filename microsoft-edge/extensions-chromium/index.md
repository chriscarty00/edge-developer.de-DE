---
description: Eine Übersicht über das Erstellen und Veröffentlichen von Microsoft Edge (Chromium)-Erweiterungen.
title: Übersicht über Microsoft Edge (Chromium)-Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, Erweiterungen entwickeln, Browsererweiterungen, Add-Ons, Partner Center, Entwickler, Chromium-Erweiterungen
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327526"
---
# <span data-ttu-id="b9066-104">Übersicht über Microsoft Edge (Chromium)-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b9066-104">Overview of Microsoft Edge (Chromium) Extensions</span></span>  

<span data-ttu-id="b9066-105">Eine Erweiterung ist ein kleines Programm, das Sie zum Hinzufügen oder Ändern von Features für Microsoft Edge \(Chromium\) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9066-105">An extension is a small program that you \(a developer\) use to add or modify features for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="b9066-106">Eine Erweiterung soll die täglichen Browsererfahrungen eines Benutzers verbessern.</span><span class="sxs-lookup"><span data-stu-id="b9066-106">An extension is intended to improve a user's day-to-day browsing experience.</span></span>  <span data-ttu-id="b9066-107">Es bietet Nischenfunktionen, die für eine Zielgruppe wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="b9066-107">It provides niche functionality that is important to a target audience.</span></span>  

<span data-ttu-id="b9066-108">Sie können eine Erweiterung erstellen, wenn Sie über eine Idee oder ein Produkt verfügen, die auf einer der folgenden Bedingungen basiert.</span><span class="sxs-lookup"><span data-stu-id="b9066-108">You may create an extension if you have an idea or product that is based upon either of the following conditions.</span></span>  

*   <span data-ttu-id="b9066-109">Ein bestimmter Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="b9066-109">A specific web browser.</span></span>  
*   <span data-ttu-id="b9066-110">Verbesserungen an features von bestimmten Webseiten.</span><span class="sxs-lookup"><span data-stu-id="b9066-110">Improvements to features of specific webpages.</span></span>  
    
<span data-ttu-id="b9066-111">Beispiele für Begleiterfahrungen sind Anzeigenblocker und Kennwortmanager.</span><span class="sxs-lookup"><span data-stu-id="b9066-111">Examples of companion experiences include ad blockers and password managers.</span></span>  

<span data-ttu-id="b9066-112">Eine Erweiterung ist ähnlich wie eine normale Web-App strukturiert.</span><span class="sxs-lookup"><span data-stu-id="b9066-112">An extension is structured similar to a regular web app.</span></span>  <span data-ttu-id="b9066-113">Sie sollte mindestens die folgenden Features enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9066-113">At a minimum, it should include the following features.</span></span>

*   <span data-ttu-id="b9066-114">Eine App-Manifest-JSON-Datei, die grundlegende Plattforminformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b9066-114">An app manifest JSON file that contains basic platform information.</span></span>  
*   <span data-ttu-id="b9066-115">Eine JavaScript-Datei, die Funktionalität definiert.</span><span class="sxs-lookup"><span data-stu-id="b9066-115">A JavaScript file that define functionality.</span></span>  
*   <span data-ttu-id="b9066-116">HTML- und CSS-Dateien, die die Benutzeroberfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="b9066-116">HTML and CSS files that define the user interface.</span></span>  

<span data-ttu-id="b9066-117">Um direkt mit einem Teil des Browsers zu funktionieren, z. B. mit einem Fenster oder einem Tab, müssen Sie API-Anforderungen senden und häufig auf den Namen des Browsers verweisen.</span><span class="sxs-lookup"><span data-stu-id="b9066-117">To work directly with part of the browser, such as a window or tab, you must send API requests and often reference the browser by name.</span></span>  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Eine Microsoft Edge-Erweiterung (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  <span data-ttu-id="b9066-119">Eine Microsoft Edge-Erweiterung \(Chromium\)</span><span class="sxs-lookup"><span data-stu-id="b9066-119">A Microsoft Edge \(Chromium\) extension</span></span>  
:::image-end:::  

## <span data-ttu-id="b9066-120">Grundlegende Orientierungshilfe</span><span class="sxs-lookup"><span data-stu-id="b9066-120">Basic guidance</span></span>  

<span data-ttu-id="b9066-121">Zu den beliebtesten Browsern zum Erstellen von Erweiterungen gehören Safari, Firefox, Chrome, Opera, Brave und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b9066-121">Some of the most popular browsers to build extensions for include Safari, Firefox, Chrome, Opera, Brave, and Microsoft Edge.</span></span>  <span data-ttu-id="b9066-122">Sehr gute Ausgangspunkte für die Suche nach Anleitungen für die Erweiterungsentwicklung und Dokumentationen sind von den Browser-Organisationen gehostete Websites.</span><span class="sxs-lookup"><span data-stu-id="b9066-122">Great places to begin your extension development tutorials and documentation research are sites hosted by the browser organizations.</span></span>  <span data-ttu-id="b9066-123">Die folgende Tabelle ist nicht endgültig und kann als Ausgangspunkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9066-123">The following table isn't definitive, and may be used as a starting point.</span></span>  

| <span data-ttu-id="b9066-124">Webbrowser</span><span class="sxs-lookup"><span data-stu-id="b9066-124">Web browser</span></span> | <span data-ttu-id="b9066-125">Chromium-basiert?</span><span class="sxs-lookup"><span data-stu-id="b9066-125">Chromium-based?</span></span> | <span data-ttu-id="b9066-126">Webseite zur Erweiterungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="b9066-126">Extension development webpage</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b9066-127">Safari</span><span class="sxs-lookup"><span data-stu-id="b9066-127">Safari</span></span> | <span data-ttu-id="b9066-128">Nein</span><span class="sxs-lookup"><span data-stu-id="b9066-128">No</span></span> | [<span data-ttu-id="b9066-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span><span class="sxs-lookup"><span data-stu-id="b9066-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span></span>][AppleDeveloperSafariservicesAppExtensions] |  
| <span data-ttu-id="b9066-130">Firefox</span><span class="sxs-lookup"><span data-stu-id="b9066-130">Firefox</span></span> | <span data-ttu-id="b9066-131">Nein</span><span class="sxs-lookup"><span data-stu-id="b9066-131">No</span></span> | [<span data-ttu-id="b9066-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span><span class="sxs-lookup"><span data-stu-id="b9066-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span></span>][MDNWebextensions] |  
| <span data-ttu-id="b9066-133">Chrom</span><span class="sxs-lookup"><span data-stu-id="b9066-133">Chrome</span></span> | <span data-ttu-id="b9066-134">Ja</span><span class="sxs-lookup"><span data-stu-id="b9066-134">Yes</span></span> | [<span data-ttu-id="b9066-135">developer.chrome.com/extensions</span><span class="sxs-lookup"><span data-stu-id="b9066-135">developer.chrome.com/extensions</span></span>][ChromeDeveloperExtensions] |  
| <span data-ttu-id="b9066-136">Opera</span><span class="sxs-lookup"><span data-stu-id="b9066-136">Opera</span></span> | <span data-ttu-id="b9066-137">Ja</span><span class="sxs-lookup"><span data-stu-id="b9066-137">Yes</span></span> | [<span data-ttu-id="b9066-138">dev.opera.com/extensions</span><span class="sxs-lookup"><span data-stu-id="b9066-138">dev.opera.com/extensions</span></span>][OperaDevExtensions] |  
| <span data-ttu-id="b9066-139">Brave</span><span class="sxs-lookup"><span data-stu-id="b9066-139">Brave</span></span> | <span data-ttu-id="b9066-140">Ja</span><span class="sxs-lookup"><span data-stu-id="b9066-140">Yes</span></span> | <span data-ttu-id="b9066-141">Verwendet [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span><span class="sxs-lookup"><span data-stu-id="b9066-141">Uses [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span></span> |  
| <span data-ttu-id="b9066-142">neuer Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b9066-142">new Microsoft Edge</span></span> | <span data-ttu-id="b9066-143">Ja</span><span class="sxs-lookup"><span data-stu-id="b9066-143">Yes</span></span> | [<span data-ttu-id="b9066-144">developer.microsoft.com/microsoft-edge/extensions</span><span class="sxs-lookup"><span data-stu-id="b9066-144">developer.microsoft.com/microsoft-edge/extensions</span></span>][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> <span data-ttu-id="b9066-145">Viele Lernprogramme der Websites verwenden browserspezifische APIs, die möglicherweise nicht mit dem Browser übereinstimmen, für den Sie entwickeln.</span><span class="sxs-lookup"><span data-stu-id="b9066-145">Many of the tutorials of the sites use browser-specific APIs that may not match the browser for which you develop.</span></span>  <span data-ttu-id="b9066-146">In den meisten Fällen funktioniert eine Chromium-Erweiterung in unterschiedlichen Chromium-Browsern auf die gleiche Weise, und die APIs funktionieren erwartungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b9066-146">In most cases, a Chromium extension works as-is in different Chromium browsers and the APIs work as expected.</span></span>  <span data-ttu-id="b9066-147">Nur einige seltener verwendete APIs sind möglicherweise strikt browserspezifisch.</span><span class="sxs-lookup"><span data-stu-id="b9066-147">Only some less common APIs may be strictly browser-specific.</span></span>  <span data-ttu-id="b9066-148">Links zu den Lernprogrammen finden Sie unter [Siehe auch](#see-also).</span><span class="sxs-lookup"><span data-stu-id="b9066-148">For links to the tutorials, navigate to [See also](#see-also).</span></span>  

## <span data-ttu-id="b9066-149">Warum Chromium?</span><span class="sxs-lookup"><span data-stu-id="b9066-149">Why Chromium?</span></span>  

<span data-ttu-id="b9066-150">Wenn Sie Ihre Erweiterung im Erweiterungsspeicher für jeden Browser veröffentlichen möchten, muss sie für jede Version so geändert werden, dass sie in jeder unterschiedlichen Browserumgebung ziel- und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9066-150">If your goal is to publish your extension in the extensions store for each browser, it must be modified for each version to target and run in each distinct browser environment.</span></span>  <span data-ttu-id="b9066-151">Beispielsweise können [Safari-Erweiterungen][AppleDeveloperSafariservicesAppExtensions] sowohl Web- als auch systemeigenen Code verwenden, um mit entsprechenden systemeigenen Anwendungen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="b9066-151">For example, [Safari extensions][AppleDeveloperSafariservicesAppExtensions] may use both web and native code to communicate with counterpart native applications.</span></span>  <span data-ttu-id="b9066-152">Die letzten vier Browser in der vorherigen Tabelle verwenden dasselbe Codepaket und minimieren die Notwendigkeit, parallele Versionen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b9066-152">The last four browsers in the previous table use the same code package, and minimizes the requirement to maintain parallel versions.</span></span>  <span data-ttu-id="b9066-153">Diese Browser basieren auf dem [Open-Source-Projekt Chromium.][|::ref1::|Home]</span><span class="sxs-lookup"><span data-stu-id="b9066-153">These browsers are based on the [Chromium open-source project][|::ref1::|Home].</span></span>  

<span data-ttu-id="b9066-154">Erstellen Sie eine Chromium-Erweiterung, um die geringste Menge an Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b9066-154">Create a Chromium extension to write the least amount of code.</span></span>  <span data-ttu-id="b9066-155">Es richtet sich auch an die maximale Anzahl von Erweiterungsspeichern und letztendlich an die maximale Anzahl von Benutzern, die Ihre Erweiterung finden und erwerben.</span><span class="sxs-lookup"><span data-stu-id="b9066-155">It also targets the maximum number of extension stores and ultimately the maximum number of users who find and acquire your extension.</span></span>  

<span data-ttu-id="b9066-156">Im Folgenden geht es hauptsächlich um Chromium-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="b9066-156">The following content focuses mostly on Chromium extensions.</span></span>  

## <span data-ttu-id="b9066-157">Browser-Kompatibilität und Erweiterungstests</span><span class="sxs-lookup"><span data-stu-id="b9066-157">Browser compatibility and extension testing</span></span>  

<span data-ttu-id="b9066-158">Gelegentlich ist die API-Parität zwischen Chromium-Browsern nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b9066-158">Occasionally, API parity doesn't exist between Chromium browsers.</span></span>  <span data-ttu-id="b9066-159">So gibt es beispielsweise Unterschiede zwischen den Identitäts- und Zahlungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="b9066-159">For example, there are differences in the identity and payment APIs.</span></span>  <span data-ttu-id="b9066-160">Um sicherzustellen, dass Ihre Erweiterung die Erwartungen der Kunden erfüllt, überprüfen Sie den API-Status in den folgenden offiziellen Browser-Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="b9066-160">To ensure your extension meets customer expectations, review API status through the following official browser docs.</span></span>  

*   [<span data-ttu-id="b9066-161">Chrome-APIs</span><span class="sxs-lookup"><span data-stu-id="b9066-161">Chrome APIs</span></span>][ChromeDeveloperExtensionsApiIndex]  
*   [<span data-ttu-id="b9066-162">In Opera unterstützte Erweiterungs-APIs</span><span class="sxs-lookup"><span data-stu-id="b9066-162">Extension APIs supported in Opera</span></span>][OperaDevExtensionsApis]  
*   [<span data-ttu-id="b9066-163">Port chrome extension to Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="b9066-163">Port Chrome extension to Microsoft Edge (Chromium)</span></span>][ExtensionsChromiumDeveloperGuidePortChrome]  
    
<span data-ttu-id="b9066-164">Die von Ihnen benötigten APIs definieren die Änderungen, die Sie vornehmen müssen, um die Unterschiede zwischen den einzelnen Browsern zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="b9066-164">The APIs you require define the changes you must make to address the differences between each browser.</span></span>  <span data-ttu-id="b9066-165">Dies kann bedeuten, dass Sie für jeden Speicher geringfügig unterschiedliche Codepakete mit kleinen Unterschieden erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="b9066-165">It may mean that you must create slightly different code packages with small differences for each store.</span></span>  

<span data-ttu-id="b9066-166">Um Ihre Erweiterung in verschiedenen Umgebungen zu testen, bevor Sie sie an einen Browserspeicher übermitteln, laden Sie sie während der Entwicklung quer in Ihren Browser.</span><span class="sxs-lookup"><span data-stu-id="b9066-166">To test your extension in different environments before you submit it to a browser store, sideload it into your browser while you develop it.</span></span>  

## <span data-ttu-id="b9066-167">Veröffentlichen Ihrer Erweiterung in Browserstores</span><span class="sxs-lookup"><span data-stu-id="b9066-167">Publish your extension to browser stores</span></span>  

<span data-ttu-id="b9066-168">Browsererweiterungen können bei den folgenden Browserstores eingereicht und darin gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="b9066-168">You may submit and seek browser extensions in the following browser stores.</span></span>  

*   [<span data-ttu-id="b9066-169">Add-ons für Firefox </span><span class="sxs-lookup"><span data-stu-id="b9066-169">Firefox Browser Add-ons</span></span>][MozillaAddonsFirefoxExtensions]  
*   [<span data-ttu-id="b9066-170">Chrome Web Store</span><span class="sxs-lookup"><span data-stu-id="b9066-170">Chrome Web Store</span></span>][GoogleChromeWebstoreCategoryExtensions]  
*   [<span data-ttu-id="b9066-171">Opera Add-ons</span><span class="sxs-lookup"><span data-stu-id="b9066-171">Opera addons</span></span>][OperaAddonsExtensions]  
*   [<span data-ttu-id="b9066-172">Microsoft Edge Add-ons</span><span class="sxs-lookup"><span data-stu-id="b9066-172">Microsoft Edge Add-ons</span></span>][MicrosoftEdgeAddonsCategoryExtensions]  

<span data-ttu-id="b9066-173">Einige Stores ermöglichen es, gelistete Erweiterungen über andere Browser herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="b9066-173">Some stores allow you to download listed extensions from other browsers.</span></span>  <span data-ttu-id="b9066-174">Der browserübergreifende Zugriff ist jedoch nicht für jeden Store garantiert.</span><span class="sxs-lookup"><span data-stu-id="b9066-174">However, cross-browser access is not guaranteed by browser stores.</span></span>  <span data-ttu-id="b9066-175">Um sicherzustellen, dass Ihre Benutzer Ihre Erweiterung in verschiedenen Browsern finden, sollten Sie einen Eintrag in jedem Browsererweiterungsspeicher verwalten.</span><span class="sxs-lookup"><span data-stu-id="b9066-175">To ensure your users find your extension in different browsers, you should maintain a listing on each browser extension store.</span></span>  

<span data-ttu-id="b9066-176">Benutzer müssen Ihre Erweiterung möglicherweise in verschiedenen Browsern installieren.</span><span class="sxs-lookup"><span data-stu-id="b9066-176">Users may need to install your extension in different browsers.</span></span> <span data-ttu-id="b9066-177">In diesem Szenario können Sie vorhandene Chromium-Erweiterungen von einem Browser in einen anderen migrieren.</span><span class="sxs-lookup"><span data-stu-id="b9066-177">In this scenario, you may migrate existing Chromium extensions from one browser to another.</span></span>  

### <span data-ttu-id="b9066-178">Migrieren einer bestehenden Erweiterung zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b9066-178">Migrate an existing extension to Microsoft Edge</span></span>  

<span data-ttu-id="b9066-179">Wenn Sie bereits eine Erweiterung für einen anderen Chromium-Browser entwickelt haben, können Sie sie an den Microsoft Edge-Add-Ons-Speicher übermitteln.</span><span class="sxs-lookup"><span data-stu-id="b9066-179">If you've already developed an extension for another Chromium browser, you may submit it to the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="b9066-180">Sie müssen Ihre Erweiterung nicht umschreiben und überprüfen, ob sie in Microsoft Edge funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b9066-180">You don't need to rewrite your extension, and must verify it works in Microsoft Edge.</span></span>  <span data-ttu-id="b9066-181">Wenn Sie eine vorhandene Chromium-Erweiterung zu anderen Chromium-Browsern migrieren, stellen Sie sicher, dass für Ihren Zielbrowser dieselben APIs oder Alternativen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b9066-181">When you migrate an existing Chromium extension to other Chromium browsers, ensure the same APIs or alternatives are available for your target browser.</span></span>  

<span data-ttu-id="b9066-182">Weitere Informationen zum Portieren Ihrer Chrome-Erweiterung zu Microsoft Edge finden Sie unter Portieren von [Chrome-Erweiterungen zu Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome]</span><span class="sxs-lookup"><span data-stu-id="b9066-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span></span> <span data-ttu-id="b9066-183">Nachdem Sie Ihre Erweiterung auf den Zielbrowser portierst, besteht der nächste Schritt in der Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="b9066-183">After you port your extension to the target browser, the next step is to publish it.</span></span>  

### <span data-ttu-id="b9066-184">Veröffentlichen auf der Microsoft Edge-Add-Ons-Website</span><span class="sxs-lookup"><span data-stu-id="b9066-184">Publish to the Microsoft Edge add-ons website</span></span>  

<span data-ttu-id="b9066-185">Um mit der Veröffentlichung Ihrer [][MicrosoftDeveloperRegistration] Erweiterung in Microsoft Edge zu beginnen, müssen Sie sich für ein Entwicklerkonto mit einem MSA-E-Mail-Konto registrieren, um Ihren Erweiterungseintrag an den Store zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="b9066-185">To start publishing your extension to Microsoft Edge, you must [register for a developer account][MicrosoftDeveloperRegistration] with an MSA email account to submit your extension listing to the store.</span></span>  <span data-ttu-id="b9066-186">Ein MSA-E-Mail-Konto enthält `@outlook.com` `@live.com` , und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b9066-186">An MSA email account includes `@outlook.com`, `@live.com`, and so on.</span></span>  <span data-ttu-id="b9066-187">Wenn Sie eine zu registrierende E-Mail-Adresse auswählen, sollten Sie überlegen, ob Sie den Besitz der Erweiterung an andere Personen in Ihrer Organisation übertragen oder teilen müssen.</span><span class="sxs-lookup"><span data-stu-id="b9066-187">When you choose an email address to register, consider if you must transfer or share ownership of the extension with others in your organization.</span></span>  <span data-ttu-id="b9066-188">Nach Abschluss der Registrierung erstellen Sie eventuell eine neue Erweiterungseinreichung für den Store.</span><span class="sxs-lookup"><span data-stu-id="b9066-188">After registration is complete, you may create a new extension submission to the store.</span></span>  

<span data-ttu-id="b9066-189">Um Ihre Erweiterung an den Store zu übermitteln, stellen Sie sicher, dass Sie die folgenden Elemente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b9066-189">To submit your extension to the store, ensure you provide the following items.</span></span>  

*   <span data-ttu-id="b9066-190">Eine Archivdatei `.zip` \( \), die Ihre Codedateien enthält.</span><span class="sxs-lookup"><span data-stu-id="b9066-190">An archive \(`.zip`\) file that contains your code files.</span></span>  
*   <span data-ttu-id="b9066-191">Alle erforderlichen visuellen Ressourcen, die ein Logo und eine kleine Werbekachel enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9066-191">All required visual assets, which include a logo and small promotional tile.</span></span>  
*   <span data-ttu-id="b9066-192">Optionale Werbemedien, z. B. Screenshots, Werbekacheln und eine Video-URL.</span><span class="sxs-lookup"><span data-stu-id="b9066-192">Optional promotional media, such as screenshots, promotional tiles, and a video URL.</span></span>  
*   <span data-ttu-id="b9066-193">Informationen, die Ihre Erweiterung beschreiben, z. B. den Namen, eine kurze Beschreibung und einen Link zu Datenschutzrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="b9066-193">Information that describes your extension such as the name, short description, and a privacy policy link.</span></span>  

> [!NOTE]
> <span data-ttu-id="b9066-194">In den verschiedenen Stores gelten möglicherweise unterschiedliche Anforderungen für die Einreichung.</span><span class="sxs-lookup"><span data-stu-id="b9066-194">Different stores may have different submission requirements.</span></span>  <span data-ttu-id="b9066-195">In der obigen Liste sind die [Anforderungen zum Veröffentlichen][ExtensionsChromiumPublish] einer Erweiterung für Microsoft Edge zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b9066-195">The above list summarizes the [requirements][ExtensionsChromiumPublish] to publish an extension for Microsoft Edge.</span></span>  

<span data-ttu-id="b9066-196">Nachdem Sie Ihre Erweiterung erfolgreich übermittelt haben, wird ihre Erweiterung einem Überprüfungsprozess unterzogen und besteht den Zertifizierungsprozess entweder durch oder schlägt diesen fehl.</span><span class="sxs-lookup"><span data-stu-id="b9066-196">After you've successfully submitted your extension, your extension undergoes a review process and either passes or fails the certification process.</span></span>  <span data-ttu-id="b9066-197">Die Besitzer werden über das Ergebnis und die nächsten Schritte benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b9066-197">Owners are notified of the outcome and given next steps as required.</span></span>  <span data-ttu-id="b9066-198">Wenn Sie ein Erweiterungsupdate an den Speicher übermitteln, wird ein neuer Überprüfungsprozess gestartet.</span><span class="sxs-lookup"><span data-stu-id="b9066-198">If you submit an extension update to the store, a new review process is started.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9066-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9066-199">See also</span></span>  

*   [<span data-ttu-id="b9066-200">Portierung einer Google Chrome-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b9066-200">Port a Google Chrome extension</span></span>][ExtensionworkshopPorting]  
*   [<span data-ttu-id="b9066-201">Erstellen einer Safari-App-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b9066-201">Build a Safari App extension</span></span>][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [<span data-ttu-id="b9066-202">Ihre erste Erweiterung (Firefox)</span><span class="sxs-lookup"><span data-stu-id="b9066-202">Your first extension (Firefox)</span></span>][MDNWebextensionsYourFirst]  
*   [<span data-ttu-id="b9066-203">Lernprogramm "Erste Schritte" (Chrome)</span><span class="sxs-lookup"><span data-stu-id="b9066-203">Get started tutorial (Chrome)</span></span>][ChromeDeveloperExtensionsGetstarted]  
*   [<span data-ttu-id="b9066-204">Erste Schritte (Opera)</span><span class="sxs-lookup"><span data-stu-id="b9066-204">Get started (Opera)</span></span>][OperaDevExtensionsGettingStarted]  
*   [<span data-ttu-id="b9066-205">Erste Schritte mit Microsoft Edge (Chromium)-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b9066-205">Get started with Microsoft Edge (Chromium) extensions</span></span>][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port chrome extension to Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Veröffentlichen einer Erweiterung | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Entwickeln von Erweiterungen für Microsoft Edge | Microsoft-Entwickler"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Microsoft-Entwickler"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Erweiterungen für Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Safari-App-Erweiterungen | Apple-Entwickler"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Erstellen einer Safari-App-Erweiterung | Apple-Entwickler"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Was sind Erweiterungen? | Chrome-Entwickler"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Chrome-APIs | Chrome-Entwickler"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial für die ersten Schritte | Chrome-Entwickler"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portieren einer Google Chrome-Erweiterung | Erweiterungs-Workshop"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Erweiterungen | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Browser-Erweiterungen | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Ihre erste Erweiterung | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Erweiterungen | Firefox Add-ons"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Erweiterungen | Opera-Add-ons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Erweiterungsdokumentation | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "In Opera unterstützten Erweiterungs-APIs | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Erste Schritte | Dev. Opera"  
