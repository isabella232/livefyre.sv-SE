---
description: Beskriver alternativ för att lägga till användarautentisering i Livefyre-appar, inklusive Janrain Capture eller din egen identitetstjänst.
seo-description: Beskriver alternativ för att lägga till användarautentisering i Livefyre-appar, inklusive Janrain Capture eller din egen identitetstjänst.
seo-title: Identitetsintegrering
solution: Experience Manager
title: Identitetsintegrering
uuid: 079dc9c7-656a-49d0-920d-9e5a421a319c
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Identitetsintegrering{#identity-integration}

Beskriver alternativ för att lägga till användarautentisering i Livefyre-appar, inklusive Janrain Capture eller din egen identitetstjänst.

## Identitetsintegrering {#t_about_identity_integration}

Beskriver alternativ för att lägga till användarautentisering i Livefyre-appar, inklusive Janrain Capture eller din egen identitetstjänst.

Livefyre-apparna innehåller interaktiva funktioner som att publicera en kommentar, skriva en granskning eller gilla innehåll. För att dina användare ska kunna interagera med Livefyre-appar måste du integrera Livefyre med en identitetstjänst med Livefyre.js Auth.

Livefyre.js Auth tillhandahåller centraliserad autentisering för alla Livefyre-appar på er webbplats och ger er det exakta sättet användare ska logga in och registrera sig. Lägg till Auth globalt i webbplatsens mall och använd den på alla sidor, eller lägg till den en gång per sida, och när användarna har signerat i Livefyre JS Auth skickar automatiskt användarens information till alla appar på sidan.

Vare sig du har byggt en anpassad identitetstjänst eller använder en identitetstjänst från tredje part som Janrain Capture, täcker det här avsnittet allt du behöver veta för att kunna integrera.
