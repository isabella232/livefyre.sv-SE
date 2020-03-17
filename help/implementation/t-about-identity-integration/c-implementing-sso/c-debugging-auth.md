---
description: Du kan logga in en användare via konsolen under integrering och testning för att felsöka auktoriseringen.
seo-description: Du kan logga in en användare via konsolen under integrering och testning för att felsöka auktoriseringen.
seo-title: Felsöka Autentiseringsdelegering
solution: Experience Manager
title: Felsöka Autentiseringsdelegering
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Felsöka Autentiseringsdelegering{#debugging-auth-delegate}

Du kan logga in en användare via konsolen under integrering och testning för att felsöka auktoriseringen.

Logga in en användare via konsolen med följande `auth.authenticate` (token) och skicka en Livefyre-användartoken för att autentisera användare på sidan.

Du kan också ändra exemplet ovan och lägga till följande textutdrag direkt i JavaScript för att snabbt logga in en användare i Livefyre (kräver en referens till auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

