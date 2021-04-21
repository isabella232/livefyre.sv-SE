---
description: Integrera en Sidenotes-app genom att följa en process som liknar Core Applications.
title: Integrering av sidenotes
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Sidenotes Integration{#sidenotes-integration}

Integrera en Sidenotes-app genom att följa en process som liknar Core Applications.

Om integreringen av Core Application är slutförd kan koden som skrivits för att generera `collectionMeta`-objektet återanvändas för Sidenotes.

Du kan också återanvända dina befintliga `auth`-delegater genom att ange ett `auth`-delegat som skapats med `fyre.conv` till signaturer i fältet (valfritt) `authDelegate`.

>[!NOTE]
>
>Med sidenotes kan du inkludera `network`, `siteId` och `articleId` i ett enskilt objekt, i stället för att skicka dem separat i andra delar av konstruktorn.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Som du kan se i avsnittet Building `collectionMeta` är `collectionMeta` ett kodat JSON-objekt. I exemplet ovan har JSON-objektet följande format innan det är JWT-kodat.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Mer information finns i `collectionMeta`-token.

## Mobilinställningar

Sidenotes har optimerats för användning i mobila enheter. För bästa resultat med mobilversioner av Livefyre-appen ställer du in det skalbara alternativet för användare på Nej. Exempel:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
