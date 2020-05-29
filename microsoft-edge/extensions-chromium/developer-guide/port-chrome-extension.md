---
description: Prozess zum Portieren der Chrome-Erweiterung an Microsoft Edge.
title: Port Chrome-Erweiterung an Microsoft (Chrom) Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567513"
---
# <span data-ttu-id="ce9c6-104">Port Chrome-Erweiterung zu Microsoft \ (Chrom \) Edge</span><span class="sxs-lookup"><span data-stu-id="ce9c6-104">Port Chrome Extension To Microsoft \(Chromium\) Edge</span></span>  

<span data-ttu-id="ce9c6-105">Der Vorgang zum Portieren einer Chrome-Erweiterung zu Microsoft Edge ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-105">The process of porting a Chrome Extension to Microsoft Edge is very straightforward.</span></span>  <span data-ttu-id="ce9c6-106">Die für Chrom geschriebenen Erweiterungen werden in den meisten Fällen auf Microsoft Edge mit minimalen Änderungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-106">Extensions written for Chromium, in most cases, run on Microsoft Edge with minimal changes.</span></span>  <span data-ttu-id="ce9c6-107">Die von Chrome unterstützten Erweiterungs-APIs und manifestschlüssel sind mit Microsoft Edge Code kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-107">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="ce9c6-108">Microsoft Edge unterstützt jedoch nicht die folgenden Erweiterungs-APIs:</span><span class="sxs-lookup"><span data-stu-id="ce9c6-108">However, Microsoft Edge does not support the following Extension APIs:</span></span>  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> <span data-ttu-id="ce9c6-109">Der Benutzer muss bei Microsoft Edge mit einem MSA-oder Aad-Konto angemeldet sein, um die API verwenden zu können `chrome.identity.getProfileUserInfo` .</span><span class="sxs-lookup"><span data-stu-id="ce9c6-109">The user must be signed into Microsoft Edge using an MSA or AAD account in order to use the `chrome.identity.getProfileUserInfo` API.</span></span>  <span data-ttu-id="ce9c6-110">Wenn der Benutzer bei Microsoft Edge unter Verwendung einer **lokalen Anzeige**angemeldet ist, gibt die API die `null` e-Mail-und ID-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-110">If the user is signed into Microsoft Edge using **On-premise AD**, the API returns `null` for the email and ID values.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ce9c6-111">**Zahlungen**: Microsoft Edge unterstützt nicht direkt eine Erweiterung, die [Chrome Web Store-Zahlungen][ChromeDeveloperWebStorePayments] verwendet, da die Anforderung zum `identity.getAuthtoken` Abrufen des Tokens für Benutzer mit Anmeldedaten zum Senden der auf der Grundlage der Ruhe basierten Lizenzierungs-API-Anforderung verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-111">**Payments**:  Microsoft Edge does not directly support an Extension that uses [Chrome Web Store payments][ChromeDeveloperWebStorePayments] due to the requirement to use the `identity.getAuthtoken` request to get the token for signed-in users to send the REST-based licensing API request.</span></span>  <span data-ttu-id="ce9c6-112">Microsoft Edge unterstützt die `getAuthtoken` Anforderung nicht, sodass dieser Fluss nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-112">Microsoft Edge does not support the `getAuthtoken` request, so this flow does not work.</span></span>  

<span data-ttu-id="ce9c6-113">Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portieren:</span><span class="sxs-lookup"><span data-stu-id="ce9c6-113">To port your Chrome Extension, follow these steps:</span></span>  

1.  <span data-ttu-id="ce9c6-114">Überprüfen Sie die in ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-114">Review the Chrome Extension APIs used in your Extensions.</span></span>  <span data-ttu-id="ce9c6-115">Wenn Sie Features oder APIs verwenden, die von Microsoft Edge nicht unterstützt werden, können Sie Ihre Erweiterung möglicherweise nicht portieren.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-115">If you are using features or APIs that are not supported by Microsoft Edge, you may not be able to port your Extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ce9c6-116">Die `getAuthToken` API funktioniert nicht mit Microsoft Edge, jedoch können Sie `launchWebAuthFlow` zum Abrufen eines OAuth2-Tokens verwenden, um Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-116">The `getAuthToken` API does not work with Microsoft Edge, however you may use `launchWebAuthFlow` to fetch an OAuth2 token to authenticate users.</span></span>  
    
1.  <span data-ttu-id="ce9c6-117">Wenn Sie `Chrome` den Namen oder die Beschreibung ihrer Durchwahl verwenden, geben Sie die Erweiterung für neu ein `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="ce9c6-117">If you are using `Chrome` in the name or description of your Extension, re-brand the Extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="ce9c6-118">Sie müssen den Zertifizierungsprozess bestehen.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-118">You must pass the certification process.</span></span>  
    
1.  <span data-ttu-id="ce9c6-119">Testen Sie Ihre Erweiterung, um zu überprüfen, ob Sie in Microsoft Edge funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-119">Test your Extension to check if it works in Microsoft Edge.</span></span>  <span data-ttu-id="ce9c6-120">Der erste Schritt besteht darin, sicherzustellen, dass die Erweiterungsentwickler Features aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-120">The first step to do this is to ensure that you have Extension developer features turned on.</span></span>  <span data-ttu-id="ce9c6-121">Dadurch können Sie Erweiterungsdateien in Microsoft Edge laden, damit Sie Ihre Erweiterung während der Entwicklung testen können.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-121">This enables you to side load Extension files in Microsoft Edge so that you are able to test your Extension while developing it.</span></span>  
    
1.  <span data-ttu-id="ce9c6-122">Wenn Sie Probleme haben, Debuggen Sie Ihre Erweiterungen in Microsoft Edge mithilfe des devtools, oder [kontaktieren Sie uns][mailtoExtensionPartnerOpsMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="ce9c6-122">If you have any issues, debug your Extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionPartnerOpsMicrosoft].</span></span>  
    
1.  <span data-ttu-id="ce9c6-123">Nun wird Ihre Erweiterung endlich aufpoliert und kann verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-123">Now your Extension is finally polished up and ready to be packaged.</span></span>  <span data-ttu-id="ce9c6-124">Wenn Sie sich auf die Übermittlung an den Microsoft Edge Addons-Katalog vorbereiten möchten \ (Microsoft Edge Addons \), müssen Sie Ihre Erweiterung nicht verpacken.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-124">If you wish to prepare for submission to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\), you do not need to package your Extension.</span></span>  <span data-ttu-id="ce9c6-125">Befolgen Sie außerdem unsere [Veröffentlichungsrichtlinien][ExtensionsPublishExtension] , um Ihre Erweiterung auf Microsoft Edge-Addons zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-125">Further, follow our [publishing guidelines][ExtensionsPublishExtension] to publish your Extension on Microsoft Edge Addons.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ce9c6-126">Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen Anwendung unter Verwendung der API austauscht `chrome.runtime.connectNative` , stellen Sie sicher, dass Sie `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf "" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-126">If your Extension exchanges messages with a native application using `chrome.runtime.connectNative` API, ensure that you set `allowedorigins` to "`extension://[Microsoft-Catalog-extensionID]`" in your native messaging host manifest file.</span></span>  <span data-ttu-id="ce9c6-127">Dadurch kann die APP die Erweiterung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ce9c6-127">This enables the app to identify the Extension.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Veröffentlichen einer Erweiterung"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalige Zahlungen – Google Chrome"  
