---
description: Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
title: Pull Request Structure
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Pull Request Structure{#pull-request-structure}

Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.

Livefyre skickar en Pull-begäran till din URL.

Om t.ex. Pull-slutpunktens URL är:

```
https://example.yoursite.com/some_path/?id={id}
```

Livefyre Pull-begäran till denna slutpunkt kommer att vara:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

där `lftoken` är en JSON Web Token som signerats med din nätverksnyckel, och **[!UICONTROL {userAuthToken}]** är den användarauth-token som genereras av Livefyre.

1. Använd `lftoken` för att validera att begäranden till din Ping for Pull URL skickades av Livefyre och inte av en skadlig agent.
1. För alla inkommande begäranden:

   * Kontrollera att frågesträngen `lftoken` finns på begäran.
   * Använd metoden `validateLivefyreToken` i Livefyre-biblioteken för att kontrollera att `lftoken` har signerats med din nätverksnyckel.

   * Om `lftoken` inte är närvarande, eller misslyckas med valideringen, ska du inte tillåta slutpunkten att svara med profilinformation. Svara istället med en 403-statuskod (förbjuden) och inget svarstext.

1. `userAuthToken` genereras av Livefyre- `buildUserAuthToken` metoden för användaren med användar-id &quot;system&quot;. Den här användaren är den första användaren som skapas för varje nytt nätverk.
