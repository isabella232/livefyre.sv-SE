---
description: Versionsinformation för 30 mars 2017-utgåvan.
seo-description: Versionsinformation för 30 mars 2017-utgåvan.
seo-title: 30 mars 2017
title: 30 mars 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 30 mars 2017{#march}

Versionsinformation för 30 mars 2017-utgåvan.

## Produktionsrelease

| Ärendetyp | Komponent | Versionsinformation |
|---|---|---|
| Fel | Social sökning | Korrigerade ett fel som förhindrade att sparade Youtube-resurser i den sociala sökningen publicerades. |
| Förbättring | Synkronisering via sociala medier | Twitter-social synkronisering har tagits bort. |
| Förbättring | Storify 2 | En förbättring har lagts till för att visa meddelandet&quot;Inga resultat hittades&quot; i ämnessökningen på Facebook när inga resultat hittas. |
| Förbättring | Strömmar | Lagt till sammanfattningsregler för SAFE-regler längst ned på en Twitter-strömsida. |
| Fel | Strömmar | En förbättring har lagts till för att synligt inaktivera kryssrutan&quot;verifierad användare&quot; i Twitter Stream-regler när uteslutna författare anges. |
| Fel | Strömmar | Korrigerade ett fel som tillät användning av nyckelord för OCH och ett platsfilter i en Twitter-regel. |
| Fel | Studio | Korrigerade ett fel som gjorde att &quot;Feature Tag&quot; inte kunde sparas korrekt när det tillämpades. |

## UAT-release

| Ärendetyp | Komponent | Versionsinformation |
|---|---|---|
| Fel | Appinnehåll | Ändrat beteendet för &quot;Mer information&quot; så att om det finns flera anonyma flagghändelser för ett visst innehåll visas alltid den tidigaste händelsen. |
| Fel | Bibliotek | Korrigerade ett fel som gjorde att bibliotekssökningar med hashtaggar ibland misslyckades. |
| Fel | Kartor | Korrigerade ett fel i kartor som stötte på ett stort antal innehåll i kluster på iOS-enheter. |
| Förbättring | Mosaik | Lagt till möjlighet att konfigurera Mosaic-appar att klicka var som helst på ett innehållskort för att öppna modal efter animeringstyp `none` i designern och `cardAnimation: 'off'`om det initieras via SDK. |
| Fel | Mosaik | Korrigerade ett fel som gjorde att användare kunde göra ändringar i Mosaic-appar i Designer. |
| Förbättring | Rättighetsbegäran | En ny status för rättighetsförfrågan med namnet&quot;Misslyckad begäran&quot; har lagts till för att markera när meddelanden om rättighetsförfrågan inte kan skickas. |
| Förbättring | Inställningar | Lagt till möjlighet för kunder att skapa regler för skräppostmoderering i Inställningar. |
| Förbättring | Social sökning | Korrigerade ett fel som förhindrade VK.com-inlägg från att visas via URL-sociala sökningar. |
| Förbättring | Social sökning | Om sökningen efter Instagram-innehåll från Studio beror på att en Instagram API-token har gått ut, visas felmeddelandet nu som en sådan. |
| Fel | Strömmar | Korrigerade ett fel som gjorde att bannern&quot;App tar inte emot nytt innehåll&quot; felaktigt visades ovanpå sidorna för flödesregel. |
| Förbättring | Strömmar | Ändrade standardvärdet för nyligen skapade strömregler till Använd SAFE-regler när det är tillämpligt. |
| Förbättring | Strömmar (tidigare Curate Rules) | Borttagen alternativet Endast vacciner från reglerna Twitter-ström/Curate, eftersom Vines nu visas som Twitter-videor. |
| Fel | Studio Shell | Korrigerade ett fel så att Livefyre Studio lästes in om https:// uttryckligen lades till på webbadressen. |

