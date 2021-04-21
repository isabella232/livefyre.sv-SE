---
description: Ändra storlek, bredd och interaktionsalternativ för appen Karta.
title: Anpassningar av funktionskort
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Anpassningar av funktionskort{#feature-card-customizations}

Ändra storlek, bredd och interaktionsalternativ för appen Karta.

<!-- 
r_feature_card_customization.dita
 -->

Kortapparna innehåller endast standardanpassningar:** [!UICONTROL Theme]**, Märkesfärg, Teckensnittsfamilj och Teckensnittsstorlek.

Du kan anpassa funktionskort med:

* **[!UICONTROL Style]** och  **[!UICONTROL Config]** alternativ för alla program i  **[!UICONTROL App Designer]**. Mer information om standardalternativen **[!UICONTROL Style]** och **[!UICONTROL Config]** för alla program i **[!UICONTROL App Designer]** finns i Anpassa appar.

* Integreringsverktyg. Mer information om hur du anpassar program med integreringsverktyg finns i Programintegreringar.
* **[!UICONTROL Call-to-action button]** Du kan använda knappen Call-to-action tillsammans med en produktkatalog för att dirigera användare till en produkt eller till din webbplats för ytterligare åtgärder.

   * **[!UICONTROL Call-to-action button]** Växla till om du vill visa knappen Ring till åtgärd.
   * **[!UICONTROL Require rights to display products]** Aktivera det här alternativet om du vill kräva att innehållsägaren har beviljat rättigheter för innehållet innan en Call-to-action-knapp visas för innehållet.

      >[!NOTE]
      >
      >Innehållet visas även om rättigheter inte har beviljats för innehållet, men knappen Call-to-action visas inte med innehållet om inte rättigheter för innehållet har beviljats.

   * **[!UICONTROL Call-to-action header text]** De ord som ska visas i rubriken ovanför knappen Call-to-action i det modala innehållet. Standardordalydelsen är&quot;Handla dessa produkter:&quot;.
   * **[!UICONTROL Call-to-action button text]** Anpassa texten på knappen Call-to-action. Standardtexten är&quot;Köp nu&quot;.
   * **[!UICONTROL Product display options]** Välj om du vill visa  **[!UICONTROL Photo]** och  **[!UICONTROL Product name]** med knappen Call-to-action.
   * **[!UICONTROL Product URL referral tracking]** Växla till om du vill spåra hänvisningar från den här appen till den associerade produktsidan.
   * **[!UICONTROL Referral tracking key-value pairs]** Lägg till parametrar för att ytterligare specificera hänvisningsspårningen från ditt appinnehåll till den associerade produktsidan.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Välj det här alternativet om du vill skapa en app för flera produktsidor. Filtrera produktspecifik UGC till appen för varje produktsida. Du kan markera en eller flera mappar som du vill associera specifika samlingar med appen.
   * **[!UICONTROL Select Product folders]**. Välj de produktmappar på den översta nivån som ska användas för att filtrera UGC. Använd `CTRL/Command + click` för att markera mer än en mapp. Livefyre använder mappen för att avgöra vilka produkter i den mappen som ska visas i appen på olika sidor.
   * **[!UICONTROL Show related content]**. Växla detta för att visa innehåll som publicerats till appen, men som taggats med ett annat produkt-ID. När det produktspecifika innehållet för appen visas visar Livefyre innehåll för andra produkter och innehåll som inte är kopplat till en produkt. Livefyre prioriterar innehållet med samma produkt-ID först, sedan innehåll som publiceras till appen med andra produkt-ID:n och sedan innehåll som publiceras till appen utan produkt-ID:n.
