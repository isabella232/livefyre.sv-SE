---
description: Du kan använda Livefyre Identity med GitHub Identity för att tillåta användare att använda sina GitHub-inloggningar för att interagera med appar på webbplatsen.
seo-description: Du kan använda Livefyre Identity med GitHub Identity för att tillåta användare att använda sina GitHub-inloggningar för att interagera med appar på webbplatsen.
seo-title: Skapa en GitHub-identitetsapp för Livefyre-identitet
title: Skapa en GitHub-identitetsapp för Livefyre-identitet
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
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
