---
description: Prozess des Portierens der Chrome-Erweiterung zu Microsoft Edge.
title: Portierung der Chrome-Erweiterung zu Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 64a92927b9fe7658562f87f326bb9ac148991031
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327694"
---
# <span data-ttu-id="a4a3c-104">Portierung der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a4a3c-104">Port your extension</span></span>  

<span data-ttu-id="a4a3c-105">Mit Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen portierung.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="a4a3c-106">Die von Chrome unterstützten Erweiterungs-APIs und Manifestschlüssel sind codekompatibel mit Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="a4a3c-107">Eine Liste der von Microsoft Edge unterstützten APIs finden Sie unter [API-Unterstützung.][ExtensionApiSupport]</span><span class="sxs-lookup"><span data-stu-id="a4a3c-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="a4a3c-108">Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu porten.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="a4a3c-109">Überprüfen Sie die in Ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste der von Microsoft Edge-Erweiterungen [unterstützten APIs.][ExtensionApiSupport]</span><span class="sxs-lookup"><span data-stu-id="a4a3c-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a4a3c-110">Wenn Ihre Erweiterung APIs verwendet, die von Microsoft Edge nicht unterstützt werden, wird sie möglicherweise nicht direkt portierung.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="a4a3c-111">Legen Sie in der Manifestdatei das Feld `update_URL` auf `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="a4a3c-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="a4a3c-112">Der Wert verweist auf die Datei Ihrer Erweiterung im `.crx` Microsoft Edge-Add-Ons-Store und ermöglicht Es Microsoft Edge, nach Erweiterungsupdates zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="a4a3c-113">Wenn die Erweiterung entweder im Namen oder in der Beschreibung ihrer Erweiterung verwendet wird, müssen Sie die Erweiterung `Chrome` mit einer neuen Bezeichnung `Microsoft Edge` benennen.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="a4a3c-114">Zum Bestehen des Zertifizierungsprozesses sind die Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="a4a3c-115">Testen Sie Ihre Erweiterung, um zu überprüfen, ob sie in Microsoft Edge funktioniert, indem [Sie Ihre Erweiterung querladen.][ExtensionsGettingStartedExtensionSideloading]</span><span class="sxs-lookup"><span data-stu-id="a4a3c-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="a4a3c-116">Wenn Probleme auftreten, können Sie Ihre Erweiterungen in Microsoft Edge mithilfe der DevTools debuggen oder [uns kontaktieren.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="a4a3c-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="a4a3c-117">Befolgen Sie [die Veröffentlichungsrichtlinien,][ExtensionsPublishPublishExtension] um Ihre Erweiterung im Microsoft Edge-Add-Ons-Store zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a4a3c-118">Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen App austauscht, stellen Sie sicher, dass Sie dies in Der manifestdatei des systemeigenen `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` Messaginghosts festlegen.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="a4a3c-119">Mit dieser Einstellung kann die App Ihre Erweiterung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="a4a3c-120">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a4a3c-120">Next steps</span></span>  

<span data-ttu-id="a4a3c-121">Nachdem Ihr Erweiterungspaket bereit für die Veröffentlichung im Microsoft Edge-Add-Ons-Store [ist,][ExtensionsPublishCreateDevAccount] erstellen Sie ein Entwicklerkonto, und veröffentlichen Sie [Ihre Erweiterung.][ExtensionsPublishPublishExtension]</span><span class="sxs-lookup"><span data-stu-id="a4a3c-121">After your extension package is ready to publish in the Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Support-| Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen der Erweiterungs-| Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwicklerregistrierungs-| Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Der Erweiterungs-| Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalzahlung | Chrome Developer"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
