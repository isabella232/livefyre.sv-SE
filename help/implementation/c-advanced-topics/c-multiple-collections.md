---
description: Visa flera samlingar på en sida.
seo-description: Visa flera samlingar på en sida.
seo-title: Flera samlingar
solution: Experience Manager
title: Flera samlingar
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

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
