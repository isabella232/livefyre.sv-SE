---
description: Ändra storlek, bredd och interaktionsalternativ för Mosaic-appen.
seo-description: Ändra storlek, bredd och interaktionsalternativ för Mosaic-appen.
seo-title: Mosaic-anpassningar
solution: Experience Manager
title: Mosaic-anpassningar
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mosaic-anpassningar{#mosaic-customizations}

Ändra storlek, bredd och interaktionsalternativ för Mosaic-appen.

Alla program använder **[!UICONTROL Style]** och **[!UICONTROL Config]** alternativ i **[!UICONTROL App Designer]**. Mer information om standardprogram **[!UICONTROL Style]** och alternativ **[!UICONTROL Config]** för alla program finns i Anpassa program i **[!UICONTROL App Designer.]**

Du kan anpassa mosaik med följande ytterligare alternativ i App Designer:

* **[!UICONTROL Content interaction]**. Anger det format med vilket nytt innehåll ska läsas in på sidan:

   * **[!UICONTROL Hover Fade]** för att tona till andra sidan av ett kort när en besökare håller muspekaren över innehållet.
   * **[!UICONTROL Hover Flip]** för att vända till den andra sidan av ett kort när en besökare håller muspekaren över innehållet.
   * **[!UICONTROL Click]** för att visa den andra sidan av ett kort när en besökare klickar med musen på innehållet.

* **[!UICONTROL Number of Tiles to Load]**. Antalet plattor som ska läsas in i en mosaik. Detta kan påverka utdatavisningen. Mosaik visas inte i ett rutnät om du inte väljer rätt antal rutor som motsvarar behållarbredden. Du kan behöva justera dessa för att stödrastret ska visas korrekt.
* **[!UICONTROL Hide social branding when rights granted]** Aktivera det här alternativet om du vill ta bort logotypen för det ursprungliga sociala medienätverket (Twitter eller Instagram) när rättigheter beviljas för ett visst innehåll.

* **[!UICONTROL Call-to-action button]** Du kan använda knappen Call-to-action tillsammans med en produktkatalog för att dirigera användare till en produkt eller till din webbplats för ytterligare åtgärder.

   * **[!UICONTROL Call-to-action button]** Växla till om du vill visa knappen Ring till åtgärd.

   * **[!UICONTROL Require rights to display products]** Aktivera det här alternativet om du vill kräva att innehållsägaren har beviljat rättigheter för innehållet innan en Call-to-action-knapp visas för innehållet.

      >[!NOTE]
      >
      >Innehållet visas även om rättigheter inte har beviljats för innehållet, men knappen Call-to-action visas inte med innehållet om inte rättigheter för innehållet har beviljats.

   * **[!UICONTROL Show call-to-action in tile]**. Välj om du vill visa knappen för att ringa upp till åtgärd på en bildbandsplatta i stället för att bara visa knappen för att ringa upp när besökaren klickar på ett kort och öppnar innehållet i ett större fönster.
   * **[!UICONTROL Call-to-action indication text]** Den text som ska visas för att uppmana användaren att klicka på kortet för att öppna modal för att ringa upp.

   * **[!UICONTROL Call-to-action header text]** De ord som ska visas i rubriken ovanför knappen Call-to-action i det modala innehållet. Standardordalydelsen är&quot;Handla dessa produkter:&quot;.

   * **[!UICONTROL Call-to-action button text]** Anpassa texten på knappen Call-to-action. Standardtexten är&quot;Köp nu&quot;.

   * **[!UICONTROL Product display options]** Välj om du vill visa **[!UICONTROL Photo]** och **[!UICONTROL Product name]** med knappen Call-to-action.

   * **[!UICONTROL Product URL referral tracking]** Växla till om du vill spåra hänvisningar från den här appen till den associerade produktsidan.

   * **[!UICONTROL Referral tracking key-value pairs]** Lägg till parametrar för att ytterligare specificera hänvisningsspårningen från ditt appinnehåll till den associerade produktsidan.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Välj det här alternativet om du vill skapa en app för flera produktsidor. Filtrera produktspecifik UGC till appen för varje produktsida. Du kan markera en eller flera mappar som du vill associera specifika samlingar med appen.
   * **[!UICONTROL Select Product folders]**. Välj de produktmappar på den översta nivån som ska användas för att filtrera UGC. Använd CTRL/Cmd + klicka för att markera flera mappar. Livefyre använder mappen för att avgöra vilka produkter i den mappen som ska visas i appen på olika sidor.
   * **[!UICONTROL Show related content]**. Växla detta för att visa innehåll som publicerats till appen, men som taggats med ett annat produkt-ID. När det produktspecifika innehållet för appen visas visar Livefyre innehåll för andra produkter och innehåll som inte är kopplat till en produkt. Livefyre prioriterar innehållet med samma produkt-ID först, sedan innehåll som publiceras till appen med andra produkt-ID:n och sedan innehåll som publiceras till appen utan produkt-ID:n.

Se [Mosaic-alternativ](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) för mer information om hur du anpassar en mosaik med Livefyre.js.
