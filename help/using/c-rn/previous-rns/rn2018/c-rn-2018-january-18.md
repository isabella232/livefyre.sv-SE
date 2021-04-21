---
description: Versionsinformation för versionen från 18 januari 2018.
title: 18 januari 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 18 januari 2018{#january}

Versionsinformation för versionen från 18 januari 2018.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Appar | Ett fel som gjorde att Avatars inte kunde återges korrekt när en jpeg-fil användes har åtgärdats. |
| Fel | ModQ | Korrigerade ett fel för S1-kunder som tillåter filtrering med Collections i ModQ. |
| Fel | Strömmar | Korrigerade ett fel som bröt en direktuppspelningsregel när språkfiltret angavs som &quot;none&quot;. |
| Fel | Strömmar | Korrigerade ett fel som förhindrade att YouTube-strömregler sparades. |
| Fel | Strömmar | Korrigerar ett fel där användare kan skapa felaktigt formaterade geo-poster i strömregler och spara dem, vilket gör att strömmen misslyckas. Nu kan användare inte längre spara felformaterade geotaggar. |
| Fel | Studio | Ett problem som gjorde att vissa användare inte kunde logga in på Livefyre har korrigerats. |

## UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Bibliotek | Säkerhetsbuggfixen. Alla autentiseringsanrop görs nu med HTTPS-protokollet i stället för HTTP. |
| Förbättring | Smarta taggar | Strömmat innehåll taggas nu automatiskt av Adobe Sensei när det sparas i en mapp eller publiceras i en app. |
| Fel | Strömmar | Ett problem har korrigerats där japanska tecken inte kunde identifieras av Instagram-strömregler. |
| Förbättring | Strömmar | Kunderna kan nu använda de logiska operatorerna (ANY, ALL, NOT) för att skapa detaljerade smarta taggfilter i strömmar som strukturerar mycket mer exakt innehåll. Om jag till exempel använder hashtaggen #himalyas kan jag välja att bara visa bilder som innehåller&quot;snögubbe&quot;&quot;berg&quot;. |
| Fel | Studio | Åtgärda ett fel som visade specialtecken i namn som HTML. |
