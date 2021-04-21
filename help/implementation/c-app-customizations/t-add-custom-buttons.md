---
description: Lägg till anpassade åtgärder i Livefyre-apparna.
title: Lägg till anpassade knappar
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Lägg till anpassade knappar{#add-custom-buttons}

Lägg till anpassade åtgärder i Livefyre-apparna.

Med Livefyre kan du lägga till anpassade knappar bredvid de befintliga åtgärdsknapparna (som **[!UICONTROL Share]** och **[!UICONTROL Flag]**) för en del av innehållet.

Använd argumentet mobile för att definiera om knappen ska visas på mobila enheter.

Så här lägger du till en anpassad åtgärdsknapp för gränssnittet för den mobila enheten:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Skicka ytterligare ett argument i ConvConfig-objektet med namnet actionButtons, som innehåller en array med objekt som beskriver varje knapp som du vill lägga till.
1. Definiera en tangent för texten som ska visas för varje knapp.
1. Lägg till ett återanrop som anropas för en klickningshändelse för varje knapp.

Återanropet anropas med ett objekt med två tangenter: `authorId` och `contentId`.
