---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886094"
---
# <span data-ttu-id="42aad-104">0.8.355-Interface-IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="42aad-104">0.8.355 - interface IWebView2Environment3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="42aad-105">Zusätzliche vom Environment-Objekt implementierte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="42aad-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="42aad-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="42aad-106">Summary</span></span>

 <span data-ttu-id="42aad-107">Member</span><span class="sxs-lookup"><span data-stu-id="42aad-107">Members</span></span>                        | <span data-ttu-id="42aad-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="42aad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42aad-109">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="42aad-109">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="42aad-110">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="42aad-110">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="42aad-111">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="42aad-111">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="42aad-112">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="42aad-112">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="42aad-113">Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="42aad-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="42aad-114">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="42aad-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="42aad-115">Member</span><span class="sxs-lookup"><span data-stu-id="42aad-115">Members</span></span>

#### <span data-ttu-id="42aad-116">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="42aad-116">add_NewVersionAvailable</span></span> 

<span data-ttu-id="42aad-117">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="42aad-117">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="42aad-118">Public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="42aad-118">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="42aad-119">Um die neuere Version des Browsers zu verwenden, müssen Sie eine neue [IWebView2Environment](IWebView2Environment.md) und [IWebView2WebView](IWebView2WebView.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="42aad-119">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="42aad-120">Das Ereignis wird nur für die neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42aad-120">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="42aad-121">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="42aad-121">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="42aad-122">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie den gleichen benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die [IWebView2Environment](IWebView2Environment.md) und IWebView2WebViews schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="42aad-122">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="42aad-123">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="42aad-123">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="42aad-124">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="42aad-124">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="42aad-125">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="42aad-125">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="42aad-126">Public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="42aad-126">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

