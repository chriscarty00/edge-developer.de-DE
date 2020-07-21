---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: 3e18c15e23338404720dae917cb6d009c41c3c04
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886553"
---
# <span data-ttu-id="a2a3f-104">Schnittstellen ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="a2a3f-104">interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="a2a3f-105">Experimentelle Optionen, die zum Erstellen der WebView2-Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="a2a3f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a2a3f-106">Summary</span></span>

 <span data-ttu-id="a2a3f-107">Member</span><span class="sxs-lookup"><span data-stu-id="a2a3f-107">Members</span></span>                        | <span data-ttu-id="a2a3f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a2a3f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2a3f-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="a2a3f-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="a2a3f-110">Die IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="a2a3f-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="a2a3f-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="a2a3f-112">Festlegen der IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2a3f-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="a2a3f-113">Eine Standardimplementierung wird in WebView2ExperimentalEnvironmentOptions. h bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="a2a3f-114">Member</span><span class="sxs-lookup"><span data-stu-id="a2a3f-114">Members</span></span>

#### <span data-ttu-id="a2a3f-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="a2a3f-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="a2a3f-116">Die IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="a2a3f-117">öffentliche HRESULT- [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="a2a3f-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="a2a3f-118">Standard ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-118">Default is disabled.</span></span> <span data-ttu-id="a2a3f-119">Universelle Windows-Plattform-apps müssen auch die [Eingeschränkte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO-Funktion für das einmalige Anmelden deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a2a3f-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="a2a3f-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="a2a3f-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="a2a3f-121">Festlegen der IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2a3f-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="a2a3f-122">öffentliche HRESULT- [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="a2a3f-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>

