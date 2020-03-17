---
description: Du kan använda Livefyre Identity med Microsoft Live Identity för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.
seo-description: Du kan använda Livefyre Identity med Microsoft Live Identity för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.
seo-title: Skapa en Microsoft Live Identity App för användning med Livefyre Identity
solution: Experience Manager
title: Skapa en Microsoft Live Identity App för användning med Livefyre Identity
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Skapa en Microsoft Live Identity App för användning med Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Microsoft Live Identity för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.

För att användare ska kunna logga in med sina inloggningsuppgifter för Microsoft Live Identity krävs följande Microsoft Live Identity-information:

* Klient-ID (privat nyckel)
* Klienthemlighet (lösenord)

Så här skapar du en Microsoft Live Identity-app som ska användas med Livefyre Identity:

1. Skapa eller logga in på ett Microsoft Live-konto på [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Skapa ett nytt program eller välj ett befintligt program som ska användas med Livefyre-identitet.
1. Klicka **[!UICONTROL Add Platform]** och välj sedan Webb som plattformstyp.
1. Kontrollera att **[!UICONTROL Allow Implicit Flow]** alternativet är markerat och ange omdirigerings-URL:en med ditt nätverksnamn i stället för {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Skapa ett nytt lösenord/nyckelpar för att hämta den privata nyckeln.
1. I **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** växlar du **[!UICONTROL Enable Microsoft Live Login]** till **[!UICONTROL On]**.
1. Ange Microsoft Live Client ID och Microsoft Live Client Secret.
1. Klicka på **[!UICONTROL Save Settings]**.

När det är klart visas appinformationssidan för Microsoft Live Identity med programmets klient-ID (Consumer Key) och Client Secret (Consumer Secret) som du kan använda på sidan Integreringsinställningar i Studio.
