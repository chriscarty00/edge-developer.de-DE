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
# Schnittstellen IWebView2Environment3 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

Zusätzliche vom Environment-Objekt implementierte Funktionalität.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[add_NewVersionAvailable](#add_newversionavailable) | Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.
[remove_NewVersionAvailable](#remove_newversionavailable) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.

Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche. Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.

## Member

#### add_NewVersionAvailable 

Das NewVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.

> Public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Um die neuere Version des Browsers zu verwenden, müssen Sie eine neue [IWebView2Environment](IWebView2Environment.md) und [IWebView2WebView](IWebView2WebView.md)erstellen. Das Ereignis wird nur für die neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird. Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.

Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie den gleichen benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die [IWebView2Environment](IWebView2Environment.md) und IWebView2WebViews schließen, die zuerst die ältere Version des Browsers verwenden. Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.

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

#### remove_NewVersionAvailable 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NewVersionAvailable hinzugefügt wurde.

> Public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken-Token)

