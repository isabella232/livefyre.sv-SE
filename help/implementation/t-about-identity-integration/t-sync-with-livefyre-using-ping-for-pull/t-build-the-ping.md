---
description: Bygg pinga så att sidan öppnas i Livefyre när användarna uppdaterar sin profil.
title: Bygg Ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
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
