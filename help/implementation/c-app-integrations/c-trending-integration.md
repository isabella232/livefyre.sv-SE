---
description: Visa de mest aktiva samlingarna på din webbplats eller i nätverket.
seo-description: Visa de mest aktiva samlingarna på din webbplats eller i nätverket.
seo-title: Trender
solution: Experience Manager
title: Trender
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 1%

---


# Trender{#trending}

Visa de mest aktiva samlingarna på din webbplats eller i nätverket.

Använd Trending för att visa samlingarna med den senaste aktiviteten på din plats eller i ditt nätverk.

## Integrering {#section_wtz_whb_c1b}

Det snabbaste sättet att integrera med Trending är att använda den byggda versionen som finns på Livefyres CDN.

Lägg först till [Livefyre.js](https://github.com/Livefyre/Livefyre.js) på sidan.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Placera sedan elementet som appen ska visas i.

```
<div id="trending"></div>
```

Använd slutligen `Livefyre.require` för att konstruera komponenten.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Nu har du en Trending App! Se allt detta i [det här exemplet](https://codepen.io/gobengo/pen/GijEy).

## Konfiguration {#section_k5k_qhb_c1b}

`network`

Det nätverk som samlingar ska hämtas från. (Obligatoriskt.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Ange plats-ID:t för att visa samlingar endast från en plats i nätverket. (Valfritt.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Ange en enda samlingstagg om du bara vill visa samlingar med den taggen. (Valfritt.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

