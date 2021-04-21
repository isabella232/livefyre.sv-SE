---
description: Du kan använda Livefyre Identity med Facebook för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.
title: Skapa en Facebook-app för användning med Livefyre-identitet
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Skapa en Facebook-app för användning med Livefyre-identitet{#create-a-facebook-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med Facebook för att tillåta användare att använda sina Facebook-inloggningar för att interagera med appar på din webbplats.

För att dina användare ska kunna logga in med sina Facebook-autentiseringsuppgifter krävs följande appinformation från Facebook:

* Program-ID
* Apphemlighet

Så här skapar du en Facebook-app som ska användas med Livefyre Identity:

1. Gå till [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Logga in på ditt Facebook-utvecklarkonto.
1. Klicka på **[!UICONTROL Add New App]** eller välj en befintlig app som ska användas med Livefyre-identitet.
1. Klicka på **[!UICONTROL Settings]** och sedan **[!UICONTROL Basic]**. Ange en **[!UICONTROL Contact Email]**-adress, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** och **[!UICONTROL Terms of Service URL]**.
1. Klicka på plustecknet ( **[!UICONTROL +]**) bredvid **[!UICONTROL Products]**.
1. Klicka på **[!UICONTROL Set Up]** under **[!UICONTROL Facebook Login]**.
1. Klicka på **[!UICONTROL Settings]** och ange följande:

   * Ange **[!UICONTROL Client OAuth Login]** till **[!UICONTROL Yes]**.
   * Ange **[!UICONTROL Web OAuth Login]** till **[!UICONTROL Yes]**.
   * Ange **[!UICONTROL Use Strict Mode for Redirect URIs]** till **[!UICONTROL Yes]**.
   * Ange **[!UICONTROL Enforce HTTPS for Web OAuth Login]** till **[!UICONTROL Yes]**.
   * Under **[!UICONTROL Valid OAuth redirect URLs]** lägger du till URL:en `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (där `{networkName}` är det nätverksnamn som tillhandahålls via Livefyre).

1. Under **[!UICONTROL App Review]**:

   * Gör appen offentlig.
   * Kontrollera att **[!UICONTROL Approved Items]** för **[!UICONTROL Login Permissions]** innehåller `email`, `public_profile` och `user_friends`.

När det är klart visas ditt program-ID och din apphemlighet på Facebook-utvecklarens Dashboard som du kan använda i Studions integreringsinställningar.
