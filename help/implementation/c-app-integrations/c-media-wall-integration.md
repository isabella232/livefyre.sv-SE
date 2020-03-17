---
description: Skapa en mediemur med strömmande innehåll i realtid.
seo-description: Skapa en mediemur med strömmande innehåll i realtid.
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Media Wall{#media-wall}

Skapa en mediemur med strömmande innehåll i realtid.

Med Media Wall kan ni skapa en social vägg i realtid för er webbplats. Använd Livefyres JavaScript SDK:s strömlinjeformade paket för att visa sociala flöden i Livefyre som en visuellt engagerande, helskärmsbaserad upplevelse som passar bra för att täcka in live-event, skapa hosting-fototävlingar och driva sociala delar av webbplatsen.

## Integrering {#section_jfm_bwb_c1b}

Det snabbaste sättet att lägga till en medievägg är att använda den byggda versionen som finns på Livefyres CDN.

Lägg först till [Livefyre.js](https://github.com/Livefyre/Livefyre.js) på webbplatsen.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Placera sedan det element som medieväggen ska visas i.

```
<div id="wall"></div>
```

Slutligen använder du `Livefyre.require` för att konstruera komponenten.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

Nu har du en mur! Se hur allt fungerar i [det här exemplet](https://codepen.io/gobengo/pen/dFwDL).

**Har du råkat ut för ett fel?** Kontrollera att du skickar rätt miljöparameter. Alternativen är `livefyre.com` (produktion) eller `t402.livefyre.com` (UAT).

>[!NOTE]
>
>All formatanpassning av tweets som återges av din medieväggsapp måste göras i enlighet med Twitters [visningskrav](https://dev.twitter.com/terms/display-requirements).

## Konfigurationsalternativ {#section_ucv_qvb_c1b}

`columns`

Gör att du kan definiera antalet kolumner för medieväggen när du skapar väggen. Om det här alternativet anges anpassas bredden på varje kolumn automatiskt till Media Wall-panelens behållarstorlek, samtidigt som det angivna antalet kolumner behålls.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Antalet innehållsobjekt som ska återges vid sidinläsning. Standardvärdet är 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Gör att du kan ange den minsta (pixelbredden) för varje kolumn i Medieväggningens behållarelement. (Medieväggen väljer automatiskt ett lämpligt antal kolumner, beroende på bredden på behållarelementet. Som standard bestäms antalet kolumner av medieväggens bredd, dividerad med den minsta innehållsbredden (300px, om den är odefinierad).

>[!NOTE]
>
>Använd inte det här alternativet i kombination med alternativet för kolumner.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Som standard visas en klickbar miniatyrbild när det finns bifogade filer för ett visst innehåll. När du klickar på det här alternativet öppnas en modal som visar foto-/videobilagan i sin helhet. Om du vill inaktivera det här alternativet anger du modal till false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Anger vilken [!UICONTROL Post Content] knapp som ska visas på väggen. Det här alternativet kräver att du skickar `opts.collection`och lägger till en Livefyre.js Auth-integrering på sidan.

`postButton` parametrar:

* `false` (standard): Visa inte knappen Skicka innehåll. (Skapar en skrivskyddad medievägg.)
* `true` (eller `LiveMediaWall.postButtons.contentWithPhotos`): Inkludera en knapp som gör att användare kan lägga till textinnehåll med bifogade foton.

* `LiveMediaWall.postButtons.content`: Inkludera en knapp som gör att användare kan lägga till textinnehåll, men inte bifoga foton.
* `LiveMediaWall.postButtons.photo`: Inkludera en knapp som gör att användare kan lägga till ett foto, men ingen text.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definierar antalet innehållsobjekt som ska läggas till i väggen när någon klickar på [!UICONTROL Show More] knappen.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Alternativ för formatkonfiguration {#section_ztv_dvb_c1b}

Media Wall erbjuder också flera konfigurationsalternativ som du kan använda för att anpassa textfärg, stil och storlek. Använd följande syntax för att implementera dessa alternativ:

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Giltiga indata finns i W3C-standarderna för egenskaperna CSS [Font Family](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Font Size](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) Line Height och [Color](https://www.w3.org/TR/css3-color/#colorunits) .

* **bodyFontSize** *(CSS Font Size String)* Teckensnittsstorleken för brödtext i innehåll.

* **bodyLineHeight** *(CSS Line Height String)* Radhöjden för innehållstext.

* **buttonActiveBackgroundColor** *(CSS-färgsträng)** Knappens bakgrundsfärg är aktiv.

* **buttonBorderColor** *(CSS-färgsträng)** Färgen för knappkanter.

* **buttonHoverBackgroundColor** *(CSS-färgsträng)* Färgen för knappens bakgrund vid hovring.

* **buttonTextColor** *(CSS-färgsträng)* Färgen för knappetiketterna.

* **cardBackgroundColor** *(CSS-färgsträng)* Bakgrundsfärgen för innehållskort i medieväggen.

* **displayNameColor** *(CSS-färgsträng)* Färgen för visningsnamn i bytelinjen.

* **fontFamily** *(CSS Font Family String)* Teckensnittsfamiljen för brödtext.

* **footerTextColor** *(CSS-färgsträng)* Färgen för sekundär text (t.ex. sidfotstext och användarnamn i rutnätet).

* **linkAttachmentBackgroundColor** *(CSS-färgsträng)* Bakgrundsfärgen för bifogade länkar (staplade bilagor).

* **linkAttachmentBorderColor** *(CSS-färgsträng)* Kantfärgen för bifogade länkar (staplade bilagor).

* **linkAttachmentTextColor** *(CSS-färgsträng)* Färgen för länkad bilagetext.

* **linkColor** *(CSS-färgsträng)* Färgen på hyperlänkar (t.ex. länkar i brödtext och länkar med visningsnamn).

* **textColor** *(CSS-färgsträng)* Färgen för brödtext.

* **titleFontSize** *(CSS Font Size String)* Teckensnittsstorleken för innehållsrubriker.

* **titleLineHeight** *(CSS Line Height String)* Radhöjden för innehållsrubriker.

* **sourceLogoColor** *(CSS-färgsträng)* Färgen för källlogotypen.

* **usernameColor** *(CSS-färgsträng)* Färgen för användarnamnen i bylinan.