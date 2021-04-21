---
description: Instagram har ändrat antalet begäranden som alla företag som använder Instagram API, inklusive Livefyre, kan göra från 5 000 begäranden per timme och token till 200 begäranden per timme och token. Detta kallas hastighetsbegränsning.
title: Instagram Rate Limiting
exl-id: b13db09b-fb5a-4711-a566-d0976172e35e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Felsökning: Begränsningar för Instagram-innehåll {#instagram-rate-limiting}

Instagram har ändrat antalet begäranden som alla företag som använder Instagram API, inklusive Livefyre, kan göra från 5 000 begäranden per timme och token till 200 begäranden per timme och token. Detta kallas *hastighetsbegränsning*.

En token är samma som ett Instagram-konto.

Du kan råka ut för ett fel som begränsar möjligheten att söka efter eller hämta innehåll från Instagram eftersom du:

* Använder ett konto för mer än en ström
* har ett stort antal Instagram-strömmar
* Kan använda hashtaggar med hög volym (till exempel `#cats` eller `#beach`)

Så här minskar du effekten av Instagram hastighetsbegränsning:

* Anslut flera Instagram-konton till ditt nätverk. Mer information om hur du lägger till Instagram-konton i ditt nätverk finns i [Om Instagram-konton](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)
Inaktivera Instagram-strömmar som du inte använder
Se till att strömmarna är avsedda för rätt nyckelord och använd smarta taggsfilter för att göra frågorna mer korrekta. Mer information om hur du använder smarta taggfilter finns i [Smarta taggar](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md)
Minimera tiden när flera personer använder samma Instagram-konto i ett nätverk för att strukturera Instagram-innehåll.
