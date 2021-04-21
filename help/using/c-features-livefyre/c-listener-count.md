---
description: Lyssnarantal är en räknare som spårar antalet webbplatsbesökare för en app på en sida och visar det här antalet.
title: Avlyssnarantal
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Avlyssnarantal{#listener-count}

Lyssnarantal är en räknare som spårar antalet webbplatsbesökare för en app på en sida och visar det här antalet.

Avlyssnarantal är antalet webbplatsbesökare som har en webbläsare öppen på den sida där en app instansieras. På så sätt kan du veta hur många besökare som finns på sidan vid en viss tidpunkt, så att du kan spåra dem när de tittar på direktuppspelning eller livematerial i realtid.

Livefyres avlyssnarantal fungerar så här:

1. Den webbplats som innehåller din app skickar en Livefyre-server var 60:e sekund.
1. Livefyre-servern svarar på det antal webbplatsbesökare på sidan som visar appen (definierat som antalet webbplatsbesökare med en webbläsare öppen för den sidan).
1. Antalet webbplatsbesökare på sidan där appen visas i appen.

Program som använder den här funktionen:

* [Chatt](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatarer för avlyssnare {#section_wcn_kxp_vz}

Avlyssnarantalet visar maximalt 10 avatarer och visar endast avatarer för de personer som har klickat på **[!UICONTROL Follow]** för konversationen.

>[!NOTE]
>
>På grund av utrymmesbegränsningar visar mobilgränssnittet endast antalet avlyssnare och en liten personikon.

I Livefyre Listener Count visas antalet personer som är aktiva på sidan vid en given tidpunkt, plus antalet personer efter konversationen. Om någon är på sidan och följer konversationen kommer användaren inte att räknas dubbelt. Om en användare till exempel är på en sida och klickar på **[!UICONTROL Follow]** kommer avlyssnarantalet inte att öka; om användaren sedan klickar på **[!UICONTROL Unfollow]**, minskar inte antalet.

Program som använder den här funktionen:

* [Chatt](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
