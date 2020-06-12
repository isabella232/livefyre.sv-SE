---
description: Moderera innehåll från ett enda intelligent gränssnitt.
seo-description: Moderera innehåll från ett enda intelligent gränssnitt.
seo-title: Moderera innehåll med hjälp av ModQ
title: Moderera innehåll med hjälp av ModQ
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# Moderera innehåll med hjälp av ModQ{#moderate-content-using-modq}

Moderera innehåll från ett enda intelligent gränssnitt.

ModQ skapar en realtidskö med allt innehåll på webbplatsen eller i nätverket som matchar de förmodereringsregler du har definierat, vilket gör att moderatorerna bara kan fokusera på innehåll som kräver deras uppmärksamhet.

När du har definierat ModQ-inställningarna läggs nytt innehåll till i strömmen, eller befintligt innehåll som flaggats av dina användare, till i kön. Ändringar av reglerna tar inte bort innehåll från ModQ, men lägger till nytt innehåll i kön enligt dina nya inställningar.

Med ModQ kan du:

* Moderera i sitt sammanhang, visa hela trådar och Godkänn, Skräp eller Bozo antingen enskilda innehållsdelar eller hela trådar med ett klick.
* Snabbare och effektivare arbetsflöde.
* Svara på innehåll och öka engagemanget i communityn.
* Möjliggör för flera moderatorer att arbeta igenom materialet utan att behöva duplicera varandras arbete.

Livefyre-innehåll listas i ModQ i upp till 6 veckor, och förmodererat ströminnehåll som inte har adresserats listas i ModQ i 90 dagar.

>[!NOTE]
>
>En enstaka del av innehållet kan listas flera gånger om det matchar flera regler för att inkluderas i ModQ. Om till exempel en del av innehållet utlöser en användarflaggregel för offensiv och sedan utlöser en annan regel för Profane, listas den två gånger i ModQ.

Innehåll som inte visas i ModQ inkluderar:

* Spärrat innehåll.
* Innehåll som godkänts av en moderator.
* Innehåll som publicerats av en förbjuden användare eller användarflaggor som används av en bannlyst användare.

## Navigeringsmetod {#section_uv4_db2_yy}

ModQ delas upp i två flikpaneler:

* **[!UICONTROL Items]** listar allt innehåll som är inbyggt i Livefyre och SocialSync och som är inriktat på moderering. Den här fliken innehåller allt innehåll i sociala sökningar eller strömmar som har flaggats eller redigerats efter moderering.
* **[!UICONTROL Streams Premoderation]** listar allt innehåll som matas in i dina appar från strömmar med inställningen Förmåttlig aktiverad. (Mer information finns i Skapa strömmar.)

Båda flikarna har många av samma filter och modereringsverktyg.

* **[!UICONTROL Item Count]** Antalet återstående objekt i kön visas i det övre vänstra hörnet av ModQ.
* **[!UICONTROL Filter]** Klicka **[!UICONTROL Filter]** för att definiera parametrar som innehållet ska listas med i rutan.
* **[!UICONTROL History]** Klicka på **[!UICONTROL History]** knappen längst upp till höger på skärmen för att öppna en lista över nyligen modererat innehåll, så att du kan granska ditt arbete eller ändra en modereringsåtgärd som du nyligen har utfört. Klicka på knappen igen för att återgå till det köade innehållet. Endast de 100 senaste åtgärderna visas. **Historik** visar inte åtgärder som har vidtagits av en annan moderator.

* **[!UICONTROL User Pane]** Klicka på knapparna för att expandera eller komprimera längst upp till höger på sidan för att öppna eller stänga användarrutan.

## Förstå ModQ-innehåll {#section_oxm_kgz_y1b}

Varje listad del av innehållet visar förhandsgranskningsinformation, inklusive den webbplats där det publicerades och dess författare. Om du markerar ett objekt visas hela innehållet, inklusive alla medier.

>[!NOTE]
>
>Innehåll som är inbyggt i Livefyre visar mer information än innehåll som läggs till i appen via strömmar eller andra sociala mediekällor.

Följande information visas när du markerar ett objekt:

