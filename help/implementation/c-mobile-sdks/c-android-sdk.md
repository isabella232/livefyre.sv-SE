---
description: Skapa Android-appar med Livefyre i botten.
seo-description: Skapa Android-appar med Livefyre i botten.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Skapa Android-appar med Livefyre i botten.

Använd det här biblioteket för att integrera Livefyre-tjänster i din Android-app. Med [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) får du ett tunt lager runt våra gemensamma API-mekanismer, baserat på utvecklingsmiljön för Gradle/Android Studio.

Livefyre innehåller också ett exempelprogram för [granskningar](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , baserat på denna SDK.

Denna Livefyre Android SDK kan användas i både Eclipse och Android Studio.

>[!NOTE]
>
>Innan du installerar Livefyre Android SDK måste du ha installerat [Android SDK](https://developer.android.com/sdk/index.html) i din miljö. Du måste även inkludera ytterligare Android SDK-paket, enligt beskrivningen i dokumentationen för Android-utvecklare > .
>[Lägga till SDK-paket](https://developer.android.com/sdk/installing/adding-packages.html)

Använd Android SDK Manager (finns i verktygsfältet Android Studio eller Eclipse) för att installera alla rekommenderade paket. Se även till att du inkluderar Androids supportdatabas.

## Eclipse {#section_dtm_slv_zz}

Så här lägger du till Livefyre Android SDK i ditt projekt i Eclipse:

1. Hämta den senaste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) från GitHub.
1. Börja med ett befintligt projekt eller skapa ett nytt.
1. Om du vill importera StreamHub-Android-SDK till arbetsytan går du till **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Bläddra och välj StreamHub-Android-SDK; den bör nu visas i paketutforskaren.
1. Högerklicka på ditt projekt och välj **[!UICONTROL Properties,]** sedan fliken Android.
1. Under biblioteksavsnittet väljer du **[!UICONTROL Add button,]** sedan StreamHub-Android-SDK i listan med bibliotek.
1. Klicka på **[!UICONTROL Apply]** och **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Så här lägger du till Livefyre Android SDK i ditt projekt i Android Studio:

1. Hämta den senaste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) från GitHub.
1. Börja med ett befintligt projekt eller skapa ett nytt.
1. Högerklicka på projektet och välj **[!UICONTROL Open Module Settings]**.
1. Markera **[!UICONTROL +]** knappen i fönstrets övre vänstra hörn.
1. Välj **[!UICONTROL Import Existing Project.]** (i den nya versionen av Android-studion hittar du **[!UICONTROL Import Existing Project]** under **[!UICONTROL More Modules]**.)

1. Bläddra och välj StreamHub-Android-SDK.

Android Studio kan begära att du konverterar SDK:n till en övertoningsversion; om detta inträffar väljer du **[!UICONTROL next]** sedan **[!UICONTROL finish]**.

Gå till **projektmappen > appmappen > build.gradle** -filen under beroenden för att lägga till följande beroende:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Kontrollera att följande rad finns i **projektmappen > settings.gradle** -filen:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Du kan anpassa konfigurationer inifrån Config.java.

## Klienter {#section_yfq_blv_zz}

StreamHub Android SDK visar flera klientklasser som kan användas för att begära Livefyre API-slutpunkter:

* **AdminClient** Exchange har en token för användarautentisering som innehåller användarinformation, nycklar och andra metadata.

* **BootstrapClient** Hämta senaste innehåll och metadata om en viss samling.

* **StreamClient** Avsök en ström för en samling för att hämta nytt, uppdaterat och borttaget innehåll.

* **WriteClient** Post, flagga och liknande innehåll i en samling.

