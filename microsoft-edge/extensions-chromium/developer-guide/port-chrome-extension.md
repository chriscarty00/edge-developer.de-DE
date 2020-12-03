---
description: Prozess zum Portieren der Chrome-Erweiterung an Microsoft Edge.
title: Port Chrome-Erweiterung zu Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195159"
---
# <span data-ttu-id="5817a-104">Portieren der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5817a-104">Port your extension</span></span>  

<span data-ttu-id="5817a-105">Mit Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen portieren.</span><span class="sxs-lookup"><span data-stu-id="5817a-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="5817a-106">Die von Chrome unterstützten Erweiterungs-APIs und manifestschlüssel sind mit Microsoft Edge Code kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5817a-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="5817a-107">Wenn Sie eine Liste der von Microsoft Edge unterstützten APIs finden möchten, navigieren Sie zu [API-Support][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="5817a-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="5817a-108">Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portieren.</span><span class="sxs-lookup"><span data-stu-id="5817a-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="5817a-109">Überprüfen Sie die in ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste der [unterstützten APIs][ExtensionApiSupport] für Microsoft-Edge-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="5817a-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5817a-110">Wenn Ihre Erweiterung APIs verwendet, die von Microsoft Edge nicht unterstützt werden, kann Sie nicht direkt portiert werden.</span><span class="sxs-lookup"><span data-stu-id="5817a-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="5817a-111">Wenn der Name `Chrome` entweder im Namen oder in der Beschreibung der Erweiterung verwendet wird, geben Sie die Erweiterung für neu ein `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="5817a-111">If the name `Chrome` is being used in either the name or the description of the extension, rebrand the extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="5817a-112">Dieser Schritt ist erforderlich, um den Zertifizierungsprozess durchlaufen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="5817a-112">This step is required to pass the certification process.</span></span>  
1.  <span data-ttu-id="5817a-113">Testen Sie Ihre Erweiterung, um zu überprüfen, ob Sie in Microsoft Edge funktioniert, indem Sie [Ihre Erweiterung Sideloading][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="5817a-113">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="5817a-114">Wenn Sie Probleme haben, können Sie Ihre Erweiterungen in Microsoft Edge mithilfe des devtools Debuggen oder [sich mit uns in Verbindung setzen][mailtoExtensionMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="5817a-114">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="5817a-115">Befolgen Sie die [Veröffentlichungsrichtlinien][ExtensionsPublishPublishExtension] , um Ihre Erweiterung im Microsoft Edge-Add-on-Store zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5817a-115">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5817a-116">Wenn die Erweiterung Nachrichten mit einer systemeigenen App mit API austauscht `chrome.runtime.connectNative` , stellen Sie sicher, dass Sie `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5817a-116">If the extension exchanges messages with a native app using `chrome.runtime.connectNative` API, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="5817a-117">Dadurch kann die APP die Erweiterung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5817a-117">This enables the app to identify the extension.</span></span>  
    
## <span data-ttu-id="5817a-118">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="5817a-118">Next steps</span></span>  

<span data-ttu-id="5817a-119">Sobald das Erweiterungspaket im Microsoft Edge-Add-ons-Store veröffentlicht werden kann, [Erstellen Sie ein Entwicklerkonto][ExtensionsPublishCreateDevAccount] , und [veröffentlichen Sie Ihre Erweiterung][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="5817a-119">Once your extension package is ready to be published to Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Unterstützung | Microsoft docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen-Erweiterung | Microsoft docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwickler Registrierung | Microsoft docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Ihrer Erweiterung | Microsoft docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalige Zahlungen | Chrome-Entwickler"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
