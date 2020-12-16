---
description: Ändra storlek, bredd och interaktionsalternativ för Media Wall-appen.
seo-description: Ändra storlek, bredd och interaktionsalternativ för Media Wall-appen.
seo-title: Anpassningar av medieväggen
solution: Experience Manager
title: Anpassningar av medieväggen
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# Anpassningar av medieväggen{#media-wall-customizations}

Ändra storlek, bredd och interaktionsalternativ för Media Wall-appen.



Media Walls strömmar bilder och annat innehåll till en social vägg i realtid och visualiserar all aktivitet kring en händelse.

Om det här alternativet är aktiverat kan användare publicera text, bilder eller video direkt i appen. Filtyper som stöds:

* Bild: JPEG, GIF, PNG
* Video: QuickTime/MOV, MP4, MPEG, WebM
* Ljud: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Anger det inledande antalet innehållsobjekt som visas.

* **[!UICONTROL Load content with animation.]** Aktivera det här alternativet om du vill läsa in medieväggen på en sida med animering. Avmarkera det här alternativet om du vill läsa in medieväggen på en sida utan animering.
* **[!UICONTROL Number of columns.]** Ange antalet kolumner för medieväggen. Antalet kolumner är detsamma oavsett storleken på fönstret eller webbläsaren. Om du väljer Auto justeras antalet kolumner så att ett optimerat antal kolumner för skärmstorleken visas.
* **[!UICONTROL Fit content to width]**. När det här alternativet är inaktiverat beskärs innehållet till en kvadrat. Aktivera det här alternativet om du vill visa en hel bild på kortet, oavsett om det fyller hela kortet eller inte.
* **[!UICONTROL Include content modal]**

   Användare kan klicka på ett foto i strömmen för att öppna det i ett överlagrat popup-fönster.

* **[!UICONTROL Require rights]**. Aktivera det här alternativet om du bara vill visa innehåll med statusen Beviljad för behörighet.
* **[!UICONTROL Hide social branding when rights granted]** Aktivera det här alternativet om du vill ta bort logotypen för det ursprungliga sociala medienätverket (Twitter eller Instagram) när rättigheter beviljas för ett visst innehåll.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Välj om du vill tillåta användare att skicka text, foton eller videoklipp med knappen Skicka.
   * **[!UICONTROL Require Media]**. Växla till om du vill att användarna bara ska kunna överföra foto- eller videoinnehåll med knappen Överför.
   * Du kan redigera standardtexten för följande fält för knappen Överför:

      * **[!UICONTROL Upload Button Text]**. Text för knappen Överför. Standardtexten är&quot;What&#39;s in your mind&quot;?
      * **[!UICONTROL Comment Modal Title]**. Titeln för de modala besökarna som använder för att publicera innehåll. Standardtexten är&quot;Skicka din kommentar&quot;.
      * **[!UICONTROL Comment Modal Button]**. Texten som besökarna på knappsajten klickar på för att publicera innehållet. Standardtexten är&quot;Skicka din kommentar&quot;.

* **[!UICONTROL Call-to-action button]** Du kan använda knappen Call-to-action tillsammans med en produktkatalog för att dirigera användare till en produkt eller till din webbplats för ytterligare åtgärder.

   * **[!UICONTROL Call-to-action button]** Växla till om du vill visa knappen Ring till åtgärd.
   * **[!UICONTROL Require rights to display products]** Aktivera det här alternativet om du vill kräva att innehållsägaren har beviljat rättigheter för innehållet innan en Call-to-action-knapp visas för innehållet.

      >[!NOTE]
      >
      >Innehållet visas även om rättigheter inte har beviljats för innehållet, men knappen Call-to-action visas inte med innehållet om inte rättigheter för innehållet har beviljats.

   * **[!UICONTROL Call-to-action header text]** De ord som ska visas i rubriken ovanför knappen Call-to-action i det modala innehållet. Standardordalydelsen är&quot;Handla dessa produkter:&quot;.
   * **[!UICONTROL Call-to-action button text]** De ord som ska visas i knappen Call-to-action i det modala innehållet. Standardtexten är&quot;Köp nu:&quot;.
   * **[!UICONTROL Product display options]** Välj om du vill visa foto- och produktnamnet med knappen Call-to-action.

      >[!NOTE]
      >
      >Både Foto- och produktnamnsknapparna markerar blått när de är aktiverade.

   * **[!UICONTROL Product URL referral tracking]** Växla till om du vill spåra hänvisningar från den här appen till den associerade produktsidan.
   * **[!UICONTROL Referral tracking key-value pairs]** Lägg till parametrar för att ytterligare specificera hänvisningsspårningen från ditt appinnehåll till den associerade produktsidan.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Välj det här alternativet om du vill skapa en app för flera produktsidor. Filtrera produktspecifik UGC till appen för varje produktsida. Du kan markera en eller flera mappar som du vill associera specifika samlingar med appen.
   * **[!UICONTROL Select Product folders]**. Välj de produktmappar på den översta nivån som ska användas för att filtrera UGC. Använd CTRL/Cmd + klicka för att markera flera mappar. Livefyre använder mappen för att avgöra vilka produkter i den mappen som ska visas i appen på olika sidor.
   * **[!UICONTROL Show related content]**. Växla detta för att visa innehåll som publicerats till appen, men som taggats med ett annat produkt-ID. När det produktspecifika innehållet för appen visas visar Livefyre innehåll för andra produkter och innehåll som inte är kopplat till en produkt. Livefyre prioriterar innehållet med samma produkt-ID först, sedan innehåll som publiceras till appen med andra produkt-ID:n och sedan innehåll som publiceras till appen utan produkt-ID:n.

Du kan anpassa medievägg med:

* **[!UICONTROL Style]** och  **[!UICONTROL Config]** alternativ för alla program i  **[!UICONTROL App Designer]**. Mer information om standardalternativen **[!UICONTROL Style]** och **[!UICONTROL Config]** för alla program i **[!UICONTROL App Designer]** finns i Anpassa appar.

* Integreringsverktyg. Se [Integrering av medievägg](/help/implementation/c-app-integrations/c-media-wall-integration.md) för mer information om hur du anpassar en medievägg med integreringsverktyg.

