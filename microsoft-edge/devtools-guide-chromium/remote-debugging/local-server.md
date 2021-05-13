---
description: Hosten Sie eine Website auf einem Webserver des Entwicklungscomputers, und greifen Sie dann über ein Android-Gerät auf die Inhalte zu.
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2d721a0ccd27befc7a59726f4c5ef9227042b30b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565092"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="access-local-servers"></a><span data-ttu-id="36dc5-104">Zugreifen auf lokale Server</span><span class="sxs-lookup"><span data-stu-id="36dc5-104">Access local servers</span></span>  

<span data-ttu-id="36dc5-105">Hosten Sie eine Website auf einem Webserver des Entwicklungscomputers, und greifen Sie dann von einem Android-Gerät auf die Inhalte zu.</span><span class="sxs-lookup"><span data-stu-id="36dc5-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="36dc5-106">Führen Sie mit einem MICROSOFT EDGE devTools eine Website von einem Entwicklungscomputer aus aus, und zeigen Sie die Website dann auf einem Android-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="36dc5-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <a name="summary"></a><span data-ttu-id="36dc5-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="36dc5-107">Summary</span></span>  

*   <span data-ttu-id="36dc5-108">Mit der Port weiterleitung können Sie Inhalte anzeigen, die vom Webserver auf Ihrem Entwicklungscomputer auf Ihrem Android-Gerät gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="36dc5-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="36dc5-109">Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät ein, um mit benutzerdefinierter Domänenzuordnung auf den Inhalt dieser Domäne zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="36dc5-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <a name="set-up-port-forwarding"></a><span data-ttu-id="36dc5-110">Einrichten der Port weiterleitung</span><span class="sxs-lookup"><span data-stu-id="36dc5-110">Set up port forwarding</span></span>  

<span data-ttu-id="36dc5-111">Die Port weiterleitung ermöglicht Ihrem Android-Gerät den Zugriff auf Inhalte, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36dc5-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="36dc5-112">Die Port weiterleitung funktioniert, indem sie einen lauschenden TCP-Port auf Ihrem Android-Gerät erstellt, der einem TCP-Port auf Ihrem Entwicklungscomputer zuteil wird.</span><span class="sxs-lookup"><span data-stu-id="36dc5-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="36dc5-113">Der Datenverkehr zwischen den Ports wird über die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer übertragen, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="36dc5-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="36dc5-114">So aktivieren Sie die Port weiterleitung:</span><span class="sxs-lookup"><span data-stu-id="36dc5-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="36dc5-115">Einrichten des [Remotedebu debuggings][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät.</span><span class="sxs-lookup"><span data-stu-id="36dc5-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="36dc5-116">Wenn Sie fertig sind, sollte Ihr Android-Gerät im linken \*\*\*\* Menü des Dialogfelds Geräte überprüfen und eine Statusanzeige **verbunden** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="36dc5-116">When you are finished, your Android device should be displayed in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="36dc5-117">Aktivieren Sie **im Dialogfeld Geräte** überprüfen in DevTools port **forwarding**.</span><span class="sxs-lookup"><span data-stu-id="36dc5-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="36dc5-118">Wählen Sie **Add rule**aus.</span><span class="sxs-lookup"><span data-stu-id="36dc5-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Hinzufügen einer Port weiterleitungsregel" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="36dc5-120">Hinzufügen einer Port weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="36dc5-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="36dc5-121">Geben Sie im Textfeld **Geräteport** auf der linken Seite die Portnummer ein, von der aus Sie auf die Website auf Ihrem `localhost` Android-Gerät zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="36dc5-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="36dc5-122">Wenn Sie z. B. über die Eingabe auf die Website `localhost:5000` zugreifen `5000` möchten.</span><span class="sxs-lookup"><span data-stu-id="36dc5-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="36dc5-123">Geben Sie **im** Textfeld Lokale Adresse auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf dem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.</span><span class="sxs-lookup"><span data-stu-id="36dc5-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="36dc5-124">Wenn Ihre Website z. B. bei der Eingabe `localhost:7331` ausgeführt `localhost:7331` wird.</span><span class="sxs-lookup"><span data-stu-id="36dc5-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="36dc5-125">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="36dc5-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="36dc5-126">Die Port weiterleitung ist jetzt eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="36dc5-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="36dc5-127">Überprüfen Sie die Statusanzeige für den Port vorwärts auf der Registerkarte ihres Geräts im Dialogfeld **Geräte** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="36dc5-127">Review the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Status der Port weiterleitung" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="36dc5-129">Status der Port weiterleitung</span><span class="sxs-lookup"><span data-stu-id="36dc5-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="36dc5-130">Öffnen Sie zum Anzeigen des Inhalts Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem Port, den Sie im Feld `localhost` **Geräteport angegeben** haben.</span><span class="sxs-lookup"><span data-stu-id="36dc5-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="36dc5-131">Wenn Sie z. B. `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="36dc5-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <a name="map-to-custom-local-domains"></a><span data-ttu-id="36dc5-132">Zuordnung zu benutzerdefinierten lokalen Domänen</span><span class="sxs-lookup"><span data-stu-id="36dc5-132">Map to custom local domains</span></span>  

