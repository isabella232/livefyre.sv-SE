---
description: Tillåt användare att klicka sig igenom samlingar från en enda sidlayout och URL.
seo-description: Tillåt användare att klicka sig igenom samlingar från en enda sidlayout och URL.
seo-title: Ändra samling
solution: Experience Manager
title: Ändra samling
uuid: 69bafcc7-c55e-47d6-bc79-b0db80fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Ändra samling{#change-collection}

Tillåt användare att klicka sig igenom samlingar från en enda sidlayout och URL.

Använd Ändra samlingsdelegat för att ändra den samling som visas på en sida, utan att ändra URL:en, medan en Livefyre-app redan är inläst. Använd den här funktionen om du vill visa foto- eller videogallerier eller andra appar där den visade samlingen ska ändras efter en användaråtgärd.

Om du till exempel klickar på en video eller ett foto i ett galleri läses en samling som är specifik för den markeringen in, medan sidans URL inte ändras.

Så här läser du in en av tre samlingar från en sida med [kommentarantal](/help/implementation/c-advanced-topics/t-display-comment-count.md) :

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```

