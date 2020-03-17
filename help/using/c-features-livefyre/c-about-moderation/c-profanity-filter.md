---
description: 'null'
seo-description: 'null'
seo-title: Använda Profanity-filtret
solution: Experience Manager
title: Använda Profanity-filtret
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Använda Profanity-filtret{#using-the-profanity-filter}

Allt innehåll som publiceras i en Livefyre-app genomsöks efter svordomar. Om ett ord som finns med i svordlistan hittas i innehållet eller i användarens visningsnamn, kommer det att flaggas som&quot;Profanity&quot;, vilket gör att du kan filtrera det för att se om det finns en förmoderering, regler, ModQ eller allmänna sökningar i appinnehåll.

>[!NOTE]
>
>Innehållet i Studio Administrator och Managers lyder inte under Profanity Rule Check, och innehåll som publicerats av en moderator kommer inte att flaggas.

Livefyre innehåller en standardsvordlista. Du kan välja att använda den här listan på nätverksnivå, ange en egen lista eller använda en sammanställning av de två. Enskilda webbplatser i ditt nätverk kan ärva nätverkets Profanity List eller använda en lista som är anpassad för att vara platsspecifik.

Om du vill ange en egen anpassad vinstlista som nätverksstandard skickar du den till kontohanteraren för Livefyre.

## Aktivera profilering {#section_yqc_qsk_f1b}

Aktivera och konfigurera vinstfiltret på både nätverks- och webbplatsnivå. Inaktivera avstavningsfiltret på nätverksnivå för att automatiskt inaktivera avstavningsfiltret för alla webbplatser som ärver från nätverket.

>[!NOTE]
>
>Allt innehåll som skickas via Livefyre kontrolleras med rikedom. Om innehåll hittas som innehåller ord som finns i standardsvordlistan eller i din anpassade Profanity-lista, markeras &quot;Profanity&quot;. Om du vill att Livefyre automatiskt ska vidta åtgärder för dessa objekt går du **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL ON]**.

## Aktivera Profanity-filtret för ett nätverk {#section_twd_ssk_f1b}

1. Välj **[!UICONTROL Network]** från menyn för nätverkslistrutor.
1. Gå till **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Rulla ned till **[!UICONTROL Profanity List]** och ange **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL ON]**.

1. Använd **[!UICONTROL Update Network Profanity List]** fältet för att lägga till ord i listan eller klicka på ett ord för att ta bort det från listan.

>[!NOTE]
>
>Om du redigerar Profanity List på nätverksnivå påverkas inte befintliga listor på webbplatsnivå. Om du vill vara säker på att ändringar från nätverket görs på platsen väljer du **[!UICONTROL Restore Network List]** för platsen efter att ändringarna har gjorts.

## Aktivera Profanity-filtret för en webbplats {#section_fld_wsk_f1b}

1. Välj platsen på menyn för nätverkslistrutor.
1. Gå till **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Rulla ned till **[!UICONTROL Profanity List]** och ange **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL ON]**.

1. Välj något av följande alternativ:

   * Om du vill ärva Profanity List från nätverket (detta är inte vanligt) anger du **[!UICONTROL Use Site Profanity List]** till **[!UICONTROL OFF]**.

   * Om du vill redigera egenskapslistan specifikt för webbplatsen ställer du in **[!UICONTROL Use Site Profanity List]** på att **[!UICONTROL On]** öppna **[!UICONTROL Update Profanity List]** fältet där du kan redigera listan:

      * Om du vill ta bort ett ord klickar du på det.
      * Om du vill lägga till ett ord skriver du ordet i **[!UICONTROL Add new word]** rutan och trycker på **[!UICONTROL Return]**.

      * Om du vill se om ett ord finns med i listan skriver du ordet i **[!UICONTROL Test profanity filter]** rutan.
   * Om du vill importera nätverkets egenskapslista igen och använda den på webbplatsen klickar du på **[!UICONTROL Restore Network List]**.
   * Om du vill ta bort allt innehåll från listan och börja från början klickar du på **[!UICONTROL Clear List]**.


## Arbeta med innehåll som innehåller Profanity {#section_epy_dtk_f1b}

Använd Profanity List för att filtrera dina innehållssökningar och för att skapa Premoderation Rules for ModQ.

Om du vill söka efter innehåll som innehåller svordomar går du till **[!UICONTROL Library > App Content]** och **[!UICONTROL Filter by Flags]** markerar **[!UICONTROL Profanity]** kryssrutan. Allt innehåll som har fångats upp av Profanity-filtret för den valda webbplatsen eller det valda nätverket visas. Den här listan kommer att innehålla innehåll som hämtas till appen med SocialSync och Streams.

Om du vill skapa regler för förmoderering väljer du Studio **[!UICONTROL Settings > Network Settings > Moderation]**. När svordomsfiltret har aktiverats visas en ny regel som gör att du kan flagga eller använda förmåttligt innehåll som innehåller svordomar. Som standard aktiveras den här regeln automatiskt **[!UICONTROL Premoderate]** för profilinnehåll, som kan ändras till antingen **[!UICONTROL Trash it]** eller **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Om ett enskilt innehåll omfattas av flera regeltyper (t.ex. både SAFE- och Flag-regler), kommer de striktare reglerna att tillämpas. Till exempel: Om din regel för förmoderering anger att innehållet ska förmåttas, men en SAFE-regel säger att det ska skräpas, kommer det att spärras.

## Visa och uppdatera Profanity-listan för ett nätverk {#section_qdb_btk_f1b}

1. Gå till **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Bläddra ned till **[!UICONTROL Profanity List]** avsnittet.
1. Ange **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL On]** att visa listan som är aktiverad för ditt nätverk (Livefyre som standard eller din överförda anpassade lista) och redigera den. Du kan redigera listan på följande sätt:
   * Om du vill ta bort ett ord klickar du på det.
   * Om du vill lägga till ett ord skriver du ordet i **[!UICONTROL Add new word]** rutan och trycker på **[!UICONTROL Return]**.
   * Om du vill se om ett ord finns med i listan skriver du ordet i **[!UICONTROL Test profanity filter]** rutan.

>[!NOTE]
>
>Endast Studio-administratörer och moderatorer kan redigera favoritlistor.