<span data-ttu-id="36dc5-133">Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf Ihrem Entwicklungscomputer anzeigen, der eine benutzerdefinierte Domäne verwendet.</span><span class="sxs-lookup"><span data-stu-id="36dc5-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="36dc5-134">Angenommen, Ihre Website verwendet eine JavaScript-Bibliothek eines Drittanbieters, die nur in der Domäne `microsoft-edge.devtools` funktioniert.</span><span class="sxs-lookup"><span data-stu-id="36dc5-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="36dc5-135">Sie erstellen also einen Eintrag in Ihrer Datei auf dem Entwicklungscomputer, um diese Domäne `hosts` `localhost` \(z. B. `127.0.0.1 microsoft-edge.devtools` \) zu zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="36dc5-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="36dc5-136">Nachdem Sie die benutzerdefinierte Domänenzuordnung und Port weiterleitung eingerichtet haben, zeigen Sie die Website auf Ihrem Android-Gerät unter der URL `microsoft-edge.devtools` an.</span><span class="sxs-lookup"><span data-stu-id="36dc5-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <a name="set-up-port-forwarding-to-proxy-server"></a><span data-ttu-id="36dc5-137">Einrichten der Port weiterleitung an den Proxyserver</span><span class="sxs-lookup"><span data-stu-id="36dc5-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="36dc5-138">Zum Zuordnung einer benutzerdefinierten Domäne müssen Sie einen Proxyserver auf dem Entwicklungscomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="36dc5-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="36dc5-139">Beispiele für Proxyserver sind [Charles][CharlesWebDebuggingProxy], [Squid][SquidCacheWiki]und [Fiddler][TelerikFiddler].</span><span class="sxs-lookup"><span data-stu-id="36dc5-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidCacheWiki], and [Fiddler][TelerikFiddler].</span></span>  

<span data-ttu-id="36dc5-140">So richten Sie die Port weiterleitung an einen Proxy ein:</span><span class="sxs-lookup"><span data-stu-id="36dc5-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="36dc5-141">Führen Sie den Proxyserver aus, und zeichnen Sie den verwendeten Port auf.</span><span class="sxs-lookup"><span data-stu-id="36dc5-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="36dc5-142">Der Proxyserver und der Webserver müssen an unterschiedlichen Ports ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="36dc5-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="36dc5-143">Richten Sie [die Port-Weiterleitung an](#set-up-port-forwarding) Ihr Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="36dc5-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="36dc5-144">Geben Sie **für das feld lokale** Adresse gefolgt vom Port ein, auf dem Der `localhost:` Proxyserver ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36dc5-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="36dc5-145">Wenn sie beispielsweise im Port ausgeführt `8000` wird, navigieren Sie zu `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="36dc5-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="36dc5-146">Geben Sie **im Feld Geräteport** die Nummer ein, auf der Ihr Android-Gerät lauschen soll, z. B. `3333` .</span><span class="sxs-lookup"><span data-stu-id="36dc5-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <a name="configure-proxy-settings-on-your-device"></a><span data-ttu-id="36dc5-147">Konfigurieren von Proxyeinstellungen auf Ihrem Gerät</span><span class="sxs-lookup"><span data-stu-id="36dc5-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="36dc5-148">Als Nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxyserver konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="36dc5-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="36dc5-149">Navigieren Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **WLAN.**</span><span class="sxs-lookup"><span data-stu-id="36dc5-149">On your Android device, navigate to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="36dc5-150">Drücken Sie lange den Namen des Netzwerks, mit dem Sie derzeit verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="36dc5-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="36dc5-151">Proxyeinstellungen gelten pro Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="36dc5-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="36dc5-152">Wählen **Sie Netzwerk ändern aus.**</span><span class="sxs-lookup"><span data-stu-id="36dc5-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="36dc5-153">Wählen **Sie Erweiterte Optionen aus.**</span><span class="sxs-lookup"><span data-stu-id="36dc5-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="36dc5-154">Die Proxyeinstellungen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36dc5-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="36dc5-155">Wählen Sie das **Menü Proxy** aus, und wählen Sie **Manuell aus.**</span><span class="sxs-lookup"><span data-stu-id="36dc5-155">Choose the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="36dc5-156">Geben Sie **für das Feld Proxyhostname** `localhost` ein.</span><span class="sxs-lookup"><span data-stu-id="36dc5-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="36dc5-157">Geben Sie **für das Feld Proxyport** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteport** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="36dc5-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="36dc5-158">Wählen Sie **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="36dc5-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="36dc5-159">Mit diesen Einstellungen gibt Ihr Gerät alle Anforderungen an den Proxy auf Ihrem Entwicklungscomputer weiter.</span><span class="sxs-lookup"><span data-stu-id="36dc5-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="36dc5-160">Der Proxy stellt Anforderungen im Auftrag Ihres Geräts, sodass Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="36dc5-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="36dc5-161">Greifen Sie jetzt wie auf dem Entwicklungscomputer auf benutzerdefinierte Domänen auf Ihrem Android-Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="36dc5-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="36dc5-162">Wenn auf Ihrem Webserver ein nicht standardmäßiger Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.</span><span class="sxs-lookup"><span data-stu-id="36dc5-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="36dc5-163">Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne am Port verwendet, sollten Sie die URL verwenden, wenn Sie die Website von Ihrem `microsoft-edge.devtools` `7331` Android-Gerät aus `microsoft-edge.devtools:7331` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="36dc5-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="36dc5-164">Denken Sie zum Fortsetzen des normalen Browsens daran, die Proxyeinstellungen auf Ihrem Android-Gerät wiederhergestellt zu haben, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.</span><span class="sxs-lookup"><span data-stu-id="36dc5-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="36dc5-165">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="36dc5-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging Proxy"  

[SquidCacheWiki]: https://wiki.squid-cache.org "Squid Wiki Proxy Wiki"  

[TelerikFiddler]: https://www.telerik.com/fiddler "Fiddler – Free Web Debugging Proxy"  

> [!NOTE]
> <span data-ttu-id="36dc5-170">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36dc5-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="36dc5-171">Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="36dc5-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="36dc5-173">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="36dc5-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
