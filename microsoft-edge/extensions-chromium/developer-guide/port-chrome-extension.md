---
description: Portierung der Chrome-Erweiterung zu Microsoft Edge
title: Port chrome extension To Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343136"
---
# <span data-ttu-id="deb48-104">Portierung Der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="deb48-104">Port your extension</span></span>  

<span data-ttu-id="deb48-105">Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen porten.</span><span class="sxs-lookup"><span data-stu-id="deb48-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="deb48-106">Die von Chrome unterstützten Erweiterungs-APIs und Manifestschlüssel sind codekompatibel mit Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="deb48-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="deb48-107">Eine Liste der apIs, die von Microsoft Edge unterstützt werden, finden Sie unter [API-Unterstützung][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="deb48-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="deb48-108">Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portierung.</span><span class="sxs-lookup"><span data-stu-id="deb48-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="deb48-109">Überprüfen Sie die in Ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste Microsoft Edge [unterstützten APIs][ExtensionApiSupport] für Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="deb48-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="deb48-110">Wenn Ihre Erweiterung APIs verwendet, die nicht von der Microsoft Edge werden, wird sie möglicherweise nicht direkt Portierung.</span><span class="sxs-lookup"><span data-stu-id="deb48-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="deb48-111">Legen Sie in der Manifestdatei das `update_URL` Feld auf . `https://edge.microsoft.com/extensionwebstorebase/v1/crx`</span><span class="sxs-lookup"><span data-stu-id="deb48-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="deb48-112">Der Wert verweist auf die Datei Ihrer Erweiterung im Microsoft Edge Add-Ons-Speicher und ermöglicht Microsoft Edge, nach `.crx` Erweiterungsupdates zu suchen.</span><span class="sxs-lookup"><span data-stu-id="deb48-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="deb48-113">Wenn sie entweder im Namen oder in der Beschreibung Ihrer Erweiterung verwendet `Chrome` wird, benennen Sie Ihre Erweiterung mit `Microsoft Edge` neu.</span><span class="sxs-lookup"><span data-stu-id="deb48-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="deb48-114">Zum Bestehen des Zertifizierungsprozesses sind die Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="deb48-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="deb48-115">Testen Sie Ihre Erweiterung, um zu überprüfen, ob sie in Microsoft Edge durch [Querladen der Erweiterung funktioniert.][ExtensionsGettingStartedExtensionSideloading]</span><span class="sxs-lookup"><span data-stu-id="deb48-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="deb48-116">Wenn Probleme auftreten, können Sie Ihre Erweiterungen in Microsoft Edge DevTools debuggen oder [uns kontaktieren.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="deb48-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="deb48-117">Befolgen Sie [die Veröffentlichungsrichtlinien,][ExtensionsPublishPublishExtension] um Ihre Erweiterung im Microsoft Edge zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="deb48-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="deb48-118">Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen App mit austauscht, stellen Sie sicher, dass Sie in Ihrer nativen `chrome.runtime.connectNative` `allowed_origins` Messaginghostmanifestdatei `extension://[Microsoft-Catalog-extensionID]` festlegen.</span><span class="sxs-lookup"><span data-stu-id="deb48-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="deb48-119">Die Einstellung ermöglicht es der App, Ihre Erweiterung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="deb48-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="deb48-120">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="deb48-120">Next steps</span></span>  

<span data-ttu-id="deb48-121">Nachdem Das Erweiterungspaket im Microsoft Edge veröffentlicht werden [kann,][ExtensionsPublishCreateDevAccount] erstellen Sie ein Entwicklerkonto, und veröffentlichen Sie [Ihre Erweiterung.][ExtensionsPublishPublishExtension]</span><span class="sxs-lookup"><span data-stu-id="deb48-121">After your extension package is ready to publish in the Microsoft Edge Add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Support | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen Der Erweiterungs-| Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwicklerregistrierungs-| Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Der Erweiterungs-| Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "One-Time Payments | Chrome Developer"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
