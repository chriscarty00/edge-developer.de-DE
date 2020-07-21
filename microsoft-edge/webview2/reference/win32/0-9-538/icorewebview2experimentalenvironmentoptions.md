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
# Schnittstellen ICoreWebView2ExperimentalEnvironmentOptions 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

Experimentelle Optionen, die zum Erstellen der WebView2-Umgebung verwendet werden.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled) | Die IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.
[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled) | Festlegen der IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft

Eine Standardimplementierung wird in WebView2ExperimentalEnvironmentOptions. h bereitgestellt.

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

## Member

#### get_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Die IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.

> öffentliche HRESULT- [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(bool * enabled)

Standard ist deaktiviert. Universelle Windows-Plattform-apps müssen auch die [Eingeschränkte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO-Funktion für das einmalige Anmelden deklarieren.

#### put_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Festlegen der IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft

> öffentliche HRESULT- [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(bool enabled)

