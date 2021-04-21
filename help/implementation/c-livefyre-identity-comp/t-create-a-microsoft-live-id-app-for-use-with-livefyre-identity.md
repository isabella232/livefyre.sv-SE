---
description: Du kan använda Livefyre Identity med Microsoft Live Identity för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.
title: Skapa en Microsoft Live Identity App för användning med Livefyre Identity
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Skapa en Microsoft Live Identity App för användning med Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Microsoft Live Identity för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.

För att användare ska kunna logga in med sina inloggningsuppgifter för Microsoft Live Identity krävs följande Microsoft Live Identity-information:

* Klient-ID (privat nyckel)
* Klienthemlighet (lösenord)

Så här skapar du en Microsoft Live Identity-app som ska användas med Livefyre Identity:

1. Skapa eller logga in på ett Microsoft Live-konto på [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Skapa ett nytt program eller välj ett befintligt program som ska användas med Livefyre-identitet.
1. Klicka på **[!UICONTROL Add Platform]** och välj sedan Webb som plattformstyp.
1. Kontrollera att alternativet **[!UICONTROL Allow Implicit Flow]** är markerat och ange omdirigerings-URL:en med ditt nätverksnamn i stället för {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Skapa ett nytt lösenord/nyckelpar för att hämta den privata nyckeln.
1. I **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** växlar du **[!UICONTROL Enable Microsoft Live Login]** till **[!UICONTROL On]**.
1. Ange Microsoft Live Client ID och Microsoft Live Client Secret.
1. Klicka på **[!UICONTROL Save Settings]**.

När det är klart visas appinformationssidan för Microsoft Live Identity med programmets klient-ID (Consumer Key) och Client Secret (Consumer Secret) som du kan använda på sidan Integreringsinställningar i Studio.
