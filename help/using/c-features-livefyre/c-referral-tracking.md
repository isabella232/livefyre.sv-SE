---
description: Spåra klickningar från hänvisningstrafik till sidan.
seo-description: Spåra klickningar från hänvisningstrafik till sidan.
seo-title: Referensspårning
solution: Experience Manager
title: Referensspårning
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
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

* [Chatt](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentarer](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioner](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

