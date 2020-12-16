---
description: Rita upp användarinnehåll på en interaktiv karta.
seo-description: Rita upp användarinnehåll på en interaktiv karta.
seo-title: Karta
solution: Experience Manager
title: Karta
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Karta{#map}

Rita upp användarinnehåll på en interaktiv karta.

Med kartan kan du strömma geotaggat innehåll till en världskarta, så att du kan hitta de sociala problemen kring nyheter eller live-event. Allt relevant innehåll visas, inklusive text, kommentarer, foton och tweets.

>[!NOTE]
>
>Kartor drivs av [©OpenStreetMap](https://www.openstreetmap.org/copyright), som innehåller de data Livefyre använder för att återge sina kartor.

## Integrering {#section_w2m_db2_d1b}

Det snabbaste sättet att använda kartan är att använda den byggda versionen som finns på Livefyres CDN.

Lägg först till [Livefyre.js](https://github.com/Livefyre/Livefyre.js) på sidan.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Placera sedan det element som Kartappen ska visas i.

```
<div id="map" style="height: 500px;"></div>
```

Slutligen använder du Livefyre.require för att konstruera kartan och hämta en samling från streamhub-sdk. Tänk på att kartan bara kan visa innehåll med geotaggade metadata. Twitter och Instagram Curate har stöd för den här funktionen. För att få bästa prestanda bör du ta med ett geolokaliseringsfilter på alla dina Curate Rules för samlingen.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Ta en titt på det här [levande exemplet](https://codepen.io/cheung31/pen/wkmbF).

## Konfiguration {#section_jc5_gxb_c1b}

`initial`

Det ursprungliga antalet objekt som ska läsas in från samlingen och visas på kartan. När det här numret har lästs in kan användaren klicka på en knapp för att visa mer. (Valfritt. Standardvärdet är 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Alternativ för att skicka till den underliggande [bipacksedeln](https://leafletjs.com/)-kartan som används för återgivning av kartan. Använd det här alternativet om du vill ange [Alternativ för map-karta för broschyrer för broschyrer](https://leafletjs.com/reference.html#map-options), inklusive kartans första mittpunkt samt inledande och högsta zoomnivåer. (Valfritt.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

