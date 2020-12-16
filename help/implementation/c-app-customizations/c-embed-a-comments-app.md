---
description: När du bäddar in kommentarappen följer du processen för att bädda in en Core-app.
seo-description: När du bäddar in kommentarappen följer du processen för att bädda in en Core-app.
seo-title: Bädda in en kommentarapp
solution: Experience Manager
title: Bädda in en kommentarapp
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Bädda in en kommentarsapp{#embed-a-comments-app}

När du bäddar in kommentarappen följer du processen för att bädda in en Core-app.

Inbäddning av appen Kommentarer följer processen för att bädda in en Core-app som beskrivs i [Bädda in en app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Exempel

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Så som beskrivs i avsnittet Building CollectionMeta är CollectionMeta ett kodat JSON-objekt. I ovanstående exempel har JSON-objektet följande format innan det är JWT-kodat:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

