---
description: Om du vill aktivera en social inloggning använder du Studio för att lägga till inloggningsuppgifterna för dina sociala appar i Livefyre-integreringen och för att anpassa inloggningsmodulen.
seo-description: Om du vill aktivera en social inloggning använder du Studio för att lägga till inloggningsuppgifterna för dina sociala appar i Livefyre-integreringen och för att anpassa inloggningsmodulen.
seo-title: Använda Studio för att ansluta sociala appar till Livefyre-implementeringen
title: Använda Studio för att ansluta sociala appar till Livefyre-implementeringen
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---


# Använda Studio för att ansluta sociala appar till din Livefyre-implementering{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Om du vill aktivera en social inloggning använder du Studio för att lägga till inloggningsuppgifterna för dina sociala appar i Livefyre-integreringen och för att anpassa inloggningsmodulen.

## Anpassa inloggningsmodulen {#section_v4c_hv2_3z}

Med inloggningsmodulen kan du anpassa den information som användarna ser när de loggar in i dina program. Du kan anpassa det modala fönstret.

* **Logo:** Överför en logotyp för användning i dina inloggningsmoduler.
* **Teckensnittsfamilj:** Välj ett teckensnitt som matchar din profilering.
* **Märkesfärg:** Ange en hexfärg som ska användas för viss text i det modala dokumentet.
* **URL för villkor:** Ange URL-adressen till företagets sida med villkor. Det här fältet är obligatoriskt för användning med Livefyre-identitet.

## Översätter Livefyre-identitet {#section_xxt_z52_3z}

Du kan skapa och ändra översättningsuppsättningar för textsträngar i Livefyre Identity.

Mer information om hur du använder översättningsuppsättningar med Livefyre-identitet finns i Översättningsuppsättningar.

Mer information om de specifika strängar du kan anpassa för Livefyre Identity finns i Livefyre Identity.

## Aktivera inloggning med e-post {#section_dlv_wzt_bbb}

Tillåt användare att använda sina e-postadresser för att logga in och interagera med appar på din webbplats.

Så här aktiverar du inloggning med ett LiveCyre-konto:

1. Navigera till **[!UICONTROL Integration Settings]** i Livefyre Studio.
1. Växla **[!UICONTROL Enable Login with Email]** till **[!UICONTROL On]**.

## Aktivera inloggning med ett Facebook-konto {#section_ph3_515_bbb}

Anslut ditt Facebook-konto till Livefyre så att användarna kan använda sina Facebook-inloggningar för att interagera med appar på din webbplats.

Så här aktiverar du inloggning med ett Facebook-konto:

1. Växla **[!UICONTROL Enable Login with Facebook]** till **[!UICONTROL ON]**.

1. Lägg till din Facebook-apps **[!UICONTROL App ID]** och **[!UICONTROL App Secret]**.

   Dessa värden listas i din Facebook-utvecklarinstrumentpanel för appen, som är tillgänglig från [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Aktivera inloggning med Google {#section_fq3_kb5_bbb}

Anslut ditt Google+-konto till Livefyre så att användarna kan använda sina Google+-inloggningar för att interagera med appar på din webbplats.

Så här aktiverar du inloggning med ett Google+-konto:

1. Växla **[!UICONTROL Enable Login with Google]** till **[!UICONTROL ON]**.

1. Lägg till din Google-apps **[!UICONTROL Client ID]** och **[!UICONTROL Client secret]**.

   Dessa värden listas i ditt projektgränssnitt för Google Cloud Platform, som finns på [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Om du vill hämta den här informationen går du till **[!UICONTROL API Manager > Credentials]** och klickar på projektnamnet.

## Aktivera en inloggning med ett Twitter-konto {#section_iyz_wb5_bbb}

Anslut ditt Twitter-konto till Livefyre så att användarna kan använda sina Twitter-inloggningar för att interagera med appar på din webbplats.

Så här aktiverar du inloggning med ett Twitter-konto:

1. Växla **[!UICONTROL Enable Login with Twitter]** till **[!UICONTROL ON]**.

1. Lägg till din Twitter-app **[!UICONTROL Consumer Key (API Key)]** och **[!UICONTROL Consumer Secret (API Secret)]**.

   Dessa värden listas på din Twitter-apps **[!UICONTROL Keys and Access Tokens]**-sida, som är tillgänglig från [https://apps.twitter.com/](https://apps.twitter.com/).

## Aktivera inloggning med Yahoo! Konto {#section_s1q_3c5_bbb}

Koppla samman din Yahoo! konto hos Livefyre så att användarna kan använda sina Yahoo! inloggningar för att interagera med appar på din webbplats.

Aktivera inloggning med en Yahoo! konto:

1. Växla **[!UICONTROL Enable Login with Yahoo!]** till **[!UICONTROL ON]**.

1. Lägg till din Yahoo! är **[!UICONTROL Client ID]** och **[!UICONTROL Client Secret]**.

   Dessa värden listas i Yahoo! app details page, available from [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Aktivera inloggning med ett Microsoft Live-konto {#section_z42_4c5_bbb}

Anslut ditt Microsoft Live ID-konto till Livefyre så att användarna kan använda sina Microsoft Live ID-inloggningar för att interagera med appar på webbplatsen.

Så här aktiverar du inloggning med ett Microsoft Live ID-konto:

1. I **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]** växlar du **[!UICONTROL Enable Microsoft Live Login]** till **[!UICONTROL On]**.

1. Ange **[!UICONTROL Microsoft Live Client ID (Private Key)]** och **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Klicka på **[!UICONTROL Save Settings]**.

   Värdena **[!UICONTROL Microsoft Live Client ID (Private Key)]** och **[!UICONTROL Microsoft Live Client Secret (Password)]** visas på informationssidan för Microsoft Live ID-appen.

## Anslut dina sociala appar till Livefyre-identitet {#section_on2_vc5_bbb}

Gör det möjligt för användarna att använda din Livefyre Identity-implementering för appar på din webbplats.

1. Skapa en app.
1. Navigera till **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**.

1. Ange nödvändiga appautentiseringsuppgifter för appen som du skapade.