* **[!UICONTROL Time in Queue:]** anger hur lång tid som innehållet lades till i ModQ.
* **[!UICONTROL App name:]** appen där innehållet visas. Länkar till webbplatsen med appen.
* **[!UICONTROL Content Body:]** text och miniatyrbilder, om sådana finns.
* **[!UICONTROL Status:]** innehållets aktuella läge (Väntande, Streckat och så vidare).
* **[!UICONTROL Author information:]** författarens namn och användarnamn.
* **[!UICONTROL Timestamp:]** den relativa tidsstämpeln för när innehållet skapades. Permalinks to the piece of content in Studio’s App Content page.
* **[!UICONTROL Flag Type:]** Stötande, oense, skräppost osv.

   * SAFE-flaggor: Spam and Bulk.
   * Flagga som används av din lista över nätverks- och webbplatsprofiler: Profanity.
   * Flaggor som används av SAFE: Hate-tal, PII (personligt identifierbar information), Insult och Profanity.
   * Användarflaggor: Spam, Offtopic, Offensive och Disagree.

* **[!UICONTROL Flag origin:]** flaggans källa. Kan vara SAFE, ett användarnamn eller Livefyre.
* **[!UICONTROL More info:]** innehåller information om innehållet, inklusive antalet gilla-markeringar, användarflaggor, svar och eventuella taggar som har tillämpats på innehållet. När du klickar på Webbplats öppnas den översta sidan på den webbplats där innehållet finns. När du klickar på tidsstämpeln öppnas en kopplad vy av innehållet i kontexten på sidan.

## Filteralternativ i ModQ {#section_r2c_qc2_yy}

Klicka **[!UICONTROL Filter]** i det övre vänstra hörnet av ModQ-fönstret för att öppna en panel med tillgängliga filteralternativ för listat innehåll. När du väljer alternativ uppdateras ModQ automatiskt så att endast det filtrerade innehållet visas. Klicka **[!UICONTROL Clear filters]** för att rensa alla valda alternativ och läsa in den fullständiga listan med objekt igen.

Olika filteralternativ är tillgängliga för **[!UICONTROL Items]** - och **[!UICONTROL Streams Premoderation]** flikarna.

Följande alternativ är tillgängliga för ModQ under både **[!UICONTROL Items]** och **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Använd fältet Sök i appar för att filtrera resultat efter program. Flera appar kan väljas.
* **[!UICONTROL System Flags]**. Filtrera innehåll efter regler som Spam, Profanity, SAFE och Premoderation.

   * Om du väljer **[!UICONTROL Spam]** det här alternativet visas allt innehåll som taggats som skräppost av SAFE.
   * Om du väljer **[!UICONTROL Profanity]** det här alternativet visas allt innehåll som taggats med Profane i nätverks- eller webbplatsprofillistan.
   * Om du väljer **[!UICONTROL SAFE]** det här alternativet visas allt innehåll i ModQ som ett resultat av dina SAFE-regler.
   * Om du väljer **[!UICONTROL Premoderation]** det här alternativet visas allt innehåll som taggats för förmoderering av nätverket, strömmen eller appinställningarna.

* **[!UICONTROL User Flags]** Filtrera innehåll efter användarflaggor. Alternativen är Offensiv, Spam, Offtopic och Disagree.
* **[!UICONTROL Rights Requests.]** Visa endast innehåll med behörighet genom att klicka i kryssrutan.
* **[!UICONTROL Entered the queue.]** Filtrera innehåll efter den tidsram som innehållet skickades till ModQ. Den tid som innehållet skickades till ModQ är inte nödvändigtvis den tid då innehållet publicerades i appen.

Följande alternativ finns för ModQ under **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtrera innehåll efter den sociala källan som innehållet kommer från. Alternativ för sociala källor är till exempel Twitter, Instagram, Facebook och RSS.

Följande alternativ finns för ModQ under **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtrera innehåll efter den rekommendation som ges av den automatiska modereringsrekommendationen.

Följande bilder visar hur modereringsrekommendationer ser ut i ModQ:  ![](assets/mod_reco1.png)

Rekommendationen om moderering ges för innehåll när det är konfigurerat i **[!UICONTROL Network Settings > Moderation]** och **[!UICONTROL Network Settings > ModQ]**.

## Åtgärder som du kan använda i ModQ {#section_h4g_wrn_z1b}

