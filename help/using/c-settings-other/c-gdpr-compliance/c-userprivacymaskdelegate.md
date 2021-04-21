---
description: Du kan ändra den varningstext som visas på videomasker med .
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Du kan ändra den varningstext som visas på videomasker med .

Denna text finns för att uppfylla GDPR-förordningen. Om en källa inte stöder en proxy visar Livefyre den här texten och en mask i innehållet, såvida inte en användare klickar på videon och godkänner den potentiella spårningen från den källan.

Om du inte använder `userPrivacyMaskDelegate` visas följande standardtext:

Lägg till `userPrivacyMaskDelegate` efter `userPrivacyOptOut`. Du kan lägga till alla sekretessflaggor för Livefyre samtidigt som en del av ett Livefyre-objekt.

Här följer ett exempel på hur du använder `userPrivacyMaskDelegate`:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
