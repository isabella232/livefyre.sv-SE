---
description: Alla tweet som matchar en regel visas inte i en ström.
seo-description: Alla tweet som matchar en regel visas inte i en ström.
seo-title: Begränsning och tweetfrekvens
solution: Experience Manager
title: Begränsning och tweetfrekvens
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Begränsning och frekvens för tweets{#throttling-and-frequency-of-tweets}

Alla tweet som matchar en regel visas inte i en ström.

Twitter-regelbegränsning och Twitter-flödesavbrott kan begränsa antalet Tweets som visas i strömmen.

>[!NOTE]
>
>Om du vill försäkra dig om att specifika tweets ingår i strömmen använder du alternativet Överför resurs på sidan Alla resurser.

* Twitter-regler stryper innehåll och drar 1 tweet per regel var femte sekund. Det gör att innehåll som visas i Livefyre-appar kan vara mer balanserat och inte överbelastas med tweets. Genom att begränsa inkommande tweets på det här sättet förhindrar du också att strömmen blir översvämmad eller oläslig under höga trafikperioder.

   >[!NOTE]
   >
   >För att säkerställa att innehåll som författarna av ditt material kan visa i dina appar, även i strömmar med hög hastighet, begränsas aldrig reglerna för specifika författare.

* Twitter-flöden kan avbrytas av flera orsaker. I vissa fall skjuter inte Twitter ut Twitter, och Livefyre får därför inte något meddelande om det nya innehållet och kan inte visas. Tjänstavbrott i Twitters API:er, eller trafik på hashtaggar/nyckelord med hög volym, kan också resultera i missade tweets.