Du kan bestämma vad du ska göra med varje del av innehållet i ModQ.

Välj något av följande alternativ:

* Ikonen som **[!UICONTROL Checkbox]** används för att godkänna innehållet
* Ikonen som **[!UICONTROL Trash can]** används för att skicka innehåll till papperskorgen
* **[!UICONTROL Request Rights]** om du vill begära rättigheter till innehållet från innehållsägaren.

   >[!NOTE]
   >
   >Du kan inte begära rättigheter i ModQ för innehåll från Instagram. Du måste använda biblioteket eller appinnehållet för att skicka rättighetsbegäranden för innehåll från Instagram.

* **[!UICONTROL Feature and Approve]** för att godkänna innehållet och även innehålla innehållet.
* **[!UICONTROL Product Tag and Approve]** om du vill lägga till en produkt från din produktkatalog i innehållet och sedan godkänna den.
* **[!UICONTROL Mark as Pending]** för att markera innehållet som väntande.

>[!NOTE]
>
>När du har papperskorgen tas innehållet och alla svar på innehållet bort permanent från ModQ. Mer information om hur du lägger till en trasig del av innehåll i en app finns i [Lägga tillbaka ett trash-objekt i en app](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Om innehållet redan är i önskat läge kan du välja Papperskorgen, Bozo eller Godkänn för att bekräfta läget och ta bort objektet från listan. När du modererar ett innehåll tas det omedelbart bort från kön och inaktiveras i andra moderatorköer.

>[!NOTE]
>
>Ströminnehållet får inte vara Bozo’d. Om du spårar direktuppspelat innehåll tas det bort permanent från direktuppspelningen och kan inte ångras.

När innehållet har modererats tas det bort från moderatorns ModQ och författaren kan inte längre redigera det inifrån strömmen. Om en moderator stänger ett objekt, eller om en användare tar bort sin kommentar, visas det som nedtonat i andra moderatorköer i realtid. När innehåll har nedtonats visas knappen på sidan så att moderatorerna kan ta bort det från sina listor och behålla sin plats på sidan oavsett annan moderatoraktivitet. **[!UICONTROL Clear Moderated]**

## Använda papperskorgsfunktionen i ModQ {#section_tpx_qgz_y1b}

Använd inställningsavsnittet för att välja alternativ som är tillgängliga när innehåll markeras som Streckat.

* ****[!UICONTROL Confirm Trash]**** Aktivera det här alternativet om du vill att moderatorerna ska bekräfta sin åtgärd när de anger innehåll som Papperskorgen. När det här alternativet är aktiverat visas en dialogruta där du uppmanas att ange ett innehåll **[!UICONTROL Trash]** och ett fält där ett **[!UICONTROL Reason for Moderation]****[!UICONTROL Note]** fält kan anges.

   (Den här inställningen är tillgänglig **[!UICONTROL only]** på nätverksnivå och gäller för alla webbplatser i nätverket.)

* ****[!UICONTROL Hide Replies]**** Aktivera det här alternativet om du vill att svar automatiskt ska skräpas när en överordnad kommentar stryps eller Bozo’d.

## Ändra användarstatus i ModQ {#section_tmw_lg1_z1b}

Klicka på **[!UICONTROL User actions]** knappen på panelen Användarsammanfattning för att stänga av, hindra eller tillåta-lista användaren.

* **[!UICONTROL Mute:]** gör att du kan stänga av flaggor från den användare som flaggar det listade innehållet. Använd det här alternativet om du vill exkludera användarens flaggor från dina förmodereringsfilter. Innehåll som de flaggar kommer inte att ange ModQ som ett resultat av flaggan, och flaggorna inkluderas inte i flaggreglerna.
* **[!UICONTROL Ban:]** kan du förbjuda den listade användaren från din plats eller ditt nätverk. (Endast Studio-administratörer eller användarhanterare får förbjuda nätverk av användare.)
* **[!UICONTROL Whitelist:]** gör att du kan tillåta listning av den listade användaren för din plats eller ditt nätverk. (Endast Studio-administratörer eller användarhanterare får nätverka för att tillåta att en användare listas.)



Appar som använder ModQ:

* [Chatt](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Knappen Överför](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

