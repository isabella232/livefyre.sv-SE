---
description: Lyssnarantal är en räknare som spårar antalet webbplatsbesökare för en app på en sida och visar det här antalet.
seo-description: Lyssnarantal är en räknare som spårar antalet webbplatsbesökare för en app på en sida och visar det här antalet.
seo-title: Avlyssnarantal
solution: Experience Manager
title: Avlyssnarantal
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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

## Avataravlyssnare {#section_wcn_kxp_vz}

Avlyssnarantalet visar maximalt 10 avatarer och visar endast avatarer för de personer som har klickat **[!UICONTROL Follow]** för konversationen.

>[!NOTE]
>
>På grund av utrymmesbegränsningar visar mobilgränssnittet endast antalet avlyssnare och en liten personikon.

I Livefyre Listener Count visas antalet personer som är aktiva på sidan vid en given tidpunkt, plus antalet personer efter konversationen. Om någon är på sidan och följer konversationen kommer användaren inte att räknas dubbelt. Om en användare till exempel befinner sig på en sida och klickar **[!UICONTROL Follow]** kommer avlyssnarantalet inte att öka; om användaren sedan klickar **[!UICONTROL Unfollow]** minskar inte antalet.

Program som använder den här funktionen:

* [Chatt](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

