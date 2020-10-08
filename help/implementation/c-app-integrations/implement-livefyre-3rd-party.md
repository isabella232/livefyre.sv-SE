---
description: Skapa Livefyre-appar från grunden för att skapa anpassade upplevelser och datavisualiseringar.
seo-description: Skapa Livefyre-appar från grunden för att skapa anpassade upplevelser och datavisualiseringar.
seo-title: Integrera Livefyre med tredjepartsintegrering
solution: Experience Manager
title: Integrera Livefyre i ett CMS-system
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Implementera Livefyre med tredjepartsintegrering

Skapa Livefyre-appar från grunden för att skapa anpassade upplevelser och datavisualiseringar.

Du kan skapa en Livefyre-app från grunden genom att konsumera Livefyre och sociala data med API:t för Bootstrap och direktuppspelning.

Information om vilka autentiseringsplattformar som stöds finns i Identitetsintegrering för Livefyre-appar som kräver autentisering.

Så här implementerar du konversationsappar (kommentarer, chatt, Live-blogg, sidobjekt):

1. Utför appintegrering.
a. Skapa en samling med CollectionMeta-token.
b. Integrera Livefyre-appar med webbplatser med hjälp av kodstrukturen Livefyre.js.

   * Mer information om hur du använder inbäddningskodstrukturen för Livefyre.js finns i [Bädda in ett program](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Mer information om hur du integrerar kommentarappen finns i [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md).

   * Mer information om hur du integrerar chattappen finns i [Chatta](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Mer information om hur du integrerar Live Blog App finns i [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Mer information om hur du integrerar Sidenotes App finns i [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Utför autentiseringsintegrering.
a. Skapa Autentiseringstoken för användare för att skicka och lagra användardata i Livefyre.
b. Integrera externa användar- och autentiseringsplattformar. En lista över plattformar som stöds finns i [Identitetsintegrering](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Utför appanpassningar. Alternativ för appanpassningar som matchar ert varumärke och er stil och lägger till anpassade funktioner.

Så här skapar du en visualiseringsapp (karta, medievägg, Trending, Carousel, bildband, Storify, Feature Card, Mosaic, Polls):

1. Utför appintegrering.
a. Skapa en samling med CollectionMeta-token.
b. Integrera Livefyre-appar med webbplatser med hjälp av kodstrukturen Livefyre.js. Mer information om hur du använder inbäddningskodstrukturen för Livefyre.js finns i [Bädda in ett program](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Mer information om hur du integrerar appen Karta finns i [Karta](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Mer information om hur du integrerar medieväggsappen finns i [Medievägg](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Mer information om hur du integrerar Trending App finns i [Trending](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Utför autentiseringsintegrering.
a. Skapa Autentiseringstoken för användare för att skicka och lagra användardata i Livefyre.
b. Integrera externa användar- och autentiseringsplattformar. En lista över plattformar som stöds finns i [Identitetsintegrering](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre stöder inte Carousel-, bildband-, Storify-, funktionskort-, mosaic- och omröstningsappar som använder Livefyre.js.

Integrera apparna med [Skapa en app](/help/using/c-about-apps/c-create-an-app.md) .