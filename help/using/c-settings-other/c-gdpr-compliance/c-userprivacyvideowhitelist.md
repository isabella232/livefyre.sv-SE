---
description: Du kan vitlista din videodomän med .
seo-description: Du kan vitlista din videodomän med .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Om du använder egna videoklipp och spelare som en del av de videoklipp som visas i en Livefyre-visualiseringsapp kan du vitlista din videodomän. När du vitlistar videodomänen tas videomasken bort för anpassade videoklipp och spelare.

>[!NOTE]
>
>Använd specifika sökvägar för att säkerställa att endast de videoklipp som är säkra vitlistas. Om du anger en bred sökväg (till exempel sampantomain.com) kan du vitlista osäkra videofilmer.

* Lägg till `userPrivacyVideoWhitelist` efter `userPrivacyOptOut`. Du kan lägga till alla sekretessflaggor för Livefyre samtidigt som en del av ett Livefyre-objekt.
* `userPrivacyVideoWhitelist` gäller endast innehåll som inte är inbäddat från sociala medier.

I följande exempel visas videoklipp som visas i appar med `sampledomain.com/cdn/videos` sökvägen vitlistade:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
