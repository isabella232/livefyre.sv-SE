---
description: Du kan tillåta att din videodomän listas.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Om du använder dina egna anpassade videoklipp och spelare som en del av de videoklipp som visas i en Livefyre-visualiseringsapp kan du ange din videodomän som tillåten. Om du tillåter att videodomänen listas tas videomasken bort för dina anpassade videoklipp och spelare.

>[!NOTE]
>
>Använd specifika sökvägar för att säkerställa att endast de videoklipp som är säkra är tillåtna. Om du anger en bred sökväg (till exempel sampantomain.com) kan du tillåta att osäkra videofilmer listas.

* Lägg till `userPrivacyVideoWhitelist` efter `userPrivacyOptOut`. Du kan lägga till alla sekretessflaggor för Livefyre samtidigt som en del av ett Livefyre-objekt.
* `userPrivacyVideoWhitelist` gäller endast innehåll som inte är inbäddat från sociala medier.

I följande exempel är videoklipp som visas i appar med sökvägen `sampledomain.com/cdn/videos` tillåtna:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
