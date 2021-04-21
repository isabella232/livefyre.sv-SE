---
description: Du kan logga in en användare via konsolen under integrering och testning för att felsöka auktoriseringen.
title: Felsöka Autentiseringsdelegering
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Felsöka Autentiseringsdelegat{#debugging-auth-delegate}

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
