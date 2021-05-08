---
description: Emulieren von Authenticators und Debuggen von WebAuthn in Microsoft Edge DevTools.
title: Emulieren von Authatoren und Debuggen von WebAuthn in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3200f22485bfd642a37a7d34ac727b8da4500d06
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231181"
---
# <span data-ttu-id="bf43c-104">Emulieren von Authatoren und Debuggen von WebAuthn in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bf43c-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="bf43c-105">Anstatt die Webauthentifizierung in Ihrer Website oder App mit physischen Authentatoren zu debuggen, verwenden Sie das **WebAuthn-Tool** in Microsoft Edge DevTools zum Erstellen und Interagieren mit softwarebasierten virtuellen Authentatoren.</span><span class="sxs-lookup"><span data-stu-id="bf43c-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="bf43c-106">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf43c-106">Before you begin</span></span>  

<span data-ttu-id="bf43c-107">Ein hervorragender Ort, um mit der Webauthentifizierung zu beginnen, ist die [Webauthentifizierungs-API-Spezifikation.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="bf43c-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="bf43c-108">Einrichten des WebAuthn-Tools</span><span class="sxs-lookup"><span data-stu-id="bf43c-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="bf43c-109">Navigieren Sie zu einer Webseite, die WebAuthn verwendet, z. B. die folgende Demowebsite.</span><span class="sxs-lookup"><span data-stu-id="bf43c-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="bf43c-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="bf43c-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="bf43c-111">Melden Sie sich bei der Website an.</span><span class="sxs-lookup"><span data-stu-id="bf43c-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="bf43c-112">[Öffnen Sie DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="bf43c-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="bf43c-113">Wählen Sie zum Öffnen des **WebAuthn-Tools** das Symbol **DevTools** anpassen \( \) > `...` \*\*\*\*  >  **WebAuthn**weitere Tools aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="WebAuthn-Tool" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="bf43c-115">**WebAuthn-Tool**</span><span class="sxs-lookup"><span data-stu-id="bf43c-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bf43c-116">Aktivieren Sie **im WebAuthn-Tool** das Kontrollkästchen Virtuelle **Authatorumgebung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf43c-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="bf43c-117">Nachdem sie aktiviert wurde, wird ein neuer Abschnitt mit dem Namen **Neuer Authentator** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf43c-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Aktivieren der virtuellen Authentatorumgebung" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="bf43c-119">Aktivieren der virtuellen Authentatorumgebung</span><span class="sxs-lookup"><span data-stu-id="bf43c-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="bf43c-120">Konfigurieren Sie **im Abschnitt Neuer** Authentator die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="bf43c-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="bf43c-121">Option</span><span class="sxs-lookup"><span data-stu-id="bf43c-121">Option</span></span> | <span data-ttu-id="bf43c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bf43c-122">Value</span></span> | <span data-ttu-id="bf43c-123">Details</span><span class="sxs-lookup"><span data-stu-id="bf43c-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="bf43c-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] oder [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="bf43c-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="bf43c-125">Das Protokoll, das der virtuelle Authentisierungsgerät für die Codierung und Decodierung verwendet</span><span class="sxs-lookup"><span data-stu-id="bf43c-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="bf43c-126">, `nfc` `ble` , oder</span><span class="sxs-lookup"><span data-stu-id="bf43c-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="bf43c-127">Der virtuelle Authentator simuliert den ausgewählten Transport für die Kommunikation mit Clients, um eine Assertion für eine bestimmte Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf43c-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="bf43c-128">Weitere Informationen finden Sie unter [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="bf43c-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="bf43c-129">Aktivieren Sie \(oder off\) mithilfe des Kontrollkästchens.</span><span class="sxs-lookup"><span data-stu-id="bf43c-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="bf43c-130">Aktivieren Sie, wenn Ihre Web-App auf residenten Schlüsseln \(auch als clientseitiges Erkennen von Anmeldeinformationen\) bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="bf43c-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="bf43c-131">Weitere Informationen finden Sie unter [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="bf43c-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="bf43c-132">Aktivieren Sie \(oder off\) mithilfe des Kontrollkästchens.</span><span class="sxs-lookup"><span data-stu-id="bf43c-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="bf43c-133">Aktivieren Sie, wenn Ihre Web-App mithilfe von Gestenmodalitäten wie Toucheingabe und Pincode, Kennworteingabe oder biometrischer Erkennung auf lokale Autorisierung angewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bf43c-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="bf43c-134">Weitere Informationen finden Sie unter [Benutzerüberprüfung.][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="bf43c-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="bf43c-135">Klicken Sie auf die Schaltfläche **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bf43c-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="bf43c-136">Ein neuer Abschnitt des neu erstellten Authentator wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf43c-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="bf43c-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="bf43c-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="bf43c-139">Der **Authenticator** enthält eine **Credentials-Tabelle.**</span><span class="sxs-lookup"><span data-stu-id="bf43c-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="bf43c-140">Die Tabelle ist leer, bis eine Anmeldeinformationen für den Authentator registriert sind.</span><span class="sxs-lookup"><span data-stu-id="bf43c-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Keine Anmeldeinformationen" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="bf43c-142">Keine Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bf43c-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="bf43c-143">Registrieren neuer Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bf43c-143">Register a new credential</span></span>  

<span data-ttu-id="bf43c-144">Führen Sie die folgenden Schritte aus, um neue Anmeldeinformationen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="bf43c-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="bf43c-145">Weitere Informationen zur [Webauthentifizierungs-API][GithubW3cWebauthn] beim Registrieren neuer Anmeldeinformationen finden Sie unter [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="bf43c-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="bf43c-146">Wählen Sie auf der Demowebsite die Option **Neue Anmeldeinformationen registrieren aus.**</span><span class="sxs-lookup"><span data-stu-id="bf43c-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="bf43c-147">Der Tabelle "Anmeldeinformationen" \*\*\*\* im WebAuthn-Tool werden nun neue Anmeldeinformationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf43c-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Anzeigen von Anmeldeinformationen" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="bf43c-149">Anzeigen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bf43c-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="bf43c-150">Wählen Sie auf der Demowebsite die Schaltfläche **Authentifizieren** aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="bf43c-151">Stellen Sie [sicher,][GithubW3cWebauthnSctnSignCounter] dass die Anzahl der Anmeldeinformationen in der **Tabelle** Anmeldeinformationen um 1 erhöht wurde, was einen erfolgreichen [AuthenticatorGetAssertion-Vorgang][GithubW3cWebauthnAuthenticatorgetassertion] kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf43c-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="bf43c-152">Exportieren und Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bf43c-152">Export and remove credentials</span></span>  

<span data-ttu-id="bf43c-153">Zum Exportieren oder Entfernen von Anmeldeinformationen wählen Sie die Schaltfläche **Exportieren** **oder** Entfernen aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportieren oder Entfernen von Anmeldeinformationen" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="bf43c-155">Exportieren oder Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bf43c-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="bf43c-156">Umbenennen eines Authentators</span><span class="sxs-lookup"><span data-stu-id="bf43c-156">Rename an authenticator</span></span>  

<span data-ttu-id="bf43c-157">Führen Sie die folgenden Schritte aus, um einen Authentator umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="bf43c-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="bf43c-158">Wählen Sie neben dem Namen des Authentator die Schaltfläche **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="bf43c-159">Bearbeiten Sie den Namen, und klicken Sie dann auf **Eingabe,** um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bf43c-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Umbenennen eines Authentators" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="bf43c-161">Umbenennen eines Authentators</span><span class="sxs-lookup"><span data-stu-id="bf43c-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="bf43c-162">Festlegen des aktiven Authentators</span><span class="sxs-lookup"><span data-stu-id="bf43c-162">Set the active authenticator</span></span>  

<span data-ttu-id="bf43c-163">Ein neu erstellter Authentator wird automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf43c-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="bf43c-164">Um einen anderen virtuellen Authentator zu verwenden, wählen Sie das **Optionsfeld Aktiv** neben dem Authentator aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="bf43c-165">DevTools unterstützt zu einem beliebigen Zeitpunkt nur einen aktiven virtuellen Authentator.</span><span class="sxs-lookup"><span data-stu-id="bf43c-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="bf43c-166">Wenn Sie den aktiven Authentator entfernen, wird nicht automatisch ein anderer Authentator aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf43c-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Festlegen des aktiven Authentator" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="bf43c-168">Festlegen des aktiven Authentator</span><span class="sxs-lookup"><span data-stu-id="bf43c-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="bf43c-169">Entfernen eines virtuellen Authentators</span><span class="sxs-lookup"><span data-stu-id="bf43c-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="bf43c-170">Um einen virtuellen Authentator zu entfernen, wählen Sie neben dem Authentator die Schaltfläche **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="bf43c-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Entfernen des Authentator" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="bf43c-172">Entfernen des Authentator</span><span class="sxs-lookup"><span data-stu-id="bf43c-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="bf43c-173">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="bf43c-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Webauthn demo | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client to Authenticator Protocol (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Übersicht über den universellen 2nd-Faktor (U2F) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Der AuthenticatorGetAssertion-Vorgang – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Transport enumeration (enum AuthenticatorTransport) - Web Authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Resident Key Requirement Enumeration (enum ResidentKeyRequirement) - Web authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Benutzerüberprüfung – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential's [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Überlegungen zum Signaturindikator – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="bf43c-185">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf43c-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bf43c-186">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf43c-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="bf43c-188">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf43c-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
