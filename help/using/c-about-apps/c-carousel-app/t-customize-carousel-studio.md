---
description: Ändra storlek, bredd och interaktionsalternativ för Carousel-appen.
seo-description: Ändra storlek, bredd och interaktionsalternativ för Carousel-appen.
seo-title: Anpassa en Carousel med Studio
solution: Experience Manager
title: Anpassa en Carousel med Studio
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Anpassa en Carousel med Studio{#customize-a-carousel-using-studio}

Ändra storlek, bredd och interaktionsalternativ för Carousel-appen.

Alla program använder **[!UICONTROL Style]** och **[!UICONTROL Config]** alternativ i **[!UICONTROL App Designer]**. Mer information om standardprogram **[!UICONTROL Style]** och alternativ för alla program i finns i Anpassa program **[!UICONTROL Config]** **[!UICONTROL App Designer]**.

Du kan anpassa en Carousel med följande ytterligare alternativ i App Designer:

* **[!UICONTROL Max Number of Items]**

   Anger antalet objekt som ska visas i Carousel. Standardvärdet är 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Endast för datorskärmar

   * Om innehållet är större än 600 pixlar visas vågrätt
   * Om innehållet är mindre än 600 pixlar visas lodrätt
   * **Lodrätt.** För datorskärmar eller mobila enheter. På mobila enheter krymps kortet så att det passar skärmstorleken.

* **[!UICONTROL Call-to-action button]** Du kan använda knappen Call-to-action tillsammans med en produktkatalog för att dirigera användare till en produkt eller till din webbplats för ytterligare åtgärder.

   * **[!UICONTROL Call-to-action button]** Växla till om du vill visa knappen för att ringa till åtgärd.
   * **[!UICONTROL Require rights to display products]** Aktivera det här alternativet om du vill kräva att innehållsägaren har beviljat rättigheter för innehållet innan en knapp för att ringa upp visas för innehållet.
   >[!NOTE]
   >
   >Innehållet visas även om rättigheter inte har beviljats för innehållet, men knappen för att ringa upp till åtgärd visas inte med innehållet om inte rättigheter för innehållet har beviljats.

   * **[!UICONTROL Show call-to-action in tile]**. Välj om du vill visa knappen för att ringa upp till åtgärd på en platta i stället för att bara visa knappen för att ringa upp när besökaren klickar på ett kort och öppnar innehållet i ett större fönster.
   * **[!UICONTROL Call-to-action indication text]** Den text som ska visas för att uppmana användaren att klicka på kortet för att öppna modalt anrop till åtgärd.
   * **[!UICONTROL Call-to-action header text]** De ord som ska visas i rubriken ovanför knappen Call-to-action i det modala innehållet. Standardtexten är&quot;Handla dessa produkter:&quot;.
   * **[!UICONTROL Call-to-action button text]** De ord som ska visas i knappen Call-to-action i det modala innehållet. Standardtexten är&quot;Köp nu:&quot;.
   * **[!UICONTROL Product display options]** Välj om du vill visa **[!UICONTROL Photo]** och **[!UICONTROL Product name]** med knappen Call-to-action.
   >[!NOTE]
   >
   >Både Foto- och produktnamnsknapparna markerar blått när de är aktiverade.

   * **[!UICONTROL Product URL referral tracking]** Växla till om du vill spåra hänvisningar från den här appen till den associerade produktsidan.
   * **[!UICONTROL Referral tracking key-value pairs]** Lägg till parametrar för att ytterligare specificera hänvisningsspårningen från ditt appinnehåll till den associerade produktsidan.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Välj det här alternativet om du vill skapa en app för flera produktsidor. Filtrera produktspecifik UGC till appen för varje produktsida. Du kan markera en eller flera mappar som du vill associera specifika samlingar med appen.
   * **[!UICONTROL Select Product folders]**. Välj de produktmappar på den översta nivån som ska användas för att filtrera UGC. Använd CTRL/Cmd + klicka för att markera flera mappar. Livefyre använder mappen för att avgöra vilka produkter i den mappen som ska visas i appen på olika sidor.
   * **[!UICONTROL Show related content]**. Växla detta för att visa innehåll som publicerats till appen, men som taggats med ett annat produkt-ID. När det produktspecifika innehållet för appen visas visar Livefyre innehåll för andra produkter och innehåll som inte är kopplat till en produkt. Livefyre prioriterar innehållet med samma produkt-ID först, sedan innehåll som publiceras till appen med andra produkt-ID:n och sedan innehåll som publiceras till appen utan produkt-ID:n.
