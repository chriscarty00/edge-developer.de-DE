---
description: Machen Sie Ihre PWA durch Veröffentlichung im Microsoft Store besser auf entdeckungsfähiger
title: Veröffentlichen Ihrer Progressive Web App im Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: progressive Web-Apps, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 68471535446a2270a23b32205717da225fd9e4bf
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461521"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="25123-104">Veröffentlichen Ihrer Progressive Web App im Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="25123-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="25123-105">Die Veröffentlichung Ihrer Progressive Web App \(PWA\) im [Microsoft Store][WindowsUwpPublishIndex] bietet die folgenden Vorteile.</span><span class="sxs-lookup"><span data-stu-id="25123-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="25123-106">Erkennbarkeit</span><span class="sxs-lookup"><span data-stu-id="25123-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="25123-107">Benutzer suchen natürlich nach Apps im App Store.</span><span class="sxs-lookup"><span data-stu-id="25123-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="25123-108">Durch die Veröffentlichung im Microsoft Store können Millionen von Windows-Benutzern Ihre PWA zusammen mit anderen Windows-Apps ermitteln.</span><span class="sxs-lookup"><span data-stu-id="25123-108">By publishing to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="25123-109">Im Store werden Apps über Kategorien, kuratierte Sammlungen und vieles mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25123-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="25123-110">Die App-Discovery-Portale bieten potenziellen Benutzern Ihrer App ein einfaches Browsen und Einkaufserlebnis.</span><span class="sxs-lookup"><span data-stu-id="25123-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="25123-111">Sie können Ihren [Store-Eintrag sogar][WindowsUwpPublishAppScreenshotsImages] um Screenshots, ein Heldenbild und Videotrailer erweitern.</span><span class="sxs-lookup"><span data-stu-id="25123-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="25123-112">Vertrauenswürdigkeit</span><span class="sxs-lookup"><span data-stu-id="25123-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="25123-113">Windows-Kunden wissen, dass sie ihren Microsoft Store-Käufen und Downloads vertrauen können, da sie die strengen [Microsoft-Qualitäts- und Sicherheitsstandards einhalten.][LegalWindowsAgreementsStorePolicies]</span><span class="sxs-lookup"><span data-stu-id="25123-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="25123-114">Einfache Installation</span><span class="sxs-lookup"><span data-stu-id="25123-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="25123-115">Der Microsoft Store bietet eine konsistente und benutzerfreundliche Installationserfahrung in [allen Windows 10-Apps.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="25123-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="25123-116">App-Analyse</span><span class="sxs-lookup"><span data-stu-id="25123-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="25123-117">Das [Windows Partner Center-Dashboard][WindowsUwpPublishIndex] bietet Ihnen [detaillierte][WindowsUwpPublishAnalytics] Analysen zu Ihrer App-Integrität, -Nutzung und vielem mehr.</span><span class="sxs-lookup"><span data-stu-id="25123-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="25123-118">Um Ihre PWA im Microsoft Store zu veröffentlichen, sind keine Codeänderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25123-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="25123-119">Stattdessen erstellen Sie eine App-Reservierung, packen Ihre PWA und übermitteln Ihr Paket an den Store.</span><span class="sxs-lookup"><span data-stu-id="25123-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="25123-120">In den folgenden Abschnitten werden die Schritte erläutert.</span><span class="sxs-lookup"><span data-stu-id="25123-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="25123-121">Erstellen einer App-Reservierung</span><span class="sxs-lookup"><span data-stu-id="25123-121">Create an app reservation</span></span>  

<span data-ttu-id="25123-122">[Windows Partner Center ist][MicrosoftPartnerDashboardWindowsOverview] der Hub, an dem Sie Ihre App an den Microsoft Store übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="25123-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="25123-123">Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="25123-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="25123-124">Führen Sie die folgenden Aktionen aus, um die registrierten Programme anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="25123-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="25123-125">Melden Sie sich mit Ihrem Microsoft-Konto beim Windows Partner Center an, und navigieren Sie zum [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span><span class="sxs-lookup"><span data-stu-id="25123-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="25123-126">Navigieren zu **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="25123-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="25123-127">Wenn **Windows & Xbox** angezeigt wird, ist Ihre App bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="25123-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="25123-128">Wenn **Windows & Xbox** nicht angezeigt wird, wählen Sie Programm hinzufügen **aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Hinzufügen eines Programms im Windows Partner Center-Dashboard" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="25123-130">Hinzufügen eines Programms im Windows Partner Center-Dashboard</span><span class="sxs-lookup"><span data-stu-id="25123-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="25123-131">Führen Sie die folgenden Aktionen aus, um sich beim Entwicklerprogramm zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="25123-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="25123-132">Navigieren Sie **zu Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="25123-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="25123-133">Wählen **Sie Erste Schritte aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="25123-134">Befolgen Sie die Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="25123-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="25123-135">Jetzt ist Ihre App im App-Entwicklerprogramm registriert.</span><span class="sxs-lookup"><span data-stu-id="25123-135">Now, your app is enrolled in the app developer program.</span></span> <span data-ttu-id="25123-136">Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="25123-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="25123-137">Navigieren Sie **zu Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="25123-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="25123-138">Wählen **Sie Übersicht**Erstellen einer neuen App  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="25123-139">Geben Sie ihren PWA-Namen in die Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="25123-139">Type your PWA name in the prompt.</span></span>  
    1.  <span data-ttu-id="25123-140">Wählen Sie `Reserve product name` aus.</span><span class="sxs-lookup"><span data-stu-id="25123-140">Choose `Reserve product name`.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Erstellen einer App-Reservierung im Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="25123-142">Erstellen einer App-Reservierung im Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="25123-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="25123-143">Wählen Sie **Produktverwaltung**Produktidentität aus, um Ihre Herausgeberdetails für die Verwendung im Abschnitt [Paket Ihres PWA](#package-your-pwa)  >  **anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="25123-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Kopieren von Herausgeberinformationen aus Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="25123-145">Kopieren von Herausgeberinformationen aus Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="25123-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="25123-146">Kopieren und speichern Sie die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="25123-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="25123-147">Paket-ID</span><span class="sxs-lookup"><span data-stu-id="25123-147">Package ID</span></span>**  
    *   **<span data-ttu-id="25123-148">Herausgeber-ID</span><span class="sxs-lookup"><span data-stu-id="25123-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="25123-149">Publisher-Anzeigename</span><span class="sxs-lookup"><span data-stu-id="25123-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa"></a><span data-ttu-id="25123-150">Packen Ihres PWA</span><span class="sxs-lookup"><span data-stu-id="25123-150">Package your PWA</span></span>  

<span data-ttu-id="25123-151">Generieren Sie ein Windows-App-Paket für Ihre PWA.</span><span class="sxs-lookup"><span data-stu-id="25123-151">Generate a Windows app package for your PWA.</span></span>  

<span data-ttu-id="25123-152">Das App-Paket ist eine Datei, die die Metadaten Ihrer App enthält, einschließlich `.msixbundle` Name, Beschreibung, Symbolen und so weiter.</span><span class="sxs-lookup"><span data-stu-id="25123-152">Your app package is an `.msixbundle` file that contains the metadata of your app including the name, description, icons, and so on.</span></span>  <span data-ttu-id="25123-153">Es verwendet das [gehostete App-Modell,][WindowsBlogWindowsdeveloperHostedAppModel]und Microsoft Edge unterstützt Ihre PWA.</span><span class="sxs-lookup"><span data-stu-id="25123-153">It uses the [Hosted App Model][WindowsBlogWindowsdeveloperHostedAppModel], with Microsoft Edge powering your PWA.</span></span>  <span data-ttu-id="25123-154">In diesem Modell verwendet Ihre PWA moderne Webfunktionen, während sie als Windows-App funktioniert.</span><span class="sxs-lookup"><span data-stu-id="25123-154">In this model, your PWA uses modern web capabilities while functioning as a Windows app.</span></span>  <span data-ttu-id="25123-155">Zu den modernen Webfunktionen gehören Service worker, offline, Pushbenachrichtigungen, Badging und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="25123-155">Modern web capabilities include service worker, offline, push notifications, badging, and more.</span></span>  

<span data-ttu-id="25123-156">Führen Sie die folgenden Aktionen aus, um ein App-Paket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="25123-156">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="25123-157">Navigieren Sie zu [PWA Builder][PwabuilderMain].</span><span class="sxs-lookup"><span data-stu-id="25123-157">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="25123-158">Geben Sie die URL Ihres PWA ein.</span><span class="sxs-lookup"><span data-stu-id="25123-158">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="25123-159">Wählen **Sie Start**Build My  >  **PWA**  >  **Windows**Options  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-159">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="25123-160">Fügen Sie die folgenden Werte ein, die Sie im Abschnitt [Erstellen einer App-Reservierung gespeichert](#create-an-app-reservation) haben.</span><span class="sxs-lookup"><span data-stu-id="25123-160">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="25123-161">Paket-ID</span><span class="sxs-lookup"><span data-stu-id="25123-161">Package ID</span></span>**  
    *   **<span data-ttu-id="25123-162">Herausgeber-ID</span><span class="sxs-lookup"><span data-stu-id="25123-162">Publisher ID</span></span>**  
    *   **<span data-ttu-id="25123-163">Publisher-Anzeigename</span><span class="sxs-lookup"><span data-stu-id="25123-163">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Einfügen von Herausgeberinformationen in PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="25123-165">Einfügen von Herausgeberinformationen in PWABuilder</span><span class="sxs-lookup"><span data-stu-id="25123-165">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25123-166">Wählen Sie **Fertig**aus.</span><span class="sxs-lookup"><span data-stu-id="25123-166">Choose **Done**.</span></span>  
1.  <span data-ttu-id="25123-167">Wenn Sie Ihr Windows-App-Paket herunterladen möchten, wählen Sie **Herunterladen aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-167">To download your Windows app package, choose **Download**.</span></span>  <span data-ttu-id="25123-168">Ihr Download ist ein `.zip` Archiv mit einer `.msixbundle` Datei.</span><span class="sxs-lookup"><span data-stu-id="25123-168">Your download is a `.zip` archive containing an `.msixbundle` file.</span></span>  <span data-ttu-id="25123-169">Verwenden Sie `.msixbundle` die Datei im Abschnitt Senden Ihres [App-Pakets an den Store.](#submit-your-app-package-to-the-store)</span><span class="sxs-lookup"><span data-stu-id="25123-169">Use the `.msixbundle` file in the [Submit your app package to the Store](#submit-your-app-package-to-the-store) section.</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="25123-170">Übermitteln Ihres App-Pakets an den Store</span><span class="sxs-lookup"><span data-stu-id="25123-170">Submit your app package to the Store</span></span>  

<span data-ttu-id="25123-171">Jetzt haben Sie Ihr `.msixbundle` App-Paket.</span><span class="sxs-lookup"><span data-stu-id="25123-171">Now, you have your `.msixbundle` app package.</span></span>  <span data-ttu-id="25123-172">Führen Sie die folgenden Aktionen aus, um Ihr App-Paket an den Store zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="25123-172">To submit your app package to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="25123-173">Navigieren zu [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="25123-173">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="25123-174">Wählen Sie Ihre App aus.</span><span class="sxs-lookup"><span data-stu-id="25123-174">Choose your app.</span></span>  
1.  <span data-ttu-id="25123-175">Wählen **Sie Übermittlung starten aus.**</span><span class="sxs-lookup"><span data-stu-id="25123-175">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Starten einer neuen App-Übermittlung im Windows Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="25123-177">Starten einer neuen App-Übermittlung im Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="25123-177">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25123-178">Führen Sie die folgenden Eingabeaufforderungen für Informationen zu Ihrer App aus.</span><span class="sxs-lookup"><span data-stu-id="25123-178">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="25123-179">pricing</span><span class="sxs-lookup"><span data-stu-id="25123-179">pricing</span></span>  
    *   <span data-ttu-id="25123-180">Altersfreigabe</span><span class="sxs-lookup"><span data-stu-id="25123-180">age rating</span></span>  
    *   <span data-ttu-id="25123-181">und mehr</span><span class="sxs-lookup"><span data-stu-id="25123-181">and more</span></span>  
        
1.  <span data-ttu-id="25123-182">Wählen Sie **in der Paketaufforderung** die Datei aus, die Sie `.msixbundle` im Abschnitt Paket Ihren [PWA generiert](#package-your-pwa) haben.</span><span class="sxs-lookup"><span data-stu-id="25123-182">On the **Packages** prompt, choose the `.msixbundle` file your generated in the [Package your PWA](#package-your-pwa) section.</span></span>  

<span data-ttu-id="25123-183">Nachdem Sie ihre Übermittlung abgeschlossen haben, wird Ihre App in der Regel innerhalb von 24 bis 48 Stunden überprüft.</span><span class="sxs-lookup"><span data-stu-id="25123-183">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="25123-184">Nachdem Sie die Genehmigung erhalten haben, ist Ihr PWA im Microsoft Store verfügbar.</span><span class="sxs-lookup"><span data-stu-id="25123-184">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store-Richtlinien | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analysieren der Leistung | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "App-Screenshots, Bilder und Trailer | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Veröffentlichen von Windows-Apps und | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Startseite | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressourcen für Partner| Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Windows-Entwicklerblog"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  

