---
description: Du kan använda Livefyre-identitet med LinkedIn för att tillåta användare att använda sina LinkedIn-inloggningar för att interagera med appar på webbplatsen.
seo-description: Du kan använda Livefyre-identitet med LinkedIn för att tillåta användare att använda sina LinkedIn-inloggningar för att interagera med appar på webbplatsen.
seo-title: Skapa en LinkedIn-app för användning med Livefyre-identitet
solution: Experience Manager
title: Skapa en LinkedIn-app för användning med Livefyre-identitet
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Skapa en LinkedIn-app för användning med Livefyre-identitet{#create-a-linkedin-app-for-use-with-livefyre-identity}

Du kan använda Livefyre-identitet med LinkedIn för att tillåta användare att använda sina LinkedIn-inloggningar för att interagera med appar på webbplatsen.

För att aktivera LinkedIn-inloggning krävs följande information för LinkedIn-appen:

* Konsumentnyckel (API-nyckel)
* Consumer Secret (API-hemlighet)

Så här skapar du en LinkedIn-app som ska användas med Livefyre-identitet:

1. Gå till https://www.linkedin.com/secure/developer och logga in på ditt LinkedIn-konto för att skapa en ny app eller välja en befintlig app som ska användas med Livefyre Identity.
1. Klicka på **[!UICONTROL Create Application]**.
1. Fyll i formuläret för att skapa programmet.
1. Aktivera appbehörigheterna **[!UICONTROL r_basicprofile]** och **[!UICONTROL r_emailaddress]** i **[!UICONTROL Default Application Permissions]**.
1. Ange **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** som `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Spara appen.
1. I **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** växlar du **[!UICONTROL Enable LinkedIn Login]** till **[!UICONTROL On]**.
1. Ange klient-ID och klienthemlighet för LinkedIn.
1. Klicka på **[!UICONTROL Save Settings]**.

När det är klart visas appinformationssidan för LinkedIn med programmets API-nyckel (Consumer Key) och API Secret (Consumer Secret) för användning på Studios integreringsinställningar.
