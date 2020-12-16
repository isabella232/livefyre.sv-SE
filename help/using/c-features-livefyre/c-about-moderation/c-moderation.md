---
description: Livefyre Spam and Abuse Filtering Engine (SAFE) är en bakgrundsprocess som analyserar allt inkommande innehåll och är aktiverad för alla Livefyre-kunder.
seo-description: Livefyre Spam and Abuse Filtering Engine (SAFE) är en bakgrundsprocess som analyserar allt inkommande innehåll och är aktiverad för alla Livefyre-kunder.
seo-title: SAFE-regler
title: SAFE-regler
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 0%

---


# SAFE-regler{#safe-rules}

Livefyre Spam and Abuse Filtering Engine (SAFE) är en bakgrundsprocess som analyserar allt inkommande innehåll och är aktiverad för alla Livefyre-kunder.



SAFE använder mönsterregler och statistiska modeller för att upptäcka skräppost, missbruk, svordomar och massinlägg (repetitiva). Du kommer då och då att se det i andra Livefyre-produkter, särskilt verktygen för innehållmoderering och ModQ.

>[!NOTE]
>
>SAFE är endast engelskt, förutom för massutskick. Kontakta er strategiska kontoansvarige om ni behöver support för andra språk.

## Studio Components using SAFE {#section_k34_4tx_vy}

Flaggor som används av SAFE kan användas med följande Studio-komponenter:

* Regler

   Du kan definiera SAFE-regler för att automatiskt flagga innehåll och definiera hur flaggat innehåll ska hanteras i **[!UICONTROL Network Settings]**.

   En webbplats kan till exempel ange en mycket låg tolerans för Profanity och definiera SAFE-regler som anger att allt innehåll som flaggats som Profane ska vara Bozo’d. Andra webbplatser kan definiera regler som anger att innehållet i Profane ska vara förmodererat innan det går in i strömmen.

* ModQ

   Du kan moderera innehåll som flaggas av SAFE-regler och andra förmodereringsregler (t.ex. SPAM, svordomar osv.) i ModQ.

* Programinnehåll i biblioteket

   Innehåll som flaggas av SAFE visas i listan i appinnehåll på fliken **[!UICONTROL Library]**. Du kan filtrera innehåll efter flaggor för att moderera innehållet.

## Alternativ för SAFE-filter {#section_pg5_ttx_vy}

SAFE använder följande flaggor för filtrerat innehåll och kan användas för att skapa regler och moderera innehåll inifrån Livefyre Studio.

* **[!UICONTROL Profanity List]**: Profilinnehåll, definierat i en lista med engelska nyckelord, baserat på gemensam användning.

   Profanity-filtret söker efter profilspråk baserat på en testad ordlista. Om det upptäcks flaggas innehållet som Profane.

   >[!NOTE]
   >
   >Livefyre har också ett andra Profanity List-filter som du kan anpassa på både plats- och nätverksnivå. Regler som skapas med Profanity List har företräde framför automatiserade regler som härstammar från filtret SAFE Profanity. Mer information finns i avsnittet Profanity List i dokumentationen Settings.

* **[!UICONTROL Mild Profanity]**: Ord och fraser accepteras i allmänhet inte i artiga konversationer, men accepteras vanligtvis i tillfälliga konversationer. I allmänhet är dessa ord och fraser tillåtna på tv-apparater.
* **[!UICONTROL Strong Profanity]**: Mycket starkt språk, t.ex. uttryck och fraser som inte är tillåtna på nätverks-TV och som används sparsamt i R-klassificerade filmer och mogna kabel-TV-program. I allmänhet används dessa ord inte i artiga eller tillfälliga samtal och de sägs i en oartig konversation med avsikt att skada avlyssnaren.
* **[!UICONTROL SPAM]**: Oombedd, vanligen kommersiellt innehåll. Den använder en statistisk modell som bygger på en rad olika funktioner (inklusive kommentarinnehåll och URL:er) för att flagga ett innehåll som SPAM. Du kan justera skräpposttrösklar om du vill anpassa SPAM-taggningsfrekvenser för ditt nätverk eller din webbplats efter begäran.
* **[!UICONTROL Mild Insult]**: Insulterande innehåll, definierat av en lista med nyckelord och frasmönster.
* **[!UICONTROL Strong Insult]**: Insulterande innehåll, definierat av en lista med nyckelord och frasmönster.
* **[!UICONTROL Hate Speech]**: En förolämpning baserad på etnicitet eller religion, särskilt när målgruppstillhörigheten är en minoritet eller skyddad.
* **[!UICONTROL ALL CAPS]**: Text med versaler (läs som stavning).
* **[!UICONTROL Mild Threat]**: Ett hot eller en förolämpning som vanligen innefattar någon form av mild svordomar riktad mot en annan person. Det här alternativet flaggar möjliga hot oftare, men har också en högre falskt positiv frekvens än **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Ett allvarligt hot eller en förolämpning som omnämns att ett eller flera personer skadas av handlingar, ofta med stark svordom. Det här alternativet flaggar potentiella hot mindre ofta, men har också en lägre falskt positiv frekvens än **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: En bild som kan ha nakenhet. Det här alternativet flaggar nudity mindre ofta, men har också en lägre falskt positiv frekvens än **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: En bild som kan ha nakenhet. Det här alternativet flaggar nudity oftare, men har också en högre falskt positiv frekvens än **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Personligt identifierbar information): Information som kan identifiera användaren. Detta kan innefatta en e-postadress, fysisk adress, personnummer, personnummer (för amerikanska kunder), kreditkortsnummer, lösenord eller annat som kan användas i bedrägeri eller för att få någons identitet.
* **[!UICONTROL Livefyre Recommends Trash]**. Ange vilken åtgärd som systemet ska utföra när den automatiska modereringsrekommendationen identifierar innehåll som ska refuseras.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Om du vill aktivera Recommendations för moderering kontaktar du supportpersonalen på Adobe Livefyre.

## Hantera innehåll som inte fångas upp av SAFE {#section_pjy_5tx_vy}

Det finns flera sätt att effektivt hantera innehåll som inte fångas upp av det här filtret. Alternativen nedan visas i den rekommenderade processordningen.

1. Som moderator tar du bort innehållet från strömmen.
1. Skapa en flaggregel som anger om ett innehåll flaggas som skräppost eller stötande av fem användare, och ange det som Bozo.
1. Förbjud den användare som publicerar oönskat innehåll så att allt innehåll hamnar direkt i Bozo-läget.
1. Lägg till specifika ord som alltid ska filtreras i din svordlista.

>[!NOTE]
>
>Om en moderator publicerar innehåll som fångas upp av vårt skräppostfilter flaggas det fortfarande som skräppost, men godkänns automatiskt och kommer inte att anges till Bozo.

Om du märker trender eller mönster för innehåll som inte fångas upp av SAFE skickar du e-post till CSM:erna med kommentar-ID:n och text.



Program som använder den här funktionen:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chatt](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskort](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Karta](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Knappen Överför](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

