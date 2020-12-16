---
description: Begränsa den typ av media som kommer in i appströmmen.
seo-description: Begränsa den typ av media som kommer in i appströmmen.
seo-title: Begränsa media
solution: Experience Manager
title: Begränsa media
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Begränsa media{#restrict-media}

Begränsa den typ av media som kommer in i appströmmen.

Som standard kan alla bifogade mediefiler bäddas in i appar. Med Livefyre kan du ändra det här alternativet för att hindra användare från att skicka valda bilagetyper till dina appar.

>[!NOTE]
>
>Livefyre samarbetar med Embeely för medieintegrering. Mer information finns i Innehållsintegrering > Egen integrering. Kontakta din tekniska kontohanterare för frågor om länkexpansion eller källor.

Det här exemplet blockerar YouTube och Vimeo-inbäddning från din kommentarström:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

När konversationen läses in:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

