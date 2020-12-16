---
description: Definiera inställningarna för att begära rättigheter för Instagram- och Twitter-inlägg.
seo-description: Definiera inställningarna för att begära rättigheter för Instagram- och Twitter-inlägg.
seo-title: Konfigurera Rights Management
solution: Experience Manager
title: Konfigurera Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# Konfigurera Rights Management{#set-up-rights-management}

Definiera inställningarna för att begära rättigheter för Instagram- och Twitter-inlägg.

Innan du kan definiera inställningar för rättighetsbegäran måste du konfigurera ett eller flera sociala konton för Instagram eller Twitter. Mer information om hur du konfigurerar ett socialt konto finns i [Lägg till ett socialt konto](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Du kan bara konfigurera behörighetshantering på nätverksnivå. Du kan inte konfigurera platsspecifik behörighetshantering.

1. Navigera till **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]** i Livefyre Studio.

   >[!NOTE]
   >
   >Du måste ha behörighet på nätverksnivå för moderatorn eller administratören för att kunna konfigurera Rights Management-konton.

1. Välj **[!UICONTROL +Add New Account]** om du inte har konfigurerat några Rights Management-konton.
1. Klicka på **[!UICONTROL Create New Setting]** under det sociala nätverk som du vill använda för Rights Management.

   >[!NOTE]
   >
   >För Instagram-konton måste du ha ett Instagram-företagskonto för att begära rättigheter med partiell automatisering. Mer information om olika typer av Instagram-konton och hur du använder dem finns i [Om Instagram-konton](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Fyll i de visade fälten. Alla fält är obligatoriska.

   * **[!UICONTROL Display name:]** Ange ett visningsnamn för att identifiera det Twitter- eller Instagram-konto som ska användas för ditt Rights Request-konto. Det här namnet är bara internt.
   * **[!UICONTROL Enabled:]**Använd som standard. Aktiverar rättighetshantering för kontot.
   * **[!UICONTROL Approval hashtag:]** Den hashtagg som innehållsägaren använder för att ange att de godkänner att använda innehållet.
   * **[!UICONTROL Terms and conditions:]** En länk till ditt nätverks villkor för återanvändning av innehåll. Det här fältet är skiftlägeskänsligt.
   * **[!UICONTROL Network and sites:]** Nätverket eller platsen som det här kontot kan begära återanvändningsrättigheter för innehåll. Om du vill göra det här kontot tillgängligt i hela nätverket markerar du det första objektet i listan eller begränsar det till vissa platser med hjälp av Kommando/CTRL-tangenten.
   * **[!UICONTROL Default message:]** Ett meddelande som ska visas med din behörighetsförfrågan. Du kan åsidosätta det här meddelandet när du begär rättigheter.

      * Livefyre presenterar ett av standardmeddelandena för moderatorerna när en moderator skickar en begäran till en innehållsförfattare. Moderatorerna kan generera ett annat standardmeddelande eller redigera meddelandet innan de skickar det. Meddelanden måste innehålla författarens Twitter- eller Instagram-handtag ({handle}), din godkännandehashtagg ({grantTag}) och en länk till dina villkor ({termsLink}).

         **[!UICONTROL Note:]** {handle}, {grantTag} och {termsLink} är skiftlägeskänsliga.

         **[!UICONTROL Note:]** För att förhindra obehörig användning kapslar Twitter in alla inkluderade URL:er med  [t.](https://t.co/) coformatting. För att förhindra att standardmeddelandet innehåller fler än 140 tecken rekommenderar Livefyre att du inte tar med URL:er i standardmeddelandet.

      * Bästa tillvägagångssätt för att skriva meddelanden om rättighetsförfrågan:

         * Skapa flera standardmeddelanden så att du inte låter som en robot. Spara varje standardmeddelande innan du skapar nästa standardmeddelande.
         * Uppmuntra dina moderatorer att anpassa den här anteckningen innan de skickar den för att förhindra att ditt nätverks förfrågningar taggas för skräppost.

1. Klicka på **[!UICONTROL Save Settings]** för att lägga till ditt Rights Request-konto.
Skicka en behörighetsförfrågan från resursbiblioteket. Mer information om hur du skickar en rättighetsbegäran från resursbiblioteket finns i [Skicka en rättighetsbegäran](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset).