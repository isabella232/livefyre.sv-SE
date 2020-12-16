---
description: För att autentisera en användare med Livefyre via ett flöde som inte aktiveras av en Livefyre-app, rekommenderar Livefyre att du implementerar metoden forEachAuthentication i ditt AuthDelegate-objekt.
seo-description: För att autentisera en användare med Livefyre via ett flöde som inte aktiveras av en Livefyre-app, rekommenderar Livefyre att du implementerar metoden forEachAuthentication i ditt AuthDelegate-objekt.
seo-title: Implementera SSO
solution: Experience Manager
title: Implementera SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
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

