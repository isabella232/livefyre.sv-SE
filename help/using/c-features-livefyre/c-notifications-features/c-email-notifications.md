---
description: Tillåt användare att välja sin meddelandefrekvens och sitt innehåll.
seo-description: Tillåt användare att välja sin meddelandefrekvens och sitt innehåll.
seo-title: E-postmeddelanden
solution: Experience Manager
title: E-postmeddelanden
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---


# E-postmeddelanden{#email-notifications}

Tillåt användare att välja sin meddelandefrekvens och sitt innehåll.

**Aktivera e-postmeddelanden för användare och moderatorer.**

Med Livefyre-appar kan du aktivera e-postmeddelanden för användare och moderatorer baserat på specifika åtgärder. Meddelandena baseras på den tidpunkt då innehållet publiceras i strömmen, vilket gör att dina användare kan fortsätta engagera sig i konversationer som de bryr sig om och få meddelanden när någon gillar eller svarar på en av sina kommentarer.

Användare och moderatorer kan välja om de vill eller inte vill få e-postmeddelanden och kan ange hur ofta e-postmeddelanden ska tas emot. I det här avsnittet beskrivs hur du konfigurerar och anpassar dessa e-postmeddelanden.

* E-postalternativ för användare: tillgängliga alternativ för användarmeddelanden.
* Alternativ för moderatorns e-post: tillgängliga meddelandealternativ för moderator.
* E-postalternativ för Livefyre-identitet: e-postmeddelanden som skickas som en del av Livefyre Identity. Dessa e-postmeddelanden är bara relevanta för Livefyre Identity-kunder.
* Datasynkronisering med Livefyre: med att behålla inställningarna synkroniserade med Livefyre.
* Anpassa e-postmeddelanden: e-postanpassningar.

Använd alternativen **Inställningar > Integreringsinställningar > Inställningar för e-postavisering** för att anpassa e-postaviseringar för ditt nätverk.

>[!NOTE]
>
>För att se till att slutanvändarna inte får oönskad e-post skickas inga e-postmeddelanden från Livefyre UAT-miljön.

**E-postalternativ för användare**

Med Livefyre kan du göra det möjligt för användare att få e-postmeddelanden om webbplatsaktivitet. Använd integrationsinställningarna för användarprofiler som tillhandahålls via Livefyre för att göra det möjligt för användare att välja sina inställningar för meddelandescheman.

>[!NOTE]
>
>E-postmeddelanden skickas endast för innehåll som postas manuellt i strömmen, och inte för innehåll som hämtas från SocialSync.

Om du vill att användare ska kunna ange sina meddelandeinställningar lägger du till ett e-postmeddelande i användarinställningarna för ditt användarprofilsystem. Lägg till motsvarande fält i databasschemat för din användarprofil och hantera sedan dina användarinställningar med Ping for Pull. (Samarbeta med din Technical Integration Manager för att definiera standardfrekvenser för ditt nätverk. Om du är Enterprise Profiles-kund skickar du de valda standardvärdena till ditt Livefyre-leveransteam för konfiguration i Livefyre-databasen.)

Användare på din webbplats kan sedan följa en konversation och börja få e-postmeddelanden genom att klicka på knappen **[!UICONTROL +Follow]** i kommentarredigeraren. Meddelandeinställningarna definieras på Livefyres nätverksnivå. Alla användarinställningar gäller för alla webbplatser och konversationer i nätverket.

**Rekommenderade standardvärden**

* Någon kommenterar i en konversation som jag följer:** Sammandrag per timme**
* Någon gillar en av mina kommentarer:** Sammandrag per timme**
* Någon besvarar en av mina kommentarer:** omedelbart**
* Följ konversationer automatiskt när jag lämnar en kommentar:** av** (avmarkerat)

**Obs**: E-postmeddelanden baseras på den tid som innehållet har godkänts för att inkluderas i strömmen.

Livefyre har två alternativ för e-postfrekvens:

