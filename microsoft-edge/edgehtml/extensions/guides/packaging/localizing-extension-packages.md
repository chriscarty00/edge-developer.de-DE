---
description: Erfahren Sie, wie Sie Ihr Microsoft Edge-Erweiterungspaket lokalisieren, damit es nach der Veröffentlichung für mehrere Locales bereit ist.
title: Lokalisierung von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, web development, html, css, javascript, developer
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397720"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a>Lokalisieren von Microsoft Edge-Erweiterungen für Windows und den Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

In diesem Handbuch wird beschrieben, wie Sie Ihre Microsoft Edge-Erweiterung lokalisieren, sodass sie nach der Veröffentlichung für mehrere Locales bereit ist.  Um Ihre Erweiterung vollständig zu lokalisieren, müssen Sie die Schritte für Windows und den Microsoft Store ausführen.  

Wenn Sie Ihre Erweiterungsressourcen für Microsoft Edge lokalisieren möchten, erfahren Sie, wie Sie das i18n-Framework im [Internationalisierungshandbuch verwenden.](../internationalization.md)  

> [!NOTE]
> Wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt, können Sie zu Lokalisieren von Name und Beschreibung [im Microsoft Store springen.](#localizing-name-and-description-in-the-microsoft-store)  

## <a name="the-localization-process-overview"></a>Übersicht über den Lokalisierungsprozess  

Der erste Schritt, um Ihre Erweiterung für eine breite Zielgruppe verfügbar zu machen, besteht in der Konfiguration der [AppxManifest](#configuring-the-appxmanifest) für mehrere Sprachen.  Im Microsoft Store zeigt dies Benutzern, welche Sprachen Ihre Erweiterung unterstützt.  Bestimmte Felder im AppxManifest müssen ebenfalls geändert werden, wenn der Name Ihrer Erweiterung in der [Windows-Benutzeroberfläche](#localizing-extension-resources-for-windows-and-the-microsoft-store)und im Microsoft Store lokalisiert werden soll.  

Sobald Ihr AppxManifest konfiguriert ist, [](#creating-json-string-resources) müssen Sie JSON-Zeichenfolgenressourcen für die Sprachen erstellen, die Sie als unterstützt angegeben haben.  Dies erfordert das Erstellen einer Datei für jede Sprache, in der jede Datei alle `.resjson` Benutzeroberflächenzeichenfolgen dieser Sprache enthält.  

Nachdem die Dateien für die unterstützten Sprachen erstellt wurden, muss eine `.resjson` [.pri-Ressourcendatei erstellt werden.](#creating-the-resources-file) Dies wird mithilfe einer Konfigurationsdatei für das MakePRI-Tool erstellt, das im [Windows 10 SDK enthalten ist.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)  

> [!NOTE]
> Wenn Sie nur das Windows 10 SDK herunterladen, um das Tool zu verwenden, können Sie nur die Features Windows SDK Signing Tools for Desktop Apps und Windows SDK for UWP Managed App auswählen, um den Download leichter zu `MakePri.exe` halten. **** ****  Das `MakePri.exe` Tool wird in Unterordnern von `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` angezeigt.  

Nachdem Sie Ihre Erweiterung hochgeladen haben, müssen Sie den Namen und die Beschreibung im [Microsoft Store lokalisieren.](#localizing-name-and-description-in-the-microsoft-store)  

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.  **Kontaktieren Sie uns mit** Ihren Anforderungen, Teil des Microsoft Store zu sein, und wir werden Sie für ein zukünftiges Update in Betracht ziehen.  

## <a name="configuring-the-appxmanifest"></a>Konfigurieren des AppXManifest  

Die Liste Unterstützte Sprachen Ihrer Erweiterung im Microsoft Store wird basierend auf den AppXManifest-Werten generiert.  Diese Liste wird mithilfe des Elements `Resource` angegeben.  

![App-Details](../../media/language-app-details.png)  

Um die Liste der Sprachen anzugeben, die von Ihrer Erweiterung unterstützt werden, können Sie ein Element im folgenden Format hinzufügen \(Dieses Element zeigt Unterstützung für Englisch, Deutsch und Französisch im `Resource` `Resource` Microsoft Store\):  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

Weitere [Informationen zu den](/windows/uwp/publish/supported-languages) vom Microsoft Store unterstützten Sprachen/Sprachcodes finden Sie unter Unterstützte Sprachen.  

Um lokalisierte Zeichenfolgen für alle öffentlich sichtbaren Elemente im AppxManifest anzugeben, müssen Sie einen Ressourcenbezeichner im Format `ms-resource:<resource id>` verwenden.  

Die folgenden Codeausschnitte machen ein vollständiges AppxManifest. Die folgenden Werte sollten aus lokalisierten Ressourcendateien abgerufen werden:  

*   Properties\DisplayName  
*   Eigenschaften\Beschreibung  
*   Properties\PublisherDisplayName  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   Applications\Application\VisualElements\DisplayName  
*   Applications\Application\VisualElements\Description  
*   Applications\Application\Extensions\Extension\AppExtension\DisplayName  

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```  

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a>Lokalisieren von Erweiterungsressourcen für Windows und den Microsoft Store  

Da Ihr AppxManifest nun für mehrere Sprachen konfiguriert ist, sollten Sie einige wichtige Unterschiede zwischen dem Lokalisieren der Benutzeroberfläche in Ihrer Erweiterung und der Lokalisierung Ihrer Erweiterung für Windows und dem Microsoft Store kennen.  

Microsoft Edge-Erweiterungen werden zwar nicht außerhalb von Microsoft Edge ausgeführt, die Verwaltung kann jedoch in Windows erfolgen.  Beispielsweise können Benutzer ihre Erweiterungen in der Einstellungs-App verwalten:  

![Einstellungs-App](../../media/settings.png)  

Der Name der Erweiterung, die in der App "Einstellungen" in Windows angezeigt wird, stammt aus dem AppXManifest.  Wenn dieser Wert in Englisch hartcodiert ist, wird die englische Version des Namens auf nicht englischen Windows-Geräten angezeigt.  Wenn das Branding Ihrer Erweiterung nur Auf Englisch ist, ist es in Ordnung, sie hartcodiert zu lassen.  

> [!NOTE]
> Wenn Sie lokalisierte Namen für Ihre Microsoft Edge-Erweiterung in Windows verwenden [](./extensions-in-the-windows-dev-center.md#name-reservation) möchten, stellen Sie sicher, dass die lokalisierten Namen auch verfügbar und reserviert sind, bevor Sie die Änderungen in der AppXManifest-Datei vornehmen.  Wenn die Namen nicht reserviert sind, erhalten Sie den folgenden Fehler, wenn Sie das endgültige Paket in Windows Dev Center hochladen:  
> 
> ![Sprachfehler](../../media/language-error.png)  

Die i18n-basierte Lokalisierungsinfrastruktur, die für JavaScript-Erweiterungen definiert ist, gilt nur innerhalb der Microsoft Edge-Umgebung.  

Außerhalb von Microsoft Edge, in Windows und im Microsoft Store, basiert das einzige unterstützte Lokalisierungsframework auf dem Lokalisierungsframework für die universelle Windows-Plattform (UWP).  

Wir unterstützen zwar JSON-basierte Ressourcen für HTML-basierte Windows-Apps, aber das Schema für die JSON-Ressourcen ist nicht mit dem Schema für JavaScript-Erweiterungen definiert.  

Es folgen die wichtigsten Unterschiede bei [HTML-basierten Windows-Apps:](/previous-versions/windows/apps/hh465228(v=win.10))  

*   Ressourcen werden in `.resjson` Dateien anstelle von Dateien `.json` angegeben.  
*   Die unterstützten Locales sollten in der AppXManifest-Datei angegeben werden, dabei ist das erste Locale das Standard-Locale.  
*   HTML-basierte Windows-Apps-Ressourcen verwenden das folgende Schema:  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    Das durch einen Unterstrich bezeichnete Name/Wert-Paar sind Kommentare für die entsprechende Zeichenfolgenressource.  
*   `.resjson` Dateien werden in Dateien kompiliert, die während der Erstellung `.pri` von AppX-Paketen enthalten sein müssen.  
    
### <a name="creating-json-string-resources"></a>Erstellen von JSON-Zeichenfolgenressourcen  

Mit einem konfigurierten AppxManifest und den unterschiedenen i18n- und UWP-Lokalisierungsframeworks können Sie Ihre Ressourcendateien erstellen.  

Nur eine Ressourcenzeichenfolge im Manifest gilt für Microsoft Edge-Erweiterungspakete.  Die `DisplayName` Zeichenfolge wird häufig in JavaScript-Erweiterungen lokalisiert und kann problemlos den von Windows erwarteten Dateien zugeordnet `.resjson` werden.  Unter der Annahme, dass dies die einzige Ressource ist, die Sie lokalisieren möchten, finden Sie hier eine Beispieldatei, `.resjson` die erstellt werden sollte:  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

Die Ressourcen-ID in jeder `.resjson` Datei muss mit der ID übereinstimmen, die im AppXManifest verwendet wird.  Unter Verwendung des `.resjson` obigen Beispielausschnitts sollte der entsprechende AppXManifest-Eintrag folgendes sein:  

`DisplayName="ms-resource:DisplayName"`  

Jede sprache, die Ihre Erweiterung unterstützt, sollte über eine entsprechende Ressourcendatei verfügen und in der `.resjson` folgenden Ordnerstruktur platziert werden:  

![Sprachordnerstruktur](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a>Erstellen der Ressourcendatei  

Nachdem Sie alle Dateien erstellt haben, können Sie den Paketressourcenindex `.resjson` \(PRI\) erstellen.  In dieser Datei werden die Ressourcen für alle unterstützten Sprachen gespeichert.  Dazu können Sie das **MakePRI-Tool** verwenden, das im Windows 10 SDK enthalten ist.  

Zuerst müssen Sie die Konfigurationsdatei erstellen.  Dadurch werden die Standardqualifizierer und die Plattform für die Ressourcen definiert.  Erstellen Sie in diesem Beispiel die Standardsprache `English (US)` und die Plattform Windows 10.  Erstellen Sie dazu eine `priconfig.xml` Datei mit dem folgenden Inhalt in der `[Root folder]` :  

![priconfig im Ordner](../../media/priconfig.png)  

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```  

Jetzt können Sie die Konfigurationsdatei und das Tool MakePRI verwenden, um die Datei resources.pri zu erstellen.  In diesem Beispiel ist der Stammspeicherort für das Projekt `[Root folder]` .  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

Sie sollten nun eine resources.pri-Datei im Stammordner haben:  

![Ressourcenordner](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a>Lokalisieren von Name und Beschreibung im Microsoft Store  

Sobald Sie versuchen, ihr vollständiges, lokalisiertes Paket hochzuladen, erkennt das Windows Dev Center, dass mehrere Sprachen unterstützt werden, und überprüft, ob sie über entsprechende lokalisierte Namen und Beschreibungen für jede Sprache verfügen.  Wenn einer der lokalisierten Werte fehlt, wird Ihre Übermittlung blockiert, bis Sie die Werte bereitstellen.  

Wenn Sie nur einen lokalisierten Namen und eine Beschreibung für den Microsoft Store (und nicht Windows) bereitstellen möchten, können Sie dazu alle lokalisierten Namen für Ihre Erweiterung [reservieren.](./extensions-in-the-windows-dev-center.md#name-reservation)  

Nachdem Sie zusätzliche lokalisierte Namen reserviert haben, können Sie eine aktualisierte Übermittlung erstellen.  Im Abschnitt Beschreibung können Sie zusätzliche Sprachen für Ihren Microsoft Store-Eintrag verwalten:  

![Verwalten von Beschreibungssprachen](../../media/manage-description-languages.png)  

Nachdem Sie weitere Sprachen verwalten ausgewählt **haben,** können Sie auswählen, welche Sprachen Sie Ihrem Microsoft Store-Eintrag hinzufügen möchten.  Die neue Sprache wird im **Abschnitt** Beschreibung als zusätzliche **Beschreibungssprache** angezeigt.  

Sie können auf den einzelnen **** Link im Abschnitt Beschreibung klicken, um einen lokalisierten Namen und eine Beschreibung, Versionshinweise und visuelle Ressourcen für jede Sprache zur Verfügung zu stellen.  Die Beschreibung für den Microsoft Store wird nicht aus dem AppXManifest extrahiert.  Jede lokalisierte Beschreibung muss manuell im Windows Dev Center eingegeben werden:  

![Japanische App-Beschreibung](../../media/japanese-app-description.png)  

Nachdem die lokalisierten Beschreibungen übermittelt und die Erweiterung veröffentlicht wurde, wird jedem Benutzer, der auf eine lokalisierte Seite der Erweiterung im Microsoft Store zutritt, die folgende Benutzeroberfläche angezeigt:  

![japanischer Windows Store](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a>AppxManifest-Beispiele  

### <a name="non-localized-appxmanifest"></a>Nicht lokalisierte AppxManifest  

Das folgende Beispiel zeigt ein AppxManifest, das nicht lokalisiert ist und nur das `en-us` Locale unterstützt.  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  

#### <a name="localized-appxmanifest"></a>Lokalisierte AppxManifest  

Dieses AppxManifest-Beispiel ist für acht weitere Locales neben "en-us" lokalisiert. Beachten Sie `ms-resource:<resource id>` die Vorkommen:  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  
