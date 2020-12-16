---
description: Du kan ändra den varningstext som visas på videomasker med .
seo-description: Du kan ändra den varningstext som visas på videomasker med .
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
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
