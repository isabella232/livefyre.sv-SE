---
description: Visa de mest aktiva samlingarna på din webbplats eller i nätverket.
title: Trender
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
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
