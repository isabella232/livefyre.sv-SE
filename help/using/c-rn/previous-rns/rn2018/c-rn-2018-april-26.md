---
description: Versionsinformation för versionen från 26 april 2018.
title: 26 april 2018
exl-id: af0ee64d-d60c-4b21-a628-08848313781c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 26 april 2018{#april}

Versionsinformation för versionen från 26 april 2018.

## Nya funktioner {#section_syx_mdt_wcb}

Följande funktioner är nya i produktionsversionen av den här versionen:

* En ny funktion har lagts till som gör att kunderna kan konfigurera ett visst antal kolumner för en medievägg. Det antal kolumner du väljer tvingar medieväggen till det antalet kolumner, oavsett storlek. I annat fall är antalet Media Wall-kolumner som standard &quot;auto&quot;, där kolumnerna justeras till ett tal som optimerar Media Wall för skärmstorleken.
* I Media Wall Designer finns det nu ett reglage som du kan använda för att stänga av den automatiska medieväggsanimeringen som visas när en sida med en medievägg läses in.
* Du kan nu välja ett tröskelvärde för tillförlitlighet för smarta taggar i strömmar. Genom att ställa in precisionspoängen (0-100) för taggar kan du styra exaktheten för de resurser som vi hämtar.
* Tillagda modereringsrekommendationer. Livefyre skannar nu in alla inlägg i kommenteringsappar och förutser om du kommer att förstöra dem eller inte baserat på historiska data och maskininlärning. Dessa rekommendationer visas i ModQ.
   * Användarna kan stänga av modereringsrekommendationer, som gör att användarna kan filtrera ModQ efter innehållet som Livefyre tror att du kommer att slänga.
   * Lagt till möjlighet att filtrera ModQ med rekommendationstaggen för moderering, Skräp.

## Problem {#section_ehw_ndt_wcb}

Problemen i följande tabeller löstes i den här versionen.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Rights Management | Ett problem har korrigerats där rättighetsförfrågningar inte fungerade för resurser efter att de hade hittats i en social sökning. |
| Förbättring | Strömmar | Den strömningsmekanism som gör att innehåll kan strömmas från Facebook för att följa en backend-ändring som skapats av Facebook har uppdaterats. |
| Fel | UGC Commerce | Ett problem har korrigerats där CTA-knappen &quot;Shop&quot; inte visades i en Mosaic- eller bildbandsapp eller i en produkt när du hovrar över ett kort med en produkt när CTA-knappen är aktiverad. |
| Förbättring | UGC Commerce | Ett problem har korrigerats där UGC Commerce-flaggan var inställd på &quot;off&quot; som standard i stället för &quot;on&quot;. |

## UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Bibliotek/sökning | Ett problem med att videoklipp inte överfördes korrekt har korrigerats. |
| Förbättring | Studio | Lagt till möjlighet att se föreslagna ord när du skriver i taggnamn. |
