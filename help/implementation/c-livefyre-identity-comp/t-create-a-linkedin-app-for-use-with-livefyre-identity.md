---
description: Du kan använda Livefyre Identity med LinkedIn för att tillåta användare att använda sina LinkedIn-inloggningar för att interagera med appar på din webbplats.
title: Skapa en LinkedIn-app för användning med Livefyre-identitet
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Skapa en LinkedIn-app för användning med Livefyre-identitet{#create-a-linkedin-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med LinkedIn för att tillåta användare att använda sina LinkedIn-inloggningar för att interagera med appar på din webbplats.

För att aktivera LinkedIn-inloggning krävs följande appinformation för LinkedIn:

* Konsumentnyckel (API-nyckel)
* Consumer Secret (API-hemlighet)

Så här skapar du en LinkedIn-app som ska användas med Livefyre-identitet:

1. Gå till https://www.linkedin.com/secure/developer och logga in på ditt LinkedIn-konto för att skapa en ny app eller välja en befintlig app som ska användas med Livefyre Identity.
1. Klicka på **[!UICONTROL Create Application]**.
1. Fyll i formuläret för att skapa programmet.
1. Aktivera appbehörigheterna **[!UICONTROL r_basicprofile]** och **[!UICONTROL r_emailaddress]** i **[!UICONTROL Default Application Permissions]**.
1. Ange **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** som `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Spara appen.
1. I **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** växlar du **[!UICONTROL Enable LinkedIn Login]** till **[!UICONTROL On]**.
1. Ange LinkedIn klient-ID och LinkedIn Client Secret.
1. Klicka på **[!UICONTROL Save Settings]**.

När det är klart visas appinformationssidan i LinkedIn en lista över programmets API-nyckel (Consumer Key) och API Secret (Consumer Secret) som kan användas på Studios integreringsinställningar.
