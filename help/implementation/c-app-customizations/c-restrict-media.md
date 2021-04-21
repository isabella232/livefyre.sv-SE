---
description: Begränsa den typ av media som kommer in i appströmmen.
title: Begränsa media
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Begränsa media{#restrict-media}

Begränsa den typ av media som kommer in i appströmmen.

Som standard kan alla bifogade mediefiler bäddas in i appar. Med Livefyre kan du ändra det här alternativet för att hindra användare från att skicka valda bilagetyper till dina appar.

>[!NOTE]
>
>Livefyre samarbetar med Embeely för medieintegrering. Mer information finns i Innehållsintegrering > Egen integrering. Kontakta din tekniska kontohanterare för frågor om länkexpansion eller källor.

Det här exemplet blockerar YouTube- och Vimeo-inbäddning från din kommentarström:

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
