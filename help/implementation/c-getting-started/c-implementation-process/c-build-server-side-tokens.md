---
description: En guide för att skapa collectionMeta och auth-tokens.
seo-description: En guide för att skapa collectionMeta och auth-tokens.
seo-title: Bygg token på serversidan
solution: Experience Manager
title: Bygg token på serversidan
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Bygg token på serversidan{#build-server-side-tokens}

En guide för att skapa collectionMeta och auth-tokens.

Genom att skapa de tokens som Livefyre använder för att validera förfrågningar säkerställer du att bara du kan uppdatera ditt Livefyre-nätverk.

## CollectionMeta-token

Lär dig hur du skapar en token för att skapa nya och visa befintliga konversationer.

## Autentiseringstoken

Lär dig hur du skapar en token för autentisering av användare, ett nödvändigt steg i integreringsprocessen om du inte använder Janrain Capture för användarhantering.

## Autentiseringstoken för användare {#section_l5l_hwt_bbb}

I det här avsnittet beskrivs hur du skapar det JSON-objekt för UserAuth som skapar den token för användarautentisering som krävs för att logga in användare i dina appar.

Om du vill skapa en variabel använder du det önskade språkbiblioteket och skickar följande parametrar:

| Parameter | Typ | Beskrivning |
|---|---|---|
| networkName | Sträng *krävs* | Namnet på Livefyre-nätverket (tillhandahålls av Livefyre). |
| networkKey | Sträng *krävs* | Den hemliga nyckeln för det här specifika nätverket (tillhandahålls av Livefyre). |
| userId | Sträng *krävs* | ID:t för användaren som loggar in som det är lagrat i ditt användarhanteringssystem (endast alfanumeriska tecken, bindestreck, understreck och punkttecken tillåts: `[a-zA-Z0-9_-.]`). **Obs!** UserId måste vara unikt. |
| förfaller | Heltal *krävs* | När token ska upphöra att gälla från och med nu (i sekunder). **Obs!** Det här värdet kan också skickas som ett flyttal. JSON-webbtoken som skapas lagrar det här värdet i UNIX-epok. |
| displayName | Sträng *krävs* | Text som identifierar den här användaren i användargränssnittet och i kommentarer. (Maximalt antal tecken: 50.) |

