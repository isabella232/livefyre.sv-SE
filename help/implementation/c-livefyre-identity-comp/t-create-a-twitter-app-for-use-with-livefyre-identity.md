---
description: Du kan använda Livefyre Identity med Twitter för att tillåta användare att använda sina Twitter-inloggningar för att interagera med appar på din webbplats.
title: Skapa en Twitter-app för användning med Livefyre-identitet
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Skapa en Twitter-app för användning med Livefyre-identitet{#create-a-twitter-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Twitter för att tillåta användare att använda sina Twitter-inloggningar för att interagera med appar på din webbplats.

För att aktivera Twitter-inloggning krävs följande appinformation för Twitter:

* Konsumentnyckel (API-nyckel)
* Consumer Secret (API-hemlighet)

Så här skapar du en Twitter-app som ska användas med Livefyre-identitet:

1. Gå till [https://apps.twitter.com/](https://apps.twitter.com/) och logga in på ditt Twitter-konto för att skapa en ny eller välja en befintlig app som ska användas med Livefyre Identity.
1. Från inställningssidan för programmet:

   * Ange **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (där **{networkName}** är det nätverksnamn som tillhandahålls av Livefyre. Exempel:** [!UICONTROL labs]** i **[!UICONTROL `labs.fyre.co`]**.)
   * Avmarkera **[!UICONTROL Enable Callback Locking]**.
   * Välj **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Välj **[!UICONTROL Access: Read only]** på fliken **[!UICONTROL Permissions]**.

När det är klart listas appens API-nyckel (Consumer Key) och API Secret (API Secret) på Twitter-sidan Application Management (Programhantering > Tangenter och åtkomsttoken) för användning på sidan Integreringsinställningar i Studio.
