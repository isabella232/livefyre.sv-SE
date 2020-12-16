---
description: Granskningar erbjuder ett brett urval av anpassningar så att du kan skapa en granskningsapp som passar dina behov och ditt varumärke.
seo-description: Granskningar erbjuder ett brett urval av anpassningar så att du kan skapa en granskningsapp som passar dina behov och ditt varumärke.
seo-title: Skapa en app för granskningar
solution: Experience Manager
title: Skapa en app för granskningar
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---


# Skapa en granskningsapp{#creating-a-reviews-app}

Granskningar erbjuder ett brett urval av anpassningar så att du kan skapa en granskningsapp som passar dina behov och ditt varumärke.

Använd appen Recensioner genom att bädda in den på din webbplats som ett JS-program. Du kan inte skapa en granskningsapp i Livefyre Studio. Information om hur du skapar en granskningsapp på din webbplats finns i [Granska integrering](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Klassificeringar {#section_hs5_c4h_21b}

Klassificeringar är det numeriska värde som användarna tilldelar granskningen. Alla granskningar måste innehålla en gradering, som visas som ett 5-stjärnigt system som standard. (Medan klassificeringarna visas som 0,5-5 i appen lagrar Livefyre förhållandet X/100 i bakänden, så att 1 stjärna är 20/100 och 2 stjärnor är 40/100. Proportionerna visas när du tittar på granskningarna i Studio.)

Värderingsskalan 0,5 till 5 kan konfigureras upp till 100, med halv gradering också tillgänglig.

Mer information finns i fältet maxRating för objektet convConfig för granskningar.

## Klassificeringsikonformat {#section_cqn_c4h_21b}

Klassificeringsikonerna kan anpassas efter din profilering och stil.

Mer information finns i **[!UICONTROL Configure Star Ratings]** under Anpassa granskningar.

## Klassificera Dimensioner {#section_cnx_snh_21b}

Klassificeringsdimensioner är de kategorier som dina granskare betygsätter din produkt eller tjänst för. Exempel på klassificeringsdimensioner är&quot;prestanda&quot;,&quot;design&quot;,&quot;kostnad&quot;,&quot;total&quot; eller någon annan kategori som du väljer.

Som standard visas en&quot;övergripande&quot; graderingsdimension, men du kan definiera och implementera flera graderingsdimensioner, vilket visas i exemplet nedan.

Mer information finns i fältet ratingDimensions under Metadata för Granska samling.

## Granska textfält {#section_xcm_4nh_21b}

Du kan även inkludera ytterligare textfält på den produkt eller upplevelse som granskas. (Textfält kan t.ex. innehålla utkast och konturer, eller missa inte.) Fältets nummer, rubrik och standardtext kan anpassas. Användarna måste fylla i alla textfält samt granskningstitel, brödtext och gradering för att kunna publicera sin granskning. Det går inte att inkludera valfria textfält.

Mer information finns i fältet ratingDimensions för Metadata för granskningssamling.

## Granska sammanfattning {#section_ysz_lnh_21b}

Som standard visas ett sammanfattningsavsnitt högst upp i granskningsappen. I det här avsnittet finns en visualisering av genomsnittlig användarklassificering och klassificeringsuppdelning för granskningssamlingen, där endast heltal visas. Det här avsnittet är skrivskyddat och kan döljas om så önskas.

Mer information finns i fältet ratingSummaryEnabled för convConfig-objektet Reviews.

## Skräppost och Profanity-filter {#section_hcm_jnh_21b}

Texten i en gransknings titel och brödtext skickas via vårt skräppostfilter och Profanity-filter så snart granskningen är publicerad.

## Textanpassning {#section_tjf_hnh_21b}

Textsträngar, inklusive verktygstips och etiketter, kan anpassas efter språk eller efter ditt varumärke.

## Svara på en granskning {#section_yng_fnh_21b}

Användarna kan svara på sina egna eller andras granskningar i varje granskningssamling. Endast användare som är inloggade kan skicka ett svar på en granskning.

Alternativet för användare att svara på en granskning är aktiverat i Studio. Ägarna kan växla den här inställningen för nätverks-, webbplats- eller samlingsnivån. Moderatorer kan endast aktivera den här inställningen för sina samlingar.

## SocialSync och Curate {#section_llh_2nh_21b}

Eftersom granskningar är utformade för att lägga till ett numeriskt värde för varje inskickat innehåll stöds inte SocialSync och Curate i granskningarna.

## Granska API:er {#section_xrh_wmh_21b}

Det finns API:er för granskningar så att du kan visa genomsnittlig information om användarbetyg och nedgraderingar samt användargranskningar i andra avsnitt på webbplatsen.

[Omdömen och recensioner](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Med API-slutpunkten för Bootstrap kan din granskning läsas av sökmotorer som Google så att innehåll och nyckelord kan förbättra sökmotoroptimeringen.

* **[!UICONTROL Average User Ratings]** API:t för genomsnittlig användarklassificering hämtar den genomsnittliga användarklassificeringen för en eller flera granskningssamlingar, så att du kan skapa en visualisering av informationen på en indexsida eller lägga till den på en sökindexsida.

* **[!UICONTROL Ratings Breakdown]** API:t för klassificering av klassificeringar hämtar en uppdelning av alla klassificeringar för en specifik granskningssamling och gör att du kan skapa en visualisering som visar antalet granskningar som är associerade med varje stjärngradering.

* **[!UICONTROL User Reviews]** API:t för användargranskningar hämtar de senaste granskningarna för en viss användare. Den här aktiviteten kan användas för att visa en användares recensioner på sidan för den offentliga profilen.
