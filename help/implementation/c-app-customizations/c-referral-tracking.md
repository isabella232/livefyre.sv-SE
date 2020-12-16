---
description: Spåra klickningar från hänvisningstrafik till sidan.
seo-description: Spåra klickningar från hänvisningstrafik till sidan.
seo-title: Referensspårning
solution: Experience Manager
title: Referensspårning
uuid: 5206cc16-9671-4b3d-a013-be1a3e8c029d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Hänvisningsspårning{#referral-tracking}

Spåra klickningar från hänvisningstrafik till sidan.

Livefyre lägger till en hänvisningsvariabel till URL:en när en kommentar publiceras eller delas i ett socialt nätverk, och för de länkar som ingår i Livefyre-e-postmeddelanden. Använd den här variabeln för att spåra hänvisningstrafik från Livefyre-appar till dina sociala eller ägda tillgångar.

Med Livefyre-appar kan du spåra dataströmmar som är ett resultat av hänvisningstrafik, så att du kan analysera webbplatsens trafik.

## Spårning av Livefyre-referenstrafik {#section_nsy_qp4_xz}

Hänvisningstrafiken för Livefyre från sociala nätverk och e-postmeddelanden kan spåras genom att undersöka frågesträngsparametrarna i webbadresserna för sidorna och implementera koden på sidan för att spåra detta via analysleverantören. Livefyre lägger till en hänvisningslänk till webbadressen när en kommentar publiceras eller delas i ett socialt nätverk, och för de länkar som ingår i Livefyre-e-postmeddelanden.

## Implementeringsexempel {#section_xvs_x44_xz}

Om trafiken kom från ett StreamHub-drivet meddelande kommer det att finnas en hubbRefSrc-frågesträngsparameter med värdet för e-post, Facebook, twitter, länkad eller permanent länk. Parameternamnet hubRefSrc kan konfigureras på nätverksnivå av ditt Livefyre-leveransteam.

Om du vill integrera med en analysplattform måste sidan leta efter navRefSrc vid inläsning och registrera trafiken om den finns.

Exempel:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```

Program som använder den här funktionen:

* [Chatt](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)