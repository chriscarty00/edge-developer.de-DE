---
description: Hosten Sie eine Website auf einem Entwicklungscomputer-Webserver, und greifen Sie dann auf den Inhalt eines Android-Geräts zu.
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: f994092460f090743119d7304bfe12aa28556b19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125412"
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

# <span data-ttu-id="e655e-104">Zugreifen auf lokale Server</span><span class="sxs-lookup"><span data-stu-id="e655e-104">Access local servers</span></span>  

<span data-ttu-id="e655e-105">Hosten Sie eine Website auf einem Entwicklungscomputer-Webserver, und greifen Sie dann auf den Inhalt eines Android-Geräts zu.</span><span class="sxs-lookup"><span data-stu-id="e655e-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="e655e-106">Führen Sie mit einem USB-Kabel und Microsoft Edge devtools eine Website von einem Entwicklungscomputer aus, und zeigen Sie dann die Website auf einem Android-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="e655e-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="e655e-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e655e-107">Summary</span></span>  

*   <span data-ttu-id="e655e-108">Mit der Port Weiterleitung können Sie Inhalte anzeigen, die von dem Webserver gehostet werden, der auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e655e-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="e655e-109">Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät für den Zugriff auf den Inhalt dieser Domäne mit benutzerdefinierter Domänenzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="e655e-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="e655e-110">Einrichten der Portweiterleitung</span><span class="sxs-lookup"><span data-stu-id="e655e-110">Set up port forwarding</span></span>  

