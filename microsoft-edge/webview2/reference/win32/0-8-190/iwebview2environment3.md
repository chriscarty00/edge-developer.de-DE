---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 43becb7f4ec9903557ccd558319e233266ac2ea1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653788"
---
# <span data-ttu-id="e1984-104">Schnittstellen IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="e1984-104">interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="e1984-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e1984-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e1984-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e1984-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="e1984-107">Zusätzliche vom Environment-Objekt implementierte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="e1984-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="e1984-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e1984-108">Summary</span></span>

 <span data-ttu-id="e1984-109">Member</span><span class="sxs-lookup"><span data-stu-id="e1984-109">Members</span></span>                        | <span data-ttu-id="e1984-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e1984-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1984-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="e1984-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="e1984-112">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="e1984-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="e1984-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="e1984-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="e1984-114">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1984-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="e1984-115">Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="e1984-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="e1984-116">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1984-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="e1984-117">Member</span><span class="sxs-lookup"><span data-stu-id="e1984-117">Members</span></span>

#### <span data-ttu-id="e1984-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="e1984-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="e1984-119">Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="e1984-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="e1984-120">Public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="e1984-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1984-121">Um die neuere Version des Browsers zu verwenden, müssen Sie eine neue [IWebView2Environment](IWebView2Environment.md) und [IWebView2WebView](IWebView2WebView.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1984-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="e1984-122">Das Ereignis wird nur für die neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1984-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="e1984-123">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e1984-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="e1984-124">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie den gleichen benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die [IWebView2Environment](IWebView2Environment.md) und IWebView2WebViews schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1984-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="e1984-125">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e1984-125">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="e1984-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="e1984-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="e1984-127">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1984-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="e1984-128">Public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="e1984-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

