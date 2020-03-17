---
description: Du kan använda Livefyre Identity med Yahoo! så att användarna kan använda sina Yahoo! inloggningar för att interagera med appar på din webbplats.
seo-description: Du kan använda Livefyre Identity med Yahoo! så att användarna kan använda sina Yahoo! inloggningar för att interagera med appar på din webbplats.
seo-title: Skapa en Yahoo! App för användning med Livefyre-identitet
solution: Experience Manager
title: Skapa en Yahoo! App för användning med Livefyre-identitet
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Skapa en Yahoo! App för användning med Livefyre-identitet{#create-a-yahoo-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Yahoo! så att användarna kan använda sina Yahoo! inloggningar för att interagera med appar på din webbplats.

För att användarna ska kunna logga in med sina Yahoo-inloggningsuppgifter krävs följande Yahoo-appinformation för Livefyre:

* Klient-ID (konsumentnyckel)
* Klienthemlighet (konsumenthemlighet)

För att skapa en Yahoo! app för användning med Livefyre Identity:

1. Gå till [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)och logga in på din Yahoo! för att skapa ett nytt eller välja en befintlig app som ska användas med Livefyre-identitet.
1. Välj **[!UICONTROL Application Type: Web Application]**.
1. Ange **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Markera **[!UICONTROL API Permissions: Profiles (Social Directory)]** och **[!UICONTROL Read Public]**.

   När det är klart visas appinformationssidan för Yahoo med programmets klient-ID (Consumer Key) och Client Secret (Consumer Secret) för användning på Studios integreringsinställningar.

   >[!NOTE]
   >
   >Om du aktiverar Yahoo! logga in utan att skapa en Yahoo! och om du lämnar fälten för klient-ID och Klienthemlighet i Studio tomma, kommer Livefyre att använda OpenID för att logga in dessa användare i dina Livefyre-appar. OAuth och anpassad varumärkning kommer inte att vara tillgängliga i detta fall.