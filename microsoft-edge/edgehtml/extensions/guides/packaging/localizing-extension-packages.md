---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Erfahren Sie, wie Sie Ihr Microsoft Edge-Erweiterungspaket lokalisieren, damit es bei der Veröffentlichung für mehrere Gebietsschemas bereit ist.
title: Lokalisierung von Erweiterungspaketen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cfa85eda47fd71099bb5d201d1cf85992931228c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234153"
---
# Lokalisieren von Microsoft Edge-Erweiterungen für Windows und den Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

In diesem Leitfaden wird erläutert, wie Sie Ihre Microsoft Edge-Erweiterung lokalisieren können, damit Sie bei der Veröffentlichung für mehrere Gebietsschemas bereit steht. Um Ihre Erweiterung vollständig zu lokalisieren, müssen Sie die Schritte für Windows und den Microsoft Store Befolgen.

Wenn Sie Ihre Erweiterungs Ressourcen für Microsoft Edge lokalisieren möchten, erfahren Sie, wie Sie das i18n-Framework im [Internationalisierungs Leit Faden](../internationalization.md)verwenden können.


> [!NOTE]
> Wenn Ihre Erweiterung nicht mehrere Sprachen unterstützt, können Sie [im Microsoft Store mit dem Lokalisieren von Name und Beschreibung](#localizing-name-and-description-in-the-microsoft-store)fortfahren.


## Übersicht über den Lokalisierungsprozess

Der erste Schritt zur Verfügbarkeit ihrer Erweiterung für ein breites Publikum besteht darin, die AppxManifest für mehrere Sprachen zu [Konfigurieren](#configuring-the-appxmanifest) . Im Microsoft Store werden die Benutzer in den von der Erweiterung unterstützten Sprachen angezeigt. Bestimmte Felder in der AppxManifest müssen ebenfalls geändert werden, wenn der Name der Erweiterung [in der Windows-Benutzeroberfläche und im Microsoft Store lokalisiert](#localizing-extension-resources-for-windows-and-the-microsoft-store)werden soll.


Nachdem Ihr AppxManifest konfiguriert wurde, müssen sie JSON- [Zeichenfolgenressourcen](#creating-json-string-resources) für die Sprachen erstellen, die Sie als unterstützt angegeben haben. Dies erfordert das Erstellen einer resjson-Datei für jede Sprache, in der jede Datei alle UI-Zeichenfolgen dieser Sprache enthält.


Nachdem die resjson-Dateien für die unterstützten Sprachen erstellt wurden, [muss eine PRI-Ressourcendatei erstellt werden](#creating-the-resources-file). Diese wird mithilfe einer Konfigurationsdatei für das **"makepri** -Tool erstellt, das im Lieferumfang des [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)enthalten ist. 

> [!NOTE]
> Wenn Sie das Windows 10 SDK nur herunterladen, um das MakePri.exe-Tool zu verwenden, können Sie nur die Features "Windows SDK-Signatur Tools für Desktop-Apps" und "Windows SDK für UWP-verwaltete Apps" auswählen, um das Herunterladen leichter zu halten. Das MakePri.exe-Tool wird in Unterordnern von C:\Program Files (x86)-Kits\10\bin\10.0.17713.0. angezeigt.


Nachdem Sie Ihre Erweiterung hochgeladen haben, besteht der letzte Schritt darin, [den Namen und die Beschreibung im Microsoft Store zu lokalisieren](#localizing-name-and-description-in-the-microsoft-store).

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion. Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.



## Konfigurieren des AppXManifest

Die Liste der unterstützten Sprachen der Erweiterung wird im Microsoft Store basierend auf Ihren AppXManifest-Werten generiert. Diese Liste wird mit dem `Resource` Element angegeben.


![Einstellungen Bild-Sprache-App-Details](./../../media/language-app-details.png)

Wenn Sie die Liste der Sprachen angeben möchten, die von der Erweiterung unterstützt werden, können Sie ein `Resource` Element im unten gezeigten Format hinzufügen (dieses `Resource` Element zeigt die Unterstützung für Englisch, Deutsch und Französisch im Microsoft Store):

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

Informationen zu den vom Microsoft Store unterstützten Sprachen/Sprachencodes finden Sie unter [Unterstützte Sprachen](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .


Um lokalisierte Zeichenfolgen für alle öffentlich sichtbaren Elemente in der AppxManifest anzugeben, müssen Sie einen Ressourcenbezeichner im Format von verwenden `ms-resource:<resource id>` .

Die folgenden Snippets machen eine vollständige AppxManifest. Die folgenden Werte sollten aus lokalisierten Ressourcendateien abgerufen werden:

- Properties\DisplayName
- Properties\Description
- Properties\PublisherDisplayName


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- Applications\Application\VisualElements\DisplayName
- Applications\Application\VisualElements\Description
- Applications\Application\Extensions\Extension\AppExtension\DisplayName

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


## Lokalisieren von Erweiterungs Ressourcen für Windows und den Microsoft Store

Nachdem Ihr AppxManifest für mehrere Sprachen konfiguriert wurde, gibt es einige wichtige Unterschiede, die Sie kennen sollten, wenn Sie die Benutzeroberfläche in ihrer Erweiterung lokalisieren und ihre Erweiterung für Windows und den Microsoft Store lokalisieren möchten.

Während Microsoft Edge-Erweiterungen nicht außerhalb von Microsoft Edge ausgeführt werden, kann die Verwaltung in Windows erfolgen. Beispielsweise können Benutzer Ihre Erweiterungen in der Einstellungs-APP verwalten:


![Bild ' Einstellungen '](./../../media/settings.png)



Der Name der Erweiterung, die in der Einstellungs-APP in Windows angezeigt wird, stammt aus dem AppXManifest. Wenn dieser Wert in Englisch hart codiert ist, wird die englische Version des Namens auf nicht englischen Windows-Geräten angezeigt. Wenn das Branding Ihrer Erweiterung nur Englisch ist, ist es in Ordnung, Sie hart codiert zu lassen.


> [!NOTE]
> Wenn Sie lokalisierte Namen für Ihre Microsoft Edge-Erweiterung in Windows verwenden möchten, stellen Sie sicher, dass die lokalisierten Namen ebenfalls [verfügbar und reserviert](./extensions-in-the-windows-dev-center.md#name-reservation) sind, bevor Sie die Änderungen in der AppXManifest-Datei vornehmen. Wenn die Namen nicht reserviert sind, erhalten Sie die folgende Fehlermeldung beim Hochladen des endgültigen Pakets in Windows dev Center:</br></br>

![Sprachfehler](./../../media/language-error.png)</br></br>


Die für JavaScript-Erweiterungen definierte i18n-basierte Lokalisierungs Infrastruktur ist nur innerhalb der Microsoft Edge-Umgebung anwendbar.

Außerhalb von Microsoft Edge, in Windows und im Microsoft Store, basiert das einzige unterstützte Lokalisierungs Framework auf dem Lokalisierungs Framework für die universelle Windows-Plattform (UWP).

Obwohl wir JSON-basierte Ressourcen für HTML-basierte Windows-apps unterstützen, entspricht das Schema für die JSON-Ressourcen nicht dem für JavaScript-Erweiterungen definierten.


Im folgenden finden Sie die wichtigsten Unterschiede in [HTML-basierten Windows-apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):
-    Ressourcen werden in resjson-Dateien anstelle von JSON-Dateien angegeben.
-    Die unterstützten Gebietsschemas sollten in der AppXManifest-Datei angegeben werden, wobei das erste Gebietsschema das Standardgebietsschema ist.
-    HTML-basierte Windows-apps-Ressourcen verwenden das folgende Schema:
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    Das Name-Wert-Paar, das durch einen Unterstrich gekennzeichnet ist, ist ein Kommentar für die entsprechende Zeichenfolgenressource.
-    resjson-Dateien werden in PRI-Dateien kompiliert, die während der AppX-Paketerstellung enthalten sein müssen.


### Erstellen von JSON-Zeichenfolgenressourcen
Mit einem konfigurierten AppxManifest in der Hand und den Unterschieden zwischen den hervorgehobenen i18n-und UWP-Lokalisierungs Frameworks können Sie Ihre Ressourcendateien erstellen.

Nur eine Ressourcenzeichenfolge im Manifest ist auf Microsoft Edge-Erweiterungspakete anwendbar. Die `DisplayName` Zeichenfolge wird häufig in JavaScript-Erweiterungen lokalisiert und kann problemlos den resjson-Dateien zugeordnet werden, die von Windows erwartet werden. Wenn Sie davon ausgehen, dass dies die einzige Ressource ist, die Sie lokalisieren möchten, finden Sie hier eine Beispiel-resjson-Datei, die erstellt werden soll:

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

Die Ressourcen-ID in jeder resjson-Datei muss mit der im AppXManifest verwendeten ID übereinstimmen. Mit dem obigen Beispiel. resjson-Snippet sollte der entsprechende AppXManifest-Eintrag wie folgt lauten:

`DisplayName="ms-resource:DisplayName"`

Jede Sprache, die von der Erweiterung unterstützt wird, sollte über eine entsprechende Resources. resjson-Datei verfügen und in der folgenden Ordnerstruktur abgelegt werden:

![Sprachordner Struktur](./../../media/resources-folder.png)


### Erstellen der Ressourcendatei
Nachdem Sie alle Ihre resjson-Dateien erstellt haben, können Sie Ihre PRI-Datei (Package Resource Index) erstellen. Diese Datei speichert die Ressourcen für alle unterstützten Sprachen. Dazu können Sie das **"makepri** -Tool verwenden, das im Lieferumfang des Windows 10 SDK enthalten ist.


Zunächst müssen Sie die Konfigurationsdatei erstellen. Damit werden die Standardqualifizierer und die Plattform für die Ressourcen definiert. Führen Sie in diesem Beispiel die Standardsprache Englisch (USA) und die Plattform Windows 10 aus. Erstellen Sie dazu eine priconfig.xml-Datei mit folgendem Inhalt im [root-Ordner]:

![priconfig im Ordner](./../../media/priconfig.png)


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

Nun können Sie die Konfigurationsdatei und das "makepri-Tool verwenden, um die Datei" Resources. pri "zu erstellen. In diesem Beispiel wird der Stammspeicherort für das Projekt [Stammordner] sein.


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

Sie sollten nun über eine Datei "Resources. pri" im Stammordner verfügen:

![Ordner "Ressourcen"](./../../media/resources.png)


## Lokalisieren von Name und Beschreibung im Microsoft Store

Nachdem Sie das vollständige, lokalisierte Paket hochgeladen haben, wird im Windows dev Center festgestellt, dass mehr als eine Sprache unterstützt wird, und es wird überprüft, ob Sie über entsprechende lokalisierte Namen und Beschreibungen verfügen. Wenn einer der lokalisierten Werte fehlt, wird ihre Übermittlung blockiert, bis Sie die Werte bereitstellen.

Wenn Sie nur einen lokalisierten Namen und eine Beschreibung für den Microsoft Store (und nicht für Windows) bereitstellen möchten, können Sie dies tun, indem Sie [alle lokalisierten Namen für Ihre Erweiterung reservieren](./extensions-in-the-windows-dev-center.md#name-reservation).


Nachdem Sie weitere lokalisierte Namen reserviert haben, können Sie eine aktualisierte Übermittlung erstellen. Im Abschnitt Beschreibung können Sie weitere Sprachen für Ihren Microsoft Store-Eintrag verwalten:

![Beschreibung der japanischen App – verwalten](./../../media/manage-description-languages.png)

Nachdem Sie "zusätzliche Sprachen verwalten" ausgewählt haben, können Sie auswählen, welche Sprachen Sie Ihrem Microsoft Store-Eintrag hinzufügen möchten. Die neue Sprache wird im Abschnitt "Beschreibung" als "zusätzliche Beschreibungssprache" angezeigt.

Sie können auf den einzelnen Link im Abschnitt "Beschreibung" klicken, um einen lokalisierten Namen und eine Beschreibung, Anmerkungen zur Version und visuelle Ressourcen für jede Sprache bereitzustellen. Die Beschreibung für den Microsoft Store wird nicht aus dem AppXManifest extrahiert. Jede lokalisierte Beschreibung muss manuell in das Windows dev Center eingegeben werden:

![Beschreibung der japanischen App](./../../media/japanese-app-description.png)

Sobald die lokalisierten Beschreibungen übermittelt und die Erweiterung veröffentlicht wurde, wird jedem, der auf eine lokalisierte Seite der Erweiterung im Microsoft Store zugreift, die folgende Benutzeroberfläche angezeigt:

![japanischer Windows Store](./../../media/japanese-windows-store.png)
 

## AppxManifest-Beispiele

### Nicht lokalisierte AppxManifest
Das folgende Beispiel zeigt eine AppxManifest, die nicht lokalisiert ist, und unterstützt nur das "en-US"-Gebietsschema.


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


#### Lokalisierte AppxManifest
Dieses AppxManifest-Beispiel ist für acht andere Gebietsschemas außer "en-US" lokalisiert. Beachten Sie die `ms-resource:<resource id>` Vorkommnisse:


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
