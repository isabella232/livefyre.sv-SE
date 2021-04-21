---
description: Versionsinformation för februari 2018-utgåvan.
title: 15 februari 2018
exl-id: 7276de37-c8cd-4e85-bc92-90c272e5bf94
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 15 februari 2018{#february}

Versionsinformation för februari 2018-utgåvan.

## Nya funktioner {#section_syx_mdt_wcb}

Följande funktioner är nya i produktionsversionen av den här versionen:

* **Smarta taggar.**

   Livefyre använder Adobe Sensei bildigenkänningsteknik för att automatiskt tagga bilder du sparar i biblioteket.
Med smarta taggar kan du spara mycket tid när du söker efter och modererar innehåll. Med smarta taggar kan du:

   * Söka i sparade bilder efter exakt innehåll baserat på bildinnehållet i stället för enbart text
   * Samla innehåll i strömmar baserat på exakta söktermer som analyserar bilden, i stället för bara text

   Mer information om smarta taggar finns i [Smarta taggar](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Meddelanden i produkten.** När du nu loggar in på Livefyre Studio öppnas ett meddelandefönster med uppdateringar om nya funktioner.
* **UGC för Carousel.** Nu kan du använda alla funktioner i UGC Commerce i Livefyre Carousel-appen. Du kan skapa en Call-to-Action Button och koppla din produktkatalog till appen för att skapa en köpbar upplevelse från Carousel.

## Problem {#section_ehw_ndt_wcb}

Problemen i följande tabeller löstes i den här versionen.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Problem | ModQ | Korrigerade ett problem där Instagram-inlägg som markerats som godkända eller hashas återgick till kön. |
| Förbättring | Rights Management | En förbättring har lagts till för att visa en varning vid försök att använda utgångna Instagram-konton när rättighetsbegäranden görs. |
| Problem | Trender | Korrigerade ett problem med Trends App som fortfarande tillåter HTTP vid olika tillfällen i stället för HTTPS. |

## UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Förbättring | Appar | Lagt till möjligheten att ta bort appar från Livefyre. |
| Problem | Omröstningar | Ändrade omröstningar så att enbart HTTPS används. Tidigare tilläts omröstningar fortfarande användas med HTTP. |
| Problem | UGC | Ett problem har korrigerats där UGC i en visualiseringsapp inte filtrerade efter produkt-ID som förväntat. |
