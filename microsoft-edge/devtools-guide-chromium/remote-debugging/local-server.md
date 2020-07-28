---
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: daa96b604d5ad48a9de49dd24dc38eab79de9c9b
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898214"
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





# <span data-ttu-id="d8fe4-103">Zugreifen auf lokale Server</span><span class="sxs-lookup"><span data-stu-id="d8fe4-103">Access Local Servers</span></span>   




<span data-ttu-id="d8fe4-104">Hosten Sie eine Website auf einem Entwicklungscomputer-Webserver, und greifen Sie dann auf den Inhalt eines Android-Geräts zu.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-104">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="d8fe4-105">Führen Sie mit einem USB-Kabel und Microsoft Edge devtools eine Website von einem Entwicklungscomputer aus, und zeigen Sie dann die Website auf einem Android-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-105">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="d8fe4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d8fe4-106">Summary</span></span>  

*   <span data-ttu-id="d8fe4-107">Mit der Port Weiterleitung können Sie Inhalte anzeigen, die von dem Webserver gehostet werden, der auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-107">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="d8fe4-108">Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät für den Zugriff auf den Inhalt dieser Domäne mit benutzerdefinierter Domänenzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-108">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="d8fe4-109">Einrichten der Portweiterleitung</span><span class="sxs-lookup"><span data-stu-id="d8fe4-109">Set up port forwarding</span></span>   

<span data-ttu-id="d8fe4-110">Mit der Port Weiterleitung kann Ihr Android-Gerät auf Inhalte zugreifen, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-110">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="d8fe4-111">Die Port Weiterleitung funktioniert durch Erstellen eines abhörenden TCP-Ports auf Ihrem Android-Gerät, der einem TCP-Port auf dem Entwicklungscomputer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-111">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="d8fe4-112">Der Datenverkehr zwischen den Anschlüssen durchläuft die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-112">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="d8fe4-113">So aktivieren Sie die Portweiterleitung:</span><span class="sxs-lookup"><span data-stu-id="d8fe4-113">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="d8fe4-114">Richten Sie das [Remotedebuggen][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-114">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="d8fe4-115">Wenn Sie den Vorgang beenden, sollten Sie Ihr Android-Gerät im linken Menü des Dialogfelds " **Geräte prüfen** " und einer **verbundenen** Statusanzeige sehen.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-115">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="d8fe4-116">Aktivieren Sie im Dialogfeld **Geräte prüfen** in devtools die **Port Weiterleitung**.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-116">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="d8fe4-117">Wählen Sie **Regel hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-117">Select **Add rule**.</span></span>  
    
    > ##### <span data-ttu-id="d8fe4-118">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="d8fe4-118">Figure 1</span></span>  
    > <span data-ttu-id="d8fe4-119">Hinzufügen einer Port Weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="d8fe4-119">Adding a port forwarding rule</span></span>  
    > ![Hinzufügen einer Port Weiterleitungsregel][ImageAddRule]  
    
1.  <span data-ttu-id="d8fe4-121">Geben Sie im Textfeld **Device Port** auf der linken Seite die Portnummer ein, auf der `localhost` Sie auf Ihrem Android-Gerät auf die Website zugreifen können möchten.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="d8fe4-122">Wenn Sie beispielsweise auf die Website von Enter aus zugreifen `localhost:5000` möchten `5000` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="d8fe4-123">Geben Sie im Textfeld **lokale Adresse** auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf Ihrem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="d8fe4-124">Beispiel: Wenn Ihre Website auf Enter ausgeführt wird `localhost:7331` `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="d8fe4-125">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-125">Select **Add**.</span></span>  

<span data-ttu-id="d8fe4-126">Die Port Weiterleitung ist nun eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="d8fe4-127">Sehen Sie sich die Statusanzeige für den Port Forward auf der Registerkarte auf Ihrem Gerät im Dialogfeld " **Geräte überprüfen** " an.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-127">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

> ##### <span data-ttu-id="d8fe4-128">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="d8fe4-128">Figure 2</span></span>  
> <span data-ttu-id="d8fe4-129">Port Weiterleitungsstatus</span><span class="sxs-lookup"><span data-stu-id="d8fe4-129">Port forwarding status</span></span>  
> ![Port Weiterleitungsstatus][ImagePortForwardingStatus]  

<span data-ttu-id="d8fe4-131">Wenn Sie den Inhalt anzeigen möchten, öffnen Sie Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem `localhost` Port, den Sie im Feld **Device Port** festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-131">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="d8fe4-132">Wenn Sie beispielsweise `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-132">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="d8fe4-133">Zuordnen zu benutzerdefinierten lokalen Domänen</span><span class="sxs-lookup"><span data-stu-id="d8fe4-133">Map to custom local domains</span></span>   

