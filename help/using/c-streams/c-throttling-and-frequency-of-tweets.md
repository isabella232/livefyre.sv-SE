---
description: Alla tweet som matchar en regel visas inte i en ström.
title: Begränsning och tweetfrekvens
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Begränsning och frekvens för tweets{#throttling-and-frequency-of-tweets}

Alla tweet som matchar en regel visas inte i en ström.

Regelbegränsning för twitter och avbrott i Twitter-flöden kan begränsa antalet tweets som visas i strömmen.

>[!NOTE]
>
>Om du vill försäkra dig om att specifika tweets ingår i strömmen använder du alternativet Överför resurs på sidan Alla resurser.

* Twitter Rules stryper innehåll och drar 1 tweet per regel var femte sekund. Det gör att innehåll som visas i Livefyre-appar kan vara mer balanserat och inte överbelastas med tweets. Genom att begränsa inkommande tweets på det här sättet förhindrar du också att strömmen blir översvämmad eller oläslig under höga trafikperioder.

   >[!NOTE]
   >
   >För att säkerställa att innehåll som författarna av ditt material kan visa i dina appar, även i strömmar med hög hastighet, begränsas aldrig reglerna för specifika författare.

* Twitter Feed-avbrott kan inträffa av flera orsaker. I vissa fall skickas inte Tweets ut av Twitter, och därför får inte Livefyre något meddelande om det nya innehållet och kan inte visas. Tjänstavbrott i Twitter API:er, eller trafik på hashtaggar/nyckelord med stora volymer, kan också resultera i missade tweets.
