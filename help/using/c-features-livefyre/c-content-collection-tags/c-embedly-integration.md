---
description: Använd embed.ly för att visa flera medieformat direkt i appen.
title: Embedly-integrering
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 5%

---

# Embedly-integrering {#embedly-integration}

Använd `embed.ly` för att visa flera medieformat, direkt i appen.

För att kunna aktivera inbäddat mediematerial från en mängd olika källor, bland annat Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify och Tumblr, använder Livefyre-appar Embeg som tredjepartsleverantör för URL-expansion. Om en användare eller moderator innehåller en länk som stöds i ett inlägg, kommer de medier som ingår i länken att expandera när de publiceras i samlingen.

Det ger Livefyre-appar tillgång till de över 250 olika inbäddade mediaalternativen som Embeely stöder.

>[!NOTE]
>
>Livefyre expanderar bara en delmängd av Embeeks fullständiga leverantörslista. Inbäddade bilder utökas endast på HTTPS-sidor om leverantören är Twitter, YouTube, Imgur, Vine, Wikipedia eller SoundCloud. Kontakta din tekniska kontohanterare för ytterligare frågor om länkexpansion eller källor.

På den här sidan visas exempel på några populära inbäddade medietyper och deras tillåtna URL-mönster. `Embed.ly` lägger ständigt till nya källor. En fullständig lista över leverantörer finns på `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>Formateringen för e-post kräver en fullständig länk. Kortare länkar fungerar inte.

Det går bara att bädda in innehåll som kan visas för allmänheten. Om du försöker bädda in innehåll som inte är offentligt visas länken till innehållet i blogginlägget och en platshållarikon medföljer. När du klickar på länken visas ett felmeddelande från den tjänst där innehållet finns, till exempel ett Facebook-meddelande för ett foto som bara är för vänner. Kontakta kontohanteraren om du märker att mediefiler inte har expanderats som förväntat.

## Exempel på e-post-URL:er

| Typ | Provider | URL:er |
|--- |--- |--- |
| Kartor | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Obs**: URL:en måste börja med  `http` och inte  `https.` |
| Sociala nätverk | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Foton | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite’s Content Uploading Service) | `https://ow.ly/i/*` |
| Omröstningar | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Dropler | `https://d.pr/i/*` |
| Ljud | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Bloggar | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Program som använder den här funktionen:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chatt](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskort](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Karta](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Omröstningar](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Trender](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Knappen Överför](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
