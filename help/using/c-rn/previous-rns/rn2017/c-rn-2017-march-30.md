---
description: Versionsinformation för 30 mars 2017-utgåvan.
title: 30 mars 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 30 mars 2017{#march}

Versionsinformation för 30 mars 2017-utgåvan.

## Produktionsrelease

| Ärendetyp | Komponent | Versionsinformation |
|---|---|---|
| Fel | Social sökning | Korrigerade ett fel som förhindrade att sparade Youtube-resurser i den sociala sökningen publicerades. |
| Förbättring | Synkronisering via sociala medier | Inaktuell Twitter Social Sync. |
| Förbättring | Storify 2 | En förbättring har lagts till för att visa meddelandet&quot;Inga resultat hittades&quot; i Facebook ämnessökning när inga resultat hittas. |
| Förbättring | Strömmar | Lagt till sammanfattningsregler för SAFE-regler längst ned på en Twitter Stream-sida. |
| Fel | Strömmar | En förbättring har lagts till för att synligt inaktivera kryssrutan&quot;verifierad användare&quot; i Twitter Stream Rules när exkluderade författare anges. |
| Fel | Strömmar | Korrigerade ett fel som tillåter användning av nyckelord för OCH och ett platsfilter i en Twitter-regel. |
| Fel | Studio | Korrigerade ett fel som gjorde att &quot;Feature Tag&quot; inte kunde sparas korrekt när det tillämpades. |

## UAT-release

| Ärendetyp | Komponent | Versionsinformation |
|---|---|---|
| Fel | Appinnehåll | Ändrat beteendet för &quot;Mer information&quot; så att om det finns flera anonyma flagghändelser för ett visst innehåll visas alltid den tidigaste händelsen. |
| Fel | Bibliotek | Korrigerade ett fel som gjorde att bibliotekssökningar med hashtaggar ibland misslyckades. |
| Fel | Kartor | Korrigerade ett fel i Kartor som stötte på ett stort antal innehåll i kluster på iOS-enheter. |
| Förbättring | Mosaik | Lagt till möjlighet att konfigurera Mosaic-appar att klicka var som helst på ett innehållskort för att öppna modala efter animeringstyp `none` i designer och `cardAnimation: 'off'`om det initieras via SDK. |
| Fel | Mosaik | Korrigerade ett fel som gjorde att användare kunde göra ändringar i Mosaic-appar i Designer. |
| Förbättring | Rättighetsbegäran | En ny status för rättighetsförfrågan med namnet&quot;Misslyckad begäran&quot; har lagts till för att markera när meddelanden om rättighetsförfrågan inte kan skickas. |
| Förbättring | Inställningar | Lagt till möjlighet för kunder att skapa regler för skräppostmoderering i Inställningar. |
| Förbättring | Social sökning | Korrigerade ett fel som förhindrade VK.com-inlägg från att visas via URL-sociala sökningar. |
| Förbättring | Social sökning | Om sökningen efter Instagram-innehåll från Studio beror på att en Instagram API-token har upphört att gälla, kommer felmeddelandet nu att indikera detta. |
| Fel | Strömmar | Korrigerade ett fel som gjorde att bannern&quot;App tar inte emot nytt innehåll&quot; felaktigt visades ovanpå sidorna för flödesregel. |
| Förbättring | Strömmar | Ändrade standardvärdet för nyligen skapade strömregler till Använd SAFE-regler när det är tillämpligt. |
| Förbättring | Strömmar (tidigare Curate Rules) | Borttagen alternativet Endast vacciner från Twitter Stream/Curate-regler, eftersom Vines nu visas som Twitter-videor. |
| Fel | Studio Shell | Korrigerade ett fel så att Livefyre Studio lästes in om https:// uttryckligen lades till på webbadressen. |
