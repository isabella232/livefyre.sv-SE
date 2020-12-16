---
description: Dela innehåll eller innehåll från en annan användare till Facebook, Twitter eller LinkedIn.
seo-description: Dela innehåll eller innehåll från en annan användare till Facebook, Twitter eller LinkedIn.
seo-title: Delning via sociala medier
solution: Experience Manager
title: Delning via sociala medier
uuid: 3fd8a628-2414-45b5-b91c-2ad33aad2634
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---


# Delning via sociala medier{#social-sharing}

Dela innehåll eller innehåll från en annan användare till Facebook, Twitter eller LinkedIn.

Med delning via sociala medier kan din community dela sina tankar från din app med sina vänner i sociala nätverk, inklusive Facebook, Twitter och LinkedIn, och dela andra användares innehåll till Facebook och Twitter. Genom att aktivera delning via sociala medier kan communityn sprida den bästa responsen till ert innehåll och få ut mer trafik till er webbplats.

## Dela innehåll till sociala nätverk {#section_t1q_mz2_wy}

Du kan konfigurera ditt nätverk så att användare kan dela till Twitter, Facebook eller LinkedIn när de publicerar innehåll i dina Livefyre-appar. Standardvärdet för Livefyre **[!UICONTROL Share Modal]** innehåller länkar till alla tre webbplatserna. Du kan anpassa det här modala språket med API:t Post To för att åsidosätta Livefyre-standardinställningen och implementera ditt eget. Mer information finns i Avancerade avsnitt > Aktivera delning via sociala medier.

När användare klickar på **[!UICONTROL Share]** för att publicera sina kommentarer i sociala nätverk (Facebook, Twitter eller LinkedIn) uppmanas de att logga in via den sociala appen. (Listan med tillgängliga delningsalternativ kan anpassas. Som standard visas kryssrutor för delning på Facebook och Twitter i alla appar.) För anpassade nätverk bör de sociala apparna konfigureras som dina sociala appar. Som en del av integreringsprocessen lägger du till programinloggningsuppgifter via sidan Integreringsinställningar i Studio.

>[!NOTE]
>
>LinkedIn inkluderas som standard i Livefyre Community-kommentarer. Anpassade nätverk måste ange värdet&quot;li&quot; när de bäddar in appen för att aktivera knappen LinkedIn i kommentarverktygsfältet. (Mer information finns i Aktivera delning via sociala medier i utvecklardokumenten.)

## Dela andra användares innehåll med sociala nätverk {#section_blw_vy2_wy}

När du klickar på **[!UICONTROL Share]** på en annan användares inlägg öppnas rutan Dela kommentar, som innehåller ett redigerbart textfält, dina aktiverade delningsalternativ och en permanent länk till inlägget.

Genom att klicka på **[!UICONTROL Share]** för ett inlägg:

* Användarna kan ansluta till sina sociala nätverk genom att klicka på Twitter- eller Facebook-ikonerna.
* När du har auktoriserat sidan att publicera i användarens sociala nätverk, kommer knapparna på Twitter eller Facebook att visas så att användaren vet att de är aktiva.
* Användarna kan anpassa innehållet i delningsrutan.
* Om du klickar på **[!UICONTROL Share]** skickas innehåll till användarens aktiva sociala nätverk, med en länk som tar andra till exakt det inlägg som användaren vill dela.
* Användare kan också välja att dela en länk till en viss kommentar genom att klistra in Permalink i ett e-postmeddelande, blogginlägg eller socialt nätverk.

>[!NOTE]
>
>Under integreringen kan du avgöra vilka sociala nätverk som är tillgängliga för delning av användarna. Du kan även integrera en anpassad Permalink för att ge enhetlighet med dina aktuella medialänkar.

När du klickar på **[!UICONTROL Share]** på en annan användares inlägg öppnas rutan **[!UICONTROL Share Comment]**, som innehåller ett redigerbart textfält, dina aktiverade delningsalternativ och en länk till inlägget.

Genom att klicka på **[!UICONTROL Share]** för ett inlägg:

* Användarna kan ansluta till sina sociala nätverk genom att klicka på Twitter- eller Facebook-ikonerna.
* När du har auktoriserat sidan att publicera i användarens sociala nätverk, kommer knapparna på Twitter eller Facebook att visas så att användaren vet att de är aktiva.
* Användarna kan anpassa innehållet i delningsrutan.
* Om du klickar på **[!UICONTROL Share]** skickas innehåll till användarens aktiva sociala nätverk, med en länk som tar andra till exakt det inlägg som användaren vill dela.
* Användare kan också välja att dela en länk till en viss kommentar genom att klistra in Permalink i ett e-postmeddelande, blogginlägg eller socialt nätverk.

>[!NOTE]
>
>Under integreringen kan du avgöra vilka sociala nätverk som är tillgängliga för delning av användarna. Du kan även integrera en anpassad Permalink för att ge enhetlighet med dina aktuella medialänkar.



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

