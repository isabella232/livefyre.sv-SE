---
description: Du kan använda Livefyre Identity med GitHub Identity för att tillåta användare att använda sina GitHub-inloggningar för att interagera med appar på webbplatsen.
title: Skapa en GitHub-identitetsapp för Livefyre-identitet
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Skapa en GitHub-identitetsapp för användning med Livefyre-identitet{#create-a-github-identity-app-for-use-with-livefyre-identity}

Du kan använda Livefyre Identity med GitHub Identity för att tillåta användare att använda sina GitHub-inloggningar för att interagera med appar på webbplatsen.

För att användare ska kunna logga in med sina GitHub-identitetsuppgifter krävs följande GitHub-identitetsinformation för Livefyre:

* Klient-ID (privat nyckel)
* Klienthemlighet (lösenord)

Så här skapar du en GitHub-identitetsapp för användning med Livefyre-identitet:

1. Skapa eller logga in på ett GitHub-konto på [](https://github.com/settings/developers).
1. Registrera ett nytt program eller välj ett befintligt program som ska användas med Livefyre Identity.
1. Ange all information i formuläret. Ange **[!UICONTROL Authorization callback URL]** med ditt nätverksnamn i stället för `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. I **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]** växlar du **[!UICONTROL Enable GitHub Login]** till **[!UICONTROL On]**.

1. Ange GitHub-klient-ID och GitHub-klienthemlighet.
1. Klicka på **[!UICONTROL Save Settings]**.

När det är klart visas appinformationssidan för GitHub Identity med programmets klient-ID (konsumentnyckel) och klienthemlighet (konsumenthemlighet) för användning på Studions integreringsinställningar.
