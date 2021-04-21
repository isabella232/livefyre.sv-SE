---
description: Visa flera samlingar på en sida.
title: Flera samlingar
exl-id: 748b6ca6-635e-4bae-9b95-cfbd4651751f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# Flera samlingar {#multiple-collections}

Visa flera samlingar på en sida.

Du kan inkludera flera samlingar på en sida på webbplatsen. Om du till exempel vill publicera en händelse kan du ha en liveblogg eller chattdiskussion under evenemanget, med en separat app på sidan som visar relaterat kuraterat innehåll från sociala nätverk. Du kan också lägga till en kommentarapp under en artikel med en chatt till sidan.

Om du vill hämta flera konversationer på en sida lägger du till en eller flera konfigurationer i en array och skickar arrayen till load-anropet. Exempel.

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
