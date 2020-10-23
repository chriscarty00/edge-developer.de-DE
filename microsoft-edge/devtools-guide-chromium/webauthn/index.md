---
description: Emulieren Sie Authentifikatoren, und Debuggen Sie webauthn in Microsoft Edge devtools.
title: Emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134093"
---
# <span data-ttu-id="42652-104">Emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="42652-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="42652-105">Anstatt die Webauthentifizierung in Ihrer Website oder App mit physikalischen Authentifikatoren zu debuggen, verwenden Sie das **webauthn** -Tool in Microsoft Edge devtools, um softwarebasierte virtuelle Authentifikatoren zu erstellen und mit Ihnen zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="42652-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="42652-106">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="42652-106">Before you begin</span></span>  

<span data-ttu-id="42652-107">Die [Webauthentifizierungs-API-Spezifikation][GithubW3cWebauthn]eignet sich hervorragend für die ersten Schritte mit der Webauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="42652-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="42652-108">Einrichten des webauthn-Tools</span><span class="sxs-lookup"><span data-stu-id="42652-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="42652-109">Navigieren Sie zu einer Webseite, die webauthen verwendet, beispielsweise die folgende Demo-Website.</span><span class="sxs-lookup"><span data-stu-id="42652-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="42652-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="42652-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="42652-111">Registrieren Sie sich bei der Website.</span><span class="sxs-lookup"><span data-stu-id="42652-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="42652-112">[Öffnen Sie devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="42652-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="42652-113">Um das **webauthn** -Tool zu öffnen, wählen Sie das Symbol **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **webauthn**aus.</span><span class="sxs-lookup"><span data-stu-id="42652-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="42652-115">**Webauthn** -Tool</span><span class="sxs-lookup"><span data-stu-id="42652-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="42652-116">Aktivieren Sie im **webauthn** -Tool das Kontrollkästchen neben **Virtual Authenticator-Umgebung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="42652-116">In the **WebAuthn** tool, choose the checkbox next to **Enable virtual authenticator environment**.</span></span>  
1.  <span data-ttu-id="42652-117">Nach der Aktivierung wird ein neuer Abschnitt mit dem Namen **neuer Authentifikator** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42652-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="42652-119">Aktivieren der virtuellen Authentifikator-Umgebung</span><span class="sxs-lookup"><span data-stu-id="42652-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="42652-120">Konfigurieren Sie im Abschnitt **neuer Authentifikator** die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="42652-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="42652-121">Option</span><span class="sxs-lookup"><span data-stu-id="42652-121">Option</span></span> | <span data-ttu-id="42652-122">Wert</span><span class="sxs-lookup"><span data-stu-id="42652-122">Value</span></span> | <span data-ttu-id="42652-123">Details</span><span class="sxs-lookup"><span data-stu-id="42652-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="42652-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] oder [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="42652-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="42652-125">Das Protokoll, das der virtuelle Authentifikator für die Codierung und Decodierung verwendet</span><span class="sxs-lookup"><span data-stu-id="42652-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="42652-126">, `nfc` , `ble` oder</span><span class="sxs-lookup"><span data-stu-id="42652-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="42652-127">Der virtuelle Authentifikator simuliert den ausgewählten Transport für die Kommunikation mit Clients, um eine Assertion für bestimmte Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="42652-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="42652-128">Weitere Informationen finden Sie unter [Authentifikator-Transport-Enumeration][GithubW3cWebauthnEnumTransport] .</span><span class="sxs-lookup"><span data-stu-id="42652-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="42652-129">Aktivieren von \ (oder Off \) mithilfe des Kontrollkästchens</span><span class="sxs-lookup"><span data-stu-id="42652-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="42652-130">Aktivieren Sie diese Option, wenn Ihre Web-App auf Resident Keys (auch als "clientseitig erkennbare Anmeldeinformationen" bezeichnet) basiert.</span><span class="sxs-lookup"><span data-stu-id="42652-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="42652-131">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zur [Anforderungs Enumeration für residente Schlüssel][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="42652-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="42652-132">Aktivieren von \ (oder Off \) mithilfe des Kontrollkästchens</span><span class="sxs-lookup"><span data-stu-id="42652-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="42652-133">Aktivieren Sie diese Option, wenn Ihre Web-App die lokale Autorisierung mithilfe von Gesten Modalitäten wie Touch plus PIN-Code, Kennworteingabe oder biometrische Erkennung anvertraut.</span><span class="sxs-lookup"><span data-stu-id="42652-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="42652-134">Weitere Informationen finden Sie unter [Benutzerüberprüfung][GithubW3cWebauthnEnumUserverification] .</span><span class="sxs-lookup"><span data-stu-id="42652-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="42652-135">Klicken Sie auf die Schaltfläche **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="42652-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="42652-136">Ein neuer Abschnitt Ihres neu erstellten Authentifikators wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42652-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="42652-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="42652-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="42652-139">Der **Authentifikator** -Abschnitt enthält eine Tabelle mit **Anmeldeinformationen** .</span><span class="sxs-lookup"><span data-stu-id="42652-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="42652-140">Die Tabelle ist leer, bis die Anmeldeinformationen für den Authentifikator registriert sind.</span><span class="sxs-lookup"><span data-stu-id="42652-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="42652-142">Keine Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="42652-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="42652-143">Registrieren einer neuen Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="42652-143">Register a new credential</span></span>  

<span data-ttu-id="42652-144">Führen Sie die folgenden Schritte aus, um eine neue Anmeldeinformationen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="42652-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="42652-145">Weitere Informationen dazu, was die [Webauthentifizierungs-API][GithubW3cWebauthn] beim Registrieren einer neuen Anmeldeinformationen tut, finden Sie unter [Erstellen einer neuen Anmelde][GithubW3cWebauthnSctnCreatecredential]Informationen.</span><span class="sxs-lookup"><span data-stu-id="42652-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="42652-146">Wählen Sie auf der Demo-Website **neue Anmeldeinformationen registrieren**aus.</span><span class="sxs-lookup"><span data-stu-id="42652-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="42652-147">Im webauthn-Tool wird nun eine neue Anmeldeinformation zur Tabelle " **Anmeldeinformationen** " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42652-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="42652-149">Anzeigen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="42652-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="42652-150">Klicken Sie auf der Demo-Website auf die Schaltfläche **Authentifizieren** .</span><span class="sxs-lookup"><span data-stu-id="42652-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="42652-151">Überprüfen Sie, ob die [Anzahl][GithubW3cWebauthnSctnSignCounter] der Anmeldeinformationen in der Tabelle mit den **Anmeldeinformationen** um 1 erhöht wurde, wodurch ein erfolgreicher [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] -Vorgang markiert wird.</span><span class="sxs-lookup"><span data-stu-id="42652-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="42652-152">Exportieren und Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="42652-152">Export and remove credentials</span></span>  

<span data-ttu-id="42652-153">Wenn Sie eine Anmeldeinformationen exportieren oder entfernen möchten, wählen Sie die Schaltfläche **exportieren** oder **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="42652-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="42652-155">Exportieren oder Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="42652-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="42652-156">Umbenennen eines Authentifikators</span><span class="sxs-lookup"><span data-stu-id="42652-156">Rename an authenticator</span></span>  

<span data-ttu-id="42652-157">Führen Sie die folgenden Schritte aus, um einen Authentifikator umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="42652-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="42652-158">Wählen Sie neben dem Namen des Authentifikators die Schaltfläche **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="42652-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="42652-159">Bearbeiten Sie den Namen, und wählen **Sie dann Enter** aus, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="42652-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="42652-161">Umbenennen eines Authentifikators</span><span class="sxs-lookup"><span data-stu-id="42652-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="42652-162">Einrichten des aktiven Authentifikators</span><span class="sxs-lookup"><span data-stu-id="42652-162">Set the active authenticator</span></span>  

<span data-ttu-id="42652-163">Ein neu erstellter Authentifikator wird automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="42652-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="42652-164">Wenn Sie einen anderen virtuellen Authentifikator verwenden möchten, wählen Sie das **aktive** Optionsfeld neben dem Authentifikator aus.</span><span class="sxs-lookup"><span data-stu-id="42652-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="42652-165">DevTools unterstützt zu einem beliebigen Zeitpunkt nur einen aktiven virtuellen Authentifikator.</span><span class="sxs-lookup"><span data-stu-id="42652-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="42652-166">Wenn Sie den aktiven Authentifikator entfernen, wird ein anderer Authentifikator nicht automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="42652-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="42652-168">Aktiven Authentifikator einrichten</span><span class="sxs-lookup"><span data-stu-id="42652-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="42652-169">Entfernen eines virtuellen Authentifikators</span><span class="sxs-lookup"><span data-stu-id="42652-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="42652-170">Um einen virtuellen Authentifikator zu entfernen, klicken Sie neben dem Authentifikator auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="42652-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="42652-172">Authentifikator entfernen</span><span class="sxs-lookup"><span data-stu-id="42652-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="42652-173">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="42652-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Webauthn-Demo | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client-zu-Authentifikator-Protokoll (CTAP) | Fido-Allianz"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Übersicht über den universellen zweiten Faktor (U2F) | Fido-Allianz"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel-Ebene 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Der authenticatorGetAssertion-Vorgang – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authentifikator-Transport-Enumeration (Enum-AuthenticatorTransport) – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeration für residente Schlüsselanforderungen (Enum ResidentKeyRequirement) – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel Ebene 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Benutzerüberprüfung – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Erstellen Sie eine neue Anmeldeinformationen-PublicKeyCredential [[Create]] (Origin, Options, sameOriginWithAncestors)-Methode – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen des öffentlichen Schlüssels Ebene 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Überlegungen zum Signatur Indikator – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel (Ebene 2) | GitHub"  

> [!NOTE]
> <span data-ttu-id="42652-185">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42652-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="42652-186">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="42652-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="42652-188">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="42652-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