<span data-ttu-id="d8fe4-134">Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf dem Entwicklungscomputer anzeigen, auf dem eine benutzerdefinierte Domäne verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-134">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="d8fe4-135">Nehmen wir beispielsweise an, dass Ihre Website eine JavaScript-Bibliothek eines Drittanbieters verwendet, die nur in der Domäne funktioniert `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-135">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="d8fe4-136">So erstellen Sie einen Eintrag in Ihrer `hosts` Datei auf Ihrem Entwicklungscomputer, um diese Domäne an `localhost` \ (beispielsweise `127.0.0.1 microsoft-edge.devtools` \) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-136">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="d8fe4-137">Nachdem Sie die benutzerdefinierte Domänenzuordnung und Portweiterleitung eingerichtet haben, können Sie die Website auf Ihrem Android-Gerät unter der URL anzeigen `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-137">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="d8fe4-138">Einrichten der Portweiterleitung an Proxy Server</span><span class="sxs-lookup"><span data-stu-id="d8fe4-138">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="d8fe4-139">Wenn Sie eine benutzerdefinierte Domäne zuordnen möchten, müssen Sie einen Proxy Server auf Ihrem Entwicklungscomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-139">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="d8fe4-140">Beispiele für Proxy Server sind [Charles][CharlesWebDebuggingProxy], [squid][SquidOptimisingWebDelivery]und [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="d8fe4-140">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="d8fe4-141">So richten Sie die Portweiterleitung an einen Proxy ein:</span><span class="sxs-lookup"><span data-stu-id="d8fe4-141">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="d8fe4-142">Führen Sie den Proxy Server aus, und notieren Sie den verwendeten Port.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-142">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d8fe4-143">Der Proxy Server und Ihr Webserver müssen auf unterschiedlichen Ports ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-143">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="d8fe4-144">Richten Sie die [Portweiterleitung](#set-up-port-forwarding) auf Ihr Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-144">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="d8fe4-145">Geben Sie für das Feld **lokale Adresse** `localhost:` den Port ein, auf dem Ihr Proxy Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-145">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="d8fe4-146">Wenn Sie beispielsweise auf Port ausgeführt wird `8000` , besuchen Sie `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-146">For example, if it is running on port `8000`, visit `localhost:8000`.</span></span>  <span data-ttu-id="d8fe4-147">Geben Sie im Feld **Device Port** die Nummer ein, die Ihr Android-Gerät hören soll, beispielsweise `3333` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-147">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  

### <span data-ttu-id="d8fe4-148">Konfigurieren von Proxyeinstellungen auf Ihrem Gerät</span><span class="sxs-lookup"><span data-stu-id="d8fe4-148">Configure proxy settings on your device</span></span>  

<span data-ttu-id="d8fe4-149">Als nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxy Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-149">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="d8fe4-150">Wechseln Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-150">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="d8fe4-151">Lange – drücken Sie den Namen des Netzwerks, mit dem Sie gerade verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-151">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d8fe4-152">Proxy Einstellungen gelten pro Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-152">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="d8fe4-153">Wählen Sie **Netzwerk ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-153">Select **Modify network**.</span></span>  
1.  <span data-ttu-id="d8fe4-154">Wählen Sie **Erweiterte Optionen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-154">Select **Advanced options**.</span></span>  <span data-ttu-id="d8fe4-155">Die Proxyeinstellungen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-155">The proxy settings display.</span></span>  
1.  <span data-ttu-id="d8fe4-156">Wählen Sie das **Proxy** -Menü und dann **manuell**aus.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-156">Select the **Proxy** menu and select **Manual**.</span></span>  
1.  <span data-ttu-id="d8fe4-157">Geben Sie für das Feld **Proxy Hostname** ein `localhost` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-157">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="d8fe4-158">Geben Sie im Feld **Proxy Port** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteanschluss** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-158">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="d8fe4-159">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-159">Select **Save**.</span></span>  

<span data-ttu-id="d8fe4-160">Mit diesen Einstellungen leitet Ihr Gerät alle seine Anforderungen an den Proxy auf dem Entwicklungscomputer weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-160">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="d8fe4-161">Der Proxy stellt Anforderungen für Ihr Gerät, damit Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-161">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="d8fe4-162">Auf Ihrem Android-Gerät können Sie nun auf benutzerdefinierte Domänen zugreifen, genau wie auf dem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-162">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="d8fe4-163">Wenn Ihr Webserver von einem nicht standardmäßigen Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-163">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="d8fe4-164">Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne `microsoft-edge.devtools` am Port verwendet `7331` , sollten Sie die URL verwenden, wenn Sie die Website von Ihrem Android-Gerät aus anzeigen `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="d8fe4-164">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="d8fe4-165">Wenn Sie das normale Browsen fortsetzen möchten, denken Sie daran, die Proxyeinstellungen auf Ihrem Android-Gerät zurückzusetzen, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-165">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

<!--  -->  



<!-- image links -->  

[ImageAddRule]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png "Abbildung 1: Hinzufügen einer Port Weiterleitungsregel"  
[ImagePortForwardingStatus]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png "Abbildung 2: Port Weiterleitungsstatus"  

<!-- links -->  

[RemoteDebuggingGettingStarted]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit dem Remote Debuggen von Android-Geräten"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging-Proxy"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: Optimieren der Web-Zustellung"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-Free Web Debugging Proxy"  

> [!NOTE]
> <span data-ttu-id="d8fe4-172">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d8fe4-173">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8fe4-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d8fe4-175">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8fe4-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
