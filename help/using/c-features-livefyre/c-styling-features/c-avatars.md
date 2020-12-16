---
description: Tillåt användare att anpassa den bild som visas med innehållet.
seo-description: Tillåt användare att anpassa den bild som visas med innehållet.
seo-title: Avatarer
title: Avatarer
uuid: bf20f3bc-3dcc-4e16-a629-3380d1a7a3f2
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Avatars{#avatars}

Tillåt användare att anpassa den bild som visas med innehållet.

Användaravatarer visas (som standard) bredvid innehåll i alla appar och hämtas från det identitetsprofilsystem som används i implementeringen. Dessa avatarer varierar i storlek beroende på i vilken app de visas.

(Med Livefyre kan du inaktivera Avatars om du inte vill visa dem i dina appar.)

>[!NOTE]
>
>Avatarerna visas vid 25p x 25p för Chatt och 50p x 50p i de flesta andra appar.

## Avatarlagring {#section_zbh_x1f_wy}

Avatars läses in asynkront i Livefyre. När en användare först loggar in i appen eller ändrar sin associerade avatarbildfil läggs deras profilbild till i en uppgiftskö. (En standardavatar visas tillfälligt när användarens dator överförs till lagringsplatsen Livefyre avatar.)

## Gravatars {#section_mqh_p1f_wy}

Livefyre stöder användningen av Gravatars. Om en användare inte har någon egen avatar som en del av användarprofilen söker Livefyre efter en Gravatar för den användaren. Om ingen Gravatar finns används standardavataren.


Program som använder den här funktionen:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chatt](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskort](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Karta](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

