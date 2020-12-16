---
description: Bygg pinga så att sidan öppnas i Livefyre när användarna uppdaterar sin profil.
seo-description: Bygg pinga så att sidan öppnas i Livefyre när användarna uppdaterar sin profil.
seo-title: Bygg Ping
solution: Experience Manager
title: Bygg Ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Bygg Ping{#build-the-ping}

Bygg pinga så att sidan öppnas i Livefyre när användarna uppdaterar sin profil.

När Livefyre får ett uppdateringsmeddelande med `networkName` och `user_id` skickar systemet en Pull-begäran till Ping for Pull-URL:en.

>[!NOTE]
>
>403/Inte auktoriserad som svar på din Ping-begäran indikerar att en ogiltig `lftoken` har lagts till i Ping-begäran. Kontrollera att `lftoken` är för en `user_id` med nätverksägarbehörighet eller för systemanvändaren. Om du använder Livefyre-bibliotek ska du använda metoden `buildLivefyreToken` för att generera en giltig systemtoken för begäran.

1. Lägg till kod på sidan som pingar Livefyre när användare uppdaterar sin profil. Skapa URL:en på följande sätt:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Ditt Livefyre-nätverksnamn angavs.
   * **[!UICONTROL user_id:]** Användarens ID.
   * **[!UICONTROL token:]** Giltig systemtoken.

1. Dra in begärandestrukturen.
