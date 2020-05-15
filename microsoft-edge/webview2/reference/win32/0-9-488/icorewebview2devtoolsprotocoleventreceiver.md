---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c83123876747cb085efd65ff013db87a501b189c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653978"
---
# <span data-ttu-id="788aa-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="788aa-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="788aa-105">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="788aa-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="788aa-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="788aa-106">Summary</span></span>

 <span data-ttu-id="788aa-107">Member</span><span class="sxs-lookup"><span data-stu-id="788aa-107">Members</span></span>                        | <span data-ttu-id="788aa-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="788aa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="788aa-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="788aa-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="788aa-110">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="788aa-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="788aa-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="788aa-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="788aa-112">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="788aa-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="788aa-113">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="788aa-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="788aa-114">Member</span><span class="sxs-lookup"><span data-stu-id="788aa-114">Members</span></span>

#### <span data-ttu-id="788aa-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="788aa-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="788aa-116">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="788aa-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="788aa-117">öffentliche HRESULT- [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="788aa-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="788aa-118">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="788aa-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="788aa-119">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="788aa-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="788aa-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="788aa-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="788aa-121">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="788aa-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="788aa-122">Public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="788aa-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

