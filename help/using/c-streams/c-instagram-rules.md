---
description: Du kan skapa direktuppspelningsregler som hämtar innehåll från Instagram.
seo-description: Du kan skapa direktuppspelningsregler som hämtar innehåll från Instagram.
seo-title: Instagramregler
title: Instagramregler
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Instagramregler{#instagram-rules}

Du kan skapa direktuppspelningsregler som hämtar innehåll från Instagram.

>[!NOTE]
>
>Innan du skapar en Instagram-ström måste du lägga till minst ett Instagram-företagskonto i **[!UICONTROL Social Accounts]** avsnittet i **[!UICONTROL Network Settings]**. Mer information om hur du konfigurerar ett Instagram-konto finns i [Om Instagram-konton](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Skapa Instagram-regler baserat på @mentions eller hashtag.

>[!NOTE]
>
>Alla Instagram-regler kräver minst en hashtagg. Om du lägger till nyckelord och ett användarnamn för regeln returneras innehåll som innehåller båda posterna.

Om du vill skapa Instagram-regler för att hämta innehåll från Instagram-flöden till din app eller mapp, filtrerar du efter:

* **[!UICONTROL Words]**

   * Ange **[!UICONTROL hashtags]** som ska inkluderas i eller exkluderas från Instagram-strömmen. Om du anger värden för både **[!UICONTROL Contains]** - och **[!UICONTROL Does not contain]** -fälten returneras bilder som innehåller den första och inte den andra.

   * Om du till exempel anger **[!UICONTROL Contains]** nyckelorden Giants, Posey och **[!UICONTROL Does not contain]** nyckelordet Dodger returneras alla inlägg som innehåller ordet Giants eller Posey, och inte ordet Dodger.

      >[!NOTE]
      >
      >Instagram Rules returnerar inlägg som innehåller den listade hashtaggen i författarens kommentarer, som kanske inte visas i strömmen.

* **[!UICONTROL Mentions]**

   * Ange **[!UICONTROL @mentions]** för att hämta till strömmen eller exkludera från strömmen.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Du måste ha ett Instagram-företagskonto konfigurerat i Livefyre för att kunna använda författarsökningen i en regel för Instagram-strömning. Mer information om hur du ställer in Instagram-affärskonton i Livefyre finns i [Om Instagram-konton](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Ange **[!UICONTROL @usernames]** för att dra in i strömmen. Kontot som är associerat med **@username** måste vara ett Instagram-företagskonto.

   * Ange **@usernames** som ska uteslutas från strömmen.

* **[!UICONTROL Additional Filters]**

   * Välj om du vill inkludera **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** eller **[!UICONTROL Photos Only]** i strömmen.

Ytterligare alternativ för strömningsregler för alla strömregler finns i Alternativ för [strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
