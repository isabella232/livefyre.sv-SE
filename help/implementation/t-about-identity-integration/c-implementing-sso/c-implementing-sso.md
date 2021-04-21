---
description: För att autentisera en användare med Livefyre via ett flöde som inte aktiveras av en Livefyre-app, rekommenderar Livefyre att du implementerar metoden forEachAuthentication i ditt AuthDelegate-objekt.
title: Implementera SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implementera SSO{#implementing-sso}

För att autentisera en användare med Livefyre via ett flöde som inte aktiveras av en Livefyre-app, rekommenderar Livefyre att du implementerar metoden forEachAuthentication i ditt AuthDelegate-objekt.

Detta anropas när `authDelegate` skickas till `auth.delegate` och en autentiseringsfunktion skickas som kan skickas flera gånger. Den här metoden ger en inversion av kontrollen för autentiseringshändelser så att din `AuthDelegateobject` kan vara självständig utan att det krävs en global referens för autentisering.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre förlitar sig på användartokens för att koordinera autentiseringen. Detta token måste därför returneras av din identitetstjänst för att autentisera en användare med Livefyre. Mer information om hur du skapar en användartoken för Livefyre finns i Skapa en användarautentiseringstoken.

>[!NOTE]
>
>När inloggningen är klar skapar autentiseringen en session för användaren och försöker läsa in användarens session när sidan uppdateras och läses in igen. `auth.logout()` kommer att rensa den här sessionen. Detta innebär att det inte är nödvändigt att hantera en användares session oberoende av auktoriseringen.
