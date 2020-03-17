---
description: Integrera en Sidenotes-app genom att följa en process som liknar Core Applications.
seo-description: Integrera en Sidenotes-app genom att följa en process som liknar Core Applications.
seo-title: Integrering av sidenotes
solution: Experience Manager
title: Integrering av sidenotes
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Integrering av sidenotes{#sidenotes-integration}

Integrera en Sidenotes-app genom att följa en process som liknar Core Applications.

Om integreringen av Core Application är slutförd kan koden som skrivits för att generera objektet återanvändas som `collectionMeta` Sidenotes.

Du kan också återanvända dina befintliga `auth` ombud genom att ange ett `auth` ombud som har skapats med `fyre.conv` till typografiska tecken i `authDelegate` fältet (valfritt).

>[!NOTE]
>
>Med sidenotes kan du inkludera `network`, `siteId`och `articleId` i ett enda objekt, i stället för att skicka dem separat i andra delar av konstruktorn.

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

Så som beskrivs i avsnittet Byggnad `collectionMeta` är `collectionMeta` ett kodat JSON-objekt. I exemplet ovan har JSON-objektet följande format innan det är JWT-kodat.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Mer information finns i `collectionMeta` token.

## Mobilinställningar

Sidenotes har optimerats för användning i mobila enheter. För bästa resultat med mobilversioner av Livefyre-appen ställer du in det skalbara alternativet för användare på Nej. Exempel:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
