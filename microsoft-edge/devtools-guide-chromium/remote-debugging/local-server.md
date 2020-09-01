---
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fb8f8aabaf426685417f90e25295f3e8e7b08994
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984907"
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





# <span data-ttu-id="cacf2-103">Zugreifen auf lokale Server</span><span class="sxs-lookup"><span data-stu-id="cacf2-103">Access local servers</span></span>   




<span data-ttu-id="cacf2-104">Hosten Sie eine Website auf einem Entwicklungscomputer-Webserver, und greifen Sie dann auf den Inhalt eines Android-Geräts zu.</span><span class="sxs-lookup"><span data-stu-id="cacf2-104">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="cacf2-105">Führen Sie mit einem USB-Kabel und Microsoft Edge devtools eine Website von einem Entwicklungscomputer aus, und zeigen Sie dann die Website auf einem Android-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="cacf2-105">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="cacf2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cacf2-106">Summary</span></span>  

*   <span data-ttu-id="cacf2-107">Mit der Port Weiterleitung können Sie Inhalte anzeigen, die von dem Webserver gehostet werden, der auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cacf2-107">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="cacf2-108">Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät für den Zugriff auf den Inhalt dieser Domäne mit benutzerdefinierter Domänenzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="cacf2-108">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="cacf2-109">Einrichten der Portweiterleitung</span><span class="sxs-lookup"><span data-stu-id="cacf2-109">Set up port forwarding</span></span>   

