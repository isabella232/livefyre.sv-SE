---
description: Bildbandet är en visualiseringsapp som visar användargenererat innehåll i ett dynamiskt enda vågrätt band med foton, som liknar en filmremsa från en kamera.
seo-description: Bildbandet är en visualiseringsapp som visar användargenererat innehåll i ett dynamiskt enda vågrätt band med foton, som liknar en filmremsa från en kamera.
seo-title: Bildband
solution: Experience Manager
title: Bildband
uuid: 2e3cb6f4-15db-4509-8a5b-a651511cdbd6
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---


# Bildband{#filmstrip}

Bildbandet är en visualiseringsapp som visar användargenererat innehåll i ett dynamiskt enda vågrätt band med foton, som liknar en filmremsa från en kamera.

## Om bildbandet {#section_tng_slj_yy}

Du kan använda bildbandet med UGC i e-handelsscenarier, till exempel produktsidor eller transaktionswebbplatser. Slutanvändare kan navigera på bildbandet genom att klicka på sidopilarna för att bläddra igenom det tillgängliga innehållet från vänster till höger. Nytt innehåll visas till vänster när det kommer in i appen. Du kan välja om den nya UGC-direktuppspelningen ska ha en etikett som säger *New* för att hjälpa besökarna att snabbt identifiera nytt innehåll.

Du kan välja om besökarna på webbplatsen ska kunna se en knapp för att ringa upp och hålla muspekaren över knappen för att se en förhandsgranskning av produkter som ska säljas. Du kan välja att associera produkter från produktkatalogen med innehåll på bildbandet. Besökare på mobiler och icke-mobilsajter kan klicka på ett kort för att visa en större bild, dela innehåll, spela upp video eller visa tillhörande produkter och en knapp för att ringa in när de ska köpa objekten.

## Vilken typ av innehåll kan jag publicera på bildbandet? {#section_b5h_qlj_yy}

Innehåll som stöds:

* Foton
* Videor
* Ljud

Innehållskällor som stöds:

* Twitter
* Instagram
* Facebook
* YouTube
* RSS
* Tumblr
* Livefyre

Det går inte att publicera innehåll som bara innehåller text på en bildband. Du kan bara publicera text om den ingår i ett foto- eller videoklipp.

## Hur ser en besökare på en webbplats innehåll på bildbandet? {#section_w5c_plj_yy}

En besökare på en webbplats ser innehåll som fyllts i på en bildband från Studio från en Studio-ström, ett bibliotek eller en social sökning. Om nytt innehåll publiceras i appen medan en besökare finns på sidan, visas det nya innehållet till vänster och det gamla innehållet till höger i realtid utan att någon besökare behöver uppdatera sin sida. Om du väljer att meddela besökaren om nytt innehåll visas ett meddelande som säger&quot;ny&quot; och en pil som pekar åt vänster för att visa nytt innehåll.

## Vad händer när en besökare klickar på ett objekt på bildbandet? {#section_cvz_nlj_yy}

På en dator eller mobil enhet klickar du på ett kort för att dela innehåll, visa en större bild, titta på en video, se flera medieobjekt eller visa tillhörande produkter taggade i användargenerationen.

På en dator för du muspekaren över knappen för att ringa upp och visa produkter som är kopplade till innehållet.

## Kan en besökare dela innehåll från en bildband? {#section_zzz_mlj_yy}

Ja. En besökare kan dela alla innehållstyper på bildbandet. På en dator eller mobil enhet klickar du på ett kort för att öppna det och sedan på delningsikonen.

## Hur läggs nytt innehåll till på bildbandet? {#section_f4w_klj_yy}

Lägg till innehåll på en bildband genom att:

* Publicera manuellt från biblioteket, appinnehållet eller ModQ.
* Konfigurera en ström som ska publiceras automatiskt.

Nytt innehåll strömmas automatiskt till bildbandsappen till vänster och flyttar det gamla innehållet till höger i realtid utan att någon besökare behöver uppdatera sidan. Om du väljer att meddela besökaren om nytt innehåll visas ett meddelande som säger&quot;nytt&quot; och en pil som pekar åt vänster för att visa nytt innehåll om de vill se det nya innehållet.

## Hur visas innehåll som bara innehåller text i appen? {#section_h31_klj_yy}

Bildbandet visar inte innehåll som bara innehåller text. På bildbandet visas endast bilder och videoklipp.

## Varför visas inte en del av mitt innehåll på min webbplats trots att innehållet visas i Studio? {#section_upr_hlj_yy}

På bildbandet visas innehållet i en vågrät remsa på fem som standard. Antalet plattor beror på storleken på den behållare som appen visas i och den plattstorlek som du väljer i appdesignern. Livefyre rekommenderar att du lägger till minst fem till tio innehållsdelar i din bildbandsapp för att tillhandahålla ett tillräckligt antal plattor med innehåll och låta användarna bläddra igenom för att hitta fler.

Ibland visas inte innehållet eftersom du har aktiverat **[!UICONTROL Require rights]**. Om du aktiverar detta måste du ha behörighet för allt innehåll i appen. Om rättighetsstatusen inte&quot;beviljas&quot; för ett visst innehåll visas det inte i appen.

## Hur vet en besökare när en ny produkt läggs till? {#section_ttt_xps_mbb}

Du kan välja att lägga till meddelanden om nytt innehåll när det läggs till genom att växla **[!UICONTROL Show Notifications]** till **[!UICONTROL On]**.

## Skapa bildband med Studio {#section_dwb_glj_yy}

Du skapar alla program i Livefyre Studio på samma sätt. Mer information om hur du skapar en bildbandsapp i Studio med standardprocessen finns i Skapa appar.