<span data-ttu-id="e655e-111">Mit der Port Weiterleitung kann Ihr Android-Gerät auf Inhalte zugreifen, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e655e-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="e655e-112">Die Port Weiterleitung funktioniert durch Erstellen eines abhörenden TCP-Ports auf Ihrem Android-Gerät, der einem TCP-Port auf dem Entwicklungscomputer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e655e-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="e655e-113">Der Datenverkehr zwischen den Anschlüssen durchläuft die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="e655e-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="e655e-114">So aktivieren Sie die Portweiterleitung:</span><span class="sxs-lookup"><span data-stu-id="e655e-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="e655e-115">Richten Sie das [Remotedebuggen][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="e655e-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="e655e-116">Wenn Sie den Vorgang beenden, sollten Sie Ihr Android-Gerät im linken Menü des Dialogfelds " **Geräte prüfen** " und einer **verbundenen** Statusanzeige sehen.</span><span class="sxs-lookup"><span data-stu-id="e655e-116">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="e655e-117">Aktivieren Sie im Dialogfeld **Geräte prüfen** in devtools die **Port Weiterleitung**.</span><span class="sxs-lookup"><span data-stu-id="e655e-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="e655e-118">Wählen Sie **Regel hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="e655e-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Hinzufügen einer Port Weiterleitungsregel" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="e655e-120">Hinzufügen einer Port Weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="e655e-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e655e-121">Geben Sie im Textfeld **Device Port** auf der linken Seite die Portnummer ein, auf der `localhost` Sie auf Ihrem Android-Gerät auf die Website zugreifen können möchten.</span><span class="sxs-lookup"><span data-stu-id="e655e-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="e655e-122">Wenn Sie beispielsweise auf die Website von Enter aus zugreifen `localhost:5000` möchten `5000` .</span><span class="sxs-lookup"><span data-stu-id="e655e-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="e655e-123">Geben Sie im Textfeld **lokale Adresse** auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf Ihrem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.</span><span class="sxs-lookup"><span data-stu-id="e655e-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="e655e-124">Beispiel: Wenn Ihre Website auf Enter ausgeführt wird `localhost:7331` `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="e655e-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="e655e-125">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e655e-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="e655e-126">Die Port Weiterleitung ist nun eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e655e-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="e655e-127">Sehen Sie sich die Statusanzeige für den Port Forward auf der Registerkarte auf Ihrem Gerät im Dialogfeld " **Geräte überprüfen** " an.</span><span class="sxs-lookup"><span data-stu-id="e655e-127">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Hinzufügen einer Port Weiterleitungsregel" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="e655e-129">Port Weiterleitungsstatus</span><span class="sxs-lookup"><span data-stu-id="e655e-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="e655e-130">Wenn Sie den Inhalt anzeigen möchten, öffnen Sie Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem `localhost` Port, den Sie im Feld **Device Port** festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="e655e-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="e655e-131">Wenn Sie beispielsweise `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="e655e-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="e655e-132">Zuordnen zu benutzerdefinierten lokalen Domänen</span><span class="sxs-lookup"><span data-stu-id="e655e-132">Map to custom local domains</span></span>  

<span data-ttu-id="e655e-133">Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf dem Entwicklungscomputer anzeigen, auf dem eine benutzerdefinierte Domäne verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e655e-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="e655e-134">Nehmen wir beispielsweise an, dass Ihre Website eine JavaScript-Bibliothek eines Drittanbieters verwendet, die nur in der Domäne funktioniert `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="e655e-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="e655e-135">So erstellen Sie einen Eintrag in Ihrer `hosts` Datei auf Ihrem Entwicklungscomputer, um diese Domäne an `localhost` \ (beispielsweise `127.0.0.1 microsoft-edge.devtools` \) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e655e-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="e655e-136">Nachdem Sie die benutzerdefinierte Domänenzuordnung und Portweiterleitung eingerichtet haben, können Sie die Website auf Ihrem Android-Gerät unter der URL anzeigen `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="e655e-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="e655e-137">Einrichten der Portweiterleitung an Proxy Server</span><span class="sxs-lookup"><span data-stu-id="e655e-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="e655e-138">Wenn Sie eine benutzerdefinierte Domäne zuordnen möchten, müssen Sie einen Proxy Server auf Ihrem Entwicklungscomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="e655e-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="e655e-139">Beispiele für Proxy Server sind [Charles][CharlesWebDebuggingProxy], [squid][SquidOptimisingWebDelivery]und [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="e655e-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="e655e-140">So richten Sie die Portweiterleitung an einen Proxy ein:</span><span class="sxs-lookup"><span data-stu-id="e655e-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="e655e-141">Führen Sie den Proxy Server aus, und notieren Sie den verwendeten Port.</span><span class="sxs-lookup"><span data-stu-id="e655e-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e655e-142">Der Proxy Server und Ihr Webserver müssen auf unterschiedlichen Ports ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e655e-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="e655e-143">Richten Sie die [Portweiterleitung](#set-up-port-forwarding) auf Ihr Android-Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="e655e-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="e655e-144">Geben Sie für das Feld **lokale Adresse** `localhost:` den Port ein, auf dem Ihr Proxy Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e655e-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="e655e-145">Wenn Sie beispielsweise auf Port ausgeführt wird `8000` , navigieren Sie zu `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="e655e-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="e655e-146">Geben Sie im Feld **Device Port** die Nummer ein, die Ihr Android-Gerät hören soll, beispielsweise `3333` .</span><span class="sxs-lookup"><span data-stu-id="e655e-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="e655e-147">Konfigurieren von Proxyeinstellungen auf Ihrem Gerät</span><span class="sxs-lookup"><span data-stu-id="e655e-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="e655e-148">Als nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxy Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e655e-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="e655e-149">Wechseln Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="e655e-149">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="e655e-150">Lange – drücken Sie den Namen des Netzwerks, mit dem Sie gerade verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="e655e-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e655e-151">Proxy Einstellungen gelten pro Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e655e-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="e655e-152">Wählen Sie **Netzwerk ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="e655e-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="e655e-153">Wählen Sie **Erweiterte Optionen**aus.</span><span class="sxs-lookup"><span data-stu-id="e655e-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="e655e-154">Die Proxyeinstellungen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e655e-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="e655e-155">Wählen Sie das **Proxy** -Menü und dann **manuell**aus.</span><span class="sxs-lookup"><span data-stu-id="e655e-155">Select the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="e655e-156">Geben Sie für das Feld **Proxy Hostname** ein `localhost` .</span><span class="sxs-lookup"><span data-stu-id="e655e-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="e655e-157">Geben Sie im Feld **Proxy Port** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteanschluss** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="e655e-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="e655e-158">Wählen Sie **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="e655e-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="e655e-159">Mit diesen Einstellungen leitet Ihr Gerät alle seine Anforderungen an den Proxy auf dem Entwicklungscomputer weiter.</span><span class="sxs-lookup"><span data-stu-id="e655e-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="e655e-160">Der Proxy stellt Anforderungen für Ihr Gerät, damit Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e655e-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="e655e-161">Auf Ihrem Android-Gerät können Sie nun auf benutzerdefinierte Domänen zugreifen, genau wie auf dem Entwicklungscomputer.</span><span class="sxs-lookup"><span data-stu-id="e655e-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="e655e-162">Wenn Ihr Webserver von einem nicht standardmäßigen Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.</span><span class="sxs-lookup"><span data-stu-id="e655e-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="e655e-163">Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne `microsoft-edge.devtools` am Port verwendet `7331` , sollten Sie die URL verwenden, wenn Sie die Website von Ihrem Android-Gerät aus anzeigen `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="e655e-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="e655e-164">Wenn Sie das normale Browsen fortsetzen möchten, denken Sie daran, die Proxyeinstellungen auf Ihrem Android-Gerät zurückzusetzen, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.</span><span class="sxs-lookup"><span data-stu-id="e655e-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <span data-ttu-id="e655e-165">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e655e-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging-Proxy"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: Optimieren der Web-Zustellung"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-Free Web Debugging Proxy"  

> [!NOTE]
> <span data-ttu-id="e655e-170">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e655e-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e655e-171">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e655e-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e655e-173">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e655e-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
