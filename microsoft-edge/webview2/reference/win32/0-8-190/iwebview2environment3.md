---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878526"
---
# <span data-ttu-id="0556a-104">0.8.355-Interface-IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="0556a-104">0.8.355 - interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="0556a-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="0556a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0556a-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0556a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="0556a-107">Zusätzliche vom Environment-Objekt implementierte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="0556a-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="0556a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0556a-108">Summary</span></span>

 <span data-ttu-id="0556a-109">Member</span><span class="sxs-lookup"><span data-stu-id="0556a-109">Members</span></span>                        | <span data-ttu-id="0556a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0556a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0556a-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0556a-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="0556a-112">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="0556a-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="0556a-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0556a-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="0556a-114">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0556a-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="0556a-115">Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="0556a-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="0556a-116">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="0556a-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="0556a-117">Member</span><span class="sxs-lookup"><span data-stu-id="0556a-117">Members</span></span>

#### <span data-ttu-id="0556a-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0556a-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="0556a-119">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="0556a-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="0556a-120">Public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="0556a-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0556a-121">Um die neuere Version des Browsers zu verwenden, müssen Sie eine neue [IWebView2Environment](IWebView2Environment.md) und [IWebView2WebView](IWebView2WebView.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="0556a-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="0556a-122">Das Ereignis wird nur für die neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0556a-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="0556a-123">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0556a-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="0556a-124">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie den gleichen benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die [IWebView2Environment](IWebView2Environment.md) und IWebView2WebViews schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="0556a-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="0556a-125">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="0556a-125">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="0556a-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0556a-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="0556a-127">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0556a-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="0556a-128">Public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="0556a-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

