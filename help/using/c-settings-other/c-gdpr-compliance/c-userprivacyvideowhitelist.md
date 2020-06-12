---
description: Du kan tillåta att din videodomän listas.
seo-description: Du kan tillåta att din videodomän listas.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Om du använder dina egna anpassade videoklipp och spelare som en del av de videoklipp som visas i en Livefyre-visualiseringsapp kan du ange din videodomän som tillåten. Om du tillåter att videodomänen listas tas videomasken bort för dina anpassade videoklipp och spelare.

>[!NOTE]
>
>Använd specifika sökvägar för att säkerställa att endast de videoklipp som är säkra är tillåtna. Om du anger en bred sökväg (till exempel sampantomain.com) kan du tillåta att osäkra videofilmer listas.

* Lägg till `userPrivacyVideoWhitelist` efter `userPrivacyOptOut`. Du kan lägga till alla sekretessflaggor för Livefyre samtidigt som en del av ett Livefyre-objekt.
* `userPrivacyVideoWhitelist` gäller endast innehåll som inte är inbäddat från sociala medier.

I följande exempel är videoklipp som visas i appar med `sampledomain.com/cdn/videos` sökvägen tillåtna:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
