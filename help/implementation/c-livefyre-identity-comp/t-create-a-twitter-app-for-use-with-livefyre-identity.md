---
description: Du kan använda Livefyre Identity med Twitter för att tillåta användare att använda sina Twitter-inloggningar för att interagera med appar på din webbplats.
seo-description: Du kan använda Livefyre Identity med Twitter för att tillåta användare att använda sina Twitter-inloggningar för att interagera med appar på din webbplats.
seo-title: Skapa en Twitter-app för användning med Livefyre-identitet
solution: Experience Manager
title: Skapa en Twitter-app för användning med Livefyre-identitet
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Skapa en Twitter-app för användning med Livefyre-identitet{#create-a-twitter-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Twitter för att tillåta användare att använda sina Twitter-inloggningar för att interagera med appar på din webbplats.

För att aktivera Twitter-inloggning krävs följande information om Twitter-appen:

* Konsumentnyckel (API-nyckel)
* Consumer Secret (API-hemlighet)

Så här skapar du en Twitter-app som ska användas med Livefyre-identitet:

1. Gå till [https://apps.twitter.com/](https://apps.twitter.com/)och logga in på ditt Twitter-konto för att skapa en ny eller välja en befintlig app som ska användas med Livefyre Identity.
1. Från inställningssidan för programmet:

   * Ange **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (där **{networkName}** är det nätverksnamn som tillhandahålls av Livefyre. Exempel:** [!UICONTROL labs]** i **[!UICONTROL `labs.fyre.co`]**.)
   * Avmarkera **[!UICONTROL Enable Callback Locking]**.
   * Välj **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. From the **[!UICONTROL Permissions]** tab, select **[!UICONTROL Access: Read only]**.

När det är klart kommer Twitters sida Application Management (Programhantering) > Keys and Access Tokens (Twitters) att visa programmets konsumentnyckel (API Key) och hemlighet (API Secret) för användning på Studios sida Integrationsinställningar.
