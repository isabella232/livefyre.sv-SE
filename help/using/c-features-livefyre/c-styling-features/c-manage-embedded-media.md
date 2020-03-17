---
description: Definiera källor från vilka användare får publicera media och från vilka medietjänster ska förbjudas.
seo-description: Definiera källor från vilka användare får publicera media och från vilka medietjänster ska förbjudas.
seo-title: Hantera inbäddade media
title: Hantera inbäddade media
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Hantera inbäddade media{#manage-embedded-media}

Definiera källor från vilka användare får publicera media och från vilka medietjänster ska förbjudas.

Som standard kan alla bifogade mediefiler bäddas in i kommentarer. En fullständig lista över leverantörer som stöds finns på embed.ly/providers.

Livefyre använder Embed.ly och standardinbäddningsprotokoll för att bädda in media i appströmmar och kommer att passera genom alla mediedata som tillhandahålls av dess källa.

Embed.ly skickar all tillgänglig information, inklusive mediets titel, beskrivning, miniatyrbild och inbäddningskod för alla angivna URL:er. Vilka objekt som är tillgängliga varierar beroende på leverantör. Till exempel: Facebook returnerar inte miniatyrbilder för sina videor och skickar bara en inbäddad video. När du klickar på Spela upp startas videon (liknande YouTubes visningsformat). Twitter skickar bara statiska bilder och skickar inte videor. Det innebär att inbyggda Twitter-videor kanske inte kan spelas upp inifrån en Livefyre-ström.

Du kan förhindra att vissa bilagor bäddas in i kommentarer när du bäddar in kommentarströmmen. Du kan också välja att dölja alla Embed.ly-tillägg på nätverks-, webbplats- och konversationsnivå med Studio och endast visa länkar till mediet, inte helt inbäddade media.

Program som använder den här funktionen:

* [Funktionskort](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Karta](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

