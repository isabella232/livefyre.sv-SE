---
description: Använd Bootstrap- och Stream API med Livefyre-appar.
seo-description: Använd Bootstrap- och Stream API med Livefyre-appar.
seo-title: Appimplementering
solution: Experience Manager
title: Appimplementering
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Appimplementering {#appimplementation}

Användningsfall: Som kund vill jag integrera Livefyre i mitt CMS-system från tredje part med metoden Livefyre.js.

Det finns tre sätt att implementera Livefyre i en anpassad AEM-komponent eller andra CMS:er som WordPress, Sitecore eller DemandWare: Implementering, API, implementering och autentisering från tredje part.

## App-implementering för Designer {#designerapp}

Vad: Det enklaste och snabbaste sättet att integrera en Livefyre-app. Du kan utforma, konfigurera och generera en anpassad JavaScript-inbäddningskod för att integrera en LiveCycle-app på en sida på några minuter.

Hur: [Skapa, förhandsgranska, publicera och bädda in en Livefyre-app](/help/using/c-about-apps/c-create-an-app.md)

Exempel: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js-implementering {#livefyrejsimp}

Vad: [Livefyre.js](/help/implementation/c-livefyre.js.md) är huvudbiblioteket som driver Apps och Auth på en webbplats. Den definierar det globala `window.Livefyre` objektet och en enda offentlig metod, Livefyre.require, som kan användas för att läsa in andra LiveFyre JavaScript-bibliotek som hjälper till med inbäddning av Livefyre-appar och integrering med andra användarautentiseringssystem.

Hur:

* [Skapa en samling med CollectionMeta-token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrera appar i tredjeparts-CMS med appintegreringar

Exempel:

* Kommentarsapp: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Granskningsapp: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Medievägg: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Mer information om avancerade anpassningar med SDK finns i StreamHub SDK:er.

## API-implementering {#apiimplementation}

För att skapa anpassade upplevelser och datavisualiseringar kan Livefyre-appar skapas från grunden genom att använda Livefyre och sociala data med hjälp av API:t Bootstrap och Stream.

## Integrering av autentisering från tredje part {#thirdpartyauth}

Information om vilka Livefyre-appar som kräver autentisering finns i [Identitetsintegrering](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) för autentiseringsplattformar från tredje part.

## Kundexempel {#customerexamples}

Följande kunder implementerade Livefyre med CMS-integreringar från tredje part:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