* Omedelbart
* Timsammandrag

**Omedelbart**

E-postmeddelanden som skickas omedelbart visar postens text, artikelrubrik, författarens användarnamn och en **svarslänk** som tar användaren till innehållet på sidan. Dessa e-postmeddelanden innehåller även länken **unsubscribe** i sidfoten, vilket gör att användare kan avbryta prenumerationen på e-postmeddelanden för den samlingen. Om du klickar på **unsubscribe **kommer du till en bekräftelsesida där du ser att de har avbeställt prenumerationen.

**Timsammandrag**

E-postmeddelanden som skickas i en timsammandrag visar allt innehåll, svar på innehåll och gilla-markeringar i innehållet inom den senaste timmen (eller så) per app som användaren följer. Om användaren följer flera appar i nätverket får användaren ett e-postmeddelande med en sammanfattning för varje app.

>[!NOTE]
>
>I konversationer utan nytt innehåll under mer än flera timmar får användare med timsammandrag aktiverat ett meddelande omedelbart efter ett nytt inlägg.

**E-postalternativ för moderator**

Moderatorer kan välja att få e-post för innehåll som publicerats i en app de följer och för kommentarer som har flaggats som skräppost eller stötande i en app de modererar. **Obs!** Inga e-postmeddelanden skickas när användare flaggar en kommentar med inställningen Inte instämmer eller Ej ämne, eftersom dessa kategorier inte anses viktiga för moderatormeddelanden.

Fälten moderator_comments och moderator_flags bör också läggas till i databasschemat för användarprofilsinställningar för moderatorn så att moderatorerna kan uppdatera frekvensen för sina e-postmeddelanden och avanmäla sig om de vill. Livefyre rekommenderar att du ställer in dessa två e-postmeddelandefält för moderatorn på **never**. Alternativen är **never** (standard), **directly** och **ofta**.

**Moderatorns e-postadress (flaggat innehåll):**

När innehåll flaggas i en modererad app visar det e-postmeddelande som skickas till moderatorn det innehåll som flaggats, det användarnamn som flaggade innehållet och en länk tillbaka till innehållssidan.

När en användare ändrar sina inställningar för e-postmeddelanden på din webbplats i ditt profilsystem synkroniserar du uppdateringen till fjärrprofilsystemet Livefyre med Livefyres Ping for Pull.

**Datasynkronisering med Livefyre**

## Anpassa e-postmeddelanden {#section_jxb_c5k_yy}

Flera fält i e-postmeddelandemallarna kan ändras så att de passar din stil och ditt varumärke.

* **[!UICONTROL From Email Address]**

   &quot;Från e-postadress&quot; för alla e-postmeddelanden kan anpassas så att de överensstämmer med ert varumärke. Livefyre rekommenderar **noreply@customerdomain.com** att ersätta **kunddomän** med ditt domännamn. (Standardvärdet är **noreply@livefyre.com**.) Skicka önskat &quot;från e-postadress&quot; till din Technical Integration Manager för konfiguration i Livefyre-databasen för ditt nätverk.

   >[!NOTE]
   >
   >Lämna det här fältet tomt om du vill inaktivera e-postmeddelanden för nätverket

* **[!UICONTROL Email Logo]**

   Den logotyp som visas i e-postmeddelanden kan anpassas för att visa din företagslogotyp, i stället för standardlogotypen Livefyre, på fliken Varumärke på sidan **Nätverksinställningar** i Studio. Anpassningen är endast tillgänglig på nätverksnivå, inte på webbplatsnivå, och är endast tillgänglig för betalande Livefyre-kunder.

* **[!UICONTROL Custom Templates]**

   Du kan implementera en helt anpassad e-postmall om du vill. Detta kommer dock att kräva en viss utvecklingsinsats och kan medföra kostnader för professionella tjänster. Kontakta kontohanteraren för mer information.



Program som använder den här funktionen:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskort](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

