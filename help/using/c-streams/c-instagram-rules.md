---
description: Du kan skapa strömregler som hämtar innehåll från Instagram.
title: Instagram Rules
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Instagram Rules{#instagram-rules}

Du kan skapa strömregler som hämtar innehåll från Instagram.

>[!NOTE]
>
>Innan du skapar en Instagram-ström måste du lägga till minst ett Instagram-företagskonto i **[!UICONTROL Social Accounts]**-avsnittet i **[!UICONTROL Network Settings]**. Mer information om hur du konfigurerar ett Instagram-konto finns i [Om Instagram-konton](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Skapa Instagram-regler baserat på @mentions eller hashtag.

>[!NOTE]
>
>Alla Instagram-regler kräver minst en hashtagg. Om du lägger till nyckelord och ett användarnamn för regeln returneras innehåll som innehåller båda posterna.

Om du vill skapa Instagram-regler för att hämta innehåll från Instagram-flöden till din app eller mapp, filtrera efter:

* **[!UICONTROL Words]**

   * Ange **[!UICONTROL hashtags]** som ska inkluderas i eller exkluderas från din Instagram-ström. Om du anger värden för både **[!UICONTROL Contains]**- och **[!UICONTROL Does not contain]**-fälten returneras bilder som innehåller den första och inte den andra.

   * Om du till exempel anger nyckelorden **[!UICONTROL Contains]** Giants, Posey och **[!UICONTROL Does not contain]** för nyckelordet Dodger, returneras alla inlägg som innehåller ordet Giants eller Posey, och ordet Dodger tas inte med.

      >[!NOTE]
      >
      >Instagram Rules returnerar inlägg som innehåller den listade hashtaggen i författarens kommentarer, som kanske inte visas i strömmen.

* **[!UICONTROL Mentions]**

   * Ange **[!UICONTROL @mentions]** för att hämta till strömmen eller exkludera från strömmen.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Du måste ha ett Instagram-företagskonto konfigurerat i Livefyre för att kunna använda författarsökningen i en Instagram Stream-regel. Mer information om hur du konfigurerar Instagram-företagskonton i Livefyre finns i [Om Instagram-konton](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Ange **[!UICONTROL @usernames]** för att hämta till strömmen. Kontot som är associerat med **@username** måste vara ett Instagram-företagskonto.

   * Ange **@usernames** som ska uteslutas från strömmen.

* **[!UICONTROL Additional Filters]**

   * Välj om du vill inkludera **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** eller **[!UICONTROL Photos Only]** i strömmen.

Ytterligare alternativ för strömningsregler för alla strömregler finns i [Alternativ för strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
