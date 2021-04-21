---
title: Använda Profanity-filtret
description: Använda Profanity-filtret
exl-id: 6ea7d913-f562-42a5-a6ea-241aa4e1089a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Använda Profanity-filtret{#using-the-profanity-filter}

Allt innehåll som publiceras i en Livefyre-app genomsöks efter svordomar. Om ett ord som finns med i svordlistan hittas i innehållet eller i användarens visningsnamn, kommer det att flaggas som&quot;Profanity&quot;, vilket gör att du kan filtrera det för att se om det finns en förmoderering, regler, ModQ eller allmänna sökningar i appinnehåll.

>[!NOTE]
>
>Innehållet i Studio Administrator och Managers lyder inte under Profanity Rule Check, och innehåll som publicerats av en moderator kommer inte att flaggas.

Livefyre innehåller en standardsvordlista. Du kan välja att använda den här listan på nätverksnivå, ange en egen lista eller använda en sammanställning av de två. Enskilda webbplatser i ditt nätverk kan ärva nätverkets Profanity List eller använda en lista som är anpassad för att vara platsspecifik.

Om du vill ange en egen anpassad vinstlista som nätverksstandard skickar du den till kontohanteraren för Livefyre.

## Aktivera profilfiltrering {#section_yqc_qsk_f1b}

Aktivera och konfigurera vinstfiltret på både nätverks- och webbplatsnivå. Inaktivera avstavningsfiltret på nätverksnivå för att automatiskt inaktivera avstavningsfiltret för alla webbplatser som ärver från nätverket.

>[!NOTE]
>
>Allt innehåll som skickas via Livefyre kontrolleras med rikedom. Om innehåll hittas som innehåller ord som finns i standardsvordlistan eller i din anpassade Profanity-lista, markeras &quot;Profanity&quot;. Om du vill att Livefyre automatiskt ska vidta åtgärder för dessa objekt aktiverar du **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL ON]**.

## Aktivera Profanity-filtret för ett nätverk {#section_twd_ssk_f1b}

1. Välj **[!UICONTROL Network]** på nätverkets listruta.
1. Gå till **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Rulla ned till **[!UICONTROL Profanity List]** och ställ in **[!UICONTROL Enable Profanity Checking]** på **[!UICONTROL ON]**.

1. Använd fältet **[!UICONTROL Update Network Profanity List]** för att lägga till ord i listan eller klicka på ett ord för att ta bort det från listan.

>[!NOTE]
>
>Om du redigerar Profanity List på nätverksnivå påverkas inte befintliga listor på webbplatsnivå. Om du vill vara säker på att ändringar från nätverket görs på platsen väljer du **[!UICONTROL Restore Network List]** för platsen när ändringarna har gjorts.

## Aktivera Profanity-filtret för en webbplats {#section_fld_wsk_f1b}

1. Välj platsen på menyn för nätverkslistrutor.
1. Gå till **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Rulla ned till **[!UICONTROL Profanity List]** och ställ in **[!UICONTROL Enable Profanity Checking]** på **[!UICONTROL ON]**.

1. Välj något av följande alternativ:

   * Om du vill ärva Profanity List från nätverket (detta är inte vanligt) anger du **[!UICONTROL Use Site Profanity List]** till **[!UICONTROL OFF]**.

   * Om du vill redigera egenskapslistan specifikt för webbplatsen anger du **[!UICONTROL Use Site Profanity List]** till **[!UICONTROL On]** för att öppna fältet **[!UICONTROL Update Profanity List]** där du kan redigera listan:

      * Om du vill ta bort ett ord klickar du på det.
      * Om du vill lägga till ett ord skriver du ordet i rutan **[!UICONTROL Add new word]** och trycker på **[!UICONTROL Return]**.

      * Om du vill se om ett ord finns med i listan skriver du ordet i rutan **[!UICONTROL Test profanity filter]**.
   * Klicka på **[!UICONTROL Restore Network List]** om du vill importera nätverkets Profanity List igen och använda den på webbplatsen.
   * Om du vill ta bort allt innehåll från listan och börja från början klickar du på **[!UICONTROL Clear List]**.


## Arbeta med innehåll som innehåller Profanity {#section_epy_dtk_f1b}

Använd Profanity List för att filtrera dina innehållssökningar och för att skapa Premoderation Rules for ModQ.

Om du vill söka efter innehåll som innehåller svordomar går du till **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** och markerar kryssrutan **[!UICONTROL Profanity]**. Allt innehåll som har fångats upp av Profanity-filtret för den valda webbplatsen eller det valda nätverket visas. Den här listan kommer att innehålla innehåll som hämtas till appen med SocialSync och Streams.

Välj **[!UICONTROL Settings > Network Settings > Moderation]** från Studio om du vill skapa regler för förmoderering. När svordomsfiltret har aktiverats visas en ny regel som gör att du kan flagga eller använda förmåttligt innehåll som innehåller svordomar. Som standard aktiverar den här regeln automatiskt **[!UICONTROL Premoderate]** för profilinnehåll, som kan ändras till antingen **[!UICONTROL Trash it]** eller **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Om ett enskilt innehåll omfattas av flera regeltyper (t.ex. både SAFE- och Flag-regler), kommer de striktare reglerna att tillämpas. Till exempel: Om din regel för förmoderering anger att innehållet ska förmåttas, men en SAFE-regel säger att det ska skräpas, kommer det att spärras.

## Visa och uppdatera Profanity-listan för ett nätverk {#section_qdb_btk_f1b}

1. Gå till **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Bläddra ned till avsnittet **[!UICONTROL Profanity List]**.
1. Ange **[!UICONTROL Enable Profanity Checking]** till **[!UICONTROL On]** om du vill visa listan som är aktiverad för ditt nätverk (Livefyre-standard eller din överförda anpassade lista) och redigera den. Du kan redigera listan på följande sätt:
   * Om du vill ta bort ett ord klickar du på det.
   * Om du vill lägga till ett ord skriver du ordet i rutan **[!UICONTROL Add new word]** och trycker på **[!UICONTROL Return]**.
   * Om du vill se om ett ord finns med i listan skriver du ordet i rutan **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Endast Studio-administratörer och moderatorer kan redigera favoritlistor.
