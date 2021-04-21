---
description: Versionsinformation för 1 november 2018.
title: 1 november 2018
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 1 november 2018{#november}

Versionsinformation för 1 november 2018.

## Nya funktioner {#section_syx_mdt_wcb}

Följande nya funktioner släpptes i produktionsversionen av den här versionen:

* Smarta taggar för video

   Utnyttja den senaste tekniken för datavinseende, som drivs av Adobe Sensei, för att automatiskt tagga videomaterial när du sparar det i biblioteket. Smarta taggar hjälper dig att hantera UGC mer effektivt men också skapa superprecisa kurationsregler (strömmar) som samlar in innehåll baserat på vad som finns i videon, inte bara texten, vilket sparar mycket arbete när du modererar oönskat innehåll.

   Funktioner:

   * Smarta taggar läggs automatiskt till i videor som hämtats från sociala sökningar, strömmar och överförda videofiler i biblioteket. Visa taggar i resursinformationen för en enskild video
   * Taggar videoklipp i formaten .MP4, .MOV och AVI
   * Taggar videoklipp på upp till 60 sekunder eller 50 MB
   * Det finns två kategorier med smarta taggar för videoklipp: funktioner (djur, objekt, platser osv.) och åtgärder (löpning, gång, sångning osv.)

   Mer information finns i [Smarta taggar](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram Rate Limiting

   Instagram har ändrat antalet begäranden som alla företag som använder Instagram API, inklusive Livefyre, kan göra från 5 000 begäranden per timme och token till 200 begäranden per timme och token. Detta kallas *hastighetsbegränsning*. Mer information finns i [Instagram Rate Limiting](/help/using/c-streams/c-instagram-rate-limiting.md).

* Ljudfiler i biblioteket

   Nu kan du utföra följande funktioner på ljudfiler från bibliotekspanelen:

   * Sök
   * Förhandsgranska
   * Importera
   * Filtrera efter ljudfiler
   * Dra och släpp filer i designern

## Problem {#section_ehw_ndt_wcb}

Inga nya problem löstes i produktionsversionen av den här versionen. Se [avsnittet ovan](#c_rn/section_syx_mdt_wcb).

## UAT-version {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Problemen i följande tabeller löstes i UAT-versionen av den här versionen.

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Förbättring | GDPR | Alla data som tilldelats tidigare kunder inom Analytics tas bort. |
| Fel | Bibliotek | Ett problem där en video som överfördes till biblioteket och sedan visades i resursinformationen inte visades korrekt har åtgärdats. |
| Fel | Mosaik | Korrigerade ett problem där mosaiken visade det sista innehållet från en Instagram-karusell som en miniatyrbild i stället för ett kort. |
| Fel | Social sökning | Korrigerade ett problem där Instagram sociala sökning inte fungerade som förväntat. |