<span data-ttu-id="cacf2-110">Mit der Port Weiterleitung kann Ihr Android-Gerät auf Inhalte zugreifen, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cacf2-110">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="cacf2-111">Die Port Weiterleitung funktioniert durch Erstellen eines abhörenden TCP-Ports auf Ihrem Android-Gerät, der einem TCP-Port auf dem Entwicklungscomputer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cacf2-111">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="cacf2-112">Der Datenverkehr zwischen den Anschlüssen durchläuft die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="cacf2-112">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="cacf2-113">So aktivieren Sie die Portweiterleitung:</span><span class="sxs-lookup"><span data-stu-id="cacf2-113">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="cacf2-114">Richten Sie das [Remotedebuggen][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="cacf2-114">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="cacf2-115">Wenn Sie den Vorgang beenden, sollten Sie Ihr Android-Gerät im linken Menü des Dialogfelds " **Geräte prüfen** " und einer **verbundenen** Statusanzeige sehen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-115">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="cacf2-116">Aktivieren Sie im Dialogfeld **Geräte prüfen** in devtools die **Port Weiterleitung**.</span><span class="sxs-lookup"><span data-stu-id="cacf2-116">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="cacf2-117">Wählen Sie **Regel hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-117">Select **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Hinzufügen einer Port Weiterleitungsregel" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="cacf2-119">Hinzufügen einer Port Weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="cacf2-119">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cacf2-120">Geben Sie im Textfeld **Device Port** auf der linken Seite die Portnummer ein, auf der `localhost` Sie auf Ihrem Android-Gerät auf die Website zugreifen können möchten.</span><span class="sxs-lookup"><span data-stu-id="cacf2-120">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="cacf2-121">Wenn Sie beispielsweise auf die Website von Enter aus zugreifen `localhost:5000` möchten `5000` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-121">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="cacf2-122">Geben Sie im Textfeld **lokale Adresse** auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf Ihrem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.</span><span class="sxs-lookup"><span data-stu-id="cacf2-122">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="cacf2-123">Beispiel: Wenn Ihre Website auf Enter ausgeführt wird `localhost:7331` `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-123">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="cacf2-124">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-124">Select **Add**.</span></span>  
    
<span data-ttu-id="cacf2-125">Die Port Weiterleitung ist nun eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="cacf2-125">Port forwarding is now set up.</span></span>  <span data-ttu-id="cacf2-126">Sehen Sie sich die Statusanzeige für den Port Forward auf der Registerkarte auf Ihrem Gerät im Dialogfeld " **Geräte überprüfen** " an.</span><span class="sxs-lookup"><span data-stu-id="cacf2-126">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Port Weiterleitungsstatus" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="cacf2-128">Port Weiterleitungsstatus</span><span class="sxs-lookup"><span data-stu-id="cacf2-128">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="cacf2-129">Wenn Sie den Inhalt anzeigen möchten, öffnen Sie Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem `localhost` Port, den Sie im Feld **Device Port** festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="cacf2-129">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="cacf2-130">Wenn Sie beispielsweise `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-130">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="cacf2-131">Zuordnen zu benutzerdefinierten lokalen Domänen</span><span class="sxs-lookup"><span data-stu-id="cacf2-131">Map to custom local domains</span></span>   

<span data-ttu-id="cacf2-132">Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf dem Entwicklungscomputer anzeigen, auf dem eine benutzerdefinierte Domäne verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cacf2-132">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="cacf2-133">Nehmen wir beispielsweise an, dass Ihre Website eine JavaScript-Bibliothek eines Drittanbieters verwendet, die nur in der Domäne funktioniert `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-133">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="cacf2-134">So erstellen Sie einen Eintrag in Ihrer `hosts` Datei auf Ihrem Entwicklungscomputer, um diese Domäne an `localhost` \ (beispielsweise `127.0.0.1 microsoft-edge.devtools` \) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-134">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="cacf2-135">Nachdem Sie die benutzerdefinierte Domänenzuordnung und Portweiterleitung eingerichtet haben, können Sie die Website auf Ihrem Android-Gerät unter der URL anzeigen `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-135">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="cacf2-136">Einrichten der Portweiterleitung an Proxy Server</span><span class="sxs-lookup"><span data-stu-id="cacf2-136">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="cacf2-137">Wenn Sie eine benutzerdefinierte Domäne zuordnen möchten, müssen Sie einen Proxy Server auf Ihrem Entwicklungscomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-137">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="cacf2-138">Beispiele für Proxy Server sind [Charles][CharlesWebDebuggingProxy], [squid][SquidOptimisingWebDelivery]und [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="cacf2-138">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="cacf2-139">So richten Sie die Portweiterleitung an einen Proxy ein:</span><span class="sxs-lookup"><span data-stu-id="cacf2-139">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="cacf2-140">Führen Sie den Proxy Server aus, und notieren Sie den verwendeten Port.</span><span class="sxs-lookup"><span data-stu-id="cacf2-140">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cacf2-141">Der Proxy Server und Ihr Webserver müssen auf unterschiedlichen Ports ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cacf2-141">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="cacf2-142">Richten Sie die [Portweiterleitung](#set-up-port-forwarding) auf Ihr Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="cacf2-142">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="cacf2-143">Geben Sie für das Feld **lokale Adresse** `localhost:` den Port ein, auf dem Ihr Proxy Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cacf2-143">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="cacf2-144">Wenn Sie beispielsweise auf Port ausgeführt wird `8000` , besuchen Sie `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-144">For example, if it is running on port `8000`, visit `localhost:8000`.</span></span>  <span data-ttu-id="cacf2-145">Geben Sie im Feld **Device Port** die Nummer ein, die Ihr Android-Gerät hören soll, beispielsweise `3333` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-145">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="cacf2-146">Konfigurieren von Proxyeinstellungen auf Ihrem Gerät</span><span class="sxs-lookup"><span data-stu-id="cacf2-146">Configure proxy settings on your device</span></span>  

<span data-ttu-id="cacf2-147">Als nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxy Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cacf2-147">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="cacf2-148">Wechseln Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="cacf2-148">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="cacf2-149">Lange – drücken Sie den Namen des Netzwerks, mit dem Sie gerade verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="cacf2-149">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cacf2-150">Proxy Einstellungen gelten pro Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cacf2-150">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="cacf2-151">Wählen Sie **Netzwerk ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-151">Select **Modify network**.</span></span>  
1.  <span data-ttu-id="cacf2-152">Wählen Sie **Erweiterte Optionen**aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-152">Select **Advanced options**.</span></span>  <span data-ttu-id="cacf2-153">Die Proxyeinstellungen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cacf2-153">The proxy settings display.</span></span>  
1.  <span data-ttu-id="cacf2-154">Wählen Sie das **Proxy** -Menü und dann **manuell**aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-154">Select the **Proxy** menu and select **Manual**.</span></span>  
1.  <span data-ttu-id="cacf2-155">Geben Sie für das Feld **Proxy Hostname** ein `localhost` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-155">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="cacf2-156">Geben Sie im Feld **Proxy Port** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteanschluss** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cacf2-156">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="cacf2-157">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="cacf2-157">Select **Save**.</span></span>  
    
<span data-ttu-id="cacf2-158">Mit diesen Einstellungen leitet Ihr Gerät alle seine Anforderungen an den Proxy auf dem Entwicklungscomputer weiter.</span><span class="sxs-lookup"><span data-stu-id="cacf2-158">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="cacf2-159">Der Proxy stellt Anforderungen für Ihr Gerät, damit Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="cacf2-159">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="cacf2-160">Auf Ihrem Android-Gerät können Sie nun auf benutzerdefinierte Domänen zugreifen, genau wie auf dem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="cacf2-160">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="cacf2-161">Wenn Ihr Webserver von einem nicht standardmäßigen Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.</span><span class="sxs-lookup"><span data-stu-id="cacf2-161">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="cacf2-162">Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne `microsoft-edge.devtools` am Port verwendet `7331` , sollten Sie die URL verwenden, wenn Sie die Website von Ihrem Android-Gerät aus anzeigen `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="cacf2-162">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="cacf2-163">Wenn Sie das normale Browsen fortsetzen möchten, denken Sie daran, die Proxyeinstellungen auf Ihrem Android-Gerät zurückzusetzen, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.</span><span class="sxs-lookup"><span data-stu-id="cacf2-163">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

<!--  
  


-->  
<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging-Proxy"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: Optimieren der Web-Zustellung"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-Free Web Debugging Proxy"  

> [!NOTE]
> <span data-ttu-id="cacf2-168">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cacf2-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cacf2-169">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cacf2-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cacf2-171">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cacf2-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
